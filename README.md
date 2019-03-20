# JS Color Picker
Simple JavaScript colorpicker which supports transparency and gradient. 

Check the Demo: https://codepen.io/komarovdesign/pen/moGNpJ

This is small (no external images or dependencies) and working solution if you need color picker right now right here :)

## Basic Usage
Each text input with <code>.clpi</code> class will be converted into color picker. If you need to have a gradient switcher add <code>.clpi-gradient</code> class

<pre><code>&lt;!-- Simple ColorPicker  --&gt;
&lt;input type=&quot;text&quot; class=&quot;clpi&quot;&gt;

&lt;!-- Gradient ColorPicker  --&gt;
&lt;input type=&quot;text&quot; class=&quot;clpi clpi-gradient&quot;&gt;
</code></pre>

## Usage
Colorpicker works with global events passing the currently triggered input.
#### If you need to reinit new colorpicker inputs.
<pre><code>colorPicker.initAll()</code></pre>

#### When color picker changed
<pre><code>window.addEventListener('colorPickerChange', function (data) {
    let i = data.detail.el;
    document.body.style.background = i.value;
});</code></pre>

#### When color picker is changing
<pre><code>window.addEventListener('colorPickerTick', function (data) {
    let i = data.detail.el;
    document.body.style.background = i.value;
});</code></pre>
