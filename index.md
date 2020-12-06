# Using Network Analysis and Natural Language Processing to help you understand the US Congress.

With the 2020 US election being close to finished, we once again find ourselves at the end of a long period of time where US politics has been on everyones lips. But for us Danes, the US political system can seem.. well, quite chaotic? In the light of the recent election, a term you might have heard come across is the United States Congress. Curious to know more about the US Congress - in particular the House of Representatives? Look no further!

On this website, we wish to give you an overview of the voting patterns in the US House of Representatives, and how it has changed over the past 13 years. In the bottom of the page, we will take you through a brief overview of how we found and processed the data, so you have the opportunity to become a US-Congress-Data-Master yourself when you are done reading this website. If you are not interested in the data, and solemnly want to know if there is chaos in congress or not, you can stop before the analysis section and stick to the visual representations of the analyses. Regardless of your technical interest, this website will provide you with answers to questions like: 

- Does polarization exist, and to what degree do the members agree with each other?
- Would a network divide the members into communities corresponding to their political party?
- What subjects separates communities in the House of Representatives? 
- And has this changed over time?


**Intrigued? Keep on reading for insights on our findings!** 

## Navigating the page 
1. [Context and termonology](## Context and termonology)
2. [Findings](## Findings)

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

**roll_info: Roll Call Data**

Insert section from notbook. 

![image](Images/roll_info.png)

**issue_info: The summary for each bill/issue**

Insert section from notbook. 

![image](Images/issue_info.png)

**roll_call_vote: The result of each Roll Call voting round**

Insert section from notbook. 

![image](Images/roll_call_vote.png)



## The Network Analysis 

## Text Analysis 

## Where do I find the data?
The four datasets used for the analyses can be downloaded from our github repository [here](data). 

TODO maybe add source?

## Where do I find the master notebook that rigurously explains this entire analysis? 
A full description of the entire analysis can be retrieved [here](https://nbviewer.jupyter.org/github/benedictehejgaard/chaos-in-congress/blob/gh-pages/WebsiteTest.ipynb). 

