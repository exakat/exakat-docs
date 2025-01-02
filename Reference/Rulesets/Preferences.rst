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

* :ref:`true-false-inconsistant-case`
* :ref:`echo-or-print`
* :ref:`constant-comparison`
* :ref:`die-exit-consistence`
* :ref:`array()---[--]-consistence`
* :ref:`$globals-or-global`
* :ref:`unset()-or-(unset)`
* :ref:`close-tags-consistency`
* :ref:`one-expression-brackets-consistency`
* :ref:`new-on-functioncall-or-identifier`
* :ref:`new-line-style`
* :ref:`regex-delimiter`
* :ref:`empty-final-element-in-array`
* :ref:`difference-consistence`
* :ref:`concatenation-interpolation-consistence`
* :ref:`heredoc-delimiter`
* :ref:`strict\_types-preference`
* :ref:`declare-strict\_types-usage`
* :ref:`encoding-usage`
* :ref:`ticks-usage`
* :ref:`logical-operators-favorite`
* :ref:`shell-favorite`
* :ref:`properties-declaration-consistence`
* :ref:`strict-or-relaxed-comparison`
* :ref:`comparisons-orientation`
* :ref:`const-or-define-preference`
* :ref:`constant-case-preference`
* :ref:`caught-variable`
* :ref:`not-or-tilde`
* :ref:`null-type-favorite`
* :ref:`string-interpolation-favorite`
* :ref:`constant--with-or-without-use`
* :ref:`if-then-return-favorite`
* :ref:`empty-array-detection`
* :ref:`strict-in\_array()-preference`
* :ref:`date()-versus-datetime-preference`
* :ref:`mono-or-multibytes-favorite`
* :ref:`short-or-complete-comparison`
* :ref:`favorite-casting-method`
* :ref:`is\_a()-versus-instanceof`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Preferences                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-ambassador`, :ref:`report-diplomat`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


