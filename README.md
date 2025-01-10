# Real-Time Vehicle Tracking System Using SIM808 and Arduino

This project is a real-time vehicle tracking system utilizing the SIM808 GPS module, Arduino, and a dynamic web application. The system tracks the vehicle's location and displays it on an interactive map, updating every few seconds.

## Features
- **Real-Time Tracking**: Displays the current location of the vehicle on an interactive map.
- **Web Integration**: A dynamic map interface built using Leaflet.js.
- **Road Details**: Fetches and displays the nearest road name using OpenStreetMap's Nominatim API.
- **User Locator**: Allows users to locate themselves on the map.
- **Directions**: Provides routing directions from the user's location to the vehicle.

## Technologies Used

### Hardware
- Arduino UNO or compatible microcontroller
- SIM808 GPS/GPRS module
- Power supply and GSM-enabled SIM card

### Software
- **Frontend**: HTML, CSS, JavaScript, Leaflet.js
- **Backend**: PHP, MySQL
- **Arduino IDE**: For programming the microcontroller

## How It Works
1. **Data Collection**:  
   The SIM808 module fetches GPS coordinates and sends them to the server using HTTP POST requests via the Arduino.

2. **Data Storage**:  
   A PHP script stores the coordinates in a MySQL database.

3. **Data Retrieval**:  
   Another PHP script fetches the latest coordinates from the database for the web interface.

4. **Map Rendering**:  
   The web application displays the vehicle's location on a map and updates it in real time.

## Installation

### Prerequisites

#### Hardware
- Arduino UNO or a compatible microcontroller.
- SIM808 GPS/GPRS Module for location tracking and data transmission.
- Power Supply for Arduino and SIM808.
- GSM-enabled SIM Card for communication with the server.
- Connecting Wires and a breadboard for circuit connections.

#### Software
- Arduino IDE: For programming the microcontroller.
- Web Server: Use XAMPP or LAMP.
- MySQL Database: For storing and retrieving location data.
- Web Browser: To access the real-time map interface.

### Steps

#### Clone the Repository
   ```bash
   git clone https://github.com/yourusername/vehicle-tracking-system.git
   cd vehicle-tracking-system
   ```

#### Configure the Server

1. **Import the Database**
   - Import the `database.sql` file into your MySQL database to set up the required tables.

2. **Update PHP Files**
   - Edit the `save_location.php` and `get_location.php` files to include your database credentials (e.g., host, username, password, and database name).

#### Upload Arduino Code

1. **Open the Sketch**
   - Open the Arduino sketch (provided in the repository) in the Arduino IDE.

2. **Configure Pins**
   - Set up the RX and TX pins in the sketch to match your hardware connections.

3. **Upload the Code**
   - Upload the sketch to your Arduino board.

#### Start the Web Application

1. **Place Files in the Web Server**
   - Copy the project files into the `htdocs` directory of your web server.

2. **Start the Server**
   - Start your web server (e.g., XAMPP or LAMP).

3. **Access the Application**
   - Open your browser and navigate to `http://localhost/map_display.html` to view the real-time map interface.

#### Run the System

1. **Power the Hardware**
   - Connect and power on the Arduino and SIM808 module.

2. **View Real-Time Tracking**
   - Open the web application to monitor the vehicle’s location in real time.

---

## Usage

1. Power on the Arduino and SIM808 module.
2. Open `map_display.html` in your browser to view the vehicle's location on the map.
3. Use the "Get Direction" button to find the route from your current location to the vehicle.

---

## Future Enhancements
- Develop a mobile app interface for better accessibility.
- Add SMS alerts for periodic location updates.
- Improve GPS accuracy with external antennas or advanced modules.

---

## Contributing
Feel free to fork this repository, submit issues, and create pull requests. Contributions are always welcome!


