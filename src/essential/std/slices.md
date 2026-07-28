---
date: 2026-07-28
---

# slices

Go 官方推荐以后尽量使用它。

```go
import "slices"
```

## Clone 复制切片

```go
s2 := slices.Clone(s1)
```

## Equal 比较两个切片

```go
a:=[]int{1,2}
b:=[]int{1,2}
fmt.Println(slices.Equal(a,b))  // true
```

## Compare 字典序比较

返回  -1 0 1

```go
a:=[]int{1,2}
b:=[]int{1,3}
slices.Compare(a,b)   // -1
```

## Contains 判断是否存在

```go
s:=[]int{1,2,3}
fmt.Println(slices.Contains(s,2))  // true
```

## Index 查找位置

找不到返回 -1

```go
s:=[]int{1,4,8}
fmt.Println(slices.Index(s,4))   // 1
```

## Delete 删除区间

```go
s:=[]int{1,2,3,4,5}
s=slices.Delete(s,1,3)
fmt.Println(s)   // [1 4 5]
```

其实底层实现还是`append(s[:i],s[j:]...)`

## Insert 插入

```go
s:=[]int{1,2,3}
s=slices.Insert(s,2,100)   // [1 2 100 3]
```

## Replace 替换

```go
s:=[]int{1,2,3,4}
s=slices.Replace(s,1,3,9,8)  // [1 9 8 4]
``` 

## Compact 去重连续重复元素

```go
s:=[]int{1,1,2,2,3,3}
s=slices.Compact(s)    // [1 2 3]
``` 

注意：不是全局去重，只能去除连续重复

## Reverse 翻转

原地修改。

```go
s:=[]int{1,2,3,4}
slices.Reverse(s)   // [4 3 2 1]
```

## Sort 排序

```go
s:=[]int{3,5,1}
slices.Sort(s)   // [1 3 5]
```

## SortFunc 自定义排序

```go
slices.SortFunc(persons, func(a,b Person) int{
        return cmp.Compare(a.Age,b.Age)
    })
```

## Max Min 最大/小值

```go
m1:=slices.Max(s)
m2:=slices.Min(s)
```
