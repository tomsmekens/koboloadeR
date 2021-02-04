## koboloadeR 0.1.9

 * changed all read.csv to read_csv to better address rendering of unicode characters
 
 * simplified the correlogram
 
 * parallelised crunching
 
 * fixed bug on select_multiple

## koboloadeR 0.1.8

  *  Re-factored the koboloadeR project structure so that it looks like a data package - R, data-raw, data - applying suggestions made here: https://raw.githubusercontent.com/statnmap/prez/master/2019-07_useR_Toulouse.pdf 

  
  *  Remove dependency to java - by switching to openxlsx package
  
  *  Included dependency to unhcRstyle package where all the brand style is managed - used now an argument to crunching report function
  
  *  Saving now all intermediary file as binary rda -- not yet tested fully...


## koboloadeR 0.1.7

  *  Added different output for the crunching report - docx, pptx, html, aspx
  
  *  Added an additional column in the dico to group questions in chapters within reports
  
  *  Added more explanation on the crunching report


## koboloadeR 0.1.6

  *  Added functions to generate dummy dataset
  
  *  Added example project
  
  *  Created and reviewed project documentation


## koboloadeR 0.1.5

  *  Added a shinapp to provide a gui for the package
 
  *  Turned previous scripts into functions


## koboloadeR 0.1.4

  *  Added a template for report generation in word as well as specific version of chart loop to be inserted in the report
 
  *  Add a function to split select_multiple - used within kobo_encode
 
  *  Fixed `kobo_projectinit` path to copy files

## koboloadeR 0.1.3

Forked from [https://github.com/mrdwab/koboloadeR](https://github.com/mrdwab/koboloadeR)

  *  Adding a `kobo_projectinit` function to set the data anlysis project folders, write the config file and add some analysis scripts.

  *  Adding a `kobo_form` function to get the form from the api. This includes 2 subfunctions: `kobo_dataset2` to have a better view of used forms & `kobo_forminfo` in order to get the form creater user name and pull it correctly from the API.

  *  Adding a `kobo_dico` function to parse the form and build a data dictionnary. The dictionnary is used to automatically generate graphs and maps. A inked functions is `kobo_label` that allows to recreate labels easily using the dictionnary.

  *  Adding a `kobo_label` function to add labels to variable using dictionnary

  *  Adding a `kobo_encode` function to re-encode variables as per dictionnary

  *  Adding a `kobo_bar_one` function to generate bar chart - frequency for all `select_one` questions

  *  Adding a `kobo_bar_multi` function to generate bar chart - frequency for all `select_multiple` questions

  *  Adding a `kobo_histo` function to generate histogramme for all `integer` questions

  *  Adding a `kobo_trend` function to generate histogramme for all `select_one` and `select_multiple` questions based 

  *  Adding a `kobo_bar_one_facet` function to generate bar chart for all `select_one` questions facetted on questions tagged as `facet` in the data analysis plan 

  *  Adding a `kobo_correlate` function to generate dot plot for all `integer` questions correlated with integer questions tagged as `correlate` in the data analysis plan 

  *  Added UNHCR Kobotoolbox server API and put it per default


## Before Fork

### koboloadeR 0.1.2

Testing `read_csv` wrapped in `setDT` to see whether it resolves issue #4.

### koboloadeR 0.1.1

The "data_viewer" Shiny app was added. 

### koboloadeR 0.1.0

KoBo Toolbox offers a convenient way to collect data using web and mobile forms. This package facilitates the retrieval of data entered using these tools using the KoBo Toolbox API (v1).

__MAIN FUNCTIONS__

  *  `kobo_datasets`
  *  `kobo_submission_count`
  *  `kobo_data_downloader`

__UTILITY FUNCTIONS__

  *  `kobo_time_parser_UTC`
  *  `kobo_time_parser`

__HELPER FUNCTIONS__

These are generally non-exported functions. Thus, you will need to prefix the functions with `koboloadeR:::` if you want to access them directly.

  *  `host`
  *  `get_me`
  *  `pwd_parse`
