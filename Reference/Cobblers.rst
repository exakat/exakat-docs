.. _Cobblers:

Cobblers
=================

Introduction
--------------------------
Cobblers mend PHP code. They apply a transformation to it. 

Cobblers are a complement to code analysis : the analysis spot code to be fixed, the cobbler mends the code. Later, the analysis doesn't find those issues anymore.

List of Cobblers
--------------------------

.. _set-typehints:

Set Typehints
#############
Automagically add scalar typehints to methods and properties. Arguments and return values are both supported. 

When multiple possible types are identified, no typehint is added. If a typehint is already set, no typehint is added.

Magic methods, such as __get(), __set(), __construct(), __desctruct(), etc are not modified by this cobbler. 

Methods which have parent's methods (resp. children's) are skipped for argument typing (resp return typing) : this may introduce a incompatible definition. On the other hand, methods which have children's methods (resp. parents') are modified for argument typing (resp return typing), thanks to covariance (resp. contravariance). 

Void (as a scalar type) and Null types are processed in a separate cobbler. 

By default, and in case of conflict, array is chosen over iterable and int is chosen over float. There are parameter to alter this behavior.



.. _set-typehints-before:

Before
++++++
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
+++++
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
++++++++++

+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                                                       |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| array_or_iterable | array   | string | When array and iterable are the only suggestions, choose 'array', 'iterable', or 'omit'. By default, it is array. |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+
| int_or_float      | float   | string | When int and float are the only suggestions, choose 'int', 'float', or 'omit'. By default, it is float.           |
+-------------------+---------+--------+-------------------------------------------------------------------------------------------------------------------+

.. _set-typehints-suggested-analysis:

Suggested Analysis
++++++++++++++++++

* :ref:`could-be-void`

.. _set-typehints-related-cobbler:

Related Cobblers
++++++++++++++++

* :ref:`var-to-public`
* :ref:`split-property-definitions`
* :ref:`set-null-type`
* :ref:`set-type-void`



.. _set-typehints-specs:

Specs
+++++

+----------------+------------------------+
| Short Name     | Functions/SetTypehints |
+----------------+------------------------+
| Exakat version | 2.3.0                  |
+----------------+------------------------+


.. _plus-one-to-pre-plusplus:

Plus One To Pre Plusplus
########################
Transforms a `+ 1` or `- 1` operation into a plus-plus (or minus-minus).

.. _plus-one-to-pre-plusplus-before:

Before
++++++
.. code-block:: php

   <?php
       $a = $a + 1;
   ?>

.. _plus-one-to-pre-plusplus-after:

After
+++++
.. code-block:: php

   <?php
       ++$a;
   ?>



.. _plus-one-to-pre-plusplus-specs:

Specs
+++++

+----------------+-------------------------+
| Short Name     | Structures/PlusOneToPre |
+----------------+-------------------------+
| Exakat version | 2.3.0                   |
+----------------+-------------------------+


.. _post-to-pre-plusplus:

Post to Pre Plusplus
####################
Transforms a post plus-plus (or minus-minus) operator, into a pre plus-plus (or minus-minus) operator.



.. _post-to-pre-plusplus-before:

Before
++++++
.. code-block:: php

   <?php 
       $a++;
   ?>

.. _post-to-pre-plusplus-after:

After
+++++
.. code-block:: php

   <?php
       ++$a;
   ?>



.. _post-to-pre-plusplus-specs:

Specs
+++++

+----------------+----------------------+
| Short Name     | Structures/PostToPre |
+----------------+----------------------+
| Exakat version | 2.3.0                |
+----------------+----------------------+


.. _remove-noscream-@:

Remove Noscream @
#################
Removes the @ operator.

.. _remove-noscream-@-before:

Before
++++++
.. code-block:: php

   <?php
       @$a;
   ?>

.. _remove-noscream-@-after:

After
+++++
.. code-block:: php

   <?php
       $a;
   ?>

.. _remove-noscream-@-suggested-analysis:

Suggested Analysis
++++++++++++++++++

* :ref:`@-operator`

.. _remove-noscream-@-reverse-cobbler:

Reverse Cobbler
+++++++++++++++

* This cobbler is its own reverse. 



.. _remove-noscream-@-specs:

Specs
+++++

+----------------+---------------------------+
| Short Name     | Structures/RemoveNoScream |
+----------------+---------------------------+
| Exakat version | 2.3.0                     |
+----------------+---------------------------+


.. _var-to-public:

Var To Public
#############
Replace the var syntax with public keyword. 

It is also possible to replace it with protected or private, with the parameter. 

.. _var-to-public-before:

Before
++++++
.. code-block:: php

   <?php
   
   class x {
       var $y = 1;
   }
   ?>

.. _var-to-public-after:

After
+++++
.. code-block:: php

   <?php
   
   class x {
       public $y = 1;
   }
   ?>


.. _var-to-public-var\_to\_visibility:

Parameters
++++++++++

+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| Name              | Default | Type   | Description                                                                          |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+
| var_to_visibility | public  | string | The destination visibility to be used. May be one of: public, protected or private.  |
+-------------------+---------+--------+--------------------------------------------------------------------------------------+

.. _var-to-public-related-cobbler:

Related Cobblers
++++++++++++++++

* :ref:`set-typehints`



.. _var-to-public-specs:

Specs
+++++

+----------------+---------------------+
| Short Name     | Classes/VarToPublic |
+----------------+---------------------+
| Exakat version | 2.3.0               |
+----------------+---------------------+


.. _split-property-definitions:

Split Property Definitions
##########################
Split multiple properties definition into independent definitions. 

This applies to classes and traits. 

.. _split-property-definitions-before:

Before
++++++
.. code-block:: php

   <?php
       class x {
           private $x, $y, $z;
       }
   ?>
   

.. _split-property-definitions-after:

After
+++++
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
++++++++++++++++++

* :ref:`multiple-property-declaration-on-one-line`



.. _split-property-definitions-specs:

Specs
+++++

+----------------+----------------------------------+
| Short Name     | Classes/SplitPropertyDefinitions |
+----------------+----------------------------------+
| Exakat version | 2.3.0                            |
+----------------+----------------------------------+


.. _set-null-type:

Set Null Type
#############
Adds a Null type to typehints when necessary. 

This cobbler only adds a null type when there is already another type. It doesn't add a null type when no type is set. 

It works on methods, functions, closures and arrow functions. It doesn't work on properties.

The null type is added as a question mark `?` when the type is unique, and as null when the types are multiple.


.. _set-null-type-before:

Before
++++++
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
+++++
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



.. _set-null-type-specs:

Specs
+++++

+----------------+-----------------------+
| Short Name     | Functions/SetNullType |
+----------------+-----------------------+
| Exakat version | 2.3.0                 |
+----------------+-----------------------+


.. _set-type-void:

Set Type Void
#############
Adds the void typehint to functions and methods, when possible

.. _set-type-void-before:

Before
++++++
.. code-block:: php

   <?php
   
   function foo() {
       return;
   }
   
   ?>

.. _set-type-void-after:

After
+++++
.. code-block:: php

   <?php
   
   function foo() : void {
       return;
   }
   
   ?>

.. _set-type-void-related-cobbler:

Related Cobblers
++++++++++++++++

* :ref:`set-typehints`
* :ref:`set-null-type`



.. _set-type-void-specs:

Specs
+++++

+----------------+-----------------------+
| Short Name     | Functions/SetTypeVoid |
+----------------+-----------------------+
| Exakat version | 2.3.0                 |
+----------------+-----------------------+



