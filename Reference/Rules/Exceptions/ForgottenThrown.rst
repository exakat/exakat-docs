.. _exceptions-forgottenthrown:


.. _forgotten-thrown:

Forgotten Thrown
++++++++++++++++

.. meta::
	:description:
		Forgotten Thrown: This rule reports when an exception is instantiated, but not thrown.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Forgotten Thrown
	:twitter:description: Forgotten Thrown: This rule reports when an exception is instantiated, but not thrown
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Forgotten Thrown
	:og:type: article
	:og:description: This rule reports when an exception is instantiated, but not thrown
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Forgotten Thrown.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ForgottenThrown.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ForgottenThrown.html","name":"Forgotten Thrown","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule reports when an exception is instantiated, but not thrown","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Forgotten Thrown.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports when an `exception <https://www.php.net/exception>`_ is instantiated, but not thrown. Often, this is a case of forgotten throw.

.. code-block:: php
   
   <?php
   
   class MyException extends \Exception { }
   
   if ($error !== false) {
       // This looks like 'throw' was omitted
       new MyException();
   }
   
   ?>
Connex PHP features
-------------------

  + `throw <https://php-dictionary.readthedocs.io/en/latest/dictionary/throw.ini.html>`_
  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Remove the instantiation expression.
* Add the throw to the new expression.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ForgottenThrown                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


