.. _classes-checkoncallusage:


.. _check-on-\_\_call-usage:

Check On __Call Usage
+++++++++++++++++++++

.. meta::
	:description:
		Check On __Call Usage: When using the magic methods __call() and __staticcall(), make sure the method exists before calling it.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check On __Call Usage
	:twitter:description: Check On __Call Usage: When using the magic methods __call() and __staticcall(), make sure the method exists before calling it
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check On __Call Usage
	:og:type: article
	:og:description: When using the magic methods __call() and __staticcall(), make sure the method exists before calling it
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check On __Call Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CheckOnCallUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CheckOnCallUsage.html","name":"Check On __Call Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When using the magic methods __call() and __staticcall(), make sure the method exists before calling it","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check On __Call Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using the magic methods `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and __staticcall(), make sure the method exists before calling it. 

If the method doesn't exists, then the same method will be called again, leading to the same failure. Finally, it will crash PHP.

.. code-block:: php
   
   <?php
   
   class safeCall {
       function __class($name, $args) {
           // unsafe call, no checks
           if (method_exists($this, $name)) {
               $this->$name(...$args);
           }
       }
   }
   
   class unsafeCall {
       function __class($name, $args) {
           // unsafe call, no checks
           $this->$name(...$args);
       }
   }
   
   ?>

See also `Method overloading <https://www.php.net/manual/en/language.oop5.overloading.php#object.call>`_ and `Magical PHP: __call <https://www.garfieldtech.com/index.php/blog/magical-php-call>`_.

Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Add a call to method_exists() before using any method name
* Relay the call to another object that doesn't handle __call() or __callStatic()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CheckOnCallUsage                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


