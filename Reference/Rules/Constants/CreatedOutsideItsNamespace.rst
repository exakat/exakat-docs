.. _constants-createdoutsideitsnamespace:

.. _constants-created-outside-its-namespace:

Constants Created Outside Its Namespace
+++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Constants Created Outside Its Namespace: Constants Created Outside Its Namespace.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constants Created Outside Its Namespace
	:twitter:description: Constants Created Outside Its Namespace: Constants Created Outside Its Namespace
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constants Created Outside Its Namespace
	:og:type: article
	:og:description: Constants Created Outside Its Namespace
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constants Created Outside Its Namespace.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/CreatedOutsideItsNamespace.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/CreatedOutsideItsNamespace.html","name":"Constants Created Outside Its Namespace","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Constants Created Outside Its Namespace","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constants Created Outside Its Namespace.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Constants Created Outside Its Namespace.

Using the `define() <https://www.php.net/define>`_ function, it is possible to create constant outside their namespace, but using the fully qualified namespace.

However, this makes the code confusing and difficult to debug. It is recommended to move the constant definition to its namespace.

.. code-block:: php
   
   <?php
   
   namespace A\B {
       // define A\B\C as 1
       define('C', 1);
   }
   
   namespace D\E {
       // define A\B\C as 1, while outside the A\B namespace
       define('A\B\C', 1);
   }
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Declare the constant in its namespace




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CreatedOutsideItsNamespace                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


