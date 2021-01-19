# VideoProcessingOctave

## `chromaR`
@detsutut has created the [chromaR](https://github.com/detsutut/chroma) toolkit containing a range of interesting functions for processing colour data derived from motion pictures in `R`. 

He has also provoided a Matlab script [VideoProcessing.m](https://github.com/detsutut/chroma/blob/master/videoProcessing.m) for users to generate their own dataset from a video file. This script extracts the average RGB value for each frame and stores the result as a `.csv` file. From the `chroma` repository:

> This means that you must have Matlab installed on your local machine. The script above inspects the video source frame by frame. Each frame is a Height×Width×3 tensor. Since we are mostly interested in exploring the color trend over the entire clip rather than focusing on the palette of a single frame at this point, the only information we need to extract here is the average color (i.e RGB triplet) of each frame.

You can find the details of how to do this on the [detsutut/chroma](https://github.com/detsutut/chroma) repository.

## Octave instead of Matlab
Matlab is *not* a cheap piece of software and is possibly not accessible to many users due to the prohibitive cost.

Fortunately [Octave](https://www.gnu.org/software/octave/index) is an open source alternative to Matlab that will run `.m` files, such as that described on the `chroma` repository, with *very* minimal changes.

Therefore, I have adapted @detsutut's original `VideoProcessing.m` file to run in Ocatve and it is available on this repository as `VideoProcessingOctave.m`.

To run this file you will need to have the [video](https://wiki.octave.org/Video_package) package for Octave installed. Installation details are available on the `video` package website. 

Load the `video` package into the environment, at the Octave prompt enter `pkg load video`, before running `VideoProcessingOctave.m.`

The difference between `VideoProcessing.m` and `VideoProcessingOctave.m` is not even a single letter: in line 19 of the script, `mov.duration` must be changed to `mov.Duration`. For those of you still struggling to see the difference, the `video` package in Octave requires that *duration* has a **capital** letter unlike it's Matlab counterpart. 

Like I said, not even a single letter's difference.
