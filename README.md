# Secrets and Policy Enforcer:

This project simulates a real task a Security Engineer Intern might work on at Atlassian: building tools to scan source code for security risks before it's merged into production.

##  What I Built so far:

### 1. `SecretScanner.java`
- Scans `.java` source code for **hardcoded secrets** such as:
  - AWS Access Keys (e.g., `AKIA...`)
  - API Tokens (e.g., `token = "123abc"`)
  - Passwords (e.g., `password = "hunter2"`)
- Uses regular expressions (regex) to search line-by-line for risky patterns.
- Outputs a CSV report of violations, showing:
  - File name
  - Line number
  - Secret type
  - Line content

### 2. `TestFile.java`
- A simulated Java source file located in the `test/` folder.
- Contains fake secrets like:
  - `String password = "hunter2";`
  - `String awsKey = "AKIAIOSFODNN7EXAMPLE";`
- Used to test and validate that the scanner detects real-world mistakes.

## Why This Project Matters

This is the kind of tool security engineers at companies like **Atlassian** use to catch sensitive info before it reaches production. It simulates a pre-merge security check — something that happens every day in DevSecOps.

Building this helped me understand:
- How to use Java for static code analysis
- How security scanning tools work under the hood
- How to use regex for practical security use cases

---

## 🚀 How to Run the Project

### Step 1: Compile
```bash
javac -d bin src/SecretScanner.java
