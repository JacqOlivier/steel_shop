# TASK: STEEL SHOP

Experts at the steel factory proposed a new approach to predict the temperature of the basic steel converter 
(final stage of steel making). It consists of an algorithm that uses machine learning. 
The task for the technical team is to design a solution that will allow operators at the facility to use a predictive model.

Your solution should be easily reviewed / presented in 30 minutes.

## Problem

Basic oxygen furnace directly reduces iron to steel by direct reduction (blowing oxygen) into the iron mix and hence reducing carbon content. This process requires to stop the process at the precise temperature T=1680°C or as close as possible to the temperature, for the steel grade produced at the facility. Due to the nature of the process, temperature can be measured only after the oxygen blow is finished.

Stopping the process too early (i.e., T < 1680°C) means that steel is not ready yet and therefore it requires restart of the oxygen blow. Experts have calculated the total cost 100EUR to restart process.

Stopping the process too late (i.e., T > 1680°C) increase equipment wears and requires higher cost at secondary metallurgy . Experts have calculated a total cost 10EUR each additional 10 degrees above 1680 per blow.

## Data

Data at the plant is measured every 5 seconds from off-gases created by the process. We estimate that the data are measured in 5 second delay.

The output.csv file contains data for multiple process iterations (blows).

* heatid - iteration id
* datetime - measurement timestamp
* gas1 - gas measurement
* end_t - temperature measurement. This is done once for each iteration, only after the blow is stopped.

## Task 1 [Evaluate data]/ Technical

* Analyze the provided dataset.
* describe concisely, with stats and plots, the core characteristics of the dataset.
* What are extreme values for the gas?

## Task 2 [Manipulate data]/ Technical

Experts have concluded that there is a delay of 5 seconds in measurement of the gas.

* Propose a function to time shift the data.
* [Discussion] Live deployment - see task 5 below: how to store timestamps for different measurements in the database? Why?

## Task 3: [Modeling]/ Technical + Discussion

* Build a model to estimate the temperature given the gas measurements.
* Provide an analysis of the model quality.
* Describe few model improvements that could benefit the final product.
* How would you use the model in a real-time production scenario?

## Task 4 [Ensuring value]/ Technical + Discussion

* How can you use your model to minimize the restart/overheat losses?
* Justify your proposal with the data.
* (optional) Prepare a simulated experiment using the data and your model.

## Task 5 [Deployment] / Discussion

* How would you deploy your model as a recommender system accessible to the operators, informing them of the stop time for each batch?

## Tips

* Ask questions if you do not understand the assignment.
    * Send emails with questions as a reply-all to email with tasks.
    * Don't leave questions until the last minute.
    * Ask for a quick call if you feel that email is not enough.
* Do not overcomplicate your solution, it is a simple problem.
* There is no single correct solution, make reasonable assumptions and your solution will be valid.
* Prepare your solution in a concise and readable format, examples:
    * documented Jupter notebook
    * script that outputs an html file with solutions/discussion
    * organized Github repo with README.md / word file / ppt for discussion
* Focus on:
    * Explain your thought process, reasons for your choices.
    * Clean and readable code (define functions, add docstring ...)
    * Output clear and documented graphs that support your analysis.
    * Be concise (it should be easy to review your solution in ~30min)
* We are not looking for buzzword models, but clean code, good understanding, and communication skills.
olution should be easily reviewed / presented in 30 minutes.