# What?

A lisp-like compile-to JS language.

# Language

## Arrays

```
[ 1 2 3 4 5 ]
```

## Objects

### Creation

Create a new blank object

```
make obj
```

### Setting

```
set obj key value
```

### Getting

```
get obj key
```

## Comments

### Single Line

```
// i am a comment
```

### Multi Line

```
/*
  i am a comment
*/
```

## Variable Assignment

```
$ a 1
```

## Function Calling

```
(add one two)
// add(one, two)
```

## Function declaration

```
def myFn [ one two ] {
  (add one two)
}
```

## Flow control

### iterate

```
$ arr [ 1 2 3 4 ]
@arr {
  (console.log item)
}
```

```
@[ 1 2 3 ] {
  (console.log item)
}
```

### if

```
? expression {

} else {

}
```

```
$ a 'hello'

? a is 'hello' {
  (console.log 'hello world!')
} else {
  (console.log 'not hello world :(')
}
```

```
? err exists {
  ! err
}
```

```
$ str 'hello world'
$ strCheck 'o w'

? str contains strCheck {
  (console.log str 'contains' strCheck)
} else {
  (console.log str 'doesnt contain' strCheck)
}
```

```
(someFn def cb [ err result ] {
  ? err kinda true {
    (console.log 'omg an error!!')
    ! err
  }
  (console.log result)
})
```

## Return Value

```
! 5 // return 5
```

```
def return5ifStringContains5Else0 [ str ] {
  ? str contains 5 {
    ! 5
  } else {
    ! 0
  }
}
```

## Modules

### Importing

```
use 'fs' as fs
```

### Exporting

```
export fs
```

### Math

#### Additionion

```
$ five (add 3 2)
```

#### Subtraction

```
$ two (sub 1000 998)
```

#### Multiplication

```
$ sixhundred (mul 100 6)
```

#### Division

```
$ two (div 10 5)
```

#### Modulus

```
$ three (mod 3 100)
```
