## Week 8, Friday
On a phone, the header was too wide to fit the photo and my name side by side, so the photo got squeezed into a narrow oval and my name wrapped onto two cramped lines. I fixed it by adding flex-wrap: wrap to the header, so the photo stays a full circle and my name drops below it when there isn't room.

## Week 9, Wednesday
1. My three pages are Home, Projects, and Tennis. Home introduces me, Projects shows what I've built, and Tennis covers the sport I spend most of my time on and where it has taken me.
2. If each page carried its own copy of the styles, I would have had to make the same edit three times, once in each file. I could easily miss one, and the pages would stop matching each other. Luckily having one styles.css, one change updates every page.
3. I don't know how to make the nav stack or shrink nicely on a phone-sized screen yet.3

## Week 9, Friday
1. For breakpoint I used min-width: 40rem (640px) for the nav, cards and footer. At that width there is enough room for three cards side by side, so it's where the row layout stops being cramped. For Task 6 I added a second breakpoint at 64rem that widens the page to 60rem on big monitors. 

2. The two things I found and fixed at phone width were that the nav links were small and close together, which makes them hard to hit with a thumb. I made them "display: inline-block", raised the font size to 1.5rem, and added "padding: 0.5rem 0" so each link is taller.

The nav took up too much vertical space once it stacked on a phone. I made the margin and padding under it 1rem by default, and put the 2rem back inside the @media block for wide screens.

On the Tennis and Projects pages the header photo was overlapping with the first row of cards, so I added top margin to main on those pages. On Tennis I also found a "<div class="cards">" that was never closed, and I added the "</div>".

3. For justify-content and align-items, align-items changed how the cards were laid out depending on the value. With center, the cards lined up through the middle, but they were different sizes because each card has a different amount of text. With stretch, all the cards were the same size, but the cards with less text had a lot of blank space. flex-start made the cards ascend and flex-end made them descend, also because of the amount of text. With flex-direction: column;, the cards stacked vertically instead of horizontally. justify-content did a whole lot of nothing based on what I saw. I think it did nothing because my cards already fill the whole row, so there was no extra space to move them around in.

4. The plain rule applies on every screen, so the phone layout works with no query at all. The media query then adds changes only when there is room. If it were the other way round, phones would have to undo the wide layout, and a phone is the cramped case where a mistake costs the most. Writing narrow first means each rule only adds what the bigger screen needs.


## Week 10, Wednesday

1. HTML is what's on the page (the content and structure).CSS is how it looks (colors, fonts, layout).JavaScript is what happens when someone does something (clicks, loads).

2. defer tells the browser to finish building the page first, then run the script. Without it, the script can run before the elements exist, so querySelector finds nothing (null) and the code breaks.

3. Dark mode only redefines the variables in body.dark (--background, --text, etc.),and every rule using var(...) picks up the new values automatically. Without variables I'd have had to find and change every typed-in color by hand across all my pages.

4. My dark mode wouldn't stick between pages and the Console showed nothing. I found it by checking localStorage in the Console.

5. I don't know how to make the theme button look like my nav links yet.

## Week 10, Friday

1. event.preventDefault() stops the form from reloading the page when I press Send. Without it, everything I typed disappears.

2. querySelector returned null because that page doesn't have a form. Using null caused the error, and the if only runs the code when the element is actually found.

3. My rule rejects messages under 10 characters after trimming spaces, because required only checks that the field isn't empty, so a single character or a few spaces would pass.

4. The theme button was the browser’s default grey and too small to tap comfortably, so I styled it to match my nav with a 44px minimum height. The Send button had no minimum height, so I gave it min-height: 44px so it’s easy to hit with a thumb.

5. Right now the form doesn’t send the message anywhere. I think something is missing that receives it and does something with it, like a place to store the messages or a way to send them to my email.



