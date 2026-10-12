# Sketch 4: Hello, Colab


## Goal

Prove that you can work in the Part 2 environment end to end: a Colab notebook, the standard setup cell, a small pandas step, and a commit to your new GitHub repository. Most of this mirrors what we did together in class this week. The point is that it works on your account, on your own, before anything graded depends on it.

## Task

1. Create a new Colab notebook named `sketch04_yourlastname`.
2. Run the standard setup cell from this week's sessions (the `%pip install` cell). It should finish without errors.
3. Load `ohio_precip_2025.csv` with pandas from the course data URL given on the Sketch 4 assignment page in Canvas. Show `.head()` and `.describe()`.
4. Use `.sort_values()` to find the five wettest stations. Print their `name` and `precip_mm_2025` columns.
5. Add a markdown cell with one or two sentences: how far above the mean is the wettest station, and does that surprise you?
6. Commit the executed notebook to the GitHub repository you created in class this week, through the GitHub web upload, with a commit message that says what the notebook does.

## Deliverable

- A link to your GitHub repository, with the executed notebook visible in it.
- A share link to your Colab notebook ("Anyone with the link can view") or the uploaded `.ipynb` file.

## Submission

Submit both to the Sketch 4 assignment in Canvas by the due date.

## Peer review

Same as every sketch: Canvas assigns you one classmate's sketch after the deadline. Use the peer review form.
