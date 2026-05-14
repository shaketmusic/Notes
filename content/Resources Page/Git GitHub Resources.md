
---
# Git

## Working with .gitignore

- [GitHub – Ignoring Files](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files)
- [git Documentation – .gitignore](https://git-scm.com/docs/gitignore)

## Interactive Git Tutorial

- [Learn Git Branching](https://learngitbranching.js.org/)

## Video Tutorials

- [Git and GitHub for Poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV) – The Coding Train (Dan Schiffman)

# GitHub Desktop

## Getting Started

- [Getting Started](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop)
- [Creating a New Repository](https://docs.github.com/en/desktop/overview/creating-your-first-repository-using-github-desktop#part-2-creating-a-new-repository)
- [Configuring a Default Editor in GitHub Desktop](https://docs.github.com/en/desktop/configuring-and-customizing-github-desktop/configuring-a-default-editor-in-github-desktop)
- [Adding a Repository from Your Local Computer to GitHub Desktop](https://docs.github.com/en/desktop/adding-and-cloning-repositories/adding-a-repository-from-your-local-computer-to-github-desktop)
- [Cloning and Forking Repositories from GitHub Desktop](https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop)
- [Committing and Reviewing Changes to Your Project in GitHub Desktop](https://docs.github.com/en/desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project-in-github-desktop)
- [Pushing Changes to GitHub from GitHub Desktop](https://docs.github.com/en/desktop/making-changes-in-a-branch/pushing-changes-to-github-from-github-desktop)

## Branching

- [Syncing Your Branch in GitHub Desktop](https://docs.github.com/en/desktop/working-with-your-remote-repository-on-github-or-github-enterprise/syncing-your-branch-in-github-desktop)
- [Managing Branches in GitHub Desktop](https://docs.github.com/en/desktop/making-changes-in-a-branch/managing-branches-in-github-desktop)

## Pull Requests

- [Creating an Issue or Pull Request from GitHub Desktop](https://docs.github.com/en/desktop/working-with-your-remote-repository-on-github-or-github-enterprise/creating-an-issue-or-pull-request-from-github-desktop)
- [Resolving a Merge Conflict on GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)
- [Resolving a Merge Conflict Using the Command Line](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)

# Git CLI

- Setup:
    
    ```bash
    git config --global user.name
    git config --global user.email
    ```
    
- Status of repo, showing tracked and untracked files, as well as commit differences between local and remote:
    
    ```bash
    git status
    ```
    
- Show a log of all commits:
    
    ```bash
    git log
    ```
    
- Pull from remote to local, and Push from local to remote:
    
    ```bash
    git pull
    git push
    ```
    
- Start tracking a specified file:
    
    ```bash
    git add <FILE_NAME>
    ```
    
    - You do not need to include the angled brackets <>.
    - Flags:
        - `-A` – Add all files
- Create a commit:
    
    ```bash
    git commit
    ```
    
    - Flags:
        - `-m "your commit message"`
    - Adding the `-m` flag to add a message and avoid usage og the VIM editor.
- Clone specified remote into local:
    
    ```bash
    git clone <REPO_LINK> <LOCAL_PATH>
    ```
    
    - If no local path is provided, current terminal directory will be used as the path.
    - You do not need to include the angled brackets <>
- Stop tracking a currently tracked file:
    
    ```bash
    git rm --cached <FILE_NAME>
    ```
    
    - You do not need to include the angled brackets <>
- Stop tracking a currently tracked folder and all files in the folder recursively:
    
    ```bash
    git rm -r <FOLDER_NAME>
    ```
    
    - You do not need to include the angled brackets <>

# Git LFS

- [About Git Large File Storage and GitHub Desktop](https://docs.github.com/en/desktop/configuring-and-customizing-github-desktop/about-git-large-file-storage-and-github-desktop) – Git LFS is automatically installed when installing GitHub Desktop
- [About Git Large File Storage](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage) – Info about Git LFS, and storage capacity
- [Configuring Git Large File Storage](https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage)

<aside>
💡 Note that Git LFS must be configured via the command line.

</aside>

## Git-LFS Tutorial

### Overview

- The [git-lfs](https://git-lfs.github.com/) package can be used for handling large files in a repo.
- Git-LFS recognizes the types of files to include based on a [*.gitattributes*](https://www.git-scm.com/docs/gitattributes) file, which is used to give attributes to pathnames. In this case, .gitattributes will be used to specify how to handle files with specific extensions.
- Git-LFS uploads large files to an online storage destination from where GitHub is able to retrieve them.

### Usage

- Install git-lfs of your system using Homebrew.
    
    ```bash
    brew install git-lfs
    ```
    
    <aside>
    ❗ *If you do not have Homebrew installed (you'll know depending on whether the previous command failed), you can install it via the terminal using the command found in the **Install Homebrew** section of [this link](https://brew.sh/).*
    
    </aside>
    
- Enable git-lfs on your repo by executing the following command in the root directory of your repository.
    
    ```bash
    git lfs install
    ```
    
- Then, you need to indicate what files should be tracked by git-lfs. The following command will create a **.gitattributes** file if you do not have one, and track files of a specified type, in this case, *.wav* files.
    
    ```bash
    git lfs track “*.wav”
    ```
    
- Add your files, Commit, and Push
    
    ```bash
    git add -A
    git commit -m “My commit message”
    git push
    ```
    
- If the push fails, try the following steps:
    - Reenable git-lfs for your repo
        
        ```bash
        git lfs install
        ```
        
    - Push your lfs file directly
        
        ```bash
        git lfs push --all origin
        ```
        
    - Try and push your most recent commit once again
        
        ```bash
        git push
        ```
        

### Resources

- [GitHub Git-LFS documentation](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage)
- [Git-LFS Unity Template](https://github.com/dcardonab/Berklee-MTEC_340/blob/main/Resources/gitignore_templates.md#unity-gitattributes)

# Recommended `.gitignore`

Copy the content below to your own `.gitignore` **file. Remember to place this file at the root of your repository.

You may comment out the last line by placing a hash at the beginning of the line if you wish to track the `.gitignore` file in your repository.

Alternatively, you may put together your own `.gitignore` based on the resources I included in [GitHub](https://github.com/dcardonab/Berklee-MTEC_340/blob/main/Resources/gitignore_templates.md). I recommend copying the Unity and the macOS sections to your own `.gitignore` file. The content at these links is the same content as the text box below.

You may refer to [this link](https://github.com/github/gitignore/tree/main) for a full list of GitHub's recommended `.gitignore` files, which may be essential for working with different programs. Refer to the [Global folder](https://github.com/github/gitignore/tree/main/Global) for `.gitignore` files for different operative systems and platforms.

### macOS/Windows/Unity/Wwise/VSCode/Rider `.gitignore`

```bash
## This .gitignore has been designed to ignore the temporary assets of the following programs/platforms:
## macOS## Unity## Wwise## Visual Studio Code## JetBrains Rider
## Remember that the .gitignore file should be placed at the root of your Unity project directory.
## Get latest from https://github.com/github/gitignore/blob/main/Unity.gitignore

##################################################
###################### MISC ######################
##################################################

## Comment the line below to track this .gitignore file.
# .gitignore

###################################################
###################### MACOS ######################
###################################################

# General
.DS_Store
.AppleDouble
.LSOverride

# Icon must end with two \r
Icon

# Thumbnails
._*

# Files that might appear in the root of a volume
.DocumentRevisions-V100
.fseventsd
.Spotlight-V100
.TemporaryItems
.Trashes
.VolumeIcon.icns
.com.apple.timemachine.donotpresent

# Directories potentially created on remote AFP share
.AppleDB
.AppleDesktop
Network Trash Folder
Temporary Items
.apdisk

#####################################################
###################### WINDOWS ######################
#####################################################

# Windows thumbnail cache files
Thumbs.db
Thumbs.db:encryptable
ehthumbs.db
ehthumbs_vista.db

# Dump file
*.stackdump

# Folder config file
[Dd]esktop.ini

# Recycle Bin used on file shares
$RECYCLE.BIN/

# Windows Installer files
*.cab
*.msi
*.msix
*.msm
*.msp

# Windows shortcuts
*.lnk

###################################################
###################### UNITY ######################
###################################################

**/[Ll]ibrary/
**/[Tt]emp/
**/[Oo]bj/
**/[Bb]uild/
**/[Bb]uilds/
**/[Ll]ogs/
**/[Uu]ser[Ss]ettings/

# MemoryCaptures can get excessive in size.
# They also could contain extremely sensitive data
**/[Mm]emoryCaptures/

# Recordings can get excessive in size
**/[Rr]ecordings/

# Uncomment this line if you wish to ignore the asset store tools plugin
# /[Aa]ssets/AssetStoreTools*

# Autogenerated Jetbrains Rider plugin
**/[Aa]ssets/Plugins/Editor/JetBrains*

# Gradle cache directory
.gradle/

# Autogenerated VS/MD/Consulo solution and project files
ExportedObj/
.consulo/
*.csproj
*.unityproj
*.sln
*.suo
*.tmp
*.user
*.userprefs
*.pidb
*.booproj
*.svd
*.pdb
*.mdb
*.opendb
*.VC.db

# Unity3D generated meta files
*.pidb.meta
*.pdb.meta
*.mdb.meta

# Unity3D generated file on crash reports
sysinfo.txt

# Builds
*.apk
*.aab
*.unitypackage
*.app

# Crashlytics generated file
crashlytics-build.properties

# Packed Addressables
**/[Aa]ssets/[Aa]ddressable[Aa]ssets[Dd]ata/*/*.bin*

# Temporary auto-generated Android Assets
**/[Aa]ssets/[Ss]treamingAssets/aa.meta
**/[Aa]ssets/[Ss]treamingAssets/aa/*

###################################################
###################### WWISE ######################
###################################################

# Project data
**/*WwiseProject/.cache
**/*.akd
**/*.prof
**/*.validationcache

# WWise Picker (Unity Editor)
**/Assets/Wwise/Editor/ProjectData/AkWwiseProjectData.asset*

# Temp Install Files
**/WwiseUnityIntegration_*_Src.zip

####################################################
###################### VSCode ######################
####################################################

**/.vscode/*
!**/.vscode/settings.json
!**/.vscode/tasks.json
!**/.vscode/launch.json
!**/.vscode/extensions.json
!**/.vscode/*.code-snippets

# Configuration file
**/.vsconfig

# Local History for Visual Studio Code
**/.history/

# Built Visual Studio Code Extensions
**/*.vsix

# Visual Studio cache directory
**/.vs/

#############################################################
###################### JetBrains Rider ######################
#############################################################

**/.idea

# User specific
**/.idea/**/workspace.xml
**/.idea/**/tasks.xml
**/.idea/shelf/*
**/.idea/dictionaries
**/.idea/httpRequests/

# Sensitive or high-churn files
**/.idea/**/dataSources/
**/.idea/**/dataSources.ids
**/.idea/**/dataSources.xml
**/.idea/**/dataSources.local.xml
**/.idea/**/sqlDataSources.xml
**/.idea/**/dynamic.xml

# Rider auto-generates .iml files, and contentModel.xml
**/.idea/**/*.iml
**/.idea/**/contentModel.xml
**/.idea/**/modules.xml
```

# UNIX Shell Navigation Commands

- Display current path:
    
    ```bash
    pwd
    ```
    
- Change directory:
    
    ```bash
    cd
    ```
    
    - If you do not provide an argument, this command will take you to the root of the User directory.
    - Arguments:
        - `.` – Current directory ; You may use this when specifying the current path
        - `..` – Parent directory
        - `/` – Go into child directory
- List all files and folders in current directory:
    
    ```bash
    ls
    ```
    
    - `-A` – Include hidden files
    - `-a` – Include hidden files as well as implied files and folders, e.g., current directory (.) and parent directory (..)
- Create a new file:
    
    ```bash
    touch <NAME_OF_NEW_FILE.EXTENSION>
    ```
    
    - Remember to supply the extension for the file you're creating
- Create a new folder inside the current path:
    
    ```bash
    mkdir <FOLDER_NAME>
    ```
    
- Remove file and folder:
    
    ```bash
    rm <FILE_NAME.EXTENSION>
    ```
    
    - You may supply an empty folder in place of the file
    - `r` – Delete folder and its contents recursively; BE VERY CAREFUL WITH THIS COMMAND!

# Troubleshooting Git and CLI

## `code` Terminal Command

If you are using VSCode as your Text Editor, you can setup the `code` keyword to open files in VSCode using the following UNIX command:

```bash
code <filename>
```

If this command isn't working, follow these instructions:

1. Open VSCode.
2. Open the Command Palette with the following key command: **Shift + Command + P.**
3. Write *Shell Command: Install 'code' command in PATH* at the prompt, and press Enter or Return.

## Developer Tools

If you do not have developer tools install on MacOS, do one of the following:

1. Install Xcode from the App Store, or
2. Run the following commands in your terminal. The first one will install developer tools and the second one will verify the installation:

```bash
xcode-select --install
xcode-select -p
```

## Exiting VIM

If your terminal ends up in VIM, potentially because you used the `git commit` command without the `-m` flag. you can exit VIM using the following sequence:

1. Press colon **:** to enable command input.
2. Use the letter **q** to quit.
3. Press enter to execute command.

## Git/GitHub CLI – Authentication Failed Error

If you want to use the CLI (Command Line Interface) with Git/GitHub, and you're running into an 'Authentication failed' error, follow these instructions:

1. Log into your GitHub account using a browser.
2. Select '**Settings**' from the user menu in the top right.
3. Select '**Developer settings**' at the bottom of the menu on the left.
4. Select '**Personal access tokens > Tokens (classic)**'.
5. Choose '**Generate new token > Generate new token (classic)**'.
6. Choose a **name** for your token (e.g., Personal Laptop), and choose any number of days under '**Expiration**'
    - Note that when the token expires, you will need to go through this process again.
7. Click on the checkbox to the left of '**repo**' in the 'Select scopes' section
    - You can read more about scopes [here](https://docs.github.com/apps/building-oauth-apps/scopes-for-oauth-apps/).
8. Click on the **Generate token** button at the bottom of the page.
9. Copy your token somewhere safe.
    - **NOTE THAT YOU WILL NOT BE ABLE TO SEE THIS TOKEN AGAIN**.
10. Back on your terminal, initiate the 'git push' command, and use this token as your password when prompted.

## Hidden Files in the Finder

To view hidden files in the macOS finder, open a finder window and use the following key command: **Command + Shift +** .

Notes:

- Hidden files start with the period character and are grayed out.
- If there are no hidden files in that folder, nothing should change from what you see.
- Some files, like *.DS_Store* will not display in the finder, regardless of whether you are displaying hidden files or not.

## Unable to Push Due to Large and/or Temporary Files

1. If you already committed your repo and it isn’t pushing, you need to remove your current commit. This will allow you to verify or add a `.gitignore` file:
    1. Open your Terminal and navigate to the root directory of your repo using `cd` commands.
        - You can verify that you are in the root directory of your repo by running the `git status` command. You should get an output indicating the state of your repository, as opposed to one that says that you aren’t in a repo.
    2. Run the command `git reset HEAD~1` to undo the commit and unstage added files from the commit.
    
    <aside>
    ⚠️ Alternatively and only if this is your first commit to your repo and you’re not working with a team, you may delete the repo a create a new one.
    
    </aside>
    
2. Verify that your `.gitignore` has been set to work with macOS and Unity, and is located in the right directory.
    1. Your `.gitignore` file should have lines that ignore every Unity file that isn’t necessary for rebuilding the project. In particular, you can reconstruct any Unity project from the folders **Assets**, **Packages**, and **Project Settings**.
        - The `.gitignore` below this text block has been designed to include only the necessary Unity folders, as well as ignore all unnecessary macOS, JetBrains Rider, VSCode, and Wwise files.
            
            [.gitignore](Git%20GitHub%20Resources.gitignore)
            
    2. Your `.gitignore` file must be located at the root level of your directory. If in doubt, you can identify the root directory in several ways:
        - In the Finder, use the keyboard shortcut **Shift + Cmd + .** to show hidden files. If you see a `.git` folder, then you know you’re in the root directory of a local repository.
        - In the terminal, navigate to the directory you assume to be the root of your local repo using the cd command. You can then run the `ls -A` command and check if there is a `.git` folder in that directory, or the git status command.
3. If you have files in your repository that are larger than 100MB, such as long uncompressed audio files, 3D models, or videos, you will need to work with Git LFS (Large File Storage). To set LFS, you may follow the Git LFS guide I included below. In particular, look at the **Git LFS Tutorial** section.
    
    [Git LFS](Git%20GitHub%20Resources.md) 
    
4. Once you have unstaged the commit that can’t be pushed onto the remote repo, verified that your `.gitignore` is both the correct one and in the right place, and setup Git LFS if you need it, you can once again add, commit, and push your repository changes. The commands below must be executed at the root level of your repository.
    1. Stage all files for a commit: `git add -A` 
    2. Commit files with a message: `git commit -m "YOUR_COMMIT_MESSAGE"`
    3. Push your commit from your local repo to your remote repo: `git push`