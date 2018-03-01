# Mighty-SoundBlaster
Recreation of famous Electronic, Electric, Reed, Theatre, and Pipe organs and their stops in OPL3 Synthesis.


# Intro
Today on "Stuff No One Asked For", we're going to make a playable organ out of a broken electronic organ, spare 90s PC parts, and a Creative Labs Sound Blaster 16! Or at least the stops for one, if it existed. Sadly, such a thing does not exist yet.

## MS-DOS Organ?
The SB16 has a YMF262 on board, which is a stereo 4-op FM synth chip. Here are the polyphony configurations it can be in:
1. 2-op mode - 18 voices
2. Double voice mode - 9 voices 
3. 4-op mode, minimum 12 voices

Rules of thumb:

* 4-op mode is a little tricky. each 4-op voice takes 2 2-op channels, to a maximum of 6. the remaining channels can be used as 2-op.
* Double voice mode sounds the best, but gives you only 9 voices maximum if you use only double voice mode stops.
* The lowest polyphony is 9 voices, which should be enough to handle most protestant hymns.

However, all of this can vary depending on the stops you use.

## Organ-ization
The Mighty SoundBlaster doesn't exist just yet, but here are the directories:
1. Solo
2. Swell 
3. Great
4. Choir
5. Pedal
7. Classics - Presets of the famous organs. This is when you want a specific sound from a specific organ, and fast. The Mighty Wurlitzer and Hammond B3 would be included here.
8. Electronic - These presets will imitate the (relatively) inexpensive electronic organs of the 70s, including Rhythmtones and Kimball Swingers. Expect your grandma's organ to be in here.
9. Reed - Several million free-reed organs and melodeons were made in the USA and Canada between the 1850s and the 1920s. They were the staple of in-house "sings", made popular by protestants settling in the American South and Midwest.
10. Combos: The stops in the first 5 directories with additional stops "added".

An example file name of a stop:
`Great - 8' Open Diapason.wopl`

## Issues and Limitations

* Not every organ treated every foundation stop the same. This is especially true with regards to electronic organs.
* Mutations and resultants will be included - eventually.
* For convenience, mixtures will be included as their own stops.
* No Crescendo pedal. How would you even implement such a thing?
* No dynamic stop modes.
* **NOTHING PROPERLY SUPPORTS THIS**. There *is* an Android Synth app that uses OPL3 synthesis and requires a MIDI controller to use, but not many phones and MIDI controllers support this.

The ultimate set-up for this would be a dedicated instrument, with one OPL3 chip per manual, but I have no idea how to design and fabricate any sort of board that would allow this. This is just a fun little exercise. Maybe if the voices were done, it would be enough inspiration.

## File format
File format for each instrument/stop will be in `WOPL`, which is the file format for FMBankEdit and the ADLMIDI fork (See my DMXOPL project for details). I have no idea if any VSTs use this format, sorry!
