## Approximation ##

DyadWaves uses a very simple approximation algorithm. User can select the wavelet name from the DWT Dashboard, percent of non-zero coefficients and the wavelet mode(Either dwtper or dwtsym) from the Approximation Dropdown menu. Based on the percentage selected, the algorithm calculates the threshold and zeroes all coefficients that have values below that threshold. Inverse DWT is then computed to reconstruct the signal from the non-zero coefficients.dwt\_per has fewer coefficients so it gives better results in most cases.

![https://lh5.googleusercontent.com/-NEsIlpY4G18/TiKNvLVyVtI/AAAAAAAAAIY/WKiAwro_ds4/s800/appx1d.png](https://lh5.googleusercontent.com/-NEsIlpY4G18/TiKNvLVyVtI/AAAAAAAAAIY/WKiAwro_ds4/s800/appx1d.png)
_Example:: 1D Approximation of a 2048 sample piecewise regular signal using db4 wavelet and DWT with periodic extension_

![https://lh4.googleusercontent.com/-QHlZhwBozhk/TiKN4ptfvcI/AAAAAAAAAIc/Ff1VrqSufHQ/s800/appx2d.png](https://lh4.googleusercontent.com/-QHlZhwBozhk/TiKN4ptfvcI/AAAAAAAAAIc/Ff1VrqSufHQ/s800/appx2d.png)
_Example:: 2D Approximation of Lena 512X512 grayscale image using db4 wavelet and DWT with periodic extension_