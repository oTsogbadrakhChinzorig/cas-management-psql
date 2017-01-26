CAS Services Management Overlay
============================

This is the example cofiguration for CAS management DEMO application.

Services management web application Maven overlay for CAS with externalized configuration.


# Versions

```xml
<cas.version>5.0.x</cas.version>
```

# Requirements

* JDK 1.8+

# Build

To see what commands are available to the build script, run:

```bash
./build.sh help
```

To package the final web application, run:

```bash
./build.sh package
```

To update `SNAPSHOT` versions run:

```bash
./build.sh package -U
```

## Note

If you are running the management web application on the same machine as the CAS server web application itself, 
you will need to eveluate the "build.sh" build script and make sure the configuration files don't override each other.

```bash
# build.sh
...
 package && java -Xdebug -Xrunjdwp:transport=dt_socket,address=5XXX,
...
```

# Deployment

## Embedded Tomcat

CAS will be available at:

* `http://cas.server.name:8080/cas-management`
* `https://cas.server.name:8443/cas-management`

## External

Deploy resultant `target/cas-management.war`  to a servlet container of choice.
