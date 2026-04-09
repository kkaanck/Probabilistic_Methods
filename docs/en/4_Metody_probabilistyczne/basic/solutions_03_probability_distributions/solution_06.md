### **Solution: Task 6 — Binomial Model**

**1. Identification of the Model and Parameters**
This problem requires the use of the Binomial distribution because we are evaluating a fixed number of independent trials (inspections), where each trial has exactly two possible outcomes (defective or functional), and the probability of finding a defective part remains constant.

The parameters for this model are:
* **$n = 10$**: The total number of trials (parts checked).
* **$p = 0.04$**: The probability of success on a single trial (producing a defective part).
* **$1 - p = 0.96$**: The probability of failure on a single trial (producing a functional part).

Let the random variable $X$ represent the number of defective parts found in the sample of 10. 

The general binomial formula is:
$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

**2. Calculating the probability of exactly 2 defective parts ($P(X = 2)$)**
To find the probability that exactly 2 out of the 10 parts are defective, we substitute $k = 2$ into the formula:

$$P(X = 2) = \binom{10}{2} (0.04)^2 (0.96)^{10-2}$$
$$P(X = 2) = \frac{10!}{2!(10-2)!} (0.0016) (0.96)^8$$
$$P(X = 2) = 45 \cdot 0.0016 \cdot (0.96)^8$$
$$P(X = 2) \approx 45 \cdot 0.0016 \cdot 0.7214 \approx 0.0519$$

There is approximately a $5.19\%$ chance of finding exactly 2 defective parts.

**3. Calculating the probability of at least one defective part ($P(X \ge 1)$)**
"At least one" means $X$ could be 1, 2, 3, ..., up to 10. Calculating each of these and summing them is inefficient. Instead, we use the complement rule. The opposite of "at least one" is "exactly zero". 

The sum of all probabilities in a distribution equals 1. Therefore:
$$P(X \ge 1) = 1 - P(X = 0)$$

First, calculate $P(X = 0)$:
$$P(X = 0) = \binom{10}{0} (0.04)^0 (0.96)^{10}$$
$$P(X = 0) = 1 \cdot 1 \cdot (0.96)^{10} \approx 0.6648$$

Next, apply the complement rule:
$$P(X \ge 1) = 1 - 0.6648 = 0.3352$$

There is approximately a $33.52\%$ chance of finding at least one defective part in the sample.

