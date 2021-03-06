---
title: influx backup – Back up data in InfluxDB
description: The 'influx backup' command backs up data stored in InfluxDB.
menu:
  v2_0_ref:
    name: influx backup
    parent: influx
weight: 101
v2.0/tags: [backup]
related:
  - /v2.0/backup-restore/backup/
---

The `influx backup` command backs up data stored in InfluxDB.

## Usage
```
influx backup [flags]
```

## Flags
| Flag           | Description                             | Input type | {{< cli/mapped >}} |
|:----           |:-----------                             |:----------:|:------------------ |
| `-h`, `--help` | Help for the `backup` command           |            |                    |
| `-p`, `--path` | Directory path to write backup files to | string     | `INFLUX_PATH`      |

{{% cli/influx-global-flags %}}
