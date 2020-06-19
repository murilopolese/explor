# Explor

This is a re-implementation of Ken Knowlton's Mini Explor system described in
two ACM papers -

http://portal.acm.org/citation.cfm?id=807020
http://portal.acm.org/citation.cfm?id=988052

See the examples directory for examples.

It's covered by the GPL but unless you distribute code written using it that
won't affect your use of it.

## Installing

*Adapted from [robmyers'](https://robmyers.org/2011/01/04/explor_update/) website*

You’ll need git, autotools, libtool and g77 installed. On Fedora the command to install them is something like:

`sudo apt install git gfortran libtool autoconf automake`

Fetch the source code:

`git clone https://github.com/murilopolese/explor.git`

Set up the build environment:

```
cd explor
./bootstrap
./configure
make
sudo make install # Take care with sudo!
```

It seems it needs sudo just to place the `explor` binary at `/usr/local/bin`. You might need to restart your bash session or `source ~/.bashrc` (or `source ~/.zshrc`) before being able to call `explor`.

## Running te examples

You can then make a test image:

```
cd examples
explor example6.explor
```

This will print messages something like this:

```
Compiling example6.explor to example6
Running example6 with output to example6.ps
```

There should be a PDF file on the examples folder with the output image.
