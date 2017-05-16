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
