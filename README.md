# Website Status Checker (Rust)

## Overview
This is a rust-based command-line tool that checks the availability and performance of multiple websites concurrently. It uses a fixed-size thread pool and the 'reqwest' HTTP client to issue status checks in parallel. 


## Build Instructions

In order to build the project in release mode, run the following command:
```bash
cd my_project
cargo build --release
```


## Usage Examples
If there is no websites in a file named sites.txt, place a url in each line. Once doing so, you will type either one of the following command in the terminal to run the program:
``` 
cargo run
cargo run -- --threads 6 --timeout 8 --retries=2 --interval=45 --cycle=4
```
You may change the numbers in the command if you wish to do so. 


## Bonus Features
- Flexible Command-Line Arguments – Adjust threads, timeouts, retries, and cycle timing without modifying the code.
- Custom Thread Pool – Efficiently fetches data in parallel using Rust's standard threads and channels.
- Retry System – Automatically retries failed requests up to a configurable number of times.
- Interval Scheduling – Repeats fetching tasks at fixed intervals, with optional limits on how many times to repeat.
- Graceful Exit with --cycle – Allows users to stop the program after a specific number of cycles.
- Manual Argument Parsing – Uses std::env::args() for lightweight command-line interface control, avoiding extra dependencies.
