.. _constants-dynamiccreation:


.. _constant-dynamic-creation:

Constant Dynamic Creation
+++++++++++++++++++++++++

.. meta::
	:description:
		Constant Dynamic Creation: Registering constant with dynamic values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Dynamic Creation
	:twitter:description: Constant Dynamic Creation: Registering constant with dynamic values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Dynamic Creation
	:og:type: article
	:og:description: Registering constant with dynamic values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant Dynamic Creation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/DynamicCreation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/DynamicCreation.html","name":"Constant Dynamic Creation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Registering constant with dynamic values","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constant Dynamic Creation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Registering constant with dynamic values. Dynamic values include values read in external sources (files, databases, remote API, `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ ), random sources (time, `rand() <https://www.php.net/rand>`_, `...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_

Dynamic constants are not possible with the ``const`` keyword, though `static <https://www.php.net/manual/en/language.oop5.static.php>`_ constant expression allows for a good range of combinations, including conditions.

.. code-block:: php
   
   <?php
   
   $a = range(0, 4);
   foreach($array as $i) {
       define("A$i", $i);
       define("N$i", true);
   }
   
   define("C", 5);
   
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/DynamicCreation                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                                                                                   |
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


