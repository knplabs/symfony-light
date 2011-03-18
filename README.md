Symfony Empty Edition
=================

What's inside?
--------------

Symfony Empty Edition comes pre-configured with the following bundles:

 * FrameworkBundle
 * SecurityBundle ( see security.yml.dist file )
 * SensioFrameworkExtraBundle
 * SecurityExtraBundle ( see config.yml.dist file )
 * DoctrineBundle ( see config.yml.dist file )
 * TwigBundle
 * SwiftmailerBundle ( see config.yml.dist file )
 * ZendBundle
 * AsseticBundle
 * WebProfilerBundle (in dev/test env)

Installation
---------------------

This distribution is made to be extracted in an empty git repository, in order to initiate a new Symfony2 project.
Nothing special, just extract and run it!

You can simply download it via `https://github.com/docteurklein/symfony-empty/tarball/master` and unpack it.

    wget --no-check-certificate https://github.com/docteurklein/symfony-empty/tarball/master -O master.tar.gz
    tar -xzvf master.tar.gz
    mv *-symfony-empty-* my-project
    cd my-project


**This requires you to be in a working git repository, at root level.**
If you are not, you can init a new repository in the current folder by simply typing:

    git init

Run the following script:

 * `./bin/vendors.sh`

It will install all submodules.



Configuration
-------------

The distribution is configured with the following defaults:

 * Twig is the only configured template engine;
 * Doctrine ORM/DBAL is configured ( see config.yml.dist file );
 * Swiftmailer is configured ( see config.yml.dist file );
 * Annotations for everything are enabled ( see config.yml.dist file ).

If you have special configurations depending on your machine or environment, you can override any config_*.yml
For example, if you have a different database password than the default one, you can modifiy by adding a file named `config_dev_local.yml`:

    doctrine:
        dbal:
            connections:
                default:
                    dbname:        my_symfony_empty_special_db_name
                    user:             florian
                    password:     chaaaangeMe


If you want to use the CLI, a console application is available at
`app/console`. Check first that your PHP is correctly configured for the CLI
by running `app/check.php`.

Enjoy!