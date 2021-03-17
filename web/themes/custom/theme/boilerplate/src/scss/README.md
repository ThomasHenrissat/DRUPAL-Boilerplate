# Structure

Simple overview of the style structure of the project.

## Base

These are styles that are applied to the whole project, they usually contain a CSS reset.

## Components

> Prefixed by `c-`

These are **unique** UI element, they are directly related to a specific template.

They are **safe to modify** since they can only affect themselves and no other components.

## Objects

> Prefixed by `o-`

These are **reusable** UI element, they can be implemented in any component by adding the corresponding markup.

They are **not safe to modify** since they will affect all the components implementing them.

If you need to modify one, make sure that you want that change to happen everywhere this object is used. Otherwise modify the component that implements this object and not the object directly.

## Scopes

> Prefixed by `s-`

These are used when we need to set appart some styles from the rest of the project, you can view them as a new context.
For example, they might come in handy if you are dealing with a third party where you can't control the markup.

## Utils

These are utilities, they contain variables and rules that we need to use regularly.

They are not linked to a particular markup.

## Vendor

These are styles comming from external sources.