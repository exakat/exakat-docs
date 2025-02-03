.. _exceptions-setchainingexception:

.. _set-chaining-exception:

Set Chaining Exception
++++++++++++++++++++++

.. meta::
	:description:
		Set Chaining Exception: Chaining exception allows rethrowing a caught exception with a new one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Chaining Exception
	:twitter:description: Set Chaining Exception: Chaining exception allows rethrowing a caught exception with a new one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Chaining Exception
	:og:type: article
	:og:description: Chaining exception allows rethrowing a caught exception with a new one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Chaining Exception.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/SetChainingException.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/SetChainingException.html","name":"Set Chaining Exception","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Chaining exception allows rethrowing a caught exception with a new one","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Set Chaining Exception.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Chaining `exception <https://www.php.net/exception>`_ allows rethrowing a caught `exception <https://www.php.net/exception>`_ with a new one. The previous `exception <https://www.php.net/exception>`_ is added to the new `exception <https://www.php.net/exception>`_, for later reference.

For that, the constructor of the chaining `exception <https://www.php.net/exception>`_ must relay the previous one to the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ constructor.

.. code-block:: php
   
   <?php
   
   //
   class myChainingException{
   	function __construct($message, $code = 0, \Throwable $exception = null) {
   		// This exception can be chained
   		parent::__construct($message, $code, $exception);
   	}
   }
   
   // No chaining possible
   class myException{
   	function __construct($message) {
   		// This exception can't chain anything
   		parent::__construct($message);
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `chaining-exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/chaining-exception.ini.html>`_


Suggestions
___________

* Add the default values to allow chaining




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/SetChainingException                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


