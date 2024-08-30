# Cloner Script

This script allows you to clone a Git repository into a selected directory. It provides an interactive way to navigate through directories and choose where to clone the repository.

## Prerequisites

- Bash shell (Can be used in windows with Git Bash or WSL or else)
- Git

## Usage

1. **Clone the repository:**

   ```bash
   git clone https://github.com/G3Labz/repo-cloner-path-chooser.git
   ```

    And use it:

   ```bash
   ./cloner.sh <repository-url>
   ```

   Replace `<repository-url>` with the URL of the Git repository you want to clone.

2. **Interactive Directory Selection:**

   - The script will prompt you to select a directory or stay in the current directory.
   - You can navigate deeper into subdirectories if needed.
   - Once you select a directory, the repository will be cloned into that directory.

## Example

```bash
$ ./cloner.sh https://github.com/G3Labz/repo-cloner-path-chooser.git
Please select a directory or stay in the current directory (/path/to/root):
1) /path/to/root/dir1
2) /path/to/root/dir2
3) Stay in the current directory
#? 1

Do you want to go deeper into /path/to/root/dir1? (y/n)
y
Please select a directory or stay in the current directory (/path/to/root/dir1):
1) /path/to/root/dir1/subdir1
2) /path/to/root/dir1/subdir2
3) Stay in the current directory
#? 3

Selected path: /path/to/root/dir1
Cloning into '/path/to/root/dir1/finjs'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 1), reused 10 (delta 1), pack-reused 0
Receiving objects: 100% (10/10), done.
Resolving deltas: 100% (1/1), done.
Repository cloned to /path/to/root/dir1/finjs and user.email set to your-email@example.com
```

## Configuration
 
- **User Email:** 🚧🚧🚧 The script sets a predefined user email for the local Git configuration. You can change the email by modifying the `USER_EMAIL` variable in the script. 🚧🚧🚧 (shall change to a be by parameters or something like that)

## Script Details

- **Root Directory:** The script determines the root directory where it is stored and starts the directory selection from there.
- **Directory Navigation:** The script lists child directories and allows you to navigate deeper if needed.
- **Cloning:** The selected directory path is used to clone the repository.
