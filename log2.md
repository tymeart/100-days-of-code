# 100 Days Of Code - Log 2

### Day 1: May 12th, 2017

**Today's Progress:** Added password to the user model since I figured I'd need it later on when I add authentication. Filled in the rest of the routes (POST, PATCH, DELETE). I started checking that the views actually render properly and realized I had to move the /new route before /:username and /:username/edit, or else "new" would be considered the username. Also changed all the :id's to :username because I was confusing id with the ObjectId that Mongoose assigns each user. Passed the usernames to the view files and tweaked the view files accordingly.

**Thoughts:** It's difficult to remember the various Mongoose methods available and what parameters they take. I need to figure out how to handle errors properly, and learn how .then() works.

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/f079bab134dcf6eb5244eb25fed7c2985e2cfa16)

### Day 2: May 14th, 2017

**Today's Progress:** Changed the ${} to #{} so the edit page would render the current username. Made the update button a little more specific as to what was being updated. Instead of using findById methods, I had Mongoose find users by username, since that's what's getting passed in as a parameter. After creating a user via the form myself, I went to the show page and realized I'd rendered the entire user object instead of just the username (oops!). Changed it to access the username key, but nothing was rendering on the page. Thought it was an async issue, but it turned out that `.find()` returns an array of object(s). Probably could have just accessed the property through the array, but I went with `.findOne()`.

**Thoughts:** I was reluctant to start today because I didn't know what I had to do next. It wasn't too long before I remembered where I'd left off though, so the rest of the time working was not bad.

**Link to Work** [MojiBox](https://github.com/tymeart/mojibox/commit/475355ce186652f05717ecc973818ba65d3dd11b)
