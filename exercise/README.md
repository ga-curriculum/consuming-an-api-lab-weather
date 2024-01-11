# ![Consuming an API Lab - Exercise](./assets/hero.png)

For this lab you will be constructing a simple Express server that makes a call to a 3rd party API and renders some data from that call in the browser.

For this assignment you'll be using the Open Weather Data API. In order to use it, please follow these steps:

- Sign up for a free [Open Weather Map](https://home.openweathermap.org/users/sign_up) account!
- Once you've signed up, you're given an API key. Copy that API key and keep track of it somewhere!
- Test the url in browswer to verify that your key works.

```
api.openweathermap.org/data/2.5/weather?zip=[ZIP CODE],us&units=imperial&appid=[API KEY]
```

> Make sure to remove the brackets around the API key and zip code!

## Instructions

### Step One: Create your `index.ejs` template:

- Create a `views` folder in the root of this lab.
- Create an `index.ejs` in the `views` folder
- Open `views/index.ejs` in your text editor and add the boilerplate HTML to it.
  - Add a link with the text `Get current weather` that points to the route `/weather`.

### Step Two: Create the `/` route:

- In `server.js` create a GET route for `/`.
- In the route handler, make the response render the `index.ejs` file.

### Step Three: Create the `/weather` route:

- In `server.js`, create a GET route for `/weather`.
- In the route handler, render the `/weather/index.ejs` template.

### Step Four: Render the `/weather/index.ejs` template:

- Create a new file `views/weather/index.ejs`.
- In this template, display an input filed for a suer to enter a zip code and a submit button.
- Add a link with the text `Back to home!` that points to the route `/`.

### Step Five: Handle the request and response:

- In `server.js`, create a POST route for `/weather`.
- In the route handler for POST `/weather`, use the request body to obtain the zip code.
- Using the zip code and the API key, make a request to the Open Weather Map API.
- Render the `/weather/show.ejs` template with the weather data.

### Step Six: Render the `/weather/show.ejs` template:

- Create a new file `views/weather/show.ejs`.
- In this template, display:
  - The name of the city
  - The current temperature
  - The current weather description
  - A link with the text `Back to home!` that points to the route `/`.

### Step Seven: Test your app:

- Start the server: `nodemon server.js`
- Open your browser and go to `http://localhost:3000`.
- Click on the `Get current weather` link and verify that you see an input field displayed on the page.
- Enter a zip code and click on the submit button and verify that you see the weather data displayed on the page.
- Click on the `Back to home!` link to see the main page again.

### Bonus

Try the following bonus challenge if you're up for it!

- Make it pretty with some more CSS!
- Add a five day forecast with their [5 day forecast endpoint](https://openweathermap.org/forecast5).
- Include the sunrise and sunset times (hint: maybe [Moment.js](https://momentjs.com/) will be helpful!) and some information about humidity, atmospheric pressure, etc.
- Use CSS Animation, images, etc. (think weather app)
- Leverage flexbox and use media queries to build a mobile version
