# avs2yuv

**This is a fork from https://github.com/DJATOM/avs2yuv used for for experimental purpose.**

A simple tool that can execute avisynth scripts.
This version is intended to be used with Avisynth+.

Supported platforms: Linux (Debian, Ubuntu), Windows 10+

## Usage

```sh
Avs2YUV 0.30
Writen by Loren Merritt, modified by BugMaster, Chikuzen
and currently maintained by DJATOM.
Modified by Arnaud de Gérard

Usage: avs2yuv [options] in.avs [-o out.y4m] [-o out2.y4m]
-nstdr	do not print info to stderr
-seek	seek to the given frame number
-frames	stop after processing this many frames
-slave	init script and do nothing
	(useful for piping from TCPDeliver to AvsNetPipe)
-raw	output raw data
-reverse_scanline	reverse scanline when piping rawdata
	(useful for piping rawdata to FFmpeg)
-depth	specify input bit depth
	(default 8, trying to guess from the script)
-fps	overwrite input framerate
-par	specify pixel aspect ratio
The outfile may be "-", meaning stdout.
The following output format are available:
	* yuv4mpeg, as used by MPlayer, FFmpeg, Libav, x264, mjpegtools. (default)
	* raw data.
```

## Compiling and installing
```bash
git clone https://github.com/adegerard/avs2yuv.git
mkdir -p avs2yuv/build && \
cd avs2yuv/build && \
cmake ../ && \
make && \
sudo make install
```
