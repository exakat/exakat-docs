.. _exceptions-trynocatch:


.. _try-without-catch:

Try Without Catch
+++++++++++++++++

.. meta::
	:description:
		Try Without Catch: Try may only hold a finally clause, to ensure that some code is always executed, in case of error or not.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Try Without Catch
	:twitter:description: Try Without Catch: Try may only hold a finally clause, to ensure that some code is always executed, in case of error or not
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Try Without Catch
	:og:type: article
	:og:description: Try may only hold a finally clause, to ensure that some code is always executed, in case of error or not
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Try Without Catch.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/TryNoCatch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/TryNoCatch.html","name":"Try Without Catch","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Try may only hold a finally clause, to ensure that some code is always executed, in case of error or not","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Try Without Catch.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Try may only hold a finally clause, to ensure that some code is always executed, in case of `error <https://www.php.net/error>`_ or not.

This is very rare.

.. code-block:: php
   
   <?php
   
   try {
   	$x = doSomething();
   } finally {
   	if (!isset($x)) {
   		$x = 'Error';
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `try <https://php-dictionary.readthedocs.io/en/latest/dictionary/try.ini.html>`_
  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_
  + `finally <https://php-dictionary.readthedocs.io/en/latest/dictionary/finally.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/TryNoCatch                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


