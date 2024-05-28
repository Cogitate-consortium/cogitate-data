# Overview of COGITATE

What are the mechanisms that give rise to consciousness? This question has been the focus of extensive research, leading to the development of several prominent theories, including Global Neuronal Workspace Theory (GNWT) and Integrated Information Theory (IIT). Critically, however, the focus so far has been on testing each theory independently, gathering evidence for/against them separately, leaving open a crucial question: which theory has higher explanatory power when tested against each other directly?

COGITATE is a pioneering Open Science adversarial collaboration to bridge this gap and evaluate GNWT and IIT through two studies, named [Experiment 1](#experiment-1-conscious-perception) (EXP1) and [Experiment 2](#experiment-2-video-game-engagement) (EXP2). In these experiments, multimodal empirical tests are conducted on human volunteers, combining magneto-electroencephalography (M-EEG), functional magnetic resonance imaging (fMRI) and intracranial electrocorticography (iEEG) along with behavioral and eye tracking measurements. The reason for this approach is to maximize the sensitivity and specificity to the tests of each hypothesis, while accounting for trade-offs between temporal and spatial specificity inherent to the currently available methods in human neuroscience.

![Cogitate overview graphic](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.1/graphics_v1.1/overview_graphic_2024-04-26_v1.1.png)

## Goals

The aim of the COGITATE project is to accelerate research on consciousness and establish a groundbreaking model for scientific practices in cognitive neuroscience at large, by demonstrating the impact of team-based adversary research and open data to address some of the major riddles in the field, much like established practices in other fields of inquiry such as physics and genomics.

Furthermore, the resulting products of this research include a large and unique multimodal database, high-end analysis tools, and a new paradigm for probing consciousness in naturalistic settings. All experimental procedures, multimodal datasets, and analysis tools developed in this project will be made openly available to the public. These products will propel further discoveries in the field of consciousness, and in cognitive neuroscience in general, which will exceed and outlast the direct outputs of the proposed studies.

## Experiments

The COGITATE consortium performed two experiments:

In [Experiment 1](#experiment-1-conscious-perception) (EXP1), two sets of clearly visible task relevant and irrelevant stimuli were shown to the subjects with different durations. The goal was to test the effects of maintenance of a percept in consciousness and task relevance and contradictory predictions regarding the involvement of prefrontal and posterior, category selective cortical areas in consciousness. Specifically, the main questions were: _How is the persistence of a stimulus in consciousness reflected in cortical hemodynamic and electrophysiological activity, i.e., are the neural responses phasic or sustained throughout a conscious experience? Do activity patterns in prefrontal areas relate to visual consciousness per se or to its consequences, i.e., task-related processes?_

In [Experiment 2](#experiment-2-video-game-engagement) (EXP2), a novel paradigm was developed to test the key predictions of GNWT and IIT while overcoming a major obstacle in the field: _creating more naturalistic conditions of invisibility that do not degrade the physical input._ To achieve this goal, an engaging video game was used with the help of which salient stimuli were presented for relatively long durations in the background. Sometimes the stimuli was not consciously seen due to attentional engagement by the game. This approach allowed us to uniquely study neural activity elicited by seen or unseen stimuli under naturalistic conditions so that the stimuli can either be task relevant or task irrelevant.

### Experiment 1: Conscious Perception

#### Objective

The primary aim of this experiment was to investigate neural activity in response to stimuli that are consciously perceived. It was designed to manipulate two key factors:

1. **Relevance of the Stimulus to the Task:** This factor was categorized into three levels—Task-relevant target, Task-relevant non-target, and Task-irrelevant stimulus.
2. **Stimulus Duration:** The stimuli were presented for durations of 500 ms, 1000 ms, and 1500 ms

This design framework allowed us to test several key hypotheses, including:

- Disentangling consciousness-related activations from task-related activations.
- Identifying brain regions that convey information about the content of consciousness.
- Examining the persistence of the content of consciousness over time.

#### Design

This experiment followed a 3x3x4x2 factorial design, with the following items:

|                                           |                                                                                                    |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Relevance of Stimulus to the Task (3)** | - Task-relevant target<br>    <br>- Task-relevant non-target<br>    <br>- Task-irrelevant stimulus |
| **Stimulus Duration (3)**                 | - 500 ms<br>    <br>- 1000 ms<br>    <br>- 1500 ms                                                 |
| **Stimulus Category (4)**                 | - Faces<br>    <br>- Objects<br>    <br>- Letters<br>    <br>- False-fonts (meaningless symbols)    <br><br>*20 identities for each category   |
| **Stimulus Orientation (2)**              | - Side view (25% right and 25% left)<br>    <br>- Front view (50%)                                           |

#### Sample Size

The sample sizes were determined based on common practices in the literature, resulting in a total of 122 subjects for fMRI, 102 for M-EEG, and 38 for iEEG. All subjects met specific criteria, including age and health conditions, to ensure data quality.

#### Task Description

A sequence of images including faces, objects, letters or meaningless symbols (‘false fonts’) with front or side (left or right) view were presented to the subjects. At the beginning of each sequence, the target images were presented and subjects were asked to memorize and remember them during the sequence. Subjects were instructed to press any buttons with their index finger when they saw targets (in either front or side views) as quickly and accurately as possible.

The duration of each sequence was approximately 2 minutes. The next sequence started when the subjects pressed the space key. Here is an example of the tasks:

![Experiment 1](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/Experiment%201%20-%20paradigm%20figure%20v1.png)

___
For a comprehensive summary of more details about the experiments, please refer to the following supplementary resources:

[COGITATE Main Scientific Paper 1 (MSP-1)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0268577)

[COGITATE Preregistration, v4](https://osf.io/gm3vd)

[EXP1 Demo Video](https://www.youtube.com/watch?v=V93Agvo4G2Y)
___

### Experiment 2: Video Game Engagement

Currently in preparation. It will be released soon!

#### Task Code and Stimuli repositories

The **task code** and **stimuli** used for EXP1 and for all modalities are available in the [cogitate-experiment-code](https://github.com/Cogitate-consortium/cogitate-experiment-code) repository.
