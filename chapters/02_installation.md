Installation
============


Computers don't understand the Scheme program directly, 
so we have to install the development tool which itself is also 
a program.

There are abundant of implementations of Scheme, each one of them has
its own characteristic and optimized for special purpose. 
For the purpose of learning, the most recommended one is Racket.

Racket is an general purpose programming language based on the Scheme Lisp,
It provides not only a collection of Scheme-class programming languages
but also a powerful and friendly integrated development environment.

Racket is a cross-platform software that runs on common operating systems
including Windows, OSX, Linux.


Linux
-----

For Linux users, there are two possible way to install Racket on your
computer.

The first is to use the package management system shipped with
your distribution. For example, Debian/Ubuntu Linux use a package system
named APT, the apt command could be use to install a new software.
For installing Racket, execute the following command in the terminal as
super user;
```
# apt-get install racket
```

The other way is to install by compiling the source of Racket.
Because the Racket is written in C programming language, so 
we have to preinstall the build toolchain before compiling:
```
# apt-get install build-essential
```

download the source code which could be found at:
http://download.racket-lang.org/

Choose the 'Unix Source' option from the combo box and click on the 
download button.

After the downloading finished, move the compressed source code file to 
a temporary directly, such as `/opt/`, the name of downloaded file at the
time of this tutorial been written is `racket-6.1.1-src.tgz`, so
we execute the following commands:

```
# cd ~/Downloads # Enter the download directory
# mv racket-6.1.1-src.tgz /opt/  # Move the file into the temporary directly
# cd /opt/ # Jump to `/opt/'
# tar xzvf racket-6.1.1-src.tgz # Decompress the compressed source code file
# cd racket-6.1.1/src # Enter the source code directory
# ./configure # Generate the Makefile
# make # Build the source code of Racket
# make install # Install Racket
``` 

The compiling costs rather long time that is because the progress doen't
only compile the Racket itself but also the modules with riched functions.

If the steps above been successfully executed, 
racket is already been put in the default executable file searching path.


Windows
-------

The best way for Windows users to install Racket is to download the installation program which could be found at:
http://download.racket-lang.org/

Choose either x64 or x86 version depends on the system you are using, then 
download it directly or from a mirror server at your option. 
The downloaded file should be something similiar to `racket-6.1.1-x86-win32.exe` or `racket-6.1.1-i386-win32.exe`

Double click on the downloaded file, follow the steps to specify the 
path which Racket's going to be installed.


