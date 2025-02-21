# Rust Memory Unsafety Example

This repository demonstrates a simple example of memory unsafety in Rust. The `bug.rs` file contains code that attempts to modify a vector's contents using a raw pointer.  This approach is extremely dangerous and can lead to undefined behavior, data corruption, and crashes. The `bugSolution.rs` file shows the safe and correct way to achieve the same outcome.

**Key Concepts:**

* **Raw Pointers:**  Raw pointers (`*const T` and `*mut T`) provide low-level access to memory but require careful handling to avoid memory safety violations.
* **Undefined Behavior:** In Rust, accessing or modifying memory in an unsafe way leads to undefined behavior; the compiler makes no guarantees about the program's outcome.
* **Memory Safety:** Rust's ownership and borrowing system is designed to prevent many common memory errors; however, unsafe code blocks (`unsafe {}`) allow bypassing these safety guarantees. Use them with extreme caution.

**How to Run:**

1. Clone this repository.
2. Navigate to the directory.
3. Compile and run the examples using `rustc bug.rs && ./bug` and `rustc bugSolution.rs && ./bugSolution`