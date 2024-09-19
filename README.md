# README

## Project Overview

This repository contains Python code for converting CSV files with "Energy" (x-axis) and "Peak/Baseline Ratio" (y-axis) data into visualizations, including:
1. Line Plot
2. Violin Plot
3. Ridgeline Plot and its First and Second Derivatives

The data is sourced from INS spectra for organic semiconductor samples, where processing the data helps identify defined peaks in amorphous samples. This analysis can be valuable for researchers working on material characterization of organic semiconductors.

---

## Requirements

The code requires the following Python libraries:
- `pandas`
- `matplotlib`
- `seaborn`
- `numpy`
- `os`

You can install the necessary dependencies using:

pip install pandas matplotlib seaborn numpy

---

## Usage

### Data Format

The input data should be in CSV format, with each file containing at least two columns:
1. Energy - x-axis values
2. Peak/Baseline Ratio - y-axis values

### File Paths and Labels

- `data_sets`: List of file paths to your CSV files.
- `labels`: Descriptive names for each dataset, used for plot legends.
- `save_path`: The directory to save the plots.

---

### 1. Line Plot: Peak to Baseline Ratios

This script generates a line plot of Peak/Baseline Ratios vs. Energy for different datasets.

#### Code Example:

```
# Define the file paths and labels
data_sets = [r'/path/to/file1.csv', r'/path/to/file2.csv']
labels = ['Dataset 1', 'Dataset 2']
save_path = r'/path/to/save/line_plot.pdf'
```

Run the script to generate the line plot and save it as a PDF.

---

### 2. Violin Plot: Distribution of Ratios

The violin plot shows the distribution of Peak/Baseline Ratios for each dataset.

#### Code Example:

```
# Define the file paths and labels
data_sets = [r'/path/to/file1.csv', r'/path/to/file2.csv']
labels = ['Dataset 1', 'Dataset 2']
save_path = r'/path/to/save/violin_plot.pdf'
create_violin_plot(data_sets, labels, save_path)
```

---

### 3. Ridgeline Plot with First and Second Derivatives

This script generates a ridgeline plot of the KDE for Peak/Baseline Ratios and their first and second derivatives, giving insights into the distribution and inflection points of the data.

#### Code Example:

```
# Define the directory containing CSV files
csv_dir = r'/path/to/csv_files/'
save_path = r'/path/to/save/plots/'

plot_ridgeline(csv_files, labels, save_path)
```

---

## Customization

- **Colors**: Customize plot colors by modifying the `custom_colors` list in the script.
- **Plot Limits**: Adjust the x-axis limits and other styling features directly in the plotting functions.

---

## Contact

For questions or contributions, feel free to open an issue or submit a pull request!

