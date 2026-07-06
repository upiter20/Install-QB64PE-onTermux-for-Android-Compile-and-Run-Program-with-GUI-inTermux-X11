# Install-QB64PE-onTermux-for-Android-Compile-and-Run-Program-with-GUI-inTermux-X11
This is manual on how to Install QB64 on Termux for Android, Compile and Run Program with GUI in Termux-X11

Install Termux for Android from F-Droid, not from Google Play.
https://f-droid.org/packages/com.termux/

Install Termux-X11 app for graphical output.
https://github.com/termux/termux-x11?ysclid=mqaw153gk8257962657




Open Termux terminal and install root-repo and X11-repo.



Use command "pkg install" to get these packages:
qb64/x11 for aarch64
freeglut/x11
mesa-dev/stable
termux-x11-nightly

More information on screenshots



Install Midnight Commander 
pkg install mc

Type command "mc" in Termux and after Midnight Commander is opened check that
QB64 after installation is placed in folder /usr/share/qb64




Go To the folder /usr/share/qb64/intternal/c and find these files:
makedat_lnx64.txt
makeline_lnx.txt
makeline_lnx_nogui.txt

Modify these files as it is marked on these screenshots:




To check compilation I have used these files:

3dballs.bas
acalc.bas
https://qb64.com/samples.html

Stopwatch - from Inform Samples
https://github.com/FellippeHeitor/InForm-demos/tree/master/Stopwatch

Download and place .bas files in Termux folder "/home"


Check compilation of the sample files according to screenshot.


Compiled files are placed in folder /usr/share/qb64 for *.bas files and in stopwatch folder for Inform sample

Open Termux-11 standalone application on the smartphone. Resume but do not exit from Termux.


Go to Preferences-Output of Termux-x11 and set Display Scale to 200%.


Go back to Termux folder /usr/share/qb64

Create the bash script to run GUI program.


Run bash script and go to Termux-x11 app to see result for each sample. 

<img width="1080" height="2340" alt="InForm_OnX11" src="https://github.com/user-attachments/assets/96cc3d08-504a-40d9-b03e-f23c029bba27" />
<img width="1080" height="2340" alt="acalc_OnX11" src="https://github.com/user-attachments/assets/04522c22-c40d-48ee-8352-be750886b57c" />
<img width="1080" height="2340" alt="3dBalls_OnX11" src="https://github.com/user-attachments/assets/c22978bf-a12e-4732-935c-0360ba24c61b" />





Inform sample is displayed in Termux-11 partly, because I failed to get library from "falcon.h". 
Compiler said that it is impossible for header file.
However, this sample proves that Inform app could be displayed too.
