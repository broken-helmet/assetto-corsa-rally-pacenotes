AC Rally Pacenote Pal
=====================

Pacenote Pal is an application for Assetto Corsa Rally that replaces the in-game codriver with an external one.
This way you can use custom voices, edit the pacenotes per stage, and change the timing.

A demo can be found here: https://youtu.be/Quq5dFNgtvQ

**This software is nowhere near finished** and has many rough edges.

How it works
------------

1. Set the audio for the in-game spotter to 0%
2. Start the program
3. Select your stage
4. Press start 
5. Drive to the start of the stage. As the countdown starts, press the space bar. You will hear a beep

Adding a voice can be done by adding a folder in the folder `voices`. Changing the pacenotes can be done by 
editing the YAML files in the `pacenotes` folder, or adding a new file.

Changing settings
-----------------

All settings can be found in the `config.yml` file.

Creating your own pacenotes from scratch
----------------------------------------

Create an empty YAML file for your pacenotes in the `pacenotes` folder, e.g. `My Notes.yml`. 
Add a single empty pacenote to it and save the file, i.e.:
```
- distance: 0
  link_to_next: false
  notes: []
```
When you (re)start Pacenote Pal, you should see the file in the list. Select it and press start.
Now you can start the stage as normal and start making your pacenotes.

A pacenote consists of three things:
1. `distance` - This is the distance into the stage for this pacenote in metres. Press the "Distance" button to
show the current distance. The codriver will call out this pacenote some time before the pacenote, so you do not 
have to keep that into account.
2. `link_to_next` - Whether when the notes from the current pacenote are called out, the next one will be called 
out immediately after it as well. 
3. `notes` - A list of the audio files to call out at this pacenote. The notes are the audio files from the voices
folder, and you can also add your own audio files if you want notes that are not in the game (e.g. sumppu). If the
file does not exist it will be skipped. The audio files have to be .wav.



Thanks to
---------
pyaccsharedmemory.py is based on https://github.com/rrennoir/PyAccSharedMemory