| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-C6 | ESP32-H2 | ESP32-P4 | ESP32-S2 | ESP32-S3 |
| ----------------- | ----- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |

# SD Card example (SDSPI)

This code is based on the original SD card example.

It has been tested to work on ESP32-C6.

All the original "helper functions" have been extracted from the ESP IDF code and placed manually in to the sdcard_main.c file. They are prefixed s_sdcard_ and, if I recall correctly, followed by the original example helper function name.

This README.md was created long after I'd created this test program, so my memory is fuzzy.

In its simple terms, the program does the following:

Test and initialise the card if needed.
If found print the previous log file.
Position to the end of the log file.
Write more log file.
End.

On each restart this means that the log file gets bigger and bigger.

There is no requirement for the sdkconfig to exist as all the original menuconfig options have been moved in to the code.

I think, if I recall,