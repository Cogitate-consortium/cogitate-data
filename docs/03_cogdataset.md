# COGITATE Dataset

The COGITATE dataset is a comprehensive collection of multimodal neuroimaging data, encompassing a total of 262 subjects. COGITATE employs three distinct neuroimaging techniques: fMRI, M-EEG, and iEEG/ECoG.

![Cogitate overview map](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/overview_map.png)

The MEG modality comprised 102 healthy subjects, also above the age of 18, with no known psychiatric or neurological issues. These participants were sourced from the Centre for Human Brain Health at the University of Birmingham (Birmingham, United Kingdom) and the Center for MRI Research of Peking University (Beijing, China).

Similarly, the fMRI modality included 122 healthy volunteers, all of whom were above the age of 18 and predominantly right-handed. These participants had no known history of psychiatric or neurological disorders and were recruited from the Yale Magnetic Resonance Research Center (New Haven, CT, United States) and the Donders Centre for Cognitive Neuroimaging (Nijmegen, Netherlands).

In contrast, the iEEG modality involved a more specialized cohort of 38 patients diagnosed with pharmaco-resistant focal epilepsy. These participants ranged in age from 10 to 65 years, had an IQ above 70, and met specific health criteria. They were recruited from multiple medical centers specializing in epilepsy treatment, including the Comprehensive Epilepsy Center at New York University (New York, NY, United States), Brigham and Women’s Hospital, Boston Children’s Hospital (Boston, MA, United States), and the University of Wisconsin School of Medicine and Public Health (Madison, WI, United States).

**Age histograms across modalities**
![Cogitate subjects age distribution](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/age%20histograms%20across%20modalities_2024-04-26_v1.1.png)

**Sex proportions across modalities**
![Cogitate subjects age distribution](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/sex%20proportions%20across%20modalities_2024-04-26_v1.1.png)

**Handedness proportions across modalities**
![Cogitate subjects age distribution](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/handedness%20proportions%20across%20modalities_2024-04-26_v1.1.png)

## Demography of Subjects

You can find the profile of participants for all modalities at [subjects_demography](https://github.com/Cogitate-consortium/cogitate-data/blob/main/assets/documentation_v1.1/linked_files_v1.1/subjects_demography-EXP1-released-data_2024-04-026_v1.1.xlsx). Here is a brief explanation about the information collected from the subjects.

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

Data from all modalities were checked at three levels. The first level checks tested whether the datasets  contained  all  expected  files  keeping  their  naming  conventions,  and  that  all  personal information had been removed. The second level checks tested subjects’ performance with respect to behavior. For [Experiment 1](02_overview.md#experiment-1-conscious-perception), subjects were excluded if their hit rate was lower than 80% or (False Alarm) FAs higher than 20% for M-EEG and fMRI, and for iEEG, a more relaxed criteria of 70% Hits and 30% FAs was used. Two M-EEG subjects were excluded due to low hit rates and one iEEG patient was excluded due to high FAs. The  third  level  checks  assessed  the  quality  of  the  neural  data.

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

### **File type glossary**

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

#### **M-EEG data**

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

#### **iEEG data**

- **Unprocessed/Raw release format**
      - Filetype: EDF

- **BIDS Format**
      - Filetype: EDF

European Data Format files used for storing and exchanging time-series biological and physiological data

EDF files are designed to accommodate data from multiple channels, allowing researchers to store and manage data collected simultaneously from different sensors or electrodes. The format supports both raw signal data and associated metadata, including information about sampling rates, units of measurement, patient demographics, and recording conditions.

## Data Acquisition

The Cogitate dataset encompasses three distinct neuroimaging modalities, along with synchronized eye-tracking and behavioral data linked to each of these modalities. Here we detail the acquisition protocol for each modality in the corresponding data release: M-EEG, iEEG

### Stimuli

Stimuli belonged to four categories that naturally fell into two groups that were clearly distinct from each other: pictures (20 faces and 20 objects) and symbols (20 letters and 20 false-fonts). Face stimuli were created using the FaceGen Modeler 3.1 program and object stimuli were taken from the Object Databank (Tarr, 1996). Faces and objects were grey-scaled (RGB: 125, 125, 125), and manipulated to have similar size and equal luminance using the SHINE toolbox (Willenbockel et al., 2010). Equal proportions of male and female faces were presented. They all had hair and belonged to different ethnicities (e.g., Caucasian, Asian, African, American) to facilitate face individuation. The orientation of the stimuli was manipulated, such that half of the stimuli from each category had a side view and the other half a front view. All letter stimuli and false fonts were generated with MAXON CINEMA 4D Studio (RC-R20) 20.059 on macOS 10.14, appearing in gray (RGB: 125, 125, 125). Three views were rendered for each font set (real font, false/pseudo font) at 0°, 30° and -30° horizontal viewing angle with the following settings: Extrusion depth 9.79% of character height, camera distance 5.65 times character height and 18° above the center of the letter (High Angle), with a simulated focal length of 135 mm (35 mm equiv.). All stimuli were presented on a rectangular aperture at an average visual angle of 6 ̊ by 6 ̊.

### Procedure

Stimuli were presented sequentially, all supra-threshold, with half being task-relevant and the other half task-irrelevant. Only one stimulus was shown on the screen at any given time. To define task relevance, subjects were instructed to detect two targets from different categories, regardless of their orientation. This online reporting enabled an explicit assessment of subjects’ performance, engaging report-related areas for later analysis. Each block began with notification of the two target stimuli, either pictorial (faces and objects) or symbolic (letters and false fonts), creating a clear distinction between relevant and irrelevant stimuli. At the start of each block, specific target stimuli were revealed with instructions such as “detect face A and object B” or "detect letter C and false-font D." Targets did not repeat across blocks. Each run included two blocks of the Face/Object task and two blocks of the Letter/False-font task, with the order counterbalanced across runs. Subjects were instructed to maintain central fixation throughout each trial. Gaze was monitored online through an eye tracker, with repeated calibrations ensuring good quality data.

Each block comprised stimuli from all four categories, with each stimulus displayed for 500, 1000, or 1500 ms, followed by a blank interval, ensuring a consistent trial duration of 2000 ms. Within each block, three trial types were presented: i) Task Relevant Targets, consisting of the specific stimuli participants were tasked with detecting; ii) Task Relevant Non-Targets, encompassing stimuli from relevant categories that were not designated targets; and iii) Task Irrelevant Stimuli, comprising stimuli from the remaining categories.

### M-EEG Data Acquisition

M-EEG recordings were acquired at the Centre for Human Brain Health (CHBH) of University of Birmingham in the United Kingdom, and at the Center for MRI Research of Peking University (PKU) in China.

#### Hardware

Both centers had a 306-channel, whole-head TRIUX MEG system from MEGIN (York Instruments; formerly Elekta). The MEG system comprised 204 planar gradiometers and 102 magnetometers in a helmet-shaped array. Simultaneous EEG was recorded using an integrated EEG system and a 64-channel electrode cap. The MEG system was equipped with a zero boil-off Helium recycling system and the noise-resilient ARMOR sensors and placed in a shielded room (2 layers of mu-metal and 1 layer of aluminum). To reduce environmental noise, the integrated active shielding system was used at PKU. In order to cover the brain more homogeneously, the MEG gantry was positioned at 68 degrees.

#### Location of Electrodes and ECG/EOG Measurements

The location of the fiducials, the positions of the 64 EEG electrodes and the participant’s head shape were recorded using a 3-D digitizer system (Polhemus Isotrak). A set of bipolar electrodes were placed on the subject’s chest (upper left and upper right chest position) to record the cardiac signal (ECG). Two sets of bipolar electrodes were placed around the eyes (two located at the outer canthi of the right and left eyes and two above and below the center of the right eye) to record eye movements and blinks (EOG). Ground and reference electrodes were placed on the back of the neck and on the right cheek, respectively. The impedance of all of the electrodes was checked to be below 10 kOhm.

![Standard Locations of EOG and ECG electrodes](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/eog_ecg_electrodes_meg.png)
Standard Locations of EOG and ECG electrodes

#### Head Position Indicator (HPI) Coils

The participant’s head position inside the MEG system was measured at the beginning and at the end of each run using four head position indicator (HPI) coils placed on the EEG cap. Specifically, the HPI coils were placed next to the left and right mastoids and on the left and right forehead. Their location relative to anatomical landmarks was digitized with a Polhemus Isotrak System. During the measurement, high frequency (>200 Hz) signals were produced by those coils and the localization of these signals was used to estimate the head position in the sensor space. To avoid the potential artifacts produced by the non-linear interaction between the signals generated by these coils, head position measurement was performed only during resting periods (as opposed to continuously).

![Standard Locations of HPI coils](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/hpi_coils_meg.png)
Standard locations of HPI coils.  
Coil Numbers: 1. Blue, 2. White, 3. Red, 4. Black, 5. Yellow

#### Anatomical MRI Data Acquisition

For each subject, a high resolution T1-weighted MRI volume (3T Siemens MRI Prisma scanner) was acquired. At CHBH, a 32-channel coil with a resolution of 1 x 1 x 1 mm, TR/TE = 2000/2.03ms; TI = 880 ms; 8° flip angle, 208 sagittal slices and field of view (FOV): 256 x 256 matrix was acquired for source localization with individual realistic head modeling. At PKU, a 64-channel coil with a resolution of 0.5 x 0.5 x 1 mm, TR/TE = 2530/2.98ms; TI = 1100 ms; 7° flip angle, 192 sagittal slices; FOV: 448 × 512 matrix was used. To avoid possible interference of body magnetization on the MEG recording, all MRI scans were acquired at least one week before the MEG session, or at any time afterwards. The FreeSurfer standard template was used (fsaverage) for participants lacking an anatomical scan (N=5).

#### Behavioral Data Acquisition

The task was executed using Matlab (PKU: R2018b; UB: R2019b) with Psychtoolbox v.3 (Pelli, 1997) on a custom PC at UB and a Dell XPS desktop PC at PKU. Visual stimuli were presented on a screen placed in front of the subjects with a PROPixx DLP LED projector (VPixx Technologies Inc.) at a resolution of 1920 x 1080 pixels and a refresh rate of 120 Hz. The distance between the subject’s eyes and the screen was different at each site (CHBH: 119 cm, PKU: 85 cm) to achieve the same FOV of 36.6 x 21.2 degrees. Subjects responded with an 8-button response box (Millikey LH-8).

#### Eye Tracking Data Acquisition

Eye movements were monitored and recorded from both eyes (binocular eye-tracking) using the MEG-compatible EyeLink 1000 Plus eye-tracker (SR Research Ltd., Ottawa, Canada). Nine-point calibration was performed at the beginning of the experiment, and recalibrated if necessary at the beginning of each block/word. Pupil size and corneal reflection data were collected at a sampling rate of 1000 Hz.

#### Behavioral Data Code Scheme

Stimuli are coded as a 4-digit number.  
1st digit = stimulus type (1 = face; 2 = object; 3 = letter; 4 = false font)  
2nd digit = stimulus orientation (1 = center; 2 = left; 3 = right)  
3rd & 4th digits = stimulus id (1...20; for faces 1...10 is male, 11...20 is female)  

e.g., "1219" = 1 is face, 2 is left orientation and 19 is a female stimulus #19

#### Eye Tracker and MEG Trigger Scheme

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

Following the empty room and rM-EEG recordings, subjects were asked to complete the task defined in the [Procedure](#procedure) section.

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
