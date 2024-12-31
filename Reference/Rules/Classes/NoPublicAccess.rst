.. _classes-nopublicaccess:

.. _no-public-access:

No Public Access
++++++++++++++++

.. meta\:\:
	:description:
		No Public Access: The properties below are declared with public access, but are never used publicly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Public Access
	:twitter:description: No Public Access: The properties below are declared with public access, but are never used publicly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Public Access
	:og:type: article
	:og:description: The properties below are declared with public access, but are never used publicly
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/NoPublicAccess.html
	:og:locale: en
  The properties below are declared with public access, but are never used publicly. They can be made protected or private.

.. code-block:: php
   
   <?php
   
   class foo {
       public $bar = 1;            // Public, and used in public space
       public $neverInPublic = 3;  // Public, but never used in outside the class
       
       function bar() {
           $neverInPublic++;
       }
   }
   
   $x = new foo();
   $x->bar = 3;
   $x->bar();
   
   ?>
Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoPublicAccess                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


