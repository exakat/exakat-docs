.. _arrays-nonconstantarray:

.. _non-constant-index-in-array:

Non-constant Index In Array
+++++++++++++++++++++++++++

.. meta::
	:description:
		Non-constant Index In Array: Undefined constants revert as strings in Arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Non-constant Index In Array
	:twitter:description: Non-constant Index In Array: Undefined constants revert as strings in Arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Non-constant Index In Array
	:og:type: article
	:og:description: Undefined constants revert as strings in Arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Non-constant Index In Array.html
	:og:locale: en
Undefined constants revert as strings in Arrays. They are also called ``barewords``.

In ``$array[index]``, PHP cannot find index as a constant, but, as a default behavior, turns it into the string ``index``. 

This default behavior raise concerns when a corresponding constant is defined, either using `define() <https://www.php.net/define>`_ or the const keyword (outside a class). The definition of the index constant will modify the behavior of the index, as it will now use the constant definition, and not the 'index' string. 

It is recommended to make index a real string (with ' or "), or to define the corresponding constant to avoid any future surprise.

Note that PHP 7.2 removes the support for this feature.

.. code-block:: php
   
   <?php
   
   // assign 1 to the element index in $array
   // index will fallback to string
   $array[index] = 1; 
   //PHP Notice:  Use of undefined constant index - assumed 'index'
   
   echo $array[index];      // display 1 and the above error
   echo "$array[index]";    // display 1
   echo "$array['index']";  // Syntax error
   
   define('index', 2);
    
   // now 1 to the element 2 in $array
   $array[index] = 1;
   
   ?>

See also `PHP RFC: Deprecate and Remove Bareword (Unquoted) Strings <https://wiki.php.net/rfc/deprecate-bareword-strings>`_ and `Syntax <https://www.php.net/manual/en/language.constants.syntax.php>`_.

Related PHP errors 
-------------------

  + `Undefined constant <https://php-errors.readthedocs.io/en/latest/messages/undefined-constant-%22%25s.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Declare the constant to give it an actual value
* Turn the constant name into a string




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/NonConstantArray                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-arrays-nonconstantarray`, :ref:`case-zencart-arrays-nonconstantarray`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


