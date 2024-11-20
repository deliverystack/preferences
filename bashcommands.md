https://chatgpt.com/share/673d2b49-a9e8-8005-8018-a56fa540191c

| Command | Example | Description | Installation |
| ------- | ------- | ----------- | ------------ |
| **[alias](https://www.gnu.org/software/bash/manual/bash.html#index-alias)** | `alias ll='ls -l'` | Define or display aliases for commands | `N/A` |
| **[bg](https://www.gnu.org/software/bash/manual/bash.html#index-bg)** | `bg %1` | Resume a job in the background | `N/A` |
| **[bind](https://www.gnu.org/software/bash/manual/bash.html#index-bind)** | `bind -P` | Display or modify key bindings and readline settings | `N/A` |
| **[break](https://www.gnu.org/software/bash/manual/bash.html#index-break)** | `for i in {1..5}; do if [[ $i -eq 3 ]]; then break; fi; done` | Exit from a loop | `N/A` |
| **[builtin](https://www.gnu.org/software/bash/manual/bash.html#index-builtin)** | `builtin echo 'Hello, World!'` | Run a shell builtin, bypassing functions and aliases | `N/A` |
| **[caller](https://www.gnu.org/software/bash/manual/bash.html#index-caller)** | `caller` | Return the context of the current subroutine call | `N/A` |
| **[cd](https://www.gnu.org/software/bash/manual/bash.html#index-cd)** | `cd /path/to/directory` | Change the shell working directory | `N/A` |
| **[command](https://www.gnu.org/software/bash/manual/bash.html#index-command)** | `command ls` | Run a command, bypassing functions and aliases | `N/A` |
| **[compgen](https://www.gnu.org/software/bash/manual/bash.html#index-compgen)** | `compgen -c` | Generate possible completions for a word | `N/A` |
| **[complete](https://www.gnu.org/software/bash/manual/bash.html#index-complete)** | `complete -W 'start stop restart' mycommand` | Specify how arguments are completed for a command | `N/A` |
| **[continue](https://www.gnu.org/software/bash/manual/bash.html#index-continue)** | `for i in {1..5}; do if [[ $i -eq 3 ]]; then continue; fi; echo $i; done` | Resume the next iteration of a loop | `N/A` |
| **[declare](https://www.gnu.org/software/bash/manual/bash.html#index-declare)** | `declare -i number=5` | Declare variables and give them attributes | `N/A` |
| **[dirs](https://www.gnu.org/software/bash/manual/bash.html#index-dirs)** | `dirs -v` | Display the list of remembered directories | `N/A` |
| **[disown](https://www.gnu.org/software/bash/manual/bash.html#index-disown)** | `disown %1` | Remove a job from the shell's job table | `N/A` |
| **[do](https://www.gnu.org/software/bash/manual/bash.html#index-do)** | `for i in {1..3}; do echo $i; done` | Start a block of commands in a loop | `N/A` |
| **[echo](https://www.gnu.org/software/bash/manual/bash.html#index-echo)** | `echo 'Hello, World!'` | Print arguments to the standard output | `N/A` |
| **[enable](https://www.gnu.org/software/bash/manual/bash.html#index-enable)** | `enable -n echo` | Enable or disable shell builtins | `N/A` |
| **[eval](https://www.gnu.org/software/bash/manual/bash.html#index-eval)** | `eval "echo Hello, World"` | Evaluate and execute arguments as a command | `N/A` |
| **[exec](https://www.gnu.org/software/bash/manual/bash.html#index-exec)** | `exec ls -l` | Replace the shell with the specified command | `N/A` |
| **[export](https://www.gnu.org/software/bash/manual/bash.html#index-export)** | `export PATH=$PATH:/new/path` | Set an environment variable | `N/A` |
| **[fc](https://www.gnu.org/software/bash/manual/bash.html#index-fc)** | `fc -l -10` | List, edit, or re-execute commands from the shell's history | `N/A` |
| **[file](https://man7.org/linux/man-pages/man1/file.1.html)** | `file example.txt` | Determine the type of a file | `N/A` |
| **[for](https://www.gnu.org/software/bash/manual/bash.html#index-for)** | `for i in 1 2 3; do echo $i; done` | Iterate over a sequence of items | `N/A` |
| **[function](https://www.gnu.org/software/bash/manual/bash.html#index-function)** | `function greet() { echo Hello; }` | Define a function in the shell | `N/A` |
| **[getopts](https://www.gnu.org/software/bash/manual/bash.html#index-getopts)** | `while getopts 'a:b:' opt; do echo $opt; done` | Parse positional parameters | `N/A` |
| **[help](https://www.gnu.org/software/bash/manual/bash.html#index-help)** | `help cd` | Display information about built-in commands | `N/A` |
| **[history](https://www.gnu.org/software/bash/manual/bash.html#index-history)** | `history 10` | Display or manipulate the command history | `N/A` |
| **[if](https://www.gnu.org/software/bash/manual/bash.html#index-if)** | `if [[ -f file.txt ]]; then echo "File exists"; fi` | Execute commands conditionally | `N/A` |
| **[jobs](https://www.gnu.org/software/bash/manual/bash.html#index-jobs)** | `jobs -l` | List active jobs | `N/A` |
| **[kill](https://www.gnu.org/software/bash/manual/bash.html#index-kill)** | `kill -9 1234` | Terminate a process by sending a signal | `N/A` |
| **[let](https://www.gnu.org/software/bash/manual/bash.html#index-let)** | `let x=5+3` | Perform arithmetic operations | `N/A` |
| **[local](https://www.gnu.org/software/bash/manual/bash.html#index-local)** | `local name='John'` | Define a local variable within a function | `N/A` |
| **[logout](https://www.gnu.org/software/bash/manual/bash.html#index-logout)** | `logout` | Exit a login shell | `N/A` |
| **[popd](https://www.gnu.org/software/bash/manual/bash.html#index-popd)** | `popd` | Remove the top entry from the directory stack and change to the new top directory | `N/A` |
| **[printf](https://www.gnu.org/software/bash/manual/bash.html#index-printf)** | `printf "Hello, %s\n" World` | Format and print data | `N/A` |
| **[pushd](https://www.gnu.org/software/bash/manual/bash.html#index-pushd)** | `pushd /path/to/directory` | Add a directory to the directory stack and change to it | `N/A` |
| **[readline](https://www.gnu.org/software/bash/manual/bash.html#index-readline)** | `Ctrl-r to search history interactively` | Provides command-line editing and history capabilities | `N/A` |
| **[readonly](https://www.gnu.org/software/bash/manual/bash.html#index-readonly)** | `readonly name='John'` | Mark variables or functions as read-only | `N/A` |
| **[return](https://www.gnu.org/software/bash/manual/bash.html#index-return)** | `return 0` | Exit a shell function and return a value | `N/A` |
| **[select](https://www.gnu.org/software/bash/manual/bash.html#index-select)** | `select option in Start Stop Quit; do echo $option; break; done` | Prompt the user to select from a list of options | `N/A` |
| **[set](https://www.gnu.org/software/bash/manual/bash.html#index-set)** | `set -x` | Set or unset shell options and positional parameters | `N/A` |
| **[shift](https://www.gnu.org/software/bash/manual/bash.html#index-shift)** | `shift 2` | Shift positional parameters to the left | `N/A` |
| **[shopt](https://www.gnu.org/software/bash/manual/bash.html#index-shopt)** | `shopt -s globstar` | Enable or disable shell options | `N/A` |
| **[source](https://www.gnu.org/software/bash/manual/bash.html#index-source)** | `source ~/.bashrc` | Execute commands from a file in the current shell | `N/A` |
| **[test](https://www.gnu.org/software/bash/manual/bash.html#index-test)** | `test -f file.txt && echo 'File exists'` | Evaluate a conditional expression | `N/A` |
| **[time](https://www.gnu.org/software/bash/manual/bash.html#index-time)** | `time ls` | Measure the time a command takes to execute | `N/A` |
| **[times](https://www.gnu.org/software/bash/manual/bash.html#index-times)** | `times` | Display accumulated user and system times for processes | `N/A` |
| **[trap](https://www.gnu.org/software/bash/manual/bash.html#index-trap)** | `trap 'echo Interrupted' SIGINT` | Execute a command when a signal is received | `N/A` |
| **[type](https://www.gnu.org/software/bash/manual/bash.html#index-type)** | `type ls` | Display information about a command type | `N/A` |
| **[ulimit](https://www.gnu.org/software/bash/manual/bash.html#index-ulimit)** | `ulimit -n 1024` | Set or display user resource limits | `N/A` |
| **[umask](https://www.gnu.org/software/bash/manual/bash.html#index-umask)** | `umask 022` | Set the default file permissions mask | `N/A` |
| **[unalias](https://www.gnu.org/software/bash/manual/bash.html#index-unalias)** | `unalias ll` | Remove aliases | `N/A` |
| **[unset](https://www.gnu.org/software/bash/manual/bash.html#index-unset)** | `unset name` | Unset a variable or function | `N/A` |
| **[until](https://www.gnu.org/software/bash/manual/bash.html#index-until)** | `until [[ $count -ge 5 ]]; do echo $count; ((count++)); done` | Loop until a condition becomes true | `N/A` |
| **[wait](https://www.gnu.org/software/bash/manual/bash.html#index-wait)** | `wait $!` | Wait for a background process to finish | `N/A` |
| **[while](https://www.gnu.org/software/bash/manual/bash.html#index-while)** | `while [[ $count -lt 5 ]]; do echo $count; ((count++)); done` | Loop as long as a condition is true | `N/A` |
| **[7z](https://www.7-zip.org/)** | `7z x archive.7z` | A file archiver with high compression ratios | `sudo apt install p7zip-full` |
| **[batcat](https://github.com/sharkdp/bat)** | `batcat file.txt` | A clone of `cat` with syntax highlighting and Git integration | `sudo apt install bat` |
| **[cargo](https://doc.rust-lang.org/cargo/)** | `cargo build` | Rust's package manager and build system | `Included with rustup installation.` |
| **[dos2unix](https://man7.org/linux/man-pages/man1/dos2unix.1.html)** | `dos2unix file.txt` | Convert DOS line endings to Unix line endings | `sudo apt install dos2unix` |
| **[exiftool](https://exiftool.org/)** | `exiftool image.jpg` | Tool for reading, writing, and editing image metadata | `sudo apt install libimage-exiftool-perl` |
| **[eyeD3](https://eyed3.readthedocs.io/)** | `eyeD3 --title 'Song Title' file.mp3` | A Python tool for managing ID3 tags in MP3 files | `sudo apt install eyed3` |
| **[ffmpeg](https://ffmpeg.org/)** | `ffmpeg -i input.mp3 output.flac` | A tool for processing multimedia files (audio and video) | `sudo apt install ffmpeg` |
| **[fx](https://github.com/antonmedv/fx)** | `echo '{"key":"value"}' | fx .key` | A command-line JSON processing tool | `npm install -g fx` |
| **[gcc](https://gcc.gnu.org/)** | `gcc program.c -o program` | The GNU Compiler Collection for C, C++, and other languages | `sudo apt install gcc` |
| **[gimp](https://www.gimp.org/)** | `gimp` | GNU Image Manipulation Program for editing and creating images | `sudo apt install gimp` |
| **[go](https://golang.org/)** | `go run main.go` | A statically typed programming language for building fast and reliable software | `sudo apt install golang-go` |
| **[id3v2](https://man7.org/linux/man-pages/man1/id3v2.1.html)** | `id3v2 --song 'Song Title' file.mp3` | Tool for editing ID3v2 tags in MP3 files | `sudo apt install id3v2` |
| **[imagemagick](https://imagemagick.org/)** | `convert input.png output.jpg` | A suite of tools for creating, editing, and converting images | `sudo apt install imagemagick` |
| **[lame](https://lame.sourceforge.io/)** | `lame input.wav output.mp3` | A high-quality MP3 encoder | `sudo apt install lame` |
| **[libmp3lame-dev](https://lame.sourceforge.io/)** | `ffmpeg -i input.wav -codec:a libmp3lame output.mp3` | Development files for the LAME MP3 encoder | `sudo apt install libmp3lame-dev` |
| **[locales](https://man7.org/linux/man-pages/man1/locale.1.html)** | `locale` | Set and configure system language and locale information | `sudo apt install locales` |
| **[metaflac](https://xiph.org/flac/documentation_tools_metaflac.html)** | `metaflac --set-tag='TITLE=Song Name' file.flac` | FLAC metadata editor to add, edit, or remove tags | `sudo apt install flac` |
| **[ngrok](https://ngrok.com/)** | `ngrok http 8080` | Expose local servers to the internet securely | `curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc && echo "deb https://ngrok-agent.s3.amazonaws.com stable main" \| sudo tee /etc/apt/sources.list.d/ngrok.list && sudo apt update && sudo apt install ngrok` |
| **[node.js](https://nodejs.org/)** | `node script.js` | JavaScript runtime built on Chrome's V8 JavaScript engine | `sudo apt install nodejs` |
| **[npm](https://www.npmjs.com/)** | `npm install -g package` | The Node | `sudo apt install npm` |
| **[nvm](https://github.com/nvm-sh/nvm)** | `nvm install 16` | Node Version Manager, to manage Node | `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh \| bash` |
| **[rust](https://www.rust-lang.org/)** | `rustc main.rs` | A systems programming language for performance and safety | `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs \| sh` |
| **[rustup](https://rust-lang.github.io/rustup/)** | `rustup update` | The Rust toolchain installer and version manager | `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs \| sh` |
| **[sox](http://sox.sourceforge.net/)** | `sox input.mp3 output.wav` | A command-line utility for audio file processing, including MP3s | `sudo apt install sox` |
| **[tmux](https://github.com/tmux/tmux)** | `tmux new -s session_name` | Terminal multiplexer to manage multiple terminal sessions | `sudo apt install tmux` |
| **[typescript](https://www.typescriptlang.org/)** | `tsc file.ts` | A superset of JavaScript that compiles to plain JavaScript | `npm install -g typescript` |
| **[unrar](https://man7.org/linux/man-pages/man1/unrar.1.html)** | `unrar x archive.rar` | Extract  | `sudo apt install unrar` |
| **[unzip](https://man7.org/linux/man-pages/man1/unzip.1.html)** | `unzip archive.zip` | Extract compressed  | `sudo apt install unzip` |


# Comprehensive Best Practices for Linux/Bash/Bourne Shell Scripting

## 1. General Best Practices

### 1.1. Use ShellCheck
- Use [ShellCheck](https://www.shellcheck.net/) to lint your scripts. It provides static analysis to catch common errors, security vulnerabilities, and style issues.

### 1.2. Always Specify the Shell
- Include a shebang (`#!/bin/bash` or `#!/bin/sh`) at the top of your script to explicitly define the shell.
```bash
#!/bin/bash
```

### 1.3. Write Portable Scripts
- Use POSIX-compliant syntax unless targeting Bash-specific features.
- Test scripts with `sh` and `dash` for portability when feasible.

### 1.4. Use Readable Formatting
- Use four spaces per indentation level for readability.
- Avoid tabs unless required for compatibility.

### 1.5. Comment Judiciously
- Provide comments for complex logic, unusual behavior, and configuration sections.
- Use comments to explain **why** something is done, not **what** is done (the code should explain that).

---

## 2. Error Handling

### 2.1. Use `set` Options for Safety
- At the start of the script, use the following `set` options for error handling:
```bash
set -euo pipefail
```
  - `-e`: Exit immediately on errors.
  - `-u`: Treat unset variables as an error and exit.
  - `-o pipefail`: Prevent masking errors in pipelines.

### 2.2. Check Return Codes
- Explicitly check the return status of critical commands:
```bash
if ! command; then
    echo "Command failed!" >&2
    exit 1
fi
```

### 2.3. Trap Signals
- Use `trap` to handle signals like `SIGINT` and clean up temporary resources:
```bash
trap 'rm -f /tmp/tempfile; exit' INT TERM EXIT
```

### 2.4. Validate Inputs
- Check for mandatory parameters and validate user input:
```bash
if [ -z "$1" ]; then
    echo "Usage: $0 <arg>" >&2
    exit 1
fi
```

---

## 3. Code Structure

### 3.1. Modularize Code
- Break the script into functions for better readability and reuse:
```bash
my_function() {
    # Function logic here
}

main() {
    my_function
}

main "$@"
```

### 3.2. Use Meaningful Names
- Use descriptive variable and function names:
```bash
source_dir="/path/to/source"
target_dir="/path/to/target"
```

### 3.3. Use Libraries for Reusable Functions
- Group reusable functions into a shared library and source them:
```bash
source "$HOME/lib/utils.sh"
```

### 3.4. Maintain a Standard Script Header
- Include metadata for clarity:
```bash
#!/bin/bash
# Script Name: myscript.sh
# Description: Brief explanation of the script
# Author: Your Name
# Date: YYYY-MM-DD
# Version: 1.0
```

---

## 4. Input and Output

### 4.1. Use `read` for User Input
- Securely read user input:
```bash
read -rp "Enter your name: " name
```

### 4.2. Use Meaningful Prompts
- Provide clear, concise messages.

### 4.3. Redirect Output
- Redirect logs and errors to files:
```bash
./myscript.sh > output.log 2> error.log
```

### 4.4. Use `printf` Over `echo`
- Use `printf` for formatted output:
```bash
printf "Processing file: %s
" "$file"
```

---

## 5. Variables

### 5.1. Use Lowercase for Variables
- Use lowercase for script variables and uppercase for environment variables:
```bash
source_dir="/path/to/source"
```

### 5.2. Quote Variables
- Always quote variables to avoid word splitting and globbing issues:
```bash
echo "Path: $source_dir"
```

### 5.3. Use Read-Only Variables
- Protect critical variables:
```bash
readonly config_file="/etc/myapp/config"
```

---

## 6. Security Practices

### 6.1. Avoid Using Hardcoded Secrets
- Use environment variables or configuration files for sensitive data.

### 6.2. Sanitize Input
- Validate user input to prevent injection attacks:
```bash
if [[ "$input" =~ [^a-zA-Z0-9] ]]; then
    echo "Invalid input" >&2
    exit 1
fi
```

### 6.3. Handle Files Securely
- Use `mktemp` for temporary files:
```bash
temp_file=$(mktemp) || exit 1
```

---

## 7. Debugging and Logging

### 7.1. Use Verbose Logging
- Provide options for verbose output:
```bash
verbose=false
while getopts "v" opt; do
    case $opt in
        v) verbose=true ;;
    esac
done

$verbose && echo "Verbose mode enabled"
```

### 7.2. Log with Timestamps
- Include timestamps in logs:
```bash
echo "$(date '+%Y-%m-%d %H:%M:%S') - Message"
```

---

## 8. File and Directory Handling

### 8.1. Test for Existence
- Check if files or directories exist before acting:
```bash
if [ ! -f "$file" ]; then
    echo "File not found: $file" >&2
    exit 1
fi
```

### 8.2. Use `find` and `globstar`
- Use `shopt -s globstar` for recursive globbing in Bash:
```bash
shopt -s globstar
for file in **/*.txt; do
    echo "$file"
done
```

---

## 9. Performance Optimization

### 9.1. Use Built-In Commands
- Prefer built-in commands over external ones (e.g., `[[ ]]` over `test`).

### 9.2. Avoid Forking Subprocesses
- Replace `$(command)` with built-ins where possible.

### 9.3. Optimize Loops
- Avoid reading large files line-by-line in Bash. Use `awk` or `sed`.

---

## 10. Testing and Maintenance

### 10.1. Automate Tests
- Create test cases for your scripts using a framework like [bats](https://github.com/bats-core/bats-core).

### 10.2. Use Version Control
- Store scripts in a Git repository for versioning.

### 10.3. Document Script Usage
- Include a `--help` flag:
```bash
usage() {
    echo "Usage: $0 [options]"
    echo "Options:"
    echo "  -h    Show help"
}

while getopts "h" opt; do
    case $opt in
        h) usage; exit ;;
    esac
done
```

By adhering to these best practices, you can write efficient, maintainable, and secure shell scripts for Linux environments.
