--- Unit Converter Microservice ---

This Python program serves as a simple microservice for unit conversion. 
It reads input from a specified text file, performs unit conversion based on the provided format, and writes the result to another text file. 

The conversion is specified in the format 'xyz', where:
    x is the starting unit (1 for grams, 2 for oz, 3 for lbs),
    y is the unit to convert to (1 for grams, 2 for oz, 3 for lbs), and
    z is the amount to be converted.

--- USAGE ---
Modify the filepaths in unitConverter.py to point to the desired input and output files.
    - INPUT_FILEPATH: Path to the text file from which the input will be read (e.g., inputService.txt).
    - OUTPUT_FILEPATH: Path to the text file where the output will be written (e.g., outputService.txt).

Run the program from the command line:
    python unitConverter.py

Place the conversion requests in the specified input file.
The program will continuously monitor the input file. 
Upon detecting content, it will perform the conversion, write the result to the output file, and clear the input file.

--- SENDING DATA ---
To send data, the user must write a string onto the specified input file that it points to.
Suppose you want to convert 150 grams to ounces with the input file being inputService.txt.
In Python, you would write:
    f = open('inputService.txt', 'w', encoding="utf-8")
    f.write('1125')

--- RECEIVING DATA ---
To receive data, the user must provide an output file that is a text file. This is where the data is eventually printed onto.
Suppose you want to receive data from the output text file named outputService.txt.
In Python, you would write:
    f = open('outputService.txt', 'r', encoding="utf-8")
    data = f.read()
Inside the variable data, will be the result '5.29 oz' as a string.

--- NOTE ---
- The program is loaded with an example inputService and outputService as well as an example on how to make a request.
- The program uses an infinite loop to continuously check for input content.
- The conversion factors are predefined within the script for grams to ounces, grams to pounds, ounces to grams, ounces to pounds, pounds to grams, and pounds to ounces.
- If the conversion units are invalid, the program writes 'Invalid conversion units' to the output file.

```mermaid
sequenceDiagram
    participant dotcom
    participant iframe
    participant viewscreen
    dotcom->>iframe: loads html w/ iframe url
    iframe->>viewscreen: request template
    viewscreen->>iframe: html & javascript
    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```
