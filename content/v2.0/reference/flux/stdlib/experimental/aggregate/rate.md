---
title: aggregate.rate() function
description: >
  The `aggregate.rate()` function calculates the rate of change per windows of time.
menu:
  v2_0_ref:
    name: aggregate.rate
    parent: Aggregate
weight: 301
---

The `aggregate.rate()` function calculates the rate of change per windows of time.

_**Function type:** Transformation_

```js
import "experimental/query"

aggregate.rate(
  every: 1m,
  groupColumns: ["column1", "column2"],
  unit: 1s
)
```

## Parameters

### every
Duration of time windows.

_**Data type:** Duration_

### groupColumns
List of columns to group by. Defaults to `[]`.

_**Data type:** Array of strings_

### unit
The time duration to use when calculating the rate. Defaults to `1s`.

_**Data type:** Duration_

## Examples

```js
import "experimental/aggregate"

from(bucket: "example-bucket")
  |> range(start: -1h)
  |> aggregate.rate(every: 5m, unit: 1m)
```

## Function definition
```js
package aggregate

import "experimental"

rate = (tables=<-, every, groupColumns=[], unit=1s) =>
  tables
    |> derivative(nonNegative:true, unit:unit)
    |> aggregateWindow(every: every, fn : (tables=<-, column) =>
      tables
        |> mean(column: column)
        |> group(columns: groupColumns)
        |> experimental.group(columns: ["_start", "_stop"], mode:"extend")
        |> sum()
    )
```

_**Used functions:**_  
[aggregateWindow()](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/aggregatewindow/)  
[derivative()](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/derivative/)  
[experimental.group()](/v2.0/reference/flux/stdlib/experimental/group/)  
[group()](/v2.0/reference/flux/stdlib/built-in/transformations/group/)  
[mean()](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/mean/)  
[sum()](/v2.0/reference/flux/stdlib/built-in/transformations/aggregates/sum/)  
