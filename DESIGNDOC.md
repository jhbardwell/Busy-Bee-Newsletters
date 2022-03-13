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
- Object literals with key:value metadata
- JSON files with key:value metadata
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
## System Architecture
```mermaid
%%{init: {'theme': 'base', 'themeVariables': 
{ 'fontSize': '18px', 'fontFamily': 'Inter',
'primaryColor': '#DDDA4D', 'edgeLabelBackground':'#F7F6DA', 'tertiaryColor': '#D5DEF6'}}}%%
flowchart TD
  %%relationships
  buttongeneratenewsletter--queues-->eventgeneratenewsletter
  buttonchoosedirections--queues-->eventchoosedirections
  buttonchoosetemplate--queues-->eventchoosetemplate
  buttonmaketemplate--queues-->eventmaketemplate
  databasebulletins--filtered-->mappedbulletins
  databaseebooks--filtered-->mappedebooks
  databaseauthors--filtered-->mappedauthors
  databasewebcomics--filtered-->mappedwebcomics
  ebookscraper--updates-->databaseebooks
  fxngarbage--deletes-->MAPDATABASES
  fxngenerate--generates-->HTML
  fxngenerate--runs-->garbagefxn
  fxnprocessinput--eventlistens-->EVENTS
  fxnrender--renders-->GUI
  fxnupdate--manages-->ebookscraper
  mappedbulletins--populates-->sectionbulletins
  mappedebooks--populates-->sectionebooks
  mappedauthors--populates-->sectionauthors
  mappedwebcomics--populates-->sectionwebcomics
  DIRECTIONS--manages-->MAPDATABASES
  TEMPLATES--filters-->DATABASES
   %% structure
   subgraph MAIN [Main Loop]
      fxndirections[Directions Algorithm]
      fxnprocessinput[Process User Input Function]
      fxnrender[Render GUI Function]
      fxngenerate[Create Newsletter Function]
      fxngarbage[Garbage Collection Function]
      fxnupdate[Update Ebooks Database]
      end
   subgraph EVENTS [Event Queue]
      eventchoosedirections
      eventchoosetemplate
      eventgeneratenewsletter
      eventmaketemplate
      end
   subgraph GUI [GUI]
      buttonchoosetemplate{Choose Template Buttons}
      buttonchoosedirections{Choose Directions RadioButtons}
      buttongeneratenewsletter{Generate Newsletter HTML Button}
      buttonmaketemplate{Make Template Button}
      end 
   subgraph DATABASES [Databases]
     databasebulletins[(Bulletin Content)]
     databaseebooks[(Ebooks Content)]
     databaseauthors[(Author Interview Content)]
     databasewebcomics[(Webcomics Content)]
     end
   subgraph MAPDATABASES [Mapped Databases]
     mappedbulletins[(Mapped Bulletin Content)]
     mappedebooks[(Mapped Ebooks Content)]
     mappedauthors[(Mapped Author Interview Content)]
     mappedwebcomics[(Mapped Webcomics Content)]
     end
   subgraph WEBSCRAPERS [Webscrapers]
     ebookscraper[[Ebook Content Scrapers]] 
     end
   subgraph TEMPLATES [Templates]
      fofnewsletter[Flight of Fantasy Newsletter]
      genericnewsletter[Generic Newsletter]
      end
   subgraph SECTION [Section]
      sectionbulletins[Bulletin]
      sectionebooks[Ebooks]
      sectionauthors[Author Interviews]
      sectionwebcomics[Webcomic Reviews]
      end
```

## Development Schedule
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Newsletter Concatenation Program Schedule
    excludes    weekends
    
    todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5
    
    section Plan
    Define problem scope      :done,    scope, 2022-01-06,5d
    Define target user        :done,    user, 2022-01-06, 5d
    Draft README              :done     readme, after user, 5d
    Draft DESIGNDOC           :done     designdoc, after draftdocs, 5d
    Create Architecture Flowchart  :done  architureflow, 2022-03-10, 2d
    Create 
    
    section Prototype
    
    section Prune
    
    section Playtest
    
    section Polish
    
    section Post
```
## Responsibilities
- keyed list (uml seq diagram)
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
## Reference Code
- [Image File Pixel Encoding](https://www.youtube.com/watch?v=RCVxXgJ8xSk&t=842s)
- [Template Literals](https://www.youtube.com/watch?v=DG4obitDvUA&t=2069s)

