# JavaScript (JS)

JavaScript statements are terminated with a semicolon, **`;`**. An individual statement will probably run without a semicolon but multiple statements will not.

## Information

### Comments

Single line comment.

``` js
// This comment is not displayed
```

Multiline comment.

``` js
/*
This comment is not displayed
This comment is not displayed
*/
```

## Mouse Over

This event is triggered when the mouse is over an element that has the `onmouseover` listener set.  It calls the associated JS function.

``` html
<p id="mouse" onmouseover="over()">Function not called</p>

<script>
    function over() {
        document.getElementById("mouse").innerHTML = "Mouse over";
        document.getElementById("mouse").style.color = "red";
    }
</script>
```

## Mouse Out

This event is triggered when the mouse is no longer over an element that has the `onmouseout` listener set.  It calls the associated JS function.

``` html
<p id="mouse" onmouseout="out()">Function not called</p>

<script>
    function out() {
        document.getElementById("mouse").innerHTML = "Mouse out";
        document.getElementById("mouse").style.color = "red";
    }
</script>
```

## This

Passing `this` as a parameter to the JS function allows the same function to be used with multiple elements.

``` html
<p onmouseover="change(this)">A paragraph.</p>
<p onmouseover="change(this)">Another paragraph.</p>

<script>
    function change(x) {
        x.style.color = "red";
        x.style.backgroundColor = "yellow";
    }
</script>
```
