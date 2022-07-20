.. _Cobblers:

Cobblers
=================

Introduction
--------------------------
Cobblers mend PHP code. They apply a transformation to it. 

Cobblers are a complement to code analysis : the analysis spot code to be fixed, the cobbler mends the code. Later, the analysis doesn't find those issues anymore.

List of Cobblers
--------------------------

.. _structures-addbracketstosingleinstructions:

.. _add-brackets-to-single-instructions:

Add Brackets To Single Instructions
+++++++++++++++++++++++++++++++++++
This cobbler adds curly brackets to single expression, with for(), foreach(), while(); and do...while() instructions. 

No brackets are added to instructions that are already bracketed.

.. _add-brackets-to-single-instructions-before:

Before
______
.. code-block:: php

   <?php
   
   if ($a) 
   	$b = 1;
   else {
   	$c = ;2
   }
   
   ?>

.. _add-brackets-to-single-instructions-after:

After
_____
.. code-block:: php

   <?php
   
   if ($a) {
   	$b = 1;
   } else {
   	$c = ;2
   }
   
   ?>



.. _add-brackets-to-single-instructions-specs:

Specs
_____

+----------------+--------------------------------------------+
| Short Name     | Structures/AddBracketsToSingleInstructions |
+----------------+--------------------------------------------+
| Exakat version | 2.4.6                                      |
+----------------+--------------------------------------------+
| Available in   |                                            |
+----------------+--------------------------------------------+


.. _classes-addfinalclass:

.. _add-final-class:

Add Final Class
+++++++++++++++
Adds ``final`` keyword to classes that can suppport it.


.. _add-final-class-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       // this class is not extended, so it might be final
   }
   
   ?>

.. _add-final-class-after:

After
_____
.. code-block:: php

   <?php
   
   final class x {
   }
   
   ?>

.. _add-final-class-suggested-analysis:

Suggested Analysis
__________________

* :ref:`class-could-be-final`

.. _add-final-class-related-cobbler:

Related Cobblers
________________

* :ref:`No anchor for Classes/AddFinalConstant <no-anchor-for-classes-addfinalconstant>`

.. _add-final-class-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-final`



.. _add-final-class-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/AddFinalClass                                            |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-addnoscream:

.. _add-no-scream-@:

Add No Scream @
+++++++++++++++
Adds the no scream operator `@` to an expression. 

.. _add-no-scream-@-before:

Before
______
.. code-block:: php

   <?php
       $a;
   ?>

.. _add-no-scream-@-after:

After
_____
.. code-block:: php

   <?php
       @$a;
   ?>

.. _add-no-scream-@-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _add-no-scream-@-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-noscream-@`



.. _add-no-scream-@-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/AddNoScream                                           |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-arraytobracket:

.. _array-to-bracket:

Array To Bracket
++++++++++++++++
This cobbler updates the array() syntax, and changes it to the bracket syntax.


.. _array-to-bracket-before:

Before
______
.. code-block:: php

   <?php
   $a = array(1, 2, 3);
   ?>

.. _array-to-bracket-after:

After
_____
.. code-block:: php

   <?php
   $a = [1, 2, 3];
   ?>



.. _array-to-bracket-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/ArrayToBracket                                        |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _attributes-createphpdoc:

.. _create-phpdoc:

Create Phpdoc
+++++++++++++
Create PHPdoc comments for classes, interfaces, traits, methods and functions.

Parameters and return types are collected, along with the name of the structure.


.. _create-phpdoc-before:

Before
______
.. code-block:: php

   '<?php
   
   class y {
       function a1(string $error, R $r = null) : int|string
       {
   
       }
   ?>

.. _create-phpdoc-after:

After
_____
.. code-block:: php

   <?php
   
   /**
    * Name : y
    */
   class y {
      /**
       * Name : a1
       *
       * string $error
       * null|R $r
       * @return int|string
       *
       */
       function a1(string $error, R $r = null) : int|string
       {
   
       }
   ?>

.. _create-phpdoc-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Attributes/RemovePhpdoc <no-anchor-for-attributes-removephpdoc>`



.. _create-phpdoc-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Attributes/CreatePhpdoc                                          |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _namespaces-gatheruse:

.. _gather-use-expression:

Gather Use Expression
+++++++++++++++++++++
Move lone use expression to the beginning of the file.

.. _gather-use-expression-before:

Before
______
.. code-block:: php

   <?php
       use A;
       ++$a;
       use B;
   ?>
   

.. _gather-use-expression-after:

After
_____
.. code-block:: php

   <?php
       use A;
       use B;
       ++$a;
   ?>

.. _gather-use-expression-suggested-analysis:

Suggested Analysis
__________________

* :ref:`hidden-use-expression`



.. _gather-use-expression-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Namespaces/GatherUse                                             |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-makestaticfunction:

.. _make-static-closures-and-arrow-functions:

Make Static Closures And Arrow Functions
++++++++++++++++++++++++++++++++++++++++
Add the static option to closures and arrow functions. This prevents the defining environment to be included in the closure.



.. _make-static-closures-and-arrow-functions-before:

Before
______
.. code-block:: php

   <?php
       $a = function () { return 1; };
       $b = fn () => 2;
   ?>
   

.. _make-static-closures-and-arrow-functions-after:

After
_____
.. code-block:: php

   <?php
       $a = static function () { return 1; };
       $b = static fn () => 2;
   ?>

.. _make-static-closures-and-arrow-functions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-static-closure`

.. _make-static-closures-and-arrow-functions-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Functions/RemoveStaticFromFunction <no-anchor-for-functions-removestaticfromfunction>`



.. _make-static-closures-and-arrow-functions-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Functions/MakeStaticFunction                                     |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _utils-multi:

.. _multiple-cobbler:

Multiple cobbler
++++++++++++++++
Allows to configure multiple cobbler in one file. The file is a YAML file, and must be located in the project's folder. 

The file containts a root object 'cobbler', filled with an array of cobblers, and their related configuration. Cobblers may be repeated as often as necessary.

cobblers:
- Functions/RenameParameter:
    oldName: $a
    newName: $b
    method: \foo
- Functions/RenameParameter:
    oldName: $a2
    newName: $b
    method: \foo2

The order of the configuration file is the order of execution. Do not rely on it.



.. _multiple-cobbler-before:

Before
______
.. code-block:: php

   

.. _multiple-cobbler-after:

After
_____
.. code-block:: php

   


.. _multiple-cobbler-configfile:

Parameters
__________

+------------+---------+--------+---------------------------------------+
| Name       | Default | Type   | Description                           |
+------------+---------+--------+---------------------------------------+
| configFile |         | string | The .yaml file in the project folder. |
+------------+---------+--------+---------------------------------------+



.. _multiple-cobbler-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Utils/Multi                                                      |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-plusonetopre:

.. _plus-one-to-pre-plusplus:

Plus One To Pre Plusplus
++++++++++++++++++++++++
Transforms a `+ 1` or `- 1` operation into a plus-plus (or minus-minus).

.. _plus-one-to-pre-plusplus-before:

Before
______
.. code-block:: php

   <?php
       $a = $a + 1;
   ?>

.. _plus-one-to-pre-plusplus-after:

After
_____
.. code-block:: php

   <?php
       ++$a;
   ?>



.. _plus-one-to-pre-plusplus-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/PlusOneToPre                                                                                                 |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


.. _structures-posttopre:

.. _post-to-pre-plusplus:

Post to Pre Plusplus
++++++++++++++++++++
Transforms a post plus-plus (or minus-minus) operator, into a pre plus-plus (or minus-minus) operator.



.. _post-to-pre-plusplus-before:

Before
______
.. code-block:: php

   <?php 
       $a++;
   ?>

.. _post-to-pre-plusplus-after:

After
_____
.. code-block:: php

   <?php
       ++$a;
   ?>



.. _post-to-pre-plusplus-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/PostToPre                                                                                                    |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


.. _classes-removemethod:

.. _remove-a-method-in-a-class:

Remove A Method In A Class
++++++++++++++++++++++++++
This removes a method in a class. The method name is provided with its fully qualified name : Name of the class:: name of the method. 

The method's name is a string.


.. _remove-a-method-in-a-class-before:

Before
______
.. code-block:: php

   <?php
   
   // removing method \x::method1 
   class x {
       function method1() {}
       function method2() {}
   }
   
   ?>

.. _remove-a-method-in-a-class-after:

After
_____
.. code-block:: php

   <?php
   
   // removed method \x::method1 
   class x {
       function method2() {}
   }
   
   ?>


.. _remove-a-method-in-a-class-name:

Parameters
__________

+------+------------+--------+-----------------------------------------------------------------+
| Name | Default    | Type   | Description                                                     |
+------+------------+--------+-----------------------------------------------------------------+
| name | x::method1 | string | Fully qualified name of the method to remove. Only one allowed. |
+------+------------+--------+-----------------------------------------------------------------+



.. _remove-a-method-in-a-class-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/RemoveMethod                                             |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _classes-removeabstract:

.. _remove-abstract:

Remove Abstract
+++++++++++++++
Remove the abstract option, from classes and methods.


.. _remove-abstract-before:

Before
______
.. code-block:: php

   <?php
   abstract class x {
       function foo() {}
       
       abstract function moo() ;
   }
   ?>

.. _remove-abstract-after:

After
_____
.. code-block:: php

   <?php
   class x {
       function foo() {}
       
       function moo() {}
   }
   ?>



.. _remove-abstract-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/RemoveAbstract                                           |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-removedollarcurly:

.. _remove-dollar-curly:

Remove Dollar Curly
+++++++++++++++++++
This cobbler transforms the ```` structure into ``{$ }``. It is assumed that the content of the curly braces are only a variable name.

This update is important for PHP 8.2, where the syntax is deprecated.



.. _remove-dollar-curly-before:

Before
______
.. code-block:: php

   <?php
   
   $a = ;
   
   ?>

.. _remove-dollar-curly-after:

After
_____
.. code-block:: php

   <?php
   
   $a = {$b};
   
   ?>



.. _remove-dollar-curly-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RemoveDollarCurly                                     |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _classes-removefinal:

.. _remove-final:

Remove Final
++++++++++++
This cobbler removes the ``final`` keyword on classes and methods.

.. _remove-final-before:

Before
______
.. code-block:: php

   <?php
   
   final class y {
       final function foo() {}
   }
   
   ?>
   

.. _remove-final-after:

After
_____
.. code-block:: php

   <?php
   
   class y {
       function foo() {}
   }
   
   ?>
   

.. _remove-final-related-cobbler:

Related Cobblers
________________

* :ref:`add-final-class`
* :ref:`No anchor for Classes/AddFinalMethod <no-anchor-for-classes-addfinalmethod>`

.. _remove-final-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`add-final-class`
* :ref:`No anchor for Classes/AddFinalMethod <no-anchor-for-classes-addfinalmethod>`



.. _remove-final-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/RemoveFinal                                              |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-removecode:

.. _remove-instructions:

Remove Instructions
+++++++++++++++++++
Removes atomic instructions from the code. The whole expression is removed, and the slot is closed. 

This cobbler works with element of a block, and not with part of larger expression (like remove a condition in a if/then, or remove the block expression of a while). 

.. _remove-instructions-before:

Before
______
.. code-block:: php

   <?php
       $a = 1; // Code to be removed
       foo(1); 
       
       do          // can remove the while expression
           ++$a;   // removing the block of the do...wihle will generate an compilation error
       while ($a < 10);
       
   ?>

.. _remove-instructions-after:

After
_____
.. code-block:: php

   <?php
       foo(1); 
   ?>

.. _remove-instructions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`useless-instructions`



.. _remove-instructions-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RemoveCode                                            |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-removenoscream:

.. _remove-noscream-@:

Remove Noscream @
+++++++++++++++++
Removes the @ operator.

.. _remove-noscream-@-before:

Before
______
.. code-block:: php

   <?php
       @$a;
   ?>

.. _remove-noscream-@-after:

After
_____
.. code-block:: php

   <?php
       $a;
   ?>

.. _remove-noscream-@-suggested-analysis:

Suggested Analysis
__________________

* :ref:`@-operator`

.. _remove-noscream-@-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _remove-noscream-@-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveNoScream                                                                                               |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


.. _structures-removeparenthesis:

.. _remove-parenthesis:

Remove Parenthesis
++++++++++++++++++
Remove useless parenthesis from return expression.

.. _remove-parenthesis-before:

Before
______
.. code-block:: php

   <?php
   function foo() {
       return (1);
   }
   ?>

.. _remove-parenthesis-after:

After
_____
.. code-block:: php

   <?php
   function foo() {
       return 1;
   }
   ?>

.. _remove-parenthesis-suggested-analysis:

Suggested Analysis
__________________

* :ref:`no-parenthesis-for-language-construct`



.. _remove-parenthesis-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RemoveParenthesis                                     |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _classes-removereadonly:

.. _remove-readonly-option:

Remove Readonly Option
++++++++++++++++++++++
Readonly is a property and class option. This cobbler removes it from both. 

The readonly keyword is removed from property definitions, and from promoted properties.


.. _remove-readonly-option-before:

Before
______
.. code-block:: php

   <?php
   
   readonly class x {
       private readonly string $x;
   }
   
   ?>

.. _remove-readonly-option-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private string $x;
   }
   
   ?>

.. _remove-readonly-option-suggested-analysis:

Suggested Analysis
__________________

* :ref:`readonly-usage`
* Classes/CouldBeReadonly



.. _remove-readonly-option-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/RemoveReadonly                                           |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-removestaticfromclosure:

.. _remove-static-from-closures-and-arrow-functions:

Remove Static From Closures And Arrow Functions
+++++++++++++++++++++++++++++++++++++++++++++++
Removes the static option from closures and arrow functions.



.. _remove-static-from-closures-and-arrow-functions-before:

Before
______
.. code-block:: php

   <?php
       $a = static function () { return 1; };
       $b = static fn () => 2;
   ?>
   

.. _remove-static-from-closures-and-arrow-functions-after:

After
_____
.. code-block:: php

   <?php
       $a = function () { return 1; };
       $b = fn () => 2;
   ?>

.. _remove-static-from-closures-and-arrow-functions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`cannot-use-static-for-closure`

.. _remove-static-from-closures-and-arrow-functions-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`make-static-closures-and-arrow-functions`



.. _remove-static-from-closures-and-arrow-functions-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Functions/RemoveStaticFromClosure                                |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _attributes-removeattribute:

.. _remove-the-attribute:

Remove The Attribute
++++++++++++++++++++
Remove attributes from all supporting structures.

Attributes are located on functions, classes, class constants, properties, methods and arguments.


.. _remove-the-attribute-before:

Before
______
.. code-block:: php

   <?php
   
   #[Attribute] 
   function foo(#[AttributeArgument] $arg) {
   
   }
   ?>

.. _remove-the-attribute-after:

After
_____
.. code-block:: php

   <?php
   
   
   function foo($arg) {
   
   }
   ?>



.. _remove-the-attribute-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Attributes/RemoveAttribute                                       |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-removetypes:

.. _remove-typehint:

Remove Typehint
+++++++++++++++
This cobbler remove the typehint mentions in the code. This might yield some speed when executing, since those tests will be not conveyed at runtime. 

Typehints from arguments, method returns and properties are all removed. 


.. _remove-typehint-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private string $p;
       
       function foo(D\E $arg) : void {
       
       }
   }
   
   ?>

.. _remove-typehint-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private $p;
       
       function foo($arg) {
       
       }
   }
   
   ?>


.. _remove-typehint-type\_to\_remove:

Parameters
__________

+----------------+---------+------+----------------------------------------------------------------------------------------------------------+
| Name           | Default | Type | Description                                                                                              |
+----------------+---------+------+----------------------------------------------------------------------------------------------------------+
| type_to_remove | all     | data | A comma separated list of types to remove. For example : never,string,A\B\C;. Use 'All' for everyt type. |
+----------------+---------+------+----------------------------------------------------------------------------------------------------------+

.. _remove-typehint-suggested-analysis:

Suggested Analysis
__________________

* :ref:`php-8.1-typehints`

.. _remove-typehint-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`set-typehints`



.. _remove-typehint-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Functions/RemoveTypes                                            |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.2.5                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _namespaces-removeuse:

.. _remove-unused-use:

Remove Unused Use
+++++++++++++++++
Removes the unused use expression from the top of the file. Groupuse are not processed yet.

.. _remove-unused-use-before:

Before
______
.. code-block:: php

   <?php
   
   use a\b;
   use c\d;
   
   new b();
   
   ?>

.. _remove-unused-use-after:

After
_____
.. code-block:: php

   <?php
   
   use a\b;
   
   new b();
   
   ?>

.. _remove-unused-use-suggested-analysis:

Suggested Analysis
__________________

* :ref:`unused-use`



.. _remove-unused-use-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Namespaces/RemoveUse                                             |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _classes-removevisibility:

.. _remove-visibility:

Remove Visibility
+++++++++++++++++
Removes the visibility on constants, properties and methods. 

For properties, the visibility is reset to public. 

.. _remove-visibility-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private const x = 1;
       private $p = 2;
       private function foo() {}
       private function __construct() {}
   }
   ?>

.. _remove-visibility-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       const x = 1;
       public $p = 2;
       function foo() {}
       function __construct() {}
   }
   ?>



.. _remove-visibility-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/RemoveVisibility                                         |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-removevariable:

.. _remove-written-only-variable:

Remove Written Only Variable
++++++++++++++++++++++++++++
This removes variables that are written only. 

.. _remove-written-only-variable-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       $a = 1;
       $a += 2; // No usage of $a
   }
   
   ?>

.. _remove-written-only-variable-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() {
   }
   
   ?>

.. _remove-written-only-variable-suggested-analysis:

Suggested Analysis
__________________

* :ref:`written-only-variables`



.. _remove-written-only-variable-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RemoveVariable                                        |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-renamefunction:

.. _rename-a-function:

Rename A Function
+++++++++++++++++
Give a function with a new name. 

This cobbler doesn't update the name of the functioncalls. 

This cobbler may be used with functions, and methods. Functions may be identified with their fully qualified name (i.e. \path\foo) and methods with the extended fully qualified name (i.e. : \path\aClass::methodName). 



.. _rename-a-function-before:

Before
______
.. code-block:: php

   <?php
       function foo() {
       
       }
   ?>

.. _rename-a-function-after:

After
_____
.. code-block:: php

   <?php
       function bar() {
       
       }
   ?>


.. _rename-a-function-name:

Parameters
__________

+------+---------+--------+-------------------------------+
| Name | Default | Type   | Description                   |
+------+---------+--------+-------------------------------+
| name | foo     | string | The new name of the function. |
+------+---------+--------+-------------------------------+

.. _rename-a-function-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-a-function-related-cobbler:

Related Cobblers
________________

* :ref:`rename-functioncalls`

.. _rename-a-function-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _rename-a-function-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RenameFunction                                        |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-renamefunctioncall:

.. _rename-functioncalls:

Rename FunctionCalls
++++++++++++++++++++
Rename a function call to another function.

.. _rename-functioncalls-before:

Before
______
.. code-block:: php

   <?php
       foo(1, 2);
   ?>

.. _rename-functioncalls-after:

After
_____
.. code-block:: php

   <?php
       bar(1, 2);
   ?>


.. _rename-functioncalls-destination:

Parameters
__________

+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| Name        | Default       | Type   | Description                                                                             |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| origin      | strtolower    | string | The function name to rename. It will be use lower-cased, and as a fully qualified name. |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| destination | mb_strtolower | string | The function name to rename. It will be use as is. FQN is possible.                     |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+

.. _rename-functioncalls-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-functioncalls-related-cobbler:

Related Cobblers
________________

* :ref:`rename-a-function`
* :ref:`rename-methodcall`

.. _rename-functioncalls-reverse-cobbler:

Reverse Cobbler
_______________

* This cobbler is its own reverse. 



.. _rename-functioncalls-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RenameFunctionCall                                    |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-renamemethodcall:

.. _rename-methodcall:

Rename Methodcall
+++++++++++++++++
Rename a method, in a methodcall, with a new name. 

This cobbler doesn't update the definition of the method. It works both on static and non-static methods. 



.. _rename-methodcall-before:

Before
______
.. code-block:: php

   <?php
       $o->method();
   ?>

.. _rename-methodcall-after:

After
_____
.. code-block:: php

   <?php
       $o->newName();
   ?>


.. _rename-methodcall-destination:

Parameters
__________

+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| Name        | Default       | Type   | Description                                                                             |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| origin      | strtolower    | string | The function name to rename. It will be use lower-cased, and as a fully qualified name. |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+
| destination | mb_strtolower | string | The function name to rename. It will be use as is. FQN is possible.                     |
+-------------+---------------+--------+-----------------------------------------------------------------------------------------+

.. _rename-methodcall-suggested-analysis:

Suggested Analysis
__________________

* :ref:`No anchor for Utils/Selector <no-anchor-for-utils-selector>`

.. _rename-methodcall-related-cobbler:

Related Cobblers
________________

* :ref:`rename-functioncalls`
* :ref:`rename-a-function`

.. _rename-methodcall-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`No anchor for Structures/RemoveMethodCall <no-anchor-for-structures-removemethodcall>`



.. _rename-methodcall-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/RenameMethodcall                                      |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-renameparameter:

.. _rename-parameter:

Rename Parameter
++++++++++++++++
Change the name of a parameter to a new name.

The destination parameter name is a constant. 
Suggestions : rename all parameters from the top method (in classes)
rename parameters $a into $b (currently, no $a available)

Limits : this cobbler doesn't check that another parameter is already using that name, nor if a local variable is also using that name. This may lead to unexpected results.


.. _rename-parameter-before:

Before
______
.. code-block:: php

   <?php
   
   foo(a: 1);
   
   function foo($a) { 
       return $a;
   }
   
   ?>

.. _rename-parameter-after:

After
_____
.. code-block:: php

   <?php
   
   foo(b: 1);
   
   function foo($b) { 
       return $b;
   }
   
   ?>


.. _rename-parameter-method:

Parameters
__________

+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| Name    | Default | Type   | Description                                                                                                      |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| oldName | $A      | string | The original name of the parameter.                                                                              |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| newName | $B      | string | The new name of the parameter.                                                                                   |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+
| method  |         | string | The name of the target method. Use a full qualified name for a function, and the class name::method for methods. |
+---------+---------+--------+------------------------------------------------------------------------------------------------------------------+



.. _rename-parameter-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Functions/RenameParameter                                        |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-setnulltype:

.. _set-null-type:

Set Null Type
+++++++++++++
Adds a Null type to typehints when necessary. 

This cobbler only adds a null type when there is already another type. It doesn't add a null type when no type is set. 

It works on methods, functions, closures and arrow functions. It doesn't work on properties.

The null type is added as a question mark `?` when the type is unique, and as null when the types are multiple.


.. _set-null-type-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() : int {
       if (rand(0, 1)) {
           return 1;
       } else {
           return null;
       }
   }
   
   ?>

.. _set-null-type-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() : ?int {
       if (rand(0, 1)) {
           return 1;
       } else {
           return null;
       }
   }
   
   ?>

.. _set-null-type-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-typehint`



.. _set-null-type-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetNullType                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


.. _functions-settypevoid:

.. _set-type-void:

Set Type Void
+++++++++++++
Adds the void typehint to functions and methods, when possible.

.. _set-type-void-before:

Before
______
.. code-block:: php

   <?php
   
   function foo() {
       return;
   }
   
   ?>

.. _set-type-void-after:

After
_____
.. code-block:: php

   <?php
   
   function foo() : void {
       return;
   }
   
   ?>

.. _set-type-void-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-void`

.. _set-type-void-related-cobbler:

Related Cobblers
________________

* :ref:`set-typehints`
* :ref:`set-null-type`

.. _set-type-void-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-typehint`



.. _set-type-void-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Functions/SetTypeVoid                                            |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _functions-settypehints:

.. _set-typehints:

Set Typehints
+++++++++++++
Automagically add scalar typehints to methods and properties. Arguments and return values are both supported. 

When multiple possible types are identified, no typehint is added. If a typehint is already set, no typehint is added.

Magic methods, such as __get(), __set(), __construct(), __desctruct(), etc are not modified by this cobbler. 

Methods which have parent's methods (resp. children's) are skipped for argument typing (resp return typing) : this may introduce a incompatible definition. On the other hand, methods which have children's methods (resp. parents') are modified for argument typing (resp return typing), thanks to covariance (resp. contravariance). 

Void (as a scalar type) and Null types are processed in a separate cobbler. 

By default, and in case of conflict, array is chosen over iterable and int is chosen over float. There are parameter to alter this behavior.



.. _set-typehints-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       private int $p = 2;
   
       function foo(int $a = 1) : int {
           return intdiv($a, $this->p);
       }
   }
   ?>

.. _set-typehints-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       private int $p = 2;
   
       function foo(int $a = 1) : int {
           return intdiv($a, $this->p);
       }
   }
   ?>
   


.. _set-typehints-int\_or\_float:

Parameters
__________

+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                                                       |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| array_or_iterable | array   | string | When array and iterable are the only suggestions, choose 'array', 'iterable', or 'omit'. By default, it is array. |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| int_or_float      | float   | string | When int and float are the only suggestions, choose 'int', 'float', or 'omit'. By default, it is float.           |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+

.. _set-typehints-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-be-void`

.. _set-typehints-related-cobbler:

Related Cobblers
________________

* :ref:`var-to-public`
* :ref:`split-property-definitions`
* :ref:`set-null-type`
* :ref:`set-type-void`



.. _set-typehints-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Functions/SetTypehints                                                                                                  |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


.. _classes-splitpropertydefinitions:

.. _split-property-definitions:

Split Property Definitions
++++++++++++++++++++++++++
Split multiple properties definition into independent definitions. 

This applies to classes and traits. 

.. _split-property-definitions-before:

Before
______
.. code-block:: php

   <?php
       class x {
           private $x, $y, $z;
       }
   ?>
   

.. _split-property-definitions-after:

After
_____
.. code-block:: php

   <?php
       class x {
           private $x;
           private $y;
           private $z;
       }
   ?>

.. _split-property-definitions-suggested-analysis:

Suggested Analysis
__________________

* :ref:`multiple-property-declaration-on-one-line`



.. _split-property-definitions-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/SplitPropertyDefinitions                                 |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-switchtomatch:

.. _switch-to-match:

Switch To Match
+++++++++++++++
Transforms a switch() into a match() expression.

The switch() syntax must have each of the cases assigning the same variable (or similar). There should not be any other operation, besides break;



.. _switch-to-match-before:

Before
______
.. code-block:: php

   <?php
       switch($a) {
           case 1: 
               $b = '1';
               break;
           case 2: 
               $b = '3';
               break;
           default:  
               $b = '0';
               break; 
       }
   ?>
   

.. _switch-to-match-after:

After
_____
.. code-block:: php

   <?php
       $b = match($a) {
           1 => '1',
           2 => '3',
           default => '0'
       };
   ?>
   

.. _switch-to-match-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-use-match`

.. _switch-to-match-related-cobbler:

Related Cobblers
________________

* :ref:`post-to-pre-plusplus`

.. _switch-to-match-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-instructions`



.. _switch-to-match-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/SwitchToMatch                                         |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _namespaces-usealias:

.. _use-available-alias:

Use Available Alias
+++++++++++++++++++
Apply systematically the use expression in the code.

.. _use-available-alias-before:

Before
______
.. code-block:: php

   <?php
       use A\B\C as D;
       new A\B\C();
   ?>
   

.. _use-available-alias-after:

After
_____
.. code-block:: php

   <?php
       use A\B\C as D;
       new D();
   ?>

.. _use-available-alias-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-use-alias`



.. _use-available-alias-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Namespaces/UseAlias                                              |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _classes-vartopublic:

.. _var-to-public:

Var To Public
+++++++++++++
Replace the var syntax with public keyword. 

It is also possible to replace it with protected or private, with the parameter. 

.. _var-to-public-before:

Before
______
.. code-block:: php

   <?php
   
   class x {
       var $y = 1;
   }
   ?>

.. _var-to-public-after:

After
_____
.. code-block:: php

   <?php
   
   class x {
       public $y = 1;
   }
   ?>


.. _var-to-public-var\_to\_visibility:

Parameters
__________

+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                          |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| var_to_visibility | public  | string | The destination visibility to be used. May be one of: public, protected or private.  |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+

.. _var-to-public-related-cobbler:

Related Cobblers
________________

* :ref:`set-typehints`



.. _var-to-public-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Classes/VarToPublic                                              |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+


.. _structures-arraykeysspeedup:

.. _array\_key\_exists()-speedup:

array_key_exists() Speedup
++++++++++++++++++++++++++
array_key_exists() is sped up when declared with a use expression.

.. _array\_key\_exists()-speedup-before:

Before
______
.. code-block:: php

   <?php
   
   namespace A {
       array_key_exists($a, $b);
   }
   
   ?>

.. _array\_key\_exists()-speedup-after:

After
_____
.. code-block:: php

   <?php
   
   namespace A {
       use function array_key_exists;
       
       array_key_exists($a, $b);
   }
   
   ?>

.. _array\_key\_exists()-speedup-suggested-analysis:

Suggested Analysis
__________________

* :ref:`always-use-function-with-array\_key\_exists()`
* :ref:`array\_key\_exists()-speedup`



.. _array\_key\_exists()-speedup-specs:

Specs
_____

+----------------+------------------------------------------------------------------+
| Short Name     | Structures/ArrayKeysSpeedup                                      |
+----------------+------------------------------------------------------------------+
| Exakat version | 2.3.0                                                            |
+----------------+------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+----------------+------------------------------------------------------------------+



