
The "googleinterface" integration package is placed inside the Leshan-server-demo module. The main class is GoogleInterface which creates an interface to Google and handles its requests. After the Leshan-Server-Demo initialization is completed, a GoogleInterface object is instantiated by running the protocol developed in the package.

The main server class is LeshanServerDemo.java

To connect to the Leshan Demo UI visit http://localhost:8080  

The package is developed into 3 subpackages:

	-data: maintains the data structures used by the program such as AuthToken data or configuration files.

	-protocol: maintains the protocols used by the service,    
     namely the management of Oauth2 and Google Smart Home.

	-integration: manages the conversion of devices and their interactions with the LwM2M server.

To register a new device, the Leshan-Client-Demo module must be used; the princiapal class of the module is LeshanClientDemo.java

Translated with www.DeepL.com/Translator (free version)

//////  UTILIZZO NGROK

To quickly test the server, the ngrok_start batch file available in this directory can be used. The batch runs the program ngrok.exe creating a tunnel to port 80(default port defined in the configuration file googleinterface/google_configuration/conf.json). 
Ngrok will provide two identical uri's, copy the https uri and use it on GoogleActions for the linking links contained in Develop/Actions(adding /smart) and Develop/Account Linking/OAuthClientInformation(adding /oauth and /token respectively). Starting the test, Google will forward requests to the links provided, which the ngrok tunnel software will route to interface 80 on the computer it is running on. DATA ARE CLEARLY NOT ACCEPTING HTTPS COMMUNICATIONS WITHOUT PAYING PREMIUM SUBSCRIPTION, Ngrok is only a solution suitable for testing.
