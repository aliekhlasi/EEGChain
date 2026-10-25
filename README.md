[![](https://img.shields.io/badge/DOI-10.1109/ICBME64381.2024.10895852-blue)](https://doi.org/10.1109/ICBME64381.2024.10895852)
[![DOI](https://zenodo.org/badge/867418734.svg)](https://doi.org/10.5281/zenodo.13888486)
# EEGChain: An Open-Access EEGLAB-based Toolbox for Building, Managing, Automating, and Reproducing Batch EEG Processing Pipelines

## About

**EEGChain** is a MATLAB graphical tool, built on [EEGLAB](https://sccn.ucsd.edu/eeglab/), for building and running EEG preprocessing pipelines without writing code. You build a pipeline from ready-made **processing blocks**, set each block's parameters in the GUI, and save the whole pipeline as a configuration file. The same pipeline can then be loaded again and applied to **many datasets in batch**. This makes preprocessing consistent across subjects, easy to share, and reproducible.

**Available processing blocks:**
- **Filtering:** high-pass and low-pass filters (`pop_eegfiltnew`)
- **Line-noise removal:** CleanLine
- **Re-referencing**
- **Channel and epoch rejection:** manual, or automatic with `clean_rawdata`
- **Channel interpolation**
- **ICA:** decomposition and component removal
- **Inspection:** signal browsing, power spectrum and scalp topography

**Execution modes:**
- *Interactive:* stop after each block to inspect the data and decide.
- *Automated:* run the whole pipeline over all loaded datasets without stopping.

Each step's output is saved in its own numbered folder (`step 1__…`, `step 2__…`), so every intermediate result can be checked.

## Getting started

**Requirements:** MATLAB, and EEGLAB with the *clean_rawdata*, *CleanLine* and *ICLabel* plugins.

```matlab
addpath('/path/to/eeglab'); eeglab nogui;          % load EEGLAB
addpath(genpath('/path/to/EEGChain/code'));         % add EEGChain
eegchain                                            % open the EEGChain window
```

Two example pipeline configurations are included in `code/utilities/sample/`.

**Original repository:** [fardinafdideh/EEGChain](https://github.com/fardinafdideh/EEGChain) (F. Afdideh). The animated demonstrations below are hosted there.
* A convenient GUI-based EEG (pre-)processing pipeline management system;
* Loading pre-stored pipeline configurations to ensure consistent signal processing and reproducibility;
* Interactive GUI for selection, rearrangement, and customization of processing blocks from the EEGLAB toolbox;
* Offering both interactive and automated pipeline execution modes, providing flexibility in processing control;
* Easy creation of pipelines by adding, removing, or rearranging pipeline building blocks;
* Adjusting the parameters of each pipeline building block through the easy-to-use GUI of EEGChain;
* The same pipeline can be applied to multiple imported EEG datasets in batch, in an automated way.

##  ICBME 2024
![](/ppt/ICBME2024.PNG)

##  EEGChain Layout
![](/ppt/EEGChain-parts.png)

###  A) Processing Blocks

###  B) (Re)-Arranging the Processing Blocks
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/creation.gif)

###  C) Loading Pre-stored Pipeline Configurations
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/configImport.gif)

###  D) Processing Pipeline

###  E) Processing Blocks Parameters
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/parameterSetting.gif)

###  F) Naming and Storing the Created Pipeline Configuration
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/config.gif)

###  G) Interactive v.s. Automated Pipeline Execution Mode
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/interactive.gif)

###  H) Raw Data Path

###  I) Dataset Loading
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/dataImportManual.gif)
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/dataImportMat.gif)

###  J) Dataset Removing
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/dataRemove.gif)

###  K) Pipeline Execution
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/startRunning.gif)
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/batchProc.gif)

###  L) Accessing the Results Directory
![](https://github.com/fardinafdideh/EEGChain/raw/main/ppt/open.gif)

## EEGChain
![Slide1](/ppt/GUI.gif)

## EEGChain Functionalities
![Slide2](/ppt/Slide2.PNG)
![Slide3](/ppt/Slide3.PNG)
![Slide4](/ppt/Slide4.PNG)
![Slide5](/ppt/Slide5.PNG)
![Slide6](/ppt/Slide6.PNG)
![Slide7](/ppt/Slide7.PNG)
![Slide8](/ppt/Slide8.PNG)
![Slide9](/ppt/Slide9.PNG)
![Slide10](/ppt/Slide10.PNG)

# How to cite
* **F. Afdideh**, M. Boozari, A. Ekhlasi, A. M. Nasrabadi, “EEGChain: An Open-Access EEGLAB-based Toolbox for Building, Managing, Automating, and Reproducing Batch EEG Processing Pipelines,” 31st National and 9th International Iranian Conference on Biomedical Engineering ([ICBME](https://ieeexplore.ieee.org/document/10895852)), 20–27, 2024. https://doi.org/10.1109/ICBME64381.2024.10895852. 
* **F. Afdideh**, M. Boozari, A. Ekhlasi, A. Motie Nasrabadi, (2024), “fardinafdideh/EEGChain: v0.0”, (v0.0), [Zenodo](https://doi.org/10.5281/zenodo.13888486). https://doi.org/10.5281/zenodo.13888486.
* **F. Afdideh**, M. Boozari, A. Ekhlasi, A. M. Nasrabadi, “EEG Signal Cleaning Pipeline Management: EEGLAB-based,” *in preparation* (listed on the [EEGLAB website](https://eeglab.org/tutorials/11_Scripting/automated_pipeline.html#other-eeglab-pipelines)).
