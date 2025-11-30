# 🐚 Simple Shell in Go

A minimal command-line shell implemented in **Go**, supporting built-in commands like  
`cd` and `exit`, along with execution of any system commands.

---

## 📌 Features

- Run any system command (`ls`, `pwd`, `cat`, etc.)
- Built-in commands:
  - `cd <path>` — change directory
  - `exit` — quit the shell
- REPL-style interface:
  ```
  > 
  ```
- Simple, clean, and beginner-friendly Go code

---

## 📁 Project Structure

```
.
└── main.go
```

---

## ▶️ How to Run

Make sure Go (1.18+) is installed.

### Clone the repository
```bash
git clone https://github.com/Kaileshwar16/Simple-shell.git
cd Simple-shell
```

### Run the shell
```bash
go run main.go
```

You will see a prompt:

```
>
```

Now you can run commands like:

```
> ls
> pwd
> cd /tmp
> echo hello world
> exit
```

---

## 🧠 How It Works (Quick Overview)

- Reads input using `bufio.Reader`
- Splits the line by spaces to get command & args
- Handles built-ins:
  - `cd` uses `os.Chdir`
  - `exit` uses `os.Exit(0)`
- All other commands are run using:
  ```go
  cmd := exec.Command(args[0], args[1:]...)
  cmd.Run()
  ```

---



