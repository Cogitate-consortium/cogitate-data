# Experiment 1: Directory Structure of Data Bundles

## Raw Data

Raw data files are organized hierarchically: Experiment modality --> Subjects --> data folders

The available modalities are: M-EEG.

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
    ├── metadata/                                # Experiment modality level metadata folder
    │    ├── devices_MEEG.json                   # List of devices used to collect the data
    │    ├── protocols_MEEG.json                 # A link to the Standard Operating Procedures (SOP)
    │    ├── subjects_demographics_MEEG.json     # Demographic information of MEEG subjects
    │    ├── tasks_EXP1.json                     # Description of the 1st Cogitate task 
    │    ├── tasks_RestinEO.json                 # Description of the Resting state task
    │    ├── tasks_Rnoise.json                   # Description of the Rnoise task 
    │    └── wirings_MEEG.PDF                    # Wiring diagram of devices_MEEG.json connections 
    └── CB036                                    # Subject folder
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

## BIDS Format

### BIDS M-EEG Data Directory Structure

```bash
COG_MEEG_EXP1_BIDS_RELEASE/
|-- dataset_description.json           # Contains information on BIDS version, type of dataset  
|-- derivatives                           # Contains processed or derived data generated from raw data  
|   |-- dicom2nifti                   # Converted NIFTI files generated from DICOM files of anatomical data
|   |   |-- sub-CA103
|   |   |   `-- ses-0
|   |   |       `-- anat
|   |   |           |-- CA103_MR_0_anat.nii.gz
|   |   |           `-- T1_defaced.png
|   |-- fs
|   |   |-- fsaverage 
|   |   |-- sub-CA103
|   |   |   |-- label
|   |   |   |   |-- aparc.annot.a2009s.ctab
|   |   |   |   |-- aparc.annot.ctab
|   |   |   |   |-- aparc.annot.DKTatlas.ctab
|   |   |   |   |-- BA_exvivo.ctab
|   |   |   |   |-- BA_exvivo.thresh.ctab
|   |   |   |   |-- lh.aparc.a2009s.annot
|   |   |   |   |-- lh.aparc.annot
|   |   |   |   |-- lh.aparc.DKTatlas.annot
|   |   |   |   |-- lh.BA1_exvivo.label
|   |   |   |   |-- lh.BA1_exvivo.thresh.label
|   |   |   |   |-- lh.BA2_exvivo.label
|   |   |   |   |-- lh.BA2_exvivo.thresh.label
|   |   |   |   |-- lh.BA3a_exvivo.label
|   |   |   |   |-- lh.BA3a_exvivo.thresh.label
|   |   |   |   |-- lh.BA3b_exvivo.label
|   |   |   |   |-- lh.BA3b_exvivo.thresh.label
|   |   |   |   |-- lh.BA44_exvivo.label
|   |   |   |   |-- lh.BA44_exvivo.thresh.label
|   |   |   |   |-- lh.BA45_exvivo.label
|   |   |   |   |-- lh.BA45_exvivo.thresh.label
|   |   |   |   |-- lh.BA4a_exvivo.label
|   |   |   |   |-- lh.BA4a_exvivo.thresh.label
|   |   |   |   |-- lh.BA4p_exvivo.label
|   |   |   |   |-- lh.BA4p_exvivo.thresh.label
|   |   |   |   |-- lh.BA6_exvivo.label
|   |   |   |   |-- lh.BA6_exvivo.thresh.label
|   |   |   |   |-- lh.BA_exvivo.annot
|   |   |   |   |-- lh.BA_exvivo.thresh.annot
|   |   |   |   |-- lh.cortex.label
|   |   |   |   |-- lh.entorhinal_exvivo.label
|   |   |   |   |-- lh.entorhinal_exvivo.thresh.label
|   |   |   |   |-- lh.MT_exvivo.label
|   |   |   |   |-- lh.MT_exvivo.thresh.label
|   |   |   |   |-- lh.perirhinal_exvivo.label
|   |   |   |   |-- lh.perirhinal_exvivo.thresh.label
|   |   |   |   |-- lh.V1_exvivo.label
|   |   |   |   |-- lh.V1_exvivo.thresh.label
|   |   |   |   |-- lh.V2_exvivo.label
|   |   |   |   |-- lh.V2_exvivo.thresh.label
|   |   |   |   |-- rh.aparc.a2009s.annot
|   |   |   |   |-- rh.aparc.annot
|   |   |   |   |-- rh.aparc.DKTatlas.annot
|   |   |   |   |-- rh.BA1_exvivo.label
|   |   |   |   |-- rh.BA1_exvivo.thresh.label
|   |   |   |   |-- rh.BA2_exvivo.label
|   |   |   |   |-- rh.BA2_exvivo.thresh.label
|   |   |   |   |-- rh.BA3a_exvivo.label
|   |   |   |   |-- rh.BA3a_exvivo.thresh.label
|   |   |   |   |-- rh.BA3b_exvivo.label
|   |   |   |   |-- rh.BA3b_exvivo.thresh.label
|   |   |   |   |-- rh.BA44_exvivo.label
|   |   |   |   |-- rh.BA44_exvivo.thresh.label
|   |   |   |   |-- rh.BA45_exvivo.label
|   |   |   |   |-- rh.BA45_exvivo.thresh.label
|   |   |   |   |-- rh.BA4a_exvivo.label
|   |   |   |   |-- rh.BA4a_exvivo.thresh.label
|   |   |   |   |-- rh.BA4p_exvivo.label
|   |   |   |   |-- rh.BA4p_exvivo.thresh.label
|   |   |   |   |-- rh.BA6_exvivo.label
|   |   |   |   |-- rh.BA6_exvivo.thresh.label
|   |   |   |   |-- rh.BA_exvivo.annot
|   |   |   |   |-- rh.BA_exvivo.thresh.annot
|   |   |   |   |-- rh.cortex.label
|   |   |   |   |-- rh.entorhinal_exvivo.label
|   |   |   |   |-- rh.entorhinal_exvivo.thresh.label
|   |   |   |   |-- rh.MT_exvivo.label
|   |   |   |   |-- rh.MT_exvivo.thresh.label
|   |   |   |   |-- rh.perirhinal_exvivo.label
|   |   |   |   |-- rh.perirhinal_exvivo.thresh.label
|   |   |   |   |-- rh.V1_exvivo.label
|   |   |   |   |-- rh.V1_exvivo.thresh.label
|   |   |   |   |-- rh.V2_exvivo.label
|   |   |   |   `-- rh.V2_exvivo.thresh.label
|   |   |   |-- mri
|   |   |   |   |-- aparc.a2009s+aseg.mgz
|   |   |   |   |-- aparc+aseg.mgz
|   |   |   |   |-- aparc.DKTatlas+aseg.mgz
|   |   |   |   |-- aseg.auto.mgz
|   |   |   |   |-- aseg.auto_noCCseg.label_intensities.txt
|   |   |   |   |-- aseg.auto_noCCseg.mgz
|   |   |   |   |-- aseg.mgz
|   |   |   |   |-- aseg.presurf.hypos.mgz
|   |   |   |   |-- aseg.presurf.mgz
|   |   |   |   |-- brain.finalsurfs.mgz
|   |   |   |   |-- brainmask.auto.mgz
|   |   |   |   |-- brainmask.mgz
|   |   |   |   |-- brain.mgz
|   |   |   |   |-- ctrl_pts.mgz
|   |   |   |   |-- filled.mgz
|   |   |   |   |-- lh.ribbon.mgz
|   |   |   |   |-- mri_nu_correct.mni.log
|   |   |   |   |-- mri_nu_correct.mni.log.bak
|   |   |   |   |-- norm.mgz
|   |   |   |   |-- nu.mgz
|   |   |   |   |-- orig
|   |   |   |   |   `-- 001.mgz
|   |   |   |   |-- orig.mgz
|   |   |   |   |-- orig_nu.mgz
|   |   |   |   |-- rawavg.mgz
|   |   |   |   |-- rh.ribbon.mgz
|   |   |   |   |-- ribbon.mgz
|   |   |   |   |-- segment.dat
|   |   |   |   |-- T1.mgz
|   |   |   |   |-- talairach.label_intensities.txt
|   |   |   |   |-- talairach.log
|   |   |   |   |-- talairach_with_skull.log
|   |   |   |   |-- transforms
|   |   |   |   |   |-- bak
|   |   |   |   |   |-- cc_up.lta
|   |   |   |   |   |-- talairach.auto.xfm
|   |   |   |   |   |-- talairach.auto.xfm.lta
|   |   |   |   |   |-- talairach_avi.log
|   |   |   |   |   |-- talairach_avi_QA.log
|   |   |   |   |   |-- talairach.lta
|   |   |   |   |   |-- talairach.m3z
|   |   |   |   |   |-- talairach_with_skull.lta
|   |   |   |   |   |-- talairach.xfm
|   |   |   |   |   `-- talsrcimg_to_711-2C_as_mni_average_305_t4_vox2vox.txt
|   |   |   |   |-- wm.asegedit.mgz
|   |   |   |   |-- wm.mgz
|   |   |   |   |-- wmparc.mgz
|   |   |   |   `-- wm.seg.mgz
|   |   |   |-- scripts
|   |   |   |   |-- build-stamp.txt
|   |   |   |   |-- lastcall.build-stamp.txt
|   |   |   |   |-- patchdir.txt
|   |   |   |   |-- pctsurfcon.log
|   |   |   |   |-- pctsurfcon.log.old
|   |   |   |   |-- ponscc.cut.log
|   |   |   |   |-- recon-all.cmd
|   |   |   |   |-- recon-all.done
|   |   |   |   |-- recon-all.env
|   |   |   |   |-- recon-all.local-copy
|   |   |   |   |-- recon-all.log
|   |   |   |   `-- recon-all-status.log
|   |   |   |-- stats
|   |   |   |   |-- aseg.stats
|   |   |   |   |-- lh.aparc.a2009s.stats
|   |   |   |   |-- lh.aparc.DKTatlas.stats
|   |   |   |   |-- lh.aparc.pial.stats
|   |   |   |   |-- lh.aparc.stats
|   |   |   |   |-- lh.BA_exvivo.stats
|   |   |   |   |-- lh.BA_exvivo.thresh.stats
|   |   |   |   |-- lh.curv.stats
|   |   |   |   |-- lh.w-g.pct.stats
|   |   |   |   |-- rh.aparc.a2009s.stats
|   |   |   |   |-- rh.aparc.DKTatlas.stats
|   |   |   |   |-- rh.aparc.pial.stats
|   |   |   |   |-- rh.aparc.stats
|   |   |   |   |-- rh.BA_exvivo.stats
|   |   |   |   |-- rh.BA_exvivo.thresh.stats
|   |   |   |   |-- rh.curv.stats
|   |   |   |   |-- rh.w-g.pct.stats
|   |   |   |   `-- wmparc.stats
|   |   |   |-- surf
|   |   |   |   |-- lh.area
|   |   |   |   |-- lh.area.mid
|   |   |   |   |-- lh.area.pial
|   |   |   |   |-- lh.avg_curv
|   |   |   |   |-- lh.curv
|   |   |   |   |-- lh.curv.pial
|   |   |   |   |-- lh.defect_borders
|   |   |   |   |-- lh.defect_chull
|   |   |   |   |-- lh.defect_labels
|   |   |   |   |-- lh.inflated
|   |   |   |   |-- lh.inflated.H
|   |   |   |   |-- lh.inflated.K
|   |   |   |   |-- lh.inflated.nofix
|   |   |   |   |-- lh.jacobian_white
|   |   |   |   |-- lh.orig
|   |   |   |   |-- lh.orig.nofix
|   |   |   |   |-- lh.pial
|   |   |   |   |-- lh.qsphere.nofix
|   |   |   |   |-- lh.smoothwm
|   |   |   |   |-- lh.smoothwm.BE.crv
|   |   |   |   |-- lh.smoothwm.C.crv
|   |   |   |   |-- lh.smoothwm.FI.crv
|   |   |   |   |-- lh.smoothwm.H.crv
|   |   |   |   |-- lh.smoothwm.K1.crv
|   |   |   |   |-- lh.smoothwm.K2.crv
|   |   |   |   |-- lh.smoothwm.K.crv
|   |   |   |   |-- lh.smoothwm.nofix
|   |   |   |   |-- lh.smoothwm.S.crv
|   |   |   |   |-- lh.sphere
|   |   |   |   |-- lh.sphere.reg
|   |   |   |   |-- lh.sulc
|   |   |   |   |-- lh.thickness
|   |   |   |   |-- lh.volume
|   |   |   |   |-- lh.w-g.pct.mgh
|   |   |   |   |-- lh.white
|   |   |   |   |-- lh.white.H -> lh.white.preaparc.H
|   |   |   |   |-- lh.white.K -> lh.white.preaparc.K
|   |   |   |   |-- lh.white.preaparc
|   |   |   |   |-- lh.white.preaparc.H
|   |   |   |   |-- lh.white.preaparc.K
|   |   |   |   |-- rh.area
|   |   |   |   |-- rh.area.mid
|   |   |   |   |-- rh.area.pial
|   |   |   |   |-- rh.avg_curv
|   |   |   |   |-- rh.curv
|   |   |   |   |-- rh.curv.pial
|   |   |   |   |-- rh.defect_borders
|   |   |   |   |-- rh.defect_chull
|   |   |   |   |-- rh.defect_labels
|   |   |   |   |-- rh.inflated
|   |   |   |   |-- rh.inflated.H
|   |   |   |   |-- rh.inflated.K
|   |   |   |   |-- rh.inflated.nofix
|   |   |   |   |-- rh.jacobian_white
|   |   |   |   |-- rh.orig
|   |   |   |   |-- rh.orig.nofix
|   |   |   |   |-- rh.pial
|   |   |   |   |-- rh.qsphere.nofix
|   |   |   |   |-- rh.smoothwm
|   |   |   |   |-- rh.smoothwm.BE.crv
|   |   |   |   |-- rh.smoothwm.C.crv
|   |   |   |   |-- rh.smoothwm.FI.crv
|   |   |   |   |-- rh.smoothwm.H.crv
|   |   |   |   |-- rh.smoothwm.K1.crv
|   |   |   |   |-- rh.smoothwm.K2.crv
|   |   |   |   |-- rh.smoothwm.K.crv
|   |   |   |   |-- rh.smoothwm.nofix
|   |   |   |   |-- rh.smoothwm.S.crv
|   |   |   |   |-- rh.sphere
|   |   |   |   |-- rh.sphere.reg
|   |   |   |   |-- rh.sulc
|   |   |   |   |-- rh.thickness
|   |   |   |   |-- rh.volume
|   |   |   |   |-- rh.w-g.pct.mgh
|   |   |   |   |-- rh.white
|   |   |   |   |-- rh.white.H -> rh.white.preaparc.H
|   |   |   |   |-- rh.white.K -> rh.white.preaparc.K
|   |   |   |   |-- rh.white.preaparc
|   |   |   |   |-- rh.white.preaparc.H
|   |   |   |   `-- rh.white.preaparc.K
|   |   |   |-- tmp
|   |   |   |-- touch
|   |   |   |   |-- aparc.a2009s2aseg.touch
|   |   |   |   |-- aparc.DKTatlas2aseg.touch
|   |   |   |   |-- apas2aseg.touch
|   |   |   |   |-- asegmerge.touch
|   |   |   |   |-- ca_label.touch
|   |   |   |   |-- ca_normalize.touch
|   |   |   |   |-- ca_register.touch
|   |   |   |   |-- conform.touch
|   |   |   |   |-- cortical_ribbon.touch
|   |   |   |   |-- em_register.touch
|   |   |   |   |-- fill.touch
|   |   |   |   |-- inorm1.touch
|   |   |   |   |-- inorm2.touch
|   |   |   |   |-- lh.aparc2.touch
|   |   |   |   |-- lh.aparcstats2.touch
|   |   |   |   |-- lh.aparcstats3.touch
|   |   |   |   |-- lh.aparcstats.touch
|   |   |   |   |-- lh.aparc.touch
|   |   |   |   |-- lh.avgcurv.touch
|   |   |   |   |-- lh.curvstats.touch
|   |   |   |   |-- lh.final_surfaces.touch
|   |   |   |   |-- lh.inflate1.touch
|   |   |   |   |-- lh.inflate2.touch
|   |   |   |   |-- lh.inflate.H.K.touch
|   |   |   |   |-- lh.jacobian_white.touch
|   |   |   |   |-- lh.pctsurfcon.touch
|   |   |   |   |-- lh.pial_surface.touch
|   |   |   |   |-- lh.qsphere.touch
|   |   |   |   |-- lh.smoothwm1.touch
|   |   |   |   |-- lh.smoothwm2.touch
|   |   |   |   |-- lh.sphmorph.touch
|   |   |   |   |-- lh.sphreg.touch
|   |   |   |   |-- lh.surfvolume.touch
|   |   |   |   |-- lh.tessellate.touch
|   |   |   |   |-- lh.topofix.touch
|   |   |   |   |-- lh.white.H.K.touch
|   |   |   |   |-- lh.white_surface.touch
|   |   |   |   |-- nu.touch
|   |   |   |   |-- relabelhypos.touch
|   |   |   |   |-- rh.aparc2.touch
|   |   |   |   |-- rh.aparcstats2.touch
|   |   |   |   |-- rh.aparcstats3.touch
|   |   |   |   |-- rh.aparcstats.touch
|   |   |   |   |-- rh.aparc.touch
|   |   |   |   |-- rh.avgcurv.touch
|   |   |   |   |-- rh.curvstats.touch
|   |   |   |   |-- rh.final_surfaces.touch
|   |   |   |   |-- rh.inflate1.touch
|   |   |   |   |-- rh.inflate2.touch
|   |   |   |   |-- rh.inflate.H.K.touch
|   |   |   |   |-- rh.jacobian_white.touch
|   |   |   |   |-- rh.pctsurfcon.touch
|   |   |   |   |-- rh.pial_surface.touch
|   |   |   |   |-- rh.qsphere.touch
|   |   |   |   |-- rh.smoothwm1.touch
|   |   |   |   |-- rh.smoothwm2.touch
|   |   |   |   |-- rh.sphmorph.touch
|   |   |   |   |-- rh.sphreg.touch
|   |   |   |   |-- rh.surfvolume.touch
|   |   |   |   |-- rh.tessellate.touch
|   |   |   |   |-- rh.topofix.touch
|   |   |   |   |-- rh.white.H.K.touch
|   |   |   |   |-- rh.white_surface.touch
|   |   |   |   |-- rusage.mri_ca_register.dat
|   |   |   |   |-- rusage.mri_em_register.dat
|   |   |   |   |-- rusage.mri_em_register.skull.dat
|   |   |   |   |-- rusage.mris_fix_topology.lh.dat
|   |   |   |   |-- rusage.mris_fix_topology.rh.dat
|   |   |   |   |-- rusage.mris_inflate.lh.dat
|   |   |   |   |-- rusage.mris_inflate.rh.dat
|   |   |   |   |-- rusage.mris_register.lh.dat
|   |   |   |   |-- rusage.mris_register.rh.dat
|   |   |   |   |-- rusage.mris_sphere.lh.dat
|   |   |   |   |-- rusage.mris_sphere.rh.dat
|   |   |   |   |-- rusage.mri_watershed.dat
|   |   |   |   |-- segstats.touch
|   |   |   |   |-- skull.lta.touch
|   |   |   |   |-- skull_strip.touch
|   |   |   |   |-- talairach.touch
|   |   |   |   |-- wmaparc.stats.touch
|   |   |   |   |-- wmaparc.touch
|   |   |   |   `-- wmsegment.touch
|   |   |   `-- trash
|-- participants.json                          # Participants demography in json format 
|-- participants.tsv                   # Participants demography in tsv format
|-- README                           # References for how to convert M-EEG data to BIDS format
|-- sub-CA103                           # Subject folder
|   `-- ses-1                           # Session/visit 1 (Experiment 1)
|       |-- anat                   # Anatomical data folder
|       |   |-- sub-CA103_ses-1_T1w.json  # Anatomical landmark coordinates for LPA: Left Preauricular Point, NAS: Nasion, RPA: Right Preauricular Point
|       |   `-- sub-CA103_ses-1_T1w.nii.gz  # T1-weighted anatomical data
|       |-- meg                           # MEG data folder
|       |   |-- sub-CA103_ses-1_acq-calibration_meg.dat # Generic data file containing raw or unprocessed data acquired during a calibration session
|       |   |-- sub-CA103_ses-1_acq-crosstalk_meg.fif # MEG data recorded during the crosstalk session
|       |   |-- sub-CA103_ses-1_coordsystem.json # Contains information on MEG coordinate system, units, head coil and anatomical landmark coordinates
|       |   |-- sub-CA103_ses-1_task-dur_run-01_channels.tsv # Contains information on the channel names, types, units, sampling rate, status, and frequency cutoffs of the filter applied to the recorded data
|       |   |-- sub-CA103_ses-1_task-dur_run-01_events.json # Contains information about the events/stimuli presented during Experiment 1, run 1 such as the event onset time, event code (trigger code), and event's category
|       |   |-- sub-CA103_ses-1_task-dur_run-01_events.tsv # Contains the same information as json file in tsv format
|       |   |-- sub-CA103_ses-1_task-dur_run-01_meg.fif  # Contains the raw/preprocessed MEG data for Experiment 1/session 1, run 1
|       |   |-- sub-CA103_ses-1_task-dur_run-01_meg.json
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
|       |   |-- sub-CA103_ses-1_task-noise_channels.tsv
|       |   |-- sub-CA103_ses-1_task-noise_meg.fif
|       |   |-- sub-CA103_ses-1_task-noise_meg.json
|       |   |-- sub-CA103_ses-1_task-rest_channels.tsv
|       |   |-- sub-CA103_ses-1_task-rest_meg.fif
|       |   `-- sub-CA103_ses-1_task-rest_meg.json
|       `-- sub-CA103_ses-1_scans.tsv
```

   </td>
  </tr>
