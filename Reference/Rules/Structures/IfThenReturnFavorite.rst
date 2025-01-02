.. _structures-ifthenreturnfavorite:

.. _if-then-return-favorite:

If Then Return Favorite
+++++++++++++++++++++++

.. meta::
	:description:
		If Then Return Favorite: Show of hands: which syntax would you prefer in a PHP function - A, B or C.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: If Then Return Favorite
	:twitter:description: If Then Return Favorite: Show of hands: which syntax would you prefer in a PHP function - A, B or C
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: If Then Return Favorite
	:og:type: article
	:og:description: Show of hands: which syntax would you prefer in a PHP function - A, B or C
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/If Then Return Favorite.html
	:og:locale: en
Show of hands: which syntax would you prefer in a PHP function - A, B or C?  
Based on a tweet from `Povilas Korop <https://twitter.com/PovilasKorop>`_ : `Show of hands: which syntax would you prefer in a PHP function - A, B or C?  <https://twitter.com/exakat/status/1542585298562998274>`_

.. code-block:: php
   
   <?php
   
   // Format A : double return
   if ($condition) {
       return A;
   } else {
       return B;
   }
   
   // Format B : early bailout
   if ($condition) {
       return A;
   } 
   return B;
   
   // Format C : ternary
   return  $condition ? A : B;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IfThenReturnFavorite                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
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


