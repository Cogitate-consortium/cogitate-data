# Curation Procedures

## Data Curation Procedure

A detailed explanation about the multiple steps that were taken to prepare the data to be released in public will be available in Appendix 7.

### Deviations from Data Curation Procedure

#### iEEG

Our approach to defacing MR/CT DICOM images involved utilizing the built-in face masking tool from XNAT. However, for 12 iEEG subjects, we encountered difficulties in executing this step. This was primarily due to variations in the DICOM images, which could include cropped images, aliasing artifacts, broken headers, missing slices, non-equidistant slices within a series, and other issues. Below is the list of subjects where the execution of the XNAT facemasking tool failed:

**Subject_ID:** CF103, CF104, CF112, CF113, CF116, CF117, CF120, CF121, CF122, CF124, CF125, CF126

To address this issue, we implemented a slightly different workflow that allowed us to successfully deface MR/CT images of these 12 subjects. However, this new approach differed in its ability to regenerate the original DICOM images post-defacement (the original output from the XNAT facemasking tool). Instead, it generated defaced NIFTI images as the primary output. For our current version of data release, we have decided to share only the defaced NIFTI images for these subjects. Details about this workflow are provided below:

1. Anonymization: MR/CT DICOM images underwent anonymization to remove the subject’s Protected Health Information (PHI).
2. NIFTI Conversion: Anonymized DICOM images were then converted to the NIFTI image format using the dcm2niix package (version: 1.0.20220505) (Li et al., 2016).
3. Defacing of NIFTI: Defacing of the NIFTI images was performed using the PyDeface package (version: 2.0.2) (Gulban et al., 2022).
4. Verification: This step involved checking the quality of the defaced NIFTI images using 2D/3D image plots to compare before and after the defacing stage.

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/merge_docs/assets/documentation/graphics/Alternative%20workflow%20for%20defacing%20challenging%20DICOM%20Images.png" alt="Alternative workflow for defacing 12 challenging MR/CT DICOM Images">
  <p>Alternative workflow for defacing 12 challenging MR/CT DICOM Images</p>
</div>

<span style="background-color: red"><b>Miscellaneous:</b></span> **In the MR data for subject CF103, one DICOM slice was inadvertently dropped during the conversion process from DICOM to NIFTI format. However, the resulting NIFTI file remains functional and usable.**

## Metadata Curation Procedure

Comprehensive guidance on extracting and managing metadata relevant to the COGITATE project is available in <a href="https://github.com/Cogitate-consortium/cogitate-data/blob/merge_docs/assets/documentation/linked_files/metadata-curation-doc_2024-05-14_v1.0.pdf" target="_blank">Appendix 8</a>.
