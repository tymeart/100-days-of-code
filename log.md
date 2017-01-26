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

### Day 4: January 5th, 2017

**Today's Progress:** Tweaked code to allow multi-digit numbers to be entered. Tried to figure out how to refer to the previously clicked button.

**Thoughts:** During the past 2 days, it's been so tough to get started. Leaving myself comments about the things to work on next helps a little.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/2c11c9aca23515c35d17dbd665c516eea87080ed)

### Day 5: January 6th, 2017

**Today's Progress:** Changed the way I'm keeping track of and displaying inputs.

**Thoughts:** I was so stuck that I watched a tutorial to get a hint for how to keep track of the inputs/outputs. I feel guilty, but I had no idea how I should set up my calculator. :< I was too focused on little parts rather than the whole, but I guess I did learn some things about nodes and vanilla JS from doing things this way.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/5b2e9858bf64a5cc75cf085665428b88b27d743d)

### Day 6: January 7th, 2017

**Today's Progress:** Got numbers and operators to display when clicked. Pulled repetitive code out into an update function (updates display with the string of inputs) and started working on a way to get spaces to show around the operators.

**Thoughts:** It's muuuuch easier to work with arrays and strings than with... nodes.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/b219b5fb801f88a704f9d5d563d913daa2102610)

### Day 7: January 8th, 2017

**Today's Progress:** Gave up trying to get the numbers and operators spaced out because I thought I was spending too much time on something kind of insignificant. Added functionality for AC, CE, and = buttons. Started thinking about how to truncate repeating decimals. 

**Thoughts:** Aside from the spacing of the displayed entries, everything I worked on today was pretty doable, which was kind of nice. It was more about the little cases I hadn't thought about and wouldn't have realized without trying things out on the calculator.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/ed4e0461bfc52c198d55d82649c61e1f7dd42fd2)

### Day 8: January 9th, 2017

**Today's Progress:** Continued working on the truncate function.

**Thoughts:** I kept rethinking what I wanted this function to do and how to do it. I think I've decided what I want it to do, so now I'm trying to figure out how to actually implement it.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/f6489cbcca639c5dec132c6790a7a12f1d0de094)

### Day 9: January 10th, 2017

**Today's Progress:** Finished the truncate function.

**Thoughts:** Shortly after I started working today, I began doubting what I was doing again. I think I just didn't have a clear vision of what I wanted. How many decimal places should be displayed? Once I finished the function for the most part (I mean, I don't think it accounts for all cases), it occurred to me that maybe I don't even need this function. Without it, I punched in 1/3 and found that the threes in the resulting repeating decimal don't go on forever in the display. Maybe all I needed was to tweak the CSS a little...

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/87ffd7f9e2e996d05c60ae6e9c13b08b8d46cbf1)

### Day 10: January 11th, 2017

**Today's Progress:** Removed the truncate function from the block that displays the total. Changed the positioning of the display and its child elements.

**Thoughts:** It's a little frustrating getting really long decimal results to display nicely at narrower viewports because I don't have a great grasp of CSS still.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/81b958f58c0569e49ad9681e1f2dcf8c3dc111c9)

### Day 11: January 12th, 2017

**Today's Progress:** Got decimal button to work. Tried to get styling for the display to fit longer results but failed... 

**Thoughts:** The CSS still bothers me, but I'm trying to not let it interfere with the progress of the rest of the calculator. I tried to get the +/- button to work, but got frustrated and thought it might not be possible. Thinking about it again, I think I should be able to do it.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/b1922ba8a88e76493bddda8b79e663ca3fda769d)

### Day 12: January 13th, 2017

**Today's Progress:** Fiddled with CSS to get larger text and more space around buttons and between the display and keypad. Got calculation to update to the evaluated result after equals button is clicked, followed by an operator. Working on getting the decimal button to work properly after the equals button is clicked and displays are updated.

**Thoughts:** Seeing some \#100DaysofCode tweets in the morning motivated me to code practically first thing after eating breakfast! I still ended up procrastinating on doing the real work though. Messed around with the CSS for a while first because it was the "easy" task to tackle.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/deb903ecc8046603ba02cfb71eebcbb4ae8198f5)

### Day 13: January 14th, 2017

**Today's Progress:** Made it so clicking the decimal button after the equal button begins a new calculation instead of using the previous result. Started thinking about how to get the % button to work.

**Thoughts:** I had no idea how to get the decimal button to work properly after the equal button is clicked and the display gets updated and cleared. I was conflicted about whether I should push through with this effort or drop the extra equal button feature because it's not very important... After checking the example calculator again, I realized if the decimal button is clicked after the equal button, it just starts a new calculation and doesn't try to append to the previous result. That was a relief.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/1a20b9ef8767587567d90a63bc989707c7f9fd4d)

### Day 14: January 15th, 2017

**Today's Progress:** Got the percent button to take the last number and turn it into a percentage (if the last entry is a number).

**Thoughts:** Worked on this piece of code in repl.it, and it felt good to progress closer to what I needed the outcome to be.

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/019b9e7b9bc59335d08717b5c1e9c19b485af900)

### Day 15: January 16th, 2017

**Today's Progress:** Got the +/- button to work, similar to the % button. I worked on the CSS again to get long results display nicely. It's a little better, and that might be the best I can do.

**Thoughts:** The JS I implemented today was pretty easy, because it was almost exactly the same as yesterday's. I'm kind of dreading refactoring the code (probably tomorrow).

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/a222e857a5e08251f65b6c8ac57f2b28aeea21e3)

### Day 16: January 17th, 2017

**Today's Progress:** Fixed a small bug where clicking the CE button after clicking = didn't clear the last number since the last item in the input was the equal sign. Changed the view for wide viewports to match the vertical layout of the narrow viewport view.

**Thoughts:** I realized that I can work on CSS for hours even when it's frustrating and not doing what I expect. Refactoring (sigh) might come tomorrow after I fix another bug I discovered today. I'm excited to be done with this project though!

**Link to Work:** [Calculator App](https://github.com/tymeart/calculator/commit/7191f0764210b4cc161174476be3d355a4eaf0ee)

### Day 17: January 18th, 2017

**Today's Progress:** Fixed a bug where clicking % or +/- before a number would display NaN instead of doing nothing. Tweaked the positioning and spacing of some elements and added a border around the keypad. Wrestled with the viewport meta tag to get the calculator to look better on mobile devices. Published to Github Pages.

**Thoughts:** I learned that NaN has a type of number. The way the calculator looks is still not ideal, but it's not too bad, I suppose. I think it's probably not too accessible either... I did change the divs to actual buttons, though they don't look it. I used Chrome's different device views for the first time, which was really helpful. I struggled with landscape orientation after including the viewport meta tag, which was for some reason cutting off the top part of my calculator. In the end I got it to be decent-looking by changing the initial-scale to a number less than 1. I'm not sure if I want to refactor this while it's still fresh in my memory, or if I want to just leave it to polish when I get a portfolio up.

**Link to Work:** [Calculator App](https://tymeart.github.io/calculator/)

### Day 18: January 19th, 2017

**Today's Progress:** Started the HTML and CSS for the next FCC project. Configured Grunt and pushed the project to Github.

**Thoughts:** I thought I'd feel more reluctant to start the next project, but it was all right. It seems simpler than the calculator, but I haven't thought too much about the logic yet.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/b0974a9168a38811d50be33c07a1318de3a2bbef)

### Day 19: January 20th, 2017

**Today's Progress:** Changed font sizes and families, spacing between elements, and background and text colors. Added the labels for session length and break length. Changed the timer display to just the minutes since I'm allowing adjustment of only minutes.

**Thoughts:** There was a bit of resistance and sleepiness today. I wasn't sure what I was going to work on, but once I started I just kept going. I think tomorrow will include the challenge of animation, which is kind of exciting!

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/532448c231110222e608f82c2a2a6ba702e7b554)

### Day 20: January 21st, 2017

**Today's Progress:** Went back to the [calculator](https://github.com/tymeart/calculator/commit/f9435c418d3dda5255542d77783009314590aa32) and changed the padding around the keypad container because it was messing up the layout on some narrower viewports (I realized when I looked at it on my phone). Changed the background color on the pomodoro timer to a different yellow. Began selecting all the buttons in JS in order to add click handlers.

**Thoughts:** I still have a lot of things to learn about git and vanilla JavaScript.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/1c1467daeb2de82c9c917751959f8b9bdf0d6743)

### Day 21: January 22nd, 2017

**Today's Progress:** Added click handlers on the + and - buttons and updated the displays to match the changed number of minutes.

**Thoughts:** I did have to reference my last project a bit, but overall the click-change-update process was much quicker to code this time around. I used forEach this time instead of a for loop, but I'm still using a chained if-else if block and wonder what's a better way of getting things to work.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/72f2d86c5bf73e7f2bb285a4718924348fd37552)

### Day 22: January 23rd, 2017

**Today's Progress:** Prevented the Work Length and Break Length from going below 1.

**Thoughts:** I thought about disabling the - button once 1 was reached, but I couldn't quite figure out how to target the correct element and toggle the disabled attribute. I discovered that a simple if condition will not do anything once 1 is reached. However, disabling the buttons might still be best for UX.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/568820885c2ff6beea7b1d6d3f3cb6df4f74691a)

### Day 23: January 24th, 2017

**Today's Progress:** Got the timer to count down to 0 using setInterval. Start button toggles between 'start' and 'pause' when clicked.

**Thoughts:** This is my first time using setInterval! I was confused at first by the examples on MDN but figured it out after looking at other people's examples. Also learned a bit about the difference between innerText and textContent.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/0d9f456a4316b96f00d4e64712b085687776d74a)

### Day 24: January 25th, 2017

**Today's Progress:** Got timer to pause when the pause button is clicked. Fixed the problem of countdown speeding up when starting up again after a pause.

**Thoughts:** I was super reluctant to work today. I did put off my coding until the end of the day and couldn't concentrate much. I'm not sure if the time I worked added up to an hour, but I feel good that I got a little bit done.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/d0e2a2c7fc4d0e8c6a426e0097f2cb881c6fe75a)
