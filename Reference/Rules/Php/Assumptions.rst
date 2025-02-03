.. _php-assumptions:


.. _assumptions:

Assumptions
+++++++++++


.. meta::

	:description:

		Assumptions: Assumptions in the code, that leads to possible bugs.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Assumptions

	:twitter:description: Assumptions: Assumptions in the code, that leads to possible bugs

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Assumptions

	:og:type: article

	:og:description: Assumptions in the code, that leads to possible bugs

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Assumptions.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Assumptions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Assumptions.html","name":"Assumptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Assumptions in the code, that leads to possible bugs","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Assumptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Assumptions in the code, that leads to possible bugs. 

Some conditions may be very weak, and lead to errors. For example, the code below checks that the variable `$a` is not null, then uses it as an array. There is no relationship between 'not null' and 'being an array', so this is an assumption.

.. code-block:: php
   
   <?php
   
   // Assumption : if $a is not null, then it is an array. This is not always the case. 
   function foo($a) {
       if ($a !== null) {
           echo $a['name'];
       }
   }
   
   // Assumption : if $a is not null, then it is an array. Here, the typehint will ensure that it is the case. 
   // Although, a more readable test is is_array()
   function foo(?array $a) {
       if ($a !== null) {
           echo $a['name'];
       }
   }
   
   ?>

See also `From assumptions to assertions <https://rskuipers.com/entry/from-assumptions-to-assertions>`_.

Connex PHP features
-------------------

  + `assumption <https://php-dictionary.readthedocs.io/en/latest/dictionary/assumption.ini.html>`_


Suggestions
___________

* Make the context of the code more explicit
* Use a class to handle specific array index
* Avoid using named index by using foreach()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Assumptions                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


