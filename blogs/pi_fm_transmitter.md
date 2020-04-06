## Rasberry Pi FM Tranmitter

All you need is a Rasberry Pi and the correct software and commands.

I used a Rasberry Pi 3 Model B Rev 1.2.
If you dont know which PI you have you can run 
```markdown
cat /proc/device-tree/model
```
result
```markdown
Raspberry Pi 3 Model B Rev 1.2
```

Operating system
I used Rasbian 9 (stretch)
If you dont know which OS you have you can run 
```markdown
cat /etc/os-release|grep PRETTY_NAME
```
result
```markdown
PRETTY_NAME="Raspbian GNU/Linux 9 (stretch)"
```

Software :

First up we need the [FM Transmiter software](https://github.com/markondej/fm_transmitter)
With a terminal make a directory to store the software then download it
```markdown
mkdir PI_FM
```
```markdown
cd PI_FM
```
```markdown
git clone https://github.com/markondej/fm_transmitter
```
Installing :

We need to check we have all dependencies to build the software
```markdown
sudo apt-get install gcc g++ make
```
Then we can build
```markdown
cd fm_transmitter/
```
```markdown
sudo make
```

If you can complete all these commands succesfully then you are DONE.

Setup of microphone for live voice transmitting :

I used an old USB webcam microphone (Logitech C310)




Examples using the software :

To transmit a .wav file 
```markdown
sudo ./fm_transmitter -f 100 -r acoustic_guitar_duet.wav
```
-f is the frequency you want to transmit on (100 Mhz)
-r is to repeat the file
*acoustic_guitar_duet.wav was a demo file available at time of downloading software













