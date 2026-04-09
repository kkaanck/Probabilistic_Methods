### **Solution: Task 9 — Poisson Model**

**1. Identification of the Model and Parameters**
This problem utilizes the Poisson distribution because we are evaluating the number of discrete events (customer service requests) occurring within a fixed, continuous interval of time (one hour).

The single parameter for this model is the average rate of occurrence:
* **$\lambda = 5$**: The expected number of requests per hour.

Let the random variable $X$ represent the exact number of requests received in one hour. The probability of receiving exactly $k$ requests is given by the Poisson probability mass function:
$$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$

**2. Calculating the probability of exactly 3 requests ($P(X = 3)$)**
To find the probability that exactly 3 requests are received in one hour, substitute $k = 3$ and $\lambda = 5$ into the formula:
$$P(X = 3) = \frac{5^3 e^{-5}}{3!}$$
$$P(X = 3) = \frac{125 \cdot e^{-5}}{3 \cdot 2 \cdot 1}$$
$$P(X = 3) \approx \frac{125 \cdot 0.006738}{6}$$
$$P(X = 3) \approx 0.1404$$

There is approximately a **$14.04\%$** probability of receiving exactly 3 requests in a given hour.

**3. Calculating the probability of at least one request ($P(X \ge 1)$)**
The event "at least one request" is the complement of receiving "exactly zero requests." Using the complement rule simplifies the calculation significantly:
$$P(X \ge 1) = 1 - P(X = 0)$$

First, compute the probability of receiving 0 requests:
$$P(X = 0) = \frac{5^0 e^{-5}}{0!}$$
$$P(X = 0) = \frac{1 \cdot e^{-5}}{1} \approx 0.006738$$

Apply the complement rule:
$$P(X \ge 1) = 1 - 0.006738 = 0.993262$$

There is approximately a **$99.33\%$** probability of receiving at least one request during the hour.

