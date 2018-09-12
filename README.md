# 100-days-of-ML-Challenge
100 days of Machine Learning coding challenge as proposed by Siraj Raval

## Day 1: Exploring and Understanding data

### Measuring spread – variance and standard deviation

Distributions allow us to characterize a large number of values using a smaller number of parameters. The normal distribution, which describes many types of real-world data, can be defined with just two: center and spread. The center of normal distribution is defined by its mean value, which we have used earlier. The spread is measured by a statistic called the standard deviation.In order to calculate the standard deviation, we must first obtain the variance, which is defined as the average of the squared differences between each value and the mean value. In mathematical notation, the variance of a set of n values of x is defined by the following formula. The Greek letter mu (similar in appearance to an m or u) denotes the mean of the values, and the variance itself is denoted by the Greek letter sigma squared (similar to a b turned sideways).

The standard deviation can be used to quickly estimate how extreme a given value is under the assumption that it came from a normal distribution. The 68-95-99.7 rule states that 68 percent of the values in a normal distribution fall within one standard deviation of the mean, while 95 percent and 99.7 percent of the values fall within two and three standard deviations, respectively. 

Applying this information to the used car data, we know that since the mean and standard deviation of price were $12,962 and $3,122, respectively, assuming that the prices are normally distributed, approximately 68 percent of cars in our data were advertised at prices between $12,962 - $3,122 = $9,840 and $12,962 + $3,122 = $16,804.

In the scatterplot we obtained via the code(in folder: Day1), the relationship we found between car prices and mileage is known as a negative association, because it forms a pattern of dots in a line sloping downward. A positive association would appear to form a line sloping upward. A flat line, or a seemingly random scattering of dots, is evidence that the two variables are not associated at all. The strength of a linear association between two variables is measured by a statistic known as correlation.

### Two-way cross-tabulations: Examining Relationships

To examine a relationship between two nominal variables, a two-way cross-tabulation is used (also known as a crosstab or contingency table). A cross-tabulation is similar to a scatterplot in that it allows us to examine how the values of one variable vary by the values of another. The format is a table in which the rows are the levels of one variable, while the columns are the levels of another.

There is a wealth of data in the CrossTable() output. The legend at the top (labeled Cell Contents) indicates how to interpret each value. The rows in the table indicate the three models of used cars: SE, SEL, and SES (plus an additional row for the total across all models). The columns indicate whether or not the car's color is conservative (plus a column totaling across both types of color). The first value in each cell indicates the number of cars with that combination of model and color. The proportions indicate that the cell's proportion is relative to the chi-square statistic, row's total, column's total, and table's total.What we are most interested in is the row proportion for conservative cars for each model. The row proportions tell us that 0.654 (65 percent) of SE cars are colored conservatively in comparison to 0.696 (70 percent) of SEL cars and 0.653 (65 percent) of SES. These differences are relatively small, suggesting that there are no substantial differences in the types of colors chosen by the model of the car.


## Day 2:

### Lazy Learning: Nearest Neighbour 

Its a method to measure the similarity of two examples using distance. Despite the simplicity of this idea, nearest neighbor methods are extremely powerful. They have been used successfully for:
1. Computer vision applications, including optical character recognition and facial recognition in both still images and video
2. Predicting whether a person will enjoy a movie or music recommendation
3. Identifying patterns in genetic data, perhaps to use them in detecting specific proteins or diseases

The k-NN algorithm treats the features as coordinates in a multidimensional feature space. Traditionally, the k-NN algorithm uses Euclidean distance, which is the distance one would measure if it were possible to use a ruler to connect two points.
Euclidean distance is specified by the following formula, where p and q are the examples to be compared, each having n features. The term p1 refers to the value of the first feature of example p, while q1 refers to the value of the first feature of example q:

dist(p,q)=sqrt[(p1-q1)^2+(p2-q1)^2+....+(pn-qn)^2]

### Choosing an appropriate k

The decision of how many neighbors to use for k-NN determines how well the model will generalize to future data. The balance between overfitting and underfitting the training data is a problem known as bias-variance tradeoff. 
In practice, choosing k depends on the difficulty of the concept to be learned, and the number of records in the training data. One common practice is to begin with k equal to the square root of the number of training examples. 
