.. _php-avoidmbdectectencoding:

.. _avoid-mb\_dectect\_encoding():

Avoid mb_dectect_encoding()
+++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Avoid mb_dectect_encoding(): mb_dectect_encoding() is bad at guessing encoding.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid mb_dectect_encoding()
	:twitter:description: Avoid mb_dectect_encoding(): mb_dectect_encoding() is bad at guessing encoding
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid mb_dectect_encoding()
	:og:type: article
	:og:description: mb_dectect_encoding() is bad at guessing encoding
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AvoidMbDectectEncoding.html
	:og:locale: en
  mb_dectect_encoding() is bad at guessing encoding. 

For example, UTF-8 and ISO-8859-1 share some common characters : when a string is build with them it is impossible to differentiate the actual encoding.

.. code-block:: php
   
   <?php
   
   $encoding = mb_encoding_detect($_GET['name']);
   
   ?>

See also `mb_encoding_detect <https://php.net/mb-encoding-detect>`_, `PHP vs. The Developer: Encoding Character Sets <https://www.daganhenderson.com/blog/2013/07/php-encoding-character-sets>`_ and `DPC2019: Of representation and interpretation: A unified theory - Arnout Boks <https://youtu.be/K2zS6vbBb9A?t=1375>`_.

Connex PHP features
-------------------

  + `mbstring <https://php-dictionary.readthedocs.io/en/latest/dictionary/mbstring.ini.html>`_


Suggestions
___________

* Store and transmit the data format




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AvoidMbDectectEncoding                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


