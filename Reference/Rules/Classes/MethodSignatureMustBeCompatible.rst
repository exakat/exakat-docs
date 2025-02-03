.. _classes-methodsignaturemustbecompatible:

.. _method-signature-must-be-compatible:

Method Signature Must Be Compatible
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Method Signature Must Be Compatible: Make sure methods signature are compatible.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Signature Must Be Compatible
	:twitter:description: Method Signature Must Be Compatible: Make sure methods signature are compatible
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Signature Must Be Compatible
	:og:type: article
	:og:description: Make sure methods signature are compatible
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Signature Must Be Compatible.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MethodSignatureMustBeCompatible.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MethodSignatureMustBeCompatible.html","name":"Method Signature Must Be Compatible","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Make sure methods signature are compatible","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Signature Must Be Compatible.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Make sure methods signature are compatible.

PHP generates the infamous Fatal `error <https://www.php.net/error>`_ at execution : ``Declaration of FooParent\:\:Bar() must be compatible with FooChildren\:\:Bar()``

.. code-block:: php
   
   <?php
   
   class x {
       function xa() {}
   }
   
   class xxx extends xx {
       function xa($a) {}
   }
   
   ?>
Related PHP errors 
-------------------

  + `Declaration of %s::%s($%s) should be compatible with %s::%s($%s = 1)  <https://php-errors.readthedocs.io/en/latest/messages/declaration-of-%25s-must-be-compatible-with-%25s.html>`_



Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `type-covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-covariance.ini.html>`_
  + `type-contravariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-contravariance.ini.html>`_


Suggestions
___________

* Fix the child class method() signature.
* Fix the parent class method() signature, after checking that it won't affect the other children.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodSignatureMustBeCompatible                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


