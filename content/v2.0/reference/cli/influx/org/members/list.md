---
title: influx org members list
description: The 'influx org members list' command lists members within an organization in InfluxDB.
menu:
  v2_0_ref:
    name: influx org members list
    parent: influx org members
weight: 301
---

The `influx org members list` command lists members within an organization in InfluxDB.

## Usage
```
influx org members list [flags]
```

## Flags
| Flag           | Description                 | Input type  | {{< cli/mapped >}} |
|:----           |:-----------                 |:----------: |:------------------ |
| `-h`, `--help` | Help for the `list` command |             |                    |
| `-i`, `--id`   | Organization ID             | string      | `INFLUX_ORG_ID`    |
| `-n`, `--name` | Organization name           | string      | `INFLUX_ORG`       |

{{% cli/influx-global-flags %}}
