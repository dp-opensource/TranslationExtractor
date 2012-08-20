transbundle
===========

- Extract messages from LaserBundle and write to stdout

    `trans:update --dump-messages de DrEvil\LaserBundle`

- Save messages to LaserBundle/Resources/translations

    `trans:update --force de DrEvil\LaserBundle`

- Specify the desired language

    `trans:update --force en DrEvil\LaserBundle`

- Set output format with `--output-format` (`yml`, `xliff`, `php`, `pot`):

    `trans:update --output-format="xliff" --force en DrEvil\LaserBundle`

- Change the prefix used for newly added messages with the `--prefix` option:

    `trans:update --output-format="xliff" --force --prefix='myprefix' en MyBundle`
