.. _extensions-extffi:


.. _ext-ffi:

ext/ffi
+++++++

.. meta::
	:description:
		ext/ffi: Extension ``FFI`` : Foreign Function Interface .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ffi
	:twitter:description: ext/ffi: Extension ``FFI`` : Foreign Function Interface 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ffi
	:og:type: article
	:og:description: Extension ``FFI`` : Foreign Function Interface 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ffi.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extffi.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extffi.html","name":"ext\/ffi","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ``FFI`` : Foreign Function Interface ","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/ffi.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


