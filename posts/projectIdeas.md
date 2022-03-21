---
title: Project Ideas
description: This is our ideas for how were going to create the project.
date: 2022-03-20
tags:
  - number 2
layout: layouts/post.njk
---
## Current Project Ideas

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
  ![clicked component](https://user-images.githubusercontent.com/73369711/159194400-3a8476fc-981d-4214-a5c7-3f767c3e9d58.JPG)


### Hash Generation with Randomized Icons/Colors
- Hash generation will be kept seperate from RPG- character seed generation.
- This feature will allow any developer to display a set of images/text in the slot for the icon.
- RPG-character will be used as default icons in our demo.
- In the case of using RPG-character, the most signifigant color will be passed into simple-colors and inverted for the element's background.