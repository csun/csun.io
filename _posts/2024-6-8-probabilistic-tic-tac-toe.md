---
layout: post
title: Probabilistic Tic-Tac-Toe
excerpt: Tic-Tac-Toe reimagined as a game of chance.
---

<style>
#pttt-iframe {
    max-height: 80vh;
}
</style>

<iframe id="pttt-iframe" frameborder="0" src="https://itch.io/embed-upload/10642801?color=FFFAF1" allowfullscreen="" width="100%" height="920"><a href="https://cameronsun.itch.io/probabilistic-tic-tac-toe">Play Probabilistic Tic-Tac-Toe on itch.io</a></iframe>

## Instructions
The rules are the same as normal tic-tac-toe, but each square has a different probability of a good (smiley face), neutral (meh face), or bad (frowny face) event happening when selected.

Good events place your mark (X or O) in the square. Bad events place your opponent's mark. Neutral events do nothing but pass the turn to the opponent.

Click in the top right to switch between playing against the CPU and local two player mode.

Icons by [Font Awesome](https://fontawesome.com/icons)

Font is [Multicolore](https://www.dafont.com/multicolore.font)

## Thoughts
I spend a lot of time thinking about the role of random chance in our lives. Which of our successes can we take credit for and which do we owe to luck? And even when things seem clear-cut, what about all the other factors we have no control over? The parents we're born to, societal power structures, the meteor that killed the dinosaurs - so many past events have an invisible impact on each new action we take. So what gives us the right to claim responsibility for our victories? Do we ever truly win? Or do we just get lucky sometimes?

So what does this have to do with the children's game embedded into this blog post?

Well, in any given game of Probabilistic Tic-Tac-Toe you can do everything right and still lose (or do everything wrong and win.) However, the better player always rises to the top over time. These are characteristics that I find interesting about a lot of other games, and I thought they'd be fun to apply to an otherwise boring, solved game like tic-tac-toe. They're also highly relevant to my life philosophy - that every outcome is effectively random, but our actions can often skew the odds in our favor. Bad breaks are inevitable, but good judgment is always rewarded (eventually, and given enough chances.)

If there's an optimal, human-executable strategy for this game, it's not immediately obvious to me. A computer could probably do an exhaustive search and play optimally, but the AI I implemented is only based on simple heuristics. Over 10k trials it beat a completely random actor about 70% of the time. Over ~50 trials I beat the AI about 60% of the time.

Enjoy!
