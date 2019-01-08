# Alpaca UiPath Form Builder

![Alpaca UiPath Form Builder](resources/logo/alpacaUiPath_logo.png)

This library and project template allows UiPath Studio users to build rich HTML forms with a variety of UI controls and configurable validation.  Forms can be built in one of two ways:

1.  In Studio by adding activities associated with specific HTML controls into their workflow
2.  A visual form builder where users can drag and drop control types in a visual environment and set their properties that way (this is more in an experimental phase than option #1)

## Project Origination:  Why?
The "custom input" activity, introduced in the 2018.3 release, allows one to display HTML forms in UiPath, but they must already be built somewhere else to display.  "Custom Input" is an invaluable activity to allow users to enter input data for use in attended processes.

There is some demand for the capability in UiPath to build an input form (in the context of an attended process) where the input form itself had dynamically generated controls based on some other data in a process.  This project allows for this as you can do things like add controls to a form in a loop or add radio button, checkbox, or select options dynamically from some data.

Beyond dynamically generated forms, it's also useful for UiPath Studio users to be able to build forms quickly without having to resort to using outside tools to do so.

## Technology
The technology is built on top of Alpaca:  http://alpacajs.org/ .   Generally UiPath is used in this case to generate JSON that Alpaca can process and the HTML and Javascript around an Alpaca form.

Other underlying technologies for the generated forms include JQuery and Bootstrap.  When other custom controls are included using method #1 (above) to build forms, other libraries are brought in dynamically as needed.  The location of all external libraries are configurable in the activities themselves.  By default they are set to access libraries on the internet (to make this as easy as possible to get started) but all included JS and CSS can also be downloaded to be referenced locally.

## Generated Forms
Generated forms are written to a ".html" file.  As the generated forms are driven by the bootstrap framework, the generated forms are "responsive"-- that is, they should adjust their look/layout when viewing on devices of different resolutions (including mobile phones).

Resulting forms work well in UiPath's "Custom Input" activity.  The generated forms can also be used outside of UiPath:  in this way this enables UiPath's Studio to become a generic full-featured HTML form building engine.  The forms layouts are completely configurable using Twitter's Bootstrap standard classes.

The activities in the Alpaca UiPath form builder library are also aimed at allowing less technical users to build web forms.  They also allow more technical users the ability to do so more quickly.

## Getting Started
1. Download the NuGet package for the Alpaca UiPath form builder library:  alpacauipathformbuilderlib.{version}.nupkg (This NuGet package was itself created from a library project "alpacauipathformbuilderlib")
2. Place this file in the subdirectory under where you installed UiPath Studio in the "Packages" subdirectory
3. You can then use the template project to create a project template in Studio or simply open this project to access form building templates and examples

## Video
### Form Building Method 1
1.  [The Basics](resources/video/01_AlpacaUiPath_FormBuilding_Method1_Basics.mp4?raw=true)
2.  [Multiple Forms](resources/video/02_AlpacaUiPath_FormBuilding_Method1_MultipleForms.mp4?raw=true)
3.  [Different Layouts, Build Forms in a Loop](resources/video/03_AlpacaUiPath_FormBuilding_Method1_LayoutsAndGeneration.mp4?raw=true)

### Form Building Method 2
[Basics]

### Available Controls
[Control Showcase](resources/video/04_AlpacaUiPath_FormBuilding_ControlTypes.mp4?raw=true)