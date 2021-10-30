Create a df

```scala
import spark.implicits._
var df = Seq(
    ("xx", "yy", 2),
    ("qq", "zz", 7)
).toDF("c1", "c2", "value")
```
