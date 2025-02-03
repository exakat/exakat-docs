.. _constants-isphpconstant:

.. _is-php-constant:

Is PHP Constant
+++++++++++++++

.. meta::
	:description:
		Is PHP Constant: Mark a constant if it is a PHP constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is PHP Constant
	:twitter:description: Is PHP Constant: Mark a constant if it is a PHP constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is PHP Constant
	:og:type: article
	:og:description: Mark a constant if it is a PHP constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is PHP Constant.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/IsPhpConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/IsPhpConstant.html","name":"Is PHP Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Mark a constant if it is a PHP constant","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Is PHP Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Mark a constant if it is a PHP constant.

.. code-block:: php
   
   <?php
   
   // This is an PHP constant
   $a = HTML_ENTITIES;
   
   // This is an PHP function
   $a = CMS_ORDER;
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/IsPhpConstant                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


