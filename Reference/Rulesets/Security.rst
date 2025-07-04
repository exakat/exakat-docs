.. _ruleset-security:

Security
++++++++

.. meta::
	:description:
		Security: Check the code for common security bad practices, especially in the Web environnement..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Security
	:twitter:description: Security: Check the code for common security bad practices, especially in the Web environnement.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Security
	:og:type: article
	:og:description: Check the code for common security bad practices, especially in the Web environnement.
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/Security.html
	:og:locale: en

This ruleset focuses on code security. 

Total : 47 analysis

* :ref:`structures-evalusage`
* :ref:`structures-phpinfousage`
* :ref:`structures-vardumpusage`
* :ref:`functions-hardcodedpasswords`
* :ref:`security-directinjection`
* :ref:`security-nosleep`
* :ref:`security-parseurlwithoutparameters`
* :ref:`security-avoidthosecrypto`
* :ref:`structures-nohardcodedport`
* :ref:`security-shouldusepreparedstatement`
* :ref:`structures-nohardcodedip`
* :ref:`security-comparehash`
* :ref:`structures-pregoptione`
* :ref:`structures-evalwithouttry`
* :ref:`security-registerglobals`
* :ref:`security-curloptions`
* :ref:`php-betterrand`
* :ref:`structures-nohardcodedhash`
* :ref:`structures-randomwithouttry`
* :ref:`security-indirectinjection`
* :ref:`security-unserializesecondarg`
* :ref:`security-dontechoerror`
* :ref:`security-shouldusesessionregenerateid`
* :ref:`security-encodedletters`
* :ref:`security-setcookieargs`
* :ref:`structures-noreturninfinally`
* :ref:`security-mkdirdefault`
* :ref:`structures-fallthrough`
* :ref:`security-uploadfilenameinjection`
* :ref:`security-anchorregex`
* :ref:`security-sessionlazywrite`
* :ref:`security-sqlite3requiressinglequotes`
* :ref:`security-nonetforxmlload`
* :ref:`security-dynamicdl`
* :ref:`security-configureextract`
* :ref:`security-moveuploadedfile`
* :ref:`security-filterinputsource`
* :ref:`security-safehttpheaders`
* :ref:`security-integerconversion`
* :ref:`security-minusoneonerror`
* :ref:`security-noentignore`
* :ref:`security-noweaksslcrypto`
* :ref:`security-keepfilesrestricted`
* :ref:`security-cryptokeylength`
* :ref:`security-incompatibletypeswithincoming`
* :ref:`security-filternotraw`
* :ref:`security-sessioncacheddata`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-ambassador`, :ref:`report-owasp`                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


