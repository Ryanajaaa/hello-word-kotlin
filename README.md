# Kotlin Hello World with VS Code

A simple guide to install Kotlin and run a Kotlin program using Visual Studio Code on Windows.

## Prerequisites

Before running this project, make sure you have:

- Java JDK 17 or newer
- Kotlin Compiler
- Visual Studio Code

Verify your installation:

```bash
java -version
javac -version
kotlinc -version
```

Expected output:

```text
openjdk 17.x.x
javac 17.x.x
info: kotlinc-jvm 2.4.0
```

---

## Project Structure

```
hello-world-kotlin/
│
├── main.kt
└── README.md
```

---

## Hello World Example

Create a file named `main.kt`:

```kotlin
fun main() {
    println("Hello, Kotlin!")
}
```

---

## Compile

Open a terminal in the project directory and run:

```bash
kotlinc main.kt -include-runtime -d main.jar
```

This command creates a file named:

```
main.jar
```

---

## Run

Run the generated JAR file:

```bash
java -jar main.jar
```

Output:

```text
Hello, Kotlin!
```

---

## Run in VS Code

1. Open the project folder in Visual Studio Code.
2. Open the integrated terminal (`Ctrl + ``).
3. Compile the project:

```bash
kotlinc main.kt -include-runtime -d main.jar
```

4. Run the application:

```bash
java -jar main.jar
```

---

## Verify Kotlin Installation

If Kotlin is installed correctly, this command should work:

```bash
kotlinc -version
```

Example output:

```text
info: kotlinc-jvm 2.4.0
```

---

## Common Issues

### `kotlinc` is not recognized

Make sure the Kotlin compiler `bin` directory is added to your system `PATH`.

Example:

```
C:\Users\<username>\Downloads\kotlin-compiler-2.4.0\kotlinc\bin
```

Restart your terminal or Visual Studio Code after updating the `PATH`.

---

### `Unable to access jarfile main.jar`

Compile the project before running:

```bash
kotlinc main.kt -include-runtime -d main.jar
```

Then run:

```bash
java -jar main.jar
```

---

### `Unresolved reference: println` in VS Code

If the project compiles successfully but VS Code shows:

```
Unresolved reference: println
```

this is usually caused by the Kotlin language extension, not by your code.

You can safely ignore the warning if `kotlinc` compiles without errors, or use IntelliJ IDEA for full Kotlin language support.

---

## Requirements

- Java JDK 17+
- Kotlin Compiler 2.4+
- Visual Studio Code

---

## Author

Created by **Ryan Andiya**
