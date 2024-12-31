.. _arrays-mistakenconcatenation:

.. _mistaken-concatenation:

Mistaken Concatenation
++++++++++++++++++++++

.. meta\:\:
	:description:
		Mistaken Concatenation: A unexpected structure is built for initialization.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mistaken Concatenation
	:twitter:description: Mistaken Concatenation: A unexpected structure is built for initialization
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mistaken Concatenation
	:og:type: article
	:og:description: A unexpected structure is built for initialization
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/MistakenConcatenation.html
	:og:locale: en
  A unexpected structure is built for initialization. It may be a typo that creates an unwanted expression.

.. code-block:: php
   
   <?php
   
   // This 'cd' is unexpected. Isn't it 'c', 'd' ? 
   $array = array('a', 'b', 'c'. 'd');
   $array = array('a', 'b', 'c', 'd');
   
   // This 4.5 is unexpected. Isn't it 4, 5 ? 
   $array = array(1, 2, 3, 4.5);
   $array = array(1, 2, 3, 4, 5);
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `concatenation <https://php-dictionary.readthedocs.io/en/latest/dictionary/concatenation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/MistakenConcatenation                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


