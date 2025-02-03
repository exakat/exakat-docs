.. _type-printf:


.. _printf-format-inventory:

Printf Format Inventory
+++++++++++++++++++++++

.. meta::
	:description:
		Printf Format Inventory: All format used in the code with printf(), vprintf(), sprintf(), scanf() and fscanf().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Printf Format Inventory
	:twitter:description: Printf Format Inventory: All format used in the code with printf(), vprintf(), sprintf(), scanf() and fscanf()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Printf Format Inventory
	:og:type: article
	:og:description: All format used in the code with printf(), vprintf(), sprintf(), scanf() and fscanf()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Printf Format Inventory.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Printf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Printf.html","name":"Printf Format Inventory","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"All format used in the code with printf(), vprintf(), sprintf(), scanf() and fscanf()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Printf Format Inventory.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

All format used in the code with `printf() <https://www.php.net/printf>`_, `vprintf() <https://www.php.net/vprintf>`_, `sprintf() <https://www.php.net/sprintf>`_, scanf() and `fscanf() <https://www.php.net/fscanf>`_.

.. code-block:: php
   
   <?php
   
   // Display a number with 2 digits
   echo printf("%'.2d\n", 123);
   
   ?>
Connex PHP features
-------------------

  + `printf <https://php-dictionary.readthedocs.io/en/latest/dictionary/printf.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Printf                                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.0                                                                                                                                                                                   |
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


