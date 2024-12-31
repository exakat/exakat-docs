.. _php-caseforpss:

.. _use-lower-case-for-parent,-static-and-self:

Use Lower Case For Parent, Static And Self
++++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Use Lower Case For Parent, Static And Self: The special parent, static and self keywords needed to be lowercase to be usable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Lower Case For Parent, Static And Self
	:twitter:description: Use Lower Case For Parent, Static And Self: The special parent, static and self keywords needed to be lowercase to be usable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Lower Case For Parent, Static And Self
	:og:type: article
	:og:description: The special parent, static and self keywords needed to be lowercase to be usable
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/CaseForPSS.html
	:og:locale: en
  The special `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ keywords needed to be lowercase to be usable. This was fixed in PHP 5.5; otherwise, they would yield a 'PHP Fatal error:  Class '`PARENT <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_' not found'.

`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ are traditionally written in lowercase only. Mixed case and Upper case are both valid, though.
Until PHP 5.5, non-lowercase version of those keywords are generating a bug.

.. code-block:: php
   
   <?php
   
   class foo {
       const aConstante = 233;
       
       function method() {
           // Wrong case, error with PHP 5.4.* and older
           echo SELF::aConstante;
           
           // Always right. 
           echo self::aConstante;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_


Suggestions
___________

* Upgrade to PHP 5.6 or more recent




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CaseForPSS                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and older                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


