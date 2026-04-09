### **Solution: Task 5 — Multinomial Model (Categories of Outcomes)**

**1. Description of the random experiment**
The random experiment consists of rolling a standard six-sided die exactly 5 independent times. The outcome of each individual roll is observed and classified into one of three mutually exclusive categories: small numbers (1 or 2), medium numbers (3 or 4), or large numbers (5 or 6).

**2. Sample Space $\Omega$**
Let $S$ denote a small number, $M$ a medium number, and $L$ a large number. The sample space $\Omega$ consists of all possible sequences of length 5 composed of these three categorical outcomes. 
$$\Omega = \{(x_1, x_2, x_3, x_4, x_5) \mid x_i \in \{S, M, L\}\}$$
*(Since there are 3 possible categories for each of the 5 rolls, the sample space contains $3^5 = 243$ unique sequences).*

**3. Multinomial distribution**
Let $X_1, X_2,$ and $X_3$ be random variables representing the total count of small, medium, and large outcomes, respectively. The probability of observing exactly $k_1$ small, $k_2$ medium, and $k_3$ large numbers follows the multinomial distribution formula:
$$P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{n!}{k_1! k_2! k_3!} p_1^{k_1} p_2^{k_2} p_3^{k_3}$$

Substituting the specific parameters of this experiment ($n=5$, and $p_1 = p_2 = p_3 = \frac{1}{3}$):
$$P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{5!}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^{k_1} \left(\frac{1}{3}\right)^{k_2} \left(\frac{1}{3}\right)^{k_3} = \frac{120}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^5$$
*(where $k_1 + k_2 + k_3 = 5$ and $k_i \ge 0$)*

**4. Interpretation of the parameters**
* **$n = 5$**: The total number of independent trials (die rolls).
* **$p_1, p_2, p_3 = \frac{1}{3}$**: The probability of a single trial resulting in category 1, 2, or 3, respectively. Because each category contains exactly 2 out of the 6 possible die faces, the probability for each is $\frac{2}{6} = \frac{1}{3}$.
* **$k_1, k_2, k_3$**: The specific number of times each categorical outcome is observed across the 5 trials.

