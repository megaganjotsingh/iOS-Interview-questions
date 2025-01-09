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

Tuples group multiple values into a single one,  useful for returning multiple values from a function.