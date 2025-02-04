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

* :ref:`structures-addzero`
* :ref:`arrays-multipleidenticalkeys`
* :ref:`classes-nonppp`
* :ref:`classes-nonstaticmethodscalledstatic`
* :ref:`classes-staticmethodscalledfromobject`
* :ref:`constants-constantstrangenames`
* :ref:`functions-redeclaredphpfunction`
* :ref:`structures-errorreportingwithinteger`
* :ref:`structures-exitusage`
* :ref:`structures-forgottenwhitespace`
* :ref:`structures-multiplybyone`
* :ref:`structures-noscream`
* :ref:`structures-notnot`
* :ref:`structures-strposcompare`
* :ref:`structures-throwsandassign`
* :ref:`structures-vardumpusage`
* :ref:`structures-uselessinstruction`
* :ref:`constants-multipleconstantdefinition`
* :ref:`functions-wrongoptionalparameter`
* :ref:`php-isnullvsequalnull`
* :ref:`type-onevariablestrings`
* :ref:`classes-staticcontainsthis`
* :ref:`structures-whilelisteach`
* :ref:`structures-multipledefinedcase`
* :ref:`structures-switchwithoutdefault`
* :ref:`structures-nestedternary`
* :ref:`constants-undefinedconstants`
* :ref:`structures-htmlentitiescall`
* :ref:`classes-undefinedconstants`
* :ref:`functions-undefinedfunctions`
* :ref:`php-deprecated`
* :ref:`structures-danglingarrayreferences`
* :ref:`functions-aliasesusage`
* :ref:`functions-usesdefaultarguments`
* :ref:`functions-wrongnumberofarguments`
* :ref:`constants-constrecommended`
* :ref:`structures-listomissions`
* :ref:`structures-ordie`
* :ref:`functions-mustreturn`
* :ref:`exceptions-overwriteexception`
* :ref:`structures-foreachreferenceisnotmodified`
* :ref:`classes-undefinedproperty`
* :ref:`structures-booleanstrictcomparison`
* :ref:`structures-loneblock`
* :ref:`php-logicalinletters`
* :ref:`structures-repeatedprint`
* :ref:`structures-printwithoutparenthesis`
* :ref:`structures-objectreferences`
* :ref:`type-norealcomparison`
* :ref:`classes-directcalltomagicmethod`
* :ref:`classes-uselessfinal`
* :ref:`structures-useconstant`
* :ref:`structures-uselessunset`
* :ref:`performances-arraymergeinloops`
* :ref:`structures-uselessparenthesis`
* :ref:`php-useobjectapi`
* :ref:`structures-alteringforeachwithoutreference`
* :ref:`php-usepathinfo`
* :ref:`structures-noparenthesisforlanguageconstruct`
* :ref:`functions-useconstantasarguments`
* :ref:`structures-impliedif`
* :ref:`structures-shouldchainexception`
* :ref:`interfaces-undefinedinterfaces`
* :ref:`security-shouldusepreparedstatement`
* :ref:`structures-printanddie`
* :ref:`structures-uncheckedresources`
* :ref:`structures-elseifelseif`
* :ref:`classes-multipledeclarations`
* :ref:`namespaces-emptynamespace`
* :ref:`structures-coulduseshortassignation`
* :ref:`performances-prepostincrement`
* :ref:`structures-indicesareintorstring`
* :ref:`type-shouldtypecast`
* :ref:`structures-nosubstrone`
* :ref:`structures-uselessbrackets`
* :ref:`structures-pregoptione`
* :ref:`structures-evalwithouttry`
* :ref:`structures-useinstanceof`
* :ref:`type-silentlycastinteger`
* :ref:`structures-timestampdifference`
* :ref:`php-internalparametertype`
* :ref:`classes-redefinedconstants`
* :ref:`classes-redefineddefault`
* :ref:`php-fopenmode`
* :ref:`structures-negativepow`
* :ref:`php-betterrand`
* :ref:`structures-ternaryinconcat`
* :ref:`traits-undefinedtrait`
* :ref:`structures-identicalconditions`
* :ref:`structures-nochoice`
* :ref:`structures-logicalmistakes`
* :ref:`structures-sameconditions`
* :ref:`structures-returntruefalse`
* :ref:`structures-couldusedir`
* :ref:`php-shouldusecoalesce`
* :ref:`structures-ifwithsameconditions`
* :ref:`exceptions-throwfunctioncall`
* :ref:`classes-useinstanceof`
* :ref:`structures-resultmaybemissing`
* :ref:`structures-nevernegative`
* :ref:`structures-emptyblocks`
* :ref:`classes-throwindestruct`
* :ref:`structures-usesystemtmp`
* :ref:`namespaces-hiddenuse`
* :ref:`namespaces-shouldmakealias`
* :ref:`classes-multipletraitorinterface`
* :ref:`namespaces-multiplealiasdefinitions`
* :ref:`structures-failingsubstrcomparison`
* :ref:`structures-shouldmaketernary`
* :ref:`structures-dropelseafterreturn`
* :ref:`classes-useclassoperator`
* :ref:`security-dontechoerror`
* :ref:`structures-uselesscasting`
* :ref:`structures-noissetwithempty`
* :ref:`structures-uselesscheck`
* :ref:`namespaces-multiplealiasdefinitionperfile`
* :ref:`structures-dirthenslash`
* :ref:`structures-repeatedregex`
* :ref:`php-noclassinglobal`
* :ref:`structures-couldusestrrepeat`
* :ref:`type-stringwithstrangespace`
* :ref:`structures-noemptyregex`
* :ref:`structures-noreferenceonleft`
* :ref:`php-assignand`
* :ref:`classes-nomagicwitharray`
* :ref:`structures-iszero`
* :ref:`structures-unconditionloopbreak`
* :ref:`structures-nextmonthtrap`
* :ref:`structures-printfarguments`
* :ref:`structures-invalidregex`
* :ref:`structures-autounsetforeach`
* :ref:`structures-identicalonbothsides`
* :ref:`php-noreferenceforternary`
* :ref:`functions-unusedinheritedvariable`
* :ref:`classes-dontunsetproperties`
* :ref:`php-strtrarguments`
* :ref:`structures-missingparenthesis`
* :ref:`functions-callbackneedsreturn`
* :ref:`performances-strpostoomuch`
* :ref:`functions-typehintedreferences`
* :ref:`structures-checkjson`
* :ref:`classes-undefinedstaticclass`
* :ref:`variables-undefinedvariable`
* :ref:`traits-undefinedinsteadof`
* :ref:`classes-undeclaredstaticproperty`
* :ref:`structures-invalidpackformat`
* :ref:`functions-shouldyieldwithkey`
* :ref:`traits-uselessalias`
* :ref:`php-missingsubpattern`
* :ref:`structures-assigneandcompare`
* :ref:`functions-typehintmustbereturned`
* :ref:`classes-checkoncallusage`
* :ref:`structures-castingternary`
* :ref:`php-concatandaddition`
* :ref:`functions-wrongreturnedtype`
* :ref:`classes-noparent`
* :ref:`php-scalararenotarrays`
* :ref:`structures-implodeargsorder`
* :ref:`structures-striptagsskipsclosedtag`
* :ref:`structures-shoulduseexplodeargs`
* :ref:`performances-usearrayslice`
* :ref:`structures-coalesceandconcat`
* :ref:`interfaces-isnotimplemented`
* :ref:`functions-noliteralforreference`
* :ref:`interfaces-cantimplementtraversable`
* :ref:`php-isawithstring`
* :ref:`structures-mbstringunknownencoding`
* :ref:`structures-mbstringthirdarg`
* :ref:`structures-mergeifthen`
* :ref:`functions-wrongtypewithcall`
* :ref:`structures-notequal`
* :ref:`classes-wrongtypedpropertyinit`
* :ref:`php-wrongtypefornativefunction`
* :ref:`functions-unknownparametername`
* :ref:`typehints-missingreturntype`
* :ref:`structures-htmlentitiescalldefaultflag`
* :ref:`functions-wrongargumentnamewithphpfunction`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | CI-checks                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


