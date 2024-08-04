# Internxt CLI commands and usage

## **Usage**

`$ npm install -g @internxt/cli $ internxt COMMAND running command... $ internxt (--version) @internxt/cli/1.1.2 darwin-arm64 node-v20.10.0 $ internxt --help [COMMAND] USAGE $ internxt COMMAND ...`

### **Commands**

* [`internxt config`](https://www.npmjs.com/package/@internxt/cli#internxt-config)
* [`internxt create-folder`](https://www.npmjs.com/package/@internxt/cli#internxt-create-folder)
* [`internxt download`](https://www.npmjs.com/package/@internxt/cli#internxt-download)
* [`internxt list`](https://www.npmjs.com/package/@internxt/cli#internxt-list)
* [`internxt login`](https://www.npmjs.com/package/@internxt/cli#internxt-login)
* [`internxt logout`](https://www.npmjs.com/package/@internxt/cli#internxt-logout)
* [`internxt logs`](https://www.npmjs.com/package/@internxt/cli#internxt-logs)
* [`internxt move`](https://www.npmjs.com/package/@internxt/cli#internxt-move)
* [`internxt trash`](https://www.npmjs.com/package/@internxt/cli#internxt-trash)
* [`internxt upload`](https://www.npmjs.com/package/@internxt/cli#internxt-upload)
* [`internxt webdav ACTION`](https://www.npmjs.com/package/@internxt/cli#internxt-webdav-action)
* [`internxt whoami`](https://www.npmjs.com/package/@internxt/cli#internxt-whoami)

**`internxt config`**Display useful information from the user logged into the Internxt CLI.

```
USAGE
  $ internxt config [--columns <value> | -x] [--filter <value>] [--no-header | [--csv | --no-truncate]]
    [--output csv|json|yaml |  | ] [--sort <value>]

FLAGS
  -x, --extended         show extra columns
      --columns=<value>  only show provided columns (comma-separated)
      --csv              output is csv format [alias: --output=csv]
      --filter=<value>   filter property by partial string matching, ex: name=foo
      --no-header        hide table header from output
      --no-truncate      do not truncate output to fit screen
      --output=<option>  output in a more machine friendly format
                         <options: csv|json|yaml>
      --sort=<value>     property to sort by (prepend '-' for descending)

DESCRIPTION
  Display useful information from the user logged into the Internxt CLI.

EXAMPLES
  $ internxt config
```

_See code:_ [_**src/commands/config.ts**_](https://github.com/internxt/cli/blob/v1.1.2/src/commands/config.ts)**`internxt create-folder`**Create a folder in your Internxt Drive

```
USAGE
  $ internxt create-folder --name <value> [--id <value>]

FLAGS
  --id=<value>    The folder id to create the folder in, defaults to your root folder
  --name=<value>  (required) The new folder name

DESCRIPTION
  Create a folder in your Internxt Drive

EXAMPLES
  $ internxt create-folder
```

_See code:_ [_**src/commands/create-folder.ts**_](https://github.com/internxt/cli/blob/v1.1.2/src/commands/create-folder.ts)**`internxt download`**Download and decrypts a file from Internxt Drive to a directory. The file name will be the same as the file name in your Drive

```
USAGE
  $ internxt download --id <value> --directory <value> [--overwrite]

FLAGS
  --directory=<value>  (required) The directory to download the file to.
  --id=<value>         (required) The id of the file to download. Use internxt list to view your files ids
  --overwrite          Overwrite the file if it already exists

DESCRIPTION
  Download and decrypts a file from Internxt Drive to a directory. The file name will be the same as the file name in
  your Drive

EXAMPLES
  $ internxt download
```

_See code:_ [_**src/commands/download.ts**_](https://github.com/internxt/cli/blob/v1.1.2/src/commands/download.ts)**`internxt list`**Lists the content of a folder id.

```
USAGE
  $ internxt list [-n] [-f <value>] [--columns <value> | -x] [--filter <value>] [--no-header | [--csv |
    --no-truncate]] [--output csv|json|yaml |  | ] [--sort <value>]

FLAGS
  -f, --id=<value>       The folder id to list. Leave empty for the root folder.
  -x, --extended         show extra columns
      --columns=<value>  only show provided columns (comma-separated)
      --csv              output is csv format [alias: --output=csv]
      --filter=<value>   filter property by partial string matching, ex: name=foo
      --no-header        hide table header from output
      --no-truncate      do not truncate output to fit screen
      --output=<option>  output in a more machine friendly format
                         <options: csv|json|yaml>
      --sort=<value>     property to sort by (prepend '-' for descending)

HELPER FLAGS
  -n, --non-interactive  Blocks the cli from being interactive. If passed, the cli will not request data through the
                         console and will throw errors directly

DESCRIPTION
  Lists the content of a folder id.

EXAMPLES
  $ internxt list
```

_See code:_ [_**src/commands/list.ts**_](https://github.com/internxt/cli/blob/v1.1.2/src/commands/list.ts)**`internxt login`**Logs into an Internxt account. If the account is two-factor protected, then an extra code will be required.
