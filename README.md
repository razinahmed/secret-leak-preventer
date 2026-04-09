# Secret Leak Preventer

![Security](https://img.shields.io/badge/Security-Tool-red)
![Bash](https://img.shields.io/badge/Bash-Script-green)
![Git](https://img.shields.io/badge/Git-Hooks-orange)
![License](https://img.shields.io/badge/License-MIT-blue)

A pre-commit security tool that prevents secrets, API keys, tokens, and credentials from being accidentally committed to Git repositories. Scans staged files for sensitive patterns before they reach your codebase.

## Description

Secret Leak Preventer integrates with your Git workflow to detect and block commits containing hardcoded secrets. It uses pattern matching to identify API keys, passwords, private keys, and other sensitive data before they are pushed to version control.

## Features

- Pre-commit hook integration for automatic scanning
- Detection of API keys, tokens, and credentials
- Pattern-based scanning for common secret formats
- Support for custom secret patterns and rules
- Lightweight with no external dependencies
- System hardening baseline included
- Makefile-based build and test workflow

## Tech Stack

- **Language:** Bash
- **Integration:** Git hooks (pre-commit)
- **Target OS:** Linux / macOS
- **Build Tool:** GNU Make

## Quick Start

```bash
# Clone the repository
git clone https://github.com/razinahmed/secret-leak-preventer.git
cd secret-leak-preventer

# Review the security script
cat scripts/security_core.sh

# Install the pre-commit hook in your target repo
cp scripts/security_core.sh /path/to/your/repo/.git/hooks/pre-commit
chmod +x /path/to/your/repo/.git/hooks/pre-commit
```

## Usage

```bash
# Build and test
make build
make test

# Run the scanner manually
bash scripts/security_core.sh
```

## Project Structure

```
secret-leak-preventer/
  scripts/
    security_core.sh  # Core secret detection script
  Makefile             # Build and test automation
  SECURITY.md          # Security policy
  LICENSE              # MIT License
```

## Contributing

Contributions are welcome. Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
