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
we use vailables in our code, it will be replaced with the original piece of data

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
