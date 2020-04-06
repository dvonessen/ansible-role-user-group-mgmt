# ansible-role-user-group-mgmt

This role creates users, primary user groups, and general groups

## Description

This role takes to dictionaries to create users and groups.
The dicts can provide a simple user cration up to a very complex creation.

## Role Variables


| Name                     | Default | Description                                                                                                   |
| :----------------------- | :-----: | ------------------------------------------------------------------------------------------------------------- |
| `user_group_mgmt_groups` |   {}    | This dict object provides an interface to create distinct groups. See [default/main.yml](./defaults/main.yml) |
| `user_group_mgmt_users`  |   {}    | This dict object privides an interface to create distinct users. See [default/main.yml](./defaults/main.yml)  |

## Role Tags

| Name                  | Description                                         |
| --------------------- | --------------------------------------------------- |
| user_group_mgmt_all   | Distinct tag to run all tasks of this role.         |
| user_group_mgmt_group | Tag to just run the groups creation/deletion tasks. |
| user_group_mgmt_user  | Tag to just run the users creation/deletion tasks.  |

## Dependencies

**None**

## Example Playbook

```yaml
- name: All
  hosts: all
  debugger: on_failed
  roles:
    - role: ansible-role-user-group-mgmt
```

For a more complete example see [sample playbook](molecule/default/converge.yml)

## License

MIT License

## Contributors

Daniel von Essen
