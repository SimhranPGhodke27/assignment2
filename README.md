# MyAPI Project

This README provides instructions for setting up and running the MyAPI application. Follow these steps to get the project up and running on your local machine.

## 1. Set Up Your Development Environment

### Install Go
- Download and install the latest version of Go from the [official Go website](https://golang.org/dl/).

### Set Up Your Workspace
- Go Modules are now the standard for managing dependencies, so you don’t need a specific GOPATH. Ensure that your Go environment is properly configured to use Go Modules.

## 2. Project Setup

1. **Create a Project Directory**
   - Create a folder named `myapi` in your local directory.

2. **Download Repository Files**
   - Download all the files from this repository into the newly created `myapi` folder.

3. **Open Command Prompt and Navigate to Project Directory**
   - Open Command Prompt on your computer.
   - Change the directory to the `myapi` project folder using the following command:

     ```bash
     cd your\projectdirectory\myapi
     ```

4. **Run the API Server**
   - Start the API server by running the following command:

     ```bash
     go run main.go
     ```

   - You should see the message: `Server is running on http://localhost:8080`.

5. **Open Another Command Prompt**
   - Open a new Command Prompt window.
   - Navigate to the `myapi` directory again using the same command:

     ```bash
     cd your\projectdirectory\myapi
     ```

## 3. Manage Users

You can now perform operations to view, retrieve, add, and delete users using the following commands:

- **To View Existing Users:**

  ```bash
  curl http://localhost:8080/users
  ```

- **To Retrieve a Particular User:**

  ```bash
  curl "http://localhost:8080/user?id=id"
  ```

  Replace `id` with the actual user ID you want to retrieve.

- **To Add a New User:**

  ```bash
  curl -X POST http://localhost:8080/users -d "{\"name\": \"New User Name\"}" -H "Content-Type: application/json"
  ```

  Replace `"New User Name"` with the desired name of the new user.

- **To Delete a User:**

  ```bash
  curl -X DELETE "http://localhost:8080/users?id=id"
  ```

  Replace `id` with the actual user ID you want to delete.

## 4. Exit the API Server

- To stop the API server, press `Ctrl+C` in the Command Prompt window where the server is running.
