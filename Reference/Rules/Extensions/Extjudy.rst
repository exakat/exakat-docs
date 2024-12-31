.. _extensions-extjudy:

.. _ext-judy:

ext/judy
++++++++

.. meta\:\:
	:description:
		ext/judy: The Judy extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/judy
	:twitter:description: ext/judy: The Judy extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/judy
	:og:type: article
	:og:description: The Judy extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extjudy.html
	:og:locale: en
  The `Judy <https://www.php.net/Judy>`_ extension. 

PHP `Judy <https://www.php.net/Judy>`_ is a PECL extension for the `Judy C library <http://judy.sourceforge.net/>`_ implementing dynamic sparse arrays.

.. code-block:: php
   
   <?php 
   $judy = new Judy(Judy::BITSET);
   if ($judy->getType() === judy_type($judy) &&
       $judy->getType() === Judy::BITSET) {
       echo 'Judy BITSET type OK'.PHP_EOL;
   } else {
       echo 'Judy BITSET type check fail'.PHP_EOL;
   }
   unset($judy);
   ?>

See also `php-judy <https://github.com/orieg/php-judy>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extjudy                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
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


