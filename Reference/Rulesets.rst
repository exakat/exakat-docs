.. _Rulesets:

Rulesets
====================

Introduction
------------------------

Exakat provides unique 1678 rules to detect BUGS, CODE SMELLS, SECURITY OR QUALITY ISSUES in your PHP code.

For more smoothly usage, the ruleset concept allow you to run a set of rules based on a decidated focus. Beawre that a Ruleset run all the associated rules and any needed dependencies.

Rulesets are configured with the -T option, when running exakat in command line. For example : 

::

   php exakat.phar analyze -p <project> -T <Security>



Summary
------------------------


Here is the list of the current rulesets supported by Exakat Engine.

+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
|Name                                           | Description                                                                                          |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-all`                            |All is a dummy ruleset, which includes all the rules.                                                 |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-analyze`                        |Check for common best practices.                                                                      |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-appinfo`                        |Appinfo is the equivalent of phpinfo() for your code.                                                 |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-attributes`                     |This ruleset gathers all rules that rely on PHP 8.+ attributes.                                       |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-ce`                             |List of rules that are part of the Community Edition                                                  |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-ci-checks`                      |Quick check for common best practices.                                                                |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-changed-behavior`               |Ruleset with all rules that identify changed behavior across PHP versions.                            |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-class-review`                   |A set of rules dedicated to class hygiene                                                             |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-classdependencies`              |A set of rules dedicated to show classes dependences                                                  |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-coding-conventions`             |List coding conventions violations.                                                                   |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp53`             |List features that are incompatible with PHP 5.3.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp54`             |List features that are incompatible with PHP 5.4.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp55`             |List features that are incompatible with PHP 5.5.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp56`             |List features that are incompatible with PHP 5.6.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp70`             |List features that are incompatible with PHP 7.0.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp71`             |List features that are incompatible with PHP 7.1.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp72`             |List features that are incompatible with PHP 7.2.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp73`             |List features that are incompatible with PHP 7.3.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp74`             |List features that are incompatible with PHP 7.4.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp80`             |List features that are incompatible with PHP 8.0.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp81`             |List features that are incompatible with PHP 8.1.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp82`             |List features that are incompatible with PHP 8.2.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp83`             |List features that are incompatible with PHP 8.3.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp84`             |List features that are incompatible with PHP 8.4.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-compatibilityphp85`             |List features that are incompatible with PHP 8.5.                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-dead-code`                      |Check the unused code or unreachable code.                                                            |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-deprecated`                     |List of deprecated features, across all PHP versions.                                                 |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-dump`                           |Dump is a collector set of rules.                                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-first`                          |A set of rules that are always run at the beginning of a project, because they are frequently used.   |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-inventory`                      |A set of rules that collect various definitions from the code                                         |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-isext`                          |Ruleset with analysis which rely on PHP's optional extensions                                         |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-isphp`                          |Ruleset with analysis which rely on PHP's core extensions                                             |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-isstub`                         |Ruleset with analysis which rely on custom stubs                                                      |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-lintbutwontexec`                |Check the code for common errors that will lead to a Fatal error on production, but lint fine.        |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-nodoc`                          |Ruleset with analysis which are not published in the docs.                                            |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-one-liners`                     |Report expressions that are one liners.                                                               |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-php-recommendations`            |Report recommendations from the PHP manual.                                                           |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-php-recommendations`            |Report recommendations from the PHP manual.                                                           |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-php9deprecations`               |Check the code for the depreciations that will happen in PHP 9.                                       |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-performances`                   |Check the code for slow code.                                                                         |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-preferences`                    |Identify preferences in the code.                                                                     |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-rector`                         |Suggests configuration to apply changes with Rector                                                   |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-security`                       |Check the code for common security bad practices, especially in the Web environnement.                |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-semantics`                      |Checks the meanings found the names of the code.                                                      |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-suggestions`                    |List of possible modernisation of the PHP code.                                                       |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-surprising`                     |A ruleset dedicated to surprising pieces of code in PHP.                                              |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-top10`                          |The most common issues found in the code                                                              |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-typechecks`                     |Checks related to types.                                                                              |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+
| :ref:`ruleset-php-cs-fixable`                 |Suggests configuration to apply changes with PHP-CS-FIXER                                             |
+-----------------------------------------------+------------------------------------------------------------------------------------------------------+

Note : in command line, don't forget to add quotes to rulesets' names that include white space.

List of rulesets
------------------------

.. toctree::
   :maxdepth: 1

   Rulesets/All.rst
   Rulesets/Analyze.rst
   Rulesets/Appinfo.rst
   Rulesets/Attributes.rst
   Rulesets/CE.rst
   Rulesets/CI-checks.rst
   Rulesets/ChangedBehavior.rst
   Rulesets/ClassReview.rst
   Rulesets/Classdependencies.rst
   Rulesets/Coding Conventions.rst
   Rulesets/CompatibilityPHP53.rst
   Rulesets/CompatibilityPHP54.rst
   Rulesets/CompatibilityPHP55.rst
   Rulesets/CompatibilityPHP56.rst
   Rulesets/CompatibilityPHP70.rst
   Rulesets/CompatibilityPHP71.rst
   Rulesets/CompatibilityPHP72.rst
   Rulesets/CompatibilityPHP73.rst
   Rulesets/CompatibilityPHP74.rst
   Rulesets/CompatibilityPHP80.rst
   Rulesets/CompatibilityPHP81.rst
   Rulesets/CompatibilityPHP82.rst
   Rulesets/CompatibilityPHP83.rst
   Rulesets/CompatibilityPHP84.rst
   Rulesets/CompatibilityPHP85.rst
   Rulesets/Dead code.rst
   Rulesets/Deprecated.rst
   Rulesets/Dump.rst
   Rulesets/First.rst
   Rulesets/Inventory.rst
   Rulesets/IsExt.rst
   Rulesets/IsPHP.rst
   Rulesets/IsStub.rst
   Rulesets/LintButWontExec.rst
   Rulesets/NoDoc.rst
   Rulesets/OneLiners.rst
   Rulesets/PHP recommendations.rst
   Rulesets/Php recommendations.rst
   Rulesets/PHP9Deprecations.rst
   Rulesets/Performances.rst
   Rulesets/Preferences.rst
   Rulesets/Rector.rst
   Rulesets/Security.rst
   Rulesets/Semantics.rst
   Rulesets/Suggestions.rst
   Rulesets/Surprising.rst
   Rulesets/Top10.rst
   Rulesets/Typechecks.rst
   Rulesets/php-cs-fixable.rst
