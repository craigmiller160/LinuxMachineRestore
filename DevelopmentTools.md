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

Next, symlink the `latest` directory from the OpenJDK directory.

```
ln -s ~/Applications/OpenJDK/jdk-* ~/Applications/OpenJDK/latest
```

Lastly, setup the necessary environment variables and `PATH` in the `.bash_profile` file.

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

Next, symlink the `latest` directory from the NodeJS directory.

```
ln -s ~/Applications/NodeJS/node-* ~/Applications/NodeJS/latest
```

Lastly, setup the necessary `PATH` in the `.bash_profile` file.

```
# NodeJS
nodejs=~/Applications/NodeJS/latest
if [ -d $nodejs ]; then
	PATH="$nodejs/bin:$PATH"
fi

# Yarn
yarn=~/.yarn
if [ -d $yarn ]; then
    PATH="$yarn/bin:$PATH"
fi
```

## IntelliJ

First, go to this link to download the Ultimate Edition of IntelliJ: <a href="https://www.jetbrains.com/idea/download/#section=linux">Download IntelliJ</a>

Then, create the IntelliJ directory with this command:

```
mkdir -p ~/Applications/IntelliJ
```

Next, copy the IntelliJ tar file to this location, unpack it, and delete the tar:

```
cp ~/Downloads/ideaIU-*.tar.gz ~/Applications/IntelliJ
tar xvf ~/Applications/IntelliJ/ideaIU-*.tar.gz -C ~/Applications/IntelliJ
rm ~/Applications/IntelliJ/*.tar.gz
```

Next, symlink the `latest` directory from the IntelliJ directory.

```
ln -s ~/Applications/IntelliJ/idea-IU-* ~/Applications/IntelliJ/latest
```

Next, run IntelliJ for the first time with this command:

```
~/Applications/IntelliJ/latest/bin/idea.sh
```

Accept the license agreement and navigate through the prompts to the license key. The credentials for this can be found in 1Password.

Now, close IntelliJ. Then copy the desktop file from this project to the appropriate directory:

```
cp ~/Development/Projects/Restore/jetbrains-idea.deskop ~/.local/share/applications
```

Now IntelliJ should be able to be opened from the applications menu.

## Maven

First, download the Maven binary from this link: https://maven.apache.org/download.cgi.

Then, create the Maven directory:

```
mkdir -p ~/Applications/Maven
```

Next, copy and unpack the tar file:

```
cp ~/Downloads/apache-maven-*.tar.gz ~/Applications/Maven
tar xvf ~/Applications/Maven/apache-maven-*.tar.gz -C ~/Applications/Maven
rm ~/Applications/Maven/apache-maven-*.tar.gz
```

Next, symlink the `latest` directory from the maven directory:

```
ln -s ~/Applications/Maven/apache-maven-* ~/Applications/Maven/latest
```

Lastly, add the following lines to the `.bash_profile` file:

```
# Maven
maven=~/Applications/Maven/latest
if [ -d $maven ]; then
	PATH="$maven/bin:$PATH"
fi
```

Oh, also there is a `settings.xml` file here that needs to go in `~/.m2/settings.xml`. Please update the password field in it too with the password in 1Password.

## Gradle

First, download the app from this link: https://gradle.org/releases/

Then, create a Gradle directory:

```
mkdir -p ~/Applications/Gradle
```

Then, copy and unpack the zip:

```
cp ~/Downloads/gradle*.zip ~/Applications/Gradle
unzip ~/Applications/Gradle/gradle*.zip -d ~/Applications/Gradle
rm ~/Applications/Gradle/*.zip
```

Next, symlink the `latest` directory from the Gradle directory:

```
ln -s ~/Applications/Gradle/gradle-* ~/Applications/Gradle/latest
```

Lastly, add the following lines to your `.bash_profile`:

```
# Gradle
gradle=~/Applications/Gradle/latest
if [ -d $gradle ]; then
	PATH="$gradle/bin:$PATH"
fi
```

## Postman

First, download the app from this link: https://www.postman.com/downloads/.

Then, create a Postman directory:

```
mkdir -p ~/Applications/Postman
```

Then, copy and unpack the tar:

```
cp ~/Downloads/Postman-*.tar.gz ~/Applications/Postman
tar xvf ~/Applications/Postman/Postman-*.tar.gz -C ~/Applications/Postman
rm ~/Applications/Postman/Postman-*.tar.gz
```

Next, symlink the `latest` directory from the Postman directory:

```
ln -s ~/Applications/Postman/Postman ~/Applications/Postman/latest
```

Lastly, copy the desktop entry from this project:

```
cp ~/Development/Projects/Restore/Postman.desktop ~/.local/share/applications/
```