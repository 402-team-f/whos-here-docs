---
title: Notes
description: This is our ideas for how were going to create the project.
date: 2022-03-20
tags:
  - number 2
layout: layouts/post.njk
---
## Final Week
Woooooo!
- We got users displaying and polling every 30 seconds
- Deleting users is still in the works
- OpenAPI is done
- IP integration is not working but we replaced with working solution
- Able to delete all users currently but will be removed when it is not needed later
- Tooltip stlying is close as well as 'Anonymous' names
- All rpg sizing, ring, accent color are working and actually look good!
- Will be changing to the '+[other user amount]' next

## Week 14

### Front End
- changed the method of detecting user activeness
- hashes username to get ring color
- will be adding resizing from the new rpg-character update 

### Back End
- Added delete endpoint but not fully set up yet
- (?) tried changes for all endpoint in both the endpoint itself and where they are being called in fetch but keep getting an error with the db
  - I can't figure out if I missed a step setting up the planetscale or if my endpoints/fetches are wrong

## Week 13

### Front End
- Added tooltips
- added username changeability
- added last accessed
- added functionality for watching if a user is active

### Back End
- fixed db structure
- made more endpoints
- progressed on endpoints

### API
- started openAPI/swagger and researched how to implement project

## Week 12

### Database
- planetscale fully connected to project (auth.js returns the whole table when ran)
  - note for getting database content: pscale connect whos-here-db main --execute 'node api/auth.js'
- added some db endpoints but they still need some testing to see if they work right
- need to link endpoints to their functionality on front end

### Front End
- added front end to crop rpg character to the right size with a ring around the head
- rpg-character images don't currently load on vercel site but load locally. need to figure out image plugin to make it work
- once figure out the resizing of rpg characters will add other functionality (expanding on click, editiable username, etc.)

- How it looks locally:
-![local current status](https://user-images.githubusercontent.com/73369711/161682672-906dd0fd-437b-4f4d-983e-cf6171e5f6b6.JPG)

- How it looks on Vercel:
-![vercel current status](https://user-images.githubusercontent.com/73369711/161682682-6e54ee39-ec55-4f45-945c-fd68d857da57.JPG)

## Week 11
- put together flow of whos-here code between the user, front, and backend
- ![project flow](https://user-images.githubusercontent.com/73369711/160329180-0245894f-8933-45c1-acbb-7af2def41b4a.JPG)
- created visualization of db table
- ![db diagram](https://user-images.githubusercontent.com/73369711/160329138-7c2c39fa-28b8-4813-849c-c9b57b1041dc.JPG)
- deployed project repo to vercel
- will begin frontend, backend, and api coding this week

## Week 10

### Idea 1
- whos here will have 2 states
  - State 1: default, a circle with background color and icon in the circle
  ![default component](https://user-images.githubusercontent.com/73369711/159194339-92ebdfb2-aedd-4583-9554-1481f62bb0e4.JPG)
  - State 2: when hovered, a tooltip will appear with user's "name" (anonymous [animal]) and last accessed data
  ![hovered component](https://user-images.githubusercontent.com/73369711/159194360-2880a5e1-ea2a-4497-92ee-c60a9b397787.JPG)

### Idea 2
- whos here will have 3 states
  - State 1: default, a circle with background color and icon in the circle
  ![default component](https://user-images.githubusercontent.com/73369711/159194372-fbf9a5ef-0e33-479a-8a5b-9ef0bc1930cd.JPG)
  - State 2: when hovered, a tooltip will appear with user's "name" (anonymous [animal]) and last accessed data
  ![hovered component](https://user-images.githubusercontent.com/73369711/159194393-f45958ca-01d1-4600-b05e-daa351d930a3.JPG)
  - State 3: when clicked, default state will enlarge horizontally to a rectangular shape with icon, user's "name", and last accessed data. When whos-here is not hovered over anymore after click, it will return to default position
  ![clicked component](https://user-images.githubusercontent.com/73369711/159196319-58b4bd82-d542-42c7-a670-077dd28fcbc6.JPG)

### Hash Generation with Randomized Icons/Colors
- Hash generation will be kept seperate from RPG- character seed generation.
- This feature will allow any developer to display a set of images/text in the slot for the icon.
- RPG-character will be used as default icons in our demo.
- In the case of using RPG-character, the most signifigant color will be passed into simple-colors and inverted for the element's background.
