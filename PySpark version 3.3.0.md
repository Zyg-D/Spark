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
   df.agg(F.max_by('col_value', 'col_order'))
   df.agg(F.min_by('col_value', 'col_order'))
   ```
   <sup>(non-deterministic: just 1 value returned)</sup>

-  ```python
   F.make_date(2020, 12, 31)
   ```


