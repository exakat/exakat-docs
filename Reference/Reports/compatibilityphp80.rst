.. _report-compatibilityphp80:

CompatibilityPHP80
++++++++++++++++++

CompatibilityPHP80
__________________

.. meta::
	:description:
		CompatibilityPHP80: The CompatibilityPHP80 report list all detected issues with PHP 8.0 compatibility..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CompatibilityPHP80
	:twitter:description: CompatibilityPHP80: The CompatibilityPHP80 report list all detected issues with PHP 8.0 compatibility.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CompatibilityPHP80
	:og:type: article
	:og:description: The CompatibilityPHP80 report list all detected issues with PHP 8.0 compatibility.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The CompatibilityPHP80 report list all detected issues with PHP 8.0 compatibility.

The CompatibilityPHP80 report displays one result per line, grouped by rule, and ordered by file and line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review. It is the same format as PerRule. 



::

    
    ----------------------------------------------------------------------------------------------------
     PHP 8.0 Resources Turned Into Objects (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-php80removesresources)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/Requests/Transport/cURL.php:116             is_resource($this->handle)              
    ----------------------------------------------------------------------------------------------------
    
    
    ----------------------------------------------------------------------------------------------------
     PHP 80 Named Parameter Variadic (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-php80namedparametervariadic)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/capabilities.php:44                         function map_meta_cap($cap, $user_id, ...$args) { /**/ } 
     /src/wp-includes/class-wp-walker.php:286                     public function paged_walk($elements, $max_depth, $page_num, $per_page, ...$args) { /**/ } 
     /src/wp-includes/functions.php:1108                          function add_query_arg(...$args) { /**/ } 
     /src/wp-includes/plugin.php:439                              function do_action($hook_name, ...$arg) { /**/ } 
     /src/wp-includes/theme.php:2568                              function add_theme_support($feature, ...$args) { /**/ } 
     /src/wp-includes/theme.php:2899                              function get_theme_support($feature, ...$args) { /**/ } 
     /src/wp-includes/theme.php:3029                              function current_theme_supports($feature, ...$args) { /**/ } 
     /src/wp-includes/wp-db.php:1395                              public function prepare($query, ...$args) { /**/ } 
    ----------------------------------------------------------------------------------------------------
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | CompatibilityPHP80                                               |
+--------------+------------------------------------------------------------------+
| Rulesets     | CompatibilityPHP80.                                              |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                              |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


