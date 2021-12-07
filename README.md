# Asymmetric Partisan Voter Turnout Games
This is the repo for [Asymmetric Partisan Voter Turnout Games](https://link.springer.com/article/10.1007/s13235-021-00384-1) published in [Dynamic Games and Applications](https://www.springer.com/journal/13235).

---
## [Data](https://github.com/camguage/Asymmetric-Partisan-Voter-Turnout-Games/blob/master/us_pres_elec_16_cty.csv)
This dataset contains county-wide turnout rates for the 2016 U.S. election. Subsetting to the state of New York, this data contains a negative relationship between electorate size and turnout rate, consistent with the comparative statics of our model:
![Figure_13](https://user-images.githubusercontent.com/71299048/145072096-6501a759-db84-4f71-b4ef-6c63043ee9bd.jpeg)

---

## [Plotting Code](https://github.com/camguage/Asymmetric-Partisan-Voter-Turnout-Games/blob/master/Plotting%20Code.R)
This script creates plots that each contain two curve, a red one which represents voting probabilities (called *q<sub>a</sub>* for supporters of candidate *A* and *q<sub>b</sub>* for supporters of candidate *B*) for which supporters of candidate *A* would be indifferent between voting and abstaining in a given election (i.e., those two actions have the same payoff given our payoff structure), and a blue one which represents voting probabilities for which supporters of candidate *B* would be indifferent between voting and abstaining in a given election. Below is a grid of 9 such plots, varying *N*, the number of people in the election, and *p<sub>A</sub>*, the proportion of voters who support candidate *A* (while keeping the "underdog" variable *c* set to zero):
![Figure_1](https://user-images.githubusercontent.com/71299048/145077943-ee41ca34-cfd2-4dcf-b3c2-09c60af6284e.jpg)
