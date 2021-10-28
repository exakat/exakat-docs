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



    

Check Install
-------------

Once the prerequisite are installed, it is advised to run to check if all is found : 

`php exakat.phar doctor`

After this run, you may edit 'config/config.ini' to change some of the default values. Most of the time, the default values will be OK for a quick start.
