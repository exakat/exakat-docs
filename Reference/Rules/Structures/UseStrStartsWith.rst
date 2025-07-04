.. _structures-usestrstartswith:


.. _use-str\_starts\_with():

Use str_starts_with()
+++++++++++++++++++++

.. meta::
	:description:
		Use str_starts_with(): There is a dedicated function to check the prefix of a string : it is called str_starts_with().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use str_starts_with()
	:twitter:description: Use str_starts_with(): There is a dedicated function to check the prefix of a string : it is called str_starts_with()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use str_starts_with()
	:og:type: article
	:og:description: There is a dedicated function to check the prefix of a string : it is called str_starts_with()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use str_starts_with().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseStrStartsWith.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseStrStartsWith.html","name":"Use str_starts_with()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There is a dedicated function to check the prefix of a string : it is called str_starts_with()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use str_starts_with().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There is a dedicated function to check the prefix of a string : it is called `str_starts_with() <https://www.php.net/str_starts_with>`_. It is available since PHP 8.0

.. code-block:: php
   
   <?php
   
   if (str_starts_with($a, 'abc')) { }
   
   // Before PHP 8.2
   if (substr($a, 0, 3) === 'abc') { }
   
   ?>

See also `str_ends_with() <https://www.php.net/str_ends_with>`_.


Suggestions
___________

* Use the native PHP function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseStrStartsWith                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


