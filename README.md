# kc-dc: keychain with docker compose

## Prerequisites

* [Docker](https://www.docker.com/get-started/) installed

```
$ docker compose version
Docker Compose version v2.20.2
```

## Limitations

* file parameters must be in the data folder, e.g. `./kc create-credential data/schema/email.json`

## Getting Started

```
$ git clone https://github.com/KeychainMDIP/kc-dc
$ cd kc-dc
$ cp sample.env .env
$ edit .env (to set node ID, node name, wallet passphrase)
$ ./start-node

In a separate terminal:

$ ./kc
Usage: keychain-cli [options] [command]

Keychain CLI tool

Options:
  -V, --version                              output the version number
  -h, --help                                 display help for command

Commands:
  accept-credential <did> [name]             Save verifiable credential for current ID
  add-group-member <group> <member>          Add a member to a group
  add-name <name> <did>                      Adds a name for a DID
  backup-id                                  Backup the current ID to its registry
  backup-wallet-did                          Backup wallet to encrypted DID and seed bank
  backup-wallet-file <file>                  Backup wallet to file
  bind-credential <schema> <subject>         Create bound credential for a user
  check-wallet                               Validate DIDs in wallet
  create-asset [file]                        Create an asset from a JSON file
  create-challenge [file] [name]             Create challenge (optionally from a file)
  create-challenge-cc <did> [name]           Create challenge from a credential DID
  create-group <name>                        Create a new group
  create-id <name> [registry]                Create a new decentralized ID
  create-poll <file> [name]                  Create poll
  create-poll-template                       Generate a poll template
  create-response <challenge>                Create a response to a challenge
  create-schema <file> [name]                Create schema DID from schema file
  create-schema <file> [name]                Create schema from a file
  create-schema-template <schema>            Create a template from a schema
  create-wallet                              Create new wallet (or show existing wallet)
  decrypt-did <did>                          Decrypt an encrypted message DID
  decrypt-json <did>                         Decrypt an encrypted JSON DID
  encrypt-file <file> <did>                  Encrypt a file for a DID
  encrypt-message <message> <did>            Encrypt a message for a DID
  encrypt-wallet                             Encrypt wallet
  fix-wallet                                 Remove invalid DIDs from the wallet
  get-asset <id>                             Get asset by name or DID
  get-credential <did>                       Get credential by DID
  get-group <did>                            Get group by DID
  get-name <name>                            Get DID assigned to name
  get-schema <did>                           Get schema by DID
  help [command]                             display help for command
  import-wallet <recovery-phrase>            Create new wallet from a recovery phrase
  issue-credential <file> [registry] [name]  Sign and encrypt a bound credential file
  list-assets                                List assets owned by current ID
  list-credentials                           List credentials by current ID
  list-groups                                List groups owned by current ID
  list-ids                                   List IDs and show current ID
  list-issued                                List issued credentials
  list-names                                 Lists names of DIDs
  list-schemas                               List schemas owned by current ID
  perf-test [N]                              Performance test to create N credentials
  publish-credential <did>                   Publish the existence of a credential to the current user manifest
  publish-poll <poll>                        Publish results to poll, hiding ballots
  recover-id <did>                           Recovers the ID from the DID
  recover-wallet-did [did]                   Recover wallet from seed bank or encrypted DID
  remove-group-member <group> <member>       Remove a member from a group
  remove-id <name>                           Deletes named ID
  remove-name <name>                         Removes a name for a DID
  rename-id <oldName> <newName>              Renames the ID
  resolve-did <did> [confirm]                Return document associated with DID
  resolve-did-version <did> <version>        Return specified version of document associated with DID
  resolve-id                                 Resolves the current ID
  restore-wallet-file <file>                 Restore wallet from backup file
  reveal-credential <did>                    Reveal a credential to the current user manifest
  reveal-poll <poll>                         Publish results to poll, revealing ballots
  revoke-credential <did>                    Revokes a verifiable credential
  rotate-keys                                Generates new set of keys for current ID
  set-property <id> <key> [value]            Assign a key-value pair to an asset
  show-mnemonic                              Show recovery phrase for wallet
  show-wallet                                Show wallet
  sign-file <file>                           Sign a JSON file
  test-group <group> [member]                Determine if a member is in a group
  unpublish-credential <did>                 Remove a credential from the current user manifest
  unpublish-poll <poll>                      Remove results from poll
  update-asset <id> [file]                   Update an asset from a JSON file
  update-poll <ballot>                       Add a ballot to the poll
  use-id <name>                              Set the current ID
  verify-file <file>                         Verify the signature in a JSON file
  verify-response <response>                 Decrypt and validate a response to a challenge
  view-poll <poll>                           View poll details
  vote-poll <poll> <vote> [spoil]            Vote in a poll
```

Details on each command can be found in the [CLI User Manual](https://keychain.org/docs/keychain/clients/cli/)
