# Plant Projected Area from RGB Photographs

Final project for OEAS 805.

## Project objective

This project explores methods for separating plant tissue from the
background in RGB photographs of Susquehanna Flats milfoil. The goal
is to estimate total projected plant area and its vertical distribution.

These measurements represent projected area. Interpreting them as
biomass would require an additional area-to-biomass relationship.


## Data Provenance

The photographs and supporting metadata were collected during field and laboratory work in the summer of 2026. Nine shoots were collected, with the current analysis focusing on five branches of a single shoot (IDX 3).

Photograph-specific spatial calibration factors were previously calculated in MATLAB using blue circular standards of known diameters.

## Project organization

| Location | Contents |
| --- | --- |
| CODE/eda_4_peerreview.ipynb | Primary notebook for peer review |
| CODE/ | Additional exploratory notebooks |
| DATA/raw/ | Original metadata and morphology spreadsheets |
| DATA/raw/GoProImages_Susquehanna_Milfoil/ | Original GoPro photographs |
| DATA/results/vertical_area/ | Previously calculated area distributions for five branches of IDX 3 |


## Photographs

The repository includes 25 unique photographs referenced in the
REFERENCE and BRANCH columns of the morphology spreadsheet.
These images total approximately 87.4 MB and are located in:

DATA/raw/GoProImages_Susquehanna_Milfoil/

Original filenames and image resolution are preserved.

Before running the notebook, update its image-folder path to this
location and its spreadsheet paths to the files in DATA/raw/.

## Required Python Packages

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- SciPy
- OpenPyXL
- Tkinter

The notebook requires a local Jupyter environment supporting the interactive Matplotlib Tk backend.

Before running the notebook, update the image and spreadsheet paths
to match your computer. Run the cells in order.

# Instructions for Lu

1. Download or clone this repository.
2. Open `CODE/eda_4_peerreview.ipynb`.
3. Update the file and folder paths in the notebook to match their locations on your computer.
4. Run the notebook cells sequentially.
5. Follow the interactive instructions for polygon cropping, plant cluster selection, and stem tracing.
6. Update the path to `DATA/results/vertical_area/` when prompted to load the previously processed branch distributions.

Because portions of the workflow involve manual selections, your results may differ slightly from the saved notebook outputs.

## Analytical Workflow

1. Photograph cropping.
2. Unsupervised K-means classification.
3. Projected plant area estimation.
4. Manual stem tracing.
5. Assignment of plant pixels to axial distance intervals.
6. Gaussian fitting and evaluation.
7. Comparison of area distributions among five branches.

## Limitations and Future Work

The calculated distributions represent projected plant area along plant axes rather than actual vertical height or biomass.

The current analysis serves as a proof of concept. Future work will apply the methodology to the remaining eight shoots to characterize variability among individuals.