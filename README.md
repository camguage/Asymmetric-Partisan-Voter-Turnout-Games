# Asymmetric Partisan Voter Turnout Games
This is the repo for [Asymmetric Partisan Voter Turnout Games](https://link.springer.com/article/10.1007/s13235-021-00384-1), published in [Dynamic Games and Applications](https://www.springer.com/journal/13235).

---
## [Data](https://github.com/camguage/Asymmetric-Partisan-Voter-Turnout-Games/blob/master/us_pres_elec_16_cty.csv)
This dataset contains county-wide turnout data for the 2016 U.S. persidential election. Subsetting to the state of New York, we see a negative relationship between electorate size and turnout rate, consistent with the comparative statics of our model:
![Figure_13](https://user-images.githubusercontent.com/71299048/145072096-6501a759-db84-4f71-b4ef-6c63043ee9bd.jpeg)

---

## [Plotting Code](https://github.com/camguage/Asymmetric-Partisan-Voter-Turnout-Games/blob/master/Plotting%20Code.R)
This script creates plots that each contain two curves, a red one which represents voting probabilities (called *q<sub>a</sub>* for supporters of candidate *A* and *q<sub>b</sub>* for supporters of candidate *B*) for which supporters of candidate *A* would be indifferent between voting and abstaining in a given election (i.e., those two actions have the same payoff given our payoff structure), and a blue one which represents voting probabilities for which supporters of candidate *B* would be indifferent between voting and abstaining in a given election. Below is a grid of 9 such plots, varying *N*, the number of people in the election, and *p<sub>A</sub>*, the proportion of voters who support candidate *A* (while keeping the "underdog" variable *c* set to zero):
![Figure_1](https://user-images.githubusercontent.com/71299048/145077943-ee41ca34-cfd2-4dcf-b3c2-09c60af6284e.jpg)
The code works as follows. It first defines three functions: `A_wins`, `B_wins`, and `tie`. Each has four arguments: `n` is number of people in our hypothetical electorate, `pa` is the proportion of that electorate which supports candidate *A* (with `pb` defined as `1-pa`), `qa` is the probability that a supporter of candidate *A* will vote, and `qb` is the probability that a supporter of candidate *B* will vote. `A_wins` simply calculates the probability that candidate *A* wins the election given the four arguments, `B_wins` calculates the probability that candidate *B* wins the election given the arguments, and `tie` calculates the probability of a tie given the arguments.

Finally, I create two plotting functions (`plotting_function_1` and `plotting_function_2`), which take as arguments two sequences of voting probabilities (`qa` and `qb`). Once `n`, `pa`, and `c` are defined inside the functions, each one calculates the expected payoff for supporters of candidate *A* and candidate *B* respectively of voting. I then plot the curve on the `qa`-`qb` axis along which the expected payoff of voting is zero (i.e., the supporter is indifferent between voting and abstaining) in red for supporters of candidate *A* and in blue for supporters of candidate *B*.
