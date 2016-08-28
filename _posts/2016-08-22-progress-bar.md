---
layout: post
title: The Long March of Progress
excerpt: How to make a progress bar with just HTML, CSS and hard work. Or a normal amount of work, as it's quite easy.
comments: true
---

This is a brief look at how to make a progress bar in HTML and CSS only. I didn't want to use the pre-made Bootstrap examples because Bootstrap somehow felt like cheating. Because it is cheating. If I can hand-write this, you can too. Turns out it was far less pain than I thought it would be. Here are the steps I took. I can't tell you this is the right way, but it works for me.

## Step 1. Bar for the course.

All of the stuff I've half-read (no one reads a full book) about development all come down to a simple maxim. Do the easy things first. For me, this was to create an empty "bar", and completely fill it.
So I created an empty section, "progress-bar", and give it a background color. Add some padding to that, and you get a passable "bar" type thing. Once you add in a border, it doesn't look too bad.

![progress-bar-full](/images/progress-bar-full.png)

And here is the pretty basic HTML/CSS for that bar above

<script src="https://gist.github.com/edwardcgordon/98414b7abf0fd2ee164b6a3df3efd89e.js"></script>

## Step 2. Progression

Progress bars are rarely full. After all, they indicate progress, not achievement. I spent a long time trying to achieve this with an internal div, and margins. It didn't work and would be fiddly if it did. So I turned to gradients instead.

At first, I couldn't get it to stop fading like a 1990's shell suit top. But I changed the % values until it worked. Here it is.

![progress-bar-half](/images/progress-bar-half.png)

And you can see the gradient rule at the end:

<script src="https://gist.github.com/edwardcgordon/8e523883345d0abd0583366a972d4a10.js"></script>

**NB. This may not work on old Internet Explorer. But if you need to care about that you're getting paid more than me, so you'll have to sort yourself out.**

## Step 3. To progress, you must go backwards

What's past is prologue. Shakespeare said that, and it somehow seems relevant to realising you've done something... sub-optimal.
I had been creating new a new class for every variation. I realised that I could actually have one class to control the common themes (width, height, border) and another to control the color and the % of the gradient.

![progress-bar-seventy](/images/progress-bar-seventy.png)

You can see in the following gist, the progress-bar rule doesn't have a color. The new class selector does. So, do that. Also, ignore the empty DIVs. I put them in to try something out and it failed. So don't use them.

<script src="https://gist.github.com/edwardcgordon/3450880d342f46df3fcfaa9904a5048d.js"></script>

## Step 4. The long march of progress

That's it. Change the colors and % as you see fit. Just make a new rule for each class you make and see what happens. Here's the ```.good``` the ```.bad``` and the ```.ugly```, below. These ones are in CodePen so you can see it action.


<p data-height="186" data-theme-id="dark" data-slug-hash="EyBkpJ" data-default-tab="css,result" data-user="edwardcgordon" data-embed-version="2" class="codepen">See the Pen <a href="https://codepen.io/edwardcgordon/pen/EyBkpJ/">Progress Bar Examples</a> by Ed Gordon (<a href="http://codepen.io/edwardcgordon">@edwardcgordon</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
