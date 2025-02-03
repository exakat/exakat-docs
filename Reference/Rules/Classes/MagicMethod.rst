.. _classes-magicmethod:

.. _magic-methods:

Magic Methods
+++++++++++++

.. meta::
	:description:
		Magic Methods: List of PHP magic methods being used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Magic Methods
	:twitter:description: Magic Methods: List of PHP magic methods being used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Magic Methods
	:og:type: article
	:og:description: List of PHP magic methods being used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Magic Methods.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MagicMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MagicMethod.html","name":"Magic Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of PHP magic methods being used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Magic Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of PHP magic methods being used. The magic methods are 

`__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__callStatic() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__sleep() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__wakeup() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__invoke() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set_state() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

``__construct`` and ``__destruct`` are omitted here, as they are routinely used to create and destroy objects.

.. code-block:: php
   
   <?php
   
   class foo{
       // PHP Magic method, called when cloning an object.
       function __clone() {}
   }
   ?>
Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MagicMethod                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


