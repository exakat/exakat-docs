.. _Rules:

Rules
====================

Introduction
------------------------

Exakat provides unique {{ANALYZERS_COUNT}} rules to detect BUGS, CODE SMELLS, SECURITY OR QUALITY ISSUES in your PHP code.

Each rule is documented with code example to allow you to remediate your code. If you want to automate remediation, ours cobblers can are there to fix the issues in your code for your.  

List of Rules
-------------------------


{{RULES_DETAILS}}


Directory by Exakat version
-----------------------------

List of analyzers, by version of introduction, newest to oldest. In parenthesis, the first element is the analyzer name, used with 'analyze -P' command, and the seconds, if any, are the ruleset, used with the -T option. Rulesets are separated by commas, as the same analysis may be used in several rulesets.

{{ANALYZER_INTRODUCTION}}

Directory by PHP Function
-------------------------

{{GLOSSARY}}


Directory by PHP Features
-------------------------

Exakat links each rules to PHP features.

{{RULES_PER_FEATURE}}


Directory by PHP Error message
------------------------------

Exakat helps reduce the amount of error and warning that code is producing by reporting pattern that are likely to emit errors.

{{PHP_ERROR_MESSAGES}}


Directory by Exception
----------------------

Exakat has rules that help identify possible exceptions in the code.

{{RULES_PER_EXCEPTION}}
