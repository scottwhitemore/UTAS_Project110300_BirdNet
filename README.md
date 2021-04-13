## birdnet
Deployment of bird call recogniser(s) developed for Project 110300: *Machine learning algorithms to classify bird calls from acoustic data*

## About the recogniser

## Running the Recogniser

### Linux and Macintosh, using Docker
For Linux and Macintosh (MACOS) operating systems we have created a *docker image* which can be run safely in a terminal window as follows:

If you have Docker installed (you may need to consult your IT department for this), start up a Terminal window and type these commands, to use the North-West Tasmanian recogniser:

```bash
docker pull scottwhitemore/birdnet:NWTAS_b3
docker run --mount type=bind,src=/full/path/to/wav/files/,dst=/data scottwhitemore/birdnet:NWTAS_b3
```

By way of explanation, 
[comment:] <> * `sudo` is to enable the super-user privileges you need to run Docker (don't worry, it's safe!).  You *may* have to use sudo
 * `docker pull` tells the docker program to download the image
   - `--mount type=bind,` indicates that you want to mount the source folder `src` in virtual storage, giving us a way to see the data and also save the predictons to local storage (your hard drive).
   - `src=/full/path/to/wav/files/` is the full path to the folder containing your audio files in WAV format.
   - 

### Windows
If you have Docker installed, you can use the same instructions as above; otherwise, scripts in Python are available.

## Notes
*  If your WAV files are sampled at 22.05kHz you will probably find it faster since the program will probably otherwise have to *down-sample* to that frequency, for example if they are sampled at 44.1kHz.
