# ☀️ Space Weather Dashboard

A simple, responsive web dashboard that shows current solar and space-weather conditions using live data from NOAA.

**Live demo:** https://ajmalmuhammed20011-arch.github.io/weather/

## Features

- **Geomagnetic activity:** current Kp index with a storm level (quiet, active, G1 to G5) and a bar chart of recent readings
- **Solar wind:** current speed and a 24-hour line chart
- **Solar flares:** current class (A, B, C, M, X) calculated from GOES X-ray flux
- **Sunspot number:** latest monthly mean
- **Magnetic field (Bz):** 24-hour chart, since southward Bz drives geomagnetic storms
- **Recent alerts:** latest official NOAA space-weather alerts
- **Impact section:** how space weather affects satellites, communication, navigation, astronauts and power grids
- Responsive layout with automatic light and dark themes

## Data sources

All data comes from the free, public [NOAA Space Weather Prediction Center](https://www.swpc.noaa.gov/) JSON services (no API key needed):

| Parameter | Endpoint |
|---|---|
| Kp index | `/products/noaa-planetary-k-index.json` |
| Solar wind speed | `/products/solar-wind/plasma-1-day.json` |
| Magnetic field (Bz) | `/products/solar-wind/mag-1-day.json` |
| Solar flares (X-ray flux) | `/json/goes/primary/xrays-6-hour.json` |
| Sunspot number | `/json/solar-cycle/observed-solar-cycle-indices.json` |
| Alerts | `/products/alerts.json` |

Base URL: `https://services.swpc.noaa.gov`

If the live feed cannot be reached, the dashboard falls back to clearly labelled sample data, and the badge at the top shows which mode is active.

## Tech

Plain HTML, CSS and JavaScript in a single file (`index.html`). Charts are drawn as inline SVG, so there are no libraries or build steps.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a browser.

## Deploy on GitHub Pages

1. Go to **Settings → Pages**.
2. Set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, then save.
3. Your site will be live at `https://<username>.github.io/<repo-name>/`.

## Example impact of space weather

A strong solar flare or coronal mass ejection can disturb Earth's ionosphere. This degrades GPS accuracy and can black out high-frequency radio, which affects aviation, shipping and emergency services.

## Credits

Data courtesy of NOAA Space Weather Prediction Center.
