# voice-bits3-hsmm

A male German hidden semi-Markov model voice, built from voice recordings provided by the [BITS](http://www.bas.uni-muenchen.de/forschung/Bas/BasBITSLGDOC/HTML/BasGeneraleng.html) project at the [Bavarian Archive of Speech Signals](http://www.bas.uni-muenchen.de/)

## Prerequisites

You will need to have [Java](https://www.java.com/) installed.
On OSX with [Homebrew](http://brew.sh/), do
```
$ brew cask install java
```
as needed.

On Debian-based Linux (including Ubuntu), do
```
$ sudo apt-get install default-jdk
```
accordingly.

### Building the voice

To assemble, test, and package the voice for another MaryTTS installation, do
```
$ ./gradlew build
```
The packaged files will be placed under `build/distributions`.
Copy the zip file and xml descriptor into your MaryTTS installation's `download` directory, then run the `marytts-component-installer` to install the voice.

### Running the voice

To build the voice and run it in an ad-hoc MaryTTS server, do
```
$ ./gradlew run
```
Then, go to [http://localhost:59125](http://localhost:59125/).
