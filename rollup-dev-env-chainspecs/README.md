# `rollup` dev environments pregenerated randomized chainspecs

## Command used for chainspec generation
```bash
export IMAGE_VERSION='26de25adc6ecbfba763eb4ac12489e8cd50ee496'
export ENVIRONMENT_NAME='rollup-fungible'

docker run --rm -it mangatasolutions/rollup-node:${IMAGE_VERSION} build-spec --randomize-chain-genesis-salt --disable-default-bootnode --raw --chain=rollup-local > ./${ENVIRONMENT_NAME}-${IMAGE_VERSION:0:7}-raw.json
```