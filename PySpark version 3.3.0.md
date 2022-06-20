-  ```python
   df.isEmpty()  # <-- (len(df.head(1)) == 0)
   ```

-  ```python
   df.withColumns()
   ```

-  ```python
   df.transform(func, *args, **kwargs)  # <-- df.transform(func)
   ```

-  ```python
   F.col('col_name').ilike('%str%')
   ```

-  ```python
   df.groupBy().agg(F.max_by('col_value', 'col_order'))
   df.groupBy().agg(F.min_by('col_value', 'col_order'))
   ```
   (non-deterministic: just 1 value returned)

-  ```python
   F.make_date(2020, 12, 31)
   ```


