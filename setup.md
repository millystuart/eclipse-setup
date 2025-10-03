# Eclipse IDE Version 2025-09 (4.37.0) Set-up

## Resources:
- https://www.makeuseof.com/install-eclipse-ide-on-linux/
- https://medium.com/@ashutoshtaikar/make-eclipse-great-again-fb347cf96c87
- https://www.javacodegeeks.com/2025/09/top-10-eclipse-plugins-every-java-developer-must-install.html
- https://developer.mamezou-tech.com/en/blogs/2025/04/13/eclipse-settings-for-newcomer/
- https://www.tabnine.com/blog/plugins-for-eclipse/#:~:text=JUnit%20is%20a%20popular%20open,to%20use%20with%20comfortable%20shortcuts.

## Installation instructions
1. Ensure that Java is installed on your system (`sudo apt install openjdk-{version-number}-jdk`)
2. Install the Eclipse Installer for Linux from their [website](https://www.eclipse.org/downloads/packages/)
3. Once installed, extract files to home (or wherever)
4. In your terminal, navigate to extracted directory
5. Run `./eclipse-inst` to launch the installer
6. Select **Java IDE for Enterprise Java and Web Developers**
7. Choose VM and installation folder location, and install

## Configuration

### Check Java version
1. **Window** > **Preferences** > **Java** > **Installed JREs**
2. Check that you are using your desired JDK, if not then follow the following instructions:
   1. Install desired JDK to your system
   2. In **Installed JREs**, press **Add** and choose type **Standard VM**
   3. For **JRE home**, press directory and locate the installed JDK. This is typically found at `/user/lib/jvm/{name-of-JDK}`
   4. Press **Finish**
   5. Check the added JDK (and if necessary, delete the old one) and **Apply and Close**

### Install plugins
1. **Help** > **Eclipse Marketplace**
2. Recommended plugins:
   - **Darkest Dark Theme DevStyle (modernise UI)**
   - Eclipse Color Theme (additional themes)
3. Additional plugins that could be used:
   - Eclipse-pmd 4.11 (static analysis of code on save, and quick fixes)
   - CheckStyle (enforce code formatting/rules)
   - EGit (Git integration if Git through UI is preferred)
   - SonarLint (quality/security checks)
   - MoreUnit (unit test helper)
   - JUnit-Tools (additional JUnit test support)
   - GitHub Copilot (AI assistance)

#### My DevStyle setup
When you install DevStyle, it will restart the IDE. Upon next launch, you will have the option to edit the theme.
1. **Workbench**: Light Custom
2. **Editors**: Intellij IDEA
3. In settings, you can further tweak your configuration if desired (**Window** > **Preferences** > **DevStyle**)

### Standardise character encoding
1. **Window** > **Preferences** > **General** > **Workspace**
2. Ensure that **Text file encoding** is set to `UTF-8`

### Showing character count line (for readability)
1. **Window** > **Preferences** > **General** > **Editors** > **Text Editors**
2. Select **Show print margin** and set it to your desired number of characters (e.g. `120`)

### Adjust font size/style
1. **Window** > **Preferences** > **General** > **Appearance** > **Colours and Fonts**
2. Select **Basic** > **Text Font** press **Edit**
3. Set to your preferred size and style

### Set up code formatting
1. **Window** > **Preferences** > **Java** > **Code Style** > **Formatter**
2. Change **Active profile** to `Java Conventions`
3. Press **Edit**
4. Expand **Indentation** tab
5. Change **Tab policy** to `Spaces only`
6. Set the **Indentation size** and **Tab size** to `4`
7. Rename profile to `My Java Conventions` and press **OK**
8. Apply and close

### Turn on autocomplete
1. **Window** > **Preferences** > **Java** > **Editor** > **Content Assist**
2. Go to the **Auto Activation** section, and change the **Auto activation triggers for Java** to `abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ._`
3. In the **Insertion** section, select **Disable insertion triggers except 'Enter'**