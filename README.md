# fullpage-canvas
This is an HTML5-based app created with a simple plugin, fullpage.js, and its associated library jQuery and jQuery-ui, and designed to be reused in multi-purposes. 

Before you set off creating all the pages and their child components, you need to initiate an instance object with H5 function sealed with such methods, such as:

var h5 = new H5();

Then embark on creating however many pages with customized and animated components with: 

h5.addPage().addComponent();

The addPage() function takes 0~1 parameter that defines the page's topic/theme, such as 'cover-page', 'contact-page', etc., which in turn lead to adding 'h5_page_cover-page' and 'h5_page_contact-page' class names to the named page's div tag, while the addComponent() function takes two parameters, first one similar to that the addPage() function takes that defines the component's usage, and the second one an object in the following format: 

<pre>
{
  text: '数据汇总',
  type: 'radar',
  data: [['A', 0.5, '#fff'], ['B', 0.3, '#eee'], ['C', 0.2, '#f00']],
  width: 200,
  height: 200,
  bg: './imgs/1.png',
  css: {
    opacity: 0,
    bottom: 0
  },
  animateIn: {
    opacity: 1,
    bottom: 100
  },
  animateOut: {
    opacity: 0,
    bottom: 0
  },
  delay: 1000,
  center: true
}
</pre>

The above object is configurable and writable, with <i>text</i> serving as the text for the component, <i>type</i> defining what function to be called to create the component, <i>data</i> telling canvas how many pieces of data to be created and how they should be displayed, <i>width</i> and <i>height</i> sizing the component, <i>css</i>, <i>animateIn</i>, <i>animateOut</i>, together with <i>delay</i> setting up the component's styles and its debuting animations, and <i>center: true</i> placing the component in the middle horrizontally.

You may call this .addPage().addComponent() functions as many times as you like to create multiple pages and related components.

