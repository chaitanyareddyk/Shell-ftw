# Shell-ftw

#### Command to match and delete duplicate files
`find . -name '*(*).pdf' #-delete`

#### Upload/Download (Copy) a dir to/from s3 
```
sudo apt  install awscli
pip3 install s3transfer
aws configure
aws s3 cp SOURCE_DIR s3://DEST_BUCKET/BUCKET_DIR/ --recursive #upload
aws s3 cp s3://DEST_BUCKET/BUCKET_DIR/ SOURCE_DIR --recursive #download
```

#### Install Google Chrome
```
sudo wget https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo apt-get -y update
sudo apt-get install -y google-chrome-stable unzip
```

#### Install chromedriver
```
sudo wget -O /tmp/chromedriver.zip http://chromedriver.storage.googleapis.com/`curl -sS chromedriver.storage.googleapis.com/LATEST_RELEASE`/chromedriver_linux64.zip
sudo unzip /tmp/chromedriver.zip chromedriver -d /usr/local/bin/
```

#### Install selenium python library
```
sudo apt-get -y install python3-pip
pip3 install selenium==3.141.0
```

#### Install and Setup VNC
```
sudo apt update
sudo apt -y install xfce4 xfce4-goodies
sudo apt -y install vnc4server
vncserver
vncserver -kill :1
mv ~/.vnc/xstartup ~/.vnc/xstartup.bak
echo "#!/bin/bash
xrdb $HOME/.Xresources
startxfce4 &" >> ~/.vnc/xstartup
sudo chmod +x ~/.vnc/xstartup
vncserver
```

#### Count no.of files in current dir
`ls -1 | wc -l`

#### Using tmux
```
tmux
Ctrl+B then d
tmux ls
tmux attach-session -t sess_no
```

#### Install tesseract and imagemagick
sudo apt install -y tesseract-ocr
sudo apt install -y imagemagick
sudo mv /etc/ImageMagick-6/policy.xml /etc/ImageMagick-6/policy.xmlout
