# Nimbus — Weather App

A premium, dark-themed weather web app built with vanilla HTML, CSS, and JavaScript. Features live weather data, animated backgrounds, liquid glass UI, and an interactive 3D Spline element.

---

## Features

- Live weather data via OpenWeatherMap API
- 5-day forecast
- Animated weather particles (rain, snow, mist) on the canvas
- Dynamic backgrounds that change with weather conditions
- Apple-style liquid glass cards with springy hover animations
- Elastic search bar animation on load
- Interactive 3D Spline scene overlay
- Responsive design (Spline hides on smaller screens)
- Real-time clock and date display
- Demo mode when no API key is provided

---

## Project Structure

```
WEATHER MAP/
├── index.html          # Main app file (all HTML, CSS, JS in one file)
├── README.md           # This file
└── asstes/
    └── bg/
        └── bg2.png     # Background wallpaper image
```

---

## Getting Started

### 1. Get a free API key

Go to [https://openweathermap.org/api](https://openweathermap.org/api) and sign up for a free account. Copy your API key from the dashboard.

### 2. Add your API key

Open `index.html` and find this line near the bottom inside the `<script>` tag:

```js
const API_KEY = 'YOUR_API_KEY_HERE';
```

Replace `YOUR_API_KEY_HERE` with your actual key.

### 3. Add your background image

Place your wallpaper image inside the `asstes/bg/` folder and make sure the filename matches this line in the CSS:

```css
background-image: url('asstes/bg/bg2.png');
```

### 4. Open in browser

Simply open `index.html` in your browser. No build tools or server required — it runs entirely in the browser.

> For the best experience, use a local development server like VS Code's **Live Server** extension.

---

## Customization

### Change the accent color
Find `:root` in the CSS and update:
```css
--accent: #64b5f6;
--accent2: #81d4fa;
```

### Change the Spline 3D scene
Find the `<spline-viewer>` tag and replace the URL:
```html
<spline-viewer url="https://prod.spline.design/YOUR_SCENE_ID/scene.splinecode"></spline-viewer>
```

### Change the background image
Replace `asstes/bg/bg2.png` with your own image file and update the path in the CSS.

---

## Tech Stack

| Technology | Usage |
|---|---|
| HTML / CSS / JS | Core app — no frameworks |
| OpenWeatherMap API | Live weather and forecast data |
| Google Fonts (Outfit, DM Serif Display) | Typography |
| Spline Viewer | Interactive 3D scene |
| Canvas API | Rain, snow, and mist particle effects |

---

## API Reference

This app uses two OpenWeatherMap endpoints:

- Current weather: `https://api.openweathermap.org/data/2.5/weather`
- 5-day forecast: `https://api.openweathermap.org/data/2.5/forecast`

Both use `units=metric` so temperatures are in Celsius.

---

## Demo Mode

If the API key is left as `YOUR_API_KEY_HERE`, the app automatically loads demo data for **Thrissur, IN** so you can preview the UI without an API key.

---

## Known Limitations

- The Spline "Built with Spline" watermark cannot be removed on the free plan
- OpenWeatherMap free tier allows 60 calls/minute
- Background image path must use forward slashes `/` not backslashes `\`

---

## Author

**Arjun Raveendran**  
Project: Nimbus Weather App
