.. _report-compatibilityphp82:

CompatibilityPHP82
++++++++++++++++++

CompatibilityPHP82
__________________

.. meta::
	:description:
		CompatibilityPHP82: The CompatibilityPHP82 report list all detected issues with PHP 8.2 compatibility..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CompatibilityPHP82
	:twitter:description: CompatibilityPHP82: The CompatibilityPHP82 report list all detected issues with PHP 8.2 compatibility.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CompatibilityPHP82
	:og:type: article
	:og:description: The CompatibilityPHP82 report list all detected issues with PHP 8.2 compatibility.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The CompatibilityPHP82 report list all detected issues with PHP 8.2 compatibility.

The CompatibilityPHP82 report displays one result per line, grouped by rule, and ordered by file and line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review. It is the same format as PerRule. 



::

    ----------------------------------------------------------------------------------------------------
     Checks Property Existence (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#classes-checkspropertyexistence)
    ----------------------------------------------------------------------------------------------------
     /app/Domain/Service/Project/ProjectIssue/Update.php:31       isset($params->tags)                    
     /app/Domain/Service/Project/ProjectIssue/Update.php:35       isset($params->releases)                
     /app/Domain/Service/Project/ProjectIssue/Update.php:39       isset($params->modules)                 
     /app/Domain/Service/Project/ProjectIssue/Update.php:43       isset($params->content)                 
     /app/Domain/Service/Project/ProjectIssue/Update.php:47       isset($params->completed)               
     /app/Domain/Service/Project/ProjectIssue/Update.php:49       isset($params->completedDate)           
     /app/Domain/Service/Project/ProjectRelease/UpdateParams.php:42 isset($this->completedDate)             
    ----------------------------------------------------------------------------------------------------
    
    
    ----------------------------------------------------------------------------------------------------
     Undefined Properties (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#classes-undefinedproperty)
    ----------------------------------------------------------------------------------------------------
     /app/Controller/Api/V1/Attachment/Upload.php:36              $request->files                         
     /app/Controller/Api/V1/Login/Code.php:39                     $request->query                         
     /app/Controller/BaseBrand.php:103                            $this->in                               
     /app/Controller/BaseBrand.php:115                            $this->in                               
     /app/Controller/BaseBrand.php:120                            $this->in                               
     /app/Controller/BaseBrand.php:132                            $this->in                               
     /app/Controller/BaseBrand.php:137                            $this->in                               
     ----------------------------------------------------------------------------------------------------
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | CompatibilityPHP82                                               |
+--------------+------------------------------------------------------------------+
| Rulesets     | CompatibilityPHP82.                                              |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                              |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


