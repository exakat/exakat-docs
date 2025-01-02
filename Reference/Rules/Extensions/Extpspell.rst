.. _extensions-extpspell:

.. _ext-pspell:

ext/pspell
++++++++++

.. meta::
	:description:
		ext/pspell: Extension pspell.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pspell
	:twitter:description: ext/pspell: Extension pspell
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pspell
	:og:type: article
	:og:description: Extension pspell
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/pspell.html
	:og:locale: en
Extension pspell.

These functions allow you to check the spelling of a word and offer suggestions.

.. code-block:: php
   
   <?php
   $pspell_link = pspell_new('en');
   
   if (pspell_check($pspell_link, 'testt')) {
       echo 'This is a valid spelling';
   } else {
       echo 'Sorry, wrong spelling';
   }
   ?>

See also `Pspell <https://www.php.net/manual/en/book.pspell.php>`_ and `pspell <https://en.wikipedia.org/wiki/Pspell>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpspell                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


