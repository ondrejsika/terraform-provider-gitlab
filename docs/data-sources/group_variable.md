---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "gitlab_group_variable Data Source - terraform-provider-gitlab"
subcategory: ""
description: |-
  The gitlab_group_variable data source allows to retrieve details about a group-level CI/CD variable.
  Upstream API: GitLab REST API docs https://docs.gitlab.com/ee/api/group_level_variables.html
---

# gitlab_group_variable (Data Source)

The `gitlab_group_variable` data source allows to retrieve details about a group-level CI/CD variable.

**Upstream API**: [GitLab REST API docs](https://docs.gitlab.com/ee/api/group_level_variables.html)



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `group` (String) The name or id of the group.
- `key` (String) The name of the variable.

### Optional

- `environment_scope` (String) The environment scope of the variable. Defaults to all environment (`*`). Note that in Community Editions of Gitlab, values other than `*` will cause inconsistent plans.
- `id` (String) The ID of this resource.

### Read-Only

- `masked` (Boolean) If set to `true`, the value of the variable will be hidden in job logs. The value must meet the [masking requirements](https://docs.gitlab.com/ee/ci/variables/#masked-variables). Defaults to `false`.
- `protected` (Boolean) If set to `true`, the variable will be passed only to pipelines running on protected branches and tags. Defaults to `false`.
- `value` (String) The value of the variable.
- `variable_type` (String) The type of a variable. Valid values are: `env_var`, `file`. Default is `env_var`.

