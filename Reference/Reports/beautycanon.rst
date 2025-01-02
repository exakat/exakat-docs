.. _report-beautycanon:

BeautyCanon
+++++++++++

BeautyCanon
___________

.. meta::
	:description:
		BeautyCanon: The Beauty Canon report lists all rules that report no issues..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: BeautyCanon
	:twitter:description: BeautyCanon: The Beauty Canon report lists all rules that report no issues.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: BeautyCanon
	:og:type: article
	:og:description: The Beauty Canon report lists all rules that report no issues.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Beauty Canon report lists all rules that report no issues.

The Beauty Canon report displays one result per line. This report lists all issues in the provided ruleset that are reporting no error.

The title of the analysis is listed on the left, and the analysis short name is listed on the right, for further documentation.

This analysis uses "Analysis" as default rule. It may otherwise configured with the -T option.




::

    Compare Hash                                                           Security/CompareHash                    
    Configure Extract                                                      Security/ConfigureExtract               
    Dynamic Library Loading                                                Security/DynamicDl                      
    Encoded Simple Letters                                                 Security/EncodedLetters                 
    Indirect Injection                                                     Security/IndirectInjection              
    Integer Conversion                                                     Security/IntegerConversion              
    Minus One On Error                                                     Security/MinusOneOnError                
    Mkdir Default                                                          Security/MkdirDefault                   
    No ENT_IGNORE                                                          Security/NoEntIgnore                    
    No Hardcoded Hash                                                      Structures/NoHardcodedHash              
    No Hardcoded Ip                                                        Structures/NoHardcodedIp                
    No Hardcoded Port                                                      Structures/NoHardcodedPort              
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | BeautyCanon                                                      |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written to the standard output.                   |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


