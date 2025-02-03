.. _Installation:

Installation
============

Summary
-------

* `Requirements`_
* `Download exakat.phar`_
* `Installation with exakat.phar`_
* `Installation on OSX`_
* `Installation on Debian/Ubuntu`_
* `Installation guide with Composer`_
* `Installation guide with Docker`_

Requirements
------------

Here are the requirements to run Exakat. 

Basic requirements : 

* exakat.phar, the main code.
* `Gremlin server <http://tinkerpop.apache.org/>`_ : exakat uses this graph database and the Gremlin 3 traversal language. Currently, only Gremlin Server is supported, with the tinkergraph and neo4j storage engine. Version 3.7.x is the recommended version, while version 3.6.x is still supported. Gremlin versions 3.5.# and older are not supported anymore. 
* Java 11.x. Java 8.x is still supported, and Java 17 will be supported when Gremlin Server does. 
* `PHP <https://www.php.net/>`_ 8.3 to run. PHP 8.2 is recommended, and PHP 8.1 is the older possible. This version requires the PHP extensions curl, openssl, hash, phar, sqlite3, tokenizer, mbstring and json. 

Optional requirements : 

* PHP 5.2 to 8.5-dev for analysis purposes. Those versions only require the ext/tokenizer extension. 
* VCS (Version Control Software), such as Git, SVN, bazaar, Mercurial. They all are optional, though git is recommended, and used as the default VCS. 
* Archives, such as zip, tgz, tbz2 may also be opened with optional helpers (See `Installation guide for optional tools`_).

OS requirements : 

* Exakat has beed tested on OSX, Alpine, Debian and Ubuntu (up to 22.04). 
* Exakat should work on Linux distributions, may be with little work. 
* Exakat hasn't been tested on Windows, and is unsupported at the moment. 

For installation, curl or wget, and zip are needed.

Download exakat.phar
--------------------

Download exakat directly from `https://www.exakat.io/versions <https://www.exakat.io/versions>`_. 

This server also provides older versions of Exakat. It is recommended to always download the last version, which is available directly with `https://www.exakat.io/versions/index.php?file=latest <https://www.exakat.io/versions/index.php?file=latest>`_. 

For each version, MD5 and SHA256 signatures are available. The downloaded MD5 must match the one in the related .md5 file. The .md5 also has the version number, for extra check.

Here is a bash script to download and check the archive. 

::

    curl -O -J 'https://www.exakat.io/versions/index.php?file=latest'
    
    curl -O -J 'https://www.exakat.io/versions/index.php?file=latest.md5'
    //9c77eb52c11ee45a93654edd22cf6af8  exakat-2.6.0.phar
    md5sum -c exakat-*.md5
    // Example : 
    // exakat-2.6.0.phar: OK
    
    curl -O -J 'https://www.exakat.io/versions/index.php?file=latest.sha256'
    //adaa20a0ff1de4caf6484cc1e57079f916ae4b96dac39aa04b9615f4117b5742  exakat-2.6.0.phar
    sha256sum -c exakat-*.sha256
    // Example : 
    // exakat-2.6.0.phar: OK
    
    rm exakat-*.md5
    rm exakat-*.sha256
    mv exakat*.phar exakat.phar
    php exakat.phar version // quick check


Installation with exakat.phar
-----------------------------

Exakat.phar includes its own installation script, as long as PHP is available. Exakat checks different pre-requisites, and proceed to install the last elements.

Exakat checks for Java and Zip installations. Then, it downloads tinkergraph and the Neo4j plugin from exakat.io and runs the `doctor` command.

The install script is the one displayed on the next section.

You can use the `install` command this way: 

::

    php exakat.phar install -v 

After this step, you can go to the tutorials section. 


Installation on OSX
-------------------

Paste the following commands in a terminal prompt. It downloads Exakat, and installs tinkerpop version 3.7.0. 
PHP 8.0 or more recent, curl, homebrew are required.

OSX installation with tinkergraph 3.7.0
########################################

This is the installation script for Exakat and tinkergraph 3.7.3. 

::

    mkdir exakat
    cd exakat
    curl -o exakat.phar 'https://www.exakat.io/versions/index.php?file=latest'
    curl -o apache-tinkerpop-gremlin-server-3.7.3-bin.zip 'https://www.exakat.io/versions/externals/apache-tinkerpop-gremlin-server-3.7.0-bin.zip'
    unzip apache-tinkerpop-gremlin-server-3.7.3-bin.zip 
    mv apache-tinkerpop-gremlin-server-3.7.3 tinkergraph
    rm -rf apache-tinkerpop-gremlin-server-3.7.3-bin.zip 
    
    # Optional : install neo4j engine.
    cd tinkergraph
    ./bin/gremlin-server.sh install org.apache.tinkerpop neo4j-gremlin 3.7.3
    cd ..
    
    php exakat.phar doctor

OSX installation troubleshooting
################################

It has be reported that installation fails on OSX 10.11 and 10.12, with error similar to 'Error grabbing Grapes'. To fix this, use the following in command line : 

::

    rm -r ~/.groovy/grapes/
    rm -r ~/.m2/


They remove some files for grapes, that it will rebuild later. Then, try again the optional install instructions.



Installation on Alpine
----------------------

Alpine installation with Tinkergraph 3.7.3
##################################################

Paste the following commands in a terminal prompt. It installs Exakat most recent version with Tinkergraph 3.7.0. 

Pre-requisite: wget, java (default-jre), php8 (mbstring, sqlite3, curl, phar, tokenizer), unzip.
Make sure that memory_limit=-1 in the php.ini file, or using '-d memory_limit=-1' in the command line.

::

    mkdir exakat
    cd exakat
    wget -O exakat.phar https://www.exakat.io/versions/index.php?file=latest
    wget -O apache-tinkerpop-gremlin-server-3.7.0-bin.zip 'https://www.exakat.io/versions/externals/apache-tinkerpop-gremlin-server-3.7.0-bin.zip'
    unzip apache-tinkerpop-gremlin-server-3.7.0-bin.zip 
    mv apache-tinkerpop-gremlin-server-3.7.0 tinkergraph
    rm -rf apache-tinkerpop-gremlin-server-3.7.0-bin.zip 
    
    # Optional : install neo4j engine.
    cd tinkergraph
    ./bin/gremlin-server.sh install org.apache.tinkerpop neo4j-gremlin 3.7.0
    cd ..

    php exakat.phar doctor


Installation on Debian/Ubuntu
-----------------------------

Debian/Ubuntu installation with Tinkergraph 3.7.0
##################################################

Paste the following commands in a terminal prompt. It installs Exakat most recent version with Tinkergraph 3.7.0. 

Pre-requisite: wget, java (default-jre), php8 (mbstring, sqlite3, curl), unzip.

::

    mkdir exakat
    cd exakat
    wget -O exakat.phar https://www.exakat.io/versions/index.php?file=latest
    wget -O apache-tinkerpop-gremlin-server-3.7.0-bin.zip 'https://www.exakat.io/versions/externals/apache-tinkerpop-gremlin-server-3.7.0-bin.zip'
    unzip apache-tinkerpop-gremlin-server-3.7.0-bin.zip 
    mv apache-tinkerpop-gremlin-server-3.7.0 tinkergraph
    rm -rf apache-tinkerpop-gremlin-server-3.7.0-bin.zip 
    
    # Optional : install neo4j engine.
    cd tinkergraph
    ./bin/gremlin-server.sh install org.apache.tinkerpop neo4j-gremlin 3.7.0
    cd ..

    php exakat.phar doctor


Installation guide with Composer
--------------------------------

Composer installation first run
###############################

To install Exakat with composer, you can use the following commands: 

::

    mkdir exakat
    cd exakat
    echo '{}' > composer.json 
    composer require exakat/exakat:2.6.8 --dev
    php vendor/bin/exakat install -v

The final command checks for the presence of Java and unZip utility. Then, it installs a local copy of a `Gremlin server <http://tinkerpop.apache.org/>`_. This is needed to run Exakat. 

Now, refer to the tutorial to run exakat.

Installation guide with Docker
------------------------------

There are several ways to use exakat with Docker. There is an image with the exakat installation, which run with a traditional installation, or inside the audited code. 

image:: images/exakat-and-docker.png

Docker image for Exakat with projects folder
############################################

Currently, Docker installation only ships with one PHP version (8.4), and with support for git, and zip (downloads).

* Install `Docker <http://www.docker.com/>`_
* Start Docker
* Pull exakat/exakat:latest

The official docker page is `exakat/exakat <https://hub.docker.com/r/exakat/exakat/>`_.

::

    docker pull exakat/exakat:latest

# Check-run exakat : 

::

    mkdir exakat
    cd exakat
    docker run -it -v $(pwd)/projects:/usr/src/exakat/projects --rm --name my-exakat exakat/exakat exakat version
    docker run -it -v $(pwd)/projects:/usr/src/exakat/projects --rm --name my-exakat exakat/exakat exakat doctor

After the last command, there should be an empty 'projects' folder in the 'exakat' folder. With the Docker install, it is possible to analyse code directly inside the code, or with the separate 'projects' folder.

Follow up with the Tutorials.
