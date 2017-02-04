# Front end tooling starting template

> A starting set up to quickly start building any HTML UI

## Usage

Is extremely easy to start working on this template because you don't have to bother learning additional tools like grunt or bower. With NPM you have everything you need. just type `npm run start` and you have a local server that refreshes your browser (with Browser Sync), watches and build your sass (with Nodemon) and js files (with Watchify and Browserify) every time you save or modify any file you are working on.

If you want to just build your sass or js modules type `npm run build-css` in the case of *sass* and `npm run build-js` in the case of *js*.

You can create additional `.scss` files under the `/sass/partials` directory to further modularize the different components that comprises your UI.
I left there the basic partials you need to set up like typography, buttons, figures and variables.

I find this approach super convenient because you write super high maintainable code as you modularize your components into different sass and js files, and in the end you only have to load one css and one js without losing that maintainability. You also can take advantage of `requirejs` on the browser with browserify.

## Installation

**NPM**

**Step 1**
Once you cloned this repo just `cd` to the directory and type this:

```sh
npm install
```

**Step 2**
Build js files needed for the first time. Type:

```sh
npm run build-js
```

**Step 3**
Start the local server and begin your magic! Type:

```sh
npm run start
```
**Note:** If you can't see the css applied at this point and just see the default styles from the browser, don't worry just refresh your browser and you will see it.

## What does it do, what's the point?

I found myself building this set up again and again every time I had to start a new project.
This template comes with the minimum set up needed to begin working with your HTML template.

It includes Nicolas Gallagher's [normalize.css](https://github.com/necolas/normalize.css) to properly reset default browsers css. As an optional, I included the super awesome [Susy](http://susy.oddbird.net/) library. If you don't want to use it, just go to `/sass/styles.scss` and comment the line that has `@import "susy";`.

It also includes the [breakpoint-sass](https://github.com/at-import/breakpoint) library to help you write media queries in Sass in a super simple way.

**What does it do?**

- It builds your sass files into one css file.
- It builds your js modules into one js file.
- It allows you to map source your files as you build your UI. Excellent for debugging purposes.
- It automatically watches whenever you make any changes to any of your sass and js modules and compile them into one file.
- With Browser Sync it automatically refreshes your browser on all the screens you are using every time you save your code. No matter if you are simultaneously watching your design on a mobile, a tablet or a desktop or wherever. Browser Sync allows you to even natively inspect your design independently on each of your devices.


## How to customize it to your preferences?

Go to `sass/partials` add your additional modules keeping the convention `_name-of-your-file.scss` and then go to `sass/styles.scss` and under the "General partial" section import the files you just created.

With js, just go to `js-modules/` create your js files and `require()` them in your `main.js` file.

## Credit

Created by Camilo Sanchez.

- [Twitter](https://twitter.com/camilosanchez)
- [Github](https://github.com/camilosanchez)
- [Dribbble](https://dribbble.com/camilosanchez)
- [Medium](https://medium.com/@camilosanchez)
- email: camilosanchez40ATgmail.com
