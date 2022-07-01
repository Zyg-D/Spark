-  ```python
   df = df1.unionByName(df2, allowMissingColumns=True)  # 3.1
   # 2.3+
   diff1 = [c for c in df2.columns if c not in df1.columns]
   diff2 = [c for c in df1.columns if c not in df2.columns]
   df = df1.select('*', *[F.lit(None).alias(c) for c in diff1]) \
   .unionByName(df2.select('*', *[F.lit(None).alias(c) for c in diff2]))
   ```
-  ```python
   F.expr(r"regexp_extract_all(col, '(\\w+)', 1)")  # 3.1
   ```
-  ```python
   F.nth_value('col_name').over(w)  # 3.1
   ```
-  ```python
   F.raise_error('sulaužiau sparką, liūdesėlis')  # 3.1
   ```
-  ```python
   F.assert_true(F.lit(5) == F.lit(4), 'ojojoi koks erroras')  # SQL nuo 2.0
   ```
-  ```python
   F.forall("array_col", lambda x: x < 0)  # holds true for all  # SQL nuo 3.0
   ```
-  ```python
   F.exists("array_col", lambda x: x < 0)  # holds true for 1+  # SQL nuo 2.4
   ```
-  ```python
   F.transform('array_col', lambda x: x * 2)  # SQL nuo 2.4
   ```
-  ```python
   F.aggregate("array_col", lit(0), lambda acc, x: acc + x, lambda acc: acc**2)  # SQL nuo 2.4
   ```
-  ```python
   F.filter("array_col", lambda x: x < 0)  # keep which holds true  # SQL nuo 2.4
   ```
-  ```python
   F.expr("timestamp_millis(col_time)")  # <<< C.unix_to_timestamp('col_time', 'ms') ???  # 3.1
   ```



