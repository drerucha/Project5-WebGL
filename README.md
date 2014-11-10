CIS 565 project 05 : WebGL globe
===================

![alt tag](https://raw.githubusercontent.com/drerucha/Project5-WebGL/master/readme_assets/globe.PNG)

## INTRODUCTION

This project is an exploration of GLSL and WebGL.

In the first part, I have implemented two dynamic wave animations that simulate a grid of vertices and run entirely on the GPU.

In the second part, I have implemented a GLSL fragment shader to render an interactive globe in WebGL. My globe includes the following features: texture blending, bump mapping, specular masking, an animated cloud layer, and animated waves.

## SIMPLE WAVES

My first wave animation was created by implementing a time-varying sin-based noise function in the vertex shader.

![alt tag](https://raw.githubusercontent.com/drerucha/Project5-WebGL/master/readme_assets/sin_wave.PNG)

My second wave animation approximates a ripple effect as if a stone were dropped in a pool of water, and was created by varying the height of vertices as a function of distance from the grid center in the vertex shader.

![alt tag](https://raw.githubusercontent.com/drerucha/Project5-WebGL/master/readme_assets/ripple_wave.PNG)

## NIGHT LIGHTS

This project began with a texture mapped sphere.

[texture mapped sphere image]

The back side of this sphere (the side not facing the light), was initially being rendered completely black. My first step was to detect which fragments were facing away from the light, and color those fragments using a separate texture that depicted the globe at night.

The diffuse lighting component was used to determine which fragments were on the dark side of the globe. If the dot product between the normal at a fragment and the light direction from that fragment were less than or equal to 0, then that fragment could not see the light source and should have the night texture instead of the daylight texture applied. Also, to prevent an abrupt change between the light and dark sides of the globe, the two textures representing day and night were linearly interpolated to provide a more realistic transition.

[back sphere without night texture image]

[back sphere with night texture image]

## SPECULAR MAP

*Coming soon.*

## CLOUDS

*Coming soon.*

## BUMP MAPPING

*Coming soon.*

## RIM LIGHTING

*Coming soon.*

## ANIMATED WAVES

*Coming soon.*