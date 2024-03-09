# shrimp_mortality

View the rendered methods document here: [https://rethinkpriorities.github.io/shrimp_mortality/](https://rethinkpriorities.github.io/shrimp_mortality/)

## About
This is the supplemental methods document and files for our report on Pre-slaughter Mortality of Farmed Shrimp. It contains all of the data and code used for the analyses in the report.
The files render a quarto book that details the method and code we used. The book has three chapters covering:
1.  Modeling shrimp pre-slaughter mortality using survival curves
2.  Comparing our estimates to others found in the literature
3.  Comparing our estimates to mortality estimates for other farmed taxa and wild shrimp.

We focus on the most farmed species, *Penaeus vannamei*, *Penaeus monodon*, and *Macrobrachium rosenbergii*. Often data for the latter included *Macrobrachium nipponese*, so we group them under the label *Macrobrachium*.

## How to use
If you want to read through the methods document and see all of the code, view the rendered methods document.

If you would like to run the code yourself locally, download all of the files in the repository. Open the `shrimp_pre-slaughter_mortality.Rproj` file to begin. This will automatically set the working directory and warn if any packages need to be installed.

## Folders
- `docs` contains the rendered html files and other site files.

- `chapters` contains the .qmd files (Quarto markdown files) where the method and code are written.

- `data` contains the .csv data files used in the analyses. It contains three subfolders:
   - `comparison` data files for comparing shrimp mortality to the mortality of other species 
   - `guesstimate` data from [Waldhorn and Autric's (2023)](https://doi.org/10.31219/osf.io/b8n3t) [Guesstimate model](https://www.getguesstimate.com/models/21679) used to build our survival curves model
   - `survival_curves` contains data created in the Survival Curves model chapter (Chapter 1) and used in subsequent chapters

### data files 
| File name   ________________________________                                                                | Description _____________________________________________________________________                                                                           |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                `comparison` folder                                   |                                                                                                                                                                                                                            |
| cross-species_data.csv                                                                               | Data we collected from the literature on mortality rates, slaughter age, and slaughter weight of other farmed species, including chickens, carnivorous fish, insects, and non-shrimp crustaceans (lobsters, crabs, etc.).  |
|               `guesstimate` folder                                                                              |                                                                                                                                                                                                                            |
| die_on_farm_samples.csv                                                                              | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of shrimp who die on farms (including pre-slaughter mortality) by species.                                                                                       |
| macrobrachium_days_lived.csv monodon_days_lived.csv vannamei_days_lived.csv                          | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of days lived on average for each life stage (larval, postlarval, juvenile-subadult) of each species analyzed. Each species is in a separate file.               |
| macrobrachium_mortality_rates.csv         monodon_mortality_rates.csv              vannamei_mortality_rates.csv           | Raw Guesstimate model estimates (5000 samples) for the mortality rates of each life stage (larval, postlarval, juvenile-subadult) of each species. Each species is in a separate file.                                         |
| slaughtered_samples.csv                                                                              | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of shrimp slaughtered in 2020 by species. The file includes estimates for "other penaeids," but that data is not analyzed here.                                      |
|              `survival_curves` folder                                                                |                                                                                                                                                                                                                            |
| bystage_farmed_shrimp_model_probs.csv                                                                | Data estimated in the Survival Curves chapter for the probability of a shrimp dying in each life stage. All three taxa are in one file.                                                                                 |
| macro_model_slaughter_probs.csv monodon_model_slaughter_probs.csv vannamei_model_slaughter_probs.csv | Data estimated in the Survival Curves chapter for the probability of a shrimp reaching slaughter age. Each species is in a separate file. 'macro' refers to *Macrobrachium*.                                                 |
| macro_totalfarmed_days.csv monodon_totalfarmed_days.csv vannamei_totalfarmed_days.csv                | Data estimated in the Survival Curves chapter for the length of the farming cycle for each species. Each species is in a separate file. 'macro' refers to *Macrobrachium*.                                                   |


