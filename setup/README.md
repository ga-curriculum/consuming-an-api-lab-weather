# ![Consuming an API Lab - Setup](./assets/hero.png)

Open your Terminal application and navigate to your `~/code/ga/labs` directory:


```bash
cd ~/code/ga/labs
```

Make a new directory called `consuming-an-api-lab`, then enter this directory:

```bash
mkdir consuming-an-api-lab
cd consuming-an-api-lab
```

In this directory create a `server.js` file:

```bash
touch server.js
```

Create a node project along with its `package.json` file by using this command:

```bash
npm init
```

During initialization, you will be prompted to customize your project and the `package.json` file.

At this point, accept the defaults (by simply just hitting `Return`/`Enter` for each prompt without adding any values), except for the entry point - set this to be `server.js`.

You will need to install three dependencies in order to get your code to work:  Express, EJS, and Axios.

```bash
npm i express ejs axios
```

Open the project's folder in VS Code:

```bash
code .
```
