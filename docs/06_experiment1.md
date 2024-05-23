# Experiment 1: Directory Structure of Data Bundles

## Raw Data

Raw data files are organized hierarchically: Experiment modality --> Subjects --> data folders

The metadata related to each level of the hierarchy is contained in a mandatory folder called 'metadata'.

Each data folder follows a naming convention {subject_context_modality\[\_modifier]} the section of the names are separated by underscores. This naming convention aims at making it easy to identify the data files that relate to the same moment in time and that were acquired simultaneously.

* subject -> this refers the the subject ID
* context -> the task or context. This section is optional and can be empty, e.g. if a subject had a standalone MR scan the context is left blank, resulting in a double underscorlike in the case of the CT scan or MR scan in the above example
* modality -> or type of data collected

The Cogitate consortium collected several types of data/metadata during the experiments:

* **BEH**: behavioral events
* **ET**: Eye tracking data
* **MR**: Magnetic resonance data (anatomical scans)

* **MEEG**: Magneto-Electroencephalographic data
* **EXQU**: Exit Questionnaire
* **CRF**: Case Report Form

All metadata related to the subject can be found under the aptly named 'metadata' folder under the subject folder (this refers mainly to the EXQU and CRF files).

The remaining metadata for the experiment as well as the demographic information on the subjects can be found in the metadata folder above the subject.

This folder includes experiment wide metadata in json format and a csv table with the demographic data of all subjects:

* **devices**: A list of devices used to collect the data
* **protocols**: a link to the Standard Operating Procedure (SOP) document used for the data collection
* **subjects_demographics**: the full set of subjects and their metadata for the specific experiment modality
* **tasks_*taskname***: a description of the behavioral task or context with which we named the data bundles.
* **wirings**: a pdf file showing how the **devices** are connected to each other depicting the experimental setup.

### Raw M-EEG Data Directory Structure

```bash
COG_MEEG_EXP1_RELEASE/
    ├── metadata/                               # Experiment modality level metadata folder
    │    ├── devices_MEEG.json                  # List of devices used to collect the data
    │    ├── protocols_MEEG.json                # A link to the Standard Operating Procedures (SOP)
    │    ├── subjects_demographics_MEEG.json    # Demographic information of MEEG subjects
    │    ├── tasks_EXP1.json                    # Description of the 1st Cogitate task 
    │    ├── tasks_RestinEO.json                # Description of the Resting state task
    │    ├── tasks_Rnoise.json                  # Description of the Rnoise task 
    │    └── wirings_MEEG.PDF                   # Wiring diagram of devices_MEEG.json connections 
    └── CB036                                   # Subject folder
        ├── metadata/                           # Subject level metadata folder
        │    ├── CB036_EXP1_CRF.json            # Subject Case Report Form (CRF)
        │    └── CB036_EXP1_EXQU.json           # Subject Exit Questionnaire responses
        ├── CB036_EXP1_BEH/                     # Behavioral Events data collected during EXP1
        ├── CB036_EXP1_LPTTriggers/             # Trigger data for synchronization
        ├── CB036_EXP1_MEEG/                    # MEEG data collected during EXP1 (fif)
        ├── CB036_EXP1_ET/                      # Eye Tracking data collected during EXP1 (asc)
        ├── CB036_RestinEO_MEEG/                # MEEG data collected during RestingEO task (fif)
        ├── CB036_RestinEO_ET/                  # Eye Tracking data collected during RestingEO task 
        ├── CB036_Rnoise_MEEG/                  # MEEG data collected during Rnoise task (fif)
        └── CB036__MR/                          # MR anatomical scan data (fif)
```

### Raw iEEG Data Directory Structure

```bash
COG_ECOG_EXP1_RELEASE/				            # Experiment modality top level folder
    ├── metadata/				                # Experiment modality level metadata folder
    │    ├── devices_ECOG.json			        # List of devices used to collect the data
    │    ├── protocols_ECOG.json		        # A link to the Standard Operating Procedure (SOP) document used for the data collection
    │	 ├── subjects_demographics_ECOG.json    # Full set of experiment modality subjects with their respective demographic information
    │    ├── tasks_EXP1.json                    # Description of the 1st Cogitate task 
    │    ├── tasks_FingerLoc.json               # Description of the Finger Localizer task
    │    └── wirings_ECOG.pdf			        # Wiring pdf file showing how the devices described in devices_ECOG.json  are connected to each other
    └── CE103                                   # Subject folder
        ├──metadata/                            # Subject level metadata folder
        │    ├── CE103_EXP1_CRF.json            # Subject Case Report Form (CRF) 
        │    └── CE103_EXP1_EXQU.json           # Subject Exit Questionnaire responses
        ├── CE103_EXP1_BEH/                     # Behavioral Events data collected during EXP1
        ├── CE103_EXP1_ECOG/                    # ECOG data files collected during EXP1
        ├── CE103_EXP1_ET/                      # Eye Tracking data collected during EXP1
        ├── CE103_FingerLoc_ECOG/       	    # Ecog data collected during the Finger Localizer task
        ├── CE103_FingerLoc_BEH/                # Behavioral event data collected during the Finger Localizer task
        ├── CE103__CT/                          # CT scan data (no task)
        ├── CE103__MR/                          # MR anatomical data
        └── CE103__ElecCoords/			        # Contains coordinate output files of MR/CT coregistration end electrode reconstruction pipeline
```

## BIDS Format

The BIDS (Brain Imaging Data Structure) file structure for M-EEG (Magnetoencephalography) and iEEG (intracranial EEG) data adheres to a standardized format for organizing neuroimaging data. Each file follows a structured naming convention indicating subject, session, task, and data type. Here's a breakdown of the key elements within each modality's data directory structure:
- dataset_description.json: Provides general information about the dataset.
- participants.json and participants.tsv: Contain demographic information about subjects.
- README.md: Offers an overview of the data and BIDS format.
- Subject-specific data: Organized under sub-[SubjectID]/.
- Session-specific data: Organized under ses-[SessionID]/.
- Anatomical and functional data: Stored in appropriate folders (anat/ for anatomical, meg/ for MEG, and ieeg/ for iEEG).
- Metadata: Related to subjects and experiments is stored in metadata/ directories.

This structured approach ensures clarity and consistency in data organization, facilitating ease of access and analysis for researchers and collaborators.

### BIDS M-EEG Data Directory Structure

```bash
COG_MEEG_EXP1_BIDS_RELEASE/
|-- dataset_description.json                                  # General information about BIDS version, type of dataset, Authors, Acknowledgments, Funding, Ethics Approvals, and the link of COGITATE website 
|-- derivatives                                               # Including metadata and coreg (coregistration)
|   |-- additional_metadata                                   # Containing all of the metadata
|   |   |-- dataset_description.json                          # General information about BIDS version, type of dataset
|   |   |-- METADATA                                          # Including metadata including the list of devices, link to COGITATE GitHub repository, types of tasks, stimuli and responses and wiring diagram of MEG data 
|   |   |   |-- analysis.json                                 # Analysis steps, the order of them and the link of analysis code repository
|   |   |   |-- devices_MEEG.json                             # List of devices used for MEG data acquisition
|   |   |   |-- protocols.json                                # Link of COGITATE wiki and MEG SOP
|   |   |   |-- tasks_EXP1_MEEG.json                          # Description of behavioral task, stimuli and responses
|   |   |   |-- tasks_RestinEO_MEEG.json                      # Description of resting-state task and type of the response
|   |   |   |-- tasks_Rnoise_MEEG.json                        # Description of empty room task
|   |   |   `-- wiring_MEEG.pdf                               # Wiring diagram of MEG
|   |   |-- README.md                                         # Containing an explanation about additional_metadata directory
|   |   |-- sub-CA103                                         # Subject folder
|   |   |   `-- METADATA                                      # Containing Case Report Form, Exit Questionnaire and subject’s demography 
|   |   |       |-- CA103_CRF.json                            # Case Report Form
|   |   |       |-- CA103_demographics.json                   # Subject’s demography
|   |   |       `-- CA103_EXQU.json                           # Exit Questionnaire

|   `-- coreg                                                 # The results of the coregistration
|       |-- dataset_description.json                          # BIDS version, Data Type, and description of the files of this directory
|       |-- README.md                               
|       |-- sub-CA103                                         # Subject folder
|       |   `-- ses-1                                         # Session 1/visit 1
|       |       `-- meg                                       # MEG folder
|       |           `-- sub-CA103_ses-1_trans.fif             # The output of coregistering MEG sensors and head to the anatomical data
|-- participants.json                                         # General information about subjects’ demography
|-- participants.tsv                                          # Subjects’ demography in tsv format
|-- README.md                                                 # Overview of MEG data and the BIDS format
|-- sub-CA103                                                 # Subject folder
|   `-- ses-1                                                 # Session 1/visit 1
|       |-- anat                                              # Folder of anatomical data
|       |   |-- sub-CA103_ses-1_T1w.json                      # Anatomical landmark coordinates
|       |   `-- sub-CA103_ses-1_T1w.nii.gz                    # Anatomical data
|       |-- meg                                               # Folder of MEG data
|       |   |-- sub-CA103_ses-1_acq-calibration_meg.dat       # Calibration data
|       |   |-- sub-CA103_ses-1_acq-crosstalk_meg.fif         # Crosstalk data
|       |   |-- sub-CA103_ses-1_coordsystem.json              # Including Information about MEG and head coil and coordinate system, units, description and anatomical landmark coordinates
|       |   |-- sub-CA103_ses-1_task-dur_run-01_channels.tsv  # Contains information on the channel names, types, units, sampling rate, status, and frequency cutoffs of the filter applied to the recorded data during run 1
|       |   |-- sub-CA103_ses-1_task-dur_run-01_events.json   # Description of sample, value and trial type    
|       |   |-- sub-CA103_ses-1_task-dur_run-01_events.tsv    # Contains information about the events/stimuli presented during Experiment 1, run 1, event’s onset time and duration, type of event, event code (trigger code) and sample
|       |   |-- sub-CA103_ses-1_task-dur_run-01_meg.fif       # Contains the raw/unprocessed MEG data during the task of Experiment 1/session 1, run 1
|       |   |-- sub-CA103_ses-1_task-dur_run-01_meg.json      # Contains power line and sampling frequencies, duration of recording, MEG, EOG and ECG and trigger channel counts during run 1
|       |   |-- sub-CA103_ses-1_task-dur_run-02_channels.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-02_events.json
|       |   |-- sub-CA103_ses-1_task-dur_run-02_events.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-02_meg.fif
|       |   |-- sub-CA103_ses-1_task-dur_run-02_meg.json
|       |   |-- sub-CA103_ses-1_task-dur_run-03_channels.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-03_events.json
|       |   |-- sub-CA103_ses-1_task-dur_run-03_events.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-03_meg.fif
|       |   |-- sub-CA103_ses-1_task-dur_run-03_meg.json
|       |   |-- sub-CA103_ses-1_task-dur_run-04_channels.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-04_events.json
|       |   |-- sub-CA103_ses-1_task-dur_run-04_events.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-04_meg.fif
|       |   |-- sub-CA103_ses-1_task-dur_run-04_meg.json
|       |   |-- sub-CA103_ses-1_task-dur_run-05_channels.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-05_events.json
|       |   |-- sub-CA103_ses-1_task-dur_run-05_events.tsv
|       |   |-- sub-CA103_ses-1_task-dur_run-05_meg.fif
|       |   |-- sub-CA103_ses-1_task-dur_run-05_meg.json
|       |   |-- sub-CA103_ses-1_task-noise_channels.tsv       # Contains information on the channel names, types, units, sampling rate, status, and frequency cutoffs of the filter applied to the recorded data during noise recording
|       |   |-- sub-CA103_ses-1_task-noise_meg.fif            # Contains the raw/unprocessed MEG data during noise recording of Experiment 1/session 1
|       |   |-- sub-CA103_ses-1_task-noise_meg.json           # Contains power line and sampling frequencies, duration of recording, MEG, EOG and ECG and trigger channel counts during noise recording
|       |   |-- sub-CA103_ses-1_task-rest_channels.tsv        # Contains information on the channel names, types, units, sampling rate, status, and frequency cutoffs of the filter applied to the recorded data during resting-state recording
|       |   |-- sub-CA103_ses-1_task-rest_meg.fif             # Contains the raw/unprocessed MEG data during resting-state recording of Experiment 1/session 1
|       |   `-- sub-CA103_ses-1_task-rest_meg.json            # Contains power line and sampling frequencies, duration of recording, MEG, EOG and ECG and trigger channel counts during resting-state recording            
|       `-- sub-CA103_ses-1_scans.tsv                         # List of MEG data files
```

### BIDS iEEG Data Directory Structure

```bash
COG_ECOG_EXP1_BIDS_RELEASE/
|-- dataset_description.json						                # General information about BIDS version, type of dataset, Authors, Acknowledgments, Funding, Ethics Approvals, and the link of COGITATE website
|-- derivatives								                        # Directory containing derived data
|   |-- additional_metadata						                    # Containing all of the metadata and CT scans
|   |   |-- dataset_description.json					            # General information about BIDS version, type of dataset and list of metadata
|   |   |-- METADATA							                    # Metadata folder
|   |   |   |-- analysis.json						                # Analysis steps, the order of them and the link of analysis code repository
|   |   |   |-- devices_ECOG.json					                # List of devices used for iEEG data acquisition
|   |   |   |-- manifest.json						                # List of all MR and CT datasets
|   |   |   |-- protocols.json						                # Link of COGITATE wiki
|   |   |   |-- tasks_EXP1_ECOG.json					            # Description of behavioral task, stimuli and responses
|   |   |   |-- tasks_FingerLoc_ECOG.json				            # Description of Finger Localizer task, stimuli and responses
|   |   |   `-- wiring_ECOG.pdf						                # Wiring diagram of iEEG
|   |   |-- README.md							                    # Containing an explanation about additional_metadata directory
|   |   |-- sub-CF102							                    # Subject folder
|   |   |   `-- METADATA						                    # Metadata folder
|   |   |       |-- CF102_CRF.json					                # Case Report Form
|   |   |       |-- CF102_demographics.json				            # Subject’s demography
|   |   |       `-- CF102_EXQU.json					                # Exit Questionnaire
|   `-- ct								                            # CT scans folder
|       |-- dataset_description.json					            # General information about BIDS version and format of CT scans
|       |-- README.md							                    # Containing an explanation about ct folder
|       |-- sub-CF102							                    # Subject folder
|       |   `-- ses-1							                    # Session 1/visit 1
|       |       `-- anat						                    # Folder of CT data
|       |           `-- sub-CF102_ses-1_ct.nii.gz			        # CT data
|-- participants_epilepsy.json						                # Contains descriptions of additional metadata including electrode implantation, seizure classification, IQ scores, auditory capabilities, seizure frequency, surgical history, MRI findings, and family medical history
|-- participants_epilepsy.tsv						                # Contains additional metadata including electrode implantation, seizure classification, IQ scores, auditory capabilities, seizure frequency, surgical history, MRI findings, and family medical history
|-- participants.json							                    # Contains descriptions of metadata including biological sex, age, handedness, weight, height, primary and secondary languages, ethnicity, education level, colorblindness status, visual correction method, eye dominance, eye chart test results, and strength of visual correction in diopters
|-- participants.tsv							                    # Contains metadata including biological sex, age, handedness, weight, height, primary and secondary languages, ethnicity, education level, colorblindness status, visual correction method, eye dominance, eye chart test results, and strength of visual correction in diopters.
|-- README.md								                        # Overview of iEEG data, the BIDS format and description of the contents of the dataset
|-- sub-CF102								                        # Subject folder
|   `-- ses-1								                        # Session 1/visit 1
|       |-- anat							                        # Folder of MR anatomical data
|       |   `-- sub-CF102_ses-1_T1w.nii.gz				            # MR anatomical data
|       |-- ieeg							                        # Folder of iEEG data
|       |   |-- sub-CF102_ses-1_atlas-desikan_labels.json		    # Contains descriptions about _ses-1_atlas-desikan_labels.tsv file
|       |   |-- sub-CF102_ses-1_atlas-desikan_labels.tsv		    # Contains electrode labels obtained from the Desikan atlas using mne.get_montage_volume_labels, along with the electrode coordinates in the subject's native T1 space
|       |   |-- sub-CF102_ses-1_atlas-destrieux_labels.json		    # Contains descriptions about _ses-1_atlas-destrieux_labels.tsv file
|       |   |-- sub-CF102_ses-1_atlas-destrieux_labels.tsv		    # Contains electrode labels obtained from the Destrieux atlas using mne.get_montage_volume_labels, along with the electrode coordinates in the subject's native T1 space
|       |   |-- sub-CF102_ses-1_laplace_mapping_ieeg.json		    # Contains referencing scheme of the electrodes
|       |   |-- sub-CF102_ses-1_space-fsaverage_coordsystem.json	# Contains the x y z coordinates of the channels
|       |   |-- sub-CF102_ses-1_space-fsaverage_electrodes.tsv		# Contains electrodes’ coordinates in fsaverage space
|       |   |-- sub-CF102_ses-1_task-Dur_channels.tsv		        # Contains information about the channel types (which channel is seeg, ecog...)
|       |   |-- sub-CF102_ses-1_task-Dur_events.json
|       |   |-- sub-CF102_ses-1_task-Dur_events.tsv			        # Contains the events timestamps, duration and descriptions aligned in the edf timeline. This file was generated by parsing the photodiode trigger and combining the photodiode time stamps with the log files information
|       |   |-- sub-CF102_ses-1_task-Dur_ieeg.eeg			        # Raw EEG data file
|       |   |-- sub-CF102_ses-1_task-Dur_ieeg.json
|       |   |-- sub-CF102_ses-1_task-Dur_ieeg.vhdr			        # Header file - Contains recording parameters and further meta-information		
|       |   `-- sub-CF102_ses-1_task-Dur_ieeg.vmrk			        # Marker file - Contains description of the event collected during the data recording
|       `-- sub-CF102_ses-1_scans.tsv					            # Time of acquisition
```

   </td>
  </tr>
