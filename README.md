# Unity AppLixir Webview Plugin

unity-webview-plugin is a plugin for Unity 5 that overlays WebView display of a website configured to display ads through AppLixir.

This project is derived from gree's unity-webview https://github.com/gree/unity-webview .

unity-webview is derived from keijiro-san's
https://github.com/keijiro/unity-webview-integration .


## Example project

An example implementation of this plugin is here: https://github.com/appjason/unity-applixir-webview .

This project has different branches that demonstrate different implementations. The standalone branch is a simple button that is not integrated with AppLixir, and the webview_webgl branch uses this plugin to modify that simple application to display reward videos. See the project for details on the implementations.

## Usage

1. Copy (or merge, if there is already a Plugins folder in the project) the Plugins directory from the plugin to the project's Assets folder.
2. Copy the WebGLTemplates folder from the Plugins folder to the Assets folder in the same project (same folder that contains the Plugins folder).
2. Create a class to handle the button click and callback results from AppLixir. These instructions will assume that class is called ButtonHandler. An example is here: https://github.com/appjason/unity-applixir-webview/blob/webview_webgl/Assets/Scripts/ButtonHandler.cs
2. Update the ButtonHandler class to trigger the webview and process the callback status.
3. Add an empty GameObject to the state (named, e.g., "ButtonHandler"), and add the ButtonHandler class as a component to that GameObject.
3. (If using the example class) From within the Unity editor, select the ButtonHandler object and set the Url on the ButtonHandler script to a website with a valid AppLixir website. See the project website folder for an example.
4. Also within the Unity editor, link the ButtonHandler GameObject from the scene to the OnClick handler for the button itself, and set the Function to ButtonHandler -> PlayVideo.
5. Copy the WebGLTemplates folder from the Plugins directory to the Assets directory.
6. From within the Unity editor, select Project Settings -> Player -> Resolution and Presentation -> WebGL Template -> unity-webview-2020.