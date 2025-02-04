.. _classes-uselesstypehint:


.. _useless-type:

Useless Type
++++++++++++

.. meta::
	:description:
		Useless Type: __get() and __set() magic methods won't enforce any type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Type
	:twitter:description: Useless Type: __get() and __set() magic methods won't enforce any type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Type
	:og:type: article
	:og:description: __get() and __set() magic methods won't enforce any type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessTypehint.html","name":"Useless Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"__get() and __set() magic methods won't enforce any type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ magic methods won't enforce any type. The name of the magic property is always cast to string.

`__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_

.. code-block:: php
   
   <?php
   
   class x {
       // type is set and ignored
       function __set(float $name, string $value) {
           $this->$name = $value;
       }
   
       // type is set and ignored
       function __get(integer $name) {
           $this->$name = $value;
       }
   
       // type is checked by PHP 8.0 linting
       // type is enforced by PHP 7.x
       function __call(integer $name) {
           $this->$name = $value;
       }
   }
   
   $o = new x;
   $b = array();
   // Property will be called 'Array'
   $o->{$b} = 2;
   
   // type of $m is check at calling time. It must be string.
   $o->{$m}();
   
   ?>

See also `__set <https://www.php.net/manual/en/language.oop5.overloading.php#object.set>`_.

Related PHP errors 
-------------------

  + `Method name must be a string <https://php-errors.readthedocs.io/en/latest/messages/method-name-must-be-a-string.html>`_



Connex PHP features
-------------------

  + `Magic Methods <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Use `string` for the `$name` parameter
* Use no type for the `$name` parameter




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessTypehint                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


