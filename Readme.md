# backup-mysql

Basic tool to backup mysql servers.


### Installation

    pip install --upgrade backup-mysql


### Setup

Create a `/etc/backups/backups.yaml` file with content similar to:

```yaml
backups:
  server:
    connection:
      type:                   mysql
      host:                   localhost
      username:               backup
      password:               password
    options:
      encryption:             secret
    s3:
      bucket:                 acme-backup-databases
      path:                   live/mysql/<suffix>

```

Now run it with

    backup-mysql server


### Build status

[![Build Status](https://travis-ci.org/ptdorf/backup-mysql.svg?branch=master)](https://travis-ci.org/ptdorf/backup-mysql)

  - http://jenkins.dotser.com/job/backup-mysql
  - https://travis-ci.org/ptdorf/backup-mysql
