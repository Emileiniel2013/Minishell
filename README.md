# Minishell

Minishell is a custom Unix-like shell written entirely in **C**, designed to mimic the core behavior of **bash**.  
It handles user input, executes commands, manages child processes, and implements redirections and pipelines — all from scratch.

This project was a deep dive into how shells actually work under the hood: process creation, I/O redirection, signal handling, and environment management.

## ⚙️ Features
- Command parsing with quotes and environment variables
- Pipelines (`|`) and redirections (`>`, `<`, `>>`)
- Built-in commands: `cd`, `echo`, `env`, `export`, `unset`, `pwd`, `exit`
- Signal handling (`Ctrl+C`, `Ctrl+D`, `Ctrl+\`)
- Exit codes matching Bash behavior
- Proper memory management and error handling

## 🧩 How to Run

```bash
git clone https://github.com/yourusername/minishell.git
cd minishell
make
./minishell
```
---

## Example usage
```bash
minishell$ echo hello | grep h > output.txt
minishell$ cat output.txt
hello
```
Press Ctrl+D or type exit to quit the shell.
---
🧠 Notes

-Written in C (C99 standard)

-Uses fork(), execve(), dup2(), and pipe() system calls

-All memory leaks checked with Valgrind

-No external libraries other than standard libc and readline 
