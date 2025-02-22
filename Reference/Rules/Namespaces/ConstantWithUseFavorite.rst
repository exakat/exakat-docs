.. _namespaces-constantwithusefavorite:


.. _constant--with-or-without-use:

Constant : With Or Without Use
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Constant : With Or Without Use: This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant : With Or Without Use
	:twitter:description: Constant : With Or Without Use: This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant : With Or Without Use
	:og:type: article
	:og:description: This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant : With Or Without Use.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/ConstantWithUseFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/ConstantWithUseFavorite.html","name":"Constant : With Or Without Use","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constant : With Or Without Use.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   use const AA as BB;
   
   // This is the fully qualified name. 
   echo \AA;
   
   // If this is used 10 times or more, then it is the standard. 
   echo BB;
   
   ?>
Connex PHP features
-------------------

  + `Fully Qualified Name <https://php-dictionary.readthedocs.io/en/latest/dictionary/fully-qualified-name.ini.html>`_
  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_
  + `Use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/ConstantWithUseFavorite                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
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


