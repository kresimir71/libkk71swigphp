AM_CFLAGS = -I$(top_srcdir)/src/lib `php-config --includes` -march=native -mtune=native  -fPIC
#AM_CXXFLAGS = `php-config --includes` -march=native -mtune=native  -fPIC

example_wrap.c: example.c example.i
	swig -php -module libkk71swigexamplessimple example.i

BUILT_SOURCES = example_wrap.c
CLEANFILES = example_wrap.c php_example.h example.php 

# Work around forbidden directory combinations.
my_libdir = $(libdir)/kk71swigphp/examples/simple
my_lib_SCRIPTS = runme.php libkk71swigexamplessimple.php
my_lib_LTLIBRARIES = libkk71swigexamplessimple.la

libkk71swigexamplessimple_la_CPPFLAGS=-DNDEBUG

libkk71swigexamplessimple_la_SOURCES = example_wrap.c example.c 



