#site use cases:

###public:
-	listen to the station
-	check what show is currently playing
	-	`GET /onair` or `GET /shows/now`
-	browse schedule for a specific show
	-	`GET /schedule`, `GET /schedule/:timeslot` 
-	browse  archived playlists/reviews/posts/news
	-	`GET /all [?], /playlists, /reviews, /posts, /news`
	-	`GET /{content-type}/:author`, `GET /{content-type}/:date`,
	-	`GET /all/:type, :date, :author`
-	get a specific review/post/news article/playlist
	-	`GET wmcn.fm/{content-type}/{year}/{month}/{day}/{slug}`, e.g. `wmcn.fm/playlist/2015/2/4/my-great-show`
-	apply to be a dj/staff
	-	`GET /apply` for both applications, auth will display staff application only to those who already have an account
-	search station contact info, history, mission, etc.
	-	`GET /about`, maybe `GET /contact` too
-	browse all/individual shows
	-	`GET /shows`, `GET /shows/:title` - maybe this brings up a need for display title vs slug, for better URIs that aren't the doc id or some other super long string
-	**?** browse all/individual djs
	-	`GET /staff`, `GET /staff/:name` for specific members. 

###dj:
-	log in/out
	-	`POST /login`, `/logout`
-	playlist:
	-	`POST /playlist`
	-	`PUT /playlist/:...`
-	edit contact info
	-	`PUT /staff/:name` ?
	-	`PUTaqwsd4 /staff/:name/pw` ? for updating password
-	**?** edit show description
	-	`PUT /shows/:timeslot` <-- only allow edits for live shows?
	
-	/rules...??

###staff:
-	review/post/news:
	-	post `POST /{content-type}`
	-	put/update `PUT /{content-type}/:...`



###admin:
-	review/post/news:
	-	post
	-	put/update
	-	delete `DELETE /{content-type}/:...`
-	dj/staff applications:
	-	get `GET /dj-applications`, `GET /staff-applications`
	-	put/update (both administrative approval as well as regular submitting)
	-	delete `DELETE /dj-applications` deletes the collection, `DELETE /dj-applications/:id...` deletes individual
-	users:
	-	view all/individual
		-	`GET /users` <-- active users, not all staff; `GET /users/:name? id?`
		-	including permissions
	-	put/update all/individual
		-	`PUT /users, /users/:...`
	-	delete all/individual
		-	`DELETE /users, /users/:...`
-	shows:
	-	view all/individual
		-	`GET /shows, /shows/:title, :timeslot`
	-	put/update all/individual
		-	`PUT /shows, /shows/:title`
	-	delete all/individual	
-	meta:
	-	open/close application page
		-	`GET /apply/open, /close` or `POST/DELETE /apply/manage` ?
	-	edit application fields & text
		-	`PUT /apply`
	-	create new "semester"
		-	`PUT /schedule` ?
	-	edit site text
		-	`PUT /about`
