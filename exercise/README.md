# ![Consuming an API Lab - Exercise](./assets/hero.png)

In this lab, we'll practice making requests to a 3rd party API to display weather forecast data in the browser using Express and EJS. You'll practice working with routes, gathering user data, and integrating API responses into the UI of your application.

## Set up your account

For this lab, we'll be using the [Open Weather Map API](https://home.openweathermap.org/). 

Follow these simple steps to get started:

- Sign up for a free account on [Open Weather Map](https://home.openweathermap.org/users/sign_up).
- Once signed up, you'll receive an API key. Don't forget to copy this key into your `.env` file for future use.
- Test your API key by making a test call to the Open Weather Map URL in your browser.

Consult the Open Weather Map Documentation for how to set up your base URL:

```text
api.openweathermap.org/data/2.5/weather?zip=[ZIP CODE],us&units=imperial&appid=[API KEY]
```

## Set up your application

### Create your `index.ejs` template

- Create a `views` folder in the root of this lab.
- Create an `index.ejs` in the `views` folder.
- Open `views/index.ejs` and add the following:
  - Create a form that collects the zip code from the user.
  - The form should have an input field for the zip code and a submit button.
  - Ensure the form submits a `POST` request to the `/weather` route.

### Handle the request and response

- In `server.js`, create a `POST` route for `/weather`.
- In the route handler for `POST` `/weather`, obtain the zip code from the request body.
- Use the `zip code` and `API key` to make a request to the `Open Weather Map API`.
- Once the weather data is received, redirect to the `/weather/show` route with the weather data.

### Render the `/weather/show.ejs` template

- Create a new file `views/weather/show.ejs`.
- In this template, display:
  - The name of the city.
  - The current temperature.
  - The current weather description.
  - A link with the text `Back to home!` that points to the route `/`.

### Test your app

- Start the server: `nodemon server.js`.
- Open your browser and go to `http://localhost:3000`.
- Verify that you are redirected to the show page and see the weather data displayed.
- Click on the `Back to home!` link to return to the main page.

### Bonus

Try the following bonus challenges if you're up for it!

- Add some style with CSS!
- Add a five day forecast with their [5 day forecast endpoint](https://openweathermap.org/forecast5).
- Include the sunrise and sunset times (hint: [Moment.js](https://momentjs.com/) may be helpful!) and some information about humidity, atmospheric pressure, etc.
- Leverage Flexbox and media queries to build a mobile version
- Add CSS Animation, images, etc.
