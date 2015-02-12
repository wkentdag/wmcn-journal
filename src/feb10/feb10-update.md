###Will Kent-Daggett
###Spring 2015 COMP-614 Indepdent Study
###February 10th weekly update
---
This week I started brainstorming a to-do list for the WMCN website (and implemented the first ASAP task), sketched out a schedule for completing all of them, and began to write the API documentation (brainstorming available [here](https://github.com/wkentdag/wmcn-journal/src/feb10/use-cases.md), draft of docs  [here](https://github.com/wmcn-fm/wmcn-api/blob/master/docs/docs.md)).


For the to-do list, I separated everything that needs to be done into three categories: stuff that must be completed ASAP for the current site, minimum functionality for the revamped site, and additional features for the new site that I hope to implement this semester but that are more luxury than necessity.

####To-do:
| priority | items | notes |
|:---|:---|:---|
| **ASAP** | ~~-add timeslot selector to show approval page~~ | **finished!**
|| - add password reset | should be easy, doable by the end of the week|
| | - display show schedule on homepage | almost complete, but has been tricky/overly sluggish; maybe change to only displaying show titles, AJAXing remaining info onclick? |
|**MVP for revamped site** |- plan, write new API *documentation* and database scheme | already started - done in 2 weeks? | 
| | - build API| maybe split into two steps - pseudocode, then implementation? |
| | - rewrite current routes with new API methods | viewing user(s), show(s), playlist(s), review/news/post(s), about, schedule, login/out, dj applications, staff applications; posting playlist, review, news, post; apply for a show/staff position; edit current user/show information |
| | - implement GUI for admin "meta" portal | add ability to flush dj applications; add ability to create a new "semester", de-activating all current users and shows; add ability to turn application on/off; add ability to update static text through an interface rather than redeploying code; add ability to `mongodump` list of all users to csv through a GUI rather than command line |
| | - add page sidebars | upcoming shows, new playlists, most-read reviews, etc; also add ability to edit these lists through an interface |
| | clean up CSS - modularize, adjust padding, etc | |
| | clean up deploy methods | |
| | redeploy on non-personal cloud droplet |
| **Hopeful additions to new site** | - select shows from blank schedule displaying their availability | |
| | - playlist XML-input autofill + typeahead suggestions |
| | - add ability to sift through artist/song stats | maybe create a separate module that takes a snapshot of the artist coll every week/day, allowing for line graphs? |
| | - add cool landing page visual feature & 404 page | toggling "wmcn 91.7" colors onhover? make it parallax? |

####Schedule:
| date | tasks to be completed: |
|:---|:---|
| 2/17 | all ASAP to-do items; front-end use sketches to clarify API needs; continued progress on API docs
| 2/24 | entire API documentation, database schema, and sitemap
| 3/3 | entire API
| 3/10 | rewritten `GET`-based html routes: i.e., viewing users, shows, playlists, news
| 3/17 | **spring break**
| 3/24 | all html routes
| 3/31 | first 2 items from admin GUI to-do
| 4/7 | all admin GUI to-do
| 4/14 | add page sidebars
| 4/21 | modularize CSS, fix deploy methods; **redeploy**
| 4/28 | work on cool new additions if time allows
| 5/5 | " " 

For logging progress on these tasks, I've created a folder within the `src` directory of this repo for every tuesday of the semester.  Each folder will contain at least a `.md` file of updates for that week, along with any other pertinent notes.

###Questions:
-	what's the best practice for implementing an API that is mostly meant to power its own site rather than extend capability to other developers? 
-	should it exist in a separate github repo? 
-	should the api be hosted on a separate subdomain (eg, `api.wmcn.fm/v1/...`) or like a regular URL (`wmcn.fm/api/v1/...`)?
-	is this timeframe realistic?