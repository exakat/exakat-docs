.. _classes-scalarorobjectproperty:


.. _scalar-or-object-property:

Scalar Or Object Property
+++++++++++++++++++++++++

.. meta::
	:description:
		Scalar Or Object Property: Property shouldn't use both object and scalar syntaxes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Scalar Or Object Property
	:twitter:description: Scalar Or Object Property: Property shouldn't use both object and scalar syntaxes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Scalar Or Object Property
	:og:type: article
	:og:description: Property shouldn't use both object and scalar syntaxes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Scalar Or Object Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ScalarOrObjectProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ScalarOrObjectProperty.html","name":"Scalar Or Object Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Property shouldn't use both object and scalar syntaxes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Scalar Or Object Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Property shouldn't use both object and scalar syntaxes. When a property may be an object, it is recommended to implement the `Null <https://www.php.net/`null <https://www.php.net/null>`_>`_ Object pattern : instead of checking if the property is scalar, make it always object.

.. code-block:: php
   
   <?php
   
   class x {
       public $display = 'echo';
       
       function foo($string) {
           if (is_string($this->display)) {
               echo $this->string;
           } elseif ($this->display instanceof myDisplayInterface) {
               $display->display();
           } else {
               print "Error when displaying\n";
           }
       }
   }
   
   interface myDisplayInterface {
       public function display($string); // does the display in its own way
   }
   
   class nullDisplay implements myDisplayInterface {
       // implements myDisplayInterface but does nothing
       public function display($string) {}
   }
   
   class x2 {
       public $display = null;
       
       public function __construct() {
           $this->display = new nullDisplay();
       }
       
       function foo($string) {
           // Keep the check, as $display is public, and may get wrong values
           if ($this->display instanceof myDisplayInterface) {
               $display->display();
           } else {
               print "Error when displaying\n";
           }
       }
   }
   
   // Simple class for echo
   class echoDisplay implements myDisplayInterface {
       // implements myDisplayInterface but does nothing
       public function display($string) {
           echo $string;
       }
   }
   
   ?>

See also `Null Object Pattern <https://en.wikipedia.org/wiki/Null_Object_pattern#PHP>`_ and `The Null Object Pattern <https://www.sitepoint.com/the-null-object-pattern-polymorphism-in-domain-models/>`_.

Connex PHP features
-------------------

  + `Object <https://php-dictionary.readthedocs.io/en/latest/dictionary/object.ini.html>`_
  + `Scalar Types <https://php-dictionary.readthedocs.io/en/latest/dictionary/scalar-typehint.ini.html>`_


Suggestions
___________

* Only use one type of syntax with your properties.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ScalarOrObjectProperty                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-classes-scalarorobjectproperty`                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


