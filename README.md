# Weather Application

This is a Django-based web application that allows users to check the current weather conditions for any city using an external weather API.

## Features
- Search for current weather by city name.
- Display temperature, humidity, weather description, and more.
- User-friendly interface.

---

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Python 3.8 or higher**
- **Django 4.0 or higher**
- **pip** (Python package manager)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/weather-app.git
   cd weather-app
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the weather API key:**
   - Register for a free API key from [OpenWeatherMap](https://openweathermap.org/api).
   - Create a `.env` file in the project root directory and add the following line:
     ```env
     WEATHER_API_KEY=your_openweathermap_api_key
     ```

5. **Run database migrations:**
   ```bash
   python manage.py migrate
   ```

## Running the Application

1. **Start the development server:**
   ```bash
   python manage.py runserver
   ```

2. **Access the application:**
   Open your web browser and navigate to [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

## Project Structure

```
weather-app/
├── manage.py
├── weather_app/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   ├── asgi.py
├── templates/
│   ├── base.html
│   ├── index.html
├── static/
│   ├── css/
│   │   ├── styles.css
│   ├── js/
│       ├── scripts.js
├── .env
├── requirements.txt
└── README.md
```

## How It Works

1. **Frontend**
   - Users enter a city name into the search bar.
   - Weather information is fetched and displayed using the API response.

2. **Backend**
   - Django handles routing and API communication.
   - The `requests` library is used to fetch weather data from OpenWeatherMap.

## Dependencies
- Django
- requests
- python-dotenv

## Deployment (Optional)

To deploy this application to a production environment, follow these steps:

1. Configure your settings for production by editing `settings.py`:
   - Use a secure `SECRET_KEY`.
   - Set `DEBUG = False`.
   - Add allowed hosts in `ALLOWED_HOSTS`.

2. Use a WSGI server like Gunicorn:
   ```bash
   pip install gunicorn
   gunicorn weather_app.wsgi
   ```

3. Serve static files using a web server like Nginx.

---

## Troubleshooting

- **API key errors:** Ensure the `.env` file contains a valid API key.
- **Module errors:** Verify all dependencies are installed using `pip freeze`.

---

## License

This project is licensed under the MIT License.

## Contributions

Feel free to fork this repository and submit pull requests for improvements or bug fixes. For major changes, please open an issue first to discuss what you would like to change.

---

Happy coding!
