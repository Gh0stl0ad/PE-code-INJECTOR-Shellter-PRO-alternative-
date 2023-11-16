# PE Code Injector (Havoc PRO alternative)

## Overview

This Python script serves as a powerful tool for injecting custom shellcode into Windows PE (Portable Executable) files, offering an alternative to traditional techniques like Shellter Pro. It is specifically crafted for penetration testers and ethical hackers, enabling them to enhance their arsenal by injecting code into executable files discreetly. This tool facilitates the addition of a new section to the target executable, allowing for the injection of tailored code to achieve various objectives during penetration testing.
## Price and where to buy it

Price: 18$
Url: https://satoshidisk.com/pay/CJtea0

## Features

-   **Covert Shellcode Injection**: The script provides a covert means of injecting custom shellcode into a specified offset within the target executable. This feature is valuable for penetration testers aiming to stealthily modify the behavior of binaries.
    
-   **Entry Point Manipulation**: Users can selectively modify the entry point of the executable or keep it unaltered based on the requirements of the penetration test.
    
-   **Automatic Section Creation**: The tool automatically creates a new section within the executable to accommodate the injected shellcode, ensuring a seamless integration into the target binary.
    
-   **Resizable Executable**: The script dynamically resizes the executable file to ensure ample space for the injected code, offering flexibility in the size and complexity of the injected payloads.
    

## Usage

### Requirements

-   Python 3
-   `pefile` library (install via `pip install pefile`)

### Command Line Usage


`python script.py inject2exe --exe <PATH_TO_EXE> --shellcode <PATH_TO_SHELLCODE> --offset <HEX_OFFSET> --output <OUTPUT_PATH>` 

**Options:**

-   `--no-ep`: Retain the original entry point.
-   `--offset`: Specify the hex offset value for injection.
-   `--output`: Specify the path for the output file.

## Examples

### Basic Usage


`python script.py inject2exe --exe target.exe --shellcode payload.bin --offset 0x1000 --output modified.exe` 

### Stealthy Operation



`python script.py inject2exe --exe target.exe --shellcode stealth_payload.bin --offset 0x2000 --output covert_modification.exe --no-ep` 
