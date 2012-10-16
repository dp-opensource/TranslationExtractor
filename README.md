transbundle
===========

Installation:

deps

    [TranslationExtractor]
    git=git@github.com:digitalpioneers/TranslationExtractor.git
    target=bundles/TransBundle

autoload.php (in the $loader->registerNamespaces array)

    $loader-registerNamespaces( array(
    (...),
    'TransBundle'                    => __DIR__.'/.../vendor/bundles',
    (...),
    );

AppKernel.php (in the registerBundles() function)

    public function registerBundles() {
        $bundles = array(
        ...,
        new TransBundle\TransBundle(),
        ...
        );

        (...)
    }



- Extract messages from LaserBundle and write to stdout

    `trans:update --dump-messages de DrEvil\LaserBundle`

- Save messages to LaserBundle/Resources/translations

    `trans:update --force de DrEvil\LaserBundle`

- Specify the desired language

    `trans:update --force en DrEvil\LaserBundle`

- Set output format with `--output-format` (`yml`, `xliff`, `php`, `pot`):

    `trans:update --output-format="xliff" --force en DrEvil\LaserBundle`

- Change the prefix used for newly added messages with the `--prefix` option:

    `trans:update --output-format="xliff" --force --prefix='myprefix' en DrEvil\LaserBundle`
