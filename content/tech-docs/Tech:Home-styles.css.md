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
background: var(--background-color-neutral, #F6F6F6);
grid-area: depth;
}

html.skin-theme-clientpref-night .card-news {
border-top-color: #FFFFEA;
background: #67540F;
}

html.skin-theme-clientpref-night .card-tech {
border-top-color: #F7F6FF;
background: #180F67;
}

html.skin-theme-clientpref-night .card-dyk {
border-top-color: #FFF2F6;
background: #67440F;
}

html.skin-theme-clientpref-night .card-services {
border-top-color: #F8FFF5;
background: #2C670F;
}

html.skin-theme-clientpref-night .card-depth {
border-top-color: #F6F6F6;
}

.card h3 {
text-align: center;
font-size: 1.5em;
}

@media (prefers-color-scheme: dark) {
html.skin-theme-clientpref-os .card-news {
border-top-color: #FFFFEA;
background: #67540F;
}

html.skin-theme-clientpref-os .card-tech {
border-top-color: #F7F6FF;
background: #180F67;
}

html.skin-theme-clientpref-os .card-dyk {
border-top-color: #FFF2F6;
background: #67440F;
}

html.skin-theme-clientpref-os .card-services {
border-top-color: #F8FFF5;
background: #2C670F;
}

html.skin-theme-clientpref-os .card-depth {
border-top-color: #F6F6F6;
}
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