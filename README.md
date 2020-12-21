# GeorgiaTech Bootcamp Final Project


## Project Results:

[Tableau Dashboard](https://public.tableau.com/shared/TBYNJP4QM?:display_count=y&:origin=viz_share_link) <br />

[Website](https://sai-praneeth-reddy.github.io/GT_US_Senate/) <br />

[DecisionTree Model - Democrats](https://github.com/sai-praneeth-reddy/GT_Final_Project/blob/master/Python/02DecisionTrees_Democrat.ipynb) <br />

[DecisionTree Model - Rebublicans](https://github.com/sai-praneeth-reddy/GT_Final_Project/blob/master/Python/03DecisionTree_Republican.ipynb) <br />


## Team Members: 
[Ana Cifuentes](https://www.linkedin.com/in/anacifuentesco/?locale=en_US) <br />
[Cornelia Harris](http://www.linkedin.com/in/corneliaharris) <br />
[Rachael Munyua](http://www.linkedin.com/in/rachael-munyua) <br />
[Sai Reddy](https://www.linkedin.com/in/saipraneeth1/) <br />
[Tariq Attarwala](https://www.linkedin.com/in/tariq-attarwala-923185a8/) <br />
[Vinh Phan](www.linkedin.com/in/vinhxphan/) <br />


## Summary : 
The goal of this project is to create a dashboard for evaluating the performance of the U.S. Senators and develop a classification model to forecast the winner of Democratic and Republican Primary election for the U.S. Senate, U.S. House and Governor. We will then look for patterns among successful candidates. 

In addition to that, we will compare voter registration in 2016 vs 2020 and its impact from the pandemic.


## Scope: 
The final results for the project will be presented in a Tableau dashbord. The dashboard will display the performance of our model in identifying winners of primary elections and also demonstrate any patterns that exist. The machine learning models we will be exploring as part of our project are:

1. Decision Trees
2. Random Forest


A dashboard to evaluate the performance of the U.S. Senators and an analysis that compares voter registration in 2016 vs 2020 will also be included.


## Technologies:
Pandas for manipulating data into required format. <br />
Sklearn for developing Machine Learning models. <br />
posttgres SQL DB for data storage. <br />
Tableau for data visualization <br />


## Data Sets:
Primary Election Results : [Fivethirtyeight](https://github.com/fivethirtyeight/data/tree/master/primary-candidates-2018) <br />
Voter Registration: [Fivethirtyeight](https://github.com/fivethirtyeight/data/tree/master/voter-registration) <br />
Senators info : [Govtrack](https://www.govtrack.us/api/v2/role?current=true&role_type=senator) <br />
Popularity: [Morning Consultant](https://morningconsult.com/2019/01/10/americas-most-and-least-popular-senators-q4-2018-2/) <br />
Ideology Score: [Govttack](https://www.govtrack.us/congress/members/report-cards/2019/senate/ideology) <br />



## Data Dictionary:

`dem_candidates.csv` contains information about the 811 candidates who have appeared on the ballot this year in Democratic primaries for Senate, House and governor, not counting races featuring a Democratic incumbent, as of August 7, 2018. 

`rep_candidates.csv` contains information about the 774 candidates who have appeared on the ballot this year in Republican primaries for Senate, House and governor, not counting races featuring a Republican incumbent, through September 13, 2018. 

Here is a description and source for each column in the accompanying datasets.

`dem_candidates.csv` and `rep_candidates.csv` include: 

Column | Description 
-------|--------------
`Candidate` | All candidates who received votes in 2018’s Democratic primary elections for U.S. Senate, U.S. House and governor in which no incumbent ran. Supplied by Ballotpedia.
`State` | The state in which the candidate ran. Supplied by Ballotpedia.
`District` | The office and, if applicable, congressional district number for which the candidate ran. Supplied by Ballotpedia.
`Office Type` | The office for which the candidate ran. Supplied by Ballotpedia.
`Race Type` | Whether it was a “regular” or “special” election. Supplied by Ballotpedia.
`Race Primary Election Date` | The date on which the primary was held. Supplied by Ballotpedia.
`Primary Status` | Whether the candidate lost (“Lost”) the primary or won/advanced to a runoff (“Advanced”). Supplied by Ballotpedia.
`Primary Runoff Status` | “None” if there was no runoff; “On the Ballot” if the candidate advanced to a runoff but it hasn’t been held yet; “Advanced” if the candidate won the runoff; “Lost” if the candidate lost the runoff. Supplied by Ballotpedia.
`General Status` | “On the Ballot” if the candidate won the primary or runoff and has advanced to November; otherwise, “None.” Supplied by Ballotpedia.
`Primary %` | The percentage of the vote received by the candidate in his or her primary. In states that hold runoff elections, we looked only at the first round (the regular primary). In states that hold all-party primaries (e.g., California), a candidate’s primary percentage is the percentage of the total Democratic vote they received. Unopposed candidates and candidates nominated by convention (not primary) are given a primary percentage of 100 but were excluded from our analysis involving vote share. Numbers come from official results posted by the secretary of state or local elections authority; if those were unavailable, we used unofficial election results from the New York Times.
`Won Primary` | “Yes” if the candidate won his or her primary and has advanced to November; “No” if he or she lost.

`dem_candidates.csv` includes: 

Column | Description 
-------|--------------
`Gender` | “Male” or “Female.” Supplied by Ballotpedia.
`Partisan Lean` | The FiveThirtyEight partisan lean of the district or state in which the election was held. Partisan leans are calculated by finding the average difference between how a state or district voted in the past two presidential elections and how the country voted overall, with 2016 results weighted 75 percent and 2012 results weighted 25 percent.
`Race` | “White” if we identified the candidate as non-Hispanic white; “Nonwhite” if we identified the candidate as Hispanic and/or any nonwhite race; blank if we could not identify the candidate’s race or ethnicity. To determine race and ethnicity, we checked each candidate’s website to see if he or she identified as a certain race. If not, we spent no more than two minutes searching online news reports for references to the candidate’s race.
`Veteran?` | If the candidate’s website says that he or she served in the armed forces, we put “Yes.” If the website is silent on the subject (or explicitly says he or she didn’t serve), we put “No.” If the field was left blank, no website was available.
`LGBTQ?` | If the candidate’s website says that he or she is LGBTQ (including indirect references like to a same-sex partner), we put “Yes.” If the website is silent on the subject (or explicitly says he or she is straight), we put “No.” If the field was left blank, no website was available.
`Elected Official?` | We used Ballotpedia, VoteSmart and news reports to research whether the candidate had ever held elected office before, at any level. We put “Yes” if the candidate has held elected office before and “No” if not. 
`Self-Funder?` | We used Federal Election Committee fundraising data (for federal candidates) and state campaign-finance data (for gubernatorial candidates) to look up how much each candidate had invested in his or her own campaign, through either donations or loans. We put “Yes” if the candidate donated or loaned a cumulative $400,000 or more to his or her own campaign before the primary and “No” for all other candidates.
`STEM?` | If the candidate identifies on his or her website that he or she has a background in the fields of science, technology, engineering or mathematics, we put “Yes.” If not, we put “No.” If the field was left blank, no website was available.
`Obama Alum?` | We put “Yes” if the candidate mentions working for the Obama administration or campaign on his or her website, or if the candidate shows up on this list of Obama administration members and campaign hands running for office. If not, we put “No.”
`Dem Party Support?` | “Yes” if the candidate was placed on the DCCC’s Red to Blue list before the primary, was endorsed by the DSCC before the primary, or if the DSCC/DCCC aired pre-primary ads in support of the candidate. (Note: according to the DGA’s press secretary, the DGA does not get involved in primaries.) “No” if the candidate is running against someone for whom one of the above things is true, or if one of those groups specifically anti-endorsed or spent money to attack the candidate. If those groups simply did not weigh in on the race, we left the cell blank.
`Emily Endorsed?` | “Yes” if the candidate was endorsed by Emily’s List before the primary. “No” if the candidate is running against an Emily-endorsed candidate or if Emily’s List specifically anti-endorsed or spent money to attack the candidate. If Emily’s List simply did not weigh in on the race, we left the cell blank.
`Gun Sense Candidate?` | “Yes” if the candidate received the Gun Sense Candidate Distinction from Moms Demand Action/Everytown for Gun Safety before the primary, according to media reports or the candidate’s website. “No” if the candidate is running against an candidate with the distinction. If Moms Demand Action simply did not weigh in on the race, we left the cell blank.
`Biden Endorsed?` | “Yes” if the candidate was endorsed by Joe Biden before the primary. “No” if the candidate is running against a Biden-endorsed candidate or if Biden specifically anti-endorsed the candidate. If Biden simply did not weigh in on the race, we left the cell blank.
`Warren Endorsed?` | “Yes” if the candidate was endorsed by Elizabeth Warren before the primary. “No” if the candidate is running against a Warren-endorsed candidate or if Warren specifically anti-endorsed the candidate. If Warren simply did not weigh in on the race, we left the cell blank.
`Sanders Endorsed?` | “Yes” if the candidate was endorsed by Bernie Sanders before the primary. “No” if the candidate is running against a Sanders-endorsed candidate or if Sanders specifically anti-endorsed the candidate. If Sanders simply did not weigh in on the race, we left the cell blank.
`Our Revolution Endorsed?` | “Yes” if the candidate was endorsed by Our Revolution before the primary, according to the Our Revolution website. “No” if the candidate is running against an Our Revolution-endorsed candidate or if Our Revolution specifically anti-endorsed or spent money to attack the candidate. If Our Revolution simply did not weigh in on the race, we left the cell blank.
`Justice Dems Endorsed?` | “Yes” if the candidate was endorsed by Justice Democrats before the primary, according to the Justice Democrats website, candidate website or news reports. “No” if the candidate is running against a Justice Democrats-endorsed candidate or if Justice Democrats specifically anti-endorsed or spent money to attack the candidate. If Justice Democrats simply did not weigh in on the race, we left the cell blank.
`PCCC Endorsed?` | “Yes” if the candidate was endorsed by the Progressive Change Campaign Committee before the primary, according to the PCCC website, candidate website or news reports. “No” if the candidate is running against a PCCC-endorsed candidate or if the PCCC specifically anti-endorsed or spent money to attack the candidate. If the PCCC simply did not weigh in on the race, we left the cell blank.
`Indivisible Endorsed?` | “Yes” if the candidate was endorsed by Indivisible before the primary, according to the Indivisible website, candidate website or news reports. “No” if the candidate is running against an Indivisible-endorsed candidate or if Indivisible specifically anti-endorsed or spent money to attack the candidate. If Indivisible simply did not weigh in on the race, we left the cell blank.
`WFP Endorsed?` | “Yes” if the candidate was endorsed by the Working Families Party before the primary, according to the WFP website, candidate website or news reports. “No” if the candidate is running against a WFP-endorsed candidate or if the WFP specifically anti-endorsed or spent money to attack the candidate. If the WFP simply did not weigh in on the race, we left the cell blank.
`VoteVets Endorsed?` | “Yes” if the candidate was endorsed by VoteVets before the primary, according to the VoteVets website, candidate website or news reports. “No” if the candidate is running against a VoteVets-endorsed candidate or if VoteVets specifically anti-endorsed or spent money to attack the candidate. If VoteVets simply did not weigh in on the race, we left the cell blank.
`No Labels Support?` | “Yes” if a No Labels-affiliated group (Citizens for a Strong America Inc., Forward Not Back, Govern or Go Home, United for Progress Inc. or United Together) spent money in support of the candidate in the primary. “No” if the candidate is running against an candidate supported by a No Labels-affiliated group or if a No Labels-affiliated group specifically anti-endorsed or spent money to attack the candidate. If No Labels simply did not weigh in on the race, we left the cell blank.

`rep_candidates.csv` includes: 

Column | Description 
-------|--------------
`Rep Party Support?` | “Yes” if the candidate was named to the NRCC’s Young Guns list (any tier) before the primary, was endorsed by the NRSC before the primary, was endorsed by the RGA before the primary or if the Senate Leadership Fund or Congressional Leadership Fund made independent expenditures in support of the candidate in the primary.  “No” if the candidate is running against someone for whom one of the above things is true, or if one of those groups specifically anti-endorsed or spent money to attack the candidate. If those groups simply did not weigh in on the race, we left the cell blank.
`Trump Endorsed?` | “Yes” if the candidate was endorsed by President Trump before the primary. “No” if the candidate is running against a Trump-endorsed candidate or if Trump specifically anti-endorsed the candidate. If Trump simply did not weigh in on the race, we left the cell blank.
`Bannon Endorsed?` | “Yes” if the candidate was endorsed by Steve Bannon before the primary. “No” if the candidate is running against a Bannon-endorsed candidate or if Bannon specifically anti-endorsed the candidate. If Bannon simply did not weigh in on the race, we left the cell blank.
`Great America Endorsed?` | “Yes” if the candidate was endorsed by the Great America Alliance before the primary, according to the Great America Alliance website, candidate website or news reports, or if Great America PAC spent money in the primary on the candidate’s behalf. “No” if the candidate is running against a Great America-endorsed candidate or if Great America specifically anti-endorsed or spent money to attack the candidate. If Great America simply did not weigh in on the race, we left the cell blank.
`NRA Endorsed?` | “Yes” if the candidate was endorsed by the National Rifle Association before the primary, according to the NRA website, candidate website or news reports, or if the NRA made independent expenditures in the primary on the candidate’s behalf. “No” if the candidate is running against an NRA-endorsed candidate or if the NRA specifically anti-endorsed or spent money to attack the candidate. If the NRA simply did not weigh in on the race, we left the cell blank.
`Right to Life Endorsed?` | “Yes” if the candidate was endorsed by the National Right to Life Committee or a local affiliate before the primary, according to the organization’s website, candidate website or news reports. “No” if the candidate is running against a Right to Life-endorsed candidate(s) or if Right to Life specifically anti-endorsed or spent money to attack the candidate. If Right to Life simply did not weigh in on the race, we left the cell blank.
`Susan B. Anthony Endorsed?` | “Yes” if the candidate was endorsed by Susan B. Anthony List before the primary, according to the SBA List website, candidate website or news reports. “No” if the candidate is running against a SBA List-endorsed candidate or if SBA List specifically anti-endorsed or spent money to attack the candidate. If SBA List simply did not weigh in on the race, we left the cell blank.
`Club for Growth Endorsed?` | “Yes” if the candidate was endorsed by the Club for Growth before the primary, according to the Club for Growth website, candidate website or news reports, or if Club for Growth Action made independent expenditures in the primary on the candidate’s behalf. “No” if the candidate is running against a Club for Growth-endorsed candidate or if the Club for Growth specifically anti-endorsed or spent money to attack the candidate. If the Club for Growth simply did not weigh in on the race, we left the cell blank.
`Koch Support?` | “Yes” if the candidate was supported by the Koch brothers’ political network in the primary. This could include an endorsement from David or Charles Koch, financial support from groups like Americans for Prosperity (including a state affiliate), Freedom Partners Action Fund or KochPAC or an endorsement from one of those groups. “No” if the candidate is running against a Koch-endorsed candidate or if the Koch brothers’ political network specifically anti-endorsed or spent money to attack the candidate. If the Koch brothers’ political network simply did not weigh in on the race, we left the cell blank.
`House Freedom Support?` | “Yes” if the candidate was supported by the House Freedom Fund in the primary. This could include an endorsement, a donation or an independent expenditure on the candidate’s behalf. “No” if the candidate is running against a House Freedom Fund-endorsed candidate or if the House Freedom Fund specifically anti-endorsed or spent money to attack the candidate. If the House Freedom Fund simply did not weigh in on the race, we left the cell blank.
`Tea Party Endorsed?` | “Yes” if the candidate was endorsed by the Tea Party Express before the primary, according to the Tea Party Express website, candidate website or news reports. “No” if the candidate is running against a Tea Party Express-endorsed candidate or if Tea Party Express specifically anti-endorsed or spent money to attack the candidate. If Tea Party Express simply did not weigh in on the race, we left the cell blank.
`Main Street Endorsed?` | “Yes” if the candidate was endorsed by the Republican Main Street Partnership before the primary, according to the candidate website or news reports. “No” if the candidate is running against a Main Street-endorsed candidate or if Main Street specifically anti-endorsed or spent money to attack the candidate. If Main Street simply did not weigh in on the race, we left the cell blank.
`Chamber Endorsed?` | “Yes” if the candidate was endorsed by the U.S. Chamber of Commerce or a state-level chamber of commerce before the primary, according to the candidate website or news reports, or if the national or state chamber of commerce made independent expenditures for the candidate during the primary. “No” if the candidate is running against a Chamber of Commerce-endorsed candidate or if the Chamber of Commerce specifically anti-endorsed or spent money to attack the candidate. If the Chamber of Commerce simply did not weigh in on the race, we left the cell blank.
