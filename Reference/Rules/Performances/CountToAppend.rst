.. _performances-counttoappend:


.. _count()-to-array-append:

Count() To Array Append
+++++++++++++++++++++++


.. meta::

	:description:

		Count() To Array Append: The array append operator is able to generate a sane index, without relying on the count() function.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Count() To Array Append

	:twitter:description: Count() To Array Append: The array append operator is able to generate a sane index, without relying on the count() function

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Count() To Array Append

	:og:type: article

	:og:description: The array append operator is able to generate a sane index, without relying on the count() function

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Count() To Array Append.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CountToAppend.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CountToAppend.html","name":"Count() To Array Append","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The array append operator is able to generate a sane index, without relying on the count() function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Count() To Array Append.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The array append operator is able to generate a sane index, without relying on the `count() <https://www.php.net/count>`_ function. This is faster, and safer.

.. code-block:: php
   
   <?php
   
   $newArray  = [];
   foreach($array as $value) {
   	// count is overkill here
   	$newArray[count($newArray)] = $value;
   }
   
   ?>
Connex PHP features
-------------------

  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Suggestions
___________

* Remove the call to count()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/CountToAppend                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


