# LanternFall
A website aimed to raise awareness of the invasive species of lanternflies.
Users can sign up to view a map of their area. On the map, the user can see pins from other users.
These pins are posts from other users that signal the kill of a lanternfly. The user can post their kills with an image and text. That post will then show up on the map

# Website
* Website: [LanternFall.com](https://lanternfall.com/)
* Guest Email: guest@gmail.com
* Guest Password: guest

# How to Run
* Run a Postgres server with the tables users, kills, and images
* Users table will have id (integer), email (char varying 320), username (char varying 64), password (char 60), and total_kills (integer)
* Kills table will have id (integer), user_id (integer), date (timestamp with time zone), loc_lat (real), loc_long (real), nickname (char varying 32), description (char varying 140), img_exist (boolean)
* Images table will have id (integer), kill_id (integer), imgname (text), img (bytea)
* Input database settings into env.json
* In server.js, change SECRET to your choice
* In map.html, replace the line 'NotRealKey' with a Google Maps API key in line 58
* Run the command 'npm install'
* Run the command 'node server.js'
# How to connect securely
* Edit lanternfall.com.key and lanternfall.com.pem with your certificates
* Then edit server.js by commenting out lines 620-622
* Then uncomment lines 626-632

# Screenshots
![alt text](Images/Website.png)
![](Images/Website2.gif)

# Built With
* Node.js
* Anime.js
* Postgres
* Cloudflare
* Google Cloud

# Authors
* Chris Lijoi
* John Dominguez
* Luke Matheson
* Oliver Nguyen
* Richard Vo
