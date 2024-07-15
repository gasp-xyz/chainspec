# `rollup` dev environments pregenerated randomized chainspecs

## Command used for chainspec generation

```bash
export MANGATA_NODE_REPO_ROOT=<path-to-mangata-node-repo-root>
export CHAINSPEC_REPO_ROOT=<path-to-chainspec-repo-root>
export ENVIRONMENT_NAME='rollup-frontend'

cd ${MANGATA_NODE_REPO_ROOT} 
cargo build --release

./target/release/rollup-node build-spec --randomize-chain-genesis-salt --disable-default-bootnode --raw --chain=rollup-local > "${CHAINSPEC_REPO_ROOT}/rollup-dev-env-chainspecs/${ENVIRONMENT_NAME}-$(/usr/bin/git rev-parse --short=7 HEAD)-raw.json"
```