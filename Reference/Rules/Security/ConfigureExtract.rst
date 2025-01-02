.. _security-configureextract:

.. _configure-extract:

Configure Extract
+++++++++++++++++

.. meta::
	:description:
		Configure Extract: The extract() function overwrites local variables when left unconfigured.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Configure Extract
	:twitter:description: Configure Extract: The extract() function overwrites local variables when left unconfigured
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Configure Extract
	:og:type: article
	:og:description: The extract() function overwrites local variables when left unconfigured
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Configure Extract.html
	:og:locale: en
The `extract() <https://www.php.net/extract>`_ function overwrites local variables when left unconfigured.

Extract imports variables from an array into the local scope. In case of a conflict, that is when a local variable already exists, it overwrites the previous variable.

In fact, `extract() <https://www.php.net/extract>`_ may be configured to handle the situation differently : it may skip the conflicting variable, prefix it, prefix it only if it exists, only import overwriting variables... It may also import them as references to the original values.

This analysis reports `extract() <https://www.php.net/extract>`_ when it is not configured explicitly. If overwriting is the intended objective, it is not reported.
Always avoid using `extract() <https://www.php.net/extract>`_ on untrusted sources, such as ``$_GET``, ``$_POST``, ``$_FILES``, or even databases records.

.. code-block:: php
   
   <?php
   
   // ignore overwriting variables
   extract($array, EXTR_SKIP);
   
   // prefix all variables explicitly variables with 'php_'
   extract($array, EXTR_PREFIX_ALL, 'php_');
   
   // overwrites explicitly variables
   extract($array, EXTR_OVERWRITE);
   
   // overwrites implicitely variables : do we really want that? 
   extract($array, EXTR_OVERWRITE);
   
   ?>

See also `extract <https://www.php.net/extract>`_.

Connex PHP features
-------------------

  + `extract <https://php-dictionary.readthedocs.io/en/latest/dictionary/extract.ini.html>`_
  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Always use the second argument of extract(), and avoid using ``EXTR_OVERWRITE``




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/ConfigureExtract                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-security-configureextract`, :ref:`case-dolibarr-security-configureextract`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


