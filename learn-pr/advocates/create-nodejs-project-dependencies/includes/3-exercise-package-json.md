You're a Node.js developer at Tailwind Traders. Knowing how to set up a new Node.js project is an important skill to have. Setup includes generating a manifest file and creating some common scripts that you're likely to use throughout the project lifecycle.

## Open project in development container

#### [Remote development (browser)](#tab/github-codespaces)

1. Start the process to create a new GitHub Codespace on the `main` branch of the [`MicrosoftDocs/node-essentials`](https://github.com/MicrosoftDocs/node-essentials) GitHub repository.

    > [!div class="nextstepaction"]
    > [Open this project in GitHub Codespaces](https://github.com/codespaces/new?azure-portal=true&hide_repo_select=true&ref=main&repo=278117471)

1. On the **Create codespace** page, review the codespace configuration settings and then select **Create new codespace**

    :::image type="content" source="../media/codespaces/codespace-configuration.png" alt-text="Screenshot of the confirmation screen before creating a new codespace.":::

1. Wait for the codespace to start. This startup process can take a few minutes.

1. Open a new terminal in the codespace.

    > [!TIP]
    > You can use the main menu to navigate to the **Terminal** menu option and then select the **New Terminal** option.
    >
    > :::image type="content" source="../media/codespaces/open-terminal-option.png" lightbox="../media/codespaces/open-terminal-option.png" alt-text="Screenshot of the codespaces menu option to open a new terminal.":::

1. Validate that Node.js is installed in your environment:

    ```bash
    node --version
    ```

    The dev container uses a Node.js LTS version such as `v20.5.1`. The exact version might be different.

1. The remaining exercises in this project take place in the context of this development container.

#### [Local development (Docker)](#tab/visual-studio-code)


1. Open **Visual Studio Code** in the context of an empty directory.
1. Ensure that you have the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) installed in Visual Studio Code.
1. Open a new terminal in the editor.
    > [!TIP]
    > You can use the main menu to navigate to the **Terminal** menu option and then select the **New Terminal** option.
    >
    > :::image type="content" source="../media/codespaces/open-terminal-option.png" lightbox="../media/codespaces/open-terminal-option.png" alt-text="Screenshot of the menu option to open a new terminal.":::
1. Clone the [`MicrosoftDocs/node-essentials`](https://github.com/MicrosoftDocs/node-essentials) GitHub repository into the current directory.

    ```bash
    git clone https://github.com/MicrosoftDocs/node-essentials.git
    ```

1. Open the repository in code with the following commands in the terminal.

    ```bash
    cd node-essentials
    code .
    ```

1. Open the **Command Palette**, search for the **Dev Containers** commands, and then select **Dev Containers: Reopen in Container**.
    :::image type="content" source="../media/codespaces/reopen-container-command-palette.png" alt-text="Screenshot of the Command Palette option to reopen the current folder within the context of a development container.":::
    > [!TIP]
    > Visual Studio Code might automatically prompt you to reopen the existing folder within a development container. This is functionally equivalent to using the command palette to reopen the current workspace in a container.
    >
    > :::image type="content" source="../media/codespaces/reopen-container-toast.png" alt-text="Screenshot of a toast notification to reopen the current folder within the context of a development container.":::
1. Validate that Node.js is installed in your environment:

    ```bash
    node --version
    ```

    The dev container uses a Node.js LTS version such as `v20.5.1`. The exact version might be different.

1. The remaining exercises in this project take place in the context of this development container.

---

## Set up a new Node.js project

1. In the terminal, change to the folder that has the files for this exercise:

   ```bash
   cd node-dependencies/3-exercise-package-json
   ```

1. View the contents of the folder:

    ```bash
    ls -R
    ```

   In this folder, you should see a **src** subfolder with an **index.js** file:

   ```output
    ./src:
    index.js
   ```

1. Run the following command to initialize a Node.js project:

    ```bash
    npm init -y
    ```

   This command generates a **package.json** file that looks similar to this example:

    ```json
    {
      "name": "<your project>",
      "version": "1.0.0",
      "description": "",
      "main": "index.js",
      "dependencies": {},
      "devDependencies": {},
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "keywords": [],
      "author": "",
      "license": "ISC"
    }
    ```

1. Edit the package.json file and modify these property values:

    - `name`: "tailwind-trader-api"
    - `description`: "HTTP API to manage items from the Tailwind Traders database"
    - `main`: "index.js"
    - `keywords`: ["api", "database"]
    - `author`: "Sam"

   Your package.json file should now look like this code:

    ```json
    {
      "name": "tailwind-trader-api",
      "version": "1.0.0",
      "description": "HTTP API to manage items from the Tailwind Traders database",
      "main": "index.js",
      "dependencies": {},
      "devDependencies": {},
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "keywords": ["api", "database"],
      "author": "Sam",
      "license": "ISC"
    }
    ```

1. In the `scripts` section, add this definition for the `start` action before the definition for the `test` action:

   ```json
   "start": "node ./src/index.js",
   ```

   Save your changes and close the package.json file.

1. Start your project with the `start` action by entering this command:

   ```bash
   npm start
   ```

   You should see this output:

   ```output
   Welcome to this application
   ```

You now have a good file structure that you can build upon as your project grows. 