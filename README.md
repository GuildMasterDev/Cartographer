# Cartographer

An interactive mapping application that runs as a desktop app (Electron) **and** a web app. Built on Leaflet and OpenStreetMap. No location permissions required — unless you explicitly ask for them.

🌍 **Live demo:** https://guildmasterdev.github.io/Cartographer

## Features

- 🗺️ Interactive OpenStreetMap integration using Leaflet
- 🔍 Forward geocoding via Nominatim — search any place by name
- 📌 Persistent markers that survive restarts (localStorage)
- 📍 Opt-in geolocation — "My Location" only runs when you ask
- 🎨 Five map styles: OpenStreetMap, Topographic, Dark (CartoDB), Satellite (ESRI), Watercolor (Stadia)
- 🛤️ Dynamic routing: connect your markers in order, with total distance
- 📤 GeoJSON export / import for your marker collections
- ⌨️ Keyboard shortcuts: `/` to search, `M` to toggle marker mode, `Esc` to clear
- 📱 Responsive layout — works in a narrow window too
- 🔒 Privacy-focused — no tracking, no account, no location data unless you click the button

## Running the desktop app

Requires Node.js 18+.

```bash
git clone https://github.com/GuildMasterDev/Cartographer.git
cd Cartographer
npm install
npm start
```

## Running in a browser

The entire app is a single `index.html` file. You can:

- Use the hosted version at https://guildmasterdev.github.io/Cartographer
- Or open `index.html` directly in a modern browser
- Or serve it from any static web host — there is no build step

## Controls

| Action | How |
| --- | --- |
| Search for a place | Type into the search bar, press Enter, click a result |
| Drop a marker | Click anywhere on the map (when marker mode is on) |
| Delete a marker | Click the marker, then click **Delete** in the popup |
| Clear all markers | Click 🗑️ Clear Markers |
| Export markers | Click ⬇️ Export — downloads a `.geojson` file |
| Import markers | Click ⬆️ Import — reads any GeoJSON FeatureCollection |
| Route markers | Click 🛤️ Draw Route (needs 2+ markers) |
| Use my location | Click 📍 My Location (prompts for permission on first use) |

## Technology

- **Electron 41** — desktop shell
- **Leaflet 1.9** — mapping library (via CDN)
- **Nominatim** — geocoding API (OpenStreetMap)
- Zero build tools, zero npm dependencies beyond Electron itself

## License

MIT

## Contributing

Pull requests welcome. The app is intentionally small — a single HTML file with inline CSS and JS. Keep it that way.
