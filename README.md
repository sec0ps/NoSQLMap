# NoSQLMap - Python 3

Python 3 compatible version of NoSQLMap, an automated NoSQL database enumeration and web application exploitation tool.

## About This Fork

This is a Python 3 port of the original [NoSQLMap](https://github.com/codingo/NoSQLMap) by the NoSQLMap Development Team. The original project was designed for Python 2, which reached end-of-life in 2020.

**Original Project**: NoSQLMap Copyright 2012-2017 NoSQLMap Development team  
**Python 3 Migration**: 2025

## What's Changed

- ✅ Full Python 3 compatibility (tested on Python 3.10+)
- ✅ Updated `print` statements to function syntax
- ✅ Converted `raw_input()` to `input()`
- ✅ Fixed bytes/string encoding for POST requests
- ✅ Updated `urllib2` to `urllib.request`
- ✅ Fixed dictionary iteration methods
- ✅ Corrected HTTP request body encoding

## Features

- **MongoDB** and **CouchDB** exploitation
- **NoSQL injection** testing for web applications (GET/POST)
- **Anonymous database access** scanning
- **User enumeration** and password hash extraction
- **Database cloning** capabilities
- **Timing-based injection** attacks
- **Burp Suite** request file import

## Requirements
```bash
pip install pymongo couchdb requests pbkdf2 gridfs
```

## Quick Start

### Interactive Mode
```bash
python nosqlmap.py
```

### Command Line Mode
```bash
# Test a web application
python nosqlmap.py \
  --attack 2 \
  --victim target.com \
  --webPort 443 \
  --uri /api/login \
  --https ON \
  --httpMethod POST \
  --postData "username,test,password,test123"

# Scan for anonymous MongoDB access
python nosqlmap.py --attack 3 --platform MongoDB
```

### Load Burp Request
1. Save a Burp Suite request to a file
2. Run NoSQLMap and select option 1 (Set options)
3. Select option 'a' (Load options from saved Burp request)
4. Provide the file path
5. Return to main menu and select option 3 (NoSQL Web App attacks)

## Usage Example
```bash
$ python nosqlmap.py

# Select option 1: Set options
# Select option a: Load Burp request file
# Select option 3: NoSQL Web App attacks
# Choose parameter to inject
# View results
```

## Security & Legal Notice

⚠️ **IMPORTANT**: This tool is for authorized security testing only.

- Only test systems you **own** or have **explicit written permission** to test
- Unauthorized access to computer systems is illegal
- Use responsibly and ethically
- The authors assume no liability for misuse

## Supported Platforms

- **Databases**: MongoDB, CouchDB
- **Languages**: PHP, Node.js/Express
- **Python**: 3.8+

## Known Limitations

- Some legacy features may have compatibility issues
- Metasploit integration requires MSF installed
- Network scanning requires appropriate permissions

## Contributing

Issues and pull requests welcome. Please maintain compatibility with Python 3.8+.

## License

See the file `doc/COPYING` for the original license terms. All original copyright notices have been preserved. This Python 3 port maintains the same license as the original project.

## Credits

**Original Authors**: NoSQLMap Development Team (2012-2017)  
**Original Repository**: https://github.com/codingo/NoSQLMap  
**Python 3 Port**: Keith Pachulski aka sec0ps (2025)

## Disclaimer

This tool is provided for educational and authorized testing purposes only. Users are responsible for complying with applicable laws and regulations.
