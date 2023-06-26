# Security

First 5 min security of a server

## Requirements

N/A

## Role Variables

| Name              | Default | type       | Description            |
| ----------------- | ------- | ---------- | ---------------------- |
| new_root_password | `empty` | string     | new root password      |
| users             | `empty` | list(user) | List of user to create |

### User Structure

| Name         | Default | type   | description                   |
| ------------ | ------- | ------ | ----------------------------- |
| **name**     | `empty` | string | Username                      |
| **password** | `empty` | string | Password Hash for this user\* |

**mandatory**

Note \*: See https://docs.ansible.com/ansible/latest/reference_appendices/faq.html#how-do-i-generate-encrypted-passwords-for-the-user-module

## Dependencies

N/A

## Example Playbook

To include this role as part of your playbook:

**Declare the role dependency in your `requirements.yml`**

    roles:
      - src: git@github.com:gstmichel/ansible-security-role
        scm: git
        version: main
        name: gstmichel.security

**Include role to your playbook**

    - hosts: servers
      roles:
         - gstmichel.security
           root_password: insecure # Password will be change to insecure

## Example Role

To include this as a role dependencies in `meta/main.yml`:

    dependencies:
      - src: git@github.com:gstmichel/ansible-security-role
        scm: git
        version: main
        name: gstmichel.security

## License

MIT

## Author Information

- [Guillaume St-Michel](guillaume.stmichel@gmailcom)
