# 🔐 Password Strength Validator

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A comprehensive password strength validation tool that combines an intuitive graphical interface with a powerful command-line utility. Built with advanced security algorithms to help users create and evaluate robust passwords for maximum protection.

## 🌟 Key Features

### 🎯 **Dual Interface Options**
- **GUI Mode**: User-friendly graphical interface with real-time feedback
- **CLI Mode**: Efficient command-line tool for developers and power users

### 🔍 **Advanced Security Analysis**
- **Smart Algorithm**: Powered by the industry-standard `zxcvbn` library for realistic password strength assessment
- **Pattern Detection**: Identifies common password patterns, keyboard walks, and dictionary words
- **Breach Detection**: Cross-references against known compromised password databases

### 🛡️ **Comprehensive Validation**
- ✅ Minimum length enforcement (12+ characters recommended)
- ✅ Character diversity analysis (uppercase, lowercase, numbers, symbols)
- ✅ Common weak password detection
- ✅ Banned password screening from data breaches
- ✅ Real-time strength scoring (0-4 scale)

### 🎲 **Secure Password Generation**
- Cryptographically secure random password creation
- Customizable length settings (8-128 characters)
- Balanced character distribution for maximum entropy

### 📊 **Reporting & Analytics**
- JSON export functionality for audit trails
- Detailed strength analysis reports
- Actionable improvement recommendations
- Comprehensive activity logging

## 🚀 Quick Start

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/DivyamAggarwal/password_strength_checker.git
   cd password_strength_checker
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or install manually:
   ```bash
   pip install zxcvbn
   ```

3. **Prepare wordlist files:**
   Ensure these files are in your project directory:
   ```
   📁 project-root/
   ├── weak_passwords.txt      # Common weak passwords
   ├── banned_passwords.txt    # Breached passwords database
   └── password_strength_validator.py
   ```

## 💻 Usage

### 🖥️ GUI Mode

Launch the graphical interface:

```bash
python password_strength_validator.py
```

**GUI Features:**
- Real-time password strength visualization
- One-click secure password generation
- Copy passwords to clipboard
- Export analysis results as JSON
- Interactive security tips and feedback

### ⌨️ CLI Mode

**Interactive CLI:**
```bash
python password_strength_validator.py --cli
```

**Direct Commands:**
```bash
# Check password strength
python password_strength_validator.py --check "YourPassword123!"

# Generate secure password (default: 16 chars)
python password_strength_validator.py --generate

# Generate custom length password
python password_strength_validator.py --generate --length 24
```

### 📋 Command Reference

| Command | Description | Example |
|---------|-------------|---------|
| `--cli` | Launch interactive CLI mode | `python validator.py --cli` |
| `--check PASSWORD` | Evaluate specific password | `python validator.py --check "mypass"` |
| `--generate` | Generate secure password | `python validator.py --generate` |
| `--length N` | Set password length (8-128) | `python validator.py --generate --length 20` |

## 🔧 Configuration

### Password Strength Criteria

| Criterion | Requirement | Impact |
|-----------|-------------|---------|
| **Minimum Length** | 12+ characters | High |
| **Character Types** | 3+ categories (upper, lower, numbers, symbols) | High |
| **Dictionary Words** | Avoid common words | Medium |
| **Patterns** | No keyboard walks or sequences | Medium |
| **Breach Database** | Not in known breaches | Critical |

### Strength Scoring

| Score | Level | Description |
|-------|-------|-------------|
| 0 | Very Weak | Easily guessable |
| 1 | Weak | Basic password |
| 2 | Fair | Moderate security |
| 3 | Good | Strong password |
| 4 | Excellent | Very strong password |

## 📁 Project Structure

```
password-strength-validator/
├── 📄 README.md
├── 📄 LICENSE
├── 📄 requirements.txt
├── 🐍 password_strength_validator.py
├── 📄 weak_passwords.txt
├── 📄 banned_passwords.txt

```

## 📊 Logging & Monitoring

All validation activities are automatically logged to:
```
./password_checker.log
```

**Log entries include:**
- 🕐 Timestamp
- 🔧 Operation type (check/generate)
- 📈 Strength score
- ⚠️ Security warnings
- 💡 Improvement suggestions

## 🛡️ Security Features

### Privacy Protection
- ✅ **Local Processing**: All operations performed locally, no network calls
- ✅ **Memory Safety**: Passwords not stored in memory longer than necessary
- ✅ **No Data Persistence**: Sensitive data cleared after analysis

### Cryptographic Security
- ✅ **Secure Random**: Uses `secrets` module for cryptographically secure randomness
- ✅ **Entropy Analysis**: Measures true password complexity
- ✅ **Pattern Recognition**: Detects subtle security weaknesses

## 🔄 API Reference

### Core Functions

```python
from password_strength_validator import PasswordValidator

validator = PasswordValidator()

# Check password strength
result = validator.check_password("MyPassword123!")
print(f"Strength: {result.score}/4")
print(f"Feedback: {result.feedback}")

# Generate secure password
secure_password = validator.generate_password(length=16)
print(f"Generated: {secure_password}")
```

## 🧪 Testing

Run the test suite:
```bash
python -m pytest tests/
```

Test coverage:
```bash
python -m pytest --cov=password_strength_validator tests/
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make changes and add tests
4. Run tests: `pytest`
5. Commit changes: `git commit -am 'Add feature'`
6. Push to branch: `git push origin feature-name`
7. Submit a Pull Request

## 📋 Roadmap

### Upcoming Features
- [ ] **Web Interface**: Browser-based password checker
- [ ] **API Endpoint**: RESTful API for integration
- [ ] **Multi-language**: Support for international character sets
- [ ] **Password Manager**: Integration with popular password managers
- [ ] **Enterprise Features**: Bulk password analysis and policy enforcement

## 🐛 Troubleshooting

### Common Issues

**Issue: `ModuleNotFoundError: No module named 'zxcvbn'`**
```bash
# Solution:
pip install zxcvbn
```

**Issue: Wordlist files not found**
```bash
# Ensure files are in the correct location:
ls -la weak_passwords.txt banned_passwords.txt
```

**Issue: GUI doesn't start on Linux**
```bash
# Install tkinter:
sudo apt-get install python3-tk
```

## 📈 Performance

- **Analysis Speed**: < 100ms per password
- **Memory Usage**: < 50MB typical
- **File Size**: Wordlists ~10MB combined
- **Supported Length**: 1-128 characters

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



---
