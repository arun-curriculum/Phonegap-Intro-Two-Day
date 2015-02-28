#Introduction to Phonegap / Cordova

##What is Phonegap / Cordova?
- Cordova is an API that allows you to write JavaScript commands that map over to native device commands.
- Phonegap is a distribution of Cordova, and also wraps in functionality such as its build tools.

##Installation

####Build Tools
- For this class we will need to have Xcode installed with the latest command line and build tools:

```
xcode-select --install
```

- You will also need the Android SDK. You can find it [here](http://developer.android.com/sdk/).
- For compiling Android apps you will need to download and install Apache Ant.
	- Windows [click here](http://ant.apache.org/bindownload.cgi)
	- With Mac it can be installed easily with Homebrew: `brew install ant`.

####Command Line Tools
- You will need to have Cordova and the Cordova-Cli installed:

```
sudo npm install cordova -g
```

##Creating a New Project
- To create a new project we can run the `cordova create` command:

```
cordova create hello com.example.hello HelloWorld
```

- The first parameter is the folder you want to generate. The second is a reverse domain identifier, and the third is the name of the project.
- When you run this command you will see a number of folders generated for you:
	- Platforms: This folder holds information and native code for each platform you choose to target such as Android or iOS.
	- Plugins: This folder will hold all of the plugin-related code that comes in importing the plugin via the command line.
	- Www: This folder will contain all of your HTML, CSS and JavaScript project files. Eventually it will be added to each platform's appropriate folder to be included in the main app.

##Cordova Plugins
- Plugins are the modules of code that allow you to write JS commands that trigger native actions.
- Most of the major native functionality is wrapped into various plugins, such as accessing the camera or pulling from the GPS.