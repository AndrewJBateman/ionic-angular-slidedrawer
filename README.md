# Ionic Slide Drawer

App to display a vertical slide drawer that raises to full height with an Ionic swipe Gesture, using the [Ionic 5 framework](https://ionicframework.com/docs) and [Capacitor](https://capacitor.ionicframework.com/).

## Table of contents

* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info

* Uses [Ionic Gestures](https://ionicframework.com/docs/v3/components/#gestures) to activate drawer

## Screenshots

![screen print](./img/drawer.png)

## Technologies

* [Ionic/angular v5.0.0](https://ionicframework.com/)
* [Ionic v5.0.0](https://ionicframework.com/)
* [Angular v8.2.14](https://angular.io/)
* [Ionic Gestures](https://ionicframework.com/docs/utilities/gestures)

## Setup

* Load dependencies using `npm i`,
* To start the server on _localhost://8100_ type: 'ionic serve'

## Code Examples

* extract from slide-drawer.component.ts: options: GestureConfig


```typescript
/*if gesture pulls drawer up more than 200px then drawer is raised all the way to the top of the ion-card-content (500px)
Note: Y axis is 0 at top and positions below 0 are negative values.*/
onEnd: ev => {
  this.renderer.setStyle(
    this.element.nativeElement,
    'transition',
    '0.3s ease-out'
  );
        
  if(ev.deltaY < -200) {
    this.renderer.setStyle(
      this.element.nativeElement,
      'transform',
      `translateY(-450px)`
    );
  } else {
    this.renderer.setStyle(
      this.element.nativeElement,
      'transform',
      `translateY(0px)`
    );
  }
}
```

## Features

* Uses a swipe gesture to open a drawer. Custom gestures and interactions can be created.

## Status & To-do list

* Status: working.
* To-do: Use to add gesture control to one of my apps.

## Inspiration

* [Joshua Morony Youotube video: SLIDE DRAWER WITH IONIC GESTURES - Ionic UI Challenge #3](https://www.youtube.com/watch?v=AW80XVSOLZg&t=28s).
* [Josh Morony website](https://www.joshmorony.com/)

## Contact

Repo created by [ABateman](https://www.andrewbateman.org) - feel free to contact me!
