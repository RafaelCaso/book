# cast run

Runs a published transaction in a local environment and prints the trace

```bash
$ cast run --help
```

```txt
Usage: cast run [OPTIONS] <TX_HASH>

Arguments:
  <TX_HASH>
          The transaction hash

Options:
  -d, --debug
          Opens the transaction in the debugger

      --decode-internal
          Whether to identify internal functions in traces

  -t, --trace-printer
          Print out opcode traces

      --quick
          Executes the transaction only with the state from the previous block.
          
          May result in different results than the live execution!

  -v, --verbose
          Prints the full address of the contract

  -l, --label <LABEL>
          Label addresses in the trace.
          
          Example: 0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045:vitalik.eth

  -r, --rpc-url <URL>
          The RPC endpoint
          
          [env: ETH_RPC_URL=]

      --flashbots
          Use the Flashbots RPC URL with fast mode
          (<https://rpc.flashbots.net/fast>).
          
          This shares the transaction privately with all registered builders.
          
          See:
          <https://docs.flashbots.net/flashbots-protect/quick-start#faster-transactions>

      --jwt-secret <JWT_SECRET>
          JWT Secret for the RPC endpoint.
          
          The JWT secret will be used to create a JWT for a RPC. For example,
          the following can be used to simulate a CL `engine_forkchoiceUpdated`
          call:
          
          cast rpc --jwt-secret <JWT_SECRET> engine_forkchoiceUpdatedV2
          '["0x6bb38c26db65749ab6e472080a3d20a2f35776494e72016d1e339593f21c59bc",
          "0x6bb38c26db65749ab6e472080a3d20a2f35776494e72016d1e339593f21c59bc",
          "0x6bb38c26db65749ab6e472080a3d20a2f35776494e72016d1e339593f21c59bc"]'
          
          [env: ETH_RPC_JWT_SECRET=]

      --rpc-timeout <RPC_TIMEOUT>
          Timeout for the RPC request in seconds.
          
          The specified timeout will be used to override the default timeout for
          RPC requests.
          
          Default value: 45
          
          [env: ETH_RPC_TIMEOUT=]

  -e, --evm-version <EVM_VERSION>
          The EVM version to use.
          
          Overrides the version specified in the config.

      --compute-units-per-second <CUPS>
          Sets the number of assumed available compute units per second for this
          provider
          
          default value: 330
          
          See also,
          https://docs.alchemy.com/reference/compute-units#what-are-cups-compute-units-per-second

      --no-rate-limit
          Disables rate limiting for this node's provider.
          
          default value: false
          
          See also,
          https://docs.alchemy.com/reference/compute-units#what-are-cups-compute-units-per-second
          
          [aliases: no-rpc-rate-limit]

      --alphanet
          Enables Alphanet features

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
```