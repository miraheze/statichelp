---
title: Tech:Home/styles.css
---

.homepage-container {
width: 100%;
display: grid;
grid-auto-columns: minmax(0, 1fr);
gap: 10px;
margin: 5px 0;
grid-template-areas:
"news news tech tech dyk dyk"
"services services services depth depth depth";
}

.card {
border-top: 4px solid;
padding: 5px 15px 10px;
}

.card-news {
border-top-color: #67540F;
background: #FFFFEA;
grid-area: news;
}

.card-tech {
border-top-color: #180F67;
background: #F7F6FF;
grid-area: tech;
}

.card-dyk {
border-top-color: #67440F;
background: #FFF2F6;
grid-area: dyk;
}

.card-services {
border-top-color: #2C670F;
background: #F8FFF5;
grid-area: services;
}

.card-depth {
border-top-color: #6F6F6F;
background: #F6F6F6;
grid-area: depth;
}

.card h3 {
text-align: center;
font-size: 1.5em;
}

@media only screen and (max-width: 900px) {
.homepage-container {
grid-template-areas:
"news news"
"tech dyk"
"services services"
"depth depth";
}
}

@media only screen and (max-width: 600px) {
.homepage-container {
grid-template-areas:
"news"
"tech"
"dyk"
"services"
"depth";
}
}



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Home/styles.css)**