# LoadLeveler Client

> This project is no longer maintained since we don't use AIX in NWPC after 2019.

A cli client for LoadLeveler in NWPC.

## Features

- Query jobs.
- Filter certain jobs.

## Installing

Install [nwpc-hpc-model](https://github.com/nwpc-oper/nwpc-hpc-model) package.

Install `loadleveler-client` package.

## Getting started

Query LoadLeveler jobs:

```
lllcient query
```

Use `llclient query --help` to see options.

Use `llclient --help` to see more subcommands.

## Config

`loadleveler-client` uses a YAML file to categories which are extracted from loadleveler `llq` command. Such as

```yaml
category_list:
  -
    id: "llq.id"
    display_name: "Id"
    label: "Job Step Id"
    record_parser_class: "DetailLabelParser"
    record_parser_arguments:
      - "Job Step Id"
    value_saver_class: "StringSaver"
    value_saver_arguments: []
  -
    id: "llq.owner"
    display_name: "Owner"
    label: "Owner"
    record_parser_class: "DetailLabelParser"
    record_parser_arguments:
      - "Owner"
    value_saver_class: "StringSaver"
    value_saver_arguments: []
```

Default config file is installed.

## LICENSE

Copyright &copy; 2016-2019, Perilla Roc

`loadleveler-client` is licensed under [GPL-3.0](./LICENSE.md)

