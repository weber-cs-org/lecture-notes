## Object-oriented

## Programming

### in

## PHP 

---

## Agenda

- Classes & Objects
- Inheritance |
- Interfaces |
- Visibility |

---

Classes & Objects
-----------------

**Declaration**

```
<?php
class Car {
    
}
```

+++

Classes & Objects
-----------------

**Properties**

```
<?php
class Car {
    private $_hasSunroof = true;
}
```

+++

Classes & Objects
-----------------

**Methods**

```
class Car {
    public function hasSunroof() {
        return &this->_hasSunroof;
    }
}
```

+++

Classes & Objects
-----------------

**Constants**

```
<?php
class Car {
    const ENGINE_V4 = 'V4';
    const ENGINE_V6 = 'V6';
    const ENGINE_V8 = 'V8';
}

echo Car::ENGINE_V6; // V6
```

+++

Classes & Objects
-----------------

**Instantiation**

```
<?php
$myCar = new Car();
if ($myCar->hasSunroof()) {
    echo 'Yay!';
}
```

---

Inheritance
-----------

```
<?php
class Chevy extends Car {
    
}
```

+++

Inheritance
-----------

```
<?php
interface Vehicle {
    public function hasSunroof();
}
```

+++

Inheritance (implementing)
--------------------------

```
<?php
class Car implements Vehicle {
    public function hasSunroof() {
        return $this->_hasSunroof;
    }
}
```

---

Visibility (public)
-------------------

- Default visibility
- Visible everywhere |

+++

Visibility (protected)
----------------------

- Visible to child classes
- Visible to object itself |
- Visible to other objects of the same type |

+++

Visibility (private)
--------------------

- Visible to the object itself
- Visible within the defining class declaration |

---



# Questions?
