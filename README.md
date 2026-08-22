# 🌦️ Weather App

A clean, responsive, and interactive **Weather Application** built with **HTML, CSS, and Vanilla JavaScript**.

The application uses the **OpenWeatherMap API** to fetch real-time weather information for any searched city and displays useful weather details including **temperature, humidity, wind speed, and weather conditions** with dynamic weather icons.

---

## 📌 About the Project

**Weather App** is a simple frontend project created to demonstrate how JavaScript can interact with an external API and dynamically update webpage content.

Users can enter the name of a city, and the application fetches the latest weather data using the **OpenWeatherMap Current Weather API**.

The interface is designed around a modern weather card with a gradient background, custom weather icons, and a simple search experience.

---

## ✨ Features

* 🔎 Search weather by **city name**
* 🌡️ View current temperature in **Celsius (°C)**
* 💧 Display current **humidity percentage**
* 💨 Display wind speed in **km/h**
* ☁️ Dynamic weather icons based on current conditions
* 🌧️ Supports multiple weather conditions
* ⌨️ Search using both the **Search button** and **Enter key**
* ❌ Displays an error message for an invalid city
* ⚡ Fetches live weather information using an API
* 🎨 Modern gradient-based weather card UI
* 📱 Responsive layout for different screen sizes

---

## 🌤️ Supported Weather Conditions

The application dynamically changes the weather icon depending on the weather returned by the API.

Currently supported conditions include:

| Weather Condition | Icon          |
| ----------------- | ------------- |
| ☀️ Clear          | `clear.png`   |
| ☁️ Clouds         | `clouds.png`  |
| 🌧️ Rain          | `rain.png`    |
| 🌦️ Drizzle       | `drizzle.png` |
| 🌫️ Mist          | `mist.png`    |

---

## 🛠️ Tech Stack

| Technology             | Usage                                                |
| ---------------------- | ---------------------------------------------------- |
| **HTML5**              | Structure and content of the application             |
| **CSS3**               | Layout, styling, gradient UI and responsive design   |
| **JavaScript (ES6+)**  | Application logic, DOM manipulation and API handling |
| **Fetch API**          | Sending asynchronous requests to the weather API     |
| **OpenWeatherMap API** | Retrieving real-time weather information             |

---

## 📂 Project Structure

```text
Weather/
│
├── images/
│   ├── search.png
│   ├── clear.png
│   ├── clouds.png
│   ├── rain.png
│   ├── drizzle.png
│   ├── mist.png
│   ├── humidity.png
│   └── wind.png
│
├── index.html
├── style.css
└── README.md
```

### Files

**`index.html`**

Contains the main structure of the Weather App along with the JavaScript responsible for:

* Fetching weather data
* Searching cities
* Updating weather information
* Handling invalid city names
* Switching weather icons
* Handling keyboard input

**`style.css`**

Contains all application styling, including:

* Weather card design
* Gradient background
* Search bar styling
* Weather information layout
* Humidity and wind sections
* Error message styling

**`images/`**

Contains all icons used by the application for search, weather conditions, humidity, and wind speed.

---

## ⚙️ How It Works

The application follows a simple workflow:

1. The user enters a city name in the search field.
2. The user clicks the **Search button** or presses **Enter**.
3. JavaScript calls the `checkWeather()` function.
4. A request is sent to the **OpenWeatherMap API** using the Fetch API.
5. The API returns the current weather data for the requested city.
6. JavaScript extracts the required information from the API response.
7. The webpage dynamically displays:

   * City name
   * Temperature
   * Humidity
   * Wind speed
   * Weather icon
8. If the city cannot be found, an **Invalid city name** message is displayed.

---

## 🌐 API Integration

This project uses the **OpenWeatherMap Current Weather API**.

The API request follows this format:

```text
https://api.openweathermap.org/data/2.5/weather?units=metric&q=CITY_NAME&appid=YOUR_API_KEY
```

The `units=metric` parameter returns the temperature in **Celsius**.

JavaScript retrieves data such as:

```javascript
data.name
data.main.temp
data.main.humidity
data.wind.speed
data.weather[0].main
```

The application then uses these values to update the interface dynamically.

---

## 💨 Wind Speed Conversion

OpenWeatherMap returns wind speed in **meters per second (m/s)**.

The application converts it into **kilometers per hour (km/h)** using:

```javascript
Math.round(data.wind.speed * 3.6)
```

So the wind information is displayed in a more familiar format:

```text
15 km/h
```

---

## 🚀 Getting Started

To run this project on your local machine, follow these steps.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

### 2. Open the Project Directory

```bash
cd YOUR_REPOSITORY
```

### 3. Configure Your API Key

Create a free account on **OpenWeatherMap** and generate an API key.

Inside the JavaScript section of `index.html`, replace:

```javascript
const apiKey = "YOUR_API_KEY";
```

with your own API key.

### 4. Run the Application

Open:

```text
index.html
```

in your browser.

For development, you can also run the application using the **Live Server** extension in Visual Studio Code.

---

## 🔐 API Key Security

Avoid committing your real API key to a public GitHub repository.

For learning projects, keeping the API request in frontend JavaScript is common, but the key will be visible to anyone who opens the source code.

For production applications, consider moving API requests to a backend or serverless function and storing API credentials securely using environment variables.

---

## 💻 Usage

Using the application is simple:

1. Open the Weather App.
2. Enter a city name, for example:

```text
Jalandhar
```

3. Click the search icon or press **Enter**.
4. The latest weather information will appear on the card.

For example:

```text
Jalandhar

22°C

Humidity: 50%
Wind Speed: 15 km/h
```

---

## ❌ Error Handling

If the entered city is not available and the API returns a `404` response, the application hides the weather section and displays:

```text
Invalid city name
```

When a valid city is searched again, the error message automatically disappears and the weather information is displayed.

---

## 🎨 UI Design

The application uses a minimal card-based interface with a gradient background:

```css
linear-gradient(135deg, #00feba, #56548a)
```

The UI includes:

* Rounded weather card
* Rounded search input
* Circular search button
* Large temperature display
* Dynamic weather icon
* Dedicated humidity and wind sections
* Dark page background

---

## 📸 Project Preview

Add a screenshot of your Weather App inside the `images` folder and use:

```md
![Weather App Preview](images/screenshot.png)
```

Then GitHub will automatically display the project screenshot inside the README.

---

## 🔮 Future Improvements

Some useful features that can be added in future versions:

* [ ] 5-day weather forecast
* [ ] Hourly weather forecast
* [ ] Detect weather using current location
* [ ] Search history
* [ ] Recently searched cities
* [ ] Sunrise and sunset information
* [ ] Feels-like temperature
* [ ] Atmospheric pressure
* [ ] Visibility information
* [ ] °C / °F temperature toggle
* [ ] Dark and light theme
* [ ] Loading indicator while fetching data
* [ ] More weather condition icons
* [ ] Improved API error handling

---

## 🤝 Contributing

Contributions are welcome.

If you want to improve this project:

1. Fork the repository.
2. Create a new feature branch.

```bash
git checkout -b feature/your-feature-name
```

3. Make your changes.
4. Commit your changes.

```bash
git commit -m "Add new feature"
```

5. Push your branch.

```bash
git push origin feature/your-feature-name
```

6. Open a **Pull Request**.

---

## 👨‍💻 Author

**Your Name**

GitHub: `@FusionXstore`

---

## ⭐ Support

If you found this project useful or liked the application, consider giving the repository a **⭐ Star**.

It helps support the project and motivates further improvements.

---

## 📄 License

This project is available for **educational and personal use**.

---

### 🌦️ Built with HTML, CSS, JavaScript & OpenWeatherMap API

