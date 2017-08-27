# verum visu toolkit

The **verum visu Audio Visualization Toolkit** is a response to the idea
that an open-source community can develop rich audio visualizations if
the software is split up into a clearly defined, accessible process.

The toolkit consists of three parts:

1. *Spectral Analyzer*
    analyzes audio for frequency data

2. **Visualizer**

3. *Video Renderer*\
    creates a video file by the frames

The *Spectral Analyzer* and *Video Renderer* are the only tools in the
toolkit. The Visualizer will do the bulk of the work in any process.
The tools (along with the [libraries](todo)), allow for the development
of specialized Visualizer parts.

### Visualizer
The interpreter consists of two parts, and these are types of programs
created by the Verum Visu community.

1. **Interpreter**\
    algorithms/neural networks create visualization data from the
    frequency data as input

2. **Director**\
    maps the visualization data to properties of shapes for the renderer
    to animate

Everything is at an extremely early stage!