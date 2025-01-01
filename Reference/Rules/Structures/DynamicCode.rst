.. _structures-dynamiccode:

.. _dynamic-code:

Dynamic Code
++++++++++++

.. meta::
	:description:
		Dynamic Code: List of instructions that were left during analysis, as they rely on dynamic data.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Code
	:twitter:description: Dynamic Code: List of instructions that were left during analysis, as they rely on dynamic data
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Code
	:og:type: article
	:og:description: List of instructions that were left during analysis, as they rely on dynamic data
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/DynamicCode.html
	:og:locale: en
List of instructions that were left during analysis, as they rely on dynamic data. 

Any further analysis will need to start from here.

.. code-block:: php
   
   <?php
   
   // Dynamic call to 'method';
   $name = 'method';
   $object->$name();
   
   // Hard coded call to 'method';
   $object->method();
   
   ?>

See also `Variable functions <https://www.php.net/manual/en/functions.variable-functions.php>`_.

Connex PHP features
-------------------

  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DynamicCode                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


