# Changelog
All notable changes to this project will be documented in this file.

## [v1.2.0-beta](https://github.com/deadbits/securitytrails-python3/releases/tag/v1.2.0-beta) - 2019-04-25
### Added
- Added url verification if user changes base_url
- Standardization of logging across all functions

### Changed
- Changed "session" to be a private variable
- Changed "parse_output" to be a private variable

## [v1.0.0-beta] - 2019-03-31
### Added
- All HTTP requests to be within try/except's
- Syntax highlighted JSON output if using `pretty_print`

### Changed
- All strings and print functions to use f-strings
- Changed docstrings for all functions to use @param format
- All prints are now functions
- Exception raise's now use new custom messages
- Changed URL building code to avoid code duplication and unneeded variable creation


[v1.0.0-beta]: https://github.com/deadbits/securitytrails-python3/releases/tag/v1.0.0-beta
