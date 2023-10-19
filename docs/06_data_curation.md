# Data Curation Procedures

This SOP ensures that data goes through a rigorous process of quality control and curation before being released to the public or other authorized users. It also emphasizes the importance of protecting patient privacy by removing or anonymizing sensitive information and follows best practices for data management and release in research or clinical settings.

All code for data curation can be found at the following link:  [https://github.com/Cogitate-consortium/cogcurate](https://github.com/Cogitate-consortium/cogcurate) [private atm, to be made public]

SOP (Standard Operating Procedure) for data release:

**Step 1: Data Upload and QC (Quality Control)**



* Data is initially uploaded to the xnat-prod (XNAT Production) server. This server is the first point of entry for all data before it is made publicly available.
* The uploaded data goes through a quality control (QC) process to ensure that it meets the necessary standards and criteria for release. This QC step helps identify any potential issues or errors in the data.
* Once the data passes QC, it is then shared into Phase 2 by the Data Management Team (DMT). 

**Step 2: Data Transfer to Curate**



* To begin the curation process, data needs to be moved from xnat-prod to a dedicated curation environment called xnat-curate.
* Setting up xsync (data synchronization) between xnat-prod and xnat-curate ensures that data can be transferred securely and efficiently. xsync helps keep the two environments synchronized and up-to-date.

**Step 3: Curation Process**



* This step involves the actual curation process, where data is carefully reviewed and prepared for public release.
* Curation is performed on both metadata and data:
    * _Metadata Curation_: 
        * Ensures that personally identifiable information (PHI) and sensitive data are properly anonymized or removed to protect patient privacy.
        * Validates and checks Clinical Research Forms (CRFs) and other metadata for accuracy and completeness.
        * Reviews and curates any additional experimental or questionnaire (ExQus) data.
    * _Data Curation_:
        * Data is checked for quality and completeness, and any discrepancies are addressed (usually done during the QC step by the DMT).
        * Image data undergoes defacing to remove facial features, which helps protect patient privacy.
        * Headers and metadata within data files are reviewed and standardized.
        * Quality checks such as FreeSurfer (fs_recon checks) are performed on structural MRI data to ensure accuracy.

  

**Step 4: Data Transfer to xnat-public**



* Once the curation process is complete, the curated data is moved from xnat-curate to the final release location, which is typically xnat-public.
* xnat-public is where the cleaned and curated data is made available to authorized users or the public, depending on the data release policies and permissions.
* Data in xnat-public should be well-organized and easily accessible to users who have been granted access. 

TODO:



* add not explaining that organization in xnat mirrors the bundles