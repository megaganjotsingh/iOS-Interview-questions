#### What is Swift?
- Swift is a Powerful language and it is developed for ios, macos, watchos and tvos applications.
- Swift uses concise syntex, type inference and does not reuire headers.
  For eg: 
  `let name = "Gaganjot Singh"`
  here it is concise 
  1. does not need to define type
  2. does not need semi colon.

---

#### Key Features?
1. Type Safety and inference → when we assign the values to some object it is required of the same type otherwise we will have compile errors. 
2. Optionals for Null Safety.
3. Closures and Generics
4. Automatic Reference Counting
5. Protocol Oriented Programming 

---

#### Explain Optionals and uses?

Optional allow a variable to hold a nil if no value is exist. This avoids run time crashes caused by null references.

```
var age: Int? = nil

age = 25

// optional binding

if let nonNilAge = age { 
	print("Non Nil Age: \(validAge)")
}
```

---

#### What is a guard statement, and how is it different from if?
guard ensures early exit if condition is not met. It’s often used for input validation.

```
var age: Int? = nil

age = 25

// optional binding

guard let age else { 
	print("age is nil")
	return
}
```

Differences-
- guard provides early exit.
- we can avoid pyramid of doom situation with guard

---

#### 5. What are tuples in Swift, and when would you use them?

Tuples group multiple values into a single one, useful for returning multiple values from a function.

```
func getPrice() -> (price: Double, currency: String) { 
	return (45.5, "$")
}

print("Price is: \(getPrice().currency) \(getPrice().price)")
```

---

#### Explain the difference between let and var?
let defines a constant (immutable).
var defines a variable (mutable).

```
let name = "Gagan"
name = "Gaganjot" // Cannot assign to value: 'name' is a 'let' constant

var name2 = "singh"
name2 = "Singh"
```

---

#### What is type inference in Swift?
Swift can infer the type of a variable or constant based on its initial value.

```
let age = 28 // Swift can infer the type of age based on 43 ie: Int
let name = "Gaganjot Singh" // Swift can infer the type of name based on "Gaganjot Singh" ie. String
```

---

#### What is a Protocol in Swift, and how is it different from a class?
A protocol defines a blueprint of methods and properties that a class, struct or enum must implement, but it does not provide the actual implementation.

Difference between Class and Protocol
1. Implementation:
   - A protocol does not provide implementation
   - A class can have implementation.
2. Inheritance:
   - A protocol can be adopted by multiple types (class, struct, enum)
   - A class can inherit the parent class (single inheritance).





---

#### What is a difference between Struct and Class?

| Feature           | Struct                             | Class                  |
| ----------------- | ---------------------------------- | ---------------------- |
| Memory Allocation | Value type (copied)                | Refernce Type (shared) |
| Inheritance       | Not supported                      | Supported              |
| Mutability        | Needs mutating keyword for changes | var allow changes      |
| ARC               | Not aplicable                      | Managed by ARC         |

Example
```
struct UserStruct { 
	var name: String
}

var user1 = UserStruct(name: "Gagan")
var user2 = user1
user2.name = "Gaganjot"

print(user1.name) // It will print: Gagan

class UserClass { 
	var name: String
	init(name: String) { 
		self.name = name
	}
}

var user3 = UserClass(name: "singh")
var user4 = user3
user4.name = "Singh"
print(user3.name) // It will print: Singh
```
---
