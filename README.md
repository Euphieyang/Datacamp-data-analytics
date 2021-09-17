# Datacamp-data-analytics

## 0.1 Introduction to Python

**Learning Goal**
1. How to write and excecute Python code with DataCamp

2. How to load data from spreadsheet

3. How to turn data into beutiful plots

### Dive into Python
Two ways of executeing Code on DataCamp: IPython shell, script editor

* IPython shell

  * "the console"
  * type a line of code, use "return key" to execute it

* script editor

  * write mutiple lines
  
  * begins with "pound" or "hash"


  * use "Run Code" to execute them
  
**Module**

Groups related tools together, Ex: make bar chart, line chart, histogram

Before write code, we need to import moduels, otherwise, we can't use their tools

we can use alias to represent names of moduels 

> import _____ (名字一定要小寫)

> import (全名) as (縮寫)

* matplotlib: creat chart
* numpy:math operations on lists of data (np)
* pandas: load tabular data (加載表格數據)
* scikit-learn: perform ML
* scipy: caontain statistics
* nltk: works for text data
* statsmodles: used in ML (sm)
* seaborn: visulize library (sns)


### Creating Variables
we use variable in our code, it will be replaced with the original piece of data

This way provides us an easy-to-use shortcuts to a piece of data

We difine variable with equl size

* rules
  
  1. must start with a letter (usually lowercase)
  2. No space/ special chatacters
  3. my_car isn't equl with MY_CAR
  * Valid Variables: b, bayes42
  * Incalid_Variables: bayes-height, bayes!, 42bayes
  
* Types

  * Float
 
    represents an integer or decimal number
   1. height=24
   2. weight= 75.5
 
  * String

    represents text, letters, number, spaces, adn special characters
    
    we difine a string by putting '___'/"____" 
   1. name='Bayes'
   2. breed='Golden Retriever'

### What is pandas?

Panda is a module for working tabular data /w rows and columns(處理表格)

* Tools

  1. Loading tabular data from different sources (DataFrame)
  2. Search for particular rows and columns
  3. Calculate aggregate statistics (mean/ variance)
  4. Combining data from mutiple sources
  
* DataFrame: Tabuular data(表格數據)

  * Loading a CSV
  
    > import pandas as pd : 將數據加載到DataFrame
   
    > df=pd.read_csv('CSV檔案名') : CSV轉DataFrame,
   
    💡 df是自取的變數名,CSV是逗號分隔的值,將表格樹存為純文件版本,記得加引號
   
    > print(df) ➡ 列出全部DataFrame
   
  * Inspecing a DataFrame(表格)
 
    > df.head(none):顯示表格前五行 

    > print(df.head(none))
   
     💡 屬於DataFrame變量,df是自取的變數,可自行修改,只出現前五句,括號內不須填寫任何東西
  
     💡 head屬於dataframe變量,在句點之後出現在行的結尾= 方法(method)

    > df.info(none): 顯示表格資訊  
   
    > print(df.info(none))
   
     💡 有幾行幾列,資料類型
     
     💡 df是自取的變數,可自行修改,括號內不須填寫任何東西

### Selecting columns
   
Columns names are strings(includes spaces or characters)
   
1. variable= dataframe name['name of colunns']

   Ex: suspect=credit_records['suspect']
      
2. variable = dataframe name.name of column

   Ex: price=credit_records.price
         
* Common mistakes in column selection
   
     1. use brakets, qoutation and string for column names /w spaces or characters

       ⭕police_report['Is Golden Retriever?']
       
       ❌police_reprt.Is Golden Retriever?
       
     2. remember qoutation' ', otherwise, it may be recognized as variable

     3. use square brakets not paretheses, otherwise it may be recognized as function
       
### Selecting raws with logic
       
logical statements to check two values and return true/flase (booleans)ex: equl to/ greather than

💡row name with qoutation and square brakets

Ex: question=12*8
    solution=96
    question==solution  ➡ true
    
* Types of logic

  1. >
  2. >=
  3. <
  4. <=
  5. ==
  6. !=
  💡In dateframe, we can compare one value to all values
  
    > dataframe檔案名稱.row name > _____
    
    > credit_records.price>20.00
  
  💡 We can also select only the true statement
  
    > dataframe檔案名稱[檔案名稱.row name>____]

    > credit_records[credit_records.price>20.00]
     
      logical test: credit_records.price>20.00
      
    > credit_records[credit_records.suspect=='Ronald Aylmer Fishers']

    >mpr[mpr.['dog breed']!='Poodle']

### Creating line plots

In order to create line plots, we need to impord matplotlib

> from matplotlib import pyplot as plt

* Type 

1. >plt.plot(x_column name, y_column name)/ 

   >plt.plot(rasom.letter, rasom frequency)

    💡 Function name: plt.plot

    💡 First positional argument: rasom.letter
 
    💡 Second positional argument: rasom.frequency
 
2. >plt.show()

   不需要參數Argument,什麼都別打, 鍵入這個function, 繪圖就會在新窗口打開
   
   
3. >plt.plot(data1.x_values, data1.y_values)

   >plt.plot(data2.x_values, data2.y_values)

    💡兩資料繪製成一個圖表，Matplotlib會自動將兩線上不同的顏色(以此類推多個資料)

### Adding text to plots

When we show plots to our audience, we need to add a label to show what it importance is.


1. Axes labels(軸標籤)

   >plt.xlabel('___string name___')

   >plt.ylabel('___string naem___')

    💡 利用命令方式標記X/Y軸，將括號內填入字串，代表標籤
    
    💡 在輸入plt.show()之前
    
    
2. Title(圖標題)

   >plt.title('_____plot name____')

    💡 括號內填入圖表標題，參數(圖表)是字串符號
    
    💡 在輸入plt.show()之前
    
    
3. Legends(圖例)

   >plt.plot(aditya.days, aditya.cases, label='Aditya')

   >plt.plot(deshuan.days, deshuan.cases, label='Deshaun')

   >plt.plot(mengfei.days, mengfei.cases, label='Mengfei')

   >plt.legend()
   
    💡label= 在圖例中使用的字串
    
    💡要記得輸入plt.legend(),不然不會出現圖例,括號內不須輸入參數
    
    
4.Arbitrary text(注釋)

  >plt.text(xcord,ycord,'____Text message_____') 

  >plt.text(5,9,'Unusually low H frequency')

   💡this function includes three arguments: x座標, y座標, 顯示的文本(字串)
   
   💡在(5,9)標記 Unusually low H frequency
   
  
5. Modifying text

   * Change front size

     >plt.title('Plot title', frontsize=20)

   * Change front color

     plt.legend(color='green')
     
### Adding some style     

Let's make plots beautiful

1. Changing line color

   >plt. plot(x, y1, color='_____')
