.. _structures-couldusearrayunique:


.. _could-use-array\_unique:

Could Use array_unique
++++++++++++++++++++++


.. meta::

	:description:

		Could Use array_unique: Use array_unique() to collect unique elements from an array.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Could Use array_unique

	:twitter:description: Could Use array_unique: Use array_unique() to collect unique elements from an array

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Could Use array_unique

	:og:type: article

	:og:description: Use array_unique() to collect unique elements from an array

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use array_unique.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseArrayUnique.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseArrayUnique.html","name":"Could Use array_unique","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use array_unique() to collect unique elements from an array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use array_unique.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use `array_unique() <https://www.php.net/array_unique>`_ to collect unique elements from an array.

Always try to use native PHP functions, instead of rebuilding them with custom PHP code.

.. code-block:: php
   
   <?php
   
       $unique = array();
       foreach ($array as $b) {
           if (!in_array($b, $unique)) {
               /*  May be more code */
               $unique[] = $b;
           }
       }
   ?>

See also `array_unique <https://www.php.net/array_unique>`_.


Suggestions
___________

* Turn the foreach() and its condition into a call to array_unique()
* Extract the condition from the foreach() and add a separate call to array_unique()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseArrayUnique                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-couldusearrayunique`, :ref:`case-openemr-structures-couldusearrayunique`                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


