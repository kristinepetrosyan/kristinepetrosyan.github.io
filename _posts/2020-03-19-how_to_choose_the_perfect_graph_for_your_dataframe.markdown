---
layout: post
title:      "How to choose the perfect graph for your dataframe?"
date:       2020-03-19 16:18:17 +0000
permalink:  how_to_choose_the_perfect_graph_for_your_dataframe
---

I recently joined Data Science 10 months boot camp and already doing my first project. I am so excited!!!

Project is related to analyzing the movie industry and giving predictions how to enter to the market. I was given a data which was suppose to clean and work with. I learnt a lot on this project and I am excited to share some of the knowledge which I think will be helpful for new starters. I was confused initially which charts to use and how to do. They are so many and I was just trying to get the best for my data. Of course I tried all of them just to see how they look. So here we go.

There are tools like Matplotlib , Seaborn, ggplot and Plotly and they include: Column Chart, Bar Graph, Line Graph, Dual Axis Chart, Area Chart, Stacked, Bar Graph, Mekko Chart, Pie Chart, Scatter Plot Chart, Bubble Chart, Waterfall Chart, Funnel Chart, Bullet Chart, Heat Map.
When you start your project and try to show your work on the graph it can get overwhelming. So many questions come on your mind. What actually matters? How do you visualize the data so you can show the insights ?

The most important, how to make final charts for presentation and which ones are more efficient ?
Just to decide and understand what type of graph or chart or plot to use and why it takes so much time and slows down your analysis. In case you choose wrong visual aid or just running after most common type of chart could cause confusion with the person whom you are presenting or lead to faulty data interpretation. For this purpose you should first understand how to create charts that clarify and provide the right canvas for your data analysis. You should clarify the reasons why you need a chart. While choosing the chart you should first overview all different types of charts.

1.You should decide whether you want to compare values and if yes then go after one of these : Column, Mekko, Bar, Pie, Line, Scatter Plot or Bullet.

As an example we see seaborn barplot which is showing the comparison of net income and genre values.
```
import matplotlib.pyplot as plt
import seaborn as sns
fig, ax = plt.subplots(figsize=(18,15))
ax = sns.barplot(x="genre", y="net_income", data=df, color="Green")

ax.set_xticklabels(df['genre']
                  )
plt.title('Net income Distribution for Genres', fontsize=25)
ax.set_ylabel('Net Income', fontsize=20)
ax.set_xlabel('Genre', fontsize=20)
```

![]((home/angelo/Desktop/genre.png)
2.In case you want to show composition, use one of these: Pie, Mekko, Stacked Column, Stacked Bar, Area or Waterfall.
As an example we see Waterfall type of plot which is showing composition of sales and transactions.
```
import matplotlib.pyplot as plt
my_plot = trans.plot(kind='bar', stacked=True, bottom=blank,legend=None, title="2014 Sales Waterfall")
my_plot.plot(step.index, step.values,'k')
my_plot.set_xlabel("Transaction Types")
my_plot.yaxis.set_major_formatter(formatter)
```
![]((home/angelo/Desktop/waterfall2.png))
3.In case you want to understand the distribution of your data, outliers, the normal tendency, and the range of values then you should use one of these charts: Scatter Plot, Mekko, Line, Column, Bar, histogram.

As an example we can see a histogram which is showing runtime minutes distribution for movies which have high ratings. We see that 100 to 130 minutes are the highest in count.
```
import matplotlib.pyplot as plt
df[‘runtime_minutes’].hist(bins=10)
```

![](home/angelo/Desktop/hist.png)
Runtime minutes of movies

4. In case you want to know more information about how a data performed during a specific time period, then you are open to choose one of these charts: Line, Column, Dual-Axis-Line.
```
import matplotlib.pyplot as plt
import matplotlib.dates as mdatesfig
ax = plt.subplots()
ax.grid(True)year = mdates.YearLocator(month=1)
month = mdates.MonthLocator(interval=3)
year_format = mdates.DateFormatter('%Y')
month_format = mdates.DateFormatter('%m')ax.xaxis.set_minor_locator(month)ax.xaxis.grid(True, which = 'minor')
ax.xaxis.set_major_locator(year)
ax.xaxis.set_major_formatter(year_format)plt.plot(data_set.index, data_set['#Passengers'], c='blue')
plt.plot(decomposition.trend.index, decomposition.trend, c='red')
```

![](home/angelo/Desktop/data.png)

5. In case you want to understand the relationship and show how something positively effects, has no effect, or negatively effects another variable, then you should go for Scatter Plot, Bubble or Line Chart.

As an example we can see the relationship between net income and production budget and we can see positive relationship which means higher production budget is higher profits will be.

```
import matplotlib.pyplot as plt
df.plot.scatter(x='production_budget',
                      c='DarkBlue',
                      y='net_income',)
```
![](home/angelo/Desktop/scatter.png)

Hope this tutorial helped you understand more about charts and when to use them.

You can find this blog published on medium.com with following link https://medium.com/@kristinelpetrosyan/how-to-choose-the-perfect-graph-for-your-dataframe-1665ee469f8b
