.. _php-uppercasekeyword:

.. _non-lowercase-keywords:

Non-lowercase Keywords
++++++++++++++++++++++

.. meta::
	:description:
		Non-lowercase Keywords: The usual convention is to write PHP keywords (like ``as``, ``foreach``, ``switch``, ``case``, ``break``, etc.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Non-lowercase Keywords
	:twitter:description: Non-lowercase Keywords: The usual convention is to write PHP keywords (like ``as``, ``foreach``, ``switch``, ``case``, ``break``, etc
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Non-lowercase Keywords
	:og:type: article
	:og:description: The usual convention is to write PHP keywords (like ``as``, ``foreach``, ``switch``, ``case``, ``break``, etc
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Non-lowercase Keywords.html
	:og:locale: en
The usual convention is to write PHP keywords (like ``as``, ``foreach``, ``switch``, ``case``, ``break``, etc.) all in lowercase. 



PHP understands them in lowercase, UPPERCASE or WilD Case, so there is nothing compulsory here. Although, it will look strange to many. 

Some keywords are missing from this analysis : ``extends``, ``implements``, ``as``. This is due to the internal `engine <https://www.php.net/engine>`_, which doesn't keep track of them in its AST representation.

.. code-block:: php
   
   <?php
   
   // usual PHP convention
   foreach($array as $element) {
       echo $element;
   }
   
   // unusual PHP conventions
   Foreach($array AS $element) {
       eCHo $element;
   }
   
   ?>
Connex PHP features
-------------------

  + `case <https://php-dictionary.readthedocs.io/en/latest/dictionary/case.ini.html>`_


Suggestions
___________

* Use lowercase only PHP keywords, except for constants such as __CLASS__.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UpperCaseKeyword                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


