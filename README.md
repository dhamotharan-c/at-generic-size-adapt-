# Generic Size Adapt Automation Tool

This tool automates the resizing of InDesign (INDD) documents based on specifications provided in a CSV file.  It eliminates the need for manual resizing, saving significant time and effort, especially when dealing with multiple size variations.

## How it Works

1. **Input:**
    * **Master InDesign File (INDD):** The source document to be resized.
    * **CSV File:** Contains the desired output sizes. Each row specifies width, height, and optionally, output file name and other settings.

2. **Processing:**
    * The tool opens the master INDD file.
    * It reads the CSV file row by row.
    * For each row, it resizes the document to the specified dimensions.
    * It saves the resized document to the output folder.

3. **Output:** Resized InDesign documents are saved in the specified output folder.

## Components

* **Master INDD File:** The source InDesign document.
* **CSV File:** Contains size specifications (see format below).
* **Output Folder:** The directory where resized INDD files are saved.

## CSV File Format

Width,Height,OutputFileName (Optional),OtherSettings (Optional) 100,200,output_100x200.indd 300,400,output_300x400.indd 500,600,output_500x600.indd ...


* **Width:** Output document width (consistent units, e.g., mm, pixels).
* **Height:** Output document height.
* **OutputFileName:** Custom output file name (optional).
* **OtherSettings:** Additional parameters (optional, implementation-dependent).

## Error Handling

The tool includes error handling for:

* Invalid CSV format
* Missing master INDD file
* Incorrect size specifications
* Write permissions in the output folder

Clear error messages are displayed to the user.

## License

This project is licensed under the [MIT License](LICENSE.md). (If you have a license file)
