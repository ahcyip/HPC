## Interactive R
```
$ apptainer run instance://spark sparkR # for sparklyr use. for sparkR, need to specify path
> library(sparklyr)
> sc = spark_connect(master = paste0("spark://",Sys.info()["nodename"],":7077"))
> df = spark_read_parquet(sc = sc, path = "my_data.parquet", memory = FALSE)
```
