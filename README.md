# OpenGL Environment Setup for Code::Blocks (Windows)

This setup automates the installation and configuration of the OpenGL development environment for **Code::Blocks with MinGW** on Windows. It includes everything needed to start OpenGL programming right away.

---

## Why Use This Setup?

Manually setting up OpenGL for Code::Blocks can be tedious. This automated script:

- Installs Code::Blocks silently
- Copies necessary OpenGL (GLUT) files to correct system locations automatically 
- Sets up the environment variables automatically
- Supports both 32-bit and 64-bit systems

---

## Instructions

1. **[Download the opengl-setup ZIP file](https://drive.google.com/uc?export=download&id=19xq37n82aNH2N9rf2WLRBTdSybArKG4j)** containing the full setup including codeblock-17.12mingw-setup.exe file.
2. **Extract** the ZIP file anywhere on your PC (e.g., Desktop or Downloads).
3. Inside the extracted folder, **right-click** on `setup.bat` and choose **Run as Administrator**.
4. The script will:
   - Install Code::Blocks 
   - Copy `glut32.dll` to the proper Windows system folder
   - Copy `glut32.lib` and `glut.h` to Code::Blocks MinGW directories
   - Add Code::Blocks to the system PATH variable automatically

After completion, you will see:

## OpenGL Setup Completed Successfully!

---

## How to Create a GLUT Project in Code::Blocks

1. **Open Code::Blocks**
2. Go to **File > New > Project**
3. Select **Empty Project** and click **Go**
4. Name your project and select a folder to save and click next.
5. Add the following path:
   ``` C:\Program Files (x86)\CodeBlocks\MinGW ```
6. After creating the project, go to the **Project menu >Select the project >right click and select- Build Options**
7. Under the **Linker settings** tab:
   - Click the **Add** button and add the following libraries(does not need to paste the full path):
     ```
     opengl32
     glu32
     glut32
     ```
9. Under the **Search directories > Compiler** tab:
   - Add this path:
    ``` C:\Program Files (x86)\CodeBlocks\MinGW ```
     
10. Under **Search directories > Linker** tab:
   - Add this path:
     ```
     C:\Program Files (x86)\CodeBlocks\MinGW\lib
     ```

---

## Run the Code

On your left, put the mouse icon on top of **Project/Files/Sources/Anything**  similar scrollbar and scroll your **mouse wheel** slowly, it will show your project name with **Source** inside. Click on Source to reveal the **main.cpp** file.

Double click to open the **main.cpp** file.

Now add the following code into the 14th line of main.cpp :

```#include<windows.h>```

press **F9** from your keyboard or click **build & run** icon from the top bar to run the program.

---

## Notes

- Make sure to **run `setup.bat` as Administrator**, or the installation may fail.
- Internet connection is required for downloading some files from Google Drive during setup.
- If Code::Blocks is already installed, the script will still configure the OpenGL files correctly.
- If codeblock installation fails for any reason, just delete the folder called **"CodeBlock"** from **C:\Program Files (x86)\CodeBlocks**  and try again.
- If you see any windows defender security popup during installation, just click "More Info" and then select **Accept / Install Anyway** to run the script.

---

## License

This script is provided for personal, educational, and non-commercial use.
