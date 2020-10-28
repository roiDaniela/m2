# Assignment 1

**By:**  Amit Moryossef, 207339102

---

1. Assertions:

   |              | Wikipedia | Encyclopedia |
   | ------------ | --------- | ------------ |
   | **Users**    | 75%       | 25%          |
   | **Accuracy** | 80%       | 95%          |

   - a. The expected grade of a student who uses Wikipedia is:
     $$
     E[X|Wikipedia] = (0.8 \times 10) \times 10 = 80
     $$

   - b. The probability that a randomly chosen student got 90 is:
     $$
     P(90) = 0.75 \times {10 \choose 9} \times 0.8^9 \times 0.2 + 0.25 \times {10 \choose 9}  \times 0.95^9 \times 0.05 = 0.28
     $$

   - c. Given Bob got 90, what is the probability he used Wikipedia?
     $$
     P(Wikipedia \cap 90) = 0.75 \times {10 \choose 9} \times 0.8^9 \times 0.2= 0.201 \\
     P(Wikipedia|90) = \frac{P(Wikipedia \cap 90)}{P(90)} = \frac{0.02}{0.028} = 0.717
     $$







2. Assertions: 

   - Total cupcakes: 30
   - Frosted: 10
   - Position: 15

   ​

   - a. The probability I will be the first to get a frosted cupcake is:

     Need 14 people to choose not frosted, which is:
     $$
     \frac{20}{30} \times \frac{19}{29} \times .... \times \frac{7}{17}
     $$
     Which we can use factorials for:
     $$
     P(<15 = n \cap 15 = f) =  \frac{20! \times 16!}{6! \times 30!} \times \frac{10}{16} = \frac{1}{6003} = 0.00016
     $$

   - b. The probability that all frosted cupcakes were already taken is:

     10 out of 14 chose **Frosted**, and the others had "no choice":
     $$
     P(<15 = 10f + 4n) = {14 \choose 10} \times \frac{10! \times 20!}{30!} = \frac{1}{30015} = 0.0000333
     $$

   - c. So far, 12 people got *n* and 2 got *f*, which leaves us with 8 *f* and 8 *n* 

     - i.

     $$
     E(reward) = \frac{8}{16} \times r_n + \frac{8}{16} \times r_f
     $$

     - ii. If I didn't get frosted, my expected reward is:
       $$
       E(reward)_n = \frac{8}{16} \times  r_n = 0.5 \times r_n
       $$
       If I did get *f*, it means there are 7 *f* and 8 *n* . The probability she does get frosted is:
       $$
       P(<16 = 3f + 12n \cap 30 = f) = {14 \choose 8} \times \frac{8! \times 7!}{15!} = \frac{7}{15} = 0.466
       $$
       So if I got *f*, and the last one did as well:
       $$
       E(reward)_ff = \frac{8}{16} \times \frac{7}{15} \times  r_f = \frac{7}{30} \times rf
       $$
       And if I got *f* and the last one did not:
       $$
       E(reward)_fn = \frac{8}{16} \times  (1- \frac{7}{15}) \times (2$ + r_n) = \frac{4}{15} \times(2$ + r_n)
       $$
       Making:
       $$
       E(reward) = \frac{8}{16} \times  r_n + \frac{7}{30} \times  r_f + \frac{4}{15} \times  (2$ + r_n) = 0.233 \times r_f + 0.766 \times r_n + 0.533
       $$

     - iii. I should take the deal when:

     - $$
       r_f < r_n + 2$
       $$

3. ​

   - a. We know that:

   $$
   E[X+Y] = \sum_{x \in X}{\sum_{y \in Y}{[(x+y)\times P(X=x \cap Y = y)]}} = \\
   \sum_{x \in X}{\sum_{y \in Y}{[x\times P(X=x \cap Y = y)]}} + \sum_{x \in X}{\sum_{y \in Y}{[y\times P(X=x \cap Y = y)]}} = \\
   \sum_{x \in X}{x \sum_{y \in Y}{P(X=x \cap Y = y)}} + \sum_{x \in X}{y\sum_{y \in Y}{P(X=x \cap Y = y)}} =
   $$

   ​

   ​	Now, because X and Y are independent, we can say that:
   $$
   \sum_{x \in X}P(X=x \cap Y=y) = P(Y=y) \\
   \sum_{y \in Y}P(X=x \cap Y=y) = P(X=x) \\	
   $$
   ​	We can continue:
   $$
   \sum_{x \in X}{x \times P(X=x)} + \sum_{x \in X}{y \times P(Y=y)} = E[x] + E[y]
   $$

   - b. Her expected reward from the cupcake is:
     $$
     E[Y] = \frac{10}{30} \times 2 + \frac{20}{30}\times 1 = \frac{4}{3}
     $$
     We know that the expectancy using Wikipedia is:

   $$
   E[X|Wikipedia] = (0.8 \times 10) \times 10 = 80
   $$

   ​	Assuming they are additive:
   $$
   E[X+Y] = 80 + 4/3
   $$

4. ​

  - a.
    - i.
    $$
    P(E) = P(F) = P(G) = \frac{2}{4} = 0.5 \\
    P(E \cap F) = P(E \cap G) = P(F \cap G) = \frac{1}{4} = 0.25
    $$

    $$
    P(E \cap F) = P(E \cap G) = P(F \cap G) = \\ 
    P(E) \times P(F) = P(F) \times P(G) = P(E)\times P(G) = \\
    0.5\times0.5 = 0.25
    $$

     	Every pair is independent.	

    - ii. We already showed that all of the subsets of `{E, F, G}` of size 2 are independent. Lets check size 3:

$$
P(E \cap F \cap G) = 1/4 = 0.25 \\
P(E) \times P(F) \times P(G) = 0.5 \times 0.5 \times 0.5 = 0.125 \neq P(E \cap F \cap G) = 0.25
$$

​		Therefore, the group `{E, F, G}` is not mutually independent.


  - b. 


    - i.

      - $$
        E[Y] = \frac {0 + 100} {2} = 50 \\
        E[X|Encyclopedia] =  (0.95 \times 10) \times 10 = 95 \\
        E[X\times Y] = E[X] \times E[Y] = 50\times 95 = 4750
        $$

    - ii. While `E[X]` does not change, `E[Y]` does, giving this particular student a better expectancy than 50, because 75% of the students are expected to get less than them. I can no longer use `E[X]xE[Y]`, instead I need to calculate the probability using sums.