############################################################################
# ------------------------------------------------------------------------
# Copyright 2020 VMware, Inc.  All rights reserved. VMware Confidential
# ------------------------------------------------------------------------
###

---
layout: "avi"
page_title: "Avi: avi_useraccountprofile"
sidebar_current: "docs-avi-resource-useraccountprofile"
description: |-
  Creates and manages Avi UserAccountProfile.
---

# avi_useraccountprofile

The UserAccountProfile resource allows the creation and management of Avi UserAccountProfile

## Example Usage

```hcl
resource "avi_useraccountprofile" "foo" {
    name = "terraform-example-foo"
    tenant_ref = "/api/tenant/?name=admin"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) Name of the object.
* `account_lock_timeout` - (Optional) Lock timeout period (in minutes).
* `credentials_timeout_threshold` - (Optional) The time period after which credentials expire.
* `max_concurrent_sessions` - (Optional) Maximum number of concurrent sessions allowed.
* `max_login_failure_count` - (Optional) Number of login attempts before lockout.
* `max_password_history_count` - (Optional) Maximum number of passwords to be maintained in the password history.


### Timeouts

The `timeouts` block allows you to specify [timeouts](https://www.terraform.io/docs/configuration/resources.html#timeouts) for certain actions:

* `create` - (Defaults to 40 mins) Used when creating the AMI
* `update` - (Defaults to 40 mins) Used when updating the AMI
* `delete` - (Defaults to 90 mins) Used when deregistering the AMI

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `uuid` -  Unique object identifier of the object.

