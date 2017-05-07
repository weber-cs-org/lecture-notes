## Functional

## Programming

### in

## PHP 

---

## Agenda

- First-class Functions
- Recursion |
- Anonymous Functions |
- Closures |
- Programming Limitations |

---

### First-class Functions

---

### Recursion

---

### Anonymous Functions

---

### Closures

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

### Programming Limitations

- **No assignments**: Not allowed to assign values to variables. However allowed to assign functions to variables.
- **No mutable state**: Not allowed, in case of an assignment, to change the value of that assignment.  Also, not allowed to change the value of any variable that had its value set as the parameter for the current function.  No changing of parameters.
- **No while and for loops**: Not allowed to use *while* or *for* commands.