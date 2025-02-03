.. _typehints-wrongtypewithdefault:


.. _wrong-type-with-default:

Wrong Type With Default
+++++++++++++++++++++++


.. meta::

	:description:

		Wrong Type With Default: The default value is not of the declared type.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Wrong Type With Default

	:twitter:description: Wrong Type With Default: The default value is not of the declared type

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Wrong Type With Default

	:og:type: article

	:og:description: The default value is not of the declared type

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Type With Default.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/WrongTypeWithDefault.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/WrongTypeWithDefault.html","name":"Wrong Type With Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The default value is not of the declared type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Type With Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The default value is not of the declared type. 

For properties, this will generate an `error <https://www.php.net/error>`_ as soon as the default value is used : this is before constructor call for properties, and when the argument is omitted for promoted properties.

For parameters, the `error <https://www.php.net/error>`_ happens when the argument is omitted, and the default value is fetched. Otherwise, it won't happen. 
This `error <https://www.php.net/error>`_ is immediately detected when a literal value is used. It only happens when the default is a constant (class or global) or an expression, as those are only solved at execution time.

.. code-block:: php
   
   <?php
   
   const A = 1;
   
   class B {
       private string $c = A;
   }
   
   new B;
   //Cannot assign string to property B::$c of type string
   ?>

See also `When does PHP check for Fatal error <https://www.exakat.io/en/when-does-php-check-for-fatal-error/>`_.

Related PHP errors 
-------------------

  + `Cannot assign %s to property %s::$%s of type %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-assign-%25s-to-property-%25s%3A%3A%24%25s-of-type-%25s.html>`_




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/WrongTypeWithDefault                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


