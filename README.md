# DME2: installation-error-fixed version


This is a fixed version DME2(The Discriminating Matrix Enumerator) algorithm for *de novo* DNA/RNA motif searching.
Original source code is available [here](http://smithlabresearch.org/software/dme/), or [here](https://github.com/smithlabcode/dme).

I tried to install it, but both of the sources returned many errors when trying to compile and install them.
I just edited the source code a little to make it **actually INSTALLABLE**.  
Notice that I did not add, delete or modify any process of motif searching.

Tested on Ubuntu 10.04.4 at 2017/01/09.

## Requirements
Just like the original program, it requires `popt` library.

## Installation
```
$ git clone https://github.com/Sihyung-Park/DME2_beta_fixed
$ cd DME2_beta_fixed
$ make && make install
```

`$` is a command line prompt.

You might have to `sudo make install` instead of `make install`.

## Use
Follow `README_DME2` file of the original program.

## License
Just like the original program, it follows GNU GPL.
