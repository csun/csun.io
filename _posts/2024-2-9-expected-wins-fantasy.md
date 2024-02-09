---
layout: post
title: Expected Wins - Blaming Fantasy Sports Failure on Bad Luck
---
I'm in a fantasy soccer league with some guys who spend more time complaining about the game than actually strategizing about how to play it. The crux of the problem is that results are heavily influenced by matchups. Even if you outscore all but one of the other players in your league, you'll still lose if that higher scoring player happens to be your opponent for the week. On the flip side, you can score terribly during a week and still record a win purely because you're lucky enough to play against a worse team. This element of chance makes for an easy scapegoat when you lose. When you win, though, your opponents will use it to bring up various stats that "prove" that you didn't deserve to.

Two of the most frequently referenced stats are the total amount of points scored by (for) or against a team over the course of a season. It's often the case that the league leader has a much lower Points Against total than anyone else. This tends to be interpreted as a sign that the league is rigged in favor of easier matchups for a certain person. However, I'd argue that Points Against is a misleading metric. The highest performing teams in the league only have to play against lower performers, naturally leading to fewer points scored against them. A low Points Against total can just be a sign that a team is performing well relative to others, not the cause of the high performance itself.

Even Points For is not necessarily a good metric because it fails to take consistency into account. Consider a 10 game season with two teams. Team A scores 90 points every week, while Team B scores 1000 points in one game and then 0 the rest of the season. Team A will finish with a 9-1 record, but Team B will finish with a higher Points For total. The owner of Team B will try to claim that they've been robbed, and that their greater Points For total proves that they're the better team. But the stats don't show that Team A had far superior consistency, which is ultimately what the game rewards in the long run.

I've come up with a simple metric that accounts for these shortcomings. I call it Expected Wins (xW). The formula is as follows:

$$xW\ =\sum _{n\ =\ 1}^{\#\ weeks\ in\ season} \ \frac{\#\ of\ teams\ outscored\ in\ week\ n}{\#\ of\ other\ teams\ in\ league}$$

Expected Wins is just the average number of wins you'd expect to have if you faced a random opponent every week of the season. Like Points For and Points Against, this is based on your actual performances throughout the season. Unlike those metrics, it also takes your consistency into account by limiting the amount of influence any given gameweek can have on the metric as a whole. A large gap between your expected and actual wins over the course of a season implies that you've gotten very (un)lucky. I know from googling around that I'm not the first person to think of this. However, I figured it was worth discussing because it doesn't seem to be displayed by any major fantasy sports sites.

Here's a plot of xW over time for my current season.

![](/images/expected_wins/plot.png)

As you can see, the only problem with this metric is that it (accurately) shows that my team is the best. It'll be tough to sell that to the other guys in my league - especially given that I'm currently in fourth place.
