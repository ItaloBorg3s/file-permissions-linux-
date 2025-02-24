# 🔒 Directory Security in Linux

Proper directory permissions are crucial to securing files and preventing unauthorized access. Below are key techniques for managing directory security.

## 📜 Viewing Directory Permissions
To check permissions of a directory, use:
```sh
ls -ld directory_name
```
This displays details about the directory itself instead of its contents.

## 🔐 Restricting Directory Access
### 1️⃣ Allow only the owner to access a directory:
```sh
chmod 700 secure_folder
```
- `7`: Owner (Read, Write, Execute)
- `0`: No access for Group and Others

### 2️⃣ Prevent accidental deletions by removing write permission:
```sh
chmod a-w important_folder
```
- `a-w`: Removes write permission from everyone

## 🏗️ Managing Shared Directories
### 3️⃣ Creating a shared directory with group access:
```sh
chmod 770 shared_folder
```
- `7`: Full access for Owner and Group
- `0`: No access for Others

### 4️⃣ Ensuring new files inherit group ownership:
```sh
chmod g+s shared_folder
```
- `g+s`: Enables the setgid bit so new files inherit group ownership

For more advanced settings, refer to:
```sh
man chmod
