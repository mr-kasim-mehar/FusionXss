# XSS Scanner Tool (Stable)

**XSS Scanner Tool** is a powerful tool built in Java using Selenium to help bug bounty hunters and penetration testers detect XSS vulnerabilities on target websites. The tool supports multi-threading, cookie management, custom payloads, and more. It is available as an executable JAR and requires Java to run.

## Requirements

- **Java JDK 22** (Set the `JAVA_HOME` path in environment variables)
- **ChromeDriver** (Download and set the path in `C:\Drivers\chromedriver.exe`)
## Features

- **Multi-threading** support for faster scanning
- **Custom XSS Payloads** with a default payloads file
- **Cookie Injection** for testing authenticated sessions
- **Negative Results Logging** for tracking unsuccessful scans
- **Timeout Configuration** for delaying the execution
- **View Mode** to show or hide the browser during scanning
## NOTE:
- Right Now it will scan the only url which have one parameter only ------> https://example.com/search?q=hi

## Setup Instructions

### 1. Java Installation

Ensure that you have Java JDK 22 or later installed. Set up the environment variables to run the tool.

- **Download Java JDK**: [Download Link](https://www.oracle.com/java/technologies/javase/jdk22-archive-downloads.html)
- **Set JAVA_HOME Environment Variable**:
  1. Go to **System Properties**.
  2. Click on **Environment Variables**.
  3. Under **System Variables**, click on **New**.
  4. Add `JAVA_HOME` as the variable name and the path of your JDK folder as the value (e.g., `C:\Program Files\Java\jdk-22`).
  5. Edit the **Path** variable, and add C:\Program Files\Java\jdk-22\bin`.

### 2. ChromeDriver Setup 7 Google Chrome

- You must have ChromeDriver installed and placed in `C:\Drivers\chromedriver.exe`.
- Install the Latest Version of Google Chrome

- **Download ChromeDriver**: [Download Link](https://googlechromelabs.github.io/chrome-for-testing/)
- Install the Latest version of Chrome driver
- Place the downloaded file in `C:\Drivers\chromedriver.exe`.
  

#### Command-Line Arguments

The tool can be run with various command-line arguments for flexible scanning.

```bash
FusionXss.exe --url <url> [options]
```
```
FusionXss.exe --file urls.txt --threads 4 --timeout 2 --payloads Min_Payloads.txt
```
```
FusionXss.exe --file urls.txt --threads 4 --timeout 2 --payloads Min_Payloads.txt
```
```
FusionXss.exe --url https://example.com --cookies sessionId:abc123:/ --payloads customPayloads.txt
```


| Option                         | Description                                                         |
|--------------------------------|---------------------------------------------------------------------|
| `--url <url>`                  | Specify the target URL to scan.                                     |
| `--file <file>`                | File containing a list of URLs to test.                             |
| `--cookies <name:value:path>`  | Add cookies for authenticated sessions (format: name:value:path).   |
| `--payloads <payload file>`    | Use a custom payload file for scanning.                             |
| `--negative <true/false>`      | Log unsuccessful scans.                                             |
| `--timeout <seconds>`          | Set request timeout in seconds.                                     |
| `--threads <number>`           | Number of threads for concurrent scanning.                          |
| `--view <on/off>`              | Toggle browser visibility (default: off).                           |

![XSS Scanner](https://github.com/mr-kasim-mehar/myimgs/blob/main/Git.png)
