.. _dump-collectmethodsthrowingexceptions:

.. _collect-methods-throwing-exceptions:

Collect Methods Throwing Exceptions
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Methods Throwing Exceptions: This is a list of all the methods and functions that throw exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Methods Throwing Exceptions
	:twitter:description: Collect Methods Throwing Exceptions: This is a list of all the methods and functions that throw exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Methods Throwing Exceptions
	:og:type: article
	:og:description: This is a list of all the methods and functions that throw exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Methods Throwing Exceptions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectMethodsThrowingExceptions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectMethodsThrowingExceptions.html","name":"Collect Methods Throwing Exceptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This is a list of all the methods and functions that throw exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Methods Throwing Exceptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This is a list of all the methods and functions that throw `exception <https://www.php.net/exception>`_.

This rule reports explicit throw's, and doesn't list exceptions passing through : for example, when the `exception <https://www.php.net/exception>`_ is thrown in a sub-call, but not caught yet.

.. code-block:: php
   
   <?php
   
   function foo($a) {
   	if ($a % 2) {
   		throw new Exception('This is not an even number');
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectMethodsThrowingExceptions                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


