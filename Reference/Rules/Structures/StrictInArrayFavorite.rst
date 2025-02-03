.. _structures-strictinarrayfavorite:


.. _strict-in\_array()-preference:

Strict In_Array() Preference
++++++++++++++++++++++++++++


.. meta::

	:description:

		Strict In_Array() Preference: It is possible to set in_array() to strict search mode, by using the third argument.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Strict In_Array() Preference

	:twitter:description: Strict In_Array() Preference: It is possible to set in_array() to strict search mode, by using the third argument

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Strict In_Array() Preference

	:og:type: article

	:og:description: It is possible to set in_array() to strict search mode, by using the third argument

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strict In_Array() Preference.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StrictInArrayFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StrictInArrayFavorite.html","name":"Strict In_Array() Preference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is possible to set in_array() to strict search mode, by using the third argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strict In_Array() Preference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is possible to set `in_array() <https://www.php.net/in_array>`_ to strict search mode, by using the third argument.

The analyzed code has less than 10% of one of the two sets : for consistency reasons, it is recommended to make them all the same. 

Warning : the two sets of operators have different precedence levels. Using and or && is not exactly the same, especially and not only, when assigning the results to a variable. 
In doubt, it is recommended to use the strict mode.

.. code-block:: php
   
   <?php 
   
   // relax mode : value may use typejuggling with the array values
   in_array($value, $array );
   
   // strict mode : value is compared to array's value with both data and type
   in_array($value, $array, true);
   
   ?>
Connex PHP features
-------------------

  + `strict-comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/strict-comparison.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StrictInArrayFavorite                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
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


