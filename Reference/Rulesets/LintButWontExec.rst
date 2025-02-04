.. _ruleset-lintbutwontexec:

LintButWontExec
+++++++++++++++

.. meta::
	:description:
		LintButWontExec: Check the code for common errors that will lead to a Fatal error on production, but lint fine..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: LintButWontExec
	:twitter:description: LintButWontExec: Check the code for common errors that will lead to a Fatal error on production, but lint fine.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: LintButWontExec
	:og:type: article
	:og:description: Check the code for common errors that will lead to a Fatal error on production, but lint fine.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/LintButWontExec.html
	:og:locale: en

This ruleset focuses on PHP code that lint (php -l), but that will not run. As such, this ruleset tries to go further than PHP, by connecting files, just like during execution.

Total : 48 analysis

* :ref:`classes-finalclass`
* :ref:`classes-finalmethod`
* :ref:`classes-thisisforclasses`
* :ref:`classes-mutualextension`
* :ref:`classes-undefinedconstants`
* :ref:`functions-mustreturn`
* :ref:`interfaces-undefinedinterfaces`
* :ref:`classes-noselfreferencingconstant`
* :ref:`classes-usingthisoutsideaclass`
* :ref:`traits-undefinedtrait`
* :ref:`classes-raisedaccesslevel`
* :ref:`classes-nopssoutsideclass`
* :ref:`classes-implementedmethodsarepublic`
* :ref:`classes-nomagicwitharray`
* :ref:`classes-methodsignaturemustbecompatible`
* :ref:`functions-mismatchtypeanddefault`
* :ref:`exceptions-cantthrow`
* :ref:`classes-abstractorimplements`
* :ref:`classes-incompatiblesignature`
* :ref:`traits-undefinedinsteadof`
* :ref:`traits-methodcollisiontraits`
* :ref:`functions-onlyvariableforreference`
* :ref:`interfaces-repeatedinterface`
* :ref:`interfaces-avoidselfininterface`
* :ref:`traits-uselessalias`
* :ref:`functions-typehintmustbereturned`
* :ref:`classes-clonewithnonobject`
* :ref:`traits-traitnotfound`
* :ref:`functions-wrongreturnedtype`
* :ref:`interfaces-isnotimplemented`
* :ref:`interfaces-cantimplementtraversable`
* :ref:`classes-wrongtypedpropertyinit`
* :ref:`classes-mismatchproperties`
* :ref:`classes-couldbestringable`
* :ref:`classes-inheritedpropertymustmatch`
* :ref:`functions-duplicatenamedparameter`
* :ref:`php-jsonserializereturntype`
* :ref:`php-falsetoarray`
* :ref:`functions-deprecatedcallable`
* :ref:`interfaces-cantoverloadconstants`
* :ref:`classes-cantoverwritefinalconstant`
* :ref:`structures-implicitconversiontoint`
* :ref:`enums-nomagicmethod`
* :ref:`typehints-wrongtypewithdefault`
* :ref:`php-cloneconstant`
* :ref:`structures-invalidcast`
* :ref:`php-onlyvariablepassedbyreference`
* :ref:`enums-duplicatecasevalue`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | LintButWontExec                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


