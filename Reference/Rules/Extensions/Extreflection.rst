.. _extensions-extreflection:

.. _ext-reflection:

ext/reflection
++++++++++++++

  Extension `Reflection <https://www.php.net/reflection>`_.

PHP comes with a complete `reflection <https://www.php.net/reflection>`_ API that adds the ability to reverse-engineer classes, interfaces, functions, methods and extensions. Additionally, the `reflection <https://www.php.net/reflection>`_ API offers ways to retrieve doc comments for functions, classes and methods.

.. code-block:: php
   
   <?php
   /**
    * A simple counter
    *
    * @return    int
    */
   function counter1()
   {
       static $c = 0;
       return ++$c;
   }
   
   /**
    * Another simple counter
    *
    * @return    int
    */
   $counter2 = function()
   {
       static $d = 0;
       return ++$d;
   
   };
   
   function dumpReflectionFunction($func)
   {
       // Print out basic information
       printf(
           PHP_EOL.'===> The %s function '%s''.PHP_EOL.
           '     declared in %s'.PHP_EOL.
           '     lines %d to %d'.PHP_EOL,
           $func->isInternal() ? 'internal' : 'user-defined',
           $func->getName(),
           $func->getFileName(),
           $func->getStartLine(),
           $func->getEndline()
       );
   
       // Print documentation comment
       printf('---> Documentation:'.PHP_EOL.' %s',PHP_EOL, var_export($func->getDocComment(), 1));
   
       // Print static variables if existant
       if ($statics = $func->getStaticVariables())
       {
           printf('---> Static variables: %s',PHP_EOL, var_export($statics, 1));
       }
   }
   
   // Create an instance of the ReflectionFunction class
   dumpReflectionFunction(new ReflectionFunction('counter1'));
   dumpReflectionFunction(new ReflectionFunction($counter2));
   ?>

See also `Reflection <https://www.php.net/manual/en/book.reflection.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extreflection                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


