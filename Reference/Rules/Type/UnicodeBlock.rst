.. _type-unicodeblock:

.. _unicode-blocks:

Unicode Blocks
++++++++++++++

  List of the Unicode blocks used in string literals.

This is the kind of characters that can be found in the applications strings.
Note that Exakat only analyze PHP scripts : any translation available in a ``.po`` or external resource is not parsed and will not show.

.. code-block:: php
   
   <?php
   
   $a = "zoo"; 
   
   $b = "ఒ"; // Telugu character
   $b = "\u{0C12}"; Same as above
   
   $b = "人"; // Chinese Mandarin character
   $b = "\u{4EBA}"; Same as above
   
   ?>

See also `Unicode block <https://en.wikipedia.org/wiki/Unicode_block>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/UnicodeBlock                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Inventory <ruleset-Inventory>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


