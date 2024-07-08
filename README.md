# RNA Secondary Structure Prediction

## Project Overview

This project implements the Nussinov-Jacobson dynamic programming algorithm for predicting RNA secondary structure and compares its performance with the Mfold algorithm and experimental data.

## Authors

- Yonatan Dudai 
- Adam Lopez Muallem 
- Mayan Shachaf

## Introduction

Predicting RNA secondary structure is crucial in computational biology due to its role in cellular functions. This project focuses on:

1. Implementing the Nussinov-Jacobson algorithm
2. Comparing results with Mfold predictions
3. Evaluating accuracy against NMR-determined structures

## Methods

### Nussinov-Jacobson Algorithm Implementation

- Input sequence: 'GGCAGUACCAAGUCGCGAAAGCGAUGGCCUUGCAAAGGGUAUGGUAAUAAGCUGCC'
- Scoring system:
  - G-C: 3 points
  - A-U: 2 points
  - G-U: 1 point
- Minimum loop size: 3 bases

### Mfold Algorithm

Used for comparison, predicts structure by minimizing free energy.

### Comparative Analysis

Utilized RNAdistance from ViennaRNA package to calculate edit distances between predicted and reference structures.

## Results

- Biological reference structure (NMR experiment): (((((((((..((((((..)))))).(((((....)))))..))).....))))))
- Nussinov-Jacobson prediction: (((((((((.(.((((....))))))).((((..)).)).((...)).))..)))))
- Mfold prediction: ((((((((((.(((((....))))).(((((....))))).)))).....))))))
### Edit Distances

- Nussinov-Jacobson vs. reference: 28
- Mfold vs. reference: 8

## Discussion

The Nussinov-Jacobson algorithm, while computationally efficient (O(n^3)), showed less accuracy compared to Mfold (O(n^5)). Mfold's predictions aligned more closely with the experimental structure, highlighting the trade-off between speed and accuracy in RNA folding algorithms.

## Conclusion

While the Nussinov-Jacobson algorithm offers computational speed, Mfold provides more accurate predictions at the cost of higher computational demands. The choice between algorithms depends on specific research goals and available resources.

## Dependencies

- ViennaRNA package
- Mfold web server


## Instructor

Prof. Danny Barash
