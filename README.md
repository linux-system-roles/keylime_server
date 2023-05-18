# keylime_server

Ansible role for configuring and deploying the server components for Keylime Remote Attestation.

## Supported Distributions

* RHEL-9.1+, CentOS Stream 9.1+
* Fedora 36+

## Role Variables

These are the variables that can be passed to the role:

| **Variable** | **Default/Choices** | **Description** |
|----------|-------------|------|
`keylime_server_verifier_ip` |  127.0.0.1 |
`keylime_server_verifier_port` | 8881 |
`keylime_server_verifier_database_url` | |
`keylime_server_verifier_tls_dir` | generate |
`keylime_server_verifier_server_key` |  default |
`keylime_server_verifier_server_key_passphrase` | default |
`keylime_server_verifier_server_cert` | default |
`keylime_server_verifier_trusted_client_ca` |  default |
`keylime_server_verifier_client_key` | default |
`keylime_server_verifier_client_key_passphrase` | default |
`keylime_server_verifier_client_cert` | default |
`keylime_server_verifier_trusted_server_ca` | default |
`keylime_server_registrar_ip` |  127.0.0.1 |
`keylime_server_registrar_port` | 8891 |
`keylime_server_registrar_database_url` | sqlite |
`keylime_server_registrar_tls_dir` | default |
`keylime_server_registrar_server_key` |  default |
`keylime_server_registrar_server_key_passphrase` | default |
`keylime_server_registrar_server_cert` | default |
`keylime_server_registrar_trusted_client_ca` | default |


## Example Playbooks


```yaml
- name: Manage keylime servers
  hosts: all

  vars:
    keylime_server_verifier_ip: "{{ ansible_host }}"
    keylime_server_registrar_ip: "{{ ansible_host }}"

  roles:
    - linux-system-roles.keylime_server
```

## License

MIT
