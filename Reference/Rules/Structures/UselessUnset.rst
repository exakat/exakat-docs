.. _structures-uselessunset:


.. _useless-unset:

Useless Unset
+++++++++++++

.. meta::
	:description:
		Useless Unset: There are situations where trying to remove a variable is actually useless.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Unset
	:twitter:description: Useless Unset: There are situations where trying to remove a variable is actually useless
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Unset
	:og:type: article
	:og:description: There are situations where trying to remove a variable is actually useless
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Unset.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessUnset.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessUnset.html","name":"Useless Unset","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There are situations where trying to remove a variable is actually useless","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Unset.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There are situations where trying to remove a variable is actually useless. 

PHP ignores any command that tries to unset a global variable, a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable, or a blind variable from a foreach loop. 

This is different from the garbage collector, which is run on its own schedule. It is also different from an explicit unset, aimed at freeing memory early : those are useful.

.. code-block:: php
   
   <?php
   
   function foo($a) {
       // unsetting arguments is useless
       unset($a);
       
       global $b;
       // unsetting global variable has no effect 
       unset($b);
   
       static $c;
       // unsetting static variable has no effect 
       unset($c);
       
       foreach($d as &$e){
           // unsetting a blind variable is useless
           (unset) $e;
       }
       // Unsetting a blind variable AFTER the loop is good.
       unset($e);
   }
   
   ?>

See also `unset <https://www.php.net/unset>`_.

Connex PHP features
-------------------

  + `unset() <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Remove the unset
* Set the variable to null : the effect is the same on memory, but the variable keeps its existence.
* Omit unsetting variables, and wait for the end of the scope. That way, PHP free memory en mass.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessUnset                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-unset <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-unset.md>`__                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-structures-uselessunset`, :ref:`case-typo3-structures-uselessunset`                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


