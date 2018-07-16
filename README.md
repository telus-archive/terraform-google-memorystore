# terraform-google-memorystore

A Terraform module for creating a fully functional Google Memorystore instance.

# Module Input Variables

Required:

* `project` - The ID of the project in which the resource belongs to
* `name` - The name of the instance

Defaults:

* `region` - GCP region to use, defaults to `useast-1`
* `network_name` - The name of the network you want to use, defaults to `default`
* `tier` - The service tier of the instance, defaults to `STANDARD_HA`
* `memory_size_gb` - Memory size in GiB, defaults to `1`
* `location_id` - The zone where the instance will be provisioned, defaults to `us-east1-b`
* `alternative_location_id` - The alternative zone where the instance will be provisioned, defaults to `us-east1-d`
* `redis_version` - The version of Redis software, defaults to `REDIS_3_2`
* `display_name` - an arbitrary and optional user-provided name for the instance, defaults to nothing
* `reserved_ip_range` - The CIDR range of internal addresses that are reserved for this instance, defaults to `192.168.0.0/29`
* `labels` - Resource labels to represent user provided metadata, defaults to nothing


# Module Outputs

* `instance_id` - The memorystore instance id

# Usage

## Examples

Take a look at [memorystore.tf](./examples/basic/memorystore.tf) for a working example.

You can overwrite more default variables if you need to.

## Launching the Instance

Initialize Terraform:

```
terraform init
```

Review your changes:

```
terraform plan
```

Apply your changes:

```
terraform apply
```

Output Instance information:

```
terraform show
```

# Contributing

When contributing to this repository, please first discuss the change you wish to make via a Github issue.

# Contributors

* [Alex Podobnik](https://github.com/alexandarp)
