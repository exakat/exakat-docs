.. _structures-overwrittenforeachvar:


.. _overwritten-foreach-var:

Overwritten Foreach Var
+++++++++++++++++++++++

.. meta::
	:description:
		Overwritten Foreach Var: When using standard blind variable names, nested foreach may lead to overwriting the variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Foreach Var
	:twitter:description: Overwritten Foreach Var: When using standard blind variable names, nested foreach may lead to overwriting the variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Foreach Var
	:og:type: article
	:og:description: When using standard blind variable names, nested foreach may lead to overwriting the variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Foreach Var.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OverwrittenForeachVar.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OverwrittenForeachVar.html","name":"Overwritten Foreach Var","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using standard blind variable names, nested foreach may lead to overwriting the variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overwritten Foreach Var.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using standard blind variable names, nested foreach may lead to overwriting the variables.

Careful coding may take advantage of that feature. Though, it tends to be `error <https://www.php.net/error>`_ prone, and will generate bugs if the code is refactored.

.. code-block:: php
   
   <?php
   
   foreach($array as $key => $value) {
       foreach($array as $key2 => $value) {
           // $value is now the one of the 2nd foreach, not the first.
           
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Change the name of one of the blind variable to use a distinct name
* Remove usage of one of the double variable
* Remove the nested foreach()
* Move the nested foreach() to a method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OverwrittenForeachVar                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


