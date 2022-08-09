.. Support:

Library & Framework Support
============================

Summary
----------------------------------

* Supported Rulesets
* Supported Reports
* Supported PHP Extensions
* Applications
* Recognized Libraries
* New analyzers
* External services
* PHP Error messages
* Exakat Changelog

External Library Support
----------------------------------

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

External Services Support
----------------------------------


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
* `bazaar <https://bazaar.canonical.com/en/>`_ - .bzr
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
* `cvs <https://www.nongnu.org/cvs/>`_ - CVS
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

Supported PHP Extensions
------------------------

PHP extensions are used to check for structures usage (classes, interfaces, etc.), to identify dependencies and directives. 

PHP extensions are described with the list of structures they define : functions, classes, constants, traits, variables, interfaces, namespaces, and directives. 

* `ext/amqp <https://github.com/alanxz/rabbitmq-c>`_
* ext/apache
* ext/apc
* ext/apcu
* ext/array
* ext/php-ast
* ext/async
* ext/bcmath
* ext/bzip2
* ext/calendar
* ext/cmark
* `ext/com <https://www.php.net/manual/en/book.com.php>`_
* `ext/crypto <https://pecl.php.net/package/crypto>`_
* ext/CSV
* ext/ctype
* ext/curl
* `ext/cyrus <https://www.php.net/manual/en/book.cyrus.php>`_
* ext/date
* `ext/db2 <https://www.php.net/manual/en/book.ibm-db2.php>`_
* ext/dba
* ext/decimal
* `ext/dio <https://www.php.net/manual/en/refs.fileprocess.file.php>`_
* ext/dom
* `ext/ds <http://docs.php.net/manual/en/book.ds.php>`_
* `ext/eaccelerator <http://eaccelerator.net/>`_
* `ext/eio <http://software.schmorp.de/pkg/libeio.html>`_
* `ext/enchant <https://www.php.net/manual/en/book.enchant.php>`_
* `ext/ereg <https://www.php.net/manual/en/function.ereg.php>`_
* `ext/ev <https://www.php.net/manual/en/book.ev.php>`_
* ext/event
* Excimer
* ext/exif
* `ext/expect <https://www.php.net/manual/en/book.expect.php>`_
* `ext/fam <http://oss.sgi.com/projects/fam/>`_
* ext/fann
* ext/ffi
* `ext/file <http://www.php.net/manual/en/book.filesystem.php>`_
* ext/fileinfo
* ext/filter
* `ext/fpm <https://www.php.net/fpm>`_
* `ext/ftp <http://www.faqs.org/rfcs/rfc959>`_
* ext/gd
* ext/gearman
* ext/gender
* ext/geoip
* ext/gettext
* `ext/gmagick <http://www.php.net/manual/en/book.gmagick.php>`_
* ext/gmp
* ext/gnupgp
* ext/grpc
* ext/hash
* `ext/hrtime <https://www.php.net/manual/en/intro.hrtime.php>`_
* `ext/pecl_http <https://github.com/m6w6/ext-http>`_
* `ext/ibase <https://www.php.net/manual/en/book.ibase.php>`_
* Ice framework
* ext/iconv
* ext/igbinary
* `ext/iis <http://www.php.net/manual/en/book.iisfunc.php>`_
* ext/imagick
* `ext/imap <http://www.php.net/imap>`_
* ext/info
* ext/inotify
* `ext/intl <http://site.icu-project.org/>`_
* `ext/json <http://www.faqs.org/rfcs/rfc7159>`_
* `ext/judy <http://judy.sourceforge.net/>`_
* ext/kdm5
* `ext/lapack <https://www.php.net/manual/en/book.lapack.php>`_
* ext/ldap
* `ext/leveldb <https://github.com/reeze/php-leveldb>`_
* `ext/libevent <http://libevent.org/>`_
* ext/libsodium
* ext/libxml
* ext/lua
* ext/lzf
* `ext/mail <http://www.php.net/manual/en/book.mail.php>`_
* `ext/mailparse <http://www.faqs.org/rfcs/rfc822.html>`_
* `ext/math <https://www.php.net/manual/en/book.math.php>`_
* ext/mbstring
* ext/mcrypt
* `ext/memcache <http://www.php.net/manual/en/book.memcache.php>`_
* ext/memcached
* `ext/mhash <http://mhash.sourceforge.net/>`_
* `ext/mongo <https://www.php.net/mongo>`_
* `ext/mongodb <https://github.com/mongodb/mongo-c-driver>`_
* ext/msgpack
* `ext/mssql <http://www.php.net/manual/en/book.mssql.php>`_
* `ext/mysql <http://www.php.net/manual/en/book.mysql.php>`_
* ext/mysqli
* `ext/ncurses <https://www.php.net/manual/en/book.ncurses.php>`_
* `ext/newt <http://people.redhat.com/rjones/ocaml-newt/html/Newt.html>`_
* ext/nsapi
* `ext/ob <https://www.php.net/manual/en/book.outcontrol.php>`_
* `ext/oci8 <https://www.php.net/manual/en/book.oci8.php>`_
* ext/odbc
* `ext/opcache <http://www.php.net/manual/en/book.opcache.php>`_
* `ext/opencensus <https://github.com/census-instrumentation/opencensus-php>`_
* ext/openssl
* `ext/parle <https://www.php.net/manual/en/book.parle.php>`_
* `ext/parsekit <http://www.php.net/manual/en/book.parsekit.php>`_
* `ext/password <https://www.php.net/manual/en/book.password.php>`_
* ext/pcntl
* ext/pcov
* ext/pcre
* ext/pdo
* ext/pgsql
* `ext/phalcon <https://docs.phalconphp.com/en/latest/reference/tutorial.html>`_
* ext/phar
* ext/pkcs11
* ext/posix
* `ext/proctitle <https://www.php.net/manual/en/book.proctitle.php>`_
* ext/protobuf
* ext/pspell
* `ext/psr <https://www.php-fig.org/psr/psr-3>`_
* Random extension
* ext/rar
* ext/rdkafka
* ext/readline
* ext/redis
* ext/reflection
* `ext/sdl <https://github.com/Ponup/phpsdl>`_
* `ext/seaslog <https://github.com/SeasX/SeasLog>`_
* `ext/sem <https://www.php.net/manual/en/book.sem.php>`_
* ext/session
* ext/shmop
* ext/simplexml
* `ext/snmp <http://www.net-snmp.org/>`_
* ext/soap
* ext/sockets
* ext/sphinx
* ext/spl
* ext/spx
* ext/sqlite
* ext/sqlite3
* `ext/sqlsrv <https://www.php.net/sqlsrv>`_
* ext/ssh2
* ext/standard
* `ext/stats <https://people.sc.fsu.edu/~jburkardt/c_src/cdflib/cdflib.html>`_
* Stomp
* String
* ext/suhosin
* ext/svm
* ext/swoole
* Extensions/Exttaint
* ext/tidy
* ext/tokenizer
* ext/tokyotyrant
* ext/trader
* ext/uopz
* ext/uuid
* `ext/v8js <https://bugs.chromium.org/p/v8/issues/list>`_
* ext/varnish
* ext/vips
* `ext/wasm <https://github.com/Hywan/php-ext-wasm>`_
* ext/wddx
* `ext/weakref <https://www.php.net/manual/en/book.weakref.php>`_
* `ext/wikidiff2 <https://www.mediawiki.org/wiki/Extension:Wikidiff2>`_
* `ext/wincache <http://www.php.net/wincache>`_
* ext/xattr
* ext/xdebug
* ext/xdiff
* ext/xhprof
* ext/xml
* ext/xmlreader
* ext/xmlrpc
* ext/xmlwriter
* ext/xsl
* ext/xxtea
* `ext/yaml <http://www.yaml.org/>`_
* Extensions yar
* ext/zend_monitor
* ext/zip
* ext/zlib
* ext/0mq
* ext/zookeeper