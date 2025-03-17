# Alto merger

A python notebook that merges a raw manual transcription on existing ALTO files. This project was created in the context of the DataLAC project on which I was tasked with improving an HTR model. 

The original goal of this project is to match a manual transcription stored in a csv file onto some ALTO XML files that where generated from an existing HTR model. This was useful to create a training dataset for the improved HTR model. However there may be other uses for it.

## How to use

### Setting environment variables

The notebook is setup to use a `.env` file with the following variables. You must create this file in order to run the script.

- `CSV_FILE_PATH`: path to the manual transcription file
- `ALTO_DIR_PATH`: path to the directory containing the ALTO files you wish to match to
- `OUTPUT_DIR_PATH`: path to the directory containing where you want the updated alto files saved to

### Structure of the csv file

Separators are set to `;` but you can easely change that.

The script is made to use a csv setup as such:

|Page|Line|Text|
|:--:|:--:|:--:|
|1|1|Lorem ipsum|

### Output

The script will create an output folder in your working directory were all matched files will be saved with their original name.