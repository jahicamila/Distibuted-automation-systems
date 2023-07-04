This project shows how to make a web server with an ESP8266 NodeMCU board that displays a web page with multiple sliders. 

The sliders control the duty cycle of different PWM signals to control the brightness of multiple LEDs. Instead of LEDs, this project can also be used to control DC motors or other actuators that require a PWM signal. 

Communication between clients and the ESP8266 is done using the WebSocket protocol. Additionally, whenever a change occurs, all clients update their slider values simultaneously.

Through the WebSocket communication protocol, several clients can be simultaneously connected to the server without blocking each other. It is shown that, unlike HTTP, the WebSocket server automatically updates the web page to all clients.

The server (ESP) receives the number of sliders and the corresponding value and adjusts the PWM duty cycle accordingly. In addition, it also informs all other clients of the new current slider values.

The following files are used to build the web server:
1.  Arduino sketch that handles the web server;
2.  index.html: to define the content of the website;
3.  sytle.css: for styling the website;
4.  script.js: for programming the website's behavior - handling what happens when the slider is moved, sending, receiving and interpreting messages received via the WebSocket protocol.

To transfer the HTML, CSS and JavaScript files needed to build this project to the ESP8266 flash memory (LittleFS), the VS Code plugin with the extension PlatformIO: LittleFS Filesystem uploade (upload files to the filesystem) was used.
