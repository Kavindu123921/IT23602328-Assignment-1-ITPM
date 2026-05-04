# IT23602328 - Assignment 1 - ITPM

## Overview
This project contains automated test cases for evaluating the
transliteration accuracy of the Chat Sinhala function available at:
https://www.pixelssuite.com/chat-translator

## Prerequisites
- Python 3.x
- pip

## Installation

### 1. Clone the repository
```
git clone https://github.com/Kavindu123921/IT23602328-Assignment-1-ITPM.git
cd IT23602328-Assignment-1-ITPM
```

### 2. Install Python dependencies
```
pip install playwright openpyxl
```

### 3. Install Playwright browsers
```
playwright install chromium
```

## How to Run Tests

### Windows
```
python test_automation.py --url "https://www.pixelssuite.com/chat-translator" --input-col "Input" --expected-col "Expected output" --actual-col "Actual Output" --status-col "Status" --wait-ms 5000 --type-delay-ms 100 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Mac/Linux
```
python test_automation.py \
  --url "https://www.pixelssuite.com/chat-translator" \
  --input-col "Input" \
  --expected-col "Expected output" \
  --actual-col "Actual Output" \
  --status-col "Status" \
  --wait-ms 5000 \
  --type-delay-ms 100 \
  --slow-mo-ms 200 \
  --save-every 1 \
  --keep-open
```

## Command Line Arguments

| Argument | Default | Description |
|---|---|---|
| --url | pixelssuite URL | Target application URL |
| --input-col | Auto-detected | Column name for Singlish input |
| --expected-col | Auto-detected | Column name for expected Sinhala output |
| --actual-col | Auto-detected | Column name for actual output |
| --status-col | Auto-detected | Column name for test status |
| --wait-ms | 5000 | Wait time (ms) after transliteration |
| --type-delay-ms | 30 | Delay (ms) between keystrokes |
| --slow-mo-ms | 0 | Slow motion delay for browser actions |
| --save-every | 0 | Save Excel after every N test cases |
| --keep-open | False | Keep browser open after tests |
| --headless | False | Run browser without UI |
| --retries | 8 | Retry attempts for output reading |
| --excel | Auto-detected | Path to Excel test cases file |
| --sheet | Test cases | Excel sheet name |

## Test Results
Results are saved automatically to:
```
Assignment 1 - Test cases.xlsx
```
Each row will be updated with:
- **Actual output** from the tool
- **Status:** PASS / FAIL / COLLECTED / UI Error

## Project Structure
```
IT23602328-Assignment-1-ITPM/
├── test_automation.py
├── README.md
└── Assignment 1 - Test cases.xlsx
```
