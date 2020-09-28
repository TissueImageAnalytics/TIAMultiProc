<p align="center">
  <img width="450" height="200" src="https://warwick.ac.uk/fac/sci/dcs/research/tia/tiatoolbox/files/tialab_logo.png">
</p>
<h1 align="center">TIA MultiProc</h1>

Multiprocessing class decorator to upgrade a single core & single file function to 
multi-core multi-file function. Specifically, designed for the [tiatoolbox](https://github.com/TIA-Lab/tiatoolbox)

Please try

    >>> from tiamultiproc.multiproc import TIAMultiProcess
    >>> import cv2
    >>> @TIAMultiProcess(iter_on="input_path")
    ... def read_images(input_path, output_dir=None):
    ...    img = cv2.imread(input_path)
    ...    return img
    >>> imgs = read_images(input_path, workers=2)

imgs will be a list of numpy arrays containing the input images.

License
=======

The source code TIAMultiProc as hosted on GitHub is released under the [GNU General Public License (Version 3)].

The full text of the licence is included in [LICENSE.md](LICENSE.md).

[GNU General Public License (Version 3)]: https://www.gnu.org/licenses/gpl-3.0.html
