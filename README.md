![resim](https://github.com/user-attachments/assets/cf2d9ee5-bea0-41ab-9e65-fd98c95c6dfe)
[![Patch recovery for fastbootd](https://github.com/galaxy-darkerdroid/patch-recovery-revived/actions/workflows/patch-recovery.yml/badge.svg)](https://github.com/galaxy-darkerdroid/patch-recovery-revived/actions/workflows/patch-recovery.yml)
# Patch-Recovery-Revived for Samsung Galaxy Note20 Ultra 4G/5G

The only working `patch-recovery` tool that ever lived to patch Samsung's recovery images to enable **fastbootd mode**.

<details>
  <summary>Screenshots 📷</summary>

![20250530_222257](https://github.com/user-attachments/assets/1dc3409c-ebd3-457c-8028-a25b55db9988)

![20250530_222251](https://github.com/user-attachments/assets/a1c0052c-f388-4073-a642-796d4c924178)

</details>

## Features

- Supports `.img`, `.lz4`, and `.zip` formats as input.
- Automatically downloads and processes recovery images from a provided URL or local path.
- Hex-patches the recovery binary to enable **fastbootd** mode.
- Signs the patched recovery image with Google's RSA private test key.
- Creates an ODIN-flashable `.tar` file for easy flashing.

## Usage

### 🟢 GitHub Workflow

Use the GitHub Actions workflow to automate the process:

1. Star and fork this repository.
2. Trigger the workflow manually via the **Actions** tab.
3. Provide the required inputs:
   - **Model**: Your device's model number.
   - **Recovery Link**: Direct download link to the recovery image.
   - You can upload the recovery and get a direct link from https://filebin.net/

- The workflow will generate a patched recovery image and upload it as an artifact.
- Optionally uploaded to [GoFile](https://gofile.io/) for easy sharing.

### Output

**The patched recovery image will be available as:**
- A `.tar` file for ODIN flashing.

### 🟢 Local Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/ravindu644/patch-recovery-revived.git
   cd patch-recovery-revived
   ```

2. Run the script:
   ```bash
   ./patch-recovery.sh <URL/Path to Recovery Image> <Model Number>
   ```

   The script will automatically install all required dependencies and process the recovery image.

### Note

If the tool does not enable fastboot mode for your device, please start an issue on GitHub. Make sure to upload the `recovery.img` file so the issue can be investigated.

## Credits

Forked and builded for Note20 Ultra by @galaxy-darkerdroid

Developed by [@ravindu644](https://github.com/ravindu644).

Got the idea from [phhusson](https://github.com/phhusson), [Johx22](https://github.com/Johx22), [ratcoded](https://github.com/ratcoded).

(This entire README and the commit messages were written by GitHub Copilot since I was too lazy. The code, however, is almost 95% written by me 😌)
