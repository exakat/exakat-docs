.. _structures-dirthenslash:

.. _\_\_dir\_\_-then-slash:

__DIR__ Then Slash
++++++++++++++++++

.. meta::
	:description:
		__DIR__ Then Slash: __DIR__ must be concatenated with a string starting with /.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: __DIR__ Then Slash
	:twitter:description: __DIR__ Then Slash: __DIR__ must be concatenated with a string starting with /
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: __DIR__ Then Slash
	:og:type: article
	:og:description: __DIR__ must be concatenated with a string starting with /
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/__DIR__ Then Slash.html
	:og:locale: en
`__DIR__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ must be concatenated with a string starting with /.

The magic constant `__DIR__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ holds the name of the current `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_, without final /. When it is used to build path, then the following path fragment must start with /. Otherwise, two directories names will be merged together.

.. code-block:: php
   
   <?php
   
   // __DIR__ = /a/b/c
   // $filePath = /a/b/c/g.php
   
   // /a/b/c/d/e/f.txt : correct path
   echo __DIR__.'/d/e/f.txt';
   echo dirname($filePath).'/d/e/f.txt';
   
   // /a/b/cd/e/f.txt : most probably incorrect path
   echo __DIR__.'d/e/f.txt';
   echo dirname($filePath).'d/e/f.txt';
   
   ?>

Suggestions
___________

* Add a check on __DIR__, as it may be '/' when run at the root of the server
* Add a '/' at the beginning of the path after __DIR__.
* Add a call to realpath() or file_exists(), before accessing the file.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DirThenSlash                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-traq-structures-dirthenslash`                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


