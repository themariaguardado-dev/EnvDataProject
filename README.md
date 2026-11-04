# Plant Projected Area from RGB Photographs

Final project for OEAS 805.

## Project objective

This project explores methods for separating plant tissue from the
background in RGB photographs of Susquehanna Flats milfoil. The goal
is to estimate total projected plant area and its vertical distribution.

These measurements represent projected area. Interpreting them as
biomass would require an additional area-to-biomass relationship.

## Current progress

The exploratory notebook examines:

- Plant representation in the morphology measurements.
- Image availability and matches with calibration metadata.
- Physical image resolution.
- Red, green, and blue brightness distributions.

The next steps are to crop or mask unnecessary image regions while
retaining all plant tissue and its immediate surroundings, compare
plant, background, and shadow pixels, and evaluate segmentation methods.

## Project organization

| Location | Contents |
| --- | --- |
| CODE/eda_plantarea.ipynb | Exploratory analysis notebook |
| DATA/raw/ | Original metadata and morphology spreadsheets |
| DATA/raw/GoProImages/ | Local photograph dataset; stored separately from GitHub |
| DATA/cleaned/ | Reserved for processed data |
| DATA/results/ | Reserved for analysis outputs |

## Photograph access

The complete photograph dataset contains 262 files totaling approximately
19.7 GB and is stored separately from this repository.

A dataset access link will be added here when available.

To run the image analysis, place the photographs in
DATA/raw/GoProImages/ or update the notebook to use their local location.

## Running the notebook

The notebook uses Python with Jupyter, NumPy, pandas, Matplotlib,
Pillow, and openpyxl for reading Excel files.

Before running the notebook, update the image and spreadsheet paths
to match your computer. Run the cells in order.

Interactive polygon cropping requires a working Matplotlib Qt backend.