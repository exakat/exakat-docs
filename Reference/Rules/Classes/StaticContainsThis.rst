.. _classes-staticcontainsthis:


.. _static-methods-can't-contain-$this:

Static Methods Can't Contain $this
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Static Methods Can't Contain $this: Static methods are also called ``class methods`` : they may be called even if the class has no instantiated object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Methods Can't Contain $this
	:twitter:description: Static Methods Can't Contain $this: Static methods are also called ``class methods`` : they may be called even if the class has no instantiated object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Methods Can't Contain $this
	:og:type: article
	:og:description: Static methods are also called ``class methods`` : they may be called even if the class has no instantiated object
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Methods Can't Contain $this.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticContainsThis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticContainsThis.html","name":"Static Methods Can't Contain $this","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Static methods are also called ``class methods`` : they may be called even if the class has no instantiated object","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Methods Can't Contain $this.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are also called ``class methods`` : they may be called even if the class has no instantiated object. Thus, the local variable ``$this`` won't exist, PHP will set it to `NULL <https://www.php.net/manual/en/language.types.null.php>`_ as usual. 
Either this is not a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, which is fixed by removing the ``static`` keyword, or replace all `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ mention by `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties ``Class\:\:$property``.

.. code-block:: php
   
   <?php
   
   class foo {
       // Static method may access other static methods, or property, or none. 
       static function staticBar() {
           // This is not possible in a static method
           return self::otherStaticBar() . static::$staticProperty;
       }
   
       static function bar() {
           // This is not possible in a static method
           return $this->property;
       }
   }
   
   ?>

See also `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>``Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_.

Related PHP errors 
-------------------

  + `Using $this when not in object context <https://php-errors.readthedocs.io/en/latest/messages/using-%24this-when-not-in-object-context.html>`_



Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Remove any $this usage
* Turn any $this usage into a static call : $this->foo() => self::foo()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticContainsThis                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-static-this <https://github.com/dseguy/clearPHP/tree/master/rules/no-static-this.md>`__                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-classes-staticcontainsthis`, :ref:`case-sugarcrm-classes-staticcontainsthis`                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


