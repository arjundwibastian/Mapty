# Mapty 🗺️

A workout-tracking app I built while working through **Jonas Schmedtmann's "The Complete JavaScript Course"** on Udemy, using **object-oriented JavaScript** (classes).

Click anywhere on the map to log a workout at that spot. Add your distance, duration and a bit of type-specific info, and it shows up both as a marker on the map and a card in the sidebar. Everything is saved in `localStorage`, so it's still there when you reload.

## How to use

1. Allow location access when the browser asks (the map centres on you).
2. Click a spot on the map.
3. Choose **Running** or **Cycling** and fill in the fields (fields swap depending on the type).
4. Hit **Enter** to save. A marker appears, and a card is added to the sidebar.
5. Click a card to pan the map back to that workout.

Running tracks **cadence** and pace (min/km); cycling tracks **elevation gain** and speed (km/h).

## What I learned

- Object-oriented programming with `class`, `constructor`, `extends` and `super`
- Inheritance: a `Workout` base class with `Running` and `Cycling` subclasses
- Encapsulating the whole app in an `App` class with methods
- Binding `this` in event listeners with `.bind()`
- Drawing markers and popups with the **Leaflet** library
- Geolocation with `navigator.geolocation.getCurrentPosition`
- Persisting data in `localStorage` with `JSON.stringify` / `JSON.parse`

## Files

- `index.html` — the layout (loads Leaflet from a CDN)
- `style.css` — the styling
- `script.js` — the classes and app logic
- `logo.png`, `icon.png` — assets

## Running it

The app needs a **secure context** for geolocation, so opening the file directly with `file://` may block location access. Serve the folder locally instead — for example the **Live Server** VS Code extension, or:

```bash
npx serve
```

Then open the given `localhost` URL. You'll also need an internet connection (Leaflet and the map tiles load from a CDN).

## Credit

Project idea and starter HTML/CSS come from the course:
[The Complete JavaScript Course: From Zero to Expert! — Jonas Schmedtmann](https://www.udemy.com/course/the-complete-javascript-course/)
