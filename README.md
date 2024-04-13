All-in-One GitHub Uploader
An all-in-one tool for uploading files, creating directories, and deleting files/directories from a GitHub repository using the GitHub API.
Prerequisites
CoffeeScript installed
Requests library installed
A GitHub access token with appropriate permissions
Setup
Replace 'your_access_token_here' in the access_token variable with your actual access token.
Modify the headers variable with your access token as needed.
Install the Requests library using npm install requests.
Usage
Uploading a File
To upload a file, call the uploadFile function with the following arguments:
repoName: The name of the GitHub repository where you want to upload the file.
filePath: The path of the file you want to upload.
commitMessage: The commit message to use for the upload.
Example:
uploadFile('your_repo_name_here', '/path/to/your/file.txt', 'Adding new file')
Creating a Directory
To create a directory, call the createDirectory function with the following arguments:
repoName: The name of the GitHub repository where you want to create the directory.
directoryPath: The path of the directory you want to create.
commitMessage: The commit message to use for the directory creation.
Example:
createDirectory('your_repo_name_here', 'new_directory', 'Creating new directory')
Deleting a File or Directory
To delete a file or directory, call the deleteFileOrDirectory function with the following arguments:
repoName: The name of the GitHub repository where the file/directory is located.
filePath: The path of the file/directory you want to delete.
commitMessage: The commit message to use for the deletion.
Example:
deleteFileOrDirectory('your_repo_name_here', 'path/to/your/file.txt', 'Deleting file.txt')
Notes
The getFileSha function is used internally to retrieve the SHA-1 hash of a file. It is not intended to be called directly.
The uploadFile function uses the base64 encoding of the file contents to create the file on GitHub.
The createDirectory function creates an empty file with the name of the directory as a placeholder.
The deleteFileOrDirectory function can be used to delete both files and directories.
Be sure to handle any errors or exceptions that may occur during the execution of these functions.
Always double-check the repository name, file/directory path, and commit message before executing any function.
Make sure to use the tool responsibly and only on systems where you have permission to do so.
