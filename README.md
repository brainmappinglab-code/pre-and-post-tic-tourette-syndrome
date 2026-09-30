# Analysis scripts for: Pre- and Post-Tic Network States in Tourette Syndrome
MATLAB analysis scripts for LFP and behavioral analyses examining pre- and post-tic network dynamics in Tourette syndrome using intracranial recordings from the centromedian thalamus (CM) and the anterior globus pallidus internus (aGPi) in 7 participants.

This repository contains the codes accompanying our paper for event construction, data segmentation, signal preprocessing, statistical analysis of annotated LFP data. Patient-level, group-level data and outputs from analysis are not included in this public repository.

Code written by Grace Lowor.

## Required Packages
1. perceive (https://github.com/neuromodulation/perceive)
2. fieldtrip (https://www.fieldtriptoolbox.org/)
3. shadedErrorBar
4. davionplot (https://www.mathworks.com/matlabcentral/fileexchange/74851-daboxplot)

## Repository Layout
```
.
├── scripts/                        # Reusable MATLAB analysis *.mlx  and *.m scripts
├── data/                           # Local/private data, ignored by git
│   ├── raw/                        # Raw .json LFP files and corresponding video labels (.mat) for each participant
│   ├── perceived/                  # .mat LFP files, if perceive is run and corresponding video labels (.mat) for each participant...
│   │   ├──LeftIPG/                 # for the left and...
│   │   └──RightIPG/                # right hemisphere       
│   ├── preprocessed/               # .mat connectivity files for each hemisphere of each participant...
│   │   ├──LeftIPG/                 # if prePostTic_Analysis_Left.mlx is run...
│   │   └──RightIPG/                # if prePostTic_Analysis_Right.mlx
│   ├── surrogate/                  # .mat file if surrogateTicCoherence.mlx
│   └── all/                        # all .mat data outputs from preprocessed/ and surrogate/ for group analysis
└── groupResults/                   # Local/generated outputs, if groupAnalysis.mlx is run, ignored by git
    └── figures/
```

### Data Placement
After obtaining data ([DATA.MD](https://github.com/brainmappinglab-code/pre-and-post-tic-tourette-syndrome/blob/main/data/DATA.md)), the code assumes that the data are stored locally following the directory structure outlined above for consistency. At minimum, the analysis scripts allows the user to browse to whatever directory the data is/will be stored for data loading and saving. 

## Running
Install the MATLAB dependencies listed under **Required Packages** and add them to your path in MATLAB using the `addpath` MATLAB function.

See [scripts/README](https://github.com/brainmappinglab-code/pre-and-post-tic-tourette-syndrome/blob/main/scripts/README.md) for info about running each analysis script.
