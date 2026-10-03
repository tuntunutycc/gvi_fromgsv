# Green View Index from Google Street View

Street-level greenery for Chiang Mai University, then a Sentinel-2 model that fills a 10 m grid.

## Review the results

The pages in [`docs/`](docs/index.html) are the maps and figures, drawn on CartoDB so they contain no API key. On GitHub Pages they open in the browser:

- [Measured GVI](docs/gvi_map.html)
- [Sample locations](docs/sample_locations.html)
- [Predicted GVI](docs/predicted_gvi_map.html)

`gvi_fromgsv.ipynb` keeps the model comparison in its saved outputs. `docs/campus_gvi_prediction.csv` is the campus prediction table.

## Run it

```bash
pip install -r requirements.txt
export GOOGLE_MAPS_API_KEY="your-key"          # Street View download only
export MAPBOX_ACCESS_TOKEN="your-token"        # optional; otherwise maps use CartoDB
```

Open `gvi_fromgsv.ipynb`. Image scoring, including SegFormer, needs the downloaded photos. The modeling sections read the CSV tables in `data/`, which are not in this repository.
