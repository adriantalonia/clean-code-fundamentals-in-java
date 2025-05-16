# ✨ 3. Clean Code Best Practices

## 📋 Table of Contents

- [✨ 3. Clean Code Best Practices](#-3-clean-code-best-practices)
  - [📋 Table of Contents](#-table-of-contents)
  - [🗣️ 3.1 Communicate Through Code](#️-31-communicate-through-code)
  - [📏 3.1.1 Use Java Code Conventions and Avoid Misinformation](#-311-use-java-code-conventions-and-avoid-misinformation)
    - [🧠 Purpose](#-purpose)
    - [🧪 Bad Examples](#-bad-examples)
    - [✅ Good Examples](#-good-examples)
    - [⚠️ Additional Misleading Code](#️-additional-misleading-code)
    - [📚 Resources for Java Code Style](#-resources-for-java-code-style)
  - [🎯 Summary Table](#-summary-table)
  - [🧾 3.1.2 Choose an Expressive Name and Avoid Mental Mapping](#-312-choose-an-expressive-name-and-avoid-mental-mapping)
    - [🧠 Purpose](#-purpose-1)
    - [🧪 Bad Examples](#-bad-examples-1)
  - [✅ Good Examples](#-good-examples-1)

## 🗣️ 3.1 Communicate Through Code

> "There are only two hard things in Computer Science: cache invalidation and naming things."  
> — Phil Karlton

Code should not just execute correctly — it should **communicate its intent** clearly and unambiguously to the reader. This means that every method, variable, and class name must make the code **self-explanatory**.

Clean code speaks for itself. Good naming, structure, and conventions prevent bugs, reduce cognitive overhead, and enable long-term maintainability.

---

## 📏 3.1.1 Use Java Code Conventions and Avoid Misinformation

### 🧠 Purpose
Java code conventions improve:
- **Readability**
- **Consistency**
- **Maintainability**
- **Team collaboration**

They also help prevent **misunderstandings or misinformation** caused by inconsistent naming or formatting.

---

### 🧪 Bad Examples

```java
public static final double pi = 3.14159265358979323846;
int YEAR;
String first_name;
public class convert_strategy {}
Set carList;
```

**Issues Identified:**

| Violation            | Explanation                                       |
| -------------------- | ------------------------------------------------- |
| 🔠 Constant Naming    | `pi` should be `PI` (UPPER_SNAKE_CASE).           |
| 🆎 Variable Casing    | `YEAR` should be `year`.                          |
| 🐫 Camel Case         | `first_name` → `firstName`.                       |
| 🧱 Class Naming       | `convert_strategy` → `ConvertStrategy`.           |
| 📦 Data Type Accuracy | `carList` is a `Set`, so name should be `carSet`. |

---

### ✅ Good Examples

```java
public static final double PI = 3.14159265358979323846;
int year;
String firstName;
public class ConvertStrategy {}
Set carSet;
```

---

### ⚠️ Additional Misleading Code

```java
Customer Customer = new Customer("Darth Vader");
Customer.name(); // Misleading - static?
```

**Problems:**
- 🚫 `Customer` (variable) conflicts with `Customer` (class).
- 😕 `Customer.name()` may be misunderstood as a static method.

✅ Better version:

```java
Customer customer = new Customer("Darth Vader");
customer.name();
```

---

### 📚 Resources for Java Code Style

- Oracle Java Code Conventions:  
  https://www.oracle.com/technetwork/java/codeconventions-150003.pdf

- Google Java Style Guide:  
  https://google.github.io/styleguide/javaguide.html

---

## 🎯 Summary Table

| Aspect              | Follow Convention Example | Avoid Example             |
| ------------------- | ------------------------- | ------------------------- |
| Constants           | `PI`                      | `pi`                      |
| Variables           | `year`                    | `YEAR`                    |
| CamelCase           | `firstName`               | `first_name`              |
| Class Names         | `ConvertStrategy`         | `convert_strategy`        |
| Type-Accurate Names | `carSet`                  | `carList` (if not a list) |
| Naming Clarity      | `customer.name()`         | `Customer.name()`         |

---

> 💡 "Communicating clearly through code starts with following basic conventions. Avoid confusion, reduce bugs, and make your code a joy to read."

---
---

## 🧾 3.1.2 Choose an Expressive Name and Avoid Mental Mapping

### 🧠 Purpose

Using expressive, self-descriptive names in code removes the need for mental interpretation. Avoid abbreviations or ambiguous names that require developers to mentally "map" a variable to its meaning. Code should read like prose and explain itself.

---

### 🧪 Bad Examples

```java
int d; // days since birthday
String n; // name of host
```

| Problem                | Explanation                                                                        |
| ---------------------- | ---------------------------------------------------------------------------------- |
| ❓ Ambiguity            | Variable names like `d` or `n` lack context, making their purpose unclear.         |
| 🧠 Mental Mapping       | Developers must rely on comments or external documentation to understand the code. |
| 🛠️ Not Self-Explanatory | The variable names do not convey their intent, reducing code readability.          |

## ✅ Good Examples

```java
int daysSinceBirthday;
String hostname;
```

**Why is this better?**

- Directly expresses the purpose of each variable.
- No need for comments or additional documentation.
- Helps maintain clean, self-documenting code.

| Guideline                      | Description                                                               |
| ------------------------------ | ------------------------------------------------------------------------- |
| Use descriptive names          | `totalAmount` is better than `ta`                                         |
| Avoid single-letter variables  | Except for simple loop counters like `i`                                  |
| Expand abbreviations           | `hostname` instead of `hn`, `count` instead of `cnt`                      |
| Stay consistent in terminology | Always use the same term for the same concept (e.g., `email`, not `mail`) |
| Prioritize clarity             | Choose names that make purpose obvious to any developer                   |

> 💡 "Good names eliminate the need for comments. They clarify purpose and reduce the risk of misunderstanding."