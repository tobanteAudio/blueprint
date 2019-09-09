# Blueprint
> A JUCE rendering backend for React.js

Blueprint is an experimental JavaScript/C++ framework that enables a [React.js](https://reactjs.org/) frontend for a [JUCE](http://juce.com/) application or plugin. It provides an embedded, ECMAScript-compliant JavaScript engine via [Duktape](http://duktape.org/), native hooks for rendering the React component tree via `juce::Component` instances, and a flexbox layout engine via [Yoga](https://yogalayout.com/).

For more information, see the introductory blog post here: [Blueprint: A JUCE Rendering Backend for React.js](https://nickwritesablog.com/blueprint-a-juce-rendering-backend-for-react-js)

## Status

|                                                                  LICENSE                                                                  |                                                              macOS                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------: |
| [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/nick-thompson/blueprint/blob/master/LICENSE.md) | [![Build Status](https://travis-ci.org/tobanteAudio/blueprint.svg?branch=master)](https://travis-ci.org/tobanteAudio/blueprint) |

## Examples
Blueprint is a very young project, but already it provides the framework on which the entire user interface for [Creative Intent](http://creativeintent.co/)'s forthcoming plugin, Remnant, is built.

![Creative Intent Remnant: Beta screenshot](https://github.com/nick-thompson/blueprint/blob/master/RemnantBeta.jpg)

Besides that, you can check out the BlueprintPlugin example in the `examples/` directory. See the "Getting Started" section
below for building and running the demo plugin.

## Getting Started
First, you'll need to collect the code and its dependencies.

#### Getting the code

```bash
$ git clone --recurse-submodules git@github.com:nick-thompson/blueprint.git
```
or
```bash
$ git clone git@github.com:nick-thompson/blueprint.git
$ cd blueprint
$ git submodule update --init --recursive
```

#### Running the examples
```bash
$ cd blueprint/packages/juce-blueprint
$ npm install
$ npm run build
$ cd ../../examples/BlueprintPlugin/Source/ui/
$ npm install
$ npm run build
```
Then open up the appropriate exporter for your platform from the appropriate example plugin directory and build as usual.

#### Starting your project
```bash
$ cd blueprint/packages/juce-blueprint
$ npm install
$ npm run build
$ npm run init -- path/to/your/project/directory
$ cd path/to/your/project/directory
$ npm start
```

Now Webpack will watch your JavaScript files for changes and update the bundle on save. The last step is to add the
`blueprint::ReactApplicationRoot` to your project and mount it into your editor. See the [PluginEditor.cpp](https://github.com/nick-thompson/blueprint/blob/master/examples/BlueprintPlugin/Source/PluginEditor.cpp#L18) file in the BlueprintPlugin example for how to do that.

## Contributing
Yes, please! I would be very happy to welcome your involvement. Take a look at the [open issues](https://github.com/nick-thompson/blueprint/issues)
or the [project tracker](https://github.com/nick-thompson/blueprint/projects/1) to see if there's outstanding work that you might
be able to get started. Or feel free to propose an idea or offer feedback by [opening an issue](https://github.com/nick-thompson/blueprint/issues/new) as well.

I don't have a formal style guide at the moment, so please try to match the present formatting in any code contributions.

## License

See [LICENSE.md](https://github.com/nick-thompson/blueprint/blob/master/LICENSE.md)
