## The basis of iterators, blocks, proc, lambda
  
**iterators** : `each`, `map`, `inject`, `collect`, `sort`, `sort`

**blocks**    :

**proc**      :

**lambda**    : 

## When you are using a block

Instead of doing like :
``` ruby
arr = [1, 2, 3]
# you want ["1", "2", "3"]
arr.map{|item| item.to_s}
```
you can do it like this :
```
arr.map(&:to_s)
```