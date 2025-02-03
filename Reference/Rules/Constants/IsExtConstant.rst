.. _constants-isextconstant:

.. _is-an-extension-constant:

Is An Extension Constant
++++++++++++++++++++++++

.. meta::
	:description:
		Is An Extension Constant: This analysis marks a constant when it belongs to an extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is An Extension Constant
	:twitter:description: Is An Extension Constant: This analysis marks a constant when it belongs to an extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is An Extension Constant
	:og:type: article
	:og:description: This analysis marks a constant when it belongs to an extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is An Extension Constant.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/IsExtConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/IsExtConstant.html","name":"Is An Extension Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This analysis marks a constant when it belongs to an extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Is An Extension Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This analysis marks a constant when it belongs to an extension.

.. code-block:: php
   
   <?php
   
   // JSON_HEX_AMP is a constant from ext/json
   echo json_encode($object, JSON_HEX_AMP);
   
   // JSON_HEX_AMP is a constant from ext/json
   echo json_encode($object, JSON_HOAX_AMP);
   
   ?>

See also `Supported PHP Extensions <http://exakat.readthedocs.io/en/latest/Annex.html#supported-php-extensions>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/IsExtConstant                                                                                                                                                                 |
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
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


