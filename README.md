# Johnstown, PA Weather & Air Quality

A small, self-contained weather and air quality display for Johnstown, Pennsylvania.

The page is a single static `index.html` file. It fetches live data in the browser from the [Open-Meteo Forecast API](https://open-meteo.com/en/docs) and the [Open-Meteo Air Quality API](https://open-meteo.com/en/docs/air-quality-api). No API key is required.

## What it shows

- Current temperature (°F), conditions, feels-like, wind (mph), humidity, and cloud cover
- Next 24 hours and a 7-day forecast
- US AQI plus PM2.5, PM10, ozone, NO₂, SO₂, CO, and UV index
- Last updated time in `America/New_York`
- Automatic refresh every 15 minutes

Coordinates used: 40.3267, -78.9220.

If the primary forecast host is rate-limited, the page falls back to Open-Meteo's historical-forecast API, which uses the same request shape.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8080
```

## Deploy

This is a free Render static site. `render.yaml` publishes the repo root with no build step. Weather requests are made by the visitor's browser, not the host.

## Credit

Weather and air quality data by [Open-Meteo](https://open-meteo.com/) (CC BY 4.0).
