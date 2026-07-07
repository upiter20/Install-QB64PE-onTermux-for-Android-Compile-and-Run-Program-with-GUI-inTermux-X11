# Install-QB64PE-onTermux-for-Android-Compile-and-Run-Program-with-GUI-inTermux-X11
This is manual on how to Install QB64PE on Termux for Android, Compile and Run Program with GUI in Termux-X11

For AARCH64!!!

Install Termux for Android from F-Droid, not from Google Play.
https://f-droid.org/packages/com.termux/

Install Termux-X11 app for graphical output.
https://github.com/termux/termux-x11?ysclid=mqaw153gk8257962657




Open Termux terminal and install root-repo and X11-repo.
<img width="1080" height="2340" alt="Install_X11repo" src="https://github.com/user-attachments/assets/eadfe19f-f4bd-4c63-8ba0-35b0f02baf5a" />
<img width="1080" height="2340" alt="Install_RootRepo" src="https://github.com/user-attachments/assets/a2790d19-4284-426e-92ee-1fe5ff8264f1" />


Use command "pkg install" to get these packages:
build-essential
alsa-lib/stable
glu/x11
libcurl-static/stable
libpng-static
mesa-dev
termux-x11-nightly



Install Midnight Commander 
pkg install mc


Copy QB64PE for Linux into Termux folder '/home'
<img width="1080" height="2340" alt="qb64pe in termux home" src="https://github.com/user-attachments/assets/1f5baae0-cae0-4511-b9ac-5ddc9b10e892" />



Type command "mc" in Termux and after Midnight Commander is opened 
go to the folder /qb64pe and find "Makefile":



Modify "Makefile" as it is marked on these screenshots:
<img width="1080" height="2340" alt="replace C++ standart" src="https://github.com/user-attachments/assets/86ca22b0-c723-49a9-866b-71571ac881bd" />
<img width="1080" height="2340" alt="PIE and 64Bits" src="https://github.com/user-attachments/assets/f0c6ed13-c4a3-4ab7-975e-c7812314c069" />
<img width="1080" height="2340" alt="ELF architect" src="https://github.com/user-attachments/assets/462012c1-9bdf-48d2-bf72-ac85410e2aae" />


Go to folder /qb64pe/internal/c/parts/video/font/freetype and find these files:
inffast.h
inftrees.h

Modify this file as it is marked on these screenshots:
<img width="1080" height="2340" alt="inffast correct" src="https://github.com/user-attachments/assets/5817c4bc-b2fb-4f92-a0c3-f64340d5f8ef" />
<img width="1080" height="2340" alt="inftrees correct" src="https://github.com/user-attachments/assets/cb863034-104e-48cc-b6e6-2a6dc129ab31" />

Go to folder /qb64pe and type command "chmod +xr setup_lnx.sh"
to make setup_lnx.sh executable


<img width="1080" height="2340" alt="chmod setup_lnx" src="https://github.com/user-attachments/assets/71549dc8-7842-4b39-9bc4-46bd7f5becb5" />


Run setup_lnx.sh.

The new executable file "qb64pe" wil be created as it is shown on screenshot.
<img width="1080" height="2340" alt="compile done" src="https://github.com/user-attachments/assets/c5be9196-4572-4840-937d-7cef6c2bc745" />



To check compilation I have used these files:

3dballs.bas
acalc.bas
https://qb64.com/samples.html



Download and place .bas files in Termux folder "/home/qb64pe"






Check compilation of the sample files according to screenshots.
<img width="1080" height="2340" alt="3dballscompile" src="https://github.com/user-attachments/assets/e4caf4dc-6944-4962-8bdb-464abfd32dbc" />
<img width="1080" height="2340" alt="acalcCompile" src="https://github.com/user-attachments/assets/947ee7b5-36cc-4c73-a4bd-fe8b49eef6b8" />



Compiled files are placed in folder /home/qb64pe for *.bas files 

Resume but do not exit from Termux.

Open Termux-11 standalone application on the smartphone. 
<img width="1080" height="2340" alt="OpenX11_Prefs" src="https://github.com/user-attachments/assets/ed0a8719-d0d7-4e34-8ba9-6bf73dd4fdbe" />



Go to Preferences-Output of Termux-x11 and set Display Scale to 200%.
<img width="1080" height="2340" alt="SetScalling" src="https://github.com/user-attachments/assets/c5a42552-1131-40f7-ab6a-7026ed120c6a" />

Go back to Termux folder /home/qb64pe

Create the bash script to run program with GUI.
<img width="1080" height="2340" alt="1783347012936" src="https://github.com/user-attachments/assets/aa88dd14-ba8f-41ec-a885-b23194b5fded" />



Run bash script and see the error about Missing GL version. 

This error is somewere inside source code of qb64pe, 
so just press Enter to proceed.
<img width="1080" height="2340" alt="1783347012870" src="https://github.com/user-attachments/assets/bc596dcc-9ac4-4f7a-a82e-b75aec12d95d" />



Go to Termux-x11 app to see result for each sample. 


<img width="1080" height="2340" alt="acalc_OnX11" src="https://github.com/user-attachments/assets/04522c22-c40d-48ee-8352-be750886b57c" />
<img width="1080" height="2340" alt="3dBalls_OnX11" src="https://github.com/user-attachments/assets/c22978bf-a12e-4732-935c-0360ba24c61b" />



As to Inform project, I have tried to compile this sample - Stopwatch
https://github.com/FellippeHeitor/InForm-demos/tree/master/Stopwatch

I placed Stopwatch .bas file and folder "Inform" into the folder "/home/qb64pe" as it is shown on screenshot
<img width="1080" height="2340" alt="StopWatchInform" src="https://github.com/user-attachments/assets/961b5679-5633-4291-86f6-79cee10c4614" />

But compilation failed because there is no implementation for function "MessageBox".

More information on screenshots.
<img width="1080" height="2340" alt="StopwatchCompile" src="https://github.com/user-attachments/assets/90337aef-f61b-405d-8b70-17b7dee9e5bd" />

<img width="1080" height="2340" alt="NoMessageBox" src="https://github.com/user-attachments/assets/18703afb-3439-4638-97b9-2befee72579d" />

