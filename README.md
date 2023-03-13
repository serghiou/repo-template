# README

## File structure

Combining resources across OSF and GitHub should yield the following structure.

```
├── .gitignore
├── LICENSE
├── README.md          <- Describes the project and orchestration (how to run)
├── data
│   ├── raw            <- The original, immutable data dump.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   ├── external       <- Data from third party sources (e.g., US Census).
│   │   └── <provider>
│   │   │   └── <date>
│   ├── conformed      <- Intermediate data that has been transformed.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   ├── extracted      <- Tabular data extracted from image data.
│   │   └── <experiment>
│   │   │   └── <conditions/replicate>
│   │   │   │   └── <date>
│   └── tidy           <- The final, canonical datasets for analysis.
│   │   └── <experiment>
├── code
│   ├── data           <- Code to process data from raw all the way to tidy.
│   │   └── <experiment>
│   ├── draft          <- Code for draft data analytics and visualizations.
│   ├── final          <- Code to produce text, figures and tables as they appear in pubilcations.
├── output
│   ├── draft          <- Tables and figures from the draft analytics
│   │   └── <experiment>
│   ├── final          <- Tables and figures from the final analytics
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
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

![alt text](https://github.com/serghiou/centrosomal-calcineurin/how-to-run-diagram.jpg?raw=true)


## How to contribute

## Be a good citizen

If you like or are reusing elements of this repo, please give a star!

## References
