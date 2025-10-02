# Water Level Monitoring Dashboard

This project is a simple, single-page web application for monitoring water levels from a specific station. It provides real-time data visualization and alerts based on predefined thresholds.

## Features

*   **Real-time Water Level:** Displays the most recent water level reading.
*   **Historical Data Chart:** A line chart showing water level trends over time.
*   **Dynamic Data Loading:** Fetches and updates data automatically every minute.
*   **Alert System:** Shows different alert levels (Safe, Warning, Danger, Critical) based on the water level.
*   **Customizable Data View:** Allows the user to change the number of data points displayed on the chart.
*   **Responsive Design:** The layout adapts to different screen sizes.

## Setup and Usage

This is a single-file application and does not require a complex setup or build process.

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd <repository-directory>
    ```
3.  **Run a local web server:**
    Because of browser security policies (CORS) regarding local file access (`file:///...`), you need to serve the `index.html` file through a local web server.

    If you have Python installed, you can use its built-in HTTP server.

    For Python 3:
    ```bash
    python -m http.server
    ```

    For Python 2:
    ```bash
    python -m SimpleHTTPServer
    ```

    Alternatively, you can use other tools like `live-server` for Node.js:
    ```bash
    npm install -g live-server
    live-server
    ```

4.  **Open the application:**
    Open your web browser and navigate to the address provided by your local server (e.g., `http://localhost:8000` or `http://127.0.0.1:8080`).

## Technologies Used

*   **HTML5**
*   **CSS3**
*   **JavaScript (ES6 Modules)**
*   **Vue.js 3:** A progressive JavaScript framework for building user interfaces.
*   **Chart.js:** A flexible JavaScript charting library for designers & developers.
*   **Chart.js Plugin Zoom:** A plugin for Chart.js that adds zooming and panning capabilities.

## How it Works

The application fetches data by making a request to a Cloudflare Worker, which acts as a proxy to scrape the water level data from the source website (`phongchongthientaihanoi.com`). The data is then parsed, and the UI is updated reactively using Vue.js. The chart is rendered using Chart.js.