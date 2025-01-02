.. _ruleset-compatibilityphp54:

CompatibilityPHP54
++++++++++++++++++

.. meta::
	:description:
		CompatibilityPHP54: List features that are incompatible with PHP 5.4..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CompatibilityPHP54
	:twitter:description: CompatibilityPHP54: List features that are incompatible with PHP 5.4.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CompatibilityPHP54
	:og:type: article
	:og:description: List features that are incompatible with PHP 5.4.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/CompatibilityPHP54.html
	:og:locale: en
This ruleset centralizes all analysis for the migration from PHP 5.3 to 5.4.

Total : 95 analysis

* :ref:`non-static-methods-called-in-a-static`
* :ref:`use-lower-case-for-parent,-static-and-self`
* :ref:`functions-removed-in-php-5.4`
* :ref:`break-with-non-integer`
* :ref:`calltime-pass-by-reference`
* :ref:`malformed-octal`
* :ref:`new-functions-in-php-5.5`
* :ref:`new-functions-in-php-5.6`
* :ref:`multiple-definition-of-the-same-argument`
* :ref:`switch-with-too-many-default`
* :ref:`crypt()-without-salt`
* :ref:`ellipsis-usage`
* :ref:`exponent-usage`
* :ref:`dereferencing-string-and-arrays`
* :ref:`class`
* :ref:`foreach-with-list()`
* :ref:`use-const-and-functions`
* :ref:`constant-scalar-expressions`
* :ref:`\_\_debuginfo()-usage`
* :ref:`mixed-keys-in-array`
* :ref:`const-with-array`
* :ref:`hash-algorithms-incompatible-with-php-5.3`
* :ref:`hash-algorithms-incompatible-with-php-5.4-5.5`
* :ref:`class-const-with-array`
* :ref:`variable-global`
* :ref:`null-on-new`
* :ref:`isset()-with-constant`
* :ref:`anonymous-classes`
* :ref:`unicode-escape-syntax`
* :ref:`new-functions-in-php-7.0`
* :ref:`php-7.0-new-classes`
* :ref:`php-7.0-new-interfaces`
* :ref:`parenthesis-as-parameter`
* :ref:`php5-indirect-variable-expression`
* :ref:`php-7-indirect-expression`
* :ref:`unicode-escape-partial`
* :ref:`define-constants-with-array`
* :ref:`no-list-with-string`
* :ref:`php7-dirname`
* :ref:`php7-relaxed-keyword`
* :ref:`cant-use-return-value-in-write-context`
* :ref:`php-7.1-new-class`
* :ref:`list-with-keys`
* :ref:`list-short-syntax`
* :ref:`use-nullable-type`
* :ref:`multiple-exceptions-catch()`
* :ref:`no-string-with-append`
* :ref:`group-use-declaration`
* :ref:`new-functions-in-php-7.3`
* :ref:`cant-inherit-abstract-method`
* :ref:`group-use-trailing-comma`
* :ref:`child-class-removes-typehint`
* :ref:`no-substr-minus-one`
* :ref:`integer-as-property`
* :ref:`no-get\_class()-with-null`
* :ref:`php-7.2-new-class`
* :ref:`list-with-reference`
* :ref:`php-7.3-last-empty-argument`
* :ref:`flexible-heredoc`
* :ref:`const-visibility-usage`
* :ref:`hash-algorithms-incompatible-with-php-7.1-`
* :ref:`php-7.0-scalar-typehints`
* :ref:`php-7.1-scalar-typehints`
* :ref:`php-7.2-scalar-typehints`
* :ref:`continue-is-for-loop`
* :ref:`trailing-comma-in-calls`
* :ref:`direct-call-to-\_\_clone()`
* :ref:`no-return-for-generator`
* :ref:`no-reference-for-static-property`
* :ref:`typed-property-usage`
* :ref:`concat-and-addition`
* :ref:`unpacking-inside-arrays`
* :ref:`generator-cannot-return`
* :ref:`coalesce-equal`
* :ref:`enum-usage`
* :ref:`$files-full\_path`
* :ref:`never-typehint-usage`
* :ref:`php-8.1-typehints`
* :ref:`php-8.0-typehints`
* :ref:`named-parameter-usage`
* :ref:`cant-overload-constants`
* :ref:`constant-scalar-expression`
* :ref:`no-private-abstract-method-in-trait`
* :ref:`clone-constant`
* :ref:`use-enum-case-in-constant-expression`
* :ref:`readonly-property-changed-by-cloning`
* :ref:`new-dynamic-class-constant-syntax`
* :ref:`class\_alias()-supports-internal-classes`
* :ref:`redeclared-static-variable`
* :ref:`static-variable-can-default-to-arbitrary-expression`
* :ref:`final-traits-are-final`
* :ref:`typed-class-constants-usage`
* :ref:`void-is-not-a-reference`
* :ref:`php-8.1-new-types`
* :ref:`php-8.2-new-types`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | CompatibilityPHP54                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-ambassador`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


