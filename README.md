# Mapit.io

Mapit.io is an interactive, browser based geography game inspired by Globle, where the goal is to guess a randomly selected mystery country. Players enter country names into a text input, and the map highlights the guessed country using a color gradient based on geographic distance to the target. The closer the guess, the greener the color; the farther, the redder.

This project uses open-source tools such as Leaflet.js for map rendering and **Turf.js for spatial calculations.

---

## Features

- Interactive world map powered by Leaflet.js
- Randomly selected target country each session
- 10 attempts per game, tracked dynamically
- Gradient color feedback based on shortest boundary distance
- Input-based country guessing (click-based guessing is optional and can be toggled)
- Dynamic scoreboard/table displaying guessed countries and their distances
- Confetti animation for successful guesses
- Clean UI layout with responsive behavior
- Accurate distance measurement using boundary-to-boundary calculations (not just centroids)

---

## Technologies Used

- HTML, CSS, JavaScript
- [Leaflet.js](https://leafletjs.com/) – for rendering and interacting with maps
- [Turf.js](https://turfjs.org/) – for geospatial analysis (distance calculation, centroids)
- [canvas-confetti](https://www.npmjs.com/package/canvas-confetti) – for celebratory effects
- GeoJSON – for country geometry data (based on Natural Earth data)

---

## How It Works

1. On page load, a random country is selected from a GeoJSON dataset.
2. Users guess by typing country names into an input box.
3. On each guess:
   - The script checks if the input matches a valid country.
   - It computes the shortest distance between the selected country and the target country, based on polygon boundaries.
   - The selected country is colored based on the distance, using a red → yellow → green scale.
   - The country and distance are added to a sortable scoreboard on the side.
4. If the guess is correct, confetti is launched and the game ends.
5. The game ends automatically after 10 incorrect guesses, revealing the correct answer.

---

### Prerequisites

- A local server 
- A modern web browser



