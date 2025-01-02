.. _report-compatibilityphp74:

CompatibilityPHP74
++++++++++++++++++

CompatibilityPHP74
__________________

.. meta::
	:description:
		CompatibilityPHP74: The CompatibilityPHP74 report list all detected issues with PHP 7.4 compatibility..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CompatibilityPHP74
	:twitter:description: CompatibilityPHP74: The CompatibilityPHP74 report list all detected issues with PHP 7.4 compatibility.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CompatibilityPHP74
	:og:type: article
	:og:description: The CompatibilityPHP74 report list all detected issues with PHP 7.4 compatibility.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The CompatibilityPHP74 report list all detected issues with PHP 7.4 compatibility.

The CompatibilityPHP74 report displays one result per line, grouped by rule, and ordered by file and line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review. It is the same format as PerRule. 



::

    ----------------------------------------------------------------------------------------------------
     PHP 7.4 Removed Functions (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-php74removedfunctions)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/ID3/getid3.php:443                          get_magic_quotes_runtime( )             
    ----------------------------------------------------------------------------------------------------
    
    ----------------------------------------------------------------------------------------------------
     idn_to_ascii() New Default (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-idnuts46)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/PHPMailer/PHPMailer.php:1468                idn_to_ascii($domain, $errorcode)       
    ----------------------------------------------------------------------------------------------------
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | CompatibilityPHP74                                               |
+--------------+------------------------------------------------------------------+
| Rulesets     | CompatibilityPHP74.                                              |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                              |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


