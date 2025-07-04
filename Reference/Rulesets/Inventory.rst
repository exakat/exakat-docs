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

* :ref:`constants-constantnames`
* :ref:`type-binary`
* :ref:`type-email`
* :ref:`type-heredoc`
* :ref:`type-hexadecimal`
* :ref:`type-httpheader`
* :ref:`type-httpstatus`
* :ref:`type-md5string`
* :ref:`type-mimetype`
* :ref:`type-pcre`
* :ref:`type-ports`
* :ref:`type-specialintegers`
* :ref:`type-charstring`
* :ref:`type-unicodeblock`
* :ref:`type-url`
* :ref:`type-hexadecimalstring`
* :ref:`functions-relayfunction`
* :ref:`type-octalinstring`
* :ref:`type-sql`
* :ref:`type-regex`
* :ref:`structures-fallthrough`
* :ref:`php-sessionvariables`
* :ref:`php-incomingvariables`
* :ref:`php-cookiesvariables`
* :ref:`php-dateformats`
* :ref:`type-arrayindex`
* :ref:`type-gpcindex`
* :ref:`type-pack`
* :ref:`type-printf`
* :ref:`functions-multipleidenticalclosure`
* :ref:`classes-magicproperties`
* :ref:`type-udpdomains`
* :ref:`type-opensslcipher`
* :ref:`classes-promotedproperties`
* :ref:`classes-extendsstdclass`
* :ref:`type-incomingdateformat`
* :ref:`type-ip`
* :ref:`structures-initthenif`
* :ref:`constants-relayconstant`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Inventory                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-inventories`                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


