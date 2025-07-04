.. _extensions-extgender:


.. _ext-gender:

ext/gender
++++++++++

.. meta::
	:description:
		ext/gender: Gender extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gender
	:twitter:description: ext/gender: Gender extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gender
	:og:type: article
	:og:description: Gender extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/gender.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgender.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgender.html","name":"ext\/gender","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Gender extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/gender.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


