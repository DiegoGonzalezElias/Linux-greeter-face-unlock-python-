# Linux greeter face unlock (python)

Firstly, you must know this only works on boot, if you lock again the screen you have to put the password like you always do. 

#### Installation

You have to install the requirements. They are at the file above requirements.txt ( or you can copy paste from here ):
```sh
sudo apt install cmake
sudo pip install face_recognition
sudo pip install opencv-python
```

What I do is basically, modify and example code from [face_recognition's github page](https://github.com/ageitgey/face_recognition/blob/master/examples/facerec_from_webcam_faster.py) and use the /etc/rc.local file, which allow you to execute code after the system boot automatically to execute that code.

The script recognize your face and if it's you change the /etc/gdm3/custom.conf file for another modified with the name of your account then restart the gdm3 service that reset the shell, so after that you log in automatically and then change again the custom.conf file for the original one.

Now that you have the script you have to take a picture of yoursefl whith any webcam program, for exmaple cheese. Create a folder where you are going to keep the python script, your photo and a copy of /etc/gdm3/custom.conf. This file is where you indicate if you have an auto login account. you have to keep a copy of that file with some uncommented lines( remember that all the files are above ) and another copy of the original with out modify on a folder, that I called original.






