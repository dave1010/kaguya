# Kaguya

Kaguya is a ChatGPT plugin that allows you to load and edit your local files in a controlled way, as well as run any Python, JavaScript, and bash script. This makes it a powerful tool for developers, enabling them to interact with their file system and run scripts directly from ChatGPT.

## Demo

Here are the demo videos of Kaguya: 

https://github.com/ykdojo/kaguya/assets/107422421/c580a6f6-5f08-43fd-ac8b-c12a319e1534

https://github.com/ykdojo/kaguya/assets/107422421/d61b8ff1-2dbd-4eb4-b1b5-45d43797ddaa

## API Endpoints

The project provides several API endpoints that allow you to interact with the file system. The API is described in the `openapi.yaml` file. Here is a brief overview:

- `POST /api/executeCommand`: Execute a shell command.
- `GET /api/listFilesInDirectory`: List files and directories in the specified directory.
- `GET /api/readFile`: Read the content of a file in the user's directory.
- `POST /api/update`: Update a file in the user's directory by performing a search-and-replace operation.
- `POST /api/updateWholeFile`: Replace the entire content of a file in the user's directory.
- `POST /api/createFile`: Create a new file.
- `POST /api/deleteFile`: Delete a file in the user's directory.
- `POST /api/renameFile`: Rename a file in the user's directory.
- `POST /api/appendToFile`: Append content to the end of an existing file.
- `POST /api/createDirectory`: Create a new directory.
- `POST /api/deleteDirectory`: Delete a directory and its contents.
- `POST /api/readMultipleFiles`: Read the content of multiple files.

## Running the Project

You can run the project using Docker. Simply execute the `docker.sh` script:

```bash
docker.sh
```

After running the script, you can interact with Kaguya through ChatGPT using the localhost port 3000.

## Tips

- Best to keep each file under 100 lines of code, particularly for writing
- Writing more than ~80 lines of code at once is not recommended. It's slow and it might not even be able to finish the task.
- You can have it read more code though. However, reading more than 500-600 lines of code at once is not recommended.
- If the target file you want to edit is long, you may want to explicitly ask it to use search and replace.
- It may not get the intention of your instructions right away. It's meant to be a conversational tool.
- If the assistant starts hallucinating, it may be helpful to start a new conversation or limit the length of each file being loaded.

## Discord

Join our Discord server [here](https://discord.com/invite/nNtVfKddDD).

## License 

This project is licensed under the terms of the MIT license ©2023.

For the full license text, please see the [LICENSE](./LICENSE) file.
