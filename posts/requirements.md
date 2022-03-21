---
title: Requirements
description: This is the requirements for our whos-here project.
date: 2022-03-20
tags:
  - another tag
layout: layouts/post.njk
---
## Project Requirements

### General Requirements
 - When the whos-here widget is on a page it should show who is there and when they last accessed
 - IP address of the user can be used to generate a hash and a random animal / photo / icon / etc should be shown
 - SimpleColors should be used to ensure that a random color that has good contrast is used
 - Back end should record when new users show up and when a new user accesses, it should see if it needs to purge any
### Back end
 - Create a data store and schema for how to store when a user was last here and a hash of who it is
 - Support multiple pages / instances in the data model
 - CREATE when the user hits the site, a call is made to the backend which tells the page WHEN someone shows up
 - READ the list of all users on the current page, delete those who are past 5 minutes of inactivity.
 - Response should include an array of hash values + animal / silly name to reference this person by
 - End point for deleting a user's record
### Front end
 - A web component for the whos-here block visually
 - A web component for the whos-here-circle that visualizes an individual
 - Use @lrnwebcomponents/simple-tooltip in order to show name and last active data on hover
 - UPDATE when a user leaves the page beforeunload can detect they are leaving and fire a call that deletes their record
 - POLL; similar to a READ but asks it to verify all users are still there. Polling should happen every 30 seconds
 - When the user accesses the page, hash the URL and send it to the end point w/ a hash of their IP address. This data informs which page someone is on for the widget but also "who" is there without leaking sensitive data