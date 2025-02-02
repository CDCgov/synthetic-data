# FHIRSheets

FhirSheetsiIs a command-line tool that reads an Excel file in FHIR cohort format and generates FHIR bundle JSON files from it. Each row in the template Excel file is used to create an individual JSON file, outputting them to a specified folder.

## Table of Contents
- [FHIRSheets](#fhirsheets)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [License](#license)

## Features
- Reads an Excel file following the FHIR cohort import template.
- Converts each row in the Excel file to a FHIR bundle JSON file.
- Exports generated JSON files to a specified output folder.

## Requirements
- Python 3.x
- Required Python packages (see `requirements.txt`)

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/CDCgov/synthetic-data.git
   cd fhir-python-cohort-generation
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
## Usage
1. **Fill Out the Template:**
   - Open the template file `src/resources/Fhir_Cohort_Import_Template.xlsx`.
   - Fill out each row with the relevant data.

2. **Run the Tool:**
   - Use the `fhirsheets.py` script with the required arguments:
     - `--input`: The path to the input Excel file.
     - `--output`: The path to the output folder where the JSON files will be saved.

   ```bash
   python fhirsheets.py --input src/resources/Fhir_Cohort_Import_Template.xlsx --output /path/to/output/folder
3. The tool will generate one FHIR bundle JSON file for each row defined in the template.

## Example

```bash
python fhirsheets.py --input src/resources/Fhir_Cohort_Import_Template.xlsx --output ./output_bundles
In this example, each row in the `Fhir_Cohort_Import_Template.xlsx` file will be processed, and a corresponding JSON file will be generated in the `output_bundles` folder.
```

## License
This project is licensed under the MIT License. See the `LICENSE` file for more information.