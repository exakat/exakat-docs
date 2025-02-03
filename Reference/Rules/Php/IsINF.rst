.. _php-isinf:


.. _manipulates-inf:

Manipulates INF
+++++++++++++++

.. meta::
	:description:
		Manipulates INF: This code handles INF situations.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Manipulates INF
	:twitter:description: Manipulates INF: This code handles INF situations
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Manipulates INF
	:og:type: article
	:og:description: This code handles INF situations
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Manipulates INF.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IsINF.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IsINF.html","name":"Manipulates INF","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This code handles INF situations","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Manipulates INF.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This code handles `INF <https://www.php.net/INF>`_ situations. `INF <https://www.php.net/INF>`_ represents the infinity, when used in a float context. It happens when a calculation returns a number that is much larger than the maximum allowed float (not integer), or a number that is not a Division by 0.

.. code-block:: php
   
   <?php
   
   // pow returns INF, as it is equivalent to 1 / 0 ^ 2
   $a = pow(0,-2); // 
   
   // exp returns an actual value, but won't be able to represent it as a float
   $a = exp(PHP_INT_MAX); 
   
   // 0 ^ -1 is like 1 / 0 but returns INF.
   $a = pow(0, -1); 
   
   var_dump(is_infinite($a));
   
   // This yields a Division by zero exception
   $a = 1 / 0; 
   
   ?>

See also `Math predefined constants <https://www.php.net/manual/en/math.constants.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IsINF                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


