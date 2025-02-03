.. _exceptions-convertedexceptions:

.. _converted-exceptions:

Converted Exceptions
++++++++++++++++++++

.. meta::
	:description:
		Converted Exceptions: Converted exceptions is when an exception is caught, then immediately converted into another one and thrown again.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Converted Exceptions
	:twitter:description: Converted Exceptions: Converted exceptions is when an exception is caught, then immediately converted into another one and thrown again
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Converted Exceptions
	:og:type: article
	:og:description: Converted exceptions is when an exception is caught, then immediately converted into another one and thrown again
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Converted Exceptions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ConvertedExceptions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ConvertedExceptions.html","name":"Converted Exceptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Converted exceptions is when an exception is caught, then immediately converted into another one and thrown again","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Converted Exceptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Converted exceptions is when an `exception <https://www.php.net/exception>`_ is caught, then immediately converted into another one and thrown again.

Sometimes, extra operations take place, such as logging or `error <https://www.php.net/error>`_ couting.

.. code-block:: php
   
   <?php
   
   try {
   	doSomething();
   } catch (MyException $e) {
   	log($e->getMessage());
   	throw new BadRequestException();
   }
   
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `try <https://php-dictionary.readthedocs.io/en/latest/dictionary/try.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ConvertedExceptions                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


