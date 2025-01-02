.. _structures-sprintfformatcompilation:

.. _sprintf-format-compilation:

Sprintf Format Compilation
++++++++++++++++++++++++++

.. meta::
	:description:
		Sprintf Format Compilation: The sprintf() format used yields an error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Sprintf Format Compilation
	:twitter:description: Sprintf Format Compilation: The sprintf() format used yields an error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Sprintf Format Compilation
	:og:type: article
	:og:description: The sprintf() format used yields an error
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sprintf Format Compilation.html
	:og:locale: en
The `sprintf() <https://www.php.net/sprintf>`_ format used yields an `error <https://www.php.net/error>`_. A format is a ``%`` pourcent character, followed by a letter. 

Some letters are not allowed: ``a, i, j, k, l, m, n, p, q, r, t, v, w, y, z, A, B, C, D, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, Y, Z``.

This applies to `printf() <https://www.php.net/printf>`_, `sprintf() <https://www.php.net/sprintf>`_, `vprintf() <https://www.php.net/vprintf>`_, `vfprintf() <https://www.php.net/vfprintf>`_, `vsprintf() <https://www.php.net/vsprintf>`_, `sscanf() <https://www.php.net/sscanf>`_, `fscanf() <https://www.php.net/fscanf>`_

.. code-block:: php
   
   <?php
   
       printf('\%we3e\\', 123); 
       //Unknown format specifier \w\\
   ?>

See also `sprintf <https://www.php.net/manual/en/function.sprintf.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Unknown+format+specifier.html>`_



Connex PHP features
-------------------

  + `sprintf <https://php-dictionary.readthedocs.io/en/latest/dictionary/sprintf.ini.html>`_


Suggestions
___________

* Fix the format




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SprintfFormatCompilation                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


