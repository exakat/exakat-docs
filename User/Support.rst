.. Support:

Library & Framework Support
============================

Summary
----------------------------------

* Supported Rulesets
* Supported Reports
* Supported PHP Extensions
* Applications
* Recognized Libraries
* New analyzers
* External services
* PHP Error messages
* Exakat Changelog

External Library Support
----------------------------------

Libraries that are popular, large and often included in repositories are identified early in the analysis process, and ignored. This prevents Exakat to analysis some code foreign to the current repository : it prevents false positives from this code, and make the analysis much lighter. The whole process is entirely automatic. 

Those libraries, or even some of the, may be included again in the analysis by commenting the ignored_dir[] line, in the projects/<project>/config.ini file. 

{{LIBRARY_LIST}}

External Services Support
----------------------------------


List of external services whose configuration files has been commited in the code.

{{EXTERNAL_SERVICES_LIST}}

Supported PHP Extensions
------------------------

PHP extensions are used to check for structures usage (classes, interfaces, etc.), to identify dependencies and directives. 

PHP extensions are described with the list of structures they define : functions, classes, constants, traits, variables, interfaces, namespaces, and directives. 

{{PHP_EXTENSION_LIST}}