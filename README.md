# 1 Data representation

## 1.1 Number systems

- how and why computers use binary to represent all forms of data
  - Any form of data needs to be converted to binary to be processed by a computer
  - Data is processed using logic gates and stored in registers

- denary, binary and hexadecimal number systems
  - Denary is a base 10 system, uses digits 0-9, unit increase by power of 10
  - Binary is a base 2 system, uses 0 and 1, unit increase by power of 2
  - Hexadecimal is a base 16 system, uses 16 characters 0-F, unit increase by power of 16

- conversion between binary, denary and hexadecimal
  - for conversion between binary and hexadecimal, convert 4 binary bits to one hexadecimal
  - for conversion from bin/hex to denary, multiply each digit by its powered value in the table
  - for conversion from denary to bin/hex, use a power table or successive division method

- how and why hexadecimal is used as a beneficial method of data representation
  - Area of use: IP address, MAC address, Colour Code in HTML/CSS, error code, memory address
  - Hexadecimal is easier for humans to understand than binary, as it is a shorter representation of the binary, easier to identify if two values are the same by human.

- Binary addition

- Overflow
  - A computer or a device has a predefined limit that it can represent or store
  - An overflow error occurs when a value outside this limit should be returned
  - for 8-bit register the limit is 255

- Logical shift
  - Bits shifted from the end of the register are lost and zeros are shifted in at the opposite end of the register
  - The positive binary integer is multiplied or divided according to the shift performed
  - The most significant bit(s) or least significant bit(s) are lost, when 1s is shifted out, the value become incorrect

- Twos Complement
  - conversion between positive/negative denary and twos complement binary
  
## 1.2 Text, sound and images

- text
  - Text is converted to binary using character set.
  - Unicode allows for a greater range of characters and symbols than ASCII, including different languages and emojis
  - Unicode requires more bits per character than ASCII
  - ASCII represents characters using 8-bit binary numbers
  - Unicode represents characters using 16-bit binary numbers

- sound
  - how to store sound
    - Sound value is recorded at each time sample
    - Each sound value is converted to binary
    - Binary is stored in a sequence
  - sound metadata
    - The sample rate is the number of samples taken in a second
    - The sample resolution is the number of bits per sample
    - The accuracy of the recording and the file size increases as the sample rate and resolution increase

- image
  - how to store image
    - Images are made up of pixels
    - Each pixel have a colour
    - the colour can be represent by a unique binary number
    - binary numbers are stored in a sequence
  - metadata of image
    - The resolution is the number of pixels in the
image
    - The colour depth is the number of bits used to represent each colour
    - The file size and quality of the image increases as
the resolution and colour depth increase

## 1.3 Data storage and compression

- units of measurement

|unit    |abbr|conversion    |
|-       |-   |-             |
|bit     |-   |1 binary digit|
|nibble  |-   |4 bit         |
|byte    |-   |8 bit         |
|kibibyte|KiB |1024 bytes    |
|mebibyte|MiB |1024 KiB      |
|gibibyte|GiB |1024 MiB      |
|tebibyte|TiB |1024 GiB      |
|pebibyte|PiB |1024 TiB      |
|exbibyte|EiB |1024 PiB      |

- calculate size of file
  - size of image = image resolution \* colour depth
  - size of audio = sample resolution \* sample rate \* duration

## Data compression

- Compression is to reduce the size of the file
- benefit
  - less bandwidth required
  - less storage space required
  - shorter transmission time
- types of compression
  - lossy
    - reduce the file size by permanently removing data
    - e.g., reducing resolution or colour depth, reducing sample rate
    - quality is lost
    - cannot recover the original file
    - smaller file than lossless compression
or resolution
  - lossless
    - Lossless compression reduces the file size without permanent loss of data
    - can restore the original file
    - usually used for text
    - Run Length Encoding is an example of lossless compression
      - group together repeated elements
      - store how many times they occur and the element value

# 7 Algorithm design and problem-solving

- program development life cycle
  - analysis: abstraction, decomposition of the problem, identification of the problem and requirements
  - design: decomposition, structure diagrams, flowcharts, pseudocode
  - coding: writing program code and iterative testing
  - testing: testing program code with the use of test data

- computer system is made up of sub-systems, which are made up of further sub-systems

- a problem can be decomposed into its component parts
  - inputs
  - processes
  - outputs
  - storage

- methods to design and construct a solution to a problem
  - structure diagrams
  - flowcharts
  - pseudocode

- Explain the purpose of a given algorithm
  - stating the purpose of an algorithm
  - describing the processes involved in an algorithm
- Identify errors in given algorithms

- Standard methods of solution
  - totalling
  - counting
  - finding maximum, minimum, average

- validation
  - validation is checking the input data to make sure it is reasonable, and/or within set bounds
  - choose the most suitable validation check for given scenario
    - range check
    - length check
    - type check
    - presence check
    - format check
    - check digit
  - implement validation check in algorithms

- verification
  - verification is a check that user has copied the data accurately
  - types of verification:
    - visual check
    - double entry check

- testing
  - tests are carried out to make sure the program
    - fully works
    - does not crash
    - meets all requirements
  - types of test data
    - Normal: data that the program should accept
    - Abnormal: data that the program should not accept
    - Extreme: data that is at the edge of what is allowed
    - Boundary: data that is on the edge of being accepted and being rejected
  
- trace table
  - complete a trace table from pseudocode or flow chart
  - each column is designated to one variable
  - could have another column for outputs

# 8 pseudocode & python writing

- code run in sequence, one line at a time
- data types:
  - pseudocode: `INTEGER`, `REAL`, `CHAR`, `STRING`, `BOOLEAN`
  - python: `int`, `float`, `str`, `bool`
- variable assignment:
  - pseudocode: `x <- 1`
  - python: `x = 1`
- output
  - pseudocode: `OUTPUT "Result is ", x`
  - python: `print("Result is ", x)`
- input
  - pseudocode: `INPUT x`
  - python: `x = input("please input x")`
  - input in python is string, if numeric value needed, use float() or int()
    - `x = int(input("please input x"))`
- selection
  - pseudocode: `IF`/`ENDIF` and `CASE OF`/`ENDCASE`
  - python: `if`, `elif`, `else`
- iteration:
  - count-controlled loops
    - pseudocode: `FOR i <- x TO y`
    - python
  - pre-condition loops
    - pseudocode: `WHILE`/`DO`/`ENDWHILE`
    - python: `while`
  - post-condition loops
    - pseudocode: `REPEAT`/`UNTIL`
    - only pre-condition in python
- arithmetic:

|arithmetic|pseudocode|python|
|-|-|-|
|addition|+|+|
|subtraction|-|-|
|multiplication|*|*|
|division|/|/|
|power of|^|**|
|integer division (get whole number and discard remainder)|DIV()|//|
|modulation(get remainder)|MOD()|%|

- comparison
  - `<`, `<=`, `>`, `>=` in both languages
  - in pseudocode we use `=` for "equal to" and `<>` for "not equal to
  - in python we use `==` for "equal to" and `!=` for "not equal to
  - boolean operators
    - psdudocode: `AND`, `OR`, `NOT`
    - python: `and`, `or`, `not`

- string manipulation
  - "Hello" is a string literal. It could be replaced by a string variable.
  - length
    - pseudocode: `LENGTH("Hello")`
    - python: `len("Hello")`
  - case
    - pseudocode: `LCASE("Hello")`, `UCASE("Hello")`
    - python: `"Hello".lower()`, `"Hello".upper()`
  - substring
    - pseudocode: `SUBSTRING("Hello", 2, 3)` return `"ell"`
      - first number is start index, first character has index 1
      - second number is the length of substring taken
    - python: `"Hello"[1:4]` return "ell"
      - first number is the start index, first character has index 0
      - second number is the end index, character at this index excluded in substring
- flow chart

![flow chart](https://user-images.githubusercontent.com/24235850/204455632-7b9e5d08-eca8-4402-8a79-0debf5e9c6ed.png)

# 10 logic gates

- complete the rest from one of
  - logic circuit
  - logic expression
  - truth table
  - all three from a problem statement
- key points
  - Do NOT simplify the circuits
  - Use a dot to show a junction in circuit
  - To complete a truth table, add labels to middle outputs, work out middle outputs first

- types of logic gate

![logic gate](https://user-images.githubusercontent.com/24235850/204453786-bb36ed00-4459-4c2f-b9eb-c66ffabd1dc3.png)
