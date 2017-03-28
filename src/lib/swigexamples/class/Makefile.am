AM_CFLAGS = -I$(top_srcdir)/src/lib
AM_CXXFLAGS = `php-config --includes` -march=native -mtune=native  -fPIC

example_wrap.cpp: example.cxx  example.h example.i
	swig -c++ -php -module libkk71swigexamplesclass example.i

BUILT_SOURCES = example_wrap.cpp
CLEANFILES = example_wrap.cpp php_example.h example.php 

# Work around forbidden directory combinations.
my_libdir = $(libdir)/kk71swigphp/examples/class
my_lib_SCRIPTS = runme.php libkk71swigexamplesclass.php
my_lib_LTLIBRARIES = libkk71swigexamplesclass.la

libkk71swigexamplesclass_la_CPPFLAGS=-DNDEBUG

libkk71swigexamplesclass_la_SOURCES = example_wrap.cpp example.cxx 



