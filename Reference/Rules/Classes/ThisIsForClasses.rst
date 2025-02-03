.. _classes-thisisforclasses:


.. _$this-belongs-to-classes-or-traits:

$this Belongs To Classes Or Traits
++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		$this Belongs To Classes Or Traits: The pseudo-variable $this must be used inside a class or trait, or bound closures.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: $this Belongs To Classes Or Traits

	:twitter:description: $this Belongs To Classes Or Traits: The pseudo-variable $this must be used inside a class or trait, or bound closures

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: $this Belongs To Classes Or Traits

	:og:type: article

	:og:description: The pseudo-variable $this must be used inside a class or trait, or bound closures

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/$this Belongs To Classes Or Traits.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ThisIsForClasses.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ThisIsForClasses.html","name":"$this Belongs To Classes Or Traits","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"The pseudo-variable $this must be used inside a class or trait, or bound closures","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/$this Belongs To Classes Or Traits.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The pseudo-variable `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ must be used inside a class or trait, or bound closures. 

`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable represents the current object, inside a class or trait scope

It is a pseudo-variable, and should be used within class's or trait's methods and not outside. It should also not be used in `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods.

PHP 7.1 is stricter and check for `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ at several situations.

.. code-block:: php
   
   <?php
   
   // as an argument
   function foo($this) {
       // Using global
       global $this;
       // Using static (not a property)
       static $this;
       
       // Can't unset it
       unset($this);
       
       try {
           // inside a foreach
           foreach($a as $this) {  }
           foreach($a as $this => $b) {  }
           foreach($a as $b => $this) {  }
       } catch (Exception $this) {
           // inside a catch
       }
       
       // with Variable Variable
       $a = this;
       $$a = 42;
   }
   
   class foo {
       function bar() {
           // Using references
           $a =& $this;
           $a = 42;
           
           // Using extract(), parse_str() or similar functions
           extract([this => 42]);  // throw new Error(Cannot re-assign $this)
           var_dump($this);
       }
   
       static function __call($name, $args) {
           // Using __call
           var_dump($this); // prints object(C)#1 (0) {}, php-7.0 printed NULL
           $this->test();   // prints ops
       }
   
   }
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Related PHP errors 
-------------------

  + `Using $this when not in object context <https://php-errors.readthedocs.io/en/latest/messages/using-%24this-when-not-in-object-context.html>`_



Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_
  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Do not use `$this` as a variable name, except for the current object, in a class, trait or closure.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ThisIsForClasses                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-classes-thisisforclasses`                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


