# How Many Three-Digit Numbers Have an Even Digit Sum?

**Problem Statement:**  
For how many three-digit numbers (100 to 999) is the sum of the digits even? (For example, 343 has an even sum of digits: 3 + 4 + 3 = 10 which is even.) Find the answer and explain why it is correct in at least two different ways.

---

# Soultion 1 (Symmetry and the Alternating Pattern)

We define the set of all three-digit numbers:

$$
S = \{100, 101, 102, \dots, 999\}
$$

There are:

$$
999 - 100 + 1 = 900 \quad \text{total three-digit numbers}
$$

Each number has a digit sum that is either **even** or **odd**.  
If these are equally likely, we expect half to have an even sum.

### Key Insight: Changing a Digit Flips the Parity

- Incrementing a number by 1 generally flips the parity of the digit sum.
  - Example: $342$ (sum = 9, odd) → $343$ (sum = 10, even)
- The only exception is when a carry affects multiple digits (e.g., $109 \rightarrow 110$), but these disruptions occure every 10 terms of the Set and **evenly spread** across the 900 numbers.
- This creates an **alternating pattern**, and overall parity (odd/even sums) distributes evenly.

So the total number of numbers with even digit sums is:

$$
\frac{900}{2} = \boxed{450}
$$

---

The Set S (S =  {100, 101, 102, ..., 999})



# Soultion 2 (Counting with the Product Rule and Parity Cases)

Each three-digit number has three digits:  
- **Hundreds digit**: 1–9 (cannot be 0)
- **Tens digit**: 0–9
- **Ones digit**: 0–9

We classify digits by **parity**:  
- **Even digits**: $0, 2, 4, 6, 8$  
- **Odd digits**: $1, 3, 5, 7, 9$

To get an **even digit sum**, the number of odd digits must be **even**.  
That happens in the following cases:

1. Even + Even + Even  
2. Odd + Odd + Even  
3. Odd + Even + Odd  
4. Even + Odd + Odd

Let’s count how many numbers satisfy each case.

---

### Case 1: Even + Even + Even

- Hundreds digit: 4 choices ($2, 4, 6, 8$)
- Tens digit: 5 choices (even digits)
- Ones digit: 5 choices (even digits)

$$
4 \times 5 \times 5 = 100 \text{ numbers}
$$

---

### Case 2: Odd + Odd + Even

- Hundreds digit: 5 choices (odd digits)
- Tens digit: 5 choices (odd digits)
- Ones digit: 5 choices (even digits)

$$
5 \times 5 \times 5 = 125 \text{ numbers}
$$

---

### Case 3: Odd + Even + Odd

- Hundreds digit: 5 choices (odd digits)
- Tens digit: 5 choices (even digits)
- Ones digit: 5 choices (odd digits)

$$
5 \times 5 \times 5 = 125 \text{ numbers}
$$

---

### Case 4: Even + Odd + Odd

- Hundreds digit: 4 choices ($2, 4, 6, 8$)
- Tens digit: 5 choices (odd digits)
- Ones digit: 5 choices (odd digits)

$$
4 \times 5 \times 5 = 100 \text{ numbers}
$$

---

### Final Total

$$
100 + 125 + 125 + 100 = \boxed{450}
$$

---

## Final Answer:
$$
\boxed{450 \text{ three-digit numbers have an even digit sum.}}
$$

