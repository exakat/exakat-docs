.. _extensions-extxsl:

.. _ext-xsl:

ext/xsl
+++++++

.. meta::
	:description:
		ext/xsl: Extension XSL.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xsl
	:twitter:description: ext/xsl: Extension XSL
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xsl
	:og:type: article
	:og:description: Extension XSL
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extxsl.html
	:og:locale: en
Extension XSL.

The XSL extension implements the XSL standard, performing XSLT transformations using the libxslt library.

.. code-block:: php
   
   <?php
   
   // Example from the PHP manual
   
   $xmldoc = new DOMDocument();
   $xsldoc = new DOMDocument();
   $xsl = new XSLTProcessor();
   
   $xmldoc->loadXML('fruits.xml');
   $xsldoc->loadXML('fruits.xsl');
   
   libxml_use_internal_errors(true);
   $result = $xsl->importStyleSheet($xsldoc);
   if (!$result) {
       foreach (libxml_get_errors() as $error) {
           echo "Libxml error: {$error->message}\n";
       }
   }
   libxml_use_internal_errors(false);
   
   if ($result) {
       echo $xsl->transformToXML($xmldoc);
   }
   
   ?>

See also `XSL extension <https://www.php.net/manual/en/intro.xsl.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxsl                                                                                                                                                                       |
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


