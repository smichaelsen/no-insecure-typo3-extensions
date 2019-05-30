# No insecure TYPO3 extensions

This package is inspired by [roave/security-advisories](https://github.com/Roave/SecurityAdvisories). When you require this package it ensures that you can not load TYPO3 extensions in versions with known vulnerabilities.

Project status: This package is relatively new and not widely used yet. I've built this with best intentions and to my best knowledge. Nevertheless this comes without guarantee. Do not hold me responsible in case something unexpected/undesired happens.

## Usage

`composer require smichaelsen/no-insecure-typo3-extensions`

From now on when you require a TYPO3 extension that has known security issues (according to the rating in the TER by the TYPO3 security team) you will get a composer conflict on `composer update`.

## Does this make my project (more) secure?

When you are maintaining TYPO3 projects it's your responsibility to stay up to date with [security advisories](https://typo3.org/help/security-advisories/) and best practices. This package can not take this responsibility from you. However it can be an additional security measure.

## Which TYPO3 extensions are covered?

This package relies on information from the [TYPO3 TER](https://extensions.typo3.org/) - so only extensions that are published there are covered. It also covers Extensions published via packagist, when they are available in the TER.

## How (often) is it updated?

[This project](https://git.maschinenraum.digital/smichaelsen/no-insecure-extensions-updater/) checks the TER extension list for updated security information twice a day updates this package when necessary.
