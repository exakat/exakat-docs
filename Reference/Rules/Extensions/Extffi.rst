.. _extensions-extffi:

.. _ext-ffi:

ext/ffi
+++++++

  Extension ``FFI`` : Foreign Function Interface .

This extension allows the loading of shared libraries (.DLL or .so), calling of C functions and accessing of C data structures in pure PHP, without having to have deep knowledge of the Zend extension API, and without having to learn a third “intermediate” language. The public API is implemented as a single class `FFI <https://www.php.net/ffi>`_ with several `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods (some of them may be called dynamically), and overloaded object methods, which perform the actual interaction with C data.

.. code-block:: php
   
   <?php
   //Example : Calling a function from shared library
   // create FFI object, loading libc and exporting function printf()
   $ffi = FFI::cdef(
       "int printf(const char *format, ...);", // this is a regular C declaration
       "libc.so.6");
   // call C's printf()
   $ffi->printf("Hello %s!\n", "world");
   ?>

See also `ext/ffi <https://github.com/dstogov/php-ffi>`_ and `A PHP Compiler, aka The FFI Rabbit Hole <https://blog.ircmaxell.com/2019/04/compilers-ffi.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extffi                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


