.. _attributes-mustusereturnreturns:


.. _must-use-result,-so-it-returns:

Must Use Result, So It Returns
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Must Use Result, So It Returns: A method or function that uses the #[MustUseResult] attribute, must return a value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Must Use Result, So It Returns
	:twitter:description: Must Use Result, So It Returns: A method or function that uses the #[MustUseResult] attribute, must return a value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Must Use Result, So It Returns
	:og:type: article
	:og:description: A method or function that uses the #[MustUseResult] attribute, must return a value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Must Use Result, So It Returns.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MustUseReturnReturns.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MustUseReturnReturns.html","name":"Must Use Result, So It Returns","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 13 Jan 2025 10:53:43 +0000","dateModified":"Mon, 13 Jan 2025 10:53:43 +0000","description":"A method or function that uses the #[MustUseResult] attribute, must return a value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Must Use Result, So It Returns.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method or function that uses the #[MustUseResult] `attribute <https://www.php.net/attribute>`_, must return a value. 

Hence, it cannot use the ``void`` and ``never`` returntypes, and it must use a ``return`` in the body of the method.

See also https://github.com/DaveLiddament/php-language-extensions?tab=readme-ov-file#mustuseresult.

Connex PHP features
-------------------

  + `Attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_
  + `Never Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/never.ini.html>`_
  + `Void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_
  + `Return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_
  + `Return Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/returntype.ini.html>`_


Suggestions
___________

* Add a type and return to the method.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/MustUseReturnReturns                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`mustuseresult`                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


