.. _user-Configuration:

Configuration
===============


Summary
-------

* `Common Behavior`_
* `Project Configuration`_
* `In-code Configuration`_
* `Commandline Configuration`_
* `Specific analysis configurations`_

Common Behavior
---------------

General Philosophy
##################
Exakat tries to avoid configuration as much as possible, so as to focus on working out of the box, rather than spend time on pre-requisite.

As such, it probably does more work, but that may be dismissed later, at reading time.

More configuration options appear with the evolution of the engine.

Precedence
##########

The exakat engine read directives from three places :

1. The command line options
2. The .exakat.ini file at the root of the code
3. The config.ini file in the project directory
4. The exakat.ini file in the config directory
5. The default values in the code


The precedence of the directives is the same as the list above : command line options always have highest priority, config.ini files are in second, when command line are not available, and finally, the default values are read in the code.

Some of the directives are only available in the config.ini files.

Common Options
###############
 
All options are the same, whatever the command provided to exakat. -f always means files, and -q always means quick. 

Any option that a command doesn't understand is ignored. 

Any option that is not recognized is ignored and reported (with visibility).


Project Configuration
---------------------

Project configuration are were the project specific configuration are stored. For example, the project name, the ignored directories or its external libraries are kept. Configurations only affect one project and not the others.

Project configuration file are called 'config.ini'. They are located, one per project, in the 'projects/&lt;project name&gt;/config.ini' file. 

Available Options
#################

Here are the currently available options in Exakat's project configuration file : projects/&lt;project name&gt;/config.ini

+-----------------------+-------------------------------------------------------------------------------------------+
| Option                | Description                                                                               |
+=======================+===========================================================================================+
| phpversion            | Version with which to run the analyze.                                                    |
|                       | It may be one of : 7.3, 7.2, 7.1, 7.0, 5.6, 5.5, 5.4, 5.3, 5.2.                           |
|                       | Default is 7.2 or the CLI version used to init the project.                               |
|                       | 5.* versions are available, but are less tested.                                          |
|                       | 7.3 is actually the current dev version.                                                  |
+-----------------------+-------------------------------------------------------------------------------------------+
| include_dirs[]        | This is the list of files and dir to include in the project's directory. It is chrooted   |
|                       | in the project's folder. Values provided with a starting / are used as a path prefix.     |
|                       | Values without / are used as a substring, anywhere in the path.                           |
|                       | include_dirs are added AFTER ignore_dirs, so as to partially ignore a folder, such as     |
|                       | the vendor folder from composer.                                                          |
+-----------------------+-------------------------------------------------------------------------------------------+
| ignore_dirs[]         | This is the list of files and dir to ignore in the project's directory. It is chrooted in |
|                       | the project's folder. Values provided with a starting / are used as a path prefix. Values |
|                       | without / are used as a substring, anywhere in the path.                                  |
+-----------------------+-------------------------------------------------------------------------------------------+
| ignore_dirs[]         | This is the list of files and dir to ignore in the project's directory. It is chrooted in |
|                       | the project's folder. Values provided with a starting / are used as a path prefix. Values |
|                       | without / are used as a substring, anywhere in the path.                                  |
+-----------------------+-------------------------------------------------------------------------------------------+
| file_extensions       | This is the list of file extensions that is considered as PHP scripts. All others are     |
|                       | ignored. All files bearing those extensions are subject to check, though they are         |
|                       | scanned first for PHP tags before being analyzed. The extensions are comma separated,     |
|                       | without dot.                                                                              |
|                       | The default are : php, php3, inc, tpl, phtml, tmpl, phps, ctp                             |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_name          | This is the project name, as it appears at the top left in the Ambassador report.         |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_url           | This is the repository URL for the project. It is used to get the source for the project. |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_vcs           | This is the VCS used to fetch the project source.                                         |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_description   | This is the description of the project.                                                   |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_packagist     | This is the packagist name for the code, when the code is fetched with composer.          |
+-----------------------+-------------------------------------------------------------------------------------------+


In-code Configuration
---------------------

In-code configuration is a configuration file that sits at the root of the code. When exakat finds it, it uses it for in-code auditing.

The file is `.exakat.yaml`, and is a valid YAML file. `.exakat.yml` is also valid, but not recommended.

In case the file is found but not valid, Exakat reverts to default values. 

Unrecognized values are ignored. 

Exakat in-code example
######################
:: 

    project: exakat
    project_name: exakat
    project_rulesets: 
    - my_ruleset
    - Security
    project_report: 
    - Ambassador
    file_extensions: php,php3,phtml
    include_dirs: 
      - /
    ignore_dirs: 
      - /tests
      - /vendor
      - /docs
      - /media
    ignore_rules:
      - Structures/AddZero
    rulesets: 
      my_ruleset: 
          - Structures/AddZero
          - Structures/MultiplyByOne


Exakat in-code skeleton
#######################

Copy-paste this YAML code into a file called `.exakat.yaml`, located at the root of your repository.

:: 

    file_extensions: php,php3,phtml
    project: <project short name>
    project_name: <project name, as displayed in reports>
    project_rulesets: 
    - <list of rulesets to apply>
    - Analysis
    file_extensions: php,php3,phtml
    project_report: 
    - <list of reports to build>
    - Ambassador
    include_dirs: 
      - /
    ignore_rules:
      - 
    ignore_dirs: 
      - /tests
      - /vendor
      - /docs
      - /media


Available Options
#################

Here are the currently available options in Exakat's project configuration file : projects/&lt;project name&gt;/config.ini

+-----------------------+-------------------------------------------------------------------------------------------+
| Option                | Description                                                                               |
+=======================+===========================================================================================+
| include_dirs[]        | This is the list of files and dir to include in the project's directory. It is chrooted   |
|                       | in the project's folder. Values provided with a starting / are used as a path prefix.     |
|                       | Values without / are used as a substring, anywhere in the path.                           |
|                       | include_dirs are added AFTER ignore_dirs, so as to partially ignore a folder, such as     |
|                       | the vendor folder from composer.                                                          |
+-----------------------+-------------------------------------------------------------------------------------------+
| ignore_dirs[]         | This is the list of files and dir to ignore in the project's directory. It is chrooted in |
|                       | the project's folder. Values provided with a starting / are used as a path prefix. Values |
|                       | without / are used as a substring, anywhere in the path.                                  |
+-----------------------+-------------------------------------------------------------------------------------------+
| ignore_rules[]        | The rules mentioned in this list are ignored when running the audit. Rules are ignored    |
|                       | after loading the rulesets configuration : as such, it is possible to ignore rules inside |
|                       | a ruleset, without ignoring the whole ruleset.                                            |
|                       | The rules in this list are Exakat's short name : ignore_rules[] = "Structures/AddZero"    |
+-----------------------+-------------------------------------------------------------------------------------------+
| file_extensions       | This is the list of file extensions that is considered as PHP scripts. All others are     |
|                       | ignored. All files bearing those extensions are subject to check, though they are         |
|                       | scanned first for PHP tags before being analyzed. The extensions are comma separated,     |
|                       | without dot.                                                                              |
|                       | The default are : php, php3, inc, tpl, phtml, tmpl, phps, ctp                             |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_name          | This is the project name, as it appears at the top left in the Ambassador report.         |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_url           | This is the repository URL for the project. It is used to get the source for the project. |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_vcs           | This is the VCS used to fetch the project source.                                         |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_description   | This is the description of the project.                                                   |
+-----------------------+-------------------------------------------------------------------------------------------+
| project_packagist     | This is the packagist name for the code, when the code is fetched with composer.          |
+-----------------------+-------------------------------------------------------------------------------------------+



Commandline Configuration
-------------------------

Commandline configurations are detailled with each command, in the _Commands section.


Specific analysis configurations
--------------------------------

Some analyzer may be configured individually. Those parameters are then specific to one analyzer, and it only affects their behavior. 

Analyzers may be configured in the `project/*/config.ini`; they may also be configured globally in the `config/exakat.ini` file.

:ref:`Array() / [  ] Consistence <array()---[--]-consistence>`
  + array_ratio : 10

    + Percentage of arrays in one of the syntaxes, to trigger the other syntax as a violation. 
:ref:`Too Many Array Dimensions <too-many-array-dimensions>`
  + maxDimensions : 3

    + Number of valid dimensions in an array.
:ref:`Custom Class Usage <custom-class-usage>`
  + forbiddenClasses : 

    + List of classes to be avoided
:ref:`Cancel Common Method <cancel-common-method>`
  + cancelThreshold : 75

    + Minimal number of cancelled methods to suggest the cancellation of the parent.
:ref:`Could Be Parent Method <could-be-parent-method>`
  + minChildren : 4

    + Minimal number of children using this method.
:ref:`Fossilized Method <fossilized-method>`
  + fossilizationThreshold : 6

    + Minimal number of overwriting methods to consider a method difficult to update.
:ref:`Immutable Signature <immutable-signature>`
  + maxOverwrite : 8

    + Minimal number of method overwrite to consider that any refactor on the method signature is now hard.
:ref:`Make Magic Concrete <make-magic-concrete>`
  + magicMemberUsage : 1

    + Minimal number of magic member usage across the code, to trigger a concrete property.
:ref:`Too Many Children <too-many-children>`
  + childrenClassCount : 15

    + Threshold for too many children classes for one class.
:ref:`Too Many Dereferencing <too-many-dereferencing>`
  + tooManyDereferencing : 7

    + Maximum number of dereferencing.
:ref:`Too Many Finds <too-many-finds>`
  + minimumFinds : 5

    + Minimal number of prefixed methods to report.
  + findPrefix : find

    + list of prefix to use when detecting the 'find'. Comma-separated list, case insensitive. 
  + findSuffix : 

    + list of fix to use when detecting the 'find'. Comma-separated list, case insensitive. 
:ref:`Too Many Injections <too-many-injections>`
  + injectionsCount : 5

    + Threshold for too many injected parameters for one class.
:ref:`Large Try Block <large-try-block>`
  + tryBlockMaxSize : 5

    + Maximal number of expressions in the try block.
:ref:`Long Preparation For Throw <long-preparation-for-throw>`
  + preparationLineCount : 8

    + Minimal number of lines before the throw.
:ref:`Missing Include <missing-include>`
  + constant_or_variable_name : 100

    + Literal value to be used when including files. For example, by configuring 'Files_MissingInclude["HOME_DIR"] = "/tmp/myDir/";', then 'include HOME_DIR . "my_class.php"; will be actually be used as '/tmp/myDir/my_class.php'. Constants must be configured with their correct case. Variable must be configured with their initial '$'. Configure any number of variable and constant names.
:ref:`Could Make A Function <could-make-a-function>`
  + centralizeThreshold : 8

    + Minimal number of calls of the function with one common argument.
:ref:`Hardcoded Passwords <hardcoded-passwords>`
  + passwordsKeys : password_keys.json

    + List of array index and property names that shall be checked for potential secret key storages.
:ref:`Prefix And Suffixes With Typehint <prefix-and-suffixes-with-typehint>`
  + prefixedType : prefixedType['is'] = 'bool';
prefixedType['has'] = 'bool';
prefixedType['set'] = 'void';
prefixedType['list'] = 'array';

    + List of prefixes and their expected returntype
  + suffixedType : prefixedType['list'] = 'bool';
prefixedType['int'] = 'int';
prefixedType['string'] = 'string';
prefixedType['name'] = 'string';
prefixedType['description'] = 'string';
prefixedType['id'] = 'int';
prefixedType['uuid'] = '\Uuid';

    + List of suffixes and their expected returntype
:ref:`Too Many Local Variables <too-many-local-variables>`
  + tooManyLocalVariableThreshold : 15

    + Minimal number of variables in one function or method to report.
:ref:`Too Many Parameters <too-many-parameters>`
  + parametersCount : 8

    + Minimal number of parameters to report.
:ref:`Too Much Indented <too-much-indented>`
  + indentationAverage : 1

    + Minimal average of indentation in a method to report. Default is 1.0, which means that the method is on average at one level of indentation or more.
  + minimumSize : 3

    + Minimal number of expressions in a method to apply this analysis.
:ref:`Useless Argument <useless-argument>`
  + maxUsageCount : 30

    + Maximum count of function usage. Use this to limit the amount of processed arguments.
:ref:`Abstract Away <abstract-away>`
  + abstractableCalls : 

    + Functions that shouldn't be called directly, unless in a method.
  + abstractableClasses : 

    + Classes that shouldn't be instantiated directly, unless in a method.
:ref:`Memoize MagicCall <memoize-magiccall>`
  + minMagicCallsToGet : 2

    + Minimal number of calls of a magic property to make it worth locally caching.
:ref:`PHP Keywords As Names <php-keywords-as-names>`
  + reservedNames : 

    + Other reserved names : all in a string, comma separated.
  + allowedNames : 

    + PHP reserved names that can be used in the code. All in a string, comma separated.
:ref:`Too Many Native Calls <too-many-native-calls>`
  + nativeCallCounts : 3

    + Number of native calls found inside another call.
:ref:`Keep Files Access Restricted <keep-files-access-restricted>`
  + filePrivileges : 0777

    + List of forbidden file modes (comma separated).
:ref:`Should Use Prepared Statement <should-use-prepared-statement>`
  + queryMethod : query_methods.json

    + Methods that call a query.
:ref:`Too Complex Expression <too-complex-expression>`
  + complexExpressionThreshold : 30

    + Minimal number of operators in one expression to report.
:ref:`Long Arguments <long-arguments>`
  + codeTooLong : 100

    + Minimum size of a functioncall or a methodcall to be considered too long.
:ref:`Too Long A Block <too-long-a-block>`
  + longBlock : 200

    + Size of a block for it to be too long. A block is commanded by a for, foreach, while, do...while, if/then else structure.
:ref:`Max Level Of Nesting <max-level-of-nesting>`
  + maxLevel : 4

    + Maximum level of nesting for control flow structures in one scope. 
:ref:`Nested Ifthen <nested-ifthen>`
  + nestedIfthen : 3

    + Maximal number of acceptable nesting of if-then structures
:ref:`@ Operator <@-operator>`
  + authorizedFunctions : noscream_functions.json

    + Functions that are authorized to sports a @.
:ref:`Duplicate Literal <duplicate-literal>`
  + minDuplicate : 15

    + Minimal number of duplication before the literal is reported.
:ref:`Selector <selector>`
  + selector : 

    + A selector expression to identify atoms in the code.
:ref:`Variables With Long Names <variables-with-long-names>`
  + variableLength : 20

    + Minimum size of a long variable name, including the initial $.


    

Check Install
-------------

Once the prerequisite are installed, it is advised to run to check if all is found : 

`php exakat.phar doctor`

After this run, you may edit 'config/config.ini' to change some of the default values. Most of the time, the default values will be OK for a quick start.
