# 基础I/O
## 字符串基础
[关于字符串的详细信息](string.md)\
此处你需要知道的是，你可以在一对`""`放若干字符，它们可以构成字符串
```jl
julia> "A quick brown fox jumps over the lazy dog."
"A quick brown fox jumps over the lazy dog."

julia> "喵(　o=^•ェ•)o"
"喵(　o=^•ェ•)o"
```

## print
`print`是基本的输出方式
```jl
julia> print(0)
0
julia> print(1,2,3) # 接受多个参数
123
julia> print("world.me.say_hello()")
world.me.say_hello()
julia>
```

## println
`println`与`print`相似，不同的是在末尾会多进行一次换行
```jl
julia> println(0)
0

julia> println(1,2,3)
123

julia>
```

## printstyled
`printstyled`允许你在控制台允许的情况下输出有风格的文字（例如彩色）
```jl
julia> printstyled(1,2,3;color=:red)
123 # 你看，这里不允许，使用输出没有特殊效果（
```

[windows的相关支持](https://docs.microsoft.com/zh-CN/windows/console/console-virtual-terminal-sequences)

## 输入
为方便进行之后的练习，现提供以下代码
```jl
julia> a=readuntil(stdin,' '); b=readline() # 前者读到空格为止，后者读到行尾
first second
"second"

julia> a
"first"

julia> b
"second"
```

利用`parse`函数，你可以读入整数
```jl
julia> a=parse(Int,readuntil(stdin,' ')); b=parse(Int,readline())
2333 4
4

julia> a,b
(2333, 4)
```

```is-newbie
## 练习
- [Hydro langs P1. io](https://hydro.ac/d/langs/p/P1)
- [Hydro H1000. A + B Problem](https://hydro.ac/p/H1000?lang=zh)
```
