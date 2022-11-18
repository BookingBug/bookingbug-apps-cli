# jrni-cli

## Installation

Requires node 14. See [Downloading and installing Nodejs and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

```npm install -g @jrni/jrni-cli```

If you see permission errors when trying to install see [Resolving EACCES permissions errors when installing packages globally](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)

Note: If you run into errors stating "Cannot find module 'vue-template-compiler'" then run the following commands to install:

```text
git clone git@github.com:jrni-platform/jrni-cli.git
cd jrni-cli
npm uninstall -g @jrni/jrni-cli
npm install
npm install -g . --no-optional
```

## Options

Options may be passed with flags, however you will be prompted to enter any missing required
options.

The options will be stored in the project directory in ```.bbugrc```. This avoids the need to
re-enter options upon re-triggering commands for a given app project.

## Versions of the cli vs server versions

In version version5.17 of the JRNI engine, a new parameter was added to the api upon install of an extensibility application. It optionally allows you to keep the configuration of the application. This feature was added to v5.17+ of the JRNI BE engine and v0.1.2 of the cli.

In short if the version of the engine is below 5.17 use v0.1.0 of the cli. If above 5.17 use v0.1.2+.

## Commands

### Install

Builds and installs an app package to the BookingBug engine. Run the command in the Jext app project
directory.

```jrni-cli install [options]```

Options:

<table>
  <tr>
    <td>--email</td><td>Email address used to log into JRNI</td>
  </tr>
  <tr>
    <td>--password</td><td>Password used to log into JRNI</td>
  </tr>
  <tr>
    <td>--host</td><td>Destination host server</td>
  </tr>
  <tr>
    <td>--companyId</td><td>Destination company</td>
  </tr>
  <tr>
    <td>--port</td><td>HTTP port to use</td>
</table>

### Uninstall

Removes an app package from the BookingBug engine.

```jrni-cli uninstall [options]```

Options:

<table>
  <tr>
    <td>--email</td><td>Email address used to log into JRNI</td>
  </tr>
  <tr>
    <td>--password</td><td>Password used to log into JRNI</td>
  </tr>
  <tr>
    <td>--host</td><td>Destination host server</td>
  </tr>
  <tr>
    <td>--companyId</td><td>Destination company</td>
  </tr>
  <tr>
    <td>--port</td><td>HTTP port to use</td>
</table>

### Tail

Display the script logs for an app package.

```jrni-cli tail [options]```

Options:

<table>
  <tr>
    <td>--email</td><td>Email address used to log into JRNI</td>
  </tr>
  <tr>
    <td>--password</td><td>Password used to log into JRNI</td>
  </tr>
  <tr>
    <td>--host</td><td>Destination host server</td>
  </tr>
  <tr>
    <td>--companyId</td><td>Destination company</td>
  </tr>
  <tr>
    <td>--port</td><td>HTTP port to use</td>
</table>

### Release

Release a new version of the application to the central app repo. This feature is only available if you have an account as a central app deployer to install apps into the central app listing repo

```jrni-cli release```

This relies on setting two env variables which is your central app repo account login (not the login to a specific client box):

APP_INSTALL_EMAIL: App install email address
APP_INSTALL_PASSWORD: App install password
