# wmcn-journal

progress journal for spring 2015 [wmcn.fm](http://www.wmcn.fm) development

[api repo](https://github.com/wmcn-fm/wmcn-api)

####To-do:
| priority | items | notes |
|:---|:---|:---|
| **ASAP** | ~~-add timeslot selector to show approval page~~ | **finished!**
|| - ~~add password reset~~ | should be easy, doable by the end of the week|
| | - ~~display show schedule on homepage~~ | almost complete, but has been tricky/overly sluggish; maybe change to only displaying show titles, AJAXing remaining info onclick? |
|**MVP for revamped site** |- ~~plan, write new API *documentation* and database scheme~~ | already started - done in 2 weeks?| 
| | - build API| maybe split into two steps - ~~pseudocode~~, then implementation? |
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
| 2/17 | ~~all ASAP to-do items; front-end use sketches to clarify API needs; continued progress on API docs~~
| 2/24 | ~~partial api docs~~
| 3/3 | ~~entire API documentation, database schema, and sitemap~~
| 3/10 | entire API
| 3/17 | **spring break**
| 3/24 | rewritten `GET`-based html routes: i.e., viewing users, shows, playlists, news
| 3/31 | all html routes
| 4/7 | first 2 items from admin GUI to-do
| 4/14 | all admin GUI to-do
| 4/21 | add page sidebars
| 4/28 | modularize CSS, fix deploy methods; **redeploy**
| 5/5 | work on cool new additions if time allows
