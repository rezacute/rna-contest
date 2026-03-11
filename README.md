# Stanford RNA 3D Folding Challenge Part 2

## Competition Description

RNA is essential to life's core functions, but predicting its 3D structure remains difficult. Unlike proteins, where models like AlphaFold have made major progress, RNA modeling is still held back by limited data and the complexity of RNA folding.

This is the second Stanford RNA 3D Folding Challenge. The first marked a major milestone, where fully automated models matched human experts for the first time. Now, you'll face even more complex targets, including ones with no structural templates, and a new evaluation metric designed to reward greater accuracy.

## Timeline

- Competition runs ~2 months
- Ends before CASP17 (April 2026)

## Goal

Predict RNA 3D structure from sequence data.

## Evaluation

**TM-score** (Template Modeling Score): 0.0 to 1.0 (higher is better)

- Measures similarity between predicted and experimental 3D structures
- For each test RNA sequence, submit 5 predictions
- Final score = average of best-of-5 TM-scores across all targets
- Some targets have multiple reference structures (score based on best match)

## Submission Format

CSV with columns:
```
ID,resname,resid,x_1,y_1,z_1,...x_5,y_5,z_5
R1107_1,G,1,-7.561,9.392,9.361,... -7.301,9.023,8.932
R1107_2,G,1,-8.02,11.014,14.606,... -7.953,10.02,12.127
```

- Submit C1' atom coordinates for each residue
- 5 structure predictions per sequence
- Use US-align for rotation/translation alignment

## Links

- [Competition Page](https://www.kaggle.com/competitions/stanford-rna-3d-folding-2)
- [CASP17](https://predictioncenter.org/)

## Approach Ideas

1. **Deep Learning**: Use transformer/attention models on RNA sequences
2. **AlphaFold-inspired**: Adapt protein structure prediction methods
3. **Graph Neural Networks**: Model RNA as graphs
4. **Quantum ML**: Explore quantum approaches for molecular structure prediction

## Files

```
.
├── README.md
├── data/           # Competition data (when downloaded)
├── notebooks/      # Analysis notebooks
├── src/            # Source code
└── models/         # Trained models
```
