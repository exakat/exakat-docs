.. _extensions-extxmlwriter:

.. _ext-xmlwriter:

ext/xmlwriter
+++++++++++++

.. meta::
	:description:
		ext/xmlwriter: Extension ext/xmlwriter.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xmlwriter
	:twitter:description: ext/xmlwriter: Extension ext/xmlwriter
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xmlwriter
	:og:type: article
	:og:description: Extension ext/xmlwriter
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/xmlwriter.html
	:og:locale: en
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

Connex PHP features
-------------------

  + `xml <https://php-dictionary.readthedocs.io/en/latest/dictionary/xml.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxmlwriter                                                                                                                                                                 |
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


