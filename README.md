# Flutter deployment in Surge

## Flutter project creation
First we need to create a Flutter project with the Flutter version inside it's stable channel.
After installing the stable version we have to enable the flutter web platform running the follwoing command:
- `flutter config -enable-web`

After this we can test if our project is really running on the web platform, running the following commnad inside the project root folder:
- `flutter run -d <chrome|edge|etc.>`


## Surge Configuration
First we need to install [node.js](https://nodejs.org/en/) in our environment, and then install the surge tool by running the following command:
- `npm i -g surge`

And with this we have all we need to make the deployment of our flutter project in surge.

## Deployment
First we need to build our flutter web project after all the changes that we need with:
- `flutter build web`

After this we only need to run the surge command inside our **BUILD/WEB** folder in our project folder:
- `surge`

With this, if you dont have an account created, the command will ask you to register your credentials and then will ask you about the folder that you want to deploy (it will present the path of your build/web folder if you runned the command inside it like mentioned before) and your custom domain. (that needs to end with ``surge.sh``).

CONGRATULATIONS!!! Now if you enter your domain in the browser you can see your flutter project working 😁 !

You can see an example from this worflow in my personal test http://jorge-home.surge.sh/#/.