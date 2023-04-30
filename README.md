## 401.- 50 Projects 50 Days - Expanding Cards

### What was the project about?

The project is part of the 50 Projects in 50 Days with Brad Travesy via Udemy. The course is a code-a-long to further cement skills used within HTML, CSS, and Vanilla JavaScript.

This particular project was to create expanding cards. The cards themselves start of small, but once clicked, each particular card will expand.

[Expanding Cards](https://totallysly.github.io/401.-50PROJECTS-50DAYS--expanding-cards--html-css-js/)

### What did I learn?

I feel pretty comfortable with HTML and CSS. I have just started to touch the surface with vanila JavaScript. I understand what manipulating the DOM is, and the theory of how to do this, but I have not had a lot of practice. This first project was a great refresher in entering DOM manipulation again.

#### Manipulating the DOM

`const panels = document.querySelectorAll('.panel')`

Using *querySelectorAll* puts all HTML elements with the class name of '*.panel*' within a **node** list. A **node** list is similar to an array, therefore you can target an individual **node**. Therefore `panel[2]` will target the **THIRD** panel.



    panels.forEach((panel) => {
	    panel.addEventListener('click', () => {
		    removeActiveClasses()
		    panel.classList.add('active')
	    })
    } )


    function removeActiveClasses() {
	    panels.forEach((panel) => {
		    panel.classList.remove('active')
	    })
    }
    
The above code was simple enough to refresh my memory in regards to basic DOM manipulation. 

Using a *forEach* loop, meaning that 

*forEach* *panel* within the node list of *PANELS*, we want to add an *eventListener* which is a *click* of the mouse.
 
 *forEach* panel that is clicked, add the class list of 'active'.
 
 We also want remove the *classList* of '*active*' from the other panel when clicked. So a *function* is created. The *function* needs to be called upon the *eventListener* of click. So it is placed before we add the *classList*.

 Within the *function* we require another *forEach* loop. But this time we want to **REMOVE** the *classList* of *'active*'.


 #### CSS

    .panel{
	    ***************;
		***************;
		flex: 0.5;
		***************;
		transition: flex 0.7s ease-in;
    }

I have never used *flex* as a way of increasing the width of an element before and it feels like a clever way of adjusting the width without setting the width. I believe this should, therefore, make responsive design a lot easier.

Even though I have used *transitions* before, this was the first time that it had clicked that you can set it for any stated property.

    .panel.active{
	    flex: 5;
    }

To further highlight the useage of *flex*, using it on any *active* class which will then expand that particular panel to 5. (The *active* class is added using JavaScript, which is detailed above).

    .panel:nth-of-type(4),
    .panel:nth-of-type(5) {
	    display: none;
    }

I have not used *:nth-of-type( )* that much before. I thought that this was a great way to remove certain cards and something I will take on board in the future for other use.



> Written with [StackEdit](https://stackedit.io/).
