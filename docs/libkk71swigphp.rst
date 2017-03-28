
Github: https://github.com/kresimir71/libkk71swigphp

What is it about?
*************************

This is a project to enable using 'swig' with C/C++ dynamic libraries for usage with PHP version 5.

How does it work?
*********************************

The project is based on gnu automake system. Many original 'swig' project examples of dynamic c/c++ libraries called from PHP are copied here. These examples are placed in src/lib/swigexamples subdirectory.

The project can be built as follows on an Ubuntu system with PHP 5.6.29:

.. code-block:: guess

 git clone https://github.com/kresimir71/libkk71swigphp.git
 cd libkk71swigphp
 autoreconf --make --install --force
 ./configure
 make install

To test 'simple' example from 'swig' distribution:

.. code-block:: guess

 cd /usr/local/lib/kk71swigphp/examples/simple
 php -n -q -d extension_dir=. -d safe_mode=Off runme.php

To test 'class' example from 'swig' distribution:

.. code-block:: guess

 cd /usr/local/lib/kk71swigphp/examples/class
 php -n -q -d extension_dir=. -d safe_mode=Off runme.php

.. API
.. ********************************

.. Tutorial
.. *******************
