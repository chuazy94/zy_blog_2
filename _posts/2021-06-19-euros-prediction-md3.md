---
layout: post
title: Our Euro 2020 Predictions Matchday 3
---

<p align = "center">
  <img src = "{{ site.baseurl }}/images/germany_portugal.png">
</p>
<p align = "center">
The Germans were back to their best with an impressive performance against the Portugese with a man of the match performance from Robin Gosens. They may top the group with a convincing performance against Hungary.
</p>

Following a not so successful 2nd round (5/12 outcomes predicted correctly and only 1 exact scoreline), we will be adopting a newer approach to our predictions. We all knew that exact score predictions were going to be very difficult so we are adopting a probability based approach to determine the most likely outcome of the match. Layering this with some of our opinion of the games, we will derive a final predicted result.

### A New Method - Poisson

Due to the randomness of the beautiful game, it is already a tall order to predict the exact score of the game. A goal in a match does not depend on previous goals or any other factors. With this, we turn to statistics in an attempt to predict the most probable outcome of the game. Fortunately, there is a distribution that follows the nature of this random occuring events and that is the Poisson distribution. In the graph below created by <a href="https://dashee87.github.io/">David Sheehan.</a>, we can clearly see that the goals per game follows a Poisson distribution.  

<p align = "center">
  <img src = "{{ site.baseurl }}/images/poisson_david_sheehan.png">
</p>
<p align = "center">
The actual goals scored by English Premier League teams (Home and Away) versus the Poisson distribution of goals scored. All credits of this image goes to <a href="https://dashee87.github.io/football/python/predicting-football-results-with-statistical-modelling/">David Sheehan.</a> 
</p>

With this, we are able to convert a single average value into a probability for changeable outcomes. We employed our weighted Expected Goals (xG) as the single average value used in the Poisson Distribution per team and calculated the distribution of goals scored in a game for each respective team. Following which, a score matrix emerges which tells us the probability of goals scored for each respective team. The probabilities are multiplied with each other to create the score matrix and we will be able to identify the "most probable" outcome. However, we should not be distracted by the most probable score because most of the probabilities are really close to each other. What would give us more confidence in are the specific outcomes - Win/Draw/Lose, Team A/B winning by more than 2 goals or if a game is likely to be high scoring.  For more details, please check out this <a href="https://help.smarkets.com/hc/en-gb/articles/115001457989-How-to-calculate-Poisson-distribution-for-football-betting">post</a> from Smarkets! 

As always, there is a huge cavaet when predicting scores like this as it is very dependent on the average value we put into the distribution for each team. The weighted xG is very much a form dependent metric and a team may completely over or underperform their xG values. We also recognised that Home ground advantage plays a very important role in this tournament. Of the 8 games which were played by a team in their Home stadium, there were 4 victories, 3 draws (including the impressive 1-1 draw between Hungary and France) and only 1 loss (Denmark lost 2-1 to Belgium). The weighted xG does not take this into account due to a lack of Home and Away matches data but we will factor this into our final predictions.

### Group A: Italy vs Wales (Home Advantage)
<em>Weighted xG (<span style="color:blue">2.10</span> - 1.42) /
<em>Weighted xGA (<span style="color:red">0.611</span> - 1.86)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Italy goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Wales Goals</strong></td>
      <td>Poisson for # of goals per team</td>
      <td>12.28%</td> 
      <td>25.75%</td>
      <td>27.01%</td>
      <td>18.88%</td>
      <td>9.90%</td>
      <td>4.15%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>24.28%</td>
      <td style="background-color:#ffe0b3">2.98%</td>
      <td style="background-color:#b3ffb3">6.25%</td>
      <td style="background-color:#b3ffb3">6.56%</td>
      <td style="background-color:#b3ffb3">4.58%</td>
      <td style="background-color:#b3ffb3">2.40%</td>
      <td style="background-color:#b3ffb3">1.01%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>34.37%</td>						
      <td style="background-color:#FFCCCC">4.22%</td>
      <td style="background-color:#ffe0b3">8.85%</td>
      <td style="background-color:#b3ffb3"><strong>9.28%</strong></td>
      <td style="background-color:#b3ffb3">6.49%</td>
      <td style="background-color:#b3ffb3">3.40%</td>
      <td style="background-color:#b3ffb3">1.43%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>24.32%</td>						
      <td style="background-color:#FFCCCC">2.99%</td>
      <td style="background-color:#FFCCCC">6.26%</td>
      <td style="background-color:#ffe0b3">6.57%</td>
      <td style="background-color:#b3ffb3">4.59%</td>
      <td style="background-color:#b3ffb3">2.41%</td>
      <td style="background-color:#b3ffb3">1.01%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>11.48%</td>					
      <td style="background-color:#FFCCCC">1.41%</td>
      <td style="background-color:#FFCCCC">2.96%</td>
      <td style="background-color:#FFCCCC">3.10%</td>
      <td style="background-color:#ffe0b3">2.17%</td>
      <td style="background-color:#b3ffb3">1.14%</td>
      <td style="background-color:#b3ffb3">0.48%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>4.06%</td>												
      <td style="background-color:#FFCCCC">0.50%</td>
      <td style="background-color:#FFCCCC">1.05%</td>
      <td style="background-color:#FFCCCC">1.10%</td>
      <td style="background-color:#FFCCCC">0.77%</td>
      <td style="background-color:#ffe0b3">0.40%</td>
      <td style="background-color:#b3ffb3">0.17%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>1.15%</td>												
      <td style="background-color:#FFCCCC">0.14%</td>
      <td style="background-color:#FFCCCC">0.30%</td>
      <td style="background-color:#FFCCCC">0.31%</td>
      <td style="background-color:#FFCCCC">0.22%</td>
      <td style="background-color:#FFCCCC">0.11%</td>
      <td style="background-color:#ffe0b3">0.05%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Italy Win</td>
      <td>51.2%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>21.02%</td>
    </tr>
    <tr>
      <td>Wales Win</td>
      <td>25.42%</td>
    </tr>
    <tr>
      <td>Italy Win >= 2 Goals</td>
      <td>29.77%</td>
    </tr>
    <tr>
      <td>Wales Win >= 2 Goals</td>
      <td>10.96%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>25.33%</td>
    </tr>        
  </tbody>
</table>

The data shows that Italy are clearly the favourites with a win probability of 51.2%. With the Italians cheering them on in Rome, it may look like this is a certain Italian victory.

Italy have been the standouts of the tournament so far, whilst Wales have been more resilient than we expected. Wales know they have to keep the scoreline down to boost their chances of going through, and we expect a really defensive performance but Italy still proving too much to handle. Wales would lose the midfield battle, but may throw bodies behind the ball in defensive positions to get as many blocks as possible. **Italy 2-0 Wales**

### Group A: Switzerland vs Turkey (Neutral)
<em>Weighted xG (<span style="color:blue">1.79</span> - 1.29) /
<em>Weighted xGA (<span style="color:red">1.16</span> - 1.85)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Switzerland goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Turkey Goals</strong></td>
      <td>Poisson for # of goals per team</td> 					
      <td>17.07%</td> 
      <td>30.18%</td>
      <td>26.67%</td>
      <td>15.72%</td>
      <td>6.95%</td>
      <td>2.46%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>27.42%</td>						
      <td style="background-color:#ffe0b3">4.68%</td>
      <td style="background-color:#b3ffb3">8.27%</td>
      <td style="background-color:#b3ffb3">7.31%</td>
      <td style="background-color:#b3ffb3">4.31%</td>
      <td style="background-color:#b3ffb3">1.91%</td>
      <td style="background-color:#b3ffb3">0.67%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>35.48%</td>												
      <td style="background-color:#FFCCCC">6.06%</td>
      <td style="background-color:#ffe0b3"><strong>10.71%</strong></td>
      <td style="background-color:#b3ffb3">9.46%</td>
      <td style="background-color:#b3ffb3">5.58%</td>
      <td style="background-color:#b3ffb3">2.47%</td>
      <td style="background-color:#b3ffb3">0.87%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>22.95%</td>				 								
      <td style="background-color:#FFCCCC">3.92%</td>
      <td style="background-color:#FFCCCC">6.93%</td>
      <td style="background-color:#ffe0b3">6.12%</td>
      <td style="background-color:#b3ffb3">3.61%</td>
      <td style="background-color:#b3ffb3">1.59%</td>
      <td style="background-color:#b3ffb3">0.56%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>9.90%</td>											
      <td style="background-color:#FFCCCC">1.69%</td>
      <td style="background-color:#FFCCCC">2.99%</td>
      <td style="background-color:#FFCCCC">2.64%</td>
      <td style="background-color:#ffe0b3">1.56%</td>
      <td style="background-color:#b3ffb3">0.69%</td>
      <td style="background-color:#b3ffb3">0.24%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>3.20%</td>																		
      <td style="background-color:#FFCCCC">0.55%</td>
      <td style="background-color:#FFCCCC">0.97%</td>
      <td style="background-color:#FFCCCC">0.85%</td>
      <td style="background-color:#FFCCCC">0.50%</td>
      <td style="background-color:#ffe0b3">0.22%</td>
      <td style="background-color:#b3ffb3">0.08%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.83%</td>																		
      <td style="background-color:#FFCCCC">0.14%</td>
      <td style="background-color:#FFCCCC">0.25%</td>
      <td style="background-color:#FFCCCC">0.22%</td>
      <td style="background-color:#FFCCCC">0.13%</td>
      <td style="background-color:#FFCCCC">0.06%</td>
      <td style="background-color:#ffe0b3">0.02%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Switzerland Win</td>
      <td>47.63%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>23.31%</td>
    </tr>
    <tr>
      <td>Turkey Win</td>
      <td>27.89%</td>
    </tr>
    <tr>
      <td>Switzerland Win >= 2 Goals</td>
      <td>25.52%</td>
    </tr>
    <tr>
      <td>Turkey Win >= 2 Goals</td>
      <td>11.71%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>18.35%</td>
    </tr>        
  </tbody>
</table>
  
The most probable score might be a 1-1 draw but it is most probable for the Swiss to snatch their first 3 points of the campaign.

Turkey were fancied as dark horses but have been extremely underwhelming so far. The Swiss are too having difficulty creating chances, with the Italian defence completely nullifying their threat in the previous matchday. We expect another disappointing performance from the Turks as Switzerland edge out a tense game. **Switzerland 1-0 Turkey**

### Group B: Finland vs Belgium (Neutral)
<em>Weighted xG (0.93 - <span style="color:blue">1.39</span>) /
<em>Weighted xGA (1.79 - <span style="color:red">1.31</span>)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Finland goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Belgium Goals</strong></td>
      <td>Poisson for # of goals per team</td> 										
      <td>39.53%</td>  
      <td>36.69%</td>
      <td>17.02%</td>
      <td>5.27%</td>
      <td>1.22%</td>
      <td>0.23%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>24.89%</td>			
      <td style="background-color:#ffe0b3">9.84%</td>
      <td style="background-color:#b3ffb3">9.13%</td>
      <td style="background-color:#b3ffb3">4.24%</td>
      <td style="background-color:#b3ffb3">1.31%</td>
      <td style="background-color:#b3ffb3">0.30%</td>
      <td style="background-color:#b3ffb3">0.06%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>34.61%</td>											
      <td style="background-color:#FFCCCC"><strong>13.68%</strong></td>
      <td style="background-color:#ffe0b3">12.70%</td>
      <td style="background-color:#b3ffb3">5.89%</td>
      <td style="background-color:#b3ffb3">1.82%</td>
      <td style="background-color:#b3ffb3">0.42%</td>
      <td style="background-color:#b3ffb3">0.08%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>24.07%</td>			 								
      <td style="background-color:#FFCCCC">9.52%</td>
      <td style="background-color:#FFCCCC">8.83%</td>
      <td style="background-color:#ffe0b3">4.10%</td>
      <td style="background-color:#b3ffb3">1.27%</td>
      <td style="background-color:#b3ffb3">0.29%</td>
      <td style="background-color:#b3ffb3">0.05%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>11.16%</td>										
      <td style="background-color:#FFCCCC">4.41%</td>
      <td style="background-color:#FFCCCC">4.09%</td>
      <td style="background-color:#FFCCCC">1.90%</td>
      <td style="background-color:#ffe0b3">0.59%</td>
      <td style="background-color:#b3ffb3">0.14%</td>
      <td style="background-color:#b3ffb3">0.03%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>3.88%</td>														
      <td style="background-color:#FFCCCC">1.53%</td>
      <td style="background-color:#FFCCCC">1.42%</td>
      <td style="background-color:#FFCCCC">0.66%</td>
      <td style="background-color:#FFCCCC">0.20%</td>
      <td style="background-color:#ffe0b3">0.05%</td>
      <td style="background-color:#b3ffb3">0.01%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>1.08%</td>															
      <td style="background-color:#FFCCCC">0.43%</td>
      <td style="background-color:#FFCCCC">0.40%</td>
      <td style="background-color:#FFCCCC">0.18%</td>
      <td style="background-color:#FFCCCC">0.06%</td>
      <td style="background-color:#FFCCCC">0.01%</td>
      <td style="background-color:#ffe0b3">0.00%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Finland Win</td>
      <td>25.04%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>27.27%</td>
    </tr>
    <tr>
      <td>Belgium Win</td>
      <td>47.33%</td>
    </tr>
    <tr>
      <td>Finland Win >= 2 Goals</td>
      <td>8.61%</td>
    </tr>
    <tr>
      <td>Belgium Win >= 2 Goals</td>
      <td>22.70%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>8.24%</td>
    </tr>        
  </tbody>
</table>

Belgium are favourites here with 47.3% probability of winning.

Belgium were turgid in the first half against Denmark but proved their quality in the second half. With Kevin de Bruyne back to his best, we can expect Belgium to create a lot of chances. Finland aren't the greatest team and after suffering the 1-0 loss against Russia, there should not be a shock in this game. We expect a Belgian victory even if they do not play to their best and they will collect maximum points in their group. **Finland 0-2 Belgium**



### Group B: Denmark vs Russia (Home Advantage)
<em>Weighted xG (<span style="color:blue">1.95</span> - 1.22) /
<em>Weighted xGA (<span style="color:red">0.95</span> - 1.17)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Denmark goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Russia Goals</strong></td>
      <td>Poisson for # of goals per team</td> 									
      <td>14.23%</td>  
      <td>27.74%</td>
      <td>27.05%</td>
      <td>17.58%</td>
      <td>8.57%</td>
      <td>3.34%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>29.62%</td>
      <td style="background-color:#ffe0b3">4.21%</td>
      <td style="background-color:#b3ffb3">8.22%</td>
      <td style="background-color:#b3ffb3">8.01%</td>
      <td style="background-color:#b3ffb3">5.21%</td>
      <td style="background-color:#b3ffb3">2.54%</td>
      <td style="background-color:#b3ffb3">0.99%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>	
      <td>36.04%</td>			
      <td style="background-color:#FFCCCC">5.13%</td>
      <td style="background-color:#ffe0b3"><strong>10.00%</strong></td>
      <td style="background-color:#b3ffb3">9.75%</td>
      <td style="background-color:#b3ffb3">6.34%</td>
      <td style="background-color:#b3ffb3">3.09%</td>
      <td style="background-color:#b3ffb3">1.20%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>21.92%</td>							
      <td style="background-color:#FFCCCC">3.12%</td>
      <td style="background-color:#FFCCCC">6.08%</td>
      <td style="background-color:#ffe0b3">5.93%</td>
      <td style="background-color:#b3ffb3">3.85%</td>
      <td style="background-color:#b3ffb3">1.88%</td>
      <td style="background-color:#b3ffb3">0.73%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>8.89%</td>								
      <td style="background-color:#FFCCCC">1.27%</td>
      <td style="background-color:#FFCCCC">2.47%</td>
      <td style="background-color:#FFCCCC">2.41%</td>
      <td style="background-color:#ffe0b3">1.56%</td>
      <td style="background-color:#b3ffb3">0.76%</td>
      <td style="background-color:#b3ffb3">0.30%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>2.70%</td>													
      <td style="background-color:#FFCCCC">0.38%</td>
      <td style="background-color:#FFCCCC">0.75%</td>
      <td style="background-color:#FFCCCC">0.73%</td>
      <td style="background-color:#FFCCCC">0.48%</td>
      <td style="background-color:#ffe0b3">0.23%</td>
      <td style="background-color:#b3ffb3">0.09%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.66%</td> 														
      <td style="background-color:#FFCCCC">0.09%</td>
      <td style="background-color:#FFCCCC">0.18%</td>
      <td style="background-color:#FFCCCC">0.18%</td>
      <td style="background-color:#FFCCCC">0.12%</td>
      <td style="background-color:#FFCCCC">0.06%</td>
      <td style="background-color:#ffe0b3">0.02%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Denmark Win</td>
      <td>52.96%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>21.96%</td>
    </tr>
    <tr>
      <td>Russia Win</td>
      <td>23.43%</td>
    </tr>
    <tr>
      <td>Denmark Win >= 2 Goals</td>
      <td>30.29%</td>
    </tr>
    <tr>
      <td>Russia Win >= 2 Goals</td>
      <td>9.29%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>19.71%</td>
    </tr>        
  </tbody>
</table>

Similar to the Switzerland-Turkey game, the most probable outcome is a 1-1 draw but Denmark are favourites here due to the number of chances they created. In the past 2 games against Finland and Belgium, they registered an xG greater than 2. In their final group game back at home in Copenhagen, Denmark will be determined to win their first game of the tournament in front of their fans.  

Denmark very nearly shocked Belgium last matchweek, but still showed a fantastic team display despite being outclassed in the second half. They know that a huge margin of victory can boost their chances of qualifying, so would go out to dominate the game. The Russians may be happy to sit back and without Eriksen, would the Danes have enough creativity to break down the Russians? We believe the Danes have enough firepower and with an attacking mindset from the start, wear down the Russians over the course of 90 mins. **Denmark 3-1 Russia**

### Group C: Ukraine vs Austria (Neutral)
<em>Weighted xG (<span style="color:blue">1.70</span> - 1.22) /
<em>Weighted xGA (1.42 - <span style="color:red">1.13</span>)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Ukraine goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Austria Goals</strong></td>
      <td>Poisson for # of goals per team</td> 									
      <td>18.27%</td> 
      <td>31.06%</td>
      <td>26.40%</td>
      <td>14.96%</td>
      <td>6.36%</td>
      <td>2.16%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>29.52%</td> 
      <td style="background-color:#ffe0b3">5.39%</td>
      <td style="background-color:#b3ffb3">9.17%</td>
      <td style="background-color:#b3ffb3">7.79%</td>
      <td style="background-color:#b3ffb3">4.42%</td>
      <td style="background-color:#b3ffb3">1.88%</td>
      <td style="background-color:#b3ffb3">0.64%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>36.02%</td>		
      <td style="background-color:#FFCCCC">6.58%</td>
      <td style="background-color:#ffe0b3"><strong>11.19%</strong></td>
      <td style="background-color:#b3ffb3">9.51%</td>
      <td style="background-color:#b3ffb3">5.39%</td>
      <td style="background-color:#b3ffb3">2.29%</td>
      <td style="background-color:#b3ffb3">0.78%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>21.97%</td>							
      <td style="background-color:#FFCCCC">4.01%</td>
      <td style="background-color:#FFCCCC">6.82%</td>
      <td style="background-color:#ffe0b3">5.80%</td>
      <td style="background-color:#b3ffb3">3.29%</td>
      <td style="background-color:#b3ffb3">1.40%</td>
      <td style="background-color:#b3ffb3">0.47%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>8.93%</td>								
      <td style="background-color:#FFCCCC">1.63%</td>
      <td style="background-color:#FFCCCC">2.77%</td>
      <td style="background-color:#FFCCCC">2.36%</td>
      <td style="background-color:#ffe0b3">1.34%</td>
      <td style="background-color:#b3ffb3">0.57%</td>
      <td style="background-color:#b3ffb3">0.19%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>2.73%</td>												
      <td style="background-color:#FFCCCC">0.50%</td>
      <td style="background-color:#FFCCCC">0.85%</td>
      <td style="background-color:#FFCCCC">0.72%</td>
      <td style="background-color:#FFCCCC">0.41%</td>
      <td style="background-color:#ffe0b3">0.17%</td>
      <td style="background-color:#b3ffb3">0.06%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.66%</td> 													
      <td style="background-color:#FFCCCC">0.12%</td>
      <td style="background-color:#FFCCCC">0.21%</td>
      <td style="background-color:#FFCCCC">0.18%</td>
      <td style="background-color:#FFCCCC">0.10%</td>
      <td style="background-color:#FFCCCC">0.04%</td>
      <td style="background-color:#ffe0b3">0.01%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ukraine Win</td>
      <td>47.84%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>23.90%</td>
    </tr>
    <tr>
      <td>Austria Win</td>
      <td>27.30%</td>
    </tr>
    <tr>
      <td>Ukraine Win >= 2 Goals</td>
      <td>25.25%</td>
    </tr>
    <tr>
      <td>Austria Win >= 2 Goals</td>
      <td>11.09%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>16.19%</td>
    </tr>        
  </tbody>
</table>

Ukraine appear to be favourites according to the score matrix and this is due the 4 goals they have already scored this campaign (only Italy, Netherlands and Belgium have scored more). 

The 23rd and 24th ranked teams in the world face off, with both teams on 3 points going into the game. Arnautovic's return would be a welcome boost for Austria, but there seems to be little to separate the sides, with talents across the pitch on both teams. We are going to go with a draw as nothing may split the teams. Both teams might be content with a point as 4 points would be enough to guarantee them a place in the Round of 16. **Ukraine 1-1 Austria**

### Group C: Netherlands vs North Macedonia (Home Advantage)
<em>Weighted xG (<span style="color:blue">2.46</span> - 1.30) /
<em>Weighted xGA (<span style="color:red">0.63</span> - 1.31)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Netherlands goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>North Macedonia Goals</strong></td>
      <td>Poisson for # of goals per team</td> 						
      <td>8.52%</td> 
      <td>20.98%</td>
      <td>25.83%</td>
      <td>21.21%</td>
      <td>13.06%</td>
      <td>6.44%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>27.36%</td> 
      <td style="background-color:#ffe0b3">2.33%</td>
      <td style="background-color:#b3ffb3">5.74%</td>
      <td style="background-color:#b3ffb3">7.07%</td>
      <td style="background-color:#b3ffb3">5.80%</td>
      <td style="background-color:#b3ffb3">3.57%</td>
      <td style="background-color:#b3ffb3">1.76%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>35.46%</td>	
      <td style="background-color:#FFCCCC">3.02%</td>
      <td style="background-color:#ffe0b3">7.44%</td>
      <td style="background-color:#b3ffb3"><strong>9.16%</strong></td>
      <td style="background-color:#b3ffb3">7.52%</td>
      <td style="background-color:#b3ffb3">4.63%</td>
      <td style="background-color:#b3ffb3">2.28%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>22.98%</td>						
      <td style="background-color:#FFCCCC">1.96%</td>
      <td style="background-color:#FFCCCC">4.82%</td>
      <td style="background-color:#ffe0b3">5.94%</td>
      <td style="background-color:#b3ffb3">4.87%</td>
      <td style="background-color:#b3ffb3">3.00%</td>
      <td style="background-color:#b3ffb3">1.48%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>9.93%</td>							
      <td style="background-color:#FFCCCC">0.85%</td>
      <td style="background-color:#FFCCCC">2.08%</td>
      <td style="background-color:#FFCCCC">2.56%</td>
      <td style="background-color:#ffe0b3">2.11%</td>
      <td style="background-color:#b3ffb3">1.30%</td>
      <td style="background-color:#b3ffb3">0.64%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>3.22%</td>											
      <td style="background-color:#FFCCCC">0.27%</td>
      <td style="background-color:#FFCCCC">0.67%</td>
      <td style="background-color:#FFCCCC">0.83%</td>
      <td style="background-color:#FFCCCC">0.68%</td>
      <td style="background-color:#ffe0b3">0.42%</td>
      <td style="background-color:#b3ffb3">0.21%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.83%</td> 										
      <td style="background-color:#FFCCCC">0.07%</td>
      <td style="background-color:#FFCCCC">0.17%</td>
      <td style="background-color:#FFCCCC">0.22%</td>
      <td style="background-color:#FFCCCC">0.18%</td>
      <td style="background-color:#FFCCCC">0.11%</td>
      <td style="background-color:#ffe0b3">0.05%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Netherlands Win</td>
      <td>59.05%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>18.28%</td>
    </tr>
    <tr>
      <td>North Macedonia Win</td>
      <td>18.50%</td>
    </tr>
    <tr>
      <td>Netherlands Win >= 2 Goals</td>
      <td>37.77%</td>
    </tr>
    <tr>
      <td>North Macedonia Win >= 2 Goals</td>
      <td>7.30%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>28.25%</td>
    </tr>        
  </tbody>
</table>

Netherlands are clear favourites here with an overwhelming 59% probability of winning. The most probable scoreline is 2-1 win but the 37.8% probability of a 2 or greater goal margin for Netherlands is one of the highest amongst the fixtures here. This is also aided with their fans cheering them on in their final group game.

The Netherlands have already topped their group and we expect a rotated squad, but still proving enough quality to dismantled an already eliminated North Macedonian side. We will be going for a Netherlands win with 2 goal margin, but could potentially be more. **Netherlands 2-0 North Macedonia**

### Group D: England vs Czech Republic (Home Advantage)
<em>Weighted xG (1.11 - <span style="color:blue">1.49</span>) /
<em>Weighted xGA (<span style="color:red">0.85</span> - 1.22)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>England goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Czech Republic Goals</strong></td>
      <td>Poisson for # of goals per team</td> 						
      <td>28.80%</td> 
      <td>35.85%</td>
      <td>22.31%</td>
      <td>9.26%</td>
      <td>2.88%</td>
      <td>0.72%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>24.04%</td>
      <td style="background-color:#ffe0b3">6.93%</td>
      <td style="background-color:#b3ffb3">8.62%</td>
      <td style="background-color:#b3ffb3">5.36%</td>
      <td style="background-color:#b3ffb3">2.23%</td>
      <td style="background-color:#b3ffb3">0.69%</td>
      <td style="background-color:#b3ffb3">0.17%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>34.27%</td>	
      <td style="background-color:#FFCCCC">9.87%</td>
      <td style="background-color:#ffe0b3"><strong>12.29%</strong></td>
      <td style="background-color:#b3ffb3">7.65%</td>
      <td style="background-color:#b3ffb3">3.17%</td>
      <td style="background-color:#b3ffb3">0.99%</td>
      <td style="background-color:#b3ffb3">0.25%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>24.42%</td>	
      <td style="background-color:#FFCCCC">7.03%</td>
      <td style="background-color:#FFCCCC">8.76%</td>
      <td style="background-color:#ffe0b3">5.45%</td>
      <td style="background-color:#b3ffb3">2.26%</td>
      <td style="background-color:#b3ffb3">0.70%</td>
      <td style="background-color:#b3ffb3">0.18%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>11.60%</td>					
      <td style="background-color:#FFCCCC">3.34%</td>
      <td style="background-color:#FFCCCC">4.16%</td>
      <td style="background-color:#FFCCCC">2.59%</td>
      <td style="background-color:#ffe0b3">1.07%</td>
      <td style="background-color:#b3ffb3">0.33%</td>
      <td style="background-color:#b3ffb3">0.08%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>4.13%</td>								
      <td style="background-color:#FFCCCC">1.19%</td>
      <td style="background-color:#FFCCCC">1.48%</td>
      <td style="background-color:#FFCCCC">0.92%</td>
      <td style="background-color:#FFCCCC">0.38%</td>
      <td style="background-color:#ffe0b3">0.12%</td>
      <td style="background-color:#b3ffb3">0.03%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>1.18%</td> 						
      <td style="background-color:#FFCCCC">0.34%</td>
      <td style="background-color:#FFCCCC">0.42%</td>
      <td style="background-color:#FFCCCC">0.26%</td>
      <td style="background-color:#FFCCCC">0.11%</td>
      <td style="background-color:#FFCCCC">0.03%</td>
      <td style="background-color:#ffe0b3">0.01%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>England Win</td>
      <td>32.71%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>25.86%</td>
    </tr>
    <tr>
      <td>Czech Republic Win</td>
      <td>40.90%</td>
    </tr>
    <tr>
      <td>England Win >= 2 Goals</td>
      <td>13.82%</td>
    </tr>
    <tr>
      <td>Czech Republic Win >= 2 Goals</td>
      <td>19.27%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>12.74%</td>
    </tr>        
  </tbody>
</table>
  
The score matrix put the Czechs as favourites here to beat England at 40.9%. They are however playing at Wembley which could potentially tip the scale to the English.

The English were disappointing against Scotland, with poor performances by many players and showing little signs of creativity. Southgate's tactical decisions and substitions were questionable. Although expectations will be high for the English (and pressure will be high on Southgate) to put in a good shift against the Czechs, the Czechs are no pushover. They have demonstrated ability to defend well and convert their chances. England will dominate the game with most of the possession, but we fancy the Czechs to take the game to the English and shock Wembley with a victory. **England 1-2 Czech Republic**

### Group D: Scotland vs Croatia (Home Advantage)
<em>Weighted xG (1.11 - <span style="color:blue">1.49</span>) /
<em>Weighted xGA (1.33 - <span style="color:red">0.97</span>)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Scotland goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Croatia Goals</strong></td>
      <td>Poisson for # of goals per team</td> 			
      <td>33.04%</td> 
      <td>36.59%</td>
      <td>20.26%</td>
      <td>7.48%</td>
      <td>2.07%</td>
      <td>0.46%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>22.49%</td> 
      <td style="background-color:#ffe0b3">7.43%</td>
      <td style="background-color:#b3ffb3">8.23%</td>
      <td style="background-color:#b3ffb3">4.56%</td>
      <td style="background-color:#b3ffb3">1.68%</td>
      <td style="background-color:#b3ffb3">0.47%</td>
      <td style="background-color:#b3ffb3">0.10%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>33.56%</td>	
      <td style="background-color:#FFCCCC">11.09%</td>
      <td style="background-color:#ffe0b3"><strong>12.28%</strong></td>
      <td style="background-color:#b3ffb3">6.80%</td>
      <td style="background-color:#b3ffb3">2.51%</td>
      <td style="background-color:#b3ffb3">0.69%</td>
      <td style="background-color:#b3ffb3">0.15%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>25.03%</td>
      <td style="background-color:#FFCCCC">8.27%</td>
      <td style="background-color:#FFCCCC">9.16%</td>
      <td style="background-color:#ffe0b3">5.07%</td>
      <td style="background-color:#b3ffb3">1.87%</td>
      <td style="background-color:#b3ffb3">0.52%</td>
      <td style="background-color:#b3ffb3">0.11%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>12.45%</td>				
      <td style="background-color:#FFCCCC">4.11%</td>
      <td style="background-color:#FFCCCC">4.56%</td>
      <td style="background-color:#FFCCCC">2.52%</td>
      <td style="background-color:#ffe0b3">0.93%</td>
      <td style="background-color:#b3ffb3">0.26%</td>
      <td style="background-color:#b3ffb3">0.06%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>4.64%</td>					
      <td style="background-color:#FFCCCC">1.53%</td>
      <td style="background-color:#FFCCCC">1.70%</td>
      <td style="background-color:#FFCCCC">0.94%</td>
      <td style="background-color:#FFCCCC">0.35%</td>
      <td style="background-color:#ffe0b3">0.10%</td>
      <td style="background-color:#b3ffb3">0.02%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>1.39%</td> 				
      <td style="background-color:#FFCCCC">0.46%</td>
      <td style="background-color:#FFCCCC">0.51%</td>
      <td style="background-color:#FFCCCC">0.28%</td>
      <td style="background-color:#FFCCCC">0.10%</td>
      <td style="background-color:#FFCCCC">0.03%</td>
      <td style="background-color:#ffe0b3">0.01%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Scotland Win</td>
      <td>28.04%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>25.82%</td>
    </tr>
    <tr>
      <td>Croatia Win</td>
      <td>45.61%</td>
    </tr>
    <tr>
      <td>Scotland Win >= 2 Goals</td>
      <td>10.86%</td>
    </tr>
    <tr>
      <td>Croatia Win >= 2 Goals</td>
      <td>22.47%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>11.71%</td>
    </tr>        
  </tbody>
</table>

Croatia are favourites in this game with a 45.61% probability of winning. Scotland have an advantage playing at home at Hampden Park.

Scotland dominated the game against England and will feel hard done to have not come away with more, whilst Croatia disappointed against the Czechs. Tierney's return to the Scottish side proved important as he made plenty of offensive and defensive runs, whilst Gilmour was outstanding throughout the game. Croatia may have the better midfield, but Scotttish tenacity and heart may see them overwhelm the Croats, especially if they're buoyed on by a raucous Hampden Park. We are tipping the Scots to finally break their duct and emerge with a shock and narrow victory. **Scotland 2-1 Croatia**

### Group E: Sweden vs Poland (Neutral)
<em>Weighted xG (<span style="color:blue">1.40</span> - 1.32) /
<em>Weighted xGA (<span style="color:red">1.55</span> - 1.59)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Sweden goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Poland Goals</strong></td>
      <td>Poisson for # of goals per team</td> 	
      <td>24.54%</td> 
      <td>34.48%</td>
      <td>24.21%</td>
      <td>11.34%</td>
      <td>3.98%</td>
      <td>1.12%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>25.34%</td> 
      <td style="background-color:#ffe0b3">6.22%</td>
      <td style="background-color:#b3ffb3">8.74%</td>
      <td style="background-color:#b3ffb3">6.14%</td>
      <td style="background-color:#b3ffb3">2.87%</td>
      <td style="background-color:#b3ffb3">1.01%</td>
      <td style="background-color:#b3ffb3">0.28%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>34.79%</td>
      <td style="background-color:#FFCCCC">8.54%</td>
      <td style="background-color:#ffe0b3"><strong>11.99%</strong></td>
      <td style="background-color:#b3ffb3">8.42%</td>
      <td style="background-color:#b3ffb3">3.94%</td>
      <td style="background-color:#b3ffb3">1.39%</td>
      <td style="background-color:#b3ffb3">0.39%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>23.88%</td>	
      <td style="background-color:#FFCCCC">5.86%</td>
      <td style="background-color:#FFCCCC">8.23%</td>
      <td style="background-color:#ffe0b3">5.78%</td>
      <td style="background-color:#b3ffb3">2.71%</td>
      <td style="background-color:#b3ffb3">0.95%</td>
      <td style="background-color:#b3ffb3">0.27%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>10.92%</td>				
      <td style="background-color:#FFCCCC">2.68%</td>
      <td style="background-color:#FFCCCC">3.77%</td>
      <td style="background-color:#FFCCCC">2.65%</td>
      <td style="background-color:#ffe0b3">1.24%</td>
      <td style="background-color:#b3ffb3">0.43%</td>
      <td style="background-color:#b3ffb3">0.12%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>3.75%</td>		
      <td style="background-color:#FFCCCC">0.92%</td>
      <td style="background-color:#FFCCCC">1.29%</td>
      <td style="background-color:#FFCCCC">0.91%</td>
      <td style="background-color:#FFCCCC">0.43%</td>
      <td style="background-color:#ffe0b3">0.15%</td>
      <td style="background-color:#b3ffb3">0.04%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>1.03%</td> 		
      <td style="background-color:#FFCCCC">0.25%</td>
      <td style="background-color:#FFCCCC">0.35%</td>
      <td style="background-color:#FFCCCC">0.25%</td>
      <td style="background-color:#FFCCCC">0.12%</td>
      <td style="background-color:#FFCCCC">0.04%</td>
      <td style="background-color:#ffe0b3">0.01%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sweden Win</td>
      <td>38.76%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>25.65%</td>
    </tr>
    <tr>
      <td>Poland Win</td>
      <td>35.02%</td>
    </tr>
    <tr>
      <td>Sweden Win >= 2 Goals</td>
      <td>17.94%</td>
    </tr>
    <tr>
      <td>Poland Win >= 2 Goals</td>
      <td>15.44%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>13.53%</td>
    </tr>        
  </tbody>
</table>

The score matrix puts the Swedes as slight favourites but it looks like a really even game.

The Swedes may feel a tad lucky to have won their previous game, and may come into this game a little cautious, knowing that every point may be crucial to them. They have shown an ability to defend really well. The Poles should be buoyed by their 1-1 draw against the Spanish. It may prove to be a cagey affair with plenty of half-chances for both sides, and we are predicting a draw. **Sweden 1-1 Poland**

### Group E: Spain vs Slovakia (Home Advantage)
<em>Weighted xG (<span style="color:blue">2.69</span> - 1.11) /
<em>Weighted xGA (<span style="color:red">0.98</span> - 1.43)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Spain goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Slovakia Goals</strong></td>
      <td>Poisson for # of goals per team</td> 	
      <td>6.77%</td> 
      <td>18.23%</td>
      <td>24.54%</td>
      <td>22.03%</td>
      <td>14.83%</td>
      <td>7.99%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>32.82%</td>
      <td style="background-color:#ffe0b3">2.22%</td>
      <td style="background-color:#b3ffb3">5.98%</td>
      <td style="background-color:#b3ffb3">8.06%</td>
      <td style="background-color:#b3ffb3">7.23%</td>
      <td style="background-color:#b3ffb3">4.87%</td>
      <td style="background-color:#b3ffb3">2.62%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>36.57%</td> 
      <td style="background-color:#FFCCCC">2.48%</td>
      <td style="background-color:#ffe0b3">6.67%</td>
      <td style="background-color:#b3ffb3"><strong>8.97%</strong></td>
      <td style="background-color:#b3ffb3">8.06%</td>
      <td style="background-color:#b3ffb3">5.42%</td>
      <td style="background-color:#b3ffb3">2.92%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>20.37%</td>	
      <td style="background-color:#FFCCCC">1.38%</td>
      <td style="background-color:#FFCCCC">3.71%</td>
      <td style="background-color:#ffe0b3">5.00%</td>
      <td style="background-color:#b3ffb3">4.49%</td>
      <td style="background-color:#b3ffb3">3.02%</td>
      <td style="background-color:#b3ffb3">1.63%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>7.56%</td>
      <td style="background-color:#FFCCCC">0.51%</td>
      <td style="background-color:#FFCCCC">1.38%</td>
      <td style="background-color:#FFCCCC">1.86%</td>
      <td style="background-color:#ffe0b3">1.67%</td>
      <td style="background-color:#b3ffb3">1.12%</td>
      <td style="background-color:#b3ffb3">0.60%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>2.11%</td>
      <td style="background-color:#FFCCCC">0.14%</td>
      <td style="background-color:#FFCCCC">0.38%</td>
      <td style="background-color:#FFCCCC">0.52%</td>
      <td style="background-color:#FFCCCC">0.46%</td>
      <td style="background-color:#ffe0b3">0.31%</td>
      <td style="background-color:#b3ffb3">0.17%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.47%</td> 	
      <td style="background-color:#FFCCCC">0.03%</td>
      <td style="background-color:#FFCCCC">0.09%</td>
      <td style="background-color:#FFCCCC">0.12%</td>
      <td style="background-color:#FFCCCC">0.10%</td>
      <td style="background-color:#FFCCCC">0.07%</td>
      <td style="background-color:#ffe0b3">0.04%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Spain Win</td>
      <td>65.16%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>15.90%</td>
    </tr>
    <tr>
      <td>Slovakia Win</td>
      <td>13.23%</td>
    </tr>
    <tr>
      <td>Spain Win >= 2 Goals</td>
      <td>44.42%</td>
    </tr>
    <tr>
      <td>Slovakia Win >= 2 Goals</td>
      <td>4.65%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>27.63%</td>
    </tr>        
  </tbody>
</table>

The score matrix puts the Spaniards as overwhelming favourites with a 65% probability to win! We know that they can create chances with an xG of 2.89 against Sweden and 3.17 against Poland. However, their problem has been the inability to convert in front of goal. They will be cheered on by their increasingly frustrated fans in Seville.

The Spaniards know how crucial a victory in this game will be, and the margin of victory may matter as well after a disappointing and wasteful performance against Poland. The Spaniards need to take the chances they create, especially against a resolute Slovak defence. We have confidence that despite misfirings in the past, the Spaniards will have the goods to show for when it matters in this game. **Spain 2-0 Slovakia**

### Group F: Germany vs Hungary (Home Advantage)
<em>Weighted xG (<span style="color:blue">1.83</span> - 1.06) /
<em>Weighted xGA (<span style="color:red">0.94</span> - 1.88)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Germany goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Hungary Goals</strong></td>
      <td>Poisson for # of goals per team</td> 
      <td>16.02%</td> 
      <td>29.34%</td>
      <td>26.86%</td>
      <td>16.40%</td>
      <td>7.51%</td>
      <td>2.75%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>34.48%</td> 
      <td style="background-color:#ffe0b3">5.52%</td>
      <td style="background-color:#b3ffb3">10.12%</td>
      <td style="background-color:#b3ffb3">9.26%</td>
      <td style="background-color:#b3ffb3">5.66%</td>
      <td style="background-color:#b3ffb3">2.59%</td>
      <td style="background-color:#b3ffb3">0.95%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>36.71%</td> 
      <td style="background-color:#FFCCCC">5.88%</td>
      <td style="background-color:#ffe0b3"><strong>10.77%</strong></td>
      <td style="background-color:#b3ffb3">9.86%</td>
      <td style="background-color:#b3ffb3">6.02%</td>
      <td style="background-color:#b3ffb3">2.76%</td>
      <td style="background-color:#b3ffb3">1.01%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>19.54%</td>
      <td style="background-color:#FFCCCC">3.13%</td>
      <td style="background-color:#FFCCCC">5.73%</td>
      <td style="background-color:#ffe0b3">5.25%</td>
      <td style="background-color:#b3ffb3">3.21%</td>
      <td style="background-color:#b3ffb3">1.47%</td>
      <td style="background-color:#b3ffb3">0.54%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>6.94%</td>
      <td style="background-color:#FFCCCC">1.11%</td>
      <td style="background-color:#FFCCCC">2.03%</td>
      <td style="background-color:#FFCCCC">1.86%</td>
      <td style="background-color:#ffe0b3">1.14%</td>
      <td style="background-color:#b3ffb3">0.52%</td>
      <td style="background-color:#b3ffb3">0.19%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>1.85%</td>
      <td style="background-color:#FFCCCC">0.30%</td>
      <td style="background-color:#FFCCCC">0.54%</td>
      <td style="background-color:#FFCCCC">0.50%</td>
      <td style="background-color:#FFCCCC">0.30%</td>
      <td style="background-color:#ffe0b3">0.14%</td>
      <td style="background-color:#b3ffb3">0.05%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>0.39%</td> 	
      <td style="background-color:#FFCCCC">0.06%</td>
      <td style="background-color:#FFCCCC">0.12%</td>
      <td style="background-color:#FFCCCC">0.11%</td>
      <td style="background-color:#FFCCCC">0.06%</td>
      <td style="background-color:#FFCCCC">0.03%</td>
      <td style="background-color:#ffe0b3">0.01%</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Germany Win</td>
      <td>65.16%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>15.90%</td>
    </tr>
    <tr>
      <td>Hungary Win</td>
      <td>13.23%</td>
    </tr>
    <tr>
      <td>Germany Win >= 2 Goals</td>
      <td>44.42%</td>
    </tr>
    <tr>
      <td>Hungary Win >= 2 Goals</td>
      <td>4.65%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>27.63%</td>
    </tr>        
  </tbody>
</table>

Germany are favourites in this game with at 54.19% probability to win but we are also looking at a high probability of a big margin of victory.

Following what was perhaps the performance of the matchweek, Germany look to have found their match winning formula. Hungary's resilience were really impressive, but Germany's dominance against Portugal was a sight to behold. Expect Hungary to sit deep and aim to hit on the counter like they did against France, but if Germany can exploit the widths and provide high quality deliveries like they did against Portugal, it would be a totally one-sided display. **Germany 4-0 Hungary**

### Group F: Portugal vs France (Neutral)
<em>Weighted xG (<span style="color:blue">2.42</span> - 1.71) /
<em>Weighted xGA (1.28 - <span style="color:red">0.87</span>)

<table>
  <thead>
    <tr>
      <th> </th>
      <th>Portugal goals</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>France Goals</strong></td>
      <td>Poisson for # of goals per team</td>
      <td>8.86%</td> 
      <td>21.48%</td>
      <td>26.02%</td>
      <td>21.02%</td>
      <td>12.74%</td>
      <td>6.17%</td>
    </tr>
    <tr>
      <td><strong>0</strong></td>
      <td>18.12%</td> 
      <td style="background-color:#ffe0b3">1.61%</td>
      <td style="background-color:#b3ffb3">3.89%</td>
      <td style="background-color:#b3ffb3">4.72%</td>
      <td style="background-color:#b3ffb3">3.81%</td>
      <td style="background-color:#b3ffb3">2.31%</td>
      <td style="background-color:#b3ffb3">1.12%</td>
    </tr>
    <tr>
      <td><strong>1</strong></td>
      <td>30.95%</td>
      <td style="background-color:#FFCCCC">2.74%</td>
      <td style="background-color:#ffe0b3">6.65%</td>
      <td style="background-color:#b3ffb3"><strong>8.06%</strong></td>
      <td style="background-color:#b3ffb3">6.51%</td>
      <td style="background-color:#b3ffb3">3.94%</td>
      <td style="background-color:#b3ffb3">1.91%</td>
    </tr>
     <tr>
      <td><strong>2</strong></td> 
      <td>26.43%</td> 
      <td style="background-color:#FFCCCC">2.34%</td>
      <td style="background-color:#FFCCCC">5.68%</td>
      <td style="background-color:#ffe0b3">6.88%</td>
      <td style="background-color:#b3ffb3">5.56%</td>
      <td style="background-color:#b3ffb3">3.37%</td>
      <td style="background-color:#b3ffb3">1.63%</td>
    </tr>
     <tr>
      <td><strong>3</strong></td>
      <td>15.05%</td> 
      <td style="background-color:#FFCCCC">1.33%</td>
      <td style="background-color:#FFCCCC">3.23%</td>
      <td style="background-color:#FFCCCC">3.92%</td>
      <td style="background-color:#ffe0b3">3.16%</td>
      <td style="background-color:#b3ffb3">1.92%</td>
      <td style="background-color:#b3ffb3">0.93%</td>
    </tr>
     <tr>
      <td><strong>4</strong></td>
      <td>6.43%</td>
      <td style="background-color:#FFCCCC">0.57%</td>
      <td style="background-color:#FFCCCC">1.38%</td>
      <td style="background-color:#FFCCCC">1.67%</td>
      <td style="background-color:#FFCCCC">1.35%</td>
      <td style="background-color:#ffe0b3">0.82%</td>
      <td style="background-color:#b3ffb3">0.40%</td>
    </tr>
     <tr>
      <td><strong>5</strong></td>
      <td>2.20%</td> 	
      <td style="background-color:#FFCCCC">0.19%</td>
      <td style="background-color:#FFCCCC">0.47%</td>
      <td style="background-color:#FFCCCC">0.57%</td>
      <td style="background-color:#FFCCCC">0.46%</td>
      <td style="background-color:#FFCCCC">0.28%</td>
      <td style="background-color:#ffe0b3">0.14%</td>
    </tr>
  </tbody>
</table>


<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Portugal Win</td>
      <td>50.06%</td>
    </tr>
    <tr>
      <td>Draw</td>
      <td>19.25%</td>
    </tr>
    <tr>
      <td>France Win</td>
      <td>26.20%</td>
    </tr>
    <tr>
      <td>Portugal Win >= 2 Goals</td>
      <td>30.24%</td>
    </tr>
    <tr>
      <td>France Win >= 2 Goals</td>
      <td>12.23%</td>
    </tr>
        <tr>
      <td>Over 2.5 Goals </td>
      <td>35.18%</td>
    </tr>        
  </tbody>
</table>

The stats put the Portugese as favourites for this game and this is simply down to the lack of chances created by France.

France were not fantastic against Hungary, spurning a couple of chances but also not creating as many chances as expected. Portugal always seem to score but their defensive frailties against Germany must be worrying for Fernando Santos. We expect Portugal to carve out enough opportunities to score, whilst France would have to dominate the midfield and have enough successful take-ons to trouble the Portuguese. If France's attack does not gel more by the time this game comes around, we have a sneaky feeling that France would rue missed chances and get outscored by Portugal. This should be a hugely entertaining match with everything to play for in this group. **Portugal 3-2 France** 
