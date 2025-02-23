.. _exceptions-rethrown:


.. _rethrown-exceptions:

Rethrown Exceptions
+++++++++++++++++++

.. meta::
	:description:
		Rethrown Exceptions: Throwing a caught exception is usually useless and dead code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rethrown Exceptions
	:twitter:description: Rethrown Exceptions: Throwing a caught exception is usually useless and dead code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rethrown Exceptions
	:og:type: article
	:og:description: Throwing a caught exception is usually useless and dead code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Rethrown Exceptions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/Rethrown.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/Rethrown.html","name":"Rethrown Exceptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Throwing a caught exception is usually useless and dead code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Rethrown Exceptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Throwing a caught `exception <https://www.php.net/exception>`_ is usually useless and dead code.

When exceptions are caught, they should be processed or transformed, but not rethrown as is.

Those issues often happen when a catch structure was positioned for debug purposes, but lost its usage later.

.. code-block:: php
   
   <?php
   
   try {
       doSomething();
   } catch (Exception $e) {
       throw $e;
   }
   
   ?>

See also `What are the best practices for catching and re-throwing exceptions? <https://stackoverflow.com/questions/5551668/what-are-the-best-practices-for-catching-and-re-throwing-exceptions/5551828>`_.

Connex PHP features
-------------------

  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Log the message of the exception for later usage.
* Remove the try/catch and let the rest of the application handle this exception.
* Chain the exception, by throwing a new exception, including the caught exception. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/Rethrown                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-exceptions-rethrown`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


