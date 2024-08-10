NYCU 2024spring 謝志仁教授 Cryptography Engineering

**⚠️ Warning: This project is for educational purposes only. Do not use it for illegal activities. Unauthorized use of this project may violate privacy laws and could result in legal consequences.**

# Project Summary

This project demonstrates a potential security vulnerability within Chrome extensions by creating a malicious extension that captures Facebook session cookies.

## Project Structure

- **hack.py**: Python script used to automate the process of acquiring and utilizing cookies.
- **chrome_test/**: Directory related to Chrome extension testing.
- **server.js**: JavaScript file responsible for receiving cookies and sending them via email.
- **package-lock.json**: Automatically generated file that describes the exact dependency tree.
- **package.json**: Contains project metadata, dependencies, and scripts.
- **node_modules/**: Directory containing project dependencies.


## How It Works

1. **hack.py**: 
   - Triggered when the user clicks a button in the Chrome extension.
   - Retrieves the user's Facebook cookies.
   - Sends the cookie values to the backend server.

2. **server.js**:
   - Collects cookie values.
   - Sends them to the attacker via email.

3. **Chrome Extension**:
   - Injects cookies into a Facebook login session, allowing the attacker to access the victim's account.

## Execution

### Running the Server

1. Navigate to the project directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the server:
   ```bash
   node server.js
   ```

### Running the Python Script

1. Ensure you have Python installed.
2. Navigate to the project directory.
3. Run the script:
   ```bash
   python hack.py
   ```

### Testing the Chrome Extension

1. Open Chrome and go to `chrome://extensions/`.
2. Enable "Developer mode."
3. Click "Load unpacked" and select the `chrome_test/` directory.
4. Trigger the extension and observe the actions in the console.

## How to Prevent Attacks

- Set up firewalls and limit user permissions.
- Regularly clean cookies and cache.
- Enable two-factor authentication.
- Ensure the HttpOnly and Secure attributes are set for cookies.
```
