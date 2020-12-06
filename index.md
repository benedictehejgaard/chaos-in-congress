# Using Network Analysis and Natural Language Processing to help you understand the US Congress.

With the 2020 US election being close to finished, we once again find ourselves at the end of a long period of time where US politics has been on everyones lips. But for us Danes, the US political system can seem.. well, quite chaotic? In the light of the recent election, a term you might have heard come across is the United States Congress. Curious to know more about the US Congress - in particular the House of Representatives? Look no further!

On this website, we wish to give you an overview of the voting patterns in the US House of Representatives, and how it has changed over the past 13 years. In the bottom of the page, we will take you through a brief overview of how we found and processed the data, so you have the opportunity to become a US-Congress-Data-Master yourself when you are done reading this website. If you are not interested in the data, and solemnly want to know if there is chaos in congress or not, you can stop before the analysis section and stick to the visual representations of the analyses. Regardless of your technical interest, this website will provide you with answers to questions like: 

- Does polarization exist, and to what degree do the members agree with each other?
- Would a network divide the members into communities corresponding to their political party?
- What subjects separates communities in the House of Representatives? 
- And has this changed over time?


**Intrigued? Keep on reading for insights on our findings!** 

## Navigating the page 
1. [Context and termonology](#Context and termonology)
2. [Findings](https://github.com/benedictehejgaard/chaos-in-congress/blob/gh-pages/index.md#findings)
3. [Data Used](#The Data Used) 
4. [Network Analysis](#Network Analysis) (advanced)
5. [Text Analysis](#Text Analysis) (advanced)
6. [Download the Dataset](#Where do I find the data?) 
7. [Download the Entire Workbook](#Where do I find the master notebook that rigurously explains this entire analysis?)


## Context and termonology
Before we get started with the results, we realize not everyone is an expert in the US Congress. If you are, you can skip this section. 

--insert section from notebook--

Below, you will find a simple overview of the above described termology: 

| Termonology    | Description                                                    |
|----------------|----------------------------------------------------------------|
| Representative | A voting member of the House of Representatives                |
| Term           | The two year period that the representatives are elected for   |
| Bill/Issue     | The law proposal/amendment that the house votes for            |
| Bill_ID        | Unique ID for each Bill/Issue                                  |
| Roll Call      | A round of voting for a bill. There can be multiple per bill.  |
| Roll_Call_ID   | Unique ID for a roll call.   


## Findings
We have nothing 


## The Data Used 

If you wish to dive deeper into the analyses behind these findings, you will first need some data. In order to carry out these investigations, you will need four datasets: 
* Congress_110_116: Congress Member Data
* roll_info: Roll Call Data
* issue_info: The summary for each bill/issue
* roll_call_vote: The result of each Roll Call voting round 

Each of these datasets contain data from the [US Congress Website](www.congress.gov). If you are curious to know exactly how we got the data, you can find a more throrough walk-through in the !!!TODO NOTEBOOK!. 

**Congress_110_116: Congress Member Data**

Insert section from notbook. 

![image](Images/Congress_110_116.png)

After cleaning, this dataset has 969 rows, corresponding to 969 members. 

**roll_info: Roll Call Data**

Insert section from notbook. 

![image](Images/roll_info.png)

We clean the data by removing all entries where either the bill ID or the result of the vote is missing. Furthermore, most bills that are presented in congress will have several votes, and only the latest vote is included in the analysis, such that each bill is represented by a single vote. Furthermore, if these were not removed, identical sumamries may appear in the text analysis which would skew the results. By only focusing on the last vote, we are sure to focus only on the longest and most accurate summary of each bill.

After data cleaning, the final dataset has 3082 Roll Calls and Bills (rows).

**issue_info: The summary for each bill/issue**

Insert section from notebook. 

![image](Images/issue_info.png)

We clean the data by removing all empty summaries. After data cleaning, the final dataset has 3639 Roll Calls (rows). 

**roll_call_vote: The result of each Roll Call voting round**

Insert section from notebook. 

![image](Images/roll_call_vote.png)

We remove all the Roll Calls that were not the latest roll call for a bill, so the list of roll calls correspond to the list of roll calls we obtained from the [roll_info](#roll_info: Roll Call Data) data cleaning. Furthermore, we notice there are multiple methods of answering; yes, yea, no, nay, thus the roll call votes are changed to binary. Notice all *not voting* and *NaN* values will be left out of this analysis:

* 1 for 'Yes', 'Yea', and 'Aye'
* 0 for 'No', and 'Nay'

After data cleaning, this dataset has the shape: Members (rows), Roll Calls (cols) = (916, 3082).

## Description of the Dataset


## The Network Analysis 

## Text Analysis 

## Where do I find the data?
The four datasets used for the analyses can be downloaded from our github repository [here](data). 

TODO maybe add source?

## Where do I find the master notebook that rigurously explains this entire analysis? 
A full description of the entire analysis can be retrieved [here](https://nbviewer.jupyter.org/github/benedictehejgaard/chaos-in-congress/blob/gh-pages/WebsiteTest.ipynb). 

