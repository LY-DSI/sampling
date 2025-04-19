# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `3`

Describe the purpose of your survey:
```
This survey aims to investigate the relationship between age and music taste, focusing on how perceptions of popular music change between individuals of different ages and within individuals over time. 
```

Describe your target population, sampling frame, sampling units, and observational units:
```
Target Population: Individuals aged 16 and older, residing in Canada, with access to digital media and some engagement with music (e.g., regular listening to music through streaming, radio, or other means).

Sampling Frame: Email lists and social media networks of university students and alumni, music-related online communities, and general population panels (such as university-managed survey pools).

Sampling Units: Individual respondents.

Sampling Strategy:

Stratified random sampling to ensure proportional age-group representation.

Oversampling of older adults (50+) to counter lower response rates.

Longitudinal component: Follow-up with a subset (N=500) after 5 years to track intra-individual changes.
```

Your 5-10 question survey:
```
1. What is your current age?

[Open text or dropdown]

2. How often do you listen to music?

Several times a day / Daily / A few times a week / Rarely / Never


3. Which genres do you enjoy most? (Select up to 3)

Pop / Rock / Hip-hop/Rap / Jazz / Classical / Electronic / Country / R&B / Other (specify)


4. How do you discover new music? (Select all that apply)

Streaming algorithms (e.g., Spotify, Apple Music) / Social media / Friends/family / Radio / Live events / Other


5. Do you feel that today’s popular music reflects your personal taste?

Yes, mostly / Somewhat / Not really / Not at all


6. How do you feel about current popular music compared to the music you listened to when you were younger?

I prefer current popular music / I prefer the music from my younger years / I like both equally / I don’t follow current popular music


7. Have your music preferences changed significantly as you've aged?

 Yes / Somewhat / No

(If yes/somewhat) Please describe how your music taste has changed: [Open text]



## Part B - Survey Evaluation:

Identify and describe survey features:

```
1. Sample Type
Stratified probability sample with a two-stage design:

First stage: Groups of telephone numbers (landline and cellular) linked to addresses or standalone numbers.

Second stage: One randomly selected individual aged 15+ per household.

Rejective sampling was used for efficiency: Volunteers completed a long interview, while non-volunteers were split into long/short interview groups.

2. Sample Size
Field sample: ~50,000 units (households).

Invitations sent: ~40,000 for electronic questionnaires.

Expected completions: 24,000 questionnaires.

3. Target Population
All individuals aged 15+ living in Canada’s 10 provinces, excluding full-time institutional residents (e.g., long-term care facilities).

4. Sampling Frame
Combined landline/cellular numbers from Census and administrative sources, supplemented by Statistics Canada’s dwelling frame.

Stratified by province/census metropolitan area (CMA), with 27 strata (e.g., Toronto, Vancouver, non-CMA regions).

5. Survey Mode(s)
Electronic questionnaire (primary) and computer-assisted telephone interviewing (CATI).

No proxy responses allowed; interviews available in English/French.

6. Timeline
Collection period: September 4 to December 28, 2018.

Reference period: Past 12 months preceding the interview.

Data release: January 26, 2021.

7. Response Rate
Not explicitly stated in the documentation, but the survey was voluntary. Response rates for GSS cycles vary and are influenced by factors such as survey mode and topic

8. Weights
Person-level weights adjusted for:

Probability of selection (accounting for rejective sampling).

Alignment with 2017 Census income distributions by province.

9. Data Processing
Automated and manual edits for consistency, flow, and family relationships (e.g., age vs. birth date checks).

Linked tax data: Personal/family income from 2017 T1FF files for ~82% of respondents (with consent); missing data imputed.

10. Cleaning & Imputation
Donor imputation: Missing values filled using records from similar respondents (9 steps for volunteering, donations, income).

Mean imputation used where donor matching was infeasible.

11. Sources of Error
Coverage bias: Excludes institutionalized populations and territories.

Non-response bias: Voluntary participation may skew results.

Measurement error: Self-reported data (e.g., volunteering hours) may be inaccurate.

12. Limitations & Biases
Undercoverage: No data from Yukon, Northwest Territories, or Nunavut.

Income data reliance: Linked tax records were incomplete for ~18% of respondents.

Recall bias: 12-month reference period may affect accuracy.

13. Documentation & Sources
Primary source: https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=4430

Variable-specific details:https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvVariableList&Id=796234

Historical cycles: https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getInstanceList&Id=87858
```

## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
