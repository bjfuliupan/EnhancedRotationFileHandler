# EnhancedRotationFileHandler
Enhanced version of the RotationFileHandler

## 介绍
类TimedRotaingFileHandler只能按照时间对日志文件进行分片，但对同一时间的日志文件不能限制大小，或按照大小进行分片。  
类RotatingFileHandler只能限制文件大小，以及按照大小对日志文件进行分片，而不能按时间进行分片。

EnhancedRotatingFileHandler结合了TimedRotaingFileHandler和RotatingFileHandler的优点：既能按照时间进行分片，又能对同一时间的文件按照大小进行分片。

EnhancedRotatingFileHandler将TimedRotaingFileHandler和RotatingFileHandler的源码进行整合，增加了协调逻辑，以及对RotatingFileHandler的逻辑进行调整以满足需求。

## 分片例子
### RotaingFileHandler
example.log<br>
example.log.1<br>
example.log.2<br>
example.log.3<br>

### TimedRotaingFileHandler
example.2019-04-28.log<br>
example.2019-04-29.log<br>

### EnhancedRotaingFileHandler
example.2019-04-28.log<br>
example.2019-04-28.log.1<br>
example.2019-04-28.log.2<br>
example.2019-04-28.log.3<br>
example.2019-04-29.log<br>
example.2019-04-29.log.1<br>
example.2019-04-29.log.2<br>
example.2019-04-29.log.3<br>
