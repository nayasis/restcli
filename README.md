
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-7-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
<h1 align="center">
  <br>
  <a href="https://github.com/restcli/restcli"><img src="images/logo.png" alt="restcli" width="200"></a>
  <br>
  restcli
  <br>
</h1>

<h4 align="center">A missing commandline application for execute <a href="https://www.jetbrains.com/help/idea/http-client-in-product-code-editor.html" target="_blank">IntelliJ HTTP Client file</a>.</h4>

<p align="center">
  <a href="https://github.com/restcli/restcli/releases/">
    <img src="https://img.shields.io/badge/restcli-latest-brightgreen"
         alt="restcli">
  </a>
  <a href="https://github.com/restcli/restcli/blob/master/LICENSE">
      <img src="https://img.shields.io/badge/license-MIT-blue"
           alt="restcli">
    </a>    
  <a href="https://paypal.me/quangson8128">
    <img src="https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&amp;style=flat">
  </a>
</p>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a> •
  <a href="https://www.producthunt.com/posts/intellij-rest-cli">Producthunt</a>
</p>

![screenshot](images/restcli_screenshots.png)

## Key Features
* Written in Kotlin 🤩
* Execute Intellij HTTP request files
* Running test script including:
    - Embedded script inside HTTP request file
    - Include external javascript test file
* Loading and inject environment variables from
    - http-client.env.json
    - http-client.private.env.json
* Cross-platform 💻🖥️
  - Windows, macOS, and Linux ready.
* Beautiful request log 🤑🤑🤑
  - Request & response detail
  - Test result table  
* Easy to custom via command-line arguments 😎
  - Custom logging request
  - Inject environment name
* Generate test report - JUnit format.  🥰🥰🥰
* Support setNextRequest. So you can custom flexible the test flow. ✨✨✨

##### Demo
![demo-rest-cli](images/demo-rest-cli.gif)

**1. Show detail request/response including test result**

<img alt="request-with-test-success" src="images/request-with-test-success.png" width="480">
<img alt="request-with-test-failed" src="images/request-with-test-failed.png" width="480">

**2. Test result table**

<img alt="test-result-table" src="images/test-result-table.png" width="480">

**3. Generate JUnit test report (XML) that can be viewed by other tools such as xunit-viewer**

<img alt="generate-junit-test-report" src="images/generate-junit-test-report.png" width="480">

## How To Use

The fastest way to get rest cli is to download the jar from [releases tab](https://github.com/restcli/restcli/releases)

```
Usage: rest-cli [-hkV] [-d=<environmentFilesDirectory>] [-e=<environmentName>]
                [-l=<logLevel>] [-G=<String=String>]... [-P=<String=String>]...
                FILES...
IntelliJ RestCli
      FILES...     Path to one or more http script files.
  -d, --env-dir=<environmentFilesDirectory>
                   Directory where config files are (default: current directory)
                   (http-client.env.json/http-client.private.env.json).
  -e, --env=<environmentName>
                   Name of the environment in config file
                   (http-client.env.json/http-client.private.env.json).
  -G, --global-env=<String=String>
                   Public environment variables
  -h, --help       Show this help message and exit.
  -k, --insecure   Disable SSL validation
  -l, --log-level=<logLevel>
                   Config log level while the executor running.
                   Valid values: NONE, BASIC, HEADERS, BODY
  -P, --private-env=<String=String>
                   Private environment variables
  -V, --version    Print version information and exit.
```

#### Example
```bash
# Move to the folder that contains your http files.
$ cd requests

$ tree
├── get-requests.http
├── http-client.env.json
├── http-client.private.env.json
├── post-requests.http
├── request-form-data.json
├── requests-with-authorization.http
├── requests-with-tests.http
└── test_script.js

$ java -jar /path/to/restcli.jar -e "test" get-requests.http
```

Note: This application required you to install `java` on your machine.

## Download

You can [download](https://github.com/restcli/restcli/releases) the latest version of restcli for Windows, macOS, and Linux.

## Credits

This software uses the following open-source packages:

- [Jflex](https://jflex.de/) -  a lexical analyzer generator (also known as scanner generator) for Java.
- [PicoCli](https://picocli.info/) - a mighty tiny command line interface
- [okhttp](https://github.com/square/okhttp) - the way modern applications network. It’s how we exchange data & media. Doing HTTP efficiently makes your stuff load faster and saves bandwidth.
- [picnic](https://github.com/JakeWharton/picnic) - A Kotlin DSL and Java/Kotlin builder API for constructing HTML-like tables that can be rendered to text.
- [mordant](https://github.com/ajalt/mordant) - Full-featured text styling for Kotlin command-line applications.

## Support

If you need help, please don't hesitate to [file an issue](https://github.com/restcli/restcli/issues/new).
 

## Sponsoring

This application is free and can be used for free, open-source, and commercial applications. `restcli` is under the MIT License (MIT). So hit the magic ⭐ button; I appreciate it!!! 🙏

## 🤝 Contributing
I appreciate your support and feedback!

Please file issues if you find bugs and have feature requests. If you can send small PRs to improve or fix bugs, that would be awesome too.

For larger PRs, please ping [@quangson91](https://twitter.com/quangson91) to discuss first.

## 📝 License

MIT License
```
Copyright (c) 2020 Duong Quang Son

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the software, and to permit persons to whom the software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
---

<h2 class="text-white mb-4">Made with <span class="heart">❤</span> by quangson91</h2>

> [restcli.github.io](https://restcli.github.io/) &nbsp;&middot;&nbsp;
> GitHub [@quangson91](https://github.com/quangson91) &nbsp;&middot;&nbsp;
> Twitter [@quangson91](https://twitter.com/quangson91)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/martinqvistgard"><img src="https://avatars2.githubusercontent.com/u/703595?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Martin Qvistgård</b></sub></a><br /><a href="#userTesting-martinqvistgard" title="User Testing">📓</a></td>
    <td align="center"><a href="https://medium.com/@willitheowl"><img src="https://avatars2.githubusercontent.com/u/1067460?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Robert Jack Will</b></sub></a><br /><a href="#ideas-matey-jack" title="Ideas, Planning, & Feedback">🤔</a></td>
    <td align="center"><a href="https://github.com/gsobczyk"><img src="https://avatars2.githubusercontent.com/u/1021528?v=4?s=100" width="100px;" alt=""/><br /><sub><b>gsobczyk</b></sub></a><br /><a href="https://github.com/restcli/restcli/commits?author=gsobczyk" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/pil0t"><img src="https://avatars3.githubusercontent.com/u/820134?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Vlad</b></sub></a><br /><a href="#userTesting-pil0t" title="User Testing">📓</a></td>
    <td align="center"><a href="https://github.com/npeters"><img src="https://avatars2.githubusercontent.com/u/935249?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Nicolas Peters</b></sub></a><br /><a href="https://github.com/restcli/restcli/commits?author=npeters" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/xargon180"><img src="https://avatars2.githubusercontent.com/u/36171927?v=4?s=100" width="100px;" alt=""/><br /><sub><b>xargon180</b></sub></a><br /><a href="https://github.com/restcli/restcli/commits?author=xargon180" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/cylonid"><img src="https://avatars.githubusercontent.com/u/12037864?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Hannes U.</b></sub></a><br /><a href="https://github.com/restcli/restcli/commits?author=cylonid" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
