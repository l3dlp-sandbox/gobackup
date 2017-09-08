GoBackup
--------

A simple backup tool like [backup/backup](https://github.com/backup/backup) RubyGem.

## Features

- No deprecations.
- Multiple Databases source support.
- Multiple Storage type support.

## Current Support status

### Compressor

- Tgz - `.tar.gz`

### Databases

- MySQL
- Redis - `mode: sync/copy`

### Storages

- Local
- FTP

## Usage

```bash
$ gobackup perform
2017/09/08 06:47:36 ======== ruby_china ========
2017/09/08 06:47:36 WorkDir: /tmp/gobackup/1504853256396379166
2017/09/08 06:47:36 ------------- Databases --------------
2017/09/08 06:47:36 => database | Redis: mysql
2017/09/08 06:47:36 Dump mysql dump to /tmp/gobackup/1504853256396379166/mysql/ruby-china.sql
2017/09/08 06:47:36

2017/09/08 06:47:36 => database | Redis: redis
2017/09/08 06:47:36 Copying redis dump to /tmp/gobackup/1504853256396379166/redis
2017/09/08 06:47:36
2017/09/08 06:47:36 ----------- End databases ------------

2017/09/08 06:47:36 ------------- Compressor --------------
2017/09/08 06:47:36 => Compress with Tgz...
2017/09/08 06:47:39 -> /tmp/gobackup/2017-09-08T14:47:36+08:00.tar.gz
2017/09/08 06:47:39 ----------- End Compressor ------------

2017/09/08 06:47:39 => storage | FTP
2017/09/08 06:47:39 -> Uploading...
2017/09/08 06:47:39 -> upload /ruby_china/2017-09-08T14:47:36+08:00.tar.gz
2017/09/08 06:48:04 Cleanup temp dir...
2017/09/08 06:48:04 ======= End ruby_china =======
```
