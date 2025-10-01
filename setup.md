# Eclipse IDE Version 2025-09 (4.37.0) Set-up

## Resources:
- https://www.makeuseof.com/install-eclipse-ide-on-linux/
- https://medium.com/@ashutoshtaikar/make-eclipse-great-again-fb347cf96c87
- https://www.javacodegeeks.com/2025/09/top-10-eclipse-plugins-every-java-developer-must-install.html
- https://developer.mamezou-tech.com/en/blogs/2025/04/13/eclipse-settings-for-newcomer/

## Installation instructions
1. Ensure Java is installed on your system (`sudo apt install openjdk-{version-number}-jdk`)
2. Install the Eclipse Installer from the [website](https://www.eclipse.org/downloads/packages/) for Linux
3. Once installed, extract files to home (or wherever desired)
4. In your terminal, navigate to extracted directory
5. Run `./eclipse-inst` to launch the installer
6. Select **Java IDE for Enterprise Java and Web Developers**
7. Select VM and installation folder location, and install

## Configuration

### Check Java version
1. **Window** -> **Preferences** -> **Java** -> **Installed JREs**
2. Check if you have the JDK you would like to use, and change the default if necessary

### Install plugins
1. **Help** -> **Eclipse Marketplace**
2. Recommended plugins:
   - **Darkest Dark Theme DevStyle (modernise UI)** has light and dark options
   - Eclipse Color Theme (additional themes)
3. Additional plugins that could be used:
   - CheckStyle (enforce code formatting/rules)
   - EGit (Git integration)
   - SonarLint (quality/security checks)
   - EclEmma (test coverage)
   - GitHub Copilot (AI assistance)

#### My DevStyle setup
When you install DevStyle, it will restart the IDE. Upon next launch, you will have the option to edit the theme.
1. **Workbench**: Light Custom
2. **Editors**: Intellij IDEA
3. In settings, you can further tweak your configuration if desired (**Window** -> **Preferences** -> **DevStyle**)

### Standardise character encoding
1. **Window** -> **Preferences** -> **General** -> **Workspace**
2. Ensure that **Text file encoding** is set to `UTF-8`

### Showing character count line (for readability)
1. **Window** -> **Preferences** -> **General** -> **Editors** -> **Text Editors**
2. Select **Show print margin** and set it to your desired number of characters (e.g. 120)

### Adjust font size/style
1. **Window** -> **Preferences** -> **General** -> **Appearance** -> **Colours and Fonts**
2. Select **Basic** -> **Text Font** press **Edit**
3. Set to your preferred size and style

### Set up code formatting
1. **Window** -> **Preferences** -> **Java** -> **Code Style** -> **Formatter**
2. Change **Active profile** to Java Conventions
3. Press **Edit**
4. Expand **Indentation** tab
5. Change **Tab policy** to `Spaces only`
6. Set the **Indentation size** and **Tab size** to `4`
7. Rename profile to My Java Conventions and press OK
8. Apply and close

### Turn on autocomplete
1. **Window** -> **Preferences** -> **Java** -> **Editor** -> **Content Assist**
2. Go to the **Auto Activation** section, and change the **Auto activation triggers for Java** to `abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ._`
3. In the **Insertion** section, select **Disable insertion triggers except 'Enter'**