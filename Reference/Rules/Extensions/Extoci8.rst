.. _extensions-extoci8:

.. _ext-oci8:

ext/oci8
++++++++

.. meta::
	:description:
		ext/oci8: Extension ext/oci8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/oci8
	:twitter:description: ext/oci8: Extension ext/oci8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/oci8
	:og:type: article
	:og:description: Extension ext/oci8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/oci8.html
	:og:locale: en
Extension ext/oci8.

OCI8 gives access Oracle Database 12c, 11g, 10g, 9i and 8i.

.. code-block:: php
   
   <?php
   
   $conn = oci_connect('hr', 'welcome', 'localhost/XE');
   if (!$conn) {
       $e = oci_error();
       trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
   }
   
   // Prepare the statement
   $stid = oci_parse($conn, 'SELECT * FROM departments');
   if (!$stid) {
       $e = oci_error($conn);
       trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
   }
   
   // Perform the logic of the query
   $r = oci_execute($stid);
   if (!$r) {
       $e = oci_error($stid);
       trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
   }
   
   // Fetch the results of the query
   print '<table border='1'>' . PHP_EOL;
   while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
       print '<tr>' . PHP_EOL;
       foreach ($row as $item) {
           print '    <td>' . ($item !== null ? htmlentities($item, ENT_QUOTES) : '&nbsp;') . '</td>' . PHP_EOL;
       }
       print '</tr>' . PHP_EOL;
   }
   print '</table>' . PHP_EOL;
   
   oci_free_statement($stid);
   oci_close($conn);
   
   ?>

See also `Oracle OCI8 <https://www.php.net/manual/en/book.oci8.php>`_ and `Oracle <https://www.oracle.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extoci8                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


