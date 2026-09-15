# Sketch 2: Format Detective

**Points:** 25 (15 for your submission + 10 for completing your peer review)

## Goal

Not all spatial data formats behave the same way. This sketch has you convert one dataset into two other formats and compare what changes — file size, field names, and one more difference you notice yourself.

## Task

Starting from any shapefile provided in the course's GitHub repository:

1. Convert it to a **GeoPackage** feature class
2. Convert it to **GeoParquet** (note, you need at least ArcGIS Pro 3.6)

You can do the GeoPackage conversion with the Export Features tool (GUI or `arcpy.conversion.ExportFeatures`); for the GeoParquet leg, use Export To Parquet (`arcpy.conversion.ExportToParquet`). Use `arcpy.ListFields` to check field names in each output, and check file sizes with the file properties in Windows Explorer (or use `os.path.getsize` if you're scripting it).

Then build a short comparison table with (at least) these four rows:

| Feature | Shapefile | GeoPackage | GeoParquet |
|---|---|---|---|
| File size | | | |
| Longest field name allowed | | | |
| *(your choice)* | | | |
| *(your choice)* | | | |

Pick your own fourth comparison point. Some ideas: does the format store one layer per file or many, does it need a sidecar/projection file, does it handle field names with spaces or special characters differently.


Then, instead of reading file sizes off Windows Explorer, get all three sizes programmatically with `os.path.getsize(path)` and print them. Note: for the shapefile and GeoPackage, `os.path.getsize` on the main file (`.shp` or `.gpkg`) won't capture sidecar files. So mention in a comment whether you summed the sidecars too and why that matters for a fair size comparison. 

## Deliverable

- A short notebook or script showing the two conversions and how you pulled the numbers for your table
- The 4-row comparison table (values filled in)
- 3 sentences on which of the three formats you'd choose for a project you're about to start, and why
- If you did the stretch task: the `os.path.getsize` code and printed sizes, with your sidecar-file comment

## Submission

Upload your notebook/script and table to the Sketch 2 assignment in Canvas by the due date above.

## Peer review

A classmate will read your submission and respond to it using the fixed peer review form found in the `/sketches/` directory. Reviews are attributed, meaning your reviewer's name will be visible to you, and vice versa. Keep your code and comments clear enough for someone else to follow.
