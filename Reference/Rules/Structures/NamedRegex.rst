.. _structures-namedregex:


.. _named-regex:

Named Regex
+++++++++++

.. meta::
	:description:
		Named Regex: Captured subpatterns may be named, for easier reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Named Regex
	:twitter:description: Named Regex: Captured subpatterns may be named, for easier reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Named Regex
	:og:type: article
	:og:description: Captured subpatterns may be named, for easier reference
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Named Regex.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NamedRegex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NamedRegex.html","name":"Named Regex","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Captured subpatterns may be named, for easier reference","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Named Regex.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Captured subpatterns may be named, for easier reference. 

From the manual : It is possible to name a subpattern using the syntax ``(?P<name>pattern)``. This subpattern will then be indexed in the matches array by its normal numeric position and also by name. PHP 5.2.2 introduced two alternative syntaxes ``(?<name>pattern)`` and ``(?'name'pattern)``.

Naming subpatterns makes it easier to know what is read from the results of the subpattern : for example, ``$r['name']`` has more meaning than ``$r[1]``. 

Named subpatterns may also be shifted in the regex without impact on the resulting array.

.. code-block:: php
   
   <?php
   
   $x = 'abc';
   preg_match_all('/(?<name>a)/', $x, $r);
   print_r($r[1]);
   print_r($r['name']);
   
   preg_match("/(?<name>a)(?'sub'b)/", $x, $s);
   print $s[2];
   print $s['sub'];
   
   ?>

See also `Subpatterns <https://www.php.net/manual/en/regexp.reference.subpatterns.php>`_.

Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Use named regex, and stop using integer-named subpatterns




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NamedRegex                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-structures-namedregex`, :ref:`case-shopware-structures-namedregex`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


