.. _exceptions-coulddropvariable:

.. _could-drop-variable:

Could Drop Variable
+++++++++++++++++++

.. meta::
	:description:
		Could Drop Variable: Suggest removing the variable in catch clause where the variable is not used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Drop Variable
	:twitter:description: Could Drop Variable: Suggest removing the variable in catch clause where the variable is not used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Drop Variable
	:og:type: article
	:og:description: Suggest removing the variable in catch clause where the variable is not used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Drop Variable.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CouldDropVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CouldDropVariable.html","name":"Could Drop Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Suggest removing the variable in catch clause where the variable is not used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Drop Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Suggest removing the variable in catch clause where the variable is not used. The type of the `exception <https://www.php.net/exception>`_ is sufficient to make the catch clause work. Although, it is recommended to use the caught `exception <https://www.php.net/exception>`_, for chaining or logging, for example.

.. code-block:: php
   
   <?php
   
   try {
   	doSomething();
   } catch(Exception1 $e) {
   	// No usage of $e : just drop it from the clause
   } catch(Exception2 $e2) {
   	// $e2 is caught and used. 
   	echo $e2->getMessage();
   }
   
   ?>
Connex PHP features
-------------------

  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_


Suggestions
___________

* Remove the unused variable




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CouldDropVariable                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


