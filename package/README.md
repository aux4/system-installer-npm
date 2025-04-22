# system-installer-npm

The [aux4 system installer](/r/public/packages/aux4/pkger/commands/aux4/pkger/system) is used to manage packages by another package system. It is used to install and uninstall system packages.

```json
{
  "scope": "<scope>",
  "name": "<name>",
  "version": "<version>",
  ...
  "system": [
    ["npm:semver"]
  ],
  "profiles": [
    ...
  ]
}
```

In this case when the *aux4 package is installed*, it will install the `semver` package using the `npm` package manager.

```bash
> npm install --global semver
```

In the same way, when the *aux4 package is uninstalled*, it will uninstall `semver` package using the `npm` package manager (only if they are not used by another aux4 package).

```bash
> npm uninstall --global semver
```

Check out the [aux4 pkger system npm](commands/aux4/pkger/system/npm) command for more information.

