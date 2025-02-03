.. _classes-couldbestatic:


.. _method-could-be-static:

Method Could Be Static
++++++++++++++++++++++


.. meta::

	:description:

		Method Could Be Static: A method that doesn't make any usage of $this could be turned into a static method.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Method Could Be Static

	:twitter:description: Method Could Be Static: A method that doesn't make any usage of $this could be turned into a static method

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Method Could Be Static

	:og:type: article

	:og:description: A method that doesn't make any usage of $this could be turned into a static method

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Could Be Static.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeStatic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeStatic.html","name":"Method Could Be Static","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A method that doesn't make any usage of $this could be turned into a static method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Could Be Static.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method that doesn't make any usage of `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ could be turned into a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. 

While `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are usually harder to handle, recognizing the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ status is a first step before turning the method into a standalone function.

.. code-block:: php
   
   <?php
   
   class foo {
       static $property = 1;
       
       // legit static method
       static function staticMethod() {
           return self::$property;
       }
   
       // This is not using $this, and could be static
       function nonStaticMethod() {
           return self::$property;
       }
   
       // This is not using $this nor self, could be a standalone function
       function nonStaticMethod() {
           return self::$property;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Make the method static
* Make the method a standalone function
* Make use of $this in the method : may be it was forgotten.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeStatic                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-classes-couldbestatic`, :ref:`case-expressionengine-classes-couldbestatic`                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


