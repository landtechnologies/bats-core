# bats-core

A GitHub action for using [bats-core](https://github.com/bats-core/bats-core), a Bash Testing framework

## How do I use it?

```shell
- name: test
  uses: landtechnologies/bats-core@v2
  with:
    directory: some/working/directory
    args: --timing -r .
```

- `directory` is the working directory used prior to executing `bats`. If not specified it defaults to the current working directory.
- `args` are any subsequent arguments passed to bats, ie `bats {args}`. If not specified `bats` will not execute, and will just install on the host (so could be used in subsequent build steps).
