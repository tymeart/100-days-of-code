# 100 Days Of Code - Log 2

### Day 1: May 12th, 2017

**Today's Progress:** Added password to the user model since I figured I'd need it later on when I add authentication. Filled in the rest of the routes (POST, PATCH, DELETE). I started checking that the views actually render properly and realized I had to move the /new route before /:username and /:username/edit, or else "new" would be considered the username. Also changed all the :id's to :username because I was confusing id with the ObjectId that Mongoose assigns each user. Passed the usernames to the view files and tweaked the view files accordingly.

**Thoughts:** It's difficult to remember the various Mongoose methods available and what parameters they take. I need to figure out how to handle errors properly, and learn how .then() works.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/f079bab134dcf6eb5244eb25fed7c2985e2cfa16)

### Day 2: May 14th, 2017

**Today's Progress:** Changed the ${} to #{} so the edit page would render the current username. Made the update button a little more specific as to what was being updated. Instead of using findById methods, I had Mongoose find users by username, since that's what's getting passed in as a parameter. After creating a user via the form myself, I went to the show page and realized I'd rendered the entire user object instead of just the username (oops!). Changed it to access the username key, but nothing was rendering on the page. Thought it was an async issue, but it turned out that `.find()` returns an array of object(s). Probably could have just accessed the property through the array, but I went with `.findOne()`.

**Thoughts:** I was reluctant to start today because I didn't know what I had to do next. It wasn't too long before I remembered where I'd left off though, so the rest of the time working was not bad.

**Link to Work** [MojiBox](https://github.com/tymeart/mojibox/commit/475355ce186652f05717ecc973818ba65d3dd11b)

### Day 3: May 15th, 2017

**Today's Progress:** Changed the interpolated JS in three places in the edit Pug file to access the username rather than the entire user object. Changed the `.findOne()` to `.findOneAndUpdate()` in the PATCH request because the changes I was making weren't being saved. Finished checking the user routes and what they were doing/displaying. Moved the emoticon view files to their own folder. Started going through the emoticon routes but have messed up the index view somehow.

**Thoughts:** I was super reluctant to work today. It's tough when you don't have a clear vision of what you need to do next. I kind of have an idea now, so hopefully tomorrow will be easier.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/9c9f12a6677ae2953ff16ee95388976896b958d7)

### Day 4: May 16th, 2017

**Today's Progress:** Added `.catch()` to all the promises I have for basic error handling. I think this probably isn't the best way to do it? Need to look up best practice. Spent the longest time trying to figure out why my root page wasn't rendering at all, and it turned out it was because I had `Emoticon.find()` instead of `db.Emoticon.find()`! Finished the emoticons POST request by finding the current user in the database, creating a new document in the database with data from the form as well as the found user's id, and pushing the newly added emoticon to the user's emoticons array. There was a lot of editing of not-specific-enough action paths and accessing properties on objects rather than passing/rendering entire objects. Basically have the routes done, I think.

**Thoughts:** I had help, but I feel good that I got a lot done today. Next step is styling and adding links to access the different routes.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/d44e71d4e06d323a67540ce50188ce951640bcc1)

### Day 5: May 17th, 2017

**Today's Progress:** Thought about how to do the DELETE request in the emoticon routes but decided to move on to UI for today. Connected the form labels to the input fields in the form to add an emoticon. Added some Semantic UI classes to style the form. Attempted to get the navbar in the index page to look the way I want. I still haven't figured out how to center items, but I did manage to properly right-align items.

**Thoughts:** Sometimes CSS frameworks are frustrating because you don't fully understand what's going on under the hood...

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/cf06939c1053176077c3f1bd7b665416784559aa)

### Day 6: May 18th, 2017

**Today's Progress:** Did parts of a few React tutorials. Decided to jump into the first React project on Free Code Camp. I created, rendered, and styled two components.

**Thoughts:** Not sure if this project is actually as simple as it seems. At the moment it seems like it'd be okay to have just 2 main components.

**Link to Work:** [Markdown Previewer](https://github.com/tymeart/markdown-previewer/commit/d060f697aa405c51029d73a9cb6b81d50c7dbf72)

### Day 7: May 19th, 2017

**Today's Progress:** Moved the navbar to base.pug so it's rendered on all pages. Added a container around all the block content on pages that didn't already have one, and styled that so the content wouldn't be hidden by the navbar. Added classes to h1's and buttons to style them. 

**Thoughts:** I still have the hardest time trying to get whitespace in Pug, but I think maybe it's impossible to get it in certain cases doing it with the pipe character. I found out I can just interpolate it, so that's a relief!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/982c02c8f10320f127d374df122378d32779de8b)

### Day 8: May 20th, 2017

**Today's Progress:** Mostly went through all the forms and styled them along with some headers and buttons I hadn't gotten to yet. Linked the "Add" link in the nav to the actual /new page. Centered all the main content on the page with flexbox. Deleted a couple of view files from the emoticons route that I didn't actually use.

**Thoughts:** I think I've finished the most basic styling. There are still little things to do to make it look nicer, but I think it's time to move back into the backend. Still gotta do authentication!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/cc0ba79c6ec04def642a56181ff9e5dcaca78513)

### Day 9: May 22nd, 2017

**Today's Progress:** Changed the emoticon route index page from finding all the emoticons to finding one user, populating its emoticons array, and passing that data to the view file. Found out the POST request from trying to add an emoticon to the collection doesn't do what I want it to do. As far as I've figured out, it's perhaps because I'm pushing in the emoticon's id rather than its content.

**Thoughts:** I was a bit excited to start adding in auth, but it looks like I have issues to sort out before that.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/b0dcc4e11278fd88cce0428dd564d3f9f48ae19d)

### Day 10: May 23rd, 2017

**Today's Progress:** Found out that newly added emoticons weren't rendering on the collection page because they weren't being saved after being pushed into the user's emoticons array. Used `.markModified()` and `.save()` to tell Mongo that the array had changed and to save it. It worked! Passed user to the index.pug file in the '/' route so base.pug would have access to the correct username in the links.

**Thoughts:** There was less reluctance to start working today because I had an idea of what to do next. Got some help from Shav (wouldn't have known to use `.markModified()` otherwise), so solving problems was a little smoother.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/4e0dc83f7c0b2b4e586ebb8416634386c60c1157)

### Day 11: May 24th, 2017

**Today's Progress:** Added a js folder to the public folder where I started writing the click handler for selecting emoticons to eventually delete. Forgot how to select and add event listeners using vanilla JavaScript, so I did a lot of Googling. Ended up taking some time learning about event propagation and event defaults. I have something that may or may not work at the moment.

**Thoughts:** I got worried because if I were to be asked to write some kind of event handler in vanilla JS in an interview, I really don't know what I would have done. Same with explaining event propagation/default. Good thing it wasn't an interview and I was free to Google all the things!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/eedf8435103c827da77124d7d8b0966acf8708af)

### Day 12: May 25th, 2017

**Today's Progress:** Had trouble linking my click handler code to my app. I thought all I had to do was put the file in the public folder, but it turns out you have to link to it with a script tag, which makes sense. Spent a while trying to figure out how to write the file path in the src, and it turns out you don't need to include `public/`. Added a background color to the hover state of the emoticon divs. Once I got it working, I made the 'selected' class toggle so the user can deselect.

**Thoughts:** I'm glad I had someone to ask for help. Note: need to check the array of selections and remove emoticons from it when they're deselected.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/2e58bef09b556253492eebdd397d0aaca6db76a5)

### Day 13: May 27th, 2017

**Today's Progress:** Went back and reviewed the learnyounode exercises that involve the http module. Rewrote the last one I did using the bl module, which I somehow didn't use the first time around even though it's in the hints... Started working on the Juggling Async exercise, and what I have right now only works sometimes.

**Thoughts:** I still haven't wrapped my head around async... Or rather, how to deal with async. :<
 
**Link to Work:** [NodeSchool learnyounode workshopper](https://github.com/tymeart/learnyounode/commit/273ad1a523aceae5b26a5393e1ec6528c4498cda)

### Day 14: May 28th, 2017

**Today's Progress:** Continued working on the Juggling Async exercise of learnyounode. Stuck the http get request in a function and ran that through a for loop, but it's not returning any data this way. This is practically the same as what I had before, I now realize. I searched for more hints but haven't fully understood those hints or solutions yet.

**Thoughts:** It's frustrating because this is such a core part of Node and I can't figure out how to deal with it.

**Link to Work:** [NodeSchool learnyounode workshopper](https://github.com/tymeart/learnyounode/commit/d0d209bc7e6e5270705aa2b205a83388239ea9e7)

### Day 15: May 30th, 2017

**Today's Progress:** Added a variable to keep track of the select mode and made it so you can toggle select mode by clicking the "Select" link in the navbar. Added a delete button below the emoticons container that appears when selectMode is true. Now user can select and click delete when the app is in select mode. In order to push the selected emoticons into the `selected` array, I wrote a function that pushes into the array if the emoticon doesn't already exist in it and removes the emoticon if it does already exist in the array. Started trying to figure out how to pass this array to the routes.

**Thoughts:** I feel like I got a lot of work done today. Need to set up authentication before I can finish the delete route.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/3bde929a83ee04655b485dc57712776407252d2d)

-----------------------------------------------
### Day 1: July 31st, 2017

**Today's Progress:** I went back to the markdown previewer project since I just finished FCC's React challenges and have a much better grasp of React now than when I started. I worked with what I had previously for a while, but it occurred to me that I couldn't pass the state around the way I wanted to. Then I realized that I could just move all the JSX into one component instead of separating the main one  into two smaller ones. I'm not sure it would have worked with the smaller components without Redux? So finally my input text was outputting things in the right place! Then I had to figure out how to get the HTML to render instead of text in tags. It turns out you have to pass the parsed markdown as a dangerouslySetInnerHTML prop.

**Thoughts:** It feels good that I'm finally beginning to understand passing props in React! I was so lost in the beginning.

**Link to Work:** [Markdown Previewer](https://github.com/tymeart/markdown-previewer/commit/9ad44e0ac51baf570c9fb7b2547c87278125ae5a)

### Day 2: August 1st, 2017

**Today's Progress:** Made various changes to the styling: set the same font for all text, changed some of the spacing, added purple coloring. Added a heading to the page for accessibility. Included a breakpoint media query so the app would look a little better on smaller viewports. Deployed to Github Pages.

**Thoughts:** I was feeling so good about my progress yesterday and today, but I told someone about this app today and he was saying that my sticking everything into one component wasn't how you're supposed to use React. I realized he was right, but I was also really upset and felt dumb for being so happy that I figured it out when I really didn't...

**Link to Work:** [Markdown Previewer](https://github.com/tymeart/markdown-previewer/commit/3ff03a688311e83e3c99e5eb9e5dadf4d538f5ee)

### Day 3: August 2nd, 2017

**Today's Progress:** Refactored my code so the App component is composed of several other components instead of rendering all the JSX itself. I pulled the header into the App component as well since it was weird to have it outside. Added a background color to the code blocks so it would be more obvious that they're lines of code.

**Thoughts:** I was super confused at first, but after reviewing some of the React challenges on FCC, I figured out how to pass the props so the app worked the way I wanted it to.

**Link to Work:** [Markdown Previewer](https://github.com/tymeart/markdown-previewer/commit/776bda027b54192269b3402f1a190088c4df8b0d)
