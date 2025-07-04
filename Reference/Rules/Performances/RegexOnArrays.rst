.. _performances-regexonarrays:


.. _regex-on-arrays:

Regex On Arrays
+++++++++++++++

.. meta::
	:description:
		Regex On Arrays: Avoid using a loop with arrays of regex or values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Regex On Arrays
	:twitter:description: Regex On Arrays: Avoid using a loop with arrays of regex or values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Regex On Arrays
	:og:type: article
	:og:description: Avoid using a loop with arrays of regex or values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Regex On Arrays.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/RegexOnArrays.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/RegexOnArrays.html","name":"Regex On Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using a loop with arrays of regex or values","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Regex On Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using a loop with arrays of regex or values. There are several PHP function which work directly on arrays, and much faster.

`preg_grep() <https://www.php.net/preg_grep>`_ is able to extract all matching strings from an array, or non-matching strings. This usually saves a loop over the strings.

`preg_filter() <https://www.php.net/preg_filter>`_ is able to extract all strings from an array, matching at least one regex in an array. This usually saves a double loop over the strings and the regex. The trick here is to provide '$0' as replacement, leading `preg_filter() <https://www.php.net/preg_filter>`_ to replace the found string by itself.

Finally, `preg_replace_callback() <https://www.php.net/preg_replace_callback>`_ an `preg_replace_callback_array() <https://www.php.net/preg_replace_callback_array>`_ are also able to apply an array of regex to an array of strings, and then, apply callbacks to the found values.

.. code-block:: php
   
   <?php
   
   $regexs = ['/ab+c/', '/abd+/', '/abe+/'];
   $strings = ['/abbbbc/', '/abd/', '/abeee/'];
   
   // Directly extract all strings that match one regex
   foreach($regexs as $regex) {
       $results[] = preg_grep($regex, $strings);
   }
   
   // extract all matching regex, by string
   foreach($strings as $string) {
       $results[] = preg_filter($regexs, array_fill(0, count($regexs), '$0'), $string);
   }
   
   // very slow way to get all the strings that match a regex
   foreach($regexs as $regex) {
       foreach($strings as $string) {
           if (preg_match($regex, $string)) {
               $results[] = $string;
           }
       }
   }
   
   ?>

See also `preg_filter <https://php.net/preg_filter>`_.

Connex PHP features
-------------------

  + `Regular Expressions <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Apply preg_match() to an array of string or regex, via preg_filter() or preg_grep().
* Apply preg_match() to an array of string or regex, via preg_replace_callback() or preg_replace_callback_array().




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/RegexOnArrays                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


