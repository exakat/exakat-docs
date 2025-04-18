.. _classes-noparent:


.. _class-without-parent:

Class Without Parent
++++++++++++++++++++

.. meta::
	:description:
		Class Without Parent: Classes should not refer to ``parent`` when it is not extending another class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Without Parent
	:twitter:description: Class Without Parent: Classes should not refer to ``parent`` when it is not extending another class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Without Parent
	:og:type: article
	:og:description: Classes should not refer to ``parent`` when it is not extending another class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Without Parent.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoParent.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoParent.html","name":"Class Without Parent","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Classes should not refer to ``parent`` when it is not extending another class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Without Parent.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Classes should not refer to ``parent`` when it is not extending another class. 

In PHP 7.4, it is a Deprecated warning. In PHP 7.3, it was a Fatal `error <https://www.php.net/error>`_, when the code was eventually executed. In PHP 8.0, PHP detects this `error <https://www.php.net/error>`_ at compile time, except for `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ keyword in a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_.

``parent`` usage in trait is detected. It is only reported when the trait is used inside a class without `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, as the trait may also be used in another class, which has a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           parent::foo();
       }
   }
   ?>
Related PHP errors 
-------------------

  + `Cannot use ""parent"" when current class scope has no parent <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-parent%3A%3A-when-current-class-scope-has-no-parent.html>`_
  + `Cannot access parent:: when current class scope has no parent <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-parent%3A%3A-when-no-class-scope-is-active.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Update the class and make it extends another class
* Change the parent mention with a fully qualified name
* Remove the call to the parent altogether




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/NoParent                                                                                                                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.9.0                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/orphanedParent.html>`__                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


