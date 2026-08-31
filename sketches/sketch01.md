# Sketch 1: One Tool, Three Ways

**Points:** 25 (15 for your submission + 10 for completing your peer review)

## Goal

ArcGIS Pro gives you three ways to run the same geoprocessing tool: the GUI dialog, ModelBuilder, and arcpy. This sketch is about exploring all three side by side, so you develop a feel for when each one is the right call.

## Task 1

Using the `kent_campus_buildings.shp` layer in data directory, run the **Buffer** tool three different ways:

1. **The Pro GUI** — open the Buffer tool dialog, fill in the parameters, and run it.
2. **ModelBuilder** — build a one-tool model that runs Buffer, and run the model.
3. **arcpy** — open the Python window in Pro and run Buffer as a single line of code, for example:

```python
arcpy.analysis.Buffer("buildings", "buildings_buffer", "100 Meters")
```

(Use your own layer name and buffer distance — this is just to show the syntax pattern. Note the modern dotted form, `arcpy.analysis.Buffer`, not the older `Buffer_analysis`.)

## Task 2

Run `arcpy.analysis.Buffer` a second time on the same layer, at a different distance than the one you used in step 3. In one sentence, say which of the two buffer outputs you'd actually trust for a planning decision, and why.

## Deliverable

A single text or Python file containing:

- The one line of arcpy code you used to run Buffer (step 3).
- 3–5 sentences reflecting on when each of the three modes — GUI, ModelBuilder, arcpy — is the right choice. Think about things like: one-off vs. repeated tasks, needing to hand a workflow to someone else, debugging, and speed of setup.
- Your second `arcpy.analysis.Buffer` line of code and the one-sentence explanation of which output you'd trust.

You do **not** need to submit screenshots of the GUI or ModelBuilder runs - just the arcpy line and your reflection.

## Submission

Upload your file to the Sketch 1 assignment in Canvas by the due date.

## Peer review

A classmate will read your submission and respond to it using the fixed peer review form found in the `/sketches/` directory. Reviews are attributed, meaning your reviewer's name will be visible to you, and vice versa. Keep your code and comments clear enough for someone else to follow.


