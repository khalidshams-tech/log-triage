# SSH Log Triage Script

A Bash script that reviews SSH authentication logs, extracts failed login attempts, and summarizes suspicious login activity by user and IP address.

## Project Description

Linux authentication logs can become long and difficult to review manually. This project provides a simple command-line script that helps an IT support or cybersecurity learner identify failed SSH login attempts and summarize repeated login failures.

The project is intentionally small, practical, and focused on defensive security basics: reading logs, filtering useful information, and producing a clearer report.

## Technologies Used

- Linux command line
- Bash scripting
- grep, awk, sort, uniq
- SSH authentication logs
- Git and GitHub

## Features

- Reads an SSH/authentication log file
- Finds failed password login attempts
- Saves matching failed-login lines to an output file
- Counts repeated failed attempts by `user@ip`
- Creates a summary report for quick review
- Includes sample logs for practice

## Project Structure

```text
log-triage/
+-- log-triage.sh
+-- README.md
+-- sample_logs/
+-- output/
+-- License
```

## Installation and Setup

1. Clone the repository:

```bash
git clone https://github.com/khalidshams-tech/log-triage.git
```

2. Open the project folder:

```bash
cd log-triage
```

3. Make the script executable:

```bash
chmod +x log-triage.sh
```

4. Run the script with the sample log:

```bash
./log-triage.sh
```

5. Run the script with a specific log file:

```bash
./log-triage.sh sample_logs/auth.log
```

## Example Output

The script creates files such as:

```text
output/ssh_failed.log
output/summary.txt
```

A summary line may look like:

```text
root@172.20.1.1  5 failed attempts
```

## Screenshots

Add screenshots here showing:

- Terminal command used to run the script
- Failed login output
- Summary report

Example:

```markdown
![Log triage terminal output](screenshots/log-triage-output.png)
```

## What I Learned

- How Linux authentication logs are structured
- How to use shell tools to filter and summarize text
- How repeated failed SSH logins can indicate suspicious activity
- How to create a small security-focused automation script
- How to document a command-line tool for portfolio use

## Future Improvements

- Add support for more log formats
- Add command-line options for input and output paths
- Add severity levels for repeated attempts
- Add sample screenshots and demo output
- Add tests using sample log files
- Add recommendations for next steps after suspicious login activity is found

## Status

Active cybersecurity/Linux portfolio project. This is one of my strongest career-aligned repos for IT support and security fundamentals.