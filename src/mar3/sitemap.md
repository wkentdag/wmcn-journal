# WMCN.fm sitemap

* `/`
	* `/about`
		* General station info: history, mission, hours, contact information
		* **API interaction**: needs to pull text from files that are editable from the admin interface
	* `/schedule`
		* Serves a PDF of the current semesters' show schedule. Only linked to as a print option through `wmcn.fm/shows`.
		* **API interaction**: must have an update method through the admin interface
	* `/shows`
		* Displays the current semester's show schedule in a calendar view by default; can switch to alphabetical
		* **API interaction**: `GET api.wmcn.fm/v1/shows/current`
			* fire calls to get hosts' info `onload` as well, or as ajax calls `onclick`?
		* `/:id`
			* Info on one specific show: blurb, hosts, active semesters, links to most recent playlists
			* **API interaction**: `GET api.wmcn.fm/v1/shows/:id`
		* `/now`
			* Calculates the "timeslot" given the current time, and then calls `/shows/:id` for that hour, redirecting the user to the current show's page.
			* **API interaction**: `GET api.wmcn.fm/v1/shows/:id`
	* `/staff`
		* Returns a list of all current staff. Station staff (management etc) will be listed first, followed by all DJs alphabetically. **API interaction**: `GET api.wmcn.fm/v1/users`
		* `/:id`
			* One specific user. Their active semesters, shows, links to most recent playlists, reviews, news. **API interaction**: `GET api.wmcn.fm/v1/users/:id`
	* `/apply`
		* Returns the current DJ application.
		* **API interaction**: must display text editable via the admin interface; must be able to `POST api.wmcn.fm/v1/applications`
	* `/archive`
		* landing page for the archive - display search categories and date slider
			* `?dateStart?dateEnd` - search by a particular date range
		* `/shows`
		* `/reviews`
		* `/news`
		* ^ should we even have these categories?
	* `/charts`
		* 