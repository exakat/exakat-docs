.. _php-php7relaxedkeyword:

.. _php7-relaxed-keyword:

Php7 Relaxed Keyword
++++++++++++++++++++

.. meta::
	:description:
		Php7 Relaxed Keyword: Most of the traditional PHP keywords may be used inside classes, enums, traits and interfaces: they can be used as constant or method name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Php7 Relaxed Keyword
	:twitter:description: Php7 Relaxed Keyword: Most of the traditional PHP keywords may be used inside classes, enums, traits and interfaces: they can be used as constant or method name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Php7 Relaxed Keyword
	:og:type: article
	:og:description: Most of the traditional PHP keywords may be used inside classes, enums, traits and interfaces: they can be used as constant or method name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php7 Relaxed Keyword.html
	:og:locale: en
Most of the traditional PHP keywords may be used inside classes, enums, traits and interfaces: they can be used as constant or method name. 

It is recommended to use this syntax cautiously, as it leads to a lot of surprises and confusion from unususpecting developpers.

This was not the case in PHP 5, and will yield parse errors.

.. code-block:: php
   
   <?php
   
   // Compatible with PHP 7.0 + 
   class foo {
   	const array = []; 
   
       // as is a PHP 5 keyword
       public function as() {
       	print_r(self::array);
       }
   }
   
   ?>

See also `Loosening Reserved Word Restrictions <https://www.php.net/manual/en/migration70.other-changes.php#migration70.other-changes.loosening-reserved-words>`_.

Connex PHP features
-------------------

  + `keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/keyword.ini.html>`_
  + `reserved-name <https://php-dictionary.readthedocs.io/en/latest/dictionary/reserved-name.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php7RelaxedKeyword                                                                                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`no-keyword-in-namespace`                                                                                                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


