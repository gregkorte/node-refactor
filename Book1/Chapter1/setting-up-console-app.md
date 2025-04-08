# Intro to working with Node.js in VS Code

### Using the Node.js to create and run programs
It's time to embark on your first program creation journey! When you installed Node.js, it came with the Node.js runtime and npm (Node Package Manager). npm includes many commands that are helpful for creating, building, and running Node.js applications. Anytime you want to run a command using npm in your terminal, it will always start with `npm`, followed by one or more subcommands. For instance, `npm init` is used to create a new Node.js project and initialize a `package.json` file.

> <sub>You've already familiarized yourself with other CLIs (Command Line Interfaces) during the front-end portion of the course. For instance, `npm` enabled you to create a Node project, which generated a `package.json` file and facilitated dependency management via `npm install`. Just as `create-react-app` offered a pre-configured React application as a template, npm provides tools to help scaffold and manage your Node.js applications efficiently.</sub>

#### Steps to set up a new Node.js/TypeScript application:

In this section, we use a shell script to automate the setup process for a new Node.js application. Unlike other frameworks, which provide built-in commands for creating, building, and running projects, Node.js does not have a single command-line interface or built-in tools for creating project structures, setting up configuration files, or managing development workflows.

Therefore, by using a shell script, we can streamline the setup process and ensure consistency across projects by automating tasks such as project initialization, dependency installation, and configuration file creation. This approach saves time and reduces the likelihood of manual errors, especially when setting up multiple projects or collaborating with a team. Additionally, it provides a convenient way to document and share the setup process with others.

1. Save the following script as `setup-nodejs-app.sh` in your root _node/server-side/workspace_ directory. Just make sure this is the directory where you want your project directory created!

    ```sh
    #!/bin/bash

    # Prompt the user for a project name
    read -p "Enter your project name: " project_name

    # Create project directory
    mkdir $project_name
    cd $project_name

    # Initialize a new Node.js project
    npm init -y

    # Create index.js with a simple Hello World program
    echo "console.log('Hello, World!');" > index.js

    # Create .vscode directory
    mkdir .vscode

    # Create launch.json configuration file
    cat <<EOL > .vscode/launch.json
    {
      "version": "0.2.0",
      "configurations": [
        {
          "type": "node",
          "request": "launch",
          "name": "Launch Program",
          "skipFiles": ["<node_internals>/**"],
          "program": "\${workspaceFolder}/index.js",
          "console": "integratedTerminal"
        }
      ]
    }
    EOL

    echo "Setup complete. Open the project in VS Code with 'code .'"
    ```

2. Give the script executable permissions by running:
    ```sh
    chmod +x setup-nodejs-app.sh
    ```

3. Run the script with:
    ```sh
    ./setup-nodejs-app.sh
    ```

4. Enter your desired project name when prompted.

5. `cd` into the directory you just created.

6. Open the project in VS Code with `code .`

7. Open the integrated terminal in VS Code (you can do this by selecting `Terminal` > `New Terminal` from the top menu).

8. In the terminal, make sure you're in the project directory you created, and then run `node index.js`. You should see "Hello, World!" printed in the terminal, and nodemon will watch for any file changes to restart the application automatically.

Congratulations! You've set up and run your first Node.js application with nodemon.

>**Follow this entire checklist every time you create a new console application for this course.**

#### What did we just do?
The `node_modules` folder that you see in the project contains all the packages that are installed by npm. *During this course, you should not need to edit or touch any of the files in this folder, and it should always be gitignored*.

We can use npm commands to start different types of projects, but for now, we focused on initializing a basic Node.js application. The `npm init -y` command created a `package.json` file, which includes metadata about our project and manages its dependencies. It's important to include a `.gitignore` file in your project to avoid committing unnecessary files to your repository. You can create a `.gitignore` file manually or use a template to exclude files like `node_modules`.

The `.vscode` folder includes configuration files for VS Code to run your project and use the debugger (we'll go in-depth on that in a few chapters). Setting `"console": "integratedTerminal"` in your `launch.json` allows you to interact with the program from the command line while it is running (to give it user input, for example).

Finally, running `node index.js` will execute our code in the Node.js runtime. `index.js` is the entry point for our application, similar to `main.js` or `Program.cs` in other languages. The program starts at the top of this file and executes line by line. Once the program runs out of code to execute, it will exit. Later on, we'll add more files, but this is all you need to know for now!

Up Next: [User Interaction in the Console and working with strings](./interacting-with-console.md)