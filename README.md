# BCI Competition 2020 Track 5 — ERP during walking (scalp, ear-EEG, and IMU)

## Overview

This dataset comprises EEG recordings from 15 healthy participants performing a visual P300 oddball task while walking on a treadmill at 1.6 m/s. The study includes simultaneous scalp-EEG (46 channels), ear-EEG (14 channels, 7 per ear), electrooculography (4 channels), and inertial measurement unit recordings (6 channels: 3-axis accelerometer and gyroscope) sampled at 100 Hz. Data were collected as part of BCI Competition 2020 Track 5 to evaluate brain-computer interface performance under ambulatory conditions, with trials temporally divided into training, validation, and test sets.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 15 |
| Channels | 46 |
| Classes | 2 |
| Trial length | 1 s |
| Sampling frequency | 100 Hz |
| Sessions | 1 |
| Total trials | 4500 |
| Paradigm | P300 |

## Data Collection Methods

Participants performed a visual oddball P300 paradigm with target ('OOO') and non-target ('XXX') stimuli (target ratio 0.2) while walking on a treadmill at 1.6 m/s. EEG was recorded from 46 scalp channels (standard 10-20 montage) plus 14 ear-EEG channels (7 per ear), 4 EOG channels, and 6 IMU channels (3-axis accelerometer and gyroscope) at 100 Hz sampling rate. Data were epoched from -190 ms to +800 ms around stimulus onset.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import BCIComp2020WalkingERP
from moabb.paradigms import P300
paradigm = P300()

dataset = BCIComp2020WalkingERP()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.BCIComp2020WalkingERP.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.3389/fnhum.2022.898300](https://doi.org/10.3389/fnhum.2022.898300)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
