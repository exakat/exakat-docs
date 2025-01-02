.. _php-mustcallparentconstructor:

.. _must-call-parent-constructor:

Must Call Parent Constructor
++++++++++++++++++++++++++++

.. meta::
	:description:
		Must Call Parent Constructor: Some PHP native classes require a call to ``parent::__construct()`` to be stable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Must Call Parent Constructor
	:twitter:description: Must Call Parent Constructor: Some PHP native classes require a call to ``parent::__construct()`` to be stable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Must Call Parent Constructor
	:og:type: article
	:og:description: Some PHP native classes require a call to ``parent::__construct()`` to be stable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Must Call Parent Constructor.html
	:og:locale: en
Some PHP native classes require a call to ``parent\:\:`__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_`` to be stable. 

As of PHP 7.3, two classes currently need that call : ``SplTempFileObject`` and ``SplFileObject``.

The `error <https://www.php.net/error>`_ is only emitted if the class is instantiated, and a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class is called.

.. code-block:: php
   
   <?php
   
   class mySplFileObject extends \SplFileObject {
       public function __construct()    { 
           // Forgottent call to parent::__construct()
       }
   }
   
   (new mySplFileObject())->passthru();
   ?>

See also `Why, php? WHY??? <https://gist.github.com/everzet/4215537>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/The+parent+constructor+was+not+called%3A+the+object+is+in+an+invalid+state.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Add a call to the parent's constructor
* Remove the extension of the parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MustCallParentConstructor                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


