# Tutorials

This repository contains two tutorials for my [PhD lab books](https://aylinsgl.github.io/lab-books/). 
For all tutorials we will use EEG data from my project ["Object representations reflect hierarchical scene structure and depend on high-level visual, semantic, and action information." (Aylin Kallmayer, Leila Zacharias, Luisa Jetter, Melissa Le-Hoa Võ)](https://doi.org/10.31234/osf.io/hs835)

Please first download the epoched data here [here](https://www.dropbox.com/scl/fi/001hjyw0r9lf6ezuynv5t/Archive.zip?rlkey=xhmini6w1xg30rjqvbh7u1xe5&st=lqpvfcra&dl=0) and move it to the `data/` folder.

Once downloaded and unzipped you have access to eeg epoch and ica files for each participant:

    .
    📦SceneGrammarEEG
     ┣ 📂sub-01
     ┃ ┣ 📂eeg
     ┃ ┃ ┣ 📜sub-01-ica.fif
     ┃ ┃ ┣ 📜sub-01_repaired-False-epo.fif
     ┃ ┃ ┗ 📜sub-01_repaired-True-epo.fif
     ┃ ┣ 📂cross_decoding
     ┃ ┣ 📂decoding
     ┣ 📂sub-02
     ┃ ┣ 📂eeg
     ┃ ┃ ┣ 📜sub-02-ica.fif
     ┃ ┃ ┣ 📜sub-02_repaired-False-epo.fif
     ┃ ┃ ┗ 📜sub-02_repaired-True-epo.fif
     ┗...

Each folder contains:
- eeg files:
    - ICA files (.fif): Independent Component Analysis files for artifact correction.
    - Epoch files (.fif): EEG epochs, both repaired and non-repaired, for further analysis.

It also contains decoding and cross-decoding results, which are not relevant for this tutorial because we will implement our own pipelines to create results.

## Preprocessing Details

raw eeg data was processed using ICA to remove eog related components automatically and repairing epochs using autoreject. It was decimated to a frequency of 250Hz.

## Experiment Details

For more details on the experiment and conditions, please refer to the paper or [here](https://aylinsgl.github.io/lab-books/projects/project-2/)
