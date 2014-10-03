# Redesign Assignment

I chose to redesign the [Wisconsin Register of Deeds Association home page](http://wrdaonline.org). I found it in an article about the [Worst Web Sites of 2013](http://www.webpagesthatsuck.com/worst-websites-of-2013.html) and, being a Wisconsin native, had to intervene.

The existing WRDA home page is a real mess. It is a table-based layout that features nested tables (very old school and bad practice), a crazy amount of inline CSS, and poor readability due to the lack of a coordinated color palette. There's also a Flash photo slideshow that takes up more area than the actual relevant content.

I had to just scrap the original code since it was so badly formatted and was mostly stuck in tables. Since their logo is an awkward size for a standard navbar, I opted for a left-hand navigation column instead.

The middle of the page contains links to what I'm sure is very useful information, but the way it was presented made certain that no one could use it. I moved the press release-style links to a new "News" section on the right side. Then I gave prominence to the most important content &ndash; the fact that 66 Wisconsin counties now have real estate records online.

I wanted to do away with the Flash slideshow altogether, but the Midwesterner in me knew that making this page too sterile is just not the Wisconsin way. To do these beautiful photos justice, I made the animation itself slightly smaller. I then noticed that the animation was letterboxing the photos in a way that made everything look...bad...

To solve this I wrapped the animation `<object>` inside of a `<div>` so that I could hide the letterboxed edges. I gave my `<div>` a fixed height and the style `overflow: hidden;` so that I could control how much of the `<object>` would show through. I set the top margin of the `<object>` to be the exact height of the top portion of letterbox. Then through trial and error I sized the `<div>` so that the bottom portion of the letterbox was cut off. I also used the `hidden-xs` class to hide the slideshow on the smallest of screens.

Finally, I added a footer to give a home to the rest of the information.