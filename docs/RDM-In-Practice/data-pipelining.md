# Data Pipelining

A data pipeline is a series of (automated) actions that ingests raw data from various sources and moves the data to a destination for storage and (eventual) analysis.

Benefits of a data pipeline include:

- Time saved by automating the boring stuff!
- Reduced mistakes.
- Tasks broken down into smaller steps.
- Reproducibility!

## When do I need a data pipeline?

Here's a rule of thumb, just as an example:

If you have a task that needs to occur >= 3 times, you could think about automating it.

If automation is not possible, think about how you can make the task as efficient as possible.

## How can I implement a data pipeline? Some examples for inspiration

- If you data collection tools have APIs, they can be leveraged to extract data.

- For example, Qualtrics has the qualtRics R package & pyQualtrics Python library which contain functions to automate exporting surveys.

- If APIs are not available, you could use R/Python to automate the use of an internet browser using the RSelenium package / Selenium library. Imagine automating the clicks and typing of going to a specific website, logging in, clicking the download button.

- You can use Windows Task Scheduler / cron / the taskscheduleR R package / cronR to schedule your scripts to run automatically, on a recurring basis as well (if needed).

- You can also send emails with R & Python! Consider if you've ever had to contact participants because you noticed something wrong with their incoming data. You could implement these data checks with a script and automatically draft and send emails (from a template) to those participants who were flagged as having issues with their data.

## QualtRics R package

```
library(readr)
library(qualtRics)

qualtrics_api_credentials(api_key = "YOUR-QUALTRICS-API-KEY", 
                          base_url = "YOUR-QUALTRICS-BASE-URL",
                          overwrite = TRUE,
                          install = TRUE)

readRenviron("~/.Renviron")

surveys <- all_surveys() 

survey_results <- fetch_survey(surveyID = surveys$id[2], # you can also replace surveys$id[2] with "<SUVREY-ID>" 
                                  verbose = TRUE)

write_csv(survey_results, paste0("path/to/folder/", format(Sys.time(), "%d-%m-%Y-%H.%M"), "_survey_results.csv"))
```

## taskscheduleR package

```
library(taskscheduleR)

scheduled_script <- "path/to/folder/myscript.R"

## run script once within 120 seconds

taskscheduler_create(taskname = "extract-data-once", rscript = scheduled_script,
                     schedule = "ONCE", starttime = format(Sys.time() + 120, "%H:%M"))

## Run every 5 minutes, starting from 10:40

taskscheduler_create(taskname = "extract-data-5min", rscript = scheduled_script,
                     schedule = "MINUTE", starttime = "10:40", modifier = 5)

## delete tasks

taskscheduler_delete("extract-data-once")
```