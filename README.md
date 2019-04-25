# Bisnode UI

This is a HTML and SCSS based technical test set by Bisnode. The aim of the test is to contribute to a CSS framework, making each component independent so components can be swapped or changed without effecting the rest of the framework.

This test was also completed with a double dash BEM methodology in mind.

[Link to live web version](https://daniel-cross.github.io/bisnode/)

# Buttons
![alt text](https://i.imgur.com/6ScFfCp.png "Bisnode buttons")

The buttons were designed inline with the specifications outlined in the docs. Each button (Primary and Secondary) has three different states: Active, Hover and Disabled.

The image above shows each button in all three states. Below is the HTML needed to replicate the buttons:

## Primary
```
<button class="btn__medium--primary">primary btn</button>
<button disabled class="btn__medium--primary">primary btn</button>
```
## Secondary
```
<button class="btn__medium--secondary">secondary btn</button>
<button disabled class="btn__medium--secondary">secondary btn</button>
```

Using the double dash BEM methodology, the buttons have a class of `btn` initially as `btn` is the component name, or block, then `__medium` is added as that is the size of the button, or element, and lastly `--primary` or `--secondary` is added as the styling option, or modifier.

This was designed with the purpose of making it easier to change or swap the size of the button at a later date without it effecting the codebase. For example `btn__large--primary` or `btn__small--secondary` could be used in the future and only affect the size of the button and it's font size.

# Cards

![alt text](https://i.imgur.com/5L7WI1e.png "Bisnode Cards")
![alt text](https://i.imgur.com/xDVAL1V.png "Bisnode Cards")


The cards were designed inline with the specifications outlined in the docs. There is one default card which contains two footer elements, a default card that contains either one or two buttons and a square care option that does not have a `border-radius`.

The image above shows the finished card components and below is the HTMl needed to replicate them:


## Default Card
```
<div class="card">
  <h4 class="card__title">Title</h4>
  <p class="card__text">Text</p>
  <div class="card__footer">
    <footer class="card__footer-left">Footer L</footer>
    <footer class="card__footer-right">Footer R</footer>
  </div>
</div>
```

## Default Card with Primary Button
```
<div class="card">
  <h4 class="card__title">Title</h4>
  <p class="card__text">Content</p>
  <div class="card__footer--btn">
    <button class="btn__medium--primary">primary btn</button>
  </div>
</div>
```

## Default Card with Primary and Secondary Button
```
<div class="card">
  <h4 class="card__title">Title</h4>
  <p class="card__text">Content</p>
  <div class="card__footer--btn">
    <button class="btn__medium--secondary">secondary btn</button>
    <button class="btn__medium--primary">primary btn</button>
  </div>
</div>
```

## Square Card
```
<div class="card--square">
  <h4 class="card__title">Title</h4>
  <p class="card__text">Content</p>
  <div class="card__footer">
    <footer class="card__footer-left">Footer L</footer>
    <footer class="card__footer-right">Footer R</footer>
  </div>
</div>
```

As you can see, adding the buttons to the card is as simple as adding `--btn` to the footer class contained in the card and then passing in the previously defined button classes.

Some small styling changes were made to ensure it is easy to see some of the smaller details, such as the body background colour changed to `#eee` from `#fff`.

**built using**
* HTML
* SASS/SCSS

**Running in browser**
* download and unzip the files
* navigate to the downloaded folder and open
* find and open the file named *index.html* with a browser of your choice, preferably Chrome

Please be mindful that you may run into issues if you're using <IE9.

**Author**

Daniel Cross

