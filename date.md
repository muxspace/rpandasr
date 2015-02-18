Manipulating a DatetimeIndex

### Prepend an element
List concatenation, such as `[index[0]-1] + index` doesn't work
since the index has the wrong type. Instead you need to use the
`insert` method of `DatetimeIndex`.
```python
index = index.insert(0, index[0] - 1)
```
While `list.insert()` mutates the list in place, this is not the
case with `DatetimeIndex.insert()`, which does not change the 
underlying object. So for a list, don't assign the return value
as it will be `None`, but for a DatetimeIndex, *do* assign the
return value. 

Outside of ReferenceClasses, operations in R have pass-by-value
semantics, so operations always have a valid return value.
```R
index <- c(index[1] - 1, index)
```
