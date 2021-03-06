---
title: View secret keys
description: View secret keys using the `influx` CLI or the InfluxDB API.
v2.0/tags: [secrets, security]
menu:
  v2_0:
    parent: Manage secrets
weight: 302
---

View secret keys using the `influx` command line interface (CLI) or the InfluxDB API.

## View secret keys using the influx CLI
Use the [`influx secret find` command](/v2.0/reference/cli/influx/secret/find/)
to list your organization's secret keys.

```sh
influx secret find
```

## View secret keys using the InfluxDB API
Use the `GET` request method and the InfluxDB `/orgs/{orgID}/secrets` API endpoint
to view your organization's secrets keys.

**Include the following:**

- Your [organization ID](/v2.0/organizations/view-orgs/#view-your-organization-id) in the request URL
- Your [authentication token](/v2.0/security/tokens/view-tokens/) in the `Authorization` header

<!-- -->
```sh
curl -XGET http://localhost:9999/api/v2/orgs/<org-id>/secrets \
  -H 'Authorization: Token YOURAUTHTOKEN'
```
