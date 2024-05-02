.. _extensions-extxml:

.. _ext-xml:

ext/xml
+++++++

  Extension xml (Parser).

This PHP extension implements support for James Clark's expat in PHP. This toolkit lets you parse, but not validate, XML documents.

.. code-block:: php
   
   <?php
   $file = "data.xml";
   $depth = array();
   
   function startElement($parser, $name, $attrs)
   {
       global $depth;
   
       if (!isset($depth[$parser])) {
           $depth[$parser] = 0;
       }
   
       for ($i = 0; $i < $depth[$parser]; $i++) {
           echo "  ";
       }
       echo "$name\n";
       $depth[$parser]++;
   }
   
   function endElement($parser, $name)
   {
       global $depth;
       $depth[$parser]--;
   }
   
   $xml_parser = xml_parser_create();
   xml_set_element_handler($xml_parser, "startElement", "endElement");
   if (!($fp = fopen($file, "r"))) {
       die("could not open XML input");
   }
   
   while ($data = fread($fp, 4096)) {
       if (!xml_parse($xml_parser, $data, feof($fp))) {
           die(sprintf("XML error: %s at line %d",
                       xml_error_string(xml_get_error_code($xml_parser)),
                       xml_get_current_line_number($xml_parser)));
       }
   }
   xml_parser_free($xml_parser);
   ?>

See also `XML Parser <http://www.php.net/manual/en/book.xml.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxml                                                                                                                                                                       |
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


