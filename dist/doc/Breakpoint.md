##Breakpoint makes writing media queries in Sass super simple. 
With breakpoint everything that is defined will automatically be converted to CSS inside an `@media` content block.
_An example being._
```
$Example-Varible: 500px //Defining the Varible

.Example-Class {
  @include breakpoint($Example-Varible) {
    // Content
  }
}
```
Will be converted to CSS by the SASS parser to look like this in your final code.
```
@media (min-width: 500px) {
  .Example-Class {
    // Content
  }
}
```
---
###Here's how we begin:

To begin we define a varible with a meaningful name, then give it a defining size.
```
$Small-tablet: 500px;
```
I told you it was simple. Check it out. You can use that variable in the Breakpoint mixin like this.

```
.My-Class {
  @include breakpoint($Small-Tablet) {
    //Class content
  }
}
```

That just did two things that are really helpful. First, we reduced the media query down to the one value that really matters here, the min-width value. (You can also build complex queries and override the defaults. We’ll get to those.) And second, we gave that media query a meaningful name. And once we start calling media queries by name we can start managing them systematically.

Let’s add a few more.

assume `min-width` (by default) if only a number
```
$Small-Tablet: 500px;
```
set `min-width/max-width` if both values are numbers
```
$Small-Desktop: 600px 800px;
```
if one value is a string, assume a feature/value pair
```
$Desktop-Max-Width: max-width 1000px;
```
string tests together within parentheses, assume each item is a feature value pair
```
$Desktop-Max-Height-Portrait: (min-height 1000px) (orientation portrait);
```
---
###And look at each in turn.
Pass Breakpoint just a number and it assumes you want it to write a `min-width` query.
```
$Small-Desktop: 500px; //defining varible

   .My-Class {
     @include breakpoint($Small-Desktop) {
       // Content
     }
   }
```   
Will convert to CSS as:
```
  @media (min-width: 500px) {
     .My-Class {
       // Content
     }
   }
```

**$Small-Desktop** is made up of two numbers. When Breakpoint sees that it will turn that into a `min-width/max-width` query.

```
.My-Class {
   @include breakpoint($ex-presidents) {
   // Content
   }
 }
```
Which turns into this CSS
 ```
@media (min-width: 600px) and (max-width: 800px) {
   .My-Class {
     // Content
   }
 }
 ```

**$Desktop-Max-Width** is made up of a number and the name of a feature to test. Breakpoint will turn these into feature/value pairs

```
$Desktop-Max-Width: max-width 1000px;

.My-Class {
   @include breakpoint($Desktop-Max-Width) {
     // Content
   }
 }
```
Which turns into this CSS
 ```
@media (max-width: 1000px) {
   .My-Class {
     // Content
   }
 }
 ```

**$Desktop-Max-Height-Portrait** has a feature/value pair, and adds a second non-numeric pair. Breakpoint can interpret text-based tests and can string together as many queries as you need.
```
$Desktop-Max-Height-Portrait: (min-height 1000px) (orientation portrait);

 .My-Class {
   @include breakpoint($Desktop-Max-Height-Portrait) {
     // Content
   }
 }
 ```
 
 Which turns into this CSS
 ```
 @media (min-height: 1000px) and (orientation: portrait) {
   .My-Class {
     // Content
   }
 }
 ```
 ---
###That’s the basics, but wait there’s more.

Breakpoint also builds in robust support for no query fallbacks.
https://github.com/at-import/breakpoint/wiki/No-Query-Fallbacks

The ability to pass the media query context to your own custom mixins.
https://github.com/at-import/breakpoint/wiki/Breakpoint-Context

Special handling for device-pixel-ratio.
https://github.com/at-import/breakpoint/wiki/Advanced-Media-Queries#resolution-media-queries