# GSoC Idea: Build Workflow Process for CHAOSS Diversity & Inclusion Badging
Issue link: https://github.com/badging/diversity-and-inclusion/issues/1
## Microtask 0
### `Q 0` How would IMS standards be helpful in improving the D&I Badging Project?


IMS standard Open Badges v2.0 defines a way to link data in with an image. This format is implemented using JSON-LD.
Open Badges can be used as credentials. This can be used to:
*  Verify if the badge is authentic
*  See who the issuers and the receivers are
* Display badges on a wide variety of platforms


Currently, D&I badging program uses png images with four badging statuses. Images are portable, but they can also be used by anyone without authorisation. Using Open Badges could improve the D&I badging program in the following ways:
* Award badges based on reviews
* Link Diversity and Inclusion metrics with a badge
* Open Badges are platform independent, so a project could showcase them in different places like website, README etc
* Contain information about issuers, reviewers, badging submission issue link


### `Q 1` What parts of the Journal of Open Source Software Documentation could be helpful in improving the D&I Badging Project?


#### **Review checklist and guidelines**


JOSS has a comprehensive review checklist that is used by a reviewer to verify what the project contains or does not contain, comparing that with what is required for an acceptable JOSS submission. This list also contains some things that the reviewer needs to confirm for themselves (if they have read the JOSS code of conduct and conflict of interest policy). 


The D&I badging submission process can adopt from this in the following manner:
* Creating a Conflict of Interest policy and additional guidelines for someone to become a reviewer
* Possibly using the issue templates in the D&I badging repository and converting them to a checklist format, where reviewers are given edit access to the issue description, and they can tick off the parts that the project/event aligns with
* Detailing who the submitting authority, reviewers and maintainers of badging repository are, and keeping important information in one place
* Creating different checklists for events and projects


#### **Roles in JOSS**


JOSS has comprehensive guidelines for its paper review process. There are mainly four kinds of people involved:
* Editor in chief - Runs a small initial check over the submitted paper and assigns handling editor(s) to it
* Handling editor - They check if the paper complies with JOSS submission guidelines, if not, then this is the point from where the paper goes no further
* Reviewers - Reviewers are the people who give direct feedback to paper submitters. They don't outright reject a paper, they suggest major or minor changes, if any required. This is done by opening issues in the paper-related software repository or by commenting on the [REVIEW] issue
* Authors - Authors are the major contributors in the software project. They are the ones responsible for making paper submission and making their submission fit with JOSS guidelines


There are defined roles in JOSS submission process. D&I badging project could benefit from a similar review workflow with some changes. Here's how that can possibly be done:
* CHAOSS maintainers equivalent Editor in Chief's
* Reviewers and Handling editors equivalent - There can be rules to determine their eligibility, or they can be volunteers similar to JOSS reviewers.
* Major software contributors/ Event Organisers - The people who are submitting their event/project into the badging program. The reviewers will give them feedback on how to improve upon their submission


#### **Review process implementation**


JOSS review process consists of [PRE-REVIEW] and [REVIEW] phases after the paper submission. Whedon, a GitHub bot, helps out extensively with the review process. Here's how that happens:
* First, Whedon opens an issue for [PRE-REVIEW] and mentions the handling editor picked by the author. Here, it is determined if the project will move forward with the review process or not.
* Next, Whedon opens an issue labeled [REVIEW] corresponding to the submitted paper and pre-review. Here, a checklist for reviewers and project eligibility is generated in the initial issue template by Whedon. If the reviewers fulfill all criteria, they suggest edits (if any required) to the project repository.


D&I badging project can get use this in the following way:
* A GitHub bot can be created to handle some common commands related to an issue-based Workflow without the intervention of project maintainers.
* The bot can participate in multiple issues, allowing reviewers to unassign themselves from reviews, setting deadlines, and possibly assign badges according to the checklist.
## Microtask 1:
### `Q 2` How do these folders differ from each other?


**README.md**


* *Project folder*
   * It contains requirements for submitting projects to D&I Badging. These requirements are based on the Journal of Open Source Software's paper submission guidelines. Diversity and Inclusion badge statuses have also been listed here, describing the badges available in Docs-Diversity-Inclusion-Badging/assets/badges directory based on how many deliverables they meet.
* *Event folder*
   * It contains only the title.


**Chaoss-Metrics.md**


* *Project folder*
   * It contains information about five CHAOSS Diversity and Inclusion metrics relevant to an open-source project. These metrics are directly defined by the questions their definition includes. For example, *Response Time and Quality of a Project* depends on responsiveness to suggestions and Pull Requests
* *Event folder*
   * Contains information about Diversity and Inclusion metrics which are used to define an event's diversity. Similar to event metrics, these are defined by asking questions. For example, *Diversity Access Tickets* can be defined by how they are used for an event, and if their usage actually leads to better inclusion.


**Criteria.md**


* *Project folder*
   * Each metric listed in CHAOSS-Metrics has been associated with more questions. The questions are divided with respect to the metric they address. There are no sections here.
* *Event folder*
   * The contents of CHAOSS-Metrics file have been addressed here and expanded upon. Each metric has two or more sections. Generally, the content of the first section is question-related to evaluating how the data associated with the metric was collected or how the contents of the event affect the metric. The last section asks if the person/organization who submitted the event gave their statement agreeing to the metric.


**Requirements.md**


* *Project folder*
   * This file contains five submission requirements and process 
* *Event folder*
   * This file contains two submission requirements and processes for events.


**badged-project.md** and **badged-events.md** are empty files that exist in Project and Event folders respectively. Overall, the Event folder seems to be missing out on more details in comparison with the Project folder.


### `Q 3` How are they similar?


Both of these folders require a solid definition of how badges work, if there would be any differences between event and project reviews. The reviewing and submission guidelines can be improved. These folders use five D&I metrics to define criteria for badging. The files are similar in what kind of information they hold differing only when it comes to the actual content specific to each folder.
## Microtask 2:
### `Q 4` Are the issue templates any different when you view them in GitHub versus your local machine? If so, how?


These issue templates are different between how they appear on GitHub (rendered Markdown) and how they appear in a text editor (source Markdown). Source Markdown has a lot more content compared to what actually shows up on the issue template. When an issue is opened using the template, the source Markdown is visible. It provides pointers on how to fill the details in an issue template.


As for the content, these templates are based on Criteria.md for both events and projects respectively. 
### `Q 5` Explain why this project may want to use GitHub issue templates as a badging submission method.


This project may want to use GitHub issue templates as a badging submission method because:
* Templates provide a basic skeleton for how information needs to be filled in an issue. For badging submissions, it is important to have information against which it can be checked how each project/event aligns with D&I metrics. Issue templates can make sure that all necessary information is collected and not missed out on.
* There can be multiple issue templates and they can be picked on the basis of requirement by the issue creator.
* There are various ways to both segregate and combine issues. They can be put together on GitHub project boards, made a part of milestones, labeled to represent different areas/status/priority and be searched by labels, all the while maintaining readability.
* Markdown based checklists can be used in issue templates, and they can be edited by people with permissions to make changes to the issue description.














## Chore: Open draft PR for Event Badge




Issue link: https://github.com/badging/meta/issues/7
PR link: https://github.com/badging/event-diversity-and-inclusion/pull/1


Some thoughts on how the existing process can be improved:
* If DCO sign off is required by someone making a PR for event badging, then doing it through GUI would only increase work, as adding DCO sign off through GitHub is not supported yet.
* Instead, instructions could be included about how to make edits and sign off commits through CLI.
* PR templates could be represented in a different manner. It could be explained better how the information in the PR template will be used.
* A diagram of submission flow could be included to give submitters a better idea about how the process will work.
