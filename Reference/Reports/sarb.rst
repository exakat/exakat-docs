.. _report-sarb:

Sarb
++++

Sarb
____

The Sarb report is a compatibility report with SARB

`SARB <https://github.com/DaveLiddament/sarb>`_ is the Static Analysis Results Baseliner. SARB is used to create a baseline of these results. As work on the project progresses SARB can takes the latest static analysis results, removes those issues in the baseline and report the issues raised since the baseline. SARB does this, in conjunction with git, by tracking lines of code between commits. SARB is the brainchild of `Dave Liddament <https://twitter.com/DaveLiddament>`_. 




::

    [
        {
            "type": "Classes\/NonPpp",
            "file": "\/home\/exakat\/elation\/code\/include\/base_class.php",
            "line": 37
        },
        {
            "type": "Structures\/NoSubstrOne",
            "file": "\/home\/exakat\/elation\/code\/include\/common_funcs.php",
            "line": 890
        },
        {
            "type": "Structures\/DropElseAfterReturn",
            "file": "\/home\/exakat\/elation\/code\/include\/smarty\/SmartyValidate.class.php",
            "line": 638
        },
        {
            "type": "Variables\/UndefinedVariable",
            "file": "\/home\/exakat\/elation\/code\/components\/ui\/ui.php",
            "line": 174
        },
        {
            "type": "Functions\/TooManyLocalVariables",
            "file": "\/home\/exakat\/elation\/code\/include\/dependencymanager_class.php",
            "line": 43
        }
    ]

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Sarb                                                             |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Json                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.sarb.json'.                    |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


