# Welcome to the Cogitate Data Release Documentation

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


![](https://slabstatic.com/prod/uploads/e7s1u9rt/posts/images/BqPvxY6krzV2M0jE0gL_jU_a.png)

![](https://slabstatic.com/prod/uploads/e7s1u9rt/posts/images/YhCPpII6QTj1tIubvGw378Ea.png)

![](https://docs.google.com/drawings/d/sYlUhqGzsQNw3Li0GS-0cDw/image?parent=14XIQaL1khTwJhSfXDwW4xQi8GbSfqZc16-irY4wpoBI&rev=1&drawingRevisionAccessToken=vH2MWY0ZyWASRw&h=549&w=841&ac=1)

![](https://docs.google.com/drawings/d/sIfdBhAMDmOjdzSd8RVi3Vg/image?parent=14XIQaL1khTwJhSfXDwW4xQi8GbSfqZc16-irY4wpoBI&rev=66&drawingRevisionAccessToken=zq7BgRUEZkgAPA&h=162&w=649&ac=1)

| Version | Author(s) |
| --- | --- |
| 1.0 | Kahraman, K., Sripad, P., Bonacchi, N., Brown, T., Melloni, L. |
| Date | Editor(s) |
| April, 2023 | Kahraman, K., Sripad, P., Bonacchi, N., Brown, T., Melloni, L. |

---

### Introduction

[COGITATE](https://www.google.com/url?q=https://www.arc-cogitate.com/&sa=D&source=editors&ust=1691514940815048&usg=AOvVaw1SwgxzULrjeW7HPrQvnYBR) is a groundbreaking endeavor within Open Science, featuring a pre-registered adversarial collaboration aimed at resolving the debate between two prominent theories of consciousness: Integrated Information Theory (IIT) and Global Neuronal Workspace theory (GNW). This initiative encompasses eleven distinct research institutions spanning three continents, utilizing three distinct neuroimaging methods in human neuroscience—fMRI, M-EEG, and iEEG—across an extensive cohort of human volunteers and patients. A comprehensive outline of Experiment 1 is available in our pre-registration document [LINK], pre-print manuscript [LINK], and forthcoming publication.

### Subjects[[a][b][c]](#cmnt1)

The full Cogitate dataset includes 256 subjects, mostly right handed (229), with a median age of 23 years.

All investigations were carried out by impartial teams with no theoretical bias to prevent confirmation bias. We assessed the predictions of the theories using 256 participants who completed an identical behavioral task using three distinct neuroimaging techniques: functional magnetic resonance imaging (fMRI, N=120), magnetoencephalography (MEEG, N=102), and intracranial electroencephalography (iEEG, N=34). [LINK TO DATA ACQUISITION MODALITIES]

### Experiment 1

Experiment 1 description, behavioral task, task blocks, etc….

Explain 2 exp were performed, hint to experiment 2 (video game) for follow up release…



### Data description

Although our data collection had a specific purpose, the data we gathered holds potential value for a range of diverse inquiries. Consequently, the COGITATE consortium has chosen to openly share all raw data collected, with the aim of facilitating its utilization for various research endeavors and promoting data reusability. This approach reflects our commitment to contributing to the broader scientific community.

We have made available two primary formats for the data acquired during the experimental phase of the COGITATE project, specifically from Experiment 1:

1. Unprocessed Data:

The unprocessed data format closely resembles the original acquired data, having undergone minimal processing to ensure compliance with GDPR/HIPAA anonymity standards.

2. BIDS Format (Brain Imaging Data Structure):

BIDS format, widely adopted in cognitive neuroscience, enhances data reusability. To facilitate others in leveraging our data, we have released it in BIDS format. The conversion scripts employed to transform the raw data into BIDS format can be accessed via this link: [LINK].

We emphasize our explicit intent to share the entirety of our data, empowering the community to integrate it into their research. When utilizing the data, it is important to consider the contextual factors and limitations that may affect its interpretation.

Release format and Modality Table

| Release format →<br>| Modality | Raw / Unprocessed | Bids converted | Bids derivatives / Pre-processed | Additionally processed |
| --- | --- | --- | --- | --- |
| Eye Tracking & Behavioral data | EDF | EDF | ASC | ASC |
| fMRI | DICOM | DICOM | NIFTI | NIFTI |
| MEEG | FIF | FIF | NPY | NPY |
| iEEG/ECoG | EDF | EDF | EDF | EDF |
|  |  |  |  |  |

#### File type glossary

EDF files

EDF files, also known as European Data Format files, are a standardized file format used for storing and exchanging time-series biological and physiological data. EDF files are commonly used in medical and scientific research contexts to record and analyze data from various types of measurements, such as electroencephalography (EEG), electrocardiography (ECG), electromyography (EMG), and other bioelectrical signals.

EDF files are designed to accommodate data from multiple channels, allowing researchers to store and manage data collected simultaneously from different sensors or electrodes. The format supports both raw signal data and associated metadata, including information about sampling rates, units of measurement, patient demographics, and recording conditions.

One of the key advantages of the EDF format is its portability and compatibility across different software and platforms. Many data analysis and visualization tools in the field of neuroscience and medicine support the EDF format, enabling researchers to share and collaborate on data without compatibility issues.

It's worth noting that there are variations and extensions of the EDF format, such as EDF+ and EDF/EDF+ Converter, which provide additional features and improvements for specific applications. Overall, EDF files play an essential role in the storage and analysis of physiological and biological data in scientific and medical research.

FIF files

FIF files in MEEG (Magnetoencephalography and Electroencephalography) refer to the File Format for the Input and Output of MEG and EEG data. MEG and EEG are neuroimaging techniques used to study brain activity. FIF files are a standardized format developed by the MNE (Magnetoencephalography and Electroencephalography) community to store and exchange MEG and EEG data.

FIF files contain various types of information related to neuroimaging data, including:

1. Raw sensor data: MEG and EEG measurements recorded from sensors placed on the scalp or near the head.
1. Event information: Time-stamped triggers or markers indicating the timing of events, such as stimulus presentations or subject responses.
1. Sensor locations and orientations: Information about the physical positions and orientations of sensors used in the measurements.
1. Head geometry: Information about the shape and structure of the subject's head, which is crucial for accurate source localization.
1. Covariance matrices: Statistical information about the relationships between sensor measurements at different time points or frequencies.
1. Anatomical MRI data: High-resolution structural images of the subject's brain, used for source localization and spatial alignment.

The FIF file format ensures compatibility and interoperability between different MEG and EEG software tools and facilitates data sharing and collaboration in the neuroimaging research community. It's worth noting that MEG and EEG data can be quite complex and multidimensional, and the FIF format provides a structured and standardized way to store and manage this data.

ASC files

ASC files in the context of eye tracking refer to data files generated by eye tracking systems, which are used to record and analyze eye movement and gaze behavior. These files contain valuable information about a person's visual attention, including where they are looking, how long they are looking at certain areas, and how their gaze moves across a screen or a visual stimulus.

ASC files typically store a time-stamped sequence of gaze data points, which include information such as:

1. Timestamps: The exact time at which each gaze data point was recorded.
1. Gaze Coordinates: The x and y coordinates on the screen where the person's gaze is directed.
1. Pupil Diameter: The size of the person's pupil, which can provide insights into changes in visual processing or cognitive load.
1. Fixations: Periods of stable gaze where the person is looking at a specific point without significant movement.
1. Saccades: Rapid eye movements between fixations, indicating shifts in attention.
1. Blinks: Instances when the person's eyes are closed, which can be important for data cleaning and analysis.

Researchers and usability professionals use ASC files to study various aspects of human visual attention and cognitive processes. Eye tracking studies can provide insights into user behavior when interacting with websites, advertisements, software interfaces, or other visual stimuli. By analyzing ASC files, researchers can better understand how people engage with visual information, make decisions, and process visual content.

Software tools and programming libraries are often used to process and analyze ASC files, extracting meaningful patterns and insights from the raw gaze data. These insights can be used to optimize user interfaces, design effective visual communication, and improve user experiences in various applications.

DICOM files

DICOM (Digital Imaging and Communications in Medicine) files are a standard format used for storing, transmitting, and managing medical images and related information. They are widely used in the field of radiology and other medical imaging specialties, such as MRI (Magnetic Resonance Imaging), CT (Computed Tomography), ultrasound, and more.

DICOM files are designed to ensure interoperability and compatibility among different imaging devices, picture archiving and communication systems (PACS), and other healthcare information systems. These files contain not only the actual image data but also metadata and contextual information, such as patient information, image acquisition parameters, study details, and more. This comprehensive set of information allows medical professionals to accurately interpret and diagnose medical images, track patient history, and collaborate effectively across different healthcare facilities.

DICOM files typically have a ".dcm" file extension and adhere to a specific structure and data format defined by the DICOM standard. This standardization facilitates seamless exchange of medical images and data between different software and hardware platforms, contributing to improved patient care and medical research.

NIFTI files

NIFTI (Neuroimaging Informatics Technology Initiative) files are a widely used file format in the field of neuroimaging, particularly in the context of functional and structural magnetic resonance imaging (MRI) data. These files store three-dimensional brain images and related metadata, allowing researchers and clinicians to store, share, and analyze neuroimaging data.

NIFTI files typically have the ".nii" or ".nii.gz" file extensions. The ".nii" format is uncompressed, while the ".nii.gz" format is compressed using gzip compression. These files contain information about the image dimensions, voxel sizes, data type (e.g., integer or floating-point values), and other relevant information.

NIFTI was developed as an improvement over the earlier Analyze file format. It addresses certain limitations of the Analyze format, such as the ability to handle 3D and 4D data (3D data over time), improved support for different data types, and better compatibility with modern software tools.

Researchers and medical professionals use NIFTI files to store various types of neuroimaging data, including structural  MRI scans, functional MRI scans, and diffusion tensor imaging (DTI) data (which captures white matter tracts and connectivity patterns within the brain).

NIFTI files are supported by many neuroimaging software packages, making them a crucial part of the neuroimaging data analysis workflow. Researchers can use these files for tasks such as preprocessing, visualization, statistical analysis, and creating anatomical atlases.

NPY files

NPY files, short for "NumPy files," are a file format used in the Python programming language for storing and exchanging numerical data. NumPy is a popular library in Python that provides support for multi-dimensional arrays and matrices, along with various mathematical functions to operate on these arrays.

NPY files are specifically used to save and load arrays and data structures created using NumPy. These files have the extension ".npy" and are binary files that efficiently store the data in a format that preserves the array's shape, data type, and other metadata. This makes them suitable for fast and efficient storage and retrieval of large numerical datasets, which is especially useful in scientific computing, data analysis, and machine learning applications.

### Acquisition Modalities

The Cogitate dataset encompasses three distinct neuroimaging modalities, along with synchronized eye-tracking and behavioral data linked to one of these modalities.

---

#### fMRI data acquisition

Anatomical and functional MRI data were acquired on two 3T Prisma scanners (Siemens, Erlangen, Germany), using 32-channel head coils. Anatomical images were acquired using a T1-weighted magnetization prepared rapid gradient echo sequence (MP-RAGE; GRAPPA acceleration factor = 2, TR/TE = 2300/3.03 ms, voxel size 1 mm isotropic, 8° flip angle). Functional images were acquired using a whole-brain T2-weighted multiband-4 sequence (time repetition [TR] / time echo [TE] = 1500/39.6 ms, 68 slices, voxel size 2 mm isotropic, 75° flip angle, A/P phase encoding direction, FOV = 210 mm, BW = 2090 Hz/Px). In addition, a single band reference image was acquired before each run. To allow for signal stabilization, the first three volumes of each run were discarded. Additional scans using the same T2-weighted sequence, but with inverted phase encoding direction (inverted RO/PE polarity), were collected at multiple points throughout the experiments.

Data for Experiment 1 was acquired from 120 Subject in 2 locations:

- Donders Center for Cognitive Neuroimaging (DCCN)
- Yale Magnetic Resonance Research Center (MRRC)

Standard Operating Procedures for both locations can be found in the following links:

- Technical checklist PRESCREENING
- Technical Checklist DCCN
- Technical Checklist MRRC

In depth functional description of the experimental apparatus:

- Functional_Description.pdf
- Optical_path_PrismaFit_BOLDscreen.pdf  

Final parameters for acquisition:

- FMRI_Blumenfeld_Tempelton_Ex1_final_parameters.pdf

---

#### iEEG (ECoG) data acquisition

intracranial electroencephalography (iEEG, N=34).

iEEG (ECoG) SOPs: New York University; Harvard University; Wisconsin University

- 25 Subjects from each lab

- Total: ca. 26 (is this still right?)

- Measurements

- SOPs

- Techniques

- etc.

- Acquisition sites:

- Harvard University at Boston Children's Hospital

- Brigham and Women's Hospital

- New York University Langone (NYU)

- University of Wisconsin

#### MEEG data acquisition

magnetoencephalography (MEEG, N=102), and

MEEG SOPs: Peking University; Birmingham University

- 50 Subjects from each lab

- Total: 102

- measurements

- SOPs

- Techniques

- etc.

- Acquisition sites:

- University of Birmingham's Centre for Human Brain Health (CHBH)

- Peking University (PKU)

#### Eye tracking and Behavioral data acquisition

All modalities acquired Eye Tracking and Behavioral data for Experiment 1 using …

### Anonymization procedures

All data acquired was reviewed and anonymized. The anonymization scripts that were used can be found here (github link to COGCURATE)

List of main procedures

Defaced,

ID datasets w/ PHI

run scripts to anonymize [link to cogcurate]

upload to XNAT

Create bundles

Defacing numbers as of 07.08.2023

Totals across all projects

- Defaced MR sessions: 233

- Non MR sessions across all projects: 329

- MR Sessions scans that are not anatomical scans (all sessions from the FMRI labs): 8012

ECOG

CoG_NYU_PhaseI: 7 / 20 subjects (7 anat scans missing / 6 scans errored out)

CoG_Harvard_PhaseI: 0 / 12 subjects (all anatomical scans missing)

CoG_WU_PhaseI: 5 / 5

FMRI

CoG_Yale_PhaseI: 62 / 62 subjects

CoG_Donder_PhaseI: 63 / 60 subjects (3 extra discarded scans / also defaced)

MEEG

CoG_PKU_PhaseI: 50 / 50 subjects

CoG_BU_PhaseI: 46 / 52 subjects (8 subjects don't have anatomical scans)

### Access COGITATE data

To facilitate access to our data, we offer two main avenues:

#### 1. Archival Format:

This approach involves providing a collection of links to bundles of data and accompanying metadata. These links grant users the ability to download specific modalities, example datasets, or the complete dataset. Access to these resources requires a registration process on our website: [LINK].

#### 2. "Live" Database Release:

Our "live" release involves an XNAT database instance that contains our data. This database offers a web interface for navigating the data and an API for programmatically retrieving specific datasets based on user interests. Comprehensive instructions on how to register, access, and query our database are provided in the subsequent sections.

By disseminating our data through these two avenues, we endeavor to make it accessible and usable for a wide range of scientific investigations.

Add detailed procedures[[d]](#cmnt4)

- XNAT open repository instance

- will contain:

- Matlab/Python code to analyze and/or pre-process data

- MRI pulse sequences developed and used to acquire the data

- all de-identified, PHI removed and defaced MRI, neurophysiological eye tracking and behavioral data adhering to the FAIR principle.

- any peer-reviewed article (as far as journal allows it)

- any experimental code

### Tutorials and Examples

### Next steps

Experiment 2 Preprocessed and fully processed data (Bids derivatives)

### Support

Where to contact us

Where to put issues

Where to get help

### Appendix

---

### Scraps

Intro to Cogitate goal and experiment [link to website]

→ What is in the release

Data release description

→ Subjects & Modalities

→ Format of the release (Database & archival format)

→ Raw / BIDS / sample_data for analysis repro

→ Link to Bundles

Miscellaneous

→ SOPs

→ Anonymization

Examples and Tutorials

Processing Tools

1. Matlab and Python code used to analyze or pre-process the data
1. Any MRI pulse sequences (binaries) developed and used to acquire the data
1. All (de-identified, PHI removed and defaced) MRI, neurophysiological, eye tracking and behavioral data adhering to the FAIR principle. The FAIR Data Principles refer to a set of guidelines to make data findable, accessible, interoperable and reusable (Wilkinson et al., 2016). Specifically, all data will be transformed to Brain Imaging Data Structure BIDS format ([http://bids.neuroimaging.io](https://www.google.com/url?q=http://bids.neuroimaging.io/&sa=D&source=editors&ust=1691514940855904&usg=AOvVaw1UB9wRRG9UEgUU64qFERxY)) and all metadata will be made available.
1. Data will be converted to shareable data formats (BIDS).

The neurophysiological recordings (clinical ECoG and experimental electrodes), relevant task data, electrode coordinates in MNI space and essential, de-identified clinical data using NINDS Common Data Elements (age, sex, duration of epilepsy, epilepsy etiology, preoperative imaging findings) and schematics of seizure onset areas will also be made available.

In order to access or download files containing behavioral, eye tracking, neurophysiological or MRI data, users will have to register. As they register, they will agree to restrictions against attempting to identify study participants, restrictions on redistribution of the data to third parties, and to properly acknowledge the data resource.[[e]](#cmnt5)

This document provides information and guidance on how to use data released by the TWCF COGITATE Project consortium.

The COGITATE Project aimed to study …

Given the richness of the COGITATE datasets and their utility for a wide range of research purposes, it is important that potential users understand what data are currently released, how the datasets are organized, how they can be accessed, what has changed since the last releases ….

(copied by HCP 1200 Subjects data release for orientation)

Final COGITATE Study Overall Totals:

X subjects with XY Modality

COGITATE subjects include

X

This data release included behavioral measures, eye tracking, fMRI and M-EEG data on subjects collected in the COGITATE production data phase (YEAR-YEAR) including unprocessed (raw defaced), pre-processed and final processed fMRI etc. pp.

fMRI data

- 50 Subjects from each lab

- Total: 122

- Measurements?

- Techniques?

- Acquisition sites:

- Donders Center for Cognitive Neuroimaging (DCCN)

- Yale Magnetic Resonance Research Center (MRRC) SOP: [Standard Operating Procedures](https://twcf-arc.slab.com/posts/kpb18fmw#h1f9d-yale)

data acqusition:

Anatomical and functional MRI data were acquired on two 3T Prisma scanners (Siemens, Erlangen, Germany), using 32-channel head coils. Anatomical images were acquired using a T1-weighted magnetization prepared rapid gradient echo sequence (MP-RAGE; GRAPPA acceleration factor = 2, TR/TE = 2300/3.03 ms, voxel size 1 mm isotropic, 8° flip angle). Functional images were acquired using a whole-brain T2-weighted multiband-4 sequence (time repetition [TR] / time echo [TE] = 1500/39.6 ms, 68 slices, voxel size 2 mm isotropic, 75° flip angle, A/P phase encoding direction, FOV = 210 mm, BW = 2090 Hz/Px). In addition, a single band reference image was acquired before each run. To allow for signal stabilization, the first three volumes of each run were discarded. Additional scans using the same T2-weighted sequence, but with inverted phase encoding direction (inverted RO/PE polarity), were collected at multiple points throughout the experiments.

data preprocessing:

Source DICOM data was converted to a BIDS compliant dataset using BIDScoin v3.6.3 (https://bidscoin.readthedocs.io). This includes converting DICOM data to nifti using dcm2niix (Li et al., 2016, PMID: 26945974) and creating event files using custom Python (Python Software Foundation, RRID:SCR_008394) code. BIDS compliance of the resulting dataset was controlled using BIDS-Validator (https://doi.org/10.5281/zenodo.3688707). Subsequently, MRI data quality control was performed using MRIQC (Esteban et al., 2017) and custom scripts for data rejection. All (f)MRI data was preprocessed using fMRIPrep 20.2.3 (Esteban, Markiewicz, et al. (2018); Esteban, Blair, et al. (2018); RRID:SCR_016216), based on Nipype 1.6.1 (Gorgolewski et al. (2011); Gorgolewski et al. (2018); RRID:SCR_002502). In addition, analysis specific preprocessing was performed using FSL 6.0.2 (FMRIB Software Library; Oxford, UK; Smith et al., 2004, RRID:SCR_002823) and custom Python scripts using the following packages: NumPy XX (van der Walt et al., 2011, RRID:SCR_008633), Pandas XX (McKinney et al., 2010) NiBabel XX (https://doi.org/10.5281/zenodo.4295521), SciPy XX (Jones et al., 2001, RRID:SCR_008058), Matplotlib XX (Hunter, 2007, RRID:SCR_008624), Scikit-learn XX (Pedregosa et al., 2011, RRID:SCR_002577).

COPY PASTED THE DOC “fMRI_data_workflow_and_analyses” FROM KEEPER/GOOGLE DRIVE

fMRI data quality control:

MRI data quality was screened using MRIQC (Esteban et al., 2017). Visual inspection of (f)MRI data was performed on the visual reports output by MRIQC and datasets with artifacts or other indicators of low data quality flagged by a trained observer, not involved in the MRI data acquisition. If the detected problems with data quality were judged severe enough to warrant potential exclusion, data was inspected by an additional observer. In total XX datasets were excluded due to low-quality. Quantitative data rejection. Additionally, fMRI datasets with excessive motion or subpar signal quality were rejected using the image quality metrics reported by MRIQC. The percentage of fMRI volumes that exceeded a thresholded of 0.2mm framewise displacement (fd_perc) was calculated per run and then averaged across runs per MRI session. Similarly, the DVARS (Power et al., 2012; dvars_nstd) was extracted per run and then averaged for each session. Finally, each MRI session that showed 2SD above the group mean on percentage framewise displacement or DVARS was rejected from all MRI data analysis. This resulted in an additional exclusion of XX MRI datasets.

Anatomical data preprocessing:

Per participant, the T1-weighted (T1w) image was corrected for intensity non-uniformity (INU) with N4BiasFieldCorrection (Tustison et al. 2010), distributed with ANTs 2.3.3 (Avants et al. 2008, RRID:SCR_004757), and used as T1w-reference throughout the workflow. The T1w-reference was then skull-stripped with a Nipype implementation of the antsBrainExtraction.sh workflow (from ANTs), using OASIS30ANTs as target template. Brain tissue segmentation of cerebrospinal fluid (CSF), white-matter (WM) and gray-matter (GM) was performed on the brain-extracted T1w using fast (FSL 5.0.9, RRID:SCR_002823, Zhang, Brady, and Smith 2001). Brain surfaces were reconstructed using recon-all (FreeSurfer 6.0.1, RRID:SCR_001847, Dale, Fischl, and Sereno 1999), and the brain mask estimated previously was refined with a custom variation of the method to reconcile ANTs-derived and FreeSurfer-derived segmentations of the cortical gray-matter of Mindboggle (RRID:SCR_002438, Klein et al. 2017). Volume-based spatial normalization to one standard space (MNI152NLin2009cAsym) was performed through nonlinear registration with antsRegistration (ANTs 2.3.3), using brain-extracted versions of both T1w reference and the T1w template. The following template was selected for spatial normalization: ICBM 152 Nonlinear Asymmetrical template version 2009c [Fonov et al. (2009), RRID:SCR_008796; TemplateFlow ID: MNI152NLin2009cAsym],

Functional data preprocessing:

For each of the fMRI BOLD runs per subject, the following preprocessing was performed. First, a reference volume and its skull-stripped version were generated using a custom methodology of fMRIPrep. A B0-nonuniformity map (or fieldmap) was estimated based on two (or more) echo-planar imaging (EPI) references with opposing phase-encoding directions, with 3dQwarp Cox and Hyde (1997) (AFNI 20160207). Based on the estimated susceptibility distortion, a corrected EPI (echo-planar imaging) reference was calculated for a more accurate co-registration with the anatomical reference. The BOLD reference was then co-registered to the T1w reference using bbregister (FreeSurfer) which implements boundary-based registration (Greve and Fischl 2009). Co-registration was configured with six degrees of freedom. Head-motion parameters with respect to the BOLD reference (transformation matrices, and six corresponding rotation and translation parameters) are estimated before any spatiotemporal filtering using mcflirt (FSL 5.0.9, Jenkinson et al. 2002). The BOLD time-series (without slice-timing correction) were resampled onto their original, native space by applying a single, composite transform to correct for head-motion and susceptibility distortions. These resampled BOLD time-series will be referred to as preprocessed BOLD in original space, or just preprocessed BOLD. The BOLD time-series were resampled into standard space, generating a preprocessed BOLD run in MNI152NLin2009cAsym space. Several confounding time-series were calculated based on the preprocessed BOLD: framewise displacement (FD), DVARS and three region-wise global signals. FD was computed using two formulations following Power (absolute sum of relative motions, Power et al. (2014)) and Jenkinson (relative root mean square displacement between affines, Jenkinson et al. (2002)). FD and DVARS are calculated for each functional run, both using their implementations in Nipype (following the definitions by Power et al. 2014). The three global signals are extracted within the CSF, the WM, and the whole-brain masks. Additionally, a set of physiological regressors were extracted to allow for component-based noise correction (CompCor, Behzadi et al. 2007). Principal components are estimated after high-pass filtering the preprocessed BOLD time-series (using a discrete cosine filter with 128s cut-off) for the two CompCor variants: temporal (tCompCor) and anatomical (aCompCor). tCompCor components are then calculated from the top 2% variable voxels within the brain mask. For aCompCor, three probabilistic masks (CSF, WM and combined CSF+WM) are generated in anatomical space. The implementation differs from that of Behzadi et al. in that instead of eroding the masks by 2 pixels on BOLD space, the aCompCor masks are subtracted a mask of pixels that likely contain a volume fraction of GM. This mask is obtained by dilating a GM mask extracted from the FreeSurfer’s aseg segmentation, and it ensures components are not extracted from voxels containing a minimal fraction of GM. Finally, these masks are resampled into BOLD space and binarized by thresholding at 0.99 (as in the original implementation). Components are also calculated separately within the WM and CSF masks. For each CompCor decomposition, the k components with the largest singular values are retained, such that the retained components’ time series are sufficient to explain 50 percent of variance across the nuisance mask (CSF, WM, combined, or temporal). The remaining components are dropped from consideration. The head-motion estimates calculated in the correction step were also placed within the corresponding confounds file. The confound time series derived from head motion estimates and global signals were expanded with the inclusion of temporal derivatives and quadratic terms for each (Satterthwaite et al. 2013). Frames that exceeded a threshold of 0.5 mm FD or 1.5 standardised DVARS were annotated as motion outliers. All resamplings can be performed with a single interpolation step by composing all the pertinent transformations (i.e. head-motion transform matrices, susceptibility distortion correction when available, and co-registrations to anatomical and output spaces). Gridded (volumetric) resamplings were performed using antsApplyTransforms (ANTs), configured with Lanczos interpolation to minimize the smoothing effects of other kernels (Lanczos 1964). Non-gridded (surface) resamplings were performed using mri_vol2surf (FreeSurfer).

What is missing? What should go somewhere else?

iEEG (ECoG) data

- 25 Subjects from each lab

- Total: ca. 26 (is this still right?)

- Measurements

- SOPs

- Techniques

- etc.

- Acquisition sites:

- Harvard University at Boston Children's Hospital

- Brigham and Women's Hospital

- New York University Langone (NYU)

- University of Wisconsin

= LINK HERE INFORMATION FROM OTHER SLAB POSTS

MEEG data

- 50 Subjects from each lab

- Total: 102

- measurements

- SOPs

- Techniques

- etc.

- Acquisition sites:

- University of Birmingham's Centre for Human Brain Health (CHBH)

- Peking University (PKU)

= LINK HERE INFORMATION FROM OTHER SLAB POSTS

= 550 Datasets total

→ Eye tracking in all modalities (all sites have same eye tracker except NYU) NOT SURE HOW TO HANDLE INFORMATION/WHERE TO PUT

→ Behavior data should get a separate section

SUMMARY SUBJECTS INFO [graphs?]

- Age

- Gender

- Dominant Hand

- Eye dominance

- Visual acuity (eye chart results, 20/20, 20/30, 20/40, etc.)

- No glasses, glasses, contact lenses

- Dioptre for both eyes for subject wearing glasses or contact lenses (if known)

- Colour blindness

- Auditory sensitivity

- Level of education

- Ethnicity

- Primary language

- Secondary language

![](https://slabstatic.com/prod/uploads/e7s1u9rt/posts/images/QtoiUtFOUy6u5AOQKUg6cnFL.png)

COGITATE Data Release                         [arc-cogitate.com](https://www.google.com/url?q=https://arc-cogitate.com/&sa=D&source=editors&ust=1691514940871202&usg=AOvVaw2NtPywRBEu9N1JyNNm13g7)

![](https://docs.google.com/drawings/d/sgVDJLdgJUqzBLj6OP88ybQ/image?parent=14XIQaL1khTwJhSfXDwW4xQi8GbSfqZc16-irY4wpoBI&rev=1&drawingRevisionAccessToken=4qgMPAnNt8xA2w&h=2&w=639&ac=1)

[[a]](#cmnt_ref1)MAybe add summary graphs for subjects demographics. Do we have these?

[[b]](#cmnt_ref2)_Marked as resolved_

[[c]](#cmnt_ref3)_Re-opened_

[[d]](#cmnt_ref4)to each release type

[[e]](#cmnt_ref5)Review this and put it in the intro/description