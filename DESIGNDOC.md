# Newsletter Concatenator Program
## Setup
A weekly newsletter with periodic reused content is HTML coded by hand.
## Problem
User newsletter generation is labor intensive, many parts remain unchanged or are swapped periodically, and asset records are entangled with content archives.
## Goals
- Automate repetitive tasks
- Optimize time management
- Organize and properly archive data
## Options
### Data Organization
- Text file HTML code [current]
- Object literals with key:vale metadata
- JSON files with key:vale metadata
### Data Search and Sort
- Manual [current]
- JavaScript algorithm
### Data Update
- Manual webpage search [current]
- Webscraper
### Newsletter Templates
- Text file HTML code with blanks [current]
- Template literal HTML code
### Newsletter Section Concatenation
- Manual [current]
- JavaScript algorithm
## Solution
Encode asset content and schedule metadata as object literals. Create JavaScript algorithm comparing pending to prior weekly contents. Make HTML template literals. Insert algorithm output. Update schedule metadata. Autogenerate newsletter HTML.
## Features
### Critical Implemented
### Critical Unimplemented
- Encode jpeg/png images as base64
### Wishlist Unimplemented
- Design program to periodically activate and deactivate webscraper
- Implement timer program
- Design webscraper to update content
- Implement webscraper
- Implement button press command pattern
- Refactor NCP to use and parse content json files
- Add pixelart mousemovement input effects to theme selection logos
## Development
### Process
- flowchart
### Architecture
- class chart
### Schedule
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
    Functionality added                 :milestone, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```
### Responsibilities
- keyed list
## Reference Code
- [Image File Pixel Encoding](https://www.youtube.com/watch?v=RCVxXgJ8xSk&t=842s)
- [Template Literals](https://www.youtube.com/watch?v=DG4obitDvUA&t=2069s)

