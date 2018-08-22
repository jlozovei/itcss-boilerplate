# ITCSS boilerplate

A simple ITCSS boilerplate to help you organize and mantain a clean, DRY and awesome CSS code.


## ITCSS

ITCSS is an awesome CSS methodology that consists, literally, in an inverted triangle within CSS. The highest the specificity of your code, the triangle gets lower.  
Within ITCSS, you have a specific structure to follow:

- Settings
- Tools
- Generic
- Base
- Objects
- Components
- Trumps


## Structure

To keep it simple, within this boilerplate I've merged some steps of ITCSS - `Base` + `Objects` and also racked off `Trumps`.
So, this is our scenario:


#### Settings

Everything within `settings` will not generate CSS code - this part is dedicated to organize your colors, base sizes and random things that can be stored within a variable and will be used along the entire project.  

```scss
$base_blue: #007bff;
$base_green: #218838;
```


#### Tools

Here we'll have a little bit of code. In general, I like to keep animations, keyframes, mixins and related stuff within `tools`. Also, it will be a nice place for you to store `extends` rules.  

```css
@keyframes fadeIn{
    0%{ opacity: 0; }
    100%{ opacity: 1; }
}
```


#### Generic

From this point, we'll start to write down our `real CSS`. Here is a good place to keep your `reset` and also  some generic rules - these rules are applied with the `Tags Selectors`, like:

```css
ul{
    padding-left: 16px;
    margin-bottom: 24px;
}
```

Beyond resets and generic rules, here I like to put some general rules, like classes applied to `body`:  

```css
body.fixed{
    overflow: hidden;
}
```

#### Objects

Following the OOCSS methodology, here we'll have small pieces of our entire `components` - we can also define as patterns that will be repeated within all the project.  
A good example we can use here is the `.button` rule:

```css
.button{
    display: inline-block;
    position: relative;
    text-align: center;
    cursor: pointer;
    border: 1px solid transparent;
}
```

We defined above a basic structure/appearance for `.button`elements; but, we haven't defined it in its whole.


#### Components

The largest part and the most specific part of our CSS code, here you will have all sort of components you can imagine - `header`, `footer`, `menu`, `sidebar`, and maybe also `buttons` again:

```css
/* wrapper element for buttons */
.button__wrapper{
    text-align: center;
    max-width: 80%;
    margin: 0 auto;
}

/* primary button */
.button.button--primary{
    background-color: #007bff;
    border-color: #007bff;
    color: #fff;
}
```


### index.css

Our main CSS file, it contains only `@import` rules.  

For a long time I used this template a lot with [Sass](https://sass-lang.com/) and now I'm using with [PostCSS](https://postcss.org/). Also, I use [gulp](http://gulpjs.com/) to create the processing and minifying tasks.


## Cool References and Further Reading

- [@ahmadajmi/awesome-itcss](https://github.com/ahmadajmi/awesome-itcss)
- [An Introduction to OOCSS - Smashing Magazine](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)

