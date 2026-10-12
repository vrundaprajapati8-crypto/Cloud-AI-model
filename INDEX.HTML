<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Weather Prediction</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #74ebd5, #ACB6E5);
      text-align: center;
      padding: 30px 15px;
      margin: 0;
    }
    .container {
      max-width: 420px;
      margin: 30px auto;
      padding: 25px;
      background: white;
      border-radius: 15px;
      box-shadow: 0 4px 15px #0002;
    }
    input, button {
      padding: 12px;
      margin: 7px 0;
      width: 90%;
      box-sizing: border-box;
      border-radius: 7px;
      font-size: 16px;
    }
    input { border: 1px solid #aaa; }
    button {
      background: #1769aa;
      color: white;
      border: none;
      cursor: pointer;
    }
    #result { margin-top: 20px; line-height: 1.8; }
  </style>
</head>
<body>
  <div class="container">
    <h1>Weather Prediction</h1>
    <p>Check the current weather of any city.</p>

    <input id="city" type="text" placeholder="Enter city name"
           value="Ahmedabad">
    <button onclick="getWeather()">Check Weather</button>

    <div id="result">Weather details will appear here.</div>
  </div>

  <script>
    async function getWeather() {
      const city = document.getElementById("city").value.trim();
      const result = document.getElementById("result");

      if (!city) {
        result.textContent = "Please enter a city name.";
        return;
      }

      result.textContent = "Loading weather...";

      try {
        const geoResponse = await fetch(
          "https://geocoding-api.open-meteo.com/v1/search?name=" +
          encodeURIComponent(city) + "&count=1&language=en&format=json"
        );

        if (!geoResponse.ok) throw new Error("Location service unavailable.");

        const geoData = await geoResponse.json();

        if (!geoData.results || geoData.results.length === 0) {
          throw new Error("City not found. Please try another city.");
        }

        const place = geoData.results[0];
        const weatherResponse = await fetch(
          "https://api.open-meteo.com/v1/forecast?latitude=" +
          place.latitude + "&longitude=" + place.longitude +
          "&current=temperature_2m,relative_humidity_2m,apparent_temperature," +
          "wind_speed_10m,weather_code&timezone=auto"
        );

        if (!weatherResponse.ok) throw new Error("Weather service unavailable.");

        const data = await weatherResponse.json();
        const w = data.current;

        const descriptions = {
          0: "Clear sky", 1: "Mainly clear", 2: "Partly cloudy",
          3: "Overcast", 45: "Fog", 48: "Rime fog",
          51: "Light drizzle", 53: "Moderate drizzle", 55: "Dense drizzle",
          61: "Light rain", 63: "Moderate rain", 65: "Heavy rain",
          71: "Light snow", 73: "Moderate snow", 75: "Heavy snow",
          80: "Rain showers", 81: "Moderate rain showers",
          82: "Heavy rain showers", 95: "Thunderstorm"
        };

        result.innerHTML =
          "<h2>" + place.name + ", " + (place.country || "") + "</h2>" +
          "<h3>" + (descriptions[w.weather_code] || "Weather conditions") + "</h3>" +
          "<p>Temperature: " + w.temperature_2m + " °C</p>" +
          "<p>Feels Like: " + w.apparent_temperature + " °C</p>" +
          "<p>Humidity: " + w.relative_humidity_2m + "%</p>" +
          "<p>Wind Speed: " + w.wind_speed_10m + " km/h</p>" +
          "<p><small>Live weather data</small></p>";
      } catch (error) {
        result.textContent = error.message ||
          "Unable to load weather. Please try again.";
      }
    }

    getWeather();
  </script>
</body>
</html>
