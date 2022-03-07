# Newsletter Concatenator Program
## Setup
A weekly newsletter with periodic reused content is HTML coded by hand.
## Problem
User newsletter generation is labor intensive, many parts remain unchanged or are swapped periodically, and asset records are entangled with content archives.
## Solution
Encode asset content and schedule metadata as object literals. Create JavaScript algorithm comparing pending to prior weekly contents. Make HTML template literals. Insert algorithm output. Update schedule metadata. Autogenerate newsletter HTML.
## Goals
## Features
### Critical Implemented
### Critical Unimplemented
- encode jpeg/png images as base64
### Wishlist Unimplemented
- Design webscraper to update content
- Implement webscraper
- implement button press command pattern
- Refactor to use and parse content json files
- Add pixelart effects to theme selection logos
## Schedule
## Architecture


```mermaid
journey
	title Me studying for exams
	section Exam is announced
		I start studying: 1: Me
		Make notes: 2: Me
		Ask friend for help: 3: Me, Friend
		We study togther: 5: Me, Friend
	section Exam Day
		Syllabys is incomplete: 2: Me
		Give exam: 1: Me, Friend
	section Result Declared
		I passed the exam with destinction!: 5: Me
		Friend barely gets passing marks: 2: Friend
```
