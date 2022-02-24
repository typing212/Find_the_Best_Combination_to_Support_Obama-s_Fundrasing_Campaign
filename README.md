# Find_-the-_Best_Combination_to_Support_Obama-s_Fundrasing_Campaign
Multi-Armed Bandit Problem - find the best combination of "media" section and call-to-action "Button" from 24 combinations.

## Key Words
Multi-Armed Bandit Problem, E-Greedy, Adaptive E-Greedy, UCB1

## Content
The multi-armed bandit problem is used in reinforcement learning. In this problem, an arm is chosen from 24 different combinations/arms and upon “pull” the arm, the learner receives a reward based on an invisible distribution of that arm. Through the algorithm designed, the best arm is identified and we will keep pulling this arm to get maximum expectation of the net rewards.

## Insights
Among those three methods, adaptive e-greedy has the most randomness in finding the best arm and UCB has the least.

If we use the same algorithm to solve the same multi-armed bandit problem for several times, it is very likely for adaptive e-greedy to gain different results on which one is the best arm. The reason is the correlation between the result and the arm selected in the first few rounds. At the beginning, the probabilities of choosing each arm are very similar. However, with the increase of times of pulls, the probability of choosing the current best arm is increasing. It means that if we get stuck at a locally best arm, the probability of correcting the mistake is getting lower and lower.

But, for e-greedy, since the e is constant, the probability of correcting the mistake is small but won’t change. In addition, by setting a higher, we could get higher chance to detect the globally best arm rather than the local best arm, which unfortunately may cause some loss.

For UCB, it plays each arm once at beginning, which eliminate the uncertainty of choosing in the first few rounds. In the following process, the index is related to the average rewards of each arm. That means not only the highest average reward but also the others are all been considered when making decisions. Therefore, in most cases, UCB always finds the same best arm.

## Collaborators
Ke Ma

Mingzhe Xu

Nanhai Zhong

Xiao Liang

