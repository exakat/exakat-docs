.. _constants-variableconstant:


.. _variable-constants:

Variable Constants
++++++++++++++++++

.. meta::
	:description:
		Variable Constants: Variable constants are constants whose value is accessed via the function constant().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable Constants
	:twitter:description: Variable Constants: Variable constants are constants whose value is accessed via the function constant()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable Constants
	:og:type: article
	:og:description: Variable constants are constants whose value is accessed via the function constant()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variable Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/VariableConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/VariableConstant.html","name":"Variable Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Variable constants are constants whose value is accessed via the function constant()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variable Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Variable constants are constants whose value is accessed via the function `constant() <https://www.php.net/constant>`_. Otherwise, there is no way to dynamically access a constant (aka, when the developer has the name of the constant as a incoming parameter, and it requires the value of it).

.. code-block:: php
   
   <?php
   
   const A = 'constant_value';
   
   $constant_name = 'A';
   
   $variableConstant = constant($constant_name);
   
   ?>

See also `constant() <https://www.php.net/constant>`_.

Connex PHP features
-------------------

  + `Dynamic Constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-constant.ini.html>`_
  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/VariableConstant                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


