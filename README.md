# XSS Scanner Tool (Beta Version)

**XSS Scanner Tool** is a powerful tool built in Java using Selenium to help bug bounty hunters and penetration testers detect XSS vulnerabilities on target websites. The tool supports multi-threading, cookie management, custom payloads, and more. It is available as an executable JAR and requires Java to run.

## Requirements

- **Java JDK 22** (Set the `JAVA_HOME` path in environment variables)
- **Selenium WebDriver**
- **ChromeDriver** (Download and set the path in `C:\Drivers\chromedriver.exe`)
- Compatible with **Windows and Kali Linux**

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

### 2. ChromeDriver Setup

You must have ChromeDriver installed and placed in `C:\Drivers\chromedriver.exe`.

- **Download ChromeDriver**: [Download Link](https://drive.google.com/drive/folders/1iky5txX0ZqsXQyla2hekqDihmChaR3Ch?usp=drive_link)
- Place the downloaded file in `C:\Drivers\chromedriver.exe`.

### 3. Running the XSS Scanner Tool

Once Java and ChromeDriver are set up, you can run the XSS scanner.

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
