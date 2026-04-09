### **Solution: Task 7 — Hypergeometric Model**

**1. Identification of the Model and Parameters**
This problem requires the Hypergeometric distribution because we are drawing a sample from a finite population without replacement. 

The parameters for this model are determined by the contents of the box and our sampling method:
* **$N = 15$**: Total population size (12 working + 3 defective bulbs).
* **$K = 3$**: Total number of "successes" in the population (defective bulbs).
* **$n = 5$**: The sample size drawn.
* **$k = 2$**: The target number of defective bulbs in our sample.

**2. Calculating the probability of exactly 2 defective bulbs ($P(X = 2)$)**
Let the random variable $X$ represent the number of defective bulbs in the drawn sample. The probability of obtaining exactly $k$ defective items is given by the hypergeometric formula:
$$P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$$

Substituting our specific parameters:
$$P(X = 2) = \frac{\binom{3}{2} \binom{15-3}{5-2}}{\binom{15}{5}}$$
$$P(X = 2) = \frac{\binom{3}{2} \binom{12}{3}}{\binom{15}{5}}$$

**3. Computing the Combinations**
* Ways to choose 2 defective bulbs from the 3 available: 
  $$\binom{3}{2} = 3$$
* Ways to choose the remaining 3 working bulbs from the 12 available: 
  $$\binom{12}{3} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220$$
* Total possible ways to choose any 5 bulbs from the 15 available: 
  $$\binom{15}{5} = \frac{15 \cdot 14 \cdot 13 \cdot 12 \cdot 11}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = 3003$$

**4. Final Calculation**
$$P(X = 2) = \frac{3 \cdot 220}{3003}$$
$$P(X = 2) = \frac{660}{3003} \approx 0.2198$$

There is approximately a **$21.98\%$** probability that the sample contains exactly 2 defective bulbs.

