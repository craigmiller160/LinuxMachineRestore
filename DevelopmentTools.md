# Setup Development Tools

This is a guide for setting up the main development tools.

## OpenJDK

First, go to this link <a href="https://jdk.java.net/archive/">OpenJDK Downloads</a> and download the `Linux/x64` build of the correct OpenJDK version.

Then, create the OpenJDK directory with this command:

```
mkdir -p ~/Applications/OpenJDK
```

Next, copy the OpenJDK tar file to this location, unpack it, and delete the tar:

```
cp ~/Downloads/openjdk-*.tar.gz ~/Applications/OpenJDK
tar xvf ~/Applications/OpenJDK/openjdk-*.tar.gz -C ~/Applications/OpenJDK
rm ~/Applications/OpenJDK/*.tar.gz
```

Next, symlink the `latest` directory from the OpenJDK file.

```
ln -s ~/Applications/OpenJDK/jdk-* ~/Applications/OpenJDK/latest
```

Lastly, setup the necessary environment variables and `PATH` in the .bash_profile file.

```
# OpenJDK
openjdk=~/Applications/OpenJDK/latest
if [ -d $openjdk ]; then
	export JAVA_HOME=$openjdk
	PATH="$openjdk/bin:$PATH"
fi
```

## NodeJS

First, go to this link <a href="https://nodejs.org/en/download/current/">NodeJS Downloads</a> and download the current Linux x64 binary.

Then, create the NodeJS directory with this command:

```
mkdir -p ~/Applications/NodeJS
```

Next, copy the NodeJS tar file to this location, unpack it, and delete the tar file:

```
cp ~/Downloads/node-*.tar.xz ~/Applications/NodeJS
tar xvf ~/Applications/NodeJS/node-*.tar.xz -C ~/Applications/NodeJS
rm ~/Applications/NodeJS/*.tar.xz
```

Next, symlink the `latest` directory from the OpenJDK file.

```
ln -s ~/Applications/NodeJS/node-* ~/Applications/NodeJS/latest
```

