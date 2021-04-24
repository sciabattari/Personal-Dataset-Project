# Scott Ciabattari's Personal Dataset Project

## Motivating Question
When I set out onto this project, I knew I wanted to do something about sports.  Sports have been a passion of mine for my entire life and it is what I plan on going into for my career. Once I knew I wanted to base my personal dataset around sports, I shifted to which sport I wanted to focus on.  Football was the obvious answer, and it was justified by the fact that the NFL offseason is upon us and in full swing.  I knew I wanted to focuz on the business side of sports with salary caps, so that is where my mind went next.  I have noticed a trend in the NFL recently and I pulled up a statistic to back up my claim. No team has ever won the Super Bowl with a Quarterback taking up more than 13% of the total cap space allowed. This statistic puzzled me, and I set out to look into the numbers behind it.  The motivating question I will be answering is: How does a Quarterback's salary impact the total wins a football team has in a year?

## Data Process
#### Sourcing
I obtained my data from <a href="https://overthecap.com/"> Over the Cap</a> [1], where I extrated the salary data for all NFL teams in the 2019 season.  I wanted to look at a recent season, but I was afraid to use the 2020 data because I felt it might've been scewed and out of line in recent years due to COVID.  Teams wanted to spend less money in 2020 due to a drop in the salary cap and less revenue coming in.  That is why I chose the 2019 season, as the more recent "normal" season.  From the data I extracted, I took and cleaned the data for Offensive spending (total money spent on the offense), Defensive spending (total money spent on the defense), and QB spending (total money spent on the Quarterback position) for all 32 NFL teams.  

#### Cleaning 
As I was adding my data into my dataset, it was clear that many things needed to be cleaned up.  I needed to get rid of all the commas in the numbers to help with the visualization section.  I also wanted to see the total amount spent by each team, and since <a href="https://overthecap.com/"> Over the Cap</a> [1] did not provide that number, I simply added my Offensive Spending and Defensive Spending columns together to get that number.  I also wanted to include percentages of how much the QB salary was related to my new total spendings columns.  I simply divided the two together, then rounded the answer and inserted % to all of them.  This gave me a more clear look at the statistic that started my motivating question in the first place and I found it very helpful. At this point I felt my data was ready to be implemented into RStudio for visualization

## Visualization
After I had completed the processing of my data, I took a step back and began to look at how I wanted to go about answering my motivating question.  My initial idea was to just look at how the QB% looked vs. Wins and I came up with this visualization. 
![QB% VS. Wins](https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%2011.42.06%20AM.png)
While this visualization was important and there seemed to be a slight trend line, it did not factor in the the total amount spent by each team.  I feel that the total amount spent is very important to understanding how teams operate their salary caps and I wanted to include that.  This visualization was also hard to read and quite messy so I began to look elsewhere.  In order to factor in all the data points I wanted, I began to think of using a scatter plot.  From there, I debated between looking at QB% vs. Offensive Spending or QB% vs. Total Spending.  This would give a different idea of how teams operate their cap space.  So I looked at the two figures side by side to see the differences. I also added an Offensive Spending vs. Defensive Spending to see if that figure gave me any room for analysis as well.
<table>
  <tr><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%2012.32.22%20PM.png"></td><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%2012.32.30%20PM.png"></td><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%2012.54.30%20PM.png"></td></tr>
   <tr><td>QB% vs. Total Salary Spent</td><td>QB% vs. Offensive Players Salary </td><td>Offensive Spending vs. Defensive Spending</td></tr>
  </table>
These visualizations gave me a new perspective on how the salary cap works. It became clear that teams are prioritizing different things depending on their individual strategies and each strategy would yield a different result. I did find it interesting how the graphs variated between looking at QB% vs Total and Offensive salaries.  They were similar, but it seemed that total was more compact while offensive was more spread out.  This could be due to some teams prioritizing or ignoring defense while keeping similar total numbers. 

## Analysis



<table>
  <tr><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%2011.42.53%20AM.png"></td><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%201.14.35%20PM.png"></td><td><img src="https://raw.githubusercontent.com/sciabattari/Personal-Dataset-Project/main/Visualizations/Screen%20Shot%202021-04-24%20at%201.19.10%20PM.png"></td></tr>
   <tr><td>Clustering of QB% vs. Total Salary</td><td>Clustering of QB% vs. Offensive Salary</td><td>Clustering of Offensive vs. Defensive Salary</td></tr>
  </table>
