# Muse EEG Analysis Guide

This guide is designed for persons interested in using the Muse headband in conjunction with the Mind Monitor app to analyze EEG data for personal insights into brain activity, particularly for on going tracking to evaluate the effects of neurofeedback training and lifestyle factors. The aim is to help me preprocess my EEG data, visualize it, and extract potential biomarkers that could be indicative of various neurological conditions or states, such as ADHD or general brain health.

## Full Disclosure

I've been learning about Neurofeedback for less than a week, so don't assume for a moment I know what I'm doing with your brain. Research into the best metrics when using EEG as a diagnostic tool is ongoing, and effectivness is often mixed due to the variability in peoples brains.

Just assume I dont know what I'm doing

## Getting Started

### Equipment and App Settings

- **Device**: Muse headband
- **Application**: Mind Monitor
- **Settings**:
  - **Recording Format**: CSV
  - **Recording Interval**: Constant

### Data Collection Procedure

1. Wear the Muse headband and ensure it's properly connected to the Mind Monitor app.
2. Adjust the Mind Monitor app settings as specified above.
3. Record 5 minutes of EEG data with your eyes closed, without engaging in active meditation.
4. Save the recording to Dropbox.

### Preparing the Data for Analysis

After recording, transfer the CSV file from Dropbox to this notebook's files directory for analysis.

## Analysis Steps

### Cell 1: Setting the Data Path

```python
# Define the path to your EEG data file
data_file = 'path/to/your/eeg_data.csv'
```

### Cell 2: Data Preprocessing and Visualization

1. This step involves preprocessing the EEG data to remove dropouts, and calculates a more accurate samplerate
2. Creates a graph overview to visualize the 4 electrodes from delta to beta to get the big picture.
3. saves the graph as a png for later in the /outputs/images folder

### Cell 3: Biomarker Extraction

In this step, we extract various potential biomarkers from the EEG data, such as:

- **DAR (Delta/Alpha Ratio)**: The latest potential indicator for adult ADHD.
- **TBR (Theta/Beta Ratio)**: The most common indicator for child ADHD.

- **TAR (Theta/Alpha Ratio)**: A straight forward indicator for anxiety. most biofeedback aims to push up alpha
- **BAR (Beta/Alpha Ratio)**: A less obvious approach for anxiety, is to push down beta, which will allow more alpha as the two work together in counter to each other

- **Average PAF (Peak Alpha Frequency)**: Considered a marker for general brain health. 10hz is good. 8hz means you are old or lacking sleep

The collection of these bio markers over time should highlight what lifestyle changes or neurofeedback techniques are effective
