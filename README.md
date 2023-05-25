# Security

First 5 min security of a server

## Requirements

N/A

## Role Variables

| Name              | Default | Description       |
| ----------------- | ------- | ----------------- |
| new_root_password | `empty` | new root password |

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
