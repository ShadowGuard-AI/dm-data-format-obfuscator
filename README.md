![Banner](banner.png)

# dm-data-format-obfuscator
Transforms data into a visually similar but structurally different format to prevent direct interpretation. For example, converting JSON to XML with scrambled field names, or changing date formats unpredictably. - Focused on Tools designed to generate or mask sensitive data with realistic-looking but meaningless values

## Install
`git clone https://github.com/ShadowGuardAI/dm-data-format-obfuscator`

## Usage
`./dm-data-format-obfuscator [params]`

## Parameters
- `-h`: Show help message and exit
- `-i`: Path to the input file.
- `-o`: Path to the output file.
- `-t`: Type of transformation to apply (json_to_xml, date_obfuscation).

## Behavior notes
- The output file may not be the input file. If the resolved output path is the input file, by the same spelling or through a symlink, the run refuses at exit 1 before anything is written and the input is left untouched.
- A date_obfuscation run counts the dates it actually rewrites. If no value in the input is a date in the expected %Y-%m-%d form, the run prints "No dates were found or rewritten.", exits 1, writes no output file, and does not print the completion line.

## License
Copyright (c) ShadowGuardAI
