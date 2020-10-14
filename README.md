# try_load_tcp_client
This library allows you to create a stable client for connecting to the server over the TCP Protocol.
## 0. Adding permissions and dependencies.
For the library to work properly, you need to add permissions:  
```
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```
As well as you want to add a library of coroutines  
```
implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.7'
implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.0'
```
```
    repositories {
        google()
        jcenter()
    }
```
## 1. Creating a client and connecting to the server.
To connect to the server we need to create a client 
```
val client = Client()
```

Then connect to the server using the ip address and port of  
```
client.connect(address, port)
```

## 2. Subscribe to receive incoming data.
To subscribe to read incoming data, you need to create a class that will inherit from HandlerImp and then pass it to the addHandlers method.

## 3. Sending a message to the server.
To send a message to the server, you need to call the write method and pass the message to it.   
```
client.send("Hello")
```

## 4. Disconnecting from the server.
To disconnect from the server, call the disconnect method.  
```
client.disconnect()
```
