---
title: influx task log find
description: The 'influx task log find' command outputs log information related to a task.
menu:
  v2_0_ref:
    name: influx task log find
    parent: influx task log
weight: 301
---

The `influx task log find` command outputs log information related to a task.

## Usage
```
influx task log find [flags]
```

## Flags
| Flag           | Description                 | Input type  |
|:----           |:-----------                 |:----------: |
| `-h`, `--help` | Help for the `find` command |             |
| `--run-id`     | Run ID                      | string      |
| `--task-id`    | **(Required)** Task ID      | string      |

{{% cli/influx-global-flags %}}
