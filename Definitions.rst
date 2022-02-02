.. Definitions:

Glossary
============

Here is a list of words, commonly used when using Exakat, with their definitions and their synonyms. 


+ `A`
    `Analysis`
        An `Analysis` is a pattern that may be detected in the code. The analysis has a human-redable description,  and a specific implementation.

    `AST`
        The Abstract Syntax Tree : a representation of the PHP code as a graph. The AST is the first consisten organisation of the PHP tokens, after tokenization. 

    `Audit`
        An `Audit` is the result of a set of Rules being run on a piece of code. The shape of the audit is the `Report`.

+ `B`
    `Bug`
        A bug is a software malfunction, which leads to undesirable output, including the halt of the execution without results.

+ `C`
    `CIT`
        Acronym for Class-Interface-Trait. Sometimes, this includes also Enum, as `CITE`. All those structures share the same namespace.

    `CITE`
        Acronym for Class-Interface-Trait-Enum. Sometimes, this excludes also Enum, as `CIT`.

    `Cobbler`
        The Exakat command to modify a piece of code.

    `CPM`
        Acronym for Constant-Property-Method.

+ `D`
    `Directive`
        A configuration option.

    `Dump`
        The phase of execution, which prepare the results from the graph database to the data storage for reports.

+ `I`
    `Initialisation`
        Set up of a data space by giving it a preset value.

    `Inventory`
        The collections of all the different values of a specific type of data, observed or measured. For example, variable names, functioncall frequency, or methods's length.
        
    `Issue`
        The result of an analysis, when an analysis is applied to a code. 

+ `L`
    `Load`
        The phase of execution, which loads the source code into the central database.

    `Lint`
        The PHP execution phase, where the text file is read, and turned into tokens and checked for consistency. 

+ `N`
    `Nullsafe`
        A nullsafe operator is able to carry a function or fail graciously. In particular, it won't stop the execution with a fatal error. For example, the null-safe operator `?->` or coalesce `??`

+ `R`
    `Report`
        A set of issues, gathered into a consistent format, after running the analysis on the code. A report may include multiple rulesets, and use various format, such as HTML, JSON or Text.

    `Rule`
        A synonym for Analysis. This may be more descriptive, and less related to implementation.

    `Ruleset`
        A consistent group of analysis, recognizable with a specific name.

+ `S`
    `Stubs`
        Stubs are a set of PHP files which provide the methods, classes and interfaces signature for a library or component. The actual code is not provided, as the important information lies in the signature.

+ `T`
    `Token`
        The atomic element of information in a PHP script. The PHP code is broken down into tokens, such as 123 or 'if' and then organized in a consisten AST before execution.

