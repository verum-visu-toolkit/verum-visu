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

<!--
verum-visu.git
    submodule: analyzer.git; package: vvanalyzer
    submodule: renderer.git; package: vvrenderer
    submodule: sptfile.git; package: vvsptfile
    submodule: frsfile.git; package: vvfrsfile
    submodule: rndfile.git; package: vvrndfile

TODO: publish:
vvanalyzer, vvrenderer, vvsptfile, vvfmsfile, vvrndfile
(the tools and Visualizer parts should reference the appropriate file formats
directly)
TODO: create, vvfmsfile, vvrndfile, and vvrenderer!
use MoviePy!
http://zulko.github.io/blog/2014/11/29/data-animations-with-python-and-moviepy/

use one make_frame function that generates image (numpy array)
for the image, draw the shapes using skimage? find how to use arrays and color
http://scikit-image.org/docs/dev/api/skimage.draw.html

OR: if it's not slower, draw svg shapes and rasterize each frame

set fps in export from MoviePy to be the speed of the analyzer

[{'type':'circle', 'args': ['var1', 'var2', 5], 'color': 'var3'}]

def render(config=None):

    video_width = config['width']
    video_height = config['height']
    def make_frame(t):
        img = np.zeros((video_width, video_height), dtype=np.uint8)

        for shape in shapes:
            args = [calc_shape_prop(arg, t) for arg in shape['args']]
            xx, yy = skimage.draw[shape['type']](args)
            img[xx, yy] = calc_shape_prop(shape['color'], t)

        return img

# frames: e.g. [[{ 'var1': 3.23, 'var2': '23423.33', 'var3': 323 }], ...]
def calc_shape_prop(prop_name, t):
    # if prop_name isn't a string, return it - it's constant
    # else, return frames[t][prop_name]


TODO: create a demo Transformer (not template yet) in python
(as separate repos)
the transformer should use the new vvanalyzer.read_output_file


in /verum-visu repo, also write more about the ideas of the project -
the repo will pretty much be the project home page (in the OSS community)
-->