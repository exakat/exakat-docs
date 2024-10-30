.. _performances-php74arraykeyexists:

.. _always-use-function-with-array\_key\_exists():

Always Use Function With array_key_exists()
+++++++++++++++++++++++++++++++++++++++++++

  `array_key_exists() <https://www.php.net/array_key_exists>`_ has been granted a special virtual machine opcode, and is much faster. This applies to PHP 7.4 and more recent. 

It requires that `array_key_exists() <https://www.php.net/array_key_exists>`_ is statically resolved, either with an initial ``\``, or a ``use function`` expression. This doesn't affect the global namespace.
This analysis is related to Php/ShouldUseFunction, and is a special case, that only concerns `array_key_exists() <https://www.php.net/array_key_exists>`_.

.. code-block:: php
   
   <?php
   
   namespace my/name/space;
   
   // do not forget the 'function' keyword, or it will apply to classes.
   use function array_key_exists as foo; // the alias is not necessary, and may be omitted.
   
   // array_key_exists is aliased to foo : 
   $c = foo($a, $b);
   
   // This call requires a fallback to global, and will be slow.
   $c = array_key_exists($a, $b);
   
   ?>

See also `Add array_key_exists to the list of specially compiled functions <https://bugs.php.net/bug.php?id=76148>`_.

Connex PHP features
-------------------

  + `vm <https://php-dictionary.readthedocs.io/en/latest/dictionary/vm.ini.html>`_
  + `opcode <https://php-dictionary.readthedocs.io/en/latest/dictionary/opcode.ini.html>`_


Suggestions
___________

* Use the `use` command for arrray_key_exists(), at the beginning of the script
* Use an initial \ before array_key_exists()
* Remove the namespace




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/Php74ArrayKeyExists                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


