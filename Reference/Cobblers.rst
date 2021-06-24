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

* :ref:`No anchor for Classes/VarToPublic <no-anchor-for-classes-vartopublic>`
* :ref:`No anchor for Classes/SplitPropertyDefinitions <no-anchor-for-classes-splitpropertydefinitions>`
* :ref:`No anchor for Functions/SetNullType <no-anchor-for-functions-setnulltype>`
* :ref:`No anchor for Functions/SetTypeVoid <no-anchor-for-functions-settypevoid>`



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



