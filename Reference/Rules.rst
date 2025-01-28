.. _Rules:

Rules
====================

Introduction
------------------------

Exakat provides unique 1661 rules to detect BUGS, CODE SMELLS, SECURITY OR QUALITY ISSUES in your PHP code.

Each rule is documented with code example to allow you to remediate your code. If you want to automate remediation, ours cobblers can are there to fix the issues in your code for your.  

List of Rules
-------------------------


.. toctree::
   :maxdepth: 1

   Rules/Php/FilesFullPath.rst
   Rules/Php/GlobalsVsGlobal.rst
   Rules/Php/RawPostDataUsage.rst
   Rules/Php/PhpErrorMsgUsage.rst
   Rules/Classes/ThisIsForClasses.rst
   Rules/Classes/ThisIsNotAnArray.rst
   Rules/Classes/ThisIsNotForStatic.rst
   Rules/Php/NewExponent.rst
   Rules/Php/StaticclassUsage.rst
   Rules/Structures/Noscream.rst
   Rules/Patterns/AbstractAway.rst
   Rules/Classes/AbstractConstants.rst
   Rules/Classes/Abstractclass.rst
   Rules/Classes/Abstractmethods.rst
   Rules/Classes/AbstractOrImplements.rst
   Rules/Classes/AbstractStatic.rst
   Rules/Classes/AccessProtected.rst
   Rules/Classes/AccessPrivate.rst
   Rules/Functions/AddDefaultValue.rst
   Rules/Complete/ReturnTypehint.rst
   Rules/Structures/AddZero.rst
   Rules/Namespaces/Alias.rst
   Rules/Variables/VariableUppercase.rst
   Rules/Type/CharString.rst
   Rules/Interfaces/AlreadyParentsInterface.rst
   Rules/Traits/AlreadyParentsTrait.rst
   Rules/Structures/AlteringForeachWithoutReference.rst
   Rules/Structures/AlternativeConsistenceByFile.rst
   Rules/Security/AnchorRegex.rst
   Rules/Structures/NeverNegative.rst
   Rules/Performances/Php74ArrayKeyExists.rst
   Rules/Arrays/AmbiguousKeys.rst
   Rules/Classes/AmbiguousStatic.rst
   Rules/Variables/AmbiguousTypes.rst
   Rules/Classes/AmbiguousVisibilities.rst
   Rules/Patterns/Factory.rst
   Rules/Exceptions/AnonymousCatch.rst
   Rules/Classes/Anonymous.rst
   Rules/Arrays/AppendAndAssignArrays.rst
   Rules/Php/Argon2Usage.rst
   Rules/Dump/ArgumentCountsPerCalls.rst
   Rules/Functions/ShouldBeTypehinted.rst
   Rules/Structures/ArrayAccessOnLiteralArray.rst
   Rules/Structures/ArrayAddition.rst
   Rules/Arrays/Arrayindex.rst
   Rules/Arrays/StringInitialization.rst
   Rules/Arrays/ArrayBracketConsistence.rst
   Rules/Structures/ArrayFillWithObjects.rst
   Rules/Structures/ArrayMapPassesByValue.rst
   Rules/Structures/ArrayMergeArrayArray.rst
   Rules/Php/AssertFunctionIsReserved.rst
   Rules/Php/AssertionUsage.rst
   Rules/Structures/AssigneAndCompare.rst
   Rules/Php/AssignAnd.rst
   Rules/Classes/MakeDefault.rst
   Rules/Structures/AssignedInOneBranch.rst
   Rules/Variables/AssignedTwiceOrMore.rst
   Rules/Php/Assumptions.rst
   Rules/Performances/Autoappend.rst
   Rules/Php/AutoloadUsage.rst
   Rules/Structures/DontCompareTypedBoolean.rst
   Rules/Performances/NoConcatInLoop.rst
   Rules/Structures/NoAssignationInFunction.rst
   Rules/Classes/AvoidOptionalProperties.rst
   Rules/Structures/PrintWithoutParenthesis.rst
   Rules/Php/AvoidReal.rst
   Rules/Interfaces/AvoidSelfInInterface.rst
   Rules/Structures/NoSubstrOne.rst
   Rules/Security/AvoidThoseCrypto.rst
   Rules/Php/UseStdclass.rst
   Rules/Performances/AvoidArrayPush.rst
   Rules/Structures/NoArrayUnique.rst
   Rules/Structures/UseInstanceof.rst
   Rules/Php/AvoidGetobjectVars.rst
   Rules/Performances/NoGlob.rst
   Rules/Php/AvoidMbDectectEncoding.rst
   Rules/Classes/AvoidOptionArrays.rst
   Rules/Php/AvoidSetErrorHandlerContextArg.rst
   Rules/Security/NoSleep.rst
   Rules/Constants/BadConstantnames.rst
   Rules/Functions/BadTypehintRelay.rst
   Rules/Structures/BailOutEarly.rst
   Rules/Type/Binary.rst
   Rules/Structures/BlindVariableUsedBeyondLoop.rst
   Rules/Variables/Blind.rst
   Rules/Structures/Bracketless.rst
   Rules/Structures/BreakOutsideLoop.rst
   Rules/Structures/Break0.rst
   Rules/Structures/BreakNonInteger.rst
   Rules/Structures/BuriedAssignation.rst
   Rules/Performances/CacheVariableOutsideLoop.rst
   Rules/Vendors/Cakephp.rst
   Rules/Dump/CallOrder.rst
   Rules/Functions/CallbackNeedsReturn.rst
   Rules/Php/CallingStaticTraitMethod.rst
   Rules/Structures/CalltimePassByReference.rst
   Rules/Functions/CanCallGenerator.rst
   Rules/Structures/CanCountNonCountable.rst
   Rules/Security/CantDisableClass.rst
   Rules/Security/CantDisableFunction.rst
   Rules/Classes/CantExtendFinal.rst
   Rules/Exceptions/CantThrow.rst
   Rules/Interfaces/CantImplementTraversable.rst
   Rules/Classes/CantInstantiateClass.rst
   Rules/Interfaces/CantOverloadConstants.rst
   Rules/Classes/CantOverwriteFinalConstant.rst
   Rules/Classes/CantOverwriteFinalMethod.rst
   Rules/Classes/CancelCommonMethod.rst
   Rules/Functions/CancelledParameter.rst
   Rules/Traits/CannotCallTraitMethod.rst
   Rules/Structures/CannotUseAppendForReading.rst
   Rules/Functions/CannotUseStaticForClosure.rst
   Rules/Classes/CantInheritAbstractMethod.rst
   Rules/Classes/CantInstantiateNonClass.rst
   Rules/Php/CantUseReturnValueInWriteContext.rst
   Rules/Constants/CaseInsensitiveConstants.rst
   Rules/Structures/CastToBoolean.rst
   Rules/Php/CastUnsetUsage.rst
   Rules/Php/CastingUsage.rst
   Rules/Structures/CastingTernary.rst
   Rules/Structures/CatchShadowsVariable.rst
   Rules/Exceptions/CatchUndefinedVariable.rst
   Rules/Exceptions/CaughtExceptions.rst
   Rules/Php/TryCatchUsage.rst
   Rules/Exceptions/CatchE.rst
   Rules/Classes/CheckAfterNullSafeOperator.rst
   Rules/Structures/CheckAllTypes.rst
   Rules/Security/CryptoKeyLength.rst
   Rules/Structures/CheckDivision.rst
   Rules/Structures/CheckJson.rst
   Rules/Classes/CheckOnCallUsage.rst
   Rules/Classes/ChecksPropertyExistence.rst
   Rules/Classes/ChildRemoveTypehint.rst
   Rules/Php/ClassConstWithArray.rst
   Rules/Classes/CouldBeFinal.rst
   Rules/Classes/CouldBeReadonly.rst
   Rules/Php/ClassFunctionConfusion.rst
   Rules/Classes/HasFluentInterface.rst
   Rules/Dump/ClassInjectionCount.rst
   Rules/Classes/ClassInvasion.rst
   Rules/Classes/ClassOverreach.rst
   Rules/Classes/FinalByOcramius.rst
   Rules/Classes/ClassUsage.rst
   Rules/Classes/NoParent.rst
   Rules/Classes/CitSameName.rst
   Rules/Functions/TypehintedReferences.rst
   Rules/Classes/MutualExtension.rst
   Rules/Classes/Classnames.rst
   Rules/Php/CloneConstant.rst
   Rules/Classes/CloningUsage.rst
   Rules/Classes/CloneWithNonObject.rst
   Rules/Php/CloseTagsConsistency.rst
   Rules/Php/CloseTags.rst
   Rules/Functions/Closure2String.rst
   Rules/Php/ClosureThisSupport.rst
   Rules/Functions/Closures.rst
   Rules/Php/Coalesce.rst
   Rules/Structures/CoalesceAndConcat.rst
   Rules/Structures/CoalesceNullCoalesce.rst
   Rules/Php/CoalesceEqual.rst
   Rules/Vendors/Codeigniter.rst
   Rules/Dump/CollectAtomCounts.rst
   Rules/Dump/CollectBlockSize.rst
   Rules/Dump/CollectCalls.rst
   Rules/Dump/CollectCatch.rst
   Rules/Dump/CollectClassChildren.rst
   Rules/Dump/CollectClassConstantCounts.rst
   Rules/Dump/CollectClassDepth.rst
   Rules/Dump/CollectClassInterfaceCounts.rst
   Rules/Dump/CollectClassTraitsCounts.rst
   Rules/Dump/CollectClassesDependencies.rst
   Rules/Dump/DumpComparedLiterals.rst
   Rules/Dump/CollectDefinitionsStats.rst
   Rules/Dump/CollectDependencyExtension.rst
   Rules/Dump/CollectFilesDependencies.rst
   Rules/Dump/CollectGlobalVariables.rst
   Rules/Dump/CollectGraphTriplets.rst
   Rules/Dump/CollectLiterals.rst
   Rules/Dump/CollectLocalVariableCounts.rst
   Rules/Dump/CollectMbstringEncodings.rst
   Rules/Dump/CollectMethodCounts.rst
   Rules/Dump/CollectMethodsThrowingExceptions.rst
   Rules/Dump/CollectNativeCallsPerExpressions.rst
   Rules/Dump/CollectParameterCounts.rst
   Rules/Dump/CollectParameterNames.rst
   Rules/Dump/CollectPhpStructures.rst
   Rules/Dump/CollectPropertyCounts.rst
   Rules/Dump/CollectPropertyUsage.rst
   Rules/Dump/CollectReadability.rst
   Rules/Dump/CollectSetLocale.rst
   Rules/Dump/CollectClassChanges.rst
   Rules/Dump/CollectStructures.rst
   Rules/Dump/CollectStubStructures.rst
   Rules/Dump/CollectThrow.rst
   Rules/Dump/CollectUseCounts.rst
   Rules/Dump/CollectVendorStructures.rst
   Rules/Dump/CollectsNames.rst
   Rules/Dump/CollectVariables.rst
   Rules/Dump/CombinedCalls.rst
   Rules/Structures/CommonAlternatives.rst
   Rules/Security/CompareHash.rst
   Rules/Structures/ComparedButNotAssignedStrings.rst
   Rules/Structures/ComparedComparison.rst
   Rules/Structures/AlwaysFalse.rst
   Rules/Php/ComparisonOnDifferentTypes.rst
   Rules/Structures/GtOrLtFavorite.rst
   Rules/Variables/ComplexDynamicNames.rst
   Rules/Composer/UseComposer.rst
   Rules/Composer/Autoload.rst
   Rules/Php/ConcatAndAddition.rst
   Rules/Structures/ConcatEmpty.rst
   Rules/Structures/ConcatenationInterpolationFavorite.rst
   Rules/Vendors/Concrete5.rst
   Rules/Structures/ConditionalStructures.rst
   Rules/Constants/ConditionedConstants.rst
   Rules/Functions/ConditionedFunctions.rst
   Rules/Security/ConfigureExtract.rst
   Rules/Variables/CloseNaming.rst
   Rules/Structures/ConstDefineFavorite.rst
   Rules/Constants/ConstDefinePreference.rst
   Rules/Classes/ConstVisibilityUsage.rst
   Rules/Php/ConstWithArray.rst
   Rules/Namespaces/ConstantWithUseFavorite.rst
   Rules/Constants/DefineInsensitivePreference.rst
   Rules/Classes/ConstantClass.rst
   Rules/Structures/ConstantComparisonConsistance.rst
   Rules/Structures/ConstantConditions.rst
   Rules/Classes/ConstantDefinition.rst
   Rules/Constants/DynamicCreation.rst
   Rules/Dump/ConstantOrder.rst
   Rules/Php/ConstantScalarExpression.rst
   Rules/Structures/ConstantScalarExpression.rst
   Rules/Variables/ConstantTypo.rst
   Rules/Classes/ConstantUsedBelow.rst
   Rules/Constants/ConstantUsedOnce.rst
   Rules/Constants/CreatedOutsideItsNamespace.rst
   Rules/Traits/ConstantsInTraits.rst
   Rules/Constants/Constantnames.rst
   Rules/Constants/ConstantUsage.rst
   Rules/Constants/ConstantStrangeNames.rst
   Rules/Classes/Constructor.rst
   Rules/Type/Continents.rst
   Rules/Structures/ContinueIsForLoop.rst
   Rules/Exceptions/ConvertedExceptions.rst
   Rules/Php/CookiesVariables.rst
   Rules/Dump/CouldBeAConstant.rst
   Rules/Structures/CouldBeStatic.rst
   Rules/Classes/CouldBeAbstractClass.rst
   Rules/Classes/CouldBeAbstractMethod.rst
   Rules/Typehints/CouldBeArray.rst
   Rules/Typehints/CouldBeBoolean.rst
   Rules/Typehints/CouldBeCIT.rst
   Rules/Typehints/CouldBeCallable.rst
   Rules/Classes/CouldBeClassConstant.rst
   Rules/Constants/CouldBeConstant.rst
   Rules/Structures/CouldBeElse.rst
   Rules/Enums/CouldBeEnum.rst
   Rules/Typehints/CouldBeFloat.rst
   Rules/Typehints/CouldBeGenerator.rst
   Rules/Typehints/CouldBeNull.rst
   Rules/Typehints/CouldBeParent.rst
   Rules/Classes/CouldBeParentMethod.rst
   Rules/Classes/CouldBePrivateConstante.rst
   Rules/Classes/CouldBeProtectedConstant.rst
   Rules/Classes/CouldBeProtectedMethod.rst
   Rules/Classes/CouldBeProtectedProperty.rst
   Rules/Classes/CouldBeReadonlyProperty.rst
   Rules/Typehints/CouldBeSelf.rst
   Rules/Structures/CouldBeSpaceship.rst
   Rules/Functions/CouldBeStaticClosure.rst
   Rules/Typehints/CouldBeString.rst
   Rules/Classes/CouldBeStringable.rst
   Rules/Structures/CouldBeTernary.rst
   Rules/Typehints/CouldBeType.rst
   Rules/Functions/CouldBeCallable.rst
   Rules/Typehints/CouldBeVoid.rst
   Rules/Structures/CouldBeArrayCombine.rst
   Rules/Structures/CouldCastToArray.rst
   Rules/Exceptions/CouldDropVariable.rst
   Rules/Classes/CouldInjectParam.rst
   Rules/Functions/CouldCentralize.rst
   Rules/Structures/MergeTernaryIntoIfthen.rst
   Rules/Typehints/CouldNotType.rst
   Rules/Classes/CouldSetPropertyDefault.rst
   Rules/Functions/CouldTypehint.rst
   Rules/Functions/CouldTypeWithArray.rst
   Rules/Functions/CouldTypeWithBool.rst
   Rules/Functions/CouldTypeWithInt.rst
   Rules/Functions/CouldTypeWithIterable.rst
   Rules/Functions/CouldTypeWithString.rst
   Rules/Namespaces/CouldUseAlias.rst
   Rules/Classes/CouldUseClassOperator.rst
   Rules/Structures/CouldUseCompact.rst
   Rules/Constants/CouldUseConstant.rst
   Rules/Structures/CouldUseMatch.rst
   Rules/Namespaces/CouldUseMagicConstant.rst
   Rules/Structures/CouldUseNullableOperator.rst
   Rules/Php/CouldUsePromotedProperties.rst
   Rules/Structures/CouldUseShortAssignation.rst
   Rules/Traits/CouldUseTrait.rst
   Rules/Exceptions/CouldUseTry.rst
   Rules/Structures/CouldUseYieldFrom.rst
   Rules/Structures/CouldUseDir.rst
   Rules/Structures/CouldUseArrayFillKeys.rst
   Rules/Structures/CouldUseArraySum.rst
   Rules/Structures/CouldUseArrayUnique.rst
   Rules/Classes/ShouldUseSelf.rst
   Rules/Structures/CouldUseStrrepeat.rst
   Rules/Structures/CouldUseStrContains.rst
   Rules/Structures/CountIsNotNegative.rst
   Rules/Performances/CountToAppend.rst
   Rules/Patterns/CourrierAntiPattern.rst
   Rules/Php/Crc32MightBeNegative.rst
   Rules/Complete/CreateCompactVariables.rst
   Rules/Complete/CreateDefaultValues.rst
   Rules/Complete/CreateForeachDefault.rst
   Rules/Complete/CreateMagicMethod.rst
   Rules/Complete/CreateMagicProperty.rst
   Rules/Php/CryptoUsage.rst
   Rules/Php/NoMoreCurlyArrays.rst
   Rules/Classes/AvoidUsing.rst
   Rules/Constants/CustomConstantUsage.rst
   Rules/Classes/CyclicReferences.rst
   Rules/Dump/CyclomaticComplexity.rst
   Rules/Classes/TypehintCyclicDependencies.rst
   Rules/Structures/DanglingArrayReferences.rst
   Rules/Php/DateFormats.rst
   Rules/Php/DateTimeNotImmutable.rst
   Rules/Structures/VariableMayBeNonGlobal.rst
   Rules/Structures/DeclareStaticOnce.rst
   Rules/Php/DeclareStrictType.rst
   Rules/Functions/DeepDefinitions.rst
   Rules/Structures/DefaultThenDiscard.rst
   Rules/Php/DefineWithArray.rst
   Rules/Classes/DefinedConstants.rst
   Rules/Exceptions/DefinedExceptions.rst
   Rules/Classes/DefinedParentMP.rst
   Rules/Classes/DefinedProperty.rst
   Rules/Classes/DefinedStaticMP.rst
   Rules/Files/DefinitionsOnly.rst
   Rules/Classes/DependantAbstractClass.rst
   Rules/Traits/DependantTrait.rst
   Rules/Patterns/DependencyInjection.rst
   Rules/Attributes/Deprecated.rst
   Rules/Functions/DeprecatedCallable.rst
   Rules/Structures/DeprecatedMbEncoding.rst
   Rules/Php/Deprecated.rst
   Rules/Dump/DereferencingLevels.rst
   Rules/Structures/DereferencingAS.rst
   Rules/Php/DetectCurrentClass.rst
   Rules/Structures/DieExitConsistance.rst
   Rules/Structures/DifferencePreference.rst
   Rules/Classes/DifferentArgumentCounts.rst
   Rules/Classes/IncompatibleConstructor.rst
   Rules/Php/DirectCallToClone.rst
   Rules/Security/DirectInjection.rst
   Rules/Php/DirectivesUsage.rst
   Rules/Structures/DirectlyUseFile.rst
   Rules/Classes/DisconnectedClasses.rst
   Rules/Php/Prints.rst
   Rules/Php/DlUsage.rst
   Rules/Performances/DoInBase.rst
   Rules/Php/NoCastToInt.rst
   Rules/Php/DeprecateDollarCurly.rst
   Rules/Structures/DontAddSeconds.rst
   Rules/Structures/DontBeTooManual.rst
   Rules/Structures/NoChangeIncomingVariables.rst
   Rules/Structures/DontChangeBlindKey.rst
   Rules/Functions/DontUseVoid.rst
   Rules/Security/DontEchoError.rst
   Rules/Structures/DontLoopOnYield.rst
   Rules/Structures/DontMixPlusPlus.rst
   Rules/Php/DontPolluteGlobalSpace.rst
   Rules/Structures/DontReadAndWriteInOneExpression.rst
   Rules/Structures/DontReuseForeachSource.rst
   Rules/Classes/DontSendThisInConstructor.rst
   Rules/Classes/DontUnsetProperties.rst
   Rules/Structures/DontUseTheTypeAsVariable.rst
   Rules/Structures/DoubleAssignation.rst
   Rules/Structures/DoubleChecks.rst
   Rules/Structures/DoubleInstruction.rst
   Rules/Structures/DoubleObjectAssignation.rst
   Rules/Performances/DoubleArrayFlip.rst
   Rules/Structures/DropElseAfterReturn.rst
   Rules/Structures/SubstrLastArg.rst
   Rules/Vendors/Drupal.rst
   Rules/Structures/DuplicateCalls.rst
   Rules/Enums/DuplicateCaseValue.rst
   Rules/Type/DuplicateLiteral.rst
   Rules/Functions/DuplicateNamedParameter.rst
   Rules/Structures/DynamicCalls.rst
   Rules/Classes/DynamicConstantCall.rst
   Rules/Classes/DynamicClass.rst
   Rules/Structures/DynamicCode.rst
   Rules/Functions/Dynamiccall.rst
   Rules/Security/DynamicDl.rst
   Rules/Classes/DynamicMethodCall.rst
   Rules/Classes/DynamicNew.rst
   Rules/Classes/DynamicPropertyCall.rst
   Rules/Classes/DynamicSelfCalls.rst
   Rules/Classes/VariableClasses.rst
   Rules/Structures/EchoPrintConsistance.rst
   Rules/Structures/EchoWithConcat.rst
   Rules/Performances/EllipsisMerge.rst
   Rules/Php/EllipsisUsage.rst
   Rules/Structures/ElseIfElseif.rst
   Rules/Structures/ElseUsage.rst
   Rules/Type/Email.rst
   Rules/Structures/ArrayCountTripleEqual.rst
   Rules/Structures/EmptyBlocks.rst
   Rules/Classes/EmptyClass.rst
   Rules/Arrays/EmptyFinal.rst
   Rules/Functions/EmptyFunction.rst
   Rules/Structures/EmptyLines.rst
   Rules/Interfaces/EmptyInterface.rst
   Rules/Structures/EmptyJsonError.rst
   Rules/Php/EmptyList.rst
   Rules/Structures/EmptyLoop.rst
   Rules/Namespaces/EmptyNamespace.rst
   Rules/Arrays/EmptySlots.rst
   Rules/Traits/EmptyTrait.rst
   Rules/Structures/EmptyTryCatch.rst
   Rules/Structures/EmptyWithExpression.rst
   Rules/Security/EncodedLetters.rst
   Rules/Php/DeclareEncoding.rst
   Rules/Complete/EnumCaseValues.rst
   Rules/Php/EnumUsage.rst
   Rules/Dump/EnvironnementVariables.rst
   Rules/Dump/EnvironmentVariables.rst
   Rules/Variables/UncommonEnvVar.rst
   Rules/Structures/ErrorMessages.rst
   Rules/Php/ErrorLogUsage.rst
   Rules/Structures/EvalUsage.rst
   Rules/Functions/ExceedingTypehint.rst
   Rules/Exceptions/AlreadyCaught.rst
   Rules/Extensions/Extexcimer.rst
   Rules/Php/ExitNoArg.rst
   Rules/Structures/ExitUsage.rst
   Rules/Functions/KillsApp.rst
   Rules/Php/ExponentUsage.rst
   Rules/Complete/ExtendedTypehints.rst
   Rules/Classes/ExtendsStdclass.rst
   Rules/Extensions/Extyar.rst
   Rules/Extensions/Exttaint.rst
   Rules/Files/Services.rst
   Rules/Structures/FailingSubstrComparison.rst
   Rules/Php/FailingAnalysis.rst
   Rules/Functions/FallbackFunction.rst
   Rules/Php/FalseToArray.rst
   Rules/Structures/CastFavorite.rst
   Rules/Vendors/Feast.rst
   Rules/Performances/FetchOneRowFormat.rst
   Rules/Files/IsComponent.rst
   Rules/Files/NotDefinitionsOnly.rst
   Rules/Structures/FileUploadUsage.rst
   Rules/Structures/FileUsage.rst
   Rules/Structures/FilePutContentsDataType.rst
   Rules/Security/FilterNotRaw.rst
   Rules/Php/FilterToAddSlashes.rst
   Rules/Classes/Finalclass.rst
   Rules/Php/FinalConstant.rst
   Rules/Classes/Finalmethod.rst
   Rules/Classes/FinalPrivate.rst
   Rules/Traits/FinalTraitsAreFinal.rst
   Rules/Structures/GoToKeyDirectly.rst
   Rules/Php/FirstClassCallable.rst
   Rules/Php/FlexibleHeredoc.rst
   Rules/Arrays/FloatConversionAsIndex.rst
   Rules/Functions/FnArgumentVariableConfusion.rst
   Rules/Complete/FollowClosureDefinition.rst
   Rules/Portability/FopenMode.rst
   Rules/Structures/ForWithFunctioncall.rst
   Rules/Php/ForeachDontChangePointer.rst
   Rules/Structures/ForeachNeedReferencedSource.rst
   Rules/Php/ForeachObject.rst
   Rules/Structures/ForeachReferenceIsNotModified.rst
   Rules/Structures/ForeachWithList.rst
   Rules/Dump/CollectForeachFavorite.rst
   Rules/Interfaces/CouldUseInterface.rst
   Rules/Exceptions/ForgottenThrown.rst
   Rules/Classes/NonPpp.rst
   Rules/Structures/ForgottenWhiteSpace.rst
   Rules/Classes/FossilizedMethod.rst
   Rules/Dump/FossilizedMethods.rst
   Rules/Attributes/Friend.rst
   Rules/Vendors/Fuel.rst
   Rules/Namespaces/ConstantFullyQualified.rst
   Rules/Functions/FunctionCalledWithOtherCase.rst
   Rules/Structures/FunctionSubscripting.rst
   Rules/Structures/FunctionPreSubscripting.rst
   Rules/Functions/DynamicCode.rst
   Rules/Functions/IsGlobal.rst
   Rules/Functions/Functionnames.rst
   Rules/Functions/LoopCalling.rst
   Rules/Php/Php54RemovedFunctions.rst
   Rules/Php/Php55RemovedFunctions.rst
   Rules/Functions/FunctionsUsingReference.rst
   Rules/Portability/GlobBraceUsage.rst
   Rules/Security/GPRAliases.rst
   Rules/Functions/GeneratorCannotReturn.rst
   Rules/Extensions/Extgeospatial.rst
   Rules/Patterns/GetterSetter.rst
   Rules/Arrays/GettingLastElement.rst
   Rules/Files/GlobalCodeOnly.rst
   Rules/Complete/GlobalDefinitions.rst
   Rules/Namespaces/GlobalImport.rst
   Rules/Structures/GlobalInGlobal.rst
   Rules/Structures/GlobalOutsideLoop.rst
   Rules/Structures/GlobalUsage.rst
   Rules/Variables/Globals.rst
   Rules/Php/Gotonames.rst
   Rules/Php/GroupUseDeclaration.rst
   Rules/Php/GroupUseTrailingComma.rst
   Rules/Type/HttpStatus.rst
   Rules/Arrays/WithCallback.rst
   Rules/Functions/HardcodedPasswords.rst
   Rules/Classes/HasMagicProperty.rst
   Rules/Php/HasPropertyHook.rst
   Rules/Functions/VariableArguments.rst
   Rules/Php/HasVirtualProperty.rst
   Rules/Php/HashAlgos.rst
   Rules/Php/HashAlgos53.rst
   Rules/Php/HashAlgos54.rst
   Rules/Php/HashAlgos71.rst
   Rules/Php/HashAlgos74.rst
   Rules/Php/HashUsesObjects.rst
   Rules/Structures/HeredocDelimiterFavorite.rst
   Rules/Type/Heredoc.rst
   Rules/Type/Hexadecimal.rst
   Rules/Type/HexadecimalString.rst
   Rules/Namespaces/HiddenUse.rst
   Rules/Structures/Htmlentitiescall.rst
   Rules/Structures/HtmlentitiescallDefaultFlag.rst
   Rules/Type/HttpHeader.rst
   Rules/Extensions/Extice.rst
   Rules/Portability/IconvTranslit.rst
   Rules/Structures/IdenticalCase.rst
   Rules/Structures/IdenticalConditions.rst
   Rules/Structures/IdenticalConsecutive.rst
   Rules/Structures/IdenticalElseif.rst
   Rules/Classes/IdenticalMethods.rst
   Rules/Structures/IdenticalOnBothSides.rst
   Rules/Structures/IdenticalVariablesInForeach.rst
   Rules/Functions/Identity.rst
   Rules/Structures/IfThenReturnFavorite.rst
   Rules/Structures/IfWithSameConditions.rst
   Rules/Structures/Iffectation.rst
   Rules/Classes/WrongName.rst
   Rules/Classes/ImmutableSignature.rst
   Rules/Classes/ImplementedMethodsArePublic.rst
   Rules/Classes/ImplementIsForInterface.rst
   Rules/Structures/ImplicitConversionToInt.rst
   Rules/Structures/ImplicitGlobal.rst
   Rules/Classes/HiddenNullable.rst
   Rules/Structures/ImpliedIf.rst
   Rules/Php/ImplodeOneArg.rst
   Rules/Structures/ImplodeArgsOrder.rst
   Rules/Php/IncludeVariables.rst
   Rules/Dump/Inclusions.rst
   Rules/Structures/IncludeUsage.rst
   Rules/Type/IncomingDateFormat.rst
   Rules/Php/IncomingValues.rst
   Rules/Type/GPCIndex.rst
   Rules/Php/IncomingVariables.rst
   Rules/Traits/IncompatibleProperty.rst
   Rules/Classes/IncompatibleSignature.rst
   Rules/Classes/IncompatibleSignature74.rst
   Rules/Security/IncompatibleTypesWithIncoming.rst
   Rules/Php/Incompilable.rst
   Rules/Structures/InconsistentConcatenation.rst
   Rules/Structures/InconsistentElseif.rst
   Rules/Variables/InconsistentUsage.rst
   Rules/Dump/IndentationLevels.rst
   Rules/Structures/IndicesAreIntOrString.rst
   Rules/Security/IndirectInjection.rst
   Rules/Structures/InfiniteRecursion.rst
   Rules/Interfaces/InheritedClassConstantVisibility.rst
   Rules/Classes/InheritedPropertyMustMatch.rst
   Rules/Variables/InheritedStaticVariable.rst
   Rules/Structures/InitThenIf.rst
   Rules/Attributes/InjectableVersion.rst
   Rules/Security/IntegerConversion.rst
   Rules/Classes/InstantiatingAbstractClass.rst
   Rules/Classes/InsufficientPropertyTypehint.rst
   Rules/Functions/InsufficientTypehint.rst
   Rules/Classes/IntegerAsProperty.rst
   Rules/Variables/InterfaceArguments.rst
   Rules/Interfaces/InterfaceMethod.rst
   Rules/Interfaces/NoGaranteeForPropertyConstant.rst
   Rules/Interfaces/IsNotImplemented.rst
   Rules/Interfaces/Interfacenames.rst
   Rules/Interfaces/InterfaceUsage.rst
   Rules/Classes/PropertyUsedInternally.rst
   Rules/Type/UdpDomains.rst
   Rules/Type/Ports.rst
   Rules/Type/StringInterpolation.rst
   Rules/Php/Php81IntersectionTypehint.rst
   Rules/Structures/InvalidCast.rst
   Rules/Constants/InvalidName.rst
   Rules/Structures/InvalidDateScanningFormat.rst
   Rules/Type/OctalInString.rst
   Rules/Structures/InvalidPackFormat.rst
   Rules/Structures/InvalidRegex.rst
   Rules/Type/Ip.rst
   Rules/Classes/IsaMagicProperty.rst
   Rules/Structures/IsZero.rst
   Rules/Classes/IsExtClass.rst
   Rules/Constants/IsExtConstant.rst
   Rules/Functions/IsExtFunction.rst
   Rules/Interfaces/IsExtInterface.rst
   Rules/Files/IsCliScript.rst
   Rules/Complete/IsExtStructure.rst
   Rules/Traits/IsExtTrait.rst
   Rules/Constants/IsGlobalConstant.rst
   Rules/Classes/IsInterfaceMethod.rst
   Rules/Project/IsLibrary.rst
   Rules/Classes/IsNotFamily.rst
   Rules/Constants/IsPhpConstant.rst
   Rules/Complete/IsPhpStructure.rst
   Rules/Complete/IsStubStructure.rst
   Rules/Classes/IsUpperFamily.rst
   Rules/Php/IsAWithString.rst
   Rules/Php/IssetMultipleArgs.rst
   Rules/Performances/IssetWholeArray.rst
   Rules/Performances/JoinFile.rst
   Rules/Vendors/Joomla.rst
   Rules/Structures/JsonEncodeExceptions.rst
   Rules/Security/KeepFilesRestricted.rst
   Rules/Php/Labelnames.rst
   Rules/Vendors/Laravel.rst
   Rules/Exceptions/LargeTryBlock.rst
   Rules/Classes/DemeterLaw.rst
   Rules/Dump/ParameterArgumentsLinks.rst
   Rules/Portability/LinuxOnlyFiles.rst
   Rules/Php/ListShortSyntax.rst
   Rules/Php/ListWithAppends.rst
   Rules/Php/ListWithKeys.rst
   Rules/Php/ListWithReference.rst
   Rules/Variables/LocalGlobals.rst
   Rules/Classes/LocallyUnusedProperty.rst
   Rules/Classes/LocallyUsedProperty.rst
   Rules/Traits/LocallyUsedProperty.rst
   Rules/Structures/LogicalMistakes.rst
   Rules/Php/LetterCharsLogicalFavorite.rst
   Rules/Php/LogicalInLetters.rst
   Rules/Performances/LogicalToInArray.rst
   Rules/Structures/LoneBlock.rst
   Rules/Structures/LongArguments.rst
   Rules/Exceptions/LongPreparation.rst
   Rules/Variables/LostReferences.rst
   Rules/Classes/LoweredAccessLevel.rst
   Rules/Constants/MagicConstantUsage.rst
   Rules/Classes/MagicMethodReturntypes.rst
   Rules/Classes/MagicMethod.rst
   Rules/Classes/MagicProperties.rst
   Rules/Classes/toStringPss.rst
   Rules/Structures/MailUsage.rst
   Rules/Complete/MakeAllStatics.rst
   Rules/Complete/MakeClassMethodDefinition.rst
   Rules/Complete/MakeFunctioncallWithReference.rst
   Rules/Classes/MakeGlobalAProperty.rst
   Rules/Classes/MakeMagicConcrete.rst
   Rules/Performances/MakeOneCall.rst
   Rules/Complete/MakeClassConstantDefinition.rst
   Rules/Type/MalformedOctal.rst
   Rules/Php/IsINF.rst
   Rules/Php/IsNAN.rst
   Rules/Arrays/MassCreation.rst
   Rules/Structures/MaxLevelOfIdentation.rst
   Rules/Structures/MissingNew.rst
   Rules/Structures/MbstringThirdArg.rst
   Rules/Structures/MbstringUnknownEncoding.rst
   Rules/Structures/MbStringNonEncodings.rst
   Rules/Type/Md5String.rst
   Rules/Performances/MemoizeMagicCall.rst
   Rules/Structures/MergeIfThen.rst
   Rules/Traits/MethodCollisionTraits.rst
   Rules/Classes/CouldBePrivateMethod.rst
   Rules/Classes/CouldBeStatic.rst
   Rules/Functions/HasFluentInterface.rst
   Rules/Functions/IsGenerator.rst
   Rules/Functions/MethodIsNotAnIf.rst
   Rules/Functions/HasNotFluentInterface.rst
   Rules/Classes/MethodIsOverwritten.rst
   Rules/Classes/MethodPropertyConfusion.rst
   Rules/Classes/MethodSignatureMustBeCompatible.rst
   Rules/Custom/MethodUsage.rst
   Rules/Classes/MethodUsedBelow.rst
   Rules/Php/MethodCallOnNew.rst
   Rules/Functions/CantUse.rst
   Rules/Functions/WithoutReturn.rst
   Rules/Type/MimeType.rst
   Rules/Security/MinusOneOnError.rst
   Rules/Functions/MismatchParameterAndType.rst
   Rules/Functions/MismatchParameterName.rst
   Rules/Classes/MismatchProperties.rst
   Rules/Functions/MismatchTypeAndDefault.rst
   Rules/Functions/MismatchedDefaultArguments.rst
   Rules/Structures/MismatchedTernary.rst
   Rules/Functions/MismatchedTypehint.rst
   Rules/Classes/MissingAbstractMethod.rst
   Rules/Structures/MissingAssignation.rst
   Rules/Attributes/MissingAttributeAttribute.rst
   Rules/Structures/MissingCases.rst
   Rules/Files/MissingInclude.rst
   Rules/Attributes/MissingOverrideMethod.rst
   Rules/Structures/MissingParenthesis.rst
   Rules/Typehints/MissingReturntype.rst
   Rules/Functions/MissingTypehint.rst
   Rules/Typehints/MissingTypehints.rst
   Rules/Classes/MissingVisibility.rst
   Rules/Php/MissingMagicIsset.rst
   Rules/Arrays/MistakenConcatenation.rst
   Rules/Structures/MisusedYield.rst
   Rules/Structures/MixedConcatInterpolation.rst
   Rules/Arrays/MixedKeys.rst
   Rules/Php/MixedUsage.rst
   Rules/Security/MkdirDefault.rst
   Rules/Structures/ModernEmpty.rst
   Rules/Functions/ModifyTypedParameter.rst
   Rules/Attributes/ModifyImmutable.rst
   Rules/Structures/strOrMbFavorite.rst
   Rules/Structures/OneLevelOfIndentation.rst
   Rules/Arrays/Multidimensional.rst
   Rules/Structures/MultilineExpressions.rst
   Rules/Namespaces/MultipleAliasDefinitions.rst
   Rules/Namespaces/MultipleAliasDefinitionPerFile.rst
   Rules/Structures/MultipleCatch.rst
   Rules/Classes/MultipleDeclarations.rst
   Rules/Classes/MultipleClassesInFile.rst
   Rules/Constants/MultipleConstantDefinition.rst
   Rules/Php/MultipleDeclareStrict.rst
   Rules/Functions/MultipleSameArguments.rst
   Rules/Exceptions/MultipleCatch.rst
   Rules/Functions/MultipleDeclarations.rst
   Rules/Functions/MultipleIdenticalClosure.rst
   Rules/Classes/MultipleTraitOrInterface.rst
   Rules/Arrays/MultipleIdenticalKeys.rst
   Rules/Classes/MultiplePropertyDeclaration.rst
   Rules/Classes/MultiplePropertyDeclarationOnOneLine.rst
   Rules/Functions/MultipleReturn.rst
   Rules/Structures/MultipleSimilarCalls.rst
   Rules/Structures/MultipleTypeCasesInSwitch.rst
   Rules/Structures/MultipleTypeVariable.rst
   Rules/Structures/MultipleUnset.rst
   Rules/Traits/MultipleUsage.rst
   Rules/Structures/MultipleDefinedCase.rst
   Rules/Structures/MultiplyByOne.rst
   Rules/Php/MustCallParentConstructor.rst
   Rules/Functions/MustReturn.rst
   Rules/Attributes/MustUseReturnReturns.rst
   Rules/Attributes/MustUseResult.rst
   Rules/Php/NamedArgumentAndVariadic.rst
   Rules/Php/NamedParameterUsage.rst
   Rules/Structures/NamedRegex.rst
   Rules/Namespaces/NamespaceUsage.rst
   Rules/Namespaces/Namespacesnames.rst
   Rules/Functions/AliasesUsage.rst
   Rules/Structures/NegativePow.rst
   Rules/Arrays/NegativeStart.rst
   Rules/Vendors/Neos.rst
   Rules/Attributes/NestedAttributes.rst
   Rules/Structures/NestedIfthen.rst
   Rules/Structures/NestedLoops.rst
   Rules/Structures/NestedMatch.rst
   Rules/Structures/NestedTernary.rst
   Rules/Php/NestedTernaryWithoutParenthesis.rst
   Rules/Functions/NeverUsedParameter.rst
   Rules/Php/NeverKeyword.rst
   Rules/Php/NeverTypehintUsage.rst
   Rules/Classes/PropertyNeverUsed.rst
   Rules/Php/Php72NewConstants.rst
   Rules/Php/Php74NewConstants.rst
   Rules/Classes/NewDynamicConstantSyntax.rst
   Rules/Php/Php54NewFunctions.rst
   Rules/Php/Php55NewFunctions.rst
   Rules/Php/Php56NewFunctions.rst
   Rules/Php/Php70NewFunctions.rst
   Rules/Php/Php71NewFunctions.rst
   Rules/Php/Php72NewFunctions.rst
   Rules/Php/Php73NewFunctions.rst
   Rules/Php/Php74NewFunctions.rst
   Rules/Php/Php80NewFunctions.rst
   Rules/Php/Php81NewFunctions.rst
   Rules/Php/Php82NewFunctions.rst
   Rules/Php/Php83NewFunctions.rst
   Rules/Php/Php84NewFunctions.rst
   Rules/Php/NewInitializers.rst
   Rules/Structures/NewLineStyle.rst
   Rules/Classes/NewThenCall.rst
   Rules/Classes/NewOnFunctioncallOrIdentifier.rst
   Rules/Dump/NewOrder.rst
   Rules/Structures/NextMonthTrap.rst
   Rules/Structures/NoValidCast.rst
   Rules/Structures/NoAppendOnSource.rst
   Rules/Functions/NoBooleanAsDefault.rst
   Rules/Structures/NoChoice.rst
   Rules/Functions/NoClassAsTypehint.rst
   Rules/Php/NoClassInGlobal.rst
   Rules/Interfaces/NoConstructorInInterface.rst
   Rules/Performances/NotCountNull.rst
   Rules/Functions/NoDefaultForReference.rst
   Rules/Structures/NoDirectAccess.rst
   Rules/Classes/DirectCallToMagicMethod.rst
   Rules/Structures/NoDirectUsage.rst
   Rules/Security/NoEntIgnore.rst
   Rules/Structures/NoEmptyRegex.rst
   Rules/Structures/NoEmptyStringWithExplode.rst
   Rules/Structures/NoHardcodedHash.rst
   Rules/Structures/NoHardcodedIp.rst
   Rules/Structures/NoHardcodedPath.rst
   Rules/Structures/NoHardcodedPort.rst
   Rules/Variables/NoInitialS.rst
   Rules/Namespaces/NoKeywordInNamespace.rst
   Rules/Php/NoListWithString.rst
   Rules/Functions/NoLiteralForReference.rst
   Rules/Enums/NoMagicMethod.rst
   Rules/Classes/NoMagicWithArray.rst
   Rules/Structures/NoMaxOnEmptyArray.rst
   Rules/Attributes/NoNamedArguments.rst
   Rules/Structures/NoNeedForElse.rst
   Rules/Structures/NoNeedForTriple.rst
   Rules/Structures/NoNeedGetClass.rst
   Rules/Security/NoNetForXmlLoad.rst
   Rules/Structures/NoNullForIndex.rst
   Rules/Php/NoNullForNative.rst
   Rules/Classes/NoNullWithNullSafeOperator.rst
   Rules/Structures/NoObjectAsIndex.rst
   Rules/Structures/NoParenthesisForLanguageConstruct.rst
   Rules/Structures/PlusEgalOne.rst
   Rules/Traits/NoPrivateAbstract.rst
   Rules/Classes/NoPublicAccess.rst
   Rules/Classes/NoReadonlyAssignationInGlobal.rst
   Rules/Type/NoRealComparison.rst
   Rules/Php/NoReferenceForStaticProperty.rst
   Rules/Php/NoReferenceForTernary.rst
   Rules/Structures/NoReferenceOnLeft.rst
   Rules/Functions/NoReferencedVoid.rst
   Rules/Php/NoReturnForGenerator.rst
   Rules/Structures/NoReturnInFinally.rst
   Rules/Functions/NoReturnUsed.rst
   Rules/Classes/NoSelfReferencingConstant.rst
   Rules/Arrays/NoSpreadForHash.rst
   Rules/Variables/NoStaticVarInMethod.rst
   Rules/Php/NoStringWithAppend.rst
   Rules/Php/NoSubstrMinusOne.rst
   Rules/Variables/NoVariableNeeded.rst
   Rules/Security/NoWeakSSLCrypto.rst
   Rules/Performances/ArrayMergeInLoops.rst
   Rules/Structures/NoGetClassNull.rst
   Rules/Structures/NoIssetWithEmpty.rst
   Rules/Performances/MbStringInLoop.rst
   Rules/Variables/VariableNonascii.rst
   Rules/Structures/NonBreakableSpaceInNames.rst
   Rules/Structures/NonIntStringAsIndex.rst
   Rules/Classes/NonNullableSetters.rst
   Rules/Classes/NonStaticMethodsCalledStatic.rst
   Rules/Arrays/NonConstantArray.rst
   Rules/Php/UpperCaseKeyword.rst
   Rules/Php/CompactInexistant.rst
   Rules/Classes/NormalMethods.rst
   Rules/Php/NotScalarType.rst
   Rules/Structures/NotEqual.rst
   Rules/Structures/NotNot.rst
   Rules/Structures/NotOrNot.rst
   Rules/Classes/SameNameAsFile.rst
   Rules/Type/Nowdoc.rst
   Rules/Classes/NullOnNew.rst
   Rules/Arrays/NullBoolean.rst
   Rules/Functions/NullTypeFavorite.rst
   Rules/Functions/NullableWithoutCheck.rst
   Rules/Php/IntegerSeparatorUsage.rst
   Rules/Structures/ObjectReferences.rst
   Rules/Type/Octal.rst
   Rules/Classes/OldStyleConstructor.rst
   Rules/Php/oldAutoloadUsage.rst
   Rules/Structures/OneDotOrObjectOperatorPerLine.rst
   Rules/Structures/OneExpressionBracketsConsistency.rst
   Rules/Structures/OneIfIsSufficient.rst
   Rules/Functions/OneLetterFunctions.rst
   Rules/Classes/OneObjectOperatorPerLine.rst
   Rules/Type/OneVariableStrings.rst
   Rules/Structures/OnlyFirstByte.rst
   Rules/Classes/OnlyStaticMethods.rst
   Rules/Functions/OnlyVariableForReference.rst
   Rules/Functions/OnlyVariablePassedByReference.rst
   Rules/Php/OnlyVariablePassedByReference.rst
   Rules/Structures/OnlyVariableReturnedByReference.rst
   Rules/Type/OpensslCipher.rst
   Rules/Php/OpensslEncryptAlgoChange.rst
   Rules/Performances/OptimizeExplode.rst
   Rules/Functions/OptionalParameter.rst
   Rules/Structures/OrDie.rst
   Rules/Classes/OrderOfDeclaration.rst
   Rules/Namespaces/OverloadExistingNames.rst
   Rules/Attributes/Override.rst
   Rules/Variables/Overwriting.rst
   Rules/Classes/OverwrittenConst.rst
   Rules/Complete/OverwrittenConstants.rst
   Rules/Exceptions/OverwriteException.rst
   Rules/Structures/OverwrittenForeachVar.rst
   Rules/Variables/OverwrittenLiterals.rst
   Rules/Complete/OverwrittenMethods.rst
   Rules/Complete/OverwrittenProperties.rst
   Rules/Structures/ForeachSourceValue.rst
   Rules/Php/Php70NewClasses.rst
   Rules/Php/Php70NewInterfaces.rst
   Rules/Php/Php70RemovedDirective.rst
   Rules/Php/Php70RemovedFunctions.rst
   Rules/Php/PHP70scalartypehints.rst
   Rules/Php/Php71microseconds.rst
   Rules/Php/Php71RemovedDirective.rst
   Rules/Php/PHP71scalartypehints.rst
   Rules/Php/Php72Deprecation.rst
   Rules/Php/Php72ObjectKeyword.rst
   Rules/Php/Php72RemovedFunctions.rst
   Rules/Php/PHP72scalartypehints.rst
   Rules/Php/PHP73LastEmptyArgument.rst
   Rules/Php/Php73RemovedFunctions.rst
   Rules/Php/Php74Deprecation.rst
   Rules/Php/Php74RemovedDirective.rst
   Rules/Php/Php74RemovedFunctions.rst
   Rules/Php/Php74ReservedKeyword.rst
   Rules/Php/Php74NewDirective.rst
   Rules/Php/Php80RemovedConstant.rst
   Rules/Php/Php80RemovedDirective.rst
   Rules/Php/Php80RemovedFunctions.rst
   Rules/Php/Php80RemovesResources.rst
   Rules/Php/PHP80scalartypehints.rst
   Rules/Php/Php81NewTypes.rst
   Rules/Php/Php81RemovedConstant.rst
   Rules/Php/Php81RemovedDirective.rst
   Rules/Php/Php81RemovedFunctions.rst
   Rules/Php/Php81RemovesResources.rst
   Rules/Php/PHP81scalartypehints.rst
   Rules/Php/Php82NewTypes.rst
   Rules/Php/Php80NamedParameterVariadic.rst
   Rules/Php/AlternativeSyntax.rst
   Rules/Arrays/Phparrayindex.rst
   Rules/Php/MiddleVersion.rst
   Rules/Constants/PhpConstantUsage.rst
   Rules/Php/EchoTagUsage.rst
   Rules/Exceptions/IsPhpException.rst
   Rules/Php/SetHandlers.rst
   Rules/Interfaces/Php.rst
   Rules/Php/ReservedNames.rst
   Rules/Attributes/PhpNativeAttributes.rst
   Rules/Php/NativeClassTypeCompatibility.rst
   Rules/Php/JsonSerializeReturnType.rst
   Rules/Php/OveriddenFunction.rst
   Rules/Type/Sapi.rst
   Rules/Variables/VariablePhp.rst
   Rules/Variables/Php5IndirectExpression.rst
   Rules/Structures/PHP7Dirname.rst
   Rules/Psr/Psr11Usage.rst
   Rules/Psr/Psr13Usage.rst
   Rules/Psr/Psr16Usage.rst
   Rules/Psr/Psr3Usage.rst
   Rules/Psr/Psr6Usage.rst
   Rules/Psr/Psr7Usage.rst
   Rules/Type/Pack.rst
   Rules/Functions/ParameterHiding.rst
   Rules/Classes/ParentFirst.rst
   Rules/Classes/ParentIsNotStatic.rst
   Rules/Classes/PssWithoutClass.rst
   Rules/Php/ParenthesisAsParameter.rst
   Rules/Type/Path.rst
   Rules/Php/PathinfoReturns.rst
   Rules/Php/PearUsage.rst
   Rules/Type/Pcre.rst
   Rules/Vendors/Phalcon.rst
   Rules/Variables/Php7IndirectExpression.rst
   Rules/Php/Php71NewClasses.rst
   Rules/Php/Php72NewClasses.rst
   Rules/Php/Php74NewClasses.rst
   Rules/Php/Php80OnlyTypeHints.rst
   Rules/Php/Php80VariableSyntax.rst
   Rules/Php/Php83NewClasses.rst
   Rules/Complete/PhpExtStubPropertyMethod.rst
   Rules/Complete/PhpNativeReference.rst
   Rules/Php/Php7RelaxedKeyword.rst
   Rules/Structures/PhpinfoUsage.rst
   Rules/Php/PlusPlusOnLetters.rst
   Rules/Namespaces/AliasConfusion.rst
   Rules/Structures/PossibleIncrement.rst
   Rules/Structures/PossibleInfiniteLoop.rst
   Rules/Interfaces/PossibleInterfaces.rst
   Rules/Php/MissingSubpattern.rst
   Rules/Exceptions/PossibleTypeError.rst
   Rules/Performances/PreCalculateUse.rst
   Rules/Performances/PrePostIncrement.rst
   Rules/Functions/PrefixToType.rst
   Rules/Arrays/ShouldPreprocess.rst
   Rules/Structures/ShouldPreprocess.rst
   Rules/Structures/PrintAndDie.rst
   Rules/Type/Printf.rst
   Rules/Structures/PrintfArguments.rst
   Rules/Performances/RegexOnCollector.rst
   Rules/Classes/PromotedProperties.rst
   Rules/Complete/PropagateConstants.rst
   Rules/Classes/PPPDeclarationStyle.rst
   Rules/Classes/CannotBeReadonly.rst
   Rules/Classes/PropertyCouldBeLocal.rst
   Rules/Classes/CouldBePrivate.rst
   Rules/Classes/ExportProperty.rst
   Rules/Classes/PropertyInvasion.rst
   Rules/Classes/PropertyDefinition.rst
   Rules/Classes/PropertyUsedAbove.rst
   Rules/Classes/PropertyUsedBelow.rst
   Rules/Classes/PropertyUsedInOneMethodOnly.rst
   Rules/Structures/PropertyVariableConfusion.rst
   Rules/Type/Protocols.rst
   Rules/Dump/PublicReach.rst
   Rules/Structures/QueriesInLoop.rst
   Rules/Classes/RaisedAccessLevel.rst
   Rules/Structures/RandomWithoutTry.rst
   Rules/Extensions/Extrandom.rst
   Rules/Arrays/RandomlySortedLiterals.rst
   Rules/Php/ReadonlyPropertyChangedByCloning.rst
   Rules/Classes/ReadonlyUsage.rst
   Rules/Functions/RealFunctions.rst
   Rules/Variables/RealVariables.rst
   Rules/Structures/RecalledCondition.rst
   Rules/Functions/Recursive.rst
   Rules/Variables/RecycledVariables.rst
   Rules/Functions/RedeclaredPhpFunction.rst
   Rules/Variables/RedeclaredStaticVariable.rst
   Rules/Classes/RedefinedConstants.rst
   Rules/Classes/RedefinedDefault.rst
   Rules/Classes/RedefinedMethods.rst
   Rules/Traits/Php.rst
   Rules/Classes/RedefinedPrivateProperty.rst
   Rules/Classes/RedefinedProperty.rst
   Rules/Php/ReflectionExportIsDeprecated.rst
   Rules/Structures/RegexDelimiter.rst
   Rules/Type/Regex.rst
   Rules/Performances/RegexOnArrays.rst
   Rules/Security/RegisterGlobals.rst
   Rules/Constants/RelayConstant.rst
   Rules/Functions/RelayFunction.rst
   Rules/Functions/RemoveParameterWithNamedOnes.rst
   Rules/Interfaces/RepeatedInterface.rst
   Rules/Structures/RepeatedRegex.rst
   Rules/Structures/RepeatedPrint.rst
   Rules/Php/ReservedKeywords7.rst
   Rules/Php/ReservedMatchKeyword.rst
   Rules/Php/ReservedMethods.rst
   Rules/Structures/ResourcesUsage.rst
   Rules/Php/RestrictGlobalUsage.rst
   Rules/Structures/ResultMayBeMissing.rst
   Rules/Exceptions/Rethrown.rst
   Rules/Structures/ReturnTrueFalse.rst
   Rules/Php/ReturnTypehintUsage.rst
   Rules/Php/ReturnWithParenthesis.rst
   Rules/Structures/ReturnVoid.rst
   Rules/Functions/RetypedReference.rst
   Rules/Structures/ReuseVariable.rst
   Rules/Classes/RewroteFinalClassConstant.rst
   Rules/Type/Sql.rst
   Rules/Security/CurlOptions.rst
   Rules/Security/SafeHttpHeaders.rst
   Rules/Php/SafePhpvars.rst
   Rules/Structures/SameConditions.rst
   Rules/Classes/PropertyMethodSameName.rst
   Rules/Structures/AutoUnsetForeach.rst
   Rules/Php/ScalarAreNotArrays.rst
   Rules/Classes/ScalarOrObjectProperty.rst
   Rules/Php/ScalarTypehintUsage.rst
   Rules/Performances/ClassOperator.rst
   Rules/Structures/ArraySearchMultipleKeys.rst
   Rules/Traits/SelfUsingTrait.rst
   Rules/Variables/SelfTransform.rst
   Rules/Functions/SemanticTyping.rst
   Rules/Security/SensitiveArgument.rst
   Rules/Structures/SequenceInFor.rst
   Rules/Php/SerializeMagic.rst
   Rules/Security/SessionLazyWrite.rst
   Rules/Php/SessionVariables.rst
   Rules/Complete/SetArrayClassDefinition.rst
   Rules/Structures/SetAside.rst
   Rules/Exceptions/SetChainingException.rst
   Rules/Complete/SetClassMethodRemoteDefinition.rst
   Rules/Complete/SetClassPropertyDefinitionWithTypehint.rst
   Rules/Complete/SetClassRemoteDefinitionWithGlobal.rst
   Rules/Complete/SetClassRemoteDefinitionWithInjection.rst
   Rules/Complete/SetClassRemoteDefinitionWithLocalNew.rst
   Rules/Complete/SetClassRemoteDefinitionWithParenthesis.rst
   Rules/Complete/SetClassRemoteDefinitionWithReturnTypehint.rst
   Rules/Complete/SetClassRemoteDefinitionWithTypehint.rst
   Rules/Complete/SetCloneLink.rst
   Rules/Security/SetCookieArgs.rst
   Rules/Complete/SetMethodFnp.rst
   Rules/Complete/SetParentDefinition.rst
   Rules/Complete/SetClassAliasDefinition.rst
   Rules/Structures/SetlocaleNeedsConstants.rst
   Rules/Structures/OneLineTwoInstructions.rst
   Rules/Php/ShellFavorite.rst
   Rules/Structures/ShellUsage.rst
   Rules/Type/Shellcommands.rst
   Rules/Php/ShortOpenTagRequired.rst
   Rules/Structures/ShortOrCompleteComparison.rst
   Rules/Arrays/ArrayNSUsage.rst
   Rules/Php/ShortTernary.rst
   Rules/Type/ShouldBeSingleQuote.rst
   Rules/Performances/ShouldCacheLocal.rst
   Rules/Structures/ShouldChainException.rst
   Rules/Classes/ShouldDeepClone.rst
   Rules/Classes/ShouldHaveDestructor.rst
   Rules/Namespaces/ShouldMakeAlias.rst
   Rules/Php/ShouldPreprocess.rst
   Rules/Type/ShouldTypecast.rst
   Rules/Php/ShouldUseCoalesce.rst
   Rules/Functions/ShouldUseConstants.rst
   Rules/Structures/ShouldUseExplodeArgs.rst
   Rules/Structures/ShouldUseForeach.rst
   Rules/Classes/ShouldUseThis.rst
   Rules/Structures/ShouldUseMath.rst
   Rules/Structures/ShouldUseOperator.rst
   Rules/Security/ShouldUsePreparedStatement.rst
   Rules/Php/UseSetCookie.rst
   Rules/Structures/ShouldMakeTernary.rst
   Rules/Structures/UseUrlQueryFunctions.rst
   Rules/Php/ShouldUseFunction.rst
   Rules/Php/ShouldUseArrayColumn.rst
   Rules/Php/ShouldUseArrayFilter.rst
   Rules/Security/ShouldUseSessionRegenerateId.rst
   Rules/Functions/ShouldYieldWithKey.rst
   Rules/Traits/SidelinedMethod.rst
   Rules/Php/SignatureTrailingComma.rst
   Rules/Type/SilentlyCastInteger.rst
   Rules/Type/SimilarIntegers.rst
   Rules/Php/GlobalWithoutSimpleVariable.rst
   Rules/Performances/SimpleSwitch.rst
   Rules/Performances/SimplifyForeach.rst
   Rules/Structures/SimplePreg.rst
   Rules/Variables/UniqueUsage.rst
   Rules/Performances/SkipEmptyArray.rst
   Rules/Arrays/SliceFirst.rst
   Rules/Performances/SlowFunctions.rst
   Rules/Complete/SolveTraitConstants.rst
   Rules/Complete/SolveTraitMethods.rst
   Rules/Type/SpecialIntegers.rst
   Rules/Php/SpreadOperatorForArray.rst
   Rules/Structures/SprintfFormatCompilation.rst
   Rules/Security/Sqlite3RequiresSingleQuotes.rst
   Rules/Typehints/StandaloneTypeTFN.rst
   Rules/Performances/StaticCallDontNeedObjects.rst
   Rules/Performances/StaticCallWithSelf.rst
   Rules/Structures/SGVariablesConfusion.rst
   Rules/Structures/StaticInclude.rst
   Rules/Structures/StaticLoop.rst
   Rules/Classes/StaticMethods.rst
   Rules/Classes/StaticMethodsCalledFromObject.rst
   Rules/Classes/StaticContainsThis.rst
   Rules/Classes/StaticCannotCallNonStatic.rst
   Rules/Classes/StaticProperties.rst
   Rules/Php/StaticVariableDefaultCanBeAnyExpression.rst
   Rules/Variables/StaticVariableInNamespace.rst
   Rules/Variables/StaticVariableInitialisation.rst
   Rules/Variables/StaticVariables.rst
   Rules/Extensions/Extstomp.rst
   Rules/Constants/StrangeName.rst
   Rules/Variables/StrangeName.rst
   Rules/Classes/StrangeName.rst
   Rules/Structures/BooleanStrictComparison.rst
   Rules/Structures/StrictInArrayFavorite.rst
   Rules/Structures/ComparisonFavorite.rst
   Rules/Extensions/Extstring.rst
   Rules/Php/StringIntComparison.rst
   Rules/Structures/StringInterpolationFavorite.rst
   Rules/Type/StringHoldAVariable.rst
   Rules/Type/StringWithStrangeSpace.rst
   Rules/Structures/StrposLessThanOne.rst
   Rules/Structures/StrposCompare.rst
   Rules/Php/StrtrArguments.rst
   Rules/Structures/SubstrToTrim.rst
   Rules/Performances/SubstrInLoops.rst
   Rules/Performances/SubstrFirst.rst
   Rules/Php/SuperGlobalUsage.rst
   Rules/Security/SuperGlobalContagion.rst
   Rules/Complete/Superglobals.rst
   Rules/Structures/SuspiciousComparison.rst
   Rules/Classes/SwappedArguments.rst
   Rules/Structures/Fallthrough.rst
   Rules/Structures/SwitchToSwitch.rst
   Rules/Structures/SwitchWithMultipleDefault.rst
   Rules/Structures/SwitchWithoutDefault.rst
   Rules/Extensions/Extswoole.rst
   Rules/Vendors/Sylius.rst
   Rules/Vendors/Symfony.rst
   Rules/Structures/TernaryInConcat.rst
   Rules/Classes/TestClass.rst
   Rules/Structures/TestThenCast.rst
   Rules/Php/MixedKeyword.rst
   Rules/Classes/CouldBeIterable.rst
   Rules/Php/ThrowUsage.rst
   Rules/Exceptions/ThrowFunctioncall.rst
   Rules/Classes/ThrowInDestruct.rst
   Rules/Exceptions/ThrowRawExceptions.rst
   Rules/Php/ThrowWasAnExpression.rst
   Rules/Exceptions/ThrownExceptions.rst
   Rules/Structures/ThrowsAndAssign.rst
   Rules/Php/DeclareTicks.rst
   Rules/Structures/TimestampDifference.rst
   Rules/Structures/ComplexExpression.rst
   Rules/Structures/LongBlock.rst
   Rules/Arrays/TooManyDimensions.rst
   Rules/Structures/TooManyChainedCalls.rst
   Rules/Classes/TooManyChildren.rst
   Rules/Classes/TooManyDereferencing.rst
   Rules/Performances/TooManyExtractions.rst
   Rules/Classes/TooManyFinds.rst
   Rules/Classes/TooManyInjections.rst
   Rules/Functions/TooManyLocalVariables.rst
   Rules/Php/TooManyNativeCalls.rst
   Rules/Functions/TooManyParameters.rst
   Rules/Structures/TooManyElseif.rst
   Rules/Functions/TooMuchIndented.rst
   Rules/Php/TrailingComma.rst
   Rules/Traits/TraitIsNotAType.rst
   Rules/Traits/TraitMethod.rst
   Rules/Traits/Traitnames.rst
   Rules/Traits/TraitNotFound.rst
   Rules/Traits/TraitUsage.rst
   Rules/Php/TriggerErrorUsage.rst
   Rules/Constants/InconsistantCase.rst
   Rules/Structures/TryFinally.rst
   Rules/Php/TryMultipleCatch.rst
   Rules/Exceptions/TryNoCatch.rst
   Rules/Type/ArrayIndex.rst
   Rules/Typehints/CouldBeInt.rst
   Rules/Typehints/CouldBeNever.rst
   Rules/Functions/TypeDodging.rst
   Rules/Functions/TypehintMustBeReturned.rst
   Rules/Classes/TypedClassConstants.rst
   Rules/Php/TypedPropertyUsage.rst
   Rules/Typehints/CouldBeIterable.rst
   Rules/Dump/Typehintorder.rst
   Rules/Dump/TypehintingStats.rst
   Rules/Typehints/CouldBeResource.rst
   Rules/Functions/Typehints.rst
   Rules/Vendors/Typo3.rst
   Rules/Type/Url.rst
   Rules/Functions/UnbindingClosures.rst
   Rules/Exceptions/UncaughtExceptions.rst
   Rules/Structures/UncheckedResources.rst
   Rules/Structures/UnconditionLoopBreak.rst
   Rules/Exceptions/CaughtButNotThrown.rst
   Rules/Classes/UndefinedConstants.rst
   Rules/Classes/UndefinedClasses.rst
   Rules/Variables/UndefinedConstantName.rst
   Rules/Constants/UndefinedConstants.rst
   Rules/Enums/UndefinedEnumcase.rst
   Rules/Functions/UndefinedFunctions.rst
   Rules/Traits/UndefinedInsteadof.rst
   Rules/Interfaces/UndefinedInterfaces.rst
   Rules/Classes/UndefinedMethod.rst
   Rules/Classes/UndefinedParentMP.rst
   Rules/Classes/UndefinedProperty.rst
   Rules/Traits/UndefinedTrait.rst
   Rules/Variables/UndefinedVariable.rst
   Rules/Classes/UndefinedStaticclass.rst
   Rules/Classes/UndefinedStaticMP.rst
   Rules/Classes/UnfinishedObject.rst
   Rules/Type/UnicodeBlock.rst
   Rules/Php/UnicodeEscapePartial.rst
   Rules/Php/UnicodeEscapeSyntax.rst
   Rules/Classes/UninitedProperty.rst
   Rules/Php/Php80UnionTypehint.rst
   Rules/Classes/UnitializedProperties.rst
   Rules/Php/DirectiveName.rst
   Rules/Functions/UnknownParameterName.rst
   Rules/Php/UnknownPcre2Option.rst
   Rules/Structures/UnknownPregOption.rst
   Rules/Php/UnpackingInsideArrays.rst
   Rules/Structures/Unpreprocessed.rst
   Rules/Classes/UnreachableConstant.rst
   Rules/Structures/UnreachableCode.rst
   Rules/Classes/UnreachableMethod.rst
   Rules/Structures/WrongRange.rst
   Rules/Classes/UnresolvedCatch.rst
   Rules/Classes/UnresolvedClasses.rst
   Rules/Classes/UnresolvedInstanceof.rst
   Rules/Namespaces/UnresolvedUse.rst
   Rules/Security/UnserializeSecondArg.rst
   Rules/Functions/UnsetOnArguments.rst
   Rules/Structures/UnsetInForeach.rst
   Rules/Php/UnsetOrCast.rst
   Rules/Structures/UnsupportedOperandTypes.rst
   Rules/Structures/UnsupportedTypesWithOperators.rst
   Rules/Exceptions/Unthrown.rst
   Rules/Classes/UntypedNoDefaultProperties.rst
   Rules/Classes/UnusedConstant.rst
   Rules/Classes/UnusedClass.rst
   Rules/Constants/UnusedConstants.rst
   Rules/Enums/UnusedEnumCase.rst
   Rules/Exceptions/UnusedExceptionVariable.rst
   Rules/Functions/UnusedFunctions.rst
   Rules/Structures/UnusedGlobal.rst
   Rules/Functions/UnusedInheritedVariable.rst
   Rules/Interfaces/UnusedInterfaces.rst
   Rules/Structures/UnusedLabel.rst
   Rules/Classes/UnusedMethods.rst
   Rules/Functions/UnusedArguments.rst
   Rules/Classes/UnusedPrivateMethod.rst
   Rules/Classes/UnusedPrivateProperty.rst
   Rules/Classes/UnusedProtectedMethods.rst
   Rules/Classes/UnusedPublicMethod.rst
   Rules/Functions/UnusedReturnedValue.rst
   Rules/Traits/UnusedClassTrait.rst
   Rules/Traits/UnusedTrait.rst
   Rules/Namespaces/UnusedUse.rst
   Rules/Php/UpperCaseFunction.rst
   Rules/Security/SessionCachedData.rst
   Rules/Security/UploadFilenameInjection.rst
   Rules/Classes/ClassAliasUsage.rst
   Rules/Classes/UseClassOperator.rst
   Rules/Php/IsnullVsEqualNull.rst
   Rules/Structures/UseArrayFunctions.rst
   Rules/Functions/UseArrowFunctions.rst
   Rules/Structures/BasenameSuffix.rst
   Rules/Php/UseBrowscap.rst
   Rules/Php/UseCli.rst
   Rules/Php/UseTrailingUseComma.rst
   Rules/Composer/UseComposerLock.rst
   Rules/Namespaces/UseFunctionsConstants.rst
   Rules/Functions/UseConstantAsArguments.rst
   Rules/Structures/UseConstant.rst
   Rules/Functions/UseConstantsAsReturns.rst
   Rules/Php/UseContravariance.rst
   Rules/Php/UseCookies.rst
   Rules/Php/UseCovariance.rst
   Rules/Php/UseDNF.rst
   Rules/Php/UseDateTimeImmutable.rst
   Rules/Structures/UseDebug.rst
   Rules/Php/UseEnumCaseInConstantExpression.rst
   Rules/Structures/UseFileAppend.rst
   Rules/Classes/UseInstanceof.rst
   Rules/Structures/UseListWithForeach.rst
   Rules/Php/CaseForPSS.rst
   Rules/Functions/AvoidBooleanArgument.rst
   Rules/Php/UseNullSafeOperator.rst
   Rules/Php/UseNullableType.rst
   Rules/Php/UseAttributes.rst
   Rules/Php/UseObjectApi.rst
   Rules/Performances/PHP7EncapsedStrings.rst
   Rules/Php/UsePathinfo.rst
   Rules/Structures/UsePositiveCondition.rst
   Rules/Structures/UseCountRecursive.rst
   Rules/Structures/UseSameTypesForComparisons.rst
   Rules/Structures/UseSystemTmp.rst
   Rules/Performances/UseBlindVar.rst
   Rules/Structures/UseCaseValue.rst
   Rules/Classes/UseThis.rst
   Rules/Structures/UseVariableInsideLoop.rst
   Rules/Php/UseWeb.rst
   Rules/Namespaces/UseWithFullyQualifiedNS.rst
   Rules/Performances/UseArraySlice.rst
   Rules/Php/UseClassAlias.rst
   Rules/Constants/ConstRecommended.rst
   Rules/Php/UseGetDebugType.rst
   Rules/Php/CouldUseIsCountable.rst
   Rules/Structures/JsonWithOption.rst
   Rules/Php/Password55.rst
   Rules/Php/UsePathinfoArgs.rst
   Rules/Php/BetterRand.rst
   Rules/Php/UseSessionStartOptions.rst
   Rules/Php/UseStrContains.rst
   Rules/Structures/UseStrEndsWith.rst
   Rules/Structures/UseStrStartsWith.rst
   Rules/Classes/UsedClass.rst
   Rules/Functions/UsedFunctions.rst
   Rules/Interfaces/UsedInterfaces.rst
   Rules/Classes/UsedMethods.rst
   Rules/Classes/UsedOnceProperty.rst
   Rules/Traits/UsedOnceTrait.rst
   Rules/Variables/VariableUsedOnce.rst
   Rules/Variables/VariableUsedOnceByContext.rst
   Rules/Classes/UsedPrivateMethod.rst
   Rules/Classes/UsedProtectedMethod.rst
   Rules/Classes/UsedPrivateProperty.rst
   Rules/Traits/UsedTrait.rst
   Rules/Namespaces/UsedUse.rst
   Rules/Classes/UselessAbstract.rst
   Rules/Functions/UselessArgument.rst
   Rules/Classes/UselessAssignationOfPromotedProperty.rst
   Rules/Structures/UselessBrackets.rst
   Rules/Exceptions/UselessCatch.rst
   Rules/Structures/UselessCheck.rst
   Rules/Structures/UselessCoalesce.rst
   Rules/Classes/UselessConstantOverwrite.rst
   Rules/Classes/UselessConstructor.rst
   Rules/Functions/UselessDefault.rst
   Rules/Classes/UselessFinal.rst
   Rules/Structures/UselessGlobal.rst
   Rules/Structures/UselessInstruction.rst
   Rules/Interfaces/UselessInterfaces.rst
   Rules/Classes/UselessMethod.rst
   Rules/Traits/UselessAlias.rst
   Rules/Structures/UselessNullCoalesce.rst
   Rules/Classes/UselessNullSafeOperator.rst
   Rules/Attributes/UselessOverride.rst
   Rules/Structures/UselessParenthesis.rst
   Rules/Functions/UselessReferenceArgument.rst
   Rules/Functions/UselessReturn.rst
   Rules/Structures/UselessShortTernary.rst
   Rules/Structures/UselessSwitch.rst
   Rules/Structures/UselessTrailingComma.rst
   Rules/Exceptions/UselessTry.rst
   Rules/Classes/UselessTypehint.rst
   Rules/Structures/UselessCasting.rst
   Rules/Functions/UselessTypeCheck.rst
   Rules/Structures/UselessUnset.rst
   Rules/Functions/UsesDefaultArguments.rst
   Rules/Php/UsesEnv.rst
   Rules/Php/UseMatch.rst
   Rules/Classes/UsingThisOutsideAClass.rst
   Rules/Attributes/UsingDeprecated.rst
   Rules/Functions/UsingDeprecated.rst
   Rules/Structures/ShortTags.rst
   Rules/Php/UsortSorting.rst
   Rules/Php/Utf8EncodeDeprecated.rst
   Rules/Classes/OldStyleVar.rst
   Rules/Complete/VariableTypehint.rst
   Rules/Constants/VariableConstant.rst
   Rules/Structures/VariableGlobal.rst
   Rules/Variables/IsLocalConstant.rst
   Rules/Structures/NoVariableIsACondition.rst
   Rules/Functions/VariableParameterAmbiguityInArrowFunction.rst
   Rules/Variables/References.rst
   Rules/Variables/VariableVariables.rst
   Rules/Variables/VariableLong.rst
   Rules/Variables/VariableOneLetter.rst
   Rules/Functions/VoidIsNotAReference.rst
   Rules/Arrays/WeakType.rst
   Rules/Classes/WeakType.rst
   Rules/Arrays/WeirdIndex.rst
   Rules/Structures/WhileListEach.rst
   Rules/Portability/WindowsOnlyConstants.rst
   Rules/Vendors/Wordpress.rst
   Rules/Variables/WrittenOnlyVariable.rst
   Rules/Classes/UndeclaredStaticProperty.rst
   Rules/Functions/WrongArgumentNameWithPhpFunction.rst
   Rules/Functions/WrongArgumentType.rst
   Rules/Php/WrongAttributeConfiguration.rst
   Rules/Namespaces/WrongCase.rst
   Rules/Classes/WrongCase.rst
   Rules/Functions/WrongCase.rst
   Rules/Structures/WrongLocale.rst
   Rules/Functions/WrongNumberOfArguments.rst
   Rules/Functions/WrongNumberOfArgumentsMethods.rst
   Rules/Functions/WrongOptionalParameter.rst
   Rules/Php/InternalParameterType.rst
   Rules/Structures/WrongPrecedenceInExpression.rst
   Rules/Php/WrongTypeForNativeFunction.rst
   Rules/Functions/WrongReturnedType.rst
   Rules/Functions/WrongTypeWithCall.rst
   Rules/Typehints/WrongTypeWithDefault.rst
   Rules/Functions/WrongTypehintedName.rst
   Rules/Classes/WrongTypedPropertyInit.rst
   Rules/Php/FopenMode.rst
   Rules/Php/YieldFromUsage.rst
   Rules/Php/YieldUsage.rst
   Rules/Vendors/Yii.rst
   Rules/Structures/YodaComparison.rst
   Rules/Structures/DirThenSlash.rst
   Rules/Php/debugInfoUsage.rst
   Rules/Php/Haltcompiler.rst
   Rules/Structures/toStringThrowsException.rst
   Rules/Performances/ArrayKeyExistsSpeedup.rst
   Rules/Php/ArrayKeyExistsWithObjects.rst
   Rules/Structures/ArrayMergeWithEllipsis.rst
   Rules/Structures/ArrayMergeAndVariadic.rst
   Rules/Php/ClassAliasSupportsInternalClasses.rst
   Rules/Structures/CryptWithoutSalt.rst
   Rules/Structures/CurlVersionNow.rst
   Rules/Structures/DateTimePreference.rst
   Rules/Structures/ErrorReportingWithInteger.rst
   Rules/Structures/EvalWithoutTry.rst
   Rules/Extensions/Extzmq.rst
   Rules/Extensions/Extcsv.rst
   Rules/Extensions/Extamqp.rst
   Rules/Extensions/Extapache.rst
   Rules/Extensions/Extapc.rst
   Rules/Extensions/Extapcu.rst
   Rules/Extensions/Extarray.rst
   Rules/Extensions/Extbcmath.rst
   Rules/Extensions/Extbzip2.rst
   Rules/Extensions/Extcalendar.rst
   Rules/Extensions/Extcmark.rst
   Rules/Extensions/Extcom.rst
   Rules/Extensions/Extcrypto.rst
   Rules/Extensions/Extctype.rst
   Rules/Extensions/Extcurl.rst
   Rules/Extensions/Extdate.rst
   Rules/Extensions/Extdb2.rst
   Rules/Extensions/Extdba.rst
   Rules/Extensions/Extdecimal.rst
   Rules/Extensions/Extdio.rst
   Rules/Extensions/Extdom.rst
   Rules/Extensions/Extds.rst
   Rules/Extensions/Exteaccelerator.rst
   Rules/Extensions/Exteio.rst
   Rules/Extensions/Extenchant.rst
   Rules/Extensions/Extev.rst
   Rules/Extensions/Extevent.rst
   Rules/Extensions/Extexif.rst
   Rules/Extensions/Extexpect.rst
   Rules/Extensions/Extfam.rst
   Rules/Extensions/Extfann.rst
   Rules/Extensions/Extffi.rst
   Rules/Extensions/Extfile.rst
   Rules/Extensions/Extfileinfo.rst
   Rules/Extensions/Extfilter.rst
   Rules/Extensions/Extfpm.rst
   Rules/Extensions/Extftp.rst
   Rules/Extensions/Extgd.rst
   Rules/Extensions/Extgearman.rst
   Rules/Extensions/Extgender.rst
   Rules/Extensions/Extgeoip.rst
   Rules/Extensions/Extgettext.rst
   Rules/Extensions/Extgmagick.rst
   Rules/Extensions/Extgmp.rst
   Rules/Extensions/Extgnupg.rst
   Rules/Extensions/Extgrpc.rst
   Rules/Extensions/Exthash.rst
   Rules/Extensions/Exthrtime.rst
   Rules/Extensions/Extibase.rst
   Rules/Extensions/Exticonv.rst
   Rules/Extensions/Extigbinary.rst
   Rules/Extensions/Extimagick.rst
   Rules/Extensions/Extimap.rst
   Rules/Extensions/Extinfo.rst
   Rules/Extensions/Extinotify.rst
   Rules/Extensions/Extintl.rst
   Rules/Extensions/Extjson.rst
   Rules/Extensions/Extjudy.rst
   Rules/Extensions/Extldap.rst
   Rules/Extensions/Extleveldb.rst
   Rules/Extensions/Extlibsodium.rst
   Rules/Extensions/Extlibxml.rst
   Rules/Extensions/Extlua.rst
   Rules/Extensions/Extlzf.rst
   Rules/Extensions/Extmail.rst
   Rules/Extensions/Extmailparse.rst
   Rules/Extensions/Extmath.rst
   Rules/Extensions/Extmbstring.rst
   Rules/Extensions/Extmcrypt.rst
   Rules/Extensions/Extmemcache.rst
   Rules/Extensions/Extmemcached.rst
   Rules/Extensions/Extmongo.rst
   Rules/Extensions/Extmongodb.rst
   Rules/Extensions/Extmsgpack.rst
   Rules/Extensions/Extmssql.rst
   Rules/Extensions/Extmysql.rst
   Rules/Extensions/Extmysqli.rst
   Rules/Extensions/Extncurses.rst
   Rules/Extensions/Extnewt.rst
   Rules/Extensions/Extnsapi.rst
   Rules/Extensions/Extob.rst
   Rules/Extensions/Extoci8.rst
   Rules/Extensions/Extodbc.rst
   Rules/Extensions/Extopcache.rst
   Rules/Extensions/Extopencensus.rst
   Rules/Extensions/Extopenssl.rst
   Rules/Extensions/Extparle.rst
   Rules/Extensions/Extpassword.rst
   Rules/Extensions/Extpcntl.rst
   Rules/Extensions/Extpcov.rst
   Rules/Extensions/Extpcre.rst
   Rules/Extensions/Extpdo.rst
   Rules/Extensions/Exthttp.rst
   Rules/Extensions/Extpgsql.rst
   Rules/Extensions/Extphalcon.rst
   Rules/Extensions/Extphar.rst
   Rules/Extensions/Extast.rst
   Rules/Extensions/Extpkcs11.rst
   Rules/Extensions/Extposix.rst
   Rules/Extensions/Extprotobuf.rst
   Rules/Extensions/Extpspell.rst
   Rules/Extensions/Extpsr.rst
   Rules/Extensions/Extrar.rst
   Rules/Extensions/Extrdkafka.rst
   Rules/Extensions/Extreadline.rst
   Rules/Extensions/Extredis.rst
   Rules/Extensions/Extreflection.rst
   Rules/Extensions/Extscrypt.rst
   Rules/Extensions/Extsdl.rst
   Rules/Extensions/Extseaslog.rst
   Rules/Extensions/Extsem.rst
   Rules/Extensions/Extsession.rst
   Rules/Extensions/Extshmop.rst
   Rules/Extensions/Extsimplexml.rst
   Rules/Extensions/Extsnmp.rst
   Rules/Extensions/Extsoap.rst
   Rules/Extensions/Extsockets.rst
   Rules/Extensions/Extsphinx.rst
   Rules/Extensions/Extspl.rst
   Rules/Extensions/Extspx.rst
   Rules/Extensions/Extsqlite.rst
   Rules/Extensions/Extsqlite3.rst
   Rules/Extensions/Extsqlsrv.rst
   Rules/Extensions/Extssh2.rst
   Rules/Extensions/Extstandard.rst
   Rules/Extensions/Extstats.rst
   Rules/Extensions/Extsuhosin.rst
   Rules/Extensions/Extsvm.rst
   Rules/Extensions/Extteds.rst
   Rules/Extensions/Exttidy.rst
   Rules/Extensions/Exttokenizer.rst
   Rules/Extensions/Exttokyotyrant.rst
   Rules/Extensions/Exttrader.rst
   Rules/Extensions/Extuopz.rst
   Rules/Extensions/Extuuid.rst
   Rules/Extensions/Extv8js.rst
   Rules/Extensions/Extvarnish.rst
   Rules/Extensions/Extvips.rst
   Rules/Extensions/Extwasm.rst
   Rules/Extensions/Extwddx.rst
   Rules/Extensions/Extweakref.rst
   Rules/Extensions/Extxattr.rst
   Rules/Extensions/Extxdebug.rst
   Rules/Extensions/Extxdiff.rst
   Rules/Extensions/Extxhprof.rst
   Rules/Extensions/Extxml.rst
   Rules/Extensions/Extxmlreader.rst
   Rules/Extensions/Extxmlrpc.rst
   Rules/Extensions/Extxmlwriter.rst
   Rules/Extensions/Extxsl.rst
   Rules/Extensions/Extxxtea.rst
   Rules/Extensions/Extyaml.rst
   Rules/Extensions/Extzendmonitor.rst
   Rules/Extensions/Extzip.rst
   Rules/Extensions/Extzlib.rst
   Rules/Extensions/Extzookeeper.rst
   Rules/Security/FilterInputSource.rst
   Rules/Structures/ForeachOnObject.rst
   Rules/Performances/CsvInLoops.rst
   Rules/Functions/funcGetArgModified.rst
   Rules/Structures/GetClassWithoutArg.rst
   Rules/Php/IdnUts46.rst
   Rules/Structures/OnceUsage.rst
   Rules/Structures/IsAVersusInstanceof.rst
   Rules/Structures/IssetWithConstant.rst
   Rules/Structures/ListOmissions.rst
   Rules/Php/Php74mbstrrpos3rdArg.rst
   Rules/Structures/McryptcreateivWithoutOption.rst
   Rules/Security/MoveUploadedFile.rst
   Rules/Structures/OpensslRandomPseudoByteSecondArg.rst
   Rules/Security/parseUrlWithoutParameters.rst
   Rules/Php/PregMatchAllFlag.rst
   Rules/Structures/pregOptionE.rst
   Rules/Classes/NoPSSOutsideClass.rst
   Rules/Php/SetExceptionHandlerPHP7.rst
   Rules/Php/DeclareStrict.rst
   Rules/Structures/StripTagsSkipsClosedTag.rst
   Rules/Performances/StrposTooMuch.rst
   Rules/Php/StrposWithIntegers.rst
   Rules/Performances/timeVsstrtotime.rst
   Rules/Structures/VardumpUsage.rst
   Rules/Php/VersionCompareOperator.rst


Directory by Exakat version
-----------------------------

List of analyzers, by version of introduction, newest to oldest. In parenthesis, the first element is the analyzer name, used with 'analyze -P' command, and the seconds, if any, are the ruleset, used with the -T option. Rulesets are separated by commas, as the same analysis may be used in several rulesets.


* 2.6.8

  * :ref:`Anonymous Catch <anonymous-catch>`
  * :ref:`Cakephp <cakephp>`
  * :ref:`Could Merge Ternary Into Ifthen <could-merge-ternary-into-ifthen>`
  * :ref:`Deprecated Attribute <deprecated-attribute>`
  * :ref:`Duplicate Enum Case Value <duplicate-enum-case-value>`
  * :ref:`Has Property Hook <has-property-hook>`
  * :ref:`Has Virtual Property <has-virtual-property>`
  * :ref:`Method Usage <method-usage>`
  * :ref:`Missing Overriden Method <missing-overriden-method>`
  * :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
  * :ref:`MustUseResult <mustuseresult>`
  * :ref:`Neos <neos>`
  * :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
  * :ref:`Remove Parameter With Named Parameters <remove-parameter-with-named-parameters>`
  * :ref:`Useless Override Attribute <useless-override-attribute>`
  * :ref:`foreach() On Object <foreach()-on-object>`

* 2.6.7

  * :ref:`Constant Used Only Once <constant-used-only-once>`
  * :ref:`Include Variables <include-variables>`
  * :ref:`No Named Parameters <no-named-parameters>`
  * :ref:`Relay Constant <relay-constant>`
  * :ref:`Static Inclusions <static-inclusions>`

* 2.6.6

  * :ref:`Count() Is Not Negative <count()-is-not-negative>`
  * :ref:`Empty Json Error <empty-json-error>`
  * :ref:`Exit Without Argument <exit-without-argument>`
  * :ref:`PHP 8.1 New Types <php-8.1-new-types>`
  * :ref:`PHP 8.2 New Types <php-8.2-new-types>`
  * :ref:`Strpos() Less Than One <strpos()-less-than-one>`
  * :ref:`Useless Coalesce <useless-coalesce>`
  * :ref:`Variable Parameter Ambiguity In Arrow Function <variable-parameter-ambiguity-in-arrow-function>`

* 2.6.5

  * :ref:`Combined Calls <combined-calls>`
  * :ref:`File_Put_Contents Using Array Argument <file\_put\_contents-using-array-argument>`
  * :ref:`Nested Match <nested-match>`
  * :ref:`Useless NullSafe Operator <useless-nullsafe-operator>`
  * :ref:`Useless Short Ternary <useless-short-ternary>`

* 2.6.4

  * :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
  * :ref:`Could Be Readonly Property <could-be-readonly-property>`
  * :ref:`Could Cast To Array <could-cast-to-array>`
  * :ref:`Could Drop Variable <could-drop-variable>`
  * :ref:`Could Use strcontains() <could-use-strcontains()>`
  * :ref:`Injectable Version <injectable-version>`
  * :ref:`Invalid Cast <invalid-cast>`
  * :ref:`Multiple Property Declaration <multiple-property-declaration>`
  * :ref:`New Object Then Immediate Call <new-object-then-immediate-call>`
  * :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`
  * :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
  * :ref:`PHP Native Attributes <php-native-attributes>`
  * :ref:`Property Export <property-export>`
  * :ref:`Try Without Catch <try-without-catch>`
  * :ref:`Wrong Precedence In Expression <wrong-precedence-in-expression>`
  * :ref:`is_a() Versus instanceof <is\_a()-versus-instanceof>`

* 2.6.3

  * :ref:`Can't Call Generator <can't-call-generator>`
  * :ref:`Cannot Use Append For Reading <cannot-use-append-for-reading>`
  * :ref:`Static Methods Cannot Call Non-Static Methods <static-methods-cannot-call-non-static-methods>`

* 2.6.2

  * :ref:`Cant Instantiate Non Class <cant-instantiate-non-class>`
  * :ref:`Count() To Array Append <count()-to-array-append>`
  * :ref:`Don't Use The Type As Variable Name <don't-use-the-type-as-variable-name>`
  * :ref:`Friend Attribute <friend-attribute>`
  * :ref:`Non Integer Nor String As Index <non-integer-nor-string-as-index>`
  * :ref:`Reserved Methods <reserved-methods>`
  * :ref:`Trait Is Not A Type <trait-is-not-a-type>`
  * :ref:`Untyped No Default Properties <untyped-no-default-properties>`
  * :ref:`Useless Trailing Comma <useless-trailing-comma>`
  * :ref:`Void Is Not A Reference <void-is-not-a-reference>`

* 2.6.1

  * :ref:`Append And Assign Arrays <append-and-assign-arrays>`
  * :ref:`Collect Graph Triplets <collect-graph-triplets>`
  * :ref:`Favorite Casting Method <favorite-casting-method>`
  * :ref:`Multiline Expressions <multiline-expressions>`
  * :ref:`Override Attribute <override-attribute>`
  * :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
  * :ref:`Static Variable In Namespace <static-variable-in-namespace>`
  * :ref:`Static Variable Initialisation <static-variable-initialisation>`
  * :ref:`Using Deprecated Feature <using-deprecated-feature>`
  * :ref:`get_class() Without Argument <get\_class()-without-argument>`

* 2.6.0

  * :ref:`Typed Class Constants Usage <typed-class-constants-usage>`

* 2.5.4

  * :ref:`Rewrote Final Class Constant <rewrote-final-class-constant>`

* 2.5.3

  * :ref:`Blind Variable Used Beyond Loop <blind-variable-used-beyond-loop>`
  * :ref:`Class Injection Count <class-injection-count>`
  * :ref:`Collect Catch Calls <collect-catch-calls>`
  * :ref:`Collect Compared Literals <collect-compared-literals>`
  * :ref:`Collect Methods Throwing Exceptions <collect-methods-throwing-exceptions>`
  * :ref:`Collect Property Usage <collect-property-usage>`
  * :ref:`Collect Structures <collect-structures>`
  * :ref:`Collect Throw Calls <collect-throw-calls>`
  * :ref:`Collects Names <collects-names>`
  * :ref:`Comparison On Different Types <comparison-on-different-types>`
  * :ref:`Constants In Traits <constants-in-traits>`
  * :ref:`Converted Exceptions <converted-exceptions>`
  * :ref:`Could Be array_combine() <could-be-array\_combine()>`
  * :ref:`Could Use Yield From <could-use-yield-from>`
  * :ref:`Default Then Discard <default-then-discard>`
  * :ref:`Final Traits Are Final <final-traits-are-final>`
  * :ref:`Identical Case In Switch <identical-case-in-switch>`
  * :ref:`Incompatible Property Between Class And Trait <incompatible-property-between-class-and-trait>`
  * :ref:`Inherited Class Constant Visibility <inherited-class-constant-visibility>`
  * :ref:`Method Is Not An If <method-is-not-an-if>`
  * :ref:`New Dynamic Class Constant Syntax <new-dynamic-class-constant-syntax>`
  * :ref:`No Null For Index <no-null-for-index>`
  * :ref:`Readonly Property Changed By Cloning <readonly-property-changed-by-cloning>`
  * :ref:`Recalled Condition <recalled-condition>`
  * :ref:`Redeclared Static Variable <redeclared-static-variable>`
  * :ref:`Short Or Complete Comparison <short-or-complete-comparison>`
  * :ref:`StandaloneType True False Null <standalonetype-true-false-null>`
  * :ref:`Static Call With Self <static-call-with-self>`
  * :ref:`Static Variable Can Default To Arbitrary Expression <static-variable-can-default-to-arbitrary-expression>`
  * :ref:`Use DNF <use-dnf>`
  * :ref:`Use Enum Case In Constant Expression <use-enum-case-in-constant-expression>`
  * :ref:`Useless Constant Overwrite <useless-constant-overwrite>`
  * :ref:`Useless Try <useless-try>`
  * :ref:`class_alias() Supports Internal Classes <class\_alias()-supports-internal-classes>`

* 2.5.2

  * :ref:`Argument Counts Per Calls <argument-counts-per-calls>`
  * :ref:`Array Access On Literal Array <array-access-on-literal-array>`
  * :ref:`Deprecated Mb_string Encodings <deprecated-mb\_string-encodings>`
  * :ref:`Different Constructors <different-constructors>`
  * :ref:`Double Checks <double-checks>`
  * :ref:`Ellipsis Merge <ellipsis-merge>`
  * :ref:`Global Definitions <global-definitions>`
  * :ref:`Init Then Update <init-then-update>`
  * :ref:`Missing Assignation In Branches <missing-assignation-in-branches>`
  * :ref:`Misused Yield <misused-yield>`
  * :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
  * :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`
  * :ref:`No A Valid Cast <no-a-valid-cast>`
  * :ref:`No Empty String With explode() <no-empty-string-with-explode()>`
  * :ref:`No Max On Empty Array <no-max-on-empty-array>`
  * :ref:`Pre-Calculate Use <pre-calculate-use>`
  * :ref:`Short Ternary <short-ternary>`
  * :ref:`Should Cache Local <should-cache-local>`
  * :ref:`Sidelined Method <sidelined-method>`
  * :ref:`Substr() In Loops <substr()-in-loops>`
  * :ref:`Superglobals <superglobals>`
  * :ref:`Unvalidated Data Cached In Session <unvalidated-data-cached-in-session>`
  * :ref:`Use str_ends_with() <use-str\_ends\_with()>`
  * :ref:`Use str_starts_with() <use-str\_starts\_with()>`
  * :ref:`strpos() With Integers <strpos()-with-integers>`

* 2.5.1

  * :ref:`Class Could Be Readonly <class-could-be-readonly>`
  * :ref:`Class Invasion <class-invasion>`
  * :ref:`Collect SetLocale <collect-setlocale>`
  * :ref:`Filter Not Raw <filter-not-raw>`
  * :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
  * :ref:`Plus Plus Used On Strings <plus-plus-used-on-strings>`
  * :ref:`Property Invasion <property-invasion>`
  * :ref:`Useless Method <useless-method>`
  * :ref:`Weak Type With Array <weak-type-with-array>`

* 2.5.0

  * :ref:`Ambiguous Types With Variables <ambiguous-types-with-variables>`
  * :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
  * :ref:`Collect Calls <collect-calls>`
  * :ref:`Could Use Class Operator <could-use-class-operator>`
  * :ref:`Could Use Namespace Magic Constant <could-use-namespace-magic-constant>`
  * :ref:`Empty Loop <empty-loop>`
  * :ref:`Incompatible Types With Incoming Values <incompatible-types-with-incoming-values>`
  * :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`
  * :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`
  * :ref:`Method Property Confusion <method-property-confusion>`
  * :ref:`Named Arguments And Variadic <named-arguments-and-variadic>`
  * :ref:`No Initial S In Variable Names <no-initial-s-in-variable-names>`
  * :ref:`No Variable Needed <no-variable-needed>`
  * :ref:`Possible TypeError <possible-typeerror>`
  * :ref:`Set Chaining Exception <set-chaining-exception>`
  * :ref:`Set Method Fnp <set-method-fnp>`
  * :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`
  * :ref:`Too Many Chained Calls <too-many-chained-calls>`
  * :ref:`Too Many Extractions <too-many-extractions>`
  * :ref:`Type Dodging <type-dodging>`
  * :ref:`Useless Assignation Of Promoted Property <useless-assignation-of-promoted-property>`

* 2.4.9

  * :ref:`Could Be Abstract Method <could-be-abstract-method>`
  * :ref:`No Keyword In Namespace <no-keyword-in-namespace>`
  * :ref:`Solve Trait Constants <solve-trait-constants>`
  * :ref:`Unused Public Methods <unused-public-methods>`
  * :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

* 2.4.8

  * :ref:`Feast usage <feast-usage>`
  * :ref:`ext/teds <ext-teds>`

* 2.4.7

  * :ref:`Clone Constant <clone-constant>`
  * :ref:`Could Inject Parameter <could-inject-parameter>`
  * :ref:`Empty Array Detection <empty-array-detection>`
  * :ref:`Enum Case Values <enum-case-values>`
  * :ref:`Geospatial <geospatial>`
  * :ref:`Ip <ip>`
  * :ref:`No Default For Referenced Parameter <no-default-for-referenced-parameter>`
  * :ref:`Random extension <random-extension>`
  * :ref:`Strict In_Array() Preference <strict-in\_array()-preference>`
  * :ref:`ext/scrypt <ext-scrypt>`

* 2.4.5

  * :ref:`DateTimeImmutable Is Not Immutable <datetimeimmutable-is-not-immutable>`
  * :ref:`If Then Return Favorite <if-then-return-favorite>`
  * :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`
  * :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
  * :ref:`No Private Abstract Method In Trait <no-private-abstract-method-in-trait>`
  * :ref:`Same Name For Property And Method <same-name-for-property-and-method>`
  * :ref:`Sprintf Format Compilation <sprintf-format-compilation>`
  * :ref:`Typehints/CouldBeResource <typehints-couldberesource>`
  * :ref:`Utf8 Encode And Decode Are Deprecated <utf8-encode-and-decode-are-deprecated>`

* 2.4.4

  * :ref:`Could Be Enumeration <could-be-enumeration>`
  * :ref:`Extensions/Exttaint <extensions-exttaint>`
  * :ref:`Ice framework <ice-framework>`
  * :ref:`Wrong Type With Default <wrong-type-with-default>`

* 2.4.3

  * :ref:`Parent Is Not Static <parent-is-not-static>`
  * :ref:`Retyped Reference <retyped-reference>`

* 2.4.2

  * :ref:`Array Addition <array-addition>`
  * :ref:`Can't Overwrite Final Method <can't-overwrite-final-method>`
  * :ref:`Collect Vendor Structures <collect-vendor-structures>`
  * :ref:`Could Set Property Default <could-set-property-default>`
  * :ref:`Excimer <excimer>`
  * :ref:`Identity <identity>`
  * :ref:`Implicit Conversion To Int <implicit-conversion-to-int>`
  * :ref:`Incoming Date Formats <incoming-date-formats>`
  * :ref:`Lowered Access Level <lowered-access-level>`
  * :ref:`Make All Statics <make-all-statics>`
  * :ref:`No Magic Method For Enum <no-magic-method-for-enum>`
  * :ref:`No Readonly Assignation In Global <no-readonly-assignation-in-global>`
  * :ref:`Overload Existing Names <overload-existing-names>`
  * :ref:`Stomp <stomp>`
  * :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`
  * :ref:`Used Once Trait <used-once-trait>`
  * :ref:`Wrong Locale <wrong-locale>`
  * :ref:`ext/CSV <ext-csv>`
  * :ref:`ext/pkcs11 <ext-pkcs11>`
  * :ref:`ext/spx <ext-spx>`

* 2.4.1

  * :ref:`Collect Stub Structures <collect-stub-structures>`
  * :ref:`Dollar Curly Interpolation Is Deprecated <dollar-curly-interpolation-is-deprecated>`
  * :ref:`Extensions yar <extensions-yar>`

* 2.4.0

  * :ref:`Could Be A Constant <could-be-a-constant>`
  * :ref:`Could Be Spaceship <could-be-spaceship>`
  * :ref:`No Constructor In Interface <no-constructor-in-interface>`
  * :ref:`Sylius usage <sylius-usage>`
  * :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
  * :ref:`Unused Enumeration Case <unused-enumeration-case>`
  * :ref:`Useless Null Coalesce <useless-null-coalesce>`

* 2.3.9

  * :ref:`Add Return Type <add-return-type>`
  * :ref:`Can't Overwrite Final Constant <can't-overwrite-final-constant>`
  * :ref:`Constant : With Or Without Use <constant--with-or-without-use>`
  * :ref:`Don't Add Seconds <don't-add-seconds>`
  * :ref:`Identical Variables In Foreach <identical-variables-in-foreach>`
  * :ref:`String Int Comparison <string-int-comparison>`
  * :ref:`Use Constants As Returns <use-constants-as-returns>`

* 2.3.8

  * :ref:`String Interpolation Favorite <string-interpolation-favorite>`
  * :ref:`Type Could Be Never <type-could-be-never>`

* 2.3.7

  * :ref:`Identical Elseif <identical-elseif>`
  * :ref:`Simplify Foreach <simplify-foreach>`
  * :ref:`Use Variable Created Inside Loop <use-variable-created-inside-loop>`

* 2.3.6

  * :ref:`Could Use array_sum() <could-use-array\_sum()>`
  * :ref:`Is Extension Structure <is-extension-structure>`
  * :ref:`Is PHP Structure <is-php-structure>`
  * :ref:`Is Stub Structure <is-stub-structure>`
  * :ref:`Missing Type In Definition <missing-type-in-definition>`
  * :ref:`Public Reach To Private Methods <public-reach-to-private-methods>`
  * :ref:`Static Call May Be Truly Static <static-call-may-be-truly-static>`
  * :ref:`Too Many Stringed Elseif <too-many-stringed-elseif>`
  * :ref:`Undefined Enumcase <undefined-enumcase>`
  * :ref:`Undefined Methods <undefined-methods>`
  * :ref:`Unfinished Object <unfinished-object>`
  * :ref:`Unreachable Method <unreachable-method>`
  * :ref:`Use class_alias() <use-class\_alias()>`

* 2.3.5

  * :ref:`Collect Dependency Extension <collect-dependency-extension>`
  * :ref:`Could Be Ternary <could-be-ternary>`
  * :ref:`Could Use Existing Constant <could-use-existing-constant>`
  * :ref:`Don't Reuse Foreach Source <don't-reuse-foreach-source>`
  * :ref:`Missing Visibility <missing-visibility>`
  * :ref:`Multiple Similar Calls <multiple-similar-calls>`
  * :ref:`Readonly Usage <readonly-usage>`
  * :ref:`Use File Append <use-file-append>`

* 2.3.3

  * :ref:`Abstract Class Constants <abstract-class-constants>`
  * :ref:`Check Division By Zero <check-division-by-zero>`
  * :ref:`Checks Property Existence <checks-property-existence>`
  * :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
  * :ref:`Getter And Setter <getter-and-setter>`
  * :ref:`Intersection Type <intersection-type>`
  * :ref:`Recycled Variables <recycled-variables>`
  * :ref:`Scope Resolution Operator <scope-resolution-operator>`
  * :ref:`This Could Be Iterable <this-could-be-iterable>`
  * :ref:`Variable Is A Local Constant <variable-is-a-local-constant>`

* 2.3.2

  * :ref:`Can't Overload Constants <can't-overload-constants>`
  * :ref:`Extends stdClass <extends-stdclass>`
  * :ref:`Null Type Favorite <null-type-favorite>`
  * :ref:`Overwritten Foreach Var <overwritten-foreach-var>`
  * :ref:`Variable And Property Type <variable-and-property-type>`

* 2.3.1

  * :ref:`Cannot Call Static Trait Method Directly <cannot-call-static-trait-method-directly>`
  * :ref:`Deprecated Callable <deprecated-callable>`
  * :ref:`Float Conversion As Index <float-conversion-as-index>`
  * :ref:`Nested Attributes <nested-attributes>`
  * :ref:`New Initializers <new-initializers>`
  * :ref:`Promoted Properties <promoted-properties>`
  * :ref:`version_compare() Operator <version\_compare()-operator>`

* 2.3.0

  * :ref:`False To Array Conversion <false-to-array-conversion>`
  * :ref:`Final Constant <final-constant>`
  * :ref:`First Class Callable <first-class-callable>`
  * :ref:`Mixed Type Usage <mixed-type-usage>`
  * :ref:`Named Parameter Usage <named-parameter-usage>`
  * :ref:`Never Keyword <never-keyword>`
  * :ref:`Never Type Usage <never-type-usage>`
  * :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`
  * :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`
  * :ref:`PHP 8.0 Types <php-8.0-types>`
  * :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`
  * :ref:`PHP 8.1 Types <php-8.1-types>`
  * :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
  * :ref:`The Mixed Keyword <the-mixed-keyword>`

* 2.2.5

  * :ref:`Calling Static Trait Method <calling-static-trait-method>`
  * :ref:`No Null For Native PHP Functions <no-null-for-native-php-functions>`

* 2.2.4

  * :ref:`$FILES full_path <$files-full\_path>`
  * :ref:`Missing Attribute Attribute <missing-attribute-attribute>`
  * :ref:`No Referenced Void <no-referenced-void>`
  * :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`

* 2.2.3

  * :ref:`Duplicate Named Parameter <duplicate-named-parameter>`
  * :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
  * :ref:`Incoming Variables <incoming-variables>`
  * :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`
  * :ref:`PHP 8.1 Removed Directives <php-8.1-removed-directives>`
  * :ref:`Wrong Argument Name With PHP Function <wrong-argument-name-with-php-function>`
  * :ref:`idn_to_ascii() New Default <idn\_to\_ascii()-new-default>`

* 2.2.2

  * :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
  * :ref:`Class Overreach <class-overreach>`
  * :ref:`Could Be Generator <could-be-generator>`
  * :ref:`Could Use Match <could-use-match>`
  * :ref:`Enum Usage <enum-usage>`
  * :ref:`Inherited Property Type Must Match <inherited-property-type-must-match>`
  * :ref:`Inherited Static Variable <inherited-static-variable>`
  * :ref:`Multiple Property Declaration On One Line <multiple-property-declaration-on-one-line>`
  * :ref:`No Object As Index <no-object-as-index>`
  * :ref:`Only First Byte Will Be Assigned <only-first-byte-will-be-assigned>`
  * :ref:`Restrict Global Usage <restrict-global-usage>`

* 2.2.1

  * :ref:`Avoid get_object_vars() <avoid-get\_object\_vars()>`
  * :ref:`Declare Static Once <declare-static-once>`
  * :ref:`No Static Variable In A Method <no-static-variable-in-a-method>`
  * :ref:`Reserved Match Keyword <reserved-match-keyword>`

* 2.2.0

  * :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
  * :ref:`Cancelled Parameter <cancelled-parameter>`
  * :ref:`Collect Block Size <collect-block-size>`
  * :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
  * :ref:`Final Private Methods <final-private-methods>`
  * :ref:`Long Preparation For Throw <long-preparation-for-throw>`
  * :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
  * :ref:`Modify Immutable <modify-immutable>`
  * :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
  * :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`
  * :ref:`PHP 80 Named Parameter Variadic <php-80-named-parameter-variadic>`
  * :ref:`Searching For Multiple Keys <searching-for-multiple-keys>`
  * :ref:`Unused Exception Variable <unused-exception-variable>`
  * :ref:`Use str_contains() <use-str\_contains()>`
  * :ref:`Wrong Attribute Configuration <wrong-attribute-configuration>`

* 2.1.9

  * :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
  * :ref:`Assumptions <assumptions>`
  * :ref:`Collect Use Counts <collect-use-counts>`
  * :ref:`Could Be Stringable <could-be-stringable>`
  * :ref:`Could Use Promoted Properties <could-use-promoted-properties>`
  * :ref:`Modified Typed Parameter <modified-typed-parameter>`
  * :ref:`Negative Start Index In Array <negative-start-index-in-array>`
  * :ref:`Optimize Explode() <optimize-explode()>`
  * :ref:`PHP 8.0 Removed Directives <php-8.0-removed-directives>`
  * :ref:`Php Ext Stub Property And Method <php-ext-stub-property-and-method>`
  * :ref:`Unsupported Types With Operators <unsupported-types-with-operators>`
  * :ref:`Use get_debug_type() <use-get\_debug\_type()>`
  * :ref:`Useless Type <useless-type>`

* 2.1.8

  * :ref:`$php_errormsg Usage <$php\_errormsg-usage>`
  * :ref:`Cancel Common Method <cancel-common-method>`
  * :ref:`Cast Unset Usage <cast-unset-usage>`
  * :ref:`Collect Atom Counts <collect-atom-counts>`
  * :ref:`Collect Classes Dependencies <collect-classes-dependencies>`
  * :ref:`Collect Files Dependencies <collect-files-dependencies>`
  * :ref:`Collect Php Structures <collect-php-structures>`
  * :ref:`Function With Dynamic Code <function-with-dynamic-code>`
  * :ref:`Mismatch Parameter And Type <mismatch-parameter-and-type>`
  * :ref:`Mismatch Parameter Name <mismatch-parameter-name>`
  * :ref:`Multiple Declaration Of Strict_types <multiple-declaration-of-strict\_types>`

* 2.1.7

  * :ref:`Collect Class Traits Counts <collect-class-traits-counts>`
  * :ref:`Collect Definitions Statistics <collect-definitions-statistics>`
  * :ref:`Collect Global Variables <collect-global-variables>`
  * :ref:`Collect Native Calls Per Expressions <collect-native-calls-per-expressions>`
  * :ref:`Collect Readability <collect-readability>`
  * :ref:`Collects Variables <collects-variables>`
  * :ref:`Could Be Parent Method <could-be-parent-method>`
  * :ref:`Don't Pollute Global Space <don't-pollute-global-space>`
  * :ref:`Missing Some Returntype <missing-some-returntype>`

* 2.1.6

  * :ref:`Different Argument Counts <different-argument-counts>`
  * :ref:`GLOB_BRACE Usage <glob\_brace-usage>`
  * :ref:`Iconv With Translit <iconv-with-translit>`
  * :ref:`Unknown Parameter Name <unknown-parameter-name>`
  * :ref:`Use Closure Trailing Comma <use-closure-trailing-comma>`
  * :ref:`Use NullSafe Operator <use-nullsafe-operator>`
  * :ref:`Use PHP Attributes <use-php-attributes>`

* 2.1.5

  * :ref:`Abstract Away <abstract-away>`
  * :ref:`Avoid Compare Typed Boolean <avoid-compare-typed-boolean>`
  * :ref:`Catch With Undefined Variable <catch-with-undefined-variable>`
  * :ref:`Collect Parameter Names <collect-parameter-names>`
  * :ref:`Collect Static Class Changes <collect-static-class-changes>`
  * :ref:`Fossilized Methods List <fossilized-methods-list>`
  * :ref:`Large Try Block <large-try-block>`
  * :ref:`Swapped Arguments <swapped-arguments>`
  * :ref:`Wrong Type For Native PHP Function <wrong-type-for-native-php-function>`

* 2.1.4

  * :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
  * :ref:`Call Order <call-order>`
  * :ref:`Could Be Float <could-be-float>`
  * :ref:`Extended Types <extended-types>`
  * :ref:`Mismatch Properties Types <mismatch-properties-types>`
  * :ref:`No Need For Triple Equal <no-need-for-triple-equal>`
  * :ref:`Type Could Be Integer <type-could-be-integer>`
  * :ref:`Typehint Could Be Iterable <typehint-could-be-iterable>`
  * :ref:`Uses PHP 8 Match() <uses-php-8-match()>`

* 2.1.3

  * :ref:`Cyclic References <cyclic-references>`
  * :ref:`Protocol lists <protocol-lists>`
  * :ref:`Wrong Argument Type <wrong-argument-type>`

* 2.1.2

  * :ref:`Collect Class Constant Counts <collect-class-constant-counts>`
  * :ref:`Collect Local Variable Counts <collect-local-variable-counts>`
  * :ref:`Collect Method Counts <collect-method-counts>`
  * :ref:`Collect Property Counts <collect-property-counts>`
  * :ref:`Could Be Array Type <could-be-array-type>`
  * :ref:`Could Be Boolean <could-be-boolean>`
  * :ref:`Could Be CIT <could-be-cit>`
  * :ref:`Could Be Callable <could-be-callable>`
  * :ref:`Could Be Null <could-be-null>`
  * :ref:`Could Be Parent <could-be-parent>`
  * :ref:`Could Be Self <could-be-self>`
  * :ref:`Could Be String <could-be-string>`
  * :ref:`Could Be Type <could-be-type>`
  * :ref:`Could Be Void <could-be-void>`
  * :ref:`Could Not Type <could-not-type>`
  * :ref:`Double Object Assignation <double-object-assignation>`
  * :ref:`Possible Alias Confusion <possible-alias-confusion>`
  * :ref:`Safe Phpvariables <safe-phpvariables>`
  * :ref:`Static Global Variables Confusion <static-global-variables-confusion>`
  * :ref:`Too Long A Block <too-long-a-block>`
  * :ref:`Too Much Indented <too-much-indented>`
  * :ref:`Using Deprecated Method <using-deprecated-method>`

* 2.1.1

  * :ref:`Check Crypto Key Length <check-crypto-key-length>`
  * :ref:`Dynamic Self Calls <dynamic-self-calls>`
  * :ref:`Keep Files Access Restricted <keep-files-access-restricted>`
  * :ref:`OpenSSL Ciphers Used <openssl-ciphers-used>`
  * :ref:`Prefix And Suffixes With Type <prefix-and-suffixes-with-type>`
  * :ref:`Throw Was An Expression <throw-was-an-expression>`
  * :ref:`Undefined Constant Name <undefined-constant-name>`
  * :ref:`Unused Trait In Class <unused-trait-in-class>`

* 2.1.0

  * :ref:`Fn Argument Variable Confusion <fn-argument-variable-confusion>`
  * :ref:`Implicit Nullable Type <implicit-nullable-type>`
  * :ref:`Missing Abstract Method <missing-abstract-method>`
  * :ref:`Signature Trailing Comma <signature-trailing-comma>`

* 2.0.9

  * :ref:`Don't Collect Void <don't-collect-void>`
  * :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
  * :ref:`Uninitialized Property <uninitialized-property>`
  * :ref:`Union Type <union-type>`
  * :ref:`Wrong Typed Property Default <wrong-typed-property-default>`

* 2.0.8

  * :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`
  * :ref:`Php 8.0 Variable Syntax Tweaks <php-8.0-variable-syntax-tweaks>`

* 2.0.7

  * :ref:`Constant Order <constant-order>`

* 2.0.6

  * :ref:`Fossilized Method <fossilized-method>`
  * :ref:`Links Between Parameter And Argument <links-between-parameter-and-argument>`
  * :ref:`Not Equal Is Not !== <not-equal-is-not-!==>`
  * :ref:`Possible Interfaces <possible-interfaces>`

* 2.0.5

  * :ref:`Missing Type <missing-type>`
  * :ref:`Semantic Typing <semantic-typing>`

* 2.0.4

  * :ref:`Coalesce Equal <coalesce-equal>`

* 2.0.3

  * :ref:`Collect Class Children Count <collect-class-children-count>`
  * :ref:`Collect Class Depth <collect-class-depth>`
  * :ref:`Collect Class Interface Counts <collect-class-interface-counts>`
  * :ref:`Exceeding Type <exceeding-type>`

* 2.0.2

  * :ref:`Inclusions <inclusions>`
  * :ref:`Insufficient Property Type <insufficient-property-type>`
  * :ref:`New Order <new-order>`
  * :ref:`Nullable Without Check <nullable-without-check>`
  * :ref:`Typehint Order <typehint-order>`
  * :ref:`Wrong Typed Name <wrong-typed-name>`

* 1.9.9

  * :ref:`Collect Mbstring Encodings <collect-mbstring-encodings>`
  * :ref:`Concrete5 usage <concrete5-usage>`
  * :ref:`Could Type With Array <could-type-with-array>`
  * :ref:`Could Type With Boolean <could-type-with-boolean>`
  * :ref:`Could Type With Int <could-type-with-int>`
  * :ref:`Could Type With Iterable <could-type-with-iterable>`
  * :ref:`Could Type With String <could-type-with-string>`
  * :ref:`Create Foreach Default <create-foreach-default>`
  * :ref:`Filter To add_slashes() <filter-to-add\_slashes()>`
  * :ref:`Immutable Signature <immutable-signature>`
  * :ref:`Is_A() With String <is\_a()-with-string>`
  * :ref:`Mbstring Third Arg <mbstring-third-arg>`
  * :ref:`Mbstring Unknown Encoding <mbstring-unknown-encoding>`
  * :ref:`Merge If Then <merge-if-then>`
  * :ref:`Shell commands <shell-commands>`
  * :ref:`Typehinting Stats <typehinting-stats>`
  * :ref:`Typo 3 usage <typo-3-usage>`
  * :ref:`Weird Array Index <weird-array-index>`
  * :ref:`Wrong Case Namespaces <wrong-case-namespaces>`
  * :ref:`Wrong Type With Call <wrong-type-with-call>`

* 1.9.8

  * :ref:`Can't Implement Traversable <can't-implement-traversable>`
  * :ref:`Parameter Hiding <parameter-hiding>`

* 1.9.7

  * :ref:`Foreach() Favorite <foreach()-favorite>`
  * :ref:`Make Functioncall With Reference <make-functioncall-with-reference>`
  * :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
  * :ref:`Too Many Dereferencing <too-many-dereferencing>`

* 1.9.6

  * :ref:`Collect Parameter Counts <collect-parameter-counts>`
  * :ref:`Create Magic Method <create-magic-method>`
  * :ref:`Dereferencing Levels <dereferencing-levels>`
  * :ref:`Duplicate Literal <duplicate-literal>`
  * :ref:`Internet Domains <internet-domains>`
  * :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`
  * :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`
  * :ref:`Non Nullable Getters <non-nullable-getters>`
  * :ref:`Use The Case Value <use-the-case-value>`

* 1.9.5

  * :ref:`Collect Literals <collect-literals>`
  * :ref:`Environment Variable Usage <environment-variable-usage>`
  * :ref:`Interfaces Don't Ensure Properties <interfaces-don't-ensure-properties>`
  * :ref:`Interfaces Is Not Implemented <interfaces-is-not-implemented>`
  * :ref:`Magic Properties <magic-properties>`
  * :ref:`No Literal For Reference <no-literal-for-reference>`
  * :ref:`Use array_slice() <use-array\_slice()>`

* 1.9.4

  * :ref:`Coalesce And Concat <coalesce-and-concat>`
  * :ref:`Comparison Is Always The Same <comparison-is-always-the-same>`
  * :ref:`Cyclomatic Complexity <cyclomatic-complexity>`
  * :ref:`Nested Ternary Without Parenthesis <nested-ternary-without-parenthesis>`
  * :ref:`PHP 74 New Directives <php-74-new-directives>`
  * :ref:`Should Use Explode Args <should-use-explode-args>`
  * :ref:`Spread Operator For Array <spread-operator-for-array>`
  * :ref:`Too Many Array Dimensions <too-many-array-dimensions>`
  * :ref:`Use Arrow Functions <use-arrow-functions>`

* 1.9.3

  * :ref:`Environment Variables <environment-variables>`
  * :ref:`Indentation Levels <indentation-levels>`
  * :ref:`Max Level Of Nesting <max-level-of-nesting>`
  * :ref:`No Spread For Hash <no-spread-for-hash>`
  * :ref:`PHP 7.4 Constant Deprecation <php-7.4-constant-deprecation>`
  * :ref:`PHP 7.4 Removed Directives <php-7.4-removed-directives>`
  * :ref:`Set Array Class Definition <set-array-class-definition>`
  * :ref:`Set Class Method Remote Definition <set-class-method-remote-definition>`
  * :ref:`Set Class Property Definition With Type <set-class-property-definition-with-type>`
  * :ref:`Set Class Remote Definition With Global <set-class-remote-definition-with-global>`
  * :ref:`Set Class Remote Definition With Local New <set-class-remote-definition-with-local-new>`
  * :ref:`Set Class Remote Definition With Parenthesis <set-class-remote-definition-with-parenthesis>`
  * :ref:`Set Class Remote Definition With Return Type <set-class-remote-definition-with-return-type>`
  * :ref:`Set Class Remote Definition With Type <set-class-remote-definition-with-type>`
  * :ref:`Use Contravariance <use-contravariance>`
  * :ref:`Use Covariance <use-covariance>`
  * :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`
  * :ref:`strip_tags() Skips Closed Tag <strip\_tags()-skips-closed-tag>`

* 1.9.2

  * :ref:`Create Compact Variables <create-compact-variables>`
  * :ref:`Create Default Values <create-default-values>`
  * :ref:`Create Magic Property <create-magic-property>`
  * :ref:`Curly-Bracketed Arrays Are Not Supported <curly-bracketed-arrays-are-not-supported>`
  * :ref:`Follow Closure Definition <follow-closure-definition>`
  * :ref:`Implode() Arguments Order <implode()-arguments-order>`
  * :ref:`Make Class Method Definition <make-class-method-definition>`
  * :ref:`Makes Class Constant Definition <makes-class-constant-definition>`
  * :ref:`No ENT_IGNORE <no-ent\_ignore>`
  * :ref:`Overwritten Constant <overwritten-constant>`
  * :ref:`Overwritten Methods <overwritten-methods>`
  * :ref:`Overwritten Properties <overwritten-properties>`
  * :ref:`PHP 7.4 Reserved Keyword <php-7.4-reserved-keyword>`
  * :ref:`Propagate Constants <propagate-constants>`
  * :ref:`Set Class Remote Definition With Injection <set-class-remote-definition-with-injection>`
  * :ref:`Set Clone Link <set-clone-link>`
  * :ref:`Set Parent Definition <set-parent-definition>`
  * :ref:`Set class_alias() Definition <set-class\_alias()-definition>`
  * :ref:`Solve Trait Methods <solve-trait-methods>`
  * :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`

* 1.9.1

  * :ref:`Php Native Reference Variable <php-native-reference-variable>`

* 1.9.0

  * :ref:`Class Without Parent <class-without-parent>`
  * :ref:`Numeric Literal Separator <numeric-literal-separator>`
  * :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
  * :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
  * :ref:`Scalar Are Not Arrays <scalar-are-not-arrays>`
  * :ref:`Serialize Magic Method <serialize-magic-method>`
  * :ref:`Similar Integers <similar-integers>`
  * :ref:`Unbinding Closures <unbinding-closures>`
  * :ref:`array_key_exists() Works On Arrays <array\_key\_exists()-works-on-arrays>`

* 1.8.9

  * :ref:`Avoid mb_dectect_encoding() <avoid-mb\_dectect\_encoding()>`
  * :ref:`Disconnected Classes <disconnected-classes>`
  * :ref:`Not Or Tilde <not-or-tilde>`
  * :ref:`Overwritten Source And Value <overwritten-source-and-value>`
  * :ref:`Useless Type Check <useless-type-check>`
  * :ref:`mb_strrpos() Third Argument <mb\_strrpos()-third-argument>`

* 1.8.8

  * :ref:`Set Aside Code <set-aside-code>`
  * :ref:`Use Array Functions <use-array-functions>`

* 1.8.7

  * :ref:`Generator Cannot Return <generator-cannot-return>`
  * :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
  * :ref:`Use DateTimeImmutable Class <use-datetimeimmutable-class>`
  * :ref:`Wrong Type Returned <wrong-type-returned>`

* 1.8.6

  * :ref:`Dependant Abstract Classes <dependant-abstract-classes>`
  * :ref:`Infinite Recursion <infinite-recursion>`
  * :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`

* 1.8.5

  * :ref:`Could Use Trait <could-use-trait>`

* 1.8.4

  * :ref:`Always Use Function With array_key_exists() <always-use-function-with-array\_key\_exists()>`
  * :ref:`Complex Dynamic Names <complex-dynamic-names>`
  * :ref:`Could Be Constant <could-be-constant>`
  * :ref:`New Constants In PHP 7.4 <new-constants-in-php-7.4>`
  * :ref:`Regex On Arrays <regex-on-arrays>`
  * :ref:`Unused Class Constant <unused-class-constant>`
  * :ref:`curl_version() Has No Argument <curl\_version()-has-no-argument>`

* 1.8.3

  * :ref:`Autoappend <autoappend>`
  * :ref:`Make Magic Concrete <make-magic-concrete>`
  * :ref:`Memoize MagicCall <memoize-magiccall>`
  * :ref:`Substr To Trim <substr-to-trim>`

* 1.8.2

  * :ref:`Identical Methods <identical-methods>`
  * :ref:`No Append On Source <no-append-on-source>`

* 1.8.1

  * :ref:`No Need For get_class() <no-need-for-get\_class()>`

* 1.8.0

  * :ref:`Already Parents Trait <already-parents-trait>`
  * :ref:`Casting Ternary <casting-ternary>`
  * :ref:`Concat And Addition <concat-and-addition>`
  * :ref:`Concat Empty String <concat-empty-string>`
  * :ref:`Minus One On Error <minus-one-on-error>`
  * :ref:`New Functions In PHP 7.4 <new-functions-in-php-7.4>`
  * :ref:`Unpacking Inside Arrays <unpacking-inside-arrays>`
  * :ref:`Useless Argument <useless-argument>`

* 1.7.9

  * :ref:`Avoid option arrays in constructors <avoid-option-arrays-in-constructors>`
  * :ref:`Trait Not Found <trait-not-found>`
  * :ref:`Useless Default Argument <useless-default-argument>`
  * :ref:`ext/ffi <ext-ffi>`
  * :ref:`ext/uuid <ext-uuid>`
  * :ref:`ext/zend_monitor <ext-zend\_monitor>`

* 1.7.8

  * :ref:`ext/svm <ext-svm>`

* 1.7.7

  * :ref:`Implode One Arg <implode-one-arg>`
  * :ref:`Incoming Values <incoming-values>`
  * :ref:`Insecure Integer Validation <insecure-integer-validation>`

* 1.7.6

  * :ref:`Caught Variable <caught-variable>`
  * :ref:`Multiple Unset() <multiple-unset()>`
  * :ref:`PHP Overridden Function <php-overridden-function>`
  * :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`

* 1.7.2

  * :ref:`Check On __Call Usage <check-on-\_\_call-usage>`
  * :ref:`Unsupported Operand Types <unsupported-operand-types>`

* 1.7.0

  * :ref:`Clone With Non-Object <clone-with-non-object>`
  * :ref:`Self-Transforming Variables <self-transforming-variables>`
  * :ref:`Should Deep Clone <should-deep-clone>`
  * :ref:`Windows Only Constants <windows-only-constants>`

* 1.6.9

  * :ref:`Inconsistent Variable Usage <inconsistent-variable-usage>`
  * :ref:`Type Must Be Returned <type-must-be-returned>`

* 1.6.8

  * :ref:`PHP 8.0 Removed Constants <php-8.0-removed-constants>`
  * :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
  * :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

* 1.6.7

  * :ref:`An OOP Factory <an-oop-factory>`
  * :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
  * :ref:`Law of Demeter <law-of-demeter>`

* 1.6.6

  * :ref:`Bad Type Relay <bad-type-relay>`
  * :ref:`Insufficient Type <insufficient-type>`

* 1.6.5

  * :ref:`Array With String Initialization <array-with-string-initialization>`
  * :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`
  * :ref:`ext/pcov <ext-pcov>`
  * :ref:`ext/weakref <ext-weakref>`

* 1.6.4

  * :ref:`Don't Be Too Manual <don't-be-too-manual>`

* 1.6.3

  * :ref:`Assign And Compare <assign-and-compare>`

* 1.6.2

  * :ref:`Typed Property Usage <typed-property-usage>`

* 1.6.1

  * :ref:`Possible Missing Subpattern <possible-missing-subpattern>`
  * :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`

* 1.5.8

  * :ref:`Multiple Identical Closure <multiple-identical-closure>`
  * :ref:`Path lists <path-lists>`

* 1.5.7

  * :ref:`Method Could Be Static <method-could-be-static>`
  * :ref:`Multiple Usage Of Same Trait <multiple-usage-of-same-trait>`
  * :ref:`Self Using Trait <self-using-trait>`
  * :ref:`ext/wasm <ext-wasm>`

* 1.5.6

  * :ref:`Isset() On The Whole Array <isset()-on-the-whole-array>`
  * :ref:`Useless Method Alias <useless-method-alias>`
  * :ref:`ext/sdl <ext-sdl>`

* 1.5.5

  * :ref:`Directly Use File <directly-use-file>`
  * :ref:`Safe HTTP Headers <safe-http-headers>`
  * :ref:`fputcsv() In Loops <fputcsv()-in-loops>`

* 1.5.4

  * :ref:`Avoid Self In Interface <avoid-self-in-interface>`
  * :ref:`Should Have Destructor <should-have-destructor>`
  * :ref:`Unreachable Class Constant <unreachable-class-constant>`

* 1.5.3

  * :ref:`Declare Global Early <declare-global-early>`
  * :ref:`Don't Loop On Yield <don't-loop-on-yield>`

* 1.5.2

  * :ref:`PHP Exception <php-exception>`
  * :ref:`Should Yield With Key <should-yield-with-key>`
  * :ref:`ext/decimal <ext-decimal>`
  * :ref:`ext/psr <ext-psr>`

* 1.5.1

  * :ref:`Use Basename Suffix <use-basename-suffix>`

* 1.5.0

  * :ref:`Could Use Try <could-use-try>`
  * :ref:`Pack Format Inventory <pack-format-inventory>`
  * :ref:`Printf Format Inventory <printf-format-inventory>`

* 1.4.9

  * :ref:`Don't Read And Write In One Expression <don't-read-and-write-in-one-expression>`
  * :ref:`Invalid Pack Format <invalid-pack-format>`
  * :ref:`Named Regex <named-regex>`
  * :ref:`No Reference For Static Property <no-reference-for-static-property>`
  * :ref:`No Return For Generator <no-return-for-generator>`
  * :ref:`Repeated Interface <repeated-interface>`
  * :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`

* 1.4.8

  * :ref:`Direct Call To __clone() <direct-call-to-\_\_clone()>`
  * :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

* 1.4.6

  * :ref:`Only Variable For Reference <only-variable-for-reference>`

* 1.4.5

  * :ref:`Add Default Value <add-default-value>`

* 1.4.4

  * :ref:`ext/seaslog <ext-seaslog>`

* 1.4.3

  * :ref:`Class Could Be Final <class-could-be-final>`
  * :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
  * :ref:`Inconsistent Elseif <inconsistent-elseif>`
  * :ref:`Use json_decode() Options <use-json\_decode()-options>`

* 1.4.2

  * :ref:`Method Collision Traits <method-collision-traits>`
  * :ref:`Undefined Insteadof <undefined-insteadof>`
  * :ref:`Undefined Variable <undefined-variable>`

* 1.4.1

  * :ref:`Must Call Parent Constructor <must-call-parent-constructor>`

* 1.4.0

  * :ref:`PHP 7.3 Removed Functions <php-7.3-removed-functions>`
  * :ref:`Trailing Comma In Calls <trailing-comma-in-calls>`

* 1.3.9

  * :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
  * :ref:`Avoid Real <avoid-real>`
  * :ref:`Case Insensitive Constants <case-insensitive-constants>`
  * :ref:`Const Or Define Preference <const-or-define-preference>`
  * :ref:`Continue Is For Loop <continue-is-for-loop>`
  * :ref:`Could Be Abstract Class <could-be-abstract-class>`

* 1.3.8

  * :ref:`Constant Case Preference <constant-case-preference>`
  * :ref:`Detect Current Class <detect-current-class>`
  * :ref:`Use is_countable <use-is\_countable>`

* 1.3.7

  * :ref:`Handle Arrays With Callback <handle-arrays-with-callback>`

* 1.3.5

  * :ref:`Locally Used Property In Trait <locally-used-property-in-trait>`
  * :ref:`PHP 7.0 Scalar Types <php-7.0-scalar-types>`
  * :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`
  * :ref:`PHP 7.2 Scalar Types <php-7.2-scalar-types>`
  * :ref:`Undefined static \:\:class <undefined-static-class>`
  * :ref:`ext/lzf <ext-lzf>`
  * :ref:`ext/msgpack <ext-msgpack>`

* 1.3.4

  * :ref:`Ambiguous Visibilities <ambiguous-visibilities>`
  * :ref:`Hash Algorithms Incompatible With PHP 7.1- <hash-algorithms-incompatible-with-php-7.1->`
  * :ref:`Hash Algorithms Incompatible With PHP 7.4- <hash-algorithms-incompatible-with-php-7.4->`

* 1.3.3

  * :ref:`Abstract Or Implements <abstract-or-implements>`
  * :ref:`Can't Implement Throwable <can't-implement-throwable>`
  * :ref:`Incompatible Signature Methods <incompatible-signature-methods>`
  * :ref:`Incompatible Signature Methods With Covariance <incompatible-signature-methods-with-covariance>`
  * :ref:`ext/eio <ext-eio>`

* 1.3.2

  * :ref:`Compared But Not Assigned Strings <compared-but-not-assigned-strings>`
  * :ref:`Comparisons Orientation <comparisons-orientation>`
  * :ref:`Could Be Static Closure <could-be-static-closure>`
  * :ref:`Don't Mix ++ <don't-mix-++>`
  * :ref:`Strict Or Relaxed Comparison <strict-or-relaxed-comparison>`
  * :ref:`move_uploaded_file Instead Of copy <move\_uploaded\_file-instead-of-copy>`

* 1.3.0

  * :ref:`Check JSON <check-json>`
  * :ref:`Const Visibility Usage <const-visibility-usage>`
  * :ref:`Should Use Operator <should-use-operator>`
  * :ref:`Single Use Variables <single-use-variables>`

* 1.2.9

  * :ref:`Configure Extract <configure-extract>`
  * :ref:`Flexible Heredoc <flexible-heredoc>`
  * :ref:`Method Signature Must Be Compatible <method-signature-must-be-compatible>`
  * :ref:`Mismatch Type And Default <mismatch-type-and-default>`
  * :ref:`Nonexistent Variable In compact() <nonexistent-variable-in-compact()>`
  * :ref:`Use The Blind Var <use-the-blind-var>`

* 1.2.8

  * :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
  * :ref:`Can't Instantiate Class <can't-instantiate-class>`
  * :ref:`Class-typed References <class-typed-references>`
  * :ref:`Do In Base <do-in-base>`
  * :ref:`Failing Analysis <failing-analysis>`
  * :ref:`Weak Typing <weak-typing>`
  * :ref:`strpos() Too Much <strpos()-too-much>`

* 1.2.7

  * :ref:`ext/cmark <ext-cmark>`

* 1.2.6

  * :ref:`Callback Function Needs Return <callback-function-needs-return>`
  * :ref:`Could Use array_unique <could-use-array\_unique>`
  * :ref:`Missing Parenthesis <missing-parenthesis>`
  * :ref:`One If Is Sufficient <one-if-is-sufficient>`

* 1.2.5

  * :ref:`Unreadable Interval Check <unreadable-interval-check>`
  * :ref:`ext/zookeeper <ext-zookeeper>`

* 1.2.4

  * :ref:`Processing Collector <processing-collector>`

* 1.2.3

  * :ref:`Don't Unset Properties <don't-unset-properties>`
  * :ref:`Redefined Private Property <redefined-private-property>`
  * :ref:`Strtr Arguments <strtr-arguments>`

* 1.2.2

  * :ref:`Drop Substr Last Arg <drop-substr-last-arg>`

* 1.2.1

  * :ref:`Possible Increment <possible-increment>`
  * :ref:`Properties Declaration Consistence <properties-declaration-consistence>`

* 1.1.10

  * :ref:`Too Many Native Calls <too-many-native-calls>`

* 1.1.9

  * :ref:`Should Preprocess Chr() <should-preprocess-chr()>`
  * :ref:`Too Many Parameters <too-many-parameters>`

* 1.1.8

  * :ref:`Mass Creation Of Arrays <mass-creation-of-arrays>`
  * :ref:`ext/db2 <ext-db2>`

* 1.1.7

  * :ref:`Could Use array_fill_keys <could-use-array\_fill\_keys>`
  * :ref:`Dynamic Library Loading <dynamic-library-loading>`
  * :ref:`PHP 7.3 Last Empty Argument <php-7.3-last-empty-argument>`
  * :ref:`Property Could Be Local <property-could-be-local>`
  * :ref:`Use Recursive count() <use-recursive-count()>`
  * :ref:`ext/leveldb <ext-leveldb>`
  * :ref:`ext/opencensus <ext-opencensus>`
  * :ref:`ext/uopz <ext-uopz>`
  * :ref:`ext/varnish <ext-varnish>`
  * :ref:`ext/xxtea <ext-xxtea>`

* 1.1.6

  * :ref:`Could Use Compact <could-use-compact>`
  * :ref:`Foreach On Object <foreach-on-object>`
  * :ref:`List With Reference <list-with-reference>`
  * :ref:`Test Then Cast <test-then-cast>`

* 1.1.5

  * :ref:`Possible Infinite Loop <possible-infinite-loop>`
  * :ref:`Should Use Math <should-use-math>`
  * :ref:`ext/hrtime <ext-hrtime>`

* 1.1.4

  * :ref:`Double array_flip() <double-array\_flip()>`
  * :ref:`Fallback Function <fallback-function>`
  * :ref:`Find Key Directly <find-key-directly>`
  * :ref:`Reuse Existing Variable <reuse-existing-variable>`
  * :ref:`Useless Catch <useless-catch>`

* 1.1.3

  * :ref:`Useless Referenced Argument <useless-referenced-argument>`

* 1.1.2

  * :ref:`Local Globals <local-globals>`
  * :ref:`Missing Include <missing-include>`

* 1.0.11

  * :ref:`No Net For Xml Load <no-net-for-xml-load>`
  * :ref:`Unused Inherited Variable In Closure <unused-inherited-variable-in-closure>`

* 1.0.10

  * :ref:`Sqlite3 Requires Single Quotes <sqlite3-requires-single-quotes>`

* 1.0.8

  * :ref:`Identical Consecutive Expression <identical-consecutive-expression>`
  * :ref:`Identical On Both Sides <identical-on-both-sides>`
  * :ref:`Mistaken Concatenation <mistaken-concatenation>`
  * :ref:`No Reference For Ternary <no-reference-for-ternary>`

* 1.0.7

  * :ref:`Not A Scalar Type <not-a-scalar-type>`
  * :ref:`Should Use array_filter() <should-use-array\_filter()>`

* 1.0.6

  * :ref:`Never Called Parameter <never-called-parameter>`
  * :ref:`Use Named Boolean In Argument Definition <use-named-boolean-in-argument-definition>`
  * :ref:`ext/igbinary <ext-igbinary>`

* 1.0.5

  * :ref:`Assigned In One Branch <assigned-in-one-branch>`
  * :ref:`Environment Variables <environment-variables>`
  * :ref:`Invalid Regex <invalid-regex>`
  * :ref:`Parent First <parent-first>`
  * :ref:`Same Variable Foreach <same-variable-foreach>`

* 1.0.4

  * :ref:`Argon2 Usage <argon2-usage>`
  * :ref:`Avoid set_error_handler $context Argument <avoid-set\_error\_handler-$context-argument>`
  * :ref:`Can't Count Non-Countable <can't-count-non-countable>`
  * :ref:`Crypto Usage <crypto-usage>`
  * :ref:`Dl() Usage <dl()-usage>`
  * :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
  * :ref:`Hash Will Use Objects <hash-will-use-objects>`
  * :ref:`Incoming Variable Index Inventory <incoming-variable-index-inventory>`
  * :ref:`Integer As Property <integer-as-property>`
  * :ref:`Maybe Missing New <maybe-missing-new>`
  * :ref:`No get_class() With Null <no-get\_class()-with-null>`
  * :ref:`Php 7.2 New Class <php-7.2-new-class>`
  * :ref:`Php 7.4 New Classes <php-7.4-new-classes>`
  * :ref:`Php 8.3 New Classes <php-8.3-new-classes>`
  * :ref:`Slice Arrays First <slice-arrays-first>`
  * :ref:`Type Array Index <type-array-index>`
  * :ref:`Unknown Pcre2 Option <unknown-pcre2-option>`
  * :ref:`Use List With Foreach <use-list-with-foreach>`
  * :ref:`Use PHP7 Encapsed Strings <use-php7-encapsed-strings>`
  * :ref:`ext/vips <ext-vips>`

* 1.0.3

  * :ref:`Ambiguous Static <ambiguous-static>`
  * :ref:`Drupal Usage <drupal-usage>`
  * :ref:`Fuel PHP Usage <fuel-php-usage>`
  * :ref:`Phalcon Usage <phalcon-usage>`

* 1.0.1

  * :ref:`Could Be Else <could-be-else>`
  * :ref:`Next Month Trap <next-month-trap>`
  * :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
  * :ref:`Simple Switch And Match <simple-switch-and-match>`
  * :ref:`Substring First <substring-first>`

* 0.12.17

  * :ref:`Is A Magic Property <is-a-magic-property>`

* 0.12.16

  * :ref:`Cookies Variables <cookies-variables>`
  * :ref:`Date Formats <date-formats>`
  * :ref:`Session Variables <session-variables>`
  * :ref:`Too Complex Expression <too-complex-expression>`
  * :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`

* 0.12.15

  * :ref:`Always Anchor Regex <always-anchor-regex>`
  * :ref:`Is Actually Zero <is-actually-zero>`
  * :ref:`Multiple Type Variable <multiple-type-variable>`
  * :ref:`Session Lazy Write <session-lazy-write>`

* 0.12.14

  * :ref:`Regex Inventory <regex-inventory>`
  * :ref:`Switch Fallthrough <switch-fallthrough>`
  * :ref:`Upload Filename Injection <upload-filename-injection>`

* 0.12.12

  * :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`
  * :ref:`ext/parle <ext-parle>`

* 0.12.11

  * :ref:`Could Be Protected Class Constant <could-be-protected-class-constant>`
  * :ref:`Could Be Protected Method <could-be-protected-method>`
  * :ref:`Method Could Be Private Method <method-could-be-private-method>`
  * :ref:`Method Used Below <method-used-below>`
  * :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`

* 0.12.10

  * :ref:`Constant Used Below <constant-used-below>`
  * :ref:`Could Be Private Class Constant <could-be-private-class-constant>`

* 0.12.9

  * :ref:`Shell Favorite <shell-favorite>`

* 0.12.8

  * :ref:`ext/fam <ext-fam>`
  * :ref:`ext/rdkafka <ext-rdkafka>`

* 0.12.7

  * :ref:`Should Use Foreach <should-use-foreach>`

* 0.12.5

  * :ref:`Logical To in_array <logical-to-in\_array>`
  * :ref:`No Substr Minus One <no-substr-minus-one>`

* 0.12.4

  * :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
  * :ref:`Avoid Concat In Loop <avoid-concat-in-loop>`
  * :ref:`Child Class Removes Type <child-class-removes-type>`
  * :ref:`Isset Multiple Arguments <isset-multiple-arguments>`
  * :ref:`Logical Operators Favorite <logical-operators-favorite>`
  * :ref:`No Magic Method With Array <no-magic-method-with-array>`
  * :ref:`Optional Parameter <optional-parameter>`
  * :ref:`ext/xattr <ext-xattr>`

* 0.12.3

  * :ref:`Group Use Trailing Comma <group-use-trailing-comma>`
  * :ref:`Mismatched Default Arguments <mismatched-default-arguments>`
  * :ref:`Mismatched Type <mismatched-type>`
  * :ref:`Scalar Or Object Property <scalar-or-object-property>`

* 0.12.2

  * :ref:`Mkdir Default <mkdir-default>`
  * :ref:`strict_types Preference <strict\_types-preference>`

* 0.12.1

  * :ref:`Const Or Define <const-or-define>`
  * :ref:`Declare strict_types Usage <declare-strict\_types-usage>`
  * :ref:`Encoding Usage <encoding-usage>`
  * :ref:`Mismatched Ternary Alternatives <mismatched-ternary-alternatives>`
  * :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
  * :ref:`Ticks Usage <ticks-usage>`

* 0.12.0

  * :ref:`Avoid Optional Properties <avoid-optional-properties>`
  * :ref:`Heredoc Delimiter <heredoc-delimiter>`
  * :ref:`Multiple Functions Declarations <multiple-functions-declarations>`
  * :ref:`Non Breakable Space In Names <non-breakable-space-in-names>`
  * :ref:`Swoole <swoole>`

* 0.11.8

  * :ref:`Cant Inherit Abstract Method <cant-inherit-abstract-method>`
  * :ref:`Codeigniter usage <codeigniter-usage>`
  * :ref:`Joomla usage <joomla-usage>`
  * :ref:`Laravel usage <laravel-usage>`
  * :ref:`Symfony usage <symfony-usage>`
  * :ref:`Use session_start() Options <use-session\_start()-options>`
  * :ref:`Wordpress usage <wordpress-usage>`
  * :ref:`Yii usage <yii-usage>`

* 0.11.7

  * :ref:`Forgotten Interface <forgotten-interface>`
  * :ref:`Order Of Declaration <order-of-declaration>`

* 0.11.6

  * :ref:`Concatenation Interpolation Consistence <concatenation-interpolation-consistence>`
  * :ref:`Could Make A Function <could-make-a-function>`
  * :ref:`Courier Anti-Pattern <courier-anti-pattern>`
  * :ref:`DI Cyclic Dependencies <di-cyclic-dependencies>`
  * :ref:`Dependency Injection <dependency-injection>`
  * :ref:`PSR-13 Usage <psr-13-usage>`
  * :ref:`PSR-16 Usage <psr-16-usage>`
  * :ref:`PSR-3 Usage <psr-3-usage>`
  * :ref:`PSR-6 Usage <psr-6-usage>`
  * :ref:`PSR-7 Usage <psr-7-usage>`
  * :ref:`Too Many Injections <too-many-injections>`
  * :ref:`ext/gender <ext-gender>`
  * :ref:`ext/judy <ext-judy>`

* 0.11.5

  * :ref:`Could Type <could-type>`
  * :ref:`Implemented Methods Must Be Public <implemented-methods-must-be-public>`
  * :ref:`Mixed Concat And Interpolation <mixed-concat-and-interpolation>`
  * :ref:`No Reference On Left Side <no-reference-on-left-side>`
  * :ref:`PSR-11 Usage <psr-11-usage>`
  * :ref:`ext/stats <ext-stats>`

* 0.11.4

  * :ref:`No Class As Type <no-class-as-type>`
  * :ref:`Use Browscap <use-browscap>`
  * :ref:`Use Debug <use-debug>`

* 0.11.3

  * :ref:`No Return Used <no-return-used>`
  * :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
  * :ref:`Try With Multiple Catch <try-with-multiple-catch>`
  * :ref:`ext/grpc <ext-grpc>`
  * :ref:`ext/sphinx <ext-sphinx>`
  * :ref:`ext/sqlite <ext-sqlite>`

* 0.11.2

  * :ref:`Alternative Syntax Consistence <alternative-syntax-consistence>`
  * :ref:`Randomly Sorted Arrays <randomly-sorted-arrays>`

* 0.11.1

  * :ref:`Difference Consistence <difference-consistence>`
  * :ref:`No Empty Regex <no-empty-regex>`

* 0.11.0

  * :ref:`Could Use str_repeat() <could-use-str\_repeat()>`
  * :ref:`Crc32() Might Be Negative <crc32()-might-be-negative>`
  * :ref:`Empty Final Element In Array <empty-final-element-in-array>`
  * :ref:`Strings With Strange Space <strings-with-strange-space>`
  * :ref:`Suspicious Comparison <suspicious-comparison>`

* 0.10.9

  * :ref:`Displays Text <displays-text>`
  * :ref:`Method Is Overwritten <method-is-overwritten>`
  * :ref:`No Class In Global <no-class-in-global>`
  * :ref:`Repeated Regex <repeated-regex>`

* 0.10.7

  * :ref:`Group Use Declaration <group-use-declaration>`
  * :ref:`Missing Cases In Switch <missing-cases-in-switch>`
  * :ref:`New Constants In PHP 7.2 <new-constants-in-php-7.2>`
  * :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`
  * :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

* 0.10.6

  * :ref:`Check All Types <check-all-types>`
  * :ref:`Do Not Cast To Int <do-not-cast-to-int>`
  * :ref:`Manipulates INF <manipulates-inf>`
  * :ref:`Manipulates NaN <manipulates-nan>`
  * :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
  * :ref:`Should Use SetCookie() <should-use-setcookie()>`
  * :ref:`Use Cookies <use-cookies>`

* 0.10.5

  * :ref:`Could Be Typed Callable <could-be-typed-callable>`
  * :ref:`Encoded Simple Letters <encoded-simple-letters>`
  * :ref:`Regex Delimiter <regex-delimiter>`
  * :ref:`Strange Name For Constants <strange-name-for-constants>`
  * :ref:`Strange Name For Variables <strange-name-for-variables>`
  * :ref:`Too Many Finds <too-many-finds>`

* 0.10.4

  * :ref:`No Need For Else <no-need-for-else>`
  * :ref:`Should Use session_regenerateid() <should-use-session\_regenerateid()>`
  * :ref:`ext/ds <ext-ds>`

* 0.10.3

  * :ref:`Multiple Alias Definitions Per File <multiple-alias-definitions-per-file>`
  * :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
  * :ref:`Used Once Property <used-once-property>`
  * :ref:`__DIR__ Then Slash <\_\_dir\_\_-then-slash>`
  * :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`

* 0.10.2

  * :ref:`Class Function Confusion <class-function-confusion>`
  * :ref:`Forgotten Thrown <forgotten-thrown>`
  * :ref:`Should Use array_column() <should-use-array\_column()>`
  * :ref:`ext/libsodium <ext-libsodium>`

* 0.10.1

  * :ref:`All strings <all-strings>`
  * :ref:`SQL queries <sql-queries>`
  * :ref:`Strange Names In Classes <strange-names-in-classes>`

* 0.10.0

  * :ref:`Error_Log() Usage <error\_log()-usage>`
  * :ref:`No Boolean As Default <no-boolean-as-default>`
  * :ref:`Raised Access Level <raised-access-level>`

* 0.9.9

  * :ref:`PHP 7.2 Deprecations <php-7.2-deprecations>`
  * :ref:`PHP 7.2 Removed Functions <php-7.2-removed-functions>`

* 0.9.8

  * :ref:`Assigned Twice <assigned-twice>`
  * :ref:`New Line Style <new-line-style>`
  * :ref:`New On Functioncall Or Identifier <new-on-functioncall-or-identifier>`

* 0.9.7

  * :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
  * :ref:`Could Be Protected Property <could-be-protected-property>`
  * :ref:`Long Arguments <long-arguments>`

* 0.9.6

  * :ref:`Avoid glob() Usage <avoid-glob()-usage>`
  * :ref:`Fetch One Row Format <fetch-one-row-format>`

* 0.9.5

  * :ref:`One Expression Brackets Consistency <one-expression-brackets-consistency>`
  * :ref:`Should Use Use Function <should-use-use-function>`
  * :ref:`ext/mongodb <ext-mongodb>`

* 0.9.4

  * :ref:`Class Should Be Final By Ocramius <class-should-be-final-by-ocramius>`
  * :ref:`String <string>`

* 0.9.3

  * :ref:`Close Tags Consistency <close-tags-consistency>`
  * :ref:`Unset() Or (unset) <unset()-or-(unset)>`

* 0.9.2

  * :ref:`$GLOBALS Or global <$globals-or-global>`
  * :ref:`Illegal Name For Method <illegal-name-for-method>`
  * :ref:`Too Many Local Variables <too-many-local-variables>`
  * :ref:`Use Composer Lock <use-composer-lock>`
  * :ref:`ext/nsapi <ext-nsapi>`

* 0.9.1

  * :ref:`Avoid Using stdClass <avoid-using-stdclass>`
  * :ref:`Avoid array_push() <avoid-array\_push()>`
  * :ref:`Invalid Octal In String <invalid-octal-in-string>`

* 0.9.0

  * :ref:`Getting Last Element <getting-last-element>`
  * :ref:`Rethrown Exceptions <rethrown-exceptions>`

* 0.8.9

  * :ref:`Array() / [  ] Consistence <array()---[--]-consistence>`
  * :ref:`Bail Out Early <bail-out-early>`
  * :ref:`Die Exit Consistence <die-exit-consistence>`
  * :ref:`Don't Change The Blind Var <don't-change-the-blind-var>`
  * :ref:`More Than One Level Of Indentation <more-than-one-level-of-indentation>`
  * :ref:`One Dot Or Object Operator Per Line <one-dot-or-object-operator-per-line>`
  * :ref:`PHP 7.1 Microseconds <php-7.1-microseconds>`
  * :ref:`Unitialized Properties <unitialized-properties>`
  * :ref:`Useless Check <useless-check>`

* 0.8.7

  * :ref:`Don't Echo Error <don't-echo-error>`
  * :ref:`No isset() With empty() <no-isset()-with-empty()>`
  * :ref:`Use \:\:Class Operator <use-class-operator>`
  * :ref:`Useless Type Casting <useless-type-casting>`
  * :ref:`ext/rar <ext-rar>`
  * :ref:`time() Vs strtotime() <time()-vs-strtotime()>`

* 0.8.6

  * :ref:`Drop Else After Return <drop-else-after-return>`
  * :ref:`Modernize Empty With Expression <modernize-empty-with-expression>`
  * :ref:`Use Positive Condition <use-positive-condition>`

* 0.8.5

  * :ref:`Should Use Ternary Operator <should-use-ternary-operator>`
  * :ref:`Unused Returned Value <unused-returned-value>`

* 0.8.4

  * :ref:`$HTTP_RAW_POST_DATA Usage <$http\_raw\_post\_data-usage>`
  * :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
  * :ref:`$this Is Not An Array <$this-is-not-an-array>`
  * :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
  * :ref:`** For Exponent <**-for-exponent>`
  * :ref:`@ Operator <@-operator>`
  * :ref:`Abstract Class Usage <abstract-class-usage>`
  * :ref:`Abstract Methods Usage <abstract-methods-usage>`
  * :ref:`Abstract Static Methods <abstract-static-methods>`
  * :ref:`Access Protected Structures <access-protected-structures>`
  * :ref:`Accessing Private <accessing-private>`
  * :ref:`Adding Zero <adding-zero>`
  * :ref:`Aliases <aliases>`
  * :ref:`All Uppercase Variables <all-uppercase-variables>`
  * :ref:`Already Parents Interface <already-parents-interface>`
  * :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
  * :ref:`Always Positive Comparison <always-positive-comparison>`
  * :ref:`Ambiguous Array Index <ambiguous-array-index>`
  * :ref:`Anonymous Classes <anonymous-classes>`
  * :ref:`Argument Should Be Typed <argument-should-be-typed>`
  * :ref:`Array Index <array-index>`
  * :ref:`Assertions <assertions>`
  * :ref:`Assign Default To Properties <assign-default-to-properties>`
  * :ref:`Autoloading <autoloading>`
  * :ref:`Avoid Parenthesis With Language Construct <avoid-parenthesis-with-language-construct>`
  * :ref:`Avoid Substr() One <avoid-substr()-one>`
  * :ref:`Avoid Those Hash Functions <avoid-those-hash-functions>`
  * :ref:`Avoid array_unique() <avoid-array\_unique()>`
  * :ref:`Avoid get_class() <avoid-get\_class()>`
  * :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`
  * :ref:`Bad Constants Names <bad-constants-names>`
  * :ref:`Binary Glossary <binary-glossary>`
  * :ref:`Blind Variables <blind-variables>`
  * :ref:`Bracketless Blocks <bracketless-blocks>`
  * :ref:`Break Outside Loop <break-outside-loop>`
  * :ref:`Break With 0 <break-with-0>`
  * :ref:`Break With Non Integer <break-with-non-integer>`
  * :ref:`Buried Assignation <buried-assignation>`
  * :ref:`Calltime Pass By Reference <calltime-pass-by-reference>`
  * :ref:`Can't Disable Class <can't-disable-class>`
  * :ref:`Can't Disable Function <can't-disable-function>`
  * :ref:`Can't Extend Final Class <can't-extend-final-class>`
  * :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
  * :ref:`Cast To Boolean <cast-to-boolean>`
  * :ref:`Cast Usage <cast-usage>`
  * :ref:`Catch Overwrite Variable <catch-overwrite-variable>`
  * :ref:`Caught Exceptions <caught-exceptions>`
  * :ref:`Caught Expressions <caught-expressions>`
  * :ref:`Class Const With Array <class-const-with-array>`
  * :ref:`Class Has Fluent Interface <class-has-fluent-interface>`
  * :ref:`Class Usage <class-usage>`
  * :ref:`Class, Interface, Enum Or Trait With Identical Names <class,-interface,-enum-or-trait-with-identical-names>`
  * :ref:`Classes Mutually Extending Each Other <classes-mutually-extending-each-other>`
  * :ref:`Classes Names <classes-names>`
  * :ref:`Clone Usage <clone-usage>`
  * :ref:`Closing Tags <closing-tags>`
  * :ref:`Closure May Use $this <closure-may-use-$this>`
  * :ref:`Closures Glossary <closures-glossary>`
  * :ref:`Coalesce <coalesce>`
  * :ref:`Common Alternatives <common-alternatives>`
  * :ref:`Compare Hash <compare-hash>`
  * :ref:`Compared Comparison <compared-comparison>`
  * :ref:`Composer Usage <composer-usage>`
  * :ref:`Composer's autoload <composer's-autoload>`
  * :ref:`Conditional Structures <conditional-structures>`
  * :ref:`Conditioned Constants <conditioned-constants>`
  * :ref:`Conditioned Function <conditioned-function>`
  * :ref:`Confusing Names <confusing-names>`
  * :ref:`Const With Array <const-with-array>`
  * :ref:`Constant Class <constant-class>`
  * :ref:`Constant Comparison <constant-comparison>`
  * :ref:`Constant Conditions <constant-conditions>`
  * :ref:`Constant Definition <constant-definition>`
  * :ref:`Constant Scalar Expression <constant-scalar-expression>`
  * :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
  * :ref:`Constants Created Outside Its Namespace <constants-created-outside-its-namespace>`
  * :ref:`Constants Names <constants-names>`
  * :ref:`Constants Usage <constants-usage>`
  * :ref:`Constants With Strange Names <constants-with-strange-names>`
  * :ref:`Constructors <constructors>`
  * :ref:`Continents <continents>`
  * :ref:`Could Be A Static Variable <could-be-a-static-variable>`
  * :ref:`Could Be Class Constant <could-be-class-constant>`
  * :ref:`Could Use Alias <could-use-alias>`
  * :ref:`Could Use Short Assignation <could-use-short-assignation>`
  * :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
  * :ref:`Could Use self <could-use-self>`
  * :ref:`Custom Class Usage <custom-class-usage>`
  * :ref:`Custom Constant Usage <custom-constant-usage>`
  * :ref:`Dangling Array References <dangling-array-references>`
  * :ref:`Deep Definitions <deep-definitions>`
  * :ref:`Define Constants With Array <define-constants-with-array>`
  * :ref:`Defined Class Constants <defined-class-constants>`
  * :ref:`Defined Exceptions <defined-exceptions>`
  * :ref:`Defined Parent MP <defined-parent-mp>`
  * :ref:`Defined Properties <defined-properties>`
  * :ref:`Defined static\:\: Or self\:\: <defined-static-or-self>`
  * :ref:`Definitions Only <definitions-only>`
  * :ref:`Dependant Trait <dependant-trait>`
  * :ref:`Deprecated PHP Functions <deprecated-php-functions>`
  * :ref:`Dereferencing String And Arrays <dereferencing-string-and-arrays>`
  * :ref:`Direct Injection <direct-injection>`
  * :ref:`Directives Usage <directives-usage>`
  * :ref:`Don't Change Incomings <don't-change-incomings>`
  * :ref:`Double Assignation <double-assignation>`
  * :ref:`Double Instructions <double-instructions>`
  * :ref:`Duplicate Calls <duplicate-calls>`
  * :ref:`Dynamic Calls <dynamic-calls>`
  * :ref:`Dynamic Class Constant <dynamic-class-constant>`
  * :ref:`Dynamic Classes <dynamic-classes>`
  * :ref:`Dynamic Code <dynamic-code>`
  * :ref:`Dynamic Function Call <dynamic-function-call>`
  * :ref:`Dynamic Methodcall <dynamic-methodcall>`
  * :ref:`Dynamic New <dynamic-new>`
  * :ref:`Dynamic Property <dynamic-property>`
  * :ref:`Dynamically Called Classes <dynamically-called-classes>`
  * :ref:`Echo Or Print <echo-or-print>`
  * :ref:`Echo With Concat <echo-with-concat>`
  * :ref:`Ellipsis Usage <ellipsis-usage>`
  * :ref:`Else If Versus Elseif <else-if-versus-elseif>`
  * :ref:`Else Usage <else-usage>`
  * :ref:`Email Addresses <email-addresses>`
  * :ref:`Empty Blocks <empty-blocks>`
  * :ref:`Empty Classes <empty-classes>`
  * :ref:`Empty Function <empty-function>`
  * :ref:`Empty Instructions <empty-instructions>`
  * :ref:`Empty Interfaces <empty-interfaces>`
  * :ref:`Empty List <empty-list>`
  * :ref:`Empty Namespace <empty-namespace>`
  * :ref:`Empty Slots In Arrays <empty-slots-in-arrays>`
  * :ref:`Empty Traits <empty-traits>`
  * :ref:`Empty Try Catch <empty-try-catch>`
  * :ref:`Empty With Expression <empty-with-expression>`
  * :ref:`Error Messages <error-messages>`
  * :ref:`Eval() Usage <eval()-usage>`
  * :ref:`Exception Order <exception-order>`
  * :ref:`Exit() Usage <exit()-usage>`
  * :ref:`Exit-like Methods <exit-like-methods>`
  * :ref:`Exponent Usage <exponent-usage>`
  * :ref:`External Config Files <external-config-files>`
  * :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
  * :ref:`File Is Component <file-is-component>`
  * :ref:`File Is Not Definitions Only <file-is-not-definitions-only>`
  * :ref:`File Uploads <file-uploads>`
  * :ref:`File Usage <file-usage>`
  * :ref:`Final Class Usage <final-class-usage>`
  * :ref:`Final Methods Usage <final-methods-usage>`
  * :ref:`Fopen Binary Mode <fopen-binary-mode>`
  * :ref:`For Using Functioncall <for-using-functioncall>`
  * :ref:`Foreach Don't Change Pointer <foreach-don't-change-pointer>`
  * :ref:`Foreach Needs Reference Array <foreach-needs-reference-array>`
  * :ref:`Foreach Reference Is Not Modified <foreach-reference-is-not-modified>`
  * :ref:`Foreach With list() <foreach-with-list()>`
  * :ref:`Forgotten Visibility <forgotten-visibility>`
  * :ref:`Forgotten Whitespace <forgotten-whitespace>`
  * :ref:`Fully Qualified Constants <fully-qualified-constants>`
  * :ref:`Function Called With Other Case Than Defined <function-called-with-other-case-than-defined>`
  * :ref:`Function Subscripting <function-subscripting>`
  * :ref:`Function Subscripting, Old Style <function-subscripting,-old-style>`
  * :ref:`Functioncall Is Global <functioncall-is-global>`
  * :ref:`Functions Glossary <functions-glossary>`
  * :ref:`Functions In Loop Calls <functions-in-loop-calls>`
  * :ref:`Functions Removed In PHP 5.4 <functions-removed-in-php-5.4>`
  * :ref:`Functions Removed In PHP 5.5 <functions-removed-in-php-5.5>`
  * :ref:`Functions Using Reference <functions-using-reference>`
  * :ref:`GPRC Aliases <gprc-aliases>`
  * :ref:`Global Code Only <global-code-only>`
  * :ref:`Global Import <global-import>`
  * :ref:`Global In Global <global-in-global>`
  * :ref:`Global Inside Loop <global-inside-loop>`
  * :ref:`Global Usage <global-usage>`
  * :ref:`Globals <globals>`
  * :ref:`Goto Names <goto-names>`
  * :ref:`HTTP Status Code <http-status-code>`
  * :ref:`Hardcoded Passwords <hardcoded-passwords>`
  * :ref:`Has Magic Method <has-magic-method>`
  * :ref:`Has Variable Arguments <has-variable-arguments>`
  * :ref:`Hash Algorithms <hash-algorithms>`
  * :ref:`Hash Algorithms Incompatible With PHP 5.3 <hash-algorithms-incompatible-with-php-5.3>`
  * :ref:`Hash Algorithms Incompatible With PHP 5.4/5.5 <hash-algorithms-incompatible-with-php-5.4-5.5>`
  * :ref:`Heredoc Delimiter Glossary <heredoc-delimiter-glossary>`
  * :ref:`Hexadecimal Glossary <hexadecimal-glossary>`
  * :ref:`Hexadecimal In String <hexadecimal-in-string>`
  * :ref:`Hidden Use Expression <hidden-use-expression>`
  * :ref:`Htmlentities Calls <htmlentities-calls>`
  * :ref:`Http Headers <http-headers>`
  * :ref:`Identical Conditions <identical-conditions>`
  * :ref:`If With Same Conditions <if-with-same-conditions>`
  * :ref:`Iffectations <iffectations>`
  * :ref:`Implements Is For Interface <implements-is-for-interface>`
  * :ref:`Implicit Global <implicit-global>`
  * :ref:`Implied If <implied-if>`
  * :ref:`Inclusions <inclusions>`
  * :ref:`Incompilable Files <incompilable-files>`
  * :ref:`Inconsistent Concatenation <inconsistent-concatenation>`
  * :ref:`Indices Are Int Or String <indices-are-int-or-string>`
  * :ref:`Indirect Injection <indirect-injection>`
  * :ref:`Instantiating Abstract Class <instantiating-abstract-class>`
  * :ref:`Interface Arguments <interface-arguments>`
  * :ref:`Interface Methods <interface-methods>`
  * :ref:`Interfaces Names <interfaces-names>`
  * :ref:`Interfaces Usage <interfaces-usage>`
  * :ref:`Internally Used Properties <internally-used-properties>`
  * :ref:`Internet Ports <internet-ports>`
  * :ref:`Interpolation <interpolation>`
  * :ref:`Invalid Constant Name <invalid-constant-name>`
  * :ref:`Is An Extension Class <is-an-extension-class>`
  * :ref:`Is An Extension Constant <is-an-extension-constant>`
  * :ref:`Is An Extension Function <is-an-extension-function>`
  * :ref:`Is An Extension Interface <is-an-extension-interface>`
  * :ref:`Is CLI Script <is-cli-script>`
  * :ref:`Is Extension Trait <is-extension-trait>`
  * :ref:`Is Global Constant <is-global-constant>`
  * :ref:`Is Interface Method <is-interface-method>`
  * :ref:`Is Library <is-library>`
  * :ref:`Is Not Class Family <is-not-class-family>`
  * :ref:`Is PHP Constant <is-php-constant>`
  * :ref:`Is Upper Family <is-upper-family>`
  * :ref:`Joining file() <joining-file()>`
  * :ref:`Labels <labels>`
  * :ref:`Linux Only Files <linux-only-files>`
  * :ref:`List Short Syntax <list-short-syntax>`
  * :ref:`List With Array Appends <list-with-array-appends>`
  * :ref:`List With Keys <list-with-keys>`
  * :ref:`Locally Unused Property <locally-unused-property>`
  * :ref:`Locally Used Property <locally-used-property>`
  * :ref:`Logical Mistakes <logical-mistakes>`
  * :ref:`Logical Should Use Symbolic Operators <logical-should-use-symbolic-operators>`
  * :ref:`Lone Blocks <lone-blocks>`
  * :ref:`Lost References <lost-references>`
  * :ref:`Magic Constant Usage <magic-constant-usage>`
  * :ref:`Magic Methods <magic-methods>`
  * :ref:`Magic Visibility <magic-visibility>`
  * :ref:`Mail Usage <mail-usage>`
  * :ref:`Make Global A Property <make-global-a-property>`
  * :ref:`Make One Call With Array <make-one-call-with-array>`
  * :ref:`Malformed Octal <malformed-octal>`
  * :ref:`Md5 Strings <md5-strings>`
  * :ref:`Method Has Fluent Interface <method-has-fluent-interface>`
  * :ref:`Method Is A Generator <method-is-a-generator>`
  * :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
  * :ref:`Methodcall On New <methodcall-on-new>`
  * :ref:`Methods Without Return <methods-without-return>`
  * :ref:`Mime Types <mime-types>`
  * :ref:`Mixed Keys In Array <mixed-keys-in-array>`
  * :ref:`Multidimensional Arrays <multidimensional-arrays>`
  * :ref:`Multiple Alias Definitions <multiple-alias-definitions>`
  * :ref:`Multiple Catch With Try <multiple-catch-with-try>`
  * :ref:`Multiple Class Declarations <multiple-class-declarations>`
  * :ref:`Multiple Classes In One File <multiple-classes-in-one-file>`
  * :ref:`Multiple Constant Definition <multiple-constant-definition>`
  * :ref:`Multiple Definition Of The Same Argument <multiple-definition-of-the-same-argument>`
  * :ref:`Multiple Exceptions Catch() <multiple-exceptions-catch()>`
  * :ref:`Multiple Identical Trait Or Interface <multiple-identical-trait-or-interface>`
  * :ref:`Multiple Index Definition <multiple-index-definition>`
  * :ref:`Multiple Returns <multiple-returns>`
  * :ref:`Multiples Identical Case <multiples-identical-case>`
  * :ref:`Multiply By One <multiply-by-one>`
  * :ref:`Must Return Methods <must-return-methods>`
  * :ref:`Namespaces <namespaces>`
  * :ref:`Namespaces Glossary <namespaces-glossary>`
  * :ref:`Native Alias Functions Usage <native-alias-functions-usage>`
  * :ref:`Negative Power <negative-power>`
  * :ref:`Nested Ifthen <nested-ifthen>`
  * :ref:`Nested Loops <nested-loops>`
  * :ref:`Nested Ternary <nested-ternary>`
  * :ref:`Never Used Properties <never-used-properties>`
  * :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`
  * :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`
  * :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`
  * :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`
  * :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
  * :ref:`No Choice <no-choice>`
  * :ref:`No Count With 0 <no-count-with-0>`
  * :ref:`No Direct Access <no-direct-access>`
  * :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
  * :ref:`No Direct Usage Of Returned Value <no-direct-usage-of-returned-value>`
  * :ref:`No Hardcoded Hash <no-hardcoded-hash>`
  * :ref:`No Hardcoded Ip <no-hardcoded-ip>`
  * :ref:`No Hardcoded Path <no-hardcoded-path>`
  * :ref:`No Hardcoded Port <no-hardcoded-port>`
  * :ref:`No List With String <no-list-with-string>`
  * :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`
  * :ref:`No Plus One <no-plus-one>`
  * :ref:`No Public Access <no-public-access>`
  * :ref:`No Real Comparison <no-real-comparison>`
  * :ref:`No Self Referencing Constant <no-self-referencing-constant>`
  * :ref:`No String With Append <no-string-with-append>`
  * :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
  * :ref:`Non Ascii Variables <non-ascii-variables>`
  * :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
  * :ref:`Non-constant Index In Array <non-constant-index-in-array>`
  * :ref:`Non-lowercase Keywords <non-lowercase-keywords>`
  * :ref:`Normal Methods <normal-methods>`
  * :ref:`Not Not <not-not>`
  * :ref:`Not Same Name As File <not-same-name-as-file>`
  * :ref:`Nowdoc Delimiter Glossary <nowdoc-delimiter-glossary>`
  * :ref:`Null On New <null-on-new>`
  * :ref:`Objects Don't Need References <objects-don't-need-references>`
  * :ref:`Octal Glossary <octal-glossary>`
  * :ref:`Old Style Constructor <old-style-constructor>`
  * :ref:`Old Style __autoload() <old-style-\_\_autoload()>`
  * :ref:`One Letter Functions <one-letter-functions>`
  * :ref:`One Object Operator Per Line <one-object-operator-per-line>`
  * :ref:`One Variable String <one-variable-string>`
  * :ref:`Only Static Methods Class <only-static-methods-class>`
  * :ref:`Only Variable Returned By Reference <only-variable-returned-by-reference>`
  * :ref:`Or Die <or-die>`
  * :ref:`Overwriting Variable <overwriting-variable>`
  * :ref:`Overwritten Class Constants <overwritten-class-constants>`
  * :ref:`Overwritten Exceptions <overwritten-exceptions>`
  * :ref:`Overwritten Literals <overwritten-literals>`
  * :ref:`PHP 7.0 New Classes <php-7.0-new-classes>`
  * :ref:`PHP 7.0 New Interfaces <php-7.0-new-interfaces>`
  * :ref:`PHP 7.0 Removed Directives <php-7.0-removed-directives>`
  * :ref:`PHP 7.0 Removed Functions <php-7.0-removed-functions>`
  * :ref:`PHP 7.1 Removed Directives <php-7.1-removed-directives>`
  * :ref:`PHP 7.2 Object Keyword <php-7.2-object-keyword>`
  * :ref:`PHP Alternative Syntax <php-alternative-syntax>`
  * :ref:`PHP Arrays Index <php-arrays-index>`
  * :ref:`PHP Bugfixes <php-bugfixes>`
  * :ref:`PHP Constant Usage <php-constant-usage>`
  * :ref:`PHP Echo Tag Usage <php-echo-tag-usage>`
  * :ref:`PHP Handlers Usage <php-handlers-usage>`
  * :ref:`PHP Interfaces <php-interfaces>`
  * :ref:`PHP Keywords As Names <php-keywords-as-names>`
  * :ref:`PHP Sapi <php-sapi>`
  * :ref:`PHP Variables <php-variables>`
  * :ref:`PHP5 Indirect Variable Expression <php5-indirect-variable-expression>`
  * :ref:`PHP7 Dirname <php7-dirname>`
  * :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
  * :ref:`Parenthesis As Parameter <parenthesis-as-parameter>`
  * :ref:`Pear Usage <pear-usage>`
  * :ref:`Perl Regex <perl-regex>`
  * :ref:`Php 7 Indirect Expression <php-7-indirect-expression>`
  * :ref:`Php 7.1 New Class <php-7.1-new-class>`
  * :ref:`Php7 Relaxed Keyword <php7-relaxed-keyword>`
  * :ref:`Phpinfo <phpinfo>`
  * :ref:`Pre-increment <pre-increment>`
  * :ref:`Preprocess Arrays <preprocess-arrays>`
  * :ref:`Preprocessable <preprocessable>`
  * :ref:`Print And Die <print-and-die>`
  * :ref:`Property Could Be Private <property-could-be-private>`
  * :ref:`Property Names <property-names>`
  * :ref:`Property Used Above <property-used-above>`
  * :ref:`Property Used Below <property-used-below>`
  * :ref:`Property Variable Confusion <property-variable-confusion>`
  * :ref:`Queries In Loops <queries-in-loops>`
  * :ref:`Random Without Try <random-without-try>`
  * :ref:`Real Functions <real-functions>`
  * :ref:`Real Variables <real-variables>`
  * :ref:`Recursive Functions <recursive-functions>`
  * :ref:`Redeclared PHP Functions <redeclared-php-functions>`
  * :ref:`Redefined Class Constants <redefined-class-constants>`
  * :ref:`Redefined Default <redefined-default>`
  * :ref:`Redefined Methods <redefined-methods>`
  * :ref:`Redefined PHP Traits <redefined-php-traits>`
  * :ref:`Redefined Property <redefined-property>`
  * :ref:`Register Globals <register-globals>`
  * :ref:`Relay Function <relay-function>`
  * :ref:`Repeated print() <repeated-print()>`
  * :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
  * :ref:`Resources Usage <resources-usage>`
  * :ref:`Results May Be Missing <results-may-be-missing>`
  * :ref:`Return True False <return-true-false>`
  * :ref:`Return Type Usage <return-type-usage>`
  * :ref:`Return With Parenthesis <return-with-parenthesis>`
  * :ref:`Return void  <return-void->`
  * :ref:`Safe Curl Options <safe-curl-options>`
  * :ref:`Same Conditions In Condition <same-conditions-in-condition>`
  * :ref:`Scalar Type Usage <scalar-type-usage>`
  * :ref:`Sensitive Argument <sensitive-argument>`
  * :ref:`Sequences In For <sequences-in-for>`
  * :ref:`Setlocale() Uses Constants <setlocale()-uses-constants>`
  * :ref:`Several Instructions On The Same Line <several-instructions-on-the-same-line>`
  * :ref:`Shell Usage <shell-usage>`
  * :ref:`Short Open Tags <short-open-tags>`
  * :ref:`Short Syntax For Arrays <short-syntax-for-arrays>`
  * :ref:`Should Be Single Quote <should-be-single-quote>`
  * :ref:`Should Chain Exception <should-chain-exception>`
  * :ref:`Should Make Alias <should-make-alias>`
  * :ref:`Should Typecast <should-typecast>`
  * :ref:`Should Use Coalesce <should-use-coalesce>`
  * :ref:`Should Use Existing Constants <should-use-existing-constants>`
  * :ref:`Should Use Local Class <should-use-local-class>`
  * :ref:`Should Use Prepared Statement <should-use-prepared-statement>`
  * :ref:`Silently Cast Integer <silently-cast-integer>`
  * :ref:`Simple Global Variable <simple-global-variable>`
  * :ref:`Simplify Regex <simplify-regex>`
  * :ref:`Slow Functions <slow-functions>`
  * :ref:`Special Integers <special-integers>`
  * :ref:`Static Loop <static-loop>`
  * :ref:`Static Methods <static-methods>`
  * :ref:`Static Methods Called From Object <static-methods-called-from-object>`
  * :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
  * :ref:`Static Properties <static-properties>`
  * :ref:`Static Variables <static-variables>`
  * :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
  * :ref:`String May Hold A Variable <string-may-hold-a-variable>`
  * :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
  * :ref:`Super Global Usage <super-global-usage>`
  * :ref:`Super Globals Contagion <super-globals-contagion>`
  * :ref:`Switch To Switch <switch-to-switch>`
  * :ref:`Switch With Too Many Default <switch-with-too-many-default>`
  * :ref:`Switch Without Default <switch-without-default>`
  * :ref:`Ternary In Concat <ternary-in-concat>`
  * :ref:`Test Class <test-class>`
  * :ref:`Throw <throw>`
  * :ref:`Throw Functioncall <throw-functioncall>`
  * :ref:`Throw In Destruct <throw-in-destruct>`
  * :ref:`Thrown Exceptions <thrown-exceptions>`
  * :ref:`Throws An Assignement <throws-an-assignement>`
  * :ref:`Timestamp Difference <timestamp-difference>`
  * :ref:`Too Many Children <too-many-children>`
  * :ref:`Trait Methods <trait-methods>`
  * :ref:`Trait Names <trait-names>`
  * :ref:`Traits Usage <traits-usage>`
  * :ref:`Trigger Errors <trigger-errors>`
  * :ref:`True False Inconsistant Case <true-false-inconsistant-case>`
  * :ref:`Try With Finally <try-with-finally>`
  * :ref:`Types <types>`
  * :ref:`URL List <url-list>`
  * :ref:`Uncaught Exceptions <uncaught-exceptions>`
  * :ref:`Unchecked Resources <unchecked-resources>`
  * :ref:`Undefined Caught Exceptions <undefined-caught-exceptions>`
  * :ref:`Undefined Class Constants <undefined-class-constants>`
  * :ref:`Undefined Classes <undefined-classes>`
  * :ref:`Undefined Constants <undefined-constants>`
  * :ref:`Undefined Functions <undefined-functions>`
  * :ref:`Undefined Interfaces <undefined-interfaces>`
  * :ref:`Undefined Parent <undefined-parent>`
  * :ref:`Undefined Properties <undefined-properties>`
  * :ref:`Undefined Trait <undefined-trait>`
  * :ref:`Undefined static\:\: Or self\:\: <undefined-static-or-self>`
  * :ref:`Unicode Blocks <unicode-blocks>`
  * :ref:`Unicode Escape Partial <unicode-escape-partial>`
  * :ref:`Unicode Escape Syntax <unicode-escape-syntax>`
  * :ref:`Unknown Directive Name <unknown-directive-name>`
  * :ref:`Unkown Regex Options <unkown-regex-options>`
  * :ref:`Unpreprocessed Values <unpreprocessed-values>`
  * :ref:`Unreachable Code <unreachable-code>`
  * :ref:`Unresolved Catch <unresolved-catch>`
  * :ref:`Unresolved Classes <unresolved-classes>`
  * :ref:`Unresolved Instanceof <unresolved-instanceof>`
  * :ref:`Unresolved Use <unresolved-use>`
  * :ref:`Unserialize Second Arg <unserialize-second-arg>`
  * :ref:`Unset Arguments <unset-arguments>`
  * :ref:`Unset In Foreach <unset-in-foreach>`
  * :ref:`Unthrown Exception <unthrown-exception>`
  * :ref:`Unused Classes <unused-classes>`
  * :ref:`Unused Constants <unused-constants>`
  * :ref:`Unused Functions <unused-functions>`
  * :ref:`Unused Global <unused-global>`
  * :ref:`Unused Interfaces <unused-interfaces>`
  * :ref:`Unused Label <unused-label>`
  * :ref:`Unused Methods <unused-methods>`
  * :ref:`Unused Parameter <unused-parameter>`
  * :ref:`Unused Private Methods <unused-private-methods>`
  * :ref:`Unused Private Properties <unused-private-properties>`
  * :ref:`Unused Protected Methods <unused-protected-methods>`
  * :ref:`Unused Traits <unused-traits>`
  * :ref:`Unused Use <unused-use>`
  * :ref:`Unusual Case For PHP Functions <unusual-case-for-php-functions>`
  * :ref:`Usage Of class_alias() <usage-of-class\_alias()>`
  * :ref:`Use === null <use-===-null>`
  * :ref:`Use Cli <use-cli>`
  * :ref:`Use Const And Functions <use-const-and-functions>`
  * :ref:`Use Constant As Arguments <use-constant-as-arguments>`
  * :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`
  * :ref:`Use Instanceof <use-instanceof>`
  * :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
  * :ref:`Use Nullable Type <use-nullable-type>`
  * :ref:`Use PHP Object API <use-php-object-api>`
  * :ref:`Use Pathinfo <use-pathinfo>`
  * :ref:`Use System Tmp <use-system-tmp>`
  * :ref:`Use This <use-this>`
  * :ref:`Use Web <use-web>`
  * :ref:`Use With Fully Qualified Name <use-with-fully-qualified-name>`
  * :ref:`Use const <use-const>`
  * :ref:`Use password_hash() <use-password\_hash()>`
  * :ref:`Use random_int() <use-random\_int()>`
  * :ref:`Used Classes <used-classes>`
  * :ref:`Used Functions <used-functions>`
  * :ref:`Used Interfaces <used-interfaces>`
  * :ref:`Used Methods <used-methods>`
  * :ref:`Used Once Variables (In Scope) <used-once-variables-(in-scope)>`
  * :ref:`Used Once Variables <used-once-variables>`
  * :ref:`Used Private Methods <used-private-methods>`
  * :ref:`Used Protected Method <used-protected-method>`
  * :ref:`Used Static Properties <used-static-properties>`
  * :ref:`Used Trait <used-trait>`
  * :ref:`Used Use <used-use>`
  * :ref:`Useless Abstract Class <useless-abstract-class>`
  * :ref:`Useless Brackets <useless-brackets>`
  * :ref:`Useless Constructor <useless-constructor>`
  * :ref:`Useless Final <useless-final>`
  * :ref:`Useless Global <useless-global>`
  * :ref:`Useless Instructions <useless-instructions>`
  * :ref:`Useless Interfaces <useless-interfaces>`
  * :ref:`Useless Parenthesis <useless-parenthesis>`
  * :ref:`Useless Return <useless-return>`
  * :ref:`Useless Switch <useless-switch>`
  * :ref:`Useless Unset <useless-unset>`
  * :ref:`Uses Default Values <uses-default-values>`
  * :ref:`Uses Environment <uses-environment>`
  * :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
  * :ref:`Using Short Tags <using-short-tags>`
  * :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`
  * :ref:`Var Keyword <var-keyword>`
  * :ref:`Variable Constants <variable-constants>`
  * :ref:`Variable References <variable-references>`
  * :ref:`Variable Variables <variable-variables>`
  * :ref:`Variables With Long Names <variables-with-long-names>`
  * :ref:`Variables With One Letter Names <variables-with-one-letter-names>`
  * :ref:`While(List() = Each()) <while(list()-=-each())>`
  * :ref:`Written Only Variables <written-only-variables>`
  * :ref:`Wrong Class Name Case <wrong-class-name-case>`
  * :ref:`Wrong Function Name Case <wrong-function-name-case>`
  * :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`
  * :ref:`Wrong Number Of Arguments In Methods <wrong-number-of-arguments-in-methods>`
  * :ref:`Wrong Optional Parameter <wrong-optional-parameter>`
  * :ref:`Wrong Parameter Type <wrong-parameter-type>`
  * :ref:`Wrong fopen() Mode <wrong-fopen()-mode>`
  * :ref:`Yield From Usage <yield-from-usage>`
  * :ref:`Yield Usage <yield-usage>`
  * :ref:`Yoda Comparison <yoda-comparison>`
  * :ref:`\:\:class <class>`
  * :ref:`__debugInfo() Usage <\_\_debuginfo()-usage>`
  * :ref:`__halt_compiler <\_\_halt\_compiler>`
  * :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
  * :ref:`crypt() Without Salt <crypt()-without-salt>`
  * :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`
  * :ref:`eval() Without Try <eval()-without-try>`
  * :ref:`ext/0mq <ext-0mq>`
  * :ref:`ext/amqp <ext-amqp>`
  * :ref:`ext/apache <ext-apache>`
  * :ref:`ext/apc <ext-apc>`
  * :ref:`ext/apcu <ext-apcu>`
  * :ref:`ext/array <ext-array>`
  * :ref:`ext/bcmath <ext-bcmath>`
  * :ref:`ext/bzip2 <ext-bzip2>`
  * :ref:`ext/calendar <ext-calendar>`
  * :ref:`ext/com <ext-com>`
  * :ref:`ext/crypto <ext-crypto>`
  * :ref:`ext/ctype <ext-ctype>`
  * :ref:`ext/curl <ext-curl>`
  * :ref:`ext/date <ext-date>`
  * :ref:`ext/dba <ext-dba>`
  * :ref:`ext/dio <ext-dio>`
  * :ref:`ext/dom <ext-dom>`
  * :ref:`ext/eaccelerator <ext-eaccelerator>`
  * :ref:`ext/enchant <ext-enchant>`
  * :ref:`ext/ev <ext-ev>`
  * :ref:`ext/event <ext-event>`
  * :ref:`ext/exif <ext-exif>`
  * :ref:`ext/expect <ext-expect>`
  * :ref:`ext/fann <ext-fann>`
  * :ref:`ext/file <ext-file>`
  * :ref:`ext/fileinfo <ext-fileinfo>`
  * :ref:`ext/filter <ext-filter>`
  * :ref:`ext/fpm <ext-fpm>`
  * :ref:`ext/ftp <ext-ftp>`
  * :ref:`ext/gd <ext-gd>`
  * :ref:`ext/gearman <ext-gearman>`
  * :ref:`ext/geoip <ext-geoip>`
  * :ref:`ext/gettext <ext-gettext>`
  * :ref:`ext/gmagick <ext-gmagick>`
  * :ref:`ext/gmp <ext-gmp>`
  * :ref:`ext/gnupgp <ext-gnupgp>`
  * :ref:`ext/hash <ext-hash>`
  * :ref:`ext/ibase <ext-ibase>`
  * :ref:`ext/iconv <ext-iconv>`
  * :ref:`ext/imagick <ext-imagick>`
  * :ref:`ext/imap <ext-imap>`
  * :ref:`ext/info <ext-info>`
  * :ref:`ext/inotify <ext-inotify>`
  * :ref:`ext/intl <ext-intl>`
  * :ref:`ext/json <ext-json>`
  * :ref:`ext/ldap <ext-ldap>`
  * :ref:`ext/libxml <ext-libxml>`
  * :ref:`ext/lua <ext-lua>`
  * :ref:`ext/mail <ext-mail>`
  * :ref:`ext/mailparse <ext-mailparse>`
  * :ref:`ext/math <ext-math>`
  * :ref:`ext/mbstring <ext-mbstring>`
  * :ref:`ext/mcrypt <ext-mcrypt>`
  * :ref:`ext/memcache <ext-memcache>`
  * :ref:`ext/memcached <ext-memcached>`
  * :ref:`ext/mongo <ext-mongo>`
  * :ref:`ext/mssql <ext-mssql>`
  * :ref:`ext/mysql <ext-mysql>`
  * :ref:`ext/mysqli <ext-mysqli>`
  * :ref:`ext/ncurses <ext-ncurses>`
  * :ref:`ext/newt <ext-newt>`
  * :ref:`ext/ob <ext-ob>`
  * :ref:`ext/oci8 <ext-oci8>`
  * :ref:`ext/odbc <ext-odbc>`
  * :ref:`ext/opcache <ext-opcache>`
  * :ref:`ext/openssl <ext-openssl>`
  * :ref:`ext/password <ext-password>`
  * :ref:`ext/pcntl <ext-pcntl>`
  * :ref:`ext/pcre <ext-pcre>`
  * :ref:`ext/pdo <ext-pdo>`
  * :ref:`ext/pecl_http <ext-pecl\_http>`
  * :ref:`ext/pgsql <ext-pgsql>`
  * :ref:`ext/phalcon <ext-phalcon>`
  * :ref:`ext/phar <ext-phar>`
  * :ref:`ext/php-ast <ext-php-ast>`
  * :ref:`ext/posix <ext-posix>`
  * :ref:`ext/protobuf <ext-protobuf>`
  * :ref:`ext/pspell <ext-pspell>`
  * :ref:`ext/readline <ext-readline>`
  * :ref:`ext/redis <ext-redis>`
  * :ref:`ext/reflection <ext-reflection>`
  * :ref:`ext/sem <ext-sem>`
  * :ref:`ext/session <ext-session>`
  * :ref:`ext/shmop <ext-shmop>`
  * :ref:`ext/simplexml <ext-simplexml>`
  * :ref:`ext/snmp <ext-snmp>`
  * :ref:`ext/soap <ext-soap>`
  * :ref:`ext/sockets <ext-sockets>`
  * :ref:`ext/spl <ext-spl>`
  * :ref:`ext/sqlite3 <ext-sqlite3>`
  * :ref:`ext/sqlsrv <ext-sqlsrv>`
  * :ref:`ext/ssh2 <ext-ssh2>`
  * :ref:`ext/standard <ext-standard>`
  * :ref:`ext/suhosin <ext-suhosin>`
  * :ref:`ext/tidy <ext-tidy>`
  * :ref:`ext/tokenizer <ext-tokenizer>`
  * :ref:`ext/tokyotyrant <ext-tokyotyrant>`
  * :ref:`ext/trader <ext-trader>`
  * :ref:`ext/v8js <ext-v8js>`
  * :ref:`ext/wddx <ext-wddx>`
  * :ref:`ext/xdebug <ext-xdebug>`
  * :ref:`ext/xdiff <ext-xdiff>`
  * :ref:`ext/xhprof <ext-xhprof>`
  * :ref:`ext/xml <ext-xml>`
  * :ref:`ext/xmlreader <ext-xmlreader>`
  * :ref:`ext/xmlrpc <ext-xmlrpc>`
  * :ref:`ext/xmlwriter <ext-xmlwriter>`
  * :ref:`ext/xsl <ext-xsl>`
  * :ref:`ext/yaml <ext-yaml>`
  * :ref:`ext/zip <ext-zip>`
  * :ref:`ext/zlib <ext-zlib>`
  * :ref:`func_get_arg() Modified Behavior <func\_get\_arg()-modified-behavior>`
  * :ref:`include_once() Usage <include\_once()-usage>`
  * :ref:`isset() With Constants <isset()-with-constants>`
  * :ref:`list() May Omit Variables <list()-may-omit-variables>`
  * :ref:`mcrypt_create_iv() With Default Values <mcrypt\_create\_iv()-with-default-values>`
  * :ref:`parse_str() Warning <parse\_str()-warning>`
  * :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`
  * :ref:`preg_replace With Option e <preg\_replace-with-option-e>`
  * :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`
  * :ref:`var_dump()... Usage <var\_dump()...-usage>`

* 0.8.3

  * :ref:`Variable Global <variable-global>`




Directory by PHP Function
-------------------------

+ `$`
    + `$HTTP_RAW_POST_DATA`

      + :ref:`$HTTP_RAW_POST_DATA Usage <$http\_raw\_post\_data-usage>`

    + `$_ENV`

      + :ref:`Incoming Variable Index Inventory <incoming-variable-index-inventory>`
      + :ref:`Incoming Variables <incoming-variables>`
      + :ref:`No Hardcoded Port <no-hardcoded-port>`
      + :ref:`Useless Global <useless-global>`

    + `$_GET`

      + :ref:`Always Anchor Regex <always-anchor-regex>`
      + :ref:`Avoid mb_dectect_encoding() <avoid-mb\_dectect\_encoding()>`
      + :ref:`Cast Usage <cast-usage>`
      + :ref:`Direct Injection <direct-injection>`
      + :ref:`Don't Change Incomings <don't-change-incomings>`
      + :ref:`Eval() Usage <eval()-usage>`
      + :ref:`Extensions/Exttaint <extensions-exttaint>`
      + :ref:`Favorite Casting Method <favorite-casting-method>`
      + :ref:`GPRC Aliases <gprc-aliases>`
      + :ref:`Implied If <implied-if>`
      + :ref:`Incoming Values <incoming-values>`
      + :ref:`Incoming Variable Index Inventory <incoming-variable-index-inventory>`
      + :ref:`Incoming Variables <incoming-variables>`
      + :ref:`Incompatible Types With Incoming Values <incompatible-types-with-incoming-values>`
      + :ref:`Indirect Injection <indirect-injection>`
      + :ref:`Insecure Integer Validation <insecure-integer-validation>`
      + :ref:`PHP Variables <php-variables>`
      + :ref:`Repeated Regex <repeated-regex>`
      + :ref:`Safe Phpvariables <safe-phpvariables>`
      + :ref:`Should Use Coalesce <should-use-coalesce>`
      + :ref:`Super Global Usage <super-global-usage>`
      + :ref:`Superglobals <superglobals>`
      + :ref:`Unvalidated Data Cached In Session <unvalidated-data-cached-in-session>`
      + :ref:`Use Web <use-web>`
      + :ref:`Useless Global <useless-global>`
      + :ref:`ext/gd <ext-gd>`
      + :ref:`ext/pcre <ext-pcre>`
      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

    + `$_POST`

      + :ref:`All Uppercase Variables <all-uppercase-variables>`
      + :ref:`Crypto Usage <crypto-usage>`
      + :ref:`Don't Change Incomings <don't-change-incomings>`
      + :ref:`GPRC Aliases <gprc-aliases>`
      + :ref:`Incoming Variable Index Inventory <incoming-variable-index-inventory>`
      + :ref:`Indirect Injection <indirect-injection>`
      + :ref:`PHP Keywords As Names <php-keywords-as-names>`
      + :ref:`Register Globals <register-globals>`
      + :ref:`Super Global Usage <super-global-usage>`
      + :ref:`Useless Global <useless-global>`

    + `$_REQUEST`

      + :ref:`GPRC Aliases <gprc-aliases>`
      + :ref:`Indirect Injection <indirect-injection>`
      + :ref:`Register Globals <register-globals>`
      + :ref:`Super Global Usage <super-global-usage>`
      + :ref:`Useless Global <useless-global>`

    + `$this`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`$this Is Not An Array <$this-is-not-an-array>`
      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Accessing Private <accessing-private>`
      + :ref:`Assign Default To Properties <assign-default-to-properties>`
      + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
      + :ref:`Avoid Optional Properties <avoid-optional-properties>`
      + :ref:`Avoid option arrays in constructors <avoid-option-arrays-in-constructors>`
      + :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
      + :ref:`Check On __Call Usage <check-on-\_\_call-usage>`
      + :ref:`Checks Property Existence <checks-property-existence>`
      + :ref:`Class Has Fluent Interface <class-has-fluent-interface>`
      + :ref:`Class Invasion <class-invasion>`
      + :ref:`Closure May Use $this <closure-may-use-$this>`
      + :ref:`Collect Property Usage <collect-property-usage>`
      + :ref:`Could Be Class Constant <could-be-class-constant>`
      + :ref:`Could Be Enumeration <could-be-enumeration>`
      + :ref:`Could Be Protected Method <could-be-protected-method>`
      + :ref:`Could Be Protected Property <could-be-protected-property>`
      + :ref:`Could Be Readonly Property <could-be-readonly-property>`
      + :ref:`Could Be Static Closure <could-be-static-closure>`
      + :ref:`Could Inject Parameter <could-inject-parameter>`
      + :ref:`Could Set Property Default <could-set-property-default>`
      + :ref:`Could Use Promoted Properties <could-use-promoted-properties>`
      + :ref:`Courier Anti-Pattern <courier-anti-pattern>`
      + :ref:`Create Default Values <create-default-values>`
      + :ref:`Create Magic Method <create-magic-method>`
      + :ref:`Create Magic Property <create-magic-property>`
      + :ref:`Cyclic References <cyclic-references>`
      + :ref:`DI Cyclic Dependencies <di-cyclic-dependencies>`
      + :ref:`Dependant Abstract Classes <dependant-abstract-classes>`
      + :ref:`Dependant Trait <dependant-trait>`
      + :ref:`Dependency Injection <dependency-injection>`
      + :ref:`Different Constructors <different-constructors>`
      + :ref:`Disconnected Classes <disconnected-classes>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Dynamic Self Calls <dynamic-self-calls>`
      + :ref:`Extends stdClass <extends-stdclass>`
      + :ref:`Extensions yar <extensions-yar>`
      + :ref:`Feast usage <feast-usage>`
      + :ref:`Getter And Setter <getter-and-setter>`
      + :ref:`Has Property Hook <has-property-hook>`
      + :ref:`Has Virtual Property <has-virtual-property>`
      + :ref:`Insufficient Property Type <insufficient-property-type>`
      + :ref:`Interfaces Don't Ensure Properties <interfaces-don't-ensure-properties>`
      + :ref:`Internally Used Properties <internally-used-properties>`
      + :ref:`Is A Magic Property <is-a-magic-property>`
      + :ref:`Law of Demeter <law-of-demeter>`
      + :ref:`Locally Unused Property <locally-unused-property>`
      + :ref:`Locally Used Property <locally-used-property>`
      + :ref:`Locally Used Property In Trait <locally-used-property-in-trait>`
      + :ref:`Long Preparation For Throw <long-preparation-for-throw>`
      + :ref:`Make Class Method Definition <make-class-method-definition>`
      + :ref:`Make Global A Property <make-global-a-property>`
      + :ref:`Make Magic Concrete <make-magic-concrete>`
      + :ref:`Memoize MagicCall <memoize-magiccall>`
      + :ref:`Method Could Be Private Method <method-could-be-private-method>`
      + :ref:`Method Could Be Static <method-could-be-static>`
      + :ref:`Method Has Fluent Interface <method-has-fluent-interface>`
      + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
      + :ref:`Method Property Confusion <method-property-confusion>`
      + :ref:`Method Used Below <method-used-below>`
      + :ref:`Minus One On Error <minus-one-on-error>`
      + :ref:`More Than One Level Of Indentation <more-than-one-level-of-indentation>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`Never Used Properties <never-used-properties>`
      + :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`No Readonly Assignation In Global <no-readonly-assignation-in-global>`
      + :ref:`Non Nullable Getters <non-nullable-getters>`
      + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
      + :ref:`Parent First <parent-first>`
      + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
      + :ref:`Property Could Be Local <property-could-be-local>`
      + :ref:`Property Could Be Private <property-could-be-private>`
      + :ref:`Property Export <property-export>`
      + :ref:`Property Invasion <property-invasion>`
      + :ref:`Property Used Above <property-used-above>`
      + :ref:`Property Used Below <property-used-below>`
      + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
      + :ref:`Property Variable Confusion <property-variable-confusion>`
      + :ref:`Public Reach To Private Methods <public-reach-to-private-methods>`
      + :ref:`Readonly Property Changed By Cloning <readonly-property-changed-by-cloning>`
      + :ref:`Redefined Default <redefined-default>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Set Aside Code <set-aside-code>`
      + :ref:`Set Class Property Definition With Type <set-class-property-definition-with-type>`
      + :ref:`Set Clone Link <set-clone-link>`
      + :ref:`Should Deep Clone <should-deep-clone>`
      + :ref:`Should Have Destructor <should-have-destructor>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Solve Trait Methods <solve-trait-methods>`
      + :ref:`Static Call With Self <static-call-with-self>`
      + :ref:`Static Methods Called From Object <static-methods-called-from-object>`
      + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
      + :ref:`Sylius usage <sylius-usage>`
      + :ref:`This Could Be Iterable <this-could-be-iterable>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`Too Complex Expression <too-complex-expression>`
      + :ref:`Too Many Injections <too-many-injections>`
      + :ref:`Typed Property Usage <typed-property-usage>`
      + :ref:`Typehints/CouldBeResource <typehints-couldberesource>`
      + :ref:`Unbinding Closures <unbinding-closures>`
      + :ref:`Undefined Methods <undefined-methods>`
      + :ref:`Undefined Properties <undefined-properties>`
      + :ref:`Unfinished Object <unfinished-object>`
      + :ref:`Uninitialized Property <uninitialized-property>`
      + :ref:`Union Type <union-type>`
      + :ref:`Unitialized Properties <unitialized-properties>`
      + :ref:`Untyped No Default Properties <untyped-no-default-properties>`
      + :ref:`Unused Methods <unused-methods>`
      + :ref:`Unused Private Methods <unused-private-methods>`
      + :ref:`Unused Private Properties <unused-private-properties>`
      + :ref:`Unused Protected Methods <unused-protected-methods>`
      + :ref:`Unused Trait In Class <unused-trait-in-class>`
      + :ref:`Use This <use-this>`
      + :ref:`Used Methods <used-methods>`
      + :ref:`Used Once Property <used-once-property>`
      + :ref:`Used Once Variables <used-once-variables>`
      + :ref:`Used Private Methods <used-private-methods>`
      + :ref:`Used Protected Method <used-protected-method>`
      + :ref:`Used Static Properties <used-static-properties>`
      + :ref:`Useless Assignation Of Promoted Property <useless-assignation-of-promoted-property>`
      + :ref:`Useless Type <useless-type>`
      + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
      + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`
      + :ref:`Wrong Number Of Arguments In Methods <wrong-number-of-arguments-in-methods>`
      + :ref:`Wrong Typed Property Default <wrong-typed-property-default>`
      + :ref:`__debugInfo() Usage <\_\_debuginfo()-usage>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`var_dump()... Usage <var\_dump()...-usage>`


+ `*`
    + `**`

      + :ref:`** For Exponent <**-for-exponent>`
      + :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
      + :ref:`Drupal Usage <drupal-usage>`
      + :ref:`Exponent Usage <exponent-usage>`
      + :ref:`Extensions yar <extensions-yar>`
      + :ref:`Laravel usage <laravel-usage>`
      + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
      + :ref:`Modify Immutable <modify-immutable>`
      + :ref:`Negative Power <negative-power>`
      + :ref:`No Named Parameters <no-named-parameters>`
      + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
      + :ref:`Symfony usage <symfony-usage>`
      + :ref:`Unused Traits <unused-traits>`
      + :ref:`Using Deprecated Method <using-deprecated-method>`
      + :ref:`ext/bcmath <ext-bcmath>`
      + :ref:`ext/decimal <ext-decimal>`
      + :ref:`ext/reflection <ext-reflection>`
      + :ref:`ext/sdl <ext-sdl>`
      + :ref:`is_a() Versus instanceof <is\_a()-versus-instanceof>`


+ `.`
    + `...`

      + :ref:`Ambiguous Static <ambiguous-static>`
      + :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
      + :ref:`Check On __Call Usage <check-on-\_\_call-usage>`
      + :ref:`Collect Vendor Structures <collect-vendor-structures>`
      + :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
      + :ref:`Don't Be Too Manual <don't-be-too-manual>`
      + :ref:`Ellipsis Merge <ellipsis-merge>`
      + :ref:`Ellipsis Usage <ellipsis-usage>`
      + :ref:`File Usage <file-usage>`
      + :ref:`First Class Callable <first-class-callable>`
      + :ref:`Fossilized Methods List <fossilized-methods-list>`
      + :ref:`Iffectations <iffectations>`
      + :ref:`Method Has Fluent Interface <method-has-fluent-interface>`
      + :ref:`Method Is A Generator <method-is-a-generator>`
      + :ref:`Misused Yield <misused-yield>`
      + :ref:`Multiple Definition Of The Same Argument <multiple-definition-of-the-same-argument>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`Named Arguments And Variadic <named-arguments-and-variadic>`
      + :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
      + :ref:`No Spread For Hash <no-spread-for-hash>`
      + :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
      + :ref:`PHP 8.0 Types <php-8.0-types>`
      + :ref:`PHP 80 Named Parameter Variadic <php-80-named-parameter-variadic>`
      + :ref:`Pack Format Inventory <pack-format-inventory>`
      + :ref:`Repeated Regex <repeated-regex>`
      + :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Signature Trailing Comma <signature-trailing-comma>`
      + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`
      + :ref:`Spread Operator For Array <spread-operator-for-array>`
      + :ref:`Static Properties <static-properties>`
      + :ref:`Type Dodging <type-dodging>`
      + :ref:`Unknown Parameter Name <unknown-parameter-name>`
      + :ref:`Unpacking Inside Arrays <unpacking-inside-arrays>`
      + :ref:`Use PHP Attributes <use-php-attributes>`
      + :ref:`Used Once Property <used-once-property>`
      + :ref:`Useless Instructions <useless-instructions>`
      + :ref:`Yii usage <yii-usage>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`
      + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`
      + :ref:`ext/ffi <ext-ffi>`
      + :ref:`ext/ldap <ext-ldap>`
      + :ref:`ext/phalcon <ext-phalcon>`
      + :ref:`ext/protobuf <ext-protobuf>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/xattr <ext-xattr>`


+ `@`
    + `@`

      + :ref:`@ Operator <@-operator>`
      + :ref:`Email Addresses <email-addresses>`
      + :ref:`Invalid Octal In String <invalid-octal-in-string>`
      + :ref:`Too Complex Expression <too-complex-expression>`
      + :ref:`Useless Instructions <useless-instructions>`
      + :ref:`ext/mssql <ext-mssql>`
      + :ref:`ext/yaml <ext-yaml>`
      + :ref:`Remove Noscream @ <remove-noscream-@>`


+ `A`
    + `AF_INET`

      + :ref:`ext/sockets <ext-sockets>`

    + `ArgumentCountError`

      + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

    + `ArrayAccess`

      + :ref:`$this Is Not An Array <$this-is-not-an-array>`
      + :ref:`Is An Extension Interface <is-an-extension-interface>`
      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `ArrayIterator`

      + :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`

    + `ArrayObject`

      + :ref:`Avoid get_object_vars() <avoid-get\_object\_vars()>`

    + `Array_search()`

      + :ref:`Find Key Directly <find-key-directly>`

    + `Array_slice()`

      + :ref:`Use array_slice() <use-array\_slice()>`

    + `Attribute`

      + :ref:`Friend Attribute <friend-attribute>`
      + :ref:`Missing Attribute Attribute <missing-attribute-attribute>`
      + :ref:`PHP Native Attributes <php-native-attributes>`
      + :ref:`Wrong Attribute Configuration <wrong-attribute-configuration>`

    + `abs()`

      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`No Real Comparison <no-real-comparison>`

    + `addslashes()`

      + :ref:`Filter To add_slashes() <filter-to-add\_slashes()>`

    + `array()`

      + :ref:`Append And Assign Arrays <append-and-assign-arrays>`
      + :ref:`Array With String Initialization <array-with-string-initialization>`
      + :ref:`Array() / [  ] Consistence <array()---[--]-consistence>`
      + :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
      + :ref:`Avoid Concat In Loop <avoid-concat-in-loop>`
      + :ref:`Class Const With Array <class-const-with-array>`
      + :ref:`Confusing Names <confusing-names>`
      + :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
      + :ref:`Could Use array_unique <could-use-array\_unique>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Empty Final Element In Array <empty-final-element-in-array>`
      + :ref:`Group Use Trailing Comma <group-use-trailing-comma>`
      + :ref:`Invalid Cast <invalid-cast>`
      + :ref:`List With Array Appends <list-with-array-appends>`
      + :ref:`Memoize MagicCall <memoize-magiccall>`
      + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
      + :ref:`Mismatched Default Arguments <mismatched-default-arguments>`
      + :ref:`More Than One Level Of Indentation <more-than-one-level-of-indentation>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
      + :ref:`PSR-3 Usage <psr-3-usage>`
      + :ref:`Preprocess Arrays <preprocess-arrays>`
      + :ref:`Short Syntax For Arrays <short-syntax-for-arrays>`
      + :ref:`Should Use array_column() <should-use-array\_column()>`
      + :ref:`Should Use array_filter() <should-use-array\_filter()>`
      + :ref:`Too Many Array Dimensions <too-many-array-dimensions>`
      + :ref:`Too Many Native Calls <too-many-native-calls>`
      + :ref:`Useless Type <useless-type>`
      + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`
      + :ref:`ext/xml <ext-xml>`
      + :ref:`Array To Bracket <array-to-bracket>`

    + `array_change_key_case()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `array_chunk()`

      + :ref:`Use Array Functions <use-array-functions>`

    + `array_column()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`
      + :ref:`Should Use array_column() <should-use-array\_column()>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `array_combine()`

      + :ref:`Could Be array_combine() <could-be-array\_combine()>`

    + `array_count_values()`

      + :ref:`Avoid array_unique() <avoid-array\_unique()>`
      + :ref:`Slow Functions <slow-functions>`

    + `array_diff()`

      + :ref:`Slow Functions <slow-functions>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`

    + `array_diff_assoc()`

      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`

    + `array_diff_key()`

      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`

    + `array_diff_uassoc()`

      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`

    + `array_fill()`

      + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
      + :ref:`Could Not Type <could-not-type>`

    + `array_fill_keys()`

      + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
      + :ref:`Could Use array_fill_keys <could-use-array\_fill\_keys>`

    + `array_filter()`

      + :ref:`Should Use array_filter() <should-use-array\_filter()>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `array_flip()`

      + :ref:`Avoid array_unique() <avoid-array\_unique()>`
      + :ref:`Double array_flip() <double-array\_flip()>`
      + :ref:`Slow Functions <slow-functions>`

    + `array_intersect()`

      + :ref:`Slow Functions <slow-functions>`

    + `array_is_list()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `array_key_exists()`

      + :ref:`Always Use Function With array_key_exists() <always-use-function-with-array\_key\_exists()>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`
      + :ref:`array_key_exists() Works On Arrays <array\_key\_exists()-works-on-arrays>`
      + :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`

    + `array_key_last()`

      + :ref:`Getting Last Element <getting-last-element>`

    + `array_keys()`

      + :ref:`Avoid array_unique() <avoid-array\_unique()>`
      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Find Key Directly <find-key-directly>`
      + :ref:`Getting Last Element <getting-last-element>`
      + :ref:`Searching For Multiple Keys <searching-for-multiple-keys>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`

    + `array_map()`

      + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
      + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
      + :ref:`Callback Function Needs Return <callback-function-needs-return>`
      + :ref:`Could Be Typed Callable <could-be-typed-callable>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `array_merge()`

      + :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
      + :ref:`Could Use array_sum() <could-use-array\_sum()>`
      + :ref:`Ellipsis Merge <ellipsis-merge>`
      + :ref:`Multiple Similar Calls <multiple-similar-calls>`
      + :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
      + :ref:`Unknown Parameter Name <unknown-parameter-name>`
      + :ref:`Unpacking Inside Arrays <unpacking-inside-arrays>`
      + :ref:`Use Array Functions <use-array-functions>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`
      + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`

    + `array_merge_recursive()`

      + :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
      + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`
      + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`

    + `array_multisort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `array_pad()`

      + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`

    + `array_product()`

      + :ref:`Use Array Functions <use-array-functions>`

    + `array_push()`

      + :ref:`Avoid array_push() <avoid-array\_push()>`
      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `array_replace()`

      + :ref:`Useless Instructions <useless-instructions>`

    + `array_search()`

      + :ref:`Find Key Directly <find-key-directly>`
      + :ref:`Searching For Multiple Keys <searching-for-multiple-keys>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `array_shift()`

      + :ref:`Should Use Foreach <should-use-foreach>`

    + `array_slice()`

      + :ref:`Use Array Functions <use-array-functions>`

    + `array_splice()`

      + :ref:`Use array_slice() <use-array\_slice()>`

    + `array_sum()`

      + :ref:`Avoid Concat In Loop <avoid-concat-in-loop>`
      + :ref:`Callback Function Needs Return <callback-function-needs-return>`
      + :ref:`Could Use array_sum() <could-use-array\_sum()>`
      + :ref:`For Using Functioncall <for-using-functioncall>`
      + :ref:`Static Loop <static-loop>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `array_udiff()`

      + :ref:`Slow Functions <slow-functions>`

    + `array_uintersect()`

      + :ref:`Slow Functions <slow-functions>`

    + `array_unique()`

      + :ref:`Avoid array_unique() <avoid-array\_unique()>`
      + :ref:`Could Use array_unique <could-use-array\_unique>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `array_unshift()`

      + :ref:`Slow Functions <slow-functions>`

    + `array_values()`

      + :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`
      + :ref:`ext/teds <ext-teds>`

    + `array_walk()`

      + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
      + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `arsort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `asort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `assert()`

      + :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
      + :ref:`PHP 7.2 Deprecations <php-7.2-deprecations>`

    + `attribute`

      + :ref:`Deprecated Attribute <deprecated-attribute>`
      + :ref:`Exit-like Methods <exit-like-methods>`
      + :ref:`Friend Attribute <friend-attribute>`
      + :ref:`Injectable Version <injectable-version>`
      + :ref:`Is PHP Structure <is-php-structure>`
      + :ref:`Method Is Overwritten <method-is-overwritten>`
      + :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
      + :ref:`Missing Attribute Attribute <missing-attribute-attribute>`
      + :ref:`Missing Overriden Method <missing-overriden-method>`
      + :ref:`Modify Immutable <modify-immutable>`
      + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
      + :ref:`MustUseResult <mustuseresult>`
      + :ref:`Nested Attributes <nested-attributes>`
      + :ref:`Override Attribute <override-attribute>`
      + :ref:`PHP Native Attributes <php-native-attributes>`
      + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`
      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
      + :ref:`Useless Override Attribute <useless-override-attribute>`
      + :ref:`Using Deprecated Feature <using-deprecated-feature>`
      + :ref:`Using Deprecated Method <using-deprecated-method>`
      + :ref:`Wrong Attribute Configuration <wrong-attribute-configuration>`
      + :ref:`IsExt <isext>`
      + :ref:`IsPHP <isphp>`
      + :ref:`IsStub <isstub>`


+ `B`
    + `Break`

      + :ref:`Break With 0 <break-with-0>`

    + `basename()`

      + :ref:`Use Basename Suffix <use-basename-suffix>`
      + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

    + `boolval()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `break`

      + :ref:`Break Outside Loop <break-outside-loop>`
      + :ref:`Break With 0 <break-with-0>`
      + :ref:`Break With Non Integer <break-with-non-integer>`
      + :ref:`Continue Is For Loop <continue-is-for-loop>`
      + :ref:`Could Use Match <could-use-match>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Identical Case In Switch <identical-case-in-switch>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Long Arguments <long-arguments>`
      + :ref:`Long Preparation For Throw <long-preparation-for-throw>`
      + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
      + :ref:`Missing Cases In Switch <missing-cases-in-switch>`
      + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
      + :ref:`Multiples Identical Case <multiples-identical-case>`
      + :ref:`Negative Start Index In Array <negative-start-index-in-array>`
      + :ref:`No Empty String With explode() <no-empty-string-with-explode()>`
      + :ref:`No Need For Else <no-need-for-else>`
      + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Several Instructions On The Same Line <several-instructions-on-the-same-line>`
      + :ref:`Simple Switch And Match <simple-switch-and-match>`
      + :ref:`Switch Fallthrough <switch-fallthrough>`
      + :ref:`Switch To Switch <switch-to-switch>`
      + :ref:`Switch With Too Many Default <switch-with-too-many-default>`
      + :ref:`Switch Without Default <switch-without-default>`
      + :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`
      + :ref:`Unreachable Code <unreachable-code>`
      + :ref:`Use The Case Value <use-the-case-value>`
      + :ref:`Useless Switch <useless-switch>`
      + :ref:`ext/expect <ext-expect>`
      + :ref:`ext/gearman <ext-gearman>`
      + :ref:`ext/gender <ext-gender>`
      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/pcntl <ext-pcntl>`
      + :ref:`ext/tokenizer <ext-tokenizer>`
      + :ref:`Switch To Match <switch-to-match>`


+ `C`
    + `CAL_GREGORIAN`

      + :ref:`ext/calendar <ext-calendar>`

    + `COM`

      + :ref:`ext/com <ext-com>`

    + `COUNT_NORMAL`

      + :ref:`Use Recursive count() <use-recursive-count()>`

    + `COUNT_RECURSIVE`

      + :ref:`Use Recursive count() <use-recursive-count()>`

    + `CURLOPT_FILE`

      + :ref:`ext/curl <ext-curl>`

    + `CURLOPT_HEADER`

      + :ref:`ext/curl <ext-curl>`

    + `CURLOPT_SSL_VERIFYPEER`

      + :ref:`Safe Curl Options <safe-curl-options>`

    + `CURLOPT_URL`

      + :ref:`Safe Curl Options <safe-curl-options>`

    + `CURLPIPE_HTTP1`

      + :ref:`PHP 7.4 Constant Deprecation <php-7.4-constant-deprecation>`

    + `CURLVERSION_NOW`

      + :ref:`curl_version() Has No Argument <curl\_version()-has-no-argument>`

    + `Closure`

      + :ref:`Argument Should Be Typed <argument-should-be-typed>`
      + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
      + :ref:`Could Be Static Closure <could-be-static-closure>`
      + :ref:`Follow Closure Definition <follow-closure-definition>`
      + :ref:`Unused Inherited Variable In Closure <unused-inherited-variable-in-closure>`

    + `Collator`

      + :ref:`ext/intl <ext-intl>`

    + `Compact()`

      + :ref:`Could Use Compact <could-use-compact>`
      + :ref:`Nonexistent Variable In compact() <nonexistent-variable-in-compact()>`

    + `Connection`

      + :ref:`No Hardcoded Port <no-hardcoded-port>`
      + :ref:`Stomp <stomp>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/ssh2 <ext-ssh2>`

    + `Count()`

      + :ref:`Can't Count Non-Countable <can't-count-non-countable>`
      + :ref:`Uses Default Values <uses-default-values>`

    + `Countable`

      + :ref:`Can't Count Non-Countable <can't-count-non-countable>`
      + :ref:`Count() Is Not Negative <count()-is-not-negative>`
      + :ref:`PHP Interfaces <php-interfaces>`
      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
      + :ref:`Use is_countable <use-is\_countable>`

    + `call_user_func()`

      + :ref:`Should Use Operator <should-use-operator>`

    + `ceil()`

      + :ref:`Do Not Cast To Int <do-not-cast-to-int>`

    + `chdir()`

      + :ref:`No Hardcoded Path <no-hardcoded-path>`

    + `chmod()`

      + :ref:`Keep Files Access Restricted <keep-files-access-restricted>`

    + `chr()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Should Preprocess Chr() <should-preprocess-chr()>`
      + :ref:`Should Use Operator <should-use-operator>`

    + `chroot()`

      + :ref:`No Hardcoded Path <no-hardcoded-path>`

    + `class_alias()`

      + :ref:`Set class_alias() Definition <set-class\_alias()-definition>`
      + :ref:`Use class_alias() <use-class\_alias()>`
      + :ref:`class_alias() Supports Internal Classes <class\_alias()-supports-internal-classes>`

    + `class_exists()`

      + :ref:`Undefined static ::class <undefined-static-class>`

    + `class_uses()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `cli_get_process_title()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `cli_set_process_title()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `closure`

      + :ref:`Avoid set_error_handler $context Argument <avoid-set\_error\_handler-$context-argument>`
      + :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
      + :ref:`Class Without Parent <class-without-parent>`
      + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
      + :ref:`Closure May Use $this <closure-may-use-$this>`
      + :ref:`Closures Glossary <closures-glossary>`
      + :ref:`Collect Parameter Counts <collect-parameter-counts>`
      + :ref:`Could Be Static Closure <could-be-static-closure>`
      + :ref:`Could Be Typed Callable <could-be-typed-callable>`
      + :ref:`First Class Callable <first-class-callable>`
      + :ref:`Follow Closure Definition <follow-closure-definition>`
      + :ref:`Function With Dynamic Code <function-with-dynamic-code>`
      + :ref:`Functions Glossary <functions-glossary>`
      + :ref:`Hidden Use Expression <hidden-use-expression>`
      + :ref:`Identity <identity>`
      + :ref:`Multiple Definition Of The Same Argument <multiple-definition-of-the-same-argument>`
      + :ref:`Multiple Identical Closure <multiple-identical-closure>`
      + :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
      + :ref:`No Static Variable In A Method <no-static-variable-in-a-method>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Pre-Calculate Use <pre-calculate-use>`
      + :ref:`Real Functions <real-functions>`
      + :ref:`Semantic Typing <semantic-typing>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Should Use array_filter() <should-use-array\_filter()>`
      + :ref:`Static Variables <static-variables>`
      + :ref:`Unbinding Closures <unbinding-closures>`
      + :ref:`Unused Inherited Variable In Closure <unused-inherited-variable-in-closure>`
      + :ref:`Use Closure Trailing Comma <use-closure-trailing-comma>`
      + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
      + :ref:`Using Deprecated Feature <using-deprecated-feature>`
      + :ref:`preg_replace With Option e <preg\_replace-with-option-e>`
      + :ref:`Make Static Closures And Arrow Functions <make-static-closures-and-arrow-functions>`

    + `collator_compare()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `collator_get_sort_key()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `com`

      + :ref:`Abstract Away <abstract-away>`
      + :ref:`Don't Unset Properties <don't-unset-properties>`
      + :ref:`Extensions yar <extensions-yar>`
      + :ref:`Http Headers <http-headers>`
      + :ref:`If Then Return Favorite <if-then-return-favorite>`
      + :ref:`Immutable Signature <immutable-signature>`
      + :ref:`Insufficient Type <insufficient-type>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Mail Usage <mail-usage>`
      + :ref:`Mismatch Parameter Name <mismatch-parameter-name>`
      + :ref:`No Append On Source <no-append-on-source>`
      + :ref:`No Hardcoded Port <no-hardcoded-port>`
      + :ref:`No Net For Xml Load <no-net-for-xml-load>`
      + :ref:`No Object As Index <no-object-as-index>`
      + :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`
      + :ref:`Not A Scalar Type <not-a-scalar-type>`
      + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`
      + :ref:`Path lists <path-lists>`
      + :ref:`Session Lazy Write <session-lazy-write>`
      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Should Use Use Function <should-use-use-function>`
      + :ref:`Should Yield With Key <should-yield-with-key>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Static Inclusions <static-inclusions>`
      + :ref:`Suspicious Comparison <suspicious-comparison>`
      + :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
      + :ref:`URL List <url-list>`
      + :ref:`Use Cookies <use-cookies>`
      + :ref:`Use Debug <use-debug>`
      + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`
      + :ref:`Wordpress usage <wordpress-usage>`
      + :ref:`ext/0mq <ext-0mq>`
      + :ref:`ext/amqp <ext-amqp>`
      + :ref:`ext/curl <ext-curl>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/fam <ext-fam>`
      + :ref:`ext/filter <ext-filter>`
      + :ref:`ext/geoip <ext-geoip>`
      + :ref:`ext/grpc <ext-grpc>`
      + :ref:`ext/libsodium <ext-libsodium>`
      + :ref:`ext/mail <ext-mail>`
      + :ref:`ext/mongodb <ext-mongodb>`
      + :ref:`ext/pecl_http <ext-pecl\_http>`
      + :ref:`ext/phalcon <ext-phalcon>`
      + :ref:`ext/protobuf <ext-protobuf>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/ssh2 <ext-ssh2>`
      + :ref:`ext/xmlrpc <ext-xmlrpc>`
      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`
      + :ref:`php-cs-fixable <php-cs-fixable>`
      + :ref:`report-Ambassador <report-ambassador>`
      + :ref:`report-BeautyCanon <report-beautycanon>`
      + :ref:`report-ClassReview <report-classreview>`
      + :ref:`report-Classes dependendies HTML <report-classes-dependendies-html>`
      + :ref:`report-Clustergrammer <report-clustergrammer>`
      + :ref:`report-Code Flower <report-code-flower>`
      + :ref:`report-Code Sniffer <report-code-sniffer>`
      + :ref:`report-CompatibilityPHP56 <report-compatibilityphp56>`
      + :ref:`report-CompatibilityPHP56 <report-compatibilityphp56>`
      + :ref:`report-CompatibilityPHP74 <report-compatibilityphp74>`
      + :ref:`report-CompatibilityPHP80 <report-compatibilityphp80>`
      + :ref:`report-CompatibilityPHP81 <report-compatibilityphp81>`
      + :ref:`report-CompatibilityPHP82 <report-compatibilityphp82>`
      + :ref:`report-CompatibilityPHP83 <report-compatibilityphp83>`
      + :ref:`report-CompatibilityPHP84 <report-compatibilityphp84>`
      + :ref:`report-Composer <report-composer>`
      + :ref:`report-Dependency Wheel <report-dependency-wheel>`
      + :ref:`report-Diplomat <report-diplomat>`
      + :ref:`report-Emissary <report-emissary>`
      + :ref:`report-Exakat Json <report-exakat-json>`
      + :ref:`report-Exakatyaml <report-exakatyaml>`
      + :ref:`report-File dependendies <report-file-dependendies>`
      + :ref:`report-File dependendies HTML <report-file-dependendies-html>`
      + :ref:`report-History <report-history>`
      + :ref:`report-Inventory <report-inventory>`
      + :ref:`report-Json <report-json>`
      + :ref:`report-Marmelab <report-marmelab>`
      + :ref:`report-Meters <report-meters>`
      + :ref:`report-Migration74 <report-migration74>`
      + :ref:`report-Migration80 <report-migration80>`
      + :ref:`report-Migration81 <report-migration81>`
      + :ref:`report-Migration82 <report-migration82>`
      + :ref:`report-Naming <report-naming>`
      + :ref:`report-None <report-none>`
      + :ref:`report-OneLiners <report-oneliners>`
      + :ref:`report-Owasp <report-owasp>`
      + :ref:`report-Perfile <report-perfile>`
      + :ref:`report-Perfule <report-perfule>`
      + :ref:`report-PhpCompilation <report-phpcompilation>`
      + :ref:`report-PhpConfiguration <report-phpconfiguration>`
      + :ref:`report-Phpcity <report-phpcity>`
      + :ref:`report-Phpcsfixer <report-phpcsfixer>`
      + :ref:`report-PlantUml <report-plantuml>`
      + :ref:`report-PublicAccess <report-publicaccess>`
      + :ref:`report-RadwellCode <report-radwellcode>`
      + :ref:`report-Rector <report-rector>`
      + :ref:`report-Sarb <report-sarb>`
      + :ref:`report-Sarif <report-sarif>`
      + :ref:`report-SimpleTable <report-simpletable>`
      + :ref:`report-Sonarcube <report-sonarcube>`
      + :ref:`report-Stats <report-stats>`
      + :ref:`report-Stubs <report-stubs>`
      + :ref:`report-StubsJson <report-stubsjson>`
      + :ref:`report-Text <report-text>`
      + :ref:`report-Top10 <report-top10>`
      + :ref:`report-Topology Order <report-topology-order>`
      + :ref:`report-TypeChecks <report-typechecks>`
      + :ref:`report-TypeSuggestion <report-typesuggestion>`
      + :ref:`report-Uml <report-uml>`
      + :ref:`report-Unused <report-unused>`
      + :ref:`report-Weekly <report-weekly>`
      + :ref:`report-Xml <report-xml>`
      + :ref:`report-Yaml <report-yaml>`

    + `compact()`

      + :ref:`Create Compact Variables <create-compact-variables>`
      + :ref:`Nonexistent Variable In compact() <nonexistent-variable-in-compact()>`

    + `config`

      + :ref:`Assigned Twice <assigned-twice>`
      + :ref:`Same Conditions In Condition <same-conditions-in-condition>`

    + `connection`

      + :ref:`No Hardcoded Port <no-hardcoded-port>`
      + :ref:`Safe Curl Options <safe-curl-options>`
      + :ref:`Stomp <stomp>`
      + :ref:`Use PHP Object API <use-php-object-api>`
      + :ref:`ext/curl <ext-curl>`
      + :ref:`ext/ftp <ext-ftp>`
      + :ref:`ext/geoip <ext-geoip>`
      + :ref:`ext/ldap <ext-ldap>`
      + :ref:`ext/mysqli <ext-mysqli>`
      + :ref:`ext/ssh2 <ext-ssh2>`

    + `constant()`

      + :ref:`Dynamic Class Constant <dynamic-class-constant>`
      + :ref:`Fully Qualified Constants <fully-qualified-constants>`
      + :ref:`PHP 7.4 Reserved Keyword <php-7.4-reserved-keyword>`
      + :ref:`Variable Constants <variable-constants>`

    + `continue`

      + :ref:`Bail Out Early <bail-out-early>`
      + :ref:`Break Outside Loop <break-outside-loop>`
      + :ref:`Continue Is For Loop <continue-is-for-loop>`
      + :ref:`More Than One Level Of Indentation <more-than-one-level-of-indentation>`
      + :ref:`No Need For Else <no-need-for-else>`
      + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
      + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`
      + :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`
      + :ref:`Unreachable Code <unreachable-code>`
      + :ref:`Upload Filename Injection <upload-filename-injection>`
      + :ref:`Useless Instructions <useless-instructions>`

    + `convert_cyr_string()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `copy()`

      + :ref:`Protocol lists <protocol-lists>`

    + `count()`

      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
      + :ref:`Count() Is Not Negative <count()-is-not-negative>`
      + :ref:`Count() To Array Append <count()-to-array-append>`
      + :ref:`Empty Array Detection <empty-array-detection>`
      + :ref:`No Count With 0 <no-count-with-0>`
      + :ref:`PHP Interfaces <php-interfaces>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`Use Recursive count() <use-recursive-count()>`
      + :ref:`Use is_countable <use-is\_countable>`
      + :ref:`Useless Check <useless-check>`
      + :ref:`Uses Default Values <uses-default-values>`

    + `countable`

      + :ref:`Use is_countable <use-is\_countable>`

    + `crc32()`

      + :ref:`Crc32() Might Be Negative <crc32()-might-be-negative>`

    + `crypt()`

      + :ref:`Use password_hash() <use-password\_hash()>`
      + :ref:`crypt() Without Salt <crypt()-without-salt>`
      + :ref:`ext/password <ext-password>`

    + `ctype`

      + :ref:`ext/ctype <ext-ctype>`

    + `curl_escape()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_exec()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `curl_file_create()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_init()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
      + :ref:`Safe Curl Options <safe-curl-options>`

    + `curl_multi_errno()`

      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`

    + `curl_multi_init()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `curl_multi_setopt()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_multi_strerror()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_pause()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_reset()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_setopt()`

      + :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`

    + `curl_share_close()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_share_errno()`

      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`

    + `curl_share_init()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`
      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `curl_share_setopt()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_share_strerror()`

      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`

    + `curl_strerror()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_unescape()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `curl_upkeep()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `curl_version()`

      + :ref:`curl_version() Has No Argument <curl\_version()-has-no-argument>`

    + `current()`

      + :ref:`Foreach Don't Change Pointer <foreach-don't-change-pointer>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`


+ `D`
    + `DB2_AUTOCOMMIT_OFF`

      + :ref:`ext/db2 <ext-db2>`

    + `DIRECTORY_SEPARATOR`

      + :ref:`Strange Name For Constants <strange-name-for-constants>`

    + `DNS_NS`

      + :ref:`Is Global Constant <is-global-constant>`

    + `DOMDocument`

      + :ref:`No Net For Xml Load <no-net-for-xml-load>`
      + :ref:`ext/dom <ext-dom>`
      + :ref:`ext/xsl <ext-xsl>`

    + `DateError`

      + :ref:`Php 8.3 New Classes <php-8.3-new-classes>`

    + `DateInterval`

      + :ref:`ext/date <ext-date>`

    + `DateTime`

      + :ref:`Clone Usage <clone-usage>`
      + :ref:`Don't Add Seconds <don't-add-seconds>`
      + :ref:`Timestamp Difference <timestamp-difference>`
      + :ref:`Use DateTimeImmutable Class <use-datetimeimmutable-class>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`
      + :ref:`ext/date <ext-date>`

    + `DateTimeImmutable`

      + :ref:`DateTimeImmutable Is Not Immutable <datetimeimmutable-is-not-immutable>`
      + :ref:`Promoted Properties <promoted-properties>`
      + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `DateTimeZone`

      + :ref:`ext/date <ext-date>`

    + `Datetime`

      + :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`

    + `Define()`

      + :ref:`Constant Case Preference <constant-case-preference>`

    + `Die`

      + :ref:`Die Exit Consistence <die-exit-consistence>`
      + :ref:`Print And Die <print-and-die>`

    + `Directory`

      + :ref:`Could Inject Parameter <could-inject-parameter>`
      + :ref:`ext/ldap <ext-ldap>`

    + `DirectoryIterator`

      + :ref:`Protocol lists <protocol-lists>`

    + `DivisionByZeroError`

      + :ref:`Check Division By Zero <check-division-by-zero>`
      + :ref:`Could Use Try <could-use-try>`
      + :ref:`Throw <throw>`

    + `date()`

      + :ref:`Abstract Away <abstract-away>`
      + :ref:`Date Formats <date-formats>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `dateTime`

      + :ref:`Clone Usage <clone-usage>`

    + `date_create()`

      + :ref:`PHP 7.1 Microseconds <php-7.1-microseconds>`

    + `date_format()`

      + :ref:`Date Formats <date-formats>`

    + `datefmt_format_object()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `datefmt_get_calendar_object()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `datefmt_get_timezone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `datefmt_set_timezone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `datetime`

      + :ref:`Timestamp Difference <timestamp-difference>`

    + `datetimeimmutable`

      + :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`

    + `debug_backtrace()`

      + :ref:`Use Debug <use-debug>`

    + `debug_print_backtrace()`

      + :ref:`Use Debug <use-debug>`

    + `debug_zval_dump()`

      + :ref:`Use Debug <use-debug>`

    + `define()`

      + :ref:`Case Insensitive Constants <case-insensitive-constants>`
      + :ref:`Conditional Structures <conditional-structures>`
      + :ref:`Const Or Define Preference <const-or-define-preference>`
      + :ref:`Constant Case Preference <constant-case-preference>`
      + :ref:`Constants Created Outside Its Namespace <constants-created-outside-its-namespace>`
      + :ref:`Constants Names <constants-names>`
      + :ref:`Define Constants With Array <define-constants-with-array>`
      + :ref:`Fully Qualified Constants <fully-qualified-constants>`
      + :ref:`Invalid Constant Name <invalid-constant-name>`
      + :ref:`Non-constant Index In Array <non-constant-index-in-array>`
      + :ref:`PHP 7.4 Reserved Keyword <php-7.4-reserved-keyword>`
      + :ref:`Propagate Constants <propagate-constants>`
      + :ref:`Use const <use-const>`

    + `defined()`

      + :ref:`Undefined Methods <undefined-methods>`

    + `deflate_init()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `dictionary`

      + :ref:`ext/enchant <ext-enchant>`

    + `die`

      + :ref:`Check JSON <check-json>`
      + :ref:`Die Exit Consistence <die-exit-consistence>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Empty Function <empty-function>`
      + :ref:`Environment Variables <environment-variables>`
      + :ref:`Error Messages <error-messages>`
      + :ref:`Exit Without Argument <exit-without-argument>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Exit-like Methods <exit-like-methods>`
      + :ref:`Implied If <implied-if>`
      + :ref:`Joomla usage <joomla-usage>`
      + :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
      + :ref:`No Direct Access <no-direct-access>`
      + :ref:`No Hardcoded Port <no-hardcoded-port>`
      + :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`
      + :ref:`Or Die <or-die>`
      + :ref:`PHP 8.1 New Types <php-8.1-new-types>`
      + :ref:`Print And Die <print-and-die>`
      + :ref:`Stomp <stomp>`
      + :ref:`Type Could Be Never <type-could-be-never>`
      + :ref:`Unreachable Code <unreachable-code>`
      + :ref:`ext/bzip2 <ext-bzip2>`
      + :ref:`ext/crypto <ext-crypto>`
      + :ref:`ext/expect <ext-expect>`
      + :ref:`ext/ibase <ext-ibase>`
      + :ref:`ext/imap <ext-imap>`
      + :ref:`ext/memcache <ext-memcache>`
      + :ref:`ext/mssql <ext-mssql>`
      + :ref:`ext/mysql <ext-mysql>`
      + :ref:`ext/pcntl <ext-pcntl>`
      + :ref:`ext/rar <ext-rar>`
      + :ref:`ext/shmop <ext-shmop>`
      + :ref:`ext/sqlite <ext-sqlite>`
      + :ref:`ext/sqlsrv <ext-sqlsrv>`
      + :ref:`ext/ssh2 <ext-ssh2>`
      + :ref:`ext/xml <ext-xml>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`

    + `directory`

      + :ref:`$FILES full_path <$files-full\_path>`
      + :ref:`Could Inject Parameter <could-inject-parameter>`
      + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
      + :ref:`Keep Files Access Restricted <keep-files-access-restricted>`
      + :ref:`No Hardcoded Path <no-hardcoded-path>`
      + :ref:`Path lists <path-lists>`
      + :ref:`Protocol lists <protocol-lists>`
      + :ref:`Unchecked Resources <unchecked-resources>`
      + :ref:`__DIR__ Then Slash <\_\_dir\_\_-then-slash>`

    + `dirname()`

      + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
      + :ref:`PHP7 Dirname <php7-dirname>`
      + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

    + `dl()`

      + :ref:`Dl() Usage <dl()-usage>`

    + `dns_get_record()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`


+ `E`
    + `ENT_IGNORE`

      + :ref:`No ENT_IGNORE <no-ent\_ignore>`

    + `ENT_QUOTES`

      + :ref:`Htmlentities Calls <htmlentities-calls>`
      + :ref:`No ENT_IGNORE <no-ent\_ignore>`
      + :ref:`ext/oci8 <ext-oci8>`

    + `ENT_SUBSTITUTE`

      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`

    + `ERROR`

      + :ref:`Check JSON <check-json>`
      + :ref:`Friend Attribute <friend-attribute>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`ext/event <ext-event>`

    + `EXTR_OVERWRITE`

      + :ref:`Configure Extract <configure-extract>`

    + `EXTR_PREFIX_ALL`

      + :ref:`Configure Extract <configure-extract>`

    + `EXTR_SKIP`

      + :ref:`Configure Extract <configure-extract>`

    + `E_ALL`

      + :ref:`Dynamic Class Constant <dynamic-class-constant>`
      + :ref:`Is Global Constant <is-global-constant>`
      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`
      + :ref:`ext/sockets <ext-sockets>`

    + `E_DEPRECATED`

      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`

    + `E_ERROR`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `E_NOTICE`

      + :ref:`crypt() Without Salt <crypt()-without-salt>`
      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`

    + `E_PARSE`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `E_STRICT`

      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`

    + `E_USER_ERROR`

      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Trigger Errors <trigger-errors>`
      + :ref:`ext/oci8 <ext-oci8>`

    + `E_USER_NOTICE`

      + :ref:`PHP Handlers Usage <php-handlers-usage>`

    + `E_USER_WARNING`

      + :ref:`PHP Handlers Usage <php-handlers-usage>`

    + `E_WARNING`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`

    + `Engine`

      + :ref:`Random extension <random-extension>`
      + :ref:`ext/tokenizer <ext-tokenizer>`
      + :ref:`ext/v8js <ext-v8js>`

    + `Error`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`Abstract Or Implements <abstract-or-implements>`
      + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
      + :ref:`Can't Count Non-Countable <can't-count-non-countable>`
      + :ref:`Can't Implement Throwable <can't-implement-throwable>`
      + :ref:`Caught Variable <caught-variable>`
      + :ref:`Check JSON <check-json>`
      + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
      + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Error Messages <error-messages>`
      + :ref:`Inherited Class Constant Visibility <inherited-class-constant-visibility>`
      + :ref:`Interfaces Don't Ensure Properties <interfaces-don't-ensure-properties>`
      + :ref:`Invalid Cast <invalid-cast>`
      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`
      + :ref:`No Return For Generator <no-return-for-generator>`
      + :ref:`PHP 7.0 New Classes <php-7.0-new-classes>`
      + :ref:`Print And Die <print-and-die>`
      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Try Without Catch <try-without-catch>`
      + :ref:`Uncaught Exceptions <uncaught-exceptions>`
      + :ref:`Undefined Constant Name <undefined-constant-name>`
      + :ref:`Undefined Properties <undefined-properties>`
      + :ref:`ext/expect <ext-expect>`
      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/sdl <ext-sdl>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`

    + `Exception`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`Anonymous Catch <anonymous-catch>`
      + :ref:`Array Access On Literal Array <array-access-on-literal-array>`
      + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
      + :ref:`Can't Implement Throwable <can't-implement-throwable>`
      + :ref:`Catch Overwrite Variable <catch-overwrite-variable>`
      + :ref:`Catch With Undefined Variable <catch-with-undefined-variable>`
      + :ref:`Caught Expressions <caught-expressions>`
      + :ref:`Caught Variable <caught-variable>`
      + :ref:`Collect Catch Calls <collect-catch-calls>`
      + :ref:`Collect Methods Throwing Exceptions <collect-methods-throwing-exceptions>`
      + :ref:`Collect Throw Calls <collect-throw-calls>`
      + :ref:`Could Drop Variable <could-drop-variable>`
      + :ref:`Default Then Discard <default-then-discard>`
      + :ref:`Defined Exceptions <defined-exceptions>`
      + :ref:`Don't Be Too Manual <don't-be-too-manual>`
      + :ref:`Empty Classes <empty-classes>`
      + :ref:`Empty Try Catch <empty-try-catch>`
      + :ref:`Error Messages <error-messages>`
      + :ref:`Exception Order <exception-order>`
      + :ref:`Excimer <excimer>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Forgotten Thrown <forgotten-thrown>`
      + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
      + :ref:`Overwritten Exceptions <overwritten-exceptions>`
      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
      + :ref:`Phalcon Usage <phalcon-usage>`
      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Rethrown Exceptions <rethrown-exceptions>`
      + :ref:`Should Chain Exception <should-chain-exception>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
      + :ref:`Throw Was An Expression <throw-was-an-expression>`
      + :ref:`Throws An Assignement <throws-an-assignement>`
      + :ref:`Type Dodging <type-dodging>`
      + :ref:`Uncaught Exceptions <uncaught-exceptions>`
      + :ref:`Unchecked Resources <unchecked-resources>`
      + :ref:`Undefined Caught Exceptions <undefined-caught-exceptions>`
      + :ref:`Unresolved Catch <unresolved-catch>`
      + :ref:`Unthrown Exception <unthrown-exception>`
      + :ref:`Use random_int() <use-random\_int()>`
      + :ref:`Useless Try <useless-try>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`ext/phar <ext-phar>`
      + :ref:`ext/protobuf <ext-protobuf>`
      + :ref:`ext/psr <ext-psr>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`
      + :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`

    + `Exit`

      + :ref:`Die Exit Consistence <die-exit-consistence>`

    + `each()`

      + :ref:`PHP 7.2 Deprecations <php-7.2-deprecations>`
      + :ref:`PHP 7.2 Removed Functions <php-7.2-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `easter_days()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `enchant_broker_init()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
      + :ref:`ext/enchant <ext-enchant>`

    + `enchant_broker_request_dict()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `enchant_broker_request_pwl_dict()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `engine`

      + :ref:`Collect Atom Counts <collect-atom-counts>`
      + :ref:`Displays Text <displays-text>`
      + :ref:`Is PHP Structure <is-php-structure>`
      + :ref:`Multiple Returns <multiple-returns>`
      + :ref:`No Net For Xml Load <no-net-for-xml-load>`
      + :ref:`Non-lowercase Keywords <non-lowercase-keywords>`
      + :ref:`Unreachable Code <unreachable-code>`
      + :ref:`Useless Type Casting <useless-type-casting>`
      + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
      + :ref:`ext/hash <ext-hash>`

    + `enum_exists()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `error`

      + :ref:`$php_errormsg Usage <$php\_errormsg-usage>`
      + :ref:`@ Operator <@-operator>`
      + :ref:`Abstract Class Constants <abstract-class-constants>`
      + :ref:`Abstract Or Implements <abstract-or-implements>`
      + :ref:`Accessing Private <accessing-private>`
      + :ref:`Always Anchor Regex <always-anchor-regex>`
      + :ref:`Ambiguous Static <ambiguous-static>`
      + :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
      + :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
      + :ref:`Avoid Optional Properties <avoid-optional-properties>`
      + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
      + :ref:`Bad Type Relay <bad-type-relay>`
      + :ref:`Break With Non Integer <break-with-non-integer>`
      + :ref:`Can't Count Non-Countable <can't-count-non-countable>`
      + :ref:`Can't Extend Final Class <can't-extend-final-class>`
      + :ref:`Can't Implement Throwable <can't-implement-throwable>`
      + :ref:`Cannot Use Append For Reading <cannot-use-append-for-reading>`
      + :ref:`Cant Inherit Abstract Method <cant-inherit-abstract-method>`
      + :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
      + :ref:`Casting Ternary <casting-ternary>`
      + :ref:`Caught Variable <caught-variable>`
      + :ref:`Check Division By Zero <check-division-by-zero>`
      + :ref:`Check JSON <check-json>`
      + :ref:`Class Without Parent <class-without-parent>`
      + :ref:`Class-typed References <class-typed-references>`
      + :ref:`Classes Mutually Extending Each Other <classes-mutually-extending-each-other>`
      + :ref:`Close Tags Consistency <close-tags-consistency>`
      + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
      + :ref:`Converted Exceptions <converted-exceptions>`
      + :ref:`Could Be Callable <could-be-callable>`
      + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
      + :ref:`Could Use Try <could-use-try>`
      + :ref:`Crypto Usage <crypto-usage>`
      + :ref:`Custom Constant Usage <custom-constant-usage>`
      + :ref:`Declare strict_types Usage <declare-strict\_types-usage>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Duplicate Named Parameter <duplicate-named-parameter>`
      + :ref:`Empty Function <empty-function>`
      + :ref:`Empty Json Error <empty-json-error>`
      + :ref:`Empty Try Catch <empty-try-catch>`
      + :ref:`Error Messages <error-messages>`
      + :ref:`Eval() Usage <eval()-usage>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Final Class Usage <final-class-usage>`
      + :ref:`Final Methods Usage <final-methods-usage>`
      + :ref:`Forgotten Thrown <forgotten-thrown>`
      + :ref:`Forgotten Whitespace <forgotten-whitespace>`
      + :ref:`Hash Will Use Objects <hash-will-use-objects>`
      + :ref:`Iconv With Translit <iconv-with-translit>`
      + :ref:`Implemented Methods Must Be Public <implemented-methods-must-be-public>`
      + :ref:`Incompatible Signature Methods <incompatible-signature-methods>`
      + :ref:`Incompatible Signature Methods With Covariance <incompatible-signature-methods-with-covariance>`
      + :ref:`Inconsistent Concatenation <inconsistent-concatenation>`
      + :ref:`Inherited Class Constant Visibility <inherited-class-constant-visibility>`
      + :ref:`Injectable Version <injectable-version>`
      + :ref:`Insufficient Type <insufficient-type>`
      + :ref:`Interfaces Is Not Implemented <interfaces-is-not-implemented>`
      + :ref:`Invalid Constant Name <invalid-constant-name>`
      + :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`
      + :ref:`Invalid Octal In String <invalid-octal-in-string>`
      + :ref:`Invalid Regex <invalid-regex>`
      + :ref:`Is Actually Zero <is-actually-zero>`
      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`
      + :ref:`Local Globals <local-globals>`
      + :ref:`Malformed Octal <malformed-octal>`
      + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`
      + :ref:`Method Collision Traits <method-collision-traits>`
      + :ref:`Method Signature Must Be Compatible <method-signature-must-be-compatible>`
      + :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
      + :ref:`Minus One On Error <minus-one-on-error>`
      + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
      + :ref:`Missing Abstract Method <missing-abstract-method>`
      + :ref:`Missing Include <missing-include>`
      + :ref:`Missing Overriden Method <missing-overriden-method>`
      + :ref:`Missing Some Returntype <missing-some-returntype>`
      + :ref:`Mixed Concat And Interpolation <mixed-concat-and-interpolation>`
      + :ref:`Modified Typed Parameter <modified-typed-parameter>`
      + :ref:`Multiple Constant Definition <multiple-constant-definition>`
      + :ref:`Multiple Definition Of The Same Argument <multiple-definition-of-the-same-argument>`
      + :ref:`Multiple Functions Declarations <multiple-functions-declarations>`
      + :ref:`Multiple Usage Of Same Trait <multiple-usage-of-same-trait>`
      + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`
      + :ref:`Named Arguments And Variadic <named-arguments-and-variadic>`
      + :ref:`Never Called Parameter <never-called-parameter>`
      + :ref:`No A Valid Cast <no-a-valid-cast>`
      + :ref:`No Direct Usage Of Returned Value <no-direct-usage-of-returned-value>`
      + :ref:`No Empty Regex <no-empty-regex>`
      + :ref:`No Keyword In Namespace <no-keyword-in-namespace>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`No Max On Empty Array <no-max-on-empty-array>`
      + :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`
      + :ref:`No Object As Index <no-object-as-index>`
      + :ref:`No Real Comparison <no-real-comparison>`
      + :ref:`No Self Referencing Constant <no-self-referencing-constant>`
      + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
      + :ref:`Non-constant Index In Array <non-constant-index-in-array>`
      + :ref:`Not A Scalar Type <not-a-scalar-type>`
      + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
      + :ref:`Nullable Without Check <nullable-without-check>`
      + :ref:`One Expression Brackets Consistency <one-expression-brackets-consistency>`
      + :ref:`Only Variable For Reference <only-variable-for-reference>`
      + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
      + :ref:`Or Die <or-die>`
      + :ref:`Override Attribute <override-attribute>`
      + :ref:`Overwritten Foreach Var <overwritten-foreach-var>`
      + :ref:`PHP 7.0 Scalar Types <php-7.0-scalar-types>`
      + :ref:`PHP 7.4 Reserved Keyword <php-7.4-reserved-keyword>`
      + :ref:`PHP 8.0 Types <php-8.0-types>`
      + :ref:`PHP Exception <php-exception>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`PSR-3 Usage <psr-3-usage>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Possible TypeError <possible-typeerror>`
      + :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
      + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
      + :ref:`Raised Access Level <raised-access-level>`
      + :ref:`Redefined Private Property <redefined-private-property>`
      + :ref:`Restrict Global Usage <restrict-global-usage>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`String May Hold A Variable <string-may-hold-a-variable>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Switch Fallthrough <switch-fallthrough>`
      + :ref:`Test Then Cast <test-then-cast>`
      + :ref:`Throw Functioncall <throw-functioncall>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
      + :ref:`Thrown Exceptions <thrown-exceptions>`
      + :ref:`Too Complex Expression <too-complex-expression>`
      + :ref:`Too Many Chained Calls <too-many-chained-calls>`
      + :ref:`Try Without Catch <try-without-catch>`
      + :ref:`Type Must Be Returned <type-must-be-returned>`
      + :ref:`Uncaught Exceptions <uncaught-exceptions>`
      + :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`
      + :ref:`Undefined Class Constants <undefined-class-constants>`
      + :ref:`Undefined Constant Name <undefined-constant-name>`
      + :ref:`Undefined Functions <undefined-functions>`
      + :ref:`Undefined Insteadof <undefined-insteadof>`
      + :ref:`Undefined Parent <undefined-parent>`
      + :ref:`Undefined Trait <undefined-trait>`
      + :ref:`Undefined static ::class <undefined-static-class>`
      + :ref:`Unfinished Object <unfinished-object>`
      + :ref:`Unicode Escape Partial <unicode-escape-partial>`
      + :ref:`Unknown Pcre2 Option <unknown-pcre2-option>`
      + :ref:`Unkown Regex Options <unkown-regex-options>`
      + :ref:`Unreadable Interval Check <unreadable-interval-check>`
      + :ref:`Unsupported Operand Types <unsupported-operand-types>`
      + :ref:`Unthrown Exception <unthrown-exception>`
      + :ref:`Untyped No Default Properties <untyped-no-default-properties>`
      + :ref:`Unused Enumeration Case <unused-enumeration-case>`
      + :ref:`Unused Parameter <unused-parameter>`
      + :ref:`Upload Filename Injection <upload-filename-injection>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`Use Constants As Returns <use-constants-as-returns>`
      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
      + :ref:`Use Nullable Type <use-nullable-type>`
      + :ref:`Useless Catch <useless-catch>`
      + :ref:`Useless Override Attribute <useless-override-attribute>`
      + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
      + :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`
      + :ref:`Weird Array Index <weird-array-index>`
      + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`
      + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`
      + :ref:`Wrong Number Of Arguments In Methods <wrong-number-of-arguments-in-methods>`
      + :ref:`Wrong Type For Native PHP Function <wrong-type-for-native-php-function>`
      + :ref:`Wrong Type Returned <wrong-type-returned>`
      + :ref:`Wrong Type With Default <wrong-type-with-default>`
      + :ref:`Yoda Comparison <yoda-comparison>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`
      + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`
      + :ref:`crypt() Without Salt <crypt()-without-salt>`
      + :ref:`error_reporting() With Integers <error\_reporting()-with-integers>`
      + :ref:`eval() Without Try <eval()-without-try>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/gender <ext-gender>`
      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/openssl <ext-openssl>`
      + :ref:`ext/posix <ext-posix>`
      + :ref:`ext/protobuf <ext-protobuf>`
      + :ref:`ext/xml <ext-xml>`
      + :ref:`ext/xsl <ext-xsl>`
      + :ref:`isset() With Constants <isset()-with-constants>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`
      + :ref:`var_dump()... Usage <var\_dump()...-usage>`

    + `error_clear_last()`

      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`

    + `error_get_last()`

      + :ref:`$php_errormsg Usage <$php\_errormsg-usage>`

    + `error_log()`

      + :ref:`Error_Log() Usage <error\_log()-usage>`

    + `error_reporting()`

      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `exception`

      + :ref:`Anonymous Catch <anonymous-catch>`
      + :ref:`Catch Overwrite Variable <catch-overwrite-variable>`
      + :ref:`Catch With Undefined Variable <catch-with-undefined-variable>`
      + :ref:`Caught Variable <caught-variable>`
      + :ref:`Check All Types <check-all-types>`
      + :ref:`Check Division By Zero <check-division-by-zero>`
      + :ref:`Collect Catch Calls <collect-catch-calls>`
      + :ref:`Collect Methods Throwing Exceptions <collect-methods-throwing-exceptions>`
      + :ref:`Collect Throw Calls <collect-throw-calls>`
      + :ref:`Converted Exceptions <converted-exceptions>`
      + :ref:`Could Drop Variable <could-drop-variable>`
      + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
      + :ref:`Defined Exceptions <defined-exceptions>`
      + :ref:`Empty Classes <empty-classes>`
      + :ref:`Empty Function <empty-function>`
      + :ref:`Exception Order <exception-order>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Forgotten Thrown <forgotten-thrown>`
      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`
      + :ref:`Large Try Block <large-try-block>`
      + :ref:`Long Preparation For Throw <long-preparation-for-throw>`
      + :ref:`Manipulates INF <manipulates-inf>`
      + :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
      + :ref:`Multiple Returns <multiple-returns>`
      + :ref:`Never Keyword <never-keyword>`
      + :ref:`Never Type Usage <never-type-usage>`
      + :ref:`No Max On Empty Array <no-max-on-empty-array>`
      + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
      + :ref:`Null On New <null-on-new>`
      + :ref:`Overwritten Exceptions <overwritten-exceptions>`
      + :ref:`PHP Exception <php-exception>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Rethrown Exceptions <rethrown-exceptions>`
      + :ref:`Set Chaining Exception <set-chaining-exception>`
      + :ref:`Should Chain Exception <should-chain-exception>`
      + :ref:`Switch Without Default <switch-without-default>`
      + :ref:`Throw <throw>`
      + :ref:`Throw Functioncall <throw-functioncall>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
      + :ref:`Throws An Assignement <throws-an-assignement>`
      + :ref:`Uncaught Exceptions <uncaught-exceptions>`
      + :ref:`Undefined Caught Exceptions <undefined-caught-exceptions>`
      + :ref:`Unresolved Catch <unresolved-catch>`
      + :ref:`Unthrown Exception <unthrown-exception>`
      + :ref:`Unused Exception Variable <unused-exception-variable>`
      + :ref:`Use Instanceof <use-instanceof>`
      + :ref:`Useless Catch <useless-catch>`
      + :ref:`Useless Try <useless-try>`
      + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`eval() Without Try <eval()-without-try>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`

    + `exec()`

      + :ref:`Can't Disable Function <can't-disable-function>`
      + :ref:`Shell Favorite <shell-favorite>`
      + :ref:`Shell commands <shell-commands>`

    + `exit`

      + :ref:`Die Exit Consistence <die-exit-consistence>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Else Usage <else-usage>`
      + :ref:`Error Messages <error-messages>`
      + :ref:`Exit Without Argument <exit-without-argument>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Exit-like Methods <exit-like-methods>`
      + :ref:`Never Type Usage <never-type-usage>`
      + :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
      + :ref:`PHP 8.1 Types <php-8.1-types>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Print And Die <print-and-die>`
      + :ref:`Switch Without Default <switch-without-default>`
      + :ref:`Unreachable Code <unreachable-code>`
      + :ref:`Use PHP Object API <use-php-object-api>`
      + :ref:`ext/dba <ext-dba>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/ftp <ext-ftp>`
      + :ref:`ext/gearman <ext-gearman>`
      + :ref:`ext/mysqli <ext-mysqli>`
      + :ref:`ext/pcntl <ext-pcntl>`
      + :ref:`ext/zip <ext-zip>`

    + `explode()`

      + :ref:`Implode One Arg <implode-one-arg>`
      + :ref:`No Empty String With explode() <no-empty-string-with-explode()>`
      + :ref:`Optimize Explode() <optimize-explode()>`
      + :ref:`Should Use Explode Args <should-use-explode-args>`

    + `extract()`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`Configure Extract <configure-extract>`
      + :ref:`Foreach With list() <foreach-with-list()>`
      + :ref:`Function With Dynamic Code <function-with-dynamic-code>`
      + :ref:`Register Globals <register-globals>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `ezmlm_hash()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`


+ `F`
    + `FALSE`

      + :ref:`ext/file <ext-file>`
      + :ref:`ext/rar <ext-rar>`

    + `FFI`

      + :ref:`ext/ffi <ext-ffi>`

    + `FILEINFO_MIME_TYPE`

      + :ref:`ext/fileinfo <ext-fileinfo>`

    + `FILE_APPEND`

      + :ref:`Use File Append <use-file-append>`

    + `FILE_BINARY`

      + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

    + `FILE_IGNORE_NEW_LINES`

      + :ref:`Should Use Existing Constants <should-use-existing-constants>`

    + `FILE_TEXT`

      + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

    + `FILTER_SANITIZE_EMAIL`

      + :ref:`PHP Variables <php-variables>`

    + `FILTER_SANITIZE_SPECIAL_CHARS`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `FILTER_SANITIZE_STRING`

      + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

    + `FILTER_UNSAFE_RAW`

      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

    + `FILTER_VALIDATE_EMAIL`

      + :ref:`ext/filter <ext-filter>`

    + `FTP_BINARY`

      + :ref:`ext/ftp <ext-ftp>`

    + `FilesystemIterator`

      + :ref:`ext/spl <ext-spl>`

    + `FilterIterator`

      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `For()`

      + :ref:`Sequences In For <sequences-in-for>`

    + `Foreach()`

      + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
      + :ref:`Blind Variable Used Beyond Loop <blind-variable-used-beyond-loop>`
      + :ref:`Identical Variables In Foreach <identical-variables-in-foreach>`
      + :ref:`Should Use Foreach <should-use-foreach>`
      + :ref:`Use List With Foreach <use-list-with-foreach>`
      + :ref:`Useless Check <useless-check>`

    + `false`

      + :ref:`Always Anchor Regex <always-anchor-regex>`
      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Assign And Compare <assign-and-compare>`
      + :ref:`Bail Out Early <bail-out-early>`
      + :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
      + :ref:`Cast To Boolean <cast-to-boolean>`
      + :ref:`Check All Types <check-all-types>`
      + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
      + :ref:`Compare Hash <compare-hash>`
      + :ref:`Conditioned Constants <conditioned-constants>`
      + :ref:`Could Be A Constant <could-be-a-constant>`
      + :ref:`Could Be Constant <could-be-constant>`
      + :ref:`Could Be Null <could-be-null>`
      + :ref:`Could Use Trait <could-use-trait>`
      + :ref:`Could Use strcontains() <could-use-strcontains()>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Double Instructions <double-instructions>`
      + :ref:`Double array_flip() <double-array\_flip()>`
      + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
      + :ref:`False To Array Conversion <false-to-array-conversion>`
      + :ref:`Forgotten Thrown <forgotten-thrown>`
      + :ref:`Implied If <implied-if>`
      + :ref:`Indices Are Int Or String <indices-are-int-or-string>`
      + :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`
      + :ref:`Logical Mistakes <logical-mistakes>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Mismatched Type <mismatched-type>`
      + :ref:`Missing Include <missing-include>`
      + :ref:`Mixed Type Usage <mixed-type-usage>`
      + :ref:`Multiple Constant Definition <multiple-constant-definition>`
      + :ref:`Multiple Returns <multiple-returns>`
      + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
      + :ref:`Nested Match <nested-match>`
      + :ref:`No Boolean As Default <no-boolean-as-default>`
      + :ref:`No Empty String With explode() <no-empty-string-with-explode()>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`No isset() With empty() <no-isset()-with-empty()>`
      + :ref:`Overwritten Literals <overwritten-literals>`
      + :ref:`PHP 7.1 Microseconds <php-7.1-microseconds>`
      + :ref:`PHP 8.0 Removed Directives <php-8.0-removed-directives>`
      + :ref:`PHP 8.0 Types <php-8.0-types>`
      + :ref:`PHP 8.1 Removed Directives <php-8.1-removed-directives>`
      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
      + :ref:`Redefined Private Property <redefined-private-property>`
      + :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
      + :ref:`Return True False <return-true-false>`
      + :ref:`Same Conditions In Condition <same-conditions-in-condition>`
      + :ref:`Sequences In For <sequences-in-for>`
      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`StandaloneType True False Null <standalonetype-true-false-null>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`String Int Comparison <string-int-comparison>`
      + :ref:`Strings With Strange Space <strings-with-strange-space>`
      + :ref:`Strpos() Less Than One <strpos()-less-than-one>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Unchecked Resources <unchecked-resources>`
      + :ref:`Undefined Interfaces <undefined-interfaces>`
      + :ref:`Unresolved Catch <unresolved-catch>`
      + :ref:`Use Instanceof <use-instanceof>`
      + :ref:`Use Named Boolean In Argument Definition <use-named-boolean-in-argument-definition>`
      + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`
      + :ref:`Use str_contains() <use-str\_contains()>`
      + :ref:`Useless Catch <useless-catch>`
      + :ref:`Useless Coalesce <useless-coalesce>`
      + :ref:`Useless Short Ternary <useless-short-ternary>`
      + :ref:`Uses Default Values <uses-default-values>`
      + :ref:`Variables With One Letter Names <variables-with-one-letter-names>`
      + :ref:`Wrong Precedence In Expression <wrong-precedence-in-expression>`
      + :ref:`ext/exif <ext-exif>`
      + :ref:`ext/inotify <ext-inotify>`
      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/memcache <ext-memcache>`
      + :ref:`ext/shmop <ext-shmop>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/sqlsrv <ext-sqlsrv>`
      + :ref:`ext/teds <ext-teds>`
      + :ref:`ext/xmlrpc <ext-xmlrpc>`
      + :ref:`ext/xsl <ext-xsl>`
      + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`
      + :ref:`strpos() With Integers <strpos()-with-integers>`
      + :ref:`version_compare() Operator <version\_compare()-operator>`

    + `fdatasync()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `fdiv()`

      + :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`

    + `feof()`

      + :ref:`Possible Infinite Loop <possible-infinite-loop>`

    + `ffi`

      + :ref:`ext/ffi <ext-ffi>`

    + `fgetc()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `fgetcsv()`

      + :ref:`Possible Infinite Loop <possible-infinite-loop>`

    + `fgets()`

      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Reuse Existing Variable <reuse-existing-variable>`

    + `fgetss()`

      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`
      + :ref:`Possible Infinite Loop <possible-infinite-loop>`

    + `file()`

      + :ref:`Joining file() <joining-file()>`

    + `file_exists()`

      + :ref:`Protocol lists <protocol-lists>`

    + `file_get_contents()`

      + :ref:`Joining file() <joining-file()>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `file_put_contents()`

      + :ref:`File_Put_Contents Using Array Argument <file\_put\_contents-using-array-argument>`
      + :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Use File Append <use-file-append>`

    + `filesize()`

      + :ref:`Protocol lists <protocol-lists>`

    + `filter_input()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

    + `filter_input_array()`

      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

    + `filter_var()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `finfo`

      + :ref:`ext/fileinfo <ext-fileinfo>`

    + `finfo_open()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `floor()`

      + :ref:`Do Not Cast To Int <do-not-cast-to-int>`

    + `fopen()`

      + :ref:`@ Operator <@-operator>`
      + :ref:`Fopen Binary Mode <fopen-binary-mode>`
      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Protocol lists <protocol-lists>`
      + :ref:`Wrong fopen() Mode <wrong-fopen()-mode>`

    + `for()`

      + :ref:`Bracketless Blocks <bracketless-blocks>`
      + :ref:`Constant Conditions <constant-conditions>`
      + :ref:`For Using Functioncall <for-using-functioncall>`
      + :ref:`Add Brackets To Single Instructions <add-brackets-to-single-instructions>`
      + :ref:`Remove Brackets Around Single Instruction <remove-brackets-around-single-instruction>`

    + `foreach()`

      + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
      + :ref:`Avoid array_unique() <avoid-array\_unique()>`
      + :ref:`Bracketless Blocks <bracketless-blocks>`
      + :ref:`Break Outside Loop <break-outside-loop>`
      + :ref:`Can't Call Generator <can't-call-generator>`
      + :ref:`Don't Change The Blind Var <don't-change-the-blind-var>`
      + :ref:`Don't Reuse Foreach Source <don't-reuse-foreach-source>`
      + :ref:`Find Key Directly <find-key-directly>`
      + :ref:`Foreach Don't Change Pointer <foreach-don't-change-pointer>`
      + :ref:`Foreach With list() <foreach-with-list()>`
      + :ref:`Foreach() Favorite <foreach()-favorite>`
      + :ref:`Identical Variables In Foreach <identical-variables-in-foreach>`
      + :ref:`No Direct Usage Of Returned Value <no-direct-usage-of-returned-value>`
      + :ref:`Objects Don't Need References <objects-don't-need-references>`
      + :ref:`Overwritten Source And Value <overwritten-source-and-value>`
      + :ref:`Should Use array_column() <should-use-array\_column()>`
      + :ref:`Should Use array_filter() <should-use-array\_filter()>`
      + :ref:`Should Yield With Key <should-yield-with-key>`
      + :ref:`Simplify Foreach <simplify-foreach>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Substr() In Loops <substr()-in-loops>`
      + :ref:`Used Once Variables (In Scope) <used-once-variables-(in-scope)>`
      + :ref:`Useless Referenced Argument <useless-referenced-argument>`
      + :ref:`foreach() On Object <foreach()-on-object>`
      + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`
      + :ref:`Add Brackets To Single Instructions <add-brackets-to-single-instructions>`
      + :ref:`Remove Brackets Around Single Instruction <remove-brackets-around-single-instruction>`

    + `forward_static_call()`

      + :ref:`Callback Function Needs Return <callback-function-needs-return>`

    + `forward_static_call_array()`

      + :ref:`Callback Function Needs Return <callback-function-needs-return>`

    + `fputcsv()`

      + :ref:`fputcsv() In Loops <fputcsv()-in-loops>`

    + `fread()`

      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `fscanf()`

      + :ref:`Printf Format Inventory <printf-format-inventory>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

    + `fseek()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `fsockopen()`

      + :ref:`Can't Disable Function <can't-disable-function>`

    + `fsync()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `ftp_connect()`

      + :ref:`Can't Disable Class <can't-disable-class>`
      + :ref:`Can't Disable Function <can't-disable-function>`
      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `func_get_arg()`

      + :ref:`Has Variable Arguments <has-variable-arguments>`
      + :ref:`func_get_arg() Modified Behavior <func\_get\_arg()-modified-behavior>`

    + `func_get_args()`

      + :ref:`Ellipsis Usage <ellipsis-usage>`
      + :ref:`Has Variable Arguments <has-variable-arguments>`
      + :ref:`PHP 7.3 Last Empty Argument <php-7.3-last-empty-argument>`
      + :ref:`Typehinting Stats <typehinting-stats>`
      + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`
      + :ref:`Wrong Number Of Arguments In Methods <wrong-number-of-arguments-in-methods>`
      + :ref:`func_get_arg() Modified Behavior <func\_get\_arg()-modified-behavior>`

    + `func_num_args()`

      + :ref:`Has Variable Arguments <has-variable-arguments>`


+ `G`
    + `GLOB_BRACE`

      + :ref:`GLOB_BRACE Usage <glob\_brace-usage>`

    + `GLOB_NOSORT`

      + :ref:`Avoid glob() Usage <avoid-glob()-usage>`

    + `Generator`

      + :ref:`Method Is A Generator <method-is-a-generator>`
      + :ref:`Should Yield With Key <should-yield-with-key>`

    + `gc_mem_caches()`

      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`

    + `generator`

      + :ref:`Can't Call Generator <can't-call-generator>`
      + :ref:`Could Be Generator <could-be-generator>`
      + :ref:`Could Use Yield From <could-use-yield-from>`
      + :ref:`Don't Loop On Yield <don't-loop-on-yield>`
      + :ref:`Generator Cannot Return <generator-cannot-return>`
      + :ref:`Method Is A Generator <method-is-a-generator>`
      + :ref:`Misused Yield <misused-yield>`
      + :ref:`No Return For Generator <no-return-for-generator>`
      + :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`
      + :ref:`Yield From Usage <yield-from-usage>`

    + `getType()`

      + :ref:`ext/judy <ext-judy>`

    + `get_browser()`

      + :ref:`Use Browscap <use-browscap>`

    + `get_called_class()`

      + :ref:`Detect Current Class <detect-current-class>`
      + :ref:`Use This <use-this>`

    + `get_class()`

      + :ref:`No Need For get_class() <no-need-for-get\_class()>`
      + :ref:`No get_class() With Null <no-get\_class()-with-null>`
      + :ref:`Scope Resolution Operator <scope-resolution-operator>`
      + :ref:`Use This <use-this>`
      + :ref:`get_class() Without Argument <get\_class()-without-argument>`

    + `get_class_methods()`

      + :ref:`Use This <use-this>`

    + `get_class_vars()`

      + :ref:`Use This <use-this>`

    + `get_debug_type()`

      + :ref:`Use get_debug_type() <use-get\_debug\_type()>`

    + `get_declared_traits()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `get_html_translation_table()`

      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `get_magic_quotes_gpc()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `get_magic_quotes_runtime()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`

    + `get_object_vars()`

      + :ref:`Avoid get_object_vars() <avoid-get\_object\_vars()>`
      + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
      + :ref:`Use This <use-this>`

    + `get_parent_class()`

      + :ref:`Use This <use-this>`
      + :ref:`get_class() Without Argument <get\_class()-without-argument>`

    + `get_resources()`

      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`

    + `getdate()`

      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `getenv()`

      + :ref:`Environment Variable Usage <environment-variable-usage>`

    + `getimagesizefromstring()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `getopt()`

      + :ref:`Use Cli <use-cli>`

    + `gettext()`

      + :ref:`ext/gettext <ext-gettext>`

    + `glob()`

      + :ref:`Avoid glob() Usage <avoid-glob()-usage>`
      + :ref:`No Direct Usage Of Returned Value <no-direct-usage-of-returned-value>`
      + :ref:`No Hardcoded Path <no-hardcoded-path>`

    + `gmdate()`

      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `gmp`

      + :ref:`ext/gmp <ext-gmp>`

    + `gmp_binomial()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `gmp_div_q()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `gmp_div_qr()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `gmp_div_r()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `gmp_kronecker()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `gmp_lcm()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `gmp_perfect_power()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `gmp_root()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `gmp_rootrem()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `gmstrftime()`

      + :ref:`Date Formats <date-formats>`


+ `H`
    + `HTML_ENTITIES`

      + :ref:`Is PHP Constant <is-php-constant>`

    + `HashContext`

      + :ref:`Php 7.2 New Class <php-7.2-new-class>`

    + `hash()`

      + :ref:`Directly Use File <directly-use-file>`

    + `hash_algos()`

      + :ref:`Hash Algorithms <hash-algorithms>`

    + `hash_equals()`

      + :ref:`Compare Hash <compare-hash>`

    + `hash_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `hash_hmac()`

      + :ref:`Directly Use File <directly-use-file>`

    + `hash_pbkdf2()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `hash_update()`

      + :ref:`Directly Use File <directly-use-file>`

    + `hash_update_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `header()`

      + :ref:`Http Headers <http-headers>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`
      + :ref:`Use Cookies <use-cookies>`

    + `header_register_callback()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `hebrevc()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `hex2bin()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `highlight_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `highlight_string()`

      + :ref:`Directly Use File <directly-use-file>`

    + `html_entity_decode()`

      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `htmlentities()`

      + :ref:`Htmlentities Calls <htmlentities-calls>`
      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`Uses Default Values <uses-default-values>`

    + `htmlspecialchars()`

      + :ref:`Htmlentities Calls <htmlentities-calls>`
      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
      + :ref:`No ENT_IGNORE <no-ent\_ignore>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `htmlspecialchars_decode()`

      + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `httpRequest`

      + :ref:`Feast usage <feast-usage>`

    + `http_build_query()`

      + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `http_build_url()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `http_parse_cookie()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `http_parse_params()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `http_redirect()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `http_response_code()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `http_support()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`


+ `I`
    + `INF`

      + :ref:`Manipulates INF <manipulates-inf>`

    + `INPUT_COOKIE`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `INPUT_ENV`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `INPUT_GET`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`

    + `INPUT_POST`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `INPUT_SERVER`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `IntervalBoundary`

      + :ref:`Php 8.3 New Classes <php-8.3-new-classes>`

    + `Intval()`

      + :ref:`Should Typecast <should-typecast>`

    + `Isset`

      + :ref:`Isset() On The Whole Array <isset()-on-the-whole-array>`

    + `Iterator`

      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `ibase_errmsg()`

      + :ref:`ext/ibase <ext-ibase>`

    + `iconv()`

      + :ref:`Iconv With Translit <iconv-with-translit>`
      + :ref:`Substring First <substring-first>`

    + `iconv_strpos()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `iconv_strrpos()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `iconv_substr()`

      + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`

    + `idn_to_ascii()`

      + :ref:`idn_to_ascii() New Default <idn\_to\_ascii()-new-default>`

    + `idn_to_utf8()`

      + :ref:`idn_to_ascii() New Default <idn\_to\_ascii()-new-default>`

    + `imageaffinematrixconcat()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imageaffinematrixget()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imageavif()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `imagecolorallocate()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `imagecolorallocatealpha()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `imagecreatefromavif()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `imagecrop()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imagecropauto()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imageflip()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imagepalettetotruecolor()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imagescale()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `imap_last_error()`

      + :ref:`ext/imap <ext-imap>`

    + `imap_open()`

      + :ref:`Can't Disable Function <can't-disable-function>`
      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `implode()`

      + :ref:`Avoid Concat In Loop <avoid-concat-in-loop>`
      + :ref:`Implode One Arg <implode-one-arg>`
      + :ref:`Implode() Arguments Order <implode()-arguments-order>`
      + :ref:`Multiple Similar Calls <multiple-similar-calls>`
      + :ref:`Use Array Functions <use-array-functions>`

    + `in_array()`

      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Processing Collector <processing-collector>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`Strict In_Array() Preference <strict-in\_array()-preference>`
      + :ref:`Logical To in_array() <logical-to-in\_array()>`

    + `inflate_init()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `ini_get()`

      + :ref:`PHP 8.0 Removed Directives <php-8.0-removed-directives>`
      + :ref:`PHP 8.1 Removed Directives <php-8.1-removed-directives>`

    + `ini_parse_quantity()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `ini_set()`

      + :ref:`Definitions Only <definitions-only>`

    + `instanceof`

      + :ref:`Already Parents Interface <already-parents-interface>`
      + :ref:`Avoid get_class() <avoid-get\_class()>`
      + :ref:`Can't Implement Traversable <can't-implement-traversable>`
      + :ref:`Class Usage <class-usage>`
      + :ref:`Collect Classes Dependencies <collect-classes-dependencies>`
      + :ref:`Could Type <could-type>`
      + :ref:`Interfaces Usage <interfaces-usage>`
      + :ref:`Is An Extension Interface <is-an-extension-interface>`
      + :ref:`Missing Parenthesis <missing-parenthesis>`
      + :ref:`Not Equal Is Not !== <not-equal-is-not-!==>`
      + :ref:`Php 8.0 Variable Syntax Tweaks <php-8.0-variable-syntax-tweaks>`
      + :ref:`Reserved Match Keyword <reserved-match-keyword>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Should Make Alias <should-make-alias>`
      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Type Dodging <type-dodging>`
      + :ref:`Undefined Classes <undefined-classes>`
      + :ref:`Undefined Interfaces <undefined-interfaces>`
      + :ref:`Undefined static ::class <undefined-static-class>`
      + :ref:`Unresolved Instanceof <unresolved-instanceof>`
      + :ref:`Unused Interfaces <unused-interfaces>`
      + :ref:`Usage Of class_alias() <usage-of-class\_alias()>`
      + :ref:`Use Instanceof <use-instanceof>`
      + :ref:`Use is_countable <use-is\_countable>`
      + :ref:`Used Interfaces <used-interfaces>`
      + :ref:`ext/psr <ext-psr>`
      + :ref:`is_a() Versus instanceof <is\_a()-versus-instanceof>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`
      + :ref:`Rename Class <rename-class>`
      + :ref:`Rename Enums <rename-enums>`
      + :ref:`Rename Interface <rename-interface>`
      + :ref:`Rename Method <rename-method>`

    + `insteadof`

      + :ref:`Method Collision Traits <method-collision-traits>`
      + :ref:`Trait Not Found <trait-not-found>`
      + :ref:`Undefined Insteadof <undefined-insteadof>`

    + `intdiv()`

      + :ref:`Could Use Try <could-use-try>`
      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`

    + `intlcal_add()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_after()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_before()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_clear()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_create_instance()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_equals()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_field_difference()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_from_date_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_actual_maximum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_actual_minimum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_available_locales()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_day_of_week_type()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_error_code()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_error_message()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_first_day_of_week()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_greatest_minimum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_keyword_values_for_locale()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_least_maximum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_locale()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_maximum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_minimal_days_in_first_week()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_minimum()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_now()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_repeated_wall_time_option()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_skipped_wall_time_option()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_time_zone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_type()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_get_weekend_transition()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_in_daylight_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_is_equivalent_to()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_is_lenient()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_is_set()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_is_weekend()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_roll()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_first_day_of_week()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_lenient()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_repeated_wall_time_option()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_skipped_wall_time_option()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_set_time_zone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlcal_to_date_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlgregcal_create_instance()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlgregcal_get_gregorian_change()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlgregcal_is_leap_year()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intlgregcal_set_gregorian_change()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_count_equivalent_ids()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_create_default()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_create_enumeration()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_create_time_zone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_create_time_zone_id_enumeration()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_from_date_time_zone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_canonical_id()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_display_name()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_dst_savings()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_equivalent_id()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_error_code()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_error_message()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_gmt()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_id()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_offset()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_raw_offset()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_region()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_tz_data_version()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_get_unknown()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_has_same_rules()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_to_date_time_zone()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intltz_use_daylight_time()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `intval()`

      + :ref:`Do Not Cast To Int <do-not-cast-to-int>`
      + :ref:`Should Typecast <should-typecast>`

    + `is_a()`

      + :ref:`Is_A() With String <is\_a()-with-string>`
      + :ref:`is_a() Versus instanceof <is\_a()-versus-instanceof>`

    + `is_array()`

      + :ref:`Assumptions <assumptions>`
      + :ref:`Could Type <could-type>`
      + :ref:`Should Use Operator <should-use-operator>`

    + `is_callable()`

      + :ref:`Check All Types <check-all-types>`

    + `is_countable()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`
      + :ref:`Use is_countable <use-is\_countable>`

    + `is_int()`

      + :ref:`Double Checks <double-checks>`
      + :ref:`Should Use Operator <should-use-operator>`

    + `is_integer()`

      + :ref:`Use Instanceof <use-instanceof>`

    + `is_iterable()`

      + :ref:`Check All Types <check-all-types>`
      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`

    + `is_null()`

      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Use === null <use-===-null>`

    + `is_object()`

      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Use Instanceof <use-instanceof>`

    + `is_readable()`

      + :ref:`Double Checks <double-checks>`

    + `is_resource()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `is_scalar()`

      + :ref:`Use Instanceof <use-instanceof>`

    + `is_string()`

      + :ref:`Check All Types <check-all-types>`
      + :ref:`Could Type <could-type>`
      + :ref:`Use Instanceof <use-instanceof>`

    + `isset`

      + :ref:`Array Access On Literal Array <array-access-on-literal-array>`
      + :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
      + :ref:`Checks Property Existence <checks-property-existence>`
      + :ref:`Cookies Variables <cookies-variables>`
      + :ref:`Default Then Discard <default-then-discard>`
      + :ref:`Isset Multiple Arguments <isset-multiple-arguments>`
      + :ref:`Isset() On The Whole Array <isset()-on-the-whole-array>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Multiple Similar Calls <multiple-similar-calls>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`No Keyword In Namespace <no-keyword-in-namespace>`
      + :ref:`No isset() With empty() <no-isset()-with-empty()>`
      + :ref:`Session Variables <session-variables>`
      + :ref:`Should Use Coalesce <should-use-coalesce>`
      + :ref:`Should Use array_column() <should-use-array\_column()>`
      + :ref:`Should Use array_filter() <should-use-array\_filter()>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Too Complex Expression <too-complex-expression>`
      + :ref:`Try Without Catch <try-without-catch>`
      + :ref:`Use Instanceof <use-instanceof>`
      + :ref:`Useless Check <useless-check>`
      + :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`
      + :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`
      + :ref:`ext/session <ext-session>`
      + :ref:`ext/xml <ext-xml>`
      + :ref:`isset() With Constants <isset()-with-constants>`

    + `iterator`

      + :ref:`Could Type With Iterable <could-type-with-iterable>`
      + :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`
      + :ref:`ext/redis <ext-redis>`

    + `iterator_to_array()`

      + :ref:`Should Yield With Key <should-yield-with-key>`


+ `J`
    + `JSON_ERROR_NONE`

      + :ref:`Check JSON <check-json>`

    + `JSON_HEX_AMP`

      + :ref:`Is An Extension Constant <is-an-extension-constant>`

    + `JSON_OBJECT_AS_ARRAY`

      + :ref:`Use json_decode() Options <use-json\_decode()-options>`

    + `JSON_THROW_ON_ERROR`

      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`

    + `JsonException`

      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`

    + `JsonSerializable`

      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `Judy`

      + :ref:`ext/judy <ext-judy>`

    + `jdtojewish()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `json_decode()`

      + :ref:`Empty Json Error <empty-json-error>`
      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`
      + :ref:`Use json_decode() Options <use-json\_decode()-options>`

    + `json_encode()`

      + :ref:`Avoid Using stdClass <avoid-using-stdclass>`
      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`

    + `json_last_error()`

      + :ref:`Check JSON <check-json>`
      + :ref:`Empty Json Error <empty-json-error>`
      + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`

    + `json_last_error_msg()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `json_validate()`

      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `judy`

      + :ref:`ext/judy <ext-judy>`


+ `K`
    + `key()`

      + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`

    + `krsort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `ksort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`


+ `L`
    + `LC_ALL`

      + :ref:`Setlocale() Uses Constants <setlocale()-uses-constants>`
      + :ref:`Wrong Locale <wrong-locale>`
      + :ref:`ext/gettext <ext-gettext>`

    + `LC_MESSAGES`

      + :ref:`Setlocale() Uses Constants <setlocale()-uses-constants>`
      + :ref:`ext/gettext <ext-gettext>`

    + `LIBXML_DTDLOAD`

      + :ref:`No Net For Xml Load <no-net-for-xml-load>`

    + `LIBXML_ERR_ERROR`

      + :ref:`ext/libxml <ext-libxml>`

    + `LIBXML_ERR_FATAL`

      + :ref:`ext/libxml <ext-libxml>`

    + `LIBXML_ERR_WARNING`

      + :ref:`ext/libxml <ext-libxml>`

    + `LIBXML_NOENT`

      + :ref:`No Net For Xml Load <no-net-for-xml-load>`

    + `LOG_DEBUG`

      + :ref:`ext/rdkafka <ext-rdkafka>`

    + `List()`

      + :ref:`List With Array Appends <list-with-array-appends>`

    + `Locale`

      + :ref:`ext/intl <ext-intl>`

    + `LogicException`

      + :ref:`PHP Exception <php-exception>`

    + `ldap_connect()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `ldap_escape()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `ldap_exop_refresh()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `ldap_first_entry()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `ldap_list()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `ldap_read()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `ldap_search()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `libxml_clear_errors()`

      + :ref:`ext/libxml <ext-libxml>`

    + `libxml_get_errors()`

      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/xsl <ext-xsl>`

    + `libxml_set_external_entity_loader()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `link()`

      + :ref:`Make Class Method Definition <make-class-method-definition>`

    + `list()`

      + :ref:`Empty List <empty-list>`
      + :ref:`Foreach With list() <foreach-with-list()>`
      + :ref:`List Short Syntax <list-short-syntax>`
      + :ref:`List With Keys <list-with-keys>`
      + :ref:`No List With String <no-list-with-string>`
      + :ref:`Optimize Explode() <optimize-explode()>`
      + :ref:`Overwritten Source And Value <overwritten-source-and-value>`
      + :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`
      + :ref:`Should Use Explode Args <should-use-explode-args>`
      + :ref:`Spread Operator For Array <spread-operator-for-array>`
      + :ref:`Use List With Foreach <use-list-with-foreach>`
      + :ref:`list() May Omit Variables <list()-may-omit-variables>`

    + `locale`

      + :ref:`Confusing Names <confusing-names>`
      + :ref:`Fn Argument Variable Confusion <fn-argument-variable-confusion>`
      + :ref:`Wrong Locale <wrong-locale>`
      + :ref:`ext/ctype <ext-ctype>`
      + :ref:`ext/gettext <ext-gettext>`
      + :ref:`ext/intl <ext-intl>`

    + `localtime()`

      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `log()`

      + :ref:`Wrong Type For Native PHP Function <wrong-type-for-native-php-function>`

    + `ltrim()`

      + :ref:`Substr To Trim <substr-to-trim>`


+ `M`
    + `MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH`

      + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

    + `MYSQLI_STORE_RESULT_COPY_DATA`

      + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`

    + `M_PI`

      + :ref:`Constant Scalar Expression <constant-scalar-expression>`

    + `Match()`

      + :ref:`Could Use Match <could-use-match>`
      + :ref:`Simple Switch And Match <simple-switch-and-match>`

    + `MessageFormatter`

      + :ref:`Null On New <null-on-new>`

    + `Mongo`

      + :ref:`ext/mongodb <ext-mongodb>`

    + `MongoClient`

      + :ref:`ext/mongo <ext-mongo>`

    + `MongoDB`

      + :ref:`ext/mongo <ext-mongo>`
      + :ref:`ext/mongodb <ext-mongodb>`

    + `MongoDb`

      + :ref:`ext/mongodb <ext-mongodb>`

    + `Mongodb`

      + :ref:`ext/mongodb <ext-mongodb>`

    + `MySQLI`

      + :ref:`New On Functioncall Or Identifier <new-on-functioncall-or-identifier>`

    + `magic_quotes_runtime()`

      + :ref:`Functions Removed In PHP 5.4 <functions-removed-in-php-5.4>`
      + :ref:`PHP 7.0 Removed Functions <php-7.0-removed-functions>`

    + `mail()`

      + :ref:`Mail Usage <mail-usage>`
      + :ref:`ext/mail <ext-mail>`

    + `main()`

      + :ref:`Extensions/Exttaint <extensions-exttaint>`

    + `match()`

      + :ref:`Bracketless Blocks <bracketless-blocks>`
      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Could Use Match <could-use-match>`
      + :ref:`Identical Case In Switch <identical-case-in-switch>`
      + :ref:`Indentation Levels <indentation-levels>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Multiline Expressions <multiline-expressions>`
      + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
      + :ref:`Reserved Match Keyword <reserved-match-keyword>`
      + :ref:`Simple Switch And Match <simple-switch-and-match>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`Switch Without Default <switch-without-default>`
      + :ref:`Too Many Stringed Elseif <too-many-stringed-elseif>`
      + :ref:`Uses PHP 8 Match() <uses-php-8-match()>`
      + :ref:`Switch To Match <switch-to-match>`

    + `max()`

      + :ref:`No Max On Empty Array <no-max-on-empty-array>`

    + `mb_chr()`

      + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
      + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`

    + `mb_convert_encoding()`

      + :ref:`Deprecated Mb_string Encodings <deprecated-mb\_string-encodings>`

    + `mb_detect_encoding()`

      + :ref:`Deprecated Mb_string Encodings <deprecated-mb\_string-encodings>`

    + `mb_encoding_aliases()`

      + :ref:`Mbstring Unknown Encoding <mbstring-unknown-encoding>`
      + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`

    + `mb_list_encodings()`

      + :ref:`Mbstring Unknown Encoding <mbstring-unknown-encoding>`
      + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`

    + `mb_ord()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
      + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`

    + `mb_parse_str()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_scrub()`

      + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
      + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`

    + `mb_split()`

      + :ref:`Optimize Explode() <optimize-explode()>`

    + `mb_str_split()`

      + :ref:`New Functions In PHP 7.4 <new-functions-in-php-7.4>`

    + `mb_stripos()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_stristr()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_strlen()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`No Count With 0 <no-count-with-0>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `mb_strpos()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Use str_contains() <use-str\_contains()>`

    + `mb_strrchr()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_strrichr()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`

    + `mb_strripos()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_strrpos()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`mb_strrpos() Third Argument <mb\_strrpos()-third-argument>`

    + `mb_strstr()`

      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_strtolower()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_strtoupper()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `mb_substr()`

      + :ref:`Avoid Substr() One <avoid-substr()-one>`
      + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
      + :ref:`Mbstring Third Arg <mbstring-third-arg>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`
      + :ref:`Substr To Trim <substr-to-trim>`

    + `mb_substr_count()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `md5()`

      + :ref:`Directly Use File <directly-use-file>`

    + `md5_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `memory_reset_peak_usage()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `microtime()`

      + :ref:`Use random_int() <use-random\_int()>`

    + `min()`

      + :ref:`No Max On Empty Array <no-max-on-empty-array>`

    + `mkdir()`

      + :ref:`Keep Files Access Restricted <keep-files-access-restricted>`
      + :ref:`Mkdir Default <mkdir-default>`

    + `mktime()`

      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `money_format()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `mongo`

      + :ref:`ext/mongo <ext-mongo>`
      + :ref:`ext/mongodb <ext-mongodb>`

    + `mongodb`

      + :ref:`ext/mongodb <ext-mongodb>`

    + `move_uploaded_file()`

      + :ref:`move_uploaded_file Instead Of copy <move\_uploaded\_file-instead-of-copy>`

    + `msg_get_queue()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `mt_rand()`

      + :ref:`Use random_int() <use-random\_int()>`

    + `mt_srand()`

      + :ref:`Use random_int() <use-random\_int()>`

    + `mysql_error()`

      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`ext/mysql <ext-mysql>`

    + `mysqli`

      + :ref:`Use PHP Object API <use-php-object-api>`
      + :ref:`ext/mysql <ext-mysql>`
      + :ref:`ext/mysqli <ext-mysqli>`

    + `mysqli_begin_transaction()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `mysqli_connect_errno()`

      + :ref:`ext/mysqli <ext-mysqli>`

    + `mysqli_connect_error()`

      + :ref:`ext/mysqli <ext-mysqli>`

    + `mysqli_error_list()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `mysqli_execute_query()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`
      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `mysqli_fetch_column()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `mysqli_release_savepoint()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `mysqli_savepoint()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `mysqli_stmt_error_list()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`


+ `N`
    + `NCURSES_COLOR_BLACK`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `NCURSES_COLOR_GREEN`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `NCURSES_COLOR_RED`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `NCURSES_COLOR_WHITE`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `NULL`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
      + :ref:`Check All Types <check-all-types>`
      + :ref:`Check JSON <check-json>`
      + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
      + :ref:`Empty Slots In Arrays <empty-slots-in-arrays>`
      + :ref:`Implicit Nullable Type <implicit-nullable-type>`
      + :ref:`Method Property Confusion <method-property-confusion>`
      + :ref:`No Max On Empty Array <no-max-on-empty-array>`
      + :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`
      + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
      + :ref:`Should Use Coalesce <should-use-coalesce>`
      + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Used Static Properties <used-static-properties>`
      + :ref:`Useless NullSafe Operator <useless-nullsafe-operator>`
      + :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`
      + :ref:`ext/eio <ext-eio>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/xmlwriter <ext-xmlwriter>`
      + :ref:`version_compare() Operator <version\_compare()-operator>`

    + `Null`

      + :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
      + :ref:`Could Be Null <could-be-null>`
      + :ref:`Duplicate Literal <duplicate-literal>`
      + :ref:`Indices Are Int Or String <indices-are-int-or-string>`
      + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
      + :ref:`No Null For Native PHP Functions <no-null-for-native-php-functions>`
      + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
      + :ref:`Null Type Favorite <null-type-favorite>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Type Must Be Returned <type-must-be-returned>`
      + :ref:`Set Null Type <set-null-type>`
      + :ref:`Set Types <set-types>`

    + `NumberFormatter`

      + :ref:`ext/intl <ext-intl>`

    + `ncurses_init()`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `ncurses_start_color()`

      + :ref:`ext/ncurses <ext-ncurses>`

    + `net_get_interfaces()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `next()`

      + :ref:`Foreach Don't Change Pointer <foreach-don't-change-pointer>`
      + :ref:`Static Loop <static-loop>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `null`

      + :ref:`@ Operator <@-operator>`
      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Assumptions <assumptions>`
      + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
      + :ref:`Avoid Optional Properties <avoid-optional-properties>`
      + :ref:`Break With Non Integer <break-with-non-integer>`
      + :ref:`Casting Ternary <casting-ternary>`
      + :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
      + :ref:`Check All Types <check-all-types>`
      + :ref:`Check JSON <check-json>`
      + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Collect Literals <collect-literals>`
      + :ref:`Comparison Is Always The Same <comparison-is-always-the-same>`
      + :ref:`Constant Conditions <constant-conditions>`
      + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
      + :ref:`Could Be Null <could-be-null>`
      + :ref:`Could Be Ternary <could-be-ternary>`
      + :ref:`Could Merge Ternary Into Ifthen <could-merge-ternary-into-ifthen>`
      + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
      + :ref:`Could Use array_fill_keys <could-use-array\_fill\_keys>`
      + :ref:`Cyclic References <cyclic-references>`
      + :ref:`Default Then Discard <default-then-discard>`
      + :ref:`Dereferencing Levels <dereferencing-levels>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Don't Unset Properties <don't-unset-properties>`
      + :ref:`File Is Not Definitions Only <file-is-not-definitions-only>`
      + :ref:`Implicit Nullable Type <implicit-nullable-type>`
      + :ref:`Incompatible Types With Incoming Values <incompatible-types-with-incoming-values>`
      + :ref:`Indices Are Int Or String <indices-are-int-or-string>`
      + :ref:`Insufficient Property Type <insufficient-property-type>`
      + :ref:`Make Global A Property <make-global-a-property>`
      + :ref:`Methods Without Return <methods-without-return>`
      + :ref:`Mismatch Properties Types <mismatch-properties-types>`
      + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
      + :ref:`Mismatched Default Arguments <mismatched-default-arguments>`
      + :ref:`Mismatched Ternary Alternatives <mismatched-ternary-alternatives>`
      + :ref:`Missing Some Returntype <missing-some-returntype>`
      + :ref:`Mixed Type Usage <mixed-type-usage>`
      + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
      + :ref:`No Max On Empty Array <no-max-on-empty-array>`
      + :ref:`No Null For Index <no-null-for-index>`
      + :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`
      + :ref:`No Reference For Ternary <no-reference-for-ternary>`
      + :ref:`No get_class() With Null <no-get\_class()-with-null>`
      + :ref:`Non Nullable Getters <non-nullable-getters>`
      + :ref:`Null On New <null-on-new>`
      + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
      + :ref:`Null Type Favorite <null-type-favorite>`
      + :ref:`Nullable Without Check <nullable-without-check>`
      + :ref:`Objects Don't Need References <objects-don't-need-references>`
      + :ref:`Optional Parameter <optional-parameter>`
      + :ref:`PSR-16 Usage <psr-16-usage>`
      + :ref:`PSR-7 Usage <psr-7-usage>`
      + :ref:`Parent First <parent-first>`
      + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
      + :ref:`Remove Parameter With Named Parameters <remove-parameter-with-named-parameters>`
      + :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
      + :ref:`Results May Be Missing <results-may-be-missing>`
      + :ref:`Return void  <return-void->`
      + :ref:`Scalar Are Not Arrays <scalar-are-not-arrays>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Set Aside Code <set-aside-code>`
      + :ref:`Set Chaining Exception <set-chaining-exception>`
      + :ref:`Set Class Property Definition With Type <set-class-property-definition-with-type>`
      + :ref:`Should Deep Clone <should-deep-clone>`
      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`StandaloneType True False Null <standalonetype-true-false-null>`
      + :ref:`True False Inconsistant Case <true-false-inconsistant-case>`
      + :ref:`Typehinting Stats <typehinting-stats>`
      + :ref:`Unbinding Closures <unbinding-closures>`
      + :ref:`Uninitialized Property <uninitialized-property>`
      + :ref:`Unset In Foreach <unset-in-foreach>`
      + :ref:`Use === null <use-===-null>`
      + :ref:`Use Browscap <use-browscap>`
      + :ref:`Use Closure Trailing Comma <use-closure-trailing-comma>`
      + :ref:`Use Debug <use-debug>`
      + :ref:`Use NullSafe Operator <use-nullsafe-operator>`
      + :ref:`Use Nullable Type <use-nullable-type>`
      + :ref:`Useless Coalesce <useless-coalesce>`
      + :ref:`Useless Null Coalesce <useless-null-coalesce>`
      + :ref:`Useless NullSafe Operator <useless-nullsafe-operator>`
      + :ref:`Useless Short Ternary <useless-short-ternary>`
      + :ref:`Useless Type Check <useless-type-check>`
      + :ref:`Weak Typing <weak-typing>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`array_merge With Ellipsis <array\_merge-with-ellipsis>`
      + :ref:`ext/amqp <ext-amqp>`
      + :ref:`ext/eio <ext-eio>`
      + :ref:`ext/inotify <ext-inotify>`
      + :ref:`ext/newt <ext-newt>`
      + :ref:`ext/oci8 <ext-oci8>`
      + :ref:`ext/sdl <ext-sdl>`
      + :ref:`ext/uopz <ext-uopz>`
      + :ref:`isset() With Constants <isset()-with-constants>`
      + :ref:`Set Null Type <set-null-type>`


+ `O`
    + `OCI_ASSOC`

      + :ref:`ext/oci8 <ext-oci8>`

    + `OCI_RETURN_NULLS`

      + :ref:`ext/oci8 <ext-oci8>`

    + `OPENSSL_CIPHER_AES_128_CBC`

      + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`

    + `OPENSSL_CIPHER_RC2_40`

      + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`

    + `OPENSSL_KEYTYPE_EC`

      + :ref:`Check Crypto Key Length <check-crypto-key-length>`

    + `OP_HALFOPEN`

      + :ref:`ext/imap <ext-imap>`

    + `Override`

      + :ref:`Missing Overriden Method <missing-overriden-method>`
      + :ref:`Override Attribute <override-attribute>`
      + :ref:`Useless Override Attribute <useless-override-attribute>`

    + `ob_end_flush()`

      + :ref:`ext/ob <ext-ob>`

    + `ob_start()`

      + :ref:`ext/ob <ext-ob>`
      + :ref:`ext/tidy <ext-tidy>`

    + `oci_error()`

      + :ref:`ext/oci8 <ext-oci8>`

    + `oci_get_implicit_resultset()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `odbc_connection_string_is_quoted()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `odbc_connection_string_quote()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `odbc_connection_string_should_quote()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `opcache_get_status()`

      + :ref:`ext/opcache <ext-opcache>`

    + `opendir()`

      + :ref:`Avoid glob() Usage <avoid-glob()-usage>`

    + `openssl_cms_encrypt()`

      + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`

    + `openssl_csr_new()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `openssl_csr_sign()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `openssl_get_cipher_methods()`

      + :ref:`OpenSSL Ciphers Used <openssl-ciphers-used>`

    + `openssl_pbkdf2()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `openssl_pkcs7_encrypt()`

      + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`

    + `openssl_pkey_derive()`

      + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`

    + `openssl_pkey_new()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `openssl_random_pseudo_bytes()`

      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Use random_int() <use-random\_int()>`

    + `openssl_spki_export()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `openssl_spki_export_challenge()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `openssl_spki_new()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `openssl_spki_verify()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `openssl_x509_fingerprint()`

      + :ref:`New Functions In PHP 5.6 <new-functions-in-php-5.6>`

    + `openssl_x509_read()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `ord()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `override`

      + :ref:`Final Class Usage <final-class-usage>`
      + :ref:`Final Methods Usage <final-methods-usage>`
      + :ref:`Missing Overriden Method <missing-overriden-method>`
      + :ref:`Useless Override Attribute <useless-override-attribute>`


+ `P`
    + `PARENT`

      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`

    + `PASSWORD_ARGON2I`

      + :ref:`Argon2 Usage <argon2-usage>`

    + `PASSWORD_ARGON2_DEFAULT_THREADS`

      + :ref:`Argon2 Usage <argon2-usage>`

    + `PASSWORD_ARGON2_DEFAULT_TIME_COST`

      + :ref:`Argon2 Usage <argon2-usage>`

    + `PASSWORD_DEFAULT`

      + :ref:`Use password_hash() <use-password\_hash()>`

    + `PATHINFO_BASENAME`

      + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

    + `PATHINFO_DIRNAME`

      + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

    + `PDO`

      + :ref:`Don't Be Too Manual <don't-be-too-manual>`
      + :ref:`Should Use Prepared Statement <should-use-prepared-statement>`
      + :ref:`ext/pdo <ext-pdo>`

    + `PHP_EOL`

      + :ref:`Compare Hash <compare-hash>`
      + :ref:`Constants Usage <constants-usage>`
      + :ref:`Don't Change The Blind Var <don't-change-the-blind-var>`
      + :ref:`File Uploads <file-uploads>`
      + :ref:`Final Class Usage <final-class-usage>`
      + :ref:`Final Methods Usage <final-methods-usage>`
      + :ref:`Joining file() <joining-file()>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`New Line Style <new-line-style>`
      + :ref:`Next Month Trap <next-month-trap>`
      + :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`
      + :ref:`PHP Constant Usage <php-constant-usage>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Restrict Global Usage <restrict-global-usage>`
      + :ref:`Same Variable Foreach <same-variable-foreach>`
      + :ref:`Should Have Destructor <should-have-destructor>`
      + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
      + :ref:`Should Yield With Key <should-yield-with-key>`
      + :ref:`Useless Instructions <useless-instructions>`
      + :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`
      + :ref:`ext/amqp <ext-amqp>`
      + :ref:`ext/apc <ext-apc>`
      + :ref:`ext/array <ext-array>`
      + :ref:`ext/crypto <ext-crypto>`
      + :ref:`ext/date <ext-date>`
      + :ref:`ext/db2 <ext-db2>`
      + :ref:`ext/dba <ext-dba>`
      + :ref:`ext/enchant <ext-enchant>`
      + :ref:`ext/ev <ext-ev>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/expect <ext-expect>`
      + :ref:`ext/file <ext-file>`
      + :ref:`ext/fileinfo <ext-fileinfo>`
      + :ref:`ext/filter <ext-filter>`
      + :ref:`ext/gearman <ext-gearman>`
      + :ref:`ext/gender <ext-gender>`
      + :ref:`ext/gmp <ext-gmp>`
      + :ref:`ext/iconv <ext-iconv>`
      + :ref:`ext/imap <ext-imap>`
      + :ref:`ext/judy <ext-judy>`
      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/math <ext-math>`
      + :ref:`ext/mcrypt <ext-mcrypt>`
      + :ref:`ext/mongo <ext-mongo>`
      + :ref:`ext/ncurses <ext-ncurses>`
      + :ref:`ext/oci8 <ext-oci8>`
      + :ref:`ext/parle <ext-parle>`
      + :ref:`ext/reflection <ext-reflection>`
      + :ref:`ext/sdl <ext-sdl>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/spl <ext-spl>`
      + :ref:`ext/standard <ext-standard>`
      + :ref:`ext/xdiff <ext-xdiff>`
      + :ref:`ext/xhprof <ext-xhprof>`
      + :ref:`ext/zip <ext-zip>`
      + :ref:`foreach() On Object <foreach()-on-object>`

    + `PHP_INT_MAX`

      + :ref:`Manipulates INF <manipulates-inf>`

    + `PHP_OS`

      + :ref:`Multiple Constant Definition <multiple-constant-definition>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`

    + `PHP_SHLIB_SUFFIX`

      + :ref:`Dl() Usage <dl()-usage>`
      + :ref:`Dynamic Library Loading <dynamic-library-loading>`
      + :ref:`ext/vips <ext-vips>`

    + `PHP_VERSION`

      + :ref:`Custom Constant Usage <custom-constant-usage>`
      + :ref:`Is CLI Script <is-cli-script>`
      + :ref:`Is Global Constant <is-global-constant>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`Redeclared PHP Functions <redeclared-php-functions>`
      + :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`

    + `PREG_JIT_STACKLIMIT_ERROR`

      + :ref:`Use Constants As Returns <use-constants-as-returns>`

    + `PREG_NO_ERROR`

      + :ref:`Use Constants As Returns <use-constants-as-returns>`

    + `PREG_SET_ORDER`

      + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`

    + `PREG_SPLIT_NO_EMPTY`

      + :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`

    + `PSPELL_FAST`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `PSPELL_RUN_TOGETHER`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `Parent`

      + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Set Class Method Remote Definition <set-class-method-remote-definition>`

    + `ParseError`

      + :ref:`eval() Without Try <eval()-without-try>`

    + `Pdo`

      + :ref:`Set Aside Code <set-aside-code>`

    + `Phar`

      + :ref:`Can't Disable Class <can't-disable-class>`
      + :ref:`__halt_compiler <\_\_halt\_compiler>`
      + :ref:`ext/phar <ext-phar>`

    + `pack()`

      + :ref:`Invalid Pack Format <invalid-pack-format>`
      + :ref:`Pack Format Inventory <pack-format-inventory>`
      + :ref:`Inventory <inventory>`

    + `parent`

      + :ref:`Abstract Class Constants <abstract-class-constants>`
      + :ref:`Abstract Static Methods <abstract-static-methods>`
      + :ref:`Already Parents Trait <already-parents-trait>`
      + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
      + :ref:`Cancel Common Method <cancel-common-method>`
      + :ref:`Class Without Parent <class-without-parent>`
      + :ref:`Collect Class Depth <collect-class-depth>`
      + :ref:`Constant Used Below <constant-used-below>`
      + :ref:`Could Be Abstract Class <could-be-abstract-class>`
      + :ref:`Could Be Parent Method <could-be-parent-method>`
      + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
      + :ref:`Cyclic References <cyclic-references>`
      + :ref:`Defined Class Constants <defined-class-constants>`
      + :ref:`Defined Parent MP <defined-parent-mp>`
      + :ref:`Different Constructors <different-constructors>`
      + :ref:`Disconnected Classes <disconnected-classes>`
      + :ref:`Empty Function <empty-function>`
      + :ref:`Fossilized Method <fossilized-method>`
      + :ref:`Fossilized Methods List <fossilized-methods-list>`
      + :ref:`Identical Methods <identical-methods>`
      + :ref:`Incompatible Signature Methods <incompatible-signature-methods>`
      + :ref:`Incompatible Signature Methods With Covariance <incompatible-signature-methods-with-covariance>`
      + :ref:`Is Upper Family <is-upper-family>`
      + :ref:`Locally Unused Property <locally-unused-property>`
      + :ref:`Method Used Below <method-used-below>`
      + :ref:`Mismatch Properties Types <mismatch-properties-types>`
      + :ref:`Missing Overriden Method <missing-overriden-method>`
      + :ref:`Multiple Identical Trait Or Interface <multiple-identical-trait-or-interface>`
      + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`
      + :ref:`Never Used Properties <never-used-properties>`
      + :ref:`Override Attribute <override-attribute>`
      + :ref:`Overwritten Class Constants <overwritten-class-constants>`
      + :ref:`Overwritten Constant <overwritten-constant>`
      + :ref:`PHP7 Dirname <php7-dirname>`
      + :ref:`Parent First <parent-first>`
      + :ref:`Parent Is Not Static <parent-is-not-static>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Property Used Above <property-used-above>`
      + :ref:`Property Used Below <property-used-below>`
      + :ref:`Redefined Property <redefined-property>`
      + :ref:`Repeated Interface <repeated-interface>`
      + :ref:`Set Chaining Exception <set-chaining-exception>`
      + :ref:`Set Parent Definition <set-parent-definition>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Too Many Children <too-many-children>`
      + :ref:`Type Dodging <type-dodging>`
      + :ref:`Typed Class Constants Usage <typed-class-constants-usage>`
      + :ref:`Undefined Class Constants <undefined-class-constants>`
      + :ref:`Undefined Parent <undefined-parent>`
      + :ref:`Undefined static:: Or self:: <undefined-static-or-self>`
      + :ref:`Unreachable Method <unreachable-method>`
      + :ref:`Unresolved Classes <unresolved-classes>`
      + :ref:`Unused Interfaces <unused-interfaces>`
      + :ref:`Unused Parameter <unused-parameter>`
      + :ref:`Use Contravariance <use-contravariance>`
      + :ref:`Use Covariance <use-covariance>`
      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
      + :ref:`Used Once Variables (In Scope) <used-once-variables-(in-scope)>`
      + :ref:`Used Protected Method <used-protected-method>`
      + :ref:`Useless Constant Overwrite <useless-constant-overwrite>`
      + :ref:`Useless Constructor <useless-constructor>`
      + :ref:`Useless Method <useless-method>`
      + :ref:`Useless Override Attribute <useless-override-attribute>`
      + :ref:`ext/pcntl <ext-pcntl>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`
      + :ref:`Set Types <set-types>`

    + `parse_ini_file()`

      + :ref:`Directly Use File <directly-use-file>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `parse_ini_string()`

      + :ref:`Directly Use File <directly-use-file>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `parse_str()`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`PHP 7.2 Deprecations <php-7.2-deprecations>`
      + :ref:`Register Globals <register-globals>`
      + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
      + :ref:`parse_str() Warning <parse\_str()-warning>`

    + `parse_url()`

      + :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`
      + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `passthru()`

      + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`

    + `password_algos()`

      + :ref:`New Functions In PHP 7.4 <new-functions-in-php-7.4>`

    + `password_get_info()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `password_hash()`

      + :ref:`Compare Hash <compare-hash>`
      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`
      + :ref:`Use password_hash() <use-password\_hash()>`
      + :ref:`ext/password <ext-password>`

    + `password_needs_rehash()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `password_verify()`

      + :ref:`Compare Hash <compare-hash>`
      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `pathinfo()`

      + :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`
      + :ref:`Use Pathinfo <use-pathinfo>`
      + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

    + `pcntl_fork()`

      + :ref:`ext/pcntl <ext-pcntl>`

    + `pcntl_getpriority()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `pdo`

      + :ref:`Don't Be Too Manual <don't-be-too-manual>`

    + `pg_connect()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pg_escape_identifier()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `pg_escape_literal()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `pg_lo_create()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pg_pconnect()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pg_query()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pg_result_status()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `pg_select()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `phar`

      + :ref:`Can't Disable Class <can't-disable-class>`
      + :ref:`Use Basename Suffix <use-basename-suffix>`
      + :ref:`ext/phar <ext-phar>`

    + `php_logo_guid()`

      + :ref:`Functions Removed In PHP 5.5 <functions-removed-in-php-5.5>`

    + `php_sapi_name()`

      + :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`

    + `php_user_filter`

      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `php_version`

      + :ref:`Should Use Operator <should-use-operator>`
      + :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`

    + `phpcredits()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `phpinfo()`

      + :ref:`Eval() Usage <eval()-usage>`
      + :ref:`Phpinfo <phpinfo>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `phpversion()`

      + :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`

    + `pi()`

      + :ref:`Use Constant Instead Of Function <use-constant-instead-of-function>`

    + `posix_access()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `posix_fpathconf()`

      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `posix_get_last_error()`

      + :ref:`ext/posix <ext-posix>`

    + `posix_pathconf()`

      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `posix_setrlimit()`

      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`

    + `posix_setsid()`

      + :ref:`ext/pcntl <ext-pcntl>`

    + `posix_sysconf()`

      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `pow()`

      + :ref:`** For Exponent <**-for-exponent>`
      + :ref:`Negative Power <negative-power>`

    + `preg_filter()`

      + :ref:`Regex On Arrays <regex-on-arrays>`

    + `preg_grep()`

      + :ref:`Regex On Arrays <regex-on-arrays>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `preg_last_error()`

      + :ref:`Use Constants As Returns <use-constants-as-returns>`

    + `preg_last_error_msg()`

      + :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`

    + `preg_match()`

      + :ref:`Regex Delimiter <regex-delimiter>`
      + :ref:`Regex Inventory <regex-inventory>`
      + :ref:`Results May Be Missing <results-may-be-missing>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `preg_match_all()`

      + :ref:`Php Native Reference Variable <php-native-reference-variable>`
      + :ref:`Regex Delimiter <regex-delimiter>`
      + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`

    + `preg_replace()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`
      + :ref:`Possible Missing Subpattern <possible-missing-subpattern>`
      + :ref:`Processing Collector <processing-collector>`
      + :ref:`Regex Delimiter <regex-delimiter>`
      + :ref:`Regex Inventory <regex-inventory>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`preg_replace With Option e <preg\_replace-with-option-e>`

    + `preg_replace_callback()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`
      + :ref:`Regex Delimiter <regex-delimiter>`
      + :ref:`Regex On Arrays <regex-on-arrays>`
      + :ref:`preg_replace With Option e <preg\_replace-with-option-e>`

    + `preg_replace_callback_array()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`
      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`
      + :ref:`Regex Delimiter <regex-delimiter>`
      + :ref:`Regex On Arrays <regex-on-arrays>`
      + :ref:`preg_replace With Option e <preg\_replace-with-option-e>`

    + `preg_split()`

      + :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`
      + :ref:`Optimize Explode() <optimize-explode()>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `prev()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `print()`

      + :ref:`Property Export <property-export>`

    + `print_r()`

      + :ref:`Use Debug <use-debug>`
      + :ref:`var_dump()... Usage <var\_dump()...-usage>`

    + `printf()`

      + :ref:`Echo Or Print <echo-or-print>`
      + :ref:`Printf Format Inventory <printf-format-inventory>`
      + :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`
      + :ref:`ext/ffi <ext-ffi>`
      + :ref:`Inventory <inventory>`

    + `proc_nice()`

      + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`

    + `proc_open()`

      + :ref:`Shell commands <shell-commands>`

    + `property_exists()`

      + :ref:`Checks Property Existence <checks-property-existence>`

    + `pspell_config_create()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pspell_new()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pspell_new_config()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`

    + `pspell_new_personal()`

      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`


+ `R`
    + `Randomizer`

      + :ref:`Random extension <random-extension>`

    + `RarArchive`

      + :ref:`ext/rar <ext-rar>`

    + `RecursiveFilterIterator`

      + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`

    + `Reflection`

      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
      + :ref:`ext/reflection <ext-reflection>`

    + `ReflectionClassConstant`

      + :ref:`Php 7.1 New Class <php-7.1-new-class>`

    + `ReflectionFunction`

      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
      + :ref:`ext/reflection <ext-reflection>`

    + `Reflector`

      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`

    + `ResourceBundle`

      + :ref:`Sylius usage <sylius-usage>`

    + `ReturnTypeWillChange`

      + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`
      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`

    + `RuntimeException`

      + :ref:`Caught Variable <caught-variable>`
      + :ref:`Defined Exceptions <defined-exceptions>`
      + :ref:`Multiple Catch With Try <multiple-catch-with-try>`
      + :ref:`Resources Usage <resources-usage>`
      + :ref:`Throw Functioncall <throw-functioncall>`

    + `rand()`

      + :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
      + :ref:`Only Variable Returned By Reference <only-variable-returned-by-reference>`
      + :ref:`Too Many Chained Calls <too-many-chained-calls>`
      + :ref:`Use random_int() <use-random\_int()>`

    + `random_bytes()`

      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`
      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Use random_int() <use-random\_int()>`

    + `random_int()`

      + :ref:`Abstract Away <abstract-away>`
      + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`
      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Use random_int() <use-random\_int()>`

    + `randomizer`

      + :ref:`Random extension <random-extension>`

    + `readdir()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `readfile()`

      + :ref:`Joining file() <joining-file()>`

    + `readline_info()`

      + :ref:`ext/readline <ext-readline>`

    + `reflection`

      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
      + :ref:`ext/reflection <ext-reflection>`

    + `register_shutdown_function()`

      + :ref:`Callback Function Needs Return <callback-function-needs-return>`
      + :ref:`Definitions Only <definitions-only>`

    + `register_tick_function()`

      + :ref:`Callback Function Needs Return <callback-function-needs-return>`
      + :ref:`Ticks Usage <ticks-usage>`

    + `restore_include_path()`

      + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
      + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
      + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`

    + `result`

      + :ref:`** For Exponent <**-for-exponent>`
      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
      + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
      + :ref:`Casting Ternary <casting-ternary>`
      + :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
      + :ref:`Check Division By Zero <check-division-by-zero>`
      + :ref:`Collect Classes Dependencies <collect-classes-dependencies>`
      + :ref:`Compared Comparison <compared-comparison>`
      + :ref:`Comparison On Different Types <comparison-on-different-types>`
      + :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
      + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
      + :ref:`Crc32() Might Be Negative <crc32()-might-be-negative>`
      + :ref:`Don't Be Too Manual <don't-be-too-manual>`
      + :ref:`Don't Collect Void <don't-collect-void>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Don't Unset Properties <don't-unset-properties>`
      + :ref:`Double Instructions <double-instructions>`
      + :ref:`Empty With Expression <empty-with-expression>`
      + :ref:`Foreach Needs Reference Array <foreach-needs-reference-array>`
      + :ref:`Function Subscripting <function-subscripting>`
      + :ref:`Identical Consecutive Expression <identical-consecutive-expression>`
      + :ref:`Identical On Both Sides <identical-on-both-sides>`
      + :ref:`Implied If <implied-if>`
      + :ref:`Joining file() <joining-file()>`
      + :ref:`Large Try Block <large-try-block>`
      + :ref:`Law of Demeter <law-of-demeter>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Method Is Overwritten <method-is-overwritten>`
      + :ref:`Methodcall On New <methodcall-on-new>`
      + :ref:`Mismatched Ternary Alternatives <mismatched-ternary-alternatives>`
      + :ref:`No A Valid Cast <no-a-valid-cast>`
      + :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`
      + :ref:`No get_class() With Null <no-get\_class()-with-null>`
      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Possible Missing Subpattern <possible-missing-subpattern>`
      + :ref:`Property Export <property-export>`
      + :ref:`Self-Transforming Variables <self-transforming-variables>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Substring First <substring-first>`
      + :ref:`Too Many Chained Calls <too-many-chained-calls>`
      + :ref:`Upload Filename Injection <upload-filename-injection>`
      + :ref:`Use PHP Object API <use-php-object-api>`
      + :ref:`Useless Instructions <useless-instructions>`
      + :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`
      + :ref:`Wordpress usage <wordpress-usage>`
      + :ref:`Written Only Variables <written-only-variables>`
      + :ref:`ext/gearman <ext-gearman>`
      + :ref:`ext/gender <ext-gender>`
      + :ref:`ext/ldap <ext-ldap>`
      + :ref:`ext/mongodb <ext-mongodb>`
      + :ref:`ext/mysql <ext-mysql>`
      + :ref:`ext/mysqli <ext-mysqli>`
      + :ref:`ext/pgsql <ext-pgsql>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/sphinx <ext-sphinx>`
      + :ref:`ext/sqlite <ext-sqlite>`
      + :ref:`ext/svm <ext-svm>`
      + :ref:`ext/xsl <ext-xsl>`
      + :ref:`isset() With Constants <isset()-with-constants>`
      + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`

    + `round()`

      + :ref:`Do Not Cast To Int <do-not-cast-to-int>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `rsort()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `rtrim()`

      + :ref:`Substr To Trim <substr-to-trim>`


+ `S`
    + `SCANDIR_SORT_NONE`

      + :ref:`Avoid glob() Usage <avoid-glob()-usage>`

    + `SDL_GetError()`

      + :ref:`ext/sdl <ext-sdl>`

    + `SDL_INIT_VIDEO`

      + :ref:`ext/sdl <ext-sdl>`

    + `SDL_Quit()`

      + :ref:`ext/sdl <ext-sdl>`

    + `SELF`

      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`

    + `SIGHUP`

      + :ref:`ext/pcntl <ext-pcntl>`

    + `SIGKILL`

      + :ref:`ext/posix <ext-posix>`

    + `SIGTERM`

      + :ref:`ext/pcntl <ext-pcntl>`

    + `SNMP`

      + :ref:`ext/snmp <ext-snmp>`

    + `SOAP_1_2`

      + :ref:`ext/soap <ext-soap>`

    + `SOCK_STREAM`

      + :ref:`ext/sockets <ext-sockets>`

    + `SOL_TCP`

      + :ref:`ext/sockets <ext-sockets>`

    + `SORT_FLAG_CASE`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SORT_LOCALE_STRING`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SORT_NATURAL`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SORT_NUMERIC`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SORT_REGULAR`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SORT_STRING`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `SQLITE3_ASSOC`

      + :ref:`Fetch One Row Format <fetch-one-row-format>`

    + `SQLITE3_BOTH`

      + :ref:`Fetch One Row Format <fetch-one-row-format>`

    + `SQLITE3_NUM`

      + :ref:`Fetch One Row Format <fetch-one-row-format>`

    + `SQLite3`

      + :ref:`Queries In Loops <queries-in-loops>`
      + :ref:`ext/sqlite3 <ext-sqlite3>`

    + `STDERR`

      + :ref:`ext/sdl <ext-sdl>`

    + `Secure`

      + :ref:`Random extension <random-extension>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`

    + `Self`

      + :ref:`Avoid Self In Interface <avoid-self-in-interface>`

    + `SensitiveParameter`

      + :ref:`Indirect Injection <indirect-injection>`
      + :ref:`PHP Native Attributes <php-native-attributes>`

    + `SessionHandlerInterface`

      + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
      + :ref:`Session Lazy Write <session-lazy-write>`

    + `SessionUpdateTimestampHandlerInterface`

      + :ref:`PHP 7.0 New Interfaces <php-7.0-new-interfaces>`
      + :ref:`Session Lazy Write <session-lazy-write>`

    + `Shmop`

      + :ref:`ext/shmop <ext-shmop>`

    + `SimpleXMLElement`

      + :ref:`ext/simplexml <ext-simplexml>`

    + `SoapClient`

      + :ref:`ext/soap <ext-soap>`

    + `Socket`

      + :ref:`No Initial S In Variable Names <no-initial-s-in-variable-names>`
      + :ref:`ext/0mq <ext-0mq>`
      + :ref:`ext/sockets <ext-sockets>`

    + `SplFileObject`

      + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`

    + `SplQueue`

      + :ref:`PHP 7.2 Scalar Types <php-7.2-scalar-types>`

    + `Sqlite3`

      + :ref:`Don't Use The Type As Variable Name <don't-use-the-type-as-variable-name>`
      + :ref:`Fetch One Row Format <fetch-one-row-format>`
      + :ref:`Set Aside Code <set-aside-code>`
      + :ref:`ext/sqlite3 <ext-sqlite3>`

    + `Static`

      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Abstract Static Methods <abstract-static-methods>`
      + :ref:`Assign Default To Properties <assign-default-to-properties>`
      + :ref:`Cannot Call Static Trait Method Directly <cannot-call-static-trait-method-directly>`
      + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
      + :ref:`Collect Local Variable Counts <collect-local-variable-counts>`
      + :ref:`Create Magic Method <create-magic-method>`
      + :ref:`Declare Global Early <declare-global-early>`
      + :ref:`Function With Dynamic Code <function-with-dynamic-code>`
      + :ref:`Inherited Static Variable <inherited-static-variable>`
      + :ref:`Magic Properties <magic-properties>`
      + :ref:`No Reference For Static Property <no-reference-for-static-property>`
      + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
      + :ref:`Normal Methods <normal-methods>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Real Variables <real-variables>`
      + :ref:`Redeclared Static Variable <redeclared-static-variable>`
      + :ref:`Set Class Method Remote Definition <set-class-method-remote-definition>`
      + :ref:`Should Be Single Quote <should-be-single-quote>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Static Call May Be Truly Static <static-call-may-be-truly-static>`
      + :ref:`Static Loop <static-loop>`
      + :ref:`Static Methods Called From Object <static-methods-called-from-object>`
      + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
      + :ref:`Static Variable Can Default To Arbitrary Expression <static-variable-can-default-to-arbitrary-expression>`
      + :ref:`Static Variable In Namespace <static-variable-in-namespace>`
      + :ref:`Static Variable Initialisation <static-variable-initialisation>`
      + :ref:`Static Variables <static-variables>`
      + :ref:`Used Once Variables (In Scope) <used-once-variables-(in-scope)>`
      + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`
      + :ref:`ext/reflection <ext-reflection>`

    + `StdClass`

      + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
      + :ref:`PHP 7.2 Scalar Types <php-7.2-scalar-types>`

    + `Stdclass`

      + :ref:`Avoid get_class() <avoid-get\_class()>`
      + :ref:`Could Use array_fill_keys <could-use-array\_fill\_keys>`
      + :ref:`Global Import <global-import>`
      + :ref:`Is An Extension Class <is-an-extension-class>`
      + :ref:`Missing Parenthesis <missing-parenthesis>`
      + :ref:`Should Deep Clone <should-deep-clone>`
      + :ref:`Unresolved Catch <unresolved-catch>`
      + :ref:`array_key_exists() Works On Arrays <array\_key\_exists()-works-on-arrays>`
      + :ref:`foreach() On Object <foreach()-on-object>`

    + `Stringable`

      + :ref:`Could Be Stringable <could-be-stringable>`

    + `Strtr()`

      + :ref:`Strtr Arguments <strtr-arguments>`

    + `Substr()`

      + :ref:`Drop Substr Last Arg <drop-substr-last-arg>`

    + `Switch()`

      + :ref:`Missing Cases In Switch <missing-cases-in-switch>`
      + :ref:`Simple Switch And Match <simple-switch-and-match>`

    + `scandir()`

      + :ref:`Avoid glob() Usage <avoid-glob()-usage>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `secure`

      + :ref:`Avoid Those Hash Functions <avoid-those-hash-functions>`
      + :ref:`Session Lazy Write <session-lazy-write>`
      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Use random_int() <use-random\_int()>`
      + :ref:`ext/libsodium <ext-libsodium>`
      + :ref:`ext/password <ext-password>`
      + :ref:`ext/scrypt <ext-scrypt>`
      + :ref:`ext/xxtea <ext-xxtea>`

    + `self`

      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Abstract Static Methods <abstract-static-methods>`
      + :ref:`Array Access On Literal Array <array-access-on-literal-array>`
      + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
      + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
      + :ref:`Const With Array <const-with-array>`
      + :ref:`Constant Class <constant-class>`
      + :ref:`Constant Used Below <constant-used-below>`
      + :ref:`Could Be Private Class Constant <could-be-private-class-constant>`
      + :ref:`Could Be Protected Class Constant <could-be-protected-class-constant>`
      + :ref:`Could Use self <could-use-self>`
      + :ref:`Defined Class Constants <defined-class-constants>`
      + :ref:`Defined static:: Or self:: <defined-static-or-self>`
      + :ref:`Deprecated Callable <deprecated-callable>`
      + :ref:`Detect Current Class <detect-current-class>`
      + :ref:`Feast usage <feast-usage>`
      + :ref:`Is Not Class Family <is-not-class-family>`
      + :ref:`Method Could Be Static <method-could-be-static>`
      + :ref:`No Self Referencing Constant <no-self-referencing-constant>`
      + :ref:`No Static Variable In A Method <no-static-variable-in-a-method>`
      + :ref:`Overwritten Class Constants <overwritten-class-constants>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Php7 Relaxed Keyword <php7-relaxed-keyword>`
      + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
      + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
      + :ref:`Self Using Trait <self-using-trait>`
      + :ref:`Should Use Math <should-use-math>`
      + :ref:`Solve Trait Constants <solve-trait-constants>`
      + :ref:`Static Call With Self <static-call-with-self>`
      + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
      + :ref:`Static Methods Cannot Call Non-Static Methods <static-methods-cannot-call-non-static-methods>`
      + :ref:`Undefined static:: Or self:: <undefined-static-or-self>`
      + :ref:`Unused Class Constant <unused-class-constant>`
      + :ref:`Unused Methods <unused-methods>`
      + :ref:`Unused Private Methods <unused-private-methods>`
      + :ref:`Upload Filename Injection <upload-filename-injection>`
      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
      + :ref:`Used Once Property <used-once-property>`
      + :ref:`Used Private Methods <used-private-methods>`
      + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`
      + :ref:`ext/pcov <ext-pcov>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`
      + :ref:`strip_tags() Skips Closed Tag <strip\_tags()-skips-closed-tag>`

    + `sem_get()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `session_register_shutdown()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `session_start()`

      + :ref:`Should Use session_regenerateid() <should-use-session\_regenerateid()>`
      + :ref:`Use session_start() Options <use-session\_start()-options>`
      + :ref:`ext/session <ext-session>`

    + `session_status()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `set_error_handler()`

      + :ref:`Avoid set_error_handler $context Argument <avoid-set\_error\_handler-$context-argument>`
      + :ref:`Definitions Only <definitions-only>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`

    + `set_exception_handler()`

      + :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`

    + `set_magic_quotes_runtime()`

      + :ref:`PHP 7.0 Removed Functions <php-7.0-removed-functions>`

    + `setcookie()`

      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`
      + :ref:`Use Cookies <use-cookies>`

    + `setlocale()`

      + :ref:`Collect SetLocale <collect-setlocale>`
      + :ref:`Setlocale() Uses Constants <setlocale()-uses-constants>`

    + `setrawcookie()`

      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`
      + :ref:`Use Cookies <use-cookies>`

    + `settype()`

      + :ref:`Should Typecast <should-typecast>`

    + `sha1()`

      + :ref:`Directly Use File <directly-use-file>`

    + `sha1_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `shell_exec()`

      + :ref:`Missing Some Returntype <missing-some-returntype>`
      + :ref:`Shell Favorite <shell-favorite>`
      + :ref:`Shell commands <shell-commands>`
      + :ref:`Preferences <preferences>`

    + `shm_attach()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `shmop`

      + :ref:`ext/shmop <ext-shmop>`

    + `shmop_open()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `show_source()`

      + :ref:`Directly Use File <directly-use-file>`

    + `simplexml_load_file()`

      + :ref:`Directly Use File <directly-use-file>`

    + `simplexml_load_string()`

      + :ref:`Directly Use File <directly-use-file>`

    + `sizeof()`

      + :ref:`Useless Check <useless-check>`

    + `sleep()`

      + :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`

    + `snmp`

      + :ref:`ext/snmp <ext-snmp>`

    + `socket`

      + :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/sockets <ext-sockets>`
      + :ref:`ext/varnish <ext-varnish>`

    + `socket_accept()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `socket_addrinfo_bind()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `socket_addrinfo_connect()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `socket_atmark()`

      + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`

    + `socket_cmsg_space()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `socket_connect()`

      + :ref:`ext/sockets <ext-sockets>`

    + `socket_create()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
      + :ref:`ext/sockets <ext-sockets>`

    + `socket_create_listen()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `socket_import_stream()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`
      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `socket_last_error()`

      + :ref:`ext/sockets <ext-sockets>`

    + `socket_read()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `socket_recvmsg()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `socket_sendmsg()`

      + :ref:`New Functions In PHP 5.5 <new-functions-in-php-5.5>`

    + `sodium_crypto_core_ristretto255_add()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_from_hash()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_is_valid_point()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_random()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_add()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_complement()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_invert()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_mul()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_negate()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_random()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_reduce()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_scalar_sub()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_core_ristretto255_sub()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_scalarmult_ristretto255()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_scalarmult_ristretto255_base()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_stream_xchacha20()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_stream_xchacha20_keygen()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_stream_xchacha20_xor()`

      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`

    + `sodium_crypto_stream_xchacha20_xor_ic()`

      + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`

    + `sort()`

      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Php Native Reference Variable <php-native-reference-variable>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `spl_autoload_register()`

      + :ref:`Definitions Only <definitions-only>`

    + `sprintf()`

      + :ref:`Printf Format Inventory <printf-format-inventory>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

    + `sqlite3`

      + :ref:`Don't Use The Type As Variable Name <don't-use-the-type-as-variable-name>`
      + :ref:`Set Aside Code <set-aside-code>`

    + `sqlsrv_errors()`

      + :ref:`ext/sqlsrv <ext-sqlsrv>`

    + `srand()`

      + :ref:`Use random_int() <use-random\_int()>`

    + `sscanf()`

      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

    + `static`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
      + :ref:`Abstract Static Methods <abstract-static-methods>`
      + :ref:`Ambiguous Static <ambiguous-static>`
      + :ref:`An OOP Factory <an-oop-factory>`
      + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
      + :ref:`Calling Static Trait Method <calling-static-trait-method>`
      + :ref:`Can't Instantiate Class <can't-instantiate-class>`
      + :ref:`Cannot Call Static Trait Method Directly <cannot-call-static-trait-method-directly>`
      + :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
      + :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
      + :ref:`Class Invasion <class-invasion>`
      + :ref:`Class Usage <class-usage>`
      + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
      + :ref:`Collect Classes Dependencies <collect-classes-dependencies>`
      + :ref:`Collect Definitions Statistics <collect-definitions-statistics>`
      + :ref:`Constant Conditions <constant-conditions>`
      + :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
      + :ref:`Constant Order <constant-order>`
      + :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
      + :ref:`Could Be A Static Variable <could-be-a-static-variable>`
      + :ref:`Could Be Static Closure <could-be-static-closure>`
      + :ref:`Could Be Typed Callable <could-be-typed-callable>`
      + :ref:`Create Foreach Default <create-foreach-default>`
      + :ref:`Declare Global Early <declare-global-early>`
      + :ref:`Declare Static Once <declare-static-once>`
      + :ref:`Defined Parent MP <defined-parent-mp>`
      + :ref:`Defined static:: Or self:: <defined-static-or-self>`
      + :ref:`Dependant Abstract Classes <dependant-abstract-classes>`
      + :ref:`Dependant Trait <dependant-trait>`
      + :ref:`Detect Current Class <detect-current-class>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Don't Unset Properties <don't-unset-properties>`
      + :ref:`Dynamic Calls <dynamic-calls>`
      + :ref:`Dynamic Classes <dynamic-classes>`
      + :ref:`Dynamic Library Loading <dynamic-library-loading>`
      + :ref:`Dynamic Methodcall <dynamic-methodcall>`
      + :ref:`Dynamic Property <dynamic-property>`
      + :ref:`Enum Case Values <enum-case-values>`
      + :ref:`File Is Not Definitions Only <file-is-not-definitions-only>`
      + :ref:`Foreach Needs Reference Array <foreach-needs-reference-array>`
      + :ref:`Forgotten Visibility <forgotten-visibility>`
      + :ref:`Fuel PHP Usage <fuel-php-usage>`
      + :ref:`Global Inside Loop <global-inside-loop>`
      + :ref:`Inherited Static Variable <inherited-static-variable>`
      + :ref:`Is Not Class Family <is-not-class-family>`
      + :ref:`Is Upper Family <is-upper-family>`
      + :ref:`Magic Visibility <magic-visibility>`
      + :ref:`Make All Statics <make-all-statics>`
      + :ref:`Method Could Be Static <method-could-be-static>`
      + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
      + :ref:`Modified Typed Parameter <modified-typed-parameter>`
      + :ref:`New Initializers <new-initializers>`
      + :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
      + :ref:`No Hardcoded Hash <no-hardcoded-hash>`
      + :ref:`No Literal For Reference <no-literal-for-reference>`
      + :ref:`No Need For get_class() <no-need-for-get\_class()>`
      + :ref:`No Net For Xml Load <no-net-for-xml-load>`
      + :ref:`No Reference For Static Property <no-reference-for-static-property>`
      + :ref:`No Return Used <no-return-used>`
      + :ref:`No Static Variable In A Method <no-static-variable-in-a-method>`
      + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
      + :ref:`Normal Methods <normal-methods>`
      + :ref:`Only Static Methods Class <only-static-methods-class>`
      + :ref:`Only Variable For Reference <only-variable-for-reference>`
      + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
      + :ref:`Only Variable Returned By Reference <only-variable-returned-by-reference>`
      + :ref:`Order Of Declaration <order-of-declaration>`
      + :ref:`Override Attribute <override-attribute>`
      + :ref:`Overwritten Class Constants <overwritten-class-constants>`
      + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
      + :ref:`Php 8.0 Variable Syntax Tweaks <php-8.0-variable-syntax-tweaks>`
      + :ref:`Property Names <property-names>`
      + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
      + :ref:`Real Variables <real-variables>`
      + :ref:`Redeclared Static Variable <redeclared-static-variable>`
      + :ref:`Reserved Match Keyword <reserved-match-keyword>`
      + :ref:`Scope Resolution Operator <scope-resolution-operator>`
      + :ref:`Set Array Class Definition <set-array-class-definition>`
      + :ref:`Set Class Remote Definition With Type <set-class-remote-definition-with-type>`
      + :ref:`Should Have Destructor <should-have-destructor>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Solve Trait Constants <solve-trait-constants>`
      + :ref:`Static Call May Be Truly Static <static-call-may-be-truly-static>`
      + :ref:`Static Call With Self <static-call-with-self>`
      + :ref:`Static Global Variables Confusion <static-global-variables-confusion>`
      + :ref:`Static Inclusions <static-inclusions>`
      + :ref:`Static Loop <static-loop>`
      + :ref:`Static Methods <static-methods>`
      + :ref:`Static Methods Called From Object <static-methods-called-from-object>`
      + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
      + :ref:`Static Methods Cannot Call Non-Static Methods <static-methods-cannot-call-non-static-methods>`
      + :ref:`Static Properties <static-properties>`
      + :ref:`Static Variable Can Default To Arbitrary Expression <static-variable-can-default-to-arbitrary-expression>`
      + :ref:`Static Variable In Namespace <static-variable-in-namespace>`
      + :ref:`Static Variable Initialisation <static-variable-initialisation>`
      + :ref:`Static Variables <static-variables>`
      + :ref:`Too Many Chained Calls <too-many-chained-calls>`
      + :ref:`Too Many Dereferencing <too-many-dereferencing>`
      + :ref:`Too Many Local Variables <too-many-local-variables>`
      + :ref:`Traits Usage <traits-usage>`
      + :ref:`Typed Class Constants Usage <typed-class-constants-usage>`
      + :ref:`Unbinding Closures <unbinding-closures>`
      + :ref:`Undefined Variable <undefined-variable>`
      + :ref:`Undefined static:: Or self:: <undefined-static-or-self>`
      + :ref:`Unsupported Operand Types <unsupported-operand-types>`
      + :ref:`Unused Class Constant <unused-class-constant>`
      + :ref:`Unused Private Methods <unused-private-methods>`
      + :ref:`Unused Private Properties <unused-private-properties>`
      + :ref:`Use ::Class Operator <use-class-operator>`
      + :ref:`Use Arrow Functions <use-arrow-functions>`
      + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
      + :ref:`Use PHP7 Encapsed Strings <use-php7-encapsed-strings>`
      + :ref:`Use This <use-this>`
      + :ref:`Use class_alias() <use-class\_alias()>`
      + :ref:`Used Classes <used-classes>`
      + :ref:`Used Once Variables <used-once-variables>`
      + :ref:`Used Private Methods <used-private-methods>`
      + :ref:`Used Static Properties <used-static-properties>`
      + :ref:`Useless Abstract Class <useless-abstract-class>`
      + :ref:`Useless Null Coalesce <useless-null-coalesce>`
      + :ref:`Useless Unset <useless-unset>`
      + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`
      + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`
      + :ref:`Wrong Type Returned <wrong-type-returned>`
      + :ref:`__halt_compiler <\_\_halt\_compiler>`
      + :ref:`ext/ffi <ext-ffi>`
      + :ref:`ext/reflection <ext-reflection>`
      + :ref:`ext/xdebug <ext-xdebug>`
      + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`
      + :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`
      + :ref:`Make Static Closures And Arrow Functions <make-static-closures-and-arrow-functions>`
      + :ref:`Remove Static From Closures And Arrow Functions <remove-static-from-closures-and-arrow-functions>`
      + :ref:`Rename Class <rename-class>`
      + :ref:`Rename Enums <rename-enums>`
      + :ref:`Rename Interface <rename-interface>`
      + :ref:`Rename Method <rename-method>`
      + :ref:`Rename Methodcall <rename-methodcall>`
      + :ref:`Rename Property <rename-property>`
      + :ref:`Rename Trait <rename-trait>`
      + :ref:`Coding conventions <coding-conventions>`

    + `stdClass`

      + :ref:`Aliases <aliases>`
      + :ref:`Avoid Using stdClass <avoid-using-stdclass>`
      + :ref:`Cant Inherit Abstract Method <cant-inherit-abstract-method>`
      + :ref:`Extends stdClass <extends-stdclass>`
      + :ref:`New On Functioncall Or Identifier <new-on-functioncall-or-identifier>`
      + :ref:`No Object As Index <no-object-as-index>`
      + :ref:`Objects Don't Need References <objects-don't-need-references>`
      + :ref:`Return Type Usage <return-type-usage>`
      + :ref:`Scope Resolution Operator <scope-resolution-operator>`
      + :ref:`class_alias() Supports Internal Classes <class\_alias()-supports-internal-classes>`
      + :ref:`ext/memcache <ext-memcache>`
      + :ref:`get_class() Without Argument <get\_class()-without-argument>`

    + `stdclass`

      + :ref:`Extends stdClass <extends-stdclass>`

    + `str_contains()`

      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Use str_contains() <use-str\_contains()>`

    + `str_ends_with()`

      + :ref:`Use str_ends_with() <use-str\_ends\_with()>`

    + `str_ireplace()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`

    + `str_pad()`

      + :ref:`Could Use str_repeat() <could-use-str\_repeat()>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `str_repeat()`

      + :ref:`Could Use str_repeat() <could-use-str\_repeat()>`

    + `str_replace()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`

    + `str_split()`

      + :ref:`No Empty String With explode() <no-empty-string-with-explode()>`
      + :ref:`Substr() In Loops <substr()-in-loops>`

    + `str_starts_with()`

      + :ref:`Use str_starts_with() <use-str\_starts\_with()>`

    + `stream_isatty()`

      + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`

    + `stream_select()`

      + :ref:`ext/inotify <ext-inotify>`

    + `stream_set_blocking()`

      + :ref:`ext/inotify <ext-inotify>`

    + `stream_set_chunk_size()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `stream_socket_client()`

      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `stream_socket_enable_crypto()`

      + :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`

    + `stream_socket_server()`

      + :ref:`@ Operator <@-operator>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `strftime()`

      + :ref:`Date Formats <date-formats>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `strip_tags()`

      + :ref:`strip_tags() Skips Closed Tag <strip\_tags()-skips-closed-tag>`

    + `stripos()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Simplify Regex <simplify-regex>`
      + :ref:`Strpos() Less Than One <strpos()-less-than-one>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Use str_contains() <use-str\_contains()>`
      + :ref:`strpos() Too Much <strpos()-too-much>`

    + `stristr()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `strlen()`

      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`No Count With 0 <no-count-with-0>`

    + `strpos()`

      + :ref:`Could Use strcontains() <could-use-strcontains()>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Simplify Regex <simplify-regex>`
      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Strpos() Less Than One <strpos()-less-than-one>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
      + :ref:`Use str_contains() <use-str\_contains()>`
      + :ref:`strpos() Too Much <strpos()-too-much>`
      + :ref:`strpos() With Integers <strpos()-with-integers>`

    + `strptime()`

      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

    + `strrchr()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `strripos()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `strrpos()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `strstr()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Slow Functions <slow-functions>`

    + `strtok()`

      + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`

    + `strtolower()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
      + :ref:`Overload Existing Names <overload-existing-names>`

    + `strtotime()`

      + :ref:`Incoming Date Formats <incoming-date-formats>`
      + :ref:`Next Month Trap <next-month-trap>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`
      + :ref:`time() Vs strtotime() <time()-vs-strtotime()>`

    + `strtoupper()`

      + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`Overload Existing Names <overload-existing-names>`
      + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

    + `strtr()`

      + :ref:`Strtr Arguments <strtr-arguments>`

    + `strval()`

      + :ref:`Concat Empty String <concat-empty-string>`

    + `substr()`

      + :ref:`Avoid Substr() One <avoid-substr()-one>`
      + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`
      + :ref:`No List With String <no-list-with-string>`
      + :ref:`No Substr Minus One <no-substr-minus-one>`
      + :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`
      + :ref:`Substr To Trim <substr-to-trim>`
      + :ref:`Substr() In Loops <substr()-in-loops>`
      + :ref:`Substring First <substring-first>`
      + :ref:`Use Basename Suffix <use-basename-suffix>`
      + :ref:`Use array_slice() <use-array\_slice()>`
      + :ref:`Wrong Parameter Type <wrong-parameter-type>`
      + :ref:`strpos() Too Much <strpos()-too-much>`

    + `substr_count()`

      + :ref:`Mono Or Multibytes Favorite <mono-or-multibytes-favorite>`

    + `substr_replace()`

      + :ref:`Make One Call With Array <make-one-call-with-array>`

    + `switch()`

      + :ref:`Bracketless Blocks <bracketless-blocks>`
      + :ref:`Break Outside Loop <break-outside-loop>`
      + :ref:`Collect Compared Literals <collect-compared-literals>`
      + :ref:`Could Use Match <could-use-match>`
      + :ref:`Identical Case In Switch <identical-case-in-switch>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Missing Cases In Switch <missing-cases-in-switch>`
      + :ref:`Multiline Expressions <multiline-expressions>`
      + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`Switch To Switch <switch-to-switch>`
      + :ref:`Switch With Too Many Default <switch-with-too-many-default>`
      + :ref:`Switch Without Default <switch-without-default>`
      + :ref:`Too Many Stringed Elseif <too-many-stringed-elseif>`
      + :ref:`Use The Case Value <use-the-case-value>`
      + :ref:`Uses PHP 8 Match() <uses-php-8-match()>`
      + :ref:`Switch To Match <switch-to-match>`

    + `sys_get_temp_dir()`

      + :ref:`No Hardcoded Path <no-hardcoded-path>`
      + :ref:`Use System Tmp <use-system-tmp>`

    + `system()`

      + :ref:`Shell commands <shell-commands>`


+ `T`
    + `TRUE`

      + :ref:`Assertions <assertions>`
      + :ref:`Constant Conditions <constant-conditions>`
      + :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
      + :ref:`True False Inconsistant Case <true-false-inconsistant-case>`
      + :ref:`Use PHP Object API <use-php-object-api>`
      + :ref:`ext/event <ext-event>`
      + :ref:`ext/xmlwriter <ext-xmlwriter>`
      + :ref:`ext/zip <ext-zip>`

    + `T_COMMENT`

      + :ref:`ext/tokenizer <ext-tokenizer>`

    + `T_DOC_COMMENT`

      + :ref:`ext/tokenizer <ext-tokenizer>`

    + `T_STRING`

      + :ref:`Constants Usage <constants-usage>`

    + `Throwable`

      + :ref:`Can't Implement Throwable <can't-implement-throwable>`
      + :ref:`Empty Try Catch <empty-try-catch>`
      + :ref:`No Object As Index <no-object-as-index>`
      + :ref:`PHP 7.0 New Interfaces <php-7.0-new-interfaces>`
      + :ref:`Set Chaining Exception <set-chaining-exception>`
      + :ref:`Try With Finally <try-with-finally>`
      + :ref:`Useless Catch <useless-catch>`
      + :ref:`ext/uopz <ext-uopz>`
      + :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`

    + `Tidy`

      + :ref:`ext/tidy <ext-tidy>`

    + `Traversable`

      + :ref:`Can't Implement Traversable <can't-implement-traversable>`

    + `True`

      + :ref:`True False Inconsistant Case <true-false-inconsistant-case>`

    + `TypeError`

      + :ref:`Random Without Try <random-without-try>`
      + :ref:`Unsupported Types With Operators <unsupported-types-with-operators>`
      + :ref:`Use get_debug_type() <use-get\_debug\_type()>`

    + `throwable`

      + :ref:`Can't Implement Throwable <can't-implement-throwable>`

    + `tidy`

      + :ref:`Use PHP Object API <use-php-object-api>`

    + `time()`

      + :ref:`Conditioned Constants <conditioned-constants>`
      + :ref:`Date Formats <date-formats>`
      + :ref:`Reuse Existing Variable <reuse-existing-variable>`
      + :ref:`Session Variables <session-variables>`
      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`
      + :ref:`Timestamp Difference <timestamp-difference>`
      + :ref:`Use Cookies <use-cookies>`
      + :ref:`Use random_int() <use-random\_int()>`
      + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`
      + :ref:`ext/zip <ext-zip>`
      + :ref:`time() Vs strtotime() <time()-vs-strtotime()>`

    + `token_get_all()`

      + :ref:`@ Operator <@-operator>`

    + `track_errors`

      + :ref:`PHP 8.0 Removed Directives <php-8.0-removed-directives>`

    + `trait_exists()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_create()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_create_from_rules()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_create_inverse()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_get_error_code()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_get_error_message()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_list_ids()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `transliterator_transliterate()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `traversable`

      + :ref:`This Could Be Iterable <this-could-be-iterable>`
      + :ref:`Typehint Could Be Iterable <typehint-could-be-iterable>`

    + `trigger_error()`

      + :ref:`Error Messages <error-messages>`
      + :ref:`Trigger Errors <trigger-errors>`
      + :ref:`Use Constant As Arguments <use-constant-as-arguments>`

    + `trim()`

      + :ref:`Substr To Trim <substr-to-trim>`
      + :ref:`Substring First <substring-first>`

    + `true`

      + :ref:`Already Parents Interface <already-parents-interface>`
      + :ref:`Always Positive Comparison <always-positive-comparison>`
      + :ref:`Ambiguous Array Index <ambiguous-array-index>`
      + :ref:`Argument Counts Per Calls <argument-counts-per-calls>`
      + :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
      + :ref:`Assign And Compare <assign-and-compare>`
      + :ref:`Avoid Compare Typed Boolean <avoid-compare-typed-boolean>`
      + :ref:`Avoid array_push() <avoid-array\_push()>`
      + :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`
      + :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
      + :ref:`Case Insensitive Constants <case-insensitive-constants>`
      + :ref:`Cast To Boolean <cast-to-boolean>`
      + :ref:`Compare Hash <compare-hash>`
      + :ref:`Confusing Names <confusing-names>`
      + :ref:`Constant Case Preference <constant-case-preference>`
      + :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
      + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
      + :ref:`Could Be A Constant <could-be-a-constant>`
      + :ref:`Could Be Boolean <could-be-boolean>`
      + :ref:`Could Be Constant <could-be-constant>`
      + :ref:`Displays Text <displays-text>`
      + :ref:`Don't Echo Error <don't-echo-error>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Drop Else After Return <drop-else-after-return>`
      + :ref:`Exit() Usage <exit()-usage>`
      + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
      + :ref:`For Using Functioncall <for-using-functioncall>`
      + :ref:`Foreach On Object <foreach-on-object>`
      + :ref:`Implied If <implied-if>`
      + :ref:`Indices Are Int Or String <indices-are-int-or-string>`
      + :ref:`Is_A() With String <is\_a()-with-string>`
      + :ref:`Logical Mistakes <logical-mistakes>`
      + :ref:`Logical To in_array <logical-to-in\_array>`
      + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
      + :ref:`Methodcall On New <methodcall-on-new>`
      + :ref:`Minus One On Error <minus-one-on-error>`
      + :ref:`Multiple Index Definition <multiple-index-definition>`
      + :ref:`Multiples Identical Case <multiples-identical-case>`
      + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`
      + :ref:`No Boolean As Default <no-boolean-as-default>`
      + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
      + :ref:`PHP 7.1 Microseconds <php-7.1-microseconds>`
      + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`
      + :ref:`PHP 8.2 New Types <php-8.2-new-types>`
      + :ref:`PHP 80 Named Parameter Variadic <php-80-named-parameter-variadic>`
      + :ref:`PHP Handlers Usage <php-handlers-usage>`
      + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`
      + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
      + :ref:`Possible Infinite Loop <possible-infinite-loop>`
      + :ref:`Queries In Loops <queries-in-loops>`
      + :ref:`Redefined Private Property <redefined-private-property>`
      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
      + :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
      + :ref:`Return True False <return-true-false>`
      + :ref:`Safe Curl Options <safe-curl-options>`
      + :ref:`Semantic Typing <semantic-typing>`
      + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
      + :ref:`Short Or Complete Comparison <short-or-complete-comparison>`
      + :ref:`Should Use SetCookie() <should-use-setcookie()>`
      + :ref:`StandaloneType True False Null <standalonetype-true-false-null>`
      + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
      + :ref:`Strict In_Array() Preference <strict-in\_array()-preference>`
      + :ref:`String Int Comparison <string-int-comparison>`
      + :ref:`Too Many Chained Calls <too-many-chained-calls>`
      + :ref:`True False Inconsistant Case <true-false-inconsistant-case>`
      + :ref:`Type Must Be Returned <type-must-be-returned>`
      + :ref:`Typo 3 usage <typo-3-usage>`
      + :ref:`Use Browscap <use-browscap>`
      + :ref:`Use Debug <use-debug>`
      + :ref:`Use Named Boolean In Argument Definition <use-named-boolean-in-argument-definition>`
      + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`
      + :ref:`Useless Null Coalesce <useless-null-coalesce>`
      + :ref:`Wrong Parameter Type <wrong-parameter-type>`
      + :ref:`Wrong Precedence In Expression <wrong-precedence-in-expression>`
      + :ref:`ext/exif <ext-exif>`
      + :ref:`ext/mongo <ext-mongo>`
      + :ref:`ext/msgpack <ext-msgpack>`
      + :ref:`ext/pecl_http <ext-pecl\_http>`
      + :ref:`ext/pkcs11 <ext-pkcs11>`
      + :ref:`ext/sqlsrv <ext-sqlsrv>`
      + :ref:`ext/teds <ext-teds>`
      + :ref:`ext/uopz <ext-uopz>`
      + :ref:`ext/xmlwriter <ext-xmlwriter>`
      + :ref:`ext/xsl <ext-xsl>`
      + :ref:`var_dump()... Usage <var\_dump()...-usage>`
      + :ref:`version_compare() Operator <version\_compare()-operator>`


+ `U`
    + `Usort()`

      + :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`

    + `uasort()`

      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`

    + `uksort()`

      + :ref:`Slow Functions <slow-functions>`
      + :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`

    + `uniqid()`

      + :ref:`Use random_int() <use-random\_int()>`
      + :ref:`ext/eio <ext-eio>`

    + `unpack()`

      + :ref:`Invalid Pack Format <invalid-pack-format>`
      + :ref:`Pack Format Inventory <pack-format-inventory>`

    + `unserialize()`

      + :ref:`Unserialize Second Arg <unserialize-second-arg>`

    + `urlencode()`

      + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`

    + `usleep()`

      + :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`

    + `usort()`

      + :ref:`Slow Functions <slow-functions>`

    + `utf8_decode()`

      + :ref:`Utf8 Encode And Decode Are Deprecated <utf8-encode-and-decode-are-deprecated>`

    + `utf8_encode()`

      + :ref:`Utf8 Encode And Decode Are Deprecated <utf8-encode-and-decode-are-deprecated>`


+ `V`
    + `ValueError`

      + :ref:`No Empty String With explode() <no-empty-string-with-explode()>`

    + `var_dump()`

      + :ref:`Use Debug <use-debug>`
      + :ref:`var_dump()... Usage <var\_dump()...-usage>`

    + `var_export()`

      + :ref:`var_dump()... Usage <var\_dump()...-usage>`

    + `version_compare()`

      + :ref:`version_compare() Operator <version\_compare()-operator>`

    + `vfprintf()`

      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

    + `vprintf()`

      + :ref:`Printf Format Inventory <printf-format-inventory>`
      + :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

    + `vsprintf()`

      + :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
      + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`


+ `W`
    + `WeakReference`

      + :ref:`Php 7.4 New Classes <php-7.4-new-classes>`

    + `while()`

      + :ref:`Bracketless Blocks <bracketless-blocks>`
      + :ref:`Break Outside Loop <break-outside-loop>`
      + :ref:`Minus One On Error <minus-one-on-error>`
      + :ref:`Add Brackets To Single Instructions <add-brackets-to-single-instructions>`
      + :ref:`Remove Brackets Around Single Instruction <remove-brackets-around-single-instruction>`

    + `wordwrap()`

      + :ref:`ext/mail <ext-mail>`


+ `X`
    + `XMLReader`

      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/xmlreader <ext-xmlreader>`

    + `XMLWriter`

      + :ref:`ext/libxml <ext-libxml>`
      + :ref:`ext/xmlwriter <ext-xmlwriter>`

    + `XSLTProcessor`

      + :ref:`ext/xsl <ext-xsl>`

    + `xmlWriter`

      + :ref:`ext/xmlwriter <ext-xmlwriter>`

    + `xml_parser_create()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
      + :ref:`ext/xml <ext-xml>`

    + `xml_parser_create_ns()`

      + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`

    + `xmlreader`

      + :ref:`ext/xmlreader <ext-xmlreader>`

    + `xmlwriter`

      + :ref:`ext/xmlwriter <ext-xmlwriter>`

    + `xmlwriter_open_memory()`

      + :ref:`ext/xmlwriter <ext-xmlwriter>`


+ `Z`
    + `zend_logo_guid()`

      + :ref:`Functions Removed In PHP 5.5 <functions-removed-in-php-5.5>`

    + `zend_monitor_pass_error()`

      + :ref:`ext/zend_monitor <ext-zend\_monitor>`

    + `zlib_decode()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`

    + `zlib_encode()`

      + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`


+ `_`
    + `_()`

      + :ref:`ext/gettext <ext-gettext>`

    + `__CLASS__`

      + :ref:`::class <class>`
      + :ref:`Detect Current Class <detect-current-class>`
      + :ref:`Interpolation <interpolation>`
      + :ref:`Non Ascii Variables <non-ascii-variables>`

    + `__DIR__`

      + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
      + :ref:`No Hardcoded Path <no-hardcoded-path>`
      + :ref:`PHP Sapi <php-sapi>`
      + :ref:`PHP7 Dirname <php7-dirname>`
      + :ref:`Static Inclusions <static-inclusions>`
      + :ref:`Use PHP7 Encapsed Strings <use-php7-encapsed-strings>`
      + :ref:`__DIR__ Then Slash <\_\_dir\_\_-then-slash>`
      + :ref:`ext/wasm <ext-wasm>`

    + `__FILE__`

      + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
      + :ref:`Magic Constant Usage <magic-constant-usage>`
      + :ref:`No Hardcoded Path <no-hardcoded-path>`
      + :ref:`__halt_compiler <\_\_halt\_compiler>`
      + :ref:`ext/fann <ext-fann>`
      + :ref:`ext/grpc <ext-grpc>`
      + :ref:`ext/inotify <ext-inotify>`
      + :ref:`ext/sem <ext-sem>`

    + `__FUNCTION__`

      + :ref:`Can't Call Generator <can't-call-generator>`
      + :ref:`PHP Overridden Function <php-overridden-function>`
      + :ref:`Use Const And Functions <use-const-and-functions>`

    + `__LINE__`

      + :ref:`Magic Constant Usage <magic-constant-usage>`

    + `__METHOD__`

      + :ref:`Already Parents Interface <already-parents-interface>`
      + :ref:`Anonymous Classes <anonymous-classes>`
      + :ref:`Class Usage <class-usage>`
      + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
      + :ref:`Parent Is Not Static <parent-is-not-static>`
      + :ref:`Should Have Destructor <should-have-destructor>`

    + `__NAMESPACE__`

      + :ref:`Could Use Namespace Magic Constant <could-use-namespace-magic-constant>`

    + `__call`

      + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
      + :ref:`Check On __Call Usage <check-on-\_\_call-usage>`
      + :ref:`Create Magic Method <create-magic-method>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`Undefined Methods <undefined-methods>`
      + :ref:`Useless Type <useless-type>`

    + `__callStatic`

      + :ref:`Create Magic Method <create-magic-method>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`

    + `__clone`

      + :ref:`Could Be Readonly Property <could-be-readonly-property>`
      + :ref:`Direct Call To __clone() <direct-call-to-\_\_clone()>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Magic Visibility <magic-visibility>`
      + :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
      + :ref:`Readonly Property Changed By Cloning <readonly-property-changed-by-cloning>`
      + :ref:`Set Clone Link <set-clone-link>`
      + :ref:`Should Deep Clone <should-deep-clone>`

    + `__construct`

      + :ref:`Anonymous Classes <anonymous-classes>`
      + :ref:`Array Access On Literal Array <array-access-on-literal-array>`
      + :ref:`Assign Default To Properties <assign-default-to-properties>`
      + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
      + :ref:`Avoid Optional Properties <avoid-optional-properties>`
      + :ref:`Avoid option arrays in constructors <avoid-option-arrays-in-constructors>`
      + :ref:`Can't Instantiate Class <can't-instantiate-class>`
      + :ref:`Collect Method Counts <collect-method-counts>`
      + :ref:`Constructors <constructors>`
      + :ref:`Could Be Readonly Property <could-be-readonly-property>`
      + :ref:`Could Be Static Closure <could-be-static-closure>`
      + :ref:`Could Set Property Default <could-set-property-default>`
      + :ref:`Could Use Promoted Properties <could-use-promoted-properties>`
      + :ref:`Courier Anti-Pattern <courier-anti-pattern>`
      + :ref:`Create Default Values <create-default-values>`
      + :ref:`DI Cyclic Dependencies <di-cyclic-dependencies>`
      + :ref:`DateTimeImmutable Is Not Immutable <datetimeimmutable-is-not-immutable>`
      + :ref:`Dependency Injection <dependency-injection>`
      + :ref:`Different Constructors <different-constructors>`
      + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
      + :ref:`Friend Attribute <friend-attribute>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Illegal Name For Method <illegal-name-for-method>`
      + :ref:`Incompatible Types With Incoming Values <incompatible-types-with-incoming-values>`
      + :ref:`Injectable Version <injectable-version>`
      + :ref:`Insufficient Property Type <insufficient-property-type>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Make Global A Property <make-global-a-property>`
      + :ref:`Missing Type In Definition <missing-type-in-definition>`
      + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`
      + :ref:`No Constructor In Interface <no-constructor-in-interface>`
      + :ref:`No Magic Method For Enum <no-magic-method-for-enum>`
      + :ref:`Non Ascii Variables <non-ascii-variables>`
      + :ref:`Non Nullable Getters <non-nullable-getters>`
      + :ref:`Old Style Constructor <old-style-constructor>`
      + :ref:`Parent First <parent-first>`
      + :ref:`Promoted Properties <promoted-properties>`
      + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
      + :ref:`Property Could Be Local <property-could-be-local>`
      + :ref:`Readonly Property Changed By Cloning <readonly-property-changed-by-cloning>`
      + :ref:`Redefined Default <redefined-default>`
      + :ref:`Scalar Or Object Property <scalar-or-object-property>`
      + :ref:`Set Aside Code <set-aside-code>`
      + :ref:`Set Chaining Exception <set-chaining-exception>`
      + :ref:`Set Class Method Remote Definition <set-class-method-remote-definition>`
      + :ref:`Should Deep Clone <should-deep-clone>`
      + :ref:`Should Have Destructor <should-have-destructor>`
      + :ref:`Should Use Local Class <should-use-local-class>`
      + :ref:`Signature Trailing Comma <signature-trailing-comma>`
      + :ref:`Static Methods Cannot Call Non-Static Methods <static-methods-cannot-call-non-static-methods>`
      + :ref:`Strange Names In Classes <strange-names-in-classes>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`Too Many Injections <too-many-injections>`
      + :ref:`Typed Property Usage <typed-property-usage>`
      + :ref:`Typehints/CouldBeResource <typehints-couldberesource>`
      + :ref:`Unfinished Object <unfinished-object>`
      + :ref:`Uninitialized Property <uninitialized-property>`
      + :ref:`Unitialized Properties <unitialized-properties>`
      + :ref:`Untyped No Default Properties <untyped-no-default-properties>`
      + :ref:`Useless Assignation Of Promoted Property <useless-assignation-of-promoted-property>`
      + :ref:`Useless Constructor <useless-constructor>`
      + :ref:`Useless Return <useless-return>`
      + :ref:`Wrong Typed Property Default <wrong-typed-property-default>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`
      + :ref:`Set Types <set-types>`

    + `__debugInfo`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`__debugInfo() Usage <\_\_debuginfo()-usage>`

    + `__destruct`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Missing Type In Definition <missing-type-in-definition>`
      + :ref:`Should Have Destructor <should-have-destructor>`
      + :ref:`Throw In Destruct <throw-in-destruct>`
      + :ref:`ext/weakref <ext-weakref>`

    + `__get`

      + :ref:`Checks Property Existence <checks-property-existence>`
      + :ref:`Could Not Type <could-not-type>`
      + :ref:`Create Magic Property <create-magic-property>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Is A Magic Property <is-a-magic-property>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Magic Properties <magic-properties>`
      + :ref:`Magic Visibility <magic-visibility>`
      + :ref:`Make Magic Concrete <make-magic-concrete>`
      + :ref:`Memoize MagicCall <memoize-magiccall>`
      + :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`Useless Type <useless-type>`
      + :ref:`Set Types <set-types>`

    + `__invoke`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`

    + `__isset`

      + :ref:`Checks Property Existence <checks-property-existence>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Magic Visibility <magic-visibility>`
      + :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
      + :ref:`Must Return Methods <must-return-methods>`

    + `__set`

      + :ref:`Checks Property Existence <checks-property-existence>`
      + :ref:`Could Not Type <could-not-type>`
      + :ref:`Create Magic Property <create-magic-property>`
      + :ref:`Extends stdClass <extends-stdclass>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Magic Properties <magic-properties>`
      + :ref:`Magic Visibility <magic-visibility>`
      + :ref:`Make Magic Concrete <make-magic-concrete>`
      + :ref:`No Magic Method With Array <no-magic-method-with-array>`
      + :ref:`Useless Type <useless-type>`
      + :ref:`Set Types <set-types>`

    + `__set_state`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`

    + `__sleep`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`

    + `__toString`

      + :ref:`Could Be Stringable <could-be-stringable>`
      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Interpolation <interpolation>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Magic Methods <magic-methods>`
      + :ref:`Must Return Methods <must-return-methods>`
      + :ref:`No A Valid Cast <no-a-valid-cast>`
      + :ref:`No Direct Call To Magic Method <no-direct-call-to-magic-method>`
      + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`
      + :ref:`Reserved Methods <reserved-methods>`
      + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`

    + `__tostring`

      + :ref:`Could Be Stringable <could-be-stringable>`

    + `__unset`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
      + :ref:`Magic Methods <magic-methods>`

    + `__wakeup`

      + :ref:`Has Magic Method <has-magic-method>`
      + :ref:`Magic Methods <magic-methods>`






Directory by PHP Features
-------------------------

Exakat links each rules to PHP features.

  + $GLOBALS

    + :ref:`Global Definitions <global-definitions>`
    + :ref:`Useless Global <useless-global>`

  + $HTTP_RAW_POST_DATA

    + :ref:`$HTTP_RAW_POST_DATA Usage <$http\_raw\_post\_data-usage>`

  + $_COOKIE

    + :ref:`Useless Global <useless-global>`

  + $_ENV

    + :ref:`Useless Global <useless-global>`

  + $_FILES

    + :ref:`$FILES full_path <$files-full\_path>`
    + :ref:`Useless Global <useless-global>`

  + $_GET

    + :ref:`Useless Global <useless-global>`

  + $_POST

    + :ref:`Useless Global <useless-global>`

  + $_REQUEST

    + :ref:`Useless Global <useless-global>`

  + $_SERVER

    + :ref:`Useless Global <useless-global>`

  + $argc

    + :ref:`Use Cli <use-cli>`

  + $argv

    + :ref:`Use Cli <use-cli>`

  + $php_errormsg

    + :ref:`$php_errormsg Usage <$php\_errormsg-usage>`

  + $this

    + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
    + :ref:`$this Is Not An Array <$this-is-not-an-array>`
    + :ref:`Closure May Use $this <closure-may-use-$this>`
    + :ref:`Coalesce <coalesce>`
    + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
    + :ref:`Should Use Local Class <should-use-local-class>`
    + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
    + :ref:`Use This <use-this>`
    + :ref:`Using $this Outside A Class <using-$this-outside-a-class>`

  + Abstract Class

    + :ref:`Insufficient Type <insufficient-type>`

  + Abstract Keyword

    + :ref:`Abstract Class Constants <abstract-class-constants>`
    + :ref:`Abstract Class Usage <abstract-class-usage>`
    + :ref:`Abstract Methods Usage <abstract-methods-usage>`
    + :ref:`Abstract Or Implements <abstract-or-implements>`
    + :ref:`Abstract Static Methods <abstract-static-methods>`
    + :ref:`Anonymous Classes <anonymous-classes>`
    + :ref:`Cant Inherit Abstract Method <cant-inherit-abstract-method>`
    + :ref:`Could Be Abstract Class <could-be-abstract-class>`
    + :ref:`Could Be Abstract Method <could-be-abstract-method>`
    + :ref:`Dependant Abstract Classes <dependant-abstract-classes>`
    + :ref:`Instantiating Abstract Class <instantiating-abstract-class>`
    + :ref:`Interfaces Is Not Implemented <interfaces-is-not-implemented>`
    + :ref:`Internet Ports <internet-ports>`
    + :ref:`Missing Abstract Method <missing-abstract-method>`
    + :ref:`No Private Abstract Method In Trait <no-private-abstract-method-in-trait>`
    + :ref:`Order Of Declaration <order-of-declaration>`
    + :ref:`Useless Abstract Class <useless-abstract-class>`

  + Abstract Syntactic Tree (AST)

    + :ref:`ext/php-ast <ext-php-ast>`

  + Addition

    + :ref:`Adding Zero <adding-zero>`
    + :ref:`Concat And Addition <concat-and-addition>`

  + Alias

    + :ref:`Multiple Alias Definitions Per File <multiple-alias-definitions-per-file>`

  + Alternative Syntax

    + :ref:`Alternative Syntax Consistence <alternative-syntax-consistence>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`

  + Anonymous Class

    + :ref:`Anonymous Classes <anonymous-classes>`
    + :ref:`Internet Ports <internet-ports>`
    + :ref:`Order Of Declaration <order-of-declaration>`

  + Arbitrary Number Of Argument

    + :ref:`func_get_arg() Modified Behavior <func\_get\_arg()-modified-behavior>`

  + Arcane

    + :ref:`strpos() With Integers <strpos()-with-integers>`

  + Argon2

    + :ref:`Argon2 Usage <argon2-usage>`

  + Argument

    + :ref:`Links Between Parameter And Argument <links-between-parameter-and-argument>`
    + :ref:`Long Arguments <long-arguments>`
    + :ref:`Unset Arguments <unset-arguments>`
    + :ref:`Use Named Boolean In Argument Definition <use-named-boolean-in-argument-definition>`
    + :ref:`Useless Referenced Argument <useless-referenced-argument>`
    + :ref:`Wrong Argument Type <wrong-argument-type>`

  + ArithmeticError Error

    + :ref:`Check Division By Zero <check-division-by-zero>`
    + :ref:`Could Use Try <could-use-try>`

  + Array

    + :ref:`Ambiguous Array Index <ambiguous-array-index>`
    + :ref:`Array Index <array-index>`
    + :ref:`Array() / [  ] Consistence <array()---[--]-consistence>`
    + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
    + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
    + :ref:`Array_merge Needs Array Of Arrays <array\_merge-needs-array-of-arrays>`
    + :ref:`Avoid Large Array Assignation <avoid-large-array-assignation>`
    + :ref:`Avoid array_unique() <avoid-array\_unique()>`
    + :ref:`Could Be Array Type <could-be-array-type>`
    + :ref:`Could Cast To Array <could-cast-to-array>`
    + :ref:`Could Use array_sum() <could-use-array\_sum()>`
    + :ref:`Empty Slots In Arrays <empty-slots-in-arrays>`
    + :ref:`False To Array Conversion <false-to-array-conversion>`
    + :ref:`Float Conversion As Index <float-conversion-as-index>`
    + :ref:`Getting Last Element <getting-last-element>`
    + :ref:`Has Property Hook <has-property-hook>`
    + :ref:`Indices Are Int Or String <indices-are-int-or-string>`
    + :ref:`Mass Creation Of Arrays <mass-creation-of-arrays>`
    + :ref:`Mistaken Concatenation <mistaken-concatenation>`
    + :ref:`Mixed Keys In Array <mixed-keys-in-array>`
    + :ref:`Multidimensional Arrays <multidimensional-arrays>`
    + :ref:`Multiple Index Definition <multiple-index-definition>`
    + :ref:`No Spread For Hash <no-spread-for-hash>`
    + :ref:`Non-constant Index In Array <non-constant-index-in-array>`
    + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
    + :ref:`PHP Arrays Index <php-arrays-index>`
    + :ref:`Randomly Sorted Arrays <randomly-sorted-arrays>`
    + :ref:`Scalar Are Not Arrays <scalar-are-not-arrays>`
    + :ref:`Short Syntax For Arrays <short-syntax-for-arrays>`
    + :ref:`Slice Arrays First <slice-arrays-first>`
    + :ref:`Type Array Index <type-array-index>`
    + :ref:`Use array_slice() <use-array\_slice()>`
    + :ref:`Use is_countable <use-is\_countable>`
    + :ref:`Weak Type With Array <weak-type-with-array>`
    + :ref:`array_key_exists() Works On Arrays <array\_key\_exists()-works-on-arrays>`

  + Array Append

    + :ref:`Append And Assign Arrays <append-and-assign-arrays>`
    + :ref:`Count() To Array Append <count()-to-array-append>`
    + :ref:`List With Array Appends <list-with-array-appends>`
    + :ref:`No String With Append <no-string-with-append>`

  + Array Spread

    + :ref:`No Spread For Hash <no-spread-for-hash>`
    + :ref:`Unpacking Inside Arrays <unpacking-inside-arrays>`

  + Array With Curly Braces

    + :ref:`Curly-Bracketed Arrays Are Not Supported <curly-bracketed-arrays-are-not-supported>`

  + ArrayObject

    + :ref:`Avoid get_object_vars() <avoid-get\_object\_vars()>`
    + :ref:`Scalar Are Not Arrays <scalar-are-not-arrays>`

  + Arrow Functions

    + :ref:`Fn Argument Variable Confusion <fn-argument-variable-confusion>`
    + :ref:`Follow Closure Definition <follow-closure-definition>`
    + :ref:`Use Arrow Functions <use-arrow-functions>`
    + :ref:`Variable Parameter Ambiguity In Arrow Function <variable-parameter-ambiguity-in-arrow-function>`

  + Assertions

    + :ref:`Assert Function Is Reserved <assert-function-is-reserved>`
    + :ref:`Assertions <assertions>`

  + Assignations

    + :ref:`Assign And Compare <assign-and-compare>`
    + :ref:`Assigned In One Branch <assigned-in-one-branch>`
    + :ref:`Compared But Not Assigned Strings <compared-but-not-assigned-strings>`
    + :ref:`Double Assignation <double-assignation>`
    + :ref:`Iffectations <iffectations>`
    + :ref:`Throws An Assignement <throws-an-assignement>`

  + Assumption

    + :ref:`Assumptions <assumptions>`

  + Attributes

    + :ref:`Friend Attribute <friend-attribute>`
    + :ref:`Missing Attribute Attribute <missing-attribute-attribute>`
    + :ref:`Modify Immutable <modify-immutable>`
    + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
    + :ref:`MustUseResult <mustuseresult>`
    + :ref:`PHP Native Attributes <php-native-attributes>`
    + :ref:`Use PHP Attributes <use-php-attributes>`
    + :ref:`Using Deprecated Feature <using-deprecated-feature>`
    + :ref:`Wrong Attribute Configuration <wrong-attribute-configuration>`

  + Backed Enumeration

    + :ref:`Enum Case Values <enum-case-values>`

  + Backward Incompatible

    + :ref:`Use get_debug_type() <use-get\_debug\_type()>`

  + Binary Integer

    + :ref:`Binary Glossary <binary-glossary>`

  + Bitwise Operators

    + :ref:`Not Or Tilde <not-or-tilde>`

  + Blind Variable

    + :ref:`Blind Variables <blind-variables>`
    + :ref:`Don't Change The Blind Var <don't-change-the-blind-var>`
    + :ref:`Use The Blind Var <use-the-blind-var>`

  + Block

    + :ref:`Bracketless Blocks <bracketless-blocks>`
    + :ref:`Empty Blocks <empty-blocks>`
    + :ref:`Lone Blocks <lone-blocks>`
    + :ref:`Too Long A Block <too-long-a-block>`
    + :ref:`Useless Brackets <useless-brackets>`

  + Boolean

    + :ref:`No Boolean As Default <no-boolean-as-default>`
    + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
    + :ref:`Return True False <return-true-false>`
    + :ref:`Use Named Boolean In Argument Definition <use-named-boolean-in-argument-definition>`

  + Branch

    + :ref:`No Choice <no-choice>`

  + Break

    + :ref:`Break Outside Loop <break-outside-loop>`
    + :ref:`Break With 0 <break-with-0>`
    + :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`

  + Call

    + :ref:`Duplicate Calls <duplicate-calls>`

  + Callables

    + :ref:`Could Be Callable <could-be-callable>`
    + :ref:`Could Be Typed Callable <could-be-typed-callable>`
    + :ref:`Deprecated Callable <deprecated-callable>`

  + Callbacks

    + :ref:`Callback Function Needs Return <callback-function-needs-return>`
    + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
    + :ref:`Could Be Callable <could-be-callable>`
    + :ref:`Handle Arrays With Callback <handle-arrays-with-callback>`

  + Case

    + :ref:`Non-lowercase Keywords <non-lowercase-keywords>`
    + :ref:`Switch Without Default <switch-without-default>`

  + Case Sensitivity

    + :ref:`Wrong Class Name Case <wrong-class-name-case>`
    + :ref:`Wrong Function Name Case <wrong-function-name-case>`

  + Cast Operator

    + :ref:`Cast To Boolean <cast-to-boolean>`
    + :ref:`Cast Unset Usage <cast-unset-usage>`
    + :ref:`Cast Usage <cast-usage>`
    + :ref:`Casting Ternary <casting-ternary>`
    + :ref:`Could Cast To Array <could-cast-to-array>`
    + :ref:`Do Not Cast To Int <do-not-cast-to-int>`
    + :ref:`Favorite Casting Method <favorite-casting-method>`
    + :ref:`Invalid Cast <invalid-cast>`
    + :ref:`No A Valid Cast <no-a-valid-cast>`
    + :ref:`Not Not <not-not>`
    + :ref:`Should Typecast <should-typecast>`
    + :ref:`Silently Cast Integer <silently-cast-integer>`
    + :ref:`Test Then Cast <test-then-cast>`
    + :ref:`Useless Type Casting <useless-type-casting>`

  + Catch

    + :ref:`Caught Exceptions <caught-exceptions>`
    + :ref:`Caught Expressions <caught-expressions>`
    + :ref:`Collect Catch Calls <collect-catch-calls>`
    + :ref:`Could Drop Variable <could-drop-variable>`
    + :ref:`Multiple Catch With Try <multiple-catch-with-try>`
    + :ref:`Try Without Catch <try-without-catch>`
    + :ref:`Useless Catch <useless-catch>`

  + Centralization

    + :ref:`Could Use Trait <could-use-trait>`

  + Chaining Exceptions

    + :ref:`Set Chaining Exception <set-chaining-exception>`
    + :ref:`Should Chain Exception <should-chain-exception>`

  + Class

    + :ref:`@ Operator <@-operator>`
    + :ref:`Abstract Class Usage <abstract-class-usage>`
    + :ref:`Abstract Methods Usage <abstract-methods-usage>`
    + :ref:`Accessing Private <accessing-private>`
    + :ref:`Ambiguous Visibilities <ambiguous-visibilities>`
    + :ref:`Anonymous Classes <anonymous-classes>`
    + :ref:`Avoid get_class() <avoid-get\_class()>`
    + :ref:`Avoid get_object_vars() <avoid-get\_object\_vars()>`
    + :ref:`Can't Overload Constants <can't-overload-constants>`
    + :ref:`Cancel Common Method <cancel-common-method>`
    + :ref:`Class Function Confusion <class-function-confusion>`
    + :ref:`Class Usage <class-usage>`
    + :ref:`Class, Interface, Enum Or Trait With Identical Names <class,-interface,-enum-or-trait-with-identical-names>`
    + :ref:`Classes Names <classes-names>`
    + :ref:`Constant Definition <constant-definition>`
    + :ref:`Constructors <constructors>`
    + :ref:`Could Be Boolean <could-be-boolean>`
    + :ref:`Could Be CIT <could-be-cit>`
    + :ref:`Could Be Generator <could-be-generator>`
    + :ref:`Could Be Parent Method <could-be-parent-method>`
    + :ref:`Could Be Static Closure <could-be-static-closure>`
    + :ref:`Could Make A Function <could-make-a-function>`
    + :ref:`Could Type With Array <could-type-with-array>`
    + :ref:`Could Use self <could-use-self>`
    + :ref:`Custom Class Usage <custom-class-usage>`
    + :ref:`Cyclic References <cyclic-references>`
    + :ref:`Deep Definitions <deep-definitions>`
    + :ref:`Detect Current Class <detect-current-class>`
    + :ref:`Disconnected Classes <disconnected-classes>`
    + :ref:`Double Object Assignation <double-object-assignation>`
    + :ref:`Dynamic Property <dynamic-property>`
    + :ref:`Dynamically Called Classes <dynamically-called-classes>`
    + :ref:`Else Usage <else-usage>`
    + :ref:`Empty Classes <empty-classes>`
    + :ref:`Functioncall Is Global <functioncall-is-global>`
    + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
    + :ref:`Incompatible Property Between Class And Trait <incompatible-property-between-class-and-trait>`
    + :ref:`Internet Ports <internet-ports>`
    + :ref:`Is An Extension Class <is-an-extension-class>`
    + :ref:`Is Not Class Family <is-not-class-family>`
    + :ref:`Is Upper Family <is-upper-family>`
    + :ref:`Is_A() With String <is\_a()-with-string>`
    + :ref:`Make Global A Property <make-global-a-property>`
    + :ref:`Manipulates INF <manipulates-inf>`
    + :ref:`Method Has Fluent Interface <method-has-fluent-interface>`
    + :ref:`Multiple Class Declarations <multiple-class-declarations>`
    + :ref:`Multiple Classes In One File <multiple-classes-in-one-file>`
    + :ref:`Multiple Constant Definition <multiple-constant-definition>`
    + :ref:`Multiple Definition Of The Same Argument <multiple-definition-of-the-same-argument>`
    + :ref:`Multiple Identical Closure <multiple-identical-closure>`
    + :ref:`No Append On Source <no-append-on-source>`
    + :ref:`No Class As Type <no-class-as-type>`
    + :ref:`No Class In Global <no-class-in-global>`
    + :ref:`No Empty Regex <no-empty-regex>`
    + :ref:`No Hardcoded Hash <no-hardcoded-hash>`
    + :ref:`No Need For get_class() <no-need-for-get\_class()>`
    + :ref:`No Reference For Ternary <no-reference-for-ternary>`
    + :ref:`No isset() With empty() <no-isset()-with-empty()>`
    + :ref:`Not Same Name As File <not-same-name-as-file>`
    + :ref:`Null On New <null-on-new>`
    + :ref:`Only Static Methods Class <only-static-methods-class>`
    + :ref:`Order Of Declaration <order-of-declaration>`
    + :ref:`Overwritten Constant <overwritten-constant>`
    + :ref:`Overwritten Methods <overwritten-methods>`
    + :ref:`Overwritten Properties <overwritten-properties>`
    + :ref:`PHP 7.0 New Classes <php-7.0-new-classes>`
    + :ref:`PHP 7.0 Scalar Types <php-7.0-scalar-types>`
    + :ref:`PHP 7.1 Scalar Types <php-7.1-scalar-types>`
    + :ref:`PHP 7.2 Scalar Types <php-7.2-scalar-types>`
    + :ref:`PHP 7.3 Last Empty Argument <php-7.3-last-empty-argument>`
    + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
    + :ref:`Php 7.1 New Class <php-7.1-new-class>`
    + :ref:`Php 7.2 New Class <php-7.2-new-class>`
    + :ref:`Php 7.4 New Classes <php-7.4-new-classes>`
    + :ref:`Php 8.3 New Classes <php-8.3-new-classes>`
    + :ref:`Reserved Keywords In PHP 7 <reserved-keywords-in-php-7>`
    + :ref:`Set Array Class Definition <set-array-class-definition>`
    + :ref:`Swapped Arguments <swapped-arguments>`
    + :ref:`Too Many Children <too-many-children>`
    + :ref:`Too Many Finds <too-many-finds>`
    + :ref:`Undefined Classes <undefined-classes>`
    + :ref:`Undefined static \:\:class <undefined-static-class>`
    + :ref:`Unreachable Class Constant <unreachable-class-constant>`
    + :ref:`Unresolved Classes <unresolved-classes>`
    + :ref:`Unused Classes <unused-classes>`
    + :ref:`Usage Of class_alias() <usage-of-class\_alias()>`
    + :ref:`Use Array Functions <use-array-functions>`
    + :ref:`Use List With Foreach <use-list-with-foreach>`
    + :ref:`Used Classes <used-classes>`
    + :ref:`Used Once Variables <used-once-variables>`
    + :ref:`Used Static Properties <used-static-properties>`
    + :ref:`Useless Argument <useless-argument>`
    + :ref:`Wrong Class Name Case <wrong-class-name-case>`
    + :ref:`list() May Omit Variables <list()-may-omit-variables>`

  + Class Aliases

    + :ref:`Set class_alias() Definition <set-class\_alias()-definition>`
    + :ref:`Usage Of class_alias() <usage-of-class\_alias()>`
    + :ref:`Use class_alias() <use-class\_alias()>`

  + Class Autoloading

    + :ref:`Autoloading <autoloading>`
    + :ref:`Composer's autoload <composer's-autoload>`
    + :ref:`Old Style __autoload() <old-style-\_\_autoload()>`

  + Class Constants Visibility

    + :ref:`Const Visibility Usage <const-visibility-usage>`

  + Class Getter Method

    + :ref:`Getter And Setter <getter-and-setter>`

  + Class Invasion

    + :ref:`Class Invasion <class-invasion>`
    + :ref:`Class Overreach <class-overreach>`
    + :ref:`No Readonly Assignation In Global <no-readonly-assignation-in-global>`

  + Class Operator

    + :ref:`Could Use Class Operator <could-use-class-operator>`
    + :ref:`Use \:\:Class Operator <use-class-operator>`

  + Class Setter Method

    + :ref:`Getter And Setter <getter-and-setter>`

  + Client URL (CURL)

    + :ref:`Safe Curl Options <safe-curl-options>`

  + Clone

    + :ref:`Clone Usage <clone-usage>`
    + :ref:`Clone With Non-Object <clone-with-non-object>`
    + :ref:`Direct Call To __clone() <direct-call-to-\_\_clone()>`
    + :ref:`Set Clone Link <set-clone-link>`
    + :ref:`Should Deep Clone <should-deep-clone>`

  + Close Tag

    + :ref:`Close Tags Consistency <close-tags-consistency>`
    + :ref:`Closing Tags <closing-tags>`

  + Closure

    + :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
    + :ref:`Closure Could Be A Callback <closure-could-be-a-callback>`
    + :ref:`Closure May Use $this <closure-may-use-$this>`
    + :ref:`Closures Glossary <closures-glossary>`
    + :ref:`Coalesce <coalesce>`
    + :ref:`Follow Closure Definition <follow-closure-definition>`
    + :ref:`Pre-Calculate Use <pre-calculate-use>`
    + :ref:`Unbinding Closures <unbinding-closures>`

  + Closure Binding

    + :ref:`Unbinding Closures <unbinding-closures>`

  + Coalesce Operator

    + :ref:`\:\:class <class>`
    + :ref:`Coalesce And Concat <coalesce-and-concat>`
    + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
    + :ref:`Coalesce Equal <coalesce-equal>`
    + :ref:`Could Be Ternary <could-be-ternary>`
    + :ref:`Could Be Ternary <could-be-ternary>`
    + :ref:`Isset Multiple Arguments <isset-multiple-arguments>`
    + :ref:`Isset() On The Whole Array <isset()-on-the-whole-array>`
    + :ref:`Should Use Coalesce <should-use-coalesce>`
    + :ref:`Useless Null Coalesce <useless-null-coalesce>`

  + Code Reuse

    + :ref:`Used Once Trait <used-once-trait>`

  + Coding Conventions

    + :ref:`Unusual Case For PHP Functions <unusual-case-for-php-functions>`
    + :ref:`Yoda Comparison <yoda-comparison>`

  + Comma Secparated Values (CSV)

    + :ref:`Do In Base <do-in-base>`
    + :ref:`Fetch One Row Format <fetch-one-row-format>`
    + :ref:`Joining file() <joining-file()>`
    + :ref:`Make One Call With Array <make-one-call-with-array>`
    + :ref:`No mb_substr In Loop <no-mb\_substr-in-loop>`
    + :ref:`ext/CSV <ext-csv>`
    + :ref:`fputcsv() In Loops <fputcsv()-in-loops>`

  + Command Line Interface (CLI)

    + :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`
    + :ref:`Is CLI Script <is-cli-script>`
    + :ref:`Use Cli <use-cli>`

  + Comparison

    + :ref:`Always Positive Comparison <always-positive-comparison>`
    + :ref:`Assign And Compare <assign-and-compare>`
    + :ref:`Compared But Not Assigned Strings <compared-but-not-assigned-strings>`
    + :ref:`Compared Comparison <compared-comparison>`
    + :ref:`Comparison Is Always The Same <comparison-is-always-the-same>`
    + :ref:`Comparisons Orientation <comparisons-orientation>`
    + :ref:`Constant Comparison <constant-comparison>`
    + :ref:`Not Equal Is Not !== <not-equal-is-not-!==>`
    + :ref:`Strict Or Relaxed Comparison <strict-or-relaxed-comparison>`
    + :ref:`String Int Comparison <string-int-comparison>`
    + :ref:`Suspicious Comparison <suspicious-comparison>`
    + :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`

  + Composer

    + :ref:`Composer Usage <composer-usage>`
    + :ref:`Composer's autoload <composer's-autoload>`
    + :ref:`Use Composer Lock <use-composer-lock>`
    + :ref:`Wrong Number Of Arguments In Methods <wrong-number-of-arguments-in-methods>`

  + Compression

    + :ref:`ext/bzip2 <ext-bzip2>`

  + Concatenation

    + :ref:`Coalesce And Concat <coalesce-and-concat>`
    + :ref:`Concat And Addition <concat-and-addition>`
    + :ref:`Concatenation Interpolation Consistence <concatenation-interpolation-consistence>`
    + :ref:`Inconsistent Concatenation <inconsistent-concatenation>`
    + :ref:`Mistaken Concatenation <mistaken-concatenation>`
    + :ref:`Mixed Concat And Interpolation <mixed-concat-and-interpolation>`
    + :ref:`Ternary In Concat <ternary-in-concat>`

  + Concrete Class

    + :ref:`Instantiating Abstract Class <instantiating-abstract-class>`

  + Condition

    + :ref:`Constant Conditions <constant-conditions>`
    + :ref:`No Choice <no-choice>`

  + Conditional Structures

    + :ref:`Conditional Structures <conditional-structures>`

  + Conditioned Structures

    + :ref:`Conditioned Constants <conditioned-constants>`

  + Const

    + :ref:`Const Or Define Preference <const-or-define-preference>`
    + :ref:`Define Constants With Array <define-constants-with-array>`
    + :ref:`Use const <use-const>`

  + Constant Scalar Expression

    + :ref:`Constant Scalar Expression <constant-scalar-expression>`
    + :ref:`Constant Scalar Expressions <constant-scalar-expressions>`
    + :ref:`Define Constants With Array <define-constants-with-array>`
    + :ref:`Propagate Constants <propagate-constants>`
    + :ref:`Static Variable Initialisation <static-variable-initialisation>`

  + Constants

    + :ref:`Abstract Static Methods <abstract-static-methods>`
    + :ref:`Bad Constants Names <bad-constants-names>`
    + :ref:`Case Insensitive Constants <case-insensitive-constants>`
    + :ref:`Class Const With Array <class-const-with-array>`
    + :ref:`Clone Constant <clone-constant>`
    + :ref:`Const Or Define <const-or-define>`
    + :ref:`Const Or Define Preference <const-or-define-preference>`
    + :ref:`Constant : With Or Without Use <constant--with-or-without-use>`
    + :ref:`Constant Case Preference <constant-case-preference>`
    + :ref:`Constant Dynamic Creation <constant-dynamic-creation>`
    + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
    + :ref:`Constant Used Only Once <constant-used-only-once>`
    + :ref:`Constants Created Outside Its Namespace <constants-created-outside-its-namespace>`
    + :ref:`Constants In Traits <constants-in-traits>`
    + :ref:`Constants Names <constants-names>`
    + :ref:`Constants Usage <constants-usage>`
    + :ref:`Constants With Strange Names <constants-with-strange-names>`
    + :ref:`Could Be A Constant <could-be-a-constant>`
    + :ref:`Could Be Constant <could-be-constant>`
    + :ref:`Could Use Existing Constant <could-use-existing-constant>`
    + :ref:`Custom Constant Usage <custom-constant-usage>`
    + :ref:`Invalid Constant Name <invalid-constant-name>`
    + :ref:`Is An Extension Constant <is-an-extension-constant>`
    + :ref:`Is Global Constant <is-global-constant>`
    + :ref:`Is PHP Constant <is-php-constant>`
    + :ref:`New Constants In PHP 7.2 <new-constants-in-php-7.2>`
    + :ref:`New Constants In PHP 7.4 <new-constants-in-php-7.4>`
    + :ref:`No Self Referencing Constant <no-self-referencing-constant>`
    + :ref:`PHP 8.1 Removed Constants <php-8.1-removed-constants>`
    + :ref:`PHP Constant Usage <php-constant-usage>`
    + :ref:`Propagate Constants <propagate-constants>`
    + :ref:`Relay Constant <relay-constant>`
    + :ref:`Should Use Existing Constants <should-use-existing-constants>`
    + :ref:`Strange Name For Constants <strange-name-for-constants>`
    + :ref:`True False Inconsistant Case <true-false-inconsistant-case>`
    + :ref:`Unused Constants <unused-constants>`
    + :ref:`Variable Constants <variable-constants>`

  + Continue

    + :ref:`Continue Is For Loop <continue-is-for-loop>`

  + Contravariance

    + :ref:`Incompatible Signature Methods With Covariance <incompatible-signature-methods-with-covariance>`
    + :ref:`Method Signature Must Be Compatible <method-signature-must-be-compatible>`
    + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`
    + :ref:`Use Contravariance <use-contravariance>`

  + Cookie

    + :ref:`Cookies Variables <cookies-variables>`
    + :ref:`Set Cookie Safe Arguments <set-cookie-safe-arguments>`
    + :ref:`Should Use SetCookie() <should-use-setcookie()>`
    + :ref:`Use Cookies <use-cookies>`

  + Countable Interface

    + :ref:`Can't Count Non-Countable <can't-count-non-countable>`
    + :ref:`Use is_countable <use-is\_countable>`

  + Covariance

    + :ref:`Incompatible Signature Methods With Covariance <incompatible-signature-methods-with-covariance>`
    + :ref:`Method Signature Must Be Compatible <method-signature-must-be-compatible>`
    + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`
    + :ref:`Use Contravariance <use-contravariance>`
    + :ref:`Use Covariance <use-covariance>`

  + Cryptography

    + :ref:`Check Crypto Key Length <check-crypto-key-length>`
    + :ref:`Compare Hash <compare-hash>`
    + :ref:`Crypto Usage <crypto-usage>`
    + :ref:`Deprecated PHP Functions <deprecated-php-functions>`
    + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`
    + :ref:`Optimize Explode() <optimize-explode()>`
    + :ref:`ext/mcrypt <ext-mcrypt>`
    + :ref:`ext/scrypt <ext-scrypt>`

  + Ctype

    + :ref:`ext/ctype <ext-ctype>`

  + Curly Brackets

    + :ref:`Bracketless Blocks <bracketless-blocks>`
    + :ref:`Useless Brackets <useless-brackets>`

  + Cyclomatic Complexity

    + :ref:`Cyclomatic Complexity <cyclomatic-complexity>`

  + Dates

    + :ref:`Date Formats <date-formats>`
    + :ref:`Don't Add Seconds <don't-add-seconds>`
    + :ref:`Invalid Date Scanning Format <invalid-date-scanning-format>`
    + :ref:`Next Month Trap <next-month-trap>`
    + :ref:`Timestamp Difference <timestamp-difference>`
    + :ref:`Use DateTimeImmutable Class <use-datetimeimmutable-class>`
    + :ref:`date() versus DateTime Preference <date()-versus-datetime-preference>`

  + Dead Code

    + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`

  + Debugger

    + :ref:`Use Debug <use-debug>`
    + :ref:`Use get_debug_type() <use-get\_debug\_type()>`
    + :ref:`var_dump()... Usage <var\_dump()...-usage>`

  + Declaration

    + :ref:`Multiple Functions Declarations <multiple-functions-declarations>`
    + :ref:`Wrong Access Style to Property <wrong-access-style-to-property>`

  + Default

    + :ref:`Default Then Discard <default-then-discard>`
    + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
    + :ref:`Switch Without Default <switch-without-default>`
    + :ref:`Useless Default Argument <useless-default-argument>`

  + Default Value

    + :ref:`Add Default Value <add-default-value>`
    + :ref:`Assign Default To Properties <assign-default-to-properties>`
    + :ref:`Create Default Values <create-default-values>`
    + :ref:`No Boolean As Default <no-boolean-as-default>`
    + :ref:`Redefined Default <redefined-default>`
    + :ref:`Uninitialized Property <uninitialized-property>`
    + :ref:`Uses Default Values <uses-default-values>`
    + :ref:`Wrong Typed Property Default <wrong-typed-property-default>`

  + Definition

    + :ref:`Definitions Only <definitions-only>`

  + Dependency Injection

    + :ref:`Dependency Injection <dependency-injection>`

  + Deprecated

    + :ref:`Functions Removed In PHP 5.5 <functions-removed-in-php-5.5>`
    + :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
    + :ref:`Using Deprecated Method <using-deprecated-method>`

  + Deprecation

    + :ref:`Deprecated Attribute <deprecated-attribute>`

  + Dereferencing

    + :ref:`Dereferencing Levels <dereferencing-levels>`
    + :ref:`Dereferencing String And Arrays <dereferencing-string-and-arrays>`
    + :ref:`Too Many Dereferencing <too-many-dereferencing>`

  + Design Pattern

    + :ref:`An OOP Factory <an-oop-factory>`
    + :ref:`Courier Anti-Pattern <courier-anti-pattern>`
    + :ref:`Dependency Injection <dependency-injection>`

  + Destructor

    + :ref:`Should Have Destructor <should-have-destructor>`

  + Directives

    + :ref:`Directives Usage <directives-usage>`
    + :ref:`PHP 7.0 Removed Directives <php-7.0-removed-directives>`
    + :ref:`PHP 7.1 Removed Directives <php-7.1-removed-directives>`
    + :ref:`PHP 74 New Directives <php-74-new-directives>`
    + :ref:`PHP 8.0 Removed Constants <php-8.0-removed-constants>`
    + :ref:`PHP 8.0 Removed Directives <php-8.0-removed-directives>`
    + :ref:`PHP 8.1 Removed Directives <php-8.1-removed-directives>`
    + :ref:`Unknown Directive Name <unknown-directive-name>`

  + DirectoryIterator

    + :ref:`Avoid glob() Usage <avoid-glob()-usage>`

  + Disable Classes

    + :ref:`Can't Disable Class <can't-disable-class>`

  + Disable Functions

    + :ref:`Can't Disable Function <can't-disable-function>`

  + Disjunctive Normal Form (DNF)

    + :ref:`Use DNF <use-dnf>`

  + DivisionByZeroError

    + :ref:`Could Use Try <could-use-try>`

  + Do While

    + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`

  + Do...while

    + :ref:`Collect Block Size <collect-block-size>`

  + Don't Repeat Yourself (DRY)

    + :ref:`Could Use Trait <could-use-trait>`
    + :ref:`Identical Case In Switch <identical-case-in-switch>`
    + :ref:`Multiple Property Declaration <multiple-property-declaration>`

  + Double Quotes Strings

    + :ref:`Should Be Single Quote <should-be-single-quote>`

  + Duck Typing

    + :ref:`Forgotten Interface <forgotten-interface>`

  + Dynamic Call

    + :ref:`Dynamic Calls <dynamic-calls>`
    + :ref:`Dynamic Code <dynamic-code>`
    + :ref:`Dynamic Function Call <dynamic-function-call>`
    + :ref:`Dynamic Methodcall <dynamic-methodcall>`
    + :ref:`Dynamic New <dynamic-new>`
    + :ref:`Function With Dynamic Code <function-with-dynamic-code>`

  + Dynamic Class

    + :ref:`Dynamic Classes <dynamic-classes>`
    + :ref:`Dynamically Called Classes <dynamically-called-classes>`

  + Dynamic Constant

    + :ref:`Case Insensitive Constants <case-insensitive-constants>`
    + :ref:`Dynamic Class Constant <dynamic-class-constant>`
    + :ref:`PHP Constant Usage <php-constant-usage>`
    + :ref:`Variable Constants <variable-constants>`

  + Dynamic Loading

    + :ref:`Dl() Usage <dl()-usage>`

  + Dynamic Properties

    + :ref:`Extends stdClass <extends-stdclass>`

  + Dynamic Variable

    + :ref:`Complex Dynamic Names <complex-dynamic-names>`
    + :ref:`Create Compact Variables <create-compact-variables>`

  + Echo

    + :ref:`Echo Or Print <echo-or-print>`
    + :ref:`Echo With Concat <echo-with-concat>`

  + Echo Tag

    + :ref:`PHP Echo Tag Usage <php-echo-tag-usage>`
    + :ref:`Using Short Tags <using-short-tags>`

  + Ellipsis

    + :ref:`Ellipsis Merge <ellipsis-merge>`
    + :ref:`Ellipsis Usage <ellipsis-usage>`
    + :ref:`No Spread For Hash <no-spread-for-hash>`

  + Email

    + :ref:`Email Addresses <email-addresses>`
    + :ref:`ext/mailparse <ext-mailparse>`

  + Empty

    + :ref:`Empty With Expression <empty-with-expression>`
    + :ref:`Modernize Empty With Expression <modernize-empty-with-expression>`

  + Encoding

    + :ref:`Deprecated Mb_string Encodings <deprecated-mb\_string-encodings>`
    + :ref:`Encoding Usage <encoding-usage>`
    + :ref:`Iconv With Translit <iconv-with-translit>`
    + :ref:`Mbstring Unknown Encoding <mbstring-unknown-encoding>`
    + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`

  + Enumeration (enum)

    + :ref:`Duplicate Enum Case Value <duplicate-enum-case-value>`
    + :ref:`Enum Case Values <enum-case-values>`
    + :ref:`Enum Usage <enum-usage>`
    + :ref:`No Magic Method For Enum <no-magic-method-for-enum>`
    + :ref:`Undefined Enumcase <undefined-enumcase>`
    + :ref:`Unused Enumeration Case <unused-enumeration-case>`

  + Enumeration Case

    + :ref:`Duplicate Enum Case Value <duplicate-enum-case-value>`
    + :ref:`Undefined Enumcase <undefined-enumcase>`
    + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`

  + Environment Variables

    + :ref:`Environment Variables <environment-variables>`

  + Error

    + :ref:`Can't Implement Throwable <can't-implement-throwable>`
    + :ref:`Error Messages <error-messages>`
    + :ref:`Trigger Errors <trigger-errors>`

  + Error Handler

    + :ref:`Avoid set_error_handler $context Argument <avoid-set\_error\_handler-$context-argument>`
    + :ref:`set_exception_handler() Warning <set\_exception\_handler()-warning>`

  + Error Handling

    + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`

  + Escape Sequences

    + :ref:`Encoded Simple Letters <encoded-simple-letters>`
    + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`
    + :ref:`Unicode Escape Partial <unicode-escape-partial>`
    + :ref:`Unicode Escape Syntax <unicode-escape-syntax>`

  + Eval()

    + :ref:`Eval() Usage <eval()-usage>`
    + :ref:`eval() Without Try <eval()-without-try>`

  + Event Loop

    + :ref:`ext/ev <ext-ev>`

  + Exception

    + :ref:`Can't Implement Throwable <can't-implement-throwable>`
    + :ref:`Caught Variable <caught-variable>`
    + :ref:`Check Division By Zero <check-division-by-zero>`
    + :ref:`Converted Exceptions <converted-exceptions>`
    + :ref:`Could Use Try <could-use-try>`
    + :ref:`Defined Exceptions <defined-exceptions>`
    + :ref:`Error Messages <error-messages>`
    + :ref:`Exception Order <exception-order>`
    + :ref:`Forgotten Thrown <forgotten-thrown>`
    + :ref:`Long Preparation For Throw <long-preparation-for-throw>`
    + :ref:`Multiple Exceptions Catch() <multiple-exceptions-catch()>`
    + :ref:`Overwritten Exceptions <overwritten-exceptions>`
    + :ref:`PHP Exception <php-exception>`
    + :ref:`Rethrown Exceptions <rethrown-exceptions>`
    + :ref:`Throw <throw>`
    + :ref:`Throw Functioncall <throw-functioncall>`
    + :ref:`Throw Raw Exceptions <throw-raw-exceptions>`
    + :ref:`Thrown Exceptions <thrown-exceptions>`
    + :ref:`Try With Multiple Catch <try-with-multiple-catch>`
    + :ref:`Uncaught Exceptions <uncaught-exceptions>`
    + :ref:`Undefined Caught Exceptions <undefined-caught-exceptions>`
    + :ref:`Unthrown Exception <unthrown-exception>`
    + :ref:`Unused Exception Variable <unused-exception-variable>`
    + :ref:`Useless Catch <useless-catch>`
    + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`

  + Exit

    + :ref:`Die Exit Consistence <die-exit-consistence>`
    + :ref:`Error Messages <error-messages>`
    + :ref:`Exit Without Argument <exit-without-argument>`
    + :ref:`Exit() Usage <exit()-usage>`
    + :ref:`Exit-like Methods <exit-like-methods>`
    + :ref:`Or Die <or-die>`
    + :ref:`Or Die <or-die>`
    + :ref:`Print And Die <print-and-die>`

  + Exponent

    + :ref:`Exponent Usage <exponent-usage>`
    + :ref:`Negative Power <negative-power>`

  + Exponential

    + :ref:`** For Exponent <**-for-exponent>`

  + Expression

    + :ref:`Identical Consecutive Expression <identical-consecutive-expression>`

  + Extensible Markup Language (XML)

    + :ref:`No Net For Xml Load <no-net-for-xml-load>`
    + :ref:`ext/xmlreader <ext-xmlreader>`
    + :ref:`ext/xmlwriter <ext-xmlwriter>`

  + Extensions

    + :ref:`Dl() Usage <dl()-usage>`
    + :ref:`Is An Extension Class <is-an-extension-class>`
    + :ref:`Is An Extension Function <is-an-extension-function>`
    + :ref:`String <string>`
    + :ref:`ext/decimal <ext-decimal>`
    + :ref:`ext/eaccelerator <ext-eaccelerator>`

  + Fallback Function

    + :ref:`Fallback Function <fallback-function>`

  + False

    + :ref:`PHP 8.0 Types <php-8.0-types>`
    + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`

  + Feature

    + :ref:`PHP 7.2 Deprecations <php-7.2-deprecations>`

  + File

    + :ref:`File Usage <file-usage>`
    + :ref:`Fopen Binary Mode <fopen-binary-mode>`
    + :ref:`Linux Only Files <linux-only-files>`
    + :ref:`Use File Append <use-file-append>`
    + :ref:`Use Pathinfo <use-pathinfo>`
    + :ref:`ext/xattr <ext-xattr>`

  + File Extension

    + :ref:`Use Basename Suffix <use-basename-suffix>`

  + File Mode

    + :ref:`Wrong fopen() Mode <wrong-fopen()-mode>`

  + File Upload

    + :ref:`File Uploads <file-uploads>`
    + :ref:`Upload Filename Injection <upload-filename-injection>`
    + :ref:`move_uploaded_file Instead Of copy <move\_uploaded\_file-instead-of-copy>`

  + FileSystemIterator

    + :ref:`Avoid glob() Usage <avoid-glob()-usage>`

  + Final Class Constants

    + :ref:`Final Constant <final-constant>`

  + Final Keyword

    + :ref:`Can't Extend Final Class <can't-extend-final-class>`
    + :ref:`Can't Overwrite Final Constant <can't-overwrite-final-constant>`
    + :ref:`Can't Overwrite Final Method <can't-overwrite-final-method>`
    + :ref:`Class Could Be Final <class-could-be-final>`
    + :ref:`Class Should Be Final By Ocramius <class-should-be-final-by-ocramius>`
    + :ref:`Final Class Usage <final-class-usage>`
    + :ref:`Final Private Methods <final-private-methods>`
    + :ref:`Overwritten Constant <overwritten-constant>`
    + :ref:`Rewrote Final Class Constant <rewrote-final-class-constant>`
    + :ref:`Useless Final <useless-final>`

  + Finally

    + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
    + :ref:`Try With Finally <try-with-finally>`
    + :ref:`Try Without Catch <try-without-catch>`

  + First Class Callable

    + :ref:`First Class Callable <first-class-callable>`

  + Flag

    + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`

  + Floating Point Numbers

    + :ref:`Could Be Float <could-be-float>`
    + :ref:`Do Not Cast To Int <do-not-cast-to-int>`
    + :ref:`Manipulates NaN <manipulates-nan>`
    + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
    + :ref:`ext/decimal <ext-decimal>`

  + Fluent Interface

    + :ref:`Class Has Fluent Interface <class-has-fluent-interface>`
    + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`

  + For

    + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
    + :ref:`For Using Functioncall <for-using-functioncall>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`
    + :ref:`Sequences In For <sequences-in-for>`
    + :ref:`Should Use Foreach <should-use-foreach>`

  + Foreach

    + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
    + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
    + :ref:`Collect Block Size <collect-block-size>`
    + :ref:`Don't Reuse Foreach Source <don't-reuse-foreach-source>`
    + :ref:`Foreach Don't Change Pointer <foreach-don't-change-pointer>`
    + :ref:`Foreach Needs Reference Array <foreach-needs-reference-array>`
    + :ref:`Foreach On Object <foreach-on-object>`
    + :ref:`Foreach Reference Is Not Modified <foreach-reference-is-not-modified>`
    + :ref:`Foreach With list() <foreach-with-list()>`
    + :ref:`Foreach() Favorite <foreach()-favorite>`
    + :ref:`Identical Variables In Foreach <identical-variables-in-foreach>`
    + :ref:`Overwritten Foreach Var <overwritten-foreach-var>`
    + :ref:`Overwritten Source And Value <overwritten-source-and-value>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`
    + :ref:`Same Variable Foreach <same-variable-foreach>`
    + :ref:`Should Use Foreach <should-use-foreach>`
    + :ref:`Simplify Foreach <simplify-foreach>`
    + :ref:`Unset In Foreach <unset-in-foreach>`

  + Format

    + :ref:`ext/msgpack <ext-msgpack>`

  + Fossilized Methods

    + :ref:`Fossilized Method <fossilized-method>`
    + :ref:`Fossilized Methods List <fossilized-methods-list>`

  + Framework

    + :ref:`Codeigniter usage <codeigniter-usage>`
    + :ref:`Concrete5 usage <concrete5-usage>`
    + :ref:`Drupal Usage <drupal-usage>`
    + :ref:`Feast usage <feast-usage>`
    + :ref:`Fuel PHP Usage <fuel-php-usage>`
    + :ref:`Ice framework <ice-framework>`
    + :ref:`Joomla usage <joomla-usage>`
    + :ref:`Laravel usage <laravel-usage>`
    + :ref:`Phalcon Usage <phalcon-usage>`
    + :ref:`Sylius usage <sylius-usage>`
    + :ref:`Symfony usage <symfony-usage>`
    + :ref:`Typo 3 usage <typo-3-usage>`
    + :ref:`Wordpress usage <wordpress-usage>`
    + :ref:`Yii usage <yii-usage>`

  + Fully Qualified Name

    + :ref:`Constant : With Or Without Use <constant--with-or-without-use>`

  + Function Subscripting

    + :ref:`Function Subscripting <function-subscripting>`
    + :ref:`Function Subscripting, Old Style <function-subscripting,-old-style>`

  + Functions

    + :ref:`Class Function Confusion <class-function-confusion>`
    + :ref:`Conditioned Function <conditioned-function>`
    + :ref:`Empty Function <empty-function>`
    + :ref:`Fallback Function <fallback-function>`
    + :ref:`Function Called With Other Case Than Defined <function-called-with-other-case-than-defined>`
    + :ref:`Functions Glossary <functions-glossary>`
    + :ref:`Functions In Loop Calls <functions-in-loop-calls>`
    + :ref:`Functions Removed In PHP 5.4 <functions-removed-in-php-5.4>`
    + :ref:`Functions Using Reference <functions-using-reference>`
    + :ref:`Is An Extension Function <is-an-extension-function>`
    + :ref:`Methods That Should Not Be Used <methods-that-should-not-be-used>`
    + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`
    + :ref:`New Functions In PHP 7.0 <new-functions-in-php-7.0>`
    + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
    + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`
    + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`
    + :ref:`New Functions In PHP 7.4 <new-functions-in-php-7.4>`
    + :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`
    + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`
    + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`
    + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`
    + :ref:`New Functions In PHP 8.4 <new-functions-in-php-8.4>`
    + :ref:`One Letter Functions <one-letter-functions>`
    + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
    + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`
    + :ref:`PHP Overridden Function <php-overridden-function>`
    + :ref:`Real Functions <real-functions>`
    + :ref:`Redeclared PHP Functions <redeclared-php-functions>`
    + :ref:`Relay Function <relay-function>`
    + :ref:`Undefined Functions <undefined-functions>`
    + :ref:`Unused Functions <unused-functions>`
    + :ref:`Unusual Case For PHP Functions <unusual-case-for-php-functions>`
    + :ref:`Used Functions <used-functions>`
    + :ref:`Useless Default Argument <useless-default-argument>`
    + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

  + Generator

    + :ref:`Can't Call Generator <can't-call-generator>`
    + :ref:`Generator Cannot Return <generator-cannot-return>`
    + :ref:`Method Is A Generator <method-is-a-generator>`
    + :ref:`No Return For Generator <no-return-for-generator>`

  + Global Code

    + :ref:`Global Code Only <global-code-only>`
    + :ref:`No Class In Global <no-class-in-global>`

  + Global Space

    + :ref:`Don't Pollute Global Space <don't-pollute-global-space>`
    + :ref:`No Class In Global <no-class-in-global>`

  + Global Variables

    + :ref:`Declare Global Early <declare-global-early>`
    + :ref:`Globals <globals>`
    + :ref:`Make Global A Property <make-global-a-property>`

  + Goto

    + :ref:`Goto Names <goto-names>`
    + :ref:`Labels <labels>`
    + :ref:`Unused Label <unused-label>`

  + Goto Labels

    + :ref:`Goto Names <goto-names>`
    + :ref:`Labels <labels>`
    + :ref:`Unused Label <unused-label>`

  + HTML Entity

    + :ref:`Htmlentities Calls <htmlentities-calls>`
    + :ref:`Htmlentities Using Default Flag <htmlentities-using-default-flag>`

  + HTML Escaping

    + :ref:`No ENT_IGNORE <no-ent\_ignore>`

  + HTTP Headers

    + :ref:`Http Headers <http-headers>`
    + :ref:`Safe HTTP Headers <safe-http-headers>`
    + :ref:`Should Use SetCookie() <should-use-setcookie()>`

  + Hard Coded

    + :ref:`Hardcoded Passwords <hardcoded-passwords>`
    + :ref:`No Hardcoded Path <no-hardcoded-path>`

  + Hash

    + :ref:`Avoid Those Hash Functions <avoid-those-hash-functions>`
    + :ref:`Compare Hash <compare-hash>`
    + :ref:`Could Be array_combine() <could-be-array\_combine()>`
    + :ref:`Hash Algorithms <hash-algorithms>`
    + :ref:`Hash Will Use Objects <hash-will-use-objects>`

  + Heredocs

    + :ref:`All strings <all-strings>`
    + :ref:`Flexible Heredoc <flexible-heredoc>`
    + :ref:`Heredoc Delimiter <heredoc-delimiter>`
    + :ref:`Heredoc Delimiter Glossary <heredoc-delimiter-glossary>`
    + :ref:`Nowdoc Delimiter Glossary <nowdoc-delimiter-glossary>`

  + Hexadecimal Integer

    + :ref:`Hexadecimal Glossary <hexadecimal-glossary>`
    + :ref:`Hexadecimal In String <hexadecimal-in-string>`

  + Hyper Text Transfer Protocol (HTTP)

    + :ref:`HTTP Status Code <http-status-code>`
    + :ref:`Http Headers <http-headers>`

  + Hyper Text Transfer Protocol Secure (HTTPS)

    + :ref:`Safe Curl Options <safe-curl-options>`

  + IP

    + :ref:`Ip <ip>`
    + :ref:`No Hardcoded Ip <no-hardcoded-ip>`

  + Iconv

    + :ref:`Iconv With Translit <iconv-with-translit>`

  + Idempotent

    + :ref:`Double Instructions <double-instructions>`
    + :ref:`Recalled Condition <recalled-condition>`

  + If Then Else

    + :ref:`Collect Block Size <collect-block-size>`
    + :ref:`Could Be Else <could-be-else>`
    + :ref:`Else If Versus Elseif <else-if-versus-elseif>`
    + :ref:`Identical Elseif <identical-elseif>`
    + :ref:`Identical On Both Sides <identical-on-both-sides>`
    + :ref:`Implied If <implied-if>`
    + :ref:`Inconsistent Elseif <inconsistent-elseif>`
    + :ref:`Merge If Then <merge-if-then>`
    + :ref:`Method Is Not An If <method-is-not-an-if>`
    + :ref:`Nested Ifthen <nested-ifthen>`
    + :ref:`No Need For Else <no-need-for-else>`

  + Iffectation

    + :ref:`Recalled Condition <recalled-condition>`
    + :ref:`Variable Is Not A Condition <variable-is-not-a-condition>`

  + ImagickException

    + :ref:`Could Use Try <could-use-try>`

  + ImagickPixelException

    + :ref:`Could Use Try <could-use-try>`

  + Immutable

    + :ref:`Use DateTimeImmutable Class <use-datetimeimmutable-class>`

  + Inclusions

    + :ref:`Collect Block Size <collect-block-size>`
    + :ref:`Collect Class Children Count <collect-class-children-count>`
    + :ref:`Collect Class Depth <collect-class-depth>`
    + :ref:`Collect Class Interface Counts <collect-class-interface-counts>`
    + :ref:`Collect Local Variable Counts <collect-local-variable-counts>`
    + :ref:`Collect Mbstring Encodings <collect-mbstring-encodings>`
    + :ref:`Collect Method Counts <collect-method-counts>`
    + :ref:`Collect Parameter Counts <collect-parameter-counts>`
    + :ref:`Collect Parameter Names <collect-parameter-names>`
    + :ref:`Inclusions <inclusions>`
    + :ref:`Inclusions <inclusions>`
    + :ref:`Indentation Levels <indentation-levels>`

  + Incoming Data

    + :ref:`Don't Change Incomings <don't-change-incomings>`

  + Increment

    + :ref:`Pre-increment <pre-increment>`

  + Indentation

    + :ref:`Indentation Levels <indentation-levels>`
    + :ref:`Max Level Of Nesting <max-level-of-nesting>`
    + :ref:`More Than One Level Of Indentation <more-than-one-level-of-indentation>`
    + :ref:`Too Much Indented <too-much-indented>`

  + Index

    + :ref:`Multiple Index Definition <multiple-index-definition>`
    + :ref:`Negative Start Index In Array <negative-start-index-in-array>`
    + :ref:`No Object As Index <no-object-as-index>`
    + :ref:`Type Array Index <type-array-index>`
    + :ref:`Weird Array Index <weird-array-index>`
    + :ref:`array_key_exists() Works On Arrays <array\_key\_exists()-works-on-arrays>`

  + Index For Arrays

    + :ref:`No Null For Index <no-null-for-index>`
    + :ref:`PHP Arrays Index <php-arrays-index>`
    + :ref:`Should Yield With Key <should-yield-with-key>`

  + Inequality

    + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`

  + Infinite

    + :ref:`Infinite Recursion <infinite-recursion>`

  + Inheritance

    + :ref:`Already Parents Interface <already-parents-interface>`
    + :ref:`Inherited Property Type Must Match <inherited-property-type-must-match>`
    + :ref:`Inherited Static Variable <inherited-static-variable>`
    + :ref:`Method Is Overwritten <method-is-overwritten>`
    + :ref:`Overwritten Constant <overwritten-constant>`
    + :ref:`Overwritten Methods <overwritten-methods>`
    + :ref:`Overwritten Properties <overwritten-properties>`
    + :ref:`Property Used Above <property-used-above>`
    + :ref:`Too Many Children <too-many-children>`

  + Inherited Variable

    + :ref:`Unused Inherited Variable In Closure <unused-inherited-variable-in-closure>`

  + Initialisation

    + :ref:`Array With String Initialization <array-with-string-initialization>`
    + :ref:`Init Then Update <init-then-update>`

  + Injection

    + :ref:`Could Inject Parameter <could-inject-parameter>`
    + :ref:`DI Cyclic Dependencies <di-cyclic-dependencies>`
    + :ref:`Direct Injection <direct-injection>`
    + :ref:`Indirect Injection <indirect-injection>`
    + :ref:`Non Nullable Getters <non-nullable-getters>`
    + :ref:`Too Many Injections <too-many-injections>`

  + Insteadof

    + :ref:`Undefined Insteadof <undefined-insteadof>`

  + Interface

    + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
    + :ref:`Can't Implement Traversable <can't-implement-traversable>`
    + :ref:`Can't Overload Constants <can't-overload-constants>`
    + :ref:`Collect Dependency Extension <collect-dependency-extension>`
    + :ref:`Empty Interfaces <empty-interfaces>`
    + :ref:`Forgotten Interface <forgotten-interface>`
    + :ref:`Implements Is For Interface <implements-is-for-interface>`
    + :ref:`Insufficient Type <insufficient-type>`
    + :ref:`Interface Arguments <interface-arguments>`
    + :ref:`Interfaces Don't Ensure Properties <interfaces-don't-ensure-properties>`
    + :ref:`Interfaces Is Not Implemented <interfaces-is-not-implemented>`
    + :ref:`Interfaces Names <interfaces-names>`
    + :ref:`Interfaces Usage <interfaces-usage>`
    + :ref:`Is An Extension Interface <is-an-extension-interface>`
    + :ref:`Is Interface Method <is-interface-method>`
    + :ref:`Is_A() With String <is\_a()-with-string>`
    + :ref:`Manipulates INF <manipulates-inf>`
    + :ref:`No Constructor In Interface <no-constructor-in-interface>`
    + :ref:`PHP 7.0 New Interfaces <php-7.0-new-interfaces>`
    + :ref:`PHP Interfaces <php-interfaces>`
    + :ref:`Possible Interfaces <possible-interfaces>`
    + :ref:`Repeated Interface <repeated-interface>`
    + :ref:`Undefined Interfaces <undefined-interfaces>`
    + :ref:`Unused Interfaces <unused-interfaces>`
    + :ref:`Used Interfaces <used-interfaces>`
    + :ref:`Useless Interfaces <useless-interfaces>`

  + Internationalization

    + :ref:`idn_to_ascii() New Default <idn\_to\_ascii()-new-default>`

  + Interpolation

    + :ref:`Interpolation <interpolation>`
    + :ref:`Mixed Concat And Interpolation <mixed-concat-and-interpolation>`
    + :ref:`One Variable String <one-variable-string>`
    + :ref:`String Interpolation Favorite <string-interpolation-favorite>`
    + :ref:`String May Hold A Variable <string-may-hold-a-variable>`

  + Intersection Type

    + :ref:`Union Type <union-type>`
    + :ref:`Wrong Type With Call <wrong-type-with-call>`

  + InvalidArgumentException

    + :ref:`Could Use Try <could-use-try>`

  + Isset

    + :ref:`Isset Multiple Arguments <isset-multiple-arguments>`
    + :ref:`Isset() On The Whole Array <isset()-on-the-whole-array>`
    + :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
    + :ref:`isset() With Constants <isset()-with-constants>`

  + Iterable

    + :ref:`Could Type With Iterable <could-type-with-iterable>`
    + :ref:`This Could Be Iterable <this-could-be-iterable>`
    + :ref:`Typehint Could Be Iterable <typehint-could-be-iterable>`

  + JavaScript Object Notation (JSON)

    + :ref:`Check JSON <check-json>`
    + :ref:`Json_encode() Without Catching Exceptions <json\_encode()-without-catching-exceptions>`
    + :ref:`PHP Native Interfaces and Return Type <php-native-interfaces-and-return-type>`
    + :ref:`Use json_decode() Options <use-json\_decode()-options>`

  + JsonException

    + :ref:`Could Use Try <could-use-try>`

  + Keyword

    + :ref:`Php7 Relaxed Keyword <php7-relaxed-keyword>`

  + Language Construct

    + :ref:`Avoid Parenthesis With Language Construct <avoid-parenthesis-with-language-construct>`
    + :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`

  + Lazy Loading

    + :ref:`Abstract Or Implements <abstract-or-implements>`
    + :ref:`Inherited Class Constant Visibility <inherited-class-constant-visibility>`

  + Library Loading

    + :ref:`Dynamic Library Loading <dynamic-library-loading>`

  + Liskov Substitution Principle (LSP)

    + :ref:`Type Dodging <type-dodging>`

  + List

    + :ref:`Empty List <empty-list>`
    + :ref:`List With Array Appends <list-with-array-appends>`
    + :ref:`List With Keys <list-with-keys>`
    + :ref:`List With Reference <list-with-reference>`
    + :ref:`No List With String <no-list-with-string>`

  + Literal

    + :ref:`Duplicate Literal <duplicate-literal>`
    + :ref:`No Literal For Reference <no-literal-for-reference>`
    + :ref:`Overwritten Literals <overwritten-literals>`

  + Local Scope

    + :ref:`Too Many Local Variables <too-many-local-variables>`

  + Local Variable

    + :ref:`Blind Variables <blind-variables>`
    + :ref:`Too Many Local Variables <too-many-local-variables>`

  + Locale

    + :ref:`Wrong Locale <wrong-locale>`

  + Log

    + :ref:`Error_Log() Usage <error\_log()-usage>`

  + Logical Operators

    + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
    + :ref:`Logical Operators Favorite <logical-operators-favorite>`
    + :ref:`Logical Should Use Symbolic Operators <logical-should-use-symbolic-operators>`
    + :ref:`Not Not <not-not>`
    + :ref:`Not Or Tilde <not-or-tilde>`

  + Loops

    + :ref:`Altering Foreach Without Reference <altering-foreach-without-reference>`
    + :ref:`Avoid Concat In Loop <avoid-concat-in-loop>`
    + :ref:`Break Outside Loop <break-outside-loop>`
    + :ref:`Continue Is For Loop <continue-is-for-loop>`
    + :ref:`Dangling Array References <dangling-array-references>`
    + :ref:`Don't Change The Blind Var <don't-change-the-blind-var>`
    + :ref:`Empty Loop <empty-loop>`
    + :ref:`Foreach On Object <foreach-on-object>`
    + :ref:`Infinite Recursion <infinite-recursion>`
    + :ref:`Possible Infinite Loop <possible-infinite-loop>`
    + :ref:`Queries In Loops <queries-in-loops>`
    + :ref:`Static Loop <static-loop>`
    + :ref:`Substr() In Loops <substr()-in-loops>`
    + :ref:`Unconditional Break In Loop <unconditional-break-in-loop>`
    + :ref:`Use Variable Created Inside Loop <use-variable-created-inside-loop>`

  + Machine Learning

    + :ref:`ext/fann <ext-fann>`

  + Magic Constants

    + :ref:`Could Use Namespace Magic Constant <could-use-namespace-magic-constant>`
    + :ref:`Could Use __DIR__ <could-use-\_\_dir\_\_>`
    + :ref:`Magic Constant Usage <magic-constant-usage>`

  + Magic Methods

    + :ref:`Check On __Call Usage <check-on-\_\_call-usage>`
    + :ref:`Could Be Stringable <could-be-stringable>`
    + :ref:`Create Magic Method <create-magic-method>`
    + :ref:`Direct Call To __clone() <direct-call-to-\_\_clone()>`
    + :ref:`Has Magic Method <has-magic-method>`
    + :ref:`Magic Method Returntype Is Restricted <magic-method-returntype-is-restricted>`
    + :ref:`Magic Methods <magic-methods>`
    + :ref:`Magic Visibility <magic-visibility>`
    + :ref:`Make Magic Concrete <make-magic-concrete>`
    + :ref:`Missing __isset() Method <missing-\_\_isset()-method>`
    + :ref:`Must Return Methods <must-return-methods>`
    + :ref:`No Magic Method For Enum <no-magic-method-for-enum>`
    + :ref:`No Magic Method With Array <no-magic-method-with-array>`
    + :ref:`Reserved Methods <reserved-methods>`
    + :ref:`Useless Type <useless-type>`
    + :ref:`__debugInfo() Usage <\_\_debuginfo()-usage>`
    + :ref:`__toString() Throws Exception <\_\_tostring()-throws-exception>`

  + Magic Property

    + :ref:`Create Magic Property <create-magic-property>`
    + :ref:`Is A Magic Property <is-a-magic-property>`
    + :ref:`Magic Properties <magic-properties>`

  + Map

    + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`

  + Match

    + :ref:`Could Use Match <could-use-match>`
    + :ref:`Reserved Match Keyword <reserved-match-keyword>`
    + :ref:`Simple Switch And Match <simple-switch-and-match>`
    + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
    + :ref:`Switch To Switch <switch-to-switch>`
    + :ref:`Switch Without Default <switch-without-default>`
    + :ref:`Uses PHP 8 Match() <uses-php-8-match()>`

  + Memoization

    + :ref:`Memoize MagicCall <memoize-magiccall>`
    + :ref:`Reuse Existing Variable <reuse-existing-variable>`

  + Merge

    + :ref:`Ellipsis Merge <ellipsis-merge>`
    + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`

  + Message Digest Algorithm 5 (MD5)

    + :ref:`Md5 Strings <md5-strings>`

  + Method

    + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
    + :ref:`Abstract Static Methods <abstract-static-methods>`
    + :ref:`Could Be Protected Method <could-be-protected-method>`
    + :ref:`Different Argument Counts <different-argument-counts>`
    + :ref:`Dynamic Methodcall <dynamic-methodcall>`
    + :ref:`Identical Methods <identical-methods>`
    + :ref:`Illegal Name For Method <illegal-name-for-method>`
    + :ref:`Implemented Methods Must Be Public <implemented-methods-must-be-public>`
    + :ref:`Interface Methods <interface-methods>`
    + :ref:`Method Collision Traits <method-collision-traits>`
    + :ref:`Method Could Be Private Method <method-could-be-private-method>`
    + :ref:`Method Is Not An If <method-is-not-an-if>`
    + :ref:`Method Is Not For Fluent Interface <method-is-not-for-fluent-interface>`
    + :ref:`Method Used Below <method-used-below>`
    + :ref:`Normal Methods <normal-methods>`
    + :ref:`Overwritten Methods <overwritten-methods>`
    + :ref:`Redefined Methods <redefined-methods>`
    + :ref:`Set Class Method Remote Definition <set-class-method-remote-definition>`
    + :ref:`Solve Trait Methods <solve-trait-methods>`
    + :ref:`Trait Methods <trait-methods>`
    + :ref:`Undefined Insteadof <undefined-insteadof>`
    + :ref:`Undefined Methods <undefined-methods>`
    + :ref:`Unreachable Method <unreachable-method>`
    + :ref:`Unused Methods <unused-methods>`
    + :ref:`Unused Public Methods <unused-public-methods>`
    + :ref:`Used Methods <used-methods>`
    + :ref:`Used Once Property <used-once-property>`
    + :ref:`Used Private Methods <used-private-methods>`
    + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

  + Methodcall

    + :ref:`Methodcall On New <methodcall-on-new>`

  + Micro-optimisation

    + :ref:`Duplicate Calls <duplicate-calls>`
    + :ref:`Ellipsis Merge <ellipsis-merge>`
    + :ref:`Pre-Calculate Use <pre-calculate-use>`
    + :ref:`Recalled Condition <recalled-condition>`
    + :ref:`Should Cache Local <should-cache-local>`
    + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`
    + :ref:`Unpreprocessed Values <unpreprocessed-values>`

  + Microtime()

    + :ref:`PHP 7.1 Microseconds <php-7.1-microseconds>`

  + Mixed

    + :ref:`Mixed Type Usage <mixed-type-usage>`
    + :ref:`PHP 8.0 Types <php-8.0-types>`
    + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
    + :ref:`The Mixed Keyword <the-mixed-keyword>`

  + Multibyte String

    + :ref:`Avoid mb_dectect_encoding() <avoid-mb\_dectect\_encoding()>`
    + :ref:`Mbstring Third Arg <mbstring-third-arg>`
    + :ref:`Mbstring Unknown Encoding <mbstring-unknown-encoding>`
    + :ref:`Mbstring Unknown Encodings <mbstring-unknown-encodings>`

  + Multidimensional Array

    + :ref:`Multidimensional Arrays <multidimensional-arrays>`
    + :ref:`Too Many Array Dimensions <too-many-array-dimensions>`

  + Name

    + :ref:`Same Name For Property And Method <same-name-for-property-and-method>`

  + Named Parameters

    + :ref:`Duplicate Named Parameter <duplicate-named-parameter>`
    + :ref:`Mismatch Parameter Name <mismatch-parameter-name>`
    + :ref:`Named Arguments And Variadic <named-arguments-and-variadic>`
    + :ref:`Named Parameter Usage <named-parameter-usage>`
    + :ref:`No Named Parameters <no-named-parameters>`
    + :ref:`Remove Parameter With Named Parameters <remove-parameter-with-named-parameters>`
    + :ref:`Unknown Parameter Name <unknown-parameter-name>`
    + :ref:`Wrong Argument Name With PHP Function <wrong-argument-name-with-php-function>`

  + Namespaces

    + :ref:`Aliases <aliases>`
    + :ref:`Could Use Alias <could-use-alias>`
    + :ref:`Empty Namespace <empty-namespace>`
    + :ref:`Fully Qualified Constants <fully-qualified-constants>`
    + :ref:`Global Import <global-import>`
    + :ref:`Multiple Alias Definitions <multiple-alias-definitions>`
    + :ref:`Static Variable In Namespace <static-variable-in-namespace>`
    + :ref:`Unresolved Use <unresolved-use>`
    + :ref:`Wrong Case Namespaces <wrong-case-namespaces>`

  + Naming

    + :ref:`Multiple Alias Definitions <multiple-alias-definitions>`
    + :ref:`Reserved Methods <reserved-methods>`

  + Native

    + :ref:`Native Alias Functions Usage <native-alias-functions-usage>`
    + :ref:`New Functions In PHP 5.4 <new-functions-in-php-5.4>`
    + :ref:`New Functions In PHP 7.1 <new-functions-in-php-7.1>`
    + :ref:`New Functions In PHP 7.2 <new-functions-in-php-7.2>`
    + :ref:`New Functions In PHP 7.3 <new-functions-in-php-7.3>`
    + :ref:`New Functions In PHP 7.4 <new-functions-in-php-7.4>`
    + :ref:`New Functions In PHP 8.0 <new-functions-in-php-8.0>`
    + :ref:`New Functions In PHP 8.1 <new-functions-in-php-8.1>`
    + :ref:`New Functions In PHP 8.2 <new-functions-in-php-8.2>`
    + :ref:`New Functions In PHP 8.3 <new-functions-in-php-8.3>`
    + :ref:`PHP 7.4 Removed Functions <php-7.4-removed-functions>`
    + :ref:`PHP 8.0 Removed Functions <php-8.0-removed-functions>`
    + :ref:`PHP 8.1 Removed Functions <php-8.1-removed-functions>`
    + :ref:`PHP Interfaces <php-interfaces>`
    + :ref:`Too Many Native Calls <too-many-native-calls>`

  + Nested Attributes

    + :ref:`Nested Attributes <nested-attributes>`
    + :ref:`New Initializers <new-initializers>`

  + Nesting

    + :ref:`Nested Loops <nested-loops>`

  + Neutral Element

    + :ref:`Multiply By One <multiply-by-one>`

  + Never Type

    + :ref:`Methods Without Return <methods-without-return>`
    + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
    + :ref:`Never Keyword <never-keyword>`
    + :ref:`Type Could Be Never <type-could-be-never>`
    + :ref:`Type Must Be Returned <type-must-be-returned>`

  + New In Initializers

    + :ref:`Nested Attributes <nested-attributes>`
    + :ref:`New Initializers <new-initializers>`

  + Non Breakable Spaces

    + :ref:`Non Breakable Space In Names <non-breakable-space-in-names>`
    + :ref:`Strings With Strange Space <strings-with-strange-space>`

  + Nowdocs

    + :ref:`All strings <all-strings>`
    + :ref:`Nowdoc Delimiter Glossary <nowdoc-delimiter-glossary>`

  + Null

    + :ref:`Avoid Optional Properties <avoid-optional-properties>`
    + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
    + :ref:`Could Be Null <could-be-null>`
    + :ref:`No Null For Index <no-null-for-index>`
    + :ref:`No Null For Native PHP Functions <no-null-for-native-php-functions>`
    + :ref:`No get_class() With Null <no-get\_class()-with-null>`
    + :ref:`Null On New <null-on-new>`
    + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
    + :ref:`Null Type Favorite <null-type-favorite>`
    + :ref:`Nullable Without Check <nullable-without-check>`
    + :ref:`Php 8.0 Only TypeHints <php-8.0-only-typehints>`
    + :ref:`Use === null <use-===-null>`

  + Null Safe Object Operator

    + :ref:`Check After Null Safe Operator <check-after-null-safe-operator>`
    + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
    + :ref:`No Null With Null Safe Operator <no-null-with-null-safe-operator>`

  + Nullable

    + :ref:`Could Be Null <could-be-null>`
    + :ref:`Could Use Null-Safe Object Operator <could-use-null-safe-object-operator>`
    + :ref:`Implicit Nullable Type <implicit-nullable-type>`
    + :ref:`Use Nullable Type <use-nullable-type>`

  + Numeric Separator

    + :ref:`Numeric Literal Separator <numeric-literal-separator>`

  + Object

    + :ref:`Array_Fill() With Objects <array\_fill()-with-objects>`
    + :ref:`Hash Will Use Objects <hash-will-use-objects>`
    + :ref:`Scalar Or Object Property <scalar-or-object-property>`
    + :ref:`Static Methods Called From Object <static-methods-called-from-object>`
    + :ref:`Unfinished Object <unfinished-object>`

  + Object API

    + :ref:`Use PHP Object API <use-php-object-api>`

  + Object Invasion

    + :ref:`Property Invasion <property-invasion>`

  + Object Nullsafe Operator ?->

    + :ref:`Useless NullSafe Operator <useless-nullsafe-operator>`

  + Object Operator ->

    + :ref:`Use NullSafe Operator <use-nullsafe-operator>`

  + Octal Integer

    + :ref:`Malformed Octal <malformed-octal>`

  + Opcode

    + :ref:`Always Use Function With array_key_exists() <always-use-function-with-array\_key\_exists()>`
    + :ref:`array_key_exists() Speedup <array\_key\_exists()-speedup>`

  + OpenSSL

    + :ref:`Check Crypto Key Length <check-crypto-key-length>`
    + :ref:`OpenSSL Ciphers Used <openssl-ciphers-used>`
    + :ref:`Openssl Encrypt Default Algorithm Change <openssl-encrypt-default-algorithm-change>`
    + :ref:`ext/mcrypt <ext-mcrypt>`
    + :ref:`openssl_random_pseudo_byte() Second Argument <openssl\_random\_pseudo\_byte()-second-argument>`

  + Operator Precedence

    + :ref:`Useless Parenthesis <useless-parenthesis>`

  + Operators

    + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
    + :ref:`Difference Consistence <difference-consistence>`
    + :ref:`Should Use Operator <should-use-operator>`
    + :ref:`Unsupported Types With Operators <unsupported-types-with-operators>`
    + :ref:`Useless Parenthesis <useless-parenthesis>`

  + Optional Parameter

    + :ref:`Optional Parameter <optional-parameter>`
    + :ref:`Wrong Optional Parameter <wrong-optional-parameter>`

  + Outgoing Data

    + :ref:`Don't Change Incomings <don't-change-incomings>`

  + Overenginer

    + :ref:`Used Once Trait <used-once-trait>`

  + Override Attribute

    + :ref:`Method Is Overwritten <method-is-overwritten>`
    + :ref:`Missing Overriden Method <missing-overriden-method>`
    + :ref:`Useless Override Attribute <useless-override-attribute>`

  + Overwrite

    + :ref:`Can't Overwrite Final Constant <can't-overwrite-final-constant>`
    + :ref:`Can't Overwrite Final Method <can't-overwrite-final-method>`
    + :ref:`Immutable Signature <immutable-signature>`
    + :ref:`Overwritten Class Constants <overwritten-class-constants>`
    + :ref:`Redefined Methods <redefined-methods>`

  + PDOException

    + :ref:`Could Use Try <could-use-try>`

  + PEAR

    + :ref:`Pear Usage <pear-usage>`

  + PHP Extension C Library (PECL)

    + :ref:`ext/lua <ext-lua>`

  + PHP Handlers

    + :ref:`PHP Handlers Usage <php-handlers-usage>`

  + PHP Predefined Exception

    + :ref:`Defined Exceptions <defined-exceptions>`
    + :ref:`Undefined Caught Exceptions <undefined-caught-exceptions>`

  + PHP Profiler

    + :ref:`ext/spx <ext-spx>`
    + :ref:`ext/xhprof <ext-xhprof>`

  + PHP Standards Recommendations (PSR)

    + :ref:`PSR-11 Usage <psr-11-usage>`
    + :ref:`PSR-13 Usage <psr-13-usage>`
    + :ref:`PSR-16 Usage <psr-16-usage>`
    + :ref:`PSR-3 Usage <psr-3-usage>`
    + :ref:`PSR-6 Usage <psr-6-usage>`
    + :ref:`PSR-7 Usage <psr-7-usage>`
    + :ref:`ext/psr <ext-psr>`

  + PHP Tags

    + :ref:`Using Short Tags <using-short-tags>`

  + PHP Variables

    + :ref:`Safe Phpvariables <safe-phpvariables>`

  + Parameter

    + :ref:`Cancelled Parameter <cancelled-parameter>`
    + :ref:`Links Between Parameter And Argument <links-between-parameter-and-argument>`
    + :ref:`Mismatch Parameter And Type <mismatch-parameter-and-type>`
    + :ref:`Mismatched Default Arguments <mismatched-default-arguments>`
    + :ref:`Missing Type In Definition <missing-type-in-definition>`
    + :ref:`Modified Typed Parameter <modified-typed-parameter>`
    + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
    + :ref:`Optional Parameter <optional-parameter>`
    + :ref:`PHP 80 Named Parameter Variadic <php-80-named-parameter-variadic>`
    + :ref:`Parameter Hiding <parameter-hiding>`
    + :ref:`Parenthesis As Parameter <parenthesis-as-parameter>`
    + :ref:`Too Many Parameters <too-many-parameters>`
    + :ref:`Unused Parameter <unused-parameter>`
    + :ref:`Wrong Optional Parameter <wrong-optional-parameter>`

  + Parenthesis

    + :ref:`Coalesce And Concat <coalesce-and-concat>`
    + :ref:`Dynamic New <dynamic-new>`
    + :ref:`Missing Parenthesis <missing-parenthesis>`
    + :ref:`Nested Ternary Without Parenthesis <nested-ternary-without-parenthesis>`
    + :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`
    + :ref:`Parenthesis As Parameter <parenthesis-as-parameter>`

  + Passing By Reference

    + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
    + :ref:`Calltime Pass By Reference <calltime-pass-by-reference>`

  + Passing By Value

    + :ref:`Array_Map() Passes By Value <array\_map()-passes-by-value>`
    + :ref:`Calltime Pass By Reference <calltime-pass-by-reference>`

  + Password

    + :ref:`Hardcoded Passwords <hardcoded-passwords>`

  + Path

    + :ref:`No Hardcoded Path <no-hardcoded-path>`
    + :ref:`Pathinfo() Returns May Vary <pathinfo()-returns-may-vary>`
    + :ref:`Use Pathinfo <use-pathinfo>`
    + :ref:`Use pathinfo() Arguments <use-pathinfo()-arguments>`

  + Performance

    + :ref:`Skip Empty Array When Merging <skip-empty-array-when-merging>`

  + Phar

    + :ref:`__halt_compiler <\_\_halt\_compiler>`

  + PharException

    + :ref:`Could Use Try <could-use-try>`

  + Port

    + :ref:`No Hardcoded Port <no-hardcoded-port>`

  + Precedence

    + :ref:`Assign And Lettered Logical Operator Precedence <assign-and-lettered-logical-operator-precedence>`
    + :ref:`Coalesce And Concat <coalesce-and-concat>`

  + Predefined Constants

    + :ref:`Should Use Existing Constants <should-use-existing-constants>`

  + Preprocessing

    + :ref:`Preprocess Arrays <preprocess-arrays>`
    + :ref:`Preprocessable <preprocessable>`
    + :ref:`Should Preprocess Chr() <should-preprocess-chr()>`
    + :ref:`Unpreprocessed Values <unpreprocessed-values>`

  + Print

    + :ref:`Displays Text <displays-text>`
    + :ref:`Echo Or Print <echo-or-print>`
    + :ref:`Print And Die <print-and-die>`
    + :ref:`Printf Number Of Arguments <printf-number-of-arguments>`
    + :ref:`Repeated print() <repeated-print()>`

  + Private Visibility

    + :ref:`Accessing Private <accessing-private>`
    + :ref:`Final Private Methods <final-private-methods>`
    + :ref:`Method Could Be Private Method <method-could-be-private-method>`
    + :ref:`Redefined Private Property <redefined-private-property>`

  + Promoted Properties

    + :ref:`Could Use Promoted Properties <could-use-promoted-properties>`
    + :ref:`Promoted Properties <promoted-properties>`
    + :ref:`Useless Assignation Of Promoted Property <useless-assignation-of-promoted-property>`

  + Properties

    + :ref:`Avoid Optional Properties <avoid-optional-properties>`
    + :ref:`Checks Property Existence <checks-property-existence>`
    + :ref:`Collect Property Counts <collect-property-counts>`
    + :ref:`Defined Properties <defined-properties>`
    + :ref:`Don't Unset Properties <don't-unset-properties>`
    + :ref:`Find Key Directly <find-key-directly>`
    + :ref:`Inherited Property Type Must Match <inherited-property-type-must-match>`
    + :ref:`Integer As Property <integer-as-property>`
    + :ref:`Internally Used Properties <internally-used-properties>`
    + :ref:`Locally Unused Property <locally-unused-property>`
    + :ref:`Locally Used Property <locally-used-property>`
    + :ref:`Locally Used Property In Trait <locally-used-property-in-trait>`
    + :ref:`Mismatch Properties Types <mismatch-properties-types>`
    + :ref:`Missing Type In Definition <missing-type-in-definition>`
    + :ref:`Never Used Properties <never-used-properties>`
    + :ref:`No Reference For Static Property <no-reference-for-static-property>`
    + :ref:`Overwritten Properties <overwritten-properties>`
    + :ref:`Properties Declaration Consistence <properties-declaration-consistence>`
    + :ref:`Property Could Be Local <property-could-be-local>`
    + :ref:`Property Names <property-names>`
    + :ref:`Property Used Above <property-used-above>`
    + :ref:`Property Used Below <property-used-below>`
    + :ref:`Property Used In One Method Only <property-used-in-one-method-only>`
    + :ref:`Property Variable Confusion <property-variable-confusion>`
    + :ref:`Redefined Property <redefined-property>`
    + :ref:`Static Properties <static-properties>`
    + :ref:`Undefined Properties <undefined-properties>`
    + :ref:`Uninitialized Property <uninitialized-property>`
    + :ref:`Unitialized Properties <unitialized-properties>`
    + :ref:`Untyped No Default Properties <untyped-no-default-properties>`

  + Property Hook

    + :ref:`Has Virtual Property <has-virtual-property>`

  + Property Type Declaration

    + :ref:`Typed Property Usage <typed-property-usage>`

  + Protocol

    + :ref:`Protocol lists <protocol-lists>`

  + Public Visibility

    + :ref:`Unused Public Methods <unused-public-methods>`

  + Query

    + :ref:`Queries In Loops <queries-in-loops>`

  + Query String

    + :ref:`parse_str() Warning <parse\_str()-warning>`

  + Random

    + :ref:`Const With Array <const-with-array>`
    + :ref:`Random Without Try <random-without-try>`
    + :ref:`Use random_int() <use-random\_int()>`

  + Readability

    + :ref:`Collect Readability <collect-readability>`
    + :ref:`Don't Mix ++ <don't-mix-++>`
    + :ref:`Long Arguments <long-arguments>`
    + :ref:`Missing Parenthesis <missing-parenthesis>`
    + :ref:`No Initial S In Variable Names <no-initial-s-in-variable-names>`
    + :ref:`One Object Operator Per Line <one-object-operator-per-line>`
    + :ref:`Preprocessable <preprocessable>`
    + :ref:`Recycled Variables <recycled-variables>`

  + Readonly

    + :ref:`Class Could Be Readonly <class-could-be-readonly>`
    + :ref:`No Readonly Assignation In Global <no-readonly-assignation-in-global>`
    + :ref:`Property Cannot Be Readonly <property-cannot-be-readonly>`
    + :ref:`Readonly Usage <readonly-usage>`

  + Real Numbers

    + :ref:`Avoid Real <avoid-real>`
    + :ref:`No Real Comparison <no-real-comparison>`

  + Recursion

    + :ref:`Functions In Loop Calls <functions-in-loop-calls>`
    + :ref:`Infinite Recursion <infinite-recursion>`
    + :ref:`Recursive Functions <recursive-functions>`

  + References

    + :ref:`Class-typed References <class-typed-references>`
    + :ref:`Foreach Needs Reference Array <foreach-needs-reference-array>`
    + :ref:`Foreach Reference Is Not Modified <foreach-reference-is-not-modified>`
    + :ref:`Functions Using Reference <functions-using-reference>`
    + :ref:`List With Reference <list-with-reference>`
    + :ref:`Lost References <lost-references>`
    + :ref:`Make Functioncall With Reference <make-functioncall-with-reference>`
    + :ref:`No Default For Referenced Parameter <no-default-for-referenced-parameter>`
    + :ref:`No Literal For Reference <no-literal-for-reference>`
    + :ref:`No Reference For Static Property <no-reference-for-static-property>`
    + :ref:`No Reference On Left Side <no-reference-on-left-side>`
    + :ref:`No Referenced Void <no-referenced-void>`
    + :ref:`Objects Don't Need References <objects-don't-need-references>`
    + :ref:`Only Variable For Reference <only-variable-for-reference>`
    + :ref:`Only Variable Passed By Reference <only-variable-passed-by-reference>`
    + :ref:`Only Variable Returned By Reference <only-variable-returned-by-reference>`
    + :ref:`Php Native Reference Variable <php-native-reference-variable>`
    + :ref:`Useless Referenced Argument <useless-referenced-argument>`
    + :ref:`Variable References <variable-references>`

  + Reflection

    + :ref:`Reflection Export() Is Deprecated <reflection-export()-is-deprecated>`

  + ReflectionException

    + :ref:`Could Use Try <could-use-try>`

  + Register Globals

    + :ref:`Register Globals <register-globals>`

  + Regular Expressions

    + :ref:`Always Anchor Regex <always-anchor-regex>`
    + :ref:`Invalid Regex <invalid-regex>`
    + :ref:`Named Regex <named-regex>`
    + :ref:`Perl Regex <perl-regex>`
    + :ref:`Possible Missing Subpattern <possible-missing-subpattern>`
    + :ref:`Regex Delimiter <regex-delimiter>`
    + :ref:`Regex Inventory <regex-inventory>`
    + :ref:`Regex On Arrays <regex-on-arrays>`
    + :ref:`Repeated Regex <repeated-regex>`
    + :ref:`Simplify Regex <simplify-regex>`
    + :ref:`Unknown Pcre2 Option <unknown-pcre2-option>`
    + :ref:`Unkown Regex Options <unkown-regex-options>`
    + :ref:`preg_match_all() Flag <preg\_match\_all()-flag>`
    + :ref:`preg_replace With Option e <preg\_replace-with-option-e>`

  + Remote Procedure Call (RPC)

    + :ref:`Extensions yar <extensions-yar>`
    + :ref:`ext/xmlrpc <ext-xmlrpc>`

  + Reserved Names

    + :ref:`PHP Keywords As Names <php-keywords-as-names>`
    + :ref:`Php7 Relaxed Keyword <php7-relaxed-keyword>`

  + Return

    + :ref:`Bail Out Early <bail-out-early>`
    + :ref:`Cant Use Return Value In Write Context <cant-use-return-value-in-write-context>`
    + :ref:`Drop Else After Return <drop-else-after-return>`
    + :ref:`Methods Without Return <methods-without-return>`
    + :ref:`Multiple Returns <multiple-returns>`
    + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
    + :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`
    + :ref:`No Return Or Throw In Finally <no-return-or-throw-in-finally>`
    + :ref:`No Return Used <no-return-used>`
    + :ref:`Unused Returned Value <unused-returned-value>`
    + :ref:`Useless Return <useless-return>`

  + Return Type

    + :ref:`Missing Some Returntype <missing-some-returntype>`
    + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
    + :ref:`Nullable Without Check <nullable-without-check>`
    + :ref:`Return Type Usage <return-type-usage>`
    + :ref:`Type Must Be Returned <type-must-be-returned>`

  + Return Type Will Change

    + :ref:`PHP Native Class Type Compatibility <php-native-class-type-compatibility>`

  + Return Value

    + :ref:`Missing Type In Definition <missing-type-in-definition>`
    + :ref:`Return With Parenthesis <return-with-parenthesis>`

  + SSL

    + :ref:`No Weak SSL Crypto <no-weak-ssl-crypto>`
    + :ref:`Safe Curl Options <safe-curl-options>`

  + SVMException

    + :ref:`Could Use Try <could-use-try>`

  + Scalar Types

    + :ref:`Not A Scalar Type <not-a-scalar-type>`
    + :ref:`PHP 8.1 Types <php-8.1-types>`
    + :ref:`Scalar Or Object Property <scalar-or-object-property>`
    + :ref:`Scalar Type Usage <scalar-type-usage>`

  + Scope

    + :ref:`Implicit Global <implicit-global>`
    + :ref:`Too Many Local Variables <too-many-local-variables>`

  + Scope Resolution Operator ::

    + :ref:`Scope Resolution Operator <scope-resolution-operator>`

  + Self

    + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
    + :ref:`Avoid Self In Interface <avoid-self-in-interface>`
    + :ref:`Could Be Self <could-be-self>`
    + :ref:`Could Use self <could-use-self>`
    + :ref:`Parent Is Not Static <parent-is-not-static>`
    + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
    + :ref:`Should Use Local Class <should-use-local-class>`
    + :ref:`Static Call With Self <static-call-with-self>`
    + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
    + :ref:`Use This <use-this>`
    + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`

  + Semantics

    + :ref:`Confusing Names <confusing-names>`
    + :ref:`Don't Use The Type As Variable Name <don't-use-the-type-as-variable-name>`
    + :ref:`Mismatch Parameter And Type <mismatch-parameter-and-type>`
    + :ref:`One Letter Functions <one-letter-functions>`
    + :ref:`Possible Alias Confusion <possible-alias-confusion>`
    + :ref:`Property Variable Confusion <property-variable-confusion>`

  + Serialization

    + :ref:`Serialize Magic Method <serialize-magic-method>`
    + :ref:`Unserialize Second Arg <unserialize-second-arg>`

  + Server Application Programming Interface (SAPI)

    + :ref:`PHP Sapi <php-sapi>`

  + Session

    + :ref:`Session Lazy Write <session-lazy-write>`
    + :ref:`Session Variables <session-variables>`
    + :ref:`Should Use session_regenerateid() <should-use-session\_regenerateid()>`
    + :ref:`Use session_start() Options <use-session\_start()-options>`
    + :ref:`ext/session <ext-session>`

  + Shell

    + :ref:`Shell Favorite <shell-favorite>`
    + :ref:`Shell Usage <shell-usage>`

  + Short Assignations

    + :ref:`Adding Zero <adding-zero>`
    + :ref:`Could Be Ternary <could-be-ternary>`
    + :ref:`Could Use Short Assignation <could-use-short-assignation>`

  + Short Syntax

    + :ref:`Coalesce Equal <coalesce-equal>`
    + :ref:`List Short Syntax <list-short-syntax>`

  + Short Tags

    + :ref:`Short Open Tags <short-open-tags>`
    + :ref:`Using Short Tags <using-short-tags>`

  + Short Ternary Operator

    + :ref:`Short Ternary <short-ternary>`
    + :ref:`Useless Short Ternary <useless-short-ternary>`

  + Silent Behavior

    + :ref:`File_Put_Contents Using Array Argument <file\_put\_contents-using-array-argument>`
    + :ref:`Never Called Parameter <never-called-parameter>`
    + :ref:`Silently Cast Integer <silently-cast-integer>`

  + Single Quotes Strings

    + :ref:`Should Be Single Quote <should-be-single-quote>`

  + Sort

    + :ref:`Usort Sorting In PHP 7.0 <usort-sorting-in-php-7.0>`

  + Spaceship Operator

    + :ref:`Could Be Spaceship <could-be-spaceship>`

  + Sqlite3

    + :ref:`Sqlite3 Requires Single Quotes <sqlite3-requires-single-quotes>`

  + Static Constant

    + :ref:`Abstract Class Constants <abstract-class-constants>`
    + :ref:`Constant Class <constant-class>`
    + :ref:`Constant Definition <constant-definition>`
    + :ref:`Constant Used Below <constant-used-below>`
    + :ref:`Could Be Class Constant <could-be-class-constant>`
    + :ref:`Could Be Protected Class Constant <could-be-protected-class-constant>`
    + :ref:`Defined Class Constants <defined-class-constants>`
    + :ref:`Makes Class Constant Definition <makes-class-constant-definition>`
    + :ref:`New Dynamic Class Constant Syntax <new-dynamic-class-constant-syntax>`
    + :ref:`Overwritten Class Constants <overwritten-class-constants>`
    + :ref:`Overwritten Constant <overwritten-constant>`
    + :ref:`Redefined Class Constants <redefined-class-constants>`
    + :ref:`Undefined Class Constants <undefined-class-constants>`
    + :ref:`Unused Class Constant <unused-class-constant>`

  + Static Expression

    + :ref:`Static Inclusions <static-inclusions>`

  + Static Method

    + :ref:`Calling Static Trait Method <calling-static-trait-method>`
    + :ref:`Cannot Call Static Trait Method Directly <cannot-call-static-trait-method-directly>`
    + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

  + Static Variables

    + :ref:`Could Be A Static Variable <could-be-a-static-variable>`
    + :ref:`Declare Global Early <declare-global-early>`
    + :ref:`Inherited Static Variable <inherited-static-variable>`
    + :ref:`No Static Variable In A Method <no-static-variable-in-a-method>`
    + :ref:`Redeclared Static Variable <redeclared-static-variable>`
    + :ref:`Static Variable Can Default To Arbitrary Expression <static-variable-can-default-to-arbitrary-expression>`
    + :ref:`Static Variable In Namespace <static-variable-in-namespace>`
    + :ref:`Static Variables <static-variables>`
    + :ref:`Used Once Variables (In Scope) <used-once-variables-(in-scope)>`

  + Strict Comparison

    + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
    + :ref:`Strict In_Array() Preference <strict-in\_array()-preference>`
    + :ref:`Strpos()-like Comparison <strpos()-like-comparison>`
    + :ref:`Use === null <use-===-null>`

  + String

    + :ref:`All strings <all-strings>`
    + :ref:`Concat Empty String <concat-empty-string>`
    + :ref:`Could Be String <could-be-string>`
    + :ref:`Could Be Stringable <could-be-stringable>`
    + :ref:`Could Type With String <could-type-with-string>`
    + :ref:`Could Use str_repeat() <could-use-str\_repeat()>`
    + :ref:`Dollar Curly Interpolation Is Deprecated <dollar-curly-interpolation-is-deprecated>`
    + :ref:`Failed Substr() Comparison <failed-substr()-comparison>`
    + :ref:`Interpolation <interpolation>`
    + :ref:`No String With Append <no-string-with-append>`
    + :ref:`One Variable String <one-variable-string>`
    + :ref:`String <string>`
    + :ref:`Use PHP7 Encapsed Strings <use-php7-encapsed-strings>`
    + :ref:`Use str_contains() <use-str\_contains()>`

  + String Increment

    + :ref:`Plus Plus Used On Strings <plus-plus-used-on-strings>`

  + String Interpolation

    + :ref:`Dollar Curly Interpolation Is Deprecated <dollar-curly-interpolation-is-deprecated>`

  + Stringable

    + :ref:`Could Be Stringable <could-be-stringable>`

  + Stubs Files

    + :ref:`Is Stub Structure <is-stub-structure>`

  + Superglobal Variables

    + :ref:`GPRC Aliases <gprc-aliases>`
    + :ref:`Incoming Variable Index Inventory <incoming-variable-index-inventory>`
    + :ref:`PHP Variables <php-variables>`
    + :ref:`Safe Phpvariables <safe-phpvariables>`
    + :ref:`Super Global Usage <super-global-usage>`
    + :ref:`Super Globals Contagion <super-globals-contagion>`
    + :ref:`Use Web <use-web>`
    + :ref:`Useless Global <useless-global>`

  + Switch

    + :ref:`Could Use Match <could-use-match>`
    + :ref:`Multiple Type Cases In Switch <multiple-type-cases-in-switch>`
    + :ref:`Multiples Identical Case <multiples-identical-case>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`
    + :ref:`Simple Switch And Match <simple-switch-and-match>`
    + :ref:`Strict Comparison With Booleans <strict-comparison-with-booleans>`
    + :ref:`Switch Fallthrough <switch-fallthrough>`
    + :ref:`Switch To Switch <switch-to-switch>`
    + :ref:`Switch With Too Many Default <switch-with-too-many-default>`
    + :ref:`Switch Without Default <switch-without-default>`
    + :ref:`Useless Switch <useless-switch>`

  + Switch Fallthrough

    + :ref:`Switch Fallthrough <switch-fallthrough>`

  + System

    + :ref:`Uses Environment <uses-environment>`

  + System Call

    + :ref:`Shell commands <shell-commands>`

  + Taint Analysis

    + :ref:`Extensions/Exttaint <extensions-exttaint>`

  + Ternary Operator

    + :ref:`Casting Ternary <casting-ternary>`
    + :ref:`Coalesce And Ternary Operators Order <coalesce-and-ternary-operators-order>`
    + :ref:`Could Be Ternary <could-be-ternary>`
    + :ref:`Could Merge Ternary Into Ifthen <could-merge-ternary-into-ifthen>`
    + :ref:`Mismatched Ternary Alternatives <mismatched-ternary-alternatives>`
    + :ref:`Nested Ternary <nested-ternary>`
    + :ref:`Nested Ternary Without Parenthesis <nested-ternary-without-parenthesis>`
    + :ref:`Should Use Ternary Operator <should-use-ternary-operator>`
    + :ref:`Ternary In Concat <ternary-in-concat>`

  + Test

    + :ref:`Test Class <test-class>`

  + Throwable

    + :ref:`Can't Implement Throwable <can't-implement-throwable>`
    + :ref:`Can't Implement Traversable <can't-implement-traversable>`

  + Tick

    + :ref:`Ticks Usage <ticks-usage>`

  + Trailing Comma

    + :ref:`Empty Final Element In Array <empty-final-element-in-array>`
    + :ref:`Signature Trailing Comma <signature-trailing-comma>`
    + :ref:`Trailing Comma In Calls <trailing-comma-in-calls>`
    + :ref:`Use Closure Trailing Comma <use-closure-trailing-comma>`
    + :ref:`Useless Trailing Comma <useless-trailing-comma>`

  + Trait

    + :ref:`Already Parents Trait <already-parents-trait>`
    + :ref:`Calling Static Trait Method <calling-static-trait-method>`
    + :ref:`Cannot Call Static Trait Method Directly <cannot-call-static-trait-method-directly>`
    + :ref:`Collect Class Traits Counts <collect-class-traits-counts>`
    + :ref:`Constants In Traits <constants-in-traits>`
    + :ref:`Could Use Trait <could-use-trait>`
    + :ref:`Dependant Trait <dependant-trait>`
    + :ref:`Empty Traits <empty-traits>`
    + :ref:`Incompatible Property Between Class And Trait <incompatible-property-between-class-and-trait>`
    + :ref:`Is Extension Trait <is-extension-trait>`
    + :ref:`Locally Used Property In Trait <locally-used-property-in-trait>`
    + :ref:`Method Collision Traits <method-collision-traits>`
    + :ref:`Multiple Identical Trait Or Interface <multiple-identical-trait-or-interface>`
    + :ref:`Multiple Usage Of Same Trait <multiple-usage-of-same-trait>`
    + :ref:`No Private Abstract Method In Trait <no-private-abstract-method-in-trait>`
    + :ref:`Redefined PHP Traits <redefined-php-traits>`
    + :ref:`Self Using Trait <self-using-trait>`
    + :ref:`Solve Trait Methods <solve-trait-methods>`
    + :ref:`Trait Methods <trait-methods>`
    + :ref:`Trait Names <trait-names>`
    + :ref:`Trait Not Found <trait-not-found>`
    + :ref:`Traits Usage <traits-usage>`
    + :ref:`Undefined Insteadof <undefined-insteadof>`
    + :ref:`Unused Trait In Class <unused-trait-in-class>`
    + :ref:`Unused Traits <unused-traits>`
    + :ref:`Used Trait <used-trait>`
    + :ref:`Useless Method Alias <useless-method-alias>`

  + Try-catch

    + :ref:`Catch Overwrite Variable <catch-overwrite-variable>`
    + :ref:`Collect Catch Calls <collect-catch-calls>`
    + :ref:`Converted Exceptions <converted-exceptions>`
    + :ref:`Could Use Try <could-use-try>`
    + :ref:`Empty Try Catch <empty-try-catch>`
    + :ref:`Large Try Block <large-try-block>`
    + :ref:`Multiple Catch With Try <multiple-catch-with-try>`
    + :ref:`Multiple Exceptions Catch() <multiple-exceptions-catch()>`
    + :ref:`Throw <throw>`
    + :ref:`Try With Finally <try-with-finally>`
    + :ref:`Try Without Catch <try-without-catch>`
    + :ref:`Uncaught Exceptions <uncaught-exceptions>`
    + :ref:`Unresolved Catch <unresolved-catch>`
    + :ref:`Useless Try <useless-try>`

  + Type Error

    + :ref:`Could Use Try <could-use-try>`

  + Type Juggling

    + :ref:`Implicit Conversion To Int <implicit-conversion-to-int>`
    + :ref:`Use Same Types For Comparisons <use-same-types-for-comparisons>`

  + Type System

    + :ref:`Argument Should Be Typed <argument-should-be-typed>`
    + :ref:`Avoid get_class() <avoid-get\_class()>`
    + :ref:`Bad Type Relay <bad-type-relay>`
    + :ref:`Child Class Removes Type <child-class-removes-type>`
    + :ref:`Could Be Null <could-be-null>`
    + :ref:`Could Be Parent <could-be-parent>`
    + :ref:`Could Inject Parameter <could-inject-parameter>`
    + :ref:`Could Not Type <could-not-type>`
    + :ref:`Could Type <could-type>`
    + :ref:`Could Type With Boolean <could-type-with-boolean>`
    + :ref:`Could Type With Int <could-type-with-int>`
    + :ref:`Exceeding Type <exceeding-type>`
    + :ref:`Extended Types <extended-types>`
    + :ref:`Implicit Nullable Type <implicit-nullable-type>`
    + :ref:`Incompatible Types With Incoming Values <incompatible-types-with-incoming-values>`
    + :ref:`Insufficient Property Type <insufficient-property-type>`
    + :ref:`Insufficient Type <insufficient-type>`
    + :ref:`Intersection Type <intersection-type>`
    + :ref:`Method Signature Must Be Compatible <method-signature-must-be-compatible>`
    + :ref:`Mismatch Parameter And Type <mismatch-parameter-and-type>`
    + :ref:`Mismatch Type And Default <mismatch-type-and-default>`
    + :ref:`Mismatched Default Arguments <mismatched-default-arguments>`
    + :ref:`Mismatched Type <mismatched-type>`
    + :ref:`Missing Type <missing-type>`
    + :ref:`Modified Typed Parameter <modified-typed-parameter>`
    + :ref:`Multiple Type Variable <multiple-type-variable>`
    + :ref:`Never Type Usage <never-type-usage>`
    + :ref:`No Class As Type <no-class-as-type>`
    + :ref:`PHP 8.0 Types <php-8.0-types>`
    + :ref:`Retyped Reference <retyped-reference>`
    + :ref:`Scalar Type Usage <scalar-type-usage>`
    + :ref:`Semantic Typing <semantic-typing>`
    + :ref:`StandaloneType True False Null <standalonetype-true-false-null>`
    + :ref:`Type Could Be Integer <type-could-be-integer>`
    + :ref:`Typed Class Constants Usage <typed-class-constants-usage>`
    + :ref:`Typed Property Usage <typed-property-usage>`
    + :ref:`Typehint Order <typehint-order>`
    + :ref:`Typehinting Stats <typehinting-stats>`
    + :ref:`Typehints/CouldBeResource <typehints-couldberesource>`
    + :ref:`Types <types>`
    + :ref:`Union Type <union-type>`
    + :ref:`Use DNF <use-dnf>`
    + :ref:`Useless Type Casting <useless-type-casting>`
    + :ref:`Useless Type Check <useless-type-check>`
    + :ref:`Variable And Property Type <variable-and-property-type>`
    + :ref:`Weak Typing <weak-typing>`
    + :ref:`Wrong Argument Type <wrong-argument-type>`
    + :ref:`Wrong Typed Name <wrong-typed-name>`

  + TypeError

    + :ref:`Possible TypeError <possible-typeerror>`

  + Typo

    + :ref:`Undefined Constants <undefined-constants>`

  + Undefined

    + :ref:`Undefined Class Constants <undefined-class-constants>`

  + UnexpectedValueException

    + :ref:`Could Use Try <could-use-try>`

  + Unicode

    + :ref:`Unicode Escape Partial <unicode-escape-partial>`
    + :ref:`Unicode Escape Syntax <unicode-escape-syntax>`

  + Union Type

    + :ref:`Intersection Type <intersection-type>`
    + :ref:`Wrong Type With Call <wrong-type-with-call>`

  + Universal Resource Locator (URL)

    + :ref:`Should Use Url Query Functions <should-use-url-query-functions>`
    + :ref:`URL List <url-list>`

  + Unreachable Code

    + :ref:`Unreachable Code <unreachable-code>`

  + Unused

    + :ref:`Unused Functions <unused-functions>`
    + :ref:`Unused Global <unused-global>`
    + :ref:`Unused Private Properties <unused-private-properties>`
    + :ref:`Unused Protected Methods <unused-protected-methods>`
    + :ref:`Used Functions <used-functions>`

  + Use

    + :ref:`Collect Use Counts <collect-use-counts>`
    + :ref:`Constant : With Or Without Use <constant--with-or-without-use>`
    + :ref:`Group Use Declaration <group-use-declaration>`
    + :ref:`Group Use Trailing Comma <group-use-trailing-comma>`
    + :ref:`Hidden Use Expression <hidden-use-expression>`
    + :ref:`Unresolved Use <unresolved-use>`
    + :ref:`Unused Use <unused-use>`
    + :ref:`Used Use <used-use>`

  + Use Alias

    + :ref:`Could Use Alias <could-use-alias>`
    + :ref:`Multiple Alias Definitions <multiple-alias-definitions>`
    + :ref:`Overload Existing Names <overload-existing-names>`
    + :ref:`Should Use Use Function <should-use-use-function>`

  + Validation

    + :ref:`Filter Not Raw <filter-not-raw>`
    + :ref:`Insecure Integer Validation <insecure-integer-validation>`
    + :ref:`No Max On Empty Array <no-max-on-empty-array>`
    + :ref:`Useless Check <useless-check>`
    + :ref:`filter_input() As A Source <filter\_input()-as-a-source>`
    + :ref:`version_compare() Operator <version\_compare()-operator>`

  + Variable Variables

    + :ref:`Variable Variables <variable-variables>`

  + Variables

    + :ref:`All Uppercase Variables <all-uppercase-variables>`
    + :ref:`Assigned Twice <assigned-twice>`
    + :ref:`Collects Variables <collects-variables>`
    + :ref:`Configure Extract <configure-extract>`
    + :ref:`Confusing Names <confusing-names>`
    + :ref:`Constant Typo Looks Like A Variable <constant-typo-looks-like-a-variable>`
    + :ref:`Could Use Compact <could-use-compact>`
    + :ref:`Multiple Type Variable <multiple-type-variable>`
    + :ref:`No Initial S In Variable Names <no-initial-s-in-variable-names>`
    + :ref:`One Variable String <one-variable-string>`
    + :ref:`Only Variable For Reference <only-variable-for-reference>`
    + :ref:`Overwriting Variable <overwriting-variable>`
    + :ref:`Php 8.0 Variable Syntax Tweaks <php-8.0-variable-syntax-tweaks>`
    + :ref:`Property Variable Confusion <property-variable-confusion>`
    + :ref:`Recycled Variables <recycled-variables>`
    + :ref:`Single Use Variables <single-use-variables>`
    + :ref:`Strange Name For Variables <strange-name-for-variables>`
    + :ref:`String May Hold A Variable <string-may-hold-a-variable>`
    + :ref:`Too Many Local Variables <too-many-local-variables>`
    + :ref:`Undefined Variable <undefined-variable>`
    + :ref:`Unused Inherited Variable In Closure <unused-inherited-variable-in-closure>`
    + :ref:`Use get_debug_type() <use-get\_debug\_type()>`
    + :ref:`Variable And Property Type <variable-and-property-type>`
    + :ref:`Variable Variables <variable-variables>`
    + :ref:`Written Only Variables <written-only-variables>`

  + Variadic

    + :ref:`Named Arguments And Variadic <named-arguments-and-variadic>`
    + :ref:`PHP 80 Named Parameter Variadic <php-80-named-parameter-variadic>`
    + :ref:`Spread Operator For Array <spread-operator-for-array>`
    + :ref:`array_merge() And Variadic <array\_merge()-and-variadic>`

  + Virtual Machine

    + :ref:`Always Use Function With array_key_exists() <always-use-function-with-array\_key\_exists()>`

  + Virtual Property

    + :ref:`Has Virtual Property <has-virtual-property>`

  + Visibility

    + :ref:`Access Protected Structures <access-protected-structures>`
    + :ref:`Ambiguous Visibilities <ambiguous-visibilities>`
    + :ref:`Can't Instantiate Class <can't-instantiate-class>`
    + :ref:`Class Overreach <class-overreach>`
    + :ref:`Could Be Class Constant <could-be-class-constant>`
    + :ref:`Could Be Private Class Constant <could-be-private-class-constant>`
    + :ref:`Could Be Protected Class Constant <could-be-protected-class-constant>`
    + :ref:`Could Be Protected Method <could-be-protected-method>`
    + :ref:`Could Be Protected Property <could-be-protected-property>`
    + :ref:`Forgotten Visibility <forgotten-visibility>`
    + :ref:`Implemented Methods Must Be Public <implemented-methods-must-be-public>`
    + :ref:`Inherited Class Constant Visibility <inherited-class-constant-visibility>`
    + :ref:`Lowered Access Level <lowered-access-level>`
    + :ref:`Magic Visibility <magic-visibility>`
    + :ref:`Missing Visibility <missing-visibility>`
    + :ref:`No Public Access <no-public-access>`
    + :ref:`Property Could Be Private <property-could-be-private>`
    + :ref:`Public Reach To Private Methods <public-reach-to-private-methods>`
    + :ref:`Raised Access Level <raised-access-level>`
    + :ref:`Unused Private Methods <unused-private-methods>`
    + :ref:`Used Protected Method <used-protected-method>`
    + :ref:`Var Keyword <var-keyword>`

  + Void

    + :ref:`Could Be Void <could-be-void>`
    + :ref:`Don't Collect Void <don't-collect-void>`
    + :ref:`Must Use Result, So It Returns <must-use-result,-so-it-returns>`
    + :ref:`No Referenced Void <no-referenced-void>`
    + :ref:`Return void  <return-void->`

  + While

    + :ref:`Cache Variable Outside Loop <cache-variable-outside-loop>`
    + :ref:`Collect Block Size <collect-block-size>`
    + :ref:`PHP Alternative Syntax <php-alternative-syntax>`
    + :ref:`While(List() = Each()) <while(list()-=-each())>`

  + Whitespace

    + :ref:`Forgotten Whitespace <forgotten-whitespace>`

  + World Wide Weab (WWW)

    + :ref:`Use Web <use-web>`

  + XXTEA

    + :ref:`ext/xxtea <ext-xxtea>`

  + Yield

    + :ref:`Can't Call Generator <can't-call-generator>`
    + :ref:`Could Be Generator <could-be-generator>`
    + :ref:`Don't Loop On Yield <don't-loop-on-yield>`
    + :ref:`Method Is A Generator <method-is-a-generator>`
    + :ref:`No Return For Generator <no-return-for-generator>`
    + :ref:`Should Yield With Key <should-yield-with-key>`
    + :ref:`Yield From Usage <yield-from-usage>`
    + :ref:`Yield Usage <yield-usage>`

  + __halt_compiler()

    + :ref:`__halt_compiler <\_\_halt\_compiler>`

  + basename

    + :ref:`Use Basename Suffix <use-basename-suffix>`

  + browscap

    + :ref:`Use Browscap <use-browscap>`

  + compact()

    + :ref:`Create Compact Variables <create-compact-variables>`
    + :ref:`Nonexistent Variable In compact() <nonexistent-variable-in-compact()>`

  + constructor

    + :ref:`Avoid option arrays in constructors <avoid-option-arrays-in-constructors>`
    + :ref:`Can't Instantiate Class <can't-instantiate-class>`
    + :ref:`Constructors <constructors>`
    + :ref:`Don't Send $this In Constructor <don't-send-$this-in-constructor>`
    + :ref:`Old Style Constructor <old-style-constructor>`
    + :ref:`Unfinished Object <unfinished-object>`
    + :ref:`Useless Constructor <useless-constructor>`
    + :ref:`Wrong Number Of Arguments <wrong-number-of-arguments>`

  + count()

    + :ref:`Count() Is Not Negative <count()-is-not-negative>`
    + :ref:`No Count With 0 <no-count-with-0>`

  + crc32

    + :ref:`Crc32() Might Be Negative <crc32()-might-be-negative>`

  + declare()

    + :ref:`Declare strict_types Usage <declare-strict\_types-usage>`
    + :ref:`Encoding Usage <encoding-usage>`
    + :ref:`Multiple Declaration Of Strict_types <multiple-declaration-of-strict\_types>`
    + :ref:`Substring First <substring-first>`
    + :ref:`Ticks Usage <ticks-usage>`
    + :ref:`time() Vs strtotime() <time()-vs-strtotime()>`

  + define()

    + :ref:`Const Or Define Preference <const-or-define-preference>`
    + :ref:`Define Constants With Array <define-constants-with-array>`
    + :ref:`Use const <use-const>`

  + dirname

    + :ref:`Use Basename Suffix <use-basename-suffix>`

  + extends

    + :ref:`Classes Mutually Extending Each Other <classes-mutually-extending-each-other>`
    + :ref:`Cyclic References <cyclic-references>`

  + extract()

    + :ref:`Configure Extract <configure-extract>`

  + glob()

    + :ref:`Avoid glob() Usage <avoid-glob()-usage>`
    + :ref:`GLOB_BRACE Usage <glob\_brace-usage>`

  + global Scope

    + :ref:`$GLOBALS Or global <$globals-or-global>`
    + :ref:`Collect Global Variables <collect-global-variables>`
    + :ref:`Global Definitions <global-definitions>`
    + :ref:`Global In Global <global-in-global>`
    + :ref:`Global Usage <global-usage>`
    + :ref:`Globals <globals>`
    + :ref:`Implicit Global <implicit-global>`
    + :ref:`Local Globals <local-globals>`
    + :ref:`PHP Variables <php-variables>`
    + :ref:`PHP5 Indirect Variable Expression <php5-indirect-variable-expression>`
    + :ref:`Restrict Global Usage <restrict-global-usage>`
    + :ref:`Simple Global Variable <simple-global-variable>`
    + :ref:`Static Global Variables Confusion <static-global-variables-confusion>`
    + :ref:`Unused Global <unused-global>`
    + :ref:`Variable Global <variable-global>`

  + implements

    + :ref:`Abstract Or Implements <abstract-or-implements>`
    + :ref:`Already Parents Interface <already-parents-interface>`
    + :ref:`Implements Is For Interface <implements-is-for-interface>`
    + :ref:`Interfaces Is Not Implemented <interfaces-is-not-implemented>`

  + include

    + :ref:`Include Variables <include-variables>`
    + :ref:`Missing Include <missing-include>`
    + :ref:`No Parenthesis For Language Construct <no-parenthesis-for-language-construct>`
    + :ref:`Static Inclusions <static-inclusions>`
    + :ref:`include_once() Usage <include\_once()-usage>`
    + :ref:`include_once() Usage <include\_once()-usage>`

  + instanceof

    + :ref:`Unresolved Instanceof <unresolved-instanceof>`
    + :ref:`Use Instanceof <use-instanceof>`
    + :ref:`is_a() Versus instanceof <is\_a()-versus-instanceof>`

  + integer

    + :ref:`Binary Glossary <binary-glossary>`
    + :ref:`Could Type With Int <could-type-with-int>`
    + :ref:`Do Not Cast To Int <do-not-cast-to-int>`
    + :ref:`Null Or Boolean Arrays <null-or-boolean-arrays>`
    + :ref:`Octal Glossary <octal-glossary>`
    + :ref:`Similar Integers <similar-integers>`
    + :ref:`Special Integers <special-integers>`
    + :ref:`Type Could Be Integer <type-could-be-integer>`

  + libsodium

    + :ref:`ext/mcrypt <ext-mcrypt>`

  + mcrypt Extension

    + :ref:`mcrypt_create_iv() With Default Values <mcrypt\_create\_iv()-with-default-values>`

  + mysqli_sql_exception

    + :ref:`Could Use Try <could-use-try>`

  + negative-index

    + :ref:`No Substr Minus One <no-substr-minus-one>`

  + new

    + :ref:`Clone Constant <clone-constant>`
    + :ref:`Dynamic New <dynamic-new>`
    + :ref:`Maybe Missing New <maybe-missing-new>`
    + :ref:`Methodcall On New <methodcall-on-new>`
    + :ref:`New On Functioncall Or Identifier <new-on-functioncall-or-identifier>`
    + :ref:`New Order <new-order>`
    + :ref:`Null On New <null-on-new>`

  + pack

    + :ref:`Invalid Pack Format <invalid-pack-format>`
    + :ref:`Pack Format Inventory <pack-format-inventory>`

  + parent

    + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
    + :ref:`Class Without Parent <class-without-parent>`
    + :ref:`Could Be Parent Method <could-be-parent-method>`
    + :ref:`Defined Parent MP <defined-parent-mp>`
    + :ref:`Must Call Parent Constructor <must-call-parent-constructor>`
    + :ref:`Parent First <parent-first>`
    + :ref:`Parent Is Not Static <parent-is-not-static>`
    + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
    + :ref:`Set Parent Definition <set-parent-definition>`
    + :ref:`Undefined Parent <undefined-parent>`
    + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
    + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`

  + phpinfo()

    + :ref:`Phpinfo <phpinfo>`

  + plus +

    + :ref:`Unsupported Operand Types <unsupported-operand-types>`

  + resource

    + :ref:`PHP 8.0 Resources Turned Into Objects <php-8.0-resources-turned-into-objects>`
    + :ref:`PHP 8.1 Resources Turned Into Objects <php-8.1-resources-turned-into-objects>`
    + :ref:`Resources Usage <resources-usage>`
    + :ref:`Typehints/CouldBeResource <typehints-couldberesource>`
    + :ref:`Unchecked Resources <unchecked-resources>`

  + sleep

    + :ref:`Avoid sleep()/usleep() <avoid-sleep()-usleep()>`

  + sprintf

    + :ref:`Printf Format Inventory <printf-format-inventory>`
    + :ref:`Sprintf Format Compilation <sprintf-format-compilation>`

  + static

    + :ref:`$this Belongs To Classes Or Traits <$this-belongs-to-classes-or-traits>`
    + :ref:`$this Is Not For Static Methods <$this-is-not-for-static-methods>`
    + :ref:`Ambiguous Static <ambiguous-static>`
    + :ref:`Cannot Use Static For Closure <cannot-use-static-for-closure>`
    + :ref:`Could Be A Static Variable <could-be-a-static-variable>`
    + :ref:`Declare Static Once <declare-static-once>`
    + :ref:`Make All Statics <make-all-statics>`
    + :ref:`Method Could Be Static <method-could-be-static>`
    + :ref:`Non Static Methods Called In A Static <non-static-methods-called-in-a-static>`
    + :ref:`Only Static Methods Class <only-static-methods-class>`
    + :ref:`Parent Is Not Static <parent-is-not-static>`
    + :ref:`Parent, Static Or Self Outside Class <parent,-static-or-self-outside-class>`
    + :ref:`Scope Resolution Operator <scope-resolution-operator>`
    + :ref:`Static Call May Be Truly Static <static-call-may-be-truly-static>`
    + :ref:`Static Call With Self <static-call-with-self>`
    + :ref:`Static Global Variables Confusion <static-global-variables-confusion>`
    + :ref:`Static Methods <static-methods>`
    + :ref:`Static Methods Called From Object <static-methods-called-from-object>`
    + :ref:`Static Methods Can't Contain $this <static-methods-can't-contain-$this>`
    + :ref:`Undefined static\:\: Or self\:\: <undefined-static-or-self>`
    + :ref:`Use Lower Case For Parent, Static And Self <use-lower-case-for-parent,-static-and-self>`
    + :ref:`Use This <use-this>`
    + :ref:`Used Static Properties <used-static-properties>`
    + :ref:`self, parent, static Outside Class <self,-parent,-static-outside-class>`

  + stdclass

    + :ref:`Avoid Using stdClass <avoid-using-stdclass>`
    + :ref:`Checks Property Existence <checks-property-existence>`
    + :ref:`Extends stdClass <extends-stdclass>`

  + strict_types

    + :ref:`Multiple Declaration Of Strict_types <multiple-declaration-of-strict\_types>`
    + :ref:`strict_types Preference <strict\_types-preference>`

  + throw

    + :ref:`Forgotten Thrown <forgotten-thrown>`
    + :ref:`Long Preparation For Throw <long-preparation-for-throw>`
    + :ref:`Throw In Destruct <throw-in-destruct>`
    + :ref:`Throw Was An Expression <throw-was-an-expression>`
    + :ref:`Thrown Exceptions <thrown-exceptions>`
    + :ref:`Throws An Assignement <throws-an-assignement>`

  + unset()

    + :ref:`Cast Unset Usage <cast-unset-usage>`
    + :ref:`Multiple Unset() <multiple-unset()>`
    + :ref:`Unset() Or (unset) <unset()-or-(unset)>`
    + :ref:`Useless Unset <useless-unset>`

  + yield from Keyword

    + :ref:`Can't Call Generator <can't-call-generator>`
    + :ref:`Could Be Generator <could-be-generator>`
    + :ref:`Could Use Yield From <could-use-yield-from>`
    + :ref:`Method Is A Generator <method-is-a-generator>`
    + :ref:`Misused Yield <misused-yield>`
    + :ref:`Yield From Usage <yield-from-usage>`
    + :ref:`Yield Usage <yield-usage>`




Directory by PHP Error message
------------------------------

Exakat helps reduce the amount of error and warning that code is producing by reporting pattern that are likely to emit errors.

263 PHP error message detailled : 

* :ref:`"static\:\:"-is-not-allowed-in-compile-time-constants <avoid-self-in-interface>`
* :ref:`$globals-can-only-be-modified-using-the-$globals[$name]-=-$value-syntax <restrict-global-usage>`
* :ref:`%s"-will-be-interpreted-as-a-class-name.-did-you-mean-"%s"?-write-"%s"%s-to-suppress-this-warning <not-a-scalar-type>`
* :ref:`%s"-will-be-interpreted-as-a-class-name.-did-you-mean-"%s"?-write-"%s"%s-to-suppress-this-warning <not-a-scalar-type>`
* :ref:`%s"-will-be-interpreted-as-a-class-name.-did-you-mean-"%s"?-write-"%s"%s-to-suppress-this-warning <not-a-scalar-type>`
* :ref:`%s%s%s():-argument-#%d%s%s%s-must-be-passed-by-reference,-value-given <array\_map()-passes-by-value>`
* :ref:`%s%s%s():-argument-#%d%s%s%s-must-be-passed-by-reference,-value-given <no-literal-for-reference>`
* :ref:`%s%s%s():-argument-#%d%s%s%s-must-be-passed-by-reference,-value-given <no-literal-for-reference>`
* :ref:`%s%s%s():-return-value-must-be-of-type-%s,-%s-returned <missing-some-returntype>`
* :ref:`%s'-is-not-a-valid-mode-for-fopen <wrong-fopen()-mode>`
* :ref:`%s()-argument-#%d%s%s%s-cannot-be-passed-by-reference <only-variable-passed-by-reference>`
* :ref:`%s()-expects-exactly-0-arguments,-%d-given <wrong-number-of-arguments>`
* :ref:`%s()-has-been-disabled-for-security-reasons <can't-disable-class>`
* :ref:`%s():-argument-#%d%s%s%s-cannot-be-passed-by-reference <only-variable-passed-by-reference>`
* :ref:`%s():-argument-#%d%s%s%s-could-not-be-passed-by-reference <only-variable-passed-by-reference>`
* :ref:`%s():-implicitly-marking-parameter-$%s-as-nullable-is-deprecated,-the-explicit-nullable-type-must-be-used-instead <implicit-nullable-type>`
* :ref:`%s():-passing-null-to-parameter-#% <no-null-for-native-php-functions>`
* :ref:`%s-%s-cannot-implement-interface-%s,-extend-exception-or-error-instead <can't-implement-throwable>`
* :ref:`%s-%s-inherits-both-%s\:\:%s-and-%s\:\:%s <overwritten-class-constants>`
* :ref:`%s-%s-must-implement-interface-%s-as-part-of-either-%s-or-%s <can't-implement-traversable>`
* :ref:`%s-and-%s-define-the-same-constant-(%s)-in-the-composition-of-%s.-however,-the-definition-differs-and-is-considered-incompatible.-class-was-composed <incompatible-property-between-class-and-trait>`
* :ref:`%s-cannot-implement-%s---it-is-not-an-interface <implements-is-for-interface>`
* :ref:`%s-function-%s\:\:%s()-cannot-be-declared-private <no-private-abstract-method-in-trait>`
* :ref:`%s\:\:%s():-return-type-must-be-%s-when-declared <magic-method-returntype-is-restricted>`
* :ref:`%s\:\:%s-cannot-override-final-constant-%s\:\:%s <can't-overwrite-final-constant>`
* :ref:`%s\:\:%s-cannot-override-final-constant-%s\:\:%s <rewrote-final-class-constant>`
* :ref:`'%s'-operator-accepts-only-positive-integers <break-with-0>`
* :ref:`__autoload()-is-deprecated,-use-spl_autoload_register()-instead <old-style-\_\_autoload()>`
* :ref:`__autoload()-is-no-longer-supported,-use-spl_autoload_register()-instead <old-style-\_\_autoload()>`
* :ref:`__clone-method-called-on-non-object <clone-constant>`
* :ref:`__clone-method-called-on-non-object <clone-with-non-object>`
* :ref:`a-function-with-return-type-must-return-a-value <type-must-be-returned>`
* :ref:`a-never-returning-%s-must-not-return <type-must-be-returned>`
* :ref:`access-level-to-%s\:\:%s-must-be-%s-(as-in-%s-%s)%s <implemented-methods-must-be-public>`
* :ref:`access-level-to-%s\:\:%s-must-be-%s-(as-in-%s-%s)%s <raised-access-level>`
* :ref:`access-level-to-%s\:\:%s-must-be-%s-(as-in-%s-%s)%s <redefined-property>`
* :ref:`access-to-undeclared-static-property-%s\:\:$%s <undefined-static-or-self>`
* :ref:`access-to-undeclared-static-property-%s\:\:$%s <wrong-access-style-to-property>`
* :ref:`accessing-static-property-%s\:\:$%s-as-non-static <wrong-access-style-to-property>`
* :ref:`an-alias-was-defined-for-%s\:\:%s-but-this-method-does-not-exist <undefined-insteadof>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <mismatch-type-and-default>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <undefined-interfaces>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <wrong-argument-type>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <wrong-parameter-type>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <wrong-type-for-native-php-function>`
* :ref:`argument-#%d-($%s)-must-be-of-type-%s,-%s-given <wrong-type-with-call>`
* :ref:`array-and-string-offset-access-syntax-with-curly-braces-is-deprecated <curly-bracketed-arrays-are-not-supported>`
* :ref:`array-and-string-offset-access-syntax-with-curly-braces-is-no-longer-supported <curly-bracketed-arrays-are-not-supported>`
* :ref:`array-to-string-conversion <invalid-cast>`
* :ref:`array_merge()-does-not-accept-unknown-named-parameters <no-spread-for-hash>`
* :ref:`array_merge()-does-not-accept-unknown-named-parameters <unknown-parameter-name>`
* :ref:`array_merge()-expects-at-least-1-parameter,-0-given <array\_merge()-and-variadic>`
* :ref:`attempt-to-read-property-"%s"-on-%s <could-use-null-safe-object-operator>`
* :ref:`attribute-"%s"-cannot-target-%s-(allowed-targets:-%s) <wrong-attribute-configuration>`
* :ref:`break-operator-accepts-only-positive-integers <break-with-non-integer>`
* :ref:`call-to-%s-method-%s\:\:%s()-from-%s%s <access-protected-structures>`
* :ref:`call-to-%s-method-%s\:\:%s()-from-%s%s <can't-instantiate-class>`
* :ref:`call-to-a-member-function-%s()-on-%s <could-use-null-safe-object-operator>`
* :ref:`call-to-a-member-function-%s()-on-%s <use-nullsafe-operator>`
* :ref:`call-to-undefined-function <throw-functioncall>`
* :ref:`call-to-undefined-function-%s() <throw-functioncall>`
* :ref:`call-to-undefined-function-%s() <undefined-functions>`
* :ref:`call-to-undefined-method-%s\:\:%s() <undefined-parent>`
* :ref:`call-to-undefined-method-%s\:\:%s() <undefined-static-or-self>`
* :ref:`calling-static-trait-method-%s\:\:%s-is-deprecated <calling-static-trait-method>`
* :ref:`calling-static-trait-method-%s\:\:%s-is-deprecated <cannot-call-static-trait-method-directly>`
* :ref:`can't-inherit-abstract-function-%s\:\:%s()-(previously-declared-abstract-in-%s) <cant-inherit-abstract-method>`
* :ref:`cannot-%s-readonly-property-%s\:\:$%s-from-%s%s <no-readonly-assignation-in-global>`
* :ref:`cannot-%s-readonly-property-%s\:\:$%s-from-%s%s <no-readonly-assignation-in-global>`
* :ref:`cannot-access-%s-constant-%s\:\:%s <access-protected-structures>`
* :ref:`cannot-access-%s-constant-%s\:\:%s <unreachable-class-constant>`
* :ref:`cannot-access-%s-property-%s\:\:$%s <access-protected-structures>`
* :ref:`cannot-access-offset-of-type-%s-on-%s <no-object-as-index>`
* :ref:`cannot-access-parent\:\:-when-current-class-scope-has-no-parent <avoid-self-in-interface>`
* :ref:`cannot-access-parent\:\:-when-current-class-scope-has-no-parent <class-without-parent>`
* :ref:`cannot-access-parent\:\:-when-current-class-scope-has-no-parent <undefined-parent>`
* :ref:`cannot-access-parent\:\:-when-no-class-scope-is-active <class-without-parent>`
* :ref:`cannot-access-parent\:\:-when-no-class-scope-is-active <parent,-static-or-self-outside-class>`
* :ref:`cannot-access-self\:\:-when-no-class-scope-is-active <parent,-static-or-self-outside-class>`
* :ref:`cannot-access-static\:\:-when-no-class-scope-is-active <self,-parent,-static-outside-class>`
* :ref:`cannot-assign-%s-to-property-%s\:\:$%s-of-type-%s <wrong-type-with-default>`
* :ref:`cannot-auto-initialize-an-array-inside-property-%s\:\:$%s-of-type-%s <false-to-array-conversion>`
* :ref:`cannot-bind-an-instance-to-a-static-closure <cannot-use-static-for-closure>`
* :ref:`cannot-call-constructor <useless-constructor>`
* :ref:`cannot-combine-named-arguments-and-argument-unpacking <named-arguments-and-variadic>`
* :ref:`cannot-inherit-previously-inherited-or-override-constant-%s-from-interface-%s <can't-overload-constants>`
* :ref:`cannot-inherit-previously-inherited-or-override-constant-%s-from-interface-%s <inherited-class-constant-visibility>`
* :ref:`cannot-inherit-previously-inherited-or-override-constant-%s-from-interface-%s <overwritten-class-constants>`
* :ref:`cannot-instantiate-enum-%s <cant-instantiate-non-class>`
* :ref:`cannot-instantiate-interface-%s <cant-instantiate-non-class>`
* :ref:`cannot-instantiate-trait-%s <cant-instantiate-non-class>`
* :ref:`cannot-override-final-%s\:\:%s()-with-%s\:\:%s() <can't-overwrite-final-method>`
* :ref:`cannot-override-final-%s\:\:%s()-with-%s\:\:%s() <final-class-usage>`
* :ref:`cannot-override-final-%s\:\:%s()-with-%s\:\:%s() <final-methods-usage>`
* :ref:`cannot-pass-parameter-%d-by-reference <only-variable-for-reference>`
* :ref:`cannot-perform-bitwise-not-on-%s <unsupported-types-with-operators>`
* :ref:`cannot-perform-bitwise-not-on-%s <unsupported-types-with-operators>`
* :ref:`cannot-perform-bitwise-not-on-%s <unsupported-types-with-operators>`
* :ref:`cannot-perform-bitwise-not-on-%s <unsupported-types-with-operators>`
* :ref:`cannot-re-assign-$this <don't-change-incomings>`
* :ref:`cannot-re-assign-auto-global-variable-%s <don't-change-incomings>`
* :ref:`cannot-unpack-array-with-string-keys <no-spread-for-hash>`
* :ref:`cannot-use-%s-as-default-value-for-parameter-$%s-of-type-%s <wrong-typed-property-default>`
* :ref:`cannot-use-%s-as-default-value-for-property-%s\:\:$%s-of-type-%s <wrong-typed-property-default>`
* :ref:`cannot-use-'final'-as-constant-modifier <final-constant>`
* :ref:`cannot-use-'mixed'-as-class-name-as-it-is-reserved <the-mixed-keyword>`
* :ref:`cannot-use-'never'-as-class-name-as-it-is-reserved <never-keyword>`
* :ref:`cannot-use-[]-for-reading <cannot-use-append-for-reading>`
* :ref:`cannot-use-a-scalar-value-as-an-array <array-with-string-initialization>`
* :ref:`cannot-use-isset()-on-the-result-of-an-expression-(you-can-use-"null-!==-expression"-instead) <isset()-with-constants>`
* :ref:`cannot-use-isset()-on-the-result-of-an-expression-(you-can-use-"null-!==-expression"-instead) <only-variable-passed-by-reference>`
* :ref:`cannot-use-lexical-variable-%s-as-a-parameter-name <multiple-definition-of-the-same-argument>`
* :ref:`cannot-use-object-of-type-%s-as-array <$this-is-not-an-array>`
* :ref:`cannot-use-positional-argument-after-argument-unpacking <named-arguments-and-variadic>`
* :ref:`class-"%s"-not-found <undefined-static-class>`
* :ref:`class-%s-cannot-extend-%s-%s <can't-extend-final-class>`
* :ref:`class-%s-cannot-implement-previously-implemented-interface-%s <multiple-identical-trait-or-interface>`
* :ref:`class-%s-cannot-implement-previously-implemented-interface-%s <repeated-interface>`
* :ref:`class-%s-contains-%d-abstract-method%s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods <abstract-or-implements>`
* :ref:`class-%s-contains-%d-abstract-method%s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods <interfaces-is-not-implemented>`
* :ref:`class-%s-contains-%d-abstract-method%s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods <missing-abstract-method>`
* :ref:`class-%s-must-implement-interface-%s-as-part-of-either-%s-or-%s <can't-implement-traversable>`
* :ref:`constant-%s-is-deprecated <php-8.1-removed-constants>`
* :ref:`constant-expression-contains-invalid-operations <class-const-with-array>`
* :ref:`constant-expression-contains-invalid-operations <nested-attributes>`
* :ref:`constant-expression-contains-invalid-operations <new-initializers>`
* :ref:`continue"-targeting-switch-is-equivalent-to-"break <continue-is-for-loop>`
* :ref:`could-not-check-compatibility-between-%s-and-%s,-because-class-%s-is-not-available <incompatible-signature-methods-with-covariance>`
* :ref:`declaration-of-%s-must-be-compatible-with-%s <immutable-signature>`
* :ref:`declaration-of-%s-must-be-compatible-with-%s <incompatible-signature-methods-with-covariance>`
* :ref:`declaration-of-%s-must-be-compatible-with-%s <incompatible-signature-methods>`
* :ref:`declaration-of-%s-must-be-compatible-with-%s <method-signature-must-be-compatible>`
* :ref:`default-value-for-parameters-with-a-%s-type-can-only-be-%s-or-null <mismatch-type-and-default>`
* :ref:`define():-argument-#3-($case_insensitive)-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported <case-insensitive-constants>`
* :ref:`define():-argument-#3-($case_insensitive)-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported <constant-case-preference>`
* :ref:`define():-argument-#3-($case_insensitive)-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported <constant-case-preference>`
* :ref:`define():-declaration-of-case-insensitive-constants-is-deprecated <case-insensitive-constants>`
* :ref:`defining-a-custom-assert()-function-is-not-allowed, <assert-function-is-reserved>`
* :ref:`duplicate-type-%s-is-redundant <duplicate-enum-case-value>`
* :ref:`empty-delimiter <no-empty-string-with-explode()>`
* :ref:`empty-delimiter <no-empty-string-with-explode()>`
* :ref:`enum-"%s"-not-found <undefined-static-class>`
* :ref:`enum-%s-cannot-include-magic-method-%s <no-magic-method-for-enum>`
* :ref:`enum-%s-cannot-include-magic-method-%s <no-magic-method-for-enum>`
* :ref:`foreach()-argument-must-be-of-type-array|object <no-direct-usage-of-returned-value>`
* :ref:`generators-cannot-return-values-using-"return" <no-return-for-generator>`
* :ref:`handling-base64-via-mbstring-is-deprecated;-use-base64_encode-base64_decode-instead <deprecated-mb\_string-encodings>`
* :ref:`handling-html-entities-via-mbstring-is-deprecated;-use-htmlspecialchars,-htmlentities,-or-mb_encode_numericentity-mb_decode_numericentity <deprecated-mb\_string-encodings>`
* :ref:`handling-qprint-via-mbstring-is-deprecated;-use-quoted_printable_encode-quoted_printable_decode <deprecated-mb\_string-encodings>`
* :ref:`handling-uuencode-via-mbstring-is-deprecated;-use-convert_uuencode-convert_uudecode-instead <deprecated-mb\_string-encodings>`
* :ref:`illegal-offset-type <indices-are-int-or-string>`
* :ref:`illegal-offset-type <no-object-as-index>`
* :ref:`illegal-offset-type-in-isset-or-empty <no-object-as-index>`
* :ref:`implicit-conversion-from-float-string-"%s"-to-int-loses <float-conversion-as-index>`
* :ref:`implicit-conversion-from-float-string-"%s"-to-int-loses <implicit-conversion-to-int>`
* :ref:`index-invalid-or-out-of-range <no-object-as-index>`
* :ref:`indirect-modification-of-overloaded-property-%s\:\:$%s-has-no-effect <no-magic-method-with-array>`
* :ref:`interface-"%s"-not-found <undefined-static-class>`
* :ref:`invalid-numeric-literal <malformed-octal>`
* :ref:`invalid-utf-8-codepoint-escape <unicode-escape-syntax>`
* :ref:`invalid-utf-8-codepoint-escape:-codepoint-too-large <unicode-escape-syntax>`
* :ref:`method-name-must-be-a-string <useless-type>`
* :ref:`methods-with-the-same-name-as-their-class-will-not-be-constructors-in-a-future-version-of-php;-%s-has-a-deprecated-constructor <old-style-constructor>`
* :ref:`must-be-a-user-defined-class-name,-internal-class-name-given <class\_alias()-supports-internal-classes>`
* :ref:`must-be-a-valid-comparison-operator <version\_compare()-operator>`
* :ref:`must-be-a-valid-encoding,-"%s"-given <mbstring-unknown-encodings>`
* :ref:`must-be-one-of-pgsql_assoc,-pgsql_num,-or-pgsql_both <use-constant-as-arguments>`
* :ref:`must-be-one-of-pgsql_notice_last,-pgsql_notice_all,-or-pgsql_notice_clear <use-constant-as-arguments>`
* :ref:`must-contain-at-least-one-element <no-max-on-empty-array>`
* :ref:`named-parameter-$x-overwrites-previous-argument <duplicate-named-parameter>`
* :ref:`needle-is-not-a-string-or-an-integer <strpos()-with-integers>`
* :ref:`no-ending-delimiter-'%c'-found <regex-inventory>`
* :ref:`non-static-method-%s\:\:%s()-cannot-be-called-statically <non-static-methods-called-in-a-static>`
* :ref:`non-static-method-%s\:\:%s()-cannot-be-called-statically <static-methods-cannot-call-non-static-methods>`
* :ref:`non-static-method-%s\:\:%s()-should-not-be-called-statically <non-static-methods-called-in-a-static>`
* :ref:`non-string-needles-will-be-interpreted-as-strings-in-the-future.-use-an-explicit-chr()-call-to-preserve-the-current-behavior <strpos()-with-integers>`
* :ref:`object-of-class-%s-could-not-be-converted-to-float <invalid-cast>`
* :ref:`object-of-class-%s-could-not-be-converted-to-float <no-a-valid-cast>`
* :ref:`object-of-class-%s-could-not-be-converted-to-int <invalid-cast>`
* :ref:`object-of-class-%s-could-not-be-converted-to-int <no-a-valid-cast>`
* :ref:`object-of-class-%s-could-not-be-converted-to-string <no-a-valid-cast>`
* :ref:`octal-escape-sequence-overflow-\\%s-is-greater-than-\\377 <invalid-octal-in-string>`
* :ref:`only-the-first-byte-will-be-assigned-to-the-string-offset <only-first-byte-will-be-assigned>`
* :ref:`only-variable-references-should-be-returned-by-reference <no-literal-for-reference>`
* :ref:`only-variable-references-should-be-returned-by-reference <no-reference-for-ternary>`
* :ref:`only-variables-can-be-passed-by-reference <only-variable-for-reference>`
* :ref:`only-variables-should-be-passed-by-reference <class-typed-references>`
* :ref:`only-variables-should-be-passed-by-reference <only-variable-for-reference>`
* :ref:`only-variables-should-be-passed-by-reference <parenthesis-as-parameter>`
* :ref:`optional-parameter-$%s-declared-before-required-parameter-$%s-is-implicitly-treated-as-a-required-parameter <wrong-optional-parameter>`
* :ref:`private-constant-%s\:\:%s-cannot-be-final-as-it-is-not-visible-to-other-classes <final-constant>`
* :ref:`private-methods-cannot-be-final-as-they-are-never-overridden-by-other-classes <final-private-methods>`
* :ref:`property-%s-does-not-exist <undefined-properties>`
* :ref:`property-%s\:\:$%s-cannot-have-type-%s <could-be-callable>`
* :ref:`redefinition-of-parameter-$%s <multiple-definition-of-the-same-argument>`
* :ref:`required-parameter-$%s-follows-optional-parameter-$%s <wrong-optional-parameter>`
* :ref:`return-type-of-%s\:\:%s()-should-either-be-compatible-with-%s\:\:%s():-mixed <php-native-class-type-compatibility>`
* :ref:`return-type-of-%s\:\:%s()-should-either-be-compatible-with-%s\:\:%s():-mixed <php-native-interfaces-and-return-type>`
* :ref:`returning-by-reference-from-a-void-function-is-deprecated <no-referenced-void>`
* :ref:`syntax-error,-unexpected-',' <reserved-match-keyword>`
* :ref:`syntax-error,-unexpected-'-',-expecting-'=' <invalid-constant-name>`
* :ref:`syntax-error,-unexpected-'|',-expecting-variable-(t_variable) <union-type>`
* :ref:`syntax-error,-unexpected-token-"&" <calltime-pass-by-reference>`
* :ref:`syntax-error,-unexpected-token-"match" <reserved-match-keyword>`
* :ref:`the-(real)-cast-has-been-removed,-use-(float)-instead <avoid-real>`
* :ref:`the-(real)-cast-is-deprecated,-use-(float)-instead <avoid-real>`
* :ref:`the-(unset)-cast-is-deprecated <cast-unset-usage>`
* :ref:`the-(unset)-cast-is-no-longer-supported <cast-unset-usage>`
* :ref:`the-behavior-of-unparenthesized-expressions-containing-both-'.'-and-'+'-'-'-will-change-in-php-8:-'+'-'-'-will-take-a-higher-precedence <concat-and-addition>`
* :ref:`the-behavior-of-unparenthesized-expressions-containing-both-'.'-and-'>>'-'<<'-will-change-in-php-8:-'<<'-'>>'-will-take-a-higher-precedence <concat-and-addition>`
* :ref:`the-each()-function-is-deprecated.-this-message-will-be-suppressed-on-further-calls <php-7.2-removed-functions>`
* :ref:`the-magic-method-%s\:\:%s()-must-have-public-visibility <magic-visibility>`
* :ref:`the-magic-method-%s\:\:%s()-must-have-public-visibility <magic-visibility>`
* :ref:`the-magic-method-%s\:\:%s()-must-have-public-visibility <magic-visibility>`
* :ref:`the-magic-method-%s\:\:%s()-must-have-public-visibility <magic-visibility>`
* :ref:`the-parent-constructor-was-not-called:-the-object-is-in-an-invalid-state <must-call-parent-constructor>`
* :ref:`too-few-arguments-to-function-%s%s%s(),-%d-passed-and-%s-%d <wrong-number-of-arguments-in-methods>`
* :ref:`too-few-arguments-to-function-%s%s%s(),-%d-passed-and-%s-%d-expected <wrong-number-of-arguments>`
* :ref:`trait-"%s"-not-found <undefined-static-class>`
* :ref:`trait-"%s"-not-found <undefined-trait>`
* :ref:`trait-method-%s\:\:%s-has-not-been-applied-as-%s\:\:%s <method-collision-traits>`
* :ref:`trait-method-%s\:\:%s-has-not-been-applied-as-%s\:\:%s <useless-method-alias>`
* :ref:`trying-to-access-array-offset-on-%s <null-or-boolean-arrays>`
* :ref:`trying-to-access-array-offset-on-%s <null-or-boolean-arrays>`
* :ref:`trying-to-access-array-offset-on-%s <null-or-boolean-arrays>`
* :ref:`trying-to-access-array-offset-on-%s <null-or-boolean-arrays>`
* :ref:`trying-to-access-array-offset-on-%s <scalar-are-not-arrays>`
* :ref:`type-%c:-unknown-format-code <invalid-pack-format>`
* :ref:`type-%c:-unknown-format-code <invalid-pack-format>`
* :ref:`type-%c:-unknown-format-code <pack-format-inventory>`
* :ref:`type-of-%s\:\:$%s-must-be-%s%s-(as-in-class-%s) <inherited-property-type-must-match>`
* :ref:`type-of-%s\:\:$%s-must-be-%s%s-(as-in-class-%s) <mismatch-properties-types>`
* :ref:`type-of-%s\:\:$%s-must-not-be-defined-(as-in-class-%s) <inherited-property-type-must-match>`
* :ref:`typed-property-%s\:\:$%s-must-not-be-accessed-before-initialization <untyped-no-default-properties>`
* :ref:`undefined-array-key <possible-missing-subpattern>`
* :ref:`undefined-class-constant-'%s\:\:%s' <avoid-self-in-interface>`
* :ref:`undefined-class-constant-'%s\:\:%s' <unused-enumeration-case>`
* :ref:`undefined-constant-"%s <non-constant-index-in-array>`
* :ref:`undefined-constant-"%s <undefined-class-constants>`
* :ref:`undefined-constant-"%s <undefined-constant-name>`
* :ref:`undefined-constant-"%s <undefined-constants>`
* :ref:`undefined-constant-%s\:\:%s <insufficient-type>`
* :ref:`undefined-constant-%s\:\:%s <undefined-enumcase>`
* :ref:`undefined-property-%s\:\:$%s <don't-unset-properties>`
* :ref:`undefined-property-%s\:\:$%s <undefined-properties>`
* :ref:`undefined-variable <casting-ternary>`
* :ref:`undefined-variable <missing-assignation-in-branches>`
* :ref:`undefined-variable <nonexistent-variable-in-compact()>`
* :ref:`undefined-variable <undefined-variable>`
* :ref:`unknown-format-specifier-"%c <sprintf-format-compilation>`
* :ref:`unknown-named-parameter-$%s <unknown-parameter-name>`
* :ref:`unparenthesized-a-?-b-:-c-?-d-:-e-is-not-supported. <nested-ternary-without-parenthesis>`
* :ref:`unsupported-operand-types <unsupported-operand-types>`
* :ref:`unsupported-operand-types <unsupported-types-with-operators>`
* :ref:`use-of-"parent"-in-callables-is-deprecated <deprecated-callable>`
* :ref:`use-of-"self"-in-callables-is-deprecated <deprecated-callable>`
* :ref:`use-of-"static"-in-callables-is-deprecated <deprecated-callable>`
* :ref:`using-$this-when-not-in-object-context <$this-belongs-to-classes-or-traits>`
* :ref:`using-$this-when-not-in-object-context <$this-is-not-for-static-methods>`
* :ref:`using-$this-when-not-in-object-context <static-methods-can't-contain-$this>`
* :ref:`using-$this-when-not-in-object-context <using-$this-outside-a-class>`
* :ref:`using-array_key_exists()-on-objects-is-deprecated. <array\_key\_exists()-works-on-arrays>`
* :ref:`wrong-encoding,-conversion-from-"%s"-to-"%s"-is-not-allowed <iconv-with-translit>`




Directory by Exception
----------------------

Exakat has rules that help identify possible exceptions in the code.

  + ArithmeticError Error

    + :ref:`Could Use Try <could-use-try>`

  + DivisionByZeroError

    + :ref:`Could Use Try <could-use-try>`

  + Exception

    + :ref:`Could Use Try <could-use-try>`

  + ImagickException

    + :ref:`Could Use Try <could-use-try>`

  + ImagickPixelException

    + :ref:`Could Use Try <could-use-try>`

  + InvalidArgumentException

    + :ref:`Could Use Try <could-use-try>`

  + JsonException

    + :ref:`Could Use Try <could-use-try>`

  + PDOException

    + :ref:`Could Use Try <could-use-try>`

  + PharException

    + :ref:`Could Use Try <could-use-try>`

  + ReflectionException

    + :ref:`Could Use Try <could-use-try>`

  + SVMException

    + :ref:`Could Use Try <could-use-try>`

  + Type Error

    + :ref:`Could Use Try <could-use-try>`

  + UnexpectedValueException

    + :ref:`Could Use Try <could-use-try>`

  + mysqli_sql_exception

    + :ref:`Could Use Try <could-use-try>`


