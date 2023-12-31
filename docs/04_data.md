# Data description
## Data acquisition
Although our data collection had a specific purpose, the data we gathered holds potential value for a range of diverse inquiries. Consequently, the COGITATE consortium has chosen to openly share all raw data collected, with the aim of facilitating its utilization for various research endeavors and promoting data reusability. This approach reflects our commitment to contributing to the broader scientific community.

We have made available two primary formats for the data acquired during the experimental phase of the COGITATE project, specifically from Experiment 1:

**1. Unprocessed Data:**

The unprocessed data format closely resembles the original acquired data, having undergone minimal processing to ensure compliance with GDPR/HIPAA anonymity standards.

**2. BIDS Format (Brain Imaging Data Structure):**

BIDS format, widely adopted in cognitive neuroscience, enhances data reusability. To facilitate others in leveraging our data, we have released it in BIDS format. The conversion scripts employed to transform the raw data into BIDS format can be accessed via this link: [LINK].

We emphasize our explicit intent to share the entirety of our data, empowering the community to integrate it into their research. When utilizing the data, it is important to consider the contextual factors and limitations that may affect its interpretation.

Release format and Modality Table:


| Release format -> <br> ___ <br> Modality | Raw / Unprocessed | Bids converted | Bids derivatives / Pre-processed | Additionally processed |
| --- | --- | --- | --- | --- |
| Eye Tracking & Behavioral data | EDF | EDF | ASC | ASC |
| fMRI | DICOM | DICOM | NIFTI | NIFTI |
| MEEG | FIF | FIF | NPY | NPY |
| iEEG/ECoG | EDF | EDF | EDF | EDF |

## File type glossary

### EDF files

EDF files, also known as European Data Format files, are a standardized file format used for storing and exchanging time-series biological and physiological data. EDF files are commonly used in medical and scientific research contexts to record and analyze data from various types of measurements, such as electroencephalography (EEG), electrocardiography (ECG), electromyography (EMG), and other bioelectrical signals.

EDF files are designed to accommodate data from multiple channels, allowing researchers to store and manage data collected simultaneously from different sensors or electrodes. The format supports both raw signal data and associated metadata, including information about sampling rates, units of measurement, patient demographics, and recording conditions.

One of the key advantages of the EDF format is its portability and compatibility across different software and platforms. Many data analysis and visualization tools in the field of neuroscience and medicine support the EDF format, enabling researchers to share and collaborate on data without compatibility issues.

It's worth noting that there are variations and extensions of the EDF format, such as EDF+ and EDF/EDF+ Converter, which provide additional features and improvements for specific applications. Overall, EDF files play an essential role in the storage and analysis of physiological and biological data in scientific and medical research.

### EDF files (Eye-tracking)

EDF (EyeLink Data Format) is a file format used to store eye-tracking data collected during experiments using the EyeLink system. It plays a crucial role in the analysis of visual attention and gaze behavior in various research fields like psychology, cognitive science, human-computer interaction, to name a few. EDF files store data collected from eye-tracking experiments, which typically involve recording where a participant's eyes are fixating and how they move while viewing a stimulus, such as images or text.

The EyeLink system, developed by SR Research Ltd., is a widely used eye-tracking hardware and software solution. The EyeLink system records various types of data during an experiment, including the position of the participant's gaze (where they are looking on the screen) and the timing of their eye movements. This data is then saved in EDF files, which have a specific structure that allows the analysis and interpretation of eye-tracking data using specialized software.
EDF files contain information such as timestamps, gaze coordinates, pupil size, and information about the visual stimuli being presented. These files can be used to analyze patterns of visual attention, fixations (periods when the eyes are relatively stationary), saccades (rapid eye movements between fixations), and other eye movement behaviors.
To work with EDF files, typically software is provided by SR Research or other third-party tools that can read and interpret the data in these files. This software allows researchers to visualize eye movement patterns, conduct statistical analyses, and draw conclusions about how participants process visual information.

### FIF files

FIF files in MEEG (Magnetoencephalography and Electroencephalography) refer to the File Format for the Input and Output of MEG and EEG data. MEG and EEG are neuroimaging techniques used to study brain activity. FIF files are a standardized format developed by the MNE (Magnetoencephalography and Electroencephalography) community to store and exchange MEG and EEG data.

FIF files contain various types of information related to neuroimaging data, including:

1. Raw sensor data: MEG and EEG measurements recorded from sensors placed on the scalp or near the head.
1. Event information: Time-stamped triggers or markers indicating the timing of events, such as stimulus presentations or subject responses.
1. Sensor locations and orientations: Information about the physical positions and orientations of sensors used in the measurements.
1. Head geometry: Information about the shape and structure of the subject's head, which is crucial for accurate source localization.
1. Covariance matrices: Statistical information about the relationships between sensor measurements at different time points or frequencies.
1. Anatomical MRI data: High-resolution structural images of the subject's brain, used for source localization and spatial alignment.

The FIF file format ensures compatibility and interoperability between different MEG and EEG software tools and facilitates data sharing and collaboration in the neuroimaging research community. It's worth noting that MEG and EEG data can be quite complex and multidimensional, and the FIF format provides a structured and standardized way to store and manage this data.

### ASC files

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

### DICOM files

DICOM (Digital Imaging and Communications in Medicine) files are a standard format used for storing, transmitting, and managing medical images and related information. They are widely used in the field of radiology and other medical imaging specialties, such as MRI (Magnetic Resonance Imaging), CT (Computed Tomography), ultrasound, and more.

DICOM files are designed to ensure interoperability and compatibility among different imaging devices, picture archiving and communication systems (PACS), and other healthcare information systems. These files contain not only the actual image data but also metadata and contextual information, such as patient information, image acquisition parameters, study details, and more. This comprehensive set of information allows medical professionals to accurately interpret and diagnose medical images, track patient history, and collaborate effectively across different healthcare facilities.

DICOM files typically have a ".dcm" file extension and adhere to a specific structure and data format defined by the DICOM standard. This standardization facilitates seamless exchange of medical images and data between different software and hardware platforms, contributing to improved patient care and medical research.

### NIFTI files

NIFTI (Neuroimaging Informatics Technology Initiative) files are a widely used file format in the field of neuroimaging, particularly in the context of functional and structural magnetic resonance imaging (MRI) data. These files store three-dimensional brain images and related metadata, allowing researchers and clinicians to store, share, and analyze neuroimaging data.

NIFTI files typically have the ".nii" or ".nii.gz" file extensions. The ".nii" format is uncompressed, while the ".nii.gz" format is compressed using gzip compression. These files contain information about the image dimensions, voxel sizes, data type (e.g., integer or floating-point values), and other relevant information.

NIFTI was developed as an improvement over the earlier Analyze file format. It addresses certain limitations of the Analyze format, such as the ability to handle 3D and 4D data (3D data over time), improved support for different data types, and better compatibility with modern software tools.

Researchers and medical professionals use NIFTI files to store various types of neuroimaging data, including structural  MRI scans, functional MRI scans, and diffusion tensor imaging (DTI) data (which captures white matter tracts and connectivity patterns within the brain).

NIFTI files are supported by many neuroimaging software packages, making them a crucial part of the neuroimaging data analysis workflow. Researchers can use these files for tasks such as preprocessing, visualization, statistical analysis, and creating anatomical atlases.

### NPY files

NPY files, short for "NumPy files," are a file format used in the Python programming language for storing and exchanging numerical data. NumPy is a popular library in Python that provides support for multi-dimensional arrays and matrices, along with various mathematical functions to operate on these arrays.

NPY files are specifically used to save and load arrays and data structures created using NumPy. These files have the extension ".npy" and are binary files that efficiently store the data in a format that preserves the array's shape, data type, and other metadata. This makes them suitable for fast and efficient storage and retrieval of large numerical datasets, which is especially useful in scientific computing, data analysis, and machine learning applications.
