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

46 rulesets detailled here : 

.. _annex-all:

All
###


.. _annex-ini-all:

All for INI
+++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [All]
   analyzer[] = "Arrays/AmbiguousKeys";
   analyzer[] = "Arrays/AppendAndAssignArrays";
   analyzer[] = "Arrays/ArrayBracketConsistence";
   analyzer[] = "Arrays/ArrayNSUsage";
   analyzer[] = "Arrays/Arrayindex";
   analyzer[] = "Arrays/EmptyFinal";
   analyzer[] = "Arrays/EmptySlots";
   analyzer[] = "Arrays/FloatConversionAsIndex";
   analyzer[] = "Arrays/GettingLastElement";
   analyzer[] = "Arrays/MassCreation";
   analyzer[] = "Arrays/MistakenConcatenation";
   analyzer[] = "Arrays/MixedKeys";
   analyzer[] = "Arrays/Multidimensional";
   analyzer[] = "Arrays/MultipleIdenticalKeys";
   analyzer[] = "Arrays/NegativeStart";
   analyzer[] = "Arrays/NoSpreadForHash";
   analyzer[] = "Arrays/NonConstantArray";
   analyzer[] = "Arrays/NullBoolean";
   analyzer[] = "Arrays/Phparrayindex";
   analyzer[] = "Arrays/RandomlySortedLiterals";
   analyzer[] = "Arrays/ShouldPreprocess";
   analyzer[] = "Arrays/SliceFirst";
   analyzer[] = "Arrays/StringInitialization";
   analyzer[] = "Arrays/TooManyDimensions";
   analyzer[] = "Arrays/WeakType";
   analyzer[] = "Arrays/WeirdIndex";
   analyzer[] = "Arrays/WithCallback";
   analyzer[] = "Attributes/Deprecated";
   analyzer[] = "Attributes/Friend";
   analyzer[] = "Attributes/InjectableVersion";
   analyzer[] = "Attributes/MissingAttributeAttribute";
   analyzer[] = "Attributes/MissingOverrideMethod";
   analyzer[] = "Attributes/ModifyImmutable";
   analyzer[] = "Attributes/MustUseResult";
   analyzer[] = "Attributes/MustUseReturnReturns";
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Attributes/NoNamedArguments";
   analyzer[] = "Attributes/Override";
   analyzer[] = "Attributes/PhpNativeAttributes";
   analyzer[] = "Attributes/UselessOverride";
   analyzer[] = "Attributes/UsingDeprecated";
   analyzer[] = "Classes/AbstractConstants";
   analyzer[] = "Classes/AbstractOrImplements";
   analyzer[] = "Classes/AbstractStatic";
   analyzer[] = "Classes/Abstractclass";
   analyzer[] = "Classes/Abstractmethods";
   analyzer[] = "Classes/AccessPrivate";
   analyzer[] = "Classes/AccessProtected";
   analyzer[] = "Classes/AmbiguousStatic";
   analyzer[] = "Classes/AmbiguousVisibilities";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/AvoidOptionArrays";
   analyzer[] = "Classes/AvoidOptionalProperties";
   analyzer[] = "Classes/AvoidUsing";
   analyzer[] = "Classes/CancelCommonMethod";
   analyzer[] = "Classes/CannotBeReadonly";
   analyzer[] = "Classes/CantExtendFinal";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/CantInstantiateClass";
   analyzer[] = "Classes/CantInstantiateNonClass";
   analyzer[] = "Classes/CantOverwriteFinalConstant";
   analyzer[] = "Classes/CantOverwriteFinalMethod";
   analyzer[] = "Classes/CheckAfterNullSafeOperator";
   analyzer[] = "Classes/CheckOnCallUsage";
   analyzer[] = "Classes/ChecksPropertyExistence";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/CitSameName";
   analyzer[] = "Classes/ClassAliasUsage";
   analyzer[] = "Classes/ClassInvasion";
   analyzer[] = "Classes/ClassOverreach";
   analyzer[] = "Classes/ClassUsage";
   analyzer[] = "Classes/Classnames";
   analyzer[] = "Classes/CloneWithNonObject";
   analyzer[] = "Classes/CloningUsage";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/ConstantClass";
   analyzer[] = "Classes/ConstantDefinition";
   analyzer[] = "Classes/ConstantUsedBelow";
   analyzer[] = "Classes/Constructor";
   analyzer[] = "Classes/CouldBeAbstractClass";
   analyzer[] = "Classes/CouldBeAbstractMethod";
   analyzer[] = "Classes/CouldBeClassConstant";
   analyzer[] = "Classes/CouldBeFinal";
   analyzer[] = "Classes/CouldBeIterable";
   analyzer[] = "Classes/CouldBeParentMethod";
   analyzer[] = "Classes/CouldBePrivate";
   analyzer[] = "Classes/CouldBePrivateConstante";
   analyzer[] = "Classes/CouldBePrivateMethod";
   analyzer[] = "Classes/CouldBeProtectedConstant";
   analyzer[] = "Classes/CouldBeProtectedMethod";
   analyzer[] = "Classes/CouldBeProtectedProperty";
   analyzer[] = "Classes/CouldBeReadonly";
   analyzer[] = "Classes/CouldBeReadonlyProperty";
   analyzer[] = "Classes/CouldBeStatic";
   analyzer[] = "Classes/CouldBeStringable";
   analyzer[] = "Classes/CouldInjectParam";
   analyzer[] = "Classes/CouldSetPropertyDefault";
   analyzer[] = "Classes/CouldUseClassOperator";
   analyzer[] = "Classes/CyclicReferences";
   analyzer[] = "Classes/DefinedConstants";
   analyzer[] = "Classes/DefinedParentMP";
   analyzer[] = "Classes/DefinedProperty";
   analyzer[] = "Classes/DefinedStaticMP";
   analyzer[] = "Classes/DemeterLaw";
   analyzer[] = "Classes/DependantAbstractClass";
   analyzer[] = "Classes/DifferentArgumentCounts";
   analyzer[] = "Classes/DirectCallToMagicMethod";
   analyzer[] = "Classes/DisconnectedClasses";
   analyzer[] = "Classes/DontSendThisInConstructor";
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/DynamicClass";
   analyzer[] = "Classes/DynamicConstantCall";
   analyzer[] = "Classes/DynamicMethodCall";
   analyzer[] = "Classes/DynamicNew";
   analyzer[] = "Classes/DynamicPropertyCall";
   analyzer[] = "Classes/DynamicSelfCalls";
   analyzer[] = "Classes/EmptyClass";
   analyzer[] = "Classes/ExportProperty";
   analyzer[] = "Classes/ExtendsStdclass";
   analyzer[] = "Classes/FinalByOcramius";
   analyzer[] = "Classes/FinalPrivate";
   analyzer[] = "Classes/Finalclass";
   analyzer[] = "Classes/Finalmethod";
   analyzer[] = "Classes/FossilizedMethod";
   analyzer[] = "Classes/HasFluentInterface";
   analyzer[] = "Classes/HasMagicProperty";
   analyzer[] = "Classes/HiddenNullable";
   analyzer[] = "Classes/IdenticalMethods";
   analyzer[] = "Classes/ImmutableSignature";
   analyzer[] = "Classes/ImplementIsForInterface";
   analyzer[] = "Classes/ImplementedMethodsArePublic";
   analyzer[] = "Classes/IncompatibleConstructor";
   analyzer[] = "Classes/IncompatibleSignature";
   analyzer[] = "Classes/IncompatibleSignature74";
   analyzer[] = "Classes/InheritedPropertyMustMatch";
   analyzer[] = "Classes/InstantiatingAbstractClass";
   analyzer[] = "Classes/InsufficientPropertyTypehint";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/IsExtClass";
   analyzer[] = "Classes/IsInterfaceMethod";
   analyzer[] = "Classes/IsNotFamily";
   analyzer[] = "Classes/IsUpperFamily";
   analyzer[] = "Classes/IsaMagicProperty";
   analyzer[] = "Classes/LocallyUnusedProperty";
   analyzer[] = "Classes/LocallyUsedProperty";
   analyzer[] = "Classes/LoweredAccessLevel";
   analyzer[] = "Classes/MagicMethod";
   analyzer[] = "Classes/MagicMethodReturntypes";
   analyzer[] = "Classes/MagicProperties";
   analyzer[] = "Classes/MakeDefault";
   analyzer[] = "Classes/MakeGlobalAProperty";
   analyzer[] = "Classes/MakeMagicConcrete";
   analyzer[] = "Classes/MethodIsOverwritten";
   analyzer[] = "Classes/MethodPropertyConfusion";
   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
   analyzer[] = "Classes/MethodUsedBelow";
   analyzer[] = "Classes/MismatchProperties";
   analyzer[] = "Classes/MissingAbstractMethod";
   analyzer[] = "Classes/MissingVisibility";
   analyzer[] = "Classes/MultipleClassesInFile";
   analyzer[] = "Classes/MultipleDeclarations";
   analyzer[] = "Classes/MultiplePropertyDeclaration";
   analyzer[] = "Classes/MultiplePropertyDeclarationOnOneLine";
   analyzer[] = "Classes/MultipleTraitOrInterface";
   analyzer[] = "Classes/MutualExtension";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NewOnFunctioncallOrIdentifier";
   analyzer[] = "Classes/NewThenCall";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoNullWithNullSafeOperator";
   analyzer[] = "Classes/NoPSSOutsideClass";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NoPublicAccess";
   analyzer[] = "Classes/NoReadonlyAssignationInGlobal";
   analyzer[] = "Classes/NoSelfReferencingConstant";
   analyzer[] = "Classes/NonNullableSetters";
   analyzer[] = "Classes/NonPpp";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NormalMethods";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/OldStyleVar";
   analyzer[] = "Classes/OneObjectOperatorPerLine";
   analyzer[] = "Classes/OnlyStaticMethods";
   analyzer[] = "Classes/OrderOfDeclaration";
   analyzer[] = "Classes/OverwrittenConst";
   analyzer[] = "Classes/PPPDeclarationStyle";
   analyzer[] = "Classes/ParentFirst";
   analyzer[] = "Classes/ParentIsNotStatic";
   analyzer[] = "Classes/PromotedProperties";
   analyzer[] = "Classes/PropertyCouldBeLocal";
   analyzer[] = "Classes/PropertyDefinition";
   analyzer[] = "Classes/PropertyInvasion";
   analyzer[] = "Classes/PropertyMethodSameName";
   analyzer[] = "Classes/PropertyNeverUsed";
   analyzer[] = "Classes/PropertyUsedAbove";
   analyzer[] = "Classes/PropertyUsedBelow";
   analyzer[] = "Classes/PropertyUsedInOneMethodOnly";
   analyzer[] = "Classes/PropertyUsedInternally";
   analyzer[] = "Classes/PssWithoutClass";
   analyzer[] = "Classes/RaisedAccessLevel";
   analyzer[] = "Classes/ReadonlyUsage";
   analyzer[] = "Classes/RedefinedConstants";
   analyzer[] = "Classes/RedefinedDefault";
   analyzer[] = "Classes/RedefinedMethods";
   analyzer[] = "Classes/RedefinedPrivateProperty";
   analyzer[] = "Classes/RedefinedProperty";
   analyzer[] = "Classes/RewroteFinalClassConstant";
   analyzer[] = "Classes/SameNameAsFile";
   analyzer[] = "Classes/ScalarOrObjectProperty";
   analyzer[] = "Classes/ShouldDeepClone";
   analyzer[] = "Classes/ShouldHaveDestructor";
   analyzer[] = "Classes/ShouldUseSelf";
   analyzer[] = "Classes/ShouldUseThis";
   analyzer[] = "Classes/StaticCannotCallNonStatic";
   analyzer[] = "Classes/StaticContainsThis";
   analyzer[] = "Classes/StaticMethods";
   analyzer[] = "Classes/StaticMethodsCalledFromObject";
   analyzer[] = "Classes/StaticProperties";
   analyzer[] = "Classes/StrangeName";
   analyzer[] = "Classes/SwappedArguments";
   analyzer[] = "Classes/TestClass";
   analyzer[] = "Classes/ThisIsForClasses";
   analyzer[] = "Classes/ThisIsNotAnArray";
   analyzer[] = "Classes/ThisIsNotForStatic";
   analyzer[] = "Classes/ThrowInDestruct";
   analyzer[] = "Classes/TooManyChildren";
   analyzer[] = "Classes/TooManyDereferencing";
   analyzer[] = "Classes/TooManyFinds";
   analyzer[] = "Classes/TooManyInjections";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Classes/TypehintCyclicDependencies";
   analyzer[] = "Classes/UndeclaredStaticProperty";
   analyzer[] = "Classes/UndefinedClasses";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UndefinedMethod";
   analyzer[] = "Classes/UndefinedParentMP";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Classes/UndefinedStaticMP";
   analyzer[] = "Classes/UndefinedStaticclass";
   analyzer[] = "Classes/UnfinishedObject";
   analyzer[] = "Classes/UninitedProperty";
   analyzer[] = "Classes/UnitializedProperties";
   analyzer[] = "Classes/UnreachableConstant";
   analyzer[] = "Classes/UnreachableMethod";
   analyzer[] = "Classes/UnresolvedCatch";
   analyzer[] = "Classes/UnresolvedClasses";
   analyzer[] = "Classes/UnresolvedInstanceof";
   analyzer[] = "Classes/UntypedNoDefaultProperties";
   analyzer[] = "Classes/UnusedClass";
   analyzer[] = "Classes/UnusedConstant";
   analyzer[] = "Classes/UnusedMethods";
   analyzer[] = "Classes/UnusedPrivateMethod";
   analyzer[] = "Classes/UnusedPrivateProperty";
   analyzer[] = "Classes/UnusedProtectedMethods";
   analyzer[] = "Classes/UnusedPublicMethod";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Classes/UseInstanceof";
   analyzer[] = "Classes/UseThis";
   analyzer[] = "Classes/UsedClass";
   analyzer[] = "Classes/UsedMethods";
   analyzer[] = "Classes/UsedOnceProperty";
   analyzer[] = "Classes/UsedPrivateMethod";
   analyzer[] = "Classes/UsedPrivateProperty";
   analyzer[] = "Classes/UsedProtectedMethod";
   analyzer[] = "Classes/UselessAbstract";
   analyzer[] = "Classes/UselessAssignationOfPromotedProperty";
   analyzer[] = "Classes/UselessConstantOverwrite";
   analyzer[] = "Classes/UselessConstructor";
   analyzer[] = "Classes/UselessFinal";
   analyzer[] = "Classes/UselessMethod";
   analyzer[] = "Classes/UselessNullSafeOperator";
   analyzer[] = "Classes/UselessTypehint";
   analyzer[] = "Classes/UsingThisOutsideAClass";
   analyzer[] = "Classes/VariableClasses";
   analyzer[] = "Classes/WeakType";
   analyzer[] = "Classes/WrongCase";
   analyzer[] = "Classes/WrongName";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Classes/toStringPss";
   analyzer[] = "Common/InterfaceUsage";
   analyzer[] = "Complete/CreateCompactVariables";
   analyzer[] = "Complete/CreateDefaultValues";
   analyzer[] = "Complete/CreateForeachDefault";
   analyzer[] = "Complete/CreateMagicMethod";
   analyzer[] = "Complete/CreateMagicProperty";
   analyzer[] = "Complete/EnumCaseValues";
   analyzer[] = "Complete/ExtendedTypehints";
   analyzer[] = "Complete/FollowClosureDefinition";
   analyzer[] = "Complete/GlobalDefinitions";
   analyzer[] = "Complete/IsExtStructure";
   analyzer[] = "Complete/IsPhpStructure";
   analyzer[] = "Complete/IsStubStructure";
   analyzer[] = "Complete/MakeAllStatics";
   analyzer[] = "Complete/MakeClassConstantDefinition";
   analyzer[] = "Complete/MakeClassMethodDefinition";
   analyzer[] = "Complete/MakeFunctioncallWithReference";
   analyzer[] = "Complete/OverwrittenConstants";
   analyzer[] = "Complete/OverwrittenMethods";
   analyzer[] = "Complete/OverwrittenProperties";
   analyzer[] = "Complete/PhpExtStubPropertyMethod";
   analyzer[] = "Complete/PhpNativeReference";
   analyzer[] = "Complete/PropagateConstants";
   analyzer[] = "Complete/ReturnTypehint";
   analyzer[] = "Complete/SetArrayClassDefinition";
   analyzer[] = "Complete/SetClassAliasDefinition";
   analyzer[] = "Complete/SetClassMethodRemoteDefinition";
   analyzer[] = "Complete/SetClassPropertyDefinitionWithTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithGlobal";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithInjection";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithLocalNew";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithParenthesis";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithReturnTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithTypehint";
   analyzer[] = "Complete/SetCloneLink";
   analyzer[] = "Complete/SetMethodFnp";
   analyzer[] = "Complete/SetParentDefinition";
   analyzer[] = "Complete/SolveTraitConstants";
   analyzer[] = "Complete/SolveTraitMethods";
   analyzer[] = "Complete/Superglobals";
   analyzer[] = "Complete/VariableTypehint";
   analyzer[] = "Composer/Autoload";
   analyzer[] = "Composer/UseComposer";
   analyzer[] = "Composer/UseComposerLock";
   analyzer[] = "Constants/BadConstantnames";
   analyzer[] = "Constants/CaseInsensitiveConstants";
   analyzer[] = "Constants/ConditionedConstants";
   analyzer[] = "Constants/ConstDefinePreference";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Constants/ConstantStrangeNames";
   analyzer[] = "Constants/ConstantUsage";
   analyzer[] = "Constants/ConstantUsedOnce";
   analyzer[] = "Constants/Constantnames";
   analyzer[] = "Constants/CouldBeConstant";
   analyzer[] = "Constants/CouldUseConstant";
   analyzer[] = "Constants/CreatedOutsideItsNamespace";
   analyzer[] = "Constants/CustomConstantUsage";
   analyzer[] = "Constants/DefineInsensitivePreference";
   analyzer[] = "Constants/DynamicCreation";
   analyzer[] = "Constants/InconsistantCase";
   analyzer[] = "Constants/InvalidName";
   analyzer[] = "Constants/IsExtConstant";
   analyzer[] = "Constants/IsGlobalConstant";
   analyzer[] = "Constants/IsPhpConstant";
   analyzer[] = "Constants/MagicConstantUsage";
   analyzer[] = "Constants/MultipleConstantDefinition";
   analyzer[] = "Constants/PhpConstantUsage";
   analyzer[] = "Constants/RelayConstant";
   analyzer[] = "Constants/StrangeName";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Constants/UnusedConstants";
   analyzer[] = "Constants/VariableConstant";
   analyzer[] = "Custom/MethodUsage";
   analyzer[] = "Dump/ArgumentCountsPerCalls";
   analyzer[] = "Dump/CallOrder";
   analyzer[] = "Dump/ClassInjectionCount";
   analyzer[] = "Dump/CollectAtomCounts";
   analyzer[] = "Dump/CollectBlockSize";
   analyzer[] = "Dump/CollectCalls";
   analyzer[] = "Dump/CollectCatch";
   analyzer[] = "Dump/CollectClassChanges";
   analyzer[] = "Dump/CollectClassChildren";
   analyzer[] = "Dump/CollectClassConstantCounts";
   analyzer[] = "Dump/CollectClassDepth";
   analyzer[] = "Dump/CollectClassInterfaceCounts";
   analyzer[] = "Dump/CollectClassTraitsCounts";
   analyzer[] = "Dump/CollectClassesDependencies";
   analyzer[] = "Dump/CollectDefinitionsStats";
   analyzer[] = "Dump/CollectDependencyExtension";
   analyzer[] = "Dump/CollectFilesDependencies";
   analyzer[] = "Dump/CollectForeachFavorite";
   analyzer[] = "Dump/CollectGlobalVariables";
   analyzer[] = "Dump/CollectGraphTriplets";
   analyzer[] = "Dump/CollectLiterals";
   analyzer[] = "Dump/CollectLocalVariableCounts";
   analyzer[] = "Dump/CollectMbstringEncodings";
   analyzer[] = "Dump/CollectMethodCounts";
   analyzer[] = "Dump/CollectMethodsThrowingExceptions";
   analyzer[] = "Dump/CollectNativeCallsPerExpressions";
   analyzer[] = "Dump/CollectParameterCounts";
   analyzer[] = "Dump/CollectParameterNames";
   analyzer[] = "Dump/CollectPhpStructures";
   analyzer[] = "Dump/CollectPropertyCounts";
   analyzer[] = "Dump/CollectPropertyUsage";
   analyzer[] = "Dump/CollectReadability";
   analyzer[] = "Dump/CollectSetLocale";
   analyzer[] = "Dump/CollectStructures";
   analyzer[] = "Dump/CollectStubStructures";
   analyzer[] = "Dump/CollectThrow";
   analyzer[] = "Dump/CollectUseCounts";
   analyzer[] = "Dump/CollectVariables";
   analyzer[] = "Dump/CollectVendorStructures";
   analyzer[] = "Dump/CollectsNames";
   analyzer[] = "Dump/CombinedCalls";
   analyzer[] = "Dump/ConstantOrder";
   analyzer[] = "Dump/CouldBeAConstant";
   analyzer[] = "Dump/CyclomaticComplexity";
   analyzer[] = "Dump/DereferencingLevels";
   analyzer[] = "Dump/DumpComparedLiterals";
   analyzer[] = "Dump/EnvironnementVariables";
   analyzer[] = "Dump/FossilizedMethods";
   analyzer[] = "Dump/Inclusions";
   analyzer[] = "Dump/IndentationLevels";
   analyzer[] = "Dump/NewOrder";
   analyzer[] = "Dump/ParameterArgumentsLinks";
   analyzer[] = "Dump/PublicReach";
   analyzer[] = "Dump/TypehintingStats";
   analyzer[] = "Dump/Typehintorder";
   analyzer[] = "Enums/CouldBeEnum";
   analyzer[] = "Enums/DuplicateCaseValue";
   analyzer[] = "Enums/NoMagicMethod";
   analyzer[] = "Enums/UndefinedEnumcase";
   analyzer[] = "Enums/UnusedEnumCase";
   analyzer[] = "Exceptions/AlreadyCaught";
   analyzer[] = "Exceptions/AnonymousCatch";
   analyzer[] = "Exceptions/CantThrow";
   analyzer[] = "Exceptions/CatchE";
   analyzer[] = "Exceptions/CatchUndefinedVariable";
   analyzer[] = "Exceptions/CaughtButNotThrown";
   analyzer[] = "Exceptions/CaughtExceptions";
   analyzer[] = "Exceptions/ConvertedExceptions";
   analyzer[] = "Exceptions/CouldDropVariable";
   analyzer[] = "Exceptions/CouldUseTry";
   analyzer[] = "Exceptions/DefinedExceptions";
   analyzer[] = "Exceptions/ForgottenThrown";
   analyzer[] = "Exceptions/IsPhpException";
   analyzer[] = "Exceptions/LargeTryBlock";
   analyzer[] = "Exceptions/LongPreparation";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/PossibleTypeError";
   analyzer[] = "Exceptions/Rethrown";
   analyzer[] = "Exceptions/SetChainingException";
   analyzer[] = "Exceptions/ThrowFunctioncall";
   analyzer[] = "Exceptions/ThrowRawExceptions";
   analyzer[] = "Exceptions/ThrownExceptions";
   analyzer[] = "Exceptions/TryNoCatch";
   analyzer[] = "Exceptions/UncaughtExceptions";
   analyzer[] = "Exceptions/Unthrown";
   analyzer[] = "Exceptions/UnusedExceptionVariable";
   analyzer[] = "Exceptions/UselessCatch";
   analyzer[] = "Exceptions/UselessTry";
   analyzer[] = "Extensions/Extamqp";
   analyzer[] = "Extensions/Extapache";
   analyzer[] = "Extensions/Extapc";
   analyzer[] = "Extensions/Extapcu";
   analyzer[] = "Extensions/Extarray";
   analyzer[] = "Extensions/Extast";
   analyzer[] = "Extensions/Extbcmath";
   analyzer[] = "Extensions/Extbzip2";
   analyzer[] = "Extensions/Extcalendar";
   analyzer[] = "Extensions/Extcmark";
   analyzer[] = "Extensions/Extcom";
   analyzer[] = "Extensions/Extcrypto";
   analyzer[] = "Extensions/Extcsv";
   analyzer[] = "Extensions/Extctype";
   analyzer[] = "Extensions/Extcurl";
   analyzer[] = "Extensions/Extdate";
   analyzer[] = "Extensions/Extdb2";
   analyzer[] = "Extensions/Extdba";
   analyzer[] = "Extensions/Extdecimal";
   analyzer[] = "Extensions/Extdio";
   analyzer[] = "Extensions/Extdom";
   analyzer[] = "Extensions/Extds";
   analyzer[] = "Extensions/Exteaccelerator";
   analyzer[] = "Extensions/Exteio";
   analyzer[] = "Extensions/Extenchant";
   analyzer[] = "Extensions/Extev";
   analyzer[] = "Extensions/Extevent";
   analyzer[] = "Extensions/Extexcimer";
   analyzer[] = "Extensions/Extexif";
   analyzer[] = "Extensions/Extexpect";
   analyzer[] = "Extensions/Extfam";
   analyzer[] = "Extensions/Extfann";
   analyzer[] = "Extensions/Extffi";
   analyzer[] = "Extensions/Extfile";
   analyzer[] = "Extensions/Extfileinfo";
   analyzer[] = "Extensions/Extfilter";
   analyzer[] = "Extensions/Extfpm";
   analyzer[] = "Extensions/Extftp";
   analyzer[] = "Extensions/Extgd";
   analyzer[] = "Extensions/Extgearman";
   analyzer[] = "Extensions/Extgender";
   analyzer[] = "Extensions/Extgeoip";
   analyzer[] = "Extensions/Extgeospatial";
   analyzer[] = "Extensions/Extgettext";
   analyzer[] = "Extensions/Extgmagick";
   analyzer[] = "Extensions/Extgmp";
   analyzer[] = "Extensions/Extgnupg";
   analyzer[] = "Extensions/Extgrpc";
   analyzer[] = "Extensions/Exthash";
   analyzer[] = "Extensions/Exthrtime";
   analyzer[] = "Extensions/Exthttp";
   analyzer[] = "Extensions/Extibase";
   analyzer[] = "Extensions/Extice";
   analyzer[] = "Extensions/Exticonv";
   analyzer[] = "Extensions/Extigbinary";
   analyzer[] = "Extensions/Extimagick";
   analyzer[] = "Extensions/Extimap";
   analyzer[] = "Extensions/Extinfo";
   analyzer[] = "Extensions/Extinotify";
   analyzer[] = "Extensions/Extintl";
   analyzer[] = "Extensions/Extjson";
   analyzer[] = "Extensions/Extjudy";
   analyzer[] = "Extensions/Extldap";
   analyzer[] = "Extensions/Extleveldb";
   analyzer[] = "Extensions/Extlibsodium";
   analyzer[] = "Extensions/Extlibxml";
   analyzer[] = "Extensions/Extlua";
   analyzer[] = "Extensions/Extlzf";
   analyzer[] = "Extensions/Extmail";
   analyzer[] = "Extensions/Extmailparse";
   analyzer[] = "Extensions/Extmath";
   analyzer[] = "Extensions/Extmbstring";
   analyzer[] = "Extensions/Extmcrypt";
   analyzer[] = "Extensions/Extmemcache";
   analyzer[] = "Extensions/Extmemcached";
   analyzer[] = "Extensions/Extmongo";
   analyzer[] = "Extensions/Extmongodb";
   analyzer[] = "Extensions/Extmsgpack";
   analyzer[] = "Extensions/Extmssql";
   analyzer[] = "Extensions/Extmysql";
   analyzer[] = "Extensions/Extmysqli";
   analyzer[] = "Extensions/Extncurses";
   analyzer[] = "Extensions/Extnewt";
   analyzer[] = "Extensions/Extnsapi";
   analyzer[] = "Extensions/Extob";
   analyzer[] = "Extensions/Extoci8";
   analyzer[] = "Extensions/Extodbc";
   analyzer[] = "Extensions/Extopcache";
   analyzer[] = "Extensions/Extopencensus";
   analyzer[] = "Extensions/Extopenssl";
   analyzer[] = "Extensions/Extparle";
   analyzer[] = "Extensions/Extpassword";
   analyzer[] = "Extensions/Extpcntl";
   analyzer[] = "Extensions/Extpcov";
   analyzer[] = "Extensions/Extpcre";
   analyzer[] = "Extensions/Extpdo";
   analyzer[] = "Extensions/Extpgsql";
   analyzer[] = "Extensions/Extphalcon";
   analyzer[] = "Extensions/Extphar";
   analyzer[] = "Extensions/Extpkcs11";
   analyzer[] = "Extensions/Extposix";
   analyzer[] = "Extensions/Extprotobuf";
   analyzer[] = "Extensions/Extpspell";
   analyzer[] = "Extensions/Extpsr";
   analyzer[] = "Extensions/Extrandom";
   analyzer[] = "Extensions/Extrar";
   analyzer[] = "Extensions/Extrdkafka";
   analyzer[] = "Extensions/Extreadline";
   analyzer[] = "Extensions/Extredis";
   analyzer[] = "Extensions/Extreflection";
   analyzer[] = "Extensions/Extscrypt";
   analyzer[] = "Extensions/Extsdl";
   analyzer[] = "Extensions/Extseaslog";
   analyzer[] = "Extensions/Extsem";
   analyzer[] = "Extensions/Extsession";
   analyzer[] = "Extensions/Extshmop";
   analyzer[] = "Extensions/Extsimplexml";
   analyzer[] = "Extensions/Extsnmp";
   analyzer[] = "Extensions/Extsoap";
   analyzer[] = "Extensions/Extsockets";
   analyzer[] = "Extensions/Extsphinx";
   analyzer[] = "Extensions/Extspl";
   analyzer[] = "Extensions/Extspx";
   analyzer[] = "Extensions/Extsqlite";
   analyzer[] = "Extensions/Extsqlite3";
   analyzer[] = "Extensions/Extsqlsrv";
   analyzer[] = "Extensions/Extssh2";
   analyzer[] = "Extensions/Extstandard";
   analyzer[] = "Extensions/Extstats";
   analyzer[] = "Extensions/Extstomp";
   analyzer[] = "Extensions/Extstring";
   analyzer[] = "Extensions/Extsuhosin";
   analyzer[] = "Extensions/Extsvm";
   analyzer[] = "Extensions/Extswoole";
   analyzer[] = "Extensions/Exttaint";
   analyzer[] = "Extensions/Extteds";
   analyzer[] = "Extensions/Exttidy";
   analyzer[] = "Extensions/Exttokenizer";
   analyzer[] = "Extensions/Exttokyotyrant";
   analyzer[] = "Extensions/Exttrader";
   analyzer[] = "Extensions/Extuopz";
   analyzer[] = "Extensions/Extuuid";
   analyzer[] = "Extensions/Extv8js";
   analyzer[] = "Extensions/Extvarnish";
   analyzer[] = "Extensions/Extvips";
   analyzer[] = "Extensions/Extwasm";
   analyzer[] = "Extensions/Extwddx";
   analyzer[] = "Extensions/Extweakref";
   analyzer[] = "Extensions/Extxattr";
   analyzer[] = "Extensions/Extxdebug";
   analyzer[] = "Extensions/Extxdiff";
   analyzer[] = "Extensions/Extxhprof";
   analyzer[] = "Extensions/Extxml";
   analyzer[] = "Extensions/Extxmlreader";
   analyzer[] = "Extensions/Extxmlrpc";
   analyzer[] = "Extensions/Extxmlwriter";
   analyzer[] = "Extensions/Extxsl";
   analyzer[] = "Extensions/Extxxtea";
   analyzer[] = "Extensions/Extyaml";
   analyzer[] = "Extensions/Extyar";
   analyzer[] = "Extensions/Extzendmonitor";
   analyzer[] = "Extensions/Extzip";
   analyzer[] = "Extensions/Extzlib";
   analyzer[] = "Extensions/Extzmq";
   analyzer[] = "Extensions/Extzookeeper";
   analyzer[] = "Files/DefinitionsOnly";
   analyzer[] = "Files/GlobalCodeOnly";
   analyzer[] = "Files/IsCliScript";
   analyzer[] = "Files/IsComponent";
   analyzer[] = "Files/MissingInclude";
   analyzer[] = "Files/NotDefinitionsOnly";
   analyzer[] = "Files/Services";
   analyzer[] = "Functions/AddDefaultValue";
   analyzer[] = "Functions/AliasesUsage";
   analyzer[] = "Functions/AvoidBooleanArgument";
   analyzer[] = "Functions/BadTypehintRelay";
   analyzer[] = "Functions/CallbackNeedsReturn";
   analyzer[] = "Functions/CanCallGenerator";
   analyzer[] = "Functions/CancelledParameter";
   analyzer[] = "Functions/CannotUseStaticForClosure";
   analyzer[] = "Functions/CantUse";
   analyzer[] = "Functions/Closure2String";
   analyzer[] = "Functions/Closures";
   analyzer[] = "Functions/ConditionedFunctions";
   analyzer[] = "Functions/CouldBeCallable";
   analyzer[] = "Functions/CouldBeStaticClosure";
   analyzer[] = "Functions/CouldCentralize";
   analyzer[] = "Functions/CouldTypeWithArray";
   analyzer[] = "Functions/CouldTypeWithBool";
   analyzer[] = "Functions/CouldTypeWithInt";
   analyzer[] = "Functions/CouldTypeWithIterable";
   analyzer[] = "Functions/CouldTypeWithString";
   analyzer[] = "Functions/CouldTypehint";
   analyzer[] = "Functions/DeepDefinitions";
   analyzer[] = "Functions/DeprecatedCallable";
   analyzer[] = "Functions/DontUseVoid";
   analyzer[] = "Functions/DuplicateNamedParameter";
   analyzer[] = "Functions/DynamicCode";
   analyzer[] = "Functions/Dynamiccall";
   analyzer[] = "Functions/EmptyFunction";
   analyzer[] = "Functions/ExceedingTypehint";
   analyzer[] = "Functions/FallbackFunction";
   analyzer[] = "Functions/FnArgumentVariableConfusion";
   analyzer[] = "Functions/FunctionCalledWithOtherCase";
   analyzer[] = "Functions/Functionnames";
   analyzer[] = "Functions/FunctionsUsingReference";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/HardcodedPasswords";
   analyzer[] = "Functions/HasFluentInterface";
   analyzer[] = "Functions/HasNotFluentInterface";
   analyzer[] = "Functions/Identity";
   analyzer[] = "Functions/InsufficientTypehint";
   analyzer[] = "Functions/IsExtFunction";
   analyzer[] = "Functions/IsGenerator";
   analyzer[] = "Functions/IsGlobal";
   analyzer[] = "Functions/KillsApp";
   analyzer[] = "Functions/LoopCalling";
   analyzer[] = "Functions/MethodIsNotAnIf";
   analyzer[] = "Functions/MismatchParameterAndType";
   analyzer[] = "Functions/MismatchParameterName";
   analyzer[] = "Functions/MismatchTypeAndDefault";
   analyzer[] = "Functions/MismatchedDefaultArguments";
   analyzer[] = "Functions/MismatchedTypehint";
   analyzer[] = "Functions/MissingTypehint";
   analyzer[] = "Functions/ModifyTypedParameter";
   analyzer[] = "Functions/MultipleDeclarations";
   analyzer[] = "Functions/MultipleIdenticalClosure";
   analyzer[] = "Functions/MultipleReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/NeverUsedParameter";
   analyzer[] = "Functions/NoBooleanAsDefault";
   analyzer[] = "Functions/NoClassAsTypehint";
   analyzer[] = "Functions/NoDefaultForReference";
   analyzer[] = "Functions/NoLiteralForReference";
   analyzer[] = "Functions/NoReferencedVoid";
   analyzer[] = "Functions/NoReturnUsed";
   analyzer[] = "Functions/NullTypeFavorite";
   analyzer[] = "Functions/NullableWithoutCheck";
   analyzer[] = "Functions/OneLetterFunctions";
   analyzer[] = "Functions/OnlyVariableForReference";
   analyzer[] = "Functions/OnlyVariablePassedByReference";
   analyzer[] = "Functions/OptionalParameter";
   analyzer[] = "Functions/ParameterHiding";
   analyzer[] = "Functions/PrefixToType";
   analyzer[] = "Functions/RealFunctions";
   analyzer[] = "Functions/Recursive";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/RelayFunction";
   analyzer[] = "Functions/RemoveParameterWithNamedOnes";
   analyzer[] = "Functions/RetypedReference";
   analyzer[] = "Functions/SemanticTyping";
   analyzer[] = "Functions/ShouldBeTypehinted";
   analyzer[] = "Functions/ShouldUseConstants";
   analyzer[] = "Functions/ShouldYieldWithKey";
   analyzer[] = "Functions/TooManyLocalVariables";
   analyzer[] = "Functions/TooManyParameters";
   analyzer[] = "Functions/TooMuchIndented";
   analyzer[] = "Functions/TypeDodging";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/TypehintedReferences";
   analyzer[] = "Functions/Typehints";
   analyzer[] = "Functions/UnbindingClosures";
   analyzer[] = "Functions/UndefinedFunctions";
   analyzer[] = "Functions/UnknownParameterName";
   analyzer[] = "Functions/UnsetOnArguments";
   analyzer[] = "Functions/UnusedArguments";
   analyzer[] = "Functions/UnusedFunctions";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UnusedReturnedValue";
   analyzer[] = "Functions/UseArrowFunctions";
   analyzer[] = "Functions/UseConstantAsArguments";
   analyzer[] = "Functions/UseConstantsAsReturns";
   analyzer[] = "Functions/UsedFunctions";
   analyzer[] = "Functions/UselessArgument";
   analyzer[] = "Functions/UselessDefault";
   analyzer[] = "Functions/UselessReferenceArgument";
   analyzer[] = "Functions/UselessReturn";
   analyzer[] = "Functions/UselessTypeCheck";
   analyzer[] = "Functions/UsesDefaultArguments";
   analyzer[] = "Functions/UsingDeprecated";
   analyzer[] = "Functions/VariableArguments";
   analyzer[] = "Functions/VariableParameterAmbiguityInArrowFunction";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Functions/WithoutReturn";
   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
   analyzer[] = "Functions/WrongArgumentType";
   analyzer[] = "Functions/WrongCase";
   analyzer[] = "Functions/WrongNumberOfArguments";
   analyzer[] = "Functions/WrongNumberOfArgumentsMethods";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Functions/WrongTypehintedName";
   analyzer[] = "Functions/funcGetArgModified";
   analyzer[] = "Interfaces/AlreadyParentsInterface";
   analyzer[] = "Interfaces/AvoidSelfInInterface";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Interfaces/CouldUseInterface";
   analyzer[] = "Interfaces/EmptyInterface";
   analyzer[] = "Interfaces/InheritedClassConstantVisibility";
   analyzer[] = "Interfaces/InterfaceMethod";
   analyzer[] = "Interfaces/InterfaceUsage";
   analyzer[] = "Interfaces/Interfacenames";
   analyzer[] = "Interfaces/IsExtInterface";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/NoConstructorInInterface";
   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
   analyzer[] = "Interfaces/Php";
   analyzer[] = "Interfaces/PossibleInterfaces";
   analyzer[] = "Interfaces/RepeatedInterface";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Interfaces/UnusedInterfaces";
   analyzer[] = "Interfaces/UsedInterfaces";
   analyzer[] = "Interfaces/UselessInterfaces";
   analyzer[] = "Namespaces/Alias";
   analyzer[] = "Namespaces/AliasConfusion";
   analyzer[] = "Namespaces/ConstantFullyQualified";
   analyzer[] = "Namespaces/ConstantWithUseFavorite";
   analyzer[] = "Namespaces/CouldUseAlias";
   analyzer[] = "Namespaces/CouldUseMagicConstant";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/GlobalImport";
   analyzer[] = "Namespaces/HiddenUse";
   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
   analyzer[] = "Namespaces/MultipleAliasDefinitions";
   analyzer[] = "Namespaces/NamespaceUsage";
   analyzer[] = "Namespaces/Namespacesnames";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Namespaces/OverloadExistingNames";
   analyzer[] = "Namespaces/ShouldMakeAlias";
   analyzer[] = "Namespaces/UnresolvedUse";
   analyzer[] = "Namespaces/UnusedUse";
   analyzer[] = "Namespaces/UseFunctionsConstants";
   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
   analyzer[] = "Namespaces/UsedUse";
   analyzer[] = "Namespaces/WrongCase";
   analyzer[] = "Patterns/AbstractAway";
   analyzer[] = "Patterns/CourrierAntiPattern";
   analyzer[] = "Patterns/DependencyInjection";
   analyzer[] = "Patterns/Factory";
   analyzer[] = "Patterns/GetterSetter";
   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/Autoappend";
   analyzer[] = "Performances/AvoidArrayPush";
   analyzer[] = "Performances/CacheVariableOutsideLoop";
   analyzer[] = "Performances/ClassOperator";
   analyzer[] = "Performances/CountToAppend";
   analyzer[] = "Performances/CsvInLoops";
   analyzer[] = "Performances/DoInBase";
   analyzer[] = "Performances/DoubleArrayFlip";
   analyzer[] = "Performances/EllipsisMerge";
   analyzer[] = "Performances/FetchOneRowFormat";
   analyzer[] = "Performances/IssetWholeArray";
   analyzer[] = "Performances/JoinFile";
   analyzer[] = "Performances/LogicalToInArray";
   analyzer[] = "Performances/MakeOneCall";
   analyzer[] = "Performances/MbStringInLoop";
   analyzer[] = "Performances/MemoizeMagicCall";
   analyzer[] = "Performances/NoConcatInLoop";
   analyzer[] = "Performances/NoGlob";
   analyzer[] = "Performances/NotCountNull";
   analyzer[] = "Performances/OptimizeExplode";
   analyzer[] = "Performances/PHP7EncapsedStrings";
   analyzer[] = "Performances/Php74ArrayKeyExists";
   analyzer[] = "Performances/PreCalculateUse";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/RegexOnArrays";
   analyzer[] = "Performances/RegexOnCollector";
   analyzer[] = "Performances/ShouldCacheLocal";
   analyzer[] = "Performances/SimpleSwitch";
   analyzer[] = "Performances/SimplifyForeach";
   analyzer[] = "Performances/SkipEmptyArray";
   analyzer[] = "Performances/SlowFunctions";
   analyzer[] = "Performances/StaticCallDontNeedObjects";
   analyzer[] = "Performances/StaticCallWithSelf";
   analyzer[] = "Performances/StrposTooMuch";
   analyzer[] = "Performances/SubstrFirst";
   analyzer[] = "Performances/SubstrInLoops";
   analyzer[] = "Performances/TooManyExtractions";
   analyzer[] = "Performances/UseArraySlice";
   analyzer[] = "Performances/UseBlindVar";
   analyzer[] = "Performances/timeVsstrtotime";
   analyzer[] = "Php/AlternativeSyntax";
   analyzer[] = "Php/Argon2Usage";
   analyzer[] = "Php/ArrayKeyExistsWithObjects";
   analyzer[] = "Php/AssertFunctionIsReserved";
   analyzer[] = "Php/AssertionUsage";
   analyzer[] = "Php/AssignAnd";
   analyzer[] = "Php/Assumptions";
   analyzer[] = "Php/AutoloadUsage";
   analyzer[] = "Php/AvoidGetobjectVars";
   analyzer[] = "Php/AvoidMbDectectEncoding";
   analyzer[] = "Php/AvoidReal";
   analyzer[] = "Php/AvoidSetErrorHandlerContextArg";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/CallingStaticTraitMethod";
   analyzer[] = "Php/CantUseReturnValueInWriteContext";
   analyzer[] = "Php/CaseForPSS";
   analyzer[] = "Php/CastUnsetUsage";
   analyzer[] = "Php/CastingUsage";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClassConstWithArray";
   analyzer[] = "Php/ClassFunctionConfusion";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/CloseTags";
   analyzer[] = "Php/CloseTagsConsistency";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/ClosureThisSupport";
   analyzer[] = "Php/Coalesce";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/CompactInexistant";
   analyzer[] = "Php/ComparisonOnDifferentTypes";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/ConstWithArray";
   analyzer[] = "Php/CookiesVariables";
   analyzer[] = "Php/CouldUseIsCountable";
   analyzer[] = "Php/CouldUsePromotedProperties";
   analyzer[] = "Php/Crc32MightBeNegative";
   analyzer[] = "Php/CryptoUsage";
   analyzer[] = "Php/DateFormats";
   analyzer[] = "Php/DateTimeNotImmutable";
   analyzer[] = "Php/DeclareEncoding";
   analyzer[] = "Php/DeclareStrict";
   analyzer[] = "Php/DeclareStrictType";
   analyzer[] = "Php/DeclareTicks";
   analyzer[] = "Php/DefineWithArray";
   analyzer[] = "Php/DeprecateDollarCurly";
   analyzer[] = "Php/Deprecated";
   analyzer[] = "Php/DetectCurrentClass";
   analyzer[] = "Php/DirectCallToClone";
   analyzer[] = "Php/DirectiveName";
   analyzer[] = "Php/DirectivesUsage";
   analyzer[] = "Php/DlUsage";
   analyzer[] = "Php/DontPolluteGlobalSpace";
   analyzer[] = "Php/EchoTagUsage";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/EmptyList";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/ErrorLogUsage";
   analyzer[] = "Php/ExitNoArg";
   analyzer[] = "Php/ExponentUsage";
   analyzer[] = "Php/FailingAnalysis";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FilterToAddSlashes";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FirstClassCallable";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/FopenMode";
   analyzer[] = "Php/ForeachDontChangePointer";
   analyzer[] = "Php/ForeachObject";
   analyzer[] = "Php/GlobalWithoutSimpleVariable";
   analyzer[] = "Php/GlobalsVsGlobal";
   analyzer[] = "Php/Gotonames";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/Haltcompiler";
   analyzer[] = "Php/HasAsymmetricVisibility";
   analyzer[] = "Php/HasPropertyHook";
   analyzer[] = "Php/HasVirtualProperty";
   analyzer[] = "Php/HashAlgos";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/HashAlgos74";
   analyzer[] = "Php/HashUsesObjects";
   analyzer[] = "Php/IdnUts46";
   analyzer[] = "Php/ImplodeOneArg";
   analyzer[] = "Php/IncludeVariables";
   analyzer[] = "Php/IncomingValues";
   analyzer[] = "Php/IncomingVariables";
   analyzer[] = "Php/Incompilable";
   analyzer[] = "Php/IntegerSeparatorUsage";
   analyzer[] = "Php/InternalParameterType";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Php/IsINF";
   analyzer[] = "Php/IsNAN";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/IssetMultipleArgs";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/Labelnames";
   analyzer[] = "Php/LetterCharsLogicalFavorite";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithAppends";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/MethodCallOnNew";
   analyzer[] = "Php/MiddleVersion";
   analyzer[] = "Php/MissingMagicIsset";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Php/MixedKeyword";
   analyzer[] = "Php/MixedUsage";
   analyzer[] = "Php/MultipleDeclareStrict";
   analyzer[] = "Php/MustCallParentConstructor";
   analyzer[] = "Php/NamedArgumentAndVariadic";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NativeClassTypeCompatibility";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NeverKeyword";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewExponent";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoCastToInt";
   analyzer[] = "Php/NoClassInGlobal";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoMoreCurlyArrays";
   analyzer[] = "Php/NoNullForNative";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoReferenceForTernary";
   analyzer[] = "Php/NoReturnForGenerator";
   analyzer[] = "Php/NoStringWithAppend";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/NotScalarType";
   analyzer[] = "Php/OnlyVariablePassedByReference";
   analyzer[] = "Php/OpensslEncryptAlgoChange";
   analyzer[] = "Php/OveriddenFunction";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Password55";
   analyzer[] = "Php/PathinfoReturns";
   analyzer[] = "Php/PearUsage";
   analyzer[] = "Php/Php54NewFunctions";
   analyzer[] = "Php/Php54RemovedFunctions";
   analyzer[] = "Php/Php55NewFunctions";
   analyzer[] = "Php/Php55RemovedFunctions";
   analyzer[] = "Php/Php56NewFunctions";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php70RemovedDirective";
   analyzer[] = "Php/Php70RemovedFunctions";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php71NewFunctions";
   analyzer[] = "Php/Php71RemovedDirective";
   analyzer[] = "Php/Php71microseconds";
   analyzer[] = "Php/Php72Deprecation";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php72NewConstants";
   analyzer[] = "Php/Php72NewFunctions";
   analyzer[] = "Php/Php72ObjectKeyword";
   analyzer[] = "Php/Php72RemovedFunctions";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php73RemovedFunctions";
   analyzer[] = "Php/Php74Deprecation";
   analyzer[] = "Php/Php74NewClasses";
   analyzer[] = "Php/Php74NewConstants";
   analyzer[] = "Php/Php74NewDirective";
   analyzer[] = "Php/Php74NewFunctions";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php74RemovedFunctions";
   analyzer[] = "Php/Php74ReservedKeyword";
   analyzer[] = "Php/Php74mbstrrpos3rdArg";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php80NamedParameterVariadic";
   analyzer[] = "Php/Php80NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80RemovedConstant";
   analyzer[] = "Php/Php80RemovedDirective";
   analyzer[] = "Php/Php80RemovedFunctions";
   analyzer[] = "Php/Php80RemovesResources";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php80VariableSyntax";
   analyzer[] = "Php/Php81IntersectionTypehint";
   analyzer[] = "Php/Php81NewFunctions";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php81RemovedConstant";
   analyzer[] = "Php/Php81RemovedDirective";
   analyzer[] = "Php/Php81RemovedFunctions";
   analyzer[] = "Php/Php81RemovesResources";
   analyzer[] = "Php/Php82NewFunctions";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/Php83NewClasses";
   analyzer[] = "Php/Php83NewFunctions";
   analyzer[] = "Php/Php84NewFunctions";
   analyzer[] = "Php/PhpErrorMsgUsage";
   analyzer[] = "Php/PlusPlusOnLetters";
   analyzer[] = "Php/PregMatchAllFlag";
   analyzer[] = "Php/Prints";
   analyzer[] = "Php/RawPostDataUsage";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/ReflectionExportIsDeprecated";
   analyzer[] = "Php/ReservedKeywords7";
   analyzer[] = "Php/ReservedMatchKeyword";
   analyzer[] = "Php/ReservedMethods";
   analyzer[] = "Php/ReservedNames";
   analyzer[] = "Php/RestrictGlobalUsage";
   analyzer[] = "Php/ReturnTypehintUsage";
   analyzer[] = "Php/ReturnWithParenthesis";
   analyzer[] = "Php/SafePhpvars";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/ScalarTypehintUsage";
   analyzer[] = "Php/SerializeMagic";
   analyzer[] = "Php/SessionVariables";
   analyzer[] = "Php/SetExceptionHandlerPHP7";
   analyzer[] = "Php/SetHandlers";
   analyzer[] = "Php/ShellFavorite";
   analyzer[] = "Php/ShortOpenTagRequired";
   analyzer[] = "Php/ShortTernary";
   analyzer[] = "Php/ShouldPreprocess";
   analyzer[] = "Php/ShouldUseArrayColumn";
   analyzer[] = "Php/ShouldUseArrayFilter";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/ShouldUseFunction";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/SpreadOperatorForArray";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/StaticclassUsage";
   analyzer[] = "Php/StringIntComparison";
   analyzer[] = "Php/StrposWithIntegers";
   analyzer[] = "Php/StrtrArguments";
   analyzer[] = "Php/SuperGlobalUsage";
   analyzer[] = "Php/ThrowUsage";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/TooManyNativeCalls";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TriggerErrorUsage";
   analyzer[] = "Php/TriggerErrorUserError";
   analyzer[] = "Php/TryCatchUsage";
   analyzer[] = "Php/TryMultipleCatch";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnknownPcre2Option";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UnsetOrCast";
   analyzer[] = "Php/UpperCaseFunction";
   analyzer[] = "Php/UpperCaseKeyword";
   analyzer[] = "Php/UseAttributes";
   analyzer[] = "Php/UseBrowscap";
   analyzer[] = "Php/UseClassAlias";
   analyzer[] = "Php/UseCli";
   analyzer[] = "Php/UseContravariance";
   analyzer[] = "Php/UseCookies";
   analyzer[] = "Php/UseCovariance";
   analyzer[] = "Php/UseDNF";
   analyzer[] = "Php/UseDateTimeImmutable";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseGetDebugType";
   analyzer[] = "Php/UseMatch";
   analyzer[] = "Php/UseNullSafeOperator";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/UseObjectApi";
   analyzer[] = "Php/UsePathinfo";
   analyzer[] = "Php/UsePathinfoArgs";
   analyzer[] = "Php/UseSessionStartOptions";
   analyzer[] = "Php/UseSetCookie";
   analyzer[] = "Php/UseStdclass";
   analyzer[] = "Php/UseStrContains";
   analyzer[] = "Php/UseTrailingUseComma";
   analyzer[] = "Php/UseWeb";
   analyzer[] = "Php/UsesEnv";
   analyzer[] = "Php/UsortSorting";
   analyzer[] = "Php/Utf8EncodeDeprecated";
   analyzer[] = "Php/VersionCompareOperator";
   analyzer[] = "Php/WrongAttributeConfiguration";
   analyzer[] = "Php/WrongTypeForNativeFunction";
   analyzer[] = "Php/YieldFromUsage";
   analyzer[] = "Php/YieldUsage";
   analyzer[] = "Php/debugInfoUsage";
   analyzer[] = "Php/oldAutoloadUsage";
   analyzer[] = "Portability/FopenMode";
   analyzer[] = "Portability/GlobBraceUsage";
   analyzer[] = "Portability/IconvTranslit";
   analyzer[] = "Portability/LinuxOnlyFiles";
   analyzer[] = "Portability/WindowsOnlyConstants";
   analyzer[] = "Project/IsLibrary";
   analyzer[] = "Psr/Psr11Usage";
   analyzer[] = "Psr/Psr13Usage";
   analyzer[] = "Psr/Psr16Usage";
   analyzer[] = "Psr/Psr3Usage";
   analyzer[] = "Psr/Psr6Usage";
   analyzer[] = "Psr/Psr7Usage";
   analyzer[] = "Security/AnchorRegex";
   analyzer[] = "Security/AvoidThoseCrypto";
   analyzer[] = "Security/CantDisableClass";
   analyzer[] = "Security/CantDisableFunction";
   analyzer[] = "Security/CompareHash";
   analyzer[] = "Security/ConfigureExtract";
   analyzer[] = "Security/CryptoKeyLength";
   analyzer[] = "Security/CurlOptions";
   analyzer[] = "Security/DirectInjection";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/DynamicDl";
   analyzer[] = "Security/EncodedLetters";
   analyzer[] = "Security/FilterInputSource";
   analyzer[] = "Security/FilterNotRaw";
   analyzer[] = "Security/GPRAliases";
   analyzer[] = "Security/IncompatibleTypesWithIncoming";
   analyzer[] = "Security/IndirectInjection";
   analyzer[] = "Security/IntegerConversion";
   analyzer[] = "Security/KeepFilesRestricted";
   analyzer[] = "Security/MinusOneOnError";
   analyzer[] = "Security/MkdirDefault";
   analyzer[] = "Security/MoveUploadedFile";
   analyzer[] = "Security/NoEntIgnore";
   analyzer[] = "Security/NoNetForXmlLoad";
   analyzer[] = "Security/NoSleep";
   analyzer[] = "Security/NoWeakSSLCrypto";
   analyzer[] = "Security/RegisterGlobals";
   analyzer[] = "Security/SafeHttpHeaders";
   analyzer[] = "Security/SensitiveArgument";
   analyzer[] = "Security/SessionCachedData";
   analyzer[] = "Security/SessionLazyWrite";
   analyzer[] = "Security/SetCookieArgs";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Security/ShouldUseSessionRegenerateId";
   analyzer[] = "Security/Sqlite3RequiresSingleQuotes";
   analyzer[] = "Security/SuperGlobalContagion";
   analyzer[] = "Security/UnserializeSecondArg";
   analyzer[] = "Security/UploadFilenameInjection";
   analyzer[] = "Security/parseUrlWithoutParameters";
   analyzer[] = "Structures/AddZero";
   analyzer[] = "Structures/AlteringForeachWithoutReference";
   analyzer[] = "Structures/AlternativeConsistenceByFile";
   analyzer[] = "Structures/AlwaysFalse";
   analyzer[] = "Structures/ArrayAccessOnLiteralArray";
   analyzer[] = "Structures/ArrayAddition";
   analyzer[] = "Structures/ArrayCountTripleEqual";
   analyzer[] = "Structures/ArrayFillWithObjects";
   analyzer[] = "Structures/ArrayMapPassesByValue";
   analyzer[] = "Structures/ArrayMergeAndVariadic";
   analyzer[] = "Structures/ArrayMergeArrayArray";
   analyzer[] = "Structures/ArrayMergeWithEllipsis";
   analyzer[] = "Structures/ArraySearchMultipleKeys";
   analyzer[] = "Structures/AssigneAndCompare";
   analyzer[] = "Structures/AssignedInOneBranch";
   analyzer[] = "Structures/AutoUnsetForeach";
   analyzer[] = "Structures/BailOutEarly";
   analyzer[] = "Structures/BasenameSuffix";
   analyzer[] = "Structures/BlindVariableUsedBeyondLoop";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/Bracketless";
   analyzer[] = "Structures/Break0";
   analyzer[] = "Structures/BreakNonInteger";
   analyzer[] = "Structures/BreakOutsideLoop";
   analyzer[] = "Structures/BuriedAssignation";
   analyzer[] = "Structures/CalltimePassByReference";
   analyzer[] = "Structures/CanCountNonCountable";
   analyzer[] = "Structures/CannotUseAppendForReading";
   analyzer[] = "Structures/CastFavorite";
   analyzer[] = "Structures/CastToBoolean";
   analyzer[] = "Structures/CastingTernary";
   analyzer[] = "Structures/CatchShadowsVariable";
   analyzer[] = "Structures/CheckAllTypes";
   analyzer[] = "Structures/CheckDivision";
   analyzer[] = "Structures/CheckJson";
   analyzer[] = "Structures/CoalesceAndConcat";
   analyzer[] = "Structures/CoalesceNullCoalesce";
   analyzer[] = "Structures/CommonAlternatives";
   analyzer[] = "Structures/ComparedButNotAssignedStrings";
   analyzer[] = "Structures/ComparedComparison";
   analyzer[] = "Structures/ComparisonFavorite";
   analyzer[] = "Structures/ComplexExpression";
   analyzer[] = "Structures/ConcatEmpty";
   analyzer[] = "Structures/ConcatenationInterpolationFavorite";
   analyzer[] = "Structures/ConditionalStructures";
   analyzer[] = "Structures/ConstDefineFavorite";
   analyzer[] = "Structures/ConstantComparisonConsistance";
   analyzer[] = "Structures/ConstantConditions";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/CouldBeArrayCombine";
   analyzer[] = "Structures/CouldBeElse";
   analyzer[] = "Structures/CouldBeSpaceship";
   analyzer[] = "Structures/CouldBeStatic";
   analyzer[] = "Structures/CouldBeTernary";
   analyzer[] = "Structures/CouldCastToArray";
   analyzer[] = "Structures/CouldUseArrayFillKeys";
   analyzer[] = "Structures/CouldUseArraySum";
   analyzer[] = "Structures/CouldUseArrayUnique";
   analyzer[] = "Structures/CouldUseCompact";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseMatch";
   analyzer[] = "Structures/CouldUseNullableOperator";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrContains";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/CouldUseYieldFrom";
   analyzer[] = "Structures/CountIsNotNegative";
   analyzer[] = "Structures/CryptWithoutSalt";
   analyzer[] = "Structures/CurlVersionNow";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/DateTimePreference";
   analyzer[] = "Structures/DeclareStaticOnce";
   analyzer[] = "Structures/DefaultThenDiscard";
   analyzer[] = "Structures/DeprecatedMbEncoding";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/DieExitConsistance";
   analyzer[] = "Structures/DifferencePreference";
   analyzer[] = "Structures/DirThenSlash";
   analyzer[] = "Structures/DirectlyUseFile";
   analyzer[] = "Structures/DontAddSeconds";
   analyzer[] = "Structures/DontBeTooManual";
   analyzer[] = "Structures/DontChangeBlindKey";
   analyzer[] = "Structures/DontCompareTypedBoolean";
   analyzer[] = "Structures/DontLoopOnYield";
   analyzer[] = "Structures/DontMixPlusPlus";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Structures/DontReuseForeachSource";
   analyzer[] = "Structures/DontUseTheTypeAsVariable";
   analyzer[] = "Structures/DoubleAssignation";
   analyzer[] = "Structures/DoubleChecks";
   analyzer[] = "Structures/DoubleInstruction";
   analyzer[] = "Structures/DoubleObjectAssignation";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/DuplicateCalls";
   analyzer[] = "Structures/DynamicCalls";
   analyzer[] = "Structures/DynamicCode";
   analyzer[] = "Structures/EchoPrintConsistance";
   analyzer[] = "Structures/EchoWithConcat";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/ElseUsage";
   analyzer[] = "Structures/EmptyBlocks";
   analyzer[] = "Structures/EmptyJsonError";
   analyzer[] = "Structures/EmptyLines";
   analyzer[] = "Structures/EmptyLoop";
   analyzer[] = "Structures/EmptyTryCatch";
   analyzer[] = "Structures/EmptyWithExpression";
   analyzer[] = "Structures/ErrorMessages";
   analyzer[] = "Structures/ErrorReportingWithInteger";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/Fallthrough";
   analyzer[] = "Structures/FilePutContentsDataType";
   analyzer[] = "Structures/FileUploadUsage";
   analyzer[] = "Structures/FileUsage";
   analyzer[] = "Structures/ForWithFunctioncall";
   analyzer[] = "Structures/ForeachNeedReferencedSource";
   analyzer[] = "Structures/ForeachOnObject";
   analyzer[] = "Structures/ForeachReferenceIsNotModified";
   analyzer[] = "Structures/ForeachSourceValue";
   analyzer[] = "Structures/ForeachWithList";
   analyzer[] = "Structures/ForgottenWhiteSpace";
   analyzer[] = "Structures/FunctionPreSubscripting";
   analyzer[] = "Structures/FunctionSubscripting";
   analyzer[] = "Structures/GetClassWithoutArg";
   analyzer[] = "Structures/GlobalInGlobal";
   analyzer[] = "Structures/GlobalOutsideLoop";
   analyzer[] = "Structures/GlobalUsage";
   analyzer[] = "Structures/GoToKeyDirectly";
   analyzer[] = "Structures/GtOrLtFavorite";
   analyzer[] = "Structures/HeredocDelimiterFavorite";
   analyzer[] = "Structures/Htmlentitiescall";
   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
   analyzer[] = "Structures/IdenticalCase";
   analyzer[] = "Structures/IdenticalConditions";
   analyzer[] = "Structures/IdenticalConsecutive";
   analyzer[] = "Structures/IdenticalElseif";
   analyzer[] = "Structures/IdenticalOnBothSides";
   analyzer[] = "Structures/IdenticalVariablesInForeach";
   analyzer[] = "Structures/IfThenReturnFavorite";
   analyzer[] = "Structures/IfWithSameConditions";
   analyzer[] = "Structures/Iffectation";
   analyzer[] = "Structures/ImplicitConversionToInt";
   analyzer[] = "Structures/ImplicitGlobal";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/ImplodeArgsOrder";
   analyzer[] = "Structures/IncludeUsage";
   analyzer[] = "Structures/InconsistentConcatenation";
   analyzer[] = "Structures/InconsistentElseif";
   analyzer[] = "Structures/IndicesAreIntOrString";
   analyzer[] = "Structures/InfiniteRecursion";
   analyzer[] = "Structures/InitThenIf";
   analyzer[] = "Structures/InvalidCast";
   analyzer[] = "Structures/InvalidDateScanningFormat";
   analyzer[] = "Structures/InvalidPackFormat";
   analyzer[] = "Structures/InvalidRegex";
   analyzer[] = "Structures/IsAVersusInstanceof";
   analyzer[] = "Structures/IsZero";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/JsonEncodeExceptions";
   analyzer[] = "Structures/JsonWithOption";
   analyzer[] = "Structures/ListOmissions";
   analyzer[] = "Structures/LogicalMistakes";
   analyzer[] = "Structures/LoneBlock";
   analyzer[] = "Structures/LongArguments";
   analyzer[] = "Structures/LongBlock";
   analyzer[] = "Structures/MailUsage";
   analyzer[] = "Structures/MaxLevelOfIdentation";
   analyzer[] = "Structures/MbStringNonEncodings";
   analyzer[] = "Structures/MbstringThirdArg";
   analyzer[] = "Structures/MbstringUnknownEncoding";
   analyzer[] = "Structures/McryptcreateivWithoutOption";
   analyzer[] = "Structures/MergeIfThen";
   analyzer[] = "Structures/MergeTernaryIntoIfthen";
   analyzer[] = "Structures/MismatchedTernary";
   analyzer[] = "Structures/MissingAssignation";
   analyzer[] = "Structures/MissingCases";
   analyzer[] = "Structures/MissingNew";
   analyzer[] = "Structures/MissingParenthesis";
   analyzer[] = "Structures/MisusedYield";
   analyzer[] = "Structures/MixedConcatInterpolation";
   analyzer[] = "Structures/ModernEmpty";
   analyzer[] = "Structures/MultilineExpressions";
   analyzer[] = "Structures/MultipleCatch";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultipleSimilarCalls";
   analyzer[] = "Structures/MultipleTypeCasesInSwitch";
   analyzer[] = "Structures/MultipleTypeVariable";
   analyzer[] = "Structures/MultipleUnset";
   analyzer[] = "Structures/MultiplyByOne";
   analyzer[] = "Structures/NamedRegex";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NegativePow";
   analyzer[] = "Structures/NestedIfthen";
   analyzer[] = "Structures/NestedLoops";
   analyzer[] = "Structures/NestedMatch";
   analyzer[] = "Structures/NestedTernary";
   analyzer[] = "Structures/NeverNegative";
   analyzer[] = "Structures/NewLineStyle";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoAppendOnSource";
   analyzer[] = "Structures/NoArrayUnique";
   analyzer[] = "Structures/NoAssignationInFunction";
   analyzer[] = "Structures/NoChangeIncomingVariables";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoDirectAccess";
   analyzer[] = "Structures/NoDirectUsage";
   analyzer[] = "Structures/NoEmptyRegex";
   analyzer[] = "Structures/NoEmptyStringWithExplode";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/NoHardcodedHash";
   analyzer[] = "Structures/NoHardcodedIp";
   analyzer[] = "Structures/NoHardcodedPath";
   analyzer[] = "Structures/NoHardcodedPort";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/NoMaxOnEmptyArray";
   analyzer[] = "Structures/NoNeedForElse";
   analyzer[] = "Structures/NoNeedForTriple";
   analyzer[] = "Structures/NoNeedGetClass";
   analyzer[] = "Structures/NoNullForIndex";
   analyzer[] = "Structures/NoObjectAsIndex";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoReferenceOnLeft";
   analyzer[] = "Structures/NoReturnInFinally";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/NoValidCast";
   analyzer[] = "Structures/NoVariableIsACondition";
   analyzer[] = "Structures/NonBreakableSpaceInNames";
   analyzer[] = "Structures/NonIntStringAsIndex";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/NotEqual";
   analyzer[] = "Structures/NotNot";
   analyzer[] = "Structures/NotOrNot";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/OnceUsage";
   analyzer[] = "Structures/OneDotOrObjectOperatorPerLine";
   analyzer[] = "Structures/OneExpressionBracketsConsistency";
   analyzer[] = "Structures/OneIfIsSufficient";
   analyzer[] = "Structures/OneLevelOfIndentation";
   analyzer[] = "Structures/OneLineTwoInstructions";
   analyzer[] = "Structures/OnlyFirstByte";
   analyzer[] = "Structures/OnlyVariableReturnedByReference";
   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";
   analyzer[] = "Structures/OrDie";
   analyzer[] = "Structures/OverwrittenForeachVar";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/PhpinfoUsage";
   analyzer[] = "Structures/PlusEgalOne";
   analyzer[] = "Structures/PossibleIncrement";
   analyzer[] = "Structures/PossibleInfiniteLoop";
   analyzer[] = "Structures/PrintAndDie";
   analyzer[] = "Structures/PrintWithoutParenthesis";
   analyzer[] = "Structures/PrintfArguments";
   analyzer[] = "Structures/PropertyVariableConfusion";
   analyzer[] = "Structures/QueriesInLoop";
   analyzer[] = "Structures/RandomWithoutTry";
   analyzer[] = "Structures/RecalledCondition";
   analyzer[] = "Structures/RegexDelimiter";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/RepeatedRegex";
   analyzer[] = "Structures/ResourcesUsage";
   analyzer[] = "Structures/ResultMayBeMissing";
   analyzer[] = "Structures/ReturnTrueFalse";
   analyzer[] = "Structures/ReturnVoid";
   analyzer[] = "Structures/ReuseVariable";
   analyzer[] = "Structures/SGVariablesConfusion";
   analyzer[] = "Structures/SameConditions";
   analyzer[] = "Structures/SequenceInFor";
   analyzer[] = "Structures/SetAside";
   analyzer[] = "Structures/SetlocaleNeedsConstants";
   analyzer[] = "Structures/ShellUsage";
   analyzer[] = "Structures/ShortOrCompleteComparison";
   analyzer[] = "Structures/ShortTags";
   analyzer[] = "Structures/ShouldChainException";
   analyzer[] = "Structures/ShouldMakeTernary";
   analyzer[] = "Structures/ShouldPreprocess";
   analyzer[] = "Structures/ShouldUseExplodeArgs";
   analyzer[] = "Structures/ShouldUseForeach";
   analyzer[] = "Structures/ShouldUseMath";
   analyzer[] = "Structures/ShouldUseOperator";
   analyzer[] = "Structures/SimplePreg";
   analyzer[] = "Structures/SprintfFormatCompilation";
   analyzer[] = "Structures/StaticInclude";
   analyzer[] = "Structures/StaticLoop";
   analyzer[] = "Structures/StrictInArrayFavorite";
   analyzer[] = "Structures/StringInterpolationFavorite";
   analyzer[] = "Structures/StripTagsSkipsClosedTag";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/StrposLessThanOne";
   analyzer[] = "Structures/SubstrLastArg";
   analyzer[] = "Structures/SubstrToTrim";
   analyzer[] = "Structures/SuspiciousComparison";
   analyzer[] = "Structures/SwitchToSwitch";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/SwitchWithoutDefault";
   analyzer[] = "Structures/TernaryInConcat";
   analyzer[] = "Structures/TestThenCast";
   analyzer[] = "Structures/ThrowsAndAssign";
   analyzer[] = "Structures/TimestampDifference";
   analyzer[] = "Structures/TooManyChainedCalls";
   analyzer[] = "Structures/TooManyElseif";
   analyzer[] = "Structures/TryFinally";
   analyzer[] = "Structures/UncheckedResources";
   analyzer[] = "Structures/UnconditionLoopBreak";
   analyzer[] = "Structures/UnknownPregOption";
   analyzer[] = "Structures/Unpreprocessed";
   analyzer[] = "Structures/UnreachableCode";
   analyzer[] = "Structures/UnsetInForeach";
   analyzer[] = "Structures/UnsupportedOperandTypes";
   analyzer[] = "Structures/UnsupportedTypesWithOperators";
   analyzer[] = "Structures/UnusedGlobal";
   analyzer[] = "Structures/UnusedLabel";
   analyzer[] = "Structures/UseArrayFunctions";
   analyzer[] = "Structures/UseCaseValue";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UseCountRecursive";
   analyzer[] = "Structures/UseDebug";
   analyzer[] = "Structures/UseFileAppend";
   analyzer[] = "Structures/UseInstanceof";
   analyzer[] = "Structures/UseListWithForeach";
   analyzer[] = "Structures/UsePositiveCondition";
   analyzer[] = "Structures/UseSameTypesForComparisons";
   analyzer[] = "Structures/UseStrEndsWith";
   analyzer[] = "Structures/UseStrStartsWith";
   analyzer[] = "Structures/UseSystemTmp";
   analyzer[] = "Structures/UseUrlQueryFunctions";
   analyzer[] = "Structures/UseVariableInsideLoop";
   analyzer[] = "Structures/UselessBrackets";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Structures/UselessCheck";
   analyzer[] = "Structures/UselessCoalesce";
   analyzer[] = "Structures/UselessGlobal";
   analyzer[] = "Structures/UselessInstruction";
   analyzer[] = "Structures/UselessNullCoalesce";
   analyzer[] = "Structures/UselessParenthesis";
   analyzer[] = "Structures/UselessShortTernary";
   analyzer[] = "Structures/UselessSwitch";
   analyzer[] = "Structures/UselessTrailingComma";
   analyzer[] = "Structures/UselessUnset";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Structures/VariableMayBeNonGlobal";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Structures/WrongLocale";
   analyzer[] = "Structures/WrongPrecedenceInExpression";
   analyzer[] = "Structures/WrongRange";
   analyzer[] = "Structures/YodaComparison";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Structures/strOrMbFavorite";
   analyzer[] = "Structures/toStringThrowsException";
   analyzer[] = "Traits/AlreadyParentsTrait";
   analyzer[] = "Traits/CannotCallTraitMethod";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/CouldUseTrait";
   analyzer[] = "Traits/DependantTrait";
   analyzer[] = "Traits/EmptyTrait";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/IncompatibleProperty";
   analyzer[] = "Traits/IsExtTrait";
   analyzer[] = "Traits/LocallyUsedProperty";
   analyzer[] = "Traits/MethodCollisionTraits";
   analyzer[] = "Traits/MultipleUsage";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Traits/Php";
   analyzer[] = "Traits/SelfUsingTrait";
   analyzer[] = "Traits/SidelinedMethod";
   analyzer[] = "Traits/TraitIsNotAType";
   analyzer[] = "Traits/TraitMethod";
   analyzer[] = "Traits/TraitNotFound";
   analyzer[] = "Traits/TraitUsage";
   analyzer[] = "Traits/Traitnames";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UnusedClassTrait";
   analyzer[] = "Traits/UnusedTrait";
   analyzer[] = "Traits/UsedOnceTrait";
   analyzer[] = "Traits/UsedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Type/ArrayIndex";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/CharString";
   analyzer[] = "Type/Continents";
   analyzer[] = "Type/DuplicateLiteral";
   analyzer[] = "Type/Email";
   analyzer[] = "Type/GPCIndex";
   analyzer[] = "Type/Heredoc";
   analyzer[] = "Type/Hexadecimal";
   analyzer[] = "Type/HexadecimalString";
   analyzer[] = "Type/HttpHeader";
   analyzer[] = "Type/HttpStatus";
   analyzer[] = "Type/IncomingDateFormat";
   analyzer[] = "Type/Ip";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Type/Md5String";
   analyzer[] = "Type/MimeType";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Type/Nowdoc";
   analyzer[] = "Type/Octal";
   analyzer[] = "Type/OctalInString";
   analyzer[] = "Type/OneVariableStrings";
   analyzer[] = "Type/OpensslCipher";
   analyzer[] = "Type/Pack";
   analyzer[] = "Type/Path";
   analyzer[] = "Type/Pcre";
   analyzer[] = "Type/Ports";
   analyzer[] = "Type/Printf";
   analyzer[] = "Type/Protocols";
   analyzer[] = "Type/Regex";
   analyzer[] = "Type/Sapi";
   analyzer[] = "Type/Shellcommands";
   analyzer[] = "Type/ShouldBeSingleQuote";
   analyzer[] = "Type/ShouldTypecast";
   analyzer[] = "Type/SilentlyCastInteger";
   analyzer[] = "Type/SimilarIntegers";
   analyzer[] = "Type/SpecialIntegers";
   analyzer[] = "Type/Sql";
   analyzer[] = "Type/StringHoldAVariable";
   analyzer[] = "Type/StringInterpolation";
   analyzer[] = "Type/StringWithStrangeSpace";
   analyzer[] = "Type/UdpDomains";
   analyzer[] = "Type/UnicodeBlock";
   analyzer[] = "Type/Url";
   analyzer[] = "Typehints/CouldBeArray";
   analyzer[] = "Typehints/CouldBeBoolean";
   analyzer[] = "Typehints/CouldBeCIT";
   analyzer[] = "Typehints/CouldBeCallable";
   analyzer[] = "Typehints/CouldBeFloat";
   analyzer[] = "Typehints/CouldBeGenerator";
   analyzer[] = "Typehints/CouldBeInt";
   analyzer[] = "Typehints/CouldBeIterable";
   analyzer[] = "Typehints/CouldBeNever";
   analyzer[] = "Typehints/CouldBeNull";
   analyzer[] = "Typehints/CouldBeParent";
   analyzer[] = "Typehints/CouldBeResource";
   analyzer[] = "Typehints/CouldBeSelf";
   analyzer[] = "Typehints/CouldBeString";
   analyzer[] = "Typehints/CouldBeVoid";
   analyzer[] = "Typehints/CouldNotType";
   analyzer[] = "Typehints/MissingReturntype";
   analyzer[] = "Typehints/MissingTypehints";
   analyzer[] = "Typehints/StandaloneTypeTFN";
   analyzer[] = "Typehints/WrongTypeWithDefault";
   analyzer[] = "Utils/Selector";
   analyzer[] = "Variables/AmbiguousTypes";
   analyzer[] = "Variables/AssignedTwiceOrMore";
   analyzer[] = "Variables/Blind";
   analyzer[] = "Variables/CloseNaming";
   analyzer[] = "Variables/ComplexDynamicNames";
   analyzer[] = "Variables/ConstantTypo";
   analyzer[] = "Variables/Globals";
   analyzer[] = "Variables/InconsistentUsage";
   analyzer[] = "Variables/InheritedStaticVariable";
   analyzer[] = "Variables/InterfaceArguments";
   analyzer[] = "Variables/IsLocalConstant";
   analyzer[] = "Variables/LocalGlobals";
   analyzer[] = "Variables/LostReferences";
   analyzer[] = "Variables/NoInitialS";
   analyzer[] = "Variables/NoStaticVarInMethod";
   analyzer[] = "Variables/NoVariableNeeded";
   analyzer[] = "Variables/Overwriting";
   analyzer[] = "Variables/OverwrittenLiterals";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RealVariables";
   analyzer[] = "Variables/RecycledVariables";
   analyzer[] = "Variables/RedeclaredStaticVariable";
   analyzer[] = "Variables/References";
   analyzer[] = "Variables/SelfTransform";
   analyzer[] = "Variables/StaticVariableInNamespace";
   analyzer[] = "Variables/StaticVariableInitialisation";
   analyzer[] = "Variables/StaticVariables";
   analyzer[] = "Variables/StrangeName";
   analyzer[] = "Variables/UncommonEnvVar";
   analyzer[] = "Variables/UndefinedConstantName";
   analyzer[] = "Variables/UndefinedVariable";
   analyzer[] = "Variables/UniqueUsage";
   analyzer[] = "Variables/VariableLong";
   analyzer[] = "Variables/VariableNonascii";
   analyzer[] = "Variables/VariableOneLetter";
   analyzer[] = "Variables/VariablePhp";
   analyzer[] = "Variables/VariableUppercase";
   analyzer[] = "Variables/VariableUsedOnce";
   analyzer[] = "Variables/VariableUsedOnceByContext";
   analyzer[] = "Variables/VariableVariables";
   analyzer[] = "Variables/WrittenOnlyVariable";
   analyzer[] = "Vendors/Cakephp";
   analyzer[] = "Vendors/Codeigniter";
   analyzer[] = "Vendors/Concrete5";
   analyzer[] = "Vendors/Drupal";
   analyzer[] = "Vendors/Feast";
   analyzer[] = "Vendors/Fuel";
   analyzer[] = "Vendors/Joomla";
   analyzer[] = "Vendors/Laravel";
   analyzer[] = "Vendors/Neos";
   analyzer[] = "Vendors/Phalcon";
   analyzer[] = "Vendors/Sylius";
   analyzer[] = "Vendors/Symfony";
   analyzer[] = "Vendors/Typo3";
   analyzer[] = "Vendors/Wordpress";
   analyzer[] = "Vendors/Yii";


.. _annex-yaml-all:

All for .exakat.yaml
++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'All':
     - 'Arrays/AmbiguousKeys'
     - 'Arrays/AppendAndAssignArrays'
     - 'Arrays/ArrayBracketConsistence'
     - 'Arrays/ArrayNSUsage'
     - 'Arrays/Arrayindex'
     - 'Arrays/EmptyFinal'
     - 'Arrays/EmptySlots'
     - 'Arrays/FloatConversionAsIndex'
     - 'Arrays/GettingLastElement'
     - 'Arrays/MassCreation'
     - 'Arrays/MistakenConcatenation'
     - 'Arrays/MixedKeys'
     - 'Arrays/Multidimensional'
     - 'Arrays/MultipleIdenticalKeys'
     - 'Arrays/NegativeStart'
     - 'Arrays/NoSpreadForHash'
     - 'Arrays/NonConstantArray'
     - 'Arrays/NullBoolean'
     - 'Arrays/Phparrayindex'
     - 'Arrays/RandomlySortedLiterals'
     - 'Arrays/ShouldPreprocess'
     - 'Arrays/SliceFirst'
     - 'Arrays/StringInitialization'
     - 'Arrays/TooManyDimensions'
     - 'Arrays/WeakType'
     - 'Arrays/WeirdIndex'
     - 'Arrays/WithCallback'
     - 'Attributes/Deprecated'
     - 'Attributes/Friend'
     - 'Attributes/InjectableVersion'
     - 'Attributes/MissingAttributeAttribute'
     - 'Attributes/MissingOverrideMethod'
     - 'Attributes/ModifyImmutable'
     - 'Attributes/MustUseResult'
     - 'Attributes/MustUseReturnReturns'
     - 'Attributes/NestedAttributes'
     - 'Attributes/NoNamedArguments'
     - 'Attributes/Override'
     - 'Attributes/PhpNativeAttributes'
     - 'Attributes/UselessOverride'
     - 'Attributes/UsingDeprecated'
     - 'Classes/AbstractConstants'
     - 'Classes/AbstractOrImplements'
     - 'Classes/AbstractStatic'
     - 'Classes/Abstractclass'
     - 'Classes/Abstractmethods'
     - 'Classes/AccessPrivate'
     - 'Classes/AccessProtected'
     - 'Classes/AmbiguousStatic'
     - 'Classes/AmbiguousVisibilities'
     - 'Classes/Anonymous'
     - 'Classes/AvoidOptionArrays'
     - 'Classes/AvoidOptionalProperties'
     - 'Classes/AvoidUsing'
     - 'Classes/CancelCommonMethod'
     - 'Classes/CannotBeReadonly'
     - 'Classes/CantExtendFinal'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/CantInstantiateClass'
     - 'Classes/CantInstantiateNonClass'
     - 'Classes/CantOverwriteFinalConstant'
     - 'Classes/CantOverwriteFinalMethod'
     - 'Classes/CheckAfterNullSafeOperator'
     - 'Classes/CheckOnCallUsage'
     - 'Classes/ChecksPropertyExistence'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/CitSameName'
     - 'Classes/ClassAliasUsage'
     - 'Classes/ClassInvasion'
     - 'Classes/ClassOverreach'
     - 'Classes/ClassUsage'
     - 'Classes/Classnames'
     - 'Classes/CloneWithNonObject'
     - 'Classes/CloningUsage'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/ConstantClass'
     - 'Classes/ConstantDefinition'
     - 'Classes/ConstantUsedBelow'
     - 'Classes/Constructor'
     - 'Classes/CouldBeAbstractClass'
     - 'Classes/CouldBeAbstractMethod'
     - 'Classes/CouldBeClassConstant'
     - 'Classes/CouldBeFinal'
     - 'Classes/CouldBeIterable'
     - 'Classes/CouldBeParentMethod'
     - 'Classes/CouldBePrivate'
     - 'Classes/CouldBePrivateConstante'
     - 'Classes/CouldBePrivateMethod'
     - 'Classes/CouldBeProtectedConstant'
     - 'Classes/CouldBeProtectedMethod'
     - 'Classes/CouldBeProtectedProperty'
     - 'Classes/CouldBeReadonly'
     - 'Classes/CouldBeReadonlyProperty'
     - 'Classes/CouldBeStatic'
     - 'Classes/CouldBeStringable'
     - 'Classes/CouldInjectParam'
     - 'Classes/CouldSetPropertyDefault'
     - 'Classes/CouldUseClassOperator'
     - 'Classes/CyclicReferences'
     - 'Classes/DefinedConstants'
     - 'Classes/DefinedParentMP'
     - 'Classes/DefinedProperty'
     - 'Classes/DefinedStaticMP'
     - 'Classes/DemeterLaw'
     - 'Classes/DependantAbstractClass'
     - 'Classes/DifferentArgumentCounts'
     - 'Classes/DirectCallToMagicMethod'
     - 'Classes/DisconnectedClasses'
     - 'Classes/DontSendThisInConstructor'
     - 'Classes/DontUnsetProperties'
     - 'Classes/DynamicClass'
     - 'Classes/DynamicConstantCall'
     - 'Classes/DynamicMethodCall'
     - 'Classes/DynamicNew'
     - 'Classes/DynamicPropertyCall'
     - 'Classes/DynamicSelfCalls'
     - 'Classes/EmptyClass'
     - 'Classes/ExportProperty'
     - 'Classes/ExtendsStdclass'
     - 'Classes/FinalByOcramius'
     - 'Classes/FinalPrivate'
     - 'Classes/Finalclass'
     - 'Classes/Finalmethod'
     - 'Classes/FossilizedMethod'
     - 'Classes/HasFluentInterface'
     - 'Classes/HasMagicProperty'
     - 'Classes/HiddenNullable'
     - 'Classes/IdenticalMethods'
     - 'Classes/ImmutableSignature'
     - 'Classes/ImplementIsForInterface'
     - 'Classes/ImplementedMethodsArePublic'
     - 'Classes/IncompatibleConstructor'
     - 'Classes/IncompatibleSignature'
     - 'Classes/IncompatibleSignature74'
     - 'Classes/InheritedPropertyMustMatch'
     - 'Classes/InstantiatingAbstractClass'
     - 'Classes/InsufficientPropertyTypehint'
     - 'Classes/IntegerAsProperty'
     - 'Classes/IsExtClass'
     - 'Classes/IsInterfaceMethod'
     - 'Classes/IsNotFamily'
     - 'Classes/IsUpperFamily'
     - 'Classes/IsaMagicProperty'
     - 'Classes/LocallyUnusedProperty'
     - 'Classes/LocallyUsedProperty'
     - 'Classes/LoweredAccessLevel'
     - 'Classes/MagicMethod'
     - 'Classes/MagicMethodReturntypes'
     - 'Classes/MagicProperties'
     - 'Classes/MakeDefault'
     - 'Classes/MakeGlobalAProperty'
     - 'Classes/MakeMagicConcrete'
     - 'Classes/MethodIsOverwritten'
     - 'Classes/MethodPropertyConfusion'
     - 'Classes/MethodSignatureMustBeCompatible'
     - 'Classes/MethodUsedBelow'
     - 'Classes/MismatchProperties'
     - 'Classes/MissingAbstractMethod'
     - 'Classes/MissingVisibility'
     - 'Classes/MultipleClassesInFile'
     - 'Classes/MultipleDeclarations'
     - 'Classes/MultiplePropertyDeclaration'
     - 'Classes/MultiplePropertyDeclarationOnOneLine'
     - 'Classes/MultipleTraitOrInterface'
     - 'Classes/MutualExtension'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NewOnFunctioncallOrIdentifier'
     - 'Classes/NewThenCall'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoNullWithNullSafeOperator'
     - 'Classes/NoPSSOutsideClass'
     - 'Classes/NoParent'
     - 'Classes/NoPublicAccess'
     - 'Classes/NoReadonlyAssignationInGlobal'
     - 'Classes/NoSelfReferencingConstant'
     - 'Classes/NonNullableSetters'
     - 'Classes/NonPpp'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NormalMethods'
     - 'Classes/NullOnNew'
     - 'Classes/OldStyleConstructor'
     - 'Classes/OldStyleVar'
     - 'Classes/OneObjectOperatorPerLine'
     - 'Classes/OnlyStaticMethods'
     - 'Classes/OrderOfDeclaration'
     - 'Classes/OverwrittenConst'
     - 'Classes/PPPDeclarationStyle'
     - 'Classes/ParentFirst'
     - 'Classes/ParentIsNotStatic'
     - 'Classes/PromotedProperties'
     - 'Classes/PropertyCouldBeLocal'
     - 'Classes/PropertyDefinition'
     - 'Classes/PropertyInvasion'
     - 'Classes/PropertyMethodSameName'
     - 'Classes/PropertyNeverUsed'
     - 'Classes/PropertyUsedAbove'
     - 'Classes/PropertyUsedBelow'
     - 'Classes/PropertyUsedInOneMethodOnly'
     - 'Classes/PropertyUsedInternally'
     - 'Classes/PssWithoutClass'
     - 'Classes/RaisedAccessLevel'
     - 'Classes/ReadonlyUsage'
     - 'Classes/RedefinedConstants'
     - 'Classes/RedefinedDefault'
     - 'Classes/RedefinedMethods'
     - 'Classes/RedefinedPrivateProperty'
     - 'Classes/RedefinedProperty'
     - 'Classes/RewroteFinalClassConstant'
     - 'Classes/SameNameAsFile'
     - 'Classes/ScalarOrObjectProperty'
     - 'Classes/ShouldDeepClone'
     - 'Classes/ShouldHaveDestructor'
     - 'Classes/ShouldUseSelf'
     - 'Classes/ShouldUseThis'
     - 'Classes/StaticCannotCallNonStatic'
     - 'Classes/StaticContainsThis'
     - 'Classes/StaticMethods'
     - 'Classes/StaticMethodsCalledFromObject'
     - 'Classes/StaticProperties'
     - 'Classes/StrangeName'
     - 'Classes/SwappedArguments'
     - 'Classes/TestClass'
     - 'Classes/ThisIsForClasses'
     - 'Classes/ThisIsNotAnArray'
     - 'Classes/ThisIsNotForStatic'
     - 'Classes/ThrowInDestruct'
     - 'Classes/TooManyChildren'
     - 'Classes/TooManyDereferencing'
     - 'Classes/TooManyFinds'
     - 'Classes/TooManyInjections'
     - 'Classes/TypedClassConstants'
     - 'Classes/TypehintCyclicDependencies'
     - 'Classes/UndeclaredStaticProperty'
     - 'Classes/UndefinedClasses'
     - 'Classes/UndefinedConstants'
     - 'Classes/UndefinedMethod'
     - 'Classes/UndefinedParentMP'
     - 'Classes/UndefinedProperty'
     - 'Classes/UndefinedStaticMP'
     - 'Classes/UndefinedStaticclass'
     - 'Classes/UnfinishedObject'
     - 'Classes/UninitedProperty'
     - 'Classes/UnitializedProperties'
     - 'Classes/UnreachableConstant'
     - 'Classes/UnreachableMethod'
     - 'Classes/UnresolvedCatch'
     - 'Classes/UnresolvedClasses'
     - 'Classes/UnresolvedInstanceof'
     - 'Classes/UntypedNoDefaultProperties'
     - 'Classes/UnusedClass'
     - 'Classes/UnusedConstant'
     - 'Classes/UnusedMethods'
     - 'Classes/UnusedPrivateMethod'
     - 'Classes/UnusedPrivateProperty'
     - 'Classes/UnusedProtectedMethods'
     - 'Classes/UnusedPublicMethod'
     - 'Classes/UseClassOperator'
     - 'Classes/UseInstanceof'
     - 'Classes/UseThis'
     - 'Classes/UsedClass'
     - 'Classes/UsedMethods'
     - 'Classes/UsedOnceProperty'
     - 'Classes/UsedPrivateMethod'
     - 'Classes/UsedPrivateProperty'
     - 'Classes/UsedProtectedMethod'
     - 'Classes/UselessAbstract'
     - 'Classes/UselessAssignationOfPromotedProperty'
     - 'Classes/UselessConstantOverwrite'
     - 'Classes/UselessConstructor'
     - 'Classes/UselessFinal'
     - 'Classes/UselessMethod'
     - 'Classes/UselessNullSafeOperator'
     - 'Classes/UselessTypehint'
     - 'Classes/UsingThisOutsideAClass'
     - 'Classes/VariableClasses'
     - 'Classes/WeakType'
     - 'Classes/WrongCase'
     - 'Classes/WrongName'
     - 'Classes/WrongTypedPropertyInit'
     - 'Classes/toStringPss'
     - 'Common/InterfaceUsage'
     - 'Complete/CreateCompactVariables'
     - 'Complete/CreateDefaultValues'
     - 'Complete/CreateForeachDefault'
     - 'Complete/CreateMagicMethod'
     - 'Complete/CreateMagicProperty'
     - 'Complete/EnumCaseValues'
     - 'Complete/ExtendedTypehints'
     - 'Complete/FollowClosureDefinition'
     - 'Complete/GlobalDefinitions'
     - 'Complete/IsExtStructure'
     - 'Complete/IsPhpStructure'
     - 'Complete/IsStubStructure'
     - 'Complete/MakeAllStatics'
     - 'Complete/MakeClassConstantDefinition'
     - 'Complete/MakeClassMethodDefinition'
     - 'Complete/MakeFunctioncallWithReference'
     - 'Complete/OverwrittenConstants'
     - 'Complete/OverwrittenMethods'
     - 'Complete/OverwrittenProperties'
     - 'Complete/PhpExtStubPropertyMethod'
     - 'Complete/PhpNativeReference'
     - 'Complete/PropagateConstants'
     - 'Complete/ReturnTypehint'
     - 'Complete/SetArrayClassDefinition'
     - 'Complete/SetClassAliasDefinition'
     - 'Complete/SetClassMethodRemoteDefinition'
     - 'Complete/SetClassPropertyDefinitionWithTypehint'
     - 'Complete/SetClassRemoteDefinitionWithGlobal'
     - 'Complete/SetClassRemoteDefinitionWithInjection'
     - 'Complete/SetClassRemoteDefinitionWithLocalNew'
     - 'Complete/SetClassRemoteDefinitionWithParenthesis'
     - 'Complete/SetClassRemoteDefinitionWithReturnTypehint'
     - 'Complete/SetClassRemoteDefinitionWithTypehint'
     - 'Complete/SetCloneLink'
     - 'Complete/SetMethodFnp'
     - 'Complete/SetParentDefinition'
     - 'Complete/SolveTraitConstants'
     - 'Complete/SolveTraitMethods'
     - 'Complete/Superglobals'
     - 'Complete/VariableTypehint'
     - 'Composer/Autoload'
     - 'Composer/UseComposer'
     - 'Composer/UseComposerLock'
     - 'Constants/BadConstantnames'
     - 'Constants/CaseInsensitiveConstants'
     - 'Constants/ConditionedConstants'
     - 'Constants/ConstDefinePreference'
     - 'Constants/ConstRecommended'
     - 'Constants/ConstantStrangeNames'
     - 'Constants/ConstantUsage'
     - 'Constants/ConstantUsedOnce'
     - 'Constants/Constantnames'
     - 'Constants/CouldBeConstant'
     - 'Constants/CouldUseConstant'
     - 'Constants/CreatedOutsideItsNamespace'
     - 'Constants/CustomConstantUsage'
     - 'Constants/DefineInsensitivePreference'
     - 'Constants/DynamicCreation'
     - 'Constants/InconsistantCase'
     - 'Constants/InvalidName'
     - 'Constants/IsExtConstant'
     - 'Constants/IsGlobalConstant'
     - 'Constants/IsPhpConstant'
     - 'Constants/MagicConstantUsage'
     - 'Constants/MultipleConstantDefinition'
     - 'Constants/PhpConstantUsage'
     - 'Constants/RelayConstant'
     - 'Constants/StrangeName'
     - 'Constants/UndefinedConstants'
     - 'Constants/UnusedConstants'
     - 'Constants/VariableConstant'
     - 'Custom/MethodUsage'
     - 'Dump/ArgumentCountsPerCalls'
     - 'Dump/CallOrder'
     - 'Dump/ClassInjectionCount'
     - 'Dump/CollectAtomCounts'
     - 'Dump/CollectBlockSize'
     - 'Dump/CollectCalls'
     - 'Dump/CollectCatch'
     - 'Dump/CollectClassChanges'
     - 'Dump/CollectClassChildren'
     - 'Dump/CollectClassConstantCounts'
     - 'Dump/CollectClassDepth'
     - 'Dump/CollectClassInterfaceCounts'
     - 'Dump/CollectClassTraitsCounts'
     - 'Dump/CollectClassesDependencies'
     - 'Dump/CollectDefinitionsStats'
     - 'Dump/CollectDependencyExtension'
     - 'Dump/CollectFilesDependencies'
     - 'Dump/CollectForeachFavorite'
     - 'Dump/CollectGlobalVariables'
     - 'Dump/CollectGraphTriplets'
     - 'Dump/CollectLiterals'
     - 'Dump/CollectLocalVariableCounts'
     - 'Dump/CollectMbstringEncodings'
     - 'Dump/CollectMethodCounts'
     - 'Dump/CollectMethodsThrowingExceptions'
     - 'Dump/CollectNativeCallsPerExpressions'
     - 'Dump/CollectParameterCounts'
     - 'Dump/CollectParameterNames'
     - 'Dump/CollectPhpStructures'
     - 'Dump/CollectPropertyCounts'
     - 'Dump/CollectPropertyUsage'
     - 'Dump/CollectReadability'
     - 'Dump/CollectSetLocale'
     - 'Dump/CollectStructures'
     - 'Dump/CollectStubStructures'
     - 'Dump/CollectThrow'
     - 'Dump/CollectUseCounts'
     - 'Dump/CollectVariables'
     - 'Dump/CollectVendorStructures'
     - 'Dump/CollectsNames'
     - 'Dump/CombinedCalls'
     - 'Dump/ConstantOrder'
     - 'Dump/CouldBeAConstant'
     - 'Dump/CyclomaticComplexity'
     - 'Dump/DereferencingLevels'
     - 'Dump/DumpComparedLiterals'
     - 'Dump/EnvironnementVariables'
     - 'Dump/FossilizedMethods'
     - 'Dump/Inclusions'
     - 'Dump/IndentationLevels'
     - 'Dump/NewOrder'
     - 'Dump/ParameterArgumentsLinks'
     - 'Dump/PublicReach'
     - 'Dump/TypehintingStats'
     - 'Dump/Typehintorder'
     - 'Enums/CouldBeEnum'
     - 'Enums/DuplicateCaseValue'
     - 'Enums/NoMagicMethod'
     - 'Enums/UndefinedEnumcase'
     - 'Enums/UnusedEnumCase'
     - 'Exceptions/AlreadyCaught'
     - 'Exceptions/AnonymousCatch'
     - 'Exceptions/CantThrow'
     - 'Exceptions/CatchE'
     - 'Exceptions/CatchUndefinedVariable'
     - 'Exceptions/CaughtButNotThrown'
     - 'Exceptions/CaughtExceptions'
     - 'Exceptions/ConvertedExceptions'
     - 'Exceptions/CouldDropVariable'
     - 'Exceptions/CouldUseTry'
     - 'Exceptions/DefinedExceptions'
     - 'Exceptions/ForgottenThrown'
     - 'Exceptions/IsPhpException'
     - 'Exceptions/LargeTryBlock'
     - 'Exceptions/LongPreparation'
     - 'Exceptions/MultipleCatch'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/PossibleTypeError'
     - 'Exceptions/Rethrown'
     - 'Exceptions/SetChainingException'
     - 'Exceptions/ThrowFunctioncall'
     - 'Exceptions/ThrowRawExceptions'
     - 'Exceptions/ThrownExceptions'
     - 'Exceptions/TryNoCatch'
     - 'Exceptions/UncaughtExceptions'
     - 'Exceptions/Unthrown'
     - 'Exceptions/UnusedExceptionVariable'
     - 'Exceptions/UselessCatch'
     - 'Exceptions/UselessTry'
     - 'Extensions/Extamqp'
     - 'Extensions/Extapache'
     - 'Extensions/Extapc'
     - 'Extensions/Extapcu'
     - 'Extensions/Extarray'
     - 'Extensions/Extast'
     - 'Extensions/Extbcmath'
     - 'Extensions/Extbzip2'
     - 'Extensions/Extcalendar'
     - 'Extensions/Extcmark'
     - 'Extensions/Extcom'
     - 'Extensions/Extcrypto'
     - 'Extensions/Extcsv'
     - 'Extensions/Extctype'
     - 'Extensions/Extcurl'
     - 'Extensions/Extdate'
     - 'Extensions/Extdb2'
     - 'Extensions/Extdba'
     - 'Extensions/Extdecimal'
     - 'Extensions/Extdio'
     - 'Extensions/Extdom'
     - 'Extensions/Extds'
     - 'Extensions/Exteaccelerator'
     - 'Extensions/Exteio'
     - 'Extensions/Extenchant'
     - 'Extensions/Extev'
     - 'Extensions/Extevent'
     - 'Extensions/Extexcimer'
     - 'Extensions/Extexif'
     - 'Extensions/Extexpect'
     - 'Extensions/Extfam'
     - 'Extensions/Extfann'
     - 'Extensions/Extffi'
     - 'Extensions/Extfile'
     - 'Extensions/Extfileinfo'
     - 'Extensions/Extfilter'
     - 'Extensions/Extfpm'
     - 'Extensions/Extftp'
     - 'Extensions/Extgd'
     - 'Extensions/Extgearman'
     - 'Extensions/Extgender'
     - 'Extensions/Extgeoip'
     - 'Extensions/Extgeospatial'
     - 'Extensions/Extgettext'
     - 'Extensions/Extgmagick'
     - 'Extensions/Extgmp'
     - 'Extensions/Extgnupg'
     - 'Extensions/Extgrpc'
     - 'Extensions/Exthash'
     - 'Extensions/Exthrtime'
     - 'Extensions/Exthttp'
     - 'Extensions/Extibase'
     - 'Extensions/Extice'
     - 'Extensions/Exticonv'
     - 'Extensions/Extigbinary'
     - 'Extensions/Extimagick'
     - 'Extensions/Extimap'
     - 'Extensions/Extinfo'
     - 'Extensions/Extinotify'
     - 'Extensions/Extintl'
     - 'Extensions/Extjson'
     - 'Extensions/Extjudy'
     - 'Extensions/Extldap'
     - 'Extensions/Extleveldb'
     - 'Extensions/Extlibsodium'
     - 'Extensions/Extlibxml'
     - 'Extensions/Extlua'
     - 'Extensions/Extlzf'
     - 'Extensions/Extmail'
     - 'Extensions/Extmailparse'
     - 'Extensions/Extmath'
     - 'Extensions/Extmbstring'
     - 'Extensions/Extmcrypt'
     - 'Extensions/Extmemcache'
     - 'Extensions/Extmemcached'
     - 'Extensions/Extmongo'
     - 'Extensions/Extmongodb'
     - 'Extensions/Extmsgpack'
     - 'Extensions/Extmssql'
     - 'Extensions/Extmysql'
     - 'Extensions/Extmysqli'
     - 'Extensions/Extncurses'
     - 'Extensions/Extnewt'
     - 'Extensions/Extnsapi'
     - 'Extensions/Extob'
     - 'Extensions/Extoci8'
     - 'Extensions/Extodbc'
     - 'Extensions/Extopcache'
     - 'Extensions/Extopencensus'
     - 'Extensions/Extopenssl'
     - 'Extensions/Extparle'
     - 'Extensions/Extpassword'
     - 'Extensions/Extpcntl'
     - 'Extensions/Extpcov'
     - 'Extensions/Extpcre'
     - 'Extensions/Extpdo'
     - 'Extensions/Extpgsql'
     - 'Extensions/Extphalcon'
     - 'Extensions/Extphar'
     - 'Extensions/Extpkcs11'
     - 'Extensions/Extposix'
     - 'Extensions/Extprotobuf'
     - 'Extensions/Extpspell'
     - 'Extensions/Extpsr'
     - 'Extensions/Extrandom'
     - 'Extensions/Extrar'
     - 'Extensions/Extrdkafka'
     - 'Extensions/Extreadline'
     - 'Extensions/Extredis'
     - 'Extensions/Extreflection'
     - 'Extensions/Extscrypt'
     - 'Extensions/Extsdl'
     - 'Extensions/Extseaslog'
     - 'Extensions/Extsem'
     - 'Extensions/Extsession'
     - 'Extensions/Extshmop'
     - 'Extensions/Extsimplexml'
     - 'Extensions/Extsnmp'
     - 'Extensions/Extsoap'
     - 'Extensions/Extsockets'
     - 'Extensions/Extsphinx'
     - 'Extensions/Extspl'
     - 'Extensions/Extspx'
     - 'Extensions/Extsqlite'
     - 'Extensions/Extsqlite3'
     - 'Extensions/Extsqlsrv'
     - 'Extensions/Extssh2'
     - 'Extensions/Extstandard'
     - 'Extensions/Extstats'
     - 'Extensions/Extstomp'
     - 'Extensions/Extstring'
     - 'Extensions/Extsuhosin'
     - 'Extensions/Extsvm'
     - 'Extensions/Extswoole'
     - 'Extensions/Exttaint'
     - 'Extensions/Extteds'
     - 'Extensions/Exttidy'
     - 'Extensions/Exttokenizer'
     - 'Extensions/Exttokyotyrant'
     - 'Extensions/Exttrader'
     - 'Extensions/Extuopz'
     - 'Extensions/Extuuid'
     - 'Extensions/Extv8js'
     - 'Extensions/Extvarnish'
     - 'Extensions/Extvips'
     - 'Extensions/Extwasm'
     - 'Extensions/Extwddx'
     - 'Extensions/Extweakref'
     - 'Extensions/Extxattr'
     - 'Extensions/Extxdebug'
     - 'Extensions/Extxdiff'
     - 'Extensions/Extxhprof'
     - 'Extensions/Extxml'
     - 'Extensions/Extxmlreader'
     - 'Extensions/Extxmlrpc'
     - 'Extensions/Extxmlwriter'
     - 'Extensions/Extxsl'
     - 'Extensions/Extxxtea'
     - 'Extensions/Extyaml'
     - 'Extensions/Extyar'
     - 'Extensions/Extzendmonitor'
     - 'Extensions/Extzip'
     - 'Extensions/Extzlib'
     - 'Extensions/Extzmq'
     - 'Extensions/Extzookeeper'
     - 'Files/DefinitionsOnly'
     - 'Files/GlobalCodeOnly'
     - 'Files/IsCliScript'
     - 'Files/IsComponent'
     - 'Files/MissingInclude'
     - 'Files/NotDefinitionsOnly'
     - 'Files/Services'
     - 'Functions/AddDefaultValue'
     - 'Functions/AliasesUsage'
     - 'Functions/AvoidBooleanArgument'
     - 'Functions/BadTypehintRelay'
     - 'Functions/CallbackNeedsReturn'
     - 'Functions/CanCallGenerator'
     - 'Functions/CancelledParameter'
     - 'Functions/CannotUseStaticForClosure'
     - 'Functions/CantUse'
     - 'Functions/Closure2String'
     - 'Functions/Closures'
     - 'Functions/ConditionedFunctions'
     - 'Functions/CouldBeCallable'
     - 'Functions/CouldBeStaticClosure'
     - 'Functions/CouldCentralize'
     - 'Functions/CouldTypeWithArray'
     - 'Functions/CouldTypeWithBool'
     - 'Functions/CouldTypeWithInt'
     - 'Functions/CouldTypeWithIterable'
     - 'Functions/CouldTypeWithString'
     - 'Functions/CouldTypehint'
     - 'Functions/DeepDefinitions'
     - 'Functions/DeprecatedCallable'
     - 'Functions/DontUseVoid'
     - 'Functions/DuplicateNamedParameter'
     - 'Functions/DynamicCode'
     - 'Functions/Dynamiccall'
     - 'Functions/EmptyFunction'
     - 'Functions/ExceedingTypehint'
     - 'Functions/FallbackFunction'
     - 'Functions/FnArgumentVariableConfusion'
     - 'Functions/FunctionCalledWithOtherCase'
     - 'Functions/Functionnames'
     - 'Functions/FunctionsUsingReference'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/HardcodedPasswords'
     - 'Functions/HasFluentInterface'
     - 'Functions/HasNotFluentInterface'
     - 'Functions/Identity'
     - 'Functions/InsufficientTypehint'
     - 'Functions/IsExtFunction'
     - 'Functions/IsGenerator'
     - 'Functions/IsGlobal'
     - 'Functions/KillsApp'
     - 'Functions/LoopCalling'
     - 'Functions/MethodIsNotAnIf'
     - 'Functions/MismatchParameterAndType'
     - 'Functions/MismatchParameterName'
     - 'Functions/MismatchTypeAndDefault'
     - 'Functions/MismatchedDefaultArguments'
     - 'Functions/MismatchedTypehint'
     - 'Functions/MissingTypehint'
     - 'Functions/ModifyTypedParameter'
     - 'Functions/MultipleDeclarations'
     - 'Functions/MultipleIdenticalClosure'
     - 'Functions/MultipleReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/MustReturn'
     - 'Functions/NeverUsedParameter'
     - 'Functions/NoBooleanAsDefault'
     - 'Functions/NoClassAsTypehint'
     - 'Functions/NoDefaultForReference'
     - 'Functions/NoLiteralForReference'
     - 'Functions/NoReferencedVoid'
     - 'Functions/NoReturnUsed'
     - 'Functions/NullTypeFavorite'
     - 'Functions/NullableWithoutCheck'
     - 'Functions/OneLetterFunctions'
     - 'Functions/OnlyVariableForReference'
     - 'Functions/OnlyVariablePassedByReference'
     - 'Functions/OptionalParameter'
     - 'Functions/ParameterHiding'
     - 'Functions/PrefixToType'
     - 'Functions/RealFunctions'
     - 'Functions/Recursive'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/RelayFunction'
     - 'Functions/RemoveParameterWithNamedOnes'
     - 'Functions/RetypedReference'
     - 'Functions/SemanticTyping'
     - 'Functions/ShouldBeTypehinted'
     - 'Functions/ShouldUseConstants'
     - 'Functions/ShouldYieldWithKey'
     - 'Functions/TooManyLocalVariables'
     - 'Functions/TooManyParameters'
     - 'Functions/TooMuchIndented'
     - 'Functions/TypeDodging'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/TypehintedReferences'
     - 'Functions/Typehints'
     - 'Functions/UnbindingClosures'
     - 'Functions/UndefinedFunctions'
     - 'Functions/UnknownParameterName'
     - 'Functions/UnsetOnArguments'
     - 'Functions/UnusedArguments'
     - 'Functions/UnusedFunctions'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UnusedReturnedValue'
     - 'Functions/UseArrowFunctions'
     - 'Functions/UseConstantAsArguments'
     - 'Functions/UseConstantsAsReturns'
     - 'Functions/UsedFunctions'
     - 'Functions/UselessArgument'
     - 'Functions/UselessDefault'
     - 'Functions/UselessReferenceArgument'
     - 'Functions/UselessReturn'
     - 'Functions/UselessTypeCheck'
     - 'Functions/UsesDefaultArguments'
     - 'Functions/UsingDeprecated'
     - 'Functions/VariableArguments'
     - 'Functions/VariableParameterAmbiguityInArrowFunction'
     - 'Functions/VoidIsNotAReference'
     - 'Functions/WithoutReturn'
     - 'Functions/WrongArgumentNameWithPhpFunction'
     - 'Functions/WrongArgumentType'
     - 'Functions/WrongCase'
     - 'Functions/WrongNumberOfArguments'
     - 'Functions/WrongNumberOfArgumentsMethods'
     - 'Functions/WrongOptionalParameter'
     - 'Functions/WrongReturnedType'
     - 'Functions/WrongTypeWithCall'
     - 'Functions/WrongTypehintedName'
     - 'Functions/funcGetArgModified'
     - 'Interfaces/AlreadyParentsInterface'
     - 'Interfaces/AvoidSelfInInterface'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/CantOverloadConstants'
     - 'Interfaces/CouldUseInterface'
     - 'Interfaces/EmptyInterface'
     - 'Interfaces/InheritedClassConstantVisibility'
     - 'Interfaces/InterfaceMethod'
     - 'Interfaces/InterfaceUsage'
     - 'Interfaces/Interfacenames'
     - 'Interfaces/IsExtInterface'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/NoConstructorInInterface'
     - 'Interfaces/NoGaranteeForPropertyConstant'
     - 'Interfaces/Php'
     - 'Interfaces/PossibleInterfaces'
     - 'Interfaces/RepeatedInterface'
     - 'Interfaces/UndefinedInterfaces'
     - 'Interfaces/UnusedInterfaces'
     - 'Interfaces/UsedInterfaces'
     - 'Interfaces/UselessInterfaces'
     - 'Namespaces/Alias'
     - 'Namespaces/AliasConfusion'
     - 'Namespaces/ConstantFullyQualified'
     - 'Namespaces/ConstantWithUseFavorite'
     - 'Namespaces/CouldUseAlias'
     - 'Namespaces/CouldUseMagicConstant'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/GlobalImport'
     - 'Namespaces/HiddenUse'
     - 'Namespaces/MultipleAliasDefinitionPerFile'
     - 'Namespaces/MultipleAliasDefinitions'
     - 'Namespaces/NamespaceUsage'
     - 'Namespaces/Namespacesnames'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Namespaces/OverloadExistingNames'
     - 'Namespaces/ShouldMakeAlias'
     - 'Namespaces/UnresolvedUse'
     - 'Namespaces/UnusedUse'
     - 'Namespaces/UseFunctionsConstants'
     - 'Namespaces/UseWithFullyQualifiedNS'
     - 'Namespaces/UsedUse'
     - 'Namespaces/WrongCase'
     - 'Patterns/AbstractAway'
     - 'Patterns/CourrierAntiPattern'
     - 'Patterns/DependencyInjection'
     - 'Patterns/Factory'
     - 'Patterns/GetterSetter'
     - 'Performances/ArrayKeyExistsSpeedup'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/Autoappend'
     - 'Performances/AvoidArrayPush'
     - 'Performances/CacheVariableOutsideLoop'
     - 'Performances/ClassOperator'
     - 'Performances/CountToAppend'
     - 'Performances/CsvInLoops'
     - 'Performances/DoInBase'
     - 'Performances/DoubleArrayFlip'
     - 'Performances/EllipsisMerge'
     - 'Performances/FetchOneRowFormat'
     - 'Performances/IssetWholeArray'
     - 'Performances/JoinFile'
     - 'Performances/LogicalToInArray'
     - 'Performances/MakeOneCall'
     - 'Performances/MbStringInLoop'
     - 'Performances/MemoizeMagicCall'
     - 'Performances/NoConcatInLoop'
     - 'Performances/NoGlob'
     - 'Performances/NotCountNull'
     - 'Performances/OptimizeExplode'
     - 'Performances/PHP7EncapsedStrings'
     - 'Performances/Php74ArrayKeyExists'
     - 'Performances/PreCalculateUse'
     - 'Performances/PrePostIncrement'
     - 'Performances/RegexOnArrays'
     - 'Performances/RegexOnCollector'
     - 'Performances/ShouldCacheLocal'
     - 'Performances/SimpleSwitch'
     - 'Performances/SimplifyForeach'
     - 'Performances/SkipEmptyArray'
     - 'Performances/SlowFunctions'
     - 'Performances/StaticCallDontNeedObjects'
     - 'Performances/StaticCallWithSelf'
     - 'Performances/StrposTooMuch'
     - 'Performances/SubstrFirst'
     - 'Performances/SubstrInLoops'
     - 'Performances/TooManyExtractions'
     - 'Performances/UseArraySlice'
     - 'Performances/UseBlindVar'
     - 'Performances/timeVsstrtotime'
     - 'Php/AlternativeSyntax'
     - 'Php/Argon2Usage'
     - 'Php/ArrayKeyExistsWithObjects'
     - 'Php/AssertFunctionIsReserved'
     - 'Php/AssertionUsage'
     - 'Php/AssignAnd'
     - 'Php/Assumptions'
     - 'Php/AutoloadUsage'
     - 'Php/AvoidGetobjectVars'
     - 'Php/AvoidMbDectectEncoding'
     - 'Php/AvoidReal'
     - 'Php/AvoidSetErrorHandlerContextArg'
     - 'Php/BetterRand'
     - 'Php/CallingStaticTraitMethod'
     - 'Php/CantUseReturnValueInWriteContext'
     - 'Php/CaseForPSS'
     - 'Php/CastUnsetUsage'
     - 'Php/CastingUsage'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClassConstWithArray'
     - 'Php/ClassFunctionConfusion'
     - 'Php/CloneConstant'
     - 'Php/CloseTags'
     - 'Php/CloseTagsConsistency'
     - 'Php/ClosureInConstant'
     - 'Php/ClosureThisSupport'
     - 'Php/Coalesce'
     - 'Php/CoalesceEqual'
     - 'Php/CompactInexistant'
     - 'Php/ComparisonOnDifferentTypes'
     - 'Php/ConcatAndAddition'
     - 'Php/ConstWithArray'
     - 'Php/CookiesVariables'
     - 'Php/CouldUseIsCountable'
     - 'Php/CouldUsePromotedProperties'
     - 'Php/Crc32MightBeNegative'
     - 'Php/CryptoUsage'
     - 'Php/DateFormats'
     - 'Php/DateTimeNotImmutable'
     - 'Php/DeclareEncoding'
     - 'Php/DeclareStrict'
     - 'Php/DeclareStrictType'
     - 'Php/DeclareTicks'
     - 'Php/DefineWithArray'
     - 'Php/DeprecateDollarCurly'
     - 'Php/Deprecated'
     - 'Php/DetectCurrentClass'
     - 'Php/DirectCallToClone'
     - 'Php/DirectiveName'
     - 'Php/DirectivesUsage'
     - 'Php/DlUsage'
     - 'Php/DontPolluteGlobalSpace'
     - 'Php/EchoTagUsage'
     - 'Php/EllipsisUsage'
     - 'Php/EmptyList'
     - 'Php/EnumUsage'
     - 'Php/ErrorLogUsage'
     - 'Php/ExitNoArg'
     - 'Php/ExponentUsage'
     - 'Php/FailingAnalysis'
     - 'Php/FalseToArray'
     - 'Php/FilesFullPath'
     - 'Php/FilterToAddSlashes'
     - 'Php/FinalConstant'
     - 'Php/FirstClassCallable'
     - 'Php/FlexibleHeredoc'
     - 'Php/FopenMode'
     - 'Php/ForeachDontChangePointer'
     - 'Php/ForeachObject'
     - 'Php/GlobalWithoutSimpleVariable'
     - 'Php/GlobalsVsGlobal'
     - 'Php/Gotonames'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/Haltcompiler'
     - 'Php/HasAsymmetricVisibility'
     - 'Php/HasPropertyHook'
     - 'Php/HasVirtualProperty'
     - 'Php/HashAlgos'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashAlgos71'
     - 'Php/HashAlgos74'
     - 'Php/HashUsesObjects'
     - 'Php/IdnUts46'
     - 'Php/ImplodeOneArg'
     - 'Php/IncludeVariables'
     - 'Php/IncomingValues'
     - 'Php/IncomingVariables'
     - 'Php/Incompilable'
     - 'Php/IntegerSeparatorUsage'
     - 'Php/InternalParameterType'
     - 'Php/IsAWithString'
     - 'Php/IsINF'
     - 'Php/IsNAN'
     - 'Php/IsnullVsEqualNull'
     - 'Php/IssetMultipleArgs'
     - 'Php/JsonSerializeReturnType'
     - 'Php/Labelnames'
     - 'Php/LetterCharsLogicalFavorite'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithAppends'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/LogicalInLetters'
     - 'Php/MethodCallOnNew'
     - 'Php/MiddleVersion'
     - 'Php/MissingMagicIsset'
     - 'Php/MissingSubpattern'
     - 'Php/MixedKeyword'
     - 'Php/MixedUsage'
     - 'Php/MultipleDeclareStrict'
     - 'Php/MustCallParentConstructor'
     - 'Php/NamedArgumentAndVariadic'
     - 'Php/NamedParameterUsage'
     - 'Php/NativeClassTypeCompatibility'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NeverKeyword'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewExponent'
     - 'Php/NewInitializers'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoCastToInt'
     - 'Php/NoClassInGlobal'
     - 'Php/NoListWithString'
     - 'Php/NoMoreCurlyArrays'
     - 'Php/NoNullForNative'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoReferenceForTernary'
     - 'Php/NoReturnForGenerator'
     - 'Php/NoStringWithAppend'
     - 'Php/NoSubstrMinusOne'
     - 'Php/NotScalarType'
     - 'Php/OnlyVariablePassedByReference'
     - 'Php/OpensslEncryptAlgoChange'
     - 'Php/OveriddenFunction'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Password55'
     - 'Php/PathinfoReturns'
     - 'Php/PearUsage'
     - 'Php/Php54NewFunctions'
     - 'Php/Php54RemovedFunctions'
     - 'Php/Php55NewFunctions'
     - 'Php/Php55RemovedFunctions'
     - 'Php/Php56NewFunctions'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php70RemovedDirective'
     - 'Php/Php70RemovedFunctions'
     - 'Php/Php71NewClasses'
     - 'Php/Php71NewFunctions'
     - 'Php/Php71RemovedDirective'
     - 'Php/Php71microseconds'
     - 'Php/Php72Deprecation'
     - 'Php/Php72NewClasses'
     - 'Php/Php72NewConstants'
     - 'Php/Php72NewFunctions'
     - 'Php/Php72ObjectKeyword'
     - 'Php/Php72RemovedFunctions'
     - 'Php/Php73NewFunctions'
     - 'Php/Php73RemovedFunctions'
     - 'Php/Php74Deprecation'
     - 'Php/Php74NewClasses'
     - 'Php/Php74NewConstants'
     - 'Php/Php74NewDirective'
     - 'Php/Php74NewFunctions'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php74RemovedFunctions'
     - 'Php/Php74ReservedKeyword'
     - 'Php/Php74mbstrrpos3rdArg'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php80NamedParameterVariadic'
     - 'Php/Php80NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80RemovedConstant'
     - 'Php/Php80RemovedDirective'
     - 'Php/Php80RemovedFunctions'
     - 'Php/Php80RemovesResources'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php80VariableSyntax'
     - 'Php/Php81IntersectionTypehint'
     - 'Php/Php81NewFunctions'
     - 'Php/Php81NewTypes'
     - 'Php/Php81RemovedConstant'
     - 'Php/Php81RemovedDirective'
     - 'Php/Php81RemovedFunctions'
     - 'Php/Php81RemovesResources'
     - 'Php/Php82NewFunctions'
     - 'Php/Php82NewTypes'
     - 'Php/Php83NewClasses'
     - 'Php/Php83NewFunctions'
     - 'Php/Php84NewFunctions'
     - 'Php/PhpErrorMsgUsage'
     - 'Php/PlusPlusOnLetters'
     - 'Php/PregMatchAllFlag'
     - 'Php/Prints'
     - 'Php/RawPostDataUsage'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/ReflectionExportIsDeprecated'
     - 'Php/ReservedKeywords7'
     - 'Php/ReservedMatchKeyword'
     - 'Php/ReservedMethods'
     - 'Php/ReservedNames'
     - 'Php/RestrictGlobalUsage'
     - 'Php/ReturnTypehintUsage'
     - 'Php/ReturnWithParenthesis'
     - 'Php/SafePhpvars'
     - 'Php/ScalarAreNotArrays'
     - 'Php/ScalarTypehintUsage'
     - 'Php/SerializeMagic'
     - 'Php/SessionVariables'
     - 'Php/SetExceptionHandlerPHP7'
     - 'Php/SetHandlers'
     - 'Php/ShellFavorite'
     - 'Php/ShortOpenTagRequired'
     - 'Php/ShortTernary'
     - 'Php/ShouldPreprocess'
     - 'Php/ShouldUseArrayColumn'
     - 'Php/ShouldUseArrayFilter'
     - 'Php/ShouldUseCoalesce'
     - 'Php/ShouldUseFunction'
     - 'Php/SignatureTrailingComma'
     - 'Php/SpreadOperatorForArray'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/StaticclassUsage'
     - 'Php/StringIntComparison'
     - 'Php/StrposWithIntegers'
     - 'Php/StrtrArguments'
     - 'Php/SuperGlobalUsage'
     - 'Php/ThrowUsage'
     - 'Php/ThrowWasAnExpression'
     - 'Php/TooManyNativeCalls'
     - 'Php/TrailingComma'
     - 'Php/TriggerErrorUsage'
     - 'Php/TriggerErrorUserError'
     - 'Php/TryCatchUsage'
     - 'Php/TryMultipleCatch'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnknownPcre2Option'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UnsetOrCast'
     - 'Php/UpperCaseFunction'
     - 'Php/UpperCaseKeyword'
     - 'Php/UseAttributes'
     - 'Php/UseBrowscap'
     - 'Php/UseClassAlias'
     - 'Php/UseCli'
     - 'Php/UseContravariance'
     - 'Php/UseCookies'
     - 'Php/UseCovariance'
     - 'Php/UseDNF'
     - 'Php/UseDateTimeImmutable'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseGetDebugType'
     - 'Php/UseMatch'
     - 'Php/UseNullSafeOperator'
     - 'Php/UseNullableType'
     - 'Php/UseObjectApi'
     - 'Php/UsePathinfo'
     - 'Php/UsePathinfoArgs'
     - 'Php/UseSessionStartOptions'
     - 'Php/UseSetCookie'
     - 'Php/UseStdclass'
     - 'Php/UseStrContains'
     - 'Php/UseTrailingUseComma'
     - 'Php/UseWeb'
     - 'Php/UsesEnv'
     - 'Php/UsortSorting'
     - 'Php/Utf8EncodeDeprecated'
     - 'Php/VersionCompareOperator'
     - 'Php/WrongAttributeConfiguration'
     - 'Php/WrongTypeForNativeFunction'
     - 'Php/YieldFromUsage'
     - 'Php/YieldUsage'
     - 'Php/debugInfoUsage'
     - 'Php/oldAutoloadUsage'
     - 'Portability/FopenMode'
     - 'Portability/GlobBraceUsage'
     - 'Portability/IconvTranslit'
     - 'Portability/LinuxOnlyFiles'
     - 'Portability/WindowsOnlyConstants'
     - 'Project/IsLibrary'
     - 'Psr/Psr11Usage'
     - 'Psr/Psr13Usage'
     - 'Psr/Psr16Usage'
     - 'Psr/Psr3Usage'
     - 'Psr/Psr6Usage'
     - 'Psr/Psr7Usage'
     - 'Security/AnchorRegex'
     - 'Security/AvoidThoseCrypto'
     - 'Security/CantDisableClass'
     - 'Security/CantDisableFunction'
     - 'Security/CompareHash'
     - 'Security/ConfigureExtract'
     - 'Security/CryptoKeyLength'
     - 'Security/CurlOptions'
     - 'Security/DirectInjection'
     - 'Security/DontEchoError'
     - 'Security/DynamicDl'
     - 'Security/EncodedLetters'
     - 'Security/FilterInputSource'
     - 'Security/FilterNotRaw'
     - 'Security/GPRAliases'
     - 'Security/IncompatibleTypesWithIncoming'
     - 'Security/IndirectInjection'
     - 'Security/IntegerConversion'
     - 'Security/KeepFilesRestricted'
     - 'Security/MinusOneOnError'
     - 'Security/MkdirDefault'
     - 'Security/MoveUploadedFile'
     - 'Security/NoEntIgnore'
     - 'Security/NoNetForXmlLoad'
     - 'Security/NoSleep'
     - 'Security/NoWeakSSLCrypto'
     - 'Security/RegisterGlobals'
     - 'Security/SafeHttpHeaders'
     - 'Security/SensitiveArgument'
     - 'Security/SessionCachedData'
     - 'Security/SessionLazyWrite'
     - 'Security/SetCookieArgs'
     - 'Security/ShouldUsePreparedStatement'
     - 'Security/ShouldUseSessionRegenerateId'
     - 'Security/Sqlite3RequiresSingleQuotes'
     - 'Security/SuperGlobalContagion'
     - 'Security/UnserializeSecondArg'
     - 'Security/UploadFilenameInjection'
     - 'Security/parseUrlWithoutParameters'
     - 'Structures/AddZero'
     - 'Structures/AlteringForeachWithoutReference'
     - 'Structures/AlternativeConsistenceByFile'
     - 'Structures/AlwaysFalse'
     - 'Structures/ArrayAccessOnLiteralArray'
     - 'Structures/ArrayAddition'
     - 'Structures/ArrayCountTripleEqual'
     - 'Structures/ArrayFillWithObjects'
     - 'Structures/ArrayMapPassesByValue'
     - 'Structures/ArrayMergeAndVariadic'
     - 'Structures/ArrayMergeArrayArray'
     - 'Structures/ArrayMergeWithEllipsis'
     - 'Structures/ArraySearchMultipleKeys'
     - 'Structures/AssigneAndCompare'
     - 'Structures/AssignedInOneBranch'
     - 'Structures/AutoUnsetForeach'
     - 'Structures/BailOutEarly'
     - 'Structures/BasenameSuffix'
     - 'Structures/BlindVariableUsedBeyondLoop'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/Bracketless'
     - 'Structures/Break0'
     - 'Structures/BreakNonInteger'
     - 'Structures/BreakOutsideLoop'
     - 'Structures/BuriedAssignation'
     - 'Structures/CalltimePassByReference'
     - 'Structures/CanCountNonCountable'
     - 'Structures/CannotUseAppendForReading'
     - 'Structures/CastFavorite'
     - 'Structures/CastToBoolean'
     - 'Structures/CastingTernary'
     - 'Structures/CatchShadowsVariable'
     - 'Structures/CheckAllTypes'
     - 'Structures/CheckDivision'
     - 'Structures/CheckJson'
     - 'Structures/CoalesceAndConcat'
     - 'Structures/CoalesceNullCoalesce'
     - 'Structures/CommonAlternatives'
     - 'Structures/ComparedButNotAssignedStrings'
     - 'Structures/ComparedComparison'
     - 'Structures/ComparisonFavorite'
     - 'Structures/ComplexExpression'
     - 'Structures/ConcatEmpty'
     - 'Structures/ConcatenationInterpolationFavorite'
     - 'Structures/ConditionalStructures'
     - 'Structures/ConstDefineFavorite'
     - 'Structures/ConstantComparisonConsistance'
     - 'Structures/ConstantConditions'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/CouldBeArrayCombine'
     - 'Structures/CouldBeElse'
     - 'Structures/CouldBeSpaceship'
     - 'Structures/CouldBeStatic'
     - 'Structures/CouldBeTernary'
     - 'Structures/CouldCastToArray'
     - 'Structures/CouldUseArrayFillKeys'
     - 'Structures/CouldUseArraySum'
     - 'Structures/CouldUseArrayUnique'
     - 'Structures/CouldUseCompact'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseMatch'
     - 'Structures/CouldUseNullableOperator'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrContains'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/CouldUseYieldFrom'
     - 'Structures/CountIsNotNegative'
     - 'Structures/CryptWithoutSalt'
     - 'Structures/CurlVersionNow'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/DateTimePreference'
     - 'Structures/DeclareStaticOnce'
     - 'Structures/DefaultThenDiscard'
     - 'Structures/DeprecatedMbEncoding'
     - 'Structures/DereferencingAS'
     - 'Structures/DieExitConsistance'
     - 'Structures/DifferencePreference'
     - 'Structures/DirThenSlash'
     - 'Structures/DirectlyUseFile'
     - 'Structures/DontAddSeconds'
     - 'Structures/DontBeTooManual'
     - 'Structures/DontChangeBlindKey'
     - 'Structures/DontCompareTypedBoolean'
     - 'Structures/DontLoopOnYield'
     - 'Structures/DontMixPlusPlus'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Structures/DontReuseForeachSource'
     - 'Structures/DontUseTheTypeAsVariable'
     - 'Structures/DoubleAssignation'
     - 'Structures/DoubleChecks'
     - 'Structures/DoubleInstruction'
     - 'Structures/DoubleObjectAssignation'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/DuplicateCalls'
     - 'Structures/DynamicCalls'
     - 'Structures/DynamicCode'
     - 'Structures/EchoPrintConsistance'
     - 'Structures/EchoWithConcat'
     - 'Structures/ElseIfElseif'
     - 'Structures/ElseUsage'
     - 'Structures/EmptyBlocks'
     - 'Structures/EmptyJsonError'
     - 'Structures/EmptyLines'
     - 'Structures/EmptyLoop'
     - 'Structures/EmptyTryCatch'
     - 'Structures/EmptyWithExpression'
     - 'Structures/ErrorMessages'
     - 'Structures/ErrorReportingWithInteger'
     - 'Structures/EvalUsage'
     - 'Structures/EvalWithoutTry'
     - 'Structures/ExitUsage'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/Fallthrough'
     - 'Structures/FilePutContentsDataType'
     - 'Structures/FileUploadUsage'
     - 'Structures/FileUsage'
     - 'Structures/ForWithFunctioncall'
     - 'Structures/ForeachNeedReferencedSource'
     - 'Structures/ForeachOnObject'
     - 'Structures/ForeachReferenceIsNotModified'
     - 'Structures/ForeachSourceValue'
     - 'Structures/ForeachWithList'
     - 'Structures/ForgottenWhiteSpace'
     - 'Structures/FunctionPreSubscripting'
     - 'Structures/FunctionSubscripting'
     - 'Structures/GetClassWithoutArg'
     - 'Structures/GlobalInGlobal'
     - 'Structures/GlobalOutsideLoop'
     - 'Structures/GlobalUsage'
     - 'Structures/GoToKeyDirectly'
     - 'Structures/GtOrLtFavorite'
     - 'Structures/HeredocDelimiterFavorite'
     - 'Structures/Htmlentitiescall'
     - 'Structures/HtmlentitiescallDefaultFlag'
     - 'Structures/IdenticalCase'
     - 'Structures/IdenticalConditions'
     - 'Structures/IdenticalConsecutive'
     - 'Structures/IdenticalElseif'
     - 'Structures/IdenticalOnBothSides'
     - 'Structures/IdenticalVariablesInForeach'
     - 'Structures/IfThenReturnFavorite'
     - 'Structures/IfWithSameConditions'
     - 'Structures/Iffectation'
     - 'Structures/ImplicitConversionToInt'
     - 'Structures/ImplicitGlobal'
     - 'Structures/ImpliedIf'
     - 'Structures/ImplodeArgsOrder'
     - 'Structures/IncludeUsage'
     - 'Structures/InconsistentConcatenation'
     - 'Structures/InconsistentElseif'
     - 'Structures/IndicesAreIntOrString'
     - 'Structures/InfiniteRecursion'
     - 'Structures/InitThenIf'
     - 'Structures/InvalidCast'
     - 'Structures/InvalidDateScanningFormat'
     - 'Structures/InvalidPackFormat'
     - 'Structures/InvalidRegex'
     - 'Structures/IsAVersusInstanceof'
     - 'Structures/IsZero'
     - 'Structures/IssetWithConstant'
     - 'Structures/JsonEncodeExceptions'
     - 'Structures/JsonWithOption'
     - 'Structures/ListOmissions'
     - 'Structures/LogicalMistakes'
     - 'Structures/LoneBlock'
     - 'Structures/LongArguments'
     - 'Structures/LongBlock'
     - 'Structures/MailUsage'
     - 'Structures/MaxLevelOfIdentation'
     - 'Structures/MbStringNonEncodings'
     - 'Structures/MbstringThirdArg'
     - 'Structures/MbstringUnknownEncoding'
     - 'Structures/McryptcreateivWithoutOption'
     - 'Structures/MergeIfThen'
     - 'Structures/MergeTernaryIntoIfthen'
     - 'Structures/MismatchedTernary'
     - 'Structures/MissingAssignation'
     - 'Structures/MissingCases'
     - 'Structures/MissingNew'
     - 'Structures/MissingParenthesis'
     - 'Structures/MisusedYield'
     - 'Structures/MixedConcatInterpolation'
     - 'Structures/ModernEmpty'
     - 'Structures/MultilineExpressions'
     - 'Structures/MultipleCatch'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultipleSimilarCalls'
     - 'Structures/MultipleTypeCasesInSwitch'
     - 'Structures/MultipleTypeVariable'
     - 'Structures/MultipleUnset'
     - 'Structures/MultiplyByOne'
     - 'Structures/NamedRegex'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NegativePow'
     - 'Structures/NestedIfthen'
     - 'Structures/NestedLoops'
     - 'Structures/NestedMatch'
     - 'Structures/NestedTernary'
     - 'Structures/NeverNegative'
     - 'Structures/NewLineStyle'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoAppendOnSource'
     - 'Structures/NoArrayUnique'
     - 'Structures/NoAssignationInFunction'
     - 'Structures/NoChangeIncomingVariables'
     - 'Structures/NoChoice'
     - 'Structures/NoDirectAccess'
     - 'Structures/NoDirectUsage'
     - 'Structures/NoEmptyRegex'
     - 'Structures/NoEmptyStringWithExplode'
     - 'Structures/NoGetClassNull'
     - 'Structures/NoHardcodedHash'
     - 'Structures/NoHardcodedIp'
     - 'Structures/NoHardcodedPath'
     - 'Structures/NoHardcodedPort'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/NoMaxOnEmptyArray'
     - 'Structures/NoNeedForElse'
     - 'Structures/NoNeedForTriple'
     - 'Structures/NoNeedGetClass'
     - 'Structures/NoNullForIndex'
     - 'Structures/NoObjectAsIndex'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoReferenceOnLeft'
     - 'Structures/NoReturnInFinally'
     - 'Structures/NoSubstrOne'
     - 'Structures/NoValidCast'
     - 'Structures/NoVariableIsACondition'
     - 'Structures/NonBreakableSpaceInNames'
     - 'Structures/NonIntStringAsIndex'
     - 'Structures/Noscream'
     - 'Structures/NotEqual'
     - 'Structures/NotNot'
     - 'Structures/NotOrNot'
     - 'Structures/ObjectReferences'
     - 'Structures/OnceUsage'
     - 'Structures/OneDotOrObjectOperatorPerLine'
     - 'Structures/OneExpressionBracketsConsistency'
     - 'Structures/OneIfIsSufficient'
     - 'Structures/OneLevelOfIndentation'
     - 'Structures/OneLineTwoInstructions'
     - 'Structures/OnlyFirstByte'
     - 'Structures/OnlyVariableReturnedByReference'
     - 'Structures/OpensslRandomPseudoByteSecondArg'
     - 'Structures/OrDie'
     - 'Structures/OverwrittenForeachVar'
     - 'Structures/PHP7Dirname'
     - 'Structures/PhpinfoUsage'
     - 'Structures/PlusEgalOne'
     - 'Structures/PossibleIncrement'
     - 'Structures/PossibleInfiniteLoop'
     - 'Structures/PrintAndDie'
     - 'Structures/PrintWithoutParenthesis'
     - 'Structures/PrintfArguments'
     - 'Structures/PropertyVariableConfusion'
     - 'Structures/QueriesInLoop'
     - 'Structures/RandomWithoutTry'
     - 'Structures/RecalledCondition'
     - 'Structures/RegexDelimiter'
     - 'Structures/RepeatedPrint'
     - 'Structures/RepeatedRegex'
     - 'Structures/ResourcesUsage'
     - 'Structures/ResultMayBeMissing'
     - 'Structures/ReturnTrueFalse'
     - 'Structures/ReturnVoid'
     - 'Structures/ReuseVariable'
     - 'Structures/SGVariablesConfusion'
     - 'Structures/SameConditions'
     - 'Structures/SequenceInFor'
     - 'Structures/SetAside'
     - 'Structures/SetlocaleNeedsConstants'
     - 'Structures/ShellUsage'
     - 'Structures/ShortOrCompleteComparison'
     - 'Structures/ShortTags'
     - 'Structures/ShouldChainException'
     - 'Structures/ShouldMakeTernary'
     - 'Structures/ShouldPreprocess'
     - 'Structures/ShouldUseExplodeArgs'
     - 'Structures/ShouldUseForeach'
     - 'Structures/ShouldUseMath'
     - 'Structures/ShouldUseOperator'
     - 'Structures/SimplePreg'
     - 'Structures/SprintfFormatCompilation'
     - 'Structures/StaticInclude'
     - 'Structures/StaticLoop'
     - 'Structures/StrictInArrayFavorite'
     - 'Structures/StringInterpolationFavorite'
     - 'Structures/StripTagsSkipsClosedTag'
     - 'Structures/StrposCompare'
     - 'Structures/StrposLessThanOne'
     - 'Structures/SubstrLastArg'
     - 'Structures/SubstrToTrim'
     - 'Structures/SuspiciousComparison'
     - 'Structures/SwitchToSwitch'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/SwitchWithoutDefault'
     - 'Structures/TernaryInConcat'
     - 'Structures/TestThenCast'
     - 'Structures/ThrowsAndAssign'
     - 'Structures/TimestampDifference'
     - 'Structures/TooManyChainedCalls'
     - 'Structures/TooManyElseif'
     - 'Structures/TryFinally'
     - 'Structures/UncheckedResources'
     - 'Structures/UnconditionLoopBreak'
     - 'Structures/UnknownPregOption'
     - 'Structures/Unpreprocessed'
     - 'Structures/UnreachableCode'
     - 'Structures/UnsetInForeach'
     - 'Structures/UnsupportedOperandTypes'
     - 'Structures/UnsupportedTypesWithOperators'
     - 'Structures/UnusedGlobal'
     - 'Structures/UnusedLabel'
     - 'Structures/UseArrayFunctions'
     - 'Structures/UseCaseValue'
     - 'Structures/UseConstant'
     - 'Structures/UseCountRecursive'
     - 'Structures/UseDebug'
     - 'Structures/UseFileAppend'
     - 'Structures/UseInstanceof'
     - 'Structures/UseListWithForeach'
     - 'Structures/UsePositiveCondition'
     - 'Structures/UseSameTypesForComparisons'
     - 'Structures/UseStrEndsWith'
     - 'Structures/UseStrStartsWith'
     - 'Structures/UseSystemTmp'
     - 'Structures/UseUrlQueryFunctions'
     - 'Structures/UseVariableInsideLoop'
     - 'Structures/UselessBrackets'
     - 'Structures/UselessCasting'
     - 'Structures/UselessCheck'
     - 'Structures/UselessCoalesce'
     - 'Structures/UselessGlobal'
     - 'Structures/UselessInstruction'
     - 'Structures/UselessNullCoalesce'
     - 'Structures/UselessParenthesis'
     - 'Structures/UselessShortTernary'
     - 'Structures/UselessSwitch'
     - 'Structures/UselessTrailingComma'
     - 'Structures/UselessUnset'
     - 'Structures/VardumpUsage'
     - 'Structures/VariableGlobal'
     - 'Structures/VariableMayBeNonGlobal'
     - 'Structures/WhileListEach'
     - 'Structures/WrongLocale'
     - 'Structures/WrongPrecedenceInExpression'
     - 'Structures/WrongRange'
     - 'Structures/YodaComparison'
     - 'Structures/pregOptionE'
     - 'Structures/strOrMbFavorite'
     - 'Structures/toStringThrowsException'
     - 'Traits/AlreadyParentsTrait'
     - 'Traits/CannotCallTraitMethod'
     - 'Traits/ConstantsInTraits'
     - 'Traits/CouldUseTrait'
     - 'Traits/DependantTrait'
     - 'Traits/EmptyTrait'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/IncompatibleProperty'
     - 'Traits/IsExtTrait'
     - 'Traits/LocallyUsedProperty'
     - 'Traits/MethodCollisionTraits'
     - 'Traits/MultipleUsage'
     - 'Traits/NoPrivateAbstract'
     - 'Traits/Php'
     - 'Traits/SelfUsingTrait'
     - 'Traits/SidelinedMethod'
     - 'Traits/TraitIsNotAType'
     - 'Traits/TraitMethod'
     - 'Traits/TraitNotFound'
     - 'Traits/TraitUsage'
     - 'Traits/Traitnames'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UnusedClassTrait'
     - 'Traits/UnusedTrait'
     - 'Traits/UsedOnceTrait'
     - 'Traits/UsedTrait'
     - 'Traits/UselessAlias'
     - 'Type/ArrayIndex'
     - 'Type/Binary'
     - 'Type/CharString'
     - 'Type/Continents'
     - 'Type/DuplicateLiteral'
     - 'Type/Email'
     - 'Type/GPCIndex'
     - 'Type/Heredoc'
     - 'Type/Hexadecimal'
     - 'Type/HexadecimalString'
     - 'Type/HttpHeader'
     - 'Type/HttpStatus'
     - 'Type/IncomingDateFormat'
     - 'Type/Ip'
     - 'Type/MalformedOctal'
     - 'Type/Md5String'
     - 'Type/MimeType'
     - 'Type/NoRealComparison'
     - 'Type/Nowdoc'
     - 'Type/Octal'
     - 'Type/OctalInString'
     - 'Type/OneVariableStrings'
     - 'Type/OpensslCipher'
     - 'Type/Pack'
     - 'Type/Path'
     - 'Type/Pcre'
     - 'Type/Ports'
     - 'Type/Printf'
     - 'Type/Protocols'
     - 'Type/Regex'
     - 'Type/Sapi'
     - 'Type/Shellcommands'
     - 'Type/ShouldBeSingleQuote'
     - 'Type/ShouldTypecast'
     - 'Type/SilentlyCastInteger'
     - 'Type/SimilarIntegers'
     - 'Type/SpecialIntegers'
     - 'Type/Sql'
     - 'Type/StringHoldAVariable'
     - 'Type/StringInterpolation'
     - 'Type/StringWithStrangeSpace'
     - 'Type/UdpDomains'
     - 'Type/UnicodeBlock'
     - 'Type/Url'
     - 'Typehints/CouldBeArray'
     - 'Typehints/CouldBeBoolean'
     - 'Typehints/CouldBeCIT'
     - 'Typehints/CouldBeCallable'
     - 'Typehints/CouldBeFloat'
     - 'Typehints/CouldBeGenerator'
     - 'Typehints/CouldBeInt'
     - 'Typehints/CouldBeIterable'
     - 'Typehints/CouldBeNever'
     - 'Typehints/CouldBeNull'
     - 'Typehints/CouldBeParent'
     - 'Typehints/CouldBeResource'
     - 'Typehints/CouldBeSelf'
     - 'Typehints/CouldBeString'
     - 'Typehints/CouldBeVoid'
     - 'Typehints/CouldNotType'
     - 'Typehints/MissingReturntype'
     - 'Typehints/MissingTypehints'
     - 'Typehints/StandaloneTypeTFN'
     - 'Typehints/WrongTypeWithDefault'
     - 'Utils/Selector'
     - 'Variables/AmbiguousTypes'
     - 'Variables/AssignedTwiceOrMore'
     - 'Variables/Blind'
     - 'Variables/CloseNaming'
     - 'Variables/ComplexDynamicNames'
     - 'Variables/ConstantTypo'
     - 'Variables/Globals'
     - 'Variables/InconsistentUsage'
     - 'Variables/InheritedStaticVariable'
     - 'Variables/InterfaceArguments'
     - 'Variables/IsLocalConstant'
     - 'Variables/LocalGlobals'
     - 'Variables/LostReferences'
     - 'Variables/NoInitialS'
     - 'Variables/NoStaticVarInMethod'
     - 'Variables/NoVariableNeeded'
     - 'Variables/Overwriting'
     - 'Variables/OverwrittenLiterals'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RealVariables'
     - 'Variables/RecycledVariables'
     - 'Variables/RedeclaredStaticVariable'
     - 'Variables/References'
     - 'Variables/SelfTransform'
     - 'Variables/StaticVariableInNamespace'
     - 'Variables/StaticVariableInitialisation'
     - 'Variables/StaticVariables'
     - 'Variables/StrangeName'
     - 'Variables/UncommonEnvVar'
     - 'Variables/UndefinedConstantName'
     - 'Variables/UndefinedVariable'
     - 'Variables/UniqueUsage'
     - 'Variables/VariableLong'
     - 'Variables/VariableNonascii'
     - 'Variables/VariableOneLetter'
     - 'Variables/VariablePhp'
     - 'Variables/VariableUppercase'
     - 'Variables/VariableUsedOnce'
     - 'Variables/VariableUsedOnceByContext'
     - 'Variables/VariableVariables'
     - 'Variables/WrittenOnlyVariable'
     - 'Vendors/Cakephp'
     - 'Vendors/Codeigniter'
     - 'Vendors/Concrete5'
     - 'Vendors/Drupal'
     - 'Vendors/Feast'
     - 'Vendors/Fuel'
     - 'Vendors/Joomla'
     - 'Vendors/Laravel'
     - 'Vendors/Neos'
     - 'Vendors/Phalcon'
     - 'Vendors/Sylius'
     - 'Vendors/Symfony'
     - 'Vendors/Typo3'
     - 'Vendors/Wordpress'
     - 'Vendors/Yii'




.. _annex-analyze:

Analyze
#######


.. _annex-ini-analyze:

Analyze for INI
+++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Analyze]
   analyzer[] = "Arrays/AmbiguousKeys";
   analyzer[] = "Arrays/AppendAndAssignArrays";
   analyzer[] = "Arrays/FloatConversionAsIndex";
   analyzer[] = "Arrays/MultipleIdenticalKeys";
   analyzer[] = "Arrays/NoSpreadForHash";
   analyzer[] = "Arrays/NonConstantArray";
   analyzer[] = "Arrays/NullBoolean";
   analyzer[] = "Arrays/RandomlySortedLiterals";
   analyzer[] = "Arrays/TooManyDimensions";
   analyzer[] = "Arrays/WeakType";
   analyzer[] = "Attributes/MissingAttributeAttribute";
   analyzer[] = "Attributes/ModifyImmutable";
   analyzer[] = "Attributes/UselessOverride";
   analyzer[] = "Classes/AbstractOrImplements";
   analyzer[] = "Classes/AbstractStatic";
   analyzer[] = "Classes/AccessPrivate";
   analyzer[] = "Classes/AccessProtected";
   analyzer[] = "Classes/AmbiguousStatic";
   analyzer[] = "Classes/AmbiguousVisibilities";
   analyzer[] = "Classes/AvoidOptionArrays";
   analyzer[] = "Classes/AvoidOptionalProperties";
   analyzer[] = "Classes/CantExtendFinal";
   analyzer[] = "Classes/CantInstantiateClass";
   analyzer[] = "Classes/CantInstantiateNonClass";
   analyzer[] = "Classes/CantOverwriteFinalConstant";
   analyzer[] = "Classes/CheckAfterNullSafeOperator";
   analyzer[] = "Classes/CheckOnCallUsage";
   analyzer[] = "Classes/CitSameName";
   analyzer[] = "Classes/CloneWithNonObject";
   analyzer[] = "Classes/CouldBeAbstractClass";
   analyzer[] = "Classes/CouldBeFinal";
   analyzer[] = "Classes/CouldBeStatic";
   analyzer[] = "Classes/CouldInjectParam";
   analyzer[] = "Classes/CyclicReferences";
   analyzer[] = "Classes/DependantAbstractClass";
   analyzer[] = "Classes/DifferentArgumentCounts";
   analyzer[] = "Classes/DirectCallToMagicMethod";
   analyzer[] = "Classes/DontSendThisInConstructor";
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/EmptyClass";
   analyzer[] = "Classes/HiddenNullable";
   analyzer[] = "Classes/ImplementIsForInterface";
   analyzer[] = "Classes/ImplementedMethodsArePublic";
   analyzer[] = "Classes/IncompatibleSignature";
   analyzer[] = "Classes/IncompatibleSignature74";
   analyzer[] = "Classes/InheritedPropertyMustMatch";
   analyzer[] = "Classes/InstantiatingAbstractClass";
   analyzer[] = "Classes/MakeDefault";
   analyzer[] = "Classes/MakeGlobalAProperty";
   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
   analyzer[] = "Classes/MismatchProperties";
   analyzer[] = "Classes/MissingAbstractMethod";
   analyzer[] = "Classes/MultipleDeclarations";
   analyzer[] = "Classes/MultipleTraitOrInterface";
   analyzer[] = "Classes/NewThenCall";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoNullWithNullSafeOperator";
   analyzer[] = "Classes/NoPSSOutsideClass";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NoPublicAccess";
   analyzer[] = "Classes/NoReadonlyAssignationInGlobal";
   analyzer[] = "Classes/NoSelfReferencingConstant";
   analyzer[] = "Classes/NonNullableSetters";
   analyzer[] = "Classes/NonPpp";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/OldStyleVar";
   analyzer[] = "Classes/ParentFirst";
   analyzer[] = "Classes/ParentIsNotStatic";
   analyzer[] = "Classes/PropertyCouldBeLocal";
   analyzer[] = "Classes/PropertyMethodSameName";
   analyzer[] = "Classes/PropertyNeverUsed";
   analyzer[] = "Classes/PropertyUsedInOneMethodOnly";
   analyzer[] = "Classes/PssWithoutClass";
   analyzer[] = "Classes/ScalarOrObjectProperty";
   analyzer[] = "Classes/ShouldUseSelf";
   analyzer[] = "Classes/ShouldUseThis";
   analyzer[] = "Classes/StaticCannotCallNonStatic";
   analyzer[] = "Classes/StaticContainsThis";
   analyzer[] = "Classes/StaticMethodsCalledFromObject";
   analyzer[] = "Classes/SwappedArguments";
   analyzer[] = "Classes/ThisIsForClasses";
   analyzer[] = "Classes/ThisIsNotAnArray";
   analyzer[] = "Classes/ThisIsNotForStatic";
   analyzer[] = "Classes/ThrowInDestruct";
   analyzer[] = "Classes/TooManyDereferencing";
   analyzer[] = "Classes/TooManyFinds";
   analyzer[] = "Classes/TooManyInjections";
   analyzer[] = "Classes/UndeclaredStaticProperty";
   analyzer[] = "Classes/UndefinedClasses";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UndefinedParentMP";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Classes/UndefinedStaticMP";
   analyzer[] = "Classes/UndefinedStaticclass";
   analyzer[] = "Classes/UnfinishedObject";
   analyzer[] = "Classes/UnreachableMethod";
   analyzer[] = "Classes/UnresolvedClasses";
   analyzer[] = "Classes/UnresolvedInstanceof";
   analyzer[] = "Classes/UnusedClass";
   analyzer[] = "Classes/UnusedConstant";
   analyzer[] = "Classes/UnusedPublicMethod";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Classes/UseInstanceof";
   analyzer[] = "Classes/UsedOnceProperty";
   analyzer[] = "Classes/UselessAbstract";
   analyzer[] = "Classes/UselessAssignationOfPromotedProperty";
   analyzer[] = "Classes/UselessConstructor";
   analyzer[] = "Classes/UselessFinal";
   analyzer[] = "Classes/UselessMethod";
   analyzer[] = "Classes/UsingThisOutsideAClass";
   analyzer[] = "Classes/WeakType";
   analyzer[] = "Classes/WrongName";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Constants/BadConstantnames";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Constants/ConstantUsedOnce";
   analyzer[] = "Constants/CreatedOutsideItsNamespace";
   analyzer[] = "Constants/InvalidName";
   analyzer[] = "Constants/MultipleConstantDefinition";
   analyzer[] = "Constants/StrangeName";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Enums/DuplicateCaseValue";
   analyzer[] = "Enums/NoMagicMethod";
   analyzer[] = "Enums/UndefinedEnumcase";
   analyzer[] = "Enums/UnusedEnumCase";
   analyzer[] = "Exceptions/CantThrow";
   analyzer[] = "Exceptions/CatchUndefinedVariable";
   analyzer[] = "Exceptions/ConvertedExceptions";
   analyzer[] = "Exceptions/ForgottenThrown";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/ThrowFunctioncall";
   analyzer[] = "Exceptions/ThrowRawExceptions";
   analyzer[] = "Exceptions/UncaughtExceptions";
   analyzer[] = "Exceptions/Unthrown";
   analyzer[] = "Exceptions/UselessTry";
   analyzer[] = "Files/MissingInclude";
   analyzer[] = "Functions/AliasesUsage";
   analyzer[] = "Functions/AvoidBooleanArgument";
   analyzer[] = "Functions/CallbackNeedsReturn";
   analyzer[] = "Functions/CanCallGenerator";
   analyzer[] = "Functions/CancelledParameter";
   analyzer[] = "Functions/CannotUseStaticForClosure";
   analyzer[] = "Functions/CouldCentralize";
   analyzer[] = "Functions/DeepDefinitions";
   analyzer[] = "Functions/DontUseVoid";
   analyzer[] = "Functions/DuplicateNamedParameter";
   analyzer[] = "Functions/EmptyFunction";
   analyzer[] = "Functions/FnArgumentVariableConfusion";
   analyzer[] = "Functions/HardcodedPasswords";
   analyzer[] = "Functions/InsufficientTypehint";
   analyzer[] = "Functions/MethodIsNotAnIf";
   analyzer[] = "Functions/MismatchParameterName";
   analyzer[] = "Functions/MismatchTypeAndDefault";
   analyzer[] = "Functions/MismatchedDefaultArguments";
   analyzer[] = "Functions/MismatchedTypehint";
   analyzer[] = "Functions/ModifyTypedParameter";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/NeverUsedParameter";
   analyzer[] = "Functions/NoBooleanAsDefault";
   analyzer[] = "Functions/NoDefaultForReference";
   analyzer[] = "Functions/NoLiteralForReference";
   analyzer[] = "Functions/NoReferencedVoid";
   analyzer[] = "Functions/NoReturnUsed";
   analyzer[] = "Functions/OnlyVariableForReference";
   analyzer[] = "Functions/OnlyVariablePassedByReference";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/RetypedReference";
   analyzer[] = "Functions/ShouldUseConstants";
   analyzer[] = "Functions/ShouldYieldWithKey";
   analyzer[] = "Functions/TooManyLocalVariables";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/TypehintedReferences";
   analyzer[] = "Functions/UndefinedFunctions";
   analyzer[] = "Functions/UnknownParameterName";
   analyzer[] = "Functions/UnusedArguments";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UnusedReturnedValue";
   analyzer[] = "Functions/UseConstantAsArguments";
   analyzer[] = "Functions/UseConstantsAsReturns";
   analyzer[] = "Functions/UselessArgument";
   analyzer[] = "Functions/UselessReferenceArgument";
   analyzer[] = "Functions/UselessReturn";
   analyzer[] = "Functions/UsesDefaultArguments";
   analyzer[] = "Functions/UsingDeprecated";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Functions/WithoutReturn";
   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
   analyzer[] = "Functions/WrongArgumentType";
   analyzer[] = "Functions/WrongNumberOfArguments";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Functions/funcGetArgModified";
   analyzer[] = "Interfaces/AlreadyParentsInterface";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/CouldUseInterface";
   analyzer[] = "Interfaces/EmptyInterface";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
   analyzer[] = "Interfaces/RepeatedInterface";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Interfaces/UselessInterfaces";
   analyzer[] = "Namespaces/ConstantFullyQualified";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/HiddenUse";
   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
   analyzer[] = "Namespaces/MultipleAliasDefinitions";
   analyzer[] = "Namespaces/OverloadExistingNames";
   analyzer[] = "Namespaces/ShouldMakeAlias";
   analyzer[] = "Namespaces/UnresolvedUse";
   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/LogicalToInArray";
   analyzer[] = "Performances/MemoizeMagicCall";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/StrposTooMuch";
   analyzer[] = "Performances/UseArraySlice";
   analyzer[] = "Php/ArrayKeyExistsWithObjects";
   analyzer[] = "Php/AssertFunctionIsReserved";
   analyzer[] = "Php/AssignAnd";
   analyzer[] = "Php/Assumptions";
   analyzer[] = "Php/AvoidMbDectectEncoding";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/Crc32MightBeNegative";
   analyzer[] = "Php/DateTimeNotImmutable";
   analyzer[] = "Php/Deprecated";
   analyzer[] = "Php/DontPolluteGlobalSpace";
   analyzer[] = "Php/EmptyList";
   analyzer[] = "Php/ExitNoArg";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/FopenMode";
   analyzer[] = "Php/ForeachObject";
   analyzer[] = "Php/HasPropertyHook";
   analyzer[] = "Php/HashAlgos";
   analyzer[] = "Php/Incompilable";
   analyzer[] = "Php/InternalParameterType";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/MissingMagicIsset";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Php/MultipleDeclareStrict";
   analyzer[] = "Php/MustCallParentConstructor";
   analyzer[] = "Php/NativeClassTypeCompatibility";
   analyzer[] = "Php/NeverKeyword";
   analyzer[] = "Php/NoCastToInt";
   analyzer[] = "Php/NoClassInGlobal";
   analyzer[] = "Php/NoNullForNative";
   analyzer[] = "Php/NoReferenceForTernary";
   analyzer[] = "Php/OnlyVariablePassedByReference";
   analyzer[] = "Php/PathinfoReturns";
   analyzer[] = "Php/Php81NewFunctions";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/ShortOpenTagRequired";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/StrposWithIntegers";
   analyzer[] = "Php/StrtrArguments";
   analyzer[] = "Php/TooManyNativeCalls";
   analyzer[] = "Php/UnknownPcre2Option";
   analyzer[] = "Php/UseObjectApi";
   analyzer[] = "Php/UsePathinfo";
   analyzer[] = "Php/UseSetCookie";
   analyzer[] = "Php/UseStdclass";
   analyzer[] = "Php/VersionCompareOperator";
   analyzer[] = "Php/WrongAttributeConfiguration";
   analyzer[] = "Php/WrongTypeForNativeFunction";
   analyzer[] = "Php/oldAutoloadUsage";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Structures/AddZero";
   analyzer[] = "Structures/AlteringForeachWithoutReference";
   analyzer[] = "Structures/AlternativeConsistenceByFile";
   analyzer[] = "Structures/AlwaysFalse";
   analyzer[] = "Structures/ArrayAccessOnLiteralArray";
   analyzer[] = "Structures/ArrayFillWithObjects";
   analyzer[] = "Structures/ArrayMapPassesByValue";
   analyzer[] = "Structures/ArrayMergeAndVariadic";
   analyzer[] = "Structures/ArrayMergeArrayArray";
   analyzer[] = "Structures/AssigneAndCompare";
   analyzer[] = "Structures/AutoUnsetForeach";
   analyzer[] = "Structures/BailOutEarly";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/BreakOutsideLoop";
   analyzer[] = "Structures/BuriedAssignation";
   analyzer[] = "Structures/CannotUseAppendForReading";
   analyzer[] = "Structures/CastToBoolean";
   analyzer[] = "Structures/CastingTernary";
   analyzer[] = "Structures/CatchShadowsVariable";
   analyzer[] = "Structures/CheckAllTypes";
   analyzer[] = "Structures/CheckDivision";
   analyzer[] = "Structures/CheckJson";
   analyzer[] = "Structures/CoalesceAndConcat";
   analyzer[] = "Structures/CoalesceNullCoalesce";
   analyzer[] = "Structures/CommonAlternatives";
   analyzer[] = "Structures/ComparedComparison";
   analyzer[] = "Structures/ConcatEmpty";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/CouldBeElse";
   analyzer[] = "Structures/CouldBeSpaceship";
   analyzer[] = "Structures/CouldBeStatic";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/CouldUseYieldFrom";
   analyzer[] = "Structures/CountIsNotNegative";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/DefaultThenDiscard";
   analyzer[] = "Structures/DirThenSlash";
   analyzer[] = "Structures/DontAddSeconds";
   analyzer[] = "Structures/DontChangeBlindKey";
   analyzer[] = "Structures/DontMixPlusPlus";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Structures/DontReuseForeachSource";
   analyzer[] = "Structures/DoubleAssignation";
   analyzer[] = "Structures/DoubleChecks";
   analyzer[] = "Structures/DoubleInstruction";
   analyzer[] = "Structures/DoubleObjectAssignation";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/EchoWithConcat";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/EmptyBlocks";
   analyzer[] = "Structures/EmptyJsonError";
   analyzer[] = "Structures/EmptyLines";
   analyzer[] = "Structures/EmptyLoop";
   analyzer[] = "Structures/EmptyTryCatch";
   analyzer[] = "Structures/ErrorReportingWithInteger";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/ForeachOnObject";
   analyzer[] = "Structures/ForeachReferenceIsNotModified";
   analyzer[] = "Structures/ForeachSourceValue";
   analyzer[] = "Structures/ForgottenWhiteSpace";
   analyzer[] = "Structures/GlobalUsage";
   analyzer[] = "Structures/Htmlentitiescall";
   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
   analyzer[] = "Structures/IdenticalCase";
   analyzer[] = "Structures/IdenticalConditions";
   analyzer[] = "Structures/IdenticalConsecutive";
   analyzer[] = "Structures/IdenticalOnBothSides";
   analyzer[] = "Structures/IdenticalVariablesInForeach";
   analyzer[] = "Structures/IfWithSameConditions";
   analyzer[] = "Structures/Iffectation";
   analyzer[] = "Structures/ImplicitConversionToInt";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/ImplodeArgsOrder";
   analyzer[] = "Structures/IndicesAreIntOrString";
   analyzer[] = "Structures/InfiniteRecursion";
   analyzer[] = "Structures/InvalidCast";
   analyzer[] = "Structures/InvalidDateScanningFormat";
   analyzer[] = "Structures/InvalidPackFormat";
   analyzer[] = "Structures/InvalidRegex";
   analyzer[] = "Structures/IsZero";
   analyzer[] = "Structures/ListOmissions";
   analyzer[] = "Structures/LogicalMistakes";
   analyzer[] = "Structures/LoneBlock";
   analyzer[] = "Structures/LongArguments";
   analyzer[] = "Structures/MaxLevelOfIdentation";
   analyzer[] = "Structures/MbStringNonEncodings";
   analyzer[] = "Structures/MbstringThirdArg";
   analyzer[] = "Structures/MbstringUnknownEncoding";
   analyzer[] = "Structures/MergeIfThen";
   analyzer[] = "Structures/MergeTernaryIntoIfthen";
   analyzer[] = "Structures/MismatchedTernary";
   analyzer[] = "Structures/MissingAssignation";
   analyzer[] = "Structures/MissingCases";
   analyzer[] = "Structures/MissingNew";
   analyzer[] = "Structures/MissingParenthesis";
   analyzer[] = "Structures/MisusedYield";
   analyzer[] = "Structures/MixedConcatInterpolation";
   analyzer[] = "Structures/ModernEmpty";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultipleTypeVariable";
   analyzer[] = "Structures/MultiplyByOne";
   analyzer[] = "Structures/NegativePow";
   analyzer[] = "Structures/NestedIfthen";
   analyzer[] = "Structures/NestedMatch";
   analyzer[] = "Structures/NestedTernary";
   analyzer[] = "Structures/NeverNegative";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoAppendOnSource";
   analyzer[] = "Structures/NoChangeIncomingVariables";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoDirectUsage";
   analyzer[] = "Structures/NoEmptyRegex";
   analyzer[] = "Structures/NoEmptyStringWithExplode";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/NoHardcodedHash";
   analyzer[] = "Structures/NoHardcodedIp";
   analyzer[] = "Structures/NoHardcodedPath";
   analyzer[] = "Structures/NoHardcodedPort";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/NoNeedForElse";
   analyzer[] = "Structures/NoNeedForTriple";
   analyzer[] = "Structures/NoNullForIndex";
   analyzer[] = "Structures/NoObjectAsIndex";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoReferenceOnLeft";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/NoValidCast";
   analyzer[] = "Structures/NoVariableIsACondition";
   analyzer[] = "Structures/NonIntStringAsIndex";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/NotEqual";
   analyzer[] = "Structures/NotNot";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/OnceUsage";
   analyzer[] = "Structures/OneLineTwoInstructions";
   analyzer[] = "Structures/OnlyFirstByte";
   analyzer[] = "Structures/OnlyVariableReturnedByReference";
   analyzer[] = "Structures/OrDie";
   analyzer[] = "Structures/OverwrittenForeachVar";
   analyzer[] = "Structures/PossibleInfiniteLoop";
   analyzer[] = "Structures/PrintAndDie";
   analyzer[] = "Structures/PrintWithoutParenthesis";
   analyzer[] = "Structures/PrintfArguments";
   analyzer[] = "Structures/QueriesInLoop";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/RepeatedRegex";
   analyzer[] = "Structures/ResultMayBeMissing";
   analyzer[] = "Structures/ReturnTrueFalse";
   analyzer[] = "Structures/SameConditions";
   analyzer[] = "Structures/ShouldChainException";
   analyzer[] = "Structures/ShouldMakeTernary";
   analyzer[] = "Structures/ShouldPreprocess";
   analyzer[] = "Structures/ShouldUseExplodeArgs";
   analyzer[] = "Structures/SprintfFormatCompilation";
   analyzer[] = "Structures/StaticInclude";
   analyzer[] = "Structures/StaticLoop";
   analyzer[] = "Structures/StripTagsSkipsClosedTag";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/StrposLessThanOne";
   analyzer[] = "Structures/SuspiciousComparison";
   analyzer[] = "Structures/SwitchToSwitch";
   analyzer[] = "Structures/SwitchWithoutDefault";
   analyzer[] = "Structures/TernaryInConcat";
   analyzer[] = "Structures/TestThenCast";
   analyzer[] = "Structures/ThrowsAndAssign";
   analyzer[] = "Structures/TimestampDifference";
   analyzer[] = "Structures/UncheckedResources";
   analyzer[] = "Structures/UnconditionLoopBreak";
   analyzer[] = "Structures/UnknownPregOption";
   analyzer[] = "Structures/Unpreprocessed";
   analyzer[] = "Structures/UnsetInForeach";
   analyzer[] = "Structures/UnsupportedOperandTypes";
   analyzer[] = "Structures/UnsupportedTypesWithOperators";
   analyzer[] = "Structures/UnusedGlobal";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UseInstanceof";
   analyzer[] = "Structures/UsePositiveCondition";
   analyzer[] = "Structures/UseSameTypesForComparisons";
   analyzer[] = "Structures/UseSystemTmp";
   analyzer[] = "Structures/UselessBrackets";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Structures/UselessCheck";
   analyzer[] = "Structures/UselessCoalesce";
   analyzer[] = "Structures/UselessGlobal";
   analyzer[] = "Structures/UselessInstruction";
   analyzer[] = "Structures/UselessNullCoalesce";
   analyzer[] = "Structures/UselessParenthesis";
   analyzer[] = "Structures/UselessShortTernary";
   analyzer[] = "Structures/UselessSwitch";
   analyzer[] = "Structures/UselessUnset";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Structures/WrongLocale";
   analyzer[] = "Structures/WrongPrecedenceInExpression";
   analyzer[] = "Structures/WrongRange";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Structures/toStringThrowsException";
   analyzer[] = "Traits/AlreadyParentsTrait";
   analyzer[] = "Traits/CannotCallTraitMethod";
   analyzer[] = "Traits/DependantTrait";
   analyzer[] = "Traits/EmptyTrait";
   analyzer[] = "Traits/MethodCollisionTraits";
   analyzer[] = "Traits/TraitIsNotAType";
   analyzer[] = "Traits/TraitNotFound";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Type/OneVariableStrings";
   analyzer[] = "Type/ShouldTypecast";
   analyzer[] = "Type/SilentlyCastInteger";
   analyzer[] = "Type/StringHoldAVariable";
   analyzer[] = "Type/StringWithStrangeSpace";
   analyzer[] = "Typehints/MissingReturntype";
   analyzer[] = "Typehints/StandaloneTypeTFN";
   analyzer[] = "Typehints/WrongTypeWithDefault";
   analyzer[] = "Variables/AssignedTwiceOrMore";
   analyzer[] = "Variables/ConstantTypo";
   analyzer[] = "Variables/LostReferences";
   analyzer[] = "Variables/OverwrittenLiterals";
   analyzer[] = "Variables/RecycledVariables";
   analyzer[] = "Variables/UndefinedConstantName";
   analyzer[] = "Variables/UndefinedVariable";
   analyzer[] = "Variables/VariableNonascii";
   analyzer[] = "Variables/VariableUsedOnce";
   analyzer[] = "Variables/VariableUsedOnceByContext";
   analyzer[] = "Variables/WrittenOnlyVariable";


.. _annex-yaml-analyze:

Analyze for .exakat.yaml
++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Analyze':
     - 'Arrays/AmbiguousKeys'
     - 'Arrays/AppendAndAssignArrays'
     - 'Arrays/FloatConversionAsIndex'
     - 'Arrays/MultipleIdenticalKeys'
     - 'Arrays/NoSpreadForHash'
     - 'Arrays/NonConstantArray'
     - 'Arrays/NullBoolean'
     - 'Arrays/RandomlySortedLiterals'
     - 'Arrays/TooManyDimensions'
     - 'Arrays/WeakType'
     - 'Attributes/MissingAttributeAttribute'
     - 'Attributes/ModifyImmutable'
     - 'Attributes/UselessOverride'
     - 'Classes/AbstractOrImplements'
     - 'Classes/AbstractStatic'
     - 'Classes/AccessPrivate'
     - 'Classes/AccessProtected'
     - 'Classes/AmbiguousStatic'
     - 'Classes/AmbiguousVisibilities'
     - 'Classes/AvoidOptionArrays'
     - 'Classes/AvoidOptionalProperties'
     - 'Classes/CantExtendFinal'
     - 'Classes/CantInstantiateClass'
     - 'Classes/CantInstantiateNonClass'
     - 'Classes/CantOverwriteFinalConstant'
     - 'Classes/CheckAfterNullSafeOperator'
     - 'Classes/CheckOnCallUsage'
     - 'Classes/CitSameName'
     - 'Classes/CloneWithNonObject'
     - 'Classes/CouldBeAbstractClass'
     - 'Classes/CouldBeFinal'
     - 'Classes/CouldBeStatic'
     - 'Classes/CouldInjectParam'
     - 'Classes/CyclicReferences'
     - 'Classes/DependantAbstractClass'
     - 'Classes/DifferentArgumentCounts'
     - 'Classes/DirectCallToMagicMethod'
     - 'Classes/DontSendThisInConstructor'
     - 'Classes/DontUnsetProperties'
     - 'Classes/EmptyClass'
     - 'Classes/HiddenNullable'
     - 'Classes/ImplementIsForInterface'
     - 'Classes/ImplementedMethodsArePublic'
     - 'Classes/IncompatibleSignature'
     - 'Classes/IncompatibleSignature74'
     - 'Classes/InheritedPropertyMustMatch'
     - 'Classes/InstantiatingAbstractClass'
     - 'Classes/MakeDefault'
     - 'Classes/MakeGlobalAProperty'
     - 'Classes/MethodSignatureMustBeCompatible'
     - 'Classes/MismatchProperties'
     - 'Classes/MissingAbstractMethod'
     - 'Classes/MultipleDeclarations'
     - 'Classes/MultipleTraitOrInterface'
     - 'Classes/NewThenCall'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoNullWithNullSafeOperator'
     - 'Classes/NoPSSOutsideClass'
     - 'Classes/NoParent'
     - 'Classes/NoPublicAccess'
     - 'Classes/NoReadonlyAssignationInGlobal'
     - 'Classes/NoSelfReferencingConstant'
     - 'Classes/NonNullableSetters'
     - 'Classes/NonPpp'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/OldStyleConstructor'
     - 'Classes/OldStyleVar'
     - 'Classes/ParentFirst'
     - 'Classes/ParentIsNotStatic'
     - 'Classes/PropertyCouldBeLocal'
     - 'Classes/PropertyMethodSameName'
     - 'Classes/PropertyNeverUsed'
     - 'Classes/PropertyUsedInOneMethodOnly'
     - 'Classes/PssWithoutClass'
     - 'Classes/ScalarOrObjectProperty'
     - 'Classes/ShouldUseSelf'
     - 'Classes/ShouldUseThis'
     - 'Classes/StaticCannotCallNonStatic'
     - 'Classes/StaticContainsThis'
     - 'Classes/StaticMethodsCalledFromObject'
     - 'Classes/SwappedArguments'
     - 'Classes/ThisIsForClasses'
     - 'Classes/ThisIsNotAnArray'
     - 'Classes/ThisIsNotForStatic'
     - 'Classes/ThrowInDestruct'
     - 'Classes/TooManyDereferencing'
     - 'Classes/TooManyFinds'
     - 'Classes/TooManyInjections'
     - 'Classes/UndeclaredStaticProperty'
     - 'Classes/UndefinedClasses'
     - 'Classes/UndefinedConstants'
     - 'Classes/UndefinedParentMP'
     - 'Classes/UndefinedProperty'
     - 'Classes/UndefinedStaticMP'
     - 'Classes/UndefinedStaticclass'
     - 'Classes/UnfinishedObject'
     - 'Classes/UnreachableMethod'
     - 'Classes/UnresolvedClasses'
     - 'Classes/UnresolvedInstanceof'
     - 'Classes/UnusedClass'
     - 'Classes/UnusedConstant'
     - 'Classes/UnusedPublicMethod'
     - 'Classes/UseClassOperator'
     - 'Classes/UseInstanceof'
     - 'Classes/UsedOnceProperty'
     - 'Classes/UselessAbstract'
     - 'Classes/UselessAssignationOfPromotedProperty'
     - 'Classes/UselessConstructor'
     - 'Classes/UselessFinal'
     - 'Classes/UselessMethod'
     - 'Classes/UsingThisOutsideAClass'
     - 'Classes/WeakType'
     - 'Classes/WrongName'
     - 'Classes/WrongTypedPropertyInit'
     - 'Constants/BadConstantnames'
     - 'Constants/ConstRecommended'
     - 'Constants/ConstantUsedOnce'
     - 'Constants/CreatedOutsideItsNamespace'
     - 'Constants/InvalidName'
     - 'Constants/MultipleConstantDefinition'
     - 'Constants/StrangeName'
     - 'Constants/UndefinedConstants'
     - 'Enums/DuplicateCaseValue'
     - 'Enums/NoMagicMethod'
     - 'Enums/UndefinedEnumcase'
     - 'Enums/UnusedEnumCase'
     - 'Exceptions/CantThrow'
     - 'Exceptions/CatchUndefinedVariable'
     - 'Exceptions/ConvertedExceptions'
     - 'Exceptions/ForgottenThrown'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/ThrowFunctioncall'
     - 'Exceptions/ThrowRawExceptions'
     - 'Exceptions/UncaughtExceptions'
     - 'Exceptions/Unthrown'
     - 'Exceptions/UselessTry'
     - 'Files/MissingInclude'
     - 'Functions/AliasesUsage'
     - 'Functions/AvoidBooleanArgument'
     - 'Functions/CallbackNeedsReturn'
     - 'Functions/CanCallGenerator'
     - 'Functions/CancelledParameter'
     - 'Functions/CannotUseStaticForClosure'
     - 'Functions/CouldCentralize'
     - 'Functions/DeepDefinitions'
     - 'Functions/DontUseVoid'
     - 'Functions/DuplicateNamedParameter'
     - 'Functions/EmptyFunction'
     - 'Functions/FnArgumentVariableConfusion'
     - 'Functions/HardcodedPasswords'
     - 'Functions/InsufficientTypehint'
     - 'Functions/MethodIsNotAnIf'
     - 'Functions/MismatchParameterName'
     - 'Functions/MismatchTypeAndDefault'
     - 'Functions/MismatchedDefaultArguments'
     - 'Functions/MismatchedTypehint'
     - 'Functions/ModifyTypedParameter'
     - 'Functions/MustReturn'
     - 'Functions/NeverUsedParameter'
     - 'Functions/NoBooleanAsDefault'
     - 'Functions/NoDefaultForReference'
     - 'Functions/NoLiteralForReference'
     - 'Functions/NoReferencedVoid'
     - 'Functions/NoReturnUsed'
     - 'Functions/OnlyVariableForReference'
     - 'Functions/OnlyVariablePassedByReference'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/RetypedReference'
     - 'Functions/ShouldUseConstants'
     - 'Functions/ShouldYieldWithKey'
     - 'Functions/TooManyLocalVariables'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/TypehintedReferences'
     - 'Functions/UndefinedFunctions'
     - 'Functions/UnknownParameterName'
     - 'Functions/UnusedArguments'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UnusedReturnedValue'
     - 'Functions/UseConstantAsArguments'
     - 'Functions/UseConstantsAsReturns'
     - 'Functions/UselessArgument'
     - 'Functions/UselessReferenceArgument'
     - 'Functions/UselessReturn'
     - 'Functions/UsesDefaultArguments'
     - 'Functions/UsingDeprecated'
     - 'Functions/VoidIsNotAReference'
     - 'Functions/WithoutReturn'
     - 'Functions/WrongArgumentNameWithPhpFunction'
     - 'Functions/WrongArgumentType'
     - 'Functions/WrongNumberOfArguments'
     - 'Functions/WrongOptionalParameter'
     - 'Functions/WrongReturnedType'
     - 'Functions/WrongTypeWithCall'
     - 'Functions/funcGetArgModified'
     - 'Interfaces/AlreadyParentsInterface'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/CouldUseInterface'
     - 'Interfaces/EmptyInterface'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/NoGaranteeForPropertyConstant'
     - 'Interfaces/RepeatedInterface'
     - 'Interfaces/UndefinedInterfaces'
     - 'Interfaces/UselessInterfaces'
     - 'Namespaces/ConstantFullyQualified'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/HiddenUse'
     - 'Namespaces/MultipleAliasDefinitionPerFile'
     - 'Namespaces/MultipleAliasDefinitions'
     - 'Namespaces/OverloadExistingNames'
     - 'Namespaces/ShouldMakeAlias'
     - 'Namespaces/UnresolvedUse'
     - 'Namespaces/UseWithFullyQualifiedNS'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/LogicalToInArray'
     - 'Performances/MemoizeMagicCall'
     - 'Performances/PrePostIncrement'
     - 'Performances/StrposTooMuch'
     - 'Performances/UseArraySlice'
     - 'Php/ArrayKeyExistsWithObjects'
     - 'Php/AssertFunctionIsReserved'
     - 'Php/AssignAnd'
     - 'Php/Assumptions'
     - 'Php/AvoidMbDectectEncoding'
     - 'Php/BetterRand'
     - 'Php/CloneConstant'
     - 'Php/ConcatAndAddition'
     - 'Php/Crc32MightBeNegative'
     - 'Php/DateTimeNotImmutable'
     - 'Php/Deprecated'
     - 'Php/DontPolluteGlobalSpace'
     - 'Php/EmptyList'
     - 'Php/ExitNoArg'
     - 'Php/FalseToArray'
     - 'Php/FopenMode'
     - 'Php/ForeachObject'
     - 'Php/HasPropertyHook'
     - 'Php/HashAlgos'
     - 'Php/Incompilable'
     - 'Php/InternalParameterType'
     - 'Php/IsAWithString'
     - 'Php/IsnullVsEqualNull'
     - 'Php/JsonSerializeReturnType'
     - 'Php/LogicalInLetters'
     - 'Php/MissingMagicIsset'
     - 'Php/MissingSubpattern'
     - 'Php/MultipleDeclareStrict'
     - 'Php/MustCallParentConstructor'
     - 'Php/NativeClassTypeCompatibility'
     - 'Php/NeverKeyword'
     - 'Php/NoCastToInt'
     - 'Php/NoClassInGlobal'
     - 'Php/NoNullForNative'
     - 'Php/NoReferenceForTernary'
     - 'Php/OnlyVariablePassedByReference'
     - 'Php/PathinfoReturns'
     - 'Php/Php81NewFunctions'
     - 'Php/ScalarAreNotArrays'
     - 'Php/ShortOpenTagRequired'
     - 'Php/ShouldUseCoalesce'
     - 'Php/StrposWithIntegers'
     - 'Php/StrtrArguments'
     - 'Php/TooManyNativeCalls'
     - 'Php/UnknownPcre2Option'
     - 'Php/UseObjectApi'
     - 'Php/UsePathinfo'
     - 'Php/UseSetCookie'
     - 'Php/UseStdclass'
     - 'Php/VersionCompareOperator'
     - 'Php/WrongAttributeConfiguration'
     - 'Php/WrongTypeForNativeFunction'
     - 'Php/oldAutoloadUsage'
     - 'Security/DontEchoError'
     - 'Security/ShouldUsePreparedStatement'
     - 'Structures/AddZero'
     - 'Structures/AlteringForeachWithoutReference'
     - 'Structures/AlternativeConsistenceByFile'
     - 'Structures/AlwaysFalse'
     - 'Structures/ArrayAccessOnLiteralArray'
     - 'Structures/ArrayFillWithObjects'
     - 'Structures/ArrayMapPassesByValue'
     - 'Structures/ArrayMergeAndVariadic'
     - 'Structures/ArrayMergeArrayArray'
     - 'Structures/AssigneAndCompare'
     - 'Structures/AutoUnsetForeach'
     - 'Structures/BailOutEarly'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/BreakOutsideLoop'
     - 'Structures/BuriedAssignation'
     - 'Structures/CannotUseAppendForReading'
     - 'Structures/CastToBoolean'
     - 'Structures/CastingTernary'
     - 'Structures/CatchShadowsVariable'
     - 'Structures/CheckAllTypes'
     - 'Structures/CheckDivision'
     - 'Structures/CheckJson'
     - 'Structures/CoalesceAndConcat'
     - 'Structures/CoalesceNullCoalesce'
     - 'Structures/CommonAlternatives'
     - 'Structures/ComparedComparison'
     - 'Structures/ConcatEmpty'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/CouldBeElse'
     - 'Structures/CouldBeSpaceship'
     - 'Structures/CouldBeStatic'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/CouldUseYieldFrom'
     - 'Structures/CountIsNotNegative'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/DefaultThenDiscard'
     - 'Structures/DirThenSlash'
     - 'Structures/DontAddSeconds'
     - 'Structures/DontChangeBlindKey'
     - 'Structures/DontMixPlusPlus'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Structures/DontReuseForeachSource'
     - 'Structures/DoubleAssignation'
     - 'Structures/DoubleChecks'
     - 'Structures/DoubleInstruction'
     - 'Structures/DoubleObjectAssignation'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/EchoWithConcat'
     - 'Structures/ElseIfElseif'
     - 'Structures/EmptyBlocks'
     - 'Structures/EmptyJsonError'
     - 'Structures/EmptyLines'
     - 'Structures/EmptyLoop'
     - 'Structures/EmptyTryCatch'
     - 'Structures/ErrorReportingWithInteger'
     - 'Structures/EvalUsage'
     - 'Structures/EvalWithoutTry'
     - 'Structures/ExitUsage'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/ForeachOnObject'
     - 'Structures/ForeachReferenceIsNotModified'
     - 'Structures/ForeachSourceValue'
     - 'Structures/ForgottenWhiteSpace'
     - 'Structures/GlobalUsage'
     - 'Structures/Htmlentitiescall'
     - 'Structures/HtmlentitiescallDefaultFlag'
     - 'Structures/IdenticalCase'
     - 'Structures/IdenticalConditions'
     - 'Structures/IdenticalConsecutive'
     - 'Structures/IdenticalOnBothSides'
     - 'Structures/IdenticalVariablesInForeach'
     - 'Structures/IfWithSameConditions'
     - 'Structures/Iffectation'
     - 'Structures/ImplicitConversionToInt'
     - 'Structures/ImpliedIf'
     - 'Structures/ImplodeArgsOrder'
     - 'Structures/IndicesAreIntOrString'
     - 'Structures/InfiniteRecursion'
     - 'Structures/InvalidCast'
     - 'Structures/InvalidDateScanningFormat'
     - 'Structures/InvalidPackFormat'
     - 'Structures/InvalidRegex'
     - 'Structures/IsZero'
     - 'Structures/ListOmissions'
     - 'Structures/LogicalMistakes'
     - 'Structures/LoneBlock'
     - 'Structures/LongArguments'
     - 'Structures/MaxLevelOfIdentation'
     - 'Structures/MbStringNonEncodings'
     - 'Structures/MbstringThirdArg'
     - 'Structures/MbstringUnknownEncoding'
     - 'Structures/MergeIfThen'
     - 'Structures/MergeTernaryIntoIfthen'
     - 'Structures/MismatchedTernary'
     - 'Structures/MissingAssignation'
     - 'Structures/MissingCases'
     - 'Structures/MissingNew'
     - 'Structures/MissingParenthesis'
     - 'Structures/MisusedYield'
     - 'Structures/MixedConcatInterpolation'
     - 'Structures/ModernEmpty'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultipleTypeVariable'
     - 'Structures/MultiplyByOne'
     - 'Structures/NegativePow'
     - 'Structures/NestedIfthen'
     - 'Structures/NestedMatch'
     - 'Structures/NestedTernary'
     - 'Structures/NeverNegative'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoAppendOnSource'
     - 'Structures/NoChangeIncomingVariables'
     - 'Structures/NoChoice'
     - 'Structures/NoDirectUsage'
     - 'Structures/NoEmptyRegex'
     - 'Structures/NoEmptyStringWithExplode'
     - 'Structures/NoGetClassNull'
     - 'Structures/NoHardcodedHash'
     - 'Structures/NoHardcodedIp'
     - 'Structures/NoHardcodedPath'
     - 'Structures/NoHardcodedPort'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/NoNeedForElse'
     - 'Structures/NoNeedForTriple'
     - 'Structures/NoNullForIndex'
     - 'Structures/NoObjectAsIndex'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoReferenceOnLeft'
     - 'Structures/NoSubstrOne'
     - 'Structures/NoValidCast'
     - 'Structures/NoVariableIsACondition'
     - 'Structures/NonIntStringAsIndex'
     - 'Structures/Noscream'
     - 'Structures/NotEqual'
     - 'Structures/NotNot'
     - 'Structures/ObjectReferences'
     - 'Structures/OnceUsage'
     - 'Structures/OneLineTwoInstructions'
     - 'Structures/OnlyFirstByte'
     - 'Structures/OnlyVariableReturnedByReference'
     - 'Structures/OrDie'
     - 'Structures/OverwrittenForeachVar'
     - 'Structures/PossibleInfiniteLoop'
     - 'Structures/PrintAndDie'
     - 'Structures/PrintWithoutParenthesis'
     - 'Structures/PrintfArguments'
     - 'Structures/QueriesInLoop'
     - 'Structures/RepeatedPrint'
     - 'Structures/RepeatedRegex'
     - 'Structures/ResultMayBeMissing'
     - 'Structures/ReturnTrueFalse'
     - 'Structures/SameConditions'
     - 'Structures/ShouldChainException'
     - 'Structures/ShouldMakeTernary'
     - 'Structures/ShouldPreprocess'
     - 'Structures/ShouldUseExplodeArgs'
     - 'Structures/SprintfFormatCompilation'
     - 'Structures/StaticInclude'
     - 'Structures/StaticLoop'
     - 'Structures/StripTagsSkipsClosedTag'
     - 'Structures/StrposCompare'
     - 'Structures/StrposLessThanOne'
     - 'Structures/SuspiciousComparison'
     - 'Structures/SwitchToSwitch'
     - 'Structures/SwitchWithoutDefault'
     - 'Structures/TernaryInConcat'
     - 'Structures/TestThenCast'
     - 'Structures/ThrowsAndAssign'
     - 'Structures/TimestampDifference'
     - 'Structures/UncheckedResources'
     - 'Structures/UnconditionLoopBreak'
     - 'Structures/UnknownPregOption'
     - 'Structures/Unpreprocessed'
     - 'Structures/UnsetInForeach'
     - 'Structures/UnsupportedOperandTypes'
     - 'Structures/UnsupportedTypesWithOperators'
     - 'Structures/UnusedGlobal'
     - 'Structures/UseConstant'
     - 'Structures/UseInstanceof'
     - 'Structures/UsePositiveCondition'
     - 'Structures/UseSameTypesForComparisons'
     - 'Structures/UseSystemTmp'
     - 'Structures/UselessBrackets'
     - 'Structures/UselessCasting'
     - 'Structures/UselessCheck'
     - 'Structures/UselessCoalesce'
     - 'Structures/UselessGlobal'
     - 'Structures/UselessInstruction'
     - 'Structures/UselessNullCoalesce'
     - 'Structures/UselessParenthesis'
     - 'Structures/UselessShortTernary'
     - 'Structures/UselessSwitch'
     - 'Structures/UselessUnset'
     - 'Structures/VardumpUsage'
     - 'Structures/WhileListEach'
     - 'Structures/WrongLocale'
     - 'Structures/WrongPrecedenceInExpression'
     - 'Structures/WrongRange'
     - 'Structures/pregOptionE'
     - 'Structures/toStringThrowsException'
     - 'Traits/AlreadyParentsTrait'
     - 'Traits/CannotCallTraitMethod'
     - 'Traits/DependantTrait'
     - 'Traits/EmptyTrait'
     - 'Traits/MethodCollisionTraits'
     - 'Traits/TraitIsNotAType'
     - 'Traits/TraitNotFound'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UselessAlias'
     - 'Type/NoRealComparison'
     - 'Type/OneVariableStrings'
     - 'Type/ShouldTypecast'
     - 'Type/SilentlyCastInteger'
     - 'Type/StringHoldAVariable'
     - 'Type/StringWithStrangeSpace'
     - 'Typehints/MissingReturntype'
     - 'Typehints/StandaloneTypeTFN'
     - 'Typehints/WrongTypeWithDefault'
     - 'Variables/AssignedTwiceOrMore'
     - 'Variables/ConstantTypo'
     - 'Variables/LostReferences'
     - 'Variables/OverwrittenLiterals'
     - 'Variables/RecycledVariables'
     - 'Variables/UndefinedConstantName'
     - 'Variables/UndefinedVariable'
     - 'Variables/VariableNonascii'
     - 'Variables/VariableUsedOnce'
     - 'Variables/VariableUsedOnceByContext'
     - 'Variables/WrittenOnlyVariable'




.. _annex-appinfo:

Appinfo
#######


.. _annex-ini-appinfo:

Appinfo for INI
+++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Appinfo]
   analyzer[] = "Arrays/ArrayNSUsage";
   analyzer[] = "Arrays/Arrayindex";
   analyzer[] = "Arrays/Multidimensional";
   analyzer[] = "Arrays/Phparrayindex";
   analyzer[] = "Arrays/WithCallback";
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Classes/Abstractclass";
   analyzer[] = "Classes/Abstractmethods";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/ClassAliasUsage";
   analyzer[] = "Classes/ClassOverreach";
   analyzer[] = "Classes/Classnames";
   analyzer[] = "Classes/CloningUsage";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/ConstantDefinition";
   analyzer[] = "Classes/DynamicClass";
   analyzer[] = "Classes/DynamicConstantCall";
   analyzer[] = "Classes/DynamicMethodCall";
   analyzer[] = "Classes/DynamicNew";
   analyzer[] = "Classes/DynamicPropertyCall";
   analyzer[] = "Classes/ImmutableSignature";
   analyzer[] = "Classes/MagicMethod";
   analyzer[] = "Classes/MultipleClassesInFile";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/OverwrittenConst";
   analyzer[] = "Classes/PromotedProperties";
   analyzer[] = "Classes/ReadonlyUsage";
   analyzer[] = "Classes/RedefinedMethods";
   analyzer[] = "Classes/StaticMethods";
   analyzer[] = "Classes/StaticProperties";
   analyzer[] = "Classes/TestClass";
   analyzer[] = "Classes/UntypedNoDefaultProperties";
   analyzer[] = "Classes/VariableClasses";
   analyzer[] = "Composer/Autoload";
   analyzer[] = "Composer/UseComposer";
   analyzer[] = "Composer/UseComposerLock";
   analyzer[] = "Constants/CaseInsensitiveConstants";
   analyzer[] = "Constants/ConditionedConstants";
   analyzer[] = "Constants/ConstantUsage";
   analyzer[] = "Constants/DynamicCreation";
   analyzer[] = "Constants/MagicConstantUsage";
   analyzer[] = "Constants/PhpConstantUsage";
   analyzer[] = "Constants/VariableConstant";
   analyzer[] = "Dump/ParameterArgumentsLinks";
   analyzer[] = "Exceptions/DefinedExceptions";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Exceptions/ThrownExceptions";
   analyzer[] = "Extensions/Extamqp";
   analyzer[] = "Extensions/Extapache";
   analyzer[] = "Extensions/Extapc";
   analyzer[] = "Extensions/Extapcu";
   analyzer[] = "Extensions/Extarray";
   analyzer[] = "Extensions/Extast";
   analyzer[] = "Extensions/Extbcmath";
   analyzer[] = "Extensions/Extbzip2";
   analyzer[] = "Extensions/Extcalendar";
   analyzer[] = "Extensions/Extcmark";
   analyzer[] = "Extensions/Extcom";
   analyzer[] = "Extensions/Extcrypto";
   analyzer[] = "Extensions/Extcsv";
   analyzer[] = "Extensions/Extctype";
   analyzer[] = "Extensions/Extcurl";
   analyzer[] = "Extensions/Extdate";
   analyzer[] = "Extensions/Extdb2";
   analyzer[] = "Extensions/Extdba";
   analyzer[] = "Extensions/Extdecimal";
   analyzer[] = "Extensions/Extdio";
   analyzer[] = "Extensions/Extdom";
   analyzer[] = "Extensions/Extds";
   analyzer[] = "Extensions/Exteaccelerator";
   analyzer[] = "Extensions/Exteio";
   analyzer[] = "Extensions/Extenchant";
   analyzer[] = "Extensions/Extev";
   analyzer[] = "Extensions/Extevent";
   analyzer[] = "Extensions/Extexcimer";
   analyzer[] = "Extensions/Extexif";
   analyzer[] = "Extensions/Extexpect";
   analyzer[] = "Extensions/Extfam";
   analyzer[] = "Extensions/Extfann";
   analyzer[] = "Extensions/Extffi";
   analyzer[] = "Extensions/Extfile";
   analyzer[] = "Extensions/Extfileinfo";
   analyzer[] = "Extensions/Extfilter";
   analyzer[] = "Extensions/Extfpm";
   analyzer[] = "Extensions/Extftp";
   analyzer[] = "Extensions/Extgd";
   analyzer[] = "Extensions/Extgearman";
   analyzer[] = "Extensions/Extgender";
   analyzer[] = "Extensions/Extgeoip";
   analyzer[] = "Extensions/Extgeospatial";
   analyzer[] = "Extensions/Extgettext";
   analyzer[] = "Extensions/Extgmagick";
   analyzer[] = "Extensions/Extgmp";
   analyzer[] = "Extensions/Extgnupg";
   analyzer[] = "Extensions/Extgrpc";
   analyzer[] = "Extensions/Exthash";
   analyzer[] = "Extensions/Exthrtime";
   analyzer[] = "Extensions/Exthttp";
   analyzer[] = "Extensions/Extibase";
   analyzer[] = "Extensions/Extice";
   analyzer[] = "Extensions/Exticonv";
   analyzer[] = "Extensions/Extigbinary";
   analyzer[] = "Extensions/Extimagick";
   analyzer[] = "Extensions/Extimap";
   analyzer[] = "Extensions/Extinfo";
   analyzer[] = "Extensions/Extinotify";
   analyzer[] = "Extensions/Extintl";
   analyzer[] = "Extensions/Extjson";
   analyzer[] = "Extensions/Extjudy";
   analyzer[] = "Extensions/Extldap";
   analyzer[] = "Extensions/Extleveldb";
   analyzer[] = "Extensions/Extlibsodium";
   analyzer[] = "Extensions/Extlibxml";
   analyzer[] = "Extensions/Extlua";
   analyzer[] = "Extensions/Extlzf";
   analyzer[] = "Extensions/Extmail";
   analyzer[] = "Extensions/Extmailparse";
   analyzer[] = "Extensions/Extmath";
   analyzer[] = "Extensions/Extmbstring";
   analyzer[] = "Extensions/Extmcrypt";
   analyzer[] = "Extensions/Extmemcache";
   analyzer[] = "Extensions/Extmemcached";
   analyzer[] = "Extensions/Extmongo";
   analyzer[] = "Extensions/Extmongodb";
   analyzer[] = "Extensions/Extmsgpack";
   analyzer[] = "Extensions/Extmssql";
   analyzer[] = "Extensions/Extmysql";
   analyzer[] = "Extensions/Extmysqli";
   analyzer[] = "Extensions/Extncurses";
   analyzer[] = "Extensions/Extnewt";
   analyzer[] = "Extensions/Extnsapi";
   analyzer[] = "Extensions/Extob";
   analyzer[] = "Extensions/Extoci8";
   analyzer[] = "Extensions/Extodbc";
   analyzer[] = "Extensions/Extopcache";
   analyzer[] = "Extensions/Extopencensus";
   analyzer[] = "Extensions/Extopenssl";
   analyzer[] = "Extensions/Extparle";
   analyzer[] = "Extensions/Extpassword";
   analyzer[] = "Extensions/Extpcntl";
   analyzer[] = "Extensions/Extpcov";
   analyzer[] = "Extensions/Extpcre";
   analyzer[] = "Extensions/Extpdo";
   analyzer[] = "Extensions/Extpgsql";
   analyzer[] = "Extensions/Extphalcon";
   analyzer[] = "Extensions/Extphar";
   analyzer[] = "Extensions/Extpkcs11";
   analyzer[] = "Extensions/Extposix";
   analyzer[] = "Extensions/Extprotobuf";
   analyzer[] = "Extensions/Extpspell";
   analyzer[] = "Extensions/Extpsr";
   analyzer[] = "Extensions/Extrandom";
   analyzer[] = "Extensions/Extrar";
   analyzer[] = "Extensions/Extrdkafka";
   analyzer[] = "Extensions/Extreadline";
   analyzer[] = "Extensions/Extredis";
   analyzer[] = "Extensions/Extreflection";
   analyzer[] = "Extensions/Extscrypt";
   analyzer[] = "Extensions/Extsdl";
   analyzer[] = "Extensions/Extseaslog";
   analyzer[] = "Extensions/Extsem";
   analyzer[] = "Extensions/Extsession";
   analyzer[] = "Extensions/Extshmop";
   analyzer[] = "Extensions/Extsimplexml";
   analyzer[] = "Extensions/Extsnmp";
   analyzer[] = "Extensions/Extsoap";
   analyzer[] = "Extensions/Extsockets";
   analyzer[] = "Extensions/Extsphinx";
   analyzer[] = "Extensions/Extspl";
   analyzer[] = "Extensions/Extspx";
   analyzer[] = "Extensions/Extsqlite";
   analyzer[] = "Extensions/Extsqlite3";
   analyzer[] = "Extensions/Extsqlsrv";
   analyzer[] = "Extensions/Extssh2";
   analyzer[] = "Extensions/Extstandard";
   analyzer[] = "Extensions/Extstats";
   analyzer[] = "Extensions/Extstomp";
   analyzer[] = "Extensions/Extstring";
   analyzer[] = "Extensions/Extsuhosin";
   analyzer[] = "Extensions/Extsvm";
   analyzer[] = "Extensions/Extswoole";
   analyzer[] = "Extensions/Exttaint";
   analyzer[] = "Extensions/Extteds";
   analyzer[] = "Extensions/Exttidy";
   analyzer[] = "Extensions/Exttokenizer";
   analyzer[] = "Extensions/Exttokyotyrant";
   analyzer[] = "Extensions/Exttrader";
   analyzer[] = "Extensions/Extuopz";
   analyzer[] = "Extensions/Extuuid";
   analyzer[] = "Extensions/Extv8js";
   analyzer[] = "Extensions/Extvarnish";
   analyzer[] = "Extensions/Extvips";
   analyzer[] = "Extensions/Extwasm";
   analyzer[] = "Extensions/Extwddx";
   analyzer[] = "Extensions/Extweakref";
   analyzer[] = "Extensions/Extxattr";
   analyzer[] = "Extensions/Extxdebug";
   analyzer[] = "Extensions/Extxdiff";
   analyzer[] = "Extensions/Extxhprof";
   analyzer[] = "Extensions/Extxml";
   analyzer[] = "Extensions/Extxmlreader";
   analyzer[] = "Extensions/Extxmlrpc";
   analyzer[] = "Extensions/Extxmlwriter";
   analyzer[] = "Extensions/Extxsl";
   analyzer[] = "Extensions/Extxxtea";
   analyzer[] = "Extensions/Extyaml";
   analyzer[] = "Extensions/Extyar";
   analyzer[] = "Extensions/Extzendmonitor";
   analyzer[] = "Extensions/Extzip";
   analyzer[] = "Extensions/Extzlib";
   analyzer[] = "Extensions/Extzmq";
   analyzer[] = "Extensions/Extzookeeper";
   analyzer[] = "Files/IsCliScript";
   analyzer[] = "Files/NotDefinitionsOnly";
   analyzer[] = "Functions/Closures";
   analyzer[] = "Functions/ConditionedFunctions";
   analyzer[] = "Functions/DeepDefinitions";
   analyzer[] = "Functions/Dynamiccall";
   analyzer[] = "Functions/FallbackFunction";
   analyzer[] = "Functions/Functionnames";
   analyzer[] = "Functions/FunctionsUsingReference";
   analyzer[] = "Functions/IsGenerator";
   analyzer[] = "Functions/MultipleDeclarations";
   analyzer[] = "Functions/Recursive";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/Typehints";
   analyzer[] = "Functions/UseArrowFunctions";
   analyzer[] = "Functions/VariableArguments";
   analyzer[] = "Interfaces/Interfacenames";
   analyzer[] = "Namespaces/Alias";
   analyzer[] = "Namespaces/NamespaceUsage";
   analyzer[] = "Namespaces/Namespacesnames";
   analyzer[] = "Patterns/CourrierAntiPattern";
   analyzer[] = "Patterns/DependencyInjection";
   analyzer[] = "Patterns/Factory";
   analyzer[] = "Php/AlternativeSyntax";
   analyzer[] = "Php/Argon2Usage";
   analyzer[] = "Php/AssertionUsage";
   analyzer[] = "Php/AutoloadUsage";
   analyzer[] = "Php/CastingUsage";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/Coalesce";
   analyzer[] = "Php/CryptoUsage";
   analyzer[] = "Php/DeclareEncoding";
   analyzer[] = "Php/DeclareStrict";
   analyzer[] = "Php/DeclareStrictType";
   analyzer[] = "Php/DeclareTicks";
   analyzer[] = "Php/DirectiveName";
   analyzer[] = "Php/DirectivesUsage";
   analyzer[] = "Php/DlUsage";
   analyzer[] = "Php/EchoTagUsage";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/ErrorLogUsage";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FirstClassCallable";
   analyzer[] = "Php/Gotonames";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/Haltcompiler";
   analyzer[] = "Php/HasAsymmetricVisibility";
   analyzer[] = "Php/HasPropertyHook";
   analyzer[] = "Php/HasVirtualProperty";
   analyzer[] = "Php/Incompilable";
   analyzer[] = "Php/IntegerSeparatorUsage";
   analyzer[] = "Php/IsINF";
   analyzer[] = "Php/IsNAN";
   analyzer[] = "Php/Labelnames";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/MiddleVersion";
   analyzer[] = "Php/MixedUsage";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NeverKeyword";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/OveriddenFunction";
   analyzer[] = "Php/PearUsage";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php80VariableSyntax";
   analyzer[] = "Php/Php81IntersectionTypehint";
   analyzer[] = "Php/PlusPlusOnLetters";
   analyzer[] = "Php/RawPostDataUsage";
   analyzer[] = "Php/ReturnTypehintUsage";
   analyzer[] = "Php/ScalarTypehintUsage";
   analyzer[] = "Php/ShortTernary";
   analyzer[] = "Php/SpreadOperatorForArray";
   analyzer[] = "Php/SuperGlobalUsage";
   analyzer[] = "Php/ThrowUsage";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TriggerErrorUsage";
   analyzer[] = "Php/TryCatchUsage";
   analyzer[] = "Php/TryMultipleCatch";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UseAttributes";
   analyzer[] = "Php/UseBrowscap";
   analyzer[] = "Php/UseClassAlias";
   analyzer[] = "Php/UseCli";
   analyzer[] = "Php/UseContravariance";
   analyzer[] = "Php/UseCookies";
   analyzer[] = "Php/UseCovariance";
   analyzer[] = "Php/UseDNF";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullSafeOperator";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/UseTrailingUseComma";
   analyzer[] = "Php/UseWeb";
   analyzer[] = "Php/UsesEnv";
   analyzer[] = "Php/YieldFromUsage";
   analyzer[] = "Php/YieldUsage";
   analyzer[] = "Psr/Psr11Usage";
   analyzer[] = "Psr/Psr13Usage";
   analyzer[] = "Psr/Psr16Usage";
   analyzer[] = "Psr/Psr3Usage";
   analyzer[] = "Psr/Psr6Usage";
   analyzer[] = "Psr/Psr7Usage";
   analyzer[] = "Security/CantDisableClass";
   analyzer[] = "Security/CantDisableFunction";
   analyzer[] = "Structures/ArrayAddition";
   analyzer[] = "Structures/ComplexExpression";
   analyzer[] = "Structures/ConstDefineFavorite";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/DateTimePreference";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/DynamicCalls";
   analyzer[] = "Structures/DynamicCode";
   analyzer[] = "Structures/ElseUsage";
   analyzer[] = "Structures/ErrorMessages";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FilePutContentsDataType";
   analyzer[] = "Structures/FileUploadUsage";
   analyzer[] = "Structures/FileUsage";
   analyzer[] = "Structures/FunctionSubscripting";
   analyzer[] = "Structures/GlobalInGlobal";
   analyzer[] = "Structures/GlobalUsage";
   analyzer[] = "Structures/IncludeUsage";
   analyzer[] = "Structures/MailUsage";
   analyzer[] = "Structures/MultipleCatch";
   analyzer[] = "Structures/NestedLoops";
   analyzer[] = "Structures/NoDirectAccess";
   analyzer[] = "Structures/NonBreakableSpaceInNames";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/OnceUsage";
   analyzer[] = "Structures/ResourcesUsage";
   analyzer[] = "Structures/ShellUsage";
   analyzer[] = "Structures/ShortTags";
   analyzer[] = "Structures/TryFinally";
   analyzer[] = "Structures/UseDebug";
   analyzer[] = "Traits/Php";
   analyzer[] = "Traits/TraitUsage";
   analyzer[] = "Traits/Traitnames";
   analyzer[] = "Type/ArrayIndex";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/Email";
   analyzer[] = "Type/GPCIndex";
   analyzer[] = "Type/Heredoc";
   analyzer[] = "Type/Hexadecimal";
   analyzer[] = "Type/Ip";
   analyzer[] = "Type/Md5String";
   analyzer[] = "Type/Nowdoc";
   analyzer[] = "Type/Octal";
   analyzer[] = "Type/Pack";
   analyzer[] = "Type/Path";
   analyzer[] = "Type/Printf";
   analyzer[] = "Type/Protocols";
   analyzer[] = "Type/Regex";
   analyzer[] = "Type/Shellcommands";
   analyzer[] = "Type/Sql";
   analyzer[] = "Type/Url";
   analyzer[] = "Variables/References";
   analyzer[] = "Variables/StaticVariables";
   analyzer[] = "Variables/UncommonEnvVar";
   analyzer[] = "Variables/VariableLong";
   analyzer[] = "Variables/VariablePhp";
   analyzer[] = "Variables/VariableVariables";
   analyzer[] = "Vendors/Cakephp";
   analyzer[] = "Vendors/Codeigniter";
   analyzer[] = "Vendors/Concrete5";
   analyzer[] = "Vendors/Drupal";
   analyzer[] = "Vendors/Feast";
   analyzer[] = "Vendors/Fuel";
   analyzer[] = "Vendors/Joomla";
   analyzer[] = "Vendors/Laravel";
   analyzer[] = "Vendors/Neos";
   analyzer[] = "Vendors/Phalcon";
   analyzer[] = "Vendors/Sylius";
   analyzer[] = "Vendors/Symfony";
   analyzer[] = "Vendors/Typo3";
   analyzer[] = "Vendors/Wordpress";
   analyzer[] = "Vendors/Yii";


.. _annex-yaml-appinfo:

Appinfo for .exakat.yaml
++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Appinfo':
     - 'Arrays/ArrayNSUsage'
     - 'Arrays/Arrayindex'
     - 'Arrays/Multidimensional'
     - 'Arrays/Phparrayindex'
     - 'Arrays/WithCallback'
     - 'Attributes/NestedAttributes'
     - 'Classes/Abstractclass'
     - 'Classes/Abstractmethods'
     - 'Classes/Anonymous'
     - 'Classes/ClassAliasUsage'
     - 'Classes/ClassOverreach'
     - 'Classes/Classnames'
     - 'Classes/CloningUsage'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/ConstantDefinition'
     - 'Classes/DynamicClass'
     - 'Classes/DynamicConstantCall'
     - 'Classes/DynamicMethodCall'
     - 'Classes/DynamicNew'
     - 'Classes/DynamicPropertyCall'
     - 'Classes/ImmutableSignature'
     - 'Classes/MagicMethod'
     - 'Classes/MultipleClassesInFile'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/OldStyleConstructor'
     - 'Classes/OverwrittenConst'
     - 'Classes/PromotedProperties'
     - 'Classes/ReadonlyUsage'
     - 'Classes/RedefinedMethods'
     - 'Classes/StaticMethods'
     - 'Classes/StaticProperties'
     - 'Classes/TestClass'
     - 'Classes/UntypedNoDefaultProperties'
     - 'Classes/VariableClasses'
     - 'Composer/Autoload'
     - 'Composer/UseComposer'
     - 'Composer/UseComposerLock'
     - 'Constants/CaseInsensitiveConstants'
     - 'Constants/ConditionedConstants'
     - 'Constants/ConstantUsage'
     - 'Constants/DynamicCreation'
     - 'Constants/MagicConstantUsage'
     - 'Constants/PhpConstantUsage'
     - 'Constants/VariableConstant'
     - 'Dump/ParameterArgumentsLinks'
     - 'Exceptions/DefinedExceptions'
     - 'Exceptions/MultipleCatch'
     - 'Exceptions/ThrownExceptions'
     - 'Extensions/Extamqp'
     - 'Extensions/Extapache'
     - 'Extensions/Extapc'
     - 'Extensions/Extapcu'
     - 'Extensions/Extarray'
     - 'Extensions/Extast'
     - 'Extensions/Extbcmath'
     - 'Extensions/Extbzip2'
     - 'Extensions/Extcalendar'
     - 'Extensions/Extcmark'
     - 'Extensions/Extcom'
     - 'Extensions/Extcrypto'
     - 'Extensions/Extcsv'
     - 'Extensions/Extctype'
     - 'Extensions/Extcurl'
     - 'Extensions/Extdate'
     - 'Extensions/Extdb2'
     - 'Extensions/Extdba'
     - 'Extensions/Extdecimal'
     - 'Extensions/Extdio'
     - 'Extensions/Extdom'
     - 'Extensions/Extds'
     - 'Extensions/Exteaccelerator'
     - 'Extensions/Exteio'
     - 'Extensions/Extenchant'
     - 'Extensions/Extev'
     - 'Extensions/Extevent'
     - 'Extensions/Extexcimer'
     - 'Extensions/Extexif'
     - 'Extensions/Extexpect'
     - 'Extensions/Extfam'
     - 'Extensions/Extfann'
     - 'Extensions/Extffi'
     - 'Extensions/Extfile'
     - 'Extensions/Extfileinfo'
     - 'Extensions/Extfilter'
     - 'Extensions/Extfpm'
     - 'Extensions/Extftp'
     - 'Extensions/Extgd'
     - 'Extensions/Extgearman'
     - 'Extensions/Extgender'
     - 'Extensions/Extgeoip'
     - 'Extensions/Extgeospatial'
     - 'Extensions/Extgettext'
     - 'Extensions/Extgmagick'
     - 'Extensions/Extgmp'
     - 'Extensions/Extgnupg'
     - 'Extensions/Extgrpc'
     - 'Extensions/Exthash'
     - 'Extensions/Exthrtime'
     - 'Extensions/Exthttp'
     - 'Extensions/Extibase'
     - 'Extensions/Extice'
     - 'Extensions/Exticonv'
     - 'Extensions/Extigbinary'
     - 'Extensions/Extimagick'
     - 'Extensions/Extimap'
     - 'Extensions/Extinfo'
     - 'Extensions/Extinotify'
     - 'Extensions/Extintl'
     - 'Extensions/Extjson'
     - 'Extensions/Extjudy'
     - 'Extensions/Extldap'
     - 'Extensions/Extleveldb'
     - 'Extensions/Extlibsodium'
     - 'Extensions/Extlibxml'
     - 'Extensions/Extlua'
     - 'Extensions/Extlzf'
     - 'Extensions/Extmail'
     - 'Extensions/Extmailparse'
     - 'Extensions/Extmath'
     - 'Extensions/Extmbstring'
     - 'Extensions/Extmcrypt'
     - 'Extensions/Extmemcache'
     - 'Extensions/Extmemcached'
     - 'Extensions/Extmongo'
     - 'Extensions/Extmongodb'
     - 'Extensions/Extmsgpack'
     - 'Extensions/Extmssql'
     - 'Extensions/Extmysql'
     - 'Extensions/Extmysqli'
     - 'Extensions/Extncurses'
     - 'Extensions/Extnewt'
     - 'Extensions/Extnsapi'
     - 'Extensions/Extob'
     - 'Extensions/Extoci8'
     - 'Extensions/Extodbc'
     - 'Extensions/Extopcache'
     - 'Extensions/Extopencensus'
     - 'Extensions/Extopenssl'
     - 'Extensions/Extparle'
     - 'Extensions/Extpassword'
     - 'Extensions/Extpcntl'
     - 'Extensions/Extpcov'
     - 'Extensions/Extpcre'
     - 'Extensions/Extpdo'
     - 'Extensions/Extpgsql'
     - 'Extensions/Extphalcon'
     - 'Extensions/Extphar'
     - 'Extensions/Extpkcs11'
     - 'Extensions/Extposix'
     - 'Extensions/Extprotobuf'
     - 'Extensions/Extpspell'
     - 'Extensions/Extpsr'
     - 'Extensions/Extrandom'
     - 'Extensions/Extrar'
     - 'Extensions/Extrdkafka'
     - 'Extensions/Extreadline'
     - 'Extensions/Extredis'
     - 'Extensions/Extreflection'
     - 'Extensions/Extscrypt'
     - 'Extensions/Extsdl'
     - 'Extensions/Extseaslog'
     - 'Extensions/Extsem'
     - 'Extensions/Extsession'
     - 'Extensions/Extshmop'
     - 'Extensions/Extsimplexml'
     - 'Extensions/Extsnmp'
     - 'Extensions/Extsoap'
     - 'Extensions/Extsockets'
     - 'Extensions/Extsphinx'
     - 'Extensions/Extspl'
     - 'Extensions/Extspx'
     - 'Extensions/Extsqlite'
     - 'Extensions/Extsqlite3'
     - 'Extensions/Extsqlsrv'
     - 'Extensions/Extssh2'
     - 'Extensions/Extstandard'
     - 'Extensions/Extstats'
     - 'Extensions/Extstomp'
     - 'Extensions/Extstring'
     - 'Extensions/Extsuhosin'
     - 'Extensions/Extsvm'
     - 'Extensions/Extswoole'
     - 'Extensions/Exttaint'
     - 'Extensions/Extteds'
     - 'Extensions/Exttidy'
     - 'Extensions/Exttokenizer'
     - 'Extensions/Exttokyotyrant'
     - 'Extensions/Exttrader'
     - 'Extensions/Extuopz'
     - 'Extensions/Extuuid'
     - 'Extensions/Extv8js'
     - 'Extensions/Extvarnish'
     - 'Extensions/Extvips'
     - 'Extensions/Extwasm'
     - 'Extensions/Extwddx'
     - 'Extensions/Extweakref'
     - 'Extensions/Extxattr'
     - 'Extensions/Extxdebug'
     - 'Extensions/Extxdiff'
     - 'Extensions/Extxhprof'
     - 'Extensions/Extxml'
     - 'Extensions/Extxmlreader'
     - 'Extensions/Extxmlrpc'
     - 'Extensions/Extxmlwriter'
     - 'Extensions/Extxsl'
     - 'Extensions/Extxxtea'
     - 'Extensions/Extyaml'
     - 'Extensions/Extyar'
     - 'Extensions/Extzendmonitor'
     - 'Extensions/Extzip'
     - 'Extensions/Extzlib'
     - 'Extensions/Extzmq'
     - 'Extensions/Extzookeeper'
     - 'Files/IsCliScript'
     - 'Files/NotDefinitionsOnly'
     - 'Functions/Closures'
     - 'Functions/ConditionedFunctions'
     - 'Functions/DeepDefinitions'
     - 'Functions/Dynamiccall'
     - 'Functions/FallbackFunction'
     - 'Functions/Functionnames'
     - 'Functions/FunctionsUsingReference'
     - 'Functions/IsGenerator'
     - 'Functions/MultipleDeclarations'
     - 'Functions/Recursive'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/Typehints'
     - 'Functions/UseArrowFunctions'
     - 'Functions/VariableArguments'
     - 'Interfaces/Interfacenames'
     - 'Namespaces/Alias'
     - 'Namespaces/NamespaceUsage'
     - 'Namespaces/Namespacesnames'
     - 'Patterns/CourrierAntiPattern'
     - 'Patterns/DependencyInjection'
     - 'Patterns/Factory'
     - 'Php/AlternativeSyntax'
     - 'Php/Argon2Usage'
     - 'Php/AssertionUsage'
     - 'Php/AutoloadUsage'
     - 'Php/CastingUsage'
     - 'Php/ClosureInConstant'
     - 'Php/Coalesce'
     - 'Php/CryptoUsage'
     - 'Php/DeclareEncoding'
     - 'Php/DeclareStrict'
     - 'Php/DeclareStrictType'
     - 'Php/DeclareTicks'
     - 'Php/DirectiveName'
     - 'Php/DirectivesUsage'
     - 'Php/DlUsage'
     - 'Php/EchoTagUsage'
     - 'Php/EllipsisUsage'
     - 'Php/ErrorLogUsage'
     - 'Php/FinalConstant'
     - 'Php/FirstClassCallable'
     - 'Php/Gotonames'
     - 'Php/GroupUseDeclaration'
     - 'Php/Haltcompiler'
     - 'Php/HasAsymmetricVisibility'
     - 'Php/HasPropertyHook'
     - 'Php/HasVirtualProperty'
     - 'Php/Incompilable'
     - 'Php/IntegerSeparatorUsage'
     - 'Php/IsINF'
     - 'Php/IsNAN'
     - 'Php/Labelnames'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/MiddleVersion'
     - 'Php/MixedUsage'
     - 'Php/NamedParameterUsage'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NeverKeyword'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewInitializers'
     - 'Php/NewWithoutParenthesis'
     - 'Php/OveriddenFunction'
     - 'Php/PearUsage'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php80VariableSyntax'
     - 'Php/Php81IntersectionTypehint'
     - 'Php/PlusPlusOnLetters'
     - 'Php/RawPostDataUsage'
     - 'Php/ReturnTypehintUsage'
     - 'Php/ScalarTypehintUsage'
     - 'Php/ShortTernary'
     - 'Php/SpreadOperatorForArray'
     - 'Php/SuperGlobalUsage'
     - 'Php/ThrowUsage'
     - 'Php/TrailingComma'
     - 'Php/TriggerErrorUsage'
     - 'Php/TryCatchUsage'
     - 'Php/TryMultipleCatch'
     - 'Php/TypedPropertyUsage'
     - 'Php/UseAttributes'
     - 'Php/UseBrowscap'
     - 'Php/UseClassAlias'
     - 'Php/UseCli'
     - 'Php/UseContravariance'
     - 'Php/UseCookies'
     - 'Php/UseCovariance'
     - 'Php/UseDNF'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullSafeOperator'
     - 'Php/UseNullableType'
     - 'Php/UseTrailingUseComma'
     - 'Php/UseWeb'
     - 'Php/UsesEnv'
     - 'Php/YieldFromUsage'
     - 'Php/YieldUsage'
     - 'Psr/Psr11Usage'
     - 'Psr/Psr13Usage'
     - 'Psr/Psr16Usage'
     - 'Psr/Psr3Usage'
     - 'Psr/Psr6Usage'
     - 'Psr/Psr7Usage'
     - 'Security/CantDisableClass'
     - 'Security/CantDisableFunction'
     - 'Structures/ArrayAddition'
     - 'Structures/ComplexExpression'
     - 'Structures/ConstDefineFavorite'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/DateTimePreference'
     - 'Structures/DereferencingAS'
     - 'Structures/DynamicCalls'
     - 'Structures/DynamicCode'
     - 'Structures/ElseUsage'
     - 'Structures/ErrorMessages'
     - 'Structures/EvalUsage'
     - 'Structures/ExitUsage'
     - 'Structures/FilePutContentsDataType'
     - 'Structures/FileUploadUsage'
     - 'Structures/FileUsage'
     - 'Structures/FunctionSubscripting'
     - 'Structures/GlobalInGlobal'
     - 'Structures/GlobalUsage'
     - 'Structures/IncludeUsage'
     - 'Structures/MailUsage'
     - 'Structures/MultipleCatch'
     - 'Structures/NestedLoops'
     - 'Structures/NoDirectAccess'
     - 'Structures/NonBreakableSpaceInNames'
     - 'Structures/Noscream'
     - 'Structures/OnceUsage'
     - 'Structures/ResourcesUsage'
     - 'Structures/ShellUsage'
     - 'Structures/ShortTags'
     - 'Structures/TryFinally'
     - 'Structures/UseDebug'
     - 'Traits/Php'
     - 'Traits/TraitUsage'
     - 'Traits/Traitnames'
     - 'Type/ArrayIndex'
     - 'Type/Binary'
     - 'Type/Email'
     - 'Type/GPCIndex'
     - 'Type/Heredoc'
     - 'Type/Hexadecimal'
     - 'Type/Ip'
     - 'Type/Md5String'
     - 'Type/Nowdoc'
     - 'Type/Octal'
     - 'Type/Pack'
     - 'Type/Path'
     - 'Type/Printf'
     - 'Type/Protocols'
     - 'Type/Regex'
     - 'Type/Shellcommands'
     - 'Type/Sql'
     - 'Type/Url'
     - 'Variables/References'
     - 'Variables/StaticVariables'
     - 'Variables/UncommonEnvVar'
     - 'Variables/VariableLong'
     - 'Variables/VariablePhp'
     - 'Variables/VariableVariables'
     - 'Vendors/Cakephp'
     - 'Vendors/Codeigniter'
     - 'Vendors/Concrete5'
     - 'Vendors/Drupal'
     - 'Vendors/Feast'
     - 'Vendors/Fuel'
     - 'Vendors/Joomla'
     - 'Vendors/Laravel'
     - 'Vendors/Neos'
     - 'Vendors/Phalcon'
     - 'Vendors/Sylius'
     - 'Vendors/Symfony'
     - 'Vendors/Typo3'
     - 'Vendors/Wordpress'
     - 'Vendors/Yii'




.. _annex-attributes:

Attributes
##########


.. _annex-ini-attributes:

Attributes for INI
++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Attributes]
   analyzer[] = "Attributes/Deprecated";
   analyzer[] = "Attributes/Friend";
   analyzer[] = "Attributes/MissingAttributeAttribute";
   analyzer[] = "Attributes/ModifyImmutable";
   analyzer[] = "Attributes/MustUseResult";
   analyzer[] = "Attributes/MustUseReturnReturns";
   analyzer[] = "Attributes/NoNamedArguments";
   analyzer[] = "Attributes/Override";
   analyzer[] = "Attributes/PhpNativeAttributes";
   analyzer[] = "Attributes/UselessOverride";
   analyzer[] = "Attributes/UsingDeprecated";
   analyzer[] = "Functions/KillsApp";
   analyzer[] = "Functions/UsingDeprecated";


.. _annex-yaml-attributes:

Attributes for .exakat.yaml
+++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Attributes':
     - 'Attributes/Deprecated'
     - 'Attributes/Friend'
     - 'Attributes/MissingAttributeAttribute'
     - 'Attributes/ModifyImmutable'
     - 'Attributes/MustUseResult'
     - 'Attributes/MustUseReturnReturns'
     - 'Attributes/NoNamedArguments'
     - 'Attributes/Override'
     - 'Attributes/PhpNativeAttributes'
     - 'Attributes/UselessOverride'
     - 'Attributes/UsingDeprecated'
     - 'Functions/KillsApp'
     - 'Functions/UsingDeprecated'




.. _annex-ce:

CE
##


.. _annex-ini-ce:

CE for INI
++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CE]
   analyzer[] = "Arrays/ArrayNSUsage";
   analyzer[] = "Arrays/Arrayindex";
   analyzer[] = "Arrays/Multidimensional";
   analyzer[] = "Arrays/MultipleIdenticalKeys";
   analyzer[] = "Arrays/NegativeStart";
   analyzer[] = "Arrays/Phparrayindex";
   analyzer[] = "Arrays/WithCallback";
   analyzer[] = "Classes/Abstractclass";
   analyzer[] = "Classes/Abstractmethods";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/CheckOnCallUsage";
   analyzer[] = "Classes/ClassAliasUsage";
   analyzer[] = "Classes/Classnames";
   analyzer[] = "Classes/CloningUsage";
   analyzer[] = "Classes/ConstantClass";
   analyzer[] = "Classes/ConstantDefinition";
   analyzer[] = "Classes/DefinedConstants";
   analyzer[] = "Classes/DefinedProperty";
   analyzer[] = "Classes/DirectCallToMagicMethod";
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/DynamicClass";
   analyzer[] = "Classes/DynamicConstantCall";
   analyzer[] = "Classes/DynamicMethodCall";
   analyzer[] = "Classes/DynamicNew";
   analyzer[] = "Classes/DynamicPropertyCall";
   analyzer[] = "Classes/FinalPrivate";
   analyzer[] = "Classes/HasMagicProperty";
   analyzer[] = "Classes/ImmutableSignature";
   analyzer[] = "Classes/IsNotFamily";
   analyzer[] = "Classes/IsaMagicProperty";
   analyzer[] = "Classes/MagicMethod";
   analyzer[] = "Classes/MultipleClassesInFile";
   analyzer[] = "Classes/MultipleDeclarations";
   analyzer[] = "Classes/MultipleTraitOrInterface";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NonPpp";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/OverwrittenConst";
   analyzer[] = "Classes/RedefinedConstants";
   analyzer[] = "Classes/RedefinedDefault";
   analyzer[] = "Classes/RedefinedMethods";
   analyzer[] = "Classes/StaticContainsThis";
   analyzer[] = "Classes/StaticMethods";
   analyzer[] = "Classes/StaticMethodsCalledFromObject";
   analyzer[] = "Classes/StaticProperties";
   analyzer[] = "Classes/TestClass";
   analyzer[] = "Classes/ThrowInDestruct";
   analyzer[] = "Classes/UndeclaredStaticProperty";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Classes/UndefinedStaticclass";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Classes/UseInstanceof";
   analyzer[] = "Classes/UselessFinal";
   analyzer[] = "Classes/VariableClasses";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Complete/CreateCompactVariables";
   analyzer[] = "Complete/CreateMagicProperty";
   analyzer[] = "Complete/FollowClosureDefinition";
   analyzer[] = "Complete/MakeClassConstantDefinition";
   analyzer[] = "Complete/MakeFunctioncallWithReference";
   analyzer[] = "Complete/OverwrittenConstants";
   analyzer[] = "Complete/OverwrittenProperties";
   analyzer[] = "Complete/SetArrayClassDefinition";
   analyzer[] = "Complete/SetParentDefinition";
   analyzer[] = "Composer/Autoload";
   analyzer[] = "Composer/UseComposer";
   analyzer[] = "Composer/UseComposerLock";
   analyzer[] = "Constants/CaseInsensitiveConstants";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Constants/ConstantStrangeNames";
   analyzer[] = "Constants/ConstantUsage";
   analyzer[] = "Constants/Constantnames";
   analyzer[] = "Constants/CustomConstantUsage";
   analyzer[] = "Constants/DynamicCreation";
   analyzer[] = "Constants/IsExtConstant";
   analyzer[] = "Constants/IsPhpConstant";
   analyzer[] = "Constants/MagicConstantUsage";
   analyzer[] = "Constants/MultipleConstantDefinition";
   analyzer[] = "Constants/PhpConstantUsage";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Constants/VariableConstant";
   analyzer[] = "Dump/CallOrder";
   analyzer[] = "Dump/CollectAtomCounts";
   analyzer[] = "Dump/CollectClassChanges";
   analyzer[] = "Dump/CollectClassChildren";
   analyzer[] = "Dump/CollectClassConstantCounts";
   analyzer[] = "Dump/CollectClassDepth";
   analyzer[] = "Dump/CollectClassInterfaceCounts";
   analyzer[] = "Dump/CollectClassTraitsCounts";
   analyzer[] = "Dump/CollectClassesDependencies";
   analyzer[] = "Dump/CollectDefinitionsStats";
   analyzer[] = "Dump/CollectFilesDependencies";
   analyzer[] = "Dump/CollectForeachFavorite";
   analyzer[] = "Dump/CollectGlobalVariables";
   analyzer[] = "Dump/CollectLiterals";
   analyzer[] = "Dump/CollectLocalVariableCounts";
   analyzer[] = "Dump/CollectMbstringEncodings";
   analyzer[] = "Dump/CollectMethodCounts";
   analyzer[] = "Dump/CollectNativeCallsPerExpressions";
   analyzer[] = "Dump/CollectParameterCounts";
   analyzer[] = "Dump/CollectParameterNames";
   analyzer[] = "Dump/CollectPhpStructures";
   analyzer[] = "Dump/CollectPropertyCounts";
   analyzer[] = "Dump/CollectReadability";
   analyzer[] = "Dump/CollectUseCounts";
   analyzer[] = "Dump/CollectVariables";
   analyzer[] = "Dump/ConstantOrder";
   analyzer[] = "Dump/CyclomaticComplexity";
   analyzer[] = "Dump/DereferencingLevels";
   analyzer[] = "Dump/EnvironnementVariables";
   analyzer[] = "Dump/FossilizedMethods";
   analyzer[] = "Dump/Inclusions";
   analyzer[] = "Dump/IndentationLevels";
   analyzer[] = "Dump/NewOrder";
   analyzer[] = "Dump/ParameterArgumentsLinks";
   analyzer[] = "Dump/TypehintingStats";
   analyzer[] = "Dump/Typehintorder";
   analyzer[] = "Exceptions/DefinedExceptions";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/ThrowFunctioncall";
   analyzer[] = "Exceptions/ThrownExceptions";
   analyzer[] = "Exceptions/UselessCatch";
   analyzer[] = "Extensions/Extamqp";
   analyzer[] = "Extensions/Extapache";
   analyzer[] = "Extensions/Extapc";
   analyzer[] = "Extensions/Extapcu";
   analyzer[] = "Extensions/Extarray";
   analyzer[] = "Extensions/Extast";
   analyzer[] = "Extensions/Extbcmath";
   analyzer[] = "Extensions/Extbzip2";
   analyzer[] = "Extensions/Extcalendar";
   analyzer[] = "Extensions/Extcmark";
   analyzer[] = "Extensions/Extcom";
   analyzer[] = "Extensions/Extcrypto";
   analyzer[] = "Extensions/Extctype";
   analyzer[] = "Extensions/Extcurl";
   analyzer[] = "Extensions/Extdate";
   analyzer[] = "Extensions/Extdb2";
   analyzer[] = "Extensions/Extdba";
   analyzer[] = "Extensions/Extdecimal";
   analyzer[] = "Extensions/Extdio";
   analyzer[] = "Extensions/Extdom";
   analyzer[] = "Extensions/Extds";
   analyzer[] = "Extensions/Exteaccelerator";
   analyzer[] = "Extensions/Exteio";
   analyzer[] = "Extensions/Extenchant";
   analyzer[] = "Extensions/Extev";
   analyzer[] = "Extensions/Extevent";
   analyzer[] = "Extensions/Extexif";
   analyzer[] = "Extensions/Extexpect";
   analyzer[] = "Extensions/Extfam";
   analyzer[] = "Extensions/Extfann";
   analyzer[] = "Extensions/Extffi";
   analyzer[] = "Extensions/Extfile";
   analyzer[] = "Extensions/Extfileinfo";
   analyzer[] = "Extensions/Extfilter";
   analyzer[] = "Extensions/Extfpm";
   analyzer[] = "Extensions/Extftp";
   analyzer[] = "Extensions/Extgd";
   analyzer[] = "Extensions/Extgearman";
   analyzer[] = "Extensions/Extgender";
   analyzer[] = "Extensions/Extgeoip";
   analyzer[] = "Extensions/Extgettext";
   analyzer[] = "Extensions/Extgmagick";
   analyzer[] = "Extensions/Extgmp";
   analyzer[] = "Extensions/Extgnupg";
   analyzer[] = "Extensions/Extgrpc";
   analyzer[] = "Extensions/Exthash";
   analyzer[] = "Extensions/Exthrtime";
   analyzer[] = "Extensions/Exthttp";
   analyzer[] = "Extensions/Extibase";
   analyzer[] = "Extensions/Exticonv";
   analyzer[] = "Extensions/Extigbinary";
   analyzer[] = "Extensions/Extimagick";
   analyzer[] = "Extensions/Extimap";
   analyzer[] = "Extensions/Extinfo";
   analyzer[] = "Extensions/Extinotify";
   analyzer[] = "Extensions/Extintl";
   analyzer[] = "Extensions/Extjson";
   analyzer[] = "Extensions/Extjudy";
   analyzer[] = "Extensions/Extldap";
   analyzer[] = "Extensions/Extleveldb";
   analyzer[] = "Extensions/Extlibsodium";
   analyzer[] = "Extensions/Extlibxml";
   analyzer[] = "Extensions/Extlua";
   analyzer[] = "Extensions/Extlzf";
   analyzer[] = "Extensions/Extmail";
   analyzer[] = "Extensions/Extmailparse";
   analyzer[] = "Extensions/Extmath";
   analyzer[] = "Extensions/Extmbstring";
   analyzer[] = "Extensions/Extmcrypt";
   analyzer[] = "Extensions/Extmemcache";
   analyzer[] = "Extensions/Extmemcached";
   analyzer[] = "Extensions/Extmongo";
   analyzer[] = "Extensions/Extmongodb";
   analyzer[] = "Extensions/Extmsgpack";
   analyzer[] = "Extensions/Extmssql";
   analyzer[] = "Extensions/Extmysql";
   analyzer[] = "Extensions/Extmysqli";
   analyzer[] = "Extensions/Extncurses";
   analyzer[] = "Extensions/Extnewt";
   analyzer[] = "Extensions/Extnsapi";
   analyzer[] = "Extensions/Extob";
   analyzer[] = "Extensions/Extoci8";
   analyzer[] = "Extensions/Extodbc";
   analyzer[] = "Extensions/Extopcache";
   analyzer[] = "Extensions/Extopencensus";
   analyzer[] = "Extensions/Extopenssl";
   analyzer[] = "Extensions/Extparle";
   analyzer[] = "Extensions/Extpassword";
   analyzer[] = "Extensions/Extpcntl";
   analyzer[] = "Extensions/Extpcov";
   analyzer[] = "Extensions/Extpcre";
   analyzer[] = "Extensions/Extpdo";
   analyzer[] = "Extensions/Extpgsql";
   analyzer[] = "Extensions/Extphalcon";
   analyzer[] = "Extensions/Extphar";
   analyzer[] = "Extensions/Extposix";
   analyzer[] = "Extensions/Extpspell";
   analyzer[] = "Extensions/Extpsr";
   analyzer[] = "Extensions/Extrar";
   analyzer[] = "Extensions/Extrdkafka";
   analyzer[] = "Extensions/Extreadline";
   analyzer[] = "Extensions/Extredis";
   analyzer[] = "Extensions/Extreflection";
   analyzer[] = "Extensions/Extsdl";
   analyzer[] = "Extensions/Extseaslog";
   analyzer[] = "Extensions/Extsem";
   analyzer[] = "Extensions/Extsession";
   analyzer[] = "Extensions/Extshmop";
   analyzer[] = "Extensions/Extsimplexml";
   analyzer[] = "Extensions/Extsnmp";
   analyzer[] = "Extensions/Extsoap";
   analyzer[] = "Extensions/Extsockets";
   analyzer[] = "Extensions/Extsphinx";
   analyzer[] = "Extensions/Extspl";
   analyzer[] = "Extensions/Extsqlite";
   analyzer[] = "Extensions/Extsqlite3";
   analyzer[] = "Extensions/Extsqlsrv";
   analyzer[] = "Extensions/Extssh2";
   analyzer[] = "Extensions/Extstandard";
   analyzer[] = "Extensions/Extstats";
   analyzer[] = "Extensions/Extstring";
   analyzer[] = "Extensions/Extsuhosin";
   analyzer[] = "Extensions/Extsvm";
   analyzer[] = "Extensions/Extswoole";
   analyzer[] = "Extensions/Exttidy";
   analyzer[] = "Extensions/Exttokenizer";
   analyzer[] = "Extensions/Exttokyotyrant";
   analyzer[] = "Extensions/Exttrader";
   analyzer[] = "Extensions/Extuopz";
   analyzer[] = "Extensions/Extuuid";
   analyzer[] = "Extensions/Extv8js";
   analyzer[] = "Extensions/Extvarnish";
   analyzer[] = "Extensions/Extvips";
   analyzer[] = "Extensions/Extwasm";
   analyzer[] = "Extensions/Extwddx";
   analyzer[] = "Extensions/Extweakref";
   analyzer[] = "Extensions/Extxattr";
   analyzer[] = "Extensions/Extxdebug";
   analyzer[] = "Extensions/Extxdiff";
   analyzer[] = "Extensions/Extxhprof";
   analyzer[] = "Extensions/Extxml";
   analyzer[] = "Extensions/Extxmlreader";
   analyzer[] = "Extensions/Extxmlrpc";
   analyzer[] = "Extensions/Extxmlwriter";
   analyzer[] = "Extensions/Extxsl";
   analyzer[] = "Extensions/Extxxtea";
   analyzer[] = "Extensions/Extyaml";
   analyzer[] = "Extensions/Extzendmonitor";
   analyzer[] = "Extensions/Extzip";
   analyzer[] = "Extensions/Extzlib";
   analyzer[] = "Extensions/Extzmq";
   analyzer[] = "Extensions/Extzookeeper";
   analyzer[] = "Files/IsCliScript";
   analyzer[] = "Files/NotDefinitionsOnly";
   analyzer[] = "Functions/AliasesUsage";
   analyzer[] = "Functions/CallbackNeedsReturn";
   analyzer[] = "Functions/CantUse";
   analyzer[] = "Functions/Closures";
   analyzer[] = "Functions/ConditionedFunctions";
   analyzer[] = "Functions/DeepDefinitions";
   analyzer[] = "Functions/DynamicCode";
   analyzer[] = "Functions/Dynamiccall";
   analyzer[] = "Functions/FallbackFunction";
   analyzer[] = "Functions/Functionnames";
   analyzer[] = "Functions/FunctionsUsingReference";
   analyzer[] = "Functions/IsExtFunction";
   analyzer[] = "Functions/IsGenerator";
   analyzer[] = "Functions/KillsApp";
   analyzer[] = "Functions/MismatchParameterName";
   analyzer[] = "Functions/MultipleDeclarations";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/NoLiteralForReference";
   analyzer[] = "Functions/Recursive";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/ShouldYieldWithKey";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/TypehintedReferences";
   analyzer[] = "Functions/Typehints";
   analyzer[] = "Functions/UnbindingClosures";
   analyzer[] = "Functions/UndefinedFunctions";
   analyzer[] = "Functions/UnknownParameterName";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UseArrowFunctions";
   analyzer[] = "Functions/UseConstantAsArguments";
   analyzer[] = "Functions/UsesDefaultArguments";
   analyzer[] = "Functions/VariableArguments";
   analyzer[] = "Functions/WrongNumberOfArguments";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/Interfacenames";
   analyzer[] = "Interfaces/IsExtInterface";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Namespaces/Alias";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/HiddenUse";
   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
   analyzer[] = "Namespaces/MultipleAliasDefinitions";
   analyzer[] = "Namespaces/NamespaceUsage";
   analyzer[] = "Namespaces/Namespacesnames";
   analyzer[] = "Namespaces/ShouldMakeAlias";
   analyzer[] = "Patterns/CourrierAntiPattern";
   analyzer[] = "Patterns/DependencyInjection";
   analyzer[] = "Patterns/Factory";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/StrposTooMuch";
   analyzer[] = "Performances/UseArraySlice";
   analyzer[] = "Php/AlternativeSyntax";
   analyzer[] = "Php/Argon2Usage";
   analyzer[] = "Php/ArrayKeyExistsWithObjects";
   analyzer[] = "Php/AssertionUsage";
   analyzer[] = "Php/AssignAnd";
   analyzer[] = "Php/AutoloadUsage";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/CastUnsetUsage";
   analyzer[] = "Php/CastingUsage";
   analyzer[] = "Php/Coalesce";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/CryptoUsage";
   analyzer[] = "Php/DeclareEncoding";
   analyzer[] = "Php/DeclareStrict";
   analyzer[] = "Php/DeclareStrictType";
   analyzer[] = "Php/DeclareTicks";
   analyzer[] = "Php/Deprecated";
   analyzer[] = "Php/DetectCurrentClass";
   analyzer[] = "Php/DirectivesUsage";
   analyzer[] = "Php/DlUsage";
   analyzer[] = "Php/EchoTagUsage";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/ErrorLogUsage";
   analyzer[] = "Php/FilterToAddSlashes";
   analyzer[] = "Php/FopenMode";
   analyzer[] = "Php/Gotonames";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/Haltcompiler";
   analyzer[] = "Php/HashAlgos74";
   analyzer[] = "Php/IdnUts46";
   analyzer[] = "Php/Incompilable";
   analyzer[] = "Php/IntegerSeparatorUsage";
   analyzer[] = "Php/InternalParameterType";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Php/IsINF";
   analyzer[] = "Php/IsNAN";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/Labelnames";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/MiddleVersion";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NoClassInGlobal";
   analyzer[] = "Php/NoMoreCurlyArrays";
   analyzer[] = "Php/NoReferenceForTernary";
   analyzer[] = "Php/OveriddenFunction";
   analyzer[] = "Php/PearUsage";
   analyzer[] = "Php/Php74Deprecation";
   analyzer[] = "Php/Php74NewClasses";
   analyzer[] = "Php/Php74NewConstants";
   analyzer[] = "Php/Php74NewFunctions";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php74RemovedFunctions";
   analyzer[] = "Php/Php74ReservedKeyword";
   analyzer[] = "Php/Php74mbstrrpos3rdArg";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php80NamedParameterVariadic";
   analyzer[] = "Php/Php80NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80RemovedConstant";
   analyzer[] = "Php/Php80RemovedDirective";
   analyzer[] = "Php/Php80RemovedFunctions";
   analyzer[] = "Php/Php80RemovesResources";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php80VariableSyntax";
   analyzer[] = "Php/PhpErrorMsgUsage";
   analyzer[] = "Php/RawPostDataUsage";
   analyzer[] = "Php/ReflectionExportIsDeprecated";
   analyzer[] = "Php/ReturnTypehintUsage";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/ScalarTypehintUsage";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/SpreadOperatorForArray";
   analyzer[] = "Php/StrtrArguments";
   analyzer[] = "Php/SuperGlobalUsage";
   analyzer[] = "Php/ThrowUsage";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TriggerErrorUsage";
   analyzer[] = "Php/TryCatchUsage";
   analyzer[] = "Php/TryMultipleCatch";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UseAttributes";
   analyzer[] = "Php/UseBrowscap";
   analyzer[] = "Php/UseCli";
   analyzer[] = "Php/UseContravariance";
   analyzer[] = "Php/UseCookies";
   analyzer[] = "Php/UseCovariance";
   analyzer[] = "Php/UseMatch";
   analyzer[] = "Php/UseNullSafeOperator";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/UseObjectApi";
   analyzer[] = "Php/UsePathinfo";
   analyzer[] = "Php/UseTrailingUseComma";
   analyzer[] = "Php/UseWeb";
   analyzer[] = "Php/UsesEnv";
   analyzer[] = "Php/WrongTypeForNativeFunction";
   analyzer[] = "Php/YieldFromUsage";
   analyzer[] = "Php/YieldUsage";
   analyzer[] = "Psr/Psr11Usage";
   analyzer[] = "Psr/Psr13Usage";
   analyzer[] = "Psr/Psr16Usage";
   analyzer[] = "Psr/Psr3Usage";
   analyzer[] = "Psr/Psr6Usage";
   analyzer[] = "Psr/Psr7Usage";
   analyzer[] = "Security/CantDisableClass";
   analyzer[] = "Security/CantDisableFunction";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Structures/AddZero";
   analyzer[] = "Structures/AlteringForeachWithoutReference";
   analyzer[] = "Structures/ArrayMapPassesByValue";
   analyzer[] = "Structures/AssigneAndCompare";
   analyzer[] = "Structures/AutoUnsetForeach";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/CastingTernary";
   analyzer[] = "Structures/CheckJson";
   analyzer[] = "Structures/CoalesceAndConcat";
   analyzer[] = "Structures/ComplexExpression";
   analyzer[] = "Structures/ConstDefineFavorite";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/CurlVersionNow";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/DirThenSlash";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/DynamicCalls";
   analyzer[] = "Structures/DynamicCode";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/ElseUsage";
   analyzer[] = "Structures/EmptyBlocks";
   analyzer[] = "Structures/ErrorMessages";
   analyzer[] = "Structures/ErrorReportingWithInteger";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/FileUploadUsage";
   analyzer[] = "Structures/FileUsage";
   analyzer[] = "Structures/ForeachReferenceIsNotModified";
   analyzer[] = "Structures/ForgottenWhiteSpace";
   analyzer[] = "Structures/FunctionSubscripting";
   analyzer[] = "Structures/GlobalInGlobal";
   analyzer[] = "Structures/GlobalUsage";
   analyzer[] = "Structures/Htmlentitiescall";
   analyzer[] = "Structures/IdenticalConditions";
   analyzer[] = "Structures/IdenticalOnBothSides";
   analyzer[] = "Structures/IfWithSameConditions";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/ImplodeArgsOrder";
   analyzer[] = "Structures/IncludeUsage";
   analyzer[] = "Structures/IndicesAreIntOrString";
   analyzer[] = "Structures/InvalidPackFormat";
   analyzer[] = "Structures/InvalidRegex";
   analyzer[] = "Structures/IsZero";
   analyzer[] = "Structures/ListOmissions";
   analyzer[] = "Structures/LogicalMistakes";
   analyzer[] = "Structures/LoneBlock";
   analyzer[] = "Structures/MailUsage";
   analyzer[] = "Structures/MbstringThirdArg";
   analyzer[] = "Structures/MbstringUnknownEncoding";
   analyzer[] = "Structures/MergeIfThen";
   analyzer[] = "Structures/MissingParenthesis";
   analyzer[] = "Structures/MultipleCatch";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultiplyByOne";
   analyzer[] = "Structures/NegativePow";
   analyzer[] = "Structures/NestedLoops";
   analyzer[] = "Structures/NestedTernary";
   analyzer[] = "Structures/NeverNegative";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoDirectAccess";
   analyzer[] = "Structures/NoEmptyRegex";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoReferenceOnLeft";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/NonBreakableSpaceInNames";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/NotEqual";
   analyzer[] = "Structures/NotNot";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/OnceUsage";
   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";
   analyzer[] = "Structures/OrDie";
   analyzer[] = "Structures/PrintAndDie";
   analyzer[] = "Structures/PrintWithoutParenthesis";
   analyzer[] = "Structures/PrintfArguments";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/RepeatedRegex";
   analyzer[] = "Structures/ResourcesUsage";
   analyzer[] = "Structures/ResultMayBeMissing";
   analyzer[] = "Structures/ReturnTrueFalse";
   analyzer[] = "Structures/SameConditions";
   analyzer[] = "Structures/ShellUsage";
   analyzer[] = "Structures/ShortTags";
   analyzer[] = "Structures/ShouldChainException";
   analyzer[] = "Structures/ShouldMakeTernary";
   analyzer[] = "Structures/ShouldUseExplodeArgs";
   analyzer[] = "Structures/StripTagsSkipsClosedTag";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/SwitchWithoutDefault";
   analyzer[] = "Structures/TernaryInConcat";
   analyzer[] = "Structures/ThrowsAndAssign";
   analyzer[] = "Structures/TimestampDifference";
   analyzer[] = "Structures/TryFinally";
   analyzer[] = "Structures/UncheckedResources";
   analyzer[] = "Structures/UnconditionLoopBreak";
   analyzer[] = "Structures/UnknownPregOption";
   analyzer[] = "Structures/UnsupportedTypesWithOperators";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UseDebug";
   analyzer[] = "Structures/UseInstanceof";
   analyzer[] = "Structures/UseSystemTmp";
   analyzer[] = "Structures/UselessBrackets";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Structures/UselessCheck";
   analyzer[] = "Structures/UselessInstruction";
   analyzer[] = "Structures/UselessParenthesis";
   analyzer[] = "Structures/UselessUnset";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Traits/IsExtTrait";
   analyzer[] = "Traits/Php";
   analyzer[] = "Traits/TraitUsage";
   analyzer[] = "Traits/Traitnames";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Type/ArrayIndex";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/Email";
   analyzer[] = "Type/GPCIndex";
   analyzer[] = "Type/Heredoc";
   analyzer[] = "Type/Hexadecimal";
   analyzer[] = "Type/Md5String";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Type/Nowdoc";
   analyzer[] = "Type/Octal";
   analyzer[] = "Type/OneVariableStrings";
   analyzer[] = "Type/Pack";
   analyzer[] = "Type/Path";
   analyzer[] = "Type/Printf";
   analyzer[] = "Type/Protocols";
   analyzer[] = "Type/Regex";
   analyzer[] = "Type/Shellcommands";
   analyzer[] = "Type/ShouldTypecast";
   analyzer[] = "Type/SilentlyCastInteger";
   analyzer[] = "Type/Sql";
   analyzer[] = "Type/StringWithStrangeSpace";
   analyzer[] = "Type/Url";
   analyzer[] = "Typehints/CouldBeArray";
   analyzer[] = "Typehints/CouldBeBoolean";
   analyzer[] = "Typehints/CouldBeCIT";
   analyzer[] = "Typehints/CouldBeFloat";
   analyzer[] = "Typehints/CouldBeInt";
   analyzer[] = "Typehints/CouldBeNull";
   analyzer[] = "Typehints/CouldBeString";
   analyzer[] = "Typehints/MissingReturntype";
   analyzer[] = "Variables/References";
   analyzer[] = "Variables/SelfTransform";
   analyzer[] = "Variables/StaticVariables";
   analyzer[] = "Variables/UncommonEnvVar";
   analyzer[] = "Variables/UndefinedVariable";
   analyzer[] = "Variables/VariableLong";
   analyzer[] = "Variables/VariableUsedOnceByContext";
   analyzer[] = "Variables/VariableVariables";
   analyzer[] = "Vendors/Codeigniter";
   analyzer[] = "Vendors/Concrete5";
   analyzer[] = "Vendors/Drupal";
   analyzer[] = "Vendors/Fuel";
   analyzer[] = "Vendors/Joomla";
   analyzer[] = "Vendors/Laravel";
   analyzer[] = "Vendors/Phalcon";
   analyzer[] = "Vendors/Symfony";
   analyzer[] = "Vendors/Typo3";
   analyzer[] = "Vendors/Wordpress";
   analyzer[] = "Vendors/Yii";


.. _annex-yaml-ce:

CE for .exakat.yaml
+++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CE':
     - 'Arrays/ArrayNSUsage'
     - 'Arrays/Arrayindex'
     - 'Arrays/Multidimensional'
     - 'Arrays/MultipleIdenticalKeys'
     - 'Arrays/NegativeStart'
     - 'Arrays/Phparrayindex'
     - 'Arrays/WithCallback'
     - 'Classes/Abstractclass'
     - 'Classes/Abstractmethods'
     - 'Classes/Anonymous'
     - 'Classes/CheckOnCallUsage'
     - 'Classes/ClassAliasUsage'
     - 'Classes/Classnames'
     - 'Classes/CloningUsage'
     - 'Classes/ConstantClass'
     - 'Classes/ConstantDefinition'
     - 'Classes/DefinedConstants'
     - 'Classes/DefinedProperty'
     - 'Classes/DirectCallToMagicMethod'
     - 'Classes/DontUnsetProperties'
     - 'Classes/DynamicClass'
     - 'Classes/DynamicConstantCall'
     - 'Classes/DynamicMethodCall'
     - 'Classes/DynamicNew'
     - 'Classes/DynamicPropertyCall'
     - 'Classes/FinalPrivate'
     - 'Classes/HasMagicProperty'
     - 'Classes/ImmutableSignature'
     - 'Classes/IsNotFamily'
     - 'Classes/IsaMagicProperty'
     - 'Classes/MagicMethod'
     - 'Classes/MultipleClassesInFile'
     - 'Classes/MultipleDeclarations'
     - 'Classes/MultipleTraitOrInterface'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoParent'
     - 'Classes/NonPpp'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/OldStyleConstructor'
     - 'Classes/OverwrittenConst'
     - 'Classes/RedefinedConstants'
     - 'Classes/RedefinedDefault'
     - 'Classes/RedefinedMethods'
     - 'Classes/StaticContainsThis'
     - 'Classes/StaticMethods'
     - 'Classes/StaticMethodsCalledFromObject'
     - 'Classes/StaticProperties'
     - 'Classes/TestClass'
     - 'Classes/ThrowInDestruct'
     - 'Classes/UndeclaredStaticProperty'
     - 'Classes/UndefinedConstants'
     - 'Classes/UndefinedProperty'
     - 'Classes/UndefinedStaticclass'
     - 'Classes/UseClassOperator'
     - 'Classes/UseInstanceof'
     - 'Classes/UselessFinal'
     - 'Classes/VariableClasses'
     - 'Classes/WrongTypedPropertyInit'
     - 'Complete/CreateCompactVariables'
     - 'Complete/CreateMagicProperty'
     - 'Complete/FollowClosureDefinition'
     - 'Complete/MakeClassConstantDefinition'
     - 'Complete/MakeFunctioncallWithReference'
     - 'Complete/OverwrittenConstants'
     - 'Complete/OverwrittenProperties'
     - 'Complete/SetArrayClassDefinition'
     - 'Complete/SetParentDefinition'
     - 'Composer/Autoload'
     - 'Composer/UseComposer'
     - 'Composer/UseComposerLock'
     - 'Constants/CaseInsensitiveConstants'
     - 'Constants/ConstRecommended'
     - 'Constants/ConstantStrangeNames'
     - 'Constants/ConstantUsage'
     - 'Constants/Constantnames'
     - 'Constants/CustomConstantUsage'
     - 'Constants/DynamicCreation'
     - 'Constants/IsExtConstant'
     - 'Constants/IsPhpConstant'
     - 'Constants/MagicConstantUsage'
     - 'Constants/MultipleConstantDefinition'
     - 'Constants/PhpConstantUsage'
     - 'Constants/UndefinedConstants'
     - 'Constants/VariableConstant'
     - 'Dump/CallOrder'
     - 'Dump/CollectAtomCounts'
     - 'Dump/CollectClassChanges'
     - 'Dump/CollectClassChildren'
     - 'Dump/CollectClassConstantCounts'
     - 'Dump/CollectClassDepth'
     - 'Dump/CollectClassInterfaceCounts'
     - 'Dump/CollectClassTraitsCounts'
     - 'Dump/CollectClassesDependencies'
     - 'Dump/CollectDefinitionsStats'
     - 'Dump/CollectFilesDependencies'
     - 'Dump/CollectForeachFavorite'
     - 'Dump/CollectGlobalVariables'
     - 'Dump/CollectLiterals'
     - 'Dump/CollectLocalVariableCounts'
     - 'Dump/CollectMbstringEncodings'
     - 'Dump/CollectMethodCounts'
     - 'Dump/CollectNativeCallsPerExpressions'
     - 'Dump/CollectParameterCounts'
     - 'Dump/CollectParameterNames'
     - 'Dump/CollectPhpStructures'
     - 'Dump/CollectPropertyCounts'
     - 'Dump/CollectReadability'
     - 'Dump/CollectUseCounts'
     - 'Dump/CollectVariables'
     - 'Dump/ConstantOrder'
     - 'Dump/CyclomaticComplexity'
     - 'Dump/DereferencingLevels'
     - 'Dump/EnvironnementVariables'
     - 'Dump/FossilizedMethods'
     - 'Dump/Inclusions'
     - 'Dump/IndentationLevels'
     - 'Dump/NewOrder'
     - 'Dump/ParameterArgumentsLinks'
     - 'Dump/TypehintingStats'
     - 'Dump/Typehintorder'
     - 'Exceptions/DefinedExceptions'
     - 'Exceptions/MultipleCatch'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/ThrowFunctioncall'
     - 'Exceptions/ThrownExceptions'
     - 'Exceptions/UselessCatch'
     - 'Extensions/Extamqp'
     - 'Extensions/Extapache'
     - 'Extensions/Extapc'
     - 'Extensions/Extapcu'
     - 'Extensions/Extarray'
     - 'Extensions/Extast'
     - 'Extensions/Extbcmath'
     - 'Extensions/Extbzip2'
     - 'Extensions/Extcalendar'
     - 'Extensions/Extcmark'
     - 'Extensions/Extcom'
     - 'Extensions/Extcrypto'
     - 'Extensions/Extctype'
     - 'Extensions/Extcurl'
     - 'Extensions/Extdate'
     - 'Extensions/Extdb2'
     - 'Extensions/Extdba'
     - 'Extensions/Extdecimal'
     - 'Extensions/Extdio'
     - 'Extensions/Extdom'
     - 'Extensions/Extds'
     - 'Extensions/Exteaccelerator'
     - 'Extensions/Exteio'
     - 'Extensions/Extenchant'
     - 'Extensions/Extev'
     - 'Extensions/Extevent'
     - 'Extensions/Extexif'
     - 'Extensions/Extexpect'
     - 'Extensions/Extfam'
     - 'Extensions/Extfann'
     - 'Extensions/Extffi'
     - 'Extensions/Extfile'
     - 'Extensions/Extfileinfo'
     - 'Extensions/Extfilter'
     - 'Extensions/Extfpm'
     - 'Extensions/Extftp'
     - 'Extensions/Extgd'
     - 'Extensions/Extgearman'
     - 'Extensions/Extgender'
     - 'Extensions/Extgeoip'
     - 'Extensions/Extgettext'
     - 'Extensions/Extgmagick'
     - 'Extensions/Extgmp'
     - 'Extensions/Extgnupg'
     - 'Extensions/Extgrpc'
     - 'Extensions/Exthash'
     - 'Extensions/Exthrtime'
     - 'Extensions/Exthttp'
     - 'Extensions/Extibase'
     - 'Extensions/Exticonv'
     - 'Extensions/Extigbinary'
     - 'Extensions/Extimagick'
     - 'Extensions/Extimap'
     - 'Extensions/Extinfo'
     - 'Extensions/Extinotify'
     - 'Extensions/Extintl'
     - 'Extensions/Extjson'
     - 'Extensions/Extjudy'
     - 'Extensions/Extldap'
     - 'Extensions/Extleveldb'
     - 'Extensions/Extlibsodium'
     - 'Extensions/Extlibxml'
     - 'Extensions/Extlua'
     - 'Extensions/Extlzf'
     - 'Extensions/Extmail'
     - 'Extensions/Extmailparse'
     - 'Extensions/Extmath'
     - 'Extensions/Extmbstring'
     - 'Extensions/Extmcrypt'
     - 'Extensions/Extmemcache'
     - 'Extensions/Extmemcached'
     - 'Extensions/Extmongo'
     - 'Extensions/Extmongodb'
     - 'Extensions/Extmsgpack'
     - 'Extensions/Extmssql'
     - 'Extensions/Extmysql'
     - 'Extensions/Extmysqli'
     - 'Extensions/Extncurses'
     - 'Extensions/Extnewt'
     - 'Extensions/Extnsapi'
     - 'Extensions/Extob'
     - 'Extensions/Extoci8'
     - 'Extensions/Extodbc'
     - 'Extensions/Extopcache'
     - 'Extensions/Extopencensus'
     - 'Extensions/Extopenssl'
     - 'Extensions/Extparle'
     - 'Extensions/Extpassword'
     - 'Extensions/Extpcntl'
     - 'Extensions/Extpcov'
     - 'Extensions/Extpcre'
     - 'Extensions/Extpdo'
     - 'Extensions/Extpgsql'
     - 'Extensions/Extphalcon'
     - 'Extensions/Extphar'
     - 'Extensions/Extposix'
     - 'Extensions/Extpspell'
     - 'Extensions/Extpsr'
     - 'Extensions/Extrar'
     - 'Extensions/Extrdkafka'
     - 'Extensions/Extreadline'
     - 'Extensions/Extredis'
     - 'Extensions/Extreflection'
     - 'Extensions/Extsdl'
     - 'Extensions/Extseaslog'
     - 'Extensions/Extsem'
     - 'Extensions/Extsession'
     - 'Extensions/Extshmop'
     - 'Extensions/Extsimplexml'
     - 'Extensions/Extsnmp'
     - 'Extensions/Extsoap'
     - 'Extensions/Extsockets'
     - 'Extensions/Extsphinx'
     - 'Extensions/Extspl'
     - 'Extensions/Extsqlite'
     - 'Extensions/Extsqlite3'
     - 'Extensions/Extsqlsrv'
     - 'Extensions/Extssh2'
     - 'Extensions/Extstandard'
     - 'Extensions/Extstats'
     - 'Extensions/Extstring'
     - 'Extensions/Extsuhosin'
     - 'Extensions/Extsvm'
     - 'Extensions/Extswoole'
     - 'Extensions/Exttidy'
     - 'Extensions/Exttokenizer'
     - 'Extensions/Exttokyotyrant'
     - 'Extensions/Exttrader'
     - 'Extensions/Extuopz'
     - 'Extensions/Extuuid'
     - 'Extensions/Extv8js'
     - 'Extensions/Extvarnish'
     - 'Extensions/Extvips'
     - 'Extensions/Extwasm'
     - 'Extensions/Extwddx'
     - 'Extensions/Extweakref'
     - 'Extensions/Extxattr'
     - 'Extensions/Extxdebug'
     - 'Extensions/Extxdiff'
     - 'Extensions/Extxhprof'
     - 'Extensions/Extxml'
     - 'Extensions/Extxmlreader'
     - 'Extensions/Extxmlrpc'
     - 'Extensions/Extxmlwriter'
     - 'Extensions/Extxsl'
     - 'Extensions/Extxxtea'
     - 'Extensions/Extyaml'
     - 'Extensions/Extzendmonitor'
     - 'Extensions/Extzip'
     - 'Extensions/Extzlib'
     - 'Extensions/Extzmq'
     - 'Extensions/Extzookeeper'
     - 'Files/IsCliScript'
     - 'Files/NotDefinitionsOnly'
     - 'Functions/AliasesUsage'
     - 'Functions/CallbackNeedsReturn'
     - 'Functions/CantUse'
     - 'Functions/Closures'
     - 'Functions/ConditionedFunctions'
     - 'Functions/DeepDefinitions'
     - 'Functions/DynamicCode'
     - 'Functions/Dynamiccall'
     - 'Functions/FallbackFunction'
     - 'Functions/Functionnames'
     - 'Functions/FunctionsUsingReference'
     - 'Functions/IsExtFunction'
     - 'Functions/IsGenerator'
     - 'Functions/KillsApp'
     - 'Functions/MismatchParameterName'
     - 'Functions/MultipleDeclarations'
     - 'Functions/MustReturn'
     - 'Functions/NoLiteralForReference'
     - 'Functions/Recursive'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/ShouldYieldWithKey'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/TypehintedReferences'
     - 'Functions/Typehints'
     - 'Functions/UnbindingClosures'
     - 'Functions/UndefinedFunctions'
     - 'Functions/UnknownParameterName'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UseArrowFunctions'
     - 'Functions/UseConstantAsArguments'
     - 'Functions/UsesDefaultArguments'
     - 'Functions/VariableArguments'
     - 'Functions/WrongNumberOfArguments'
     - 'Functions/WrongOptionalParameter'
     - 'Functions/WrongReturnedType'
     - 'Functions/WrongTypeWithCall'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/Interfacenames'
     - 'Interfaces/IsExtInterface'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/UndefinedInterfaces'
     - 'Namespaces/Alias'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/HiddenUse'
     - 'Namespaces/MultipleAliasDefinitionPerFile'
     - 'Namespaces/MultipleAliasDefinitions'
     - 'Namespaces/NamespaceUsage'
     - 'Namespaces/Namespacesnames'
     - 'Namespaces/ShouldMakeAlias'
     - 'Patterns/CourrierAntiPattern'
     - 'Patterns/DependencyInjection'
     - 'Patterns/Factory'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/PrePostIncrement'
     - 'Performances/StrposTooMuch'
     - 'Performances/UseArraySlice'
     - 'Php/AlternativeSyntax'
     - 'Php/Argon2Usage'
     - 'Php/ArrayKeyExistsWithObjects'
     - 'Php/AssertionUsage'
     - 'Php/AssignAnd'
     - 'Php/AutoloadUsage'
     - 'Php/BetterRand'
     - 'Php/CastUnsetUsage'
     - 'Php/CastingUsage'
     - 'Php/Coalesce'
     - 'Php/ConcatAndAddition'
     - 'Php/CryptoUsage'
     - 'Php/DeclareEncoding'
     - 'Php/DeclareStrict'
     - 'Php/DeclareStrictType'
     - 'Php/DeclareTicks'
     - 'Php/Deprecated'
     - 'Php/DetectCurrentClass'
     - 'Php/DirectivesUsage'
     - 'Php/DlUsage'
     - 'Php/EchoTagUsage'
     - 'Php/EllipsisUsage'
     - 'Php/ErrorLogUsage'
     - 'Php/FilterToAddSlashes'
     - 'Php/FopenMode'
     - 'Php/Gotonames'
     - 'Php/GroupUseDeclaration'
     - 'Php/Haltcompiler'
     - 'Php/HashAlgos74'
     - 'Php/IdnUts46'
     - 'Php/Incompilable'
     - 'Php/IntegerSeparatorUsage'
     - 'Php/InternalParameterType'
     - 'Php/IsAWithString'
     - 'Php/IsINF'
     - 'Php/IsNAN'
     - 'Php/IsnullVsEqualNull'
     - 'Php/Labelnames'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/LogicalInLetters'
     - 'Php/MiddleVersion'
     - 'Php/MissingSubpattern'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NoClassInGlobal'
     - 'Php/NoMoreCurlyArrays'
     - 'Php/NoReferenceForTernary'
     - 'Php/OveriddenFunction'
     - 'Php/PearUsage'
     - 'Php/Php74Deprecation'
     - 'Php/Php74NewClasses'
     - 'Php/Php74NewConstants'
     - 'Php/Php74NewFunctions'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php74RemovedFunctions'
     - 'Php/Php74ReservedKeyword'
     - 'Php/Php74mbstrrpos3rdArg'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php80NamedParameterVariadic'
     - 'Php/Php80NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80RemovedConstant'
     - 'Php/Php80RemovedDirective'
     - 'Php/Php80RemovedFunctions'
     - 'Php/Php80RemovesResources'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php80VariableSyntax'
     - 'Php/PhpErrorMsgUsage'
     - 'Php/RawPostDataUsage'
     - 'Php/ReflectionExportIsDeprecated'
     - 'Php/ReturnTypehintUsage'
     - 'Php/ScalarAreNotArrays'
     - 'Php/ScalarTypehintUsage'
     - 'Php/ShouldUseCoalesce'
     - 'Php/SignatureTrailingComma'
     - 'Php/SpreadOperatorForArray'
     - 'Php/StrtrArguments'
     - 'Php/SuperGlobalUsage'
     - 'Php/ThrowUsage'
     - 'Php/ThrowWasAnExpression'
     - 'Php/TrailingComma'
     - 'Php/TriggerErrorUsage'
     - 'Php/TryCatchUsage'
     - 'Php/TryMultipleCatch'
     - 'Php/TypedPropertyUsage'
     - 'Php/UseAttributes'
     - 'Php/UseBrowscap'
     - 'Php/UseCli'
     - 'Php/UseContravariance'
     - 'Php/UseCookies'
     - 'Php/UseCovariance'
     - 'Php/UseMatch'
     - 'Php/UseNullSafeOperator'
     - 'Php/UseNullableType'
     - 'Php/UseObjectApi'
     - 'Php/UsePathinfo'
     - 'Php/UseTrailingUseComma'
     - 'Php/UseWeb'
     - 'Php/UsesEnv'
     - 'Php/WrongTypeForNativeFunction'
     - 'Php/YieldFromUsage'
     - 'Php/YieldUsage'
     - 'Psr/Psr11Usage'
     - 'Psr/Psr13Usage'
     - 'Psr/Psr16Usage'
     - 'Psr/Psr3Usage'
     - 'Psr/Psr6Usage'
     - 'Psr/Psr7Usage'
     - 'Security/CantDisableClass'
     - 'Security/CantDisableFunction'
     - 'Security/DontEchoError'
     - 'Security/ShouldUsePreparedStatement'
     - 'Structures/AddZero'
     - 'Structures/AlteringForeachWithoutReference'
     - 'Structures/ArrayMapPassesByValue'
     - 'Structures/AssigneAndCompare'
     - 'Structures/AutoUnsetForeach'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/CastingTernary'
     - 'Structures/CheckJson'
     - 'Structures/CoalesceAndConcat'
     - 'Structures/ComplexExpression'
     - 'Structures/ConstDefineFavorite'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/CurlVersionNow'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/DereferencingAS'
     - 'Structures/DirThenSlash'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/DynamicCalls'
     - 'Structures/DynamicCode'
     - 'Structures/ElseIfElseif'
     - 'Structures/ElseUsage'
     - 'Structures/EmptyBlocks'
     - 'Structures/ErrorMessages'
     - 'Structures/ErrorReportingWithInteger'
     - 'Structures/EvalUsage'
     - 'Structures/EvalWithoutTry'
     - 'Structures/ExitUsage'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/FileUploadUsage'
     - 'Structures/FileUsage'
     - 'Structures/ForeachReferenceIsNotModified'
     - 'Structures/ForgottenWhiteSpace'
     - 'Structures/FunctionSubscripting'
     - 'Structures/GlobalInGlobal'
     - 'Structures/GlobalUsage'
     - 'Structures/Htmlentitiescall'
     - 'Structures/IdenticalConditions'
     - 'Structures/IdenticalOnBothSides'
     - 'Structures/IfWithSameConditions'
     - 'Structures/ImpliedIf'
     - 'Structures/ImplodeArgsOrder'
     - 'Structures/IncludeUsage'
     - 'Structures/IndicesAreIntOrString'
     - 'Structures/InvalidPackFormat'
     - 'Structures/InvalidRegex'
     - 'Structures/IsZero'
     - 'Structures/ListOmissions'
     - 'Structures/LogicalMistakes'
     - 'Structures/LoneBlock'
     - 'Structures/MailUsage'
     - 'Structures/MbstringThirdArg'
     - 'Structures/MbstringUnknownEncoding'
     - 'Structures/MergeIfThen'
     - 'Structures/MissingParenthesis'
     - 'Structures/MultipleCatch'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultiplyByOne'
     - 'Structures/NegativePow'
     - 'Structures/NestedLoops'
     - 'Structures/NestedTernary'
     - 'Structures/NeverNegative'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoChoice'
     - 'Structures/NoDirectAccess'
     - 'Structures/NoEmptyRegex'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoReferenceOnLeft'
     - 'Structures/NoSubstrOne'
     - 'Structures/NonBreakableSpaceInNames'
     - 'Structures/Noscream'
     - 'Structures/NotEqual'
     - 'Structures/NotNot'
     - 'Structures/ObjectReferences'
     - 'Structures/OnceUsage'
     - 'Structures/OpensslRandomPseudoByteSecondArg'
     - 'Structures/OrDie'
     - 'Structures/PrintAndDie'
     - 'Structures/PrintWithoutParenthesis'
     - 'Structures/PrintfArguments'
     - 'Structures/RepeatedPrint'
     - 'Structures/RepeatedRegex'
     - 'Structures/ResourcesUsage'
     - 'Structures/ResultMayBeMissing'
     - 'Structures/ReturnTrueFalse'
     - 'Structures/SameConditions'
     - 'Structures/ShellUsage'
     - 'Structures/ShortTags'
     - 'Structures/ShouldChainException'
     - 'Structures/ShouldMakeTernary'
     - 'Structures/ShouldUseExplodeArgs'
     - 'Structures/StripTagsSkipsClosedTag'
     - 'Structures/StrposCompare'
     - 'Structures/SwitchWithoutDefault'
     - 'Structures/TernaryInConcat'
     - 'Structures/ThrowsAndAssign'
     - 'Structures/TimestampDifference'
     - 'Structures/TryFinally'
     - 'Structures/UncheckedResources'
     - 'Structures/UnconditionLoopBreak'
     - 'Structures/UnknownPregOption'
     - 'Structures/UnsupportedTypesWithOperators'
     - 'Structures/UseConstant'
     - 'Structures/UseDebug'
     - 'Structures/UseInstanceof'
     - 'Structures/UseSystemTmp'
     - 'Structures/UselessBrackets'
     - 'Structures/UselessCasting'
     - 'Structures/UselessCheck'
     - 'Structures/UselessInstruction'
     - 'Structures/UselessParenthesis'
     - 'Structures/UselessUnset'
     - 'Structures/VardumpUsage'
     - 'Structures/WhileListEach'
     - 'Structures/pregOptionE'
     - 'Traits/IsExtTrait'
     - 'Traits/Php'
     - 'Traits/TraitUsage'
     - 'Traits/Traitnames'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UselessAlias'
     - 'Type/ArrayIndex'
     - 'Type/Binary'
     - 'Type/Email'
     - 'Type/GPCIndex'
     - 'Type/Heredoc'
     - 'Type/Hexadecimal'
     - 'Type/Md5String'
     - 'Type/NoRealComparison'
     - 'Type/Nowdoc'
     - 'Type/Octal'
     - 'Type/OneVariableStrings'
     - 'Type/Pack'
     - 'Type/Path'
     - 'Type/Printf'
     - 'Type/Protocols'
     - 'Type/Regex'
     - 'Type/Shellcommands'
     - 'Type/ShouldTypecast'
     - 'Type/SilentlyCastInteger'
     - 'Type/Sql'
     - 'Type/StringWithStrangeSpace'
     - 'Type/Url'
     - 'Typehints/CouldBeArray'
     - 'Typehints/CouldBeBoolean'
     - 'Typehints/CouldBeCIT'
     - 'Typehints/CouldBeFloat'
     - 'Typehints/CouldBeInt'
     - 'Typehints/CouldBeNull'
     - 'Typehints/CouldBeString'
     - 'Typehints/MissingReturntype'
     - 'Variables/References'
     - 'Variables/SelfTransform'
     - 'Variables/StaticVariables'
     - 'Variables/UncommonEnvVar'
     - 'Variables/UndefinedVariable'
     - 'Variables/VariableLong'
     - 'Variables/VariableUsedOnceByContext'
     - 'Variables/VariableVariables'
     - 'Vendors/Codeigniter'
     - 'Vendors/Concrete5'
     - 'Vendors/Drupal'
     - 'Vendors/Fuel'
     - 'Vendors/Joomla'
     - 'Vendors/Laravel'
     - 'Vendors/Phalcon'
     - 'Vendors/Symfony'
     - 'Vendors/Typo3'
     - 'Vendors/Wordpress'
     - 'Vendors/Yii'




.. _annex-ci-checks:

CI-checks
#########


.. _annex-ini-ci-checks:

CI-checks for INI
+++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CI-checks]
   analyzer[] = "Arrays/MultipleIdenticalKeys";
   analyzer[] = "Classes/CheckOnCallUsage";
   analyzer[] = "Classes/DirectCallToMagicMethod";
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/MultipleDeclarations";
   analyzer[] = "Classes/MultipleTraitOrInterface";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NonPpp";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/RedefinedConstants";
   analyzer[] = "Classes/RedefinedDefault";
   analyzer[] = "Classes/StaticContainsThis";
   analyzer[] = "Classes/StaticMethodsCalledFromObject";
   analyzer[] = "Classes/ThrowInDestruct";
   analyzer[] = "Classes/UndeclaredStaticProperty";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Classes/UndefinedStaticclass";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Classes/UseInstanceof";
   analyzer[] = "Classes/UselessFinal";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Constants/ConstantStrangeNames";
   analyzer[] = "Constants/MultipleConstantDefinition";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/ThrowFunctioncall";
   analyzer[] = "Functions/AliasesUsage";
   analyzer[] = "Functions/CallbackNeedsReturn";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/NoLiteralForReference";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/ShouldYieldWithKey";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/TypehintedReferences";
   analyzer[] = "Functions/UndefinedFunctions";
   analyzer[] = "Functions/UnknownParameterName";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UseConstantAsArguments";
   analyzer[] = "Functions/UsesDefaultArguments";
   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
   analyzer[] = "Functions/WrongNumberOfArguments";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/HiddenUse";
   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
   analyzer[] = "Namespaces/MultipleAliasDefinitions";
   analyzer[] = "Namespaces/ShouldMakeAlias";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/StrposTooMuch";
   analyzer[] = "Performances/UseArraySlice";
   analyzer[] = "Php/AssignAnd";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/Deprecated";
   analyzer[] = "Php/FopenMode";
   analyzer[] = "Php/InternalParameterType";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Php/NoClassInGlobal";
   analyzer[] = "Php/NoReferenceForTernary";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/StrtrArguments";
   analyzer[] = "Php/UseObjectApi";
   analyzer[] = "Php/UsePathinfo";
   analyzer[] = "Php/WrongTypeForNativeFunction";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Structures/AddZero";
   analyzer[] = "Structures/AlteringForeachWithoutReference";
   analyzer[] = "Structures/AssigneAndCompare";
   analyzer[] = "Structures/AutoUnsetForeach";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/CastingTernary";
   analyzer[] = "Structures/CheckJson";
   analyzer[] = "Structures/CoalesceAndConcat";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/DirThenSlash";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/EmptyBlocks";
   analyzer[] = "Structures/ErrorReportingWithInteger";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/ForeachReferenceIsNotModified";
   analyzer[] = "Structures/ForgottenWhiteSpace";
   analyzer[] = "Structures/Htmlentitiescall";
   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
   analyzer[] = "Structures/IdenticalConditions";
   analyzer[] = "Structures/IdenticalOnBothSides";
   analyzer[] = "Structures/IfWithSameConditions";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/ImplodeArgsOrder";
   analyzer[] = "Structures/IndicesAreIntOrString";
   analyzer[] = "Structures/InvalidPackFormat";
   analyzer[] = "Structures/InvalidRegex";
   analyzer[] = "Structures/IsZero";
   analyzer[] = "Structures/ListOmissions";
   analyzer[] = "Structures/LogicalMistakes";
   analyzer[] = "Structures/LoneBlock";
   analyzer[] = "Structures/MbstringThirdArg";
   analyzer[] = "Structures/MbstringUnknownEncoding";
   analyzer[] = "Structures/MergeIfThen";
   analyzer[] = "Structures/MissingParenthesis";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultiplyByOne";
   analyzer[] = "Structures/NegativePow";
   analyzer[] = "Structures/NestedTernary";
   analyzer[] = "Structures/NeverNegative";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoEmptyRegex";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoReferenceOnLeft";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/NotEqual";
   analyzer[] = "Structures/NotNot";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/OrDie";
   analyzer[] = "Structures/PrintAndDie";
   analyzer[] = "Structures/PrintWithoutParenthesis";
   analyzer[] = "Structures/PrintfArguments";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/RepeatedRegex";
   analyzer[] = "Structures/ResultMayBeMissing";
   analyzer[] = "Structures/ReturnTrueFalse";
   analyzer[] = "Structures/SameConditions";
   analyzer[] = "Structures/ShouldChainException";
   analyzer[] = "Structures/ShouldMakeTernary";
   analyzer[] = "Structures/ShouldUseExplodeArgs";
   analyzer[] = "Structures/StripTagsSkipsClosedTag";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/SwitchWithoutDefault";
   analyzer[] = "Structures/TernaryInConcat";
   analyzer[] = "Structures/ThrowsAndAssign";
   analyzer[] = "Structures/TimestampDifference";
   analyzer[] = "Structures/UncheckedResources";
   analyzer[] = "Structures/UnconditionLoopBreak";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UseInstanceof";
   analyzer[] = "Structures/UseSystemTmp";
   analyzer[] = "Structures/UselessBrackets";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Structures/UselessCheck";
   analyzer[] = "Structures/UselessInstruction";
   analyzer[] = "Structures/UselessParenthesis";
   analyzer[] = "Structures/UselessUnset";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Type/OneVariableStrings";
   analyzer[] = "Type/ShouldTypecast";
   analyzer[] = "Type/SilentlyCastInteger";
   analyzer[] = "Type/StringWithStrangeSpace";
   analyzer[] = "Typehints/MissingReturntype";
   analyzer[] = "Variables/UndefinedVariable";


.. _annex-yaml-ci-checks:

CI-checks for .exakat.yaml
++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CI-checks':
     - 'Arrays/MultipleIdenticalKeys'
     - 'Classes/CheckOnCallUsage'
     - 'Classes/DirectCallToMagicMethod'
     - 'Classes/DontUnsetProperties'
     - 'Classes/MultipleDeclarations'
     - 'Classes/MultipleTraitOrInterface'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoParent'
     - 'Classes/NonPpp'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/RedefinedConstants'
     - 'Classes/RedefinedDefault'
     - 'Classes/StaticContainsThis'
     - 'Classes/StaticMethodsCalledFromObject'
     - 'Classes/ThrowInDestruct'
     - 'Classes/UndeclaredStaticProperty'
     - 'Classes/UndefinedConstants'
     - 'Classes/UndefinedProperty'
     - 'Classes/UndefinedStaticclass'
     - 'Classes/UseClassOperator'
     - 'Classes/UseInstanceof'
     - 'Classes/UselessFinal'
     - 'Classes/WrongTypedPropertyInit'
     - 'Constants/ConstRecommended'
     - 'Constants/ConstantStrangeNames'
     - 'Constants/MultipleConstantDefinition'
     - 'Constants/UndefinedConstants'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/ThrowFunctioncall'
     - 'Functions/AliasesUsage'
     - 'Functions/CallbackNeedsReturn'
     - 'Functions/MustReturn'
     - 'Functions/NoLiteralForReference'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/ShouldYieldWithKey'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/TypehintedReferences'
     - 'Functions/UndefinedFunctions'
     - 'Functions/UnknownParameterName'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UseConstantAsArguments'
     - 'Functions/UsesDefaultArguments'
     - 'Functions/WrongArgumentNameWithPhpFunction'
     - 'Functions/WrongNumberOfArguments'
     - 'Functions/WrongOptionalParameter'
     - 'Functions/WrongReturnedType'
     - 'Functions/WrongTypeWithCall'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/UndefinedInterfaces'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/HiddenUse'
     - 'Namespaces/MultipleAliasDefinitionPerFile'
     - 'Namespaces/MultipleAliasDefinitions'
     - 'Namespaces/ShouldMakeAlias'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/PrePostIncrement'
     - 'Performances/StrposTooMuch'
     - 'Performances/UseArraySlice'
     - 'Php/AssignAnd'
     - 'Php/BetterRand'
     - 'Php/ConcatAndAddition'
     - 'Php/Deprecated'
     - 'Php/FopenMode'
     - 'Php/InternalParameterType'
     - 'Php/IsAWithString'
     - 'Php/IsnullVsEqualNull'
     - 'Php/LogicalInLetters'
     - 'Php/MissingSubpattern'
     - 'Php/NoClassInGlobal'
     - 'Php/NoReferenceForTernary'
     - 'Php/ScalarAreNotArrays'
     - 'Php/ShouldUseCoalesce'
     - 'Php/StrtrArguments'
     - 'Php/UseObjectApi'
     - 'Php/UsePathinfo'
     - 'Php/WrongTypeForNativeFunction'
     - 'Security/DontEchoError'
     - 'Security/ShouldUsePreparedStatement'
     - 'Structures/AddZero'
     - 'Structures/AlteringForeachWithoutReference'
     - 'Structures/AssigneAndCompare'
     - 'Structures/AutoUnsetForeach'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/CastingTernary'
     - 'Structures/CheckJson'
     - 'Structures/CoalesceAndConcat'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/DirThenSlash'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/ElseIfElseif'
     - 'Structures/EmptyBlocks'
     - 'Structures/ErrorReportingWithInteger'
     - 'Structures/EvalWithoutTry'
     - 'Structures/ExitUsage'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/ForeachReferenceIsNotModified'
     - 'Structures/ForgottenWhiteSpace'
     - 'Structures/Htmlentitiescall'
     - 'Structures/HtmlentitiescallDefaultFlag'
     - 'Structures/IdenticalConditions'
     - 'Structures/IdenticalOnBothSides'
     - 'Structures/IfWithSameConditions'
     - 'Structures/ImpliedIf'
     - 'Structures/ImplodeArgsOrder'
     - 'Structures/IndicesAreIntOrString'
     - 'Structures/InvalidPackFormat'
     - 'Structures/InvalidRegex'
     - 'Structures/IsZero'
     - 'Structures/ListOmissions'
     - 'Structures/LogicalMistakes'
     - 'Structures/LoneBlock'
     - 'Structures/MbstringThirdArg'
     - 'Structures/MbstringUnknownEncoding'
     - 'Structures/MergeIfThen'
     - 'Structures/MissingParenthesis'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultiplyByOne'
     - 'Structures/NegativePow'
     - 'Structures/NestedTernary'
     - 'Structures/NeverNegative'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoChoice'
     - 'Structures/NoEmptyRegex'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoReferenceOnLeft'
     - 'Structures/NoSubstrOne'
     - 'Structures/Noscream'
     - 'Structures/NotEqual'
     - 'Structures/NotNot'
     - 'Structures/ObjectReferences'
     - 'Structures/OrDie'
     - 'Structures/PrintAndDie'
     - 'Structures/PrintWithoutParenthesis'
     - 'Structures/PrintfArguments'
     - 'Structures/RepeatedPrint'
     - 'Structures/RepeatedRegex'
     - 'Structures/ResultMayBeMissing'
     - 'Structures/ReturnTrueFalse'
     - 'Structures/SameConditions'
     - 'Structures/ShouldChainException'
     - 'Structures/ShouldMakeTernary'
     - 'Structures/ShouldUseExplodeArgs'
     - 'Structures/StripTagsSkipsClosedTag'
     - 'Structures/StrposCompare'
     - 'Structures/SwitchWithoutDefault'
     - 'Structures/TernaryInConcat'
     - 'Structures/ThrowsAndAssign'
     - 'Structures/TimestampDifference'
     - 'Structures/UncheckedResources'
     - 'Structures/UnconditionLoopBreak'
     - 'Structures/UseConstant'
     - 'Structures/UseInstanceof'
     - 'Structures/UseSystemTmp'
     - 'Structures/UselessBrackets'
     - 'Structures/UselessCasting'
     - 'Structures/UselessCheck'
     - 'Structures/UselessInstruction'
     - 'Structures/UselessParenthesis'
     - 'Structures/UselessUnset'
     - 'Structures/VardumpUsage'
     - 'Structures/WhileListEach'
     - 'Structures/pregOptionE'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UselessAlias'
     - 'Type/NoRealComparison'
     - 'Type/OneVariableStrings'
     - 'Type/ShouldTypecast'
     - 'Type/SilentlyCastInteger'
     - 'Type/StringWithStrangeSpace'
     - 'Typehints/MissingReturntype'
     - 'Variables/UndefinedVariable'




.. _annex-changed-behavior:

Changed Behavior
################


.. _annex-ini-changed-behavior:

Changed Behavior for INI
++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Changed Behavior]
   analyzer[] = "Arrays/AmbiguousKeys";
   analyzer[] = "Arrays/AppendAndAssignArrays";
   analyzer[] = "Arrays/ArrayNSUsage";
   analyzer[] = "Arrays/Arrayindex";
   analyzer[] = "Arrays/EmptySlots";
   analyzer[] = "Arrays/FloatConversionAsIndex";
   analyzer[] = "Arrays/GettingLastElement";
   analyzer[] = "Arrays/MassCreation";
   analyzer[] = "Arrays/NegativeStart";
   analyzer[] = "Arrays/NoSpreadForHash";
   analyzer[] = "Arrays/NonConstantArray";
   analyzer[] = "Arrays/WeakType";
   analyzer[] = "Arrays/WeirdIndex";
   analyzer[] = "Arrays/WithCallback";
   analyzer[] = "Attributes/Deprecated";
   analyzer[] = "Attributes/Friend";
   analyzer[] = "Attributes/InjectableVersion";
   analyzer[] = "Attributes/MissingAttributeAttribute";
   analyzer[] = "Attributes/ModifyImmutable";
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Attributes/PhpNativeAttributes";
   analyzer[] = "Attributes/UselessOverride";
   analyzer[] = "Classes/AbstractConstants";
   analyzer[] = "Classes/AbstractOrImplements";
   analyzer[] = "Classes/AbstractStatic";
   analyzer[] = "Classes/Abstractclass";
   analyzer[] = "Classes/Abstractmethods";
   analyzer[] = "Classes/AccessPrivate";
   analyzer[] = "Classes/AccessProtected";
   analyzer[] = "Classes/AmbiguousStatic";
   analyzer[] = "Classes/AmbiguousVisibilities";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/AvoidOptionArrays";
   analyzer[] = "Classes/AvoidOptionalProperties";
   analyzer[] = "Classes/CancelCommonMethod";
   analyzer[] = "Classes/CannotBeReadonly";
   analyzer[] = "Classes/CantExtendFinal";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/CantInstantiateClass";
   analyzer[] = "Classes/CheckAfterNullSafeOperator";
   analyzer[] = "Classes/CheckOnCallUsage";
   analyzer[] = "Classes/ChecksPropertyExistence";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/CitSameName";
   analyzer[] = "Classes/ClassAliasUsage";
   analyzer[] = "Classes/ClassInvasion";
   analyzer[] = "Classes/ClassOverreach";
   analyzer[] = "Classes/ClassUsage";
   analyzer[] = "Classes/Classnames";
   analyzer[] = "Classes/CloneWithNonObject";
   analyzer[] = "Classes/CloningUsage";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/ConstantClass";
   analyzer[] = "Classes/ConstantDefinition";
   analyzer[] = "Classes/ConstantUsedBelow";
   analyzer[] = "Classes/Constructor";
   analyzer[] = "Classes/CouldBeAbstractClass";
   analyzer[] = "Classes/CouldBeAbstractMethod";
   analyzer[] = "Classes/CouldBeFinal";
   analyzer[] = "Classes/CouldBeIterable";
   analyzer[] = "Classes/CouldBeParentMethod";
   analyzer[] = "Classes/CouldBePrivate";
   analyzer[] = "Classes/CouldBePrivateConstante";
   analyzer[] = "Classes/CouldBePrivateMethod";
   analyzer[] = "Classes/CouldBeProtectedConstant";
   analyzer[] = "Classes/CouldBeProtectedMethod";
   analyzer[] = "Classes/CouldBeProtectedProperty";
   analyzer[] = "Classes/CouldBeReadonly";
   analyzer[] = "Classes/CouldBeReadonlyProperty";
   analyzer[] = "Classes/CouldBeStatic";
   analyzer[] = "Classes/CouldBeStringable";
   analyzer[] = "Classes/CouldInjectParam";
   analyzer[] = "Classes/CouldSetPropertyDefault";
   analyzer[] = "Classes/CouldUseClassOperator";
   analyzer[] = "Classes/CyclicReferences";
   analyzer[] = "Classes/DefinedConstants";
   analyzer[] = "Classes/DefinedParentMP";
   analyzer[] = "Classes/DefinedProperty";
   analyzer[] = "Classes/DefinedStaticMP";
   analyzer[] = "Classes/DemeterLaw";
   analyzer[] = "Classes/DependantAbstractClass";
   analyzer[] = "Classes/DifferentArgumentCounts";
   analyzer[] = "Classes/DisconnectedClasses";
   analyzer[] = "Classes/DontSendThisInConstructor";
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/DynamicClass";
   analyzer[] = "Classes/DynamicMethodCall";
   analyzer[] = "Classes/DynamicNew";
   analyzer[] = "Classes/DynamicPropertyCall";
   analyzer[] = "Classes/DynamicSelfCalls";
   analyzer[] = "Classes/EmptyClass";
   analyzer[] = "Classes/ExportProperty";
   analyzer[] = "Classes/ExtendsStdclass";
   analyzer[] = "Classes/FinalByOcramius";
   analyzer[] = "Classes/Finalclass";
   analyzer[] = "Classes/Finalmethod";
   analyzer[] = "Classes/FossilizedMethod";
   analyzer[] = "Classes/HasMagicProperty";
   analyzer[] = "Classes/HiddenNullable";
   analyzer[] = "Classes/IdenticalMethods";
   analyzer[] = "Classes/ImmutableSignature";
   analyzer[] = "Classes/ImplementIsForInterface";
   analyzer[] = "Classes/ImplementedMethodsArePublic";
   analyzer[] = "Classes/IncompatibleConstructor";
   analyzer[] = "Classes/IncompatibleSignature";
   analyzer[] = "Classes/IncompatibleSignature74";
   analyzer[] = "Classes/InheritedPropertyMustMatch";
   analyzer[] = "Classes/InsufficientPropertyTypehint";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/IsExtClass";
   analyzer[] = "Classes/IsInterfaceMethod";
   analyzer[] = "Classes/IsNotFamily";
   analyzer[] = "Classes/IsUpperFamily";
   analyzer[] = "Classes/LocallyUnusedProperty";
   analyzer[] = "Classes/LocallyUsedProperty";
   analyzer[] = "Classes/LoweredAccessLevel";
   analyzer[] = "Classes/MagicMethod";
   analyzer[] = "Classes/MagicMethodReturntypes";
   analyzer[] = "Classes/MakeDefault";
   analyzer[] = "Classes/MakeGlobalAProperty";
   analyzer[] = "Classes/MakeMagicConcrete";
   analyzer[] = "Classes/MethodIsOverwritten";
   analyzer[] = "Classes/MethodPropertyConfusion";
   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
   analyzer[] = "Classes/MethodUsedBelow";
   analyzer[] = "Classes/MismatchProperties";
   analyzer[] = "Classes/MissingVisibility";
   analyzer[] = "Classes/MultipleDeclarations";
   analyzer[] = "Classes/MultiplePropertyDeclaration";
   analyzer[] = "Classes/MultiplePropertyDeclarationOnOneLine";
   analyzer[] = "Classes/MultipleTraitOrInterface";
   analyzer[] = "Classes/MutualExtension";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoNullWithNullSafeOperator";
   analyzer[] = "Classes/NoPSSOutsideClass";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NoPublicAccess";
   analyzer[] = "Classes/NoReadonlyAssignationInGlobal";
   analyzer[] = "Classes/NoSelfReferencingConstant";
   analyzer[] = "Classes/NonNullableSetters";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NormalMethods";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/OldStyleVar";
   analyzer[] = "Classes/OneObjectOperatorPerLine";
   analyzer[] = "Classes/OnlyStaticMethods";
   analyzer[] = "Classes/OrderOfDeclaration";
   analyzer[] = "Classes/OverwrittenConst";
   analyzer[] = "Classes/PPPDeclarationStyle";
   analyzer[] = "Classes/ParentFirst";
   analyzer[] = "Classes/ParentIsNotStatic";
   analyzer[] = "Classes/PromotedProperties";
   analyzer[] = "Classes/PropertyCouldBeLocal";
   analyzer[] = "Classes/PropertyDefinition";
   analyzer[] = "Classes/PropertyInvasion";
   analyzer[] = "Classes/PropertyMethodSameName";
   analyzer[] = "Classes/PropertyNeverUsed";
   analyzer[] = "Classes/PropertyUsedAbove";
   analyzer[] = "Classes/PropertyUsedInOneMethodOnly";
   analyzer[] = "Classes/PropertyUsedInternally";
   analyzer[] = "Classes/PssWithoutClass";
   analyzer[] = "Classes/RaisedAccessLevel";
   analyzer[] = "Classes/ReadonlyUsage";
   analyzer[] = "Classes/RedefinedConstants";
   analyzer[] = "Classes/RedefinedDefault";
   analyzer[] = "Classes/RedefinedMethods";
   analyzer[] = "Classes/RedefinedPrivateProperty";
   analyzer[] = "Classes/RedefinedProperty";
   analyzer[] = "Classes/RewroteFinalClassConstant";
   analyzer[] = "Classes/SameNameAsFile";
   analyzer[] = "Classes/ShouldDeepClone";
   analyzer[] = "Classes/ShouldHaveDestructor";
   analyzer[] = "Classes/ShouldUseSelf";
   analyzer[] = "Classes/ShouldUseThis";
   analyzer[] = "Classes/StaticContainsThis";
   analyzer[] = "Classes/StaticMethods";
   analyzer[] = "Classes/StaticMethodsCalledFromObject";
   analyzer[] = "Classes/StaticProperties";
   analyzer[] = "Classes/StrangeName";
   analyzer[] = "Classes/SwappedArguments";
   analyzer[] = "Classes/TestClass";
   analyzer[] = "Classes/ThisIsForClasses";
   analyzer[] = "Classes/ThisIsNotAnArray";
   analyzer[] = "Classes/TooManyDereferencing";
   analyzer[] = "Classes/TooManyFinds";
   analyzer[] = "Classes/TooManyInjections";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Classes/TypehintCyclicDependencies";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UndefinedMethod";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Classes/UndefinedStaticMP";
   analyzer[] = "Classes/UndefinedStaticclass";
   analyzer[] = "Classes/UnfinishedObject";
   analyzer[] = "Classes/UninitedProperty";
   analyzer[] = "Classes/UnitializedProperties";
   analyzer[] = "Classes/UnreachableConstant";
   analyzer[] = "Classes/UnreachableMethod";
   analyzer[] = "Classes/UnresolvedCatch";
   analyzer[] = "Classes/UnresolvedClasses";
   analyzer[] = "Classes/UnresolvedInstanceof";
   analyzer[] = "Classes/UnusedClass";
   analyzer[] = "Classes/UnusedConstant";
   analyzer[] = "Classes/UnusedMethods";
   analyzer[] = "Classes/UnusedPrivateMethod";
   analyzer[] = "Classes/UnusedProtectedMethods";
   analyzer[] = "Classes/UnusedPublicMethod";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Classes/UseInstanceof";
   analyzer[] = "Classes/UseThis";
   analyzer[] = "Classes/UsedClass";
   analyzer[] = "Classes/UsedMethods";
   analyzer[] = "Classes/UsedOnceProperty";
   analyzer[] = "Classes/UsedPrivateMethod";
   analyzer[] = "Classes/UsedProtectedMethod";
   analyzer[] = "Classes/UselessAbstract";
   analyzer[] = "Classes/UselessAssignationOfPromotedProperty";
   analyzer[] = "Classes/UselessConstantOverwrite";
   analyzer[] = "Classes/UselessConstructor";
   analyzer[] = "Classes/UselessFinal";
   analyzer[] = "Classes/UselessMethod";
   analyzer[] = "Classes/UselessNullSafeOperator";
   analyzer[] = "Classes/UselessTypehint";
   analyzer[] = "Classes/UsingThisOutsideAClass";
   analyzer[] = "Classes/VariableClasses";
   analyzer[] = "Classes/WeakType";
   analyzer[] = "Classes/toStringPss";
   analyzer[] = "Complete/CreateCompactVariables";
   analyzer[] = "Complete/CreateDefaultValues";
   analyzer[] = "Complete/CreateForeachDefault";
   analyzer[] = "Complete/CreateMagicMethod";
   analyzer[] = "Complete/CreateMagicProperty";
   analyzer[] = "Complete/EnumCaseValues";
   analyzer[] = "Complete/ExtendedTypehints";
   analyzer[] = "Complete/FollowClosureDefinition";
   analyzer[] = "Complete/GlobalDefinitions";
   analyzer[] = "Complete/IsExtStructure";
   analyzer[] = "Complete/IsPhpStructure";
   analyzer[] = "Complete/MakeAllStatics";
   analyzer[] = "Complete/MakeClassConstantDefinition";
   analyzer[] = "Complete/MakeClassMethodDefinition";
   analyzer[] = "Complete/OverwrittenProperties";
   analyzer[] = "Complete/PhpExtStubPropertyMethod";
   analyzer[] = "Complete/PhpNativeReference";
   analyzer[] = "Complete/PropagateConstants";
   analyzer[] = "Complete/ReturnTypehint";
   analyzer[] = "Complete/SetArrayClassDefinition";
   analyzer[] = "Complete/SetClassMethodRemoteDefinition";
   analyzer[] = "Complete/SetClassPropertyDefinitionWithTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithGlobal";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithInjection";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithLocalNew";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithReturnTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithTypehint";
   analyzer[] = "Complete/SetCloneLink";
   analyzer[] = "Complete/SetMethodFnp";
   analyzer[] = "Complete/SetParentDefinition";
   analyzer[] = "Complete/SolveTraitConstants";
   analyzer[] = "Complete/SolveTraitMethods";
   analyzer[] = "Complete/Superglobals";
   analyzer[] = "Complete/VariableTypehint";
   analyzer[] = "Composer/Autoload";
   analyzer[] = "Composer/UseComposer";
   analyzer[] = "Composer/UseComposerLock";
   analyzer[] = "Constants/ConditionedConstants";
   analyzer[] = "Constants/ConstDefinePreference";
   analyzer[] = "Constants/ConstantUsedOnce";
   analyzer[] = "Constants/CouldUseConstant";
   analyzer[] = "Constants/CreatedOutsideItsNamespace";
   analyzer[] = "Constants/CustomConstantUsage";
   analyzer[] = "Constants/DefineInsensitivePreference";
   analyzer[] = "Constants/DynamicCreation";
   analyzer[] = "Constants/InconsistantCase";
   analyzer[] = "Constants/InvalidName";
   analyzer[] = "Constants/IsExtConstant";
   analyzer[] = "Constants/IsGlobalConstant";
   analyzer[] = "Constants/IsPhpConstant";
   analyzer[] = "Constants/MagicConstantUsage";
   analyzer[] = "Constants/MultipleConstantDefinition";
   analyzer[] = "Constants/PhpConstantUsage";
   analyzer[] = "Constants/RelayConstant";
   analyzer[] = "Constants/StrangeName";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Constants/UnusedConstants";
   analyzer[] = "Constants/VariableConstant";
   analyzer[] = "Custom/MethodUsage";
   analyzer[] = "Dump/ArgumentCountsPerCalls";
   analyzer[] = "Dump/CallOrder";
   analyzer[] = "Dump/ClassInjectionCount";
   analyzer[] = "Dump/CollectAtomCounts";
   analyzer[] = "Dump/CollectBlockSize";
   analyzer[] = "Dump/CollectCalls";
   analyzer[] = "Dump/CollectCatch";
   analyzer[] = "Dump/CollectClassChanges";
   analyzer[] = "Dump/CollectClassChildren";
   analyzer[] = "Dump/CollectClassConstantCounts";
   analyzer[] = "Dump/CollectClassDepth";
   analyzer[] = "Dump/CollectClassInterfaceCounts";
   analyzer[] = "Dump/CollectClassTraitsCounts";
   analyzer[] = "Dump/CollectClassesDependencies";
   analyzer[] = "Dump/CollectDefinitionsStats";
   analyzer[] = "Dump/CollectDependencyExtension";
   analyzer[] = "Dump/CollectFilesDependencies";
   analyzer[] = "Dump/CollectForeachFavorite";
   analyzer[] = "Dump/CollectGlobalVariables";
   analyzer[] = "Dump/CollectGraphTriplets";
   analyzer[] = "Dump/CollectLiterals";
   analyzer[] = "Dump/CollectLocalVariableCounts";
   analyzer[] = "Dump/CollectMbstringEncodings";
   analyzer[] = "Dump/CollectMethodCounts";
   analyzer[] = "Dump/CollectMethodsThrowingExceptions";
   analyzer[] = "Dump/CollectNativeCallsPerExpressions";
   analyzer[] = "Dump/CollectParameterCounts";
   analyzer[] = "Dump/CollectParameterNames";
   analyzer[] = "Dump/CollectPhpStructures";
   analyzer[] = "Dump/CollectPropertyCounts";
   analyzer[] = "Dump/CollectPropertyUsage";
   analyzer[] = "Dump/CollectReadability";
   analyzer[] = "Dump/CollectSetLocale";
   analyzer[] = "Dump/CollectStructures";
   analyzer[] = "Dump/CollectStubStructures";
   analyzer[] = "Dump/CollectThrow";
   analyzer[] = "Dump/CollectUseCounts";
   analyzer[] = "Dump/CollectVariables";
   analyzer[] = "Dump/CollectVendorStructures";
   analyzer[] = "Dump/CollectsNames";
   analyzer[] = "Dump/CombinedCalls";
   analyzer[] = "Dump/ConstantOrder";
   analyzer[] = "Dump/CouldBeAConstant";
   analyzer[] = "Dump/CyclomaticComplexity";
   analyzer[] = "Dump/DereferencingLevels";
   analyzer[] = "Dump/DumpComparedLiterals";
   analyzer[] = "Dump/EnvironnementVariables";
   analyzer[] = "Dump/FossilizedMethods";
   analyzer[] = "Dump/Inclusions";
   analyzer[] = "Dump/IndentationLevels";
   analyzer[] = "Dump/NewOrder";
   analyzer[] = "Dump/ParameterArgumentsLinks";
   analyzer[] = "Dump/PublicReach";
   analyzer[] = "Dump/TypehintingStats";
   analyzer[] = "Dump/Typehintorder";
   analyzer[] = "Enums/CouldBeEnum";
   analyzer[] = "Enums/NoMagicMethod";
   analyzer[] = "Enums/UndefinedEnumcase";
   analyzer[] = "Enums/UnusedEnumCase";
   analyzer[] = "Exceptions/AlreadyCaught";
   analyzer[] = "Exceptions/CantThrow";
   analyzer[] = "Exceptions/CatchE";
   analyzer[] = "Exceptions/CatchUndefinedVariable";
   analyzer[] = "Exceptions/CaughtButNotThrown";
   analyzer[] = "Exceptions/CaughtExceptions";
   analyzer[] = "Exceptions/ConvertedExceptions";
   analyzer[] = "Exceptions/CouldDropVariable";
   analyzer[] = "Exceptions/DefinedExceptions";
   analyzer[] = "Exceptions/ForgottenThrown";
   analyzer[] = "Exceptions/IsPhpException";
   analyzer[] = "Exceptions/LargeTryBlock";
   analyzer[] = "Exceptions/LongPreparation";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/PossibleTypeError";
   analyzer[] = "Exceptions/Rethrown";
   analyzer[] = "Exceptions/SetChainingException";
   analyzer[] = "Exceptions/ThrowFunctioncall";
   analyzer[] = "Exceptions/ThrowRawExceptions";
   analyzer[] = "Exceptions/TryNoCatch";
   analyzer[] = "Exceptions/UncaughtExceptions";
   analyzer[] = "Exceptions/Unthrown";
   analyzer[] = "Exceptions/UnusedExceptionVariable";
   analyzer[] = "Exceptions/UselessCatch";
   analyzer[] = "Exceptions/UselessTry";
   analyzer[] = "Extensions/Extamqp";
   analyzer[] = "Extensions/Extapache";
   analyzer[] = "Extensions/Extapc";
   analyzer[] = "Extensions/Extapcu";
   analyzer[] = "Extensions/Extarray";
   analyzer[] = "Extensions/Extast";
   analyzer[] = "Extensions/Extbcmath";
   analyzer[] = "Extensions/Extbzip2";
   analyzer[] = "Extensions/Extcalendar";
   analyzer[] = "Extensions/Extcmark";
   analyzer[] = "Extensions/Extcom";
   analyzer[] = "Extensions/Extcrypto";
   analyzer[] = "Extensions/Extcsv";
   analyzer[] = "Extensions/Extctype";
   analyzer[] = "Extensions/Extcurl";
   analyzer[] = "Extensions/Extdate";
   analyzer[] = "Extensions/Extdb2";
   analyzer[] = "Extensions/Extdba";
   analyzer[] = "Extensions/Extdecimal";
   analyzer[] = "Extensions/Extdio";
   analyzer[] = "Extensions/Extdom";
   analyzer[] = "Extensions/Extds";
   analyzer[] = "Extensions/Exteio";
   analyzer[] = "Extensions/Extenchant";
   analyzer[] = "Extensions/Extev";
   analyzer[] = "Extensions/Extevent";
   analyzer[] = "Extensions/Extexcimer";
   analyzer[] = "Extensions/Extexif";
   analyzer[] = "Extensions/Extexpect";
   analyzer[] = "Extensions/Extfam";
   analyzer[] = "Extensions/Extfann";
   analyzer[] = "Extensions/Extffi";
   analyzer[] = "Extensions/Extfile";
   analyzer[] = "Extensions/Extfileinfo";
   analyzer[] = "Extensions/Extfilter";
   analyzer[] = "Extensions/Extfpm";
   analyzer[] = "Extensions/Extftp";
   analyzer[] = "Extensions/Extgd";
   analyzer[] = "Extensions/Extgearman";
   analyzer[] = "Extensions/Extgender";
   analyzer[] = "Extensions/Extgeoip";
   analyzer[] = "Extensions/Extgeospatial";
   analyzer[] = "Extensions/Extgettext";
   analyzer[] = "Extensions/Extgmagick";
   analyzer[] = "Extensions/Extgmp";
   analyzer[] = "Extensions/Extgnupg";
   analyzer[] = "Extensions/Extgrpc";
   analyzer[] = "Extensions/Exthash";
   analyzer[] = "Extensions/Exthrtime";
   analyzer[] = "Extensions/Exthttp";
   analyzer[] = "Extensions/Extibase";
   analyzer[] = "Extensions/Extice";
   analyzer[] = "Extensions/Exticonv";
   analyzer[] = "Extensions/Extigbinary";
   analyzer[] = "Extensions/Extimagick";
   analyzer[] = "Extensions/Extimap";
   analyzer[] = "Extensions/Extinfo";
   analyzer[] = "Extensions/Extinotify";
   analyzer[] = "Extensions/Extintl";
   analyzer[] = "Extensions/Extjson";
   analyzer[] = "Extensions/Extjudy";
   analyzer[] = "Extensions/Extldap";
   analyzer[] = "Extensions/Extleveldb";
   analyzer[] = "Extensions/Extlibsodium";
   analyzer[] = "Extensions/Extlibxml";
   analyzer[] = "Extensions/Extlua";
   analyzer[] = "Extensions/Extlzf";
   analyzer[] = "Extensions/Extmail";
   analyzer[] = "Extensions/Extmailparse";
   analyzer[] = "Extensions/Extmath";
   analyzer[] = "Extensions/Extmbstring";
   analyzer[] = "Extensions/Extmcrypt";
   analyzer[] = "Extensions/Extmemcache";
   analyzer[] = "Extensions/Extmemcached";
   analyzer[] = "Extensions/Extmongo";
   analyzer[] = "Extensions/Extmongodb";
   analyzer[] = "Extensions/Extmsgpack";
   analyzer[] = "Extensions/Extmssql";
   analyzer[] = "Extensions/Extmysqli";
   analyzer[] = "Extensions/Extncurses";
   analyzer[] = "Extensions/Extnewt";
   analyzer[] = "Extensions/Extnsapi";
   analyzer[] = "Extensions/Extob";
   analyzer[] = "Extensions/Extoci8";
   analyzer[] = "Extensions/Extodbc";
   analyzer[] = "Extensions/Extopcache";
   analyzer[] = "Extensions/Extopencensus";
   analyzer[] = "Extensions/Extopenssl";
   analyzer[] = "Extensions/Extparle";
   analyzer[] = "Extensions/Extpassword";
   analyzer[] = "Extensions/Extpcntl";
   analyzer[] = "Extensions/Extpcov";
   analyzer[] = "Extensions/Extpcre";
   analyzer[] = "Extensions/Extpdo";
   analyzer[] = "Extensions/Extpgsql";
   analyzer[] = "Extensions/Extphalcon";
   analyzer[] = "Extensions/Extphar";
   analyzer[] = "Extensions/Extpkcs11";
   analyzer[] = "Extensions/Extposix";
   analyzer[] = "Extensions/Extprotobuf";
   analyzer[] = "Extensions/Extpspell";
   analyzer[] = "Extensions/Extpsr";
   analyzer[] = "Extensions/Extrandom";
   analyzer[] = "Extensions/Extrar";
   analyzer[] = "Extensions/Extrdkafka";
   analyzer[] = "Extensions/Extreadline";
   analyzer[] = "Extensions/Extredis";
   analyzer[] = "Extensions/Extreflection";
   analyzer[] = "Extensions/Extsdl";
   analyzer[] = "Extensions/Extseaslog";
   analyzer[] = "Extensions/Extsem";
   analyzer[] = "Extensions/Extsession";
   analyzer[] = "Extensions/Extshmop";
   analyzer[] = "Extensions/Extsimplexml";
   analyzer[] = "Extensions/Extsnmp";
   analyzer[] = "Extensions/Extsoap";
   analyzer[] = "Extensions/Extsockets";
   analyzer[] = "Extensions/Extsphinx";
   analyzer[] = "Extensions/Extspl";
   analyzer[] = "Extensions/Extspx";
   analyzer[] = "Extensions/Extsqlite";
   analyzer[] = "Extensions/Extsqlite3";
   analyzer[] = "Extensions/Extsqlsrv";
   analyzer[] = "Extensions/Extssh2";
   analyzer[] = "Extensions/Extstandard";
   analyzer[] = "Extensions/Extstats";
   analyzer[] = "Extensions/Extstomp";
   analyzer[] = "Extensions/Extstring";
   analyzer[] = "Extensions/Extsuhosin";
   analyzer[] = "Extensions/Extsvm";
   analyzer[] = "Extensions/Extswoole";
   analyzer[] = "Extensions/Exttaint";
   analyzer[] = "Extensions/Exttidy";
   analyzer[] = "Extensions/Exttokenizer";
   analyzer[] = "Extensions/Exttokyotyrant";
   analyzer[] = "Extensions/Exttrader";
   analyzer[] = "Extensions/Extuopz";
   analyzer[] = "Extensions/Extuuid";
   analyzer[] = "Extensions/Extv8js";
   analyzer[] = "Extensions/Extvarnish";
   analyzer[] = "Extensions/Extvips";
   analyzer[] = "Extensions/Extwasm";
   analyzer[] = "Extensions/Extwddx";
   analyzer[] = "Extensions/Extweakref";
   analyzer[] = "Extensions/Extxattr";
   analyzer[] = "Extensions/Extxdebug";
   analyzer[] = "Extensions/Extxdiff";
   analyzer[] = "Extensions/Extxhprof";
   analyzer[] = "Extensions/Extxml";
   analyzer[] = "Extensions/Extxmlrpc";
   analyzer[] = "Extensions/Extxmlwriter";
   analyzer[] = "Extensions/Extxsl";
   analyzer[] = "Extensions/Extxxtea";
   analyzer[] = "Extensions/Extyaml";
   analyzer[] = "Extensions/Extyar";
   analyzer[] = "Extensions/Extzendmonitor";
   analyzer[] = "Extensions/Extzip";
   analyzer[] = "Extensions/Extzlib";
   analyzer[] = "Extensions/Extzmq";
   analyzer[] = "Extensions/Extzookeeper";
   analyzer[] = "Files/DefinitionsOnly";
   analyzer[] = "Files/IsComponent";
   analyzer[] = "Files/MissingInclude";
   analyzer[] = "Files/NotDefinitionsOnly";
   analyzer[] = "Files/Services";
   analyzer[] = "Functions/AddDefaultValue";
   analyzer[] = "Functions/AliasesUsage";
   analyzer[] = "Functions/AvoidBooleanArgument";
   analyzer[] = "Functions/CancelledParameter";
   analyzer[] = "Functions/CannotUseStaticForClosure";
   analyzer[] = "Functions/CantUse";
   analyzer[] = "Functions/Closure2String";
   analyzer[] = "Functions/Closures";
   analyzer[] = "Functions/ConditionedFunctions";
   analyzer[] = "Functions/CouldBeCallable";
   analyzer[] = "Functions/CouldBeStaticClosure";
   analyzer[] = "Functions/CouldCentralize";
   analyzer[] = "Functions/CouldTypeWithIterable";
   analyzer[] = "Functions/CouldTypeWithString";
   analyzer[] = "Functions/CouldTypehint";
   analyzer[] = "Functions/DeepDefinitions";
   analyzer[] = "Functions/DeprecatedCallable";
   analyzer[] = "Functions/DontUseVoid";
   analyzer[] = "Functions/DuplicateNamedParameter";
   analyzer[] = "Functions/DynamicCode";
   analyzer[] = "Functions/EmptyFunction";
   analyzer[] = "Functions/ExceedingTypehint";
   analyzer[] = "Functions/FallbackFunction";
   analyzer[] = "Functions/FnArgumentVariableConfusion";
   analyzer[] = "Functions/FunctionCalledWithOtherCase";
   analyzer[] = "Functions/Functionnames";
   analyzer[] = "Functions/FunctionsUsingReference";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/HardcodedPasswords";
   analyzer[] = "Functions/HasFluentInterface";
   analyzer[] = "Functions/HasNotFluentInterface";
   analyzer[] = "Functions/Identity";
   analyzer[] = "Functions/InsufficientTypehint";
   analyzer[] = "Functions/IsExtFunction";
   analyzer[] = "Functions/IsGenerator";
   analyzer[] = "Functions/IsGlobal";
   analyzer[] = "Functions/KillsApp";
   analyzer[] = "Functions/MismatchParameterAndType";
   analyzer[] = "Functions/MismatchParameterName";
   analyzer[] = "Functions/MismatchTypeAndDefault";
   analyzer[] = "Functions/MismatchedDefaultArguments";
   analyzer[] = "Functions/MismatchedTypehint";
   analyzer[] = "Functions/MissingTypehint";
   analyzer[] = "Functions/ModifyTypedParameter";
   analyzer[] = "Functions/MultipleDeclarations";
   analyzer[] = "Functions/MultipleIdenticalClosure";
   analyzer[] = "Functions/MultipleReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/NoClassAsTypehint";
   analyzer[] = "Functions/NoDefaultForReference";
   analyzer[] = "Functions/NoLiteralForReference";
   analyzer[] = "Functions/NoReferencedVoid";
   analyzer[] = "Functions/NoReturnUsed";
   analyzer[] = "Functions/NullTypeFavorite";
   analyzer[] = "Functions/NullableWithoutCheck";
   analyzer[] = "Functions/OneLetterFunctions";
   analyzer[] = "Functions/OnlyVariableForReference";
   analyzer[] = "Functions/OnlyVariablePassedByReference";
   analyzer[] = "Functions/OptionalParameter";
   analyzer[] = "Functions/ParameterHiding";
   analyzer[] = "Functions/PrefixToType";
   analyzer[] = "Functions/RealFunctions";
   analyzer[] = "Functions/Recursive";
   analyzer[] = "Functions/RedeclaredPhpFunction";
   analyzer[] = "Functions/RelayFunction";
   analyzer[] = "Functions/RemoveParameterWithNamedOnes";
   analyzer[] = "Functions/RetypedReference";
   analyzer[] = "Functions/SemanticTyping";
   analyzer[] = "Functions/ShouldBeTypehinted";
   analyzer[] = "Functions/ShouldUseConstants";
   analyzer[] = "Functions/TooManyParameters";
   analyzer[] = "Functions/TooMuchIndented";
   analyzer[] = "Functions/TypeDodging";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/Typehints";
   analyzer[] = "Functions/UnknownParameterName";
   analyzer[] = "Functions/UnsetOnArguments";
   analyzer[] = "Functions/UnusedFunctions";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UseArrowFunctions";
   analyzer[] = "Functions/UseConstantAsArguments";
   analyzer[] = "Functions/UseConstantsAsReturns";
   analyzer[] = "Functions/UsedFunctions";
   analyzer[] = "Functions/UselessArgument";
   analyzer[] = "Functions/UselessDefault";
   analyzer[] = "Functions/UselessReferenceArgument";
   analyzer[] = "Functions/UselessTypeCheck";
   analyzer[] = "Functions/UsesDefaultArguments";
   analyzer[] = "Functions/VariableArguments";
   analyzer[] = "Functions/VariableParameterAmbiguityInArrowFunction";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Functions/WrongArgumentNameWithPhpFunction";
   analyzer[] = "Functions/WrongArgumentType";
   analyzer[] = "Functions/WrongCase";
   analyzer[] = "Functions/WrongNumberOfArguments";
   analyzer[] = "Functions/WrongNumberOfArgumentsMethods";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Functions/WrongTypehintedName";
   analyzer[] = "Functions/funcGetArgModified";
   analyzer[] = "Interfaces/AlreadyParentsInterface";
   analyzer[] = "Interfaces/AvoidSelfInInterface";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Interfaces/CouldUseInterface";
   analyzer[] = "Interfaces/EmptyInterface";
   analyzer[] = "Interfaces/InterfaceMethod";
   analyzer[] = "Interfaces/InterfaceUsage";
   analyzer[] = "Interfaces/Interfacenames";
   analyzer[] = "Interfaces/IsExtInterface";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/NoConstructorInInterface";
   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
   analyzer[] = "Interfaces/Php";
   analyzer[] = "Interfaces/PossibleInterfaces";
   analyzer[] = "Interfaces/RepeatedInterface";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Interfaces/UnusedInterfaces";
   analyzer[] = "Interfaces/UsedInterfaces";
   analyzer[] = "Interfaces/UselessInterfaces";
   analyzer[] = "Namespaces/Alias";
   analyzer[] = "Namespaces/AliasConfusion";
   analyzer[] = "Namespaces/ConstantFullyQualified";
   analyzer[] = "Namespaces/ConstantWithUseFavorite";
   analyzer[] = "Namespaces/CouldUseAlias";
   analyzer[] = "Namespaces/CouldUseMagicConstant";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/GlobalImport";
   analyzer[] = "Namespaces/HiddenUse";
   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
   analyzer[] = "Namespaces/MultipleAliasDefinitions";
   analyzer[] = "Namespaces/NamespaceUsage";
   analyzer[] = "Namespaces/Namespacesnames";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Namespaces/OverloadExistingNames";
   analyzer[] = "Namespaces/ShouldMakeAlias";
   analyzer[] = "Namespaces/UnresolvedUse";
   analyzer[] = "Namespaces/UnusedUse";
   analyzer[] = "Namespaces/UseFunctionsConstants";
   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
   analyzer[] = "Namespaces/UsedUse";
   analyzer[] = "Namespaces/WrongCase";
   analyzer[] = "Patterns/AbstractAway";
   analyzer[] = "Patterns/CourrierAntiPattern";
   analyzer[] = "Patterns/DependencyInjection";
   analyzer[] = "Patterns/Factory";
   analyzer[] = "Patterns/GetterSetter";
   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/Autoappend";
   analyzer[] = "Performances/AvoidArrayPush";
   analyzer[] = "Performances/CacheVariableOutsideLoop";
   analyzer[] = "Performances/ClassOperator";
   analyzer[] = "Performances/CountToAppend";
   analyzer[] = "Performances/DoInBase";
   analyzer[] = "Performances/DoubleArrayFlip";
   analyzer[] = "Performances/EllipsisMerge";
   analyzer[] = "Performances/FetchOneRowFormat";
   analyzer[] = "Performances/IssetWholeArray";
   analyzer[] = "Performances/LogicalToInArray";
   analyzer[] = "Performances/MakeOneCall";
   analyzer[] = "Performances/MbStringInLoop";
   analyzer[] = "Performances/MemoizeMagicCall";
   analyzer[] = "Performances/NoConcatInLoop";
   analyzer[] = "Performances/NoGlob";
   analyzer[] = "Performances/NotCountNull";
   analyzer[] = "Performances/OptimizeExplode";
   analyzer[] = "Performances/PHP7EncapsedStrings";
   analyzer[] = "Performances/Php74ArrayKeyExists";
   analyzer[] = "Performances/PreCalculateUse";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/RegexOnArrays";
   analyzer[] = "Performances/RegexOnCollector";
   analyzer[] = "Performances/SimpleSwitch";
   analyzer[] = "Performances/SimplifyForeach";
   analyzer[] = "Performances/SkipEmptyArray";
   analyzer[] = "Performances/SlowFunctions";
   analyzer[] = "Performances/StaticCallDontNeedObjects";
   analyzer[] = "Performances/StrposTooMuch";
   analyzer[] = "Performances/SubstrFirst";
   analyzer[] = "Performances/SubstrInLoops";
   analyzer[] = "Performances/TooManyExtractions";
   analyzer[] = "Performances/UseArraySlice";
   analyzer[] = "Performances/UseBlindVar";
   analyzer[] = "Performances/timeVsstrtotime";
   analyzer[] = "Php/ArrayKeyExistsWithObjects";
   analyzer[] = "Php/AssertFunctionIsReserved";
   analyzer[] = "Php/Assumptions";
   analyzer[] = "Php/AutoloadUsage";
   analyzer[] = "Php/AvoidGetobjectVars";
   analyzer[] = "Php/AvoidMbDectectEncoding";
   analyzer[] = "Php/AvoidReal";
   analyzer[] = "Php/AvoidSetErrorHandlerContextArg";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/CallingStaticTraitMethod";
   analyzer[] = "Php/CantUseReturnValueInWriteContext";
   analyzer[] = "Php/CaseForPSS";
   analyzer[] = "Php/CastingUsage";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClassConstWithArray";
   analyzer[] = "Php/ClassFunctionConfusion";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/CloseTagsConsistency";
   analyzer[] = "Php/ClosureThisSupport";
   analyzer[] = "Php/Coalesce";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/CompactInexistant";
   analyzer[] = "Php/ComparisonOnDifferentTypes";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/ConstWithArray";
   analyzer[] = "Php/CookiesVariables";
   analyzer[] = "Php/CouldUseIsCountable";
   analyzer[] = "Php/Crc32MightBeNegative";
   analyzer[] = "Php/CryptoUsage";
   analyzer[] = "Php/DateFormats";
   analyzer[] = "Php/DateTimeNotImmutable";
   analyzer[] = "Php/DeclareEncoding";
   analyzer[] = "Php/DeclareStrict";
   analyzer[] = "Php/DeclareStrictType";
   analyzer[] = "Php/DeprecateDollarCurly";
   analyzer[] = "Php/DetectCurrentClass";
   analyzer[] = "Php/DirectivesUsage";
   analyzer[] = "Php/DlUsage";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/ErrorLogUsage";
   analyzer[] = "Php/ExitNoArg";
   analyzer[] = "Php/ExponentUsage";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FilterToAddSlashes";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FirstClassCallable";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/FopenMode";
   analyzer[] = "Php/ForeachDontChangePointer";
   analyzer[] = "Php/ForeachObject";
   analyzer[] = "Php/GlobalWithoutSimpleVariable";
   analyzer[] = "Php/GlobalsVsGlobal";
   analyzer[] = "Php/Gotonames";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/Haltcompiler";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/HashAlgos74";
   analyzer[] = "Php/HashUsesObjects";
   analyzer[] = "Php/ImplodeOneArg";
   analyzer[] = "Php/IncomingValues";
   analyzer[] = "Php/IntegerSeparatorUsage";
   analyzer[] = "Php/InternalParameterType";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Php/IsINF";
   analyzer[] = "Php/IsNAN";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/IssetMultipleArgs";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/Labelnames";
   analyzer[] = "Php/LetterCharsLogicalFavorite";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithAppends";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/MethodCallOnNew";
   analyzer[] = "Php/MiddleVersion";
   analyzer[] = "Php/MissingMagicIsset";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Php/MixedKeyword";
   analyzer[] = "Php/MixedUsage";
   analyzer[] = "Php/MultipleDeclareStrict";
   analyzer[] = "Php/MustCallParentConstructor";
   analyzer[] = "Php/NamedArgumentAndVariadic";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NativeClassTypeCompatibility";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NeverKeyword";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewExponent";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NoCastToInt";
   analyzer[] = "Php/NoClassInGlobal";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoNullForNative";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/NotScalarType";
   analyzer[] = "Php/OnlyVariablePassedByReference";
   analyzer[] = "Php/OpensslEncryptAlgoChange";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Password55";
   analyzer[] = "Php/PathinfoReturns";
   analyzer[] = "Php/PearUsage";
   analyzer[] = "Php/Php54RemovedFunctions";
   analyzer[] = "Php/Php55NewFunctions";
   analyzer[] = "Php/Php55RemovedFunctions";
   analyzer[] = "Php/Php56NewFunctions";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php70RemovedDirective";
   analyzer[] = "Php/Php70RemovedFunctions";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php71NewFunctions";
   analyzer[] = "Php/Php71RemovedDirective";
   analyzer[] = "Php/Php71microseconds";
   analyzer[] = "Php/Php72Deprecation";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php72NewConstants";
   analyzer[] = "Php/Php72NewFunctions";
   analyzer[] = "Php/Php72ObjectKeyword";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php74Deprecation";
   analyzer[] = "Php/Php74NewClasses";
   analyzer[] = "Php/Php74NewConstants";
   analyzer[] = "Php/Php74NewFunctions";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php74RemovedFunctions";
   analyzer[] = "Php/Php74ReservedKeyword";
   analyzer[] = "Php/Php74mbstrrpos3rdArg";
   analyzer[] = "Php/Php80NamedParameterVariadic";
   analyzer[] = "Php/Php80NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80RemovedConstant";
   analyzer[] = "Php/Php80RemovedDirective";
   analyzer[] = "Php/Php80RemovedFunctions";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php80VariableSyntax";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php81RemovedDirective";
   analyzer[] = "Php/Php81RemovesResources";
   analyzer[] = "Php/Php82NewFunctions";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/Php83NewClasses";
   analyzer[] = "Php/Php83NewFunctions";
   analyzer[] = "Php/PhpErrorMsgUsage";
   analyzer[] = "Php/PregMatchAllFlag";
   analyzer[] = "Php/Prints";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/ReflectionExportIsDeprecated";
   analyzer[] = "Php/ReservedKeywords7";
   analyzer[] = "Php/ReservedMethods";
   analyzer[] = "Php/ReservedNames";
   analyzer[] = "Php/RestrictGlobalUsage";
   analyzer[] = "Php/ReturnTypehintUsage";
   analyzer[] = "Php/ReturnWithParenthesis";
   analyzer[] = "Php/SafePhpvars";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/ScalarTypehintUsage";
   analyzer[] = "Php/SerializeMagic";
   analyzer[] = "Php/SessionVariables";
   analyzer[] = "Php/SetExceptionHandlerPHP7";
   analyzer[] = "Php/SetHandlers";
   analyzer[] = "Php/ShellFavorite";
   analyzer[] = "Php/ShortOpenTagRequired";
   analyzer[] = "Php/ShortTernary";
   analyzer[] = "Php/ShouldPreprocess";
   analyzer[] = "Php/ShouldUseArrayColumn";
   analyzer[] = "Php/ShouldUseArrayFilter";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/ShouldUseFunction";
   analyzer[] = "Php/SpreadOperatorForArray";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/StaticclassUsage";
   analyzer[] = "Php/StringIntComparison";
   analyzer[] = "Php/StrposWithIntegers";
   analyzer[] = "Php/StrtrArguments";
   analyzer[] = "Php/SuperGlobalUsage";
   analyzer[] = "Php/ThrowUsage";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/TooManyNativeCalls";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TriggerErrorUsage";
   analyzer[] = "Php/TryCatchUsage";
   analyzer[] = "Php/TryMultipleCatch";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnknownPcre2Option";
   analyzer[] = "Php/UnsetOrCast";
   analyzer[] = "Php/UpperCaseFunction";
   analyzer[] = "Php/UpperCaseKeyword";
   analyzer[] = "Php/UseAttributes";
   analyzer[] = "Php/UseBrowscap";
   analyzer[] = "Php/UseCli";
   analyzer[] = "Php/UseContravariance";
   analyzer[] = "Php/UseCookies";
   analyzer[] = "Php/UseDateTimeImmutable";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseMatch";
   analyzer[] = "Php/UseNullSafeOperator";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/UseObjectApi";
   analyzer[] = "Php/UsePathinfo";
   analyzer[] = "Php/UsePathinfoArgs";
   analyzer[] = "Php/UseSessionStartOptions";
   analyzer[] = "Php/UseSetCookie";
   analyzer[] = "Php/UseStrContains";
   analyzer[] = "Php/UsortSorting";
   analyzer[] = "Php/Utf8EncodeDeprecated";
   analyzer[] = "Php/VersionCompareOperator";
   analyzer[] = "Php/WrongAttributeConfiguration";
   analyzer[] = "Php/WrongTypeForNativeFunction";
   analyzer[] = "Php/YieldFromUsage";
   analyzer[] = "Php/YieldUsage";
   analyzer[] = "Php/debugInfoUsage";
   analyzer[] = "Portability/FopenMode";
   analyzer[] = "Portability/GlobBraceUsage";
   analyzer[] = "Portability/IconvTranslit";
   analyzer[] = "Portability/LinuxOnlyFiles";
   analyzer[] = "Portability/WindowsOnlyConstants";
   analyzer[] = "Project/IsLibrary";
   analyzer[] = "Psr/Psr11Usage";
   analyzer[] = "Psr/Psr13Usage";
   analyzer[] = "Psr/Psr16Usage";
   analyzer[] = "Psr/Psr3Usage";
   analyzer[] = "Psr/Psr6Usage";
   analyzer[] = "Psr/Psr7Usage";
   analyzer[] = "Security/AnchorRegex";
   analyzer[] = "Security/AvoidThoseCrypto";
   analyzer[] = "Security/CantDisableClass";
   analyzer[] = "Security/CantDisableFunction";
   analyzer[] = "Security/CompareHash";
   analyzer[] = "Security/ConfigureExtract";
   analyzer[] = "Security/CryptoKeyLength";
   analyzer[] = "Security/CurlOptions";
   analyzer[] = "Security/DirectInjection";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/DynamicDl";
   analyzer[] = "Security/EncodedLetters";
   analyzer[] = "Security/FilterInputSource";
   analyzer[] = "Security/FilterNotRaw";
   analyzer[] = "Security/GPRAliases";
   analyzer[] = "Security/IncompatibleTypesWithIncoming";
   analyzer[] = "Security/IndirectInjection";
   analyzer[] = "Security/IntegerConversion";
   analyzer[] = "Security/KeepFilesRestricted";
   analyzer[] = "Security/MinusOneOnError";
   analyzer[] = "Security/MkdirDefault";
   analyzer[] = "Security/MoveUploadedFile";
   analyzer[] = "Security/NoEntIgnore";
   analyzer[] = "Security/NoNetForXmlLoad";
   analyzer[] = "Security/NoSleep";
   analyzer[] = "Security/NoWeakSSLCrypto";
   analyzer[] = "Security/RegisterGlobals";
   analyzer[] = "Security/SafeHttpHeaders";
   analyzer[] = "Security/SensitiveArgument";
   analyzer[] = "Security/SessionCachedData";
   analyzer[] = "Security/SessionLazyWrite";
   analyzer[] = "Security/SetCookieArgs";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Security/ShouldUseSessionRegenerateId";
   analyzer[] = "Security/Sqlite3RequiresSingleQuotes";
   analyzer[] = "Security/SuperGlobalContagion";
   analyzer[] = "Security/UnserializeSecondArg";
   analyzer[] = "Security/UploadFilenameInjection";
   analyzer[] = "Security/parseUrlWithoutParameters";
   analyzer[] = "Structures/AlternativeConsistenceByFile";
   analyzer[] = "Structures/AlwaysFalse";
   analyzer[] = "Structures/ArrayAccessOnLiteralArray";
   analyzer[] = "Structures/ArrayAddition";
   analyzer[] = "Structures/ArrayCountTripleEqual";
   analyzer[] = "Structures/ArrayMapPassesByValue";
   analyzer[] = "Structures/ArrayMergeAndVariadic";
   analyzer[] = "Structures/ArrayMergeArrayArray";
   analyzer[] = "Structures/ArrayMergeWithEllipsis";
   analyzer[] = "Structures/ArraySearchMultipleKeys";
   analyzer[] = "Structures/AssignedInOneBranch";
   analyzer[] = "Structures/BailOutEarly";
   analyzer[] = "Structures/BasenameSuffix";
   analyzer[] = "Structures/BlindVariableUsedBeyondLoop";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/Bracketless";
   analyzer[] = "Structures/Break0";
   analyzer[] = "Structures/BreakNonInteger";
   analyzer[] = "Structures/BreakOutsideLoop";
   analyzer[] = "Structures/BuriedAssignation";
   analyzer[] = "Structures/CalltimePassByReference";
   analyzer[] = "Structures/CastFavorite";
   analyzer[] = "Structures/CastToBoolean";
   analyzer[] = "Structures/CastingTernary";
   analyzer[] = "Structures/CatchShadowsVariable";
   analyzer[] = "Structures/CheckAllTypes";
   analyzer[] = "Structures/CheckDivision";
   analyzer[] = "Structures/CoalesceAndConcat";
   analyzer[] = "Structures/CoalesceNullCoalesce";
   analyzer[] = "Structures/CommonAlternatives";
   analyzer[] = "Structures/ComparedButNotAssignedStrings";
   analyzer[] = "Structures/ComparedComparison";
   analyzer[] = "Structures/ComparisonFavorite";
   analyzer[] = "Structures/ComplexExpression";
   analyzer[] = "Structures/ConcatenationInterpolationFavorite";
   analyzer[] = "Structures/ConditionalStructures";
   analyzer[] = "Structures/ConstDefineFavorite";
   analyzer[] = "Structures/ConstantConditions";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/CouldBeArrayCombine";
   analyzer[] = "Structures/CouldBeElse";
   analyzer[] = "Structures/CouldBeSpaceship";
   analyzer[] = "Structures/CouldBeStatic";
   analyzer[] = "Structures/CouldBeTernary";
   analyzer[] = "Structures/CouldCastToArray";
   analyzer[] = "Structures/CouldUseArraySum";
   analyzer[] = "Structures/CouldUseArrayUnique";
   analyzer[] = "Structures/CouldUseCompact";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseMatch";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrContains";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/CouldUseYieldFrom";
   analyzer[] = "Structures/CountIsNotNegative";
   analyzer[] = "Structures/CryptWithoutSalt";
   analyzer[] = "Structures/CurlVersionNow";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/DateTimePreference";
   analyzer[] = "Structures/DeclareStaticOnce";
   analyzer[] = "Structures/DefaultThenDiscard";
   analyzer[] = "Structures/DeprecatedMbEncoding";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/DifferencePreference";
   analyzer[] = "Structures/DirThenSlash";
   analyzer[] = "Structures/DirectlyUseFile";
   analyzer[] = "Structures/DontAddSeconds";
   analyzer[] = "Structures/DontChangeBlindKey";
   analyzer[] = "Structures/DontCompareTypedBoolean";
   analyzer[] = "Structures/DontLoopOnYield";
   analyzer[] = "Structures/DontMixPlusPlus";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Structures/DontReuseForeachSource";
   analyzer[] = "Structures/DontUseTheTypeAsVariable";
   analyzer[] = "Structures/DoubleAssignation";
   analyzer[] = "Structures/DoubleChecks";
   analyzer[] = "Structures/DoubleInstruction";
   analyzer[] = "Structures/DoubleObjectAssignation";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/DuplicateCalls";
   analyzer[] = "Structures/DynamicCalls";
   analyzer[] = "Structures/EchoPrintConsistance";
   analyzer[] = "Structures/EchoWithConcat";
   analyzer[] = "Structures/ElseUsage";
   analyzer[] = "Structures/EmptyBlocks";
   analyzer[] = "Structures/EmptyJsonError";
   analyzer[] = "Structures/EmptyLines";
   analyzer[] = "Structures/EmptyLoop";
   analyzer[] = "Structures/EmptyWithExpression";
   analyzer[] = "Structures/ErrorMessages";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/ExitUsage";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/Fallthrough";
   analyzer[] = "Structures/FilePutContentsDataType";
   analyzer[] = "Structures/FileUploadUsage";
   analyzer[] = "Structures/FileUsage";
   analyzer[] = "Structures/ForWithFunctioncall";
   analyzer[] = "Structures/ForeachNeedReferencedSource";
   analyzer[] = "Structures/ForeachReferenceIsNotModified";
   analyzer[] = "Structures/ForeachSourceValue";
   analyzer[] = "Structures/ForeachWithList";
   analyzer[] = "Structures/FunctionPreSubscripting";
   analyzer[] = "Structures/FunctionSubscripting";
   analyzer[] = "Structures/GetClassWithoutArg";
   analyzer[] = "Structures/GlobalInGlobal";
   analyzer[] = "Structures/GlobalOutsideLoop";
   analyzer[] = "Structures/GlobalUsage";
   analyzer[] = "Structures/GoToKeyDirectly";
   analyzer[] = "Structures/GtOrLtFavorite";
   analyzer[] = "Structures/HeredocDelimiterFavorite";
   analyzer[] = "Structures/Htmlentitiescall";
   analyzer[] = "Structures/HtmlentitiescallDefaultFlag";
   analyzer[] = "Structures/IdenticalCase";
   analyzer[] = "Structures/IdenticalConditions";
   analyzer[] = "Structures/IdenticalConsecutive";
   analyzer[] = "Structures/IdenticalElseif";
   analyzer[] = "Structures/IdenticalOnBothSides";
   analyzer[] = "Structures/IdenticalVariablesInForeach";
   analyzer[] = "Structures/IfThenReturnFavorite";
   analyzer[] = "Structures/IfWithSameConditions";
   analyzer[] = "Structures/Iffectation";
   analyzer[] = "Structures/ImplicitGlobal";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/ImplodeArgsOrder";
   analyzer[] = "Structures/IncludeUsage";
   analyzer[] = "Structures/InconsistentElseif";
   analyzer[] = "Structures/IndicesAreIntOrString";
   analyzer[] = "Structures/InfiniteRecursion";
   analyzer[] = "Structures/InitThenIf";
   analyzer[] = "Structures/InvalidCast";
   analyzer[] = "Structures/InvalidDateScanningFormat";
   analyzer[] = "Structures/InvalidPackFormat";
   analyzer[] = "Structures/InvalidRegex";
   analyzer[] = "Structures/IsZero";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/JsonEncodeExceptions";
   analyzer[] = "Structures/JsonWithOption";
   analyzer[] = "Structures/LogicalMistakes";
   analyzer[] = "Structures/LoneBlock";
   analyzer[] = "Structures/LongArguments";
   analyzer[] = "Structures/LongBlock";
   analyzer[] = "Structures/MailUsage";
   analyzer[] = "Structures/MaxLevelOfIdentation";
   analyzer[] = "Structures/MbStringNonEncodings";
   analyzer[] = "Structures/MbstringThirdArg";
   analyzer[] = "Structures/MbstringUnknownEncoding";
   analyzer[] = "Structures/McryptcreateivWithoutOption";
   analyzer[] = "Structures/MergeIfThen";
   analyzer[] = "Structures/MergeTernaryIntoIfthen";
   analyzer[] = "Structures/MismatchedTernary";
   analyzer[] = "Structures/MissingAssignation";
   analyzer[] = "Structures/MissingCases";
   analyzer[] = "Structures/MissingNew";
   analyzer[] = "Structures/MissingParenthesis";
   analyzer[] = "Structures/MisusedYield";
   analyzer[] = "Structures/ModernEmpty";
   analyzer[] = "Structures/MultilineExpressions";
   analyzer[] = "Structures/MultipleCatch";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultipleSimilarCalls";
   analyzer[] = "Structures/MultipleTypeCasesInSwitch";
   analyzer[] = "Structures/MultipleTypeVariable";
   analyzer[] = "Structures/NamedRegex";
   analyzer[] = "Structures/NegativePow";
   analyzer[] = "Structures/NestedIfthen";
   analyzer[] = "Structures/NestedLoops";
   analyzer[] = "Structures/NestedMatch";
   analyzer[] = "Structures/NestedTernary";
   analyzer[] = "Structures/NeverNegative";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoAppendOnSource";
   analyzer[] = "Structures/NoArrayUnique";
   analyzer[] = "Structures/NoAssignationInFunction";
   analyzer[] = "Structures/NoChangeIncomingVariables";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoDirectAccess";
   analyzer[] = "Structures/NoDirectUsage";
   analyzer[] = "Structures/NoEmptyStringWithExplode";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/NoHardcodedHash";
   analyzer[] = "Structures/NoHardcodedIp";
   analyzer[] = "Structures/NoHardcodedPath";
   analyzer[] = "Structures/NoHardcodedPort";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/NoMaxOnEmptyArray";
   analyzer[] = "Structures/NoNeedForElse";
   analyzer[] = "Structures/NoNeedForTriple";
   analyzer[] = "Structures/NoNullForIndex";
   analyzer[] = "Structures/NoObjectAsIndex";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoReferenceOnLeft";
   analyzer[] = "Structures/NoReturnInFinally";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/NoValidCast";
   analyzer[] = "Structures/NoVariableIsACondition";
   analyzer[] = "Structures/NonBreakableSpaceInNames";
   analyzer[] = "Structures/NonIntStringAsIndex";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/NotEqual";
   analyzer[] = "Structures/NotNot";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/OnceUsage";
   analyzer[] = "Structures/OneDotOrObjectOperatorPerLine";
   analyzer[] = "Structures/OneExpressionBracketsConsistency";
   analyzer[] = "Structures/OneIfIsSufficient";
   analyzer[] = "Structures/OneLevelOfIndentation";
   analyzer[] = "Structures/OneLineTwoInstructions";
   analyzer[] = "Structures/OnlyFirstByte";
   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";
   analyzer[] = "Structures/OverwrittenForeachVar";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/PhpinfoUsage";
   analyzer[] = "Structures/PlusEgalOne";
   analyzer[] = "Structures/PossibleIncrement";
   analyzer[] = "Structures/PossibleInfiniteLoop";
   analyzer[] = "Structures/PrintAndDie";
   analyzer[] = "Structures/PrintWithoutParenthesis";
   analyzer[] = "Structures/QueriesInLoop";
   analyzer[] = "Structures/RandomWithoutTry";
   analyzer[] = "Structures/RecalledCondition";
   analyzer[] = "Structures/RegexDelimiter";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/RepeatedRegex";
   analyzer[] = "Structures/ResourcesUsage";
   analyzer[] = "Structures/ResultMayBeMissing";
   analyzer[] = "Structures/ReturnTrueFalse";
   analyzer[] = "Structures/ReturnVoid";
   analyzer[] = "Structures/ReuseVariable";
   analyzer[] = "Structures/SGVariablesConfusion";
   analyzer[] = "Structures/SameConditions";
   analyzer[] = "Structures/SequenceInFor";
   analyzer[] = "Structures/SetlocaleNeedsConstants";
   analyzer[] = "Structures/ShellUsage";
   analyzer[] = "Structures/ShortOrCompleteComparison";
   analyzer[] = "Structures/ShortTags";
   analyzer[] = "Structures/ShouldChainException";
   analyzer[] = "Structures/ShouldMakeTernary";
   analyzer[] = "Structures/ShouldPreprocess";
   analyzer[] = "Structures/ShouldUseExplodeArgs";
   analyzer[] = "Structures/ShouldUseForeach";
   analyzer[] = "Structures/ShouldUseMath";
   analyzer[] = "Structures/ShouldUseOperator";
   analyzer[] = "Structures/SimplePreg";
   analyzer[] = "Structures/SprintfFormatCompilation";
   analyzer[] = "Structures/StaticInclude";
   analyzer[] = "Structures/StaticLoop";
   analyzer[] = "Structures/StrictInArrayFavorite";
   analyzer[] = "Structures/StringInterpolationFavorite";
   analyzer[] = "Structures/StripTagsSkipsClosedTag";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/StrposLessThanOne";
   analyzer[] = "Structures/SubstrLastArg";
   analyzer[] = "Structures/SubstrToTrim";
   analyzer[] = "Structures/SuspiciousComparison";
   analyzer[] = "Structures/SwitchToSwitch";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/SwitchWithoutDefault";
   analyzer[] = "Structures/TernaryInConcat";
   analyzer[] = "Structures/TestThenCast";
   analyzer[] = "Structures/ThrowsAndAssign";
   analyzer[] = "Structures/TimestampDifference";
   analyzer[] = "Structures/TooManyChainedCalls";
   analyzer[] = "Structures/TooManyElseif";
   analyzer[] = "Structures/TryFinally";
   analyzer[] = "Structures/UncheckedResources";
   analyzer[] = "Structures/UnknownPregOption";
   analyzer[] = "Structures/Unpreprocessed";
   analyzer[] = "Structures/UnreachableCode";
   analyzer[] = "Structures/UnsetInForeach";
   analyzer[] = "Structures/UnsupportedOperandTypes";
   analyzer[] = "Structures/UnsupportedTypesWithOperators";
   analyzer[] = "Structures/UnusedGlobal";
   analyzer[] = "Structures/UnusedLabel";
   analyzer[] = "Structures/UseArrayFunctions";
   analyzer[] = "Structures/UseCaseValue";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UseCountRecursive";
   analyzer[] = "Structures/UseDebug";
   analyzer[] = "Structures/UseFileAppend";
   analyzer[] = "Structures/UseInstanceof";
   analyzer[] = "Structures/UseListWithForeach";
   analyzer[] = "Structures/UsePositiveCondition";
   analyzer[] = "Structures/UseStrEndsWith";
   analyzer[] = "Structures/UseStrStartsWith";
   analyzer[] = "Structures/UseSystemTmp";
   analyzer[] = "Structures/UseUrlQueryFunctions";
   analyzer[] = "Structures/UseVariableInsideLoop";
   analyzer[] = "Structures/UselessBrackets";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Structures/UselessCoalesce";
   analyzer[] = "Structures/UselessGlobal";
   analyzer[] = "Structures/UselessInstruction";
   analyzer[] = "Structures/UselessNullCoalesce";
   analyzer[] = "Structures/UselessParenthesis";
   analyzer[] = "Structures/UselessShortTernary";
   analyzer[] = "Structures/UselessSwitch";
   analyzer[] = "Structures/UselessTrailingComma";
   analyzer[] = "Structures/UselessUnset";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Structures/VariableMayBeNonGlobal";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Structures/WrongLocale";
   analyzer[] = "Structures/WrongPrecedenceInExpression";
   analyzer[] = "Structures/WrongRange";
   analyzer[] = "Structures/YodaComparison";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Structures/strOrMbFavorite";
   analyzer[] = "Structures/toStringThrowsException";
   analyzer[] = "Traits/CannotCallTraitMethod";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/CouldUseTrait";
   analyzer[] = "Traits/DependantTrait";
   analyzer[] = "Traits/EmptyTrait";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/IncompatibleProperty";
   analyzer[] = "Traits/IsExtTrait";
   analyzer[] = "Traits/LocallyUsedProperty";
   analyzer[] = "Traits/MethodCollisionTraits";
   analyzer[] = "Traits/MultipleUsage";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Traits/Php";
   analyzer[] = "Traits/SelfUsingTrait";
   analyzer[] = "Traits/SidelinedMethod";
   analyzer[] = "Traits/TraitMethod";
   analyzer[] = "Traits/TraitNotFound";
   analyzer[] = "Traits/TraitUsage";
   analyzer[] = "Traits/Traitnames";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UnusedClassTrait";
   analyzer[] = "Traits/UnusedTrait";
   analyzer[] = "Traits/UsedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Type/ArrayIndex";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/CharString";
   analyzer[] = "Type/Continents";
   analyzer[] = "Type/DuplicateLiteral";
   analyzer[] = "Type/Email";
   analyzer[] = "Type/GPCIndex";
   analyzer[] = "Type/Heredoc";
   analyzer[] = "Type/Hexadecimal";
   analyzer[] = "Type/HexadecimalString";
   analyzer[] = "Type/HttpHeader";
   analyzer[] = "Type/HttpStatus";
   analyzer[] = "Type/IncomingDateFormat";
   analyzer[] = "Type/Ip";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Type/Md5String";
   analyzer[] = "Type/MimeType";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Type/Nowdoc";
   analyzer[] = "Type/Octal";
   analyzer[] = "Type/OctalInString";
   analyzer[] = "Type/OneVariableStrings";
   analyzer[] = "Type/OpensslCipher";
   analyzer[] = "Type/Pack";
   analyzer[] = "Type/Path";
   analyzer[] = "Type/Pcre";
   analyzer[] = "Type/Ports";
   analyzer[] = "Type/Printf";
   analyzer[] = "Type/Protocols";
   analyzer[] = "Type/Regex";
   analyzer[] = "Type/Sapi";
   analyzer[] = "Type/Shellcommands";
   analyzer[] = "Type/ShouldBeSingleQuote";
   analyzer[] = "Type/ShouldTypecast";
   analyzer[] = "Type/SilentlyCastInteger";
   analyzer[] = "Type/SimilarIntegers";
   analyzer[] = "Type/SpecialIntegers";
   analyzer[] = "Type/Sql";
   analyzer[] = "Type/StringHoldAVariable";
   analyzer[] = "Type/StringInterpolation";
   analyzer[] = "Type/StringWithStrangeSpace";
   analyzer[] = "Type/UdpDomains";
   analyzer[] = "Type/UnicodeBlock";
   analyzer[] = "Type/Url";
   analyzer[] = "Typehints/CouldBeCIT";
   analyzer[] = "Typehints/CouldBeCallable";
   analyzer[] = "Typehints/CouldBeGenerator";
   analyzer[] = "Typehints/CouldBeNever";
   analyzer[] = "Typehints/CouldBeParent";
   analyzer[] = "Typehints/CouldBeResource";
   analyzer[] = "Typehints/CouldBeSelf";
   analyzer[] = "Typehints/CouldBeVoid";
   analyzer[] = "Typehints/CouldNotType";
   analyzer[] = "Typehints/MissingReturntype";
   analyzer[] = "Typehints/StandaloneTypeTFN";
   analyzer[] = "Typehints/WrongTypeWithDefault";
   analyzer[] = "Utils/Selector";
   analyzer[] = "Variables/AmbiguousTypes";
   analyzer[] = "Variables/AssignedTwiceOrMore";
   analyzer[] = "Variables/Blind";
   analyzer[] = "Variables/CloseNaming";
   analyzer[] = "Variables/ComplexDynamicNames";
   analyzer[] = "Variables/ConstantTypo";
   analyzer[] = "Variables/Globals";
   analyzer[] = "Variables/InconsistentUsage";
   analyzer[] = "Variables/InheritedStaticVariable";
   analyzer[] = "Variables/InterfaceArguments";
   analyzer[] = "Variables/IsLocalConstant";
   analyzer[] = "Variables/LocalGlobals";
   analyzer[] = "Variables/LostReferences";
   analyzer[] = "Variables/NoInitialS";
   analyzer[] = "Variables/NoStaticVarInMethod";
   analyzer[] = "Variables/Overwriting";
   analyzer[] = "Variables/OverwrittenLiterals";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RealVariables";
   analyzer[] = "Variables/RedeclaredStaticVariable";
   analyzer[] = "Variables/References";
   analyzer[] = "Variables/SelfTransform";
   analyzer[] = "Variables/StaticVariableInitialisation";
   analyzer[] = "Variables/StaticVariables";
   analyzer[] = "Variables/StrangeName";
   analyzer[] = "Variables/UncommonEnvVar";
   analyzer[] = "Variables/UndefinedConstantName";
   analyzer[] = "Variables/VariableLong";
   analyzer[] = "Variables/VariableNonascii";
   analyzer[] = "Variables/VariableOneLetter";
   analyzer[] = "Variables/VariableUppercase";
   analyzer[] = "Variables/VariableUsedOnce";
   analyzer[] = "Variables/VariableUsedOnceByContext";
   analyzer[] = "Variables/WrittenOnlyVariable";
   analyzer[] = "Vendors/Cakephp";
   analyzer[] = "Vendors/Codeigniter";
   analyzer[] = "Vendors/Concrete5";
   analyzer[] = "Vendors/Drupal";
   analyzer[] = "Vendors/Feast";
   analyzer[] = "Vendors/Fuel";
   analyzer[] = "Vendors/Joomla";
   analyzer[] = "Vendors/Laravel";
   analyzer[] = "Vendors/Neos";
   analyzer[] = "Vendors/Phalcon";
   analyzer[] = "Vendors/Sylius";
   analyzer[] = "Vendors/Symfony";
   analyzer[] = "Vendors/Typo3";
   analyzer[] = "Vendors/Wordpress";
   analyzer[] = "Vendors/Yii";


.. _annex-yaml-changed-behavior:

Changed Behavior for .exakat.yaml
+++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Changed Behavior':
     - 'Arrays/AmbiguousKeys'
     - 'Arrays/AppendAndAssignArrays'
     - 'Arrays/ArrayNSUsage'
     - 'Arrays/Arrayindex'
     - 'Arrays/EmptySlots'
     - 'Arrays/FloatConversionAsIndex'
     - 'Arrays/GettingLastElement'
     - 'Arrays/MassCreation'
     - 'Arrays/NegativeStart'
     - 'Arrays/NoSpreadForHash'
     - 'Arrays/NonConstantArray'
     - 'Arrays/WeakType'
     - 'Arrays/WeirdIndex'
     - 'Arrays/WithCallback'
     - 'Attributes/Deprecated'
     - 'Attributes/Friend'
     - 'Attributes/InjectableVersion'
     - 'Attributes/MissingAttributeAttribute'
     - 'Attributes/ModifyImmutable'
     - 'Attributes/NestedAttributes'
     - 'Attributes/PhpNativeAttributes'
     - 'Attributes/UselessOverride'
     - 'Classes/AbstractConstants'
     - 'Classes/AbstractOrImplements'
     - 'Classes/AbstractStatic'
     - 'Classes/Abstractclass'
     - 'Classes/Abstractmethods'
     - 'Classes/AccessPrivate'
     - 'Classes/AccessProtected'
     - 'Classes/AmbiguousStatic'
     - 'Classes/AmbiguousVisibilities'
     - 'Classes/Anonymous'
     - 'Classes/AvoidOptionArrays'
     - 'Classes/AvoidOptionalProperties'
     - 'Classes/CancelCommonMethod'
     - 'Classes/CannotBeReadonly'
     - 'Classes/CantExtendFinal'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/CantInstantiateClass'
     - 'Classes/CheckAfterNullSafeOperator'
     - 'Classes/CheckOnCallUsage'
     - 'Classes/ChecksPropertyExistence'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/CitSameName'
     - 'Classes/ClassAliasUsage'
     - 'Classes/ClassInvasion'
     - 'Classes/ClassOverreach'
     - 'Classes/ClassUsage'
     - 'Classes/Classnames'
     - 'Classes/CloneWithNonObject'
     - 'Classes/CloningUsage'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/ConstantClass'
     - 'Classes/ConstantDefinition'
     - 'Classes/ConstantUsedBelow'
     - 'Classes/Constructor'
     - 'Classes/CouldBeAbstractClass'
     - 'Classes/CouldBeAbstractMethod'
     - 'Classes/CouldBeFinal'
     - 'Classes/CouldBeIterable'
     - 'Classes/CouldBeParentMethod'
     - 'Classes/CouldBePrivate'
     - 'Classes/CouldBePrivateConstante'
     - 'Classes/CouldBePrivateMethod'
     - 'Classes/CouldBeProtectedConstant'
     - 'Classes/CouldBeProtectedMethod'
     - 'Classes/CouldBeProtectedProperty'
     - 'Classes/CouldBeReadonly'
     - 'Classes/CouldBeReadonlyProperty'
     - 'Classes/CouldBeStatic'
     - 'Classes/CouldBeStringable'
     - 'Classes/CouldInjectParam'
     - 'Classes/CouldSetPropertyDefault'
     - 'Classes/CouldUseClassOperator'
     - 'Classes/CyclicReferences'
     - 'Classes/DefinedConstants'
     - 'Classes/DefinedParentMP'
     - 'Classes/DefinedProperty'
     - 'Classes/DefinedStaticMP'
     - 'Classes/DemeterLaw'
     - 'Classes/DependantAbstractClass'
     - 'Classes/DifferentArgumentCounts'
     - 'Classes/DisconnectedClasses'
     - 'Classes/DontSendThisInConstructor'
     - 'Classes/DontUnsetProperties'
     - 'Classes/DynamicClass'
     - 'Classes/DynamicMethodCall'
     - 'Classes/DynamicNew'
     - 'Classes/DynamicPropertyCall'
     - 'Classes/DynamicSelfCalls'
     - 'Classes/EmptyClass'
     - 'Classes/ExportProperty'
     - 'Classes/ExtendsStdclass'
     - 'Classes/FinalByOcramius'
     - 'Classes/Finalclass'
     - 'Classes/Finalmethod'
     - 'Classes/FossilizedMethod'
     - 'Classes/HasMagicProperty'
     - 'Classes/HiddenNullable'
     - 'Classes/IdenticalMethods'
     - 'Classes/ImmutableSignature'
     - 'Classes/ImplementIsForInterface'
     - 'Classes/ImplementedMethodsArePublic'
     - 'Classes/IncompatibleConstructor'
     - 'Classes/IncompatibleSignature'
     - 'Classes/IncompatibleSignature74'
     - 'Classes/InheritedPropertyMustMatch'
     - 'Classes/InsufficientPropertyTypehint'
     - 'Classes/IntegerAsProperty'
     - 'Classes/IsExtClass'
     - 'Classes/IsInterfaceMethod'
     - 'Classes/IsNotFamily'
     - 'Classes/IsUpperFamily'
     - 'Classes/LocallyUnusedProperty'
     - 'Classes/LocallyUsedProperty'
     - 'Classes/LoweredAccessLevel'
     - 'Classes/MagicMethod'
     - 'Classes/MagicMethodReturntypes'
     - 'Classes/MakeDefault'
     - 'Classes/MakeGlobalAProperty'
     - 'Classes/MakeMagicConcrete'
     - 'Classes/MethodIsOverwritten'
     - 'Classes/MethodPropertyConfusion'
     - 'Classes/MethodSignatureMustBeCompatible'
     - 'Classes/MethodUsedBelow'
     - 'Classes/MismatchProperties'
     - 'Classes/MissingVisibility'
     - 'Classes/MultipleDeclarations'
     - 'Classes/MultiplePropertyDeclaration'
     - 'Classes/MultiplePropertyDeclarationOnOneLine'
     - 'Classes/MultipleTraitOrInterface'
     - 'Classes/MutualExtension'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoNullWithNullSafeOperator'
     - 'Classes/NoPSSOutsideClass'
     - 'Classes/NoParent'
     - 'Classes/NoPublicAccess'
     - 'Classes/NoReadonlyAssignationInGlobal'
     - 'Classes/NoSelfReferencingConstant'
     - 'Classes/NonNullableSetters'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NormalMethods'
     - 'Classes/NullOnNew'
     - 'Classes/OldStyleConstructor'
     - 'Classes/OldStyleVar'
     - 'Classes/OneObjectOperatorPerLine'
     - 'Classes/OnlyStaticMethods'
     - 'Classes/OrderOfDeclaration'
     - 'Classes/OverwrittenConst'
     - 'Classes/PPPDeclarationStyle'
     - 'Classes/ParentFirst'
     - 'Classes/ParentIsNotStatic'
     - 'Classes/PromotedProperties'
     - 'Classes/PropertyCouldBeLocal'
     - 'Classes/PropertyDefinition'
     - 'Classes/PropertyInvasion'
     - 'Classes/PropertyMethodSameName'
     - 'Classes/PropertyNeverUsed'
     - 'Classes/PropertyUsedAbove'
     - 'Classes/PropertyUsedInOneMethodOnly'
     - 'Classes/PropertyUsedInternally'
     - 'Classes/PssWithoutClass'
     - 'Classes/RaisedAccessLevel'
     - 'Classes/ReadonlyUsage'
     - 'Classes/RedefinedConstants'
     - 'Classes/RedefinedDefault'
     - 'Classes/RedefinedMethods'
     - 'Classes/RedefinedPrivateProperty'
     - 'Classes/RedefinedProperty'
     - 'Classes/RewroteFinalClassConstant'
     - 'Classes/SameNameAsFile'
     - 'Classes/ShouldDeepClone'
     - 'Classes/ShouldHaveDestructor'
     - 'Classes/ShouldUseSelf'
     - 'Classes/ShouldUseThis'
     - 'Classes/StaticContainsThis'
     - 'Classes/StaticMethods'
     - 'Classes/StaticMethodsCalledFromObject'
     - 'Classes/StaticProperties'
     - 'Classes/StrangeName'
     - 'Classes/SwappedArguments'
     - 'Classes/TestClass'
     - 'Classes/ThisIsForClasses'
     - 'Classes/ThisIsNotAnArray'
     - 'Classes/TooManyDereferencing'
     - 'Classes/TooManyFinds'
     - 'Classes/TooManyInjections'
     - 'Classes/TypedClassConstants'
     - 'Classes/TypehintCyclicDependencies'
     - 'Classes/UndefinedConstants'
     - 'Classes/UndefinedMethod'
     - 'Classes/UndefinedProperty'
     - 'Classes/UndefinedStaticMP'
     - 'Classes/UndefinedStaticclass'
     - 'Classes/UnfinishedObject'
     - 'Classes/UninitedProperty'
     - 'Classes/UnitializedProperties'
     - 'Classes/UnreachableConstant'
     - 'Classes/UnreachableMethod'
     - 'Classes/UnresolvedCatch'
     - 'Classes/UnresolvedClasses'
     - 'Classes/UnresolvedInstanceof'
     - 'Classes/UnusedClass'
     - 'Classes/UnusedConstant'
     - 'Classes/UnusedMethods'
     - 'Classes/UnusedPrivateMethod'
     - 'Classes/UnusedProtectedMethods'
     - 'Classes/UnusedPublicMethod'
     - 'Classes/UseClassOperator'
     - 'Classes/UseInstanceof'
     - 'Classes/UseThis'
     - 'Classes/UsedClass'
     - 'Classes/UsedMethods'
     - 'Classes/UsedOnceProperty'
     - 'Classes/UsedPrivateMethod'
     - 'Classes/UsedProtectedMethod'
     - 'Classes/UselessAbstract'
     - 'Classes/UselessAssignationOfPromotedProperty'
     - 'Classes/UselessConstantOverwrite'
     - 'Classes/UselessConstructor'
     - 'Classes/UselessFinal'
     - 'Classes/UselessMethod'
     - 'Classes/UselessNullSafeOperator'
     - 'Classes/UselessTypehint'
     - 'Classes/UsingThisOutsideAClass'
     - 'Classes/VariableClasses'
     - 'Classes/WeakType'
     - 'Classes/toStringPss'
     - 'Complete/CreateCompactVariables'
     - 'Complete/CreateDefaultValues'
     - 'Complete/CreateForeachDefault'
     - 'Complete/CreateMagicMethod'
     - 'Complete/CreateMagicProperty'
     - 'Complete/EnumCaseValues'
     - 'Complete/ExtendedTypehints'
     - 'Complete/FollowClosureDefinition'
     - 'Complete/GlobalDefinitions'
     - 'Complete/IsExtStructure'
     - 'Complete/IsPhpStructure'
     - 'Complete/MakeAllStatics'
     - 'Complete/MakeClassConstantDefinition'
     - 'Complete/MakeClassMethodDefinition'
     - 'Complete/OverwrittenProperties'
     - 'Complete/PhpExtStubPropertyMethod'
     - 'Complete/PhpNativeReference'
     - 'Complete/PropagateConstants'
     - 'Complete/ReturnTypehint'
     - 'Complete/SetArrayClassDefinition'
     - 'Complete/SetClassMethodRemoteDefinition'
     - 'Complete/SetClassPropertyDefinitionWithTypehint'
     - 'Complete/SetClassRemoteDefinitionWithGlobal'
     - 'Complete/SetClassRemoteDefinitionWithInjection'
     - 'Complete/SetClassRemoteDefinitionWithLocalNew'
     - 'Complete/SetClassRemoteDefinitionWithReturnTypehint'
     - 'Complete/SetClassRemoteDefinitionWithTypehint'
     - 'Complete/SetCloneLink'
     - 'Complete/SetMethodFnp'
     - 'Complete/SetParentDefinition'
     - 'Complete/SolveTraitConstants'
     - 'Complete/SolveTraitMethods'
     - 'Complete/Superglobals'
     - 'Complete/VariableTypehint'
     - 'Composer/Autoload'
     - 'Composer/UseComposer'
     - 'Composer/UseComposerLock'
     - 'Constants/ConditionedConstants'
     - 'Constants/ConstDefinePreference'
     - 'Constants/ConstantUsedOnce'
     - 'Constants/CouldUseConstant'
     - 'Constants/CreatedOutsideItsNamespace'
     - 'Constants/CustomConstantUsage'
     - 'Constants/DefineInsensitivePreference'
     - 'Constants/DynamicCreation'
     - 'Constants/InconsistantCase'
     - 'Constants/InvalidName'
     - 'Constants/IsExtConstant'
     - 'Constants/IsGlobalConstant'
     - 'Constants/IsPhpConstant'
     - 'Constants/MagicConstantUsage'
     - 'Constants/MultipleConstantDefinition'
     - 'Constants/PhpConstantUsage'
     - 'Constants/RelayConstant'
     - 'Constants/StrangeName'
     - 'Constants/UndefinedConstants'
     - 'Constants/UnusedConstants'
     - 'Constants/VariableConstant'
     - 'Custom/MethodUsage'
     - 'Dump/ArgumentCountsPerCalls'
     - 'Dump/CallOrder'
     - 'Dump/ClassInjectionCount'
     - 'Dump/CollectAtomCounts'
     - 'Dump/CollectBlockSize'
     - 'Dump/CollectCalls'
     - 'Dump/CollectCatch'
     - 'Dump/CollectClassChanges'
     - 'Dump/CollectClassChildren'
     - 'Dump/CollectClassConstantCounts'
     - 'Dump/CollectClassDepth'
     - 'Dump/CollectClassInterfaceCounts'
     - 'Dump/CollectClassTraitsCounts'
     - 'Dump/CollectClassesDependencies'
     - 'Dump/CollectDefinitionsStats'
     - 'Dump/CollectDependencyExtension'
     - 'Dump/CollectFilesDependencies'
     - 'Dump/CollectForeachFavorite'
     - 'Dump/CollectGlobalVariables'
     - 'Dump/CollectGraphTriplets'
     - 'Dump/CollectLiterals'
     - 'Dump/CollectLocalVariableCounts'
     - 'Dump/CollectMbstringEncodings'
     - 'Dump/CollectMethodCounts'
     - 'Dump/CollectMethodsThrowingExceptions'
     - 'Dump/CollectNativeCallsPerExpressions'
     - 'Dump/CollectParameterCounts'
     - 'Dump/CollectParameterNames'
     - 'Dump/CollectPhpStructures'
     - 'Dump/CollectPropertyCounts'
     - 'Dump/CollectPropertyUsage'
     - 'Dump/CollectReadability'
     - 'Dump/CollectSetLocale'
     - 'Dump/CollectStructures'
     - 'Dump/CollectStubStructures'
     - 'Dump/CollectThrow'
     - 'Dump/CollectUseCounts'
     - 'Dump/CollectVariables'
     - 'Dump/CollectVendorStructures'
     - 'Dump/CollectsNames'
     - 'Dump/CombinedCalls'
     - 'Dump/ConstantOrder'
     - 'Dump/CouldBeAConstant'
     - 'Dump/CyclomaticComplexity'
     - 'Dump/DereferencingLevels'
     - 'Dump/DumpComparedLiterals'
     - 'Dump/EnvironnementVariables'
     - 'Dump/FossilizedMethods'
     - 'Dump/Inclusions'
     - 'Dump/IndentationLevels'
     - 'Dump/NewOrder'
     - 'Dump/ParameterArgumentsLinks'
     - 'Dump/PublicReach'
     - 'Dump/TypehintingStats'
     - 'Dump/Typehintorder'
     - 'Enums/CouldBeEnum'
     - 'Enums/NoMagicMethod'
     - 'Enums/UndefinedEnumcase'
     - 'Enums/UnusedEnumCase'
     - 'Exceptions/AlreadyCaught'
     - 'Exceptions/CantThrow'
     - 'Exceptions/CatchE'
     - 'Exceptions/CatchUndefinedVariable'
     - 'Exceptions/CaughtButNotThrown'
     - 'Exceptions/CaughtExceptions'
     - 'Exceptions/ConvertedExceptions'
     - 'Exceptions/CouldDropVariable'
     - 'Exceptions/DefinedExceptions'
     - 'Exceptions/ForgottenThrown'
     - 'Exceptions/IsPhpException'
     - 'Exceptions/LargeTryBlock'
     - 'Exceptions/LongPreparation'
     - 'Exceptions/MultipleCatch'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/PossibleTypeError'
     - 'Exceptions/Rethrown'
     - 'Exceptions/SetChainingException'
     - 'Exceptions/ThrowFunctioncall'
     - 'Exceptions/ThrowRawExceptions'
     - 'Exceptions/TryNoCatch'
     - 'Exceptions/UncaughtExceptions'
     - 'Exceptions/Unthrown'
     - 'Exceptions/UnusedExceptionVariable'
     - 'Exceptions/UselessCatch'
     - 'Exceptions/UselessTry'
     - 'Extensions/Extamqp'
     - 'Extensions/Extapache'
     - 'Extensions/Extapc'
     - 'Extensions/Extapcu'
     - 'Extensions/Extarray'
     - 'Extensions/Extast'
     - 'Extensions/Extbcmath'
     - 'Extensions/Extbzip2'
     - 'Extensions/Extcalendar'
     - 'Extensions/Extcmark'
     - 'Extensions/Extcom'
     - 'Extensions/Extcrypto'
     - 'Extensions/Extcsv'
     - 'Extensions/Extctype'
     - 'Extensions/Extcurl'
     - 'Extensions/Extdate'
     - 'Extensions/Extdb2'
     - 'Extensions/Extdba'
     - 'Extensions/Extdecimal'
     - 'Extensions/Extdio'
     - 'Extensions/Extdom'
     - 'Extensions/Extds'
     - 'Extensions/Exteio'
     - 'Extensions/Extenchant'
     - 'Extensions/Extev'
     - 'Extensions/Extevent'
     - 'Extensions/Extexcimer'
     - 'Extensions/Extexif'
     - 'Extensions/Extexpect'
     - 'Extensions/Extfam'
     - 'Extensions/Extfann'
     - 'Extensions/Extffi'
     - 'Extensions/Extfile'
     - 'Extensions/Extfileinfo'
     - 'Extensions/Extfilter'
     - 'Extensions/Extfpm'
     - 'Extensions/Extftp'
     - 'Extensions/Extgd'
     - 'Extensions/Extgearman'
     - 'Extensions/Extgender'
     - 'Extensions/Extgeoip'
     - 'Extensions/Extgeospatial'
     - 'Extensions/Extgettext'
     - 'Extensions/Extgmagick'
     - 'Extensions/Extgmp'
     - 'Extensions/Extgnupg'
     - 'Extensions/Extgrpc'
     - 'Extensions/Exthash'
     - 'Extensions/Exthrtime'
     - 'Extensions/Exthttp'
     - 'Extensions/Extibase'
     - 'Extensions/Extice'
     - 'Extensions/Exticonv'
     - 'Extensions/Extigbinary'
     - 'Extensions/Extimagick'
     - 'Extensions/Extimap'
     - 'Extensions/Extinfo'
     - 'Extensions/Extinotify'
     - 'Extensions/Extintl'
     - 'Extensions/Extjson'
     - 'Extensions/Extjudy'
     - 'Extensions/Extldap'
     - 'Extensions/Extleveldb'
     - 'Extensions/Extlibsodium'
     - 'Extensions/Extlibxml'
     - 'Extensions/Extlua'
     - 'Extensions/Extlzf'
     - 'Extensions/Extmail'
     - 'Extensions/Extmailparse'
     - 'Extensions/Extmath'
     - 'Extensions/Extmbstring'
     - 'Extensions/Extmcrypt'
     - 'Extensions/Extmemcache'
     - 'Extensions/Extmemcached'
     - 'Extensions/Extmongo'
     - 'Extensions/Extmongodb'
     - 'Extensions/Extmsgpack'
     - 'Extensions/Extmssql'
     - 'Extensions/Extmysqli'
     - 'Extensions/Extncurses'
     - 'Extensions/Extnewt'
     - 'Extensions/Extnsapi'
     - 'Extensions/Extob'
     - 'Extensions/Extoci8'
     - 'Extensions/Extodbc'
     - 'Extensions/Extopcache'
     - 'Extensions/Extopencensus'
     - 'Extensions/Extopenssl'
     - 'Extensions/Extparle'
     - 'Extensions/Extpassword'
     - 'Extensions/Extpcntl'
     - 'Extensions/Extpcov'
     - 'Extensions/Extpcre'
     - 'Extensions/Extpdo'
     - 'Extensions/Extpgsql'
     - 'Extensions/Extphalcon'
     - 'Extensions/Extphar'
     - 'Extensions/Extpkcs11'
     - 'Extensions/Extposix'
     - 'Extensions/Extprotobuf'
     - 'Extensions/Extpspell'
     - 'Extensions/Extpsr'
     - 'Extensions/Extrandom'
     - 'Extensions/Extrar'
     - 'Extensions/Extrdkafka'
     - 'Extensions/Extreadline'
     - 'Extensions/Extredis'
     - 'Extensions/Extreflection'
     - 'Extensions/Extsdl'
     - 'Extensions/Extseaslog'
     - 'Extensions/Extsem'
     - 'Extensions/Extsession'
     - 'Extensions/Extshmop'
     - 'Extensions/Extsimplexml'
     - 'Extensions/Extsnmp'
     - 'Extensions/Extsoap'
     - 'Extensions/Extsockets'
     - 'Extensions/Extsphinx'
     - 'Extensions/Extspl'
     - 'Extensions/Extspx'
     - 'Extensions/Extsqlite'
     - 'Extensions/Extsqlite3'
     - 'Extensions/Extsqlsrv'
     - 'Extensions/Extssh2'
     - 'Extensions/Extstandard'
     - 'Extensions/Extstats'
     - 'Extensions/Extstomp'
     - 'Extensions/Extstring'
     - 'Extensions/Extsuhosin'
     - 'Extensions/Extsvm'
     - 'Extensions/Extswoole'
     - 'Extensions/Exttaint'
     - 'Extensions/Exttidy'
     - 'Extensions/Exttokenizer'
     - 'Extensions/Exttokyotyrant'
     - 'Extensions/Exttrader'
     - 'Extensions/Extuopz'
     - 'Extensions/Extuuid'
     - 'Extensions/Extv8js'
     - 'Extensions/Extvarnish'
     - 'Extensions/Extvips'
     - 'Extensions/Extwasm'
     - 'Extensions/Extwddx'
     - 'Extensions/Extweakref'
     - 'Extensions/Extxattr'
     - 'Extensions/Extxdebug'
     - 'Extensions/Extxdiff'
     - 'Extensions/Extxhprof'
     - 'Extensions/Extxml'
     - 'Extensions/Extxmlrpc'
     - 'Extensions/Extxmlwriter'
     - 'Extensions/Extxsl'
     - 'Extensions/Extxxtea'
     - 'Extensions/Extyaml'
     - 'Extensions/Extyar'
     - 'Extensions/Extzendmonitor'
     - 'Extensions/Extzip'
     - 'Extensions/Extzlib'
     - 'Extensions/Extzmq'
     - 'Extensions/Extzookeeper'
     - 'Files/DefinitionsOnly'
     - 'Files/IsComponent'
     - 'Files/MissingInclude'
     - 'Files/NotDefinitionsOnly'
     - 'Files/Services'
     - 'Functions/AddDefaultValue'
     - 'Functions/AliasesUsage'
     - 'Functions/AvoidBooleanArgument'
     - 'Functions/CancelledParameter'
     - 'Functions/CannotUseStaticForClosure'
     - 'Functions/CantUse'
     - 'Functions/Closure2String'
     - 'Functions/Closures'
     - 'Functions/ConditionedFunctions'
     - 'Functions/CouldBeCallable'
     - 'Functions/CouldBeStaticClosure'
     - 'Functions/CouldCentralize'
     - 'Functions/CouldTypeWithIterable'
     - 'Functions/CouldTypeWithString'
     - 'Functions/CouldTypehint'
     - 'Functions/DeepDefinitions'
     - 'Functions/DeprecatedCallable'
     - 'Functions/DontUseVoid'
     - 'Functions/DuplicateNamedParameter'
     - 'Functions/DynamicCode'
     - 'Functions/EmptyFunction'
     - 'Functions/ExceedingTypehint'
     - 'Functions/FallbackFunction'
     - 'Functions/FnArgumentVariableConfusion'
     - 'Functions/FunctionCalledWithOtherCase'
     - 'Functions/Functionnames'
     - 'Functions/FunctionsUsingReference'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/HardcodedPasswords'
     - 'Functions/HasFluentInterface'
     - 'Functions/HasNotFluentInterface'
     - 'Functions/Identity'
     - 'Functions/InsufficientTypehint'
     - 'Functions/IsExtFunction'
     - 'Functions/IsGenerator'
     - 'Functions/IsGlobal'
     - 'Functions/KillsApp'
     - 'Functions/MismatchParameterAndType'
     - 'Functions/MismatchParameterName'
     - 'Functions/MismatchTypeAndDefault'
     - 'Functions/MismatchedDefaultArguments'
     - 'Functions/MismatchedTypehint'
     - 'Functions/MissingTypehint'
     - 'Functions/ModifyTypedParameter'
     - 'Functions/MultipleDeclarations'
     - 'Functions/MultipleIdenticalClosure'
     - 'Functions/MultipleReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/MustReturn'
     - 'Functions/NoClassAsTypehint'
     - 'Functions/NoDefaultForReference'
     - 'Functions/NoLiteralForReference'
     - 'Functions/NoReferencedVoid'
     - 'Functions/NoReturnUsed'
     - 'Functions/NullTypeFavorite'
     - 'Functions/NullableWithoutCheck'
     - 'Functions/OneLetterFunctions'
     - 'Functions/OnlyVariableForReference'
     - 'Functions/OnlyVariablePassedByReference'
     - 'Functions/OptionalParameter'
     - 'Functions/ParameterHiding'
     - 'Functions/PrefixToType'
     - 'Functions/RealFunctions'
     - 'Functions/Recursive'
     - 'Functions/RedeclaredPhpFunction'
     - 'Functions/RelayFunction'
     - 'Functions/RemoveParameterWithNamedOnes'
     - 'Functions/RetypedReference'
     - 'Functions/SemanticTyping'
     - 'Functions/ShouldBeTypehinted'
     - 'Functions/ShouldUseConstants'
     - 'Functions/TooManyParameters'
     - 'Functions/TooMuchIndented'
     - 'Functions/TypeDodging'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/Typehints'
     - 'Functions/UnknownParameterName'
     - 'Functions/UnsetOnArguments'
     - 'Functions/UnusedFunctions'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UseArrowFunctions'
     - 'Functions/UseConstantAsArguments'
     - 'Functions/UseConstantsAsReturns'
     - 'Functions/UsedFunctions'
     - 'Functions/UselessArgument'
     - 'Functions/UselessDefault'
     - 'Functions/UselessReferenceArgument'
     - 'Functions/UselessTypeCheck'
     - 'Functions/UsesDefaultArguments'
     - 'Functions/VariableArguments'
     - 'Functions/VariableParameterAmbiguityInArrowFunction'
     - 'Functions/VoidIsNotAReference'
     - 'Functions/WrongArgumentNameWithPhpFunction'
     - 'Functions/WrongArgumentType'
     - 'Functions/WrongCase'
     - 'Functions/WrongNumberOfArguments'
     - 'Functions/WrongNumberOfArgumentsMethods'
     - 'Functions/WrongOptionalParameter'
     - 'Functions/WrongReturnedType'
     - 'Functions/WrongTypeWithCall'
     - 'Functions/WrongTypehintedName'
     - 'Functions/funcGetArgModified'
     - 'Interfaces/AlreadyParentsInterface'
     - 'Interfaces/AvoidSelfInInterface'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/CantOverloadConstants'
     - 'Interfaces/CouldUseInterface'
     - 'Interfaces/EmptyInterface'
     - 'Interfaces/InterfaceMethod'
     - 'Interfaces/InterfaceUsage'
     - 'Interfaces/Interfacenames'
     - 'Interfaces/IsExtInterface'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/NoConstructorInInterface'
     - 'Interfaces/NoGaranteeForPropertyConstant'
     - 'Interfaces/Php'
     - 'Interfaces/PossibleInterfaces'
     - 'Interfaces/RepeatedInterface'
     - 'Interfaces/UndefinedInterfaces'
     - 'Interfaces/UnusedInterfaces'
     - 'Interfaces/UsedInterfaces'
     - 'Interfaces/UselessInterfaces'
     - 'Namespaces/Alias'
     - 'Namespaces/AliasConfusion'
     - 'Namespaces/ConstantFullyQualified'
     - 'Namespaces/ConstantWithUseFavorite'
     - 'Namespaces/CouldUseAlias'
     - 'Namespaces/CouldUseMagicConstant'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/GlobalImport'
     - 'Namespaces/HiddenUse'
     - 'Namespaces/MultipleAliasDefinitionPerFile'
     - 'Namespaces/MultipleAliasDefinitions'
     - 'Namespaces/NamespaceUsage'
     - 'Namespaces/Namespacesnames'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Namespaces/OverloadExistingNames'
     - 'Namespaces/ShouldMakeAlias'
     - 'Namespaces/UnresolvedUse'
     - 'Namespaces/UnusedUse'
     - 'Namespaces/UseFunctionsConstants'
     - 'Namespaces/UseWithFullyQualifiedNS'
     - 'Namespaces/UsedUse'
     - 'Namespaces/WrongCase'
     - 'Patterns/AbstractAway'
     - 'Patterns/CourrierAntiPattern'
     - 'Patterns/DependencyInjection'
     - 'Patterns/Factory'
     - 'Patterns/GetterSetter'
     - 'Performances/ArrayKeyExistsSpeedup'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/Autoappend'
     - 'Performances/AvoidArrayPush'
     - 'Performances/CacheVariableOutsideLoop'
     - 'Performances/ClassOperator'
     - 'Performances/CountToAppend'
     - 'Performances/DoInBase'
     - 'Performances/DoubleArrayFlip'
     - 'Performances/EllipsisMerge'
     - 'Performances/FetchOneRowFormat'
     - 'Performances/IssetWholeArray'
     - 'Performances/LogicalToInArray'
     - 'Performances/MakeOneCall'
     - 'Performances/MbStringInLoop'
     - 'Performances/MemoizeMagicCall'
     - 'Performances/NoConcatInLoop'
     - 'Performances/NoGlob'
     - 'Performances/NotCountNull'
     - 'Performances/OptimizeExplode'
     - 'Performances/PHP7EncapsedStrings'
     - 'Performances/Php74ArrayKeyExists'
     - 'Performances/PreCalculateUse'
     - 'Performances/PrePostIncrement'
     - 'Performances/RegexOnArrays'
     - 'Performances/RegexOnCollector'
     - 'Performances/SimpleSwitch'
     - 'Performances/SimplifyForeach'
     - 'Performances/SkipEmptyArray'
     - 'Performances/SlowFunctions'
     - 'Performances/StaticCallDontNeedObjects'
     - 'Performances/StrposTooMuch'
     - 'Performances/SubstrFirst'
     - 'Performances/SubstrInLoops'
     - 'Performances/TooManyExtractions'
     - 'Performances/UseArraySlice'
     - 'Performances/UseBlindVar'
     - 'Performances/timeVsstrtotime'
     - 'Php/ArrayKeyExistsWithObjects'
     - 'Php/AssertFunctionIsReserved'
     - 'Php/Assumptions'
     - 'Php/AutoloadUsage'
     - 'Php/AvoidGetobjectVars'
     - 'Php/AvoidMbDectectEncoding'
     - 'Php/AvoidReal'
     - 'Php/AvoidSetErrorHandlerContextArg'
     - 'Php/BetterRand'
     - 'Php/CallingStaticTraitMethod'
     - 'Php/CantUseReturnValueInWriteContext'
     - 'Php/CaseForPSS'
     - 'Php/CastingUsage'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClassConstWithArray'
     - 'Php/ClassFunctionConfusion'
     - 'Php/CloneConstant'
     - 'Php/CloseTagsConsistency'
     - 'Php/ClosureThisSupport'
     - 'Php/Coalesce'
     - 'Php/CoalesceEqual'
     - 'Php/CompactInexistant'
     - 'Php/ComparisonOnDifferentTypes'
     - 'Php/ConcatAndAddition'
     - 'Php/ConstWithArray'
     - 'Php/CookiesVariables'
     - 'Php/CouldUseIsCountable'
     - 'Php/Crc32MightBeNegative'
     - 'Php/CryptoUsage'
     - 'Php/DateFormats'
     - 'Php/DateTimeNotImmutable'
     - 'Php/DeclareEncoding'
     - 'Php/DeclareStrict'
     - 'Php/DeclareStrictType'
     - 'Php/DeprecateDollarCurly'
     - 'Php/DetectCurrentClass'
     - 'Php/DirectivesUsage'
     - 'Php/DlUsage'
     - 'Php/EnumUsage'
     - 'Php/ErrorLogUsage'
     - 'Php/ExitNoArg'
     - 'Php/ExponentUsage'
     - 'Php/FalseToArray'
     - 'Php/FilesFullPath'
     - 'Php/FilterToAddSlashes'
     - 'Php/FinalConstant'
     - 'Php/FirstClassCallable'
     - 'Php/FlexibleHeredoc'
     - 'Php/FopenMode'
     - 'Php/ForeachDontChangePointer'
     - 'Php/ForeachObject'
     - 'Php/GlobalWithoutSimpleVariable'
     - 'Php/GlobalsVsGlobal'
     - 'Php/Gotonames'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/Haltcompiler'
     - 'Php/HashAlgos71'
     - 'Php/HashAlgos74'
     - 'Php/HashUsesObjects'
     - 'Php/ImplodeOneArg'
     - 'Php/IncomingValues'
     - 'Php/IntegerSeparatorUsage'
     - 'Php/InternalParameterType'
     - 'Php/IsAWithString'
     - 'Php/IsINF'
     - 'Php/IsNAN'
     - 'Php/IsnullVsEqualNull'
     - 'Php/IssetMultipleArgs'
     - 'Php/JsonSerializeReturnType'
     - 'Php/Labelnames'
     - 'Php/LetterCharsLogicalFavorite'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithAppends'
     - 'Php/ListWithKeys'
     - 'Php/MethodCallOnNew'
     - 'Php/MiddleVersion'
     - 'Php/MissingMagicIsset'
     - 'Php/MissingSubpattern'
     - 'Php/MixedKeyword'
     - 'Php/MixedUsage'
     - 'Php/MultipleDeclareStrict'
     - 'Php/MustCallParentConstructor'
     - 'Php/NamedArgumentAndVariadic'
     - 'Php/NamedParameterUsage'
     - 'Php/NativeClassTypeCompatibility'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NeverKeyword'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewExponent'
     - 'Php/NewInitializers'
     - 'Php/NoCastToInt'
     - 'Php/NoClassInGlobal'
     - 'Php/NoListWithString'
     - 'Php/NoNullForNative'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoSubstrMinusOne'
     - 'Php/NotScalarType'
     - 'Php/OnlyVariablePassedByReference'
     - 'Php/OpensslEncryptAlgoChange'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Password55'
     - 'Php/PathinfoReturns'
     - 'Php/PearUsage'
     - 'Php/Php54RemovedFunctions'
     - 'Php/Php55NewFunctions'
     - 'Php/Php55RemovedFunctions'
     - 'Php/Php56NewFunctions'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php70RemovedDirective'
     - 'Php/Php70RemovedFunctions'
     - 'Php/Php71NewClasses'
     - 'Php/Php71NewFunctions'
     - 'Php/Php71RemovedDirective'
     - 'Php/Php71microseconds'
     - 'Php/Php72Deprecation'
     - 'Php/Php72NewClasses'
     - 'Php/Php72NewConstants'
     - 'Php/Php72NewFunctions'
     - 'Php/Php72ObjectKeyword'
     - 'Php/Php73NewFunctions'
     - 'Php/Php74Deprecation'
     - 'Php/Php74NewClasses'
     - 'Php/Php74NewConstants'
     - 'Php/Php74NewFunctions'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php74RemovedFunctions'
     - 'Php/Php74ReservedKeyword'
     - 'Php/Php74mbstrrpos3rdArg'
     - 'Php/Php80NamedParameterVariadic'
     - 'Php/Php80NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80RemovedConstant'
     - 'Php/Php80RemovedDirective'
     - 'Php/Php80RemovedFunctions'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php80VariableSyntax'
     - 'Php/Php81NewTypes'
     - 'Php/Php81RemovedDirective'
     - 'Php/Php81RemovesResources'
     - 'Php/Php82NewFunctions'
     - 'Php/Php82NewTypes'
     - 'Php/Php83NewClasses'
     - 'Php/Php83NewFunctions'
     - 'Php/PhpErrorMsgUsage'
     - 'Php/PregMatchAllFlag'
     - 'Php/Prints'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/ReflectionExportIsDeprecated'
     - 'Php/ReservedKeywords7'
     - 'Php/ReservedMethods'
     - 'Php/ReservedNames'
     - 'Php/RestrictGlobalUsage'
     - 'Php/ReturnTypehintUsage'
     - 'Php/ReturnWithParenthesis'
     - 'Php/SafePhpvars'
     - 'Php/ScalarAreNotArrays'
     - 'Php/ScalarTypehintUsage'
     - 'Php/SerializeMagic'
     - 'Php/SessionVariables'
     - 'Php/SetExceptionHandlerPHP7'
     - 'Php/SetHandlers'
     - 'Php/ShellFavorite'
     - 'Php/ShortOpenTagRequired'
     - 'Php/ShortTernary'
     - 'Php/ShouldPreprocess'
     - 'Php/ShouldUseArrayColumn'
     - 'Php/ShouldUseArrayFilter'
     - 'Php/ShouldUseCoalesce'
     - 'Php/ShouldUseFunction'
     - 'Php/SpreadOperatorForArray'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/StaticclassUsage'
     - 'Php/StringIntComparison'
     - 'Php/StrposWithIntegers'
     - 'Php/StrtrArguments'
     - 'Php/SuperGlobalUsage'
     - 'Php/ThrowUsage'
     - 'Php/ThrowWasAnExpression'
     - 'Php/TooManyNativeCalls'
     - 'Php/TrailingComma'
     - 'Php/TriggerErrorUsage'
     - 'Php/TryCatchUsage'
     - 'Php/TryMultipleCatch'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnknownPcre2Option'
     - 'Php/UnsetOrCast'
     - 'Php/UpperCaseFunction'
     - 'Php/UpperCaseKeyword'
     - 'Php/UseAttributes'
     - 'Php/UseBrowscap'
     - 'Php/UseCli'
     - 'Php/UseContravariance'
     - 'Php/UseCookies'
     - 'Php/UseDateTimeImmutable'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseMatch'
     - 'Php/UseNullSafeOperator'
     - 'Php/UseNullableType'
     - 'Php/UseObjectApi'
     - 'Php/UsePathinfo'
     - 'Php/UsePathinfoArgs'
     - 'Php/UseSessionStartOptions'
     - 'Php/UseSetCookie'
     - 'Php/UseStrContains'
     - 'Php/UsortSorting'
     - 'Php/Utf8EncodeDeprecated'
     - 'Php/VersionCompareOperator'
     - 'Php/WrongAttributeConfiguration'
     - 'Php/WrongTypeForNativeFunction'
     - 'Php/YieldFromUsage'
     - 'Php/YieldUsage'
     - 'Php/debugInfoUsage'
     - 'Portability/FopenMode'
     - 'Portability/GlobBraceUsage'
     - 'Portability/IconvTranslit'
     - 'Portability/LinuxOnlyFiles'
     - 'Portability/WindowsOnlyConstants'
     - 'Project/IsLibrary'
     - 'Psr/Psr11Usage'
     - 'Psr/Psr13Usage'
     - 'Psr/Psr16Usage'
     - 'Psr/Psr3Usage'
     - 'Psr/Psr6Usage'
     - 'Psr/Psr7Usage'
     - 'Security/AnchorRegex'
     - 'Security/AvoidThoseCrypto'
     - 'Security/CantDisableClass'
     - 'Security/CantDisableFunction'
     - 'Security/CompareHash'
     - 'Security/ConfigureExtract'
     - 'Security/CryptoKeyLength'
     - 'Security/CurlOptions'
     - 'Security/DirectInjection'
     - 'Security/DontEchoError'
     - 'Security/DynamicDl'
     - 'Security/EncodedLetters'
     - 'Security/FilterInputSource'
     - 'Security/FilterNotRaw'
     - 'Security/GPRAliases'
     - 'Security/IncompatibleTypesWithIncoming'
     - 'Security/IndirectInjection'
     - 'Security/IntegerConversion'
     - 'Security/KeepFilesRestricted'
     - 'Security/MinusOneOnError'
     - 'Security/MkdirDefault'
     - 'Security/MoveUploadedFile'
     - 'Security/NoEntIgnore'
     - 'Security/NoNetForXmlLoad'
     - 'Security/NoSleep'
     - 'Security/NoWeakSSLCrypto'
     - 'Security/RegisterGlobals'
     - 'Security/SafeHttpHeaders'
     - 'Security/SensitiveArgument'
     - 'Security/SessionCachedData'
     - 'Security/SessionLazyWrite'
     - 'Security/SetCookieArgs'
     - 'Security/ShouldUsePreparedStatement'
     - 'Security/ShouldUseSessionRegenerateId'
     - 'Security/Sqlite3RequiresSingleQuotes'
     - 'Security/SuperGlobalContagion'
     - 'Security/UnserializeSecondArg'
     - 'Security/UploadFilenameInjection'
     - 'Security/parseUrlWithoutParameters'
     - 'Structures/AlternativeConsistenceByFile'
     - 'Structures/AlwaysFalse'
     - 'Structures/ArrayAccessOnLiteralArray'
     - 'Structures/ArrayAddition'
     - 'Structures/ArrayCountTripleEqual'
     - 'Structures/ArrayMapPassesByValue'
     - 'Structures/ArrayMergeAndVariadic'
     - 'Structures/ArrayMergeArrayArray'
     - 'Structures/ArrayMergeWithEllipsis'
     - 'Structures/ArraySearchMultipleKeys'
     - 'Structures/AssignedInOneBranch'
     - 'Structures/BailOutEarly'
     - 'Structures/BasenameSuffix'
     - 'Structures/BlindVariableUsedBeyondLoop'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/Bracketless'
     - 'Structures/Break0'
     - 'Structures/BreakNonInteger'
     - 'Structures/BreakOutsideLoop'
     - 'Structures/BuriedAssignation'
     - 'Structures/CalltimePassByReference'
     - 'Structures/CastFavorite'
     - 'Structures/CastToBoolean'
     - 'Structures/CastingTernary'
     - 'Structures/CatchShadowsVariable'
     - 'Structures/CheckAllTypes'
     - 'Structures/CheckDivision'
     - 'Structures/CoalesceAndConcat'
     - 'Structures/CoalesceNullCoalesce'
     - 'Structures/CommonAlternatives'
     - 'Structures/ComparedButNotAssignedStrings'
     - 'Structures/ComparedComparison'
     - 'Structures/ComparisonFavorite'
     - 'Structures/ComplexExpression'
     - 'Structures/ConcatenationInterpolationFavorite'
     - 'Structures/ConditionalStructures'
     - 'Structures/ConstDefineFavorite'
     - 'Structures/ConstantConditions'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/CouldBeArrayCombine'
     - 'Structures/CouldBeElse'
     - 'Structures/CouldBeSpaceship'
     - 'Structures/CouldBeStatic'
     - 'Structures/CouldBeTernary'
     - 'Structures/CouldCastToArray'
     - 'Structures/CouldUseArraySum'
     - 'Structures/CouldUseArrayUnique'
     - 'Structures/CouldUseCompact'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseMatch'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrContains'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/CouldUseYieldFrom'
     - 'Structures/CountIsNotNegative'
     - 'Structures/CryptWithoutSalt'
     - 'Structures/CurlVersionNow'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/DateTimePreference'
     - 'Structures/DeclareStaticOnce'
     - 'Structures/DefaultThenDiscard'
     - 'Structures/DeprecatedMbEncoding'
     - 'Structures/DereferencingAS'
     - 'Structures/DifferencePreference'
     - 'Structures/DirThenSlash'
     - 'Structures/DirectlyUseFile'
     - 'Structures/DontAddSeconds'
     - 'Structures/DontChangeBlindKey'
     - 'Structures/DontCompareTypedBoolean'
     - 'Structures/DontLoopOnYield'
     - 'Structures/DontMixPlusPlus'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Structures/DontReuseForeachSource'
     - 'Structures/DontUseTheTypeAsVariable'
     - 'Structures/DoubleAssignation'
     - 'Structures/DoubleChecks'
     - 'Structures/DoubleInstruction'
     - 'Structures/DoubleObjectAssignation'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/DuplicateCalls'
     - 'Structures/DynamicCalls'
     - 'Structures/EchoPrintConsistance'
     - 'Structures/EchoWithConcat'
     - 'Structures/ElseUsage'
     - 'Structures/EmptyBlocks'
     - 'Structures/EmptyJsonError'
     - 'Structures/EmptyLines'
     - 'Structures/EmptyLoop'
     - 'Structures/EmptyWithExpression'
     - 'Structures/ErrorMessages'
     - 'Structures/EvalUsage'
     - 'Structures/EvalWithoutTry'
     - 'Structures/ExitUsage'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/Fallthrough'
     - 'Structures/FilePutContentsDataType'
     - 'Structures/FileUploadUsage'
     - 'Structures/FileUsage'
     - 'Structures/ForWithFunctioncall'
     - 'Structures/ForeachNeedReferencedSource'
     - 'Structures/ForeachReferenceIsNotModified'
     - 'Structures/ForeachSourceValue'
     - 'Structures/ForeachWithList'
     - 'Structures/FunctionPreSubscripting'
     - 'Structures/FunctionSubscripting'
     - 'Structures/GetClassWithoutArg'
     - 'Structures/GlobalInGlobal'
     - 'Structures/GlobalOutsideLoop'
     - 'Structures/GlobalUsage'
     - 'Structures/GoToKeyDirectly'
     - 'Structures/GtOrLtFavorite'
     - 'Structures/HeredocDelimiterFavorite'
     - 'Structures/Htmlentitiescall'
     - 'Structures/HtmlentitiescallDefaultFlag'
     - 'Structures/IdenticalCase'
     - 'Structures/IdenticalConditions'
     - 'Structures/IdenticalConsecutive'
     - 'Structures/IdenticalElseif'
     - 'Structures/IdenticalOnBothSides'
     - 'Structures/IdenticalVariablesInForeach'
     - 'Structures/IfThenReturnFavorite'
     - 'Structures/IfWithSameConditions'
     - 'Structures/Iffectation'
     - 'Structures/ImplicitGlobal'
     - 'Structures/ImpliedIf'
     - 'Structures/ImplodeArgsOrder'
     - 'Structures/IncludeUsage'
     - 'Structures/InconsistentElseif'
     - 'Structures/IndicesAreIntOrString'
     - 'Structures/InfiniteRecursion'
     - 'Structures/InitThenIf'
     - 'Structures/InvalidCast'
     - 'Structures/InvalidDateScanningFormat'
     - 'Structures/InvalidPackFormat'
     - 'Structures/InvalidRegex'
     - 'Structures/IsZero'
     - 'Structures/IssetWithConstant'
     - 'Structures/JsonEncodeExceptions'
     - 'Structures/JsonWithOption'
     - 'Structures/LogicalMistakes'
     - 'Structures/LoneBlock'
     - 'Structures/LongArguments'
     - 'Structures/LongBlock'
     - 'Structures/MailUsage'
     - 'Structures/MaxLevelOfIdentation'
     - 'Structures/MbStringNonEncodings'
     - 'Structures/MbstringThirdArg'
     - 'Structures/MbstringUnknownEncoding'
     - 'Structures/McryptcreateivWithoutOption'
     - 'Structures/MergeIfThen'
     - 'Structures/MergeTernaryIntoIfthen'
     - 'Structures/MismatchedTernary'
     - 'Structures/MissingAssignation'
     - 'Structures/MissingCases'
     - 'Structures/MissingNew'
     - 'Structures/MissingParenthesis'
     - 'Structures/MisusedYield'
     - 'Structures/ModernEmpty'
     - 'Structures/MultilineExpressions'
     - 'Structures/MultipleCatch'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultipleSimilarCalls'
     - 'Structures/MultipleTypeCasesInSwitch'
     - 'Structures/MultipleTypeVariable'
     - 'Structures/NamedRegex'
     - 'Structures/NegativePow'
     - 'Structures/NestedIfthen'
     - 'Structures/NestedLoops'
     - 'Structures/NestedMatch'
     - 'Structures/NestedTernary'
     - 'Structures/NeverNegative'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoAppendOnSource'
     - 'Structures/NoArrayUnique'
     - 'Structures/NoAssignationInFunction'
     - 'Structures/NoChangeIncomingVariables'
     - 'Structures/NoChoice'
     - 'Structures/NoDirectAccess'
     - 'Structures/NoDirectUsage'
     - 'Structures/NoEmptyStringWithExplode'
     - 'Structures/NoGetClassNull'
     - 'Structures/NoHardcodedHash'
     - 'Structures/NoHardcodedIp'
     - 'Structures/NoHardcodedPath'
     - 'Structures/NoHardcodedPort'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/NoMaxOnEmptyArray'
     - 'Structures/NoNeedForElse'
     - 'Structures/NoNeedForTriple'
     - 'Structures/NoNullForIndex'
     - 'Structures/NoObjectAsIndex'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoReferenceOnLeft'
     - 'Structures/NoReturnInFinally'
     - 'Structures/NoSubstrOne'
     - 'Structures/NoValidCast'
     - 'Structures/NoVariableIsACondition'
     - 'Structures/NonBreakableSpaceInNames'
     - 'Structures/NonIntStringAsIndex'
     - 'Structures/Noscream'
     - 'Structures/NotEqual'
     - 'Structures/NotNot'
     - 'Structures/ObjectReferences'
     - 'Structures/OnceUsage'
     - 'Structures/OneDotOrObjectOperatorPerLine'
     - 'Structures/OneExpressionBracketsConsistency'
     - 'Structures/OneIfIsSufficient'
     - 'Structures/OneLevelOfIndentation'
     - 'Structures/OneLineTwoInstructions'
     - 'Structures/OnlyFirstByte'
     - 'Structures/OpensslRandomPseudoByteSecondArg'
     - 'Structures/OverwrittenForeachVar'
     - 'Structures/PHP7Dirname'
     - 'Structures/PhpinfoUsage'
     - 'Structures/PlusEgalOne'
     - 'Structures/PossibleIncrement'
     - 'Structures/PossibleInfiniteLoop'
     - 'Structures/PrintAndDie'
     - 'Structures/PrintWithoutParenthesis'
     - 'Structures/QueriesInLoop'
     - 'Structures/RandomWithoutTry'
     - 'Structures/RecalledCondition'
     - 'Structures/RegexDelimiter'
     - 'Structures/RepeatedPrint'
     - 'Structures/RepeatedRegex'
     - 'Structures/ResourcesUsage'
     - 'Structures/ResultMayBeMissing'
     - 'Structures/ReturnTrueFalse'
     - 'Structures/ReturnVoid'
     - 'Structures/ReuseVariable'
     - 'Structures/SGVariablesConfusion'
     - 'Structures/SameConditions'
     - 'Structures/SequenceInFor'
     - 'Structures/SetlocaleNeedsConstants'
     - 'Structures/ShellUsage'
     - 'Structures/ShortOrCompleteComparison'
     - 'Structures/ShortTags'
     - 'Structures/ShouldChainException'
     - 'Structures/ShouldMakeTernary'
     - 'Structures/ShouldPreprocess'
     - 'Structures/ShouldUseExplodeArgs'
     - 'Structures/ShouldUseForeach'
     - 'Structures/ShouldUseMath'
     - 'Structures/ShouldUseOperator'
     - 'Structures/SimplePreg'
     - 'Structures/SprintfFormatCompilation'
     - 'Structures/StaticInclude'
     - 'Structures/StaticLoop'
     - 'Structures/StrictInArrayFavorite'
     - 'Structures/StringInterpolationFavorite'
     - 'Structures/StripTagsSkipsClosedTag'
     - 'Structures/StrposCompare'
     - 'Structures/StrposLessThanOne'
     - 'Structures/SubstrLastArg'
     - 'Structures/SubstrToTrim'
     - 'Structures/SuspiciousComparison'
     - 'Structures/SwitchToSwitch'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/SwitchWithoutDefault'
     - 'Structures/TernaryInConcat'
     - 'Structures/TestThenCast'
     - 'Structures/ThrowsAndAssign'
     - 'Structures/TimestampDifference'
     - 'Structures/TooManyChainedCalls'
     - 'Structures/TooManyElseif'
     - 'Structures/TryFinally'
     - 'Structures/UncheckedResources'
     - 'Structures/UnknownPregOption'
     - 'Structures/Unpreprocessed'
     - 'Structures/UnreachableCode'
     - 'Structures/UnsetInForeach'
     - 'Structures/UnsupportedOperandTypes'
     - 'Structures/UnsupportedTypesWithOperators'
     - 'Structures/UnusedGlobal'
     - 'Structures/UnusedLabel'
     - 'Structures/UseArrayFunctions'
     - 'Structures/UseCaseValue'
     - 'Structures/UseConstant'
     - 'Structures/UseCountRecursive'
     - 'Structures/UseDebug'
     - 'Structures/UseFileAppend'
     - 'Structures/UseInstanceof'
     - 'Structures/UseListWithForeach'
     - 'Structures/UsePositiveCondition'
     - 'Structures/UseStrEndsWith'
     - 'Structures/UseStrStartsWith'
     - 'Structures/UseSystemTmp'
     - 'Structures/UseUrlQueryFunctions'
     - 'Structures/UseVariableInsideLoop'
     - 'Structures/UselessBrackets'
     - 'Structures/UselessCasting'
     - 'Structures/UselessCoalesce'
     - 'Structures/UselessGlobal'
     - 'Structures/UselessInstruction'
     - 'Structures/UselessNullCoalesce'
     - 'Structures/UselessParenthesis'
     - 'Structures/UselessShortTernary'
     - 'Structures/UselessSwitch'
     - 'Structures/UselessTrailingComma'
     - 'Structures/UselessUnset'
     - 'Structures/VardumpUsage'
     - 'Structures/VariableGlobal'
     - 'Structures/VariableMayBeNonGlobal'
     - 'Structures/WhileListEach'
     - 'Structures/WrongLocale'
     - 'Structures/WrongPrecedenceInExpression'
     - 'Structures/WrongRange'
     - 'Structures/YodaComparison'
     - 'Structures/pregOptionE'
     - 'Structures/strOrMbFavorite'
     - 'Structures/toStringThrowsException'
     - 'Traits/CannotCallTraitMethod'
     - 'Traits/ConstantsInTraits'
     - 'Traits/CouldUseTrait'
     - 'Traits/DependantTrait'
     - 'Traits/EmptyTrait'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/IncompatibleProperty'
     - 'Traits/IsExtTrait'
     - 'Traits/LocallyUsedProperty'
     - 'Traits/MethodCollisionTraits'
     - 'Traits/MultipleUsage'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Traits/Php'
     - 'Traits/SelfUsingTrait'
     - 'Traits/SidelinedMethod'
     - 'Traits/TraitMethod'
     - 'Traits/TraitNotFound'
     - 'Traits/TraitUsage'
     - 'Traits/Traitnames'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UnusedClassTrait'
     - 'Traits/UnusedTrait'
     - 'Traits/UsedTrait'
     - 'Traits/UselessAlias'
     - 'Type/ArrayIndex'
     - 'Type/Binary'
     - 'Type/CharString'
     - 'Type/Continents'
     - 'Type/DuplicateLiteral'
     - 'Type/Email'
     - 'Type/GPCIndex'
     - 'Type/Heredoc'
     - 'Type/Hexadecimal'
     - 'Type/HexadecimalString'
     - 'Type/HttpHeader'
     - 'Type/HttpStatus'
     - 'Type/IncomingDateFormat'
     - 'Type/Ip'
     - 'Type/MalformedOctal'
     - 'Type/Md5String'
     - 'Type/MimeType'
     - 'Type/NoRealComparison'
     - 'Type/Nowdoc'
     - 'Type/Octal'
     - 'Type/OctalInString'
     - 'Type/OneVariableStrings'
     - 'Type/OpensslCipher'
     - 'Type/Pack'
     - 'Type/Path'
     - 'Type/Pcre'
     - 'Type/Ports'
     - 'Type/Printf'
     - 'Type/Protocols'
     - 'Type/Regex'
     - 'Type/Sapi'
     - 'Type/Shellcommands'
     - 'Type/ShouldBeSingleQuote'
     - 'Type/ShouldTypecast'
     - 'Type/SilentlyCastInteger'
     - 'Type/SimilarIntegers'
     - 'Type/SpecialIntegers'
     - 'Type/Sql'
     - 'Type/StringHoldAVariable'
     - 'Type/StringInterpolation'
     - 'Type/StringWithStrangeSpace'
     - 'Type/UdpDomains'
     - 'Type/UnicodeBlock'
     - 'Type/Url'
     - 'Typehints/CouldBeCIT'
     - 'Typehints/CouldBeCallable'
     - 'Typehints/CouldBeGenerator'
     - 'Typehints/CouldBeNever'
     - 'Typehints/CouldBeParent'
     - 'Typehints/CouldBeResource'
     - 'Typehints/CouldBeSelf'
     - 'Typehints/CouldBeVoid'
     - 'Typehints/CouldNotType'
     - 'Typehints/MissingReturntype'
     - 'Typehints/StandaloneTypeTFN'
     - 'Typehints/WrongTypeWithDefault'
     - 'Utils/Selector'
     - 'Variables/AmbiguousTypes'
     - 'Variables/AssignedTwiceOrMore'
     - 'Variables/Blind'
     - 'Variables/CloseNaming'
     - 'Variables/ComplexDynamicNames'
     - 'Variables/ConstantTypo'
     - 'Variables/Globals'
     - 'Variables/InconsistentUsage'
     - 'Variables/InheritedStaticVariable'
     - 'Variables/InterfaceArguments'
     - 'Variables/IsLocalConstant'
     - 'Variables/LocalGlobals'
     - 'Variables/LostReferences'
     - 'Variables/NoInitialS'
     - 'Variables/NoStaticVarInMethod'
     - 'Variables/Overwriting'
     - 'Variables/OverwrittenLiterals'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RealVariables'
     - 'Variables/RedeclaredStaticVariable'
     - 'Variables/References'
     - 'Variables/SelfTransform'
     - 'Variables/StaticVariableInitialisation'
     - 'Variables/StaticVariables'
     - 'Variables/StrangeName'
     - 'Variables/UncommonEnvVar'
     - 'Variables/UndefinedConstantName'
     - 'Variables/VariableLong'
     - 'Variables/VariableNonascii'
     - 'Variables/VariableOneLetter'
     - 'Variables/VariableUppercase'
     - 'Variables/VariableUsedOnce'
     - 'Variables/VariableUsedOnceByContext'
     - 'Variables/WrittenOnlyVariable'
     - 'Vendors/Cakephp'
     - 'Vendors/Codeigniter'
     - 'Vendors/Concrete5'
     - 'Vendors/Drupal'
     - 'Vendors/Feast'
     - 'Vendors/Fuel'
     - 'Vendors/Joomla'
     - 'Vendors/Laravel'
     - 'Vendors/Neos'
     - 'Vendors/Phalcon'
     - 'Vendors/Sylius'
     - 'Vendors/Symfony'
     - 'Vendors/Typo3'
     - 'Vendors/Wordpress'
     - 'Vendors/Yii'




.. _annex-class-review:

Class Review
############


.. _annex-ini-class-review:

Class Review for INI
++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Class Review]
   analyzer[] = "Classes/AbstractConstants";
   analyzer[] = "Classes/AvoidOptionArrays";
   analyzer[] = "Classes/CancelCommonMethod";
   analyzer[] = "Classes/CannotBeReadonly";
   analyzer[] = "Classes/CantInstantiateNonClass";
   analyzer[] = "Classes/CantOverwriteFinalConstant";
   analyzer[] = "Classes/ClassInvasion";
   analyzer[] = "Classes/ConstantClass";
   analyzer[] = "Classes/CouldBeAbstractClass";
   analyzer[] = "Classes/CouldBeClassConstant";
   analyzer[] = "Classes/CouldBeFinal";
   analyzer[] = "Classes/CouldBeParentMethod";
   analyzer[] = "Classes/CouldBePrivate";
   analyzer[] = "Classes/CouldBePrivateConstante";
   analyzer[] = "Classes/CouldBePrivateMethod";
   analyzer[] = "Classes/CouldBeProtectedConstant";
   analyzer[] = "Classes/CouldBeProtectedMethod";
   analyzer[] = "Classes/CouldBeProtectedProperty";
   analyzer[] = "Classes/CouldBeReadonly";
   analyzer[] = "Classes/CouldBeReadonlyProperty";
   analyzer[] = "Classes/CouldBeStatic";
   analyzer[] = "Classes/CouldBeStringable";
   analyzer[] = "Classes/CouldInjectParam";
   analyzer[] = "Classes/CouldSetPropertyDefault";
   analyzer[] = "Classes/CyclicReferences";
   analyzer[] = "Classes/DependantAbstractClass";
   analyzer[] = "Classes/DifferentArgumentCounts";
   analyzer[] = "Classes/DisconnectedClasses";
   analyzer[] = "Classes/ExportProperty";
   analyzer[] = "Classes/FinalByOcramius";
   analyzer[] = "Classes/FinalPrivate";
   analyzer[] = "Classes/Finalclass";
   analyzer[] = "Classes/Finalmethod";
   analyzer[] = "Classes/FossilizedMethod";
   analyzer[] = "Classes/HiddenNullable";
   analyzer[] = "Classes/IncompatibleConstructor";
   analyzer[] = "Classes/InheritedPropertyMustMatch";
   analyzer[] = "Classes/InsufficientPropertyTypehint";
   analyzer[] = "Classes/LoweredAccessLevel";
   analyzer[] = "Classes/MagicMethodReturntypes";
   analyzer[] = "Classes/MismatchProperties";
   analyzer[] = "Classes/MissingAbstractMethod";
   analyzer[] = "Classes/MissingVisibility";
   analyzer[] = "Classes/MultiplePropertyDeclaration";
   analyzer[] = "Classes/MutualExtension";
   analyzer[] = "Classes/NewThenCall";
   analyzer[] = "Classes/NoNullWithNullSafeOperator";
   analyzer[] = "Classes/NoParent";
   analyzer[] = "Classes/NoReadonlyAssignationInGlobal";
   analyzer[] = "Classes/NoSelfReferencingConstant";
   analyzer[] = "Classes/NonNullableSetters";
   analyzer[] = "Classes/ParentIsNotStatic";
   analyzer[] = "Classes/PropertyCouldBeLocal";
   analyzer[] = "Classes/PropertyInvasion";
   analyzer[] = "Classes/PropertyMethodSameName";
   analyzer[] = "Classes/RaisedAccessLevel";
   analyzer[] = "Classes/RedefinedMethods";
   analyzer[] = "Classes/RedefinedProperty";
   analyzer[] = "Classes/RewroteFinalClassConstant";
   analyzer[] = "Classes/ShouldUseSelf";
   analyzer[] = "Classes/StaticCannotCallNonStatic";
   analyzer[] = "Classes/UndeclaredStaticProperty";
   analyzer[] = "Classes/UndefinedMethod";
   analyzer[] = "Classes/UnfinishedObject";
   analyzer[] = "Classes/UninitedProperty";
   analyzer[] = "Classes/UnreachableConstant";
   analyzer[] = "Classes/UnreachableMethod";
   analyzer[] = "Classes/UntypedNoDefaultProperties";
   analyzer[] = "Classes/UnusedConstant";
   analyzer[] = "Classes/UselessAssignationOfPromotedProperty";
   analyzer[] = "Classes/UselessConstantOverwrite";
   analyzer[] = "Classes/UselessNullSafeOperator";
   analyzer[] = "Classes/UselessTypehint";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Enums/NoMagicMethod";
   analyzer[] = "Enums/UndefinedEnumcase";
   analyzer[] = "Exceptions/SetChainingException";
   analyzer[] = "Functions/ExceedingTypehint";
   analyzer[] = "Functions/ModifyTypedParameter";
   analyzer[] = "Functions/NullableWithoutCheck";
   analyzer[] = "Functions/TypeDodging";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Interfaces/AvoidSelfInInterface";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/NoConstructorInInterface";
   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
   analyzer[] = "Interfaces/UselessInterfaces";
   analyzer[] = "Performances/MemoizeMagicCall";
   analyzer[] = "Performances/StaticCallWithSelf";
   analyzer[] = "Php/MissingMagicIsset";
   analyzer[] = "Structures/CouldBeStatic";
   analyzer[] = "Structures/DoubleObjectAssignation";
   analyzer[] = "Traits/IncompatibleProperty";
   analyzer[] = "Traits/SelfUsingTrait";
   analyzer[] = "Traits/SidelinedMethod";
   analyzer[] = "Traits/TraitIsNotAType";
   analyzer[] = "Traits/UnusedClassTrait";
   analyzer[] = "Traits/UsedOnceTrait";
   analyzer[] = "Typehints/WrongTypeWithDefault";
   analyzer[] = "Variables/NoStaticVarInMethod";


.. _annex-yaml-class-review:

Class Review for .exakat.yaml
+++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Class Review':
     - 'Classes/AbstractConstants'
     - 'Classes/AvoidOptionArrays'
     - 'Classes/CancelCommonMethod'
     - 'Classes/CannotBeReadonly'
     - 'Classes/CantInstantiateNonClass'
     - 'Classes/CantOverwriteFinalConstant'
     - 'Classes/ClassInvasion'
     - 'Classes/ConstantClass'
     - 'Classes/CouldBeAbstractClass'
     - 'Classes/CouldBeClassConstant'
     - 'Classes/CouldBeFinal'
     - 'Classes/CouldBeParentMethod'
     - 'Classes/CouldBePrivate'
     - 'Classes/CouldBePrivateConstante'
     - 'Classes/CouldBePrivateMethod'
     - 'Classes/CouldBeProtectedConstant'
     - 'Classes/CouldBeProtectedMethod'
     - 'Classes/CouldBeProtectedProperty'
     - 'Classes/CouldBeReadonly'
     - 'Classes/CouldBeReadonlyProperty'
     - 'Classes/CouldBeStatic'
     - 'Classes/CouldBeStringable'
     - 'Classes/CouldInjectParam'
     - 'Classes/CouldSetPropertyDefault'
     - 'Classes/CyclicReferences'
     - 'Classes/DependantAbstractClass'
     - 'Classes/DifferentArgumentCounts'
     - 'Classes/DisconnectedClasses'
     - 'Classes/ExportProperty'
     - 'Classes/FinalByOcramius'
     - 'Classes/FinalPrivate'
     - 'Classes/Finalclass'
     - 'Classes/Finalmethod'
     - 'Classes/FossilizedMethod'
     - 'Classes/HiddenNullable'
     - 'Classes/IncompatibleConstructor'
     - 'Classes/InheritedPropertyMustMatch'
     - 'Classes/InsufficientPropertyTypehint'
     - 'Classes/LoweredAccessLevel'
     - 'Classes/MagicMethodReturntypes'
     - 'Classes/MismatchProperties'
     - 'Classes/MissingAbstractMethod'
     - 'Classes/MissingVisibility'
     - 'Classes/MultiplePropertyDeclaration'
     - 'Classes/MutualExtension'
     - 'Classes/NewThenCall'
     - 'Classes/NoNullWithNullSafeOperator'
     - 'Classes/NoParent'
     - 'Classes/NoReadonlyAssignationInGlobal'
     - 'Classes/NoSelfReferencingConstant'
     - 'Classes/NonNullableSetters'
     - 'Classes/ParentIsNotStatic'
     - 'Classes/PropertyCouldBeLocal'
     - 'Classes/PropertyInvasion'
     - 'Classes/PropertyMethodSameName'
     - 'Classes/RaisedAccessLevel'
     - 'Classes/RedefinedMethods'
     - 'Classes/RedefinedProperty'
     - 'Classes/RewroteFinalClassConstant'
     - 'Classes/ShouldUseSelf'
     - 'Classes/StaticCannotCallNonStatic'
     - 'Classes/UndeclaredStaticProperty'
     - 'Classes/UndefinedMethod'
     - 'Classes/UnfinishedObject'
     - 'Classes/UninitedProperty'
     - 'Classes/UnreachableConstant'
     - 'Classes/UnreachableMethod'
     - 'Classes/UntypedNoDefaultProperties'
     - 'Classes/UnusedConstant'
     - 'Classes/UselessAssignationOfPromotedProperty'
     - 'Classes/UselessConstantOverwrite'
     - 'Classes/UselessNullSafeOperator'
     - 'Classes/UselessTypehint'
     - 'Classes/WrongTypedPropertyInit'
     - 'Enums/NoMagicMethod'
     - 'Enums/UndefinedEnumcase'
     - 'Exceptions/SetChainingException'
     - 'Functions/ExceedingTypehint'
     - 'Functions/ModifyTypedParameter'
     - 'Functions/NullableWithoutCheck'
     - 'Functions/TypeDodging'
     - 'Functions/WrongReturnedType'
     - 'Interfaces/AvoidSelfInInterface'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/NoConstructorInInterface'
     - 'Interfaces/NoGaranteeForPropertyConstant'
     - 'Interfaces/UselessInterfaces'
     - 'Performances/MemoizeMagicCall'
     - 'Performances/StaticCallWithSelf'
     - 'Php/MissingMagicIsset'
     - 'Structures/CouldBeStatic'
     - 'Structures/DoubleObjectAssignation'
     - 'Traits/IncompatibleProperty'
     - 'Traits/SelfUsingTrait'
     - 'Traits/SidelinedMethod'
     - 'Traits/TraitIsNotAType'
     - 'Traits/UnusedClassTrait'
     - 'Traits/UsedOnceTrait'
     - 'Typehints/WrongTypeWithDefault'
     - 'Variables/NoStaticVarInMethod'




.. _annex-classdependencies:

Classdependencies
#################


.. _annex-ini-classdependencies:

Classdependencies for INI
+++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Classdependencies]
   analyzer[] = "Dump/CollectClassesDependencies";


.. _annex-yaml-classdependencies:

Classdependencies for .exakat.yaml
++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Classdependencies':
     - 'Dump/CollectClassesDependencies'




.. _annex-coding-conventions:

Coding conventions
##################


.. _annex-ini-coding-conventions:

Coding conventions for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Coding conventions]
   analyzer[] = "Arrays/EmptySlots";
   analyzer[] = "Arrays/MistakenConcatenation";
   analyzer[] = "Classes/MultipleClassesInFile";
   analyzer[] = "Classes/MultiplePropertyDeclarationOnOneLine";
   analyzer[] = "Classes/OrderOfDeclaration";
   analyzer[] = "Classes/WrongCase";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Functions/OneLetterFunctions";
   analyzer[] = "Functions/WrongCase";
   analyzer[] = "Functions/WrongTypehintedName";
   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
   analyzer[] = "Namespaces/WrongCase";
   analyzer[] = "Php/CloseTags";
   analyzer[] = "Php/ReturnWithParenthesis";
   analyzer[] = "Php/UpperCaseFunction";
   analyzer[] = "Php/UpperCaseKeyword";
   analyzer[] = "Structures/Bracketless";
   analyzer[] = "Structures/ConstantComparisonConsistance";
   analyzer[] = "Structures/DontBeTooManual";
   analyzer[] = "Structures/EchoPrintConsistance";
   analyzer[] = "Structures/HeredocDelimiterFavorite";
   analyzer[] = "Structures/MixedConcatInterpolation";
   analyzer[] = "Structures/PlusEgalOne";
   analyzer[] = "Structures/UselessTrailingComma";
   analyzer[] = "Structures/YodaComparison";
   analyzer[] = "Type/ShouldBeSingleQuote";
   analyzer[] = "Type/SimilarIntegers";
   analyzer[] = "Type/StringInterpolation";
   analyzer[] = "Variables/VariableUppercase";


.. _annex-yaml-coding-conventions:

Coding conventions for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Coding conventions':
     - 'Arrays/EmptySlots'
     - 'Arrays/MistakenConcatenation'
     - 'Classes/MultipleClassesInFile'
     - 'Classes/MultiplePropertyDeclarationOnOneLine'
     - 'Classes/OrderOfDeclaration'
     - 'Classes/WrongCase'
     - 'Constants/ConstRecommended'
     - 'Functions/OneLetterFunctions'
     - 'Functions/WrongCase'
     - 'Functions/WrongTypehintedName'
     - 'Namespaces/UseWithFullyQualifiedNS'
     - 'Namespaces/WrongCase'
     - 'Php/CloseTags'
     - 'Php/ReturnWithParenthesis'
     - 'Php/UpperCaseFunction'
     - 'Php/UpperCaseKeyword'
     - 'Structures/Bracketless'
     - 'Structures/ConstantComparisonConsistance'
     - 'Structures/DontBeTooManual'
     - 'Structures/EchoPrintConsistance'
     - 'Structures/HeredocDelimiterFavorite'
     - 'Structures/MixedConcatInterpolation'
     - 'Structures/PlusEgalOne'
     - 'Structures/UselessTrailingComma'
     - 'Structures/YodaComparison'
     - 'Type/ShouldBeSingleQuote'
     - 'Type/SimilarIntegers'
     - 'Type/StringInterpolation'
     - 'Variables/VariableUppercase'




.. _annex-compatibilityphp53:

CompatibilityPHP53
##################


.. _annex-ini-compatibilityphp53:

CompatibilityPHP53 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP53]
   analyzer[] = "Arrays/ArrayNSUsage";
   analyzer[] = "Arrays/MixedKeys";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Extensions/Extdba";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/UseFunctionsConstants";
   analyzer[] = "Php/CantUseReturnValueInWriteContext";
   analyzer[] = "Php/CaseForPSS";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClassConstWithArray";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/ClosureThisSupport";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/ConstWithArray";
   analyzer[] = "Php/DefineWithArray";
   analyzer[] = "Php/DirectCallToClone";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/ExponentUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/MethodCallOnNew";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoReturnForGenerator";
   analyzer[] = "Php/NoStringWithAppend";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Php54NewFunctions";
   analyzer[] = "Php/Php55NewFunctions";
   analyzer[] = "Php/Php56NewFunctions";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/StaticclassUsage";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/debugInfoUsage";
   analyzer[] = "Structures/Break0";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/ForeachWithList";
   analyzer[] = "Structures/FunctionSubscripting";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp53:

CompatibilityPHP53 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP53':
     - 'Arrays/ArrayNSUsage'
     - 'Arrays/MixedKeys'
     - 'Classes/Anonymous'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NullOnNew'
     - 'Classes/TypedClassConstants'
     - 'Exceptions/MultipleCatch'
     - 'Extensions/Extdba'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/UseFunctionsConstants'
     - 'Php/CantUseReturnValueInWriteContext'
     - 'Php/CaseForPSS'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClassConstWithArray'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/ClosureThisSupport'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/ConstWithArray'
     - 'Php/DefineWithArray'
     - 'Php/DirectCallToClone'
     - 'Php/EllipsisUsage'
     - 'Php/EnumUsage'
     - 'Php/ExponentUsage'
     - 'Php/FilesFullPath'
     - 'Php/FlexibleHeredoc'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos71'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/MethodCallOnNew'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoListWithString'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoReturnForGenerator'
     - 'Php/NoStringWithAppend'
     - 'Php/NoSubstrMinusOne'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Php54NewFunctions'
     - 'Php/Php55NewFunctions'
     - 'Php/Php56NewFunctions'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php71NewClasses'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/StaticclassUsage'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullableType'
     - 'Php/debugInfoUsage'
     - 'Structures/Break0'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/DereferencingAS'
     - 'Structures/ForeachWithList'
     - 'Structures/FunctionSubscripting'
     - 'Structures/IssetWithConstant'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NoGetClassNull'
     - 'Structures/PHP7Dirname'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/VariableGlobal'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/Binary'
     - 'Type/MalformedOctal'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp54:

CompatibilityPHP54
##################


.. _annex-ini-compatibilityphp54:

CompatibilityPHP54 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP54]
   analyzer[] = "Arrays/MixedKeys";
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/UseFunctionsConstants";
   analyzer[] = "Php/CantUseReturnValueInWriteContext";
   analyzer[] = "Php/CaseForPSS";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClassConstWithArray";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/ConstWithArray";
   analyzer[] = "Php/DefineWithArray";
   analyzer[] = "Php/DirectCallToClone";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/ExponentUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoReturnForGenerator";
   analyzer[] = "Php/NoStringWithAppend";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Php54RemovedFunctions";
   analyzer[] = "Php/Php55NewFunctions";
   analyzer[] = "Php/Php56NewFunctions";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/StaticclassUsage";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/debugInfoUsage";
   analyzer[] = "Structures/BreakNonInteger";
   analyzer[] = "Structures/CalltimePassByReference";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/CryptWithoutSalt";
   analyzer[] = "Structures/DereferencingAS";
   analyzer[] = "Structures/ForeachWithList";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp54:

CompatibilityPHP54 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP54':
     - 'Arrays/MixedKeys'
     - 'Classes/Anonymous'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NullOnNew'
     - 'Classes/TypedClassConstants'
     - 'Exceptions/MultipleCatch'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/UseFunctionsConstants'
     - 'Php/CantUseReturnValueInWriteContext'
     - 'Php/CaseForPSS'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClassConstWithArray'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/ConstWithArray'
     - 'Php/DefineWithArray'
     - 'Php/DirectCallToClone'
     - 'Php/EllipsisUsage'
     - 'Php/EnumUsage'
     - 'Php/ExponentUsage'
     - 'Php/FilesFullPath'
     - 'Php/FlexibleHeredoc'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashAlgos71'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoListWithString'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoReturnForGenerator'
     - 'Php/NoStringWithAppend'
     - 'Php/NoSubstrMinusOne'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Php54RemovedFunctions'
     - 'Php/Php55NewFunctions'
     - 'Php/Php56NewFunctions'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php71NewClasses'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/StaticclassUsage'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullableType'
     - 'Php/debugInfoUsage'
     - 'Structures/BreakNonInteger'
     - 'Structures/CalltimePassByReference'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/CryptWithoutSalt'
     - 'Structures/DereferencingAS'
     - 'Structures/ForeachWithList'
     - 'Structures/IssetWithConstant'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NoGetClassNull'
     - 'Structures/PHP7Dirname'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/VariableGlobal'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/MalformedOctal'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp55:

CompatibilityPHP55
##################


.. _annex-ini-compatibilityphp55:

CompatibilityPHP55 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP55]
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Extensions/Extapc";
   analyzer[] = "Extensions/Extmysql";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/UseFunctionsConstants";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClassConstWithArray";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/ConstWithArray";
   analyzer[] = "Php/DefineWithArray";
   analyzer[] = "Php/DirectCallToClone";
   analyzer[] = "Php/EllipsisUsage";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/ExponentUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoReturnForGenerator";
   analyzer[] = "Php/NoStringWithAppend";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Password55";
   analyzer[] = "Php/Php55RemovedFunctions";
   analyzer[] = "Php/Php56NewFunctions";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/debugInfoUsage";
   analyzer[] = "Structures/ConstantScalarExpression";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp55:

CompatibilityPHP55 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP55':
     - 'Classes/Anonymous'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NullOnNew'
     - 'Classes/TypedClassConstants'
     - 'Exceptions/MultipleCatch'
     - 'Extensions/Extapc'
     - 'Extensions/Extmysql'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/UseFunctionsConstants'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClassConstWithArray'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/ConstWithArray'
     - 'Php/DefineWithArray'
     - 'Php/DirectCallToClone'
     - 'Php/EllipsisUsage'
     - 'Php/EnumUsage'
     - 'Php/ExponentUsage'
     - 'Php/FilesFullPath'
     - 'Php/FlexibleHeredoc'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashAlgos71'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoListWithString'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoReturnForGenerator'
     - 'Php/NoStringWithAppend'
     - 'Php/NoSubstrMinusOne'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Password55'
     - 'Php/Php55RemovedFunctions'
     - 'Php/Php56NewFunctions'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php71NewClasses'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullableType'
     - 'Php/debugInfoUsage'
     - 'Structures/ConstantScalarExpression'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/IssetWithConstant'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NoGetClassNull'
     - 'Structures/PHP7Dirname'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/VariableGlobal'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/MalformedOctal'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp56:

CompatibilityPHP56
##################


.. _annex-ini-compatibilityphp56:

CompatibilityPHP56 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP56]
   analyzer[] = "Classes/Anonymous";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
   analyzer[] = "Classes/NullOnNew";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Functions/GeneratorCannotReturn";
   analyzer[] = "Functions/MultipleSameArguments";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/DefineWithArray";
   analyzer[] = "Php/DirectCallToClone";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/GroupUseDeclaration";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoListWithString";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoReturnForGenerator";
   analyzer[] = "Php/NoStringWithAppend";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/PHP70scalartypehints";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/ParenthesisAsParameter";
   analyzer[] = "Php/Php70NewClasses";
   analyzer[] = "Php/Php70NewFunctions";
   analyzer[] = "Php/Php70NewInterfaces";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php7RelaxedKeyword";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/RawPostDataUsage";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnicodeEscapePartial";
   analyzer[] = "Php/UnicodeEscapeSyntax";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/IssetWithConstant";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/SwitchWithMultipleDefault";
   analyzer[] = "Structures/VariableGlobal";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/MalformedOctal";
   analyzer[] = "Variables/Php5IndirectExpression";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp56:

CompatibilityPHP56 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP56':
     - 'Classes/Anonymous'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/NonStaticMethodsCalledStatic'
     - 'Classes/NullOnNew'
     - 'Classes/TypedClassConstants'
     - 'Exceptions/MultipleCatch'
     - 'Functions/GeneratorCannotReturn'
     - 'Functions/MultipleSameArguments'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/DefineWithArray'
     - 'Php/DirectCallToClone'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FlexibleHeredoc'
     - 'Php/GroupUseDeclaration'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashAlgos71'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoListWithString'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoReturnForGenerator'
     - 'Php/NoStringWithAppend'
     - 'Php/NoSubstrMinusOne'
     - 'Php/PHP70scalartypehints'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/ParenthesisAsParameter'
     - 'Php/Php70NewClasses'
     - 'Php/Php70NewFunctions'
     - 'Php/Php70NewInterfaces'
     - 'Php/Php71NewClasses'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php7RelaxedKeyword'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/RawPostDataUsage'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnicodeEscapePartial'
     - 'Php/UnicodeEscapeSyntax'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullableType'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/IssetWithConstant'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NoGetClassNull'
     - 'Structures/PHP7Dirname'
     - 'Structures/SwitchWithMultipleDefault'
     - 'Structures/VariableGlobal'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/MalformedOctal'
     - 'Variables/Php5IndirectExpression'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp70:

CompatibilityPHP70
##################


.. _annex-ini-compatibilityphp70:

CompatibilityPHP70 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP70]
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/ConstVisibilityUsage";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Classes/toStringPss";
   analyzer[] = "Exceptions/MultipleCatch";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Functions/funcGetArgModified";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/EmptyList";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/ForeachDontChangePointer";
   analyzer[] = "Php/GlobalWithoutSimpleVariable";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashAlgos71";
   analyzer[] = "Php/ListShortSyntax";
   analyzer[] = "Php/ListWithAppends";
   analyzer[] = "Php/ListWithKeys";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/NoSubstrMinusOne";
   analyzer[] = "Php/PHP71scalartypehints";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php70RemovedDirective";
   analyzer[] = "Php/Php70RemovedFunctions";
   analyzer[] = "Php/Php71NewClasses";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/ReservedKeywords7";
   analyzer[] = "Php/SetExceptionHandlerPHP7";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseNullableType";
   analyzer[] = "Php/UsortSorting";
   analyzer[] = "Structures/BreakOutsideLoop";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/McryptcreateivWithoutOption";
   analyzer[] = "Structures/NegativeOffsetOnString";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/SetlocaleNeedsConstants";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/HexadecimalString";
   analyzer[] = "Variables/Php7IndirectExpression";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp70:

CompatibilityPHP70 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP70':
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/ConstVisibilityUsage'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Classes/toStringPss'
     - 'Exceptions/MultipleCatch'
     - 'Functions/VoidIsNotAReference'
     - 'Functions/funcGetArgModified'
     - 'Interfaces/CantOverloadConstants'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/EmptyList'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FinalConstant'
     - 'Php/FlexibleHeredoc'
     - 'Php/ForeachDontChangePointer'
     - 'Php/GlobalWithoutSimpleVariable'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashAlgos71'
     - 'Php/ListShortSyntax'
     - 'Php/ListWithAppends'
     - 'Php/ListWithKeys'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/NoSubstrMinusOne'
     - 'Php/PHP71scalartypehints'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php70RemovedDirective'
     - 'Php/Php70RemovedFunctions'
     - 'Php/Php71NewClasses'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/ReservedKeywords7'
     - 'Php/SetExceptionHandlerPHP7'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseNullableType'
     - 'Php/UsortSorting'
     - 'Structures/BreakOutsideLoop'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/McryptcreateivWithoutOption'
     - 'Structures/NegativeOffsetOnString'
     - 'Structures/NoGetClassNull'
     - 'Structures/SetlocaleNeedsConstants'
     - 'Structures/pregOptionE'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/HexadecimalString'
     - 'Variables/Php7IndirectExpression'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp71:

CompatibilityPHP71
##################


.. _annex-ini-compatibilityphp71:

CompatibilityPHP71 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP71]
   analyzer[] = "Arrays/StringInitialization";
   analyzer[] = "Classes/CantInheritAbstractMethod";
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/IntegerAsProperty";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Classes/UsingThisOutsideAClass";
   analyzer[] = "Extensions/Extmcrypt";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/GroupUseTrailingComma";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/PHP72scalartypehints";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php70RemovedDirective";
   analyzer[] = "Php/Php70RemovedFunctions";
   analyzer[] = "Php/Php71NewFunctions";
   analyzer[] = "Php/Php71RemovedDirective";
   analyzer[] = "Php/Php71microseconds";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Structures/ArrayMergeWithEllipsis";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Type/HexadecimalString";
   analyzer[] = "Type/OctalInString";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp71:

CompatibilityPHP71 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP71':
     - 'Arrays/StringInitialization'
     - 'Classes/CantInheritAbstractMethod'
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/IntegerAsProperty'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Classes/UsingThisOutsideAClass'
     - 'Extensions/Extmcrypt'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Php/BetterRand'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FinalConstant'
     - 'Php/FlexibleHeredoc'
     - 'Php/GroupUseTrailingComma'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/PHP72scalartypehints'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php70RemovedDirective'
     - 'Php/Php70RemovedFunctions'
     - 'Php/Php71NewFunctions'
     - 'Php/Php71RemovedDirective'
     - 'Php/Php71microseconds'
     - 'Php/Php72NewClasses'
     - 'Php/Php73NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/SignatureTrailingComma'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Structures/ArrayMergeWithEllipsis'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/NoGetClassNull'
     - 'Structures/NoSubstrOne'
     - 'Structures/pregOptionE'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Type/HexadecimalString'
     - 'Type/OctalInString'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp72:

CompatibilityPHP72
##################


.. _annex-ini-compatibilityphp72:

CompatibilityPHP72 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP72]
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Constants/UndefinedConstants";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Php/AvoidSetErrorHandlerContextArg";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/FlexibleHeredoc";
   analyzer[] = "Php/HashAlgos53";
   analyzer[] = "Php/HashAlgos54";
   analyzer[] = "Php/HashUsesObjects";
   analyzer[] = "Php/ListWithReference";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoReferenceForStaticProperty";
   analyzer[] = "Php/PHP73LastEmptyArgument";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php72Deprecation";
   analyzer[] = "Php/Php72NewClasses";
   analyzer[] = "Php/Php72NewConstants";
   analyzer[] = "Php/Php72NewFunctions";
   analyzer[] = "Php/Php72ObjectKeyword";
   analyzer[] = "Php/Php72RemovedFunctions";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/TrailingComma";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Structures/ArrayMergeWithEllipsis";
   analyzer[] = "Structures/CanCountNonCountable";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/NoGetClassNull";
   analyzer[] = "Structures/pregOptionE";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp72:

CompatibilityPHP72 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP72':
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Constants/UndefinedConstants'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Php/AvoidSetErrorHandlerContextArg'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/ConcatAndAddition'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FinalConstant'
     - 'Php/FlexibleHeredoc'
     - 'Php/HashAlgos53'
     - 'Php/HashAlgos54'
     - 'Php/HashUsesObjects'
     - 'Php/ListWithReference'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoReferenceForStaticProperty'
     - 'Php/PHP73LastEmptyArgument'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php72Deprecation'
     - 'Php/Php72NewClasses'
     - 'Php/Php72NewConstants'
     - 'Php/Php72NewFunctions'
     - 'Php/Php72ObjectKeyword'
     - 'Php/Php72RemovedFunctions'
     - 'Php/Php73NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/SignatureTrailingComma'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/ThrowWasAnExpression'
     - 'Php/TrailingComma'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Structures/ArrayMergeWithEllipsis'
     - 'Structures/CanCountNonCountable'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/NoGetClassNull'
     - 'Structures/pregOptionE'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp73:

CompatibilityPHP73
##################


.. _annex-ini-compatibilityphp73:

CompatibilityPHP73 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP73]
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Constants/CaseInsensitiveConstants";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Php/AssertFunctionIsReserved";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/CoalesceEqual";
   analyzer[] = "Php/CompactInexistant";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/IntegerSeparatorUsage";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php73NewFunctions";
   analyzer[] = "Php/Php73RemovedFunctions";
   analyzer[] = "Php/Php74NewDirective";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/TypedPropertyUsage";
   analyzer[] = "Php/UnknownPcre2Option";
   analyzer[] = "Php/UnpackingInsideArrays";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Structures/ArrayMergeWithEllipsis";
   analyzer[] = "Structures/ContinueIsForLoop";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp73:

CompatibilityPHP73 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP73':
     - 'Attributes/NestedAttributes'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Constants/CaseInsensitiveConstants'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Php/AssertFunctionIsReserved'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/CoalesceEqual'
     - 'Php/CompactInexistant'
     - 'Php/ConcatAndAddition'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FinalConstant'
     - 'Php/IntegerSeparatorUsage'
     - 'Php/NamedParameterUsage'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewInitializers'
     - 'Php/NewWithoutParenthesis'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php73NewFunctions'
     - 'Php/Php73RemovedFunctions'
     - 'Php/Php74NewDirective'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/SignatureTrailingComma'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/ThrowWasAnExpression'
     - 'Php/TypedPropertyUsage'
     - 'Php/UnknownPcre2Option'
     - 'Php/UnpackingInsideArrays'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Structures/ArrayMergeWithEllipsis'
     - 'Structures/ContinueIsForLoop'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp74:

CompatibilityPHP74
##################


.. _annex-ini-compatibilityphp74:

CompatibilityPHP74 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP74]
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Functions/UnbindingClosures";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Namespaces/NoKeywordInNamespace";
   analyzer[] = "Php/ArrayKeyExistsWithObjects";
   analyzer[] = "Php/AvoidGetobjectVars";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/DetectCurrentClass";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FilesFullPath";
   analyzer[] = "Php/FilterToAddSlashes";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/HashAlgos74";
   analyzer[] = "Php/IdnUts46";
   analyzer[] = "Php/NamedParameterUsage";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoMoreCurlyArrays";
   analyzer[] = "Php/PHP80scalartypehints";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php74Deprecation";
   analyzer[] = "Php/Php74NewClasses";
   analyzer[] = "Php/Php74NewConstants";
   analyzer[] = "Php/Php74NewFunctions";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php74RemovedFunctions";
   analyzer[] = "Php/Php74ReservedKeyword";
   analyzer[] = "Php/Php74mbstrrpos3rdArg";
   analyzer[] = "Php/Php80NewFunctions";
   analyzer[] = "Php/Php80OnlyTypeHints";
   analyzer[] = "Php/Php80UnionTypehint";
   analyzer[] = "Php/Php80VariableSyntax";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/ReflectionExportIsDeprecated";
   analyzer[] = "Php/ScalarAreNotArrays";
   analyzer[] = "Php/SignatureTrailingComma";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/UseMatch";
   analyzer[] = "Structures/CurlVersionNow";
   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Traits/NoPrivateAbstract";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp74:

CompatibilityPHP74 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP74':
     - 'Attributes/NestedAttributes'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Functions/UnbindingClosures'
     - 'Functions/VoidIsNotAReference'
     - 'Interfaces/CantOverloadConstants'
     - 'Namespaces/NoKeywordInNamespace'
     - 'Php/ArrayKeyExistsWithObjects'
     - 'Php/AvoidGetobjectVars'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/ConcatAndAddition'
     - 'Php/DetectCurrentClass'
     - 'Php/EnumUsage'
     - 'Php/FilesFullPath'
     - 'Php/FilterToAddSlashes'
     - 'Php/FinalConstant'
     - 'Php/HashAlgos74'
     - 'Php/IdnUts46'
     - 'Php/NamedParameterUsage'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewInitializers'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoMoreCurlyArrays'
     - 'Php/PHP80scalartypehints'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php74Deprecation'
     - 'Php/Php74NewClasses'
     - 'Php/Php74NewConstants'
     - 'Php/Php74NewFunctions'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php74RemovedFunctions'
     - 'Php/Php74ReservedKeyword'
     - 'Php/Php74mbstrrpos3rdArg'
     - 'Php/Php80NewFunctions'
     - 'Php/Php80OnlyTypeHints'
     - 'Php/Php80UnionTypehint'
     - 'Php/Php80VariableSyntax'
     - 'Php/Php81NewTypes'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/ReflectionExportIsDeprecated'
     - 'Php/ScalarAreNotArrays'
     - 'Php/SignatureTrailingComma'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/ThrowWasAnExpression'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/UseMatch'
     - 'Structures/CurlVersionNow'
     - 'Structures/DontReadAndWriteInOneExpression'
     - 'Structures/OpensslRandomPseudoByteSecondArg'
     - 'Traits/ConstantsInTraits'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Traits/NoPrivateAbstract'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp80:

CompatibilityPHP80
##################


.. _annex-ini-compatibilityphp80:

CompatibilityPHP80 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP80]
   analyzer[] = "Arrays/NegativeStart";
   analyzer[] = "Attributes/NestedAttributes";
   analyzer[] = "Classes/FinalPrivate";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/OldStyleConstructor";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Exceptions/AnonymousCatch";
   analyzer[] = "Functions/MismatchParameterName";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Functions/WrongOptionalParameter";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Php/AvoidGetobjectVars";
   analyzer[] = "Php/CastUnsetUsage";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/EnumUsage";
   analyzer[] = "Php/FinalConstant";
   analyzer[] = "Php/MixedKeyword";
   analyzer[] = "Php/NamedArgumentAndVariadic";
   analyzer[] = "Php/NeverTypehintUsage";
   analyzer[] = "Php/NewInitializers";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/PHP81scalartypehints";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php80NamedParameterVariadic";
   analyzer[] = "Php/Php80RemovedConstant";
   analyzer[] = "Php/Php80RemovedDirective";
   analyzer[] = "Php/Php80RemovedFunctions";
   analyzer[] = "Php/Php80RemovesResources";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php81RemovesResources";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/PhpErrorMsgUsage";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/ReservedMatchKeyword";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/StringIntComparison";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Structures/ArrayMapPassesByValue";
   analyzer[] = "Structures/MultipleTypeCasesInSwitch";
   analyzer[] = "Structures/NoMaxOnEmptyArray";
   analyzer[] = "Structures/UnsupportedTypesWithOperators";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Variables/RedeclaredStaticVariable";


.. _annex-yaml-compatibilityphp80:

CompatibilityPHP80 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP80':
     - 'Arrays/NegativeStart'
     - 'Attributes/NestedAttributes'
     - 'Classes/FinalPrivate'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/OldStyleConstructor'
     - 'Classes/TypedClassConstants'
     - 'Exceptions/AnonymousCatch'
     - 'Functions/MismatchParameterName'
     - 'Functions/VoidIsNotAReference'
     - 'Functions/WrongOptionalParameter'
     - 'Interfaces/CantOverloadConstants'
     - 'Php/AvoidGetobjectVars'
     - 'Php/CastUnsetUsage'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/CloneConstant'
     - 'Php/ClosureInConstant'
     - 'Php/ConcatAndAddition'
     - 'Php/EnumUsage'
     - 'Php/FinalConstant'
     - 'Php/MixedKeyword'
     - 'Php/NamedArgumentAndVariadic'
     - 'Php/NeverTypehintUsage'
     - 'Php/NewInitializers'
     - 'Php/NewWithoutParenthesis'
     - 'Php/PHP81scalartypehints'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php80NamedParameterVariadic'
     - 'Php/Php80RemovedConstant'
     - 'Php/Php80RemovedDirective'
     - 'Php/Php80RemovedFunctions'
     - 'Php/Php80RemovesResources'
     - 'Php/Php81NewTypes'
     - 'Php/Php81RemovesResources'
     - 'Php/Php82NewTypes'
     - 'Php/PhpErrorMsgUsage'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/ReservedMatchKeyword'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/StringIntComparison'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Structures/ArrayMapPassesByValue'
     - 'Structures/MultipleTypeCasesInSwitch'
     - 'Structures/NoMaxOnEmptyArray'
     - 'Structures/UnsupportedTypesWithOperators'
     - 'Traits/ConstantsInTraits'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Variables/RedeclaredStaticVariable'




.. _annex-compatibilityphp81:

CompatibilityPHP81
##################


.. _annex-ini-compatibilityphp81:

CompatibilityPHP81 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP81]
   analyzer[] = "Arrays/FloatConversionAsIndex";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Functions/NoReferencedVoid";
   analyzer[] = "Functions/VoidIsNotAReference";
   analyzer[] = "Php/CallingStaticTraitMethod";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/MixedKeyword";
   analyzer[] = "Php/NamedArgumentAndVariadic";
   analyzer[] = "Php/NativeClassTypeCompatibility";
   analyzer[] = "Php/NeverKeyword";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/NoNullForNative";
   analyzer[] = "Php/OpensslEncryptAlgoChange";
   analyzer[] = "Php/Php74RemovedDirective";
   analyzer[] = "Php/Php80RemovedDirective";
   analyzer[] = "Php/Php81NewFunctions";
   analyzer[] = "Php/Php81NewTypes";
   analyzer[] = "Php/Php81RemovedConstant";
   analyzer[] = "Php/Php81RemovedDirective";
   analyzer[] = "Php/Php81RemovedFunctions";
   analyzer[] = "Php/Php82NewTypes";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/RestrictGlobalUsage";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/UseEnumCaseInConstantExpression";
   analyzer[] = "Php/VersionCompareOperator";
   analyzer[] = "Traits/CannotCallTraitMethod";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Variables/InheritedStaticVariable";
   analyzer[] = "Variables/RedeclaredStaticVariable";
   analyzer[] = "Variables/StaticVariableInitialisation";


.. _annex-yaml-compatibilityphp81:

CompatibilityPHP81 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP81':
     - 'Arrays/FloatConversionAsIndex'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Functions/NoReferencedVoid'
     - 'Functions/VoidIsNotAReference'
     - 'Php/CallingStaticTraitMethod'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClosureInConstant'
     - 'Php/FalseToArray'
     - 'Php/JsonSerializeReturnType'
     - 'Php/MixedKeyword'
     - 'Php/NamedArgumentAndVariadic'
     - 'Php/NativeClassTypeCompatibility'
     - 'Php/NeverKeyword'
     - 'Php/NewWithoutParenthesis'
     - 'Php/NoNullForNative'
     - 'Php/OpensslEncryptAlgoChange'
     - 'Php/Php74RemovedDirective'
     - 'Php/Php80RemovedDirective'
     - 'Php/Php81NewFunctions'
     - 'Php/Php81NewTypes'
     - 'Php/Php81RemovedConstant'
     - 'Php/Php81RemovedDirective'
     - 'Php/Php81RemovedFunctions'
     - 'Php/Php82NewTypes'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/RestrictGlobalUsage'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/UseEnumCaseInConstantExpression'
     - 'Php/VersionCompareOperator'
     - 'Traits/CannotCallTraitMethod'
     - 'Traits/ConstantsInTraits'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Variables/InheritedStaticVariable'
     - 'Variables/RedeclaredStaticVariable'
     - 'Variables/StaticVariableInitialisation'




.. _annex-compatibilityphp82:

CompatibilityPHP82
##################


.. _annex-ini-compatibilityphp82:

CompatibilityPHP82 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP82]
   analyzer[] = "Arrays/FloatConversionAsIndex";
   analyzer[] = "Classes/ChecksPropertyExistence";
   analyzer[] = "Classes/ExtendsStdclass";
   analyzer[] = "Classes/NewDynamicConstantSyntax";
   analyzer[] = "Classes/TypedClassConstants";
   analyzer[] = "Classes/UndefinedProperty";
   analyzer[] = "Functions/DeprecatedCallable";
   analyzer[] = "Interfaces/InheritedClassConstantVisibility";
   analyzer[] = "Php/ClassAliasSupportsInternalClasses";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/DeprecateDollarCurly";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/Php82NewFunctions";
   analyzer[] = "Php/ReadonlyPropertyChangedByCloning";
   analyzer[] = "Php/StaticVariableDefaultCanBeAnyExpression";
   analyzer[] = "Php/Utf8EncodeDeprecated";
   analyzer[] = "Php/VersionCompareOperator";
   analyzer[] = "Structures/DeprecatedMbEncoding";
   analyzer[] = "Traits/CannotCallTraitMethod";
   analyzer[] = "Traits/ConstantsInTraits";
   analyzer[] = "Traits/FinalTraitsAreFinal";
   analyzer[] = "Traits/NoFinalAlias";
   analyzer[] = "Variables/RedeclaredStaticVariable";
   analyzer[] = "Variables/StaticVariableInitialisation";


.. _annex-yaml-compatibilityphp82:

CompatibilityPHP82 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP82':
     - 'Arrays/FloatConversionAsIndex'
     - 'Classes/ChecksPropertyExistence'
     - 'Classes/ExtendsStdclass'
     - 'Classes/NewDynamicConstantSyntax'
     - 'Classes/TypedClassConstants'
     - 'Classes/UndefinedProperty'
     - 'Functions/DeprecatedCallable'
     - 'Interfaces/InheritedClassConstantVisibility'
     - 'Php/ClassAliasSupportsInternalClasses'
     - 'Php/ClosureInConstant'
     - 'Php/DeprecateDollarCurly'
     - 'Php/FalseToArray'
     - 'Php/NewWithoutParenthesis'
     - 'Php/Php82NewFunctions'
     - 'Php/ReadonlyPropertyChangedByCloning'
     - 'Php/StaticVariableDefaultCanBeAnyExpression'
     - 'Php/Utf8EncodeDeprecated'
     - 'Php/VersionCompareOperator'
     - 'Structures/DeprecatedMbEncoding'
     - 'Traits/CannotCallTraitMethod'
     - 'Traits/ConstantsInTraits'
     - 'Traits/FinalTraitsAreFinal'
     - 'Traits/NoFinalAlias'
     - 'Variables/RedeclaredStaticVariable'
     - 'Variables/StaticVariableInitialisation'




.. _annex-compatibilityphp83:

CompatibilityPHP83
##################


.. _annex-ini-compatibilityphp83:

CompatibilityPHP83 for INI
++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [CompatibilityPHP83]
   analyzer[] = "Interfaces/InheritedClassConstantVisibility";
   analyzer[] = "Php/ClosureInConstant";
   analyzer[] = "Php/NewWithoutParenthesis";
   analyzer[] = "Php/Php83NewClasses";
   analyzer[] = "Php/Php83NewFunctions";
   analyzer[] = "Structures/GetClassWithoutArg";
   analyzer[] = "Traits/ConstantsInTraits";


.. _annex-yaml-compatibilityphp83:

CompatibilityPHP83 for .exakat.yaml
+++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'CompatibilityPHP83':
     - 'Interfaces/InheritedClassConstantVisibility'
     - 'Php/ClosureInConstant'
     - 'Php/NewWithoutParenthesis'
     - 'Php/Php83NewClasses'
     - 'Php/Php83NewFunctions'
     - 'Structures/GetClassWithoutArg'
     - 'Traits/ConstantsInTraits'




.. _annex-dead-code:

Dead code
#########


.. _annex-ini-dead-code:

Dead code for INI
+++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Dead code]
   analyzer[] = "Classes/CantExtendFinal";
   analyzer[] = "Classes/LocallyUnusedProperty";
   analyzer[] = "Classes/UnreachableMethod";
   analyzer[] = "Classes/UnresolvedCatch";
   analyzer[] = "Classes/UnresolvedInstanceof";
   analyzer[] = "Classes/UnusedClass";
   analyzer[] = "Classes/UnusedMethods";
   analyzer[] = "Classes/UnusedPrivateMethod";
   analyzer[] = "Classes/UnusedPrivateProperty";
   analyzer[] = "Classes/UnusedProtectedMethods";
   analyzer[] = "Constants/UnusedConstants";
   analyzer[] = "Enums/UnusedEnumCase";
   analyzer[] = "Exceptions/AlreadyCaught";
   analyzer[] = "Exceptions/CaughtButNotThrown";
   analyzer[] = "Exceptions/CouldDropVariable";
   analyzer[] = "Exceptions/Rethrown";
   analyzer[] = "Exceptions/Unthrown";
   analyzer[] = "Functions/UnusedFunctions";
   analyzer[] = "Functions/UnusedInheritedVariable";
   analyzer[] = "Functions/UnusedReturnedValue";
   analyzer[] = "Functions/UselessTypeCheck";
   analyzer[] = "Interfaces/UnusedInterfaces";
   analyzer[] = "Namespaces/EmptyNamespace";
   analyzer[] = "Namespaces/UnusedUse";
   analyzer[] = "Structures/EmptyLines";
   analyzer[] = "Structures/IdenticalElseif";
   analyzer[] = "Structures/UnreachableCode";
   analyzer[] = "Structures/UnsetInForeach";
   analyzer[] = "Structures/UnusedLabel";
   analyzer[] = "Structures/UseVariableInsideLoop";
   analyzer[] = "Traits/EmptyTrait";
   analyzer[] = "Traits/SelfUsingTrait";
   analyzer[] = "Variables/StaticVariableInNamespace";


.. _annex-yaml-dead-code:

Dead code for .exakat.yaml
++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Dead code':
     - 'Classes/CantExtendFinal'
     - 'Classes/LocallyUnusedProperty'
     - 'Classes/UnreachableMethod'
     - 'Classes/UnresolvedCatch'
     - 'Classes/UnresolvedInstanceof'
     - 'Classes/UnusedClass'
     - 'Classes/UnusedMethods'
     - 'Classes/UnusedPrivateMethod'
     - 'Classes/UnusedPrivateProperty'
     - 'Classes/UnusedProtectedMethods'
     - 'Constants/UnusedConstants'
     - 'Enums/UnusedEnumCase'
     - 'Exceptions/AlreadyCaught'
     - 'Exceptions/CaughtButNotThrown'
     - 'Exceptions/CouldDropVariable'
     - 'Exceptions/Rethrown'
     - 'Exceptions/Unthrown'
     - 'Functions/UnusedFunctions'
     - 'Functions/UnusedInheritedVariable'
     - 'Functions/UnusedReturnedValue'
     - 'Functions/UselessTypeCheck'
     - 'Interfaces/UnusedInterfaces'
     - 'Namespaces/EmptyNamespace'
     - 'Namespaces/UnusedUse'
     - 'Structures/EmptyLines'
     - 'Structures/IdenticalElseif'
     - 'Structures/UnreachableCode'
     - 'Structures/UnsetInForeach'
     - 'Structures/UnusedLabel'
     - 'Structures/UseVariableInsideLoop'
     - 'Traits/EmptyTrait'
     - 'Traits/SelfUsingTrait'
     - 'Variables/StaticVariableInNamespace'




.. _annex-deprecated:

Deprecated
##########


.. _annex-ini-deprecated:

Deprecated for INI
++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Deprecated]
   analyzer[] = "Constants/CaseInsensitiveConstants";
   analyzer[] = "Functions/IsExtFunction";
   analyzer[] = "Functions/NoReferencedVoid";
   analyzer[] = "Php/AssertFunctionIsReserved";
   analyzer[] = "Php/CallingStaticTraitMethod";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
   analyzer[] = "Php/NoNullForNative";


.. _annex-yaml-deprecated:

Deprecated for .exakat.yaml
+++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Deprecated':
     - 'Constants/CaseInsensitiveConstants'
     - 'Functions/IsExtFunction'
     - 'Functions/NoReferencedVoid'
     - 'Php/AssertFunctionIsReserved'
     - 'Php/CallingStaticTraitMethod'
     - 'Php/JsonSerializeReturnType'
     - 'Php/NestedTernaryWithoutParenthesis'
     - 'Php/NoNullForNative'




.. _annex-dump:

Dump
####


.. _annex-ini-dump:

Dump for INI
++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Dump]
   analyzer[] = "Dump/ArgumentCountsPerCalls";
   analyzer[] = "Dump/CallOrder";
   analyzer[] = "Dump/ClassInjectionCount";
   analyzer[] = "Dump/CollectAtomCounts";
   analyzer[] = "Dump/CollectBlockSize";
   analyzer[] = "Dump/CollectCalls";
   analyzer[] = "Dump/CollectCatch";
   analyzer[] = "Dump/CollectClassChanges";
   analyzer[] = "Dump/CollectClassChildren";
   analyzer[] = "Dump/CollectClassConstantCounts";
   analyzer[] = "Dump/CollectClassDepth";
   analyzer[] = "Dump/CollectClassInterfaceCounts";
   analyzer[] = "Dump/CollectClassTraitsCounts";
   analyzer[] = "Dump/CollectClassesDependencies";
   analyzer[] = "Dump/CollectDefinitionsStats";
   analyzer[] = "Dump/CollectDependencyExtension";
   analyzer[] = "Dump/CollectFilesDependencies";
   analyzer[] = "Dump/CollectForeachFavorite";
   analyzer[] = "Dump/CollectGlobalVariables";
   analyzer[] = "Dump/CollectGraphTriplets";
   analyzer[] = "Dump/CollectLiterals";
   analyzer[] = "Dump/CollectLocalVariableCounts";
   analyzer[] = "Dump/CollectMbstringEncodings";
   analyzer[] = "Dump/CollectMethodCounts";
   analyzer[] = "Dump/CollectMethodsThrowingExceptions";
   analyzer[] = "Dump/CollectNativeCallsPerExpressions";
   analyzer[] = "Dump/CollectParameterCounts";
   analyzer[] = "Dump/CollectParameterNames";
   analyzer[] = "Dump/CollectPhpStructures";
   analyzer[] = "Dump/CollectPropertyCounts";
   analyzer[] = "Dump/CollectPropertyUsage";
   analyzer[] = "Dump/CollectReadability";
   analyzer[] = "Dump/CollectSetLocale";
   analyzer[] = "Dump/CollectStructures";
   analyzer[] = "Dump/CollectStubStructures";
   analyzer[] = "Dump/CollectThrow";
   analyzer[] = "Dump/CollectUseCounts";
   analyzer[] = "Dump/CollectVariables";
   analyzer[] = "Dump/CollectVendorStructures";
   analyzer[] = "Dump/CollectsNames";
   analyzer[] = "Dump/CombinedCalls";
   analyzer[] = "Dump/ConstantOrder";
   analyzer[] = "Dump/CouldBeAConstant";
   analyzer[] = "Dump/CyclomaticComplexity";
   analyzer[] = "Dump/DereferencingLevels";
   analyzer[] = "Dump/DumpComparedLiterals";
   analyzer[] = "Dump/EnvironnementVariables";
   analyzer[] = "Dump/FossilizedMethods";
   analyzer[] = "Dump/Inclusions";
   analyzer[] = "Dump/IndentationLevels";
   analyzer[] = "Dump/NewOrder";
   analyzer[] = "Dump/TypehintingStats";
   analyzer[] = "Dump/Typehintorder";
   analyzer[] = "Exceptions/CaughtExceptions";
   analyzer[] = "Exceptions/TryNoCatch";
   analyzer[] = "Php/ComparisonOnDifferentTypes";
   analyzer[] = "Php/IncludeVariables";


.. _annex-yaml-dump:

Dump for .exakat.yaml
+++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Dump':
     - 'Dump/ArgumentCountsPerCalls'
     - 'Dump/CallOrder'
     - 'Dump/ClassInjectionCount'
     - 'Dump/CollectAtomCounts'
     - 'Dump/CollectBlockSize'
     - 'Dump/CollectCalls'
     - 'Dump/CollectCatch'
     - 'Dump/CollectClassChanges'
     - 'Dump/CollectClassChildren'
     - 'Dump/CollectClassConstantCounts'
     - 'Dump/CollectClassDepth'
     - 'Dump/CollectClassInterfaceCounts'
     - 'Dump/CollectClassTraitsCounts'
     - 'Dump/CollectClassesDependencies'
     - 'Dump/CollectDefinitionsStats'
     - 'Dump/CollectDependencyExtension'
     - 'Dump/CollectFilesDependencies'
     - 'Dump/CollectForeachFavorite'
     - 'Dump/CollectGlobalVariables'
     - 'Dump/CollectGraphTriplets'
     - 'Dump/CollectLiterals'
     - 'Dump/CollectLocalVariableCounts'
     - 'Dump/CollectMbstringEncodings'
     - 'Dump/CollectMethodCounts'
     - 'Dump/CollectMethodsThrowingExceptions'
     - 'Dump/CollectNativeCallsPerExpressions'
     - 'Dump/CollectParameterCounts'
     - 'Dump/CollectParameterNames'
     - 'Dump/CollectPhpStructures'
     - 'Dump/CollectPropertyCounts'
     - 'Dump/CollectPropertyUsage'
     - 'Dump/CollectReadability'
     - 'Dump/CollectSetLocale'
     - 'Dump/CollectStructures'
     - 'Dump/CollectStubStructures'
     - 'Dump/CollectThrow'
     - 'Dump/CollectUseCounts'
     - 'Dump/CollectVariables'
     - 'Dump/CollectVendorStructures'
     - 'Dump/CollectsNames'
     - 'Dump/CombinedCalls'
     - 'Dump/ConstantOrder'
     - 'Dump/CouldBeAConstant'
     - 'Dump/CyclomaticComplexity'
     - 'Dump/DereferencingLevels'
     - 'Dump/DumpComparedLiterals'
     - 'Dump/EnvironnementVariables'
     - 'Dump/FossilizedMethods'
     - 'Dump/Inclusions'
     - 'Dump/IndentationLevels'
     - 'Dump/NewOrder'
     - 'Dump/TypehintingStats'
     - 'Dump/Typehintorder'
     - 'Exceptions/CaughtExceptions'
     - 'Exceptions/TryNoCatch'
     - 'Php/ComparisonOnDifferentTypes'
     - 'Php/IncludeVariables'




.. _annex-first:

First
#####


.. _annex-ini-first:

First for INI
+++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [First]
   analyzer[] = "Complete/ReturnTypehint";
   analyzer[] = "Complete/VariableTypehint";
   analyzer[] = "Variables/IsLocalConstant";


.. _annex-yaml-first:

First for .exakat.yaml
++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'First':
     - 'Complete/ReturnTypehint'
     - 'Complete/VariableTypehint'
     - 'Variables/IsLocalConstant'




.. _annex-inventory:

Inventory
#########


.. _annex-ini-inventory:

Inventory for INI
+++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Inventory]
   analyzer[] = "Classes/ExtendsStdclass";
   analyzer[] = "Classes/MagicProperties";
   analyzer[] = "Classes/PromotedProperties";
   analyzer[] = "Constants/Constantnames";
   analyzer[] = "Constants/RelayConstant";
   analyzer[] = "Functions/MultipleIdenticalClosure";
   analyzer[] = "Functions/RelayFunction";
   analyzer[] = "Php/CookiesVariables";
   analyzer[] = "Php/DateFormats";
   analyzer[] = "Php/IncomingVariables";
   analyzer[] = "Php/SessionVariables";
   analyzer[] = "Structures/Fallthrough";
   analyzer[] = "Structures/InitThenIf";
   analyzer[] = "Type/ArrayIndex";
   analyzer[] = "Type/Binary";
   analyzer[] = "Type/CharString";
   analyzer[] = "Type/Email";
   analyzer[] = "Type/GPCIndex";
   analyzer[] = "Type/Heredoc";
   analyzer[] = "Type/Hexadecimal";
   analyzer[] = "Type/HexadecimalString";
   analyzer[] = "Type/HttpHeader";
   analyzer[] = "Type/HttpStatus";
   analyzer[] = "Type/IncomingDateFormat";
   analyzer[] = "Type/Ip";
   analyzer[] = "Type/Md5String";
   analyzer[] = "Type/MimeType";
   analyzer[] = "Type/OctalInString";
   analyzer[] = "Type/OpensslCipher";
   analyzer[] = "Type/Pack";
   analyzer[] = "Type/Pcre";
   analyzer[] = "Type/Ports";
   analyzer[] = "Type/Printf";
   analyzer[] = "Type/Regex";
   analyzer[] = "Type/SpecialIntegers";
   analyzer[] = "Type/Sql";
   analyzer[] = "Type/UdpDomains";
   analyzer[] = "Type/UnicodeBlock";
   analyzer[] = "Type/Url";


.. _annex-yaml-inventory:

Inventory for .exakat.yaml
++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Inventory':
     - 'Classes/ExtendsStdclass'
     - 'Classes/MagicProperties'
     - 'Classes/PromotedProperties'
     - 'Constants/Constantnames'
     - 'Constants/RelayConstant'
     - 'Functions/MultipleIdenticalClosure'
     - 'Functions/RelayFunction'
     - 'Php/CookiesVariables'
     - 'Php/DateFormats'
     - 'Php/IncomingVariables'
     - 'Php/SessionVariables'
     - 'Structures/Fallthrough'
     - 'Structures/InitThenIf'
     - 'Type/ArrayIndex'
     - 'Type/Binary'
     - 'Type/CharString'
     - 'Type/Email'
     - 'Type/GPCIndex'
     - 'Type/Heredoc'
     - 'Type/Hexadecimal'
     - 'Type/HexadecimalString'
     - 'Type/HttpHeader'
     - 'Type/HttpStatus'
     - 'Type/IncomingDateFormat'
     - 'Type/Ip'
     - 'Type/Md5String'
     - 'Type/MimeType'
     - 'Type/OctalInString'
     - 'Type/OpensslCipher'
     - 'Type/Pack'
     - 'Type/Pcre'
     - 'Type/Ports'
     - 'Type/Printf'
     - 'Type/Regex'
     - 'Type/SpecialIntegers'
     - 'Type/Sql'
     - 'Type/UdpDomains'
     - 'Type/UnicodeBlock'
     - 'Type/Url'




.. _annex-isext:

IsExt
#####


.. _annex-ini-isext:

IsExt for INI
+++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [IsExt]
   analyzer[] = "Php/OveriddenFunction";


.. _annex-yaml-isext:

IsExt for .exakat.yaml
++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'IsExt':
     - 'Php/OveriddenFunction'




.. _annex-isphp:

IsPHP
#####


.. _annex-ini-isphp:

IsPHP for INI
+++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [IsPHP]
   analyzer[] = "Php/OveriddenFunction";


.. _annex-yaml-isphp:

IsPHP for .exakat.yaml
++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'IsPHP':
     - 'Php/OveriddenFunction'




.. _annex-isstub:

IsStub
######


.. _annex-ini-isstub:

IsStub for INI
++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [IsStub]
   analyzer[] = "Php/OveriddenFunction";


.. _annex-yaml-isstub:

IsStub for .exakat.yaml
+++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'IsStub':
     - 'Php/OveriddenFunction'




.. _annex-lintbutwontexec:

LintButWontExec
###############


.. _annex-ini-lintbutwontexec:

LintButWontExec for INI
+++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [LintButWontExec]
   analyzer[] = "Classes/AbstractOrImplements";
   analyzer[] = "Classes/CantOverwriteFinalConstant";
   analyzer[] = "Classes/CloneWithNonObject";
   analyzer[] = "Classes/CouldBeStringable";
   analyzer[] = "Classes/Finalclass";
   analyzer[] = "Classes/Finalmethod";
   analyzer[] = "Classes/ImplementedMethodsArePublic";
   analyzer[] = "Classes/IncompatibleSignature";
   analyzer[] = "Classes/InheritedPropertyMustMatch";
   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
   analyzer[] = "Classes/MismatchProperties";
   analyzer[] = "Classes/MutualExtension";
   analyzer[] = "Classes/NoMagicWithArray";
   analyzer[] = "Classes/NoPSSOutsideClass";
   analyzer[] = "Classes/NoSelfReferencingConstant";
   analyzer[] = "Classes/RaisedAccessLevel";
   analyzer[] = "Classes/ThisIsForClasses";
   analyzer[] = "Classes/UndefinedConstants";
   analyzer[] = "Classes/UsingThisOutsideAClass";
   analyzer[] = "Classes/WrongTypedPropertyInit";
   analyzer[] = "Enums/DuplicateCaseValue";
   analyzer[] = "Enums/NoMagicMethod";
   analyzer[] = "Exceptions/CantThrow";
   analyzer[] = "Functions/DeprecatedCallable";
   analyzer[] = "Functions/DuplicateNamedParameter";
   analyzer[] = "Functions/MismatchTypeAndDefault";
   analyzer[] = "Functions/MustReturn";
   analyzer[] = "Functions/OnlyVariableForReference";
   analyzer[] = "Functions/TypehintMustBeReturned";
   analyzer[] = "Functions/WrongReturnedType";
   analyzer[] = "Interfaces/AvoidSelfInInterface";
   analyzer[] = "Interfaces/CantImplementTraversable";
   analyzer[] = "Interfaces/CantOverloadConstants";
   analyzer[] = "Interfaces/IsNotImplemented";
   analyzer[] = "Interfaces/RepeatedInterface";
   analyzer[] = "Interfaces/UndefinedInterfaces";
   analyzer[] = "Php/CloneConstant";
   analyzer[] = "Php/FalseToArray";
   analyzer[] = "Php/JsonSerializeReturnType";
   analyzer[] = "Php/OnlyVariablePassedByReference";
   analyzer[] = "Structures/ImplicitConversionToInt";
   analyzer[] = "Structures/InvalidCast";
   analyzer[] = "Traits/MethodCollisionTraits";
   analyzer[] = "Traits/TraitNotFound";
   analyzer[] = "Traits/UndefinedInsteadof";
   analyzer[] = "Traits/UndefinedTrait";
   analyzer[] = "Traits/UselessAlias";
   analyzer[] = "Typehints/WrongTypeWithDefault";


.. _annex-yaml-lintbutwontexec:

LintButWontExec for .exakat.yaml
++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'LintButWontExec':
     - 'Classes/AbstractOrImplements'
     - 'Classes/CantOverwriteFinalConstant'
     - 'Classes/CloneWithNonObject'
     - 'Classes/CouldBeStringable'
     - 'Classes/Finalclass'
     - 'Classes/Finalmethod'
     - 'Classes/ImplementedMethodsArePublic'
     - 'Classes/IncompatibleSignature'
     - 'Classes/InheritedPropertyMustMatch'
     - 'Classes/MethodSignatureMustBeCompatible'
     - 'Classes/MismatchProperties'
     - 'Classes/MutualExtension'
     - 'Classes/NoMagicWithArray'
     - 'Classes/NoPSSOutsideClass'
     - 'Classes/NoSelfReferencingConstant'
     - 'Classes/RaisedAccessLevel'
     - 'Classes/ThisIsForClasses'
     - 'Classes/UndefinedConstants'
     - 'Classes/UsingThisOutsideAClass'
     - 'Classes/WrongTypedPropertyInit'
     - 'Enums/DuplicateCaseValue'
     - 'Enums/NoMagicMethod'
     - 'Exceptions/CantThrow'
     - 'Functions/DeprecatedCallable'
     - 'Functions/DuplicateNamedParameter'
     - 'Functions/MismatchTypeAndDefault'
     - 'Functions/MustReturn'
     - 'Functions/OnlyVariableForReference'
     - 'Functions/TypehintMustBeReturned'
     - 'Functions/WrongReturnedType'
     - 'Interfaces/AvoidSelfInInterface'
     - 'Interfaces/CantImplementTraversable'
     - 'Interfaces/CantOverloadConstants'
     - 'Interfaces/IsNotImplemented'
     - 'Interfaces/RepeatedInterface'
     - 'Interfaces/UndefinedInterfaces'
     - 'Php/CloneConstant'
     - 'Php/FalseToArray'
     - 'Php/JsonSerializeReturnType'
     - 'Php/OnlyVariablePassedByReference'
     - 'Structures/ImplicitConversionToInt'
     - 'Structures/InvalidCast'
     - 'Traits/MethodCollisionTraits'
     - 'Traits/TraitNotFound'
     - 'Traits/UndefinedInsteadof'
     - 'Traits/UndefinedTrait'
     - 'Traits/UselessAlias'
     - 'Typehints/WrongTypeWithDefault'




.. _annex-nodoc:

NoDoc
#####


.. _annex-ini-nodoc:

NoDoc for INI
+++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [NoDoc]
   analyzer[] = "Complete/CreateCompactVariables";
   analyzer[] = "Complete/CreateDefaultValues";
   analyzer[] = "Complete/CreateForeachDefault";
   analyzer[] = "Complete/CreateMagicMethod";
   analyzer[] = "Complete/CreateMagicProperty";
   analyzer[] = "Complete/ExtendedTypehints";
   analyzer[] = "Complete/FollowClosureDefinition";
   analyzer[] = "Complete/IsExtStructure";
   analyzer[] = "Complete/IsPhpStructure";
   analyzer[] = "Complete/IsStubStructure";
   analyzer[] = "Complete/MakeAllStatics";
   analyzer[] = "Complete/MakeClassConstantDefinition";
   analyzer[] = "Complete/MakeClassMethodDefinition";
   analyzer[] = "Complete/MakeFunctioncallWithReference";
   analyzer[] = "Complete/OverwrittenConstants";
   analyzer[] = "Complete/OverwrittenMethods";
   analyzer[] = "Complete/OverwrittenProperties";
   analyzer[] = "Complete/PhpExtStubPropertyMethod";
   analyzer[] = "Complete/PhpNativeReference";
   analyzer[] = "Complete/PropagateConstants";
   analyzer[] = "Complete/ReturnTypehint";
   analyzer[] = "Complete/SetArrayClassDefinition";
   analyzer[] = "Complete/SetClassAliasDefinition";
   analyzer[] = "Complete/SetClassMethodRemoteDefinition";
   analyzer[] = "Complete/SetClassPropertyDefinitionWithTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithGlobal";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithInjection";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithLocalNew";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithParenthesis";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithReturnTypehint";
   analyzer[] = "Complete/SetClassRemoteDefinitionWithTypehint";
   analyzer[] = "Complete/SetCloneLink";
   analyzer[] = "Complete/SetParentDefinition";
   analyzer[] = "Complete/SolveTraitMethods";
   analyzer[] = "Complete/VariableTypehint";
   analyzer[] = "Variables/IsLocalConstant";


.. _annex-yaml-nodoc:

NoDoc for .exakat.yaml
++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'NoDoc':
     - 'Complete/CreateCompactVariables'
     - 'Complete/CreateDefaultValues'
     - 'Complete/CreateForeachDefault'
     - 'Complete/CreateMagicMethod'
     - 'Complete/CreateMagicProperty'
     - 'Complete/ExtendedTypehints'
     - 'Complete/FollowClosureDefinition'
     - 'Complete/IsExtStructure'
     - 'Complete/IsPhpStructure'
     - 'Complete/IsStubStructure'
     - 'Complete/MakeAllStatics'
     - 'Complete/MakeClassConstantDefinition'
     - 'Complete/MakeClassMethodDefinition'
     - 'Complete/MakeFunctioncallWithReference'
     - 'Complete/OverwrittenConstants'
     - 'Complete/OverwrittenMethods'
     - 'Complete/OverwrittenProperties'
     - 'Complete/PhpExtStubPropertyMethod'
     - 'Complete/PhpNativeReference'
     - 'Complete/PropagateConstants'
     - 'Complete/ReturnTypehint'
     - 'Complete/SetArrayClassDefinition'
     - 'Complete/SetClassAliasDefinition'
     - 'Complete/SetClassMethodRemoteDefinition'
     - 'Complete/SetClassPropertyDefinitionWithTypehint'
     - 'Complete/SetClassRemoteDefinitionWithGlobal'
     - 'Complete/SetClassRemoteDefinitionWithInjection'
     - 'Complete/SetClassRemoteDefinitionWithLocalNew'
     - 'Complete/SetClassRemoteDefinitionWithParenthesis'
     - 'Complete/SetClassRemoteDefinitionWithReturnTypehint'
     - 'Complete/SetClassRemoteDefinitionWithTypehint'
     - 'Complete/SetCloneLink'
     - 'Complete/SetParentDefinition'
     - 'Complete/SolveTraitMethods'
     - 'Complete/VariableTypehint'
     - 'Variables/IsLocalConstant'




.. _annex-one-liners:

One Liners
##########


.. _annex-ini-one-liners:

One Liners for INI
++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [One Liners]
   analyzer[] = "Functions/UseArrowFunctions";
   analyzer[] = "Php/Coalesce";
   analyzer[] = "Php/ShortTernary";
   analyzer[] = "Php/ThrowWasAnExpression";
   analyzer[] = "Php/UseNullSafeOperator";


.. _annex-yaml-one-liners:

One Liners for .exakat.yaml
+++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'One Liners':
     - 'Functions/UseArrowFunctions'
     - 'Php/Coalesce'
     - 'Php/ShortTernary'
     - 'Php/ThrowWasAnExpression'
     - 'Php/UseNullSafeOperator'




.. _annex-php-recommendations:

PHP recommendations
###################


.. _annex-ini-php-recommendations:

PHP recommendations for INI
+++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [PHP recommendations]
   analyzer[] = "Attributes/MissingAttributeAttribute";
   analyzer[] = "Classes/CouldBeStringable";
   analyzer[] = "Classes/ThrowInDestruct";
   analyzer[] = "Constants/BadConstantnames";
   analyzer[] = "Interfaces/NoConstructorInInterface";
   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
   analyzer[] = "Performances/AvoidArrayPush";
   analyzer[] = "Php/Crc32MightBeNegative";
   analyzer[] = "Php/ImplodeOneArg";
   analyzer[] = "Php/NoCastToInt";
   analyzer[] = "Php/NotScalarType";
   analyzer[] = "Php/ReservedMethods";
   analyzer[] = "Php/ReturnWithParenthesis";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/NoIssetWithEmpty";
   analyzer[] = "Structures/ShortTags";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/UnsupportedOperandTypes";
   analyzer[] = "Structures/UseConstant";
   analyzer[] = "Structures/UselessCasting";
   analyzer[] = "Type/NoRealComparison";


.. _annex-yaml-php-recommendations:

PHP recommendations for .exakat.yaml
++++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'PHP recommendations':
     - 'Attributes/MissingAttributeAttribute'
     - 'Classes/CouldBeStringable'
     - 'Classes/ThrowInDestruct'
     - 'Constants/BadConstantnames'
     - 'Interfaces/NoConstructorInInterface'
     - 'Namespaces/UseWithFullyQualifiedNS'
     - 'Performances/AvoidArrayPush'
     - 'Php/Crc32MightBeNegative'
     - 'Php/ImplodeOneArg'
     - 'Php/NoCastToInt'
     - 'Php/NotScalarType'
     - 'Php/ReservedMethods'
     - 'Php/ReturnWithParenthesis'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/EvalUsage'
     - 'Structures/NoIssetWithEmpty'
     - 'Structures/ShortTags'
     - 'Structures/StrposCompare'
     - 'Structures/UnsupportedOperandTypes'
     - 'Structures/UseConstant'
     - 'Structures/UselessCasting'
     - 'Type/NoRealComparison'




.. _annex-php-recommendations:

PHP recommendations
###################


.. _annex-ini-php-recommendations:

PHP recommendations for INI
+++++++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [PHP recommendations]
   analyzer[] = "";


.. _annex-yaml-php-recommendations:

PHP recommendations for .exakat.yaml
++++++++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'PHP recommendations':
     - ''




.. _annex-performances:

Performances
############


.. _annex-ini-performances:

Performances for INI
++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Performances]
   analyzer[] = "Arrays/GettingLastElement";
   analyzer[] = "Arrays/SliceFirst";
   analyzer[] = "Classes/MakeMagicConcrete";
   analyzer[] = "Classes/UseClassOperator";
   analyzer[] = "Functions/Closure2String";
   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/Autoappend";
   analyzer[] = "Performances/AvoidArrayPush";
   analyzer[] = "Performances/CacheVariableOutsideLoop";
   analyzer[] = "Performances/ClassOperator";
   analyzer[] = "Performances/CountToAppend";
   analyzer[] = "Performances/CsvInLoops";
   analyzer[] = "Performances/DoInBase";
   analyzer[] = "Performances/DoubleArrayFlip";
   analyzer[] = "Performances/EllipsisMerge";
   analyzer[] = "Performances/FetchOneRowFormat";
   analyzer[] = "Performances/IssetWholeArray";
   analyzer[] = "Performances/JoinFile";
   analyzer[] = "Performances/MakeOneCall";
   analyzer[] = "Performances/MbStringInLoop";
   analyzer[] = "Performances/NoConcatInLoop";
   analyzer[] = "Performances/NoGlob";
   analyzer[] = "Performances/NotCountNull";
   analyzer[] = "Performances/OptimizeExplode";
   analyzer[] = "Performances/PHP7EncapsedStrings";
   analyzer[] = "Performances/Php74ArrayKeyExists";
   analyzer[] = "Performances/PreCalculateUse";
   analyzer[] = "Performances/PrePostIncrement";
   analyzer[] = "Performances/RegexOnArrays";
   analyzer[] = "Performances/RegexOnCollector";
   analyzer[] = "Performances/ShouldCacheLocal";
   analyzer[] = "Performances/SimpleSwitch";
   analyzer[] = "Performances/SimplifyForeach";
   analyzer[] = "Performances/SkipEmptyArray";
   analyzer[] = "Performances/SlowFunctions";
   analyzer[] = "Performances/StaticCallDontNeedObjects";
   analyzer[] = "Performances/SubstrFirst";
   analyzer[] = "Performances/SubstrInLoops";
   analyzer[] = "Performances/TooManyExtractions";
   analyzer[] = "Performances/UseBlindVar";
   analyzer[] = "Performances/timeVsstrtotime";
   analyzer[] = "Php/ShouldUseArrayColumn";
   analyzer[] = "Php/ShouldUseFunction";
   analyzer[] = "Php/UsePathinfoArgs";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseYieldFrom";
   analyzer[] = "Structures/EchoWithConcat";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/ForWithFunctioncall";
   analyzer[] = "Structures/GlobalOutsideLoop";
   analyzer[] = "Structures/NestedLoops";
   analyzer[] = "Structures/NoArrayUnique";
   analyzer[] = "Structures/NoAssignationInFunction";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/Noscream";
   analyzer[] = "Structures/RecalledCondition";
   analyzer[] = "Structures/SimplePreg";
   analyzer[] = "Structures/Unpreprocessed";
   analyzer[] = "Structures/WhileListEach";


.. _annex-yaml-performances:

Performances for .exakat.yaml
+++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Performances':
     - 'Arrays/GettingLastElement'
     - 'Arrays/SliceFirst'
     - 'Classes/MakeMagicConcrete'
     - 'Classes/UseClassOperator'
     - 'Functions/Closure2String'
     - 'Performances/ArrayKeyExistsSpeedup'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/Autoappend'
     - 'Performances/AvoidArrayPush'
     - 'Performances/CacheVariableOutsideLoop'
     - 'Performances/ClassOperator'
     - 'Performances/CountToAppend'
     - 'Performances/CsvInLoops'
     - 'Performances/DoInBase'
     - 'Performances/DoubleArrayFlip'
     - 'Performances/EllipsisMerge'
     - 'Performances/FetchOneRowFormat'
     - 'Performances/IssetWholeArray'
     - 'Performances/JoinFile'
     - 'Performances/MakeOneCall'
     - 'Performances/MbStringInLoop'
     - 'Performances/NoConcatInLoop'
     - 'Performances/NoGlob'
     - 'Performances/NotCountNull'
     - 'Performances/OptimizeExplode'
     - 'Performances/PHP7EncapsedStrings'
     - 'Performances/Php74ArrayKeyExists'
     - 'Performances/PreCalculateUse'
     - 'Performances/PrePostIncrement'
     - 'Performances/RegexOnArrays'
     - 'Performances/RegexOnCollector'
     - 'Performances/ShouldCacheLocal'
     - 'Performances/SimpleSwitch'
     - 'Performances/SimplifyForeach'
     - 'Performances/SkipEmptyArray'
     - 'Performances/SlowFunctions'
     - 'Performances/StaticCallDontNeedObjects'
     - 'Performances/SubstrFirst'
     - 'Performances/SubstrInLoops'
     - 'Performances/TooManyExtractions'
     - 'Performances/UseBlindVar'
     - 'Performances/timeVsstrtotime'
     - 'Php/ShouldUseArrayColumn'
     - 'Php/ShouldUseFunction'
     - 'Php/UsePathinfoArgs'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseYieldFrom'
     - 'Structures/EchoWithConcat'
     - 'Structures/EvalUsage'
     - 'Structures/ForWithFunctioncall'
     - 'Structures/GlobalOutsideLoop'
     - 'Structures/NestedLoops'
     - 'Structures/NoArrayUnique'
     - 'Structures/NoAssignationInFunction'
     - 'Structures/NoSubstrOne'
     - 'Structures/Noscream'
     - 'Structures/RecalledCondition'
     - 'Structures/SimplePreg'
     - 'Structures/Unpreprocessed'
     - 'Structures/WhileListEach'




.. _annex-preferences:

Preferences
###########


.. _annex-ini-preferences:

Preferences for INI
+++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Preferences]
   analyzer[] = "Arrays/ArrayBracketConsistence";
   analyzer[] = "Arrays/EmptyFinal";
   analyzer[] = "Classes/NewOnFunctioncallOrIdentifier";
   analyzer[] = "Classes/PPPDeclarationStyle";
   analyzer[] = "Constants/ConstDefinePreference";
   analyzer[] = "Constants/DefineInsensitivePreference";
   analyzer[] = "Constants/InconsistantCase";
   analyzer[] = "Exceptions/CatchE";
   analyzer[] = "Functions/NullTypeFavorite";
   analyzer[] = "Namespaces/ConstantWithUseFavorite";
   analyzer[] = "Php/CloseTagsConsistency";
   analyzer[] = "Php/DeclareEncoding";
   analyzer[] = "Php/DeclareStrict";
   analyzer[] = "Php/DeclareStrictType";
   analyzer[] = "Php/DeclareTicks";
   analyzer[] = "Php/GlobalsVsGlobal";
   analyzer[] = "Php/LetterCharsLogicalFavorite";
   analyzer[] = "Php/ShellFavorite";
   analyzer[] = "Php/UnsetOrCast";
   analyzer[] = "Structures/ArrayCountTripleEqual";
   analyzer[] = "Structures/CastFavorite";
   analyzer[] = "Structures/ComparisonFavorite";
   analyzer[] = "Structures/ConcatenationInterpolationFavorite";
   analyzer[] = "Structures/ConstantComparisonConsistance";
   analyzer[] = "Structures/DateTimePreference";
   analyzer[] = "Structures/DieExitConsistance";
   analyzer[] = "Structures/DifferencePreference";
   analyzer[] = "Structures/EchoPrintConsistance";
   analyzer[] = "Structures/GtOrLtFavorite";
   analyzer[] = "Structures/HeredocDelimiterFavorite";
   analyzer[] = "Structures/IfThenReturnFavorite";
   analyzer[] = "Structures/IsAVersusInstanceof";
   analyzer[] = "Structures/NewLineStyle";
   analyzer[] = "Structures/NotOrNot";
   analyzer[] = "Structures/OneExpressionBracketsConsistency";
   analyzer[] = "Structures/RegexDelimiter";
   analyzer[] = "Structures/ShortOrCompleteComparison";
   analyzer[] = "Structures/StrictInArrayFavorite";
   analyzer[] = "Structures/StringInterpolationFavorite";
   analyzer[] = "Structures/strOrMbFavorite";


.. _annex-yaml-preferences:

Preferences for .exakat.yaml
++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Preferences':
     - 'Arrays/ArrayBracketConsistence'
     - 'Arrays/EmptyFinal'
     - 'Classes/NewOnFunctioncallOrIdentifier'
     - 'Classes/PPPDeclarationStyle'
     - 'Constants/ConstDefinePreference'
     - 'Constants/DefineInsensitivePreference'
     - 'Constants/InconsistantCase'
     - 'Exceptions/CatchE'
     - 'Functions/NullTypeFavorite'
     - 'Namespaces/ConstantWithUseFavorite'
     - 'Php/CloseTagsConsistency'
     - 'Php/DeclareEncoding'
     - 'Php/DeclareStrict'
     - 'Php/DeclareStrictType'
     - 'Php/DeclareTicks'
     - 'Php/GlobalsVsGlobal'
     - 'Php/LetterCharsLogicalFavorite'
     - 'Php/ShellFavorite'
     - 'Php/UnsetOrCast'
     - 'Structures/ArrayCountTripleEqual'
     - 'Structures/CastFavorite'
     - 'Structures/ComparisonFavorite'
     - 'Structures/ConcatenationInterpolationFavorite'
     - 'Structures/ConstantComparisonConsistance'
     - 'Structures/DateTimePreference'
     - 'Structures/DieExitConsistance'
     - 'Structures/DifferencePreference'
     - 'Structures/EchoPrintConsistance'
     - 'Structures/GtOrLtFavorite'
     - 'Structures/HeredocDelimiterFavorite'
     - 'Structures/IfThenReturnFavorite'
     - 'Structures/IsAVersusInstanceof'
     - 'Structures/NewLineStyle'
     - 'Structures/NotOrNot'
     - 'Structures/OneExpressionBracketsConsistency'
     - 'Structures/RegexDelimiter'
     - 'Structures/ShortOrCompleteComparison'
     - 'Structures/StrictInArrayFavorite'
     - 'Structures/StringInterpolationFavorite'
     - 'Structures/strOrMbFavorite'




.. _annex-rector:

Rector
######


.. _annex-ini-rector:

Rector for INI
++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Rector]
   analyzer[] = "Arrays/MultipleIdenticalKeys";
   analyzer[] = "Functions/Closure2String";
   analyzer[] = "Functions/NeverUsedParameter";
   analyzer[] = "Php/IsAWithString";
   analyzer[] = "Structures/AddZero";
   analyzer[] = "Structures/CouldUseShortAssignation";
   analyzer[] = "Structures/CouldUseStrContains";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/ForWithFunctioncall";
   analyzer[] = "Structures/ImpliedIf";
   analyzer[] = "Structures/MultipleDefinedCase";
   analyzer[] = "Structures/MultiplyByOne";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/ShouldPreprocess";
   analyzer[] = "Type/ShouldTypecast";


.. _annex-yaml-rector:

Rector for .exakat.yaml
+++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Rector':
     - 'Arrays/MultipleIdenticalKeys'
     - 'Functions/Closure2String'
     - 'Functions/NeverUsedParameter'
     - 'Php/IsAWithString'
     - 'Structures/AddZero'
     - 'Structures/CouldUseShortAssignation'
     - 'Structures/CouldUseStrContains'
     - 'Structures/ElseIfElseif'
     - 'Structures/ForWithFunctioncall'
     - 'Structures/ImpliedIf'
     - 'Structures/MultipleDefinedCase'
     - 'Structures/MultiplyByOne'
     - 'Structures/NoChoice'
     - 'Structures/ShouldPreprocess'
     - 'Type/ShouldTypecast'




.. _annex-security:

Security
########


.. _annex-ini-security:

Security for INI
++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Security]
   analyzer[] = "Functions/HardcodedPasswords";
   analyzer[] = "Php/BetterRand";
   analyzer[] = "Security/AnchorRegex";
   analyzer[] = "Security/AvoidThoseCrypto";
   analyzer[] = "Security/CompareHash";
   analyzer[] = "Security/ConfigureExtract";
   analyzer[] = "Security/CryptoKeyLength";
   analyzer[] = "Security/CurlOptions";
   analyzer[] = "Security/DirectInjection";
   analyzer[] = "Security/DontEchoError";
   analyzer[] = "Security/DynamicDl";
   analyzer[] = "Security/EncodedLetters";
   analyzer[] = "Security/FilterInputSource";
   analyzer[] = "Security/FilterNotRaw";
   analyzer[] = "Security/IncompatibleTypesWithIncoming";
   analyzer[] = "Security/IndirectInjection";
   analyzer[] = "Security/IntegerConversion";
   analyzer[] = "Security/KeepFilesRestricted";
   analyzer[] = "Security/MinusOneOnError";
   analyzer[] = "Security/MkdirDefault";
   analyzer[] = "Security/MoveUploadedFile";
   analyzer[] = "Security/NoEntIgnore";
   analyzer[] = "Security/NoNetForXmlLoad";
   analyzer[] = "Security/NoSleep";
   analyzer[] = "Security/NoWeakSSLCrypto";
   analyzer[] = "Security/RegisterGlobals";
   analyzer[] = "Security/SafeHttpHeaders";
   analyzer[] = "Security/SessionCachedData";
   analyzer[] = "Security/SessionLazyWrite";
   analyzer[] = "Security/SetCookieArgs";
   analyzer[] = "Security/ShouldUsePreparedStatement";
   analyzer[] = "Security/ShouldUseSessionRegenerateId";
   analyzer[] = "Security/Sqlite3RequiresSingleQuotes";
   analyzer[] = "Security/UnserializeSecondArg";
   analyzer[] = "Security/UploadFilenameInjection";
   analyzer[] = "Security/parseUrlWithoutParameters";
   analyzer[] = "Structures/EvalUsage";
   analyzer[] = "Structures/EvalWithoutTry";
   analyzer[] = "Structures/Fallthrough";
   analyzer[] = "Structures/NoHardcodedHash";
   analyzer[] = "Structures/NoHardcodedIp";
   analyzer[] = "Structures/NoHardcodedPort";
   analyzer[] = "Structures/NoReturnInFinally";
   analyzer[] = "Structures/PhpinfoUsage";
   analyzer[] = "Structures/RandomWithoutTry";
   analyzer[] = "Structures/VardumpUsage";
   analyzer[] = "Structures/pregOptionE";


.. _annex-yaml-security:

Security for .exakat.yaml
+++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Security':
     - 'Functions/HardcodedPasswords'
     - 'Php/BetterRand'
     - 'Security/AnchorRegex'
     - 'Security/AvoidThoseCrypto'
     - 'Security/CompareHash'
     - 'Security/ConfigureExtract'
     - 'Security/CryptoKeyLength'
     - 'Security/CurlOptions'
     - 'Security/DirectInjection'
     - 'Security/DontEchoError'
     - 'Security/DynamicDl'
     - 'Security/EncodedLetters'
     - 'Security/FilterInputSource'
     - 'Security/FilterNotRaw'
     - 'Security/IncompatibleTypesWithIncoming'
     - 'Security/IndirectInjection'
     - 'Security/IntegerConversion'
     - 'Security/KeepFilesRestricted'
     - 'Security/MinusOneOnError'
     - 'Security/MkdirDefault'
     - 'Security/MoveUploadedFile'
     - 'Security/NoEntIgnore'
     - 'Security/NoNetForXmlLoad'
     - 'Security/NoSleep'
     - 'Security/NoWeakSSLCrypto'
     - 'Security/RegisterGlobals'
     - 'Security/SafeHttpHeaders'
     - 'Security/SessionCachedData'
     - 'Security/SessionLazyWrite'
     - 'Security/SetCookieArgs'
     - 'Security/ShouldUsePreparedStatement'
     - 'Security/ShouldUseSessionRegenerateId'
     - 'Security/Sqlite3RequiresSingleQuotes'
     - 'Security/UnserializeSecondArg'
     - 'Security/UploadFilenameInjection'
     - 'Security/parseUrlWithoutParameters'
     - 'Structures/EvalUsage'
     - 'Structures/EvalWithoutTry'
     - 'Structures/Fallthrough'
     - 'Structures/NoHardcodedHash'
     - 'Structures/NoHardcodedIp'
     - 'Structures/NoHardcodedPort'
     - 'Structures/NoReturnInFinally'
     - 'Structures/PhpinfoUsage'
     - 'Structures/RandomWithoutTry'
     - 'Structures/VardumpUsage'
     - 'Structures/pregOptionE'




.. _annex-semantics:

Semantics
#########


.. _annex-ini-semantics:

Semantics for INI
+++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Semantics]
   analyzer[] = "Arrays/AmbiguousKeys";
   analyzer[] = "Arrays/WeirdIndex";
   analyzer[] = "Classes/AmbiguousStatic";
   analyzer[] = "Classes/AmbiguousVisibilities";
   analyzer[] = "Classes/MethodPropertyConfusion";
   analyzer[] = "Classes/PropertyMethodSameName";
   analyzer[] = "Classes/StrangeName";
   analyzer[] = "Constants/ConstantStrangeNames";
   analyzer[] = "Constants/CouldBeConstant";
   analyzer[] = "Constants/StrangeName";
   analyzer[] = "Functions/FnArgumentVariableConfusion";
   analyzer[] = "Functions/FunctionCalledWithOtherCase";
   analyzer[] = "Functions/MismatchParameterAndType";
   analyzer[] = "Functions/OneLetterFunctions";
   analyzer[] = "Functions/ParameterHiding";
   analyzer[] = "Functions/PrefixToType";
   analyzer[] = "Functions/SemanticTyping";
   analyzer[] = "Functions/WrongTypehintedName";
   analyzer[] = "Namespaces/AliasConfusion";
   analyzer[] = "Namespaces/OverloadExistingNames";
   analyzer[] = "Php/ClassFunctionConfusion";
   analyzer[] = "Php/ReservedNames";
   analyzer[] = "Structures/ArrayAccessOnLiteralArray";
   analyzer[] = "Structures/DontUseTheTypeAsVariable";
   analyzer[] = "Structures/PropertyVariableConfusion";
   analyzer[] = "Structures/SGVariablesConfusion";
   analyzer[] = "Structures/TooManyChainedCalls";
   analyzer[] = "Structures/WrongLocale";
   analyzer[] = "Type/DuplicateLiteral";
   analyzer[] = "Type/SimilarIntegers";
   analyzer[] = "Variables/AmbiguousTypes";
   analyzer[] = "Variables/NoInitialS";
   analyzer[] = "Variables/NoVariableNeeded";
   analyzer[] = "Variables/StrangeName";
   analyzer[] = "Variables/VariableOneLetter";


.. _annex-yaml-semantics:

Semantics for .exakat.yaml
++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Semantics':
     - 'Arrays/AmbiguousKeys'
     - 'Arrays/WeirdIndex'
     - 'Classes/AmbiguousStatic'
     - 'Classes/AmbiguousVisibilities'
     - 'Classes/MethodPropertyConfusion'
     - 'Classes/PropertyMethodSameName'
     - 'Classes/StrangeName'
     - 'Constants/ConstantStrangeNames'
     - 'Constants/CouldBeConstant'
     - 'Constants/StrangeName'
     - 'Functions/FnArgumentVariableConfusion'
     - 'Functions/FunctionCalledWithOtherCase'
     - 'Functions/MismatchParameterAndType'
     - 'Functions/OneLetterFunctions'
     - 'Functions/ParameterHiding'
     - 'Functions/PrefixToType'
     - 'Functions/SemanticTyping'
     - 'Functions/WrongTypehintedName'
     - 'Namespaces/AliasConfusion'
     - 'Namespaces/OverloadExistingNames'
     - 'Php/ClassFunctionConfusion'
     - 'Php/ReservedNames'
     - 'Structures/ArrayAccessOnLiteralArray'
     - 'Structures/DontUseTheTypeAsVariable'
     - 'Structures/PropertyVariableConfusion'
     - 'Structures/SGVariablesConfusion'
     - 'Structures/TooManyChainedCalls'
     - 'Structures/WrongLocale'
     - 'Type/DuplicateLiteral'
     - 'Type/SimilarIntegers'
     - 'Variables/AmbiguousTypes'
     - 'Variables/NoInitialS'
     - 'Variables/NoVariableNeeded'
     - 'Variables/StrangeName'
     - 'Variables/VariableOneLetter'




.. _annex-suggestions:

Suggestions
###########


.. _annex-ini-suggestions:

Suggestions for INI
+++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Suggestions]
   analyzer[] = "Arrays/RandomlySortedLiterals";
   analyzer[] = "Arrays/ShouldPreprocess";
   analyzer[] = "Arrays/SliceFirst";
   analyzer[] = "Attributes/MissingOverrideMethod";
   analyzer[] = "Classes/CancelCommonMethod";
   analyzer[] = "Classes/CheckAfterNullSafeOperator";
   analyzer[] = "Classes/CouldBeAbstractMethod";
   analyzer[] = "Classes/CouldBeIterable";
   analyzer[] = "Classes/CouldBeReadonly";
   analyzer[] = "Classes/CouldBeReadonlyProperty";
   analyzer[] = "Classes/CouldSetPropertyDefault";
   analyzer[] = "Classes/CouldUseClassOperator";
   analyzer[] = "Classes/LoweredAccessLevel";
   analyzer[] = "Classes/MagicMethodReturntypes";
   analyzer[] = "Classes/ParentFirst";
   analyzer[] = "Classes/ShouldDeepClone";
   analyzer[] = "Classes/ShouldHaveDestructor";
   analyzer[] = "Classes/ShouldUseSelf";
   analyzer[] = "Classes/TooManyChildren";
   analyzer[] = "Classes/UnitializedProperties";
   analyzer[] = "Classes/UselessTypehint";
   analyzer[] = "Constants/CouldUseConstant";
   analyzer[] = "Enums/CouldBeEnum";
   analyzer[] = "Exceptions/CouldDropVariable";
   analyzer[] = "Exceptions/CouldUseTry";
   analyzer[] = "Exceptions/LargeTryBlock";
   analyzer[] = "Exceptions/LongPreparation";
   analyzer[] = "Exceptions/OverwriteException";
   analyzer[] = "Exceptions/ThrowRawExceptions";
   analyzer[] = "Exceptions/UnusedExceptionVariable";
   analyzer[] = "Functions/AddDefaultValue";
   analyzer[] = "Functions/Closure2String";
   analyzer[] = "Functions/CouldBeStaticClosure";
   analyzer[] = "Functions/CouldCentralize";
   analyzer[] = "Functions/NeverUsedParameter";
   analyzer[] = "Functions/NoReturnUsed";
   analyzer[] = "Functions/RemoveParameterWithNamedOnes";
   analyzer[] = "Functions/TooManyParameters";
   analyzer[] = "Functions/TooMuchIndented";
   analyzer[] = "Functions/UselessDefault";
   analyzer[] = "Interfaces/AlreadyParentsInterface";
   analyzer[] = "Interfaces/UnusedInterfaces";
   analyzer[] = "Namespaces/AliasConfusion";
   analyzer[] = "Namespaces/CouldUseAlias";
   analyzer[] = "Namespaces/CouldUseMagicConstant";
   analyzer[] = "Patterns/AbstractAway";
   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
   analyzer[] = "Performances/IssetWholeArray";
   analyzer[] = "Performances/SubstrFirst";
   analyzer[] = "Php/AvoidReal";
   analyzer[] = "Php/CompactInexistant";
   analyzer[] = "Php/CouldUseIsCountable";
   analyzer[] = "Php/CouldUsePromotedProperties";
   analyzer[] = "Php/DetectCurrentClass";
   analyzer[] = "Php/ImplodeOneArg";
   analyzer[] = "Php/IssetMultipleArgs";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/NewExponent";
   analyzer[] = "Php/PregMatchAllFlag";
   analyzer[] = "Php/ReturnWithParenthesis";
   analyzer[] = "Php/ShouldPreprocess";
   analyzer[] = "Php/ShouldUseArrayColumn";
   analyzer[] = "Php/ShouldUseArrayFilter";
   analyzer[] = "Php/ShouldUseCoalesce";
   analyzer[] = "Php/UseDateTimeImmutable";
   analyzer[] = "Php/UseGetDebugType";
   analyzer[] = "Php/UseSessionStartOptions";
   analyzer[] = "Php/UseStrContains";
   analyzer[] = "Structures/ArraySearchMultipleKeys";
   analyzer[] = "Structures/BasenameSuffix";
   analyzer[] = "Structures/BlindVariableUsedBeyondLoop";
   analyzer[] = "Structures/BooleanStrictComparison";
   analyzer[] = "Structures/CouldBeArrayCombine";
   analyzer[] = "Structures/CouldBeSpaceship";
   analyzer[] = "Structures/CouldBeTernary";
   analyzer[] = "Structures/CouldCastToArray";
   analyzer[] = "Structures/CouldUseArrayFillKeys";
   analyzer[] = "Structures/CouldUseArraySum";
   analyzer[] = "Structures/CouldUseArrayUnique";
   analyzer[] = "Structures/CouldUseCompact";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/CouldUseMatch";
   analyzer[] = "Structures/CouldUseNullableOperator";
   analyzer[] = "Structures/CouldUseStrContains";
   analyzer[] = "Structures/DeclareStaticOnce";
   analyzer[] = "Structures/DirectlyUseFile";
   analyzer[] = "Structures/DontCompareTypedBoolean";
   analyzer[] = "Structures/DontLoopOnYield";
   analyzer[] = "Structures/DropElseAfterReturn";
   analyzer[] = "Structures/EchoWithConcat";
   analyzer[] = "Structures/EmptyWithExpression";
   analyzer[] = "Structures/FunctionPreSubscripting";
   analyzer[] = "Structures/JsonEncodeExceptions";
   analyzer[] = "Structures/JsonWithOption";
   analyzer[] = "Structures/ListOmissions";
   analyzer[] = "Structures/LongBlock";
   analyzer[] = "Structures/MismatchedTernary";
   analyzer[] = "Structures/MultilineExpressions";
   analyzer[] = "Structures/MultipleSimilarCalls";
   analyzer[] = "Structures/MultipleUnset";
   analyzer[] = "Structures/NamedRegex";
   analyzer[] = "Structures/NoNeedGetClass";
   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/OneIfIsSufficient";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/PossibleIncrement";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/ReuseVariable";
   analyzer[] = "Structures/SGVariablesConfusion";
   analyzer[] = "Structures/SetAside";
   analyzer[] = "Structures/ShouldUseForeach";
   analyzer[] = "Structures/ShouldUseMath";
   analyzer[] = "Structures/ShouldUseOperator";
   analyzer[] = "Structures/SubstrLastArg";
   analyzer[] = "Structures/SubstrToTrim";
   analyzer[] = "Structures/TooManyElseif";
   analyzer[] = "Structures/UnreachableCode";
   analyzer[] = "Structures/UseArrayFunctions";
   analyzer[] = "Structures/UseCaseValue";
   analyzer[] = "Structures/UseCountRecursive";
   analyzer[] = "Structures/UseFileAppend";
   analyzer[] = "Structures/UseListWithForeach";
   analyzer[] = "Structures/UseStrEndsWith";
   analyzer[] = "Structures/UseStrStartsWith";
   analyzer[] = "Structures/UseUrlQueryFunctions";
   analyzer[] = "Structures/WhileListEach";
   analyzer[] = "Traits/MultipleUsage";
   analyzer[] = "Variables/ComplexDynamicNames";
   analyzer[] = "Variables/NoStaticVarInMethod";


.. _annex-yaml-suggestions:

Suggestions for .exakat.yaml
++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Suggestions':
     - 'Arrays/RandomlySortedLiterals'
     - 'Arrays/ShouldPreprocess'
     - 'Arrays/SliceFirst'
     - 'Attributes/MissingOverrideMethod'
     - 'Classes/CancelCommonMethod'
     - 'Classes/CheckAfterNullSafeOperator'
     - 'Classes/CouldBeAbstractMethod'
     - 'Classes/CouldBeIterable'
     - 'Classes/CouldBeReadonly'
     - 'Classes/CouldBeReadonlyProperty'
     - 'Classes/CouldSetPropertyDefault'
     - 'Classes/CouldUseClassOperator'
     - 'Classes/LoweredAccessLevel'
     - 'Classes/MagicMethodReturntypes'
     - 'Classes/ParentFirst'
     - 'Classes/ShouldDeepClone'
     - 'Classes/ShouldHaveDestructor'
     - 'Classes/ShouldUseSelf'
     - 'Classes/TooManyChildren'
     - 'Classes/UnitializedProperties'
     - 'Classes/UselessTypehint'
     - 'Constants/CouldUseConstant'
     - 'Enums/CouldBeEnum'
     - 'Exceptions/CouldDropVariable'
     - 'Exceptions/CouldUseTry'
     - 'Exceptions/LargeTryBlock'
     - 'Exceptions/LongPreparation'
     - 'Exceptions/OverwriteException'
     - 'Exceptions/ThrowRawExceptions'
     - 'Exceptions/UnusedExceptionVariable'
     - 'Functions/AddDefaultValue'
     - 'Functions/Closure2String'
     - 'Functions/CouldBeStaticClosure'
     - 'Functions/CouldCentralize'
     - 'Functions/NeverUsedParameter'
     - 'Functions/NoReturnUsed'
     - 'Functions/RemoveParameterWithNamedOnes'
     - 'Functions/TooManyParameters'
     - 'Functions/TooMuchIndented'
     - 'Functions/UselessDefault'
     - 'Interfaces/AlreadyParentsInterface'
     - 'Interfaces/UnusedInterfaces'
     - 'Namespaces/AliasConfusion'
     - 'Namespaces/CouldUseAlias'
     - 'Namespaces/CouldUseMagicConstant'
     - 'Patterns/AbstractAway'
     - 'Performances/ArrayKeyExistsSpeedup'
     - 'Performances/IssetWholeArray'
     - 'Performances/SubstrFirst'
     - 'Php/AvoidReal'
     - 'Php/CompactInexistant'
     - 'Php/CouldUseIsCountable'
     - 'Php/CouldUsePromotedProperties'
     - 'Php/DetectCurrentClass'
     - 'Php/ImplodeOneArg'
     - 'Php/IssetMultipleArgs'
     - 'Php/LogicalInLetters'
     - 'Php/NewExponent'
     - 'Php/PregMatchAllFlag'
     - 'Php/ReturnWithParenthesis'
     - 'Php/ShouldPreprocess'
     - 'Php/ShouldUseArrayColumn'
     - 'Php/ShouldUseArrayFilter'
     - 'Php/ShouldUseCoalesce'
     - 'Php/UseDateTimeImmutable'
     - 'Php/UseGetDebugType'
     - 'Php/UseSessionStartOptions'
     - 'Php/UseStrContains'
     - 'Structures/ArraySearchMultipleKeys'
     - 'Structures/BasenameSuffix'
     - 'Structures/BlindVariableUsedBeyondLoop'
     - 'Structures/BooleanStrictComparison'
     - 'Structures/CouldBeArrayCombine'
     - 'Structures/CouldBeSpaceship'
     - 'Structures/CouldBeTernary'
     - 'Structures/CouldCastToArray'
     - 'Structures/CouldUseArrayFillKeys'
     - 'Structures/CouldUseArraySum'
     - 'Structures/CouldUseArrayUnique'
     - 'Structures/CouldUseCompact'
     - 'Structures/CouldUseDir'
     - 'Structures/CouldUseMatch'
     - 'Structures/CouldUseNullableOperator'
     - 'Structures/CouldUseStrContains'
     - 'Structures/DeclareStaticOnce'
     - 'Structures/DirectlyUseFile'
     - 'Structures/DontCompareTypedBoolean'
     - 'Structures/DontLoopOnYield'
     - 'Structures/DropElseAfterReturn'
     - 'Structures/EchoWithConcat'
     - 'Structures/EmptyWithExpression'
     - 'Structures/FunctionPreSubscripting'
     - 'Structures/JsonEncodeExceptions'
     - 'Structures/JsonWithOption'
     - 'Structures/ListOmissions'
     - 'Structures/LongBlock'
     - 'Structures/MismatchedTernary'
     - 'Structures/MultilineExpressions'
     - 'Structures/MultipleSimilarCalls'
     - 'Structures/MultipleUnset'
     - 'Structures/NamedRegex'
     - 'Structures/NoNeedGetClass'
     - 'Structures/NoParenthesisForLanguageConstruct'
     - 'Structures/NoSubstrOne'
     - 'Structures/OneIfIsSufficient'
     - 'Structures/PHP7Dirname'
     - 'Structures/PossibleIncrement'
     - 'Structures/RepeatedPrint'
     - 'Structures/ReuseVariable'
     - 'Structures/SGVariablesConfusion'
     - 'Structures/SetAside'
     - 'Structures/ShouldUseForeach'
     - 'Structures/ShouldUseMath'
     - 'Structures/ShouldUseOperator'
     - 'Structures/SubstrLastArg'
     - 'Structures/SubstrToTrim'
     - 'Structures/TooManyElseif'
     - 'Structures/UnreachableCode'
     - 'Structures/UseArrayFunctions'
     - 'Structures/UseCaseValue'
     - 'Structures/UseCountRecursive'
     - 'Structures/UseFileAppend'
     - 'Structures/UseListWithForeach'
     - 'Structures/UseStrEndsWith'
     - 'Structures/UseStrStartsWith'
     - 'Structures/UseUrlQueryFunctions'
     - 'Structures/WhileListEach'
     - 'Traits/MultipleUsage'
     - 'Variables/ComplexDynamicNames'
     - 'Variables/NoStaticVarInMethod'




.. _annex-surprising:

Surprising
##########


.. _annex-ini-surprising:

Surprising for INI
++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Surprising]
   analyzer[] = "Structures/SequenceInFor";
   analyzer[] = "Structures/StrposLessThanOne";


.. _annex-yaml-surprising:

Surprising for .exakat.yaml
+++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Surprising':
     - 'Structures/SequenceInFor'
     - 'Structures/StrposLessThanOne'




.. _annex-top10:

Top10
#####


.. _annex-ini-top10:

Top10 for INI
+++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Top10]
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Classes/UnitializedProperties";
   analyzer[] = "Classes/UnresolvedInstanceof";
   analyzer[] = "Constants/ConstRecommended";
   analyzer[] = "Functions/ShouldYieldWithKey";
   analyzer[] = "Performances/ArrayMergeInLoops";
   analyzer[] = "Performances/CsvInLoops";
   analyzer[] = "Performances/NoConcatInLoop";
   analyzer[] = "Performances/SubstrFirst";
   analyzer[] = "Php/AvoidReal";
   analyzer[] = "Php/ConcatAndAddition";
   analyzer[] = "Php/LetterCharsLogicalFavorite";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/MissingSubpattern";
   analyzer[] = "Structures/CouldUseStrrepeat";
   analyzer[] = "Structures/DanglingArrayReferences";
   analyzer[] = "Structures/FailingSubstrComparison";
   analyzer[] = "Structures/ForWithFunctioncall";
   analyzer[] = "Structures/NextMonthTrap";
   analyzer[] = "Structures/NoChoice";
   analyzer[] = "Structures/NoSubstrOne";
   analyzer[] = "Structures/ObjectReferences";
   analyzer[] = "Structures/QueriesInLoop";
   analyzer[] = "Structures/RepeatedPrint";
   analyzer[] = "Structures/StrposCompare";
   analyzer[] = "Structures/UseListWithForeach";
   analyzer[] = "Type/NoRealComparison";
   analyzer[] = "Variables/VariableUsedOnce";


.. _annex-yaml-top10:

Top10 for .exakat.yaml
++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Top10':
     - 'Classes/DontUnsetProperties'
     - 'Classes/UnitializedProperties'
     - 'Classes/UnresolvedInstanceof'
     - 'Constants/ConstRecommended'
     - 'Functions/ShouldYieldWithKey'
     - 'Performances/ArrayMergeInLoops'
     - 'Performances/CsvInLoops'
     - 'Performances/NoConcatInLoop'
     - 'Performances/SubstrFirst'
     - 'Php/AvoidReal'
     - 'Php/ConcatAndAddition'
     - 'Php/LetterCharsLogicalFavorite'
     - 'Php/LogicalInLetters'
     - 'Php/MissingSubpattern'
     - 'Structures/CouldUseStrrepeat'
     - 'Structures/DanglingArrayReferences'
     - 'Structures/FailingSubstrComparison'
     - 'Structures/ForWithFunctioncall'
     - 'Structures/NextMonthTrap'
     - 'Structures/NoChoice'
     - 'Structures/NoSubstrOne'
     - 'Structures/ObjectReferences'
     - 'Structures/QueriesInLoop'
     - 'Structures/RepeatedPrint'
     - 'Structures/StrposCompare'
     - 'Structures/UseListWithForeach'
     - 'Type/NoRealComparison'
     - 'Variables/VariableUsedOnce'




.. _annex-typechecks:

Typechecks
##########


.. _annex-ini-typechecks:

Typechecks for INI
++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [Typechecks]
   analyzer[] = "Classes/ChildRemoveTypehint";
   analyzer[] = "Classes/CouldBeIterable";
   analyzer[] = "Classes/FossilizedMethod";
   analyzer[] = "Exceptions/PossibleTypeError";
   analyzer[] = "Functions/BadTypehintRelay";
   analyzer[] = "Functions/InsufficientTypehint";
   analyzer[] = "Functions/MismatchTypeAndDefault";
   analyzer[] = "Functions/MismatchedDefaultArguments";
   analyzer[] = "Functions/MismatchedTypehint";
   analyzer[] = "Functions/MissingTypehint";
   analyzer[] = "Functions/NoClassAsTypehint";
   analyzer[] = "Functions/ShouldBeTypehinted";
   analyzer[] = "Functions/WrongArgumentType";
   analyzer[] = "Functions/WrongTypeWithCall";
   analyzer[] = "Interfaces/UselessInterfaces";
   analyzer[] = "Php/NotScalarType";
   analyzer[] = "Typehints/CouldBeCallable";
   analyzer[] = "Typehints/CouldBeFloat";
   analyzer[] = "Typehints/CouldBeGenerator";
   analyzer[] = "Typehints/CouldBeInt";
   analyzer[] = "Typehints/CouldBeIterable";
   analyzer[] = "Typehints/CouldBeNever";
   analyzer[] = "Typehints/CouldBeNull";
   analyzer[] = "Typehints/CouldBeParent";
   analyzer[] = "Typehints/CouldBeResource";
   analyzer[] = "Typehints/CouldBeSelf";
   analyzer[] = "Typehints/CouldBeString";
   analyzer[] = "Typehints/CouldBeVoid";


.. _annex-yaml-typechecks:

Typechecks for .exakat.yaml
+++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'Typechecks':
     - 'Classes/ChildRemoveTypehint'
     - 'Classes/CouldBeIterable'
     - 'Classes/FossilizedMethod'
     - 'Exceptions/PossibleTypeError'
     - 'Functions/BadTypehintRelay'
     - 'Functions/InsufficientTypehint'
     - 'Functions/MismatchTypeAndDefault'
     - 'Functions/MismatchedDefaultArguments'
     - 'Functions/MismatchedTypehint'
     - 'Functions/MissingTypehint'
     - 'Functions/NoClassAsTypehint'
     - 'Functions/ShouldBeTypehinted'
     - 'Functions/WrongArgumentType'
     - 'Functions/WrongTypeWithCall'
     - 'Interfaces/UselessInterfaces'
     - 'Php/NotScalarType'
     - 'Typehints/CouldBeCallable'
     - 'Typehints/CouldBeFloat'
     - 'Typehints/CouldBeGenerator'
     - 'Typehints/CouldBeInt'
     - 'Typehints/CouldBeIterable'
     - 'Typehints/CouldBeNever'
     - 'Typehints/CouldBeNull'
     - 'Typehints/CouldBeParent'
     - 'Typehints/CouldBeResource'
     - 'Typehints/CouldBeSelf'
     - 'Typehints/CouldBeString'
     - 'Typehints/CouldBeVoid'




.. _annex-php-cs-fixable:

php-cs-fixable
##############


.. _annex-ini-php-cs-fixable:

php-cs-fixable for INI
++++++++++++++++++++++


INI configuration for built-in rulesets. Copy them in config/rulesets.ini, and edit them to your owns.
::

 [php-cs-fixable]
   analyzer[] = "Classes/DontUnsetProperties";
   analyzer[] = "Namespaces/UnusedUse";
   analyzer[] = "Php/ImplodeOneArg";
   analyzer[] = "Php/IsnullVsEqualNull";
   analyzer[] = "Php/IssetMultipleArgs";
   analyzer[] = "Php/LogicalInLetters";
   analyzer[] = "Php/NewExponent";
   analyzer[] = "Structures/CouldUseDir";
   analyzer[] = "Structures/ElseIfElseif";
   analyzer[] = "Structures/MultipleUnset";
   analyzer[] = "Structures/PHP7Dirname";
   analyzer[] = "Structures/UseConstant";


.. _annex-yaml-php-cs-fixable:

php-cs-fixable for .exakat.yaml
+++++++++++++++++++++++++++++++


YAML configuration for built-in rulesets. Copy them in your code, with the name .exakat.yaml, and edit them to your owns.
::

  rulesets:
    'php-cs-fixable':
     - 'Classes/DontUnsetProperties'
     - 'Namespaces/UnusedUse'
     - 'Php/ImplodeOneArg'
     - 'Php/IsnullVsEqualNull'
     - 'Php/IssetMultipleArgs'
     - 'Php/LogicalInLetters'
     - 'Php/NewExponent'
     - 'Structures/CouldUseDir'
     - 'Structures/ElseIfElseif'
     - 'Structures/MultipleUnset'
     - 'Structures/PHP7Dirname'
     - 'Structures/UseConstant'




