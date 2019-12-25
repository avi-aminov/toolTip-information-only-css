# toolTip-information-only-css
toolTip information only css


<style>
  .css-tooltip{
	display: inline-block;
	position: relative;
	cursor: pointer;
}

.css-tooltip:hover::after,
.css-tooltip:hover::before{
	display:block;
	z-index: 99999;
}

.css-tooltip::before{
	content: '';
    width: 0px;
    height: 0px;
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
	border-bottom: 5px solid #2f2f2f;
	position: absolute;
	display:none;
}

.css-tooltip::after{
	content: attr(aria-label);
	width: 250px;
    padding: 10px;
    color: #fff;
    background: #202020;
	position: absolute;
	display:none;
	-webkit-box-shadow: 5px 5px 4px #aaa;
    -moz-box-shadow: 5px 5px 4px #aaa;
    box-shadow: 5px 5px 4px #aaa;
}

.small.css-tooltip::after{
	width: 150px;
}

.css-tooltip.bottom::before{
    left: 50%;
    top: calc(100% + 10px);
}

.css-tooltip.bottom::after{
    left: calc(50% - 125px);
    top: calc(100% + 15px);
}

.small.css-tooltip.bottom::after{
    left: calc(50% - 85px);
}

.css-tooltip.top::before{
	left: 50%;
    bottom: calc(100% + 10px);
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-top: 5px solid #2f2f2f;
    border-bottom: 0;
}

.css-tooltip.top::after{
    left: calc(50% - 125px);
    bottom: calc(100% + 15px);
	-webkit-box-shadow: 5px -5px 4px #aaa;
    -moz-box-shadow: 5px -5px 4px #aaa;
    box-shadow: 5px -5px 4px #aaa;
}

.small.css-tooltip.top::after{
	left: calc(50% - 85px);
}

.css-tooltip.left-top::before{
    right: calc(100% + 20px);
    top: 50%;
    border-top: 5px solid transparent;
    border-bottom: 5px solid transparent;
    border-left: 5px solid #2f2f2f;
    border-right: 0;
}

.css-tooltip.left-top::after{
    right: calc(100% + 25px);
    top: 0;
    -webkit-box-shadow: -5px -5px 4px #aaa;
    -moz-box-shadow: -5px -5px 4px #aaa;
    box-shadow: -5px -5px 4px #aaa;
}

.css-tooltip.right-top::before{
    left: calc(100% + 20px);
    top: 50%;
    border-top: 5px solid transparent;
    border-bottom: 5px solid transparent;
    border-right: 5px solid #2f2f2f;
    border-left: 0;
}

.css-tooltip.right-top::after{
	left: calc(100% + 25px);
    top: 0;
    -webkit-box-shadow: 5px 5px 4px #aaa;
    -moz-box-shadow: 5px 5px 4px #aaa;
    box-shadow: 5px 5px 4px #aaa;
}



  </style>

<span 
  class="css-tooltip right-top small" 
  aria-label="Lorem Ipsum is simindustry's standard dummy text ever since the 1500s,">
    Right Top Small
</span>

Example:
```html
<span 
  class="css-tooltip right-top small" 
  aria-label="Lorem Ipsum is simindustry's standard dummy text ever since the 1500s,">
    Right Top Small
</span>
```
