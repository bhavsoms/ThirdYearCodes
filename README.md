
**Statistical Tests and Text Data Processing Theory**

This file provides theoretical foundations for the statistical tests and text data processing techniques covered in the code examples.

**1. Statistical Tests**

**1.1. One-Way ANOVA:**

* **Purpose:** Compares means of three or more independent groups to assess if there's a statistically significant difference between them.
* **Assumptions:** Independent samples, normality of data within each group, homogeneity of variances (equal variances).
* **H null hypothesis:** The means of all groups are equal.
* **H alternative hypothesis:** At least one pair of means is different.
* **Test statistic:** F-statistic, measures the ratio of variances between groups and within groups.
* **Rejection criteria:** If the p-value (probability of observing the F-statistic by chance, assuming H0 is true) is less than a significance level (e.g., 0.05), we reject the null hypothesis and conclude significant differences.

**1.2. Two-Way ANOVA:**

* **Purpose:** Similar to one-way ANOVA, but compares means across two independent factors with multiple levels simultaneously.
* **Assumptions:** Independent samples, normality of data within each subgroup, homogeneity of variances across subgroups.
* **H null hypothesis:** There's no interaction effect between the factors (no additional effect on the dependent variable beyond the main effects of each factor).
* **H alternative hypothesis:** There's an interaction effect between the factors.
* **Test statistic:** F-statistic calculated for both main effects and interaction effect.
* **Rejection criteria:** Similar to one-way ANOVA, p-values less than the significance level indicate a significant difference.

**1.3. T-Test:**

**1.3.1 Independent Samples T-Test:**

* **Purpose:** Compares the means of two independent groups to determine if there's a statistically significant difference.
* **Assumptions:** Independent samples, normality of data in both groups, homogeneity of variances.
* **H null hypothesis:** The means of the two groups are equal.
* **H alternative hypothesis:** The means are different.
* **Test statistic:** T-statistic, measures the difference between the means relative to the pooled standard deviation.
* **Rejection criteria:** Similar to one-way ANOVA.

**1.3.2 Paired Samples T-Test:**

* **Purpose:** Compares means from the same subjects or groups measured before and after a treatment or under different conditions.
* **Assumptions:** Normality of differences (differences between paired samples), independence of errors (no correlation between the differences for each paired sample).
* **H null hypothesis:** The mean difference between pairs is zero.
* **H alternative hypothesis:** The mean difference is not zero.
* **Test statistic:** T-statistic calculated using the differences between paired samples.
* **Rejection criteria:** Similar to one-way ANOVA.

**2. Text Data Processing**

**2.1. Text Preprocessing:**

* **Purpose:** Prepares text data for further analysis by cleaning and transforming it into a suitable format for algorithms.
* **Common techniques:**
    * **Lowercasing:** Converting all text to lowercase for case-insensitive processing.
    * **Punctuation removal:** Removing punctuation marks (e.g., commas, periods) except when part of words (e.g., "won't").
    * **Stopword removal:** Removing common words with little semantic meaning (e.g., "the", "a", "is").
    * **Frequent/Rare word removal:** Removing words that appear too often or too rarely in the corpus, potentially indicating noise or irrelevant terms.
    * **Stemming:** Reducing words to their base forms (e.g., "running" to "run").
    * **Lemmatization:** Reducing words to their dictionary form, considering parts of speech (e.g., "better" to "good").

**2.2. Declarative vs. Imperative Programming:**

* **Declarative programming:** Focuses on "what" needs to be done, leaving the "how" (specific implementation details) to the underlying system. This often makes code more readable and maintainable.
* **Imperative programming:** Explicitly specifies step-by-step instructions on "how" to perform tasks.

**3. Visualization Libraries**

**3.1. CanvasJS.Chart:**

* A JavaScript library for creating interactive charts (line, column, pie, bar, etc.)
* Offers customization options for appearance and interactivity.

**3.2. HTML5 Canvas:**

* A browser API for drawing graphics and animations directly on a web page.
* Requires writing JavaScript code to define