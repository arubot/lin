# Lin
Dynamic scripting language based on Kotlin, forked from Kaiper

### What's this?

Currently on closed development, **Lin** is a attempt to run a kotlinscript (`.kts`) subset as a interpreted language, as opposed to a compiled language.

### But why?

I really like the Kotlin syntax and I want to let users be able to run custom commands on Aru using this language.

### What will be the differences?

Mostly, due to it being a interpreted language, there'll be a lack of static-checking. Furthermore, I'm not really wanting to implement a type-system, so variables and functions will have some really simple support for types parameters/return types at all.

### Actual Examples

#### Kotlinscript
```kts
val s: String

s = "Hello World!"

fun print(str: String) : Unit {
  kotlin.io.println(str)
}

fun now() : Int = System.currentTimeMillis()

fun makeResult(v: String, i: Int) : String {
  return "$v - result $i"
}

print(makeResult(s, now()))
```

#### Lin
```kts
val s

s = "Hello World!"

fun print(str) {
  lin.io.println(str)
}

fun now() = lin.sys.currentTimeMillis()

fun makeResult(v, i) {
  return "$v - result $i"
}

print(makeResult(s, now()))
```

### ETA

Probably when I finish implementing Custom Commands on Aru.
