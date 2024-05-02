.. _extensions-extgender:

.. _ext-gender:

ext/gender
++++++++++

  Gender extension.

The Gender PHP extension is a port of the gender.c program originally written by Joerg Michael. Its main purpose is to find out the gender of firstnames, based on a database of over 40000 firstnames from 54 countries.

.. code-block:: php
   
   <?php
   
   namespace Gender;
   
   $gender = new Gender;
   
    
   $name = 'Milene';
   $country = Gender::FRANCE;
    
   $result = $gender->get($name, $country);
   
   $data = $gender->country($country);
   
   switch($result) {
       case Gender::IS_FEMALE:
           printf('The name %s is female in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::IS_MOSTLY_FEMALE:
           printf('The name %s is mostly female in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::IS_MALE:
           printf('The name %s is male in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::IS_MOSTLY_MALE:
           printf('The name %s is mostly male in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::IS_UNISEX_NAME:
           printf('The name %s is unisex in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::IS_A_COUPLE:
           printf('The name %s is both male and female in %s\n', $name, $data['country']);
       break;
   
    
       case Gender::NAME_NOT_FOUND:
           printf('The name %s was not found for %s\n', $name, $data['country']);
       break;
   
    
       case Gender::ERROR_IN_NAME:
           echo 'There is an error in the given name!'.PHP_EOL;
       break;
    
       default:
           echo 'An error occurred!'.PHP_EOL;
       break;
   
   }
   
   ?>

See also `ext/gender manual <https://www.php.net/manual/en/book.gender.php>`_ and `genderReader <https://github.com/cstuder/genderReader>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgender                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


