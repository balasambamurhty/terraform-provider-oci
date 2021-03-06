---
layout: "oci"
page_title: "OCI: oci_objectstorage_object_head"
sidebar_current: "docs-oci-datasource-object_storage-object_head"
description: |-
  Provides a list of Object metadata
---

# Data Source: oci_objectstorage_object_head
The `oci_objectstorage_object_head` data source allows access to the list of OCI object metadata

Provides a datasource for fetching object metadata.

## Example Usage

```hcl
data "oci_objectstorage_object_head" "test_object_head" {
	#Required
	bucket = "${var.object_bucket}"
	namespace = "${var.object_namespace}"
	object = "${var.object_object}"
}
```

## Argument Reference

The following arguments are supported:

* `bucket` - (Required) The name of the bucket. Avoid entering confidential information. Example: `my-new-bucket1` 
* `namespace` - (Required) The top-level namespace used for the request.
* `object` - (Required) The name of the object. Avoid entering confidential information. Example: `test/object1.log` 


## Attributes Reference

The following attributes are exported:
 
* `metadata` - The metadata of the object
* `content-type` - The content-type of the object
* `content-length` - The content-length of the object

