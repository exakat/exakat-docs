.. Annex:

Annex
=====

* Supported Rulesets
* Supported Reports
* Supported PHP Extensions
* Supported Frameworks
* Applications
* Recognized Libraries
* New analyzers
* External services
* PHP Error messages
* Exakat Changelog

Supported Rulesets
------------------

Exakat groups analysis by rulesets. This way, analyzing 'Security' runs all possible analysis related to security. One analysis may belong to multiple rulesets.

* All
* Analyze
* Appcontent
* Appinfo
* CI-checks
* Calisthenics
* ClassReview
* ClearPHP
* Coding Conventions
* CompatibilityPHP53
* CompatibilityPHP54
* CompatibilityPHP55
* CompatibilityPHP56
* CompatibilityPHP70
* CompatibilityPHP71
* CompatibilityPHP72
* CompatibilityPHP73
* CompatibilityPHP74
* CompatibilityPHP80
* Complete
* Custom
* Dead code
* DefensiveProgrammingTM
* Dismell
* Dump
* First
* Internal
* Inventory
* Level 1
* Level 2
* Level 3
* Level 4
* Level 5
* LintButWontExec
* Newfeatures
* None
* OneFile
* PHP recommendations
* Performances
* Portability
* Preferences
* RadwellCodes
* Rector
* SOLID
* Security
* Semantics
* Simple
* Stats
* Suggestions
* Top10
* Typechecks
* Typehints
* Unassigned
* Under Work
* php-cs-fixable

Supported Reports
-----------------

Exakat produces various reports. Some are general, covering various aspects in a reference way; others focus on one aspect. 

  * Ambassador
  * Ambassadornomenu
  * Drillinstructor
  * Top10
  * Text
  * Xml
  * Uml
  * Yaml
  * Plantuml
  * None
  * Simplehtml
  * Owasp
  * Perfile
  * Beautycanon
  * Phpconfiguration
  * Phpcompilation
  * Favorites
  * Manual
  * Inventories
  * Clustergrammer
  * Filedependencies
  * Filedependencieshtml
  * Classdependencies
  * Stubs
  * StubsJson
  * Radwellcode
  * Grade
  * Weekly
  * Scrutinizer
  * Codesniffer
  * Phpcsfixer
  * Facetedjson
  * Json
  * Onepagejson
  * Marmelab
  * Simpletable
  * Exakatyaml
  * Codeflower
  * Dependencywheel
  * Phpcity
  * Sarb
  * Exakatvendors
  * Topology
  * Migration73
  * Migration74
  * Migration80
  * Meters


Supported PHP Extensions
------------------------

PHP extensions are used to check for structures usage (classes, interfaces, etc.), to identify dependencies and directives. 

PHP extensions are described with the list of structures they define : functions, classes, constants, traits, variables, interfaces, namespaces, and directives. 

* `ext/amqp <https://github.com/alanxz/rabbitmq-c>`_
* `ext/apache <https://www.php.net/manual/en/book.apache.php>`_
* `ext/apc <https://www.php.net/apc>`_
* `ext/apcu <http://www.php.net/manual/en/book.apcu.php>`_
* `ext/array <https://www.php.net/manual/en/book.array.php>`_
* `ext/php-ast <https://pecl.php.net/package/ast>`_
* `ext/async <https://github.com/concurrent-php/ext-async>`_
* `ext/bcmath <http://www.php.net/bcmath>`_
* `ext/bzip2 <https://www.php.net/bzip2>`_
* `ext/cairo <https://cairographics.org/>`_
* `ext/calendar <http://www.php.net/manual/en/ref.calendar.php>`_
* `ext/cmark <https://github.com/commonmark/cmark>`_
* `ext/com <https://www.php.net/manual/en/book.com.php>`_
* `ext/crypto <https://pecl.php.net/package/crypto>`_
* `ext/csprng <https://www.php.net/manual/en/book.csprng.php>`_
* `ext/ctype <https://www.php.net/manual/en/ref.ctype.php>`_
* `ext/curl <https://www.php.net/manual/en/book.curl.php>`_
* `ext/cyrus <https://www.php.net/manual/en/book.cyrus.php>`_
* `ext/date <https://www.php.net/manual/en/book.datetime.php>`_
* `ext/db2 <https://www.php.net/manual/en/book.ibm-db2.php>`_
* `ext/dba <https://www.php.net/manual/en/book.dba.php>`_
* `ext/decimal <http://php-decimal.io>`_
* `ext/dio <https://www.php.net/manual/en/refs.fileprocess.file.php>`_
* `ext/dom <https://www.php.net/manual/en/book.dom.php>`_
* `ext/ds <http://docs.php.net/manual/en/book.ds.php>`_
* `ext/eaccelerator <http://eaccelerator.net/>`_
* `ext/eio <http://software.schmorp.de/pkg/libeio.html>`_
* `ext/enchant <https://www.php.net/manual/en/book.enchant.php>`_
* `ext/ereg <https://www.php.net/manual/en/function.ereg.php>`_
* `ext/ev <https://www.php.net/manual/en/book.ev.php>`_
* `ext/event <https://www.php.net/event>`_
* `ext/exif <https://www.php.net/manual/en/book.exif.php>`_
* `ext/expect <https://www.php.net/manual/en/book.expect.php>`_
* `ext/fam <http://oss.sgi.com/projects/fam/>`_
* `ext/fann <https://www.php.net/manual/en/book.fann.php>`_
* `ext/fdf <http://www.adobe.com/devnet/acrobat/fdftoolkit.html>`_
* `ext/ffi <https://www.php.net/manual/en/book.ffi.php>`_
* `ext/ffmpeg <http://ffmpeg-php.sourceforge.net/>`_
* `ext/file <http://www.php.net/manual/en/book.filesystem.php>`_
* `ext/fileinfo <https://www.php.net/manual/en/book.fileinfo.php>`_
* `ext/filter <https://www.php.net/manual/en/book.filter.php>`_
* `ext/fpm <https://www.php.net/fpm>`_
* `ext/ftp <http://www.faqs.org/rfcs/rfc959>`_
* `ext/gd <https://www.php.net/manual/en/book.image.php>`_
* `ext/gearman <https://www.php.net/manual/en/book.gearman.php>`_
* `ext/gender <https://www.php.net/manual/en/book.gender.php>`_
* `ext/geoip <https://www.php.net/manual/en/book.geoip.php>`_
* `ext/gettext <https://www.gnu.org/software/gettext/manual/gettext.html>`_
* `ext/gmagick <http://www.php.net/manual/en/book.gmagick.php>`_
* `ext/gmp <https://www.php.net/manual/en/book.gmp.php>`_
* `ext/gnupgp <http://www.php.net/manual/en/book.gnupg.php>`_
* `ext/grpc <http://www.grpc.io/>`_
* `ext/hash <http://www.php.net/manual/en/book.hash.php>`_
* `ext/hrtime <https://www.php.net/manual/en/intro.hrtime.php>`_
* `ext/pecl_http <https://github.com/m6w6/ext-http>`_
* `ext/ibase <https://www.php.net/manual/en/book.ibase.php>`_
* `ext/iconv <https://www.php.net/iconv>`_
* `ext/igbinary <https://github.com/igbinary/igbinary/>`_
* `ext/iis <http://www.php.net/manual/en/book.iisfunc.php>`_
* `ext/imagick <https://www.php.net/manual/en/book.imagick.php>`_
* `ext/imap <http://www.php.net/imap>`_
* `ext/info <https://www.php.net/manual/en/book.info.php>`_
* `ext/inotify <https://www.php.net/manual/en/book.inotify.php>`_
* `ext/intl <http://site.icu-project.org/>`_
* `ext/json <http://www.faqs.org/rfcs/rfc7159>`_
* `ext/judy <http://judy.sourceforge.net/>`_
* `ext/kdm5 <https://www.php.net/manual/en/book.kadm5.php>`_
* `ext/lapack <https://www.php.net/manual/en/book.lapack.php>`_
* `ext/ldap <https://www.php.net/manual/en/book.ldap.php>`_
* `ext/leveldb <https://github.com/reeze/php-leveldb>`_
* `ext/libevent <http://www.libevent.org/>`_
* `ext/libsodium <https://github.com/jedisct1/libsodium-php>`_
* `ext/libxml <http://www.php.net/manual/en/book.libxml.php>`_
* `ext/lua <https://www.php.net/manual/en/book.lua.php>`_
* `ext/lzf <https://www.php.net/lzf>`_
* `ext/mail <http://www.php.net/manual/en/book.mail.php>`_
* `ext/mailparse <http://www.faqs.org/rfcs/rfc822.html>`_
* `ext/math <https://www.php.net/manual/en/book.math.php>`_
* `ext/mbstring <http://www.php.net/manual/en/book.mbstring.php>`_
* `ext/mcrypt <http://www.php.net/manual/en/book.mcrypt.php>`_
* `ext/memcache <http://www.php.net/manual/en/book.memcache.php>`_
* `ext/memcached <https://www.php.net/manual/en/book.memcached.php>`_
* `ext/mhash <http://mhash.sourceforge.net/>`_
* `ext/ming <http://www.libming.org/>`_
* `ext/mongo <https://www.php.net/mongo>`_
* `ext/mongodb <https://github.com/mongodb/mongo-c-driver>`_
* `ext/msgpack <https://github.com/msgpack/msgpack-php>`_
* `ext/mssql <http://www.php.net/manual/en/book.mssql.php>`_
* `ext/mysql <http://www.php.net/manual/en/book.mysql.php>`_
* `ext/mysqli <https://www.php.net/manual/en/book.mysqli.php>`_
* `ext/ncurses <https://www.php.net/manual/en/book.ncurses.php>`_
* `ext/newt <http://people.redhat.com/rjones/ocaml-newt/html/Newt.html>`_
* `ext/nsapi <https://www.php.net/manual/en/install.unix.sun.php>`_
* `ext/ob <https://www.php.net/manual/en/book.outcontrol.php>`_
* `ext/oci8 <https://www.php.net/manual/en/book.oci8.php>`_
* `ext/odbc <http://www.php.net/manual/en/book.uodbc.php>`_
* `ext/opcache <http://www.php.net/manual/en/book.opcache.php>`_
* `ext/opencensus <https://github.com/census-instrumentation/opencensus-php>`_
* `ext/openssl <https://www.php.net/manual/en/book.openssl.php>`_
* `ext/parle <https://www.php.net/manual/en/book.parle.php>`_
* `ext/parsekit <http://www.php.net/manual/en/book.parsekit.php>`_
* `ext/password <https://www.php.net/manual/en/book.password.php>`_
* `ext/pcntl <https://www.php.net/manual/en/book.pcntl.php>`_
* `ext/pcov <https://github.com/krakjoe/pcov>`_
* `ext/pcre <https://www.php.net/manual/en/book.pcre.php>`_
* `ext/pdo <https://www.php.net/manual/en/book.pdo.php>`_
* `ext/pgsql <https://www.php.net/manual/en/book.pgsql.php>`_
* `ext/phalcon <https://docs.phalconphp.com/en/latest/reference/tutorial.html>`_
* `ext/phar <http://www.php.net/manual/en/book.phar.php>`_
* `ext/posix <https://standards.ieee.org/findstds/standard/1003.1-2008.html>`_
* `ext/proctitle <https://www.php.net/manual/en/book.proctitle.php>`_
* `ext/pspell <https://www.php.net/manual/en/book.pspell.php>`_
* `ext/psr <https://www.php-fig.org/psr/psr-3>`_
* `ext/rar <https://www.php.net/manual/en/book.rar.php>`_
* `ext/rdkafka <https://github.com/arnaud-lb/php-rdkafka>`_
* `ext/readline <https://www.php.net/manual/en/book.readline.php>`_
* `ext/recode <http://www.php.net/manual/en/book.recode.php>`_
* `ext/redis <https://github.com/phpredis/phpredis/>`_
* `ext/reflection <https://www.php.net/manual/en/book.reflection.php>`_
* `ext/runkit <https://www.php.net/manual/en/book.runkit.php>`_
* `ext/sdl <https://github.com/Ponup/phpsdl>`_
* `ext/seaslog <https://github.com/SeasX/SeasLog>`_
* `ext/sem <https://www.php.net/manual/en/book.sem.php>`_
* `ext/session <https://www.php.net/manual/en/book.session.php>`_
* `ext/shmop <https://www.php.net/manual/en/book.sem.php>`_
* `ext/simplexml <https://www.php.net/manual/en/book.simplexml.php>`_
* `ext/snmp <http://www.net-snmp.org/>`_
* `ext/soap <https://www.php.net/manual/en/book.soap.php>`_
* `ext/sockets <https://www.php.net/manual/en/book.sockets.php>`_
* `ext/sphinx <https://www.php.net/manual/en/book.sphinx.php>`_
* `ext/spl <http://www.php.net/manual/en/book.spl.php>`_
* `ext/sqlite <https://www.php.net/manual/en/book.sqlite.php>`_
* `ext/sqlite3 <https://www.php.net/manual/en/book.sqlite3.php>`_
* `ext/sqlsrv <https://www.php.net/sqlsrv>`_
* `ext/ssh2 <https://www.php.net/manual/en/book.ssh2.php>`_
* `ext/standard <https://www.php.net/manual/en/ref.info.php>`_
* `ext/stats <https://people.sc.fsu.edu/~jburkardt/c_src/cdflib/cdflib.html>`_
* `String <https://www.php.net/manual/en/ref.strings.php>`_
* `ext/suhosin <https://suhosin.org/>`_
* `ext/svm <http://www.php.net/svm>`_
* `ext/swoole <https://www.swoole.com/>`_
* `ext/tidy <https://www.php.net/manual/en/book.tidy.php>`_
* `ext/tokenizer <http://www.php.net/tokenizer>`_
* `ext/tokyotyrant <https://www.php.net/manual/en/book.tokyo-tyrant.php>`_
* `ext/trader <https://pecl.php.net/package/trader>`_
* `ext/uopz <https://pecl.php.net/package/uopz>`_
* `ext/uuid <https://linux.die.net/man/3/libuuid>`_
* `ext/v8js <https://bugs.chromium.org/p/v8/issues/list>`_
* `ext/varnish <https://www.php.net/manual/en/book.varnish.php>`_
* `ext/vips <https://github.com/jcupitt/php-vips-ext>`_
* `ext/wasm <https://github.com/Hywan/php-ext-wasm>`_
* `ext/wddx <https://www.php.net/manual/en/intro.wddx.php>`_
* `ext/weakref <https://www.php.net/manual/en/book.weakref.php>`_
* `ext/wikidiff2 <https://www.mediawiki.org/wiki/Extension:Wikidiff2>`_
* `ext/wincache <http://www.php.net/wincache>`_
* `ext/xattr <https://www.php.net/manual/en/book.xattr.php>`_
* `ext/xcache <https://xcache.lighttpd.net/>`_
* `ext/xdebug <https://xdebug.org/>`_
* `ext/xdiff <https://www.php.net/manual/en/book.xdiff.php>`_
* `ext/xhprof <http://web.archive.org/web/20110514095512/http://mirror.facebook.net/facebook/xhprof/doc.html>`_
* `ext/xml <http://www.php.net/manual/en/book.xml.php>`_
* `ext/xmlreader <http://www.php.net/manual/en/book.xmlreader.php>`_
* `ext/xmlrpc <http://www.php.net/manual/en/book.xmlrpc.php>`_
* `ext/xmlwriter <https://www.php.net/manual/en/book.xmlwriter.php>`_
* `ext/xsl <https://www.php.net/manual/en/intro.xsl.php>`_
* `ext/xxtea <https://pecl.php.net/package/xxtea>`_
* `ext/yaml <http://www.yaml.org/>`_
* `ext/yis <http://www.tldp.org/HOWTO/NIS-HOWTO/index.html>`_
* `ext/zbarcode <https://github.com/mkoppanen/php-zbarcode>`_
* `ext/zend_monitor <http://files.zend.com/help/Zend-Server/content/zendserverapi/zend_monitor-php_api.htm>`_
* `ext/zip <https://www.php.net/manual/en/book.zip.php>`_
* `ext/zlib <https://www.php.net/manual/en/book.zlib.php>`_
* `ext/0mq <http://zeromq.org/>`_
* `ext/zookeeper <https://www.php.net/zookeeper>`_

Supported Frameworks
--------------------

Frameworks, components and libraries are supported via Exakat extensions.

List of extensions : there are 10 extensions

* :ref:`Cakephp <extension-cakephp>`
* :ref:`Drupal <extension-drupal>`
* :ref:`Laravel <extension-laravel>`
* :ref:`Pmb <extension-pmb>`
* :ref:`Prestashop <extension-prestashop>`
* :ref:`Shopware <extension-shopware>`
* :ref:`Slim <extension-slim>`
* :ref:`Symfony <extension-symfony>`
* :ref:`Wordpress <extension-wordpress>`
* :ref:`ZendF <extension-zendf>`





Applications
------------

A number of applications were scanned in order to find real life examples of patterns. They are listed here : 

* `ChurchCRM <http://churchcrm.io/>`_
* `Cleverstyle <https://cleverstyle.org/en>`_
* `Contao <https://contao.org/en/>`_
* `Dolibarr <https://www.dolibarr.org/>`_
* `Dolphin <https://www.boonex.com/>`_
* `Edusoho <https://www.edusoho.com/en>`_
* `ExpressionEngine <https://expressionengine.com/>`_
* `FuelCMS <https://www.getfuelcms.com/>`_
* `HuMo-Gen <http://humogen.com/>`_
* `LiveZilla <https://www.livezilla.net/home/en/>`_
* `Magento <https://magento.com/>`_
* `Mautic <https://www.mautic.org/>`_
* `MediaWiki <https://www.mediawiki.org/>`_
* `NextCloud <https://nextcloud.com/>`_
* `OpenConf <https://www.openconf.com/>`_
* `OpenEMR <https://www.open-emr.org/>`_
* `Phinx <https://phinx.org/>`_
* `PhpIPAM <https://phpipam.net/download/>`_
* `Phpdocumentor <https://www.phpdoc.org/>`_
* `Piwigo <https://www.piwigo.org/>`_
* `PrestaShop <https://prestashop.com/>`_
* `SPIP <https://www.spip.net/>`_
* `SugarCrm <https://www.sugarcrm.com/>`_
* `SuiteCrm <https://suitecrm.com/>`_
* `TeamPass <https://teampass.net/>`_
* `Thelia <https://thelia.net/>`_
* `ThinkPHP <http://www.thinkphp.cn/>`_
* `Tikiwiki <https://tiki.org/>`_
* `Tine20 <https://www.tine20.com/>`_
* `Traq <https://traq.io/>`_
* `Typo3 <https://typo3.org/>`_
* `Vanilla <https://open.vanillaforums.com/>`_
* `Woocommerce <https://woocommerce.com/>`_
* `WordPress <https://www.wordpress.org/>`_
* `XOOPS <https://xoops.org/>`_
* `Zencart <https://www.zen-cart.com/>`_
* `Zend-Config <https://docs.zendframework.com/zend-config/>`_
* `Zurmo <http://zurmo.org/>`_
* `opencfp <https://github.com/opencfp/opencfp>`_
* `phpMyAdmin <https://www.phpmyadmin.net/>`_
* `phpadsnew <http://freshmeat.sourceforge.net/projects/phpadsnew>`_
* `shopware <https://www.shopware.com/>`_
* `xataface <http://xataface.com/>`_


Recognized Libraries
--------------------

Libraries that are popular, large and often included in repositories are identified early in the analysis process, and ignored. This prevents Exakat to analysis some code foreign to the current repository : it prevents false positives from this code, and make the analysis much lighter. The whole process is entirely automatic. 

Those libraries, or even some of the, may be included again in the analysis by commenting the ignored_dir[] line, in the projects/<project>/config.ini file. 

* `ADOdb <https://adodb.org/dokuwiki/doku.php/>`_
* `atoum <http://atoum.org/>`_
* `BBQ <https://github.com/eventio/bbq>`_
* `CakePHP <https://cakephp.org/>`_
* `CI xmlRPC <http://apigen.juzna.cz/doc/ci-bonfire/Bonfire/class-CI_Xmlrpc.html>`_
* `CPDF <https://pear.php.net/reference/PhpDocumentor-latest/li_Cpdf.html>`_
* `Codeception <https://codeception.com/>`_
* `DomPDF <https://github.com/dompdf/dompdf>`_
* `FPDF <http://www.fpdf.org/>`_
* `phpGACL <http://phpgacl.sourceforge.net/>`_
* `gettext Reader <http://pivotx.net/dev/docs/trunk/External/PHP-gettext/gettext_reader.html>`_
* `jpGraph <http://jpgraph.net/>`_
* `HTML2PDF <http://sourceforge.net/projects/phphtml2pdf/>`_
* `HTML Purifier <http://htmlpurifier.org/>`_
* http_class
* `IDNA convert <https://github.com/phpWhois/idna-convert>`_
* `lessc <http://leafo.net/lessphp/>`_
* `magpieRSS <http://magpierss.sourceforge.net/>`_
* `MarkDown Parser <http://processwire.com/apigen/class-Markdown_Parser.html>`_
* `Markdown <https://github.com/michelf/php-markdown>`_
* `mpdf <http://www.mpdf1.com/mpdf/index.php>`_
* oauthToken
* passwordHash
* `pChart <http://www.pchart.net/>`_
* `pclZip <http://www.phpconcept.net/pclzip/>`_
* `Propel <http://propelorm.org/>`_
* `phpExecl <https://phpexcel.codeplex.com/>`_
* `phpMailer <https://github.com/PHPMailer/PHPMailer>`_
* `PHPSpec <http://www.phpspec.net/en/latest/>`_
* `PHPUnit <https://www.phpunit.de/>`_
* `qrCode <http://phpqrcode.sourceforge.net/>`_
* `Services_JSON <https://pear.php.net/package/Services_JSON>`_
* `sfYaml <https://github.com/fabpot-graveyard/yaml/blob/master/lib/sfYaml.php>`_
* `SimplePie <http://simplepie.org/>`_
* `SimpleTest <https://github.com/simpletest/simpletest>`_
* `swift <http://swiftmailer.org/>`_
* `Smarty <http://www.smarty.net/>`_
* `Symfony Unit Test <https://symfony.com/doc/current/testing.html>`_
* `tcpdf <http://www.tcpdf.org/>`_
* `text_diff <https://pear.php.net/package/Text_Diff>`_
* `text highlighter <https://pear.php.net/package/Text_Highlighter/>`_
* `tfpdf <http://www.fpdf.org/en/script/script92.php>`_
* `Typo3TestingFramework <https://github.com/TYPO3/testing-framework>`_
* UTF8
* `Xajax <https://github.com/Xajax/Xajax>`_
* `Yii <http://www.yiiframework.com/>`_
* `Zend Framework <http://framework.zend.com/>`_

New analyzers
-------------

List of analyzers, by version of introduction, newest to oldest. In parenthesis, the first element is the analyzer name, used with 'analyze -P' command, and the seconds, if any, are the ruleset, used with the -T option. Rulesets are separated by commas, as the same analysis may be used in several rulesets.


* 2.2.0

  * Cancelled Parameter (Functions/CancelledParameter ; Analyze)
  * Collect Block Size (Dump/CollectBlockSize)
  * Constant Typo Looks Like A Variable (Variables/ConstantTypo ; Analyze, OneFile)
  * PHP 80 Named Parameter Variadic (Php/Php80NamedParameterVariadic ; CompatibilityPHP80)
  * PHP Resources Turned Into Objects (Php/Php80RemovesResources ; CompatibilityPHP80)
  * Unused Exception Variable (Exceptions/UnusedExceptionVariable ; Suggestions)
  * Use str_contains() (Php/UseStrContains ; Suggestions)
  * Wrong Attribute Configuration (Php/WrongAttributeConfiguration ; Analyze)

* 2.1.9

  * Array_Fill() With Objects (Structures/ArrayFillWithObjects ; Analyze)
  * Assumptions (Php/Assumptions ; Analyze)
  * Complete/PhpExtStubPropertyMethod (Complete/PhpExtStubPropertyMethod ; Complete)
  * Could Be Stringable (Classes/CouldBeStringable ; Analyze, LintButWontExec)
  * Could Use Promoted Properties (Php/CouldUsePromotedProperties ; Suggestions)
  * Dump/CollectUseCOunts (Dump/CollectUseCounts ; Dump)
  * Modified Typed Parameter (Functions/ModifyTypedParameter ; Analyze, ClassReview)
  * Negative Start Index In Array (Arrays/NegativeStart)
  * Nullable With Constant (Functions/NullableWithConstant ; CompatibilityPHP80)
  * Optimize Explode() (Performances/OptimizeExplode ; Performances)
  * PHP 8.0 Removed Directives (Php/Php80RemovedDirective ; CompatibilityPHP80)
  * Unsupported Types With Operators (Structures/UnsupportedTypesWithOperators ; Analyze, CompatibilityPHP80)
  * Use get_debug_type() (Php/UseGetDebugType ; Suggestions)
  * Useless Typehint (Classes/UselessTypehint ; Suggestions, ClassReview)

* 2.1.8

  * $php_errormsg Usage (Php/PhpErrorMsgUsage ; CompatibilityPHP80)
  * Cancel Common Method (Classes/CancelCommonMethod)
  * Cast Unset Usage (Php/CastUnsetUsage ; CompatibilityPHP80)
  * Collect Atom Counts (Dump/CollectAtomCounts ; Dump)
  * Collect Classes Dependencies (Dump/CollectClassesDependencies ; Dump)
  * Collect Files Dependencies (Dump/CollectFilesDependencies ; Dump)
  * Collect Php Structures (Dump/CollectPhpStructures ; Dump)
  * Function With Dynamic Code (Functions/DynamicCode ; Internal)
  * Mismatch Parameter And Type (Functions/MismatchParameterAndType ; Analyze, Semantics)
  * Mismatch Parameter Name (Functions/MismatchParameterName ; Analyze, CompatibilityPHP80)
  * Multiple Declaration Of Strict_types (Php/MultipleDeclareStrict ; Analyze)

* 2.1.7

  * Collect Class Traits Counts (Dump/CollectClassTraitsCounts ; Dump)
  * Collect Native Calls Per Expressions (Dump/CollectNativeCallsPerExpressions ; Dump)
  * Collect Readability (Dump/CollectReadability ; Dump)
  * Collect Variables (Dump/CollectVariables ; Dump)
  * Could Be Parent Method (Classes/CouldBeParentMethod)
  * Don't Pollute Global Space (Php/DontPolluteGlobalSpace ; Analyze)
  * Dump/CollectDefinitionsStats (Dump/CollectDefinitionsStats ; Dump)
  * Dump/CollectGlobalVariables (Dump/CollectGlobalVariables ; Dump)
  * Missing Some Returntype (Typehints/MissingReturntype ; Analyze, Typehints, CI-checks)

* 2.1.6

  * Different Argument Counts (Classes/DifferentArgumentCounts)
  * GLOB_BRACE Usage (Portability/GlobBraceUsage ; Portability)
  * Iconv With Translit (Portability/IconvTranslit ; Portability)
  * Unknown Parameter Name (Functions/UnknownParameterName ; Analyze, CI-checks)
  * Use Closure Trailing Comma (Php/UseTrailingUseComma ; Appinfo)
  * Use NullSafe Operator (Php/UseNullSafeOperator ; Appinfo)
  * Use PHP Attributes (Php/UseAttributes ; Appinfo)

* 2.1.5

  * Abstract Away (Patterns/AbstractAway ; Suggestions)
  * Catch Undefined Variable (Exceptions/CatchUndefinedVariable ; Analyze)
  * Collect Parameter Names (Dump/CollectParameterNames ; Dump)
  * Dont Compare Typed Boolean (Structures/DontCompareTypedBoolean ; Suggestions)
  * Dump/CollectClassChanges (Dump/CollectClassChanges ; Dump)
  * Dump/FossilizedMethods (Dump/FossilizedMethods ; Dump)
  * Large Try Block (Exceptions/LargeTryBlock ; Suggestions)
  * Swapped Arguments (Classes/SwappedArguments)
  * Wrong Type For Native PHP Function (Php/WrongTypeForNativeFunction ; Analyze, CI-checks)

* 2.1.4

  * Array_merge Needs Array Of Arrays (Structures/ArrayMergeArrayArray ; Analyze)
  * Call Order (Dump/CallOrder ; Dump)
  * Could Be Float (Typehints/CouldBeFloat ; Typechecks, Typehints)
  * Could Be Integer (Typehints/CouldBeInt ; Typechecks, Typehints)
  * Could Be Iterable (Typehints/CouldBeIterable ; Typechecks, Typehints)
  * Extended Typehints (Complete/ExtendedTypehints ; Complete)
  * Mismatch Properties Typehints (Classes/MismatchProperties)
  * No Need For Triple Equal (Structures/NoNeedForTriple ; Analyze)
  * Php/UseMatch (Php/UseMatch ; CompatibilityPHP74)

* 2.1.3

  * Cyclic References (Classes/CyclicReferences)
  * Protocol lists (Type/Protocols ; Appinfo)
  * Wrong Argument Type (Functions/WrongArgumentType ; Analyze, Typechecks)

* 2.1.2

  * Collect Class Constant Counts (Dump/CollectClassConstantCounts)
  * Collect Local Variable Counts (Dump/CollectLocalVariableCounts ; Dump)
  * Collect Method Counts (Dump/CollectMethodCounts ; Dump)
  * Collect Property Counts (Dump/CollectPropertyCounts ; Dump)
  * Could Be Array Typehint (Typehints/CouldBeArray ; Typehints)
  * Could Be Boolean (Typehints/CouldBeBoolean ; Typehints)
  * Could Be CIT (Typehints/CouldBeCIT ; Typehints)
  * Could Be Callable (Typehints/CouldBeCallable ; Typechecks, Typehints)
  * Could Be Null (Typehints/CouldBeNull ; Typechecks, Typehints)
  * Could Be Parent (Typehints/CouldBeParent ; Typechecks, Typehints)
  * Could Be Self (Typehints/CouldBeSelf ; Typechecks, Typehints)
  * Could Be String (Typehints/CouldBeString ; Typechecks, Typehints)
  * Could Be Void (Typehints/CouldBeVoid ; Typechecks, Typehints)
  * Could Not Type (Typehints/CouldNotType ; Typehints)
  * Double Object Assignation (Structures/DoubleObjectAssignation ; Analyze, ClassReview)
  * Possible Alias Confusion (Namespaces/AliasConfusion ; Suggestions)
  * Safe Phpvariables (Php/SafePhpvars ; Internal)
  * Static Global Variables Confusion (Structures/SGVariablesConfusion ; Suggestions)
  * Too Long A Block (Structures/LongBlock ; Suggestions)
  * Too Much Indented (Functions/TooMuchIndented ; Suggestions)
  * Using Deprecated Method (Functions/UsingDeprecated ; Analyze)

* 2.1.1

  * Check Crypto Key Length (Security/CryptoKeyLength ; Security)
  * Dynamic Self Calls (Classes/DynamicSelfCalls)
  * Keep Files Access Restricted (Security/KeepFilesRestricted ; Security)
  * OpenSSL Ciphers Used (Type/OpensslCipher ; Inventory)
  * Prefix And Suffixes With Typehint (Functions/PrefixToType ; Semantics)
  * Throw Was An Expression (Php/ThrowWasAnExpression ; CompatibilityPHP72, CompatibilityPHP73, CompatibilityPHP74)
  * Undefined Constant Name (Variables/UndefinedConstantName ; Analyze)
  * Unused Trait In Class (Traits/UnusedClassTrait ; ClassReview)

* 2.1.0

  * Fn Argument Variable Confusion (Functions/FnArgumentVariableConfusion ; Analyze, Semantics)
  * Hidden Nullable (Classes/HiddenNullable)
  * Missing Abstract Method (Classes/MissingAbstractMethod ; Analyze, ClassReview)
  * Signature Trailing Comma (Php/SignatureTrailingComma ; CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73, CompatibilityPHP74)

* 2.0.9

  * Dont Collect Void (Functions/DontUseVoid ; Analyze)
  * Php 8.0 Only TypeHints (Php/Php80OnlyTypeHints ; Appinfo, CompatibilityPHP56, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73, CompatibilityPHP74)
  * Uninitilized Property (Classes/UninitedProperty)
  * Union Typehint (Php/Php80UnionTypehint ; Appinfo, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73, CompatibilityPHP74)
  * Wrong Typed Property Default (Classes/WrongTypedPropertyInit ; Analyze, LintButWontExec, ClassReview, CI-checks)

* 2.0.8

  * New Functions In PHP 8.0 (Php/Php80NewFunctions)
  * Php 8.0 Variable Syntax Tweaks (Php/Php80VariableSyntax ; Appinfo, CompatibilityPHP74)

* 2.0.7

  * Constant Order (Dump/ConstantOrder)

* 2.0.6

  * Fossilized Method (Classes/FossilizedMethod)
  * Links Between Parameter And Argument (Dump/ParameterArgumentsLinks ; Appinfo)
  * Not Equal Is Not !== (Structures/NotEqual ; Analyze, CI-checks)
  * Possible Interfaces (Interfaces/PossibleInterfaces ; Internal)

* 2.0.5

  * Missing Typehint (Functions/MissingTypehint)
  * Semantic Typing (Functions/SemanticTyping ; Semantics)

* 2.0.4

  * Coalesce Equal (Php/CoalesceEqual)

* 2.0.3

  * Collect Class Children Count (Dump/CollectClassChildren)
  * Collect Class Depth (Dump/CollectClassDepth ; Dump)
  * Collect Class Interface Counts (Dump/CollectClassInterfaceCounts ; Dump)
  * Exceeding Typehint (Functions/ExceedingTypehint ; ClassReview)

* 2.0.2

  * Dump/Inclusions (Dump/Inclusions ; Dump)
  * Dump/NewOrder (Dump/NewOrder ; Dump)
  * Insufficient Property Typehint (Classes/InsufficientPropertyTypehint)
  * Nullable Without Check (Functions/NullableWithoutCheck ; ClassReview)
  * Typehint Order (Dump/TypehintOrder ; )
  * Wrong Typehinted Name (Functions/WrongTypehintedName ; Coding Conventions, Semantics)

* 1.9.9

  * Collect Mbstring Encodings (Dump/CollectMbstringEncodings ; Dump)
  * Complete/CreateForeachDefault (Complete/CreateForeachDefault ; Complete)
  * Concrete usage (Vendors/Concrete5 ; Appinfo)
  * Could Type With Array (Functions/CouldTypeWithArray ; Under Work)
  * Could Type With Boolean (Functions/CouldTypeWithBool ; Under Work)
  * Could Type With Int (Functions/CouldTypeWithInt ; Under Work)
  * Could Type With Iterable (Functions/CouldTypeWithIterable ; Under Work)
  * Could Type With String (Functions/CouldTypeWithString ; Under Work)
  * Filter To add_slashes() (Php/FilterToAddSlashes ; CompatibilityPHP74)
  * Immutable Signature (Classes/ImmutableSignature ; Appinfo)
  * Is_A() With String (Php/IsAWithString ; Analyze, Simple, Rector, CI-checks)
  * Mbstring Third Arg (Structures/MbstringThirdArg ; Analyze, CI-checks)
  * Mbstring Unknown Encoding (Structures/MbstringUnknownEncoding ; Analyze, CI-checks)
  * Merge If Then (Structures/MergeIfThen ; Analyze, CI-checks)
  * Shell commands (Type/Shellcommands ; Appinfo)
  * Typehinting Stats (Dump/TypehintingStats ; Dump)
  * Typo 3 usage (Vendors/Typo3 ; Appinfo)
  * Weird Array Index (Arrays/WeirdIndex)
  * Wrong Case Namespaces (Namespaces/WrongCase ; Coding Conventions)
  * Wrong Type With Call (Functions/WrongTypeWithCall ; Analyze, Typechecks, CI-checks)

* 1.9.8

  * Cant Implement Traversable (Interfaces/CantImplementTraversable ; Analyze, LintButWontExec, CI-checks)
  * Parameter Hiding (Functions/ParameterHiding ; Semantics)
  * Propagate Calls (Complete/PropagateCalls)

* 1.9.7

  * Foreach() Favorite (Dump/CollectForeachFavorite ; Dump)
  * Make Functioncall With Reference (Complete/MakeFunctioncallWithReference ; Complete)
  * Too Many Dereferencing (Classes/TooManyDereferencing)
  * Use Url Query Functions (Structures/UseUrlQueryFunctions ; Suggestions)

* 1.9.6

  * Collect Parameter Counts (Dump/CollectParameterCounts ; Dump)
  * Create Magic Method (Complete/CreateMagicMethod ; )
  * Custom/NotInThisList (Custom/NotInThisList ; Under Work)
  * Dump/DereferencingLevels (Dump/DereferencingLevels ; Dump)
  * Duplicate Literal (Type/DuplicateLiteral ; Semantics)
  * Internet Domains (Type/UdpDomains ; Inventory)
  * No Weak SSL Crypto (Security/NoWeakSSLCrypto ; Security)
  * No mb_substr In Loop (Performances/MbStringInLoop ; Performances)
  * Non Nullable Getters (Classes/NonNullableSetters)
  * Use Case Value (Structures/UseCaseValue ; Suggestions)

* 1.9.5

  * Collect Literals (Dump/CollectLiterals ; Dump)
  * Environment Variable Usage (Dump/EnvironnementVariables ; Dump)
  * Interfaces Don't Ensure Properties (Interfaces/NoGaranteeForPropertyConstant ; Analyze, ClassReview)
  * Interfaces Is Not Implemented (Interfaces/IsNotImplemented ; Analyze, LintButWontExec, ClassReview, CI-checks)
  * Magic Properties (Classes/MagicProperties)
  * No Literal For Reference (Functions/NoLiteralForReference ; Analyze, CI-checks)
  * Use array_slice() (Performances/UseArraySlice ; Analyze, CI-checks)

* 1.9.4

  * Coalesce And Concat (Structures/CoalesceAndConcat ; Analyze, CI-checks)
  * Constant Comparison (Structures/AlwaysFalse ; Analyze)
  * Cyclomatic Complexity (Dump/CyclomaticComplexity ; Dump)
  * Nested Ternary Without Parenthesis (Php/NestedTernaryWithoutParenthesis ; Appinfo, CompatibilityPHP74)
  * PHP 74 New Directives (Php/Php74NewDirective ; CompatibilityPHP73)
  * Should Use Explode Args (Structures/ShouldUseExplodeArgs ; Analyze, CI-checks)
  * Spread Operator For Array (Php/SpreadOperatorForArray ; Appinfo)
  * Too Many Array Dimensions (Arrays/TooManyDimensions)
  * Use Arrow Functions (Functions/UseArrowFunctions ; Appinfo)

* 1.9.3

  * Complete/SetClassRemoteDefinitionWithParenthesis (Complete/SetClassRemoteDefinitionWithParenthesis ; Complete)
  * Complete/SetClassRemoteDefinitionWithTypehint (Complete/SetClassRemoteDefinitionWithTypehint ; Complete)
  * Environment Variables (Dump/EnvironmentVariables ; )
  * Indentation Levels (Dump/IndentationLevels ; Dump)
  * Max Level Of Nesting (Structures/MaxLevelOfIdentation ; Analyze)
  * No Spread For Hash (Arrays/NoSpreadForHash)
  * PHP 7.4 Constant Deprecation (Php/Php74Deprecation ; CompatibilityPHP74)
  * PHP 7.4 Removed Directives (Php/Php74RemovedDirective ; CompatibilityPHP74)
  * Set Class Method Remote Definition (Complete/SetClassMethodRemoteDefinition ; Complete)
  * Set Class Property Definition With Typehint (Complete/SetClassPropertyDefinitionWithTypehint ; Complete)
  * Set Class Remote Definition With Global (Complete/SetClassRemoteDefinitionWithGlobal ; Complete)
  * Set Class Remote Definition With Local New (Complete/SetClassRemoteDefinitionWithLocalNew ; Complete)
  * Set Class Remote Definition With Return Typehint (Complete/SetClassRemoteDefinitionWithReturnTypehint ; Complete)
  * Set String Method Definition (Complete/SetStringMethodDefinition ; Complete)
  * SetA rray Class Definition (Complete/SetArrayClassDefinition ; Complete)
  * Use Contravariance (Php/UseContravariance ; Appinfo)
  * Use Covariance (Php/UseCovariance ; Appinfo)
  * openssl_random_pseudo_byte() Second Argument (Structures/OpensslRandomPseudoByteSecondArg ; CompatibilityPHP74)
  * strip_tags Skips Closed Tag (Structures/StripTagsSkipsClosedTag ; Analyze, CI-checks)

* 1.9.2

  * Complete/SetClassRemoteDefinitionWithInjection (Complete/SetClassRemoteDefinitionWithInjection ; Complete)
  * Create Compact Variables (Complete/CreateCompactVariables)
  * Create Default Values (Complete/CreateDefaultValues ; Complete)
  * Create Magic Property (Complete/CreateMagicProperty ; Complete)
  * Follow Closure Definition (Complete/FollowClosureDefinition ; Complete)
  * Implode() Arguments Order (Structures/ImplodeArgsOrder ; Analyze, CI-checks)
  * Make Class Constant Definition (Complete/MakeClassConstantDefinition ; Complete)
  * Make Class Method Definition (Complete/MakeClassMethodDefinition ; Complete)
  * No ENT_IGNORE (Security/NoEntIgnore ; Security)
  * No More Curly Arrays (Php/NoMoreCurlyArrays ; CompatibilityPHP74)
  * Overwritten Constant (Complete/OverwrittenConstants ; Complete)
  * Overwritten Methods (Complete/OverwrittenMethods ; Complete)
  * Overwritten Properties (Complete/OverwrittenProperties ; Complete)
  * PHP 7.4 Reserved Keyword (Php/Php74ReservedKeyword ; CompatibilityPHP74)
  * Propagate Constants (Complete/PropagateConstants ; Complete)
  * Set Class_Alias Definition (Complete/SetClassAliasDefinition ; Complete)
  * Set Clone Link (Complete/SetCloneLink ; Complete)
  * Set Parent Definition (Complete/SetParentDefinition ; Complete)
  * Solve Trait Methods (Complete/SolveTraitMethods ; Complete)
  * array_merge() And Variadic (Structures/ArrayMergeAndVariadic ; Analyze)

* 1.9.1

  * Complete/PhpNativeReference (Complete/PhpNativeReference)

* 1.9.0

  * Class Without Parent (Classes/NoParent)
  * Numeric Literal Separator (Php/IntegerSeparatorUsage ; Appinfo, CompatibilityPHP73)
  * PHP 7.4 Removed Functions (Php/Php74RemovedFunctions ; CompatibilityPHP74)
  * Reflection Export() Is Deprecated (Php/ReflectionExportIsDeprecated ; CompatibilityPHP74)
  * Scalar Are Not Arrays (Php/ScalarAreNotArrays ; Analyze, CompatibilityPHP74, CI-checks)
  * Serialize Magic Method (Php/SerializeMagic ; Internal)
  * Similar Integers (Type/SimilarIntegers ; Coding Conventions, Semantics)
  * Unbinding Closures (Functions/UnbindingClosures ; CompatibilityPHP74)
  * array_key_exists() Works On Arrays (Php/ArrayKeyExistsWithObjects ; Analyze, CompatibilityPHP74)

* 1.8.9

  * Avoid mb_dectect_encoding() (Php/AvoidMbDectectEncoding ; Analyze)
  * Disconnected Classes (Classes/DisconnectedClasses)
  * Not Or Tilde (Structures/NotOrNot ; Preferences)
  * Overwritten Source And Value (Structures/ForeachSourceValue ; Analyze, OneFile)
  * Useless Type Check (Functions/UselessTypeCheck ; Dead code, OneFile)
  * mb_strrpos() Third Argument (Php/Php74mbstrrpos3rdArg ; CompatibilityPHP74)

* 1.8.8

  * Set Aside Code (Structures/SetAside)
  * Use Array Functions (Structures/UseArrayFunctions ; Suggestions)

* 1.8.7

  * Cant Use Function (Functions/CantUse)
  * Generator Cannot Return (Functions/GeneratorCannotReturn ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Use DateTimeImmutable Class (Php/UseDateTimeImmutable ; Suggestions)
  * Wrong Type Returned (Functions/WrongReturnedType ; Analyze, ClassReview, CI-checks)

* 1.8.6

  * Dependant Abstract Classes (Classes/DependantAbstractClass ; Analyze, ClassReview)
  * Infinite Recursion (Structures/InfiniteRecursion ; Analyze)
  * Modules/IncomingData (Modules/IncomingData ; Internal)
  * Modules/NativeReplacement (Modules/NativeReplacement ; Internal)
  * Null Or Boolean Arrays (Arrays/NullBoolean)

* 1.8.5

  * Could Use Trait (Traits/CouldUseTrait)

* 1.8.4

  * Always Use Function With array_key_exists() (Performances/Php74ArrayKeyExists ; Performances)
  * Complex Dynamic Names (Variables/ComplexDynamicNames ; Suggestions)
  * Could Be Constant (Constants/CouldBeConstant ; Suggestions)
  * New Constants In PHP 7.4 (Php/Php74NewConstants ; CompatibilityPHP74)
  * Regex On Arrays (Performances/RegexOnArrays ; Performances)
  * Unused Class Constant (Classes/UnusedConstant)
  * curl_version() Has No Argument (Structures/CurlVersionNow ; CompatibilityPHP74)

* 1.8.3

  * Autoappend (Performances/Autoappend ; Performances)
  * Make Magic Concrete (Classes/MakeMagicConcrete)
  * Memoize MagicCall (Performances/MemoizeMagicCall ; Analyze, ClassReview)
  * Substr To Trim (Structures/SubstrToTrim ; Suggestions)

* 1.8.2

  * Identical Methods (Classes/IdenticalMethods)
  * No Append On Source (Structures/NoAppendOnSource ; Analyze)

* 1.8.1

  * No Need For get_class() (Structures/NoNeedGetClass)

* 1.8.0

  * Already Parents Trait (Traits/AlreadyParentsTrait ; Analyze)
  * Casting Ternary (Structures/CastingTernary ; Analyze, OneFile, CI-checks)
  * Concat And Addition (Php/ConcatAndAddition ; Analyze, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73, CompatibilityPHP74, Top10, CompatibilityPHP80, CI-checks)
  * Concat Empty String (Structures/ConcatEmpty ; Analyze, OneFile)
  * Minus One On Error (Security/MinusOneOnError ; Security)
  * New Functions In PHP 7.4 (Php/Php74NewFunctions ; CompatibilityPHP74)
  * Unpacking Inside Arrays (Php/UnpackingInsideArrays ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73)
  * Useless Argument (Functions/UselessArgument)

* 1.7.9

  * Avoid option arrays in constructors (Classes/AvoidOptionArrays)
  * Trait Not Found (Traits/TraitNotFound ; Analyze, LintButWontExec)
  * Useless Default Argument (Functions/UselessDefault ; Suggestions)
  * ext/ffi (Extensions/Extffi ; Appinfo, Appcontent)
  * ext/uuid (Extensions/Extuuid ; Appinfo)
  * ext/zend_monitor (Extensions/Extzendmonitor ; Appinfo)

* 1.7.8

  * ext/svm (Extensions/Extsvm)

* 1.7.7

  * Implode One Arg (Php/ImplodeOneArg)
  * Incoming Values (Php/IncomingValues ; Internal)
  * Integer Conversion (Security/IntegerConversion ; Security)

* 1.7.6

  * Caught Variable (Exceptions/CatchE)
  * Multiple Unset() (Structures/MultipleUnset ; Suggestions, php-cs-fixable)
  * PHP Overridden Function (Php/OveriddenFunction ; Appinfo)
  * array_merge With Ellipsis (Structures/ArrayMergeWithEllipsis ; )

* 1.7.2

  * Check On __Call Usage (Classes/CheckOnCallUsage)
  * Unsupported Operand Types (Structures/UnsupportedOperandTypes ; )

* 1.7.0

  * Clone With Non-Object (Classes/CloneWithNonObject)
  * Self-Transforming Variables (Variables/SelfTransform ; Internal)
  * Should Deep Clone (Classes/ShouldDeepClone ; Suggestions)
  * Windows Only Constants (Portability/WindowsOnlyConstants ; )

* 1.6.9

  * Inconsistent Variable Usage (Variables/InconsistentUsage ; Under Work)
  * Typehint Must Be Returned (Functions/TypehintMustBeReturned)

* 1.6.8

  * PHP 8.0 Removed Constants (Php/Php80RemovedConstant)
  * PHP 8.0 Removed Functions (Php/Php80RemovedFunctions ; CompatibilityPHP80)

* 1.6.7

  * An OOP Factory (Patterns/Factory ; Appinfo)
  * Constant Dynamic Creation (Constants/DynamicCreation ; Appinfo)
  * Law of Demeter (Classes/DemeterLaw)

* 1.6.6

  * Bad Typehint Relay (Functions/BadTypehintRelay)
  * Insufficient Typehint (Functions/InsufficientTypehint ; Analyze, Typechecks)

* 1.6.5

  * String Initialization (Arrays/StringInitialization)
  * Variable Is Not A Condition (Structures/NoVariableIsACondition ; Analyze)
  * ext/pcov (Extensions/Extpcov ; Appinfo)
  * ext/weakref (Extensions/Extweakref ; Appinfo)

* 1.6.4

  * Defined Classes (Modules/DefinedClasses)
  * Don't Be Too Manual (Structures/DontBeTooManual ; Coding Conventions)
  * Use Coalesce Equal (Structures/UseCoalesceEqual ; )

* 1.6.3

  * Assign And Compare (Structures/AssigneAndCompare)

* 1.6.2

  * Typed Property Usage (Php/TypedPropertyUsage)

* 1.6.1

  * Possible Missing Subpattern (Php/MissingSubpattern ; Analyze, Top10, CI-checks)
  * array_key_exists() Speedup (Performances/ArrayKeyExistsSpeedup)

* 1.5.8

  * Multiple Identical Closure (Functions/MultipleIdenticalClosure)
  * Path lists (Type/Path ; Appinfo)

* 1.5.7

  * Method Could Be Static (Classes/CouldBeStatic)
  * Multiple Usage Of Same Trait (Traits/MultipleUsage ; Suggestions)
  * Self Using Trait (Traits/SelfUsingTrait ; Dead code, ClassReview)
  * ext/wasm (Extensions/Extwasm ; Appinfo)

* 1.5.6

  * Isset() On The Whole Array (Performances/IssetWholeArray ; Performances, Suggestions)
  * Useless Alias (Traits/UselessAlias ; Analyze, LintButWontExec, CI-checks)
  * ext/async (Extensions/Extasync)
  * ext/sdl (Extensions/Extsdl ; Appinfo)

* 1.5.5

  * Directly Use File (Structures/DirectlyUseFile ; Suggestions)
  * Safe HTTP Headers (Security/SafeHttpHeaders ; Security)
  * fputcsv() In Loops (Performances/CsvInLoops)

* 1.5.4

  * Avoid Self In Interface (Interfaces/AvoidSelfInInterface ; ClassReview)
  * Should Have Destructor (Classes/ShouldHaveDestructor)
  * Unreachable Class Constant (Classes/UnreachableConstant ; ClassReview)

* 1.5.3

  * Don't Loop On Yield (Structures/DontLoopOnYield)
  * Variable May Be Non-Global (Structures/VariableMayBeNonGlobal ; Internal)

* 1.5.2

  * PHP Exception (Exceptions/IsPhpException)
  * Should Yield With Key (Functions/ShouldYieldWithKey ; Analyze, Top10, CI-checks)
  * ext/decimal (Extensions/Extdecimal ; Appinfo)
  * ext/psr (Extensions/Extpsr ; Appinfo)

* 1.5.1

  * Use Basename Suffix (Structures/BasenameSuffix)

* 1.5.0

  * Could Use Try (Exceptions/CouldUseTry)
  * Pack Format Inventory (Type/Pack ; Inventory, Appinfo)
  * Printf Format Inventory (Type/Printf ; Inventory, Appinfo)
  * idn_to_ascii() New Default (Php/IdnUts46 ; CompatibilityPHP74)

* 1.4.9

  * Don't Read And Write In One Expression (Structures/DontReadAndWriteInOneExpression ; Analyze, CompatibilityPHP73, CompatibilityPHP74)
  * Invalid Pack Format (Structures/InvalidPackFormat ; Analyze, CI-checks)
  * Named Regex (Structures/NamedRegex ; Suggestions)
  * No Reference For Static Property (Php/NoReferenceForStaticProperty ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * No Return For Generator (Php/NoReturnForGenerator ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Repeated Interface (Interfaces/RepeatedInterface ; Analyze, LintButWontExec)
  * Wrong Access Style to Property (Classes/UndeclaredStaticProperty)

* 1.4.8

  * Direct Call To __clone() (Php/DirectCallToClone)
  * filter_input() As A Source (Security/FilterInputSource ; Security)

* 1.4.6

  * Only Variable For Reference (Functions/OnlyVariableForReference)

* 1.4.5

  * Add Default Value (Functions/AddDefaultValue)

* 1.4.4

  * ext/seaslog (Extensions/Extseaslog)

* 1.4.3

  * Class Could Be Final (Classes/CouldBeFinal)
  * Closure Could Be A Callback (Functions/Closure2String ; Performances, Suggestions)
  * Inconsistent Elseif (Structures/InconsistentElseif ; Analyze)
  * Use json_decode() Options (Structures/JsonWithOption ; Suggestions)

* 1.4.2

  * Method Collision Traits (Traits/MethodCollisionTraits)
  * Undefined Insteadof (Traits/UndefinedInsteadof ; Analyze, LintButWontExec, CI-checks)
  * Undefined Variable (Variables/UndefinedVariable ; Analyze, CI-checks)

* 1.4.1

  * Must Call Parent Constructor (Php/MustCallParentConstructor)

* 1.4.0

  * PHP 7.3 Removed Functions (Php/Php73RemovedFunctions)
  * Trailing Comma In Calls (Php/TrailingComma ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)

* 1.3.9

  * Assert Function Is Reserved (Php/AssertFunctionIsReserved ; Analyze, CompatibilityPHP73)
  * Avoid Real (Php/AvoidReal ; Suggestions, Top10)
  * Case Insensitive Constants (Constants/CaseInsensitiveConstants ; Appinfo, CompatibilityPHP73)
  * Const Or Define Preference (Constants/ConstDefinePreference ; Preferences)
  * Continue Is For Loop (Structures/ContinueIsForLoop ; Analyze, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73)
  * Could Be Abstract Class (Classes/CouldBeAbstractClass)

* 1.3.8

  * Constant Case Preference (Constants/DefineInsensitivePreference)
  * Detect Current Class (Php/DetectCurrentClass ; Suggestions, CompatibilityPHP74)
  * Use is_countable (Php/CouldUseIsCountable ; Suggestions)

* 1.3.7

  * Handle Arrays With Callback (Arrays/WithCallback)

* 1.3.5

  * Locally Used Property In Trait (Traits/LocallyUsedProperty ; Internal)
  * PHP 7.0 Scalar Typehints (Php/PHP70scalartypehints ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * PHP 7.1 Scalar Typehints (Php/PHP71scalartypehints ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * PHP 7.2 Scalar Typehints (Php/PHP72scalartypehints ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71)
  * Undefined ::class (Classes/UndefinedStaticclass)
  * ext/lzf (Extensions/Extlzf ; Appinfo)
  * ext/msgpack (Extensions/Extmsgpack ; Appinfo)

* 1.3.4

  * Ambiguous Visibilities (Classes/AmbiguousVisibilities)
  * Hash Algorithms Incompatible With PHP 7.1- (Php/HashAlgos71 ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * Hash Algorithms Incompatible With PHP 7.4- (Php/HashAlgos74 ; CompatibilityPHP74)
  * ext/csprng (Extensions/Extcsprng ; Appinfo)

* 1.3.3

  * Abstract Or Implements (Classes/AbstractOrImplements)
  * Can't Throw Throwable (Exceptions/CantThrow ; Analyze, LintButWontExec)
  * Incompatible Signature Methods (Classes/IncompatibleSignature ; Analyze, LintButWontExec)
  * Incompatible Signature Methods With Covariance (Classes/IncompatibleSignature74 ; Analyze)
  * ext/eio (Extensions/Exteio ; Appinfo)

* 1.3.2

  * > Or < Comparisons (Structures/GtOrLtFavorite ; Preferences)
  * Compared But Not Assigned Strings (Structures/ComparedButNotAssignedStrings ; Under Work)
  * Could Be Static Closure (Functions/CouldBeStaticClosure)
  * Dont Mix ++ (Structures/DontMixPlusPlus ; Analyze)
  * Strict Or Relaxed Comparison (Structures/ComparisonFavorite ; Preferences)
  * move_uploaded_file Instead Of copy (Security/MoveUploadedFile ; Security)

* 1.3.0

  * Check JSON (Structures/CheckJson ; Analyze, CI-checks)
  * Const Visibility Usage (Classes/ConstVisibilityUsage)
  * Should Use Operator (Structures/ShouldUseOperator ; Suggestions)
  * Single Use Variables (Variables/UniqueUsage ; Under Work)

* 1.2.9

  * Compact Inexistant Variable (Php/CompactInexistant ; CompatibilityPHP73, Suggestions)
  * Configure Extract (Security/ConfigureExtract ; Security)
  * Flexible Heredoc (Php/FlexibleHeredoc ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Method Signature Must Be Compatible (Classes/MethodSignatureMustBeCompatible)
  * Mismatch Type And Default (Functions/MismatchTypeAndDefault ; Analyze, LintButWontExec, Typechecks)
  * Use The Blind Var (Performances/UseBlindVar ; Performances)

* 1.2.8

  * Cache Variable Outside Loop (Performances/CacheVariableOutsideLoop ; Performances)
  * Cant Instantiate Class (Classes/CantInstantiateClass)
  * Do In Base (Performances/DoInBase ; Performances)
  * Php/FailingAnalysis (Php/FailingAnalysis ; Internal)
  * Typehinted References (Functions/TypehintedReferences ; Analyze, CI-checks)
  * Weak Typing (Classes/WeakType ; Analyze)
  * strpos() Too Much (Performances/StrposTooMuch ; Analyze, CI-checks)

* 1.2.7

  * ext/cmark (Extensions/Extcmark)

* 1.2.6

  * Callback Function Needs Return (Functions/CallbackNeedsReturn)
  * Could Use array_unique (Structures/CouldUseArrayUnique ; Suggestions)
  * Missing Parenthesis (Structures/MissingParenthesis ; Analyze, Simple, Level 5, CI-checks)
  * One If Is Sufficient (Structures/OneIfIsSufficient ; Suggestions)

* 1.2.5

  * Wrong Range Check (Structures/WrongRange ; Analyze)
  * ext/zookeeper (Extensions/Extzookeeper)

* 1.2.4

  * Processing Collector (Performances/RegexOnCollector)

* 1.2.3

  * Don't Unset Properties (Classes/DontUnsetProperties)
  * Redefined Private Property (Classes/RedefinedPrivateProperty ; Analyze)
  * Strtr Arguments (Php/StrtrArguments ; Analyze, CI-checks)

* 1.2.2

  * Drop Substr Last Arg (Structures/SubstrLastArg)

* 1.2.1

  * Possible Increment (Structures/PossibleIncrement ; Suggestions)
  * Properties Declaration Consistence (Classes/PPPDeclarationStyle)

* 1.1.10

  * Too Many Native Calls (Php/TooManyNativeCalls)

* 1.1.9

  * Should Preprocess Chr() (Php/ShouldPreprocess ; Suggestions)
  * Too Many Parameters (Functions/TooManyParameters)

* 1.1.8

  * Mass Creation Of Arrays (Arrays/MassCreation)
  * ext/db2 (Extensions/Extdb2 ; Appinfo)

* 1.1.7

  * Could Use array_fill_keys (Structures/CouldUseArrayFillKeys ; Suggestions)
  * Dynamic Library Loading (Security/DynamicDl ; Security)
  * PHP 7.3 Last Empty Argument (Php/PHP73LastEmptyArgument ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Property Could Be Local (Classes/PropertyCouldBeLocal)
  * Use Count Recursive (Structures/UseCountRecursive ; Suggestions)
  * ext/leveldb (Extensions/Extleveldb ; Appinfo)
  * ext/opencensus (Extensions/Extopencensus ; Appinfo)
  * ext/uopz (Extensions/Extuopz ; Appinfo)
  * ext/varnish (Extensions/Extvarnish ; Appinfo)
  * ext/xxtea (Extensions/Extxxtea ; Appinfo)

* 1.1.6

  * Could Use Compact (Structures/CouldUseCompact ; Suggestions)
  * Foreach On Object (Php/ForeachObject)
  * List With Reference (Php/ListWithReference ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Test Then Cast (Structures/TestThenCast ; Analyze)

* 1.1.5

  * Possible Infinite Loop (Structures/PossibleInfiniteLoop ; Analyze)
  * Should Use Math (Structures/ShouldUseMath ; Suggestions)
  * ext/hrtime (Extensions/Exthrtime)

* 1.1.4

  * Double array_flip() (Performances/DoubleArrayFlip ; Performances)
  * Fallback Function (Functions/FallbackFunction ; Appinfo)
  * Find Key Directly (Structures/GoToKeyDirectly ; Under Work)
  * Reuse Variable (Structures/ReuseVariable ; Suggestions)
  * Useless Catch (Exceptions/UselessCatch)

* 1.1.3

  * Useless Referenced Argument (Functions/UselessReferenceArgument)

* 1.1.2

  * Local Globals (Variables/LocalGlobals ; )
  * Missing Include (Files/MissingInclude)

* 1.1.1

  * Inclusion Wrong Case (Files/InclusionWrongCase)

* 1.0.11

  * No Net For Xml Load (Security/NoNetForXmlLoad ; Security)
  * Unused Inherited Variable In Closure (Functions/UnusedInheritedVariable)

* 1.0.10

  * Sqlite3 Requires Single Quotes (Security/Sqlite3RequiresSingleQuotes)

* 1.0.8

  * Identical Consecutive Expression (Structures/IdenticalConsecutive ; Analyze)
  * Identical On Both Sides (Structures/IdenticalOnBothSides ; Analyze, CI-checks)
  * Mistaken Concatenation (Arrays/MistakenConcatenation)
  * No Reference For Ternary (Php/NoReferenceForTernary ; Analyze, CI-checks)

* 1.0.7

  * Not A Scalar Type (Php/NotScalarType)
  * Should Use array_filter() (Php/ShouldUseArrayFilter ; Suggestions)

* 1.0.6

  * Never Used Parameter (Functions/NeverUsedParameter ; Analyze, Suggestions)
  * Use Named Boolean In Argument Definition (Functions/AvoidBooleanArgument ; Analyze)
  * ext/igbinary (Extensions/Extigbinary)

* 1.0.5

  * Assigned In One Branch (Structures/AssignedInOneBranch ; Under Work)
  * Environment Variables (Variables/UncommonEnvVar ; Appinfo)
  * Invalid Regex (Structures/InvalidRegex ; Analyze, CI-checks)
  * Parent First (Classes/ParentFirst)
  * Same Variable Foreach (Structures/AutoUnsetForeach ; Analyze, CI-checks)

* 1.0.4

  * Argon2 Usage (Php/Argon2Usage ; Appinfo, Appcontent)
  * Array Index (Type/ArrayIndex ; Inventory, Appinfo)
  * Avoid set_error_handler $context Argument (Php/AvoidSetErrorHandlerContextArg ; CompatibilityPHP72)
  * Can't Count Non-Countable (Structures/CanCountNonCountable ; CompatibilityPHP72)
  * Crypto Usage (Php/CryptoUsage ; Appinfo, Appcontent)
  * Dl() Usage (Php/DlUsage ; Appinfo)
  * Don't Send $this In Constructor (Classes/DontSendThisInConstructor ; Analyze)
  * Hash Will Use Objects (Php/HashUsesObjects ; CompatibilityPHP72)
  * Incoming Variable Index Inventory (Type/GPCIndex ; Inventory, Appinfo, Appcontent)
  * Integer As Property (Classes/IntegerAsProperty ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71)
  * Maybe Missing New (Structures/MissingNew ; Analyze)
  * No get_class() With Null (Structures/NoGetClassNull ; Analyze, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Php 7.2 New Class (Php/Php72NewClasses ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Php 7.4 New Class (Php/Php74NewClasses ; CompatibilityPHP74)
  * Slice Arrays First (Arrays/SliceFirst)
  * Unknown Pcre2 Option (Php/UnknownPcre2Option ; Analyze, CompatibilityPHP73)
  * Use List With Foreach (Structures/UseListWithForeach ; Suggestions, Top10)
  * Use PHP7 Encapsed Strings (Performances/PHP7EncapsedStrings ; Performances)
  * ext/vips (Extensions/Extvips ; Appinfo, Appcontent)

* 1.0.3

  * Ambiguous Static (Classes/AmbiguousStatic)
  * Drupal Usage (Vendors/Drupal ; Appinfo)
  * FuelPHP Usage (Vendors/Fuel ; Appinfo, Appcontent)
  * Phalcon Usage (Vendors/Phalcon ; Appinfo)

* 1.0.1

  * Could Be Else (Structures/CouldBeElse ; Analyze)
  * Next Month Trap (Structures/NextMonthTrap ; Analyze, Top10, CI-checks)
  * Printf Number Of Arguments (Structures/PrintfArguments ; Analyze, CI-checks)
  * Simple Switch (Performances/SimpleSwitch)
  * Substring First (Performances/SubstrFirst ; Performances, Suggestions, Top10)

* 0.12.17

  * Is A PHP Magic Property (Classes/IsaMagicProperty)

* 0.12.16

  * Cookies Variables (Php/CookiesVariables)
  * Date Formats (Php/DateFormats ; Inventory)
  * Incoming Variables (Php/IncomingVariables ; Inventory)
  * Session Variables (Php/SessionVariables ; Inventory)
  * Too Complex Expression (Structures/ComplexExpression ; Appinfo)
  * Unconditional Break In Loop (Structures/UnconditionLoopBreak ; Analyze, Level 3, CI-checks)

* 0.12.15

  * Always Anchor Regex (Security/AnchorRegex)
  * Is Actually Zero (Structures/IsZero ; Analyze, Level 2, CI-checks)
  * Multiple Type Variable (Structures/MultipleTypeVariable ; Analyze, Level 4)
  * Session Lazy Write (Security/SessionLazyWrite ; Security)

* 0.12.14

  * Regex Inventory (Type/Regex ; Inventory, Appinfo, Appcontent)
  * Switch Fallthrough (Structures/Fallthrough ; Inventory, Security, Stats)
  * Upload Filename Injection (Security/UploadFilenameInjection)

* 0.12.12

  * Use pathinfo() Arguments (Php/UsePathinfoArgs ; Performances)
  * ext/parle (Extensions/Extparle)

* 0.12.11

  * Could Be Protected Class Constant (Classes/CouldBeProtectedConstant ; ClassReview)
  * Could Be Protected Method (Classes/CouldBeProtectedMethod ; ClassReview)
  * Method Could Be Private Method (Classes/CouldBePrivateMethod)
  * Method Used Below (Classes/MethodUsedBelow ; )
  * Pathinfo() Returns May Vary (Php/PathinfoReturns ; Analyze, Level 4)

* 0.12.10

  * Constant Used Below (Classes/ConstantUsedBelow)
  * Could Be Private Class Constant (Classes/CouldBePrivateConstante ; ClassReview)

* 0.12.9

  * Shell Favorite (Php/ShellFavorite)

* 0.12.8

  * ext/fam (Extensions/Extfam)
  * ext/rdkafka (Extensions/Extrdkafka ; Appinfo)

* 0.12.7

  * Should Use Foreach (Structures/ShouldUseForeach)

* 0.12.5

  * Logical To in_array (Performances/LogicalToInArray)
  * No Substr Minus One (Php/NoSubstrMinusOne ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)

* 0.12.4

  * Assign With And Precedence (Php/AssignAnd ; Analyze, CI-checks)
  * Avoid Concat In Loop (Performances/NoConcatInLoop ; Performances, Top10)
  * Child Class Removes Typehint (Classes/ChildRemoveTypehint)
  * Isset Multiple Arguments (Php/IssetMultipleArgs ; Suggestions, php-cs-fixable)
  * Logical Operators Favorite (Php/LetterCharsLogicalFavorite ; Preferences, Top10)
  * No Magic Method With Array (Classes/NoMagicWithArray ; Analyze, Level 4, LintButWontExec, CI-checks)
  * Optional Parameter (Functions/OptionalParameter ; DefensiveProgrammingTM)
  * PHP 7.2 Object Keyword (Php/Php72ObjectKeyword ; CompatibilityPHP72)
  * ext/xattr (Extensions/Extxattr ; Appinfo)

* 0.12.3

  * Group Use Trailing Comma (Php/GroupUseTrailingComma ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71)
  * Mismatched Default Arguments (Functions/MismatchedDefaultArguments ; Analyze, Typechecks)
  * Mismatched Typehint (Functions/MismatchedTypehint ; Analyze, Typechecks)
  * Scalar Or Object Property (Classes/ScalarOrObjectProperty)

* 0.12.2

  * Mkdir Default (Security/MkdirDefault ; Security)
  * ext/lapack (Extensions/Extlapack)
  * strict_types Preference (Php/DeclareStrict ; Appinfo, Preferences)

* 0.12.1

  * Const Or Define (Structures/ConstDefineFavorite ; Appinfo)
  * Declare strict_types Usage (Php/DeclareStrictType ; Appinfo, Preferences)
  * Encoding Usage (Php/DeclareEncoding)
  * Mismatched Ternary Alternatives (Structures/MismatchedTernary ; Analyze, Suggestions, Level 4)
  * No Return Or Throw In Finally (Structures/NoReturnInFinally ; Security)
  * Ticks Usage (Php/DeclareTicks ; Appinfo, Preferences)

* 0.12.0

  * Avoid Optional Properties (Classes/AvoidOptionalProperties)
  * Heredoc Delimiter (Structures/HeredocDelimiterFavorite ; Coding Conventions)
  * Multiple Functions Declarations (Functions/MultipleDeclarations ; Appinfo)
  * Non Breakable Space In Names (Structures/NonBreakableSpaceInNames ; Appinfo, Appcontent)
  * ext/swoole (Extensions/Extswoole ; Appinfo)

* 0.11.8

  * Cant Inherit Abstract Method (Classes/CantInheritAbstractMethod)
  * Codeigniter usage (Vendors/Codeigniter ; Appinfo)
  * Ez cms usage (Vendors/Ez ; Appinfo)
  * Joomla usage (Vendors/Joomla ; Appinfo, Appcontent)
  * Laravel usage (Vendors/Laravel ; Appinfo, Appcontent)
  * Symfony usage (Vendors/Symfony ; Appinfo)
  * Use session_start() Options (Php/UseSessionStartOptions ; Suggestions)
  * Wordpress usage (Vendors/Wordpress ; Appinfo)
  * Yii usage (Vendors/Yii ; Appinfo, Appcontent)

* 0.11.7

  * Forgotten Interface (Interfaces/CouldUseInterface ; Analyze)
  * Order Of Declaration (Classes/OrderOfDeclaration)

* 0.11.6

  * Concatenation Interpolation Consistence (Structures/ConcatenationInterpolationFavorite ; Preferences)
  * Could Make A Function (Functions/CouldCentralize ; Analyze, Suggestions)
  * Courier Anti-Pattern (Patterns/CourrierAntiPattern ; Appinfo, Appcontent, Dismell)
  * DI Cyclic Dependencies (Classes/TypehintCyclicDependencies ; Dismell)
  * Dependency Injection (Patterns/DependencyInjection ; Appinfo)
  * PSR-13 Usage (Psr/Psr13Usage ; Appinfo)
  * PSR-16 Usage (Psr/Psr16Usage ; Appinfo)
  * PSR-3 Usage (Psr/Psr3Usage ; Appinfo)
  * PSR-6 Usage (Psr/Psr6Usage ; Appinfo)
  * PSR-7 Usage (Psr/Psr7Usage ; Appinfo)
  * Too Many Injections (Classes/TooManyInjections)
  * ext/gender (Extensions/Extgender ; Appinfo)
  * ext/judy (Extensions/Extjudy ; Appinfo)

* 0.11.5

  * Could Typehint (Functions/CouldTypehint ; Under Work)
  * Implemented Methods Are Public (Classes/ImplementedMethodsArePublic)
  * Mixed Concat And Interpolation (Structures/MixedConcatInterpolation ; Analyze, Coding Conventions)
  * No Reference On Left Side (Structures/NoReferenceOnLeft ; Analyze, CI-checks)
  * PSR-11 Usage (Psr/Psr11Usage ; Appinfo)
  * ext/stats (Extensions/Extstats ; Appinfo)

* 0.11.4

  * No Class As Typehint (Functions/NoClassAsTypehint)
  * Use Browscap (Php/UseBrowscap ; Appinfo)
  * Use Debug (Structures/UseDebug ; Appinfo)

* 0.11.3

  * No Return Used (Functions/NoReturnUsed ; Analyze, Suggestions, Level 4)
  * Only Variable Passed By Reference (Functions/OnlyVariablePassedByReference ; Analyze)
  * Try With Multiple Catch (Php/TryMultipleCatch ; Appinfo)
  * ext/grpc (Extensions/Extgrpc)
  * ext/sphinx (Extensions/Extsphinx ; Appinfo)

* 0.11.2

  * Alternative Syntax Consistence (Structures/AlternativeConsistenceByFile ; Analyze)
  * Randomly Sorted Arrays (Arrays/RandomlySortedLiterals)

* 0.11.1

  * Difference Consistence (Structures/DifferencePreference)
  * No Empty Regex (Structures/NoEmptyRegex ; Analyze, CI-checks)

* 0.11.0

  * Could Use str_repeat() (Structures/CouldUseStrrepeat ; Analyze, Level 1, Top10, CI-checks)
  * Crc32() Might Be Negative (Php/Crc32MightBeNegative ; Analyze, PHP recommendations)
  * Empty Final Element (Arrays/EmptyFinal)
  * Strings With Strange Space (Type/StringWithStrangeSpace ; Analyze, CI-checks)
  * Suspicious Comparison (Structures/SuspiciousComparison ; Analyze, Level 3)

* 0.10.9

  * Displays Text (Php/Prints ; Internal)
  * Method Is Overwritten (Classes/MethodIsOverwritten)
  * No Class In Global (Php/NoClassInGlobal ; Analyze, CI-checks)
  * Repeated Regex (Structures/RepeatedRegex ; Analyze, Level 1, CI-checks)

* 0.10.7

  * Group Use Declaration (Php/GroupUseDeclaration)
  * Missing Cases In Switch (Structures/MissingCases ; Analyze)
  * New Constants In PHP 7.2 (Php/Php72NewConstants ; CompatibilityPHP72)
  * New Functions In PHP 7.2 (Php/Php72NewFunctions ; CompatibilityPHP72)
  * New Functions In PHP 7.3 (Php/Php73NewFunctions ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, CompatibilityPHP73)

* 0.10.6

  * Check All Types (Structures/CheckAllTypes ; Analyze)
  * Do Not Cast To Int (Php/NoCastToInt ; )
  * Manipulates INF (Php/IsINF)
  * Manipulates NaN (Php/IsNAN ; Appinfo)
  * Set Cookie Safe Arguments (Security/SetCookieArgs ; Security)
  * Should Use SetCookie() (Php/UseSetCookie ; Analyze)
  * Use Cookies (Php/UseCookies ; Appinfo, Appcontent)

* 0.10.5

  * Could Be Typehinted Callable (Functions/CouldBeCallable ; Under Work)
  * Encoded Simple Letters (Security/EncodedLetters ; Security)
  * Regex Delimiter (Structures/RegexDelimiter ; Preferences)
  * Strange Name For Constants (Constants/StrangeName ; Analyze)
  * Strange Name For Variables (Variables/StrangeName ; Analyze)
  * Too Many Finds (Classes/TooManyFinds)

* 0.10.4

  * No Need For Else (Structures/NoNeedForElse ; Analyze)
  * Should Use session_regenerateid() (Security/ShouldUseSessionRegenerateId ; Security)
  * ext/ds (Extensions/Extds)

* 0.10.3

  * Multiple Alias Definitions Per File (Namespaces/MultipleAliasDefinitionPerFile ; Analyze, CI-checks)
  * Property Used In One Method Only (Classes/PropertyUsedInOneMethodOnly ; Analyze)
  * Used Once Property (Classes/UsedOnceProperty ; Analyze)
  * __DIR__ Then Slash (Structures/DirThenSlash ; Analyze, Level 3, CI-checks)
  * self, parent, static Outside Class (Classes/NoPSSOutsideClass)

* 0.10.2

  * Class Function Confusion (Php/ClassFunctionConfusion ; Semantics)
  * Forgotten Thrown (Exceptions/ForgottenThrown)
  * Should Use array_column() (Php/ShouldUseArrayColumn ; Performances, Suggestions, Level 4)
  * ext/libsodium (Extensions/Extlibsodium ; Appinfo, Appcontent)

* 0.10.1

  * All strings (Type/CharString ; Inventory)
  * SQL queries (Type/Sql ; Inventory, Appinfo)
  * Strange Names For Methods (Classes/StrangeName)

* 0.10.0

  * Error_Log() Usage (Php/ErrorLogUsage ; Appinfo)
  * No Boolean As Default (Functions/NoBooleanAsDefault ; Analyze)
  * Raised Access Level (Classes/RaisedAccessLevel)

* 0.9.9

  * PHP 7.2 Deprecations (Php/Php72Deprecation)
  * PHP 7.2 Removed Functions (Php/Php72RemovedFunctions ; CompatibilityPHP72)

* 0.9.8

  * Assigned Twice (Variables/AssignedTwiceOrMore ; Analyze)
  * New Line Style (Structures/NewLineStyle ; Preferences)
  * New On Functioncall Or Identifier (Classes/NewOnFunctioncallOrIdentifier)

* 0.9.7

  * Avoid Large Array Assignation (Structures/NoAssignationInFunction ; Performances)
  * Could Be Protected Property (Classes/CouldBeProtectedProperty)
  * Long Arguments (Structures/LongArguments ; Analyze)

* 0.9.6

  * Avoid glob() Usage (Performances/NoGlob ; Performances)
  * Fetch One Row Format (Performances/FetchOneRowFormat)

* 0.9.5

  * One Expression Brackets Consistency (Structures/OneExpressionBracketsConsistency ; Preferences)
  * Should Use Function (Php/ShouldUseFunction ; Performances)
  * ext/mongodb (Extensions/Extmongodb)
  * ext/zbarcode (Extensions/Extzbarcode ; Appinfo)

* 0.9.4

  * Class Should Be Final By Ocramius (Classes/FinalByOcramius)
  * String (Extensions/Extstring ; Appinfo, Appcontent)
  * ext/mhash (Extensions/Extmhash ; Appinfo, CompatibilityPHP54, Appcontent)

* 0.9.3

  * Close Tags Consistency (Php/CloseTagsConsistency)
  * Unset() Or (unset) (Php/UnsetOrCast ; Preferences)

* 0.9.2

  * $GLOBALS Or global (Php/GlobalsVsGlobal ; Preferences)
  * Illegal Name For Method (Classes/WrongName)
  * Too Many Local Variables (Functions/TooManyLocalVariables ; Analyze)
  * Use Composer Lock (Composer/UseComposerLock ; Appinfo)
  * ext/ncurses (Extensions/Extncurses ; Appinfo)
  * ext/newt (Extensions/Extnewt ; Appinfo)
  * ext/nsapi (Extensions/Extnsapi ; Appinfo)

* 0.9.1

  * Avoid Using stdClass (Php/UseStdclass ; Analyze, OneFile, Simple, Level 4)
  * Avoid array_push() (Performances/AvoidArrayPush)
  * Invalid Octal In String (Type/OctalInString ; Inventory, CompatibilityPHP71)

* 0.9.0

  * Getting Last Element (Arrays/GettingLastElement)
  * Rethrown Exceptions (Exceptions/Rethrown ; Dead code)

* 0.8.9

  * Array() / [  ] Consistence (Arrays/ArrayBracketConsistence)
  * Bail Out Early (Structures/BailOutEarly ; Analyze, OneFile, Simple, Level 4)
  * Die Exit Consistence (Structures/DieExitConsistance ; Preferences)
  * Dont Change The Blind Var (Structures/DontChangeBlindKey ; Analyze)
  * More Than One Level Of Indentation (Structures/OneLevelOfIndentation ; Calisthenics)
  * One Dot Or Object Operator Per Line (Structures/OneDotOrObjectOperatorPerLine ; Calisthenics)
  * PHP 7.1 Microseconds (Php/Php71microseconds ; CompatibilityPHP71)
  * Unitialized Properties (Classes/UnitializedProperties ; OneFile, Simple, Suggestions, Level 4, Top10)
  * Useless Check (Structures/UselessCheck ; Analyze, OneFile, Simple, Level 1, CI-checks)

* 0.8.7

  * Don't Echo Error (Security/DontEchoError ; Analyze, Security, Simple, Level 1, CI-checks)
  * No isset() With empty() (Structures/NoIssetWithEmpty ; Analyze, PHP recommendations, OneFile, RadwellCodes, Simple, Level 4, CI-checks)
  * Use ::Class Operator (Classes/UseClassOperator)
  * Useless Type Casting (Structures/UselessCasting ; Analyze, PHP recommendations, OneFile, RadwellCodes, Simple, Level 4, CI-checks)
  * ext/rar (Extensions/Extrar ; Appinfo)
  * time() Vs strtotime() (Performances/timeVsstrtotime ; Performances, OneFile, RadwellCodes)

* 0.8.6

  * Drop Else After Return (Structures/DropElseAfterReturn)
  * Modernize Empty With Expression (Structures/ModernEmpty ; Analyze, OneFile, Simple)
  * Use Positive Condition (Structures/UsePositiveCondition ; Analyze, OneFile, Simple)

* 0.8.5

  * Should Make Ternary (Structures/ShouldMakeTernary ; Analyze, OneFile, Simple, CI-checks)
  * Unused Returned Value (Functions/UnusedReturnedValue)

* 0.8.4

  * $HTTP_RAW_POST_DATA Usage (Php/RawPostDataUsage ; Appinfo, CompatibilityPHP56)
  * $this Belongs To Classes Or Traits (Classes/ThisIsForClasses ; Analyze, Simple)
  * $this Is Not An Array (Classes/ThisIsNotAnArray ; Analyze)
  * $this Is Not For Static Methods (Classes/ThisIsNotForStatic ; Analyze)
  * ** For Exponent (Php/NewExponent ; Suggestions, php-cs-fixable)
  * ::class (Php/StaticclassUsage ; CompatibilityPHP54, CompatibilityPHP53)
  * <?= Usage (Php/EchoTagUsage ; Appinfo, Simple)
  * @ Operator (Structures/Noscream ; Analyze, Appinfo, Performances, ClearPHP, CI-checks)
  * Abstract Class Usage (Classes/Abstractclass ; Appinfo, Appcontent)
  * Abstract Methods Usage (Classes/Abstractmethods ; Appinfo, Appcontent)
  * Abstract Static Methods (Classes/AbstractStatic ; Analyze, Simple)
  * Access Protected Structures (Classes/AccessProtected ; Analyze, Simple)
  * Accessing Private (Classes/AccessPrivate ; Analyze, Simple)
  * Adding Zero (Structures/AddZero ; Analyze, OneFile, ClearPHP, Simple, Level 1, CI-checks)
  * Aliases (Namespaces/Alias ; Appinfo)
  * Aliases Usage (Functions/AliasesUsage ; Analyze, OneFile, ClearPHP, Simple, Level 1, CI-checks)
  * All Uppercase Variables (Variables/VariableUppercase ; Coding Conventions)
  * Already Parents Interface (Interfaces/AlreadyParentsInterface ; Analyze, Suggestions, Level 3)
  * Altering Foreach Without Reference (Structures/AlteringForeachWithoutReference ; Analyze, ClearPHP, Simple, Level 1, CI-checks)
  * Always Positive Comparison (Structures/NeverNegative ; Analyze, Simple, CI-checks)
  * Ambiguous Array Index (Arrays/AmbiguousKeys)
  * Anonymous Classes (Classes/Anonymous ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Argument Should Be Typehinted (Functions/ShouldBeTypehinted ; Typechecks)
  * Array Index (Arrays/Arrayindex ; Appinfo)
  * Assertions (Php/AssertionUsage ; Appinfo)
  * Assign Default To Properties (Classes/MakeDefault ; Analyze, ClearPHP, Simple, Level 2)
  * Autoloading (Php/AutoloadUsage ; Appinfo)
  * Avoid Parenthesis (Structures/PrintWithoutParenthesis ; Analyze, Simple, CI-checks)
  * Avoid Substr() One (Structures/NoSubstrOne ; Analyze, Performances, CompatibilityPHP71, Simple, Suggestions, Level 2, Top10, CI-checks)
  * Avoid Those Hash Functions (Security/AvoidThoseCrypto ; Security)
  * Avoid array_unique() (Structures/NoArrayUnique ; Performances)
  * Avoid get_class() (Structures/UseInstanceof ; Analyze, Simple, CI-checks)
  * Avoid sleep()/usleep() (Security/NoSleep ; Security)
  * Bad Constants Names (Constants/BadConstantnames ; Analyze, PHP recommendations)
  * Binary Glossary (Type/Binary ; Inventory, Appinfo, CompatibilityPHP53)
  * Blind Variables (Variables/Blind ; )
  * Bracketless Blocks (Structures/Bracketless ; Coding Conventions)
  * Break Outside Loop (Structures/BreakOutsideLoop ; Analyze, CompatibilityPHP70)
  * Break With 0 (Structures/Break0 ; CompatibilityPHP53, OneFile)
  * Break With Non Integer (Structures/BreakNonInteger ; CompatibilityPHP54, OneFile)
  * Buried Assignation (Structures/BuriedAssignation ; Analyze)
  * Calltime Pass By Reference (Structures/CalltimePassByReference ; CompatibilityPHP54)
  * Can't Disable Class (Security/CantDisableClass ; Appinfo)
  * Can't Disable Function (Security/CantDisableFunction ; Appinfo, Appcontent)
  * Can't Extend Final (Classes/CantExtendFinal ; Analyze, Dead code, Simple)
  * Cant Use Return Value In Write Context (Php/CantUseReturnValueInWriteContext ; CompatibilityPHP54, CompatibilityPHP53)
  * Cast To Boolean (Structures/CastToBoolean ; Analyze, OneFile, Simple, Level 1)
  * Cast Usage (Php/CastingUsage ; Appinfo)
  * Catch Overwrite Variable (Structures/CatchShadowsVariable ; Analyze, ClearPHP, Simple)
  * Caught Exceptions (Exceptions/CaughtExceptions ; )
  * Caught Expressions (Php/TryCatchUsage ; Appinfo)
  * Class Const With Array (Php/ClassConstWithArray ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * Class Has Fluent Interface (Classes/HasFluentInterface ; )
  * Class Usage (Classes/ClassUsage ; )
  * Class, Interface Or Trait With Identical Names (Classes/CitSameName ; Analyze)
  * Classes Mutually Extending Each Other (Classes/MutualExtension ; LintButWontExec, ClassReview)
  * Classes Names (Classes/Classnames ; Appinfo)
  * Clone Usage (Classes/CloningUsage ; Appinfo)
  * Close Tags (Php/CloseTags ; Coding Conventions)
  * Closure May Use $this (Php/ClosureThisSupport ; CompatibilityPHP53)
  * Closures Glossary (Functions/Closures ; Appinfo)
  * Coalesce (Php/Coalesce ; Appinfo, Appcontent)
  * Common Alternatives (Structures/CommonAlternatives ; Analyze, Simple)
  * Compare Hash (Security/CompareHash ; Security, ClearPHP)
  * Compared Comparison (Structures/ComparedComparison ; Analyze)
  * Composer Namespace (Composer/IsComposerNsname ; Appinfo, Internal)
  * Composer Usage (Composer/UseComposer ; Appinfo)
  * Composer's autoload (Composer/Autoload ; Appinfo)
  * Concrete Visibility (Interfaces/ConcreteVisibility ; Analyze, Simple, LintButWontExec)
  * Conditional Structures (Structures/ConditionalStructures ; )
  * Conditioned Constants (Constants/ConditionedConstants ; Appinfo, Internal)
  * Conditioned Function (Functions/ConditionedFunctions ; Appinfo, Internal)
  * Confusing Names (Variables/CloseNaming ; Under Work)
  * Const With Array (Php/ConstWithArray ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * Constant Class (Classes/ConstantClass ; Analyze, Simple, CI-checks)
  * Constant Comparison (Structures/ConstantComparisonConsistance ; Coding Conventions, Preferences)
  * Constant Conditions (Structures/ConstantConditions ; )
  * Constant Definition (Classes/ConstantDefinition ; Appinfo, Stats)
  * Constant Scalar Expression (Php/ConstantScalarExpression ; )
  * Constant Scalar Expressions (Structures/ConstantScalarExpression ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * Constants (Constants/Constantnames ; Inventory, Stats)
  * Constants Created Outside Its Namespace (Constants/CreatedOutsideItsNamespace ; Analyze)
  * Constants Usage (Constants/ConstantUsage ; Appinfo)
  * Constants With Strange Names (Constants/ConstantStrangeNames ; Analyze, Simple, CI-checks)
  * Constructors (Classes/Constructor ; Internal)
  * Continents (Type/Continents ; )
  * Could Be Class Constant (Classes/CouldBeClassConstant ; ClassReview)
  * Could Be Static (Structures/CouldBeStatic ; Analyze, OneFile, ClassReview)
  * Could Use Alias (Namespaces/CouldUseAlias ; OneFile, Suggestions)
  * Could Use Short Assignation (Structures/CouldUseShortAssignation ; Analyze, Performances, OneFile, Simple, CI-checks)
  * Could Use __DIR__ (Structures/CouldUseDir ; Analyze, Simple, Suggestions, Level 3, php-cs-fixable, CI-checks)
  * Could Use self (Classes/ShouldUseSelf ; Analyze, Simple, Suggestions, Level 3, ClassReview)
  * Custom Class Usage (Classes/AvoidUsing ; Custom)
  * Custom Constant Usage (Constants/CustomConstantUsage ; )
  * Dangling Array References (Structures/DanglingArrayReferences ; Analyze, PHP recommendations, ClearPHP, Simple, Level 1, Top10, CI-checks)
  * Deep Definitions (Functions/DeepDefinitions ; Analyze, Appinfo, Simple)
  * Define With Array (Php/DefineWithArray ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Defined Class Constants (Classes/DefinedConstants ; Internal)
  * Defined Exceptions (Exceptions/DefinedExceptions ; Appinfo)
  * Defined Parent MP (Classes/DefinedParentMP ; Internal)
  * Defined Properties (Classes/DefinedProperty ; Internal)
  * Defined static:: Or self:: (Classes/DefinedStaticMP ; Internal)
  * Definitions Only (Files/DefinitionsOnly ; Internal)
  * Dependant Trait (Traits/DependantTrait ; Analyze, Level 3)
  * Deprecated PHP Functions (Php/Deprecated ; Analyze, CI-checks)
  * Dereferencing String And Arrays (Structures/DereferencingAS ; Appinfo, CompatibilityPHP54, CompatibilityPHP53)
  * Direct Injection (Security/DirectInjection ; Security)
  * Directives Usage (Php/DirectivesUsage ; Appinfo)
  * Don't Change Incomings (Structures/NoChangeIncomingVariables ; Analyze)
  * Double Assignation (Structures/DoubleAssignation ; Analyze)
  * Double Instructions (Structures/DoubleInstruction ; Analyze, Simple)
  * Duplicate Calls (Structures/DuplicateCalls ; )
  * Dynamic Calls (Structures/DynamicCalls ; Appinfo, Internal, Stats)
  * Dynamic Class Constant (Classes/DynamicConstantCall ; Appinfo)
  * Dynamic Classes (Classes/DynamicClass ; Appinfo)
  * Dynamic Code (Structures/DynamicCode ; Appinfo)
  * Dynamic Function Call (Functions/Dynamiccall ; Appinfo, Internal, Stats)
  * Dynamic Methodcall (Classes/DynamicMethodCall ; Appinfo)
  * Dynamic New (Classes/DynamicNew ; Appinfo)
  * Dynamic Property (Classes/DynamicPropertyCall ; Appinfo)
  * Dynamically Called Classes (Classes/VariableClasses ; Appinfo, Stats)
  * Echo Or Print (Structures/EchoPrintConsistance ; Coding Conventions, Preferences)
  * Echo With Concat (Structures/EchoWithConcat ; Analyze, Performances, Simple, Suggestions)
  * Ellipsis Usage (Php/EllipsisUsage ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * Else If Versus Elseif (Structures/ElseIfElseif ; Analyze, Simple, php-cs-fixable, Rector, CI-checks)
  * Else Usage (Structures/ElseUsage ; Appinfo, Appcontent, Calisthenics, Stats)
  * Email Addresses (Type/Email ; Inventory, Appinfo)
  * Empty Blocks (Structures/EmptyBlocks ; Analyze, Simple, CI-checks)
  * Empty Classes (Classes/EmptyClass ; Analyze, Simple)
  * Empty Function (Functions/EmptyFunction ; Analyze, Simple)
  * Empty Instructions (Structures/EmptyLines ; Analyze, Dead code, Simple)
  * Empty Interfaces (Interfaces/EmptyInterface ; Analyze, Simple)
  * Empty List (Php/EmptyList ; Analyze, CompatibilityPHP70)
  * Empty Namespace (Namespaces/EmptyNamespace ; Analyze, Dead code, OneFile, Simple, CI-checks)
  * Empty Slots In Arrays (Arrays/EmptySlots ; Coding Conventions)
  * Empty Traits (Traits/EmptyTrait ; Analyze, Simple)
  * Empty Try Catch (Structures/EmptyTryCatch ; Analyze, Level 3)
  * Empty With Expression (Structures/EmptyWithExpression ; OneFile, Suggestions)
  * Error Messages (Structures/ErrorMessages ; Appinfo)
  * Eval() Usage (Structures/EvalUsage ; Analyze, Appinfo, Security, Performances, OneFile, ClearPHP, Simple)
  * Exception Order (Exceptions/AlreadyCaught ; Dead code)
  * Exit() Usage (Structures/ExitUsage ; Analyze, Appinfo, OneFile, ClearPHP, CI-checks)
  * Exit-like Methods (Functions/KillsApp ; Internal)
  * Exponent Usage (Php/ExponentUsage ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * External Config Files (Files/Services ; Internal)
  * Failed Substr Comparison (Structures/FailingSubstrComparison ; Analyze, Simple, Level 3, Top10, CI-checks)
  * File Is Component (Files/IsComponent ; Internal)
  * File Uploads (Structures/FileUploadUsage ; Appinfo)
  * File Usage (Structures/FileUsage ; Appinfo)
  * Final Class Usage (Classes/Finalclass ; LintButWontExec, ClassReview)
  * Final Methods Usage (Classes/Finalmethod ; LintButWontExec, ClassReview)
  * Fopen Binary Mode (Portability/FopenMode ; Portability)
  * For Using Functioncall (Structures/ForWithFunctioncall ; Performances, ClearPHP, Simple, Level 1, Top10)
  * Foreach Don't Change Pointer (Php/ForeachDontChangePointer ; CompatibilityPHP70)
  * Foreach Needs Reference Array (Structures/ForeachNeedReferencedSource ; Under Work)
  * Foreach Reference Is Not Modified (Structures/ForeachReferenceIsNotModified ; Analyze, Simple, CI-checks)
  * Foreach With list() (Structures/ForeachWithList ; CompatibilityPHP54, CompatibilityPHP53)
  * Forgotten Visibility (Classes/NonPpp ; Analyze, ClearPHP, Simple, Level 1, CI-checks)
  * Forgotten Whitespace (Structures/ForgottenWhiteSpace ; Analyze, CI-checks)
  * Fully Qualified Constants (Namespaces/ConstantFullyQualified ; Analyze)
  * Function Called With Other Case Than Defined (Functions/FunctionCalledWithOtherCase ; )
  * Function Subscripting (Structures/FunctionSubscripting ; Appinfo, CompatibilityPHP53)
  * Function Subscripting, Old Style (Structures/FunctionPreSubscripting ; Suggestions)
  * Functioncall Is Global (Functions/IsGlobal ; Under Work)
  * Functions Glossary (Functions/Functionnames ; Appinfo)
  * Functions In Loop Calls (Functions/LoopCalling ; Under Work)
  * Functions Removed In PHP 5.4 (Php/Php54RemovedFunctions ; CompatibilityPHP54)
  * Functions Removed In PHP 5.5 (Php/Php55RemovedFunctions ; CompatibilityPHP55)
  * Functions Using Reference (Functions/FunctionsUsingReference ; Appinfo, Appcontent)
  * GPRC Aliases (Security/GPRAliases ; Internal)
  * Global Code Only (Files/GlobalCodeOnly ; Internal)
  * Global Import (Namespaces/GlobalImport ; Internal)
  * Global In Global (Structures/GlobalInGlobal ; Appinfo)
  * Global Inside Loop (Structures/GlobalOutsideLoop ; Performances)
  * Global Usage (Structures/GlobalUsage ; Analyze, Appinfo, ClearPHP)
  * Globals (Variables/Globals ; Internal)
  * Goto Names (Php/Gotonames ; Appinfo, ClearPHP)
  * HTTP Status Code (Type/HttpStatus ; Inventory)
  * Hardcoded Passwords (Functions/HardcodedPasswords ; Analyze, Security, OneFile, Simple, Level 3)
  * Has Magic Property (Classes/HasMagicProperty ; Internal)
  * Has Variable Arguments (Functions/VariableArguments ; Appinfo, Internal)
  * Hash Algorithms (Php/HashAlgos ; Analyze, Level 4)
  * Hash Algorithms Incompatible With PHP 5.3 (Php/HashAlgos53 ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Hash Algorithms Incompatible With PHP 5.4/5.5 (Php/HashAlgos54 ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72)
  * Heredoc Delimiter Glossary (Type/Heredoc ; Appinfo)
  * Hexadecimal Glossary (Type/Hexadecimal ; Inventory, Appinfo)
  * Hexadecimal In String (Type/HexadecimalString ; Inventory, CompatibilityPHP70, CompatibilityPHP71)
  * Hidden Use Expression (Namespaces/HiddenUse ; Analyze, OneFile, Simple, CI-checks)
  * Htmlentities Calls (Structures/Htmlentitiescall ; Analyze, Simple, CI-checks)
  * Http Headers (Type/HttpHeader ; Inventory)
  * Identical Conditions (Structures/IdenticalConditions ; Analyze, Simple, CI-checks)
  * If With Same Conditions (Structures/IfWithSameConditions ; Analyze, Simple, CI-checks)
  * Iffectations (Structures/Iffectation ; Analyze)
  * Implement Is For Interface (Classes/ImplementIsForInterface ; Analyze, Simple)
  * Implicit Global (Structures/ImplicitGlobal ; )
  * Implied If (Structures/ImpliedIf ; Analyze, ClearPHP, Simple, CI-checks)
  * Inclusions (Structures/IncludeUsage ; Appinfo)
  * Incompilable Files (Php/Incompilable ; Analyze, Appinfo, ClearPHP, Simple)
  * Inconsistent Concatenation (Structures/InconsistentConcatenation ; Internal)
  * Indices Are Int Or String (Structures/IndicesAreIntOrString ; Analyze, OneFile, Simple, CI-checks)
  * Indirect Injection (Security/IndirectInjection ; Security)
  * Instantiating Abstract Class (Classes/InstantiatingAbstractClass ; Analyze, Simple)
  * Interface Arguments (Variables/InterfaceArguments ; )
  * Interface Methods (Interfaces/InterfaceMethod ; )
  * Interfaces Glossary (Interfaces/Interfacenames ; Appinfo)
  * Interfaces Usage (Interfaces/InterfaceUsage ; )
  * Internally Used Properties (Classes/PropertyUsedInternally ; )
  * Internet Ports (Type/Ports ; Inventory)
  * Interpolation (Type/StringInterpolation ; Coding Conventions)
  * Invalid Constant Name (Constants/InvalidName ; Analyze, Simple)
  * Is An Extension Class (Classes/IsExtClass ; )
  * Is An Extension Constant (Constants/IsExtConstant ; Internal, First)
  * Is An Extension Function (Functions/IsExtFunction ; Internal, First)
  * Is An Extension Interface (Interfaces/IsExtInterface ; Internal, First)
  * Is CLI Script (Files/IsCliScript ; Appinfo, Internal)
  * Is Composer Class (Composer/IsComposerClass ; Internal)
  * Is Composer Interface (Composer/IsComposerInterface ; Internal)
  * Is Extension Trait (Traits/IsExtTrait ; Internal, First)
  * Is Generator (Functions/IsGenerator ; Appinfo, Internal)
  * Is Global Constant (Constants/IsGlobalConstant ; Internal)
  * Is Interface Method (Classes/IsInterfaceMethod ; Internal)
  * Is Library (Project/IsLibrary ; )
  * Is Not Class Family (Classes/IsNotFamily ; Internal)
  * Is PHP Constant (Constants/IsPhpConstant ; Internal)
  * Is Upper Family (Classes/IsUpperFamily ; Internal)
  * Joining file() (Performances/JoinFile ; Performances)
  * Labels (Php/Labelnames ; Appinfo)
  * Linux Only Files (Portability/LinuxOnlyFiles ; Portability)
  * List Short Syntax (Php/ListShortSyntax ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, Internal, CompatibilityPHP53, CompatibilityPHP70)
  * List With Appends (Php/ListWithAppends ; CompatibilityPHP70)
  * List With Keys (Php/ListWithKeys ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, Appcontent, CompatibilityPHP53, CompatibilityPHP70)
  * Locally Unused Property (Classes/LocallyUnusedProperty ; Dead code, Simple)
  * Locally Used Property (Classes/LocallyUsedProperty ; Internal)
  * Logical Mistakes (Structures/LogicalMistakes ; Analyze, Simple, Level 1, CI-checks)
  * Logical Should Use Symbolic Operators (Php/LogicalInLetters ; Analyze, OneFile, ClearPHP, Simple, Suggestions, Level 2, Top10, php-cs-fixable, CI-checks)
  * Lone Blocks (Structures/LoneBlock ; Analyze, Simple, Level 4, CI-checks)
  * Lost References (Variables/LostReferences ; Analyze, Simple)
  * Magic Constant Usage (Constants/MagicConstantUsage ; Appinfo)
  * Magic Methods (Classes/MagicMethod ; Appinfo)
  * Magic Visibility (Classes/toStringPss ; CompatibilityPHP70, Simple)
  * Mail Usage (Structures/MailUsage ; Appinfo)
  * Make Global A Property (Classes/MakeGlobalAProperty ; Analyze, Simple)
  * Make One Call With Array (Performances/MakeOneCall ; Performances)
  * Malformed Octal (Type/MalformedOctal ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Mark Callable (Functions/MarkCallable ; Appinfo, Internal, First)
  * Md5 Strings (Type/Md5String ; Inventory, Appinfo)
  * Method Has Fluent Interface (Functions/HasFluentInterface ; )
  * Method Has No Fluent Interface (Functions/HasNotFluentInterface ; )
  * Methodcall On New (Php/MethodCallOnNew ; CompatibilityPHP53)
  * Methods Without Return (Functions/WithoutReturn ; Analyze)
  * Mime Types (Type/MimeType ; Inventory)
  * Mixed Keys Arrays (Arrays/MixedKeys ; CompatibilityPHP54, CompatibilityPHP53)
  * Multidimensional Arrays (Arrays/Multidimensional ; Appinfo)
  * Multiple Alias Definitions (Namespaces/MultipleAliasDefinitions ; Analyze, Simple, CI-checks)
  * Multiple Catch (Structures/MultipleCatch ; Appinfo, Internal)
  * Multiple Class Declarations (Classes/MultipleDeclarations ; Analyze, Simple, CI-checks)
  * Multiple Classes In One File (Classes/MultipleClassesInFile ; Appinfo, Coding Conventions)
  * Multiple Constant Definition (Constants/MultipleConstantDefinition ; Analyze, Simple, CI-checks)
  * Multiple Definition Of The Same Argument (Functions/MultipleSameArguments ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, OneFile, ClearPHP, Simple)
  * Multiple Exceptions Catch() (Exceptions/MultipleCatch ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * Multiple Identical Trait Or Interface (Classes/MultipleTraitOrInterface ; Analyze, OneFile, Simple, CI-checks)
  * Multiple Index Definition (Arrays/MultipleIdenticalKeys ; Analyze, OneFile, Simple, CI-checks)
  * Multiple Returns (Functions/MultipleReturn ; )
  * Multiples Identical Case (Structures/MultipleDefinedCase ; Analyze, OneFile, ClearPHP, Simple, Level 1, CI-checks)
  * Multiply By One (Structures/MultiplyByOne ; Analyze, OneFile, ClearPHP, Simple, Level 1, CI-checks)
  * Must Return Methods (Functions/MustReturn ; Analyze, Simple, Level 2, LintButWontExec, CI-checks)
  * Namespaces (Namespaces/NamespaceUsage ; Appinfo)
  * Namespaces Glossary (Namespaces/Namespacesnames ; Appinfo)
  * Negative Power (Structures/NegativePow ; Analyze, OneFile, Simple, Level 3, CI-checks)
  * Nested Ifthen (Structures/NestedIfthen ; Analyze, RadwellCodes)
  * Nested Loops (Structures/NestedLoops ; Appinfo)
  * Nested Ternary (Structures/NestedTernary ; Analyze, ClearPHP, Simple, Level 1, CI-checks)
  * Never Used Properties (Classes/PropertyNeverUsed ; Analyze, Simple)
  * New Functions In PHP 5.4 (Php/Php54NewFunctions ; CompatibilityPHP53)
  * New Functions In PHP 5.5 (Php/Php55NewFunctions ; CompatibilityPHP54, CompatibilityPHP53)
  * New Functions In PHP 5.6 (Php/Php56NewFunctions ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * New Functions In PHP 7.0 (Php/Php70NewFunctions ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * New Functions In PHP 7.1 (Php/Php71NewFunctions ; CompatibilityPHP71)
  * No Choice (Structures/NoChoice ; Analyze, Simple, Level 2, Top10, CI-checks)
  * No Count With 0 (Performances/NotCountNull ; Performances)
  * No Direct Access (Structures/NoDirectAccess ; Appinfo)
  * No Direct Call To Magic Method (Classes/DirectCallToMagicMethod ; Analyze, Level 2, CI-checks)
  * No Direct Usage (Structures/NoDirectUsage ; Analyze, Simple)
  * No Hardcoded Hash (Structures/NoHardcodedHash ; Analyze, Security, Simple)
  * No Hardcoded Ip (Structures/NoHardcodedIp ; Analyze, Security, ClearPHP, Simple)
  * No Hardcoded Path (Structures/NoHardcodedPath ; Analyze, ClearPHP, Simple)
  * No Hardcoded Port (Structures/NoHardcodedPort ; Analyze, Security, ClearPHP, Simple)
  * No List With String (Php/NoListWithString ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * No Parenthesis For Language Construct (Structures/NoParenthesisForLanguageConstruct ; Analyze, ClearPHP, RadwellCodes, Simple, Suggestions, Level 2, CI-checks)
  * No Plus One (Structures/PlusEgalOne ; Coding Conventions, OneFile)
  * No Public Access (Classes/NoPublicAccess ; Analyze)
  * No Real Comparison (Type/NoRealComparison ; Analyze, Simple, Level 2, Top10, CI-checks)
  * No Self Referencing Constant (Classes/NoSelfReferencingConstant ; Analyze, Simple, LintButWontExec, ClassReview)
  * No String With Append (Php/NoStringWithAppend ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * No array_merge() In Loops (Performances/ArrayMergeInLoops ; Analyze, Performances, ClearPHP, Simple, Level 2, Top10, CI-checks)
  * Non Ascii Variables (Variables/VariableNonascii ; Analyze)
  * Non Static Methods Called In A Static (Classes/NonStaticMethodsCalledStatic ; Analyze, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, Simple, CI-checks)
  * Non-constant Index In Array (Arrays/NonConstantArray ; Analyze, Simple)
  * Non-lowercase Keywords (Php/UpperCaseKeyword ; Coding Conventions, RadwellCodes)
  * Normal Methods (Classes/NormalMethods ; Appcontent)
  * Not Definitions Only (Files/NotDefinitionsOnly ; Appinfo)
  * Not Not (Structures/NotNot ; Analyze, OneFile, Simple, CI-checks)
  * Not Same Name As File (Classes/NotSameNameAsFile ; )
  * Not Same Name As File (Classes/SameNameAsFile ; Internal)
  * Nowdoc Delimiter Glossary (Type/Nowdoc ; Appinfo)
  * Null Coalesce (Php/NullCoalesce ; )
  * Null On New (Classes/NullOnNew ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, OneFile, Simple)
  * Objects Don't Need References (Structures/ObjectReferences ; Analyze, OneFile, ClearPHP, Simple, Level 2, Top10, CI-checks)
  * Octal Glossary (Type/Octal ; Appinfo)
  * Old Style Constructor (Classes/OldStyleConstructor ; Analyze, Appinfo, OneFile, ClearPHP, Simple, CompatibilityPHP80)
  * Old Style __autoload() (Php/oldAutoloadUsage ; Analyze, OneFile, ClearPHP, Simple)
  * One Letter Functions (Functions/OneLetterFunctions ; Coding Conventions, Semantics)
  * One Object Operator Per Line (Classes/OneObjectOperatorPerLine ; Calisthenics)
  * One Variable String (Type/OneVariableStrings ; Analyze, RadwellCodes, Simple, CI-checks)
  * Only Static Methods (Classes/OnlyStaticMethods ; Internal)
  * Only Variable Returned By Reference (Structures/OnlyVariableReturnedByReference ; Analyze, Simple)
  * Or Die (Structures/OrDie ; Analyze, OneFile, ClearPHP, Simple, CI-checks)
  * Overwriting Variable (Variables/Overwriting ; )
  * Overwritten Class Const (Classes/OverwrittenConst ; Appinfo)
  * Overwritten Exceptions (Exceptions/OverwriteException ; Analyze, Simple, Suggestions, Level 4, CI-checks)
  * Overwritten Literals (Variables/OverwrittenLiterals ; Analyze)
  * PHP 7.0 New Classes (Php/Php70NewClasses ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * PHP 7.0 New Interfaces (Php/Php70NewInterfaces ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * PHP 7.0 Removed Directives (Php/Php70RemovedDirective ; CompatibilityPHP70, CompatibilityPHP71)
  * PHP 7.0 Removed Functions (Php/Php70RemovedFunctions ; CompatibilityPHP70, CompatibilityPHP71)
  * PHP 7.1 Removed Directives (Php/Php71RemovedDirective ; CompatibilityPHP71)
  * PHP Alternative Syntax (Php/AlternativeSyntax ; Appinfo)
  * PHP Arrays Index (Arrays/Phparrayindex ; Appinfo)
  * PHP Bugfixes (Php/MiddleVersion ; Appinfo, Appcontent)
  * PHP Constant Usage (Constants/PhpConstantUsage ; Appinfo)
  * PHP Handlers Usage (Php/SetHandlers ; )
  * PHP Interfaces (Interfaces/Php ; )
  * PHP Keywords As Names (Php/ReservedNames ; Analyze, Simple)
  * PHP Sapi (Type/Sapi ; Internal)
  * PHP Variables (Variables/VariablePhp ; )
  * PHP5 Indirect Variable Expression (Variables/Php5IndirectExpression ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * PHP7 Dirname (Structures/PHP7Dirname ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, Suggestions, php-cs-fixable)
  * Parent, Static Or Self Outside Class (Classes/PssWithoutClass ; Analyze, Simple)
  * Parenthesis As Parameter (Php/ParenthesisAsParameter ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Pear Usage (Php/PearUsage ; Appinfo, Appcontent)
  * Perl Regex (Type/Pcre ; Inventory)
  * Php 7 Indirect Expression (Variables/Php7IndirectExpression ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * Php 7.1 New Class (Php/Php71NewClasses ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * Php7 Relaxed Keyword (Php/Php7RelaxedKeyword ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Phpinfo (Structures/PhpinfoUsage ; Security, OneFile, Simple)
  * Pre-increment (Performances/PrePostIncrement ; Analyze, Performances, Simple, Level 4, CI-checks)
  * Preprocess Arrays (Arrays/ShouldPreprocess ; Suggestions)
  * Preprocessable (Structures/ShouldPreprocess ; Analyze, Rector)
  * Print And Die (Structures/PrintAndDie ; Analyze, Simple, CI-checks)
  * Property Could Be Private Property (Classes/CouldBePrivate ; ClassReview)
  * Property Names (Classes/PropertyDefinition ; Internal)
  * Property Used Above (Classes/PropertyUsedAbove ; Internal)
  * Property Used Below (Classes/PropertyUsedBelow ; Internal)
  * Property Variable Confusion (Structures/PropertyVariableConfusion ; Semantics)
  * Queries In Loops (Structures/QueriesInLoop ; Analyze, OneFile, Simple, Level 1, Top10)
  * Random Without Try (Structures/RandomWithoutTry ; Security)
  * Real Functions (Functions/RealFunctions ; Appcontent, Stats)
  * Real Variables (Variables/RealVariables ; Under Work)
  * Recursive Functions (Functions/Recursive ; Appinfo)
  * Redeclared PHP Functions (Functions/RedeclaredPhpFunction ; Analyze, Appinfo, Simple, CI-checks)
  * Redefined Class Constants (Classes/RedefinedConstants ; Analyze, Simple, CI-checks)
  * Redefined Default (Classes/RedefinedDefault ; Analyze, Simple, CI-checks)
  * Redefined Methods (Classes/RedefinedMethods ; Appinfo)
  * Redefined PHP Traits (Traits/Php ; Appinfo)
  * Redefined Property (Classes/RedefinedProperty ; ClassReview)
  * References (Variables/References ; Appinfo)
  * Register Globals (Security/RegisterGlobals ; Security)
  * Relay Function (Functions/RelayFunction ; Analyze)
  * Repeated print() (Structures/RepeatedPrint ; Analyze, Simple, Suggestions, Level 3, Top10, CI-checks)
  * Reserved Keywords In PHP 7 (Php/ReservedKeywords7 ; CompatibilityPHP70)
  * Resources Usage (Structures/ResourcesUsage ; Appinfo)
  * Results May Be Missing (Structures/ResultMayBeMissing ; Analyze, Simple, CI-checks)
  * Return True False (Structures/ReturnTrueFalse ; Analyze, Simple, Level 1, CI-checks)
  * Return Typehint Usage (Php/ReturnTypehintUsage ; Appinfo, Internal)
  * Return With Parenthesis (Php/ReturnWithParenthesis ; Coding Conventions, PHP recommendations, Suggestions)
  * Return void  (Structures/ReturnVoid ; )
  * Safe Curl Options (Security/CurlOptions ; Security)
  * Same Conditions In Condition (Structures/SameConditions ; Analyze, Simple, CI-checks)
  * Scalar Typehint Usage (Php/ScalarTypehintUsage ; Appinfo)
  * Sensitive Argument (Security/SensitiveArgument ; Internal)
  * Sequences In For (Structures/SequenceInFor ; )
  * Setlocale() Uses Constants (Structures/SetlocaleNeedsConstants ; CompatibilityPHP70)
  * Several Instructions On The Same Line (Structures/OneLineTwoInstructions ; Analyze)
  * Shell Usage (Structures/ShellUsage ; Appinfo)
  * Short Open Tags (Php/ShortOpenTagRequired ; Analyze, Simple)
  * Short Syntax For Arrays (Arrays/ArrayNSUsage ; Appinfo, CompatibilityPHP53)
  * Should Be Single Quote (Type/ShouldBeSingleQuote ; Coding Conventions, ClearPHP)
  * Should Chain Exception (Structures/ShouldChainException ; Analyze, Simple, CI-checks)
  * Should Make Alias (Namespaces/ShouldMakeAlias ; Analyze, OneFile, Simple, CI-checks)
  * Should Typecast (Type/ShouldTypecast ; Analyze, OneFile, Simple, CI-checks)
  * Should Use Coalesce (Php/ShouldUseCoalesce ; Analyze, Simple, Suggestions, Level 3, CI-checks)
  * Should Use Constants (Functions/ShouldUseConstants ; Analyze, Simple)
  * Should Use Local Class (Classes/ShouldUseThis ; Analyze, ClearPHP, Simple)
  * Should Use Prepared Statement (Security/ShouldUsePreparedStatement ; Analyze, Security, Simple, CI-checks)
  * Silently Cast Integer (Type/SilentlyCastInteger ; Analyze, Simple, CI-checks)
  * Simple Global Variable (Php/GlobalWithoutSimpleVariable ; CompatibilityPHP70)
  * Simplify Regex (Structures/SimplePreg ; Performances)
  * Slow Functions (Performances/SlowFunctions ; Performances, OneFile)
  * Special Integers (Type/SpecialIntegers ; Inventory)
  * Static Loop (Structures/StaticLoop ; Analyze, Simple, Level 4)
  * Static Methods (Classes/StaticMethods ; Appinfo)
  * Static Methods Called From Object (Classes/StaticMethodsCalledFromObject ; Analyze, Simple, CI-checks)
  * Static Methods Can't Contain $this (Classes/StaticContainsThis ; Analyze, ClearPHP, Simple, Level 1, CI-checks)
  * Static Properties (Classes/StaticProperties ; Appinfo)
  * Static Variables (Variables/StaticVariables ; Appinfo)
  * Strict Comparison With Booleans (Structures/BooleanStrictComparison ; Analyze, Simple, Suggestions, Level 2, CI-checks)
  * String May Hold A Variable (Type/StringHoldAVariable ; Analyze, Simple)
  * String glossary (Type/String ; )
  * Strpos()-like Comparison (Structures/StrposCompare ; Analyze, PHP recommendations, ClearPHP, Simple, Level 2, Top10, CI-checks)
  * Super Global Usage (Php/SuperGlobalUsage ; Appinfo)
  * Super Globals Contagion (Security/SuperGlobalContagion ; Internal)
  * Switch To Switch (Structures/SwitchToSwitch ; Analyze, RadwellCodes, Simple)
  * Switch With Too Many Default (Structures/SwitchWithMultipleDefault ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, ClearPHP, Simple)
  * Switch Without Default (Structures/SwitchWithoutDefault ; Analyze, ClearPHP, Simple, CI-checks)
  * Ternary In Concat (Structures/TernaryInConcat ; Analyze, Simple, Level 3, CI-checks)
  * Test Class (Classes/TestClass ; Appinfo)
  * Throw (Php/ThrowUsage ; Appinfo)
  * Throw Functioncall (Exceptions/ThrowFunctioncall ; Analyze, Simple, Level 1, CI-checks)
  * Throw In Destruct (Classes/ThrowInDestruct ; Analyze, Simple, CI-checks)
  * Thrown Exceptions (Exceptions/ThrownExceptions ; Appinfo)
  * Throws An Assignement (Structures/ThrowsAndAssign ; Analyze, Simple, CI-checks)
  * Timestamp Difference (Structures/TimestampDifference ; Analyze, Simple, Level 3, CI-checks)
  * Too Many Children (Classes/TooManyChildren ; Suggestions)
  * Trait Methods (Traits/TraitMethod ; )
  * Trait Names (Traits/Traitnames ; Appinfo)
  * Traits Usage (Traits/TraitUsage ; Appinfo)
  * Trigger Errors (Php/TriggerErrorUsage ; Appinfo)
  * True False Inconsistant Case (Constants/InconsistantCase ; Preferences)
  * Try With Finally (Structures/TryFinally ; Appinfo, Internal)
  * Typehints (Functions/Typehints ; Appinfo)
  * URL List (Type/Url ; Inventory, Appinfo)
  * Uncaught Exceptions (Exceptions/UncaughtExceptions ; Analyze)
  * Unchecked Resources (Structures/UncheckedResources ; Analyze, ClearPHP, Simple, Level 2, CI-checks)
  * Undefined Caught Exceptions (Exceptions/CaughtButNotThrown ; Dead code)
  * Undefined Class Constants (Classes/UndefinedConstants ; Analyze, CI-checks)
  * Undefined Classes (Classes/UndefinedClasses ; Analyze)
  * Undefined Constants (Constants/UndefinedConstants ; Analyze, CompatibilityPHP72, Simple, CI-checks)
  * Undefined Functions (Functions/UndefinedFunctions ; Analyze, CI-checks)
  * Undefined Interfaces (Interfaces/UndefinedInterfaces ; Analyze, CI-checks)
  * Undefined Parent (Classes/UndefinedParentMP ; Analyze, Simple)
  * Undefined Properties (Classes/UndefinedProperty ; Analyze, ClearPHP, Simple, CI-checks)
  * Undefined Trait (Traits/UndefinedTrait ; Analyze, LintButWontExec, CI-checks)
  * Undefined static:: Or self:: (Classes/UndefinedStaticMP ; Analyze, Simple)
  * Unicode Blocks (Type/UnicodeBlock ; Inventory)
  * Unicode Escape Partial (Php/UnicodeEscapePartial ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Unicode Escape Syntax (Php/UnicodeEscapeSyntax ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * Unknown Directive Name (Php/DirectiveName ; Internal)
  * Unkown Regex Options (Structures/UnknownPregOption ; Analyze, Simple)
  * Unpreprocessed Values (Structures/Unpreprocessed ; Analyze, OneFile, ClearPHP, Simple)
  * Unreachable Code (Structures/UnreachableCode ; Dead code, OneFile, ClearPHP, Simple, Suggestions, Level 3)
  * Unresolved Catch (Classes/UnresolvedCatch ; Dead code, ClearPHP)
  * Unresolved Classes (Classes/UnresolvedClasses ; Analyze)
  * Unresolved Instanceof (Classes/UnresolvedInstanceof ; Analyze, Dead code, ClearPHP, Simple, Top10)
  * Unresolved Use (Namespaces/UnresolvedUse ; Analyze, ClearPHP, Simple)
  * Unserialize Second Arg (Security/UnserializeSecondArg ; Security)
  * Unset Arguments (Functions/UnsetOnArguments ; OneFile)
  * Unset In Foreach (Structures/UnsetInForeach ; Analyze, Dead code, OneFile, Simple)
  * Unthrown Exception (Exceptions/Unthrown ; Analyze, Dead code, ClearPHP, Simple)
  * Unused Arguments (Functions/UnusedArguments ; Analyze, Simple)
  * Unused Classes (Classes/UnusedClass ; Analyze, Dead code, Simple)
  * Unused Constants (Constants/UnusedConstants ; Dead code, Simple)
  * Unused Functions (Functions/UnusedFunctions ; Dead code, Simple)
  * Unused Global (Structures/UnusedGlobal ; Analyze, Simple)
  * Unused Interfaces (Interfaces/UnusedInterfaces ; Dead code, Simple, Suggestions, Level 2)
  * Unused Label (Structures/UnusedLabel ; Dead code, Simple)
  * Unused Methods (Classes/UnusedMethods ; Dead code, Simple)
  * Unused Private Methods (Classes/UnusedPrivateMethod ; Dead code, OneFile, Simple)
  * Unused Private Properties (Classes/UnusedPrivateProperty ; Dead code, OneFile, Simple)
  * Unused Protected Methods (Classes/UnusedProtectedMethods ; Dead code)
  * Unused Traits (Traits/UnusedTrait ; Simple)
  * Unused Use (Namespaces/UnusedUse ; Dead code, ClearPHP, Simple)
  * Unusual Case For PHP Functions (Php/UpperCaseFunction ; Coding Conventions)
  * Usage Of class_alias() (Classes/ClassAliasUsage ; Appinfo)
  * Use === null (Php/IsnullVsEqualNull ; Analyze, OneFile, RadwellCodes, Simple, php-cs-fixable, CI-checks)
  * Use Cli (Php/UseCli ; Appinfo)
  * Use Const And Functions (Namespaces/UseFunctionsConstants ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * Use Constant (Structures/UseConstant ; Analyze, PHP recommendations, php-cs-fixable, CI-checks)
  * Use Constant As Arguments (Functions/UseConstantAsArguments ; Analyze, Simple, CI-checks)
  * Use Instanceof (Classes/UseInstanceof ; Analyze, Simple, CI-checks)
  * Use Lower Case For Parent, Static And Self (Php/CaseForPSS ; CompatibilityPHP54, CompatibilityPHP53)
  * Use Nullable Type (Php/UseNullableType ; Appinfo, CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53, CompatibilityPHP70)
  * Use PHP Object API (Php/UseObjectApi ; Analyze, ClearPHP, Simple, CI-checks)
  * Use Pathinfo (Php/UsePathinfo ; Analyze, Simple, Level 3, CI-checks)
  * Use System Tmp (Structures/UseSystemTmp ; Analyze, Simple, Level 3, CI-checks)
  * Use This (Classes/UseThis ; Internal)
  * Use Web (Php/UseWeb ; Appinfo)
  * Use With Fully Qualified Name (Namespaces/UseWithFullyQualifiedNS ; Analyze, Coding Conventions, PHP recommendations, Simple)
  * Use const (Constants/ConstRecommended ; Analyze, Coding Conventions, Top10, CI-checks)
  * Use password_hash() (Php/Password55 ; CompatibilityPHP55)
  * Use random_int() (Php/BetterRand ; Analyze, Security, CompatibilityPHP71, Simple, Level 2, CI-checks)
  * Used Classes (Classes/UsedClass ; Internal)
  * Used Functions (Functions/UsedFunctions ; Internal)
  * Used Interfaces (Interfaces/UsedInterfaces ; Internal)
  * Used Methods (Classes/UsedMethods ; Internal)
  * Used Once Variables (In Scope) (Variables/VariableUsedOnceByContext ; Analyze, OneFile, ClearPHP, Simple, Level 4)
  * Used Once Variables (Variables/VariableUsedOnce ; Analyze, OneFile, Simple, Top10)
  * Used Private Methods (Classes/UsedPrivateMethod ; Internal)
  * Used Protected Method (Classes/UsedProtectedMethod ; )
  * Used Static Properties (Classes/UsedPrivateProperty ; Internal)
  * Used Trait (Traits/UsedTrait ; Internal)
  * Used Use (Namespaces/UsedUse ; )
  * Useless Abstract Class (Classes/UselessAbstract ; Analyze, Simple)
  * Useless Brackets (Structures/UselessBrackets ; Analyze, RadwellCodes, Simple, CI-checks)
  * Useless Constructor (Classes/UselessConstructor ; Analyze, Simple, Level 3)
  * Useless Final (Classes/UselessFinal ; Analyze, OneFile, ClearPHP, Simple, CI-checks)
  * Useless Global (Structures/UselessGlobal ; Analyze, OneFile, Simple, Level 2)
  * Useless Instructions (Structures/UselessInstruction ; Analyze, OneFile, ClearPHP, Simple, Level 1, CI-checks)
  * Useless Interfaces (Interfaces/UselessInterfaces ; Analyze, ClearPHP, Simple, ClassReview, Typechecks)
  * Useless Parenthesis (Structures/UselessParenthesis ; Analyze, Simple, CI-checks)
  * Useless Return (Functions/UselessReturn ; Analyze, OneFile, Simple, Level 4)
  * Useless Switch (Structures/UselessSwitch ; Analyze, Simple)
  * Useless Unset (Structures/UselessUnset ; Analyze, OneFile, ClearPHP, Simple, Level 2, CI-checks)
  * Uses Default Values (Functions/UsesDefaultArguments ; Analyze, Simple, CI-checks)
  * Uses Environment (Php/UsesEnv ; Appinfo, Appcontent)
  * Using $this Outside A Class (Classes/UsingThisOutsideAClass ; Analyze, CompatibilityPHP71, Simple, LintButWontExec)
  * Using Short Tags (Structures/ShortTags ; Appinfo)
  * Usort Sorting In PHP 7.0 (Php/UsortSorting ; CompatibilityPHP70)
  * Var Keyword (Classes/OldStyleVar ; Analyze, OneFile, ClearPHP, Simple, Level 1)
  * Variable Constants (Constants/VariableConstant ; Appinfo, Stats)
  * Variables Variables (Variables/VariableVariables ; Appinfo, Stats)
  * Variables With Long Names (Variables/VariableLong ; Appinfo)
  * Variables With One Letter Names (Variables/VariableOneLetter ; Semantics)
  * While(List() = Each()) (Structures/WhileListEach ; Analyze, Performances, OneFile, Simple, Suggestions, Level 2, CI-checks)
  * Written Only Variables (Variables/WrittenOnlyVariable ; Analyze, OneFile, Simple)
  * Wrong Class Name Case (Classes/WrongCase ; Coding Conventions, RadwellCodes, Simple)
  * Wrong Function Name Case (Functions/WrongCase ; Coding Conventions)
  * Wrong Number Of Arguments (Functions/WrongNumberOfArguments ; Analyze, OneFile, Simple, CI-checks)
  * Wrong Number Of Arguments In Methods (Functions/WrongNumberOfArgumentsMethods ; Under Work)
  * Wrong Optional Parameter (Functions/WrongOptionalParameter ; Analyze, Simple, Level 1, CI-checks)
  * Wrong Parameter Type (Php/InternalParameterType ; Analyze, OneFile, Simple, CI-checks)
  * Wrong fopen() Mode (Php/FopenMode ; Analyze, CI-checks)
  * Yield From Usage (Php/YieldFromUsage ; Appinfo, Appcontent)
  * Yield Usage (Php/YieldUsage ; Appinfo, Appcontent)
  * Yoda Comparison (Structures/YodaComparison ; Coding Conventions)
  * __debugInfo() Usage (Php/debugInfoUsage ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP53)
  * __halt_compiler (Php/Haltcompiler ; Appinfo)
  * __toString() Throws Exception (Structures/toStringThrowsException ; Analyze, OneFile, Simple)
  * crypt() Without Salt (Structures/CryptWithoutSalt ; CompatibilityPHP54)
  * error_reporting() With Integers (Structures/ErrorReportingWithInteger ; Analyze, Simple, CI-checks)
  * eval() Without Try (Structures/EvalWithoutTry ; Analyze, Security, Simple, Level 3, CI-checks)
  * ext/0mq (Extensions/Extzmq ; Appinfo)
  * ext/amqp (Extensions/Extamqp ; Appinfo)
  * ext/apache (Extensions/Extapache ; Appinfo)
  * ext/apc (Extensions/Extapc ; Appinfo, CompatibilityPHP55)
  * ext/apcu (Extensions/Extapcu ; Appinfo)
  * ext/array (Extensions/Extarray ; Appinfo)
  * ext/bcmath (Extensions/Extbcmath ; Appinfo)
  * ext/bzip2 (Extensions/Extbzip2 ; Appinfo)
  * ext/cairo (Extensions/Extcairo ; Appinfo)
  * ext/calendar (Extensions/Extcalendar ; Appinfo)
  * ext/com (Extensions/Extcom ; Appinfo)
  * ext/crypto (Extensions/Extcrypto ; Appinfo)
  * ext/ctype (Extensions/Extctype ; Appinfo)
  * ext/curl (Extensions/Extcurl ; Appinfo)
  * ext/cyrus (Extensions/Extcyrus ; Appinfo)
  * ext/date (Extensions/Extdate ; Appinfo)
  * ext/dba (Extensions/Extdba ; Appinfo, CompatibilityPHP53)
  * ext/dio (Extensions/Extdio ; Appinfo)
  * ext/dom (Extensions/Extdom ; Appinfo)
  * ext/eaccelerator (Extensions/Exteaccelerator ; Appinfo)
  * ext/enchant (Extensions/Extenchant ; Appinfo)
  * ext/ereg (Extensions/Extereg ; Appinfo, CompatibilityPHP70)
  * ext/ev (Extensions/Extev ; Appinfo)
  * ext/event (Extensions/Extevent ; Appinfo)
  * ext/exif (Extensions/Extexif ; Appinfo)
  * ext/expect (Extensions/Extexpect ; Appinfo)
  * ext/fann (Extensions/Extfann ; Appinfo)
  * ext/fdf (Extensions/Extfdf ; Appinfo, CompatibilityPHP53)
  * ext/ffmpeg (Extensions/Extffmpeg ; Appinfo)
  * ext/file (Extensions/Extfile ; Appinfo)
  * ext/fileinfo (Extensions/Extfileinfo ; Appinfo)
  * ext/filter (Extensions/Extfilter ; Appinfo)
  * ext/fpm (Extensions/Extfpm ; Appinfo)
  * ext/ftp (Extensions/Extftp ; Appinfo)
  * ext/gd (Extensions/Extgd ; Appinfo)
  * ext/gearman (Extensions/Extgearman ; Appinfo)
  * ext/geoip (Extensions/Extgeoip ; Appinfo)
  * ext/gettext (Extensions/Extgettext ; Appinfo)
  * ext/gmagick (Extensions/Extgmagick ; Appinfo)
  * ext/gmp (Extensions/Extgmp ; Appinfo)
  * ext/gnupgp (Extensions/Extgnupg ; Appinfo)
  * ext/hash (Extensions/Exthash ; Appinfo)
  * ext/ibase (Extensions/Extibase ; Appinfo)
  * ext/iconv (Extensions/Exticonv ; Appinfo)
  * ext/iis (Extensions/Extiis ; Appinfo, Portability)
  * ext/imagick (Extensions/Extimagick ; Appinfo)
  * ext/imap (Extensions/Extimap ; Appinfo)
  * ext/info (Extensions/Extinfo ; Appinfo)
  * ext/inotify (Extensions/Extinotify ; Appinfo)
  * ext/intl (Extensions/Extintl ; Appinfo)
  * ext/json (Extensions/Extjson ; Appinfo)
  * ext/kdm5 (Extensions/Extkdm5 ; Appinfo)
  * ext/ldap (Extensions/Extldap ; Appinfo)
  * ext/libevent (Extensions/Extlibevent ; Appinfo)
  * ext/libxml (Extensions/Extlibxml ; Appinfo)
  * ext/lua (Extensions/Extlua ; Appinfo)
  * ext/mail (Extensions/Extmail ; Appinfo)
  * ext/mailparse (Extensions/Extmailparse ; Appinfo)
  * ext/math (Extensions/Extmath ; Appinfo)
  * ext/mbstring (Extensions/Extmbstring ; Appinfo)
  * ext/mcrypt (Extensions/Extmcrypt ; Appinfo, CompatibilityPHP71)
  * ext/memcache (Extensions/Extmemcache ; Appinfo)
  * ext/memcached (Extensions/Extmemcached ; Appinfo)
  * ext/ming (Extensions/Extming ; Appinfo, CompatibilityPHP53)
  * ext/mongo (Extensions/Extmongo ; Appinfo)
  * ext/mssql (Extensions/Extmssql ; Appinfo)
  * ext/mysql (Extensions/Extmysql ; Appinfo, CompatibilityPHP55)
  * ext/mysqli (Extensions/Extmysqli ; Appinfo)
  * ext/ob (Extensions/Extob ; Appinfo)
  * ext/oci8 (Extensions/Extoci8 ; Appinfo)
  * ext/odbc (Extensions/Extodbc ; Appinfo)
  * ext/opcache (Extensions/Extopcache ; Appinfo)
  * ext/openssl (Extensions/Extopenssl ; Appinfo)
  * ext/parsekit (Extensions/Extparsekit ; Appinfo)
  * ext/password (Extensions/Extpassword ; Appinfo, Appcontent)
  * ext/pcntl (Extensions/Extpcntl ; Appinfo)
  * ext/pcre (Extensions/Extpcre ; Appinfo)
  * ext/pdo (Extensions/Extpdo ; Appinfo)
  * ext/pecl_http (Extensions/Exthttp ; Appinfo, Appcontent)
  * ext/pgsql (Extensions/Extpgsql ; Appinfo)
  * ext/phalcon (Extensions/Extphalcon ; Appinfo)
  * ext/phar (Extensions/Extphar ; Appinfo)
  * ext/php-ast (Extensions/Extast ; Appinfo)
  * ext/posix (Extensions/Extposix ; Appinfo)
  * ext/proctitle (Extensions/Extproctitle ; Appinfo)
  * ext/pspell (Extensions/Extpspell ; Appinfo)
  * ext/readline (Extensions/Extreadline ; Appinfo)
  * ext/recode (Extensions/Extrecode ; Appinfo, Portability)
  * ext/redis (Extensions/Extredis ; Appinfo)
  * ext/reflection (Extensions/Extreflection ; Appinfo)
  * ext/runkit (Extensions/Extrunkit ; Appinfo)
  * ext/sem (Extensions/Extsem ; Appinfo)
  * ext/session (Extensions/Extsession ; Appinfo)
  * ext/shmop (Extensions/Extshmop ; Appinfo)
  * ext/simplexml (Extensions/Extsimplexml ; Appinfo)
  * ext/snmp (Extensions/Extsnmp ; Appinfo)
  * ext/soap (Extensions/Extsoap ; Appinfo)
  * ext/sockets (Extensions/Extsockets ; Appinfo)
  * ext/spl (Extensions/Extspl ; Appinfo)
  * ext/sqlite (Extensions/Extsqlite ; Appinfo)
  * ext/sqlite3 (Extensions/Extsqlite3 ; Appinfo)
  * ext/sqlsrv (Extensions/Extsqlsrv ; Appinfo)
  * ext/ssh2 (Extensions/Extssh2 ; Appinfo)
  * ext/standard (Extensions/Extstandard ; Appinfo)
  * ext/suhosin (Extensions/Extsuhosin ; Appinfo)
  * ext/tidy (Extensions/Exttidy ; Appinfo)
  * ext/tokenizer (Extensions/Exttokenizer ; Appinfo)
  * ext/tokyotyrant (Extensions/Exttokyotyrant ; Appinfo)
  * ext/trader (Extensions/Exttrader ; Appinfo)
  * ext/v8js (Extensions/Extv8js ; Appinfo)
  * ext/wddx (Extensions/Extwddx ; Appinfo)
  * ext/wikidiff2 (Extensions/Extwikidiff2 ; Appinfo)
  * ext/wincache (Extensions/Extwincache ; Appinfo, Portability)
  * ext/xcache (Extensions/Extxcache ; Appinfo)
  * ext/xdebug (Extensions/Extxdebug ; Appinfo)
  * ext/xdiff (Extensions/Extxdiff ; Appinfo)
  * ext/xhprof (Extensions/Extxhprof ; Appinfo)
  * ext/xml (Extensions/Extxml ; Appinfo)
  * ext/xmlreader (Extensions/Extxmlreader ; Appinfo)
  * ext/xmlrpc (Extensions/Extxmlrpc ; Appinfo)
  * ext/xmlwriter (Extensions/Extxmlwriter ; Appinfo)
  * ext/xsl (Extensions/Extxsl ; Appinfo)
  * ext/yaml (Extensions/Extyaml ; Appinfo)
  * ext/yis (Extensions/Extyis ; Appinfo)
  * ext/zip (Extensions/Extzip ; Appinfo)
  * ext/zlib (Extensions/Extzlib ; Appinfo)
  * func_get_arg() Modified (Functions/funcGetArgModified ; Analyze, CompatibilityPHP70, Simple)
  * include_once() Usage (Structures/OnceUsage ; Analyze, Appinfo)
  * isset() With Constant (Structures/IssetWithConstant ; CompatibilityPHP54, CompatibilityPHP55, CompatibilityPHP56, CompatibilityPHP53)
  * list() May Omit Variables (Structures/ListOmissions ; Analyze, Simple, Suggestions, Level 3, CI-checks)
  * mcrypt_create_iv() With Default Values (Structures/McryptcreateivWithoutOption ; CompatibilityPHP70)
  * parse_str() Warning (Security/parseUrlWithoutParameters ; Security)
  * preg_match_all() Flag (Php/PregMatchAllFlag ; Simple, Suggestions)
  * preg_replace With Option e (Structures/pregOptionE ; Analyze, Security, CompatibilityPHP70, CompatibilityPHP71, CompatibilityPHP72, Simple, CI-checks)
  * set_exception_handler() Warning (Php/SetExceptionHandlerPHP7 ; CompatibilityPHP70)
  * var_dump()... Usage (Structures/VardumpUsage ; Analyze, Security, ClearPHP, CI-checks)

* 0.8.3

  * Variable Global (Structures/VariableGlobal)




PHP Error messages
------------------

Exakat helps reduce the amount of error and warning that code is producing by reporting pattern that are likely to emit errors.

106 PHP error message detailled : 

* :ref:` Cannot use parent when current class scope has no parent <class-without-parent>`
* :ref:` Default value for parameters with a int type can only be int or NULL  <mismatch-type-and-default>`
* :ref:` array_merge() expects at least 1 parameter, 0 given <array\_merge()-and-variadic>`
* :ref:`"continue" targeting switch is equivalent to "break". Did you mean to use "continue 2"? <continue-is-for-loop>`
* :ref:`A function with return type must return a value (did you mean "return null;" instead of "return;"?) <typehint-must-be-returned>`
* :ref:`Access level to Bar\:\:$publicProperty must be public (as in class Foo) <raised-access-level>`
* :ref:`Access level to c\:\:iPrivate() must be public (as in class i)  <concrete-visibility>`
* :ref:`Access level to x\:\:foo() must be public (as in class i) <implemented-methods-are-public>`
* :ref:`Access level to xx\:\:$x must be public (as in class x) <redefined-property>`
* :ref:`Access to undeclared static property <wrong-access-style-to-property>`
* :ref:`Accessing static property aa\:\:$a as non static <wrong-access-style-to-property>`
* :ref:`An alias (%s) was defined for method %s(), but this method does not exist <undefined-insteadof>`
* :ref:`Argument 1 passed to foo() must be of the type integer, string given <mismatch-type-and-default>`
* :ref:`Argument cannot be passed by reference <only-variable-for-reference>`
* :ref:`Argument cannot be passed by reference <typehinted-references>`
* :ref:`Array and string offset access syntax with curly braces is deprecated <no-more-curly-arrays>`
* :ref:`Call to a member function m() on null <use-nullsafe-operator>`
* :ref:`Call to undefined function <throw-functioncall>`
* :ref:`Call to undefined method theParent\:\:bar() <undefined-parent>`
* :ref:`Can't inherit abstract function A\:\:bar() <cant-inherit-abstract-method>`
* :ref:`Cannot access parent\:\: when current class scope has no parent <avoid-self-in-interface>`
* :ref:`Cannot access parent\:\: when current class scope has no parent <undefined-parent>`
* :ref:`Cannot access private const  <unreachable-class-constant>`
* :ref:`Cannot access static\:\: when no class scope is active <self,-parent,-static-outside-class>`
* :ref:`Cannot override final method Foo\:\:Bar() <final-class-usage>`
* :ref:`Cannot override final method Foo\:\:FooBar() <final-methods-usage>`
* :ref:`Cannot pass parameter 1 by reference <no-literal-for-reference>`
* :ref:`Cannot pass parameter 1 by reference <only-variable-for-reference>`
* :ref:`Cannot perform bitwise not on array <unsupported-types-with-operators>`
* :ref:`Cannot perform bitwise not on bool <unsupported-types-with-operators>`
* :ref:`Cannot perform bitwise not on object <unsupported-types-with-operators>`
* :ref:`Cannot perform bitwise not on resource <unsupported-types-with-operators>`
* :ref:`Cannot unpack array with string keys <no-spread-for-hash>`
* :ref:`Cannot use "parent" when no class scope is active <self,-parent,-static-outside-class>`
* :ref:`Cannot use "self" when no class scope is active <self,-parent,-static-outside-class>`
* :ref:`Cannot use "static" when no class scope is active <self,-parent,-static-outside-class>`
* :ref:`Cannot use a scalar value as an array <string-initialization>`
* :ref:`Cannot use isset() on the result of an expression (you can use "null !== expression" instead) <isset()-with-constant>`
* :ref:`Cannot use object of type Foo as array <$this-is-not-an-array>`
* :ref:`Case-insensitive constants are deprecated. The correct casing for this constant is "A" <constant-case-preference>`
* :ref:`Class 'PARENT' not found <use-lower-case-for-parent,-static-and-self>`
* :ref:`Class 'x' not found <undefined-\:\:class>`
* :ref:`Class BA contains 1 abstract method and must therefore be declared abstract or implement the remaining methods (A\:\:aFoo) <abstract-or-implements>`
* :ref:`Class b cannot implement previously implemented interface i <cant-implement-traversable>`
* :ref:`Class b cannot implement previously implemented interface i <repeated-interface>`
* :ref:`Class c contains 1 abstract method and must therefore be declared abstract or implement the remaining methods (a\:\:foo) <missing-abstract-method>`
* :ref:`Class fooThrowable cannot implement interface Throwable, extend Exception or Error instead <can't-throw-throwable>`
* :ref:`Class x contains 2 abstract methods and must therefore be declared abstract or implement the remaining methods (x\:\:m1, x\:\:m2) <interfaces-is-not-implemented>`
* :ref:`Class x must implement interface Traversable as part of either Iterator or IteratorAggregate <cant-implement-traversable>`
* :ref:`Could not check compatibility between xx\:\:bar(B $a) and foo\:\:bar(A $a), because class A is not available <incompatible-signature-methods-with-covariance>`
* :ref:`Creating default object from empty value <undefined-variable>`
* :ref:`Declaration of FooParent\:\:Bar() must be compatible with FooChildren\:\:Bar() <method-signature-must-be-compatible>`
* :ref:`Declaration of a\:\:foo($a) should be compatible with ab1\:\:foo($a) <maxoverwrite>`
* :ref:`Declaration of ab\:\:foo($a) must be compatible with a\:\:foo($a = 1)  <incompatible-signature-methods-with-covariance>`
* :ref:`Declaration of ab\:\:foo($a) must be compatible with a\:\:foo($a = 1)  <incompatible-signature-methods>`
* :ref:`Declaration of ab\:\:foo($a) should be compatible with a\:\:foo($a = 1)  <incompatible-signature-methods-with-covariance>`
* :ref:`Declaration of ab\:\:foo($a) should be compatible with a\:\:foo($a = 1)  <incompatible-signature-methods>`
* :ref:`Defining a custom assert() function is deprecated, as the function has special semantics <assert-function-is-reserved>`
* :ref:`Delimiter must not be alphanumeric or backslash  <no-empty-regex>`
* :ref:`Generators cannot return values using "return"  <generator-cannot-return>`
* :ref:`Generators cannot return values using "return" <no-return-for-generator>`
* :ref:`Indirect modification of overloaded property c\:\:$b has no effect <no-magic-method-with-array>`
* :ref:`Invalid numeric literal <malformed-octal>`
* :ref:`Method name must be a string <useless-typehint>`
* :ref:`Methods with the same name as their class will not be constructors in a future version of PHP; %s has a deprecated constructor <old-style-constructor>`
* :ref:`Non-static method A\:\:B() should not be called statically <non-static-methods-called-in-a-static>`
* :ref:`Old style constructors are DEPRECATED in PHP 7.0, and will be removed in a future version. You should always use __construct() in new code. <old-style-constructor>`
* :ref:`Only variable references should be returned by reference <no-literal-for-reference>`
* :ref:`Only variable references should be returned by reference <no-reference-for-ternary>`
* :ref:`Only variables can be passed by reference <only-variable-for-reference>`
* :ref:`Only variables should be passed by reference <typehinted-references>`
* :ref:`Return value of foo() must be an instance of Bar, none returned  <typehint-must-be-returned>`
* :ref:`Return value of foo() must be of the type int, string returned <missing-some-returntype>`
* :ref:`The (real) cast is deprecated, use (float) instead <avoid-real>`
* :ref:`The behavior of unparenthesized expressions containing both '.' and '+'/'-' will change in PHP 8: '+'/'-' will take a higher precedence <concat-and-addition>`
* :ref:`The behavior of unparenthesized expressions containing both '.' and '>>'/'<<' will change in PHP 8: '<<'/'>>' will take a higher precedence <concat-and-addition>`
* :ref:`The each() function is deprecated. This message will be suppressed on further calls <php-7.2-removed-functions>`
* :ref:`The parent constructor was not called: the object is in an invalid state <must-call-parent-constructor>`
* :ref:`Too few arguments to function foo(), 1 passed and exactly 2 expected <wrong-number-of-arguments>`
* :ref:`Trait 'T' not found <undefined-trait>`
* :ref:`Trait 'a' not found  <trait-not-found>`
* :ref:`Trait method M has not been applied, because there are collisions with other trait methods on C <method-collision-traits>`
* :ref:`Trait method f has not been applied, because there are collisions with other trait methods on x <useless-alias>`
* :ref:`Trying to access array offset on value of type boolean <null-or-boolean-arrays>`
* :ref:`Trying to access array offset on value of type float <null-or-boolean-arrays>`
* :ref:`Trying to access array offset on value of type int <null-or-boolean-arrays>`
* :ref:`Trying to access array offset on value of type null <null-or-boolean-arrays>`
* :ref:`Trying to access array offset on value of type null <scalar-are-not-arrays>`
* :ref:`Uncaught ArgumentCountError: Too few arguments to function, 0 passed <wrong-number-of-arguments>`
* :ref:`Undefined class constant <avoid-self-in-interface>`
* :ref:`Undefined constant 'y' <undefined-constant-name>`
* :ref:`Undefined function <undefined-functions>`
* :ref:`Undefined variable:  <undefined-variable>`
* :ref:`Unknown named parameter $d in <unknown-parameter-name>`
* :ref:`Unparenthesized a ? b : c ? d : e is deprecated. Use either (a ? b : c) ? d : e or a ? b : (c ? d : e) <nested-ternary-without-parenthesis>`
* :ref:`Unsupported operand types <unsupported-operand-types>`
* :ref:`Unsupported operand types <unsupported-types-with-operators>`
* :ref:`Use of undefined constant y - assumed 'y' (this will throw an Error in a future version of PHP) <undefined-constant-name>`
* :ref:`Using $this when not in object context <$this-belongs-to-classes-or-traits>`
* :ref:`__autoload() is deprecated, use spl_autoload_register() instead <old-style-\_\_autoload()>`
* :ref:`__clone method called on non-object <clone-with-non-object>`
* :ref:`define(): Declaration of case-insensitive constants is deprecated <case-insensitive-constants>`
* :ref:`iconv(): Wrong charset, conversion from UTF-8' to ASCII//TRANSLIT' is not allowed <iconv-with-translit>`
* :ref:`pack(): Type t: unknown format code <invalid-pack-format>`
* :ref:`syntax error, unexpected '-', expecting '=' <invalid-constant-name>`
* :ref:`unpack(): Type t: unknown format code <invalid-pack-format>`




External services
-----------------

List of external services whose configuration files has been commited in the code.

* `Apache <http://www.apache.org/>`_ - .htaccess, htaccess.txt
* `Apple <http://www.apple.com/>`_ - .DS_Store
* `appveyor <http://www.appveyor.com/>`_ - appveyor.yml, .appveyor.yml
* `ant <https://ant.apache.org/>`_ - build.xml
* `apigen <http://apigen.github.io/ApiGen/>`_ - apigen.yml, apigen.neon
* `arcunit <https://www.archunit.org/>`_ - .arcunit
* `artisan <http://laravel.com/docs/5.1/artisan>`_ - artisan
* `atoum <http://atoum.org/>`_ - .bootstrap.atoum.php, .atoum.php, .atoum.bootstrap.php
* `arcanist <https://secure.phabricator.com/book/phabricator/article/arcanist_lint/>`_ - .arclint, .arcconfig
* `bazaar <http://bazaar.canonical.com/en/>`_ - .bzr
* `babeljs <https://babeljs.io/>`_ - .babel.rc, .babel.js, .babelrc
* `behat <http://docs.behat.org/en/v2.5/>`_ - behat.yml.dist, behat.yml
* `box2 <https://github.com/box-project/box2>`_ - box.json, box.json.dist
* `bower <http://bower.io/>`_ - bower.json, .bowerrc
* `circleCI <https://circleci.com/>`_ - circle.yml, .circleci
* `codacy <http://www.codacy.com/>`_ - .codacy.json
* `codeception <https://codeception.com/>`_ - codeception.yml, codeception.dist.yml
* `codecov <https://codecov.io/>`_ - .codecov.yml, codecov.yml
* `codeclimate <http://www.codeclimate.com/>`_ - .codeclimate.yml
* `composer <https://getcomposer.org/>`_ - composer.json, composer.lock, vendor
* `couscous <http://couscous.io/>`_ - couscous.yml
* `Code Sniffer <https://github.com/squizlabs/PHP_CodeSniffer>`_ - .php_cs, .php_cs.dist, .phpcs.xml, php_cs.dist, phpcs.xml, phpcs.xml.dist
* `coveralls <https://coveralls.zendesk.com/>`_ - .coveralls.yml
* `crowdin <https://crowdin.com/>`_ - crowdin.yml
* `cvs <http://savannah.nongnu.org/projects/cvs>`_ - CVS
* `docker <http://www.docker.com/>`_ - .dockerignore, .docker, docker-compose.yml, Dockerfile
* `dotenv <https://symfony.com/doc/current/components/dotenv.htmls>`_ - .env.dist, .env, .env.example
* `drone <http://docs.drone.io/>`_ - .dockerignore, .docker
* `drupalci <https://www.drupal.org/project/drupalci>`_ - drupalci.yml
* `drush <https://www.drupal.org/project/drupalci>`_ - drush.services.yml
* `editorconfig <https://editorconfig.org/>`_ - .editorconfig
* `eslint <http://eslint.org/>`_ - .eslintrc, .eslintignore, eslintrc.js, .eslintrc.js, .eslintrc.json
* `Exakat <https://www.exakat.io/>`_ - .exakat.yaml, .exakat.yml, .exakat.ini
* `flintci <https://flintci.io/>`_ - .flintci.yml
* `git <https://git-scm.com/>`_ - .git, .gitignore, .gitattributes, .gitmodules, .mailmap, .githooks
* `github <https://www.github.com/>`_ - .github
* `gitlab <https://www.gitlab.com/>`_ - .gitlab-ci.yml
* `gulpfile <http://gulpjs.com/>`_ - gulpfile.js
* `grumphp <https://github.com/phpro/grumphp>`_ - grumphp.yml.dist, grumphp.yml
* `gush <https://github.com/gushphp/gush>`_ - .gush.yml
* `gruntjs <https://gruntjs.com/>`_ - Gruntfile.js
* `humbug <https://github.com/humbug/box.git>`_ - humbug.json.dist, humbug.json
* `infection <https://infection.github.io/>`_ - infection.yml, .infection.yml, infection.json.dist
* `insight <https://insight.sensiolabs.com/>`_ - .sensiolabs.yml
* `jetbrains <https://www.jetbrains.com/phpstorm/>`_ - .idea
* `jshint <http://jshint.com/>`_ - .jshintrc, .jshintignore
* `mercurial <https://www.mercurial-scm.org/>`_ - .hg, .hgtags, .hgignore, .hgeol
* `mkdocs <http://www.mkdocs.org>`_ - mkdocs.yml
* `npm <https://www.npmjs.com/>`_ - package.json, .npmignore, .npmrc, package-lock.json
* `openshift <https://www.openshift.com/>`_ - .openshift
* `phan <https://github.com/etsy/phan>`_ - .phan
* `pharcc <https://github.com/cbednarski/pharcc>`_ - .pharcc.yml
* `phalcon <https://phalconphp.com/>`_ - .phalcon
* `phpbench <https://github.com/phpbench/phpbench>`_ - phpbench.json
* `phpci <https://www.phptesting.org/>`_ - phpci.yml
* `Phpdocumentor <https://www.phpdoc.org/>`_ - .phpdoc.xml, phpdoc.dist.xml
* `phpdox <https://github.com/theseer/phpdox>`_ - phpdox.xml.dist, phpdox.xml
* `phinx <https://phinx.org/>`_ - phinx.yml
* `phpformatter <https://github.com/mmoreram/php-formatter>`_ - .formatter.yml
* `phpmetrics <http://www.phpmetrics.org/>`_ - .phpmetrics.yml.dist
* `phpsa <https://github.com/ovr/phpsa>`_ - .phpsa.yml
* `phpspec <http://www.phpspec.net/en/latest/>`_ - phpspec.yml, .phpspec, phpspec.yml.dist
* `phpstan <https://github.com/phpstan>`_ - phpstan.neon, .phpstan.neon, phpstan.neon.dist
* `phpswitch <https://github.com/jubianchi/phpswitch>`_ - .phpswitch.yml
* `PHPUnit <https://www.phpunit.de/>`_ - phpunit.xml.dist, phpunit.xml
* `prettier <https://prettier.io/>`_ - .prettierrc, .prettierignore
* `psalm <https://getpsalm.org/>`_ - psalm.xml
* `puppet <https://puppet.com/>`_ - .puppet
* `rmt <https://github.com/liip/RMT>`_ - .rmt.yml
* `robo <https://robo.li/>`_ - RoboFile.php
* `scrutinizer <https://scrutinizer-ci.com/>`_ - .scrutinizer.yml
* `semantic versioning <http://semver.org/>`_ - .semver
* `SPIP <https://www.spip.net/>`_ - paquet.xml
* `stickler <https://stickler-ci.com/docs>`_ - .stickler.yml
* `storyplayer <https://datasift.github.io/storyplayer/>`_ - storyplayer.json.dist
* `styleci <https://styleci.io/>`_ - .styleci.yml
* `stylelint <https://stylelint.io/>`_ - .stylelintrc
* `sublimelinter <http://www.sublimelinter.com/en/latest/>`_ - .csslintrc
* `svn <https://subversion.apache.org/>`_ - svn.revision, .svn, .svnignore
* `transifex <https://www.transifex.com/>`_ - .tx
* `Robots.txt <http://www.robotstxt.org/>`_ - robots.txt
* `travis <https://travis-ci.org/>`_ - .travis.yml, .env.travis, .travis, .travis.php.ini, .travis.coverage.sh, .travis.ini
* `varci <https://var.ci/>`_ - .varci, .varci.yml
* `Vagrant <https://www.vagrantup.com/>`_ - Vagrantfile
* `visualstudio <https://code.visualstudio.com/>`_ - .vscode
* `webpack <https://webpack.js.org/>`_ - webpack.mix.js, webpack.config.js
* `yarn <https://yarnpkg.com/lang/en/>`_ - yarn.lock
* `Zend_Tool <https://framework.zend.com/>`_ - zfproject.xml

External links
--------------

List of external links mentionned in this documentation.

* `#QuandLeDevALaFleme <https://twitter.com/bsmt_nevers/status/949238391769653249>`_
* `$_ENV <https://www.php.net/reserved.variables.environment.php>`_
* `$GLOBALS <https://www.php.net/manual/en/reserved.variables.globals.php>`_
* `$HTTP_RAW_POST_DATA variable <https://www.php.net/manual/en/reserved.variables.httprawpostdata.php>`_
* `.exakat.ini` or `.exakat.yaml` file. See `Add Exakat To Your CI Pipeline <https://www.exakat.io/add-exakat-to-your-ci-pipeline/>`_
* `.phar` from the exakat.io website : `www.exakat.io <http://www.exakat.io/versions/>`_
* `1003.1-2008 - IEEE Standard for Information Technology - Portable Operating System Interface (POSIX(R)) <https://standards.ieee.org/findstds/standard/1003.1-2008.html>`_
* `7z <https://www.7-zip.org/7z.html>`_
* `::class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class.class>`_
* `@deprecated <https://docs.phpdoc.org/latest/references/phpdoc/tags/deprecated.html>`_
* `[blog] array_column() <https://benramsey.com/projects/array-column/>`_
* `[CVE-2017-6090] <https://cxsecurity.com/issue/WLB-2017100031>`_
* `[HttpFoundation] Make sessions secure and lazy #24523 <https://github.com/symfony/symfony/pull/24523>`_
* `__autoload <https://www.php.net/autoload>`_
* `__set <https://www.php.net/manual/en/language.oop5.overloading.php#object.set>`_
* `A PHP extension for Redis <https://github.com/phpredis/phpredis/>`_
* `About circular references in PHP <https://johann.pardanaud.com/blog/about-circular-references-in-php>`_
* `Add array_key_exists to the list of specialy compiled functions <https://bugs.php.net/bug.php?id=76148>`_
* `Allow a trailing comma in function calls <https://wiki.php.net/rfc/trailing-comma-function-calls>`_
* `Alpine Linux <https://alpinelinux.org/>`_
* `Alternative PHP Cache <https://www.php.net/apc>`_
* `Alternative syntax <https://www.php.net/manual/en/control-structures.alternative-syntax.php>`_
* `Anonymous functions <https://www.php.net/manual/en/functions.anonymous.php>`_
* `APCU <http://www.php.net/manual/en/book.apcu.php>`_
* `Argon2 Password Hash <https://wiki.php.net/rfc/argon2_password_hash>`_
* `Arithmetic Operators <https://www.php.net/manual/en/language.operators.arithmetic.php>`_
* `Aronduby Dump <https://github.com/aronduby/dump>`_
* `Array <https://www.php.net/manual/en/language.types.array.php>`_
* `array <https://www.php.net/manual/en/language.types.array.php>`_
* `Array Functions <https://www.php.net/manual/en/ref.array.php>`_
* `array_fill_keys <https://www.php.net/array_fill_keys>`_
* `array_filter <https://php.net/array_filter>`_
* `array_key_exists() with objects <https://wiki.php.net/rfc/deprecations_php_7_4#array_key_exists_with_objects>`_
* `array_map <https://www.php.net/array_map>`_
* `array_merge <https://www.php.net/array_merge>`_
* `array_search <https://www.php.net/array_search>`_
* `array_slice <http://www.php.net/array_slice>`_
* `array_unique <https://www.php.net/array_unique>`_
* `ArrayAccess <https://www.php.net/manual/en/class.arrayaccess.php>`_
* `Arrays <https://www.php.net/manual/en/book.array.php>`_
* `Arrays syntax <https://www.php.net/manual/en/language.types.array.php>`_
* `Arrow functions <https://www.php.net/manual/en/functions.arrow.php>`_
* `assert <https://www.php.net/assert>`_
* `Assignation Operators <https://www.php.net/manual/en/language.operators.assignment.php>`_
* `Autoloading Classe <https://www.php.net/manual/en/language.oop5.autoload.php>`_
* `Autoloading Classes <https://www.php.net/manual/en/language.oop5.autoload.php>`_
* `Avoid Else, Return Early <http://blog.timoxley.com/post/47041269194/avoid-else-return-early>`_
* `Avoid nesting too deeply and return early (part 1) <https://github.com/jupeter/clean-code-php#avoid-nesting-too-deeply-and-return-early-part-1>`_
* `Avoid option arrays in constructors <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#avoid-option-arrays-in-constructors>`_
* `Avoid optional services as much as possible <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#avoid-optional-services-as-much-as-possible>`_
* `Backward incompatible changes <https://www.php.net/manual/en/migration71.incompatible.php>`_
* `Backward incompatible changes PHP 7.0 <https://www.php.net/manual/en/migration70.incompatible.php>`_
* `basename <http://www.php.net/basename>`_
* `Bazaar <https://bazaar.canonical.com/en/>`_
* `BC Math Functions <http://www.php.net/bcmath>`_
* `Benoit Burnichon <https://twitter.com/BenoitBurnichon>`_
* `Bitmask Constant Arguments in PHP <https://medium.com/@liamhammett/bitmask-constant-arguments-in-php-cf32bf35c73>`_
* `Bitwise Operators <https://www.php.net/manual/en/language.operators.bitwise.php>`_
* `Brandon Savage <https://twitter.com/BrandonSavage>`_
* `browscap <http://browscap.org/>`_
* `Bug #50887 preg_match , last optional sub-patterns ignored when empty <https://bugs.php.net/bug.php?id=50887>`_
* `Bzip2 Functions <https://www.php.net/bzip2>`_
* `Cairo Graphics Library <https://cairographics.org/>`_
* `Calendar Functions <http://www.php.net/manual/en/ref.calendar.php>`_
* `Callback / callable <https://www.php.net/manual/en/language.types.callable.php>`_
* `Can you spot the vulnerability? (openssl_verify) <https://twitter.com/ripstech/status/1124325237967994880>`_
* `Cant Use Return Value In Write Context <https://stackoverflow.com/questions/1075534/cant-use-method-return-value-in-write-context>`_
* `Carnage <https://twitter.com/giveupalready>`_
* `cat: write error: Broken pipe <https://askubuntu.com/questions/421663/cat-write-error-broken-pipe>`_
* `Change the precedence of the concatenation operator <https://wiki.php.net/rfc/concatenation_precedence>`_
* `Changes to variable handling <https://www.php.net/manual/en/migration70.incompatible.php>`_
* `Class Abstraction <https://www.php.net/abstract>`_
* `Class Constant <https://www.php.net/manual/en/language.oop5.constants.php>`_
* `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_
* `class_alias <https://www.php.net/class_alias>`_
* `Classes abstraction <https://www.php.net/abstract>`_
* `Classes Abstraction <https://www.php.net/manual/en/language.oop5.abstract.php>`_
* `Closure class <https://www.php.net/closure>`_
* `Closure::bind <https://www.php.net/manual/en/closure.bind.php>`_
* `Cmark <https://github.com/commonmark/cmark>`_
* `Codeigniter <https://codeigniter.com/>`_
* `COM and .Net (Windows) <https://www.php.net/manual/en/book.com.php>`_
* `compact <http://www.php.net/compact>`_
* `Comparison Operators <https://www.php.net/manual/en/language.operators.comparison.php>`_
* `composer <https://getcomposer.org/>`_
* `Concrete 5 <https://www.concrete5.org/>`_
* `Conflict resolution <https://www.php.net/manual/en/language.oop5.traits.php#language.oop5.traits.conflict>`_
* `Constant definition <https://www.php.net/const>`_
* `Constant Scalar Expressions <https://wiki.php.net/rfc/const_scalar_exprs>`_
* `constant() <https://www.php.net/constant>`_
* `Constants <https://www.php.net/manual/en/language.constants.php>`_
* `Constructors and Destructors <https://www.php.net/manual/en/language.oop5.decon.php>`_
* `Cookies <https://www.php.net/manual/en/features.cookies.php>`_
* `count <https://www.php.net/count>`_
* `Courier Anti-pattern <https://r.je/oop-courier-anti-pattern.html>`_
* `Covariant Returns and Contravariant Parameters <https://wiki.php.net/rfc/covariant-returns-and-contravariant-parameters>`_
* `crc32() <https://www.php.net/crc32>`_
* `Cross-Site Scripting (XSS) <https://phpsecurity.readthedocs.io/en/latest/Cross-Site-Scripting-(XSS).html>`_
* `crypt <http://www.php.net/crypt>`_
* `Cryptography Extensions <https://www.php.net/manual/en/refs.crypto.php>`_
* `CSPRNG <https://www.php.net/manual/en/book.csprng.php>`_
* `Ctype funtions <https://www.php.net/manual/en/ref.ctype.php>`_
* `curl <http://www.php.net/curl>`_
* `Curl for PHP <https://www.php.net/manual/en/book.curl.php>`_
* `curl_version <https://www.php.net/manual/en/function.curl-version.php>`_
* `CVS <https://www.nongnu.org/cvs/>`_
* `CWE-484: Omitted Break Statement in Switch <https://cwe.mitre.org/data/definitions/484.html>`_
* `CWE-625: Permissive Regular Expression <https://cwe.mitre.org/data/definitions/625.html>`_
* `Cyrus <https://www.php.net/manual/en/book.cyrus.php>`_
* `d3.js <https://github.com/mbostock/d3>`_
* `Data filtering <https://www.php.net/manual/en/book.filter.php>`_
* `Data structures <http://docs.php.net/manual/en/book.ds.php>`_
* `Database (dbm-style) Abstraction Layer <https://www.php.net/manual/en/book.dba.php>`_
* `Date and Time <https://www.php.net/manual/en/book.datetime.php>`_
* `DCDFLIB <https://people.sc.fsu.edu/~jburkardt/c_src/cdflib/cdflib.html>`_
* `Dead Code: Unused Method <https://vulncat.fortify.com/en/detail?id=desc.structural.java.dead_code_unused_method>`_
* `declare <https://www.php.net/manual/en/control-structures.declare.php>`_
* `Declare <https://www.php.net/manual/en/control-structures.declare.php>`_
* `define <https://www.php.net/manual/en/function.define.php>`_
* `Dependency Injection Smells <http://seregazhuk.github.io/2017/05/04/di-smells/>`_
* `Deprecate and remove continue targeting switch <https://wiki.php.net/rfc/continue_on_switch_deprecation>`_
* `Deprecate and remove INTL_IDNA_VARIANT_2003 <https://wiki.php.net/rfc/deprecate-and-remove-intl_idna_variant_2003>`_
* `Deprecate curly brace syntax <https://derickrethans.nl/phpinternalsnews-19.html>`_
* `Deprecated features in PHP 5.4.x <https://www.php.net/manual/en/migration54.deprecated.php>`_
* `Deprecated features in PHP 5.5.x <https://www.php.net/manual/en/migration55.deprecated.php>`_
* `Deprecated features in PHP 7.2.x <https://www.php.net/manual/en/migration72.deprecated.php>`_
* `Deprecation allow_url_include <https://wiki.php.net/rfc/deprecations_php_7_4#allow_url_include>`_
* `Deprecations for PHP 7.2 <https://wiki.php.net/rfc/deprecations_php_7_2>`_
* `Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_
* `Destructor <https://www.php.net/manual/en/language.oop5.decon.php#language.oop5.decon.destructor>`_
* `DIO <https://www.php.net/manual/en/refs.fileprocess.file.php>`_
* `Dir predefined constants <https://www.php.net/manual/en/dir.constants.php>`_
* `directive error_reporting <https://www.php.net/manual/en/errorfunc.configuration.php#ini.error-reporting>`_
* `Directly calling __clone is allowed <https://wiki.php.net/rfc/abstract_syntax_tree#directly_calling_clone_is_allowed>`_
* `dirname <https://www.php.net/dirname>`_
* `dist.exakat.io <http://dist.exakat.io/>`_
* `dl <http://www.php.net/dl>`_
* `Do your objects talk to strangers? <https://www.brandonsavage.net/do-your-objects-talk-to-strangers/>`_
* `Docker <http://www.docker.com/>`_
* `Docker image <https://hub.docker.com/r/exakat/exakat/>`_
* `Document Object Model <https://www.php.net/manual/en/book.dom.php>`_
* `Don't pass this out of a constructor <http://www.javapractices.com/topic/TopicAction.do?Id=252>`_
* `Don’t turn off CURLOPT_SSL_VERIFYPEER, fix your PHP configuration <https://www.saotn.org/dont-turn-off-curlopt_ssl_verifypeer-fix-php-configuration/>`_
* `dotdeb instruction <https://www.dotdeb.org/instructions/>`_
* `Double quoted <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.double>`_
* `download <https://www.exakat.io/download-exakat/>`_
* `Drupal <http://www.drupal.org/>`_
* `Dynamically Access PHP Object Properties with $this <https://drupalize.me/blog/201508/dynamically-access-php-object-properties>`_
* `E_WARNING for invalid container read array-access <https://wiki.php.net/rfc/notice-for-non-valid-array-container>`_
* `Eaccelerator <http://eaccelerator.net/>`_
* `elseif/else if <https://www.php.net/manual/en/control-structures.elseif.php>`_
* `empty <http://www.php.net/empty>`_
* `Empty Catch Clause <http://wiki.c2.com/?EmptyCatchClause>`_
* `Empty interfaces are bad practice <https://r.je/empty-interfaces-bad-practice.html>`_
* `empty() <https://www.php.net/empty>`_
* `Enchant spelling library <https://www.php.net/manual/en/book.enchant.php>`_
* `Ereg <https://www.php.net/manual/en/function.ereg.php>`_
* `Error reporting <https://php.earth/docs/security/intro#error-reporting>`_
* `Escape sequences <https://www.php.net/manual/en/regexp.reference.escape.php>`_
* `Ev <https://www.php.net/manual/en/book.ev.php>`_
* `eval <http://www.php.net/eval>`_
* `Event <https://www.php.net/event>`_
* `Exakat <http://www.exakat.io/>`_
* `Exakat cloud <https://www.exakat.io/exakat-cloud/>`_
* `Exakat SAS <https://www.exakat.io/get-php-expertise/>`_
* `exakat/exakat <https://hub.docker.com/r/exakat/exakat/>`_
* `Exception::__construct <https://www.php.net/manual/en/exception.construct.php>`_
* `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_
* `Exchangeable image information <https://www.php.net/manual/en/book.exif.php>`_
* `Execution Operators <https://www.php.net/manual/en/language.operators.execution.php>`_
* `EXP30-C. Do not depend on the order of evaluation for side effects <https://wiki.sei.cmu.edu/confluence/display/c/EXP30-C.+Do+not+depend+on+the+order+of+evaluation+for+side+effects>`_
* `expect <https://www.php.net/manual/en/book.expect.php>`_
* `explode <https://www.php.net/manual/en/function.explode.php>`_
* `ext-async <https://github.com/concurrent-php/ext-async>`_
* `ext-http <https://github.com/m6w6/ext-http>`_
* `ext/ast <https://pecl.php.net/package/ast>`_
* `ext/gender manual <https://www.php.net/manual/en/book.gender.php>`_
* `ext/hash extension <http://www.php.net/manual/en/book.hash.php>`_
* `ext/hrtime manual <https://www.php.net/manual/en/intro.hrtime.php>`_
* `ext/inotify manual <https://www.php.net/manual/en/book.inotify.php>`_
* `ext/leveldb on Github <https://github.com/reeze/php-leveldb>`_
* `ext/lua manual <https://www.php.net/manual/en/book.lua.php>`_
* `ext/mbstring <http://www.php.net/manual/en/book.mbstring.php>`_
* `ext/memcached manual <https://www.php.net/manual/en/book.memcached.php>`_
* `ext/OpenSSL <https://www.php.net/manual/en/book.openssl.php>`_
* `ext/readline <https://www.php.net/manual/en/book.readline.php>`_
* `ext/recode <http://www.php.net/manual/en/book.recode.php>`_
* `ext/SeasLog on Github <https://github.com/SeasX/SeasLog>`_
* `ext/sqlite <https://www.php.net/manual/en/book.sqlite.php>`_
* `ext/sqlite3 <https://www.php.net/manual/en/book.sqlite3.php>`_
* `ext/uopz <https://pecl.php.net/package/uopz>`_
* `ext/varnish <https://www.php.net/manual/en/book.varnish.php>`_
* `ext/zookeeper <https://www.php.net/zookeeper>`_
* `Extension Apache <https://www.php.net/manual/en/book.apache.php>`_
* `extension FANN <https://www.php.net/manual/en/book.fann.php>`_
* `extension mcrypt <http://www.php.net/manual/en/book.mcrypt.php>`_
* `extract <https://www.php.net/extract>`_
* `Ez <https://ez.no/>`_
* `Factory (object-oriented programming) <https://en.wikipedia.org/wiki/Factory_(object-oriented_programming)>`_
* `FAM <http://oss.sgi.com/projects/fam/>`_
* `FastCGI Process Manager <https://www.php.net/fpm>`_
* `FDF <http://www.adobe.com/devnet/acrobat/fdftoolkit.html>`_
* `ffmpeg-php <http://ffmpeg-php.sourceforge.net/>`_
* `file_get_contents <https://www.php.net/file_get_contents>`_
* `filesystem <http://www.php.net/manual/en/book.filesystem.php>`_
* `Filinfo <https://www.php.net/manual/en/book.fileinfo.php>`_
* `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_
* `Firebase / Interbase <https://www.php.net/manual/en/book.ibase.php>`_
* `Flag Argument <https://martinfowler.com/bliki/FlagArgument.html>`_
* `FlagArgument <https://www.martinfowler.com/bliki/FlagArgument.html>`_
* `Floating point numbers <https://www.php.net/manual/en/language.types.float.php#language.types.float>`_
* `Floats <https://www.php.net/manual/en/language.types.float.php>`_
* `Fluent Interfaces in PHP <http://mikenaberezny.com/2005/12/20/fluent-interfaces-in-php/>`_
* `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_
* `Foreign Function Interface <https://www.php.net/manual/en/book.ffi.php>`_
* `Frederic Bouchery <https://twitter.com/FredBouchery/>`_
* `From assumptions to assertions <https://rskuipers.com/entry/from-assumptions-to-assertions>`_
* `FuelPHP <https://fuelphp.com>`_
* `Function arguments <https://www.php.net/manual/en/functions.arguments.php>`_
* `Functions <https://www.php.net/manual/en/language.functions.php>`_
* `Gearman on PHP <https://www.php.net/manual/en/book.gearman.php>`_
* `Generalize support of negative string offsets <https://wiki.php.net/rfc/negative-string-offsets>`_
* `Generator delegation via yield from <https://www.php.net/manual/en/language.generators.syntax.php#control-structures.yield.from>`_
* `Generator Syntax <https://www.php.net/manual/en/language.generators.syntax.php>`_
* `Generators overview <https://www.php.net/manual/en/language.generators.overview.php>`_
* `GeoIP <https://www.php.net/manual/en/book.geoip.php>`_
* `get_class <https://www.php.net/get_class>`_
* `Gettext <https://www.gnu.org/software/gettext/manual/gettext.html>`_
* `Git <https://git-scm.com/>`_
* `Github Action <https://docs.github.com/en/actions>`_
* `Github.com/exakat/exakat <https://github.com/exakat/exakat>`_
* `global namespace <https://www.php.net/manual/en/language.namespaces.global.php>`_
* `GMP <https://www.php.net/manual/en/book.gmp.php>`_
* `Gnupg Function for PHP <http://www.php.net/manual/en/book.gnupg.php>`_
* `Goto <https://www.php.net/manual/en/control-structures.goto.php>`_
* `Gremlin server <http://tinkerpop.apache.org/>`_
* `Group Use Declaration RFC <https://wiki.php.net/rfc/group_use_declarations>`_
* `GRPC <http://www.grpc.io/>`_
* `Handling file uploads <https://www.php.net/manual/en/features.file-upload.php>`_
* `Hardening Your HTTP Security Headers <https://www.keycdn.com/blog/http-security-headers>`_
* `hash <http://www.php.net/hash>`_
* `HASH Message Digest Framework <http://www.php.net/manual/en/book.hash.php>`_
* `hash_algos <https://www.php.net/hash_algos>`_
* `hash_file <https://www.php.net/manual/en/function.hash-file.php>`_
* `Heredoc <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.heredoc>`_
* `Holger Woltersdorf <https://twitter.com/hollodotme>`_
* `How to fix Headers already sent error in PHP <http://stackoverflow.com/questions/8028957/how-to-fix-headers-already-sent-error-in-php>`_
* `How to pick bad function and variable names <http://mojones.net/how-to-pick-bad-function-and-variable-names.html>`_
* `htmlentities <https://www.php.net/htmlentities>`_
* `htmlspecialchars <https://www.php.net/htmlspecialchars>`_
* `https://hub.docker.com/r/exakat/exakat-ga <https://hub.docker.com/r/exakat/exakat-ga>`_
* `https://www.exakat.io/ <https://www.exakat.io/>`_
* `https://www.exakat.io/versionss/index.php?file=latest <https://www.exakat.io/versions/index.php?file=latest>`_
* `IBM Db2 <https://www.php.net/manual/en/book.ibm-db2.php>`_
* `Iconv <https://www.php.net/iconv>`_
* `iconv() <https://www.php.net/manual/en/function.iconv.php>`_
* `ICU <http://site.icu-project.org/>`_
* `Ideal regex delimiters in PHP <http://codelegance.com/ideal-regex-delimiters-in-php/>`_
* `idn_to_ascii <https://www.php.net/manual/en/function.idn-to-ascii.php>`_
* `IERS <https://www.iers.org/IERS/EN/Home/home_node.html>`_
* `igbinary <https://github.com/igbinary/igbinary/>`_
* `IIS Administration <http://www.php.net/manual/en/book.iisfunc.php>`_
* `Image Processing and GD <https://www.php.net/manual/en/book.image.php>`_
* `Imagick for PHP <https://www.php.net/manual/en/book.imagick.php>`_
* `IMAP <http://www.php.net/imap>`_
* `Implement ZEND_ARRAY_KEY_EXISTS opcode to speed up array_key_exists() <https://github.com/php/php-src/pull/3360>`_
* `implode <https://www.php.net/implode>`_
* `In a PHP5 class, when does a private constructor get called? <https://stackoverflow.com/questions/26079/in-a-php5-class-when-does-a-private-constructor-get-called>`_
* `in_array() <https://www.php.net/in_array>`_
* `include <https://www.php.net/manual/en/function.include.php>`_
* `include_once <https://www.php.net/manual/en/function.include-once.php>`_
* `Incrementing/Decrementing Operators <https://www.php.net/manual/en/language.operators.increment.php>`_
* `Info Predefined Constants <https://www.php.net/manual/en/info.constants.php>`_
* `Insecure Transportation Security Protocol Supported (TLS 1.0) <https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/insecure-transportation-security-protocol-supported-tls-10/>`_
* `Instanceof <https://www.php.net/manual/en/language.operators.type.php>`_
* `Integer overflow <https://www.php.net/manual/en/language.types.integer.php#language.types.integer.overflow>`_
* `Integer Syntax <https://www.php.net/manual/en/language.types.integer.php#language.types.integer.syntax>`_
* `Integers <https://www.php.net/manual/en/language.types.integer.php>`_
* `Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_
* `Internal Constructor Behavior <https://wiki.php.net/rfc/internal_constructor_behaviour>`_
* `Is it a bad practice to have multiple classes in the same file? <https://stackoverflow.com/questions/360643/is-it-a-bad-practice-to-have-multiple-classes-in-the-same-file>`_
* `Isset <http://www.php.net/isset>`_
* `Isset Ternary <https://wiki.php.net/rfc/isset_ternary>`_
* `It is the 31st again <https://twitter.com/rasmus/status/925431734128197632>`_
* `iterable pseudo-type <https://www.php.net/manual/en/migration71.new-features.php#migration71.new-features.iterable-pseudo-type>`_
* `Iterables <https://www.php.net/manual/en/language.types.iterable.php>`_
* `Joomla <http://www.joomla.org/>`_
* `json_decode <https://www.php.net/json_decode>`_
* `Judy C library <http://judy.sourceforge.net/>`_
* `Kafka client for PHP <https://github.com/arnaud-lb/php-rdkafka>`_
* `Kerberos V <https://www.php.net/manual/en/book.kadm5.php>`_
* `Lapack <https://www.php.net/manual/en/book.lapack.php>`_
* `Laravel <http://www.lavarel.com/>`_
* `Late Static Bindings <https://www.php.net/manual/en/language.oop5.late-static-bindings.php>`_
* `libeio <http://software.schmorp.de/pkg/libeio.html>`_
* `libevent <http://www.libevent.org/>`_
* `libmongoc <https://github.com/mongodb/mongo-c-driver>`_
* `libuuid <https://linux.die.net/man/3/libuuid>`_
* `libxml <http://www.php.net/manual/en/book.libxml.php>`_
* `Lightweight Directory Access Protocol <https://www.php.net/manual/en/book.ldap.php>`_
* `list <https://www.php.net/manual/en/function.list.php>`_
* `List of function aliases <https://www.php.net/manual/en/aliases.php>`_
* `List of HTTP header fields <https://en.wikipedia.org/wiki/List_of_HTTP_header_fields>`_
* `List of HTTP status codes <https://en.wikipedia.org/wiki/List_of_HTTP_status_codes>`_
* `List of Keywords <https://www.php.net/manual/en/reserved.keywords.php>`_
* `List of other reserved words <https://www.php.net/manual/en/reserved.other-reserved-words.php>`_
* `List of TCP and UDP port numbers <https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers>`_
* `list() Reference Assignment <https://wiki.php.net/rfc/list_reference_assignment>`_
* `Logical Expressions in C/C++. Mistakes Made by Professionals <http://www.viva64.com/en/b/0390/>`_
* `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_
* `Loosening Reserved Word Restrictions <https://www.php.net/manual/en/migration70.other-changes.php#migration70.other-changes.loosening-reserved-words>`_
* `lzf <https://www.php.net/lzf>`_
* `Magic Constants <https://www.php.net/manual/en/language.constants.predefined.php>`_
* `Magic Hashes <https://blog.whitehatsec.com/magic-hashes/>`_
* `Magic Method <https://www.php.net/manual/en/language.oop5.magic.php>`_
* `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_
* `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_
* `mail <https://www.php.net/mail>`_
* `Mail related functions <http://www.php.net/manual/en/book.mail.php>`_
* `Marco Pivetta tweet <https://twitter.com/Ocramius/status/811504929357660160>`_
* `Math predefined constants <https://www.php.net/manual/en/math.constants.php>`_
* `Mathematical Functions <https://www.php.net/manual/en/book.math.php>`_
* `mb_encoding_detect <https://php.net/mb-encoding-detect>`_
* `mb_str_split <https://www.php.net/mb_str_split>`_
* `Mbstring <http://www.php.net/manual/en/book.mbstring.php>`_
* `mcrypt_create_iv() <https://www.php.net/manual/en/function.mcrypt-create-iv.php>`_
* `MD5 <https://www.php.net/md5>`_
* `Media Type <https://en.wikipedia.org/wiki/Media_type>`_
* `Memcache on PHP <http://www.php.net/manual/en/book.memcache.php>`_
* `mercurial <https://www.mercurial-scm.org/>`_
* `Method overloading <https://www.php.net/manual/en/language.oop5.overloading.php#object.call>`_
* `mhash <http://mhash.sourceforge.net/>`_
* `Microsoft SQL Server <http://www.php.net/manual/en/book.mssql.php>`_
* `Microsoft SQL Server Driver <https://www.php.net/sqlsrv>`_
* `Ming (flash) <http://www.libming.org/>`_
* `MongoDB driver <https://www.php.net/mongo>`_
* `move_uploaded_file <https://www.php.net/move_uploaded_file>`_
* `msgpack for PHP <https://github.com/msgpack/msgpack-php>`_
* `MySQL Improved Extension <https://www.php.net/manual/en/book.mysqli.php>`_
* `mysqli <https://www.php.net/manual/en/book.mysqli.php>`_
* `Named Arguments <https://wiki.php.net/rfc/named_params>`_
* `Ncurses Terminal Screen Control <https://www.php.net/manual/en/book.ncurses.php>`_
* `Negative architecture, and assumptions about code <https://matthiasnoback.nl/2018/08/negative-architecture-and-assumptions-about-code/>`_
* `Nested Ternaries are Great <https://medium.com/javascript-scene/nested-ternaries-are-great-361bddd0f340>`_
* `Net SNMP <http://www.net-snmp.org/>`_
* `net_get_interfaces <https://www.php.net/net_get_interfaces>`_
* `New Classes and Interfaces <https://www.php.net/manual/en/migration70.classes.php>`_
* `New custom object serialization mechanism <https://wiki.php.net/rfc/custom_object_serialization>`_
* `New features <https://www.php.net/manual/en/migration56.new-features.php>`_
* `New global constants in 7.2 <https://www.php.net/manual/en/migration72.constants.php>`_
* `New global constants in 7.4 <https://www.php.net/manual/en/migration74.constants.php>`_
* `New object type <https://www.php.net/manual/en/migration72.new-features.php#migration72.new-features.iterable-pseudo-type>`_
* `Newt <http://people.redhat.com/rjones/ocaml-newt/html/Newt.html>`_
* `No Dangling Reference <https://github.com/dseguy/clearPHP/blob/master/rules/no-dangling-reference.md>`_
* `Nowdoc <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.nowdoc>`_
* `Null and True <https://twitter.com/Chemaclass/status/1144588647464951808>`_
* `Null Coalescing Assignment Operator <https://wiki.php.net/rfc/null_coalesce_equal_operator>`_
* `Null Coalescing Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.coalesce>`_
* `Null Object Pattern <https://en.wikipedia.org/wiki/Null_Object_pattern#PHP>`_
* `Nullable types <https://wiki.php.net/rfc/nullable_types>`_
* `Object Calisthenics, rule # 2 <http://williamdurand.fr/2013/06/03/object-calisthenics/>`_
* `Object Calisthenics, rule # 5 <http://williamdurand.fr/2013/06/03/object-calisthenics/#one-dot-per-line>`_
* `Object cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_
* `Object Inheritance <http://www.php.net/manual/en/language.oop5.inheritance.php>`_
* `Object Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_
* `Object interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_
* `Objects and references <https://www.php.net/manual/en/language.oop5.references.php>`_
* `ODBC (Unified) <http://www.php.net/manual/en/book.uodbc.php>`_
* `online <https://www.exakat.io/top-10-php-classic-traps/>`_
* `OPcache functions <http://www.php.net/manual/en/book.opcache.php>`_
* `opencensus <https://github.com/census-instrumentation/opencensus-php>`_
* `OpennSSL [PHP manual] <https://www.php.net/manual/en/book.openssl.php>`_
* `openssl_random_pseudo_byte <https://www.php.net/openssl_random_pseudo_bytes>`_
* `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_
* `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_
* `Optimization: How I made my PHP code run 100 times faster <https://mike42.me/blog/2018-06-how-i-made-my-php-code-run-100-times-faster>`_
* `Optimize array_unique() <https://github.com/php/php-src/commit/6c2c7a023da4223e41fea0225c51a417fc8eb10d>`_
* `Option to make json_encode and json_decode throw exceptions on errors <https://ayesh.me/Upgrade-PHP-7.3#json-exceptions>`_
* `Oracle OCI8 <https://www.php.net/manual/en/book.oci8.php>`_
* `original idea <https://twitter.com/b_viguier/status/940173951908700161>`_
* `Original MySQL API <http://www.php.net/manual/en/book.mysql.php>`_
* `Output Buffering Control <https://www.php.net/manual/en/book.outcontrol.php>`_
* `Overload <https://www.php.net/manual/en/language.oop5.overloading.php#object.get>`_
* `pack <https://www.php.net/pack>`_
* `Packagist <https://packagist.org/>`_
* `parent <https://www.php.net/manual/en/keyword.parent.php>`_
* `Parsekit <http://www.php.net/manual/en/book.parsekit.php>`_
* `Parsing and Lexing <https://www.php.net/manual/en/book.parle.php>`_
* `Passing arguments by reference <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.by-reference>`_
* `Passing by reference <https://www.php.net/manual/en/language.references.pass.php>`_
* `Password hashing <https://www.php.net/manual/en/book.password.php>`_
* `Password Hashing <https://www.php.net/manual/en/book.password.php>`_
* `Pattern Modifiers <https://www.php.net/manual/en/reference.pcre.pattern.modifiers.php>`_
* `PCOV <https://github.com/krakjoe/pcov>`_
* `PCRE <https://www.php.net/pcre>`_
* `PEAR <http://pear.php.net/>`_
* `pecl crypto <https://pecl.php.net/package/crypto>`_
* `PECL ext/xxtea <https://pecl.php.net/package/xxtea>`_
* `pg_last_error <https://www.php.net/manual/en/function.pg-last-error.php>`_
* `Phalcon <https://phalconphp.com/>`_
* `phar <http://www.php.net/manual/en/book.phar.php>`_
* `PHP - Fatal error: Unsupported operand types [duplicate] <https://stackoverflow.com/questions/2108875/php-fatal-error-unsupported-operand-types>`_
* `PHP 7 performance improvements (3/5): Encapsed strings optimization <https://blog.blackfire.io/php-7-performance-improvements-encapsed-strings-optimization.html>`_
* `PHP 7.0 Backward incompatible changes <https://www.php.net/manual/en/migration70.incompatible.php>`_
* `PHP 7.0 Removed Functions <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.removed-functions>`_
* `PHP 7.1 no longer converts string to arrays the first time a value is assigned with square bracket notation <https://www.drupal.org/project/adaptivetheme/issues/2832900>`_
* `PHP 7.2's "switch" optimisations <https://derickrethans.nl/php7.2-switch.html>`_
* `PHP 7.2's switch optimisations <https://derickrethans.nl/php7.2-switch.html>`_
* `PHP 7.3 Removed Functions <https://www.php.net/manual/en/migration73.incompatible.php#migration70.incompatible.removed-functions>`_
* `PHP 7.3 UPGRADE NOTES <https://github.com/php/php-src/blob/3b6e1ee4ee05678b5d717cd926a35ffdc1335929/UPGRADING#L66-L81>`_
* `PHP 7.4 Removed Functions <https://www.php.net/manual/en/migration74.incompatible.php#migration70.incompatible.removed-functions>`_
* `PHP 8: Constructor property promotion <https://stitcher.io/blog/constructor-promotion-in-php-8>`_
* `PHP <https://www.php.net/>`_
* `PHP class name constant case sensitivity and PSR-11 <https://gist.github.com/bcremer/9e8d6903ae38a25784fb1985967c6056>`_
* `PHP Classes containing only constants <https://stackoverflow.com/questions/16838266/php-classes-containing-only-constants>`_
* `PHP Clone and Shallow vs Deep Copying <http://jacob-walker.com/blog/php-clone-and-shallow-vs-deep-copying.html>`_
* `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_
* `PHP Data Object <https://www.php.net/manual/en/book.pdo.php>`_
* `PHP Decimal <http://php-decimal.io>`_
* `PHP extension for libsodium <https://github.com/jedisct1/libsodium-php>`_
* `PHP gmagick <http://www.php.net/manual/en/book.gmagick.php>`_
* `PHP Options And Information <https://www.php.net/manual/en/book.info.php>`_
* `PHP Options/Info Functions <https://www.php.net/manual/en/ref.info.php>`_
* `PHP return(value); vs return value; <https://stackoverflow.com/questions/2921843/php-returnvalue-vs-return-value>`_
* `PHP RFC: Add Stringable interface <https://wiki.php.net/rfc/stringable>`_
* `PHP RFC: Allow a trailing comma in function calls <https://wiki.php.net/rfc/trailing-comma-function-calls>`_
* `PHP RFC: Allow abstract function override <https://wiki.php.net/rfc/allow-abstract-function-override>`_
* `PHP RFC: Allow trailing comma in parameter list <https://wiki.php.net/rfc/trailing_comma_in_parameter_list>`_
* `PHP RFC: Arrays starting with a negative index <https://wiki.php.net/rfc/negative_array_index>`_
* `PHP RFC: Arrow Functions <https://wiki.php.net/rfc/arrow_functions>`_
* `PHP RFC: Convert numeric keys in object/array casts <https://wiki.php.net/rfc/convert_numeric_keys_in_object_array_casts>`_
* `PHP RFC: Deprecate and Remove Bareword (Unquoted) Strings <https://wiki.php.net/rfc/deprecate-bareword-strings>`_
* `PHP RFC: Deprecate left-associative ternary operator <https://wiki.php.net/rfc/ternary_associativity>`_
* `PHP RFC: Deprecations for PHP 7.2 : Each() <https://wiki.php.net/rfc/deprecations_php_7_2#each>`_
* `PHP RFC: Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_
* `PHP RFC: get_debug_type <https://wiki.php.net/rfc/get_debug_type>`_
* `PHP RFC: is_countable <https://wiki.php.net/rfc/is-countable>`_
* `PHP RFC: Nullsafe operator <https://wiki.php.net/rfc/nullsafe_operator>`_
* `PHP RFC: Numeric Literal Separator <https://wiki.php.net/rfc/numeric_literal_separator>`_
* `PHP RFC: Scalar Type Hints <https://wiki.php.net/rfc/scalar_type_hints>`_
* `PHP RFC: Shorter Attribute Syntax <https://wiki.php.net/rfc/shorter_attribute_syntax>`_
* `PHP RFC: str_contains <https://wiki.php.net/rfc/str_contains>`_
* `PHP RFC: Syntax for variadic functions <https://wiki.php.net/rfc/variadics>`_
* `PHP RFC: Unicode Codepoint Escape Syntax <https://wiki.php.net/rfc/unicode_escape>`_
* `PHP RFC: Union Types 2.0 <https://wiki.php.net/rfc/union_types_v2>`_
* `PHP RFC: Variable Syntax Tweaks <https://wiki.php.net/rfc/variable_syntax_tweaks>`_
* `PHP Tags <https://www.php.net/manual/en/language.basic-syntax.phptags.php>`_
* `PHP why pi() and M_PI <https://stackoverflow.com/questions/42021176/php-why-pi-and-m-pi>`_
* `PHP-cs-fixer <https://github.com/FriendsOfPHP/PHP-CS-Fixer>`_
* `php-ext-wasm <https://github.com/Hywan/php-ext-wasm>`_
* `php-vips-ext <https://github.com/jcupitt/php-vips-ext>`_
* `php-zbarcode <https://github.com/mkoppanen/php-zbarcode>`_
* `PHP: When is /tmp not /tmp? <https://www.the-art-of-web.com/php/where-is-tmp/>`_
* `phpsdl <https://github.com/Ponup/phpsdl>`_
* `PHPUnit <https://www.phpunit.de/>`_
* `plantuml <http://plantuml.com/>`_
* `PMB <https://www.sigb.net/>`_
* `PostgreSQL <https://www.php.net/manual/en/book.pgsql.php>`_
* `Predefined Constants <https://www.php.net/manual/en/reserved.constants.php>`_
* `Predefined Exceptions <https://www.php.net/manual/en/reserved.exceptions.php>`_
* `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_
* `preg_filter <https://php.net/preg_filter>`_
* `Prepare for PHP 7 error messages (part 3) <https://www.exakat.io/prepare-for-php-7-error-messages-part-3/>`_
* `printf <https://www.php.net/printf>`_
* `Process Control <https://www.php.net/manual/en/book.pcntl.php>`_
* `proctitle <https://www.php.net/manual/en/book.proctitle.php>`_
* `Properties <https://www.php.net/manual/en/language.oop5.properties.php>`_
* `Property overloading <https://www.php.net/manual/en/language.oop5.overloading.php#language.oop5.overloading.members>`_
* `Pspell <https://www.php.net/manual/en/book.pspell.php>`_
* `PSR-11 : Dependency injection container <https://github.com/container-interop/fig-standards/blob/master/proposed/container.md>`_
* `PSR-13 : Link definition interface <http://www.php-fig.org/psr/psr-13/>`_
* `PSR-16 : Common Interface for Caching Libraries <http://www.php-fig.org/psr/psr-16/>`_
* `PSR-3 : Logger Interface <http://www.php-fig.org/psr/psr-3/>`_
* `PSR-3 <https://www.php-fig.org/psr/psr-3>`_
* `PSR-6 : Caching <http://www.php-fig.org/psr/psr-6/>`_
* `Putting glob to the test <https://www.phparch.com/2010/04/putting-glob-to-the-test/>`_
* `RabbitMQ AMQP client library <https://github.com/alanxz/rabbitmq-c>`_
* `rar <https://en.wikipedia.org/wiki/RAR_(file_format)>`_
* `Rar archiving <https://www.php.net/manual/en/book.rar.php>`_
* `RectorPHP <https://getrector.org/>`_
* `References <https://www.php.net/references>`_
* `Reflection <https://www.php.net/manual/en/book.reflection.php>`_
* `Reflection export() methods <https://wiki.php.net/rfc/deprecations_php_7_4#reflection_export_methods>`_
* `Regular Expressions (Perl-Compatible) <https://www.php.net/manual/en/book.pcre.php>`_
* `resources <https://www.php.net/manual/en/language.types.resource.php>`_
* `return <https://www.php.net/manual/en/function.return.php>`_
* `Return Inside Finally Block <https://www.owasp.org/index.php/Return_Inside_Finally_Block>`_
* `Return Type Declaration <https://www.php.net/manual/en/functions.returning-values.php#functions.returning-values.type-declaration>`_
* `Returning values <https://www.php.net/manual/en/functions.returning-values.php>`_
* `RFC 7159 <http://www.faqs.org/rfcs/rfc7159>`_
* `RFC 7230 <https://tools.ietf.org/html/rfc7230>`_
* `RFC 822 (MIME) <http://www.faqs.org/rfcs/rfc822.html>`_
* `RFC 959 <http://www.faqs.org/rfcs/rfc959>`_
* `RFC : Arrow functions <https://wiki.php.net/rfc/arrow_functions>`_
* `RFC Preload <https://wiki.php.net/rfc/preload>`_
* `RFC: Return Type Declarations <https://wiki.php.net/rfc/return_types>`_
* `runkit <https://www.php.net/manual/en/book.runkit.php>`_
* `Salted Password Hashing - Doing it Right <https://crackstation.net/hashing-security.htm>`_
* `SARB <https://github.com/DaveLiddament/sarb>`_
* `Scalar type declarations <https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.scalar-type-declarations>`_
* `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_
* `Secure Hash Algorithms <https://en.wikipedia.org/wiki/Secure_Hash_Algorithms>`_
* `Semaphore, Shared Memory and IPC <https://www.php.net/manual/en/book.sem.php>`_
* `Session <https://www.php.net/manual/en/book.session.php>`_
* `session_regenerateid() <https://www.php.net/session_regenerate_id>`_
* `Sessions <https://www.php.net/manual/en/book.session.php>`_
* `Set-Cookie <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie>`_
* `set_error_handler <http://www.php.net/set_error_handler>`_
* `setcookie <http://www.php.net/setcookie>`_
* `setlocale <https://www.php.net/setlocale>`_
* `shell_exec <http://www.php.net/shell_exec>`_
* `SimpleXML <https://www.php.net/manual/en/book.simplexml.php>`_
* `Single Function Exit Point <http://wiki.c2.com/?SingleFunctionExitPoint>`_
* `SOAP <https://www.php.net/manual/en/book.soap.php>`_
* `Sockets <https://www.php.net/manual/en/book.sockets.php>`_
* `Sphinx Client <https://www.php.net/manual/en/book.sphinx.php>`_
* `Spread Operator in Array Expression  <https://wiki.php.net/rfc/spread_operator_for_array>`_
* `Spread Operator in Array Expression <https://wiki.php.net/rfc/spread_operator_for_array>`_
* `sqlite3 <http://www.php.net/sqlite3>`_
* `SQLite3::escapeString <https://www.php.net/manual/en/sqlite3.escapestring.php>`_
* `SSH2 functions <https://www.php.net/manual/en/book.ssh2.php>`_
* `Standard PHP Library (SPL) <http://www.php.net/manual/en/book.spl.php>`_
* `Static Analysis Results Interchange Format (SARIF) <https://docs.oasis-open.org/sarif/sarif/v2.0/sarif-v2.0.html>`_
* `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_
* `str_contains <https://www.php.net/str_contains>`_
* `Strict typing <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration.strict>`_
* `Stricter type checks for arithmetic/bitwise operators <https://wiki.php.net/rfc/arithmetic_operator_type_checks>`_
* `String functions <https://www.php.net/manual/en/ref.strings.php>`_
* `Strings <https://www.php.net/manual/en/language.types.string.php>`_
* `strip_tags <https://www.php.net/manual/en/function.strip-tags.php>`_
* `strpos not working correctly <https://bugs.php.net/bug.php?id=52198>`_
* `strtr <http://www.php.net/strtr>`_
* `Structuring PHP Exceptions <https://www.alainschlesser.com/structuring-php-exceptions/>`_
* `Subpatterns <https://www.php.net/manual/en/regexp.reference.subpatterns.php>`_
* `substr <http://www.php.net/substr>`_
* `Suhosin.org <https://suhosin.org/>`_
* `Sun, iPlanet and Netscape servers on Sun Solaris <https://www.php.net/manual/en/install.unix.sun.php>`_
* `Superglobals <https://www.php.net/manual/en/language.variables.superglobals.php>`_
* `Supported PHP Extensions <http://exakat.readthedocs.io/en/latest/Annex.html#supported-php-extensions>`_
* `Supported Protocols and Wrappers <https://www.php.net/manual/en/wrappers.php>`_
* `SVM <http://www.php.net/svm>`_
* `Svn <https://subversion.apache.org/>`_
* `Swoole <https://www.swoole.com/>`_
* `Symfony <http://www.symfony.com/>`_
* `Syntax <https://www.php.net/manual/en/language.constants.syntax.php>`_
* `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_
* `tetraweb/php <https://hub.docker.com/r/tetraweb/php/>`_
* `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_
* `The basics of Fluent interfaces in PHP <https://tournasdimitrios1.wordpress.com/2011/04/11/the-basics-of-fluent-interfaces-in-php/>`_
* `The Closure Class <https://www.php.net/manual/en/class.closure.php>`_
* `The Definitive 2019 Guide to Cryptographic Key Sizes and Algorithm Recommendations <https://paragonie.com/blog/2019/03/definitive-2019-guide-cryptographic-key-sizes-and-algorithm-recommendations>`_
* `The Linux NIS(YP)/NYS/NIS+ HOWTO <http://www.tldp.org/HOWTO/NIS-HOWTO/index.html>`_
* `The list function & practical uses of array destructuring in PHP <https://sebastiandedeyne.com/the-list-function-and-practical-uses-of-array-destructuring-in-php>`_
* `The main PPA for PHP (7.4, 7.3, 7.2, 7.1, 7.0, 5.6)  <https://launchpad.net/~ondrej/+archive/ubuntu/php>`_
* `Throw Expression <https://wiki.php.net/rfc/throw_expression>`_
* `Throwable <https://www.php.net/manual/en/class.throwable.php>`_
* `Tidy <https://www.php.net/manual/en/book.tidy.php>`_
* `tokenizer <http://www.php.net/tokenizer>`_
* `tokyo_tyrant <https://www.php.net/manual/en/book.tokyo-tyrant.php>`_
* `trader <https://pecl.php.net/package/trader>`_
* `Trailing Comma In Closure Use List <https://wiki.php.net/rfc/trailing_comma_in_closure_use_list>`_
* `Trailing Commas In List Syntax <https://wiki.php.net/rfc/list-syntax-trailing-commas>`_
* `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_
* `Traversable <https://www.php.net/manual/en/class.traversable.php>`_
* `trigger_error <https://www.php.net/trigger_error>`_
* `trim <https://www.php.net/manual/en/function.trim.php>`_
* `Tutorial 1: Let’s learn by example <https://docs.phalconphp.com/en/latest/reference/tutorial.html>`_
* `Type array <https://www.php.net/manual/en/language.types.array.php>`_
* `Type Casting <https://php.net/manual/en/language.types.type-juggling.php#language.types.typecasting>`_
* `Type Declaration <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_
* `Type declarations  <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_
* `Type Declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_
* `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_
* `Type hinting for interfaces <http://phpenthusiast.com/object-oriented-php-tutorials/type-hinting-for-interfaces>`_
* `Type Juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_
* `Type juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_
* `Type Juggling Authentication Bypass Vulnerability in CMS Made Simple <https://www.netsparker.com/blog/web-security/type-juggling-authentication-bypass-cms-made-simple/>`_
* `Type Operators <https://www.php.net/manual/en/language.operators.type.php#language.operators.type>`_
* `Typed Properties 2.0 <https://wiki.php.net/rfc/typed_properties_v2>`_
* `Typo3 <https://typo3.org/>`_
* `Unbinding $this from non-static closures <https://wiki.php.net/rfc/deprecations_php_7_4#unbinding_this_from_non-static_closures>`_
* `Understanding Dependency Injection <http://php-di.org/doc/understanding-di.html>`_
* `Unicode block <https://en.wikipedia.org/wiki/Unicode_block>`_
* `Unicode spaces <https://www.cs.tut.fi/~jkorpela/chars/spaces.html>`_
* `unserialize() <https://www.php.net/unserialize>`_
* `unset <https://www.php.net/unset>`_
* `Unset casting <https://www.php.net/manual/en/language.types.null.php#language.types.null.casting>`_
* `UPGRADING 7.3 <https://github.com/php/php-src/blob/PHP-7.3/UPGRADING#L83-L95>`_
* `UPGRADING PHP 8.0 <https://github.com/php/php-src/blob/master/UPGRADING>`_
* `Use of Hardcoded IPv4 Addresses <https://docs.microsoft.com/en-us/windows/desktop/winsock/use-of-hardcoded-ipv4-addresses-2>`_
* `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_
* `Using namespaces: fallback to global function/constant <https://www.php.net/manual/en/language.namespaces.fallback.php>`_
* `Using non-breakable spaces in test method names <http://mnapoli.fr/using-non-breakable-spaces-in-test-method-names/>`_
* `Using single characters for variable names in loops/exceptions <https://softwareengineering.stackexchange.com/questions/71710/using-single-characters-for-variable-names-in-loops-exceptions?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa/>`_
* `Using static variables <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.static>`_
* `V8 Javascript Engine <https://bugs.chromium.org/p/v8/issues/list>`_
* `Vagrant file <https://github.com/exakat/exakat-vagrant>`_
* `Variable basics <https://www.php.net/manual/en/language.variables.basics.php>`_
* `Variable functions <https://www.php.net/manual/en/functions.variable-functions.php>`_
* `Variable scope <https://www.php.net/manual/en/language.variables.scope.php>`_
* `Variable Scope <https://www.php.net/manual/en/language.variables.scope.php>`_
* `Variable variables <https://www.php.net/manual/en/language.variables.variable.php>`_
* `Variable-length argument lists <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_
* `Variables <https://www.php.net/manual/en/language.variables.basics.php>`_
* `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_
* `Vladimir Reznichenko <https://twitter.com/kalessil>`_
* `Void functions <https://www.php.net/manual/en/migration71.new-features.php#migration71.new-features.void-functions>`_
* `Warn when counting non-countable types <https://www.php.net/manual/en/migration72.incompatible.php#migration72.incompatible.warn-on-non-countable-types>`_
* `Wddx on PHP <https://www.php.net/manual/en/intro.wddx.php>`_
* `Weak references <https://www.php.net/manual/en/book.weakref.php>`_
* `What are the best practices for catching and re-throwing exceptions? <https://stackoverflow.com/questions/5551668/what-are-the-best-practices-for-catching-and-re-throwing-exceptions>`_
* `What's all this 'immutable date' stuff, anyway? <https://medium.com/@codebyjeff/whats-all-this-immutable-date-stuff-anyway-72d4130af8ce>`_
* `When to declare classes final <http://ocramius.github.io/blog/when-to-declare-classes-final/>`_
* `Why 777 Folder Permissions are a Security Risk <https://www.spiralscripts.co.uk/Blog/why-777-folder-permissions-are-a-security-risk.html>`_
* `Why does PHP 5.2+ disallow abstract static class methods? <https://stackoverflow.com/questions/999066/why-does-php-5-2-disallow-abstract-static-class-methods>`_
* `Why, php? WHY??? <https://gist.github.com/everzet/4215537>`_
* `wikidiff2 <https://www.mediawiki.org/wiki/Extension:Wikidiff2>`_
* `Wincache extension for PHP <http://www.php.net/wincache>`_
* `Wordpress <https://www.wordpress.org/>`_
* `xattr <https://www.php.net/manual/en/book.xattr.php>`_
* `xcache <https://xcache.lighttpd.net/>`_
* `Xdebug <https://xdebug.org/>`_
* `xdiff <https://www.php.net/manual/en/book.xdiff.php>`_
* `XHprof Documentation <http://web.archive.org/web/20110514095512/http://mirror.facebook.net/facebook/xhprof/doc.html>`_
* `XML External Entity <https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XXE%20injection>`_
* `XML Parser <http://www.php.net/manual/en/book.xml.php>`_
* `XML-RPC <http://www.php.net/manual/en/book.xmlrpc.php>`_
* `xmlreader <http://www.php.net/manual/en/book.xmlreader.php>`_
* `XMLWriter <https://www.php.net/manual/en/book.xmlwriter.php>`_
* `XSL extension <https://www.php.net/manual/en/intro.xsl.php>`_
* `YAML Ain't Markup Language <http://www.yaml.org/>`_
* `Yii <http://www.yiiframework.com/>`_
* `Yoda Conditions <https://en.wikipedia.org/wiki/Yoda_conditions>`_
* `Zend Monitor - PHP API <http://files.zend.com/help/Zend-Server/content/zendserverapi/zend_monitor-php_api.htm>`_
* `ZeroMQ <http://zeromq.org/>`_
* `zip <https://en.wikipedia.org/wiki/Zip_(file_format)>`_
* `Zip <https://www.php.net/manual/en/book.zip.php>`_
* `Zlib <https://www.php.net/manual/en/book.zlib.php>`_


Ruleset configurations
----------------------

INI configuration for built-in rulesets. Copy them in config/themes.ini, and make your owns.

24 rulesets detailled here : 

* `Analyze <ruleset_ini_analyze>`_
* `CI-checks <ruleset_ini_ci-checks>`_
* `ClassReview <ruleset_ini_classreview>`_
* `Coding Conventions <ruleset_ini_coding conventions>`_
* `CompatibilityPHP53 <ruleset_ini_compatibilityphp53>`_
* `CompatibilityPHP54 <ruleset_ini_compatibilityphp54>`_
* `CompatibilityPHP55 <ruleset_ini_compatibilityphp55>`_
* `CompatibilityPHP56 <ruleset_ini_compatibilityphp56>`_
* `CompatibilityPHP70 <ruleset_ini_compatibilityphp70>`_
* `CompatibilityPHP71 <ruleset_ini_compatibilityphp71>`_
* `CompatibilityPHP72 <ruleset_ini_compatibilityphp72>`_
* `CompatibilityPHP73 <ruleset_ini_compatibilityphp73>`_
* `CompatibilityPHP74 <ruleset_ini_compatibilityphp74>`_
* `CompatibilityPHP80 <ruleset_ini_compatibilityphp80>`_
* `Dead code <ruleset_ini_dead code>`_
* `LintButWontExec <ruleset_ini_lintbutwontexec>`_
* `Performances <ruleset_ini_performances>`_
* `Rector <ruleset_ini_rector>`_
* `Security <ruleset_ini_security>`_
* `Semantics <ruleset_ini_semantics>`_
* `Suggestions <ruleset_ini_suggestions>`_
* `Top10 <ruleset_ini_top10>`_
* `Typechecks <ruleset_ini_typechecks>`_
* `php-cs-fixable <ruleset_ini_php-cs-fixable>`_



.. _ruleset_ini_analyze:

Analyze
This ruleset centralizes a large number of classic trap and pitfalls when writing PHP.
_______

| [Analyze]
|   analyzer[] = "Arrays/AmbiguousKeys";
|   analyzer[] = "Arrays/MultipleIdenticalKeys";
|   analyzer[] = "Arrays/NoSpreadForHash";
|   analyzer[] = "Arrays/NonConstantArray";
|   analyzer[] = "Arrays/NullBoolean";
|   analyzer[] = "Arrays/RandomlySortedLiterals";
|   analyzer[] = "Arrays/TooManyDimensions";
|   analyzer[] = "Classes/AbstractOrImplements";
|   analyzer[] = "Classes/AbstractStatic";
|   analyzer[] = "Classes/AccessPrivate";
|   analyzer[] = "Classes/AccessProtected";
|   analyzer[] = "Classes/AmbiguousStatic";
|   analyzer[] = "Classes/AmbiguousVisibilities";
|   analyzer[] = "Classes/AvoidOptionArrays";
|   analyzer[] = "Classes/AvoidOptionalProperties";
|   analyzer[] = "Classes/CantExtendFinal";
|   analyzer[] = "Classes/CantInstantiateClass";
|   analyzer[] = "Classes/CheckOnCallUsage";
|   analyzer[] = "Classes/CitSameName";
|   analyzer[] = "Classes/CloneWithNonObject";
|   analyzer[] = "Classes/ConstantClass";
|   analyzer[] = "Classes/CouldBeAbstractClass";
|   analyzer[] = "Classes/CouldBeFinal";
|   analyzer[] = "Classes/CouldBeStatic";
|   analyzer[] = "Classes/CouldBeStringable";
|   analyzer[] = "Classes/CyclicReferences";
|   analyzer[] = "Classes/DependantAbstractClass";
|   analyzer[] = "Classes/DifferentArgumentCounts";
|   analyzer[] = "Classes/DirectCallToMagicMethod";
|   analyzer[] = "Classes/DontSendThisInConstructor";
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/EmptyClass";
|   analyzer[] = "Classes/FinalByOcramius";
|   analyzer[] = "Classes/HiddenNullable";
|   analyzer[] = "Classes/ImplementIsForInterface";
|   analyzer[] = "Classes/ImplementedMethodsArePublic";
|   analyzer[] = "Classes/IncompatibleSignature";
|   analyzer[] = "Classes/IncompatibleSignature74";
|   analyzer[] = "Classes/InstantiatingAbstractClass";
|   analyzer[] = "Classes/MakeDefault";
|   analyzer[] = "Classes/MakeGlobalAProperty";
|   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MissingAbstractMethod";
|   analyzer[] = "Classes/MultipleDeclarations";
|   analyzer[] = "Classes/MultipleTraitOrInterface";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoPSSOutsideClass";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NoPublicAccess";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/NonNullableSetters";
|   analyzer[] = "Classes/NonPpp";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/OldStyleConstructor";
|   analyzer[] = "Classes/OldStyleVar";
|   analyzer[] = "Classes/ParentFirst";
|   analyzer[] = "Classes/PropertyCouldBeLocal";
|   analyzer[] = "Classes/PropertyNeverUsed";
|   analyzer[] = "Classes/PropertyUsedInOneMethodOnly";
|   analyzer[] = "Classes/PssWithoutClass";
|   analyzer[] = "Classes/RedefinedConstants";
|   analyzer[] = "Classes/RedefinedDefault";
|   analyzer[] = "Classes/RedefinedPrivateProperty";
|   analyzer[] = "Classes/ScalarOrObjectProperty";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/ShouldUseThis";
|   analyzer[] = "Classes/StaticContainsThis";
|   analyzer[] = "Classes/StaticMethodsCalledFromObject";
|   analyzer[] = "Classes/SwappedArguments";
|   analyzer[] = "Classes/ThisIsForClasses";
|   analyzer[] = "Classes/ThisIsNotAnArray";
|   analyzer[] = "Classes/ThisIsNotForStatic";
|   analyzer[] = "Classes/ThrowInDestruct";
|   analyzer[] = "Classes/TooManyDereferencing";
|   analyzer[] = "Classes/TooManyFinds";
|   analyzer[] = "Classes/TooManyInjections";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UndefinedClasses";
|   analyzer[] = "Classes/UndefinedConstants";
|   analyzer[] = "Classes/UndefinedParentMP";
|   analyzer[] = "Classes/UndefinedProperty";
|   analyzer[] = "Classes/UndefinedStaticMP";
|   analyzer[] = "Classes/UndefinedStaticclass";
|   analyzer[] = "Classes/UnresolvedClasses";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Classes/UnusedClass";
|   analyzer[] = "Classes/UnusedConstant";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Classes/UseInstanceof";
|   analyzer[] = "Classes/UsedOnceProperty";
|   analyzer[] = "Classes/UselessAbstract";
|   analyzer[] = "Classes/UselessConstructor";
|   analyzer[] = "Classes/UselessFinal";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Classes/WeakType";
|   analyzer[] = "Classes/WrongName";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Constants/BadConstantnames";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Constants/ConstantStrangeNames";
|   analyzer[] = "Constants/CreatedOutsideItsNamespace";
|   analyzer[] = "Constants/InvalidName";
|   analyzer[] = "Constants/MultipleConstantDefinition";
|   analyzer[] = "Constants/StrangeName";
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Exceptions/CantThrow";
|   analyzer[] = "Exceptions/CatchUndefinedVariable";
|   analyzer[] = "Exceptions/ForgottenThrown";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/ThrowFunctioncall";
|   analyzer[] = "Exceptions/UncaughtExceptions";
|   analyzer[] = "Exceptions/Unthrown";
|   analyzer[] = "Exceptions/UselessCatch";
|   analyzer[] = "Files/InclusionWrongCase";
|   analyzer[] = "Files/MissingInclude";
|   analyzer[] = "Functions/AliasesUsage";
|   analyzer[] = "Functions/AvoidBooleanArgument";
|   analyzer[] = "Functions/CallbackNeedsReturn";
|   analyzer[] = "Functions/CancelledParameter";
|   analyzer[] = "Functions/CouldCentralize";
|   analyzer[] = "Functions/DeepDefinitions";
|   analyzer[] = "Functions/DontUseVoid";
|   analyzer[] = "Functions/EmptyFunction";
|   analyzer[] = "Functions/FnArgumentVariableConfusion";
|   analyzer[] = "Functions/HardcodedPasswords";
|   analyzer[] = "Functions/InsufficientTypehint";
|   analyzer[] = "Functions/MismatchParameterAndType";
|   analyzer[] = "Functions/MismatchParameterName";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MismatchedDefaultArguments";
|   analyzer[] = "Functions/MismatchedTypehint";
|   analyzer[] = "Functions/ModifyTypedParameter";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/NeverUsedParameter";
|   analyzer[] = "Functions/NoBooleanAsDefault";
|   analyzer[] = "Functions/NoLiteralForReference";
|   analyzer[] = "Functions/NoReturnUsed";
|   analyzer[] = "Functions/OnlyVariableForReference";
|   analyzer[] = "Functions/OnlyVariablePassedByReference";
|   analyzer[] = "Functions/RedeclaredPhpFunction";
|   analyzer[] = "Functions/RelayFunction";
|   analyzer[] = "Functions/ShouldUseConstants";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Functions/TooManyLocalVariables";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Functions/TypehintedReferences";
|   analyzer[] = "Functions/UndefinedFunctions";
|   analyzer[] = "Functions/UnknownParameterName";
|   analyzer[] = "Functions/UnusedArguments";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UnusedReturnedValue";
|   analyzer[] = "Functions/UseConstantAsArguments";
|   analyzer[] = "Functions/UselessReferenceArgument";
|   analyzer[] = "Functions/UselessReturn";
|   analyzer[] = "Functions/UsesDefaultArguments";
|   analyzer[] = "Functions/UsingDeprecated";
|   analyzer[] = "Functions/WithoutReturn";
|   analyzer[] = "Functions/WrongArgumentType";
|   analyzer[] = "Functions/WrongNumberOfArguments";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Functions/funcGetArgModified";
|   analyzer[] = "Interfaces/AlreadyParentsInterface";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/ConcreteVisibility";
|   analyzer[] = "Interfaces/CouldUseInterface";
|   analyzer[] = "Interfaces/EmptyInterface";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
|   analyzer[] = "Interfaces/RepeatedInterface";
|   analyzer[] = "Interfaces/UndefinedInterfaces";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Namespaces/ConstantFullyQualified";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/HiddenUse";
|   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
|   analyzer[] = "Namespaces/MultipleAliasDefinitions";
|   analyzer[] = "Namespaces/ShouldMakeAlias";
|   analyzer[] = "Namespaces/UnresolvedUse";
|   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/LogicalToInArray";
|   analyzer[] = "Performances/MemoizeMagicCall";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/StrposTooMuch";
|   analyzer[] = "Performances/UseArraySlice";
|   analyzer[] = "Php/ArrayKeyExistsWithObjects";
|   analyzer[] = "Php/AssertFunctionIsReserved";
|   analyzer[] = "Php/AssignAnd";
|   analyzer[] = "Php/Assumptions";
|   analyzer[] = "Php/AvoidMbDectectEncoding";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/Crc32MightBeNegative";
|   analyzer[] = "Php/Deprecated";
|   analyzer[] = "Php/DontPolluteGlobalSpace";
|   analyzer[] = "Php/EmptyList";
|   analyzer[] = "Php/FopenMode";
|   analyzer[] = "Php/ForeachObject";
|   analyzer[] = "Php/HashAlgos";
|   analyzer[] = "Php/Incompilable";
|   analyzer[] = "Php/InternalParameterType";
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Php/MultipleDeclareStrict";
|   analyzer[] = "Php/MustCallParentConstructor";
|   analyzer[] = "Php/NoClassInGlobal";
|   analyzer[] = "Php/NoReferenceForTernary";
|   analyzer[] = "Php/PathinfoReturns";
|   analyzer[] = "Php/ReservedNames";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/ShortOpenTagRequired";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/StrtrArguments";
|   analyzer[] = "Php/TooManyNativeCalls";
|   analyzer[] = "Php/UnknownPcre2Option";
|   analyzer[] = "Php/UseObjectApi";
|   analyzer[] = "Php/UsePathinfo";
|   analyzer[] = "Php/UseSetCookie";
|   analyzer[] = "Php/UseStdclass";
|   analyzer[] = "Php/WrongAttributeConfiguration";
|   analyzer[] = "Php/WrongTypeForNativeFunction";
|   analyzer[] = "Php/oldAutoloadUsage";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Structures/AddZero";
|   analyzer[] = "Structures/AlteringForeachWithoutReference";
|   analyzer[] = "Structures/AlternativeConsistenceByFile";
|   analyzer[] = "Structures/AlwaysFalse";
|   analyzer[] = "Structures/ArrayFillWithObjects";
|   analyzer[] = "Structures/ArrayMergeAndVariadic";
|   analyzer[] = "Structures/ArrayMergeArrayArray";
|   analyzer[] = "Structures/AssigneAndCompare";
|   analyzer[] = "Structures/AutoUnsetForeach";
|   analyzer[] = "Structures/BailOutEarly";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/BreakOutsideLoop";
|   analyzer[] = "Structures/BuriedAssignation";
|   analyzer[] = "Structures/CastToBoolean";
|   analyzer[] = "Structures/CastingTernary";
|   analyzer[] = "Structures/CatchShadowsVariable";
|   analyzer[] = "Structures/CheckAllTypes";
|   analyzer[] = "Structures/CheckJson";
|   analyzer[] = "Structures/CoalesceAndConcat";
|   analyzer[] = "Structures/CommonAlternatives";
|   analyzer[] = "Structures/ComparedComparison";
|   analyzer[] = "Structures/ConcatEmpty";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/CouldBeElse";
|   analyzer[] = "Structures/CouldBeStatic";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/DirThenSlash";
|   analyzer[] = "Structures/DontChangeBlindKey";
|   analyzer[] = "Structures/DontMixPlusPlus";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
|   analyzer[] = "Structures/DoubleAssignation";
|   analyzer[] = "Structures/DoubleInstruction";
|   analyzer[] = "Structures/DoubleObjectAssignation";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/EmptyBlocks";
|   analyzer[] = "Structures/EmptyLines";
|   analyzer[] = "Structures/EmptyTryCatch";
|   analyzer[] = "Structures/ErrorReportingWithInteger";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/ExitUsage";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForeachReferenceIsNotModified";
|   analyzer[] = "Structures/ForeachSourceValue";
|   analyzer[] = "Structures/ForgottenWhiteSpace";
|   analyzer[] = "Structures/GlobalUsage";
|   analyzer[] = "Structures/Htmlentitiescall";
|   analyzer[] = "Structures/IdenticalConditions";
|   analyzer[] = "Structures/IdenticalConsecutive";
|   analyzer[] = "Structures/IdenticalOnBothSides";
|   analyzer[] = "Structures/IfWithSameConditions";
|   analyzer[] = "Structures/Iffectation";
|   analyzer[] = "Structures/ImpliedIf";
|   analyzer[] = "Structures/ImplodeArgsOrder";
|   analyzer[] = "Structures/InconsistentElseif";
|   analyzer[] = "Structures/IndicesAreIntOrString";
|   analyzer[] = "Structures/InfiniteRecursion";
|   analyzer[] = "Structures/InvalidPackFormat";
|   analyzer[] = "Structures/InvalidRegex";
|   analyzer[] = "Structures/IsZero";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LogicalMistakes";
|   analyzer[] = "Structures/LoneBlock";
|   analyzer[] = "Structures/LongArguments";
|   analyzer[] = "Structures/MaxLevelOfIdentation";
|   analyzer[] = "Structures/MbstringThirdArg";
|   analyzer[] = "Structures/MbstringUnknownEncoding";
|   analyzer[] = "Structures/MergeIfThen";
|   analyzer[] = "Structures/MismatchedTernary";
|   analyzer[] = "Structures/MissingCases";
|   analyzer[] = "Structures/MissingNew";
|   analyzer[] = "Structures/MissingParenthesis";
|   analyzer[] = "Structures/MixedConcatInterpolation";
|   analyzer[] = "Structures/ModernEmpty";
|   analyzer[] = "Structures/MultipleDefinedCase";
|   analyzer[] = "Structures/MultipleTypeVariable";
|   analyzer[] = "Structures/MultiplyByOne";
|   analyzer[] = "Structures/NegativePow";
|   analyzer[] = "Structures/NestedIfthen";
|   analyzer[] = "Structures/NestedTernary";
|   analyzer[] = "Structures/NeverNegative";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoAppendOnSource";
|   analyzer[] = "Structures/NoChangeIncomingVariables";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoDirectUsage";
|   analyzer[] = "Structures/NoEmptyRegex";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/NoHardcodedHash";
|   analyzer[] = "Structures/NoHardcodedIp";
|   analyzer[] = "Structures/NoHardcodedPath";
|   analyzer[] = "Structures/NoHardcodedPort";
|   analyzer[] = "Structures/NoIssetWithEmpty";
|   analyzer[] = "Structures/NoNeedForElse";
|   analyzer[] = "Structures/NoNeedForTriple";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoReferenceOnLeft";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/NoVariableIsACondition";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/NotEqual";
|   analyzer[] = "Structures/NotNot";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/OnceUsage";
|   analyzer[] = "Structures/OneLineTwoInstructions";
|   analyzer[] = "Structures/OnlyVariableReturnedByReference";
|   analyzer[] = "Structures/OrDie";
|   analyzer[] = "Structures/PossibleInfiniteLoop";
|   analyzer[] = "Structures/PrintAndDie";
|   analyzer[] = "Structures/PrintWithoutParenthesis";
|   analyzer[] = "Structures/PrintfArguments";
|   analyzer[] = "Structures/QueriesInLoop";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/RepeatedRegex";
|   analyzer[] = "Structures/ResultMayBeMissing";
|   analyzer[] = "Structures/ReturnTrueFalse";
|   analyzer[] = "Structures/SameConditions";
|   analyzer[] = "Structures/ShouldChainException";
|   analyzer[] = "Structures/ShouldMakeTernary";
|   analyzer[] = "Structures/ShouldPreprocess";
|   analyzer[] = "Structures/ShouldUseExplodeArgs";
|   analyzer[] = "Structures/StaticLoop";
|   analyzer[] = "Structures/StripTagsSkipsClosedTag";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/SuspiciousComparison";
|   analyzer[] = "Structures/SwitchToSwitch";
|   analyzer[] = "Structures/SwitchWithoutDefault";
|   analyzer[] = "Structures/TernaryInConcat";
|   analyzer[] = "Structures/TestThenCast";
|   analyzer[] = "Structures/ThrowsAndAssign";
|   analyzer[] = "Structures/TimestampDifference";
|   analyzer[] = "Structures/UncheckedResources";
|   analyzer[] = "Structures/UnconditionLoopBreak";
|   analyzer[] = "Structures/UnknownPregOption";
|   analyzer[] = "Structures/Unpreprocessed";
|   analyzer[] = "Structures/UnsetInForeach";
|   analyzer[] = "Structures/UnsupportedTypesWithOperators";
|   analyzer[] = "Structures/UnusedGlobal";
|   analyzer[] = "Structures/UseConstant";
|   analyzer[] = "Structures/UseInstanceof";
|   analyzer[] = "Structures/UsePositiveCondition";
|   analyzer[] = "Structures/UseSystemTmp";
|   analyzer[] = "Structures/UselessBrackets";
|   analyzer[] = "Structures/UselessCasting";
|   analyzer[] = "Structures/UselessCheck";
|   analyzer[] = "Structures/UselessGlobal";
|   analyzer[] = "Structures/UselessInstruction";
|   analyzer[] = "Structures/UselessParenthesis";
|   analyzer[] = "Structures/UselessSwitch";
|   analyzer[] = "Structures/UselessUnset";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Structures/WrongRange";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Structures/toStringThrowsException";
|   analyzer[] = "Traits/AlreadyParentsTrait";
|   analyzer[] = "Traits/DependantTrait";
|   analyzer[] = "Traits/EmptyTrait";
|   analyzer[] = "Traits/MethodCollisionTraits";
|   analyzer[] = "Traits/TraitNotFound";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Type/OneVariableStrings";
|   analyzer[] = "Type/ShouldTypecast";
|   analyzer[] = "Type/SilentlyCastInteger";
|   analyzer[] = "Type/StringHoldAVariable";
|   analyzer[] = "Type/StringWithStrangeSpace";
|   analyzer[] = "Typehints/MissingReturntype";
|   analyzer[] = "Variables/AssignedTwiceOrMore";
|   analyzer[] = "Variables/ConstantTypo";
|   analyzer[] = "Variables/LostReferences";
|   analyzer[] = "Variables/OverwrittenLiterals";
|   analyzer[] = "Variables/StrangeName";
|   analyzer[] = "Variables/UndefinedConstantName";
|   analyzer[] = "Variables/UndefinedVariable";
|   analyzer[] = "Variables/VariableNonascii";
|   analyzer[] = "Variables/VariableUsedOnce";
|   analyzer[] = "Variables/VariableUsedOnceByContext";
|   analyzer[] = "Variables/WrittenOnlyVariable";| 






.. _ruleset_ini_ci-checks:

CI-checks
This ruleset is a collection of important rules to run in a CI pipeline.
_________

| [CI-checks]
|   analyzer[] = "Arrays/MultipleIdenticalKeys";
|   analyzer[] = "Classes/CheckOnCallUsage";
|   analyzer[] = "Classes/ConstantClass";
|   analyzer[] = "Classes/DirectCallToMagicMethod";
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/MultipleDeclarations";
|   analyzer[] = "Classes/MultipleTraitOrInterface";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NonPpp";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/RedefinedConstants";
|   analyzer[] = "Classes/RedefinedDefault";
|   analyzer[] = "Classes/StaticContainsThis";
|   analyzer[] = "Classes/StaticMethodsCalledFromObject";
|   analyzer[] = "Classes/ThrowInDestruct";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UndefinedConstants";
|   analyzer[] = "Classes/UndefinedProperty";
|   analyzer[] = "Classes/UndefinedStaticclass";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Classes/UseInstanceof";
|   analyzer[] = "Classes/UselessFinal";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Constants/ConstantStrangeNames";
|   analyzer[] = "Constants/MultipleConstantDefinition";
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/ThrowFunctioncall";
|   analyzer[] = "Exceptions/UselessCatch";
|   analyzer[] = "Functions/AliasesUsage";
|   analyzer[] = "Functions/CallbackNeedsReturn";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/NoLiteralForReference";
|   analyzer[] = "Functions/RedeclaredPhpFunction";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Functions/TypehintedReferences";
|   analyzer[] = "Functions/UndefinedFunctions";
|   analyzer[] = "Functions/UnknownParameterName";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UseConstantAsArguments";
|   analyzer[] = "Functions/UsesDefaultArguments";
|   analyzer[] = "Functions/WrongNumberOfArguments";
|   analyzer[] = "Functions/WrongOptionalParameter";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/UndefinedInterfaces";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/HiddenUse";
|   analyzer[] = "Namespaces/MultipleAliasDefinitionPerFile";
|   analyzer[] = "Namespaces/MultipleAliasDefinitions";
|   analyzer[] = "Namespaces/ShouldMakeAlias";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/StrposTooMuch";
|   analyzer[] = "Performances/UseArraySlice";
|   analyzer[] = "Php/AssignAnd";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/Deprecated";
|   analyzer[] = "Php/FopenMode";
|   analyzer[] = "Php/InternalParameterType";
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Php/NoClassInGlobal";
|   analyzer[] = "Php/NoReferenceForTernary";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/StrtrArguments";
|   analyzer[] = "Php/UseObjectApi";
|   analyzer[] = "Php/UsePathinfo";
|   analyzer[] = "Php/WrongTypeForNativeFunction";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Structures/AddZero";
|   analyzer[] = "Structures/AlteringForeachWithoutReference";
|   analyzer[] = "Structures/AssigneAndCompare";
|   analyzer[] = "Structures/AutoUnsetForeach";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/CastingTernary";
|   analyzer[] = "Structures/CheckJson";
|   analyzer[] = "Structures/CoalesceAndConcat";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/DirThenSlash";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/EmptyBlocks";
|   analyzer[] = "Structures/ErrorReportingWithInteger";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/ExitUsage";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForeachReferenceIsNotModified";
|   analyzer[] = "Structures/ForgottenWhiteSpace";
|   analyzer[] = "Structures/Htmlentitiescall";
|   analyzer[] = "Structures/IdenticalConditions";
|   analyzer[] = "Structures/IdenticalOnBothSides";
|   analyzer[] = "Structures/IfWithSameConditions";
|   analyzer[] = "Structures/ImpliedIf";
|   analyzer[] = "Structures/ImplodeArgsOrder";
|   analyzer[] = "Structures/IndicesAreIntOrString";
|   analyzer[] = "Structures/InvalidPackFormat";
|   analyzer[] = "Structures/InvalidRegex";
|   analyzer[] = "Structures/IsZero";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LogicalMistakes";
|   analyzer[] = "Structures/LoneBlock";
|   analyzer[] = "Structures/MbstringThirdArg";
|   analyzer[] = "Structures/MbstringUnknownEncoding";
|   analyzer[] = "Structures/MergeIfThen";
|   analyzer[] = "Structures/MissingParenthesis";
|   analyzer[] = "Structures/MultipleDefinedCase";
|   analyzer[] = "Structures/MultiplyByOne";
|   analyzer[] = "Structures/NegativePow";
|   analyzer[] = "Structures/NestedTernary";
|   analyzer[] = "Structures/NeverNegative";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoEmptyRegex";
|   analyzer[] = "Structures/NoIssetWithEmpty";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoReferenceOnLeft";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/NotEqual";
|   analyzer[] = "Structures/NotNot";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/OrDie";
|   analyzer[] = "Structures/PrintAndDie";
|   analyzer[] = "Structures/PrintWithoutParenthesis";
|   analyzer[] = "Structures/PrintfArguments";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/RepeatedRegex";
|   analyzer[] = "Structures/ResultMayBeMissing";
|   analyzer[] = "Structures/ReturnTrueFalse";
|   analyzer[] = "Structures/SameConditions";
|   analyzer[] = "Structures/ShouldChainException";
|   analyzer[] = "Structures/ShouldMakeTernary";
|   analyzer[] = "Structures/ShouldUseExplodeArgs";
|   analyzer[] = "Structures/StripTagsSkipsClosedTag";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/SwitchWithoutDefault";
|   analyzer[] = "Structures/TernaryInConcat";
|   analyzer[] = "Structures/ThrowsAndAssign";
|   analyzer[] = "Structures/TimestampDifference";
|   analyzer[] = "Structures/UncheckedResources";
|   analyzer[] = "Structures/UnconditionLoopBreak";
|   analyzer[] = "Structures/UseConstant";
|   analyzer[] = "Structures/UseInstanceof";
|   analyzer[] = "Structures/UseSystemTmp";
|   analyzer[] = "Structures/UselessBrackets";
|   analyzer[] = "Structures/UselessCasting";
|   analyzer[] = "Structures/UselessCheck";
|   analyzer[] = "Structures/UselessInstruction";
|   analyzer[] = "Structures/UselessParenthesis";
|   analyzer[] = "Structures/UselessUnset";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Type/OneVariableStrings";
|   analyzer[] = "Type/ShouldTypecast";
|   analyzer[] = "Type/SilentlyCastInteger";
|   analyzer[] = "Type/StringWithStrangeSpace";
|   analyzer[] = "Typehints/MissingReturntype";
|   analyzer[] = "Variables/UndefinedVariable";| 






.. _ruleset_ini_classreview:

ClassReview
This ruleset focuses on classes construction issues, and their related structures : traits, interfaces, methods, properties, constants.
___________

| [ClassReview]
|   analyzer[] = "Classes/AvoidOptionArrays";
|   analyzer[] = "Classes/CancelCommonMethod";
|   analyzer[] = "Classes/CouldBeAbstractClass";
|   analyzer[] = "Classes/CouldBeClassConstant";
|   analyzer[] = "Classes/CouldBeFinal";
|   analyzer[] = "Classes/CouldBeParentMethod";
|   analyzer[] = "Classes/CouldBePrivate";
|   analyzer[] = "Classes/CouldBePrivateConstante";
|   analyzer[] = "Classes/CouldBePrivateMethod";
|   analyzer[] = "Classes/CouldBeProtectedConstant";
|   analyzer[] = "Classes/CouldBeProtectedMethod";
|   analyzer[] = "Classes/CouldBeProtectedProperty";
|   analyzer[] = "Classes/CouldBeStatic";
|   analyzer[] = "Classes/CyclicReferences";
|   analyzer[] = "Classes/DependantAbstractClass";
|   analyzer[] = "Classes/DifferentArgumentCounts";
|   analyzer[] = "Classes/DisconnectedClasses";
|   analyzer[] = "Classes/Finalclass";
|   analyzer[] = "Classes/Finalmethod";
|   analyzer[] = "Classes/FossilizedMethod";
|   analyzer[] = "Classes/HiddenNullable";
|   analyzer[] = "Classes/InsufficientPropertyTypehint";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MissingAbstractMethod";
|   analyzer[] = "Classes/MutualExtension";
|   analyzer[] = "Classes/NoParent";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/NonNullableSetters";
|   analyzer[] = "Classes/PropertyCouldBeLocal";
|   analyzer[] = "Classes/RaisedAccessLevel";
|   analyzer[] = "Classes/RedefinedProperty";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/UndeclaredStaticProperty";
|   analyzer[] = "Classes/UninitedProperty";
|   analyzer[] = "Classes/UnreachableConstant";
|   analyzer[] = "Classes/UnusedConstant";
|   analyzer[] = "Classes/UselessTypehint";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Functions/ExceedingTypehint";
|   analyzer[] = "Functions/ModifyTypedParameter";
|   analyzer[] = "Functions/NullableWithoutCheck";
|   analyzer[] = "Functions/WrongReturnedType";
|   analyzer[] = "Interfaces/AvoidSelfInInterface";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/NoGaranteeForPropertyConstant";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Performances/MemoizeMagicCall";
|   analyzer[] = "Structures/CouldBeStatic";
|   analyzer[] = "Structures/DoubleObjectAssignation";
|   analyzer[] = "Traits/SelfUsingTrait";
|   analyzer[] = "Traits/UnusedClassTrait";| 






.. _ruleset_ini_coding conventions:

Coding Conventions
This ruleset centralizes all analysis related to coding conventions. Sometimes, those are easy to extract with static analysis, and so here they are. No all o them are available.
__________________

| [Coding Conventions]
|   analyzer[] = "Arrays/EmptySlots";
|   analyzer[] = "Arrays/MistakenConcatenation";
|   analyzer[] = "Classes/MultipleClassesInFile";
|   analyzer[] = "Classes/OrderOfDeclaration";
|   analyzer[] = "Classes/WrongCase";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Functions/OneLetterFunctions";
|   analyzer[] = "Functions/WrongCase";
|   analyzer[] = "Functions/WrongTypehintedName";
|   analyzer[] = "Namespaces/UseWithFullyQualifiedNS";
|   analyzer[] = "Namespaces/WrongCase";
|   analyzer[] = "Php/CloseTags";
|   analyzer[] = "Php/ReturnWithParenthesis";
|   analyzer[] = "Php/UpperCaseFunction";
|   analyzer[] = "Php/UpperCaseKeyword";
|   analyzer[] = "Structures/Bracketless";
|   analyzer[] = "Structures/ConstantComparisonConsistance";
|   analyzer[] = "Structures/DontBeTooManual";
|   analyzer[] = "Structures/EchoPrintConsistance";
|   analyzer[] = "Structures/HeredocDelimiterFavorite";
|   analyzer[] = "Structures/MixedConcatInterpolation";
|   analyzer[] = "Structures/PlusEgalOne";
|   analyzer[] = "Structures/YodaComparison";
|   analyzer[] = "Type/ShouldBeSingleQuote";
|   analyzer[] = "Type/SimilarIntegers";
|   analyzer[] = "Type/StringInterpolation";
|   analyzer[] = "Variables/VariableUppercase";| 






.. _ruleset_ini_compatibilityphp53:

CompatibilityPHP53
This ruleset centralizes all analysis for the migration from PHP 5.2 to 5.3.
__________________

| [CompatibilityPHP53]
|   analyzer[] = "Arrays/ArrayNSUsage";
|   analyzer[] = "Arrays/MixedKeys";
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extdba";
|   analyzer[] = "Extensions/Extfdf";
|   analyzer[] = "Extensions/Extming";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/CantUseReturnValueInWriteContext";
|   analyzer[] = "Php/CaseForPSS";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/ClosureThisSupport";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/MethodCallOnNew";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php54NewFunctions";
|   analyzer[] = "Php/Php55NewFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/StaticclassUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/Break0";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/DereferencingAS";
|   analyzer[] = "Structures/ForeachWithList";
|   analyzer[] = "Structures/FunctionSubscripting";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/Binary";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";| 






.. _ruleset_ini_compatibilityphp54:

CompatibilityPHP54
This ruleset centralizes all analysis for the migration from PHP 5.3 to 5.4.
__________________

| [CompatibilityPHP54]
|   analyzer[] = "Arrays/MixedKeys";
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extmhash";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/CantUseReturnValueInWriteContext";
|   analyzer[] = "Php/CaseForPSS";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php54RemovedFunctions";
|   analyzer[] = "Php/Php55NewFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/StaticclassUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/BreakNonInteger";
|   analyzer[] = "Structures/CalltimePassByReference";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/CryptWithoutSalt";
|   analyzer[] = "Structures/DereferencingAS";
|   analyzer[] = "Structures/ForeachWithList";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";| 






.. _ruleset_ini_compatibilityphp55:

CompatibilityPHP55
This ruleset centralizes all analysis for the migration from PHP 5.4 to 5.5.
__________________

| [CompatibilityPHP55]
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extapc";
|   analyzer[] = "Extensions/Extmysql";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Namespaces/UseFunctionsConstants";
|   analyzer[] = "Php/ClassConstWithArray";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/ConstWithArray";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/EllipsisUsage";
|   analyzer[] = "Php/ExponentUsage";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Password55";
|   analyzer[] = "Php/Php55RemovedFunctions";
|   analyzer[] = "Php/Php56NewFunctions";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/debugInfoUsage";
|   analyzer[] = "Structures/ConstantScalarExpression";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";| 






.. _ruleset_ini_compatibilityphp56:

CompatibilityPHP56
This ruleset centralizes all analysis for the migration from PHP 5.5 to 5.6.
__________________

| [CompatibilityPHP56]
|   analyzer[] = "Classes/Anonymous";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/NonStaticMethodsCalledStatic";
|   analyzer[] = "Classes/NullOnNew";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Functions/GeneratorCannotReturn";
|   analyzer[] = "Functions/MultipleSameArguments";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/DefineWithArray";
|   analyzer[] = "Php/DirectCallToClone";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseDeclaration";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoListWithString";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoReturnForGenerator";
|   analyzer[] = "Php/NoStringWithAppend";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP70scalartypehints";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/ParenthesisAsParameter";
|   analyzer[] = "Php/Php70NewClasses";
|   analyzer[] = "Php/Php70NewFunctions";
|   analyzer[] = "Php/Php70NewInterfaces";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php7RelaxedKeyword";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/RawPostDataUsage";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnicodeEscapePartial";
|   analyzer[] = "Php/UnicodeEscapeSyntax";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/IssetWithConstant";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/SwitchWithMultipleDefault";
|   analyzer[] = "Structures/VariableGlobal";
|   analyzer[] = "Type/MalformedOctal";
|   analyzer[] = "Variables/Php5IndirectExpression";
|   analyzer[] = "Variables/Php7IndirectExpression";| 






.. _ruleset_ini_compatibilityphp70:

CompatibilityPHP70
This ruleset centralizes all analysis for the migration from PHP 5.6 to 7.0.
__________________

| [CompatibilityPHP70]
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/ConstVisibilityUsage";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/toStringPss";
|   analyzer[] = "Exceptions/MultipleCatch";
|   analyzer[] = "Extensions/Extereg";
|   analyzer[] = "Functions/funcGetArgModified";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/EmptyList";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/ForeachDontChangePointer";
|   analyzer[] = "Php/GlobalWithoutSimpleVariable";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashAlgos71";
|   analyzer[] = "Php/ListShortSyntax";
|   analyzer[] = "Php/ListWithAppends";
|   analyzer[] = "Php/ListWithKeys";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/NoSubstrMinusOne";
|   analyzer[] = "Php/PHP71scalartypehints";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php70RemovedDirective";
|   analyzer[] = "Php/Php70RemovedFunctions";
|   analyzer[] = "Php/Php71NewClasses";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/ReservedKeywords7";
|   analyzer[] = "Php/SetExceptionHandlerPHP7";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Php/UseNullableType";
|   analyzer[] = "Php/UsortSorting";
|   analyzer[] = "Structures/BreakOutsideLoop";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/McryptcreateivWithoutOption";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/SetlocaleNeedsConstants";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Type/HexadecimalString";
|   analyzer[] = "Variables/Php7IndirectExpression";| 






.. _ruleset_ini_compatibilityphp71:

CompatibilityPHP71
This ruleset centralizes all analysis for the migration from PHP 7.0 to 7.1.
__________________

| [CompatibilityPHP71]
|   analyzer[] = "Arrays/StringInitialization";
|   analyzer[] = "Classes/CantInheritAbstractMethod";
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/IntegerAsProperty";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Extensions/Extmcrypt";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/GroupUseTrailingComma";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/PHP72scalartypehints";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php70RemovedDirective";
|   analyzer[] = "Php/Php70RemovedFunctions";
|   analyzer[] = "Php/Php71NewFunctions";
|   analyzer[] = "Php/Php71RemovedDirective";
|   analyzer[] = "Php/Php71microseconds";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/pregOptionE";
|   analyzer[] = "Type/HexadecimalString";
|   analyzer[] = "Type/OctalInString";| 






.. _ruleset_ini_compatibilityphp72:

CompatibilityPHP72
This ruleset centralizes all analysis for the migration from PHP 7.1 to 7.2.
__________________

| [CompatibilityPHP72]
|   analyzer[] = "Constants/UndefinedConstants";
|   analyzer[] = "Php/AvoidSetErrorHandlerContextArg";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/FlexibleHeredoc";
|   analyzer[] = "Php/HashAlgos53";
|   analyzer[] = "Php/HashAlgos54";
|   analyzer[] = "Php/HashUsesObjects";
|   analyzer[] = "Php/ListWithReference";
|   analyzer[] = "Php/NoReferenceForStaticProperty";
|   analyzer[] = "Php/PHP73LastEmptyArgument";
|   analyzer[] = "Php/Php72Deprecation";
|   analyzer[] = "Php/Php72NewClasses";
|   analyzer[] = "Php/Php72NewConstants";
|   analyzer[] = "Php/Php72NewFunctions";
|   analyzer[] = "Php/Php72ObjectKeyword";
|   analyzer[] = "Php/Php72RemovedFunctions";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/TrailingComma";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/CanCountNonCountable";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/NoGetClassNull";
|   analyzer[] = "Structures/pregOptionE";| 






.. _ruleset_ini_compatibilityphp73:

CompatibilityPHP73
This ruleset centralizes all analysis for the migration from PHP 7.2 to 7.3.
__________________

| [CompatibilityPHP73]
|   analyzer[] = "Constants/CaseInsensitiveConstants";
|   analyzer[] = "Php/AssertFunctionIsReserved";
|   analyzer[] = "Php/CoalesceEqual";
|   analyzer[] = "Php/CompactInexistant";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/IntegerSeparatorUsage";
|   analyzer[] = "Php/Php73NewFunctions";
|   analyzer[] = "Php/Php73RemovedFunctions";
|   analyzer[] = "Php/Php74NewDirective";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/TypedPropertyUsage";
|   analyzer[] = "Php/UnknownPcre2Option";
|   analyzer[] = "Php/UnpackingInsideArrays";
|   analyzer[] = "Structures/ContinueIsForLoop";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";| 






.. _ruleset_ini_compatibilityphp74:

CompatibilityPHP74
This ruleset centralizes all analysis for the migration from PHP 7.3 to 7.4.
__________________

| [CompatibilityPHP74]
|   analyzer[] = "Functions/UnbindingClosures";
|   analyzer[] = "Php/ArrayKeyExistsWithObjects";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/DetectCurrentClass";
|   analyzer[] = "Php/FilterToAddSlashes";
|   analyzer[] = "Php/HashAlgos74";
|   analyzer[] = "Php/IdnUts46";
|   analyzer[] = "Php/NestedTernaryWithoutParenthesis";
|   analyzer[] = "Php/NoMoreCurlyArrays";
|   analyzer[] = "Php/Php74Deprecation";
|   analyzer[] = "Php/Php74NewClasses";
|   analyzer[] = "Php/Php74NewConstants";
|   analyzer[] = "Php/Php74NewFunctions";
|   analyzer[] = "Php/Php74RemovedDirective";
|   analyzer[] = "Php/Php74RemovedFunctions";
|   analyzer[] = "Php/Php74ReservedKeyword";
|   analyzer[] = "Php/Php74mbstrrpos3rdArg";
|   analyzer[] = "Php/Php80NewFunctions";
|   analyzer[] = "Php/Php80OnlyTypeHints";
|   analyzer[] = "Php/Php80UnionTypehint";
|   analyzer[] = "Php/Php80VariableSyntax";
|   analyzer[] = "Php/ReflectionExportIsDeprecated";
|   analyzer[] = "Php/ScalarAreNotArrays";
|   analyzer[] = "Php/SignatureTrailingComma";
|   analyzer[] = "Php/ThrowWasAnExpression";
|   analyzer[] = "Php/UseMatch";
|   analyzer[] = "Structures/CurlVersionNow";
|   analyzer[] = "Structures/DontReadAndWriteInOneExpression";
|   analyzer[] = "Structures/OpensslRandomPseudoByteSecondArg";| 






.. _ruleset_ini_compatibilityphp80:

CompatibilityPHP80
This ruleset centralizes all analysis for the migration from PHP 7.4 to 8.0.
__________________

| [CompatibilityPHP80]
|   analyzer[] = "Arrays/NegativeStart";
|   analyzer[] = "Classes/OldStyleConstructor";
|   analyzer[] = "Functions/MismatchParameterName";
|   analyzer[] = "Functions/NullableWithConstant";
|   analyzer[] = "Php/CastUnsetUsage";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/Php80NamedParameterVariadic";
|   analyzer[] = "Php/Php80RemovedConstant";
|   analyzer[] = "Php/Php80RemovedDirective";
|   analyzer[] = "Php/Php80RemovedFunctions";
|   analyzer[] = "Php/Php80RemovesResources";
|   analyzer[] = "Php/PhpErrorMsgUsage";
|   analyzer[] = "Structures/UnsupportedTypesWithOperators";| 






.. _ruleset_ini_dead code:

Dead code
This ruleset focuses on dead code : expressions or even structures that are written, valid but never used.
_________

| [Dead code]
|   analyzer[] = "Classes/CantExtendFinal";
|   analyzer[] = "Classes/LocallyUnusedProperty";
|   analyzer[] = "Classes/UnresolvedCatch";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Classes/UnusedClass";
|   analyzer[] = "Classes/UnusedMethods";
|   analyzer[] = "Classes/UnusedPrivateMethod";
|   analyzer[] = "Classes/UnusedPrivateProperty";
|   analyzer[] = "Classes/UnusedProtectedMethods";
|   analyzer[] = "Constants/UnusedConstants";
|   analyzer[] = "Exceptions/AlreadyCaught";
|   analyzer[] = "Exceptions/CaughtButNotThrown";
|   analyzer[] = "Exceptions/Rethrown";
|   analyzer[] = "Exceptions/Unthrown";
|   analyzer[] = "Functions/UnusedFunctions";
|   analyzer[] = "Functions/UnusedInheritedVariable";
|   analyzer[] = "Functions/UnusedReturnedValue";
|   analyzer[] = "Functions/UselessTypeCheck";
|   analyzer[] = "Interfaces/UnusedInterfaces";
|   analyzer[] = "Namespaces/EmptyNamespace";
|   analyzer[] = "Namespaces/UnusedUse";
|   analyzer[] = "Structures/EmptyLines";
|   analyzer[] = "Structures/UnreachableCode";
|   analyzer[] = "Structures/UnsetInForeach";
|   analyzer[] = "Structures/UnusedLabel";
|   analyzer[] = "Traits/SelfUsingTrait";| 






.. _ruleset_ini_lintbutwontexec:

LintButWontExec
This ruleset focuses on PHP code that lint (php -l), but that will not run. As such, this ruleset tries to go further than PHP, by connecting files, just like during execution.
_______________

| [LintButWontExec]
|   analyzer[] = "Classes/AbstractOrImplements";
|   analyzer[] = "Classes/CloneWithNonObject";
|   analyzer[] = "Classes/CouldBeStringable";
|   analyzer[] = "Classes/Finalclass";
|   analyzer[] = "Classes/Finalmethod";
|   analyzer[] = "Classes/IncompatibleSignature";
|   analyzer[] = "Classes/MethodSignatureMustBeCompatible";
|   analyzer[] = "Classes/MismatchProperties";
|   analyzer[] = "Classes/MutualExtension";
|   analyzer[] = "Classes/NoMagicWithArray";
|   analyzer[] = "Classes/NoPSSOutsideClass";
|   analyzer[] = "Classes/NoSelfReferencingConstant";
|   analyzer[] = "Classes/RaisedAccessLevel";
|   analyzer[] = "Classes/UsingThisOutsideAClass";
|   analyzer[] = "Classes/WrongTypedPropertyInit";
|   analyzer[] = "Exceptions/CantThrow";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MustReturn";
|   analyzer[] = "Functions/OnlyVariableForReference";
|   analyzer[] = "Functions/TypehintMustBeReturned";
|   analyzer[] = "Interfaces/CantImplementTraversable";
|   analyzer[] = "Interfaces/ConcreteVisibility";
|   analyzer[] = "Interfaces/IsNotImplemented";
|   analyzer[] = "Interfaces/RepeatedInterface";
|   analyzer[] = "Traits/MethodCollisionTraits";
|   analyzer[] = "Traits/TraitNotFound";
|   analyzer[] = "Traits/UndefinedInsteadof";
|   analyzer[] = "Traits/UndefinedTrait";
|   analyzer[] = "Traits/UselessAlias";| 






.. _ruleset_ini_performances:

Performances
This ruleset focuses on performances issues : anything that slows the code's execution.
____________

| [Performances]
|   analyzer[] = "Arrays/GettingLastElement";
|   analyzer[] = "Arrays/SliceFirst";
|   analyzer[] = "Classes/MakeMagicConcrete";
|   analyzer[] = "Classes/UseClassOperator";
|   analyzer[] = "Functions/Closure2String";
|   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/Autoappend";
|   analyzer[] = "Performances/AvoidArrayPush";
|   analyzer[] = "Performances/CacheVariableOutsideLoop";
|   analyzer[] = "Performances/CsvInLoops";
|   analyzer[] = "Performances/DoInBase";
|   analyzer[] = "Performances/DoubleArrayFlip";
|   analyzer[] = "Performances/FetchOneRowFormat";
|   analyzer[] = "Performances/IssetWholeArray";
|   analyzer[] = "Performances/JoinFile";
|   analyzer[] = "Performances/MakeOneCall";
|   analyzer[] = "Performances/MbStringInLoop";
|   analyzer[] = "Performances/NoConcatInLoop";
|   analyzer[] = "Performances/NoGlob";
|   analyzer[] = "Performances/NotCountNull";
|   analyzer[] = "Performances/OptimizeExplode";
|   analyzer[] = "Performances/PHP7EncapsedStrings";
|   analyzer[] = "Performances/Php74ArrayKeyExists";
|   analyzer[] = "Performances/PrePostIncrement";
|   analyzer[] = "Performances/RegexOnArrays";
|   analyzer[] = "Performances/RegexOnCollector";
|   analyzer[] = "Performances/SimpleSwitch";
|   analyzer[] = "Performances/SlowFunctions";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Performances/UseBlindVar";
|   analyzer[] = "Performances/timeVsstrtotime";
|   analyzer[] = "Php/ShouldUseArrayColumn";
|   analyzer[] = "Php/ShouldUseFunction";
|   analyzer[] = "Php/UsePathinfoArgs";
|   analyzer[] = "Structures/CouldUseShortAssignation";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/ForWithFunctioncall";
|   analyzer[] = "Structures/GlobalOutsideLoop";
|   analyzer[] = "Structures/NoArrayUnique";
|   analyzer[] = "Structures/NoAssignationInFunction";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/Noscream";
|   analyzer[] = "Structures/SimplePreg";
|   analyzer[] = "Structures/WhileListEach";| 






.. _ruleset_ini_rector:

Rector
`RectorPHP <https://getrector.org/>`_ is a reconstructor tool. It applies modifications in the PHP code automatically. Exakat finds results which may be automatically updated with rector. 
______

| [Rector]
|   analyzer[] = "Php/IsAWithString";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/ShouldPreprocess";| 






.. _ruleset_ini_security:

Security
This ruleset focuses on code security. 
________

| [Security]
|   analyzer[] = "Functions/HardcodedPasswords";
|   analyzer[] = "Php/BetterRand";
|   analyzer[] = "Security/AnchorRegex";
|   analyzer[] = "Security/AvoidThoseCrypto";
|   analyzer[] = "Security/CompareHash";
|   analyzer[] = "Security/ConfigureExtract";
|   analyzer[] = "Security/CryptoKeyLength";
|   analyzer[] = "Security/CurlOptions";
|   analyzer[] = "Security/DirectInjection";
|   analyzer[] = "Security/DontEchoError";
|   analyzer[] = "Security/DynamicDl";
|   analyzer[] = "Security/EncodedLetters";
|   analyzer[] = "Security/FilterInputSource";
|   analyzer[] = "Security/IndirectInjection";
|   analyzer[] = "Security/IntegerConversion";
|   analyzer[] = "Security/KeepFilesRestricted";
|   analyzer[] = "Security/MinusOneOnError";
|   analyzer[] = "Security/MkdirDefault";
|   analyzer[] = "Security/MoveUploadedFile";
|   analyzer[] = "Security/NoEntIgnore";
|   analyzer[] = "Security/NoNetForXmlLoad";
|   analyzer[] = "Security/NoSleep";
|   analyzer[] = "Security/NoWeakSSLCrypto";
|   analyzer[] = "Security/RegisterGlobals";
|   analyzer[] = "Security/SafeHttpHeaders";
|   analyzer[] = "Security/SessionLazyWrite";
|   analyzer[] = "Security/SetCookieArgs";
|   analyzer[] = "Security/ShouldUsePreparedStatement";
|   analyzer[] = "Security/ShouldUseSessionRegenerateId";
|   analyzer[] = "Security/Sqlite3RequiresSingleQuotes";
|   analyzer[] = "Security/UnserializeSecondArg";
|   analyzer[] = "Security/UploadFilenameInjection";
|   analyzer[] = "Security/parseUrlWithoutParameters";
|   analyzer[] = "Structures/EvalUsage";
|   analyzer[] = "Structures/EvalWithoutTry";
|   analyzer[] = "Structures/Fallthrough";
|   analyzer[] = "Structures/NoHardcodedHash";
|   analyzer[] = "Structures/NoHardcodedIp";
|   analyzer[] = "Structures/NoHardcodedPort";
|   analyzer[] = "Structures/NoReturnInFinally";
|   analyzer[] = "Structures/PhpinfoUsage";
|   analyzer[] = "Structures/RandomWithoutTry";
|   analyzer[] = "Structures/VardumpUsage";
|   analyzer[] = "Structures/pregOptionE";| 






.. _ruleset_ini_semantics:

Semantics
This ruleset focuses on human interpretation of the code. It reviews special values of literals, and named structures.
_________

| [Semantics]
|   analyzer[] = "Arrays/WeirdIndex";
|   analyzer[] = "Functions/FnArgumentVariableConfusion";
|   analyzer[] = "Functions/MismatchParameterAndType";
|   analyzer[] = "Functions/OneLetterFunctions";
|   analyzer[] = "Functions/ParameterHiding";
|   analyzer[] = "Functions/PrefixToType";
|   analyzer[] = "Functions/SemanticTyping";
|   analyzer[] = "Functions/WrongTypehintedName";
|   analyzer[] = "Php/ClassFunctionConfusion";
|   analyzer[] = "Structures/PropertyVariableConfusion";
|   analyzer[] = "Type/DuplicateLiteral";
|   analyzer[] = "Type/SimilarIntegers";
|   analyzer[] = "Variables/VariableOneLetter";| 






.. _ruleset_ini_suggestions:

Suggestions
This ruleset focuses on possibly better syntax than the one currently used. Those may be code modernization, alternatives, more efficient solutions, or simply left over from older versions. 
___________

| [Suggestions]
|   analyzer[] = "Arrays/RandomlySortedLiterals";
|   analyzer[] = "Arrays/ShouldPreprocess";
|   analyzer[] = "Arrays/SliceFirst";
|   analyzer[] = "Classes/CancelCommonMethod";
|   analyzer[] = "Classes/ParentFirst";
|   analyzer[] = "Classes/ShouldDeepClone";
|   analyzer[] = "Classes/ShouldHaveDestructor";
|   analyzer[] = "Classes/ShouldUseSelf";
|   analyzer[] = "Classes/TooManyChildren";
|   analyzer[] = "Classes/UnitializedProperties";
|   analyzer[] = "Classes/UselessTypehint";
|   analyzer[] = "Constants/CouldBeConstant";
|   analyzer[] = "Exceptions/CouldUseTry";
|   analyzer[] = "Exceptions/LargeTryBlock";
|   analyzer[] = "Exceptions/OverwriteException";
|   analyzer[] = "Exceptions/UnusedExceptionVariable";
|   analyzer[] = "Functions/AddDefaultValue";
|   analyzer[] = "Functions/Closure2String";
|   analyzer[] = "Functions/CouldBeStaticClosure";
|   analyzer[] = "Functions/CouldCentralize";
|   analyzer[] = "Functions/NeverUsedParameter";
|   analyzer[] = "Functions/NoReturnUsed";
|   analyzer[] = "Functions/TooManyParameters";
|   analyzer[] = "Functions/TooMuchIndented";
|   analyzer[] = "Functions/UselessDefault";
|   analyzer[] = "Interfaces/AlreadyParentsInterface";
|   analyzer[] = "Interfaces/UnusedInterfaces";
|   analyzer[] = "Namespaces/AliasConfusion";
|   analyzer[] = "Namespaces/CouldUseAlias";
|   analyzer[] = "Patterns/AbstractAway";
|   analyzer[] = "Performances/ArrayKeyExistsSpeedup";
|   analyzer[] = "Performances/IssetWholeArray";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Php/AvoidReal";
|   analyzer[] = "Php/CompactInexistant";
|   analyzer[] = "Php/CouldUseIsCountable";
|   analyzer[] = "Php/CouldUsePromotedProperties";
|   analyzer[] = "Php/DetectCurrentClass";
|   analyzer[] = "Php/ImplodeOneArg";
|   analyzer[] = "Php/IssetMultipleArgs";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/NewExponent";
|   analyzer[] = "Php/PregMatchAllFlag";
|   analyzer[] = "Php/ReturnWithParenthesis";
|   analyzer[] = "Php/ShouldPreprocess";
|   analyzer[] = "Php/ShouldUseArrayColumn";
|   analyzer[] = "Php/ShouldUseArrayFilter";
|   analyzer[] = "Php/ShouldUseCoalesce";
|   analyzer[] = "Php/UseDateTimeImmutable";
|   analyzer[] = "Php/UseGetDebugType";
|   analyzer[] = "Php/UseSessionStartOptions";
|   analyzer[] = "Php/UseStrContains";
|   analyzer[] = "Structures/BasenameSuffix";
|   analyzer[] = "Structures/BooleanStrictComparison";
|   analyzer[] = "Structures/CouldUseArrayFillKeys";
|   analyzer[] = "Structures/CouldUseArrayUnique";
|   analyzer[] = "Structures/CouldUseCompact";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/DirectlyUseFile";
|   analyzer[] = "Structures/DontCompareTypedBoolean";
|   analyzer[] = "Structures/DontLoopOnYield";
|   analyzer[] = "Structures/DropElseAfterReturn";
|   analyzer[] = "Structures/EchoWithConcat";
|   analyzer[] = "Structures/EmptyWithExpression";
|   analyzer[] = "Structures/FunctionPreSubscripting";
|   analyzer[] = "Structures/JsonWithOption";
|   analyzer[] = "Structures/ListOmissions";
|   analyzer[] = "Structures/LongBlock";
|   analyzer[] = "Structures/MismatchedTernary";
|   analyzer[] = "Structures/MultipleUnset";
|   analyzer[] = "Structures/NamedRegex";
|   analyzer[] = "Structures/NoNeedGetClass";
|   analyzer[] = "Structures/NoParenthesisForLanguageConstruct";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/OneIfIsSufficient";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/PossibleIncrement";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/ReuseVariable";
|   analyzer[] = "Structures/SGVariablesConfusion";
|   analyzer[] = "Structures/SetAside";
|   analyzer[] = "Structures/ShouldUseForeach";
|   analyzer[] = "Structures/ShouldUseMath";
|   analyzer[] = "Structures/ShouldUseOperator";
|   analyzer[] = "Structures/SubstrLastArg";
|   analyzer[] = "Structures/SubstrToTrim";
|   analyzer[] = "Structures/UnreachableCode";
|   analyzer[] = "Structures/UseArrayFunctions";
|   analyzer[] = "Structures/UseCaseValue";
|   analyzer[] = "Structures/UseCountRecursive";
|   analyzer[] = "Structures/UseListWithForeach";
|   analyzer[] = "Structures/UseUrlQueryFunctions";
|   analyzer[] = "Structures/WhileListEach";
|   analyzer[] = "Traits/MultipleUsage";
|   analyzer[] = "Variables/ComplexDynamicNames";| 






.. _ruleset_ini_top10:

Top10
This ruleset is a selection of analysis, with the top 10 most common. Actually, it is a little larger than that. 
_____

| [Top10]
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Classes/UnitializedProperties";
|   analyzer[] = "Classes/UnresolvedInstanceof";
|   analyzer[] = "Constants/ConstRecommended";
|   analyzer[] = "Functions/ShouldYieldWithKey";
|   analyzer[] = "Performances/ArrayMergeInLoops";
|   analyzer[] = "Performances/CsvInLoops";
|   analyzer[] = "Performances/NoConcatInLoop";
|   analyzer[] = "Performances/SubstrFirst";
|   analyzer[] = "Php/AvoidReal";
|   analyzer[] = "Php/ConcatAndAddition";
|   analyzer[] = "Php/LetterCharsLogicalFavorite";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/MissingSubpattern";
|   analyzer[] = "Structures/CouldUseStrrepeat";
|   analyzer[] = "Structures/DanglingArrayReferences";
|   analyzer[] = "Structures/FailingSubstrComparison";
|   analyzer[] = "Structures/ForWithFunctioncall";
|   analyzer[] = "Structures/NextMonthTrap";
|   analyzer[] = "Structures/NoChoice";
|   analyzer[] = "Structures/NoSubstrOne";
|   analyzer[] = "Structures/ObjectReferences";
|   analyzer[] = "Structures/QueriesInLoop";
|   analyzer[] = "Structures/RepeatedPrint";
|   analyzer[] = "Structures/StrposCompare";
|   analyzer[] = "Structures/UseListWithForeach";
|   analyzer[] = "Type/NoRealComparison";
|   analyzer[] = "Variables/VariableUsedOnce";| 






.. _ruleset_ini_typechecks:

Typechecks
This ruleset focuses on typehinting. Missing typehint, or inconsistent typehint, are reported. 
__________

| [Typechecks]
|   analyzer[] = "Classes/ChildRemoveTypehint";
|   analyzer[] = "Classes/FossilizedMethod";
|   analyzer[] = "Functions/BadTypehintRelay";
|   analyzer[] = "Functions/InsufficientTypehint";
|   analyzer[] = "Functions/MismatchTypeAndDefault";
|   analyzer[] = "Functions/MismatchedDefaultArguments";
|   analyzer[] = "Functions/MismatchedTypehint";
|   analyzer[] = "Functions/MissingTypehint";
|   analyzer[] = "Functions/NoClassAsTypehint";
|   analyzer[] = "Functions/ShouldBeTypehinted";
|   analyzer[] = "Functions/WrongArgumentType";
|   analyzer[] = "Functions/WrongTypeWithCall";
|   analyzer[] = "Interfaces/UselessInterfaces";
|   analyzer[] = "Php/NotScalarType";
|   analyzer[] = "Typehints/CouldBeCallable";
|   analyzer[] = "Typehints/CouldBeFloat";
|   analyzer[] = "Typehints/CouldBeInt";
|   analyzer[] = "Typehints/CouldBeIterable";
|   analyzer[] = "Typehints/CouldBeNull";
|   analyzer[] = "Typehints/CouldBeParent";
|   analyzer[] = "Typehints/CouldBeSelf";
|   analyzer[] = "Typehints/CouldBeString";
|   analyzer[] = "Typehints/CouldBeVoid";| 






.. _ruleset_ini_php-cs-fixable:

php-cs-fixable
[PHP-CS-fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) is a tool to automatically fix PHP Coding Standards issues. It applies modifications in the PHP code automatically. Exakat finds results which may be automatically updated with php-cs-fixer. 
______________

| [php-cs-fixable]
|   analyzer[] = "Classes/DontUnsetProperties";
|   analyzer[] = "Php/ImplodeOneArg";
|   analyzer[] = "Php/IsnullVsEqualNull";
|   analyzer[] = "Php/IssetMultipleArgs";
|   analyzer[] = "Php/LogicalInLetters";
|   analyzer[] = "Php/NewExponent";
|   analyzer[] = "Structures/CouldUseDir";
|   analyzer[] = "Structures/ElseIfElseif";
|   analyzer[] = "Structures/MultipleUnset";
|   analyzer[] = "Structures/PHP7Dirname";
|   analyzer[] = "Structures/UseConstant";| 





Exakat Changelog
----------------

Here is the changelog of exakat. 

Version 2.2.1 (Chen, coming up)
+ Architecture
    + 
+ Report
    + 
+ Analysis
    + 
+ Tokenizer
    + 

**Version 2.2.0 (Mao, 2020-10-15)**

+ Architecture
    + 
+ Report
    + 
+ Analysis
    + 
+ Tokenizer
    + 

**Version 2.1.9 (Yin, 2020-10-01)**

+ Architecture
    + Removed old and unused commands
    + Modernized usage of docker as phpexec
    + New directive php_extensions to managed list of ext
+ Report
    + Ambassador : removed 3 gremlins from typehint stats, added scalar types
    + New Migration80 report, dedicated to PHP 8.0 migrations
    + New Stubs.ini report, dedicated to exakat extensions production
+ Analysis
    + New analysis : report arguments which are not nullable because of constants.
    + New analysis : could use stringable interface
    + New analysis : suggest explode()'s third argument when applicable
    + New analysis : suggest PHP 8.0 promoted properties
    + New analysis : report arrays with negative index, and auto-indexing 
    + New analysis : report unsupported types with operators
    + New analysis : report usage of track_errors directive (PHP 8.0)
    + New analysis : report useless types on __get/__set
    + New analysis : count the number of use expressions in a file
    + New analysis : Avoid modifying typed arguments
    + New analysis : Report Assumptions in the code
    + New analysis : array_fill() usage with objects
    + New analysis : mismatch between parameter name and type
    + Updated analysis : magic methods definitions also find usage for __invoke()
    + Updated analysis : noscream operator usage may have exceptions
    + Updated analysis : identical methods and identical closures
    + Updated data : list of exceptions and their emitters
+ Tokenizer
    + Upgraded detection of extensions' structures, beyond functions

**Version 2.1.8 (Chou, 2020-09-18)**

+ Architecture
    + added '--' options, and kept the '-' options, for migration purposes. (--format and -format are both available)
    + Added support for PHP 8 attributes in dump.sqlite
    + Added 'precision' to rule docs. 
    + Moved all but one data collection from Dump -collect to Dump/ analysis. 
+ Report
    + New report : SARIF
    + Typehint suggestion report : Tick classes when they are fully covered
    + Weekly report : fix donuts display.
    + Stubsjson : Added support for PHP attributes
    + Stubs : Added support for PHP attributes
+ Analysis
    + New ruleset : CI-Checks
    + New analysis : 'Multiple declare(strict_types = 1)'
    + New analysis : 'No more (unset) in PHP 8'
    + New analysis : Cancel methods in parent : when methods should not have been abstracted in parent class.
    + New analysis : '$php_errormsg is removed in PHP 8'
    + New analysis : 'Mismatch Parameter Name' checks parameter names between inherited methods for consistency
    + Upgraded analysis : 'Useless Arguments' is accelerated
    + Upgraded analysis : 'Don't use Void' weeded out false positives
    + Upgraded analysis : 'Wrong type for native calls' weeded out false positives
    + Upgraded analysis : 'Non static methods called statically' was refactored for PHP 8.0 support
    + Upgraded analysis : 'PHP Keywords' includes 'match'
    + Upgraded analysis : 'Useless instruction' reports '$a ?? null' as useless.
    + Upgraded analysis : 'Uncaught exceptions' is extended to local variables
    + Upgraded analysis : 'Foreach favorites' also covers the keys
    + Upgraded analysis : 'Should Preprocess' skips expressions with constants
    + Upgraded analysis : 'Compare Hashes' has more functions covered
    + Removed analysis : 'Normal Properties' : no need anymore.
+ Tokenizer
    + Moved isPhp attribute to Task/Load plugin
    + Created isExt attribute to Task/Load plugin

**Version 2.1.7 (zi, 2020-09-07)**

+ Architecture
    + Refactored loading class, to keep query load at optimal size for Gremlin
    + GC during load to free memory
    + More typehints
    + Move several collections to Dump/ ruleset
+ Report
    + Upgraded Typesuggestion report with report on closures and arrow functions
    + Added Arrowfunctions in inventories
    + Added collection of arguments and details for closures and arrowfunctions
+ Analysis
    + New analysis : Could Be In Parent : suggest methods that should be defined in a parent
    + New analysis : Don't pollute namespace
    + New analysis : report insufficient return typehints
    + Upgraded analysis : 'Method signature must be compatible' now PHP 8.0 compatible
    + Upgraded analysis : 'Wrong type with native function' fixes false positives
    + Upgraded analysis : 'Same condition' added coverage for || conditions
    + Upgraded analysis : 'Missing returntype' extended to class typehints
    + Upgraded analysis : 'Should Use This' also covers special functions like get_class_called()
    + Upgraded analysis : 'No concat in loop' skips nested loops
    + Upgraded analysis : 'Always false' covers typehint usage 
    + Upgraded analysis : 'NoChoice' doesn't report large expressions
    + Upgraded analysis : 'Dont mix PlusPlus' skip () and =
    + Upgraded analysis : 'Fallthrough' don't report final cases without break
    + Checked unit tests : 3663 / 3630 test pass (99% pass)
+ Tokenizer
    + Removed 'root' property
    + Upgraded to new Attributes #[] in detection and normalisation
    + Fixed constant detection within instanceof
    + Created RETURN and RETURNED for Arrowfunctions (there is no return otherwise)
    + Parent method also calls children methods when those are not defined there
    + Support for multiple attributes in one syntax

**Version 2.1.6 (Night Patrol Deity, 2020-08-28)**

+ Architecture
    + More typehints coverage
    + Various speed-up
    + Lighter logging with gremlin
    + Fixed installation path
+ Report
    + Upgraded Typesuggestion report
    + Upgraded Stubs and Stubsjson
+ Analysis
    + New analysis : report PHP 8.0 unknown parameters
    + New analysis : overwritten methods with different argument counts
    + New analysis : Warn of iconv and TRANSLIT for portability
    + New analysis : Warn of glob and  {} for portability
    + Upgraded analysis : 'Useless check' covers new situations.
    + Upgraded analysis : 'Abstract away' now covers new calls.
    + Upgraded analysis : 'Must return Typehint' skips Void.
    + Upgraded analysis : 'Missing new' with less false positives
    + Checked unit tests : 3559 / 3630 test pass (98% pass)
+ Tokenizer
    + Support for Virtualmethod and imports from traits
    + Refactored Usenamespace atom
    + Fixed calculations of fullnspath for static::class
    + Fixed detection of null/true/false in new()
    + Added support for T_BAD_CHARACTER

**Version 2.1.5 (Day Patrol Deity, 2020-08-04)**

+ Architecture
    + Fixed comment size estimation by 1 for T_COMMENT
    + Added more typehints to code
+ Report
    + Typehint suggestions : added ticks to fully typed methods
    + Emissary : Extract more information from dump.sqlite, instead of datastore.sqlite
    + Ambassador : Added a list of parameters, defined in the application
    + Ambassador : Added a list of fossilised methods
    + Stubs : Added check around PHP native functions and CIT
    + StubsJson : Added property for PHP native structures
+ Analysis
    + New analysis : Report insufficient initialisation for array_merge() collector variable
    + New analysis : Report useless triple equals 
    + New analysis : Don't compare typed boolean return values
    + New analysis : Report wrong type used with PHP functions
    + New analysis : Suggest abstracting away some PHP native functions
    + New analysis : Report try block that are too large
    + New analysis : Report variables potentially undefined in catch clause
    + New analysis : Report swapped arguments in methods overwriting
    + Upgraded analysis : InvalidPackFormat speed up
    + Upgraded analysis : Added parameter to Security/ShouldUsePreparedStatement to choose the preparing method
    + Upgraded analysis : Added parameter to Security/HardcodedPasswords to choose the name of properties/index
    + Upgraded analysis : PHP 8.0 new scalar typehint, stringable interface
+ Tokenizer
    + Added support for named parameters (PHP 8.0)
    + Trimmed some properties from atoms
    + Removed non-existent atom mentions
    + Added support for Attributes (WIP)
    + Added support for ?-> 
    + Added support for new T_*_NAME tokens

**Version 2.1.4 (Marshal of Heavenly Blessing, 2020-07-23)**

+ Architecture
    + Added time of last commit in audit results
    + Added more typehints
    + Upgraded PHP native method description with typehints (WIP)
+ Report
    + Typehint suggestion report
    + New toplogies : call order, 
    + Ambassador : new statistics for typehint usage
+ Analysis
    + New analysis : Report double assignation of objects
    + New analysis : Typehints/CouldBe*, which makes suggestions for typehints
    + New analysis : Checks for argument type when typehint is present in custom methods
    + Upgraded analysis : Too Many Finds may be configured for threshold and prefix/suffix
    + Upgraded analysis : Typehints stats were extended to properties and multiple typehints
    + Upgraded analysis : Global outside Loop is extended to static variable too
    + Upgraded analysis : ErrorMessages also detect local variable contents
    + Upgraded analysis : Speed up for NullBoolean, Interfaces IsNotImplemented, InvalidPackFormat, arrayIndex, noWeakCrypto
    + Checked unit tests : 3532 / 3496 test pass (99% pass)
+ Tokenizer
    + Removed 'aliased' property in atoms
    + Fixed spotting of PHP native constants, when in Define() structure
    + Fixed loading of false values
    + Added support for the trailing comma in closure's use expression
    + more handling of phpdocs
    + Null is now reused when it is a default value, as a typehint. 
    + Logical was split in two : Logical and Bitoperation
    + Added support for match() {} expression
    + Fixed boolean calculations during Load
    + Removed auto-referencing in DEFAULT calculations

**Version 2.1.3 (Marshal of the Heavenly Canopy, 2020-07-02)**

+ Architecture
    + Removed all usage of datastore in Reports, and only rely on dump.
    + ignore_rules is now case insensitive
    + Moved some of the loading to a separate gremlin call to reduce the size of node load.
    + Fixed the branch option with Git calls.
    + Storing trait's use expresion's options.
+ Report
    + Ambassador ; New inventory : PHP protocol used (php, phar, glob://...)
    + Stubs and StubsJson, have been tested extensively
+ Analysis
    + New analysis : report double assignations of the same object ($a = $b = new C)
    + New analysis : report cyclic references
    + Upgraded analysis : Used Constants edge situations
    + Upgraded analysis : No real comparison : extended analysis to constants
    + Upgraded analysis : extended detection of dynamic method calls to call_user_func*
    + Upgraded analysis : paths are detected with new functions
    + Checked unit tests : 3490 / 3520 test pass (99% pass)
+ Tokenizer
    + More phpdoc support (from code to report)
    + Added isPHP to absolute FQN notations

**Version 2.1.2 (Mountain Deity, 2020-06-25)**

+ Architecture
    + Removed files task from initproject.
    + Added ignore_rule directive, to ignore specific rules while running a specific report
    + More documentation (in particular, modifications section)
    + Exakat avoids to return twice the same results (file and line)
    + Sped up some analysis, and added a time limit per analysis
    + Removed double linking for static variables
+ Report
    + New reports ; Stubs and StubsJson, which produce the stubs of the audited code (PHP and JSON format) (WIP)
    + New report ; Typehint suggestion (WIP)
    + Ambassador ; offers the configuration for all the rules that spotted issues in the current audit, for reuse in other codes
    + Collect the number of property per class
+ Analysis
    + New analysis : Report methods that are too much indented on average
    + New analysis : Report possible confusion between a class and an alias
    + New analysis : Report variables that are static and global at the same time
    + New analysis : Report statement with long blocks
    + New analysis : Report phpdoc's deprecated methods and function calls
    + Upgraded analysis : Dereferencing levels now include () and = 
    + Upgraded analysis : Unused Methods now skips classes that calls themselves dynamically 
    + Upgraded analysis : No Need Get_class() was refactored
    + Upgraded analysis : Avoid Optional Properties was refactored
    + Upgraded analysis : Variable inconsistent Usage was extended with more reach
    + Upgraded analysis : Indirect Injections was upgraded with better reach with variables
    + Upgraded analysis : Direct Injections was upgraded with include
    + Upgraded analysis : PHP 8.0 new scalar typehint, stringable interface
    + Upgraded analysis : Mismatch Type and default now avoids undefined constants
    + Upgraded analysis : Wrong Optional Parameter is upgraded for PHP 8.0
    + Upgraded analysis : Indentation level was refactored
    + Checked unit tests : 3480 / 3510 test pass (99% pass)
+ Tokenizer
    + Upgraded detection of PHP native constants, when they are in absolute notation
    + Dump task stores use expressions' options, plus minor fixes
    + Added support for Attributes (PHP 8.0)
    + Added support for Union types (PHP 8.0)
    + AtomIs step (WITH_VARIABLE) was extended with local variables
    + DEFAULT doesn't point anymore on auto-updated values
    + Extended support for phpdoc in the code
    + Added support for promoted properties (PHP 8.0)

**Version 2.1.1 (Earth Deity, 2020-06-01)**

+ Architecture
    + Using timeLimit() to prevent Gremlin from running too deep in the rabbit hole
    + Added Neo4j Graphson V3 Graph driver
    + Moved 'Dump' rules to a specific Ruleset for easier administration
    + Propagated the upgrade to PHP 8.0 union types to three more rules
    + Fixed access to the list of ignored files
    + Added support for explicit stub files
    + Fixed multiple calls to Dump (better reentrant)
+ Report
    + New report : Meters, which holds measures for the audited code.
    + Ambassador : inventory of OpenSSL ciphers
+ Analysis
    + New analysis : Report unused traits
    + New analysis : Report chmod 777 system calls
    + New analysis : Check for keylength when generated by PHP
    + New analysis : Report methods with prefix/suffix and expected typehint
    + New analysis : Mark classes when they call dynamically their own methods
    + New analysis : Check for constants hidden in variable names ${X} != $X;
    + New analysis : Throw will be an expression in PHP 8.0
    + Upgraded analysis : Dangling operator now checks for loops too
    + Upgraded analysis : 'Variables used once' now skips variable definitions
    + Upgraded analysis : 'Access Private' takes into account dynamic classes
    + Upgraded analysis : 'Could Centralize' now uses a custom threshold. Default is 8 usage of an expression to centralize.
    + Upgraded analysis : 'Return true/false' checks that they are alone in the blocks
    + Upgraded analysis : 'Unreachable code' checks on constants values before reporting the next expression
    + Upgraded analysis : 'Magic methods' are case insensitive
    + Upgraded analysis : 'No Hardcoded passwords' has new functions that require a password
    + Upgraded analysis : 'Unused methods' are omitted for dynamically called methods and overwritten methods
    + Upgraded analysis : Insufficient Property Typehint also works for untyped properties
    + Upgraded analysis : PHP 8.0 new scalar typehint, stringable interface
    + Checked unit tests : 3383 / 3444 test pass (98% pass)
+ Tokenizer
    + Arguments with null as default values, automatically are nullable
    + Intval is also an integer for logical operations
    + Default Values now omits recursives assignations
    + Fixed fullnspath for PHP short tags
    + Added link between new command and constructor of anonymous classes.

**Version 2.1.0 (City God, 2020-05-13)**

+ Architecture
    + results stored in HashResults are now testable
    + Moved all query methods to Query/DSL namespace, from Analyzer class
+ Report
    + New report : ClassReview, with focus on classes structures
    + New report : Typechecks, with focus on type hint usage
    + Ambassador : Added typehint stats section
    + Ambassador : fixed display of classes name in classes tree
    + Ambassador : some missing sections have been rehabilitated
+ Analysis
    + New analysis : Trailing comma in signature (PHP 8.0)
    + New analysis : Hidden nullable types
    + New analysis : Not implemented abstract methods
    + New analysis : Report confusion between variables and arguments with arrow functions
    + Upgraded analysis : No literal for reference was extended 
    + Upgraded analysis : Add zero is extended to constants
    + Upgraded analysis : This is for classes is now valid with arrow functions
    + Upgraded analysis : Useless arguments takes also into account constants
    + Upgraded analysis : Wrong Type With Call supports variadic arguments
    + Upgraded analysis : Extension constants now support fully qualified names
    + Upgraded analysis : Bad Typehint relay is compatible with union types
    + Upgraded analysis : Multiple Identical Cases now handles constants too
    + Checked unit tests : 3437 / 3477 test pass (99% pass)
+ Tokenizer
    + Restored 'List' atom
    + Interface methods are now 'abstract' by default
    + Added 'array' typehint for variadic arguments
    + Distinguish between argument and local variable in fn functions
    + Removed nullable property
    + propagate calls now propagates closures and arrow functions
    + Added support for union types (PHP 8.0)
    + Check all error messages from php, not just the first ones

**Version 2.0.9 (Jialan, 2020-04-30)**

+ Architecture
    + Added option in TU for analysis that won't fill the result table.
    + Reduced the number of duplicate links in the graph
    + Upgraded tokens for PHP 8.0. 
+ Analysis
    + New analysis : Don't collect void
    + New analysis : Wrongly inited properties
    + New analysis : Not inited properties
    + Upgraded analysis : PHP 8.0 removed functions
    + Upgraded analysis : Useless instructions also include global/static variables
    + Upgraded analysis : Bad Relay Function now works with return types and property types
    + Upgraded analysis : 'Scalar or object properties' are upgraded with static calls
    + Removed analysis : Classes and Arrays IsRead and IsModified. Use properties now.
    + Checked unit tests : 3347 / 3420 test pass (97% pass)
+ Tokenizer
    + Fixed edge case for xor, with intval
    + Refactored multiple calculation for cast values
    + Added support for links between constants and use expressions
    + Linked classes with calls, when using use expression

**Version 2.0.8 (Ao Run, 2020-04-20)**

+ Architecture
    + Added new information in dump.sqlite, to make report autonomous
+ Analysis
    + Upgraded analysis : Paths are also recognized with constants, and more functions
    + Upgraded analysis : Should Use single Quotes
    + Checked unit tests : 3328 / 3398 test pass (97% pass)
+ Tokenizer
    + Fixed detection of PHP constants

**Version 2.0.7 (Ao Shun, 2020-04-14)**

+ Architecture
    + Adopted strict_types
    + Removed ctype1 attribute
    + Moved linting into separate processes
    + Refactored analysis to export to dump via SQL
    + Added 'None' ruleset to Dump task
+ Report
    + Ambassador : Added Constant's order report
    + None : Added support for No report
+ Analysis
    + Upgraded analysis : Undefined class constants
    + Upgraded analysis : Undefined global constants
    + Upgraded analysis : Undefined property
    + Checked unit tests : 3347 / 3420 test pass (97% pass)
+ Tokenizer
    + Support PHP 8.0's tokens
    + Added support for multiple typehint in the engine
    + Fixed edge case for boolean type casting

**Version 2.0.6 (Ao Qin, 2020-03-04)**

+ Architecture
    + Refactored analysis types for first UT
    + Moving to PHP 7.4 by default
+ Report
    + Rector : added more coverage
    + All : better display of typed properties
+ Analysis
    + New analysis : Semantic names of arguments
    + New analysis : !$a == $b
    + New prototype : possibles interfaces
    + Upgraded analysis : Overwritten literals now skips .=
    + Upgraded analysis : Scalar or object handles return type
    + Checked unit tests : 3322 / 3420 test pass (97% pass)

**Version 2.0.5 (Ao Guang, 2019-11-25)**

+ Architecture
    + Fixed access to severity and timetofix from compiled extension
+ Report
    + Ambassador : Fixed links to documentation
+ Analysis
    + Upgraded analysis : Mismatched Type and Default now omit undefined constants
    + Checked unit tests : 3366 / 3402 test pass (99% pass)

**Version 2.0.4 (Army Defeating Star of Heaven's Gate, 2019-11-18)**

+ Architecture
    + Reducing Analyzer's class method count
    + Moving more collections to Dump/ and Complete/
+ Report
    + Rector : added more coverage
    + Ambassador : Skiped analysis are now reported, not with -1
    + Ambassador : Foreach favorites's graph is displayed
    + Ambassador : Visibility suggestion has full method names
+ Analysis
    + Upgraded analysis : Don't Mix ++ now skips $a[$b++]
    + Upgraded analysis : Type hint stats skips some return values
    + Checked unit tests : 3365 / 3401 test pass (99% pass)

**Version 2.0.3 (Military Star of the North Pole, 2019-11-11)**

+ Architecture
    + Added check on xdebug presence (nesting limit)
    + Moving more collections to Dump/
+ Analysis
    + New analysis : Nullable typehint requires a test on NULL
    + New analysis : Typehint that requires too much
    + Upgraded analysis : Printf check on arguments works with '.'
    + Upgraded analysis : No magic for arrays skips __get()
    + Upgraded analysis : Const recommended, but not when methods are used
    + Upgraded analysis : Written only variables handles compact()
    + Upgraded analysis : Callbacks need returns, but not for spl_autoload_register()
    + Upgraded analysis : Extended analysis to Concatenation an Heredoc for Email
    + Upgraded analysis : Disconnected classes handles case sensitivity
    + Checked unit tests : 3371 / 3397 test pass (99% pass)

**Version 2.0.2 (Danyuan Star of Honesty and Chasity, 2019-11-04)**

+ Architecture
    + Adding more typehint
    + Created new class to build Dot files
    + Cleaned double examples
    + Dump handles multiple definitions for constants, class, trait, functions.
+ Report
    + Added new Topology report
    + Added new Type hint topology sort
    + Stubs : added class constant visibility
+ Analysis
    + New analysis : Report argument whose name clashes with typehint
    + New analysis : Report properties that are insufficiently typed
    + Moved 'Inclusions' to Dump/
    + Added steps to find original and relayed arguments
+ Tokenizer
    + Fixed paralellisation bug in Load

**Version 2.0.1 (Military Star of the North Pole, 2019-10-28)**

+ Architecture
    + Added more return type
    + Centralized reading for ini or json
+ Report
    + Ambassador: fixed Foreach favorites
    + Ambassador: added sort to number of parameter list
    + Checked unit tests : 3345 / 3377 test pass (99% pass)
+ Analysis
    + Upgraded xmlwriter to json

**Version 2.0.0 (Civil Star of Mystery and Darkness, 2019-10-21)**

+ Architecture
    + Manual file/line fixes
    + More simplifcations in load step
+ Report
    + Ambassador : fixed performance display
    + Ambassador : report list of shell commands
    + Typehint4all : first report
    + Perfile : fixed sorting
+ Analysis
    + New analysis : Report possible typehint for bool, int, string, array. WIP
    + Upgraded analysis : common alternatives are extended to switch and elsif
    + Upgraded analysis : xmlreader description includes class constants, properties and methods.
    + Upgraded analysis : callback needs return, is extended to php native functions
    + Checked unit tests : 3345 / 3377 test pass (99% pass)

**Version 1.9.9 (Lasting Prosperity Star of True Man, 2019-10-14)**

+ Architecture
    + Documentation review
+ Report
    + New reports : Stubs, Rector
    + Typehint stats
    + Stubs takes into account use expression
    + Added Concrete5 and Typo3 as vendors
+ Analysis
    + New analysis : checks on is_a third argument
    + New analysis : Invalid mbstring encodings
    + New analysis : Weird Index in arrays
    + New analysis : Avoid FILTER_SANITIZE_MAGIC_QUOTES
    + New analysis : Don't forget third argument
    + New analysis : Hard to update methods
    + New analysis : Merge two ifthen into one
    + New analysis : Report wrong type with calls
    + New analysis : Check case for namespaces
    + Updated analysis : Undefined interfaces now includes interfaces extensions
    + Updated analysis : Report more wrong types with return type 
    + Updated analysis : Register globals also applied to class
    + Updated analysis : Could Use Try covers more new, functions and static calls
    + Updated analysis : Useless Cast also reports (string) array (always Array)
    + Checked unit tests : 3343 / 3366 test pass (99% pass)
+ Tokenizer
    + Create default values for foreach
    + Load captures empty files, and omit them
    + Create default values also handles ??=

**Version 1.9.8 (Giant Gate Star of Dark Essence, 2019-10-07)**

+ Architecture
    + Upgraded dump command to handle multiple -P
    + .yaml configuration handles multiple reports
    + Started journey to strict_types
    + Code cleaning
+ Report
    + Ambassador : Fixed report of Flexible Docs
    + Ambassador : trimmed delimiters in inventories
    + Inventory : Foreach, with key values
+ Analysis
    + New analysis : Wrong case for functions
    + New analysis : Parameter Hiding
    + New analysis : Report usage of Traversable
    + Updated analysis : Undeclared properties skips undefined properties
    + Updated analysis : Useless Interface, modernized query
    + Updated analysis : String Holding Variables now skips default, const, sprintf
    + Updated analysis : Binaries are not confused with hex
    + Updated analysis : Extended 'Insufficient typehint' to abstract classes
    + Checked unit tests : 3324 / 3343 test pass (99% pass)
+ Tokenizer
    + Fixed handling of large powers
    + Added more escaping when storing to SQLITE

**Version 1.9.7 (Greedy Wolf Star of Sunlight, 2019-09-30)**

+ Architecture
    + Added support for analysis reporting missing values in a reference list
    + Fixe batch dumping of results
+ Report
    + Ambassador : new inventory : dereferencing levels
+ Analysis
    + New analysis : Use PHP Native URL parsing functions
    + New analysis : Maximum dereferencing level
    + New analysis : Use case value in a switch : it was already tested
    + Updated analysis : No class as typehint accepts abstract classes
    + Updated analysis : Create Magic Property reachs out to traits
    + Updated analysis : Security also reports usage of unserialize()
    + Updated analysis : Mistmatched default argument also covers methods
    + Updated analysis : Never used parameter also covers methods
    + Updated analysis : Unused global also cover static variables
    + Updated analysis : Duplicate strings threshold is not 15, not 5.
    + Checked unit tests : 3289 / 3319 test pass (99% pass)
+ Tokenizer
    + RETURNTYPE, TYPEHINT, and DEFAUT are not always on, with Void atom, or better.
    + DEFAULT value targets end-values, skips ??, ?:, () and =.
    + Exceptions now reports errors in the Query, not where it is thrown

**Version 1.9.6 (Star of Birth, 2019-09-23)**

+ Architecture
    + Moved new elements to Complete/
    + Moved new elements to Dump/
    + Initial configuration of project now includes analysis parameters with default
    + Added descriptions to Rulesets
    + New command Config : displays current configuration for reuse and editing
    + Upgraded Doctor : support for docker-php, in-code 
+ Report
    + Ambassador : removed {} on magic property inventory
    + Ambassador : new inventory of network protocols used (udp://, ssh2://...)
+ Analysis
    + New analysis : avoid mb_string inside loops
    + New analysis : avoid SSLvx and TLSv1.0
    + New analysis : report duplicate literal in the code, with parameter
    + New analysis : warn about null property
    + New coverage : calls to __call and __callStatic
    + Updated coverage : expressions with parenthesis
    + Updated coverage : default values are now targeting the final value in multiple assignations.
    + Updated analysis : Strange Variable name skips Staticdefinition and its default value 
    + Updated analysis : Useless instructions are upgrade with pure functions
    + Updated analysis : Extended Closure2string with Arrowfunctions
    + Updated analysis : Extended 'Could be local variable' to traits
    + Updated analysis : Unused Global also covers static variables
    + Checked unit tests : 3279 / 3304 test pass (99% pass)
+ Tokenizer
    + Updated tokens for PHP 7.4

**Version 1.9.5 (Star of Adversity, 2019-09-16)**

+ Architecture
    + Added count property to Analysis node, stepstone for Diff analysis
    + Added support for 'optional' step 
    + Added support for 'interfaces' as typehint for remote definitions
    + Removed more true/false values
    + Fixed strtolower with mb_strtolower in Dump
+ Report
    + Added several PHP error messages 
    + Ambassador : added inventory of magic properties
    + Ambassador : added inventory of typehints for methods (WIP)
    + Added support for function/closure/argument arguments
    + Added support for function/closure/argument arguments
+ Analysis
    + New analysis : No literal value as referenced argument
    + New analysis : use array_slice or array_splice
    + New analysis : Useless typechecks with Typehint
    + New analysis : Report non-implemented interfaces
    + New analysis : Incompatible Signatures with Self (PHP 7.4+)
    + New analysis : Report wrong expectations from interfaces
    + Upgraded analysis : Excluded __construct and __destruct from Magic Methods
    + Upgraded analysis : Concat and Addition : Now also for bitshift
    + Upgraded analysis : Incompatible Signatures with Self (PHP 7.3)
    + Upgraded analysis : Elseif and Sequences are omitted in Level analysis
+ Tokenizer
    + Upgraded support for magic properties

**Version 1.9.4 (Star of Benefit, 2019-09-09)**

+ Architecture
    + Dump avoid storing multiple definition for the same class
    + Added more native return definitions
    + Adding UT for Complete/
    + Dump inventories are being moved to analysis class
    + Moving more Themes => rulesets
+ Report
    + Ambassador : Fixed several internal links
    + Ambassador : Displays the levels of nesting in the code
    + Ambassador : Upgraded compatibility report with PHP 7.4
    + New report : Stubs
+ Analysis
    + New analysis : PHP 7.4 New Directives
    + New analysis : Too many dimensions with array
    + New analysis : Check concat and coalesce precedence
    + New analysis : Adopt explode() third argument
    + New analysis : Ternary and useless assignation
    + New analysis : Nested ternary without parenthesis
    + New analysis : Spread operator with arrays
    + New analysis : Max level of indentation 
    + New analysis : Use Arrowfunctions
    + Upgraded analysis : Clone with non object handles containers
    + Upgraded analysis : Calling non-static methods statically
    + Upgraded analysis : Unresolved Instanceof
    + Upgraded analysis : Array_merge and variadic, extended to isset
    + Checked unit tests : 3234 / 3259 test pass (99% pass)
+ Tokenizer
    + Last element of list() is not omitted anymore

**Version 1.9.3 (Star of Longevity, 2019-09-02)**

+ Architecture
    + Created new Complete category, with data complement for analysis
    + Refactored constant propagation
    + Made code compatible with PHP 7.4
    + Rename project_themas to project_rulesets
    + Added support of -p with .exakat.yaml
+ Report
    + Ambassador : reworked presentation for visibility suggestions
+ Analysis
    + New analysis : report covariance and contravariance for compatibility
    + New analysis : no spread operator for hash values
    + New analysis : self-closing tags are omitted by strip_tags
    + New analysis : report Openssl_random_pseudo_byte second argument usage
    + New analysis : CURLPIPE_HTTP1 is obsolete
    + New analysis : removed PHP 7.4 directives
    + New analysis : do not use ... with array_merge without checks
    + Updated analysis : added crc32c as hash algorithm
    + Removed analysis : Removed Curly Arrays (double take)
    + Checked unit tests : 3219 / 3240 test pass (99% pass)
+ Tokenizer
    + Extended OVERWRITE to Interfaces
    + Extended support for class_alias()

**Version 1.9.2 (Star of Prosperity, 2019-08-26)**

+ Architecture
    + Introduced a new set of analysis : Complete
    + Cleaned code for PHP 7.4 usage
    + Refactored Query to skip impossible Gremlin calls
    + Now using Project for project names
+ Report
    + New report : classes dependencies (HTML version)
    + New report : files dependencies (HTML and DOT version)
    + Ambassador : datas -> data
+ Analysis
    + New analysis : {} are deprecated in PHP 7.4
    + New analysis : Don't use ENT_IGNORE
    + New analysis : fn is a PHP 7.4 keyword
    + Updated analysis : Functions/UseConstantAsArguments covers also password_hash()
    + Updated analysis : printf arguments now handles positional formatters
    + Checked unit tests : 3172 / 3199 test pass (99% pass)
+ Tokenizer
    + Fixed precedence for left associativity

**Version 1.9.1 (Star of Life, 2019-08-19)**

+ Architecture
    + Fixed zip as code source
+ Report
    + Ambassador : Fixed issues list for Favorites
    + Owasp : switched dashboards
+ Analysis
    + Updated analysis : Loop Calling got one extra check
    + Checked unit tests : 3148 / 3187 test pass (99% pass)

**Version 1.9.0 (Ming Wenzhang of Jiayin, 2019-07-29)**

+ Architecture
    + Added missing configuration file for tinkergraph 3.4
    + Upgraded support for running exakat with PHP 7.4
+ Analysis
    + New analysis : array_key_exists() now report object usage
    + New analysis : report mb_strrpos 4th argument
    + New analysis : Reflection export are deprecated
    + New analysis : Report classes without parents but with 'parent'
    + New analysis : Don't use scalar as arrays
    + New analysis : Report use of PHP 7.4 serialize method
    + Updated analysis : Multiple Identical Keys checks for undefined keys first
    + Updated analysis : Dont be too manual : extended to catch clauses
    + Updated analysis : setcookie detection anchors the keyword at the beginning of the string
    + Updated analysis : Failed Substr comparison now works with constants
    + Updated analysis : Added support for continue 2 and 3
    + Checked unit tests : 3147 / 3186 test pass (99% pass)
+ Tokenizer
    + Added support for __serialize and __unserialize
    + Added support for numeric literal separator
    + Skip entirely unparsable files

**Version 1.8.9 (Meng Feiqing of Jiachen, 2019-07-22)**

+ Architecture
    + Check on graphdb configuration : default to nogremlin
    + Added support for baseline for project and report
    + Moved more doc to ruleset
    + Check on .git folder for update
    + Added -version option for upgrade command
    + Doctor honors .exakat.yml file
+ Analysis
    + New analysis : Report useless type of checks
    + New analysis : Disconnected classes 
    + New analysis : Avoid using mb_detect_encoding()
    + New analysis : Check that source and blind variables are different in foreach
    + New analysis : ~ or ! favorite
    + Updated analysis : Is Zero omits multiplications
    + Updated analysis : Used Private Property is upgraded
    + Updated analysis : Multiple Identical Keys : refactored
    + Updated analysis : Undefined variables now skips extract, include, eval
    + Checked unit tests : 3147 / 3166 test pass (99% pass)
+ Tokenizer
    + Refactored support for Foreach : each blind variable is in VALUE
    + Upgraded precedence for ! (not)
    + Propagate constants with assignations
    + Fixed link to $this inside heredoc and co
    + Fixed an edgecase where Static method call was confused with Newcall

**Version 1.8.8 (Wei Yuqing of Jiawu, 2019-07-15)**

+ Architecture
    + Modernized tinkergraph support
    + When pcntl is available, stubs are produced in a child process
    + Removed duplicated methods
    + Exported sequences to helpers
    + More UT libraries are supported
    + Federated BUSYTIMEOUT in constant
+ Report
    + Ambassador and all dependend reports were refactored : menu is configurable with Yaml
    + Emissary is the upcoming configurable report. 
+ Analysis
    + New step : Load data from code
    + New analysis : Variables used for setting aside value temporarily
    + New analysis : Use PHP array_ functions, instead of loops
    + Updated analysis : Unused methods now skips methods from PHP native interfaces (Arrayaccess)
    + Updated analysis : No class for typehint is now omitting PHP and extensions classes
    + Updated analysis : Switch to Switch applies to comparisons now
    + Updated analysis : Close namingg was sped up significantly
    + Updated analysis : array_column() suggestion was refined
    + Updated analysis : Htmlentities parameters also support some parenthesis usage
    + Updated analysis : Constant Scalar Expression only target specified expressions
    + Updated analysis : Static Properties skip Virtual properties
    + Checked unit tests : 3131 / 3155 test pass (99% pass)
+ Tokenizer
    + Refactored support for Exit and Die
    + Added raw support for phpdoc

**Version 1.8.7 (Hu Wenchang of Jiashen, 2019-07-08)**

+ Architecture
    + Added bugs fixes up to 7.3.7
    + New factory method for the graph
+ Analysis
    + New analysis : Backward compatible check on generators (can't return)
    + New analysis : Report wrong return typehint
    + New analysis : Use DateTimeImmutable
    + New concept : Methods that throw errors 
    + Updated analysis : Recursive functions disambiguate methods
    + Updated analysis : Refactored property/variable confusion
    + Updated analysis : Could typehint checks on type validations
    + Updated analysis : Variable used once check for abstract methods
    + Updated analysis : Array_merge in loops omits file_put_contents()
    + Updated analysis : Simple Regex covers all special sequences, and unicode sequences
    + Checked unit tests : 3131 / 3142 test pass (99% pass)
+ Tokenizer
    + Differentiated support for self and static in calls
    + Moved Symfony support to its extension
    + Reworked loading to make it parallels. 

**Version 1.8.6 (Wei Yuqing of Jiawu, 2019-07-01)**

+ Architecture
    + Added support for Tinkegraph 3.4
    + Extended support for Dev 
    + Renamed Themes to Ruleset (WIP)
    + Split several long running queries into smaller chunks
    + Cached files to memory, write them once only
    + Optimized sides queries : omitting them when possible
    + Added count of issues in Analyse node
    + Optimized loading by grouping by inV
    + More coverage for Arrowfunction
+ Report
    + Dump : collect PHP cyclomatic complexity
+ Analysis
    + New analysis : Dependant abstract classes
    + New analysis : Don't use Null or Boolean as an array
    + New analysis : Infinite recursion
    + Updated analysis : Raised levels 
    + Updated analysis : Method signature must be compatible
    + Updated analysis : Access Private in Trait is OK
    + Updated analysis : Recursive function 
    + Checked unit tests : 3099 / 3105 test pass (99% pass)
+ Tokenizer
    + Upgraded support for 'Modules'

**Version 1.8.5 (Zhan Zijiang of Jiaxu, 2019-06-24)**

+ Architecture
    + Fixed several bugs in the online documentation
    + Started removing analysis, replacing with analysis
    + Fixed path in docker PHP usage.
+ Report
    + Ambassador : Export full INI and YAML config to replicate audit
+ Analysis
    + New analysis : Unused class constants
    + New analysis : Could Use available Trait
    + New analysis : literal that Could Be Constant 
    + Updated analysis : Access Private in Trait is OK
    + Updated analysis : multiple identical argument is extended to closures, methods
    + Updated analysis : ext/rdkafka
    + Updated analysis : No Hardcoded Hash is accelerated
    + Updated analysis : Extended printf() check to constants
    + Updated analysis : Optimized 'redefined method'
    + Updated analysis : Memoize Magic Call
    + Updated analysis : set_locale requires constants
    + Checked unit tests : 3099 / 3105 test pass (99% pass)
+ Tokenizer
    + Added missing isModified to Foreach keys
    + Class Method Definition handles old style constructor
    + strict_types don't yield a block
    + Added typed values for magic constants
    + Refactored new -> constructor link for Self, Static, parent
    + Added missing arguments count to Newcall
    
**Version 1.8.4 (Wang Wenqing of Jiazi, 2019-06-17)**

+ Architecture
    + Added support for PHP in docker images for compilation tests
    + First prototype for Gremlin in a specific docker image 
+ Report
    + Ambassador : restored original URL
    + Replaced 'Complexity' => 'Time To Fix'
    + Replaced 'Receipt' => Ruleset
+ Analysis
    + New analysis : regex with arrays
    + New analysis : Complex property names
    + New analysis : array_key_exists speed up
    + New analysis : curl_version forbidden argument
    + New analysis : PHP 7.4 new functions, classes and constants
    + Fixed analysis : Long Variable
    + Updated analysis : printf() format check extended to constants
    + Updated analysis : Written only variables is extended to static and global
    + Updated analysis : refactored 'Make default' 
    + Updated analysis : 'Wrong number of arguments' is extended to methods
    + Updated analysis : 'Use coalesce' checks for
    + Updated analysis : Refactored 'Nested ifthen' to have a parameter
    + Updated analysis : Extended 'Class Usage' to return typehint
    + Updated analysis : Sped up 'Used Classes'
    + Checked unit tests : 2993 / 3071 test pass (97% pass)
+ Tokenizer
    + Upgraded handling of declare with strict_types
    + Support for magic properties across classes and traits
    + Added support for parent with properties
    + Properties are handled with static and normal at the same time
    + Fixed virtualproperties with static keyword (self and parent are ok)
    + Added argument count for 'new A', without parenthesis
    + Restored old break behavior for PHP 5 and older.

**Version 1.8.3 (Jade Man of Yang, 2019-06-10)**

+ Architecture
    + Extension docs show version numbers
    + Manual uses internal links
+ Report
    + New report : SARB
    + Updated report : Ambassador list number of arguments in natural order
+ Analysis
    + New analysis : from substr() to trim()
    + New analysis : suggest making magic property a concrete one (2 ways)
    + New analysis : no array auto-append
    + Updated analysis : 'Scalar or object property' refactored
    + Updated analysis : 'Multiple identical keys' get a new check on intval, broadened to constants
    + Updated analysis : 'Indirect injection' accelerated
    + Updated analysis : 'Could be class constant' accelerated
    + Updated analysis : 'Never used property' refactored
    + Updated analysis : 'Modern empty' modernized and broadened
    + Updated analysis : 'Useless check' skips isset/empty as they may be useful
    + Updated analysis : 'Identical methoods' skips abstract methods
    + Updated analysis : 'No Count Zero' also uses sizeof(), skips switch()
    + Checked unit tests : 2993 / 3071 test pass (97% pass)
+ Tokenizer
    + Upgraded local definitions for properties to Load phase
    + Handle static keyword in closures
    + Moved 'Real' to 'Float' 
    + Created 'Scalartypehint' atom
    + Fixed intval, boolval for \true and \false

**Version 1.8.2 (Zhao Ziyu of Dingchou, 2019-06-03)**

+ Architecture
    + Refactored 'Update' command, to VCS
    + Collect missing definitions counts
    + Report handles a list of analysis names
+ Analysis
    + New analysis : No Need To Get_Class
    + New analysis : Report identical inherited methods
    + New analysis : Function returning -1 in case of error
    + Updated analysis : TypeHint must be returned, doesn't apply to abstract methods or interface methods
    + Updated analysis : 'Could Use Interface' also checks for static and visibility
    + Updated analysis : 'Concat empty' skips variables
    + Checked unit tests : 3024 / 3048 test pass (99% pass)
+ Tokenizer
    + Created 'virtual' properties, for limiting children agglomerations
    + Fixed normalized code for use traits
    + Added DEFAULT to all variable definitions
    + Connect strings to class definitions
    + Handle variable in 'compact', when they are static

**Version 1.8.1 (Zhang Wentong of Dinghai, 2019-05-27)**

+ Architecture
    + Fixed Symlink destination
    + Added collecting classes children, traits and interfaces counts
    + Added support for constants and functions in modules
    + Added missing functions in data
+ Report
    + New report : exakatYaml, which help configuring exakat
    + New report : Yaml
    + New report : Top10
    + Updated report : Json, text and xml get 'fullcode'
+ Analysis
    + Updated analysis : Should use self is extended to parent classes
    + Updated analysis : Should use prepared statement now skips some SQL queries
    + Checked unit tests : 3024 / 3048 test pass (99% pass)

**Version 1.8.0 (Zang Wengong of Dingyou, 2019-05-20)**

+ Architecture
    + Added missing native PHP functions
    + Restored anchor for ignore_dirs[] configuration
    + Removed more MAX_LOOPING usage
+ Report
    + Ambassador : removed { & @ } artefacts from globals
+ Analysis
    + New analysis : Function returning -1 in case of error
    + New analysis : Report PHP 7.4 unpacking inside array
    + New analysis : Report PHP 7.4 new functions and fn
    + New analysis : Useless arguments
    + New analysis : Addition and concatenation precedence for PHP 7.4
    + New analysis : report concatenation of empty strings
    + New analysis : casting has precedence over ternary
    + New analysis : report already used traits
    + New analysis : report missing traits in use expression
    + Updated analysis : isset on whole arrays : extended analysis to Phpvariables
    + Updated analysis : SQLITE3 requires single quotes
    + Updated analysis : Dir then slash : extended to constants
    + Updated analysis : Variable Strange Name extended to strange types
    + Updated analysis : Possible interface's analysis is sped up
    + Checked unit tests : 3021 / 3045 test pass (99% pass)
+ Tokenizer
    + Fixed fullcode of Usetrait
    + Extended method definitions to traits
    + Extended fluent interface detection to parents
    + Fixed dump for visibility change
    + Handle method aliases in use expression (as)
    + Better noDelimiter for double quotes strings

**Version 1.7.9 (Shi Shutong of Dingwei, 2019-05-13)**

+ Architecture
    + Upgraded list of functions by extension : openssl, math, hrtime
    + Added global atom to track all globals
    + Rewrote several Dump queries with DSL
    + Added support for Notice in Phpexec
    + Added support for .exakat.ini and .exakat.yaml
    + Added support for arrow functions : fn => 
    + Added support for spread operator in arrays [...[1,2,3]]
+ Report
    + Inventories : added 'inclusions' and 'global variables'
    + Ambassador : added global variables
+ Analysis
    + New analysis : support for ext/ffi, uuid
    + Updated analysis : Nested Ternary handles parenthesis
    + Updated analysis : Static loops is extended to references and arrays
    + Updated analysis : Recursive function is extended to Magic methods and Closures
    + Checked unit tests : 3014 / 3019 test pass (99% pass)
+ Tokenizer
    + Moved 'is_in_ignored_dir' to a property
    + Cleaned getFullnspath() call in Load
    + Fixed latent bug on Function fullnspath
    + Heredoc and Nowdoc are reported as constant if needed
    + Isset() is not read
    + Ignore PHP notices when linting
    + Globals are now centralised across a repository
    + Extended definitions for Virtualproperties
    + Removed double DEFINITION link with new

**Version 1.7.8 (Cui Juqing of Dingyi, 2019-05-06)**

+ Architecture
    + renamed test.php to ut.php in tests
    + reorganized destinations folders 
    + organized exakat for 'inside code' audit
+ Analysis
    + New analysis : support for libsvm
    + Updated analysis : Multiple unset() handles unset() at the beginning of the scope
    + Updated analysis : undefined static class now accounts for PHP and module classes
    + Checked unit tests : 2961 / 2995 test pass (99% pass)
+ Tokenizer
    + Extended class usage to static::class.
    + refactored 2 analysis for speed : double instruction and double assignations
    + fixed recent bug where Project token is twice.

**Version 1.7.7 (Sima Qing of Dingmao, 2019-04-29)**

+ Architecture
    + Upgraded to gremlin-php 3.1.1
    + Moved autoload into its own namespace
    + Started extending themes to modules
    + Skip external libraries when unit testing
    + Dump got one more query moved to DSL
    + Fixed build for overwritten methods, extended to magic methods
    + Load tokens by batch (5000+ tokens), not by file. 
+ Analysis
    + New analysis : Security : integer conversion
    + New analysis : implode() with one argument
    + Updated analysis : Invalid Regex handles \\ more precisely
    + Updated analysis : delimiter detection was checked for all of them
    + Checked unit tests : 2947 / 2983 test pass (99% pass)
+ Tokenizer
    + Upgraded Fallback detection for functions

**Version 1.7.6 (Jade Maiden of Yin, 2019-04-22)**

+ Architecture
    + Refactored Class definition with return typehint 
    + Added configuration for including development extensions.
    + Extended LoadFinal typehint hunting
+ Report
    + Phpcsfixer : new report
    + Ambassador : report usage of overridden PHP functions
    + Ambassador : new favorite : variable name in catch clause
+ Analysis
    + New analysis : array_merge and ellipsis should use coalesce
    + New analysis : Report overridden PHP native functions
    + New analysis : Merge all unset() into one
    + Updated analysis : Added missing constant for curl, pgsql, openssl
    + Updated analysis : Variadic are not variable arguments
    + Updated analysis : Useless Reference argument extended to foreach()
    + Updated analysis : Use Constant also covers pi()
    + Updated analysis : Inclusion Wrong Case handles dirname with 2nd argument
    + Updated analysis : Useless Argument : handles some edge cases with arrays
    + Checked unit tests : 2947 / 2975 test pass (99% pass)
+ Tokenizer
    + Upgraded handling of isRead and isModified attributes
    + Changed variadic argument counts in method declarations
    + Fixed original value in 'Sign'

**Version 1.7.5 (Xue King Zhuanlun, 2019-04-15)**

+ Architecture
    + Cleaned unused variables
+ Report
    + Ambassador : bugfixes report version 7.3, dropped 5.6 and 5.5
+ Analysis
    + Updated analysis : Already interface : extended to interface parents
    + Updated analysis : Else if to elseif : extended to one-liners
    + Updated analysis : No reference for ternary was extended
    + Updated analysis : Implements is for interface
    + Updated analysis : Refactored Is a Magic Property
    + Updated analysis : Refactored Conditional structures for constants
    + Checked unit tests : 2926 / 2950 test pass (99% pass)
+ Tokenizer
    + Link properties to magicmethod
    + Deduplicated virtual properties
    + Added isRead and IsModified properties. Omitting the corresponding analysis.

**Version 1.7.4 (Lu King Pingdeng, 2019-04-08)**

+ Architecture
    + reports, themes may be specified multiple times
    + 'project' command also work on themes and report from command line
    + Added htmlpurifier in auto-ignored libraries
    + Counting definitions, omitting Virtualproperties
    + Automatically detect identical files
+ Report
    + Inventories are grouped by values, sorted by count
+ Analysis
    + Updated analysis : This is for class : extended analysis to self and parent
    + Updated analysis : Undefined Classes
    + Updated analysis : Refactored Defined Parent MP 
    + Updated analysis : Redefined PHP function is restricted to global scope
    + Updated analysis : Could Use Alias also covers functions, constants.
    + Updated analysis : Refined SQL detection
    + Fixed step : goToALlParentsTrait missed some of the parent
    + Checked unit tests : 2916 / 2944 test pass (99% pass)
+ Tokenizer
    + Removed impossible implementations of traits
    + Fixed functioncalls' 'absolute' property
    + Refined parent's definitions
    + Trait also sports virtualproperties
    + Virtualproperties now respect visibilities
    + Distinguish Variables from Staticpropertynames
    + Added missing DEFINITION for Use (namespaces)

**Version 1.7.3 (Huang, King Dushi, 2019-04-01)**

+ Architecture
    + New command 'show' that display project creation command
    + Refactored UT detection mechanism
+ Report
    + Ambassador : report identical files in the code
    + Ambassador : global variable inventory is now grouped by name
+ Analysis
    + Updated analysis : PPPDeclaration style : handles Virtualproperties
    + Updated analysis : Closure2string : extended analysis
    + Updated analysis : Non-Ascii variable skips { }, & and @
    + Updated analysis : Could Be Static exclude abstract methods
    + Updated analysis : MismatchedTypehint : handles methodcalls and class hierarchy
    + Updated analysis : Could Use Try : refined analysis to avoid literals
    + Updated analysis : Hidden use, handles Virtualproperty
    + Updated analysis : Classes, wrong case, handles FQN
    + Checked unit tests : 2846 / 2926 test pass (97% pass)
+ Tokenizer
    + Moved creation of Virtualproperty early, to catch more situations
    + Virtualproperty mimic Propertydefinition
    + Added extra check when roaming the classes tree
    + Handles Sign constant values correctly

**Version 1.7.2 (Dong King Taishan, 2019-03-25)**

+ Architecture
    + Restored the external library checker
    + Added support for extension's CIT (Symfony, Drupal)
+ Report
    + Ambassador : added Suggestions theme to docs.
    + Perfile : New report, text, per file
+ Analysis
    + New analysis : Report potential 'unsupported operand type'
    + New analysis : Check for existence with __call() and __callstatic
    + Updated analysis : Wrong number of arguments (methods) upgraded
    + Updated analysis : Could Be Static ignores empty methods, constants methods
    + Updated analysis : Added Variable to possibly useless expression
    + Updated analysis : Constant names are detected based on available noDelimiter
    + Updated analysis : Abstract classes may have no abstract methods
    + Checked unit tests : 2889 / 2912 test pass (99% pass)
+ Tokenizer
    + Added link between __clone and clone
    + Now handling functions and constants when ignored
    + Fixed dynamic constants in collector

**Version 1.7.1 (Bi King Biancheng, 2019-03-18)**

+ Report
    + Ambassador : report lines that concentrate lots of issues
+ Analysis
    + Extended GoToAllImplements to extended interfaces
    + Updated analysis : NoScream usage, with authorized functioncall list like fopen
    + Updated analysis : HiddenUse with support for virtual properties
    + Checked unit tests : 2867 / 2900 test pass (99% pass)
+ Tokenizer
    + Added support for 'Virtualproperties'
    + Harmonized file escaping feature

**Version 1.7.0 (Bao King Yama, 2019-03-11)**

+ Architecture
    + Added auto-documenting 'ignored' cit to weed out obvious false positive
+ Report
    + Made Diplomat the default report
    + Added History report : it stores metrics from audit to audit
+ Analysis
    + New analysis : Identify self transforming variables ($x = foo($x))
    + New analysis : Report unclonable variables
    + Updated analysis : Undefined Classes, Interfaces and Trait now omit 'ignored' cit from folders
    + Updated analysis : Inconsistent usage is refactored for properties
    + Updated analysis : Useless expression, with clone new x
    + Updated analysis : Only Variable For Reference accepts $this, $_GET
    + Updated analysis : Lost References was modernized
    + Checked unit tests : 2854 / 2884 test pass (99% pass)
+ Tokenizer
    + Refactored support for Staticmethod (in a trait's use)
    + Added definitions for trait's use
    
**Version 1.6.9 (Lu King Wuguan, 2019-03-04)**

+ Architecture
    + Optimized Dump when navigating the links to the File Atom
    + Refactored LoadFinal into separate classes
    + Upgraded to Tinkergraph 3.3.5
    + Added options to cleandb to stop and start gremlin from exakat
    + Skip the task if no analysis has to run
+ Analysis
    + New analysis : Report inconsistent usage of properties or variables
    + New analysis : Typehinted return must return
    + Updated analysis : Variables used once handles closure (use) correctly
    + Updated analysis : Is Zero was refactored partially (WIP)
    + Updated analysis : Bad Typehint relay got a fix
    + Updated analysis : Function Subscripting is only suggested for one usage
    + Updated analysis : Lost References was modernized
    + Checked unit tests : 2854 / 2881 test pass (99% pass)
+ Tokenizer
    + Added definition for injected properties
    + Fixed sack() for subqueries
    + $this is not a classic variable
    + Removed double DEFINITION links
    + Fixed edge case with define() at the end of a script

**Version 1.6.8 (Yu King Songdi, 2019-02-25)**

+ Architecture
    + Added support for PHP 8.0
    + Fixed Constant FNP
    + Advance progressbar when ignoring files
+ Report
    + Ambassador : report usage of factories
    + Collect stats about Foreach usage
+ Analysis
    + New analysis : Report violation of law of Demeter
    + New analysis : Report removed constants and functions in PHP 8.0
    + Updated analysis : Refactored Nullable Typehint
    + Checked unit tests : 2851 / 2872 test pass (99% pass)
+ Tokenizer
    + Fixed edge case for Logical with strings
    + Reduced max level of looping in GoToAllParents
    + Distinguish $$ and ${$

**Version 1.6.7 (Li King Chujiang, 2019-02-18)**

+ Architecture
    + Documentation covers more PHP functions
    + Added some missing PHP functions
    + Fixed destination folder for extensions
+ Report
    + Ambassador : limited size of default values in visibility report.
    + Ambassador : reporting class depth
    + Ambassador : reporting dynamically created constants
    + Diplomat : leanner, meaner version of Ambassador
    + New category : Top 10 classic mistakes
+ Analysis
    + New analysis : Report when relayed typehint are not the sames
    + Updated analysis : Regex now handles local variables and constants
    + Updated analysis : Variables Used Once now covers closures and use
    + Checked unit tests : 2846 / 2867 test pass (99% pass)
+ Tokenizer
    + Defineconstant may be constant
    + Fixed handling of Nullable for typehint
    + Started preparing for Gremlin 3.4.0 : WIP

**Version 1.6.6 (Jiang King Qinguang , 2019-02-11)**

+ Architecture
    + Removed FetchContext() from DSL
    + Added options to follow constants from atomIs.
+ Report
    + Now dumps magic methods
+ Analysis
    + New analysis : Report insufficient interfaces in typehint
    + Updated analysis : Class constant now ignore empty classes
    + Checked unit tests : 2837 / 2858 test pass (99% pass)
+ Tokenizer
    + Moved 'Define' to its own atom
    + Upgraded Logical to hanlde Strings as PHP
    + Fixed T_POWER => T_POW
    + Refactored calculation for globalpath
    + Fixed edgecase with endswitch;

**Version 1.6.5 (Mahagate, 2019-02-04)**

+ Architecture
    + Added CVS as an external service
    + Graph GSNeo4j export variable for shell access. putenv is not sufficient
    + Dump : report class name, not its code
    + Extended listAllThemes to extensions
    + Fixed bug in extension loader with phar
+ Report
    + Ambassador : restored file dependencies tree
    + Ambassador : fixed altered directive filename
    + Ambassador : added direct link to docs
+ Analysis
    + New analysis : arrays that are initialized with strings
    + New analysis : Avoid Lone variables as conditions
    + New analysis : Added support for weakref and pcov
    + Updated analysis : extended regex to arrays in preg_* calls
    + Updated analysis : Implicit globals now also marks the variable in global space
    + Updated analysis : Add Zero, Multiply by One also cover 2 * $x = 1;
    + Updated analysis : Could Use Interface now takes into account PHP interfaces, and classes first level.
    + Updated analysis : Relay Functions now omits calls to parent's __construct and __destruct
    + Checked unit tests : 2830 / 2852 test pass (99% pass)

**Version 1.6.4 (Parasamgate, 2019-01-28)**

+ Architecture
    + Added support for CVS as a VCS
    + Upgraded support for tar as a VCS
    + Added support modification counts by files
    + Added first tracking for closures
    + Upgraded Tinkergraph driver
+ Report
    + Added Atoms in the documentations
    + Extra protection for Class Changes
+ Analysis
    + Updated analysis : Use-arguments are now counted as arguments
    + Updated analysis : Max Argument check was refactored
    + Updated analysis : IsModified now takes into account extensions
    + Updated analysis : Should Use This now exclude empty methods
    + Updated analysis : undefined classes now support PHP 7.4 typed properties
    + Updated analysis : added missing scalar PHP types
    + Updated analysis : uncaught exceptions now cover parents
    + Updated analysis : refactored incompatibility checks for methods
    + Checked unit tests : 2824 / 2841 test pass (99% pass)
+ Tokenizer
    + Refactored alternative ending, removed extra VOID
    + Upgraded contexts and their nesting
    + Added extra checks on variables names
    + Added support for ??= (PHP 7.4)

**Version 1.6.3 (Paragate, 2019-01-21)**

+ Architecture
    + Better presentation for exakat extensions
    + Added build.xml for Jenkins
    + Fixed copyright years
+ Report
    + Ambassador : fixed class name for Phpcompilation
+ Analysis
    + New analysis : assign and compare at the same time
    + Updated analysis : uncaught exceptions now cover parents
    + Updated analysis : strpos too much is extended to strrpos and strripos
    + Updated analysis : Refactored Indirect injections for more refined reports
    + Updated analysis : Empty Block doesn't omit Ifthen anymore
    + Updated analysis : Implemented methods are public mistook interface methods
    + Updated analysis : Object Reference omits arguments that are wholly assigned
    + Checked unit tests : 2808 / 2826 test pass (99% pass)
+ Tokenizer
    + Added support for PHP 7.4 typed properties (needs PHP 7.4-dev)

**Version 1.6.2 (Silver Headed Gate, 2019-01-14)**

+ Architecture
    + Fixed infinite loop when an option missed a value
    + Produce phpversion in config.ini, but leave it commented
+ Report
    + Ambassador : colored syntax for visibility report
    + Ambassador : inventory reports now display number of usages
+ Analysis
    + Updated analysis : Added support for PHP 7.2.14
    + Updated analysis : Avoid Using Class handles \
    + Updated analysis : Unused Functions works with multiple identical functions
    + Checked unit tests : 2795 / 2817 test pass (99% pass)
+ Tokenizer
    + Fixed bug that mixed T_OR and T_XOR
    + Fixed bug that missed intval for Power
    + Handles multiple definitions of functions
    + Removed one Void too many with closing tag

**Version 1.6.1 (Golden Light Gate, 2019-01-07)**

+ Architecture
    + Upgraded documentation for Extensions
    + Upgraded processing of files, specially with special chars
    + Project stops when no token are found
    + Storing hash for each files. RFU.
+ Report
    + Ambassador : added support for class constant's changes
    + Ambassador : added classSize report
    + Ambassador : 'New issues' now takes line difference into account
    + Themes are better dumped
+ Analysis
    + New analysis : array_key_exists() is faster in PHP 7.4
    + New analysis : partial report from preg_match()
    + Updated analysis : Avoid Using Class handles \
    + Updated analysis : Class Usage uses class_alias()
    + Updated analysis : Empty traits 
    + Updated analysis : Unused arguments now skips __set()
    + Updated analysis : Path strings
    + Updated analysis : Missing include handles more concatenations
    + Checked unit tests : 2792 / 2812 test pass (99% pass)
+ Tokenizer
    + Fixed precedence for identical operators
    + Fixed bug with ?> inside switch

**Version 1.6.0 (VirupakSa, 2018-12-31)**

+ Architecture
    + VCS are not tested when they are not used
+ Analysis
    + Updated analysis : Php Reserved names ignores variable variables
    + Updated analysis : Array not using a constant, with Heredoc
    + Updated analysis : Long arguments
    + Updated analysis : Empty With Expression ignores simple assignations
    + Refactored analysis : Callback needs returns
    + Refactored analysis : No Return used
    + Checked unit tests : 2780 / 2805 test pass (99% pass)
+ Tokenizer
    + Fixed regression with Yield and =>
    + Fixed edge case "$a[-0x00]"

**Version 1.5.9 (Dhrtarastra, 2018-12-24)**

+ Architecture
    + Use PHP in project config for default PHP version
    + cleandb uses -p
    + Moved projects/.exakat to projects/<-p>/.exakat folders
    + Using $config and not more hardcoded tinkergraph
    + Extra check on doctor 
+ Report
    + Ambassador : extra check for 'previous' report
+ Analysis
    + Upgraded analysis : Empty With Expression skip a few false positive
    + Checked unit tests : 2770 / 2795 test pass (99% pass)
+ Tokenizer
    + Fixed edgecase for methods named 'class'
    + Fixed class name in Project

**Version 1.5.8 (Virudhaka, 2018-12-17)**

+ Architecture
    + Handles themas provided by extensions
    + Added busyTimeout for dump.sqlite
    + Reduced size of thema tables
    + Docs handle parameter dynamically
    + Added 'update' for extensions
+ Report
    + Ambassador : added a 'Path' inventory, with file paths
+ Analysis
    + New analysis : Closures that are identical
    + Upgraded analysis : Url and SQL detection, case sensitivity
    + Upgraded analysis : Could Use array_fill_keys
    + Upgraded analysis : Undefined functions doesn't miss functions inside classes, handles interfaces
    + Upgraded analysis : Empty Functions better handles return; 
    + Upgraded analysis : Long Argument may be configured
    + Upgraded analysis : Fixed bug with empty include path
    + Checked unit tests : 2770 / 2795 test pass (99% pass)
+ Tokenizer
    + Added FNP to strings
    + First link between method and definition with typehint
    + Support for class_alias
    + Fixed edge case with use ?>
    + Fixed variable in string behavior for $this and $php variables

**Version 1.5.7 (Vaisravana, 2018-12-10)**

+ Architecture
    + Extended Dump to support aliased methods
    + Support for SQLITE in extensions
    + Moved each framework to extensions
    + Added Laravel extension
+ Documentation
    + First version for the Extension chapter
    + Fixed mysterious ' in the docs
+ Report
    + Ambassador : added a 'New issues' section, with new analysis
    + Ambassador : added trait matrix
    + Ambassador : fixed an infinite loop when trait include themselves in cycles
    + Added more message count to several reports
+ Analysis
    + New analysis : method could be static
    + New analysis : multiple inclusion of traits
    + New analysis : avoid self using traits
    + New analysis : ext/wasm and ext/async
    + Upgraded analysis : No Hardcoded Hash, skip hexadecimal numbers
    + Upgraded analysis : Defined properties extends to traits
    + Upgraded analysis : PSS outside a class, when PSS are in strings
    + Upgraded analysis : Access private works with methods (not just static)
    + Checked unit tests : 2772 / 2785 test pass (99% pass)
+ Tokenizer
    + Fixed bug in Dump, when nothing to clean
    + Fixed edge bug on Callable detection
    + Extended support for self, static and parent, in typehint and new
    + Fixed precedence of yield and yield from
    + Fixed handling of throw at the end of a script
    + Added support to solve conflict on traits

**Version 1.5.6 (Jingang, 2018-12-03)**

+ Architecture
    + Moved all framework to extensions. WIP.
    + Code cleaning
    + Refactored the analysis dependency sorting
    + Now display progress bar for files
    + Fixed configuration for directories and files
+ Report
    + Fixed FileDependecy and DependencyWheel, to actually count messages
+ Analysis
    + Added a lot more new method descriptions for PHP native classes
    + New analysis : suggestion simplification for !isset($a) || !isset($a[1])
    + New analysis : Useless Trait alias
    + New analysis : report usage of ext/sdl
    + Upgraded analysis : Refactored IsZero, to handle assignations and parenthesis
    + Upgraded analysis : pack format is better checked
    + Checked unit tests : 2759 / 2771 test pass (99% pass)
+ Tokenizer
    + Fixed a missing fullnspath for origin in Use for Traits
    + Handles simple aliases for traits methods
    + Fixed mishandling of variables inside strings
    + Fixed support of negative numbers inside strings
    + Fixed bug with yield inside an array
    + Fixed strange case with define and integers as constant names

**Version 1.5.5 (Ratnadhvaja, 2018-11-25)**

+ Architecture
    + Initial version of Exakat extensions
    + Moved processing of 2-tokens files to Load
    + Speed up CSV creations
    + Upgrades are read from https, no http
    + Moved loading's sqlite to memory for speed gain
    + Doctor now auto-create test folder
+ Report
    + New report : Php city. See your PHP code as a city
    + Ambassador : Appinfo() now reports keywords used as method or property
    + Fixed reported names of properties
+ Analysis
    + New analysis : checks some HTTP headers for security
    + New analysis : Use _file() functions, not file_get_contents()
    + New analysis : Optimize looks for fgetcsv()
    + Upgraded analysis : Several refactored analysis
    + Checked unit tests : 3083 / 3096 test pass (99% pass)
+ Tokenizer
    + Fixed encoding error in loading, for clone types.

**Version 1.5.4 (Mahakasyapa, 2018-11-19)**

+ Architecture
    + Added error message for memory limit 
    + Added GC to Project action
    + Migrated Melis to extension
    + Dumping data is now done en masse
    + Analysers now handle side-queries
    + Clear message in case of memory limit
    + Doctor doesn't stop at missing helpers
    + VCS leak less errors
    + Added support for 7z
    + Extended validation for themas
    + Restored Tinkergraph driver 
    + Upgrade logs with extra reports
+ Analysis
    + New analysis : Report problems with class constant visibilities
    + New analysis : Avoid self, parent and static in interfaces
    + Upgraded analysis : Variable reuse now skips empty arrays
    + Checked unit tests : 3077 / 3090 test pass (99% pass)
+ Tokenizer
    + Fixed bug where variable was mistaken for a string inside strings

**Version 1.5.3 (Ananda, 2018-11-12)**

+ Architecture
    + Extended results to methods, traits
    + Added support for PHP 7.2.12
    + 'master' is not used anymore as default branch
    + Fixed creation of initial config/exakat.ini
    + Fixed handling badly written exakat.ini or PHP binary paths
+ Report
    + Ambassador : report classes that could be final or abstract
+ Analysis
    + New analysis : Property Used Once : now includes redefined functions
    + New analysis : iterator_to_array() should use yield with keys or array_merge()
    + New analysis : Don't loop on yield : use yield from
    + Upgraded analysis : Dependant trait now include parent-traits
    + Checked unit tests : 3080 / 3093 test pass (99% pass)
+ Tokenizer
    + Changed handling of variable that are both global AND local
    + Disambiguated variables and properties
    + Extended OVERWRITE to constants and methods

**Version 1.5.2 (Master Puti, 2018-11-05)**

+ Report
    + Fixed storage of themes in dump.sqlite
    + Ambassador : report nothing when there are no trait, interface or class in the tree.
+ Analysis
    + New analysis : idn_to_ascii() will get new default
    + New analysis : support for decimal extension
    + New analysis : support for psr extension
    + Upgraded analysis : Extended support to PHP native exceptions
    + Upgraded analysis : Could use typecast now handles intval() second param
    + Upgraded analysis : Variable strange names avoids properties
    + Checked unit tests : 3058 / 3085 test pass (99% pass)
+ Tokenizer
    + Upgraded support for arrays inside strings (string/constant distinction)
    + Added DEFINITION for constant() and defined()
    + Fixed value of line for some ***definition

**Version 1.5.1 (Eighteen Arhats, 2018-10-29)**

+ Analysis
    + New analysis : could use basename() second args
    + Upgraded analysis : Variables strange names do not report ...
    + Checked unit tests : 3061 / 3079 test pass (99% pass)
+ Tokenizer
    + Moved TRAILING as a property
    + Moved NULLABLE as a property
    + Sync ALIAS with AS
    + Fixed link between Use expression when using an alias

**Version 1.5.0 (Pilanpo Bodhisattva, 2018-10-22)**

+ Architecture
    + Fixed " in the examples of the manual
    + Upgraded stability with new history testing
+ Report
    + Ambassador : now report interface and trait hierarchy
    + Ambassador : new format inventory for pack and printf
    + Dump : Fixed list of traits
+ Analysis
    + New analysis : Could Use Try, for native calls that may produce an exception
    + New analysis : idn_to_ascii() will get new default
    + Upgraded analysis : Undefined variables exclude $this
    + Upgraded analysis : Variables used once avoid properties
    + Upgraded analysis : ext/json : JsonException
    + Upgraded analysis : added new PHP 7.3 constants (curl, pgsql, mbstring, standard)
    + Upgraded analysis : scalar or object property now ignore NULL as default
    + Refactored analysis : UsedProtectedMethod
    + Checked unit tests : 3059 / 3071 test pass (99% pass)
+ Tokenizer
    + Handles NaN and INF when the literals reach them
    + Static constant may be variable if object is variable
    + Removed superfluous linking for static calls.

**Version 1.4.9 (Lingji Bodhisattva, 2018-10-15)**

+ Architecture
    + Extended documentation with phpVersion, time to fix and severity
    + Upgraded bufixes to PHP 7.2.11
    + Added more tests on arguments in the DSL
    + Removed double definitions for class constants
    + Initial support for extension folder
+ Report
    + Collect the number of local variables, per method
+ Analysis
    + New analysis : report accessing properties the wrong way
    + New analysis : suggest named patterns
    + New analysis : check Pack() arguments
    + New analysis : Return in generators, for PHP 7.0 +
    + New analysis : Repeated interfaces
    + New analysis : Static properties shouldn't use references until PHP 7.3
    + New analysis : Don't read and write in the same expression
    + Upgraded analysis : is interface methods, extended to magic methods
    + Upgraded analysis : empty regex
    + Upgraded analysis : never used properties
    + Upgraded analysis : logical operators in letters
    + Upgraded analysis : could use interface, extended with PHP native interfaces
    + Upgraded analysis : Is Zero, better handling of mixed expressions
    + Refactored analysis : Empty functions
    + Refactored analysis : Used Private Methods
    + Checked unit tests : 3036 / 3055 test pass (99% pass)
+ Tokenizer
    + Added DEFINITION between new and __construct
    + Added support for className::class() 
    + Added better support for dynamic method calls
    + Added better support for dynamic property calls
    + Removed some usage of TokenIs

**Version 1.4.8 (Ksitigarbha, 2018-10-08)**

+ Architecture
    + Adding more validation at DSL step level : stricter check on args, speed gain
    + Cleaning more analysis from MAX_LOOPING variable
    + Better protection for file names 
    + Removed static properties from DSL
+ Analysis
    + New analysis : Don't use __clone before PHP 7.0
    + New analysis : Watch out for filter_input as a data source
    + Upgraded analysis : Method Used Below refactored for speed
    + Upgraded analysis : Undefined class constants now takes into account interfaces
    + Removed anaysis : Relaxed Heredoc was double with Flexible Heredoc
    + Checked unit tests : 3016 / 3033 test pass (99% pass)
+ Tokenizer
    + Build links between methodcall and method in a class
    + Added links between method and its overwritten version in child
    + Fixed fallback for functions
    + Fixed linked between traits and their definition
    + Removed variable definition for Parametername
    + Simplified double usage between return and pushExpression()

**Version 1.4.7 (Maitreya, 2018-10-01)**

+ Architecture
    + Added 'Suggestions' section to documentation, for many rules
    + WIP : removing usage of MAX_LOOPING in analysis
    + Added a lot of new external services
    + Added documentation for creating a new analysis
+ Analysis
    + Upgraded analysis : No interface was dropped in PHP 7.2
    + Upgraded analysis : IsAMagicProperty extended to parents
    + Removed anaysis : Relaxed Heredoc was double with Flexible Heredoc
    + Checked unit tests : 3017 / 3029 test pass (99% pass)
+ Tokenizer
    + Linking variable in closure's use to its local variable
    + Removed some unused atoms from GraphElements

**Version 1.4.6 (Dipankara, 2018-09-24)**

+ Architecture
    + Various code refactorisations
    + Migration to PHPUnit 7.3.5
    + Fixed filenames case
    + Better handling of VCS
    + More validations for project names
    + More docs
+ Report
    + Ambassador/Weekly : fixed ' in analyser titles
+ Analysis
    + Upgraded analysis : Fopen mode accepts 'r+b'
    + Upgraded analysis : Unused Traits
    + Upgraded analysis : Undefined Variables
    + Checked unit tests : 3020 / 3033 test pass (99% pass)
+ Tokenizer
    + New analysis : report literal used with reference
    + Added support for boolval to Keyvalue
    + Fixed support for boolval to Arraylist
    + Added DEFINITION to static methods
    + Added Variabledefinition for local variables
    + Fixed bug in Not

**Version 1.4.5 (Guanyin Bodhisattva, 2018-09-17)**

+ Architecture
    + Removed times() for until() in Dumps
+ Report
    + Manual : added folders tree
+ Analysis
    + New analysis : Add Default To Parameter
    + Upgraded analysis : Avoid reporting PHP function as classes
    + Upgraded analysis : More empty Functions than just foo() {}
    + Upgraded analysis : Wrong Number of argument now takes into account variadic
    + Upgraded analysis : Should Use Constant now encompasses () and ?: structures
    + Upgraded analysis : This Is Not An Array now takes ArrayObject/SimpleXmlElement into account
    + Checked unit tests : 3009 / 3020 test pass (99% pass)
+ Tokenizer
    + Fixed 'constant' status with Arrayliteral
    + Fixed bug where strings are build close to the end of the script

**Version 1.4.4 (White Dragon Horse, 2018-09-10)**

+ Architecture
    + Doctor reports the set of tokens used
    + Lots of docs checks
+ Report
    + Ambassador / Phpconfiguration : report disable_functions and disable_classes
    + Finished Weekly report
+ Analysis
    + New analysis : report ext/seaslog
    + Upgraded analysis : Incompatible signatures
    + Fixed DSL : analysisIs
    + Checked unit tests : 3000 / 3010 test pass (99% pass)
+ Tokenizer
    + Closure are now processed with runplugin
    + Removed depencencies to usedClasses
    + Fixed detections of Closure at the end of a script

**Version 1.4.3 (Sha Wujing, 2018-09-03)**

+ Architecture
    + No error if missing svn
    + Extended 'First' thema
    + Now reporting PHP native CIT, constants and functions
+ Report
    + Ambassador : php.ini suggestions includes disable_functions
+ Analysis
    + New analysis : report typecasting for json_decode
    + New analysis : report classes that could be final
    + New analysis : simplify closure into callback
    + New analysis : report inconsistent elseif conditions
    + Upgraded analysis : Reduced false positive on Type/Default mismatch
    + Upgraded analysis : Drop Else After Return uses elsif
    + Upgraded analysis : Unused Private Property (rare)
    + Checked unit tests : 2990 / 3004 test pass (99% pass)
+ Tokenizer
    + Removed extra Void after function definitions
    + Fixed fullnspath with define()

**Version 1.4.2 (Zhu Bajie, 2018-08-27)**

+ Architecture
    + Fixed leftover bugs in the new DSL language
    + Adopter Query in LoadFinal (first test)
    + Extended support for clone type 1
+ Report
    + New Report : Weekly report
+ Analysis
    + New analysis : report forgotten conflict in traits
    + New analysis : undefined insteadof
    + New analysis : undefined variable
    + New analysis : report classes that must call parent::__construct
    + Upgraded analysis : Inexistant Compact variable
    + Upgraded analysis : Test class was refactored
    + Checked unit tests : 2975 / 2989 test pass (99% pass)
+ Tokenizer
    + New atom : Staticmethod, for Insteadof (replacing 'Staticconstant')
    + Added DEFINITION link for array('class', 'method') structure

**Version 1.4.1 (Tang Sanzang, 2018-08-20)**

+ Architecture
    + Spined off Query for Gremlin, with Exakat DSL.
    + Centralized 'methods' property in Analysis class
    + Extended MAX_LOOPING usage
+ Analysis
    + Added new thema : Class Review
    + Upgraded analysis : Defined Parent MP (less queries)
    + Upgraded analysis : Less false positives
    + Added support for PHP 7.2.9
    + Checked unit tests : 2965 / 2980 test pass (99% pass). 
+ Tokenizer
    + Fixed Edge case with Ternary and Boolean
    + Added Staticpropertyname to distinguish from variables
    + Added support for remote definitions to methods
    + Removed global path for CIT (no fallback) 

**Version 1.4.0 (Sun Wu Kong, 2018-08-13)**

+ Architecture
    + Chunked result inserts for Dump
    + More support for PHP 7.4
+ Report
    + Ambassador : added new Appinfo for relaxed Heredoc, trailing comma...
+ Analysis
    + New analysis : class can be abstract
    + New analysis : trailing comma
    + New analysis : relaxed heredoc
    + New analysis : removed functions in PHP 7.3
    + New analysis : continue versus break
    + Upgraded analysis : Hardcoded passwords is extended to objects
    + Checked unit tests : 2964 / 2979 test pass (99% pass). 
+ Tokenizer
    + Measure definitions stats for classes. 
    + Added support for relaxed heredoc
    + Added support for closure as a return value
    + Refactored support for Ternary and Labels

**Version 1.3.9 (Du Ruhui, 2018-08-06)**

+ Architecture
    + Added support for PHP 7.4
    + 'Copy' won't update anymore
+ Report
    + Ambassador : fixed repeated 'compatibility' menu entry
+ Analysis
    + New analysis : avoid __CLASS__ and get_called_class().
    + New analysis : prepare for (real) deprecation 
    + New analysis : const / define preference
    + New analysis : define case sensitivity preference
    + New analysis : avoid defining assert() in namespaces
    + Removed analysis : Variables/Arguments
    + Checked unit tests : 2957 / 2971 test pass (99% pass). 
+ Tokenizer
    + Removed Noscream - AT atom
    + Added definition for class constants
    + Fixed bug : can't apply ~ to false
    + Extended DEFINITION support to closure's use and references

**Version 1.3.8 (Fang Xuanling, 2018-07-30)**

+ Architecture
    + 'Copy' won't update code anymore.
+ Analysis
    + Upgraded analysis : 'should use operator' only applies to constant chr() call
    + Upgraded analysis : Useless Instructions is faster
    + Checked unit tests : 2948 / 2962 test pass (99% pass). 
+ Tokenizer
    + Added support for variable definitions in methods

**Version 1.3.7 (unnamed demon, 2018-07-16)**

+ Architecture
    + Fixed handling of multiple updates
+ Report
    + More documentations
+ Analysis
    + New analysis : report usage of callback to process array
    + New analysis : report usage of case insensitive constants
    + Upgraded analysis : Hardcoded passwords is extended to objects
    + Upgraded analysis : Go To Key Directly handles comparisons
    + Added support for PHP 7.0.20
    + Checked unit tests : 2948 / 2962 test pass (99% pass). 

**Version 1.3.6 (Zhang Gongjin, 2018-07-16)**

+ Architecture
    + Added support for Rar archives
    + Removed call to gremlin server at 'status' time
+ Analysis
    + New analysis : support for msgpack extension
    + New analysis : support for lzf extension
    + Upgraded analysis : added missing function names in several extensions
    + Checked unit tests : 2941 / 2955 test pass (99% pass). 

**Version 1.3.5 (Gao Shilian, 2018-07-09)**

+ Architecture
    + Removed 4 unused exceptions
    + Extracted Query from Analysis
+ Report
    + Reports : centralized all doc reading
    + Reports : doc reading now parses sections (avoid overlap)
    + Ambassador : Added exakat version and build to dashboard.
    + Ambassador : Added Class Tree (All class hierarchies)
+ Analysis
    + Fixed bug with 'last' and '2last'
    + New analysis : Report undefined::class
    + New analysis : Report returned assignations as useless
    + New analysis : Split scalar typehint by versions
    + Upgraded analysis : Extended Reuse Variable to instantiations
    + Upgraded analysis : Masking parenthesis are only for referenced arguments
    + Upgraded analysis : Wrong case doesn't apply to parent/static/self
    + Upgraded analysis : Locally Unused Properties are extended to traits
    + Upgraded analysis : Should Preprocess is extended to concatenations
    + Upgraded analysis : Array_key_fill exclude variables by default
    + Upgraded analysis : Ambiguous static reports the whole property definition
    + Checked unit tests : 2919 / 2944 test pass (99% pass). 
+ Tokenizer
    + Added missing constants
    + Fixed support for goto true;
    + Fixed edge case for nested ternaries and boolean
    + Moved Goto and Label to Name Atom

**Version 1.3.4 (Cheng Yaojin, 2018-07-02)**

+ Architecture
    + Added check when unarchiving tar.gz and tar.bz
    + Added check for neo4j installation, (error grabing)
    + Moved Upgrade to tmp folder
+ Analysis
    + Parameters are actually defined in the class
    + New analysis : ambiguous visibilities of properties
    + New analysis : report usage of PHP 7.1+ hash algorithm
    + New analysis : csprng (random_bytes and random_int)
    + New analysis : ext/libeio
    + New analysis : report incompatible signatures for methods
    + Upgraded analysis : Unused Private Methods handles fluent interfaces
    + Upgraded analysis : Defined Parent keyword
    + Upgraded analysis : Recursion
    + Refactored codeIs/codeIsNot
    + Checked unit tests : 2908 / 2923 test pass (99% pass). 
+ Tokenizer
    + Added support for 'parent' definitions
    + Fixed element counts in concatenation 
    + Fixed operator priority in Strval
    + Upgraded handling of undefined constants to string

**Version 1.3.3 (Ma Sanbao, 2018-06-25)**

+ Architecture
    + Better handling of fallback to global for functions
    + Weekly code clean
    + Refactored several analysis for speed
+ Report
    + Ambassador : fixed regression in the dashboard
    + Fixed edge case with properties
+ Analysis
    + New analysis : closure that can be static
    + Upgraded analysis : empty function doesn't count static or global
    + Upgraded analysis : reported globals include $GLOBALS also
    + Checked unit tests : 2881 / 2911 test pass (98% pass). 
+ Tokenizer
    + Moved collection of functioncall to LoadFinal
    + Added collection of interfaces and newcall
    + Moved Declare to its own token
    + Moved Property definitions to its own token

Version 1.3.2 (Duan Zhixian, coming up)
+ Architecture
    + Reading stats from store, not graph.
    + Git now fails silently if login is requested at clone / pull
+ Report
    + New analysis : == or === favorites
    + New analysis : > or < favorites
    + Upgraded analysis : written only variables is now faster
    + Upgraded analysis : PHP reserved words has now 2 parameters
    + Removed analysis : Type/Integer, Real, Closures.
    + Checked unit tests : 2901 / 2914 test pass (99% pass). 
+ Tokenizer
    + Static, PPP, Final and Abstract are now properties
    + Fixed regex in several rules
    + Added support for code clone detection (WIP)

**Version 1.3.1 (Liu Hongji, 2018-06-03)**

+ Architecture
    + Cleaned code of unused classes and ;
    + Fixed connexion script to the database
    + Fixed check of php.log folder
+ Report
    + Ambassador : display correct compilation state
+ Analysis
    + Upgraded analysis : used constant is also applied to defined()
    + Upgraded analysis : used protected methods is case insensitive
    + Upgraded analysis : Empty class omits extended classes
    + Upgraded analysis : More sequences to SimplePreg
    + Upgraded analysis : Throwable is not 'unthrown' anymore
    + Removed analysis : Static CPM
    + Checked unit tests : 2901 / 2914 test pass (99% pass). 
+ Tokenizer
    + Upgraded support for ::class

**Version 1.3.0 (Xue Rengui, 2018-06-03)**

+ Architecture
    + Added support for Tinkergraph 3.3.3
    + Handles situations where exakat has no database
    + Check for PHP version at bootstrap
+ Report
    + Ambassador : Updated PHP recommendation report with PHP 7.3
    + All : Variables don't sport ... nor & anymore
+ Analysis
    + New analysis : Single Use Variable
    + New analysis : Should Use Operator
    + New analysis : Check JSON production
    + New analysis : Report visibility usage with constants
    + Upgraded analysis : used constant is also applied to defined()
    + Upgraded analysis : used protected methods is case insensitive
    + Upgraded analysis : used directives handle function version
    + Upgraded analysis : added lcg_value for better rand
    + Upgraded analysis : Use Nullable extended to methods, closures.
    + Upgraded analysis : Fixed support for '_' native function
    + Checked unit tests : 2895 / 2907 test pass (99% pass). 

**Version 1.2.9 (Wang Gui, 2018-05-28)**

+ Architecture
    + Removed query cache from gremlin
    + Added pre-query check to prevent queries that have no chance of result
+ Report
    + Ambassador : first 50% of documentation fix : double quotes are not well displayed
    + Ambassador : Results are ordered by files, then by lines
+ Analysis
    + New analysis : Flexible Heredoc syntax
    + New analysis : Non-compatible methods
    + New analysis : Use the Blind Var
    + New analysis : Inexistant Compact
    + New analysis : Typehint / default value mismatch
    + Upgraded analysis : strict_types are not recognized as undefined constant
    + Upgraded analysis : More new methods for PHP 7.3
    + Upgraded analysis : Dependant traits
    + Upgraded analysis : Strpos comparison
    + Upgraded analysis : Method Must Return
    + Checked unit tests : 2885 / 2889 test pass (99% pass). 
+ Tokenizer
    + Interface may have const, not traits (Loading)
    + Added support for static call to methods

**Version 1.2.8 (Xu Jingzong, 2018-05-21)**

+ Architecture
    + Implemented a cache for speed boost.
    + Refactored files finding method
    + Git VCS always submit a user when cloning (using exakat by default)
    + Moved custom themes from themas.ini to themes.ini
+ Report
    + Ambassador : fixed naming the audit
    + Ambassador : added 'Dead code' section
    + Doctor : split themes display (default/customs)
+ Analysis
    + New analysis : Report what should be done in SQL
    + New analysis : Typehinted reference
    + New analysis : Strpos doing too much work
    + New analysis : Can't instantiate class
    + Upgraded analysis : Don't echo error
    + Upgraded analysis : PPP Declaration style
    + Upgraded analysis : Useless abstract class
    + Upgraded analysis : Buried assignation doesn't report declare anymore
    + Upgraded analysis : Abstract methods are not reported as unused
    + Upgraded analysis : relaxed version constraint for all Extensions/*
    + Checked unit tests : 2852 / 2856 test pass (99% pass). 
+ Tokenizer
    + Fixed handling of short_open_tags
    + Fixed edge case with % 

**Version 1.2.7 (Li Yuanji, 2018-05-14)**

+ Architecture
    + Extended status command to all VCS
    + Added support for customized themes
    + Added Upgrading section, List of parametrized analysis, revamped summary
    + Simplified handling of commandline options
    + Removed usage of JSON for 'doctor'
+ Report
    + A lot more documentation, examples, links.
    + Optimized type downloader
    + Added report themes pre-requisites
+ Analysis
    + New analysis : ext/cmark
    + Upgraded analysis : too many children is configurable
    + Upgraded analysis : error_reporting 0 and -1 are not reported as issues.
    + Checked unit tests : 2835 / 2839 test pass (99% pass). 
+ Tokenizer
    + Fixed bug where constant self referenced.
    + Moved Identifiers to Names
    + Added first definitions for members. 

**Version 1.2.6 (Li Jiancheng, 2018-05-07)**

+ Architecture
    + Moved more classes to helpers
    + Removed constants for Tokens
    + Upgraded to Robo 1.2.3
+ Report
    + Added support for custom themas for reports.
+ Analysis
    + New analysis : zookeeper
    + New analysis : Report missing parenthesis
    + New analysis : Report invalid interval checks
    + New analysis : Suggest array_unique when possible
    + New analysis : Report when callback needs a return
    + New analysis : Reduce the number of if
    + Updated Exception list, up to PHP 7.3
    + Upgraded analysis : Printf Arguments
    + Upgraded analysis : Count On Null
    + Upgraded analysis : Regex on Collector
    + Upgraded analysis : File Inclusion wrong case handles parenthesis
    + Upgraded analysis : Make globals a property
    + Upgraded analysis : Invalid regex
    + Checked unit tests : 2814 / 2818 test pass (99% pass). 
+ Tokenizer
    + Added definition links for staticmethodcalls.
    + Added boolean and int values to __DIR__ and co.
    + Removed several static properties
    + Fixed precedence of instanceof
    + Added support for Null val

**Version 1.2.5 (Li Yuan, 2018-04-30)**

+ Architecture
    + Added command 'config' to configure project from commandline
    + Made Exakat reentrant
    + Moved Configuration creation to external file
    + Upgraded status when audit isn't run yet
+ Analysis
    + New analysis : Regex on Collector
    + Upgraded analysis : Only Variable with reference argument
    + Upgraded analysis : File Inclusion Wrong Case
    + Upgraded analysis : Invalid Regex
    + Added support for PHP 7.2.5, 7.1.17 and 7.0.30
    + Checked unit tests : 2802 / 2809 test pass (99% pass). 
+ Tokenizer
    + Fixed various bugs with constant scalar expression

**Version 1.2.4 (Li Chunfeng, 2018-04-23)**

+ Architecture
    + Now fail with explicit message for memory running out
+ Report
    + Ambassador : Updated 'confusing variables' report
+ Analysis
    + Upgraded analysis : Could be short assignment
    + Upgraded analysis : Could be static
    + Upgraded analysis : Fail Substr Comparison (handles constants)
    + Checked unit tests : 2796 / 2801 test pass (99% pass). 
+ Tokenizer
    + Added propagation of constants when value can be processed
    + Introduced 'Parameter' token, to differentiate with Variable
    + Fixed syntax highlighting
    + Fixed a bug with negative bitshift

**Version 1.2.3 (Yuan Tiangang, 2018-04-16)**

+ Architecture
    + New append for logs
+ Report
    + New report : Manual.
    + Ambassador : Rewrote the export of 'confusing variables'
+ Analysis
    + New analysis : report strtr bad usage
    + New analysis : don't unset properties
    + Upgraded analysis : Invalid Regex
    + Upgraded analysis : Property Could Be Local 
    + Upgraded analysis : No Hardcoded path
    + Upgraded analysis : echo/print preferences also report printf
    + Removed analysis : Close Naming (now done at Report level)
    + Checked unit tests : 2770 / 2786 test pass (99% pass). 
+ Tokenizer
    + Removed double definition for functioncalls

**Version 1.2.2 (Yin Kaishan, 2018-04-09)**

+ Architecture
    + Cleaned doctor so it works even without requirements
    + Fixed special chars with git URL
+ Report
    + Ambassador : new inventory with classes changes in heritage
    + Ambassador : new inventory of large expressions
    + Upgraded report : Defined Exceptions are cleaned of doubles
+ Analysis
    + New analysis : report Redefined Private Properties
    + New analysis : report substr() usage with strlen
    + Upgraded analysis for Inclusion Wrong Case filenames
    + Upgraded analysis : Cast To Boolean is extended to True/False
    + Upgraded analysis : Omit negative lengths
    + Upgraded analysis : interface search also include parameter counts
    + Upgraded analysis : Failed Substr Comparison handles special chars
    + Upgraded analysis : Identical consecutive omits arrays
    + Checked unit tests : 2757 / 2775 test pass (99% pass). 

**Version 1.2.1 (Fu Yi, 2018-04-02)**

+ Architecture
    + Fixed generation of analysis logs
    + Fixed doctor, which wouldn't diagnostic the absence of needed extensions
+ Report
    + More real-life examples in docs
+ Analysis
    + New favorites : property declaration unique or multiples ? 
    + New analysis : $a = +$b;
    + New analysis for Melis : Regex check and Route constraints
    + Upgraded analysis : Constant used below
    + Checked unit tests : 2760 / 2766 test pass (99% pass). 
+ Tokenizer
    + Fixed counts in property declarations
    + Fixed final new lines in heredoc/nowdoc

**Version 1.2.0 (Xiao Yu, 2018-03-26)**

+ Architecture
    + Upgraded concurrency with analysis
    + Replaced $_SERVER['_'] by PHP_BINARY
    + Removed old code (> 1.0.0)
    + Adopted 'stable' version for progressbar
    + Fixed loading with Bazaar
    + Added support for Parametrized analysis
    + Better initial configuration with doctor
+ Report
    + Ambassador : upgraded analysis settings table
+ Analysis
    + New analysis : Report Private functions for Wordpress
    + New analysis : Suggest simplifying chr(123);
    + New analysis : Too many native calls
    + Updated analysis : fallthrough are not reported with die
    + New Theme : Random
    + Collecting more stats for classes.
    + Checked unit tests : 2758 / 2741 test pass (99% pass). 
+ Tokenizer
    + Upgraded support for Heredoc

**Version 1.1.9 (Qin Qiong, 2018-03-19)**

+ Architecture
    + Better documentation for reports
    + Adding Real Code examples to documentation
    + Refactored Config reading
    + Moved more VCS information to its own class
+ Report
    + Upgraded report : Ambassador reports the number of parameters in methods
    + New report : favorites (spin-off from Ambassador)
    + Upgraded report : Inventories also covers Dateformat, Regex, Sql, Url, Email, Unicode Blocks.
+ Analysis
    + New analysis : too many parameters
    + New analysis : report mass creation of arrays
    + Checked unit tests : 2755 / 2738 test pass (99% pass). 

**Version 1.1.8 (Yuchi Gong, 2018-03-12)**

+ Architecture
    + Reduced cache when running analysis
    + Fixed order of analysis 
+ Report
    + Ambassador : fixed faceted search problems
    + Codacy : added codacy-style report
+ Analysis
    + New analysis : support for IBM db2, leveldb
    + New analysis : should use count's second argument
    + Upgraded analysis : Randomly sorted arrays
    + Checked unit tests : 2749 / 2731 test pass (99% pass). 
+ Tokenizer
    + Fixed edge case where die is an argument
    + Fixed edge case where Yield returns a array

**Version 1.1.7 (Xu Maogong, 2018-03-05)**

+ Architecture
    + Removed most static in Analysis
+ Report
    + New format : All, that produces all reports
    + Ambassador : new report estimates fitting PHP version
    + Ambassador : report enable_dl in configuration
+ Analysis
    + New analysis : report dynamic library loading
    + New analysis : suggest array_fill_keys()
    + New analysis : PHP 7.3 optional last argument
    + New analysis : added support for xxtea, opencensus, varnish, uopz
    + Upgraded BugFixes report to PHP 7.2.3
    + Updated analysis : ext/cairo has new functions
    + Updated analysis : PHP 7.3 new functions
    + Removed analysis : NullCoalesce (double)
    + Checked unit tests : 2743 / 2731 test pass (99% pass). 
+ Tokenizer
    + Moved 'constant' to plugins
    + Fixed bug when updating with HG

**Version 1.1.6 (Wei Zheng, 2018-02-26)**

+ Architecture
    + Created 'First', a recipe of initial analysis
    + Prepared installation for compose
+ Report
    + Restored 'INLINE' results 
    + New reports : Stats
    + Collect PHP native function cool
+ Analysis
    + New analysis : report suggest compact instead of array
    + New analysis : list with references (PHP 7.3+)
    + New analysis : report situation where check is done on non-cast value
    + New analysis : foreach( $array as $o -> $v) as error prone
    + Handle cases where PHP regex are not compilable anyway
    + Checked unit tests : 2732 / 2722 test pass (99% pass). 
+ Tokenizer
    + Propagate constant concatenation values.
    + Fixed calculation of intval
    + Refactored Configuration readers
    + Fixed bug when calculating __METHOD__

**Version 1.1.5 (Li Shimin, 2018-02-19)**

+ Architecture
    + Refactored all reports
    + Removed outdated Devoops report
+ Report
    + Upgraded BugFixes report to PHP 7.2.2
    + Ambassador : generates a list of confusing variables
    + New report : OWASP
+ Analysis
    + New analysis : Use Math
    + New analysis : Extensions ext/hrtime
    + New analysis : Possible Infinite Loops
    + Upgraded analysis : addZero, Multiply by one supports new situations
    + Upgraded analysis : added microtime, uniqid .. to better rand.
    + Checked unit tests : 2719 / 2724 test pass (99% pass). 
+ Tokenizer
    + Fixed check on script compilation that was too strict.
    + Fixed internal assert() 
    + Exported VCS to separate classes
    + Refactored load with 3 separate plugins : intval, noDelimiter, booval

**Version 1.1.4 (The Great White Turle, 2018-02-12)**

+ Architecture
    + Build concatenation values in scalar constante expression.
    + Upgraded export of file dependencies values
+ Report
    + Ambassador : fixed duration of audit.
    + Composer : provides a full list of depend extensions
+ Analysis
    + New analysis : Report useless catch
    + New analysis : suggest using array_search / array_keys instead of foreach
    + New analysis : double array_flip is slow
    + New analysis : Suggest using cached values
    + New analysis : Functions that fallback to global namespace
    + Upgraded analysis : Encoded letters supports leading 0 in unicode codepoint
    + Upgraded analysis : Variable strange names now report 3 identical consecutive letters
    + Upgraded analysis : Upgraded support to __dir__
    + Checked unit tests : 2716 / 2711 test pass (99% pass). 
+ Tokenizer
    + Fixed definitions link for functions

**Version 1.1.3 (The fairy Su'e, 2018-02-05)**

+ Report
    + Fixed Ambassador : the favorites weren't displayed. 
+ Analysis
    + New analysis : Report useless references
    + New analysis : Melis configuration : Undefined configuration array
    + New analysis : Melis configuration : make string.
    + Upgraded analysis : Parent first
    + Checked unit tests : 2700 / 2695 test pass (99% pass). 
+ Tokenizer
    + Better handling of Labels. 
    + Fixed edge case where class and constants where mistaken one for the other

**Version 1.1.2 (Jade Rabbit Spirit, 2018-01-29)**

+ Architecture
    + Upgraded docs to tinkergraph 3.2.7
+ Analysis
    + New analysis : Report missing included files
    + New analysis : ZF3 : No Echo Outside a View.
    + New analysis : Local Global variable : report variable that looks global but are not
    + Upgraded analysis : Directive names are check with case sensitive analysis
    + Checked unit tests : 2687 / 2693 test pass (99% pass). 
+ Tokenizer
    + Magic Constant hold their actual value
    + Fixed Fullnspath for constants (case sensitive)
    + Fixed edge case with exit and die
    + Fixed edge case with exit and die and -1

**Version 1.1.1 (Wood Xie of Dipper, 2018-01-22)**

+ Architecture
    + Fixed path when calling exakat from outside its install folder
    + First analysis for Melis Framework
    + Optimized dictionary collection
+ Report
    + Ambassador : upgraded graph for class sizes
+ Analysis
    + New analysis : report case problems with includes
    + New analysis : Melis framework
    + New analysis : inventory of view properties for Zend Framework
    + New analysis : report view files for Zend Framework
    + Upgraded analysis : + is accepted as regex delimiter
    + Upgraded analysis : same condition searches inside blocks
    + Checked unit tests : 2665 / 2671 test pass (99% pass). 
+ Tokenizer
    + Magic constants __DIR__ and __FILE__ get their actual value in noDelimiter
    + Created Eval atom
    + Removed 'Name' token for echo, print, die, exit.
    + Upgraded handling of constant names inside strings
    + Removed a bug when storing dictionary.

**Version 1.1.0 (Wood Dragon of Horn, 2018-01-15)**

+ Architecture
    + Replaced 'code' property with a dictionary
+ Tokenizer
    + Introduced 'Magicmethod' for Magic methods in class
    + Fixed a bug when ' is in file path
    + Fixed a bug when several raw HTML are in a PHP script.
 
Version 1.0.11 (Wood Dragon of Well, 2018-01-08)
+ Architecture
    + Added assertion for property name.
+ Report
    + Ambassador : Added report of classes's size.
    + Fixed missing audit end's time. 
+ Analysis
    + New analysis : Sqlite3 doesn't escape " 
    + Upgraded analysis : Strange names also report qqqq sequences in variable names
    + Checked unit tests : 2617 / 2657 test pass (99% pass). 
+ Tokenizer
    + Fixed fullnspath handling for constants (case insensitive for the constant name)
 
Version 1.0.10 (Wood Wolf of Legs, 2018-01-01)
+ Architecture
    + Fixed Sqlite3 escaping error : use ', not "
+ Report
    + 
+ Analysis
    + Upgraded analysis : ? is possible as delimiter
    + Analysis works better with nested structures
    + Checked unit tests : 2601 / 2649 test pass (99% pass). 
+ Tokenizer
    + First plugin for Load Task.
    + Upgraded support for define-d constant.
    + Introduced Phpvariable
    + Fixed scoping with array index.
 
**Version 1.0.9 (King of Dust Protection, 2017-12-25)**

+ Report
    + Ambassador : list complex expressions.
    + Dump : added function inventory
    + Dump : added begin and end line for structures.
+ Analysis
    + New analysis : report reference error with Ternary operator
    + New analysis : report Undefined classes in Wordpress.
    + Upgraded analysis : preg option E, tighter regex.
+ Tokenizer
    + Better handling of long path name. TBC.
    + Introduced Parent, Static, Self, Exit, Echo, Print.
 
**Version 1.0.8 (King of Heat Protection, 2017-12-18)**

+ Architecture
    + Doctor reports memory_limit and JAVA_OPTIONS/JAVA_HOME
    + Made database restart more portable 
    + Added spell checking on docs
+ Report
    + Ambassador : Regex inventory added
    + Ambassador : Largest expressions reported
+ Analysis
    + New analysis : report identical operands on both sides of operator
    + New analysis : report potentially mistaken concatenation in array
    + New analysis : report mistaken scalar typehint
    + New analysis : report undefined classes by symfony version
    + New analysis : report undefined classes by wordpress version
    + Upgraded analysis : Interfaces are also reported from return typehint
    + Upgraded analysis : Mistaken concatenation got rid of various false-positives
    + Checked unit tests : 2601 / 2633 test pass (99% pass). 
+ Tokenizer
    + Isset, Empty, Phpvariables now have their own atom.
    + Fixed edge case with $ token
    + Fixed Constant fqn building
    + UTF-8 protection for propertyname

**Version 1.0.7 (King of Heat Protection, 2017-12-11)**

+ Architecture
    + Added /var to default omitted folders
+ Analysis
    + New analysis : should use array_filter.
    + New analysis : ext/igbinary
    + Checked unit tests : 2533 / 2599 test pass (97% pass). 
+ Tokenizer
    + Fixed 
 
**Version 1.0.6 (Fuli, 2017-12-04)**

+ Architecture
    + Refactored description
    + Moved PHPsyntax to a function
+ Analysis
    + New analysis : Never used parameter.
    + New analysis : always use named boolean parameters
    + Upgraded analysis : unused arguments
    + Checked unit tests : 2573 / 2585 test pass (99% pass). 
+ Tokenizer
    + Added new token : This for $this
    + Updated loader to handle PHP 7.3 functioncall syntax (final ,)
    + Turned Markcallable into an independant analysis

**Version 1.0.5 (King of Cold Protection, 2017-11-27)**

+ Architecture
    + Configured Exakat for Tinkergraph 3.3. Still unfinished.
    + Documentation now has an external link to extensions. 
+ Report
    + Ambassador : added more inventories : URL SQL, email, GET index, MD5, Mime
+ Analysis
    + New analysis : parent first
    + New analysis : Report uncommon Environment Vars
    + New analysis : Report invalid Regex
    + New analysis : Report contatenation in Zend DB
    + Fixed analysis : Deprecated Functions
    + Fixed analysis : Unknown PCRE2 option 
    + Upgraded analysis : hardcoded password
    + Upgraded analysis : array_merge in loops 
    + Upgraded analysis : substr() first. Handle following expressions
    + Refactored analysis : Used Functions
    + Refactored analysis : Add Zero
    + Checked unit tests : 2573 / 2585 test pass (99% pass). 
+ Tokenizer
    + Fixed a bug that linked functions and definitions

**Version 1.0.4 (Boxiang Demon, 2017-11-20)**

+ Architecture
    + PhpExec, get only path to binary.
    + Cleaned docs of double links
    + Cleaned code
+ Report
    + Added libsodium, Argon2 to Crypto; DL() usage to PHP.
    + Compatibility report only focuses on backward incompatibilities.
    + New recipes will cover 'suggestions for better code'. Coming up. 
+ Analysis
    + New analysis : " string is better than ' (sorry...)
    + New analysis : PHP 7.3's PCRE 2 
    + New analysis : report missing 'new' in front of class name.
    + New analysis : use is_object instead of is_resource for ext/hash
    + New analysis : report non-countable calls
    + New analysis : report DL usage in Appinfo
    + New analysis : slice first, then map arrays. 
    + New analysis : Avoid 5th argument in PHP 7.2 for set_error_handler
    + New analysis : avoid null with get_class()
    + New analysis : suggest using list() with foreach instead of arrays
    + New analysis : avoid using $this as argument in constructor
    + New analysis : Report usage of ext/vips
    + New inventory : GPC variables
    + Updated analysis : Use Class Operator doesn't report methods names anymore
    + Updated analysis : Long argument size is raised to 60 chars
    + Updated analysis : ignore when missing break is in last case
    + Updated analysis : Use This ignores 'self'.
    + Updated analysis : Randomly sorted Arrays ignores arrays of 3 or less.
    + Updated analysis : ext/mcrypt gets its constants
    + Updated analysis : more strange names being used in code
    + Updated analysis : more PHP 7.2 removed functions
    + Checked unit tests : 2563 / 2572 test pass (99% pass). 
+ Tokenizer
    + Reduced duplicated that may lead to loading error. 

**Version 1.0.3 (Baize Demon, 2017-11-13)**

+ Architecture
    + Fixed driver Tinkergraph, which was not setting the right ids.
    + Doctor now reports $JAVA_OPTIONS, in case one need to allocate more memory
    + Doctor now reports token limit
    + Moved config.ini creation to first phase of init.
    + Fixed collect of error when init with git.
    + Upgraded driver gremlin-php to 3.0.2
+ Report
    + Ambassador : Now reports the namespaces as a tree.
    + New analysis : report members that are static and not. 
    + Updated analyzis : normal method called statically.
+ Analysis
    + Added support for Drupal, FuelPHP and Phalcon.

**Version 1.0.2 (Suanni Demon, 2017-11-06)**

+ Architecture
    + Better report of error messages from VCS.
    + Updated support for Vagrant 
+ Report
    + Ambassador : Fixed display for 'Callback'
+ Analysis
    + New analysis : substr() first, then replace.
    + New analysis : report double prepare (WP).
    + New analysis : avoir the +1 month trap
    + New analysis : check for printf() options
    + New analysis : check for placeholder in prepare (WP)
    + New analysis : avoid direct injection into prepare (WP)
    + New analysis : performance recommendation for switch. 
    + New analysis : merge if/if into if/then/else
    + Checked unit tests : 2500 / 2536 test pass (99% pass). 

**Version 1.0.1 (Xueshi Demon, 2017-10-30)**

+ Architecture
    + Created Result class for Graphdb results
    + Docker image is updated with version 1.0.1
    + Vagrant files are updated with version 1.0.1
    + Preparing support for Gremlin 3.3.0
+ Report
    + Added support for PHP 7.1.11 and 7.0.25
+ Analysis
    + New analysis : could be else (for consecutive opposite if/then)
    + Checked unit tests : 2517 / 2527 test pass (99% pass). 

**Version 1.0.0 (Roushi Demon, 2017-10-23)**

+ Architecture
    + Tested on Gremlin 3.2.6. Checked Gremlin 3.3.0, but it needs more work.
    + Upgraded doctor for installation and report.
    + Upgraded docs to set gremlin-server as default install.
+ Report
    + Added support for Clang-style report.
    + Ambassador : fixed link to exception Tree.
    + Inventories : Date format, 
    + Audit names are reported in every Ambassador-style report. 
+ Analysis
    + Upgraded PHP directive list.
    + Functions In For loop : prevent issue if the function uses a loop variable.
    + Useless instruction : do not report return $i++ if $i is reference
    + Useless instruction : Avoir reporting properties when they are magic
    + New analysis : mark properties to be magic.
    + Upgraded list of PHP logins, to report hard coded passwords.
    + Upgraded close naming : variables that differ with 1 chars are reported.
    + Added assert(false...) to list of branching syntax.
    + Checked unit tests : 2515 / 2525 test pass (99% pass). 

Version 0.12.16 (Tawny Lion Demon, 2017-10-16)
+ Report
    + Beta version for Drill Instructor
    + Upgraded Inventories report with Sessions, Cookies, Incoming variables
+ Analysis
    + New analysis : Expression too complex.
    + New analysis : Session Handler must implements SessionUpdateTimestampHandlerInterface
    + New analysis : is Zero : additions that negate some terms
    + New analysis : unconditional loops
    + Upgraded Zend Framework review with latest versions (feed, http, eventmanager...)
    + Upgraded 'Strange names' with new typos
    + Upgraded 'Logical to in_array' to handle separated comparisons
    + Checked unit tests : 2505 / 2515 test pass (99% pass). 
+ Tokenizer
    + Fixed bug with Sign in Additions.

Version 0.12.15 (Nine Headed Lion, 2017-10-09)
+ Architecture
    + Server : now supports stop, start and restart.
    + Every audit gets a random name, for easy differentiation
    + Added support for PHP 7.3
+ Report
    + Ambassador : list of analysis that report nothing : Good job! 
    + Slim report : fixed build
+ Analysis
    + New analysis : file upload names vulnerability check
    + New analysis : variable that may hold different types of date
    + New analysis : always anchor regex
    + Checked unit tests : 2475 / 2480 test pass (99% pass). 

Version 0.12.14 (Grand Saint of Nine Spirits, 2017-10-02)
+ Architecture
    + Support UTF-8 on Gremlin Server (other encoding are not)
    + Better display of vcs updates
+ Report
    + Ambassador : added Security and Performances
    + Ambassador : Upgraded exception presentation
+ Analysis
    + New analysis : report fallthrough in switch
    + New analysis : inventory regex 
    + Added support for PHP 7.1.10 and 7.0.24

Version 0.12.13 (King of the Southern Hill, 2017-09-25)
+ Architecture
    + Code cleaning
+ Report
    + Ambassador : changed display of the audit
+ Analysis
    + Refactored several analysis

Version 0.12.12 (Ruler of the Kingdom of Miefa, 2017-09-18)
+ Report
    + Ambassador : fixed collect of interfaces and trait names
+ Analysis
    + New analysis : ext/Parle
    + New analysis : help optimize pathinfo() usage
    + New analysis : catch array_values() usage with list and pathinfo()
    + Updated analysis : Don't show error messages with catch->getMessage();
    + Updated analysis : No concat in loop handles $x = $c . $x;
    + Checked unit tests : 2456 / 2461 test pass (99% pass). 
+ Tokenizer
    + Added support for ', " and > in file names. Still missing support for \
    + Restaured fallback to global constants.
    + Fixed special case : <?php ++$x ?>

Version 0.12.11 (Half-Guanyin, 2017-09-11)
+ Architecture
    + Added support options for branches and tags
    + Added support for config in server mode
+ Report
    + Fixed methods dump for interfaces.
+ Analysis
    + Added all analysis to report could be private/protected for 
+ Tokenizer
    + Fixed handling of '<' char in paths

Version 0.12.10 (Golden Nosed Albino Rat Spirit, 2017-09-04)
+ Architecture
    + Upgraded server version with config alteration features.
    + New generated config-cache
+ Report
    + Fixed property names in Visibility report
+ Analysis
    + Arrays/IsModified : arrays are not modified unless in a (unset)
+ Tokenizer
    + Fixed 'constant' for functioncalls
    + Introduced 'Name' for Identifier without a fullnspath
    + Added support for branches and tags in init
    + Fixed edge case with $o->$$b

Version 0.12.9 (Lady Earth Flow, 2017-08-28)
+ Architecture
    + Creates config.cache, with cached calculated configs. Remove to update.
+ Report
    + GraphQL : Upgraded GraphQL report, with relationships.
+ Analysis
    + New analysis : suggest moving for() to foreach()
    + New analysis : shell_exec/exec/`backtick` favorite
    + Update analysis : Abstract Static is for PHP 7.0-
+ Tokenizer
    + Removed Arguments and ARGUMENTS. 
    + Finished 'factory' from Config.
    + Better handling of long path names.

Version 0.12.8 (ruler of the Kingdom of Biqiu, 2017-08-21)
+ Analysis
    + New analysis : use foreach, not for()
    + New analysis : ext/fam, ext/rdkafka
+ Tokenizer
    + Fixed edge case where pathnames are too long on OSX.

Version 0.12.7 (Old Man of the South Pole, 2017-08-14)
+ Architecture
    + Fixed project_vcs when none is used.
+ Analysis
    + Better documentation for in_array replacements and array_unique()
    + Added support for PHP 7.1.8 and 7.0.22

Version 0.12.6 (White Faced Vixen Spirit, 2017-08-07)
+ Analysis
    + New analysis : no negative for strings before 7.1
    + New analysis : use in_array instead of ||
    + Updated analysis : preg_quote has no delimiter
+ Tokenizer
    + Fixed bug in handling real value for negative numbers

Version 0.12.5 (White Deer Spirit, 2017-07-31)
+ Architecture
    + Removed config singleton
+ Report
    + New report : simpletables (HTML)
+ Analysis
    + New analysis : report optional parameters
    + New analysis : report concat inside a loop
    + Updated analysis : Could Be Class Constant, when no visibility is provided.

Version 0.12.4 (peacock Mahamayuri, 2017-07-24)
+ Architecture
    + Optimized performances for large projects (over 2M tokens)
    + Support Neo4j as a driver for Tinkgerpop
+ Report
    + Now covering all PHP 7.2 features
+ Analysis
    + New analysis : Extension xattr
    + New analysis : report 'object' as a class name
    + New analysis : No Array for magic property
    + New analysis : suggest reducing code for isset
    + New favorite : and / &&
    + Updated analysis : fetch correct delimiter, even if escaped.
    + Extended coverage for several analysis
    + Removed several nested-subqueries (bad for performances)
+ Tokenizer
    + Tinkergraph/Neo4j : reworked loading data from disk.
    + Added protection for $ in filename

Version 0.12.3 (Golden Winged Great Peng, 2017-07-17)
+ Architecture
    + Prepared options for several back servers : Tinkergraph, Gremlin-Server/Neo4j, Janusgraph
+ Report
    + New report : Marmelab (GraphQL server)
+ Analysis
    + New analysis : Report when a property is used as object or scalar
    + New analysis : Mismatched Typehint 
    + New analysis : Mismatched Default values 
    + Upgraded analysis : 
    + Fixed a gremlin bug in noAtomInside
+ Tokenizer
    + Added support for trailing comma in group use (PHP 7.2)
    + Fixed building of constants' values

Version 0.12.2 (Samantabhadra, 2017-07-10)
+ Architecture
    + Added support for Tinkergraph as graph backend
+ Report
    + Ambassador : reports callback/closures, all 3 declares (ticks, encoding, strict_types)
    + Ambassador : reports strict_types as favorite
    + PlantUML : upgraded report
+ Analysis
    + New analysis : Mismatched ternary branches
    + New analysis : mkdir, by default, uses 777. 
    + New analysis : ext/lapack
    + Upgraded analysis : option E for preg_match, refined results
    + Checked unit tests : 2337 / 2366 test pass (99% pass). 
+ Tokenizer
    + Added support for Instanceof and GROUPUSE with Nsname

Version 0.12.1 (Yellow Toothed Elephant, 2017-07-03)
+ Architecture
    + Refactored structures extractions in dump
+ Report
    + New report : PlantUML
    + Ambassador : Appinfo now reports how popular is a feature
+ Analysis
    + New analysis : Const / Define() favorite for constants
    + New analysis : do not return in finally
    + Upgraded analysis : Add Zero was refactored
+ Tokenizer
    + Prepared list of tokens and relations

Version 0.12.0 (Manjusri, 2017-06-26)
+ Architecture
    + Added support for Janusgraph (Gremlin 3)
    + Refactored dump's data collection for speed.bb
+ Report
    + Added support for Wordpress and Joomla as Frameworks
+ Analysis
    + New analysis : Avoid Optional properties
    + New analysis : Multiple declarations of functions
    + New analysis : Non breakable spaces in names
    + New analysis : Favorite Heredoc delimiter
    + New analysis : ext/swoole
+ Tokenizer
    + Modified several nodes/links names, for compatibility purposes

Version 0.11.8 (Xiaozuanfeng, 2017-06-19)
+ Architecture
    + Starte working on JanusGraph to add to Neo4j/Gremlin3
+ Report
    + Ambassador : reports Strings encoding and Unicode-block (when available)
    + Ambassador : reports framework founds (first 6, more as we go).
    + Ambassador : reports how frequently an analysis yield results to compare with current situation
+ Analysis
    + New analysis : Classes where declaration order differs from : use, const, properties and methods.
    + New analysis : Could use interface (but implements is missing)
    + New analysis : Cant Inherit Abstract Method (PHP 7.2 upgrade)
    + New analysis : use session_start() options
    + Updated analysis : Dynamica method calls cover {} too
    + Checked unit tests : 2305 / 2305 test pass (100% pass). 
+ Tokenizer
    + Checked code on early PHP 7.2 version

Version 0.11.7 (Long Armed Ape Monkey, 2017-06-12)
+ Report
    + Ambassador : report detected patterns (2 firsts)
    + None report : for when dump is sufficient
+ Analysis
    + New analysis : could factor functioncalls
    + New analysis : PSR-* usage
    + New analysis : support for Judy and Gender extensions
    + Added thema for Compatibility PHP 7.3
    + Added thema for Dependency Injection 
+ Tokenizer
    + Fixed edge case where classes starting with 'namespace' where mistakenly processed
    + Removed Block from CIT 

Version 0.11.6 (Red Bottomed Horse Monkey, 2017-06-05)
+ Architecture
    + Removed singleton to Config. WIP
+ Report
    + Ambassador : reports usage of PSR 3,6,7,11,13,16.
    + UML : report now protects file names
+ Analysis
    + New analysis : Ext stats
    + New analysis : report mixed concatenation / interpolation strings
    + Updated analysis : htmlentities actually uses combinaison, not alternatives, 
    + Updated analysis : Close Tag consistency ignores __HALT_COMPILER files

Version 0.11.5 (Intelligent Stone Monkey, 2017-05-30)
+ Report
    + Ambassador : fixed visibility suggestion
    + New report : Dependency wheel
+ Analysis
    + New analysis : avoid typehinting with classes
    + New analysis : implemented methods must be public
    + New analysis : no reference on left of assignement
    + New analysis : Could typehint with instanceof
    + Updated analysis : Useless parenthesis cover clone, yield, yield from.
    + Updated analysis : Make One Call also reports nested calls
+ Tokenizer
    + Split functions and closures, 
    + Split classes and anonymous classes
    + Split variable with definitions (Property, Static and Global)
    + File count is always reported (even 0)
 
Version 0.11.4 (Six Eared Macaque, 2017-05-22)
+ Architecture
    + Results : returns now multiple results at once
+ Report
    + New report : codeflower
    + Ambassador : report usage of Debug functions, browscap
    + Ambassador : omits 0 in donuts
    + Ambassador : faceted search for compatiblity
+ Analysis
    + New analysis : report functions whose return is not used
    + New analysis : only variable can be passed by reference
    + Added limits to all in-depth searches
    + Checked unit tests : 2216 / 2216 test pass (100% pass). 
+ Tokenizer
    + Fixed edge case, where return is finished by a close tag
    + Split Variables into Variables, Objects and Arrays.

Version 0.11.3 (Sun Deity of Mao, 2017-05-15)
+ Architecture
    + Speed up batch processing for lists of analysis
    + Split data collection from the initial dump.
+ Report
    + Ambassador : Upgraded presentation of issues, and internals links.
+ Analysis
    + New analysis : Sphinx extension
    + New analysis : GRPC extension
    + New analysis : reports arrays that are randomly sorted.
    + New analysis : report multiple catch clauses
    + Updated analysis : direct injections include all SERVER_* values
    + Upgrade for PHP 7.1.15 and 7.0.19
+ Tokenizer
    + Split Functioncall into Functioncall, MethocallCall and Newcall. 
    + Added support for 'namespace' in any full name.

Version 0.11.2 (Scorpion Demon, 2017-05-08)
+ Architecture
    + Code cleaning, and more stability
+ Analysis
    + New analysis : Report preference between != and <>
    + New analysis : report empty regex and wrong delimiters
    + Added protection for $ in RegexDelimiters 

Version 0.11.1 (Ruler of Women's Country, 2017-05-01)
+ Architecture
    + Fixed handling for large list of data in gremlin queries
    + Handles static in anonymous classes correctly
+ Report
    + Reports handle traits like class.
+ Analysis
    + New analysis : ends arrays with , or not (favorite)
    + New analysis : suspicious comparison 
    + New analysis : strange spaces in strings
+ Tokenizer
    + Arrays are now Arrayliteral, split from Functioncall

Version 0.11.0 (Immortal Ruyi, 2017-04-24)
+ Architecture
    + Removed prepared statements from loops in dump
    + made Gremlin cache compatible with 32bits platforms
+ Report
    + Ambassador : first work on upgrading visibilities for properties.
+ Analysis
    + New analysis : could use str_repeat()
    + New analysis : Crc32() Might Be Negative
    + Update analysis : Queries in loop reports cubrid and sqlsrv, prepared statements.
    + Update analysis : type mismatch for indices works on constants too.
    + Update analysis : Loop calling covers less ground
+ Tokenizer
    + Split function and method entities for differentiated processing

Version 0.10.9 (Single Horned Rhinoceros King, 2017-04-17)
+ Architecture
    + File extensions are processed before include/ignore dirs.
    + Reduced number of DEFINITION links, leading to less processing.
    + Added several assertion() in the code
    + Added assertions report in doctor (better leave them out with phar)
+ Report
    + Added support for PHP 7.0.18 and 7.1.4
    + Ambassador : better layout for favorites
    + Zend Framework : 8 new components supported
    + Zend Framework : now supports zendframework/zendframework too
    + Zend Framework : report unused components 
+ Analysis
    + New analysis : report nested Use expressions
    + New analysis : report repeated regex (to be federated)
    + New analysis : report code that output directly to std
    + Updated analysis : Should use this now omits overwritten methods
    + New analysis : report overwritten methods
    + Upgraded analysis : 2123 / 2123 test pass (100% pass)

Version 0.10.8 (King of Spiritual Touch, 2017-04-10)
+ Report
    + Slim report : list of routes used. 
+ Analysis
    + New analysis : report Group Use Declaration (PHP 7.0+)
    + Zend Framework : 30 components are now covered. 
    + Slim : No echo in route callable and Inventory of routes.
    + PHP : list of new PHP 7.2 functions.
+ Tokenizer
    + Sped up loading time by 10%. 
    + Added support for PHP6 binary string : $a = u'b';

Version 0.10.7 (Immortal of Antelope Power, 2017-04-03)
+ Report
    + Ambassador : fixed composer report.
    + Added report for Composer (beta phase)
    + Added report for Slim framework.
+ Analysis
    + Added support for Slim versions.
    + Added 10 new components for Zend Framework 3
+ Tokenizer
    + Fixed support for $ in file names.

Version 0.10.6 (Immortal of Elk Power, 2017-03-27)
+ Architecture
    + Major speed up of loading and analysis
    + Fixed themes configuration.
+ Report
    + Ambassador : report cookies usage, infinite and NAN usage
    + Zend Framework : Report incompatibilites component/version for ZF3
+ Analysis
    + Upgraded analysis : 1941 / 1941 test pass (100.00% pass)
    + New analysis : Zend Framework 3 Deprecated 
    + New analysis : Zend cache, view, db.
    + New analysis : Report missing type tests.
    + New analysis : suggest setcookie() with safe arguments
    + New analysis : Do not cast to Int
    + New analysis : CakePHP classes compatibilities from 2.5 to 3.3
    + Upgraded analysis : instanceof doesn't report traits anymore
    + Upgraded analysis : mb_ereg has options in the 4th arguments
    + Upgraded analysis : more strange names 
+ Tokenizer
    + Reviewed most of the load processing.
    + Reduced the number of 'fullnspath' properties.

Version 0.10.5 (Immortal of Tiger Power, 2017-03-13)
+ Architecture
    + Collect graph size in dump.sqlite
    + Collect memory usage in dump.sqlite
    + Now uses the calling PHP version to run all parts of exakat (no config)
    + Doctor report the ran gremlin version. 
+ Report
    + Ported the Zend Framework report to ambassador
    + Added regex delimiter in favorites.
    + Ambassador : syntax coloring 
+ Analysis
    + New analysis : could be typehinted 'callable'
    + New analysis : encoded letters in strings for security
    + New analysis : report arguments that may be callable
    + New analysis : report strangely named variables
    + New analysis : report strangely named constants
    + New analysis : too many FindsBy*() methods
    + Updated analysis : Useless Instructions doesn't report array_merge(_recursive) with one argument
    + Updated analysis : array_replace handles ... 
    + Updated analysis : 7.2 deprecation with assert()
    + Generalized usage of commons for CIT
    + Added first 4 set of analysis for Zend Framework 3
    + Added support for dynamic new $a[i];
+ Tokenizer
    + Fixed fullnspath with new on functioncall
    + Reduced the number of fullnspath loaded
    + Added support for 's'() as functioncall
    + Fixed case where file names has ' ' in it
    
Version 0.10.4 (Dragon King of the West Sea, 2017-03-06)
+ Architecture
    + Ignore some classic files by default (README, LICENSE...)
+ Report
    + Ambassador : protection of HTML values
    + PHPcompilation : fixed export to stdout
+ Analysis
    + New analysis : report useless else branches
    + New analysis : should regenerate session Id, for PHP and Zend Framework
    + Added support for Extension Data structures (ext/ds)
    + Upgraded analysis : Hardcoded Hash
    + Speed up analysis for extensions
+ Tokenizer
    + Fixed edge case where a constant was used inside a ternary operator
    + Fixed processing of labels
    
Version 0.10.3 (Dragon King of the Jing River, 2017-02-27)
+ Architecture
    + Added URL glossary to Manual.
    + Extended CS ruleset
    + Use exakat/exakat as user/login for git. 
    + New helper to rename analysis
    + Project command now accept -P/-T to run one analysis/Thema directly
+ Report
    + New report style : Codesniffer
+ Analysis
    + New analysis : suggest usage for array_column()
    + New analysis : __DIR__ must be concatenated with a string starting with '/'
    + New analysis : report usage of parent, self and static outside a class/trait
    + New analysis : report properties used only in one method
    + New analysis : report properties used only once at all
    + New analysis : multiple aliases per class
    + Updated analysis : Fopen() mode support 'e' option (7.1.2 + )
    + Updated analysis : Make One Call covers str_replace, substr_replace, preg_replace*
    + Updated analysis : Unused arguments : now ignores arguments from interface or parent
+ Tokenizer
    + Removed double DEFINITION link. Faster loading, less processing.
    + Fixed an edge case when function name is boolean or null.
    + Cleaned atom and tokens names
    + Fixed edge case when object is instantiated in a ternary
    
Version 0.10.2 (Water Lizard Dragon, 2017-02-20)
+ Architecture
    + 
+ Report
    + Text format now understand -T, -P to extract only some of the results.
    + Fixed dump of extends. 
+ Analysis
    + Added support for PHP 7.1.2 and PHP 7.0.16
    + New analysis : report forgotten 'throw' keyword.
    + New analysis : report class / function confusing name
    + Added support for libsodium
    + Upgraded PHP Relaxed Keyword : Ignore properties.
    + Upgraded analysis : 1824 / 1826 test pass (99.9% pass)
+ Tokenizer
    + Fixed a bug that mistakes native PHP classes for functions
    + Fixed rare situation with grouped const/function.
    
Version 0.10.1 (King of Wuji Kingdom, 2017-02-13)
+ Architecture
    + Report SVN revision when updating or not.
    + Default reports are in config.
    + Configure now supports include_dirs, to include files.
    + Project name is now noted in datastore.
    + Inventories is a default themas; PHP Compatibility < 5.6 are not default anymore.
+ Documentation
    + Fixed outgoing links
    + Better coverage of PHP functions
+ Report
    + Added 'Inventories' report : reports all names and literals
    + Ambassador : Added list of included files, Yield From and classes stats
+ Analysis
    + New Analysis : Strange Names For Methods (Classes/StrangeName)
    + New Analysis : SQL queries (Type/Sql)
    + New Analysis : Avoid Non Wordpress Globals (Wordpress/AvoidOtherGlobals)
    + Upgraded analysis : Should be single quote, escape sequences refined.
    + Upgraded analysis : Should Preprocess now support determinist PHP functions
    + Upgraded analysis : 1817 / 1824 test pass (99.6% pass)
+ Tokenizer
    + Fixed LOC counting.
    + Fixed edge case when closure is directly use as argument
    + Fixed double inventories for Use's Definitions
    
Version 0.10.0 (Azure Lion, 2017-02-06)
+ Architecture
    + Replacement of booleans with constants (WIP)
    + Removed PHPloc (merged features into load)
    + Added coding standard for Code Sniffer (ruleset.xml)
    + PHP version used default to running script version
    + Now reading Token Constants from the binaries
    + Doctor reports project configuration if -p is used
+ Report
    + 
+ Analysis
    + New Analysis : No Boolean As Default 
    + New Analysis : Raised Access Level 
    + New Analysis : Recommend Wpdb->prepare when variables are in query
    + Directive suggestion now include error_log
    + Upgraded analysis : UselessParenthesis also checks Typehint
    + Upgraded analysis : 1804 / 1811 test pass (99.6% pass)
+ Tokenizer
    + Reinforced detection of parsable PHP script
    + Fixed Files command : it now cleans data before running
    + Removed warning about memory
    + Index creation made lighter

Version 0.9.9 (Pilanpo Bodhisattva, 2017/01/30)
+ Architecture
    + Moving true/false to constants
+ Report
    + Ambassador : Added 'Compilation' and Version compatibility reports.
    + Prepared collection of dependencies in dump
+ Analysis
    + New Thema : Compatibility PHP 7.2
    + New analysis : Deprecated Features of PHP 7.2
    + New analysis : Removed Function for PHP 7.2
    + New preference : New Line Style
    + Upgraded analysis : 1781 / 1802 test pass (98.9% pass)

**Version 0.9.8 (Multiple Eyed Creature, 2017-01-23)**

+ Architecture
    + Moved 'Truthy/Falsy' as 'boolean' characteristics
    + Updated Gremlin3 interface to handle Groovy maps
    + Added default name when creating project
+ Report
    + Added checks on merged table at Dump stage
    + Added support for PHP 7.1.1 and 7.0.15
+ Analysis
    + New analysis : variables assigned twice or more
    + New preference : new x() / new x;
    + Upgraded analysis : 1785 / 1794 test pass (99.5% pass)
    + Fixed Interface usage : missing interfaces extends interfaces
    + Added extra check for Functioncalls
+ Tokenizer
    + Added support for instanceof + several names

**Version 0.9.7 (Hundred Eyed Demon Lord, 2017-01-16)**

+ Architecture
    + Fixed constant names for tokens in Load
    + Changed duplication check to dedup(). Cleaned analysis for duplicates.
    + Speed but for large projects. Work in Progress. 
    + Reduced usage of static properties
    + Better detection of PHP scripts during project
+ Report
    + Fixed generation of inventories when no target is provided
+ Analysis
    + New analysis : Could Be Protected Property (not a public)
    + New analysis : avoid large literal arrays in local variables. 
    + New analysis : report long arguments. 
    + Removed analysis : Structures/EchoArguments (double with Echo With Concat)
+ Tokenizer
    + Fixed list of constants for PHP 7.1

**Version 0.9.6 (Spider Demons, 2017-01-09)**

+ Architecture
    + Added support for report/analysis theme list in config (exakat and project)
    + Better cleaning of projects
    + Doctor : Initialisation with themes/reports; Reports executable being used.
    + Added a log for gremlin Queries
    + Rebuild the server command
    + Added 'catalog' command
+ Report
    + Split Phpconfiguration into eponymous and Phpcompilation
+ Analysis
    + New analysis : avoid Glob, use scandir without sorting.
    + New analysis : always configure ext/sqlite3 FetchRow()
    + New analysis : no string with append
    + Removed analysis : Structures/ForeachSourcesNotVariable
    + Upgraded Analysis 'Should Import Functions'
    + Upgraded analysis : 1764 / 1773 test pass (99.5% pass). 
+ Tokenizer
    + Added 'aliased' property to nodes.

**Version 0.9.5 (Immortal Ziyang, 2017-01-04)**

+ Architecture
    + Better check of PHP version 
+ Report
    + Ambassador : report analysis settings
    + PHP Compilations : supports all extensions
    + New report : Inventories
+ Analysis
    + New analysis : Don't Use Fallback to Global space
    + New analysis : MongoDB (ext/mongo version 3)
    + New analysis : zbarcode 
    + Bug : Fixed intval for octals in Arrays/MultipleIdenticalKeys
    + Removed analysis : Php/InconsistantClosingTag (double)
+ Tokenizer
    + Ranking arguments, not functioncall

**Version 0.9.4 (Lady of Jinsheng Palace, 2016-12-19)**

+ Architecture
    + Rewrote the concurrence check (removed needs for ext/sem)
    + Results are never double anymore
    + Upgraded gremlin calls, to handle \n
    + Dump cleans the previous values before dumping
    + Excluded namespaces classes when searching for external libraries
+ Report
    + Ambassador : extension usage, inventories, global lists, stats, PHP Compilation directives
    + Covers more compilation directives (Not finished)
+ Analysis
    + New analysis : Final by Ocramius
    + Upgraded : Comparison with == : added curl_exec
    + Upgraded : isset with constant (mistake on properties as arrays)
    + Upgraded : Avoid using now uses full NS path
    + Upgraded : Useless instructions handles for() correctly
    + Upgraded : Recursive, IsGenerator and Loop Calling includes yield from
    + Upgraded analysis : 1741 / 1750 test pass (99.5% pass). 

**Version 0.9.3 (Purple-Gold Bells, 2016-12-12)**

+ Architecture
    + Lots of cleaned code
    + Harmonized data for extensions
    + Stop 'project' if no code is available
    + Now using stub in phar.
+ Report
    + Added directives, bugfixes, external services and 
    + Added support for PHP 7.0.14 and 5.6.29
+ Analysis
    + New analysis : Wordpress, recommend prepare()
    + More favorite reports : final ?> and unset()/(unset)
    + Reduced number of double reports for many analysis
    + Update : Fixed analysis with $THIS
    + Upgrade : report useless casting of comparisons
    + Update : Should use this takes into account parent::

**Version 0.9.2 (Golden Haired Hou, 2016-12-05)**

+ Architecture
    + First version of Exakat for docker (beta)
    + Added a waiting loop in cleandb
    + Docs include a list of new analysis per version
+ Report
    + Added 2 first inventories, Appinfo() in Ambassador
    + Favorites now reports global/$GLOBALS
    + Restore composer.lock report
    + Upgraded uselessReturn for the final return. 
+ Analysis
    + New analysis for Newt, Nsapi, 
    + New analysis : __ in methods names
    + New analysis : Too many local variables
    + New analysis : Avoid array_push()
    + Upgraded ext/apache coverage
**Version 0.9.1 (Sai Tai Sui, 2016-11-28)**

+ Architecture
    + Docker supported in exakat/config.ini for PHP binaries. 
    + Added exakatSince in analysis documentation
    + Added some missing tokens in anonymize command
+ Report
    + Added several new analysis for PHP 7.1
+ Analysis
    + new analysis : find methods that could return Void
    + new analysis : find malformed octal sequence in strings
    + new analysis : spot rethrown exception
    + new analysis : reach the last element
    + new analysis : find undefined Zend Framework classes (2.0 to 3.0)
    + Upgraded analysis : 1706 / 1714 test pass (99.5% pass). 
+ Tokenizer
    + Fixed handling references (some were missing)
    + Fixed handling of ellipsis (some were missing)

**Version 0.9.0 (Python Demon, 2016-11-21)**

+ Architecture
    + Project now include 'Preference' analysis
    + Dump is now incremental (-u option), and doesn't need to be run in paralell
    + Added new hashAnalysis table, to handle generic results from analysis.
    + Added project name in the graph.
    + New command 'status' to report the current status of exakat
+ Report
    + Ambassador includes 'Preferences' section and new menu system
    + Upgraded progressbar to display project processing
+ Analysis
    + New analysis : Early Bail Out (with if/then)
    + New analysis : PHP 7.1 backward incompatibilities with microseconds
    + New analysis : Wordpress : recommend using WP api, not PHP.
    + Upgraded 'Constant condition' to include do..while()
    + Upgraded 'Useless Abstract' to include methodless classes
    + Upgraded analysis : 1687 / 1697 test pass (99% pass). 
+ Tokenizer
    + Added 'Array' to list of determinist functions (more constants are spotted)
    + Fixed 'Name' for Array Short Syntax.
    + Fixed variadic support

**Version 0.8.9 (Yellow Brows Great King, 2016-11-14)**

+ Architecture
    + Fixed and document -tgz and -zip option of init
    + Removed progress folder
    + Made MagicNumber a parallel task in Project.
    + Turned some die into assertion()
    + .phar doesn't report any PHP errors. 
    + Checked compilation with PHP 5.3->7.2
+ Report
    + Removed Faceted report
    + Added Bugfixes for PHP 7.0.13, 5.6.28 and PHP 7.2
    + Added 'One variable string' to Radwell report
+ Analysis
    + New analysis : Object Calisthenics #1, #4
    + New analysis : check that properties are all set at constructor time.
    + New analysis : spot useless checks
    + Updated UndefinedParentMP to take PHP ext classes into account
    + Upgraded 'array_merge in loops' with file_put_contents
    + Upgraded 'useless parenthesis' with math operations
    + Upgraded analysis : 1666 / 1682 test pass (99% pass). 
    + Added debug Query method to analysis
+ Tokenizer
    + Fixed Files to compile first, then count tokens
    + Find Ext Lib handle UT classes better
    + Added limit to 'code' before loading into database. There is a 2M limit.
    + Fixed edge case with nested foreach()
    + Fixed segmentation fault when getting tokens from a script with wrong encoding
    

**Version 0.8.8 (Apricot Immortal, 2016-11-07)**

+ Architecture
    + Added concurency test to avoid running several instance at the same time
    + Report error when it happens with git clone
    + Added UT classes to external libraries
    + Dump is now hidden until finished.
    + Better detection of java and composer (Thanks Julien)
+ Report
    + New report : Radwell
    + New report : PhpConfiguration helping with configure and php.ini
    + Ambassador : Fixed dashboard values
+ Analysis
    + New analysis : time() vs strtotime('now')
    + New analysis : useless casting
    + New analysis : No Isset() with Empty()
    + New analysis : don't echo errors
    + New analysis : ext/rar
    + New analysis : use Class::class when possible
    + Added array_key_exists() to slow functions list.
    + Upgraded UpperCaseKeywords to handle partial uppercase
    + Added reported directives for ext/filter
    + Upgraded 'Variables used once' to exclude $this and arguments
    + Upgraded Unreachable Code with break/continue;
    + Multiple Identical Keys now handles null, boolean, real.
    + Upgraded analysis : 1652 / 1668 test pass (99% pass). 
+ Tokenizer
    + Now spots \true, \false, \null as Boolean and Null
    + Removed 'xargs too many arguments' error on Linux

**Version 0.8.7 (Naked Demon, 2016-10-31)**

+ Architecture
    + Upgraded Boolean and Integer to report results without storing them in graph
+ Analysis
    + New analysis : modernizable empty() calls
    + New analysis : recommend Positive conditions
    + New analysis : drop else after return
    + Upgraded analysis : unreacheable code handles if/then with returns.
    + Added tests for Boolean and Null
    + More not Hashes dict.
    + Upgraded analysis : 1637 / 1650 test pass (99% pass). 
+ Tokenizer
    + Fixed line number of <?= 
    + Fixed token on arguments

**Version 0.8.6 (Fuyun Sou, 2016-10-24)**

+ Architecture
    + New command to ping a queue
    + More documentation
+ Report
    + Ambassador report sped up multiple times
    + Text, Json and XML all report only analysis (not the dependencies)
+ Analysis
    + New analysis : suggest ternary instead of Ifthen
    + New analysis : check for returned value usage
    + Added support for PHP 7.0.12 and 5.6.27
    + Added more bugs fixing from extensions
    + Fixed analysis for Zend Framework 1
    + Ignore $this in variable used once
    + Fixed report with unlimited arguments functions
    + Overwritten literals : Ignore assignations in for()
    + Upgraded old PHP 5.* analysis to Gremlin 3
    + Upgraded analysis : 1639 / 1645 test pass (99% pass). 
+ Tokenizer
    + Fixed precedence between require and .
    + Better fullcode for <?= 

**Version 0.8.5 (Naked Demon, 2016-10-17)**

+ Architecture
    + Moved all classes under Exakat folder for clean hierarchy
+ Report
    + Ambassador : restored line number in display
+ Analysis
    + New analysis, check for substr() comparisons with literals
    + New analysis, suggest boolean cast, instead of Ternary.
    + New analysis, spot 3 levels of if/then
    + Upgraded 'hardcoded password', for kadm5 and hash_* functions
    + Upgraded 'external libs', with Zend Framework
    + Upgraded analysis : 1625 / 1638 test pass (99% pass). 

**Version 0.8.4 (Lingkongzi, 2016-10-10)**

+ Architecture
    + Moved Tasks into Exkat\Tasks
    + Fixed findExternalLibs
+ Report
    + Ambassador report got good annex, fixed settings and faceted search
    + Omit clearPHP if not present in docs
+ Analysis
    + New analysis : detect multiple identical traits/interface in CIT
    + New analysis : suggest creating aliases to reduce code
    + New analysis : spot aliases that may be reused again
    + New analysis : hidden use, that are not at the beginning of the code
    + Upgraded analysis : 1607 / 1618 test pass (99% pass). 
    + More documentations to many analysis
    + HasMagicProperty report all magic methods 
    + Upgraded 'Useless Parenthesis' with more situations
    + Upgraded 'Unchecked resources' with 2 more situations
    + Fixed several analysis when using Boolean and Null as a class
    + Fixed analysisIsNot with arrays
    + Removed include-like from undefined functions
    + Arrays/AmbiguousKeys : Extended to arrays calls
+ Tokenizer
    + Fixed edge case with return ?>
    + Fixed path for reporting

**Version 0.8.3 (Guzhi Gong, 2016-10-03)**

+ Architecture
    + Created temp folder .exakat in projects_dir
    + Removed mentions of float, only using Real
    + Moved Config to Exakat\Config
    + More examples in docs
+ Report
    + Added settings and files to Ambassador
+ Analysis
    + New analysis for dependant Traits
    + Added new Theme 'Cakephp' with 6 analysis for migration
    + New values for Not-a-hash
    + Unresolved Catch now takes Throwable into account
+ Tokenizer
    + Fixed edge case where return is used inside if/then without {} nor value.
    + Fixed 'code' and 'token' for ?: and ()

**Version 0.8.2 (Jinjie Shiba Gong, 2016-09-26)**

+ Architecture
    + More examples in docs
    + Fixed 'file' in results
+ Report
    + Added more media for Ambassador
+ Analysis
    + New analysis for count/strlen compared to 0
    + Upgraded analysis : 1563 / 1579 test pass (99% pass). 
    + Backported all 4 Wordpress analysis (wpdb, nonce usage)
    + Added new Wordpress analysis : variable escaping in templates
+ Tokenizer
    + Fixed <?= so it is handled like echo

**Version 0.8.1 (Babo'erben, 2016-09-19)**

+ Architecture
    + Added main Try/Catch
+ Report
    + Added 'Ambassador' report. 
+ Analysis
    + Upgraded analysis : 1540 / 1561 test pass (99% pass). 
    + More documentation (examples, glossary) 
    + Added a list of stopwords for No Hardcoded Hash
    + Upgraded analysis 'No Hardcoded Path' with protocols and glob with wildcards
    + Upgraded analysis 'No Hardcoded Hash' with stopwords
    + Added new Analysis for portability : spot common Linux files
    + Added new Analysis : use system temp dir, not hardcoded one 
    + New analysis that spot unused protected methods
    + Added Time-to-fix and severity to all analysis
+ Tokenizer
    + Fixed edge case with if/then and try/catch 
    + Synchronized constants in Tokens/Consts*.php
    + Added support for PHP 7.2

**Version 0.8.0 (Benbo'erba, 2016-09-12)**

+ Architecture
    + More examples in the docs
    + Better find root in export
+ Report
    + Prepared code for new report style
+ Analysis
    + New analysis : no throw in __destruct
    + New analysis : spot empty blocks in control structures
    + Update : Check parse_str and mb_parse_str()
    + Upgraded analysis : 1524 / 1540 test pass (99% pass). 
+ Tokenizer
    + Fixed representation of [] and [index] with static properties

Version 0.7.10 (Nine Headed Bug, 2016-09-05)
+ Architecture
    + Added optional dependency to mbstring in Doctor
    + 
+ Analysis
    + Added analysis for PHP 7.1 features
    + Upgraded analysis : 1377 / 1510 test pass (91% pass). 
+ Tokenizer
    + Removed parasit 'void' added in sequences.
    + Raised export max depth to 15. 
    + Fixed FQN for new without parenthesis
    + Fixed support for PHP 5.5/5.6. 
    + Added support for iterable
    + Checked support for extensions and ignore dirs 

**Version 0.7.9 (Wansheng Princess, 2016-08-29)**

+ Architecture
    + Added several features at Loading time : mark global variables in $GLOBALS,
      fallback FQN in functions, link constant to definitions.
+ Analysis
    + Added analysis for impossible comparisons (count($a) < or >= 0)
    + Added analysis for PHP 7.1 : removed directives, added functions
    + Upgraded analysis : 1485 / 1522 test pass (97.5% pass). 
+ Tokenizer
    + Fixed edge case with <?= $v;
    + Fixed priorities between include and .
    + Better support of trait in classes

**Version 0.7.8 (Wansheng Dragon King, 2016-08-22)**

+ Architecture
    + Prepared databases for PHP 7.2
+ Analysis
    + Reports that preg_match results are not checked
    + Report List short syntax usage.
    + Upgraded analysis : 1224 / 1493 test pass. 
+ Tokenizer
    + 

**Version 0.7.7 (Water Repelling Golden Crystal Beast, 2016-08-17)**

+ Analysis
    + Upgraded Bug database to handle PHP 7.0.10, 5.6.24 and 5.5.38

**Version 0.7.5 (Jade Faced Princess, 2016-07-19)**

+ Architecture
    + Added 'anonymize' command, that anonymize files and projects
+ Analysis
    + new analysis : recommend preg_replace_callback_array() when there are several call to preg_replace_callback_array()
    + Upgraded analysis : 1103 / 1464 test pass. 
+ Tokenizer
    + Lots of fixes for stability : tested on 28M tokens 

**Version 0.7.4 (Great Sage Who Pacifies Heaven, 2016-07-12)**

+ Architecture
    + Entirely rewrote the 'Tokenizer' part
    + Upgraded database schema 
+ Analysis
    + Upgraded analysis : 1027 / 1461 test pass. 
+ Tokenizer
    + Entirely rewrote the 'Tokenizer' part
    + 1851 UT pass correctly (extra 51)

**Version 0.6.7 (Red boy, 2016-05-30)**

+ Report
    + Added List With Keys in Appinfo()
    + Added by-reference functions mention
    + Now reporting good visibility/static for __callstatic
    + Added bug info for PHP 7.0.7, 5.5.36, 5.6.21
+ Analysis
    + New : recommend instanceof over is_object()
    + Fixed several ignored limitations, due to case : $phpversion
+ Tokenizer
    + Fixed 'originclass' in namespaced use

**Version 0.6.6 (Princess Iron Fan, 2016-05-23)**

+ Report
    + New report, suggest disable_functions directive value.
    + Added support for memcached directives
+ Analysis
    + New analysis : spot throw without new
    + New analysis : suggest adding 2nd parameter to unserialize in PHP 7.0+
    + New analysis : spot successive if/then with the same condition
    + Added support for zendoptimizer and suhosin extensions
    + PHP7 indirect expression : added support for {} in properties
+ Tokenizer
    + Raised cycle count, to speed up building AST for large projects

**Version 0.6.5 (Great Sage Who Pacifies Heaven, 2016-05-16)**

+ Analysis
    + New analysis : spot globals that may be turned into property
    + New analysis : check that ZF1 classes are well located
    + Upgraded 'dangling foreach reference' to support key=>value
    + Better support for PHP 7 indirect expression
    + More directives for xdebug
    + Eval Without Try is PHP 7 only
    + No Choice analysis is now case insensitive
+ Tokenizer
    + Added support for keys in list() (PHP 7.1)
    + Added support for constant visibility (PHP 7.2)
    + Added support for Multi catch : catch(A|B $e) (PHP 7.1)
    + Fixed bug with + and instanceof
    + Fixed precedence between :: and ??

**Version 0.6.4 (Bull Demon King, 2016-05-09)**

+ Architecture
    + Externalized the list of recognized libraries to Json
    + Added 'Wordpress' and 'Coding convention' as Recipes
+ Report
    + Initial report for Zend Framework. Still prototyping.
+ Analysis
    + Accelerated analysis for Implicit GLobals variables
    + New analyze : Indirect Injections (Security)
    + New analyze : Should Use Coalesce (code upgrade)
    + New analyze : Suggest dirname(__FILE__) => __DIR__
    + Added 'str_rot13' as unsafe 'crypto'
    + Properties without default can't be redefined
    + Added Yield and Yield From as structures without parenthesis needs
    + Double Assignation, unless 2nd call is a functioncall (less false positives)

**Version 0.6.3 (Jade Faced Princess, 2016-05-02)**

+ Architecture
    + Removed several useless pieces of code (self analysis)
    + Added documentation for Wordpress Recipes
    + Lengthened Cycle for tokenizer
+ Report
    + Added bugfixes for PHP 7.0.6, 5.6.21, 5.5.35.
    + Now reporting token counts per files 
+ Analysis
    + New analysis : Spot variable that holds $_GET, $_POST, $_REQUEST or $_COOKIE values (internal)
    + New analysis : Report variables that are overwritten by themselves
    + New analysis : Report useless switch (empty, 1 case only)
    + Upgraded NoChoice to handle larger sequences
    + Upgraded Useless Global to handle global $x / $GLOBALS['x'] situations
    + New analysis : Wordpress Recipe : Unverified Nonce, Best Usage for $wpdb
    + New analysis : Void for PHP 7.1   
+ Tokenizer
    + Fixed but with Typehint
    + Added phppowerpoint class in external libraries

**Version 0.6.2 (Long Armed Ape Monkey, 2016-04-25)**

+ Architecture
    + Fixed phar detection (based on ext/phar)
    + Cleaned code with myself
+ Report
    + New report format : clustergrammer
+ Analysis
    + New analysis : same conditions in If / Then
    + New analysis : spot dead code in catch expressions
    + Static loops now exclude methods usage
    + Indirect variable expression are stricter
    + preg_* Option e has better support for delimiters
    + Upgraded Direct Injection in case of concatenation
    + Detect Ellipsis when counting arguments
    + Could use short assignation : avoid $a += $a + 3;
+ Tokenizer
    + Sped up Typehint detection
    + No indexing for T_STRING in properties
    + Reduced errors from token_get_all() 

**Version 0.6.1 (Red Bottomed Horse Monkey, 2016-04-18)**

+ Architecture
    + Prepared to support PHP 7.1
    + Fixed bug in user / passwords when initing the project
    + Better support for ::class when searching for libraries
+ Analysis
    + UselessParenthesis : spot nested parenthesis
    + Spot exceptions that are thrown but uncaught by the current code
    + Support for ext/lua, 
    + New : Check catch order in try/catch
    + Better identification of Composer classes, based on composer.json
    + Now spot interfaces in use declarations (less undefined interfaces)
+ Tokenizer
    + Added support for PHP 7.1
    + key => value in list() calls
    + visibility for constants in Classes and Interfaces
    + Accelerated up Typehint support

**Version 0.6.0 (Intelligent Stone Monkey, 2016-04-11)**

+ Architecture
    + Fixed a bug in Find external libraries
    + Applied fixed based on new analysis audit
    + Fixed a bug that prevented results to be prepared for report (Thanks Philippe G.)
+ Report
    + Now reports reason for excluding a file from analysis
+ Analysis
    + New analysis : Logical Mistake (first version),
    + New analysis : Iffectations (code restoration)
    + New analysis : Common alternatives
    + New analysis : No Choice (No alternatives)
    + New analysis : Random_* Without Try (security risk)
    + New analysis : Unknown PCRE options
    + New analysis : Identical conditions
    + New analysis : Hardcoded hashes 
    + Upgrade List with appends with variable name
    + Upgrade /e option detection
    + Fixed detection of unused use, with long namespaces.
    + Added finfo to ext/finfo
    + Finds exceptions that are reserved for later throwing
    + Exclude anonymous classes from Already Defined Interface
+ Tokenizer
    + Extended cycle number to speed up tokenizer. 
    + Better escaping of file names 

**Version 0.5.9 (Six Eared Macaque, 2016-04-04)**

+ Architecture
    + One progressbar per Recipe during project analysis
    + report's documentation
    + Upgraded 'External Lib' to ignore Composer folders.
    + Fixed a bug about interpreting tokens 
    + Dump collects classes, interfaces, traits definitions 
    + Now storing project name in database for future use
    + Removed PHP configuration modifications (error_reporting, display_errors)
+ Report
    + Added 'Uml' report : hierarchy report
    + Now reports Pear Usage
    + Upgraded Bugfix database for 7.0.5, 5.6.20 and 5.5.34
    + Report Yield (from) usage
    + New external configuration files : bazar, github, docker, openshift
+ Analysis
    + Added detection for undefined classes in ZF (1.8 to 1.12)
    + New : report undefined Traits
    + Added support for parent/grandparent when checking argument numbers
    + Added support for V8js
+ Tokenizer
    + Fixed bug in fullnspath for use within trait or class
    + It is possible to reach a property on an array append
    + Fixed AST between PHP 5 and 7 for globals
    + Simplified ++ analysis

**Version 0.5.8 (Sun Deity of Mao, 2016-03-28)**

+ Architecture
    + Moved to self::, instead of static::.
    + First UT for command line
    + Sped up phploc. Prepare code for finite states, in Tasks.
    + Prepare for Gremlin3 (moved gremlin calls to class)
    + Reduced shell_exec usage
+ Report
    + Fixed display bugs in Devoops report
    + Removed double analysis
    + 'Wrong number of arguments' now supports constructors
+ Analysis
    + Upgraded 'No Hardcoded IP' to handle constants, spot domains
    + Added support for TokyoTyrant
    + New analysis : spot simple regex, and suggest strpos
    + Excluded "$a[b]" from undefined constants
+ Tokenizer
    + Fixed bug with nested call to echo.
    + Fixed bug where concatenation ends on a 'AS' keyword
    + Added support of Constants in Foreach
    + Fixed multiple bugs in Grouped Use
    + Support for function as 'class' in static calls
    + Comparison accepts powers
    + Added support for empty array short syntax in sequence
    + Support constant with visibility
    + Parenthesis may be the base for Arrays

**Version 0.5.7 (Scorpion Demon, 2016-03-21)**

+ Architecture
    + Added support for folders in UT, for tests that requires several files
    + Improved compatibility with PHPunit
    + Moving gremlin_query() to Gremlin2 class
    + Doctor also reports for phar
    + Improved adaptation to PHP and Exakt in server mode
    + Autoload shouldn't die
    + Fixed case when calling Phpexec
    + Upgraded status presentation in server mode
+ Report
    + More details for Global Variable list
+ Analysis
    + Now spotting class when it is inside a string
    + Check for $this outside a trait/class
    + Check for ternary/concatenation precedence
    + Spot classes that attempt to extend final 
    + Spot set_exception_handler() that may need rework
    + Refined array_merge analysis, in case of nested loops
+ Tokenizer
    + Yield [from] may be inside an array
    + Refactored for/foreach tokens
    + Added support for a 'Project' node

**Version 0.5.6 (Ruler of Women's Country, 2016-03-14)**

+ Architecture
    + Fixed some backward compatibility with PHP 5.4
    + Started revamping 'Status' command 
    + Centralized all tokenizations to PhpExec class
    + Removed usage of __DIR__ and __FILE__ 
+ Analysis
    + Spot usage of empty() that can't work on PHP 5.4
    + Suggest using random_int instead of rand
    + Upgraded 'No Array_merge in loops' with array_merge_recursive
    + Added support for scalar type hint in Undefined Classes
    + New analysis : Better rand()
+ Tokenizer
    + Instanceof has lower precedence than comparison

**Version 0.5.5 (Immortal Ruyi, 2016-03-07)**

+ Architecture
    + Added default values for all neo4j_* configs
+ Report
    + Added support for bugfixes in 7.0.4, 5.6.19 and 5.5.33
    + Added support for bugfixes in 7.1.0-dev
+ Analysis
    + Added support for Typehint in Undeclared Classes
    + Extended 'Multiple Classes in One File' to interfaces and traits
    + Added analysis for truthy and falsy
    + Spot interfaces implemented by parents (Thanks PHP Inspect)
    + Report usage for unsafe Curl options
+ Tokenizer
    + Fixed emptyString inside a Heredoc
    + Fixed bug where Sign has lower priority than Power

**Version 0.5.4 (Nezha, 2016-02-29)**

+ Architecture
    + Removed some shell_exec() to help with portability
    + Clean command now rebuilds an empty datastore
    + Check the availability of php binaries before using
    + Produce report in a hidden folder, then push it
+ Report
    + Report the list of bug fixes that apply to code
+ Analysis
    + Help using preg_match_all options
+ Tokenizer
    + Fixed a bug with reference and instanceof

**Version 0.5.3 (Li Jing, 2016-02-22)**

+ Architecture
    + More UT
    + Supports symlinks for neo4j's folder
    + Supports symlinks for 'code' folder in projects
    + Added upgrade command to check for exakat's available versions and upgrade
+ Analysis
    + Spot CLI scripts
    + Undefined Interfaces avoids self, parent, static
    + Fixed bug in spotting undefined Interface
    + Variable Used Once in a method are not arguments
    + Added support for all structures in Double Assignation

**Version 0.5.2 (Single Horned Rhinoceros King, 2016-02-15)**

+ Analysis
    + Fixed functioncall detection with 'empty'
    + Refined 'Buried assignation' analysis
    + Fixed a bug when using definitions (class, trait, interface, functions...)
    + Better support for case-insensitive constants
    + 
+ Tokenizer
    + Fixed bug in use statement
    + Now spots PHP code in files without extension
    + Upgraded support for grouped Use statement
    + namespace may be a valid nsname part
    + Fixed bracket reports in do...while

**Version 0.5.1 (King of Spiritual Touch, 2016-02-08)**

+ Architecture
    + Added test in UT to skip incompilable sources
    + Stabilized tokenizer's UT (partial)
+ Report
    + HTML protection in Devoops format
    + No display of negative stats
    + Added support for directives : wincache, xcache, apc, opcache
    + Added support for eaccelerator and openssl
+ Analysis
    + New analysis : Spot unknown PHP directive names
    + Fixed Constants/MultipleDefinedConstants
    + Better detection of functioncalls (with List)
    + Better spotting of ini_set arguments
    + Unreachable code now finds die and exit
    + ObjectReference won't report references on scalar types
    + Revamped 'pregOptionE' analysis
    + Cleaned code with too many arguments
    + Removed useless print
    + Better report of eval() usage
    + Revamped 'Dynamic code' report
    + Fixed bug in Case/Default that are empty
    + Avoided sequences of sequences in Case/Default
    + Fixed Detection of classes' usage with extension
+ Tokenizer
    + Fixed bracket detection on While and DoWhile
    + Detect void in DoWhile
    + Removed useless T_DIE token
    + Fixed fullcode processing for anonymous classes

**Version 0.5.0 (Immortal of Antelope Power, 2016-02-01)**

+ Architecture
    + Added support for HTTP API, through 'server' command. 
+ Analysis
    + Fopen modes checked
    + Redefined default, in class's properties
+ Tokenizer
    + Fixed situation where echo and print used parenthesis (they don't)
    + Fixed rare but with instanceof and concatenation
    + Fixed support of integers in Gremlin
    + Fixed bug in addslashes and and $ protection order
    + Made Assignations more robust (no un-processed tokens)
    + Reduced the number of shell_exec usage => speed up
    + Finished support for relaxed keyword support in classes (PHP 7)

**Version 0.4.6 (Immortal of Elk Power, 2016-01-25)**

+ Architecture
    + New installation script with Vagrant and Ansible (Thanks Alexis!)
    + Updated documentation
    + Added a command to remove a project
+ Report
    + Devoops reports has case-insensitive menu sort
+ Analysis
    + Spot redefined properties, classes and methods. 
    + Spot properties that may be turned private
    + Fixed special case in Wrong Number Of Arguments
    + Fixed 'OnePage' analysis
+ Tokenizer
    + Finished support for relaxed keywords in classes
    + Sped up tokenizer by keeping counts of tokens in datastore
    + Fixed detection of CakePHP
    + Fixed special case with Labels
    + Fixed rare case with die() within ternary operator

**Version 0.4.5 (Immortal of Tiger Power, 2016-01-18)**

+ Architecture
    + Upgraded documentation
    + Default command is 'help'
+ Report
    + Better version for FacetedJson report
+ Analysis
    + New analysis that spots wrong type of argument in PHP internal functions
    + Fixed Isset With Constant for PHP 7
    + Fixed a bug that limited query size during analysis (good for bigger projects)
    + Include variadic (...) to Variable Argument Number
+ Tokenizer
    + Fixed a bug that blocked tokenizer when a analyzed script generated parse errors.
    + Added support for bazar, svn.
    + Fixed a bug in Nsnames at Loading time.

**Version 0.4.4 (Crown Prince Mo'ang, 2016-01-11)**

+ Architecture
    + Reviewed OnePage analysis
    + Dump as now an option to select Recipes
    + Dump forces line to be integer
    + Added a task to update a project's code (git only ATM)
+ Report
    + Better check when opening database for report (more to come)
    + FacetedJson (and Json) report ignore non-unicode lines
    + Added 'search' box to facetedJson
+ Analysis
    + Switch To Switch suggestions
    + Unused arguments patch for arguments used in methods
    + Unused properties doesn't mistake function static variable
+ Tokenizer
    + All Nsnames are now build at Loading time
    + Constants may be calld 'const'
    + More relaxed syntax for methods (exit, include, eval...)
    + Foreach may use coalesce
    + Fixed an edge case with Closures in functioncall

**Version 0.4.3 (Tuolong, 2015-01-04)**

+ Architecture
    + Copyright year bump
    + Doctor reports memory_limit and php version consistency
    + Switched to rmDirRecursive
+ Report
    + Removed old style reporting system
+ Analysis
    + Fixed fileupload and filesystem directives reports
    + Added report of Environment variable usage
    + Added iconv_set_encoding to the list of directive usage
    + Extension analyzes now takes into account namespaces and traits
    + Analysiss all have severity and time to fix
+ Tokenizer
    + 

**Version 0.4.2 (Red Boy, 2015-12-22)**

+ Architecture
    + Published documentation on http://exakat.readthedocs.org
    + First version of the faceted report (-format Faceted)
+ Report
    + First version of the faceted report (-format Faceted)
    + Fixed Dump that actually finishes after some time
+ Analysis
    + Spot unused arguments
    + Fixed notInInterface() filter
    + Upgraded HtmlEntitiesCall

**Version 0.4.1 (Azure Lion, 2015-12-14)**

+ Architecture
    + Rebuild the report system, for speed and versatility.
+ Report
    + Available format : JSON, Sqlite, XML, Text and HTML (Devoops).
    + Rules are now part of the documentation. 
+ Analysis
    + Upgraded 'Buried assignations' 
    + Locally Unused also spots properties without visibility (but with definition)
    + Could be class constant, if the property is used at least once
    + Better detection of files that are Definitions only (fix at Namespace calls)
    + ++ is now correctly reported as isRead and isWritten in Arguments
    + Closure's use($x) are now reported in both context (calling and called)
    + Removed usage of 'back' method, that is blocking at high token counts
+ Tokenizer
    + Fixed support for {} and {$ } inside strings
    + Fixed bug with Typehint, that prevented compilation
    + Fixed several (rare) edge cases with Sign and Staticproperties.
    + Fixed detection of closing tags

**Version 0.4.0 (Lion Lynx Demon, 2015-12-07)**

+ Architecture
    + Made PHP 7.0 the default (moved to 0.4.0)
    + Ran unit tests on PHPunit 5.1
    + Added a background tasks to build report. Will allow for progressive report.
+ Report
    + Rewrote the report from scratch. Should be finished next iteration.
    + New report is working for XML and Text report.
+ Analysis
    + Added support for ext/pecl_http
    + Added several classic folders as ignored by default (change this in config.ini)
    + Create a check for functioncall (and not methods)
    + Spots join('', file())
    + Safely ignoring some dynamic calls in undefined functions (Thanks Marc Delisle)
    + Removed ArrayAppend from double assignation
+ Tokenizer
    + Fixed a bug when class was auto-referenced.
    + Fixed detecting Static properties when they are also arrays.
    + Fixed fatal errors for mal-formed octals

Version 0.3.12 (Nine Tailed Vixen, 2015-11-30)
+ Architecture
    + ProgressBar is now displayed during Analyze phase.
+ Report
    + Report list of error messages used in the library
+ Analysis
    + Omit eval with hardcoded strings
    + Exclude some index from _SERVER from the report (they are safe)
    + Exclude php://* files as hard coded path
    + Report usage of timestamp to calculate duration 
    + Spots unused traits
    + Fixed support for big integers
+ Tokenizer
    + First support for relaxed keywords in classes. More to come.
    + Checked UT on PHP 7 (Soon to become default version)
    + Fixed version detection in Tokenizer
    + Fixed fullnspath in Use expression;

Version 0.3.11 (Hu A'qi, 2015-11-16)
+ Architecture
    + Report external services files that may be in the repository
+ Report
    + Report nested dirname calls (may be changed in PHP 7)
+ Analysis
    + Better spotting of static loops
    + Don't confuse $globals and $GLOBALS
+ Tokenizer
    + Rewrote support for As in classes. 
    + Fixed arguments that were indexed as Void
    + Trimmed code

Version 0.3.10 (Silver Horned King, 2015-11-09)
+ Architecture
    + Centralized call to cypher.
+ Report
    + Sped up several analyzes
+ Analysis
    + Fixed naming bug with reflexion
    + Support class name in arrays, short syntax
    + Report Relay Functions
    + More PHP 7 incompatibilities reports
+ Tokenizer
    + Support for 7.1 compilation (dev only)
    + Added cakephp to external libraries
    + Fixed parsing bug with static (as property definition)
    + Fixed 'count' in sequences from Function
    + Rewrote Argument detection (when there is no parenthesis)

Version 0.3.9 (Golden Horned King, 2015-11-02 up)
+ Architecture
    + Cleaned code with Exakat
+ Analysis
    + Refined report about double assignation
    + Fixed argument counting in Function Definition
    + Better support of array in Locally Used Properties
    + Updated Composer database
+ Tokenizer
    + Fixed a bug that ignored Blocks
    + Fixed a rare bug with echo and the following arguments

**Version 0.3.8 (Baihuaxiu, 2015-10-26)**

+ Architecture
    + Cleaned too many display (they go to log now), leaving commandline empty (or -v)
    + A lot more PHP 7 incompatibilities spotted 
+ Report
    + Added the list of global variables in the projects (if any)
    + Fixed reports for PHP 5.2 (they were ignored)
+ Analysis
    + Better handling of composer in unresolved classes
    + Spot setlocale with string (PHP 7)
    + Spot string unpacking (PHP 7)
    + Upgraded static method call, to avoid classes of the same family
    + Report eval without try/catch
    + Report preg_replace with /e 
    + Fixed report for empty list()
    + Spot hexadecimal in strings 
    + Report usort (and co) as incompatibilities between PHP 7 and 5
+ Tokenizer
    + Fixed edge case with Sign and namespaced function
    + Added xajax, adodb and gacl as common library
    + Fixed arguments in short array syntax
    + Fixed case where [3] was spotted inside a string

**Version 0.3.7 (Yellow Robe Demon, 2015-10-19)**

+ Architecture
    + Added and reviewed many UT. More stability.
+ Report
    + Fixed the report of the actual version of PHP being used.
    + Non-run analysis are not marked with a stethoscope
    + Report now report closures and not the containing method
    + Removed some dashboard that would generate empty links
+ Analysis
    + Better spot of blocks inside Alternative syntax
    + Speed up method spotting
    + Fixed properties which were mistaken with deep definitions
+ Tokenizer
    + Fixed fullcode for Typehint
    + Removed Ppp and moved it to Visibility

**Version 0.3.6 (White Bone Demon, 2015-10-12)**

+ Architecture
    + Large speed up at Parsing stage, for large projects
    + Added git informations in Doctor
+ Tokenizer
    + Changed processing for Arguments.
    + Support for more PHP 7 features, including Use Grouping, 
    + Fixed support for ~ 
    + Simplified ::class handling

**Version 0.3.5 (Mingyue, 2015-10-06)**

+ Architecture
    + Reported usage of array constants, improving backward compatibility
    + Checked running on PHP 7
+ Report
    + Added Definition annex
    + Fixed 'version incompatible' report that was mistaken with 'no result'
    + List all directives being modified in the code
    + List more directives that should be set for production.
+ Analysis
    + Reworked the Themes about compatibility. 
    + Added many tests for PHP 7.0 compatibility
    + Sped up UsedMethod analysis
    + Added support for PHP 7 feature : Unicode Escape Sequences, New functions/classes/interfaces, Removed Functions, 
+ Tokenizer
    + Changed processing for Empty PHP code
    + Support Variable Indirection for both PHP 5 and 7 (depends on exec version)
    + Avoid ignoring all code when finding External Libraries
    + Fixed edge cases with declare() when it is conditional.
    + Support for PHP 7's f()()()

Version 0.3.4 (Qingfeng, 2015-09-28 up)
+ Architecture
    + Added token_limit configuration to avoid running too large project (default is 1 000 000)
    + Several new tools for internal consistency check.
    + Removed support for neo-contrib's gremlin plugin
+ Report
    + Report libraries that were found and ignored
+ Analysis
    + Sped up queries that required previous analysis or multiples atoms
    + Spot global keywords inside loops (perf)
    + Better spotting of Composer classes 
    + Report double assignations
+ Tokenizer
    + Added support for Anonymous classes (PHP 7)
    + Fixed namespace manipulations (They weren't lower case)
    + Mark constants as fail back globals or local to the namespace
    + Support Null Coalesce operator (PHP 7)
    + Fixed rare case for empty strings and noDelimiter

**Version 0.3.3 (Immortal Zhenyuan, 2015-09-21)**

+ Architecture
    + Removed some shell stderr that leaked to the main script
+ Report
    + Added the list of used analysis
    + favicon is now used in the report (Devoops)
    + Fixed count report for Else 
    + Fixed directive reports for trader, bcmath and ldap.
+ Analysis
    + Rebuild the composer database
    + Fixed htmlentities analyze
    + Spot usage of 'substr($s, $p, +/- 1)' and recommend '$s[$p]'
+ Tokenizer
    + Fixed Multiplication with instantiation

**Version 0.3.2 (Tiger Vanguard, 2015-09-14)**

+ Report
    + Added link back from analysis to its themes.
+ Analysis
    + Useless Returns are now Trait compatible
    + Optimized Composer validation 
    + Removed IsKnownVendor analyze (replaced by Composer)
    + Spot inconsistent concatenations ("$a b".$c)
+ Tokenizer
    + Fixed situation where forgotten white spaces didn't have a file
    + Removed DELETE and S_STRING index
    + Fixed compatibility with Debian (shell commands)
    + Added UT for and / && precedence versus =
    + Fixed identification of empty instructions (Functions / Closure have different behaviors)

**Version 0.3.1 (Yellow Wind Demon, 2015-09-03)**

+ Architecture
    + Removed usage of Everyman dependencies
    + Added support for Neo4j Authentication
    + Added a JobQueue
    + Cleaned code with exakat itself
+ Report
    + Added Dump to SQLITE format for custom manipulations of the results
    + Added new collection of rules for Calesthenics (dev)
    + Updated composer database 
    + Now reporting found Composer.
+ Analysis
    + Fixed Compilation spotting
+ Tokenizer
    + Fixed an edge case with Sign, when used in a concatenation

Version 0.3.0 (Lingxuzi, 2015-Aug-25)
+ Architecture
    + Moved to Thinkaurelius's gremlin plug-in, Neo4j 2.2.4 and Java 8.
+ Report
    + Added a view by File 
    + Added sorting for results (by file and by analyze)
+ Analysis
    + Spot functions whose results should be checked before they are used
    + Spot breaks/continue out of a loop
    + Exports all the results in a dump.sqlite file
+ Tokenizer
    + Fixed a minor bug with ::class (messed up the {} counts)
    + removed dependency to Everyman's Neo4j classes.
    + Added a step that removes big and identifiable libraries in PHP (such as tcpdf, jpgraph, etc..)

Version 0.2.5 (Scholar in a White Robe, 2015-Aug-17)
+ Report
    + List the files that are ignored in the annex
+ Analysis
    + Updated Knowledge Database for memcache, aliases, zlib, standard
    + Added more directives to Review
    + Added support for xhprof
+ Tokenizer
    + Fixed bug with Else (Not-alternative)
    + Fixed Sequence creation with If-Then
    + Yield may be assigned
    + Removed one Tokenizer's operation (filterOut2)
    + Fixed priorities with Concatenation, Multiplication, Additions
    + Process Echo and Print separately
    + Automatically removes common bundled libraries to reduce app size

**Version 0.2.4 (Black Wind Demon, 2015-06-22)**

+ Analysis
    + Rebuild the composer database
    + Lots of new extensions supported : ev, libevent, event, php-ast, wikidiff2, proctitle, inotify, ibase, amqp, geoip, output buffering,
    + Report errors when non-variables are returned by reference
    + Marked more analyzes for PHP 7
    + Fixed Unpreprocess structures with split
    + Upgraded spotting for useless parenthesis
    + Added a check ++$i vs $i++;
    + Exclude abstract methods from Variables Used Once
    + Added new directives
    + Also check for ASP Tags
+ Tokenizer
    + Fixed the fullpath for functions when they are not defined in the code
    + Upgraded support for Return Type (PHP 7.0+)
    + error_reporting with -1 is OK
    + Fixed a precedence problem with & and &&
    + Refactored Ifthen token to support return type 
    + Added a kill command when cleaning Database

**Version 0.2.3 (Techu Shi, 2015-06-22)**

+ Analysis
    + Report usage of Return Typehint, and Scalar Typehint
    + Report usage of classes that used to return null on new
    + Report useless abstract classes
+ Tokenizer
    + Upgraded 'init' command, to handle various VCS
    + Added support for Return Typehint

**Version 0.2.2 (Xiong Shangjun, 2015-06-16)**

+ Analysis
    + Now spots short assignations
    + More UselessInstructions spotted
    + Ignore Unset as modified values in loops
+ Tokenizer
    + Added support for PHP7 new tokens (T_SPACESHIP, T_COALESCE, T_YIELD_FROM)
    + Split loading into more .csv files for lighter and more robust queries
    + Better support for arrays [1,2,3] as functioncall (just like array())
    + Process tokens by batches of 800
    + Clean vertex at each queries, not Sequence

**Version 0.2.1 (General Yin, 2015-06-02)**

+ Analysis
    + sizeOf may have 2 arguments
    + 2 clearPHP link added in documentation
+ Tokenizer
    + Fixed bug with Bitshift and Addition
    + Fixed bug with Sequence when merging sequences
    + Fixed bug with String and Addition
    + Fixed Visibility in Use instruction
    + Foreach accepts Constants as Source
    + Fixed special case for nested IfThen

**Version 0.2.0 (Demon of Confusion, 2015-05-15)**

+ First version


