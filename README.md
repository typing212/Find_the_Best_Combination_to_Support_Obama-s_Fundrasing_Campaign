# Find_the_Best_Combination_to_Support_Obama-s_Fundraising_Campaign
Multi-Armed Bandit Problem - find the best combination of "media" section and call-to-action "Button" from 24 combinations.

## Key Words
Multi-Armed Bandit Problem, E-Greedy, Adaptive E-Greedy, UCB1

## Content
This project is based on a case study of Obama’s fundraising campaign. In this project, we are required to find the best combination of “media” section and call-to-action “Button” from 24 combinations. We aim to find the one that results in the highest sign-up rate. Due to the budget limit, we are supposed to find the best combination/arm in the least amount of tries as possible less than one million. 

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

