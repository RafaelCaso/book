# forge soldeer push

Push a Dependency to the Repository

```bash
$ forge soldeer push --help
```

```txt
Usage: forge soldeer push [OPTIONS] <DEPENDENCY>~<VERSION> [PATH]

Arguments:
  <DEPENDENCY>~<VERSION>
          The dependency name and version, separated by a tilde.
          
          This should always be used when you want to push a dependency to the
          central repository: `<https://soldeer.xyz>`.

  [PATH]
          Use this if the package you want to push is not in the current
          directory.
          
          Example: `soldeer push mypkg~0.1.0 /path/to/dep`.

Options:
  -d, --dry-run
          If set, does not publish the package but generates a zip file that can
          be inspected

      --skip-warnings
          Use this if you want to skip the warnings that can be triggered when
          trying to push dotfiles like .env

  -h, --help
          Print help (see a summary with '-h')

Display options:
      --color <COLOR>
          Log messages coloring

          Possible values:
          - auto:   Intelligently guess whether to use color output (default)
          - always: Force color output
          - never:  Force disable color output

  -q, --quiet
          Do not print log messages

      --verbose
          Use verbose output

For more information, read the README.md
```