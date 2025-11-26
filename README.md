Live demo : https://gmt-458-web-gis.github.io/geogame-oguzozalp/


# GeoPath Quiz – Design Documentation

## 1. Aim

This project is developed for GMT458 Web GIS Assignment 2.
The aim is to design a simple geographic quiz game that includes a temporal component and uses a mapping library inside a web environment.

The game structure is inspired by classic level-based games such as Candy Crush, but adapted to a geography-question format with multiple levels and a map background.

---

## 2. Game Concept

### **Overview**

GeoPath Quiz is a 4-level geography quiz game.
Each level contains **5 questions** with **4 multiple-choice options** displayed over a map interface.
Players must answer at least **3 out of 5 questions correctly** to complete a level.

The main objective is to provide a fun, interactive way to test geographic knowledge while integrating a geo-component using Leaflet.

---

## 3. Game Progression

### **Level Structure**

* Total of **4 levels**, visually represented on a map-style level screen.
* Each level unlocks only after the previous one is successfully completed.
* The user returns to the Level Map after each completed level.

### **Per-Level Rules**

* **5 questions** appear one by one.
* Each question has **4 answer choices**.
* The player must achieve **≥ 3 correct answers** to pass.
* The user may make **maximum 2 mistakes** in a level.

### **Time Component**

* Each level must be completed within **60 seconds**.
* If the time expires, the player fails the level.

---

## 4. Geo Component

* The quiz is displayed on top of a **Leaflet map**.
* Map may remain static or pan/zoom slightly during transitions.
* Geographical content of the questions is supported by having a map always visible in the background.

---

## 5. Number of Questions

* **5 questions per level**
* **20 questions total**

All questions will be stored in a structured JSON file.

---

## 6. Lives / Mistakes

* No global life system.
* Mistakes are evaluated **per level**.
* The user may answer **incorrectly up to 2 times** each level.
* A third wrong answer ends the level.

---

## 7. JS Libraries

### **Primary Library**

* **Leaflet.js**
  Used to display an interactive map and satisfy the geo-component requirement.

### **Additional Libraries (optional bonus)**

* **D3.js** → for animated progress bar or timer animation
* **Vanilla JS** for game logic and DOM events

---

## 8. Level Map Design (Sketch Description)

The Level Map visually resembles classic path-based games (e.g., Candy Crush):

* A pastel-colored background (static image).
* 4 round “level nodes” arranged along a curved path.

  * Level 1 → unlocked
  * Levels 2–4 → locked
* When the user clicks on an unlocked node, the quiz for that level begins.
* After successfully completing a level, the next level changes from locked to unlocked.

*(Hand-drawn or simple digital sketches are included as required in the assignment.)*

---

## 9. Quiz Screen Layout (Sketch Description)

* Top: **Countdown timer (60 seconds)**
* Center: **Question text**
* Bottom: **4 answer buttons**
* Background: **Leaflet map** (static or minimal movement)

---

## 10. Level Completion Screen

Displayed after each level:

* “Congratulations! You passed Level X.”
* Shows the number of correct answers (e.g., 4/5).
* Button: “Return to Level Map”

---

## 11. Data Source

A structured JSON file containing all questions, answer choices, and correct answers.
This approach supports clean separation of data and logic.

---

## 12. Summary

This design fulfills the requirements for:

* Geo-component (Leaflet)
* Time-based progression
* Level-based gameplay
* Frontend layout with sketches and explanation
* Clear explanation of difficulty and progression
* Stated JS libraries

The implementation phase will convert this design into a full web application hosted on GitHub Pages.

