# forge clone

Clone a contract from Etherscan

```bash
$ forge clone --help
```

```txt
Usage: forge clone [OPTIONS] <ADDRESS> [PATH]

Arguments:
  <ADDRESS>
          The contract address to clone

  [PATH]
          The root directory of the cloned project
          
          [default: .]

Options:
      --no-remappings-txt
          Do not generate the remappings.txt file. Instead, keep the remappings
          in the configuration

      --keep-directory-structure
          Keep the original directory structure collected from Etherscan.
          
          If this flag is set, the directory structure of the cloned project
          will be kept as is. By default, the directory structure is re-orgnized
          to increase the readability, but may risk some compilation failures.

  -e, --etherscan-api-key <KEY>
          The Etherscan (or equivalent) API key
          
          [env: ETHERSCAN_API_KEY=]

  -c, --chain <CHAIN>
          The chain name or EIP-155 chain ID
          
          [env: CHAIN=]

      --shallow
          Perform shallow clones instead of deep ones.
          
          Improves performance and reduces disk usage, but prevents switching
          branches or tags.

      --no-git
          Install without adding the dependency as a submodule

      --no-commit
          Do not create a commit

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
```