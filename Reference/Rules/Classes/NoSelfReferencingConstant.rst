.. _classes-noselfreferencingconstant:


.. _no-self-referencing-constant:

No Self Referencing Constant
++++++++++++++++++++++++++++

.. meta::
	:description:
		No Self Referencing Constant: It is not possible to use a constant to define itself in a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Self Referencing Constant
	:twitter:description: No Self Referencing Constant: It is not possible to use a constant to define itself in a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Self Referencing Constant
	:og:type: article
	:og:description: It is not possible to use a constant to define itself in a class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Self Referencing Constant.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoSelfReferencingConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoSelfReferencingConstant.html","name":"No Self Referencing Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"It is not possible to use a constant to define itself in a class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Self Referencing Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to use a constant to define itself in a class. It yields a fatal `error <https://www.php.net/error>`_ at runtime. 

The PHP `error <https://www.php.net/error>`_ reads : ``Cannot declare `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-referencing constant 'self\:\:C2'``. Unlike PHP which is `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-referencing, `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ referencing variables can't have a value : just don't use that.
The code may access an already declared constant with `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or with its class name.
This `error <https://www.php.net/error>`_ is not detected by linting. It is only detected at instantiation time : if the class is not used, it won't appear.

.. code-block:: php
   
   <?php
       class a { 
           const C1 = 1;         // fully defined constant
           const C2 = self::C2;  // self referencing constant
           const C3 = a::C3 + 2; // self referencing constant
       }
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Give a literal value to this constant
* Give a constant value to this constant : other class constants or constant are allowed here.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoSelfReferencingConstant                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


