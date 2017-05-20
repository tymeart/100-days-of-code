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
