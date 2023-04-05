# Awesome Annotation Library

This library provides a simple and elegant solution for parsing annotations in JavaScript projects. It makes it easy to organize and scale your projects by extracting meaningful information from your code.

With this library, you can parse module.exports = class Something, annotations for default exporting class, functions, properties, methods, static methods, static properties, async methods, async functions, and more!


## Features

>    Supports a wide range of JavaScript syntax for annotations.

>    Easy to use and integrate into your projects.

>    Makes it simple to extract and organize meaningful information from your code.

## Usage

To get started with this library, simply include it in your project and start using it to parse your annotations.

## Installation

You can install awesome-annotation as a dependency in your project by running the following command in your terminal:

``` 
npm install awesome-annotation
```

Or if you are using Yarn:

``` 
yarn add awesome-annotation 
```

After successful installation, you can import the package in your project and start using it.

## Guide

You can use the annotation function in your project by requiring it in your code:

```javascript 
  const annotation = require("awesome-annotation");
```

The annotation function takes two arguments: the path to the file you want to parse for annotations, and an options object (which is optional).

Here is an example of how you could use the annotation function:

```javascript 
  const fileContent = annotation("/test/testone1.js", { cached: true, debug: false });

  console.table(fileContent.annotations);
  console.table(fileContent.getAnnos("UserController"));

  console.log(fileContent.exports.something, "@@");
  console.log(new fileContent.exports());
```

The fileContent variable will contain the annotations found in the file, as well as information about the exports. You can access the annotations through the annotations property, and use the getAnnos method to get annotations for a specific exported entity. Additionally, you can access the exports themselves through the exports property.


## Contributing

We welcome contributions to this library. If you would like to contribute, please fork the repository and submit a pull request.


## License

This library is open-source and available under the MIT License.