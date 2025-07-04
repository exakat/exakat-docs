.. _Rulesets:

Rulesets
====================

Introduction
------------------------

Exakat provides unique {{ANALYZERS_COUNT}} rules to detect BUGS, CODE SMELLS, SECURITY OR QUALITY ISSUES in your PHP code.

For more smoothly usage, the ruleset concept allow you to run a set of rules based on a decidated focus. Beawre that a Ruleset run all the associated rules and any needed dependencies.

Rulesets are configured with the -T option, when running exakat in command line. For example : 

::

   php exakat.phar analyze -p <project> -T <Security>



Summary
------------------------


Here is the list of the current rulesets supported by Exakat Engine.

{{RULESETS_TABLE}}

Note : in command line, don't forget to add quotes to rulesets' names that include white space.

List of rulesets
------------------------

{{RULESETS_DETAILS}}
