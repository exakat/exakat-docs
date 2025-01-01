.. _php-closetagsconsistency:

.. _close-tags-consistency:

Close Tags Consistency
++++++++++++++++++++++

.. meta::
	:description:
		Close Tags Consistency: PHP scripts may omit the final closing tag.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Close Tags Consistency
	:twitter:description: Close Tags Consistency: PHP scripts may omit the final closing tag
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Close Tags Consistency
	:og:type: article
	:og:description: PHP scripts may omit the final closing tag
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/CloseTagsConsistency.html
	:og:locale: en
PHP scripts may omit the final closing tag. 

This is a convention, used to avoid the infamous 'headers already sent' `error <https://www.php.net/error>`_ message, that appears when a script with extra invisible spaces is included before actually emitting the headers.

The PHP manual recommends : "If a file is pure PHP code, it is preferable to omit the PHP closing tag at the end of the file.". (See `PHP Tags <https://www.php.net/manual/en/language.basic-syntax.phptags.php>`_)::

   
   
   .. code-block:: php
      
      <?php
      
      class foo {
      
      }
Connex PHP features
-------------------

  + `close-tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/close-tag.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CloseTagsConsistency                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


