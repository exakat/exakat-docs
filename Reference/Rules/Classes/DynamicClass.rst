.. _classes-dynamicclass:

.. _dynamic-classes:

Dynamic Classes
+++++++++++++++

.. meta::
	:description:
		Dynamic Classes: This is a list of the dynamic calls of classes used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Classes
	:twitter:description: Dynamic Classes: This is a list of the dynamic calls of classes used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Classes
	:og:type: article
	:og:description: This is a list of the dynamic calls of classes used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Classes.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicClass.html","name":"Dynamic Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"This is a list of the dynamic calls of classes used in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dynamic Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This is a list of the dynamic calls of classes used in the code.

Dynamic classes


.. code-block:: php
   
   <?php
   
   class x {
       static function staticMethod() {}
   }
   
   $class = 'x';
   $class::staticMethod();
   
   ?>
Connex PHP features
-------------------

  + `dynamic-class <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicClass                                                                                                                                                                    |
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
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


