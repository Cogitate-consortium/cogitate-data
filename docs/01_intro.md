# Introduction

This document provides guidance and detailed information on the datasets released by COGITATE, how to access them, the directory structure, and a description on various types of data acquired for each modality.

## Updates

This is the <span style="color:red;">third version</span> (<span style="color:red;">V1.2</span>) of the COGITATE data release document. New updates or any changes to the previous versions will be announced here, and as a versioned document [here](https://github.com/Cogitate-consortium/cogitate-data/tree/main/assets/) as well.

In <span style="color:red;">V1.2</span>, we released the second subset of magnetoencephalography (MEG) data (batch 2) in the Brain Imaging Data Structure (<a href="https://bids-specification.readthedocs.io/en/stable/" target="_blank">BIDS</a>) format, along with eye tracking data (ET) in RAW format. This subset includes data from 52 subjects who participated in [Experiment 1](02_overview.md#experiment-1-conscious-perception), are released, packaged in a Bundle format.

<span style="background-color: red"><b>Attention:</b></span>
**The anatomical MRI scans are not available for subjects with the following IDs: CA101, CA102, CA104, CA110, CA111, and CA152. As a result, the folder containing the “sub-CX???_ses-1_trans.fif” does not exist for these subjects under “/derivatives/coreg”. Instead, the FreeSurfer standard template (fsaverage) was utilized.**

## Future Releases

Here are the items that will be released soon:

### Experiment 1

* Unprocessed/raw format of all M-EEG data (batch 1 and batch 2)
* Unprocessed/raw and BIDS format of fMRI data

## Previous Releases

Here is the list of previous COGITATE data release documents:

| Version | Data Release Document | Description |
| --- | --- | --- |
| v1.0 | <a href="https://github.com/Cogitate-consortium/cogitate-data/blob/main/assets/documentation_v1.0/MEEG-DR-doc_2024-03-18_v1.0.pdf" target="_blank">MEEG-DR-doc_2024-03-18_v1.0</a> | MEEG (batch 1) data release document |
| v1.1 | <a href="https://github.com/Cogitate-consortium/cogitate-data/blob/main/assets/documentation_v1.1/iEEG-DR-doc_2024-04-03_v1.1.pdf" target="_blank">iEEG-DR-doc_2024-04-03_v1.1</a> | iEEG data release document |

## Documentation Changes

In each new version of the COGITATE data release document, relevant content for another modality/experiment is appended to the previous version, and there may be modifications made to the content of the previous versions. The list of these changes is compiled in the following documents:

| Version | Data Release Documentation Changes | Description |
| --- | --- | --- |
| v1.0 | <a href="https://github.com/Cogitate-consortium/cogitate-data/blob/main/assets/documentation_v1.1/Documentation-Changes_2024-04-17_v1.0.pdf" target="_blank">Documentation-Changes_2024-04-17_v1.0</a> | Changes from MEEG (batch 1) data release document (v1.0) to iEEG data release document (v1.1) |
| v1.1 | <a href="https://github.com/Cogitate-consortium/cogitate-data/blob/main/assets/documentation_v1.2/Documentation-Changes_2024-06-11_v1.1.pdf" target="_blank">Documentation-Changes_2024-06-11_v1.1</a> | Changes from iEEG data release document (v1.1) to MEEG (batch 2) data release document (v1.2) |

<span style="background-color: red"><b>Attention:</b></span>
**M-EEG, MEEG, M/EEG, MEG/EEG or MEG might be used interchangeably throughout this document or the name of data folders, but all of them pertain to a singular data. This also applies to iEEG and ECoG (Electrocorticography).**
