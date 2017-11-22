tcollector is a framework to collect data points and store them in OpenTSDB.
It allows you to write simple collectors that it'll run and monitor.  It also
handles the communication with the TSDs.




## 改动
   将数据收集到opentsdb改动为将数据收集到openfalcon中，采用http的方式
+ 修改收集的数据格式为

```
 [
    {
        "endpoint": "test-endpoint",        主机名
        "metric": "test-metric",            metric
        "timestamp": ts,                    时间戳
        "step": 60,                         收集间隔（collectors目录下的值）
        "value": 1,
        "counterType": "GAUGE",             目前只支持gauve
        "tags": "idc=lg,loc=beijing",       tag（/soft/tcollector/collectors/etc/config.py配置）
    },

    {
        "endpoint": "test-endpoint",
        "metric": "test-metric2",
        "timestamp": ts,
        "step": 60,
        "value": 2,
        "counterType": "GAUGE",
        "tags": "idc=lg,loc=beijing",
    },
]
```

## 配置文件
```

```


For more info, see the [TCollector Documentation](http://www.opentsdb.net/tcollector.html)

[![Build Status](https://travis-ci.org/OpenTSDB/tcollector.svg?branch=master)](https://travis-ci.org/OpenTSDB/tcollector)


