# Rust command-line to-do tracker

The application is a command-line to-do tracker. 
It records our tasks into a text file, displays them as a list in the terminal, and lets us mark them complete.


The program interface will handle these three actions:
- Add new tasks to a to-do list.
- Remove completed tasks from that list.
- Print all the current tasks in the list.


## Run
Clone the repo : `git clone https://github.com/Th3M4r10/command-line-To-Do-tracker.git`

`cd command-line-To-Do-tracker/rusty-journal`

`cargo build`



## Options

```bash
$ target/debug/rusty-journal -h
Rusty Journal 0.1.0
A command line to-do app written in Rust

USAGE:
    rusty-journal.exe [OPTIONS] <SUBCOMMAND>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -j, --journal-file <journal-file>    Use a different journal file

SUBCOMMANDS:
    add     Write tasks to the journal file
    done    Remove an entry from the journal file by position
    help    Prints this message or the help of the given subcommand(s)
    list    List all tasks in the journal file

```


## Usage
```
cargo run -- -j test-journal.json add "Murali : Hii"

cargo run -- -j test-journal.json add "M4r10 : Hello"

cargo run -- -j test-journal.json add "Murali : What's your name ?"

cargo run -- -j test-journal.json add "M4r10 : This is M4r10, You ?"

cargo run -- -j test-journal.json add "Murali : I'm Murali, Nice to meet you :)"                      
```


```bash
$ cargo run -- -j test-journal.json list  
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.05s
     Running `target\debug\rusty-journal.exe -j test-journal.json list`
1: Murali : Hi                                        [2024-06-23 19:23]
2: M4r10 : Hello                                      [2024-06-23 19:23]
3: Murali : What's your name ?                        [2024-06-23 19:24]
4: M4r10 : This is M4r10, You ?                       [2024-06-23 19:25]
5: Murali : I'm Murali, Nice to meet you :)           [2024-06-23 19:26]

```


```bash
$ cargo run -- -j test-journal.json done 5                                       
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.08s
     Running `target\debug\rusty-journal.exe -j test-journal.json done 5`
     
$ cargo run -- -j test-journal.json list  
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.05s
     Running `target\debug\rusty-journal.exe -j test-journal.json list`
1: Murali : Hi                                        [2024-06-23 19:23]
2: M4r10 : Hello                                      [2024-06-23 19:23]
3: Murali : What's your name ?                        [2024-06-23 19:24]
4: M4r10 : This is M4r10, You ?                       [2024-06-23 19:25]
```