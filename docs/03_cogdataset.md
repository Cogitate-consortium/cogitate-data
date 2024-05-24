# COGITATE Dataset

The COGITATE dataset is a comprehensive collection of multimodal neuroimaging data, encompassing a total of 262 subjects. COGITATE employs three distinct neuroimaging techniques: fMRI, M-EEG, and iEEG/ECoG.

![Cogitate overview map](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/overview_map.png)

The MEG modality comprised 102 healthy subjects, also above the age of 18, with no known psychiatric or neurological issues. These participants were sourced from the Centre for Human Brain Health at the University of Birmingham (Birmingham, United Kingdom) and the Center for MRI Research of Peking University (Beijing, China).

Similarly, the fMRI modality included 122 healthy volunteers, all of whom were above the age of 18 and predominantly right-handed. These participants had no known history of psychiatric or neurological disorders and were recruited from the Yale Magnetic Resonance Research Center (New Haven, CT, United States) and the Donders Centre for Cognitive Neuroimaging (Nijmegen, Netherlands).

In contrast, the iEEG modality involved a more specialized cohort of 38 patients diagnosed with pharmaco-resistant focal epilepsy. These participants ranged in age from 10 to 65 years, had an IQ above 70, and met specific health criteria. They were recruited from multiple medical centers specializing in epilepsy treatment, including the Comprehensive Epilepsy Center at New York University (New York, NY, United States), Brigham and Women’s Hospital, Boston Children’s Hospital (Boston, MA, United States), and the University of Wisconsin School of Medicine and Public Health (Madison, WI, United States).

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/age%20histograms%20across%20modalities_2024-04-26_v1.1.png" alt="Age histograms across modalities">
  <p>Age histograms across modalities</p>
</div>

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/sex%20proportions%20across%20modalities_2024-04-26_v1.1.png" alt="Sex proportions across modalities">
  <p>Sex proportions across modalities</p>
</div>

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/handedness%20proportions%20across%20modalities_2024-04-26_v1.1.png" alt="Handedness proportions across modalities">
  <p>Handedness proportions across modalities</p>
</div>

## Demography of Subjects

You can find the profile of participants for all modalities at [subjects_demography](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/linked_files_v1.1/subjects_demography-EXP1-released-data_2024-04-026_v1.1.xlsx). Here is a brief explanation about the information collected from the subjects.

### **Demographic Information for M-EEG**

The below items are included in the subjects’ demography for M-EEG modality:

Participant_ID (participant identifier), sex (biological sex of participant), age (age of participant at the time of testing), handedness (right, left or ambidextrous), included in [MSP](https://doi.org/10.1371/journal.pone.0268577) (whether the data was used for the experiments or not), phase\* (determining in which stage the data is, phase 2/phaseII (optimization) or phase 3/phaseIII (replication)), QC\** status (passed/not), if Not (in QC status) QC rejection reason, weight (weight of participant at the time of study in pounds), height (height of participant at the time of study in inches), primary and secondary language, race (ethnicity of the participant), education, compensation (whether the subject was paid or not), colorblind (determining whether the subject can distinguish the colors and perceiving them correctly or not), visual correction (none or using any glasses or contact lenses), eye dominance (which eye is dominant), eye chart results (the outcome of a visual acuity test performed using the eye chart) and dioptry (visual acuity of the participant in Diopters).

\***Phase:** COGITATE project has three phases. In **phase 1**, all data were acquired by theory neutral teams. To ensure replicability of the results, the entire dataset was split into two halves, each with an equal mixture of data from each of the labs for each modality. In **phase 2**, after evaluating data quality, the first half of the data were used for developing analysis tools (optimization of methods). The purpose of **phase 2** was to define the best analysis practices and to agree upon, in consultation with expert advisors. In **phase 3**, the replication phase, the second half of the data were analyzed using the concurred procedure, agreed upon protocols, thereby allowing an in-house replication of the results obtained in phase 2.

\****QC (quality control):** A number of items were checked for all the data of each modality which are elaborated in the section of [Quality Check](#quality-check) and [Exclusion Criteria](#exclusion-criteria).

### **Demographic Information for fMRI**

All of the items are similar to the M-EEG modality.

### **Demographic Information for iEEG**

In addition to the properties mentioned for M-EEG modality, the below parameters were also provided for this modality:

Electrode scheme (the scheme used for implanting the electrodes, Stereo, Subdural grid & Strips), number of implanted electrodes, implant hemisphere (brain hemisphere where the electrodes implanted, right, left, both or bilateral), IQ (score and name of the test used for assessment (FSIQ, WISC, VCI, POI, WMI, PSI, AMI, VMI), WADA (intracarotid sodium amobarbital, a test that determines which side of the subject’s brain controls language and memory functions), seizure type (classification of seizure type), age of onset (age at which the first symptoms of seizure appeared), auditory normal hearing (indicator of whether the participant had normal hearing capabilities, yes or no), epilepsy seizure classification (categorization of epilepsy as per standard seizure classification), epilepsy seizure aura (description of any sensory or perceptual symptoms before a seizure occured), epilepsy seizure semiology (signs and symptoms exhibited during epileptic seizures), epilepsy seizure frequency (frequency of seizures experienced by participant), epilepsy post ictal semiology (symptoms and signs after an epileptic seizure), epilepsy trigger (identified factors or circumstances that increased the likelihood of experiencing a seizure), epilepsy duration uncontrolled (the duration that seizures had not been successfully managed or medically controlled), epilepsy seizure onset zone (brain region identified as the initial site of seizure activity), epilepsy resection (details of any surgical resection performed for seizure control), epilepsy language lateralization (determination of the dominant hemisphere for language function), epilepsy past surgical history (record of any previous surgeries related to the treatment of epilepsy), epilepsy past medical history (medical history relevant to epilepsy diagnosis and treatment), epilepsy family history (presence of seizure or epilepsy disorders in family members), other neurological disorders (any other diagnosed neurological disorders besides epilepsy), epilepsy MRI findings (summary of MRI findings relevant to epilepsy diagnosis), epilepsy pathology findings (pathological findings from tissue analysis post-surgery or biopsy).

#### Quality Check

Data from all modalities were checked at three levels. The first level checks tested whether the datasets  contained  all  expected  files  keeping  their  naming  conventions,  and  that  all  personal information had been removed. The second level checks tested subjects’ performance with respect to behavior. For [Experiment 1](02_overview.md#experiment-1-conscious-perception), subjects were excluded if their hit rate (Hit) was lower than 80% or false alarm (FA) was higher than 20% for M-EEG and fMRI, and for iEEG, a more relaxed criteria of 70% Hits and 30% FAs was used. Two M-EEG subjects were excluded due to low hit rates and one iEEG patient was excluded due to high FAs. The  third  level  checks  assessed  the  quality  of  the  neural  data.

#### Exclusion Criteria

The generic exclusion criteria used across [Experiment 1](02_overview.md#experiment-1-conscious-perception) and [Experiment 2](02_overview.md#experiment-2-video-game-engagement) included: (a) insufficient number of trials in each of the experimental conditions (&lt;30 for M-EEG or &lt;20 for fMRI), due to excessive muscular artifacts, movement, noisy recording, or subjects deciding to stop the experiments. If a given  analysis  showed  that  a  good  enough  signal  could  be  obtained  with  fewer  trials,  these numbers were amended; and (b) low performance in the attention tasks. In [Experiment 1](02_overview.md#experiment-1-conscious-perception), this translates into: &lt;80% Hits, >20% FAs for fMRI and M-EEG subjects; &lt;70% Hits, >30% FAs for iEEG patients. In addition, data was excluded from analysis if it did not pass any of the predefined data quality checks.

## Description of COGITATE Data

Although our data collection had a specific purpose, the data we gathered holds potential value for a range of diverse inquiries. Consequently, the COGITATE consortium has chosen to openly share all raw data collected (including the data that did not pass the quality criteria), to facilitate its utilization for various research endeavors and promote data reusability.

We have made available two primary formats for the data acquired during the experimental phase of the COGITATE project, specifically [Experiment 1](02_overview.md#experiment-1-conscious-perception):

1. Unprocessed/Raw Data
2. BIDS Format

### **1. Unprocessed/Raw Data**

The unprocessed data format closely resembles the original acquired data, having undergone minimal processing to ensure compliance with [GDPR](https://gdpr-info.eu) (General Data Protection Regulation)/[HIPAA](https://www.hhs.gov/hipaa/for-professionals/compliance-enforcement/index.html) (Health Insurance Portability & Accountability Act) anonymity standards.

### **2. BIDS Format**

BIDS format, widely adopted in cognitive neuroscience, enhances data reusability. To facilitate others in leveraging our data, we have released it in [BIDS](https://bids-specification.readthedocs.io/en/stable/) format.

### **File Type Glossary**

Here are the various file formats used for each modality of the COGITATE dataset along with a short description of them.

#### **Eye Tracking & Behavioral Data**

- **Unprocessed/Raw release format**
        - Filetype: ASC/CSV
- **BIDS Format**
        - Filetype: ASC/CSV

The two eye trackers used within COGITATE are:
<br>1. EyeLink eye tracker
<br>2. Tobii eye tracker

**1) EyeLink eye tracker**: Most of the sites used this eye tracker which produces data in the EDF format, EyeLink Data Format. This data was immediately converted to ASCII text files using the converter provided by Eyelink. This is the ASC files that we used in our data.

**2) Tobii eye tracker**: The other eye tracker was the Tobii eye tracker used by New York University Langone for ECOG data. This eye tracker produces data in the form of CSV files.
<br>The files generated by eye tracking systems, containing information about eye movement and gaze behavior which typically store a time-stamped sequence of gaze data points and include information such as:

1. Timestamps: The exact time at which each gaze data point was recorded.
2. Gaze Coordinates: The x and y coordinates on the screen where the person's gaze is directed.
3. Pupil Diameter: The size of the person's pupil, which can provide insights into changes in visual processing or cognitive load.
4. Fixations: Periods of stable gaze where the person is looking at a specific point without significant movement.
5. Saccades: Rapid eye movements between fixations, indicating shifts in attention.
6. Blinks: Instances when the person's eyes are closed, which can be important for data cleaning and analysis.

Behavioral data is available in CSV format and it provides below information:

1. Blocks
2. Events
3. Trials
4. Stimulus and jitter duration
5. Subject's responses

#### **M-EEG Data**

- **Unprocessed/Raw release format**
      - Filetype: FIF

- **BIDS Format**
      - Filetype: FIF

File Format for the Input and Output of MEG and EEG data

FIF files contain various types of information related to neuroimaging data, including:

1. Raw sensor data: MEG and EEG measurements recorded from sensors placed on the scalp or near the head.
2. Event information: Time-stamped triggers or markers indicating the timing of events, such as stimulus presentations or subject responses.
3. Sensor locations and orientations: Information about the physical positions and orientations of sensors used in the measurements.
4. Head geometry: Information about the shape and structure of the subject's head, which is crucial for accurate source localization.
5. Covariance matrices: Statistical information about the relationships between sensor measurements at different time points or frequencies.
6. Anatomical MRI data: High-resolution structural images of the subject's brain, used for source localization and spatial alignment.

#### **iEEG/ECoG Data**

- **Unprocessed/Raw release format**
      - Filetype: EDF

- **BIDS Format**
      - Filetype: [BrainVision](https://www.brainproducts.com/support-resources/brainvision-core-data-format-1-0/)

European Data Format files used for storing and exchanging time-series biological and physiological data

EDF files are designed to accommodate data from multiple channels, allowing researchers to store and manage data collected simultaneously from different sensors or electrodes. The format supports both raw signal data and associated metadata, including information about sampling rates, units of measurement, patient demographics, and recording conditions.

The [BrainVision](https://www.brainproducts.com/support-resources/brainvision-core-data-format-1-0/) format, often shortened to BV, is a widely employed file format in neuroscience research, specifically designed for organizing neurophysiological data. It comprises several files, including the header file (.vhdr), marker file (.vmrk), and raw EEG data file (*.eeg), alongside possible auxiliary files. These components store essential details like recording parameters, event markers, and the raw EEG data.

#### **MR/CT Data**

- **Unprocessed/Raw release format**
      - Filetype: DICOM/NIFTI

- **BIDS Format**
      - Filetype: DICOM/NIFTI

DICOM (.dcm file extension) is a standard format utilized for storing CT (Computed Tomography) scans and MRI (Magnetic Resonance Imaging) data. These files encompass not only the image data but also essential metadata, including imaging parameters.

NIFTI (.nii.gz file extension) serves as another format employed for a subset of subjects where our standard procedure encountered challenges. With the exception of the MR and CT scans for 12 subjects within the iEEG data, all other datasets of similar nature are stored in DICOM format. Further details regarding these 12 problematic datasets are available in [this section](04_data.md#deviations-from-data-curation-procedure). NIFTI files encapsulate image data alongside metadata concerning spatial orientation, voxel dimensions, and additional imaging parameters.

## Data Acquisition

The Cogitate dataset encompasses three distinct neuroimaging modalities, along with synchronized eye-tracking and behavioral data linked to each of these modalities. Here we detail the acquisition protocol for each modality in the corresponding data release: M-EEG, iEEG

### Stimuli

Stimuli belonged to four categories that naturally fell into two groups that were clearly distinct from each other: pictures (20 faces and 20 objects) and symbols (20 letters and 20 false-fonts). Face stimuli were created using the FaceGen Modeler 3.1 program and object stimuli were taken from the Object Databank (Tarr, 1996). Faces and objects were grey-scaled (RGB: 125, 125, 125), and manipulated to have similar size and equal luminance using the SHINE toolbox (Willenbockel et al., 2010). Equal proportions of male and female faces were presented. They all had hair and belonged to different ethnicities (e.g., Caucasian, Asian, African, American) to facilitate face individuation. The orientation of the stimuli was manipulated, such that half of the stimuli from each category had a side view and the other half a front view. All letter stimuli and false fonts were generated with MAXON CINEMA 4D Studio (RC-R20) 20.059 on macOS 10.14, appearing in gray (RGB: 125, 125, 125). Three views were rendered for each font set (real font, false/pseudo font) at 0°, 30° and -30° horizontal viewing angle with the following settings: Extrusion depth 9.79% of character height, camera distance 5.65 times character height and 18° above the center of the letter (High Angle), with a simulated focal length of 135 mm (35 mm equiv.). All stimuli were presented on a rectangular aperture at an average visual angle of 6 ̊ by 6 ̊.

### Procedure

Stimuli were presented sequentially, all supra-threshold, with half being task-relevant and the other half task-irrelevant. Only one stimulus was shown on the screen at any given time. To define task relevance, subjects were instructed to detect (press a button; non-speeded response) two targets from different categories, regardless of their orientation. This online reporting enabled an explicit assessment of subjects’ performance, engaging report-related areas for later analysis. Each block began with notification of the two target stimuli, either pictorial (faces and objects) or symbolic (letters and false fonts), creating a clear distinction between relevant and irrelevant stimuli. At the start of each block, specific target stimuli were revealed with instructions such as “detect face A and object B” or "detect letter C and false-font D." Targets did not repeat across blocks. Each run included two blocks of the Face/Object task and two blocks of the Letter/False-font task, with the order counterbalanced across runs. Subjects were instructed to maintain central fixation throughout each trial. Gaze was monitored online through an eye tracker, with repeated calibrations ensuring good quality data.

Each block comprised stimuli from all four categories, with each stimulus displayed for 500, 1000, or 1500 ms, followed by a blank interval, ensuring a consistent trial duration of 2000 ms. To  avoid  periodic  presentation  of  the  stimuli, random jitter was added to the end of each trial (mean inter-trial interval of 400 ms, jittered 200-2000 ms, with truncated  exponential  distribution). Within each block, three trial types were presented: i) Task Relevant Targets, consisting of the specific stimuli participants were tasked with detecting; ii) Task Relevant Non-Targets, encompassing stimuli from relevant categories that were not designated targets; and iii) Task Irrelevant Stimuli, comprising stimuli from the remaining categories.

#### iEEG related modifications of the design
Only half of the stimuli were used as targets for the iEEG experiments. The selection of target faces kept the balance of gender and ethnicity. Letters were chosen in equal amounts from the first and second parts of the alphabet, and the corresponding false-fonts were used. All stimuli were presented as relevant non-targets and irrelevant stimuli, matching the designs of the aforementioned procedure.

### M-EEG Data Acquisition

M-EEG recordings were acquired at the Centre for Human Brain Health (CHBH) of University of Birmingham in the United Kingdom, and at the Center for MRI Research of Peking University (PKU) in China.

#### Hardware

Both centers had a 306-channel, whole-head TRIUX MEG system from MEGIN (York Instruments; formerly Elekta). The MEG system comprised 204 planar gradiometers and 102 magnetometers in a helmet-shaped array. Simultaneous EEG was recorded using an integrated EEG system and a 64-channel electrode cap. The MEG system was equipped with a zero boil-off Helium recycling system and the noise-resilient ARMOR sensors and placed in a shielded room (2 layers of mu-metal and 1 layer of aluminum). To reduce environmental noise, the integrated active shielding system was used at PKU. In order to cover the brain more homogeneously, the MEG gantry was positioned at 68 degrees.

#### Location of Electrodes and ECG/EOG Measurements

The location of the fiducials, the positions of the 64 EEG electrodes and the participant’s head shape were recorded using a 3-D digitizer system (Polhemus Isotrak). A set of bipolar electrodes were placed on the subject’s chest (upper left and upper right chest position) to record the cardiac signal (ECG). Two sets of bipolar electrodes were placed around the eyes (two located at the outer canthi of the right and left eyes and two above and below the center of the right eye) to record eye movements and blinks (EOG). Ground and reference electrodes were placed on the back of the neck and on the right cheek, respectively. The impedance of all of the electrodes was checked to be below 10 kOhm.

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/eog_ecg_electrodes_meg.png" alt="Standard Locations of EOG and ECG electrodes">
  <p>Standard Locations of EOG and ECG electrodes</p>
</div>

#### Head Position Indicator (HPI) Coils

The participant’s head position inside the MEG system was measured at the beginning and at the end of each run using four head position indicator (HPI) coils placed on the EEG cap. Specifically, the HPI coils were placed next to the left and right mastoids and on the left and right forehead. Their location relative to anatomical landmarks was digitized with a Polhemus Isotrak System. During the measurement, high frequency (>200 Hz) signals were produced by those coils and the localization of these signals was used to estimate the head position in the sensor space. To avoid the potential artifacts produced by the non-linear interaction between the signals generated by these coils, head position measurement was performed only during resting periods (as opposed to continuously).

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/hpi_coils_meg.png">
  <p>Standard locations of HPI coils. Coil Numbers: 1. Blue, 2. White, 3. Red, 4. Black, 5. Yellow</p>
</div>

#### Anatomical MRI Data Acquisition

For each subject, a high resolution T1-weighted MRI volume (3T Siemens MRI Prisma scanner) was acquired. At CHBH, a 32-channel coil with a resolution of 1 x 1 x 1 mm, TR/TE = 2000/2.03ms; TI = 880 ms; 8° flip angle, 208 sagittal slices and field of view (FOV): 256 x 256 matrix was acquired for source localization with individual realistic head modeling. At PKU, a 64-channel coil with a resolution of 0.5 x 0.5 x 1 mm, TR/TE = 2530/2.98ms; TI = 1100 ms; 7° flip angle, 192 sagittal slices; FOV: 448 × 512 matrix was used. To avoid possible interference of body magnetization on the MEG recording, all MRI scans were acquired at least one week before the MEG session, or at any time afterwards. The FreeSurfer standard template was used (fsaverage) for participants lacking an anatomical scan (N=5).

#### Behavioral Data Acquisition

The task was executed using Matlab (CHBH: R2019b, PKU: R2018b) with Psychtoolbox v.3 (Pelli, 1997) on a custom PC at CHBH and a Dell XPS desktop PC at PKU. Visual stimuli were presented on a screen placed in front of the subjects with a PROPixx DLP LED projector (VPixx Technologies Inc.) at a resolution of 1920 x 1080 pixels and a refresh rate of 120 Hz. The distance between the subject’s eyes and the screen was different at each site (CHBH: 119 cm, PKU: 85 cm) to achieve the same FOV of 36.6 x 21.2 degrees. Participants responded with both hands using two 5-button response boxes (CHBH: NAtA, PKU: SINORAD).

#### Eye Tracking Data Acquisition

Eye movements were monitored and recorded from both eyes (binocular eye-tracking) using the MEG-compatible EyeLink 1000 Plus eye-tracker (SR Research Ltd., Ottawa, Canada). Nine-point calibration was performed at the beginning of the experiment, and recalibrated if necessary at the beginning of each block/word. Pupil size and corneal reflection data were collected at a sampling rate of 1000 Hz.

#### Behavioral Data Code Scheme

Stimuli are coded as a 4-digit number.  
1st digit = stimulus type (1 = face; 2 = object; 3 = letter; 4 = false font)  
2nd digit = stimulus orientation (1 = center; 2 = left; 3 = right)  
3rd & 4th digits = stimulus id (1...20; for faces 1...10 is male, 11...20 is female)  

e.g., "1219" = 1 is face, 2 is left orientation and 19 is a female stimulus #19

#### Eye Tracker and MEG Code Scheme

The channel name that contains the eye tracker data in the FIF file is as follows: MISC1 (X), MISC2 (Y), and MISC3 (pupil)

##### **Defining some terms**

**Trial**: Stimulus presentation followed by a fixation (the two add up to 2 sec) followed by a jitter of 200 msec to 2000 ms.

**Mini block**: presentation of 34 to 38 stimuli, in the beginning of which the target stimuli were presented.

**Block**: composed of 4 mini blocks. At the end of each block, there was a break.

**Break**: Pause between 2 blocks

##### **Successive trigger scheme**

The triggers were sent successively. The first trigger represented the stimulus type, followed by orientation, stimulus duration, and task relevance, all interspaced by 50 ms. Additionally, a trigger was sent upon key press.

##### **1st Trigger (on Stimulus Onset): Stimulus Type**

- 1 to 20: faces
        - 1 to 10 males,
        - 11 to 20 females
- 21 to 40: objects
- 41 to 60: letters
- 61 to 80: falses

##### **2nd Trigger (2 Frames after Stimulus Onset): Stimulus Orientation**

- 101: Center
- 102: Left
- 103: Right

##### **3rd Trigger (4 Frames after Stimulus Onset): Stimulus Duration**

- 151: 500 msec
- 152: 1000 msec
- 153: 1500 msec

##### **4th Trigger (6 Frames after Stimulus Onset): Stimulus Task Relevance**

- 201: Task relevant target
- 202: Task relevant non target
- 203: Task irrelevant

##### **5th Trigger (8 Frames after Stimulus Onset): Trial ID Triggers**

- 111-148: Trial number

##### **Response Trigger**

- 255: Following button press.

##### **Stimulus Presentation End**

- 96: Offset of stimulus presentation (onset of blank)
- 97: Offset of blank (onset of jitter period)
      - Note that both these are fixations, they are just divided into blank and jitter.

##### **General Triggers to Mark Experiment Progression**

86: Onset of experiment  
81: Onset of recording  
83: Offset of recording

##### **Miniblock ID Triggers**

161-200: Miniblock ID trigger

##### **Zeroes**

0: Zeros were sent between the successive triggers to reset the LPT, see below. These were also sent to the eye tracker but did not mean anything and they can safely be ignored.

##### **How The LPT Triggers Were Sent**

The LPT port of the computer was used for sending the triggers and it was done by using the sendTrig function. This function sets the port in a specific state (whatever trigger we want to send) and logs the trigger afterwards, noting if it is sent and what time the command for sending it is executed. For each trigger that is being sent, the port is being reset after a frame to 0.

In the beginning of the experiment, a few triggers were sent to mark experiment onset and onset of recording. Then, a mini block was initiated. The participant was presented with the target screen and required to press the spacebar to proceed. When the participant pressed the space button, the miniblock ID was sent. Only once the miniblock trigger was sent the fixation appeared. This means that there was a small delay between key press and fixation onset. Following the first fixation, a jitter started, which was also logged. Then, the first stimulus was displayed. Upon the presentation of the stimulus, the successive triggers were initiated. The first trigger occurred directly after the onset of the stimulus, indicating the stimulus ID (1-80). Then, after 2 frames, the orientation trigger (101-103) was sent, followed by the duration trigger (151 to 153) at 4 frames, the task demand trigger (201-203) at 6 frames, and finally, the trial ID trigger (111 to 148) at 8 frames.

#### Empty Room Recording

Prior to each experiment, MEG signals from the empty room were recorded for 3-minutes.

#### Resting-State (rM-EEG)

The resting-state data for each participant was also recorded for 5-minutes and the subjects were asked to keep their eyes open and fixated on a point presented at the center of the screen. M-EEG signals were sampled at a rate of 1 kHz and band-pass filtered between 0.01 and 330 Hz prior to sampling.

#### Task (tM-EEG)

Following the empty room and rM-EEG recordings, subjects were asked to complete the task defined in the [Procedure](#procedure) section. tM-EEG consisted of 10 runs, with 4 blocks each. During each block, a ratio of 34-38 trials was presented, with 32 non-targets (8 of each category), 2-6 targets (number chosen randomly), and  each  trial  lasting  2.4 s approximately. Rest breaks between runs and blocks were included. Random jitter was added at the end of each trial (mean inter-trial interval of 0.4 s jittered 0.2-2.0 s, truncated exponential distribution) to avoid periodic presentation of the stimuli.

|              |          |            |                 |                  |
| ------------ | -------- | ---------- | --------------- | ---------------- |
| **Task**     | **Runs** | **Blocks** | **Trials**      | **Total trials** |
| Experiment 1 | 10       | 4          | 34-38 per block | 1440             |

#### Full Structure of Session

Complete standard procedure of an M-EEG session is available in [MEG Standard Operating Procedure](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/linked_files_v1.0/MEG%20SOP_v1.0.pdf).

#### Inclusion Criteria

The items below were assessed for the subjects before the data was acquired:

- Age range: 18 to 35 (since over the age of 35 subjects might have a hard time maintaining central focus)
- Handedness: right
- Hearing problems: no
- Hearing aid: no
- Vision problems: no, or corrected-to-normal with soft lenses
- No MRI in the last week
- MRI compatible: no metal, medical implants, etc. No claustrophobia. Note: dental implants are allowed (particularly for non-magnetic materials) unless it generates big impacts on MEG signals, and this will be checked prior to MEG recording.
- No known history of psychiatric or neurological disorders, e.g.,
    - Not have been formally diagnosed with attention deficit (hyperactivity) disorder (AD(H)D).
    - Not have been formally diagnosed with autism spectrum disorder (ASD)
    - Not suffer from epilepsy

#### Quality Check and Exclusion Criteria

For M-EEG, the first stage of the third-level checks focused on system-related and external noise generators. It was tested using the signal spectra in the empty room recording, the resting state session, and the experiment itself for all sensors. Any sensor and/or specific frequency revealing extensive noise using visual inspection, was flagged to document potential problems. Ultimately, this did not lead to any exclusions. Next, all experimental data blocks were visually inspected for abnormalities in spectra (peaks not explainable by physiology), and in ICA components, and checked for extremely noisy (based on the score of differences between the original and Maxwell-filtered data > 7) and flat sensors. The latter step was performed in a collaboration between the data monitoring team and members of the centers where data was acquired to check whether any potential changes in preprocessing for particular subjects were needed. Finally, we tested if all experimental cells (i.e. task-relevant non-targets and task-irrelevant stimuli for each one of the four categories) have enough trials (N=30).

### iEEG Data Acquisition

iEEG recordings were obtained from patients with pharmacologically resistant epilepsy undergoing invasive electrophysiological monitoring at the Comprehensive Epilepsy Center at New York University (NYU) Langone Health Center, Brigham and Women’s Hospital, Children’s Hospital Boston (Harvard Medical School), and University of Wisconsin School of Medicine and Public Health (WU).

#### Hardware

Brain activity was recorded with a combination of intracranially subdural platinum-iridium electrodes embedded in SILASTIC sheets (2.3 mm diameter contacts, Ad-Tech Medical Instrument and PMT Corporation) and/or depth stereo-electroencephalographic platinum- iridium electrodes (PMT Corporation; 0.8-mm diameter, 2.0-mm length cylinders; separated from adjacent contacts by 1.5 to 2.43 mm), or Behnke-Fried depth stereo- electroencephalographic platinum-iridium electrodes (Ad-Tech Medical, BF08R-SP21X-0C2, 1.28 mm in diameter, 1.57 mm in length, 3 to 5.5 mm spacing). The decision to implant, electrode targeting, and the duration of invasive monitoring was solely determined on clinical grounds and without reference to this or any other study. Electrodes were arranged as grid arrays (either 8 × 8 with 10 mm center-to-center spacing, 8 x 16 contacts with 3 mm spacing, or hybrid macro/micro 8 x 8 contacts with 10 mm spacing and 64 integrated microcontacts with 5 mm spacing), linear strips (1 × 8/12 contacts), depth electrodes (1 × 8/12 contacts), or a combination thereof. Subdural electrodes covered extensive portions of lateral and medial frontal, parietal, occipital, and temporal cortex of the left and/or right hemisphere. Recordings from grid, strip and depth electrode arrays were done using a Natus Quantum amplifier (Pleasonton, CA) or a Neuralynx Atlas amplifier (Bozeman, MT). A total of 4057 electrodes (892 grids, 346 strips, 2819 depths) were implanted across 32 patients with drug-resistant focal epilepsy undergoing clinically motivated invasive monitoring. 3512 electrodes (780 grids, 307 strips, 2425 depths) that were unaffected by epileptic activity, artifacts, or electrical noise were used in subsequent analyses. To determine the electrode localization for each patient, a postoperative CT (computed tomography) scan and a pre-operative T1 MRI were acquired and co-registered. Recordings were obtained continuously during the patients’ stay in the hospital. All data was stored with stimulus and timing markers permitting offline synchronization.

#### Anatomical MRI Data Acquisition

Before the participants underwent surgery and electrode implantation, T1-weighted MR data were acquired from them. At NYU, imaging was performed using the Siemens Biograph mMR scanner. At Harvard, the imaging sequence utilized was MPRAGE (magnetization-prepared rapid gradient-echo), with a Siemens Skyra 3T scanner. At WU, imaging was conducted using the GE MEDICAL SYSTEMS SIGNA Artist scanner. The rationale behind acquiring MR scans was the spatial resolution it offers for brain tissue visualization.

#### CT Data Acquisition

Following surgery, post-operative CT scans were obtained from the subjects to assist in localizing the electrodes on specific brain tissue. At NYU, scans were performed using a Siemens SOMATOM Force scanner. At Harvard, imaging was conducted using the Medtronic O-arm MVS O2, manufactured by Medtronic. At WU, scans were acquired utilizing the GE MEDICAL SYSTEMS Optima CT660 scanner.

<span style="background-color: red"><b>Please note:</b></span>
**MR and CT data were collected for the subjects at Brigham and Women’s Hospital and Children’s Hospital Boston. However, due to the data protection policies, they are not included in the COGITATE Data Release.**

#### Behavioral Data Acquisition

The task was implemented using Matlab (Harvard: R2020b; NYU: R2020a, WU: 2021a), Psychtoolbox v.3 (Pelli, 1997), and run on a Dell Precision 5540 laptop, with a 15.6" Ultrasharp screen (screen size 345 x 195 mm2; resolution 1920 x 1080) at NYU and Harvard and on a Dell D29M PC with an Acer V196WL 19" LED LCD monitor (screen size 406.4 x 254 mm2; resolution 1440 x 990) at WU. The distance between the subject’s eyes and the screen was 80 cm. But the actual distance was measured for each subject before the start of recording to ensure that the size of the stimulus was 6 x 6 of visual angle. Participants responded using an 8-button response box (Millikey LH-8; response hand(s) varied based on the setting in the patient’s room).

#### Eye Tracking Data Acquisition

At Harvard and Wisconsin, EyeLink 1000 Plus Camera was used to collect eye-tracking data, and a thirteen-point calibration was performed several times during the experiment. The calibration was performed at the beginning of the experiment, and recalibrated in-between blocks, if necessary to meet precision requirements. At NYU, eye-tracking data was collected throughout the duration of the experiment using a Tobii-4C eye-tracker. A nine-point calibration was performed several times during the experiment (besides Harvard, where thirteen-point calibration was used). Pupil size and corneal reflection data were collected at a sampling rate of 500 Hz at Harvard and Wisconsin and at a sampling rate of 90 Hz at NYU. The Eyelink system recorded monocular data, while the Tobii system recorded binocular data. For the former cases, only one eye was recorded as determined by ocular dominance. The experiment was not influenced by the Eye-tracking recording.

#### Behavioral Data Code Scheme

The behavioral code scheme is similar to the M-EEG modality which is explained in [this section](#behavioral-data-code-scheme).

#### Eye Tracker Data Code 

The eye tracker code scheme for the iEEG modality follows a similar structure to that described for M-EEG data. You can find detailed explanations [here](#eye-tracker-and-meg-code-scheme).

#### iEEG Code Scheme
##### Photodiode Trigger Scheme

For ECOG patients, the type of port utilized by the M-EEG team (LPT) was incompatible with our recording system. Consequently, a photodiode was employed. A photodiode is an electronic device that records changes in luminance and converts them into voltage.

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/photodiode.png" alt="An example of a photodiode" style="width:50%;">
  <p>An example of a photodiode</p>
</div>

In the experimental code, it was ensured that when a new event occurred on the screen (such as stimulus onset or stimulus offset), a white flash appeared in the bottom right corner. The photodiode device was positioned atop the flashing square and connected to the amplifier recording the iEEG channel signals. This additional channel facilitated the identification of event onsets in our task. This type of recording only allows binary signals (the photodiode is either on or off). However, specific events were encoded with varying numbers of subsequent pulses.

**Stimulus Presentation Onset**

The flashing square was flashed only once at the onset of each new stimulus.

**Stimulus Presentation Offset**

The flashing square was flashed only once at the offset of each stimulus.

**Start of the Inter-Trial Interval**

The flashing square was flashed only once at the beginning of the inter-trial interval. The inter-trial interval was initiated 2 seconds after stimulus onset and persisted for a random duration (following a truncated exponential distribution between 0.2 and 2 seconds, with a mean of 0.4 seconds).

**Block Start**

The start of an experimental block was marked by sending 4 consecutive pulses.

**Block End**

The end of an experimental block was marked by sending 2 consecutive pulses.

**Experiment Start and End**

The beginning and end of the experiment were marked by sending 3 consecutive pulses.

<a name="schematic-representation-of-the-photodiode-channel"></a>

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/Schematic%20representation%20of%20the%20photodiode%20channel.png" alt="Schematic representation of the photodiode channel">
  <p>Schematic representation of the photodiode channel</p>
</div>

##### Log File Alignment

The photodiode channel solely indicates when a specific event occurred in the iEEG signals, lacking any information about the nature of the event (unlike an LPT trigger in MEG). To identify specific events in the signal, the timing information from the log file was combined with that from the photodiode.

The log file contains a description of each presented event along with a corresponding time stamp from the experimental computer. The photodiode channel recorded time stamps for each event, indicating when it occurred according to the acquisition computer clock. The goal was to align the log file and the photodiode to associate each event in the photodiode signal with the corresponding event description in the log file. This step was crucial since misalignment could lead to incorrect event descriptions in the iEEG signal, compromising the entire analysis.

The procedure relies on the fact that both the log file and the photodiode had timestamps. These timestamps were recorded on different clocks. Unfortunately, computer clocks tended to drift away from one another, and these drifts accumulated to be quite significant over extended periods of time (they could be several seconds apart after 1 hour). Therefore, the timestamps of the photodiode and the log file could not be used interchangeably. However, over short periods of time, these drifts were negligible. What this meant was that the interval between two successive timestamps in the log file should be quite consistent with the intervals between two successive events in the photodiode. This provided us with the most thorough check possible: if the events in the log file and in the photodiode were aligned, then there should be only tiny differences between the differences between successive events in both. Here is a step-by-step description of the alignment procedure.

**Extract the Photodiode Timestamps**

The timestamps from the photodiode triggers were extracted as the first step. As illustrated in the figure [Schematic representation of the photodiode channel](#schematic-representation-of-the-photodiode-channel), a square pulse was generated for each event during the recording. The onset of each of these pulses was sought. To achieve this, a threshold was initially established, below which the photodiode was considered to be in the off state and above which it was considered to be on (based on visual inspection of the data, which was facilitated by the clean nature of photodiode signals). Subsequently, the signal was binarized using this threshold (signal_bin = signal > threshold), resulting in a signal consisting only of ones and zeros. Next, the discrete difference of the binary signal was computed (y(i + 1) = y(i + 1) - y(i)). This operation produced a “1” when the photodiode transitioned from off to on (onset) and a “-1” when it transitioned from on to off (offset). Since only the onset was of interest, the timestamps of the ones were extracted, representing the timestamps of the photodiode.

**Verify Event Count Alignment**

The first step in aligning the photodiode events and the log files was to check if the number of events in each matched. If they did not match, then there was a problem.

**Aligning the Two Signals**

To ensure alignment of both signals, the discrete difference between the photodiode and log file timestamps was computed, providing the interval between successive events for each signal. The resulting arrays were then plotted atop each other. Misalignment between the two sources of timing information could be easily detected, as they did not overlap. Perfect overlap between the two was necessary to consider the signals aligned. Additionally, the difference between the two signals was computed to ensure minimal deviation.

**Integrating Information**

Once the two signals were properly aligned, the log file events could be used as descriptors of the events marked at the timestamps from the photodiode.

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/Illustration%20of%20the%20alignment%20pipeline.png" alt="Illustration of the alignment pipeline">
  <p>Illustration of the alignment pipeline</p>
</div>

The alignment procedure allowed the information from the log file to be utilized in generating well-described events in the iEEG data. The events were encoded as “/” separated strings and stored in an events.tsv table. An extensive description of each event type and their levels are as follows:

**Task Name:** Dur

**Task Description:** Description of the experimental factors and their level with the correct syntax to access them from the MNE epochs object. Note that factor and level names are case-sensitive. We describe the syntax for each condition separately. However, note that you can fetch a combination of factors from the epochs using a forward slash. For example, if you wish to fetch the face target trials, you can combine both conditions like so: epochs['face/Relevant target'] will fetch all face target trials. In addition, the epochs objects are equipped with metadata, where the name of the column is the name of the factor, and the level follows the same nomenclature as below. This can be used for more sophisticated trial filtering and retrieval.

**Experimental Design:**

- Event Type:
    - Marks the different events occurring within a trial.
    - Factor Type: Categorical
    - Factor 1:
        - Name: stimulus onset
        - Description: Marks the onset of the visual stimuli. With epochs['stimulus onset'], extract all epochs time-locked to the visual stimulus onset.
    - Factor 2:
        - Name: stimulus offset
        - Description: Marks the offset of the visual stimuli. With epochs['stimulus offset'], extract all epochs time-locked to the offset of the visual stimulus.
    - Factor 3:
        - Name: jitter onset
        - Description: Marks the beginning of the inter-trial jitter. All trials lasted 2 sec., with an added jitter of 400ms on average. With epochs['jitter onset'], extract all epochs time-locked to the beginning of the jitter period (2 sec. after stimulus onset).
- Block:
    - Marks the experimental blocks.
    - Factor Type: Discrete
    - Factor 1:
        - Name: block_*
        - Description: Experimental blocks. Our experiment consisted of 5 blocks, in between which participants were allowed to take a break. With epochs['block_1'], extract all epochs of the first experimental block.
- Miniblock:
    - Marks the experimental miniblocks.
    - Factor Type: Discrete
    - Factor 1:
        - Name: miniblock_*
        - Description: Experimental miniblocks. Each experimental block consisted of 4 miniblocks. At the beginning of each miniblock, the two target stimuli were presented to the participant, which the participant had to remember to be able to detect in the stream of stimuli. With epochs['miniblock_1'], extract all epochs of the first experimental miniblock.
- Category:
    - Category of the visual stimuli.
    - Factor Type: Categorical
    - Factor 1:
        - Name: face
        - Description: Identifies face trials. With epochs['face'], extract all epochs in which a face was presented.
    - Factor 2:
        - Name: object
        - Description: Identifies object trials. With epochs['object'], extract all epochs in which an object was presented.
    - Factor 3:
        - Name: letter
        - Description: Identifies letter trials. With epochs['letter'], extract all epochs in which a letter was presented.
    - Factor 4:
        - Name: false
        - Description: Identifies false font trials (i.e., symbols). With epochs['false'], extract all epochs in which a false font was presented.
- Identity:
    - Identity of the visual stimuli.
    - Factor Type: Categorical
    - Factor 1:
        - Name: face_*
        - Description: Identifies the identity of face trials. With epochs['face_*'], extract all epochs in which that specific face was presented. From 1-9, leading 0.
    - Factor 2:
        - Name: object_*
        - Description: Identifies the identity of object trials. With epochs['object_*'], extract all epochs in which that specific object was presented. From 1-9, leading 0.
    - Factor 3:
        - Name: letter_*
        - Description: Identifies the identity of letter trials. With epochs['letter_*'], extract all epochs in which that specific letter was presented. From 1-9, leading 0.
    - Factor 4:
        - Name: false_*
        - Description: Identifies the identity of false font trials (i.e., symbols). With epochs['false__*'], extract all epochs in which that specific false font was presented. From 1-9, leading 0.
- Orientation:
    - Orientation of the displayed stimuli.
    - Factor Type: Categorical
    - Factor 1:
        - Name: Center
        - Description: Identifies stimuli presented in the center orientation. With epochs['Center'], extract all epochs in which a stimulus was presented in the center orientation.
    - Factor 2:
        - Name: Left
        - Description: Identifies stimuli presented in the Left orientation. With epochs['Left'], extract all epochs in which a stimulus was presented in the Left orientation.
    - Factor 3:
        - Name: Right
        - Description: Identifies stimuli presented in the Right orientation. With epochs['Right'], extract all epochs in which a stimulus was presented in the Right orientation.
- Duration:
    - Duration a visual stimulus was presented for.
    - Factor Type: Categorical
    - Factor 1:
        - Name: 500ms
        - Description: Identifies stimuli presented for 500ms. With epochs['500ms'], extract all epochs in which the stimulus was displayed for 500ms.
    - Factor 2:
        - Name: 1000ms
        - Description: Identifies stimuli presented for 1000ms. With epochs['1000ms'], extract all epochs in which the stimulus was displayed for 1000ms.
    - Factor 3:
        - Name: 1500ms
        - Description: Identifies stimuli presented for 1500ms. With epochs['1500ms'], extract all epochs in which the stimulus was displayed for 1500ms.
- Task Relevance:
    - Task relevance of a given trial.
    - Factor Type: Categorical
    - Factor 1:
        - Name: Relevant target
        - Description: Identifies target stimuli. Target stimuli are presented at the beginning of each miniblock, and participants must detect them among the sequence of presented stimuli by pressing a button. With epochs['Relevant target'], extract all target trials.
    - Factor 2:
        - Name: Relevant non-target
        - Description: Identifies task-relevant non-target stimuli. We considered task-relevant stimuli that were of the same category as the target but of a different identity. With epochs['Relevant non-target'], extract all task-relevant non-target trials.
    - Factor 3:
        - Name: Irrelevant
        - Description: Identifies task-irrelevant non-target stimuli. We considered task-irrelevant stimuli that were of a different category than the target. With epochs['Irrelevant'], extract all task-irrelevant non-target trials.
- Response:
    - Rated response of the participants.
    - Factor Type: Categorical
    - Factor 1:
        - Name: Hit
        - Description: Participants correctly identified a target by pressing a button. With epochs['Hit'], extract all target trials for which the participants pressed a key.
    - Factor 2:
        - Name: CorrRej
        - Description: Participants correctly rejected a non-target stimulus and did not press any button. With epochs['CorrRej'], extract all non-target trials for which the participants did not press a key.
    - Factor 3:
        - Name: Miss
        - Description: Participants failed to press a button when a target stimulus was presented. With epochs['Miss'], extract all target trials in which participants failed to press a button.
    - Factor 4:
        - Name: FA
        - Description: Participants mistakenly pressed a button when a non-target stimulus was presented. With epochs['FA'], extract all non-target trials in which participants pressed a button.
    - Factor 5:
        - Name: n.a.
        - Description: For the events stimulus offset and jitter onset, the response is set to n.a. as the response relates to the visual stimulus, not to the other events. This should not be used to access the data.

#### Surface Reconstruction and Electrode Localization

Subject-specific pial surfaces were automatically reconstructed based on a pre-implant T1 weighted MR image using the [Freesurfer](http://surfer.nmr.mgh.harvard.edu) image analysis suite (‘recon-all’, Dale et al., 1999). Post-implant CT images were co-registered with the pre-implant MR images using FLIRT (Jenkinson and Smith, 2001), as implemented in [FSL](http://fsl.fmrib.ox.ac.uk/fsl/) (Smith et al., 2004). For NYU patients, we used a semi-automatic approach to generating electrode labels. For manual cases, co-registered MR and CT slices were examined using FSLView (Smith et al., 2004). For grids, we localized three corner electrodes and the remaining electrodes coordinates were then automatically interpolated along the shared plane using the known inter-electrode distances. Strip and depth electrodes were localized manually when they did not follow straight trajectories. When depth electrodes were in a straight line, the first and last electrodes were localized manually, and electrodes in between were automatically interpolated and labeled based on known inter-electrode distances and serial labeling convention. For WU patients, electrodes were localized manually using the [SubNuclear toolbox](https://github.com/ckovach/SubNuclear/tree/master). Electrode locations were further refined within the space of the pre-operative MRI using three-dimensional non-linear thin-plate spline warping (Rohr et al., 2001), which corrected for post-operative shift and distortion. The warping was constrained with manually selected points through the brain, which was visually aligned with landmarks in pre-implantation MRI and post-implantation CT. For Harvard subjects, individual contacts from depth electrodes were labeled manually from the CT image using the [BioImage Suite](https://bioimagesuiteweb.github.io/webapp/)’s  Electrode Editor tool (legacy version 3.5; Joshi, et al., 2011). The coordinates in CT image-space were converted to coordinates within the patient’s segmented MRI brain-space using the [iELVis toolbox](https://github.com/iELVis/iELVis) (yangWangElecPjct; Yang, Wang, et al., 2012; Groppe et al., 2017). For all sites, the electrode spatial coordinates were transformed from the individual patient space into the standard space of the Montreal Neurological Institute (MNI-152) template for plotting purposes. At NYU, this transformation was performed using the DARTEL algorithm (Ashburner, 2007) implemented in SPM8 (Wellcome Department of Imaging Neuroscience, London, United Kingdom). At Harvard, this transformation was performed using the [iELVis toolkit](https://github.com/iELVis/iELVis). At WU the transformation was performed with the [SubNuclear toolbox](https://github.com/ckovach/SubNuclear/tree/master) using img2imgcoord utility.

#### Finger Localizer Task

In the Finger Localizer task, participants were presented with four circles, one of which was filled with a specific color, serving as a cue for participants to press the corresponding colored button on the response box. The filled state of the circle persisted for the duration of the response time, followed by an additional delay of 200 milliseconds. The Inter-Trial Intervals (ITIs) were uniformly distributed, with a mean of 0.55 seconds and a range from 0.400 to 0.700 seconds. The experimental protocol comprised 80 trials, distributed equally among the four colors, with 20 trials per color, and the sequence of trials was randomized. This task aimed to identify brain regions responsible for motor control, particularly those governing finger movements, and to pinpoint electrodes selectively activated by specific motor responses, such as button presses.

<div style="text-align:center;">
  <img src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/FingerLoc.png" alt="An illustration depicting a trial in which the participant is required to press the blue button" style="width:50%;">
  <p>An illustration depicting a trial in which the participant is required to press the blue button</p>
</div>

<span style="background-color: red"><b>Please note:</b></span> **Although participants completed this task concurrently with [Experiment 1](02_overview.md#experiment-1-conscious-perception), we did not utilize the data in the analysis, as it was primarily acquired for use in [Experiment 2](02_overview.md#experiment-2-video-game-engagement). Consequently, the data pertaining to the Finger Localizer task is not included in this version of our data release.**

#### Task (tiEEG)

Participants proceeded to Experiment 1 either after or before completing the [Finger Localizer task](#finger-localizer-task). tiEEG consisted of 5 runs containing 4 blocks each, and 34-38 trials per block, 32 non-targets (8 of each category) and 2-6 targets, with each trial lasting 2.4 s approximately, for a total of 720 trials. Rest breaks between runs and blocks were included. Random jitter was added at the end of each trial (mean inter-trial interval of 0.4 s jittered 0.2-2.0 s, truncated exponential distribution) to avoid periodic presentation of the stimuli. Additional information about the task can be found [here](#procedure).

|              |          |            |                 |                  |
| ------------ | -------- | ---------- | --------------- | ---------------- |
| **Task**     | **Runs** | **Blocks** | **Trials**      | **Total trials** |
| Experiment 1 | 5       | 4          | 34-38 per block | 720             |

#### Full Structure of Session

Complete standard procedure of an iEEG session is available in [iEEG Standard Operating Procedure](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/linked_files_v1.1/SOP%20iEEG%20General_v2.pdf).

#### Inclusion Criteria

For the iEEG studies, subjects were 10-65 years old, able to provide informed consent, had IQ > 70, fluent in English, with self-reported normal hearing, normal or corrected-to-normal vision, and cognitive and language abilities within or above the normal range in formal neuropsychological testing performed before surgery. They must not have had an electrographic seizure within 3-hours prior to testing.

#### Quality Check

A comprehensive quality assessment was conducted on the iEEG data. The data underwent manual annotation by epileptologists, excluding channels within the epileptic onset zone, as well as those exhibiting artifacts or showing complete flatness due to electrode contact issues. Channel rejection was independently performed by both the data monitoring and iEEG teams, with results compared to ensure consistency. Additionally, electrode reconstruction was verified to align with subjects' CT scans. Finally, we inspected for significant disturbances in the spectra.

#### Exclusion Criteria

Subjects who were unable to complete a sufficient number of trials due to excessive muscular artifacts, movement, noisy recordings, or a decision by the subject to terminate the experiment were excluded. Subjects who exhibited a low performance in the attention task were also excluded – this translates to <70% Hits and >30% FAs. In addition, data was also excluded if it did not pass any of the pre-defined data quality checks.

