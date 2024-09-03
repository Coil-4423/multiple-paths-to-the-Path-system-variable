You can add multiple paths to the `Path` system variable, but there’s only one `Path` variable in the system environment. What you do is add multiple directory paths to this single `Path` variable. Each directory path should be separated by a semicolon (`;`). Here's a detailed explanation:

### Understanding the `Path` Variable

- **Single `Path` Variable:** In the "Environment Variables" dialog, there is one `Path` variable under "System variables" (or "User variables" if you are modifying user-specific settings).
  
- **Multiple Paths in `Path`:** This single `Path` variable can contain multiple paths, each separated by a semicolon. When you run a command, the system searches through each directory listed in the `Path` variable to find the executable.

### How to Add Multiple Paths

1. **Open Environment Variables:**
   - Right-click on "This PC" or "Computer" on your desktop or in File Explorer.
   - Select "Properties."
   - Click on "Advanced system settings."
   - Click the "Environment Variables" button.

2. **Edit the `Path` Variable:**
   - In the "System variables" section, find the `Path` variable and select it.
   - Click "Edit."

3. **Add Paths:**
   - In the "Edit Environment Variable" dialog, you will see a list of directories.
   - You can click "New" to add a new path to the list.
   - If you prefer, you can also manually add the path to the end of the list, making sure it’s separated from existing entries by a semicolon.

4. **Example:**
   Suppose your existing `Path` variable looks like this:
   ```
   C:\Program Files\Java\jdk1.8.0_231\bin;C:\Program Files\Python38
   ```
   To add Node.js, you would add its path:
   ```
   C:\Program Files\Java\jdk1.8.0_231\bin;C:\Program Files\Python38;C:\Program Files\nodejs
   ```

5. **Save Your Changes:**
   - Click "OK" to close the "Edit Environment Variable" dialog.
   - Click "OK" again to close the "Environment Variables" dialog.
   - Click "OK" to close the "System Properties" dialog.

6. **Verify:**
   - Open a new Command Prompt or PowerShell window.
   - Run `node -v` and `npm -v` to check if Node.js and npm are now accessible.

### Key Points

- **Do Not Create Multiple `Path` Variables:** You should only have one `Path` variable. Instead of creating multiple `Path` variables, manage the paths within this single variable.
  
- **Editing Safely:** Always append new paths rather than overwriting the entire `Path` variable to avoid removing important existing paths.

- **Backup Your `Path`:** Before making changes, copy the current `Path` variable value to a text file as a backup. This way, you can restore it if needed.

By following these guidelines, you can successfully manage multiple paths within a single `Path` variable and ensure that your system can locate executables for different applications.
