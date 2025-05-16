# H&E Stain Normalization and Separation

This repository provides a Python implementation for normalizing the color appearance of H&E-stained histopathological images and separating them into their Hematoxylin and Eosin components.

🔗 **Demo Video**: [Watch here](https://youtu.be/tNfcvgPKgyU)  
🎥 **Intro to H&E Stains**: [Watch explanation](https://youtu.be/yUrwEYgZUsA)

---


## 📘 Description

Stain variability across labs and equipment can negatively impact digital pathology analyses. This code standardizes staining and separates key components, enhancing consistency for downstream image processing tasks.

The workflow is adapted from:
- **Macenko et al.**, ISBI 2009: [Link to paper](http://wwwx.cs.unc.edu/~mn/sites/default/files/macenko2009.pdf)
- **Vink et al.**, J Microscopy 2013

Original MATLAB implementation:  
[GitHub - mitkovetta/staining-normalization](https://github.com/mitkovetta/staining-normalization/blob/master/normalizeStaining.m)

Additional references:
- [PMC Article](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5226799/)
- [PLOS ONE Article](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0169875)

---

## 🔬 Method Overview

**Input**: RGB image of H&E-stained tissue  
**Output**:  
- Color-normalized image  
- Hematoxylin-only image  
- Eosin-only image

### Steps:
1. Convert image to Optical Density (OD) space
2. Remove pixels below OD threshold (transparent regions)
3. Perform SVD on filtered OD values
4. Identify stain vectors from dominant directions
5. Normalize stain intensities
6. Separate Hematoxylin and Eosin components
7. Reconstruct normalized image using standard stain profiles

---

## 💻 Requirements

- Python 3.x
- numpy
- opencv-python
- matplotlib


