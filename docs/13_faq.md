# FAQ

## Cogitate M-EEG BIDS FAQs

### Where are the trans files?

The trans.fif files are provided under /derivatives/coreg. They are the results of the coregistration. This information is also included as landmarks in sidecar json of the NIFTI file.

### What is under derivatives/additional_metadata?

This directory contains some additional metadata collected along with the data. The top level METADATA directory contains some files common to all subjects: They are analysis.json, devices_MEEG.json, protocols.json, tasks_EXP1_MEEG.json, tasks_RestinEO_MEEG.json, tasks_Rnoise_MEEG.json, wiring_MEEG.pdf.

Subject level directories contain three files: CXXXX_CRF.json, CXXXX_demographics.json, CXXXX_EXQU.json which are respectively subject specific demographics, case report form and the exit questionnaire. The demographics information is redundant with the information in the participants.tsv files.

### What does BATCH1 mean?

The M-EEG datasets for COGITATE are being released in two batches in order to facilitate the BIOMAG Connectivity Challenge 2024. This means that one half of the data is initially made available to the participants of the challenge followed by the second half a few months later. This is where BATCH1 and BATCH2 come in.

### I cannot find the EOG channel in the data?

The EOG channel for site A can be found in `EOG004` and the EOG channels for site B can be found in `BIO002`. Typically in our code, we prefer to rename the channels as below.

```
# Fix EOG001 channel name (required for CA only)
if 'EOG004' in raw.ch_names:
raw. rename_channels ({ 'EOG004': 'EOG001'})

# Fix EOG001 channel name(required for CB only)
eog_ch = raw.copy().pick_types(meg=False, eeg=False, eog=True)
if len(eog_ch. ch_names) < 2:
raw.set_channel_types({'BIO002': 'eog'})
raw.rename_channels({'BIO002': 'EOG002'})
```

### What do the channels MISC1, MISC2 and MISC3 contain?

These channels contain the eye tracker data with MISC1 (X), MISC2 (Y), and MISC3 (pupil) channels containing the X, Y (gaze) and the Pupil information respectively. This information is however also shared separately in the eye tracking data release.
