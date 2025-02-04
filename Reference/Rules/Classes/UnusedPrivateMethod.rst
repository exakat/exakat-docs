.. _classes-unusedprivatemethod:


.. _unused-private-methods:

Unused Private Methods
++++++++++++++++++++++

.. meta::
	:description:
		Unused Private Methods: Private methods that are not used in the local class are dead code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Private Methods
	:twitter:description: Unused Private Methods: Private methods that are not used in the local class are dead code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Private Methods
	:og:type: article
	:og:description: Private methods that are not used in the local class are dead code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Private Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedPrivateMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedPrivateMethod.html","name":"Unused Private Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Private methods that are not used in the local class are dead code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Private Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Private methods that are not used in the local class are dead code. Protected methods that are not used in the local class or its children, are dead code.

Private methods are reserved for the defining class. Thus, they must be used with the current class, with ``$this`` or ``self\:\:``.

Protected methods, in a standalone class, are also included.
This analysis skips classes that makes `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ dynamic calls, such as ``$this->$method()``.

.. code-block:: php
   
   <?php
   
   class Foo {
       // Those methods are used
       private function method() {}
       private static function staticMethod() {}
   
       // Those methods are not used
       private function unusedMethod() {}
       private static function staticUnusedMethod() {}
       
       public function bar() {
           self::staticMethod();
           $this->method();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Remove the private method, as it is unused
* Add a call to this private method
* Change method visibility to make it available to other classes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedPrivateMethod                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
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
| Related rule | :ref:`unused-public-methods`                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


