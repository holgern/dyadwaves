## Wavelet Transform ##

> There are three wavelet transform modes - dwt\_sym, swt and dwt\_per. All of them have same display system and the DWT output can be saved as text file using the "Save DWT Output" button in the 1D mode and as image in 2D mode.

### 1D::Decimated DWT (Symmetric Extension) ###

> Of all the modes , this one is the best equipped to deal with signal boundary issues. Signal is symmetrically extended at every stage so there are no sharp jumps and discontinuities. On the negative side, there is some redundancy in the system as this isn't an N input N output system.

![https://lh4.googleusercontent.com/-PCJ9CWxHYN0/TiDyuvbZ7eI/AAAAAAAAAG4/P6K0fPb-8AE/s800/db1.png](https://lh4.googleusercontent.com/-PCJ9CWxHYN0/TiDyuvbZ7eI/AAAAAAAAAG4/P6K0fPb-8AE/s800/db1.png)
_Example:: 2 Level dwt\_sym decomposition using db1 wavelet_


### 1D::Stationary Wavelet Transform(Undecimated) ###

> For 1D case, an N input signal yields 2XN output coefficients at each stage. There is more redundancy but it is useful in cases where translation-invariance is needed. This software also uses SWT (alongside the other two modes) for denoising.

![https://lh3.googleusercontent.com/-U-xjVuBxFzk/TiIdkwlhi6I/AAAAAAAAAH4/O0-2DzK7ZIE/s800/swt.png](https://lh3.googleusercontent.com/-U-xjVuBxFzk/TiIdkwlhi6I/AAAAAAAAAH4/O0-2DzK7ZIE/s800/swt.png)
_Example:: 2 Level SWT Decomposition of a 5400 sample signal_


### 1D::Decimated DWT (Periodic Extension) ###

dwt\_per mode is a N input and ~N output system and ,thus, often is the fastest scheme of the three.Although, periodic extension may sometimes result in subpar performance at the signal boundaries. Regardless, having least redundancy makes it suitable for some approximation applications.

![https://lh6.googleusercontent.com/-VKnKRO_8UFE/TiIeu__ks3I/AAAAAAAAAH8/H99ab3jhxxE/s800/dwt_per.png](https://lh6.googleusercontent.com/-VKnKRO_8UFE/TiIeu__ks3I/AAAAAAAAAH8/H99ab3jhxxE/s800/dwt_per.png)
_Example:: 3 Level Decomposition of a piecewise regular signal using dwt with periodic extension_


### 2D::Decimated DWT (Symmetric Extension) ###

2D DWT is similar to 1D in terms of options with one exception - you have an option of faster processing a color image by treating it as a grayscale image. This is due to speed issues in this implementation. Smaller Images ( < 512 X 512) shouldn't be too much of a nuisance on most systems.

![https://lh4.googleusercontent.com/-vCE6J6Fzwy4/TiImnLVRyII/AAAAAAAAAIA/_YoH_byEP9I/s800/sym2d.png](https://lh4.googleusercontent.com/-vCE6J6Fzwy4/TiImnLVRyII/AAAAAAAAAIA/_YoH_byEP9I/s800/sym2d.png)
_Example:: 2 level Decomposition of a 512-by-512 color image using dwt sym_

### 2D::Stationary Wavelet Transform (UnDecimated) ###

Same goes for Stationary Wavelet Transform with the additional caution that speed is an even bigger of an issue for high number of decomposition levels( > 2 actually if color image is large in size).

![https://lh4.googleusercontent.com/-nnAl_4iFtfI/TiD0r_WwmOI/AAAAAAAAAG8/ZwD5jAztMK0/s800/db1-2.png](https://lh4.googleusercontent.com/-nnAl_4iFtfI/TiD0r_WwmOI/AAAAAAAAAG8/ZwD5jAztMK0/s800/db1-2.png)
_Example:: 2 Level SWT Decomposition of a color image_

### 2D::Decimated DWT (Periodic Extension) ###




![https://lh3.googleusercontent.com/-Q0mOx66G6G8/TiIqHqai9rI/AAAAAAAAAII/GngqJBmFx0Q/s800/dwt2dper2.png](https://lh3.googleusercontent.com/-Q0mOx66G6G8/TiIqHqai9rI/AAAAAAAAAII/GngqJBmFx0Q/s800/dwt2dper2.png)
_Example:: 3 Level Decomposition of a 256-by256 image using dwt (periodic extension)_