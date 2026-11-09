# Sketch 5: Two Maps, One Truth

## Goal

The same data can tell two different visual stories depending on how you classify it. The goal here is to demonstrate that problem

## Task 1

In a Colab notebook (remember the standard setup cell from Sketch 4, if you're starting a fresh notebook):

1. Load `cuyahoga_tracts_acs.gpkg` from the course data URL on the Sketch 5 assignment page, or another polygon layer with a numeric column that you've already worked with this semester. Pick **one** column to map. If you're using the Cuyahoga tracts, pick any ACS column EXCEPT `total_population`, and print how many tracts are missing it (`.isna().sum()`).
2. Make a choropleth map of that column using one classification scheme (e.g., quantiles). Build it the way 12_01's notebook built its map, piece by piece, so the finished map has: `scheme=` and `k=`, a legend with a real title and units (`legend_kwds`), `missing_kwds` so that tracts with no value are visible and labeled instead of disappearing, and a title that names the scheme and `k`. (If you're using the Cuyahoga tracts, frame the map to the land tracts as in step 5 of the notebook, or the Lake Erie tract will swallow the figure.)
3. Make a **second** choropleth map of the *same* column and the *same* colormap (`cmap`), but with a **different classification scheme** (e.g., equal interval, or natural breaks/Fisher-Jenks). `geopandas.GeoDataFrame.plot(..., scheme=...)` uses `mapclassify` under the hood for this — it's already installed by the setup cell.
4. Print the bin counts for both schemes, the way the small-multiples cells in Tuesday's notebook did: call the `mapclassify` class directly on the column with `.dropna()` and print `.counts`. These numbers are the evidence for your five sentences below.
5. Save each map as a PNG with `fig.savefig("...", dpi=200, bbox_inches="tight")`, as in step 7 of the notebook, and download the files from Colab's Files panel.

## Task 2

Make a **third** choropleth map of the same column and colormap, using a classification scheme different from both of your first two (e.g., if you used quantiles and equal interval above, try natural breaks/Fisher-Jenks here). Print its bin counts too. One sentence: when would you actually use this third scheme over the other two?

## Deliverable

- Maps, plotted and visible in your notebook, each with legend, missing-data handling, and a title that names the scheme.
- The printed bin counts for both schemes.
- 5 sentences: which of your two maps could mislead a reader, and why? Be specific - use the bin counts, point to where the classification scheme changes which areas look "high" or "low," and say what a reader might wrongly conclude as a result.

## Submission

Submit your Colab notebook link (set sharing to "Anyone with the link can view") or link to the executed `.ipynb` file on GitHub

## Peer review

A classmate will read your submission and respond to it using the fixed peer review form (see the peer review form on Canvas). Reviews are attributed (your reviewer's name will be visible to you, and vice versa) so keep your code and comments clear enough for someone else to follow.
