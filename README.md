Description
===========

An implementation in python of an algorithm for denoising data without using
fitting functions.


License
=======

All code from this project is licensed under the GPLv3. See 'LICENSE' for more.


Instructions
============

As an example, running

	./denoise -i noisy_data.txt -o denoised_data.txt -u 20.0

will take the data sequence on noisy_data.txt (one value per line), denoise it and
write the denoised sequence on denoised_data.txt. Above, '-u 20.0' sets the
denoising coefficient mu: mu = 0.0 means no denoising at all, while larger values
of mu enforce more denoising and therefore a smoother output sequence.

You can view a plot of both the original and denoised sequences by adding '-p'
to the command above.

For testing purposes, sample data with noise is provided on the directory
'noisy_data'. Try running:

	./denoise -i noisy_data/sine.txt -p -u 10.0

and set the denoising coefficient to different values to get a feeling for
how the denoising algorithm works.


Required Libraries
==================

The following python libraries are used:

    - numpy
    - matplotlib

On Ubuntu/Debian, you can install these libraries with:

	sudo apt-get install python3-numpy python3-matplotlib


Contributors & Contact Information
==================================

Diego Assencio / diego@assencio.com
