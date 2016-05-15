# THG MyProtein - Product Page

Listed below is my approach and how I've managed my time:

### Git
This has been a great excercise in familiarising myself with Git. I completed this [tutorial](https://try.github.io/levels/1/challenges/1)

Note: I have an understanding of, and will continue to experiment with branches, etc - as I'm sure these are used regularly by the team.

### Setup Virtual Machine
Set up using the following:
 - Download and install virtualBox.
 - Downloaded - Kick off - is a skeleton (like a base to get started) of folders and files.
 - Install Vagrant.1.6.5

### CSS 
Looked into the benefits of OOCSS, SMACSS and BEM, learnt how to write clean, easy to maintain code; by using familiar syntax someone else would be able to quickly get to grips with it, which would be really important when working as part of the team.

[Youtube video](http:www.youtube.com/watch?v=j9Uxge675So)

Read various articles and concluded that BEM is the better option but to also use the SMACSS Prefixes. eg: 

    .is--block-name {...}
    .l-block-name__element {...}
    .u-block-name--modifier {...}

Note: Would like to spend more time reading and getting familiar with this.

### HTML5
Researched how HTML5 now uses semantically valuable elements 
Header, Footer, Aside, Article, Section, Figure ,Nav
Will continue to research <http://html5doctor.com/article-archive/>

---

### MyProtein Product Page
Looked at the [webpage](http://www.myprotein.com/sports-nutrition/impact-whey-protein/10530943.html) and noticed the css uses a mixture of “-” dashes and caps to separate the name attributes.  

Suggestion: We could implement a mixture of SMACSS and BEM.

The site links to an alternative site for mobiles,
<link rel="alternate" media="only screen and (max-width: 640px)" href="http://m.myprotein.com/sports-nutrition/impact-whey-protein/10530943.html">

Also links to separate site for different languages
<link rel="alternate" hreflang="da-dk" href="http://m.myprotein.dk/sports-nutrition/impact-whey-protein/10530943.html"/>

Thoughts: Making the site fully responsive, maintenance would be more manageable, all content is working towards same goal and we're not having to optimise different versions of the site. Having an alternate mobile site poses potential duplicate content issues.

---

### The Build
Concentrating on the 'product-content' section:
- make sections responsive
- product-promo to pop-up on desktop (if i have time to figure out either with css or javaScript)
- JavaScript to create dropdown options (this might something I'll have to look into after this test)

**I've made various comments within the code to highlight why I have done things the way I have.**


#### General notes
- Make things modular
- Write things that are encapsulated so they can be reused. 
- Find Compass repo on github
- Mixins for SASS
- Vagrant = task runner for Dev environment

##### SublimeText with Chrome LivePreload
Rather than code within Dreamweaver I wanted to familiarise myself with SublimeText and using Chrome LivePreload. In time it would be great to learn some of the short-cuts and packages.
Command -T
Command-shift-period
Emmet - “html:5-TAB” (for html page structure)

##### Bootstrap
I didn’t use it, not just because you said you’d rather I didn’t, but because it comes with a lot of bloat. Tried to keep it lean and only include exactly what needs to be there. 

Instead of using an off-the-shelf taskrunner such as CodeKit, I've aquired a framework start-kit that has Gulp already installed and various tasks pre-loaded. scss, img and JavaScript compilers etc were already set up. I've opted to use this due to time constraints but will go back and explore this further.

##### SASS - Preprocessor 
Notes below taken from Chris Coyiers [video](https://www.youtube.com/watch?v=vsTrAfJFLXI) although this was published on Oct 25, 2012 so might be slightly outdated? I kept these notes in mind but will need to further explore them.

Notes:

**Variables** - Don’t assign variables to modules. Always assign them to a config file. 

    $blue:#0079c1 
    ( Name them something more generic - e.g. “Brand Colour A” rather than “Blue” (incase the brand colour blue changes to pink, for example)
    h1 {$blue;}
    
**Mixins**

    @mixin font-stack($font-family: 'Whitney', $font-weight: 400, $font-size: 3em) {
    font-family: $font-family;
    font-weight: $font-weight;
    font-size: $font-size;
    }

    body {
    @include font-stack;
    }

    .button {
    @include font-stack('Open San', 600);
    }

**Vendor prefixes**
Eg: -moz-, -webkit- (x2)

    @import “compass/css3”;
    .module {
    @ include background(linear-gradient (white,#ccc)
     );
    }
    
Spits out:

    .module {
    background:-webkit-gradient(linear,50% 05 50% 100%, color-stop(0%, #ffffff), colour-stop(100%, #cccccc));
    background:-webkit-linear-gradient(#ffffff, #cccccc);
    background:-moz-linear-gradient(#ffffff, #cccccc);
    background:-o-linear-gradient(#ffffff, #cccccc);
    background:linear-gradient(#ffffff, #cccccc);
    }

If you add another bit:

    @import “compass/css3”;
     $experimental-support-for-svg:true;
      .module {
      @ include background(linear-gradient (white,#ccc)
     );
    }
    
Spits out data URI - code string for svg gradient image.
    
**Media Queries**

    @media all and (min-width: 1001px) {...}
    @media all and (max-width: 1000px) and (min-width: 700px) {...}
    @media all and (max-width: 699px) and (min-width: 520px), (min-width: 1151px)     {...}



---








