# DoradoM1
Instructions on installing ONT Dorado on Mac M1 machines:
## Installation
Download [this](https://cdn.oxfordnanoportal.com/software/analysis/dorado-0.2.1-osx-arm64.tar.gz) file and put it in the desired directory.
## Required Dependencies
If homebrew is not installed on your system, follow the instructions from the [homebrew](https://brew.sh/) website for installation.
```
brew install hdf5 libaec zstd openssl autoconf@2.69
brew link hdf5 libaec zstd openssl autoconf@2.69
```
This is probably not the most efficient, but for Dorado to work for me it wasn't until all of these were downloaded and linked that it ran.

## Xcode Installation
Download the [Xcode](https://developer.apple.com/download/all/) developer to run Dorado. This allows Dorado access to metal. Once it installed and licences have been accepted and whatnot, run this line.
```
sudo xcode-select --switch {PATH_TO_XCODE_IN_APPLICATIONS_FOLDER}/Contents/Developer
```
## Verification
Once all of this has been downloaded navigate to the Dorado folder to verify it is executable.
```
cd {PATH_TO_DORADO}/bin
./dorado -h
```
The output should look like this:
```
Usage: dorado [options] subcommand

Positional arguments:
basecaller
download
duplex

Optional arguments:
-h --help               shows help message and exits
-v --version            prints version information and exits
-vv                     prints verbose version information and exits
```
# Enjoy basecalling!
