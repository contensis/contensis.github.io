# Workflow states
Once created, components will always have one of the following workflow states: _Draft_, _Awaiting Publish_ or _Published_.

## Draft
When a component is created it will be in the _Draft_ state until it has been published for the first time and will be highlighted in grey.

Another indication that the item is in draft is that it has no major version in its version number _e.g._ 0.6.

## Awaiting publish

When a component has been published at least once, and had further changes saved to it, the component will be _Awaiting Publish_ until it is published. It's effectively published and has a new draft state. Components that are _Awaiting Publish_ will be highlighted in orange.

Another indication that the item is _Awaiting Publish_ is that it will have major and minor version numbers _e.g._ 1.6.

## Published

When a component is published and has had no further changes made to it, the component status will be _Published_ and the highlight will be green.

Another indication that the item is in the _Published_ state is that it only has a major number in its version number _e.g._ 2.0.
