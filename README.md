# Mini-Project 1

# Overview

In this mini-project, you will create at least two data visualizations of variables in the [College Scorecard](https://collegescorecard.ed.gov/) dataset and then write up your findings in a short blog post (400-500 words). You will study the data documentation, review the data dictionary to select variables for your analysis, and then finally produce your plots. In your blog post, you will detail how the data in this dataset was produced, along with what we learn by reviewing the plots. 

# Learning Goals

* Navigate different forms of data documentation
* Recognize differences in variable types and how they get assigned to `R` data objects 
* Examine variation in and co-variation between data variables through exploratory plotting in `R`
* Communicate data findings in writing and effective data graphics
* Evaluate the ethical dimensions of data resources

# Detailed Instructions

## Set up your environment

1. In RStudio, `File` > `New Project` > `Version Control` > `Git` and then copy the URL to this repo. Open `scorecard_analysis.qmd` and add your group member's names to the header (lines 5, 7, and 9). 
2. You should have already installed the `rscorecard` package in lab 1. If for some reason it is not installed. Install the `rscorecard` package by entering the following in your console: 

`install.packages("rscorecard")`

3. If you still have access to your API key from lab 1, copy this API key into line 31 of `scorecard_analysis.qmd`. Run that code chunk. If you don't have that key, navigate [here](https://api.data.gov/signup/) to sign up for an API key through Data.gov. After you enter your name and email, the API key will be emailed to you. 

## Get to know the scorecard data

4. Download **both** the Scorecard Data Dictionary and the Institution-Level Technical Documentation [here](https://collegescorecard.ed.gov/data/documentation/). Read pages 2-3 of the Technical Documentation to learn more about this dataset. You should already be somewhat familiar with the format of the data dictionary from lab 1. Refer back to that lab for help navigating it.  

5. In addition to `unitid` and `instnm`, select five more variables from the data dictionary that you'd like to work with in your analysis. There is a lot of missing data in this dataset so I encourage you to select variables from those that we used in lab 1; all of the variables we examined in lab 1 are suitable for this assignment. We're only going to be looking at MA schools, so you can leave variables that record the state and region of the institution off of your list. *Select at least one numeric variable, and at least one ordinal variable.* Read up on these selected variables in the Technical Documentation (Command/Control + F to find the variable name in the PDF.)

## Import and prepare data

6. On line 38 of `scorecard_analysis.qmd`, add the list of variable names (from column 6 in the data dictionary) as additional arguments to the `sc_select()` function. *Note that you should supply these names in lowercase.* Run the code chunk. 
7. Check out the data frame, and note columns with many missing values. **If you've selected variables other than the variables that we used in lab 1 and the values are missing in more than 25% of rows, return to the data dictionary and select new columns.** Re-run the code. 
8. Recode your ordinal variable in the code chunk starting at line 43. Be sure to reference lab 1 for help with this!

## Design two data visualizations

9. As a group, devise a question about the state of MA colleges in 2018 that you would like to answer with your data. Your question should be concise and should be a question that can be answered with the data available to you. Avoid questions that require predictive analysis or analysis of variables that not represented in this dataset. 

10. Create two data visualizations showcasing that help address your question. At least one plot should visualize distributions and/or frequencies. You may select how you would like to design the second plot. However, both plots should be clearly related to the question you've asked. Be sure to label your plots with all five required components of context. Add a caption to both plots explaining how you've mapped values onto different plot aesthetics. 

## Write blog post

10. In 400-500 words, you should write a blog post reporting on your visualization:
  * Paragraph 1: Introduce the dataset, how the data was produced, and what you specifically will be visualizing in your plots. 
  * Paragraph 2: Report on findings from your visualizations.
    * For each plot, you should summarize at least one quantitative fact that we can extrapolate, **and** interpret that finding. (e.g. on this plot, we can see that ... This indicates that ...)
  * Paragraph 3: Summarize the key takeaway from your analysis and describe at least one ethical concern we should consider when analyzing this data. You may consider:
    * What assumptions and commitments informed the design of this dataset?
    * Who has had a say in data collection and analysis regarding this dataset? Who has been excluded?
    * What are the benefits and harms of this dataset, and how are they distributed amongst diverse social groups?
    
## Record standards and submit assignment

11. Open `standards.qmd`, and under each heading, indicate how the work you completed for this project demonstrated fluency in that standard. You may wish to reference the Evaluation section below for help with writing this up. 
12. Open `contributions.qmd` and briefly describe each team member's contributions to the project. 
13. When you are done, you should save all .qmd files, render the documents, commit changes, and then push changes back to GitHub. That's it for submission. You don't need to submit anything on Moodle. 

# Evaluation 

You will be evaluated on the extent to which your mini-project demonstrates fluency in the following course learning dimensions:

* Understanding Datasets:
  * 1 point - Demonstrates an ability to interpret data dictionaries
  * 1 point - Demonstrates an ability to recognize different types of variables
  * 1 point - Demonstrates an ability to detail the provenance of a dataset (how the data was produced) in writing
* Visualization Aesthetics
  * 1 point - Demonstrates an ability to map variables onto appropriate plot aesthetics
  * 1 point - Demonstrates an ability to adjust the scales of plot aesthetics
  * 1 point - Demonstrates an ability to address overplotting
* Plotting Frequencies and Distributions
  * 1 point - Demonstrates an ability to represent statistical information on a plot
  * 1 point - Demonstrates an ability to accurately label plots with all five required pieces of context
  * 1 point - Demonstrates an ability to accurately summarize and interpret plot findings in writing
  

