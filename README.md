# 🖥️ simple-unix-shell — A Unix-like Command Line Shell in C

This project is a lightweight **Unix-style command-line shell**, written in C as part of the 42 curriculum.  
It was developed as a **group project**, where **I focused primarily on command parsing and data structures**, while my project partner focused on **command execution and process handling**.

> 🤝 **Project collaborators:**  
> - *Anton Kiiski*  
> - *Laura Guillen* https://github.com/solleksmori

---

## 📌 What the Program Does

`simple-unix-shell` behaves similarly to a basic Unix shell. It continuously:

1. Displays a prompt  
2. Reads user input  
3. Parses commands into a structured format  
4. Executes programs  
5. Waits for the next command  

The shell allows users to run system commands, chain them together, redirect input/output, and interact with the environment.

---

## ✨ Features

- Execute external programs using system calls  
- Built-in commands (such as `cd`, `exit`, etc.)  
- Support for pipes (`|`)  
- Input and output redirections (`<`, `>`, `>>`)  
- Environment variable handling  
- Signal handling (e.g. `Ctrl-C`, `Ctrl-D`)  
- Error handling and graceful failures  

---

## 🔧 Building the Project

Inside the project directory:

```bash
make
```
Other useful commands:
```bash
make clean
make fclean
make re
```

---

## ▶️ Running the Shell

Start the shell by running:
```bash
./minishell
```
You can then type commands as you would in a normal Unix shell, for example:
```bash
ls -l
echo "Hello world"
cat file.txt | grep test
```

---

## 🧠 How It Works (High Level)

- User input is read from standard input
- The command line is tokenized and parsed
- Commands are organized into an Abstract Syntax Tree (AST)
- Linked lists are used as core data structures for tokens, commands, and environment variables
- Pipes and redirections are resolved based on the AST structure
- Child processes are created using fork
- Programs are executed with execve
- The parent process waits for child processes to finish
- Signals are handled to keep the shell responsive

---

## 🧵 What I Learned

- Designing and implementing a robust command parser
- Structuring shell logic using an Abstract Syntax Tree (AST)
- Using linked lists to model flexible, dynamic data
- Handling complex input syntax and edge cases
- Collaborating on a low-level systems project with clear ownership areas

---

## 📄 Notes

- This project emphasizes systems programming fundamentals:
- Parsing complex user input
- Structuring execution logic with an AST
- Managing processes and file descriptors
- Writing stable, predictable low-level C code
- It was built to deepen understanding of how Unix shells work internally.

