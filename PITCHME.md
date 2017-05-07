## Functional

## Programming

### in

## PHP 

---

## Agenda

- First-class Functions
- Anonymous Functions |
- Closures |
- Recursion |
- Programming Limitations |

---

### First-class Functions

```
$input = array(1, 2, 3, 4, 5, 6);

// Creates a new anonymous function and assigns it to a variable
$filter_even = function($item) {
    return ($item % 2) == 0;
};

// Built-in array_filter accepts both the data and the function
$output = array_filter($input, $filter_even);

print_r($output);
```

---

### Anonymous Functions

```
$input = array(1, 2, 3, 4, 5, 6);

// Creates a new anonymous function and assigns it to a variable
$filter_even = function($item) {
    return ($item % 2) == 0;
};

// The function doesn't need to be assigned to a variable.
$output = array_filter($input, function($item) {
    return ($item % 2) == 0;
});

print_r($output);

```

---

### Closures

> A closure is an anonymous function that can access variables imported from the outside scope without using any global variables.
>
> Closures can work around variable scope restrictions in a clean way.

```
function criteria_greater_than($min) {
    return function($item) use ($min) {
        return $item > $min;
    };
}
```

---

### Recursion

> Recursion, a feature that allows a function to call itself, is supported by the language, but most of the PHP code focus is on iteration.

---

### Programming Limitations

- **No assignments**: Not allowed to assign values to variables. However allowed to assign functions to variables.

**Invalid**

```
$value = 10;
```

**Valid**

```
$value_ten = function() {
    return 10;
}
```

+++

### Programming Limitations

- **No assignments**: Not allowed to assign values to variables. However allowed to assign functions to variables.
- **No mutable state**: Not allowed, in case of an assignment, to change the value of that assignment.  Also, not allowed to change the value of any variable that had its value set as the parameter for the current function.  No changing of parameters.

+++

- **No mutable state**: Not allowed, in case of an assignment, to change the value of that assignment.  Also, not allowed to change the value of any variable that had its value set as the parameter for the current function.  No changing of parameters.

**Invalid**

```
function my_func($x) {
    $x = 2;
    ...
}
```

+++

### Programming Limitations

- **No assignments**: Not allowed to assign values to variables. However allowed to assign functions to variables.
- **No mutable state**: Not allowed, in case of an assignment, to change the value of that assignment.  Also, not allowed to change the value of any variable that had its value set as the parameter for the current function.  No changing of parameters.
- **No while and for loops**: Not allowed to use *while* or *for* commands.

+++

- **No while and for loops**: Not allowed to use *while* or *for* commands.

**Invalid**

```
$i = 1;
while ($i <= 10) {
    echo $i++;
}
```

and

```
for ($i = 1; $i <= 10; $i++) {
    echo $i;
}
```

or

```
$arr = array(1, 2, 3, 4);
foreach ($arr as &$value) {
    $value = $value * 2;
}
```