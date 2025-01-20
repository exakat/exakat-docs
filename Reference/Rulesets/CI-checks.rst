.. _ruleset-ci-checks:

CI-checks
+++++++++

.. meta::
	:description:
		CI-checks: Quick check for common best practices..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: CI-checks
	:twitter:description: CI-checks: Quick check for common best practices.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: CI-checks
	:og:type: article
	:og:description: Quick check for common best practices.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/CI-checks.html
	:og:locale: en
This ruleset is a collection of important rules to run in a CI pipeline.

Total : 177 analysis

* :ref:`adding-zero`
* :ref:`multiple-index-definition`
* :ref:`forgotten-visibility`
* :ref:`non-static-methods-called-in-a-static`
* :ref:`static-methods-called-from-object`
* :ref:`constants-with-strange-names`
* :ref:`redeclared-php-functions`
* :ref:`error\_reporting()-with-integers`
* :ref:`exit()-usage`
* :ref:`forgotten-whitespace`
* :ref:`multiply-by-one`
* :ref:`@-operator`
* :ref:`not-not`
* :ref:`strpos()-like-comparison`
* :ref:`throws-an-assignement`
* :ref:`var\_dump()...-usage`
* :ref:`useless-instructions`
* :ref:`multiple-constant-definition`
* :ref:`wrong-optional-parameter`
* :ref:`use-===-null`
* :ref:`one-variable-string`
* :ref:`static-methods-can't-contain-$this`
* :ref:`while(list()-=-each())`
* :ref:`multiples-identical-case`
* :ref:`switch-without-default`
* :ref:`nested-ternary`
* :ref:`undefined-constants`
* :ref:`htmlentities-calls`
* :ref:`undefined-class-constants`
* :ref:`undefined-functions`
* :ref:`deprecated-php-functions`
* :ref:`dangling-array-references`
* :ref:`native-alias-functions-usage`
* :ref:`uses-default-values`
* :ref:`wrong-number-of-arguments`
* :ref:`use-const`
* :ref:`list()-may-omit-variables`
* :ref:`or-die`
* :ref:`must-return-methods`
* :ref:`overwritten-exceptions`
* :ref:`foreach-reference-is-not-modified`
* :ref:`undefined-properties`
* :ref:`strict-comparison-with-booleans`
* :ref:`lone-blocks`
* :ref:`logical-should-use-symbolic-operators`
* :ref:`repeated-print()`
* :ref:`avoid-parenthesis-with-language-construct`
* :ref:`objects-don't-need-references`
* :ref:`no-real-comparison`
* :ref:`no-direct-call-to-magic-method`
* :ref:`useless-final`
* :ref:`use-constant-instead-of-function`
* :ref:`useless-unset`
* :ref:`no-array\_merge()-in-loops`
* :ref:`useless-parenthesis`
* :ref:`use-php-object-api`
* :ref:`altering-foreach-without-reference`
* :ref:`use-pathinfo`
* :ref:`no-parenthesis-for-language-construct`
* :ref:`use-constant-as-arguments`
* :ref:`implied-if`
* :ref:`should-chain-exception`
* :ref:`undefined-interfaces`
* :ref:`should-use-prepared-statement`
* :ref:`print-and-die`
* :ref:`unchecked-resources`
* :ref:`else-if-versus-elseif`
* :ref:`multiple-class-declarations`
* :ref:`empty-namespace`
* :ref:`could-use-short-assignation`
* :ref:`pre-increment`
* :ref:`indices-are-int-or-string`
* :ref:`should-typecast`
* :ref:`avoid-substr()-one`
* :ref:`useless-brackets`
* :ref:`preg\_replace-with-option-e`
* :ref:`eval()-without-try`
* :ref:`avoid-get\_class()`
* :ref:`silently-cast-integer`
* :ref:`timestamp-difference`
* :ref:`wrong-parameter-type`
* :ref:`redefined-class-constants`
* :ref:`redefined-default`
* :ref:`wrong-fopen()-mode`
* :ref:`negative-power`
* :ref:`use-random\_int()`
* :ref:`ternary-in-concat`
* :ref:`undefined-trait`
* :ref:`identical-conditions`
* :ref:`no-choice`
* :ref:`logical-mistakes`
* :ref:`same-conditions-in-condition`
* :ref:`return-true-false`
* :ref:`could-use-\_\_dir\_\_`
* :ref:`should-use-coalesce`
* :ref:`if-with-same-conditions`
* :ref:`throw-functioncall`
* :ref:`use-instanceof`
* :ref:`results-may-be-missing`
* :ref:`always-positive-comparison`
* :ref:`empty-blocks`
* :ref:`throw-in-destruct`
* :ref:`use-system-tmp`
* :ref:`hidden-use-expression`
* :ref:`should-make-alias`
* :ref:`multiple-identical-trait-or-interface`
* :ref:`multiple-alias-definitions`
* :ref:`failed-substr()-comparison`
* :ref:`should-use-ternary-operator`
* :ref:`drop-else-after-return`
* :ref:`use-class-operator`
* :ref:`don't-echo-error`
* :ref:`useless-type-casting`
* :ref:`no-isset()-with-empty()`
* :ref:`useless-check`
* :ref:`multiple-alias-definitions-per-file`
* :ref:`\_\_dir\_\_-then-slash`
* :ref:`repeated-regex`
* :ref:`no-class-in-global`
* :ref:`could-use-str\_repeat()`
* :ref:`strings-with-strange-space`
* :ref:`no-empty-regex`
* :ref:`no-reference-on-left-side`
* :ref:`assign-and-lettered-logical-operator-precedence`
* :ref:`no-magic-method-with-array`
* :ref:`is-actually-zero`
* :ref:`unconditional-break-in-loop`
* :ref:`next-month-trap`
* :ref:`printf-number-of-arguments`
* :ref:`invalid-regex`
* :ref:`same-variable-foreach`
* :ref:`identical-on-both-sides`
* :ref:`no-reference-for-ternary`
* :ref:`unused-inherited-variable-in-closure`
* :ref:`don't-unset-properties`
* :ref:`strtr-arguments`
* :ref:`missing-parenthesis`
* :ref:`callback-function-needs-return`
* :ref:`strpos()-too-much`
* :ref:`class-typed-references`
* :ref:`check-json`
* :ref:`undefined-static-class`
* :ref:`undefined-variable`
* :ref:`undefined-insteadof`
* :ref:`wrong-access-style-to-property`
* :ref:`invalid-pack-format`
* :ref:`should-yield-with-key`
* :ref:`useless-method-alias`
* :ref:`possible-missing-subpattern`
* :ref:`assign-and-compare`
* :ref:`type-must-be-returned`
* :ref:`check-on-\_\_call-usage`
* :ref:`casting-ternary`
* :ref:`concat-and-addition`
* :ref:`wrong-type-returned`
* :ref:`class-without-parent`
* :ref:`scalar-are-not-arrays`
* :ref:`implode()-arguments-order`
* :ref:`strip\_tags()-skips-closed-tag`
* :ref:`should-use-explode-args`
* :ref:`use-array\_slice()`
* :ref:`coalesce-and-concat`
* :ref:`interfaces-is-not-implemented`
* :ref:`no-literal-for-reference`
* :ref:`can't-implement-traversable`
* :ref:`is\_a()-with-string`
* :ref:`mbstring-unknown-encoding`
* :ref:`mbstring-third-arg`
* :ref:`merge-if-then`
* :ref:`wrong-type-with-call`
* :ref:`not-equal-is-not-!==`
* :ref:`wrong-typed-property-default`
* :ref:`wrong-type-for-native-php-function`
* :ref:`unknown-parameter-name`
* :ref:`missing-some-returntype`
* :ref:`htmlentities-using-default-flag`
* :ref:`wrong-argument-name-with-php-function`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | CI-checks                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


