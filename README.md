# Dockerized Minecraft Server

## How to use

Start this Docker image using `docker run`:

```
docker run --name minecraft-server -v /path/to/your/server-files:/opt/minecraft programie/minecraft-server
```

## Available environment variables

The following environment variables can be used to modify the behavior of the Minecraft server (passed using the `-e` or `--env` option of the `docker run` command):

| Variable | Description | Default value |
| --- | --- | --- |
| MINECRAFT_SERVER_JAR | The filename of the jar file in */opt/minecraft* used to start the Minecraft server | minecraft-server.jar |
| MINECRAFT_CMD_OPTS | Additional options passed to the Minecraft server | |
| JAVA_HEAP_MAX | The maximum heap size for the Java process (omit or set to an empty string to use the container limits) | |
| JAVA_HEAP_MIN | The minimum heap size for the Java process (only used if *JAVA_HEAP_MAX* has been defined) | |
| JAVA_OPTS | Additional options passed to the JVM before the *-jar* option | |
| JMXREMOTE_ENABLE | Enable remote control via JMX (e.g. to use with JConsole or VisualVM) | |
| JMXREMOTE_PORT | The port to use for JMX remote control | 3000 |
| JVMREMOTE_HOSTNAME | The hostname to which JConsole or VisualVM should connect to | localhost |