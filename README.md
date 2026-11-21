## 1. Student Information

- **Student ID:** 202400706
- **Chosen Phenotype:** Actin dots
- **Image Field ID:** 16819
- **Actin Image:** `16819-actin.DIB`
- **DNA Image:** `16819-DNA.DIB`

## 2. Introduction

This activity explores cell morphology and fluorescence staining patterns using the BBBC018v1 image dataset. Fiji/ImageJ was used to observe the fluorescence images and measure five selected cells. RStudio was then used to summarize the measurements, calculate descriptive statistics, and create plots to visualize cell area, circularity, and actin fluorescence intensity.

## 3. Software and Dataset

**Software used:**
- Fiji/ImageJ for image visualization and cell measurements.
- RStudio and R for data analysis and visualization.
- GitHub for organizing and presenting the project files.

**Dataset:** BBBC018v1 from the Broad Bioimage Benchmark Collection.

- [Dataset page](https://bbbc.broadinstitute.org/BBBC018)
- [Download dataset](https://data.broadinstitute.org/bbbc/BBBC018/BBBC018_v1_images.zip)

## 4. Procedure and Workflow

### Step 1. Downloading Fiji/ImageJ

Fiji/ImageJ was downloaded from the official website and prepared for image analysis. The application was launched to access the tools needed to open fluorescence images and measure cell morphology.

### Step 2. Downloading and Extracting the BBBC018 Dataset

The BBBC018v1 image dataset was downloaded and extracted. The files corresponding to image field 16819 were located for the activity.

<img width="959" height="482" alt="image" src="https://github.com/user-attachments/assets/3f25c8b0-674f-4251-88d2-69acd29bd08c" />


**Screenshot 1.** Extracted BBBC018 dataset files.

### Step 3. Opening the Selected Image in Fiji

The selected actin image, `16819-actin.DIB`, was opened in Fiji for cell morphology measurements. The DNA image (`16819-DNA.DIB`) was also used as a visual reference to locate nuclei and separate neighboring cells. The Bio-Formats Importer was used to open the image files.

<img width="958" height="538" alt="Screenshot 2026-10-28 091409" src="https://github.com/user-attachments/assets/a415907d-9e9d-401d-9c7c-25b659d6c567" />

**Screenshot 3.** Opening the selected fluorescence image in Fiji.

### Step 4. Selecting, Tracing, and Measuring Five Cells

Five identifiable cells were selected from the actin image and outlined using Fiji's selection tools. The selected regions were managed using the ROI Manager. Measurements included area, mean fluorescence intensity, circularity, and aspect ratio. The results were saved as `data/fiji_results.csv`.

<img width="955" height="539" alt="Screenshot 2026-10-28 091315" src="https://github.com/user-attachments/assets/069ccf01-3af1-48f4-9299-8edd0e812686" />

**Screenshot 4.** Selecting cells, managing ROIs, and recording measurements in Fiji.

### Step 5. Analyzing the Measurements in RStudio

The Fiji measurement data were imported into RStudio for analysis. An R script (`scripts/analyze_cells.R`) was used to calculate summary statistics and generate visualizations. The summary results were saved as `results/cell_summary.csv`.

<img width="931" height="536" alt="Screenshot 2026-10-28 091429" src="https://github.com/user-attachments/assets/d0cd70e1-2d48-49d4-9c90-0b241ec6eb23" />


**Screenshot 5.** Analyzing cell measurements using RStudio.

## 5. Results and Data Analysis

Five cells from image field 16819 were measured using Fiji/ImageJ. The measurements were analyzed in RStudio to obtain the mean values and compare the morphology and actin fluorescence intensity of the selected cells.

### Summary of Measurements

| Measurement | Mean Value |
|---|---:|
| Cell area | 132.8 pixels² |
| Circularity | 0.8528 |
| Aspect ratio | 1.1022 |
| Mean actin fluorescence intensity | 573.6164 arbitrary units |

### Figure 1. Cell Area Versus Circularity

<img width="900" height="650" alt="area_vs_circularity" src="https://github.com/user-attachments/assets/a8b5fc8c-ab82-4964-a603-69497f077e2c" />


**Interpretation:** The plot shows the relationship between the measured area and circularity of the five cells. Cell 2 had the largest area at 144 pixels², while Cell 1 had the smallest at 125 pixels². Cell 3 had the highest circularity (0.917), while Cell 4 had the lowest (0.791). These differences indicate variation in cell size and shape across the five measured cells.

### Figure 2. Actin Fluorescence Intensity

<img width="900" height="650" alt="actin_intensity" src="https://github.com/user-attachments/assets/ed78557a-123c-4f1e-acdd-1c511ee634bb" />


**Interpretation:** The plot compares the mean actin fluorescence intensity among the five selected cells. Cell 3 had the highest mean intensity (679.742 arbitrary units), whereas Cell 4 had the lowest (449.957 arbitrary units). These differences reflect variation in the measured actin fluorescence signal among the selected cell regions.

## 6. Guide Questions

### 1. Which specific phenotype did you choose, and what visible features support that choice?

I chose **Actin dots** based on visual comparison with the BBBC018 phenotype examples, observing punctate/dot-like F-actin staining features in the cells of field 16819. Because this is a visual classification from the image field rather than a verified ground-truth label, it serves as an observational categorization.

### 2. Were your five cells mostly round or elongated? Refer to your circularity and aspect-ratio results.

The five measured cells were mostly round rather than elongated. Their mean circularity was 0.8528 (closer to 1.0, indicating high roundness) and their mean aspect ratio was 1.1022 (close to 1.0, indicating minimal elongation).

### 3. What role does actin play in maintaining cell shape and in cell movement (Karp Chapter 9)?

Actin filaments help maintain cell shape by forming a supportive cytoskeletal network beneath the plasma membrane and drive cell movement through regulated actin polymerization/depolymerization and interactions with myosin motor proteins. Together, these dynamics enable cell shape remodeling, protrusions, and force generation for motility.

### 4. Why can a single fixed fluorescence image NOT show how fast a cell moves?

A single fixed fluorescence image captures cells at only one static moment after fixation and does not record displacement over time. Determining how fast a cell moves requires time-lapse measurements across multiple time points, such as in live-cell imaging.

## 7. Data Attribution

We used image set BBBC018v1 from the Broad Bioimage Benchmark Collection (Ljosa et al., Nature Methods, 2012).

Dataset: https://bbbc.broadinstitute.org/BBBC018

The BBBC018 images are distributed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 license (CC BY-NC-SA 3.0). Refer to the dataset page for the original attribution and license details.
