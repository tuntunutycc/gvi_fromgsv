# Green View Index from Google Street View

Street-level greenery for Chiang Mai University, then a Sentinel-2 model that fills a 10 m grid.

## Review the results

Open the site, not the files on github.com. GitHub shows those HTML files as source code. The interactive pages are here:

- [Overview](https://tuntunutycc.github.io/gvi_fromgsv/)
- [Measured GVI](https://tuntunutycc.github.io/gvi_fromgsv/gvi_map.html)
- [Sample locations](https://tuntunutycc.github.io/gvi_fromgsv/sample_locations.html)
- [Predicted GVI](https://tuntunutycc.github.io/gvi_fromgsv/predicted_gvi_map.html)

The maps use Mapbox Streets. Each map has a layer control: turn a layer off to see the streets underneath. The token in those pages is a public Mapbox token; restrict it to `https://tuntunutycc.github.io/*` in the Mapbox account so it only works on this site.

`gvi_fromgsv.ipynb` keeps the model comparison in its saved outputs. `docs/campus_gvi_prediction.csv` is the campus prediction table.

## Run it

```bash
pip install -r requirements.txt
export GOOGLE_MAPS_API_KEY="your-key"          # Street View download only
export MAPBOX_ACCESS_TOKEN="your-token"        # optional; otherwise maps use CartoDB
```

Open `gvi_fromgsv.ipynb`. Image scoring, including SegFormer, needs the downloaded photos. The modeling sections read the CSV tables in `data/`, which are not in this repository.

## Smartphone photos

The 220 ground-truth phone photos are not stored in this repository. Reviewers can open them here:

[Taken — Google Drive](https://drive.google.com/drive/folders/1j1rRkgSTc4mlZ8Q3b6BDDwZqmTCuD82w?usp=sharing)
