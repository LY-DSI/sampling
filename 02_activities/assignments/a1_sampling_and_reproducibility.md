# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: Yi Li
The blog post suggests that tracing systems tend to prioritize efficiency over representativeness, which leads to an overemphasis on institutional outbreaks. The toy model clearly demonstrates how structural biases can distort public health narratives.Similar issues affect both digital tracing—where privacy concerns can reduce app uptake—and manual efforts, which often suffer from participant attrition in marginalized communities.

The simulation model (whitby_covid_tracing.py) includes three key sampling stages, each reflecting the structural biases discussed in the associated blog post. The first stage, Initial Infection Sampling, uses np.random.choice() within the simulate_event() function to randomly infect 10% of the total population (1,000 individuals across weddings and brunches), based on a uniform attack rate. This step assumes equal risk across events and represents an unbiased—but typically unobservable—baseline transmission, aligning with the blog’s premise that “10% of people at every event are infected.” The second stage, Primary Contact Tracing Sampling, applies np.random.rand() with a threshold defined by TRACE_SUCCESS = 0.20 to simulate tracing success. Here, only infected individuals (about 100 people) are eligible, and each has a 20% chance of being traced through Bernoulli sampling, mirroring real-world limitations like imperfect recall and resource constraints. This reflects the blog’s claim that “an infection has only a 20% chance of being traced to a source event.” The final stage, Secondary Contact Tracing Sampling, introduces conditional tracing based on event-level thresholds. Events with at least two primary-traced cases (as determined by event_trace_counts and SECONDARY_TRACE_THRESHOLD = 2) trigger full tracing of all infected attendees at that event. This deterministic mechanism disproportionately affects large gatherings—like weddings—making them more likely to be flagged for follow-up, while smaller events like brunches often go unnoticed. This models the blog’s argument that contact tracing systems tend to favor low-effort, high-yield targets, thereby reinforcing structural biases.

To make the whitby_covid_tracing.py script reproducible, a fixed random seed (np.random.seed(42)) was added after the imports to ensure consistent outputs from stochastic functions like np.random.choice() and np.random.rand(), which previously led to different results with each run. This change guarantees that infections and primary tracing outcomes follow the same sequence every time, producing identical histograms across runs. Additionally, the number of simulation repetitions was reduced from 1000 to 100 to improve runtime efficiency during testing; with the seed in place, fewer runs still demonstrate reproducibility. These changes result in consistent outputs (e.g., traced proportions at weddings reliably cluster around ~40%), though they do limit variability, which is important in research settings. To assess robustness, running multiple seeds or removing the seed entirely may be preferable. The choice of seed (42) is arbitrary but sufficient to stabilize results.


```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
