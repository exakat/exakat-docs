.. _structures-listomissions:

.. _list()-may-omit-variables:

list() May Omit Variables
+++++++++++++++++++++++++

.. meta::
	:description:
		list() May Omit Variables: Simply omit any unused variable in a list() call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: list() May Omit Variables
	:twitter:description: list() May Omit Variables: Simply omit any unused variable in a list() call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: list() May Omit Variables
	:og:type: article
	:og:description: Simply omit any unused variable in a list() call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/list() May Omit Variables.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ListOmissions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ListOmissions.html","name":"list() May Omit Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Simply omit any unused variable in a list() call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/list() May Omit Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Simply omit any unused variable in a `list() <https://www.php.net/list>`_ call. 

`list() <https://www.php.net/list>`_ is the only PHP function that accepts to have omitted arguments. If the following code makes no usage of a listed variable, just omit it.

.. code-block:: php
   
   <?php
       // No need for '2', so no assignation
       list ($a, , $b) = array(1, 2, 3);
       
       // works with PHP 7.1 short syntax
       [$a, , $b] = array(1, 2, 3);
   
       // No need for '2', so no assignation
       list ($a, $c, $b) = array(1, 2, 3);
   ?>

See also `list <https://www.php.net/manual/en/function.list.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Remove the unused variables from the list call
* When the ignored values are at the beginning or the end of the array, array_slice() may be used to shorten the array.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ListOmissions                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Suggestions <ruleset-Suggestions>`                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-structures-listomissions`, :ref:`case-fuelcms-structures-listomissions`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


