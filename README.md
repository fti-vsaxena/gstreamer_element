# Gstreamer :

- GStreamer is open source, cross platform, pipeline based framework for multimedia. Gstreamer is used in Media players, Video/Audio editors, Web browsers, Streaming servers, etc. They rely heavily on threads to process the data.
- GStreamer helps build pipeline workflows in which it reads a file in one format, process them (resize, rescale, add filters) and then export it into another format.

## Installation (Ubuntu):

Follow this [blog](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) to install all the dependencies (such as codec files and other libraries) and build OpenCV with GStreamer.


## Basic Terms : 

### GstElement : 
- GstElement object is the basic building block for media pipeline. All the elements such as decoder, encoder, demux which we see as a black box, have been derived from GstElement.
- Elements (such as sink, source or filter) have properties which are used to modify their behaviour. They also have signals which help them execute a function call on the element.
- Properties of gstreamer elements can be viewed by using gst-inspect-1.0

**Source** — Source elements are those which can only generate data. Such as video file or an IP camera.

**Sink** — Sink elements are end points in a pipeline. For example, Output video playback, soundcard playback, screen, disk writing are sink elements.

**Filters** - They have both input and output. They recieve data as well as send the data after some kind of processing.Examples of such examples are converters, demuxers and decoders.

### Pipeline :

- In simple terms, we take in several components of GStreamer, such as input video source, video decoder and output source, put them together one after the other.
- Each element is seperated by ‘!’ and has spaces before and after ‘!’.
