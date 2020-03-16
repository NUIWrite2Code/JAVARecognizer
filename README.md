# Write2Code
[**_Write2Code_**](https://write2codejavarecognizer.firebaseapp.com) is an web application integrating the two components: [**JAVARecognizer**](https://github.com/NUIWrite2Code/JAVARecognizer) and [**wschecker**](https://github.com/NUIWrite2Code/wschecker)     
The **_JAVARecognizer_** is a JAVA handwritten-code recognizer. 
  
It provides the user with the following feautures:  
* Digital handwriting input capture
* Handwriting recognition
* JAVA code checking
```URL of the app: https://write2codejavarecognizer.firebaseapp.com```
# Requirements
The recognizer component was built using the following technologies:
* Programming Language: **Javascript**. This programming language is used to 
  * operate with DOM elements within HTML pages, 
  * make requests to the [**Checker**](https://github.com/NUIWrite2Code/wschecker) component, 
  * and to process the responses coming from it. 
  * The code is recognized and operational through the web browser.
* Main technologies and libraries:
  * [**MyScript**](https://developer.myscript.com/docs/interactive-ink/1.3/overview/about/):
    * [**MyScript Interactive Ink SDK**](https://developer.myscript.com/docs/interactive-ink/1.3/overview/about/) is a set of graphical libraries and server APIs provided by MyScript to help developers build applications that require digital handwriting recognition. All recognition operations are processed on the MyScript Server with WebSocket used as the communication protocol.
    * On the client side, we use the [**myscript-text-web**](https://github.com/MyScript/myscript-text-web) module to capture digital handwriting input and handle the communication with the server.
  * **HTML**: Stands for Hyper-Text Markup Language, and is used to give structure and order to the elements that will appear in the client through the web browser.
  * **CSS**: Stands for Cascading Style Sheets, and its used to control the style of the webpage and to determine how HTML elements are to be displayed.
  * **NodeJS**: Javascript runtime environment used to bring the features of Javascript language to backend, or in other words, outside of the web browser. Myscript and Polymer-CLI are supported with NodeJS.
  * [**Polymer-CLI**](https://polymer-library.polymer-project.org/3.0/docs/tools/polymer-cli): Library used to create custom elements used as DOM elements in the web pages of the GUI. This technology was used following the implementation recommendation given by MyScript documentation and its community of developers.
  * The recognizer was deployed using [**Firebase Hosting**](https://firebase.google.com/products/hosting), which is a SaaS (Software as a Service) Cloud service to host and deploy web and mobile applications. 
# Configuration
The configuration followed the steps indicated in the following link: https://polymer-library.polymer-project.org/2.0/docs/toolbox/deploy

Once the environment is configured, following the previous link, anytime we want to have the recognizer deployed we need to follow the next commands inside the project root:
* polymer build
  * This command will create the web elements required by MyScript in the HTML file.
* firebase deploy
  * This command will upload and update the cloud node hosting the web project.
