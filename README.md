## Müvie Haus

![](https://media.giphy.com/media/56vLtntOmVfvG/giphy.gif)

Our new client, Gerard von Schtieffel, owns an independent theatre that plays only the best movies across time and genres. He's hired us because in this new-fangled age of technology, he needs a new edge in order to compete with the Megaplexes of the world (Megaplexi? Megapli?).

That edge? [**AJAX**. Click here for some documentation of AJAX GET with jQuery!](https://api.jquery.com/jquery.get/). [More documentation for jQuery AJAX in general](http://api.jquery.com/jquery.ajax/). Be sure to look at this before you're **DONE** with the homework winkwink

Gerard wants to be able to manage his new website on his own. He'll be able to search for a movie and add it to his list of movies currently playing at the Müvie Haus.

To do this, we'll be getting data from the Open Movie Database (OMDB) using AJAX.

This exercise will help introduce students into using AJAX, and give a **VERY SOFT** introduction into APIs. We'll use the data AJAX returns to dynamically change the page with DOM manipulation and play with Skeleton styling some more!

## Set Up

Starter code has been provided. Work in the `starter.js` file, and make edits to `index.html` and `style.css` as necessary.

## Completion

There are four functions in the JavaScript. Aim to complete all four. There are bonuses to tackle afterwards!

## Assignment

There are four functions

* getData should take an input of a movieTitle, and **RETURN** an **AJAX GET** to `http://www.omdbapi.com/?t=**MOVIE-TITLE**&r=json`  
    Try GETting that URL in Postman and seeing what the data it returns looks like.

* addAJAXFunction is a listener on the submit button. This function uses the **movie input element's value** (which should be a movie title!) and **invokes getData** with the movie title. When getData is **DONE**, it should invoke handleResponse

* skeletonizeMovie takes two inputs, `name` and `imagePath`, and creates a series of elements that fit into the skeleton scheme of the HTML. There is already an example of what this looks like in the HTML! This function does not append to the body, but **returns** the overall parent element

* handleResponse should take an input of data, parse through it to isolate the movie name and the image path, and invokes skeletonizeMovie to create an element. **Append** that element in the appropriate spot.

## Bonus

* What happens if you search for something and it doesn't return a legitimate movie? It will still append to the page, and mess up the styling of subsequent movies. Add a conditional so that only searches with good results will append movie information to the page

* Skeleton doesn't quite work perfectly once we surpass twelve columns in a row. We like structure, so add a conditional that will create a new div row, append that to the right element, and then append the new movie when appropriate
