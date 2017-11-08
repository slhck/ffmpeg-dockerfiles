# ffmpeg-docker

Docker test files for building FFmpeg under Ubuntu and CentOS.

Used for verifying the [compilation guides](https://trac.ffmpeg.org/wiki/CompilationGuide/) in the FFmpeg Wiki.

This image can't do much; have a look at [`jrottenberg/ffmpeg`](https://github.com/jrottenberg/ffmpeg) for a well-maintained ffmpeg Docker image featuring more libraries.

## Usage

Building:

    docker build -t ffmpeg-ubuntu -f Dockerfile-ubuntu .
    docker build -t ffmpeg-centos -f Dockerfile-centos .

Running:

    docker run -i --rm -t ffmpeg-ubuntu
    docker run -i --rm -t ffmpeg-centos

This calls `ffmpeg` with the default help option. Use volumes to mount input files and pipes to generate output:

## License

Copyright 2017 Werner Robitza

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.