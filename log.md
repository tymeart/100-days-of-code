# 100 Days Of Code - Log

### Day 1: January 2nd, 2017

**Today's Progress:** I spent a lot of the time working on the CSS, and I realized the vertical layout of the numbers display on top of the keypad is probably better UX-wise, so I might change the "desktop" view to look like that as well later on.  
When it came time to figure out how to actually get my calculator to function, I felt like HTML data attributes would work somehow, but I didn't quite know how. Rewatched part of the drum kit tutorial of JavaScript30 and Googled vanilla JavaScript things to piece together an ugly piece of code that gets the numbers and operations to show up in the display when the buttons are clicked.  
Installed Hub so I can create Github repos from command line.  

*tl;dr:* Tweaked CSS for narrower viewport, got numbers and operations to display when clicked. Exported code from Codepen and pushed to Github.

**Thoughts:** Vanilla JS is a little tough because I'm not used to it. I'm confused about what to do with the scss & css files I got from exporting from Codepen, about precompiling, and about what to include/exclude from a Github repo. 

**Link to work:** [Calculator App](https://github.com/tymeart/calculator/commit/9c7371ffdb9ea4ab22512953529bad558f57d1fa)

### Day 2: January 3rd, 2017  

**Today's Progress:** After a lot of Googling, trying to figure out what to use to compile my Sass files, I installed and configured Grunt. Refactored the JS to display spaces between the clicked numbers and operations. Started trying to figure out how to implement the AC and CE buttons.  

**Thoughts:** I was pretty pooped after getting Grunt set up, but I'm glad I pushed through and did some actual coding.  

**Link to work:** [Calculator App](https://github.com/tymeart/calculator/commit/c9986275bd029ccee7a353d7039596f31bc69616)  

### Day 3: January 4th, 2017

**Today's Progress:** I got the AC button to work and added a transition to the buttons so the background color changes when clicked.

**Thoughts:** The logic of clearing the div when the AC button is clicked didn't take as long to figure out as I thought it would. Thinking about the CE button, though, I realize I need to add some way of keeping track of previously entered numbers. I feel like overall I need to step back and think more deeply about the logic behind the calculator instead of doing it piece by piece.

**Link to work:** [Calculator App](https://github.com/tymeart/calculator/commit/dafcf8b597212d1c0d08fa5efb0252c7dd80c1b5)
