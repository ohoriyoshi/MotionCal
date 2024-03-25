# MotionCal Project Build Instructions for macOS

This document provides a comprehensive guide for setting up and building the MotionCal project on macOS.

## Prerequisites

- Access to a macOS computer with internet connectivity.
- Familiarity with basic terminal operations.

## Installation Steps

### 1. Install Homebrew

Open the terminal and execute the following command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Add Homebrew to your shell's PATH by running:

sh
Copy code
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
Apply the changes by sourcing your profile:

sh
Copy code
source ~/.zprofile
2. Install Dependencies
Install wxWidgets using Homebrew:

sh
Copy code
brew install wxwidgets
Check the installation by verifying the version of wx-config:

sh
Copy code
wx-config --version
3. Clone or Download the Project
Clone the MotionCal project from GitHub or download it as a ZIP file and extract it.

4. Edit the Makefile
Navigate to the MotionCal directory and open the Makefile in a text editor. Make the necessary edits for macOS build options:

make
Copy code
# Uncomment the line for macOS and add the architecture flag for ARM64
OS = MACOSX_CLANG
CFLAGS = -O2 -Wall -DMACOSX -arch arm64
Adjust any other necessary sections in the Makefile as per your requirements.

5. Build the Project
In the terminal, initiate the build process with:

sh
Copy code
make
Follow any error instructions to make required adjustments.

6. Run the Application
Once the build is successful, execute the generated MotionCal.app:

sh
Copy code
open MotionCal.app
7. Troubleshooting
If you encounter build issues, consult the error messages and perform the necessary troubleshooting.

For additional information, contributions, or questions, please refer to the issues section or submit a pull request.
