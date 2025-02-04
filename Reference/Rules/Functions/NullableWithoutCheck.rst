.. _functions-nullablewithoutcheck:


.. _nullable-without-check:

Nullable Without Check
++++++++++++++++++++++

.. meta::
	:description:
		Nullable Without Check: Nullable typed argument or properties should be checked before usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nullable Without Check
	:twitter:description: Nullable Without Check: Nullable typed argument or properties should be checked before usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nullable Without Check
	:og:type: article
	:og:description: Nullable typed argument or properties should be checked before usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nullable Without Check.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NullableWithoutCheck.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NullableWithoutCheck.html","name":"Nullable Without Check","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Nullable typed argument or properties should be checked before usage","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Nullable Without Check.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Nullable typed argument or properties should be checked before usage. When they are `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, they probably won't behave like the other type, and lead to an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // This will emit a fatal error when $a = null
   function foo(?A $a) {
       return $a->m();
   }
   
   // This is stable
   function foo(?A $a) {
       if ($a === null) {
           return 42;
       } else {
           return $a->m();
       }
   }
   
   ?>

See also `Null Return Types <https://afilina.com/learn/nulls/return-types>`_.

Connex PHP features
-------------------

  + `Null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_
  + `Return Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-typehint.ini.html>`_


Suggestions
___________

* Add a check on return value




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NullableWithoutCheck                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


