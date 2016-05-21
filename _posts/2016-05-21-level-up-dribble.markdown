---
layout: post
title:  "Level Up With Dribbble"
date:   2016-05-21 15:40:00 +0100
---

As a web designer or developer it can sometimes be difficult to learn new skills or techniques. Especially if you're stuck building on the same website every day or just modifying existing themes for clients. Some times you just need something fresh, exciting and new.

Whilst helping with todays Stamford Code Club at Haatch (a monthly event for all ages mostly aimed at teenagers that I help run with a few others), I took the decision to pick a random design from Dribbble and decided to try and code it under an hour. This isn't something I've ever really done before but I wanted to create something different. It turned out to be quite good fun.

## The Challenge
After a quick dabble through Dribbble I came across a mobile app design for an Events App with a 'Tinder' style swipe interface for finding an event to attend, you can see it [here](https://dribbble.com/shots/2110032-App-for-events).

![Dribbble](https://d13yacurqjgara.cloudfront.net/users/149817/screenshots/2110032/app-6-nahlad.png)

## The Result
So with the challenge set, I headed my way to [codepen.io](http://codepen.io) and put my fingers to keyboard. The end result isn't something that's perfect but that wasn't the goal, the goal was to have some fun and learn some new techniques and patterns I could apply in my work else where. For about 40 minutes of on and off work between helping out other people I'm quite happy with it.

<p data-height="621" data-theme-id="light" data-slug-hash="grNNjE" data-default-tab="result" data-user="joshantbrown" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/joshantbrown/pen/grNNjE/">grNNjE</a> by Josh Brown (<a href="http://codepen.io/joshantbrown">@joshantbrown</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

## The Wash Up
The whole process was super fun and I highly recommend anyone who's interested or involved in web design giving it a go. Remember the goal isn't to build a pixel perfect masterpiece, but if you want to then go ahead, the main goal is to have fun creating and learn something in the process.

### Lesson One
One of the first few things I tackled after the background and the content was the header navigation, there's nothing too special here but I did like the design touch of a glowing bar under the currently active item. I knew exactly how to implement this using a pseudo element and some box shadow giving it a nice level of progressive enhancement. The main lesson here for me was just the design idea of having elements like this glow to show active states. Nice touch from the designer.

### Lesson Two
Flexbox is awesome, like really. This isn't so much something I've learnt here specifically but every time I get a chance to use it I get reminded all over again how awesome it is. I only really used it for the 3 buttons across the bottom to give them even spacing but still.

### Lesson Three
The last part I added was the 'stacking' of the cards behind the front card, I'm not happy with how I achieved the effect in the end and looking back I would have done things differently here. It's possible if you get the HTML and CSS right to remove the front card from the DOM using JavaScript and have the whole animation of the card behind fade in and grow to take the previous ones place happen using only the CSS. In order to achieve this you need to really utilise the CSS Transform property I however used a combination of width, margin and absolute positioning which means instead you get a weird movement of the cards around the screen.

The key to having the other cards stack in the way they do is by using a combination of general and direct sibling selectors to make the cards appear  differently depending on their position in the DOM. Alternatively you could utilise nth-child selectors. I've attached a little example of this below focusing on the opacity, but you'll also need to get the positioning and z-index right to get it working like in the CodePen.

```css
.card {
  /* Base Card Style including 1st Card */
}

.card ~ .card {
  /* Generic Sibling Card Style */
  opacity: 0; /* We don't want to see any more cards than we say we do */
}

.card:first-child + .card {
  /* 2nd Card */
  opacity: .5 !important;
}

.card:first-child + .card + .card, .card:nth-child(3) {
  /* 3rd card with an additional alternative selector */
  opacity: .5 !important;
}
```

So yeah lots of lessons learnt about how I could have made the code cleaner using a different selector syntax, made it possible to nicely transition between cards if we were to add real swipe interactive functionality.

### Conclusion
There's lots I took away from this exercise but above all it was a fun way to spend some time creating something. I could take things further especially down this web version of the card sort animation but I think I've learnt enough that if I ever needed to actually build something like that I'd know exactly what to do. If there's enough interest in what that looks like though I may create it for a future post! Definitely give this exercise a go yourselves though and see where you can get to, would love to see what you come up with. So go give Dribbble a browse and get creating.
