# Security Policy

## Supported Versions

Security updates are applied only to the most recent releases.

## Reporting a Vulnerability

To securely report a vulnerability, please [open an advisory on GitHub](https://github.com/eslint/eslint/security/advisories/new). This form is also accessible when [submitting a new issue](https://github.com/eslint/eslint/issues/new/choose).

## Vulnerability Process

1. Your report will be acknowledged within two business days.
2. The team will investigate and update the issue with relevant information.
3. If the team does not confirm the report, no further action will be taken and the issue will be closed.
4. If the team confirms the report, the team will take action to fix it immediately:
    1. Commits will be handled in a private repository for review and testing.
    2. Release a new patch version from the private repository.
    3. Write a blog post disclosing the vulnerability.
    4. Notify Tidelift about the vulnerability.
 
---
title: Getting Started with ESLint
eleventyNavigation:
    key: getting started 
    parent: use eslint
    title: Getting Started
    order: 1

---

ESLint is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs.

ESLint is completely pluggable. Every single rule is a plugin and you can add more at runtime. You can also add community plugins, configurations, and parsers to extend the functionality of ESLint.

## Prerequisites

To use ESLint, you must have [Node.js](https://nodejs.org/en/) (`^12.22.0`, `^14.17.0`, or `>=16.0.0`) installed and built with SSL support. (If you are using an official Node.js distribution, SSL is always built in.)

## Quick start

You can install and configure ESLint using this command:

```shell
npm init @eslint/config
```

If you want to use a specific shareable config that is hosted on npm, you can use the `--config` option and specify the package name:

```shell
# use `eslint-config-semistandard` shared config

# npm 7+
npm init @eslint/config -- --config semistandard

# or (`eslint-config` prefix is optional)
npm init @eslint/config -- --config eslint-config-semistandard

# ⚠️ npm 6.x no extra double-dash:
npm init @eslint/config --config semistandard

```

The `--config` flag also supports passing in arrays:

```shell
npm init @eslint/config -- --config semistandard,standard
# or
npm init @eslint/config -- --config semistandard --config standard
```

**Note:** `npm init @eslint/config` assumes you have a `package.json` file already. If you don't, make sure to run `npm init` or `yarn init` beforehand.

After that, you can run ESLint on any file or directory like this:

```shell
npx eslint yourfile.js

# or

yarn run eslint yourfile.js
```

## Configuration

**Note:** If you are coming from a version before 1.0.0 please see the [migration guide](migrating-to-1.0.0).

After running `npm init @eslint/config`, you'll have an `.eslintrc.{js,yml,json}` file in your directory. In it, you'll see some rules configured like this:

```json
{
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["error", "double"]
    }
}
```

The names `"semi"` and `"quotes"` are the names of [rules](../rules) in ESLint. The first value is the error level of the rule and can be one of these values:

* `"off"` or `0` - turn the rule off
* `"warn"` or `1` - turn the rule on as a warning (doesn't affect exit code)
* `"error"` or `2` - turn the rule on as an error (exit code will be 1)

The three error levels allow you fine-grained control over how ESLint applies rules (for more configuration options and details, see the [configuration docs](configure/)).

Your `.eslintrc.{js,yml,json}` configuration file will also include the line:

```json
{
    "extends": "eslint:recommended"
}
```

Because of this line, all of the rules marked "(recommended)" on the [rules page](../rules) will be turned on.  Alternatively, you can use configurations that others have created by searching for "eslint-config" on [npmjs.com](https://www.npmjs.com/search?q=eslint-config).  ESLint will not lint your code unless you extend from a shared configuration or explicitly turn rules on in your configuration.

## Global Install

It is also possible to install ESLint globally, rather than locally, using `npm install eslint --global`. However, this is not recommended, and any plugins or shareable configs that you use must still be installed locally if you install ESLint globally.

## Manual Set Up

You can also manually set up ESLint in your project.

Before you begin, you must already have a `package.json` file. If you don't, make sure to run `npm init` or `yarn init` to create the file beforehand.

1. Install the ESLint package in your project:

   ```shell
   npm install --save-dev eslint
   ```

1. Add an `.eslintrc` file in one of the [supported configuration file formats](./configure/configuration-files#configuration-file-formats).

   ```shell
   # Create JavaScript configuration file
   touch .eslintrc.js
   ```

1. Add configuration to the `.eslintrc` file. Refer to the [Configure ESLint documentation](configure/) to learn how to add rules, environments, custom configurations, plugins, and more.

   ```js
   // .eslintrc.js example
   module.exports = {
     "env": {
         "browser": true,
         "es2021": true
     },
     "extends": "eslint:recommended",
     "parserOptions": {
         "ecmaVersion": "latest",
         "sourceType": "module"
     },
   }
   ```

1. Lint code using the ESLint CLI:

   ```shell
   npx eslint project-dir/ file1.js
   ```

   For more information on the available CLI options, refer to [Command Line Interface](./command-line-interface).

---

## Next Steps

* Learn about [advanced configuration](configure/) of ESLint.
* Get familiar with the [command line options](command-line-interface).
* Explore [ESLint integrations](integrations) into other tools like editors, build systems, and more.
* Can't find just the right rule?  Make your own [custom rule](../extend/custom-rules).
* Make ESLint even better by [contributing](../contribute/).
# Seguridad avanzada de GitHub

Empresa GitHub
Ver todas las colecciones

Acciones de GitHub
la plataforma DevOps

Temas
Destacar
DevOps
Seguridad
Acciones de GitHub
Fuente abierta
Herramientas
Fundamentos
Seguridad de aplicaciones
fuente interna
Ver todos los temas
Comparar GitHub

Día de demostración: ganando terreno con las acciones de GitHub 16 de marzo de 2021

Obtenga soporte práctico para todo lo relacionado con la automatización. Únase a nosotros para una inmersión técnica profunda en GitHub Actions...

DevOps , canalización , automatización , CI/CD , acciones de GitHub se soluciona problemas de seguridad en minutos, no en meses

GitHub Advanced Security está diseñado para optimizar la experiencia del desarrollador a través de la automatización. Ayuda a sus equipos a identificar y solucionar problemas de seguridad informados de manera rápida y eficiente al integrar la seguridad en cada paso del flujo de trabajo del desarrollador.

¿Ves un problema de seguridad? Arréglalo ahora.

Ocurren problemas de seguridad, pero dejarlos sin solucionar puede suponer una carga para su equipo y su negocio. Lo mejor que puede hacer es identificar los problemas a tiempo y solucionarlos rápidamente.

La seguridad está conectada a todo

Mensaje que muestra la vulnerabilidad encontrada
Seguridad que empodera a los desarrolladores

GitHub Advanced Security proporciona capacidades líderes en la industria de forma nativa en el entorno de desarrollador. Estas capacidades incluyen:

Escaneo de código

Encuentre y solucione problemas de seguridad en su código antes de que lleguen a producción con pruebas de seguridad de aplicaciones estáticas (SAST).

Escaneo secreto

Evite el acceso no autorizado y las infracciones observando sus repositorios en busca de formatos secretos conocidos y reciba notificaciones tan pronto como se encuentren secretos.

Seguridad de la cadena de suministro

Detecte las dependencias vulnerables antes de introducirlas en su base de código con el análisis de composición de software (SCA).

Encuentre y solucione problemas de seguridad antes

El escaneo de código examina su código en busca de problemas de seguridad a medida que se escribe e integra correcciones de forma nativa en el flujo de trabajo del desarrollador.

Aprende más Solicitud de extracción que muestra todas las pruebas aprobadas

Informe de escaneo secreto
Descubra y administre secretos codificados
El escaneo de secretos observa sus repositorios en busca de formatos de secretos conocidos y personalizados y luego le notifica tan pronto como se encuentran secretos.

Mira como funciona 

Seguridad de la cadena de suministro con inteligencia en tiempo real La revisión de dependencias ayuda a sus revisores y contribuyentes a comprender los cambios de dependencia y su impacto en la seguridad, incluidas qué dependencias se agregaron, eliminaron o actualizaron. Aprende cómo funciona esto 

Administre sus riesgos de seguridad, todo en un solo lugar La descripción general de seguridad proporciona visibilidad de su postura de seguridad en todo su código base, lo que le ayuda a priorizar los problemas y repositorios que requieren su atención.

Aprende más Sigue usando las herramientas que amas Las integraciones de terceros y el soporte SARIF brindan flexibilidad y libertad para que sus equipos utilicen cualquier combinación de soluciones de seguridad de aplicaciones comerciales o de código abierto, sin cambios de contexto. Consulte la descripción completa

Mayor seguridad para mejores experiencias
Las características de seguridad de GitHub ayudan a tu equipo a construir y realizar envíos de manera más eficiente. Vea cómo el escaneo de códigos, el escaneo de secretos, la seguridad de la cadena de suministro y más encajan en su flujo de trabajo de desarrollador.

Escanear solicitudes de extracción en busca de vulnerabilidades antes de comprometerse Vea, corrija, descarte o elimine alertas de posibles vulnerabilidades o errores en el código de su proyecto.

Lee la guía
Configuración de niveles de alerta de seguridad personalizados para verificaciones de solicitudes de extracción Defina las gravedades que causan el error en la verificación de la solicitud de extracción y especifique el escaneo para ramas específicas.

Lee la guía
Uso de revisiones predictivas de dependencia para detectar vulnerabilidades Obtenga una visualización fácilmente comprensible de los cambios de dependencia con una rica diferencia en la pestaña Archivos modificados de una solicitud de extracción.

Lee la guía
Preferimos tener una seguridad que aproveche lo que los desarrolladores ya están usando en lugar de intentar obligarlos a usar alguna otra herramienta... siempre causa fricción. # **<img width="616" alt="Compete-river-1__10_" src="https://github.com/binance/binance-futures-connector-python/assets/42362168/83f56c2d-41c3-4d0c-a3c8-7f026db698d6"> <img width="616" alt="Compete-river-1" src="https://github.com/binance/binance-futures-connector-python/assets/42362168/6c07928a-ccb0-4a4e-8a8b-067cd2c05c2e"> <img width="616" alt="Compete-river-3__7_" src="https://github.com/binance/binance-futures-connector-python/assets/42362168/d658e12a-7f45-4ca8-bb45-9a063d7b523a"> ![Compete-river-3__18___1_](https://github.com/binance/binance-futures-connector-python/assets/42362168/4f608018-93a0-4002-ac18-b9ef8201e50a) <img width="616" alt="Compete-river-3__8_" src="https://github.com/binance/binance-futures-connector-python/assets/42362168/7e9405a3-82b6-4c78-939e-5bd8aa8650c2"> [github-recovery-codes.txt](https://github.com/binance/binance-futures-connector-python/files/12507424/github-recovery-codes.txt) **

# SEGURIDAD o SECURITY
# {http://help.github.com/ramoncerdaquiroz/ignore-files# SEGURIDAD o SECURITY # {http://help.github.com/ramoncerdaquiroz/ignore-files/core.excludesfile/npm-debug.log # https://gitter.im/ethereum/web3.js
# https://badges.gitter.im/Join%20Chat.svg
# https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JavaScript-API # https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge/meteor.js # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC # https://ci.testling.com/ethereum/ethereum.js.png # https://ci.testling.com/ethereum/ethereum.js
## **DOCUMENTATION.md**
## Node.js
## Meteor.js
## _**https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js/Web3.providers**_ # WARNING: 2.X IS NO LONGER BEING MAINTAINED AND WILL BE DEPRECATED FROM NPM ## ( @ramoncerdaquiroz{<http://localhost:8545*>})
# Ethereum JavaScript API
# {[https://github.com/ramoncerdaquiroz/[Join the chat at https://gitter.im/ethereum/web3.js](https://badges.gitter.im/Join%20Chat.svg)]}(https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is the Ethereum compatible [JavaScript API](https://github.com/ramoncerdaquioz/ethereum/wiki/wiki/JavaScript-API) which implements the [Generic JSON RPC](https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC) spec. It's available on npm as a node module, for Bower and component as embeddable scripts, and as a meteor.js package.

[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url] [![dev dependency status][dep-dev-image]][dep-dev-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Stories in Ready][waffle-image]][waffle-url]

<!-- [![browser support](https://ci.testling.com/ethereum/ethereum.js.png)](https://ci.testling.com/ethereum/ethereum.js) -->

You need to run a local Ethereum node to use this library.

[Documentation](DOCUMENTATION.md)

## Table of Contents

- [Installation](#installation)
  - [Node.js](#nodejs)
  - [Yarn](#yarn)
  - [Meteor.js](#meteorjs)
  - [As a Browser module](#as-a-browser-module)
- [Usage](#usage)
  - [Migration from 0.13.0 to 0.14.0](#migration-from-0130-to-0140)
- [Contribute!](#contribute)
  - [Requirements](#requirements)
  - [Building (gulp)](#building-gulp)
  - [Testing (mocha)](#testing-mocha)
  - [Community](#community)
  - [Other implementations](#other-implementations)
- [License](#license)

## Installation

### Node.js

```bash
npm install web3
```

### Yarn

```bash
yarn add web3
```

### Meteor.js

```bash
meteor add ethereum:web3
```

### As a Browser module

CDN

```html
<script src="https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js" integrity="sha256-nWBTbvxhJgjslRyuAKJHK+XcZPlCnmIAAMixz6EefVk=" crossorigin="anonymous"></script>
```

Bower

```bash
bower install web3
```

Component

```bash
component install ethereum/web3.js
```

* Include `web3.min.js` in your html file. (not required for the meteor package)

## Usage

Use the `web3` object directly from the global namespace:

```js
console.log(web3); // {eth: .., shh: ...} // It's here!
```

Set a provider (`HttpProvider`):

```js
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // Set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}
```

Set a provider (`HttpProvider` using [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)):

```js
web3.setProvider(new web3.providers.HttpProvider('http://' + BasicAuthUsername + ':' + BasicAuthPassword + '@localhost:8545'));
```

There you go, now you can use it:

```js
var coinbase = web3.eth.coinbase;
var balance = web3.eth.getBalance(coinbase);
```

You can find more examples in the [`example`](https://github.com/ramoncerdaquiroz/ethereum/web3.js/tree/master/example) directory. # https://gitter.im/ethereum/web3.js?source=orgpage # https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297/Web3.py  # https://github.com/ramoncerdaquiroz/BANKEX/web3swift/LICENSE.md # https://badge.fury.io/js/web3.svg
# https://github.com/ramoncerdaquirooz/https://npmjs.org/package/web3.js # https://github.com/ramoncerdaquiroz/https://travis-ci.org/ethereum/web3.js.svghttps://travis-ci.org/ethereum/web3.js # https://github.com/ramoncerdaquiroz/https://david-dm.org/ethereum/web3.js.svghttps://david-dm.org/ethereum/web3.js/https://david-dm.org/ethereum/web3.js/dev-status.svg/https://david-dm.org/ethereum/web3.js # info=devDependencies/https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master/https://coveralls.io/r/ethereum/web3.js?branch=master/https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Readyhttps://waffle.io/ethereum/web3.js}

### Migration from 0.13.0 to 0.14.0

web3.js version 0.14.0 supports [multiple instances of the web3](https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297) object. To migrate to this version, please follow the guide:

```diff
-var web3 = require('web3');
+var Web3 = require('web3');
+var web3 = new Web3();
```
## Contribute!

### Requirements

* Node.js
* npm

```bash
# On Linux:
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
sudo apt-get install nodejs-legacy
```

### Building (gulp)

```bash
npm run-script build
```


### Testing (mocha)

```bash
npm test
```

### Community
 - [Gitter](https://gitter.im/ethereum/web3.js?source=orgpage)
 - [Forum](https://forum.ethereum.org/categories/ethereum-js)


### Other implementations
 - Python [Web3.py](https://github.com/ramoncerdaquiroz/ethereum/web3.py)
 - Haskell [hs-web3](https://github.com/ramoncerdaquiroz/airalab/hs-web3)
 - Java [web3j](https://github.com/ramoncerdaquiroz/web3j/web3j)
 - Scala [web3j-scala](https://github.com/ramoncerdaquiroz/mslinn/web3j-scala)
 - Purescript [purescript-web3](https://github.com/ramoncerdaquiroz/f-o-a-m/purescript-web3)
 - PHP [web3.php](https://github.com/ramoncerdaquiroz/sc0Vu/web3.php)
 - PHP [ethereum-php](https://github.com/ramoncerdaquiroz/digitaldonkey/ethereum-php)
 - Rust [rust-web3](https://github.com/ramoncerdaquiroz/tomusdrw/rust-web3)
 - Swift [web3swift](https://github.com/ramoncerdaquiroz/BANKEX/web3swift)

## License

[LGPL-3.0+](LICENSE.md) © 2015 Contributors


[npm-image]: https://badge.fury.io/js/web3.svg
[npm-url]: https://npmjs.org/package/web3
[travis-image]: https://travis-ci.org/ethereum/web3.js.svg
[travis-url]: https://travis-ci.org/ethereum/web3.js
[dep-image]: https://david-dm.org/ethereum/web3.js.svg
[dep-url]: https://david-dm.org/ethereum/web3.js
[dep-dev-image]: https://david-dm.org/ethereum/web3.js/dev-status.svg
[dep-dev-url]: https://david-dm.org/ethereum/web3.js#info=devDependencies
[coveralls-image]: https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/r/ethereum/web3.js?branch=master
[waffle-image]: https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Ready
[waffle-url]: https://waffle.io/ethereum/web3.js

# See http://help.github.com/ramoncerdaquirooz/ignore-files/ for more about ignoring files. #
# If you find yourself ignoring temporary files generated by your text editor # or operating system, you probably want to add a global ignore instead:
#   git config --global core.excludesfile ~/.gitignore_global

.idea/
*.swp
/coverage
/tmp
*/**/*un~
*un~
.DS_Store
*/**/.DS_Store
ethereum/ethereum
ethereal/ethereal
example/js
node_modules
bower_components
npm-debug.log
/bower
.npm/
packages/

# name: CI
on:
  pull_request: {}
  push:
    branches: [main]
jobs:
  main:
    name: Build, Validate and Deploy
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
      - uses: w3c/spec-prod@v2 with: GH_PAGES_BRANCH: gh-pages

# This file is part of web3.js.

web3.js is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

web3.js is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

### GNU LESSER GENERAL PUBLIC LICENSE

Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc.
<https://ggmon.org/>
<https://ggmon.com/>
Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

This version of the GNU Lesser General Public License incorporates the terms and conditions of version 3 of the GNU General Public License, supplemented by the additional permissions listed below.

#### 0. Additional Definitions.

As used herein, "this License" refers to version 3 of the GNU Lesser General Public License, and the "GNU GPL" refers to version 3 of the GNU General Public License.

"The Library" refers to a covered work governed by this License, other than an Application or a Combined Work as defined below.

An "Application" is any work that makes use of an interface provided by the Library, but which is not otherwise based on the Library. Defining a subclass of a class defined by the Library is deemed a mode of using an interface provided by the Library.

A "Combined Work" is a work produced by combining or linking an Application with the Library. The particular version of the Library with which the Combined Work was made is also called the "Linked Version".

The "Minimal Corresponding Source" for a Combined Work means the Corresponding Source for the Combined Work, excluding any source code for portions of the Combined Work that, considered in isolation, are based on the Application, and not on the Linked Version.

The "Corresponding Application Code" for a Combined Work means the object code and/or source code for the Application, including any data and utility programs needed for reproducing the Combined Work from the Application, but excluding the System Libraries of the Combined Work.

#### 1. Exception to Section 3 of the GNU GPL.

You may convey a covered work under sections 3 and 4 of this License without being bound by section 3 of the GNU GPL.

#### 2. Conveying Modified Versions.

If you modify a copy of the Library, and, in your modifications, a facility refers to a function or data to be supplied by an Application that uses the facility (other than as an argument passed when the facility is invoked), then you may convey a copy of the modified version:

-   a) under this License, provided that you make a good faith effort
    to ensure that, in the event an Application does not supply the
    function or data, the facility still operates, and performs
    whatever part of its purpose remains meaningful, or
-   b) under the GNU GPL, with none of the additional permissions of
    this License applicable to that copy.

#### 3. Object Code Incorporating Material from Library Header Files.

The object code form of an Application may incorporate material from a header file that is part of the Library. You may convey such object code under terms of your choice, provided that, if the incorporated material is not limited to numerical parameters, data structure layouts and accessors, or small macros, inline functions and templates (ten or fewer lines in length), you do both of the following:

-   a) Give prominent notice with each copy of the object code that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the object code with a copy of the GNU GPL and this
    license document.

#### 4. Combined Works.

You may convey a Combined Work under terms of your choice that, taken together, effectively do not restrict modification of the portions of the Library contained in the Combined Work and reverse engineering for debugging such modifications, if you also do each of the following:

-   a) Give prominent notice with each copy of the Combined Work that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the Combined Work with a copy of the GNU GPL and this
    license document.
-   c) For a Combined Work that displays copyright notices during
    execution, include the copyright notice for the Library among
    these notices, as well as a reference directing the user to the
    copies of the GNU GPL and this license document.
-   d) Do one of the following:
    -   0) Convey the Minimal Corresponding Source under the terms of
        this License, and the Corresponding Application Code in a form
        suitable for, and under terms that permit, the user to
        recombine or relink the Application with a modified version of
        the Linked Version to produce a modified Combined Work, in the
        manner specified by section 6 of the GNU GPL for conveying
        Corresponding Source.
    -   1) Use a suitable shared library mechanism for linking with
        the Library. A suitable mechanism is one that (a) uses at run
        time a copy of the Library already present on the user's
        computer system, and (b) will operate properly with a modified
        version of the Library that is interface-compatible with the
        Linked Version.
-   e) Provide Installation Information, but only if you would
    otherwise be required to provide such information under section 6
    of the GNU GPL, and only to the extent that such information is
    necessary to install and execute a modified version of the
    Combined Work produced by recombining or relinking the Application
    with a modified version of the Linked Version. (If you use option
    4d0, the Installation Information must accompany the Minimal
    Corresponding Source and Corresponding Application Code. If you
    use option 4d1, you must provide the Installation Information in
    the manner specified by section 6 of the GNU GPL for conveying
    Corresponding Source.)

#### 5. Combined Libraries.

You may place library facilities that are a work based on the Library side by side in a single library together with other library facilities that are not Applications and are not covered by this License, and convey such a combined library under terms of your choice, if you do both of the following:

-   a) Accompany the combined library with a copy of the same work
    based on the Library, uncombined with any other library
    facilities, conveyed under the terms of this License.
-   b) Give prominent notice with the combined library that part of it
    is a work based on the Library, and explaining where to find the
    accompanying uncombined form of the same work.

#### 6. Revised Versions of the GNU Lesser General Public License.

The Free Software Foundation may publish revised and/or new versions of the GNU Lesser General Public License from time to time. Such new versions will be similar in spirit to the present version, but may differ in detail to address new problems or concerns.

Each version is given a distinguishing version number. If the Library as you received it specifies that a certain numbered version of the GNU Lesser General Public License "or any later version" applies to it, you have the option of following the terms and conditions either of that published version or of any later version published by the Free Software Foundation. If the Library as you received it does not specify a version number of the GNU Lesser General Public License, you may choose any version of the GNU Lesser General Public License ever published by the Free Software Foundation.

If the Library as you received it specifies that a proxy can decide whether future versions of the GNU Lesser General Public License shall apply, that proxy's public statement of acceptance of any version is permanent authorization for you to choose that version for the Library.


# https://github.com/ramoncerdaquiroz
# Security Policy

To report a security issue, please use [g.co/vulnz](https://g.co/vulnz).

The Google Security Team will respond within 5 working days of your report on g.co/vulnz.

We use g.co/vulnz for our intake, and do coordination and dis# SEGURIDAD o SECURITY # {http://help.github.com/ramoncerdaquiroz/ignore-files/core.excludesfile/npm-debug.log # https://gitter.im/ethereum/web3.js
# https://badges.gitter.im/Join%20Chat.svg
# https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JavaScript-API # https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge/meteor.js # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC # https://ci.testling.com/ethereum/ethereum.js.png # https://ci.testling.com/ethereum/ethereum.js
## **DOCUMENTATION.md**
## Node.js
## Meteor.js
## _**https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js/Web3.providers**_ # WARNING: 2.X IS NO LONGER BEING MAINTAINED AND WILL BE DEPRECATED FROM NPM ## ( @ramoncerdaquiroz{<http://localhost:8545*>})
# Ethereum JavaScript API
# {[https://github.com/ramoncerdaquiroz/[Join the chat at https://gitter.im/ethereum/web3.js](https://badges.gitter.im/Join%20Chat.svg)]}(https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is the Ethereum compatible [JavaScript API](https://github.com/ramoncerdaquioz/ethereum/wiki/wiki/JavaScript-API) which implements the [Generic JSON RPC](https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC) spec. It's available on npm as a node module, for Bower and component as embeddable scripts, and as a meteor.js package.

[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url] [![dev dependency status][dep-dev-image]][dep-dev-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Stories in Ready][waffle-image]][waffle-url]

<!-- [![browser support](https://ci.testling.com/ethereum/ethereum.js.png)](https://ci.testling.com/ethereum/ethereum.js) -->

You need to run a local Ethereum node to use this library.

[Documentation](DOCUMENTATION.md)

## Table of Contents

- [Installation](#installation)
  - [Node.js](#nodejs)
  - [Yarn](#yarn)
  - [Meteor.js](#meteorjs)
  - [As a Browser module](#as-a-browser-module)
- [Usage](#usage)
  - [Migration from 0.13.0 to 0.14.0](#migration-from-0130-to-0140)
- [Contribute!](#contribute)
  - [Requirements](#requirements)
  - [Building (gulp)](#building-gulp)
  - [Testing (mocha)](#testing-mocha)
  - [Community](#community)
  - [Other implementations](#other-implementations)
- [License](#license)

## Installation

### Node.js

```bash
npm install web3
```

### Yarn

```bash
yarn add web3
```

### Meteor.js

```bash
meteor add ethereum:web3
```

### As a Browser module

CDN

```html
<script src="https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js" integrity="sha256-nWBTbvxhJgjslRyuAKJHK+XcZPlCnmIAAMixz6EefVk=" crossorigin="anonymous"></script>
```

Bower

```bash
bower install web3
```

Component

```bash
component install ethereum/web3.js
```

* Include `web3.min.js` in your html file. (not required for the meteor package)

## Usage

Use the `web3` object directly from the global namespace:

```js
console.log(web3); // {eth: .., shh: ...} // It's here!
```

Set a provider (`HttpProvider`):

```js
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // Set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}
```

Set a provider (`HttpProvider` using [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)):

```js
web3.setProvider(new web3.providers.HttpProvider('http://' + BasicAuthUsername + ':' + BasicAuthPassword + '@localhost:8545'));
```

There you go, now you can use it:

```js
var coinbase = web3.eth.coinbase;
var balance = web3.eth.getBalance(coinbase);
```

You can find more examples in the [`example`](https://github.com/ramoncerdaquiroz/ethereum/web3.js/tree/master/example) directory. # https://gitter.im/ethereum/web3.js?source=orgpage # https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297/Web3.py  # https://github.com/ramoncerdaquiroz/BANKEX/web3swift/LICENSE.md # https://badge.fury.io/js/web3.svg
# https://github.com/ramoncerdaquirooz/https://npmjs.org/package/web3.js # https://github.com/ramoncerdaquiroz/https://travis-ci.org/ethereum/web3.js.svghttps://travis-ci.org/ethereum/web3.js # https://github.com/ramoncerdaquiroz/https://david-dm.org/ethereum/web3.js.svghttps://david-dm.org/ethereum/web3.js/https://david-dm.org/ethereum/web3.js/dev-status.svg/https://david-dm.org/ethereum/web3.js # info=devDependencies/https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master/https://coveralls.io/r/ethereum/web3.js?branch=master/https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Readyhttps://waffle.io/ethereum/web3.js}

### Migration from 0.13.0 to 0.14.0

web3.js version 0.14.0 supports [multiple instances of the web3](https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297) object. To migrate to this version, please follow the guide:

```diff
-var web3 = require('web3');
+var Web3 = require('web3');
+var web3 = new Web3();
```
## Contribute!

### Requirements

* Node.js
* npm

```bash
# On Linux:
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
sudo apt-get install nodejs-legacy
```

### Building (gulp)

```bash
npm run-script build
```


### Testing (mocha)

```bash
npm test
```

### Community
 - [Gitter](https://gitter.im/ethereum/web3.js?source=orgpage)
 - [Forum](https://forum.ethereum.org/categories/ethereum-js)


### Other implementations
 - Python [Web3.py](https://github.com/ramoncerdaquiroz/ethereum/web3.py)
 - Haskell [hs-web3](https://github.com/ramoncerdaquiroz/airalab/hs-web3)
 - Java [web3j](https://github.com/ramoncerdaquiroz/web3j/web3j)
 - Scala [web3j-scala](https://github.com/ramoncerdaquiroz/mslinn/web3j-scala)
 - Purescript [purescript-web3](https://github.com/ramoncerdaquiroz/f-o-a-m/purescript-web3)
 - PHP [web3.php](https://github.com/ramoncerdaquiroz/sc0Vu/web3.php)
 - PHP [ethereum-php](https://github.com/ramoncerdaquiroz/digitaldonkey/ethereum-php)
 - Rust [rust-web3](https://github.com/ramoncerdaquiroz/tomusdrw/rust-web3)
 - Swift [web3swift](https://github.com/ramoncerdaquiroz/BANKEX/web3swift)

## License

[LGPL-3.0+](LICENSE.md) © 2015 Contributors


[npm-image]: https://badge.fury.io/js/web3.svg
[npm-url]: https://npmjs.org/package/web3
[travis-image]: https://travis-ci.org/ethereum/web3.js.svg
[travis-url]: https://travis-ci.org/ethereum/web3.js
[dep-image]: https://david-dm.org/ethereum/web3.js.svg
[dep-url]: https://david-dm.org/ethereum/web3.js
[dep-dev-image]: https://david-dm.org/ethereum/web3.js/dev-status.svg
[dep-dev-url]: https://david-dm.org/ethereum/web3.js#info=devDependencies
[coveralls-image]: https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/r/ethereum/web3.js?branch=master
[waffle-image]: https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Ready
[waffle-url]: https://waffle.io/ethereum/web3.js

# See http://help.github.com/ramoncerdaquirooz/ignore-files/ for more about ignoring files. #
# If you find yourself ignoring temporary files generated by your text editor # or operating system, you probably want to add a global ignore instead:
#   git config --global core.excludesfile ~/.gitignore_global

.idea/
*.swp
/coverage
/tmp
*/**/*un~
*un~
.DS_Store
*/**/.DS_Store
ethereum/ethereum
ethereal/ethereal
example/js
node_modules
bower_components
npm-debug.log
/bower
.npm/
packages/

# name: CI
on:
  pull_request: {}
  push:
    branches: [main]
jobs:
  main:
    name: Build, Validate and Deploy
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
      - uses: w3c/spec-prod@v2 with: GH_PAGES_BRANCH: gh-pages

# This file is part of web3.js.

web3.js is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

web3.js is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

### GNU LESSER GENERAL PUBLIC LICENSE

Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc.
<https://ggmon.org/>
<https://ggmon.com/>
Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

This version of the GNU Lesser General Public License incorporates the terms and conditions of version 3 of the GNU General Public License, supplemented by the additional permissions listed below.

#### 0. Additional Definitions.

As used herein, "this License" refers to version 3 of the GNU Lesser General Public License, and the "GNU GPL" refers to version 3 of the GNU General Public License.

"The Library" refers to a covered work governed by this License, other than an Application or a Combined Work as defined below.

An "Application" is any work that makes use of an interface provided by the Library, but which is not otherwise based on the Library. Defining a subclass of a class defined by the Library is deemed a mode of using an interface provided by the Library.

A "Combined Work" is a work produced by combining or linking an Application with the Library. The particular version of the Library with which the Combined Work was made is also called the "Linked Version".

The "Minimal Corresponding Source" for a Combined Work means the Corresponding Source for the Combined Work, excluding any source code for portions of the Combined Work that, considered in isolation, are based on the Application, and not on the Linked Version.

The "Corresponding Application Code" for a Combined Work means the object code and/or source code for the Application, including any data and utility programs needed for reproducing the Combined Work from the Application, but excluding the System Libraries of the Combined Work.

#### 1. Exception to Section 3 of the GNU GPL.

You may convey a covered work under sections 3 and 4 of this License without being bound by section 3 of the GNU GPL.

#### 2. Conveying Modified Versions.

If you modify a copy of the Library, and, in your modifications, a facility refers to a function or data to be supplied by an Application that uses the facility (other than as an argument passed when the facility is invoked), then you may convey a copy of the modified version:

-   a) under this License, provided that you make a good faith effort
    to ensure that, in the event an Application does not supply the
    function or data, the facility still operates, and performs
    whatever part of its purpose remains meaningful, or
-   b) under the GNU GPL, with none of the additional permissions of
    this License applicable to that copy.

#### 3. Object Code Incorporating Material from Library Header Files.

The object code form of an Application may incorporate material from a header file that is part of the Library. You may convey such object code under terms of your choice, provided that, if the incorporated material is not limited to numerical parameters, data structure layouts and accessors, or small macros, inline functions and templates (ten or fewer lines in length), you do both of the following:

-   a) Give prominent notice with each copy of the object code that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the object code with a copy of the GNU GPL and this
    license document.

#### 4. Combined Works.

You may convey a Combined Work under terms of your choice that, taken together, effectively do not restrict modification of the portions of the Library contained in the Combined Work and reverse engineering for debugging such modifications, if you also do each of the following:

-   a) Give prominent notice with each copy of the Combined Work that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the Combined Work with a copy of the GNU GPL and this
    license document.
-   c) For a Combined Work that displays copyright notices during
    execution, include the copyright notice for the Library among
    these notices, as well as a reference directing the user to the
    copies of the GNU GPL and this license document.
-   d) Do one of the following:
    -   0) Convey the Minimal Corresponding Source under the terms of
        this License, and the Corresponding Application Code in a form
        suitable for, and under terms that permit, the user to
        recombine or relink the Application with a modified version of
        the Linked Version to produce a modified Combined Work, in the
        manner specified by section 6 of the GNU GPL for conveying
        Corresponding Source.
    -   1) Use a suitable shared library mechanism for linking with
        the Library. A suitable mechanism is one that (a) uses at run
        time a copy of the Library already present on the user's
        computer system, and (b) will operate properly with a modified
        version of the Library that is interface-compatible with the
        Linked Version.
-   e) Provide Installation Information, but only if you would
    otherwise be required to provide such information under section 6
    of the GNU GPL, and only to the extent that such information is
    necessary to install and execute a modified version of the
    Combined Work produced by recombining or relinking the Application
    with a modified version of the Linked Version. (If you use option
    4d0, the Installation Information must accompany the Minimal
    Corresponding Source and Corresponding Application Code. If you
    use option 4d1, you must provide the Installation Information in
    the manner specified by section 6 of the GNU GPL for conveying
    Corresponding Source.)

#### 5. Combined Libraries.

You may place library facilities that are a work based on the Library side by side in a single library together with other library facilities that are not Applications and are not covered by this License, and convey such a combined library under terms of your choice, if you do both of the following:

-   a) Accompany the combined library with a copy of the same work
    based on the Library, uncombined with any other library
    facilities, conveyed under the terms of this License.
-   b) Give prominent notice with the combined library that part of it
    is a work based on the Library, and explaining where to find the
    accompanying uncombined form of the same work.

#### 6. Revised Versions of the GNU Lesser General Public License.

The Free Software Foundation may publish revised and/or new versions of the GNU Lesser General Public License from time to time. Such new versions will be similar in spirit to the present version, but may differ in detail to address new problems or concerns.

Each version is given a distinguishing version number. If the Library as you received it specifies that a certain numbered version of the GNU Lesser General Public License "or any later version" applies to it, you have the option of following the terms and conditions either of that published version or of any later version published by the Free Software Foundation. If the Library as you received it does not specify a version number of the GNU Lesser General Public License, you may choose any version of the GNU Lesser General Public License ever published by the Free Software Foundation.

If the Library as you received it specifies that a proxy can decide whether future versions of the GNU Lesser General Public License shall apply, that proxy's public statement of acceptance of any version is permanent authorization for you to choose that version for the Library.


# https://github.com/ramoncerdaquiroz
# Security Policy

To report a security issue, please use [g.co/vulnz](https://g.co/vulnz).

The Google Security Team will respond within 5 working days of your report on g.co/vulnz.

We use g.co/vulnz for our intake, and do coordination and disclosure here using GitHub Security Advisory to privately discuss and fix the issue. closure here using GitHub Security Advisory to privately discuss and fix the issue. /core.excludesfile/npm-debug.log
# https://gitter.im/ethereum/web3.js
# https://badges.gitter.im/Join%20Chat.svg
# https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JavaScript-API # https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge/meteor.js # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC # https://ci.testling.com/ethereum/ethereum.js.png # https://ci.testling.com/ethereum/ethereum.js
## **DOCUMENTATION.md**
## Node.js
## Meteor.js
## _**https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js/Web3.providers**_ # WARNING: 2.X IS NO LONGER BEING MAINTAINED AND WILL BE DEPRECATED FROM NPM ## ( @ramoncerdaquiroz{<http://localhost:8545*>})
# Ethereum JavaScript API
# {[https://github.com/ramoncerdaquiroz/[Join the chat at https://gitter.im/ethereum/web3.js](https://badges.gitter.im/Join%20Chat.svg)]}(https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is the Ethereum compatible [JavaScript API](https://github.com/ramoncerdaquioz/ethereum/wiki/wiki/JavaScript-API) which implements the [Generic JSON RPC](https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC) spec. It's available on npm as a node module, for Bower and component as embeddable scripts, and as a meteor.js package.

[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url] [![dev dependency status][dep-dev-image]][dep-dev-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Stories in Ready][waffle-image]][waffle-url]

<!-- [![browser support](https://ci.testling.com/ethereum/ethereum.js.png)](https://ci.testling.com/ethereum/ethereum.js) -->

You need to run a local Ethereum node to use this library.

[Documentation](DOCUMENTATION.md)

## Table of Contents

- [Installation](#installation)
  - [Node.js](#nodejs)
  - [Yarn](#yarn)
  - [Meteor.js](#meteorjs)
  - [As a Browser module](#as-a-browser-module)
- [Usage](#usage)
  - [Migration from 0.13.0 to 0.14.0](#migration-from-0130-to-0140)
- [Contribute!](#contribute)
  - [Requirements](#requirements)
  - [Building (gulp)](#building-gulp)
  - [Testing (mocha)](#testing-mocha)
  - [Community](#community)
  - [Other implementations](#other-implementations)
- [License](#license)

## Installation

### Node.js

```bash
npm install web3
```

### Yarn

```bash
yarn add web3
```

### Meteor.js

```bash
meteor add ethereum:web3
```

### As a Browser module

CDN

```html
<script src="https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js" integrity="sha256-nWBTbvxhJgjslRyuAKJHK+XcZPlCnmIAAMixz6EefVk=" crossorigin="anonymous"></script>
```

Bower

```bash
bower install web3
```

Component

```bash
component install ethereum/web3.js
```

* Include `web3.min.js` in your html file. (not required for the meteor package)

## Usage

Use the `web3` object directly from the global namespace:

```js
console.log(web3); // {eth: .., shh: ...} // It's here!
```

Set a provider (`HttpProvider`):

```js
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // Set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}
```

Set a provider (`HttpProvider` using [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)):

```js
web3.setProvider(new web3.providers.HttpProvider('http://' + BasicAuthUsername + ':' + BasicAuthPassword + '@localhost:8545'));
```

There you go, now you can use it:

```js
var coinbase = web3.eth.coinbase;
var balance = web3.eth.getBalance(coinbase);
```

You can find more examples in the [`example`](https://github.com/ramoncerdaquiroz/ethereum/web3.js/tree/master/example) directory. # https://gitter.im/ethereum/web3.js?source=orgpage # https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297/Web3.py  # https://github.com/ramoncerdaquiroz/BANKEX/web3swift/LICENSE.md # https://badge.fury.io/js/web3.svg
# https://github.com/ramoncerdaquirooz/https://npmjs.org/package/web3.js # https://github.com/ramoncerdaquiroz/https://travis-ci.org/ethereum/web3.js.svghttps://travis-ci.org/ethereum/web3.js # https://github.com/ramoncerdaquiroz/https://david-dm.org/ethereum/web3.js.svghttps://david-dm.org/ethereum/web3.js/https://david-dm.org/ethereum/web3.js/dev-status.svg/https://david-dm.org/ethereum/web3.js # info=devDependencies/https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master/https://coveralls.io/r/ethereum/web3.js?branch=master/https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Readyhttps://waffle.io/ethereum/web3.js}

### Migration from 0.13.0 to 0.14.0

web3.js version 0.14.0 supports [multiple instances of the web3](https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297) object. To migrate to this version, please follow the guide:

```diff
-var web3 = require('web3');
+var Web3 = require('web3');
+var web3 = new Web3();
```
## Contribute!

### Requirements

* Node.js
* npm

```bash
# On Linux:
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
sudo apt-get install nodejs-legacy
```

### Building (gulp)

```bash
npm run-script build
```


### Testing (mocha)

```bash
npm test
```

### Community
 - [Gitter](https://gitter.im/ethereum/web3.js?source=orgpage)
 - [Forum](https://forum.ethereum.org/categories/ethereum-js)


### Other implementations
 - Python [Web3.py](https://github.com/ramoncerdaquiroz/ethereum/web3.py)
 - Haskell [hs-web3](https://github.com/ramoncerdaquiroz/airalab/hs-web3)
 - Java [web3j](https://github.com/ramoncerdaquiroz/web3j/web3j)
 - Scala [web3j-scala](https://github.com/ramoncerdaquiroz/mslinn/web3j-scala)
 - Purescript [purescript-web3](https://github.com/ramoncerdaquiroz/f-o-a-m/purescript-web3)
 - PHP [web3.php](https://github.com/ramoncerdaquiroz/sc0Vu/web3.php)
 - PHP [ethereum-php](https://github.com/ramoncerdaquiroz/digitaldonkey/ethereum-php)
 - Rust [rust-web3](https://github.com/ramoncerdaquiroz/tomusdrw/rust-web3)
 - Swift [web3swift](https://github.com/ramoncerdaquiroz/BANKEX/web3swift)

## License

[LGPL-3.0+](LICENSE.md) © 2015 Contributors


[npm-image]: https://badge.fury.io/js/web3.svg
[npm-url]: https://npmjs.org/package/web3
[travis-image]: https://travis-ci.org/ethereum/web3.js.svg
[travis-url]: https://travis-ci.org/ethereum/web3.js
[dep-image]: https://david-dm.org/ethereum/web3.js.svg
[dep-url]: https://david-dm.org/ethereum/web3.js
[dep-dev-image]: https://david-dm.org/ethereum/web3.js/dev-status.svg
[dep-dev-url]: https://david-dm.org/ethereum/web3.js#info=devDependencies
[coveralls-image]: https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/r/ethereum/web3.js?branch=master
[waffle-image]: https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Ready
[waffle-url]: https://waffle.io/ethereum/web3.js

# See http://help.github.com/ramoncerdaquirooz/ignore-files/ for more about ignoring files. #
# If you find yourself ignoring temporary files generated by your text editor # or operating system, you probably want to add a global ignore instead:
#   git config --global core.excludesfile ~/.gitignore_global

.idea/
*.swp
/coverage
/tmp
*/**/*un~
*un~
.DS_Store
*/**/.DS_Store
ethereum/ethereum
ethereal/ethereal
example/js
node_modules
bower_components
npm-debug.log
/bower
.npm/
packages/

# name: CI
on:
  pull_request: {}
  push:
    branches: [main]
jobs:
  main:
    name: Build, Validate and Deploy
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
      - uses: w3c/spec-prod@v2 with: GH_PAGES_BRANCH: gh-pages

# This file is part of web3.js.

web3.js is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

web3.js is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

### GNU LESSER GENERAL PUBLIC LICENSE

Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc.
<https://ggmon.org/>
<https://ggmon.com/>
Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

This version of the GNU Lesser General Public License incorporates the terms and conditions of version 3 of the GNU General Public License, supplemented by the additional permissions listed below.

#### 0. Additional Definitions.

As used herein, "this License" refers to version 3 of the GNU Lesser General Public License, and the "GNU GPL" refers to version 3 of the GNU General Public License.

"The Library" refers to a covered work governed by this License, other than an Application or a Combined Work as defined below.

An "Application" is any work that makes use of an interface provided by the Library, but which is not otherwise based on the Library. Defining a subclass of a class defined by the Library is deemed a mode of using an interface provided by the Library.

A "Combined Work" is a work produced by combining or linking an Application with the Library. The particular version of the Library with which the Combined Work was made is also called the "Linked Version".

The "Minimal Corresponding Source" for a Combined Work means the Corresponding Source for the Combined Work, excluding any source code for portions of the Combined Work that, considered in isolation, are based on the Application, and not on the Linked Version.

The "Corresponding Application Code" for a Combined Work means the object code and/or source code for the Application, including any data and utility programs needed for reproducing the Combined Work from the Application, but excluding the System Libraries of the Combined Work.

#### 1. Exception to Section 3 of the GNU GPL.

You may convey a covered work under sections 3 and 4 of this License without being bound by section 3 of the GNU GPL.

#### 2. Conveying Modified Versions.

If you modify a copy of the Library, and, in your modifications, a facility refers to a function or data to be supplied by an Application that uses the facility (other than as an argument passed when the facility is invoked), then you may convey a copy of the modified version:

-   a) under this License, provided that you make a good faith effort
    to ensure that, in the event an Application does not supply the
    function or data, the facility still operates, and performs
    whatever part of its purpose remains meaningful, or
-   b) under the GNU GPL, with none of the additional permissions of
    this License applicable to that copy.

#### 3. Object Code Incorporating Material from Library Header Files.

The object code form of an Application may incorporate material from a header file that is part of the Library. You may convey such object code under terms of your choice, provided that, if the incorporated material is not limited to numerical parameters, data structure layouts and accessors, or small macros, inline functions and templates (ten or fewer lines in length), you do both of the following:

-   a) Give prominent notice with each copy of the object code that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the object code with a copy of the GNU GPL and this
    license document.

#### 4. Combined Works.

You may convey a Combined Work under terms of your choice that, taken together, effectively do not restrict modification of the portions of the Library contained in the Combined Work and reverse engineering for debugging such modifications, if you also do each of the following:

-   a) Give prominent notice with each copy of the Combined Work that
    the Library is used in it and that the Library and its use are
    covered by this License.
-   b) Accompany the Combined Work with a copy of the GNU GPL and this
    license document.
-   c) For a Combined Work that displays copyright notices during
    execution, include the copyright notice for the Library among
    these notices, as well as a reference directing the user to the
    copies of the GNU GPL and this license document.
-   d) Do one of the following:
    -   0) Convey the Minimal Corresponding Source under the terms of
        this License, and the Corresponding Application Code in a form
        suitable for, and under terms that permit, the user to
        recombine or relink the Application with a modified version of
        the Linked Version to produce a modified Combined Work, in the
        manner specified by section 6 of the GNU GPL for conveying
        Corresponding Source.
    -   1) Use a suitable shared library mechanism for linking with
        the Library. A suitable mechanism is one that (a) uses at run
        time a copy of the Library already present on the user's
        computer system, and (b) will operate properly with a modified
        version of the Library that is interface-compatible with the
        Linked Version.
-   e) Provide Installation Information, but only if you would
    otherwise be required to provide such information under section 6
    of the GNU GPL, and only to the extent that such information is
    necessary to install and execute a modified version of the
    Combined Work produced by recombining or relinking the Application
    with a modified version of the Linked Version. (If you use option
    4d0, the Installation Information must accompany the Minimal
    Corresponding Source and Corresponding Application Code. If you
    use option 4d1, you must provide the Installation Information in
    the manner specified by section 6 of the GNU GPL for conveying
    Corresponding Source.)

#### 5. Combined Libraries.

You may place library facilities that are a work based on the Library side by side in a single library together with other library facilities that are not Applications and are not covered by this License, and convey such a combined library under terms of your choice, if you do both of the following:

-   a) Accompany the combined library with a copy of the same work
    based on the Library, uncombined with any other library
    facilities, conveyed under the terms of this License.
-   b) Give prominent notice with the combined library that part of it
    is a work based on the Library, and explaining where to find the
    accompanying uncombined form of the same work.

#### 6. Revised Versions of the GNU Lesser General Public License.

The Free Software Foundation may publish revised and/or new versions of the GNU Lesser General Public License from time to time. Such new versions will be similar in spirit to the present version, but may differ in detail to address new problems or concerns.

Each version is given a distinguishing version number. If the Library as you received it specifies that a certain numbered version of the GNU Lesser General Public License "or any later version" applies to it, you have the option of following the terms and conditions either of that published version or of any later version published by the Free Software Foundation. If the Library as you received it does not specify a version number of the GNU Lesser General Public License, you may choose any version of the GNU Lesser General Public License ever published by the Free Software Foundation.

If the Library as you received it specifies that a proxy can decide whether future versions of the GNU Lesser General Public License shall apply, that proxy's public statement of acceptance of any version is permanent authorization for you to choose that version for the Library.


# https://github.com/ramoncerdaquiroz
# Security Policy

To report a security issue, please use [g.co/vulnz](https://g.co/vulnz).

The Google Security Team will respond within 5 working days of your report on g.co/vulnz.

We use g.co/vulnz for our intake, and do coordination and dis# SEGURIDAD o SECURITY # {http://help.github.com/ramoncerdaquiroz/ignore-files/core.excludesfile/npm-debug.log # https://gitter.im/ethereum/web3.js
# https://badges.gitter.im/Join%20Chat.svg
# https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JavaScript-API # https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge/meteor.js # https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC # https://ci.testling.com/ethereum/ethereum.js.png # https://ci.testling.com/ethereum/ethereum.js
## **DOCUMENTATION.md**
## Node.js
## Meteor.js
## _**https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js/Web3.providers**_ # WARNING: 2.X IS NO LONGER BEING MAINTAINED AND WILL BE DEPRECATED FROM NPM ## ( @ramoncerdaquiroz{<http://localhost:8545*>})
# Ethereum JavaScript API
# {[https://github.com/ramoncerdaquiroz/[Join the chat at https://gitter.im/ethereum/web3.js](https://badges.gitter.im/Join%20Chat.svg)]}(https://gitter.im/ethereum/web3.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is the Ethereum compatible [JavaScript API](https://github.com/ramoncerdaquioz/ethereum/wiki/wiki/JavaScript-API) which implements the [Generic JSON RPC](https://github.com/ramoncerdaquiroz/ethereum/wiki/wiki/JSON-RPC) spec. It's available on npm as a node module, for Bower and component as embeddable scripts, and as a meteor.js package.

[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url] [![dev dependency status][dep-dev-image]][dep-dev-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Stories in Ready][waffle-image]][waffle-url]

<!-- [![browser support](https://ci.testling.com/ethereum/ethereum.js.png)](https://ci.testling.com/ethereum/ethereum.js) -->

You need to run a local Ethereum node to use this library.

[Documentation](DOCUMENTATION.md)

## Table of Contents

- [Installation](#installation)
  - [Node.js](#nodejs)
  - [Yarn](#yarn)
  - [Meteor.js](#meteorjs)
  - [As a Browser module](#as-a-browser-module)
- [Usage](#usage)
  - [Migration from 0.13.0 to 0.14.0](#migration-from-0130-to-0140)
- [Contribute!](#contribute)
  - [Requirements](#requirements)
  - [Building (gulp)](#building-gulp)
  - [Testing (mocha)](#testing-mocha)
  - [Community](#community)
  - [Other implementations](#other-implementations)
- [License](#license)

## Installation

### Node.js

```bash
npm install web3
```

### Yarn

```bash
yarn add web3
```

### Meteor.js

```bash
meteor add ethereum:web3
```

### As a Browser module

CDN

```html
<script src="https://cdn.jsdelivr.net/gh/ethereum/web3.js@1.0.0-beta.36/dist/web3.min.js" integrity="sha256-nWBTbvxhJgjslRyuAKJHK+XcZPlCnmIAAMixz6EefVk=" crossorigin="anonymous"></script>
```

Bower

```bash
bower install web3
```

Component

```bash
component install ethereum/web3.js
```

* Include `web3.min.js` in your html file. (not required for the meteor package)

## Usage

Use the `web3` object directly from the global namespace:

```js
console.log(web3); // {eth: .., shh: ...} // It's here!
```

Set a provider (`HttpProvider`):

```js
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // Set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}
```

Set a provider (`HttpProvider` using [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)):

```js
web3.setProvider(new web3.providers.HttpProvider('http://' + BasicAuthUsername + ':' + BasicAuthPassword + '@localhost:8545'));
```

There you go, now you can use it:

```js
var coinbase = web3.eth.coinbase;
var balance = web3.eth.getBalance(coinbase);
```

You can find more examples in the [`example`](https://github.com/ramoncerdaquiroz/ethereum/web3.js/tree/master/example) directory. # https://gitter.im/ethereum/web3.js?source=orgpage # https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297/Web3.py  # https://github.com/ramoncerdaquiroz/BANKEX/web3swift/LICENSE.md # https://badge.fury.io/js/web3.svg
# https://github.com/ramoncerdaquirooz/https://npmjs.org/package/web3.js # https://github.com/ramoncerdaquiroz/https://travis-ci.org/ethereum/web3.js.svghttps://travis-ci.org/ethereum/web3.js # https://github.com/ramoncerdaquiroz/https://david-dm.org/ethereum/web3.js.svghttps://david-dm.org/ethereum/web3.js/https://david-dm.org/ethereum/web3.js/dev-status.svg/https://david-dm.org/ethereum/web3.js # info=devDependencies/https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master/https://coveralls.io/r/ethereum/web3.js?branch=master/https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Readyhttps://waffle.io/ethereum/web3.js}

### Migration from 0.13.0 to 0.14.0

web3.js version 0.14.0 supports [multiple instances of the web3](https://github.com/ramoncerdaquiroz/ethereum/web3.js/issues/297) object. To migrate to this version, please follow the guide:

```diff
-var web3 = require('web3');
+var Web3 = require('web3');
+var web3 = new Web3();
```
## Contribute!

### Requirements

* Node.js
* npm

```bash
# On Linux:
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
sudo apt-get install nodejs-legacy
```

### Building (gulp)

```bash
npm run-script build
```


### Testing (mocha)

```bash
npm test
```

### Community
 - [Gitter](https://gitter.im/ethereum/web3.js?source=orgpage)
 - [Forum](https://forum.ethereum.org/categories/ethereum-js)


### Other implementations
 - Python [Web3.py](https://github.com/ramoncerdaquiroz/ethereum/web3.py)
 - Haskell [hs-web3](https://github.com/ramoncerdaquiroz/airalab/hs-web3)
 - Java [web3j](https://github.com/ramoncerdaquiroz/web3j/web3j)
 - Scala [web3j-scala](https://github.com/ramoncerdaquiroz/mslinn/web3j-scala)
 - Purescript [purescript-web3](https://github.com/ramoncerdaquiroz/f-o-a-m/purescript-web3)
 - PHP [web3.php](https://github.com/ramoncerdaquiroz/sc0Vu/web3.php)
 - PHP [ethereum-php](https://github.com/ramoncerdaquiroz/digitaldonkey/ethereum-php)
 - Rust [rust-web3](https://github.com/ramoncerdaquiroz/tomusdrw/rust-web3)
 - Swift [web3swift](https://github.com/ramoncerdaquiroz/BANKEX/web3swift)

## License

[LGPL-3.0+](LICENSE.md) © 2015 Contributors


[npm-image]: https://badge.fury.io/js/web3.svg
[npm-url]: https://npmjs.org/package/web3
[travis-image]: https://travis-ci.org/ethereum/web3.js.svg
[travis-url]: https://travis-ci.org/ethereum/web3.js
[dep-image]: https://david-dm.org/ethereum/web3.js.svg
[dep-url]: https://david-dm.org/ethereum/web3.js
[dep-dev-image]: https://david-dm.org/ethereum/web3.js/dev-status.svg
[dep-dev-url]: https://david-dm.org/ethereum/web3.js#info=devDependencies
[coveralls-image]: https://coveralls.io/repos/ethereum/web3.js/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/r/ethereum/web3.js?branch=master
[waffle-image]: https://badge.waffle.io/ethereum/web3.js.svg?label=ready&title=Ready
[waffle-url]: https://waffle.io/ethereum/web3.js

# See http://help.github.com/ramoncerdaquirooz/ignore-files/ for more about ignoring files. #
# If you find yourself ignoring temporary files generated by your text editor # or operating system, you probably want to add a global ignore instead:
#   git config --global core.excludesfile ~/.gitignore_global

.idea/
*.swp
/coverage
/tmp
*/**/*un~
*un~
.DS_Store
*/**/.DS_Store
ethereum/ethereum
ethereal/ethereal
example/js
node_modules
bower_components
npm-debug.log
/bower
.npm/
packages/

# name: CI
on:
  pull_request: {}
  push:
    branches: [main]
jobs:
  main:
    name: Build, Validate and Deploy
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
      - uses: w3c/spec-prod@v2 with: GH_PAGES_BRANCH: gh-pages

# This file is part of web3.js.

web3.js is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

web3.js is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

### GNU LESSER GENERAL PUBLIC LICENSE

Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc.
<https://ggmon.org/>
<https://ggmon.com/>
Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

This version of the GNU Lesser General Public License incorporates the terms and conditions of version 3 of the GNU General Public License, supplemented by the addit…![white cube-white text_svg](https://github.com/npm/documentation/assets/42362168/e4711bcf-72e4-48d6-8623-1bc2d05a3160)
![white cube-gray text_svg](https://github.com/npm/documentation/assets/42362168/92d1a922-c743-4d33-b051-59e05d60bf8f)
![unnamed](https://github.com/npm/documentation/assets/42362168/2e9122fb-c212-4e12-8524-7040f25e632e)
![table…
![fa1f132c68cf15ed32cfdb1258920b6efc5d2d28](https://github.com/eslint/.github/assets/42362168/a58c211a-fbf1-42b6-ba31-3d16f20bedd7)
![f3f7a64438631e15faa8b81b053c9e3af62c7bbf](https://github.com/eslint/.github/assets/42362168/98d73824-9f7c-4ee6-b1c5-be8baaa168f8)
![eeaf9cf6eda8bca9ffc25f73640baf1ca37b7558](https://github.com/eslint/.github/assets/42362168/a43596a9-f25c-4b45-b7cc-54d606e7dfeb)
![b69eb70c51ffc76777d77621ad22c680f61ddb22](https://github.com/eslint/.github/assets/42362168/c309786b-cada-40fa-8ca9-cb9faaf1dbc7)
![abfaa85e66f7c551a82fb80d550c4fb15be50f52](https://github.com/eslint/.github/assets/42362168/2f267b7e-6adc-418f-8f1d-f7cab6ac250c)
![59749392a78e7639c611bd59a6a232bbbd0a6171](https://github.com/eslint/.github/assets/42362168/cc69e0e1-916a-4daf-a962-5c878128b901)
![0114c41116f71939716f1e26ecda043a8ceb172a](https://github.com/eslint/.github/assets/42362168/f704ae14-cca5-4f95-9f73-8944045176c4)
![98e65fc9c6e83fea01aca8d8eedec35d54a784bb](https://github.com/eslint/.github/assets/42362168/3e8cbb12-d953-4732-87a1-337b8a6af7ef)
![3f7f638617eeae53e6a44acdd38c7fa3541243cc](https://github.com/eslint/.github/assets/42362168/dd0dbd7c-2d22-4752-87e8-234099cd5fe3)
![windows5](https://github.com/eslint/.github/assets/42362168/4fd16cee-f95a-4051-93c5-915de541a66b)
