
# Which team was statistically more dominant: the 1995–96 Bulls or the 2016–17 Warriors? 

  ##   Problem Definition
Dominance. Dominance is the state or condition of having power, authority, control, or a leading position over others. Being dominant is having power over others. Being a dominant team is outperforming opponents, achieving big results through unmatched skill and dedicating how a game unfolds rather than the opponents. In basketball being dominant is a way to become one of the best players in the league like Shaq, Jordan, Lebron, Curry and others all were one of the most dominant players in their era. Being a dominant team is a way to become the best team ever in general like the 86 celtics, 01 lakers, 96 bulls, 17 warriors and more. The 95 - 96 bulls is the most dominant basketball team ever; until in 2016/17 the warriors stepped in. Now most fans are debating which team is the most dominant? In this project I'm going to statistically find out which team is the most dominant; the 96 bulls or the 17 warriors. 

## Data Description
To find out which team was the most dominant I have to use stats that make a team the most dominant. I use the variables of the average points, assists, rebounds, steals, blocks, Fg% (field goal percentages), and Opp_Fg%(opponents field goal percentages) in that season. Points, assists, rebounds, steals, and blocks are the five most important basketball stats ever. Fg% and Opp_FG% are stats that find out through all the points, is the team consistent in their scoring (Fg%) and how does their defence contribute to the opponents scoring (Opp_Fg%).The data used in this project comes from the [sportsradar](https://developer.sportradar.com/basketball/reference/nba-seasonal-statistics) (Sportsradar, n.d.) website that gives api’s on nba stats. I used it for the warriors only because that website only had seasons from 2013-2026. I got the Bulls stats from the [basketballreference](https://www.basketball-reference.com/teams/CHI/1996.html) (Sports Reference LLC, n.d.) website. The data set is 2 rows and 8 columns long. Each row represents an individual team's per-game averages for a single regular season.

## Data Cleaning and Preparation
First I created a dataset to make all my variables as columns and the teams to be my rows. I started modifying my dataset using pandas dataframe (df = pd.DataFrame). For the warriors data I use the API that the website gave me using “import requests”, plugged in the stats that I needed. One thing I could find was the 96 bulls API. I tried everything to find it. Some of the websites wanted money for their API key and others didn't have those seasons back in those days. So what I did was go to the basketball reference website; they only had their total season stats so I plugged the stats in my df and divided all the stats by 82 because that's how many games they played that season.i also rounded the stats by 2 to make the df cleaner ('Points':[115.9,round(8625/82, 2)]) except the fg and opp_fg because its percentages 

## Data Visualizations and Insights:
<img width="1189" height="590" alt="output" src="https://github.com/user-attachments/assets/b8176345-9ec7-4de8-87cc-3d6ef0223daf" />
I used a barplot to examine and compare their average stats of the season. As you can see the warriors have a higher value in all of the stats except for rebounds. The warriors don't overtake them in value, the bulls do put in a competition in most of them. 
<img width="790" height="590" alt="fg%" src="https://github.com/user-attachments/assets/fa1999f2-dcaa-425b-bf3e-dcb765154961" />
However, making another barplot for the percentages we see that the warriors have a better field goal percentages and less opponent field percentage which is better than having more.

## Storytelling and Narrative
In the visualizations we see that the warriors overtake the bulls in most of the stats making this debate less debatable almost overtaking them in the top best stats in basketball and having a better field goal and opponent field goal percentage which describes how dominate their defence was compared to the bulls which the bulls did have one of the best defenders all all time like Scottie Pippen and Micheal Jordan. I honestly think based on this; this does conclude who was the most dominant team ever, and it's the 2016-17 Golden State Warriors.

## Limitations, Ethics, and Reflection:
The different eras really did a toll on this data. Between 1996 and 2017, the evolution of teams playstyles  and the 3 point revolution is a massive difference. It’s more fast pace and the 3 pointer is used way more in 2017. Some biases that exist in this data is not including the post season. Relying solely on regular season averages overlooks playoff dominance which both of them had which did lead both of them to a championship that year. Also the API availability shows how the warriors data was pulled via the Sportsradar API whereas the bulls data was manually pulled due to modern API date range limits. While the math was verified, comping data from those could include potential minor reporting conflicts. If i had more time and data i would've definitely explore on their postseason stats and their average stats but not including their mvp that year(Stephen Curry, Micheal Jordan) to see the differences 


Code:
Click here to access my code for this project

Reference and transparency:

Data sets: Sportsradar. (n.d.). NBA seasonal statistics API. Sportsradar Developer Portal. https://developer.sportradar.com/basketball/reference/nba-seasonal-statistics

Sports Reference LLC. (n.d.). 1995-96 Chicago Bulls roster and stats. Basketball-Reference.com. https://www.basketball-reference.com/teams/CHI/1996.html

Ai tool: I use copilot ai to make a bar plot for the percentages and I use google gemini to help me make a more detailed research question and to problem solve for my visuals as well. 


