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

### Day 25: January 26th, 2017

**Today's Progress:** Made it so the timer display matches the adjusted work length interval. Pulled the setInterval function into a separate function outside of the click handler and wrote a similar function to be called when break timer starts. Tweaked placement of timer updates and changed condition for when next timer gets kicked off to make sure the countdowns start and end on the right numbers.

**Thoughts:** I'm proud that I thought of making the setInterval function into the startWork function and having startWork and startBreak call each other. I've pretty much gotten the main functionality of the timer done, and I wouldn't have made this much progress today if it weren't for the people who helped me when I got stuck. 

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/28f2add8f8c7d36610585552c1c481a6918e4ee9)

### Day 26: January 27th, 2017

**Today's Progress:** Added a circle for the clock animation and had to reposition everything within the countdown div. Started reading about some different CSS properties I could possibly use for the animation.

**Thoughts:** Positioning is so difficult! My CSS skills are still so weak... Animation is going to take longer than I expected since I have to figure out how to display the sections of a circle.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/488dcf3b27314a5ccc0dc79b32fc05ef595a2e95)

### Day 27: January 28th, 2017

**Today's Progress:** I found a tutorial for a pie chart-looking timer and tried applying it to my pomodoro timer, but I didn't understand what the CSS was doing or how to tailor it to the way my divs were already set up. I found other examples that were basically what I wanted my timer animation to look like, but I didn't understand the CSS behind them. I then found a pen for a simple CSS half circle on Codepen and decided to fork it and just play around with it to learn. I thought I would rotate two semicircles and clip certain parts of it to create the illusion I wanted. But after figuring out the rotation animation, I thought a bit more about how to link this animation up with the countdown and start/pause, it occurred to me that I should be using HTML canvas and JS, not just CSS by itself.

**Thoughts:** Determining what certain pieces of CSS did what was difficult for me since transition- and animation-related properties were still kind of unfamiliar. I was also confused about border-radius because I'd forgotten what each value represents and wrongly assumed they were the same as with margin and padding. 

**Link to Work:** [CSS Half Circle](https://codepen.io/tymeart/pen/XpzGLq)

### Day 28: January 29th, 2017

**Today's Progress:** Read around trying to figure out where to start with using JS to animate my timer. Finally found examples of canvas/JS code (on MDN!) that I would need, so I set up my canvas element and got the canvas context so I can start drawing arcs to form a circle.

**Thoughts:** Today's session was super difficult because I was dealing with sleepiness and a headache. I considered using a library like ProgressBar.js because I already feel like I'm spending more time on this project than I need to, but I'm going to write the code myself because I really want to learn more about animation.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/ab4ef2b39aeed84ad1422b966fd4e46470e2c497)

### Day 29: January 30th, 2017

**Today's Progress:** Learned how to draw arcs in canvas.

**Thoughts:** I for some reason thought that I could animate the arcs with just a for loop, but then I remembered requestAnimationFrame, so that's what I will work on tomorrow. I feel like maybe hooking the animation up with the timer countdown won't be too bad.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/5792d7f7b432f71e6b48eefad4704e5f25fd22c4)

### Day 30: January 31st, 2017

**Today's Progress:** Implemented requestAnimationFrame and a time difference to animate the arc, but stuck it in my button click handler, so it only animates a little bit before stopping and continues when the button is clicked again.

**Thoughts:** Spent most of my time looking through examples, and each of them were slightly different (and most were difficult to understand). One thing I saw repeatedly was using the Date object to get a time difference, so I decided to do the same, and I think it worked, though now I'm unsure of when the startTime actually begins. Still have to figure out how to get the arc to continue animating unless the pause button is clicked and how to keep the countdown running in sync with the animation.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/1e3808760f5a0892447d6745c7b516e846240000)

### Day 31: February 1st, 2017

**Today's Progress:** I switched from trying to use requestAnimationFrame to using setInterval to animate the arcs because I read that it's unnecessary to refresh the screen at 60fps when all I need is to get a complete circle at the end of 60 seconds. Also, rAF gets throttled even more than setInterval does when the tab is in the background??

**Thoughts:** I felt relieved when I finally got a full circle animation. With rAF in the click handler, it only animated a piece at a time and I would have to keep clicking the button. Still have to figure out how to sync the animation with my timer.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/d79b7faf5e42687e4f5fff93acf9deee61384c8e)

### Day 32: February 2nd, 2017

**Today's Progress:** Played around with placing the draw function within the existing timer setInterval, within another setInterval as well as just by itself. I added pause functionality to the draw function, but there's a huge lag when restarted after being paused. When trying out my timer setInterval with a delay of 60,000 ms (1 minute), I discovered that my countdown was not working as it should. I compared it to a stopwatch, and the number displayed wasn't changing even after 1.5 minutes. I couldn't figure out why, since when the delay was set to 1000 ms (1 second), the countdown seemed to work fine. Eventually I tried again, comparing with my stopwatch, and realized the number would finally get decremented after 2 minutes! So there's something fundamentally problematic about how I've set up (the order) of the actions within my timer setInterval callback function.

**Thoughts:** I thought I was one step closer to being done, but now it feels like I've taken two steps back. I'm going to look back at setInterval and what exactly happens when it's used, because apparently I don't understand it very well.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/23d06eb2a864af868b3460762494b30318059d92)

### Day 33: February 3rd, 2017

**Today's Progress:** I realized that the delay at the beginning of my timer was due to the nature of setInterval. It begins with a delay and then executes the callback. In order to begin with the action instead of the delay, I'm trying to invoke the callback immediately before calling setInterval. I pulled out the anonymous functions and stuck them in an updateDisplay function. However, this updateDisplay function takes in a parameter, so I think I have to write a function that will create the setInterval with the callback with the correct argument passed in.

**Thoughts:** Starting was tough because it's late and I was sleepy... I wasn't sure where to begin, but I thought I should give priority to the timer, as it's the core of this project. Creating the updateDisplay function made me feel slightly better about the DRYness of my code. It's so messy and all over the place...

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/20ad63a0f10243be5b52db60cef9909e2c4cf3cf)

### Day 34: February 4th, 2017

**Today's Progress:** I wrote a function to create setInterval with an anonymous function that calls updateDisplay, but it doesn't work. Nothing works right now. I went back and hard-coded a few things in the updateDisplay function in case my use of the parameter and template strings was incorrect and causing trouble.

**Thoughts:** The createInterval method is quite expensive because it creates a new function every time setInterval runs, but even so I feel like it should work? But it doesn't, and I'm not sure what to do now.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/7130cf1f1804fc1fffe16599028cd307e5e6b23a)

### Day 35: February 5th, 2017

**Today's Progress:** I abandoned the createInterval function from yesterday because it was inefficient and didn't work. I split the updateDisplay function into two: one for the work session and one for the break session. This way, I don't need to pass in a parameter! Instead of trying to call the function before setInterval within startWork, I decremented the workLength in a setTimeout before calling startWork so the countdown would start after the first minute and continue from there.

**Thoughts:** I *think* I've got the timer working properly now. It does decrement every minute, though I haven't checked that it still works during the break session and that it transitions between sessions properly. Now I'm back to my problem of getting the animation to sync with the countdown...

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/6fabdd2d7e1b2937f5ca82259604251000710d41)

### Day 36: February 6th, 2017

**Today's Progress:** After more reading, I think it may be impossible to sync my arc animation to the timer countdown since JS is single-threaded. I started figuring out what I need to do to get my timer to display seconds now that I can't have the animation represent them.

**Thoughts:** I was pretty down after the realization and felt like I might have to start all over. I put off working on displaying the seconds for a while. Now I've at least thought about it and psuedocoded it out, so I feel a little better.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/2bc5c303b1afaa35888b24313d730c2ed46ff486)

### Day 37: February 7th, 2017

**Today's Progress:** Rewrote work and break functions to countdown seconds as well as minutes. Included a function to update the timer display. Changed the setInterval delay so the timer updates every second.

**Thoughts:** I feel like my functions may be getting too convoluted, like I might have an extra, unnecessary wrapper function. Or is this how modular(?) it's supposed to be?

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/236046e79e5c9dbaacf5ee5cc01c0213ac265f2a)

### Day 38: February 8th, 2017

**Today's Progress:** Fixed the issue with the seconds countdown. Fixed the issue where starting a work session from less than 10 minutes would switch back to 24 minutes after the first second by changing when the timer minutes get updated with the workLength number.

**Thoughts:** I realized my process for these past two projects has been very reactive. I start with a chunk of code that I think does what I want it to, but I run it and fix it as I go. I guess that's what iterations and development are about? But part of me feels like I should be able to get much closer from the get go.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/308616182808b48bf2df241021ec76209bd9b747)

### Day 39: February 9th, 2017

**Today's Progress:** Got the timer to stop prepending zeroes to minutes less than 10. Worked on getting the work session to transition to the break session properly.

**Thoughts:** I feel like my errors are simple ones that can be fixed by moving a line of code or adding a single character, but I just can't see how to fix them.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/a6fd5343059aff88904e327f92059cf7f0e694aa)

### Day 40: February 10th, 2017

**Today's Progress:** Continued trying to get the sessions to transition properly. The timer either skips 00:00 or the beginning of the next session (5:00 in the case of the default break). I logged out the result of updateTimerDisplay when minutes and seconds are '00', and that came out undefined.

**Thoughts:** Maybe I should have thought this out more thoroughly before I jumped into the code. I can't see the flaws in my logic. I don't know how to get my timer from skipping 00:00.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/c2783cc46e72026b1b6e1d1b54ba445ffef6b559)

### Day 41: February 11th, 2017

**Today's Progress:** Put together a page for my team's hackathon project, which includes a form input and submit button. Started utilizing Semantic UI for the results of the submission.

**Thoughts:** My design skills are so weak! I don't know the best way to space things out so that they're responsive. What units should I use for what? Need to look into this...

**Link to Work:** [Gift.io](https://github.com/tymeart/gift.io/commit/a1b8cf4930e59aac9fb9d1faac0e72e9e7841c3e)

### Day 42: February 12th, 2017

**Today's Progress:** Changed spacing and alignment of various elements on the index page as well as the color of the card title texts.

**Thoughts:** Today's tweaks had to be looked up because I didn't understand what was happening/didn't know what properties would solve my problems. I was pretty content with how it looked when I passed it off, but it did get changed a bit to fit the scrolling transitions and to integrate some styling that my teammate wanted.

**Link to Work:** [Gift.io](https://github.com/tymeart/gift.io/commit/b59eb6bb552eb4f2025b2103cd24bfcbe83bbec5)

### Day 43: February 13th, 2017

**Today's Progress:** Began revamping personal site by adding full-page sections for the landing page, about me, projects, and contact info.

**Thoughts:** I'm going to go with a basic, simple layout first. Maybe I'll add more interesting shapes/designs later on.

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/0262e5dc846711d62e05c79550fdd8aaabe91fa4)

### Day 44: February 14th, 2017

**Today's Progress:** Removed full-page sizing from the sections because I decided I didn't want that kind of layout. Added anchor tags to allow jumping from the nav to specific sections. Adjusted padding for the sections so they aren't so close together.

**Thoughts:** I've been pretty reluctant to work, partly because I don't have much of a vision for how I want my page to look like. I'll get more done when I don't wait until late at night to work...

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/bcf1d236fde90544afde422b855b855fbbcde269)

### Day 45: February 15th, 2017

**Today's Progress:** Added alt attribute to the image tags. Linked calculator project, the only project on Github at the moment. Wrote short descriptions for each of the projects. Spaced out the projects and contact links with flexbox.

**Thoughts:** I should develop mobile-first...

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/47f5a6403eb075a88e68cd2e5c316155cc142efb)

### Day 46: February 16th, 2017

**Today's Progress:** Update timer display when workLength adjustment buttons are clicked. Consolidate runWorkSession and runBreakSession into one function. Add an onBreak variable to track which session the timer is on. Refactored the updateTimerDisplay function to display a string so that minutes and seconds remain numbers. Moved the clearInterval and setInterval around in the startWork and startBreak functions. Instead of running one of the functions when the start button is clicked, set an interval with runSession...

**Thoughts:** I don't think I would have been able to get this to work without help. I was so stuck with the logic at many points during the project! Just a few more little things to do, and maybe a refactoring of the code.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/6d627fe6af4cff930454c01f67063fc1a83a9a04)

### Day 47: February 17th, 2017

**Today's Progress:** Added random quote machine and Wikipedia viewer to Github and linked them in portfolio.

**Thoughts:** Yesterday, my quote machine wasn't working, but today it's suddenly working again... I discovered my weather app isn't working though, so I think I'll look into using JSONP on that and see if it works again.

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/5b6bd0ab9a116ad12122c9b5f62d3877c57e93be)

### Day 48: February 18th, 2017

**Today's Progress:** More looking at error messages about CORS issues. Tried using axios instead of getJSON, which worked locally but not on Github Pages...

**Thoughts:** I don't know if it's possible to use OpenWeatherMap API at all at this point if I can't access the data over HTTPS.

**Link to Work:** [Weather App](https://github.com/tymeart/weather-app/commit/a1a59f02da0aae35e563f776370e27161d1670df)

### Day 49: February 19th, 2017

**Today's Progress:** Gave up on getting the weather app to work because the API endpoint isn't accessible with HTTPS anyway... Added alert messages on pomodoro timer that pop up at the end of a session before beginning the next one.

**Thoughts:** Still need to fix the narrower viewport views, but I'm glad to be done with the timer.

**Link to Work** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/c402fae4c54eb07bf089fdd8474bb7d40ba04803)

### Day 50: February 20th, 2017

**Today's Progress:** I started the Responsive Web Design Fundamentals course on Udacity. Started working on making this "home town app" responsive.

**Thoughts:** I hope I can get through this course quickly and apply the gained knowledge to my own projects.

**Link to Work:** [Home Town App (Udacity)](https://classroom.udacity.com/courses/ud893/lessons/3494350031/concepts/35019794250923#)

### Day 51: February 21st, 2017

**Today's Progress:** Continued working through the Udacity course. Made it to the middle of "Common Responsive Patterns."

**Thoughts:** I've learned that I should check for widths (should be relative) and tap targets (should be about 48px x 48px) when making a responsive page. Should finish this course tomorrow, and then I'll be back on my projects.

**Link to Work:** [Mostly Fluid Pattern](https://classroom.udacity.com/courses/ud893/lessons/3561069759/concepts/36132285380923)

### Day 52: February 22nd, 2017

**Today's Progress:** Completed the Udacity course on RWD and began trying to apply some of my new knowledge on my pomodoro timer. Fixed the issue with white space in the right and bottom margins in mobile views by making padding/spacing smaller.

**Thoughts:** Even my CSS could use some refactoring...

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/59f11d43b9249798b0ac72c513ec600f0d66534f)

### Day 53: February 23rd, 2017

**Today's Progress:** Tweaked the UI of my pomodoro timer to look better on different devices. 

**Thoughts:** I had the hardest time trying to resize the start button. It turned out to be restricted in height because its container was a fixed height. When YDKCSS...

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/4ab60417f585cf9f30e9e65d8a2d8e28ca16836e)

### Day 54: February 24th, 2017

**Today's Progress:** Made a minor change to the width of the countdown div, which was causing extra (white) space on the side of the screen in some mobile views. Spent some time trying to figure out why the app wasn't working on my phone. Tried to debug with Web Inspector, but along the way I realized it wasn't even working in my desktop Safari. Found out that forEach doesn't work on the NodeList that gets returned from querySelectorAll in many browsers.

**Thoughts:** I'm glad that I now have direction on what to do next.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/3785e38b1fd3aa69599468ed8b6711f68d6c14aa)

### Day 55: Februrary 25th, 2017

**Today's Progress:** Did the first 5 exercises of learnyounode at Node School.

**Thoughts:** Since I didn't continue learning Node after the last time I went to Node School, I decided to start all over. This time I got farther a lot faster! Feel pretty good because that means I've made some progress.

**Link to Work:** [none]

### Day 56: February 26th, 2017

**Today's Progress:** I rewrote the forEach block in my pomodoro timer code to use a for loop instead, so the app should work in most mobile browsers now. Tried to fix the weird positioning in mobile Safari to no avail.

**Thoughts:** Debugging something that shows up only on a mobile device is really hard.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/9af178f0afeb5e8f03f8e0cc093a2c235657f4c0)

### Day 57: February 27th, 2017

**Today's Progress:** Decided that I'm not going to include screenshots of my projects. Rearranged the project section elements. Increased font size.

**Thoughts:** Maybe I'll change my mind again in the future, but I quite like the simplicity of it right now. Also, oops, I should be developing mobile-first.

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/dad3bd530c64ffd564bf5a506913fbc97075fc67)

### Day 58: February 28th, 2017

**Today's Progress:** Went through 3 more learnyounode exercises.

**Thoughts:** The modularize it exercise has been the toughest so far. I reread the instructions and hints multiple times and still didn't really understand where things should go and how the callbacks should work. The next two excercises involving the http module were okay, but now I'm pretty lost on the async one.

**Link to Work:** [none]

### Day 59: March 1st, 2017

**Today's Progress:** Went back to my Wikipedia viewer to make sure it looked okay and worked on mobile. I had to add the viewport meta tag, but most of the breakpoints were already set when I was working on this project originally. I also changed the "Get a random article" div to an actual button. Added the viewport meta tag to my random quote machine as well, and changed the Twitter button to an actual button as well. Added 2 breakpoints for narrower viewports. It's hard to test on my phone because my OS/version of Safari is a bit old and doesn't seem to recognize some the dimension units. Discovered that the button to get a new quote doesn't work though...

**Thoughts:** I should review the notes I took on accessibility.

**Link to Work:** [Wikipedia Viewer](https://github.com/tymeart/wikipedia-viewer/commit/e7ac28bad5636d334f5c4e5beb17cbf22cee2c02), [Random Quote Machine](https://github.com/tymeart/random-quote-machine/commit/aa562cb3a88f43d32ff3736f20b3b3f86c140814)

### Day 60: March 2nd, 2017

**Today's Progress:** Changed the click handler on the new quote button from .click() to .on() with click and touch events. Included vendor prefixes. Added a fallback of definite pixels for the quote box min-height since calc() isn't supported on all browsers.

**Thoughts:** Despite all this, my app does not work on my phone. I checked it on my friend's HTC One, and it worked, so I'm hoping it works all right in newer browsers than mine. I should check if my apps work in Firefox!

**Link to Work:** [Random Quote Machine](https://github.com/tymeart/random-quote-machine/commit/f785577d3976a4c52bbe481f7ba8f7bc921004aa)

### Day 61: March 3rd, 2017

**Today's Progress:** Centered all the section contents, which weren't displaying as centered on narrower viewports. Increased the h1 font size a bit. Aligned the project titles to the right so they didn't leave odd-looking spaces when breaking onto new lines. Added more padding below the project descriptions. Rearranged the social media links to be vertical in narrower viewports and horizontal in viewports wider than 600px.

**Thoughts:** I was about to work on the tribute page project, but then I figured working on my portfolio page would be more beneficial right now. Still don't know what to write about myself... Anyway, I kind of want to have the project titles and descriptions aligned, but I think I'd have to use tables and not flexbox to get that effect. Hmm...

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/079df9f9f6b21e46527c6cef132701b069e820eb)

### Day 62: March 4th, 2017

**Today's Progress:** Changed the projects section to a column layout on narrower viewports. Began adding colors.

**Thoughts:** I just realized that in order to support all browsers, I would have to not rely solely on flexbox. That makes me wonder if I should go back to using floats first as a fallback and then add flexbox for newer browsers. But isn't that redundant? Anyways, I don't have a vision for how I want my portfolio page to look aesthetically, so I'm kind of okay with the plainness right now.

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/3da42edebb5ddab9dbfcf0436d39c385e210e946)

### Day 63: March 5th, 2017

**Today's Progress:** I started working on my tribute page since I'm not sure what to work on, and I think it's about time I learn Bootstrap. I was going to review by going through the old FCC exercises, but the version of Bootstrap that Codepen includes is version 4, so I'm looking to the docs for reference instead.

**Thoughts:** Too sleepy to get very far...

**Link to Work:** [Tribute Page](http://codepen.io/tymeart/pen/LWRVPe?editors=1100)

### Day 64: March 6th, 2017

**Today's Progress:** Decided not to include a photo of Sol LeWitt and use a photo of one of his Wall Drawings guidelines instead. Debated between a broader summary of his contributions and a timeline of his life. Decided to go with the latter and began including a couple of the details.

**Thoughts:** I felt pretty unmotivated to learn every bit of Bootstrap as well as to read through all the details that are online about LeWitt's life, even though those are the points of this project.

**Link to Work:** [Tribute Page](https://codepen.io/tymeart/pen/LWRVPe?editors=1100)

### Day 65: March 7th, 2017

**Today's Progress:** Started working on the visuals of a pretend milk tea review blog.

**Thoughts:** I didn't feel like working on the tribute page, so I asked my friend what website I should make. Her answer: a milk tea review blog. I had an initial idea for the layout but might go in a completely different direction. I asked my friend for suggestions on the blog title (probably wouldn't stick with it if this were real) and color pairs. This was pretty fun! I think it's been a while since I've really played and let myself experience the creative process like this without worrying about the practicalities.

**Link to Work:** [Milk Tea Review Blog](http://codepen.io/tymeart/pen/LWbgRL?editors=1100)

### Day 66: March 8th, 2017

**Today's Progress:** Tried to get the posts to wrap around the circle using shape-outside but haven't figured out why it's not working yet.

**Thoughts:** The circle div itself seems to have everything it's supposed to, so I wonder if the issue is the fact that my list of posts is a flex box?

**Link to Work:** [Milk Tea Review Blog](https://codepen.io/tymeart/pen/LWbgRL?editors=1100)

### Day 67: March 9th, 2017

**Today's Progress:** I finally got the text to wrap around the circle!

**Thoughts:** Eventually I realized that it wasn't my circle that was wrong, because it met the requirements for shape-outside to be used. I hid my original text and pasted in some lorem ipsum in paragraph tags, and to my surprise it wrapped the way I wanted it to! I tried wrapping the paragraph tags into list items in an unordered list, the way I had my original text, and it still worked. After commenting out some properties to see how it affected the text, I discovered that my problem was that I had set my ul to a certain width.

**Link to Work:** [Milk Tea Review Blog](https://codepen.io/tymeart/pen/LWbgRL?editors=1100)

### Day 68: March 10th, 2017

**Today's Progress:** Learned to make a triangle with CSS. I wanted to see how I could fill it with text, but I think that would require using the shape-inside property, which needs a definite width and height.

**Thoughts:** I spent more time looking for how to use shape-inside than actually trying it out. I'm excited to figure this out!

**Link to Work:** [CSS Shapes](http://codepen.io/tymeart/pen/qrrQVo?editors=1100)

### Day 69: March 11th, 2017

**Today's Progress:** Worked on Material-UI card components for my team's project at a React hackathon. We're building a way for groups to vote on restaurants they would like to eat at and ultimately to make a reservation for the one with the most upvotes. 

**Thoughts:** Styling in React is weird. I'm surprised how rigid Material-UI is compared to Semantic UI and maybe Bootstrap? I can't seem to change the width of these cards I have; I can only change the width of the container that holds them.

**Link to Work:** [Reserve.io](https://github.com/tymeart/reserve.io/commit/81797b62eae76e07d27b8b43babf30b35f743154)

### Day 70: March 12th, 2017

**Today's Progress:** Continued refining our UI. Found out how to change the width of each card so there would be a couple in a row rather than all in a column. Set a couple of breakpoints so our app would be a little bit more responsive. Learned some things about git workflow.

**Thoughts:** My knowledge of React is so little that I was able to only do some styling. Working on this project was a good review of that small part of React, but I should have pushed myself to learn more.

**Link to Work:** [Reserve.io](https://github.com/tymeart/reserve.io/commit/dfc65777f98b8a2813b7fbf9d69332aba6c673ec)

### Day 71: March 13th, 2017

**Today's Progress:** Set up the project with Gulp.

**Thoughts:** Am I ever going to remember the viewport meta tag without looking it up? haha Gulp is much faster than Grunt, and the config file is easier to read! I have no idea yet how I'm going to make this game work.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/blob/master/index.html)

### Day 72: March 14th, 2017

**Today's Progress:** Figured out that I linked my stylesheet in the HTML file wrong lol. Styled the play buttons a bit and added a start button and strict mode button.

**Thoughts:** After trying to get my random quote machine to work on my phone (and not doing so well), I'm debating about whether to use flexbox and percentages in my CSS for better older browser compatibility.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/0daeac9af3d71e874be636dd61231260b3b869c6)

### Day 73: March 15th, 2017

**Today's Progress:** Renamed the divs related to the buttons that will be pressed during play. Positioned the play buttons so they were two on top and two on the bottom, then added a clipping path to the container to make it look like a circle. Spaced out the play button container and the controls.

**Thoughts:** Decided to just go with flexbox... Since I'm nearly done with styling though, I'll have to start thinking about the logic behind the game soon.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/5a12f8c67aea406fba543ccb5f7233c869b0a76f)

### Day 74: March 16th, 2017

**Today's Progress:** Changed the play button colors and made the hover states lighter versions of those colors. Styled the control panel and its elements. Started learning how to make a toggle switch in CSS for the strict mode.

**Thoughts:** This is the first time I'm not making my buttons flat! Exciting~

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/2f2067648784a09449a6ba320e622893a4afa4ad)

### Day 75: March 17th, 2017

**Today's Progress:** Worked on making a toggle switch in isolation so I can add one into my Simon game in place of the Strict button.

**Thoughts:** I think I should go back and review how absolute and relative positioning work. Also display: block/inline-block/inline.

**Link to Work:** [Toggle Switch](https://codepen.io/tymeart/pen/mWqwzm?editors=1100)

### Day 76: March 18th, 2017

**Today's Progress:** Added a toggle switch in place of the strict button.

**Thoughts:** Sass let me do some crazy nesting, but it's probably not a good idea to write like that since it's difficult to understand? Even with the nesting, my knowlede of sass is so limited and I feel like it could've been written it DRYer.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/2bf446eea344ab828092aa27e03e620d8ffbfa0a)

### Day 77: March 19th, 2017

**Today's Progress:** Made the last style adjustments for the time being. Changed the blue because it was too similar to the green. Lightened the yellow a bit. Made the background a little bit lighter and changed the control panel grays to yellower hues to match the background. Began thinking about how the game is actually going to work.

**Thoughts:** I'm relieved that I have some idea how to make this work.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/e0b4eac09533d66a58089a5319e1a8d9d7457121)

### Day 78: March 20th, 2017

**Today's Progress:** Began coding out the randomizing of button light-ups. The random order is done, I think, but now I'm trying to figure out how to actually make the buttons light up.

**Thoughts:** I think this randomizer will have to be a function. I feel like maybe the "proper" way to do this is to think about what functions you need first, and then write them, rather than writing code and grouping it into functions??

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/91c54f638c84cf90cd686d7787d9aac4537b8561)

### Day 79: March 21st, 2017

**Today's Progress:** I spent most of the afternoon trying to get freeCodeCamp to run locally (MongoDB!) and looking through issues to possibly take on, but I don't think that counts as coding. I started learning about CSS grid layout. Didn't get any visible results, and I wonder if it's my browser.

**Thoughts:** At first, it was quite difficult to wrap my head around how to use a grid layout, and I was thinking about it like I think about flexbox. I'm beginning to see that's like drawing out a structure/scaffold and then placing items within (or even outside!) it. I think it'll be really difficult for me to make these layouts without drawing out the grid structure first on paper, because I find it hard to visualize the columns and rows.

**Link to Work:** [CSS Grid](https://codepen.io/tymeart/pen/BWrPGK)

### Day 80: March 22nd, 2017

**Todays' Progress:** Changed the lightened colors to 20% lighter. Changed the count number class to an id and initiate a count variable to keep track of what round the game is on. Have the count increase every round. Started thinking about updating the count display. Changed demoArr to computerPlays to be clear that the array is what the computer "presses." Changed the ids of the play buttons to reflect the colors instead of numbers. Go through each item in computerPlays, add the lightup class to each button, and remove it after 1 second.

**Thoughts:** I'm still stuck on how to get the buttons to actually light up, since each button is a different color. Overlay the button with white? I was extremely reluctant to work on this today, partly because I'm unsure how to do what I need to do, partly because I'm not that interested in this project... But I feel like since I already started, I might as well try to finish.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/3bd688761e09f2e08b54cc892d8b52617b5e535b)

### Day 81: March 25th, 2017

**Today's Progress:** While looking at a pen that happened to be on the front page of Codepen, I realized I could change an element's opacity on hover. I believe this is somethhing I already knew, *and* it's how my friend told me he did the "light-ups" in his Simon game. Perhaps I was being stubborn about finding a way to do it by changing the background color of the buttons... After finally getting past this button light-up issue, I pulled some of my code into separate functions and began working on handling the user's button presses.

**Thoughts:** I'm wondering if making all these separate functions is a good/bad practice? I feel so much better about working on this project now that I've cleared a major block.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/fc7dc0491bcea0186b44f5b455a6a0a31f52e7d8)

### Day 82: March 26th, 2017

**Today's Progress:** Finished the basic first iteration of what I planned in my pseudocode. Began realizing how complex this is going to get. Started looking in to how to get the buttons to play audio when clicked.

**Thoughts:** I haven't actually tried any of the code I've written so far to see if it does what I want it to. I'm certain the setTimeouts won't work inside the for loops I've set them in. Need to figure out how that actually works...

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/5554a90969cbb8bccb9c48014282618216459d6d)

### Day 83: March 27th, 2017

**Today's Progress:** I added instances of the audio clips that should play when the play buttons are chosen by the computer/clicked by the user. For running the computer plays, I moved the adding and removing of the lightup class inside a switch statement. For getting the user's button clicks, I added an switch statment to play the correct sounds.

**Thoughts:** My refactoring of the runComputerPlays function made it a lot longer and more repetitive...

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/14830933c9c42f289b1126ebef164382f78d52f0)

### Day 84: April 4th, 2017

**Today's Progress:** I started a new project! I started adding styles to get the basic positioning and sizing of the main components.

**Thoughts:** I haven't gotten to the new and difficult things yet, but I'm excited to work on something that I would use often!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/689ae0cf9bf72e305a2bdada943e8e7fdf9a7b66)

### Day 85: April 6th, 2017

**Today's Progress:** Installed Chromedriver to be able to run axe-cli tests in Chrome, but it turned out I didn't really even need to since the default is PhantomJS. Tested my portfolio page, Pomodoro Timer, and Wikipedia Viewer. My portfolio page had no violations, and the Pomodoro Timer only had one easily fixable one. Wikipedia Viewer had the most violations (3), so I went through and fixed them.

**Thoughts:** The button on the Wikipedia Viewer failed the color contrast rule, which surprised me because I thought it was a decent contrast. Seeing how dark a color has to be against white text for a good contrast rating was pretty eye-opening.

**Link to Work:** [Pomodoro Timer](https://github.com/tymeart/pomodoro/commit/4915543cb740adb1da8da2a36491f02bd2a63e2e), [Wikipedia Viewer](https://github.com/tymeart/wikipedia-viewer/commit/6b4711479d3e4526b9c0f65f8b785bd08dfba5b1)

### Day 86: April 7th, 2017

**Today's Progress:** Increased font size. Styled elements to have rounded corners. Started positioning the divs within the collection div.

**Thoughts:** Positioning elements so they wrap onto the next row at smaller viewports didn't seem like it would be difficult. That part was okay, but it was the spacing on the (current) second row that is the problem. I don't think flexbox can arrange all the items to one side and leave spaces to the right when there aren't enough items to fill the whole row. Guess I should learn CSS grid!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/a64755f4568a7e36896c7c217b74593694052fd6)

### Day 87: April 9th, 2017

**Today's Progress:** Wrapped the getComputerPlays call in a for loop so it runs the appropriate number of times for the round number. Changed the var keyword to let in the for loop that includes a setTimeout. Added the lang attribute to the html tag. Moved the if statement at the end that compares the computerPlays and userPlays into the startGame function, modified it so it would break out of the loop if the user clicks the wrong button.

**Thoughts:** I'm kind of surprised that I actually felt like working on this project today. My code is still terribly messy, but for now I'm going to leave the refactoring for later.

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/4527d40a951a4dcf9632d72604c5f437c7313a8d)

### Day 88: April 10th, 2017

**Today's Progress:** Included a way to track what mode the game is in (strict or regular) by creating a variable and changing its value whenever the state of the strict mode toggle is changed. Modified the condition at the end of startGame to break out of the loop only when strict mode is on. Added a click listener on the start button so startGame will run when it is clicked. Somehow I had two separate sets of styles for the start class, so I combined them when I changed the class to an id. Also removed the styling that made the play buttons change colors on hover.

**Thoughts:** I think I can finally check to see if any of my code works. I probably should have done so a long time ago... I need to remember to put a limit on the number of rounds. 

**Link to Work:** [Simon Game](https://github.com/tymeart/simon/commit/1f95562dfe679b3b4bdd86121b54f93b23d68e76)

### Day 89: April 11th, 2017

**Today's Progress:** I did the little exercise at the end of the introductory Node and NPM lesson in Rithm School's free online courses. It had me use fs.appendFile and the request module to get data from an API, which are things I'd never done in Node before. Also continued through the intro to Express lessons but haven't tackled the exercise at the end of that yet.

**Thoughts:** The basic Node exercise was pretty simple, but the Express stuff was harder to understand, I guess because I'm not too familiar with routing and request & response yet. It's still kind of confusing.

**Link to Work:** [Rithm School Node exercise](https://github.com/tymeart/rithm-school-exercises/blob/master/node-exercises/main.js)

### Day 90: April 13th, 2017

**Today's Progress:** Changed the font styles. Kept trying different heights for the sections. Fussed with getting certain elements centered on older browsers.

**Thoughts:** I still have trouble getting websites to look okay on different devices, and that's kind of disappointing.

**Link to Work:** [Portfolio Page](https://github.com/tymeart/tymeart.github.io/commit/9a03025f4d08feb0788a98e60c57fa610b4d7775)

### Day 91: April 14th, 2017

**Today's Progress:** Worked on the Pug template for the '/' route. Had to look up how to iterate through an array and have it display each as a list item in an unordered list. Had to look up how to link a stylesheet and how the folder structure has to be set up to be used with Express. Started trying to put a search bar on the index page as well, but haven't figured out the template inheritance yet.

**Thoughts:** I was surprised how long doing these Pug templates took.

**Link to Work:** [Rithm School Intro to Express exercise](https://github.com/tymeart/rithm-school-exercises/commit/4c6e67ecdd49deee32c31013204044264d2e63b4)
