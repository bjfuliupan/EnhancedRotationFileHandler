# EnhancedTimedRotationFileHandler
Enhanced version of the TimedRotationFileHandler

## 介绍
类TimedRotaingFileHandler只能按照时间对日志文件进行分片，但对同一时间的日志文件不能限制大小，或按照大小进行分片。
类RotatingFileHandler只能限制文件大小，以及按照大小对日志文件进行分片，而不能按时间进行分片。

EnhancedTimedRotatingFileHandler结合了TimedRotaingFileHandler和RotatingFileHandler的优点：既能按照时间进行分片，又能对同一时间的文件按照大小进行分片。

## 分片例子
### RotaingFileHandler
example.log\r\n
example.log.1\r\n
example.log.2\r\n
example.log.3\r\n

### TimedRotaingFileHandler
example.2019-04-28.log\r\n
example.2019-04-29.log\r\n

### EnhancedTimedRotaingFileHandler
example.2019-04-28.log\r\n
example.2019-04-28.log.1\r\n
example.2019-04-28.log.2\r\n
example.2019-04-28.log.3v
example.2019-04-29.log\r\n
example.2019-04-29.log.1\r\n
example.2019-04-29.log.2\r\n
example.2019-04-29.log.3\r\n
