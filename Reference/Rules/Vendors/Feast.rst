.. _vendors-feast:


.. _feast-usage:

Feast usage
+++++++++++

.. meta::
	:description:
		Feast usage: This analysis reports usage of the Feast framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Feast usage
	:twitter:description: Feast usage: This analysis reports usage of the Feast framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Feast usage
	:og:type: article
	:og:description: This analysis reports usage of the Feast framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Feast usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Feast.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Feast.html","name":"Feast usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports usage of the Feast framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Feast usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis reports usage of the Feast framework.

FEAST is a radically different PHP Framework that was built from the ground up to be an alternative to the dependency-heavy frameworks that exist already. Its goal is a light-weight footprint that just lets you get stuff done.

.. code-block:: php
   
   <?php
   
   $this->httpRequest->postJson(self::URL . '/subscribers');
   $this->httpRequest->addArguments($data);
   $this->httpRequest->authenticate($this->apiKey, '');
   $this->httpRequest->makeRequest();
   $response = $this-httpRequest->getResponseAsJson();
   
   ?>

See also `Feast <https://docs.feast-framework.com/>`_ and `Feast on github<https://github.com/feastframework/framework>`_.

Connex PHP features
-------------------

  + `Framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Feast                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


