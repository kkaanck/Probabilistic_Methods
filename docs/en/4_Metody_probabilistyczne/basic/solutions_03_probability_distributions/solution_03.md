### **Solution: Task 3 — Geometric Model (Waiting for the First Event)**

**1. Description of the random experiment**
The random experiment consists of inspecting consecutive printed pages one by one until a page with a printing error is found. Each page inspection is an independent trial with two possible outcomes: it either contains an error (probability $p$) or it does not (probability $1-p$).

**2. Sample Space $\Omega$**
Let $E$ denote a page with an error and $C$ denote a clean page (no error). The sample space $\Omega$ consists of all possible sequences of pages ending with the first error. Because the error could occur on the 1st page, the 2nd page, the 100th page, or theoretically never, the sample space is infinite.
$$\Omega = \{E, (C, E), (C, C, E), (C, C, C, E), \dots\}$$

**3. Probability distribution**
The random variable $X$ represents the number of trials (pages inspected) needed to obtain the first success (error). The probability that the first error occurs exactly on the $k$-th page means the first $k-1$ pages must be clean, and the $k$-th page must have an error.

The formula for the geometric distribution is:
$$P(X = k) = (1-p)^{k-1} \cdot p$$
*(where $k \in \{1, 2, 3, \dots\}$)*

**4. Definition of a "success"**
In this mathematical model, a "success" is defined as finding a page with a printing error. The geometric distribution is specifically used to count the number of trials needed to achieve this first "success".