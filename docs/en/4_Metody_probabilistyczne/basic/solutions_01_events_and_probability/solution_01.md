# Solution

## Task 1


We will use **H** for Heads and **T** for Tails.



---

# Task 1 Solution: Coin Tossing Sample Spaces

**Experiment Definition:** Tossing a fair coin where the order of outcomes matters.

### 1. One Coin Toss ($\Omega_1$)

When tossing a single coin, there is only one step, and only two possible results can occur.

**Tree Diagram:**

```text
START
 │
 ├── H (Heads)
 └── T (Tails)

```

* **Sample Space:** $\Omega_1 = \{H, T\}$
* **Number of Elementary Outcomes:** $|\Omega_1| = 2^1 = 2$

### 2. Two Coin Tosses ($\Omega_2$)

When we toss the coin a second time, each of the previous outcomes branches out into two new possibilities.

**Tree Diagram:**

```text
START
 │
 ├── H
 │   ├── H  -> (H, H)
 │   └── T  -> (H, T)
 │
 └── T
     ├── H  -> (T, H)
     └── T  -> (T, T)

```

* **Sample Space:** $\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\}$
* **Number of Elementary Outcomes:** $|\Omega_2| = 2^2 = 4$

### 3. Three Coin Tosses ($\Omega_3$)

Adding a third toss means we branch out one more time. Notice how the number of total branches doubles with each new step.

**Tree Diagram:**

```text
START
 │
 ├── H
 │   ├── H
 │   │   ├── H  -> (H, H, H)
 │   │   └── T  -> (H, H, T)
 │   └── T
 │       ├── H  -> (H, T, H)
 │       └── T  -> (H, T, T)
 │
 └── T
     ├── H
     │   ├── H  -> (T, H, H)
     │   └── T  -> (T, H, T)
     └── T
         ├── H  -> (T, T, H)
         └── T  -> (T, T, T)

```

* **Sample Space:** $\Omega_3 = \{(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$
* **Number of Elementary Outcomes:** $|\Omega_3| = 2^3 = 8$

### 4. Summary of the Number of Elementary Outcomes

Because each toss has exactly 2 possible outcomes, the total number of elementary outcomes grows exponentially.

| Experiment | Number of Tosses ($n$) | Total Outcomes ($2^n$) |
| --- | --- | --- |
| One Toss ($\Omega_1$) | 1 | $2^1 = 2$ |
| Two Tosses ($\Omega_2$) | 2 | $2^2 = 4$ |
| Three Tosses ($\Omega_3$) | 3 | $2^3 = 8$ |

### 5. What does an "Elementary Outcome" represent?

In the context of this experiment, an **elementary outcome** represents one specific, ordered sequence of coin toss results from the beginning of the experiment to the end.

For example, in the three-coin toss experiment ($\Omega_3$), the elementary outcome $(H, T, H)$ specifically means:

1. The *first* toss resulted in Heads.
2. The *second* toss resulted in Tails.
3. The *third* toss resulted in Heads.

Because the order matters, the outcome $(H, T, H)$ is an entirely different elementary outcome from $(H, H, T)$, even though both contain exactly two Heads and one Tail.

---
