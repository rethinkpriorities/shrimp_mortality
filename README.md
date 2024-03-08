# shrimp_mortality

View the rendered methods document here: 

## About
This is the supplemental methods document and files for our report on Pre-slaughter Mortality in Farmed Shrimp. It contains all of the data and code used for the analyses in the report.
The files render a quarto book that details the method used and code we used. The book has three chapter covering:
1.  Modeling shrimp pre-slaughter mortality using survival curves
2.  Comparing our estimates to others found in the literature
3.  Comparing our estimates to mortality estimates for other farmed taxa and wild shrimp.

We focus on the most farmed species, *Penaeus vannamei*, *Penaeus monodon*, and *Macrobrachium rosenbergii*. Often data for the later included *Macrobrachium nipponese*, so we group the under the label *Macrobrachium*.

## Files

`_book` contains the rendered html files.

`chapters` contains the .qmd files where the method and code are written.

`data` contains the .csv used in the analyses.
 - `comparison` data files for comparing shrimp mortality to the mortality of other species 
 - `guesstimate` data from [Waldhorn and Autric's (2023)](https://doi.org/10.31219/osf.io/b8n3t) Guesstimate model used to build our survival curves model
 - `survival_curves` contains data created in the Survival Curves model chapter (Chapter 1) and used in subsequent chapters

### data files 

| File name ___________________________                                                                | Description __________________________________________________________________                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **comparison folder**                                                                                |                                                                                                                                                                                                                            |
| cross-species_data.csv                                                                               | Data we collected from the literature on mortality rates, slaughter age, and slaughter weight of other farmed species, including chickens, carnivorous fish, insects, and non-shrimp crustaceans (lobsters, crabs, etc.).  |
| **guesstimate folder**                                                                               |                                                                                                                                                                                                                            |
| die_on_farm_samples.csv                                                                              | Guesstimate model estimates (5000 samples) for the number of shrimp who die on farms (including pre-slaughter mortality) by species.                                                                                       |
| macrobrachium_days_lived.csv monodon_days_lived.csv vannamei_days_lived.csv                          | Guesstimate model estimates (5000 samples) for the number of days lived on average for each life stage (larval, postlarval, juvenile-subadult) of each species analyzed. Each species is in a separate file.               |
| macrobrachium_mortality_rates.csv         monodon_mortality_rates.csv              vannamei_mortality_rates.csv           | Guesstimate model estimates (5000 samples) for the mortality rates of each life stage (larval, postlarval, juvenile-subadult) of each species. Each species is in a separate file.                                         |
| slaughtered_samples.csv                                                                              | Guesstimate model estimates (5000 samples) for the number of shrimp slaughtered in 2020, by species. File includes estimates for "other penaeids" but that data is not analyzed here.                                      |
| **survival_curves folder**                                                                           |                                                                                                                                                                                                                            |
| bystage_farmed_shrimp_model_probs.csv                                                                | Data estimated in the Survival Curves chapter for the probability of a shrimp dying in each life stage. All three taxa are in the on file.                                                                                 |
| macro_model_slaughter_probs.csv monodon_model_slaughter_probs.csv vannamei_model_slaughter_probs.csv | Data estimated in the Survival Curves chapter for the probability of a shrimp reaching slaughter age. Each species is in a separate file. 'macro' refers to Macrobrachium.                                                 |
| macro_totalfarmed_days.csv monodon_totalfarmed_days.csv vannamei_totalfarmed_days.csv                | Data estimated in the Survival Curves chapter for the length of the farming cycle for each species. Each species is in a separate file. 'macro' refers to Macrobrachium.                                                   |
