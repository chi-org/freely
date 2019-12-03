## Description of your website, including

### Purpose
Our project is to create a web application for homeschool educators.
### Functionality / features
  - Login
  - Student setup (just a name for tagging)
  - Add/Edit/Delete an "Activity". This is like a "note" that can consist of a date (past, present or future), text, photo/video/audio, "completed" flag and tag one or more students
  - Ability to view "Activities" as a task list with filters for today, this week, and future
  - Ability to search for any activity including past and "complete" activities

### Target audience
Teachers and Educators

### Tech stack
ExpressJs ReactJs NodeJs Js MongoDB Window MacOS Wifi Chrome Android Food


## Dataflow Diagram
```javascript
user: {
    name: {
        first: String,
        last: String
    },
    dateJoined: Date,
    students: [{
        type: String
    }],
    activities: [{
        name: String,
        textContent: String,
        date: Date,
        dateCompleted: Date,
        students: [{
            type: String
        }],
        assets: [{
            type: String // assuming links to external storage, data type can change
        }]
    }]
}
```

## Application Architecture Diagram

## User Stories

## Wireframes for multiple standard screen sizes, created using industry standard software

## Screenshots of your Trello board throughout the duration of the project


```text
Our project is to create a web application for homeschool educators. It needs to be responsive and fully functional on phone, tablet and desktop. At the very least it needs the following functionality...

  - Login
  - Student setup (just a name for tagging)
  - Add/Edit/Delete an "Activity". This is like a "note" that can consist of a date (past, present or future), text, photo/video/audio, "completed" flag and tag one or more students
  - Ability to view "Activities" as a task list with filters for today, this week, and future
  - Ability to search for any activity including past and "complete" activities

  If time was to permit, the next features we would like to see are...
  - Add/Edit/Delete "Goals" that can be grouped into categories and subcategories (with no limit to the number of levels)
  - An intuitive way of tagging categories/subcategories (at any level) and/or goals when adding or editing "activities"
  - The ability to view all linked "activities" within the context of a category, subcategory or goal
  - The ability to mark a goal as "achieved"
```