[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![preprint](https://img.shields.io/badge/preprint-https%3A%2F%2Fosf.io%2Fhgdvq%2F-orange)](https://osf.io/hgdvq/)
[![materials](https://img.shields.io/badge/materials-https%3A%2F%2Fosf.io%2Fn9uv4%2F-blue)](https://osf.io/n9uv4/)


# Readme for "Banana and *banane*: Cross-language phonological overlap supports bilingual toddlers’ word representations"

Created by [Esther Schott](https://github.com/e-schott) and [Charlotte Moore](https://github.com/CharlotteMoore927)

You can find the associated OSF project, including the stimuli used in the studies, at: [OSF LINK](https://osf.io/n9uv4/)

## Steps to replicate the analysis
1. open the ```CogMisp-24.Rproj``` file located in the root folder using RStudio
2. run renv::restore() to install the necessary packages
3. open & knit ```cm_manuscript.Rmd```


## Repository overview

**scripts** - this folder contains the scripts used to generate the analysis and manuscript. 

### Pre-processing steps that are not shared 
These scripts contain data with identifyable information (date of birth, date of participantion, non-random participant id) and are not shared:
- ```cm1_demog.Rmd``` reads in demographics & data cleaning for child ethnicity and maternal education
- ```cm2_merge.Rmd``` read in all participant info, merge, anonmyize participant naming, prep for merging with eye data, check that all participants are present

### Shared Scripts
- ```cm3_preprocessing.Rmd``` check for pre-data analysis exclusion criteria (health, language,..), do preparatory eyetracking steps  
- ```cm4_eyetracking_analysis.Rmd``` calculate descriptives on sample, eyetracking ANOVAs, some plots
- ```cm5_pupillometry.Rmd``` compute pupillometry analyses (for supplemental materials)
- ```cm6_growth_curves.Rmd``` compute growth curve analyses
- ```cm_manuscript.Rmd``` (in main directory) contains manuscript
- ```cm_supplement.Rmd``` (in main directry) supplemental materials for manuscript



**data** - this folder contains raw data inputs. 
- ***trial_info*** contains Stimuli, info on AOIs, items, trial orders (used in cm3 script)
- ***participant_info***   none of these are shared because they contain identifying information. for de-identified datasets for reanalysis, see ```results/processed data```


**results** this contains the processed data & output

- ***processed_data*** - This file contains preprocessed data

  + ```cm_merged_eye_data.Rdata``` output from cm2 script, input for ```cm3_preprocessing.Rmd```
  + ```cm_participant_info.Rdata.``` output from cm2 script, input for ```cm3_preprocessing.Rmd``` 
  + ```preprocessed_eye_data.Rdata``` output from cm3 script, input for ```cm4_eyetracking_analysis.Rmd``` and ```cm5_pupillometry.Rmd```
  + ```cm_target_words_known.csv``` questionnaire data on parent report of target words known, input for ```cm4_eyetracking_analysis.Rmd``` 

  + ```eye_data_binned_models.Rdata``` output from cm4 script, input for   ```cm6_growth_curves.Rmd``` 
  + ```eye_data_binned_plots.Rdata``` output from cm4 script, input for ```cm6_growth_curves.Rmd``` 


- **figures** - this folder contains figures generated by the analysis script.

