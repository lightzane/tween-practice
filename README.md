# Tween Practice
Just practicing ```TweenMax.min.js```. [See Demo](https://timelights.github.io/tween-practice)

```html
<h1>Headers Are Cool</h1>
<ul>
	<li>
		<h3>Lorem ipsum</h3>
		<samp>Dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua.</samp>
	</li>
	<li>
		<h3>Lorem ipsum</h3>
		<samp>Dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua.</samp>
	</li>
</ul><br>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
```

### JavaScript
```javascript
// define tweens
var t_showHeader = TweenMax.from('h1', 0.5, {opacity:0,y:'100px'})
var t_showDl = TweenMax.staggerFrom('li', 0.5, {opacity:0,x:'100px'}, 0.3)
var t_showP = TweenMax.staggerFrom('p', 0.5, {opacity:0,y:'-100px'},0.3)

// set default ease
TweenLite.defaultEase = Back.easeOut

// Create timeline to make order amongst the tweens
var tl = new TimelineMax({yoyo:true,repeatDelay:1})
tl.add(t_showHeader)
tl.add(t_showDl)
tl.add(t_showP)
```