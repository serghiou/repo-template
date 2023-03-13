# README

## Authors

Stelios Serghiou, Eirini Tsekitsidou

## Publication

When we have the preprint or publication, we will post the link here!

## File structure

Combining resources across OSF and GitHub should yield the following structure.

```
├── .gitignore          <- Lists files to be ignored in syncing between local and remote.
├── LICENSE             <- Describes license to the contents of this repo.
├── README.md           <- Describes the project and orchestration (how to run)
├── data
│   ├── raw             <- The original, immutable data dump.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   ├── external        <- Data from third party sources (e.g., US Census).
│   │   └── <provider>
│   │   │   └── <date>
│   ├── conformed       <- Intermediate data that has been transformed.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   ├── extracted       <- Tabular data extracted from image data.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   └── tidy            <- The final, canonical datasets for analysis.
│   │   └── <experiment>
├── code
│   ├── data_processing <- Code to process data from raw all the way to tidy.
│   │   └── <experiment>
│   ├── draft           <- Code for draft data analytics and visualizations.
│   ├── final           <- Code to produce text, figures and tables as they appear in pubilcations.
├── output
│   ├── draft           <- Tables and figures from the draft analytics
│   │   └── <experiment>
│   ├── final           <- Tables and figures from the final analytics
├── references          <- Data dictionaries, manuals, and all other explanatory materials.
├── requirements.txt    <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
├── publication                      
│   ├── journal                      <- Journal that this was submitted to
│       ├── submission-1_YYYY-MM-DD  <- All materials of submission 1
│           ├── docs                 <- All documents for submission
│           ├── figures              <- All figures for submission
│           ├── tables               <- All tables for submission
```

## Code structure

All code follows the following structure.

```
├── Title
│   ├── Inputs         <- Define the input sources.
│   ├── Outputs        <- Define the outputs.
├── Setup
│   ├── Import         <- Import modules.
│   ├── Parameters     <- Input parameters (e.g., source files)
│   ├── Configs        <- Input any configurations (e.g., from a config file).
│   └── Functions      <- Define all functions.
├── Read
│   ├── Import         <- Import data.
│   ├── Conform        <- Conform data to a format appropriate for analysis.
├── Compute
│   ├── Compute        <- Compute descriptive statistics, visualize, analyze.
├── Write
│   ├── Conform        <- Conform data to a format appropriate for storage.
│   ├── Export         <- Write/push/sink data to a storage service.
```

## How to run

To run this code, use the following diagramatic acyclic graph (DAG). Note that this applies for each experiment.

![How to run diagram](https://github.com/serghiou/centrosomal-calcineurin/blob/main/how-to-run.jpg?raw=true)


## How to get help

If you encounter a bug, please file an issue with a minimal reproducible example [here](https://github.com/serghiou/centrosomal-calcineurin/issues) and please Label it as a "bug" (option on the right of your window). For help on how to use the package, please file an issue with a clearly actionable question [here](https://github.com/serghiou/centrosomal-calcineurin/issues) and label it as "help wanted." For all other questions and discussion, please email the first author.

## Be a good citizen

If you like or are reusing elements of this repo, please give a star!
