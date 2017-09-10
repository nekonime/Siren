# Siren
📣 Siren is a simple JavaScript wake word library.

## "Okay... why tho?"
Good question! At the moment, AFAIK, there is no way to use a wakeword for Tal Ater's amazing JavaScript voice recognition library, [Annyang](https://github.com/TalAter/annyang). So, not wanting to run two full copies of his script, I decided to make my own which *should* be lighter, just as fast, and easily capable of detecting a single wakeword.

## The Two Versions
`siren.annyang.js` is the original, lightest, and simplest version. It comes ready to use with Annyang without any function calling on your part. (Calls `annyang.start();` on word detection.)

`siren.general.js` is the more fully featured version, which DOES support Annyang as well, but can be more easily used with whatever other function you want to call, upon hearing your trigger word.

## Usage
Annyang version: `siren({ trigger: "your-wake-word", locale: "en-US" });`

General version: `siren({ trigger: "your-wake-word", advance: "function-to-execute();", locale: "en-US" });`

`trigger` is the word that Siren will listen for.

`advance` is the function that you want Siren to execute upon hearing your trigger word.

`locale` (optional) will tune the Speech engine to better interpret accents. See [here](http://nekoni.me/language-codes)

Re-enabling Siren after your function is finished is as simple as calling `siren.start();`, or `siren.forceStart();` if using Annyang. The latter will call `annyang.abort();` before re-enabling Siren with `siren.start();`. Or you could just run those yourself seperately. You do you, fam.

## TO-DO
- Figure out what to write under "To-do"
