# Travel Tide: Find your own way!

## Objective
This is the Mastery Project of Masterschool cohort in February 2026.
With a given dataset of the Travel Tide travel agency of > 5 Million sessions,
the scope was to clean and transform the dataset for analysis. 
The goal was to come from a session based table with millions of rows, 
to a representative user based table and build groups of users by segmentation. 
To avoid churn and strengthen retention we wanted to assign relevant perks for each group.

## Dataset
We had four tables of data: Sessions (fact), Hotels, Flights, Users. 
The session based table had 5 Million rows, including many, that never converted into an actual trip, cancellations etc. 
We decided that in order to find perks for cohorts, we needed to look at the data from a user perspective. 
Also, in order to give recommendations and make our systems run fast and smoothly, we came up with a much smaller set of data of 5998 representative users.  

## Tools
Our main tool for cleaning, transforming and analysing the data was SQL. 
For further insights and visualisations we connected the transformed data to Tableau.
The final presentation was created with the help of gamma/slides (AI-powered).

## Challenges
There was an issue that we had to tackle because some nights (spent at the hotels) had a negative value.
Since this did not make logical sense, we decided to change these values into positive 1. 
We did this to take into account that there was an actual trip. 
At the same time we wanted to be conservative and not exaggerate the revenue for these trips. 
Another challenge to tackle was cancellations. 
We decided to exclude them first from our sessions and moved on to build the user based table from only valid trips. 
At the same time we wanted to keep the cohort of users that is interested in a trip but never booked one (Dreamers). 

## Insights
We came up with 7 (+ group "Others") groups and each group has an assigned perk. 
