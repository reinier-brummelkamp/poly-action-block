# poly-action-block

The `poly-action-block` provides a carousel like button that animates actions that will execute when clicked. 
Execution can be in the form of navigating or raising a JavaScript event.  


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Data structure

The following is sample json shows properties for each action. All properties are optional, e.g. if you do 
not want header or footer elements, simply omit all properties related to headers or footers
 
```
{
    "actions": [
        {
            //Action block anchor and event configuration
            "href": "http://www.domain.com", //href for action, default null
            "hrefNewWindow" : false, //Open href in new window, default false
            "eventName" : "click", //JavaScript event name, default null
            "eventData" : { "user" : "me"}, //Associated JavaScript event data, default null 
            "duration" : 1000, //Duration to show this action in milliseconds, default 5000
            "entryAnimation": "slide-from-right-animation", //polymer animation name to use when showing this action
            "exitAnimation": "slide-left-animation", //polymer animation name to use when hiding this action 
            
            //Action block style
            "actionItemCssClass" : "action-item", //Css class for the action item, default null
            "actionItemInlineStyle" : "property: value;", //Inline css style for the action item, default null 
            
            //Action block slide header configuration
            "headerImgSrc": "http://lorempixel.com/16/16/", //Image src for header img, default null
            "headerIronIconName": "header-iron-icon-name", //Iron icon name for header iron-icon, default null
            "headerLabel": "Header label", //Header label, default null
            
            //Action block slide header styles
            "headerImgCssClass" : "header-image", //Css class for the header img, default null 
            "headerImgInlineStyle" : "property: value;", //Inline css style for the header img, default null
            "headerIronIconCssClass" : "header-iron-icon", //Css class for the header iron-icon, default null
            "headerIronIconInlineStyle" : "property: value;", //Inline css style for the header iron-icon, default null
            "headerLabelCssClass" : "header-label", //Css class for the header label, default null
            "headerLabelInlineStyle" : "property: value;", //Inline css style for the header label, default null
            
            //Action block slide body configuration
            "imgSrc": "http://lorempixel.com/64/64/", //Image src for the action item img, default null
            "ironIconName": "icon-icon-name", //Iron icon name for the action item iron-icon, default null
            "label": "Label", //Action item label, default null
            
            //Action block slide body styles
            "imgCssClass" : "image", //Css class for the action item img, default null
            "imgInlineStyle" : "property: value;", //Inline css style for the action item img, default null
            "ironIconCssClass" : "iron-icon", //Css class for the action item iron-icon, default null
            "ironIconInlineStyle" : "property: value;", //Inline css style for the action item iron-icon, default null
            "labelCssClass" : "label", //Css class for the action item label, default null
            "labelInlineStyle" : "property: value;", //Inline css style for the action item label, default null
            
            //Action block slide footer configuration
            "footerImgSrc": "http://lorempixel.com/16/16/", //Image src for footer img, default null
            "footerIronIconName": "footer-iron-icon-name", //Iron icon name for footer iron-icon, default null
            "footerLabel": "Footer label", //Footer label, default null
            
            //Action block slide footer styles
            "footerImgCssClass" : "footer-image",//Css class for the footer img, default null 
            "footerImgInlineStyle" : "property: value;", //Inline css style for the footer img, default null
            "footerIronIconCssClass" : "footer-iron-icon",//Css class for the footer iron-icon, default null
            "footerIronIconInlineStyle" : "property: value;", //Inline css style for the footer iron-icon, default null
            "footerLabelCssClass" : "footer-label", //Css class for the footer label, default null
            "footerLabelInlineStyle" : "property: value;" //Inline css style for the footer label, default null
        }
    ]
}
```

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/poly-action-block/`, where `poly-action-block` is the name of the directory containing it.


## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/poly-action-block/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.
