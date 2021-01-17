# react-inject-script

Dynamically inject `<script>` to your react app html file. Benefit, we can load desired library on demand instead of load everything on start up.

## Installation
`yarn add react-inject-script`

## Usage
```
import injectScript from 'react-inject-script';


.....

injectScript('any-unique-name', 'https://link.to.file/min.js').then(() => {
  setTimeout(() => console.log('Successfully loaded'), 1000);
})
.catch(e => {
  console.log(`Failed to load: ${e}`);
});


```
description

'any-unique-name' should be unique per project. this to prevent from the <script> is injected twice if the library is called more than 1

Source code is copied from here: https://www.linkedin.com/pulse/make-opencv-work-react-apps-james-shen