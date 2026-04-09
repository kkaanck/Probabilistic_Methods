### **Solution: Task 4 — Poisson Model (Arrival of Events)**

**1. Description of the random experiment**
The random experiment consists of observing a system (a web service) over a continuous, fixed interval of time (one hour) and counting the total number of discrete, independent events (error reports) that occur during that interval.

**2. Sample Space $\Omega$**
The sample space $\Omega$ represents all possible total counts of error reports received in the given time interval. Because there is no theoretical upper limit to how many reports could be received, the sample space is the set of all non-negative integers.
$$\Omega = \{0, 1, 2, 3, \dots\}$$

**3. Probability distribution formula**
Let $X$ denote the random variable representing the number of error reports received in one hour. The probability of observing exactly $k$ reports follows the Poisson probability mass function. The formula is:
$$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$
*(where $k \in \{0, 1, 2, \dots\}$ and $e \approx 2.71828$)*

**4. Interpretation of the parameter $\lambda$**
The parameter $\lambda$ (lambda) represents the expected value, or the average rate of occurrences of the event within the specified continuous interval. In this specific scenario, the interval is defined as one hour, and the historical average rate is given as 3 error reports. Therefore, for a one-hour interval, the parameter is:
$$\lambda = 3$$

