.. _php-issetmultipleargs:

.. _isset-multiple-arguments:

Isset Multiple Arguments
++++++++++++++++++++++++

.. meta::
	:description:
		Isset Multiple Arguments: isset() may be used with multiple arguments and acts as a AND.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Isset Multiple Arguments
	:twitter:description: Isset Multiple Arguments: isset() may be used with multiple arguments and acts as a AND
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Isset Multiple Arguments
	:og:type: article
	:og:description: isset() may be used with multiple arguments and acts as a AND
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Isset Multiple Arguments.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IssetMultipleArgs.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IssetMultipleArgs.html","name":"Isset Multiple Arguments","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"isset() may be used with multiple arguments and acts as a AND","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Isset Multiple Arguments.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`isset() <https://www.www.php.net/isset>`_ may be used with multiple arguments and acts as a AND.

.. code-block:: php
   
   <?php
   
   // isset without and 
   if (isset($a, $b, $c)) {
       // doSomething()
   }
   
   // isset with and 
   if (isset($a) && isset($b) && isset($c)) {
       // doSomething()
   }
   
   ?>

See also `Isset <http://www.php.net/isset>`_.

Connex PHP features
-------------------

  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_
  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_


Suggestions
___________

* Merge all isset() calls into one




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IssetMultipleArgs                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thinkphp-php-issetmultipleargs`, :ref:`case-livezilla-php-issetmultipleargs`                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


