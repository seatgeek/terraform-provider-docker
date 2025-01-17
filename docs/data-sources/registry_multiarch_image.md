---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "docker_registry_multiarch_image Data Source - terraform-provider-docker"
subcategory: ""
description: |-
  Reads the image metadata for each manifest in a Docker multi-arch image from a Docker Registry.
---

# docker_registry_multiarch_image (Data Source)

Reads the image metadata for each manifest in a Docker multi-arch image from a Docker Registry.

## Example Usage

```terraform
### Must be a Docker multi-arch image
data "docker_registry_multiarch_image" "alpine" {
  name = "alpine:latest"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of the Docker image, including any tags. e.g. `alpine:latest`

### Optional

- `insecure_skip_verify` (Boolean) If `true`, the verification of TLS certificates of the server/registry is disabled. Defaults to `false`

### Read-Only

- `id` (String) The ID of this resource.
- `manifests` (Set of Object) The metadata for each manifest in the image (see [below for nested schema](#nestedatt--manifests))

<a id="nestedatt--manifests"></a>
### Nested Schema for `manifests`

Read-Only:

- `architecture` (String)
- `media_type` (String)
- `os` (String)
- `sha256_digest` (String)


