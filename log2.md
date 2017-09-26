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

**Thoughts:** I was super confused at first, but after reviewing some of the React challenges on FCC, I figured out how to pass the props so the app worked the way I wanted it to. I'm still confused about what kind of components to use in different cases (stateful vs stateless/class component vs functional component) and how to write them.

**Link to Work:** [Markdown Previewer](https://github.com/tymeart/markdown-previewer/commit/776bda027b54192269b3402f1a190088c4df8b0d)

### Day 4: August 3rd, 2017

**Today's Progress:** Spent some time going through a couple of the Redux challenges on FCC. Decided to just jump into the next FCC React project, the Camper Leaderboard. I set it up and started laying out the table component. 

**Thoughts:** So far I'm having a hard time figuring out how to separate this app into components. Like will each row be a user component with each user's stats? Do I break that component into smaller components? Kind of intimidated about how to filter/sort by clicking a button/link, but that will come later.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/b10f14ef4b10c8298998054db487190e428c4a87)

### Day 5: August 4th, 2017

**Today's Progress:** Renamed the Board component to Table because I thought it would be clearer. Initialized state in the App component with an array for the users. Made an API call with axios to get the top 100 campers in the last 30 days and set `this.state.users` to that array.

**Thoughts:** I'm still uncertain about whether I should break the Users component into smaller components, but I suppose if I need to I can do that later. I feel good about jumping into the API call but still need to figure out how to pass the data around.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/ae8d77e67e8e7bdd87dfeb426ad10509e8d8ff82)

### Day 6: August 5th, 2017

**Today's Progress:** Passed the data to Table and iterated over the array to render each user's info in a table row. Made another API call for the list of top campers of all time and set that data to another property in the state. Added buttons to click to show the two lists of campers.

**Thoughts:** I was glad I was able to properly render the list of recent campers and learned that you can't pass an object as a prop. Now I'm trying to figure out how to display the two sets of data. This problem makes me wonder about accessibility in React. At first I was going to make the table headings <a> tags, but I wouldn't have an href, which I think might be bad practice? I made them buttons instead, but I'm not sure that's the right move either.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/b604ec8633e922627251361e4de3cec084396320)

### Day 7: August 6th, 2017

**Today's Progress:** Moved the buttons from the table header to outside the table because I couldn't figure out how to pass props with them inside (I felt like I would have to pass the props from child to parent). I'll move them back once I figure out how to do this passing of props.

**Thoughts:** I'm really stuck on how to render each set of data on the click of the buttons. In my mind it's so simple, but clearly I still don't have a good understanding of props and how to pass them.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/ee3d2d26a78709deab3ef76552de800e529792df)

### Day 8: August 7th, 2017

**Today's Progress:** Still pushing things around, not having a clear idea of what to do. Moved the API calls to an `updateUsers` function and made it one call that depends on the option passed in. That will set the state for a single users key instead of having two keys/ separate arrays for each data set, which makes sense since only one set will be showed at a time. I haven't figured out how to pass the correct option in though.

**Thoughts:** I've been looking at examples trying to figure out how to make the display change on click, but I'm still quite lost.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/ee3d2d26a78709deab3ef76552de800e529792df)

### Day 9: August 8th, 2017

**Today's Progress:** Got my SortButtons to work! They now load the correct data when clicked. The main problem I was having was that I wasn't accessing the prop (function) passed to SortButton. At one point, it was automatically and continuously making the API calls and rerendering the table on its own. There's something I don't understand going on with the binding, but the way it is right now works...

**Thoughts:** The solution ended up being much simpler than I thought. I guess I was comparing to the FCC example project, which does have a few more features than mine does. It also has more components. I might make the table rows into a User component. This project has me wondering about accessibility and UX/design patterns. I like the way the example project has table headings clickable, which makes it look like the sorting in your email. For me that's intuitive, but I don't know if it is for most other people? The alternative is what I have right now: clear buttons outside of the table. It's probably good for people using screenreaders?

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/41b75f812b6cf375f2a21a0a27007847d1510a59)

### Day 10: August 9th, 2017

**Today's Progress:** Linked the usernames to the respective user profile pages and styled the links a bit. Made the buttons larger and more cohesive color-wise.

**Thoughts:** I think since I left the buttons I need to make it clearer how the list is currently being sorted.

**Link to Work:** [Camper Leaderboard](https://github.com/tymeart/camper-leaderboard/commit/1a7b084235a43e8361c74c19b66f5093528033e2)

### Day 11: August 10th, 2017

**Today's Progress:** Started adding highlighting (background color) to a column to show how the list of users was currently being sorted. To do this, I added one of two classes to all the items in each point column and started writing a function that would add/remove a class to the items in the column.

**Thoughts:** I wrote the new function very naively, with a lengthy if/else statement. When I started up the app, I was getting an error saying that function was not defined. I couldn't figure out why; I thought maybe I was using the wrong variable keywords..

**Link to Work:** [Camper Leaderboard](https://tymeart.github.io/camper-leaderboard)

### Day 12: August 11th, 2017

**Today's Progress:** Figured out that my function was "not defined" because I needed to call it with `this`. Had to iterate through the column items since it was a nodelist, which I'd forgotten. This got me very close, but I noticed that some of the column items were not hightlighted. My guess was that the data loading and data rendering were sort of clashing, so I moved the function call into the `updateUsers` function and chained it to the end.

**Thoughts:** I feel good that I pushed through the problems I was facing and found solutions.

**Link to Work:** [Camper Leaderboard](https://tymeart.github.io/camper-leaderboard)

### Day 13: August 12th, 2017

**Today's Progress:** Finished the final exercise in the learnyounode workshopper from Node School. The hardest part was figuring out what different Date methods would return and how I could use each one. Then I wasn't sure how to get the results to display (not with `return` but with `res.end()`.

**Thoughts:** I'm glad I finally finished this workshopper, but since I worked on it over the course of several months, I've forgotten a lot and still don't have a very good idea of how Node works. I suppose this was only supposed to be an intro, but there's nothing in particular I can say I've taken away from working through these exercises.

**Link to Work:** [learnyounode](https://github.com/tymeart/learnyounode/commit/c9baabf4450a7734e7987c6bfa5e9f133da064b6)

### Day 14: August 13th, 2017

**Today's Progress:** Wireframed a bit and set up the project. Made a separate folder for components and a file for each component. Imported referenced files as I went.

**Thoughts:** I still don't have a good idea of the differences among various ways to write components...

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/44be8a458549f79243888c31e29535f0f384e0e3)

### Day 15: August 14th, 2017

**Today's Progress:** Fixed some JSX that was causing errors. Hard-coded some recipe objects into the state so I could try passing something to the various components. Successfully rendered the sidebar! Started styling it as well.

**Thoughts:** I kind of can't believe I successfully passed the recipes properly (ha).

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/d5bdc73aaf784bebd6245502ec6a8f218d04317e)

### Day 16: August 15th, 2017

**Today's Progress:** Added a right border to the sidebar and resized the button. Refactored the RecipeList to include RecipeListItem.

**Thoughts:** Using RecipeListItem inside of RecipeList was kind of difficult because I was getting confused about how to pass and access the props.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/dbc1890432590d27b87f89b0632d3896767c05a4)

### Day 17: August 16th, 2017

**Today's Progress:** Realized that I should make the main tag into a component, so I did that. Looked at the example project's code since I'm pretty stuck, and they have the ingredients as an array, which makes sense, so I changed my ingredients to also be an array of strings rather than a single string. Tried to write a function that gets run when a recipe title is clicked on, but I don't know how to make MainSection render different things based on the target of the click...

**Thoughts:** Getting to work today was really tough. I was procrastinating because I don't know how to move forward.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/f12f6ca50ef381965e2a1acbaa2a60712fa3491a)

### Day 18: August 17th, 2017

**Today's Progress:** Broke some components onto more lines for more readability because I was adding so many attributes. Other than that, I kept trying to make something render in the MainSection on click of the RecipeListItems. I tried changing how I structured the recipes data in the state. I briefly thought putting the click handler functions in the Sidebar would work out, but then realized it had to be higher up (in the parent) if I wanted to pass the state to MainSection, which is the sibling of Sidebar.

**Thoughts:** After talking to someone for help, I've learned that I either need to use Redux or not break the app into so many components/have one single component? At least I have a better idea of what to do now.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/23e90e0d4d024b99331a6d87689e09824f8fb4a4)

### Day 19: August 18th, 2017

**Today's Progress:** I was still unsure of what to do at the beginning of today's work session. I was looking for forum discussion on this project but didn't find much else besides people's finished projects. So I took a look at two, and [one of them](https://codepen.io/eddyerburgh/pen/xVeJvB?editors=0010) was helpful even though it initially seemed very different from what I wanted to do. They wrote a function to find the index of something in their data, and I thought I should do the same for my problem. It occurred to me yesterday, but for some reason I thought implementing it wasn't a good idea? It isn't very optimal the way I've set it up, but I did get recipe details to render on the click of recipe titles in the sidebar! Also have `MainSection` render only when `this.state.display` isn't null.

**Thoughts:** Yesterday there were a lot of different thoughts entangled and I couldn't move forward in any direction. I'm glad I've finally made progress and can move on to the next problem.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/b945eb3f8e888c12fdc5abc817ee0ec8acb84c23)

### Day 20: August 19th, 2017

**Today's Progress:** Tried to get different components to render inside `MainSection` but didn't know how to set things up to do that. I added an ingredients key to the recipes since I do want to have those in the end.

**Thoughts:** Architecture is hard.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/f8b1bb17910658a83fa29da325f51d885c64406f)

### Day 21: August 21st, 2017

**Today's Progress:** Added keys to the App state to use later in conditional rendering. It works, except once again I've run into the problem of getting the correct recipe to render.

**Thoughts:** I almost didn't work on this project today because I was feeling so stuck. But it is a little bit easier to think when you're not falling asleep...

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/3e78c70bd1fecb27c04c10858c3fd8464f7b700a)

### Day 22: August 22nd, 2017

**Today's Progress:** Finally got recipe details and recipe form to render in `MainSection` when the recipe titles and button are clicked on. I set intital state of `displayRecipe` to null so I could setState to the recipe object when the title is clicked in the sidebar. Then for displaying the form, I just have `displayForm` toggle between true and false since what gets rendered doesn't change (static form that doesn't require passed in data). I was having trouble with the conditional renders, which I finally figured out was mainly because of what I was setting as initial state. Types have to stay the same (?), and {} is truthy.

**Thoughts:** I'm so glad I finally got past the problem I had. I feel like I was struggling for so long! I also have a better idea about how to utilize localStorage, which is the next step.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/4e858c8c5308cb71bdbe27839a4436a6efc6556b)

### Day 23: August 23rd, 2017

**Today's Progress:** Styled some of the MainSection by adding padding to the right side because text was stretching too far that way. Made the edit and delete buttons in the RecipeDetails bigger and positioned them in the corner. Added a Google font for once instead of just going with "serif" or "sans-serif." Started working on getting the form submission to save new recipes by looking into how to access input values from multiple input fields.

**Thoughts:** I feel kind of bad that I didn't tackle the thing I need to do to make progress but sort of procrastinated by working on the look of things.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/06912f059b7f0c8d725b07e26cc324c52830b0b5)

### Day 24: August 24th, 2017

**Today's Progress:** I thought using refs in an uncontrolled component would be the way to handle multiple inputs in a form, but actually it wasn't necessary. I made separate onChange handlers for the input fields and one for the submit button. Then I had each input correspond to a piece of state, which determines the value of the input. Clicking the submit button logged the values of each input, which means now I just have to figure out how to incorporate localStorage.

**Thoughts:** Selecting an item out of a list seems like a very common problem to solve, but I guess I didn't search hard enough.. The way I did it was kind of hacky, and I think I should go back to Stephen Grider's YouTube search project to see how to do it in a better way.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/537b134b433d01f01db99f944b0ca9496570b2b6)

### Day 25: August 26th, 2017

**Today's Progress:** Moved the initial recipes from state to an array outside of the App class. Included a function to check for support and availability of localStorage and initialized the recipes.

**Thoughts:** I'm not sure if I initialized the object in localStorage properly... I still have to figure out how to parse the ingredients and instructions. Not sure if I should keep them as strings in an array or if I should put everything into a single string.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/0cb064032bace0e904222c8252d8e2eca56c184f)

### Day 26: August 27th, 2017

**Today's Progress:** Started including localStorage in the `handleSubmit` function so adding a new recipe will save it in localStorage. Also added a few more comments to the code in `componentWillMount` about things to do.

**Thoughts:** I'm still trying to figure out the logic of what should happen and under what conditions.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/6e4ce916e23ec4a79485a4e792775bbd35d3053b)

### Day 27: August 28th, 2017

**Today's Progress:** Looking at my code, I was confused and not getting anywhere with figuring out the logic, so I wrote it out on paper. It became very clear that I had a piece of functionality that I would repeat again and again, so I know I need to break that into a separate function. Started extracting the recipes from localStorage into something I can setState to later.

**Thoughts:** It's funny how effective writing/drawing things out with pen and paper is.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/859087b8326fc6957989b33b3b61113357ba084f)

### Day 28: August 29th, 2017

**Today's Progress:** I changed the instructions from an array of strings back to a single string because I figure that's how it'll be when the user clicks the submit button. Stringified the object containing the recipe ingredients and instructions since localStorage only takes strings. Then I parsed it when retrieving it to be set in state. Sliced the title that ultimately gets passed into setState. Because of the format of things that are saved into localStorage, I had to change how I was accessing the data (array indices + object keys instead of solely object keys). After doing that and getting some errors, I found out I wasn't stringifying & parsing the objects because that object was either coming back null or as the string literal "[object Object]".

**Thoughts:** I need to fix the way I'm determining if it's the first time the user has visited the page, or maybe I just need to remove the first-visit-indicator. For the most part the app is still working with localStorage, yay!

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/2c7d4d30f98f6cd4ea930ae5cd4ae606548bd23a)

### Day 29: August 31st, 2017

**Today's Progress:** Made some small changes, like the names of the handlers that deal with the inputs in the add recipe form and the wording of the alert message if localStorage is not available. Added newline characters in the instructions strings. Learned about the `pre` tag and white-space properties in CSS. Pulled out the code that gets the recipes from localStorage and set them in state and put that into an `updateRecipeState` function. Got the recipe form working! Things were breaking because I was trying to use JSON.parse() on the object containing the recipe ingredients and instructions. I was getting an error that usually appears when you try to use JSON.parse() on something that's already an object. But when I logged the object at a specific index, it returned piece of a string. In the end I used JSON.parse() in the childe component that renders the data, and that worked.

**Thoughts:** I feel like I accomplished a lot today.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/552197ce9f7a94d13928d93cf782b2877135b5b4)

### Day 30: September 1st, 2017

**Today's Progress:** Made the delete button work. Since I needed access to the current recipe, I bound the handler function to the button and passed in the current recipe title, which that component had access to. Started trying to figure out how to make the edit feature work.

**Thoughts:** At least that's how I think the binding and passing values works... I did the same thing for the camper leaderboard, but I understood it less at the time. I was confused as to why I had to still use .bind() when I had already defined the function as an arrow function, but I kind of get it now.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/292cd953506c2a4eafcf4f953a5d0349f934c794)

### Day 31: September 2nd, 2017

**Today's Progress:** Made it so the MainSection clears whenever a new recipe is saved and when the delete button is clicked by changing some state in the `updateRecipeState` function. Started adding a component for the edit form, but I might be able to reuse the form component for adding a recipe... Made a new click handler for the edit button. I'm trying to pass it the current recipe the same way I did with the delete button.

**Thoughts:** It feels good to be able to reason about how to connect things in React now. There are so many links to keep track of (at least without Redux).

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/16c56030930901e5095142c2503783305b7fc1b5)

### Day 32: September 3rd, 2017

**Today's Progress:** Wrote the function to handle the submission of the edit form. It looks pretty similar to the function that handles the new recipe submission except I delete the old recipe if the title is edited.

**Thoughts:** Reusing the new recipe submit form seems possible, but I think it might be clearer if they're separate.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/8907990b8a9a50898e3da074e0d083aa7fdcf51a)

### Day 33: September 5th, 2017

**Today's Progress:** Made it so the MainSection is cleared when `updateRecipeState` runs and when a recipe in the sidebar is clicked when the edit form is displayed. I set the values in the edit form to those of the current recipe. I spent a while trying to figure out how to pass the old, uneditted recipe to the submit edit handler. I looked at someone else's project to see how they did it, and it was so simple! Just delete the old recipe and add a new recipe with whatever values are in the edit form. I was talking to a friend about component state and relearned that not all the state has to be in the top level component. So I'm trying to refactor my forms so that they manage their own state for the text inputs. However, I need to figure out how to get the submit handlers to work again since those I think I need to keep in the App component where they will update state. In the edit form, I noticed the ingredients are comma separated but without spaces after the commas, so I fixed that.

**Thoughts:** I think I should include a "Cancel" button on both of the forms. There's still so much to learn about using React.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/1eb1f7024645410e3f052416594523841c44efc6)

### Day 34: September 6th, 2017

**Today's Progress:** Finished moving the change handlers for the forms from the App component to the individual form components. Then I passed the recipe data from the forms to the submit button handlers. I logged some things and it seems like the submit handlers are receiving the correct data, but maybe there's something wrong with the way I'm manipulating it because I'm not getting the results I want at the moment...

**Thoughts:** I realized that even though I'm making sure the recipe titles and ingredients aren't empty, it's still possible for someone to input a space or a bunch of spaces.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/0b693cb20a15df9ed5de858d492b8dba0da16b32)

### Day 35: September 7th, 2017

**Today's Progress:** Finally got the submit handlers on both forms working. It turns out it wasn't working on the new recipe form because I had to change where it was pulling the title and ingredients to check if they were empty. I was checking the state instead of the form data. Also added cancel buttons on the two forms and got those to work. The edit form returns to the recipe details view when cancelled.

**Thoughts:** I've got the main functionality of the app done, I think! Yay! Now I'm trying to add transitions.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/cebbeb112f92f8ddcfe605bf0f712db44ea6f308)

### Day 36: September 8th, 2017

**Today's Progress:** Added CSS transitions to the components that appear in MainSection (recipe details, recipe form, and edit form).

**Thoughts:** It was surprisingly difficult to figure out how to get the transitions to work. At first I also installed the wrong version of the react-transition-group package because v1.x are the ones that are stable, not the latest v2.x?? Then I wasn't sure which components `<CSSTransitionGroup>` should wrap (how far down the parent/child chain?). Anyway, I finally got it working, though there is no transition between clicked recipes since they're within the same component. The transition to the forms is kind of weird and jerky, so I'll have to see if I can tweak that. 

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/63ca34a912cd1c750805636bd25c934058acb662)

### Day 37: September 9th, 2017

**Today's Progress:** Altered the transition speeds so that recipe details appeared faster and the forms entered and left slower. Changed the sidebar color to orange and rounded all the buttons. Added a keyline below the recipe heading, which required redistributing the spacing. Changed the cursor when hovering over buttons and recipe titles in the sidebar. I noticed that there was white space (not orange) below the sidebar for one of the recipes that was longer, so I fixed that by adding padding on the bottom of the sidebar to match the padding on the bottom of the main section.

**Thoughts:** I woke up a little earlier to work because I was going to be busy the whole day, and I felt like I got a lot of work done!

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/bf4eee0d7188f528be49d7ab58095d823497ebc2)

### Day 38: September 10th, 2017

**Today's Progress:** Mainly worked on styling the forms today, which included the color of the input field borders and button colors. Added a line to clarify the expected format for the ingredients. Increased letter spacing on buttons. Tweaked the colors for the recipe title borders in the sidebar and the keylines.

**Thoughts:** I attended a retrospective talk about how front-end web development has changed over the years, and proptypes in React came up briefly. I think I should've been using them this whole time, especially because I had so much trouble with the types of data getting passed around.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/2904e830baf6bb911e6f3172240da752124325a4)

### Day 39: September 12th, 2017

**Today's Progress:** I was going to add a confirmation when the delete button is clicked, but I realized I should make it a little bit harder to accidentally click it. I moved it to the view with the edit form and left it in that corner in the heading while the submit and cancel buttons are at the bottom. Added hover color and transition to the delete button as well. Made it so recipes are displayed right after being created or editted.

**Thoughts:** There are more things I could do, especially with refactoring, but I don't feel like working on this project much longer.

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/b42fb00b389b77718fa4ff42ebaff91a9ba8f395)

### Day 40: September 14th, 2017

**Today's Progress:** I spent some time truncating recipe titles in the sidebar, and I got that to work, but then it meant I would have to change the way the recipe details are accessed (I guess I was relying on the recipe title in the sidebar). I didn't like the way the truncated titles looked anyway, so I scrapped that idea. Went ahead and deployed the app. I also started working on some styling for the Noisebridge library app, though I don't want to push the changes up yet.

**Thoughts:** Although there are many things I could do to improve Recipe Box as it is now, the point was to learn React, not build a great recipe app. It could benefit from some refactoring, but I don't really know how to go about doing it at this point...

**Link to Work:** [Recipe Box](https://github.com/tymeart/recipe-box/commit/8c78914b80928faca546ffdcd49b23f54ce76aa9)

### Day 41: September 15th, 2017

**Today's Progress:** Changed the layout of the books list to a grid of cards. Made the alt attributes on images (book covers) a little more specific by having them include the title of the book. The title and author for each book card were heading tags, so I changed them to p tags. Also got rid of a span that didn't seem to be used at all.

**Thoughts:** My flexbox understanding could use some work.

**Link to Work:** [Noisebridge Library App](https://github.com/nb-library-wg/nb-library-react/commit/6d17ca9c46ed86e06428d8f9352408b35d35bade)

### Day 42: September 16th, 2017

**Today's Progress:** Started changing the layout of my portfolio page to be a grid layout of my projects. I'm going to add images later on, so I added spans as placeholders for now. I also went back to my Random Quote Generator to change the AJAX call to use cors-anywhere since crossorigin.me doesn't seem to be working anymore.

**Thoughts:** I don't know how I'm going to make this layout unique. I was inspired by my friend [Sasha's portfolio site](https://sashatran.com), but I don't want mine to be that close of a copy to hers...

**Link to Work:** [Portfolio](https://github.com/tymeart/tymeart.github.io/commit/eb40c043cb840a622e669379edde9a5d7b366837)

### Day 43: September 17th, 2017

**Today's Progress:** I took out the Google fonts and background gradient since I don't like them that much anymore. Changed the font sizes to rem. I moved the social media links to the header and added space between the h1 and the top of the page as well as between the h1 and the paragraph below it. Shortened the calculator description since it was so much longer than the others'. Added flex-grow to the project titles and descriptions so that they take up the remaining space.

**Thoughts:** I still don't know how I'm going to do the project tiles. I took screenshots of the projects (except MojiBox for now), but I'm worried they won't look very nice all together in a grid.

**Link to Work:** [Portfolio](https://github.com/tymeart/tymeart.github.io/commit/26b193ab56a945f141498bbb4df94b455e360088)

### Day 44: September 18th, 2017

**Today's Progress:** I made the links in the project cards larger so they fill up the entire card. This moved the text to the center of the card, and I don't mind this look. I might add the screenshots as background images. Changed the social media text links to icons, which involved some reading about how to make them accessible.

**Thoughts:** The use of `aria-hidden` was a bit difficult to understand, but I guess that was because I didn't understand the non-decorative use of icons?

**Link to Work:** [Portfolio](https://github.com/tymeart/tymeart.github.io/commit/89b2403fdcee2f308c18815620d106339c5d5423)

### Day 45: September 19th, 2017

**Today's Progress:** I mainly worked on the Redux challenges on Free Code Camp, so I didn't push anything to Github...

**Thoughts:** It's confusing so far. They're just functions and objects, but there are so many terms!

**Link to Work:** none

### Day 46: September 20th, 2017

**Today's Progress:** I made really small changes in my portfolio page. Just a few wording things in 2 of the project descriptions and adding more spacing. Then I got sucked into editing all my project READMEs.

**Thoughts:** I should really go ahead and add the images to see if I like them in the background.

**Link to Work:** [Portfolio](https://github.com/tymeart/tymeart.github.io/commit/e7bd7196c1b7f3e15f61e7d0b6949c29aecf0f1c)

### Day 47: September 21st, 2017

**Today's Progress:** I finished the Redux challenges on FCC. Started the process of deploying MojiBox, so I deployed the Mongo database and set the database url to the environment variable.

**Thoughts:** When I started the challenges today, I was super confused about all the terms. It was tough following the lessons because I had to stop and recall what each thing was multiple times. But by the time I finished the Redux challenges, I think things were becoming clearer.

**Link to Work:** none

### Day 48: September 22nd, 2017

**Today's Progress:** Finished deploying MojiBox. Set the local env variable for the Mongo url as well as the key on Heroku. Changed the port on `app.listen` since Heroku sets its own port.

**Thoughts:** Did have to Google some error messages, but it was a relatively easy process. I wish I could have the mojibox url name on Heroku!

**Link to Work:** [MojiBox](https://github.com/tymeart/mojibox/commit/84cbde68c1501063486ef1a625014e84a33a0886)

### Day 49: September 23rd, 2017

**Today's Progress:** Updated the MojiBox link with the deployed Heroku app one. Cropped my screenshots and added them into a folder in the project. I was originally going to set each background manually since the entire page is hard coded, but now I'm considering making it a bit more dynamic and putting all the project info into JS objects. Went ahead and merged the new layout into master since it's close to being done.

**Thoughts:** The layout is still so boring...

**Link to Work:** [Portfolio](https://github.com/tymeart/tymeart.github.io/commit/5176022534057a0bc57998c19c24edd3874311af)

### Day 50: September 24th, 2017

**Today's Progress:** Created my to do app yesterday and set up the components today. Took me a few minutes to recall how to map over items in an array and render each one with the items as separate components in the list component. Also took me a bit to figure out how to do handler functions again. Still trying to remember/figure out what I should do the state with regards to the submit handler.

**Thoughts:** Good thing I'm making this app, because I obviously need to review and strengthen my React skills.

**Link to Work:** [To Do](https://github.com/tymeart/todo/commit/b79ba5ff02be08f21c72fb6f1ea67913d8040a73)

### Day 51: September 25th, 2017

**Today's Progress:** Moved App.js and App.test.js to the components folder and changed the title of the page. Had a bit of trouble getting the tasks to render in the list after submitting, but got it to work.

**Thoughts:** I kept having to check what I did in my last project. I'm trying to learn alternative ways of doing things by looking at someone else's React to do app. There's still so much I don't understand. I want to clear the input field after submitting, but I'm not sure how to do that yet.

**Link to Work:** [To Do](https://github.com/tymeart/todo/commit/1399c049802440a450c88b8c157466cd1034411d)
