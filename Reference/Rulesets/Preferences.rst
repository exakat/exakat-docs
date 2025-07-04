.. _ruleset-preferences:

Preferences
+++++++++++

.. meta::
	:description:
		Preferences: Identify preferences in the code..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Preferences
	:twitter:description: Preferences: Identify preferences in the code.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Preferences
	:og:type: article
	:og:description: Identify preferences in the code.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/Preferences.html
	:og:locale: en

This ruleset identify code with multiple forms, and report when one is more frequent than the others. Echo vs print, shell_exec() vs ``, etc.

Total : 40 analysis

* :ref:`constants-inconsistantcase`
* :ref:`structures-echoprintconsistance`
* :ref:`structures-constantcomparisonconsistance`
* :ref:`structures-dieexitconsistance`
* :ref:`arrays-arraybracketconsistence`
* :ref:`php-globalsvsglobal`
* :ref:`php-unsetorcast`
* :ref:`php-closetagsconsistency`
* :ref:`structures-oneexpressionbracketsconsistency`
* :ref:`classes-newonfunctioncalloridentifier`
* :ref:`structures-newlinestyle`
* :ref:`structures-regexdelimiter`
* :ref:`arrays-emptyfinal`
* :ref:`structures-differencepreference`
* :ref:`structures-concatenationinterpolationfavorite`
* :ref:`structures-heredocdelimiterfavorite`
* :ref:`php-declarestrict`
* :ref:`php-declarestricttype`
* :ref:`php-declareencoding`
* :ref:`php-declareticks`
* :ref:`php-lettercharslogicalfavorite`
* :ref:`php-shellfavorite`
* :ref:`classes-pppdeclarationstyle`
* :ref:`structures-comparisonfavorite`
* :ref:`structures-gtorltfavorite`
* :ref:`constants-constdefinepreference`
* :ref:`constants-defineinsensitivepreference`
* :ref:`exceptions-catche`
* :ref:`structures-notornot`
* :ref:`functions-nulltypefavorite`
* :ref:`structures-stringinterpolationfavorite`
* :ref:`namespaces-constantwithusefavorite`
* :ref:`structures-ifthenreturnfavorite`
* :ref:`structures-arraycounttripleequal`
* :ref:`structures-strictinarrayfavorite`
* :ref:`structures-datetimepreference`
* :ref:`structures-strormbfavorite`
* :ref:`structures-shortorcompletecomparison`
* :ref:`structures-castfavorite`
* :ref:`structures-isaversusinstanceof`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Preferences                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-ambassador`, :ref:`report-diplomat`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


