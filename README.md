This project shows how to make a web server with an ESP8266 NodeMCU board that displays a web page with multiple sliders. The sliders control the duty cycle of different PWM signals to control the brightness of multiple LEDs. Instead of LEDs, this project can also be used to control DC motors or other actuators that require a PWM signal. Communication between clients and the ESP8266 is done using the WebSocket protocol. Additionally, whenever a change occurs, all clients update their slider values simultaneously.

Through the WebSocket communication protocol, several clients can be simultaneously connected to the server without blocking each other. It is shown that, unlike HTTP, the WebSocket server automatically updates the web page to all clients.

The user moves the slider to adjust the brightness value. The slider can have a minimum value of 0 and a maximum value of 100% which shows the highest brightness. The brightness value shows the duty cycle percentage.

The server (ESP) receives the number of sliders and the corresponding value and adjusts the PWM duty cycle accordingly. In addition, it also informs all other clients of the new current slider values.

To transfer the HTML, CSS and JavaScript files needed to build this project to the ESP8266 flash memory (LittleFS), the VS Code plugin with the extension PlatformIO: LittleFS Filesystem uploade (upload files to the filesystem) was used.

The following files are used to build the web server:
• Arduino sketch that handles the web server;
• index.html: to define the content of the website;
• sytle.css: for styling the website;
• script.js: for programming the website's behavior - handling what happens when the slider is moved, sending, receiving and interpreting messages received via the WebSocket protocol.
