###Will Kent-Daggett
###Spring 2015 COMP-614 Indepdent Study
###April 7th weekly update

---
####Progress update:

The basic API functions that I outlined in the initial docs have been completed: here is the [release link](https://github.com/wmcn-fm/wmcn-api/releases/tag/v0.1). As I mention in the notes to that release, there are several big caveats to the "complete"-ness of the API, which is why I marked it as pre-alpha.

* I have had a persistent problem establishing a connection to the database due to some trivial permissions error. Since I'm learning Postgres on the fly I have had a hard time debugging it and **haven't been able to test that any of my database calls are returning the proper results**. I know it's a permissions error because of the error feedback, and I'm assuming the calls are essentailly correct because the structure of this app mirrors that of the (working) Node-Postgres API I'm building in COMP-225, and I've set this app up exactly the same. I'm going into Paul's office hours tomorrow morning to figure it out. I'm expecting to have to tinker with the syntax a little bit to fix some assumptions I made, but for the methods to basically work as expected.
* All of the `POST` requests are currently sending fake data, although they are set up to switch to accept real data from `req.body` by uncommenting a few lines of code.
* On a related note, additional logic needs to be added to handle "real" requests. e.g., when a call is issued to `POST /playlists`, it currently just generates fake info for the columns in the playlist table (id#, content, timestamp) and dumps it into the table. The next step in development is to have the request fetch the user's `user` document from the `req.body` and add the user's id and the playlist id to the `author` table, in addition to adding the real information to the playlist table.
* I'm currently generating SQL queries using plain strings; even when using paramterized queries to provide some barrier to SQL injection, writing out multi-line strings is a pain and slows down development. The next iteration of the API will use [node-sql](https://github.com/brianc/node-sql) to generate queries instead.