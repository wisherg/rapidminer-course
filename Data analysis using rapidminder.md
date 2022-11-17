# Data analysis using rapidminder



* I'm sorry for that there isn't a class  face to face with you.   self-discipline is important for online class!

* my name: wang peng

* contact: dingding or tell:18858158273

* score： class assignment or homework  50% ;the final projects 50% 

* how to do classwork

* Welcome for any question


## Lesson One

### introduction

1, data analysis is important, no matter what major you are

2, data analysis tools: python or rapidminder.     python is powful but rapidminder is easier to use

### installtion
https://my.rapidminer.com/nexus/account/index.html


### open a sample data:

* out, res

### how to use the document of rapidminder

### the data

* In most case, the data is a two-dimensional table:   row/ columns;   example(entity)/attribute(feature);

* data type:  Numerical   Binominal   polynominal  real  date integer text

  there is the same data type in the values of one columns/attribute.
  
  
  

### open a local data

### the location of rapidminder

C:\Users\wp\Documents\RapidMiner\Local Repository\processes

* alibabadata

* this data "t_alibaba_data3" is got from Ali-tianchi Data competitions  https://tianchi.aliyun.com/ and contain the record of actions in Tmall. 

* There are four columns: 

  user(user ID),brand(brand ID on Tmall), 

  behavr(four type of behavior: 0 browsing the brand; 1 buying; 2 Adding to wishlist; 3 adding to cart)

  date

  * classwork 1.1

  * 1 import the alibaba data from local/change the col name/
  
  * 2 import the titanic data from sample
  
    

###  Select Attributes 

###  Generate Attributes    

* classwork 1.2
* 1 rename the alibaba data and show the result
* 2  select one attribute; select two attributs from alibaba data
* 3  Generate  a new Attributes named date1 and add the year 



### convert type

### Filter Examples   

* condition class : expression; custom_filter

 ### Filter Example Range      

### sort

* classwork2.1
* 1 convert the type of the new attributes to date type, delete the orign "date" columns and store in the data repository
* 2 select the date of all the purchase recorder of  the user  10944750  (expression/custom_filter)
* 3 sort the data by the date and show the earliest 5 recorder 

### Aggregate 

https://gitee.com/wing2004/data-analysis-by-rapidminder/blob/master/timg.jpg

the most useful function in data analysis——Aggregate （groupby）

By “Aggregate” we are referring to a process involving one or more of the following steps:

* Splitting the data into groups based on some criteria.

* Applying a function to each group independently.

* Combining the results into a data structure.



* classwork 2.2
* 1 the number of records for each brand
* 2 the number of browsing records for each brand
* 3 the number of buying record for each usber



### change the columns type and the problem of the aggregate result in last class

* understand the sort of nominal and numerical
* edit imported data



* classwork 3.1
* 1  get the user whose purchase number is above 20
* 2  the number of records for each brand and each kind of behavior
* 3  get the top 5 brands of sales

### plot——line, bar，pie

* classwork 3.2

* 1 the number of records of different behavr and plot the line and bar figure

* 2 the distribution of the number of buying record for each brand and plot the log-log figure for it

  

### Aggregate for time

* classwork 3.3
* 1, the number of buying record for each date and plot the line figure
* 2, the number of buying record for each date in May and plot line figure
* 3,  the number of buying record for each month and plot the line figure

###  Pivot

​             The Pivot Operator creates a *pivot table*, summarizing the  data in a larger table by reorganizing it into groups and calculating   sums, averages, or other statistics for each group.  

* classwork 4.1
* 1, the number of records of different behavr for each brand by groupby
* 2, the number of records of different behavr for each brand by pivot and compare the result between question 1 and 2
* 3, calculate the conversion rate (the number buying / the number browsing)
* 4, plot the scatter figure for the number buying and the number browsing

###  De-Pivot   and  Transpose    



regular expression

https://www.runoob.com/regexp/regexp-tutorial.html

https://c.runoob.com/front-end/854/

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions



   * classwork 4.2  
   * 1, the number of records of different behavr for each brand by pivot and De-Pivot the four behavr_count col
   * 2, get the number of records of different behavr for each brand by pivot and transpose it

## append and join

* classwork 4.3
* 1  get the number of records of each date and then Generate three new Attributes  which contain day, month , week  
* 2, filter example by month =4 and month =6 and append this two result, then plot the line figure using day as x and count as y

### count（xxx）_? problem for mac 



* classwork 5.1

* 1, join the two result above question and plot the two line figure using day as x and count as y1 and y2 (one to one)
* 2, get the number of records of each date and join the result into the origin alibaba_changed data (one to many)

## A new data :  shoes

this data contain 5000 shoes which comes from the taobao Search Results.  the attribute named as info~ is the features of those shoes as we can see in the taobao.com

 important attribute:  prices, sales, location, nick

"nick" is the nick name of the shop the shoes belong to



### replace/ split / wirte

* classwork 5.2
* 1, for col "sales",  replace the "人付款" by ""  
* 2, for location,  split it with " "  
* 3, generate a new col for the right city
* 4, generate gmv (sales* price) col
* 5, save the new changed data.



## Aggregate / sum average

* classwork 5.3
* 1,the number of "info.鞋面材质" and plot the bar figure for top 10 
* 2, the sales, the gmv, the average price, the number of "info.鞋面材质" and plot the figure
* 3, get the gmv of different  "info.鞋面材质" for each shop by pivot



### plot--histogram / distribution

* the distribution for integer and real
* classwork 6.1
* 1,  the distribution of sales of shoes in data in log-log plot
* 2,  plot the price distribution and histogram of shoes 

## quartile and boxplot

* quartile: min  25%  median  75%  max

* classwork 6.2
* 1，plot the price boxplot for "info.鞋面材质"
* 2，get all the recorder of top 5 "info.鞋面材质"  and plot the price boxplot for top 5 "info.鞋面材质"

### parallel coordinate

* classwork 6.3
* 1, the gmv, the average of gmv, the average price, the number of shoes，the sales, the average of sales for different shops
* 2, get the gmv top 5 shops and normalize the attribute and plot the parallel coordinate

### Scatter scatter_matrix and sunburst

* classwork 7.1
* 1, basing on the result of 6.3 and plot the scatter and the scatter_matrix for different nick and the Bubble
* 2 the gmv for each info.功能 info.鞋头款式 info.鞋面内里材质 info.鞋面材质 nick
* 3 choose the top 5 gmv shopes and plot the sunburst by the result above of top 5

### Choropleth map and Map operator

* classwork 7.2
* 1, get the number of shoes for different province 
* 2, try to plot the choropleth map and fix the problem by the map operator

### Choropleth map, point map and join operator

* data-2017city
* classwork 7.3
* 1, get the number of shoes for different province
* 2, plot the Choropleth map  by join these two data
* 3   get the number of shoes for different city and plot the point map

# Machine learning by rapidminer

### the iris data  and classification in rapidminer

### operator : split data and apply model 

* classification is one of important kind of Machine learning algorithms 
* the type of columns： label  id  att



```
'feature_names': ['sepal length (cm)',
  'sepal width (cm)',
  'petal length (cm)',
  'petal width (cm)'],
  iris数据集是用来给花做分类的数据集，每个样本包含了花萼长度、花萼宽度、花瓣长度、花瓣宽度四个特征（前4列）
```

* classwork 8.1

* 1,  plot the scatter figure for different type of iris

* 2, train a classification model by Decision tree

  

* classwork 8.2

* 3, split the data and apply the model on the rest

* 4, validate the model by the operator performance

### the alibaba_data and classification

* predict whether a user would purchase a brand ; how many times user browse the brand/ add to cart / add to wishlist

* in this question,  what is the example?

* data preparation

  

* classwork 8.3

* 1, change the type of columns to nominal and pivot it (group  by user and brand; column grouping the behavr)

* replace the miss value in above result

* change the col count(XXX)_1 to binominal and set it to label

  

* classwork 8.4

* 1, train a classification model by Decision tree for the alibaba_data

* 2, split the data and apply the model on the rest

* 3, validate the model by the operator performance(binominal)

### Churn Modeling——Customer Data /Subprocess/ rebalance/ Cross Validation

a customer dataset that contains customer attributes like:
- Age
- Technology used (4G, fiber, etc.)
- Date since he/she is a customer
- Average bill last year
- Number of support calls
- Did he/she abandon last year?         

### f measure      

F-measure provides a way to express both concerns with a single score. Once precision and recall have been calculated for a binary or multiclass classification problem, the two scores can be combined into the calculation of the F-Measure. The traditional F measure is calculated as follows: This is the harmonic mean of the two fractions.

​        F1 = 2 (precision * recall) / (precision + recall) = 2TP / (2TP + FP + FN)      

* classwork 9.1
* 1 import the data from "Samples/Templates/Churn Modeling/Customer Data" 
* 2  set the ChurnIndicator columns to label and change it to Binominal  and put these two operator into subprocess
* 3,  plot the Scatter figure and watch the influencing factor.
* 4,  train a classification model by Decision tree for this data and validate the model by the operator performance(binominal)（f measure）

#### Cross Validation

​        The input ExampleSet is partitioned into *k* subsets of equal  size. Of the *k* subsets, a single subset is retained as the         test data set (i.e. input of the Testing subprocess). The remaining *k - 1* subsets are used as training data set (i.e. input of the   Training subprocess). The cross validation process is then repeated *k*   times, with each of the *k* subsets used exactly once as the  test data. The *k* results from the *k* iterations are  averaged (or otherwise combined) to produce a single estimation. The  value *k* can be adjusted using the *number of folds* parameter.     

https://blog.csdn.net/weixin_39942397/article/details/111698335 

* classwork 9.2
* 1, use operator Cross Validation to validate this model

#### rebalance

Many more customers stay than churn (hopefully!). In order for our model to learn how churners behave, we re-balance the data to focus on the case we're interested in. This is like a magnifying glass on churn!

* classwork 9.3
* 1 use the operator Sample to re-balance the data
* 2, train  the new model base on the re-balanced data



### Cross Validation and rebalance on the alibaba_data

* classwork 9.4

* plot bar fig on the number of true and false recorder
* train a model and get the f measure 
* re-train new model with Cross Valiation and rebalanced data and get the f measure

## direct marketing

Create a customer response model based on past responses to targeted marketing campaigns, in order to predict those customers that are likely to respond to and increase the conversion rate of new campaigns.

difference between past data and new data

#### get the weights for each columns by Decision Tree

select attribution by weights

* classwork 10.1
* 1  import past campaign data; remove the columns name; multiply the data
* 2, using operator " Weight by Information Gain "  get  the weight for each columns
* 3, split data; train a model using Decision Tree; validate it by f1; get the weights for each columns by this model
* 4, remove the least weight; tarn a model again; compare the scores

#### feature weights in rapidminer    

### Find Threshold

Typically, omitting recipients that would have responded, incurs a higher cost than sending a campaign to somebody who does not respond. Accounting for those costs, calculate and apply the optimum confidence threshold.  

Specify the costs of missing a potential respondent vs. the costs of including somebody into the campaign 

* classwork 10.2
* 1，Use operator Cross Validation to get a Decision Tree model；validate this model by the operator performance(binominal) 
* 2, Using find Threshold operator, specify the costs of missing a potential respondent vs. the costs of including somebody into the campaign. get the Threshold and apply the threshold on the new data    

### weight and threshold on alibaba data

* classwork 10.3
* 1. show the weight of att by the ways above
* 2, Using find Threshold operator and get the Threshold and apply the threshold on the test data and show the change of f1-scores 
     

## CREDIT RISK MODELING

Predict the risk of counterparty credit default by training a Support Vector Machine (SVM) model on credit default data, optimizing its core parameters C and gamma and scoring risk on new data.

For the firms where a default observation is missing, the default risk should be predicted.

### the optimization operator

 This optimization operator  finds the optimal values of the selected parameters for  the Operators in its subprocess.      

This optimization operator varies the important SVM parameters C and gamma to return a model with maximum prediction accuracy.

* classwork 11.1
* 1 import  the Counterparty Risk Data ;  set the role;  split data into those rows that have a label value and those where the label value is missing;  remove the labels columns for the exampleSets which should be used to predict the default risk 
* 2, Use operator Cross Validation to train a Support Vector Machine (SVM) model 
* 3 Use the optimization operator varies the important SVM parameters C and gamma to return a model with maximum prediction accuracy;  Using the optimized SVM model, predict the likelihood of credit default.

* classwork 11.2
* 1,  using operator " Weight by Information Gain "  get  the weight for each columns
* 2,  replace the SVM to a tree decision model 
* 3 , Using find Threshold operator, specify the costs.   get the Threshold and apply the threshold on the new data

* classwork 11.3

1, Use the optimization operator on alibaba-data


## MARKET BASKET ANALYSIS

Model associations between products by determining sets of items frequently purchased together and building association rules to derive recommendations.

The data denotes how many times a certain product has been purchased as part of a transactions

**Support**  **Confidence**   **Lift**

https://www.kdnuggets.com/2016/04/association-rules-apriori-algorithm-tutorial.html

* classwork 12.1
* import transaction data; Aggregate transaction data via concatenation so that the products in a transaction are in one entry, separated by the pipe symbol
* rename the concatenation columns and set the Invoice columns to  id
* Using FP-Growth, determine frequent item sets. A frequent item sets denotes that the items (products) in the set have been purchased together frequently, i.e. in a certain ratio of transactions. This ratio is given by the support of the item set.（min-support 0.005）
* Create association rules which can be used for product recommendations depending on the confidences of the rules.(min confidence 0.1)

### the alibaba_data and associations analysis

* classwork 12.2

* import alibaba data and get all purchasing recorder

* groupy by user and brand to remove duplicate records; Aggregate transaction data via concatenation  so that the brands in a transaction are in one entry

* rename the concatenation columns and set the user columns to  id

  

* classwork 12.3

* Using FP-Growth, determine frequent item sets; Create association rules

##         the iris data  and clustering in rapidminer      

the difference between clustering and classification

clustering don't need label

### k-means

​        The k-means algorithm determines a set of *k* clusters and  assigns each Examples to exact one cluster. The clusters consist of  similar Examples. The similarity between Examples is based on a distance measure between them.      

* classwork 13.1

* import iris data and train a classification model by  Random Tree  
* remove the label column and clustering it by k-means
* visualize  the cluster by Cluster Model Visualizer             

### Cluster time series data

price data for the German DAX 30 stocks - by standardizing each series and finally clustering the series using X-Means to account for price risk relationships.

* classwork 13.2
* 1 import the data; visualize the time series ; Set the date column to role ID
* 2 Standardize each price time series, i.e. perform a Z-transformation of the values so that they have a mean of 0 and a standard deviation of 1 afterwards.; then visualize the changed time series and compare it with before
* 3  Transpose data set (so that each time series is a row now)
* classwork 13.3
* 1, cluster the data by k-means so that each series falls into one cluster.
* 2, visualize  the cluster by Cluster Model Visualizer 
* 3,  visualize the time series of different cluster



## final work

* 70% classwork must be finished， more is good
* choose the data from the "dataforclass"; if you want other data, let me know first.
* write a data analysis report which should be a doc file and the rapidminer rmp file
* at least five different figure which must be illustrated. more is better
* in order to analysis this data, at least one Machine learning model is trained and should be validated. more is better
* there should be adequate description of Data analysis. 
* data analysis tools must be rapidminer. other tools is unacceptable. 

## regression

the difference between regression and classification

* classwork 14.1
* 1 import the Polynomial data and train a tree model by this data to predict the value of label
* 2, Use operator Cross Validation to train a tree model.
* 3, Use the optimization operator varies the parameters and try to get a better model.

### regression on new alibaba_data 

new alibabadata come from

https://tianchi.aliyun.com/competition/entrance/231522/introduction

behavior_type分为1浏览（b），2收藏，3购物车，4购买(four type of behavior: 1 browsing the brand; 2 Adding to wishlist; 3 adding to cart; 4 buying)



* classwork 14.2

* 1 import u_i_tabel_isin.csv ;   change the type of columns to polynomial ; Generate a new Attributes base on "time"  which contain the date  

* 2,  make the sales number for each category of the day 17 as label

*  3, make the number of behavior for each category of the day 16 as the attributes

* classwork 14.3
* 1, join the label and attributes and rain a tree model 



* classwork 15.1

* 1,  define a subprocess which contain the core process above; using this subprocess generate the data in 18 
* 2,  use the model to predict the sales number of the day 18  and validate this result by performance operate

### how to get more example and more attribution

* classwork 15.2
* 1, using loop operator get the data of different date
* 2, get more example by Sliding window 
* 3 , train model on new data and validate it

* classwork 15.3
* 1, the sales number for each category of the day 17 is label; make the number of behavior for each category of the day 15 and 16 as the attributes
* 2, train model on new data and validate it



​      

