# Sketch 3: Wrap It in a Function

**Points:** 25 (15 for your submission + 10 for completing your peer review)


## Goal

A geoprocessing tool that only runs once and with one hardcoded input isn't reusable. Wrapping it in a function turns a one-off script into a small tool you (or a classmate) can run again on different data.

## Task 1

Write a Python function that:

- Takes **at least two parameters** (for example, an input feature class and a distance, or an input and an output path).
- Wraps **one geoprocessing tool** of your choice (Buffer, Clip, Dissolve, Select — anything you've used so far), using modern arcpy syntax, e.g. `arcpy.analysis.Buffer(...)`, not `Buffer_analysis(...)`.
- Uses a `try`/`except` block so that if the tool fails (bad input, missing file, license issue, etc.), your function prints or logs a clear message instead of crashing with a raw traceback.
- Has a **docstring** explaining what the function does and what its parameters are.

Then **call your function twice**, with two different sets of inputs, to show it generalizes

A minimal skeleton, to show the shape (fill in the details yourself — don't just copy this):

```python
def buffer_layer(in_features, out_features, distance):
    """Buffer in_features by distance and save the result to out_features."""
    try:
        arcpy.analysis.Buffer(in_features, out_features, distance)
        print(f"Buffered {in_features} -> {out_features}")
    except arcpy.ExecuteError:
        print(arcpy.GetMessages(2))

buffer_layer("parcels", "parcels_buf", "50 Meters")
buffer_layer("roads", "roads_buf", "25 Meters")
```

## Task 2

Add a **second** `except` branch that catches bad-distance input (for example, a negative or non-numeric distance) distinctly from the geoprocessing-tool failure your first `except` already handles. The two failure modes must print two different, clearly worded messages. Call your function once more with a deliberately bad distance to show the new branch firing. You can use any file you'd data you'd like, including from the `/data/part1/variety/` directory

## Deliverable

A Jupyter notebook containing your function (with docstring and try/except) and the two calls that exercise it with different inputs.Include the second `except` branch and the extra call that triggers it.

## Submission

Upload your script to the Sketch 3 assignment in Canvas by the due date 

## Peer review

A classmate will read your submission and respond to it using the fixed peer review form found in the `/sketches/` directory. Reviews are attributed, meaning your reviewer's name will be visible to you, and vice versa. Keep your code and comments clear enough for someone else to follow.
