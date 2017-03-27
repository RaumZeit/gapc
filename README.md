# GAP-C

The Bellman's GAP Compiler (GAP-C) is the novel ADP compiler which
translates GAP-L programs into efficient C++ code. It implements
several semantic analyses for optimization purposes, error reporting,
type checking and automatic table design.

The compiler is free and open-source. You can install it directly
from popular linux distributions or download the source code. It
is written in C++ and uses flex and bison for its lexer and parser.

Bellman's GAP which is a programming system for writing dynamic programming algorithms over sequential data. It is the second generation implementation of the algebraic dynamic programming framework (ADP).

### Install
It is recommended to install GAP-C from the distribution's package
manager (unless you want to develop GAP-C itself).

### Ubuntu
Bellman's GAP is available as a pre-compiled Debian package via
Ubuntus launchpad system, a Ubuntu Personal Package Archive (PPA).
On your command line, execute the three following commands
```
sudo add-apt-repository ppa:bibi-help/bibitools
sudo apt-get update
sudo apt-get install bellmansgapc
```

### MacPorts
Under Mac OS X you may want to use [MacPorts](https://www.macports.org)
to install the compiler. There is a ports description on the BiBiServ
MacPorts repository.

Gapc depends (amongst other libraries) on boost. The boost library
must be build with the same compiler environment as gapc. Therefore,
to be sure that gapc will work, boost should be rebuild.

__Attention! This could be a problem for existing programs referencing a possibly previous installed boost library.__

Install compiler enviroment :
```
sudo port install gcc48 
```
If you have no previous boost installation, call :
```
sudo port -ns install configure.compiler=macports-gcc-4.8 
```
Otherwise boost needs to be upgraded :
```
sudo port -ns upgrade --force boost configure.compiler=macports-gcc-4.8 
```
You can then install GAP-C via:
```
sudo port install http://bibiserv.techfak.uni-bielefeld.de/resources/macports/ports/lang/gapc.tgz
```

### Compile and Install
You can compile and install Bellman's GAP from source. Always download the latest version at (Password: hganon):
```
hg clone ssh://hganon@hg.cebitec.uni-bielefeld.de/pi/software/gapc
```
To install Bellman's GAP from source call:
```
./configure --prefix=[install-path]
make
make install
```

### Authors
G. Sauthoff, T. Gatter

Users of Bellman's GAP Cafe are requested to cite :

_Sauthoff, Georg and Janssen, Stefan and Giegerich, Robert_

[Bellman's GAP - A Declarative Language for Dynamic Programming](http://dx.doi.org/10.1145/2003476.2003484), ACM, 2011
