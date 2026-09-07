# Step 17 — Examine Moderators
[← Previous Step: Examine Heterogeneity](https://github.com/adnan-mayof/Examine-Heterogeneity/blob/main/README.md)
[← Previous Step: Conduct the Meta-Analysis](https://github.com/adnan-mayof/Conduct-the-Meta-Analysis/blob/main/README.md)


## Maya’s Evidence Synthesis Journey

### Why Are Some Effects Larger Than Others?

Maya has now completed the first major stages of her quantitative analysis.

She started with **111 eligible studies** for the systematic review.

After determining which studies could contribute quantitative results, **22 studies** contributed to the primary meta-analysis.

She then:

* prepared the analysis data
* calculated effect sizes
* conducted the meta-analysis
* examined heterogeneity

For this illustrative example, her meta-analysis produced:

> **Pooled Hedges' g = 0.64 (95% CI [0.52, 0.76])**

She also found evidence of between-study heterogeneity:

> **I² = 58%**

Maya looks at the forest plot again.

> **Maya:** “The studies don't all have the same effect.”

> **Mentor:** “Right.”

> **Maya:** “And we know there is variation. But can we figure out what might explain it?”

> **Mentor:** “That's exactly what moderator analysis is for.”

Maya opens the extraction dataset from Step 13.

She already collected information about:

* AI technology
* AI function
* learner level
* intervention duration
* learning context
* outcome type
* study design

> **Maya:** “So these characteristics might help explain why the effects differ?”

> **Mentor:** “They might. Now we need to test those possibilities carefully.”

---

# 1. What Is a Moderator?

A **moderator** is a characteristic that may be associated with variation in the effect of an intervention or exposure across studies.

In Maya's review, potential moderators could include:

* type of AI technology
* AI function
* learner level
* intervention duration
* learning context
* outcome type
* study design

For example:

> **Does intervention duration help explain why some AI interventions have larger effects than others?**

That is a moderator question.

---

# 2. Heterogeneity vs. Moderators

Maya remembers the previous step.

### Step 16 asked:

> **“How much do the effects differ?”**

### Step 17 asks:

> **“Are study characteristics associated with differences in the effects?”**

The distinction is:

| Question                                      | Analysis           |
| --------------------------------------------- | ------------------ |
| How much do effects vary?                     | Heterogeneity      |
| What characteristics might explain variation? | Moderator analysis |

The process is:

```text id="x7n4fz"
Individual effect sizes
        ↓
Meta-analysis
        ↓
Pooled effect
        ↓
Heterogeneity
        ↓
Effects vary
        ↓
Potential explanations
        ↓
Moderators
```

---

# 3. Maya's Potential Moderators

Maya reviews her extraction dataset.

| Variable              | Example categories                   |
| --------------------- | ------------------------------------ |
| AI technology         | AI tutor, chatbot, adaptive AI       |
| AI function           | Tutoring, feedback, assessment       |
| Learner level         | High school, undergraduate, graduate |
| Intervention duration | Short, medium, long                  |
| Learning context      | Classroom, online, blended           |
| Outcome               | Achievement, knowledge, skill        |
| Study design          | RCT, quasi-experimental              |

Maya now has several hypotheses she could investigate.

But her mentor gives her an important warning.

> **Mentor:** “Having a variable does not automatically mean you should test it as a moderator.”

---

# 4. Moderators Should Be Planned

Maya asks:

> **Maya:** “Why can't I test every variable?”

Her mentor explains:

> **Mentor:** “Because if you test enough variables, some results may appear interesting simply by chance.”

Moderator analyses should therefore be guided by:

* the research question
* theory
* prior evidence
* the protocol
* plausible mechanisms
* available data

Maya remembers that her research question specifically asks:

> **What characteristics of the intervention, learners, learning context, and study methodology explain variation in effects?**

That provides a foundation for her moderator analysis.

---

# 5. Categorical Moderators

Some moderators consist of categories.

For example:

**AI function**

* Tutoring
* Feedback
* Assessment

Maya can compare the estimated effects across these categories.

Suppose her illustrative results are:

| AI function | Studies | Pooled Hedges' g |
| ----------- | ------: | ---------------: |
| Tutoring    |       8 |             0.78 |
| Feedback    |       7 |             0.61 |
| Assessment  |       7 |             0.48 |

Maya sees that tutoring has the largest estimated effect.

> **Maya:** “So tutoring is definitely better!”

Her mentor pauses.

> **Mentor:** “Not so fast.”

---

# 6. A Difference Between Groups Is Not Automatically Evidence of a Moderator

Maya asks:

> **Maya:** “Why not?”

Her mentor explains:

> **Mentor:** “The subgroup estimates are different, but we need to statistically test whether the difference between groups is greater than would be expected from sampling variation.”

This is critical.

For example:

**Tutoring: g = 0.78**

**Feedback: g = 0.61**

The estimates differ.

But Maya needs a formal moderator test.

She cannot simply look at the two numbers and conclude that AI function explains the difference.

---

# 7. The Omnibus Test

For a categorical moderator with multiple groups, Maya may conduct an **omnibus test of moderators**.

Conceptually, the test asks:

> **“Do the estimated effects differ across the moderator categories?”**

For example:

```text id="0q83q1"
AI Function
     │
 ┌───┼───────────┐
 ↓   ↓           ↓
Tutoring Feedback Assessment
 0.78    0.61       0.48
       ↓
Moderator test
       ↓
Do the groups differ?
```

The exact statistical implementation depends on the meta-analytic model.

---

# 8. Example Moderator Result

Suppose Maya obtains:

> **QM(2) = 7.84, p = .020**

Maya asks:

> **Maya:** “What does that tell me?”

Her mentor explains:

> “The moderator test provides evidence that the estimated effects differ across the AI-function categories.”

But Maya still needs to examine:

* the subgroup estimates
* confidence intervals
* number of studies in each subgroup
* methodological differences
* possible confounding
* whether the moderator was prespecified

---

# 9. Continuous Moderators

Not every moderator is categorical.

Some variables are continuous.

For example:

**Intervention duration**

| Study | Duration |
| ----- | -------: |
| S001  |  4 weeks |
| S002  |  6 weeks |
| S003  |  8 weeks |
| S004  | 12 weeks |
| S005  | 16 weeks |

Maya asks:

> **Maya:** “Can I test whether longer interventions produce larger effects?”

> **Mentor:** “Yes. Intervention duration can be treated as a continuous moderator if that matches your analysis plan and the data support it.”

The question becomes:

> **Is intervention duration associated with variation in effect size?**

---

# 10. Meta-Regression

When Maya examines a continuous study-level moderator, she enters the territory of **meta-regression**.

Conceptually:

```text id="9i2f8r"
Intervention duration
        ↓
      Model
        ↓
Effect size
```

For example, she could investigate whether effect size changes as intervention duration increases.

A simplified model might be represented as:

**Effect size = intercept + slope × duration + error**

The slope describes the estimated association between duration and effect size.

---

# 11. Example Meta-Regression Result

Suppose Maya obtains:

> **β = 0.025 per additional week**

with:

> **95% CI [0.008, 0.042], p = .006**

Maya asks:

> **Maya:** “So every additional week causes the effect to increase by 0.025?”

> **Mentor:** “No.”

This is a **study-level association**.

It does not establish that adding one week of intervention would causally increase the effect by 0.025.

Maya should describe it as an association between study-level intervention duration and estimated effect size.

---

# 12. Association Is Not Causation

This is especially important for observational characteristics of studies.

Suppose studies with longer interventions also tend to:

* use newer AI technology
* have larger samples
* use different populations
* use different outcome measures

If Maya finds a relationship between duration and effect size, she cannot automatically conclude that duration itself caused the difference.

Other study characteristics may be related to both.

Therefore:

> **Moderator analysis identifies statistical associations; it does not automatically establish causality.**

---

# 13. The Ecological Nature of Study-Level Moderators

Maya asks:

> **Maya:** “But I'm using study characteristics. Does that change how I interpret the result?”

> **Mentor:** “Yes.”

A study-level moderator describes differences **between studies**.

For example:

> Studies using longer interventions tended to have larger effects.

That does **not necessarily mean**:

> Individual students who receive a longer intervention will experience a larger effect.

This is an important limitation of study-level moderator analysis.

---

# 14. Subgroup Analysis

Maya learns that categorical moderators can often be examined through subgroup analyses.

For example:

### Learner level

| Learner level | Studies | Hedges' g |
| ------------- | ------: | --------: |
| High school   |       6 |      0.51 |
| Undergraduate |      10 |      0.71 |
| Graduate      |       6 |      0.59 |

Maya can describe the estimated effects within each subgroup.

But again:

> **Different subgroup estimates do not automatically establish a statistically meaningful subgroup difference.**

The between-group test matters.

---

# 15. Why Sample Size Matters

Maya notices that some moderator categories contain many studies while others contain only a few.

For example:

| AI function | Studies |
| ----------- | ------: |
| Tutoring    |      12 |
| Feedback    |       8 |
| Assessment  |       2 |

Maya asks:

> **Maya:** “Can I compare all three groups?”

Her mentor responds:

> **Mentor:** “You can examine them if the analysis is methodologically appropriate, but the small assessment subgroup requires caution.”

A subgroup represented by very few studies may produce:

* imprecise estimates
* unstable estimates
* wide confidence intervals

Therefore, Maya should consider the amount of evidence supporting each subgroup.

---

# 16. Don't Create Categories Just to Get a Result

Maya considers dividing intervention duration into:

* 1–4 weeks
* 5–7 weeks
* 8–10 weeks
* 11–13 weeks
* 14–16 weeks

Her mentor asks:

> **Mentor:** “Why those categories?”

Maya pauses.

> **Maya:** “Because they give me more groups.”

> **Mentor:** “That's not enough.”

Categorization should be justified by:

* theory
* substantive meaning
* protocol
* prior evidence
* meaningful thresholds

Creating arbitrary categories after seeing the data can produce misleading results.

When appropriate, a continuous moderator may be preferable to arbitrary categorization.

---

# 17. Too Many Moderators

Maya now has many possible variables.

She lists:

1. AI technology
2. AI function
3. learner level
4. intervention duration
5. learning context
6. outcome type
7. study design
8. publication year
9. sample size

Her mentor asks:

> **Mentor:** “How many studies do you have?”

> **Maya:** “Twenty-two.”

Her mentor responds:

> **Mentor:** “Then you need to be careful.”

With only 22 studies, fitting a large number of moderator variables can produce unstable estimates and overfitting.

The amount of information available should guide how many moderators Maya examines.

---

# 18. The “10 Studies per Predictor” Rule

Maya hears a common rule:

> **“You need 10 studies per moderator.”**

Her mentor clarifies:

> **Mentor:** “Treat that as a rough rule of thumb, not a universal law.”

The often-cited **10 studies per predictor** idea is used as a caution about the limited information available for meta-regression.

It does not mean:

> “If you have fewer than 10 studies, meta-regression is impossible.”

Nor does it mean:

> “If you have exactly 10 studies, the analysis is automatically appropriate.”

The appropriate number depends on:

* model complexity
* number of predictors
* heterogeneity
* study sizes
* distribution of moderators
* quality of the data
* research design

With only **22 studies**, Maya should keep the moderator analysis focused and theoretically justified.

---

# 19. Univariate vs. Multivariable Meta-Regression

Maya learns that moderator analyses can have different levels of complexity.

### One moderator

For example:

> Does intervention duration relate to effect size?

### Multiple moderators

For example:

> Does intervention duration remain associated with effect size after accounting for learner level and AI function?

The second question requires a more complex model.

Maya should not automatically include every available moderator in one model.

---

# 20. Confounding Between Moderators

Suppose:

* longer interventions are mostly used with AI tutors
* shorter interventions are mostly used with chatbots

Maya observes that longer interventions have larger effects.

But she cannot easily determine whether the difference is associated with:

**duration**

or

**AI function**

or both.

This illustrates why moderator results should be interpreted cautiously.

Study characteristics can be correlated with one another.

---

# 21. The Risk of Multiple Testing

Maya asks:

> **Maya:** “What happens if I test 20 different moderators?”

Her mentor explains:

> “The more statistical tests you conduct, the greater the opportunity to observe apparently interesting findings by chance.”

Therefore, Maya should:

* prespecify important moderators
* limit unnecessary analyses
* distinguish planned from exploratory analyses
* report all relevant analyses transparently
* interpret exploratory findings cautiously

---

# 22. Moderator Analysis Does Not Prove a Mechanism

Suppose Maya finds:

> AI tutoring studies have larger effects than chatbot studies.

She should not automatically conclude:

> “Tutoring is more effective because it provides personalized instruction.”

That is a **possible explanation**, but the moderator analysis itself does not establish the mechanism.

The study-level data may not contain enough information to test that explanation.

Maya should distinguish:

**Observed association**

from

**Proposed explanation**

---

# 23. Maya's First Categorical Moderator

Maya decides to examine **AI function**.

Her illustrative results are:

| AI function |  k | Hedges' g | 95% CI       |
| ----------- | -: | --------: | ------------ |
| Tutoring    |  8 |      0.78 | [0.61, 0.95] |
| Feedback    |  7 |      0.61 | [0.44, 0.78] |
| Assessment  |  7 |      0.48 | [0.27, 0.69] |

The omnibus moderator test is:

> **QM(2) = 7.84, p = .020**

Maya writes:

> “Estimated effects differed across AI-function categories.”

She does **not** write:

> “AI tutoring definitely causes larger learning gains.”

The second statement goes beyond what the moderator analysis establishes.

---

# 24. Maya's Continuous Moderator

Next, Maya examines intervention duration.

Her illustrative meta-regression gives:

> **β = 0.025 per week**

> **95% CI [0.008, 0.042]**

> **p = .006**

Maya interprets this as:

> “Across the included studies, longer intervention duration was statistically associated with larger estimated effects.”

She adds an important qualification:

> “Because duration is a study-level characteristic and the analysis is observational across studies, this association should not be interpreted as evidence that extending an intervention by one week would necessarily produce a corresponding increase in learning.”

---

# 25. Moderator Results and Heterogeneity

Maya remembers Step 16.

She asks:

> **Maya:** “Can moderators explain all the heterogeneity?”

> **Mentor:** “Not necessarily.”

A moderator may explain **some** variation while substantial unexplained heterogeneity remains.

For example:

| Analysis                    |    τ² |
| --------------------------- | ----: |
| Before moderator            | 0.052 |
| After AI-function moderator | 0.036 |

Maya observes that estimated between-study variance decreased.

That may suggest that AI function accounts for some variation.

But it does not mean that AI function explains everything.

Other factors may remain.

---

# 26. Explained Heterogeneity

Maya asks:

> **Maya:** “Can I say the moderator explains 100% of the heterogeneity if tau-squared becomes zero?”

Her mentor explains:

> **Mentor:** “Be careful.”

The interpretation of reductions in τ² and related measures depends on the model and estimation method.

Moderator analyses can indicate that a covariate accounts for some between-study variation, but the analysis should not be presented as proof of a causal mechanism.

Maya documents the model and the change in estimated heterogeneity.

---

# 27. Moderator Analysis and Risk of Bias

Maya remembers Step 10.

She wonders whether study quality could itself be related to effect size.

For example:

> Do studies with different risk-of-bias judgments produce different estimated effects?

This could potentially be examined as a study characteristic if it was prespecified and there are enough informative studies.

But Maya must be careful.

Risk-of-bias judgments are not simply another interchangeable study characteristic.

They represent methodological concerns about the evidence.

Any analysis involving risk of bias should follow the review's protocol and the guidance of the selected risk-of-bias tool.

---

# 28. Moderator Analysis Is Not the Same as Meta-Regression

Maya summarizes:

### Moderator analysis

The broader concept of examining whether study characteristics are associated with differences in effect sizes.

### Subgroup analysis

Often used for categorical moderators.

### Meta-regression

A statistical regression framework for examining associations between effect sizes and study-level covariates.

So:

> **Meta-regression is one way to conduct moderator analysis.**

---

# 29. Maya's Moderator Decision Process

Before running another analysis, Maya asks:

```text id="0y8v8a"
Is the moderator relevant to the research question?
        ↓
Was it prespecified?
        ↓
Is there enough information?
        ↓
Are categories meaningful?
        ↓
Are the studies sufficiently represented?
        ↓
Is the analysis statistically appropriate?
        ↓
Run the analysis
        ↓
Interpret cautiously
        ↓
Report transparently
```

This prevents Maya from simply searching the data for interesting patterns.

---

# 30. Maya's Moderator Table

After completing her planned analyses, Maya creates:

| Moderator     | Type        | Studies | Result                 | Interpretation                                 |
| ------------- | ----------- | ------: | ---------------------- | ---------------------------------------------- |
| AI function   | Categorical |      22 | QM(2) = 7.84, p = .020 | Effects differed across categories             |
| Learner level | Categorical |      22 | QM(2) = 2.31, p = .315 | No clear evidence of subgroup differences      |
| Duration      | Continuous  |      22 | β = 0.025, p = .006    | Longer duration associated with larger effects |
| Study design  | Categorical |      22 | QM(1) = 1.48, p = .224 | No clear evidence of subgroup differences      |

These values are **illustrative**.

Maya would replace them with the actual results from her analysis.

---

# 31. What Does “No Significant Moderator” Mean?

Maya notices that learner level has:

> **p = .315**

She asks:

> **Maya:** “Does that prove learner level doesn't matter?”

Her mentor explains:

> “No.”

A non-significant moderator test means the analysis did not provide sufficient evidence of a difference or association under the specified model and assumptions.

It does not prove that the moderator has no relationship with effects.

The estimate and uncertainty still matter.

---

# 32. What Does a Significant Moderator Mean?

Similarly, a significant moderator does not automatically prove a causal explanation.

For example:

> **AI function: p = .020**

This provides evidence that estimated effects differ across AI-function categories.

It does not establish:

> “AI function causes the difference.”

Other differences between the groups may contribute.

Maya must interpret moderator findings as **associations within the evidence base** unless stronger causal evidence supports a causal conclusion.

---

# 33. Exploratory Moderator Analysis

Sometimes Maya may identify an interesting moderator that was not specified in the original protocol.

Her mentor explains:

> **Mentor:** “You can conduct exploratory analyses, but be transparent.”

Maya should distinguish:

### Prespecified analysis

Planned before examining the results.

### Exploratory analysis

Conducted after seeing the available evidence or results to explore an emerging question.

Exploratory findings can be useful for generating hypotheses.

But they should not be presented as though they were prespecified confirmatory findings.

---

# 34. Maya's Final Understanding

Maya looks at her results.

She now understands the progression:

```text id="s5j1e7"
Step 15
What is the overall effect?
        ↓
Step 16
How much do effects vary?
        ↓
Step 17
What study characteristics
might explain the variation?
```

She has moved from:

> **“What is the average effect?”**

to:

> **“Why might the effects differ?”**

---

# 35. What Happens Next?

Maya's mentor points to her intervention-duration analysis.

> **Mentor:** “You've examined several moderators. But now suppose you want to model multiple study-level characteristics simultaneously.”

Maya asks:

> **Maya:** “So I could examine several predictors in one model?”

> **Mentor:** “Yes. That's where meta-regression becomes especially important.”

Maya looks at her 22 studies.

> **Maya:** “But with only 22 studies, I need to be careful about how many predictors I include.”

> **Mentor:** “Exactly.”

That takes Maya to:

# Step 18 — Conduct Meta-Regression

---

# 36. Key Takeaways

By the end of Step 17, Maya understands:

1. A moderator is a characteristic that may be associated with variation in effect sizes.
2. Heterogeneity asks how much effects vary.
3. Moderator analysis asks whether study characteristics are associated with that variation.
4. Potential moderators should be guided by the research question, theory, prior evidence, and protocol.
5. Categorical moderators can be examined through subgroup analyses and formal between-group tests.
6. A difference between subgroup estimates does not automatically establish a moderator effect.
7. Continuous moderators can be examined using meta-regression.
8. Study-level moderator associations should not automatically be interpreted as causal effects.
9. A study-level relationship does not necessarily describe what happens to individual participants.
10. Small subgroups can produce imprecise or unstable estimates.
11. Arbitrary categorization of continuous variables should be avoided unless substantively justified.
12. Testing many moderators can increase the opportunity for chance findings and unstable estimates.
13. A moderator may explain some heterogeneity without explaining all of it.
14. A statistically significant moderator does not automatically establish a causal mechanism.
15. A non-significant moderator does not prove that the moderator has no relationship with effect size.
16. Prespecified and exploratory moderator analyses should be clearly distinguished.
17. Meta-regression is one statistical approach for conducting moderator analysis.
18. With only 22 studies, Maya should keep moderator analyses focused and carefully justified.
19. The next step is to examine multiple study-level predictors through meta-regression.

---

# Repository Structure

```text id="g0y6tr"
step-17-examine-moderators/
│
├── README.md
│
├── moderators/
│   ├── moderator-guide.md
│   ├── categorical-moderators.md
│   ├── continuous-moderators.md
│   ├── subgroup-analysis.md
│   └── moderator-decisions.md
│
├── data/
│   ├── moderator-data.xlsx
│   └── meta-analysis-data.xlsx
│
├── results/
│   ├── moderator-results.md
│   ├── subgroup-results.md
│   └── moderator-table.xlsx
│
├── documentation/
│   ├── prespecified-moderators.md
│   ├── exploratory-analyses.md
│   └── analysis-log.md
│
└── assessment/
    └── assessment.md
```

---

# Assessment

## Instructions

Choose the best answer for each question.

### 1. What is a moderator?

A. A characteristic that may be associated with variation in effect sizes
B. A database used to search for studies
C. A method for removing duplicate records
D. A risk-of-bias scoring system

### 2. What is the main difference between heterogeneity and moderator analysis?

A. Heterogeneity asks how much effects vary, while moderator analysis examines whether study characteristics are associated with that variation
B. They are exactly the same
C. Moderator analysis determines whether studies are eligible
D. Heterogeneity determines the research question

### 3. Which could be a moderator in Maya's review?

A. AI function
B. File name
C. Database search number
D. Reference-manager folder

### 4. Why should moderators be prespecified when possible?

A. To prevent researchers from selecting variables only after seeing interesting results
B. To guarantee statistical significance
C. To increase the number of studies
D. To remove heterogeneity

### 5. Maya compares three AI-function groups and finds different pooled estimates. What should she do before concluding that AI function is a moderator?

A. Select the group with the largest effect
B. Conduct an appropriate statistical test of the differences between groups
C. Remove the smallest group
D. Assume the difference is causal

### 6. What is a categorical moderator?

A. A moderator represented by meaningful categories
B. A moderator that must always be measured in dollars
C. A moderator with no values
D. A moderator that cannot be analyzed statistically

### 7. Which is an example of a continuous moderator?

A. AI function classified as tutoring, feedback, or assessment
B. Intervention duration measured in weeks
C. Study design classified as randomized or quasi-experimental
D. Learner level classified into categories

### 8. What statistical approach can examine the relationship between a continuous study-level moderator and effect size?

A. Meta-regression
B. Deduplication
C. Title screening
D. Risk-of-bias assessment

### 9. Maya finds that longer interventions are associated with larger effects. What should she conclude?

A. Longer interventions definitely cause larger effects
B. The study-level data show an association between duration and estimated effect size
C. Every additional week causes the same increase in learning
D. Duration is automatically the most important moderator

### 10. Why should Maya be cautious when interpreting study-level moderators?

A. Study-level associations do not necessarily describe individual-level relationships
B. Moderators can never be measured
C. Study-level data are always invalid
D. Meta-analysis cannot include moderators

### 11. Why can small moderator subgroups be challenging?

A. They may produce imprecise or unstable estimates
B. They always produce large effects
C. They cannot contain effect sizes
D. They automatically invalidate the meta-analysis

### 12. What should Maya avoid when creating moderator categories?

A. Using theoretically meaningful categories
B. Following categories prespecified in the protocol
C. Creating arbitrary categories simply to obtain interesting results
D. Reporting the number of studies in each category

### 13. What does an omnibus moderator test evaluate?

A. Whether the estimated effects differ across moderator categories
B. Whether all studies are duplicates
C. Whether the search strategy is complete
D. Whether every study has low risk of bias

### 14. Maya obtains a non-significant moderator test. What is the most appropriate interpretation?

A. The moderator has absolutely no relationship with effect size
B. The analysis did not provide sufficient evidence of a moderator association under the specified model
C. The moderator must be removed from the review
D. The meta-analysis must be repeated

### 15. What does a statistically significant moderator result establish?

A. A causal mechanism
B. An association between the moderator and variation in estimated effects under the model
C. That every study has the same effect
D. That all heterogeneity has been explained

### 16. Why should Maya avoid testing a very large number of moderators with only 22 studies?

A. The analysis may become unstable and produce chance or overfitted findings
B. More moderators always improve the model
C. It guarantees that no moderator will be significant
D. Moderators cannot be categorical

### 17. What is the difference between prespecified and exploratory moderator analyses?

A. Prespecified analyses are planned in advance, while exploratory analyses investigate questions that emerge later
B. Exploratory analyses are always more reliable
C. Prespecified analyses cannot be statistical
D. There is no difference

### 18. What should Maya do if a moderator explains only part of the heterogeneity?

A. Claim that all heterogeneity has been explained
B. Recognize that other sources of variation may remain
C. Remove all remaining studies
D. Change the research question

### 19. Which statement about meta-regression is most appropriate?

A. It can examine associations between study-level covariates and effect sizes
B. It automatically establishes causality
C. It eliminates heterogeneity
D. It can be conducted without considering the number of studies

### 20. What is the next step after examining moderators?

A. Search the databases again
B. Conduct meta-regression
C. Repeat title and abstract screening
D. Recalculate the research question

---

# Answer Key

| Question | Answer |
| -------- | ------ |
| 1        | A      |
| 2        | A      |
| 3        | A      |
| 4        | A      |
| 5        | B      |
| 6        | A      |
| 7        | B      |
| 8        | A      |
| 9        | B      |
| 10       | A      |
| 11       | A      |
| 12       | C      |
| 13       | A      |
| 14       | B      |
| 15       | B      |
| 16       | A      |
| 17       | A      |
| 18       | B      |
| 19       | A      |
| 20       | B      |

---

# Maya's Evidence Synthesis Journey

```text id="q7k2hx"
1. Identify the Research Gap
        ↓
2. Develop the Research Question
        ↓
3. Develop Search Terms From PICO/PICOS
        ↓
4. Test and Refine the Search Strategy
        ↓
5. Search the Databases
        ↓
6. Develop and Register the Protocol
        ↓
7. Download and Manage the Search Results
        ↓
8. Title and Abstract Screening
        ↓
9. Full-Text Screening
        ↓
10. Risk-of-Bias Assessment
        ↓
11. Data Extraction
        ↓
12. Decide Whether Meta-Analysis Is Appropriate
        ↓
13. Prepare the Data for Analysis
        ↓
14. Calculate Effect Sizes
        ↓
15. Conduct the Meta-Analysis
        ↓
16. Examine Heterogeneity
        ↓
17. Examine Moderators
        ↓
18. Conduct Meta-Regression
```

## Transition to Step 18

Maya has examined several potential moderators.

She now wants to answer a more complex question:

> **“What happens if I examine several study-level characteristics simultaneously?”**

Her mentor points to the analysis plan.

> **Mentor:** “That's where meta-regression comes in.”

Maya is ready for the next stage:

# Step 18 — Conduct Meta-Regression
