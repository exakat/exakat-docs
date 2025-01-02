.. _ruleset-compatibilityphp74:

CompatibilityPHP74
++++++++++++++++++

.. meta::
	:description:
		CompatibilityPHP74: List features that are incompatible with PHP 7.4..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CompatibilityPHP74
	:twitter:description: CompatibilityPHP74: List features that are incompatible with PHP 7.4.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CompatibilityPHP74
	:og:type: article
	:og:description: List features that are incompatible with PHP 7.4.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/CompatibilityPHP74.html
	:og:locale: en
This ruleset centralizes all analysis for the migration from PHP 7.3 to 7.4.

Total : 55 analysis

* :ref:`detect-current-class`
* :ref:`don't-read-and-write-in-one-expression`
* :ref:`idn\_to\_ascii()-new-default`
* :ref:`concat-and-addition`
* :ref:`new-functions-in-php-7.4`
* :ref:`curl\_version()-has-no-argument`
* :ref:`php-7.4-new-classes`
* :ref:`new-constants-in-php-7.4`
* :ref:`php-7.4-removed-functions`
* :ref:`mb\_strrpos()-third-argument`
* :ref:`array\_key\_exists()-works-on-arrays`
* :ref:`reflection-export()-is-deprecated`
* :ref:`unbinding-closures`
* :ref:`scalar-are-not-arrays`
* :ref:`php-7.4-reserved-keyword`
* :ref:`no-more-curly-arrays`
* :ref:`php-7.4-constant-deprecation`
* :ref:`php-7.4-removed-directives`
* :ref:`hash-algorithms-incompatible-with-php-7.4-`
* :ref:`openssl\_random\_pseudo\_byte()-second-argument`
* :ref:`nested-ternary-without-parenthesis`
* :ref:`filter-to-add\_slashes()`
* :ref:`php-8.0-variable-syntax-tweaks`
* :ref:`new-functions-in-php-8.0`
* :ref:`php-8.0-only-typehints`
* :ref:`union-typehint`
* :ref:`signature-trailing-comma`
* :ref:`throw-was-an-expression`
* :ref:`uses-php-8-match()`
* :ref:`avoid-get\_object\_vars()`
* :ref:`enum-usage`
* :ref:`$files-full\_path`
* :ref:`final-constant`
* :ref:`never-typehint-usage`
* :ref:`php-8.1-typehints`
* :ref:`php-8.0-typehints`
* :ref:`named-parameter-usage`
* :ref:`nested-attributes`
* :ref:`new-initializers`
* :ref:`cant-overload-constants`
* :ref:`no-private-abstract-method-in-trait`
* :ref:`clone-constant`
* :ref:`no-keyword-in-namespace`
* :ref:`constants-in-traits`
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

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | CompatibilityPHP74                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-diplomat`, :ref:`report-ambassador`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


