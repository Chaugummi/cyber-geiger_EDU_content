# GEIGER EDU learning content

This repo contains examples of learning content for the GEIGER Mobile Learning program in HTML format.

## Creating a new lesson
Please take the provided template and the example lesson (password/password_safety) as a reference guide.

Lessons ought to be developed mobile first. This means when opening the HTML-site in your browser make sure that a mobile-device-view is selected (Pixel 2 is here the standard).
Example: In Chrome press F12 or rightclick the page and select the "Inspect" option. Afterwards activate "Toggle device toolbar" or press Ctrl + Shift + M. Finally make sure you have the device "Pixel 2" selected.

## Editor

[BlueGriffon](http://bluegriffon.org) can be used as an editor for lessons. After opening an HTML file, the "Dual View" at the bottom of the application can be enabled and the result can be inspected live. The file can be edited in both views.

![image](https://user-images.githubusercontent.com/36758233/128883505-ffe2268b-8c06-4e7a-b9a3-9febecd9f5d6.png)

Due to the difference in screen / window size, the result in BlueGriffon may look slightly different compared to what it looks like in the app. However, the structure of the document will remain the same.

## Meta Data

Some meta data is required when creating a new lesson or lesson category. These files are standard JSON and are stored in the respective directories, for example the directory 'password' contains a lesson_category_meta.json file, while the lesson 'password/password_safety' contains a lesson_meta.json file.

### lesson_category_meta.json

A lesson category meta file contains the category ID and titles in various languages.

```json

{
  "lessonCategoryId": "CID001",
  "title": {
    "eng": "Passwords",
    "ger": "Passwörter"
  }
}

```

### lesson_meta.json

A lesson meta file contains the category and lesson IDs, titles and motivations in various languages, the estimated duration of the lesson in minutes, the difficulty, and whether it has a quiz or not.

```json

{
  "lessonId": "LPW001",
  "lessonCategoryId": "CID001",
  "title": {
    "eng": "Password Safety",
    "ger": "Passwortsicherheit"
  },
  "motivation": {
    "eng": "Improve your password security!",
    "ger": "Verbessere deine Passwortsicherheit!"
  },
  "duration": 3,
  "difficulty": 0,
  "hasQuiz": true
}

```
The difficulty attribute is defined from 0 to 2, with the levels being:
0: Beginner
1: Advanced
2: Master

The hasQuiz attribute can be defined as true or false.
