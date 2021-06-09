---
layout: post
title: Our Euro 2020 Predictions
---

<p align="center">
  <img width="1000" height="562" src="{{ site.baseurl }}/images/euro_2020.png">
</p>


In the spirit of the Euro 2020 (or 2021) Championships, Ashley and I decided to whip out our crystal balls to predict some of the results in the first round of fixtures. The objectives are simple - beat <a href="https://www.fifa.com/worldcup/news/south-africa-2010-unlikeliest-star-1275628">Paul the Octopus</a> and also emerge victorious in our respective Fantasy leagues. We have a slight advantage in the form of data (albeit limited) and a cognitive understanding of the game although these predictions will probably not be worth more than the <a href="https://www.huffpost.com/entry/paul-the-octopus-could-be_n_646660">$4.5 Million</a>  Paul was valued at. 

## Methodology

Our methodology is very loosely based on analysing the most recent performances of individual teams across the international friendlies, World Cup qualifiers and Nations League competition. Metrics used to analyse performances are Expected Goals (xG) and Expected Goals Against (xGA). xG values were kindly provided by <a href="https://footystats.org/">footystats.org</a>. While xG is used to determine the team's offensive capabilities based on shot quality, xGA is helps to rate their defensive capabilities by considering the opponent's xG (aka the quality of shots conceded). In simple terms, a higher xG relates to a better offensive output while a lower xGA is a stronger defensive display. 

We then analysed the performance of the xG model in relation to the actual result. This helps to identify not only the reliance of the xG model, but more importantly how clinical the teams are in attack. The following were the results we got:


<div class="row">
        <div class="column">
            <img alt="RMSE" src="{{ site.baseurl }}/images/Euro_2020_xG_RMSE.png" width="520" height="650">
        </div>
        <div class="column">
            <img alt="xG_over_goals" src="{{ site.baseurl }}/images/Euro_2020_goals_over_xg.png" width="520" height="650">
        </div>
</div>

On the left, we calculated the Root Mean Squared Error of the xG values versus the actual goals scored. This helps to identify if the xG model was a good predictor of the actual number of goals scored. On the right, we have a simple illustration of the xG over actual goals scored. This provides an indication if the xG model has been underpredicting (a high goals over xG) or overpredicting (a negative goals over xG) the team's goalscoring prowess. Both plots will need to be used hand in hand to analyse the teams performance. Denmark and Belgium immediately stand up at the top of the chart, with high RMSE and Goals over xG. With a highly in-form Romelu Lukaku and Kevin de Bruyne behind him, it is hardly suprising to see Belgium being so ruthless in taking their chances. Denmark also boost prolific goalscorers in their ranks (Olsen, Dolberg and of course the legendary Braithwaite) and their 8-0 thumping of Moldova did massively boost their Goals over xG record.

With this analysis, we calculated a weighted xG and weighted xGA that accounts for form by giving a heavier weightage to the most recent games (wow data science). Of course, with all these numbers, it is not pragmatic to predict a 2.53 - 1.5 victory for England against Croatia so we employed a little bit of our knowledge of the games. It is also important to note that international tournaments have this magical factor of regular upsets and surprises (South Korea 2002, Greece 2004, etc.) that do not come so often in friendlies or qualifiers. We also want to highlight that the Goals over xG values are very much dependent on the quality of oppositions the team is facing (eg. thrashing a team (who has a part-time dentist, part-time player in goal) 11-0 will greatly skew this metric. Our predictions will therefore be very much dependent on both what the data is telling us and our understanding of the game. With this, lets get to our predictions!

## Our Predictions

### Group A : Turkey vs Italy
<em>Weighted xG (1.41 - <span style="color:blue">2.00</span>) /
<em>Weighted xGA (<span style="color:red">1.20</span> - 0.648)

A tough game to call as Turkey should prove a tougher prospect than neutrals may suspect for Euro dark horses Italy. The xG model predicts Italy's xG pretty well while it does show that Turkey has been scoring higher than their xG values (about 0.5). However, with a superior defensive record (2nd lowest xGA), we fancy Italy to just about scrape through with a dogged performance. **Turkey 0-2 Italy**.

### Group A : Wales vs Switzerland
<em>Weighted xG (1.23 - <span style="color:blue">1.98</span>) /
<em>Weighted xGA (<span style="color:red">1.44</span> - 1.13)

The xG model shows that Wales are less clinical in converting their chances while Switzerland are one of the top 5 clinical teams. This match between 2 decent sides without much star power in a star-studded euros, both teams would not want to lose their opening game which may result in a cagey draw.**Wales 1-1 Switzerland**.

### Group B : Denmark vs Finland
<em>Weighted xG (<span style="color:blue">1.39</span> - 0.939) /
<em>Weighted xGA (1.13 - <span style="color:red">1.49</span>)

As indicated by the model, the Danes are one of the most clinical teams in the tournament. The Danes should have enough quality to comfortably see off a Finnish side which are one of the weaker teams at the tournament (both one of the lowest xG and highest xGA). No surprises here. **Denmark 2-0 Finland**.

### Group B : Belgium vs Russia
<em>Weighted xG (<span style="color:blue">1.60</span> - 1.17) /
<em>Weighted xGA (0.871 - <span style="color:red">1.05</span>)

The Red Devils need to have something to show for their golden generation, and this tournament might be their best bet. Questions remain about their depth defensively, but we expect them to take the game to Russia and just have too much quality offensively as seen in the graphs above. We believe they will continue their fine form into the opening match. **Belgium 3-0 Russia**.


### Group C: Austria vs North Macedonia
<em>Weighted xG (1.58 - <span style="color:blue">1.69</span>) /
<em>Weighted xGA (<span style="color:red">1.25</span> - 0.993)

North Macedonia, one of the weakest teams in the tournament, could be a surprise package. The graphs indicate a very efficient conversion of chances which included that shock 2-1 victory over the Germans. Their xG are also pretty high (granted they played Liechenstein and Kazkhstan). Austria on the other hand, have displayed a lower ability to convert their chances and lower xG. North Macedonia have lost their previous 2 encounters with the Austrians, but opening matchday fixtures can prove to be tense affairs, where im backing a low-quality game ending in a goalless draw. **Austria 0-0 North Macedonia**.

### Group C: Netherlands vs Ukraine
<em>Weighted xG (<span style="color:blue">2.87</span> - 1.83) /
<em>Weighted xGA (0.543 - <span style="color:red">0.911</span>)

This could be a tricky one considering the vast difference in xG and xGA between the 2 nations. The xG model also suggests that both teams are not as clinical in taking their chances, with the Dutch being the bottom team. Frank de Boer is seemingly out of his depth as the head coach, with plenty of off-pitch issues as well.  A previous affair ended in a draw between the sides, but we are tipping the Dutch to have issues as a team and falling to a somewhat shock loss to Ukraine. **Netherlands 1-2 Ukraine**.

### Group D: England vs Croatia
<em>Weighted xG (1.65 - <span style="color:blue">1.99</span>) /
<em>Weighted xGA (0.747 -<span style="color:red"> 0.942</span>)

The xG model rather accurately predicts the goals scored for both teams so looking at the xG and xGA values, we can expect this to be a really closely contested affair. The English will be out for revenge against the Croats, especially with the past few years having been great for English youth development. Croatia are well drilled, but we expect a moment of magic by one of the English players to prove decisive. **England 2-1 Croatia**.

### Group D: Scotland vs Czech Republic
<em>Weighted xG (1.398 - <span style="color:blue">1.70</span>) /
<em>Weighted xGA (<span style="color:red">1.13</span> - 1.06)

Scotland seems to have a slightly better conversion of shots compared to their opponents. This match could prove pivotal in seeing which team finishes third in their group, and we think the Czechs have the slightly better players with more experience, coupled with a greater xG and lower xGA to come away with a win. **Scotland 0-2 Czech Republic**.

### Group E: Poland vs Slovakia
<em>Weighted xG (1.21 - <span style="color:blue">1.24</span>) /
<em>Weighted xGA (0.913 - <span style="color:red"> 1.15 </span>)

Although Poland have a slightly lower xG compared to Slovakia, the model shows that they have been very clinical in converting their chances. We expect the Poles have enough talented players with a very much in form Robert Lewandowski playing at the highest level. They should see through this game against a weaker Slovakia side. **Poland 2-0 Slovakia**.

### Group E: Spain vs Sweden
<em>Weighted xG (<span style="color:blue">1.99</span> - 1.38) /
<em>Weighted xGA (0.531 - <span style="color:red"> 1.02</span>)

Spain may look like a promising team on paper with a high xG but we think they have not sufficiently addressed the cracks that saw them under-perform at the last World Cup. Historically, they have struggled to secure a result in their opening games of international tournaments (winning 1 out of the last 4). Sweden would be a resolute opposition, who may come away with a great point. Shock result number 2. **Spain 1-1 Sweden**.

### Group F: Hungary vs Portugal
<em>Weighted xG (1.77 - <span style="color:blue"> 2.53</span>) /
<em>Weighted xGA (0.862 - <span style="color:red">1.08</span>)

The current holders have to be tipped as outsiders for the title again this year, albeit having to come through a tough group first. Hungary, although being the 4th most clinical team, should prove no match for a Portugal side who have a much more superior xG and filled with world class talents. **Hungary 1-3 Portugal**.

### Group F: France vs Germany
<em>Weighted xG (<span style="color:blue">2.04</span> - 1.72) /
<em>Weighted xGA (0.753 - <span style="color:red">0.886</span> )

This is perhaps the biggest fixture of the opening games. The shock inclusion of Benzema may prove costly if squad harmony is disrupted down the line, but there seems to be no issues currently for France. On the other hand, Joachim Low has outstayed his welcome for a couple of years, and his tactical naivety will cost Germany in the group of death. A very much in-form France with a high xG and efficiency in shot conversion should see France dispatch the Germans off in a thoroughly entertaining clash. **France 3-1 Germany**.

![alt text for screen readers]({{ site.baseurl }}/images/france_vs_germany.png "France vs Germany, the French emerged as 2-0 victors in the 2016 European Tournament")

## Closing words

This is it. The stage is set for a much anticipated tournament that has been pushed back a year! I will be rating my own predictions and refining them in subsequent fixtures! If you did use some of predictions to make a bet (whether for or against), or if you are feeling generous, feel free to buy us a beer  <a href="https://www.buymeacoffee.com/zychua">here</a>! All the best and of course, thank you for reading!
