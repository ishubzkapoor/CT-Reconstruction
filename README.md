# CT Reconstruction: Sinogram Generation and Backprojection

This project demonstrates the basic idea behind **Computed Tomography (CT) image reconstruction** using a 2D phantom image.  
The goal is to show how projection data is generated from different viewing angles and how the original image can be reconstructed using backprojection.

## Project Overview

In CT imaging, an object is scanned from multiple angles.  
For each angle, the object is projected onto a detector, producing one column of a **sinogram**.  
By collecting many projections, we can reconstruct an approximation of the original object.

This project visualizes two important steps:

1. **Sinogram Generation**
2. **Backprojection Reconstruction**

---

## 1. Sinogram Generation

The phantom image is rotated step by step.  
For each rotation angle, the pixel intensities are summed along one direction to create a projection.

These projections are stacked together to form the sinogram.

![Sinogram generation](assets/sinogram_generation.gif)

The sinogram shows how object structures move across the detector as the scanning angle changes.

---

## 2. Backprojection Reconstruction

Backprojection takes each projection from the sinogram and spreads it back across the image plane at the corresponding angle.

As more projections are accumulated, the reconstructed image gradually becomes closer to the original phantom.

![Backprojection reconstruction](assets/better_backprojection_animation.gif)

This demonstrates the core reconstruction idea used in CT imaging.

---

## Key Concepts

- **Phantom Image**: A synthetic test image used to simulate a scanned object.
- **Projection**: A 1D measurement obtained by summing image intensities along one direction.
- **Sinogram**: A 2D representation of projections collected over many angles.
- **Backprojection**: A reconstruction method that maps projection data back into image space.
- **Filtered Backprojection**: An improved method that applies filtering before backprojection to reduce blurring.

---

## Applicability to Real World Scenario

- Shows the mathematical basis of CT reconstruction visually.
- Connects image processing with real-world medical and industrial imaging systems.
- Helps understand how raw projection data can be transformed into a reconstructed image.

---

## Technologies Used

- Python
- NumPy
- Matplotlib
- scikit-image
- Jupyter Notebook

---

## Applications

This concept is used in:

- Medical CT scanners
- Industrial non-destructive testing
- X-ray inspection systems
- Radar and microwave imaging
- SAR/GPR backprojection-based imaging

---

## How to Run

Install the required Python libraries:

```bash
pip install numpy matplotlib scikit-image
