# verum visu toolkit

**verum visu** (Latin for *true to see*) is a project applying modular design
to the process of audio visualization, allowing for fully customizable, rich
visualizations that can utilize multiple languages or applications.

The **verum visu Toolkit** defines audio visualization as a process using three pieces of software:

1. *Spectral Analyzer*\
    analyzes audio for frequency data

2. **Visualizer**

3. *Video Renderer*\
    creates a video file by the frames

The *Spectral Analyzer* and *Video Renderer* are the tools in the
toolkit. The Visualizer is a step created by *you* or someone else in the
**verum visu community**, and that is what actually defines the relationship between
the audio and the visuals. The Visualizer could be written in any language&mdash;it
just needs to be able to read and write JSON files.

<!-- for now (8.26.17), if it's written in Python, you can use vv's file format libs -->

This toolkit exists so that you can experiment with audio visualization without
paying any attention to the technical aspects of spectral analysis and pixel rendering.
It allows you to streamline the process of visualization since you only need to create a
Visualizer, which defines everything about your visualization.

### Visualizer
The Visualizer is actually two applications:

1. **Interpreter**\
    creates visualization data from the frequency data as input (using algorithms
    /neural networks)

2. **Director**\
    configures how visualization data should be mapped to properties of shapes for the
    renderer to animate


> (8.26.17) Everything is at an extremely early stage!