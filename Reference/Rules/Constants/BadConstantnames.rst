.. _constants-badconstantnames:


.. _bad-constants-names:

Bad Constants Names
+++++++++++++++++++

.. meta::
	:description:
		Bad Constants Names: PHP's manual recommends that developer do not use constants with the convention ``__NAME__``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Bad Constants Names
	:twitter:description: Bad Constants Names: PHP's manual recommends that developer do not use constants with the convention ``__NAME__``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Bad Constants Names
	:og:type: article
	:og:description: PHP's manual recommends that developer do not use constants with the convention ``__NAME__``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Bad Constants Names.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/BadConstantnames.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/BadConstantnames.html","name":"Bad Constants Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"PHP's manual recommends that developer do not use constants with the convention ``__NAME__``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Bad Constants Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP's manual recommends that developer do not use constants with the convention ``__NAME__``. Those are reserved for PHP future use. 

For example, ``__TRAIT__`` recently appeared in PHP, as a magic constant. In the future, other may appear. 

The analyzer reports any constant which name is ``__.*.__``, or even ``_.*_`` (only one underscore).

.. code-block:: php
   
   <?php
   
   const __MY_APP_CONST__ = 1;
   
   const __MY_APP_CONST__ = 1;
   
   define('__MY_OTHER_APP_CONST__', 2);
   
   ?>

See also `Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Avoid using names that doesn't comply with PHP's convention




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/BadConstantnames                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-constants-badconstantnames`, :ref:`case-zencart-constants-badconstantnames`                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


