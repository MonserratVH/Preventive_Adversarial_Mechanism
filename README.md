# Preventive Defense Mechanism Against Adversarial Attacks Based on Structural Watermarking

#### Actual Defenses
Existing methods for generating adversarial examples for text applications have shown that models can be fooled by modifying their inputs at character, term, or sentence level, using strategies such as adding, deleting, substituting, or swapping parts of the text. Actual adversarial defenses use current input modification knowledge to define a set of possible modifications that model inputs can have, and thus incorporate processes to identify them and minimize their impact on model results.

![Adversarial Defense Approaches](https://github.com/MonserratVH/Preventive_Adversarial_Mechanism/blob/main/Figures/adversarial_defense_approaches.jpg)



#### Problem 
Although existing defenses have contributed to maintaining correct model results, they depend on modification process knowledge. The dependence on modification knowledge results in a reduction of generality and a decrease in their effectiveness to maintain model results.

In face of adversarial examples, the key factor for an effective defense is generality, because it is not possible to cover all possible modifications given that new vulnerabilities are constantly being discovered. Therefore, we consider that adversarial defenses should be more general, and in contrast to current defenses, establish a validation process to validate the authenticity and integrity of the inputs before they are processed by the model

## Proposal
#### Preventive Defense Mechanism
We propose a two-step preventive defense mechanism to achieve an attack-independent defense. The preventive defense scheme include two principal process: 1) a watermarking process to include a mark to inputs model and 2) an input validation process to validate that inputs contain the marked input characteristics before they are processed by the model.

####H Hypothesis

By determining the authenticity and integrity of text-inputs, it is possible to define modification process-independent defenses that exhibit greater generality across different modifications, contributing to maintaining correct results in face of different adversarial attacks.
