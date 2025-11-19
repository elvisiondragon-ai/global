# How to Run this Project Locally

To run this project locally and view `index.html` in your browser, follow these steps:

1.  **Initial State:** The `package.json` file initially did not contain any scripts for running a local development server.

2.  **Install `serve`:** I installed `serve` as a development dependency. `serve` is a static file serving utility that is lightweight and easy to use.
    ```bash
    npm install serve --save-dev
    ```

3.  **Update `package.json`:** I then updated the `package.json` file to include `start` and `dev` scripts. These scripts tell npm to use the `serve` command to serve the current directory (`.`).
    ```json
    {
      "private": true,
      "scripts": {
        "start": "serve .",
        "dev": "serve ."
      },
      "dependencies": {
        "@vercel/edge": "^0.1.2"
      },
      "devDependencies": {
        "serve": "^14.2.1"
      }
    }
    ```

4.  **Run the Development Server:** Now, you can start the local development server by running either of the following commands in your terminal:
    ```bash
    npm start
    # or
    npm run dev
    ```
    After running the command, `serve` will typically provide you with a local address (e.g., `http://localhost:3000` or `http://localhost:5000`) where you can access your `index.html` file in your web browser.