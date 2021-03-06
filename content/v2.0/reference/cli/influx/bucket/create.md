---
title: influx bucket create
description: The 'influx bucket create' command creates a new bucket in InfluxDB.
menu:
  v2_0_ref:
    name: influx bucket create
    parent: influx bucket
weight: 201
---

The `influx bucket create` command creates a new bucket in InfluxDB.

## Usage
```
influx bucket create [flags]
```

## Flags
| Flag                | Description                                     | Input type  | {{< cli/mapped >}}   |
|:----                |:-----------                                     |:----------: |:------------------   |
| `-h`, `--help`      | Help for the `create` command                   |             |                      |
| `-n`, `--name`      | Bucket name                                     | string      | `INFLUX_BUCKET_NAME` |
| `-o`, `--org`       | Organization name                               | string      | `INFLUX_ORG`         |
| `--org-id`          | Organization ID                                 | string      | `INFLUX_ORG_ID`      |
| `-r`, `--retention` | Duration in nanoseconds bucket will retain data | duration    |                      |

{{% cli/influx-global-flags %}}
