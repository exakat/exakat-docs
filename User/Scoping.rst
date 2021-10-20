.. _Scoping:

Scoping analysis
================

Summary
-------


* `scoping files`_
* `scoping rules`_
* `scoping reports`_



Scoping files
----------------------

ignore_dirs and include_dirs are the option used to select files within a folder. Here are some tips to choose 

* From the full list of files, ignore_dirs[] is applied, then include_dirs is applied. The remaining list is processed.
* ignore one file : 
  `ignore_dirs[] = "/path/to/file.php"`

* ignore one dir : 
  `ignore_dirs[] = "/path/to/dir/"`

* ignore siblings but include one dir : 
  `ignore_dirs[] = "/path/to/parent/";`
  `include_dirs[] = "/path/to/parent/dir/"`

* ignore every name containing 'test' : 
  `ignore_dirs[] = "test";`

* only include one dir (and exclude the rest): 
  `include_dirs[] = "/path/to/dir/";`

* omitting include_dirs defaults to `"include_dirs[] = ""`
* omitting ignore_dirs defaults to `"ignore_dirs[] = ""`
* including or ignoring files multiple times only has effect once

include_dirs has priority over the `config.cache` configuration file. If a folder has been marked for exclusion in the `config.cache` file, it may be forced to be included by configuring its value with include_dirs in the `config.ini` file. 

Scoping rules
------------------------------
to be completed




Scoping reports
------------------------------

Exakat builds a list of analysis to run, based on two directives : `project_reports` and `projects_themes`. Both are list of rulesets. Unknown rulesets are omitted. 

project_reports makes sure you can extract those reports, while `projects_themes` allow you to build reports a la carte later, and avoid running the whole audit again.

Required rulesets
#################
First, analysis are very numerous, and it is very tedious to sort them by hand. Exakat only handles 'themes' which are groups of analysis. There are several list of rulesets available by default, and it is possible to customize those lists. 

When using the `projects_themes` directive, you can configure which rulesets must be processed by exakat, each time a 'project' command is run. Those rulesets are always run. 

Report-needed rulesets
######################

Reports are build based on results found during the auditing phase. Some reports, like 'Ambassador' or 'Drillinstructor' needs the results of specific rulesets. Others, like 'Text' or 'Json' build reports at the last moment. 

As such, exakat uses the project_reports directive to collect the list of necessary rulesets, and add them to the `projects_themes` results. 

Late reports
############

It is possible de extract a report, even if the configuration has not been explicitly set for it. 

For example, it is possible to build the Owasp report after telling exakat to build a 'Ambassador' report, as Ambassador includes all the analysis needed for Owasp. On the other hand, the contrary is not true : one can't get the Ambassador report after running exakat for the Owasp report, as Owasp only covers the security rulesets, and Ambassador requires other rulesets. 

Recommendations
###############

* The 'Ambassador' report has all the classic rulesets, it's the most comprehensive choice. 
* To collect everything possible, use the ruleset 'All'. It's also the longest-running ruleset of all. 
* To get one report, simply configure project_report with that report. 
* You may configure several rulesets, like 'Security', 'Suggestions', 'CompatibilityPHP73', and later extract independant results with the 'Text' or 'Json' format.
* If you just want one compulsory report and two optional reports (total of three), simply configure all of them with project_report. It's better to produce extra reports, than run again a whole audit to collect missing informations. 
* It is possible to configure customized rulesets, and use them in project_rulesets
* Excluding one analyzer is not supported. Use custom rulesets to build a new one instead. 

Example
#######

::

    project_reports[] = 'Drillinstructor';
    project_reports[] = 'Owasp';

    project_themes[] = 'Security';
    project_themes[] = 'Suggestions';
    

With that configuration, the Drillinstructor and the Owasp report are created automatically when running 'project'. Use the following command to get the specific rulesets ; 

::

    php exakat.phar report -p <project> -format Text -T Security -v 
    

Predefined config files
------------------------

INI configuration for built-in rulesets. Copy them in config/themes.ini, and make your owns.

28 rulesets detailled here : 

.. _annex-preferences:

Preferences
###########


| [Preferences]
|   analyzer[] = "Arrays/ArrayBracketConsistence";
|   analyzer[] = "Arrays/EmptyFinal";
|   analyzer[] = "Classes/NewOnFunctioncallOrIdentifier";
|   analyzer[] = "Classes/PPPDeclarationStyle";
|   analyzer[] = "Constants/ConstDefinePreference";
|   analyzer[] = "Constants/DefineInsensitivePreference";
|   analyzer[] = "Constants/InconsistantCase";
|   analyzer[] = "Exceptions/CatchE";
|   analyzer[] = "Php/CloseTagsConsistency";
|   analyzer[] = "Php/DeclareEncoding";
|   analyzer[] = "Php/DeclareStrict";
|   analyzer[] = "Php/DeclareStrictType";
|   analyzer[] = "Php/DeclareTicks";
|   analyzer[] = "Php/GlobalsVsGlobal";
|   analyzer[] = "Php/LetterCharsLogicalFavorite";
|   analyzer[] = "Php/ShellFavorite";
|   analyzer[] = "Php/UnsetOrCast";
|   analyzer[] = "Structures/ComparisonFavorite";
|   analyzer[] = "Structures/ConcatenationInterpolationFavorite";
|   analyzer[] = "Structures/ConstantComparisonConsistance";
|   analyzer[] = "Structures/DieExitConsistance";
|   analyzer[] = "Structures/DifferencePreference";
|   analyzer[] = "Structures/EchoPrintConsistance";
|   analyzer[] = "Structures/GtOrLtFavorite";
|   analyzer[] = "Structures/NewLineStyle";
|   analyzer[] = "Structures/NotOrNot";
|   analyzer[] = "Structures/OneExpressionBracketsConsistency";
|   analyzer[] = "Structures/RegexDelimiter";



.. _annex-analyze:

Analyze
#######


| [Analyze]
|   analyzer[] = "Arrays/AmbiguousKeys";
|   analyzer[] = "Arrays/MultipleIdenticalKeys";
|   analyzer[] = "Arrays/NoSpreadForHash";
|   analyzer[] = "Arrays/NonConstantArray";
|   analyzer[] = "Arrays/NullBoolean";
|   analyzer[] = "Arrays/RandomlySortedLiterals";
|   analyzer[] = "Arrays/TooManyDimensions";
|   analyzer[] = "Attributes/MissingAttributeAttribute";
|   analyzer[] = "Attributes/ModifyImmutable";
|   analyzer[] = "Classes/AbstractOrImplements";
|   analyzer[] = "Classes/AbstractStatic";
|   analyzer[] = "Classes/AccessPrivate";
|   analyzer[] = "Classes/AccessProtected";
|   analyzer[] = "Classes/AmbiguousStatic";
|   analyzer[] = "Classes/AmbiguousVisibilities";
|   analyzer[] = "Classes/AvoidOptionArrays";
|   analyzer[] = "Classes/AvoidOptionalProperties";
|   analyzer[] = "Classes/CantExtendFinal";
|   analyzer[] = "Classes/CantInstantiateClass";
|   analyzer[] = "Classes/CheckOnCallUsage";
|   analyzer[] = "Classes/CitSameName";
|   analyzer[] = "Classes/CloneWithNonObject";
|   analyzer[] = "Classes/CouldBeAbstractClass";
|   analyzer[] = "Classes/CouldBeFinal";
|   analyzer[] = "Classes/CouldBeStatic";
|   analyzer[] = "Classes/CouldBeStringable";
|   analyzer[] = "Classes/CyclicReferences";
|   analyzer[] = "Classes/DependantAbstractClass";
|   analyzer[] = "Classes/DifferentArgumentCounts";
|   analyzer[] = "Classes/DirectCallToMagicMethod";
|   analyzer[] = "Classes/DontSendThisInConstructor";
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/EmptyClass";
|   analyzer[] = "Classes/FinalByOcramius";
|   analyzer[] = "Classes/HiddenNullable";
|   analyzer[] = "Classes/ImplementIsForInterface";
|   analyzer[] = "Classes/ImplementedMethodsArePublic";
|   analyzer[] = "Classes/IncompatibleSignature";
|   analyzer[] = "Classes/IncompatibleSignature74";
|   analyzer[] = "Classes/InheritedPropertyMustMatch";
|   analyzer[] = "Classes/InstantiatingAbstractClass";
|   analyzer[] = "Classes/MakeDefault";
|   analyzer[] = "Classes/MakeGlobalAProperty";
|   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MissingAbstractMethod";
|   analyzer[] = "Classes/MultipleDeclarations";
|   analyzer[] = "Classes/MultipleTraitOrInterface";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoPSSOutsideClass";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NoPublicAccess";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/NonNullableSetters";
|   analyzer[] = "Classes/NonPpp";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/OldStyleConstructor";
|   analyzer[] = "Classes/OldStyleVar";
|   analyzer[] = "Classes/ParentFirst";
|   analyzer[] = "Classes/PropertyCouldBeLocal";
|   analyzer[] = "Classes/PropertyNeverUsed";
|   analyzer[] = "Classes/PropertyUsedInOneMethodOnly";
|   analyzer[] = "Classes/PssWithoutClass";
|   analyzer[] = "Classes/RedefinedConstants";
|   analyzer[] = "Classes/RedefinedDefault";
|   analyzer[] = "Classes/RedefinedPrivateProperty";
|   analyzer[] = "Classes/ScalarOrObjectProperty";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/ShouldUseThis";
|   analyzer[] = "Classes/StaticContainsThis";
|   analyzer[] = "Classes/StaticMethodsCalledFromObject";
|   analyzer[] = "Classes/SwappedArguments";
|   analyzer[] = "Classes/ThisIsForClasses";
|   analyzer[] = "Classes/ThisIsNotAnArray";
|   analyzer[] = "Classes/ThisIsNotForStatic";
|   analyzer[] = "Classes/ThrowInDestruct";
|   analyzer[] = "Classes/TooManyDereferencing";
|   analyzer[] = "Classes/TooManyFinds";
|   analyzer[] = "Classes/TooManyInjections";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UndefinedClasses";
|   analyzer[] = "Classes/UndefinedConstants";
|   analyzer[] = "Classes/UndefinedParentMP";
|   analyzer[] = "Classes/UndefinedProperty";
|   analyzer[] = "Classes/UndefinedStaticMP";
|   analyzer[] = "Classes/UndefinedStaticclass";
|   analyzer[] = "Classes/UnresolvedClasses";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Classes/UnusedClass";
|   analyzer[] = "Classes/UnusedConstant";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Classes/UseInstanceof";
|   analyzer[] = "Classes/UsedOnceProperty";
|   analyzer[] = "Classes/UselessAbstract";
|   analyzer[] = "Classes/UselessConstructor";
|   analyzer[] = "Classes/UselessFinal";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Classes/WeakType";
|   analyzer[] = "Classes/WrongName";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Constants/BadConstantnames";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Constants/ConstantStrangeNames";
|   analyzer[] = "Constants/CreatedOutsideItsNamespace";
|   analyzer[] = "Constants/InvalidName";
|   analyzer[] = "Constants/MultipleConstantDefinition";
|   analyzer[] = "Constants/StrangeName";
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Exceptions/CantThrow";
|   analyzer[] = "Exceptions/CatchUndefinedVariable";
|   analyzer[] = "Exceptions/ForgottenThrown";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/ThrowFunctioncall";
|   analyzer[] = "Exceptions/UncaughtExceptions";
|   analyzer[] = "Exceptions/Unthrown";
|   analyzer[] = "Exceptions/UselessCatch";
|   analyzer[] = "Files/InclusionWrongCase";
|   analyzer[] = "Files/MissingInclude";
|   analyzer[] = "Functions/AliasesUsage";
|   analyzer[] = "Functions/AvoidBooleanArgument";
|   analyzer[] = "Functions/CallbackNeedsReturn";
|   analyzer[] = "Functions/CancelledParameter";
|   analyzer[] = "Functions/CannotUseStaticForClosure";
|   analyzer[] = "Functions/CouldCentralize";
|   analyzer[] = "Functions/DeepDefinitions";
|   analyzer[] = "Functions/DontUseVoid";
|   analyzer[] = "Functions/DuplicateNamedParameter";
|   analyzer[] = "Functions/EmptyFunction";
|   analyzer[] = "Functions/FnArgumentVariableConfusion";
|   analyzer[] = "Functions/HardcodedPasswords";
|   analyzer[] = "Functions/InsufficientTypehint";
|   analyzer[] = "Functions/MismatchParameterAndType";
|   analyzer[] = "Functions/MismatchParameterName";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MismatchedDefaultArguments";
|   analyzer[] = "Functions/MismatchedTypehint";
|   analyzer[] = "Functions/ModifyTypedParameter";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/NeverUsedParameter";
|   analyzer[] = "Functions/NoBooleanAsDefault";
|   analyzer[] = "Functions/NoLiteralForReference";
|   analyzer[] = "Functions/NoReturnUsed";
|   analyzer[] = "Functions/OnlyVariableForReference";
|   analyzer[] = "Functions/OnlyVariablePassedByReference";
|   analyzer[] = "Functions/RedeclaredPhpFunction";
|   analyzer[] = "Functions/RelayFunction";
|   analyzer[] = "Functions/ShouldUseConstants";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Functions/TooManyLocalVariables";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Functions/TypehintedReferences";
|   analyzer[] = "Functions/UndefinedFunctions";
|   analyzer[] = "Functions/UnknownParameterName";
|   analyzer[] = "Functions/UnusedArguments";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UnusedReturnedValue";
|   analyzer[] = "Functions/UseConstantAsArguments";
|   analyzer[] = "Functions/UselessReferenceArgument";
|   analyzer[] = "Functions/UselessReturn";
|   analyzer[] = "Functions/UsesDefaultArguments";
|   analyzer[] = "Functions/UsingDeprecated";
|   analyzer[] = "Functions/WithoutReturn";
|   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
|   analyzer[] = "Functions/WrongArgumentType";
|   analyzer[] = "Functions/WrongNumberOfArguments";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Functions/funcGetArgModified";
|   analyzer[] = "Interfaces/AlreadyParentsInterface";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/ConcreteVisibility";
|   analyzer[] = "Interfaces/CouldUseInterface";
|   analyzer[] = "Interfaces/EmptyInterface";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
|   analyzer[] = "Interfaces/RepeatedInterface";
|   analyzer[] = "Interfaces/UndefinedInterfaces";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Namespaces/ConstantFullyQualified";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/HiddenUse";
|   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
|   analyzer[] = "Namespaces/MultipleAliasDefinitions";
|   analyzer[] = "Namespaces/ShouldMakeAlias";
|   analyzer[] = "Namespaces/UnresolvedUse";
|   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/LogicalToInArray";
|   analyzer[] = "Performances/MemoizeMagicCall";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/StrposTooMuch";
|   analyzer[] = "Performances/UseArraySlice";
|   analyzer[] = "Php/ArrayKeyExistsWithObjects";
|   analyzer[] = "Php/AssertFunctionIsReserved";
|   analyzer[] = "Php/AssignAnd";
|   analyzer[] = "Php/Assumptions";
|   analyzer[] = "Php/AvoidMbDectectEncoding";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/Crc32MightBeNegative";
|   analyzer[] = "Php/Deprecated";
|   analyzer[] = "Php/DontPolluteGlobalSpace";
|   analyzer[] = "Php/EmptyList";
|   analyzer[] = "Php/FopenMode";
|   analyzer[] = "Php/ForeachObject";
|   analyzer[] = "Php/HashAlgos";
|   analyzer[] = "Php/Incompilable";
|   analyzer[] = "Php/InternalParameterType";
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingMagicIsset";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Php/MultipleDeclareStrict";
|   analyzer[] = "Php/MustCallParentConstructor";
|   analyzer[] = "Php/NativeClassTypeCompatibility";
|   analyzer[] = "Php/NoClassInGlobal";
|   analyzer[] = "Php/NoReferenceForTernary";
|   analyzer[] = "Php/OnlyVariableForReference";
|   analyzer[] = "Php/PathinfoReturns";
|   analyzer[] = "Php/ReservedNames";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/ShortOpenTagRequired";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/StrtrArguments";
|   analyzer[] = "Php/TooManyNativeCalls";
|   analyzer[] = "Php/UnknownPcre2Option";
|   analyzer[] = "Php/UseObjectApi";
|   analyzer[] = "Php/UsePathinfo";
|   analyzer[] = "Php/UseSetCookie";
|   analyzer[] = "Php/UseStdclass";
|   analyzer[] = "Php/WrongAttributeConfiguration";
|   analyzer[] = "Php/WrongTypeForNativeFunction";
|   analyzer[] = "Php/oldAutoloadUsage";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Structures/AddZero";
|   analyzer[] = "Structures/AlteringForeachWithoutReference";
|   analyzer[] = "Structures/AlternativeConsistenceByFile";
|   analyzer[] = "Structures/AlwaysFalse";
|   analyzer[] = "Structures/ArrayFillWithObjects";
|   analyzer[] = "Structures/ArrayMapPassesByValue";
|   analyzer[] = "Structures/ArrayMergeAndVariadic";
|   analyzer[] = "Structures/ArrayMergeArrayArray";
|   analyzer[] = "Structures/AssigneAndCompare";
|   analyzer[] = "Structures/AutoUnsetForeach";
|   analyzer[] = "Structures/BailOutEarly";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/BreakOutsideLoop";
|   analyzer[] = "Structures/BuriedAssignation";
|   analyzer[] = "Structures/CastToBoolean";
|   analyzer[] = "Structures/CastingTernary";
|   analyzer[] = "Structures/CatchShadowsVariable";
|   analyzer[] = "Structures/CheckAllTypes";
|   analyzer[] = "Structures/CheckJson";
|   analyzer[] = "Structures/CoalesceAndConcat";
|   analyzer[] = "Structures/CommonAlternatives";
|   analyzer[] = "Structures/ComparedComparison";
|   analyzer[] = "Structures/ConcatEmpty";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/CouldBeElse";
|   analyzer[] = "Structures/CouldBeStatic";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/DirThenSlash";
|   analyzer[] = "Structures/DontChangeBlindKey";
|   analyzer[] = "Structures/DontMixPlusPlus";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
|   analyzer[] = "Structures/DoubleAssignation";
|   analyzer[] = "Structures/DoubleInstruction";
|   analyzer[] = "Structures/DoubleObjectAssignation";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/EmptyBlocks";
|   analyzer[] = "Structures/EmptyLines";
|   analyzer[] = "Structures/EmptyTryCatch";
|   analyzer[] = "Structures/ErrorReportingWithInteger";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/ExitUsage";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForeachReferenceIsNotModified";
|   analyzer[] = "Structures/ForeachSourceValue";
|   analyzer[] = "Structures/ForgottenWhiteSpace";
|   analyzer[] = "Structures/GlobalUsage";
|   analyzer[] = "Structures/Htmlentitiescall";
|   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
|   analyzer[] = "Structures/IdenticalConditions";
|   analyzer[] = "Structures/IdenticalConsecutive";
|   analyzer[] = "Structures/IdenticalOnBothSides";
|   analyzer[] = "Structures/IfWithSameConditions";
|   analyzer[] = "Structures/Iffectation";
|   analyzer[] = "Structures/ImpliedIf";
|   analyzer[] = "Structures/ImplodeArgsOrder";
|   analyzer[] = "Structures/InconsistentElseif";
|   analyzer[] = "Structures/IndicesAreIntOrString";
|   analyzer[] = "Structures/InfiniteRecursion";
|   analyzer[] = "Structures/InvalidPackFormat";
|   analyzer[] = "Structures/InvalidRegex";
|   analyzer[] = "Structures/IsZero";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LogicalMistakes";
|   analyzer[] = "Structures/LoneBlock";
|   analyzer[] = "Structures/LongArguments";
|   analyzer[] = "Structures/MaxLevelOfIdentation";
|   analyzer[] = "Structures/MbstringThirdArg";
|   analyzer[] = "Structures/MbstringUnknownEncoding";
|   analyzer[] = "Structures/MergeIfThen";
|   analyzer[] = "Structures/MismatchedTernary";
|   analyzer[] = "Structures/MissingCases";
|   analyzer[] = "Structures/MissingNew";
|   analyzer[] = "Structures/MissingParenthesis";
|   analyzer[] = "Structures/MixedConcatInterpolation";
|   analyzer[] = "Structures/ModernEmpty";
|   analyzer[] = "Structures/MultipleDefinedCase";
|   analyzer[] = "Structures/MultipleTypeVariable";
|   analyzer[] = "Structures/MultiplyByOne";
|   analyzer[] = "Structures/NegativePow";
|   analyzer[] = "Structures/NestedIfthen";
|   analyzer[] = "Structures/NestedTernary";
|   analyzer[] = "Structures/NeverNegative";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoAppendOnSource";
|   analyzer[] = "Structures/NoChangeIncomingVariables";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoDirectUsage";
|   analyzer[] = "Structures/NoEmptyRegex";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/NoHardcodedHash";
|   analyzer[] = "Structures/NoHardcodedIp";
|   analyzer[] = "Structures/NoHardcodedPath";
|   analyzer[] = "Structures/NoHardcodedPort";
|   analyzer[] = "Structures/NoIssetWithEmpty";
|   analyzer[] = "Structures/NoNeedForElse";
|   analyzer[] = "Structures/NoNeedForTriple";
|   analyzer[] = "Structures/NoObjectAsIndex";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoReferenceOnLeft";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/NoVariableIsACondition";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/NotEqual";
|   analyzer[] = "Structures/NotNot";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/OnceUsage";
|   analyzer[] = "Structures/OneLineTwoInstructions";
|   analyzer[] = "Structures/OnlyFirstByte";
|   analyzer[] = "Structures/OnlyVariableReturnedByReference";
|   analyzer[] = "Structures/OrDie";
|   analyzer[] = "Structures/PossibleInfiniteLoop";
|   analyzer[] = "Structures/PrintAndDie";
|   analyzer[] = "Structures/PrintWithoutParenthesis";
|   analyzer[] = "Structures/PrintfArguments";
|   analyzer[] = "Structures/QueriesInLoop";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/RepeatedRegex";
|   analyzer[] = "Structures/ResultMayBeMissing";
|   analyzer[] = "Structures/ReturnTrueFalse";
|   analyzer[] = "Structures/SameConditions";
|   analyzer[] = "Structures/ShouldChainException";
|   analyzer[] = "Structures/ShouldMakeTernary";
|   analyzer[] = "Structures/ShouldPreprocess";
|   analyzer[] = "Structures/ShouldUseExplodeArgs";
|   analyzer[] = "Structures/StaticLoop";
|   analyzer[] = "Structures/StripTagsSkipsClosedTag";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/SuspiciousComparison";
|   analyzer[] = "Structures/SwitchToSwitch";
|   analyzer[] = "Structures/SwitchWithoutDefault";
|   analyzer[] = "Structures/TernaryInConcat";
|   analyzer[] = "Structures/TestThenCast";
|   analyzer[] = "Structures/ThrowsAndAssign";
|   analyzer[] = "Structures/TimestampDifference";
|   analyzer[] = "Structures/UncheckedResources";
|   analyzer[] = "Structures/UnconditionLoopBreak";
|   analyzer[] = "Structures/UnknownPregOption";
|   analyzer[] = "Structures/Unpreprocessed";
|   analyzer[] = "Structures/UnsetInForeach";
|   analyzer[] = "Structures/UnsupportedTypesWithOperators";
|   analyzer[] = "Structures/UnusedGlobal";
|   analyzer[] = "Structures/UseConstant";
|   analyzer[] = "Structures/UseInstanceof";
|   analyzer[] = "Structures/UsePositiveCondition";
|   analyzer[] = "Structures/UseSystemTmp";
|   analyzer[] = "Structures/UselessBrackets";
|   analyzer[] = "Structures/UselessCasting";
|   analyzer[] = "Structures/UselessCheck";
|   analyzer[] = "Structures/UselessGlobal";
|   analyzer[] = "Structures/UselessInstruction";
|   analyzer[] = "Structures/UselessParenthesis";
|   analyzer[] = "Structures/UselessSwitch";
|   analyzer[] = "Structures/UselessUnset";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Structures/WrongRange";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Structures/toStringThrowsException";
|   analyzer[] = "Traits/AlreadyParentsTrait";
|   analyzer[] = "Traits/DependantTrait";
|   analyzer[] = "Traits/EmptyTrait";
|   analyzer[] = "Traits/MethodCollisionTraits";
|   analyzer[] = "Traits/TraitNotFound";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Type/OneVariableStrings";
|   analyzer[] = "Type/ShouldTypecast";
|   analyzer[] = "Type/SilentlyCastInteger";
|   analyzer[] = "Type/StringHoldAVariable";
|   analyzer[] = "Type/StringWithStrangeSpace";
|   analyzer[] = "Typehints/MissingReturntype";
|   analyzer[] = "Variables/AssignedTwiceOrMore";
|   analyzer[] = "Variables/ConstantTypo";
|   analyzer[] = "Variables/LostReferences";
|   analyzer[] = "Variables/OverwrittenLiterals";
|   analyzer[] = "Variables/StrangeName";
|   analyzer[] = "Variables/UndefinedConstantName";
|   analyzer[] = "Variables/UndefinedVariable";
|   analyzer[] = "Variables/VariableNonascii";
|   analyzer[] = "Variables/VariableUsedOnce";
|   analyzer[] = "Variables/VariableUsedOnceByContext";
|   analyzer[] = "Variables/WrittenOnlyVariable";



.. _annex-attributes:

Attributes
##########


| [Attributes]
|   analyzer[] = "Attributes/MissingAttributeAttribute";
|   analyzer[] = "Attributes/ModifyImmutable";
|   analyzer[] = "Functions/KillsApp";
|   analyzer[] = "Functions/UsingDeprecated";



.. _annex-ce:

CE
##


| [CE]
|   analyzer[] = "Arrays/ArrayNSUsage";
|   analyzer[] = "Arrays/Arrayindex";
|   analyzer[] = "Arrays/Multidimensional";
|   analyzer[] = "Arrays/MultipleIdenticalKeys";
|   analyzer[] = "Arrays/NegativeStart";
|   analyzer[] = "Arrays/Phparrayindex";
|   analyzer[] = "Arrays/WithCallback";
|   analyzer[] = "Classes/Abstractclass";
|   analyzer[] = "Classes/Abstractmethods";
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CheckOnCallUsage";
|   analyzer[] = "Classes/ClassAliasUsage";
|   analyzer[] = "Classes/Classnames";
|   analyzer[] = "Classes/CloningUsage";
|   analyzer[] = "Classes/ConstantClass";
|   analyzer[] = "Classes/ConstantDefinition";
|   analyzer[] = "Classes/DefinedConstants";
|   analyzer[] = "Classes/DefinedProperty";
|   analyzer[] = "Classes/DirectCallToMagicMethod";
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/DynamicClass";
|   analyzer[] = "Classes/DynamicConstantCall";
|   analyzer[] = "Classes/DynamicMethodCall";
|   analyzer[] = "Classes/DynamicNew";
|   analyzer[] = "Classes/DynamicPropertyCall";
|   analyzer[] = "Classes/FinalPrivate";
|   analyzer[] = "Classes/HasMagicProperty";
|   analyzer[] = "Classes/ImmutableSignature";
|   analyzer[] = "Classes/IsNotFamily";
|   analyzer[] = "Classes/IsaMagicProperty";
|   analyzer[] = "Classes/MagicMethod";
|   analyzer[] = "Classes/MultipleClassesInFile";
|   analyzer[] = "Classes/MultipleDeclarations";
|   analyzer[] = "Classes/MultipleTraitOrInterface";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NonPpp";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/OldStyleConstructor";
|   analyzer[] = "Classes/OverwrittenConst";
|   analyzer[] = "Classes/RedefinedConstants";
|   analyzer[] = "Classes/RedefinedDefault";
|   analyzer[] = "Classes/RedefinedMethods";
|   analyzer[] = "Classes/StaticContainsThis";
|   analyzer[] = "Classes/StaticMethods";
|   analyzer[] = "Classes/StaticMethodsCalledFromObject";
|   analyzer[] = "Classes/StaticProperties";
|   analyzer[] = "Classes/TestClass";
|   analyzer[] = "Classes/ThrowInDestruct";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UndefinedConstants";
|   analyzer[] = "Classes/UndefinedProperty";
|   analyzer[] = "Classes/UndefinedStaticclass";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Classes/UseInstanceof";
|   analyzer[] = "Classes/UselessFinal";
|   analyzer[] = "Classes/VariableClasses";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Complete/CreateCompactVariables";
|   analyzer[] = "Complete/CreateMagicProperty";
|   analyzer[] = "Complete/FollowClosureDefinition";
|   analyzer[] = "Complete/MakeClassConstantDefinition";
|   analyzer[] = "Complete/MakeFunctioncallWithReference";
|   analyzer[] = "Complete/OverwrittenConstants";
|   analyzer[] = "Complete/OverwrittenProperties";
|   analyzer[] = "Complete/SetArrayClassDefinition";
|   analyzer[] = "Complete/SetParentDefinition";
|   analyzer[] = "Complete/SetStringMethodDefinition";
|   analyzer[] = "Composer/Autoload";
|   analyzer[] = "Composer/IsComposerClass";
|   analyzer[] = "Composer/IsComposerInterface";
|   analyzer[] = "Composer/IsComposerNsname";
|   analyzer[] = "Composer/UseComposer";
|   analyzer[] = "Composer/UseComposerLock";
|   analyzer[] = "Constants/CaseInsensitiveConstants";
|   analyzer[] = "Constants/ConditionedConstants";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Constants/ConstantStrangeNames";
|   analyzer[] = "Constants/ConstantUsage";
|   analyzer[] = "Constants/Constantnames";
|   analyzer[] = "Constants/CustomConstantUsage";
|   analyzer[] = "Constants/DynamicCreation";
|   analyzer[] = "Constants/IsExtConstant";
|   analyzer[] = "Constants/IsPhpConstant";
|   analyzer[] = "Constants/MagicConstantUsage";
|   analyzer[] = "Constants/MultipleConstantDefinition";
|   analyzer[] = "Constants/PhpConstantUsage";
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Constants/VariableConstant";
|   analyzer[] = "Dump/CallOrder";
|   analyzer[] = "Dump/CollectAtomCounts";
|   analyzer[] = "Dump/CollectClassChanges";
|   analyzer[] = "Dump/CollectClassChildren";
|   analyzer[] = "Dump/CollectClassConstantCounts";
|   analyzer[] = "Dump/CollectClassDepth";
|   analyzer[] = "Dump/CollectClassInterfaceCounts";
|   analyzer[] = "Dump/CollectClassTraitsCounts";
|   analyzer[] = "Dump/CollectClassesDependencies";
|   analyzer[] = "Dump/CollectDefinitionsStats";
|   analyzer[] = "Dump/CollectFilesDependencies";
|   analyzer[] = "Dump/CollectForeachFavorite";
|   analyzer[] = "Dump/CollectGlobalVariables";
|   analyzer[] = "Dump/CollectLiterals";
|   analyzer[] = "Dump/CollectLocalVariableCounts";
|   analyzer[] = "Dump/CollectMbstringEncodings";
|   analyzer[] = "Dump/CollectMethodCounts";
|   analyzer[] = "Dump/CollectNativeCallsPerExpressions";
|   analyzer[] = "Dump/CollectParameterCounts";
|   analyzer[] = "Dump/CollectParameterNames";
|   analyzer[] = "Dump/CollectPhpStructures";
|   analyzer[] = "Dump/CollectPropertyCounts";
|   analyzer[] = "Dump/CollectReadability";
|   analyzer[] = "Dump/CollectUseCounts";
|   analyzer[] = "Dump/CollectVariables";
|   analyzer[] = "Dump/ConstantOrder";
|   analyzer[] = "Dump/CyclomaticComplexity";
|   analyzer[] = "Dump/DereferencingLevels";
|   analyzer[] = "Dump/EnvironnementVariables";
|   analyzer[] = "Dump/FossilizedMethods";
|   analyzer[] = "Dump/Inclusions";
|   analyzer[] = "Dump/IndentationLevels";
|   analyzer[] = "Dump/NewOrder";
|   analyzer[] = "Dump/ParameterArgumentsLinks";
|   analyzer[] = "Dump/TypehintingStats";
|   analyzer[] = "Dump/Typehintorder";
|   analyzer[] = "Exceptions/DefinedExceptions";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/ThrowFunctioncall";
|   analyzer[] = "Exceptions/ThrownExceptions";
|   analyzer[] = "Exceptions/UselessCatch";
|   analyzer[] = "Extensions/Extamqp";
|   analyzer[] = "Extensions/Extapache";
|   analyzer[] = "Extensions/Extapc";
|   analyzer[] = "Extensions/Extapcu";
|   analyzer[] = "Extensions/Extarray";
|   analyzer[] = "Extensions/Extast";
|   analyzer[] = "Extensions/Extasync";
|   analyzer[] = "Extensions/Extbcmath";
|   analyzer[] = "Extensions/Extbzip2";
|   analyzer[] = "Extensions/Extcairo";
|   analyzer[] = "Extensions/Extcalendar";
|   analyzer[] = "Extensions/Extcmark";
|   analyzer[] = "Extensions/Extcom";
|   analyzer[] = "Extensions/Extcrypto";
|   analyzer[] = "Extensions/Extcsprng";
|   analyzer[] = "Extensions/Extctype";
|   analyzer[] = "Extensions/Extcurl";
|   analyzer[] = "Extensions/Extcyrus";
|   analyzer[] = "Extensions/Extdate";
|   analyzer[] = "Extensions/Extdb2";
|   analyzer[] = "Extensions/Extdba";
|   analyzer[] = "Extensions/Extdecimal";
|   analyzer[] = "Extensions/Extdio";
|   analyzer[] = "Extensions/Extdom";
|   analyzer[] = "Extensions/Extds";
|   analyzer[] = "Extensions/Exteaccelerator";
|   analyzer[] = "Extensions/Exteio";
|   analyzer[] = "Extensions/Extenchant";
|   analyzer[] = "Extensions/Extereg";
|   analyzer[] = "Extensions/Extev";
|   analyzer[] = "Extensions/Extevent";
|   analyzer[] = "Extensions/Extexif";
|   analyzer[] = "Extensions/Extexpect";
|   analyzer[] = "Extensions/Extfam";
|   analyzer[] = "Extensions/Extfann";
|   analyzer[] = "Extensions/Extfdf";
|   analyzer[] = "Extensions/Extffi";
|   analyzer[] = "Extensions/Extffmpeg";
|   analyzer[] = "Extensions/Extfile";
|   analyzer[] = "Extensions/Extfileinfo";
|   analyzer[] = "Extensions/Extfilter";
|   analyzer[] = "Extensions/Extfpm";
|   analyzer[] = "Extensions/Extftp";
|   analyzer[] = "Extensions/Extgd";
|   analyzer[] = "Extensions/Extgearman";
|   analyzer[] = "Extensions/Extgender";
|   analyzer[] = "Extensions/Extgeoip";
|   analyzer[] = "Extensions/Extgettext";
|   analyzer[] = "Extensions/Extgmagick";
|   analyzer[] = "Extensions/Extgmp";
|   analyzer[] = "Extensions/Extgnupg";
|   analyzer[] = "Extensions/Extgrpc";
|   analyzer[] = "Extensions/Exthash";
|   analyzer[] = "Extensions/Exthrtime";
|   analyzer[] = "Extensions/Exthttp";
|   analyzer[] = "Extensions/Extibase";
|   analyzer[] = "Extensions/Exticonv";
|   analyzer[] = "Extensions/Extigbinary";
|   analyzer[] = "Extensions/Extiis";
|   analyzer[] = "Extensions/Extimagick";
|   analyzer[] = "Extensions/Extimap";
|   analyzer[] = "Extensions/Extinfo";
|   analyzer[] = "Extensions/Extinotify";
|   analyzer[] = "Extensions/Extintl";
|   analyzer[] = "Extensions/Extjson";
|   analyzer[] = "Extensions/Extjudy";
|   analyzer[] = "Extensions/Extkdm5";
|   analyzer[] = "Extensions/Extlapack";
|   analyzer[] = "Extensions/Extldap";
|   analyzer[] = "Extensions/Extleveldb";
|   analyzer[] = "Extensions/Extlibevent";
|   analyzer[] = "Extensions/Extlibsodium";
|   analyzer[] = "Extensions/Extlibxml";
|   analyzer[] = "Extensions/Extlua";
|   analyzer[] = "Extensions/Extlzf";
|   analyzer[] = "Extensions/Extmail";
|   analyzer[] = "Extensions/Extmailparse";
|   analyzer[] = "Extensions/Extmath";
|   analyzer[] = "Extensions/Extmbstring";
|   analyzer[] = "Extensions/Extmcrypt";
|   analyzer[] = "Extensions/Extmemcache";
|   analyzer[] = "Extensions/Extmemcached";
|   analyzer[] = "Extensions/Extmhash";
|   analyzer[] = "Extensions/Extming";
|   analyzer[] = "Extensions/Extmongo";
|   analyzer[] = "Extensions/Extmongodb";
|   analyzer[] = "Extensions/Extmsgpack";
|   analyzer[] = "Extensions/Extmssql";
|   analyzer[] = "Extensions/Extmysql";
|   analyzer[] = "Extensions/Extmysqli";
|   analyzer[] = "Extensions/Extncurses";
|   analyzer[] = "Extensions/Extnewt";
|   analyzer[] = "Extensions/Extnsapi";
|   analyzer[] = "Extensions/Extob";
|   analyzer[] = "Extensions/Extoci8";
|   analyzer[] = "Extensions/Extodbc";
|   analyzer[] = "Extensions/Extopcache";
|   analyzer[] = "Extensions/Extopencensus";
|   analyzer[] = "Extensions/Extopenssl";
|   analyzer[] = "Extensions/Extparle";
|   analyzer[] = "Extensions/Extparsekit";
|   analyzer[] = "Extensions/Extpassword";
|   analyzer[] = "Extensions/Extpcntl";
|   analyzer[] = "Extensions/Extpcov";
|   analyzer[] = "Extensions/Extpcre";
|   analyzer[] = "Extensions/Extpdo";
|   analyzer[] = "Extensions/Extpgsql";
|   analyzer[] = "Extensions/Extphalcon";
|   analyzer[] = "Extensions/Extphar";
|   analyzer[] = "Extensions/Extposix";
|   analyzer[] = "Extensions/Extproctitle";
|   analyzer[] = "Extensions/Extpspell";
|   analyzer[] = "Extensions/Extpsr";
|   analyzer[] = "Extensions/Extrar";
|   analyzer[] = "Extensions/Extrdkafka";
|   analyzer[] = "Extensions/Extreadline";
|   analyzer[] = "Extensions/Extrecode";
|   analyzer[] = "Extensions/Extredis";
|   analyzer[] = "Extensions/Extreflection";
|   analyzer[] = "Extensions/Extrunkit";
|   analyzer[] = "Extensions/Extsdl";
|   analyzer[] = "Extensions/Extseaslog";
|   analyzer[] = "Extensions/Extsem";
|   analyzer[] = "Extensions/Extsession";
|   analyzer[] = "Extensions/Extshmop";
|   analyzer[] = "Extensions/Extsimplexml";
|   analyzer[] = "Extensions/Extsnmp";
|   analyzer[] = "Extensions/Extsoap";
|   analyzer[] = "Extensions/Extsockets";
|   analyzer[] = "Extensions/Extsphinx";
|   analyzer[] = "Extensions/Extspl";
|   analyzer[] = "Extensions/Extsqlite";
|   analyzer[] = "Extensions/Extsqlite3";
|   analyzer[] = "Extensions/Extsqlsrv";
|   analyzer[] = "Extensions/Extssh2";
|   analyzer[] = "Extensions/Extstandard";
|   analyzer[] = "Extensions/Extstats";
|   analyzer[] = "Extensions/Extstring";
|   analyzer[] = "Extensions/Extsuhosin";
|   analyzer[] = "Extensions/Extsvm";
|   analyzer[] = "Extensions/Extswoole";
|   analyzer[] = "Extensions/Exttidy";
|   analyzer[] = "Extensions/Exttokenizer";
|   analyzer[] = "Extensions/Exttokyotyrant";
|   analyzer[] = "Extensions/Exttrader";
|   analyzer[] = "Extensions/Extuopz";
|   analyzer[] = "Extensions/Extuuid";
|   analyzer[] = "Extensions/Extv8js";
|   analyzer[] = "Extensions/Extvarnish";
|   analyzer[] = "Extensions/Extvips";
|   analyzer[] = "Extensions/Extwasm";
|   analyzer[] = "Extensions/Extwddx";
|   analyzer[] = "Extensions/Extweakref";
|   analyzer[] = "Extensions/Extwikidiff2";
|   analyzer[] = "Extensions/Extwincache";
|   analyzer[] = "Extensions/Extxattr";
|   analyzer[] = "Extensions/Extxcache";
|   analyzer[] = "Extensions/Extxdebug";
|   analyzer[] = "Extensions/Extxdiff";
|   analyzer[] = "Extensions/Extxhprof";
|   analyzer[] = "Extensions/Extxml";
|   analyzer[] = "Extensions/Extxmlreader";
|   analyzer[] = "Extensions/Extxmlrpc";
|   analyzer[] = "Extensions/Extxmlwriter";
|   analyzer[] = "Extensions/Extxsl";
|   analyzer[] = "Extensions/Extxxtea";
|   analyzer[] = "Extensions/Extyaml";
|   analyzer[] = "Extensions/Extyis";
|   analyzer[] = "Extensions/Extzbarcode";
|   analyzer[] = "Extensions/Extzendmonitor";
|   analyzer[] = "Extensions/Extzip";
|   analyzer[] = "Extensions/Extzlib";
|   analyzer[] = "Extensions/Extzmq";
|   analyzer[] = "Extensions/Extzookeeper";
|   analyzer[] = "Files/IsCliScript";
|   analyzer[] = "Files/NotDefinitionsOnly";
|   analyzer[] = "Functions/AliasesUsage";
|   analyzer[] = "Functions/CallbackNeedsReturn";
|   analyzer[] = "Functions/CantUse";
|   analyzer[] = "Functions/Closures";
|   analyzer[] = "Functions/ConditionedFunctions";
|   analyzer[] = "Functions/DeepDefinitions";
|   analyzer[] = "Functions/DynamicCode";
|   analyzer[] = "Functions/Dynamiccall";
|   analyzer[] = "Functions/FallbackFunction";
|   analyzer[] = "Functions/Functionnames";
|   analyzer[] = "Functions/FunctionsUsingReference";
|   analyzer[] = "Functions/IsExtFunction";
|   analyzer[] = "Functions/IsGenerator";
|   analyzer[] = "Functions/KillsApp";
|   analyzer[] = "Functions/MarkCallable";
|   analyzer[] = "Functions/MismatchParameterName";
|   analyzer[] = "Functions/MultipleDeclarations";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/NoLiteralForReference";
|   analyzer[] = "Functions/NullableWithConstant";
|   analyzer[] = "Functions/Recursive";
|   analyzer[] = "Functions/RedeclaredPhpFunction";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Functions/TypehintedReferences";
|   analyzer[] = "Functions/Typehints";
|   analyzer[] = "Functions/UnbindingClosures";
|   analyzer[] = "Functions/UndefinedFunctions";
|   analyzer[] = "Functions/UnknownParameterName";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UseArrowFunctions";
|   analyzer[] = "Functions/UseConstantAsArguments";
|   analyzer[] = "Functions/UsesDefaultArguments";
|   analyzer[] = "Functions/VariableArguments";
|   analyzer[] = "Functions/WrongNumberOfArguments";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/Interfacenames";
|   analyzer[] = "Interfaces/IsExtInterface";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/UndefinedInterfaces";
|   analyzer[] = "Namespaces/Alias";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/HiddenUse";
|   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
|   analyzer[] = "Namespaces/MultipleAliasDefinitions";
|   analyzer[] = "Namespaces/NamespaceUsage";
|   analyzer[] = "Namespaces/Namespacesnames";
|   analyzer[] = "Namespaces/ShouldMakeAlias";
|   analyzer[] = "Patterns/CourrierAntiPattern";
|   analyzer[] = "Patterns/DependencyInjection";
|   analyzer[] = "Patterns/Factory";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/StrposTooMuch";
|   analyzer[] = "Performances/UseArraySlice";
|   analyzer[] = "Php/AlternativeSyntax";
|   analyzer[] = "Php/Argon2Usage";
|   analyzer[] = "Php/ArrayKeyExistsWithObjects";
|   analyzer[] = "Php/AssertionUsage";
|   analyzer[] = "Php/AssignAnd";
|   analyzer[] = "Php/AutoloadUsage";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/CastUnsetUsage";
|   analyzer[] = "Php/CastingUsage";
|   analyzer[] = "Php/Coalesce";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/CryptoUsage";
|   analyzer[] = "Php/DeclareEncoding";
|   analyzer[] = "Php/DeclareStrict";
|   analyzer[] = "Php/DeclareStrictType";
|   analyzer[] = "Php/DeclareTicks";
|   analyzer[] = "Php/Deprecated";
|   analyzer[] = "Php/DetectCurrentClass";
|   analyzer[] = "Php/DirectivesUsage";
|   analyzer[] = "Php/DlUsage";
|   analyzer[] = "Php/EchoTagUsage";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/ErrorLogUsage";
|   analyzer[] = "Php/FilterToAddSlashes";
|   analyzer[] = "Php/FopenMode";
|   analyzer[] = "Php/Gotonames";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/Haltcompiler";
|   analyzer[] = "Php/HashAlgos74";
|   analyzer[] = "Php/IdnUts46";
|   analyzer[] = "Php/Incompilable";
|   analyzer[] = "Php/IntegerSeparatorUsage";
|   analyzer[] = "Php/InternalParameterType";
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Php/IsINF";
|   analyzer[] = "Php/IsNAN";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/Labelnames";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MiddleVersion";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
|   analyzer[] = "Php/NoClassInGlobal";
|   analyzer[] = "Php/NoMoreCurlyArrays";
|   analyzer[] = "Php/NoReferenceForTernary";
|   analyzer[] = "Php/OveriddenFunction";
|   analyzer[] = "Php/PearUsage";
|   analyzer[] = "Php/Php74Deprecation";
|   analyzer[] = "Php/Php74NewClasses";
|   analyzer[] = "Php/Php74NewConstants";
|   analyzer[] = "Php/Php74NewFunctions";
|   analyzer[] = "Php/Php74RemovedDirective";
|   analyzer[] = "Php/Php74RemovedFunctions";
|   analyzer[] = "Php/Php74ReservedKeyword";
|   analyzer[] = "Php/Php74mbstrrpos3rdArg";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/Php80NamedParameterVariadic";
|   analyzer[] = "Php/Php80NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80RemovedConstant";
|   analyzer[] = "Php/Php80RemovedDirective";
|   analyzer[] = "Php/Php80RemovedFunctions";
|   analyzer[] = "Php/Php80RemovesResources";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/Php80VariableSyntax";
|   analyzer[] = "Php/Php81RemovedDirective";
|   analyzer[] = "Php/PhpErrorMsgUsage";
|   analyzer[] = "Php/RawPostDataUsage";
|   analyzer[] = "Php/ReflectionExportIsDeprecated";
|   analyzer[] = "Php/ReturnTypehintUsage";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/ScalarTypehintUsage";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/SpreadOperatorForArray";
|   analyzer[] = "Php/StrtrArguments";
|   analyzer[] = "Php/SuperGlobalUsage";
|   analyzer[] = "Php/ThrowUsage";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TriggerErrorUsage";
|   analyzer[] = "Php/TryCatchUsage";
|   analyzer[] = "Php/TryMultipleCatch";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UseAttributes";
|   analyzer[] = "Php/UseBrowscap";
|   analyzer[] = "Php/UseCli";
|   analyzer[] = "Php/UseContravariance";
|   analyzer[] = "Php/UseCookies";
|   analyzer[] = "Php/UseCovariance";
|   analyzer[] = "Php/UseMatch";
|   analyzer[] = "Php/UseNullSafeOperator";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/UseObjectApi";
|   analyzer[] = "Php/UsePathinfo";
|   analyzer[] = "Php/UseTrailingUseComma";
|   analyzer[] = "Php/UseWeb";
|   analyzer[] = "Php/UsesEnv";
|   analyzer[] = "Php/WrongTypeForNativeFunction";
|   analyzer[] = "Php/YieldFromUsage";
|   analyzer[] = "Php/YieldUsage";
|   analyzer[] = "Psr/Psr11Usage";
|   analyzer[] = "Psr/Psr13Usage";
|   analyzer[] = "Psr/Psr16Usage";
|   analyzer[] = "Psr/Psr3Usage";
|   analyzer[] = "Psr/Psr6Usage";
|   analyzer[] = "Psr/Psr7Usage";
|   analyzer[] = "Security/CantDisableClass";
|   analyzer[] = "Security/CantDisableFunction";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Structures/AddZero";
|   analyzer[] = "Structures/AlteringForeachWithoutReference";
|   analyzer[] = "Structures/ArrayMapPassesByValue";
|   analyzer[] = "Structures/AssigneAndCompare";
|   analyzer[] = "Structures/AutoUnsetForeach";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/CastingTernary";
|   analyzer[] = "Structures/CheckJson";
|   analyzer[] = "Structures/CoalesceAndConcat";
|   analyzer[] = "Structures/ComplexExpression";
|   analyzer[] = "Structures/ConstDefineFavorite";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/CurlVersionNow";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/DereferencingAS";
|   analyzer[] = "Structures/DirThenSlash";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/DynamicCalls";
|   analyzer[] = "Structures/DynamicCode";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/ElseUsage";
|   analyzer[] = "Structures/EmptyBlocks";
|   analyzer[] = "Structures/ErrorMessages";
|   analyzer[] = "Structures/ErrorReportingWithInteger";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/ExitUsage";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/FileUploadUsage";
|   analyzer[] = "Structures/FileUsage";
|   analyzer[] = "Structures/ForeachReferenceIsNotModified";
|   analyzer[] = "Structures/ForgottenWhiteSpace";
|   analyzer[] = "Structures/FunctionSubscripting";
|   analyzer[] = "Structures/GlobalInGlobal";
|   analyzer[] = "Structures/GlobalUsage";
|   analyzer[] = "Structures/Htmlentitiescall";
|   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
|   analyzer[] = "Structures/IdenticalConditions";
|   analyzer[] = "Structures/IdenticalOnBothSides";
|   analyzer[] = "Structures/IfWithSameConditions";
|   analyzer[] = "Structures/ImpliedIf";
|   analyzer[] = "Structures/ImplodeArgsOrder";
|   analyzer[] = "Structures/IncludeUsage";
|   analyzer[] = "Structures/IndicesAreIntOrString";
|   analyzer[] = "Structures/InvalidPackFormat";
|   analyzer[] = "Structures/InvalidRegex";
|   analyzer[] = "Structures/IsZero";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LogicalMistakes";
|   analyzer[] = "Structures/LoneBlock";
|   analyzer[] = "Structures/MailUsage";
|   analyzer[] = "Structures/MbstringThirdArg";
|   analyzer[] = "Structures/MbstringUnknownEncoding";
|   analyzer[] = "Structures/MergeIfThen";
|   analyzer[] = "Structures/MissingParenthesis";
|   analyzer[] = "Structures/MultipleCatch";
|   analyzer[] = "Structures/MultipleDefinedCase";
|   analyzer[] = "Structures/MultiplyByOne";
|   analyzer[] = "Structures/NegativePow";
|   analyzer[] = "Structures/NestedLoops";
|   analyzer[] = "Structures/NestedTernary";
|   analyzer[] = "Structures/NeverNegative";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoDirectAccess";
|   analyzer[] = "Structures/NoEmptyRegex";
|   analyzer[] = "Structures/NoIssetWithEmpty";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoReferenceOnLeft";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/NonBreakableSpaceInNames";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/NotEqual";
|   analyzer[] = "Structures/NotNot";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/OnceUsage";
|   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";
|   analyzer[] = "Structures/OrDie";
|   analyzer[] = "Structures/PrintAndDie";
|   analyzer[] = "Structures/PrintWithoutParenthesis";
|   analyzer[] = "Structures/PrintfArguments";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/RepeatedRegex";
|   analyzer[] = "Structures/ResourcesUsage";
|   analyzer[] = "Structures/ResultMayBeMissing";
|   analyzer[] = "Structures/ReturnTrueFalse";
|   analyzer[] = "Structures/SameConditions";
|   analyzer[] = "Structures/ShellUsage";
|   analyzer[] = "Structures/ShortTags";
|   analyzer[] = "Structures/ShouldChainException";
|   analyzer[] = "Structures/ShouldMakeTernary";
|   analyzer[] = "Structures/ShouldUseExplodeArgs";
|   analyzer[] = "Structures/StripTagsSkipsClosedTag";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/SwitchWithoutDefault";
|   analyzer[] = "Structures/TernaryInConcat";
|   analyzer[] = "Structures/ThrowsAndAssign";
|   analyzer[] = "Structures/TimestampDifference";
|   analyzer[] = "Structures/TryFinally";
|   analyzer[] = "Structures/UncheckedResources";
|   analyzer[] = "Structures/UnconditionLoopBreak";
|   analyzer[] = "Structures/UnknownPregOption";
|   analyzer[] = "Structures/UnsupportedTypesWithOperators";
|   analyzer[] = "Structures/UseConstant";
|   analyzer[] = "Structures/UseDebug";
|   analyzer[] = "Structures/UseInstanceof";
|   analyzer[] = "Structures/UseSystemTmp";
|   analyzer[] = "Structures/UselessBrackets";
|   analyzer[] = "Structures/UselessCasting";
|   analyzer[] = "Structures/UselessCheck";
|   analyzer[] = "Structures/UselessInstruction";
|   analyzer[] = "Structures/UselessParenthesis";
|   analyzer[] = "Structures/UselessUnset";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Traits/IsExtTrait";
|   analyzer[] = "Traits/Php";
|   analyzer[] = "Traits/TraitUsage";
|   analyzer[] = "Traits/Traitnames";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";
|   analyzer[] = "Type/ArrayIndex";
|   analyzer[] = "Type/Binary";
|   analyzer[] = "Type/Email";
|   analyzer[] = "Type/GPCIndex";
|   analyzer[] = "Type/Heredoc";
|   analyzer[] = "Type/Hexadecimal";
|   analyzer[] = "Type/Md5String";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Type/Nowdoc";
|   analyzer[] = "Type/Octal";
|   analyzer[] = "Type/OneVariableStrings";
|   analyzer[] = "Type/Pack";
|   analyzer[] = "Type/Path";
|   analyzer[] = "Type/Printf";
|   analyzer[] = "Type/Protocols";
|   analyzer[] = "Type/Regex";
|   analyzer[] = "Type/Shellcommands";
|   analyzer[] = "Type/ShouldTypecast";
|   analyzer[] = "Type/SilentlyCastInteger";
|   analyzer[] = "Type/Sql";
|   analyzer[] = "Type/StringWithStrangeSpace";
|   analyzer[] = "Type/Url";
|   analyzer[] = "Typehints/CouldBeArray";
|   analyzer[] = "Typehints/CouldBeBoolean";
|   analyzer[] = "Typehints/CouldBeCIT";
|   analyzer[] = "Typehints/CouldBeFloat";
|   analyzer[] = "Typehints/CouldBeInt";
|   analyzer[] = "Typehints/CouldBeNull";
|   analyzer[] = "Typehints/CouldBeString";
|   analyzer[] = "Typehints/MissingReturntype";
|   analyzer[] = "Variables/References";
|   analyzer[] = "Variables/SelfTransform";
|   analyzer[] = "Variables/StaticVariables";
|   analyzer[] = "Variables/UncommonEnvVar";
|   analyzer[] = "Variables/UndefinedVariable";
|   analyzer[] = "Variables/VariableLong";
|   analyzer[] = "Variables/VariableUsedOnceByContext";
|   analyzer[] = "Variables/VariableVariables";
|   analyzer[] = "Vendors/Codeigniter";
|   analyzer[] = "Vendors/Concrete5";
|   analyzer[] = "Vendors/Drupal";
|   analyzer[] = "Vendors/Ez";
|   analyzer[] = "Vendors/Fuel";
|   analyzer[] = "Vendors/Joomla";
|   analyzer[] = "Vendors/Laravel";
|   analyzer[] = "Vendors/Phalcon";
|   analyzer[] = "Vendors/Symfony";
|   analyzer[] = "Vendors/Typo3";
|   analyzer[] = "Vendors/Wordpress";
|   analyzer[] = "Vendors/Yii";



.. _annex-ci-checks:

CI-checks
#########


| [CI-checks]
|   analyzer[] = "Arrays/MultipleIdenticalKeys";
|   analyzer[] = "Classes/CheckOnCallUsage";
|   analyzer[] = "Classes/DirectCallToMagicMethod";
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/MultipleDeclarations";
|   analyzer[] = "Classes/MultipleTraitOrInterface";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NonPpp";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/RedefinedConstants";
|   analyzer[] = "Classes/RedefinedDefault";
|   analyzer[] = "Classes/StaticContainsThis";
|   analyzer[] = "Classes/StaticMethodsCalledFromObject";
|   analyzer[] = "Classes/ThrowInDestruct";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UndefinedConstants";
|   analyzer[] = "Classes/UndefinedProperty";
|   analyzer[] = "Classes/UndefinedStaticclass";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Classes/UseInstanceof";
|   analyzer[] = "Classes/UselessFinal";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Constants/ConstantStrangeNames";
|   analyzer[] = "Constants/MultipleConstantDefinition";
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/ThrowFunctioncall";
|   analyzer[] = "Exceptions/UselessCatch";
|   analyzer[] = "Functions/AliasesUsage";
|   analyzer[] = "Functions/CallbackNeedsReturn";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/NoLiteralForReference";
|   analyzer[] = "Functions/RedeclaredPhpFunction";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Functions/TypehintedReferences";
|   analyzer[] = "Functions/UndefinedFunctions";
|   analyzer[] = "Functions/UnknownParameterName";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UseConstantAsArguments";
|   analyzer[] = "Functions/UsesDefaultArguments";
|   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
|   analyzer[] = "Functions/WrongNumberOfArguments";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/UndefinedInterfaces";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/HiddenUse";
|   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
|   analyzer[] = "Namespaces/MultipleAliasDefinitions";
|   analyzer[] = "Namespaces/ShouldMakeAlias";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/StrposTooMuch";
|   analyzer[] = "Performances/UseArraySlice";
|   analyzer[] = "Php/AssignAnd";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/Deprecated";
|   analyzer[] = "Php/FopenMode";
|   analyzer[] = "Php/InternalParameterType";
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Php/NoClassInGlobal";
|   analyzer[] = "Php/NoReferenceForTernary";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/StrtrArguments";
|   analyzer[] = "Php/UseObjectApi";
|   analyzer[] = "Php/UsePathinfo";
|   analyzer[] = "Php/WrongTypeForNativeFunction";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Structures/AddZero";
|   analyzer[] = "Structures/AlteringForeachWithoutReference";
|   analyzer[] = "Structures/AssigneAndCompare";
|   analyzer[] = "Structures/AutoUnsetForeach";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/CastingTernary";
|   analyzer[] = "Structures/CheckJson";
|   analyzer[] = "Structures/CoalesceAndConcat";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/DirThenSlash";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/EmptyBlocks";
|   analyzer[] = "Structures/ErrorReportingWithInteger";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/ExitUsage";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForeachReferenceIsNotModified";
|   analyzer[] = "Structures/ForgottenWhiteSpace";
|   analyzer[] = "Structures/Htmlentitiescall";
|   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
|   analyzer[] = "Structures/IdenticalConditions";
|   analyzer[] = "Structures/IdenticalOnBothSides";
|   analyzer[] = "Structures/IfWithSameConditions";
|   analyzer[] = "Structures/ImpliedIf";
|   analyzer[] = "Structures/ImplodeArgsOrder";
|   analyzer[] = "Structures/IndicesAreIntOrString";
|   analyzer[] = "Structures/InvalidPackFormat";
|   analyzer[] = "Structures/InvalidRegex";
|   analyzer[] = "Structures/IsZero";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LogicalMistakes";
|   analyzer[] = "Structures/LoneBlock";
|   analyzer[] = "Structures/MbstringThirdArg";
|   analyzer[] = "Structures/MbstringUnknownEncoding";
|   analyzer[] = "Structures/MergeIfThen";
|   analyzer[] = "Structures/MissingParenthesis";
|   analyzer[] = "Structures/MultipleDefinedCase";
|   analyzer[] = "Structures/MultiplyByOne";
|   analyzer[] = "Structures/NegativePow";
|   analyzer[] = "Structures/NestedTernary";
|   analyzer[] = "Structures/NeverNegative";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoEmptyRegex";
|   analyzer[] = "Structures/NoIssetWithEmpty";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoReferenceOnLeft";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/NotEqual";
|   analyzer[] = "Structures/NotNot";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/OrDie";
|   analyzer[] = "Structures/PrintAndDie";
|   analyzer[] = "Structures/PrintWithoutParenthesis";
|   analyzer[] = "Structures/PrintfArguments";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/RepeatedRegex";
|   analyzer[] = "Structures/ResultMayBeMissing";
|   analyzer[] = "Structures/ReturnTrueFalse";
|   analyzer[] = "Structures/SameConditions";
|   analyzer[] = "Structures/ShouldChainException";
|   analyzer[] = "Structures/ShouldMakeTernary";
|   analyzer[] = "Structures/ShouldUseExplodeArgs";
|   analyzer[] = "Structures/StripTagsSkipsClosedTag";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/SwitchWithoutDefault";
|   analyzer[] = "Structures/TernaryInConcat";
|   analyzer[] = "Structures/ThrowsAndAssign";
|   analyzer[] = "Structures/TimestampDifference";
|   analyzer[] = "Structures/UncheckedResources";
|   analyzer[] = "Structures/UnconditionLoopBreak";
|   analyzer[] = "Structures/UseConstant";
|   analyzer[] = "Structures/UseInstanceof";
|   analyzer[] = "Structures/UseSystemTmp";
|   analyzer[] = "Structures/UselessBrackets";
|   analyzer[] = "Structures/UselessCasting";
|   analyzer[] = "Structures/UselessCheck";
|   analyzer[] = "Structures/UselessInstruction";
|   analyzer[] = "Structures/UselessParenthesis";
|   analyzer[] = "Structures/UselessUnset";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Type/OneVariableStrings";
|   analyzer[] = "Type/ShouldTypecast";
|   analyzer[] = "Type/SilentlyCastInteger";
|   analyzer[] = "Type/StringWithStrangeSpace";
|   analyzer[] = "Typehints/MissingReturntype";
|   analyzer[] = "Variables/UndefinedVariable";



.. _annex-classreview:

ClassReview
###########


| [ClassReview]
|   analyzer[] = "Classes/AvoidOptionArrays";
|   analyzer[] = "Classes/CancelCommonMethod";
|   analyzer[] = "Classes/ConstantClass";
|   analyzer[] = "Classes/CouldBeAbstractClass";
|   analyzer[] = "Classes/CouldBeClassConstant";
|   analyzer[] = "Classes/CouldBeFinal";
|   analyzer[] = "Classes/CouldBeParentMethod";
|   analyzer[] = "Classes/CouldBePrivate";
|   analyzer[] = "Classes/CouldBePrivateConstante";
|   analyzer[] = "Classes/CouldBePrivateMethod";
|   analyzer[] = "Classes/CouldBeProtectedConstant";
|   analyzer[] = "Classes/CouldBeProtectedMethod";
|   analyzer[] = "Classes/CouldBeProtectedProperty";
|   analyzer[] = "Classes/CouldBeStatic";
|   analyzer[] = "Classes/CyclicReferences";
|   analyzer[] = "Classes/DependantAbstractClass";
|   analyzer[] = "Classes/DifferentArgumentCounts";
|   analyzer[] = "Classes/DisconnectedClasses";
|   analyzer[] = "Classes/FinalPrivate";
|   analyzer[] = "Classes/Finalclass";
|   analyzer[] = "Classes/Finalmethod";
|   analyzer[] = "Classes/FossilizedMethod";
|   analyzer[] = "Classes/HiddenNullable";
|   analyzer[] = "Classes/InheritedPropertyMustMatch";
|   analyzer[] = "Classes/InsufficientPropertyTypehint";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MissingAbstractMethod";
|   analyzer[] = "Classes/MutualExtension";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/NonNullableSetters";
|   analyzer[] = "Classes/PropertyCouldBeLocal";
|   analyzer[] = "Classes/RaisedAccessLevel";
|   analyzer[] = "Classes/RedefinedProperty";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UninitedProperty";
|   analyzer[] = "Classes/UnreachableConstant";
|   analyzer[] = "Classes/UnusedConstant";
|   analyzer[] = "Classes/UselessTypehint";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Functions/ExceedingTypehint";
|   analyzer[] = "Functions/ModifyTypedParameter";
|   analyzer[] = "Functions/NullableWithoutCheck";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Interfaces/AvoidSelfInInterface";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Performances/MemoizeMagicCall";
|   analyzer[] = "Php/MissingMagicIsset";
|   analyzer[] = "Structures/CouldBeStatic";
|   analyzer[] = "Structures/DoubleObjectAssignation";
|   analyzer[] = "Traits/SelfUsingTrait";
|   analyzer[] = "Traits/UnusedClassTrait";
|   analyzer[] = "Variables/NoStaticVarInMethod";



.. _annex-coding-conventions:

Coding conventions
##################


| [Coding conventions]
|   analyzer[] = "";



.. _annex-compatibilityphp53:

CompatibilityPHP53
##################


| [CompatibilityPHP53]
|   analyzer[] = "Arrays/ArrayNSUsage";
|   analyzer[] = "Arrays/MixedKeys";
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extdba";
|   analyzer[] = "Extensions/Extfdf";
|   analyzer[] = "Extensions/Extming";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/CantUseReturnValueInWriteContext";
|   analyzer[] = "Php/CaseForPSS";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/ClosureThisSupport";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/MethodCallOnNew";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php54NewFunctions";
|   analyzer[] = "Php/Php55NewFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/StaticclassUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/Break0";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/DereferencingAS";
|   analyzer[] = "Structures/ForeachWithList";
|   analyzer[] = "Structures/FunctionSubscripting";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/Binary";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";



.. _annex-compatibilityphp54:

CompatibilityPHP54
##################


| [CompatibilityPHP54]
|   analyzer[] = "Arrays/MixedKeys";
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extmhash";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/CantUseReturnValueInWriteContext";
|   analyzer[] = "Php/CaseForPSS";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php54RemovedFunctions";
|   analyzer[] = "Php/Php55NewFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/StaticclassUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/BreakNonInteger";
|   analyzer[] = "Structures/CalltimePassByReference";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/CryptWithoutSalt";
|   analyzer[] = "Structures/DereferencingAS";
|   analyzer[] = "Structures/ForeachWithList";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";



.. _annex-compatibilityphp55:

CompatibilityPHP55
##################


| [CompatibilityPHP55]
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extapc";
|   analyzer[] = "Extensions/Extmysql";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Password55";
|   analyzer[] = "Php/Php55RemovedFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";



.. _annex-compatibilityphp56:

CompatibilityPHP56
##################


| [CompatibilityPHP56]
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/RawPostDataUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";



.. _annex-compatibilityphp70:

CompatibilityPHP70
##################


| [CompatibilityPHP70]
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/toStringPss";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extereg";
|   analyzer[] = "Functions/funcGetArgModified";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EmptyList";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/ForeachDontChangePointer";
|   analyzer[] = "Php/GlobalWithoutSimpleVariable";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithAppends";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php70RemovedDirective";
|   analyzer[] = "Php/Php70RemovedFunctions";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/ReservedKeywords7";
|   analyzer[] = "Php/SetExceptionHandlerPHP7";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/UsortSorting";
|   analyzer[] = "Structures/BreakOutsideLoop";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/McryptcreateivWithoutOption";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/SetlocaleNeedsConstants";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Type/HexadecimalString";
|   analyzer[] = "Variables/Php7IndirectExpression";



.. _annex-compatibilityphp71:

CompatibilityPHP71
##################


| [CompatibilityPHP71]
|   analyzer[] = "Arrays/StringInitialization";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Extensions/Extmcrypt";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php70RemovedDirective";
|   analyzer[] = "Php/Php70RemovedFunctions";
|   analyzer[] = "Php/Php71NewFunctions";
|   analyzer[] = "Php/Php71RemovedDirective";
|   analyzer[] = "Php/Php71microseconds";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Type/HexadecimalString";
|   analyzer[] = "Type/OctalInString";



.. _annex-compatibilityphp72:

CompatibilityPHP72
##################


| [CompatibilityPHP72]
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Php/AvoidSetErrorHandlerContextArg";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashUsesObjects";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php72Deprecation";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php72NewConstants";
|   analyzer[] = "Php/Php72NewFunctions";
|   analyzer[] = "Php/Php72ObjectKeyword";
|   analyzer[] = "Php/Php72RemovedFunctions";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/CanCountNonCountable";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/pregOptionE";



.. _annex-compatibilityphp73:

CompatibilityPHP73
##################


| [CompatibilityPHP73]
|   analyzer[] = "Constants/CaseInsensitiveConstants";
|   analyzer[] = "Php/AssertFunctionIsReserved";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/CompactInexistant";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/IntegerSeparatorUsage";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php73RemovedFunctions";
|   analyzer[] = "Php/Php74NewDirective";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnknownPcre2Option";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";



.. _annex-compatibilityphp74:

CompatibilityPHP74
##################


| [CompatibilityPHP74]
|   analyzer[] = "Functions/UnbindingClosures";
|   analyzer[] = "Php/ArrayKeyExistsWithObjects";
|   analyzer[] = "Php/AvoidGetobjectVars";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/DetectCurrentClass";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/FilesFullPath";
|   analyzer[] = "Php/FilterToAddSlashes";
|   analyzer[] = "Php/HashAlgos74";
|   analyzer[] = "Php/IdnUts46";
|   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
|   analyzer[] = "Php/NoMoreCurlyArrays";
|   analyzer[] = "Php/Php74Deprecation";
|   analyzer[] = "Php/Php74NewClasses";
|   analyzer[] = "Php/Php74NewConstants";
|   analyzer[] = "Php/Php74NewFunctions";
|   analyzer[] = "Php/Php74RemovedDirective";
|   analyzer[] = "Php/Php74RemovedFunctions";
|   analyzer[] = "Php/Php74ReservedKeyword";
|   analyzer[] = "Php/Php74mbstrrpos3rdArg";
|   analyzer[] = "Php/Php80NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/Php80VariableSyntax";
|   analyzer[] = "Php/ReflectionExportIsDeprecated";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/UseMatch";
|   analyzer[] = "Structures/CurlVersionNow";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
|   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";



.. _annex-compatibilityphp80:

CompatibilityPHP80
##################


| [CompatibilityPHP80]
|   analyzer[] = "Arrays/NegativeStart";
|   analyzer[] = "Classes/FinalPrivate";
|   analyzer[] = "Classes/OldStyleConstructor";
|   analyzer[] = "Functions/MismatchParameterName";
|   analyzer[] = "Functions/NullableWithConstant";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Php/AvoidGetobjectVars";
|   analyzer[] = "Php/CastUnsetUsage";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EnumUsage";
|   analyzer[] = "Php/Php74RemovedDirective";
|   analyzer[] = "Php/Php80NamedParameterVariadic";
|   analyzer[] = "Php/Php80RemovedConstant";
|   analyzer[] = "Php/Php80RemovedDirective";
|   analyzer[] = "Php/Php80RemovedFunctions";
|   analyzer[] = "Php/Php80RemovesResources";
|   analyzer[] = "Php/PhpErrorMsgUsage";
|   analyzer[] = "Php/ReservedMatchKeyword";
|   analyzer[] = "Structures/ArrayMapPassesByValue";
|   analyzer[] = "Structures/UnsupportedTypesWithOperators";



.. _annex-compatibilityphp81:

CompatibilityPHP81
##################


| [CompatibilityPHP81]
|   analyzer[] = "Php/NativeClassTypeCompatibility";
|   analyzer[] = "Php/OpensslEncryptAlgoChange";
|   analyzer[] = "Php/Php74RemovedDirective";
|   analyzer[] = "Php/Php80RemovedDirective";
|   analyzer[] = "Php/Php81RemovedConstant";
|   analyzer[] = "Php/Php81RemovedDirective";
|   analyzer[] = "Php/RestrictGlobalUsage";
|   analyzer[] = "Variables/InheritedStaticVariable";



.. _annex-dead-code:

Dead code
#########


| [Dead code]
|   analyzer[] = "Classes/CantExtendFinal";
|   analyzer[] = "Classes/LocallyUnusedProperty";
|   analyzer[] = "Classes/UnresolvedCatch";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Classes/UnusedClass";
|   analyzer[] = "Classes/UnusedMethods";
|   analyzer[] = "Classes/UnusedPrivateMethod";
|   analyzer[] = "Classes/UnusedPrivateProperty";
|   analyzer[] = "Classes/UnusedProtectedMethods";
|   analyzer[] = "Constants/UnusedConstants";
|   analyzer[] = "Exceptions/AlreadyCaught";
|   analyzer[] = "Exceptions/CaughtButNotThrown";
|   analyzer[] = "Exceptions/Rethrown";
|   analyzer[] = "Exceptions/Unthrown";
|   analyzer[] = "Functions/UnusedFunctions";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UnusedReturnedValue";
|   analyzer[] = "Functions/UselessTypeCheck";
|   analyzer[] = "Interfaces/UnusedInterfaces";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/UnusedUse";
|   analyzer[] = "Structures/EmptyLines";
|   analyzer[] = "Structures/UnreachableCode";
|   analyzer[] = "Structures/UnsetInForeach";
|   analyzer[] = "Structures/UnusedLabel";
|   analyzer[] = "Traits/SelfUsingTrait";



.. _annex-lintbutwontexec:

LintButWontExec
###############


| [LintButWontExec]
|   analyzer[] = "Classes/AbstractOrImplements";
|   analyzer[] = "Classes/CloneWithNonObject";
|   analyzer[] = "Classes/CouldBeStringable";
|   analyzer[] = "Classes/Finalclass";
|   analyzer[] = "Classes/Finalmethod";
|   analyzer[] = "Classes/IncompatibleSignature";
|   analyzer[] = "Classes/InheritedPropertyMustMatch";
|   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MutualExtension";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoPSSOutsideClass";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/RaisedAccessLevel";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Exceptions/CantThrow";
|   analyzer[] = "Functions/DuplicateNamedParameter";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/OnlyVariableForReference";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/ConcreteVisibility";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/RepeatedInterface";
|   analyzer[] = "Php/OnlyVariableForReference";
|   analyzer[] = "Traits/MethodCollisionTraits";
|   analyzer[] = "Traits/TraitNotFound";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";



.. _annex-performances:

Performances
############


| [Performances]
|   analyzer[] = "Arrays/GettingLastElement";
|   analyzer[] = "Arrays/SliceFirst";
|   analyzer[] = "Classes/MakeMagicConcrete";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Functions/Closure2String";
|   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/Autoappend";
|   analyzer[] = "Performances/AvoidArrayPush";
|   analyzer[] = "Performances/CacheVariableOutsideLoop";
|   analyzer[] = "Performances/CsvInLoops";
|   analyzer[] = "Performances/DoInBase";
|   analyzer[] = "Performances/DoubleArrayFlip";
|   analyzer[] = "Performances/FetchOneRowFormat";
|   analyzer[] = "Performances/IssetWholeArray";
|   analyzer[] = "Performances/JoinFile";
|   analyzer[] = "Performances/MakeOneCall";
|   analyzer[] = "Performances/MbStringInLoop";
|   analyzer[] = "Performances/NoConcatInLoop";
|   analyzer[] = "Performances/NoGlob";
|   analyzer[] = "Performances/NotCountNull";
|   analyzer[] = "Performances/OptimizeExplode";
|   analyzer[] = "Performances/PHP7EncapsedStrings";
|   analyzer[] = "Performances/Php74ArrayKeyExists";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/RegexOnArrays";
|   analyzer[] = "Performances/RegexOnCollector";
|   analyzer[] = "Performances/SimpleSwitch";
|   analyzer[] = "Performances/SlowFunctions";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Performances/UseBlindVar";
|   analyzer[] = "Performances/timeVsstrtotime";
|   analyzer[] = "Php/ShouldUseArrayColumn";
|   analyzer[] = "Php/ShouldUseFunction";
|   analyzer[] = "Php/UsePathinfoArgs";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/ForWithFunctioncall";
|   analyzer[] = "Structures/GlobalOutsideLoop";
|   analyzer[] = "Structures/NoArrayUnique";
|   analyzer[] = "Structures/NoAssignationInFunction";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/SimplePreg";
|   analyzer[] = "Structures/WhileListEach";



.. _annex-rector:

Rector
######


| [Rector]
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/ShouldPreprocess";



.. _annex-security:

Security
########


| [Security]
|   analyzer[] = "Functions/HardcodedPasswords";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Security/AnchorRegex";
|   analyzer[] = "Security/AvoidThoseCrypto";
|   analyzer[] = "Security/CompareHash";
|   analyzer[] = "Security/ConfigureExtract";
|   analyzer[] = "Security/CryptoKeyLength";
|   analyzer[] = "Security/CurlOptions";
|   analyzer[] = "Security/DirectInjection";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/DynamicDl";
|   analyzer[] = "Security/EncodedLetters";
|   analyzer[] = "Security/FilterInputSource";
|   analyzer[] = "Security/IndirectInjection";
|   analyzer[] = "Security/IntegerConversion";
|   analyzer[] = "Security/KeepFilesRestricted";
|   analyzer[] = "Security/MinusOneOnError";
|   analyzer[] = "Security/MkdirDefault";
|   analyzer[] = "Security/MoveUploadedFile";
|   analyzer[] = "Security/NoEntIgnore";
|   analyzer[] = "Security/NoNetForXmlLoad";
|   analyzer[] = "Security/NoSleep";
|   analyzer[] = "Security/NoWeakSSLCrypto";
|   analyzer[] = "Security/RegisterGlobals";
|   analyzer[] = "Security/SafeHttpHeaders";
|   analyzer[] = "Security/SessionLazyWrite";
|   analyzer[] = "Security/SetCookieArgs";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Security/ShouldUseSessionRegenerateId";
|   analyzer[] = "Security/Sqlite3RequiresSingleQuotes";
|   analyzer[] = "Security/UnserializeSecondArg";
|   analyzer[] = "Security/UploadFilenameInjection";
|   analyzer[] = "Security/parseUrlWithoutParameters";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/Fallthrough";
|   analyzer[] = "Structures/NoHardcodedHash";
|   analyzer[] = "Structures/NoHardcodedIp";
|   analyzer[] = "Structures/NoHardcodedPort";
|   analyzer[] = "Structures/NoReturnInFinally";
|   analyzer[] = "Structures/PhpinfoUsage";
|   analyzer[] = "Structures/RandomWithoutTry";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/pregOptionE";



.. _annex-semantics:

Semantics
#########


| [Semantics]
|   analyzer[] = "Arrays/WeirdIndex";
|   analyzer[] = "Functions/FnArgumentVariableConfusion";
|   analyzer[] = "Functions/MismatchParameterAndType";
|   analyzer[] = "Functions/OneLetterFunctions";
|   analyzer[] = "Functions/ParameterHiding";
|   analyzer[] = "Functions/PrefixToType";
|   analyzer[] = "Functions/SemanticTyping";
|   analyzer[] = "Functions/WrongTypehintedName";
|   analyzer[] = "Php/ClassFunctionConfusion";
|   analyzer[] = "Structures/PropertyVariableConfusion";
|   analyzer[] = "Type/DuplicateLiteral";
|   analyzer[] = "Type/SimilarIntegers";
|   analyzer[] = "Variables/VariableOneLetter";



.. _annex-suggestions:

Suggestions
###########


| [Suggestions]
|   analyzer[] = "Arrays/RandomlySortedLiterals";
|   analyzer[] = "Arrays/ShouldPreprocess";
|   analyzer[] = "Arrays/SliceFirst";
|   analyzer[] = "Classes/CancelCommonMethod";
|   analyzer[] = "Classes/ParentFirst";
|   analyzer[] = "Classes/ShouldDeepClone";
|   analyzer[] = "Classes/ShouldHaveDestructor";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/TooManyChildren";
|   analyzer[] = "Classes/UnitializedProperties";
|   analyzer[] = "Classes/UselessTypehint";
|   analyzer[] = "Constants/CouldBeConstant";
|   analyzer[] = "Exceptions/CouldUseTry";
|   analyzer[] = "Exceptions/LargeTryBlock";
|   analyzer[] = "Exceptions/LongPreparation";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/UnusedExceptionVariable";
|   analyzer[] = "Functions/AddDefaultValue";
|   analyzer[] = "Functions/Closure2String";
|   analyzer[] = "Functions/CouldBeStaticClosure";
|   analyzer[] = "Functions/CouldCentralize";
|   analyzer[] = "Functions/NeverUsedParameter";
|   analyzer[] = "Functions/NoReturnUsed";
|   analyzer[] = "Functions/TooManyParameters";
|   analyzer[] = "Functions/TooMuchIndented";
|   analyzer[] = "Functions/UselessDefault";
|   analyzer[] = "Interfaces/AlreadyParentsInterface";
|   analyzer[] = "Interfaces/UnusedInterfaces";
|   analyzer[] = "Namespaces/AliasConfusion";
|   analyzer[] = "Namespaces/CouldUseAlias";
|   analyzer[] = "Patterns/AbstractAway";
|   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
|   analyzer[] = "Performances/IssetWholeArray";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Php/AvoidReal";
|   analyzer[] = "Php/CompactInexistant";
|   analyzer[] = "Php/CouldUseIsCountable";
|   analyzer[] = "Php/CouldUsePromotedProperties";
|   analyzer[] = "Php/DetectCurrentClass";
|   analyzer[] = "Php/ImplodeOneArg";
|   analyzer[] = "Php/IssetMultipleArgs";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/NewExponent";
|   analyzer[] = "Php/PregMatchAllFlag";
|   analyzer[] = "Php/ReturnWithParenthesis";
|   analyzer[] = "Php/ShouldPreprocess";
|   analyzer[] = "Php/ShouldUseArrayColumn";
|   analyzer[] = "Php/ShouldUseArrayFilter";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/UseDateTimeImmutable";
|   analyzer[] = "Php/UseGetDebugType";
|   analyzer[] = "Php/UseSessionStartOptions";
|   analyzer[] = "Php/UseStrContains";
|   analyzer[] = "Structures/ArraySearchMultipleKeys";
|   analyzer[] = "Structures/BasenameSuffix";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/CouldUseArrayFillKeys";
|   analyzer[] = "Structures/CouldUseArrayUnique";
|   analyzer[] = "Structures/CouldUseCompact";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseMatch";
|   analyzer[] = "Structures/DeclareStaticOnce";
|   analyzer[] = "Structures/DirectlyUseFile";
|   analyzer[] = "Structures/DontCompareTypedBoolean";
|   analyzer[] = "Structures/DontLoopOnYield";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/EmptyWithExpression";
|   analyzer[] = "Structures/FunctionPreSubscripting";
|   analyzer[] = "Structures/JsonWithOption";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LongBlock";
|   analyzer[] = "Structures/MismatchedTernary";
|   analyzer[] = "Structures/MultipleUnset";
|   analyzer[] = "Structures/NamedRegex";
|   analyzer[] = "Structures/NoNeedGetClass";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/OneIfIsSufficient";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/PossibleIncrement";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/ReuseVariable";
|   analyzer[] = "Structures/SGVariablesConfusion";
|   analyzer[] = "Structures/SetAside";
|   analyzer[] = "Structures/ShouldUseForeach";
|   analyzer[] = "Structures/ShouldUseMath";
|   analyzer[] = "Structures/ShouldUseOperator";
|   analyzer[] = "Structures/SubstrLastArg";
|   analyzer[] = "Structures/SubstrToTrim";
|   analyzer[] = "Structures/UnreachableCode";
|   analyzer[] = "Structures/UseArrayFunctions";
|   analyzer[] = "Structures/UseCaseValue";
|   analyzer[] = "Structures/UseCountRecursive";
|   analyzer[] = "Structures/UseListWithForeach";
|   analyzer[] = "Structures/UseUrlQueryFunctions";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Traits/MultipleUsage";
|   analyzer[] = "Variables/ComplexDynamicNames";
|   analyzer[] = "Variables/NoStaticVarInMethod";



.. _annex-top10:

Top10
#####


| [Top10]
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/UnitializedProperties";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/CsvInLoops";
|   analyzer[] = "Performances/NoConcatInLoop";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Php/AvoidReal";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/LetterCharsLogicalFavorite";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForWithFunctioncall";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/QueriesInLoop";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/UseListWithForeach";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Variables/VariableUsedOnce";



.. _annex-typechecks:

Typechecks
##########


| [Typechecks]
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/FossilizedMethod";
|   analyzer[] = "Functions/BadTypehintRelay";
|   analyzer[] = "Functions/InsufficientTypehint";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MismatchedDefaultArguments";
|   analyzer[] = "Functions/MismatchedTypehint";
|   analyzer[] = "Functions/MissingTypehint";
|   analyzer[] = "Functions/NoClassAsTypehint";
|   analyzer[] = "Functions/ShouldBeTypehinted";
|   analyzer[] = "Functions/WrongArgumentType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Php/NotScalarType";
|   analyzer[] = "Typehints/CouldBeCallable";
|   analyzer[] = "Typehints/CouldBeFloat";
|   analyzer[] = "Typehints/CouldBeGenerator";
|   analyzer[] = "Typehints/CouldBeInt";
|   analyzer[] = "Typehints/CouldBeIterable";
|   analyzer[] = "Typehints/CouldBeNull";
|   analyzer[] = "Typehints/CouldBeParent";
|   analyzer[] = "Typehints/CouldBeSelf";
|   analyzer[] = "Typehints/CouldBeString";
|   analyzer[] = "Typehints/CouldBeVoid";



.. _annex-php-cs-fixable:

php-cs-fixable
##############


| [php-cs-fixable]
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Php/ImplodeOneArg";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/IssetMultipleArgs";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/NewExponent";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/MultipleUnset";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/UseConstant";



