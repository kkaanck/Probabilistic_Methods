### **Solution: Task 2 — Hypergeometric Model (Sampling from a Batch)**

**1. Description of the random experiment**
The random experiment consists of selecting a sample of exactly 4 components from a finite population of 20 components (15 functional and 5 defective). The selection is conducted *without replacement*, meaning each drawn component alters the probability of subsequent draws.

**2. Definition of the random variable $X$**
The random variable $X$ represents the exact number of defective components contained within the drawn sample of 4 components.

**3. Possible values of $X$**
Because the sample size is 4 and there are 5 defective components available in the population, it is possible to draw anywhere from 0 to 4 defective components. Therefore, the possible values for the random variable $X$ are:
$$X \in \{0, 1, 2, 3, 4\}$$

**4. Probability distribution**
The probability of obtaining exactly $k$ defective components follows the hypergeometric distribution. It is calculated by dividing the number of ways to choose $k$ defective components and $4-k$ functional components by the total number of ways to choose any 4 components from the 20 available.

The general formula is:
$$P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$$

Substituting the specific parameters of this model ($N = 20$, $K = 5$, $n = 4$):
$$P(X = k) = \frac{\binom{5}{k} \binom{15}{4-k}}{\binom{20}{4}}$$
*(where $k \in \{0, 1, 2, 3, 4\}$)*

**5. Definition of a "success"**
In this mathematical model, a "success" is defined as selecting a defective component. This aligns with the random variable $X$, which is specifically designed to count the occurrences of defective elements in the sample.

