.. _extensions-extenchant:

.. _ext-enchant:

ext/enchant
+++++++++++

  Extension Enchant.

Enchant is the PHP binding for the `Enchant spelling library <https://www.php.net/manual/en/book.enchant.php>`_. Enchant steps in to provide uniformity and conformity on top of all spelling libraries, and implement certain features that may be lacking in any individual provider library. 


.. code-block:: php
   
   <?php
   $tag = 'en_US';
   $r = enchant_broker_init();
   $bprovides = enchant_broker_describe($r);
   echo 'Current broker provides the following backend(s):'.PHP_EOL;
   print_r($bprovides);
   
   $dicts = enchant_broker_list_dicts($r);
   print_r($dicts);
   if (enchant_broker_dict_exists($r,$tag)) {
       $d = enchant_broker_request_dict($r, $tag);
       $dprovides = enchant_dict_describe($d);
       echo 'dictionary $tag provides:'.PHP_EOL;
       $wordcorrect = enchant_dict_check($d, 'soong');
       print_r($dprovides);
       if (!$wordcorrect) {
           $suggs = enchant_dict_suggest($d, 'soong');
           echo 'Suggestions for "soong":';
           print_r($suggs);
       }
       enchant_broker_free_dict($d);
   } else {
   }
   enchant_broker_free($r);
   ?>

See also `Enchant spelling library <https://www.php.net/manual/en/book.enchant.php>`_ and `Enchant <https://www.abisource.com/projects/enchant/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extenchant                                                                                                                                                                   |
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


