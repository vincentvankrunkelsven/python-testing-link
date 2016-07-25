---
title       : Insert the chapter title here
description : Insert the chapter description here

--- type:MultipleChoiceExercise lang:python xp:50 skills:1 key:b5c6f05fb5
## A really bad movie

Have a look at the plot that showed up in the viewer to the right. Which type of movies have the worst rating assigned to them?

*** =instructions
- Long movies, clearly
- Short movies, clearly
- Long movies, but the correlation seems weak
- Short movies, but the correlation seems weak

*** =hint
Have a look at the plot. Do you see a trend in the dots?

*** =pre_exercise_code
```{python}
# The pre exercise code runs code to initialize the user's workspace. You can use it for several things:

# 1. Pre-load packages, so that users don't have to do this manually.
import pandas as pd
import matplotlib.pyplot as plt

# 2. Preload a dataset. The code below will read the csv that is stored at the URL's location.
# The movies variable will be available in the user's console.
movies = pd.read_csv("http://s3.amazonaws.com/assets.datacamp.com/course/introduction_to_r/movies.csv")

# 3. Create a plot in the viewer, that students can check out while reading the exercise
plt.scatter(movies.runtime, movies.rating)
plt.show()
```

*** =sct
```{python}
# The sct section defines the Submission Correctness Tests (SCTs) used to
# evaluate the student's response. All functions used here are defined in the
# pythonwhat Python package

msg_bad = "That is not correct!"
msg_success = "Exactly! The correlation is very weak though."

# Use test_mc() to grade multiple choice exercises.
# Pass the correct option (option 4 in the instructions) to correct.
# Pass the feedback messages, both positive and negative, to feedback_msgs in the appropriate order.
test_mc(4, [msg_bad, msg_bad, msg_bad, msg_success])
```