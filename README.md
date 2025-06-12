# AnjLab Code Box - PLC Utility Library for CoDeSys

## Overview

AnjLab Code Box is a comprehensive PLC utility library designed for use with CoDeSys. It provides a collection of function blocks and functions that simplify common PLC programming tasks, including signal processing, time calculations, mathematical operations, string manipulation, and more.

## Features

### Signal Processing
- **Debounce Functions**: Filter noisy digital signals (`DebunceBoolIn`, `DebunceBoolInOut`, `DebunceBoolOut`)
- **Edge Detection**: Detect rising and falling edges with filtering (`DetectEdgeFiltered`)
- **Click Detection**: Detect double clicks and long presses (`DoubleClick`, `LongClick`)
- **PWM Generation**: Create PWM signals with configurable frequency and duty cycle (`PwmClock`, `PwmDc`, `PwmPw`)
- **Filtering**: Noise reduction filters for analog signals (`FilterNR`, `FilterTW`)

### Time and Date Utilities
- **Sun Position**: Calculate sunrise, sunset, and solar noon times (`SunPositionTimes`, `SunMidday`)
- **Date/Time Conversion**: Extensive functions for date and time manipulation (`DateToElements`, `DayOfWeek`, `DayOfYear`, etc.)
- **Time Calculations**: Difference between timestamps, week of year calculations, etc.

### Mathematical Functions
- **Rounding**: Ceil, floor, round, and truncate operations
- **Exponents**: Efficient power calculations (`ExpN`, `Exp10`)
- **Scaling**: Linear scaling of values (`ScaleReal`)
- **Random Numbers**: Pseudo-random number generation (`Random`)

### String Manipulation
- **Character Operations**: Count characters, remove substrings, case conversion
- **String Processing**: Various string utility functions

### Data Conversion
- **Bit Manipulation**: Count bits, toggle bits, load bits into bytes
- **Byte Swapping**: Swap bytes in words and dwords
- **IP Address Decoding**: Convert IP string to DWORD format

## Installation

1. Download the `.library` file from the releases section
2. Import the library into your CoDeSys project
3. Add the library to your application's dependencies

Alternatively, you can import any POU exported by the library directly into your project from the source PLCopen XML file.

## Usage

After installation, you can call any of the functions or function blocks from your PLC code. For example:

```iecst
// Example: Debounce a digital input
VAR
    fbDebounce: DebunceBoolIn;
    bFilteredOutput: BOOL;
END_VAR

fbDebounce(input := %IX0.0, output => bFilteredOutput);
```

## Requirements

- CoDeSys development environment (version compatible with PLCopen XML version 6.0.200)
- Target PLC that supports the standard function set used by the library

## License

Apache 2.0

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests with your improvements.

## Support

For support or feature requests, please open an issue on the GitHub repository.
