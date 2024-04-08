# Muse EEG Analysis Guide

This guide is designed for individuals using the Muse headband in conjunction with the Mind Monitor app to analyze EEG data for personal insights into brain activity. The aim is to help users preprocess their EEG data, visualize it, and extract potential biomarkers that could be indicative of various neurological conditions or states, such as ADHD or general brain health.

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

This step involves preprocessing the EEG data to remove noise and artifacts, followed by creating a graph overview to visualize the data trends and patterns.

### Cell 3: Biomarker Extraction

In this step, we extract various potential biomarkers from the EEG data, such as:

- **DAR (Delta/Alpha Ratio)**: Used as a potential indicator for adult ADHD.
- **Average PAF (Peak Alpha Frequency)**: Considered a marker for general brain health.

The extraction of these biomarkers can provide insights into the individual's neurological state or potential neurological conditions.
