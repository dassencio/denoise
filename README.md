![Functional tests](https://github.com/dassencio/denoise/workflows/Functional%20tests/badge.svg)
![Static code analysis](https://github.com/dassencio/denoise/workflows/Static%20code%20analysis/badge.svg)

# Description

`denoise` is a script (written in Python 3) which denoises data without using
fitting functions. It implements the algorithm described
[here](http://diego.assencio.com/?index=df0bdbd936cfac191141770bf91a6b6e).

# License

All code from this project is licensed under the GPLv3. See the
[`LICENSE`](https://github.com/dassencio/denoise/tree/master/LICENSE)
file for more information.

# Required modules

The following modules are used:

- `numpy`
- `matplotlib`

You can install them with the following command:

    pip3 install numpy matplotlib

# Usage instructions

As an example, running

    ./denoise -i noisy_data.txt -o denoised_data.txt -u 20.0

will take the data sequence on `noisy_data.txt` (one value per line), denoise it
and write the denoised sequence on `denoised_data.txt`. Above, `-u 20.0` specifies
the denoising coefficient &mu;: &mu; = 0.0 means no denoising at all, while larger
values of &mu; enforce more denoising and therefore generate smoother output
sequences.

You can view a plot of both the original and denoised sequences by adding `-p`
to the command above.

For testing purposes, sample data with noise is provided on the `noisy_data`
subdirectory. Try running:

    ./denoise -i noisy_data/sine.txt -p -u 10.0

and set the denoising coefficient to different values to get a feeling for
how the denoising algorithm works.

# Contributors & contact information

Diego Assencio / diego@assencio.com
