.. _extensions-extyaml:

.. _ext-yaml:

ext/yaml
++++++++

  Extension YAML.

This extension implements the `YAML Ain't Markup Language <http://www.yaml.org/>`_ (YAML) data serialization standard. Parsing and emitting are handled by the `LibYAML <http://pyyaml.org/wiki/LibYAML>`_ library.

.. code-block:: php
   
   <?php
   $addr = array(
       'given' => 'Chris',
       'family'=> 'Dumars',
       'address'=> array(
           'lines'=> '458 Walkman Dr.
           Suite #292',
           'city'=> 'Royal Oak',
           'state'=> 'MI',
           'postal'=> 48046,
         ),
     );
   $invoice = array (
       'invoice'=> 34843,
       'date'=> '2001-01-23',
       'bill-to'=> $addr,
       'ship-to'=> $addr,
       'product'=> array(
           array(
               'sku'=> 'BL394D',
               'quantity'=> 4,
               'description'=> 'Basketball',
               'price'=> 450,
             ),
           array(
               'sku'=> 'BL4438H',
               'quantity'=> 1,
               'description'=> 'Super Hoop',
               'price'=> 2392,
             ),
         ),
       'tax'=> 251.42,
       'total'=> 4443.52,
       'comments'=> 'Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.',
       );
   
   // generate a YAML representation of the invoice
   $yaml = yaml_emit($invoice);
   var_dump($yaml);
   
   // convert the YAML back into a PHP variable
   $parsed = yaml_parse($yaml);
   
   // check that roundtrip conversion produced an equivalent structure
   var_dump($parsed == $invoice);
   ?>

See also `YAML <https://www.php.net/manual/en/book.yaml.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extyaml                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


