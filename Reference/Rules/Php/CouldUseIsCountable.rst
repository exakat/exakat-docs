.. _php-coulduseiscountable:


.. _use-is\_countable:

Use is_countable
++++++++++++++++

.. meta::
	:description:
		Use is_countable: is_countable() checks if a variables holds a value that can be counted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use is_countable
	:twitter:description: Use is_countable: is_countable() checks if a variables holds a value that can be counted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use is_countable
	:og:type: article
	:og:description: is_countable() checks if a variables holds a value that can be counted
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use is_countable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CouldUseIsCountable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CouldUseIsCountable.html","name":"Use is_countable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"is_countable() checks if a variables holds a value that can be counted","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use is_countable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`is_countable() <https://www.php.net/is_countable>`_ checks if a variables holds a value that can be counted. It is recommended to use it before calling `count() <https://www.php.net/count>`_.

`is_countable() <https://www.php.net/is_countable>`_ accepts arrays and object whose class implements \`countable <https://www.php.net/countable>`_.

.. code-block:: php
   
   <?php
   
   function foo($arg) {
       if (!is_countable($arg)) {
           // $arg cannot be passed to count()
           return 0
       }
       return count($arg);
   }
   
   function bar($arg) {
       if (!is_array($arg) and !$x instanceof \Countable) {
           // $arg cannot be passed to count()
           return 0
       }
   
       return count($arg);
   }
   
   ?>

See also `PHP RFC: is_countable <https://wiki.php.net/rfc/is-countable>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `countable <https://php-dictionary.readthedocs.io/en/latest/dictionary/countable.ini.html>`_


Suggestions
___________

* Use is_countable()
* Create a compatibility function that replaces is_countable() until the code is ready for PHP 7.3




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CouldUseIsCountable                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.3 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


