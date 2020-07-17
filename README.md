# :zap: Ionic Slide Drawer

App to display a vertical slide drawer that raises to full height with an Ionic swipe Gesture, using the [Ionic 5 framework](https://ionicframework.com/docs) and [Capacitor](https://capacitor.ionicframework.com/).

## :page_facing_up: Table of contents

* [:zap: Ionic Slide Drawer](#zap-ionic-slide-drawer)
  * [:page_facing_up: Table of contents](#page_facing_up-table-of-contents)
  * [:books: General info](#books-general-info)
  * [:camera: Screenshots](#camera-screenshots)
  * [:signal_strength: Technologies](#signal_strength-technologies)
  * [:floppy_disk: Setup](#floppy_disk-setup)
  * [:computer: Code Examples](#computer-code-examples)
  * [:cool: Features](#cool-features)
  * [:clipboard: Status & To-do list](#clipboard-status--to-do-list)
  * [:clap: Inspiration](#clap-inspiration)
  * [:envelope: Contact](#envelope-contact)

## :books: General info

* Uses [Ionic Gestures](https://ionicframework.com/docs/v3/components/#gestures) to activate drawer

## :camera: Screenshots

![screen print](./img/drawer.png)

## :signal_strength: Technologies

* [Ionic/angular v5](https://ionicframework.com/)
* [Ionic v5](https://ionicframework.com/)
* [Angular v10](https://angular.io/)
* [Ionic Gestures](https://ionicframework.com/docs/utilities/gestures)

## :floppy_disk: Setup

* Load dependencies using `npm i`,
* To start the server on _localhost://8100_ type: 'ionic serve'

## :computer: Code Examples

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

## :cool: Features

* Uses a swipe gesture to open a drawer. Custom gestures and interactions can be created.

## :clipboard: Status & To-do list

* Status: working.
* To-do: nothing.

## :clap: Inspiration

* [Joshua Morony Youtube video: SLIDE DRAWER WITH IONIC GESTURES - Ionic UI Challenge #3](https://www.youtube.com/watch?v=AW80XVSOLZg&t=28s).
* [Josh Morony website](https://www.joshmorony.com/)

## :envelope: Contact

* Repo created by [ABateman](https://www.andrewbateman.org) * you are welcome to [send me a message](https://andrewbateman.org/contact)
