restic
=========

Sets up restic to backup to other servers via SFTP.

Requirements
------------

A user named `restic_local_user` on the local host and a user named
`restic_remote_user` on the remote host with SSH configured between these two.
For the latter the [ssh-link](https://gitlab.com/veenj/ansible-ssh-link) role of
veenj might come in handy.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`restic_passphrase` | supersecretpassphrase | required, passphrase for the backup
`restic_host` | `some.host.tld`             | required, remote host
`restic_local_user` | `local_user`          | required, user on the local host
`restic_local_paths` | `[]`                 | required, paths on the local host
`restic_remote_user` | `remote_user`        | required, remote user
`restic_remote_path` | `"/some/path"`       | required, path on the remote host

Dependencies
------------

None.

Example Playbook
----------------

See `molecule/default/playbook.yml`.

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
