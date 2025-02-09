.. _classes-hasmagicproperty:


.. _has-magic-method:

Has Magic Method
++++++++++++++++

.. meta::
	:description:
		Has Magic Method: The class has defined one of the magic methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Magic Method
	:twitter:description: Has Magic Method: The class has defined one of the magic methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Magic Method
	:og:type: article
	:og:description: The class has defined one of the magic methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Magic Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/HasMagicProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/HasMagicProperty.html","name":"Has Magic Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The class has defined one of the magic methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Has Magic Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The class has defined one of the magic methods.

The magic methods are  : `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__callStatic() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__sleep() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__wakeup() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__invoke() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set_state() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

`__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ and `__destruct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ are omitted here.

.. code-block:: php
   
   <?php
   
   class WithMagic {
       // some more methods, const or properties
       
       public function __get() {
           // doSomething();
       }
   }
   
   ?>

See also `Property overloading <https://www.php.net/manual/en/language.oop5.overloading.php#language.oop5.overloading.members>`_..

Connex PHP features
-------------------

  + `Magic Methods <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HasMagicProperty                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
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


