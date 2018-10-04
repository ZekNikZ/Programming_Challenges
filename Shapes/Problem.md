# Shapes
## Overview
Your task is to create a program which opens a user-specified file and draws certain shapes (made out of asterisks (`*`)) according to certain commands.
You will:
1. ask the user for a name of a file up to five times,
2. read each command from the file and execute them accordingly, and;
3. draw the result of each command to the screen and to an output file.
## Input File Format
The input file will begin with single line for comments, which shall be ignored for parsing.
Each subsequent line is guaranteed to contain a _command_, and one or more _arguments_. The possible commands are as follows:
- `RECTANGLE [height] [width]` - draws a _filled_ rectangle of asterisks of height `height` and width `width`.
- `TRIANGLE [height]` - draws a _filled_ triangle (with tip pointing upward) of asterisks of height `height`.
- `DIAMOND [width]` - draws a _hollow_ diamond of asterisks of width `width`. `width` will always be odd or zero.

You may assume that:
- Any command which is not one of the above can be safely ignored.
- Each line will contain a single command and the proper number of arguments for such command.
- Each command argument will be a nonnegative integer.
## Process
1. Prompt the user for an input file with the phrase `"Please enter a file name: "`. Read a file name from the user (echo-print the entered text).
2. If the file cannot be opened, respond with the phrase `"File cannot be opened."` and try again. If five such attempts have been made, respond with the phrase `"Maximum attempts reached."` and exit the program.
3. Skip the first line of the input file.
4. Read each command from the input file and display the specified shape to both the screen and write to the file `output.txt`, followed by a linefeed. See above for a command reference and below for examples on what the shapes should look like.
## Submission
Submit both a flowchart and C++ program which implements this program. Remember to abide by the proper documentation and programming style standards.
## Example Input and Output
Sample Input File (`input.data`):
```
This is a sample input file
RECTANGLE 6 4
TRIANGLE 5
DIAMOND 3
SQUARE 4
RECTANGLE 1 10
DIAMOND 1
TRIANGLE 2
DIAMOND 5
```

Sample Output 1:
```
Please enter a file name: input
File cannot be opened.
Please enter a file name: data
File cannot be opened.
Please enter a file name: input.txt
File cannot be opened.
Please enter a file name: Input.data
File cannot be opened.
Please enter a file name: bad_file_name
File cannot be opened.
Maximum attempts reached.

```

Sample Output 2:
```
Please enter a file name: input
File cannot be opened.
Please enter a file name: input.data

****
****
****
****
****
****

*
**
***
****
*****

 *
* *
 *

**********

*

*
**

  *
 * *
*   *
 * *
  *

```

Sample Output File 2 (`output.txt`)
```
****
****
****
****
****
****

*
**
***
****
*****

 *
* *
 *

**********

*

*
**

  *
 * *
*   *
 * *
  *

```
