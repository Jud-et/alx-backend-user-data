# Personal Data Privacy Handler 🛡️

A robust Python application for handling sensitive personal information with enterprise-grade security measures.

## Description 📝

This project implements secure handling of Personally Identifiable Information (PII) through logging filters, database encryption, and password management. Perfect for those who like their data like their coffee - filtered and strong! ☕

## Features 🌟

- PII field obfuscation with regex magic ✨
- Custom log formatting with redaction capabilities 🎭
- Secure database connections (because we're not animals) 🔒
- Password hashing that would make quantum computers sweat 💪
- Validation system pickier than a toddler at dinner time 🔍

## Installation 🚀

```bash
# Clone with caution
git clone https://github.com/yourusername/personal-data-handler.git

# Install dependencies (they're needier than a cat)
pip install -r requirements.txt
```

## Usage 💡

```python
# Example: Filter sensitive data (like your browser history)
from filtered_logger import filter_datum

result = filter_datum(["password"], "***", "password=secret123", ";")
# Output: password=***
```


## Project Tasks 📋

1. **Regex-ing - Field Obfuscation** 🔒
   - Implements `filter_datum` function to redact sensitive fields
   - Uses regex pattern matching for field replacement
   - Handles dynamic field lists and custom separators
   - Perfect for sanitizing log messages without breaking their structure

2. **Log Formatter - Custom Redaction** 📝
   - Creates `RedactingFormatter` class extending logging.Formatter
   - Automatically filters sensitive data in log records
   - Maintains consistent log format while protecting PII
   - Supports multiple field redaction in a single pass

3. **Secure Logger Creation** 🎯
   - Implements `get_logger` function returning logging.Logger
   - Configures logger with proper PII field protection
   - Sets up StreamHandler with custom formatter
   - Defines PII_FIELDS tuple for standardized field protection

4. **Database Connection Handler** 🔌
   - Creates secure MySQL database connection
   - Implements environment variable configuration
   - Handles connection parameters securely
   - Provides fallback defaults for critical parameters

5. **Data Reading & Filtering** 👀
   - Implements main function for data retrieval
   - Automatically filters PII from database records
   - Formats output with proper field separation
   - Handles database connections and cursors safely

6. **Password Encryption** 🔐
   - Implements `hash_password` function using bcrypt
   - Generates secure salt for each password
   - Returns bytes-type hashed password
   - Ensures one-way encryption for security

7. **Password Validation** ✅
   - Implements `is_valid` function for password verification
   - Safely compares hashed passwords with provided passwords
   - Handles byte-string conversions automatically
   - Returns boolean for simple validation logic

## Environment Variables 🌍

```bash
PERSONAL_DATA_DB_USERNAME=root
PERSONAL_DATA_DB_PASSWORD=your_password
PERSONAL_DATA_DB_HOST=localhost
PERSONAL_DATA_DB_NAME=your_db_name
```

## Requirements 📦

- Python 3.7+
- MySQL 5.7+
- bcrypt
- mysqlclient
- A sense of security (and humor)

## Author ‍💻
Judith  - Because someone has to take responsibility for this security masterpiece!

## License 📜

MIT - Feel free to copy, just don't blame me if something goes wrong! 😉

## Acknowledgments 🙏

- Coffee ☕
- Stack Overflow, documentation and AI tools  (my true mentor)
- The person who invented regex (we have a love/hate relationship)

Remember: With great power comes great responsibility... and the need for proper data handling! 🦸‍♂️
