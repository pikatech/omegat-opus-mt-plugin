# OmegaT Opus-MT plugin

This plugin lets you add a custom remote Machine Translator. The plugin is meant to be used in conjunction with a REST service running an
Opus-MT translation model. A matching service can be found under https://github.com/pikatech/opus-mt-rest-service.

You can configure four parameters in the MT configuration window.

* __URL__: the URL to connect to
* __source__: The name of the source parameter that will take the source language.
* __target__: The name of the target parameter that will take the target language.
* __source__: The name of the text parameter that will take the content of the segment to be translated.

`GET ${url}?${source}=en-US&${target}=fr-FR&${text}=Hello World!` 

## Caveat

There are currently several limitations, for this plugin:

* only one custom MT can be used,
* the HTTP method used is always GET
* the expected response is in JSON with the schema `{"translation": "Hello World!"}` 
* When changing the name of the MT, the changes are effective after restarting the application

## Installation

You can get a plugin jar file from zip/tgz distribution file.
The OmegaT plugin should be placed in `$HOME/.omegat/plugins` or `C:\Program Files\OmegaT\plugins`
depending on your operating system.

## License

This project is distributed under the GNU general public license version 3 or later.

