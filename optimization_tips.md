**`select(col.alias('c')` > `.withColumn('c', col)`**

Examples and references: https://stackoverflow.com/questions/59789689

**Increase Shuffle partitions**

Going over default 200 may remove OOM error.  
http://orastack.com/spark-scaling-to-large-datasets.html

**Have smaller and more executors, rather than larger and few executors**

http://orastack.com/spark-scaling-to-large-datasets.html


