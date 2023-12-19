.. _report-exakatyaml:

Exakatyaml
++++++++++

Exakatyaml
__________

Builds a list of ruleset, based on the number of issues from the previous audit.

Exakatyaml helps with the configuration of exakat in a CI. It builds a list of ruleset, based on the number of issues from the previous audit.

Continuous Integration require steps that yield no issues. This is good for analysis that yield no results : in a word, all analysis that are currently clean should be in the CI. That way, any return will be monitored.

On the other hand, other analysis that currently yield issues needs to be fully cleaned before usage. 

::

    project: my_project
    project_name: my_project
    project_themes: {  }
    project_reports:
        - Ambassador
    rulesets:
        ruleset_0: # 0 errors found
             "Accessing Private":                                 Classes/AccessPrivate
             "Adding Zero":                                       Structures/AddZero
             "Aliases Usage":                                     Functions/AliasesUsage
             "Already Parents Interface":                         Interfaces/AlreadyParentsInterface
             "Already Parents Trait":                             Traits/AlreadyParentsTrait
             "Altering Foreach Without Reference":                Structures/AlteringForeachWithoutReference
             "Alternative Syntax Consistence":                    Structures/AlternativeConsistenceByFile
             "Always Positive Comparison":                        Structures/NeverNegative
    # Other results here
        ruleset_1: # 1 errors found
             "Constant Class":                                    Classes/ConstantClass
             "Could Be Abstract Class":                           Classes/CouldBeAbstractClass
             "Dependant Trait":                                   Traits/DependantTrait
             "Double Instructions":                               Structures/DoubleInstruction
    # Other results here
        ruleset_2: # 2 errors found
             "Always Anchor Regex":                               Security/AnchorRegex
             "Forgotten Interface":                               Interfaces/CouldUseInterface
    # Other results here
        ruleset_3: # 3 errors found
             "@ Operator":                                        Structures/Noscream
             "Indices Are Int Or String":                         Structures/IndicesAreIntOrString
             "Modernize Empty With Expression":                   Structures/ModernEmpty
             "Property Variable Confusion":                       Structures/PropertyVariableConfusion
    # Other results here
        ruleset_4: # 4 errors found
             "Buried Assignation":                                Structures/BuriedAssignation
             "Identical Consecutive Expression":                  Structures/IdenticalConsecutive
    # Other results here
        ruleset_122: # 122 errors found
             "Method Could Be Static":                            Classes/CouldBeStatic




::

    project: page_manager
    project_name: drupal_page_manager
    project_themes: {  }
    project_reports:
        - Ambassador
    rulesets:
        ruleset_0: # 0 errors found
             "$HTTP_RAW_POST_DATA Usage":                         Php/RawPostDataUsage
             "$this Belongs To Classes Or Traits":                Classes/ThisIsForClasses
             "$this Is Not An Array":                             Classes/ThisIsNotAnArray
             "$this Is Not For Static Methods":                   Classes/ThisIsNotForStatic
             "Abstract Or Implements":                            Classes/AbstractOrImplements
             "Access Protected Structures":                       Classes/AccessProtected
             "Accessing Private":                                 Classes/AccessPrivate
             "Adding Zero":                                       Structures/AddZero
             "Aliases Usage":                                     Functions/AliasesUsage
             "Already Parents Interface":                         Interfaces/AlreadyParentsInterface
             "Already Parents Trait":                             Traits/AlreadyParentsTrait
             "Altering Foreach Without Reference":                Structures/AlteringForeachWithoutReference
             "Alternative Syntax Consistence":                    Structures/AlternativeConsistenceByFile
             "Always Positive Comparison":                        Structures/NeverNegative
             "Ambiguous Array Index":                             Arrays/AmbiguousKeys
             "Ambiguous Static":                                  Classes/AmbiguousStatic
             "Ambiguous Visibilities":                            Classes/AmbiguousVisibilities
             "Anonymous Classes":                                 Classes/Anonymous
             "Assert Function Is Reserved":                       Php/AssertFunctionIsReserved
             "Assign And Compare":                                Structures/AssigneAndCompare
             "Assign Default To Properties":                      Classes/MakeDefault
             "Assign With And":                                   Php/AssignAnd
             "Assigned Twice":                                    Variables/AssignedTwiceOrMore
             "Avoid Parenthesis":                                 Structures/PrintWithoutParenthesis
             "Avoid Those Hash Functions":                        Security/AvoidThoseCrypto
             "Avoid Using stdClass":                              Php/UseStdclass
             "Avoid get_class()":                                 Structures/UseInstanceof
             "Avoid option arrays in constructors":               Classes/AvoidOptionArrays
             "Avoid set_error_handler $context Argument":         Php/AvoidSetErrorHandlerContextArg
             "Avoid sleep()/usleep()":                            Security/NoSleep
             "Bad Constants Names":                               Constants/BadConstantnames
             "Callback Needs Return":                             Functions/CallbackNeedsReturn
             "Can't Count Non-Countable":                         Structures/CanCountNonCountable
             "Can't Extend Final":                                Classes/CantExtendFinal
             "Can't Throw Throwable":                             Exceptions/CantThrow
             "Cant Inherit Abstract Method":                      Classes/CantInheritAbstractMethod
             "Cant Instantiate Class":                            Classes/CantInstantiateClass
             "Case Insensitive Constants":                        Constants/CaseInsensitiveConstants
             "Cast To Boolean":                                   Structures/CastToBoolean
             "Casting Ternary":                                   Structures/CastingTernary
             "Catch Overwrite Variable":                          Structures/CatchShadowsVariable
             "Check All Types":                                   Structures/CheckAllTypes
             "Check JSON":                                        Structures/CheckJson
             "Check On __Call Usage":                             Classes/CheckOnCallUsage
             "Child Class Removes Typehint":                      Classes/ChildRemoveTypehint
             "Class Function Confusion":                          Php/ClassFunctionConfusion
             "Class Should Be Final By Ocramius":                 Classes/FinalByOcramius
             "Class, Interface Or Trait With Identical Names":    Classes/CitSameName
             "Classes Mutually Extending Each Other":             Classes/MutualExtension
             "Clone With Non-Object":                             Classes/CloneWithNonObject
             "Common Alternatives":                               Structures/CommonAlternatives
             "Compact Inexistant Variable":                       Php/CompactInexistant
             "Compare Hash":                                      Security/CompareHash
             "Compared Comparison":                               Structures/ComparedComparison
             "Concat And Addition":                               Php/ConcatAndAddition
             "Concat Empty String":                               Structures/ConcatEmpty
             "Concrete Visibility":                               Interfaces/ConcreteVisibility
             "Configure Extract":                                 Security/ConfigureExtract
             "Const Visibility Usage":                            Classes/ConstVisibilityUsage
             "Constants Created Outside Its Namespace":           Constants/CreatedOutsideItsNamespace
             "Constants With Strange Names":                      Constants/ConstantStrangeNames
             "Continue Is For Loop":                              Structures/ContinueIsForLoop
             "Could Be Else":                                     Structures/CouldBeElse
             "Could Be Static":                                   Structures/CouldBeStatic
             "Could Use Short Assignation":                       Structures/CouldUseShortAssignation
             "Could Use __DIR__":                                 Structures/CouldUseDir
             "Could Use self":                                    Classes/ShouldUseSelf
             "Could Use str_repeat()":                            Structures/CouldUseStrrepeat
             "Crc32() Might Be Negative":                         Php/Crc32MightBeNegative
             "Dangling Array References":                         Structures/DanglingArrayReferences
             "Deep Definitions":                                  Functions/DeepDefinitions
             "Define With Array":                                 Php/DefineWithArray
             "Deprecated Functions":                              Php/Deprecated
             "Direct Call To __clone()":                          Php/DirectCallToClone
             "Direct Injection":                                  Security/DirectInjection
             "Don't Change Incomings":                            Structures/NoChangeIncomingVariables
             "Don't Echo Error":                                  Security/DontEchoError
             "Don't Read And Write In One Expression":            Structures/DontReadAndWriteInOneExpression
             "Don't Send $this In Constructor":                   Classes/DontSendThisInConstructor
             "Don't Unset Properties":                            Classes/DontUnsetProperties
             "Dont Change The Blind Var":                         Structures/DontChangeBlindKey
             "Dont Mix ++":                                       Structures/DontMixPlusPlus
             "Double Assignation":                                Structures/DoubleAssignation
             "Dynamic Library Loading":                           Security/DynamicDl
             "Echo With Concat":                                  Structures/EchoWithConcat
             "Else If Versus Elseif":                             Structures/ElseIfElseif
             "Empty Blocks":                                      Structures/EmptyBlocks
             "Empty Instructions":                                Structures/EmptyLines
             "Empty Interfaces":                                  Interfaces/EmptyInterface
             "Empty Namespace":                                   Namespaces/EmptyNamespace
             "Empty Traits":                                      Traits/EmptyTrait
             "Empty Try Catch":                                   Structures/EmptyTryCatch
             "Encoded Simple Letters":                            Security/EncodedLetters
             "Eval() Usage":                                      Structures/EvalUsage
             "Exception Order":                                   Exceptions/AlreadyCaught
             "Exit() Usage":                                      Structures/ExitUsage
             "Failed Substr Comparison":                          Structures/FailingSubstrComparison
             "Flexible Heredoc":                                  Php/FlexibleHeredoc
             "Foreach On Object":                                 Php/ForeachObject
             "Foreach Reference Is Not Modified":                 Structures/ForeachReferenceIsNotModified
             "Forgotten Visibility":                              Classes/NonPpp
             "Forgotten Whitespace":                              Structures/ForgottenWhiteSpace
             "Fully Qualified Constants":                         Namespaces/ConstantFullyQualified
             "Functions/BadTypehintRelay":                        Functions/BadTypehintRelay
             "Global Usage":                                      Structures/GlobalUsage
             "Group Use Declaration":                             Php/GroupUseDeclaration
             "Group Use Trailing Comma":                          Php/GroupUseTrailingComma
             "Hash Algorithms Incompatible With PHP 5.3":         Php/HashAlgos53
             "Hash Algorithms":                                   Php/HashAlgos
             "Hash Will Use Objects":                             Php/HashUsesObjects
             "Hexadecimal In String":                             Type/HexadecimalString
             "Hidden Use Expression":                             Namespaces/HiddenUse
             "Htmlentities Calls":                                Structures/Htmlentitiescall
             "Identical Conditions":                              Structures/IdenticalConditions
             "Identical On Both Sides":                           Structures/IdenticalOnBothSides
             "If With Same Conditions":                           Structures/IfWithSameConditions
             "Illegal Name For Method":                           Classes/WrongName
             "Implement Is For Interface":                        Classes/ImplementIsForInterface
             "Implemented Methods Are Public":                    Classes/ImplementedMethodsArePublic
             "Implicit Global":                                   Structures/ImplicitGlobal
             "Implied If":                                        Structures/ImpliedIf
             "Inclusion Wrong Case":                              Files/InclusionWrongCase
             "Incompatible Signature Methods":                    Classes/IncompatibleSignature
             "Incompilable Files":                                Php/Incompilable
             "Indirect Injection":                                Security/IndirectInjection
             "Integer As Property":                               Classes/IntegerAsProperty
             "Integer Conversion":                                Security/IntegerConversion
             "Invalid Class Name":                                Classes/WrongCase
             "Invalid Constant Name":                             Constants/InvalidName
             "Invalid Pack Format":                               Structures/InvalidPackFormat
             "Invalid Regex":                                     Structures/InvalidRegex
             "Is Actually Zero":                                  Structures/IsZero
             "List Short Syntax":                                 Php/ListShortSyntax
             "List With Appends":                                 Php/ListWithAppends
             "List With Reference":                               Php/ListWithReference
             "Logical Mistakes":                                  Structures/LogicalMistakes
             "Logical Should Use Symbolic Operators":             Php/LogicalInLetters
             "Lone Blocks":                                       Structures/LoneBlock
             "Lost References":                                   Variables/LostReferences
             "Make Global A Property":                            Classes/MakeGlobalAProperty
             "Method Collision Traits":                           Traits/MethodCollisionTraits
             "Method Signature Must Be Compatible":               Classes/MethodSignatureMustBeCompatible
             "Minus One On Error":                                Security/MinusOneOnError
             "Mismatch Type And Default":                         Functions/MismatchTypeAndDefault
             "Mismatched Default Arguments":                      Functions/MismatchedDefaultArguments
             "Mismatched Ternary Alternatives":                   Structures/MismatchedTernary
             "Mismatched Typehint":                               Functions/MismatchedTypehint
             "Missing Cases In Switch":                           Structures/MissingCases
             "Missing Include":                                   Files/MissingInclude
             "Missing New ?":                                     Structures/MissingNew
             "Missing Parenthesis":                               Structures/MissingParenthesis
             "Mixed Concat And Interpolation":                    Structures/MixedConcatInterpolation
             "Mkdir Default":                                     Security/MkdirDefault
             "Multiple Alias Definitions Per File":               Namespaces/MultipleAliasDefinitionPerFile
             "Multiple Class Declarations":                       Classes/MultipleDeclarations
             "Multiple Constant Definition":                      Constants/MultipleConstantDefinition
             "Multiple Exceptions Catch()":                       Exceptions/MultipleCatch
             "Multiple Identical Trait Or Interface":             Classes/MultipleTraitOrInterface
             "Multiple Index Definition":                         Arrays/MultipleIdenticalKeys
             "Multiple Type Variable":                            Structures/MultipleTypeVariable
             "Multiples Identical Case":                          Structures/MultipleDefinedCase
             "Multiply By One":                                   Structures/MultiplyByOne
             "Must Call Parent Constructor":                      Php/MustCallParentConstructor
             "Must Return Methods":                               Functions/MustReturn
             "Negative Power":                                    Structures/NegativePow
             "Nested Ternary":                                    Structures/NestedTernary
             "Never Used Parameter":                              Functions/NeverUsedParameter
             "New Constants In PHP 7.2":                          Php/Php72NewConstants
             "New Functions In PHP 7.0":                          Php/Php70NewFunctions
             "New Functions In PHP 7.1":                          Php/Php71NewFunctions
             "New Functions In PHP 7.2":                          Php/Php72NewFunctions
             "New Functions In PHP 7.3":                          Php/Php73NewFunctions
             "Next Month Trap":                                   Structures/NextMonthTrap
             "No Choice":                                         Structures/NoChoice
             "No Direct Call To Magic Method":                    Classes/DirectCallToMagicMethod
             "No Direct Usage":                                   Structures/NoDirectUsage
             "No Empty Regex":                                    Structures/NoEmptyRegex
             "No Hardcoded Hash":                                 Structures/NoHardcodedHash
             "No Hardcoded Ip":                                   Structures/NoHardcodedIp
             "No Hardcoded Path":                                 Structures/NoHardcodedPath
             "No Hardcoded Port":                                 Structures/NoHardcodedPort
             "No Magic With Array":                               Classes/NoMagicWithArray
             "No Parenthesis For Language Construct":             Structures/NoParenthesisForLanguageConstruct
             "No Real Comparison":                                Type/NoRealComparison
             "No Reference For Ternary":                          Php/NoReferenceForTernary
             "No Reference On Left Side":                         Structures/NoReferenceOnLeft
             "No Return For Generator":                           Php/NoReturnForGenerator
             "No Return Or Throw In Finally":                     Structures/NoReturnInFinally
             "No Return Used":                                    Functions/NoReturnUsed
             "No Self Referencing Constant":                      Classes/NoSelfReferencingConstant
             "No String With Append":                             Php/NoStringWithAppend
             "No Substr Minus One":                               Php/NoSubstrMinusOne
             "No Substr() One":                                   Structures/NoSubstrOne
             "No get_class() With Null":                          Structures/NoGetClassNull
             "No isset() With empty()":                           Structures/NoIssetWithEmpty
             "Non Ascii Variables":                               Variables/VariableNonascii
             "Non Static Methods Called In A Static":             Classes/NonStaticMethodsCalledStatic
             "Non-constant Index In Array":                       Arrays/NonConstantArray
             "Not A Scalar Type":                                 Php/NotScalarType
             "Not Not":                                           Structures/NotNot
             "Objects Don't Need References":                     Structures/ObjectReferences
             "Old Style Constructor":                             Classes/OldStyleConstructor
             "Old Style __autoload()":                            Php/oldAutoloadUsage
             "One Variable String":                               Type/OneVariableStrings
             "Only Variable For Reference":                       Functions/OnlyVariableForReference
             "Only Variable Passed By Reference":                 Functions/OnlyVariablePassedByReference
             "Only Variable Returned By Reference":               Structures/OnlyVariableReturnedByReference
             "Or Die":                                            Structures/OrDie
             "Overwritten Exceptions":                            Exceptions/OverwriteException
             "Overwritten Literals":                              Variables/OverwrittenLiterals
             "PHP 7.0 New Classes":                               Php/Php70NewClasses
             "PHP 7.0 New Interfaces":                            Php/Php70NewInterfaces
             "PHP 7.0 Removed Directives":                        Php/Php70RemovedDirective
             "PHP 7.0 Removed Functions":                         Php/Php70RemovedFunctions
             "PHP 7.0 Scalar Typehints":                          Php/PHP70scalartypehints
             "PHP 7.1 Microseconds":                              Php/Php71microseconds
             "PHP 7.1 Removed Directives":                        Php/Php71RemovedDirective
             "PHP 7.1 Scalar Typehints":                          Php/PHP71scalartypehints
             "PHP 7.2 Deprecations":                              Php/Php72Deprecation
             "PHP 7.2 Object Keyword":                            Php/Php72ObjectKeyword
             "PHP 7.2 Removed Functions":                         Php/Php72RemovedFunctions
             "PHP 7.2 Scalar Typehints":                          Php/PHP72scalartypehints
             "PHP 7.3 Last Empty Argument":                       Php/PHP73LastEmptyArgument
             "PHP 7.3 Removed Functions":                         Php/Php73RemovedFunctions
             "PHP7 Dirname":                                      Structures/PHP7Dirname
             "Parent First":                                      Classes/ParentFirst
             "Parent, Static Or Self Outside Class":              Classes/PssWithoutClass
             "Parenthesis As Parameter":                          Php/ParenthesisAsParameter
             "Pathinfo() Returns May Vary":                       Php/PathinfoReturns
             "Php 7 Indirect Expression":                         Variables/Php7IndirectExpression
             "Php 7.1 New Class":                                 Php/Php71NewClasses
             "Php 7.2 New Class":                                 Php/Php72NewClasses
             "Php7 Relaxed Keyword":                              Php/Php7RelaxedKeyword
             "Phpinfo":                                           Structures/PhpinfoUsage
             "Possible Infinite Loop":                            Structures/PossibleInfiniteLoop
             "Possible Missing Subpattern":                       Php/MissingSubpattern
             "Preprocessable":                                    Structures/ShouldPreprocess
             "Print And Die":                                     Structures/PrintAndDie
             "Printf Number Of Arguments":                        Structures/PrintfArguments
             "Property Could Be Local":                           Classes/PropertyCouldBeLocal
             "Queries In Loops":                                  Structures/QueriesInLoop
             "Random Without Try":                                Structures/RandomWithoutTry
             "Redeclared PHP Functions":                          Functions/RedeclaredPhpFunction
             "Redefined Class Constants":                         Classes/RedefinedConstants
             "Redefined Default":                                 Classes/RedefinedDefault
             "Redefined Private Property":                        Classes/RedefinedPrivateProperty
             "Register Globals":                                  Security/RegisterGlobals
             "Repeated Interface":                                Interfaces/RepeatedInterface
             "Repeated Regex":                                    Structures/RepeatedRegex
             "Repeated print()":                                  Structures/RepeatedPrint
             "Results May Be Missing":                            Structures/ResultMayBeMissing
             "Rethrown Exceptions":                               Exceptions/Rethrown
             "Return True False":                                 Structures/ReturnTrueFalse
             "Safe Curl Options":                                 Security/CurlOptions
             "Safe HTTP Headers":                                 Security/SafeHttpHeaders
             "Same Variables Foreach":                            Structures/AutoUnsetForeach
             "Scalar Or Object Property":                         Classes/ScalarOrObjectProperty
             "Self Using Trait":                                  Traits/SelfUsingTrait
             "Session Lazy Write":                                Security/SessionLazyWrite
             "Set Cookie Safe Arguments":                         Security/SetCookieArgs
             "Setlocale() Uses Constants":                        Structures/SetlocaleNeedsConstants
             "Several Instructions On The Same Line":             Structures/OneLineTwoInstructions
             "Short Open Tags":                                   Php/ShortOpenTagRequired
             "Should Chain Exception":                            Structures/ShouldChainException
             "Should Make Alias":                                 Namespaces/ShouldMakeAlias
             "Should Typecast":                                   Type/ShouldTypecast
             "Should Use Constants":                              Functions/ShouldUseConstants
             "Should Use Prepared Statement":                     Security/ShouldUsePreparedStatement
             "Should Use SetCookie()":                            Php/UseSetCookie
             "Should Yield With Key":                             Functions/ShouldYieldWithKey
             "Silently Cast Integer":                             Type/SilentlyCastInteger
             "Sqlite3 Requires Single Quotes":                    Security/Sqlite3RequiresSingleQuotes
             "Static Methods Can't Contain $this":                Classes/StaticContainsThis
             "Strange Name For Constants":                        Constants/StrangeName
             "Strange Name For Variables":                        Variables/StrangeName
             "String Initialization":                             Arrays/StringInitialization
             "String May Hold A Variable":                        Type/StringHoldAVariable
             "Strings With Strange Space":                        Type/StringWithStrangeSpace
             "Strpos()-like Comparison":                          Structures/StrposCompare
             "Strtr Arguments":                                   Php/StrtrArguments
             "Suspicious Comparison":                             Structures/SuspiciousComparison
             "Switch Fallthrough":                                Structures/Fallthrough
             "Switch To Switch":                                  Structures/SwitchToSwitch
             "Switch Without Default":                            Structures/SwitchWithoutDefault
             "Ternary In Concat":                                 Structures/TernaryInConcat
             "Test Then Cast":                                    Structures/TestThenCast
             "Throw Functioncall":                                Exceptions/ThrowFunctioncall
             "Throw In Destruct":                                 Classes/ThrowInDestruct
             "Throws An Assignement":                             Structures/ThrowsAndAssign
             "Timestamp Difference":                              Structures/TimestampDifference
             "Too Many Finds":                                    Classes/TooManyFinds
             "Too Many Native Calls":                             Php/TooManyNativeCalls
             "Trailing Comma In Calls":                           Php/TrailingComma
             "Traits/TraitNotFound":                              Traits/TraitNotFound
             "Typehint Must Be Returned":                         Functions/TypehintMustBeReturned
             "Typehinted References":                             Functions/TypehintedReferences
             "Unchecked Resources":                               Structures/UncheckedResources
             "Unconditional Break In Loop":                       Structures/UnconditionLoopBreak
             "Undeclared Static Property":                        Classes/UndeclaredStaticProperty
             "Undefined Constants":                               Constants/UndefinedConstants
             "Undefined Insteadof":                               Traits/UndefinedInsteadof
             "Undefined static:: Or self::":                      Classes/UndefinedStaticMP
             "Unicode Escape Syntax":                             Php/UnicodeEscapeSyntax
             "Unknown Pcre2 Option":                              Php/UnknownPcre2Option
             "Unkown Regex Options":                              Structures/UnknownPregOption
             "Unpreprocessed Values":                             Structures/Unpreprocessed
             "Unreachable Code":                                  Structures/UnreachableCode
             "Unset In Foreach":                                  Structures/UnsetInForeach
             "Unthrown Exception":                                Exceptions/Unthrown
             "Unused Constants":                                  Constants/UnusedConstants
             "Unused Global":                                     Structures/UnusedGlobal
             "Unused Inherited Variable In Closure":              Functions/UnusedInheritedVariable
             "Unused Interfaces":                                 Interfaces/UnusedInterfaces
             "Unused Label":                                      Structures/UnusedLabel
             "Unused Private Methods":                            Classes/UnusedPrivateMethod
             "Unused Private Properties":                         Classes/UnusedPrivateProperty
             "Unused Returned Value":                             Functions/UnusedReturnedValue
             "Upload Filename Injection":                         Security/UploadFilenameInjection
             "Use Constant As Arguments":                         Functions/UseConstantAsArguments
             "Use Constant":                                      Structures/UseConstant
             "Use Instanceof":                                    Classes/UseInstanceof
             "Use Nullable Type":                                 Php/UseNullableType
             "Use PHP Object API":                                Php/UseObjectApi
             "Use Pathinfo":                                      Php/UsePathinfo
             "Use System Tmp":                                    Structures/UseSystemTmp
             "Use With Fully Qualified Name":                     Namespaces/UseWithFullyQualifiedNS
             "Use const":                                         Constants/ConstRecommended
             "Use random_int()":                                  Php/BetterRand
             "Used Once Variables":                               Variables/VariableUsedOnce
             "Useless Abstract Class":                            Classes/UselessAbstract
             "Useless Alias":                                     Traits/UselessAlias
             "Useless Brackets":                                  Structures/UselessBrackets
             "Useless Casting":                                   Structures/UselessCasting
             "Useless Constructor":                               Classes/UselessConstructor
             "Useless Final":                                     Classes/UselessFinal
             "Useless Global":                                    Structures/UselessGlobal
             "Useless Instructions":                              Structures/UselessInstruction
             "Useless Interfaces":                                Interfaces/UselessInterfaces
             "Useless Parenthesis":                               Structures/UselessParenthesis
             "Useless Return":                                    Functions/UselessReturn
             "Useless Switch":                                    Structures/UselessSwitch
             "Useless Unset":                                     Structures/UselessUnset
             "Var Keyword":                                       Classes/OldStyleVar
             "Weak Typing":                                       Classes/WeakType
             "While(List() = Each())":                            Structures/WhileListEach
             "Wrong Number Of Arguments":                         Functions/WrongNumberOfArguments
             "Wrong Optional Parameter":                          Functions/WrongOptionalParameter
             "Wrong Parameter Type":                              Php/InternalParameterType
             "Wrong Range Check":                                 Structures/WrongRange
             "Wrong fopen() Mode":                                Php/FopenMode
             "__DIR__ Then Slash":                                Structures/DirThenSlash
             "__toString() Throws Exception":                     Structures/toStringThrowsException
             "error_reporting() With Integers":                   Structures/ErrorReportingWithInteger
             "eval() Without Try":                                Structures/EvalWithoutTry
             "ext/ereg":                                          Extensions/Extereg
             "ext/mcrypt":                                        Extensions/Extmcrypt
             "filter_input() As A Source":                        Security/FilterInputSource
             "func_get_arg() Modified":                           Functions/funcGetArgModified
             "include_once() Usage":                              Structures/OnceUsage
             "isset() With Constant":                             Structures/IssetWithConstant
             "list() May Omit Variables":                         Structures/ListOmissions
             "move_uploaded_file Instead Of copy":                Security/MoveUploadedFile
             "parse_str() Warning":                               Security/parseUrlWithoutParameters
             "preg_replace With Option e":                        Structures/pregOptionE
             "self, parent, static Outside Class":                Classes/NoPSSOutsideClass
             "set_exception_handler() Warning":                   Php/SetExceptionHandlerPHP7
             "var_dump()... Usage":                               Structures/VardumpUsage
        ruleset_1: # 1 errors found
             "Constant Class":                                    Classes/ConstantClass
             "Could Be Abstract Class":                           Classes/CouldBeAbstractClass
             "Dependant Trait":                                   Traits/DependantTrait
             "Double Instructions":                               Structures/DoubleInstruction
             "Drop Else After Return":                            Structures/DropElseAfterReturn
             "Empty Classes":                                     Classes/EmptyClass
             "Forgotten Thrown":                                  Exceptions/ForgottenThrown
             "Inconsistent Elseif":                               Structures/InconsistentElseif
             "Instantiating Abstract Class":                      Classes/InstantiatingAbstractClass
             "List With Keys":                                    Php/ListWithKeys
             "Logical To in_array":                               Performances/LogicalToInArray
             "No Need For Else":                                  Structures/NoNeedForElse
             "Same Conditions In Condition":                      Structures/SameConditions
             "Should Use session_regenerateid()":                 Security/ShouldUseSessionRegenerateId
             "Static Loop":                                       Structures/StaticLoop
             "Too Many Injections":                               Classes/TooManyInjections
             "Undefined Caught Exceptions":                       Exceptions/CaughtButNotThrown
             "Unresolved Catch":                                  Classes/UnresolvedCatch
             "Unserialize Second Arg":                            Security/UnserializeSecondArg
             "Use Positive Condition":                            Structures/UsePositiveCondition
             "Useless Catch":                                     Exceptions/UselessCatch
             "Useless Check":                                     Structures/UselessCheck
        ruleset_2: # 2 errors found
             "Always Anchor Regex":                               Security/AnchorRegex
             "Forgotten Interface":                               Interfaces/CouldUseInterface
             "No Class As Typehint":                              Functions/NoClassAsTypehint
             "No array_merge() In Loops":                         Performances/ArrayMergeInLoops
             "Pre-increment":                                     Performances/PrePostIncrement
             "Randomly Sorted Arrays":                            Arrays/RandomlySortedLiterals
             "Should Make Ternary":                               Structures/ShouldMakeTernary
             "Should Use Coalesce":                               Php/ShouldUseCoalesce
             "Use === null":                                      Php/IsnullVsEqualNull
        ruleset_3: # 3 errors found
             "@ Operator":                                        Structures/Noscream
             "Indices Are Int Or String":                         Structures/IndicesAreIntOrString
             "Modernize Empty With Expression":                   Structures/ModernEmpty
             "Property Variable Confusion":                       Structures/PropertyVariableConfusion
             "Too Many Local Variables":                          Functions/TooManyLocalVariables
             "Unused Classes":                                    Classes/UnusedClass
             "Usort Sorting In PHP 7.0":                          Php/UsortSorting
        ruleset_4: # 4 errors found
             "Buried Assignation":                                Structures/BuriedAssignation
             "Identical Consecutive Expression":                  Structures/IdenticalConsecutive
             "Nested Ifthen":                                     Structures/NestedIfthen
             "No Boolean As Default":                             Functions/NoBooleanAsDefault
             "Use Named Boolean In Argument Definition":          Functions/AvoidBooleanArgument
        ruleset_5: # 5 errors found
             "Avoid Optional Properties":                         Classes/AvoidOptionalProperties
             "Empty Function":                                    Functions/EmptyFunction
             "Relay Function":                                    Functions/RelayFunction
             "Strict Comparison With Booleans":                   Structures/BooleanStrictComparison
             "Use Class Operator":                                Classes/UseClassOperator
             "strpos() Too Much":                                 Performances/StrposTooMuch
        ruleset_6: # 6 errors found
             "Used Once Property":                                Classes/UsedOnceProperty
        ruleset_7: # 7 errors found
             "No Class In Global":                                Php/NoClassInGlobal
             "Uncaught Exceptions":                               Exceptions/UncaughtExceptions
             "Unused Functions":                                  Functions/UnusedFunctions
             "Wrong Number Of Arguments In Methods":              Functions/WrongNumberOfArgumentsMethods
        ruleset_8: # 8 errors found
             "Could Make A Function":                             Functions/CouldCentralize
             "Insufficient Typehint":                             Functions/InsufficientTypehint
             "Long Arguments":                                    Structures/LongArguments
             "Property Used In One Method Only":                  Classes/PropertyUsedInOneMethodOnly
             "Static Methods Called From Object":                 Classes/StaticMethodsCalledFromObject
        ruleset_9: # 9 errors found
             "PHP Keywords As Names":                             Php/ReservedNames
             "Undefined Trait":                                   Traits/UndefinedTrait
             "Written Only Variables":                            Variables/WrittenOnlyVariable
        ruleset_10: # 10 errors found
             "Bail Out Early":                                    Structures/BailOutEarly
             "Hardcoded Passwords":                               Functions/HardcodedPasswords
             "Multiple Alias Definitions":                        Namespaces/MultipleAliasDefinitions
        ruleset_11: # 11 errors found
             "Variable Is Not A Condition":                       Structures/NoVariableIsACondition
        ruleset_13: # 13 errors found
             "Undefined Functions":                               Functions/UndefinedFunctions
             "Unused Use":                                        Namespaces/UnusedUse
        ruleset_14: # 14 errors found
             "Iffectations":                                      Structures/Iffectation
             "No Public Access":                                  Classes/NoPublicAccess
        ruleset_16: # 16 errors found
             "Overwriting Variable":                              Variables/Overwriting
        ruleset_17: # 17 errors found
             "No Net For Xml Load":                               Security/NoNetForXmlLoad
             "Unresolved Instanceof":                             Classes/UnresolvedInstanceof
        ruleset_21: # 21 errors found
             "Undefined Class Constants":                         Classes/UndefinedConstants
        ruleset_27: # 27 errors found
             "Locally Unused Property":                           Classes/LocallyUnusedProperty
             "Never Used Properties":                             Classes/PropertyNeverUsed
        ruleset_35: # 35 errors found
             "Useless Referenced Argument":                       Functions/UselessReferenceArgument
        ruleset_38: # 38 errors found
             "Uses Default Values":                               Functions/UsesDefaultArguments
        ruleset_47: # 47 errors found
             "Unused Arguments":                                  Functions/UnusedArguments
        ruleset_49: # 49 errors found
             "Undefined Properties":                              Classes/UndefinedProperty
        ruleset_77: # 77 errors found
             "Undefined Parent":                                  Classes/UndefinedParentMP
        ruleset_78: # 78 errors found
             "Undefined ::class":                                 Classes/UndefinedStaticclass
        ruleset_82: # 82 errors found
             "Class Could Be Final":                              Classes/CouldBeFinal
        ruleset_86: # 86 errors found
             "Unused Protected Methods":                          Classes/UnusedProtectedMethods
        ruleset_89: # 89 errors found
             "Unresolved Classes":                                Classes/UnresolvedClasses
        ruleset_94: # 94 errors found
             "Used Once Variables (In Scope)":                    Variables/VariableUsedOnceByContext
        ruleset_122: # 122 errors found
             "Method Could Be Static":                            Classes/CouldBeStatic
        ruleset_133: # 133 errors found
             "Should Use Local Class":                            Classes/ShouldUseThis
        ruleset_159: # 159 errors found
             "Undefined Interfaces":                              Interfaces/UndefinedInterfaces
        ruleset_160: # 160 errors found
             "Unused Methods":                                    Classes/UnusedMethods
        ruleset_183: # 183 errors found
             "Undefined Variable":                                Variables/UndefinedVariable
        ruleset_337: # 337 errors found
             "Unresolved Use":                                    Namespaces/UnresolvedUse
        ruleset_595: # 595 errors found
             "Undefined Classes":                                 Classes/UndefinedClasses
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Exakatyaml                                                       |
+--------------+------------------------------------------------------------------+
| Rulesets     | Exakatyaml doesn't depend on rulesets.                           |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Yaml                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in '.exakat.yaml'.                        |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


