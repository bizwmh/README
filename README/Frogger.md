# Frogger
## Overview
Frogger is a tool to help you organize the files on your computer and attached external 
drives.  
It takes a configuration file (simply called the Frogger configuration) as input.  
The Frogger confiuguration consists of a set of parameters in key-value format.  
With these parameters the user tells Frogger which action it has to execute.  
As output Frogger generates a report about all files processed in the job.  
Additionally Frogger can perform file system operations, mainly copying files.
## The Frogger Configuration
### General
Frogger configurations are stored in the 'conf' sub folder with the extension '.conf'.  
The default configuration file is 'Frogger.conf'.  
A configuration parameter value can be of one of 2 types:
* String  
key = value denotes a single valued parameter
+ List of strings  
key = [value1, value2, ...] denotes a multi-valued paramter

If a value contains one of the special characters "${}:,*\", the value must be enclosed in double quotes.
### Paramter Descriptions

| Key         | Value Description
|:------------|:-----------------
| Input       | the path to an input directory     
|             | Frogger will process all files found in the given directory and sub-directories     
| Include     | a [Glob](https://docs.oracle.com/javase/tutorial/essential/io/fileOps.html#glob) pattern
|             | Frogger will only process files matching the given pattern.
| Exclude     | a [Glob](https://docs.oracle.com/javase/tutorial/essential/io/fileOps.html#glob) pattern
|             | Frogger will **not** process files matching the given pattern.
| Before      | a date in the format "dd.MM.yyyy"
|             | Frogger will only process which are older than the given date.
| Since       | a date in the format "dd.MM.yyyy"
|             | Frogger will only process which are younger than the given date.
| SkipSubTree | a [Glob](https://docs.oracle.com/javase/tutorial/essential/io/fileOps.html#glob) pattern
|             | Frogger will skip the processing of the directory matching the pattern.
## File Attributes
A Frogger report can contain the data for the below given file attributes.
### Regular Files
| Name         | Description
|:-------------|:-----------------
| Path         | The path to the parent folder of the file
| Name         | The name of the file
| Type         | The file type given as the file extension
| lastModified | The date when the file was last modified
| Size         | The size of the file in bytes
### Image Files
| Name        | Description
|:-------------------|:-----------------
|Aperture            |
|Color Space         |
|Date/Time original  |
|Date/Time digitized |
|Exposure Time       |
|Flash               |
|F-Number            |
|Focus               |
|Format              |
|Height              |
|ISO                 |
|Model               | 
|Shutter             |
|Width               |
|White Balance       |
|X-Resolution        |
|Y-Resolution        |