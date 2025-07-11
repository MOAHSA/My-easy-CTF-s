# SecureSystem

A simple **Secure Login System** implemented in C++ featuring basic anti-debugging techniques and a custom password verification mechanism.

---

## Overview

This program simulates a secure login environment with the following features:

- **Username and password authentication** with a fixed username.
- **Password encryption** using character shifting and random padding.
- **Anti-debugging checks** to detect and prevent debugging attempts:
  - Uses `IsDebuggerPresent()` on Windows.
  - Uses `ptrace()` on Unix-like systems.
  - Detects unusual delays caused by debugging.
- Limits the number of login attempts to prevent brute force.
- Reveals a secret message upon successful authentication.

---

## Key Components

- **Anti-debugging methods** to detect if the program is being debugged.
- **Custom encryption logic** that processes password input and compares it with a predefined cipher and key.
- **Login flow** with input validation, attempt tracking, and user feedback.

---

## Usage

Compile and run the program.  
The user is prompted to enter a username and password.  
On successful authentication, the program displays a secret message.

---

## Dependencies

- Standard C++ libraries.  
- Platform-specific headers for anti-debugging features (`windows.h` on Windows, `sys/ptrace.h` on Unix).

---

## License

Feel free to use and modify this code for educational purposes.

---

Made with ❤️ to demonstrate basic security concepts in C++.
