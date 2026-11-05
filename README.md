# LandMeasure

A responsive, browser-based land area and perimeter calculator.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in a modern browser, or serve the folder with a local static web server.
3. Allow location permission if you want to use **My location**.

The app uses external CDN and map services, so an internet connection is required.

## Publish with GitHub Pages
1. Create a GitHub repository (for example, `landmeasure`).
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then Save.
6. GitHub Pages will provide the public website URL.

## Map and calculation services
- Leaflet 1.9.4 for interactive mapping.
- Esri World Imagery for the default satellite basemap.
- OpenStreetMap tiles for the optional street basemap.
- OpenStreetMap Nominatim for place search.
- Turf.js 6.5.0 for geodesic polygon area and perimeter calculations.

## Important service notes
This is a no-backend prototype. Public map and geocoding services have usage policies, rate limits, and availability constraints. For a public or high-traffic production deployment, review each provider's current terms and consider a dedicated/contracted tile and geocoding provider. Do not bulk-download or prefetch map tiles.

## Measurement limitations
- Area and perimeter are calculated geodesically from the selected WGS84 coordinates.
- The app assumes points are entered around the boundary in order and that the polygon does not cross itself.
- Map imagery and GPS positions can be offset or inaccurate.
- This is an estimate, not a cadastral survey or legal boundary determination.
- The browser geolocation feature requires HTTPS (or localhost) and user permission.
