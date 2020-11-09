# degreeofreedom
My new techno-political-nerdsnipe blog where you can participate...with a [github pull request](https://github.com/javasjosh/degreeofreedom). Here is a sample of the content:

# The Best Browser State For Front-end Development?
JBR 11-08-20

What us the best browser state? I mean, if you were to sit down at a browser, ready to *create*, either to write fiction, or perhaps make software, what would be your environment? What is interesting (and a little depressing TBH) is how quickly we've all abandoned the browser's lovely do-everything-at-the-last-minute runtime and slapped a build-tool around its neck. Are you really so certain there's nothing more to be said for build-free environments?

Let me just say that we'll probably all agree that there are circumstances, mainly when learning a new feature, or isolating a bug, where a very simple page might come in handy, so we just make an HTML file or, do something in [Codepen](https://codepen.io/javajosh). However, what if you wanted to make anything? What would you need?

To get to the answer, I spent a lot of time making little tools and experiments with raw html and javascript. Over time I noticed I wanted the same things over and over, and so these formed my personal library. Finally, to be a good citizen I tucked all of those into a global object. This is similar, so far, to how jQuery, Lodash, or d3 work.

For the next step, you've got to go with me and make a strong distinction between two kinds of web. The first web, the RESTful web, is mostly about written documents like academic papers, pointing to each other as references. {{It was designed for a world where people linked to each other's stuff, and everyone had a long-lived domain that would be a stable namespace for everything they ever do. But this space was sadly difficult to navigate, and forums turned out to serve much the same purpose (and in fact had many key advantages over the self-hosted blogosphere)}} TODO: figure out how footnotes/sidenotes work  .

The second, the web for applications, especially Single Page Applications, is, in my not-humble-at-all view, better expressed as something like Canvas or, even better, SVG. With SVG you get several excellent (and expensive to reimpliment) features that get rendered with a fast 2D coprocessor. You also get automatic hit detection for click-to-element mapping and function invocation (which we ignore, putting all listeners on root).

BTW, I want to build an "SVG archetype" image that includes all the tags and option combinations. These will be my (hopefully easier to use) starting points:


<svg id="greenSquare" width=500 height=500 viewBox="-1 -1 2 2">
  <rect x=0 y=0 width=1 height=1 fill=green />
  <a xlink:href="https://degreeofreedom.com">
    <text x=0 y=0 font-size=".1" text-decoration="underline" fill="blue">&#176; o' Freedom</text>
  </a>
</svg>
<script>
  const greenSquare = document.getElementById('greenSquare');
</script>

The visual space we create is very similar to the webspace, in that we visualize it as a set of resources that point to each other. However, we add a new rule: every new resource is going to be specified as a combination of any of the other resources. So the whole space is a combination of (possibly repeating) resources. We also want to take into account that every resource is changing over time, as users adjust this, or alter that about the document. We might say that the Name of the resource is stable, but we can also posit the existence of every version of the resource in time, using either a linked list, or an idexing scheme, or some other way to "go back to time zero". In any event, you can see that this is something like a trie of strings, where the characters are a little more vague.

We will take this concept, and explore it around the most fun area, which is the construction of games (and generally large complex finite state machines). And then extend it "down" toward the browser and operating system, even hardware, and also "up" to include simulations of (ideally deployable) networks. In the meantime, just realize that this programming model is the amaze (and extremely small, yet readable and easy to debug, in a browser).

I want this to be "famous software" the likes of React, Redux, jQuery, or Erlang. Maybe also GTD (Getting Things Done). Clojure and D3, two inspirations and from inspirational inventors.

We show them events dropping from the top of the image:
<svg>
  
</svg>

Somewhat at odds with most people, I'd like to move toward two things. First, I want to be able to draw paths in a radially symmetric space inside the unit circle. (The goal here is to give meaning to the number of decimal places, even if it means giving up some range).




