10-06-2025 16:25:57

Status :

Tags :


```

how you can get a react project setup locally we're going to be using the recommended build tool called vit
and yes it is pronounced vit that's French for quick or fast and to get started you're welcome to click the
screenshot here which will take you directly to VJs dodev if you want to read a little bit more about vit but I
also in this scrim will be walking you through how to get everything set up in order to use vit on your machine you
need to have node and npm installed already on your machine if you open up a terminal you can type node space- V
that's to check the version of node that you have installed if it gives you any kind of version that 18 and above then
you're golden and you'll likely be able to skip the next few slides that I'm about to show you we also want to check
if npm is installed although as far as I know once you install node you automatically get npm don't quote me on
that for sure but go ahead and use npm space- V to check what your npm version
is if your terminal essentially says I have no idea what you're talking about when you type this in that means you
need to install node and npm and I'm not necessarily going to walk us through how to install node because there's a
million YouTube videos that can help you out in fact if you click the screenshot here it will take you directly to the
query on YouTube specifically installing nodejs with a package called NVM which
is short for node version manager I have found personally that node version manager is the Least Complicated way to
not only install node but also to update it as new versions of node are released now just for reference I've included
screenshots here which you can click either one to take you either to the NVM Repository which is the node version
manager you would use if you're on a Mac or a Linux machine and over here on the right is a link to a similar repository
for NVM Windows which as I'm sure you have figured out is specifically for Windows platform now at the time of
recording it does look like the NVM DWIs team is working on a new package called runtime which it says is the successor
to NVM for Windows but since that is not yet released you'll just have to click on the screenshot and see if runtime is
the new way to do this now I know I I'm not going to walk through this whole thing I'm not going to go through every single step but once you do have NVM
installed you'll simply run NVM install D- LTS for the long-term supported
version and that will just get you the most updated stable version of node once you've done that you can check again for
your node version and your npm version and once those are showing real numbers you are golden and ready to move on and
of course as with all version numbers you see here when you do this it's probably not going to be these exact versions of node and npm because the
ecosystem is evolving pretty quickly and building your first project with vit couldn't be easier in your terminal
You're simply going to type npm create vit at latest and this will jump you into kind of a wizard that helps you
create your project It'll ask you to name your project so you'll put in something like first- react and hit
enter then it'll ask you to select a framework as you can see there are other Frameworks that are supported by vit
we're going to go down to react and for this you just use your arrow keys and hit return to submit once you do that
it's going to ask you which variant you want to use we're just going to keep it as simple as possible for now and just
use the regular JavaScript version hit return to submit that again and everything will get scaffolded and ready
for you to run and helpfully enough it tells you exactly what to do we're going to first CD into our project then we're
going to run npm install which will only take a few seconds to finish and at this point once we're finished I personally
prefer to run the development server inside of the integrated terminal in vs code and so I'm just going to use
codespace dot that's the shortcut for opening the current folder inside of vs
code and once I'm in vs code I can run npm run Dev this will spin up a
development server on Port 5173 and I can just go to Local Host colon 5173 to
see the default project that is created with vit at this point you can interact
with the different files and the code that you see if this truly is your first time interacting with react it might
seem a little bit over in you would go directly here into the SRC or Source folder and find a couple files there
essentially you can delete most of the content of those files but it's always good to kind of play around in a new I
guess you could call it code base just to get a lay of the land and with that you should be completely set up to run a
react app locally with vit again because I'm going to be giving you a number of challenges many of which include some
starter code I still recommend being here on scrimba to do those challenges with as few barriers as possible the the
more you can get your hands on the code the better you're going to learn react before we jump into some of the more theoretical reasons as to why people
have really adopted react so heavily I want to sort of jump in a time machine and go back to see how this react looked
in the very very early days of react we'll get a chance to get our hands on the keyboard and really dive into some
code before taking another break and learning a bit more about the history of why we enjoy
react let's spend just a minute talking about JavaScript libraries and JavaScript Frameworks at this point in
your Learning Journey you may have heard these terms before and wondered what they were so I think we should go through them first let's talk a little
bit about the difference between what a library is and what a framework is generally speaking a library is
something that is just a collection of reusable code when you're programming sometimes you'll find yourself having to
rewrite some logic over and over and over again maybe even across different code bases and this is kind of where
librar step in the point of libraries usually is to reduce the need to write some repetitive or complex things from
scratch over and over because it's just a collection of reusable code it's really up to you how it's going to be
used when it's going to be used there really aren't any boundaries that you're expected to stay within its main purpose
is just to simplify the task that you were already going to be doing a framework on the other hand is a bit
more structured it usually has some kind of predetermined architecture and expects you to follow a specified
pattern of development oftentimes it's pretty important that you're very familiar with the documentation for
Frameworks because they do expect you to follow their patterns instead of essentially having no boundaries like a
library often has you are expected to work within the boundaries that are set by the framework maybe put a little

simpler there's kind of like a right way and a wrong way to use the framework itself so the question often comes up is

react a library or is it a framework well if you go to the react homepage it specifically calls itself a library it

says it's the library for web and Native user interfaces honestly react has been

built out as a whole ecosystem these days to a point where one of the most common ways to use react is to do it

using a framework like nextjs we're going to be talking about that in a second I think it could be really

interesting for us to take a quick overview of the history of some very popular libraries and Frameworks in

JavaScript we back in 2006 there was a really popular library that was introduced called jQuery and chances are

you have heard of jQuery even if you're pretty new to web development I would not be surprised if you've heard of jQuery one of the main purposes of

jQuery was to bridge the gap between different browsers and how they interpreted JavaScript to interact with

the document object model or the Dom jQuery made it a lot easier to achieve that cross browser compatibility whereas

before with regular JavaScript it was kind of a question you might write some JavaScript that worked well in Chrome

but didn't work in Firefox or Safari jQuery definitely falls into the realm of a library its syntax essentially

accomplishes the same thing that regular Dom JavaScript can accomplish but with a syntax that's a lot more tur and some

would say more familiar or easier to deal with then around 2010 there was a bit of a surge in JavaScript Frameworks

when angularjs Ember and backbone came out there were definitely others at the time as well but these were a little bit

more closely aligned to a framework they expected you to do things a specific way and they started introducing the

concepts of components on the web angularjs actually has kind of a funny history it was created by engineers at

Google its original name was simply angular and then later around 2013 when

react the new angular and vue.js came out angular the original angular angular

one I guess you could say rebranded as angularjs so that the new version of angular could simply be called angular

around the same time we also saw react and I think just a little bit later view JS came out and these three libraries

slf Frameworks sort of represented the next wave of how to build web apps in JavaScript things definitely did not

start slowing down at 2013 they only got more intense in 2016 we saw the release

of spelt and nextjs which is a full stack framework that uses react as its UI library and from 2020 on we saw a lot

more showing up in remix solid Astro quick Redwood Alpine there's so many

others that have shown up since then each one of these has its own unique approach to web development both

front-end and full stack web development and it definitely can be pretty overwhelming to consider the realm of

possibilities that exists out there so of all the different choices that you have to learn why choose react for many

of you taking this course you are probably looking at react because it has the highest job demand if you're

considering getting into web development or you're trying to level up your skills as a web developer I'm sure you have

noticed that react has probably more job demand than any of the other libraries or Frameworks out there this is why we

at scrimba have chosen react to be the friend and library of choice in our friend and developer career path maybe

as a quick aside it's also important to note that often times people hiring web developers they're not going to be

turned off by somebody who doesn't know their specific stack they know that they're going to have to train somebody

in their own stack and they're really just looking for somebody who has the capability of learning and building cool

things that said it definitely doesn't hurt to choose a library like react that already has the highest job demand

another thing that makes react a great choice is that it has a huge ecosystem and community that supports it between

the react deflex Discord server the reactjs subreddit and the wealth of npm

packages that were specifically written for react code you are definitely surrounded by a great ecosystem with

react another thing that some people report they really like about react is that it has less magic that's happening

behind the scenes don't get me wrong react is doing a lot of magical things behind the scenes but you as the

developer are often expected to Simply rely on regular JavaScript methods to

accomplish certain tasks and react whereas some other Frameworks expect you to learn their framework specific way of

doing something as we go through this course I think you'll see a few examples of that this next one isn't specific to

react but it's very composable and declarative this is a great reason to use react as opposed to just not using a

library at all and lastly react is being very actively developed the team at meta

were the original ones to create react back in 2013 and it's been actively

developed ever since now a question that I very often see in our scrimba forums and subreddits where people are learning

programming is asking do I really need to learn JavaScript before I learn react and my personal hesitating emphatic

answer is yes you absolutely have to know JavaScript before you jump into

learning react if you tried to learn the two at the same time it would become very easy to conflate what is Javascript

and what is react and I think doing so would be a huge step backwards in your education in web development so that's

why in the introduction to the course I specifically say it's important to already be familiar with HTML CSS and

JavaScript before trying to learn react now Library and Frameworks they're not for everyone so let's talk about when

you might not want a framework if you were just working on a simple static landing page for a business or your own

personal website it might be fine with such a small project to just stick to the core Technologies of HTML CSS and

JavaScript remember that Frameworks or libraries like react are a big code base of their own and they will have to be

pulled down to the users's machine anytime they want to run your project on Modern fast networks that's not usually

that much of a problem but if it's it's just a simple small project or if you do have Network load concerns maybe you

need your app to correctly run on slow 3G networks in different parts of the

world then those would both be good reasons to just skip using a library or framework altogether or at the very

least to use a very lightweight one these UI libraries and Frameworks also come with quite a hefty learning curve

compared to just the core Technologies so that's something you might need to take into account when you're deciding

whether it's the right time to use a framework also where the core Technologies of HTML CSS and JavaScript

are not evolving or changing that often Frameworks do tend to be improved and upgraded so you may find yourself

spending a fair amount of time doing maintenance to your application upgrading to the newest version whatever

it might be and it's possible that's not something that you want to spend your time doing and lastly if you are already

embedded in a codebase it's possible that the framework of your choice may not be super compatible or at least not

easily compatible with your exist existing code base in the decisions you make in all of web development you'll

find that there's always tradeoffs and so these are just some of the concerns you might want to keep in mind when it

comes to choosing your library or framework okay let's get back to talking about some of these reasons to use react

by talking about this specific point here how react is composable and

declarative when we first wrote this code I mentioned that it can seem a little bit strange for us to have what

looks like h HTML directly here inside of our JavaScript and that's true in fact when react was first introduced

there was a short amount of time when this syntax didn't exist at all instead react exported a function that was

called create element now this is not to be confused with the document. create

element although the concept is pretty similar you see within react we can call this create element function and it

takes three parameters the first parameter is what type of element you want to create very similar to

document.createelement the second parameter is something that's called props we're going to spend a lot of time

in props a little bit later for now because I'm creating an H1 I'm just going to pass null here because I'm more

interested in showing what gets returned from this than anything else the third parameter is what children we want our

H1 to have in our case this is an H1 that's just going to have some text so I'm just going to put some text in here

and we'll say this is Hello from create element okay I'll hit save we see we get

essentially the same thing that we had before the syntaxes maybe not as familiar and a little bit more verbose

especially by the way once you start to Nest these inside of each other but I'm not really planning to go deep down that

rabbit hole instead what I want to do is take the returned value from this function and save it in a variable let's

go ahead and call this uh react element I'll set it equal to this create element

call and we'll go ahead and still render our react element but now that I've done that I can console log react element and

let's open up the console and see what we get okay look at that so what create element returns is an object that has

some information about the Dom node that is going to get inserted by react into our actual Dom notice this object is

just a regular JavaScript object it needs to be structured in this way so that react can understand what it is but

it's just a JavaScript object remember this because it will be key for us down the road when we start talking about jsx

so long story short in the very early days of react they created this function called create element it still exists

today as we can see we're in version 19 and we can still use it and create element returns a regular JavaScript

object with a specific structure that makes sense to react now I don't have firsthand experience with this but I

suspect that the react team realized that this wasn't going to be a long-term solution and so they created jsx which

is that HTML looking thing that we saw in the beginning of the scrim let's take just a minute to look really quickly at

jsx and then we'll pull up some more slides and we'll talk about some of the main reasons why we care about react so

much as you can probably tell using Create element is not the greatest developer experience we didn't really go

into it but if you wanted to Nest elements together like if you had an H1

that had I don't know maybe a span inside with some text well you would

have to take your create element and then instead of the children being just a text node like this it would be

another react element which you would have to get by calling create element and so then you would have your span it

would have let's just say no props and then it would have its own children I'm inside the span and so forth definitely

a far cry from how we're used to adding elements to the D with HTML and so pretty shortly after react was initially

released the same team that created react also created the Syntax for jsx

which allows developers to write what they're already very familiar with in writing HTML if you want to add a span

in here just like in HTML you would simply add a span and under the hood react is going to take this set of jsx

elements that are nested together and it's going to turn them into those create element calls that we saw before

let's clean some of this up this one's just sitting outside here and we no longer need create element let me go

ahead and change this H1 to just be a regular H1 that says hello from jsx and

notice what the console still says this is from before we made this change and it still says hello from create element

as the children we go ahead and hit save and we get an object with the exact same structure so the main point I want to

get across is that jsx is simply what we call syntactic sugar on top of the

create element call and under the hood react is taking this jsx syntax and turning it into calls to create element

now there is a bit more to the object that we see here for example I can't just copy the object I see in the

console and paste it in place of react element or try to type this out manually there is a little bit more happening

behind the scenes but that's not really that relevant for you in this stage of your react Journey next we're going to

pull up a few slides and learn a little bit more about some of the reasons that we love react but I don't want you to

forget the syntax you see here because I will be giving you an exercise requiring you to write it all again from scratch

we're going to be covering a bunch of different reasons why react is a great choice for libraries to be learning at

this point in your Learning Journey but there's two main reasons I want to talk about why it's best that we graduate

from just using the vanilla Technologies of HTML CSS and JavaScript so what makes

react so great well the first major reason we're going to talk about is that react is something called composable all

this means is that we have the tools available to us that allow us to easily create reusable and interchangeable

pieces of the web that can be combined in a lot of different ways to create complex systems now I'll admit this next

analogy is not the absolute Perfect Analogy but let's talk for a second about what is arguably the most famous

statue in the world this is Michael Angelo's statue of David and I've had the privilege of seeing this in person

in Italy and if you've never seen it in person you might not understand just how large the statue is it is a 14t tall

solid marble statue when this was created Michelangelo had a block of marble and he carved away chunks of that

until what was left was the statue that you see here my point in showing this is that the statue of David and all

sculptures that were carved as a single solid block of stone or whatever material what you have left is a single

unit and it can't be reused or repurposed in any way which for artwork makes a lot of sense now the reason this

might not be the absolute best analogy is because this next picture is not nearly as beautiful as the original

Statue of David if if we are to set Aesthetics aside you can see that someone has replicated the statue of

David with Lego bricks again not nearly as beautiful but I think it encapsulates the principle of composability really

well if you've ever played with Lego bricks you know that they usually come in a big jumbled pile and you can use

those Lego bricks to create whatever your mind can conjure up each one of those little Lego bricks can be reused

and repurposed in a lot of different ways some of which are really rudimentary and simple and some of which

are pretty complex like replicating the statue of David in artwork obviously this is more beautiful but in web

development it's a very powerful tool for us to be able to take little pieces and combine them together in complex

ways let's take a look at a small piece of code here what you see here is a snippet from the bootstrap website if

you have been in web development for a while you might be familiar with what bootstrap is it's just a pre-built CSS

library and I took this directly from their website where it showed a bu of different examples of navigation bars

this is over 30 lines of code that represent a single navigation bar that by itself is not that remarkable

navigation bars can often times end up being this long or much longer but if you were around in the early days of the

web you might have seen a series of HTML files Each of which was a different page on your website and anytime you wanted

this navigation bar to be at the top of that web page you had to copy and paste this code to a separate HTML file this

meant that the first 30 something or more lines of code were dedicated to a navigation bar and the only thing that

really changed would require you to scroll way down the HTML page to find not only that but if you wanted to make

a change to this navigation bar you might have to make it in a lot of different places now we can contrast

that with what we get with react which is custom components you can even hear the similarity in the name there these

represent components that are more composable I've given these kind of silly names here to really highlight the

fact that these are custom there are things that I have created they're obviously not native HTML elements but

instead a custom component that represents all of the code that we saw here this my awesome navbar encapsulates

all of this code and then anytime in my document that I want to include a Navar

I can simply render a copy of my awesome navbar and I will get everything that

comes with the code that we see here and if I want to make a change I can make that change in one place and it will

reflect everywhere my awesome Navar is used now we're not fully ready to jump directly into the syntax of react but I

wanted to give you a chance to get your hands on this and really just kind of figure things out as you go interacting

with code that is unfamiliar to you is a great way to obviously become familiar with it and to really create those links

in your mind that will help you understand this in the end you can see in our mini browser that I have that bootstrap navigation bar showing up here

and in root. render I have this my awesome Navar custom component if I scroll up we can see the code for that

custom component and that starts right here on line four one thing you'll notice is that throughout the code I am

using class name instead of just class that's not a mistake it's something that we do have to do in react we're going to

touch on that later but for now what I'd like to do is give you a challenge that will require you to deduce what I have

done here and try to create your very own custom component in react let's scroll down here and I will add a

challenge here okay your challenge is to create your very first custom react component using

the my awesome navbar component above as your template you'll call your new component main content and just have it

return a simple H1 element that says something like react is great after you create that new component make sure that

you are rendering it inside of root. render just like we are with my awesome navbar just render it right here below

that okay I'll hand it over to you time to work on this challenge

okay well we can look above to the example of my awesome Navar and see that to create a new component we just have

to create a new function and that function will return some jsx in this example that jsx is much more complex

than what we're going to do but that's okay so down here let's go ahead and create a new function called main

content and we'll have it return some jsx we'll just have it return an H1

notice that in the case above we're returning everything collected together in parenthesis this is just a way for us

to be able to start our markup on the next line we're going to talk more about that later but I don't necessarily have

to do that if in this case I'm just returning a simple H1 let's go ahead and say react is great okay I can hit save

and notice that our H1 is not showing up well we've created this function but we're not you could say calling it or

rendering an instance of main content we can do that by surrounding the name of

our function in what looks like HTML tags let's go ahead and hit save and

there we have our react is great main content component is rendering to our mini browser this is awesome a quick

note I do have to put this slash towards the end if I don't include it then I get some kind of scrimba Errors showing up

here so it's important that for self-closing components which is mostly what we'll be dealing with in this

course I do have to make sure I include that slash at the end and that covers the concept of composability and react

as we prog rest through the course we are going to go a lot deeper into the concept of composability we'll see a

bunch of different ways that we can make our components much much more composable than they are just as we see here but I

think this has been a good start and a great way for us to get our hands on the keyboard next we're going to talk about

another major reason why people love react and front-end libraries like react in general and that is that it's

declarative so that's what we'll be talking about next

another reason that we love react is because it is something that we call declarative declarative simply means

that we can lean on the library of react to handle all of the manual tedious

tasks that we otherwise would have to worry about ourselves and I think understanding declarative is most

helpful if we look at its opposite which is imperative so with something declarative we can tell the program what

should be done and we can think of it like the computer saying just tell me what needs to happen and I'm going to to

worry about how to actually do it whereas with the opposite of imperative we need to describe how things should be

done this is like the computer saying I need you to describe to me every single step along the way on how to do

something and then I'll execute the steps that you tell me to execute let's see an example of this in code so we

have here just about as basic of a react app as you can possibly have which is all we've really worked on so far but I

want you to get your hands on the keyboard and try out a challenge okay your challenge is to recreate this above

line of code which is actually still showing in our mini browser cuz I haven't hit refresh yet but by recreating it in vanilla JavaScript by

creating the H1 using the create element method on the document giving it some

text content just using the text content property of the new element you created then giving that new element a class

name of header and then using append child to append this new element that you created to the with the ID of root

and by the way just so that we really drive this point home I don't want you to use inner HTML to accomplish any of

this using inner HTML is a little bit shady anyway there's some situations where you can get in trouble by using it

anyway if it has been a while since you've done this kind of manual down manipulation it's okay to search on

Google to figure out how to do this use chat GPT to help you out just don't let chat GPT write all the code for you and

and then copy and paste it okay it's your turn work on this

challenge okay so we can get our new H1 let's say this is going to be we'll just

call it H1 and we'll use document.createelement we'll create a new H1 element we can add

some text content to it by accessing the text content property and maybe we'll

just say this is manual imperative

coding okay I can give my H1 a class Name by setting its class

name equal to header and then I can grab the div with the ID of root by using get

element by ID we'll grab the root and then I can say append child and we'll append the new H1 there now I don't

think I've actually set up a class of header but that's okay let's hit save and sure enough that works just fine

this is imperative coding though as the header says and it's because we've had to manually tell it every single step of

the way first create a new element then manually add this text content to it then add a class name to it and each one

of these has to be on its own line of code then take this new H1 child that we have slowly built up over time append it

grab the element with the IDE of root append the new H1 to it and as this says

this is really imperative we have to tell it every single step of the way what to do the way that we have just

seen how we do it in react is of of course quite a bit more declarative here we can simply say hey react I'm going to

let you figure out how you should really turn this into a text node inside of an

H1 element we of course would say the class name is equal to header in order

to be consistent with what we have down below and react is going to figure out how to do this a really good analogy

that I have heard of to illustrate the difference between declarative and imperative is if you were to go to a

restaurant and tell the host I'd like you to lead me down the hallway by 50 steps and then turn right we'll walk

another 35 steps and I'd like you to then seat us at the booth on the left in that case we have had to direct the host

on every single step of the way how to set us down at a table at a restaurant the equivalent declarative way is to

trust that the host will know exactly how to do their job and all we would have to say is something like we would

like a table for four the host might then walk us to the exact same booth that we otherwise manually directed them

to csat but we've been able to offload those specific instructions to a person

or in the case of react a library that we can simply trust to do its job now of

course with something as simple as putting a single H1 on the page well first of all we likely would just do

something like that directly into our HTML but with react where most of the content on our page is going to be

created in JavaScript this example already demonstrates how much nicer it is to do it in a more declarative way

and especially if you think of all the steps that would be required to create even something as simple as this little

section project that we're going to work on it's just going to be so much easier to do it in react where every element

can be structured and look just like HTML without us having to do all of the imperative manual tedious task of

creating these text nodes and appending them to text elements and appending those text elements to their parents and

so forth speaking of the react FAA project that you see here it's time for us to jump in and start creating this

from scratch before we jump right into our

section one project of react facts there's just a little bit of I guess you could call it housekeeping that I want

to take care of just so that we are set up to have success in working on this project and in my regular Style I want

to start us off with a challenge I know you just did this exact same thing but we're getting those repetitions in so

that you can build the muscle memory in your fingers I want you to set up a new react tap from scratch I've given you a

couple hints here that should help you along the way and in the end I just want you to render a simple H1 element just

like we did before okay I'll hand it over to you work on this

challenge all right let's clean up this text and we need to import the create

root method from react-dom client with that we can create

a root and we do it of course by calling create root then we we need to pass to

create root a Dom node where all of our markup will be stuffed inside of and react is going to handle all that for us

so we just need to grab that Dom node by calling something like document. get

element by ID or query selector we'll go ahead and use get element by ID to get the element with the ID of root once

again that's in our HTML it's our actual markup right here and react will be in charge of putting all of our markup that

we eventually create in react right inside of this div so this tells react

where to eventually render the markup and we need to then call the render method on the root so root. render and

this is where we tell it what to render we'll go ahead and put in our jsx and we'll just say this is react I

don't know I'm not getting very creative here okay hitting save should make this show up it should say this is react

perfect okay great job let's tackle the housekeeping I want to handle first I mentioned in the very beginning that you

you might have noticed we're using this jsx extension instead of a regular JS

extension I'm actually fairly certain this would work if I were to rename this to just index.js and hit save we're

still working however under the hood we're using vit which we did see a lesson on how to set that up locally and

in the documentation of vit they recommend that if you ever have a Javascript file in react that is using

jsx in any capacity then you should use a jsx X extension instead of a regular.

JS extension we won't necessarily go into why V expects you to do that just

know that it really helps vit in its ability to bundle your code performant and just make things work smoothly in

the end so it's now. jsx I need to come make sure that I'm referencing the jsx

file and keep in mind before I wrote this line I really wouldn't have needed to do that and if we were using that old

API using Create element and doing all of this manually without jsx then we wouldn't have to rename this to a jsx

file but because we are using this H1 right here with jsx we need to make sure that it is a jsx file okay that was one

of the things I wanted to cover the other little point of housekeeping I wanted to handle at this point was to talk something about images in the react

fax project we do have two logos we've got the react logo up here in the header of this little project and then we also

have the logo floating around down here on the right side with static images that aren't going to be changing or

aren't coming from some kind of CDN or database there is a kind of unique way that you have to deal with them that's

different than what you might be familiar with when using vanilla HTML CSS and JavaScript let me go ahead and

take the project that you just built here and first of all we'll go ahead and put this on its own line so we can just deal with this single line here by

itself and I'm going to change it to be an image element when you're writing static HTML you are probably pretty

familiar with saying that your source is going to equal a string and then that is going to to be a relative path to where

your image is living I've put the react logo PNG file on the same level as my

index. jsx file and so I should be able to Simply say

react-app file and run it locally install the dependencies it would be using vit in the background this would

still continue to work however if you aren't really following along here in scrimba and you set up a

new vit project there's a chance that putting a relative path in your image source like this wouldn't work correctly

so I wanted to address that now if anybody who isn't following along here in scrimba finds that when I talk about

putting your image path in the same way that I have here where it's just a path that's relative to the current file that

you're writing in and you find that it's not working the quickest solution for now is to just make it an absolute path

from your route for example if all of your code is in an SRC folder you might

put slsrc and then keep working your way down to where this actual PNG file is

maybe you have like an assets folder like that and when you do that this will start to work again now my point of

housekeeping here is to let you know there is a better way to deal with static images in react but we're not

quite yet set up to learn about that that's actually going to happen in the next section but again I just wanted to

get ahead of it a little bit at this point so that there isn't too much confusion happening from those of you

not following along here in scrimba and there is one final point of housekeeping I want to take care of now and that is

to talk about what you do when you want to render multiple elements inside of your render it's really common for us to

have components and react that render more than just one HTML element however you'll notice if for example I have an

image and then I also try to render let's say underneath it an H1 that says

this is another element I'm getting this warning here and if you have over it it says jsx Expressions must have one

parent element and it's true when I'm trying to render something I cannot render two elements side by side in the

way that I'm attempting to here remember when we learned about how jsx compiles down to that call to create element and

this is a create element from react so I'll just go ahead to make sure that's clear we'll import create element from

react well trying to render two jsx elements side by side like this would

kind of be like trying to do this create element create element of course I have

a problem here and I don't think this is exactly what it's trying to do but I find it helpful to think of it as a

problem in terms of trying to call two functions back to back like this on the same line let me get rid of this syntax

error so that we can deal with this other one and of course I'm not limited to only ever rendering one thing at a

time I just need to make sure that it's wrapped together in a parent so in react this simply means means that if I want

to have two elements I need to wrap them into a single parent element that can house both of those elements together

this is kind of akin to how we saw we can have create element in this case it would be similar to saying we have a div

we're not going to worry about props and then the children would be calling another instance of create element and

this is okay to do now for accessibility reasons div should probably be the last

resort of what you reach to there are a lot of other semantically correct HTML elements that we could use in its place

for example maybe a main element would make a little bit more sense here or if it's a section it could be a section or

an article it can be really helpful to go over to mdn and learn about these semantically correct containers and

choose the one that makes the most sense okay we've covered a lot of ground in this random housekeeping lesson as a

quick recap if you're ever going to have any amount of jsx inside of your file make sure that you rename your file

extension to be jsx instead of JS secondly when it comes to images actually let me fix the path here cuz

hopefully that didn't cause too many problems we can see that this is working if I scroll down we have our H1 there

when it comes to images for now I'm just going to be using a relative path and there's a chance that doing so inside of

a freshly created V project would cause problems so I showed you how to use the absolute path from your project route in

order to make this work for now and we'll be seeing a kind of more accepted way to do this later and last of all you

can only ever render a sing single jsx element at a time and that element can have as many children as you want but

there does need to be one parent element that encapsulates all of the other elements you want to show up on the page

with that we are now poised to start working on our react fax page and we're just going to take it one little step at

a time all right I'm excited to get

started on our section project as a reminder this is what we're aiming for and in this particular challenge we're

aiming for this point there's some really rudimentary styles that I've included in our index.css just so that

this didn't look quite so much like an isore but notice for now I'm just styling the core elements and you won't

have to worry too much about this at this point you are starting from scratch again I'm sorry if that feels a bit obnoxious I do want to have your memory

working so that you're not just cruising along through this course without putting in the effort some hints here if you're doing this here in scrimba for

the image source you can just set it equal to react logo.png I've included that here in the project on the same

root folder as everything else but as I mentioned in a previous scrim if you're following along locally with a vit

project that you set up manually then you might for now have to put an absolute path to this logo we're soon

going to be learning about another way we can pull in images when they're static images but for now we're not

quite there yet also since we haven't officially learned about how to tie class names into our jsx or do inline

Styles when you render this image it's going to be quite a bit larger than what you see here but you can just use the

width property just like you can in HTML in my example down there I just have it set equal to 40 pixels in width okay

enough talking I'll hand it over to you to get started on this

challenge okay we can go ahead and import create root from

react-dom client we'll create a root with create root remember when we're

doing this we pass to it where we want react to put everything so we'll grab the Dom node where we want everything to

get put inside of and that will be with the div that has the idea of root in our HTML right here and then when we call

render we're telling react what we want to put inside of that div as a reminder

I can't render an image followed by a sibling H1 followed by my unordered list

but instead I need to make sure that I'm only ever rendering a single parent element that surrounds everything I

could choose a div if I wanted to I usually tend to do that as a last resort for now I'm just going to call it a main

because that feels a little bit more semantically correct okay let's surround these with the main like that and I'll

go ahead and stub out my unordered list with my five list items let's start with

the image and I'm going to add the source equal to react

logo.png and we'll see when I save we get quite a large image here this is where I think normally I would resort to

adding some CSS to style this but for now we can see that we can just add width like we would in HTML and set this

equal to 40 pixels okay quite a bit more manageable let me go ahead and fill in the rest of the text and I'll just cut

to a finished point for that so you don't have to sit and watch me do that and there we have it all of our text is

added in one last thing I need to make sure I do is to add some alt text to my image so I'll just say this is the react

logo and awesome now of course the project that we're working on here is very very small in scope compared to a

full website or web app that you would normally see and right now we're just kind of stuffing everything right here

inside of root. render and I'm sure as you have probably figured out or can imagine this isn't going to be the

long-term way that we do this so next what we'll be doing is learning about how to make custom components which will

allow us a lot more flexibility and certainly a greater sense of organization than just trying to stuff

everything inside of root. render so that's what we'll be doing next but before we jump into that I have a little

quiz that I want us to take just to reinforce the concepts that we've learned so

far let's do a quick quiz before we move on and start learning about custom components in react and what I'm going

to do is Mark this as a challenge in scriba which will pause the playback and give you an opportunity to actually

click here into the editor and type your answers down and I would recommend actually typing the answers down because

there's something about having to verbalize or write down your concise answer that requires you to think

through it a little bit more rather than just kind of thinking within yourself I kind of get the answer to that question

so when it pauses actually click in here read through the questions answer them and then we'll go through it

together okay where does react put all of the elements I create in jsx when I

call root. render remember there's two parts to creating this root and using this root the first part is creating the

root and telling it where you want to put all of the elements that get rendered and then the second part is

what you want to render in that spot so when react renders all of this it puts it all inside of this div with the ID of

root because that's the one we selected when we created this rout and you can actually verify that even here in

scrimba if you open your developer tools and you select one of the elements in the mini browser here if you dig deep

enough you'll eventually find this HTML document nested inside of the HTML document of the scrimo window and you

can find the div with the ID of root and you can expand it and you'll see this main element and it will have an image

in an H1 and unordered list and everything so let me actually type down an answer

here okay it'll put all of those elements inside of the div with the idea of root or of course you could choose a

different element when you're calling create root and it'll put it inside of that element instead okay number two

what would show up in my console if I were to run this line of code console log H1 with the text hello world I

intended this to be a little bit more of a generic answer not necessarily giving me the exact structure but the answer is

an object this object is just a plain JavaScript object it does have its prototype chain set up in a specific way

that react can recognize and use it but it's just a plain JavaScript object if we were to create a new element or

create a new text node or something like that in plain JavaScript and console like that it wouldn't be just a regular

JavaScript object it would be an instance of whatever it was that we were creating like a new HTML element for

example so let me fill out this answer a little more and I just wrote out essentially what we just talked about

okay number three what is wrong with this code hopefully it was clear that I wasn't expecting you to say Well it

needed to import the create root method or anything like that but instead the point is that we can't have two sibling

elements being rendered together like we show here instead there has to be some kind of wrapper comp component or

element rather so we might have a div or let's say a section Just for kicks so

this would be the correct way and now nothing is wrong with this code let me type that answer down again you can only

render one parent element at a time and as a reminder that parent element can have as many children elements as you

want to put in there okay let's scroll down a little bit number four what does it mean for something to be declarative

instead of imperative imperative means you need to tell the computer exactly

how to do its job step by step you give it very specific instructions for it to accomplish the task whereas declarative

we can lean on the library or framework or whatever it is that we're using to do

the heavy lifting for us and we can write our code in a lot more of a descriptive way and let the tool like

react handle the heavy lifting for us you might have participated in or seen one of those challenges where you're

supposed to describe to somebody how to make a peanut butter and jelly sandwich and when the person takes the

instructions very very literally it usually ends up as a big mess that's more like giving imperative commands to

doing a regular task whereas the declarative way would be to say please make a peanut butter and jelly sandwich

and you would just trust that the other person knows how to handle all of the steps along the way I think another

helpful way to think of the term declarative is to use this word describe declarative means we can write our code

to Simply describe what should show up on the page and allow the tool like reacts to handle the details on how to

put those things on the page HTML for example is a very declarative language because you simply describe the contents

of a page and we expect the browser to know how to handle displaying that in

vanilla JavaScript when you're trying to create a bunch of elements on the page it's very imperative because without

something like jsx you can't simply type out the structure of your page you need to create the nodes individually and

append text to to them and add click handlers and all sorts of things like that I think I'm belaboring the point a

little bit let's move on to number five what does it mean for something to be composable all composable means for us

in web development is that we can take larger sections of what we're trying to build and break it down into smaller

pieces we can make those pieces flexible enough to handle multiple different scenarios so that they can be reused in

multiple different ways which allows us to in the end write a little less code which leads to fewer bugs and and allows

us to make something greater than if we just tried to I guess metaphorically carve the final product out of one

single giant block of stone so as an answer that might look something like this when something is composable it

means that we have small pieces that we can put together to make something larger or greater than what the

individual pieces themselves could possibly make great job on this quiz hopefully all of this was pretty

straightforward at this point this is a great chance to do some self-reflection and see if you think you might be fall

in behind then this is not the time to just keep pushing forward remember nobody's giving you a grade for this

course you're not going to receive some kind of award by going through it quicker in fact in the end you're less

likely to get the outcomes that you want if you plow ahead without understanding what we're learning keep up the great

work and next we're going to look into making custom components in

react when we first started talking about components we saw this example where we can encapsulate a bunch of

logic inside of our own custom components almost like our own custom HTML Elements which gives us a lot of

flexibility to reuse those elements whenever we need to make changes in one place and have it reflect that change

everywhere and ultimately provide us a lot of composability with the way that we write our user interfaces so far we

have not really been doing that at all we've been stuffing everything inside of root. render which has served us really

well as we're learning the basic syntax but it's time for us to jump into creating our own custom component now

it's not actually the first time that you've done it because you got your hands on super early in the course where

you were able to create your own main content component and what we saw back then was that we use the concept of a

function to give us the power of reusability and I'm sure this is a familiar concept because functions are

used in every programming language that I know of and its purpose is to encapsulate reusable pieces of code

allow you some flexibility with things like adding parameters to it and then to call that function whenever you need to

accomplish that task and that's exactly what we do when we're creating custom components let's see an example of how

we might into it creating custom components and then we'll see just some really slight tweaks to make it sort of

the more accepted react way let's say I wanted to take everything here that I am currently rendering inside of root.

render and put it inside of its own custom component well just like any other function let's go ahead and try

this we'll say I want to return this markup and notice that here I'm starting

with the main element right here on the same line as my return this is viable as long as I start on the same line with my

jsx all of the other jsx will kind of follow as part of the return however

it's much prettier to put this inside of parenthesis I can just wrap everything inside of parentheses and that allows me

to keep my jsx markup on its own lines let's give this function a name maybe we'll just call it uh maybe temporary

name for now clearly we're going to be changing this and I probably should spell temporary correctly okay well what

would happen if inside of root. render instead of having all of my jsx there I

just called temporary name let's make this a little bit larger and let's save it and see what happens and look at that

it's working just fine and this makes sense because we're returning those JavaScript objects that get created with

jsx code from our temporary name so it's essentially the same thing as if we just cut this out and pasted it in this

temporary name function calls place however when we're dealing with react as you have seen this isn't really how we

render these components the first thing to know is that with custom components in react we have to use something called

Pascal case it's essentially the same thing as camel case where normally you would have a space you remove the space

and put a capital letter the only difference is we need to start with a capital letter as well so we would have

temporary name with a capital T at the beginning so let me go ahead and change this up here and then the only other

difference is instead of calling it like a regular function with the parentheses we would surround it in angle brackets

in very much the same way we would a self-closing HTML element okay let's hit

save and awesome things are working exactly like they were not only that but now we're following the regular react

convention okay guess what time it is it's time for a challenge and guess what I'm not going to make you write it all

from scratch again at least not right now okay the first part of your challenge is to to create a new page

component that page component should return an order list of the reasons why you're excited to be here learning react

don't worry too much about this list just throw something in there and make it fun then after you've created the

definition for that custom component make sure that you render it to the page so it actually shows up in the mini

browser okay good luck work on this

challenge okay well to create a new custom component we create a new function we call it page with a capital

P and we can have it return some jsx I'm going to surround it in parentheses so I

can put it on its own lines and we'll have it be actually supposed to be an ordered list and we'll just put in a

couple list items here maybe for one we'll say react is a popular

Library so I will be able to fit in with

all the coolest devs out there awesome and I don't know for the other one let's

say that I am more likely to get a job as a

front-end developer if I know react and I think there's some truth to that react

is the most popular UI Library out there knowing react doesn't hurt by any means when applying to jobs let's clean up

this challenge text and let's see what happens at this point if I hit save notice that our page is still blank well

that's because we've defined our component but we are not creating an instance of it we're not rendering it at

all again I technically could call it like it were a function and we see that that kind of works however the of course

much stronger convention is for us to render it as if it were an HTML element by surrounding it in those angle

brackets while we're looking at this I think it's important to note that while throughout this course we're mostly

going to be dealing with self-closing components like we see here any component that you create can also have

its own separate closing tag like we see here and you can see if I hit save it's

going to be working exactly the same in my Advanced course here on scrimba I do talk a lot more about this way of using

components this is another example of how components are very composable opening up quite a bit of power to

developers when it comes time to placing some elements inside don't worry too

much about this because as I mentioned we're not really going to be doing a whole lot of this throughout this course

so we'll just be sticking mostly to the self-closing syntax that we see here okay nice work on part one of this

challenge in part two we're going to be adding a little bit more to the page that we see here this would be a perfect

time to again do a self assessment to see if you are ready to move on one thing you could do and I'll mention this

a few times is you could just delete everything and see if you can build the whole thing again from scratch without

any help so I'll bring all this back but that is an exercise that you are more than welcome to impose upon yourself at

any point through this course when you're ready let's move on and we'll start on part two of The

Challenge all right let's get started on part two of this Challenge and actually at the end of this challenge our little

silly page that we're making here is going to look an awful lot like the react fa section project that we're

going to be building as well I've broken the steps down into three bullet points each one represents another section of

our page so the first thing I want you to do is to add a header element that will be the first thing that we're

returning from our page component and that will just have an image element inside make sure to read the text for

any of the details here about setting the source the width or the alt text after that I want you to add an H1 to

our main page that has something like Reasons I'm excited to learn react put it above the ordered list and then wrap

both the H1 and the ordered list in a main element again this is allowing us to maintain some semantic structuring

inside of our little page here then at the bottom you'll add a footer that just has some text like this okay I'll turn

it over to you go ahead and work on this

challenge I think the biggest trick in this challenge is that as soon as you

add a header you're now trying to render two sibling elements at once if you hover your mouse over here on the

closing parentheses where the red squiggly is it very helpfully tells us jsx Expressions must have one parent

element for now what I'm going to do is just add a div to surround these but very soon we're going to talk about

another way that we can accomplish this a div will work just great for us for now inside our header We'll add an image

element and we'll just go ahead and add those three attributes we have our source our width and of course width is

not a required attribute by any means very shortly we're going to learn more about how to use real CSS to do this

sort of thing and as always we should make sure we include our alt text okay

for our second bullet point here I'm actually going to work a little bit backwards I'm going to first surround

everything in a main element okay and then I'll add my H1

here at the top I think my spacing is a little bit funny here because of the way I had it formatted let me fix this okay

it's been a minute since we hit save let's go ahead and see how we're doing okay things are looking pretty good we

have one final thing and that is to add our footer and this wasn't really part of the challenge I think I'm going to

put this in a small tag like this just to provide it a little less emphasis and

let's just go ahead and copy what we see here and at the time of recording we are

in 2024 and uh my last name is zero so

we'll just put that in there and awesome let me hit save good now we're protected

from people trying to steal our really important code here let's go ahead and clean up the challenge

text and awesome hopefully that wasn't too big of a challenge if it was that's completely okay and again that's a

perfect sign that tells you that it's time to keep practicing this before pushing ahead now some of you seeing

this might be wondering why we're just shoving everything together into this one large page component this doesn't

really teach us about composability and how we can make our own smaller custom components that each do one little piece

at a time and you would be right we are going to be doing this very soon soon and that should improve the

composability and the readability of our code before we do that I have another quick quiz that I want to give and then

we'll jump right into making multiple different custom components and talking about the relationship between parent

and child components okay let's do another really

quick quiz you know the deal I'll mark this as a challenge it'll pause the stream and I actually want you to click

in and type your answers down under each one of these questions then we'll go over everything

together okay number one what is a react component simply put a react component

is a function that returns react elements okay so what exactly is a react

element well a react element is a react version of what we see in the Dom you

can think of it kind of like the react version of an HTML element and because jsx looks so similar to HTML elements we

call them reactive elements however the main difference is when we're returning react elements like our div and our

header and everything else that you see here well first is turning the jsx syntax into calls to react. create

element and then the create element function is turning them into JavaScript objects that react then is able to

interpret and turn into real Dom nodes under the hood so in answer to this question we say that a react component

is simply a function that returns react elements and I think the pluralization here is key sometimes you'll hear people

talk about how this is UI that the react component is returning this is just short for user interface it essentially

means the same thing we just talked about okay number two what is wrong with the code that we see here well it is a

pretty small change but we need to make sure that when we're defining our components in react we need to use what's called Pascal case and that is

where the first letter is capitalized the rest of it follows the regular rules of camel casing all right and then

number three what is wrong with the code that you see here the component itself is perfectly fine however when it comes

time to render that component and render in this case just means to create an instance of this component and let react

put it on our actual page we don't call it like a regular function as you see here instead we surround it in the angle

brackets similar to regular HTML syntax this is a way to signify to react that

we want to create an instance of this header component which under the hood essentially WS our component Returns the

header element with the image inside these react elements as we talked about in question number one which then

eventually get compiled down to those JavaScript objects which react then interprets as real elements in the Dom I

know when I list out that many different steps it makes it seem a little bit inefficient but trust me react is very

fast at doing all of this okay short and sweet hopefully you were able to follow along next we're going to be learning

more about how we can compose our components

together I mentioned that there would be an alternative to surrounding everything that we see here in a div like I did

here to avoid that issue with multiple different jsx elements trying to be rendered all at once and this workaround

is something that react has actually created itself we're going to import something called capital F fragment and

that comes directly from the react Library this is a so-called built-in component from react that we can use and

we can render it right here as if it were a regular HTML element we'll put

the closing fragment down here at the bottom need to make sure I close this correctly and I can indent everything

and we see that that error has gone away I can hit save and my page is going to display the same way it was before

there's a slight difference though in the resulting HTML when I had a div here

remember that I'm rendering that div and all of its contents directly here inside

of my HTML and so what I end up getting is another nested div whose purpose

doesn't really exists and then all of the other markup that I have here if I

were to just copy and paste this into my HTML this is essentially what react would be creating when I use a fragment

react will not actually insert another nested level of an element here it's a workaround that allows us to combine

multiple different elements together but without creating creting another Dom node that it has to worry about so by

using a fragment I essentially end up with this it's a little bit cleaner it doesn't insert unnecessary elements into

the Dom as much it also can have a couple other random side effects like when you're dealing with flexbox or grid

containers and child elements most of that is a bit beyond the scope of what we're concerned about right now let me

clean up my HTML here since react is going to be doing that work for us and one final thing I want to talk about is

this is is a little bit cumbersome to have to import the capital F fragment like this and so react has actually

implemented a simpler way where instead of typing out fragment I can put an empty angle bracket set just like this

and then I don't need to import anything so when you're looking at my code or other react code you might see these

empty angle brackets just like you see here and under the hood that's just creating a fragment which essentially

allows us to bypass that issue about rendering multiple sibling react elements together no real challenge with

this one just wanted to make sure I covered that base as we've talked about it's really

not ideal that we have a single page component and we're just stuffing all of our markup into that page component

don't get me wrong in real react apps this is still a very very small component these components can sometimes

become hundreds of lines long and there's legitimate reasons to do it that way but that wouldn't be a great

learning experience for us as we're trying to learn more about composing our components together to help illustrate

this I'm going to provide a quick mini challenge for you okay in this challenge I want you to

take the header element that we're currently rendering inside of the page component and move it into its own

component called header then in its place I want you to render an instance of that new header component so that

when you hit save well everything will pretty much look exactly the same where you see it now okay go ahead and give

this your best shot

all right well if we want to create another component we won't want to do that inside of our page component here

but instead outside of it so I'm going to create a new header function it will

return the code right here these elements this header element and that

does the first part of the challenge next all we need to do is create an instance of that header component and

we'll do it in the exact same way that we've seen before and that we SE down here with the page component we'll

surround the name of our function in these angle brackets just like that I'll

hit save and my header is still up here at the top now of course when we're dealing with such a small application

like we see here this is probably Overkill I think I'm probably prematurely optimizing to create

separate components like this but I hope the idea is coming across when you're working on a larger application your

header is very unlikely to be three lines of code it might include a lot more dealing with user interaction

pulling in data from a database and all sorts of more complex things like that in those cases I think it becomes much

more apparent that it's really really helpful to move that kind of logic into its own separate component thus

compartmentalizing it and making it not only reusable but a lot easier to deal with as a developer okay let's continue

on with this challenge just to get a little extra repetition in the continuation of this

challenge is to move move both the main element into its own component that you call Main content and the footer element

into its own component called footer then make sure that you remove that from the page component and render main

content and footer in its place go ahead and work on this

challenge okay let's go ahead and create a new function called main content and

before I work on that I'll go ahead and create my footer component as well let's add a return to each of these okay we'll

come down here and copy the or rather cut out the main element here and put it

inside of our main content and we'll do the same thing with our footer again if I hit save at this point

we'll see that I'm only showing my header because my page is only rendering my header component so we'll go ahead

and render our main content and our footer hit save and we're back where we

started again I know this might seem a little bit tedious hopefully getting the repetition in like that is a good thing

as a react developer you are going to write hundreds and thousands of components so this is really just

starting you out on that Journey also again this is pretty clear that it's prematurely optimizing to create these

three separate components if you were to know that this was the extent of the page you were trying to create then you

probably wouldn't do this however in most scenarios it really does make a lot more sense sense to have a separate

header component maybe a separate footer component and then probably quite a bit more than just a single main content

component that contains the main portions of your site let me go ahead and clean up the challenge text and

before we move on I just want to talk about the terminology of parent and child components what we've done here is

set up a bit of a hierarchy where we have a page component and that page component which we're rendering right

here will on its own render a header component and the other two components and typically in a larger react app this

will continue on down the tree where for example the main content component might be rendering other custom components and

those ones will probably be rendering other custom components creating this tree hierarchy which results in what we

call parent components and child components and you can take that analogy as far down the line as you want calling

grandchild components and grandparent components which in the end allows us to really create a masterpiece of composed

custom react components together which similar to that statue of David made out of Lego bricks allows us to create the

website or web application that we want to create all right nice job on that challenge at this point I think it's

well overdue for us to learn more about how we can style our components because right now we're not doing a whole lot of

styling here we're doing some inline styling with the width attribute and I have some CSS that's just selecting

entire elements and so let's go ahead and see what it takes for us to add some CSS to our components

let's get started first by completing another challenge inside of our header right here where I've left a space for

you I want you to add a nav element inside that nav element you should add an unordered list which should contain

three list items and those list items should say pricing about and contact

don't worry at this point about any kind of styling it's not going to look very pretty go ahead and work on this

challenge okay okay so let's add a nav element like this inside that nav We'll

add an unordered list and we'll have three list items those will say

pricing about and contact okay let's see what we've gotten ourselves into we'll

hit save and it's beautiful done ship it no let's learn about some styling so that we can make this look actually like

a navigation bar instead of this weird 1990s website fortunately styling

something in react is not that different than you are already familiar with using vanilla HTML and CSS let me clean up

this challenge text and head over to our HTML file notice that we are linking our

stylesheet here inside of our HTML file which means just like in regular vanilla

HTML and CSS we can just add any classes that we want to our jsx over here in

react and then access those classes in our our CSS file in order to style them

however as we've briefly touched on there is one minor difference and that is whenever we're styling something in

jsx we won't use class equals but instead we'll use class name with a

capital N and there's actually a good reason for this I think a common misconception is that people think well

we're inside of a Javascript file and the word class is a reserved keyword in JavaScript when you're creating a new

class of something but that's actually not the reason that we use class name in react remember that react is going to

take these jsx elements and eventually turn them into native Dom elements and

when we're creating a Dom element like if I were to say we're creating a new

unordered list I would use document.createelement unordered list and then in JavaScript if

I wanted to add a class name to that I would say ul. class name equals and then

set it equal to the class name that I want it to have of course in vanilla Dom JavaScript there's also things like

class list where you can add properties and so forth but that's not what we're concerned with at this point under the

hood I'm accessing the native Dom properties of this unordered list that I'm creating in jsx and so something

you'll just have to become used to in react whenever you want to add a class to your jsx you'll use the property

class name instead so with our unordered list maybe we'll give this the class

name of I don't know n nav Das list maybe obviously in such a small setup it

might be easier just to select the nav and then the unordered list inside of nav but that kind of defeats the purpose

of learning about CSS with classes so with our unordered list with the class

name of nav list we can go over to our CSS and let's select nav list just like

we are used to doing with a DOT at the beginning because it's a class name and maybe the first thing we should do is

take off those bullet points by saying list style none and sure enough there it goes our bullet points are gone okay and

with that under our belts that brings us to the next part of our challenge the next part of the challenge is to use

flexbox and lined our list items up horizontally so that they're in line with the react logo which should in the

end look something more like this I think in this example I did bump up the font size but you don't have to worry

about that if you don't want to as I've written in the note here just for practices sake I don't want you selecting any bare elements like

selecting the entire nav or the entire unordered list but make sure that you add a class anywhere that you're wanting

to do some styling all right it's your turn to work on this

challenge I think the trickiest part with this challenge is having to create a couple different flexbox containers so

let's just start right here with our unordered list which we already have a class name for so I should be able to

say display flex and okay the items are lining up that's great I'm going to

worry about the spacing in just a minute but for now let's get it so that the logo and the unordered list are in a

line if we look at our markup again we have our logo right here and our nav is

the next item that needs to be aligned which means that the parent of these two the header is what needs to become a

flex container I could just select the header I think if I were doing this for real I probably would just select the

header in this case but I'm going to give it a class name of header just so we can get a little extra typing

practice in there and then in our CSS we will actually I'm going to put this above the nav list we'll say header is

display flex and oh I need to uh hit save here so that applies okay cool

those are now in a line of course it looks like things got a little bit squeezed with our logo which is just

kind of what happens when you make something a flex container with an image in it it will stretch it to be the full height in order to fix that I can say

align let's see items to the center and yeah that set my logo back to the same

proportions that it was before because I just have the two items the image element and the nav element I think I

can just say justify content space between and sure enough that pushed the

nav over here to the right and then I think I'm going to have to style each one of these list items and only because

I'm a man of my word I'm going to add a class name to each one of them in the real world I would just select the LI

Children of the nav list element we'll go ahead and call this nav list item

okay in our well let's hit save I have to remember to hit save on scrimo there and then we'll select the naav list item

and my goal is to get some spacing here I think if I put a margin let's try

margin right of 10 pixels and wow actually that looks pretty good I think

I might bump up the font size to just something like 1.1 R just to see yep I

think that's pretty good I actually think my margin right is putting a space over here on the right let's try margin

left and I think that might be a little better I think my nav and the rest of my page is going to line up a little bit

nicer that way now my image is looking a little bit smaller than I think I would like it to and so now that we know how

to add styles with classes let's go ahead and do a third part of our challenge all right the last challenge

in this scrim is to move the width style off of the jsx on the image here and

over into the CSS using a dedicated class name on the image element then make sure to change that width to 55

pixels instead of the 40 pixels that we currently have let's pause now to work on this

challenge all right let's give this a dedicated class name maybe we'll just call this nav D logo and I'll hit save

we'll go over to the CSS and access the nav Das logo give it a width of 55

pixels and well look at that it automatically applied immediately as soon as I finish that we can go over to

the element again and remove that 40 pixel width and okay that's looking pretty good now before we move on I want

to encourage you to take some time to put some additional effort into styling the page that we have here obviously

what we have is just about as basic as it could possibly get I did this myself and I put maybe 5 minutes of styling

into this and I think it shows it's definitely not going to win any Design Awards or anything like that but give it

your own little flare you don't even have to use this dark theme that we've been using you can switch it to something completely different and fun I

want this to be not only an opportunity to practice playing in the code which is probably why you're here on scrimba in

the first place but also to give you an opportunity to interact with the scrimba community especially the scrimba

community over on Discord there's a dedicated I built this channel in our scrimba Discord server and that would be

a great place to put your own design tweak on this post it over there in the ibuilt this Channel and really feel

proud about what you've done so far in this course once you've had a chance to put some flare on this and post something in the Discord server then

come back here to the course and we'll keep moving forward we've spent some time separating

each of the parts of our main app into different components but these components are still kind of cluttering

up our index. jsx file especially as these components were to get larger and larger as we built our site out we would

find this not to be a tenable solution as I'm sure you can imagine fortunately moving these components into their own

files is a really simple task here in the project explore I'm going to create a new file and we'll call it capital H

header. jsx remember because the header component has jsx in it whenever we have

a file that will contain jsx we need to make sure we use the jsx extension so

that vit does a more thorough job when it comes to compiling our code down so like I said this process is going to be

pretty pretty straightforward I'm going to cut the header component out from the index file and go over to my header file

paste it in here now if I save this I'm going to get errors because I'm missing

the header component that I'm trying to render in my index file it's trying to render header but it doesn't know

anything about header so I'm going to place a challenge pause here just to give you a chance to think through what

the steps are that need to happen in order for this to start working again you're welcome to actually do those

steps if you want but it's not necessarily what I'm expecting at this point we'll do that in just a second with the other components I think

there's just two small changes we need to make in order for our page to start working again so take a second to see if

you can figure out what those are well currently our header is kind of

trapped inside of our header file and so I need to make sure that I export this component there's a lot of different

ways to do this one of the most common ways I see is just using export default in front of of your function of course

technically because this is a default export we don't necessarily have to give it a name but I think for debugging

purposes this actually ends up being pretty beneficial for us okay so now we have a way to send our header component

out of the header file let's go over to our index and all we need to do is to import it and because I exported default

I can just say import header I don't have to surround it in curly braces because I'm exporting it as a default

and I will import that from do/ Capital H header if this is your first time

dealing with exports and imports in JavaScript as a really quick highle overview when you default export

something all you have to do is say import and then you can call it whatever you want at this point I could have said

whatever component and then as long as I called it whatever component down here

whatever component it should just work I'll go ahead and hit save and we'll see that we're up and running again

naturally I like to just keep everything consistently named so of course I'm going to rename this to header also as a

quick recap for imports and exports here because I'm beginning this with a do slash that's a way to indicate that I'm

importing this from my own file and not from a thirdparty package that lives in my node modules folder it also has a

default of JS for the extension and in this case it also tends to work with jsx

so I don't have to include that part but I think some teams decide they do want to do that a lot of things just end up

being conventions that you have to learn from whatever project or team you're on it's most important to stick with the

conventions of your project and just to stay consistent okay I renamed that let's hit save we can see that we're up

and running all right it's your turn let me type out a challenge okay not too shocking but your challenge is to move

the main content component and the footer components into their own separate files probably just called Main

content. jsx and footer. jsx and then of course you'll need to do whatever else

needs to happen in order for our app to continue working go ahead and get started on this

challenge all right let's create a couple new files Main content.

jsx and footer. jsx it's probably helpful to note right now I'm just kind

of stuffing everything here at the project route because we don't have that much often times you'll find people

creating a folder that's called components and putting all of their designated component files into that

folder and of course as your project gets larger and larger you'll have to come up with more intense ways to

organize things so that it's not too overwhelming every project tends to be different so don't take what I'm doing

here as gospel and be willing to be flexible as long as you understand the principles it should all be pretty

straightforward okay let's take our main content component and we will put it

into our main content here I'm going to just type out export default and then paste in the rest of the component we'll

go ahead and do the same thing for our footer we'll take that out put it in our footer export default and we need to

remember to import those things so I'll go ahead and do that because I chose the

same names as what we had before I won't need to make any changes there our index file now looks really clean and

everything is still working as always feel free to play around with this code if you want to move things into their

own components folder and change your Imports just to play around with things that would be a great way to get your

hands on the code even more then whenever you're ready let's keep moving

forward when I'm starting out on a new project one thing that I really like to do is try to solidify a mental model of

how I'm going to build a certain app or page at this point in the process I'm not trying to write out exactly what I'm

trying to create I'm simply making sure I understand what needs to show up on the page and how I might go about

creating that this is a great time to tackle any tricky areas of a specific

design that I think I might run into and start thinking about that earlier rather than later so I'm going to Mark a

challenge here I want you to take just a minute or two and see if you can figure out how you would separate each part of

this page what kinds of elements you might use any specific CSS you might decide to use and stuff like that so go

ahead and take a minute to think about that in web development there's always a

lot of different ways to approach a specific problem so the way that I'm thinking about this may not be the same

that you did and that's okay when I see this page I see two main parent components one would be this header

which fortunately doesn't have a whole lot in there for us and then sort of a main content section this one unlike the

practice one that we were doing doesn't have a footer inside the header I might just have a single logo that contains

both the icon and the text a lot of Brands will make sure that their text is actually part of the image to make sure

it's the same for no particular reason we're going to actually use this as a text element so we'll have two elements

we'll have the logo image itself and then some text to me I can just see right now because I will have these in

line I could either use an image and a span both of which are inline elements and I probably won't face too many

issues with that of course if I do run into anything I usually just tend to Resort directly to flexbox and that's a

great way for me to get things all aligned nice and neatly and then I just have maybe an H1 sitting here in the

main content of our page and our unordered list and then of course in the background we have sort of a partial

background image we're going to see how we might tackle that once I've started creating this mental model I can start

thinking of Those portions of the page in terms of actual elements that I want to create often times I will put

everything inside of some sort of container in this case I just have it as a div with a class name of container and

then we have our two main sections our header section and our main section ction so those would be our header

element and our main element in HTML and although we don't really have other navigation elements like we had in our

practice app with the pricing about and contact very typically clicking the logo or the logo text I guess in our case

would send you back to the homage of a website so that would be considered part of the navigation we're not going to

bother with anchor tags in this case but it still would make sense for us to set it up correctly and put it inside of nav

element that's where we'll have an image and a span perhaps and we'll make sure to apply some styles to those then in

our main section as we said we just have a simple H1 and then an unordered list with some list items and everything

should be pretty peachy from there it seems like it's going to be a pretty straightforward project by way of

organization I probably will do a very similar setup as I had before where I might have some sort of app component

which will be in charge of rendering essentially everything and then that app component will render a header component

which will contain the markup in our header section up here and maybe a main or a main content component just like we

had in our practice that renders everything on the main element hopefully that can be a helpful practice for you

feel free to adapt it to whatever makes the most sense for you but I do find that it tends to be one of the best ways

when I'm preparing for a new project to make sure that I get started off on the right foot with this quick mental

outline of the project behind us let's jump into a series of challenges where you will have a chance to build each

piece of this section project let's get the very Bare Bones of

this project set up and as a little gift I'm not going to require you to write any more create root code hopefully

you've had enough repetition now that if you needed to you could do that again so let me walk through the steps and then

I'll hand it over to you to work on this first part of the project first I want you to create a separate app.jsx file it

will be a sibling to this current index. jsx file and you're going to create a new app component it's just going to be

called app this is a really common way to set up a react app where you'll have index. jsx which is involved in setting

up things like the root and doing other more project configuration style things

and then having a separate file like app.jsx which will export a component

called app or something along those lines whose job it is to aggregate all of the other parts of your app that you

want it acts as sort of a parent component to everything that will get displayed on your page after that I want

you to create a separate components folder and you're going to create two different component files inside a navb

bar. jsx and a main. jsx for now in those components all you'll need to do

is render something like an H1 that says like navbar goes here or main component goes here make sure to export those and

inside of the app component that you just created before this you'll import and render the navbar and main

components then inside of this file index. jsx you'll import and render the

app component right here in root. render as a final step and this one might require a little bit of extra research

if you haven't done this before I want you to go over to Google font and get the inter font with the weights of 400

600 and 700 then just add the links to those Google fonts here in the index.html file and make sure to do it

above this link element here so it'll go up here okay that's all the steps for

this challenge it's quite a bit to do but I think you should be able to do it relatively quickly so I'll hand it over to you to work on this

challenge all right let's start by creating some files I'll create a new

app.jsx with a capital A and app and here we will just get set up we'll

export default our app function and you know what let's take it one little step

at a time I'll first render an H1 here that says app component here let's go

over to index. jsx and import it we'll import app from slapp and down here

let's just get it rendered this is kind of a nice intermediate way for us to just make sure that everything is

working correctly okay cool app component here now let's create our components folder and inside components

I'll go ahead and create a navb bar. jsx and a main. jsx and I'll just copy and

paste this is kind of the cheater way but it'll save a little bit of time we'll call this Main and we'll say

that's the main component and we'll do the same thing for navbar okay and then over in app.jsx we

don't want this to be rendering its own markup per se at least not right now but instead we want to import our main

component and that's going to be from SL components because we're inside the

components folder SL Main and we'll import navbar from components SL navbar

and then we will just render the let's see we'll do the Navar first and then

because we have two siblings that we're trying to render we need to wrap them in some kind of parent we'll just use a

fragment at this time and we hit save and awesome looks like that's working great okay then we need to bring in I

think as a final step a little bit separate from everything else some Google fonts we're going to bring in the

inter font with the weights 400 600 and 700 and actually it looks like at the

time of recording this Google fonts has introduced something called variable fonts which allow me to bring in the

font and then set a specific style to change the font kind of however I want with the weights so we'll just go ahead

and bring in the variable font it's totally okay if you didn't do it that way during the challenge but I can just

bring in those links and we're not ready to use these quite yet but I'll go over to index. jsx and just clean up our

challenge text and cool we're in a great starting place in the next part of our section project challenge we will be

working on the navigation bar styling at the

top I wanted to give some fair warning about the next few challenges that we are about to do there will be a few

points throughout this entire course where we're working on our section project and it does kind of turn into

mostly CSS work I'm going to leave it up to you to decide if you want the refresher on CSS or you want the

challenge of working on the CSS of course doing the CSS and styling is likely to be a large part of any

front-end job that you have and so personally I think it's good experience but if you are coming to this course

with quite a bit of experience in CSS and styling in general following a design and getting your project to look

the way it's supposed to look then you have my kind of hesitant permission to skip the CSS portions of the upcoming

lessons that it if you've never tried to mimic a design from a design program like figma or it's been a while since

you've done any CSS then I highly highly recommend that you do complete the CSS portions of these challenges that we're

about to do in this lesson we're just going to be focusing on the navigation bar at the top if you click the

screenshot here that will take you to the figma design where you can see things like the font the sizing the

colors and so forth I'm also going to leave this Google slide in the lower corner if you need to reference the

figma design again in one of the future lessons that we do during this project so let's get started on the navbar your

challenge is to to complete the Navar so that it looks like the design I have a couple hints here for semantic HTML

purposes the Navar should render a header as its top level component and it should have a nav element nested inside

then we can put the image and the text of react facts which in our case will be two separate elements they can both be

rendered inside of the nav as children and semantically it makes sense because typically in a navigation bar your

site's logo in the nav bar on the upper left will also include some kind of an that navigates the user to the homepage

usually and then as a hint I've already mentioned this but make sure you reference the figma design so you can get the most accurate information about

the colors and sizes and so forth all right it's your turn give this Navar Your Best

Shot all right so instead of an H1 let's go ahead and render our header element

inside the header we will add a nav element and our nav is going to have an

image and we'll fill this out in just a second and then the text let's just go ahead and add this as a span we can type

in react facts right now I think we can get rid of the challenge text we kind of

have an idea of what we're doing let's hit save and okay all we see is react facts that's probably what we'd expect

let's fill out the image and then we'll have a bunch of styling to do so first we need to make sure we have a source

and remember image sources here in scrimba might end up being a little bit different than the way that you're doing them locally if you're using for example

a vit project I think it will work if I type in a relative path I'm here inside

of my components folder so I need to make sure to go back a directory and then I have my

react-spring up I'm just going to leave it like this cuz I think this will work a majority of the computers and very

soon we'll be learning about another way we can bring in this logo that will work across whatever platform you're using

okay in our image we want to make sure we always include an ALT text so we'll say this is the react logo and from

there we are just going to have some styling to do I think that's pretty much all that's left for this challenge so I

could go through and add class names to everything more power to you if that's how you decided to do this challenge

it's great to get practice with class name however because I know that this site is just going to have one header

one nav and that nav is only going to have one image and one span inside I'm going to shortcut that a little bit and

just access these elements so this is the point at which we'll mostly be working in CSS and again if you already

feel very very comfortable with CSS it's okay you have my permission to skip this part otherwise please stick around and

watch this process I've chosen to include this because I think it could be a helpful reminder and helpful practice

for a lot of people taking this course so let's move over to our CSS file and this image is driving me a little bit

crazy let's access the image inside of our nav and say that the width is let's

give it 30 pixels and boy 30 just looks a little bit small I think the design says 30 but I don't know I think I like

40 a little better we might even bump that up a little more later okay so by default react fax is not aligned to the

center vertical aligning like this I personally believe is best done with flex box so I'm going to access the

parent and make it a flex container so that that's the nav element let me just

make sure and yeah so our nav will be the flex parent or the flex container and the image and the span will become

the flex items inside of it so this will be display flex and then we can align

the items to the center and perfect that looks pretty good if I look at the design the entire header shows that it

is about 90 pixels so I'm going to style the header and give it a height of 90

pixels and I think that makes it so the nav is not taking up all that space you know what before we do anything else I'm

going to give it a background color and just bring in the say the background

color from the design on figma which is this color and yeah we can see that that's not the correct height so now

that the header has a height let's just make sure that the nav has a height of 100% so that it fills the entire parent

container and cool now that's centered it's pushed pretty close up there to the left and that's because I had added this

margin of zero to the body I kind of need that cuz if I don't then we can see we get that Gap around our header so

let's leave this at zero but then we can just add some padding inside of honestly

I don't think it would matter if it's the header or the nav let's go ahead and put it inside the header and let's give

it maybe 30 pixels on the top and bottom and 25 pixels on the left and right I

think that looks pretty good okay now I think the biggest eyesore is the text of act fact which is barely visible right

now let's separate it from the image by about the seven pixels that the design

shows so we'll give the image itself a margin right of seven pixels I guess we could also give the span a margin left

of seven pixels I don't think it would matter too much either way and let's go ahead and select that text so this is

going to be the nav with the child of a span and again I just as easily could have gone here and given class names to

everything maybe just so I'm covering my bases just as a reminder we don't say class equals but we say class name with

a capital N equals and then everything else is exactly the same as you're used to with regular classes in this case I

am going to take the shortcut okay the color is driving me crazy let's switch it to the blue color from the design and

let's bump up the font size a bit and the design does say that it's

22.25 pixels if we take that and divide it by 16 we can get the REM size which

is a better practice to use for our font size anyway I'm going to round a little bit and say that it's about 1.3 REM and

actually I think it more closely rounds to 1.4 so let's just bump that up again okay that's looking pretty good the font

is not quite right though and that's where our inter font comes into play I'm just going to style the entire body to

have that so we'll say the font family is going to be enter let me make sure

that is yeah that's working okay great and maybe we'll just give a Sans serif back up for that if we look at the

design that react fax text has a font weight of

700 and that is looking pretty darn good all right that's really taking shape

great job working on this challenge next we'll naturally be styling the main content

section all right I'm going to have the same caveat for this lesson we are mostly doing CSS in this challenge so do

with that what you will if you could use practice in CSS then we would love to have you do this challenge either way I

do want you to at least add all of the markup that needs to happen here so let's take a look at the challenge

itself just like the navbar challenge we're going to be building out the main content section so that it matches what

we see in the figma design there are two aspects of the figma design that I want you to skip for now because we'll be

doing those as separate challenges one is having the bullets on the side be a different color and I believe a

different size and the second is this side react logo over here don't worry about those two aspects but do worry

about everything else that you see and try to match the design as closely as possible go ahead and get started on

this challenge okay let's do the markup here

I'm going to surround everything in a main element since that's semantically correct for the main content on our page

and we will have the fun facts about react be in H1 here so I'll go ahead and

type that in and then simply enough we have an unordered list this should feel pretty familiar cuz our challenges

earlier on in the course were essentially doing this exact same thing and with that we'll just have five list

items and I'll go ahead on a Mac and hit option shift down and that will let me copy this line and I won't make you sit

and watch me type out all of the text here so I'll go ahead and copy and paste that in all right let's hit save and

awesome that's a great start let me make this a little bit bigger so we have a little more space to see these items and

we are just going to jump over to this CSS now and get started working on that first let's get the background and the

text in the right color I think I'm just going to set a background color on the

body If instead I were to style the main element which I'm sure we could make work but we'll see let me comment this

one out and put it here on Main yeah we'll see that we have actually a couple issues that are highlighted here first

of all we get some collapsing margin happening with our H1 the default margin on the top of the H1 one is actually

pushing our entire main section down and so we get that white stripe there and secondly we're not taking up the full

height of our page we might address that in just a minute but I think it makes a ton of sense to put the background color

just on the body so we don't have to worry about that so that's what we'll do for now I am currently pushed all the

way up to the left here because the body has a margin of zero and again I don't want to add margin to the body because

that's going to kind of mess up our header up there so that's a perfect thing for us to do on the main element

we'll go ahead and give this some padding and it looks like it's about 60 pixels on the top and about 30 pixels on

the left we'll just let that go top and bottom and left and right and that's looking pretty far down I do think

that's because of that H1 margin so I'll go ahead and select the H1 inside of my main and set the margin to zero and yeah

that looks a lot closer because I set a dark background on the body I think I also am going to use the body selector

to select the color and just change it to White that way if I did create a footer or something and wanted that text

to also be white because it's a dark background then I wouldn't have to repeat that style but I don't know we're

venturing into Realms where it really doesn't matter how you do it at that point all right let's set the font size

here while we're at it and the design currently shows that it's 39 pixels that

translates to about 2.4 Rim so that's what we'll set that at let me make this a little wider again okay let's start

working on our list the lines look like they're pretty tight together and the design shows that there's about 20

pixels of space between them at this point I suppose I could say Main and then child selector of unordered list

but at this point because I might have multiple unordered lists I'm just going to kind of do my own personal best

practice and in my main section I'll go ahead and give this a class name and

let's say it's the facts list okay then over in R CSS I can just select dot fact

list and it looks like it's about 46 pixels pushed away from the header so

let's give this a margin top of 46 pixels make this a little taller here

and I think actually if I make this wider we can see this one starts to get a little bit wide in this case it's not

so bad but if we were to add more facts for example that had a lot more words we would end up with a full width list item

there and so maybe what I'll do is give this a Max width and let's just say

something like 400 pixels that way when this gets really wide we are still limiting ourselves to the width of this

list I don't know that's a design decision that might not make a big difference right now okay let's add some

space above and below each of the list items I'll just go ahead and select the facts list and get all the list items

inside of there and I can add a margin to both the top and the Bottom by using

margin block so that will will allow me to say 10 pixels on the top and 10 pixels on the bottom of each item and

that gives us a little bit of extra space there that's nice and in the design if we look really closely each of

these also has a line height set and it says 19 pixels let's see if that really makes much of a difference and boy

there's barely any difference there but it does make a little bit of a difference especially when it starts to wrap so we'll just leave it in there and

one other thing I actually just realized is my items are not spaced as much as I thought they would be the design shows

them as 20 pixels apart but I just realized that when I'm doing margin block the bottom margin for one item and

the top margin for the other are collapsing together into a single 10 pixel margin so I can either set this to

margin block of 20 pixels and that actually looks a little bit more correctly spaced or I think I can do

padding block of 10 pixels and padding does not collapse in the same way I

think I'm going to leave it just here at padding block so I don't have to worry about thinking about collaps margins in the future but either way should work

just fine and okay this is in a pretty good place the only other two things we have on this project like I mentioned is

to color the bullets here and then to add the little react logo on the right

those do have a little bit of a gotcha to them so we're just going to do them separately in their own challenges I'll

remove this challenge text and we will go ahead and start tackling those challenges

next I was going to have coloring the bullets so that they were a little bit larger and blue be a challenge that I

gave you and of course if you want to try and do it on your own you're more than welcome to do that a really common

way to customize bullets like this are to completely remove the bullets from the unordered list and then to use a

before pseudo element and create your own little CSS shape that is in the

shape of a bullet but at that point it felt a little too I guess nitty-gritty to be really diving into doing that with

CSS in the middle of the react course I know I said it's good to practice CSS but I think that might have been a

little bit Overkill instead we're going to stray just a tiny bit from the design and we're going to use a special pseudo

selector called marker so I can grab my list items here and I can use colon

colon marker and this is a pseudo selector that's very specifically

intended to add styles to your bullet points in list items I can grab the

color of let's see our span right here and actually I can just grab this whole style I think let's go ahead and set the

color and just like that our bullets are now the same blue color as react facts I

am allowed to style any font properties like font size and I did find that 1.5

RS is about as large as I can go before these start getting misaligned we can see if I were to make this something

really large like four rims that the alignment ends up being a little bit messed up and I tried for quite a while

to get these two align and couldn't really do that if you know of a good way to do this then please reach out to me

on the scrimba Discord server I would love to know how you did it but that said don't waste a bunch of time on it

I'm just going to set it to 1.5 where they look like they're still pretty well aligned and we'll just leave it at that

it does stray a little bit from the design cuz I think these bullets are a little bit bigger than what we see there they're probably more like two Rim but I

just couldn't deal with the misalignment it was bugging me just a little too much okay you get that one for free didn't

make you do any work there the last little design thing we'll add is the logo over here and that will pretty much

wrap up the react fa section project for us we just have one more tiny thing that

we're going to add and that is the react logo that's floating here in the background because this isn't an element

that is really a semantically important part of our markup I'm just going to have you add it as a background image

instead of trying to add it as an image element for example I don't need a screen reader to read that there's an

image element here or have it be accessible via the keyboard or anything like that so I think it's okay for it to

just be a background image on the main element the challenges that we've done up until now at least had a little bit

of markup that you had to write react code or jsx code for this one is going

to be purely CSS so I do give you permission if you feel completely solid with your CSS skills I give you

permission to skip this one that said I think CSS can be fun so even if you are you're welcome to stick around and do

this challenge I've given some hints about how you should use the background image with the URL and one thing I did

add is the react logo half.png file here it is only the actual half of the logo

like it looks like here it's not just bleeding off the side of the page that just has more to do with how I exported

it from figma but honestly it makes the job a little bit easier to match the design that we see here one thing I'm

going to do really quick just because it's bugging me is I'm going to create an images folder and I'm going to move

my logos in to that images folder and that means I need to come over to my navbar and just fix my reference here

we're going to start with Slash images hitting save and okay everything is working great read the challenge text

here and I'll pass it on to you to start working on the

challenge okay on our main element I'm going to add a background image and

we'll set that to a URL I think in CSS I don't have to have my quotation marks so

I'm just going to say slimes SL react logo

half.png awesome there we go by default it is repeating so I'm going to add the

background repeat property and just set that to the value of no repeat okay and

that's making it float by default in the upper left so that's where the background position comes from and

background position is actually a combination of two different properties so there's background position X X and

background position Y in fact let's just use those to start and then we'll make it short so X would be the left and

right or the horizontal positioning and one option I have here is to put it all the way to the right that looks pretty

good that's halfway there and then I would add background position Y and

right doesn't make sense there because we're talking about up and down so I could say top which I think is the

default in this case I could say bottom that pushes it a little bit too far to the bottom I can say Center and that

puts it directly in the center although it looks a little bit High compared to the design the design looks like it's

not exactly in the center so what I can do is provide a percentage of where it

should sit in that direction so I think if I were to put it at something like 65% that seems about right so maybe

we'll just stick with 65% now I can combine these though and make these a little bit more straightforward so we'll

say background position right space 65% and then I can get rid of my specific

background position X and Y properties and now I'm just being pigy but I think this might be just a hair lower we'll go

ahead and say yeah let's to get at 70% keep in mind we're not really doing any

mobile first or desktop first designs if I start to make this really large then things I don't know they don't look

great they're breaking down a little bit but for now this is going to work okay for us again CSS isn't really the point

of this course again if you feel pretty comfortable with the background shorthand property then you actually can

combine these three together and just say background is this value space this value space this value myself I always

forget what order these need to be in so I either have to look it up or I just choose to do this three separate

properties like we have here okay let me clean up the challenge text here and let's just navigate over to our index

page so we can actually be looking at some react code again hopefully for some of you that was helpful to spend some

time on the CSS we will be going back forth to CSS a little bit as the course progresses but I'm excited as I'm sure

you are to get back to learning more about react we've just barely started scratching the surface of what react is

capable of doing now we have a few administrative details to help set us up for Success through this course and then

we'll be doing a recap of the actual react things that we've learned so far so buckle up we're just getting started

and it gets more and more exciting from here hey yo you did it you built your

first react project I know it might not seem like much but it's really exciting these first few steps of building a

static page are really crucial in your journey to learning react as a quick recap the things that we've learned we

talked about why we should even care about react in the first place we talked about how the composability Paradigm

that it introduces is super helpful in how you can structure your applications going forward and how its declarative

nature just really improves the developer experience we practiced time and time again probably too many times

in your eyes how to set up a new react project but we also talked about how you can set things up locally on your own

machine using V scrimba is a great environment to play around with your code and to learn very interactively

like we're doing here but eventually you'll be wanting to build your own projects on your local machine so we made sure to cover that we talked about

jsx and how it's a so-called syntactic sugar on top of react. create element

and how in the end all it's doing is returning JavaScript objects those objects then describe what react should

be placing on the page and it gives us react developers a really nice familiar

syntax that we can use to describe what should end up in our web app we built our own custom components which is the

Crux of having composability in react and truth be told we have yet only scratched the surface of the ways in

which building custom components gives you the flexibility that composition gives and just so we're not left with

something terrible to look at we talked about styling and spent a fair amount of time actually building the styles for

our app if you haven't yet done so this would be an ideal time to head over to the scrimba Discord community and post a

message about the accomplishment of finishing section one of the react course you can click on the screenshot

you see here for an invite to the Discord community and a link directly to the today I did Channel this might be a

good time to take a quick break from learning react if you have found yourself binging this course it's

important for your brain to rest and relax so that it can actually digest the information you've already consumed and

make some space for what is to come and we do have some really exciting things to come so once you're ready let's go

ahead and jump into the next

section with the basic concepts and syntax of building static pages in react under our belt we are now poised to

progress forward and start learning about how we can write datadriven react apps you see in our previous project

everything that was displaying on the page we had hardcoded directly into our markup and there certainly is still a

place for hard-coded text on a page anything that is considered static or unchanging is going to be written

directly into the code however we are soon going to learn about how the power of react comes not only from its

composability and declarative nature but from its ability to receive information

in the form of data and use that to produce reusable components on the page the project we'll be building in

this section is going to be a travel journal and the primary thing that will make it different from the static page

that we made in the previous section is that all of the information that we see on the page is actually going to be

contained in a regular Javascript file in the form of regular objects and

arrays this is the completed project over here and you can see that we have this data.js file where all of the

information lives and then the react code that we write will take this array iterate over it and produce react Cod

components with that information inserted in the correct Place feel free to peruse around this

code to see if you can get a cursory level understanding of what's going on and as always you can click on the

screenshot you see here to take you to the figma design so you can be prepared to start building this project based on

the real colors and spacing that are defined in the figma file in this section we are going to be

learning first of course why reusability is important and we'll recognize that it's actually something that you are

exposed to in just about every website you visit then we'll dive into the Syntax

for the primary vehicle for doing reusability and datadriven react components which is something called

props then with an understanding of how props works we will create components

from an array of data just like we were talking about earlier and of course this wouldn't be a

real scrimba course if we didn't include a ton of Hands-On challenges along the way so warm up those fingers get ready

to complete all of the challenges in this section which is what we'll be diving into right

away we'll start working on this section project of the travel Journal by having kind of a softball challenge this will

mostly be review of the things that we've learned previously our task is simply to make this header section for

the travel journal the first thing you should do is click on the screenshot here that's going to open this design in

figma so you can see the details for this design and I've tried to set you up for success with this project by

including a fairly detailed description of the task at hand a couple things that I have done already for you if we look

in our index.html I've pulled in the Google font of inter which is the font that you'll see is used here in the

design and then I've also pulled in this little Globe image just right here as globe.png and so you'll be able to use

that as your image source feel free to style this however you want you can use class names or because this is a

relatively small app I'm okay if you want to use some element selectors assuming you're using some good semantic

HTML for the app if it's been a minute since you finished section one this will be a great way to brush off the rest so

I'll hand it over to you to work on this challenge all right so let's create an

app component in a separate file so I'll just create a new file called

app.jsx and before I jump back and forth I'll go ahead and import it even though it's not really exporting yet we'll get

that in just a second so we'll import app from the app file and then I'll just go ahead and render my app right here

all right I think I'll probably error if I hit save so I'm not going to do that quite yet we'll go over to

app.jsx and I will export default my function app and just as a sanity check

just to make sure things are working I like to just render something like an H1 that says I'm the app component okay

let's hit save okay good no mistake so far we're importing the app and rendering it correctly let's go check

out our challenge text okay so that's this first part done next we need to

create a components folder and a header component which I guess I wasn't explicit about that being inside the

components folder but hopefully you figured that out it's not a big deal if you didn't something probably important

to point out is that our app is going to end up being really small there's not a whole lot to this page as you can see

and so creating a separate components folder is maybe a little bit of Overkill or maybe you like doing it file

organization really does end up being pretty subjective and so just make sure you're following the conventions of

whatever project you're in or if it's your own project you can make up whatever conventions you want just to

see it done a little bit differently than we have been I'm going to create this components folder and inside I'll

create a header. jsx file and let's see what did the challenge tell us to do create a components folder header

component render the header inside the app component okay that was a little bit vague but that's what I was trying to do

so we'll export default function header and we'll have it also

just return an H1 for now I'm the header component we're exporting it here now

let's go over to app and inside our app we're going to import header from and

now our path has to start with/ components SL Capital H header okay instead of our H1

let's go ahead and render our header and I'm the header component Perfect all

right let's see what else we have that is done now let's go back to our header

and instead of returning in H1 I'm going to return a semantic HTML header element

inside the header I'll go ahead and put my image this is the little Globe image

so my source is going to be now let's see I'm inside my header which is inside

the components folder and I need to be outside the components folder so I need to go do/ globe.png and then we'll go

ahead and I guess we can call our text for the my travel Journal we'll just

call that an H1 and we'll say that's my travel Journal let's hit save and the

globe is impossible to see because it's white on a white background let's see if we give the header a background of red

okay awesome there's our globe and we have our text let's go back to our Challenge and I guess we can mark the

second one off and the third one is basically all design at this point we've done all of the react specific stuff

we're going to do with this challenge if you already feel really comfortable with your CSS skills then I do give you

permission to skip the rest of this as we're just going to be doing CSS however even if a little bit you want to get

some extra practice with CSS or watch how somebody else writes their CSS then please by by all means stick around

we'll get through this pretty quickly because my page is so small and I only have one header I'm going to select the

elements from the header just directly so we have our header and instead of a background of red if I go and look over

at the design I can see that the color is actually this color and let's go

ahead and get the layout correct I'm going to use display of flex just to get everything lined up and it's pretty huge

right now but I'll go ahead and justify content to the center the text is

actually white so we'll change the color to white I can see from the design that the height is 55 pixels oh okay and we

need to also align our items to the center and I think that should be everything for this section itself now

let's go ahead and style the image so I'll select the image that's inside the header again if you were to ever

consider putting more than one image in here you might want to give this some kind of class name like I don't know

globe or something I trust that you understand the concept of class name in react and selecting with classes in

general in CSS so I'm just going to keep it simple for now it looks like the width of this little Globe is 24 pixels

and if I look closely it has a margin right of s pixels and then let's go ahead and

select my H1 we'll change the font size back down to one RM and actually the

design shows that it's a little bit smaller than 16 pixels so maybe I'll I

don't know just kind of estimate at this point 0.9 R we'll say I think the font weight is a little bit lower so we'll go

ahead and say the font weight is 500 and that looks a little more accurate to the design and the font family is different

too the font family is enter and let's see is that making a difference yes it is perfect one last

thing that I just realized we didn't do we always always always have to put our alt text on our images so I'll say maybe

Globe icon okay let's go see and yep we were able to do that one and so let's go

ahead and check that off and I guess now that we've done that and scratched that itch let's go ahead and clean up this

challenge text and awesome great work everything we've done so far should represent things that you have already

learned by this point in the course if maybe you're picking up this course again after a little bit of a break and

some of this feels unfamiliar this is the best time to go back and review what you might be a little bit Rusty on and I

say that because we're now ready to move forward on our section project and start learning about how we can make the rest

of this page here once you feel good and ready let's keep moving

forward let's Jump Right In and start building an instance of our journal entry component the main purpose of this

exercise is to highlight the fact that we're not quite ready to finish off the app as we currently have it at least not

in a reasonable way that starts to use the potential of react so your challenge is to build out the entry component and

there's a couple things that I've done for you since we last saw this code first of all I created the entry. jsx

file already for you so you don't have to worry about that I also pulled in the little marker icon that's just sitting

right here next to the country name or the location name and that's just right here inside of a new images folder that

I created and it's called marker.png I also pulled the globe.png in there just because that made sense and fixed the

reference to it in the header now since your task is going to be creating an instance of this component and filling

out the data it will require you to hardcode that data for now and in an effort to try and make that a little bit

less tedious I've included this japan. MD file we're going to delete this pretty soon but this just has the text

here so you can copy and paste it at least without having to go back and forth between the design so much all

right let's go back to our challenge text some notes I included I only want you to render one instance of this entry

component and I guess I wasn't explicit about this but you will want to render that inside of the app just right

underneath header you might already recognize that's going to include its own little challenge but I'm not going

to say anything more about that as I've mentioned I pulled in marker.png so make sure you use that and then a reminder

that the main purpose of this challenge is to show you where some of our limitations in our understanding of react currently are so don't worry about

the fact that you're hard coding all of this data into the component some of you may not have been worried about that in the first place okay I think I've set

you up with everything you need so I'll pass it over to you to work on this challenge okay let's go ahead and we're

going to export default a new function called entry this is called entry

because it's like a journal entry in our travel journal and when I look at the design I see everything in this entry as

a surrounding div or I think if I were to be a bit more semantically correct

this might work out as an HTML article element planning out the CSS ahead I might put this as two separate elements

and use a flex box going this way and then the elements that are in here might end up just naturally flowing top to

bottom if they're all block elements although this view on Google Maps I might have to do a little bit something with that and that's okay we'll figure

it out as we go so I want to from each of my entries we'll go ahead and return a parent article element and you know

what I'm going to build out the structure first and then I'll come back and do some styling which means it's going to look pretty terrible for a

little bit let's just throw everything on the page so I have my main image and I just realized I didn't put the URL to

the image in my japan. MD so hopefully that didn't cause too many issues with anybody but the URL is very clearly

listed in the design and you should have been over in the design anyway so we'll go ahead and give it this URL there and

we always need to include our alt let's go ahead and say Mount food

okay kind of reading this left to right we next would run into our little image of the marker there and then the

location name and the view on Google Maps link so I'm going to surround all

three of these items in its own div just so I can give it some flexbox styling we'll go ahead and create a div and

we'll fill out those images so we have an image source of we're inside of our

components folder so I need to go out and then into images and then to marker.png we'll include our alt that

says a marker icon maybe call it a map marker icon all right the next thing we

had the name of the country that we were visiting and I don't know for now I think I'm just going to use a span

because that's also an inline element let's just go ahead and do that we'll say this was Japan and then we had a

link so that's my anchor and I'll need an href that goes to the link for Google

Maps go ahead and just grab this and we'll put that in there oh and this is not self-closing we need some text on

it so we'll say view on Google Maps now I'm Flying Blind a little bit here

because I haven't created an instance of my entry component let's go ahead and hit save no errors that's always good

let's go over to our app.js and let's import our entry I'll just copy this one

all right so here is where there's kind of a little gotcha if you remember we can't put two sibling components side by

side side like this now I don't think I have a reason yet to wrap everything if

I need to add some Styles I might have to change this to a container div of some sort but because I don't want to

add a bunch of extra stuff to it I'm just going to use these fragments and that solves that problem there let's go

ahead and hit save and my image is ginormous let's go ahead and start styling that part up so over in my entry

I'm going to buy myself a little bit of room by cleaning up this challenge text I'm going to start off by making my

article into a flex container I think that will be an okay way to do it this

is coding we might change things along the way oh and I do want to give my article a class name and let's call it

uh let's say it's a journal entry just so it's really clear what we're doing here okay let's go to our CSS and create

a journal entry sometimes i' like to put the name of the element here just so

that it's really clear what we're doing I think it makes it a little bit easier to find and let's give it a display of

flex okay so I should be able to scroll over to the right and see that and now let's go ahead and style up this image

it's not the only image and I don't really want to just select the direct children so let's go ahead and give this

a class name as well and we'll say this is I don't know maybe this is the main

image yeah that's good enough all right back to our CSS let's style our main

image and in the design we can see that the width is set to 125 pixels ah and I

bet this was a little bit tricky because the URLs that we're using they have a different aspect ratio than what our

design shows our design shows a portrait where it's taller than it is wide and the actual image itself is wider than it

is tall the fix for this is for me to use the object fit CSS rule but it does

mean that I need a container for it so over here I'll go ahead and and just create a little

container and I can surround my image in that container will give this a class

name of let's go main image container

okay now that I've done that in my CSS we can select our main image container

give it the height and width that we want so this is actually what we want here and we can specify the height which

in the design show 168 pixels very specific and we need an

overflow of hidden then we can tell the image we want it to have a height of

100% the container a width of 100% the container and object fit of let's use

cover and actually that's looking pretty good we do need rounded Corners though so let's give this a border radius of 5

pixels just a little subtle rounded corner there we'll worry about our our spacing in a little bit I'm going to

make this a little bit wider for us okay making good progress so far let's deal with getting the rest of the content on

the page and then we'll do some final touches or I might just do the final touches for you let's go ahead and call

each one of these an H2 that seems logical so in our entry let's see where

are we we have this div H2S our Block Level so that should put it onto the

next line for us and oh well let's see that needs to be inside this div if we

want it to do that okay and let's see this says Mount Fuji let's just see where it is oh okay that's better than I

thought it would be it's a good start then we'll give another block element I guess we could call the date an

H3 well no it doesn't feel like a header let's go ahead and just call it a paragraph and we'll style it up to be a

little more bold let's go grab our dates and we'll do another paragraph

here all right let's see how we did oh well because we're using a display of

flex our item here trunk in order to fit all of the long text here we can

counteract that by in our CSS let's see in our image container we need to say Flex shrink of zero and at this point

I'm just going to use the magic of editing and just like that with the snap of a finger all of the design for our

entry component is done if only it were that easy in real life right I think I'll probably increase the size this

just a little bit so we can see all of our text and awesome it might not be 100% perfect but that's okay it's good

enough for us to move on hopefully as you were doing this exercise you could see that there's a pretty significant

limitation to the way that we're hardcoding all of the data here in our entry component as it stands if we

wanted to create a second entry we would likely have to create another entry component and that doesn't really make

sense when it comes to using reusable components because well obviously we're not taking advantage of the reusability

aspect of a component in react feel free to look at some of the changes that I made in the markup or the CSS although

they're not crucial to your understanding of react it can sometimes be overwhelming to be tossed into a big

change like what we just saw with the design then once you're ready let's move forward and start talking about how we can make this entry component more

reusable as we've already discussed the way that we have our entry components setup is not reusable at all if we were

to go to our app.jsx and create another instance of our entry component we're

constrained to having another trip to Mount Fuji and that's because the way that we set it up is by hardcoding all

of the information directly here into the component so obviously this isn't going to be our ultimate solution

because we want our travel journal to have more than one destination in it the idea of reusable components can be found

all over the internet if you go to amazon.com for example you can see we have this list of new releases in cell

phones and accessories and although the information in each one of these products is different the structure of

it appears to be exactly the same we have a little badge icon an image a product name a rating and a price and

you will see this all over the web let's take IMDb for example when it comes time for a new movie to be entered as a fan

favorite you can imagine there isn't a developer who's jumping in and typing the HTM code down furiously to try and

get this new movie entered into the fan favorites list instead what's displayed here is data driven which means all

someone has to do at IMDb is add a new movie to the database and the site will automatically update to display the

repeated elements of that new movie here in this list which consist of a cover image a rating a title and so forth and

as you can imagine react has a solution for structuring our code in a way that is more similar to this where it can be

data driven we're going to talk about the datadriven aspect of react a little bit later but for now we can see that

our component is so hardcoded that there's no meaningful way for us to have it represent different kinds of data and

in react this is where the concept of props comes into play in my years of teaching react I have found that props

tends to be one of the first hurdles for people that are just getting into learning react and so my plan is to take

the topic of props and to spread it out a little bit thin we'll take one little step at a time and in typical scrimba

fashion you'll get your hands on the keyboard and I think by the end you'll have a really solid understanding of how props works and react so without further

Ado let's jump in and start learning one of the most impactful and exciting aspects of

react let's start by understanding the basic concept of props and react what

you see here is just a plain index.html file we haven't introduced anything

dealing with react in this I want you to take a close look at the elements that you see here and see if you can figure

out what's wrong with them let's start with the anchor tag an

a tag an anchor tag is intended to link you to another place but currently we

don't have an attribute like the href specified without an href this link is

essentially useless we need the href property in order for us to send someone to another page maybe like google.com

similarly the image element is basically useless without any kind of Source property we need to add this Source

attribute or property in order to specify exactly what image will be here we could put the path to a local file or

we could put the address of a file that's hosted somewhere on the internet input is interesting because I think on

its own it actually will yeah it actually will put an input

box that we could type into if we wanted to however there are attributes or properties that we can add to the input

that will make it a lot more let's say beefed up or capable for example I can

add a placeholder that says something like first name and that suddenly makes the first name text appear inside of my

element on the page or there's ones that have even more consequence to them like the type property if I change the type

of this input to something totally different like submit now it changes from an input text box to a button

similarly it could change it to radio and it completely changes the visual look of this input these are Concepts

that I'm sure you're already very familiar with let's look at a similar parallel example in JavaScript here I've

written a function that's called add two numbers together and it just hard returns one and two think for a second

what is wrong with this function it's syntactically correct but what's wrong with a function like

this well it's very very limited in its capabilities right now if I call add two

numbers together it will always return three essentially it's a useless function now you might already see where

I'm going with this if I add some parameters like let's say A and B to this function now I can dynamically add

and return the result or rather the sum of the two numbers that I pass in and

with the small addition of these two parameters that I've added I now have sort of beefed up this function in a way

that it's capable of adding whatever two numbers I want not just the hardcoded one and two that used to be there again

these Concepts should be familiar to you by now but this is just a primer for us to understand the concept of props in

react in both of these instances in JavaScript and HTML we can see that

passing additional information to our maybe elements or in this case functions

allows us to reuse these elements or functions in multiple different ways so

with that primer under our belts let's look at another conceptual parallel that is a little more

visual let's take a second to understand props in a little bit more of a visual way here we have a screenshot albeit

kind of an older screenshot from YouTube and as we look around the site and honestly as you look around pretty much

any web app you're going to find this repeated nature of different components on the page for example here in this top

playlist we have a number of different videos Each of which has a very similar structure we have an image on the top

half in some bold text right below that we have the title of the video and there's other aspects too like the

viewership count each video also has a little Tim stamp in the lower right and the other visual aspects that you see

here obviously you can imagine that whenever a new video gets uploaded to YouTube there isn't a developer that's

going in and manually recreating any of this content but instead the data of that new video like the cover image the

title the number of views and so forth is being stored in a database and this flexible reusable component is able to

receive the information about that specific video in order to display it as a unique video on YouTube and as you

become more familiar with this concept you'll start to see how these reusable components can be nested together for

example not only do we have individual I don't know let's call them video tile components but we have repeated lists of

those video tile components which maybe we would call it something like a video tile list or a video list component

inside of those video list components are a nested list of video tile components and kind of as we saw on the

Apple website there's this section over here on the left which albeit pretty small is probably a repeated component

each one of these just has an icon and a title okay I think I've beat this concept into the ground I think you're

probably starting to understand it now let's go back to some react code and see how we can actually implement this in

the code there's one more quick thing we need to

cover before we can start using props in react which is the way that we will be able to make our components more

reusable we've learned about jsx and how this syntax that looks very much like

HTML is able to be interpreted as a way to create new elements on the page and

whatever we put in between our opening tag and our closing tag just like in HTML is what will actually get rendered

as in this case text or in some cases other nested elements on our website

however one of the most common things you'll find yourself doing is having some sort of variable or value that you

need to have displaying on your page for example let's say in the process of creating our component we came up with a

first name which let's set it equal to Joe and a last name which will set to

Schmo and instead of saying hello world we wanted to say hello Joe Schmo when

you're first learning react it might be tempting to try and just stick first name in here and then a space and then

last name or maybe as we're used to doing it in vanilla JavaScript we might

do some string concatenation so we might try to say first name plus a blank space

and then plus the last name now I'm not going to hit save yet but I want you to think about what it is that will happen

when I refresh this page some of you probably figured out that it's just going to literally display the text that

I put between my opening and closing H1 element fortunately react has made it really easy for us to interpret

JavaScript values in the middle of our jsx as opposed to literally displaying this text as if it were what I wanted

displaying on the screen and the way I can do that is by simply surrounding any JavaScript values with a single set of

curly braces so we'll see I'll be able to hit save and now Joe is correctly coming through so that brings us to the

first challenge that I'm going to give you simply enough your challenge is to finish off this H1 below so that it says

says hello joeo there shouldn't be any of these characters or the variable name last name or anything like that go ahead

and work on this challenge all right simply enough all we need to do is get rid of those

characters and then surround last name in a set of curly braces now let's talk for a second about what's going on with

this line when react is being transpiled or compiled to regular JavaScript this

less than symbol followed by the name of the element followed by the greater than symbol it's able to interpret that as

the beginning of being in jsx I kind of like to think of it as entering into jsx

land let's call it once we're in jsx land the code that we have that follows will be interpreted literally on the

screen like we see with this word hello however once we run into this opening curly brace react says okay we're no

longer in jsx what follows should be interpreted as regular JavaScript and thus we enter what you I guess could

call JavaScript land and here in JavaScript land we have this variable first name which has been declared

earlier just like we would in normal JavaScript and so it gets interpreted or rather the actual value that first name

represents gets put into the place of this curly brace variable expression

that we see here then with the closing curly brace we're now back in jsx land and we have a literal space here that

gets interpreted as a space I guess I should probably hit save so we see that this is working so there's our space

right there in the code or on the display and then with the opening curly brace we enter back into JavaScript land

and we get a JavaScript expression in this case a variable that's set to the string Schmo and the transpiler will

take everything here replace it with what its value actually is and that's what gets displayed on the screen let's

clean up this challenge text and at this point it's important for our understanding to realize that the

JavaScript that we put in here as long as some value is getting returned from that JavaScript we can run whatever

JavaScript code we want inside of the curly braces that we put even though we're inside of jsx for example let's

say we wanted to instead of saying hello Joo let's go ahead and clean some of this up what if we wanted to have it say

it is currently and then whatever time it currently is well because I can run

whatever JavaScript I want inside of a set of curly braces again as long as a value is being returned from that

expression I can run code like okay let's create a new date and then I'm going to call get hours on that date and

then well let's just see what this shows up as okay it is currently 15 if you're

from a place that uses 24-hour clock that certainly makes sense we also might do a modulo 12 if we want to have that

display in 12-hour time and there it goes it says it is currently 3: maybe we say it is currently about 3: and that

makes sense because for me right now it is 3:23 p.m. now I would say with great power comes great responsibility and

having a a bunch of logic stuffed into the middle of our jsx here is it my personal favorite and so my personal

preference would still be to put my logic happening up here let's say maybe const hours equals and then we'll paste

in that expression and then simply enough I would just say hours goes here and we get the same result and we can

take this as far down this Rabbit Hole as we want for example let's say we wanted it to display either good morning

good afternoon good evening or good night depending on what time of day it was all

we'd have to do is simply write out our Logic for determining what this particular word should be and again I

would prefer myself to do this up here before the return in our component and then we would simply display the text

that resulted from our calculations right here in the code because this is more of a simple algorithmic challenge

I'm just going to write out my solution and then I'll give you a really simple challenge for displaying the correct text down here inside of our H1

okay I just hit refresh so we can see our hardcoded good night right here and I've written out the following logic

it's pretty straightforward I got rid of the modulo 12 so we could go all the way up to I think it ends at 23 hours I

created this let variable called time of day and then all I did after that was create some conditionals that said if

it's before 12:00 then we'll say this time of day text is morning if it's between 12: and 5:00 p.m. then it's

afternoon if it's before 900 p.m. then we'll say it's evening and otherwise we'll say it's night I don't know maybe

these aren't the perfect hours but now it's your turn we'll have a really simple challenge simply enough your

challenge is to change this hard-coded word night to display the text that we determined from the logic above go ahead

and work on this challenge all right all we have to do is get our time of day variable we'll put

it in right here and then of course if we were just to hit refresh now it would say good time of day and that's not

exactly what we want if we however surround it in curly braces now this will be interpreted as the JavaScript

value of time of day which was determined up here in our logic and we get good afternoon because again it's

about 3:00 my time and we can see that this is working if right now it's about

15 for me so if I were to change this this wouldn't make any sense but let's go ahead and say between the hours of

12: and 2 it's considered afternoon I'll go ahead and hit save and sure enough even though it's 3:30 my time we're

getting a good evening let's go ahead and change that back cuz that's pretty weird okay now that we've gone through

how to put Javascript inside of our jsx we are primed to look more into the actual syntax of props and see how we

can make the components that we're creating more reusable in order for us to learn the

syntax of using props and react we're going to use this little contact book that I made as an example as you can see

everything right now is just hardcoded here inside of app so we have these article elements these articles

represent each one of these contact cards and just like we saw before everything is hardcoded which again for

a tiny app like this might be okay but if you had any dreams to scale this to a

bigger amount than just having four different contacts in your contact book then this clearly won't be the way to go

so to familiarize ourselves with the code I'm going to give you a fairly straightforward Challenge and then over

the course of the next two scrims we'll be talking more about the syntax for props and react so your challenge is to

First create a new contact component in another file in this list below choose

one of them to move over to that new contact component that you create then back here in our app component I want

you to import that new contact component and create four instances of it in the meantime you can just delete all of the

articles that are here once you've moved one of them over into that contact component and don't be too worried about

the data that's in these because we'll get it back in the next scrims while you're on this last step of the

challenge where you import and render four instances of the contact card I want you to be thinking ahead of time

what the problem is going to be when we do it that way there shouldn't be a syntax error or anything like that but

there will be an obvious bug that shows up on our page okay I'll turn it over to you go ahead and start working on this

challenge all right so first we're just going to create a contact. jsx file and

I'll export default my contact component

function we'll just have it return one of these articles okay paste that in I

think that should be everything from this side let's go back to app.jsx and we will import contact from

contact and let's go ahead and just delete the four articles that we have

here and we'll render four of these contact components okay now if you

didn't take a second to think about what's going to show up before I hit save I want you to think now what are we

going to see when we hit refresh let's hit save and we have four Mr whiskerson

as much as we love Mr whiskerson we really want all of our contacts to be in our contact book and naturally the

reason that for Mr whiskerson are showing up is because we took the hard-coded data and we set that as

what's being returned from our contact component this is not terribly unlike having a function that's called add two

numbers and then just hardcoding having it return 1+ 2 this function can only

literally do one thing and it has no flexibility to work with other numbers that we might want to add together as

we've mentioned the way that I can make this function more flexible is by taking in parameters and then instead of

hardcoding the data in here allowing the person who's using the add to numbers function to provide numbers A and B and

then simply return the added sum of those two okay I think we've become pretty familiar with this little little

contact example that we have in the next scrim we're going to focus on how we can pass our information into the contact

component as we see it from this side of the equation then in the scrim that follows we'll go over to our contact

card and we'll see how we can consume or receive the information that's being passed in to the contact component when

it's being rendered from this side if you need a little more time with this code that's fine feel free to play

around and when you're ready let's see how we can pass information into our cont contct

component we need a way to pass data into our contact component otherwise we'll have to hardcode everything into

that component and it basically ruins the whole purpose of having reusable components fortunately react has chosen

a way to do this that makes a lot of sense for anyone who has done any kind of HTML in the past just like in HTML

when I have a reusable element like a link I can pass in different attributes in HTML to alter the behavior of that

link element I also can pass information into that link like an href so that the

link can act a little differ from other links that have different values for their href now in HTML I can't simply

come to my link and add whatever I want here and set it equal to something

because well this whatever I want attribute is not something that's defined in the HTML spec for the link

element that said the way that we pass data into a rea act component is going to look very very similar to how we do

it in HTML however because a contact component is a custom component it's

something that I created I can in fact pass in whatever I want as what looks

like an attribute in HTML but in react is called a property or more commonly a

prop and because it's custom I can create a prop that's called whatever I want and I can set it equal to whatever

value I want it to have so take a second to think if I'm passing data into my

contact component what kind of data would I want to be passing in the answer to this question is whatever information

we need to pass in so that the contact component can finish its job it can display what it needs to display

remember the goal is to take out any hardcoded data more specifically the image source the name of our contact the

actual phone number of our contact and the email of our contact those four pieces of information don't belong here

in the contact card unless for whatever reason we don't want to reuse this component let's go ahead and start with

the image over in our app component let's get rid of this whatever I want

and let's choose to pass in a prop called IMG I can set this equal to and

let's go over to our contact we'll just take the path to our file and we'll set

it equal to the path to that file now remember we haven't yet started working on how we can consume the props that

we're passing into our component so in this scrim we're just going to be doing some work here on this side of the

equation and in the next Grim we'll finally get to a place where we can see our contacts working the way that they're supposed to be working now I do

have a challenge coming up that you might hate me a little bit for giving to you but just try to trust that I have

your best interest in mind just like in HTML we're not limited to having a single attribute on our HTML elements

we're not limited to to having a single prop on our react components I'll go ahead and put these on their own lines

because I know I'm going to have a few of them and this is perfectly syntactically correct I'm going to go

ahead and do one more of these props and then the challenge that I know you're going to hate me for is you are going to

be in charge of adding all of the rest of the props for these contacts I guess we can just work from top down so we

already handled the image next we're going to be passing in the name and the name for this first one will be Mr

whiskerson and now the time has come let me type down what your challenge is I

usually don't love giving out busy work but this is an example of a time when getting your hands on the keyboard and

getting as much repetition as you can is going to be your best friend passing props into a react component is one of

the most common things that you'll do in any react application so let's start off strong a little bit of a trial by fire

your task is to add all of the rest of the data to the contact card instances and what I've done is I've pasted in the

article elements that we had in the old version when we were hardcoding everything keep in mind each one of

these contacts should have an image a name a phone number and an email and that's all the setup you need warm up

those fingers and get started on this challenge okay let's go ahead and do

this so I'm going to pass in a phone because I get to choose the names of these I could choose phone number like

this although I think it's fairly clear what it means when I say phone so I'm just going to pass in phone and let's go

ahead and grab the phone number and pass that in as data keep in mind what we're

passing in right now is a string everything is a string in HTML you kind

of have to do it that way you pass everything in as a string in react we're going to see that there's a way to pass

in any data type to our components but for now everything we're displaying is a string so this will work great and

lastly we have an email for Mr whiskerson and and here it is right here

pass that in and that should be all the information we need for our contact card to work when again eventually we come to

the contact side and consume the data that we're passing in I'll do one more of these by hand and then I'll speed up

through the rest of it so you don't have to tediously watch me do this we add our props right here after the name of the

contact and before the closing angle bracket make sure we leave a space there I'm going to pass in an image prop and

I'll set this equal to the path of the image for fluffykins it's right there

we'll pass that in awesome notice that I can do these in line as we're seeing here or if there's a lot of props I can

put each one on their own line either way is completely syntactically right and correct I'm a little worried that

you're not going to be able to see the stuff I'm typing behind the mini browser over here so I am going to put these on

their own lines okay the name let's just copy it to make sure we don't get it wrong

fluffy kins goes right there phone this one right here and

email is this guy right here maybe just so I don't have to scroll as far I'll go

ahead and delete these two articles now that I'm done with them and as I mentioned I'm just going to speed up

through the rest of this so you don't have to tediously watch me do this hopefully you already put in your time so we'll try to get through this quick

okay let's all be honest that wasn't really that bad let's go ahead and clean out our challenge text here now

hopefully one thing you notice is just how much nicer the organization of this is we've been able to have more of a

data Focus here where the data is most important and we've been able to have

more of a layout and design Focus here in the individual contact card and if we

want to make a change to how the contact card is laid out or add some new classes

or anything like that we can do it from one place here in the contact component and out here in the app component it

doesn't really care about that we're able to just pass in data and have the contact card handle everything else of

course if we decide we want to add additional data as we're passing this in then we would need to make modifications

to both the contact card and to the props that we're passing into the contact component but that's kind of

true of the way that we were doing it before anyway okay is it time for the big reveal let's go ahead and hit save

and of course we still have four Mr whiskerson don't worry your effort was not in vain in the next Grim we're going

to be learning about how we can consume the information that we're passing in as props to our contact component so that's

what we'll be doing next in the last lesson we learned how

we can pass our own custom data into the components that we're creating using

properties more commonly referred to as props in a way that's very similar to how we can pass data or information into

an HTML element using the HTML elements attributes we also talked about how there's a difference where in an HTML

element I can't choose to create whatever attributes I want on those HTML

elements they have to be attributes that are recognized according to the HTML spec but with react as we're passing in

data we can pass in whatever props we want we got to choose the names here we just happen to choose names that were

really logical and easy to understand always a good way to approach your variable naming so how do we receive

these on the contact side so we can finally get rid of all of the hardcoded data that we have in here well just like

a function that receives a parameter my react components will receive something in the functions parameter which will be

an object that represents all of the properties that we passed in really commonly I might call this something

like props but just like any function parameter name I can call this whatever I want in fact let's see what happens

when I console log whatever since that's the name we chose let me make this a

little bit smaller here and open up our console we'll hit save and we can see that we have a JavaScript object that

was console logged four different times now I want you to think for a second why did it console log four times if we only

wrote One console log well it's because we have four instances of our contact

component and remember although the syntax looks an awful lot like HTML really what's happening under the hood

is this function is getting called this contact function component is being executed and because it's happening four

times it's being executed four times and we have one console log that's being run four times let me actually copy one of

these from the console so we can talk a little bit more about it and I'll just paste it down here and I'll go ahead and

clean this up so it's a little easier to see what's going on okay so this was the

first one that got console logged and I think this should probably be looking pretty familiar what we received as the

parameter to our contact component or in other words what we're receiving as props I'll go ahead and change this to

props because that's much more common is an object a regular JavaScript object

where it's got properties that map to the values that we passed in in our app

component right here keep in mind we got to choose the names of these props so if I were to for example change IMG to

something like the full word of image we can hit save and now we can see that the first instance in our console doesn't

have an IMG prop but instead has a an image prop or an image property to the

props object that we're receiving now I don't want to go too far down that rabbit hole so we'll clean that up let's

go over to our contact we'll clean up what we have here as well and now it's going to be time for a challenge let me

go ahead and type that out now that we're receiving an object that has all

of the data that the instance of the contact component needs in order to correctly display our contacts up here

we should be primed now to update our contact component so that we can use that data instead of the hard-coded data

that it currently has so your challenge is to fix the code below to use the props object and the values that it

holds to replace the hardcoded values that we have below as a quick note there's going to be a small bug in the

code so I want you to do your best to squash it just don't be disheartened when you hit save and you see a little

bit of an inconsistency in the context this challenge does require you now to synthesize some of the information that

you've learned previously with the information that we've just been learning it's okay if that's a bit of a

challenge for you but I do want to encourage you again to give it your absolute best shot Don't just run into

the first sign of trouble and decide to hit play and watch me do it instead turn to an AI assistant turn to the scrimba

Discord Community ask a friend or Google it or go back and rewatch some of the

previous lessons if that might help jog your memory all of those are yes more timec consuming but they will be a much

better learning experience for you remember you're here to learn react and the only way to do that is to work

through it the more difficult way all right all right enough of a soapbox speech I'll pass it over to you to work

on this challenge I'll go ahead and clean up the

challenge text here and let's actually start right here in the H3 at first we

might decide just to try and type in props do name props is an object and it

has a name property so I should be able to do that well don't feel bad if you fell into this trap I happen to fall

into this trap all the time I'll hit save and we have literally props name showing up for every contact here of

course when we're inside of jsx and we need to evaluate a JavaScript value we

need to surround it in a single set of curly braces simple enough now when I hit save awesome even though the

pictures and everything else is the same the names are coming through our contacts are becoming unique let's go

ahead and do the same thing for our source now our source is a string but

we're going to pull that string off of the props object which is in JavaScript so I'm going to get rid of my quotation

marks and put a set of curly braces and then we say props

doimg now this is where that little bug comes into play we'll hit save and look

at that we have fluffykins Felix and pumpkin working but Mr whiskerson is not working why is that well it's a bug that

we introduced when I was talking about how we get to choose whatever name we want for these properties and in doing

so I changed this one to the full text of image so let's go ahead and change this back to IMG it's always going to be

important that the names of our properties that we pass into our components are consistent across every instance of that component now we hit

save and we've squashed that bug coming back to contact we can do the same thing now with the phone we'll go ahead and

delete the hard-coded phone set of curly braces props do phone and for the email

curly braces props do email hit save and awesome we're back to a working state

for our contact book now hopefully I'm not belaboring the point but over the years of teaching props I have found it

to be a sticking point for people in their Learning Journey and I don't want that to be the case for you so we're

taking it one little bite at a time and we've basically come to the conclusion here we've been able to Define what

information via Properties or props that we're passing into our custom components in the code of our custom components

we're receiving that as an object that we're deciding to call props let's get rid of this console log and then we're

accessing the data on that props object with regular JavaScript using props doimg props name and so forth if you

feel like you've been able to follow along up until this point give yourself a big high five or a pat on the back

that's a pretty big accomplishment I know we've put quite a bit of work into what now appears to be a fairly simple

concept but writing props in react is going to be an everyday part of your react life so hopefully you can

appreciate the extra time time and attention we're taking on it before we move back to our travel Journal I want

to show you a cool little trick that we can do when it comes to the props that we pass in so that's what we'll be

working on in the next scrim okay it's time to give you a prop

quiz sorry I couldn't help myself like before your task is to read through each of these questions to actually click

into the editor and type down your answers don't forget in scrimba if you have any changes that you make to the

code you can always save it as a note so that you have access to it later you can even record your own voice talking over

the top of the note if you wanted to keep an audio note and all of those are saved here in your account on scrimba so

pause now answer the questions through this quiz and then you can hit play and we'll go through the quiz

together number one what do props help us accomplish well just like parameters

being passed into a a function props being passed into a component help us

make that component more reusable as you become more and more experienced in react you'll realize that

there are times when it makes a lot of sense to pass props into a component so that it's reusable and other times when

it might be possible to pass props into a component but it's just not always necessary I can't tell you how much time

I have spent trying to create a component that's very reusable and then ended up only using it one maybe two

times that's just one of those things that will come with experience as you write more and more react code remember

when we pass props into a component it could be data that actually gets displayed as a part of that component or

it could sort of be like metadata that you're passing into the component that in a way configures it to act a certain

way either way it helps us make any component that we create more reusable

so that we can keep our code AS dry as possible okay so number to how do you pass a prop into a component in the same

way that you pass attributes to HTML elements like a source attribute for an

image you essentially do the same thing when you're passing props to a component so if I have my own component like let's

say my awesome header I'm using a strange name just to make it very clear that this is a custom one you can pass a

prop of your own choosing like maybe title into that component that brings us

to number number three can I pass a custom prop like for example blah blah blah to a native Dom element so for

example a div with the lower case D well the answer is no so we come to the next

part why not and that's because under the hood when react sees a regular HTML

element that we're trying to render we express that element through the jsx syntax and that jsx syntax actually

returns an object and the object describes the actual Dom node that should be created when we add an

attribute to a regular Dom element like a lowercase D div the object that this

jsx creates is expecting to be able to add this property to the Dom element and

since Dom elements don't have an attribute called blah blah blah I can't just choose the props that I want to add

to Native Dom elements like this div so let me try typing out a summary of

that so the answer is no because the jsx that we used to describe those native

Dom elements we want react to create will eventually be turned into real Dom elements and real Dom elements don't

have whatever properties let's say Properties or attributes specified in

the HTML specification which as we all know doesn't include properties like blah blah blah okay I think we

understand that concept how do I receive props in a component simply enough the

parameters to that component function will receive a value called props which of course we could name whatever we want

but by very strong convention will be props and that leads us to the last

question which is what data type is props in the component when I receive it this parameter which we're calling props

is an object which means if I want to access the properties of that object I

use do syntax so Props dot whatever the prop was that I passed in let's use blah

blah blah because that's what we said before okay awesome job on that quiz if you struggled with any of these

questions of course don't hesitate to go back and review the things that we've recently learned and when you're ready

Let's Move On by this point in the course you

should already be familiar with the concept of object destructuring but just in case we're going to do a quick recap

right now let's say we have this variable const person and it's equal to an object with an image name phone and

email properties as we've already seen I can go ahead and access any of those properties by calling person the name of

the object Dot and then the name of the property in that object like name and of

course this works as we would expect with Mr whiskerson showing up because that's the name of my person object

however in certain circumstances it can be kind of nice to destructure some of the variables out of our objects and use

them directly I can do that by saying const and then using a set of curly braces specifying the names of the

properties that I want to pull out of my object like image and name and then setting that equal to my person object

what this does is it declares two new variables in one go IMG and name and it

sets their values equal to the value of the property that has the same name

inside of this object so if I go ahead and now just console log name not

person. name but just name we'll hit save and we get the same thing Mr whiskerson I can do the same for mg and

we get the path that was inside of this object but is now outside in a global variable it's important to note at this

point that I don't get to decide what I'm calling these for example I couldn't just decide well I actually want this to

be image the full word spelled out because we'll see if I try to get that from the object it's going to be

undefined because there is no image property on this object now JavaScript

doesn't just leave us high and dry there is some trickery I can do in case you weren't familiar I can say I want to

grab the information from the IMG property but I want to rename it and I can put this little Co in here I want to

rename it image and now when I do that I do correctly get the information from this IMG property but renaming it to

image this isn't terribly important right now I just wanted to qualify what I said when I said we have to use the

same names as the properties in the object let's back this part off to a

working State here and I'll just leave this down here in case you want to play with it but let's let bring this concept into react by seeing how we can apply

object destructuring to the props that we're bringing in remember props is an object even if you were to only pass a

single property in your react component it would still come in as a props object with a single property on it and because

it's an object I can choose to just destructure it right here in line I happen to know that it's going to have

an IMG property a name a phone and an email of course now that I've gotten rid

of my props object and instead have defined these four new variables and pulled their values from the props

object my code below is no longer going to work so that leads us to a quick

challenge okay your challenge is to fix the bug that we've just introduced now that we are destructuring the props

object right here in line in the definition of our contact component go ahead and get started on this challenge

okay should have been a pretty straightforward one remembering that we are no longer bringing in the props object all we really need to do is take

all of the instances where we're saying props dot image or name or phone or email and get rid of the props dot part

we can hit save and sure enough our contacts are back the main reason I'm taking time to show this is because it

will be a really common thing as you're seeing react code out in the wild to see props being destructured in line the way

that we've done it right here as far as I know there's no functional difference between destructuring them in line like

this or having the props object like this it really would just depend on your own personal preference or more

importantly the preference of the maintainers of whatever repository of code you're working in it's more important above everything else to be

consistent with how you're writing it I personally oscillate between the two and I don't know that I have that strong of

an opinion one way or the other however for the remainder of this course I will likely just be using the props object

for a pretty simple reason when we get to a point where we're declaring other variables inside of our component code I

find it does become a little bit easier to keep track of which variables are coming from outside from props and which

variables are coming inside being defined inside the body of our component by signifying that something is coming

from the outside with that props doob syntax before it so I'll go ahead and

change this back to props we've already changed this back to props and although it does provide a little bit of extra

visual clutter I do find there being a benefit in knowing very easily when something is coming down through props

and when something is being defined in another way let's clean up our code a little bit here and although there

certainly will be more for us to learn about props going forward it's time for us to get our hands on the keyboard and

practice these props a little bit

more all right I'm not going to make you spin up an entirely new react app completely from scratch but we are going

to be starting pretty close to the beginning in my index. jsx I am importing and rendering this app

component and the app component I've just barely scaffolded for you this challenge is going to require a little

bit more than I have in the past but you should be plenty well equipped to complete this challenge we're going to

create a little page where you display some of your favorite jokes and so first you'll need to create a joke component

that will be in its own file and then here inside of our app I want you to import and render maybe four or five

instances of that joke component each one of those joke components should receive two props a setup prop and a

punchline prop and then render those inside of your joke component really however you want we just want to display

the text of the joke on the page take some time to look up some of your favorite two-part jokes that have a

little setup in a punchline or maybe you already know some off hand or if you need a little bit of inspiration you can

go over to jokes. MD where I've included some of my favorites I do have a little extra credit here I'll let you read

through this and decide if you want to do it or not it does touch on something that we haven't yet taught so it will

likely include some outside research in order to complete all right the time is yours start working on this

challenge okay I think I'm going to work a little bit backwards here so first we'll go ahead and you know what I kind

of know what the challenge says so I'm going to buy myself some room here we'll import a joke component which we haven't

yet created so we'll have to create that in just a second and inside here we'll

go ahead let's turn this into maybe a main element and we'll

render five instances of our joke component one 2 3 4 5 all right let's go

over before I hit save and kind of Crash everything let's create our joke.

jsx and over there we'll get started with our export default function joke

and let's do a little bit of a sanity check here I'm just going to render an H1 that says inside the joke component

okay hitting save I should see five times yep inside the joke component perfect and this Scrolls down a little

bit for the fifth one okay so I need to pass the data for my jokes into my joke

components so for each one of these I'm going to add a new prop called setup and

we'll set that equal to a string I'm just going to go over to my jokes. MD and copy each one of these

jokes okay I've copied those and then over in my app.js we'll go ahead and

paste those in and I can already tell this is going to be a little bit too horizontally wide for the setup that I'm

recording on so I'm going to go ahead and put each one of these on their own lines all right so I'm passing in a

setup let's go ahead and also add a punchline prop and I'll just do the same thing where I copy the punch lines from

over here in my jokes file and we'll go back and paste those in right there

these are great jokes by the way I don't know if you've actually taken the time to think through them but there were some of my favorites okay job done right

what do you think will happen when I hit save I don't think I fooled too many of you you're too smart for that so if I

hit save we'll see I'm still seeing inside the joke component five times I'm passing my props into my joke component

but my joke component is not making use of them so we'll go ahead here and accept our props and let's just go ahead

and console log our props just to take a look at that okay cool we're getting

five different objects again because I'm rendering five instances of the joke component and the props that it's

receiving is an object with a setup property and a punchline property perfect let's go ahead and scaffold out

the rest of this component so maybe I'll just create a div actually I might just

create a fragment here we'll probably need to turn that into a div later if we want to style it but for now this will

be okay and let's just put a paragraph for the setup a paragraph for the

punchline and maybe we'll have a little separator with a little horizontal rule this will be a little bit rough for now

but that's okay all right if I hit save we'll just have a bunch of horizontal rules showing up because my paragraphs are empty let's go ahead and say that I

want to First display props do setup and then I want to display a props do

punchline again remember we need the curly braces otherwise we would just be literally putting in the text props do

setup and that's all that would show up five times okay Moment of Truth awesome we're getting our jokes displaying on

the page I think I'm going to take just a second to add a little bit of style here all right all I did was add a

little bit of margin to the body and then I gave a class name of setup and bolded the text I also gave this one a

class name of punchline but I haven't actually done anything with that yet just trying to keep it simple for now

and just like that we've been able to pass information from the outer component of our app or in other words

the parent component that then renders well first renders this main element and then inside of that it has these

children components of our custom joke component and we pass the data in through props a setup prop and a

punchline prop now I did have a little extra credit and I figured I would go through this at this point although what

we're about to talk about isn't necessarily something that we've learned yet for example let's say we have a joke

that really only has a punchline it's just a oneliner joke and it doesn't have a setup my personal favorite that I

included in the example is this one that says that it's hard to explain puns to

kleptomaniax because they take things literally well in this case I'm not going to be providing a setup there's no

reason to have a setup there however if I hit save we'll see that we just have this sentence that's kind of floating in

here I guess it's not as apparent there but let's imagine in our joke we decided instead of just having the joke text

there we were to say something like setup colon and punchline colon and then if I go ahead

and hit save we see we just have this setup that's floating here without any text there again this isn't something

that we have learned yet we will be learning this in the future but if you took the time to do the extra credit you

might have come across a concept called conditional rendering with conditional rendering I can tell react that I only

want to include this paragraph element if a certain condition exists one way I

can do that there's a number of different ways but one way is I can surround the entire paragraph element in

a set of curly braces and then at the beginning before I render the paragraph I can say if there's a props do setup or

in other words if that is a truthy value then I want you to render or R return

this paragraph element one kind of shortcut way I can do that is to use a double mersand essentially this says if

props do setup is truthy it's an existing value it's not an empty string or undefined then I want you to return

this in the place of this little expression that we have here it's maybe not a huge Improvement but I can go

ahead and hit save and we just show our punch line here we don't have the floating setup that we had before the

really nice thing about react is that it uses just plain JavaScript under the hood which means I could accomplish

essentially the same thing in another way let's say instead of just removing this completely from the Dom if prop.

setup doesn't exist i instead wanted to maybe add well let's say a style prop I

can say the style is going to be display of none but only if and uh let me move

this down for just a second only if props do setup does not exist one way I

could accomplish this is by using something like a Turner a regular JavaScript expression of aary so I would

say display is going to be well first is props do setup a thing if so then maybe

we say that it will be a display of block but otherwise it will be a display of none we can hit save and see we

essentially accomplished the same task although this way does appear to be quite a bit more complicated than what

we had before I'll go ahead and reverse that back to the conditional rendering which is also something you'll see very

commonly the point is react us using JavaScript under the hood and there's a lot of native JavaScript apis and

techniques we are going to be learning about that help us display things on our page in the way that we want to I hope

that this was a helpful exercise I'm really looking forward to seeing people's different jokes that they have

and we have one more little thing that we need to learn about props before we're able to move forward and continue

with working on our section project of the travel

Journal we have just one more thing we need to cover regarding passing data through props before we can finally

continue back on with our travel Journal project up until now we have only passed this string data type through our props

and that's what we're most familiar with we've talked about how props are a very similar concept to passing attributes in

HTML and in HTML we have to pass a string there isn't really another alternative in certain circumstances we

can pass something that looks like it's not a string like a function for example but in reality we still have to surround

them in these quotation marks so they're a string with react however because we're working in JavaScript we're not

limited to just using a string and I actually wanted to make this into a challenge that will help you think a

little bit more critically so your challenge is to think how you might go about passing in a prop that isn't of a

string data type let's say for example we wanted to pass to each one of our joke components an up votes and down

votes prop that is a number instead of a string as well as maybe a prop that is

an array of comment objects and a Boolean of whether or not the joke is a pun with this challenge you don't

necessarily have to go through and actually do this if you'd like then you're absolutely more than welcome to

but I'm going to pause the scrim now and give you a chance to Think Through how you might do this and if you'd like play around with the

code while we're here inside of our jsx as we've learned we can switch over into

a sort of JavaScript mode by using a set of curly braces and I can do the exact

same thing when it comes to passing props let's say I wanted to add an upvotes count I can create the upvotes

prop and then instead of putting quotation marks because that signifies that I'm about to pass in a string since

my upvotes may be something that I want to do some kind of math on like if I were to add a little thumbs up or heart

icon that when a user clicks it it would add one to the existing upvotes then

instead of using a string I'm going to pass in a set of curly braces and then put in whatever number I want to pass as

my data type down to my joke component let's go over to our joke component and just console log our props again just so

we can see what's coming in now and I'll open up the console here and awesome we can see that with the first one going to

move this up a little bit with the first one we have just a punch line that's one we didn't pass a setup to but at the end

of our object we have an upvotes that says 10 and it's the number 10 it's not a string 10 and because props do upvotes

is a number if I needed to I could do some math on it so for example I could console log props do upvotes plus one

and I think I'll probably get some not of numbers or undefined here because I only put it in one of my components on

this first joke but we can see for the first one in the console we get 11 because it originally was hand and then

we added one let me bring this back to just props let's go back to our app here

and if we wanted to do something like a Boolean for this is pun property let's

go ahead and say this one is pun and huh is this one a pun that's a little

strange it's about puns and I think it is a pun too it's kind of a double on Tundra it's a great joke so we'll say

this is a pun it's a true as a pun again not a string but the actual Boolean value of true let me go through and add

the is pun property to the rest of these and jeez most of these are puns I guess

this one isn't really a pun we'll go ahead and call that one false let's go ahead and hit save to see what we get

for the consoles and sure enough we have a new prop called isun and it's either the Boolean value true or in the case of

this last one it's the Boolean value false again because it's a Boolean I could do an operator on it like the not

not operator or flip it from its value with just the single knot of course because it's a Boolean value I could do

something like console log knot props do is pun and flip it with this knot

operator we can see that we get the opposite of what we had before whereas if I had passed this in as a string it

wouldn't really do what we were hoping that it would do and this goes just as well for things that are a bit more

complex like if we wanted to pass in maybe an array of comments I can set a

new prop called comments do one set of curly braces this can be a little bit confusing because it looks like the

Syntax for a JavaScript object but remember this is just getting me into a JavaScript expression inside of that

expression I can do my square brackets in order to start a new array and that

new array might be an array of objects this is looking a little bit crazy it

sometimes can help to put these on their own lines like this and these comments can be as complex as we need them to be

maybe each one of them has an author that is some sort of author ID like a user ID it might have a body which is

the text of the actual comment or maybe this would just say text it could have a

title if for some reason your comment is owed to have a title and of course because it's an array we would probably

have multiples of these we can come put our console log back I'll just log all

of props since not all of them have comments and actually just to make it a little easier to see we'll go ahead and

just console log prop. comments we'll get some undefined but there we see we have an array of two comment objects in

the first joke that we put those properties in just for the sake of completeness I think it's helpful to

know that technically it's totally fine to take your strings and also surround them in curly braces because a string is

also a valid data type in JavaScript but I think because we're already so familiar with writing strings as our

attribute values in HTML it's also completely valid just to leave the curly braces off and pass a string directly to

your prop like this however I couldn't do the same if I wanted to pass in any other data type than a string like the

value true this is going to be a syntax error and I would have to surround this in a set of curly braces

okay I think you probably get the point here now we should be finally primed to get back to our travel journal and take

the next few steps that we need to take I want to interrupt our regularly

scheduled programming here and talk about how we can handle static assets outside of scrimba naturally I always

recommend people follow along this course on scrimba

docomo on your local machine or wherever it might be you might find that the way that we're referencing static assets

like these images may not work in your environment using a build tool like vit is going to essentially rearrange where

these images are being held and so referencing them with a relative path may lead to Broken links think of it

this way when you're using a system like vit it's going to rearrange your code under the hood to make things a bit more

performant and especially when you run a final build that gets deployed online

it's going to essentially compress all of this code into single files like a single giant JavaScript file that

includes all of the react Library as well as all of your code a single HTML

file and a single CSS file and more likely than not a place for all of your images to live but the structure of your

folders will be different at that time and so that's why these relative paths are likely not going to work to solve

this problem what you can do is import your images from their relative path so

that JavaScript is aware of where they were before all of this restructuring happened and the build tool in the

process of building itself can fix the relative paths that you used when you were importing those assets if all of

what I just said makes absolutely no sense really don't worry too much about it I just wanted to make sure I address

it because I know in past versions of this course it has been a bit of a confusing point and handling static

assets the way that vit does works here in scrimba because we're using vit as our bundler under the hood at least for

these react projects all this means is that when I have something like this image that is a hard-coded string

leading to the relative path of the Mr whiskerson PNG file if you're working locally on your machine what you can do

instead is say I'm going to import let's call it Mr whiskerson from and then I'm

going to use that relative path now I have a variable that I can use to

replace this hardcoded string I'll put a set of curly braces and just say this is Mr whiskerson so I'll go ahead and do

this for all four of them and we'll see that everything is still working just fine okay I've imported each one of

these static images and now I'll go through and replace the image text that we have here okay we can hit save and

sure enough all of the images are working just fine now throughout the rest of this course you may or may not

see me doing this kind of import of static assets so I just want to warn you ahead of time if you are following along

in an environment outside of scrimba you may have to take just one extra step to import whatever static asset I'm

referring to whereas in scrimba I can just use the relative path as it is okay

let's get back to our regular lessons all right we're finally back

here at the travel Journal but we have learned so much about props and reacts in fact so much that it might look

strange that if we look back at our entry component we still have everything hardcoded let's go ahead and fix that

over in our app.jsx we have our challenge text your challenge is to pass props to our entry component right here

so that it can display its data I've put all the data that you need over here in data. MD so that you can find each prop

name and its value one thing that's a little tricky about data. MD is this image prop IMG prop it's going to be an

object so make sure that you pass it in correctly and that object will have both an SRC property and an ALT or alt

property then when you go over to the entry component just make sure that you remember that that IMG is not going to

be a text data type it's going to be an object so you'll have to deal with that accordingly then of course after you

pass in all of the props that entry needs to display its data make sure as I mentioned go over to entry. jsx receive

those props and replace any of the hardcoded data in that component to use the incoming props instead this is one

of those refactors that when you hit refresh it's going to look like nothing changed but that's just a normal part of

web development all right it's your turn start working on this challenge

all right I already know I'm going to be passing enough props here that I want to put them each on their own lines and

let's go to data. MD okay we'll start off with our IMG which will be an object

with a source and an ALT all right so IMG prop is going to be equal to and

this is where things might have been a little bit tricky remember if we're going to use a data type other than a

string we need to start our set of curly braces in order to get into a JavaScript expression and then my object is also

going to have a set of curly braces hopefully that didn't throw too many people off if it did that's okay it's

something that we'll just take a little bit of time to get used to our image is going to have a source property which

I'll just leave empty for now and an ALT property which I'll leave empty let's go

grab that data from right here okay I'll put these on their own lines just to

help so that when I paste it in it will work correctly all right let's hit paste and perfect okay that's passing in

correctly let's get to the next prop Let's see we have title and Country I

think I can remember those well enough so we'll pass in a title this is a title for our entry and it's going to say

Mount Fuji and oh it looks like I have an extra comma over there let's get rid of that and oh I've got my curly braces

messed up okay let's go back to data. MD and let's see our next two are title and

Country so I think I can remember both of those our next prop we'll start here on the next line we'll start with title

and that's going to be equal to Mount Fuji and then our country this is for

the little name next to the map marker there is equal to Japan okay let's see

what else we have Google Maps link I'll go ahead and copy both of these and we

will put in a new prop Google Maps link and we'll set it equal to the link that we just copied and I think almost done I

think we just have the dates and the text there so yep dates and text and

we'll just add those in all right it can be a little deceiving if I hit save now it'll look like everything's the same

but that's not because we succeeded in our challenge which I can remember so I'll get rid of the text but because we

haven't changed our entry component at all looks like we're already receiving props so I guess I did a little bit of

that work for you just to make sure things are coming in correctly let's go ahead and console log our prop

okay cool our image is an object that has a source and an alt we have a title a country Google Maps link which is

rather long our dates and our text at this point the rest of this is just replacing any of the hardcoded data we

had with the new incoming data let me minimize this just to buy some room here on the image and we'll go ahead and

change some of these so for the image source I need to put a set of curly braces because I need to evaluate the

JavaScript expression that's coming in through props and we had

img.src I think this is probably the trickiest part of this but shouldn't have been too bad we'll go props

img.com our image is coming through and I can only assume that our image alt

text is coming through as well all right let's do the rest of this so right here we have hardcoded Japan we're going to

instead put props do country for my Google Maps link I'm going to leave the text as hardcoded cuz every one of mine

will say the same thing but this hre is what can get replaced so I'll put a set of curly braces and we'll do props dog

Google Maps link I think is what it was let me just double check that Google Maps link yes okay here we have our

entry title let's go ahead props do tile the dates will become props DOD dates

and the text will become props . text is it text yeah text perfect okay the

boring Moment of Truth we'll hit save and everything looks the same but of course we know as the developer of this

component that the data is no longer hardcoded but instead being pulled in from the outside although this

particular update might seem a little boring it does mean that we now have the power to reuse our entry component to

create more instances which aren't just duplicates of Mount Fuji this is a huge

step in our journey and react learning props is one of the more difficult things as I've mentioned for beginners to grasp hopefully this exercise has

been helpful if you were able to get through this exercise without too much additional help then giant kudos to you

that's a big step if not that's completely okay remember you're not here to get a grade or to set any kind of

speed record through this course go back practice what you need to practice take the time you need to take because we do

have a lot more to learn but the new things that we'll be learning will be hinging upon the knowledge that you've

learned thus far once you've done a little happy dance and congratulated yourself then we'll keep moving

forward this lesson is basically a spoiler alert for what we're about to learn because we are going to see how we

can use the array.map method to take regular JavaScript data and turn it into

jsx elements that can be displayed on the screen and so this felt like a really natural time to do a quick review

of the map method if it's been a while or you're feeling a bit hazy about the do map method you can click the

screenshot here that will take you to the mdn docs on the map method and I would just recommend going through

Reading everything they have playing with the interactive demos they have and everything like that to help bring you

up to speed on do map so what we'll be doing is a series of challenges I've got three challenges here but instead of

just going through everything in one go I'm going to have you do challenge one first then we'll we go through it

together then challenge two go through it together then Challenge three remember the goal is to look at our

input data and try to turn it into some output data using the map method so

pause now and start working on challenge

one okay so the first thing we'll do is run nums mapmap takes a callback

function and I'm going to use a function declaration just for now to better

understand exactly what's going on here and this callback function is going to run for every item in my array that I'm

running map on and then whatever I return from this function so I'm going to add a return inside here whatever I

return from this function will get placed at the same index as the original item with whatever kind of modification

we make to it and then in the end map returns a brand new array that will be the exact same length as the original

array and so we should probably be saving that let's say const and these are squares so we'll say squares is

equal to the array that comes back from calling nums map and then this function will be taking a look at every item or

probably better is to say it's going to look at each number or num inside of the original array and then we will have it

return num * num that'll give us the square of that number now if I console

log squares we should get our output of 149 16 and 25 in an array and sure

enough there it is okay let's move on to challenge two I'm going to comment out this console log this time given an

array of strings return an array where the first letter of each string is capitalized at this point you might be

recognizing we're essentially just doing some JavaScript algorithm challenges here obviously do a quick search on

Google if you need to so now it's your time again pause and work on Challenge number two

well let's set everything up we'll say maybe capitalized it's not really capitalized but I think you get the idea

we'll run names. map and this time I think I will use an arrow function

whether or not you're really familiar with arrow functions I think by now it's probably time that you become versed in

Arrow functions so I'm going to use that syntax and over time I think you'll just get used to it the more you see it I'll

start out by opening up the body of this function and using a return but then we'll use some of the benefits of an

arrow function by removing some of these extra characters that we don't need now this function is going to be looking at

each of the names inside of the names array so we'll call it name and like I mentioned now we're essentially just

doing a JavaScript algorithm challenge so I'll say we want to return and we can

actually index into Strings as if they were an array so I'm going to say get me the first character of this name and

we'll call do2 uppercase and then I bet many of you came across the slice method

so I'm going to use name. slice starting at index one now if I don't provide a

second parameter it means just start at index of one or in other words the second character of the string and get

me everything from that point until the end honestly I'm winging it a little bit so we'll see if this is working I'm

going to console log capitalized and let's run it and see how we did okay

that looks awesome great now that brings us to challenge number three and this is the one that's really intended to

prepare us to understand how we can use the map method alongside jsx in react to

turn regular JavaScript data into something that gets displayed on the screen by react this time you have

another array of strings we have a few different Pokémon names here and your job is to use the map method to return a

new array of strings this time the strings are kind of like HTML strings where they're surrounded with these

paragraph tags opening and closing tags keep in mind we are not doing anything react specific there's nothing special

about putting the paragraph elements or the paragraph tags around the text that you want but this will be very similar

to what we do when it comes time to do this in react so pause now and work on Challenge number three

all right hopefully you found that was maybe even easier than Challenge number two let's start off by creating a new

variable maybe let's call it paragraphs and we'll set that equal to the array that comes back from calling pokémon.

map and this time let's use an arrow function again I'm going to look at every single well let's see I think

Pokemon is both the singular and the plural form of Pokemon so maybe we'll just call this mon for individual

monsters and let's start out by opening the body of this function like we did before and then I think we'll go through and clean up some of our Arrow function

extra characters that we have so I'm going to return and essentially all I'm doing is taking the string of my

individual monster man and surrounding it with the paragraph opening and closing tags so I'll use a template

string here and we'll put in our paragraph tags like this but then in the

middle I will just inject the individual string of the Pokémon and now if we

console log paragraphs okay we get an array of well

they're still just strings but they look kind of like paragraph elements awesome work now if I wanted to clean up my

arrow functions I only have one parameter so I don't need those parentheses surrounding there and then I

could take advantage of my implicit return by moving up the return value

here and getting rid of my curly braces and sure enough that's much more concise I can do the same thing up here now this

return value is a little bit longer so you can decide whether or not you actually want to do this but I can put

that up on the next line or if you want to use the next line you can surround your return value in parentheses and

then start that on the next line and that should work just fine too let's just double check

that okay looking great in fact I suspect that these aren't actually necessary in the first place yeah I

guess the parentheses really aren't that necessary I think I like them there just for maybe my own sake in keeping things

balanced but you can do it however you want okay now that we've reviewed array. map we should be perfectly primed to

jump right into the next lesson we just did a review on how we

can create arrays from other arrays now the next thing we need to understand is that reacts knows how to render arrays

let's say for example I had an array let's say this is the Ninja Turtles and

for now I'll just set this up as an array of Str and this is an example of a time when it

can be kind of helpful just to see what happens scrimba is a great environment to do this in so let's see what happens

if I want to render this array of Ninja Turtles as I said it's just an array of strings but of course if I were to just

type Ninja Turtles like the variable name then I would just get the literal text Ninja Turtles so let's go ahead and

Surround this in a set of curly braces and see what happens okay look at that react was able to render it of course it

just mashed everything together because it's trying to render these strings and it looks like it just concatenated them

and stuffed them on the page as bare text of course there's no difference if we wanted to instead of setting this as

a variable ahead of time we just wanted to hardcode an array directly in here I

can comment this out and see that we get the exact same result let me put this back so we're using our Ninja Turtles

variable and although for our example we're using an array of strings it could

be an array of any data type well that's not actually entirely true if I were to change this into just a

regular object let's say first name Bob and uh I don't even need to go more in

depth than that I wish I were a Ninja Turtle but I'm just a regular person let's see what happens when we try to

render an array with objects in it okay we do get an error and that says that objects are not valid as a react child

so that is an error that you will likely see often in fact this has nothing to do with arrays react simply can't render

objects unless that object is of a very specific type remember way back in the

beginning of this course we learned that jsx simply returns an object so if I

were to say H1 and let's go ahead and put

donatella's name in here and then console log jsx let me get rid of this

for now we can remember that jsx is an object so although react isn't able to

render the objects that we create or maybe that we pull down as data from an API somewhere it is able to render a

specific kind of object and that is an object that was created with the jsx

syntax or if you remember under the hood the object that gets created with a call to react. create element so let me pull

this back to when we had our array of Ninja Turtles and I'm going to give you

a little challenge okay this is bordering on the realm of busy work but

for this challenge I want you to manually turn this array of strings into an array of jsx elements so you'll

actually get rid of the quotation marks by surrounding each one of the Ninja Turtle names with I put an H2 element

but you can choose and play around with whatever element you want then before you hit save try to think what's going

to render to the page and see if you can make sense of what it's doing go ahead and get started on this

challenge okay I'll go through this pretty quickly just so you don't have to sit and watch me type out some jsx code

okay let's clean this up to buy some room here so in this case all we've done is we've taken an array and we filled it

with jsx elements or in other words we filled it with those special react objects that get created when we use jsx

and if we go ahead and hit save we can see that we actually get our H2S displaying on the page so react was able

to take an array of jsx elements and render them exactly how we might expect it to in the end this would be really no

different than if I were to take this list and to just paste it directly in here of course I'd have to get rid of my

commas for that to work but we can see hitting save gives me the same results let's back this off to using the array

again and I'll hit save you might have noticed that there is a little warning that says each child in a list should

have a unique key prop we're going to cover that a bit later so don't be too concerned about that now all right so

combin in what we just learned about how react can render arrays of jsx elements

specifically is what we're most interested in and what we were just reminded of previously with the capabilities of using array. map we can

take those two topics and we can apply them to our react apps so that instead of taking this data and hardcoding a new

instance of a joke component and putting in the punchline and the setup we can instead pull in all of the jokes data

from an outside source which is what might happen if we were pulling the data down from an API for example as an array

of data and turn that array of data into an array of joke component instances

where we pass the specific data down to those joke components through props that

might have been a little bit hard to follow just for me talking so let's get our hands on the keyboard we're going to do some challenges in the next

scrim let me walk you through a couple quick changes that I made before we take what we've just learned and apply to

react first of all as you probably already noticed I took all of our hardcoded instances of our joke

components and just moved them outside here and commented them out then where we used to have jokes. MD I created a

jokes data.js file we're not quite ready to learn how to pull data down from an

API and use that data in our react apps we are going to be doing that in the next section so for now we're just going

to kind of mimic that I'm exporting an array of joke objects from this file

this would be kind of similar to the data that we're pulling down from an API then all I'm going to do in my app

component is import jokes data from that file and we can see if we console log

jokes data then we do successfully pull in the array of joke objects great so

now what I can do with this jokes data is I can create a new array of elements

let's go ahead and call it joke maybe joke elements and I'll set that not equal to an array that I'm going to

Define with my square brackets here but instead with the array that gets returned by calling jokes

data.map map takes a callback function so we'll just stub that out for now and it's going to look at each joke and as

it iterates over the array of jokes data I'm going to have access to each joke in

that array we'll call it a joke object and that's going to be an object so this is a joke object well it's not a joke

object object it's not a fake object it's an object that represents the data for a joke so what I'm doing here is I'm

taking this array of regular JavaScript objects and I'm going to turn them into

an array of joke elements so for each item in my jokes data I'm going to

return a joke component and then I can pass the data from this JavaScript joke

object down through props to my joke component and by I can do that I mean

you're going to do that so that's going to be a challenge let me type that out all right your challenge is to see if

you can correctly pass the necessary props to the joke component in the do map and render the joke elements array

so that the jokes show up on the page again you can look down below to see what the structure of our joke

components looked like and after you finished passing those props as it mentions don't forget to render the joke

elements array that can be kind of a pain to not realize why nothing's showing up I'll hand it over to you now

to work on this challenge okay well if we look below we can see

that our joke component is able to receive a setup prop and a punchline prop and if we look at the jokes data

that's coming in we specifically have a property in each object that is called setup and another that's called

punchline so in my jsx I'm going to include a property called setup and I'll

set it equal to the data that I find inside of my joke object do setup I

think it's really important to make a distinction at this point the data that we're pulling in from jokes data this

one has a predefined property called setup let's assume I were pulling this down from an API that I don't get to

control I'm sort of beholden to the property name that they chose on their joke objects if for example these

weren't called setup but maybe something like question then when I'm trying to

render this data I can't use joke. setup just because I thought setup was a better term I have to use the one that

they said joke. question in fact let's just verify that this is working I'm going to skip ahead and render my joke

elements right now I hope we don't get any errors because we're not passing in a punch line let's just see what happens

okay my punch lines are empty but my setups are working so the distinction I think is important to make is that the

array of joke data that we're getting in that array has a question property I'm going to change this back in a second

but our joke component which we got to Define we can choose whatever prop name we want to to pass in because I'm

calling it setup inside of my joke component I'm still going to be using props do setup whether the data coming

in used the phrase setup or not just so that we're not getting our terminology crossed or any kind of confusion

happening I am going to put this back to setup and then we'll go ahead and change this back to setup but I remember in the

beginning that being a confusing distinction just remember that you get to determine what you call your props in

the components that you write and when you're in control of the data you also get to choose its structure very often

you'll find that you're not in control of the data and you are stuck with whatever names they chose when they were

creating the database we can hit save and see that our setups are still working okay let's just go ahead and

finish this off by adding our punchline prop and that is going to be equal to

joke. punchline we'll hit save and awesome our jokes are working again now

we can see if we do a little bit of cleanup let's get rid of our challenge text and all of this comment out old

stuff that we were hardcoding before we can see just how much simpler our code now is because we're pulling in data

from an external source which is often times what you'll find yourself doing and we can use regular JavaScript

methods like the map method to create an array of joke components and pass that data in keep in mind our code here

wouldn't change even if we had a thousand jokes in our jokes data unless of course you decided you didn't want to

immediately display all 1,000 jokes on the page then we'd have a little bit of work to do pagination or whatever it

might be all right now we're equipped to go back to our travel journal and not just be stuck with our single Mount Fuji

trip but instead we can take more trips and we can store that data in an external Source in this case just like a

Javascript file and then iterate over that data to display all of the different entries that we want to

display in our travel Journal so that's what we'll work on next but before we do that I do want to give you a little quiz

about what we've learned regarding using the map method in our react

apps all right it's time for another quiz this time specifically about what we were just learning with map make sure

to actually click into the editor and type out your answers and when you're done you can hit play and we'll go

through it together okay number one what does the

map array method actually do the map array method is a vanilla JavaScript array method it's something that's built

into JavaScript and has nothing specific to do with react and you can run that method on top of any kind of array in

JavaScript you pass to it a callback function it will iterate over or Loop over every item in that array run the

function that you pass to it and whatever you return from that function it's going to put in the same index of a

new array that gets returned from the map method a key part of that is that it

returns a new array and I'll go ahead and kind of summarize what I just said

so it returns a new array and then whatever gets returned from the Callback function provided is placed at the same

index in that new array usually what we end up doing is taking the items from the original array and modifying them in

some kind of way okay question number two what do we usually use map for in react usually in react we receive some

kind of array of raw data usually from an API in our case we're just stuffing

it inside of a Javascript file and exporting that array but we we receive that raw data and we turn it into jsx

elements that can be displayed on the page okay and number three I don't believe is something we've explicitly

talked about but it would require some critical thinking why is using map better than just creating the components

manually by typing them out well I'd say there's a few reasons first of all we don't always know what data we're going

to have ahead of time in our case we know exactly how many jokes we have and what the jok's data says so we

technically could manually type it out in fact we did manually type it out however in my experience that's not

usually how it works so I guess answer number one we could say we often don't

have the data ahead of time when we're building our app so we simply can't manually type them out even if we wanted

to a second reason though that I think is maybe a little more important is that by using the dot map method we can make

our code a lot more self- sustaining in other words if we were to manually type out all of our jokes like we had in the

original version and then our jokes data were to update we would have to go back to our code and type out new jokes

because new jokes got added to the data however when we're mapping over the array of data we are accessing that

array directly which means that if there are new jokes added to the end of this list simply refreshing the page is going

to pull that joke into the app it will render this array including the new jokes that we added If instead of adding

it here it for example got added to a database that we pulled that data down from an API all we would need to do is

fetch that data and the new jokes would be included and our app would render those new items so let me try to

summarize that here it's not terribly unlike when we're writing a c style for Loop let's say we had let I equal Z and

often times we'll find ourselves looping over the length of an array so we'll say I is less than some array. length and

then of course i++ and fix this typo here the reason

we're using some array. length is because we don't want to know how long the array is we just want it to iterate

over an entire array no matter how long that length is so let me try to summarize this here essentially it makes

our code more self-sustaining it doesn't require additional changes from us the developer to change the code whenever

the data changes great job on this quiz hopefully you were able to answer all these questions now let's finally get

back to our section project and start applying what we've learned all right everything that we've

worked on so far has come to this point before we start let me just walk you through a couple things really quickly

first of all instead of having the markdown file that we had before with some of the information I've created

this data.js file this is exporting an array of objects each object represents

one entry in in our travel Journal I've also added an ID property to each one don't worry about that for now we're

going to be talking about that really soon but for now you should have all the data that you need when you import this

array which is part of your challenge let's see right here to import that array from data JS map over that array

to create an entry component for every item in that array and then to render that array of Entry components imp place

of the current entry component this current entry component is displaying our Mount Fuji right now but after

you've mapped through the array of data and displayed that in place of this one you should have all three of them showing up I believe there's actually

one really small style change that I want to make I'm going to add a margin bottom here of 36 pixels just so that

they're not shoved up right next to each other okay the time has come I know that you can do this challenge it represents

a culmination of everything that we've learned so far throughout this section so it's possible this will be a little

bit of a challenge if you do find that it's way too hard of a challenge for you then that's a good indication that you

should probably pause doing this challenge go back revisit some of the lessons and the examples and the

practices that we've done throughout this section practice them again and reach out to the scrimba community if

you have any questions at all head over to Discord there is always someone from the community online that's willing to

help okay I'll hand it over to you okay let's start by importing our

data we'll just call it data and we'll get it from the data file I can get rid

of my challenge text and I'm not sure if I've explicitly covered this or not but

I'm going to be doing the mapping inside of the body of my function but before my

return it probably would have worked out just fine if you had done it outside of the component but common practice is to

do this as part of the body of the functions let's go ahead and start right here by creating a new variable let's

call it entry elements since this will represent an array of J X elements and

I'll set it equal to data. map so map again will return a new array and we

want to use our callback function inside here stub that out and for every one of

the entries we'll just say it's a single entry we want to return some jsx so we'll return and I'm going to wrap this

in a set of parentheses just so I can start this on its own line we'll go ahead and return an instance of my entry

component and we can start taking the data from the entry and putting it into our entry component our image is going

to equal I'm going to use a set of curly braces because I have entry. IMG and oh

no see I almost made the same mistake we are actually passing an object into our image so I want to pass an object

remember the first set of curly braces puts me into JavaScript and the second set represents an object and I need to

pass in a source so my source is going to be let's see entry that's this entry

object. image. SRC okay great and then we have an ALT which we will set to

entry. image. alt now this is clearly the lonand way to do this because our

data does happen to match up we have an image property which is an object with an SRC property and an ALT property I

actually can shorten this quite a bit instead of repeating each of the properties here I can simply say my

image is going to be entry. image so I guess the way that I

was starting it in the first place was actually going to be right this might be a little confusing the entry component

is expecting the image prop to be an object and that object needs to have a source property or an SRC property and

an ALT property and if we go and look at our entry. image let's see right here in

data JS entry. image it is exactly shaped that way it's an object with a source property and an ALT property so

because our data happens to line up with exactly what our entry component is expecting then I can just pass in the

whole object this is actually kind of foreshadowing of something else we're going to see soon okay so I also need to

pass in a title and this is going to be entry. tile we'll do country and I'm

just kind of looking down here to see which properties I need so the country is going to be entry. country the Google

Maps link entry. Google Maps link oh and

I need my curly braces here oh and uh this is not an object these are my props so I need an equal sign okay my dates is

going to equal entry. dates and my text entry. text of course if I hit save

we're still going to be showing just Mount Fuji and that's because I haven't yet replaced this so let's get rid of

this entry component and instead grab our array of jsx elements and stick them

right here so a set of curly braces to go into JavaScript and then we'll Supply our array This Is The Moment of Truth

keep your fingers crossed let's hit save and awesome look at this we have all three of our entries showing up on our

page the images make it clear that we have different data for each one of the components but we can look and see each

one is unique to its own entry data awesome this is some great progress and

actually we've covered a majority of what I want to talk about in this whole section of the course mapping data in

react is one of the most common things you'll find yourself doing and I personally think it's really neat that

react has given us JavaScript primitive ways like the array.map method to

accomplish the repetition of our components while passing in unique data to each one I do have a couple of extra

topics that I want to talk about that's more of a sneak peek into the next section but I do want to give another

soapbox speech that says if this was too big of a struggle for you first of all that's complet completely okay but

second of all it's a good indication that it's time to go back and restudy this ractice it until you feel like you

could do this from scratch if you needed to as I said reach out to the community for help or to Simply post a win that

you were able to finish sort of the MVP of our travel journal app once you've

come down from this high of accomplishing such a great task we'll keep moving

forward the coolest part about the way that we've set this up in react is that the dis play is a function of the data

that we're pulling into our app this just means that if we were to come to our data JS file and let's say just copy

and paste these last three items I can hit save only changing the data and we

come to our app and check it out we actually have those extra components showing up on our screen of course as

I've said usually we'd be pulling this data in from an API but that's beside the point at this time we'll be getting

there soon let me undo this so we don't have so many of the gang hope I'm saying

that right and let's hit save so we just have our three items there again now we notice that when we're hitting save

we're getting this warning in the console and it says that each child in a list should have a unique key prop and

it even tells us where we're rendering that list and this is a common warning that you'll likely come across many

times when you're writing react code anytime you take an array of data and turn it into an array of components or

an array of react elements react has an interesting system under the hood that it uses to keep track of what order

everything is in when you give it an array of react elements it's a little bit outside the scope of this course to

really discuss why but from a really high level overview if you were to ever include functionality where the user

could add new items to this list or maybe remove one of the items from the list react needs this unique key prop

that it talks about in order to keep track of which one you're actually removing or where you're adding new

elements again it's a bit outside the scope to get into the nitty-gritty of why but it's really easy to implement

because all we need to do is pass a unique prop called key and it actually

has to be KY I know we've talked about how we get to choose the names of our props well this is an exception it has

to be key and the value that we pass to it has to be unique so I can't pass for example a hardcoded one to it because

then every one of them would have the same number and you can see the warning says they encountered two children in

this case it probably should say three children with the same key one well a really common thing for us to do

especially when we're getting data from a database is that data or that array of data will usually have an ID attribute

associated with it and this is actually managed by the database it ensures that these IDs will be unique across the

entire collection in that database or the entire table of that database and so

if your data does have an ID in my case I just typed them in manually then this

is the the first place to start when it comes to providing a unique key so I can just say entry. ID hit save and our

warning goes away of course in our case because we only have three entries I could have used pretty much anything

here the title dates text link to Google Maps the country these are all unique

across these three but of course if I were to visit another place in Japan and have another entry for Japan then that

clearly is not a good key to use because it would be repeated over multiple elements in array whenever you can just

stick with IDs while I'm talking about that if you do happen to have an array that doesn't have an ID something I

often will see beginners do is they will access the index which is something that

map provides to your callback function if you need it and then trying to use that index in place of having an actual

unique property about your data and I'll be completely honest with you this is recommended against but if I hit save

you can see I'm not getting any kind of warning in my case because I'm not going to be adding or removing any of these

elements at least not from the UI itself the index will kind of get the job done

in a pinch but generally speaking if you can avoid it just don't use the index as your key I'm actually pretty sure

there's an entire article on the react talks that talk about this or at least a section somewhere so in a pinch it will

work but whenever you can use an ID instead okay all the warnings gone our app is looking good there's just a few

miscellaneous topics that I want to make sure I cover while we're still on the topic of props so that's what we'll be

doing over the next couple scrims one thing you might have noticed

especially if you were typing this all out from scratch is that the amount of properties that we're passing to our

entry component it's getting a little bit lengthy and I'm sure you can imagine if we were to have a lot more data

included in each one of these objects imagine an object that has something like 20 or 30 or more properties to it

it would become way too cumbersome to try and add a new prop for every single one of the properties in that object one

way that we can make this a little bit more concise is by noticing that what we're doing here is creating a prop for

image for example and passing entry. image title entry. tile country entry.

country well it sounds like our entry is interested in every property of the

entry object object that we're passing to it which means instead of passing down every property of our entry as a

separate prop what I could do is just create an entry prop and pass the entire

object down notice that I do need to keep my key here this is something that's specific to react as we talked

about so even though I am passing a part of my entry down I need to tell react

that it's got a unique key that it can grab on entry. ID but the rest of the entry object I can pass as a single Le

prop called entry in my case of course I got to choose this name I could have said something like obj for object or

just the word object but let's keep it as entry of course because I'm changing the props that I'm sending down if I hit

save sure enough everything is broken gosh we're not even displaying a single thing I thought at least some broken

links would show up here so let's go over to entry and have ourselves a little challenge there it is your

challenge is to fix our component I am intentionally being a bit vague here because I want you to think critically

and use this as an opportunity to gauge your understanding of props what's being passed down as props and how we can make

changes to the code of our components so that everything starts working again I believe in you I know you've got this

I'll hand it over to you to work on this

challenge well if we open our console and something that can be helpful on scrimba is to open your actual browser

developer tools console on a Mac I can hit command option J and it will open those directly but I can see down here

in the console it says that it cannot read properties of undefined reading source and that makes sense because

before we were receiving an IMG prop which was an object that had a source property but we're no longer receiving

IMG which means this is undefined and we get an error trying to read the do Source property on top of the undefined

value in JavaScript if I want to temporarily bypass this error I can use optional chaining and I think this will

yeah so this shows some elements at least showing up on my screen we can clearly see that things are broken so

this will give me a chance to console log the props which is always a good place to start when you're debugging

something okay and sure enough if we look really closely it's a bit of a mess when it's all in line but we can see

that we're receiving a single property called entry and that entry prop has a value of an object where all of the

other data is being stored which means all I really need to do is everywhere I have props dot go ahead and select

everything on the page all I need to do is add an entry in front of that and

then access the properties of that entry as it's nested inside let's clean up this console log I'm actually going to

remove my optional chaining there and we'll go ahead and hit save and awesome we're working again now although

everything is working I think it's helpful to notice at this point that the reason we're magically working is

because the data that we have inside of our data array match mates exactly in

terms of the language or the property names that we're using matches exactly with what our entry is expecting as a

reminder if we were to change what properties we were passing down then we would have to make a change here to

reflect how the data looks because we're passing this entire object down we're now essentially stuck using the exact

property names that are here sometimes when you're dealing with an API you might have something that isn't truly

conventional JavaScript like you might be pulling in something that says Google Maps link but with snake case instead of

camel case I'll go ahead and hit save and we can see now that Mount Fuji at least in the display we no longer have

an underline under view on Google Maps and that's because the object that we're passing down expects it to say Google

uncore msor link in in our entry we're not doing that let's see where's our

link Source right here we're still using camel casing so just something to keep in mind when you are passing down entire

objects you will be stuck using whatever properties they give you let's go ahead and change this back we can hit save and

now our link is working again so there's certainly trade-offs one really nice thing is that we just have a single prop

here we're passing the entire object down and if you really don't like the way that the data is structured or

rather the way that the property names are set up there are ways that you can rename them just for the sake of your

own code but we won't be worrying too much about that right now all right we are so close to done there is one little

thing that I wanted to show you regarding exactly what we have here it's another relatively concise way that we

can pass down all of the properties of our entry item here and it does look a little bit unique so I wanted to make

sure I covered it just so that you weren't super confused by it if you did see it in the wild so that's what we'll

be touching on next there's one last little syntactic

trick that you can use when you're passing a full object down through props and I wanted to touch on it just in case

you did see it in the wild because the syntax looks a little bit confusing the trick uses the JavaScript object spread

notation but instead of spreading the object itself this is our entry object

that we're pulling from our data instead of spreading the object itself like this what we actually can do is remove our

prop entirely put a set of curly braces and spread in our entry object react

will look at this and it will take all of the individual properties of our entry object and create a new prop that

matches each of the properties of this entry object so essentially it would see that our data has an ID property an

image property a title property and let's just start with those cuz that's all I can remember offand and it would

be essentially like doing exactly what we had before where we say ID equals entry. ID image equals entry. image and

remember image in this case is an object that's totally okay and title equals

entry do title and so on and so forth until it covered every single one of the

properties of our entry object let me put this back to use this new spread syntax that we see here but of course we

just went through changing this so that it passed down an entry object through props and we have props do entry.

everything so if I go ahead and hit save then we can see we're completely broken and I considered having you do a

challenge to do this but I just made you do this work so I'm going to go ahead and do this for you everywhere I have

entry dot I'm just going to multiple select and we'll delete that so essentially this is back to exactly the

way we had it I'll hit save and awesome everything is working again in some ways

this is kind of like The Best of Both Worlds you don't have quite as much clutter here by having to say props do

entry. image. source and so forth throughout the code of this component and on the other side of the equation

over here we get to Simply say curly braces dot dot dot entry so this is more

concise and this is more concise however in certain circumstances I find myself

personally struggling with this method only because it really obscures what data is coming down through this entry

object in my case I have to go all the way to my entry component and console log my props just to see what data is

coming in if I were to make alterations to this like say I had a new property in that entry object that I needed to

display somewhere I'd have to make sure I understood exactly what was coming through I guess it's really not that big

of a deal when I say it out loud but for the sake of this course I'm going to leave this here for this scrim but going

forward I'm likely either going to create a separate prop for each of the data points that I want to pass down or

I'm going to pass down an entire object and just kind of live with the more verbose syntax that we have to have here

on the component side of the equation and all right right folks that marks the end of our travel Journal I'm sure

there's lots of improvements that you could make to it I would love to see them if you want to make your own design

changes or more interestingly I'd love to see what places you have visited fortunately all you have to do is go to

data.js because of the way we structured this and make changes directly to the data hit save and your own information

will show up here head over to the Discord post a screenshot of some of the cool places that you visited or if you

don't feel like going in that depth just post a screenshot of your progress here with the travel journal the scrimba

Discord Community is one of the most welcoming places ever the last thing we have to do is do a quick recap of

everything that we've learned throughout this section and if you're a scrimba pro member we'll be giving you a solo project that you can work on that will

be in a similar scope to what we've worked on in our section project with the travel journal and will give you an

opportunity to really test and push yourself to see if you're able to recreate something similar to this from

scratch if you're not yet a scrimba pro member I highly recommend testing in it out and trying one of these solo

projects because they make all the difference in not only this react course but the scrimba frontend career path in

general what a great job you've done on the Travel Journal project I hope that it's been an inspiration to you to get

out there and do a little bit more traveling too what we've learned in this section has enabled us to build some

pretty cool stuff we started out by talking about why reusability is important in the first first place we

saw that probably most of the websites that we visit have some component of reusability that is driven by its data

as opposed to just being hardcoded by a developer somewhere there will likely always be static portions of whatever

web page you'll build but more often than not you will find yourself using data to drive the content of your

website or your web app and we learned in react a primary way of being able to

reuse our components is by providing props just like how functions have parameters that give that function the

ability to be reused with any kind of data that's passed to it props give react components that same power and we

learned how react can render an array of components which allowed us to create an

array of components from a raw array of data in our case we had our data just

directly in our project but more often than not you would find yourself calling out to some kind of API to get that data

map it and then display that data to the page this marks a giant step forward in

our understanding of react and also the level of cool projects that we can build with it so this would be a perfect time

to head over to the scrimba Discord community and post your accomplishment in the today I did Channel go there to

celebrate your own wins as well as congratulate others on the wins that they've been having recently

too once you've had a chance to do that this might be a good time to take a break because what's coming up is a

really meaty section the topics we are about to cover will really step up your

react game and Empower you to create truly amazing interactive web apps with

react once you've had a chance to celebrate your wins and rest your brain a little bit we'll Dive Right into that

in the next

section you have done an amazing job so far in this course and now we are finally approaching probably the most

exciting section in this course which is building interactive web apps in react I am so excited because this

section really unlocks a huge section of react that allows us to create really

Dynamic exciting web applications what we've been working on so far is First Learning the fundamental

building blocks of react by building static websites this was really important for us because we needed to

learn the syntax of creating our own components and generally of course how to spin up a react app from

scratch how react is even working behind the scenes and what its main philosophy

is then we moved on to how we could build reusable components we learned about props and how we can pass data

into those components this allowed us to use static data to generate portions of our web page which is what set up the

foundation for what we are about to learn and I've done my best to make these sections really exciting and

hopefully you weren't like our grumpy friend Stanley here bored out of your mind while learning these

topics now the Crux of what we are about to start learning lies in understanding

the difference between static web pages and dynamic web apps we've been mostly

working with static web pages in react so far and you can tell something is a static web page based on the fact that

it is usually readon in other words there's no user-driven changes to the data behind the

scenes some really common examples that come to mind of this are blogs

when I'm visiting a Blog I'm usually just consuming or reading the content on the blog now there might be tiny

interactive elements on most blogs these days but I think you get the idea that's not the portion of the site I'm talking

about the same goes for news sites it's presented to us we consume the information in a readon way but we're

not updating the news that's written on the news site recipes are another good

example of this and I'm sure we could come up with many more we are totally capable of building the

front ends of these kinds of websites in react however what we are about to venture into is understanding how we can

build Dynamic web apps in react you could classify something as a dynamic web app when it has read and

right capabilities or the user has ability to change the data as such these kinds of dynamic web

apps tend to be highly interactive typically these kinds of apps will have portions of the site that

will display your data specific to you as the user of this app some examples that come to mind are

a bank website you log into your bank website it displays your information your account balances allows you to

transfer actual money or at least the ones in zeros that represent money and so

forth also pretty much any SAS product or service like Airbnb there's portions

of their site that will display static information to you like a list of properties but you have the ability to

filter through them and organize them by Price or rating you can click into them and maybe most interactively you can

book the Airbnb and pay for it this kind of leads into a whole section of sites

that are e-commerce sites the ability to add items to your cart and purchase it

with your money are telltale signs of a dynamic web app and these days I'm sure if you were

to look around you would find probably hundreds of different web apps that you have signed up for and at least used in

the past to guide our curriculum through this section we are going to be making a

really exciting web app called Chef Claude Chef Claw is a recipe app where

you will input a list of ingredients that you have on hand and at the click of a button send that list of

ingredients off to an AI API to generate a recipe for you based on your

ingredients and this project is actually going to have two options for different AIS you can use one using claw AI

through the anthropic API and another using mistal AI which we will access

through the hugging face API boy that was a lot of acronyms this project is super exciting

it's actually something I find myself using and it's going to help us really grasp all of the concepts from this

section in creating Dynamic web apps with react so without further Ado let's

dive in and start learning

sometimes when I'm starting a new project that might feel a little bit overwhelming I try to find parts of the project that I already do know how to

build up until now we've only been building static pages in react and the truth is that there are parts of this

app that are completely static so I'm going to give you a challenge Now to create this header section it's mostly

just meant as I guess both a continuation of the previous section to make sure we're still practicing and as

a way just to warm us up for learning all about how we can make this app a really nice interactive app by the end

of the section so your challenge is to start by building the header components you're going to do it in a separate file

and then render it here in the app component if you click on the screenshot here it will take you to the figma

design file and there's a couple things that I'm setting you up with just because it's a little more tricky first

of all I've already included the chef CLA icon.png file that's the little robot with the chef's hat here in the

logo so inside of your header component you can import that as we've seen with handling static assets you can import it

and then render it as the source for this image element in the CSS I've also put a little bit of starter CSS here

maybe most interestingly I've set the font family to enter already which is being imported in our HTML file so you

don't have to worry too much about going to Google fonts and grabbing that also figma has recently changed where it has

obscured a little bit some of the CSS rules that you might need and one that I found a little bit challenging was the

Box shadow that it has underneath the header right here there's a tiny little box shadow that helps separate it from

the rest of the body and although it's a small detail it actually makes a pretty big visual difference and so the code

for it is right here just feel free to copy and paste this into the box Shadow of Your header also keep in mind the

design on figma it is a little bit more optimized for a bit of a wider screen if

you want you can follow exactly the sizing and just pull your mini browser a bit wider or there's the feature where

you can maximize it it to show up bigger inside of this scribo window either way is totally fine if you do decide to keep

this a little bit on the smaller side which is what I'm going to do I'm probably going to change a couple of the

values that are in figma just to make it fit better on the mini browser the changes are minor it's not that

important to our learning so feel free to do it however makes the most sense for you okay it's your time to shine go

ahead and get started on building the header component okay I'm going to work a

little bit backwards and pretend that we have already built a header component that I can import and render here so

let's go ahead and let's see we'll just call it header. jsx it'll be its own file in the same folder as the app

component because we have a relatively small scoped project I'm not going to worry at this point about creating a

separate components folder or making a really deeply nested structure in our project so we'll just keep it like this

if we need to we can always refactor later and then right here I'll go ahead and render

my Capital H header component and I'm not going to hit save cuz we'll crash cuz this doesn't exist yet so let's

create that file header Capital H header. jsx and there it is we'll create

our function we'll export default function header and we'll do a little

sanity check here we'll say we have an H1 that will return that just says

header component here hit save and sure enough it's showing up awesome let's get

the content on the page and then we'll worry about styling it so I am going to

use a semantic HTML header element and we have a very simple header often with

real businesses just to make sure everything stays exactly as their brand needs it to be the logo or the icon and

the text will all actually just be a single image in my case what we have exported is just this little chef logo

so we will need to put some text there so we'll render an image and we'll

render I guess we can call it an H1 it's kind of like the site header again usually this is part of an image so

that's not what we would dedicate our H1 to but I think we'll be okay so we'll say this is Chef cloud and the source is

going to be equal to the icon I could in scrimba give a path to the icon and say/

images SL Chef cloud icon.png and I think that should work

yep there's our Icon better practice though as we've discussed is to import any static assets so I'm going to grab

let's see this text here we'll import it and call it the chef CLA logo and we'll

import it from that icon or that path to the PNG and put Chef Cloud logo here it

should be exactly the same yes perfect we have the content let's do some styling I'm going to access my header

we'll give it a display of flex we'll justify everything to the center I guess

in both directions so we'll align items to the center as well the design shows that there's about an 11 pixel gap

between the icon and the text we're going to make this icon smaller in just a second see I'm having trouble seeing

exactly what the header and the body is let me just temporarily give this a crazy background color we'll say the

background color is red okay that's pretty good the height seems a little

bit large to me it looks like in the design it's set to 108 pixels oh that's

even larger let's go ahead and uh use our discretion to change this to something different 80 pixels seems a

little more reasonable and then we can go ahead and fix our image and oh let's grab this box Shadow code while we're

here and stick it there change the background color away from Red we'll get rid of that line I think I'll look ahead

a little bit and change the background color of my body to the background color

that is in the design and wow that is very subtle oh it looks like it also is

coloring the header so we'll need to specify that this needs to stay white so this will be a background color of white

and yeah that's working perfect okay let's get access to our image uh because

I'm only going to have one header and it's only going to have one image I'll just select those directly as a

descendant or I'll select the image as a descendant of the header I think that won't be a problem but we can always

classes if we need a little more specificity the width on this I think it says it's 40 something let's see what it

looks like as a 50 pixel width that looks pretty manageable yeah let's go ahead and stick with 50 for now and then

I will do the same selecting my H1 inside my header okay in the design it

has the font size set to 32 pixels which is two rim and I think that might be the

default size for an H1 so I don't think I actually need that let's try the font weight it shows us

400 and yes that does make a difference and it looks a little more Sleek being not quite as bold so let's keep it like

that sometimes we get issues with default margins but it looks like that's

not causing a problem here so I don't even need to say margin zero we've already got the font family set to enter

let's comment this out and make sure that's working it's subtle but it's working so I guess that's it we've got

our header all set up I know it's a lot to spend this much time doing CSS in the middle of a course on react I really do

try my best to integrate some of the past lessons that you've had especially here on scrimba if you're taking the

friend and developer career path just so things don't get stale you know what I mean it's better to practice it now even

though it's not technically what we're learning and as I've mentioned before you do have my permission to skip some

of the CSS that we do if it's something you already feel completely familiar and comfortable with okay so we finished

this top section and although we are going to add some interactivity to our tiny little form here the structure of

the form just being an input and a button as well as the looks of it can be started as static so we're going to do

that next before we move on to more of the meat of the

section when our users first come to the chef Cloud app they're just going to see

the header and this little form here we might decide to add a little blurb that explains what this app is supposed to do

but for now the only other static thing that we need to really worry about is creating this form it will of course

have some interactivity with it and we're going to learn all about how we can deal with forms in react a bit later

in this section but for now let's go ahead and get this form added now I have made you do a lot of this manual work I

know that it's just repetitive CSS work mostly and so I'm going to give you a little treat I'm going to work through

this I will keep it here in the recording and it will be the remainder of this lesson so if you're interested to see how I create and Design This

little form then by all means stick around if you're ready to move on from the static stuff we about to jump into

some really exciting things so that can be what you do next so you're welcome to skip ahead to that if you want I'm going

to get started first let's see let's head to our app and underneath our header I'm going to include another

component called main now I need to wrap this in something because we can't render to Sibling elements like that in

react I need to import main from Main

and then of course I need to create that so we'll create a new file called main. jsx

and spin up our component as I usually like to do I'll just return something simple to make sure things are hooked up

okay great we're showing main component there the content that we're concerned about at this point is very simple we

are going to probably be doing most of our markup here inside of the main component but for now we can just create

our form and so first because this is the main section of our app we're going

to surround it in the semantic main element and and then we'll add a form I

know this is just a simple single input and a button but even stuff like this I much prefer to put in a form first of

all it's more semantically correct we are creating a form here it makes it better for assisted Technologies to

understand what's going on we also get some built-in functionality when we put it inside of a form for example when a

user fills the input out and then hits the enter button it will automatically submit the form it will have access to

the form data if we need it and it's just a whole host of benefit s by using an actual HTML form okay so in the

design we just have an input and a button typically for accessibility

reasons we would want to make sure we also include a label or another option that we can do is to add an ARA

attribute to our input that's called ARA label and so I'll set that equal to add

ingredient so that anybody using a screen reader can very easily understand what they're supposed to do with this

input okay let's put this on its own line because we're going to add some extra properties here we want this to be a

type of text we'll give it a placeholder just like we saw in the design we can

say something like for example oregano as a reminder a placeholder is a great place to put an example of what should

be entered as text into that field and it isn't a great place to put the actual label so I wouldn't want to say

something like add ingredient as my placeholder okay by default forms are are pretty ugly so let's hit refresh and

yeah oh our button has no text we might want to say add ingredient there okay let's see what we're working with

perfect well not quite perfect yet let's go ahead and style it up chances are I'm

not going to be adding any more forms to this page so I could just select the form element but I'm not sure why I'm

feeling like I probably want to give this a class name so I'm going to give it a class name of add ingredient form

okay I'll hit save so that applies we'll go over to the CSS and start styling this let's access our add ingredient

form and I'm going to add a display of flex even though we do already have inline elements just so that it makes it

a bit easier for me to Center things so I can justify content Center We'll add a

gap of about 12 pixels I think the design shows and it's sitting right against the header so let me also add

some padding to the main element we'll give it maybe 10 on the top and bottom and 30 on the left and right and I guess

I need to specify padding and oh when I did that I see that my elements are stretching now that's a default with

display Flex so if I were to instead say align item Center that should fix that

issue of course our button is a little large you know what I'm going to cheat and just make this a little bit wider I

should probably add some kind of no wrap rule to the button but for now I'm not going to worry about it okay let's

access our input I'm going to grab the style for my form and then specify the

input on it and let's give it some border radius of about six pixels the

default border is a little bit crazy so we will add our own border styles of one

pixel solid and then I'm just going to grab this color from the design okay

that looks much better the padding is a bit tight there so we'll add a padding of about 9 pixels on the top and bottom

and 13 on the left and right awesome looking good I'm going to make this a little bit wider so add ingredient doesn't wrap again the design does have

a little bit of a box Shadow around it so I'm just going to paste that in from my Dev mode inigma which you likely

don't have access to for this design and then one thing I noticed from the design is the input does get pretty wide as the

screen gets wider so I do want it to grow I can use the flex grow property we'll just set it to one so that as the

screen expands it does get wider although I do think I want to add a minimum and a maximum cuz it can get a

little bit squishy right down there and a little bit too wide way out here so let's give this a minwidth of let's say

150 pixels and a Max width of maybe about 400 pixels so as we get wider it

should stop growing yeah perfect okay the input is looking pretty good let's go ahead and style our button and then

we can move on so we'll access the button and for whatever reason I'm sure there's a good reason for it but buttons

do not take on the font family that's specified elsewhere even if you specify it in the body here so I'm going to make

sure I specify the inter font family for our button we'll also give it a border

radius of 6 pixels just like our input the border is looking a bit intense so I

think for now I'm just going to say border none on the button let's give it a background color and this is a color

specified in the design of course the text is now impossible to read so we will specify the font color with the

color rule all right that's looking a little better and H the button is pretty squatty I could try to add padding to it

although I don't really want to add padding and try to guess to make it the exact same height as my input uh maybe

what we can do is take away the Align item Center and well actually that just

kind of makes it work that just makes it look better it's using the default of stretch as it's align items and that

actually looks pretty good I'm not sure that this will make much of a difference but I'm going to specify a height on my

whole form the design looks like the input is 38 pixels tall so we'll just add that it doesn't look like it's

making a change but maybe any other structural changes that we make that height might be good or maybe it'll be

bad and we get rid of it for now let's leave it in now the design does show a plus before the add ingredient and it

looks like our button is quite a bit wider now the design does show this little plus icon on the button button

before the add ingredient and I could just go in and type that into the markup

but it feels almost decorative to me so I think what I'm going to do instead is use a before pseudo selector and just

say that the content is a plus and then maybe give it a little bit of margin right just to separate it a little bit

and I need my semicolon here okay that's looking good all right with this behind us let's keep moving forward and start

jumping into the meat of the section and actually our button is still looking a little bit squished so let's see if

maybe we give it a width of 150 pixels I think the design shows quite a bit more

oh and I think the font size is a little bit smaller the font size looks like it's set to 14 pixels which comes out to

0.875 Rim and oh yeah that makes a big difference it also looks from the design

that the font weight might be adjusted looks like it's set to 500 let's see if

that's making a difference oh it's a very slight difference but we'll go ahead and leave it in oh and one last

thing I'm noticing that our form is shoved up pretty close to our header it looks like in the design there's about a

70 pixel space between those I think that's going to be a little bit large for such a small site here so I'm going

to call an audible and let's see our padding on our main element is 10 on the

top and bottom 30 on the left and right I'm going to go ahead and specify

let's see 10 pixels for the bottom and then change this to yeah let's say 30 pixels on the top this is a little bit

less common if you have just three values then it's top left and right and bottom kind of a weird way I'm honestly

not sure how I remember that but it's working great okay we're done with the static portions of our page we have a

lot to dive into still I think a really good idea is for us to take a step back and get a highle overview of the project

and make sure that we understand and how we're going to go about building it that'll be something we do really quickly in the next

scrim other than just building the static parts of your page it's a really good idea when you're starting a new

project like this to try and take a step back and think about how you would approach solving the problem assuming

you're fairly new to react that might not be entirely possible at this point because you still have quite a bit left

to learn but I thought it would be helpful for us to get a highle overview of how we're going to approach building

this project when the user First shows up as I've mentioned they will simply see our header and a little form like

this where they can start adding ingredients once they start adding ingredients we're going to change the layout of the page a little bit we'll

include this header that says ingredients on hand we're going to map over the array of ingredients that

they've entered into the form and we're going to have a call to action down here where they can click this get a recipe

button this is where things get pretty fun clicking the get a recipe button will send the list of ingredients

embedded in a prompt that we send to the Claude API from anthropic CLA is an

extremely capable text completion AI that will take the prompt we send to it which will include the list of

ingredients and it's going to generate a recipe now on this next screen I had to split it because we're going to be

scrolling up and down the page but you can see it will have a suggested recipe it's going to have a basic text at the

top that tells you what it recommends that you make and then it will have a formatted list of ingredients and a

formatted list of instructions the way we're going to handle this formatting is fairly simple but it's not something we

have to be too concerned about right now now there's still a lot left we have yet to learn so don't let all of this feel

like it's too overwhelming I promise we're going to take it one step at a time and by the end of this section you

are going to be able to complete this entire project from scratch if you needed to all right I'm too excited to wait any longer let's jump

in the primary thing that sets apart a static website from a web application is

the user's ability to interact with the things that they see on the screen and one of the primary ways that we do that

is by listening for events so let's talk about how we can add event listeners to our components in react first of all

based on the prerequisites for this course I expect that you already are familiar with the concept of adding an

event listener in regular Dom JavaScript where you would select some elements and

you would use the addevent listener method this method takes two parameters

the first one is the type of event that you want to listen for like a click event and the second is a function that

should run should the click event ever happen on this specific element another way that you can add event listeners to

elements is directly from the HTML if for example I wanted to well let's say

we have a button here and it'll just say trigger event inside the HTML I can add

an attribute to my button called onclick all lowercase like this and set it equal to the string

of a function that exists in my JavaScript file maybe called handle click and I use a set of parentheses

here to indicate that I want to run that function when the onclick is triggered or rather when the click event happens

and although I seem to find this HTML method of adding event listeners a little more rare than using the add

event listener method in JavaScript the way that we're going to do this in react is actually more similar to the way that

we see it here the syntax is very similar to how we do it in HTML so let's go to our JavaScript I'll get rid of

this line here and the way that we can add an event listener is one of the properties that we passed to this button

so I can add an onclick but this time I'm going to use a capital c as a reminder sometimes it's easy to forget

that we're actually inside of a Javascript file even though what we're writing looks a lot like HTML and this

jsx code that we have will be converted into a regular JavaScript object that JavaScript object will then by react be

turned into an actual Dom node that displays on the page but because we're here in jsx any of the attributes that

we add to our react elements are going to be accessing the actual Dom nodes attributes or properties and in

JavaScript that accesses the document object model it does use camel casing like this that's the same reason that

we're using class name because class name is the actual Dom node property now

because we are here in JavaScript I don't need to set this equal to a string of a function that I'm trying to run

instead I can set it to the actual JavaScript expression that I want to run which means if I want to I can just

stick a function right here in line and whatever I'm going to run here let's say

console log clicked the body of this function will run anytime a click event happens on this button let me hit save

and oh we have our trigger event button let's go ahead and get rid of this okay so if I hit click me then we get the

JavaScript that we put inside of our function actually running on the click event now I don't person Al love to put

my functions right here in line sometimes I'll find myself doing it more often than not I will create a function

outside at the top level of my component above the return and so I might have

something like function handle click and we'll go ahead and just put our console log back and this leads us to our first

challenge your challenge is to add the new function that we just created handle click to the button go ahead and give

this one a shot now some of you might have been a little

bit tricked by adding handle click followed by a set of parentheses I had mentioned that this is the way that we

do it inside of our HTML however because we're here in JavaScript if I include this set of parentheses it's going to

run this function as soon as the component loads or is rendered let me go ahead and hit save and watch the bottom

of your screen for the console and you'll see it immediately ran I was clicked even though I didn't actually

click the button we don't want to include the set of parentheses here because that does indicate that we want

to run the function immediately as opposed to passing the contents of the function or the functionality of the

function to the button element so that it will only run when the click event is triggered so I'll go ahead and hit save

and now it will run I was clicked when I click the click me button awesome before

I get too much further I do want to point you towards the documentation on responding to events click the

screenshot if you want to head to the react documentation for this and I also included a slide that leads you to the

mouse event handler functions which give you an example of different Mouse events that you can respond to in react and

this documentation is going to be helpful for you for the next challenge all right your next challenge is to log

something to the console whenever the mouse hovers over the image now because we're hovering it's not going to be the

click event which is why I gave you the documentation here feel free to go check that out and with that I'll pass it over

to you to finish this challenge in that documentation we can

see that there is an event called on Mouse over and there's also on Mouse enter either of these would have worked

just fine for this challenge let's clean up this challenge text so we declutter a little bit and I'll go ahead first and

create my function here we'll say handle Mouse over and then on my image I can

add an on Mouse capital M over capital O equals and then my function of handle

Mouse over let's have this console log I was hovering

let's hit save and cross our fingers and sure enough when we hover over the image we get I was hovered we can do that

really fast and get lots of console logs awesome it can be kind of fun to check out all the different events that you're

able to respond to I think a lot of them you likely haven't even heard of and could probably find some really cool

ways to use them so feel free to poke around the documentation for the different Handler functions this site

will take you to the section on mouse event handlers but if you were to scroll up or down you would see other ones like

touch event handlers and pointer event handlers keyboard event handlers and so forth so lots of really cool stuff there

hopefully this is fairly straightforward enough we're going to be doing a lot of event handling it's one of the cruxes of

having a web application over just something that's purely static so lots of really fun things coming

up as we just discussed when our users first come to our app they're going to be presented with a pretty simplistic UI

and their task is to type in an ingredient and click add ingredient when they start adding ingredients they're

going to be presented with a new section of the site which will list the ingredients that they've entered out for

them if you think critically back on what we learned in the last section you might recognize that what essentially

we're going to be doing is adding the ingredients that the user is submitting through this form to an array and then

we'll be mapping over that array to display a list item for every item in the array so with that in mind I've set

up a bit of a review challenge I created an array of ingredients and I want you to as part of your challenge map over

this list of ingredients and then render them as list items I've added a little unordered list it's going to be

completely unstyled but you can render your array of list items right here as a quick note if you are already a little

bit familiar with react you will recognize that we're doing this in a weird way I wanted to point that out now

so nobody got confused as to why I was teaching it this way by the end of this lesson we're going to see the limitation

we have but for now don't worry about that and I'll hand it over to you to work on this review

challenge I will go ahead and create a new variable let's call it maybe ingredients list maybe ingredients list

items just to be really explicit and we'll set that equal to the array that

comes back by calling ingredients. map for each ingredient which is just going

to be a bare string I will return and I'm going to use a set of parentheses here so I can take advantage of the

implicit return with with arrow functions I'm going to return a list item and I can just put the ingredient

directly inside there because it's just a string for now I am going to add my key cuz I know I'm going to get a

warning so I'll make sure to add the ingredient later when we actually do this we will figure out a way to make

sure that ingredients are unique in our array okay so I'll take my ingredients list items and render them right here

like it told me to do let's hit save and awesome our ingredients are showing up

let's clean this up well we just learned about event listeners so I have another challenge for you I'm throwing a little

bit of a curveball here because in the last lesson we only really practiced with mouse events the on Mouse over and

the onclick events but between me giving you the exact event handler name and

exactly where to put it on the form I think you'll be able to figure this one out so your task is to add an onsubmit

to the form element and have the function which you can Define right here simply console log form submitted for

now all right let's get cracken I'll go ahead and create the

function first we'll call it the handle submit function it's going to console

log form submitted and I can add the onsubmit Handler to my form and we'll

set it equal to handle submit this is tangential but you might be asking why are we doing a handle submit on the form

instead of a handle click on the button I'd say there's at least a couple reasons primarily it feels more semantic

we're submitting a form we've created an actual form element and clicking the button will submit the form so what we

should be doing is handling the submission of the form maybe more importantly if a user hits enter in the

input well that's not going to trigger a button click event however it will trigger a form on submit event and so

for free we essentially get the capability to type into the input and hit return or enter without having to

handle a separate vent on the input we haven't really done anything to handle the text that's in here so it doesn't

matter what's there I'll go ahead and click well I have to save first I'll type in here I'll click add ingredient

and awesome we get form submitted we also can type in here and hit enter and sure enough we get form submitted now

later on in this section we are going to do a much deeper dive on forms so there's going to be a couple things that

I add to my handle submit I'll explain them briefly but especially if you're not familiar with how forms native work

on the web I'm really not expecting you to memorize this stuff right now for now let's start by cleaning up this

challenge text to buy ourselves some room and the first thing that I actually forgot to put on my input is a name

property whenever we're submitting a form our inputs all need to have a name we'll see why in just a second but I'm

going to call this ingredient secondly when I submitted my form you might have noticed that the form actually refreshed

the page and now that we have a name on our input we we can actually see a URL

change if I were to say I don't know a cumin I'll hit enter and sure enough the

page refreshed and if you look up in the little mini browser URL you'll see that it says question mark ingredient equals

cumin this has to do with the way that forms natively submit on the web however in our modern framework of react we

actually don't currently want this page to do a full refresh and so I can prevent that from happening by grabbing

the event that is passed to my handle submit function and and calling

event.prevent default let me hit save and put this back to just a slash we'll

go ahead and I can just say testing and hit enter and awesome our form didn't refresh our URL didn't change and we did

get our form submitted running awesome okay in order for us to do the next challenge which is hopefully going to

drive home the point that I'm trying to make in this lesson I'm going to do a little bit of hand waving coding again

if you're not familiar with this and it doesn't make sense it's completely okay please don't be too concerned about it

my goal is to have you do a challenge where you take the ingredient that was typed into the input and try to add it

to the ingredients list in order to grab the ingredient that was entered into the input I need to grab the form data that

was submitted with the form that was submitted in order to grab the text of

the ingredient that the user put into the input box and submitted with the form I need to grab that through form

data I can grab that form data on the form itself and I can access the form

Dom element itself through the event that was run when the handle submit function runs so I can get the form data

by creating a new instance of form data and passing the event. current Target

then I can get the ingredient so the let's call it the new ingredient by

calling form data doget and then passing in the name which is ingredient this is

the name of the input from my form let's go ahead and just console log new

ingredient we'll hit save I'll type testing hit enter and check it out we

got our form submitted of course we can actually probably get rid of that console log and we got our new ingredient which is testing that's

pretty boring let's add I don't know what's a more exciting ingredient let's say jalapenos oh come on we can get an NA in

there let's do that perfect okay jalapenos again this wasn't intended to

be something that we actually learned in this lesson so I went through it really quickly please don't be too concerned

about it but do be concerned with your upcoming challenge okay this is the challenge that is really going to drive

home the message that I'm trying to get to in this lesson we have access to our new ingredient instead of console

logging it I want you to add it to our array of ingredients after you've done that I want you to add a console log of

your ingredients because spoiler alert what we might be hoping would happen which is to have the page update with

the new item that they added it's not going to work now this hint says that it's a on liner solution so don't

overthink it I guess technically it's two lines because I'm also asking you to console log the ingredients okay let's

get your hands on the keyboard again and work on this challenge okay so inside of our handle

submit we might be thinking well I can just push to the ingredients array the

new ingredient we'll go ahead and as asked console log the ingredients array

and let's hit save we'll put in our jalapenos add ingredient let's look at

what we got and sure enough it got added to the list however and maybe this was a

really really roundabout way to make this point we clearly have not updated our page in a more imperative system

like if we were not using react and just building the site with regular JavaScript accessing the Dom properties

we commonly would find ourselves pushing a new ingredient to the list of ingredients and then either manually

adding a new Dom element to our unordered list or running some kind of function that does this operation Maps

over the new updated ingredients list and pushes all of those elements to the Dom however with the declarative nature

of react we don't want to have to do that we want to be able to just update our data or the list of ingredients and

have react recognized that change and reflect it on the page for us so that's

the ultimate goal I know this was kind of long but trust me what we're about to learn is maybe the most important

feature that you will learn as a beginner in react so again this was a very roundabout way to get to this point

but what we're about to learn which is the concept of react state is the key to making all of this work for US state is

one of the most important things that you will learn about react and so I'm using that fact to justify all of the

Hoops that I had you jump through in this lesson so get excited we are finally about to jump into State and

learn how we can harness a major part of the power that react brings to web

development over my years of teaching react I found that one of the major confusions stems from not understanding

fully the difference between props which we have talked about in the last section and state which we are just now learning

about so I want to spend a little bit of extra time understanding the differences between props and state and we'll start

the comparison by talking first about props in react when we talk about props we're referring to the properties that

are being passed down into a component in order for that component to work

correctly similar to how a function receives parameters from above another way you could word It Is by saying that

properties not only are being passed down into a component in order for it to work correctly but almost in a sense in

order to configure that component to work in the way that you want it to work or to display what you want it to

display an important point when it comes to props and something that distinguishes it from state is that a

component that receives props is not allowed to modify those props using a more technical term props are immutable

or unchangeable and when we stop to think about it this makes a lot of sense for example if we have our classic add

to numbers function we came to the conclusion that this function really is

only useful to us if we're able to accept some parameters like numbers A and B this is exactly what we're doing

when we pass props down from above including parameters here of course makes it a much more flexible function

that can do a lot more than just adding two hard-coded numbers like if we were to say return 1 + 2 instead as we've

talked about a number of times of course I would use my parameters instead to make this function a lot more flexible

to use with any number that I might want this is the function definition but the real values are being passed down when I

call add two numbers this is where I might put my one and two in and let's just go ahead and console log the

results here and of course this is going to return to us three however we need to

think of these values as immutable especially when it comes to props and react because as you would expect it

would be pretty strange for me as the first line of my function here to say actually the value that you gave me for

a doesn't matter at all I'm going to set that equal to something completely different and then naturally that's

going to really mess up our function the person using our function add to numbers is going to expect the result to be

three but instead they're going to receive a 44 which makes absolutely no sense so just to be clear don't do this

because the parameters coming in should be immutable similarly in react I wouldn't want to have a function let's

say it's our navbar that receives props and then to have any part of the body of

my component say well I know you gave me a props dot let's say logo icon but then

we say I don't really care what you gave me so I'm going to set this equal to some other icon.png this would be pretty

confusing if we're expecting to receive a prop called logo icon and when we use

this Navar we create an instance of it and we passed down a prop called logo

icon and you know we set it to I don't know I'm kind of stretching here uh

let's say spatula. PNG doing this we're trying to configure our navbar so that

it will use this specific logo icon but the contents of our navbar component are saying I don't care what you had I'm

going to set it equal to what I want it to be equal to so just like above don't do this to be clear this doesn't mean

that whatever component is rendering your navbar couldn't have a value that changes like if you had a button on your

site where the user could click it and it would change the logo in the Navar I'm reaching a little bit with this

example but that would be completely okay changing the value that we're passing down to to our Navar is a very

normal thing in react in the same way that when we're calling add two numbers I might be able to click a button and

change the numbers that are being passed into this function but specifically the props that are coming in or in this case

the parameters that are coming in should not be changed in the body of the component okay I think I might be

beating a dead horse here so let's move on and now we'll talk about how state is different from props in that state is

intended to change so that's what we'll be covering next

if props are referring to the information that's being passed into a component for it to work correctly or as

we mentioned to configure it and if props are not meant to be changed from

within the component that's receiving it State on the other hand refers to any values that are managed by the component

itself kind of similar to any variables that are declared inside of a function I

say kind of similar because there is a difference and we're going to talk about that in just a second but it's important

to note that anytime you have a changing value inside of your component that needs to be saved between renders and

more often than not displayed or used as logic to figure out what needs to be displayed you'll be using something

called state within react so even if the quick description that I gave here doesn't fully make sense to you that's

okay I bet at the end of this section if you were to come back to this lesson it would suddenly start to make sense for

you there's a phrase that you might come across when it comes to understanding State and reac act and that is that the

view or rather the user interface the actual page that you get to see as a user is a function of the state of your

component and there are three main points to consider here first of all is this term called render I've said it a

couple times up until now but you can think of the term render as simply running the function remember all of our

react components are simply functions and we have to return some sort of jsx or user interface from that component

well when react runs into an instance of our component in other words if it sees something like this that looks like an

HTML element it's going to run our in this case app function and that app

function might create some functions within its body it might set a couple variables and usually in the end it will

return some kind of view once react has run this app function it's only going to

run it again if either the props that it's receiving change somehow imagine if

we were passing in a dark mode prop to our app component and maybe it starts

out as true and then a user clicks a little toggle that switches it from dark mode to light mode and then this would

change to false if that prop value changes then react is going to rerun our

app function or in other words it's going to render this app component so that's one time that react will render

or rerun that function is if the props that it's receiving do change from above or it will also render if internally it

has a state value that changes now a state value is different than just a

random variable that you declare within the body of your function you might remember when we had our favorite things

list we had just declared an array of strings and changing that array did not

update the view and that's because that array was not being saved as a state value it was simply saved as a variable

Within the component and don't be confused we really haven't talked much about the syntax behind how to create

state yet so we are going to get there I promise a second key point is that changing a local non-state variable does

not cause react to render the component I guess I kind of hinted at that at the end of Point number one however if you

use a react provided set State function in order to change a state value not

just a local non-state value but an actual State value calling that set State function will update the view it

will rerun the code in the function of your component so that logically leads us to point number three where the view

or what the user sees is simply a function of the state from within your application if State changes then react

needs to rerun or render your component so that something new gets returned and

replaces whatever used to be on the page so you can see that this concept of state is really powerful in react if we

we update our state then react will automatically react to that updated State and it will display a new view it

might not be super apparent on its face but this is a really awesome thing as a web developer because it means that we

don't need to imperatively update the view ourself all we need to do is make sure that the state of our application

or you could kind of think of it as the data of our application is as up to-date

as we want it to be and as long as we do that then react will handle the rest it

will update the view for us it will change whatever parts of the Dom need to change as a reaction to the change in

state and we don't have to do any of that manual Dom manipulation at least for the most part A really simple maybe

overly simple analogy is of a light switch and a light bulb a light switch

represents the state of the I guess electricity in your room if the light switch is turned off there's no

electricity running to It's associated light bulb and therefore the view is well a dark room a light bulb that's off

if you change the state of the light switch by flipping the switch on then the view will automatically update in

other words the light bulb will turn on and the room will be illuminated I think this is about as far as I can go with

just explaining it and so in the next Grim we're going to dive right into the actual syntax and I promise if what we

covered here didn't make perfect sense it's going to clear up as we get to see the syntax of it see see how it affects

react see how it's used within the react ecosystem how Changing State updates the view all of that's going to make a lot

more sense when we get to get our hands on the code and actually practice it so let's Jump Right

In we saw in an earlier lesson that it's not going to work for us to Simply

create new variables here like let's say we have a variable that we're calling State and we set it equal to the string

yes we can use this variable to display what gets shown here so I'll just put

state in its place and we'll see that we do get the value yes and to be totally clear If This Were changeable and then

right below it I were to set it equal to something else like heck yes this

actually probably isn't going to look very good in there this is technically okay I'm not sure why I would do this

but I can hit save and we get heck yes I don't want to say no because of course state is important to know the problem

comes when as a response to a user Interac I try to change the state for

example if I were to add an onclick inside of my button and maybe I have a

function called handle click and all that did was change the state actually

let's have clicking the button change it to heck yes like this and we put handle click down in our unclick let's hit save

and watch what happens I'm going to click yes and check it out nothing happens this is exactly what we saw with

our array of Favorite Things simply change in a local variable is not going to make react rerun our component or in

other words it's not going to make react react to the change of state and display

the updated value that it has instead we have to use a function that's provided by react to save these variables in an

actual State as far as react is concerned this is just a local variable no matter what we decide to call it to

set up a variable that react will place in the view and reender whenever that state changes we need to pull in that

function from react a very common way that you'll see this is to import a

destructured use State Hook from the react library in fact I would bet that

as you're looking at react code out in the wild this is probably going to be how you'll see it the most often however

just to be totally clear that this US state function is coming from the react Library I'm going to import the entire

react Library this is a little less performant when it comes to to tree shaking and not pulling in all the stuff

that you don't need although with modern build tools that doesn't matter but if that makes no sense don't worry about

what I just said but I just want to be clear I'm going to be importing react and then using react. use state in order

to access that function and actually let me clean up some of this extra stuff we'll be adding some of it back but for

now this will just clear up any confusion let's change this because we don't have State anymore we'll change

this back to a hardcoded yes and okay let's be curious and we'll save the

result that comes back from calling react. State and let's just log it to

the console okay interesting what we get back is an array where the first value

is undefined and the second value well scrimba displays it as F parenthesis but it simply means that it's a function

let's see what happens if when I call use State I provide a value let's put a string hello and hit save okay

interesting we get an array back but this time instead of undefined for the first value we get the string hello when

we pass in a value when we're calling react. us state it provides an initial

state so if we know that our component needs to start with the state with a certain value then we can pass it in

here great well before we talk about the second value the function that that's being returned in our result I'm going

to give you a challenge okay this challenge will require you to do some critical thinking your task is to

replace our hardcoded yes right here with some state that you initiate inside of react. state and we don't want it to

say hello we want it to say yes so go ahead and get started on this

challenge the first thing we need to do is not say hello we'll go ahead and say yes and secondly instead of hardcoding

yes here we want to use curly braces so we can evaluate some JavaScript and then currently we're saving this array that

we get back from UST State as this variable result so we'll go ahead and say result but we only care about the

first item of the result array so index zero quick aside for people who are

already familiar with UST State yes we're going to be changing how we're doing this we pretty much never index

into the array that gets back from UST state so don't worry too much about that let's clean up the challenge text

because I'm confident this is going to work and sure enough we get our value yes that is now a state value as opposed

to a local variable value we can test really quick that this is working so if I change this to heck yes and hit save

sure enough our state is correctly displaying there and awesome okay well there's a couple of problems we have

because first of all changing the code like this in order to change the state isn't viable it's not something the user

can do and also this way of doing this is kind of clunky so as I mentioned we're going to learn a better way to

reference our state and give power to the user so that when they interact with the page they can update the state and

therefore change what's in the view so that's what's coming up

next when we call react. usate we're receiving an array in return and as we

mentioned it's a bit clunky to access the index of zero of that array so what

we do more often is leverage array destructuring in JavaScript in order to get back what we actually need in order

to give more meaningful names to what gets returned from our UST State call so let me go ahead and destruct structure

this by putting a set of square brackets around it and since we know that the resultant array has two items I'm going

to put a second item here let's just call it funk for now because we know that it's a function that we're getting

returned now that I'm destructuring this array result is no longer an array which means that I don't need to index into

that array in order to get the value I can simply call result if you're feeling a bit lost when it comes to array D

structuring I would highly recommend taking a pause and doing a quick chat GPT or Google search about array

destructuring to see if you can better grasp what's going on one thing that's nice about this being an array that

we're receiving in return is that we can call this value whatever we want and as

long as I update my code to say whatever we want it's going to work just fine if

what was getting returned by react. usate was an object instead we wouldn't have the same flexibility we would have

to use our curly braces instead of our Square brackets because it's coming back as an object and then we would be forced

to use whatever properties that object had when we're destructuring it so having an array is really useful in that

case because we want to give this a name that is more indicative of the state that we're trying to save so maybe let's

call it something like is important and once again we'll make sure that we update that in everywhere it exists of

course hitting save gives us the same result next let's go ahead and Tackle understanding what this function is and

how it will will play an important role in using State inside of our react

components we've seen a couple times already how we can't just set up a value

like important set it equal to yes and then have some kind of user interaction like a button click that changes the

value manually of important to something else while it will change the value in

memory it's not telling react in any way to reender the page and in fact this is

even true of values that we save in state let's change this to a let so that we can manually change it to something

different we'll say is important equals heck yes and if I hit refresh it will

show heck yes here but it would never react to for example a button click if

we wanted the user to be able to click a button on the page in order to update that state I'm not going to go down that

rabbit hole just take my word for it I can hit refresh and see it says heck yes but adding an on to try and change that

will not update the screen just like we saw it before when we weren't even using State however the function that we get

pasted from react. state if we call this function and provide a new value it will

reender the page it will successfully update State and Trigger reacts to reender the page with the new state

displayed let me hit save so that we don't have heck yes there anymore and let's talk about the conventions for

this function name because just like is important we get to choose what we call this function and there's a really

strong convention where we start the function name with the word set as in we're setting a new value and then you

continue the name from the state variable itself so it would be is important and set is important I'm going

to fix my I here so that it is capitalized just to make sure my camel casing is correct and in order to use

this function I can simply call set is important and provide the new value that

I want and I guess it's already Yes this will be heck yes however I'm not going to hit

save and let me tell you why we talked about how running this function will update the state to the new value and it

will have react render our component rendering our component essentially just means it's going to run the code inside

of our function so I'm going to put a pause here to give you a chance to see if you can think through what would

happen if I were to hit save and react were to render this component

hopefully some of you actually took a chance to hit save and see what would happen I'm going to hit save and we can

see that we get an error that says too many renders react limits the number of renders to prevent an infinite Loop why

do you think an infinite Loop happened well remember when we call this function react is going to update the state and

render rendering means rerunning this code rening this code means calling this

function which then updates the state and renders which updates the state and rerenders and on and on and on so let me

comment this out and we'll get our state app back into a working State and now

I'm going to provide a challenge for you okay this challenge comes in two parts first I want you to create a function

called handle click that runs set is important and let's just give it the value of definitely for now and then

you'll add an event listener to the button so that it runs handle click whenever the button is clicked go ahead

and get started on this challenge okay let's go ahead and create our

function called handle click it's going to call the function that we were

returned from UST State this state setting function sometimes referred to as a set State function we'll go ahead

and call set is important and because I definitely don't want to put no here because state is very important to no so

we'll say definitely then down on my button we'll give it an onclick event handler that calls handle click clear up

our challenge text and we'll hit save and let's see what happens I'll click

this and The Styling is not really working out for us but we can see that the state changed maybe let's go back to

uh heck yes click heck yes and at this point we've hit a bit of a dead end we

were successfully able to call the state Setter function that we got back which we chose to call set is important and in

its simplest form we were able to just provide a new value for state so that when the user clicks the button it

changes to that new value of State renders and displays the new value of State on the page however we're stuck

because we can't get out of heck yes if the user keeps clicking the button obviously we have nothing else to change

to we've manually set it equal to the string HEC yes however just because we're temporarily at a dead end doesn't

mean we can't learning so in the next lesson we're going to get our hands on the keyboard a lot and do a series of challenges to try and help us reinforce

the idea of state and setting State you know this whole section is all

about State and I think it might be useful for us to have a little app where you count how many times I'm going to

say the word state in this entire section but we do have an app that's a little bit more Dynamic than what we

were just seeing and so this will be a good way for us to step by step practice setting up our state and practice

including some event listeners where the user can change that state so the first part of your challenge is to create some

new state that will track our count value where the initial value will be the number zero and don't forget to

replace the hard-coded zero that we currently have with the state that you create as the first part of this challenge okay go ahead and get started

with this to create some new state we will

simply call react. use State we'll set an initial value of zero and what this

returns is an array so we'll go ahead and destructure that array immediately when we receive it first we'll receive

our count and I guess you could call this something like State count but let's just keep it simple and call it

count and the second thing is the setter function that they provide to us so that we can change that state and trigger a

render in react by convention I will use the same name as my state but I'll start

it with the word set so I'll say set count and lastly I can use my new count

variable right here and I'll hit refresh this won't change much for us because we

still don't have any interactivity with our buttons but if I do change the initial value like setting it to 10

awesome okay we can see 10 showing up there let's go back to zero for our starter Point okay let's jump to the

second part of this challenge I want you to create a function that's called add

that will run when the plus button is clicked and for now it can just consol log the string add or something like

that no need to worry about changing State quite yet as a reminder it's a pretty strong convention to create any

functions that your component will need to run inside of your function but above the return so instead of coming outside

of your function up here and creating a function called add you would want to do that inside your function probably below

where you're creating state so right here okay take it

away okay let's add a function called well add and for now the body of it will

just console log the text add and then on our plus button which is let's see

not this one that's the minus this is our plus button right here we'll go ahead and add an onclick and set that

equal to add all right let's hit save and clicking the plus good should console log add perfect add add add and

minus of course does nothing quite yet okay this brings us to the next challenge up until this point we've

touched a little bit on what you could do in order to update the count although we haven't explicitly talked about how

we could do something like this where every time they click it a different value gets displayed in other words in

the past we've done a thing where we said something like set count and then hardcoded the number one in there or I

think in the last example we had changed the text to heck yes for it being important to learn state but of course

that meant that every single time we click the button it just kept resetting the state to the same value so that

brings us to this challenge where I want you to see if you can figure out a way so that when you click plus multiple times it will continue to increment the

number so give it your best shot see if you can figure out how to do this challenge

okay hopefully that challenge went okay all I need to do is call set count and then for the value that I pass in here

it turns out I do have access to what the current value is with count and so I'll go ahead and put in count but I

don't want it to set to the current count I want it to set to one above the current count so I'll say count plus one

let's hit save we can hit plus and awesome this is working now I do want to address a common misconception with

beginners and react and that is those of you that tried to do count Plus+ first of all if we try to run this we'll see

that when I click plus we get an error that says you can't assign to a constant variable so you might have gone up here

and said well let's change it to let and I'll hit save and look at this I get

some pretty funny behavior I'm clicking it two times and only after clicking it two times will it actually increment

let's see what happens if we were to put the Plus+ before the count in case you're not familiar with that trick it

simply increments one to count before returning it and so the value becomes the new incremented version so let's hit

save and okay technically this is working but I don't want you to get too Ed to this because this is a big no note

in react remember doing count Plus+ is the same as doing count equals count

plus one and in react whenever you want to change State you will never ever ever change it directly in the way that we're

doing here where you say here's my state variable set it equal to something different it's a big no no in react so

try to remember that if you are ever modifying the value directly then you're doing it wrong on the contrary saying

count + one it's not directly modifying count it's simply providing the new

value that we want our count to have to set count which will then update State

rerender the component and display everything correctly let me go ahead and change this back to a const in fact that

should have been our first red flag when it was warning us that we were trying to change a constant hit save and we're

back to the way we were before but at least now we're doing it the correct way okay that brings us to the last

challenge your challenge is to add functionality to the minus button of course the functionality that it should

add is to decrease the count by one give this one Your Best

Shot I'm doing essentially what I had in the add function so I'm just going to duplicate my logic there we'll change

this to maybe subtract I'll change this to minus one and then we will add an

onclick actually let me just copy this whole thing we'll add that directly to our minus button and changes to the

subtract function hit save and awesome we're going up and down perfect awesome

work it's great to get our hands on the keyboard and be practicing this we had a lot of practice in this one if you need

it's completely okay to go back and redo all of these practices from scratch if you really want to add a little extra

challenge this would be a great time to come through and just delete all of the code that we've written regarding State

and see if you can create it again from scratch I won't leave you in a broken State like this so I'll put it back but

just remember that you're here to learn and learning comes through lots of practice once you're ready we're going

to move forward and see another way that we can use our state Setter

function the way we have our code structured right now it's technically working just fine I can hit plus it's

incrementing I can hit minus it's decrementing and the way we're doing this is by calling our state Setter

function which we're calling set count and providing a new value for the state that we want it to have once we call set

count it will change the state to the new version that we provide and it will rerender with count now being that new

version that we provided however there is another way we can use our state Setter function set count in this case

where instead of providing the new value we provide a callback function in the body of this callback function we need

to return the new value that we want state to be on the next render of this component if I were to essentially

recreate exactly what I had before four I would just return count + one which is basically no different than what I had

and we can hit save and see this is working as we might expect however the difference comes in the fact that this

callback function is going to be past the old value of the state before your

set count function ran and so what I can do is take this old value and instead of

using count which is my state variable I can use the temporary version which is old value in place of what used to be

count I'll hit save and we'll see this is also working now instead of old value

I like to use preve and then the name of my state variable so pre count in this

case this is a fairly common convention that I have seen quite a bit in the code and it's one that I try to adhere to I

think it's a little bit more clear what state value we're dealing with and at first glance it might look like this is

just a ton of extra work but if I take advantage of the more tur syntax of

Arrow functions I can simply say PR count and then an arrow to return pref

count plus one and in the end it's not terribly different than what we had before so why exactly are we doing this

let me actually type this out as a written note for those of you that are maybe more visual Learners it'll give you something to refer back to and read

through as we talk about it together so a general rule of thumb is that if you ever need the old value of your state in

order to help you determine what the new value of State should be after calling your set State function or in our case

we're calling it set count then it's a good idea to pass a callback function to your state Setter function instead of

using the state value directly like we're doing down here still the Callback function that you pass to it will

receive the old value of State as its parameter which allows you to then determine the new value of your state

this is going to seem a little bit crazy let me bring this back down to zero let's hit save and I'm going to show you

a difference that doing this makes even though honestly it's not something you're like going to run into very often let's go

ahead and duplicate this line three times and I'm going to duplicate the old version that we have down here three

times as well I'll hit save and I want you to think what do you expect will happen if I call the add function or

rather if I click the plus button which then calls the add function and when I hit the minus button which calls the

subtract function well you would think that it would increment it three times if we hit the plus button and check it

out it does we immediately go up to three however if I I hit the subtract button we only go down one time all

three of these set counts get batched together the reason and specifics as to why are a bit outside the scope of this

course but this is a admittedly overly simplistic example of how using a

callback function if you need access to the old value of state to determine the new value of State helps behave kind of

the way that you might expect whereas using the state value directly doesn't

now I don't want this to be anything that hangs anybody up let's go ahead and get rid of this I simply wanted to show that there is a slight difference in the

way that react handles the two but again for a majority of the time you won't notice the difference but this is a good

rule of thumb to stick by and it's the internal rule I'm going to use for myself as we continue through this

course okay that was a lot of talking let's do a challenge simply enough your

challenge is to update the subtract function so that it uses a callback function instead of using the state

directly to determine the new state go ahead and give this a shot

we took a kind of roundabout way to arrive at what we have currently for our ad function but we can see that if I

simply say pre count Arrow preve count minus one we really only had a few extra

characters to type and now we have adhered to a little bit of a better practice anytime we're setting state

that relies on the old value of state I'm going to clean up this challenge text but I'll leave this note here for

anybody who wants some additional reading and again this would be a great time if you really want to challenge

yourself to just come through and delete everything and see if you can recreate it from scratch and I really mean that

that's something you should do it's not just me saying that would be nice if you did it I mean you should do this again

you're here to learn this stuff deeply not just to passively watch me teach you about it and kind of think to yourself

yeah I think I get it prove to yourself that you get it by doing it it's not just going to give you those warm

fuzzies when you actually complete it and everything's working it's also going to strengthen you as a

developer in react and frankly assuming you plan to look for a job it's going to make you a more viable job candidate

there's so many benefits to getting your hands on the keyboard and practicing it would just be a tragedy if you skipped

through all of these practices instead of doing them and finding ways to challenge yourself outside of the

challenges that I give you all right stepping off my Soap Box again I think we have thoroughly covered the concept

of state so it feels like it's time for a little quiz

okay it's time for another quiz as always I'm going to insert a pause here I want you to click in and actually type

down your answers to these questions taking quizzes like this is scientifically proven to improve your

ability to retain this information and recall it at a later time so don't skip answering these questions okay I'll hand

it over to you all right number one you have two

options for what you can pass into a state Setter function like the set count function that that we had in our counter

app so what are those two different options well for one we can simply pass

the new version of state that we want to replace the old version of State this works great for any kind of state where

we don't care what the old version of State used to be we simply want to set it to some new value that has nothing to

do with the old value later in the section we'll be talking a bit about forms and we're going to see where we make use of that there's also lots of

other applications for this first way of updating State the second way is to pass

a callback function to our set State function this callback function needs to

return what we want the new value of state to be and this callback function is going to receive the old version of

State as a parameter and the purpose of that parameter is to then help us determine what the new value of State

should be okay numbers two and three I think we kind of touched on these already but when would you want to pass

the first option from the answer above in other words simply passing the new version of state that we want it to

become and this would happen anytime we don't care what the previous value was we simply want to set a new value and

naturally and conversely number three when would we pass the second option it's the exact opposite it's whenever we

do care about the previous value of state and we need it in order to help us determine what the new value of State

should be okay hopefully that was pretty straightforward if not that's okay maybe go back through this quiz again and see

if the repetition will help out out once you feel good about this let's keep moving

forward at this point it's going to be really helpful for us to review the tary operator in JavaScript if you feel like

you've already got a good handle on it then this challenge should come pretty easily to you if not then I'd recommend

going over to the mdn docs on the conditional operator also known as the Turner you can click the screenshot here

to go directly to the documentation on that we'll be using it in this pretty simplified example this makes a slight

tweak to our app from before now it asks if we feel like going out tonight we're not using any kind of state here we're

not handling the click of the button to change that state or anything like that we're simply practicing the Turner here

so your challenge is to replace the if else that's right here with using a Turner right here on line 8 instead we

have a variable called is going out and we have a variable called answer which will contain the text if is going out is

true then the answer will be yes if it's false then the answer will be no it's being displayed down here in the center

of the button again don't worry about clicking the button to change the answer or anything like that you'll simply

include your Turner here hit save and it should show the correct answer there and then of course you can test it by

changing this to false to make sure that your code is working okay it's your

turn if you're not as familiar with the Turner that's okay we can see that the syntax actually consists of two

different parts one is a question mark and the other is a colon and it's really just a simplified way to have an if else

statement in a single line so what I can do is I can say I want answer to equal

and then first we're going to check if is going out is true so we'll say is going out equals true and if it is true

then what I want answer to equal is the string yes so that's essentially my if

if this condition evaluates the true then this is what should get returned my else is going to be separated with a

colon and then I'll have my string no now you can actually Nest Turner's multiple levels down as a way to replace

an if else if else if else if block but I personally find that a little bit more

difficult to understand and follow so I tend to stick to a Turner if I simply have an if else statement but otherwise

it's totally fine to use an if else if or a switch even so let's go ahead and get rid of our old code here we can see

it's quite a bit simplified first let's make sure that everything is working so I'll hit save and sure enough we get yes

if we change this to false we get no okay now there is another way that I can simplify this just a little bit more we

know that is going out is already a Boolean and so I don't necessarily need to equate it to the Boolean true I can

simply say is going out and that's already going to be the bullion that I need so we H save we see no we change

false to true and we see we get yes and actually because I'm not block scoped

anymore with the curly braces of my if El I could change this to a const if I wanted now in this case I've set aside a

separate variable just to figure out what the string should be and then I'm rendering that variable down inside the

return of my component but there's another way to do this and that is to Simply move my Turner into my component

itself and it will figure it out on the Fly this should be a pretty straightforward challenge but we'll go

ahead and keep our fingers warm so that you can keep learning your challenge is to move the Turner directly inside of

the jsx remember once I go into my curly BRAC inside my jsx I can run any

JavaScript expression that returns a value that makes sense in this context so go ahead and give this challenge a

shot simply enough I no longer need my answer variable I'm just going to take this expression and put it right in

place of answer we'll go ahead and clean this up and the challenge text too and

awesome this is quite a bit simpler than what it was before this might seem a little bit out of place but we're going

to see in the next lesson why this is helpful for us

this challenge will be a collection of the past few things that we've been learning we're going to make it so that our users can actually click the button

and change the answer from yes to no or no to yes so your challenge is first to initialize some State for the is going

out we initialize it as a Boolean you can choose true or false I guess depending on what your mood is like

right now then and the language I'm using is a little bit vague I want you to make it so that clicking the button will flip that Boolean value for from

True to false or false to true and then right now I just have this back as a hardcoded yes you're going to display

yes if is going out as true and know if it's false okay I believe in you give this your best

shot first we need to initialize some states so we'll need to import and as a

reminder we could just import the use State function from react this is a very

common way that you'll see this done as I mentioned before I'm going to actually import the entire react Library just so

that I can use react. state only for the purpose of keeping it clear that this is

a function that comes from react I'll initialize the value to true well who am I kidding I don't really feel like going

out tonight let's set this as false and what gets returned is an array so we will destructure that array when we save

it in variables we'll say is going out and then by convention I'll start my Setter function with the word set is

going out okay awesome and you know what I think I'm going to skip to this last

one it's completely fine if you didn't do that but I want to display this as either yes or no depending on my value

of is going out and to do that I'm just going to do an inline Turner like we just did in the last lesson so I'll say

is going out question mark in other words if is going out is true then I want it to display yes but otherwise I

want it to display no let's see if this is working I had said false so let's see if it changes to no and perfect okay

let's see let's buy ourselves some room here we got done with those parts of the challenge now we need to make it so that

clicking the button actually flips that Boolean value similar to how we are just doing this inline expression if we want

to we can add our onclick function Handler directly inside of the curly

braces that we have here I'm going to start by doing this and then I think we'll see in a second why my personal

preference is to put these functions up above the return section of our component so I can just do this as an

inline Arrow function and when the button is clicked I want it to call set

is going out and if you remember we just learned how there's two different options I have when I'm calling my state

Setter function I can either provide the new value that I want state to have or I

can provide a callback function I want to synthesize the quiz that we recently took and give you a chance to think

through this which of those two versions do we want to use in this case well we can simply ask ourselves do we need to

know what the old value is in order to determine the new value and in this case yes we we need to know if it was false

so that we can flip it to true or if it was true so that we can flip it to false and I guess it's kind of a mixed answer

because the truth is I have a way to just flip a Boolean to its opposite so what I can do is say it's not is going

out and that should get the job done in fact let's test that out we'll hit save we have no we click it and it says yes

okay it's working so you know what maybe this is a little bit of a gray area in that question of do we need the old

value or not because we do need the old value and I can just access the old value and this

will work fine maybe for completeness sake we'll also see what this looks like to use an inline function and you know

what I can already see this is getting a little bit crazy we have our inline click Handler function and that is

calling set is going out which is taking a function and I don't know about you but this is maybe one level too much of

inception for me I think it's going to be clearer to move this outside of our return so let's create a function and

call it something like change mind and we'll take what we have here let's see how far do we need to go all these curly

braces and parentheses are also really confusing when it's in line like that and okay I missed one we'll clear out

everything in here except that outer set of curly braces and simply call change mind this puts my mind much more at ease

than what we had before okay so if I'm going to use the Callback function version of my state Setter then I can

get the preve state and maybe just for brevity we'll just call it prieve and I

can just immediately return the opposite of prieve hit save and no yes no yes no

awesome let's clean up this challenge text and one last thing I want to do before we move on is address this button

first of all I admit this is not a very good user experience with our silly little learning app here it feels weird

to click no and have that be the way to change the answer so if you're designing a real website with a user interface

maybe don't choose a button that clicking it will flip it to its opposite value but since that's where we are

right now one thing that will be really important for us is to address the accessibility of this button I'm going

to put some of these values on their own lines so that we can add an ARA label to

anyone using assisted Technologies like a screen reader the purpose of this button is going to be pretty opaque and

so I'm going to include an ARA label that will both clarify what the state of this button currently is and describe

what will happen if you click it so I can say something like the current answer is and then I'll just stuff in

the yes or no value that we're determining right here so actually I can just copy my Turner and put it right

there so that's what the current answer is and I could say something like click to change it little additions like this

make a huge difference for a number of people so this is an important thing to keep in mind while we're developing our

code frankly I should have included this earlier or probably just changed our button to something like an H2 so this

might be a little bit overdue glad that we're adding it in now okay great job with these challenges if you did find

yourself struggling to complete that challenge then this is one of those perfect opportunities to take a break go

back a couple lessons review what we've learned try to practice them again from scratch and eventually you'll get to

this point you'll be able to do this challenge with no problems and that's a great time to Pat yourself on the back

go take a walk get an ice cream do something celebratory because we've made some awesome progress here once you're

ready we'll keep moving forward up until now the examples of

State we've been using have used pretty primitive values like booleans or strings but a very common thing that

you'll find yourself doing is including more complex data like arrays and objects in your state variables and it

warrants a little extra attention to see how we can update more complex State like arrays and objects so let's start

with arrays and hey this looks familiar this is the little app we were using when we first started learning how we

can't just save the values we want to display on the screen in local variables like trying to do this but instead if we

want those values to display on the screen and to update when we change those values we need to use react state

so we'll get started with a quick challenge I want you to convert the code below so that instead of using this My

Favorite Things array in a local variable you should instead create some State and set that state as an initial

value of an empty array don't worry right now about the ad favorite thing function we'll get to that soon go ahead

and get started on this challenge I'm going to save this

variable name so I'm actually going to destructure what will get returned from

our array we'll go ahead and also include our set my favorite things and

instead of this being an empty array we're going to use react. use State and

we'll put that array as the initial value and then of course I need to import react because I'm not currently

doing that so we'll import react from react okay I think hitting save should

be fine of course add item doesn't quite yet work I can do a quick test of this by taking maybe a couple items from the

all Favorite Things sort of database of favorite things there and just sticking them here inside of my Ed State and sure

enough okay hitting refresh shows raindrops on roses and whiskers on kittens perfect I'm going to undo that

just so we don't get duplicated items when we do start adding to the array okay none of that was technically new

but the reason that I wanted to record this scrim is so that we can see how we can make updates to our array well at

first it can be tempting to Simply say well I know how to add something to an array I can say my favorite things. push

however there's a couple things wrong with this first of all even if we do try to put something in here like a test we

can see it's not actually working and the reason is because simply modifying the state value directly doesn't also

trigger a render in react there's something special about the setter function that we receive when we're

calling react. state that does trigger a render in react so I'm curious if I were

to maybe console log my favorite things and try this out we'll see that sure

enough it is adding those items to our array but because we're not using the

set my favorite things function it's not triggering a render there's something else that's wrong with this though

besides the fact that it's just not updating what we see on the screen and that is that it's a pretty hard and fast

rule in react that you never ever want to directly modify State using something

like push it's a destructive action to arrays it modifies the original array it

doesn't just return a new array with that modification it actually modifies the original one and just like when we

had a variable called count and we decided we never wanted to do count Plus+ even if it was inside a state

Setter function like set count we talked about how this is a replacement for count equals count + one and saying

count equals something different is just a bad idea in react similarly using something like My Favorite Things ray.

Push is always a bad idea in react assuming My Favorite Things is a state variable okay so to modify anything in

state as we know we have to use the setter function that we receive so we'll use set my favorite things okay so I'm

sure you remember we have two different options we have to decide between when it comes to using the state Setter function do we want to provide just a

bare new value or do we want to provide a callback function I'm actually going to put in a pause here so you have a

chance to think through this which of those two options do we want to do in this

case we provide a new value if we don't care about the old value at all we

provide a callback function if we do care about what the previous value of state was or in other words if we need

to use the previous value of state to help us determine the new value of state and in this case we want to start adding

items from the all favorite things to our favorite things or My Favorite Things array and so we need to remember

what was already in the list in order to not only determine which of the new items we want to add but also so we will

continue to display the old items as we add new items to our list so we'll go ahead and include a callback function

and we'll just call the previous state maybe previous fave things or pre fave

things that's kind of a mouthful we'll include our arrow and now we need to think how are we going to update this

array without modifying the original one because I still wouldn't want to say pre fave things. push even though it kind of

seems like I'm accessing a different array this is a reference to our original Favorite Things array or My

Favorite Things array so this is also not something we want to do but in true functional programming fashion the way

that I can update the array in react is by providing a brand new array and then

I can use all of the items from the previous array and then I can start this array out by taking all of the items

using the spread operator from the previous Favorite Things array and then I can add my let's just put this in

angle brackets so that you know this isn't the real syntax I'll put in my new item here what this does is it accesses

the previous version of my favorite things array and it returns a brand new array so it's not going to be modifying

the existing My Favorite Things array it's returning a brand new array that includes all of the items that were

previously there plus the new item that I want to add just for test sake I'm

going to just include the string test here and we can see that this is working

awesome it's of course not interacting with the all Favorite Things array yet but we're going to get there in just a second however because I did kind of

just blow through this and didn't ask you to put any critical thought into this surprise I have another quick

challenge for you okay I cleaned up the old challenge text moved it down here

and your challenge is I shouldn't be doing this you should be doing it every time the add item button is clicked it

should add another string test to the list on the page like we just saw it doing see if you can remember what we

did before you just scrub back and see how I did it think critically spend at least 3 or 5 minutes trying to figure it

out see if you can remember what we did hopefully this is a good wakeup call for anyone who was maybe passively watching

okay I'll hand it over to you anytime we want to change State we

need to use our state Setter function so the first thing I'll do is call set my favorite things I need access to my

previous array and so the safest way to do that is to use a callback function I'll just stub out this empty inline

Arrow function now this callback function is going to receive the previous state maybe we'll go ahead and

call this pre fave things even though again that's quite a mouthful and we'll

use an implicit return here so we can get rid of our curly braces and we are going to return a new array that

includes all of the pre fave things and adds test to the list now don't be too

confused we're not yet using these emojis so the first time I click add item I'm starting with an empty array

and then adding the string test the second time I'm clicking add item I'm starting with an array that has just the

single string test in it and I'm adding a second one and then a third one and so forth let's see how we're doing we'll

hit save add item awesome it's showing up of course we have key issues because

we're not having any repeated items here but now we are having repeated items there that's okay for now awesome work

this wasn't a super simple challenge so hopefully it wasn't too frustrating Kudos if you were able to write this

without even looking back but it's completely okay if you did have to go back and study again okay let's clean up

this text so we buy ourselves some room back and I'm actually going to put this on its own lines just so that it's a

little bit easier to read and oh looks like formatting bumped everything out that's great that's okay okay so I'm

actually going to do this part because it deals with indexing into this all Favorite Things array honestly this is

not really something you'll find yourself doing in react so I don't want this to become a challenge I'm going to

use the pre fave things array to figure out what index in the all Favorite

Things array I want to add the new item from so when the pre fave things array

has nothing in it it's going to be the index of zero which is the same index of the new item in all favorite things that

we want to add so I'm just going to say all favorite things at the index of pref

things. length again this is sort of where this example starts to break down because this is not something you'll

find yourself doing super often because react is just a lot of JavaScript this is kind of a fun

challenge at the same time let's cross our fingers hit save and see what we have we'll go ahead and add items

Raindrops on Roses whiskers on kittens bright copper kettles and warm woen mittens awesome please Disney don't sue

me awesome work on these challenges updating an array in state is something you'll find yourself doing quite often

in react so this is a great thing for us to learn and a great thing for you to practice as much as you can next we're

going to take a look at how we can update another complex data type and state which is

objects all right finally at long last we're back here with our Chef CLA app

and now we're armed with the knowledge that we need to make this work as you might remember where we left off we just

had this local array of ingredients and we tried to do an ingredients. push to

push the new ingredient onto that array and of course we saw that it didn't update our view now we understand that

react doesn't update The View when just little local variables like this change instead we have to put these values in

state then as long as we use the state Setter function that react gives to us we can change the data and rely on react

to update our view to reflect the new updated data to our users so your challenge is to do exactly that update

our app so that when the user enters A new ingredient and submits the form it will add that new ingredient to our list

I added a note down here just like before I don't want you yet to worry about what's going on in these two lines

of data just take the new ingredient and be grateful that you don't have to know this no I'm totally kidding we're going

to cover this later by the way when you work on this you don't have to begin the array with these three items you can put

whatever you want it can be empty you can add a couple just to make sure it's working whatever you want so go ahead

and get started on this challenge all right let's go ahead and

import react so that we can pull in state and watch this trickery I'm not

even going to delete this line I'm just going to refactor it to use state so we'll say ingredients set

ingredients and that's going to be equal to react. use State and then we will

wrap our array and let me make this small for a second I think I'm going to

keep this empty actually yeah we'll just keep it empty for now okay so it's being saved in state I think I can hit refresh

and everything should still be working awesome of course we lost our items because we removed them from the array

you might have noticed also that I did remove the ingredients. push line because as we've learned we do not want

to directly modify any of our state variables we always need to do it through calling the state Setter

function so at the end of my handle submit right here I'm going to call set

ingredients and I do need to know the previous list of ingredients so that I can use that list in my updated list so

we'll say previous ingredients and this will be a function and I can just return

a new array that's going to include all of the previous ingredients and it's going to stick the new ingredient right

there at the end so jeez in the end we really just added one line of code and

refactored this line of code let's clean up our challenge text we'll hit save and

moment of truth let's say we have some chicken awesome chicken and up right there now of course our form is not

emptying we're going to address this a little bit later when we talk about forms so for now I just kind of have to

annoyingly delete the old entry myself let's say we have some limes and maybe

some salsa awesome great work on this challenge shift CLA and myself are

really happy with your progress in this section so far so we had a chance to apply what we just learned about

updating arrays in state next we're going to see what it takes to update a different complex object and state which

is objects now let's take a look at what

it's like to save objects in state we have an example of a little contact card here and we're holding an object in

state which represents the information for this particular contact the first four properties are all pretty

self-explanatory they display the actual information first name last name phone number and email this last one is

favorite we are going to ignore dealing with that for now at least in this first challenge But ultimately it's going to

determine whether this star is an empty star or a filled star but before we get there I want to give you a challenge

where you're going to fill in the values that are currently being hardcoded so we've got the name phone number and

email and instead use the values that are being saved in this object and state

from that we're currently calling contact so go ahead and get started on this challenge of these four properties

the trickiest one might have been the name because we're saving the first name and the last name under different

properties all I really need to do is do a set of curly braces and we'll pull in the first name by doing contact. first

name and then outside of the curly braces I can do an actual space because we're outside the curly braces this will

represent an actual space in the text and then I'll do another set and add my

last name the tricky thing about this challenge is I'll hit save and it will look like nothing changed but now it's

using the dynamic values from our state okay then we'll go ahead and just do the same same thing for our phone number

contact. phone and our email address which was contact. email hit save and awesome okay

now let's deal with the is favorite property and ultimately our goal is so that we can click the star icon and it

will flip the value inate from True to false or false to true and following the declarative nature of react it will also

update the actual icon here from an empty star to a field star and vice versa we're going to do that actually in

two parts so for the last challenge in this lesson we'll be making it so that the icon of the star will represent

whatever the current value of state is so if this is false it will be an empty star and if it's true it will be a

filled star let me actually type that out as a challenge okay so your challenge is to use a Turner so that you

can determine which of the two star images which we're importing by the way so either this star filled value

variable or this star empty variable should be used based on the value of

contact do is favorite for now you can just test how things are working by manually flipping this to true and of

course when you do that it should update the star to be the filled in Star so

your turn area will be here I'm going to be a little bit vague on the rest that you should be working on because I think

you'll be able to figure it out so I'm going to pass it over to you to work on this challenge okay let's put in our

Turner here and we are going to be looking at contact. is favorite and if it's a truthy value in this case

it will actually be the Boolean value of true or false then we want it to be star

filled because I have this set as a variable as I'm importing it it should just work out as far as becoming my

image source and otherwise I want it to be star empty let's clean up this challenge

text and lastly I need to take the star icon and come down to my image source

where it used to be coded as star empty and now we'll use whatever the value of star star icon is let's hit save and

okay we're empty we are not yet set up to make this click actually flip the

value there we're going to be getting to that very soon but for now let's change this hardcoded value to True hit save

and awesome we have a filled star okay well while you were changing the star icon in our image source you might have

noticed that we have an ALT attribute here which has a hard-coded value saying

empty star icon we also have an accessibility property called Aria pressed which is defaulted to false and

actually you know what this button should also have an ARA label associated with it because this button doesn't have

any text that makes it obvious what clicking it will do so staying in line with the assumption that everything is

not favored currently this I guess would say something like add to favorites

however we want all of these values the ARA pressed the ARA label and the image

alt to change all based on the current value of contact. is favorite so before

we move on and learn how we can programmatically flip this by clicking the button let's go ahead and do a

challenge that updates those things as well okay in this challenge I've given you the tasks that you need to complete

but I'm not going to give you any starter code or any hints as to what to do because I believe at this point you

should be able to accomplish these things again the reason that we're doing this extra work work is so that we can

really take advantage of react's declarative nature where the state that we're maintaining up above is what

determines the display and the functionality of some of these elements on the page so give this one your best

shot and we'll come back and do it together afterward okay I think the Aro press is probably the easiest because it

should track one for one with whatever the value of contacts dot is favorite is

this button is going to be represented as a pressed button to assist of Technologies if the contact is favorited

and that just kind of makes sense with the ARA label I can either say add to favorites or remove from favorites and

we've seen an example where we're doing our Turner up here I think I'm also going to show an example of just doing

an inline Turner here I'll use a set of curly braces instead of my quotation marks so that I can evaluate some

JavaScript and we'll take a look at contact. is favorite we'll put our question mark and if it's truthy we want

this to say let's see if it's favorite then we want it to say remove from

favorites because it's already favorited and otherwise we'll say add to favorites

and then we can just do the exact same thing with our image alt we'll surround this in a set of curly braces we'll

check contact dot is favorite and if so then we want it to

say fill star icon but otherwise it should say empty star icon most of this

fun functionality is stuff that just sits a little bit behind the scenes and is only really viewable if you're

looking at the source code or if you're using assist of technology so I think we might just have to assume that it's

working and we'll clean up this challenge text and we're in a pretty good place however most of this has just

been prepping for what we're actually here to learn which is how we can update our state when what's being saved in

state is an object we're going to see in the next lesson why that might not be as simple as we think and how we can go

about doing it we've set up our markup so that it

will react to the changes in state and this is exactly what we want the only thing we're missing is the user

interactivity with this star icon the goal is of course to be able to click the star icon and have it flip from True

to false or false to true and by having it flip I mean the is favorite property

on our contact object so down here in our toggle favorite this is where I would probably want to use my set

contact and we have to think to ourselves do I need to know the previous contact in order to determine what the

new contact is and the answer is yes I need to know what the is favorite property was so that I can flip it from

its old value to the well opposite of its old value so we'll go ahead and use a callback function in here and we'll

grab the previous contact and we will return an object and the contents of

this object can be a little bit tricky so that's why we have a dedicated lesson for this it can be tempting to think

that I'm changing the is favorite property so I'm going to return an object that has not the current is

favorite value but looks at the opposite of preve contact do is favorite and

there is a bug with the way that we've written it here before hitting save and even before testing it out I'm going to

insert a pause here and give you a chance to see if you can figure out what the problem is with the way that we currently have it

written remember in my callback function for my state Setter function the goal is to return a replacement State and in

this case my state is an object that has five properties first name last name phone email and is favorite however what

I'm returning is not an object with five properties but an object with only one property which means let me go ahead and

hit save when I click my star icon all of the other information disappears

however it does look like our star is working as we might expect I can flip it back and forth It's correctly pulling in

the opposite of what it previously was but of course our contact is now just an object with one property the best way

for me to make sure that I copy all of the old properties is to Simply spread in everything from the previous contact

and then I will include a new version of is favorite if you're feeling a little

bit Rusty on the object spread syntax like we have here it's essentially like taking the old version that we had up

here and just copying and pasting it down we'll indent this correctly and what we're returning is a new object

that has all of the properties from the old one first name last name phone email and the old is favorite but then we're

overwriting that is favorite property with the opposite of what it used to be and believe it or not this is not a

syntax error in JavaScript it will simply take the last one that's declared if you have multiple instances of the

same key in an object it will just take the last one that's declared and use that value as the final value for the

object now we don't actually want this hardcoded because we don't at any given time know what these values are going to

be so we'll come back to using our spread syntax here let's hit save we have all our information back cuz it's a

fresh render of this component and moment of truth let's click the star and awesome it's flipping back and forth as

we would expect perfect okay well I would be doing you a disservice if I didn't give you a chance to write this

so I do have a quick challenge for you your challenge is simply to rewrite what we just did if you're not entirely sure

how you should do this then I would recommend rather than just skipping the exercise Al together and watching me do

it for you scrub back in the lesson and get a refresher on how we did it and then come back to this Challenge and try

it again for yourself all right it's your turn to shine take it

away we need to use our set contact function we do care about the previous

version of state so we'll access preve contact and use an inline function here rather than opening my set of curly

braces and saying return object I'm going to make use of the implicit return

by using a set of parentheses and wrapping inside of that the object that I want to return I'll pull in all of the

pre contact properties and then switch the is favorite to be the opposite of

pre contact. is favorite I probably should default this to false I think

that's more logical for a new contact in a contact book but we'll go ahead and

check it out it's working just great awesome some work on this we have learned quite a bit about State how to

set State some complex data types in state and how we can make modifications to those and now we're ready to move on

to the next topic which is dealing with

forms Although our Chef Claud app has just about as simple of a form as you could possibly have it's got the single

input and a button to submit the text from that input you'll find that creating forms of one type or another

will be a really common task that you end up doing in your react applications whether it be something that's very

clearly a form like a sign up or a login page or something that's maybe a little bit more subtle of a form like when you

favorite a tweet or upvote a post on Reddit any kind of interaction with the data that exists in a database from your

application will often times be handled by submitting a form and if you've been

developing for the web for a long time you'll know that forms have been around for a very very long time here in our

HTML file we just have a regular form element it's got a couple of labels that are associated with a couple of inputs

and then an input type submit which is our button at the bottom the form property has a method attribute that you

can give to it by default this method is get and submitting a form with a get

request actually let me get rid of my action and my method the default method is get and I'm going to comment out my

script here so I'll refresh this and type in my my first name and last name

hit submit and you'll see that first of all there was a full page refresh that happened it cleared out our form but it

also tried to navigate us to a different location if you look in the URL it says slash which is my homepage but then it

stuffed the information that I put into the form into a query string in the URL

so commonly in the early days of the web we would include an action property that would specify some kind of server code

maybe a PHP file for example and let me actually let me just say this is a get request so that it stays the same as it

was I'll comment this back out and let's go back to our homepage here I can fill

out my information and we're going to get an error because we don't have a PHP file but we'll see we hit submit and it

attempts to go to /iy server code. PHP and then it puts

the information from the form into the query string after that point this is where a PHP file would then take that

information do some sanitizing checks on it submit to the database or whatever it

might be process it somehow and likely return another HTML page that the browser can then display on the page for

the user fast forward a little bit and JavaScript became a little bit more of a

popular way to gather information from a form and send it to some kind of backend so let me get rid of this action because

we don't have a PHP file and I'll leave my method there for now I'm going to have to manually go back to my index

page here and now we can look at our JavaScript and see that we have set up an event listener for the submit event

on my form when that submit event happens we're going to capture the event

which has a bunch of information about the event that we're listening for and the first thing we do is prevent the

default which includes refreshing the page so now that we have that we can see I can put in my name and hit submit and

instead of the page refreshing and everything clearing out or attempting to go to a different URL we intercept

accepted that in JavaScript we maybe did some processing of the data from the form somehow submitted it to this fake

API which of course is just console logging the data and the text submitted

we can see in the console we did get an object that contains both the first name and last name well what comes next in

the history of web development is a little bit Rocky in fact when I was recording a course about react router I

included a whole lesson that I called hot take forms in react are bad I'm not

going to dive into how react used to deal with forms because as you can tell I really didn't like the way that it did

it it was cumbersome it was a little difficult to teach but after the last about 8 years of teaching react I can

confidently and happily say that now forms were bad they are so much better

now in react 19 than they ever have been by the way I do need to point out that we are currently in a scrim with a

Google slide of a screenshot from a scrim that had a Google slide which included a screenshot from scrim I think

this is about as deep of an Inception we've ever had on scrimba so you are learning react in a golden age because

you will not have to learn forms the way that I had to learn them and the way that I've had to teach them for nearly a

decade now because react has shifted to using the native capabilities of form

over the next few lessons we'll be talking a little bit more about what I mean by that but in the meantime if you'd like you can click the screenshot

here which will take you to the react documentation on the built-in browser form component and you can kind of dip

your toes into what we're going to be learning with form again the form that we're building with Chef Claude is very

simplistic but we are going to dive a bit deeper into forms than we need for this project mostly to cover our bases

but trust me when I say it's going to be a much more pleasant experience than it ever has been in the past react 19 has

changed the game it's truly amazing the improvements that they've made okay without further Ado let's jump in and

start learning about forms and react the next few lessons are actually going

to be kind of a hybrid review of forms that you should already be familiar with at this point and how we deal with them

in react honestly because of how react 19 can now deal with forms this is going to be a little bit closer tied to just a

review of forms in HTML so to get us started let's just start building out this form and actually I was going to

get rid of this H1 let's go ahead and call this a signup form and I'm going to have more elements maybe I'll put

everything here inside of a section okay so to start out a form we will always start with a form element an HTML form

element we're going to discuss some of the attributes that we can add to our form but for now let's also get an input

in here input is kind of a crazy component or element in HTML because

it's very overloaded in other words there's a lot of different types of input and depending on what type of

input you use what gets displayed in the form is drastically different from another type for example if we have a

type of text it's going to show up as a regular input box if we were to instead

do a type of radio we get a little circle that you can click and these are

intended to have multiple different options I'm a little bit torn how I feel about this it feels like maybe they

tried to get input to do too many things but I'm certainly not an HTML expert so

there's probably a good reason for it okay so type is one of the most important things that we're going to add

to our inputs I would say maybe the second most important thing is to give it a name attribute the name attribute

is how we're going to access the data that is input into this input Box by the

user so after the form is submitted we'll need to make sure we have a reasonable name so that we can access

that data since this is going to be a signup form let's go ahead and put email that will be the name and actually if

I'm going to make this email there's a dedicated type of email that I can use use for this input I think what that

does mostly on mobile devices it will pop up a slightly different keyboard that has that little at symbol that's

really accessible and maybe a couple other little things with the keyboard change either way it's a good idea to

put it there oh I also think it might be helpful for password managers although I'm not 100% sure on that either way you

should always strive to put the correct type for your inputs so we'll go ahead and use email okay we can hit refresh

and see this input is very unclear what it should be doing and it can be tempting to then say well I'm going to

use the placeholder attribute to say this is going to be where the email goes in fact I think this is something you

will very commonly see but it's a habit that I'm going to try and weed out of you right now a placeholder is not the

correct tool to use as a label for your input a placeholder instead can be a

great place to put an example of what should be filled in like let's say Joe ato.com but for accessibility reasons

it's much more difficult for screen readers for example to make any sense of an input it won't read the placeholder

text and so it's going to be difficult for anyone using a screen reader to know what they're supposed to do with this input I can get around that with an ARA

label but whenever possible we should just use a label element this is where

we can simply say email and if we actually take our closing tag for the label element and put it on the other

side of our input in other words wrapping our input as a child of the label then this label will automatically

get a associated with this input and we can tell that easily by clicking email and see that our cursor is then focused

inside of the input box the design here is awful so don't judge me for that

we'll fix it up soon I'll probably fix it up after this lesson so you don't have to watch me doing more CSS with a

form but for now this will get the trick done while we're talking about labels if you can't put your label around your

input the way that we did there but instead would prefer them to sit side by side as siblings you can still do this

but we do have to take a couple extra things into consideration first of all we need to associate this label with

this specific input and we can do that with an HTML 4 attribute if you're familiar with regular HTML forms and

HTML labels you'll recognize this as the four attribute in regular HTML but

because we're dealing with dom elements here it's not the JavaScript label element doesn't have a four property it

has an HTML for property and so in react because we're dealing with JavaScript we will use that property HTML 4 its value

needs to be the ID of the input that you want to use so we'll give this an ID of email and say that this label is

associated with the input with the idea of email so I can hit save and you'll see I click on email and my cursor gets

focused inside the input as well I personally prefer the look of this even though it does require me to do a little

bit of extra work I think it also makes doing CSS for this just a little bit easier but honestly whichever way you

choose is going to be completely fine okay I feel like I've been talking for a really long time this might be a silly

challenge but I think it's time to get your hands on the keyboard okay this is pretty straightforward I want you to add

another label and another input for our password field and because we haven't done any styling on here I'm going to

just manually add a Brak element and then leave some space here for you to do your work make sure you use the correct

type when you're adding your password input and don't forget to fill in the other attributes that are necessary too

go ahead and get started on this challenge all right simply enough and

maybe I'm going to be a cheater for doing this I'm going to copy all of these properties and we'll update the

data so we have HTML 4 we'll call this password and then set the ID to password

for our input this will say password the type there actually is a dedicated

password type this is the one that will put in the filled in dots instead of the actual characters just to keep it a

little more private we'll give it a name of password and the placeholder I don't think we need a placeholder for password

hit save and sure enough we get the password field working this lesson is getting a little bit long I'm going to

touch on one more thing we'll dive just a little bit deeper into some of the other input types that are available to

us but the last thing I want to talk about is the button element the button element is a little bit unique and it

has a quirk that is important to remember if you've been doing any kind of HTML for a long time you might

recognize that there is a different type of input called a type of submit and as

I mentioned different types of inputs can dramatically change the way it's displayed on the screen well input type

submit is no different because uh let me comment out this button and I think I have to move this out we'll hit save and

check it out it doesn't really look like an input it looks like a button and that's true if I wanted to change the

text on it I would have to add another attribute called value well the default is submit let's I don't know say click

okay we see that's working but this is where our button comes in because buttons if they're placed inside of a

form they act like an input type submit or rather buttons also have a type

property and by default outside of a form the type is button inside of a form the type is submit so a button makes a

lot more sense to me and I'm just going to give it the text of submit all right we have a super basic form I'm going to

give this a little bit of love in the CSS and I'll see you in the next lesson

there's a few interesting things happening to our form when we try to submit it first of all let me go ahead

and type in an email let's just put in bb.com and I don't know password 1 123

we saw this before but if I hit enter or I press the submit button I'll go ahead and hit enter this time we see that

we're actually directed to a different address or a different URL and it serialized the data from the form and

put it up in the query string of that URL native forms on the web work this exact same way if we don't specify a different

type of method the default is going to be a get request and a get request

involves getting information from a URL in this case even though we're trying to send data up to the server the kind of

tricky way that the web works is it tries to get a request from a URL and

then includes a query string with the information that we're trying to pass to it this actually works in a lot of cases

and actually is a good idea in a a lot of cases for something sensitive like an email and password for a signup form

it's probably not a good idea to serialize and put that information in the URL if we instead change this to a

post method and you'll notice that I'm typing these in all caps that's actually just a convention in HTML I can just

keep it in lowercase if I want in fact I think I will leave it that way if instead I use a post method then it

doesn't put the information from the form up in the URL but instead it creates a post request and it puts that

information in the body of that request which is not something that we'll be able to just see right here in our user

interface let me go back to just regular slash I'll enter the same information

and hit enter and we can see we are still getting a full page refresh but we are no longer putting that information

up in the URL okay how can we stop this full page refresh so we can process this information in JavaScript instead of as

the web was built trying to send it directly to a backend file to process it well as we saw in the chef Cloud app we

can add an on submit Handler to our form

and we can prevent the page from refreshing by using that prevent default that we saw before let me go ahead and

create a function called handle submit it's going to take the event and before

I do anything else let's go ahead and set this up as our submission Handler for the form I mentioned this before but

even for the most simple of forms I prefer to be watching for the submit event on the form rather than something

like the Click event on a button for a number of reasons that I've already outlined with that event we can stop the

page from refreshing by telling it to prevent the default and we call that as

a function this makes it so that the page will not refresh again hit save put in the same information and hit submit

and sure enough nothing happens really at all let me just go ahead and console log submit Ed just to make sure that

that's actually working okay good our function is being called successfully now this event that's being passed to

the handle submit function is actually pretty powerful it has a lot of information about it first of all I can

get access to the actual form Dom node so I can say something like const form

maybe it we'll say form L for form element is equal to event. current

Target or in this specific case you also could just use Target it's a little bit safer to use current Target in this case

and with this form element I can actually create a new set of form data so let's go ahead and create some form

data and I can create this by setting it equal to a new instance of the capital F

form data this is something built directly into JavaScript you could go over to mdn and look it up and learn

more about form data but if I pass the entire form element to it then what I get back is the data from that form this

form data object will give me access to each of the values of my inputs by using

a simple get method so I can say my first name and no we're not doing first name last name my email is equal to form

data. getet and then I can use the name property this is why name is so

important to put in our inputs I can use that name property of email to get the data from the form so let's go ahead and

console log our email I'll hit save and we'll put something in hit submit and

sure enough we're able to console log our email address okay so we're able to listen for the submit event on our form

we have a function to deal with it we're preventing the default refresh of the whole page we're getting the form

element from the current Target of the event we're then creating a set of form data we're able to get the information

from that form data and we'll notice that the form is still filled in so I'll have to manually call something like

form l. reset which is a method on form elements that allows me to reset the

form one thing to keep in mind as we go forward about this reset method when you're doing challenges and you run this

line of code it's going to work just fine and when you're doing it on your local machine or pretty much anywhere else it's going to work exactly as you'd

expect for some reason on scrimba in the recording it's not actually recording the form reset so I'll probably mention

at some point that the form successfully reset and it's probably not going to look like that in the recording but just

keep in mind that it really is working behind the scenes in fact I just reset this I'll go ahead and type this information in type in my super secure

password of password and I can hit submit and sure enough for me the form did successfully reset and then of

course instead of console logging our email we would gather the info from the form and probably submit it to a backend

this backend would be in charge of doing data sanitization and submitting that info to a database or in the case of a

signup form maybe sending a confirmation email or something like that awesome got a working form but you might be thinking

hey Bob this doesn't really look that great this seems to be bleeding into that realm of imperative coding as

opposed to declarative coding and you would be right but keep in mind that prior to react 19 it actually used to be

quite a bit more difficult to gather form information or maybe I should qualify that the traditional way of

gathering information from a form which used something called controlled components which we'll actually be

touching on in the next section was quite a bit more cumbersome than first of all what we're doing here and more

importantly what we're about to learn in the next lesson react 19 has introduced a much better way to gather form

information so feel free to play around in the code here as always and when you're ready we'll jump into the next

scrim if you remember we were talking about forms back in probably the original spec for HTML there was a

property or an attribute that you could add to your form called action and this is where you would tell where your

browser should send the information from the form to often times this would end up being for example a PHP file and the

code in that PHP file would then receive that form and process it save it to a

database return some kind of new HTML whatever it might be with our onsubmit

that we're handling here we're able to do a lot of this on the client side and that's pretty nice but we do find

ourselves handling a lot of things imperatively within our own code base for example if I'm handling the

submission in my Javas script of course I'm going to want to prevent the default of a full page refresh and since this is

a form that I'm submitting of course I'm going to need to get the form element and create some form data from it if I'm

submitting the form of course I'm going to want the form to reset at the end there's a number of sensible defaults

that we kind of just wish were being handled for us and in react 19 we can react 19 allows us to not only use a

regular action for a backend file if we need to like we have here but we also

can pass a function to it maybe instead of sticking with the name of the event

that I'm trying to handle like handle submit and onsubmit I'm going to go ahead and get rid of my onsubmit

entirely and maybe we just make this a little more declarative like this is my

sign up function now because I can pass functions to my form actions I'll go

ahead and pass this signup function and when you're passing a function to your action it doesn't receive an event

because we're not handling an event per se but instead it's just automatically going to receive the form data this is

awesome behind the scenes the action function is going to prevent the default for us so we can get rid of that these

next two lines of code Were Us trying to get access to the form data which it's already giving us so we can get rid of

both of those and it's going to reset the form for us automatically so I can get rid of that let's go ahead and

console log our email and just see if this really is all we need we'll hit save and oh that warning actually

brought up a good point we had our method of post but if we're specifying a function in the action then we don't

need to do that manually so let's hit refresh again I'll fill out this form and hit submit and check it out in our

console we have our email address and we were able to do that in a single line of code also the form reset and the page

didn't Refresh on submit if I sound probably unreasonably excited it's because I've had to do it in a much much

more difficult way for a really long time so bear with me and my excitement which probably seems pretty silly to you

but something feels so good about just going back to the native web with a little bit of benefits mixed into it

from react because I've been talking so darn much I'm going to give you a very simple Challenge and then we're going to

come back to our Chef Claud app and apply what we've learned over there currently we're just getting the

email from our signup form but we're going to need the password as well so I want you to get the password from the

form as well and log it to the console just to be sure that it came in correctly short and sweet I'll hand it

over to you all right easy enough I can get the password by calling formdata

doget and the name value that we chose for our password input is logically

enough password so we'll just say password and I'll console log the password we'll hit save I'll put this in

I've just been kind of mashing the keyboard for my passwords and so yep sure enough we get the password in

awesome of course there's a lot more that needs to be taken into consideration when it comes to forms but

for now this is going to be good enough to help us refactor our Chef Cloud app so let's jump into

that all right we're back with Chef Claude and your challenge is to use a form action instead of the onsubmit in

this handle submit function that we're currently doing in the onsubmit Handler we have on our form I want you to use

the form action capabilities that we now have with react 19 so I'll pass it over to you to finish this challenge you

might remember or as you were testing it out might have noticed that we are able to add items to our list but we actually

didn't even put our form reset down at the bottom here fortunately when we transition this over to use actions

instead we're going to get that for free so instead of onsubmit let's go ahead and set this up as our action and I'm

going to call this add ingredient we'll change the name of our function changing the name of the function by the way is

not required it just makes it a little more I guess semantically sensible so

don't worry too much about that okay we're going to receive the form data we don't have to prevent the default we

don't have to create our own form data we can leave this line of code in and

this line of code and we don't have a form reset from before but we should just get that for free let's go ahead

and clean up our challenge text hit save add oregano and I'll hit enter first and

sure enough that added to the list and our form cleared maybe all add basil and try clicking the button and same thing

awesome that was such a quick challenge that I'm actually going to take some time to tell you how things used to be

in react we're not going to dive deep into it but the way that we used to do form handling and react is we used to

track the state of every one of our inputs and on every input element we would add an onchange event handler

every single keystroke that happened inside of an input or the clicking of a radio button or checkbox or whatever it

might be any single change to the information in the form we would update our local react State instead of using

the internal state that already exists in forms which meant every single one of our inputs had to have an onchange it

also had to have a value property so that we could make sure the input's value or the actual text of the input

was correctly updated whenever State changed and this whole setup was called controlled components this was because

react was in charge of controlling the state of the inputs and the form in general and the truth is there are still

times here and there where you might find that useful for the most part you're not going to have to worry about

that and we can delete a lot of code compared to what we were required to have before now although Chef Claude

doesn't have any more requirements as far as our form goes there's still a bit more that we need to learn about forms

and react because as I've mentioned includ forms and react is a very common task so I want to make sure that I cover

those

bases even though our Chef CLA app isn't going to require these I wanted to cover

some other form input types just so that we have those under our belt in case we ever need them we won't be covering

every single one of the types but this will be a good way to get our feet wet with other ways of collecting

information from our users the first one that we should talk about is a text area element one thing that's unique about

text area is well first of all it's not an input type text area or anything like that it's simply its own element also it

actually isn't a self-closing it has a separate closing tag which is the text area closing tag the difference between

a text area and an input is that it's intended for longer form text you'll also notice that in the very lower right

there's a little handlebar for the user to change whatever size gets displayed

here here but you also can set a default size in your CSS is kind of the preferred way or there's a property

called rows and columns where you can change the size directly here in the HTML well I guess we're in jsx but it

has those properties still I'll go ahead and add a label for this one and maybe

since this is a longer form text we'll I don't know say it's some kind of description that the users going to be

entering in and we will need our HTML 4 because we are not wrapping the lab

around our text area although that would be a legitimate way to do it as well we'll say it's for description which

means we need to give this an ID of description and assuming we want to actually gather this information from

our signup function up above we will need to also add a name property which will also be description cool looking

good we'll keep this lesson kind of short and sweet because we are going to be diving into other input types that

have a few extra considerations we need to keep in mind but before we move on there is something that I remembered now

that I added to this code since we last saw it and that is this default value property in my case I'm adding this

default value simply so that I don't have to type new things in every time I submit this form when we come back

around to seeing what information we're getting in our form data it's really helpful when testing this not to have to

fill these values in every single time default value is a way to initialize this element with a default value and

this default value is still changeable I could change this to whatever I want but you might also be able to see some value

in the default value property if you were loading up a form that you needed to pre-populate with the user's data for

example I've seen apps where I go to maybe my profile section and if I want to change maybe my address it will show

me a form but it will pre-populate it or set a default value to the data that I had previously entered but still allow

me to change it and resubmit that form so that's all that's happening here with the default value I'll probably add more

default values to the other elements as I go on just so that it makes it easier to test submitting my form okay in the

next lesson we're going to jump into radio buttons and see how they can be a little bit different than the other

inputs that we've dealt with the next input I want to talk about

is an input of type radio we'll hit save

and see that we get nothing all that special here I'm certain this isn't the first radio button you've seen radio

buttons are used when you have multiple options for the user to choose from and you only want them to be able to select

one at a time let's put a label on this button so that it doesn't look so silly just as a circle sitting there on my

page and maybe just to show that it works totally fine to wrap our labels

around our inputs I'll go ahead and wrap a label around this particular input

let's indent that input by doing doing so I think we lose a little bit of neatness in terms of the structure of

our HTML but we also gain back some of the fluff that we have to add just to

associate the two together in this case I'm going to put my label text and for now let's just say label text after my

input that way once I've made another little change we're about to see my radio buttons will be able to align

neatly on the left side and the label will be on the right side even without any label text I think because of the

way my C SS is set up if I hit save we'll see that that's going to align to the left and I think that radio buttons

look a lot better if you have all of your radio buttons aligned on the left and then you have the label on the right

of course you can change that around and use some CSS grid maybe to get them all aligned on the right side but uh let's

just keep it like this and for now I'm just going to say label text cuz we're going to see what we're using this radio for and awesome we get label text now

let me go ahead and duplicate these so we have a few different options here and as I mentioned one of the standout

features of a radio button is that we're only able to select one of them however if we check I can actually select all of

these so why exactly is that well in order for them to be exclusive from each

other I need to give a name property to my radios but that name property has to

be the same for all of the radios that I want the user to only be able to select one of now I'm going to make these radio

buttons represent an employ employment status so I'll go ahead and give the name of employment status to all three

of these the same exact name let's hit save and now I can only select one of

these at a time selecting a different one will change which one it's selected of course one thing that I really like

to do when I have radio buttons like this is to surround them in a field set element so I'll go ahead and take this

closing tag and just wrap all of these in a field set and then do a format indent those and we'll just go ahead and

hit save oh and it looks like maybe we need to make a little change to our field set let me go ahead and add a

display of flex and a flex direction of column on that okay that looks better

okay so the field set gives us this little outline when we're inside of a field set we also can give a little

label to the entire field set with a legend property or element I mean and in

that element we'll go ahead and say employment status and awesome now you

can change the design for this this is sort of the default I've updated some colors and such but I'm not going to

worry too much about the rest of the design okay instead of label text let's go ahead and include our different

options we'll say unemployed part-time and

fulltime awesome and because they have the same name we can only select one of them at a given time time now there's a

couple things we need to take into account first of all before we move on in this text area I'm going to add a

default value and maybe I'll just say this is a description so we'll hit save

I'll go ahead and check part-time and hit submit oh and in our function we're only conso logging the password so

actually let me throw in a quick challenge here okay the challenge I want you to

try and do is grab the employment status from the form and log it to the console just when you're submitting the form

remember to choose one of the options cuz we haven't yet discovered how to create a default selected option however

before anybody jumps into this and starts pulling their hair out I want to give you a caveat or a note here to let

you know that it's not quite going to work the way that you might expect and we're going to fix what this problem is

so I just don't want to set you up for failure just know ahead of time it's not going to work quite yet so give this

challenge your best shot and if you'd like you can see if you're able to fix the problem that we run into when we try

to do it the way it currently is written go ahead and get started on this challenge okay well let's just give it

our best shot we'll go ahead and try to grab the employment status and that will

come from form data. getet and we'll pass in the name of

employment status is that the one we chose yeah employment status right here I'll just copy it and paste it just in

case and let's go ahead and try to log employment status and see what happens

so I'll hit refresh I'll choose part-time I'll hit submit and all we get

is on interesting so our radio buttons by default they don't come with their

own value per se or rather the default may not be exactly what we need in fact

let's hit save and to refresh the form and I'll hit submit and you'll see that the other option if we don't select

something is null but I'll go ahead and choose full-time hit submit again and now that value of on comes in when we're

creating radio buttons we need to provide a value property and this value is what we want the data to be when this

form gets submitted for example if we're here on the unemployed we might want this to say unemployed as the value

think of this value as the actual value that you might save to a database so

I'll go ahead and fill these in as well we'll say this one is part-time this one is full-time

we'll hit save we'll choose maybe part-time hit submit and now we actually get the value that we associated with

the input that we ended up selecting and that's the value that we were able to pull in from our form data okay that's a

lot of information that we just talked about and all we've covered so far is radio buttons however they're pretty

important and it's good to know some of their nuances that we run into the only other thing I want to touch on before we

finally move on from radio buttons is how we can automatic ly select one of these or I guess if you were pulling in

existing information and wanted to prepopulate the correct Choice instead of using something like default value

which is what we have used above instead we choose the input that we want to have

the selected option already and we use a different one called default

checked and we will set this equal to a Boolean value of true actually well

let's hit save we see that we automatically get fulltime selected I think we might be able to do the string

true and yeah that works as well but because we're here in react and we can put in real JavaScript values let's go

ahead and use a real bullion okay let's move on from radio buttons and talk about the radio button sibling which is

the check box a very close relative to the radio

button is a checkbox let me go ahead and create something very similar to this

actually I'll just copy this whole F set here let's change the legend to something where a user might select

multiple boxes maybe something like I don't know dietary

restrictions I'll go ahead and change all of these to a type of checkbox and

update the names let me get rid of the default checked that we had here although

actually I guess this is an important time to note that let me go ahead and hit save default checked does work the

same as it does with with radio buttons we can see that fulltime here has a check mark even though we haven't

selected that with checkboxes though because we can have multiple checkboxes selected at a given time I can put

default checked on multiple different items and so we can have multiple different things selected at once let me

go ahead and get rid of these default checks just for now actually I'll go ahead and leave it on that third one

we're doing essentially the same thing we were doing before so I will update the labels that I have here and let's

say maybe we have a dietary restriction of kosher let's say Vegan and maybe

glutenfree and I'll update the values as well remember when I submit my form whatever I put in the value if the box

is checked will be what gets sent to my form data so with this one we'll say

kosher and in this case I'm choosing a lowercase k here I guess it just depends

on what data you actually want showing up in your database that's what you would put here as your value we'll say

Vegan and the other value is down here so that will be gluten free okay so far

so good let's hit save we have our gluten-free checkbox already checked because of the default checked and let's

see what happens when we submit our form so up here I'm going to grab let's see

I'll just duplicate the employment status one we'll change this to dietary

restrictions let's see did I use an s yes dietary restrictions and so that's what I'll do my form data.

getet with and let's see what happens when I hit save and hit submit we look

at the console okay so we did get gluten-free showing up as one of the checked items what happens if I check

another one let's say kosher submit interesting I am only getting kosher and

actually Let me refresh this form to clear that out we'll do both kosher and actually let's just do all three submit

and check it out we are only getting one of our options showing up in the form data when we get it this is something

that I think is pretty unique to checkboxes and there's a really easy way around it the form data object that

we're calling this.get method on it also has a method called get all with a

capital A by including that if I hit save we'll check all three of these and hit submit now we get an array with all

of the values that we expect to be getting with a checkbox that can have multiple things checked at once

so when it comes to checkboxes they're almost exactly the same as radio buttons each one has the

same name property each one has a different value we can use default checked to automatically check it when

the form loads however if we want to get an array of all of the checked items

then we will need to use form data. getet all instead of just doget the fact

that we have to do this a little differently will play a bit more of a significant role in a lesson that's coming up very shortly on on how we can

more concisely get all of the information from a form but for now hopefully what we've done here makes sense as always please feel free to play

with the code that you see here and when you're ready we'll keep moving

forward there are a ton of different input types and it's certainly outside the scope of this course to talk about

every single one of them however I do want to cover the select and option elements just as one final Harrah here

with forms we'll talk quickly about submitting the form and then we'll kind of get off this little side trail that

we've embarked on and get back to our project and the topics that more closely relate to this specific project let's

say I want to add a dropdown where the user can choose their favorite color we'll go ahead and start with a label

like we usually do this time I'll go back to having a label that's separate from my select elements and here we'll

say what is your favorite color because my select is going to be a sibling

element let me just get that started I'm going to give an HTML 4 attribute to my

label and we will call it fave color and I'll have to give this an ID of fave

color okay so a select will give me the box but in order to have a drop- down

list with different options in it I need to use an option element I'll go ahead

and fill these out for every color in the royi Biff color spectrum

let me go ahead and hit save you won't be able to see this in the recording but if you were to come click on this form

and click the drop down you'll see a browser implemented version of this dropdown box which I'm sure you've seen

a million times by now a main thing that's different is in order to gather that information up in our function I

need to give a name attribute not to my options but to my select if we think

about it this makes sense because we need to gather the one chosen option and

the only place that we could give a name to that would make sense with that is the parent select box let's give this a

name that is also fave color however in order for each one of these to have its own value each one of the options needs

to have a unique value so I'll give each one of these a value property and I'm

just going to copy the color and I guess I don't need this to be uh curly braces like this we'll do a string pass in the

color and then I'm going to be particular I guess and lowercase each of these values since I've been lower

casing my values before okay awesome we'll hit save let's go ahead and choose blue we'll hit submit

and oh you know what I forgot to update this function let's not conso log dietary restrictions now instead let's

get fave color is equal to form data. getet fave color and then we'll console

log fave color okay let's try it again hit save go down to something like blue

hit submit and sure enough we're getting the value of blue with the lowercase b cuz that's what we set our value to for

that option now we can see that it's defaulting to the first item in that list if I want to change that I can

simply add to my select let's see that's right here default value and set it

equal to one of the values down below like Indigo now if I hit refresh we see

indigo is the default value that shows up you also might be familiar with select boxes where what it actually says

is something like choose your favorite color or choose a color we can achieve that same thing by creating a new Option

at the very top we'll give it a value of an empty string and we'll give it the text of something like choose a color

okay we're partly there and oh we're still showing Inigo let's get rid of our default value here actually I'm going to

leave this as a default value of empty string since technically our choose a color is the value of empty string and

so awesome that now shows up we actually wouldn't need this here I don't believe in order for it to show that since it's

the item in the top spot but it doesn't hurt to leave it there and lastly assuming we don't want a user to be able

to submit choose a color as their final answer here we can add a property to the

option that says that this is disabled if I hit submit now I'll hit save and in

my dropdown box and you will probably have to click into this form to see this but it says choose a color at the top

but it's grayed out it's not an option that the user can select we can still submit the form though we get a value of

null and so if I need this to be a required field then I can simply on my select add a required property we'll hit

save try to hit submit and we get a browser implemented warning that you might not be able to see here in the

recording but it says please select an item in the list so I'm forced to come down select an item and awesome as I

mentioned we're straying a little bit from our main topic of learning react but forms in react can be a little

complex fortunately as of react 19 now that we're able to use this form action

we can finally rely on forms to maintain their own State and to Simply collect the data using the form data object that

we get inside of the function that we pass to our form action as you can imagine if our form had say 40 or 50

fields it could become a bit annoying to have to select the data for every single one of them there is a quick shortcut

that we can use to more concisely grab all of the data from the form it's not a silver bullet sometimes you will need to

select all of the individual items by themselves maybe for example ex if you had to do some kind of Manual

sanitization of your inputs although in the end you would probably want to use something that was a little more robust

like using the Zod library but that's definitely a different discussion so let's see one way that we can more

concisely grab our data currently we are going through

every one of our inputs and grabbing the information from them one line at a time

and as I mentioned there are times when this may be necessary but if we had a a form that was 40 or 5050 or more

different inputs maybe first you would want to address why you have such a long form but let's pretend the size of the

form is outside of your control and you just need to Simply grab all of the data there's a utility that we can use built

into JavaScript called object capital O object. from entries all I have to do

here is pass in the entire form data object and let's see what we get if I

console log the object or the results from object. from entries I kind of gave

it away we'll hit save we'll submit our form oh I have to choose the favorite color and submit and we see that we get

an object back the object has all of the name values as properties in the object

and the values in the form as the values to those properties in the object if I'm

trying to build up an object to then send to a database it looks like I am most of the way there however if we look

really closely we'll notice and you know what I'm going to copy this object from the console since you can't

see my arrow down there and we'll just paste it down here okay we can see with

dietary restrictions what we get back is just a string gluten-free and remember sometimes with checkboxes we want the

user to be able to select multiples however if I do this and hit submit and

we look closely at the object that comes back we still have the same structure it just says gluten-free remember with

checkboxes I had to use that form data. getall in order to get the property from

there so I am unfortunately still going to have to do that let me go ahead and

save most of the data we'll just save it as The Returned value from object. from

entries and then individually I'm going to get the dietary let's just call it

dietary data and that's going to be by calling form data. get all and

separately I'm going to get the diet let's call it dietary data actually let me make this into a challenge it looks

like my old challenge text is up here anyway so we'll just clean that up and give you a new challenge I'm sorry that it's been so

long since I've given you a challenge hopefully nobody got too complacent in the meantime since we are on a bit of a

detour here this is going to be a fairly straightforward challenge I want you to see if you can remember how to grab an

array of checked items from the dietary restrictions check boxes you should be able to then console log dietary data

and get back an array instead of a single string all right get started on this

challenge I think it's more of a mini challenge at this point all we have to do is say form data. getall get all is

the key here we'll give it the name of dietary

restrictions and let's go ahead and console log it just to make sure it's giving us what we want you know what I'm

coming down here to change my default value to let's say blue just so I don't

have have to keep selecting that all right I'll select another one vegan hit submit and awesome we get our array of

selected items from our checkboxes now that I have an array I can combine the

object that I got with data with the array that I got with dietary data at the Key of dietary data essentially

overwriting what data. dietary restrictions used to be so I can just say maybe const all data is equal to an

object that takes all of the properties from data and then includes a property

called dietary restrictions and the value is going to be dietary data I also could simplify

this a little bit just by choosing to name this dietary restrictions instead and then I can go like that and I'll

just get rid of this console log because it's referencing the wrong variable name I guess before we assume it's all working out we'll console log all data

hit save let's select all three of these hit submit look at what we got and awesome if we look closely dietary

restrictions is an array that has kosher vegan and gluten-free in it okay let's finally be done talking about forms

let's get back to the main project that we're working on and start diving deeper into a topic that we did briefly see

before but now we'll actually take the time to understand it and that is conditional

rendering over the next few lessons we are going to be doing sort of a minseries on this topic called

conditional rendering and although it's going to span a few different lessons mostly we'll just be talking about what

it is and how we do it seeing multiple different ways that you can accomplish conditional rendering depending on your

use case and your needs fortunately understanding conditional rendering is not that difficult in our Chef CLA app

the user is first presented with a simple input and a button and only after the user adds some ingredients to the

list will they first be presented with this ingredients on hand header with the unordered list below it as it wouldn't

be as intuitive to have just an empty unordered list and this ingredients on hand with nothing after it unless

something is added to the list also after some ingredients are added we can actually set this up to be after a

certain number of ingredients if we want we then will present the user with this section down below that says to get a

recipe again it wouldn't really make sense to show this on the screen unless there were some ingredients on hand and

lastly we have an entire recipe that we need to display but we will only have that recipe after the user clicks get a

recipe and makes that roundtrip call to the anthropic API so everything in the

suggested recipe and the recipe itself that all needs to be I guess you could say hidden or not rendered to the page

unless we actually have a recipe to display so this is where conditional rendering comes into play as you can

kind of into it from the name it means that we render parts of our page based on a condition if that condition

evaluates to true then react will render that portion of the page if it's false

it simply won't be rendered and as a reminder when I say it won't be rendered I mean it it won't even be added to the

document you could search for it in the dev tools but it wouldn't be there at all I guess you also can set up

conditional rendering so that it hides elements that actually are on the page but for the most part we're just not

going to render it to the page at all if those conditions aren't met so let's dive into this topic of conditional

rendering and then we're going to come back to the chef Cloud app and apply what we've

learned here we're back in the Jokes app that we created in the last section and

I wanted to give us a challenge so that we could make it where the user could click a button and clicking the button

would display the punch line to get us started I have a quick challenge for you I want you to create a state that's

labeled as is shown and it will be a Boolean type that defaults to false and then I want you to add a button

underneath the punch line for each one of the jokes that when clicked will toggle the value of is shown back and

forth we're not going to worry at this point on any conditional rendering so just so we can more easily tell that

this is working I'm going to console log is shown but I won't hit save because it'll break your app okay your turn get

started on this challenge we're going to use use state from react so I'll make sure I import

react from react again a very common way that you'll see this done is simply to import used state from react just while

we're learning I'll keep it as import react from react so we can tell that this is state from the react Library

I'll create my new destructured array we'll say is shown and set is shown is

equal to react. use State and we'll create an initial value of false while

I'm still up here I can probably clean this out we'll create a function and

maybe we'll just call it toggle shown this isn't strictly necessary I could do an inline function on my button actually

you know what let's do that first so I'll create my button we'll have it say something like

show punchline I'll add an onclick to it this onclick is going to be a function

and this function's job is going to be to call set is shown we do care about the previous value of state so that we

can flip it from whatever it used to be to the new value so I'm going to say previous shown and this is going to be

an arrow function we'll say previous shown and then return the opposite of

previous shown now we can see this is why I like to do my functions elsewhere this looks a little too crazy for me so

I'll go ahead create a function toggle shown we'll take the code right here

paste it in and we no longer need this Anonymous inline function instead we'll just call toggle shown now notice at

this point nothing relies on is shown in order to be be displayed and so that's

why I have this console log here just so I can see that it's working we see that it's false but let's open the console

and we'll see something really interesting we actually see false five times I'm actually going to insert a

pause here and give you a chance to think why is it that we're seeing false five times Well if we go to our app.jsx we

can see that we're mapping over some data and for every item in this array we're displaying a joke component or

rendering a joke component means that we're calling this joke function if we go to our jokes data which we're mapping

over we can see that we have an array with five items in it so this joke component even though from our app.jsx

it kind of looks like we just have one of them the fact that we have an array means that however many jokes we have in

this array is how many times this function will get called which means inside of our joke function this console

log is going to get called one time for every instance of our joke component I'm guessing that was probably clear for

most of you but I just think it's good to reiterate stuff like that okay let me hit show Punch Line and we only get one

new entry in our console and we can see that it was set to True perfect okay for

this next challenge I'm actually going to do this a little bit backwards let me start by typing out the challenge now

your challenge is to make it so that this paragraph only gets shown if the value for is shown is set to true the

reason I say this is backwards is because we haven't officially learned how to do this but when we were just

finishing up with this app in the last section I left in this little snippet of code here that shows you exactly how to

do it we're going to talk about why this works in the next lesson but for now you have a perfect templates to help you

complete this challenge oh and uh let me just make sure this is clear this is the challenge so go ahead and give this your

best shot and then we'll talk through it well in this previous example we had been talking about jokes that may not

have a setup but were just kind of a oneliner joke that was more of just a punchline and inside of our jokes data

we included a joke that didn't have a setup property and so what we did is we surrounded our jsx in a set of curly

braces and we included first a condition this double emper sand and then the

thing that we wanted to render if this condition had a truthy value so we can

do this exact same thing let's surround our jsx with a set of curly braces that

will allow us to evaluate some JavaScript and I can start by saying if is shown is equal to true then or and

this paragraph again we're going to talk about why this double emper sand Works in this case but first let's go ahead

and hit save I'll click show punchline we can see that the punch lines are missing now I'll click show punchline on

this one and awesome the punchline shows up now many of you are probably thinking I can simplify this is shown is already

a Boolean so I don't need to compare it to the value of true if is shown as true

we get exactly what we need here and just to show that's working maybe this time I'll hit the punch line on the

second joke and because this state is being saved inside of the joke component each one gets to maintain its own State

we're actually going to be diving deep into that idea a little bit later but for now it's simply means that I can

click show Punch Line on just this one joke and it's the only one that will show the punch line not only that but I

can actually click the button again and it will hide the punch line we're going to address that user experience in just a minute so this lesson has gotten a

little bit long already but before throwing you into a challenge I want to talk more about why this works we're

more familiar with the double emper sand being a way for us to compare one value with another when we're doing something

like an if else if statement as opposed to in this case where we're using it for conditional rendering so why exactly

does this work that's what we'll be touching on

next we're pretty familiar with using the double mersand when we have something like an if statement I don't

know let's just say true and true and you know if we do a console log

here uh everything was true we often think of this emper sand as a way to

check the truthiness of the thing on its left and the truthiness of the thing on its right if both of them evaluate to

true or a truthy value then this if statement will run however that's not

entirely true even though this condition would suggest otherwise what's really happening here is a left to right

evaluation inside of our if statement the computer will first evaluate the truthiness of the leftand argument of

course the Boolean value true is truthy so then it sees there's a double emper understand and because the item on the

left was true it's going to continue evaluating through the next expression if this one also is truthy then we know

the whole thing will evaluate to a single true value and the if condition will will run this drives with our

understanding if we were to change the second one to false like this we can think of it as a left to right operation

okay that's truthy and well that tells the computer that means that the item on the right hand side also needs to be

truthy then it reads false and it says oh nope this whole thing will evaluate to false and the console log will not

run so I guess this would have to say everything was not true so does it jive with our understanding if instead we

were to change this first one to false if we go from left to right we might think well this is false we then get the

double emper sand it notices that this is true but because both items on the

left and right were not truthy values it evaluates the whole thing as false however we can see that this isn't

precisely what's happening let me go ahead and change this true this is not something that you'll see very often but

we'll change it to an operation that we can know if it ran or not let's say this

code is running I'm actually just going to comment out this console log so it doesn't become become confusing let me change this to True we'll hit save we

can see that in the console we do get this code is running okay well what happens if I change this to false I'll

hit save and the console log did not run at all what's really happening is that

left to write operation it notices that this is false it sees that this is a double emper sand but because the first

condition already evaluated to false it kind of short circuits the rest of this

line and it doesn't need to even eval valate this because it knows that it's going to evaluate to false or some kind

of falsy value so in JavaScript this console log won't run at all of course

if we were to reverse this we put the console log first and then say and false

we will get the console log running because it's the first thing that it evaluates it runs the console log

function it sees it's a double emper sand and it says well this was not a falsy value so I'm going to continue

evaluating and then it gets false it returns this falsy value to the if

statement here and it becomes false so this property of the double emper sand short circuiting the rest of this line

is exactly what we're taking advantage of when we're using conditional rendering in the way that we're doing

here the double emper sand can be a quick way to either display something or not display something if is shown is

falsy then this expression will just return a falsy value and and in our case

because isown is a Boolean react will interpret this as meaning nothing should be rendered in this spot however if is

shown is truthy then the double emper sand says just return whatever's on the right side here if this is falsy then

the whole thing will evaluate to false and nothing will get displayed but as we know since we wrote this code we're not

returning anything falsy we're following up our double emers sand with what we want to get displayed so that was kind

of a long- winded way to talk about this but hopefully that helps make some sense of why the double emper sand Works in

this case and as I mentioned it can be a good way to either conditionally render something or not render it at all in a

little bit we're going to quickly touch on a shortcoming of using this method for conditionally rendering but before

then I want to get your hands more on the keyboard and have some practice so that's what we'll do in the next

lesson this is a pretty straightforward challenge your task is to only display this H1 if there are unread messages in

state right now we have two items hardcoded in here we're not actually displaying the text of these messages

anywhere so it doesn't matter what it is as long as there are items in that array it should display this H1 and if there

are no items in the array then for now we're just going to have it be a blank page this H1 won't be rendered at all

let me put those back in there and I think that's everything you need to know so go ahead and get started on this

challenge well in this case unread messages is not a Boolean value and even

an empty array is a truthy value so we couldn't simply wrap this H1 in curly

braces and say if unread messages and display the H1 because let's go ahead

and hit save we do have the H1 showing up but even if it's an empty array we still have the H1 showing up it's best

to be really explicit with what exactly we're looking for in this case because it's an array we need to know if the

length is greater than zero so if the length is greater than zero it will display this message let's actually get

rid of this Blank Space here and we'll say unread messages. length and this is

wrapping a little bit so let me go ahead and put these on their own lines like this hit save and awesome we have two

unread messages and then of course if we added to this array it would update that number so we've seen how using this sort

of short circuited way of using the and operator gives us a chance to determine whether something should or shouldn't be

rendered at all however it does turn out there are some limitations to this and to highlight those limitations I'm going

to give you another challenge I'm fabricating this scenario

a little bit here just to prove a point but for this challenge if there are zero unread messages I want you to display a

paragraph not an H1 but a paragraph that simply says something like you have no unread messages in this case I do want

you to use the and Operator just like we did above and you'll just do it right here below the previous one that we did

and as it says the logic is going to be the opposite of what we have for the H1 so that if there are unread messages it

will display this H1 and if there are not unread messages it will instead display the paragraph that you're about

to create for anyone who's already familiar with conditional rendering and react I know this is a silly exercise

I'm building up to another way that we can do conditional rendering okay take it

away I can just copy the logic here down below and in this case I'm going to say

if the unread message count is equal to zero then I want to display a paragraph

that and I'll just copy the text here okay we'll hit save we have two unread messages if I get rid of those in state

okay a paragraph you have no unread messages perfect okay well what we've done here is highlighted an issue where

we essentially have an if else statement if unread messages. length is greater than zero then we display this H1 but

the only other option is if the length is equal to zero because it's an array we can't have negative length in it

however it's a little bit verbose what we're doing here we are repeating oursel for this unread messages. length check

and in this case we're only ever displaying one item or the other so as you can probably tell that I'm driving

towards a point that in this case when we're trying to decide between displaying one thing or another thing

The Logical and operator is not going to be our best choice not only that but let me actually clear up this Challenge and

clear up this that we just did but it can be really tempting to see something

like unread messages. length and try to infer a truthiness out of it in

JavaScript the value zero is considered a falsy value and so it's tempting to say that if unread messages. length is a

truthy value then I want you to display this H1 and we might Pat ourselves on the back and think that we're doing a

great job here you know we might hit save see that it looks like it's working and ship it however let's see what

happens if I empty my array and hit save again we simply get the number zero

displayed when this evaluates to the number zero react will choose to display that zero instead of just considering it

a falsy value and not displaying anything so unless we're very sure that we're being explicit in our condition

and ensuring that that expression will evaluate to a real Boolean value and not just a truthy or a falsey value there's

potential for bugs to show up in our code like having a random zero floating somewhere on our page kind of in summary

the and operator can be a good way to quickly either display something or not display it if you use it make sure that

your expression will always evaluate to a real Boolean otherwise there's another option that we can use to conditionally

render things and react and that's what we're going to be talking about

next we have Kind of a Funny UI bug right now where if we click show

punchline it does show the punchline but the button still says show Punch Line furthermore clicking show punchline

again actually hides the punch line so knowing what you know now and what we've learned with the and operator to do

conditional rendering I'm going to put in a pause here and I want you to think about how you might change the button to say hide punchline instead of show

punchline of course only at the appropriate time when things are already shown I'm not going to type this down as

a challenge cuz I'm not necessarily expecting you to write the code for it although you're more than welcome to go above and beyond and do so so see if

you're able to figure out a way that you could change the button to say hide punchline if the punch line is already

shown one way we could go about this is duplicating this button having one that says show Punch Line and one that says

hide punch line we then would have to conditionally render one button or the other button based on the is shown

property so I would say if is shown is true and uh well actually let's see if

is shown we want this to say if not is shown so if it's equal to false then we want to say show Punch Line and if is

shown is true then we want to display hide punch line and we should see that

this will work it says show punchline we click it and now it says hide punchline if you think about it when the state

changes react is actually removing the old button and putting a new button element in its place but we can already

tell by the duplicated code that we can probably do this in a better way and the better way that we can do that is by

using a Turner in this case I wouldn't even have to duplicate my button so I can just get rid of this and the only

thing that's really changing about this button is that first word so let me back this off I'm going to get rid of

everything that we just added and instead of saying show punchline I'll go ahead and determine what this word

should be in JavaScript so I'll put a set of curly braces to jump into JavaScript and I can use a Turner to say

if is shown is true then I want this to display the following string let's see if it's true

then I want it to say hide but otherwise I want it to say show let's hit save and

we'll click show punchline and awesome it now says hide punchline not only that but because we are only changing the

text of our button and not actually swapping out the entire button element itself after clicking it we still have

tab focus on that button so I could hit spacebar and it would toggle that button back and forth to hide and show the

punch line for that one specific joke so that's kind of an extra benefit because we're not swapping out the entire button

element but just changing the word on the button so now that we know about the Turner there is one last thing that I

want to talk about and that is that there is a little bit of push back in the react Community to using the and

operator at all because of that little bug that we saw before where if your expression evaluates to a zero it

actually would display a zero on your page bugs like that can be completely gotten rid of if we simply choose to use

a Turner instead so instead of an and operator I'll use a question mark and as an alternative in my else basically the

second part of my Turner or I guess the third part the first part is the expression second part is the truthy

value that gets returned in this third part we'll say null it's a little bit of extra typing but it is kind of a

prevailing thought in react these days to do this just to avoid any potential of having that Zer show up on the page

or just generally having your expression maybe not evaluate to what you think it's going to evaluate to so there are

some who would say just don't use the double emper sand at all and just always use a tary with null as your alternative

option and we'll see that this is working exactly as we would expect we're currently showing or hiding the punch

line correctly the button says hide punchline and show punchline I think what I'll probably do is just leave this

example with the double emper sand and I'll leave this one with the Turner just so you see the alternative and between

these two options with the and operator and the Turner I would say probably 90 95% of your conditional rendering needs

will be met with that if you do have something a bit more complex like if based on whatever value you have you

might display more than three or four things in that case it might be better just to put your logic up here inside of

your component to determine either what element should get displayed or what the text should that gets displayed do all

of that logic work outside of your return above your return I should say save it in some kind of variable and

then just display that variable down below because we're just dealing in JavaScript here you also could do

something like create a function that takes a parameter and determines what the output should be and then inside of

your JavaScript expression down here you could simply call that function and that

function would be in charge of returning the jsx or in this case just the string that should get displayed there's a

million ways to do it and it's kind of hard to go over every single one of them because well there's always a lot of

ways to solve the same problem everything that we've covered here so far is going to be plenty for us to get

back to our Chef claw app however before we jump back into Chef CLA I do want us

to get some hands on the keyboard here and practice conditional rendering we'll also have a quick conditional rendering

quiz so stretch out those finger muscles or do whatever you need to do to be ready to complete a challenge

okay let's give this one a shot your challenge is to display the correct kind of text inside this H1 if there are no

unread messages so if this is an empty array it should display you're all caught up if there's exactly one unread

message in it then it should display you have one unread message and message will be singular you don't have to display

the singular word there actually let me put the quote on the other side there and if there's more than one unread messages then you want to display you

have and then the number of unread messages but the word messages should be plural there's definitely more than one

way to solve this problem so so give it your best shot don't be too concerned if the way that I do it is going to be

different than yours just see if you can get it to work so I'll pass it over to you to work on this challenge one way I could choose to go

about this is to decide which H1 I'm going to display one of these three based on the conditions that it has I

also could potentially choose to do a Turner but because I have three different options here it would likely

have to be a nested Turner which I personally kind of despise nested taries

I think there's always a better way to do things in the last lesson I briefly mentioned at the end that one thing you

could do is to set a variable for what text gets displayed and then run your logic here above your return in order to

determine what that text should be if you chose to conditionally render your H1s using an and operator or some kind

of Turner that is 100 % okay but just for the sake of seeing it a different way I'm going to go ahead and create a

new variable I'll set it as a let variable so that I can change it and maybe let's have this say uh we'll just

say text and I'll just leave it undefined for now then I can just use a regular if block to say if messages.

length is equal to zero then I'll go ahead and set text equal to this message

that says you're all caught up else if my messages. length is exactly equal to

one we'll set text equal to this message instead and that needs to be a string

and not have this formatting here and otherwise we are certain that it will be

greater than one so we will just copy this down here we'll change this to messages and I'll use

messages. length inside of my text which means I need to use a template string so

I'll go ahead and put that interpolation there and change this to a template string and the word messages is plural

okay so by the end of running through this logic text is going to be exactly the text that I want so I'll put a set

of curly braces and just say text let's clean up the challenge hit save and we

get an error and that's because I'm checking message. length not messages. length Okay cool you have two unread

messages let's lower this down to one one unread message perfect and if we

make it an empty array you're all caught up if this logic were to get much more complex than this I might put this

inside of a function and say something like determine text we can simply put

all of this inside and then we'd want to make sure we returned the text and

actually by doing that I don't need to save a separate variable so I could simply say return this string and we

could just do that in each of those cases and then all I would have to do is call

determine text with my set of parenthesis there to immediately execute it upon this getting rendered let's just

see if that's working so okay we get you're all caught up if I add a single item back in here then I get you have

one unread message and a second one two unread messages perfect again I actually

didn't expect anybody to do it this way if you did Bravo in kind of thinking outside the box I just wanted to show

that there's a lot of different ways to handle this and now that you understand the concept of conditional rendering

simply using JavaScript to determine what should get displayed to the screen or if something should get displayed to

the screen at all the whole world of possibilities is going to open to you in how you actually accomplish that task

just to shift gears a little bit I do want to give a quick quiz about conditional rendering so that we can

start thinking Less in terms of the code and More in terms of the highle concept and then as I promised we'll get back to

our Chef Cloud app and apply what we've learned

before moving on let's do a quick quiz about conditional rendering just like before I'm going to put in a pause here

I want you to actually click in and type down your answers it's a great way to think outside of the specific syntax

that we've been working with so go ahead and answer these questions and then we'll go through them

together okay number one what is conditional rendering in a highly Dynamic web application we often have

changing dat data or changing local state and we may choose to display something different or not display

something at all depending on that state so one way we might answer this is that

conditional rendering is when we want to only sometimes display something on the

page based on some kind of condition

okay we also talked about two of probably the main ways that you'll see conditional rendering being used one is

by using the and operator so when would we want to use that well it's ideal for

either displaying something or displaying nothing at all so it's good for when you want to either yes display

something or not display something when it comes to either displaying option A

or instead displaying option b that's when number three a Turner is best used

so we can say it's good for when you need to decide which of two things to

display and yes you can use nested taries to determine any number of things

that you might want to display but personally that's where number four comes in what if you need to decide

between greater than two options on what to display in which case the world kind of opens up to you you could use an if

else if else conditional and of course in that case you can have as many else

ifs as you need or you might decide to use something like a switch statement or

kind of implicit in this answer is basically any other way you might want to do it okay great job on this quiz

let's finally get back to Chef Claud and apply the conditional rendering that we've

learned all right that was a long Sidetrack on learning conditional rendering but as I mentioned it's

something you're going to be doing quite a bit and we're going to apply it right now in our Chef Cloud app we have the

input and when we add ingredients let's just say testing it displays the list of ingredients it seems like it's

conditional rendering but what's really happening is we have this unordered list that is always being rendered to the

page and it simply has no list items inside of it which is why it looks like nothing's there but what I'm going to do

is paste in a more finished version of this that includes this ingredients on hand the list of ingredients like we

already have and then this little call to action at the bottom that says ready for a recipe so let me go ahead and

paste in some pre-written code we'll walk through it so that it's not too jarring and we'll see that we are in

dire need of some conditional

rendering all right I replaced our simple unordered list with this new section and let's take a second to walk

through it I know sometimes if someone just throws a bunch of code up here it can be a little bit jarring and I don't want to lose anybody here first of all I

am going to make this a little bit bigger just just so we can maybe separate those words a little bit so

what we've added into the section first is a little H2 that announces the below list is going to be the ingredients we

have on hand of course it's a little bit weird because it's just a colon and then there's nothing after it we do have our

unordered list currently being rendered to the page but because our ingredients list items is an empty array nothing is

displaying and then we just have this little call to action that says are you ready for a recipe generate a recipe

from the list of ingredients and it's got this get a recipe button there's no onclick on it yet we're going to get to

that in a little bit but clearly what we have here is not a great user experience it's really cluttering up the page with

irrelevant information at the current starting point with having no ingredients in our list oh and I almost

forgot I do have in the CSS some Associated class names and styles which is why it looks like it's styled already

okay let's apply what we've learned with conditional rendering and make it so that ingredients on hand and this ready

for a recipe section don't show up unless there are items in our ingredients list I'll type this out as a

challenge just to buy some room I'm actually going to minimize this for now if we want we can bring it back up or

even make it really large so that we get a little bit better spacing for now again I'm just going to minimize it okay

your challenge is using conditional rendering I want you to only render this entire section if there are ingredients

added to the list of ingredients assuming you went through the conditional rendering sections that we

just finished and were able to do the challenges this should be a prettyy straightforward challenge for you there's always more than one way to get

things done especially in react so as long as when you first load the app this whole section doesn't appear and when

you add an ingredient it does appear then you should be golden of course when you do that the ingredients on hand

should have one item in the unordered list all right your time to shine we can know if we have ingredients in our list

if the ingredients array that's being held in state has a length that is greater than zero and so I will surround

my entire section here in a set of curly braces and I can set up a condition that

says if ingredients. length is greater than zero then I want to display the

section we learned two main ways that we can do this I think I'm just going to use the double emper sand and let's see

if that's working first okay well that section is gone so that's good let's hope it comes back we'll add oregano to

our list and perfect we get it showing up on the page as I mentioned you want to be

careful when you're dealing with the double emper sand if you have a habit of not being quite as explicit as using the

greater than zero so that this will actually turn into a Boolean and you're relying on the fact that ingredients.

length of zero is a falsy value and might Short Circuit the rest of this you're probably going to be disappointed

we can see if I hit refresh I get a zero actually showing up on the page so you can either make sure that you're always

very explicit and this is evaluating to an actual Boolean or you can use a Turner if you want to be extra cautious

so you can say if ingredients. length is greater than zero then display this but

otherwise display null and we'll see that this is working as well I can add oregano that shows up but if I were to

rely a little more heavily on the fact that ingredients. length of zero is falsy then I wouldn't actually render a

zero instead I would get the expected behavior and I can add oregano and then get the rest showing up on the page

there are just different schools of thoughts you can choose which ever one you want I think I'll go ahead and stick

with the double emper sand and simply remember to put my greater than zero in

here we'll just make sure that's working again perfect just to really drill this

in we are going to do another challenge but we will do it in the next

scrim towards the very end of this project we are going to be sending this list of ingredients to a real AI API so

that it can determine a recipe that we could make given the ingredients that we passed to it however if we just have a

single ingredient the chef might not really know what we're supposed to do with that it also would probably

generate a recipe that has a bunch of ingredients we don't have which might still happen anyway but try to imagine

telling a chef to make something and the only ingredient you have on hand is oregano however currently we're

prompting our user if they're ready for a recipe by having a single ingredient on there so maybe for the sake of our

users Ultimate culinary experience let's update our app so that the get recipe

container div which is this one right here will only get displayed if our ingredients list has at least four items

in it because fewer than that and we might just not get very good results again this is super similar to the last

one but I think it does help illustrate a little point that we'll see in just a second okay go ahead and get started on

this challenge we're doing essentially the same thing that we were doing before we're just going to surround this div in

a set of curly braces and put a condition and that condition is the same as the last one well almost the same

we're looking at ingredients. length but we want it to be greater than three this time and I'll put my little short

circuit and operator there let's clean up the challenge text and hit save and

give this a try I'll just add in some oregano maybe chicken some jalapenos and

maybe we have some cream of mushroom soup awesome okay with the fourth

ingredient added we now have this ready for a recipe thing showing up down at the bottom and that experience seems a

lot more reasonable to me all right well we do still have additional parts of our site that we need to render including

this entire suggested recipe section so what we'll do is put a bit of a placeholder in its place for now before

we start integrating any kind of AI and later we can replace it with the real thing so let's Jump Right In and tackle

that next challenge as you know once the user has

input a few ingredients they're going to click this get a recipe button that will send send an API call out to the

anthropic Claud API or as we'll see there's other options as well and return a recipe that we can display down below

we're not quite ready to reach out to the API but I do see a chance for us to make some progress in our Chef Cloud app

that will give us a chance to practice both the creation of state which honestly it's been a minute since we've done in this course and some conditional

rendering which you're probably pretty sick of doing by now so I'm going to give you this multi-part challenge that

will kind of be a placeholder for now and then we'll be refactoring this and building upon it as we make this app a

little bit closer to its final form the first part of your challenge is to Simply create some Boolean State you can

call it recipe shown and it's just going to represent whether or not we've gotten the recipe back from our AI Chef to

start it out you'll default the value to false then I want you to go over to recipe code. MD this file here and

you're just going to Commander control a and Commander control C to copy the entire contents here what I've done is

taken the response that I've gotten back from an AI when I was testing this out and I've wrapped it in all of this HTML

or I guess jsx code so you're going to grab everything here head back to main.

jsx and down below you're going to paste it in place of this comment right here if you hit save at that point it's going

to display it on the mini browser but the next part of your task is to make it so that when the user clicks the get a

recipe button it will flip the recipe shown state from false to true and you'll use conditional rendering to only

display that entire recipe code content if recipe shown is true a couple things

first of all yes this is just a placeholder in the future we will not be using recipe shown to determine if the

content should be displayed or not instead we're going to save the response from the AI in our state and if that

response is not null then it will do the same thing it'll display the recipe content section secondly and this is

more administrative you'll notice that I just hardcoded a few options in here so we didn't have to add four different

ingredients every time we wanted to click get a recipe okay I think you should be all set up to get working on

this challenge it's a little bit longer it has a few more steps than normal but I know that everything here should be

something that you're capable of doing so I'll pass it over to you to work on the challenge all right first let's

create our Bull and state so I'll do that here we're going to create recipe shown and and use set recipe shown as

the state Setter function and that's going to be coming from react. State it's just a Boolean and we're defaulting

it to false I'm going to kind of clean these up as I go just to buy a little bit of room okay now we need to go grab

the markup in recipe code. MD I'm just going to grab and copy everything come back to main. jsx and it's going to look

a little bit bloated but we'll just stuff it all here inside of this file and I think I'll do a quick format here

yeah there we go for anybody who is feeling pretty concerned that this file is getting pretty long and trying to

attend to a few different needs for our app you have a very good point and we are going to be addressing that very

soon but for now we're just going to have to live with the Clutter a little bit okay so that was step two copy and

paste pretty straightforward all right when the user clicks the get a recipe button I want to flip the recipe shown

state to true I'll go ahead and create a new function we'll say toggle recipe

shown this will call set recipe shown it will look at the previous value of shown

and flip it to its opposite we could have also done this as an inline function it's pretty straightforward but

I kind of prefer this way personally and now let's come down to our get a recipe button and add an onclick Handler to

toggle recipe shown okay that should be everything from three and then we are doing some conditional rendering so we

will surround our entire Chef CLA recommends portion let's see that goes

all the way to this section we'll surround it in a set of curly braces and we'll say if recipe shown is true then

display this section all right let's clean this up hit save cross our fingers

and hope for the best we've already got our ingredients there cuz they're hard coated in let's click get a recipe and

look at that we can scroll down and see the recipe that Chef Cloud recommended for us or at least the one we're

pretending it recommended for us well that's not entirely fair this actually came from the AI it just didn't do it

right now awesome this user experience is actually turning out pretty great however I'd say there are three main

issues that we have yet to solve and this is going to set us up for what we're about to learn for the rest of the

section the first one is kind of a developer experience issue that that we're experiencing here and that is what

we just talk about this file has gotten quite long I mean in the end it's only 81 lines of code that's not actually

that bad I've seen much much longer react components than this but it does kind of feel like we're dealing with a

few different things first of all this whole recipe shown section it could probably be its own component and the

same goes for the ingredients maybe not I could see an argument for keeping it here but for the sake of practice we're

going to move this into its own component I guess we theoretically could do the same thing with our form

I imagine I'm probably just going to keep this the way it is but we have some cleanup to do so that our code is a

little bit easier to reason about in doing so we also have some topics to learn that are regarding where State

should live in our react component hierarchy how we can pass State down to the components and still have them be

able to change the parent State and just generally understanding what all that means in the first place another maybe

more user Centric issue that we're facing is if I'm scrolled to the top here let's go ahead and hit refresh I

can't scroll down cuz my recipe section isn't displaying currently if I click get a recipe well I don't have a lot of

visual indication that the recipe is ready other than suddenly there's a scroll bar and so if I start scrolling

then I realized oh it actually did respond with the recipe so that user experience could be improved by having

the app simply scroll down for us to let the user know that the recipe is ready for them we also eventually will want to

add some kind of loading state currently clicking get a recipe just immediately displays everything here but when we're

dealing with the API it's going to take some time for that response to come back and we want to give the users some visual indication that it is trying to

work in the background and lastly I guess this is both a developer and a user experience well we want to get the

recipe from the real AI API not just from this hard-coded thing that we currently have so we've made great

progress awesome job on the challenges that you've had so far I hope that you're still keeping up with them

learning to code should not be a lonely task you should be reaching out to the superactive scrimba Discord server and

asking your questions there getting help from people it is totally worldwide so at any time of day or night there is

always someone awake and active on the scriba Discord server feel free to play around with the code that you've written

here and when you're ready to dive in we will first start tackling how we can improve the developer experience by

offloading some of this code to separate components

here we are back at our very simple counter app I even removed the text that was saying how many times would Bob say

the word state in this section and that's because I just want to focus on the core elements that we need now I'll be the first to admit this challenge is

pretty contrived essentially the task is to take this H2 and put it inside of its

own component and then pass our count value through props to that component so

that by the time you're done everything should work exactly the way that it is currently working read through the

specific directions here that should give some hints as to what you need to do and I guess before we start I'll just

promise you that this isn't just meant to be busy work it's actually less about getting repetition and practice in this

time and more about building to a point so go ahead and get started on this

challenge I think I tend to like working backwards on stuff like this so I'm going to cut out the H2 and render this

fictional count component and we will go ahead and pass it a number prop whose

value will will be the count that is being held in state okay that does not exist so let's pretend like it does for

a second and import it we'll just import it from a file that we'll call Capital C count and we'll create that file count.

jsx and there it is we'll go ahead and set this up we know that we want it to take props

because we need access to that number prop I'll go ahead and return if I can

spell it right will return the H1 that I cut out earlier but now instead of count I don't

have that anymore cuz I'm not in a file where state is being created instead I'm receiving that state through props and

specifically a prop called number all right let's see if we made any mistakes we'll hit save and okay it seems to be

working as we would expect okay as I mentioned that was pretty contrived a component that just renders an H2 is

probably Overkill for most instances I suppose there are times when you want your H2 to always be styled a specific

way and I don't know maybe have some specific functionality attached to it but the reason that we did this

challenge is because I wanted to take a chance to talk about rendering let me go

ahead and add a console log and we'll say app rendered and then I'm going to

do a similar console log inside of my count of course this time we'll say

count rendered we have briefly discussed what rendered means in react and I don't

plan on doing a super deep dive into everything that happens when react is rendering components but the crucial

things for us to understand at this point is when we talk about something being rendered we can think of it as the

function of that component being run here we're rendering the app component

which essentially tells react hey I want you to go to the app functional component the function and just run

through the code there run that function so if we go to app we see it's going to be setting up some state it defines a

few functions here that we use within the body of this component in our case we also put a console log here and then

we return some jsx which represents the elements that will eventually get turned to Dom elements that get put on the page

and then it renders jsx which represent react Elements which eventually will get turned to Dom elements that get placed

on the page and that's what the user actually sees so let's see what happens when I hit save and open my console okay

we see we got app rendered so the app function ran because our console log ran

so we know that it ran and our count rendered console log the one that's here also ran and that's because inside of

the app component we are rendering or creating an instance of the count component which means react ran the

count function and therefore our console log ran okay well let's see what happens when I change the state inside of my app

component so I'll go ahead and let's click plus and check it out in our console we got app rendered and count

rendered again both of them ran again so changing the state inside of our app

component is rerunning this function although a really interesting thing to note is that the count value is now

updated it's not rerunning it and setting it back to zero that's one of the main features of state it maintains

its value from from one render to the next which is happening behind the scenes in react if this were just a

plain function and nothing else special about it then of course our value would keep getting reset back to zero but that

isn't happening not only that but our count rendered again as well and let me

scroll down a little bit so you can see the instance of the count that we have and I'm going to insert a pause to give

you a second to think why is it that count rendered even though it was only state in the parent component or the app

component that changed try thinking through that see if you can make sense of why the count component

rendered well intuitively we probably think well it's because it relies on this count value that exists within the

app component in order to correctly display the number on the page whatever the current value of state is and that

is true it's a bit of a partial truth but it makes sense if we go to the count component if we didn't rerun this

component with a new value for props do number then what gets displayed would

never update now the reason that I say this is a partial truth and I'm starting to flirt with the line of going outside

the scope of what I really wanted to teach in this course is because the truth is any components that we have

inside of our app component in this case will get rendered whether they rely on

the state or not they will by default get rendered by react there's a little bit of controversy about this and quite

a bit of misunder understanding the truth is even if you have a component that doesn't technically need to render

doing so by react is super super fast and it's not something that often leads to any kind of performance issues and if

it does there are things that you can do to improve the performance again that's outside the scope of this course it's

most important to know that if we have a state change inside of one component like we have inside of our app component

react will render its own elements that that component is in charge of rendering

and it will render all of the child components that are nested inside of the

return of this component if those components have their own children to display those also will get rendered I

go quite a bit more in-depth on this topic in my Advanced react course here on scrimba so once you finish this

course assuming you are planning on continuing to learn react that will be a great resource for you but in the

meantime what we've discussed here is good enough for us and opens a door for us to now start talking about State and

props and how they relate to each other and how data gets passed around in a react

application let's look at a slightly more realistic example than the counter that we just saw back in our contact

card if you remember we had our little star icon and clicking the star would fill it in or empty it out essentially

toggling the is favorite property on our state object but let's say we wanted to move this star element to not just be

the button with the image ins side that we have here but into its own component so that we could reuse it in other

places in this app so at this point I'm going to type out a challenge for you to start working on okay your challenge is to move the

star image which is actually this button with the image inside into its own

component which you'll call Star the star component should receive a prop called is filled that it uses to

determine which of the two icons it will display as a reminder you will need to make sure that you take the two import

statements and move them into the component that you create the star component while you're working on that

I'll want you to get rid of this onclick this is what I mean here when it says don't worry about the ability to flip

this value quite yet so in doing so you can actually just get rid of on you know what I'm just going to get rid of onclick right now here after you've

created that star component here in our app.jsx file I want you to import and render that component in place of the

button element that we have here and then make sure you pass the correct prop to it so that it will work as we expect

or at least it will reflect the value of contact. is favorite so you can switch this value to true just to make sure

that that star suddenly fills in go ahead and get started on this

challenge I think I've done a lot of working backwards where I cut this out and render a component that doesn't

exist so maybe this time I will start forwards I'll create a new file called star.

jsx and inside star actually before I forget I'm going to import these two

lines here I don't need them in here anymore so we'll go ahead and import

those and then I'll create my component I do know that I want this to

receive props because I'm going to have an is filled prop sent to it and then I'll say return we'll come back over to

app let me grab this button and paste it in the return of the star component and

format and we used to be looking directly at the contact object in state but we are now going to be receiving

essentially this value of is favorite from props so this will be props Dot and

I think we said to call it is filled so let me go ahead and change everywhere that we had contact. is favorite to

props dois filled and over in app I can now import that component so I'll just

do it right here we'll import Star from dostar and render it in place of the

button and I'll hit save I still need to pass the prop to it but let's just see oh it's going to struggle a little bit

because I don't have that prop pass to it so let's go ahead and add is filled is going to be the value of contact. is

favorite and oh nope I do still have a bug let's see reference eror star empty is not defined and oh yes I have this

right here this line is no longer needed but I do need to put that logic over in

my other component so let's see I know what I'm doing here let's clean up that challenge and go back to Star and okay

perfect right here we'll paste in that line of logic and yep it was expecting

star icon and we're no longer looking at contact. is favorite we need props dois

filled I have star filled and star empty let's try again okay cool now we get our app back up and running or I should say

it's partially running because I got rid of my onclick on my button we can see that clicking the star doesn't actually

do anything here we do need to test it though let's make sure we change is favorite to true and hit save cool our

star is filling in so now we just need to try and think how are we going to make it so that our nested component the

one that is now inside of the star component how can we enable the star component to make a change to its

parents state in fact I'm going to put in a pause here so you have a chance to think through that you don't necessarily

have to write any code you're welcome to if you want but think for a second how might we be able to add some

functionality back to our star component so that clicking it will then change the state that lives here inside of app I

remember when I was first starting out I thought well I just need to add an onclick Handler to my star component and

let's just see where that takes us so I'll go ahead and add onclick and we'll just pass in the toggle favorite

function hit save and click the button and not quite it's still not working why

do you think that is take a second to think why is it not yet working for

us remember how the properties that we're adding to our jsx elements map

directly to the Dom elements that exist in JavaScript in JavaScript elements that we pull from the Dom they have a

class name property that we can change and Dom elements like an H2 or a regular

button or an image or any of these regular Dom elements they also have a Dom property called onclick well we're

not quite directly working with a Dom element here we're working with a custom component in react any of the properties

that we put on our custom component in react they're chosen by us and so

despite the fact that we named this on click with a Capital C just like we would if it were a regular bare Dom

element or in this case a react element because it's jsx which gets turned into

a Dom element this onclick is simply going to be yet another prop that we need to receive inside the star

component so that it will work this on click is just another custom property or

prop that we're passing to our star component which we would then need to receive as one of the props in order to

actually do something with it inside of my star component this is where my regular react element of the button that

I want to add an event listener to exists so in order to get the onclick here I need to put it on top of my

button so I'll go ahead and use onclick with the capital c and the value that I'll pass to it is the function that I'm

receiving through props called onclick one thing that I sometimes do to clarify

exactly what's Happening Here is I'll go to my custom component and instead of giving it the exact same name as what

would be placed on a regular Dom element I might change it to something that's obviously more custom like handle click

doing so won't magically fix it I need to come over to my star and realize that I'm not receiving a prop called onclick

anymore I'm receiving a prop called handle click so I'll change just a handle click and let's just see what

happens I have my star I click it and it empties out awesome we've talked about how we can pass any JavaScript data type

down through props and functions like we're doing here are no exception we're passing this function down to our star

prop so that we can put it on the native element this lowercase b button element

so that it can correctly listen for the click event and run this function running this function will still

interact with the parent state in order to change it so over the next few lessons we are now going to dive a

little bit deeper into State and props the react hierarchy and what the component tree looks like and all kinds

of really fun stuff we'll get lots of chances to see different ways that we can structure our state and our props

and as a reminder all of this is bringing us back to our Chef CLA app where we had kind of a long component

and a desire to move some of those sections of the component to their own individual components that then get

rendered by the main parent component so without further Ado let's jump in and start seeing how react handles State and

props and the component tree at this point I think it's helpful

for us to look at how we pass data from one component to another in react let's look at a sample diagram of a react

application we can imagine that the rectangles closer to the top represent parent or grandparent components and the

lines simply represent that that component is rendering an instance of another component below it the name of

these components isn't important in this example the name of these components isn't that important it's just important

that we understand the hierarchy that's here as you're building your application you might realize that this bottom

component here is in need of some states so that the user can change something and react will reender that component as

you continue building you might also realize that there is a sibling component or in other words a component

that is also being rendered by the same parent that is also in need of the state that you just created in its sibling

component we're going to do a challenge in this code in just a second but this is a perfect example of this in our

index file we're rendering an app component the app component is rendering a header component and a body component

and as we were building this in the header component we initialized some state for our current users username we

set it equal to Joe and that's what's being displayed up here in the upper right however as we we started building

out our body component we realized that we need access to the currently logged in user so we can fill in this text

where it says welcome back and then blank we want this to say welcome back Joe so think for a second is there any

way that we are able to pass the state that we created from this component over to its sibling

component well as it turns out in react no we can't this isn't how data Flows In

react in react data can only flow downwards it only works in one direction

from a more parent component down to Children components so take another second to think how could you make it so

this component that is currently saying data please can get access to the state from its sibling

component because data only flows downward the easiest thing that we could do is simply to bump that state up to a

parent component and then pass that information down through props this way both of these bottom level components

can have access to the information that it needs well what will inevitably happen as you continue to build out your

app is you'll find that you have yet another component that needs access to that information and once again we find

ourselves being unable to pass information from the component that we just gave state to to its so-called

sibling component that now needs access to that state and it's important to note that we certainly can't go from any

child component up to a I guess you could call this an aunt or Uncle component because there's not even a

reference in the code from this bottom component to any other component in the hierarchy so this also is not something

that we can do which means once again we are forced to pull our state up to a higher level and pass down through props

to the components that need it the information from that state as you can imagine this can get a bit cumbersome

over time and there are a number of different solutions that can help us avoid having to pass props many levels

down tools like context which is built into react or thirdparty libraries like

Redux or Zoo stand which were created to help this data management problem all of

those topics are outside the scope of this course and so we are just going to be sticking with State and props however

I can offer a little plug for my Advanced course here on scrimba where we do dive into context and we learn how we

can use context to avoid having to drill props through so many layers of our component tree so let's apply what we

just learned about moving State up and passing its information down through props by working on a

challenge here we are in our header component which is currently the location of the state that we created

for our username your challenge is to raise this state up a level and then pass it down to both the header and the

body components through props and then the last part of this challenge will be to make it so that in the body component

we aren't looking at this Blank Space here but instead we're able to render the username in its place go ahead and

give this challenge your best

shot in this hierarchy we can imagine that this box right here is the app

component and it is rendering the header and the body but right now our state is

living down here in the header so as we saw we need to lift that state up so

that it will live in the app component let's go ahead and cut this state out

we'll go over to the app component and we will just put it right there and I had already imported react from react in

these components just in case you wanted to play around with putting it in different locations but at this point we

can get rid of those and I guess while we're here we'll clean up this challenge text too okay let's come back here where

we just put our new state and we can pass that state down through props we'll just maybe call it a prop of username

and we'll set it equal to the value of username from State and now let's see

what happens I'm going to hit save I'm probably going to get an error that talks about how username is not defined

so we can go through and fix those in our header we are referencing username but we don't have state here anymore

instead we are going to be getting this from props so I can just add props do

username in its place and let's see if that works yes our header has Joe in it

let's go over to our body we will also accept props here and once again instead

of these hard-coded underlines we are going to get props do username Moment of

Truth hit save and perfect our body also says welcome back Joe we can also double

check that this is working by changing Joe to something else like Bob and perfect it changes in both locations

with only one state change understanding that data flows in a single Direction

and that direction is always from parent to child components or downward in the tree can be extremely helpful for you as

you start working on architecting your react applications I think the last important thing to touch on with this

before we move on is to know that it's best practice to keep your state as locally defined as it needs to be in

other words if this component down here on the bottom were the only one that needed State then that's a great place

to put state if its sibling needs access to that state then moving it up just one level is the best way it might be

tempting to think well I'm going to stop refactoring this I'm just going to shove my state at the top of my application

and then pass it down as many levels as I need to but as a rule of thumb that's generally not a good idea and if you do

have state that is truly Global across your entire application that's usually the time to start looking at one of

those alternative solutions that I mentioned like context Redux or zoo or something like that okay with this under

our belts I think it is time for us to do a round of challenges to help us really cement in what we have been

learning about when it comes to props and state and react

this is the beginning of a series of challenges that we are going to work on so that we can reinforce what we've

learned in the past up until now and so we can prime ourselves to learn some new

information and we're just going to be building a silly little series of buttons that actually was inspired by my

roadter Pro which is what I use for mixing the sound from my microphone and it has these eight buttons over on the

right side that are kind of fun pastell colors and they are just for doing sound

effects I literally never use those buttons although I think they're programmed with sounds let me see what

they do the funny thing is while this is

recording I actually can't hear what it's doing so I'm going to turn that off we've got some funny sounds over here

the point is when I press these buttons they light up and when you press them again they turn back off and so that's

the inspiration for the project that we're working on the first part of this challenge is first to initialize some

state with a default value that is the array of pads that were pulled in I called them pads because they're

technically called sound pads so don't let that be confusing if we go to pads. JS where we're playing this in it's an

array of objects they have an ID a color which we're going to use eventually and an onv value which we're also going to

be using eventually for the purposes of this challenge you should find yourself only needing access to the ID although

I'm not going to tell you why yet that's going to be part of your challenge so you'll be creating some State inside of

this app you'll initialize the value of that state with this array that we're importing this is honestly kind of a

strange thing to do we're going to see exactly why we're putting it in state later but then what I want you to do is

to map over that state array and to display each one of them as a button element I've already written some CSS

for you so it should show up in a 2x4 grid and as it mentions here don't worry

about the on Prop or the color property quite yet once you've mapped over that array you'll put the elements right here

or I guess if you want you could just map over it right here inside of the markup so go ahead and give this one Your Best

Shot all right first things first let's go ahead and create some State we'll call these I guess pads and we'll use

set pads as our state Setter function that'll be equal to react. use state of

course I need to import react in order for this to work so let's do that not impro let's import react from

react and initialize this with the array of pads okay that is part one part two

let's go ahead and create some I don't know maybe we'll just say button

elements and that will come from pads. map for each pad I'm going to return a

button element I'm going to use a set of parentheses so I can do an implicit return on the next line and we'll bring

in our button and one thing I always find myself forgetting to do is to actually render

my elements after I have created them so let's go ahead and do that now we're going to have a little error or a

warning I guess oh you know what uh pads to that's funny I chose a bad name here

because that's exactly what I'm calling my objects coming in you know what you probably chose a different name for this

I'm actually going to change the name of this one to pads data just so that I can still call this pads inside of my

component okay let's see if we hit save and get the warning I was expecting yeah each child in the list should have a

unique key prop and that's because we're mapping over it we need to make sure that we provide a key and fortunately I

gave you the IDS for each one of these so that's what we'll use in this case because we manually did it we know that

they're unique so let's give that an ID so or a key of pad. ID we'll hit save

that warning goes away and awesome okay this is really just to partially reinforce what we have been working on

up until now and also to set us up a little bit more to learn about State and

some ways in which we will often times find ourselves dealing with State inside of a react application great job on this

challenge let's jump into part

two okay sorry if I led you astray before we move on to part two of this challenge we actually need to spend a

little bit of time to finally learn about inline Styles in react this isn't

something that we use terribly often in HTML but in HTML you can provide an

inline style directly on your HTML attribute by using the style attribute

whatever I put inside of the quotes inside of this text will get rendered by the CSS engine and so I could say

something like background Das color colon and I don't know let's do

something crazy like red okay I'll hit save and we see that it's applying and

actually this inline style is taking precedence over the CSS rule that I already have changing the background

color of the body let's go ahead and undo that it's a little bit of an eyesore we hit save okay that's a little

better we can do a very similar thing in our react code anytime we have a jsx

element that is going to be turned into a native n element basically anything that is a real HTML element we can pass

a style prop to it however because we're in jsx we're not going to set this equal

to a string where we say something like background-color but instead we're going

to set this equal to an object now I have found this to be a tricky thing for beginners in react if you remember when

we do a set of curly braces inside of our jsx it first puts us into JavaScript

so this is not setting it equal to an object it's simply saying I want you to evaluate some JavaScript inside here the

JavaScript that we want to evaluate in here is an object and so I need my second set of curly braces in fact

sometimes what I end up doing just to avoid that confusion is I'll create a separate variable let's call it Styles

and set it equal to an object and then replace that kind of silly double object looking thing with my object that I

defined elsewhere you definitely don't have to do it this way it might not be that confusing to you to just have your

object nested inside but let's just see what it looks like like this now I'm creating this object in JavaScript so if

I want to access the background color an important thing to remember is that I need to use my CSS properties as the

camel cased version of those properties first of all because well it won't make sense for us to have a key that tries to

do background- color but perhaps more importantly we need to remember that we

are working inside of a Javascript file even though it looks like we're typing HTML if you remember in regular Dom

JavaScript if we wanted to get an element we'd say something like document. getet element by ID something

and if if we wanted to alter the style of that we would say do style and then we could access the background color

property of it and set it equal to something the reason this is camel cased is because that's how they have it set

up in Dom JavaScript and so I need to camelcase my CSS properties I think you

understand that let me go ahead and get rid of that and let's just see that this is working we'll remember we're styling

the button elements right now so if I change this to the string red awesome we

get our red button all right well in this case we're just hardcoding a color to change the

background color of these buttons however usually in react you'll find yourself doing something like this

adding an inline style when you need it to be something that's more Dynamic let me show you an example I'm actually

going to clear out the button Styles there and we can just get rid of this

object and I'm going to set up a little challenge for you and I want us to imagine that we want to enable a feature

for for our app that allows it to receive maybe a prop called Dark mode

let me actually put these on their own lines just to buy myself some room okay

so here in our index. jsx file this is where we're instantiating our app component and let's go ahead and imagine

that we are adding a dark mode feature to our app and we want this to either say true or false let's go ahead and say

true for now and we will come over to our app component and we'll make use of

that incoming dark mode prop to change the background color and well really I

mean that's something I want you to do so I'll type this out as a

challenge okay these are still read from the previous time we refreshed let's go ahead and change it or save it so that

it updates and your challenge is to use a Turner to determine what the background color of the buttons should

be based on the incoming dark mode prop if it's set to true then set the

background color to this color and if it's false then set it to this color go ahead and get started on this

challenge well we're passing a dark mode prop to our app component but we are not

receiving it at all so let's go ahead and grab props and you know what as a reminder I think what I'll do this time

is I'm going to destructure this immediately and just grab dark mode directly from the incoming props object

either way is totally fine I just wanted to remind us that this is an option let's go ahead and create our Styles

object we also could have done this in line directly here in our button and we'll change the background

color camel case two and then we'll take a look at dark mode we'll use our Turner

here we'll say if dark mode is true then I want it to be this color and otherwise

we'll have it be this color lastly I need to include my style attribute here

and we'll set it equal to the Styles let's clean up this challenge text hit save

okay so they are dark because dark mode is set as true and if we come over here

and change it to false they are light awesome hopefully you can start to see that this can be applied in a lot of

different ways the way that we've done it here is pretty simplistic we're going to apply this idea to our soundpad over

the next couple lessons and we're also going to see how we can do Dynamic class names feel free to play around with this

and just experiment with the different kinds of things you can do dynamically with your styles for example maybe you

make it so that if there's an even number of pads that are coming in from pads data then they display in one color

and if it's an odd number then you display it in a different way I don't know the world is your oyster doing

stuff like that though is one of the best ways to just explore what's possible really exercising your

curiosity is going to be one of the best ways that you can learn so play around as much as you want when you're ready we

will move into part two of our sound pads challenge

these buttons are looking a little bit boring especially if we compare them to the buttons on the roadter pro that are

nice and colorful and bright so let's address that now your challenge is to First create a separate component that

we'll just call pad and replace this button element with that new pad component I want you to pass this pad

component a prop called color whose value will be the color property from our pad objects that we have and inside

the pad component that we're about to create I want you to apply an inline style to the button and maybe that

wasn't entirely clear when you create the new pad component you're going to take this button and that's what will be

returned from the pad component I want you to apply an inline style to that button so that it can set the background

color of the button to the color that we're passing to our component we're not yet dealing with the on property we're

going to be doing that soon you might have to read through this challenge a couple times there were some things that I skipped out on to give you a chance to

figure them out on your own and so I'm going to pass it over to you now to work on this

challenge all right I'm going to copy this button we have a bit of change to make we'll create a new file called pad.

jsx in that file let's go ahead and set up our component since I copied that button

I'll go ahead and return that directly and I'm going to remove the key because

I'm not going to be doing any repetition here inside of the pad component but instead we'll be doing that in app.jsx

let's go ahead and import our pad from the file called pad and we'll replace

our button with an instance of this pad component we don't need a closing tag here because it's going to be self-

closing and yes the key can stay on here that should fix the issue with needing a

key actually I'm trying to think if this would be broken let's hit save and okay yeah we've got our buttons on the screen

okay so that is number one number two let's pass the pad component a prop called color okay let's do that right

here color is equal to pad. color and we are passing the pad component a color

prop but we are not receiving it at all so let me go ahead and receive props and

we could either do our inline style actually yeah let's just do our inline style right here on the button we'll set

style equal to an object and that object needs to be inside of the first set of

curly braces also it's important to remember that we don't want to call the this Styles or something else weird

currently we're dealing with the actual button element so we need this property to be correctly spelled okay inside this

object I'm going to set the background color equal to props docolor and before

I hit save let's go back over to app we'll see how we're doing we passed the color prop and we applied it inside the

component we'll deal with on soon okay let's clear some of this text out and

cross our fingers we should see a little bit more of a colorful display here all right let's hit save and that looks so

much better sorry for any of my OCD friends who are wishing that the order was exactly the same I'm kind of feeling

that pain too well the order is the same it's just in a different orientation and

the way that I marked down the buttons was left to right and top to bottom I don't know I did it in a weird way I'm

sorry still our buttons are looking great in the next part of the challenge we're going to finally make use of that

on propop and apply some something similar to our Dynamic styles that we have but instead this time it will be a

dynamic class name so once you have made sense of what we've done here and you've had a chance to play around in the code

let's jump into that next part of the

challenge oh no our buttons are not lit up anymore and that's because I added some CSS that turns them off by default

or in other words it just adds this opacity of 0.1 by default to the button

however I did give us a way to include an opacity of one and that is if our button is to have an on class name let

me bump this up here and we'll see if the button is supposed to be on then it will have this full opacity and the

colors will be nice and bright but I need you to work to make that the case

so part three of this challenge is to update the code so that if the button is on or in other words if the data says

that on is true then the button should get a class name of the string on this

is even a little more vague than last time so I'm hoping that you've been paying attention in doing the challenges

if not that's okay go back try them again it should be a good primer for this challenge so I'm going to insert a

pause here and you can start working on challenge part three in order for this component to

know whether it's on or off we have to pass that data in to our pad component

just like we did with the color so I'm going to add a new prop called on and set it equal to the value of pad. on

remember this on property is coming directly from the pads data well maybe I should say indirectly from the pads data

we're saving pads data in state as this value of pads that's going to be the

same thing we're going to talk about why we're doing that really soon in an upcoming lesson and so this pads is the

array of objects and we're mapping over it so each one of them has an on property we're passing that down to our

pad component so so let's go ahead and receive it in props and we can always do something like conso log props Doon just

to make sure that's coming through and we see that we did get eight instances of this console running because we have

eight instances of our pad component and if we were to map this closely to pads. JS we'd see that it is in order as we

would expect okay let's close the console get rid of this console log and in order to add a dynamic class name I

can access the class name prop that I would pass to my button or attribute I

guess that I would pass to my button but this time instead of hardcoding a class name here I can evaluate some JavaScript

there's a few ways that I could do this I could say first I need to check props Doon and if that's truthy or true in

this case then I want to add the string on as my class name otherwise I guess I

could do an empty string this should work so I'll hit save and

awesome some of our buttons are turned on and let's see it's buttons number 1 3

4 and eight if I were to come here we'd see that 1 3 4 and eight are the ones

that matches perfectly okay now instead of an empty string Just for information sake I could put null here and that

would work as well now some of you may have tried to use the double emper sand as we learned in conditional rendering

to only include the string on if props Doon is truthy and let's see what happens I'll hit save our buttons are

working but let's check out our console it says that it received false for a non bullan attribute class name remember

when we're using this double emper sand if this is a falsy value it will return whatever that value is and in this case

it returned false and so it's like we were setting the class name to false and react wasn't super happy with that in

fact it even has a super helpful message that says if you used to conditionally omit it with the class name condition

double ERS value pass class name condition question mark value otherwise undefined instead and oh that's an

interesting way to do it using undefined I guess since the documentation or the warning says to do that maybe instead of

using null we'll go ahead and just follow what they said I think null would also work just fine here all right let's

save our warnings gone awesome great job by the react team for including such a helpful warning great work my friend

again play around with this code as much as you want and when you're ready believe it or not we still have more to learn with these sound

pads over the next two lessons we are going to be seeing two different ways that we can architect this silly little

app that we're making with regards to having multiple of these pad components

and having some state that controls whether or not they are turned on or off we're receiving their initial values

through this array here but we do want the user to be able to click them and have that onv value flip from True to

false or false to true so in this lesson and in this challenge we're going to see one possible way that we could do this

and in the next lesson we'll see another way we could do it and we'll talk about which one is likely the better option

for us so what we have right now and I've created this diagram to make this a little easier to comprehend we have our

app component which is where we are importing our pads. JS data we're

mapping over that array of data which in this case I've simplified to only show an on property we're mapping over that

array and we're creating our pad components of course we have eight of them this diagram has four for space

sake and as we're mapping over the array of pads we are passing down to it a prop

called on which passes the correct Boolean value down to each of these components those components are then

using that on value to determine whether or not the class name of on should be

displayed and we can see we're doing the same with color but let's just focus on on for now the first option for how we

can have these pad components control their own on state is by initializing new state in each one of these

components we would then take the value of props Doon that's coming in from

above from our app component and set that as the initial value in our state

for each one of these components then we would have a function defined inside of the pad component code

that that would allow it to flip its own value from True to false or vice

versa of course because we are rendering multiple instances of this pad component

each one would have its own state which react would be keeping track of and clicking each one individually would

change just that one component's value in state so let's implement this by working

on this challenge your challenge is to create some State inside of the pad component which will control whether

it's considered on or off to initialize the state for the initial value of that

state you'll use the incoming props Doon value then you'll need to create an

event listener so that when this pad is clicked it will toggle from on to off or of course the other way around and by

the end everything else should already be set up so that clicking the pad itself will make it flip and you'll be

able to turn them on and off each individually so go ahead and get started on this

challenge we need the use State Hook from react so we're going to import

react from react and let's just initialize it right here we'll just say

this is going to be on and set on is equal to react. use State and the

initial value is not just going to be me deciding to hardcode something but instead we're going to set it as the

value of props Doon let's clean this challenge text up I already know what I need to do so I'm going to have a

function that I'll choose to call toggle and and it's simply going to call the set on function it will need to know the

previous version of it and just flip it to the opposite so we'll just say the opposite of preon and then I will add an

onclick Handler to my button which calls toggle fairly straightforward how we

have this set up at least let's hope it works I'll go ahead and click these and oh of course I missed one last

thing I don't want to be looking at props Doon I just want to be looking at the state of on let's try that again and

awesome look everything's working perfect okay well this seems pretty darn

straightforward so why would I care to try a different way of doing this as I

mentioned there's more than one way we could approach this problem there's probably more than just two ways even as

there very often is in web development and programming in general so in the next lesson I want to see another way

that we can structure this and my goal here isn't to First teach you a bad way of doing it and then teaching you a good

way it's simply to help drive a point home when it comes to the interaction between props and state and just

architecting react applications in general as always play around with the code as much as you need to in order to

understand what we just did if you want it doesn't hurt to scrub back to before I did this and try it again on your own

from scratch when you're ready we'll move on

there's actually a name for how we set this up in the last lesson where we're taking an initial source of Truth this

array mapping over it and creating components passing information to that component through props and then the

most relevant part to what we're talking about here setting State based on the initial value of the incoming props and

then of course the reason that we would set State internally is so that this component would be able to change that

state the name of that is called derived state which makes sense it's deriving its initial State based on incoming

props well as it turns out you probably don't need derived State this is a

screenshot from the Legacy react blog and you can see in a couple places it warns you that this is an old version of

their blog but in reality the information on this page still holds water pretty well today you can click on

the screenshot if you want to read more about it but we're going to be talking about the biggest problem with derived

state which is that you can end up with multiple sources of Truth you see the

way that we have this written we have the state living in the app component which is supposed to represent the

current state of all of the pads but in reality once we derive State inside the

pad and allow it to update itself as soon as any of these pads gets clicked it's going to be out of sync with the

parent state that we had and because of that we have two different sources of Truth on its face this is probably the

most straight forward way to get something that looks like it's working so I can click these they appear to be

updating just fine and maybe that's all the features we want at least for now

however because we have two sources of Truth certain potential features in the future suddenly become a little bit more

difficult to add for example let's imagine that we wanted to include a button down here that simply said turn

all of the pads off because this exists outside of the individual pad component it would be

here in the app where we'd add that button maybe just right here down below the rendered array of

pads however actually implementing this feature would involve some kind of crazy

seeming workarounds and that's because if we were to Simply set pads and turn every one of those pads off well our pad

components wouldn't care they're not making use of this pads array state in

fact let me take a second to implement that feature at least how it should be working if everything were working the

way we'd expect just to I guess prove a point that it's not going to work okay

so here I've included a button that says turn all off clicking the button right

here will run this turn all pads off function that function is running this

console log just so that we can see that it's running and then it's calling set pads which if we look is the first time

we're calling set pads and updating this pads array in state it looks at the previous array of

pads and then it Maps over them and basically says just give me all the data from the previous pad just so we don't

lose the color and such but then it changes on to false for all of them let

we hit save we'll click turn all off and we can see our console log is running but of course our pads are not turning

off don't worry too much about the implementation details of this function we're going to be writing something very

similar to this but the point I'm trying to make is if we need any kind of control over all of the data in these

pads then we are going to be better off structuring our code in a different way so what we're going to do is we're going

to remove the state from the individual pad components and as such they won't need to update their state so we'll be

able to get rid of those toggle functions and instead we're going to make use of the state that already

exists inside of our app then we will still create a toggle function inside of our app which gives us the ability to

toggle one of the objects in this array and will update the local state of this aray inside the app component by using

set pads because we're updating this local state it's going to reender all of the pads and almost all of them will

receive the same on Prop that they received before except for the one that got clicked the way we'll know which one

got clicked is by passing this toggle function down to each of the pads when

the pad gets clicked it will send a signal up to the parent component it will tell it which pad got clicked based

on some ID number that will pass to it the toggle function will update that one item in the array everything will get

rendered and that one item in the array will then be different from its previous value and so it will flip now believe me

I know this sounds more complex and that's because it is however this is the best practice in react when you're

dealing with state in this way it's better to have a unified source of truth

because now we don't have a separate source of Truth on each pad they are simply reflecting this single source of

truth that exists in state on the app component now I'm going to give you a challenge that will get us part of the

way here and then we'll be working through the actual implementation details of this toggle function together

so let me go ahead and first I'm going to get rid of this turn all off code and then I'll include a challenge text

here okay your challenge is to First create a toggle function and for now all it needs to do is log clicked to the

console then I want you to pass that function down to each of the pad components and set it up so that when

that individual button gets clicked it will run the function that we passed to it all right I'll hand it over to you to

work on this

challenge all right let's do this we'll create a function that we call toggle and it's just going to console log

clicked then when we're mapping over our array of pads data we will add let's

just call the propt and we'll set it equal to the function toggle okay we'll head over to our pad component and now

we're receiving a prop called toggle and well look at that that's the same function name we gave it here let's go

ahead and delete this and then instead of toggle this will be props do toggle we're going to lose the ability to flip

that state but that's okay let's go ahead and click it and okay we're getting our console log running so this

is been a great way for us to get a high Lev overview of the approach we're going to take but it feels a little bit like

this scrim has gotten long so in the next lesson we're going to talk about how we can implement this toggle

function so that instead of just console logging clicked we can make it toggle the state of the button that was

clicked we're currently passing the toggle function which we defined in our app component down to every instance of

our pad component currently all it's doing is console login clicked and that

is definitely working of course that's not the ultimate goal now one thing

that's important to note is that each of these pad components has access to props do toggle the toggle function that we're

passing down to it but because this toggle function is defined in the parent component there really is only one

toggle function it's not like we've duplicated this toggle function eight times which means there isn't any

built-in connection for the toggle function to know which button triggered this function I think technically we

could try to grab the event and use something like event.target to figure

out which button it was that caused the click event but as you become more experienced in reacts you're going to

learn that accessing Dom nodes like this is kind of a code smell it just doesn't

feel right it's not really the react way to do this so let's say in our toggle function

we receive the ID of which button was clicked then we would be able to look

through the array of our pads find the one with the ID that was clicked and

flip its onv value to the opposite of whatever it used to be in fact sometimes

what I like to do is write this out as sort of pseudo code or comments in this case so we'll say map over the pads

array if the current item has the same ID as the one passed to this function flip

its on value okay so let's start thinking about this we're passing the toggle function

down and if we come to our pad component we have a tiny roadblock first of all I

can't just say well now I want props do toggle to take a parameter because if you remember when we first learned about

event handlers we don't want this set of parentheses here it's going to call it as soon as this function runs so I'll

hit save and oh of course I got rid of my console log to demonstrate that let's say toggle

function okay let me hit save okay we see that immediately without me even clicking it it ran this props do toggle

function that's not exactly what we want and I guess a second problem is

even if we could do this we don't get to choose what gets passed as a parameter

to our event handler functions this is something that's built into the Dom it will always be the event that gets

passed to these functions so how can we work around this so that we can pass an

ID we don't have this ID defined anywhere we're going to get there in a second but how can we write this so that

we can pass an ID to this function instead of it automatically receiving an event object well a super easy way to

work around this is to say I'm going to create an anonymous inline function here and this is the function that the event

handler will run this is the one that will receive the event as its parameter I don't need this but the only thing

this function will do is run props do toggle and now because I'm outside of the event handler function I can pass

whatever parameter I want to this function okay so all we're missing now

is this ID and then of course the code for the toggle function how can I get access to this ID

well you might be thinking hey we're passing the ID down through this key prop well there's one little problem let

me come here and console log props dokey and I'm going to get rid of my console

log for the toggle function we'll hit save and we get an immediate warning that says hey key is not a prop you

can't access it it's going to be undefined so don't try to do that if you need to access the same value then you

should pass it a different prop okay so we can't access prop stock key but of course Nothing is Stopping Us

from passing another prop let's call it idid and we'll pass pad. ID just like we

did with key now over in my pad component I can console logs. ID and I

get my one through eight these are the ID numbers of these eight color pads perfect so now instead of passing

the ID I can say prop. ID we'll get rid of this console log let's go over to our app and console log the ID that we're

passing to this function hit save click it and look at that that was number six 1 2 3 4 5 six

perfect should be 1 2 3 and so forth awesome everything's working and now

inside of our toggle function we have access to which of the elements in our pads array was clicked and we can start

executing our plan here and you know what I was planning on doing this one

for us but I feel like I've been talking for way too long so I am going to type this up as a

challenge all right we're stepping up our game a little bit I did briefly show you an example of what we're going to be

doing here earlier but I definitely didn't expect you to memorize it so this is going to be a bit more challenging of

a challenge than we've done before but don't let that discourage you I know that you'll be able to do this it's

definitely one of those opportunities where you might want to turn to chat GPT or Claude or some coding assistant or

ask in the scrimba Discord Community if you need a little extra help as opposed to just skipping ahead and watching me

do all the work you could say it's where the rubber hits the road this is really where the progress is made and I did try

to give you a little bit more step-by-step instructions instead of being vague like I've done before so the

overview of the challenge is essentially to make everything work again but the steps to do so is I want you to call set

pads and update the state of the one pad that was clicked based on its ID to do

that you're going to map over the previous pads array and if the current item that you're iterating over has the

same ID as the one that is passed to this function then you're going to return a new object with all the

previous values staying the same as they were if you need to refer back earlier

in the section to how we update an object in State this would be a good time to do that make sure you return a

new object where all of the other values stay as they were but the on value will be flipped to the opposite of what it

was before if the IDS don't match then just return the previous item as it was

completely unchanged take your time with this one it's completely okay if this takes extra time

extra brain power it's completely expected I know you can do this one I'll

hand it over to you to work on this challenge all right let's clean this up to buy ourselves a little bit of room

the first thing I'm going to do is call set pads I need to know what the previous

array looked like so we'll say preve pads and this will be an arrow function

and I think the thing that makes us more challenging than some of the other challenges is that we're going to be

then calling pre pads. map and whatever we return from pref pads. map is the

array that will replace the original pads that we had thus setting State and

rendering all of the pads in this array but the part that makes this tricky is map also takes a callback function and

so because I'm getting tired of seeing the word pad let's maybe call it item a little bit more generic this time and

this is going to be another callback function um well actually I'm going to open this up on its own line here all

right so now that we are looking at the individual items within the previous pads array this is where I can start to

look to see if item. ID is equal to this ID that's being passed into toggle and

if you remember in the instructions it said if the IDS match then return a new object where the on value is flipped and

if it doesn't match then just return the item as it was before well if we think

about it this is a perfect time to use a Turner and it might get a little bit long horizontally here but what we can

do is return and then we'll check if item. ID is equal to the ID passed in

and if it is then we're going to return a new object that has all of the properties of item but where the on

property is the opposite of item.on this should look very familiar I think

the structure might be a little bit different but this is very similar to when we were updating our contact card

as we were learning about updating an object in state we're getting an error because we need to finish off our Turner

if the IDS do not match then we can just return the item exactly how it was we don't need to make any modification to

it if you're relatively new to software development and maybe new to JavaScript

in general this might look kind of crazy to you but trust me if you take the time now to Think Through how this is working

and the longer you are writing code the more easily your brain will simply be able to make sense of what's going on

here this is not a terribly uncommon thing to happen in react and there certainly are other more verbose but

possibly easier to understand ways to write this but I promise it's going to be best to just take the time to

understand what we've written here maybe before I go too high up on that That Soap Box let's make sure that

this is working okay Moment of Truth all right and there's one more

thing that probably made this challenge a bit tricky we can see I'll hit save I'll

click one of these and geez it's not quite working yet let's go over to pad and see if we can debug it well notice

first of all that we still have our state that we're using and we're using that state as the expression that should

be determining whether or not the onass is added so let's get rid of this state I'm sorry if that threw anybody for too

big of a loop and we'll change on to props Doon the version of on that's

being passed from above now and let's try again hit save cross your fingers and click these buttons

perfect now I know that we wrote a lot of extra code especially compared to the way we were doing it before where each

pad component had its own state and its own way of updating that state however now we're set up in a much more react

like way where we have a single source of truth that data flows in Just One Direction it passes down through props

to the components that need it and those props can trigger changes through these callback functions or these functions

being passed through props which will trigger a change to the main single source of Truth in the state of the

parent component I completely understand if that seems absolutely crazy but do

remember if we now wanted to add a feature like like for example a button that said turn all of the buttons off we

could do that really easily we would just have a button when we click it it would do something very similar to this

except instead of checking if the IDS match it would simply return what we have here but a hardcoded

false and that's it it would change every item in the pads array and by

changing the state react would automatically react to that change

updating our button elements and the displaying new buttons on the page where they're all dimmed and turned

off all right we've made some great progress when it comes to our understanding of state and react and

props and how the two can work together where it's best to keep your state although there's a lot more to talk

about with that topic but we are long overdue to get back to our Chef CLA project and find some ways that we can

apply what we've been learning to that project

we're in a pretty good spot with our Chef CLA app if we scroll down we can see it has gotten a little bit long

mostly that's because we're hardcoding in a response from the CLA API for now

but for the sake of practice what I'd like us to do is refactor our app so that a couple of these sections get put

into their own components this will help make things look a little bit cleaner and for the most part it's just going to

be some good Hands-On practice so your challenge is first to move the entire recipe section into its own CLA recipe

component and that is this section let's see right here everything from this

section tag down to this closing section tag again this is hardcoded for now we're going to change that up when we

get real results from the cloud API and the second thing is for us to move the list of ingredients or the section that

has all the ingredients in it into its own ingredients list component doing this is going to be more than just

cutting out parts of the markup here and putting it in its own component than rendering that component because

remember those components are interacting with state in one way or another so that's going to require you

to think a little bit more critically about how you're going to communicate between the parent and child components

whether or not State needs to move down to a child component or live in the parent component I'm going to leave all

of that up to you while you work on this Challenge and then of course as always we're going to be going through this challenge together so let's go ahead and

I'll put in a pause now you can start on this

challenge all right I'm going to buy myself a little bit of room by cleaning up this challenge text but I will do

that right after I create those components so we need a claw recipe component and an ingredients list

component and I didn't make this part of the challenge but I'm actually going to put these under a folder called

components mostly just so that it's a little easier to find in my list here in fact I might end up moving Main and

header into this components directory as well but for now let's not worry about that okay so I'm going to create first a

CLA recipe. jsx file and I'll also create an ingredients list. jsx file

I'll stub out a function here so we'll just export default function ingredients

list and return this is sort of my version of a console log for new

components ingredients list component I'm going to just copy this and paste it

here and then change this to Cloud recipe and looks like I spelled

ingredients list wrong right here okay we'll fix that then in our main we'll go ahead and import those new

components and we'll make sure that's coming from the components directory and we'll do the same thing

for cloud recipe actually I'm going to put cloud recipe on top here all right let's hit save I don't think anything

should change because we haven't rendered those yet okay I'm going to clean up this challenge text and let's

see for the cloud recipe oh actually you know what I am going to put cloud recipe below ingredients list because that's

how we're rendering them on the page so we'll do the ingredients list um actually let's do the cloud recipe first

because I think this is going to take a little less work for us so I'll take out this entire section I'm going to render

the claw recipe component and then let's hit save and uh I need to click get a

recipe for that to show and okay we're getting the claw recipe component in our H1 okay let's get rid of this H1 and

paste in that section we'll hit save click get a recipe and okay we have that

section done now notice that in this case I'm doing my conditional rendering on the parent component here in my main

this recipe shown is only being used to determine whether or not this component should get rendered but I don't have any

data to pass down to Cloud recipe at least not yet because it's all hardcoded the ingredients list however is going to

be a little bit different let's go ahead and this section right here I'll cut this out and replace it with an instance

of ingredients list and then in my ingredients list I will get rid of my H1

actually let's hit save and okay we get our ingredients list component that's perfect okay let's replace this now with

the section that we cut out and we will likely find that we're going to break

I'll hit save and sure enough in fact I know what the problem is but let's look at the console ingredients list items is

not defined and that's because it's right here ingredients list items okay so we have some things that we need to

pull down we can kind of see from this view that we have ingredients list items missing we have ingredients missing and

we have this toggle recipe shown function missing now if you got stuck on the challenge before getting to this

point I'm actually going to put in another challenge here now that we've gone partway through I want you to give

it another shot just in case it didn't work out for you the first time if you were able to get this all working great

on you you don't have to do this challenge but if not this is another great opportunity to get some real practice in so I'll put in a pause now

for you to give this another

shot all right so these values are defined on our main component and we need to either bring them in from the

main component through props or there might be some things that we can actually compute here inside of the

ingredients list let's see let's start with this ingredients array this seems like a pretty important thing for our

ingredients list to have knowledge of and we'll remember those ingredients are coming from our form and the state is

being set here in the parent because the form does not live inside the same

component ingredients list I don't think there's going to be a meaningful way that we can move all of that down into

ingredients list instead let's go ahead and pass the ingredients through props

so I'll say ingredients is equal to ingredients and for the sake of my horizontal space I'll go ahead and put

some of this on its own lines and then we'll go to our ingredients list let's pull in props and this will now be props

do ingredients all right so I'm probably not going to get anything yet when I hit

save because we still have a couple of other undefined things this ingredients list items let's check this one out if

we go back to our main component and find where we were creating ingredients list items we're doing this based on the

ingredients array well we have access to this ingredients array inside of our ingredients list items so why don't we

take this out of here and make it a little bit more locally scoped I guess to our ingredients list it seems

appropriate because our ingredients list should probably be the component in charge of creating this ingredients list

items now I need to change this from ingredients. map to props do ingredients. map and let me actually

comment out this button for now and hit save look at that okay that's working and our ingredients are showing now the

reason I commented this button out is because we oh let's see where was it right there yeah we get this toggle

recipe shown that we don't have inside of this component yet so let's think for a second do I want to bring this toggle

recipe shown function uh let's see where did we Define that right here do I want to bring this function down inside of

ingredients list or do I want to pass it down through props well my main component it needs to know

whether the recipe is shown or not so that it can conditionally render the clawed recipe if I were to bring all of

this state down into the ingredients list component there wouldn't be a great way for me to pass that value of recipe

shown back up to my main component and then use it for conditional rendering so it makes sense to live here and so we

will need to pass that value down through props let's give this a new prop

we'll just give it with the same name of toggle recipe shown so that'll be toggle recipe shown equals toggle recipe shown

let me put these on their own lines then we will go grab it from props and this

will be props do toggle recipe shown we'll hit save and look at that I think we should be at a working place I can

click get a recipe that shows my hardcoded recipe and awesome this was a

long challenge we had to do a lot of work here and in the end it is maybe a little bit questionable whether that was

worth it or not we did get to remove quite a bit of code from our main component and sort of offload that work

to a couple of components that are maybe a little more honed in on what they're supposed to be doing so it's neither

right nor wrong per se architecting your react application will just take years and years of experience to figure out

what you like best and what makes the most sense for your team but I do think this was a good exercise in thinking

through where should State live how should we get information down to our other components if they even need them

in the first place where should things like this map that we're doing live so hopefully you understand what I'm trying

to get at here and at this point the only major feature we have left to add to Chef Claude is actually getting the

recipe from the AI this is super exciting this is where we actually get to make this app work the way it's

supposed to work instead of having a hard-coated recipe like we currently have so in the next lesson we'll be

seeing how we can sign up for these different AI engines there's going to be a couple different op options for you to

choose from and then we'll get to see how we can Implement actually calling out to those AIS sending them our

ingredients list and getting a recipe back in return so get excited that's what's coming up

next all right let's finally add AI to our system so that we can be pulling in

a real recipe rather than the one that we have hardcoded in this Grim I'll walk you through two different options for

AIS that you can sign up for and the only reason that I'm offering two different options is because when I

first started creating this project anthropic which is the company that created Claude AI was offering a $5

credit to anybody who would confirm their phone number and although $5 may not sound like that much it goes a

really long way especially with the version of the Claud API that we are going to be using however since then

they have taken away that offering so if you're okay putting $5 into a Claude account then you can sign up with Claude

I promise you it's going to go a lot further than it seems the grand total that I have used in all of my creating

of this project and testing has been I think less than 1 cent also Claude is a

very capable AI it's one of the best that's out there but as I mentioned if you're not interested in putting $5 into

your anthropic account then I'll be showing you another option using hugging face which will be completely free so

I'll help you get set up with an account on both anthropic and hugging face let's start with anthropic you can click the

screenshot here to take you to this very page to create an account with anthropic and once you've gone through this

initial phase it will take you to a sign up page where you'll want to make sure you put in your full name and whatever

nickname you want to include here make sure to check the box and click continue this will ask you questions about your

organization if you don't have an organization then I guess you could just put your last name here or something

these other two inputs for industry and website are optional anyway so once you put in an organization name you should

be able to click create account once you click create account it should drop you into sort of a dashboard prompt page and

from here you'll want to go ahead and click get API keys this will take you to your settings specifically under the API

keys for your settings there as I mentioned in order to create an API key and make any use of it you will have to

add at least $5 to your account so the first thing we'll do is go over to plans and billing and there you can see the

little warning up there that says to get started you have to upgrade your plan and purchase some credits so click

upgrade this will pop open a modal you'll want to make sure you choose this build option on the left I think that's

the default and then click continue and then it's just going to ask you a couple questions you can see I put in my

organization name as scrimba once you fill these out and scroll down to the bottom go ahead and click continue then

you'll be prompted to add your billing information and once you fill all that out you'll be able to click continue and

you'll have some money in your account okay with that behind us we can click over on API Keys click create a key you

can give the this key a name something that will be clear as to what you were using this key for so it really doesn't

matter what you name it I guess I chose to call this my first key you could choose to call it recipe app or Chef

Claud or something that's specific to the project if you'd like then we'll click create key and this model is very

important you don't want to close this model before you have a chance to copy the key once you close this model as it

says you won't be able to view it again make sure you copy that key and maybe temporarily paste it into some kind of

text editor so you can reference it again we're going to be talking about this pretty soon but this is a key you want to make sure doesn't get published

on GitHub with any of your repositories is never really referenced in your front-end code at all again we'll be

talking about that in an upcoming lesson so for now just make sure you copy this key before you close the model or you're

going to have to create a new key from scratch once you have that key assuming you are following along with us here in

scrimba you'll want to go over to your scrimba account so in version two of scrimba this is kind of the homepage

that you're dropped into go ahead and click your own little Avatar in the upper left and in this submenu here

you'll see the option for settings click settings and you might need to scroll down just a little bit but under scrim

settings you'll see this button that says edit your environment go ahead and click that and this is a place in

scrimba that allows you to add environment variables that are accessible from any of your scrims when

we as the teachers are recording anything that requires an API key for example we're going to use a variable

shorthand which will be referencing your own personal environment well for us it was referencing our environment when we

recorded it for you when you run the code it will reference your environment so you'll go ahead and click new key and

from here you'll need to include a name and a value the name will be what is referenced in our code base and I'm

going to be using anthropic aior key all in capital letters so assuming you are

following here in scrimba and you're using the anthropic API make sure that you get this exactly right the same way

that I have it here otherwise you're going to have to change it every time you do one of your challenges then for the value you will paste in the API key

that you copied from the model before right here once you've pasted that in you can go ahead and click save then in

any scrim when you see me writing with this saved in your environment inside of any scrimba with that API key saved to

your own scriba environment anytime I reference process. env. anthropic API

key just like I did in this line it will look up that environment variable in your own environment and use it instead

of the one that I used when I was recording now as I mentioned the CLA API is one of the best AIS that's out there

at least at the time of recording this I've noticed that it's giving me excellent results and even though I did

have to put $5 into my account it costs me essentially nothing to use it like I

said I've used I think a total of 1 cent since I first began creating and preparing this project however I did

want to include an option that was completely free as well and in the admitted ly limited testing that I've

done with it it also is producing great results and that is by using an AI model that's hosted by hugging face you can if

you haven't heard of hugging face you can kind of think of it like the GitHub for AI models some of the AI models that

are hosted by hugging face are free and some of them are paid so creating a hugging face account is free and the

model that we've chosen is also a free model so you can click on the screenshot here to go to the sign up page for

hugging face and just like before you'll go through the account creation process it's going to ask you for some

information about your profile it looks like the only things that are required here are a username a full name and then

to agree with the terms of service in this check box at the bottom once you've done that you can click create account which will drop you into sort of an

introductory page but you'll notice that at least at the time of recording this there was a little alert at the top that

required me to confirm my email so I went to my email I clicked the link that was there and that dropped me into this

page where it says my email address has been verified successfully at this point you don't need to worry too much about

creating an organization or joining an organization instead we are going to create an access token similar to the

API key that we created with anthropic click on the sort of placeholder Avatar in the upper right and from this menu

you'll go ahead and click on settings in the submenu on the left we'll go ahead and click on access tokens and from

there we will create a new token on the create a new access token page the only things that you'll need to worry about

is giving your token a name I've chosen this this time to call it recipe app and the only checkbox that we need to worry

about is this one right here under inference that says we want to make calls to the serverless inference API so

make sure you check that box we can scroll down a little bit and then see nothing else is checked we can just

click create token just like with anthropic this is going to give us a modal that once we close it we won't be

able to access our API key again so make sure you copy this paste it into some

kind of text editor just temporarily until you have a chance to put it in an environment variable either in a EnV

file on your machine if you're doing everything locally or inside of scrimba just like we did before with the

anthropic API key in our environment variables just like I did with anthropic I'm going to be using the name HF

accessor token so make sure you type this in exactly the same way or it's going to be a little bit annoying to

have to go back and forth changing the name from the way that I recorded it and of course don't forget to hit save now

as I mentioned I'm going to offer a really easy way for you to have one or the other of these so for the remainder

of this project I'm going to be offering a way to make your API calls to either one of these and I'll try to make it as

simple as possible to switch I'm going to be using the Claude AI because I have already added money to my account and

I've been getting pretty good results with it but I'll be trying to make it as easy as possible for those who want to

follow using hugging face to do so in a really easy way all right that was a lot of talking and not enough coding let's

jump in and start making calls to the real Claude API so in the next lesson let's finally start sending our prompt

to a real Ai and getting back a real recipe so we can replace the hard-coated one we

have let's finally make use of AI to generate our recipes when given a list

of ingredients as opposed to this silly hardcoded thing that we've done so far now because this isn't a course all

about Ai and how to use AI apis I'm just going to have the code written for you

which I'm sorry if that's a little anticlimactic but the truth is I wanted to stay focus on learning react here and

not getting too sidetracked by learning AI that said I did include a link here to a course here on scrimba called intro

to AI engineering taught by Tom and it's an excellent introduction to help you get your feet wet when it comes to AI

engineering you can click the screenshot here it's just a short 90-minute course but I would recommend doing so maybe

after you finish this section in react so I've written the code that will use both the claw API and the hug face API

and we can find that right here in a file that I've called ai. JS now in the last lesson you should have created an

environment variable either for the anthropic API key or for the HF access

token and a quick warning that I wanted to make sure I got out of the way at this point is that if you're following

Along on your local machine instead of here on scrimba I need to remind you that you do not commit these API keys to

any repositories here on scrimba we have a dedic dedicated system setup for creating environment variables that are

specific to each user they don't get exposed to the public but if you're following along locally and you're using

let's say a file called EnV and you have your anthropic API key in there you need

to make sure that you get ignore that file if you don't know what that means it's outside the scope of this course

but a quick Google search should help you out additionally because the API calls we're making are coming directly

from a browser environment to the respective apis you can see I added this

property here called dangerously allow browser that means that we can make API calls to anthropic directly from our

browser as opposed to having to relay it through a server this means that if you were to deploy your project anywhere

live online like netlify for example anybody who comes to your site could dig around through the code and find your

actual anthropic API key or hugging face access token or whatever private variables you think are private but

actually aren't really the only way to secure these a API Keys is to relay these requests through some kind of

server whether it's a server that you have created or a serverless function on whatever deployment platform you're

using so here inside the scrimba environment you have nothing to worry about but locally make sure you heed

this warning that I've given you okay let's walk through this code so that you at least get a highlevel overview of

what it's doing when you're interacting with an AI you need to give it some kind of system prompt that helps set the

stage for the AI to know what it's supposed to be tasked with as you can see I've created this system prompt that

says you are an assistant that receives a list of ingredients that a user has and suggests a recipe that they could

make with some or all of those ingredients I did end up having to specify that the AI does not need to use

every single ingredient that is mentioned and it's allowed to include some additional ingredients that they

didn't mention but as I said try not to include too many of those another really important instruction that I added to

the end here is to format the response in markdown so that it would be easier to render to a web page we're going to

come back to this and see how this is really helpful for us oh and something I just realized is I'm importing things

like this anthropic Constructor or this HF inference Constructor from these libraries but I have not included those

as dependencies so I'm just going to go ahead and make sure I add those as npm packages to my dependencies here in

scrimba I just add the dependency here in the interface if you're following Al locally you'll need to npm install

exactly what you see here and here now with anthropic I'm creating this anthropic instance this is all part of

the software developer kit that they give me I had to pass my API key so that it knows who I am when I'm making

requests and because I am making these requests directly from a browser I had to include this property dangerously

allow browser and set it equal to true you can see with hugging face I do something very similar down here I have

to pass my access token to this new instance of HF inference again the details of this are not that important

for you to know but do make sure you follow these comments because if if you didn't follow along in the last scrim

where we add these to your environment variables on scrimba you will need to do that before this will work then I just

have two custom functions that I wrote this first one get recipe from Chef Claude which takes an ingredients array

and makes a call to the anthropic API to create a new message or down here I'm

using get recipe from mistol now hugging face is like a host for different AI

models and in this case I found that mistal AI was actually a really good model that came from hugging face and it

was giving me pretty good responses depending on when you're watching this chances are this model may have been

updated so you might want to go to the hugging face website and just see what mistal models there are and you might

need to change the model that we're using here with anthropic I did opt to use this Claude 3 High cou version and

at the time of recording this is actually the cheapest version that they have with anthropic and it was giving me

great results so it was fast extremely cheap and giving me great results so I think it's a great one to stick with as

far as I can tell there isn't too much of a benefit with one of the more expensive models which can be 10 times

the cost per API call in each of these cases in one way or another I'm passing in that system prompt variable the one

that we defined up here above sending this off to the respective apis and then

just kind of drilling down into the responses to get the content that comes back from the AI guy it looks like I

have a little bit of error handling here on the mistal side I probably should include that in the chef Claud side too

okay again that was just meant to be a highle overview you do not need to understand everything that's going on

here if you would like to learn more or practice with it you can go to the intr AI engineering course and learn a little

bit more about it there so what does this mean for you well it means that inside of our main file when we want to

use an AI to generate the actual recipe all we need to do is import one of the two functions that I wrote here in our

ai. JS file then in the appropriate spot I'm not going to show you exactly where because that's going to be an upcoming

challenge all you have to do is call the function and pass to it the array of ingredients that we're saving in state

here in our main.js file so this is awesome yes I've done a bit of this work for you but you can see that it's not

that much code we're working with less than 60 lines of code here and that includes two different AIS that you can

get these recipes from we truly are living in a modern age this is awesome okay now that we're all caught up on

what's happening in the background with this ai. JS file we are now going to jump in and well make use of these

functions this is where it starts to get really fun so in the next lesson I'm going to have a challenge for

you this is a really fun part of this project actually pulling a real recipe from the AI because we're pretty far

through this react course I'm going to make this challenge a bit more vague and give you a chance to really think

critically and and synthesize all the skills that you've been learning and practicing up until this point to solve

this challenge mostly on your own now just so that it's not completely overwhelming we're going to go through a

bit of the problem solving process and to do so I'm going to give you this kind of in challenge mini quiz so I have two

questions here just like our regular quizzes I want you to click into the editor and type down your answers hopefully this will help guide you in

the correct direction so that in the next lesson when you actually start writing your code you'll at least have a good idea of where you should be

starting so go ahead and answer the questions in this mini

quiz all right for number one I want you to think about where the recipe response should live inside of our react app and

how you're going to make sure that it doesn't disappear between each state change in the app or I guess another way

to say it is to make sure it doesn't disappear every single time the app gets rendered I'm not talking about if you

were to hit Refresh on the browser because that would probably require using some kind of browser storage like

local storage and that's a little bit outside the scope of this project well once I get the recipe back from the AI

I'm going to save that in react state so that can be my answer here I'll say I'm

going to save the response in react state by doing this I can make sure that

if I were to add another ingredient and then click get a recipe again the old recipe wouldn't just completely

disappear or any other state changes that I might decide to include in this app react state allows me to save

information from one render to the next and if I ever change that state it will cause a reender so for now in react

state is going to be a great place for us to save that response number two what action from the user should trigger

getting the recipe we have these functions that I pulled in get recipe from Chef Claude and get recipe from

mistol at what point am I going to call these functions well I know it's not going to be as soon as my app loads

because I need my list of ingredients I need the user to be able to add to the list of ingredients but it's when the

user clicks this get a recipe button hopefully that was pretty straightforward based on the UI that we've chosen here with a button that

literally says get a recipe so for number two when the user clicks the get

uh recipe button although this question seemed a bit straightforward when you actually go to work on this challenge I

think you'll find that it might be a little bit more involved than you might think when we refactored things we

passed our function that get a recipe button is calling down through props to another component that's all I'm going

to say for now because now we should be set up in the next lesson to have you actually work on the code for this

challenge all right here we go our challenge is to get a recipe from the AI and this time you're actually going to

write the code so either using the get recipe from Chef Claude function or the get recipe from mistro function make it

so that when the user clicks the get a recipe button the text response from the AI will be displayed below currently we

have it hardcoded so that when we click get a recipe it's just toggling the recipe on and of course this is just

hardcoded but what it should be doing is displaying the real recipe from the AI currently we're using this recipe shown

State I'll leave it up to you to determine whether or not this is still important to have and keep in mind that

we did ask the AI to return markdown so it will just be displaying raw markdown

it's not going to look very pretty quite yet we're going to end up using a package that will render the markdown

for us this is a bit more of an involved exercise but I know that you'll be able to do it don't be afraid to reach out to

the Discord Community if you need help or to look back on previous lessons if you're forgetting some of the syntax

that's a completely normal and okay thing to be doing also don't hesitate to use a tool like Claude or chat gbt to

help you out pretty much any of those things would be much much better than just skipping the exercise because you

got a little bit stuck you got this go ahead and get started on this challenge

sometimes when I'm building a new feature like this I like to start at the point where the user is interacting with

the code which in our case would be this get a recipe button so let's go down and look at that button and actually it's

over here in our ingredients list we're passing this toggle recipy shown function down to ingredients list and

it's pulling that in through props and right here our onclick says toggle recipe shown this was always intended to

be a temporary measure and the state that is changing when we click that button this recipe shown State we could

continue to use it in order to conditionally render the recipe from Chef Claude but honestly I think we'll

be better off just saving the response from the AI in state and if that

response is truthy or is not an empty string then that's the value we can use to conditionally render this whole

section down here so the first thing I think I want to do is rename this function because we're not just toggling

whether the recipe is shown we're actually getting a recipe so let's say get recipe and yeah that's good enough I

was going to say get recipe idea but get recipe gets the job done so now that we've changed that function name we'll

go ahead and pass the real function down we might as well change our prop name

while we're at it to the same name get recipe and we'll need to go over to ingredients list to fix that so Props

dog recipe okay that was all just for changing the name let's go back and change how that function Works instead

of setting the recipe with whether it's shown or not we are going to call get recipe from I'm going to use Chef Claude

And if we remember these functions are expecting a list of ingredients which we are saving in state so I can just pass

in my ingredients to the AI function now assuming you did this Challenge from

scratch without too much help or skipping ahead to watching me do it you may have run into an issue because the

functions that we're pulling in they are async functions which means by default they are going to return a promise let's

let's go back to our main this means we can either use a then to unpack the

promise afterwards or a little bit more of an updated syntax as we can use async

await so I'm going to make this an async function will await the response and

we'll save that as a recipe idea or maybe let's call this something that's

clear it's from an AI we'll say generated recipe and this should be in markdown so I'm going to say markdown uh

that might be Overkill Let's uh let's just call it recipe markdown okay that's good enough okay I like to do sanity

checks whenever I can before I get too deep into a feature without having tested it and then have no idea where

I've broken things so let's go ahead and console log recipe markdown we'll hit save and see if we need to fix any bugs

okay let's click get a recipe we're waiting a little while while the AI is responding to us and let's open the

console awesome check it out this is the response text from from anthropics claw API and sure enough given the exact same

list of ingredients it keeps recommending spaghetti bolog if you look closely you can see the text includes

things like hash marks and dashes this is all part of markdown and so we are going to be displaying that correctly

later but we'll notice that if I try to scroll down nothing is there because we're no longer setting the recipe shown

inside of our get recipe function so instead of console logging our recipe markdown let's go ahead and save this to

State and let's create the state first instead of recipe shown let's just call

this recipe because this is where we're going to save the recipe text instead of

starting this as a Boolean we'll start it as an empty string and then I will call set recipe with the recipe mark

down so we'll just do that right here and then we can use the state of the recipe to determine what should get

rendered right now we're saying recipe shown and Claud recipe will just make this say if the recipe has a truthy

value or in other words as long as it's not an empty string then we'll display the cloud recipe we haven't yet of

course replaced the hard-coated stuff in Cloud recipe but let's make sure that our conditional rendering is working

I'll click get a recipe and after just a little bit of time we can see that we can scroll down and it's displaying the

chef Cloud recipe Let Me Close Our console to buy a little bit of room and now what we can do is pass this recipe

down through props to Cloud recipe so we'll just say recipe equals recipe and over in our Cloud recipe we are now

going to be receiving props and I'm actually just going to get rid of everything that was hardcoded here and

let's just render the text from props do recipe hit save click get a recipe and

here we go okay much less beautiful but it's markdown we're going to format it in a really easy way using a third party

package but for now this is working awesome and it's really exciting to have a real recipe coming in of course

currently we have the ingredients hard coated so just for fun let's let's go over to our main file we'll get rid of

the hardc recipe ingredients and actually let me get rid of this challenge text to we'll say that this is

an empty array and uh probably doesn't need to be on its own line anymore let's

hit save and I don't know let's come up with some good stuff let's say we've got some chicken we'll still say we have all

the main spices just so it knows that we've got what we need on hand for spice uh maybe we have some corn maybe some

heavy cream and we have some pasta I don't know let's go ahead and give this a shot we'll click get a recipe takes a

little bit of time now that it's reaching out to the real API and let's see it wants us to make a creamy chicken

and pasta bake boy that sounds really good great work on this challenge hopefully you were able to get through

it and honestly I don't even feel bad if it was a struggle because that is where the Learning Happens let's go ahead and

format this so that it doesn't just look like a giant wall of text and we'll essentially be at the last phases of

this app at least for now let's get this crazy block of text

formatted so that it actually looks presentable for our user and the really good news is we aren't going to have to

do any of this manually because we ask the AI to return the recipe formatted in

a markdown format we can use a package called react markdown I think there's a number of other ones but this is a very

popular one to turn the markdown format of text into something that renders as HTML you can click click on the

screenshot here to go to the npm package for react markdown I believe it will automatically bump you down to the

section that shows you how to use it and since you will often find yourself using thirdparty packages to help you out in

your react codebase we are going to turn this into a challenge first let me come over to the cloud recipe here and I'll

type out the challenge text you know reading documentation is one of the most common things you'll

find yourself doing as a software engineer and and often times other people have written code that does the

task that you are trying to do so it's really common to find a thirdparty package like we have here with react

markdown that can just accomplish our task and allow us to complete features a lot faster so I think this will be a

good exercise even though it's more react adjacent using a thirdparty package so your challenge is to see if

you can figure out how to use the react markdown package I've included it here in the list of dependencies but if

you're following Along on your own machine you will need to make sure that you npm install react Das markdown all

of that information is going to be here on the npm page anyway but I want you to use react markdown so that you can

render

props.com that getss turned into react elements a little bit nicer this means all you'll have to do is add this

suggest recipe container class to the section right here I guess I should

probably type that Ino okay that should be pretty straightforward all right it's your time

to shine go check out the documentation for react markdown by clicking this screenshot and give this challenge your

best shot all right over in the documentation

we can see that what we need to do is import react markdown from react D markdown

and this thing that we're importing is a component unlike all of the custom components that we have been using so

far like our ingredients list component is a self-closing component our CLA recipe component is self-closing as well

if you look in the documentation we can see that this react markdown component has an opening and a closing tag and so

we will go ahead and render react markdown and on the other end of props recipe which we're passing in we will

render the other half of react markdown and this is small enough I don't think we need this to be on its own line we'll

just do that this concept of having separate opening and closing tags for your custom components it's something

that you'll see pretty regularly in react it's using a concept called children but for the most part I'm not

going to be covering react children in this course instead that is something that I cover in my Advanced react course

okay let's hit save you can see I put back in my default ingredients from the last scrim that we created and I'll

click get a recipe once that recipe comes in let's scroll scr down and wow look at that that is looking so much

better than it did before let's go ahead and add our class name here just to see how that changes things this was I'm not

going to guess it let's go over here suggested recipe container and let's try again we'll hit save click get a recipe

and we can scroll down and awesome okay this looks a lot more like the design that we saw in figma the last thing that

I want to add here is a transition that's a little bit nicer than just jumping straight into this text so I

think I'm going to add an H2 here that just says something like

Chef Claude recommends and then we need to keep in mind that for those using

assist of Technologies if we're conditionally rendering this section we need to add an ARA live equals polite

this way when react conditionally renders it to the page for the first time it will be announced and read

through the assist of Technologies let's go ahead and hit save and we'll just see

what our new H2 looks like okay chef CLA recommends awesome and that folks

represents a perfect stopping point for us in our Chef CLA app now it's not perfect by any means we actually are

going to be revisiting this again in the next section but we have a few more things that we need to learn about first

and you are probably getting pretty tired of spaghetti bolog and creamy chicken and pasta bake it's a lot of

carbs to be taken in we have learned so much in this section that the things that we've learned in this section

represent some of the most commonly used things in react and so before we move on I'd like to do a quick recap to take a

look back at everything we've learned before we're ready to move on and continue learning some awesome things about react and continue working on some

amazing projects holy cow we have made it to the

end of Section 3 this was a mey section and you have finally built your first

interactive react app congratulations with the knowledge that you gained and practiced in this section the sky is the

limit as to what you can build let's do a quick recap of the things that we've learned in the process of building our

Chef CLA app we learned about event listeners which are the basis of interactivity on the web from there we

spent a long time learning about State and react State gives us a chance to maintain data between reenders of react

and cause new renders and react so that we can follow the Paradigm of react which says that the UI or what the user

sees should be a function of the state this gives us a super declarative API in

react which allows us to Simply up upate the data that react is maintaining and rely on react to update the view

accordingly we discovered a number of different ways that we can conditionally render parts of our app based on the

state or the incoming props for any given component this gives us not only flexibility in what actually gets

displayed to the browser but also gives us a chance to add another interactive element to our app we learned all about

forms in react which gives us a chance to collect information from the user and do something with it we could send it

off to to a database to be stored which of course is a very important component when it comes to interactive and dynamic

web applications then we took a little bit of a side quest from Chef Claude and learned about some different State

Management strategies different ways that we can architect our app and the pros and cons of each of those ways

we'll actually be getting a chance later on in this course to revisit this topic of where State should be held and

controlled I know I've said finishing the other sections were huge accomplishments but believe me when I say this is the biggest accomplishment

yet we covered so much ground that you would really be doing yourself and the community a disservice if you didn't go

over to the scrimba Discord community and post an awesome celebratory message in the today I did Channel you worked

really hard in this section so you deserve some praise now we have one more section in this course that will be

focused on learning new topics and then we have a couple really fun projects lined up after that once you've had a

chance to do a little happy dance and to rest your brain for a little bit let's keep moving forward

welcome to section four and the last section where we'll be focusing on learning new things in react in this

course this entire section is all about how we can handle side effects in react and in the years that I've been teaching

react I have found that understanding side effects in react can be one of the more tricky things that even seasoned

react developers can experience when react transitioned away from class components into functional components

and started using hooks back in version 16.3 the way that the world thought about react kind of changed forever

there wasn't nearly as much talk about side effects in react as there is these days which once you understand the

concept of side effects actually turns out to be a good thing let's take a quick look into what we'll be learning

in this section we've already learned about the new way that react handles forms with form actions and some other

apis that are a bit outside the scope of this course however there are instances where you may still want to do form in

the way that they used to be done in react which is using controlled components the app that we'll be

building in this section which we're going to talk about in a second uses controlled components and so I figured

this would be a good opportunity to cover that topic then we'll be taking a bit of a studious asside to talk about

functional programming and how the react philosophy has really centered around

functional programming this will give us a better understanding of the concept of side effects and how we can best think

about them in react then on a more practical level we are going to be creating a side effect so that we can

fetch some data there's a lot of different ways to deal with fetching data but we will be seeing how we can

fetch some data as soon as our app loads then for the majority of this section we will specifically be talking about side

effects what they are how we can create them in react what pitfalls we need to be on the lookout for and so forth and

of course this wouldn't be scriba if there weren't a ton of Hands-On challenges along the way speaking of

which to drive this curriculum forward we are going to be building a meme generator it's a pretty straightforward

app it has an input for top text so when you type into this top text input box on

every keystroke the text on the meme image will update and then of course the same for the bottom text when you type

into this input the bottom text will update on every keystroke and then you have the option to click a button which

will get a new random meme image from a list of popular meme images that comes from the meme API called image flip

we'll also have a quick chance to apply the concepts that we learn in this section to add a feature to our Chef CLA

app from the last section so no more delay let's jump right

in to help us guide our discussion about side effects we are going to be following this meme generator project

and unlike the previous projects where I actually have us start it completely from scratch we are going to be

beginning this one from a starting point so before I just threw you into an unfamiliar code base I wanted to walk

through the codee here and give you a chance to walk through it yourself I think it's helpful to have somebody

explain the code but I think it's even more helpful to take the time to go through things on your own and maybe

even try to change things fortunately the starting point for this app is really straightforward we can start over

here in our index we're just creating a root and rendering the app component the app component is simply importing the

header and main components and rendering those the header is simply this purple header up top top and the main is well

everything else on the page the header is as simple as it might seem and the main is currently not doing anything

reae other than simply rendering the jsx you can see we're hardcoding the image

the top text and the bottom text the one thing that is a little bit different about this and we're going to be talking

about this soon is how the inputs kind of look like they belong to a form and the button kind of looks like it submits

that form but the truth is that's not exactly how this one works the user will simply type into the top text input box

and that will every keystroke update the text that displays on the image up at the top of course the bottom text does

the same for the bottom and clicking the button doesn't submit any form anywhere it just randomly gets a new meme image

this project will be a little bit on the simple side I know a lot of memes these days have text in different positions

than just the top and bottom but we're not going to get that deep into it as I said everything is just hardcoded right

now in the next lesson we're going to be moving this into react State and then we'll jump into building this project

and the main reason we're doing this project is learning how we can make fetch request to an API as soon as our

app loads before I just jump into the next lesson I'm going to put a pause in here to give you a chance to look

through this code make sure you understand what's going on again it's not terribly complicated it's kind of just like walking through some HTML but

doing so should hopefully Prime you to have Success Through the rest of this project so take some time now to peruse

through the code all right hopefully that was helpful in

the next lesson we are going to move some of this information into

State all right let's get started right off with a challenge I want you to move the hard-coded meme information that we

have down here into react State the state should contain an object that has

a top text bottom text and image properties and then set the initial values of those properties to the values

that you see below in fact you know what I'm going to make a change here just so that it's clear this is an image URL at

this point we're not going to worry about hooking up the inputs or the button so you're just simply creating

State and using that state value instead of the hardcoded ones down below go ahead and get started on this

challenge all right let's go ahead and create let's call it Meme and set Meme

and this will be equal to react . use State and I need to before I forget

anything else import react from react and actually you know what we've had three sections where we're importing the

entire react library and I mentioned specifically that it makes it a little bit easier to know that Ed state is

coming from the react library but I think you probably get it for now so I'm just going to switch it up we're going to destructure use State and pull that

in from the react library and then just call you state like this honestly this is probably the more common way that

you'll see it so I think it'll be good to see it both both ways all right my initial state is going to be an object

as it mentions down here and we're going to have a top text property a bottom text property and I'm just setting these

equal to empty strings for now we're going to fix this in a second and then an image URL property okay for the top

text we have one does not simply and no right there bottom text walk into Mordor

and let's grab this image URL as our starting point here clean up the

challenge text and we need to switch these to now use the state value instead so this is going to be meme. image URL

this one is meme. toop text and meme.

bottom text these kinds of refactors are not super thrilling because I will hit save and it essentially looks like I

didn't do any work but we've primed ourselves to now be able to update our state which will of course update the UI

this whole section is about side effects and using a built-in function from react called use effect but I kind of want to

take care of some of the other items that we have for example being able to type into these inputs and have them on

every keystroke update our text so I guess we have pun intended a little bit of an aside to take before we get into

side effects so in the next lesson let's hook up these inputs so that they can update our

state in the last section we learned all about forms and how we can add an action

property to our forms in order to catch the information whenever that form gets submitted I mentioned at the time that

that represents an update to react this is something new in react 19 that is

very very welcomed before this update we had to use something called controlled components whenever we created a form

and truth be told I think it was one of the worst parts of react it was overly complex it felt like it was Reinventing

the wheel and with that glowing review we are going to start using controlled components don't get me wrong there are

still instances where controlled components make sense in react and we are about to see one of them remember

with our two inputs here we aren't collecting information from the user and then submitting it somewhere for it to

be processed that's really what a form is intended for instead we just want every single keystroke that the user

types into our inputs here to update immediately on the page which means

every change of the inputs is going to update our local state as such we don't

need to use the underlying ability of forms to maintain and hold their own

information and then submit it all at once in a form data object but rather we

want to set it up so that we have an event listener on our inputs let's see this input and this input that on every

keystroke or change of the input we want it to update our state now I thought about doing a whole aside and and giving

you a series of challenges for this but truth be told because with react 19 we have form actions and a couple other

slightly more advanced hooks that we were given to deal with submitting forms I'm actually just going to walk through

this and hope that it makes as much sense as possible again this is not the Crux of our section which is supposed to

be talking about side effects first let's see the onchange event listener working so I'm going to add an on change

event listener and I'll call a function which I haven't created yet called handle change whenever the change

happens let's create this function handle change and I'll just console log changed

for now let's hit save I'll click into the box let me open the console I'll click into the box and I will

type some characters okay you can see every single keystroke spaces letters everything it

called my handle change function okay well how is this helpful to us what I can do is I can look at the event that

comes through on my handle change since this is an event listener the value passed to that function is information

about the event that was fired I can grab whatever text is currently in this input Box off of the event and then set

my top text or bottom text we're going to see how to do both I can set the value of that text equal to whatever the

input box currently says so from this event I'm going to pull off a value and

I'm just going to destructure it right off the event we're going to get the actual value from

event.target the event is the event that was fired Target is the element that

fired the event and actually there's another one you know what I think I'm actually going to use current Target you

don't need to worry at this point the difference between the two the point is I'm going to console log my value we'll

hit save and I will type into the input box again and you can see in our console

the first character I typed it logged the value which was just the letter T then Ty y typ typ every keystroke is now

being logged to the console okay well I think this is probably a good point at which I can get your hands on the

keyboard and give you a challenge this challenge is only going to partially solve what we're working on but it'll be

a good way for me not just to be droning

on okay your challenge is to update the top text value in the meme state object

this one right here every time the top text input box is changed now for now I

don't want you to worry at all about the bottom text in fact I removed the onchange event listener on the bottom

text input box just so it wouldn't be confusing this challenge will hearken back to how you can update a single

property in an object's state so if that's feeling a little bit Rusty for you you may want to open up the lesson

in the last section where we went over this or of course you could ask in the scrimba Discord for some help or just

plug it into into Google or chat GPT and you should be able to find an answer pretty quickly all right your time to shine go ahead and get started on this

challenge anytime we want to update State we need to use our state Setter function so I'm going to call set Meme

and because we don't want to erase all of the other properties of our meme we do need access to the previous version

of the meme so I'm going to use a callback function and what I'll return will be an object but because I'm inside

of an arrow function I need to wrap that object in a set of parentheses just to be a little more confusing we'll bring

in all of the properties from the previous Meme and we'll change our top text to be whatever value is currently

in the input box let's clean this up hit save and we'll say Shut Up And Take My

Money cool awesome on every keystroke this was updating and because react is

so good at what it does it was updating really quickly there was really no in every keystroke for having it render

and display the new text okay I think we've bitten off quite a bit in this lesson we're going to learn how we can

make our bottom text input box also work without having to write an entirely separate function for it as well as

learning one little gotcha when it comes to controlled components and what the term controlled components means in the

first place all of that's coming up

next all right what even is a controlled compon component well remember how I

talked about that forms have their own ability to hold their state internally I mean we can see that when I type into my

bottom text form this is some text this value is being saved somewhere it's

being rendered to the screen by the browser and that's because forms have an intrinsic built-in ability to hold this

data in this case react is not controlling the output of this form or

the actual display of this form a controlled component on the other hand is one that react is in control of me

changing this text doesn't change anything else on the page so an uncontrolled component is for example an

input box that react is not in control of and doesn't reflect the current value of State any controlled component is one

that react is in control of and does reflect the current value of State the idea when react was kind of in its early

stages actually just up until very recently the idea was that react should hold the single source of Truth for

anything that is being displayed on the page so text like this that didn't conform to using state in react felt a

little bit like an anti-pattern I guess in the theory of react all this means is

that as we can see I'm able to type something different in my input box than what the bottom text is supposed to be

according to react I have two different versions of Truth in order to make this a controlled component there are two

things that I need to do the first is I need to be able to update state every time there's a change inside of my input

box this is exactly what we did by adding this onchange event handler in the top text input box however there's

one more part to this and that is that the current display value of our top text input box doesn't reflect what the

top text state says it kind of looks like it because our placeholder is actually the same thing let me actually

change this to something different and I'll hit save okay you can see something

different is correctly displaying in our meme but both of our input boxes are empty again they don't really look empty

because of the placeholder I guess that was a little bit confusing but in a true controlled component we want to manually

set the value of this input box equal to whatever the current value is in state

in our case it would be meme. toop text so now we can see the input box actually

reflects the current value of state by saying something different the two sort es of Truth have been united into one

it's just held by react and I can change this and whatever changes in the top

text input box will change on the page as well so those are really the two parts when it comes to having a

controlled component we need to have the component or the input box accurately

reflect what the current value of state is and also every single change will update that state and as such react now

has essentially kicked the form's ability to maintain its own separate State internally to the curb and it's

taking control over everything it's kind of like being a control freak in this case in our case because we want the

state to update on every keystroke it actually makes sense for us to use a controlled component here so let's do

the same thing for the bottom text we're going to give it a value of meme. bottom

text and I'll also copy this onchange over at first glance it might look like

we kind of have to use a second function because right now we are hard coding that this handle change function will

change the top text in fact if I hit save and then start changing this oh we

can see we start to get some weird errors happening because there's a little bit of fighting happening between

these two values oh well and I guess I'm displaying the bottom text value but I'm

trying to update the top text accordingly fortunately instead of having to create a completely separate

function I can use the name value that each of my inputs have in order to correctly update which portion of state

I'm going to change by the way I know that we're moving kind of quickly here my old course had probably six straight

lessons on controlled components and different kinds of inputs but with react 19 kind of making that mostly obsolete I

really just wanted to fly through this so I'm sorry if anybody is feeling a little bit lost that's really okay

because again we're here in a section about effects I want to get to learning about side effects as quickly as

possible here we're pulling in the value from event. current Target I can also pull in the name property that's exactly

this right here name of either top text or bottom text and by ensuring that bottom text is spelled exactly the same

way as the bottom text property in our state instead of hardcoding top text here I can use a set of square brackets

and say whatever name is currently changing the input that's the property

on the state that I want to update again it's okay if that makes no sense at all let me hit save I don't want this to say

something different let's have it say One does not simply we'll hit save again

okay so I can start to change this one great one does not and then we'll just go ahead and change this and look at

that it's correctly reflecting the respective pieces of State depending on the name property from each of the

inputs all right jeez that was quite a whirlwind as I said that's not really the important part here we have part of

the core functionality working with the top text and bottom text now finally let's dive in start learning about side

effects and react and see how that even applies here to the meme generator

project the next task that we have in our meme generator app has to do with fetching some data you see we could

hardcode all of the memes that we want to include as possible images that we get when we click the get a new meme

image button but that's not as fun we want to use an API that has the currently most popular meme images in

its database and we're going to be using an API called the image flip API which has a dedicated endpoint to give us 100

of the currently most popular meme images in order to get those we are going to have to make a fetch request to

the database with all the meme images our site will make a request out there and because it's asynchronous we don't

know exactly how long it's going to take for it to respond but eventually a response is going to come back to our

react app and we are going to store the array of meme images in in our local

state in the react app then from the array of meme images that we got back from the database we will randomly

choose one every time the user clicks the get a new meme image button which means clicking the button itself isn't

going to be making a fetch request and returning a response but instead simply loading up the app will have the side

effect of grabbing that array of data from the image flip API then everything else is just going to be processed

locally Within our app like randomly choosing an item from that array of 100 meme images so if we're not kicking off

a request when we click the button I want you to think when are we going to be kicking off this first request to get

all of the meme images well to be honest I think I gave the answer away in something I said earlier but we're going

to grab all of these meme images as soon as our app loads and describing it that way makes it sound like it should be

really easy in the end it really is easy but it requires us to have a basic understanding of the functional

programming Paradigm how that relates to react and how we can initiate this initial request upon the loading of our

app for the first time so just to help us have a greater understanding of what a side effect even is we're going to

take a really high level Overview at a programming Paradigm called functional

programming I'll caveat this lesson by saying that I am definitely not an expert in functional programming but I

think a really highlevel overview of function programming will be helpful in understanding a little bit more deeply

how react works and what the philosophy behind creating react was it's also

going to help us when we're talking in terms of side effects which is what we're currently working on in our little

side quest here there are a number of main principles with functional programming and we are just going to be

touching on a few of them the first one that I want to talk about is the concept of pure functions a pure function is one

that if it's given the same inputs it will always produce the same outputs and

running that function will never have any kind of change elsewhere in your system this is where the concept of UI

as a function of State comes from all it simply means is that the whole job of your components that you're writing are

to take input which in one example might be incoming props from some above

component and given those props its entire purpose is to return a user interface some kind of Dom elements that

display on the screen and if it's written correctly no matter how many times your app component is rendered if

the props are the same then the UI that's produced will always be the same now if the props that are coming in

exist in a parent component and that component changes those props somehow maybe those props are actually part of

State in that parent component then the change in props will cause our app component to render and potentially

produce different results in the user interface and this exact same principle applies if what changes is an internal

State change to our component changing that state will then produce a new user interface and as long as that state

changes the same it doesn't matter how many times your app component renders it will always produce the same user

interface and we talked early on about how react is in charge of doing all of the nitty-gritty behind the scenes and

we as developers just get to worry about making sure that our state or our incoming props are being represented Ed

correctly so that what react produces in the user interface is well represented

correctly on the page as such it's really important that the code inside of our components is pure in other words it

doesn't change anything outside of its own system and this leads us to the next main principle which is immutability and

we've talked about this if we have a component that's receiving props it's very important in react that we never

change those props to anything else otherwise doing this means that our props are mutable and in functional

programming and especially here in react props are immutable the truth is state is also considered immutable which might

seem a little weird because we have been changing State quite a bit throughout this course but all it means is that

we're not going to be directly mutating State we're not going to change State equal to something else we will always

use the setter function that we receive with Ed state in order to make any changes in the end what's really

happening behind the scenes is it's not just setting state equal to something different it's replacing that state with

a completely brand new version of it which then causes our entire component to rerun with that new version of State

feels a little bit like splitting hairs but it's an important thing in react to understand that immutability is key

lastly and this relates quite a bit with the first one of pure functions but hopefully ties in our main concept here

is that our components in react should avoid side effects which just means that if we are going to run our app component

or create an instance of our app component like we do here then we need to make sure that it will not affect any

kind of outside system imagine if you will every time I ran this component it

made some sort of post request to add an item to a list in a database this would

prove pretty problematic because if react needs to render our app component I don't know hundreds of times if every

time it did it it was adding something to a list in a database case you probably understand why that's a bad

thing we could really end up with major outside problems if we were to allow our components to do anything like this okay

so where does that leave us well we are going to discover that side effects are still kind of an important thing for us

to have in our web applications we want to be able to mutate data in databases and do things like add values to local

storage or subscribe to websocket connections and so we need a solution in

react that allows us to a void side effects as much as possible but also to escape from that Paradigm whenever it's

necessary so that we can keep developing what we need to build so this leads us into the conversation of how we can deal

with side effects in react a really common thing that you

will need to do in your react applications is to fetch data outside of your own react app and in order for us

to fetch that data and then display that information on our page we need to perform at least two steps first of all

we need to fetch the data or get the data so we'll call this step number one and for number two we need to display

the data which requires us to save the data in State first we'll see what might

seem like an intuitive way to do this and then we're going to find out quickly why that's not quite the whole story and

we'll have a pretty major bug in our component I'm going to be using data from the Star Wars API it's just a

simple API that can return information about the Star Wars universe and we'll save that in state and display it just

as a Json object it's going to look more or less like this with a bit more information this is just stringified and

hardcoded this object but we'll replace that in a second okay well we'll take this naive approach first we'll go ahead

and fetch data from the Star Wars API this is the endpoint we can use to get the character in the Star Wars Universe

with the ID of one which happens to be Luke Skywalker and then fetch returns a promise so we'll go ahead and resolve

that promise which will give us a response back the response contains a bunch of extra information metadata

about the response itself the body of the response and so forth that body in this case is coming back as Json and so

I can pull the Json out and turn it into a JavaScript object and then I can get

that data and what I usually like to do is just console log it to see what it looks like okay let's clean up our notes

here let's hit save open our console and okay we got the data in everything seems

to be great all right well let's say instead of calling this generically state let's say this is Star Wars data

and we'll go ahead and set the Star Wars data and actually I've had a lot of

talking in these last few scrims so let's give you a challenge real quick all right this isn't practicing

anything new per se but I do want to get your hands on the keyboard as always so instead of console logging the data I

want you to save it in state and then display it to the the page essentially you'll just be replacing this hardcoded

object with the data that is saved in state for anyone in the no already yes this is not the correct way to do this

in react we're very soon going to see a problem that we'll run into but for now I'll put in a pause and have you work on

this challenge all right well instead of

console logging the data let's go ahead and call set Star Wars data with the data instead and we'll go ahead and

replace this object with the Star Wars data let's clean up the challenge text we'll hit save and it started at zull

you probably saw that pretty briefly and then it replaced it with the object awesome so what's the problem Bob this

seems like it's working great well we can highlight what the problem is by adding in some code here let's just put

in a console log that says rendered and keep in mind any code that we have inside of our component is going to run

anytime this component renders by react so let me go ahead and hit save and we

don't even need to open up the console to see that we are stuck in an infinite Loop we didn't notice this happening

behind the scenes but all of the code including this fetch request that we were running was happening many many

many times in the background let me comment out this render just so it stops uh displaying that to the page but even

though we're not seeing the rendered console log multiple times there is this fetch request happening infinitely in

the background in fact I'm going to comment this out so that we have an opportunity to talk about it okay this

one's going to take some critical thinking I'm going to put in a pause here and I want you to think about why it is that we are stuck in an infinite

Loop if we have this fetch request uncommented think back to everything that you've learned about how react

deals with State how it decides what should get displayed to the screen and how it decides whether a component

should be rendered or not so take a minute to see if you can figure out why we were stuck in an infinite Loop

when we had our fetch request uncommented and the component rendered it ran through the code here it

performed a fetch request or I should say it kicked off or started a fetch request because the fetch request takes

some time to complete it then came to this return and displayed this null on the page because we initialized our Star

Wars data as null then in what probably feels like an eternity to a computer the

response finally comes back it pulls the body of the response out and changes it into a JavaScript object and then most

crucially it sets that data to local state what is it that react does when we

change local

state if we change local state react will render this component it needs to

display the most updated version of state to the page so the component has to render however when we set Star Wars

data and we rerender this component a new fetch request gets kicked off when that one completes it sets the Star Wars

data which reenders the component which calls a fetch request which sets the Star Wars data which reenders the

component and we get stuck in an infinite Loop now I haven't hit save since I uncommented this so This fetch

request is not currently happening in the background but I'll just pre-warn you if you do want to play around with

this code if you hit save it's going to start kicking off this fetch request so just be aware of that so how do we avoid

this problem with how react deals with setting State and rendering if we want to include a fetch request that only

happens one time well this is the natural next step in our discussion about side effects and specifically a

hook that react gives us called use effect so let's Dive Right into learning

use effect and see how it can help us solve this problem that we're

facing let's kick off the discussion about use effect by looking once again

at what react's primary tasks are as we've discussed the main thing that it's in charge of is working with the Dom and

the browser in order to render user interface to the page very helpfully along with that it's going to manage any

state for us between render Cycles which gives us developers a way for a value to

be remembered from one render to the next and because we have state and we have props react is in charge of

updating the UI once again kind of like we talked about in the first point it will update that UI whenever the state

or the incoming props change there's a lot of other things things that react of course is doing behind the scenes but I

think it would be fair to boil down all of the very detailed things that it does to these kind of main tasks well this

naturally leads us to ask what can't react handle on its own and primarily react can't really do much regarding

outside effects some examples of this are interfacing with local storage if we're relying on a value from local

storage and that value changes one way or another react isn't automatically going to update itself based on the

changes from local storage I guess let me also be clear about local storage and the rest of the items in this list I'm

not saying you can't use these tools with a react application I'm simply saying react isn't automatically

connected to them and so we need to connect these things manually ourselves another example of an outside effect

that reacts doesn't automatically connect to is an API or any kind of database interaction we need to manually

call out to an API and receive the data that comes back in order to then display it on the screen this is exactly what we

we're doing with the Star Wars API along that same vein anything dealing with subscriptions like a websocket

connection react doesn't automatically know how to connect to outside systems or what to do if data were to come in

and change and so we need to take that into account as we're writing our code essentially this could just be boiled

down to basically anything that react isn't in charge of which is what we saw in the last slide so how can we deal

with these outside effects well that's where the use effect hook comes in whereas it's really important for our

react component components to be pure components and follow some of those principles of functional programming

that we talked about earlier use effect gives us a way to sort of create an escape hatch in fact Escape hatches is

exactly what the react docs talk about you can click on the screenshot here to go to this page talking all about Escape

hatches this goes beyond the scope of just use effect but if you scroll down to this section which says synchronizing

with effects it will talk about use effect a little bit feel free to read through this sort of as a reading the

textbook before class sort of thing and once you're ready we're going to jump into the syntax of use

effect let's learn how we can apply the use effect hook to fix the issue that we were having with our Star Wars data

rendering this component in an infinite Loop before we get started I want to give you a chance to go check out the

use effect documentation the screenshots that I had given you before talked more about how to use use effect this one

actually gives you the real syntax and so this would be a good chance to go check out the documentation before

running through the rest of the scrim we can see from the signature here that there are two parameters that we need to

pass to use effect the first one it calls setup which turns out to be a callback function and the second

parameter is optional that's what the question mark here means and it's an array of dependencies in this scrim

we're going to talk about the setup callback function and in the next one we'll talk about the dependencies so

let's come back to our code and if I uncomment this console log and hit save we can remember that we are are stuck in

this infinite Loop of rendering and the reason is because of this set Star Wars data line which is causing a render of

our component which is kicking off a fetch request setting Star Wars data and so forth in the infinite Loop let me

just comment out this line here and hit save that will stop the infinite rendering for now use effect is a

function that we can import from react in a very similar way that we were doing with react. usate we can call react. use

effect and as I mentioned there are two parameters the first one is is going to be a callback function now almost

exclusively these days you'll see this written as an arrow function like this but just in an effort to make this

completely transparent I'm going to put an inline function declaration like this and then we'll switch it back for an

arrow function later I think having the function keyword here makes it much more apparent that we're working within a

callback function what use effect allows me to do is inside of the code of this callback function I can put any code

that is going to have some kind of side effect outside of the react ecosystem system in the case of our fetch request

here where we are trying to get data from an outside system this would be the correct kind of code to put inside of a

side effect with use effect more specifically the code I put inside of this callback function is the code where

I want to synchronize data from an outside system with our internal react State now I have a confession to make

and that is that if we were to uncomment this setting Star Wars data line and hit

save we're going to see that we are still stuck in an infinite Loop so what went wrong how come our use effect

didn't solve everything let me actually go ahead and comment out this line again so on its face it would seem like

putting this code inside of our use effect made really no difference and the truth is without the optional

dependencies array which we're going to be talking about in the next lesson that's kind of true there is one minor

difference that I think is important to note at this point and that is that any code you put inside of this callback

function is guaranteed to only run after react has mounted your elements to the

Dom or in other words painted the elements from your component to the page we can get a glimpse into this if we

were to console log may be effect ran here inside of our callback function

we'll hit save we can see we first get rendered and then we get effect ran and the truth is that has nothing to do with

order if I place this console log below that one in terms of where it sits on the page we're still going to get

rendered first and that's because it's running through this code reaches this console log runs the console log renders

the elements to the page and then runs our function inside of our use effect so that's kind of a slight difference

between just having this code sitting outside the use effect similar to our console log here but for our purposes

when we uncommit this line we're still going to be running this effect function on every single render of our component

so let's dive in and talk about that dependencies array and see how it's going to help us solve this problem

I've made a small tweak to our little sample app here and that was to add this counter and a button to increment the

count and of course I changed this to dark mode for any of you who felt blinded by the last example that we had

the only reason I added a counter was so that we had a really easy way for us to force react to reender this component we

can see in the console that the first time we load this up we get the rendered console log here and then we get our

effect ran console log as well if I go ahead and click the add button we can see we get both of those console logs

running again this shows us that the use effect callback function we have is running on every single render of our

component which is why moving this set Star Wars data line inside of the use effect didn't solve our problem however

what we'll learn about now will solve this problem and that is the second parameter that we can pass to the use

effect function if by default the first parameter this callback function will run on every single render the second

parameter gives us a chance to stop it from running on every single render if we want it to and in practice you pretty

much will always want to include this dependencies array I can't think of too many times when you would want your use

effect functions to run on every single render so what exactly goes here well it is called a dependencies array so this

will always be an array of values that react is going to watch between one render and the next if any of the values

in this array change between those two renders then react will know that it should run this function again so let's

play with this for a second let me go ahead and put the count value that we're tracking in state as a value inside of

my dependencies array I'll click save we can see we got rendered and effect ran

so now we know that this effect will run on the very first render of the component and let me click the add

button and we see we got rendered and we got effect ran again let's dive even deeper and see what happened behind the

scenes the very first time this component rendered I'll hit refresh now so we reset our count to zero count here

was evaluated as the value of zero our console log rendered ran react then painted this div and its child elements

to the page then it ran this effect function and behind the scenes it's storing this array with the value of

zero so that it can compare the dependencies array on the next time this happens so I go ahead and click add now

what happens well this count value which remember it's saved as count react

incremented the count from 0 to one it painted the stuff on the page and then it looked at this effect function and

its dependencies array and this time the dependency count had a value of one and so behind the scenes react was looking

at what it used to be the last time this effect ran which was an array with a zero in this first index here or I guess

the zero index and then it compared it to what it currently has which is an array with a one inside and the logic of

react says well it used to be an array with a zero now it's an array with a one these are different from each other and

so I need to rerun this callback function again so as you can imagine it's called a dependencies array because

this callback function depends on the value that you're putting inside the parentheses here all right let's do two

things first of all I've been kind of changing this value of count I think it's important for us to remember that

this is still a variable it's not a hard-coded number but I think that can be a good practice for us I want you to

think what would happen if I hardcoded this as a zero I'm going to hit save we get rendered and effect Ran So I'll put

in a pause here click the add button and try to see if you could explain why it's doing what it's

doing okay I'll click the add button and this time we only got rendered logging to the console which means that this

callback function did not run this time so what's going on here well because I've hardcoded a zero inside of my array

the first time our component rendered it saved this dependencies array as an array with a zero inside and the next

time it rendered after we clicked the add button it compared it to the hard-coded array with a zero inside and

this time because these arrays contain the exact same data as each other react thought well I don't need to rerun this

callback function because nothing has changed nothing that this function depends on has changed and so I don't

need to try and synchronize with any outside system again because nothing has changed okay so that's the first thing

let's go ahead and set this back to count the second thing is let's go ahead and uncomment our set Star Wars data

I'll hit save and check it out we are no longer caught in an infinite Loop I'm going to put in another pause here and I

want you to try and reason through why it is that now that we have this dependencies array here we suddenly are

no longer stuck in a loop when we're setting our Star Wars

Data before when we were setting our Star Wars data it was rendering our component which was causing our use

effect function to run again because we hadn't taught it when not to run now our

count has not changed even though we're setting our Star Wars data and rendering this component which is why we got a

second rendered console log displaying because our count has not changed we are no longer making another fetch request

so now I want you to think what's going to happen if I click the add

button while clicking the add button is going to change my count value which is going to make it so that between the two

different renders my count value inside my dependency array will have changed and therefore I will be kicking off

another fetch request so let me click the add button and we can see that we did get rendered effect ran and then

rendered again it's a little hard to tell because the data hasn't changed since the last time but it did rerender

this and it did make another fetch request okay we are way too long overdue to have you do a challenge so let me

type out a challenge for you all right your challenge is to rewrite the use effect for now we're going to have it

rerun anytime the count changes so anytime this add button is clicked and for now you don't have to go fetch data

from the Star Wars API or anything like that you can simply console log effect function ran so give this Your Best Shot

see if you can remember how the use effect function

works I can create a new side effect in react by using react. use effect

the first parameter is a callback function before we were using a function declaration like this although I did

mention that the much more common way you'll see this is by using an inline Anonymous Arrow function so we'll go

ahead and switch to doing it that way for now I'm just going to copy this effect function ran console log and I

need to make sure to include my dependencies array so that it only runs when the count value changes let's clean

up this text we'll hit save I'll click add and we got effect function ran a second time okay if this is your first

exposure to use effect and react first of all congratulations on doing that challenge the syntax can seem a little

bit weird but second of all you might be wondering why are we putting count inside of this dependencies array we've

learned that the dependencies array can give us some control over when this effect function runs but it might not

seem super apparent why we're putting count in here and the truth is we probably shouldn't be putting count in

here so that's what we're going to be covering next

all right so we've learned that the dependency array gives us some control over when our effect function runs and

we learned that react is going to compare the values inside of our dependencies array from one render to

the next in order to determine whether this effect function should run again so how do we determine what we should put

inside of our dependencies array well I think if we take a second to truly understand what values we should putting

inside of our dependencies array it will suddenly start to click for us right now we have this count value in here and

that was simply to show that this effect function will run whenever we increment the count but if we look at our code

there's no code inside of here that depends on the value of count in order to correctly synchronize with an outside

system changing count is simply going to call another fetch request to the Star

Wars API which knows nothing about count nor depends on count to get correct data

so let's see what happens if we simply remove count from our dependencies array I'll hit save okay we can see we got

rendered which is the very first time our component rendered then behind the scenes react put this div and his

children on the page first with an empty array displaying as the data down here

then our use effect function ran and this console log ran which is why we see effect ran in the console the fetch

request kicked off it took a little while for the data to come back but eventually when it did we set the Star

Wars data with that data and react triggered another reender keep in mind when it ran this effect function it

looked at our dependencies array which was an empty array let me go ahead and type this down just in a comment here so

this was on the first render it had an empty array set Star Wars data triggered a render it did the whole render thing

and placed the new information on the screen with the correct Star Wars data then it looked at our dependencies array

this time around and what it did is it compared an empty dependency array to Another Empty dependency array when

it saw that nothing in these arrays had changed because there is nothing in the array it said I don't need to rerun this

effect because nothing that this effect depends on has changed and because we've removed count here count is also not

something that this code depends on so if I click add I'm simply going to get rendered every time and the effect is

not going to run anymore all right well we've learned quite a bit of stuff what I'd like to do is in the next couple

lessons I want to First do a quiz that we can talk a little more high level about what use effect is helping us with

and then we're going to have just a small series of challenges to give us some more practice in understanding use

effect all right it's quiz time again just like before read through these questions click into the editor and type

down your answers for question number one it's been a little bit of time since we talked about functional programming

and pure functions so don't hesitate to open up that lesson on functional programming in another T tab or

something and review that before answering this question in the quiz so go ahead and answer the questions in this

quiz okay number one in what way are react components meant to be pure functions and actually I'm going to pull

up my old slides on this one right here the idea of the pure functions was to

say that a component when it's given certain props should always return the same user interface and the same thing

holds true of a state change or any internal state in the component given the same state values or the same props

values it should always return the same user interface and so that's the main idea of pure functions in react so given

the same props or state a component will always return the same content or the same UI that gets rendered on the page

another aspect of having pure functions in react is that rendering your component or running that component

function will never affect any kind of outside system we talked previously and

imagined a scenario where maybe our component every single time it rendered were to add an item to a list in a

database this would be very blatantly not a pure function because every time it runs it adds a new item to a database

which means we are very much affecting an outside system so that's just another important aspect of having pure

functions in react that leads us very naturally to what is a side effect in react and what are some examples well

really side effect is any code that affects or we could even say interacts

with an outside system it's a little nuanced but even doing a get request to

an API is considered a side effect even though we're not really making a change to that outside system simply

interacting with the outside system makes it a side effect in the realm of react components some examples of this

might include interacting with local storage anything dealing with an AP

or making a connection like through web sockets one we hadn't really talked too much about was doing any kind of manual

Dom manipulation all of these are services or systems that exist outside of react and so interacting with them

inside of your components is considered a side effect in react so number three by contrast what is not considered a

side effect in react and what are some examples well in this case it's really anything that react is in charge of some

examples of which are maintaining State keeping the UI in sync with whatever

data you're working with rendering Dom elements and certainly there's a lot of

other things that react is in charge of but all of those would be considered not side effects in react all right number

four this is kind of the meat of this quiz when does react run your use effect well it will always run your use effect

code as soon as the component loads or let's say renders and more specifically

it's when it renders for the first time this most commonly happens when you first refresh your page or launch your

app and it gets loaded into the browser for the first time although it could also be if you were conditionally

rendering something and it was not present on the page before but then some State value changes and it becomes

present on the page that would be considered the first render for that component react will also run your use

effect function every time a component renders assuming you have no dependencies array

so on every rerender of the component assuming no dependencies array and maybe to answer this next one when will it not

rerun the effect function well that's going to happen if between renders the values in the dependencies array have

not changed and lastly how would you explain what the dependencies array is well

spoken more literally it's the second parameter to the use effect function but more importantly it's a way for react to

know whether or not it should rerun the effect function I know it probably feels like I'm

beating a dead horse with this use effect thing the reason I do this is because I do find that use effect tends

to be the most confusing Topic in react not only for beginners but is widely misunderstood by even seasoned veterans

in react I really want my students of this react course to come away from the course having a pretty solid

understanding of use effect when to use it when not to use it and so we are going to have a short series of

challenges that will do to help us really drill in use effect as well as another aspect of use effect that we

have yet to learn along the way we're also finally going to come back to our meme generator so we can apply what

we've learned regarding use effect to that

app all right in order to get our repetitions in the first part of your challenge is to write our use effect

from scratch I want you to fetch the data from the URL that is right here and save it in the Star Wars data State

while you're doing this make sure you don't get stuck in an infinite rendering Loop like we did before go ahead and get

started on the first part of this

challenge I'm going to copy this URL and then just get rid of this challenge text

and in its place we will call react. use effect I'll put a callback function as

my first parameter and before I forget I'm going to put my second parameter as an empty dependencies array we'll

revisit this and determine whether or not we need to add anything to that dependencies array what I want to do is

fetch the URL that I copied we'll say then we'll get the response and we'll

pull the JavaScript object out of that and then we will take the data that we

get and we will set Star Wars data with that data now before I hit save I want

to think to myself anytime I'm creating an effect what does this effect rely on are there any values that I need to make

sure I include in my dependencies array so that if that value were to change I might need to fetch new data or do do

some other kind of interaction with an external system and in this case no none of the values that I'm using inside of

my fetch request rely on anything outside I just want to get the data that lives at this URL so by putting an empty

array essentially it's like saying I just want you to do this fetch request the first time you mount and then you

won't have to do this fetch request again later we'll hit save we start with an empty object very briefly and then

the data comes in and we fill it in with the data from the Star Wars API okay that should have just been repetition

there the next challenge we do will expand upon this a little bit more okay I've made a couple really small changes

here first of all I'm beginning my count value at one and secondly I've changed the text of the button to say get next

character notice that the URL on the Star Wars API says SLP people SL1 well

this SL1 is the ID of a character in the Star Wars database and if I were to do

two or three or four or five I would get new characters being return to me through my API request so what I want

you to do is to combine the count value which has up until now been kind of a silly way just for us to trigger renders

and make it so that when we click the get next character button it will change this one to a two or a three or a four

whatever the count currently is and get new data for that new character while you're doing this remember to consider

your dependencies array what may or may not need to be in there all right go ahead and give this challenge Your Best

Shot

well the first thing we want to do is not have this one be hardcoded so I'm going to use a template string and

simply replace my one with some interpolated value of the count I did

change this from a zero to a one because I don't believe there's a character with an ID of zero so let me hit save and we

should see that okay we're still getting Luke Skywalker because this was set to a one if I instead were to hardcode the

initial value for my count state to a two and hit save we should get yes a new character C3PO okay well we don't want

to start at two let's start at one and I'll hit save before I make any kind of change to the dependencies array and

let's go ahead and click get next character okay we see that the count is two but our data did not update and

that's because our use effect doesn't know that it should be watching for changes to the count value in order to

determine if this function should run again but we actually are depending on the count value now before we weren't

but now it does matter if count changes we need this effect to run again so that we can accurately reflect the new

information on the screen so in my dependencies array I'm going to add my count value we'll hit save we get Luke

Skywalker and I'll click get next character and there it is we get C3PO we

can go to the next one R2-D2 Darth Vader Leo Orana and so forth I really hope

this hasn't been Overkill and I hope that use effect is at least starting to become clear if it hasn't clicked quite

yet the more you use it and the more honestly bugs that you find with use effect the more solid your understanding

of it will be as I mentioned we do still have some more to learn about with use effect but it's been so long since we

have seen our meme generator project that I think we should go back to that apply what we've learned and honestly I

think once we have done that we'll mostly be done with that project it was a pretty quick one so let's jump back

into the meme generator with a

challenge okay everything that we've been learning about use effect has led to this moment the way that we are going

to structure this app is that as soon as the app loads we're going to make a call to the image flip API and I've included

a screenshot of the documentation as well as a link you can click this screenshot to go to this link and you'll

need this in order to complete the challenge that we have so the way that this app is going to work is as soon as

our app loads it should make an API call to the image flip API and it will get an

array of memes so it's not going to be that when the user clicks get a new meme image that it makes an API call but

instead when the app loads it will get I think it's like a 100 memes then clicking the get a new meme image button

will simply randomly choose one of the items from that original array of 100

memes that we got when the app first loaded the only reason that we're doing it this way is because I don't think

that the image flip API has an endpoint to just get a Rand random meme image at

least not one that's free so this will work for us for now and your challenge is to write the code that gets an array

of memes from the image flip API as soon as the component renders for the first time again you'll need to check the

image flip documentation in fact I'm going to leave this up for just a second so you have a chance to click here and

when you get there you'll find the correct URL that you'll need to call in order to get that array of memes once

you've gotten the array of memes back you'll need to save it to state so that we can access it from the opponent and

react at this point I don't need you to worry about this get a new meme image button and I do want to give you some

fair warning if you're tempted to use an async await function I'm going to ask you not to do that but instead to use

then in order to resolve the promises that come back from Fetch we're going to learn why after this challenge all right

your time to shine get started on this challenge to get the array of memes from the image flip

API well since we need to kick off this request as soon as the component loads

this would be a great time for us to use use effect this is an example of a side

effect in react because we want to synchronize our local state from within this main component with an outside

system which is the data that lives at the image flip API so I've imported use effect from react and I can call use

effect here the first parameter is a function and because it's the more common way you'll see it I'm going to

use an inline Arrow function and before we write this code I'm going to immediately start thinking about the

dependencies array that I need to include here so what does our side effect of fetching data from the API

depend on in order to make sure that it is correctly syncing the data from the

image flip API with our internal State well in our case it doesn't rely on anything it doesn't depend on anything

in order for that sync to happen correctly in other words there isn't any local state that if it were changed we

would need to go refetch data so that it was correct in our we're simply getting a list of 100 memes and we're going to

be using that list for our app so I want to make sure I include the dependencies

array because I don't want this fetch request to happen every single time State changes and the component

rerenders which remember happens every time we type in the input boxes here so I need to make sure I include this and

effectively this is like saying I only want you to run the side effect one time when the component first mounts all

right so what do we want to do we want to fetch and if we go to the documentation we can see there is an

endpoint called getor memes and we can find the url there and so I'm going to

paste it in it's just this one for the api. image flip.com sget memes and I

need a closing quotation mark there and as I mentioned for now we are just going to resolve this with a then chain we get

a response back from Fetch and we will need to call res. Json that's going to

parse the Json body that we get from making this API call into JavaScript and

we can access that with data or this is just a parameter you can call it whatever you want let's go ahead and

console log this data okay we'll hit save I'll open up my console and perfect

it looks like we get the data correctly if we look closely the data that comes back is an object it has a success

property and I guess confusingly because we chose to call this data it has a data property which is an object that has a

memes array and so that's how we need to dig into this response data to access the array of memes so again I guess kind

of confusingly it's data. dat. memes by the way quick side note when I hit save

it's refreshing our app which is kicking off yet another fetch request however refreshing your browser is something

completely different than just changing State locally there's a difference between clicking refresh which reruns

all of the code from react and changing state where react simply determines what needs to reender to the page but doesn't

refresh your browser so that's just why hitting save and refreshing is causing the fetch request to run again and this

time it looks like in the console we accurately got the array of memes if I scroll down here it's uh it's pretty

long in fact it's long enough that it doesn't even show everything here in scrimba by the way if you're following along here in scrimba you can open your

developer tools and anything that we conso log here will also conso log in your developer tools so that can be a

good way to look into more complex items that we're console logging like this array here okay well we don't want to

console log it we want to put it in state and that state does not exist so we're going to create a new one maybe

we'll call this let's call it all memes and we'll pull in set all memes is equal

to use State and this is going to be an array so I'm just going to initialize it as an empty array and then instead of

console logging we'll call set all memes and yeah we want to set this array in

state let's close our console since we're not console logging anymore we can get rid of our challenge text and

actually I'm going to keep this hint here for now because we're going to talk about that in a second I can hit save

it's not going to be very clear that this is actually working but I trust that set all memes is working the way

it's supposed to work so why did I give you this hint that says not to try and use an async awa function if you're

familiar with async AWA it might have been tempting to say well I want to use await for resolving these promises and

so I want to make this function an async function so I can use the await keyword and make this code a little bit tidier

if you're not quite as familiar it allows you to do something like this where you say well the response is equal

to await the finishing of this promise and in this case response would also be

a promise so we can say const data equals await res. Json and then we can

simply set all memes to data. out memes like this this is quite a bit tidier I

personally like using async functions however when you're using use effect you can never make this function an async

function so before I screw everything up let me get rid of all this and in the

next couple lessons we are going to talk a little bit more about use effect because there is a really important aspect of use effect that we have not

yet had a chance to cover and understanding it is going to explain why we can't make this into an async

function and what we can do to work around on that limitation so once you've had a chance to make sure that what

we've done here makes sense I will see you in the next

lesson we'll start this one off with a pretty simple challenge just to get your fingers typen on the keyboard and make

sure you're awake we have this very simple app that has a button with the text of toggle window tracker and then

we have a window tracker component notice that the button isn't currently set up to do anything that's going to be

your challenge over in the window tracker component right now is just displaying this H1 that says window

width and then it displays the window width at the time that it was rendered we'll notice that if we change our

window width the display doesn't actually update but if I were to refresh we would get a new value of 494 here

we're going to address this a little bit later for now though we can just focus on this first part of the challenge the

first thing I want you to do is to create new state called show and default it to true then I want you to make it so

that when you click the button it will toggle that show value and thirdly you should make it so that you only display

this window tracker component if show is set to true I'll hand it over to you now to work on this

challenge all right let's go ahead and create some State we'll say react. use

State and I'm already seeing I'm going to have to import react from react in order to do that react. use state is

going to give us some values back so we'll say show and set show is equal to

react. State and we'll default it to true all right and then we need a function so that it will toggle it I

could either do this in line with my button or my personal preference is to make a named function out here so I'll

say function toggle we'll call set show it will look at the previous value of show and just return the opposite about

as simple of a set State function you can have I'll add the onclick event to

my button that calls toggle and lastly I need to conditionally render my window

tracker so that it will only display if show is true so I'll go ahead and use

the double emper sand method let's clean up our challenge text hit save and

toggle window tracker okay perfect now let's take a look at something if I go to window tracker remember that this

window. inner width is being calculated as soon as this component mounts to the

page which in our case will happen as soon as we refresh the browser so I refresh we're at 418 if I resize this a

little bit and refresh it recalculates we're down to 390 however I also can

toggle my window tracker off change my window size and toggle it back on and we'll see that we're at 470 and actually

I don't have to toggle it off first I can resize it we'll notice that the 470 doesn't change but if I toggle it off

and then on we get the new value so why exactly is it doing that well when I toggle it off it's being completely

removed from the page I'm not just hiding it from View and CSS or anything it's actually getting removed from the

document itself and so when I put it back on the page this window. inner width is being evaluated again and the

new inner width of my window is being displayed however we can do better than this if we want this number to display

more in a live fashion while I'm updating the width of the window what we can do is listen for a dedicated resize

event on the window itself and then add some state to our window tracker and

update that state with the window. inner width every time the window is resized or rather every time the window resize

event triggers by updating our state on our window tracker we can have react rerender this component and give us a

live view of what the current window inner width is however because I need to run this event listener on the window

itself I don't have a dedicated on resize event like we do with other Dom

event listeners like we have been using th far so in order to add this resize

event listener on the window I'm going to have to do some more manual imperative Dom manipulation and because

I'm going to be interacting with a system outside of react Itself by trying to interact with the window of the

browser I want you to think for a second what tool does react give me so that I can interact with those outside systems

and sync the internal State and react with

it that's right it is use effect so I can go ahead and use react. use effect

I'll put my callback function inside here and when we try to think about our dependencies array one thing that can be

really tempting is to try and look at window. inner width and say well anytime

window.in width changes then I want to rerun my effect to synchronize window.in

width with the state that we're going to set up in the future however something that's important to remember is that

window. innerwidth is actually a static value right now it's 388 so this would be kind of like me putting in 388 as a

hard-coded value here and then we have to remember that when I resize my window I'm not telling react to render anything

I'm not changing state or doing anything like that at least not yet so as tempting as it might seem putting the

window.in width in there isn't going to be the solution here so let me go ahead and get rid of that so instead of that

we are going to add our event listener on top of the window so I'll call window window. addevent listener and the event

that I can listen for is actually called resize and we'll pass a call back function that will run anytime the

resize event happens and for now let's just go ahead and console log resized

all right let's hit save I'll start resizing and look at that we get our console log running every pixel I think

essentially that the window gets resized all right well the next step is something that I think you should be

able to do pretty easily by now so I will type this out as a challenge all right here's your challenge first of

all I want you to create some State called windowwidth and default it to the window.in width as its initial value

then whenever the window width changes you should update that state to the new window.in width and then down here below

instead of displaying window.in width you should display the new state that you created so that it updates every

time the window width changes in the end you can see what we're doing is we're interacting with an outside system by

adding a manual ad event listener to our Dom and then syncing our local state to

the source of Truth which is the outside system that we're grabbing the window. inner width from by syncing internal

state with it we'll be able to actually display to the user the value from that external system or the window in this

case all right it's your time to shine go ahead and get started on this

challenge okay let's call react. use State and I'll create cre the variables

that I'm going to save this as this will be my window width and we'll call it set window width

we'll initialize this to the window. inner width as the initial value then

instead of console logging resized I'll call set window width and in this case I

don't really care what the previous value is I can simply reset it to whatever the current window.in width is

when this event was called then lastly I setting window width and state but I'm not actually using it anywhere so I will

replace window. inner width with the state value of window width let's clean up our challenge text hit save and we'll

try resizing the browser and look at that our window width is accurately reflecting on the page for the user to

see well now let's take a look at a little at a little bug we

have remember our window tracker component is only displaying if the parent

great job on these challenges unfortunately I have some bad news and that is that we have a bit of a bug in

this in in our code and the bug exists over in our

window tracker but because this lesson has gotten a little bit long we are going to talk about the bug and what the

main fix is for it in the next lesson

we have a pretty sneaky bug that lives in our window tracker component right now and it's not immediately apparent

what the problem is using the app makes it seem like everything is working just fine we get our window width updating on

the page we can toggle it on and off if it's off we can resize and it doesn't

look like anything's happening so what's the problem here well we can highlight it if we were to add a console log back

into our resize event let's just say resized I'll hit refresh if I resize it I'm going to try and just resize it one

little section I think it'll maybe go by two pixels okay so we got a single console log running well let me toggle

off my window tracker I'll do a resize we'll do a single Pixel again okay it's still resizing even though my window

tracker component doesn't live on the screen okay well what happens if I toggle this back on and off a bunch of

times and then try to resize the browser right now we have two resized in the

console I'm going to go just a single Pixel here here and take a look at that it looks like we got seven new resized

console logs showing up just by doing one resize event so why the heck is this happening well remember use effect gives

us a chance inside of react to interact with or sync state with some kind of

external system in this case when we're adding an event listener to our window object this is happening outside of

react I'm registering an event listener with the browser when I toggle the window tracker off I'm not giving any

kind of instruction to the browser to say hey I'm done with that event listener you don't need to listen

anymore when I toggle the window tracker back on it's remounting the window tracker component and in the first time

that it mounts it's adding another event listener kind of a silly analogy I came up with I imagine myself walking into a

store asking a store employee if they have I don't know a certain item in stock by doing so that employee has to

go maybe back into a warehouse to check to see if they have it in stock and in the meantime if I just kind of abandon

my cart and leave the store at no point did I tell the worker that hey I actually don't need you to do that work

anymore and kind of to stretch the analogy a little bit thin when we toggled our window tracker on and off a

bunch of times it's kind of like me going from one employee to the next asking them to go do a task for me and

then just kind of leaving them and not needing them to complete their task because we're creating a side effect in

react it's really important that if we reach a point where we don't need to inter interact with that outside system

anymore like for example if we're toggling off our window tracker then it's really important that we clean up

any of the side effects that we have created in this case we're adding an event listener it's going to be

important that we remove the event listener if instead on the mounting of our component we had created a websocket

connection with a server then it would be important if we unmount that component to disconnect that websocket

connection fortunately in react this is a pretty easy task Remember When when we created our use effect we passed a

callback function as the first parameter to use effect but as it stands we're not currently returning anything from this

function so you might be wondering well what does react do with the value that we return from the function that we

passed to use effect and as it turns out what we can optionally return from a use effect is a function in fact just to

make it abundantly clear in the syntax I'm going to use a function declaration like this so behind the scenes react is

going to call the function that we gave it and it's going to save as a variable the function that we return from our use

effect callback function and when this component gets unmounted and react determines that it's time to potentially

clean up any of the side effects that we have created in our use effect it will take the function that we give to it and

it will just run the code it doesn't know what's in that code so it's up to us to make sure that we clean up any of

the side effects that we created in the first part of our function with the ad event listener method there is sort of a

sister method called remove event listener and in order to make that work I have to pass it the exact same

function that I used when I was setting it up so in order for that to make sense I'm going to have to move that function

into its own named function and let's give it a name maybe watch window width

I can pass this named function to my ad event listener so that's working again and then in my cleanup function from my

use effect I need to call window remove event listener and I'm going to remove

the resize event listener that we created and need to pass my watch window withd function so that it knows which of

the functions it needs to remove Let's see we still have our console login here so we should be able to test to see if

this is working I'll hit refresh let's resize just to make sure we're working okay okay we got four of those that's

cuz I moved it a few times if I go really slow I can get it to do one at a time let's clear that out I'll turn off

my window tracker and we'll try resizing okay we're not getting our console log I'll also kind of turn it on and off a

bunch of times and now it's on let's try to resize it just by a little bit and

sure enough we only get the console log running once so as a recap because we have an empty array here we are just

calling this use Effect one time when the component first mounts to the page when we do that we're setting up an

event listener for the resize event on the window object and it's going to run this function if the resize event ever

happened then we're returning our cleanup function which says if this component ever unmounts just run whatever code I

put inside of this function so that I can be sure I don't have any of these side effects just kind of floating

around inside my browser so as long as my component is on the page this event will work just as we might expect as

soon as it leaves the page react runs our function which removes the event listener and therefore I no longer get

my resize console running in fact one last thing that we can do just to see for sure that this is happening is if I

add a console log inside of my cleanup function saying cleaning up let me hit save we can trigger the resize event

like this okay we get resized and then when I toggle it off I get cleaning up

so one final recap before we move on use effect allows us to interact with outside systems and potentially have

side effects inside of our react code which normally should be side effect less it takes two parameters the first

one is the effect function and the second one is the array of dependencies that determines when that effect

function should run again at bare minimum if we include an empty array it will only run the first time this

component mounts to the page because it depends on nothing else to rerun and at the most if we were to not include this

array at all it would run on every single render of this component in fact we can delete this dependencies array

and hit save will see that it's going to run both resized and cleaning up every

single time this component renders you will pretty much always want to include a dependencies array and think very

carefully about which values you want to be watching in order to trigger this effect again then lastly the Callback

function as the first parameter to use effect is allowed to return a function which will clean up any of the side

effects that you might have created inside of your use effect code returning this cleanup function is something you

will want to always be aware of but it isn't something you always have to do it's relatively common to have your side

effects not have anything that's lingering and needs to be cleaned up so just know that it's here as a tool for

you to use if you need it but it's not something that you absolutely have to have to correctly write a use effect as

always if you need to go through the content that we've been talking about with use effect that's completely okay

it is what I have found to be one of the most confusing topics not just for beginners in react but for even seasoned

react veterans use effect is great as a tool whenever you absolutely need it to kind of have that escape hatch from the

react ecosystem and the react functional programming Paradigm but it is something that can be commonly abused for those

who don't really understand what it's for or what the common workarounds are for it with practice I know that you are

going to be an expert when it comes to understanding effects in

react we're actually going to have a chance to apply what we just learned about use effect and the cleanup

function to our Chef Cloud app from the last section but before we find ourselves juggling too many things I

want to tie a nice little bow on our meme generator because currently our get a new meme image button doesn't work

we're saving the array of all memes in state but what we need to do now is randomly choose one of those meme images

when the button gets clicked this is going to be more of a quick algorithmic challenge rather than dealing with any

side effects but I really want to finish off this app so we can move on from it so let me type out a challenge for you

all right your challenge is to get a random image from the array of all memes when the user clicks this get a new meme

image button once you have gotten a random image from the array make sure that you write whatever code it is that

you need to write so that the image you selected will display on the page as I've done a few times I'm being a little

bit vague because I want you to think how that's going to work so go ahead and give this challenge Your Best

Shot let's work in the same order that the user is going to be interacting with the page so down on our button see

that's right here let's add an onclick event listener for a function we have not yet written we'll say maybe call it

get meme image so let's go ahead and write this function just going to do that in place of the challenge text get

M image and this is where it's kind of just an algorithmic challenge so what I can do is get a random

number from Z to the length of the array we'll just say array. length then we

will use that random number to get a

random meme object from the array and then we will need to set State and

that's the state of the current meme which is the object we're saving in state up here all right so let's get a

random number we can just say const random number and honestly getting a

random number is something I sometimes have to look up but we can simply say math. floor math. random times all

memes. length if you've never seen this before in JavaScript maybe just copy this line and paste it into chat GPT and

have it explained it to you it's not too terribly difficult to understand but it's enough to know that this will get a

random number between zero and the highest index in our all memes array

which means we'll never try to index outside of the array so that was that step we want to use that random number

to get a random Meme and I think I can just do this together we'll say maybe

New Meme URL is equal to all memes at the index of random number and those

meme images have a URL property you weren't like expected to know that per se but along the way of doing this

challenge you probably wanted to console log the New Meme that you index into or console log all memes just to see what

the structure of each one of those meme objects was and you at that point should have seen that there's a URL property okay and

then we're going to set the state well we're setting the state of an object and we don't want to lose the top text or

bottom text so I'm going to say set meme I need to know what the previous meme

was and I'm going to return a new object that has all of the properties from the

previous meme but changes the image URL to the New Meme URL this should be

straightforward enough for you at this point in the course if not that's completely okay but it is probably a

good indication that you need to do a little bit more studying and a little bit more practice before just kind of plowing ahead with the course okay let's

test it out we'll hit save get a new meme image and awesome okay we got a new

meme image and this is going to work with all of the images from that memes array again as I mentioned some of the

memes don't just take a top text and bottom deck so it'll be a little bit hit or miss how funny these memes that you

create are awesome we can mark the generator as completed I'm sure there's other things that you could decide to do

with this project and as always feel free to do that play with this code add your own features and most importantly

go to the scrimba Discord and share your awesome work okay I want to jump back for just a few short lessons to the chef

Cloud project because now that we understand use effect there's a little but really nice feature that we can add

to that project so once you've had a chance to say goodbye to the meme generator let's continue forward

I wanted to go over a pretty truncated view into refs in react and the used ref

hook I say it's really truncated because we're going to be going through it pretty quickly only because I have an

improvement that I want to add to our Chef CLA app that will require us to use refs and actually this reminds me before

we move on I was getting a little bit bugged that we had not moved some of our components that really should be in a

components folder and really quick before we jump right into the slides I did make a couple really simple changes

to our Chef Cloud app primarily I moved some of the components into a components folder I think before I maybe had the

main component and the header component sitting outside in the project route but they felt a little more natural inside

the components folder so I moved them there and then fixed the references that we had with our relative paths in each

of those components that needed them just wanted to make sure I highlighted that before anyone got confused why it was looking a little different okay so

what are refs in react and is use ref refs are fairly straightforward they are very similar to State except for two

major things the first one is that you can mutate refs directly with props or

with State we know that it needs to be immutable and the term immutable might not on its face make a lot of sense

because you might be thinking well we do change State all the time that's how we trigger reenders and react but to split

hairs when I'm talking about mutable I'm saying we're not saying something like okay here's my ingredient State and I'm

going to push a new item to my list of ingredients this would be directly mutating State when we know that we're

supposed to use the state Setter function behind the scenes react is not just setting our old ingredients array

equal to something new or doing something like push it's following a more appropriate functional programming

Paradigm where behind the scenes it's replacing the old version of state with the new version of state and then kind

of queuing it up to render the page so let me get rid of this line and refs on

the other hand are things that we can mutate directly we can just set them equal to something different and maybe

more importantly for US changing a ref doesn't cause a render and react for

reasons that might not be immediately apparent refs tend to commonly be used for accessing Dom nodes without needing

to assign IDs to them and Run Dom manipulation commands like document. get

element by ID or query selector refs give us a way to access those Domino creating a ref in combination with using

a ref prop which we're going to see in just a minute give us a chance to do some of those manual dumb manipulation

tasks and again the reason for this might not be immediately apparent but that's okay we're going to get to it I

did mention this is a very highle overview of refs I do dive a little bit more deeply into refs in my Advanced

react course which is kind of the natural progression after this free intro to react course where in one of

the sections I cover refs in a little bit more detail and give you a little bit more practice with them all right why am I talking about all this in our

Chef CLA app we are getting our recipe we can click the get a recipe button and

if we look very carefully we'll see that the scroll bar when the AI finally gets back to us the scroll bar on the app

will appear and we can scroll down and see the recipe however as far as the user experience goes it's not that great

we don't really give a clear indication to the user that the recipe has finally loaded and unless their page just

happens to be a little bit longer like we see here in this case it's a little more obvious they can click get a recipe

and what used to be blank will then become populated with the recipe once it's loaded but I don't know that we

want to bank on this because their browser might be a little bit shorter like this so what can we do well there

is a domod property we would just I'm putting Dom node here as a placeholder

called scroll into view and as the name suggests when you select a Dom node and

you call scroll into view on it the browser will automatically jump down to that section so if our Dom node were

this entire recipe section whenever scroll into view is called the browser will jump down so that that sits at the

top of our view and actually for us that might be a little more jarring we might want to have this section be what we

scroll into view just so that it's a clear transition between where they see it here at the bottom and they'll still

be able to see it here at the top so the trick is how do I get access to this Dom node well in vanilla JavaScript all we

would do is we would add an ID to one of our elements and then we would call a get element by ID and that might be able

to work for us just fine however react is really centered around having reusable components we haven't spent too

much time talking about reusability that actually is another Topic in my Advanced react course that we spend quite a bit

of time talking about we go really in depth on reusability in react but the point is if I were to reuse this

component or render my main component for whatever reason multiple times I would end up with two elements that have

the same ID on the page and if you know anything about HTML that's just a no no you're not supposed to do that so this

is where refs come in refs give us a chance to access a Dom node so that we can call methods like scroll into view

and they are easy enough to create when we use the use ref hook in react so I'll

go ahead and create a new ref here since we are allowed to mutate our refs directly I won't need to do the same

thing I did with use state where I'm given a state Setter function but instead I can just give my ref a name

let's call it the recipe section because I'm going to be scrolling down to the recipe section and we set that equal to

react. use ref kind of a standard practice if I am using my ref to set on

a Dom node I'll initialize it as null and now that I've done that what I can do is take any element that I want to

have access to the native domod of and I can set a special ref property now I

don't actually want to put it on the input but I'm just using this as an example ref is a dedicated property in

react it's set aside for the use of setting these refs on Dom nodes and so

if I did want it on my input I would say ref equals curly braces recipe section

just like that now let's get it off this input this isn't actually where we want it let's think where is it that we do

want our ref to exist remember the purpose of the ref is so that we can call scroll into view on it when the

recipe loads so that the browser will automatically scroll down and I think we decided that this ready for a recipe

sort of call to action would be a good place to scroll down to so where does this live I think we ended up putting

this inside of our ingredients list so if we go to our ingredients list sure enough here's this section and we have

this div right here that says ready for a recipe that's this div right here on the page so this is where I'm going to

set my ref I'm going to say ref equals curly braces and we don't have access to

this ref recipe section quite yet because it exists on the parent component that is rendering ingredients

list so I want you to think how can we get access inside of this child component to the recipe section ref

which currently only exists inside of our main component what mechanism do we have in react to get access to that if

you said props then props to you that's correct so here is our ingredients list

we can go ahead and say we're creating a new prop called ref now I don't want this to be confusing because I did just

say that ref is a dedicated property in react it means something special but I

probably should have qualified that it only means that if it's put on a lowercase regular react element kind of

like how on a button lowercase b button I can say onclick and this is the actual

event listener whereas if I'm working with a custom component like ingredients list if I say on click all I'm really

doing is creating a new prop a custom prop that just so happens to be be spelled exactly the same as the native

Dom property for onclick the same exact thing goes with ref so I'm going to set ref equal to recipe section that's the

ref that we created up here above and this means that I can go to my ingredients list and we need to make

sure yep we're receiving props and I'm going to be receiving this through props

do ref because that was the name of the ref that we gave it in this case because we're working with the lowercase D div

regular native Dom element or what will get turned into a native Dom element this ref does mean something special all

right well this lesson is growing a little bit long so let's go ahead and do this I am first going to just console

log recipe section so we can get a better idea of what this ref looks like and we're going to open our console

because we need to look very closely at something I'll hit save down in our console we see that recipe section is an

object that has a current property I'll be completely transparent here I'm not entirely sure why refs when they're

created are always objects with a current property but that's just something you'll have to get used to the

reason it says null is because that's what we initialize it here if I were to instead say this is a string and hit

save we can see now it's an object with a current property and its value is the string that we initialized it with so

that's all that's happening down there let's change this back to null I'll hit save and now I'll click get a recipe

we'll wait for the API to return its response and now take a look at this our recipe section ref is now an object with

a current property but the value of that current property is a div now scrimba console is representing this almost like

a jsx element div but it's really representing a native Dom element for the div where we set our ref inside of

our ingredients list right here okay this lesson has gotten quite long I do have a challenge for you and it's going

to hearken back to use effect so once you feel comfortable with what we've done here again I know it's been kind of

a whirlwind we will jump right into that and actually Implement our scroll into view

feature one thing I realized I might need to clarify is why when we first render our page the recipe section ref

is set to null or the object with the current property is set to null in my case here because I am console logging

it immediately after it's created on line 11 it's still set to null and react

hasn't yet had a chance to render the elements on the page as soon as the elements on the page get rendered

ingredients list gets rendered which then includes this section down here where the ref is being stored at that

point the ref is then immediately stored as this div but we're just not getting a chance to see that because we are conso

logging it before anything has been rendered to the page clicking the get a recipe button when the recipe response

comes back it sets State and it reeners the component which then reruns our

console log line and we get to see even though it's a little bit delayed the fact that the ref has been accurately

set on that div in fact I think we could also see that if we just add another

ingredient here I'll hit enter and yeah sure enough in the console we can see that the recipe ref is set to the div

just wanted to clear that up just in case anyone was confused why it was initializing as null okay let's apply

refs so that we can add the feature that we want to add where the page will scroll down so the problem that we have

is that we want to scroll down to this ready for a recipe section only after the claw recipe section is rendered to

the page or in other words when recipe as we're initializing it is not an empty

string anymore maybe keeping in mind that that this is a section all about use effect I'm going to put a pause in

here and give you a chance to think from a highle architecting overview what might need to happen in order to solve

this problem or add this feature if we think about it we are hoping to create a bit of a side effect because we want to

scroll the browser down which involves doing a manual Dom node method call and we want to synchronize that action or

that side effect with a value that react is holding in state with recipe and so

this brings us to your challenge I want you to add a new side effect that calls recipe section.

current. scroll into view but it should only do this if the recipe is not an

empty string and if recipes section. current is not null that's an important thing we'd want to make sure we can't

scroll it into view if if recipes section. current is not the div Dom node

but is null we're going to get an error if we call scroll into view so we need to make sure of that as well the

important part of this challenge is I want you to think carefully about what values you would want to include in your

dependencies array what will this side effect actually depend on in order to perform its action correctly once again

I'm being a little bit vague I want you to put on your thinking cap and give this challenge your best shot so go

ahead and start working on this challenge

all right well to create a new effect we're going to call react. use effect

alternatively of course we could just destructure that from the react Library up above use effect takes two parameters

we have a function and a dependencies array let's worry about the dependencies

array next we'll first work on this function so the clue to the code we're going to have here is written in the

challenge text if the recipe is not an empty string so we'll need to add a conditional here if the recipe does not

equal an empty string we could theoretically also just say if recipe is a truthy value I think I'll opt to be a

little more explicit and specifically say if it's not an empty string and

recipe section. current does not equal null once again I probably could just

say and recip section. current but we'll stick with being explicit here if those things are true then I know that I want

to call recipe section. current. scroll

into view well let's think carefully about what we might want to include in the dependencies array what would happen

if we put nothing in the dependencies array and we just left it as an empty array like this in fact I'm actually

going to put in a pause here so you have to so you take a second to think about that if our side effect depends on

nothing which is what it means to have an empty array here then this use effect

would run when the first time when the component first mounts and when the component first mounts recipe is equal

to an empty string and so our scroll into view would not get called this is

exactly what we would hope that it would do we don't want it to try and scroll down to it right at the beginning when the component is first mounted but

because we're telling it that it depends on no external values then it's never going to call this use effect function

again so an empty array is incorrect inside of our dependencies array we want

react to rerun this side effect anytime that recipe changes if the state value

for recipe changes we want it to rerun this effect to determine if it's time to call scroll into view so let's clean up

this challenge text and we'll hit save and give this a shot I'm going to click get a recipe and check it out it

scrolled us into view that's awesome now one thing I'm sure that you noticed is that it did it pretty abruptly it just

kind of jumped down the page immediately and if you are already familiar with the scroll interview method you might be

shouting at your screen wait there's a better way to do this unfortunately there's a small limitation and this

lesson has gotten a little bit long already so we're going to talk about that bug in the next lesson and see a

little bit of a work around for it but in the meantime if this use effect that you wrote here made sense to you then

Kudos that represents a big leap in your understanding of side effects and react and if it didn't that's okay having a

solid understanding of use effect took me quite a while to grasp so it's definitely nothing to be ashamed of but

but it does give you an indication that it might be time to go back in the course and maybe review some of the

lessons that we've had previously once you're ready we are going to add some code that will do a little bit more of a

smooth transition down to this ready for recipe section just to make the user experience a little bit

better in the previous lesson we got our scroll into view to work although we did notice that it's a little bit abrupt the

user experience isn't as great as it could be if instead of immediately jumping down the page if it were to

smoothly scroll down the page to this ready for recipe section and the reason that it's jumping immediately is because

that's just the default behavior for the scroll into view method but as I mentioned if you've used scroll into

view before you might be saying hey there is a way to do this and that's by adding a configuration object where you

can say the behavior should be smooth and if you happen to be following Along

on your local machine then you could put this into your code and it would just work correctly however for those of you

that are following along here in the scrimba interface there is a small problem and that is that well Behavior

smooth just doesn't work let me show you what I mean we'll click get a recipe and when the response came back we can see

it might have scrolled like a pixel or two down the page but it simply didn't scroll smoothly down to the section that

we wanted it to and the reason for it is a little bit interesting it's actually not a bug in scrimba it's a known bug in

at least Chromebase browsers that use an iframe for whatever reason if you have an iframe that you're trying to run

scroll into view with a behavior of smooth on it just doesn't work and our scrimba environment is a little bit

unique because we do have an iframe that displays our mini browser so this Behavior smooth isn't going to work

inside of scriba but in your local environment and pretty much everywhere else unless you're using an iframe it

should work just fine for you I did find a little bit of a workaround I'm not going to really dive deep into the code

although I'm going to paste it here for you to have a chance to play with and just so we can see that it's working so

right here it's simply figuring out exactly where on the page or in the viewable area of the browser that it

should scroll down to and then it's using window. scroll with behavior smooth and for whatever reason this

works just fine inside of a mini browser so let me hit save we'll go ahead and click get a recipe and sure enough we

got a nice smooth scroll down to where we wanted it to go I'm going to leave this line of code commented out just so

if you refer to this you can know that this in pretty much every other environment is going to work just fine for you but I'll leave my real code here

so that we get the behavior that we want great work making it this far through this section I know that side effects

can be a little bit hard to grasp and I know that from going on about 8 years of teaching react at this point hopefully

the way that I presented it was able to demystify what side effects are and how and when to use use effect and react if

it does feel a little bit hazy or cloudy to you still that's completely okay use this as an opportunity to join the

scrimba Discord if you haven't already and start asking questions there see if any of our amazing community members can

help clarify for you when and how you should be using use effect in react and believe it or not this essentially wraps

up the scope of all the topics that I wanted to talk about in this intro to react course however because we're here

on scrimba and because we have such a strong emphasis on getting your hands on the code for the remaining of this

course we are going to be in fullon Project mode we have some awesome things coming up so even though we're done with

these topics the real benefit of this course is going to be with getting your hands on the code and practicing as much

as you can building projects let's do a quick recap of what we've learned in this section and then we are going to

dive head first into some awesome project building

experiences wow can you even believe how far we have come in this course it truly

is mind-blowing especially if you look back at some of the topics we were covering in the first section of the

course your understanding and capabilities in react have truly expanded we have come to the end of the

new instruction in this course that said some of the most important tasks I have yet to give you in the upcoming sections

before we jump straight into those let's do a quick recap of what we have learned in this last section we started off with

some quick lessons about controlled components since we wanted to update our state on every single keystroke of our

input boxes we had to make them into controlled components react 19 has introduced new ways to handle forms

which are quite a bit more intuitive and in line with the native web platform but there are certain circumstances where

controlled components can still be important to know we took a quick dip into Theory as we talked about

functional programming in react and how reacts adopted the Paradigm that it currently has which helped us understand

the whole concept of side effects in the first place then we looked into how we can fetch data with react not

necessarily when a user interacts with our page to request that data but when the app loads for the first time time

and that led us into understanding the actual application or syntax of applying side effects in our react app you're

about to dive into some really exciting projects and so this would be a great time to express your excitement about

finishing section 4 over in the scrimba Discord communities today I did Channel clicking the screenshot will take you

directly there where you can celebrate with the other people who are also completing great tasks today all right I

can hardly wait let's jump into some Project work

the remainder of this course is going to be two back-to-back Capstone projects starting with this first one which is a

game called tenes now let me be completely clear ask anybody in the field and they will very frequently tell

you that project building is the way to learn something new there is no way to

get better at react than to have your hands on the keyboard practicing react as much as possible so although we won't

necessarily be learning much new content in these remaining two sections they do represent the most important parts of

this entire course do not under any circumstances skip these Capstone projects or you will only be shorting

your own education really I don't mean to go on too big of a guilt trip but this is where the real learning

happens if you're not familiar with the game of tenes it's a game that's a little bit more geared towards children

as it deals with rolling a bunch of dice the way that you play and there's a gif here that will kind of and show you how

it works you roll your dice you try to get all 10 dice to have the same number

on top and so in our game which will just move over here to the live version I can click the dice that I want to hold

when I roll it will roll all the dice except for the ones that I held and let's see how lucky I can get here we're

just going with the fours there's another one another one and this is usually where I start to

get pretty unlucky in my roles okay there's one one more and okay we have our last four here what's really fun

about this app and you won't be able to see it here in the recording but if you refresh here and play through the game

you'll see that when you click the last number and all the numbers are the same then a really fun confetti drop starts

from the top of the browser window the button changes to new game and clicking it will of course start a new game feel

free to look through the code ahead of time if you kind of want to get a lay of the land and see all of the fun things

that we're going to be working on and keep in mind that this project is going to be one where I am simply giving you a

challenge and then expecting you to work through the challenge even if it stretches your capabilities and

understanding a bit and then we go through it together to make sure that we're on the same page well what are we waiting for let's jump right into the

first challenge here we are starting from an

almost completely blank canvas the only things that we have are our react and react Dom dependencies installed our

index that HTML is Bare Bones as it usually is in a react app although I did include the inter font from Google fonts

so you don't have to worry about that and our CSS is very sparse just some very basic Styles so that we can start

from a good place hopefully this feels good to you I know it's probably a little daunting it's been a while since

we have set up a react app completely from scratch but that's exactly why we're doing it so the challenge this

time is just to start up a brand new react app some notes on how I'd like it structured I want you you to create a

separate app component that will be in a separate file then here in the index. jsx file I want you to import and render

that app component inside the contents of the app component just render a main element it doesn't have to have anything

inside of it but then what you'll do is just style everything so that it looks like this very beginning State here

where we have this blue background color and the main element which is the white box here with the rounded Corners click

on the screenshot here to go directly to the figma file where you can get all of the specific Styles including the colors

and how much of a rounded corner there is and everything like that all right let's Jump Right In go ahead and spin up

our brand new react app if you had to go back to some of the earlier lessons and see how we scaffold

a new app and react believe me it's completely okay in fact the recommended way of spinning up a new react app is by

using vit and vit will bootstrap all of this beginning stuff for you so truly don't be fretting too much if you don't

remember how to do these beginning lines of code that said we are going to go through this together I need to import

react Dom from react-dom and I'm going to call react

Dom to create a new root element and we have to tell it where that root is going

to exist so not a string we need document. getet element by ID with the

ID of root that's going to reach into our index.html and find the div with the ID of root right here and this will

serve as the root for our entire react app everything will get stuffed right here inside of this div I'm just going

to chain on top of the create root the render method and I'm going to have it

render the app component that I have not yet created but for now let's pretend we

have created it we'll import app from slapp and let's go ahead and create that file

app.jsx I honestly can't remember if I taught this earlier in the course but whenever I'm creating a new file that is

intended to be a react component best practice is to give a capital letter to

the file name so since app.jsx is going to export default function app this is

going to be my app component I want to make sure that the file name starts with a capital letter okay this app component

just needs to return a main element for now so that's what we'll put in and just to make sure I can see it let's go ahead

and type something here we'll cross our finger and hit save and oh we got an

error let's see react on.cc create root is not a function and ah yes I missed

this critical part here this has to come from the client library in reactdom okay good here we go type something here not

too big of a bug that's okay okay let's spend the rest of our time doing some

styling I can see from the design file inigma that I have this kind of dark

blue background color so I'll set background color to the dark blue that I see in the design and then we will

select our main element and give it the background color from the design as well it's kind of like a whitish color it's a

little hard to see but underneath type something here we have that white box just to make it a little more visible

let me give it a height for now we'll give it maybe let's say 400 pixels just

to start out and I'll make my thing a little bit bigger here so we can see that bottom border let's actually start

with 300 I'm going to be changing this in just a second so this shouldn't be too big of a deal and I need that blue

border around everything I think I'll accomplish that with some padding let's go ahead and give this some padding of

20 pixels all right we need a border radius for the rounded Corners so we

will add a border radius of 5 pixels and really quick let's address the issue on

mobile sizes we see first of all this will just expand to as wide as we decide to go with our browser and we hardcoded

this height of 300 pixels on here I think we can do a little bit better than this

by adding some view height that allows the box to take up the entire view height but we'll also do some Max height

stuff so that it doesn't get out of hand let me make this a little bit tall and just try to give this a height of 100

view height and well actually we're able to scroll here I think that has to do with our padding let's go ahead and move

our 100 view height to the body We'll add a height of 100% to to the main

element and then I'm actually going to change the display of the body to flex

we'll use a flex direction of column and then we actually have a layer between

our body element and our main element and that is a little bit tricky to find but remember we are stuffing our entire

react app here inside of the div with the idea of root and so we need to make sure that that div will fill its entire

parent container so I'm going to select the div with the idea of root and tell it that the height should be 1

100% okay we don't get a scroll bar let's see if we make this bigger okay we

have that 20 pixel padding around everything and the box is resizing accordingly I think there's a point at

which it's going to get way too big and so on this main element I'm going to give it a let's put it right here we'll

call it a Max height of I don't know let's say 400 pixels maybe we'll do the

same thing for a Max width and then I think I will make this float in the

middle and actually what I'm controlling here is the div with the idea of root let's

see if this works we'll just Center everything so I'll do justify content Center and align items Center and H this

always kind of gets me I think because we are going multiple levels down between the body and our main element we

just need to pass along some of these Styles so I need to make sure that my width is also

100% And I think I need to do that same thing with my main element and then we will actually move

the max height and width to our div with the idea of root and yeah that looks like it might have done it our main

element is a block level element so it should already be taking up 100% width of its parent container the only reason

we had to add this to the div with the idea of root is because creating a flex box for its parent changes the display

for its child the div with the idea of root for any of you who are much better at CSS than I am there might be a better

way to do this I would be happy to hear about it in the Discord or you can reach out to me on X but for now I'm going to

stick with this I'm also going to just resize this browser so that we don't have to think too much about it let's go

over to app and remove the type something here hit save and it looks

like we are in the same starting point that we're supposed to be in and listen I know that starting from a completely

blank canvas can be a really challenging thing when you're first learning a new technology so don't feel bad if you were

feeling a bit stuck it's also a really long time in this course since we have started a new react app from scratch so

if that was a little bit of a struggle that's completely okay from here on though we are going to be having challenges that should be pretty doable

for you at this point in the course so take it as just another sanity check if the upcoming challenges do represent too

big of a challenge for you it's not something to feel bad about but it is a solid indication that you might need to

go back and rework some of the practices and projects that we've done in the previous sections so without further Ado

let's jump in and start adding some more content to our tenes

game in this part of the challenge we are going to create the dice that actually show up on the page we're just

going to have some hard-coded values for now so other than simply creating a component this is going to be a pretty

CSS heavy challenge because this is a Capstone project I am going to ask that you do the CSS I know in the past I have

said that we should just focus on react but but due to this project being intended to practice all of the skills

that it takes to build new apps and react I do want you to do the CSS for this that said once you're done getting

these dice kind of in the center of the page like this the rest of our CSS will be relatively simple in comparison I've

also tried to give you some hints in the challenge text but we'll get there in just a second your challenge is to create a die component and yes D is the

correct singular of dice unfortunately it will make the rest of this project sound a little bit violent but I promise

I'm a benevolent actor here this is going to be a fun project your die component should take a value prop where

it will take in whatever value it's going to display on the dice as a number and I don't know that I wrote it here

but it should render a button with that value

displayed then for now I want you to render 10 instances of this new die component we'll just render it manually

so it'll be here actually 10 times where you'll pass in a value to each one one where the value is somewhere between 1

and six inclusive then I want you to add The Styling to the main element and the die component so that it looks like it

does on the slide as a hint what I would recommend doing is creating a container around the 10 die components that you

render and using a display of grid to get them evenly spaced in the two rows

with five columns like you see here in the picture speaking of the picture just like in the other ones you can click on

the screenshot to take you directly to the figma design file so you can find things like the code for this for this

drop shadow or the or the font size or or whatever else you might need the design for so I'd recommend making a

container so that you can get your grid evenly spaced with the dice and then turning the main element which is what

we have as this white background into a flex box to make it easier to Center up

vertically and horizontally the container for your dice I wrote both of those hints down here so you have access

to them easily all right I know you've got this let's get started on this challenge I'll start by creating a new

file called d. jsx a totally innocent version of D and then we will export

default our function die we already know it's going to take props because well

the challenge said for it to take props it's going to have a value prop and this should return a button because this is

going to be clickable by our users we want to make sure that we use the button element so that we get all the free

accessibility stuff that comes with the button element and what goes inside will be props Dov Val props Dov Val might

seem like it's a little bit out of the blue and that's because we haven't rendered any die components let's go

ahead and see I can get rid of this we'll import die from die I'm going to

put this on its own line to start and we will just have a

presentational div this is just going to be the container let's give it a class name and call it dice container and

inside I can render 10 instances of my die component and I'll just pass in a

value of one it's also okay if you chose to pass it in as a string I don't think

it's going to matter too much for us at this point and then I will just copy and paste this 10 times I lost count 1 2 3 4

5 6 7 8 9 one more 10 and it's probably not going to be pretty but let's go

ahead and refresh and sure enough we get our 10 Buton butons on the page awesome

at this point I think we will mostly be over in the CSS so let's go over here

and I guess we're already here in the main element so let's go ahead and change this to a display of flex I'll

give it a flex direction of column and we will justify content

Center and align items to the center okay nice that got all of our buttons

just right there in the center of the page let's go ahead and select our dice container change this to a display of

grid and I'll be completely honest here CSS grid is not something that I have a ton of experience in so I usually end up

turning to chat GPT to help me come up with the styles that I end up putting in my grid let's go ahead and change our

grid template so that we have two autosized columns so that's going to be

Auto auto and then we want five one fraction unit rows and so I can use

repeat five times of one fraction unit awesome we can give some spacing to

this with a gap of 20 pixels and now let's work on our buttons a little bit

so these will just be the buttons inside the dice container so I'm just going to select it like this and I'm just going

to put down some of the CSS that I can find in the design so we have a height of 50 pixels a width of 50

pixels there's a pretty cool box shadow in the design so I can just copy be the

value that I found there it's going to have a border radius of 10 pixels and it

looks like we get some interesting default borders from the button so we'll just say border is none the button kind

of has its own color and it's a little too similar to the background so we'll give it a background color of pure white

and oh yeah that makes it stand out a lot better the font is pretty small let's give it a font size of let's try

two rims oh that's really big let's try maybe 1.75 uh that's a little more manageable

although I think we probably could bump up the font weight to bold oh yeah that's looking great buttons

automatically have the text as centered but for whatever reason buttons do not automatically have a cursor of pointer

so I'm going to add that you won't be able to see this in the recording but if you refresh the app and have your mouse

over each of these buttons you'll get that familiar Mickey Mouse glove hand that indicates that it's clickable we're

rendering all ones right now I think think one thing I have found is that buttons don't tend to inherit the font

family from any parent elements although honestly I don't think we've set the font family here I'll do that later and

we are going to be using the inter font and maybe we'll just include a sand serif as a backup and actually I said

I'm going to do that later I'm just going to copy and paste it right now but we can see that if I didn't specifically

put a font family on my buttons then for some reason it doesn't inherit the font family from the parent so we'll leave it

in both places while we're doing that we should probably test all of the numbers so we're not just basing our decisions

on all ones I'll go ahead and include two three four five and six and hit save

and awesome yeah these are looking great and I dare say that we probably are pretty close to the design so I think we

can call this one a win again yes that was a lot of CSS but also again this is fortunately the last of the major CSS

challenges that we're going going to have at least in this project great work on this challenge next what we'll do is

get rid of our 10 hardcoded die components and more programmatically generate a random list of 10 numbers so

that's what's coming up next when we're faced with a slightly

bigger challenge like generate 10 random dice components and display them to the screen sometimes it can be a little bit

overwhelming a great practice to get into is to learn how to take those larger problems and break them down into

smaller pieces so that you can solve each piece at a time in fact this is one of the key things that hiring managers

and people giving Tech interviews are looking for they're looking for your ability to break down a problem into

smaller pieces solve those individual pieces and put them together so that they create a solution to the entire

problem so we are going to break up this challenge of getting 10 random dice elements on the page into two parts

first I just want you to write a fun called all new Dice and actually you know what I'm going to on the flag

decide to call this generate all new dice that returns an array of 10 random numbers between 1 to six inclusive for

now you can just manually call this generate all new dice function and log the results to the console as with any

algorithmic challenge there's more than one way to do this if you need help learning how to create a random number

in JavaScript then a quick Google search or asking chat GPT should be helpful to you however because we're inside of

learning environment here I highly recommend you don't simply copy and paste this challenge text to chat GPT

and have it give you an answer that is only going to short your own learning and take away a perfect opportunity to

think critically and how to solve this problem that said I don't expect you to have memorized how to generate a random

number in JavaScript so just use your best judgment make sure that you're putting your effort into this so that

you are not shorting your own education all right that's enough of that guilt trip go ahead and get started on this

challenge all right let's write a function

actually I'm going to do this inside my app component I'll create a function called generate all new

Dice and even creating this function is something that we could break down into smaller parts let's say first we need to

create a new array and it'll just be empty then we need to Loop 10 times

since we're trying to create 10 numbers and inside that loop we're going to

generate a random number between 1 and six and we will push that number to the

array and outside the loop we will simply return the array okay let's solve it this way and then I think I'll show

another way that you can solve this just to show you that there's more than one way to solve these kinds of problems we'll create a new array let's just call

it new Dice and it'll be empty we need to Loop 10 times so we'll just use a

regular C Style for loop I equal 0 I is less than 10 I ++ we'll say a random

number is equal to and we can use math. random and actually we'll go math. floor

math. random and if you're looking for a number between zero and some other number you can multiply this by six and

then add one or we can simply say let's do math. ceiling instead of rounding down we're going to round up and that

way our lowest number will be a one and we won't have to add one in the end so that's our random number and then we

will simply say new dice dobush the random number and let me

start clearing out some of these comments here and then all we have to do is return the array of new dice let's go

ahead and console log a call to generate all new Dice and see what happens okay

let's open our console and it looks like there's 10 numbers there they're all between 1 and six let's hit save again

just to make sure yep that one's good that one's good okay I think we're pretty safe that our function is working

like we want can clean up the challenge text just for fun I thought I would show another way that you can do this and

it's actually the solution I think I'm just going to leave here so this was a very imperative way to do this another

more functional programming approach would be for us to use some array methods what I can do is simply return a

new array I don't tend to find myself using the new array Constructor very often unless I'm doing exactly what

we're doing here the array Constructor can take how many items that array should have and arrays have a method

called fill where we can just fill every item in the array with something that we want for example some throw away value

like a zero this by itself isn't super helpful but we can now use a map method

to look at every item in the array and put our math. sealing math. random I

probably shouldn't have deleted this time six code so this will map over the new array with 10 items and actually let

me show you this so if I get rid of this map and hit save we see we get our array with 10 zeros in it that's what's

happening in these first two lines of code we map over that array and fill it and for every item in it we simply

return a random number from 1 to six and okay looks like we are getting a working

function once again one way isn't necessarily better than the other I don't know what the difference between

the performance metrics would be in the way that we had it before and the way we have it now I kind of like this functional programming approach so I'm

just going to leave it like this but it truly doesn't matter that much okay well let's move on to the next part of this

challenge where instead of just generating a random array of numbers we turn that into new die components that

way we can get rid of this manual die component repetition that we have here going on

we created a function where we can create an array of 10 random numbers but

next we need to find a way to move those 10 random numbers from just being here in memory and react to the page doing so

requires us to create some state so that's your challenge to create some state that will hold our array of

numbers you can just initialize that state by calling our generate all new dice function that way when the app

loads for the first time it will call this generate all new dice function and just have those 10 random numbers ready

to display then right here in the code I'm actually going to put a comment here that says map over dice here I want you

to map over that array that's being held in state to create an array of die elements this says elements should say

components and then render those in place of our manually written 10 die elements here remember to pass a value

into them so it can correctly display the number from the array and state when you do this you'll probably run into

that warning about having to have a unique key prop for each one of your items you can just ignore that warning

for now we're going to change things up in a little bit to fix that warning okay you should be set with everything you

need go ahead and work on this challenge all right let's go ahead and

import use state from react and just right here at the top of the function

we'll create some new States let's call it Dice and set Dice and then just right

here at the top of the component we will create some new state we'll call it Dice and set dice is equal to use State and

we will initialize it with the array that comes back from our generate all new dice function so we'll just give

that a call then what we could do is just get rid of these 10 manual die components here and we could do our map

right here and say dice. map and kind of do the logic there that's a completely

legitimate way to do this however my personal preference is to create a separate variable inside the body of my

function before the return where I can say something like dice elements and it

just feels like a little bit of a better separation of logic for me I guess I'll just go ahead and render these dice

elements since my cursor was already down there and we can say dice. map and for every number inside this array I can

render a die component where the value is that number so this is where we can

see if it works the dice on the page currently read 1 2 3 4 5 six and then four ones if I hit save it looks like we

yep get a bunch of random numbers let's hit save again and awesome this is working great let's clean up some of our

comments here just to keep things clean and as I mentioned we got this warning that says we need a unique key prop and

we'll be fixing this in the future when we change our array from being an array of just plain numbers into an array of

objects but that isn't quite what we're going to be working on next the next thing we'll do is include a button that

allows the user to roll the dice without having to refresh the whole

application the next challenge we have is to add a roll button so that when the user clicks the button it will generate

10 new dice for us later down the line we'll make it so that clicking individual dice will hold them and

exempt them from the roll button but for now we'll just generate all 10 new dice so the challenge is written out here and

you can add your new button down here there's one little change that I wanted to point out and that is that I made a

mistake on the font that I was supposed to be pulling in I was pulling in the inter font and so I updated this to pull

in the actual font from the design which is Carla and then I updated our CSS to use Carla instead of inter so sorry for

anyone that was looking at the design and wondering what I was talking about with the inter font okay you should be equipped to work on this challenge so

I'll put in a pause now and give you a chance to add a roll button to our Ten's app okay let's start by adding our

button first and it's just going to say roll it ain't going to be pretty but

let's refresh it and okay we have our roll button and now let's hook it up to actually work so I'll go ahead and add

an onclick on it that will call let's see what should we call the function maybe probably roll dice so we will need

to make sure we create that function roll dice and it's going to update the

dice on the Page by updating State and we have this set dice function so that

is all we're going to be doing inside this function of roll dice is calling set set Dice and in our case we

currently don't care what the previous dice used to be because we're just generating 10 new dice so I can just say

generate all new Dice and this might be it other than some styling let's hit

save click roll and yeah look at that all our dice are being regenerated so let's go style our button just to make

it look not quite so ugly I'll probably first want to give it a class name so

let's give it a class name of maybe roll D Dice and we'll select it in our

CSS this will be the button with the class of roll dice and it looks like in

the design we are sitting at about 50 pixels high and about 100 pixels

wide there's no border but there is a border

radius of about six pixels I'll just grab the background color from the

design which is this kind of purple color there the color of the text though needs to be white the font size looks

like it needs to be a little bit bigger maybe let's try something around 1.2

rims yeah it looks pretty decent and just like before we did not bring in the

font family because buttons don't inherit the font family we can see if I

add the font family of Carla it does make a difference because we have both

of those buttons I think I might just have a button select leor that uses that font family and then I can remove it in

these two places and actually while I'm at it I'm going to move this cursor pointer up to my generic button selector

and that way again you won't be able to see it in the recording but if you refresh it you'll see we now have a

cursor of pointer on all of our buttons here and then the only other thing for now is to give it some spacing we

actually have a couple of other elements we're going to be adding to this page like the title and a little

instructional paragraph so I think what I might do is instead of manually adding the I think the design shows about 25

pixels on the bottom I'm going to come up to my main container and instead of

justifying the content to the center I'm going to say space between oh that is too much um you know

there's one that we don't use quite as often called space evenly and yeah that one looks pretty good we might be

changing this later as we add more elements to the page but that's okay just make sure our button is still working and and awesome W this is an

awesome tenes roll look at that we have five threes all at once that's great we are not able to hold the dice quite yet

but as it turns out that is the next challenge we're going to be doing we need to make it so that when the user clicks the dice it will hold that Dice

and exempt it from clicking the roll button so that only the unheld dice will get changed before we move directly into

that though I wanted to make sure that you are feeling comfortable with these exercises that we're doing this

challenge should have been a relatively straightforward challenge for for you assuming you were able to get through all of the previous challenges and the

previous sections as I've said before if you found that this was a pretty difficult challenge for you then I would

recommend taking a pause going back redoing some of the previous challenges maybe you took a little break since you

took those sections of this course that's completely okay but it is probably time to revisit those so that you can refresh yourself before just

trying to force your way through the rest of this Capstone project if on the other hand you felt pretty comfortable

with that challenge awesome work and let's move on to learning how we can hold the

dice the next challenge we're going to have is to make it so that the user can click on the dice to hold it so that

when they click the roll button it won't change the dice that are being held to do this we need to have more information

about each individual die than just its current value up until now we've just

been saving an array of bare numbers but our challenge for this lesson is to update that array of numbers in state so

that it becomes an array of objects instead that way each object can have a value property which will contain the

same number that we were using before but also additional information about whether that die is being held or not

and that's just going to be represented with a Boolean when you make the change from having dice be an array of numbers

to an array of objects it will also break another part of our code so make

sure that while you're doing this you update things so that we're back to a working State all right the time is yours to work on this challenge

let's find the place in the code where we were originally adding just a bare number and change it to add an object

instead and that is this line right here when we're mapping over our array of 10

numbers instead of just putting a bare number in there we can instead put an object in its place whose value is going

to be what we had here before and oh I think I have my braces off a little bit right there okay whose value but also

have an is held property which we will default to false oh and because we're

using an arrow function I need to surround my object with a set of parentheses just so that it doesn't

think I'm beginning the body of the function like that let me go ahead and put these properties on their own lines

just to clear up the spacing a little bit and now let's try to Think Through the other places in our code that was

expecting our state to have an array of numbers instead of an array of objects

and I can see one right here we were mapping over our array of dice and I chose to call this numb because it was

just a bare number but now I'll go ahead and call this maybe a die object and so

the value should be diob doval now I'm not seeing anywhere else that we would

have any problems so let's hit save let's click roll and okay we're back to

a working State perfect in an upcoming challenge we of course are going to make it so the user can click on these

buttons and hold them in place which effectively would mean that we find that specific die in the array and flip its

is held value but before we move on I want to address the each child in the

list should have a unique key prop warning that we've been getting remember when we map over an array and we create

an array of jsx elements react needs a prop that's dedicated to jsx elements

called key so that it can keep track of items every time something gets rendered

and it's crucial that that key be unique to this specific die now of course we

couldn't use diob doval as the key because the whole purpose of this game is to get all of them to have the same

value very often you'll find yourself mapping over an array of data that gets pulled down from an API and more often

than not that data includes some kind of ID that was generated by the database that's holding that data and if you have

something like that then perfect that's definitely what you should use as your key because it's pretty much guaranteed

to be unique to that object in our case though we're generating our data right here and so we need a way that we can

add an ID property to our dice so that first of all we can add it as the key

prop here so that react knows how to distinguish this individual die component from other die components in

this array but it's also going to end up being pretty helpful for us when it comes time to hold the dice so one thing

that I can do is use a third party package there's a really simple one that's called Nano ID so I'm just adding

that to my list of dependencies I can import Nano ID from the package Nano ID

and this will generate a unique ID number for me by simply calling Nano ID like this I'll hit save and we'll see

that oh of course we are still using die object. value as our key we need die object. ID as our key and okay awesome

now our warning goes away okay so our data is primed so that each individual die component has way to know if it's

held or not but of course we don't yet have a way for the user to change that so that's what we'll be doing in the

next

challenge very soon we're going to add the capability for the user to click the die so that it will be held but unless

we add some special styling for dice that are being held it's going to be a little bit difficult to test this out so

the first thing that we'll do is style our held's dice or in other words the dice who have an is held property to

true so that when they are being held they will have this kind of light green background color the way that we'll test

this in this lesson is I'm just going to change the is held property to true for all the dice so when you have

successfully completed this challenge all of them should turn that light green background color so that's what your

challenge is I need you to add conditional styling to the die component over in die. jsx so that if it's held or

in other words if is held is equal to True its background color changes to this light green color which I've given

you the hex value for right here there's different ways that you can handle this conditional styling I'm going to leave

it up to you to decide which one you want and remember currently the die component doesn't yet know if it's being

held or not and I'm going to leave it a little bit vague like that so you'll have a chance to figure out what that means and how to fix it go ahead and get

started on this challenge the first thing I need to do is to make sure that I am teaching the

die component how to know if it's held or not currently we are only passing a

value down to our die component and so I'm going to put this on its own line to buy myself a little

bit of room here and pass in the is held prop or I should say a prop that I'm

choosing to called is held because it happens to be the name of the property in the object so the value will be die

object do is held in that way each of the die components will know through

props if it's held or not now at this point what I could do is either conditionally render a class name as in

the class name could look at props that is held and either apply the green background color or Not by adding or

removing this class name but I think what I'm going to do is just use an inline style so in my button I'll say

style equals and then I could either pass my Styles directly here or something I tend to like to do is to add

a separate object up here and pass in the Styles directly

remember these styles are accessing the native Dom properties and so when I want to change the background color

especially because I'm here in an object I can't as easily use background Dash color without surrounding it with a set

of quotation marks instead I need to use the capital c color or the camel cased

version of this property and I can use a Turner that says let's look at prop. is

held and if it's true then I want the back color to be that green color that

we see right here so let me copy that and we'll paste it in there we'll just set the color to white which is what it

is in the CSS all right I think we might be all set up let's hit save and sure enough look at that we get all green

colors and that's because we had changed this from false to true if I change it to false then we can see that it all

turns white again okay now we are ready to tackle the challenge of holding each die whenever it gets

clicked we talked previously in our section about State about a concept called derived State and generally

speaking we found that it's better to have a single source of Truth where the state is held on the parent well it

turns out arten game is a perfect example of this it might be tempting when you're first starting to write

react to say well I want each dice to be able to know if it is currently being held or not and so you might go to your

die component and add new state to it that says bring in the incoming prop of

is held and then set internal state that can be used to display whether the die

is being held or not and then you would create a function inside of the D component that when the die component is

clicked it would flip that internal state for that one single die however as it turns out if we're looking forward to

the mechanics of our game we can only know if the user has won the game if all of the dice are being held and if all

the dice have the same value but if each die component were in charge of flipping

its own state it would become out of sync with the state that's being held in the parent in other words when we first

load our component this first die that has the value of is held of true gets passed down to the die component but if

the user clicks it and flips it to false that doesn't change the parent state where it says is held as true and so

hopefully you can see that that would become a problem so although it does tend to be a little bit more code a more

correct approach that does not rely on using derived state would be to get rid

of the state from the die components keep the state that is currently in our app and create a parent hold function

that we pass down to each one of our die components this hold function would take an ID so that when one of the dice is

clicked it would call the hold function pass to it the ID of itself and the

parent state would be able to Loop over the array of dice objects find the one

with the ID that was called in the hold function and simply flip the is held

property of that one die that was a lot of talking I hope this diagram helped

visualize what I'm talking about and so the first part of this new feature is what we are going to be working on now I

want you to create a function that's just called hold and it will take an ID as a parameter for now all the function

has to do is console log the ID then I want you to figure out how you're going to pass this hold function down to each

instance of the die component so that when each one is clicked it will log its own unique ID property and I did mention

here that there's more than one way to make this work so just feel free to choose whichever one you want in the end

because each one has a unique ID the way that you will tell if it worked is if by clicking this first button it will

display one ID and then clicking another button will display a different ID we're starting to creep up on a little bit

more difficult challenges here but I know that you've got it in you to get this done so go ahead and get started on

this challenge okay let's get started I think I'll put my function just down here

below roll dice and we'll say this is hold it's going to take an ID as a

parameter and simply console log that ID well now what we need to do is figure

out how we can pass this hold function down to our components let me clean this up to to buy some room and clearly in

order for each die component to have access to this function we need to pass it down through props I'm going to put

each of these properties on their own lines just to again buy some room and

we'll go ahead and pass the hold function just like this down to our die

components however we hit kind of a blocker at this point remember when we go over to our die we're receiving props

do hold now and I can simply add to my button let's see right here maybe let me

put this on its own line too right here we can say onclick it's going to call

props do hold here's where the problem begins and I wouldn't be surprised if some of you doing this challenge ran

into this issue if I go ahead and click for we'll see that I don't get an ID I get something that says synthetic base

event if I click another one they're just all saying synthetic base event I'm going to put another pause in here and

see if you can figure out what's going on here remember these onclick events the

function that you pass to it we don't get to decide what parameter it receives it will always receive an event object

so we need to think back how can we provide our own parameter if we want to call a function well instead of just

passing props do hold as the function that gets called when onclick happens we

can instead kind of wrap that in a function that says this is the function you should run when the onclick for this

button happens and this function will will call props do hold and at this point I can put in whatever parameter I

want well we run to another problem I don't have access to the ID here in my

component so simply enough what I could do is just come down here once again and

also pass my ID property so this would be die object. ID once again this ID is

coming in clutch for us and over in the die component I'm now receiving props

that ID so I can pass that in right here props that ID let's try this again I hit the four and there's a crazy looking ID

that was generated by Nano ID we'll Click Five and sure enough a completely unique different ID just for Giggles I

had mentioned that there's more than one way to do this and so I figured I'd give you a chance to see what that might look like there might be more than just these

two ways obviously but here what I can do when I'm passing down my hold function instead of just passing down

the hold function as a whole I can do essentially what I did in my onclick and say I'm going to pass down this unique

function and this will end up being a closure that captures the ID value that I passed to this parameter right here

and so in that case I don't even need to pass my ID down and when I'm receiving it I don't need to do this anymore

because props do hold is now a closed function that already contains the ID of

this specific die component I think the way that we had it before might be a little bit more intuitive but because

this is working and just for the sake of seeing a different way to do something I'm going to leave it like this okay

we're making good progress next we need to make it so that we're not just console logging the ID when the user

clicks the button but instead we are updating the is held property on the correct die in the

array let's make it so that users can click the die and instead of it obviously console logging the ID it will

change its is held property to true or if it's already true it'll change it back to false you'll know that you've

succeeded in this challenge if clicking a die will change it to Green since we have already set that up over in the die

component however keep in mind that we haven't yet implemented the feature where clicking roll will only change the

dice that have not been held and as a hint although this is more like a reminder because I've said it before

there's more than one way to accomplish this so don't spin your wheels too much trying to make sure you get it exactly

the same way that I'm about to do it if clicking the dice changes it from white to green or green to White then that's

how you'll know you've succeeded this will be one of the more difficult challenges that we have throughout this whole section but fortunately for you

we've actually done something nearly identical to this in the past when we learned about State using this little

sound pads exercise you can click the screenshot here to go back to that exercise if you need a refresher on what

we ended up doing so that we could flip these on and off so you should be prepped now to have everything you need

to work on this challenge all right I'm going to buy some room by getting rid of the challenge text since

I know what we need to do instead of console logging the ID we need to update our state because we're holding our

state in one unified place here in the parent component to all the die components we can simply call set Dice

and our task is going to be a little bit more complex because we have a whole array of dice that we're looking at and

we only need to change the is held property of one of those dice as such I do need to know what my old dice were so

I'm going to use a callback function and I think for the sake of clarity to start this out I'm going to open the body of

this function and use an actual return keyword here remember dice is an array

of objects and so what I need to return when I'm calling set dice is another array of objects and I can get a new

array by calling old dice. map and I will look at each one of the dice or

each die in the array of dice and the most important thing for me at this point is to check if this die has the

same ID as the one that was clicked or the same ID that we're receiving as a parameter to our hold function so I

could do an if statement and check if die. ID is equal to ID or I can just use

a Turner which will allow me to be a little more concise I'm going to return

and then first check if die. ID equals the ID and if it does then what I want want

to return is a new object and it will contain all of the properties from the original die but the ish held property

is going to be the opposite of die do is held if the IDS don't match that will be

my else section in my Turner operation here I can simply return the old version

of the die I don't need to change it whatsoever okay first let's check to see if we are working I'll hit save and boy

that is a terrible tenes roll I don't know if I've seen one that bad in a long time I guess we have three sixes oh no

it's not and oh look at that we have four sixes oh awesome clicking them makes them green awesome as I said if we

didn't want to hold them I could click them again and they would flip to the opposite of is held so we get to go back

and fourth and as I mentioned clicking roll is just going to refresh them completely we don't save any of the dice

which is fine that's what we're going to be working on next well let me come back to my code and do a quick refactor I

mentioned using an explicit return like this but because I'm using Arrow functions I can rely on implicit returns

so let me pull this up to its own line and boy this is going to get a little confusing okay I've gotten rid of that

explicit return here I am mapping and using another arrow function so I think

I can do another implicit return I might have to open some parentheses let's get rid of our curly

braces and let's see and let's see actually I don't think I need that one

and I don't like the spacing of this let's see okay that makes and okay yeah

that works I don't know that it's really that much easier to read but I guess it saves us a couple lines of code whatever

let's just hit save to make sure this is still working and let's see we have 3 twos perfect or maybe we change our mind

and we select the fours great work okay the next big feature we have is to make it so that when we click the roll button

we don't lose our held dice but only roll the dice that are not being held so that's what's coming up next

other than checking if the user has won the game I think this is the last major feature that we have to add to our tenes

game your challenge this time is to update our roll dice function so that instead of generating all new dice every

time the button is clicked it will look through the existing dice in the array

and only roll the ones that are not being held as a hint this is going to look really similar to to the hold

function I guess we didn't call it hold dice we called it hold and it's helpful to remember that what we mean when we

say you're rolling a die really you're just going to be updating the value property of that D object I'm not going

to get any more detailed than that I want you to figure out how to finish this challenge so the time is yours go

ahead and refactor our roll dice function we know that we're going to be

updating our state so we do still need set dice here but in instead of generating all new dice we are going to

look at the old dice array and we'll map over it checking each die along the way

if it is being held so we'll use this Arrow function and we will map over old

Dice and for each die in the array I'm going to check if die do is held is true

I'll just use a Turner here and if the is held property of this particular die is true then I don't want to change

anything I just want to return the same die object otherwise I'm going to return

a new object that has all the same properties of the original die this is important because it allows us to keep

our ID that we generated when we first created The Dice objects but I want to

change the value property to be a new random number which I can just get by calling this code up here let's go ahead

and I think we have it right let's get rid of this challenge text hit save and oh we got a good amount of twos here all

right moment of truth we'll hit roll and look at that all the dice except for the ones being held rolled so I can play

through the rest of this game holding the dice as I go and we're getting pretty lucky so far

there we go all right well this brings us to the beginning of the last feature

and that is that we need to be able to indicate to the user that they have completed the game as it stands right

now if I click this two they're all green and I know know personally that that means I've achieved tenes but I can

still hit roll there's no way for me to reset this game other than to refresh the page and maybe most importantly

there is a critical lack of confetti dropping down from the page all of those are things we are going to be working

through as challenges but before I do that speaking of indicating some information to the

user I am just going to paste in some of the elements you can see from the design

we have a header and a little paragraph that instructs the user how to play the game so those are not really worthy of a

challenge at this point I'm just going to paste in some of that markup as well as provide a few Styles here see I'll

just put it right here below the main and we'll just paste those in right there let's hit save and well I think I

want a little bit more space above my button or below the dice container so let's see where are we right here on our

dice container let's just put a margin bottom maybe 40 pixels okay yeah that's looking

pretty good great work on getting this challenge done and all of the challenges

in this feature we're now able to hold the dice and continue rolling the ones that are not held which is essentially

the Crux of playing tenes as always feel free to play around with this code as much as you want make sure that you

understand it before just plowing ahead once you're ready we will move on and start implementing some of the logic for

what happens when the game is over

okay guys I have a confession to make and that is that this is not the first time I have taught this course using

this project the tenes project in the previous version of this react course I also went through pretty much all of

these same things with the tenes game however as I was reviewing some of the things that I taught back then I

realized that I made a mistake and so I wanted to make sure that I got it right this time and that I gave you a chance

to think critically because what we're about to cover is a mistake that not only I made in the past but one that I

see very often in the react Community especially with beginners and react and

so we're going to take a little break from writing code and we're going to put on our critical thinking hats our goal

is to indicate to the user that the game is over if first of all all the dice are being held and second of all if all the

dice have the same value if those two conditions are true then we can consider the game as being over and one so let's

start planning ahead and think how we might accomplish this some questions that we can consider would be first of

all do we need to save a game one value in state somewhere if you think the answer is yes then why and if you think

the answer is no then why not and secondly do we need to create a side effect with react. use effect to

synchronize this game one value whether it's being held in state or not with the current state of the dice these two

questions are meant to guide you in your planning session here as we decide how we're going to implement this feature so

I'm going to put it on pause here just like when we've taken quizzes in the past I want you to type your answer into

the comments here both for number one and number two and then I want you to have a conclusion section where you

write out a simple plan of how you're going to implement this feature so I'll go ahead and put in a pause here don't

skip this step this is a crucial thing for you to get practice with as you're learning take some time now to answer

these questions what I taught in the previous iteration of this course and this part

of the challenge was I created new state and I said we're going to have a

variable a state variable called tenes and we'll call set tenes the reason I chose tenes is

because in the real game you're supposed to shout tenes when you have gotten all of it it's really a race against other

people and so that was equal to use State and and we set the initial value

as false and then I also created a side effect that watched for Anytime the dice

State changed and then checked for conditions to see if tenes was true in

other words if all the dice are held and all the dice have the same value and as I'm sure you have guessed by now I

realized now that this was not the correct way to do this so if we're looking at the answers to these do we

need to save a game one value in state well as it turns out the answer is no

remember how react will reender our component every time the state changes

part of rendering the component doesn't just mean it updates what's on the page but it means that it reruns all of the

code inside of our function so instead of setting a new state variable all I

need to do is derive the value of whether the game is one or not based on

the current value of dice in fact this set dice function is the only state

Setter in our code that's going to cause or rerender anyway instead of creating new state I can simply use the state

that already exists with dice and every time the component renders I can check

again to see if the game one conditions have been met I'm not going to write

this code because we are going to do that in the next lesson but I will write a comment that simply says check if the

game is one and I can do this on the top level of my app component this code will

run after every single render in other words every time the dice gets set to

something different and I can use this variable that I create if the game is one to add whatever features I want to

add change the text of the button or make the confetti fall down if instead I were to save the game one value in state

then I would need to include a side effect so that I could synchronize the dice state with the game one state and

so question number two definitely would depend on what your answer to question number one was if you answered yes then

you would likely need a side effect so that you could synchronize those two pieces of state but since we answered no

we don't need a side effect so we can again say no we don't need a side effect I think when we write the code for these

features we'll get to see exactly why we won't need these things and we can keep it as simple as possible so our

conclusion is that we can derive the G G one status based on the condition or

we'll say conditions of the current dice State because of this we can calculate

whether the game has been won on every single render just in regular code here at the top level of my component and so

maybe to be more specific I'll just say on every render as I mentioned this is a really

common Pitfall in react in fact so much so that there's a dedicated article in the react docs that's dedicated to

teaching you that you might not need an effect so many developers in the early days of the use effect API were misusing

it that the team had to put together a whole tutorial to teach people to stop using side effects when it isn't

necessary specifically it says that they are meant to be an escape hatch from the react Paradigm they let you step outside

of react and synchronize your components with some external system in our case

we're not trying to synchronize with an external system we're just trying to derive a value based on our current

state I hope that makes sense I know that's a bit theoretical but again I think you'll see just how easy it is to

add this new feature where we can determine if the game has been won without having to deal with State

without having to deal with side effects so without further Ado let's jump in and get our hands back on the keyboard so we

can start typing some more code we'll do this in a series of

smaller challenges the first thing I want you to do is simply to log game one to the console only if the two winning

conditions are met which I've outlined here and we've talked about before for now you don't even need to save a

variable you can simply put a conditional right here at the top level of our component go ahead and get

started on this challenge the tricky one with this challenge has more to do with getting

these winning conditions right than it does pretty much anything else we can simply have an if condition that if it

evaluates the true will console log the game is one and so the trick is simply

making sure that we get these conditions correct and there's a lot of ways to determine if all the dice are being held

and if all the dice have the same value I'm going to make use of an array method called every it lets you pass in a

callback function and if that callback function returns true for every item in

the array then the entire expression evaluates to true so for example I can say if dice.

and we're going to look at each die in the array and say if die do is held then

return true or in this case it's simply going to return the value of die. is held which means if every die is

currently being held then this entire expression will just evaluate to the Boolean true whereas the map array

method returns a new array every simply returns a bullan okay so there is one

expression we also want to check if every dice has the same value well if

every dice has the same value I could just arbitrarily choose one of the dice get its value and check if every item in

that array has the same value as the first ey I'm going to put this on its

own lines I think just to maybe space this out a little more easily and we'll

say if dice. every not dive. every dice. every we'll look at each die and we

could say if the current di value is equal to the very first dice in the

array so dice at the index of zero. value then that means that every dice

has the same value so let's get rid of our challenge text let's hit save we

should not get game one because our winning conditions are not true yet and I guess we need to play through this

game threes look like a good start and whoa look at that four more threes in one roll that's

crazy and okay here we go so when when I click this we should get game one in the

console perfect okay now that we've been able to figure out the logic for our winning condition let's go ahead and do

a second part to this

challenge okay for challenge part number two I want you to create a new game one variable and I'll leave it up to you to

determine what its value should be it should be pretty straightforward since we just wrote the logic for it and also

if game one is true I want you to change the button text so that it says new game instead of roll this by itself won't

make the new Game feature actually work that's something we're going to do in a couple challenges from now but it'll be

one step closer all right I'll hand it over to you well we don't need to check the

conditional or run any code at this point but we do want the values that are being held inside of our conditional so

I'm just going to cut those out and delete here we'll create a game one

variable and that's just going to equal whatever the Boolean value is from these expressions and remember what we're

doing here is deriving the game one value based on the current state of the dice array which means every time the

dice array changes or in other words any action that we take that might call set dice our component will render the

entire app function will run again and we will get an updated version of game

one of course it's just a Boolean so it'll be false most of the time you're playing the game until the very last

click but I think you get the idea okay for number two let's change the text of the button based on this game one

variable we can get rid of the challenge text and we will let's see right here

I'm just going to put roll on its own line so that we can instead of hard coding roll use a Turner we'll say if

game one then we want it to say new game but otherwise it'll say roll okay I'll

hit save and I'm going to play through this game I'll skip ahead so you don't have to watch it okay moment of truth

I'm going to hold the two and sure enough that changed to new game I don't actually love that it is wrapping like

that let me come to the button in CSS and I think it's this one we'll change

the width to 150 yeah that looks a little better actually you know what I think instead of hard coding this as 150

I think that's going to look a little bit wide when the text just says roll I'm actually going to allow this to

adjust the width based on the text that's in there so I can say white space

should be no wrap I don't want the text to wrap then I can set the width I believe to Auto and at that point I

probably want to make sure I give some padding to this and I just reference the design it looks like we can say we're

about 6 pixels on the top and bottom and 21 pixels on the left and right okay so

if I hit save guess I have to go to one of these to hit save the button resized and it still has some decent padding I

think that's a little better all right I think the next challenge is going to be by far the funnest challenge that we have in this entire project and that is

to make it so that when the game gets won we get the awesome confetti drop in our app so let's jump into that one

next this one is definitely the most fun challenge in this entire project and that is to make the confetti drop when

the game is won there's a really fun package called react confetti and it couldn't be simpler to use I've already

installed it in our project you can click on the screenshot here to go to its GitHub repository and read through

the use section it will recommend including a width and height prop but for now we can just ignore that it will

default to the window size they recommend doing that because if you resize the window then your confetti

will be the wrong size I guess that could be a challenge that you do based on the work we did with side effects in

section 4 but for now again just ignore the height and width props I've already installed the project

in our dependencies and there is one major caveat at the time of recording this because react 19 has not officially

been launched and we've been using the release candidate version for this course react confetti doesn't quite yet

work on the release candidate of react 19 so I did have to downgrade to react version 1831 which is the most recent

stable version of react react 19 has been on the very precipice of being released for a number of months now so

by the time you're watching this I would wouldn't be surprised if react confetti works just fine on the official release

of react 19 but for now we're going to deal with it this way oh and I almost forgot I have a fun gift that shows you

exactly what will happen when you have won the game the confetti will drop our text will change to new game like we did

in the last section that button won't quite work yet but like I said this is the most fun challenge for sure okay

your turn get started on this challenge okay we can see from the documentation that what we need to do is import the

conf confetti component and it's just a default export from the package so we'll import it from react confetti we have

our game one variable here which is what we will use to conditionally render the confetti component so we'll say game one

and then render the confetti component like I said it pretty much couldn't be

simpler let's get rid of this challenge text hit save and I'll fast forward through this so that it's a winning game

okay one downside of the way that the recordings work here on scrimba is that any elements that are displayed on the

canvas of our web browser don't actually get recorded into the scrim and the confetti is using the canvas to create

all of the colorful confetti shapes so I'm going to click three here and sure enough I can see the confetti dropping

and I'm sure that you did this Challenge and succeeded in it and were able to see the confetti drop on your end as well at

this point in order to start a new game the user would have to refresh our page so let's go ahead and implement the

logic we need need so that the new game button works and I believe that we'll wrap up the last feature that we need to

add to our tenes game you know what I changed my mind

there is one more topic I want to touch on that's a little more boring than actually implementing the new game

functionality so we're going to get this one over with first so that we can end on a high note of adding the last

feature to our game what we're going to be talking about has to do with this line of code here on line seven where

we're initializing our State we're calling Ed State and then we're giving it an initial value but the way that

we're giving it an initial value is by calling a function and at first glance this might seem like it's fine this is

the initialization of the state right so it's only going to run this line of code one time and then handle any changes to

that state behind the scenes well let's remember that every time we make any kind of state change in our app like

when we click a button to hold it or click the roll button we are changing state in our component which means that

react is going to rerun all of the code inside of this function and part of running this whole function includes

calling this generate all new dice function because react is handling the state behind the scenes it's not going

to update the State per se just because we called this but it really is calling this function on every state change and

I can demonstrate that by adding a console log to generate all new dice let's say generate all new dice was

called okay let me hit save that that'll refresh the app and we can see that we get it one time which is what we would

expect but when we wow look at that we have six sixes every single time I hold one of these dice it's also calling

generate allnew dice again now the code inside the generate all new dice function is not that intensive it's

doing a few things it's mapping over an array with 10 items which JavaScript can do extremely fast for each one of those

items it is calling this Nano ID function which I imagine is not very expensive even if you're doing it 10

times but then in the end react is just discarding everything that is returned from this array after the first time it

runs it because it knows it doesn't want to reset the state so how can we address

this issue well fortunately react made it really easy when we're initializing our state we can provide a regular value

for the initial State like we're doing here it might not look like a regular value but since we're calling this

function and that's returning the array that's pretty much equivalent to providing just a bare value alter

atively we can provide a function for react to run and then that function

needs to return the value that we want to use as the initial state by doing this react will make sure that it does

not rerun this function on the subsequent rerenders of our component so I still have my console log here inside

of the generate all new dice function but if I hit save we get it once for the first time but then as I'm holding Dice

and clicking roll and changing State otherwise our component is rendering but it is is not rerunning our generate

allnew dice function again again in this case the performance benefit is a little bit underwhelming but if you were doing

a more expensive operation in order to initialize your state this would be a perfect way to ensure that you only have

to do that one time let's clean up this console log and we can close our console and now as promised we'll move on and

make it so that the new game button actually starts the game over from scratch so the user can play again

this is another example of a challenge that I'm going to be pretty vague about and just give you more of a scrum style

user story and leave it up to you the developer to figure out what needs to happen in the code to accomplish the

task the task at hand is to allow the user to play a new game when the new game button is clicked and I guess it's

probably redundant to say and they've already won the new game button currently will only show up if they've won the game and actually that's all I'm

going to say about the challenge so I'll hand it over to you to work on adding this

feature well so far all I've done with this button is conditionally render the text depending on the value of game one

but of course this onclick is always going to call roll dice whether the text says new game or it says roll one

approach I could take is to conditionally render a button that says roll that calls roll dice if game one is

false and otherwise render a completely different button with a completely different function that it calls if the

game is one however to me that feels like a bit of extra work that I don't really need to do instead what I could

do is simply update the logic for my R dice function so that it checks if game is one and if it is then it will do one

thing and if it isn't yet one then it will do another thing so let's come up to our R dice function and the code that

we have here is code that I really only want it to run if the game is not one so

if not game one then I'll move this code inside of this conditional but now I can

add an else which means that the game is one where I can just set the dice to be

all new Dice and fortunately I created a function called generate all new dice

when I generate all new dice it will reset all of them to an is held of false

which means that our value for game one should now be false and the confetti will stop playing all the green will go

away and the numbers should be shuffled again let's go ahead and hit save I'll spare you watching me run through this

game by skipping ahead okay I'll click the last six I'm seeing the confetti on

my end and now the moment of truth if I click new game Awesome everything starts over from the beginning State I can see

an argument to be made that we are kind of overloading this function and it might be better to conditionally render

a second button but I think for now I am probably just going to leave things the way that they are here at this point all

of the features of my app have been added however there is one crucial thing that I've neglected to do because we

have a highly interactive app here especially when you're dealing with games there is a lot to consider when it

comes to making sure that your app is accessible for those using assistive Technologies in an effort to keep us

laser focused on practicing react specific things we haven't yet touched on those but I would definitely be doing

a disservice if we didn't include them in our app so in the next lesson I'll walk through a few of the accessibility

changes that we need to make to our app so that it is usable by

everyone because we chose to use a button element for our die components we get a lot of accessibility benefits for

free just from HTML in general for accessibility purposes it's important

for clickable items to usually either be a button or an anchor like a link

leading to another page otherwise you have to start considering using tab index to make sure that it's

accessible via the keyboard and setting the RO as a button and all sorts of things so using a button here was

already an accessibility win that said because the information in the button simply has a number in it we can improve

how assistive Technologies announce the buttons by adding an ARA label property

and because we have some data here I can get pretty descriptive with what my ARA label should include so I can say

something like this is a die with a value of and I can stick in some

variables here we'll say props do Val and I think it especially would be helpful to know whether it is being held

or not and so I could add in a Turner here that says let's check the is held property oh and it looks like I used the

wrong curly brace here and if it's being held then we can say it's actually going

to read out the word held but otherwise it's going to read out not held so this

is already a huge Improvement it's probably the lowest hanging fruit for improving the accessibility in enses app

something that is very similar and related but also can be really helpful to include is a property called AR

oppressed this is a way to indicate to assist of Technologies whether or not this button which is kind of acting like

a checkbox or a toggle is currently being selected or not we're kind of covering that by including the term held

or not here but this can also just be another easy thing to add and we can

simply give it the Boolean value of is held the next thing we can do is make it a bit more obvious when the game has

been won right now we're really only indicating that the game has been won by dropping a bunch of confetti but for

those who might not be able to see that confetti or notice that the button text has changed from Roll to new game we can

add what's called an AR alive region this is a section of our markup that when changed a screen reader will make

sure to announce whatever content we put there in and doing so doesn't even have to mess with the visual representation

of our app normally let's come down to where we're conditionally rendering the

confetti and I'm going to include a div here and I can include the ARA live and

set it equal to polite anything that I put inside of this div will get read out

by a screen reader whenever the content there changes so I can conditionally render based on the value of game one

maybe a paragraph that says something like congratulations you won press new game

to start again of course by default this will add a new paragraph to our page

which we may not want to do and so we can actually include some CSS with a

class name often times it's called something like Sr only for screen reader only

and in our CSS it will make it so that paragraph is never visible on the screen but it will get read by assist of

Technologies so I'm just pasting in here an Sr only set of rules that I have copied from another project it basically

goes above and beyond to ensure that anything marked with Sr only will never actually get displayed on the page now

at this point there actually is one more accessibility Improvement that I'd like to add but it touches on something that

you have learned in this course and so I'm going to turn it into into a challenge and give you a chance to look

back at something we learned in section 4 and see if you can recall that information or maybe go back and restudy

it so that you can complete the next challenge and we'll be doing all of this in the next

scrim I'll actually be truly impressed if you're able to do this challenge without referring to past materials so

if you're feeling a bit lost as we talk about what this challenge requires don't feel bad whatsoever ever because it was

something that we kind of just got a quick sneak peek on in section 4 but I do want you to give this your best shot

I want you to go back to section 4 if you need to to review the lessons that we learned there and then bring that

knowledge back to this challenge to try and apply it in cognitive science recalling information like that and then

applying it is one of the best things you can do to retain that information for the future a quick change that I've

made to our code just temporarily is when we're creating new dice I just gave it a value of five that way we don't

have to keep playing the game whenever we want to test the end scenario I probably should have done that a bit

sooner but if we take a close look I can hold all of the dice and when I hold the

last one we can see that the button focus is actually here way on the first button in our list for a keyboard user

that means in order to access the new game button way down here I have to hit tab about 10 times just to get down to

that button before I can hit spacebar or enter to tr trigger the new game button definitely not ideal so our challenge is

to make it so that when the game is over the new game button automatically receives keyboard Focus so that keyboard

users can easily trigger it without having to tab through all the dice first the code we need to add to make this

work is not that extensive but I did want to give you two major hints to help guide us along the way the first one is

that focusing a Dom element with the focus method which exists on Dom nodes

requires accessing a native Dom node I want you to think back to section 4 what

tool have we learned about that allows us to do that then in order to automatically call the focus method on a

Dom element when the game is one requires us to synchronize this local game one value or variable with an

external system which is the Dom so think again what tool have we learned about in the past that allows us to

synchronize react with an external system the answer to these two questions is hopefully going to guide you in the

right direction to solving this challenge again if this is feeling pretty over your head that's okay you

can click this Mario box to get a power up which will take you back to the lesson where we learned about the answer

to number one and then the next lesson in that same course will lead you to the answer to number two and hopefully give

you the tools you need to come back here to solve this challenge so without further Ado I will hand it over to you

to work on this challenge in react the preferred way to

access a Dom node is by using a ref we can create a ref by pulling in the use

ref hook and then simply calling use ref usually we will initialize it with null

if we're using it to access a Dom node and we'll save it as a variable which let's call it button ref at its core

refs allow us to save values between the render Cycles without actually

triggering a rerender itself many times this ends up being used to access a Dom

node from the markup that gets returned from our component with this button ref I can use a dedicated property on all

react elements like this lowercase b button called ref and I can set my button ref on this button by doing this

when react renders these elements it's going to set button ref equal to this Dom node which I can then call methods

like focus on as a reminder I can come up here and console log my button ref

we'll see that at first it ends up as an object with a current property whose value is null and that's because we

initialized it with null but then after it rendered the button down here it set it equal to something different we're

just not seeing that in the console log if I click one of these then it triggers a rerender of our component and this

console log runs again now with the correct value of button ref which again is an object with a current property

whose value is the Dom Noe of that button scrim but makes it look like it's

kind of a jsx element or something but that's just a simple representation of the actual Dom node okay so with hint

number two I want to automatically call focus on my button ref. current only

when the game one variable is true and in this case we need to synchronize our

local game one variable with the Dom by manually imperatively calling the focus

method on that button so what tool do we have that allows us to synchronize our

local react stuff with an external system like the Dom well that tool is

use effect and so I'm going to pull in use effect let's get rid of this console

log here and at this point I can get rid of my challenge text and Below game one

because I'm going to need to add game one as an item in my dependency array I

need to make sure I do it after we Define it I can call use effect and I'll

pass the first parameter which is my callback function and before I forget my

second parameter which is the dependencies array that looks at game one this way this effect will only run

on the very first time that the component renders and then again if game one ever

changes this gives us an opportunity to check if the game is one then we can

simply call Button ref current that's the property we have to access in order

to actually get to the Dom node and then . Focus let's see how we do we'll hit

save I'm going to just select all of these fives and when I click the last one our

new game button gets focused so all I have to do is hit spacebar and we get a new game this is a much better

experience for for any of our keyboard users and a benefit for me the teacher was a great opportunity to review some

of the topics that we learned in the last section this has been an awesome project and now we have finally rounded

out the last features since we're here at the end of this project and near the end of the section this is a great time

for you to maybe do a little bit of a self assessment look back at all of the code that we've written in this project

and think to yourself is this something that you could write by yourself if you needed to I as an instructor can only do

so much to request of you to do all of these challenges by yourself without just letting me hold your hand through

them and in your self assessment if you feel like maybe you could have done a better job then there's absolutely no

problem with going back to the beginning of the section looking at that blank screen that asks you to spin up a brand

new react app and seeing if you can do the series of challenges again if you

really want to be a crazy person you could simply highlight everything and hit delete and try to build it again

from scratch things like this terrify me personally but I know some people really thrive on challenges like that before I

have a panic attack let me command see that and get all of my code back oh and I can't leave it like this where our

game is basically useless with this automatic five number being put in every one of our dice all right that's better

congratulations on making it this far it truly is a major accomplishment I hope

that you're feeling proud of yourselves and I hope that you can find a great way to celebrate this

win forgive the pun but you my friend are on a serious role what a great job

you did on that significant series of challenges and what a fun project to build this is one of those projects that

I can bring my kids in and have them play and they actually have fun playing it it is so rewarding to build something

like this that other people can enjoy and the fun doesn't have to stop here I have a few extra credit ideas that you

can roll with if you want for one you could try adding a timer and or a roll counter to see how quickly you can win

the game or in how few roles you could win the game you could style the dice so that they actually look like real dice

with pips instead of numbers and you could deploy your project live so that others can play on their own machines

the possibilities are endless but one thing that I do want to make sure you do is to head over to the today I did

channel in the scrimba Discord Community there's really no better place to celebrate with others that are also

working on similar improvements and content as you and it doesn't have to stop there feel free to share it on your

LinkedIn or your ex accounts if you're planning on looking for your first job in Tech then there's no better way than

to engage with the communities that are around you once you've had a chance to celebrate for a little bit remember that

the job isn't done we have one more really awesome Capstone project in this course and so that's what we'll be

gearing up for next everything in this course has

culminated up to this final Capstone project called assembly end game in this

game you are fighting the forces of evil to try and save the world's programming languages from being extinguished only

leaving the Assembly Language left okay let's be real it's just a rebranded version of hangman but instead of

drawing a little person every time you get a wrong guess you eliminate one of the programming languages from the world

so let's see we've got a felet word here oh shoot so e is not in the final letter so HTML it's been real we've lost HTML

let's try a oh no CSS is gone I O a look at that okay we've lost JavaScript but

we still have react on the line oh this is tough uh let's try an L uh let's see

is this the word floor nope oh no we've lost react maybe blood a look it is the

word blood so we are still left in this world with some usable languages and we can see that we've won the game this is

going to be a super fun project to work on you can click on the screenshots here to see the different designs that we

have over in figma and I want to take this chance to reemphasize the importance of trying to do all of the

challenges on your own before watching me walk through the solutions this is a critical part of your education and it

can be so tempting at even the first slight hiccup in trying to complete one of the challenges to then just click

continue and watch me do it and think to yourself oh yeah I think I kind of understood that I could have gotten that

that is very tempting even for me so don't fall into that trap if you do feel like you get stuck rather than just

skipping the exercise and watching me do it turn to the scrimba community and ask for help or for more immediate feedback

start a conversation with chat GPT and ask it to help clarify any questions that you have you might even want to

preface it with don't write the answer for me but help me understand this going through that process although much more

tedious than just watching someone else do it is the way that you get better at this all right strap yourselves in for

the battle of the welfare of our programming

Community when you're just starting out building a project that's as exciting as this one at least I think this is an

exciting project it can be so tempting to just jump immediately into the code and start building the project however

it's a really good habit to get into to spend some time planning out your project even if you're not why framing

it and writing down a whole bunch of steps that you're going to perform simply getting a highlevel overview of

the project and thinking through it ahead of time before diving deep into building it can really help set you on

the right path so before we code anything I wanted to take some time to do a little bit of project planning

together and my hope is that it will help set a good direction for you as we go through the next series of challenges

that we have so I have a few questions that I came up with and these are certainly not the only questions that

might help you plan your project ahead of time but one of the things that I like to ask myself especially when we

are given a design like we have here remember you can click on these screenshots to go to the figma design so

you can inspect all the specific details of them when we're given a design like this something that I like to ask myself

is what are the main containers of elements that I'm going to need as it turns out this tends to be a great place

to start scaffolding your app when you are coding it so that you don't find yourself too deep down one rabbit hole

without being able to show any progress on the other parts of the app another thing that you can think about is what

values you're going to need to have in this app because we're working in a react app you can think specifically

what values need to be saved in state and what values might I be able to derive from the already existing state

another thing that's important to keep in mind is the user that's using your app and so you could ask yourself how

will the user interact with my app and what events do I need to be handling so I've typed these questions out right

here actually I'm going to put a little bit of extra space between them because just like a quiz I want you to type in

here the answers that you come up with on your own there's no right or wrong answer for this it's really just to get

your mind working from a higher level view of the project to help guide your development from this point forward I'm

going to move the slides over to the screenshot of the game so you can refer to this especially when you're answering questions 1 and two which might prove to

be a bit of a help while you're answering these questions so I'm going to put in a pause now and I'll give you a chance to type out your answers to

these

okay the first one what are the main containers of elements I need in this app let's just use our Winning State

version here in the middle we can see there's kind of a header up at the top it's just some static information we

have this bar in the middle that seems to present some kind of game status we

have the U win or the game over but we also saw when we were playing the game that it will give you messages along the

way so it's kind of a status section below that we have a list of languages which will be updating as you're playing

the game name next we have the actual word that we're trying to guess with a blank spot for every letter of the word

and the letters filled out that we have correctly guessed then we have a keyboard section which is the main point

of contact with our user this is where they'll be clicking around to make their guesses and finally a new game button at

the bottom which will only show up at the end of the game identifying all of these sections gives us a great starting

point with how we can start scaffolding or bootstrapping this project okay let's see question number two what values will

need to be saved in State versus what values can be derived from the state I think the answer to this will become

more apparent as we start writing our code but it's still helpful for us to think about it ahead of time perhaps an

even more enlightening question isn't what will be held in state and what will be derived from state but simply what

values do we need to know about for example we need to know if the game is over or not whether that's something

that is saved in state or derived from State might become a little more obvious as we're writing the code but it's good

to know we need to know if the game is over we need to know if the user has won or lost we need to keep track of how

many wrong guesses the user has had as well as what the randomly selected word

by the game is and which letters the user has already guessed knowing which letters the user has already guessed and

the correct word will help us determine which keys on the keyboard should be green versus red versus yellow the

display of the new game button at the bottom will probably be determined by that value that we determined earlier

whether the game was over or not and there might be a few other little hidden ones here and there as we go throughout

the app now you'll notice I'm not necessarily typing the answers down here I think it's helpful to type the answers

down but for the sake of time I'm just going to be speaking them out loud okay we kind of touched on this already how will the user interact with the app and

what events do I need to handle it seems like the main point of contact is our keyboard here the user will be clicking

on the keys which should cause renders where it will determine if that was the right guess wrong guess change the

keyboard update our word or kill off another programming language so the keyboard is probably the main point of

contact with our users and lastly a new game button which of course will only show up when the game is over hopefully

you can start to adopt a quick planning session like this into your own workflow because I truly believe is going to help

you not only avoid pitfalls that you might not have seen otherwise but to in general become a better architect of

your code because you've given yourself the opportunity to plan things out ahead of time all right now let's take what we

have just discovered through this project planning session and now with a better overview let's start building some pieces of this

project I've always felt like a great way to start making progress on an app is not to get too bogged down in getting

all the functionality working right away but instead to just get something on the page so we're going to be taking little

bites out of building this project by first just adding a little header section that includes the title of the

game and a little description paragraph the overarching goal for the next few Challen Alles is to build out the main

parts of the app but we're just going to start with this little piece for now one thing that can be helpful to note as

you're working in CSS is that I have already made the body Aid Flex container with everything Justified to the center

which is why game goes here is in the center I've also Chang the background color the text color the font family and

a few other things similar to the tenes app as we're building out the main structure of the site we will be

spending a bit more time in CSS and because this is a Capstone project I also expect you to write the CSS I know

that might not be everybody's favorite thing but when you get a job as a react developer they are going to expect that

you know how to write CSS okay go ahead and get started on this

challenge you might have noticed in the final version of the code that we saw that we had opted to kind of just put

everything here inside of our hangman function and actually you know the name of this is a Remnant from when I first

started writing it let's call it a s assly end game so we could spend a

little extra effort by moving things out into other components but at least for now while I'm scaffolding and

potentially for the entire life cycle of this app I'm just going to be putting everything here inside of my assembly

endgame component so instead of game goes here let's go ahead and create a header element and because this is the

title of the game this is an appropriate place to add an H1 we'll say assembly

end game and then let's add a description in a paragraph and I am just

going to paste in the text from the design let me start out by making this a

little bit more narrow and I think I'll wrap this just to save a little bit of horizontal space okay we're going to

have some design that we need to work on which I think will be next so I'll come over to my CSS and let's go ahead and

select our header because we're just going to have one header I don't know that I'm going to bother to give it a

class name I think it'll be enough for us to just select the element itself the body is justifying this to the center

but the text still needs to be centered so we can say text align to the center

and well actually you know that might be the only Style on the header specifically let's go ahead and select our H1 now and we will bump the font

size down a little bit cuz the default styling is a little bit large let's go ahead and say 1.25 remms the design also

shows that it has a little bit less of a bold font weight so we'll set that to to 500 and yeah it makes a tiny difference

and then we have to look a little bit closely but in the design we can see that the color is slightly different from anything else it's kind of a

yellowish color at least that's kind of how it looks on this background okay let's go ahead and select the paragraph

now because that also has a different font size which if we convert it from

pixels in the design to RS we get about 0.875 Rim I don't love how it's wrapping

it looks a little bit wide to me so I'm actually going to include a Max width

and let's try 350 pixels okay that's wrapping a lot nicer at least to me and

then we do have a different color so we'll set that to the same color as the design all right this is a good start

next you know I think we'll just kind of work our way down the page we'll start on this status

section we're still in these challenges where we're building out the main parts of our app mostly focusing on having the

I elements on the page we'll worry about interactivity later so your challenge this time is to build the status section

which comes right below the header for now because we're not worrying about having it be too Dynamic you can just

hardcode in a winning game State maybe that will boost your mood through the rest of this scaffolding process so go

ahead and get started on this

challenge as with most of these CSS challenges there are certainly many different ways that you could do it so

don't feel like the way that I'm doing it is necessarily the best way or the correct way it's probably just the way

that makes the most sense to my brain so below our header I'm going to add a section and while I'm here I'll go ahead

and give it a class name of let's call it game- status we'll get the content in

here and then start worrying about the design for it the style for the you win

text inside of this status is not only a little bit larger but the semantic meaning of it I think holds a little bit

more weight to the status of the game so I'm going to make it an H2 we've already

used an H1 on this page so we'll just move on to the next one and we'll hard code in uinn and then below it we'll

just put a paragraph that says well done awesome okay I'll hit save so those

elements will show up on the page and yes we have some styling to do let's go over to our CSS we already created a

game status so I'll select game- status and sometimes I like to give myself an

indication as to what kind of element this is being attached to so I'll do something like section. game status for

now we are going to hardcode in the background color that's the green winning color and because there's two

elements in here I could try to space them correctly and everything but I think I'm just going to set this to a

display of flex use a flex Direction not Flex basis but a flex direction of

column I'll align the items to the center and it looks like it's already

Justified to the center I don't think I need to say justify content Center yeah but doesn't appear to be doing anything

it looks like there's some default styling applied to the H1 and to the H2

and the paragraph So let's select those individually I'm just going to bring this line down and then access the H2

we'll set the font size to 1.25 RM oh and it looks like the design the color

is different oh actually the color for both is different so let's just do that in the parent here we'll change the color to that kind of more yellowy color

like our header up here while we're at it let's see what it looks like to get rid of our margin and well zero is going

to be not enough so first let's maybe do this to the paragraph as well I'll set a

margin of zero yeah it's a bit squeezed and I think if I make this something a little bit bigger like five pixels and

we'll say five pixels oh yeah that looks much better let's see there's also a border radius which we missed so border

radius of four pixels it looks like from the design just to round out the corners of the status and then I want to

separate it a little bit from this header I can use either margin top and margin bottom or I can combine them and

use margin block which is a helpful way to just provide margin to the top and bottom of an element and okay yeah that

separates it in a nice way all right this is looking good on to the next

challenge in the next part of this challenge we will add the list of languages with elements that are

sometimes referred to as chips they're just like little badge elements on the page so that's the challenge this time I

want you to create those language chips however it's going to be a little bit more involved than that I've provided to

you a new file called languages. JS this is an array of objects each object

representing one of the languages that will get displayed on the page collecting them together in objects like

this allows me to not only provide the name but also whatever background color and regular color they should be using I

mostly didn't want that to be super tedious for you to have to do manually or to have to create nine separate

elements down here in your markup because this is a Capstone project I'm going to continue being pretty vague but

I did want to give you a hint for the layout and that is for the container that you use around these elements if

you set it to a flex box and make sure that it can wrap it should make your job a lot easier you might also need to

apply a Max width so that it doesn't just try to span the entire width of the page for reference I'm going to be using

a Max width of 350 pixels okay that's all the hints I'm going to give you get started on this

challenge all right let's create a new section this section will act as the

container for my language chips and as such let's go ahead and give it a class name of of well let's just call it

language chips language- chips now I'm not going to hardcode anything here but

instead I'm going to import my list of languages from let's see languages JS

export const okay this is not default exported which means I need to destructure it and this is going to come

from languages and uh this needs to be a relative path let me just make sure this

is working I'm going to console log languages and okay good they're coming into this file just fine

with that array of languages I can map over them and create new elements on the page for each one of them a common thing

to do is to do that map operation directly here inside of your markup although my personal preference has

leaned towards creating a separate variable here in the body of my function before my return so I'm going to create

a new variable that I call language L's for language elements no let's call it language elements and this is going to

be an array from calling languages. map we'll look at each language and let's go ahead and return

we'll make these spans they seem like they're maybe appropriate as a span the text inside will be Lang do was it name

let's go check yeah lang. name and then we have background color and color so we will use those in our Styles actually

let me put this down in this section first and hit save just so we can see that this is working okay that is

terribly ugly but we're on the right track so inside of this span I can provide an inline style and so that's

what I'm going to do this needs to be an object and actually you know for the sake of saving my horizontal space I

think what I'll do is create a new variable which means I can't do an implicit return anymore let me Shuffle

some things around here we're going to return this span I can get rid of this

and by doing that I can now just create I'll say Styles is equal to an object where the back ground color is going to

be lang. background color and the text color or color is going to be lang.

color and then I can just pass in my Styles object right here the other way would have worked fine too this feels

better to me for some reason let's see if that made any difference okay well that's a good step in the right

direction I think in our CSS we can Style Both the language chips as well as

the individual language chip so let me give this a class name or rather give

each one of these a class name and I'm just going to call it chip for now we'll

hit save and then go over to our CSS oh actually let's fix this warning first

where we need to add a unique key prop our list of languages doesn't have an ID for each object but the name is

guaranteed to be unique because well we're not going to be adding to this list so I'll just use the lang. name as

the key and I'm going to start putting these on their own lines so let me add a

key which is equal to to lang. name okay good our warning is gone let's go over

to our CSS we have language chips that we need to style and chip that we need

to style so section dot language- chips

I had mention that we should change the display to flex and that we want it to

wrap so I can set the flex wrap to wrap okay awesome we need a little bit of

space in there they're really crammed in together let's give it a five pixel Gap we want things to be a little more

centered let's justify the content to the center and I had mentioned that I'm going to be adding a Max width of

350 pixels okay let's work on the individual chips and I think that might

finish this off those were spans with a class of Chip and let's see in the

design it shows they have a border radius of three pixels and a little bit of padding around them looks like it's

about 4.5 pixels wow that's actually looking pretty great let me try resizing

the browser here just to make sure that we're doing pretty good and yeah it's not a big deal if that wraps down but we

probably won't be getting too much smaller than this anyway nice work on completing that challenge let's move on to the next

one all right let's display our word on the page to do this you will want to

First create a current word in state and for now just for fun we can initialize

it as the word react act this represents the random word that the game will choose for us but for now we'll just

hardcode it then in order to display each of the letters you'll map over the letters of the word which means you'll

need to turn it to an array first because map only works on arrays and then display each one as a span element

inside that span just make sure you're capitalizing the letters and then just generally style it to look like the

design just a little hint in case it helps anybody in order to get the little underline at the bottom of the box you

can simply use the Border bottom property in your CSS all right go ahead and get started on this

challenge let's create some new state just here at the top of our component it will be for current word and of course

Set current word equals and let's see we're importing react I think I'm going to

import use State like this and call use state

and we'll just initialize it as the word react I guess we could initialize it as capital letters but this looks like it's

screaming to me so I'm just going to use react like that all right well let's create another section where this can be

held I'll give it a class name of word and I could do my map right here inside

of my markup but once again I'm going to keep it consistent by doing it up here maybe let's call it letter elements

and I need an array to work with but what I'm saving in state is a string I can simply turn a string into an array

by calling current word dosit on every empty space which if we conso log letter

elements we can see gives me an array of all the letters in the word and now that

I have an array I can map over it all right for each letter I'm going to

return a span and we'll just put the letter in the span we'll give it a class name and actually

we can just select the span inside of word yeah let's do that I'll hit save oh

we need to actually render this so I'll take my letter elements we'll put it here in the section okay well that's

underwhelming but let's go ahead and style it over in our CSS we will select our section of word and I think I'll

probably reach for Flex box once again we'll set the display to flex we'll Center it with justify content going to

buy some room by putting a margin bottom on my language chips above there of I think the design shows about 36 pixels

and let's put some effort now into the span so I'm just going to select the

child element of the span inside of my section and each item will have a height

of let's see the design shows 40 pixels so we'll say 40 and then we'll also do a width of 40 a background

color of this kind of dark color from the design ah and then they are sitting

in the upper left I think for each span I can also use a display of let's try

Flex I might have to change this we'll justify the content to the center and align the items to the center and oh I'm

just realizing that we're working with lowercase letters here not the end of the world but I had asked to uppercase

them so I should probably do that here we'll say dot to uppercase

okay that is better ah and of course we are getting our keyr error oh and we're

console logging stuff still let me clean something up here let's see right here we're cons logging the letter elements

let's get rid of that and we'll hit refresh okay we're still getting the key prop issue so when we're mapping over

this I guess we need to decide what unique property we're going to use now this isn't something I normally would

advise doing but because we're working with something that isn't guaranteed to have unique elements I might be working

with a word that has multiples of the same letter I can't just use my letter as my key but I do know that I'm not

going to be removing any letters from this list or rearranging them or anything I mean in the game I might be

hiding them but the word itself is not going to be rearranging the letters and because of that I can actually access

another property inside of my callback function for map of the index of each item that it's mapping over and for now

this is going to work just fine as a key because again I won't be rearranging anything and it will never get confused

by react okay that suppressed that warning for us looks like we're almost there let's go back to our CSS I think

we can bump up our font size this would be the equivalent of

1.125 Rim okay let's add that border bottom of one pixel solid and then it's

this color from the design and in the design it shows a little bit of space between these let's add a gap of two

pixels and oh not to the word but to the word list here all right wow that is

looking awesome again I know we're doing a lot of CSS here we just have one more major element that will take a bit of

CSS and that is our keyboard and after that we'll finally be able to start jumping into the functionality of this

app arguably the most important part of this app is the keyboard it's the main

thing that our users are going to be interacting with and it's your challenge to get it up on the page I've created a

static variable that just has all of the letters in the alphabet that you can use to map over the letters and display the

letters in the keyboard make sure that you make each letter in the keyboard an actual button element because well

semantically that's correct and it also will come with a bunch of free accessibility benefits as well go ahead

and get started on this

challenge all right let's come down and I'm going to to create yet another

section we'll open that up I'm going to give it a class name of let's say

keyboard and we'll come back to The Styling in a minute kind of like we're doing up here we'll render H what should

we call it maybe keyboard elements we haven't created that variable yet so let's go ahead and do so right here

keyboard elements is equal to the alphabet dosit the only reason we have

to split it is because I wrote it up there as a string just so I didn't have to type as many characters trying to put

each letter as its own string in an array okay so this gives us an array and then we can map over that array and for

each letter in that array we will return a button element it's going to have the

letter inside and actually I forgot to mention this but I wanted to uppercase

it so that's what we'll do we're mapping so we need to make sure that we include a key and because we are only rendering

one button for each letter of the alphabet I can use that letter as unique key we're not worrying about the

functionality for it quite yet so I don't know let's see what it is we hit save and oh whoops I did that wrong

that's supposed to be the actual variable of the letter that's why I got my key warning okay there we go you

could have chosen either flexbox or grid to style it honestly because of the design grid seems to make more sense but

because of my stronger familiarity with flexbox I'm actually going to lean on flexbox to handle this one so let me

access the section with the class of keyboard we'll give it a display of flex

we need to make sure that it can wrap so I'll say Flex wrap wrap will give a gap of eight pixels and let me space it away

from the word a little bit maybe right up here we'll give a margin bottom of

like 20 pixels yeah looks better we'll justify the content to the center and I

believe it's going to yeah it's just going to keep spreading out so again I'll give this a Max width of I think

the design shows it's around 450 pixels now things aren't lining up super well but I suspect that has to do with our

actual keys so let's access section. keyboard and then the spans inside no

the buttons inside all right the design shows that it is 35 pixels high and wide

oh yeah look at that that lines up much nicer I'm going to copy the background color from the design

let's change the default border for these buttons to a one pixel solid and

then I'll paste in this color from the design as well I usually like to make my buttons have a cursor of pointer and oh

we need a little bit of a border radius as well I think it shows that it's three pixels all right I don't know what you

think but that seems like it is working and looking pretty good to me now the last piece of our app is to have this

new game button at the bottom but because I love you guys and you've done such a great job on the challenges so far I have a little surprise I can snap

my magic fingers and just like that we now have a new game button in our app yay I figured

this was an easy enough element we didn't really need a whole separate challenge for it we're in our second Capstone here you don't need a challenge

on how to add a single button okay well it sure is looking good but of course it's not doing anything so let's jump

into the next challenge where we will start adding some functionality to this

all right so we've added the keyboard let's start working on making the keyboard actually work of course the

user is going to click these letters in order to give their guesses as to what should be in the word right now we're

displaying the word it's going to be blank letters of course so our overall goal for the next few challenges is to

allow the user to start guessing the letters by clicking the buttons the specific challenge for this scrim is to

be announced but first I want you to think what's going to be the best way that we can store the user's guest

letter I'm going to put in a pause here and give you a chance to think through

that because we need to remember the user's guessed letters across every

render of our component and we know that when the user guesses a letter we want to update the UI in a few different ways

right we need to display the letter here if it is a correct letter we need to cross out one of the languages if it's a

wrong letter we need to change the keyboard key color if it's right or wrong to either green or red so because

of all those things we want to make sure that we save the user guest letters in state so let me type out what your

challenge will be your challenge is to create a new array in state to hold the user's guest

letters and when the user chooses a letter or clicks one of these buttons you need to add that letter to the state

array for now we're not going to worry whether it was a right or wrong guess there's a few other ramifications with

that so we're just going to focus on adding it to the state array and you'll probably want to conso log this array

just here near the top of the component so that you can make sure that it's working correctly go ahead and get started on this

challenge okay we'll create some new state maybe we'll call it guest letters

and set guest letters is equal to use State and we'll initialize it with an

empty array let's go ahead and console log Our Guest letters as a reminder this

console log is going to run every time our component gets rendered and because we're about to make it so that clicking

the button will set state that will render it and that will run our console log right here okay maybe right below

the alphabet here I'll create a click Handler we'll call it maybe add guest

letter we are going to need to know what letter was guest so we'll assume that we

can pull that in as a parameter to the function to update our state of course we will call set guested letters we do

need to know what the previous letters were so we'll access the previous letters uh letters in a callback

function and as a first iteration of this function let's just say we're going to return a new array that has all of

the previous letters and then adds the new letter at the end some of you might already notice what kind of issue we

might face with this but we will fix that in a second let's take add guest letter and where are our buttons right

here's our keyboard buttons and so I will add maybe right here I'll add an onclick that runs add guest letter but I

need to do a little bit more than this because remember when I have an event listener like onclick if I just pass a

function I don't get to choose what parameter it receives it's going to receive an event object from JavaScript

so what I can do is simply wrap this in its own Anonymous inline function and then the only thing that function is

going to perform is calling add guest letter at which point I can pass in the

letter while we're mapping over them to that function this is getting a bit wide

let me clean this up a little bit okay let's hit save and open our

console a b c d e FG awesome if you

haven't yet discovered what bug I introduced in the way that I wrote my ad guest letter function here I'm going to

refresh this page and give you a chance to see if you can figure it out so I'll put in a pause here see if you you can

figure out what kind of bug we have

currently if the user keeps guessing the same letter a bunch of times we are going to be duplicating the guest

letters in our array and that's not what we want to do we want to make sure that we are only including letter into this

array if it isn't already present there's a few different ways that we can do this and just for fun I'll show you

two different ways that you could choose the first thing we could do is let me put this on a separate line actually let

me just get rid of this we're going to be doing it from scratch here one way I can ensure that I'm not duplicating the

letters here is I can check if the previous letters already includes the letter that I'm trying to add and I can

use a Turner that says if that returns true in other words the letter that I'm trying to add already exists in the

previous letters then I can just return the previous letters I don't need to make any changes to it but otherwise I

can do what we were doing before where we just spread in the previous letters and then add the new letter to the end

here let me put these on their own lines as well let me hit save and just make sure this is working if I click a I get

a added if I click a again okay it's not adding it perfect let's do B and C and

then try to do a again it looks like it's logging it to the console but at least it's not adding the previously

guessed letters to the array and duplicating them again just for fun I think it can be a good learning experience to see another way that we

can do this perhaps using an API in JavaScript that you're not yet familiar with I'm going to get rid of what we had

and let me fix my brackets here open up the body of this and what we can do is create something called a set in

JavaScript a set is very similar to an array in JavaScript except it doesn't allow for duplicates it's built into

JavaScript to not allow duplicates and so what I could do is create a new variable let's call it maybe letters set

and that's going to equal a new set and we can pass in the array of previous letters to pre populate this set then I

can say letter set. add sets in JavaScript have a method called add and

you can add the new letter to the set which will automatically remove duplicates from the set then I can turn

the set back into an array and return it by using return array Dot from my letter

set let's go ahead and see how this is working I can click a yep I'm clicking a a bunch of times this does have an

interesting side effect where it is rendering our component even though we're not changing the state of this

variable so that's kind of interesting but it is working and oh we probably not seeing those lower ones so I can click a

b BBB CCC and the array just has a b and c in it well I haven't taken the time to

figure out why it is rendering the component every time I click it whereas what we had before is not and so I think

I'm actually just going to back up to the other version right here and we'll just leave it at this either solution is

completely fine and valid okay now that we have a way to store in state the letters that the user has

guessed we have the ability to start working on some of the other user interface pieces of the app where the

game can give feedback to the user so that's what we'll dive into

next all right folks this is one of those challenges that's going to require you to think critically I'm being pretty

vague in all the steps that will need to take place in order to complete this Challenge and as a bonus you are going

to get a chance to read about and use a fairly popular thirdparty react package so first let's talk about the challenge

I want you to update the keyboard keys to display whether the selected letter that the user just clicked is right or

wrong as you can see from the design if the letter is a correct letter that's in the word then it turns green if it's

wrong then it turns red for testing purposes we're still keeping the current word as react and displaying it here

we're going to get to obscuring that and choosing a random word later but this will really help with testing of course

if you hit re e a c or t then the letters should turn green and if you choose anything else they should turn

red as a bonus I am recommending that you use this clsx package it's going to

require you to go learn about it but as you can see it receives about 21 million weekly downloads so it is a pretty

popular package and its whole purpose is to give you a chance to construct the class name String that's the string that

you are passing into your elements like this right here class name we have hardcoded it to be chip or in the case

of the button which we are going to be styling we are not passing in any class names and clsx gives you a chance to

construct those class names conditionally so if you want to use clsx you're welcome to do so click on the

screenshot here to go to npm and read all about it there's a chance that the documentation may prove a little bit

confusing if you find that's true then don't be afraid to turn to Google or the AI assistant of your choice to ask how

this package is used so try to psych yourself up for this awesome Challenge and I'll turn it over to you to start

working on

it when I first was building this app I thought to myself I wonder if I should save in state an array of all the

correct letters and another array of all the incorrect letters but then I realized that we can easily derive that

value by simply looking at the array of guest letters and by looking at the current word as we are mapping over the

alphabet and displaying the buttons for each letter of the alphabet we can take the opportunity to check if the current

letter that we're looking at is in the array of guested letters and if it is then we can check to see if it's correct

or Not by seeing if that letter is also in the current word if those two conditions are true in other words it's

been guessed and it's in the current word we can change it to the green background and if it's in the guest

letters but it's not in the current word then we we can change it to the red background no new state necessary at all

I can simply derive those values based on the state that we already have so let's come down to our keyboard elements

here and I'm going to need to include some additional logic before I return this button so I'm going to open up a

set of curly braces and move my button inside just so I have some ability to

write some additional logic here I'll go ahead and put this in a parentheses while I have some serious formatting ISS

choose to figure out right here okay but now that I'm doing an explicit return I can start writing some additional logic

up here so let's think what are some of the values that I need to know well I need to know if the letter has been

already guessed remember I'm mapping over the alphabet and this map operation

is going to happen every time our component rerenders which means I know that I can have an updated version of

our currently guessed letters and the current word so if I want to know if the letter has been guessed I can simply

check inside of the guest letters to see if it includes the current letter that we're mapping over okay well now let's

check to see if the guest letter is correct well first of all it's important that the letter has been guessed

otherwise it's neither correct or incorrect so if it is guessed and the

current word includes this letter then yes this is a correct letter guess and

it wouldn't be enough to have an is wrong variable that simply says it's not

is correct because every letter would be considered wrong because we're not comparing it to make sure that it's been

guessed so we would simply say const is wrong is and I'm just going to take this logic and reverse the fact that it's

included in the current word okay how is this helpful well at this point I could now add a class name to my button and

try to do a crazy nested Turner that says first let's check to see if it's

guest and then if it is let's check to see if it's correct and if it isn't

let's check to see if it's wrong and apply certain class names accordingly but this is where the clsx package comes

into play what clsx allows me to do is create an object where the keys are the

names of the classes that I might want to apply and the values of those keys is

a Boolean as to whether or not that class name should be applied this will be much easier to just show so let me go

ahead and create a new variable called class name and this will be the string that gets returned by calling the clsx

package or function rather there's a bunch of different ways to use clsx as

I'm sure you discovered from the documentation but the most common way that I find myself using it is to

provide an object and as I mentioned the keys of this object will be a potential

class name that will end up on the button in the end so for example I might have a class name called correct and I

only want the correct class to be applied if is correct is true and I

could do another one for wrong or incorrect let's call it wrong and say this is if is wrong is true I haven't

created these class names yet but let's finish up our work here first of all I need to apply this class name that

results from calling clsx and I don't believe I've imported clsx yet so let's

go ahead and do that before that becomes a problem import clsx X from clsx is a

pretty hard thing to say actually now that I'm saying it so many times while we're still here let me go ahead and

console log class name we'll get a better idea of what's going on here well

this console actually doesn't show anything but the little popup down below shows that it was an empty string let me

see what happens if I click a oh whoops we do have an error here current word. include is not a function yes this needs

to be includes sorry for anyone who was shouting at their screen because that

was a mistake okay let's try this again we'll click a okay look it console logged correct if we put B it's going to

console log both correct and wrong and that's because what it's doing here as it's looping through the entire keyboard

it's looking at each letter and it saw that a was guessed and it is in the

final word or the current word which is react so we have an A there is correct

became true it applied the class name of correct and then it just console logged that class name for that specific letter

which was correct then it continued through its map and it got to the letter B it said yes this is in the list of

guest letters and so it is guest but it is not in the current word so is wrong

is true which means that wrong is going to be applied and it consol logged wrong

and then I think behind the scenes there's actually a bunch of empty strings that are happening because every other letter in here is not gu

okay let me close the console I have some styles that I just have copied over it just has the background colors from

the design so let's see where is here's our keyboard and we'll just put these

right there okay button. correct and button. wrong and I would have thought that would have applied let's go ahead

and hit save let's try a and oh you know what is happening we have a specificity

battle going on up above I am being more specific about this button than this button so I guess let's just add the

same level of specificity well actually increasing the specificity and okay there we go we get our letter A being

colored as green because it's in the final answer let's go ahead and click B and awesome so let's go back up to our

Challenge and sure enough we were able to update the keyboard when a letter is right or wrong this should work all the

way through R should be in there let's see T should be in there and we've gotten all

the letters so everything else should be read feel free to continue playing around with clsx we are going to be

using this in a couple different places in this project mostly to help us avoid any crazy nested taries or having to

write a bunch of conditional logic just to determine our class names I guess another thing to note about this package

is that although we are using it in a way where these are mutually exclusive classes it doesn't have to be that way

you can provide an object that has a lot of different class names and it will just apply all of them where the value

at that key ends up being a truthy value all right we're making great progress let's keep it

going all right there's really no hints that I'm giving you this time at all I'm just asking you to add the next feature

to our app so your challenge is to only display the correctly guessed letters in the word right now we're displaying the

entire word which of course defeats the purpose of a game like this so now that we have some UI feedback as to whether

the letter that they guessed on the keyboard is correct or not if the letter is correct then we want to display it in

the final word but otherwise we just want it to display nothing I guess an empty string I'm going to let you find

where in the code you would need to make that change and that's it I'll hand it over to you now to work on this

challenge well naturally I think the first place we want to look is where we are displaying these letters and so if

we come down to the letter elements this is where we are looking at the current

word we're splitting it so it's an array we're mapping it and then for every letter in that array of letters so re e

a c and T we're creating a span and inside that span we are just

automatically putting in the letter so this is where our logic is going to live instead of always putting the letter in

we could put in a Turner here that's says if the guest letters remember the

array that we are keeping track of as the user is clicking the buttons If the

guest letters includes the current letter that we're mapping over in the current word that means that the user

has guessed this letter and it was correct because at this point we are only mapping over the letters in the

actual word and so I can use this turn that says if the guest letters array includes the letter that we're looking

at and I'm actually going to pop this onto its own line here then I want to

display the uppercase version of that letter but otherwise I'll just put in an empty string so when I hit save all of

the letters should disappear perfect oh it looks like I still have a console log hanging out for this class name let's

get rid of that so the letters disappear and then let's start guessing the letters we know that it's react so r e a

c and let's do a nonl like w and okay perfect nothing else updated and we'll

do T awesome although the final code ended up being pretty straightforward

hopefully this was a good challenge because remember I only gave you the feature that we wanted to add and it was

up to you to figure out how to do that if you were able to do that that is a great sign that you are following along

you're understanding this code and ultimately hopefully you're not getting stuck in tutorial Hell by just watching

me do all of this with without actually getting your hands on the keyboard and practicing we're making great progress

let's keep it going

we're on to the next goal so far there's basically no consequences to getting wrong letters and so we need to add a

little bit of tension to the game by adding in the mechanism that will count the number of incorrect guesses and

actually have consequences that lead the user to potentially losing the game in this game we only have eight wrong

guesses that we're allowed to get before assembly is the only language that we're left with in the world and so we need to

be able to count how many wrong guesses the user has had we talked earlier about how we could have chosen to track in

state an array of correct letters and then another piece of State for the wrong letters and honestly that could

have worked just fine however the way that we currently have this setup where we have the current word and the array

of guest letters both of which are being held in state we can actually figure out how many wrong guesses the user has had

based on just these two values so your challeng is to do exactly that I want you to derive a variable which you can

call wrong guess count for the number of incorrect guesses by using these other state values current word and guest

letters that we're already holding in this component we're starting to add a bunch of extra values here either for

State or the static value or we're about to create a derived value so I'm actually going to create a little bit of

Separation with some comments I'll say that these are the state values let's say this is a static value and uh we'll

just say values in case we have to put something else there and right here we will add a section for derived values

for now once you have created this variable just to test it we'll say that uh you can just console log the variable

or let's say the wrong yes count we'll make better use for it in the upcoming challenges all right the time is yours

go ahead and get started on this

challenge well we have an array of all of the guest letters both correct and

incorrect ones so if we could filter out the correct letters from this guest letters array all that would be left is

the incorrect letters and then we could simply take the length of that array to get the exact count for the number of

wrong guesses the user has had this certainly is not the only way to do it but it is the way that I will be

proceeding so we'll say const wrong guess count and actually just for now so

that I don't have to try and chain too many things together I'm going to maybe have a wrong guesses array and we'll

just take care of this in two steps I will probably end up combining them once we understand what's going on here okay

so let's look through the guest letters array and we're going to create a new array by filtering out the correct

letters and so my filter is going to look at every letter in the guest

letters array and we only want to include in the resulting array this

wrong guesses array the letters that are not in the current word so I can say current word. includes and

I'll go ahead and put my negative there because I want to make sure that the current word does not include the

current letter that we're looking at from the guest letters array let's do a little bit of an intermediary step we'll

console log the wrong guess's array okay starts out as an empty array as we'd

expect if I add a okay we're still an empty array because that was a correct letter let's go B okay look at that

we've got a B in there d F perfect just for good measure let's put in a correct

letter okay we're console logging the array again but it does not of course include the correct letter great well

then obviously the only last thing we need to do is take the length of the wrong guess's array and that's going to

give us our wrong guess count at this point instead of creating a separate

variable I'm just going to have the wrong guess count like this and chain on

a DOT length at the end of everything else that we have let's just go ahead and and make sure oh whoops I put this

in the wrong place this is where I put the do length and I want to console log

the wrong guess count okay let's try it out zero a is correct so we're still at

zero e is correct still at Zero D okay we're at 1 2 3 4 and five cool this

wrong guess count is going to be pretty crucial for us to be able to do a couple of the other things involved in adding

this incorrect yes's mechanism to the game like starting to cross off different programming languages or

knowing if the game has been lost that's also going to help us fix our status section up here which currently is just

hardcoded to you win and so this was a pretty important feature that we just added and something that I think is kind

of nice is that we were able to just derive it from the state that we're already maintaining generally speaking

if you don't need something to be in state it's usually better for it not to be in state let me go ahead and clean up

some of these Extra Spaces here and awesome great job on this Challenge on to the next

one now that we have access to the number of incorrect guesses from the user one of the first things we can do

is to mark off the languages that have been lost based on how many incorrect yeses there have been to me the CSS for

adding this little gray overlay and the skull felt a little bit outside the scope of the course and so I just went

ahead and added these rules here it's just a pseudo element where if you add the Lost class name to our language chip

it's the span with the chip class then it will gray it out with an overlay that's opacity of 70% and it has this

little skull emoji and everything else here feel free to look through these CSS rules if you want but as I said it just

felt a little bit like a distraction to worry too much about this the only thing you really need to know is written up

here in the challenge text when you're mapping over the languages you should determine how many those languages have

been lost and then add the Lost class if it is a language that's been lost I give

a hint here where you can combine the wrong guest count that we figured out in the last scrim right here and combine it

with the current index of the item in the array as you're mapping over the languages array you're welcome to use

clsx if you want if you do decide to use clsx you'll need to refer back to the

documentation on how you can always include a class name because right now

we are including this hardcoded chip class name and we want to make sure we don't lose that this one however is a

relatively easy one to do manually just right here inside of this class name prop if you'd like all right time to get

your hands on the

keyboard all right so let's come down to where we are mapping over our language elements and let's try to reason through

how we can determine if the current language that we're looking at while we're mapping over them is a lost langu language well if we can get access to

the index of the current item in the array since our array will always be in this same order that we see here we can

know that if we have a wrong guess count of one then any index that's less than

one or in other words any index that's less than the number of wrong guesses

should be considered a lost language and needs to get the Lost class name added to it inside the Callback function of my

map I can add a second parameter called index which gives me access to the

current index of whichever item we're mapping over and with that current index I can create a new variable that says

something like is language lost and set that equal to the Boolean that results from saying the index is less than the

wrong guess count so if our wrong guest count is zero then even the item at the

zero index is not going to be considered lost because Zer is not less than zero

if our wrong guest count is one then this will evaluate to true for the very first item and we'll mark it as lost if

the wrong guest count is two again this will evaluate to true for the items with the index of both zero and one and so

forth with this is language lost variable I now can update my class name

to include the Lost class name if that's true and I'll just show this in two different ways I can do this manually by

updating my class name here to use a template string and simply say is

language lost and use a Turner and if it is lost then we'll add add the Lost keyword otherwise we'll just maybe use

an empty string so we don't add any additional classes and let's try this out we'll hit save we'll choose a wrong

letter and awesome well not awesome we lost HTML let's do a correct letter or

maybe a few correct letters and then another wrong one oh no okay bye CSS

okay look at this we are doing this correctly okay well since we do have the

clsx package I guess it doesn't hurt to use it so right here I'm going to create

a class name variable and I'll give clsx a call we want to make sure that

unconditionally we always include the chip class and so if one of the parameters that I passed to this

function is just a string then it will just always include that in the final resulting class name I also don't have

to use an object like we did with the keyboard letters instead I can just pass in a Turner here that says is language

lost if so then include the string lost otherwise well actually you know what I

could even do the short circuit double emand method and this should work just fine too in clsx if this evaluates to

false then it just will ignore this parameter to the function anyway then I can come down here and just update all

this with the class name that we determined above let's hit save and we should get the same results we're

getting closer and closer to the end great job on this Challenge and since I don't think I've said it recently take

some time to look through our code again if any of this has been confusing for you it's time to put in the effort to

become familiar with this code before just plowing ahead there's absolutely nothing wrong with doing that in fact

just plowing ahead will put you in a worst spot in the end once you're ready we'll keep moving

forward currently we are rendering our new game button even at the beginning of the game your challenge is to create a

new derived variable called is game over which evaluates the true if the user has guessed incorrectly eight times eight

times because we have nine items in our languages array but we want to leave assembly as the only remaining language

at the end that said I do want you to consider how we might make this value or this is game over value a bit more

Dynamic if we were to ever add or remove languages from the languages array over here in this languages. JS file once

you've completed challenge number one your second challenge is then to conditionally render this new game button only if the game is over and at

this point it doesn't matter if they've won or lost it's just if the game is over for this first part try to think

critically as to what conditions in which the game should be considered over and in this case I don't mean game over

like in the old Mario game over where you lost it really just means game over whether you won or lost all right your

turn to take the Reigns and work on this

challenge I didn't type this down but I did mention it as I was speaking but this is game over value is something

that we can derive based on the existing state and because we know that the game should be considered over whether the

game was won or lost maybe the first thing we should do is try to derive some State about whether the game is lost and

then we could say well the game is over if either the game is one or the game is lost so let's go ahead and first create

is game one and again you may have chosen a completely different way to approach this that's okay I didn't say

anything in the challenges about creating these extra variables I'm just going to use them to separate

my logic out a little bit more okay well how can I know if the game is one let's think about this one well I've got my

current word this of course has all the correct letters in it what if I were to check to see if every single one of the

letters in our current word was also in our array of guessed letters that should

mean that the user has guessed every one of the letters in the current word which should indicate that the game has been

won I could do a for Loop to Loop over every letter in the current word I could use a map but there is a builtin method

called every which allows me to pass in a function that should return a Boolean

for every item in the array on which I'm calling every the Callback function

returns true then the entire expression evaluates to true that's going to make a lot more sense if we actually see it

written down so first I need to take my current word which is a string and turn it into an array so that I can even call

the dot every method on it so we'll say current word dosit and that will give me

the array of letters in the current word on which I can call. every and we'll

look at each individual letter and if the guest letters array includes this

letter this will evaluate to true and if every single letter that we map over in

this current word returns true as in every one of those letters is included in the guest letters array then every

will return true and this entire expression will return true and so is game one will be the ban value true okay

cool I think that should work just fine well maybe let's go ahead and conso log it so we'll conso log is game one we'll

hit save and then just type out the correct answer so false that's good we haven't yet won the game r e a c that's

a bunch of falses and then T and we evaluate to True perfect let's close the

console get rid of our console log now let's work on is game lost this one's a

little different intuitively it might seem that we should just say it's the opposite of is game one but the state of

the game isn't either one or lost there's also a currently Inplay state of

the game instead we'll need separate logic to determine if the game has ended and is lost well we know that the game

is lost if the user has a wrong guess count that is equal to eight or I guess

greater than or equal to eight just to cover our bases and and actually let's type it out that way first we'll say

wrong guess count is greater than or equal to 8 but now as I mentioned in the challenge text it would probably be

helpful for us to consider how we can make this more Dynamic if the length of the array were ever to change so maybe

instead of eight hardcoded we'll just say languages. length minus one because

again we need to leave assembly here so that at least if all the other programming languages disappear we can

still program something well somebody can program something I certainly couldn't okay so that finally leads us

to the is game over variable the game is over if either the game is won or the

game is lost so now that we've put that work in we should be able to easily say is game over is equal to is game one or

is game lost this is kind of just an intermediary convenience variable anywhere that we are relying on it we

could have theoretically just said is game one or is game lost but this way is a little bit fewer characters all right

so that was challenge number one number two we need to conditionally render the new game button only if the game is over

so we'll come all the way down to our button right here add some curly braces and we'll go ahead and say is the game

over and if that evaluates to true then we will render this button okay let's test it out we'll hit save and let's see

should we win or lose first let's go ahead and win first R E A C T okay cool

our new game button has shown up let's refresh this and just do a bunch of lost

letters here oh I guess he is in there okay one more and we should be up not going to do R let's do Q all right the

new game button showed up there too perfect with our new derived values we have a new Improvement that we can make

to our app so that's what we'll jump on to

next now that we know whether the game is over and whether the person has won or lost we can come back back down to

this game status section and update it so that it's not a hardcoded uwin but instead we'll only display this uwin

well done message if of course the user has won the game or alternatively we'll display this game over you better start

learning assembly if the user has lost the game there's actually a third status that we're going to include here which

is a sort of farewell message to each one of these programming languages whenever the user gets a wrong guess but

we'll be worrying about that in a little bit so for now your challenge is written up here I want you to conditionally

render the one or lost statuses from the design both in the text and the Styles

based on the new derived variables that we created is game one is game lost or

is game over as a quick note we want to make sure that we are always rendering the surrounding section so you can see

in the design here even when there is no message being displayed we want that space to be open and if we were to

remove that section from the Dom with conditional rendering then I think everything else would kind of bump up

and then when a message popped up everything would bump back down we just want to leave that like an open slot all

right the time is yours get started on this

challenge let's come down to this section and we're going to be dealing with this section right here and as I

mentioned we don't want to conditionally render this whole section because things would start to jump around on the page

instead we can conditionally render what's inside that section so we will open this space up a little bit one

point of trouble that you may have run into is that we get an error if we surround two of these elements in curly

braces like this just like how components need to return a single parent element if we're going to be

evaluating an expression that has some jsx inside it needs to be surrounded with a single parent element we could

use something like a div or because we don't necessarily want to add any additional elements to the page we can

just put in a fragment just like this now there's a lot of different ways that we could handle the conditional

rendering here and there's certainly not one correct way just like in most of the stuff that we do when we're building

these apps so the different approaches that I'll show you now are just different options that you might choose

on the top level we can think of it as having two different states one where the game is not yet over and we want to

display either a blank space or if we go into this design the little farewell message while we're in the middle of

playing the game when the user chooses a wrong letter or the other state is that the game is over and then it kind of

branches again from there either they've won or they've lost currently we are only really dealing with this second

scenario where the game is over and we can use a Turner to help us determine on the top level which of those two major

States whether the game is over or the game is not yet over is true so let's say if the game is over then we will

render this section and for now I'm just going to put an else in here that maybe

just says null let me format this cuz my spacing is looking a little funny at this point we could decide whether we

want to Nest another Turner inside here to check if the game is one and if the

game is one we render this one that says you win and otherwise we render the one that says that you lost or game over

alternatively we could just change the text because we want the H2 and the paragraph to stay there whether they've

won or lost but for some reason I think I would prefer to Nest a Turner here in

this case it wouldn't be terribly confusing I think I'd be able to read it kind of like an if else statement which

is a little bit of foreshadowing as to the next way we're going to see to do this so rather than putting a Turner

here to determine the text and then another Turner here to determine this text as well let's go ahead and just

give this a shot we'll say if the game is one and we're just nesting a Turner

here we'll move this fragment with the H2 and paragraph inside

and if the game is not won in this instance we can know that the game is lost because we're not reaching this

code unless the game is over and then there's only two options from then the game is one or the game is not one which

means the game is lost so maybe then we'll just copy this and we'll indent it

and then we'll change our text it says game over and then this one says you

lose better start learning assembly and I just copied that from The Design This is something we'll be coming back to

later but I guess this isn't so terrible if we have our indentation correct then

we can kind of read this like an IFL statement before we refactor anything here let's go ahead and get our Styles

working because our styles are still going to make it look like they have won even if they've lost let me just guess a

bunch of wrong letters here okay so it says game over you lose which is great

that's a good first step but the green box sure makes it look like we won the game just like how there's different ways that we could have done this

conditional rendering there's a few different ways that we could handle changing the Styles as well because we're kind of on a kick using clsx here

I think I'm going to use clsx so above my return just right here I'm going to

create a new variable called game status class and I'll set that equal to clsx or

a call to that function clsx and we have a class name that's already being used

here of game status so let me copy this and put that as my first argument which

just means that I want you to always include the game status class and I guess I'll go ahead and set this equal

to the game status class this is the string that's being returned from clsx

and then I can provide maybe another object where I have different properties like a one class that is determined

based on a condition and a lost class that is based on another condition well

we have variables that I think help us know when we're won or lost so so I will apply the one class if is one or is game

one is true and I'll apply the Lost class if is game lost is true and we'll

keep a close eye on these to make sure that this logic is correct let's go ahead and refresh this app we haven't

changed it since we added our little nested Turner in there and okay because the game is neither won nor lost we have

a blank message there but the space is still being taken up so that's good the green box is not good so let's go over

to our CSS and add some rules for one and lost so let's go over to the CSS and

here's our section with the game status and I think right here I'm going to add

section. game status. one and I'll do the same thing for DOT lost both of

these will just be changing the background color and the winning color

is this one actually I guess I can just take this line out of there and put it right here and the losing color from the

design is this one right here all right let's uh go intentionally lose the game

to see if that's working actually let's win the game first we owe ourselves that okay react awesome okay the space got

taken up it has the green background it's got the new message perfect let's refresh and we'll intentionally lose the

game okay perfect as you can tell a successful completion of this challenge

did require a bit more than what I had led on in the beginning I just gave you the feature and expected that you would

be able to think critically and do some of these tasks by yourself this was a hard challenge so if you didn't quite

complete it then like I've said before don't feel bad this is all part of the learning process if you were able to

complete it then do your little happy dance because that's pretty impressive I had mentioned that we might look at a

different way to do this conditional rendering and so I think in the next lesson I'm just going to quickly show you another way that we can handle the

logic that we're currently doing right here

before we jump into a quick side lesson I wanted to apologize for anyone who is following along locally I had a design

flaw that I didn't realize I had introduced here because as I'm recording here in scrimba our mini browser here is

quite narrow and the flaw was something that I kind of overlooked those of you who have been using a wider screen have

probably noticed that things are not aligning quite right and it turns out it's any of the elements that I have

added a Max width to you see when I have the justify content Center on my body

it's taking the center point of the element as it would be if it weren't constrained with a Max width so this

paragraph for example which we can clearly see is off center from the entire page if I take the max width off

then it expands to its full width and the center point of it aligns correctly with the center of the page I can come

down here to let's see this is my language chips I also have a Max width if I take that off then it aligns

correctly to the center I do still want those to have a Max width just so that they wrap in the way that I want so

there's a few different fixes that I can provide I can either on every one of these put a margin in line of Auto but

another fix that I found is we can provide another Flex box to the parent

of all of these sections so that would be the main element I can say the display is going to be flex and we're

getting a crazy layout right now but we will adjust the flex Direction so that

it points downward in a column kind of like block elements and then I can use align items to the center and just like

that we get everything nice and aligned to the center because of this I actually no longer need my display Flex or ad

justify content on my body so I can get rid of those Styles and everything's in harmony making the main element its own

Flex container does introduce a new problem if I win the game we can see that our status message is really tiny

now it's being compressed to only fit the space that it has and so something we might want to add to our section with

a game status right here is and I'll group these with the other sizing properties we'll say the width should be

100% but we will also set a Max width and just need to spell that right of 350

pixels that is looking much better and everything seems to be in harmony now

again I apologize for anyone who was just ringing their hands at the missile alignment I know that would have bugged

me if I were in your shoes all right let's jump back in and learn about another way that we can handle conditional

rendering sure correct indentation can make our nested turnery look at least a

little bit manageable but come on these crazy frowny faces are just really pretty awful I personally don't love

nesting Turner and I thought it could be helpful for us to see another way that we could handle all of this conditional

rendering it might be tempting to think well I can just simplify all of this crazy Turner logic by putting an if else

statement directly inside however as it turns out we can't use IFL statements

inside of our jsx expressions like this and that's because IFL statements don't implicitly return anything an expression

on the other hand like a turner does automatically return these values and since they get returned as a JavaScript

expression automatically does then it can get rendered to the page however that doesn't stop us from using an if

else statement inside of a helper function so I'm going to just come up here right let's see maybe right below

our game status I'll create a function that we call render game status and

because I'm inside of a function I can return something from these functions and I can use JavaScript statements like

an if else block at this point it's more of an algorithmic challenge to figure out exactly how to equate what we have

down here with what's going to be in the function I don't think that's an important part of the scope of this course so one way I

could do this is to quickly do an early return and say if the game is not over

so is game over then for now we're going to be changing this later but for now we're returning null so I can say let's

return null because this is an earlier return from this point on in the code I can assume that is game over is true and

so I can just separately check is the game one if so let's return and let's

grab this guy right here and put that there and otherwise we will return this

one down here later in this series of challenges we are going to be finding some of the things that we can offload

to a separate file and because of how tall this function is it feels like a good candidate for that for now we're

not going to do that and I can just simplify all of this by calling render

game status maybe I should hit save and test this out first okay let's win the game

first okay awesome that's applying the way we'd think and then we'll go ahead and lose the game I guess I can't keep

choosing correct letters if I want to lose the game okay awesome again this is

not a right or wrong way to do it when I do find that my rendering logic is getting a little bit complex I'll

sometimes prefer to offload that to a function that lives inside the body of my component we've really been jumping

from one challenge to the next I think it might be helpful at this point for us to step back again and take a quick

inventory as to what we might still be missing in our

game just to reorient ourselves after this Whirlwind of challenges that we've done so far I think it could be helpful

for us to take an inventory of the features that we still have in our backlog if you've gone over to the figma

design you have already seen that we are planning to do these farewell messages every time the user gets something wrong

and I don't remember if I've mentioned it but these are going to be randomly chosen from a list of different farewell

messages so we do still need to handle this use case so we'll say that we need some farewell messages in the status

section we also have a few pretty glaring accessibility issues that we need to make sure we fix so I'll say

we're going to fix the accessibility issues and maybe just in case you didn't already know this because it took me an

embarrassingly long time to figure this out but the reason accessibility is shortened like this is because it's

starts with an A it has 11 letters in the middle and then it ends with a Y you'll also see abbreviations like

internationalization which is I 18n because there's 18 letters in the middle

of these two letters okay so we have some accessibility issues we need to fix we also currently have a new game button

that doesn't work so we need to make the new game button work we're currently hardcoding the word that we need to

guess as react so we need to actually choose a random word from a list of

words and then last but not least we definitely want to make sure we drop some confetti when the user wins we'll

certainly be making other improvements and little tweaks to the app along the way but I think this represents a full

picture of the backlog that we still have to work on maybe this would also be a good opportunity to remind you that if

you've been sitting down for a while maybe it's time to get up stretch take a few deep breaths go for a walk do

whatever it is you need to do to reenter and refocus yourself I also won't be offended at all if you

decide it's time to shut down the computer and pick this up at another time as they say we need to sharpen the

saw once you're feeling refreshed and renewed let's jump into this backlog and continue making progress to finishing

this app this is a fun game but let's not

forget what's at stake here every time the user gets a wrong letter we have to Bid Farewell to one of the languages

that gets erased from existence including this farewell message up in the status bar is your challenge for

this lesson as a help what I've done is created a get farewell text function inside of this new util.from

returns one of them now I'm not going to click on it but I do have a hintmd file

that I have created if you give this your best shot and you find yourself getting stuck for maybe more than 15 or

20 minutes at that point you would have my permission to go over to hintmd to see if that hint helps you out but I do

want you to do your best to solve the challenge without using that hint if you can the time is yours go ahead and get

started on this

challenge all right since I assume you have done that challenge now I'll go over to the hint and this instructs us

that we need to know if the most recently guessed letter was a correct guess or not if we think in terms of the

render cycle for our game when the user clicks one of the buttons to choose a letter what's actually rendering our app

is that we are placing that letter in an array of guest letters guest letters doesn't indicate if it was a correct

guess or not we are deriving that information elsewhere but simply by adding it to the array of guest letters

our app is rendering and then based on that information is updating the display

if the guest letter was in the word then it puts it in its correct spot in the word if it wasn't in the word then it's

killing off one of our programming languages and marking the letter as red as the keyboard gets rendered however we

need a way to know if the last item in that array of guest letters was a correct guess or not and by the way this

probably isn't the only way to do it it's simply the way that I came up with but I'm super open to feedback if

somebody comes up with a more logical or easier to reason about way then I would love to hear it come over to the Discord

you can at mention me you can even send me a DM on X if you'd like Okay so let's come back to our app and maybe just to

get started I'll go ahead and import this function we'll import the get farewell text from utils and maybe what

we can do is derive whether or not the last guest letter was a correct letter

or maybe since I'm going to display this only if the last guest letter was incorrect we'll go ahead and say const

is last guest letter or let's just say last guess

incorrect okay well I can get access to the last guest letter by finding the

last item in our guest letters array so maybe I'll do that separately just so that I can kind of separate my logic

here a little bit let's say last guest letter that is going to be equal to the

array of guest letters at the index of the array of guest letters. length but

then we have to do minus one just because of the zero indexing so this will get me the last guest letter it

doesn't indicate whether it is correct or not but now what I can do is I can check to see if the current word

includes the last guest letter and because this is a Boolean as to whether it's incorrect I'm going to say it does

not include the last guess letter let's console log this is last guess incorrect

we'll hit save oh interesting we did show True when the app was first

rendered even though we haven't made a guess yet and that would be because guest letters is an empty array guest

letters. length is zero and so we are trying to index into guest letters at

the index of -1 which is going to be undefined so maybe we can just protect

against this by making sure that the last guest letter is a real value and

only then will we check if the current word includes the last guest letter okay let's try this again okay undefined

that's going to work for us because it's a falsy value and we'll pass any of the conditional checks that we have later

well actually before we continue on let me try this okay so we get yes it was an

incorrect guess as the most recent one it should be another true another true

and then let's do a letter we know is in there false okay good that is correctly telling us if the most recent guest was

incorrect okay so what do we do now whenever the most recent guess was an incorrect guess then we want to display

the farewell message we wrote a helper function to help us determine what should get rendered in that status

section right here in render Gam status and we were just returning null if the game is not yet over but what we can do

now is to also check if the last guess was incorrect so we can say if the game

is not over and the is last guess incorrect is true then we can see we

just have a single line here maybe we'll just render this as a paragraph so I'll

return I need my return here return a paragraph and for now let's just get the

styling correct I'm going to just say by we'll add a class name and maybe we'll

say this is a farewell message and over in our CSS we

can select the farewell message let's see game status here's one lost let's go

ahead and oh look this is probably going to select the paragraph We already have that's okay um actually yeah let's

duplicate this one and then make sure that the paragraph has a class of farewell message and I'm just going to

paste in some of the styles that you can find in the design which gives it a dashed border a purplish background

color it makes it italics bumps up the font weight a little bit and well let's just see what this looks like I haven't

yet saved over here let's make sure yep we're returning this it's just going to say buy for now let's hit save and oh

shoot I've made a mistake in my logic here and let's think about it okay so the game is not over the last guess is

not incorrect so we're not considering it correct but it's not incorrect so then it skips this it comes to if the is

game one is true that's not going to be true ah so then it's just hitting the else and it's telling us that the game

is over you know what let's instead of having this else here let's explicitly check if the is game lost is true then

we'll do that and then otherwise at the very end after all these returns if none of them hit then we will return null

okay let's try again oh awesome okay our game over is gone let's go ahead and hit Z and oh look at that I just realized I

don't want to put my styles on the paragraph I want to put those styles on

the game status this is a mistake on my part I think I'm just going to leave it here in the recording because it's a

very common thing so we can go back and fix this let's see we have some styles that are already being applied

dynamically with clsx let's go ahead and just duplicate this we'll change this to

be maybe a class called farewell and let's take the section specific Styles

which are the background color and the Border here and we'll just replace that one clean this up a little bit the font

style and font weight I believe I still want to be sitting there on the text itself and so now we will go over to

where we have our clsx call right here and let's add another one called farewell and let's think this is going

to apply if the is last guess incorrect but I think we might also want to make

sure that we're not conflicting with the is game lost styles and so let's just make sure that the is game over is not

true and the last guess is incorrect let's try this out we'll get an

incorrect guess and okay well our styles are playing it's floating up there at the top a little bit let's go check that

out and right here yes it looks like we're doing a display of flex Flex Direction column we're doing a line

items which in the column Direction makes it centered horizontally but in this case we will also need to do

justify content Center and okay great Just for kicks let's refresh again and

see if the other message is still working even though we changed the justify content and so I'll need to win

the game real quick okay good that's looking great let's get rid of that console log that's running every time

we'll clean up our challenge text and just like the message says well done there's a lot of moving parts to this

challenge we had to create a couple more derived values so that we could more easily check to see if the last letter

was incorrect and therefore displaying that message the last thing we need to do is call our get farewell text

function maybe I prematurely deleted the challenge text but that's the last thing we need to do instead of it just saying

by we want to randomly choose one of those farewell messages so let's see

right here it's saying buy instead let's go ahead and call get farewell text and

let's see we need to call this function but it's expecting the language to be passed in so how can we get access to

the language that was just removed well let's see one language is going to get removed for every incorrect guess and I

believe we derived some State yeah for the wrong guess count so what if we

index into the array of languages at the index of wrong guess count and then I

think it would have to be minus one because language is is zero indexed let's go ahead and give that a try so

right here get farewell text uh this is getting really long let me put these on its own lines and and I'll put the class

name there we'll just kind of format this a little bit okay so I can call get farewell text I need to index into

languages to try and find the correct language in this array I want to index by the wrong guess count and then that's

going to be minus one and then we have to remember too that languages is an array of objects and so if we want the

name of the language we're going to have to callame oh boy okay let's see if that works let's get it wrong and all right P

HTML sad day but also happy day it's working that's quite a roller coaster of

emotions we're on great work on this challenge I know that there were a lot of moving parts to this and something

that seemed as simple as just display a simple message here ended up being quite a bit of logic hopefully that went well

for you that we're really building something that has a lot of moving Parts I think I don't need this on its own

line actually that's good enough and we can check one more item off of our backlog we're getting closer to

completing this app

before we jump into fixing some accessibility issues I added another item to our backlog which is to disable

the keyboard when the game is over right now when the user completes the game let's go ahead and win here they can

continue to guest letters and lose the game which wow gives us some pretty strange results here in order to stop

the user from continuing to guess we can simply disable every one of these buttons whenever the game is over this

is just going to be a super quick challenge it's your task here to do exactly that so go ahead and disable the

keyboard when the game is

over let's see let's come down to our keyboard elements and inside of the code

for our button we can simply say disabled is equal to is game over so

let's hit save buttons are still working which is good because the game is not over and okay just like that we can no

longer click these buttons maybe let's just add a little bit of styling here so

let's go ahead and say inside of the keyboard the button when it's disabled

let's give it a cursor of not allowed and then we can actually set some opacity on it just to make it a little

more obvious that the keyboard is disabled okay well doing this brings us into the next part of our backlog which

is to fix some accessibility issues I was planning on starting that in the

same lesson but I think just to keep everything organized we are going to do this in the next

lesson one thing that's really important to do as you're building your app is to try and keep accessibility in mind

specifically when you're choosing what elements to put on the page for example we made sure to make every one of the

keys in the keyboard a button element because we get quite a bit of accessibility benefits for free by using

a semantically correct button element instead of for example just making this a div that is clickable buttons

automatically come with their own Focus State the ability to tab through them and you can make divs accessible but you

just have to do a lot more work to get that done however when we're working in react and we're dynamically rendering or

removing things from the page it's still really important for us to keep in mind what is changing and what might be

difficult for assistive Technologies to keep up with if we don't specifically cater our code to those needs the thing

that got me thinking about how we need to disable the keyboard when the game is over is that we want to also tell

assisted technologies that those keys are disabled there are some screen readers that will announce when a button

is disabled but some of them don't and so we can add a dedicated Arya disabled property if we can find our buttons here

okay right here we have disabled it but we can add an Arya disabled and we could

decide to set this equal to is game over in the same way that we did with the disabled property however when we're

thinking about someone who is using the Tab Key to tab through all of these letters maybe a better user experience

would be to disable the ones that have already been chosen to do that I could simply say something like the array of

guest letters includes this current letter that we're looking at and I guess at that point it might be a choice to

decide if that's also when we want to disable the keys in general we've already included some logic that doesn't

allow the user to keep trying to add the same letter to the array of guest letters so I think I'll probably just

leave it the way that it is thinking about the user experience from the point of view of someone using a screen reader

as well when they're tabbing through these the screen reader will say the letter that is currently being focused

in the button but it might be just a slightly better experience for us to label it with maybe the word letter

beforehand so it actually says letter a letter b letter C I guess at that point it might just be a preference I'm not

really sure but let's go ahead just for the sake of it and add an ARA label and this will simply say the word letter

followed by the actual letter okay so that should make the user interactive

part of it a lot more usable for those using assisted Technologies we also need to take some time to look at any

portions of our site that are being dynamically rendered well one of those is the status message that pops up up

here screen readers are not just going to automatically announce things that get added to the Dom by react but

fortunately there's a way that we can Mark certain portions of our app as sections that will be live updated so we

chose to render this with a function which is right here in render game

status but the parent of these elements is just down here in the markup right

here this section with the game status what we can do is add an ARA live region

to it and say that it is polite polite just means that it's not going to interrupt the rest of whatever it's

currently reading to announce changes to the section it will kind of cue it to the end of any changes that the screen

readers currently reading there's also a role property and we can essentially say this section's role is to be a status

let me put these on their own lines and doing this will give us some additional accessibility benefits okay well let's

think about another part of this app that kind of acts like a status and is definitely something we would want to

have read to our users if they're using a screen reader well I think it's going to be pretty important that they have

some idea of what the current revealed status of our word is and while we could

just surround the let's see this one this is our actual word we could

surround this in an AR live region just like we did up here above with the game status however because this is such an

important part of the game I think we could put a little bit of extra effort into what gets read out by a screen

reader when this is being updated now because this isn't a dedicated course to accessibility I am just going to kind of

explain the code that I'm writing as we go and hopefully it will give you some ideas of how to improve your own apps in

the future something that we can do is we can create an entirely separate section whose sole purpose is not to

display anything visually but to be read out loud by a screen reader and then with CSS we can just completely hide it

from the Dom so maybe right below our word here I'm going to add another section and I'm going to add some CSS

that will essentially just completely hide it from the Dom we'll give it a class name of Sr only for screen reader

only then in our CSS I'm going to just paste in a screen reader only class that

I have defined in another project it essentially is removing it from the visible area and doing everything it can

to make sure it never shows up then just like we did in our status section we can

also put an ARA live of polite and a roll of status right let me put these on

their on lines too and oh I said Dash instead of equals okay so now anything

that I put inside of this section is just going to be read out by the screen reader and that will happen anytime

there's an update to this section so maybe the first thing I'll do is to put a paragraph that will just read out what

the current word is and because this will never be there visually I can actually type in the text that I want

the screen reader to read so I can say something like the current word colon and then I can just have it read out

each individual letter of the current word so let's see we we have our current word We'll add a do split to turn it

into an array and then we can map over it and for each letter in that array if

the letter is currently revealed or in other words if the array of guest letters includes the current letter then

we'll just have it read out the letter out loud and uh not the literal string letter but the letter itself and

otherwise well it won't read anything out although I have found that if you have an empty string it's just going to

ignore it so what we can do is actually just have it read the word blank so it'll say something like R blank blank

blank blank another thing that I have found as I've played around with screen readers is that if you add a period like

this it will add a little bit of an extra pause so if there were multiple letters instead of saying racd just

super fast I think this might give it just a little bit of a pause between them I guess don't quote me on that I'm

not 100% sure it's been a little bit since I've played with it okay well let's see I'm still mapping over this

but I'm not actually turning it into a string that it can read out and let me put a period here too just in case that

works the same way as I was describing before but now we can join things back together and we'll put a little bit of a

space in there just to make it a little more readable for the screen reader okay I know this looks a little bit crazy we

could probably offload some of this to a helper function if we want but I think this is going to get the job done for

now there's actually a little bit more that I want to add to this section but since we've bitten off quite a bit in

this lesson I want to give you a chance to review what we've done maybe think about other apps that you have created

see if there's any of these accessibility roles that we've talked about that you could apply over there and then there's one other thing I want

to add to this section which we're kind of treating like a generic screen reader status update section and so we'll do

that in the next lesson another accessibility user

experience Improvement that we can make is not just to reread out the current state of the word and the status that we

have up above but we could simply announce whenever a letter was guessed correctly or incorrectly every time the

letter is guessed so after the user selects a letter we could have the screen reader read something out like

correct the letter R is in the word or sorry the letter Q is not in the word we

could even add something that says you have six attempts left now we could choose to do that in a completely

different section but I think just before this paragraph I'm going to add another paragraph that will announce

whether or not the previously guessed letter was correct so let's go ahead and add a paragraph and what we'll do is

check to see if the most recently guessed letter is in the current word we'll have it read out correct the

letter whatever is in the word otherwise we'll have it read the negative side of that statement and I think we are saving

the last guest letter Yeah we actually created a separate variable up here so we can get access to that awesome so

let's see write down here we're going to check to see if the current word includes the last guest letter and if it

does this is where we can have the text of the paragraph just read out what we

want it to say so correct the letter and then this will be the last guest letter

is in the word otherwise we can put our message that says sorry the letter last

guest letter is not in the word and then whether it was right or not we could say

something like you have H we need to know how many attempts they're going to

have left let me just hardcode this we'll say you have four attempts left

and let's see the number of attempts that they have left is going to be we

had figured something out up above and yeah we were using languages. length minus one as our number of incorrect

guesses that we're allowed to have so I guess we could just use this again although I kind of want to just derive

that value so we can use it elsewhere maybe just right here at the top I'll say something like number of guesses

remaining left number of guesses left is equal to languages do length and then

minus one because we need to leave assembly as the last item okay so then number of guess is left Let's see we can

just say this and then with that new derived value we can come down to our

screen reader only section again and then instead of putting in the hardcoded for we'll say numb guesses left and with

just those few updates maybe a dozen or two lines of code we have now made this app much much more accessible for those

using any kind of assist of Technology of course it's also important to make sure you go through and make sure that

your contrast ratios are good enough and everything like that but what we've done here marks a huge step forward in the

accessibility friendliness of this app right now another developer coming to the section might pretty easily miss the

class name of Sr only and so I think it can be helpful to include a little

comment here that can say that this is a kind of combined visually hidden ARA

live region for status updates okay let's come up to our list here and we're

just going to mark this one off there likely are other improvements we could make there's always more that you can do

but we just have three more really small features to add to our game two of which are crucial for the functionality of the

game and one of which is just going to be a really fun way to wrap things up so next let's jump on to the next item in

our backlog and actually now that I'm looking at this I'm going to swap these two I want us first to choose a random

word from a list of words so that's what we'll be working on

next this should be a pretty short and sweet challenge we are going to make it so that a random word is chosen when the

game starts right now we're just hardcoding rea react but we're going to make it so that a random word will get

chosen I've created a new file called words. JS that has close to 500 words in

it I tried to weed out anything that was fewer than five letters and greater than

something like nine letters I think and so your task is to come over here to utils.py

algorithmic challenge nothing very react specific to it but then I want you to import that function into this file the

app.jsx file and figure out where to use that function go ahead and get started

on this

challenge all right let's come over to

utils.py a random number that's in the index of the array of words so let's

create a random index and set that equal to math. floor math. random and then we

can make sure that it's limited to the length of the array by multiplying this by words. length then all we have to do is

return words at the index of our random index easy peasy okay let's come over

here to our app file and from utils we're already importing the get farewell text let's go ahead and also import get

random word and we're really flying through this challenge we've already finished one and two let's figure out

where to use that function well we were hardcoding react as the initial word that we were using and instead of using

react we're basically going to be turning on the game now we're going to call get random word and let's try

playing our game we'll hit save and look at that we no longer have a felet word here oo this is a long one this is eight

letters let's see usually longer words in hangman are a little bit easier but

I'm not doing very well here Ah that's why there's two eyes sorry HTML CSS and

JavaScript we have already lost you let's see what could this be ah I think

this is military sure enough all right well we're still left with typescript node Python and Ruby so we did pretty

good military yay we won now some of you might have remembered that if we are initializing state by calling a function

like this technically every time we cause a render in our app react will

rerun this function even though it's not going to use its returned value to change the state again it is calling

this function again every time this get random word function is not a very expensive function but it doesn't hurt

us to use lazy State initialization which we learned in the last section by simply wrapping this in a callback

function this way on the very first render react will call this function and it will get our random word and set the

initial state but on subsequent rerenders it's just going to Simply ignore this function that way we're not

running any extra operations that we don't need to be awesome let's clean up

this challenge text and Mark this next one as completed the next thing we'll be

working on is giving the new game button some love so that clicking it actually resets the

game this is going to be another short and sweet one that's how you know we're really tying off the Loose Ends of our

game here your challenge is to make the new game button reset the game go ahead and get started on this

challenge all right well let's hook up our button first and then we'll write the logic for it so maybe just right

here I'll add a new function that says start new game and I'll just console log

start a new game that'll do for now we'll go ahead and hook up our button which is way down here at the bottom for

new game we'll say onclick it's going to Simply call start new game okay let's

hit save and I guess we need to actually play this game now in order to display the new game button oh no this is not a

good start oh I don't need to win this game for this to show up I can just lose the game okay let's go ahead and click

new game start a new game perfect okay oh I just thought of another feature we need to add we need to display the word

after the game has been lost otherwise it's so anticlimactic we never get to figure out what it was anyway let's stay

focused up here where we are resetting the game okay we don't need to console

log start a new game there are two things that we need to update first of all we need to get a new random word

because this one's been used now and secondly we are maintaining a list of guest letters and we need to empty that

back out because we want our keyboard to refresh we don't want to display any of those letters to the new word and so

forth so we can use our state Setter functions to set the current word and of of course once again we will call get

random word and then we will say set guest letters to an empty array once

again shorten suweet this should be working let's go ahead and just lose the game right now these last letters tend

to not be correct and we'll click new game and perfect everything starts over okay I'm actually going to add that item

to our list here we need to reveal what the word was if the user loses the game

in the meantime we can mark this one off we are so close to the Finish Line I can

practically taste it so let's hurry on to the next

challenge this one will require a little bit extra thinking compared to the last two challenges so what I want you to do

is to reveal the missing letters of the word if the user loses the game so for example let's just lose the game real

quick here oh jeez I'm not losing okay here we go we don't want this to be a mystery we want to reveal what the word

was to the user so you'll have to think through the logic of how these letters get displayed and if the game is lost

you'll want to reveal the missing letters and as it mentions here for now let's go ahead and style them with the

same red color that we use for the button Keys when they're incorrect go ahead and get started on this

challenge all right well let's go down to where we are figuring this logic out

of how we display the letters and that's right here when we're mapping over the current word I think the first thing

I'll do is figure out the logic to display the missing letters only when the user has lost the game and then

we'll worry about styling them the most concise way I could think to do this wouldn't be to conditionally render one

span or another depending on whether they missed that letter and lost the game or not although that would have

been a completely legitimate way to do it if that's how you decided to solve it currently as I'm mapping over the

current word I am publicly displaying that secret letter if it is included in the guest letters what I could do is

simply come up with another variable that will also display this letter if the game is lost so that if the game is

not lost it will only display it if it's in the guest letters and if the game is lost it will just display all the

letters so let's go ahead and do that one thing I can do is just create a new variable that's called maybe something

like should reveal letter and I want the letter to be revealed if the game is

lost just automatically display the letter or if the guest letters includes

the letter that we're currently mapping over oh and I was using an implicit return before so I'm going to have to

fix some of my brackets here let's see I'll move this down here we'll return the span yeah there we go okay so

instead of doing this we'll say should reveal letter and let's go ahead and lose the game and see if it shows all

the letters well this is a long one all right holy cow three T's okay statement yes perfect the word was revealed now

because clsx is so powerful we can use it to determine if the letter was not in

the guest letters array and if the game is over then we can dynamically add a class name so let's see right below here

let's go ahead and say maybe the letter class name is equal to

clsx and the first thing we want to make sure is that the game is lost we want to

add a class name if this letter was not included in the guest letters so we'll say if not guest letters do includes the

current letter then we can add the class let's call it missed letter I'll go

ahead and make sure to add my class name of letter class name I'll hit save and

come to my CSS and I guess we're already here so this rule right here the span is

what we're trying to attach to let's add a class for M letter and we will just

change its color to be the red color from the design okay let's go ahead and

lose this game wow that looks so good that is a much better end of game user experience

all right the last Challenge and arguably the most fun one let's make it so that our confetti will drop when the

user wins the game this challenge kind of feels like

in golf when you just barely missed a p and all you have to do is just send it home we've literally done this exact

same challenge in the last project at the end of tenes so this should feel right at home to you I've already

installed the react confetti package and imported the confetti component here all you need to do is trigger the confetti

drop when the user wins the game I'll hand it over to you to send us

home I guess before I walk through this challenge you may have noticed that I did have to downgrade my version of

react back to react 18 that simply has to do with the fact that react 19 is not

officially launched yet it's still on the release candidate version and it seems like the react confetti package is

not yet working with react 19 all right let's do it we'll go down to our markup

down here below and it doesn't really matter where we do it I think I'm just going to have it be rendered right here

at the top we'll call this a glass half full kind of decision and we'll say if the game is one then we'll go ahead and

render confetti now I actually actually am going to add some of the options to

confetti the props that you can pass to it specifically I'm actually going to turn off the infinite confetti by

setting recycle equal to false and you can specify the number of pieces these

are just things you can find from the documentation for react confetti and I'm going to bump it up a little bit to a

thousand let's do our best to win this game this would be a little anticlimactic if I lose now oh I'm on a

roll look at that I think we need another vowel here oh yeah o I think

it's distance here we go before I click the N it's going to be anticlimactic for

you as the viewer because you're not going to be able to see the canvas elements of the confetti dropping but I

can tell you that it is awesome what a celebration I guess you'll just have to hit refresh and play the game for

yourself now surely there are other improvements we can make to this game but before we jump into a recap of

everything that we did with this game I want you to take a second and just look at this code base this is a hefty code

base let me go ahead and check this off too obviously this doesn't compare to any Enterprise level apps that you're

making but this definitely represents the longest app that we have built in this course and it looks and works

amazing huge congratulations to you if you made it through the entire react course up until this point that is an

amazing accomplishment we are going to celebrate that even more in the wrapup that we'll do in the next scrim and

recap everything that we've learned

well you've done it you've saved Humanity from having to suffer through writing assembly for everything in all

seriousness this was a complex project and you have done an amazing job working through all of the challenges along the

way to building it and just like the tenes game this is another one that will be super fun to share with your family

and friends if you want to keep the fun going there are a few extra credit ideas that I came up with first you could

simply display the remaining guest's count we do have the visual of the remaining languages but maybe just

having the number of remaining guesses allowed could be a helpful UI addition we do celebrate the win with the

confetti component but you could consider rendering some kind of I don't know anti-c confetti when the game is

lost or maybe another animation that really makes the user feel that loss you could also Implement something like a

chess timer that starts when a new game starts and causes a loss if the time Runs Out adding a little bit of extra

pressure to the player there are a couple things that you definitely should do the first one is you should deploy

this live online so you can share it with other people including putting it in your portfolio and secondly you

guessed it you should head over to the today I did channel on the scrimba Discord server even if you don't have it

posted live online to share a link with other people simply leaving a message there to celebrate your win is a great

way to engage with the community amazing job completing this

project hey you did it we're here at the end of the course you should be so proud

of yourself for finishing because assuming you've done all the challenges and projects in this course you are well

on your way to becoming a proficient react developer as I said in the very beginning of this course My Philosophy

is that the easiest way to get good at something is to put in the work to do it the hard way and considering you are

here at the end having done all the projects you have put in the hard work and I can promise you that it will have

been worth it let's take a look back on the projects that we worked on in the different sections of this course and do

a quick recap of what we have learned in section one we started with really basic

static pages and reacts that we could build a solid foundation to support the rest of our learning in react and we

begun that section by First Learning why we even care about react in the first place we talked about how react is

declarative making it a much better developer experience and how react is composable allowing us to build reusable

pieces that can be combined together to make a masterpiece P of a web app we touched on setting up a new react

project not only in terms of the code that you have to write but also how to do it on your local machine then we

learned about react elements and how jsx was created to make creating those react elements a very familiar experience

similar to writing HTML then we learned about the Crux of composability in react

by learning about custom components custom components allow us to collocate logic markup and styling all in the same

place to create a custom reusable piece of code and then of course we needed to make sure that we added some styling so

that we weren't just throwing around ugly components with that knowledge we were able to build our first static

react fax web page from there we moved on to our second section where we built a travel journal what set this travel

Journal apart from the react fax project is that it was Data driven we really drove home the concept that reusability

is extremely important and learned how we can take our react components pass props into them so that they could be

reused in multiple different ways once we knew how to pass props into a component similar to how you pass

parameters into a function we learned how we can use vanilla JavaScript array methods to create components from an

array of data doing this allowed us to put the data for our travel journal in one place and simply map over it to

create the ultimate view on the page this meant that if we wanted to add new entries to our travel journal or change

a detail of one of the items all we had to do was change it in one place the data then we really dialed it up to 11

and jumped into this Chef Claud project in Section 3 this section was entirely dedicated to building interactive web

apps whereas before we were working with static readon Pages now we're able to

respond to the users inputs by learning about event listeners and how we can update our app based on the interactions

of our users we learned about state which allows us not only to save information between one render and the

next but also allowed us developers to focus on updating the state correctly

and letting that flow to the UI which is what react is intended to do changes to

the state will automatically update what the user sees we learned about conditional rendering how we can display

or not display certain parts of the web page based on conditions then we learned about forms and how react 19 enables an

entirely new approach to forms which is much more closely aligned with how the native web platform handles forms

and we took a chance to dabble just a little bit into different State Management strategies although State

Management is a rabbit hole that would probably require an entire course of its own then we had a lot of fun building

our meme generator and learning about side effects in react we began the section by talking about controlled

components which are essentially the way that react has approached dealing with forms all the way up until very recently

at the time of this recording but there are scenarios where controlled components can still be useful in our

case we wanted to update our state so that the top text would reflect on every keystroke what the user was typing into

the input box then we talked a little bit about how react has a philosophical basis in functional programming we

touched on the concepts of immutability in react and how our components shouldn't affect any outside systems

from themselves however the purpose of the side effect section is to learn how we can use an escape hatch from that

functional programming Paradigm when we absolutely need to and the way that we did this in our meme generator project

was to fetch some data as soon as the component loaded having a so-called escape hatch which gives us a chance to

safely handle side effects whenever they're absolutely necessary turns out not only to be a really important thing

in react but also one of the more misunderstood aspects of react then we got to the place where the rubber met

the road and that was in our Capstone projects we built two back-to-back games that were both really fun to build and

legitimately are fun to play hopefully looking back at all of these sections gives you a really strong sense of

appreciation as to how much time and effort you put into this course this would be a perfect opportunity for you

to head to the today I did channel on the scrimba Discord server and post a message thereare I say brag about this

tremendous accomplishment now I don't want to just leave you hanging at the end of this course so I wanted to give

you some ideas of what you could be working on next naturally I'd first like to put in a plug for my Advanced react

course here on scrimba the advanced react course is the progression from where we left off at the end of this

course in that course we dive deep into reusability in react and learn a bunch of new ways that we can turn our

reusable components into even more reusable components we learn how to build single page applications using the

react router library and we learn all about performance in react and how we can improve the performance of our react

apps another really important topic you could move on to if you haven't already learned it is typescript and good news I

also have a typescript course here on scrimba and it is is completely free I already mentioned react router but you

could focus specifically on learning the react router package at the time of recording react router is about to

release version 7 which is a completely new version of react router if you're looking to go more into a fullstack

realm nextjs and remix are awesome Frameworks that you can use to be building not only the front ends like

we've learned here in react but also the back ends so you can handle server interactions data caching cookies and

all of that if you are interested in backend you could go the direct backend route by learning no. JS with or without

Express all to help you build rest apis that your front-end react apps can consume and last but certainly not least

you could learn about deployment and how you can get your apps live on the web for your friends family and potential

future employers to check out my name is Bob s it has been my absolute pleasure to teach this course and guide you

through learning react my username pretty much everywhere on the web is Bob zero although these days I do tend to be

most active on X if if you click my username here it will take you to my profile I would certainly appreciate a

follow and folks that's all I have left to say except for congratulations on completing this learn react

[Music]

course hi I'm Tom from scrimba and in this section I'm going to take you through a couple of really useful VSS

code and Chrome browser extensions which you going to make your life as a react developer just a little bit easier as we

look at these extensions we're going to be working on this layout this is actually a screenshot right here so the

company is urban nest and this is the dashboard and on the dashboard we've got

four product cards and four user detail cards these contain dashboard type

activities like changing billing address or changing password now if we have a close look at

this you can see that we've got the username right here in the header also here in the dashboard title we're using

it again down here and you might also notice that we've got the location here

and that is going to affect which currency symbol we use and we've also got the user's email address in this

card right here so you're starting to get a feel hopefully for the way that props are used in this project now at

the moment we're working inside scrimber and I've already written some of the code let's just open up the mini browser

and see where we are so we've got a header and we've got a footer but we haven't got any of that content in the

middle and the reason for that is that we've got this dashboard component but it's completely empty so what we're

going to work on is getting this dashboard component sorted out using some browser extensions and to do that I

want to move everything over to vs

code really easy to do in scrimba I just click on settings download zip

that's downloaded a file and there we are we've already unzipped the file and

I'm just going to change this name to something more useful and I'll call it Urban

nest and now let's head over to vs code and open up this

folder so it was in downloads Urban Nest okay we've got all of our code here and

we can just follow the instructions inside readme.md to start the server so

we just need to do npm install and npm start let's open up a new instance of the terminal so first npm

install and that will bring in all of our

packages and then mpm start to start the server and then we

can just click on this link and there we are we are open in the browser and we can see we've got the header and the

footer okay let's just take a quick look at the code we've got so you understand how this layout works we start off with

app.js that is bringing in the header and the footer also in here we've got some State this is just set up with me

so we've got my name my email address my location and my age which is honestly

not entirely accurate and then we're just rendering out the header and the footer components passing in the props

that they need now there's nothing particularly strange going on the header is basically what you'd expect we've got

this nav element and then it's right here that we're using the username and the location and if we flip back to the

browser that's what you can see right here now down in the footer it says follow us on Instagram that's kind of

important if we go to the footer we've got this cheeky little bit of turnery

right here and I might just make that a little bit clearer by bringing it down onto a couple of lines so what's going

on here is that we're checking the age and if it's greater than 50 we're inviting them to follow us on Facebook

if if it's greater than 12 we're inviting them to follow us on Instagram and if not so they're under 12 we're

inviting them to follow us on Tik Tok and if we just head back to app.jsx I said that my age was

30 and that's right we're sing Instagram down here but we could change that and now it says Tik Tok okay let's

put that back now I can still show you the screenshot that we've got we should have it right here in images and that's

just going to show us what we're working towards so we've got these four product cards we've already got a component for

that right here product card. jsx we're reusing that four times and then down

here we've got the user detail cards again we've already got the react in there so we've got all of that code

available to us we just need to put it to good use in dashboard. jsx so the

first thing we need in dashboard is a functional component and that brings us

to our first

extension adding an extension in VSS code is really easy we just come to this icon right here or you can go to views

and extensions and then in here you can just search for the extension you want

you could just use a keyword and see what comes up I actually know the one I'm looking for but if I put in react

it's this first one which comes up is es7 plus react Redux react native

Snippets a really Snappy name all I need to do is Click

install a couple of things to notice on this page it's got nearly 13 million downloads which is great it's also well

reviewed and we could scroll down and see a bit of information about it and what features it's got but I'm just

going to give you a quick demonstration so let's just close that come to dashboard. jsx now I'm going to use a

key binding and in vs code there are loads of key bindings it just means key combinations that bring up some kind of

shortcut I'm going to use command shift and R but if you're on Windows you would actually use control out and R what that

does is it brings up this pretty fish looking menu of all of these options and

these are all code Snippets that this extension can give us so we've got stuff

here which is both for react for Redux and for react native some of it is Legacy so you'll likely never use it

some of it is is highly complex that you probably haven't come across as yet so

we've got for example hocc which stands for higher order components when we

click that it gives us the code we need but hey that's getting a little bit ahead of ourselves so again command

shift R and let's actually do something useful what we want to create here is a

functional component and so we can use this search functionality and I've put in functional

comp and then down here at the bottom creates a react functional component

with es7 module system that sounds good now we could just click on this right here but as we're going to be reusing

this a bit why don't we try and remember these four letters r f c e and that stands for react functional component

and then the E is for export we use that just by typing it right here in the editor react functional component export

hit enter and look there we are it's made a functional component for us and

it's actually taken the name dashboard from the name of the file so we don't have to so that is a nice really quick

way of setting up a functional component now I should give you a warning here that if you rely too much on these

automated code Snippets you might end up in a situation where you can't even write very basic react code like a

functional component you could end up looking pretty silly for example in an interview environment so do make sure

you actually know the code that you're generating automatically that is the best way to use a tool like this it

should just be for saving time okay let's quickly pop back to our screenshot and we can see that we need a

dashboard right here that's going to be inside an H1 so let's return that

here we also have the name of the user in this case Tom's dashboard so let's

take that in as props and I'm actually destructuring the

props right here so I'm using username inside the curly braces and then we can

use it right here we don't have to say props do username now the dashboard is going to have these four product cards

and we've got the data for the product cards right here in this data folder product

data.js now we also need to use product card. jsx so we've got some importing to

do and to be honest importing can be a your pain cuz you can end up with some really long relative paths because

you've got a heavily nested file structure it can be quite confusing and really difficult to debug so we're going

to use a really useful vs code extension which is going to help us with importing

now the snippet that we used before gives us this import statement that we don't actually need so let's delete

that and now let's investigate an extension which will help us with importing and the extension I'm looking

for is called Auto Import relative path this is the one

right here so let's click install and if we just clear the search box that will

take us back to our installed extensions what you'll notice is that we got two for the price of one we've got Auto

Import relative path and drag and drop import relative path and it's this one that I'm really interested in although

they come together so let's just go back to the files and what I'm going to do is

take this component that we want to import I'm going to drag it over now if I let it go now it's just going to open

the file but if I put it in position hold down the shift key and then release the mouse button there I get our full

import statement including the relative path this is a really short relative path so it wouldn't have been that much

trouble to write it ourselves but it's done it for us all we need to do is update the name and now we can use the

product card components but in order to use it effectively we need to get access to this data we're going to be mapping

over that data so let's import that next and again I'll just drag it and hold

down shift and drop it in so we want to import product

data from and then we've got the relative path this one a little bit more complicated because it is in a different

folder so that has saved us a little bit of cognitive load okay let's map over

this data so I'll set up a const right here inside the component and I'll call this const product

cards and then we'll take product

data call the map method and that will take in an arrow function with a single

parameter which will be a product and let's bring this down onto a

new line because we've got quite a lot to do here so for each product want to return to this array an instance of our

product card component and that is going to need some

props let's just have a quick look at the product card components so each one is an article and inside we've got a

card title an item name we've got a currency symbol which we're sorting out

right here based on the location we've got the price we've got the source for the image and the out text so we need to

bring in all all of this and let's actually just copy this

list and we need to remember when mapping over data and creating these components that each one needs to have a

key prop and the key prop if we look at the data is going to be this ID so it will

be available at product ID and actually most of these are going to come from

product location is the exception so let's just put product in these five

props and then location we are taking in in app.jsx so we've got it set right

here when eventually we add in the dashboard component we'll be passing it down so let's bring it in right here and

we should be done so let's just take our product cards and we're going to render

them down here in this return statement and they're going to live inside a section and that section needs

to have the CSS class name of product cards

container we've got an error here and that's because we're no longer rendering just one thing so we can just wrap

everything here in a

fragment and then we'll take the product cards and render them right there okay

let's save that and we'll head over to app.js and let's see if we can import

our dashboard and I'll do this one a different way I'm just going to write import and then when I put a d we see

dashboard if I click on it it does the rest for us so you've got two options the drag and drop we did before or just

writing import the name of the component and then let it do the rest okay down

between the header and the footer we can render the dashboard and we do need to pass in some

props we need the username and we also need the location

and we will actually be adding to that list later okay let's hit save we can open up

the mini browser and there we are we have got our four product cards so that is looking

pretty good now we're not done because go back to the screenshots well we need

the these user detail cards as well we've already got a component for that right here so all we need to do is bring

those in so back at the dashboard let's import user detail

cards and as they are actually the main content on that page they are going to

go in an HTML main element now we know we want four of them and things do get a

little bit strange here because we've got the email address and we've got the username so I haven't given us a data

file like we've got here to map over I don't think it's realistic that that information would be coming down from

some API or something like that so instead we're just going to render this one out four

times just to save you watching me do loads of typing I've actually got a text file right here with everything that we

need so I'm just going to copy that over and I'll just pass those in as

props and if we just check that component we can see that each one is expecting title and

text that should do the trick and just notice how we've used curly braces on two of these where we are including

props the user email and the usern name okay let's hit save and then when we

open up the browser we've got a bit of a problem so something has gone wrong let's just investigate what's going on

in this component so we have got the user detail card that should work just

fine but let's check the props that we've got coming in we've got username and location we haven't got user email

so let's add that to the list and let's just make sure in app.js that we're

passing that down to the dashboard we're not at this

moment let's save and try again and there we are look that is

working just

fine okay now we've got that working I want to show you a really cool Chrome extension let's come up here to our

Chrome settings go to extensions visit Chrome web store and again we'll search

on react and this is the one we want react developer tools we're going to add it to Chrome and now let's go back to

our layout and we'll just open up the dev tools and what we're going to get from this extension is a couple of

options right in here and actually we're not because I need to do a refresh and

now when I click on these two arrows right here we'll see two new options

components and profiler let's just click on components and we might just make ourselves a little bit more so we can

actually see our app so what have we got here we can

actually see the entire react tree we've got the app we've got the header and if

we click on one like I've just clicked on header we can see the props we've got we've got location UK username Tom if we

move on down to the dashboard we've got our individual product cards again we can see all of our props in here that is

pretty cool let's just head up to app here we've got the hooks so we've got all of our State let's just change one

of these so one of the benefits of this extension is that we can just make some changes and see rendering actually

happen live right here we've got the pound sign because I've put my location as the UK let's change that to

us and when I hit enter look what happens we get the dollar sign instead

and if I scroll right to the bottom it says here follow us on Instagram let's change my age to 130

and now it says follow us on Facebook take it down to age one follow us on Tik

Tok so you can really see how the state that you change is percolating down

through the apps as it's passed down as props so that can be really really useful for understanding how an app

works and of course for debugging now we had another option in here which was this one profiler and this is quite an

advanced one and you're probably not going to use this anytime soon but I want to show you quickly and just explain a bit about what it does what

happens is that we can click the blue button to record and now we can interact

with the app and so because this is basically a static site at the moment

I'm just going to flip back to the components and then let's make some changes let's put the age back to

30 and the country back to UK and now if we go back to Prof filer

I'll stop the recording and now we get some feedback on how fast our app

responded and exactly what happens so we can see what rendered and how long it

took and that can be really really useful for seeing reenders you might find in a complex app where something's

gone wrong that you're just rendering the same component thousands of times and it's causing performance issues well

this is the tool to help you debug that as I say it is quite an advanced topic not one you're going to use anytime soon

but good to know that it's there okay we're not quite done I want to go back to vs code and I just want to show you

two more

extensions let's go to the extensions Tab and here I'm going to search for

react tree and we come across react component tree let's install

that and I'm just going to close down that tab now down here we got a new option build tree let's click it and

look what we get here we get a similar view of the tree as we actually got in the dev tools this one is also pretty

useful so imagine you've got a massive app and you're looking at a component

well right now if we go to dashboard it's going to highlight it here and you can instantly see how it fits into the

tree again let's go back to the file explorer I'll take product card and now

when I to the tree and by the way we've got a new icon for it right here I can easily find it in this tree and just see

what the parent or sibling elements

are now this one I think is quite useful but there's actually a somewhat better

one I'm just going to put in here react tree all as one word this is the one I

want let's install that okay we get another option down here which is start tree let's click

that and I'm just going to close all of the open files and it's inviting us to select a

file let's click on that and we will go to downloads Urban Nest let's just take

the top of the funnel so app.jsx let's open that and look here we get a really

nice visualization of the app and we might just zoom out a little bit so we

can see it all so we've got app.jsx the three components it renders and the two

components we've just added to the dashboard if we click this P icon which is gray out in here that will actually

open up all of the props so you can see what's going on we've got the username

here and here for example we can see that we passed title and text down to user detail card you can also change the

direction it might be a bit easier to read left to right than top to bottom and also you can play around with the

layout which again in a big app might be useful just to be able to sort of spread things around and see what is where and

perhaps consider some changes consider making things a little bit more economical okay so we are done those are

some pretty useful extensions that you can use with vs code or with chrome to make your life as a react developer just

a little bit easier

## References


