# DepthKit for A-Frame
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

An A-Frame component for rendering [DepthKit](http://www.depthkit.tv) volumetric videos in WebVR. The A-Frame component wraps [DepthKit.js](https://github.com/juniorxsound/DepthKit.js) which is a small library that provides the same functionality for [Three.js](https://github.com/mrdoob/three.js) projects.
- [Usage](#usage)
- [Contribute](#contribute)

![DepthKit AFrame](https://raw.githubusercontent.com/juniorxsound/DepthKit-A-Frame/master/docs/movement.gif?token=APLD_It_uvXAHdio-sYe_JUHWQEXUHslks5aZRfAwA%3D%3D)

## Usage
Start by cloning/forking the repository and including ```aframe.depthkit.min.js``` from the ```./dist``` folder (make sure to clone using ```--recursive``` flag if you plan to run the examples to clone the git submodules too)

The simplest way you can initialize a DepthKit video is to create a ```depthkit``` entity inside an A-Frame ```a-scene``` tag:
```html
<a-scene>
      <a-entity depthkit="type: wire;
                          metaPath: ../ext/DepthKit/assets/Chae/Chae_Demo_Upres.txt;
                          videoPath: ../ext/DepthKit/assets/Chae/Chae_Demo_Upres.webm;
                          autoplay: true;
                          loop: true;">
      </a-entity>
</a-scene>
```
Where the ```type``` attribute support ```wire/points/mesh``` for rendering different styles, ```metaPath``` is the path to the ```.txt``` file with the parameters (exported by DepthKit Visualize) and ```videoPath``` is for the path to the video file.

## Contribute
PRs are welcome ✊🏻 make sure to clone using the ```git clone --recursive```.

### Build system
- ```npm run start``` uses ```concurrently``` to start both an ```http-server``` and a ```watchify``` build opreation on every save to ```./dist/aframe.depthkit.js```
- ```npm run build``` builds and minifies to ```./dist/aframe.depthkit.min.js```
