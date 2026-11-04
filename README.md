# Simple-Cryptographer
<img width="1158" height="787" alt="Screenshot 2026-09-26 154032" src="https://github.com/user-attachments/assets/947c5164-ffb5-4e40-b717-cb27cf244197" />

This repo consists of a Python Cryptography Application (CLI, GUI, EXECUTABLE) and a web version that runs in any browser.
The program is solely built on python and serves as a way to encrypt and decrypt messages.

This project is a basic encryption and decryption toolkit that supports 10 classical historical ciphers. A total of 3 versions could be find in the files: a Procedural Command-Line Interface, a polished, Object-Oriented Graphical User Interface, and a web page version. The final executable represents the best desktop version of the app yet, and the web version lets you use the toolkit without installing anything.

## 🆕 Update: Web Version

The app now has a webpage. The web version is a single self-contained file, `index.html`, with no dependencies, and it runs entirely in the browser. Nothing you type is sent to a server.

**Live site:** `https://<your-username>.github.io/<repo-name>/` *(replace with your GitHub Pages URL)*

What's new in this update:
- **Browser-based interface** - Runs on desktop and mobile without Python or an installer
- **All 10 ciphers** - Same translation logic as the GUI, ported from Python to JavaScript
- **Same look and feel** - The dark Atomic One Dark Pro inspired theme carries over from the desktop GUI
- **Dynamic parameter fields** - Shift, Key, and Diameter fields appear only for the ciphers that use them
- **Browser clipboard support** - Copy Result and Paste Result use the system clipboard, with a "Copied!" confirmation
- **Fullscreen mode** - Toggle with the ⛶ button; press `Esc` to exit
- **Zero setup** - Single `index.html` file, no build step and no external libraries

### Running the Web Version Locally
1. Download or clone the repository
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari)

### Hosting Your Own Copy on GitHub Pages
1. Make sure `index.html` is at the root of your repository
2. Go to **Settings → Pages**
3. Under *Build and deployment*, select the `main` branch and the `/ (root)` folder, then save
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two

> **Note:** Copy and Paste use the browser Clipboard API, which only works on `https://` or `localhost`. GitHub Pages serves over HTTPS, so this works there. The browser will ask for permission the first time you use Paste.

### Web vs. Desktop Differences
- The command-line `Cipher` base classes are not included in the web version, since the GUI never used them
- Ciphers that work on letters (Caesar, Atbash, Beaufort, Vigenère, and others) shift only A–Z; accented or non-English letters pass through unchanged

## Core Features
- **Extensive Cipher Library** - Support for [10 distinct ciphers](#supported-ciphers)
- **Multiple Interfaces** - Includes a lightweight, text-based `CLI` version for quick terminal operations, a fully-featured `GUI` version, and a `Web` version that runs in the browser
- **Object-Oriented Architecture** - The GUI version utilizes an `OOP` design, completely separating translation layer and graphical elements for maximum code reusability
- **Dynamic User Interface** - GUI and web versions intelligently adapt to the selected cipher from the dropdown
- **Custom Theme** - The GUI and web versions are highly inspired by Atomic One Dark Pro featuring a `nightly` theme
- **Clipboard Integration** - The output can be copied and pasted by the help of buttons, integrated seamlessly inside the GUI and web page
- **Cipher Stacking** - Users can manually pass the output of one encryption process into another cipher to layer their token

## Supported Ciphers
All versions of the application share the same cipher logic and capabilities, boasting time and space efficiencies `(mostly O(*n*) time complexity)`.
All of the supported Ciphers are given below:
- **Caesar** : Classic Substitution cipher, great example of numeric shift
- **A1Z26** : Converts letter into corresponding alphabetical index
- **Atbash** : Reverses the alphabets
- **Baconian** : Encodes text into a 5 - character binary sequence of A and B
- **Beaufort** : A polyalphabetic substitution cipher requiring a key
- **Vigenère** : A polyalphabetic cipher using a key to shift characters
- **XOR** : A bitwise cipher converting text into hexadecimal format via secret keys
- **Scytale** : A transposition cipher requiring column diameter to wrap text
- **Rot13** : A fixed substitution cipher, shifting digits by 13 places
- **Morse Code** : Simple translation layer for alphanumeric to standard dots, dashes and slashes

## Technologies / Tools Used
- **Python 3.10+** : Core Programming Language
- **Tkinter** : Standard Python GUI toolkit used for creation of GUI and windows
- **Math Module** : Built-in Python Library used for column calculations in the Scytale Cipher
- **`Pyinstaller`** : Used to compile the final `.exe` application
- **HTML, CSS, JavaScript** : Power the web version (`index.html`), with no frameworks or external libraries
- **GitHub Pages** : Hosts the web version

*`While designing the program, it was kept in mind to utilize minimum number of external modules and libraries so that most of the code consists of pure python and understanding the code could be easy`*

## Steps to Install & Run the Project
### Prerequisites:
`Python 3.10+` via the official Python installer *(not needed for the web version)*
### Running the Source Code
1. Clone or download the repository to your local machine
2. Open terminal and navigate to project directory
3. Both `CLI` and `GUI` versions could run through ide if the dependencies are installed *(All that is listed in tools used)*
### Running the Executable
GUI version of the program can be directly opened through the `.exe` file in the folder `dist` found inside the releases folder
### Using the Web Version
Open the live site, or open `index.html` in your browser. See [Update: Web Version](#-update-web-version) for details.

## Instructions for Testing
1. Launch the application, any version works (GUI or web is recommended)
2. Select a Cipher via dropdown or the list
3. Input Data in the input box or field
4. Configure Parameters as per the cipher; `key`, `diameter`, `shift` might be required in some ciphers
5. Choose between encryption or decryption and get the output

### Testing Decryption (Reversibility):
1. Copy Result in output block after encryption
2. Click Clear button or continue running the code in CLI version
3. Paste the result in the input box / field and decrypt it
4. Verify if the original string is restored in the output box

**Test Edge Cases:** Input numbers, special characters or empty strings, all of these could be tackled by the `run_safely` wrapper and `alpha-checks`. Any kind of crash can be tackled through the help of `try` and `except` blocks too. The web version shows errors (such as a missing key) directly in the output box.

# Screenshots
<img width="1360" height="1790" alt="#1-vtpj" src="https://github.com/user-attachments/assets/121f4472-578a-4ece-b19a-06484ddcb4d4" />

<img width="1156" height="788" alt="#3-vtpj" src="https://github.com/user-attachments/assets/3028a1b7-abd2-4b44-84ee-bfa74ed5f083" />

<img width="1161" height="785" alt="#4-vtpj" src="https://github.com/user-attachments/assets/7bd8730f-3c49-4e3c-8de4-32ad94dcc122" />

<!-- TODO: add a screenshot of the web version here -->
