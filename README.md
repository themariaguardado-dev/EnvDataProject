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
| DATA/raw/GoProImages_Susquehanna_Milfoil/ | 25 photographs referenced in the morphology spreadsheet |
| DATA/cleaned/ | Reserved for processed data |
| DATA/results/ | Reserved for analysis outputs |

## Photographs

The repository includes 25 unique photographs referenced in the
REFERENCE and BRANCH columns of the morphology spreadsheet.
These images total approximately 87.4 MB and are located in:

DATA/raw/GoProImages_Susquehanna_Milfoil/

Original filenames and image resolution are preserved.

Before running the notebook, update its image-folder path to this
location and its spreadsheet paths to the files in DATA/raw/.

## Running the notebook

The notebook uses Python with Jupyter, NumPy, pandas, Matplotlib,
Pillow, and openpyxl for reading Excel files.

Before running the notebook, update the image and spreadsheet paths
to match your computer. Run the cells in order.

Interactive polygon cropping requires a working Matplotlib Qt backend.