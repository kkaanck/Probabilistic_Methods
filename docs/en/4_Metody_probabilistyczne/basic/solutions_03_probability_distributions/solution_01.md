# Solution

## Task 1

We are asked to analyze an experiment in which **3 consecutive screws** are inspected.
Each screw can be in one of two states:

- good,
- defective.

The probability that a screw is defective is equal to \(p\), so the probability that a screw is good is equal to \(1-p\).
We also assume:

- the inspections are **independent**,
- the probability \(p\) is the same for each inspected screw.

This is exactly the setting of a **binomial model**, because we have a fixed number of trials, two possible outcomes in each trial, and the same success probability in every trial.

---

### 1. Description of the random experiment

The random experiment consists of checking **three consecutive screws**, one after another.

For each inspected screw we record whether it is:

- defective,
- or good.

So the outcome of the experiment is not a single number at the beginning, but rather a **sequence of three observations**.

For example:

- the first screw may be good, the second defective, the third good,
- or all three may be defective,
- or all three may be good,
- and so on.

Thus the experiment is a sequence of **three Bernoulli trials**.

---

### 2. Sample space \( \Omega \)

Since each screw can be either good or defective, and we inspect 3 screws, every outcome is a sequence of length 3 built from the symbols:

- \(G\) — good,
- \(D\) — defective.

Therefore the sample space is

\[
\Omega=\{GGG,\; GGD,\; GDG,\; GDD,\; DGG,\; DGD,\; DDG,\; DDD\}.
\]

Why are there exactly 8 outcomes?

Because:

- for the first screw we have 2 possibilities,
- for the second screw we have 2 possibilities,
- for the third screw we have 2 possibilities.

Hence

\[
|\Omega|=2\cdot 2\cdot 2=2^3=8.
\]

So the sample space contains all possible sequences of good/defective results for three inspections.

---

### 3. Probabilities of the elements of the sample space

Now we determine the probability of each elementary outcome.

Because the inspections are independent, the probability of a sequence is the product of the probabilities of its components.

We use:

\[
P(D)=p, \qquad P(G)=1-p.
\]

Now we compute each probability one by one.

#### Outcome \(GGG\)

This means:

- first screw good,
- second screw good,
- third screw good.

Therefore

\[
P(GGG)=(1-p)(1-p)(1-p)=(1-p)^3.
\]

#### Outcome \(GGD\)

This means:

- first good,
- second good,
- third defective.

Hence

\[
P(GGD)=(1-p)(1-p)p=(1-p)^2p.
\]

#### Outcome \(GDG\)

\[
P(GDG)=(1-p)p(1-p)=(1-p)^2p.
\]

#### Outcome \(GDD\)

\[
P(GDD)=(1-p)pp=(1-p)p^2.
\]

#### Outcome \(DGG\)

\[
P(DGG)=p(1-p)(1-p)=p(1-p)^2.
\]

#### Outcome \(DGD\)

\[
P(DGD)=p(1-p)p=p^2(1-p).
\]

#### Outcome \(DDG\)

\[
P(DDG)=pp(1-p)=p^2(1-p).
\]

#### Outcome \(DDD\)

\[
P(DDD)=ppp=p^3.
\]

So the probabilities of all elementary outcomes are:

\[
\begin{aligned}
P(GGG)&=(1-p)^3,\\
P(GGD)&=(1-p)^2p,\\
P(GDG)&=(1-p)^2p,\\
P(GDD)&=(1-p)p^2,\\
P(DGG)&=p(1-p)^2,\\
P(DGD)&=p^2(1-p),\\
P(DDG)&=p^2(1-p),\\
P(DDD)&=p^3.
\end{aligned}
\]

Notice an important point:

Different elementary outcomes may have the same probability.
For instance, \(GGD\), \(GDG\), and \(DGG\) each contain exactly one defective screw, so each of them has probability

\[
p(1-p)^2.
\]

This observation is what later leads to the binomial distribution for the **number of defective screws**.

---

### 4. What is considered a success in this model?

In a binomial model, we must decide what counts as a **success** in each trial.

Here the natural choice is:

\[
\text{success} = \text{“the inspected screw is defective”}.
\]

Why is this the correct interpretation?

Because the problem explicitly gives the probability \(p\) for the event

\[
\text{“a screw is defective”}.
\]

So each inspection is a Bernoulli trial with:

- success = defective screw,
- failure = good screw.

Thus the random variable usually associated with the binomial model would count the **number of defective screws among the three inspected screws**.

---

### Final conclusion

The experiment consists of observing 3 independent inspections, each with two outcomes: good or defective.
The sample space is

\[
\Omega=\{GGG,\; GGD,\; GDG,\; GDD,\; DGG,\; DGD,\; DDG,\; DDD\}.
\]

Each elementary outcome has probability obtained by multiplying the factors \(p\) and \(1-p\) according to the positions of defective and good screws.

The success in this binomial model is:

\[
\boxed{\text{“a screw is defective”}}.
\]

Therefore this task is a standard example of a **binomial setting with 3 Bernoulli trials and success probability \(p\)**.
