# DepthKit for A-Frame
An A-Frame component for rendering DepthKit volumetric videos in WebVR. The A-Frame component wraps [DepthKit.js](https://github.com/juniorxsound/DepthKit.js) which is a small library that provides the same functionality for [Three.js](https://github.com/mrdoob/three.js) projects.
- [Usage](#usage)
- [Contribute](#contribute)
- [Example](https://juniorxsound.github.io/DepthKit-A-Frame/)

![DepthKit AFrame](https://github.com/juniorxsound/DepthKit-A-Frame/blob/master/docs/screenshot.png)

## Usage
Start by cloning/forking the library and including ```aframe.depthkit.min.js``` from the ```./dist``` folder (make sure to clone using ```--recursive``` flag if you plan to run the examples to clone the git submodules too)

The simplest way you can initialize a DepthKit video is to create a ```depthkit``` entity inside an A-Frame ```a-scene``` tag:
```html
<a-scene>
      <a-entity depthkit="type: wire;
                          metaPath: ../ext/DepthKit/assets/Chae/Chae_Demo_Upres.txt;
                          videoPath: ../ext/DepthKit/assets/Chae/Chae_Demo_Upres.webm;">
      </a-entity>
</a-scene>
```
Where the ```type``` attribute support ```wire/points/mesh``` for rendering different styles, ```metaPath``` is the path to the ```.txt``` file with the parameters (exported by DepthKit Visualize) and ```videoPath``` is for the path to the video file.

### Advanced usage

## Contribute
PR's are welcome ✊🏻 as I am not extremely familiar with the A-Frame ecosystem if you want to help make sure to clone using the ```git clone --recursive```.

### Build system

