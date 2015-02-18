Manipulating a DatetimeIndex

### Prepend an element
```python
index.insert(0, index[0] - 1)
```
List concatenation, such as `[index[0]-1] + index` doesn't work
since the index has the wrong type.


```R
c(index[1] - 1, index)
```
