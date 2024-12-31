.. _extensions-extds:

.. _ext-ds:

ext/ds
++++++

.. meta\:\:
	:description:
		ext/ds: Extension Data Structures : `Data structures <http://docs.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ds
	:twitter:description: ext/ds: Extension Data Structures : `Data structures <http://docs
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ds
	:og:type: article
	:og:description: Extension Data Structures : `Data structures <http://docs
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extds.html
	:og:locale: en
  Extension Data Structures : `Data structures <http://docs.php.net/manual/en/book.ds.php>`_.

.. code-block:: php
   
   <?php
   
   $vector = new \Ds\Vector();
   
   $vector->push('a');
   $vector->push('b', 'c');
   
   $vector[] = 'd';
   
   print_r($vector);
   
   ?>

See also `Efficient data structures for PHP 7 <https://medium.com/@rtheunissen/efficient-data-structures-for-php-7-9dda7af674cd#.x69w9j6ui>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extds                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.4                                                                                                                                                                                  |
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


