<script setup>
import Home from './components/Home.vue'
</script>

<template>
  <div class="container">
    <Home />
  </div>
</template>

<style scoped>
/* CSS Reset */
html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}

* {
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

* {
  margin: 0rem;
  padding: 0rem;
}

a {
  text-decoration: none;
}

/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}

body {
  line-height: 1;
}

ol,
ul {
  list-style: none;
}

blockquote,
q {
  quotes: none;
}

blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

html,
body {
  padding: none;
  margin: 0rem !important;
}

/* Fonts */
@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-300.woff) format("woff");
  font-weight: 300;
  font-style: normal;
  unicode-range: U+000-5FF;
}

@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-400.woff) format("woff");
  font-weight: 400;
  font-style: normal;
  unicode-range: U+000-5FF;
}

@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-500.woff) format("woff");
  font-weight: 500;
  font-style: normal;
  unicode-range: U+000-5FF;
}

@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-600.woff) format("woff");
  font-weight: 600;
  font-style: normal;
  unicode-range: U+000-5FF;
}

@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-700.woff) format("woff");
  font-weight: 700;
  font-style: normal;
  unicode-range: U+000-5FF;
}

@font-face {
  font-family: "Poppins";
  src: local("Poppins"), url(./Poppins/poppins-800.woff) format("woff");
  font-weight: 800;
  font-style: normal;
  unicode-range: U+000-5FF;
}

.container {
  width: 100%;
  height: 100vh;
  font-family: Poppins;
}
</style>
