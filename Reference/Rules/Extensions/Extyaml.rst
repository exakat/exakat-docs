.. _extensions-extyaml:


.. _ext-yaml:

ext/yaml
++++++++


.. meta::

	:description:

		ext/yaml: Extension YAML.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/yaml

	:twitter:description: ext/yaml: Extension YAML

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/yaml

	:og:type: article

	:og:description: Extension YAML

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/yaml.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extyaml.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extyaml.html","name":"ext\/yaml","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension YAML","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/yaml.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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


