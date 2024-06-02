# ![Consuming an API Lab - Setup](./assets/hero.png)

## Setup

Open your Terminal application and navigate to your `~/code/ga/labs` directory:

```bash
cd ~/code/ga/labs
```

Make a new repository on [GitHub](https://github.com/) named `consuming-an-api-lab`.

Clone a copy of your remote repo locally by using the `git clone` command:

```bash
git clone https://github.com/<your-username>/consuming-an-api-lab.git
```

> 🚨 Do not copy the above command. It will not work. Your GitHub username will replace <github-username> (including the < and >) in the URL above.

Next, `cd` into your new cloned directory, `consuming-an-api-lab`:

```bash
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

You will need to install three dependencies for this exercise: Express, EJS, and Dotenv.

```bash
npm i express ejs dotenv
```

Open the project's folder in VS Code:

```bash
code .
```
