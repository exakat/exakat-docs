.. _ruleset-inventory:

Inventory
+++++++++

.. meta::
	:description:
		Inventory: A set of rules that collect various definitions from the code .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inventory
	:twitter:description: Inventory: A set of rules that collect various definitions from the code 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inventory
	:og:type: article
	:og:description: A set of rules that collect various definitions from the code 
	:og:url: https://exakat.readthedocs.io/en/latest/Rulesets/Inventory.html
	:og:locale: en

This ruleset collect all free-text names used in the code : variables, global, arguments, methods, classes, etc...

For example : 

+ Classes/MagicProperties
+ Constants/Constantnames : names of global Constants
+ Php/CookieVariables : names of cookies
+ Php/DateFormats : date formats
+ Php/IncomingVariables : names of the GET/POST arguments
+ Php/SessionVariables : names of the session variables
+ Type/ArrayIndex : indices used in arrays
+ Type/Binary : binary values
+ Type/CharString : string values
+ Type/Email : hardcoded emails
+ Type/GPCIndex : GET, POST and COOKIE names
+ Type/Hexadecimal : hexadecimal values
+ Type/HexadecimalString : hexadecimal values
+ Type/HttpHeader : HTTP headers
+ Type/HttpStatus : HTTP status
+ Type/Md5String : MD5 string
+ Type/MimeType : Mime types
+ Type/OctalInString : octal values
+ Type/OpensslCipher : names of OpenSSL cipher 
+ Type/Pack : pack() formats
+ Type/Pcre : regex strings
+ Type/Ports : server ports mentioned
+ Type/Printf : printf() and co formatting strings
+ Type/Regex : regex strings
+ Type/SpecialIntegers : integer, with special values
+ Type/Sql : SQL strings
+ Type/UdpDomains : UDP domains
+ Type/UnicodeBlock : Unicode blocks
+ Type/Url : URL



Total : 39 analysis

* :ref:`constants-names`
* :ref:`binary-glossary`
* :ref:`email-addresses`
* :ref:`heredoc-delimiter-glossary`
* :ref:`hexadecimal-glossary`
* :ref:`http-headers`
* :ref:`http-status-code`
* :ref:`md5-strings`
* :ref:`mime-types`
* :ref:`perl-regex`
* :ref:`internet-ports`
* :ref:`special-integers`
* :ref:`all-strings`
* :ref:`unicode-blocks`
* :ref:`url-list`
* :ref:`hexadecimal-in-string`
* :ref:`relay-function`
* :ref:`invalid-octal-in-string`
* :ref:`sql-queries`
* :ref:`regex-inventory`
* :ref:`switch-fallthrough`
* :ref:`session-variables`
* :ref:`incoming-variables`
* :ref:`cookies-variables`
* :ref:`date-formats`
* :ref:`type-array-index`
* :ref:`incoming-variable-index-inventory`
* :ref:`pack-format-inventory`
* :ref:`printf-format-inventory`
* :ref:`multiple-identical-closure`
* :ref:`magic-properties`
* :ref:`internet-domains`
* :ref:`openssl-ciphers-used`
* :ref:`promoted-properties`
* :ref:`extends-stdclass`
* :ref:`incoming-date-formats`
* :ref:`ip`
* :ref:`init-then-update`
* :ref:`relay-constant`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Inventory                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


