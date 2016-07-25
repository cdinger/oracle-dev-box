# Oracle Dev Box

A generic, empty Oracle XE instance for development purposes.

## Install

1. Download [`oracle-xe-11.2.0-1.0.x86_64.rpm`](http://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html)
and place the zip file in `puppet/modules/oracle/files/`.
2. `vagrant up`

This boots up an Oracle XE instance running on port 1521. Username is `sys`; password is `manager`.

Most of this was blatantly stolen from rails-dev-box-runs-oracle.

