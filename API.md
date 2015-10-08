# API Documentation for Open Science Grid Interface
There will be two primary routes: job and user. 

Job will have three controllers: info create, and delete.
* info will have 4 parameters associated with it: Job ID, Status, Time, and Log
* Create will have 1 parameter associated with it: image file
* Delete will have 1 parameter associated with it: Job 

User will have four controllers: login, info, logout
* login will have 2 parameters associated with it: email and password
* info will have 3 parameters associated with it: email, phone, and password
* Logout will have 1 parameter associated with it: email
* Register will have 3 parameter associated with it: email, phone, and password

### Overview
#### Format
- /route
	* /controller
		+ parameter (HTTP method(s))

- /job
	* /info
		+ Job ID (get)
		+ status (get)
		+ time (get)
		+ log (get)
	* /create
		+ image file (post)
	* /delete
		+ Job ID (post)
- /user
	* /login
		+ email (post)
		+ password (post)
	* /info
		+ email (get/post)
		+ phone (get/post)
		+ password (get/post)
	* /logout
		+ email (post)
	* /register
		+ email (post)
		+ phone (post)
		+ password (post)
