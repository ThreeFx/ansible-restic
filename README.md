restic
=========

Sets up restic to backup to other servers via SFTP.

Requirements
------------

A user named `restic_local_user` on the local host and a restic repository. If
remote be sure that SSH is configured between these two.  For the latter the
[ssh-link](https://gitlab.com/veenj/ansible-ssh-link) role of veenj might come
in handy.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`restic_password` | supersecretpassword     | required, password for the backup
`restic_local_user` | `local_user`          | required, user on the local host
`restic_local_paths` | `[]`                 | required, paths on the local host
`restic_repository` | "sftp:user@host:/dst" | required, repository to back up to
`restic_name` | "mybackup" | required, name of the backup (in case of multiple
jobs)

Dependencies
------------

None.

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
