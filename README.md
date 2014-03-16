PiFMPlay
========
It's an addon for pifm (a program to transmit FM-Radio) for the raspberry pi mini computer.

PiFMPlay makes it easier to play music and control your FM-Broadcast.

PiFM is written by [Icrobotics](http://www.icrobotics.co.uk/wiki/index.php)

PiFMPlay is written by Mikael Jakhelln.
"It's not pretty, but it works."

This fork by Richard Parslow.

##How to use it:

First directly on your Pi or via ssh

Create a local directory in your home folder:
>mkdir pifm

Change to that directory:
>cd pifm

Get the latest version of pifm:
>wget http://omattos.com/pifm.tar.gz

Unpack the archive:
>tar -xvf pifm.tar.gz

Make pifm an executable:
>sudo chmod +x pifm

Save pifmplay to your pi (same folder as pifm e.g /home/pi/pifm).
Allow pifmplay an executable:
>sudo chmod +x pifmplay

Install sox and ffmpeg:
>sudo apt-get install ffmpeg sox libsox-fmt-all 

Attach an antenna to GPIO4 on your raspberry pi. (suggest using a GPIO Break-out board I use this one http://www.maplin.co.uk/p/gpio-break-out-pcb-for-raspberry-pi-n95nq)

###Test it:

>sudo sh pifmplay . 91.3

(91.3 is the default frequency, change it to whatever frequency you want to broadcast on.)

###Play a file with:

>sudo sh pifmplay "/path/to/file.mp3"

>sudo sh pifmplay "/path/to/file.m4a"

>sudo sh pifmplay "/path/to/file.wav"

this will play a file with pifm.

###Play a folder with:

>sudo sh pifmplay "/path/to/folder" 101.5

(this will play all files in the specified directory with pifm on frequency 101.5)

###How to Pause/Stop broadcast and skip songs:
Open another terminal.

>sudo sh pifmplay pause

>sudo sh pifmplay resume

>sudo sh pifmplay stop

>sudo sh pifmplay next

To control pifmplay from the same terminal, run pifm in the background:
>sudo sh pifmplay "/path/to/folder" &
(though you might want to remove the text output)

Check if there is an update to pifm here: 
[icrobotics.co.uk](http://www.icrobotics.co.uk/wiki/index.php/Turning_the_Raspberry_Pi_Into_an_FM_Transmitter)

Current version now offers stereo link is here (http://omattos.com/pifm.tar.gz)

####Wishes for the future versions of pifmplay:
- Redirect all sound output to pifmplay (redirect all alsa sound output).
- Youtube stream (might be possible with [youtube-dl](http://www.raspberrypi.org/phpBB3/viewtopic.php?p=97710))
- di.fm/soundcloud/spotify/pandora streaming

####If you get in trouble using this, IT'S YOUR OWN RESPONSIBILITY:
The raspberry pi can be made into a powerful fm-transmitter, if you filter and amplify the signal. 
But using a powerful fm-transmitter without a proper licence is illegal in most countries.
So if you break any laws and get fined for it, it's YOUR OWN FAULT!!
But it should be fine as long as you don't attach a big antenna to it, for example no longer than 20cm.
