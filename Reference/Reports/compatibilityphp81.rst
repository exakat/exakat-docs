.. _report-compatibilityphp81:

CompatibilityPHP81
++++++++++++++++++

CompatibilityPHP81
__________________

The CompatibilityPHP56 report list all detected issues with PHP 8.1 compatibility.

The CompatibilityPHP81 report displays one result per line, grouped by rule, and ordered by file and line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review. It is the same format as PerRule. 



::

    
    ----------------------------------------------------------------------------------------------------
     PHP 8.1 Removed Directives (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-php81removeddirective)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/pomo/po.php:24                              @ini_set('auto_detect_line_endings', 1) 
    ----------------------------------------------------------------------------------------------------
    
    
    ----------------------------------------------------------------------------------------------------
     PHP Native Class Type Compatibility (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-nativeclasstypecompatibility)
    ----------------------------------------------------------------------------------------------------
     /src/wp-includes/Requests/Cookie/Jar.php:102                 public function offsetUnset($key) { /**/ } 
     /src/wp-includes/Requests/Cookie/Jar.php:63                  public function offsetExists($key) { /**/ } 
     /src/wp-includes/Requests/Cookie/Jar.php:73                  public function offsetGet($key) { /**/ } 
     /src/wp-includes/Requests/Cookie/Jar.php:89                  public function offsetSet($key, $value) { /**/ } 
     /src/wp-includes/Requests/Response/Headers.php:26            public function offsetGet($key) { /**/ } 
     /src/wp-includes/Requests/Response/Headers.php:43            public function offsetSet($key, $value) { /**/ } 
     /src/wp-includes/Requests/Utility/CaseInsensitiveDictionary.php:40 public function offsetExists($key) { /**/ } 
     /src/wp-includes/Requests/Utility/CaseInsensitiveDictionary.php:51 public function offsetGet($key) { /**/ } 
     /src/wp-includes/Requests/Utility/CaseInsensitiveDictionary.php:68 public function offsetSet($key, $value) { /**/ } 
     /src/wp-includes/Requests/Utility/CaseInsensitiveDictionary.php:82 public function offsetUnset($key) { /**/ } 
     /src/wp-includes/Requests/Utility/FilteredIterator.php:40    public function current( ) { /**/ }     
     /src/wp-includes/Requests/Utility/FilteredIterator.php:53    public function unserialize($serialized) { /**/ } 
     /src/wp-includes/Requests/Utility/FilteredIterator.php:53    public function unserialize($serialized) { /**/ } 
     /src/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php:103 public function offsetGet($index) { /**/ } 
     /src/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php:114 public function offsetSet($index, $newval) { /**/ } 
     /src/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php:122 public function offsetUnset($index) { /**/ } 
     /src/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php:35 public function count( ) { /**/ }       
     /src/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php:94 public function offsetExists($index) { /**/ } 
    ----------------------------------------------------------------------------------------------------

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | CompatibilityPHP81                                               |
+--------------+------------------------------------------------------------------+
| Rulesets     | CompatibilityPHP81.                                              |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                              |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


