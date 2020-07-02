<!--
Version: 1.0

**Change Log**
20200622 - inital version
-->

Perlin2DSmoke
-------------------------------------
[Asset Store Link](http://u3d.as/1Wyn)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
- [Perlin2DSmoke](#perlin2dsmoke)
- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Terms of Use](#terms-of-use)
- [Overview/Setup](#overviewsetup)
- [ScreenShots](#screenshots)
- [Scripts](#scripts)
    - [Perlin2dSmoke.cs](#perlin2dsmokecs)
    - [updateMousePosition.cs](#updatemousepositioncs)
    - [Other Scripts](#other-scripts)
- [Shaders](#shaders)
    - [Perlin2dSmoke_Base.shadergraph](#perlin2dsmoke_baseshadergraph)
    - [Perlin2dSmoke_MouseRect.shadergraph](#perlin2dsmoke_mouserectshadergraph)
    - [RT2T.shadergraph](#rt2tshadergraph)
- [FAQ](#faq)
    - [Effect is Stretched ?](#effect-is-stretched-)
    - [testing and notes](#testing-and-notes)

<!--TOC-->


## Contact  

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Website: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  


## Description Features

Displays a smoke effect on one or more objects,  
with the ability to distort the smoke if needed.


* Customize using standard Shader Graphs
* Simultaneous distortions in the smoke using the mouse
    * this can be changed to any game object as well.
* Unity Free friendly.
* Fully commented C# and Shader Graph code.
* Awesome demos!



## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

## Overview/Setup 

your scences may need to be adjusted to apply this effect correctly.
1. first a camera will generate a cameraRenderTexture 
    * this should only see the objects you want to apply the smoke to (use Culling Mask)
2. the cameraRenderTexture will be passed to the Perlin2dSmoke.cs (which is on a game object)
3. Perlin2dSmoke.cs outputs a outputTexture, which then can be used in a UI Image or other game Objects.

here are two images to show

![Imgur](https://i.imgur.com/wKscPgTm.png)  

![Imgur](https://i.imgur.com/PKvvvhmm.png)

## ScreenShots

![Imgur](https://i.imgur.com/voIGwfBm.png) 

![Imgur](https://i.imgur.com/RpIwh9J.gif)

![Imgur](https://i.imgur.com/NeDm52W.gif)

![Imgur](https://i.imgur.com/5Xkk1Mz.gif)

![Imgur](https://i.imgur.com/9KQKMv3.gif)

## Scripts 

### Perlin2dSmoke.cs
Description:  
this script will take in a Render Texture (typically from a camera) and applied a material to it, and outputs a buffer (Render Texture) to later be used in a UI Image of other asset.

Material:  
this material will apply the effect to the texture  

cameraRenderTexture:  
this is the RenderTexture from the camera  

outputTexture:  
this is the outputTexture  

updateInterval:  
this is how often the effect will be applied to the outputTexture.  

### updateMousePosition.cs  
Description:  
used to update material with the mouse position.
-- make sure to use Perlin2dSmoke_MouseRect.shadergraph

Material:  
this material will apply the effect to the texture  

force:   
this is the maxium force that will be applied to the smoke

speed:
the speed to update the force  


### Other Scripts
The Other scripts are basically just used for the Demos.


## Shaders 

### Perlin2dSmoke_Base.shadergraph
used to apply the effect to a texture.

### Perlin2dSmoke_MouseRect.shadergraph
a new version of the Perlin2dSmoke_Base.shadergraph that has the ability to react to the mouse cursor.  

### RT2T.shadergraph
this takes the outputTexture from Perlin2dSmoke.cs and applies it to a UI Image or other game object.


## FAQ

### Effect is Stretched ?
you can solve this my resizing the RenderTextures to be the same size of the Screen.

### testing and notes
This works 100% in the editor,  
however had issues with the WebGL platform.