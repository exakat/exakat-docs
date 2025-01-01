.. _extensions-extlibxml:

.. _ext-libxml:

ext/libxml
++++++++++

.. meta::
	:description:
		ext/libxml: Extension libxml.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/libxml
	:twitter:description: ext/libxml: Extension libxml
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/libxml
	:og:type: article
	:og:description: Extension libxml
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extlibxml.html
	:og:locale: en
Extension libxml.

These functions/constants are available as of PHP 5.1.0, and the following core extensions rely on this libxml extension: DOM, libxml, SimpleXML, SOAP, WDDX, XSL, XML, `XMLReader <https://www.php.net/xmlreader>`_, XMLRPC and `XMLWriter <https://www.php.net/xmlwriter>`_.

.. code-block:: php
   
   <?php
   
   // $xmlstr is a string, containing a XML document. 
   
   $doc = simplexml_load_string($xmlstr);
   $xml = explode(PHP_EOL, $xmlstr);
   
   if ($doc === false) {
       $errors = libxml_get_errors();
   
       foreach ($errors as $error) {
           echo display_xml_error($error, $xml);
       }
   
       libxml_clear_errors();
   }
   
   
   function display_xml_error($error, $xml)
   {
       $return  = $xml[$error->line - 1] . PHP_EOL;
       $return .= str_repeat('-', $error->column) . '^'.PHP_EOL;
   
       switch ($error->level) {
           case LIBXML_ERR_WARNING:
               $return .= 'Warning ',$error->code.': ';
               break;
            case LIBXML_ERR_ERROR:
               $return .= 'Error '.$error->code.': ';
               break;
           case LIBXML_ERR_FATAL:
               $return .= 'Fatal Error '.$error->code.': ';
               break;
       }
   
       $return .= trim($error->message) .
                  PHP_EOL.'  Line: '.$error->line .
                  PHP_EOL.'  Column: '.$error->column;
   
       if ($error->file) {
           $return .= "\n  File: $error->file";
       }
   
       return $return.PHP_EOL.PHP_EOL.'--------------------------------------------'.PHP_EOL.PHP_EOL;
   }
   
   ?>

See also `libxml <http://www.php.net/manual/en/book.libxml.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extlibxml                                                                                                                                                                    |
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


