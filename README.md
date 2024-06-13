# SCSS Utilities

## Description
Reusable SCSS Utils

## Author
Srikar Phani Kumar Marti

## Version
1.0.0

## License
ISC

## Repository
[GitHub Repository](https://github.com/srikarphanikumar/scss-utils.git)

## Installation
You can install the package using npm or yarn:

````sh
npm install @scss/utils
````
or
````sh
yarn add @scss/utils
````

## Importing
````scss
@import '~@scss/utils';
````

## Files

<details>
<summary> Variables </summary>
<pre>
.sample-class {
    color: $color-red;
    font-size: $font-size-16;
    ...
}
</pre>
</details>

<details>
<summary>Functions</summary>
<pre>
shade-color(red, 20%) => #990000
complement-color(blue) => #ff00ff
px-to-rem(16) => 1rem
rem-to-px(1) => 16px
add-quotes(hello) => "hello"
remove-quotes("hello") => hello
round-to(3.14159, 2) => 3.14
average(2, 4, 6, 8) => 5
first(1 2 3 4 5) => 1
last(1 2 3 4 5) => 5
</pre>
</details>

<details>
<summary>Geometry</summary>
<pre>
.sample {
    @include circle(50px, #f00);
    @include triangle(100px, 100px, #0f0, down);
    @include rectangle(100px, 50px, #00f);
    @include square(50px, #ff0);
    @include oval(100px, 50px, #0ff);
    @include diamond(50px, #f0f);
    @include parallelogram(100px, 50px, #f00, 45deg);
    @include trapezoid(100px, 50px, #0f0, 0.5);
}
</pre>
</details>

<details>
<summary>Mixins</summary>
<pre>
// All available mixins
.sample {
    @include text-truncate;
    @include text-bold;
    @include text-italic;
    @include text-size(20px);
    @include text-color(#333);
    @include text-shadow(1px 1px 2px rgba(0, 0, 0, 0.5));
    @include border-radius(4px);
    @include box-shadow(2px 2px 4px rgba(0, 0, 0, 0.2));
    @include button-style(#007bff, #fff);
    @include clearfix;
    @include visually-hidden;
    @include border-side(top, 1px, solid, #ccc);
    @include box-sizing(border-box);
    @include position(relative);
    @include visibility(hidden);
    @include transition(all, 0.3s, ease);
    @include flex-align(center);
    @include flex-direction(column);
}
</pre>
</details>

<details>
<summary>Utility Functions</summary>
<pre>
.sample {
    font-size: rem(16); // Result: 1rem
    width: em(320); // Result: 20em
    color: lighten(#000, 20%); // Result: #333333
    background-color: darken(#fff, 10%); // Result: #e6e6e6
    background-color: to-rgba(#f00, 0.5); // Result: rgba(255, 0, 0, 0.5)
    $value: strip-units(20px); // Result: 20
    angle: to-radians(45deg); // Result: 0.7854rad
    angle: to-degrees(0.7854rad); // Result: 45deg
    result: mod(10, 3); // Result: 1
    value: clamp(5, 10, 20); // Result: 10
    area: triangle-area(5, 10); // Result: 25
    area: circle-area(5); // Result: 78.53975
    sequence: fibonacci(10); // Result: 55
    even: is-even(6); // Result: true
    odd: is-odd(5); // Result: true
    text: capitalize('hello world'); // Result: 'Hello world'
    text: title-case('hello world'); // Result: 'Hello World'
    text: hyphenate('hello world'); // Result: 'hello-world'
    text: camel-case('hello world'); // Result: 'HelloWorld'
    id: unique-id(); // Result: 'id-uniqueid'
    text: reverse('hello world'); // Result: 'dlrow olleh'
    text: truncate('hello world', 5); // Result: 'hello...'
    text: repeat('abc', 3); // Result: 'abcabcabc'
    text: replace('hello world', 'world', 'universe'); // Result: 'hello universe'
    result: contains('hello world', 'world'); // Result: true
    number: is-number(10); // Result: true
    integer: is-integer(10); // Result: true
    decimal: is-decimal(10.5); // Result: true
    list: is-list((1, 2, 3)); // Result: true
    length: list-length((1, 2, 3)); // Result: 3
    nth: list-nth((1, 2, 3), 2); // Result: 2
    head: list-head((1, 2, 3)); // Result: 1
    tail: list-tail((1, 2, 3)); // Result: 3
    map: is-map(('key': 'value')); // Result: true
    keys: map-keys(('key': 'value')); // Result: 'key'
    values: map-values(('key': 'value')); // Result: 'value'
    value: map-get(('key': 'value'), 'key'); // Result: 'value'
}
</pre>
</details>

<details>
<summary>Media Queries</summary>
<pre>
.sample {
    width: 100%;

    @include mobile-only {
        background-color: red;
    }

    @include tablet-only {
        background-color: green;
    }

    @include desktop-only {
        background-color: blue;
    }

    @include large-desktop-only {
        background-color: yellow;
    }

    @include extra-large-desktop-only {
        background-color: purple;
    }

    @include mobile-up {
        font-size: 14px;
    }

    @include tablet-up {
        font-size: 16px;
    }

    @include desktop-up {
        font-size: 18px;
    }

    @include large-desktop-up {
        font-size: 20px;
    }

    @include extra-large-desktop-up {
        font-size: 22px;
    }

    @include mobile-down {
        padding: 10px;
    }

    @include tablet-down {
        padding: 20px;
    }

    @include desktop-down {
        padding: 30px;
    }

    @include large-desktop-down {
        padding: 40px;
    }

    @include extra-large-desktop-down {
        padding: 50px;
    }
}
</pre>
</details>

#### Animations (as classes)</summary>
````html
// This will add 'bounce' animation to the div tag
<div class="animated bounce">Bouncing Text</div>

// Similarly
<div class="animated spin">Spinning Image</div> // For 'spin'
<div class="animated fade-in">Fading Element</div> // For 'fade-in'
<div class="animated pulse">Pulsing Element</div> // For 'pulse'
<div class="animated shake">Shaking Element</div> // For 'shake'
<div class="animated slide-in">Sliding In Element</div>// For 'slide-in'
<div class="animated zoom-in">Zooming In Element</div> // For 'zoom-in'
.
.
.
````
