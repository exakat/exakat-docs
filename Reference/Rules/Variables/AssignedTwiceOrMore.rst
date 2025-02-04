.. _variables-assignedtwiceormore:


.. _assigned-twice:

Assigned Twice
++++++++++++++

.. meta::
	:description:
		Assigned Twice: The same variable is assigned twice in the same function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Assigned Twice
	:twitter:description: Assigned Twice: The same variable is assigned twice in the same function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Assigned Twice
	:og:type: article
	:og:description: The same variable is assigned twice in the same function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Assigned Twice.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/AssignedTwiceOrMore.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/AssignedTwiceOrMore.html","name":"Assigned Twice","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The same variable is assigned twice in the same function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Assigned Twice.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The same variable is assigned twice in the same function.

While this is possible and quite common, it is also a good practice to avoid changing a value from one literal to another. It is far better to assign the new value to 

Incremental changes to a variables are not reported here.

.. code-block:: php
   
   <?php
   
   function foo() {
       // incremental changes of $a;
       $a = 'a';
       $a++;
       $a = uppercase($a);
       
       $b = 1;
       $c = bar($b);
       // B changed its purpose. Why not call it $d? 
       $b = array(1,2,3);
       
       // This is some forgotten debug
       $e = $config->getSomeList();
       $e = array('OneElement');
   }
   
   ?>
Connex PHP features
-------------------

  + `Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Remove the first assignation
* Remove the second assignation
* Change the name of the variable in one or both cases




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/AssignedTwiceOrMore                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.8                                                                                                                   |
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


