**Spark decimal** is probably not the same as Java BigDecimal, as `scale` in Spark can't be negative.
```none
decimal(precision, scale)
    precision : 1 <= precision <= 38
    scale     : 0 <= scale <= precision

`precision` must be of such size that it could hold ALL the digits: before and after the decimal point.

`precision` is a frame, `scale` is how much do we shift it to the right.  
First, the frame is put on the number so that the right side of the frame is on the decimal point.  
Then, `scale` shift is applied. After scale shift: 
    if the left side of the frame cut off part of the number, the result is null;
    if the right side of the frame went beyond the number, zeros are filled to the left of the right side of the frame;
    if the right side of the frame cut off part of the number, rounding is applied so that no digit remains to the right.
If precision = scale, only those numbers will remain, which don't have a whole number part before the decimal point.
```
