# Project Setup

Follow these steps to set up your project:

1. Initialize a new npm project:
    ```sh
    npm init -y
    ```

2. Install TypeScript as a development dependency:
    ```sh
    npm i -D typescript
    ```

3. Install ts-node as a development dependency:
    ```sh
    npm i -D ts-node
    ```

4. Install nodemon as a development dependency:
    ```sh
    npm i -D nodemon
    ```

5. Create a `tsconfig.json` file with the following content:
    ```json
    {
        "compilerOptions": {
            "module": "NodeNext",
            "moduleResolution": "NodeNext",
            "baseUrl": "src",
            "outDir": "dist",
            "sourceMap": true,
            "noImplicitAny": true
        },
        "include": ["src/**/*"]
    }
    ```

6. Create a `nodemon.json` file with the following content:
    ```json
    {
        "watch": ["src"],
        "ext": ".ts,.js",
        "exec": "ts-node ./src/index.ts"
    }
    ```

7. Create a folder named `src` and add an `index.ts` file inside it.

8. Add the following line to the `scripts` section of your `package.json`:
    ```json
    "start": "nodemon"
    ```

9. Run the project:
    - Add a `console.log("something")` statement in `index.ts`.
    - Start the project by running:
        ```sh
        npm start
        ```
This will verify that the project is set up correctly.
