**THIS ROLE IS WIP. DO NOT USE**

You'll need to add /home/.github-backup/.ssh/id_rsa.pub to SSH Keys on GitHub

?? Also need to set ENV['GITHUB_ACCESS_TOKEN'] in /home/.github-backup/.profile so that it has access to private repos

Usage
-----

```yaml
- name: Backup GitHub Repositories
  hosts: all
  roles:
    - { role: github_backup, username: garethrees, backup_root: /var/github-backup, token: S3CR3T }
```

TODO
----

- Doesn't seem to work when run by cron
- Allow specifying the github-backup user
- Figure out how to set API Token
- Use run-with-lockfile?
- Check sticky group is being set on cloned repos

LICENCE
-------

[GNU GPL v3.0](LICENCE), for now
