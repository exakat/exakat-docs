.. _extensions-extdecimal:


.. _ext-decimal:

ext/decimal
+++++++++++

.. meta::
	:description:
		ext/decimal: Extension php-decimal, by ``Rudi Theunissen``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/decimal
	:twitter:description: ext/decimal: Extension php-decimal, by ``Rudi Theunissen``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/decimal
	:og:type: article
	:og:description: Extension php-decimal, by ``Rudi Theunissen``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/decimal.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extdecimal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extdecimal.html","name":"ext\/decimal","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension php-decimal, by ``Rudi Theunissen``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/decimal.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension php-decimal, by ``Rudi Theunissen``.

This library provides a PHP extension that adds support for correctly-rounded, arbitrary-precision decimal floating point arithmetic. Applications that rely on accurate numbers (ie. money, measurements, or mathematics) can use Decimal instead of float or string to represent numerical values.

.. code-block:: php
   
   <?php
   
   use Decimal\Decimal;
   
   $op1 = new Decimal("0.1", 4);
   $op2 = "0.123456789";
   
   print_r($op1 + $op2);
   
   
   use Decimal\Decimal;
   
   /**
    * @param int $n The factorial to calculate, ie. $n!
    * @param int $p The precision to calculate the factorial to.
    *
    * @return Decimal
    */
   function factorial(int $n, int $p = Decimal::DEFAULT_PRECISION): Decimal
   {
       return $n < 2 ? new Decimal($n, $p) : $n * factorial($n - 1, $p);
   }
   
   echo factorial(10000, 32);
   
   ?>

See also `PHP Decimal <http://php-decimal.io>`_ and `libmpdec <http://www.bytereef.org/mpdecimal/quickstart.html>`_.

Connex PHP features
-------------------

  + `Extensions <https://php-dictionary.readthedocs.io/en/latest/dictionary/extension.ini.html>`_
  + `Floating Point Numbers <https://php-dictionary.readthedocs.io/en/latest/dictionary/float.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extdecimal                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


