.. _php-cookiesvariables:


.. _cookies-variables:

Cookies Variables
+++++++++++++++++

.. meta::
	:description:
		Cookies Variables: Cookies names, used across the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cookies Variables
	:twitter:description: Cookies Variables: Cookies names, used across the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cookies Variables
	:og:type: article
	:og:description: Cookies names, used across the application
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cookies Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CookiesVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CookiesVariables.html","name":"Cookies Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Cookies names, used across the application","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cookies Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Cookies names, used across the application.

.. code-block:: php
   
   <?php
   
   if (isset($_COOKIE['myCookie'])) {
       // Usual method for reading and setting cookies
       $_COOKIE['myCookie']++;
   }
   
   // Usual method for writing cookies
   setcookie('myCookie', $value);
   
   ?>

See also `setcookie <http://www.php.net/setcookie>`_.

Connex PHP features
-------------------

  + `Cookie <https://php-dictionary.readthedocs.io/en/latest/dictionary/cookie.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CookiesVariables                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.16                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


