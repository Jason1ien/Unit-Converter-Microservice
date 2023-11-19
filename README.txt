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

--- EXAMPLE USAGE ---
Suppose you want to convert 150 grams to ounces. 
Place the following content in input file:
    1125
After running the program, you will find the result '5.29 oz' in the output file.

--- NOTE ---
- The program is loaded with an example inputService and outputService as well as an example on how to make a request.
- The program uses an infinite loop to continuously check for input content.
- The conversion factors are predefined within the script for grams to ounces, grams to pounds, ounces to grams, ounces to pounds, pounds to grams, and pounds to ounces.
- If the conversion units are invalid, the program writes 'Invalid conversion units' to the output file.

---- COMMUNICATION CONTRACT ----

1. Members will do all communication over Discord.

2. Members should respond within 24 hours over Discord. If a response cannot be made within 24 hours, they should communicate that ahead of time and let the other know the time frame at which they will be unavailable.

3. Members should keep each other updated on the progress of the microservice. If a delay in the microservice occurs, the individual is responsible for letting the other know ahead of time of any delays.

4. If a change needs to be made to the microservice, the members should notify each other 24 hours before the expected deadline of the microservice. Members should prevent last-minute changes if at all possible.

5. Members must notify each other about any current class status. Meaning if one decides to drop the class, they must give notice. Members should try their best to communicate and prevent ghosting.
