![Banner](img/banner.png)

# COMP4010/5120 Data Visualization - Homework 2 Question Set

This assignment introduces you to a new type of plot called [ridgeline plot](https://www.data-to-viz.com/graph/ridgeline.html), and also require you to apply the skills you have learned so far in the course. We will be using the same fictional VinUni enrolment data from Week 5 AE, plus some Vietnam population data to construct a [population pyramid plot](https://education.nationalgeographic.org/resource/population-pyramid/). 

# Submission requirements

Similar to the weekly AEs and prior homeworks, you should submit your work in 2 formats: `Rmd` and `pdf` to Canvas.
Answers for non-coding questions should be added in the file as plain text.

## Task 1: Creating a ridgeline plot for VinUni enrolment data

### Summary of task requirements

- Recreate the example plot to the best of your ability  (minor differences like font size and figure size are accepted).
- Provide a short comment about what information you are able to intepret from this ridgeline plot.

### Task description

Install the package `ggridges` ([quick beginner's guide](https://cran.r-project.org/web/packages/ggridges/vignettes/introduction.html)). Use `ggridges` to create a ridgeline plot of the distribution of percentage of enrolled students by college in the fictional VinUni dataset [`college_data_normalized.csv`](college_data_normalized.csv).

Recreate the following plot to the best of your ability (minor differences like font size and figure size are accepted), and provide a short comment about what information you are able to intepret from this ridgeline plot:

![Task 1](img/task1.png)

You should do this by creating a function called `theme_college_stats()` to store your theme for the following exercises. In particular, the theme should have the following properties:

- Centered and bold plot title.
- Only y-axis major grid lines are visible.
- Axis title and ticks labels should be bold.
- Font size should be readable and does not need to be identical to the example plot provided above.

Additionally, the font family used in the above plot is [Open Sans from Google Font](https://fonts.google.com/specimen/Open+Sans).
The color palette used for color coding the colleges is: `#78d6ff` for CAS, `#ffee54` for CBM, `#992212` for CECS, and `#117024` for CHS.

Finally, please provide a short comment about what information you are able to intepret from this ridgeline plot.

## Task 2: Creating a bar chart for 2118 VinUni data

### Summary of task requirements

- Filter the VinUni enrolment data to extract only data from the year 2118.
- Recreate the example plot to the best of your ability (minor differences like font size and figure size are accepted).

### Task description

Recreate the following plot to the best of your ability (minor differences like font size and figure size are accepted):

![Task 2](img/task3.png)

## Task 3: Creating a pie chart for 2118 VinUni data

### Summary of task requirements

- Recreate the example plot to the best of your ability (minor differences like font size and figure size are accepted).
- Provide a short comment comparing the effectiveness of the pie chart and the bar chart from Task 2 to represent the same data.

### Task description

Recreate the following plot to the best of your ability (minor differences like font size and figure size are accepted):

![Task 3](img/task2.png)

Hint: If you're unsure how to create this pie chart, check out [`coord_polar()` documentation](https://ggplot2.tidyverse.org/reference/coord_polar.html).

## Task 4: Creating population pyramids for Vietnam data from 1975 to 2025

### Summary of task requirements

- Create a series of 11 individual population pyramid plots for Vietnam from 1975 to 2025.
- Create a theme to style the plots as close as possible to the example plot provided below (you can use other color schemes).
- Provide a comment describing what information does a population pyramid of a year tell you? 
- Provide a comment, based on the 11 plots, describing your idea of what is going on with the population in Vietnam? Optional: Provide your hypothesis/explanation to why that is happening.

### Task description

Create a series of 11 individual [population pyramid]((https://education.nationalgeographic.org/resource/population-pyramid/)) plots for Vietnam from 1975 to 2025, based on the data files [`Viet Nam-####.csv`](./). In particular, the x-axis should represent the percentage of total population while the y-axis should be the age group. Below is an example plot of the data for 2020:

![Task 4](img/task4.png)

Please try to recreate the plot to the best of your ability. You can pick any color schemes you would like for your plot. In the example plot above, the colors `#109466` and `#112e80` are used for female and male respectively.

To avoid copy and pasting a lot of code, you can create a function called `create_population_pyramid(file_name)` to generate a population pyramid with the defined style and theme for a given data file.

Please describe what information does a population pyramid of a year tell you? Based on the 11 plots you've just generated, describe your idea of what is going on with the population in Vietnam? **Optional**: Provide your hypothesis/explanation to why that is happening.

## Task 5: Creating line graph for Vietnamese total population count from 1975 to 2025

### Summary of task requirements

- Create a line graph for Vietnamese total population count from 1975 to 2025.

### Task description

Using all provided data files for Vietnamese population from 1975 to 2025, create a line graph for Vietnamese total population count from 1975 to 2025. As the data for 2025 is predicted data, plot it with a dashed line from 2020 to highlight that it is a prediction.

Recreate the following plot to the best of your ability (minor differences like font size and figure size are accepted):

![Task 5](img/task5.png)

You can pick any color schemes you would like for your plot. In the example plot above, the color `#112e80` is used for the lines and points and `#999999` is used for the dashed line.

## Task 6: Your own Hall of Fame/Shame

Find an interesting data visualization online and provide a critique of it. It can be a great visualization or a terrible one, up to you!

In 3-4 sentences: 

- Provide and introduction to the visualization and an image of it along with proper credit/citation. To insert an image in R Markdown, use: 
```![Caption for the picture.](/path/to/image.png)```
- Describe the purpose of the visualization and the question it is attempting to answer.

In bullet points: identify the strengths and weaknesses of the visualization.

In two to three paragraphs (80-150 words): give a critique/analysis/constructive comments about the visualization. Apply the you knowledge of effective visualization and what you've have learned in the course to your analysis. Can you suggest some improvements that can be made to the visualization?

Side note: inserting an image in R Markdown should look something like this:

![Task 6](img/task6.png)