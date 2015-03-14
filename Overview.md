# DyadWaves #

> DyadWaves is an easy to use GUI for 1D and 2D Wavelet Transform. This software is pretty basic with functionality consisting of Wavelet Transform computation, signal/image approximation and denoising using up to three transform modes. It uses separate executables for 1D and 2D processing that are appropriately labeled. They should appear in your windows start menu and , if you so choose, your windows desktop. This software is build using c++ and Nokia's QT4(http://qt.nokia.com/). 1D Dyadwaves graphs are build using QWT library courtesy of Qwt project (http://qwt.sf.net).  FFT computations are done using FFTW3 library(http://www.fftw.org/).

| [Overview](http://code.google.com/p/dyadwaves/wiki/Overview#Overview) | Modes, Wavelets, Input/Output,Display |
|:----------------------------------------------------------------------|:--------------------------------------|
| [Wavelet Transform](http://code.google.com/p/dyadwaves/wiki/dwt) | DWT/SWT Computation in 1D and 2D |
| [Approximation](http://code.google.com/p/dyadwaves/wiki/appx) | Signal and Image Approximation |
| [DeNoising](http://code.google.com/p/dyadwaves/wiki/denoise) | Signal and Image Denoising |
| [Issues and Contact](http://code.google.com/p/dyadwaves/wiki/issues) | Information on Latest Version |

## Overview ##

### Transform Modes ###

> There are three available modes

#1 **dwt\_sym** - Decimated Discrete Wavelet Transform using symmetric extension.

#2 **dwt\_per** - Decimated Discrete Wavelet Transform using periodic extension.

#3 **swt** - Stationary (Undecimated) Wavelet Transform. It also uses peiodic extension.

### Wavelet Families ###

> Four wavelet families are available.

1. **Daubechies**- 15 orthogonal wavelets are available, ranging from 2-tap filters to 30-tap filters.

2. **Biorthogonal** - Symmetric filter non-orthogonal wavelets. bior1.1 to bior6.8

3. **Coiflets** - 5 wavelets. coif1 - coif5.

4. **Symmlets** - 10 wavelets from sym1 to sym10.

> Wavelets, associated filters and filter frequency response can be plotted by selecting the wavelet from the "Choose Wavelet Family" dropdown box in the DWT Dashboard and then using appropriate pushbuttons in the Display Dashboard as shown below.

![https://lh5.googleusercontent.com/-QngH_5PbP14/TiFV9O3zBWI/AAAAAAAAAHM/-KgdTE1cdDs/s800/wavedisp.png](https://lh5.googleusercontent.com/-QngH_5PbP14/TiFV9O3zBWI/AAAAAAAAAHM/-KgdTE1cdDs/s800/wavedisp.png)

### Input/Output ###

**1D ::** 1D I/O  is very, very basic at this point. It accepts text files arranged in either one row or one column([Example](http://wavelet1d.googlecode.com/svn/trunk/src/signal.txt)). You can save outputs (coefficients and processed signal) in the same 1D text format or you can save graphs as image/pdf/svg files.

**2D ::** Input is in the form of images ( tif,tiff,jpeg,bmp,png). Output images can be saved in these same five formats. I expect to add more formats in upcoming versions.

### Display:: 1D Interface ###

> _1D_ Interface displays input and output graphs. These graphs can be zoomed in and zoomed out. IDWT graphs have additional options of saving and viewing each graph separately as the display view can get very busy if decomposition levels are large specially if screen resolution isn't very high.

![https://lh3.googleusercontent.com/-ClyWKAE84Wk/TiFm_xseQwI/AAAAAAAAAHc/eh8zfhgE97o/s800/disp1d-1.png](https://lh3.googleusercontent.com/-ClyWKAE84Wk/TiFm_xseQwI/AAAAAAAAAHc/eh8zfhgE97o/s800/disp1d-1.png)

_Example:: Individual graphs can be viewed separately by clicking on "VIEW #" buttons_

> ![https://lh6.googleusercontent.com/-8Xl05nSG2q4/TiFoQtqiFZI/AAAAAAAAAHg/JmH60fGi6WA/s800/disp1d-2.png](https://lh6.googleusercontent.com/-8Xl05nSG2q4/TiFoQtqiFZI/AAAAAAAAAHg/JmH60fGi6WA/s800/disp1d-2.png)

_Example:: Graphs can also be viewed and saved in printer-friendly format(blue on white)_

Please also note that "save as PDF/SVG" format will also save outputs in the five image format and uses rendering of the graph which in most cases result in better results. "Save as Image" is the quick and dirty format and will capture the pixmap as is so the results may not be up to par on many occasions.


### Display:: 2D Interface ###

> _2D_ interface display is similar to the 1D case minus any zoom functionality. However, if the images are large they may not fit in the application window or they may not appear proportionally to their dimensions. In such a case, you have the option of viewing full size image. There is also an option of viewing all DWT coefficients. These are liberally zeropadded in order to have a rectangular image.

![https://lh3.googleusercontent.com/-LDcbRToB-Gs/TiFrl-2uUaI/AAAAAAAAAHk/RsAbha0WE-U/s912/disp2d-1.png](https://lh3.googleusercontent.com/-LDcbRToB-Gs/TiFrl-2uUaI/AAAAAAAAAHk/RsAbha0WE-U/s912/disp2d-1.png)

_Example:: 2D 2 level DWT View of Lena image._

![https://lh6.googleusercontent.com/-S_vpCzN-fyU/TiFtU3DxNEI/AAAAAAAAAHo/wAAZNWo4lng/s912/disp2d-2.png](https://lh6.googleusercontent.com/-S_vpCzN-fyU/TiFtU3DxNEI/AAAAAAAAAHo/wAAZNWo4lng/s912/disp2d-2.png)

_Example:: Viewing Full size DWT Decomposition_