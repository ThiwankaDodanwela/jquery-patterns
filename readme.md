##Recommended jQuery Plugin Patterns

###Introduction

So, you've tried your hand at writing jQuery plugins and you're comfortable putting together something that probably works. Awesome!. Thing is, you think there might be better ways you could be writing them - you've seen them done a number of different ways in the wild, but aren't really sure what the differences between these patterns are or how to get started with them. This project hopes to help solve this.

I began this patterns repo after seeing a number of efforts made in the past to create a one-size-fits-all jQuery plugin boilerplate. Whilst the idea of such a boilerplate is a great idea in theory, the reality is that in plugin development we <b>rarely</b> approach writing plugins in one very-fixed way using a single pattern all the time. 

Some patterns may work better for structuring solutions to a particular problem or component than others. Some developers may wish to use the widget factory. Some may not. Some might like to take advantage of nested namespacing patterns.  Some might want to use custom events or pub/sub to communicate from plugins to the rest of their app. Some may prefer using extend patterns and so on.

This project won't seek to provide solutions to every possible pattern, but will attempt to cover popular patterns developers often use in the wild.

###Patterns 

<ul>
<li>A lightweight start; perfect as a generic template for beginners and above, uses a basic defaults object, simple constructor for assigning the element to work with and extending options with defaults and a lightweight wrapper around the constructor to avoid issues with multiple instantiations - jquery.basic.plugin-boilerplate.js</li>
<li>Widget factory; for building complex, stateful plugins based on object-oriented principles. The majority of jQueryUI heavily relies on the widget factory as a base for components and this template covers almost all supported default methods including triggering events - jquery.widget-factory.plugin-boilerplate.js</li>
<li>Namespaced pattern; to avoid collisions and improve code organization when working with components under another namespace - jquery.namespace.plugin-boilerplate.js</li>
<li>Better options; Globally/Per-call overridable options for greater option customization, based on Ben Almans pluginization talk - jquery.best-options.plugin-boilerplate.js</li>
<li>Custom events (Pseudo Pub/Sub); for better application decoupling. Uses the Widget factory, but could be applied to the generic template - jquery.customevents.plugin-boilerplate.js</li>
<li>Extend pattern - jquery.extend-skeleton.plugin-boilerplate.js</li>
<li>Non Widget-factory widget; if you wish to stay away from the widget factory. Uses Ben Alman's simplewidget including coverage for creation, instantiation and other best practices that may be helpful  - jquery.simplewidget.plugin-boilerplate.js</li>
</ul>


###Contributing

If you have ideas for improvements that can be made to patterns currently in the repo, please feel free to create a new issue for discussion or send a pull request upstream. The same can be said about new patterns you wish to propose being added; for the sake of limiting confusion and complexity, I would ideally like to keep the number of overall patterns in the repo below 10 for now.

###Coming soon

Whilst a number of patterns are well commented, I would like to improve comments on all of them to ease understanding and also include more inline examples of sample usage for beginners. 

###Credits
Thanks to @peolanha, @ajpiano, @mathias, @cowboy, @dougneiner and others for their previous work (or tips) in this area. Some of this work is used as a basis for further improvements.