.. _classes-undefinedstaticmp:

.. _undefined-static-or-self:

Undefined static\:\: Or self\:\:
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Undefined static:: Or self::: The identified property or method are undefined.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined static:: Or self::
	:twitter:description: Undefined static:: Or self::: The identified property or method are undefined
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined static:: Or self::
	:og:type: article
	:og:description: The identified property or method are undefined
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined static:: Or self::.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedStaticMP.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedStaticMP.html","name":"Undefined static:: Or self::","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The identified property or method are undefined","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined static:: Or self::.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The identified property or method are undefined. `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ refer to the current class, or one of its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or trait.

.. code-block:: php
   
   <?php
   
   class x {
       static public function definedStatic() {}
       private definedStatic = 1;
       
       public function method() {
           self::definedStatic();
           self::undefinedStatic();
   
           static::definedStatic;
           static::undefinedStatic;
       }
   }
   
   ?>

See also `Late Static Bindings <https://www.php.net/manual/en/language.oop5.late-static-bindings.php>`_.

Related PHP errors 
-------------------

  + `Access to undeclared static property: %s::$%s <https://php-errors.readthedocs.io/en/latest/messages/access-to-undeclared-static-property-%25s%3A%3A%24%25s.html>`_
  + `Call to undefined method %s::%s() <https://php-errors.readthedocs.io/en/latest/messages/call-to-undefined-method-%25s%3A%3A%25s%28%29.html>`_



Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Define the missing method or property
* Remove usage of that undefined method or property
* Fix name to call an actual local structure
* Fix object to one of the local property




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedStaticMP                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-classes-undefinedstaticmp`, :ref:`case-sugarcrm-classes-undefinedstaticmp`                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


