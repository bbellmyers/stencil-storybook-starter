# Stencil + Storybook

* Stencil component project from cli
* Add storybook/react per cli
* wire together, sharing www directory
* Force es5 build to ensure compability with IE11.
  * Note that when Stencil component is changed, you need to manually refresh Storybook
* Includes a fixed version of the document.baseURI polyfill, which is required
  to allow Stencil components to load on Storybook stories.
  * https://github.com/ionic-team/stencil/issues/1994
