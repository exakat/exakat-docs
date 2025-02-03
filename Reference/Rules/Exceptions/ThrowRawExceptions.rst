.. _exceptions-throwrawexceptions:


.. _throw-raw-exceptions:

Throw Raw Exceptions
++++++++++++++++++++

.. meta::
	:description:
		Throw Raw Exceptions: Avoid throwing native PHP exceptions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Throw Raw Exceptions
	:twitter:description: Throw Raw Exceptions: Avoid throwing native PHP exceptions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Throw Raw Exceptions
	:og:type: article
	:og:description: Avoid throwing native PHP exceptions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Throw Raw Exceptions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ThrowRawExceptions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/ThrowRawExceptions.html","name":"Throw Raw Exceptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Avoid throwing native PHP exceptions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Throw Raw Exceptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid throwing native PHP exceptions. Consider defining specific and meaningful `exception <https://www.php.net/exception>`_, by extending the native one.
Thanks to `Atif Shahab Qureshi <https://twitter.com/Atif__Shahab>`_ for the inspiration.

.. code-block:: php
   
   <?php
   
   // Throwing a raw exception
   throw new exception('This is an error!');
   
   class myException extends Exception {}
   
   throw new myException('This is a distinguished error!');
   
   ?>

See also `Stop using regular exceptions in PHP! <https://abdlrahmansaber.medium.com/stop-using-regular-exceptions-in-php-e6aed2629dce>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Define an adapted exception and throw it instead




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ThrowRawExceptions                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


