.. _extensions-extxmlwriter:

.. _ext-xmlwriter:

ext/xmlwriter
+++++++++++++

  Extension ext/`xmlwriter <https://www.php.net/xmlwriter>`_.

The `XMLWriter <https://www.php.net/xmlwriter>`_ extension wraps the libxml `xmlWriter <https://www.php.net/xmlwriter>`_ API inside PHP.

.. code-block:: php
   
   <?php
   $xw = xmlwriter_open_memory();
   xmlwriter_set_indent($xw, TRUE);
   xmlwriter_start_document($xw, NULL, 'UTF-8');
   xmlwriter_start_element($xw, 'root');
   xmlwriter_write_attribute_ns($xw, 'prefix', '', 'http://www.php.net/uri');
   xmlwriter_start_element($xw, 'elem1');
   xmlwriter_write_attribute($xw, 'attr1', 'first');
   xmlwriter_end_element($xw);
   xmlwriter_full_end_element($xw);
   xmlwriter_end_document($xw);
   $output = xmlwriter_flush($xw, true);
   print $output;
   // write attribute_ns without start_element first
   $xw = xmlwriter_open_memory();
   var_dump(xmlwriter_write_attribute_ns($xw, 'prefix', 'id', 'http://www.php.net/uri', 'elem1'));
   print xmlwriter_output_memory($xw);
   ?>

See also `XMLWriter <https://www.php.net/manual/en/book.xmlwriter.php>`_ and `Module xmlwriter from libxml2 <http://xmlsoft.org/html/libxml-xmlwriter.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxmlwriter                                                                                                                                                                 |
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
| Features     | xml                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


