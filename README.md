# THG MyProtein Product Page
description of task

As i've been coding table based emails for over six years my knowledge of front end design is far from where it should be. I've had to learn alot to get as far as I have with this task. It's been a great execise to get me started with the foundations of front end design. Listed below is how i've managed my time.

### Git
Having never used Git, I thought the first step should be to work out if I could use it. I completed this [tutorial](https://try.github.io/levels/1/challenges/1)

### Set up virtual machine
I'm not familiar with using vertual machines, and with help set up using the following:
 - Download and install virtualBox.
 - Downloaded - Kickoff - lightweight front end framework (use as starting point)
 - Install Vagrant.1.6.5

### CSS 
Looked into the benefits of OOCSS, SMACSS and BEM, trying to learn how to write clean, easy to maintain code, by using a familiar syntax someone else should be able to quickly get to grips with it.

[Youtube video](http:www.youtube.com/watch?v=j9Uxge675So)

Also read up various articles online and concluded that BEM is the better option but to also use the SMACSS Prefixes. eg: 
.is--block-name {...}
.l-block-name__element {...}
.u-block-name--modifier {...}

Would like to spend more time reading and getting familiar with this.

### HTML5
Looked into how HTML5 now uses semantically valuable elements 
<Header>, <Footer>,<Aside>,<Article>,<Section>,<Figure>,<Nav>
I havn't quite got my head around using these so want to continue to research <http://html5doctor.com/article-archive/>

### MyProtein Product page
Look at the sent over [webpage](http://www.myprotein.com/sports-nutrition/impact-whey-protein/10530943.html) and noticed the css uses a mixture of “-” dashes and caps to separate the name attributes, could implement a mixture of SMACSS and BEM.

The site links to an alternative site for mobiles,
<link rel="alternate" media="only screen and (max-width: 640px)" href="http://m.myprotein.com/sports-nutrition/impact-whey-protein/10530943.html">

Also links to separate site for different languages
<link rel="alternate" hreflang="da-dk" href="http://m.myprotein.dk/sports-nutrition/impact-whey-protein/10530943.html"/>

Fully Responsive v’s Mobile site - Maintenance easier - all content is working towards same goal - not having to optimise 2 different versions of the site.

Potential duplicate content issue.