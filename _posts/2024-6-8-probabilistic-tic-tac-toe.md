---
layout: post
title: Probabilistic Tic-Tac-Toe
excerpt: Tic-Tac-Toe reimagined as a game of chance.
---
Please see the associated [Hacker News comments](https://news.ycombinator.com/item?id=40635397) for discussion related to this game, [including an algorithm for optimal play](https://louisabraham.github.io/articles/probabilistic-tic-tac-toe) presented by [Louis Abraham](https://louisabraham.github.io/).
{:.comments-leader}

<style>
#pttt-iframe {
    max-height: 80vh;
}
</style>

<iframe id="pttt-iframe" frameborder="0" src="https://itch.io/embed-upload/10669100?color=FFFAF1" allowfullscreen="" width="100%" height="920"><a href="https://cameronsun.itch.io/probabilistic-tic-tac-toe">Play Probabilistic Tic-Tac-Toe on itch.io</a></iframe>

## Instructions
The rules are the same as normal tic-tac-toe, but each square has a different probability of a good (smiley face), neutral (meh face), or bad (frowny face) event happening when selected.

Good events place your mark (X or O) in the square. Bad events place your opponent's mark. Neutral events do nothing but pass the turn to the opponent.

Click in the top left to choose between 1x, 2x, and 3x speed for animations.

Click in the top right to go to the settings menu. Here you can switch between singleplayer and multiplayer modes, choose the difficulty, and enable tutor mode. On impossible difficulty, the computer will play mathematically optimally. As such, it will always get more wins than you over the course of many (tens to hundreds of) games. You will be able to beat it occasionally though.

Tutor mode is designed to give an insight into what the impossible AI thinks about each move. When hovering over a square in tutor mode, it shows the probability of winning the game given that you a) select that square and b) continue to play optimally for the rest of the game.

## Attribution and Source
[Project source is available here](https://github.com/csun/probabilistic-tic-tac-toe)

Icons by [Font Awesome](https://fontawesome.com/icons)

Font is [Multicolore](https://www.dafont.com/multicolore.font)

## Thoughts
I spend a lot of time thinking about the role of random chance in our lives. Which of our successes can we take credit for and which do we owe to luck? And even when things seem clear-cut, what about all the other factors we have no control over? The parents we're born to, societal power structures, the meteor that killed the dinosaurs - so many past events have an invisible impact on each new action we take. So what gives us the right to claim responsibility for our victories? Do we ever truly win? Or do we just get lucky sometimes?

So what does this have to do with the children's game embedded into this blog post?

Well, in any given game of Probabilistic Tic-Tac-Toe you can do everything right and still lose (or do everything wrong and win.) However, the better player always rises to the top over time. These are characteristics that I find interesting about a lot of other games, and I thought they'd be fun to apply to an otherwise boring, solved game like tic-tac-toe. They're also highly relevant to my life philosophy - that every outcome is effectively random, but our actions can often skew the odds in our favor. Bad breaks are inevitable, but good judgment is always rewarded (eventually, and given enough chances.)

If there's an optimal, human-executable strategy for this game, it's not immediately obvious to me. A computer could probably do an exhaustive search and play optimally, but the AI I implemented is only based on simple heuristics. Over 10k trials it beat a completely random actor about 66% of the time and tied about 6%. Over ~50 trials I beat the regular AI about 54% of the time and tied about 5%.

Enjoy!

## Optimal Solver Update - June 6th 2024
The game has been solved by [Louis Abraham.](https://louisabraham.github.io/articles/probabilistic-tic-tac-toe) I'm not sure if others have come up with similar solutions independently, but Louis was the one who helped me implement the optimal solver (dubbed "Impossible" difficulty) into the game.

I ran a couple tests of its strength:
- In 40 trials against me, the optimal solver won 50% of the time and tied 12.5%.
- In ~750 trials against a random actor, the optimal solver won 71.2% of the time and tied 4.1% of the time.
- In ~800 trials against the regular AI, the optimal solver won 59.5% of the time and tied 7.5% of the time.

Playing on impossible difficulty after playing on regular was very interesting. The heuristics-based regular AI plays an "expansive" style where it takes over as much of the board as possible - even when high quality winning moves are available. The impossible AI is much more aggressive. I've seen even seen it make plays where the "bad" odds significantly outweigh the "good" in order to secure a win early. This probably only happens when losing the square does not benefit the opponent. With that being said, it still does use the "expansive" style showcased by the regular AI as well when it makes sense to do so.
