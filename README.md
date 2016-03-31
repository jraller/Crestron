# Crestron
SIMPL+ modules

## settings-from-file.usp

This module allows you to load settings from a file. The file can be loaded to the processor using the Toolbox File Manager. The default path and filename is \User\settings.txt.

Add additional digital or serial values with ALT+.

Values in the file need to consist of:

[start of line][string]:[value][end of line]

and any lines that do not match this format will be ignored. This allows you to add comments documenting the file.

When loading in digital values you can create a NOT for each of them, and then pass both the raw and NOTed version through a buffer controlled by the load_os signal. These can be passed into Toggles such that the raw buffered version goes to [set] and the NOTed buffered version goes to [reset] and clock is the driving button from the UI.

When loading strings for use with numeric-string-to-analog.usp us a Make String Permanent symbol.

### Roadmap

add the ability to have both identifier and default value in the parameter -- in design, to be completed in April 2016

## numeric-string-to-analog.usp

This can be combined with settings-from-file.usp to allow the loading of analog values.
