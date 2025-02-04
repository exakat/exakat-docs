.. _arrays-masscreation:


.. _mass-creation-of-arrays:

Mass Creation Of Arrays
+++++++++++++++++++++++

.. meta::
	:description:
		Mass Creation Of Arrays: This rule reports literal creation of arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mass Creation Of Arrays
	:twitter:description: Mass Creation Of Arrays: This rule reports literal creation of arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mass Creation Of Arrays
	:og:type: article
	:og:description: This rule reports literal creation of arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mass Creation Of Arrays.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/MassCreation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/MassCreation.html","name":"Mass Creation Of Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"This rule reports literal creation of arrays","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mass Creation Of Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports literal creation of arrays. This happens by assigning several indices in a row.

It is recommended to federate all index assignations in one ``array()`` or ``[]`` call, rather than multiple successive instructions.

This applies to all constant and simple variable assignation. Anything more complex could still be done, afterward. That way, it reduces partially the load of the easy assignations.

.. code-block:: php
   
   <?php
       
   $row['name'] = $name;
   $row['last'] = $last;
   $row['address'] = $address;
   if (!isset($zipCode)) {
       $row['zipCode'] = $zipCode;
   }
   
   $row = [
       'name' => $name,
       'last' => $last,
       'address' => $address,
   ];
   if (!isset($zipCode)) {
       $row['zipCode'] = $zipCode;
   }
   
   ?>
Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `compact() <https://php-dictionary.readthedocs.io/en/latest/dictionary/compact.ini.html>`_
  + `Index For Arrays <https://php-dictionary.readthedocs.io/en/latest/dictionary/index-array.ini.html>`_


Suggestions
___________

* Use ``compact()`` to collect variables to one array.
* Replace assignations with one ``[]`` call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/MassCreation                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


