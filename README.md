## birdnet
Deployment of bird call recogniser(s) developed for Project 110300: *Machine learning algorithms to classify bird calls from acoustic data*

## About the recogniser

## Running the Recogniser

### Docker / Linux and Macintosh
For Linux and Macintosh (MACOS) operating systems we have created a *docker image* which can be run safely in a terminal window as follows:

If you have Docker installed (you may need to consult your IT department for this), start up a Terminal window and type these commands:

```bash
sudo docker pull scottwhitemore/birdnet:NWTAS_b3
docker run --mount type=bind,src=\$(pwd)/test_wavs,dst=/data scottwhitemore/birdnet:NWTAS_b3
```
By way of explanation, 
 * `sudo` is to enable the super-user privileges you need to run Docker (don't worry, it's safe!)
 * 

### Windows
If you have Docker, great you can use the same ; otherwise python scripts
