# Welcome to the Cogitate Data Release Documentation

![](https://slabstatic.com/prod/uploads/e7s1u9rt/posts/images/YhCPpII6QTj1tIubvGw378Ea.png)

---

| Version | Author(s) |
| --- | --- |
| 1.0 | Kahraman, K., Sripad, P., Brown, T., Melloni, L., Bonacchi, N. |

| Date | Editor(s) |
| --- | --- |
| April, 2023 | Kahraman, K., Sripad, P., Brown, T., Melloni, L., Bonacchi, N. |

---

 Scraps

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