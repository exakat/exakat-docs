.. _extensions-extctype:

.. _ext-ctype:

ext/ctype
+++++++++

.. meta\:\:
	:description:
		ext/ctype: Extension ext/ctype.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ctype
	:twitter:description: ext/ctype: Extension ext/ctype
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ctype
	:og:type: article
	:og:description: Extension ext/ctype
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extctype.html
	:og:locale: en
  Extension ext/`ctype <https://www.php.net/ctype>`_.

Ext/`ctype <https://www.php.net/ctype>`_ checks whether a character or string falls into a certain character class according to the current `locale <https://www.php.net/locale>`_.

.. code-block:: php
   
   <?php
   $strings = array('AbCd1zyZ9', 'foo!#$bar');
   foreach ($strings as $testcase) {
       if (ctype_alnum($testcase)) {
           echo "The string $testcase consists of all letters or digits.\n";
       } else {
           echo "The string $testcase does not consist of all letters or digits.\n";
       }
   }
   ?>

See also `Ctype functions <https://www.php.net/manual/en/ref.ctype.php>`_.

Connex PHP features
-------------------

  + `ctype <https://php-dictionary.readthedocs.io/en/latest/dictionary/ctype.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extctype                                                                                                                                                                     |
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


