# ![Consuming an API Lab - Exercise](./assets/hero.png)

For this lab you will be constructing a simple Express server that makes a call to a 3rd party API and renders some data from that call in the browser.

## Instructions

1. Create your `index.ejs` template:

  - Create a `views` folder in the root of this lab.
  - Create an `index.ejs` in the `views` folder
  - Open `views/index.ejs` in your text editor and add the boilerplate HTML to it.
	- Add a link with the text `Get a cat fact` that points to the route `/cats/fact`.

2. Create the `/` route:

  - In `server.js` create a GET route for `/`.
  - In the route handler, make the response render the `index.ejs` file.

3. Create the `/cats/fact` route:

	- In `server.js`, create a GET route for `/cats/fact`.
	- In the route handler, make a GET request to the API endpoint `https://catfact.ninja/fact` using the axios dependency.

4. Render the `cat/fact.ejs` template:

	- Create a new file `views/cat/fact.ejs`.
	- In this template, display the text of the cat fact received from the API response.
	- Add a link with the text Get another cat fact! that points to the route `/cats/fact`.

5. Handle the request and response:

	- In the route handler for `/cats/fact`, process the API response and extract the cat fact text.
	- Render the `cat/fact.ejs` template with the cat fact data.

6. Test your app:

	- Start the server: `nodemon server.js`
	- Open your browser and go to `http://localhost:3000`.
	- Click on the `Get a cat fact` link and verify that you see a cat fact displayed on the page.
	- Click on the `Get another cat fact!` link to fetch and display a new cat fact.
