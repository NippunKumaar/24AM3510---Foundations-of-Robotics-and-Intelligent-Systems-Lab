# Student Setup Guide and Standard Lab SOP

**Course:** 24AM3510 - Foundations of Robotics and Intelligent Systems

**Course repository:** [24AM3510 Robotics Lab](https://github.com/NippunKumaar/24AM3510---Foundations-of-Robotics-and-Intelligent-Systems-Lab.git)

Complete this one-time setup before Lab 1. You will use the same setup for all later labs.

## What you need

- A Windows 10/11 computer or macOS computer
- Internet access
- About 2 GB of free storage
- Permission to install software on the computer

## Part A - Install the required software

### 1. Install Visual Studio Code

1. Download VS Code from [code.visualstudio.com](https://code.visualstudio.com/).
2. Install it using the default options.
3. Open VS Code after installation.

### 2. Install Python

1. Download Python 3.14.x from [python.org/downloads](https://www.python.org/downloads/).
2. Install it using the default options.
3. **Windows only:** select **Add Python to PATH** on the first installer screen.
4. Confirm installation in a terminal:

       python --version

   On macOS, use this if needed:

       python3 --version

### 3. Install Git

Git is needed to download updates to the course materials.

- **Windows:** install Git from [git-scm.com](https://git-scm.com/download/win), accepting the default choices.
- **macOS:** open Terminal and run:

       xcode-select --install

  If this is already installed, macOS will report that no action is needed.

Confirm installation:

    git --version

### 4. Add VS Code extensions

In VS Code, open **Extensions** from the left sidebar. Install:

1. **Python** (published by Microsoft)
2. **Jupyter** (published by Microsoft)

Restart VS Code if prompted.

## Part B - Download the course repository

1. In VS Code, press:
   - **Windows:** Ctrl+Shift+P
   - **macOS:** Cmd+Shift+P
2. Select **Git: Clone**.
3. Paste this repository URL:

       https://github.com/NippunKumaar/24AM3510---Foundations-of-Robotics-and-Intelligent-Systems-Lab.git

4. Choose a convenient local location, for example Documents or Desktop.
5. When VS Code asks whether to open the cloned repository, choose **Open**.

Do not download a ZIP file. Cloning with Git lets you receive later lab updates easily.

## Part C - Create the course Python environment

Open the VS Code terminal using **Terminal > New Terminal**. The terminal must be opened in the course repository folder, which contains requirements.txt.

### macOS

Run:

    python3 -m venv .venv
    source .venv/bin/activate
    python -m pip install --upgrade pip
    python -m pip install -r requirements.txt
    python -m ipykernel install --user --name robotics-labs --display-name "Python (Robotics Labs)"

### Windows PowerShell

Run:

    python -m venv .venv
    .\.venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    python -m pip install -r requirements.txt
    python -m ipykernel install --user --name robotics-labs --display-name "Python (Robotics Labs)"

If PowerShell prevents activation, run this once in the same terminal and repeat the activation command:

    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

The .venv folder is your personal course environment. Do not upload it, copy it, or submit it.

## Part D - Select the correct VS Code environment and notebook kernel

1. Press Ctrl+Shift+P (Windows) or Cmd+Shift+P (macOS).
2. Select **Python: Select Interpreter**.
3. Select the interpreter that includes **.venv** and belongs to this course repository.
4. Open a Jupyter notebook.
5. Select **Select Kernel** in the top-right corner.
6. Choose **Python (Robotics Labs)**. If this name is not shown, choose the environment labelled .venv.

## Part E - Start Lab 1

1. Open the folder **Lab-1**.
2. Open **Lab_01_Robot_Visualization_and_Coordinate_Frames.ipynb**.
3. Confirm that the selected kernel is the course .venv environment.
4. Run the first code cell. It must print the Robotics Toolbox version without an error.
5. Run the notebook from top to bottom.
6. Complete both assignment problems and write answers in the requested Markdown cells.
7. Save a personal submission copy using your name and USN, for example:

       Lab_01_Robot_Visualization_and_Coordinate_Frames_YourUSN.ipynb

8. Submit the saved, fully executed notebook through the Google Form before the deadline.

## Standard operating procedure for every lab

Follow this routine for Lab 1, Lab 2, Lab 3, and all later Python labs.

1. Open the local course repository in VS Code.
2. Open the terminal and activate the existing .venv environment:

   **macOS**

       source .venv/bin/activate

   **Windows PowerShell**

       .\.venv\Scripts\Activate.ps1

3. Download the newest teaching materials:

       git pull

4. Open the required lab folder.
5. Create a personal working copy of the supplied worksheet before entering answers.
6. Select the course .venv kernel.
7. Read the Markdown explanation before each code cell; predict the output; then run and modify the code as instructed.
8. Complete both assignment problems independently.
9. Save the executed notebook and submit it through the Google Form.

## Troubleshooting

| Problem | Action |
|---|---|
| Python command is not found | Restart VS Code. On macOS, use python3 instead of python. On Windows, reinstall Python and select Add Python to PATH. |
| ModuleNotFoundError | Confirm that .venv is selected as the notebook kernel. In the activated environment, run: python -m pip install -r requirements.txt |
| Wrong notebook output or an old version | In the repository folder, run: git pull |
| Git pull refuses because of local changes | Do not edit the original teaching notebook. Save your work using a different filename, then ask the instructor for help. |
| Plot window does not appear | Run the earlier import cells first, then rerun the plotting cell. |

## Academic integrity and use of AI

AI may be used to clarify concepts or diagnose an error, but every student must understand and be able to explain submitted code and answers. Record any meaningful AI assistance in the notebook when requested. Blindly copying AI-generated code is not acceptable.
