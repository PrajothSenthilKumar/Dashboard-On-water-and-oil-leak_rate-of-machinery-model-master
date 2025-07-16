# Local Deployment Guide

## Prerequisites

1. **Install WSL2**  
   Download WSL2 from the Microsoft Store.

2. **Install nvm**

3. **Install Node.js**
   ```bash
   nvm install 20.18
   ```

4. **Install AWS CLI**
   > *Note: unzip is required before installing AWS CLI. apt install unzip prerequisite step needed since unzip won’t exist*

   Install `unzip`:
   ```bash
   sudo apt install unzip
   ```

5. **Avoid Mounted Folders**
   Ideally, **do not** use mounted folders (e.g., `/mnt`) for the code because it runs very slow there.  
   Instead, move the code to your home directory (`~`).

   To locate your current directory in Windows Explorer:
   ```bash
   explorer.exe .
   ```

## Cloning the Repository

6. Clone the repository into your **home folder**.  
   If you cannot clone using HTTPS, generate a personal access token:

   - Go to [GitHub Tokens](https://github.com/settings/tokens)
   - Select the **repo** scope
   - Click **Generate new token (classic)**

7. In the home folder Generate an SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "<github-username>"
   ```

8. Display your public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

9. **Clone the repository**:
   ```bash
   git clone <repository-url>
   ```

10. Navigate into the cloned folder:
    ```bash
    cd gologic-platform
    ```

## Running the Setup

11. In the `gologic-platform` project directory, execute:
    ```bash
    ./setup-local.sh
    ```
