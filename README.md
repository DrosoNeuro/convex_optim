## Convex optimisation and applications

The following problem was inspired by power and sample size calculations used in Neyman-Pearson hypothesis testing and Null Hypothesis Significance Testing, respectively.The problem was in general inspired by personal experiences in wet-lab environments as well as by the following two publications:http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0032734 and https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4347431/ 

In many areas of research, different variants of hypothesis testing are applied to make inference about empirical data. Two of these approaches are the Neyman-Pearson framework and the Null Hypothesis Significance Testing (NHST) framework<sup>1</sup>, both of which compare the likelihood of two competing hypotheses with the goal to minimise the error conducted. Typically, one distinguishes between Type I and Type II errore, which describe the chance of *falsely rejecting* a *true* *Null* Hypothesis (false positive) and the chance of *falsely rejecting* a *true* *alternative* hypothesis (false negative), respectively.

In the Neyman Pearson framework, the maximally acceptable errors are fixed beforehand, while in the NSHT framework, they can be fixed both before and after the data collection. In both cases, however, deciding which threshold values to use is not based on any scientific or statistical theoretical rules, but rather are defined by custom rules. 

Ideally, researchers can use a large sample size to decrease both their Type I and Type II errors.However, in a setting like animal research, large sample sizes can be considered as problematic due to animal ethics concerns. On the other hand, experiments with large Type I or Type II errors diminish the trustworthiness of the respective research results and increase the risk of non-reproducibility, which is ethically problematic as well since it hampers translation and might have potentially dangerous effects for human subjects in clinical trials.

## Description of the problem (rough)

In pre-clinical and clinical trials, power analyses are routinely applied to calculate the optimal amount of test subjects needed. The goal is to minimise the number of test subjects while at the same time minimising the probabilities of Type I and Type II errors

min N = $$(\sigma^2 * (z_{\alpha}+z_{\beta})^2) / (\tau)$$

Randomisation examples: 
- sex
- age
- place of living
- socio-economic status
- behavioural factors
etc.


min amount of subjects
N = 2

<sup>1</sup>Please not that NHST is theoretically problematic amalgamation of the Neyman-Pearason hypothesis testing framework and the Fisher hypothesis framework.It is advised to refrain from using NHST in the first place, since it often leads to inconsistent and scientifically invalid inferences. However, NHST is the predominantly used method in many areas of science, hence it is included in this analysis.

s.t. 
power >= x
typeI error rate <= y
effect >= z

maleA - maleB = 0
femaleA - femaleB = 0
etc.

