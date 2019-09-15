# list.sort() and sorted(list)
The difference between sort() and sorted()

## sort
sort() is a method of list.
This method rewrite the origin list.
```
origin_list = [4, 2, 6, 3]

origin_list.sort()
# [2, 3, 4, 6]
```

## sorted
sorted() is a built-in functions.
This method make a new list.
```
origin_list = [4, 2, 6, 3]

sorted_list = sorted(origin_list)
# origin_list: [4, 2, 6, 3]
# sorted_list: [2, 3, 4, 6]
```
