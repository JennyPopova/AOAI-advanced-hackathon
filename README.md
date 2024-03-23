# AOAI-advanced-hackathon
 
### Install audio processing in terminal:
sudo add-apt-repository ppa:mc3man/trusty-media  
sudo apt-get update  
sudo apt-get install ffmpeg 

### Install Libraries:
* On Ubuntu 16.04 or 18.04, run the following commands for the installation of required packages:
  ```sh
  sudo apt-get update
  sudo apt-get install libssl-dev libasound2
  ```
* On Debian 9, run the following commands for the installation of required packages:
  ```sh
  sudo apt install libgstreamer1.0-0 \
  gstreamer1.0-plugins-base \
  gstreamer1.0-plugins-good \
  gstreamer1.0-plugins-bad \
  gstreamer1.0-plugins-ugly
  

### Python environment: 
pip install -r Labs/requirements.txt

### Fill .env file with provided keys