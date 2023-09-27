# Se20uari114_AI4104
Assignment 2
Hardware Setup
We established a connection between the Raspberry Pi and our computer using Real VNC Viewer. Both the Raspberry Pi and the computer were connected to the same Wi-Fi network to ensure communication.

We connected the DHT11 temperature sensor to the Raspberry Pi for data acquisition.

We developed a Python script that combines the functionality of the Adafruit_DHT library for reading sensor data and the pyrebase library for interacting with Firebase.

The script configured Firebase authentication by providing the API key, database URL, and storage bucket credentials obtained from the Firebase project.

Within the script, we set up the DHT11 sensor by specifying its type (DHT11) and the GPIO pin it was connected to on the Raspberry Pi.

In a continuous loop, the script read temperature and humidity data from the DHT11 sensor using the Adafruit_DHT.read_retry() function.

If valid data was obtained from the sensor, we formatted it and sent it to Firebase under a "Status" child node. We utilized the db.child("Status").push(data) method to push data to Firebase.

The script printed the sensor data to the console and indicated that it was successfully sent to Firebase.

