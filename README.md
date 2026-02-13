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

#### Hypothesis
By determining the authenticity and integrity of text-inputs, it is possible to define modification process-independent defenses that exhibit greater generality across different modifications, contributing to maintaining correct results in face of different adversarial attacks. **Invisible textual watermarks**, when combined with deterministic reconstruction, can serve as a preventive gate that enforces request integrity *before* model execution. 

The proposed mechanism relies on three core principles:

1. **Imperceptibility**  
   The watermark does not alter the visible content or semantics of the request.

2. **Determinism**  
   The watermark can be reconstructed exactly from the visible text using shared parameters.

3. **Preventive gating**  
   Requests that fail verification are blocked before reaching the DL model.


![Preventive Defense Mechanism Approach](https://github.com/MonserratVH/Preventive_Adversarial_Mechanism/blob/main/Figures/preventive_defense_mechanism.jpg)


## Watermarking process
To protect the integrity of inputs, the watermarking process embeds a watermark to input on a hierarchical scheme at sentence and term level applying hash tables and hash functions using a particular key for this process.

#### Hashing Sentence
![Watermarking at Sentence Level](https://github.com/MonserratVH/Preventive_Adversarial_Mechanism/blob/main/Figures/watermark_sentence_level.jpg)


#### Hashing Term 
![Watermarking at Term Level](https://github.com/MonserratVH/Preventive_Adversarial_Mechanism/blob/main/Figures/watermark_term_level.jpg)


#### Repository Structure

```text
.
├── Figures
├── Preventive_Defense_Mechanism.ipynb  # Preventive Defense Mechanism Against Adversarial Attacks Based on Structural Watermarking
├── README.md             # Project documentation

```

---


## Researchers

- _Monserrat Vázquez-Hernández_  
    mvazquez@inaoe.mx  
    https://orcid.org/0000-0001-9206-5706  

- _Luis Alberto Morales-Rosales_  
    lamorales@conacyt.mx  
    [[https://orcid.org/0000-0002-4753-9375](https://orcid.org/0000-0002-4753-9375)
  
- _Ignacio Algredo-Badillo_  
    algredobadillo@inaoep.mx  
    https://orcid.org/0000-0002-4748-3500

- _Luis Villaseñor-Pineda_  
    villasen@inaoep.mx  
    https://orcid.org/0000-0003-1294-9128


## Acknowledgements

 - This work is supported by CONAHCYT/México scholarship 814461. Besides, it was founded by Catedras-CONAHCYT projects 882 and 613


