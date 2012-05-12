# Before you start to learn the block tricks, please be sure you know the following basic knowledge
  
how to use these iterators : `each`, `map`, `inject`, `collect`, `sort`, `sort`
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