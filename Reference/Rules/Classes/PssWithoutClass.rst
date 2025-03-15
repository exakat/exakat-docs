.. _classes-psswithoutclass:


.. _parent,-static-or-self-outside-class:

Parent, Static Or Self Outside Class
++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Parent, Static Or Self Outside Class: Parent, static and self keywords must be used within a class, a trait, an interface or an enum.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Parent, Static Or Self Outside Class
	:twitter:description: Parent, Static Or Self Outside Class: Parent, static and self keywords must be used within a class, a trait, an interface or an enum
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Parent, Static Or Self Outside Class
	:og:type: article
	:og:description: Parent, static and self keywords must be used within a class, a trait, an interface or an enum
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Parent, Static Or Self Outside Class.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PssWithoutClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PssWithoutClass.html","name":"Parent, Static Or Self Outside Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Parent, static and self keywords must be used within a class, a trait, an interface or an enum","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Parent, Static Or Self Outside Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ keywords must be used within a class, a trait, an interface or an enum. They make no sense outside a class or trait scope, as `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ refers to the current class and `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ refers to one of `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ above.

PHP 7.0 and later detect some of their usage at compile time, and emits a fatal `error <https://www.php.net/error>`_.
`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ may be used in a function or a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, but not globally.

.. code-block:: php
   
   <?php
   
   class x {
       const Y = 1;
       
       function foo() {
           // self is \x
           echo self::Y;
       }
   }
   
   const Z = 1;
   // This lint but won't anymore
   echo self::Z;
   
   ?>
Related PHP errors 
-------------------

  + `Cannot access self:: when no class scope is active <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-self%3A%3A-when-no-class-scope-is-active.html>`_
  + `Cannot use "parent" when current class scope has no parent <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-parent%3A%3A-when-no-class-scope-is-active.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_
  + `Self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Make sure the keyword is inside a class context




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/PssWithoutClass                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


