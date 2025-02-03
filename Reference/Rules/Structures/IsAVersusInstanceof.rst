.. _structures-isaversusinstanceof:

.. _is\_a()-versus-instanceof:

is_a() Versus instanceof
++++++++++++++++++++++++

.. meta::
	:description:
		is_a() Versus instanceof: is_a() and instanceof have the same functional use: checking if an object is of a specific class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: is_a() Versus instanceof
	:twitter:description: is_a() Versus instanceof: is_a() and instanceof have the same functional use: checking if an object is of a specific class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: is_a() Versus instanceof
	:og:type: article
	:og:description: is_a() and instanceof have the same functional use: checking if an object is of a specific class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/is_a() Versus instanceof.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IsAVersusInstanceof.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IsAVersusInstanceof.html","name":"is_a() Versus instanceof","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"is_a() and instanceof have the same functional use: checking if an object is of a specific class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/is_a() Versus instanceof.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`is_a() <https://www.php.net/is_a>`_ and `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ have the same functional use: checking if an object is of a specific class. 

The analyzed code has less than 10% of one of them: either `is_a() <https://www.php.net/is_a>`_ or `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_. For consistency reasons, it is recommended to make them all the same. 

It happens that `is_a() <https://www.php.net/is_a>`_ or instance are used depending on coding style and files. One file may be consistently using `is_a() <https://www.php.net/is_a>`_, while the others are all using `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_. 


.. code-block:: php
   
   <?php
   
   if (is_a($object, $class)) { /**/ }
   
   if ($object instanceof $class) { /**/ }
   
   // Note : code is not representative of actual code.
   
   ?>
Connex PHP features
-------------------

  + `instanceof <https://php-dictionary.readthedocs.io/en/latest/dictionary/instanceof.ini.html>`_


Suggestions
___________

* Adopt one of the two syntaxes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IsAVersusInstanceof                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


