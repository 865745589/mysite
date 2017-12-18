(function e(b,g,d){function c(m,j){if(!g[m]){if(!b[m]){var i=typeof require=="function"&&require;
if(!j&&i){return i(m,!0)}if(a){return a(m,!0)}var k=new Error("Cannot find module '"+m+"'");
throw k.code="MODULE_NOT_FOUND",k}var h=g[m]={exports:{}};b[m][0].call(h.exports,function(l){var o=b[m][1][l];
return c(o?o:l)},h,h.exports,e,b,g,d)}return g[m].exports}var a=typeof require=="function"&&require;
for(var f=0;f<d.length;f++){c(d[f])}return c})({1:[function(b,c,a){c.exports={log:b("./ac-console/log")}
},{"./ac-console/log":2}],2:[function(d,f,b){var a="f7c9180f-5c45-47b4-8de4-428015f096c0";
var c=!!(function(){try{return window.localStorage.getItem(a)}catch(h){}}());f.exports=function g(){if(window.console&&typeof console.log!=="undefined"&&c){console.log.apply(console,Array.prototype.slice.call(arguments,0))
}}},{}],3:[function(c,d,b){var g=c("./utils/addEventListener");var a=c("./shared/getEventType");
d.exports=function f(k,i,j,h){i=a(k,i);return g(k,i,j,h)}},{"./shared/getEventType":10,"./utils/addEventListener":11}],4:[function(d,b,f){var g=d("./utils/eventTypeAvailable");
var j=d("./shared/camelCasedEventTypes");var c=d("./shared/windowFallbackEventTypes");
var h=d("./shared/prefixHelper");var a={};b.exports=function i(m,l){var n;var o;
var k;l=l||"div";m=m.toLowerCase();if(!(l in a)){a[l]={}}o=a[l];if(m in o){return o[m]
}if(g(m,l)){return o[m]=m}if(m in j){for(k=0;k<j[m].length;k++){n=j[m][k];if(g(n.toLowerCase(),l)){return o[m]=n
}}}for(k=0;k<h.evt.length;k++){n=h.evt[k]+m;if(g(n,l)){h.reduce(k);return o[m]=n
}}if(l!=="window"&&c.indexOf(m)){return o[m]=i(m,"window")}return o[m]=false}},{"./shared/camelCasedEventTypes":5,"./shared/prefixHelper":6,"./shared/windowFallbackEventTypes":7,"./utils/eventTypeAvailable":8}],5:[function(b,c,a){c.exports={transitionend:["webkitTransitionEnd","MSTransitionEnd"],animationstart:["webkitAnimationStart","MSAnimationStart"],animationend:["webkitAnimationEnd","MSAnimationEnd"],animationiteration:["webkitAnimationIteration","MSAnimationIteration"],fullscreenchange:["MSFullscreenChange"],fullscreenerror:["MSFullscreenError"]}
},{}],6:[function(b,d,a){var i=["-webkit-","-moz-","-ms-"];var f=["Webkit","Moz","ms"];
var h=["webkit","moz","ms"];var c=function(){this.initialize()};var g=c.prototype;
g.initialize=function(){this.reduced=false;this.css=i;this.dom=f;this.evt=h};g.reduce=function(j){if(!this.reduced){this.reduced=true;
this.css=[this.css[j]];this.dom=[this.dom[j]];this.evt=[this.evt[j]]}};d.exports=new c()
},{}],7:[function(b,c,a){c.exports=["transitionend","animationstart","animationend","animationiteration"]
},{}],8:[function(c,f,b){var a={window:window,document:document};f.exports=function d(i,g){var h;
i="on"+i;if(!(g in a)){a[g]=document.createElement(g)}h=a[g];if(i in h){return true
}if("setAttribute" in h){h.setAttribute(i,"return;");return(typeof h[i]==="function")
}return false}},{}],9:[function(d,f,c){var b=d("./utils/removeEventListener");var a=d("./shared/getEventType");
f.exports=function g(k,i,j,h){i=a(k,i);return b(k,i,j,h)}},{"./shared/getEventType":10,"./utils/removeEventListener":12}],10:[function(c,f,b){var d=c("@marcom/ac-prefixer/getEventType");
f.exports=function a(j,i){var h;var g;if("tagName" in j){h=j.tagName}else{if(j===window){h="window"
}else{h="document"}}g=d(i,h);if(g){return g}return i}},{"@marcom/ac-prefixer/getEventType":4}],11:[function(b,c,a){c.exports=function d(i,g,h,f){if(i.addEventListener){i.addEventListener(g,h,!!f)
}else{i.attachEvent("on"+g,h)}return i}},{}],12:[function(b,c,a){c.exports=function d(i,g,h,f){if(i.removeEventListener){i.removeEventListener(g,h,!!f)
}else{i.detachEvent("on"+g,h)}return i}},{}],13:[function(b,c,a){c.exports=8},{}],14:[function(b,c,a){c.exports=11
},{}],15:[function(b,c,a){c.exports=9},{}],16:[function(b,c,a){c.exports=1},{}],17:[function(b,c,a){c.exports=3
},{}],18:[function(b,c,a){var d=b("../isNode");c.exports=function f(h,g){if(!d(h)){return false
}if(typeof g==="number"){return(h.nodeType===g)}return(g.indexOf(h.nodeType)!==-1)
}},{"../isNode":22}],19:[function(g,d,j){var b=g("./isNodeType");var c=g("../COMMENT_NODE");
var k=g("../DOCUMENT_FRAGMENT_NODE");var i=g("../ELEMENT_NODE");var h=g("../TEXT_NODE");
var m=[i,h,c,k];var f=" must be an Element, TextNode, Comment, or Document Fragment";
var p=[i,h,c];var l=" must be an Element, TextNode, or Comment";var n=[i,k];var o=" must be an Element, or Document Fragment";
var a=" must have a parentNode";d.exports={parentNode:function(q,t,s,r){r=r||"target";
if((q||t)&&!b(q,n)){throw new TypeError(s+": "+r+o)}},childNode:function(q,t,s,r){r=r||"target";
if(!q&&!t){return}if(!b(q,p)){throw new TypeError(s+": "+r+l)}},insertNode:function(q,t,s,r){r=r||"node";
if(!q&&!t){return}if(!b(q,m)){throw new TypeError(s+": "+r+f)}},hasParentNode:function(q,s,r){r=r||"target";
if(!q.parentNode){throw new TypeError(s+": "+r+a)}}}},{"../COMMENT_NODE":13,"../DOCUMENT_FRAGMENT_NODE":14,"../ELEMENT_NODE":16,"../TEXT_NODE":17,"./isNodeType":18}],20:[function(c,d,b){var g=c("./internal/isNodeType");
var a=c("./DOCUMENT_FRAGMENT_NODE");d.exports=function f(h){return g(h,a)}},{"./DOCUMENT_FRAGMENT_NODE":14,"./internal/isNodeType":18}],21:[function(c,d,b){var g=c("./internal/isNodeType");
var a=c("./ELEMENT_NODE");d.exports=function f(h){return g(h,a)}},{"./ELEMENT_NODE":16,"./internal/isNodeType":18}],22:[function(b,c,a){c.exports=function d(f){return !!(f&&f.nodeType)
}},{}],23:[function(c,d,b){var f=c("./internal/validate");d.exports=function a(g){f.childNode(g,true,"remove");
if(!g.parentNode){return g}return g.parentNode.removeChild(g)}},{"./internal/validate":19}],24:[function(g,c,i){g("@marcom/ac-polyfills/Array/prototype.indexOf");
var o=g("@marcom/ac-dom-nodes/isNode");var b=g("@marcom/ac-dom-nodes/COMMENT_NODE");
var k=g("@marcom/ac-dom-nodes/DOCUMENT_FRAGMENT_NODE");var j=g("@marcom/ac-dom-nodes/DOCUMENT_NODE");
var h=g("@marcom/ac-dom-nodes/ELEMENT_NODE");var f=g("@marcom/ac-dom-nodes/TEXT_NODE");
var a=function(r,q){if(!o(r)){return false}if(typeof q==="number"){return(r.nodeType===q)
}return(q.indexOf(r.nodeType)!==-1)};var m=[h,j,k];var n=" must be an Element, Document, or Document Fragment";
var p=[h,f,b];var l=" must be an Element, TextNode, or Comment";var d=" must be a string";
c.exports={parentNode:function(q,t,s,r){r=r||"node";if((q||t)&&!a(q,m)){throw new TypeError(s+": "+r+n)
}},childNode:function(q,t,s,r){r=r||"node";if(!q&&!t){return}if(!a(q,p)){throw new TypeError(s+": "+r+l)
}},selector:function(q,t,s,r){r=r||"selector";if((q||t)&&typeof q!=="string"){throw new TypeError(s+": "+r+d)
}}}},{"@marcom/ac-dom-nodes/COMMENT_NODE":13,"@marcom/ac-dom-nodes/DOCUMENT_FRAGMENT_NODE":14,"@marcom/ac-dom-nodes/DOCUMENT_NODE":15,"@marcom/ac-dom-nodes/ELEMENT_NODE":16,"@marcom/ac-dom-nodes/TEXT_NODE":17,"@marcom/ac-dom-nodes/isNode":22,"@marcom/ac-polyfills/Array/prototype.indexOf":102}],25:[function(b,c,a){b("@marcom/ac-polyfills/Array/prototype.slice");
var h=b("./internal/validate");var g=b("./shims/querySelectorAll");var f=("querySelectorAll" in document);
c.exports=function d(i,j){j=j||document;h.parentNode(j,true,"querySelectorAll","context");
h.selector(i,true,"querySelectorAll");if(!f){return g(i,j)}return Array.prototype.slice.call(j.querySelectorAll(i))
}},{"./internal/validate":24,"./shims/querySelectorAll":26,"@marcom/ac-polyfills/Array/prototype.slice":103}],26:[function(c,b,f){c("@marcom/ac-polyfills/Array/prototype.indexOf");
var j=c("@marcom/ac-dom-nodes/isElement");var h=c("@marcom/ac-dom-nodes/isDocumentFragment");
var k=c("@marcom/ac-dom-nodes/remove");var d="_ac_qsa_";var i=function(n,l){var m;
if(l===document){return true}m=n;while((m=m.parentNode)&&j(m)){if(m===l){return true
}}return false};var g=function(l){if("recalc" in l){l.recalc(false)}else{document.recalc(false)
}window.scrollBy(0,0)};b.exports=function a(l,n){var p=document.createElement("style");
var q=d+(Math.random()+"").slice(-6);var m=[];var o;n=n||document;document[q]=[];
if(h(n)){n.appendChild(p)}else{document.documentElement.firstChild.appendChild(p)
}p.styleSheet.cssText="*{display:recalc;}"+l+'{ac-qsa:expression(document["'+q+'"] && document["'+q+'"].push(this));}';
g(n);while(document[q].length){o=document[q].shift();o.style.removeAttribute("ac-qsa");
if(m.indexOf(o)===-1&&i(o,n)){m.push(o)}}document[q]=null;k(p);g(n);return m}},{"@marcom/ac-dom-nodes/isDocumentFragment":20,"@marcom/ac-dom-nodes/isElement":21,"@marcom/ac-dom-nodes/remove":23,"@marcom/ac-polyfills/Array/prototype.indexOf":102}],27:[function(b,d,a){var f=function(){};
d.exports=function c(g){if(arguments.length>1){throw new Error("Second argument not supported")
}if(g===null||typeof g!=="object"){throw new TypeError("Object prototype may only be an Object.")
}if(typeof Object.create==="function"){return Object.create(g)}else{f.prototype=g;
return new f()}}},{}],28:[function(c,d,b){c("@marcom/ac-polyfills/Array/prototype.forEach");
var a=Object.prototype.hasOwnProperty;d.exports=function f(){var h;var g;if(arguments.length<2){h=[{},arguments[0]]
}else{h=[].slice.call(arguments)}g=h.shift();h.forEach(function(j){if(j!=null){for(var i in j){if(a.call(j,i)){g[i]=j[i]
}}}});return g}},{"@marcom/ac-polyfills/Array/prototype.forEach":101}],29:[function(f,d,h){var o;
var n=f("@marcom/ac-object/extend");var j=f("@marcom/ac-object/create");var p=f("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var c=f("@marcom/ac-dom-traversal/querySelectorAll");var l=f("@marcom/ac-dom-events/addEventListener");
var b=f("@marcom/ac-dom-events/removeEventListener");var a=f("@marcom/ac-console");
try{o=f("@marcom/ac-analytics")}catch(m){a.log(m.message)}var g={dataAttribute:"analytics-share",interactionEvents:["click"],autoEnable:true};
var q=function(r){r=r||{};this.options=n(g,r);p.call(this);this.elements=[];this.eventObserver=null;
this.publishShareClick=this.publishShareClick.bind(this);if(this.options.autoEnable){this.enable()
}};var k=p.prototype;var i=q.prototype=j(k);i.enable=function(){if(!o){return false
}this._createObserver();this.bindEventListener()};i.disable=function(){if(!o){return false
}this.unbindEventListener()};i.bindEventListener=function(){var s=0;this.elements=this.populateElements();
s=this.elements.length;for(var r=0;r<s;r++){l(this.elements[r],"click",this.publishShareClick)
}};i.unbindEventListener=function(){var s=(this.elements&&this.elements.length?this.elements.length:0);
for(var r=0;r<s;r++){b(this.elements[r],"click",this.publishShareClick)}};i.populateElements=function(){return c("[data-"+this.options.dataAttribute+"]",(this.options.context||document))
};i.publishShareClick=function(s){var t=s.currentTarget;var r=this.parseDataAttribute(t.getAttribute("data-"+this.options.dataAttribute));
if(typeof r==="object"){if(!r.title){console.log("data-"+this.options.dataAttribute+" attribute must have a `title` property");
return false}this.trigger("click",r)}};i.parseDataAttribute=function(t){var r={};
try{r=JSON.parse(t)}catch(s){console.log("data-"+this.options.dataAttribute+" must be a valid JSON string")
}return r};i.destroy=function(){this.disable();this.elements=[];this.eventObserver=null;
this.publishShareClick=null;this.options=null};i._createObserver=function(){if(!o||!o.observer||!o.observer.Event){return false
}this.eventObserver=new o.observer.Event(this,this.options)};d.exports=q},{"@marcom/ac-analytics":"@marcom/ac-analytics","@marcom/ac-console":1,"@marcom/ac-dom-events/addEventListener":3,"@marcom/ac-dom-events/removeEventListener":9,"@marcom/ac-dom-traversal/querySelectorAll":25,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-object/create":27,"@marcom/ac-object/extend":28}],30:[function(c,d,b){var a=c("./../AnalyticsShare");
d.exports=function(f){return new a(f)}},{"./../AnalyticsShare":29}],31:[function(f,g,b){var d="f7c9180f-5c45-47b4-8de4-428015f096c0";
var c=!!window.localStorage.getItem(d);g.exports=function a(h){return function(){if(c&&typeof(window.console)==="object"){return console[h].apply(console,Array.prototype.slice.call(arguments,0))
}}}},{}],32:[function(b,c,a){c.exports=b("./internal/expose")("log")},{"./internal/expose":31}],33:[function(b,c,a){c.exports={EventEmitterMicro:b("./ac-event-emitter-micro/EventEmitterMicro")}
},{"./ac-event-emitter-micro/EventEmitterMicro":34}],34:[function(b,c,a){function f(){this._events={}
}var d=f.prototype;d.on=function(g,h){this._events[g]=this._events[g]||[];this._events[g].unshift(h)
};d.once=function(g,j){var i=this;function h(k){i.off(g,h);if(k!==undefined){j(k)
}else{j()}}this.on(g,h)};d.off=function(g,i){if(!this.has(g)){return}if(arguments.length===1){this._events[g]=null;
delete this._events[g];return}var h=this._events[g].indexOf(i);if(h===-1){return
}this._events[g].splice(h,1)};d.trigger=function(g,j){if(!this.has(g)){return}for(var h=this._events[g].length-1;
h>=0;h--){if(j!==undefined){this._events[g][h](j)}else{this._events[g][h]()}}};
d.has=function(g){if(g in this._events===false||this._events[g].length===0){return false
}return true};d.destroy=function(){for(var g in this._events){this._events[g]=null
}this._events=null};c.exports=f},{}],35:[function(b,c,a){c.exports={getWindow:function(){return window
},getDocument:function(){return document},getNavigator:function(){return navigator
}}},{}],36:[function(d,f,b){var a=d("./touchAvailable").original;var h=d("./helpers/globals");
var g=d("@marcom/ac-function/once");function c(){var i=h.getWindow();return(!a()&&!i.orientation)
}f.exports=g(c);f.exports.original=c},{"./helpers/globals":35,"./touchAvailable":40,"@marcom/ac-function/once":41}],37:[function(f,g,c){var d=f("./isDesktop").original;
var a=f("./isTablet").original;var h=f("@marcom/ac-function/once");function b(){return(!d()&&!a())
}g.exports=h(b);g.exports.original=b},{"./isDesktop":36,"./isTablet":39,"@marcom/ac-function/once":41}],38:[function(b,c,a){var d=b("./helpers/globals");
c.exports=function f(){var g=d.getWindow();return("devicePixelRatio" in g&&g.devicePixelRatio>=1.5)
}},{"./helpers/globals":35}],39:[function(f,g,c){var d=f("./isDesktop").original;
var i=f("./helpers/globals");var h=f("@marcom/ac-function/once");var b=600;function a(){var k=i.getWindow();
var j=k.screen.width;if(k.orientation&&k.screen.height<j){j=k.screen.height}return(!d()&&j>=b)
}g.exports=h(a);g.exports.original=a},{"./helpers/globals":35,"./isDesktop":36,"@marcom/ac-function/once":41}],40:[function(c,d,b){var g=c("./helpers/globals");
var f=c("@marcom/ac-function/once");function a(){var j=g.getWindow();var h=g.getDocument();
var i=g.getNavigator();return !!(("ontouchstart" in j)||(j.DocumentTouch&&h instanceof j.DocumentTouch)||(i.maxTouchPoints>0)||(i.msMaxTouchPoints>0))
}d.exports=f(a);d.exports.original=a},{"./helpers/globals":35,"@marcom/ac-function/once":41}],41:[function(b,c,a){c.exports=function d(g){var f;
return function(){if(typeof f==="undefined"){f=g.apply(this,arguments)}return f
}}},{}],42:[function(b,c,a){c.exports=function d(f,h){var g=null;return function(){if(g===null){f.apply(this,arguments);
g=setTimeout(function(){g=null},h)}}}},{}],43:[function(f,g,d){var c=f("./helpers/TabManager");
var b=f("./helpers/hideSiblingElements");var a=f("./helpers/showSiblingElements");
var i=function(j){this._tabbables=null;this._firstTabbableElement=null;this._lastTabbableElement=null;
this._relatedTarget=null;this.el=j;this._handleOnFocus=this._handleOnFocus.bind(this)
};var h=i.prototype;h.start=function(){this.updateTabbables();b(this.el);if(this._firstTabbableElement){if(!this.el.contains(document.activeElement)){this._firstTabbableElement.focus()
}}else{console.warn("this._firstTabbableElement is null, CircularTab needs at least one tabbable element.")
}this._relatedTarget=document.activeElement;document.addEventListener("focus",this._handleOnFocus,true)
};h.stop=function(){a(this.el);document.removeEventListener("focus",this._handleOnFocus,true)
};h.updateTabbables=function(){this._tabbables=c.getTabbableElements(this.el);this._firstTabbableElement=this._tabbables[0];
this._lastTabbableElement=this._tabbables[this._tabbables.length-1]};h._handleOnFocus=function(j){if(!this.el.contains(j.target)){j.preventDefault();
this.updateTabbables();if(this._relatedTarget===this._lastTabbableElement||this._relatedTarget===null){this._firstTabbableElement.focus();
this._relatedTarget=this._firstTabbableElement;return}if(this._relatedTarget===this._firstTabbableElement){this._lastTabbableElement.focus();
this._relatedTarget=this._lastTabbableElement;return}}else{this._relatedTarget=j.target
}};h.destroy=function(){this.stop();this.el=null;this._tabbables=null;this._firstTabbableElement=null;
this._lastTabbableElement=null;this._relatedTarget=null;this._handleOnFocus=null
};g.exports=i},{"./helpers/TabManager":44,"./helpers/hideSiblingElements":46,"./helpers/showSiblingElements":50}],44:[function(c,d,b){var g=c("./../maps/focusableElement");
var a=function(){this.focusableSelectors=g.join(",")};var f=a.prototype;f.isFocusableElement=function(k,j,i){if(!j&&!this._isDisplayed(k,j)){return false
}var l=k.nodeName.toLowerCase();var h=g.indexOf(l)>-1;if(l==="a"){return true}if(h){return !k.disabled
}if(!k.contentEditable){return true}i=i||parseFloat(k.getAttribute("tabindex"));
return !isNaN(i)};f.isTabbableElement=function(j,i){if(!i&&!this._isDisplayed(j,i)){return false
}var h=j.getAttribute("tabindex");h=parseFloat(h);if(!isNaN(h)){return(h>=0)}else{return this.isFocusableElement(j,i,h)
}};f._isDisplayed=function(h){var i=h.getBoundingClientRect();return i.top>0&&i.left>0&&i.width>0&&i.height>0
};f.getTabbableElements=function(m,h){var o=m.querySelectorAll(this.focusableSelectors);
var k=o.length;var j=[];for(var n=0;n<k;n++){if(this.isTabbableElement(o[n],h)){j.push(o[n])
}}return j};f.getFocusableElements=function(k,h){var o=k.querySelectorAll(this.focusableSelectors);
var j=o.length;var n=[];for(var m=0;m<j;m++){if(this.isFocusableElement(o[m],h)){n.push(o[m])
}}return n};d.exports=new a()},{"./../maps/focusableElement":52}],45:[function(c,b,d){var a=c("./setAttributes");
var h=c("./../maps/ariaMap");var k=c("./TabManager");var f="data-original-";var i="tabindex";
var j=function(m,n){var l=m.getAttribute(f+n);if(!l){l=m.getAttribute(n)||"";a(m,f+n,l)
}};b.exports=function g(m){if(k.isFocusableElement(m)){j(m,i);a(m,i,-1)}else{var n=k.getTabbableElements(m,true);
var l=n.length;while(l--){j(n[l],i);a(n[l],i,-1)}}j(m,h.HIDDEN);a(m,h.HIDDEN,true)
}},{"./../maps/ariaMap":51,"./TabManager":44,"./setAttributes":48}],46:[function(c,f,b){var d=c("./hide");
f.exports=function a(j,i){i=i||document.body;var h=j;var g=j;while((h=h.previousElementSibling)){d(h)
}while((g=g.nextElementSibling)){d(g)}if(j.parentElement&&j.parentElement!==i){a(j.parentElement)
}}},{"./hide":45}],47:[function(b,d,a){var f=function(j,h){if(typeof h!=="string"){return
}var k=h.split(/\s+/);for(var g=0;g<k.length;g++){if(j.getAttribute(k[g])){j.removeAttribute(k[g])
}}};var c=function(h,g){if(h.length){for(var j=0;j<h.length;j++){f(h[j],g)}}else{f(h,g)
}};d.exports=c},{}],48:[function(d,f,c){var b=function(h,g,i){if(h&&h.nodeType===1){h.setAttribute(g,i)
}};var a=function(g,j,k){if(typeof k!=="string"){k=k.toString()}if(!g){return}if(g.length){for(var h=0;
h<g.length;h++){b(g[h],j,k)}}else{b(g,j,k)}};f.exports=a},{}],49:[function(c,b,d){var h=c("./removeAttributes");
var a=c("./setAttributes");var i=c("./../maps/ariaMap");var f="data-original-";
var k="tabindex";var g=function(m,n){var l=m.getAttribute(f+n);if(typeof l==="string"){if(l.length){a(m,n,l)
}else{h(m,n)}h(m,f+n)}};b.exports=function j(m){h(m,k+" "+i.HIDDEN);g(m,k);g(m,i.HIDDEN);
var n=m.querySelectorAll("["+f+k+"]");var l=n.length;while(l--){g(n[l],k)}}},{"./../maps/ariaMap":51,"./removeAttributes":47,"./setAttributes":48}],50:[function(d,f,c){var b=d("./show");
f.exports=function a(j,i){i=i||document.body;var h=j;var g=j;while((h=h.previousElementSibling)){b(h)
}while((g=g.nextElementSibling)){b(g)}if(j.parentElement&&j.parentElement!==i){a(j.parentElement)
}}},{"./show":49}],51:[function(b,c,a){c.exports={AUTOCOMPLETE:"aria-autocomplete",CHECKED:"aria-checked",DISABLED:"aria-disabled",EXPANDED:"aria-expanded",HASPOPUP:"aria-haspopup",HIDDEN:"aria-hidden",INVALID:"aria-invalid",LABEL:"aria-label",LEVEL:"aria-level",MULTILINE:"aria-multiline",MULTISELECTABLE:"aria-multiselectable",ORIENTATION:"aria-orientation",PRESSED:"aria-pressed",READONLY:"aria-readonly",REQUIRED:"aria-required",SELECTED:"aria-selected",SORT:"aria-sort",VALUEMAX:"aria-valuemax",VALUEMIN:"aria-valuemin",VALUENOW:"aria-valuenow",VALUETEXT:"aria-valuetext",ATOMIC:"aria-atomic",BUSY:"aria-busy",LIVE:"aria-live",RELEVANT:"aria-relevant",DROPEFFECT:"aria-dropeffect",GRABBED:"aria-grabbed",ACTIVEDESCENDANT:"aria-activedescendant",CONTROLS:"aria-controls",DESCRIBEDBY:"aria-describedby",FLOWTO:"aria-flowto",LABELLEDBY:"aria-labelledby",OWNS:"aria-owns",POSINSET:"aria-posinset",SETSIZE:"aria-setsize"}
},{}],52:[function(b,c,a){c.exports=["input","select","textarea","button","optgroup","option","menuitem","fieldset","object","a[href]","*[tabindex]","*[contenteditable]"]
},{}],53:[function(b,c,a){b("@marcom/ac-polyfills/Array/prototype.slice");b("@marcom/ac-polyfills/Element/prototype.classList");
var d=b("./className/add");c.exports=function f(){var j=Array.prototype.slice.call(arguments);
var h=j.shift(j);var g;if(h.classList&&h.classList.add){h.classList.add.apply(h.classList,j);
return}for(g=0;g<j.length;g++){d(h,j[g])}}},{"./className/add":54,"@marcom/ac-polyfills/Array/prototype.slice":103,"@marcom/ac-polyfills/Element/prototype.classList":106}],54:[function(b,c,a){var d=b("./contains");
c.exports=function f(h,g){if(!d(h,g)){h.className+=" "+g}}},{"./contains":55}],55:[function(b,c,a){var f=b("./getTokenRegExp");
c.exports=function d(h,g){return f(g).test(h.className)}},{"./getTokenRegExp":56}],56:[function(b,c,a){c.exports=function d(f){return new RegExp("(\\s|^)"+f+"(\\s|$)")
}},{}],57:[function(c,d,b){var f=c("./contains");var g=c("./getTokenRegExp");d.exports=function a(i,h){if(f(i,h)){i.className=i.className.replace(g(h),"$1").trim()
}}},{"./contains":55,"./getTokenRegExp":56}],58:[function(d,f,c){d("@marcom/ac-polyfills/Array/prototype.slice");
d("@marcom/ac-polyfills/Element/prototype.classList");var b=d("./className/remove");
f.exports=function a(){var j=Array.prototype.slice.call(arguments);var h=j.shift(j);
var g;if(h.classList&&h.classList.remove){h.classList.remove.apply(h.classList,j);
return}for(g=0;g<j.length;g++){b(h,j[g])}}},{"./className/remove":57,"@marcom/ac-polyfills/Array/prototype.slice":103,"@marcom/ac-polyfills/Element/prototype.classList":106}],59:[function(b,c,a){arguments[4][11][0].apply(a,arguments)
},{dup:11}],60:[function(b,c,a){arguments[4][12][0].apply(a,arguments)},{dup:12}],61:[function(b,c,a){arguments[4][27][0].apply(a,arguments)
},{dup:27}],62:[function(d,c,g){var m=d("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var j=d("@marcom/ac-dom-events/utils/addEventListener");var b=d("@marcom/ac-dom-events/utils/removeEventListener");
var i=d("@marcom/ac-object/create");var f=d("./internal/KeyEvent");var k="keydown";
var l="keyup";function a(n){this._keysDown={};this._DOMKeyDown=this._DOMKeyDown.bind(this);
this._DOMKeyUp=this._DOMKeyUp.bind(this);this._context=n||document;j(this._context,k,this._DOMKeyDown,true);
j(this._context,l,this._DOMKeyUp,true);m.call(this)}var h=a.prototype=i(m.prototype);
h.onDown=function(n,o){return this.on(k+":"+n,o)};h.onceDown=function(n,o){return this.once(k+":"+n,o)
};h.offDown=function(n,o){return this.off(k+":"+n,o)};h.onUp=function(n,o){return this.on(l+":"+n,o)
};h.onceUp=function(n,o){return this.once(l+":"+n,o)};h.offUp=function(n,o){return this.off(l+":"+n,o)
};h.isDown=function(n){n+="";return this._keysDown[n]||false};h.isUp=function(n){return !this.isDown(n)
};h.destroy=function(){b(this._context,k,this._DOMKeyDown,true);b(this._context,l,this._DOMKeyUp,true);
this._keysDown=null;this._context=null;m.prototype.destroy.call(this);return this
};h._DOMKeyDown=function(o){var n=this._normalizeKeyboardEvent(o);var p=n.keyCode+="";
this._trackKeyDown(p);this.trigger(k+":"+p,n)};h._DOMKeyUp=function(o){var n=this._normalizeKeyboardEvent(o);
var p=n.keyCode+="";this._trackKeyUp(p);this.trigger(l+":"+p,n)};h._normalizeKeyboardEvent=function(n){return new f(n)
};h._trackKeyUp=function(n){if(this._keysDown[n]){this._keysDown[n]=false}};h._trackKeyDown=function(n){if(!this._keysDown[n]){this._keysDown[n]=true
}};c.exports=a},{"./internal/KeyEvent":64,"@marcom/ac-dom-events/utils/addEventListener":59,"@marcom/ac-dom-events/utils/removeEventListener":60,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-object/create":61}],63:[function(c,d,b){var a=c("./Keyboard");
d.exports=new a()},{"./Keyboard":62}],64:[function(c,d,b){var a=["keyLocation"];
function f(g){this.originalEvent=g;var h;for(h in g){if(a.indexOf(h)===-1&&typeof g[h]!=="function"){this[h]=g[h]
}}this.location=(this.originalEvent.location!==undefined)?this.originalEvent.location:this.originalEvent.keyLocation
}f.prototype={preventDefault:function(){if(typeof this.originalEvent.preventDefault!=="function"){this.originalEvent.returnValue=false;
return}return this.originalEvent.preventDefault()},stopPropagation:function(){return this.originalEvent.stopPropagation()
}};d.exports=f},{}],65:[function(b,c,a){c.exports={BACKSPACE:8,TAB:9,ENTER:13,SHIFT:16,CONTROL:17,ALT:18,COMMAND:91,CAPSLOCK:20,ESCAPE:27,PAGE_UP:33,PAGE_DOWN:34,END:35,HOME:36,ARROW_LEFT:37,ARROW_UP:38,ARROW_RIGHT:39,ARROW_DOWN:40,DELETE:46,ZERO:48,ONE:49,TWO:50,THREE:51,FOUR:52,FIVE:53,SIX:54,SEVEN:55,EIGHT:56,NINE:57,A:65,B:66,C:67,D:68,E:69,F:70,G:71,H:72,I:73,J:74,K:75,L:76,M:77,N:78,O:79,P:80,Q:81,R:82,S:83,T:84,U:85,V:86,W:87,X:88,Y:89,Z:90,NUMPAD_ZERO:96,NUMPAD_ONE:97,NUMPAD_TWO:98,NUMPAD_THREE:99,NUMPAD_FOUR:100,NUMPAD_FIVE:101,NUMPAD_SIX:102,NUMPAD_SEVEN:103,NUMPAD_EIGHT:104,NUMPAD_NINE:105,NUMPAD_ASTERISK:106,NUMPAD_PLUS:107,NUMPAD_DASH:109,NUMPAD_DOT:110,NUMPAD_SLASH:111,NUMPAD_EQUALS:187,TICK:192,LEFT_BRACKET:219,RIGHT_BRACKET:221,BACKSLASH:220,SEMICOLON:186,APOSTRAPHE:222,APOSTROPHE:222,SPACEBAR:32,CLEAR:12,COMMA:188,DOT:190,SLASH:191}
},{}],66:[function(b,c,a){arguments[4][3][0].apply(a,arguments)},{"./shared/getEventType":73,"./utils/addEventListener":75,dup:3}],67:[function(b,c,a){arguments[4][4][0].apply(a,arguments)
},{"./shared/camelCasedEventTypes":68,"./shared/prefixHelper":69,"./shared/windowFallbackEventTypes":70,"./utils/eventTypeAvailable":71,dup:4}],68:[function(b,c,a){arguments[4][5][0].apply(a,arguments)
},{dup:5}],69:[function(b,c,a){arguments[4][6][0].apply(a,arguments)},{dup:6}],70:[function(b,c,a){arguments[4][7][0].apply(a,arguments)
},{dup:7}],71:[function(b,c,a){arguments[4][8][0].apply(a,arguments)},{dup:8}],72:[function(b,c,a){arguments[4][9][0].apply(a,arguments)
},{"./shared/getEventType":73,"./utils/removeEventListener":76,dup:9}],73:[function(b,c,a){arguments[4][10][0].apply(a,arguments)
},{"@marcom/ac-prefixer/getEventType":67,dup:10}],74:[function(b,c,a){c.exports=function d(f){f=f||window.event;
return(typeof f.target!=="undefined")?f.target:f.srcElement}},{}],75:[function(b,c,a){arguments[4][11][0].apply(a,arguments)
},{dup:11}],76:[function(b,c,a){arguments[4][12][0].apply(a,arguments)},{dup:12}],77:[function(c,d,b){d.exports=function a(f){var g;
f=f||window;if(f===window){g=window.pageXOffset;if(!g){f=document.documentElement||document.body.parentNode||document.body
}else{return g}}return f.scrollLeft}},{}],78:[function(c,d,b){d.exports=function a(f){var g;
f=f||window;if(f===window){g=window.pageYOffset;if(!g){f=document.documentElement||document.body.parentNode||document.body
}else{return g}}return f.scrollTop}},{}],79:[function(b,c,a){arguments[4][13][0].apply(a,arguments)
},{dup:13}],80:[function(b,c,a){arguments[4][14][0].apply(a,arguments)},{dup:14}],81:[function(b,c,a){arguments[4][16][0].apply(a,arguments)
},{dup:16}],82:[function(b,c,a){arguments[4][17][0].apply(a,arguments)},{dup:17}],83:[function(b,c,a){arguments[4][18][0].apply(a,arguments)
},{"../isNode":86,dup:18}],84:[function(b,c,a){arguments[4][19][0].apply(a,arguments)
},{"../COMMENT_NODE":79,"../DOCUMENT_FRAGMENT_NODE":80,"../ELEMENT_NODE":81,"../TEXT_NODE":82,"./isNodeType":83,dup:19}],85:[function(b,c,a){arguments[4][21][0].apply(a,arguments)
},{"./ELEMENT_NODE":81,"./internal/isNodeType":83,dup:21}],86:[function(b,c,a){arguments[4][22][0].apply(a,arguments)
},{dup:22}],87:[function(b,c,a){arguments[4][23][0].apply(a,arguments)},{"./internal/validate":84,dup:23}],88:[function(b,c,a){arguments[4][27][0].apply(a,arguments)
},{dup:27}],89:[function(b,c,a){var f=b("./extend");c.exports=function d(h,g){if(typeof h!=="object"){throw new TypeError("defaults: must provide a defaults object")
}g=g||{};if(typeof g!=="object"){throw new TypeError("defaults: options must be a typeof object")
}return f({},h,g)}},{"./extend":90}],90:[function(b,c,a){arguments[4][28][0].apply(a,arguments)
},{"@marcom/ac-polyfills/Array/prototype.forEach":101,dup:28}],91:[function(b,c,a){c.exports={Modal:b("./ac-modal-basic/Modal"),Renderer:b("./ac-modal-basic/Renderer"),classNames:b("./ac-modal-basic/classNames"),dataAttributes:b("./ac-modal-basic/dataAttributes")}
},{"./ac-modal-basic/Modal":92,"./ac-modal-basic/Renderer":93,"./ac-modal-basic/classNames":94,"./ac-modal-basic/dataAttributes":95}],92:[function(b,a,f){var k={addEventListener:b("@marcom/ac-dom-events/addEventListener"),removeEventListener:b("@marcom/ac-dom-events/removeEventListener"),target:b("@marcom/ac-dom-events/target")};
var h={getScrollX:b("@marcom/ac-dom-metrics/getScrollX"),getScrollY:b("@marcom/ac-dom-metrics/getScrollY")};
var c={create:b("@marcom/ac-object/create"),defaults:b("@marcom/ac-object/defaults")};
var i=b("@marcom/ac-keyboard");var n=b("@marcom/ac-keyboard/keyMap");var l=b("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var d=b("./Renderer");var m={retainScrollPosition:false};function j(o,p){l.call(this);
this.options=c.defaults(m,o);this.renderer=new d(p);this.opened=false;this._keysToClose=[n.ESCAPE];
this._attachedKeysToClose=[];this.close=this.close.bind(this)}var g=j.prototype=c.create(l.prototype);
g.open=function(){if(this.options.retainScrollPosition){this._saveScrollPosition()
}if(!this.opened){this._attachEvents();this.trigger("willopen");this.renderer.open();
this.opened=true;this.trigger("open")}};g.close=function(o){var q;var p;if(this.opened){if(o&&o.type==="click"){q=k.target(o);
p=this.renderer.options.dataAttributes.close;if(!q.hasAttribute(p)){return}}this.trigger("willclose");
this._removeEvents();this.renderer.close();if(this.options.retainScrollPosition){this._restoreScrollPosition()
}this.opened=false;this.trigger("close")}};g.render=function(){this.renderer.render()
};g.appendContent=function(o,p){this.renderer.appendContent(o,p)};g.removeContent=function(o){this.renderer.removeContent(o)
};g.destroy=function(){this._removeEvents();this.renderer.destroy();for(var o in this){if(this.hasOwnProperty(o)){this[o]=null
}}};g.addKeyToClose=function(p){var o=this._keysToClose.indexOf(p);if(o===-1){this._keysToClose.push(p);
this._bindKeyToClose(p)}};g.removeKeyToClose=function(p){var o=this._keysToClose.indexOf(p);
if(o!==-1){this._keysToClose.splice(o,1)}this._releaseKeyToClose(p)};g._bindKeyToClose=function(p){var o=this._attachedKeysToClose.indexOf(p);
if(o===-1){i.onUp(p,this.close);this._attachedKeysToClose.push(p)}};g._releaseKeyToClose=function(p){var o=this._attachedKeysToClose.indexOf(p);
if(o!==-1){i.offUp(p,this.close);this._attachedKeysToClose.splice(o,1)}};g._removeEvents=function(){if(this.renderer.modalElement){k.removeEventListener(this.renderer.modalElement,"click",this.close)
}this._keysToClose.forEach(this._releaseKeyToClose,this)};g._attachEvents=function(){if(this.renderer.modalElement){k.addEventListener(this.renderer.modalElement,"click",this.close)
}this._keysToClose.forEach(this._bindKeyToClose,this)};g._restoreScrollPosition=function(){window.scrollTo(this._scrollX||0,this._scrollY||0)
};g._saveScrollPosition=function(){this._scrollX=h.getScrollX();this._scrollY=h.getScrollY()
};a.exports=j},{"./Renderer":93,"@marcom/ac-dom-events/addEventListener":66,"@marcom/ac-dom-events/removeEventListener":72,"@marcom/ac-dom-events/target":74,"@marcom/ac-dom-metrics/getScrollX":77,"@marcom/ac-dom-metrics/getScrollY":78,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-keyboard":63,"@marcom/ac-keyboard/keyMap":65,"@marcom/ac-object/create":88,"@marcom/ac-object/defaults":89}],93:[function(c,b,h){var a={add:c("@marcom/ac-classlist/add"),remove:c("@marcom/ac-classlist/remove")};
var f={defaults:c("@marcom/ac-object/defaults")};var k={remove:c("@marcom/ac-dom-nodes/remove"),isElement:c("@marcom/ac-dom-nodes/isElement")};
var j=c("./classNames");var l=c("./dataAttributes");var d={modalElement:null,contentElement:null,closeButton:null,classNames:j,dataAttributes:l};
var g=function(m){m=m||{};this.options=f.defaults(d,m);this.options.classNames=f.defaults(d.classNames,m.classNames);
this.options.dataAttributes=f.defaults(d.dataAttributes,m.dataAttributes);this.modalElement=this.options.modalElement;
this.contentElement=this.options.contentElement;this.closeButton=this.options.closeButton
};var i=g.prototype;i.render=function(){if(!k.isElement(this.modalElement)){this.modalElement=this.renderModalElement(this.options.classNames.modalElement)
}if(!k.isElement(this.contentElement)){this.contentElement=this.renderContentElement(this.options.classNames.contentElement)
}if(this.closeButton!==false){if(!k.isElement(this.closeButton)){this.closeButton=this.renderCloseButton(this.options.classNames.closeButton)
}this.modalElement.appendChild(this.closeButton)}this.modalElement.appendChild(this.contentElement);
document.body.appendChild(this.modalElement);return this.modalElement};i.renderCloseButton=function(n){var m;
n=n||this.options.classNames.closeButton;m=this._renderElement("button",n);m.setAttribute(this.options.dataAttributes.close,"");
return m};i.renderModalElement=function(m){m=m||this.options.classNames.modalElement;
return this._renderElement("div",m)};i.renderContentElement=function(m){m=m||this.options.classNames.contentElement;
return this._renderElement("div",m)};i.appendContent=function(m,n){if(!k.isElement(m)){return
}if(arguments[1]===undefined){this.contentElement.appendChild(m)}else{if(k.isElement(n)){n.appendChild(m)
}}};i.removeContent=function(m){if(m){if(this.modalElement.contains(m)){k.remove(m)
}}else{this._emptyContent()}};i.open=function(){var n=[document.documentElement].concat(this.options.classNames.documentElement);
var m=[this.modalElement].concat(this.options.classNames.modalOpen);a.add.apply(null,n);
a.add.apply(null,m)};i.close=function(){var n=[document.documentElement].concat(this.options.classNames.documentElement);
var m=[this.modalElement].concat(this.options.classNames.modalOpen);a.remove.apply(null,n);
a.remove.apply(null,m)};i.destroy=function(){var m=[document.documentElement].concat(this.options.classNames.documentElement);
if(this.modalElement&&document.body.contains(this.modalElement)){this.close();document.body.removeChild(this.modalElement)
}a.remove.apply(null,m);for(var n in this){if(this.hasOwnProperty(n)){this[n]=null
}}};i._renderElement=function(o,p){var n=document.createElement(o);var m=[n];if(p){m=m.concat(p)
}a.add.apply(null,m);return n};i._emptyContent=function(){this.contentElement.innerHTML=""
};b.exports=g},{"./classNames":94,"./dataAttributes":95,"@marcom/ac-classlist/add":53,"@marcom/ac-classlist/remove":58,"@marcom/ac-dom-nodes/isElement":85,"@marcom/ac-dom-nodes/remove":87,"@marcom/ac-object/defaults":89}],94:[function(b,c,a){c.exports={modalElement:"modal",modalOpen:"modal-open",documentElement:"has-modal",contentElement:"modal-content",closeButton:"modal-close"}
},{}],95:[function(b,c,a){c.exports={close:"data-modal-close"}},{}],96:[function(b,c,a){c.exports={Modal:b("./ac-modal/Modal"),createStandardModal:b("./ac-modal/factory/createStandardModal"),createFullViewportModal:b("./ac-modal/factory/createFullViewportModal")}
},{"./ac-modal/Modal":97,"./ac-modal/factory/createFullViewportModal":98,"./ac-modal/factory/createStandardModal":99}],97:[function(c,d,b){var h=c("@marcom/ac-modal-basic").Modal;
var g=c("@marcom/ac-event-emitter-micro").EventEmitterMicro;var i=c("@marcom/ac-accessibility/CircularTab");
function a(j){g.call(this);this.options=j||{};this._modal=new h(j,this.options.renderer);
this.opened=false;this._render();this.closeButton=this._modal.renderer.closeButton;
this.modalElement=this._modal.renderer.modalElement;this.contentElement=this._modal.renderer.contentElement;
this.modalElement.setAttribute("role","dialog");this.closeButton.setAttribute("aria-label","Close");
this._circularTab=new i(this.modalElement);this._onWillOpen=this._onWillOpen.bind(this);
this._onOpen=this._onOpen.bind(this);this._onWillClose=this._onWillClose.bind(this);
this._onClose=this._onClose.bind(this);this._bindEvents()}var f=a.prototype=Object.create(g.prototype);
f.open=function(){this._modal.open();this.opened=this._modal.opened};f.close=function(){this._modal.close()
};f.appendContent=function(j){this._modal.appendContent(j)};f.removeContent=function(j){this._modal.removeContent(j)
};f.destroy=function(){this._releaseEvents();this._modal.destroy();this._removeModalFocus();
this._circularTab.destroy();this._focusObj=null;for(var j in this){if(this.hasOwnProperty(j)){this[j]=null
}}};f.addKeyToClose=function(j){this._modal.addKeyToClose(j)};f.removeKeyToClose=function(j){this._modal.removeKeyToClose(j)
};f._render=function(){this._modal.render();this._modal.renderer.modalElement.setAttribute("aria-hidden","true")
};f._bindEvents=function(){this._modal.on("willopen",this._onWillOpen);this._modal.on("open",this._onOpen);
this._modal.on("willclose",this._onWillClose);this._modal.on("close",this._onClose)
};f._releaseEvents=function(){this._modal.off("willopen",this._onWillOpen);this._modal.off("open",this._onOpen);
this._modal.off("willclose",this._onWillClose);this._modal.off("close",this._onClose)
};f._onWillOpen=function(){this.trigger("willopen")};f._onOpen=function(){this.opened=this._modal.opened;
this._giveModalFocus();this.trigger("open")};f._onWillClose=function(){this.trigger("willclose");
this._removeModalFocus()};f._onClose=function(){this.opened=this._modal.opened;
this.trigger("close")};f._giveModalFocus=function(){this.modalElement.setAttribute("aria-hidden","false");
this._activeElement=document.activeElement;this.closeButton.focus();this._circularTab.start()
};f._removeModalFocus=function(){this._circularTab.stop();this.modalElement.setAttribute("aria-hidden","true");
if(this._activeElement){this._activeElement.focus();this._activeElement=null}};
d.exports=a},{"@marcom/ac-accessibility/CircularTab":43,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-modal-basic":91}],98:[function(g,h,d){var c=g("../Modal");
var b=g("@marcom/ac-modal-basic").classNames;var f={retainScrollPosition:true,renderer:{classNames:{documentElement:[b.documentElement].concat("has-modal-full-viewport"),modalElement:[b.modalElement].concat("modal-full-viewport")}}};
function a(j){var i=new c(f);if(j){i.appendContent(j)}return i}h.exports=a},{"../Modal":97,"@marcom/ac-modal-basic":91}],99:[function(c,b,d){var h=c("../Modal");
var f=c("@marcom/ac-modal-basic").classNames;var i=c("@marcom/ac-modal-basic").dataAttributes;
var a={add:c("@marcom/ac-classlist/add")};var j={renderer:{classNames:{documentElement:[f.documentElement].concat("has-modal-standard"),modalElement:[f.modalElement].concat("modal-standard")}}};
function g(p){var o=new h(j);if(p){o.appendContent(p)}var l=document.createElement("div");
var n=document.createElement("div");var m=document.createElement("div");var k=document.createElement("div");
a.add(l,"content-table");a.add(n,"content-cell");a.add(m,"content-wrapper");a.add(k,"content-padding","large-8","medium-10");
o.modalElement.setAttribute(i.close,"");m.setAttribute(i.close,"");n.setAttribute(i.close,"");
l.appendChild(n);n.appendChild(m);m.appendChild(k);o.modalElement.appendChild(l);
k.appendChild(o.contentElement);k.appendChild(o.closeButton);return o}b.exports=g
},{"../Modal":97,"@marcom/ac-classlist/add":53,"@marcom/ac-modal-basic":91}],100:[function(b,c,a){if(!Array.isArray){Array.isArray=function(d){return Object.prototype.toString.call(d)==="[object Array]"
}}},{}],101:[function(b,c,a){if(!Array.prototype.forEach){Array.prototype.forEach=function d(l,k){var j=Object(this);
var f;var g;if(typeof l!=="function"){throw new TypeError("No function object passed to forEach.")
}var h=this.length;for(f=0;f<h;f+=1){g=j[f];l.call(k,g,f,j)}}}},{}],102:[function(b,c,a){if(!Array.prototype.indexOf){Array.prototype.indexOf=function d(g,h){var i=h||0;
var f=0;if(i<0){i=this.length+h-1;if(i<0){throw"Wrapped past beginning of array while looking up a negative start index."
}}for(f=0;f<this.length;f++){if(this[f]===g){return f}}return(-1)}}},{}],103:[function(b,c,a){(function(){var d=Array.prototype.slice;
try{d.call(document.documentElement)}catch(f){Array.prototype.slice=function(n,j){j=(typeof j!=="undefined")?j:this.length;
if(Object.prototype.toString.call(this)==="[object Array]"){return d.call(this,n,j)
}var l,h=[],k,g=this.length;var o=n||0;o=(o>=0)?o:g+o;var m=(j)?j:g;if(j<0){m=g+j
}k=m-o;if(k>0){h=new Array(k);if(this.charAt){for(l=0;l<k;l++){h[l]=this.charAt(o+l)
}}else{for(l=0;l<k;l++){h[l]=this[o+l]}}}return h}}}())},{}],104:[function(b,c,a){if(document.createEvent){try{new window.CustomEvent("click")
}catch(d){window.CustomEvent=(function(){function f(h,i){i=i||{bubbles:false,cancelable:false,detail:undefined};
var g=document.createEvent("CustomEvent");g.initCustomEvent(h,i.bubbles,i.cancelable,i.detail);
return g}f.prototype=window.Event.prototype;return f}())}}},{}],105:[function(c,d,a){if(!Date.now){Date.now=function b(){return new Date().getTime()
}}},{}],106:[function(b,c,a){
/*! @source http://purl.eligrey.com/github/classList.js/blob/master/classList.js*/
;
if("document" in self){if(!("classList" in document.createElement("_"))){(function(n){if(!("Element" in n)){return
}var d="classList",j="prototype",q=n.Element[j],f=Object,o=String[j].trim||function(){return this.replace(/^\s+|\s+$/g,"")
},g=Array[j].indexOf||function(u){var t=0,s=this.length;for(;t<s;t++){if(t in this&&this[t]===u){return t
}}return -1},r=function(s,t){this.name=s;this.code=DOMException[s];this.message=t
},k=function(t,s){if(s===""){throw new r("SYNTAX_ERR","An invalid or illegal string was specified")
}if(/\s/.test(s)){throw new r("INVALID_CHARACTER_ERR","String contains an invalid character")
}return g.call(t,s)},h=function(w){var v=o.call(w.getAttribute("class")||""),u=v?v.split(/\s+/):[],t=0,s=u.length;
for(;t<s;t++){this.push(u[t])}this._updateClassName=function(){w.setAttribute("class",this.toString())
}},i=h[j]=[],m=function(){return new h(this)};r[j]=Error[j];i.item=function(s){return this[s]||null
};i.contains=function(s){s+="";return k(this,s)!==-1};i.add=function(){var w=arguments,v=0,t=w.length,u,s=false;
do{u=w[v]+"";if(k(this,u)===-1){this.push(u);s=true}}while(++v<t);if(s){this._updateClassName()
}};i.remove=function(){var x=arguments,w=0,t=x.length,v,s=false,u;do{v=x[w]+"";
u=k(this,v);while(u!==-1){this.splice(u,1);s=true;u=k(this,v)}}while(++w<t);if(s){this._updateClassName()
}};i.toggle=function(t,u){t+="";var s=this.contains(t),v=s?u!==true&&"remove":u!==false&&"add";
if(v){this[v](t)}if(u===true||u===false){return u}else{return !s}};i.toString=function(){return this.join(" ")
};if(f.defineProperty){var p={get:m,enumerable:true,configurable:true};try{f.defineProperty(q,d,p)
}catch(l){if(l.number===-2146823252){p.enumerable=false;f.defineProperty(q,d,p)
}}}else{if(f[j].__defineGetter__){q.__defineGetter__(d,m)}}}(self))}else{(function(){var f=document.createElement("_");
f.classList.add("c1","c2");if(!f.classList.contains("c2")){var g=function(i){var h=DOMTokenList.prototype[i];
DOMTokenList.prototype[i]=function(l){var k,j=arguments.length;for(k=0;k<j;k++){l=arguments[k];
h.call(this,l)}}};g("add");g("remove")}f.classList.toggle("c3",false);if(f.classList.contains("c3")){var d=DOMTokenList.prototype.toggle;
DOMTokenList.prototype.toggle=function(h,i){if(1 in arguments&&!this.contains(h)===!i){return i
}else{return d.call(this,h)}}}f=null}())}}},{}],107:[function(b,c,a){if(typeof Object.assign!="function"){Object.assign=function(h){if(h==null){throw new TypeError("Cannot convert undefined or null to object")
}h=Object(h);for(var d=1;d<arguments.length;d++){var g=arguments[d];if(g!=null){for(var f in g){if(Object.prototype.hasOwnProperty.call(g,f)){h[f]=g[f]
}}}}return h}}},{}],108:[function(b,c,a){
/*! MIT License
 *
 * performance.now polyfill
 * copyright Paul Irish 2015
 *
 */
;
b("../Date/now");(function(){if("performance" in window==false){window.performance={}
}if("now" in window.performance==false){var f=Date.now();if(performance.timing&&performance.timing.navigationStart){f=performance.timing.navigationStart
}window.performance.now=function d(){return Date.now()-f}}})()},{"../Date/now":105}],109:[function(b,c,a){arguments[4][13][0].apply(a,arguments)
},{dup:13}],110:[function(b,c,a){arguments[4][14][0].apply(a,arguments)},{dup:14}],111:[function(b,c,a){arguments[4][15][0].apply(a,arguments)
},{dup:15}],112:[function(b,c,a){arguments[4][16][0].apply(a,arguments)},{dup:16}],113:[function(b,c,a){arguments[4][17][0].apply(a,arguments)
},{dup:17}],114:[function(b,c,a){arguments[4][18][0].apply(a,arguments)},{"../isNode":118,dup:18}],115:[function(b,c,a){arguments[4][19][0].apply(a,arguments)
},{"../COMMENT_NODE":109,"../DOCUMENT_FRAGMENT_NODE":110,"../ELEMENT_NODE":112,"../TEXT_NODE":113,"./isNodeType":114,dup:19}],116:[function(b,c,a){arguments[4][20][0].apply(a,arguments)
},{"./DOCUMENT_FRAGMENT_NODE":110,"./internal/isNodeType":114,dup:20}],117:[function(b,c,a){arguments[4][21][0].apply(a,arguments)
},{"./ELEMENT_NODE":112,"./internal/isNodeType":114,dup:21}],118:[function(b,c,a){arguments[4][22][0].apply(a,arguments)
},{dup:22}],119:[function(b,c,a){arguments[4][23][0].apply(a,arguments)},{"./internal/validate":115,dup:23}],120:[function(b,c,a){c.exports=window.Element?(function(d){return d.matches||d.matchesSelector||d.webkitMatchesSelector||d.mozMatchesSelector||d.msMatchesSelector||d.oMatchesSelector
}(Element.prototype)):null},{}],121:[function(b,c,a){arguments[4][24][0].apply(a,arguments)
},{"@marcom/ac-dom-nodes/COMMENT_NODE":109,"@marcom/ac-dom-nodes/DOCUMENT_FRAGMENT_NODE":110,"@marcom/ac-dom-nodes/DOCUMENT_NODE":111,"@marcom/ac-dom-nodes/ELEMENT_NODE":112,"@marcom/ac-dom-nodes/TEXT_NODE":113,"@marcom/ac-dom-nodes/isNode":118,"@marcom/ac-polyfills/Array/prototype.indexOf":102,dup:24}],122:[function(d,f,c){var g=d("@marcom/ac-dom-nodes/isElement");
var i=d("./internal/validate");var a=d("./internal/nativeMatches");var h=d("./shims/matchesSelector");
f.exports=function b(k,j){i.selector(j,true,"matchesSelector");if(!g(k)){return false
}if(!a){return h(k,j)}return a.call(k,j)}},{"./internal/nativeMatches":120,"./internal/validate":121,"./shims/matchesSelector":124,"@marcom/ac-dom-nodes/isElement":117}],123:[function(b,c,a){arguments[4][25][0].apply(a,arguments)
},{"./internal/validate":121,"./shims/querySelectorAll":125,"@marcom/ac-polyfills/Array/prototype.slice":103,dup:25}],124:[function(c,d,b){var f=c("../querySelectorAll");
d.exports=function a(l,g){var k=l.parentNode||document;var h=f(g,k);var j;for(j=0;
j<h.length;j++){if(h[j]===l){return true}}return false}},{"../querySelectorAll":123}],125:[function(b,c,a){arguments[4][26][0].apply(a,arguments)
},{"@marcom/ac-dom-nodes/isDocumentFragment":116,"@marcom/ac-dom-nodes/isElement":117,"@marcom/ac-dom-nodes/remove":119,"@marcom/ac-polyfills/Array/prototype.indexOf":102,dup:26}],126:[function(b,c,a){c.exports.EventEmitter=b("./ac-event-emitter/EventEmitter")
},{"./ac-event-emitter/EventEmitter":127}],127:[function(d,c,f){var h="EventEmitter:propagation";
var k=function(l){if(l){this.context=l}};var g=k.prototype;var i=function(){if(!this.hasOwnProperty("_events")&&typeof this._events!=="object"){this._events={}
}return this._events};var a=function(m,o){var p=m[0];var q=m[1];var n=m[2];if((typeof p!=="string"&&typeof p!=="object")||p===null||Array.isArray(p)){throw new TypeError("Expecting event name to be a string or object.")
}if((typeof p==="string")&&!q){throw new Error("Expecting a callback function to be provided.")
}if(q&&(typeof q!=="function")){if(typeof p==="object"&&typeof q==="object"){n=q
}else{throw new TypeError("Expecting callback to be a function.")}}if(typeof p==="object"){for(var l in p){o.call(this,l,p[l],n)
}}if(typeof p==="string"){p=p.split(" ");p.forEach(function(r){o.call(this,r,q,n)
},this)}};var j=function(o,p){var l;var m;var n;l=i.call(this)[o];if(!l||l.length===0){return
}l=l.slice();this._stoppedImmediatePropagation=false;for(m=0,n=l.length;m<n;m++){if(this._stoppedImmediatePropagation||p(l[m],m)){break
}}};var b=function(m,n,o){var l=-1;j.call(this,n,function(q,p){if(q.callback===o){l=p;
return true}});if(l===-1){return}m[n].splice(l,1)};g.on=function(){var l=i.call(this);
a.call(this,arguments,function(n,o,m){l[n]=l[n]||(l[n]=[]);l[n].push({callback:o,context:m})
});return this};g.once=function(){a.call(this,arguments,function(m,o,l){var n=function(p){o.call(l||this,p);
this.off(m,n)};this.on(m,n,this)});return this};g.off=function(n,p){var m=i.call(this);
if(arguments.length===0){this._events={}}else{if(!n||(typeof n!=="string"&&typeof n!=="object")||Array.isArray(n)){throw new TypeError("Expecting event name to be a string or object.")
}}if(typeof n==="object"){for(var o in n){b.call(this,m,o,n[o])}}if(typeof n==="string"){var l=n.split(" ");
if(l.length===1){if(p){b.call(this,m,n,p)}else{m[n]=[]}}else{l.forEach(function(q){m[q]=[]
})}}return this};g.trigger=function(m,n,l){if(!m){throw new Error("trigger method requires an event name")
}if(typeof m!=="string"){throw new TypeError("Expecting event names to be a string.")
}if(l&&typeof l!=="boolean"){throw new TypeError("Expecting doNotPropagate to be a boolean.")
}m=m.split(" ");m.forEach(function(o){j.call(this,o,function(p){p.callback.call(p.context||this.context||this,n)
}.bind(this));if(!l){j.call(this,h,function(q){var p=o;if(q.prefix){p=q.prefix+p
}q.emitter.trigger(p,n)})}},this);return this};g.propagateTo=function(m,n){var l=i.call(this);
if(!l[h]){this._events[h]=[]}l[h].push({emitter:m,prefix:n})};g.stopPropagatingTo=function(o){var m=i.call(this);
if(!o){m[h]=[];return}var p=m[h];var n=p.length;var l;for(l=0;l<n;l++){if(p[l].emitter===o){p.splice(l,1);
break}}};g.stopImmediatePropagation=function(){this._stoppedImmediatePropagation=true
};g.has=function(l,s,p){var o=i.call(this);var m=o[l];if(arguments.length===0){return Object.keys(o)
}if(!m){return false}if(!s){return(m.length>0)?true:false}for(var n=0,q=m.length;
n<q;n++){var r=m[n];if(p&&s&&r.context===p&&r.callback===s){return true}else{if(s&&!p&&r.callback===s){return true
}}}return false};c.exports=k},{}],128:[function(b,c,a){c.exports={DOMEmitter:b("./ac-dom-emitter/DOMEmitter")}
},{"./ac-dom-emitter/DOMEmitter":129}],129:[function(c,b,d){var f;var k=c("ac-event-emitter").EventEmitter,j=c("./DOMEmitterEvent"),g={addEventListener:c("@marcom/ac-dom-events/addEventListener"),removeEventListener:c("@marcom/ac-dom-events/removeEventListener"),dispatchEvent:c("@marcom/ac-dom-events/dispatchEvent")},a={querySelectorAll:c("@marcom/ac-dom-traversal/querySelectorAll"),matchesSelector:c("@marcom/ac-dom-traversal/matchesSelector")};
var i="dom-emitter";function h(l){if(l===null){return}this.el=l;this._bindings={};
this._delegateFuncs={};this._eventEmitter=new k()}f=h.prototype;f.on=function(){this._normalizeArgumentsAndCall(Array.prototype.slice.call(arguments,0),this._on);
return this};f.once=function(){this._normalizeArgumentsAndCall(Array.prototype.slice.call(arguments,0),this._once);
return this};f.off=function(){this._normalizeArgumentsAndCall(Array.prototype.slice.call(arguments,0),this._off);
return this};f.has=function(l,q,p,n){var o,r;if(typeof q==="string"){o=q;r=p}else{r=q;
n=p}if(o){var m=this._getDelegateFuncBindingIdx(l,o,r,n,true);if(m>-1){return true
}return false}if(this._eventEmitter&&this._eventEmitter.has.apply(this._eventEmitter,arguments)){return true
}return false};f.trigger=function(n,m,o,s){n=this._parseEventNames(n);n=this._cleanStringData(n);
var q,r,p,l=n.length;if(typeof m==="string"){q=this._cleanStringData(m);r=o}else{r=m;
s=o}for(p=0;p<l;p++){this._triggerDOMEvents(n[p],r,q)}return this};f.emitterTrigger=function(m,o,p){if(!this._eventEmitter){return this
}m=this._parseEventNames(m);m=this._cleanStringData(m);o=new j(o,this);var n,l=m.length;
for(n=0;n<l;n++){this._eventEmitter.trigger(m[n],o,p)}return this};f.propagateTo=function(l,m){this._eventEmitter.propagateTo(l,m);
return this};f.stopPropagatingTo=function(l){this._eventEmitter.stopPropagatingTo(l);
return this};f.stopImmediatePropagation=function(){this._eventEmitter.stopImmediatePropagation();
return this};f.destroy=function(){this._triggerInternalEvent("willdestroy");this.off();
var l;for(l in this){if(this.hasOwnProperty(l)){this[l]=null}}};f._parseEventNames=function(l){if(!l){return[l]
}return l.split(" ")};f._onListenerEvent=function(n,m){var l=new j(m,this);this._eventEmitter.trigger(n,l,false)
};f._setListener=function(l){this._bindings[l]=this._onListenerEvent.bind(this,l);
g.addEventListener(this.el,l,this._bindings[l])};f._removeListener=function(l){g.removeEventListener(this.el,l,this._bindings[l]);
this._bindings[l]=null};f._triggerInternalEvent=function(l,m){this.emitterTrigger(i+":"+l,m)
};f._normalizeArgumentsAndCall=function(l,n){var r={};if(l.length===0){n.call(this,r);
return}if(typeof l[0]==="string"||l[0]===null){l=this._cleanStringData(l);r.events=l[0];
if(typeof l[1]==="string"){r.delegateQuery=l[1];r.callback=l[2];r.context=l[3]}else{r.callback=l[1];
r.context=l[2]}n.call(this,r);return}var m,p,q=":",o=l[0];for(m in o){if(o.hasOwnProperty(m)){r={};
p=this._cleanStringData(m.split(q));r.events=p[0];r.delegateQuery=p[1];r.callback=o[m];
r.context=l[1];n.call(this,r)}}};f._registerDelegateFunc=function(n,p,q,l,o){var m=this._delegateFunc.bind(this,n,p,q,o);
this._delegateFuncs[p]=this._delegateFuncs[p]||{};this._delegateFuncs[p][n]=this._delegateFuncs[p][n]||[];
this._delegateFuncs[p][n].push({func:l,context:o,delegateFunc:m});return m};f._cleanStringData=function(o){var n=false;
if(typeof o==="string"){o=[o];n=true}var m=[],q,s,r,p,l=o.length;for(q=0;q<l;q++){s=o[q];
if(typeof s==="string"){if(s===""||s===" "){continue}r=s.length;while(s[0]===" "){s=s.slice(1,r);
r--}while(s[r-1]===" "){s=s.slice(0,r-1);r--}}m.push(s)}if(n){return m[0]}return m
};f._unregisterDelegateFunc=function(n,q,l,p){if(!this._delegateFuncs[q]||!this._delegateFuncs[q][n]){return
}var o=this._getDelegateFuncBindingIdx(n,q,l,p),m;if(o>-1){m=this._delegateFuncs[q][n][o].delegateFunc;
this._delegateFuncs[q][n].splice(o,1);if(this._delegateFuncs[q][n].length===0){this._delegateFuncs[q][n]=null
}}return m};f._unregisterDelegateFuncs=function(l,n){if(!this._delegateFuncs[n]){return
}if(l!==null&&!this._delegateFuncs[n][l]){return}if(l===null){var m;for(m in this._delegateFuncs[n]){if(this._delegateFuncs[n].hasOwnProperty(m)){this._unbindDelegateFunc(m,n)
}}return}this._unbindDelegateFunc(l,n)};f._unbindDelegateFunc=function(l,n){var o,p,m=0;
while(this._delegateFuncs[n][l]&&this._delegateFuncs[n][l][m]){o=this._delegateFuncs[n][l][m];
p=this._delegateFuncs[n][l][m].length;this._off({events:l,delegateQuery:n,callback:o.func,context:o.context});
if(this._delegateFuncs[n][l]&&p===this._delegateFuncs[n][l].length){m++}}o=p=null
};f._unregisterDelegateFuncsByEvent=function(l){var m;for(m in this._delegateFuncs){if(this._delegateFuncs.hasOwnProperty(m)){this._unregisterDelegateFuncs(l,m)
}}};f._delegateFunc=function(l,p,r,n,q){if(this._targetHasDelegateAncestor(q.target,p)){var m=Array.prototype.slice.call(arguments,0),o=m.slice(4,m.length);
n=n||window;if(typeof q.detail==="object"){o[0]=q.detail}r.apply(n,o)}};f._targetHasDelegateAncestor=function(n,m){var l=n;
while(l&&l!==this.el&&l!==document.documentElement){if(a.matchesSelector(l,m)){return true
}l=l.parentNode}return false};f._on=function(p){var m=p.events,q=p.callback,o=p.delegateQuery,n=p.context,l=p.unboundCallback||q;
m=this._parseEventNames(m);m.forEach(function(v,r,t,u,s){if(!this.has(s)){this._setListener(s)
}if(typeof u==="string"){v=this._registerDelegateFunc(s,u,v,r,t)}this._triggerInternalEvent("willon",{evt:s,callback:v,context:t,delegateQuery:u});
this._eventEmitter.on(s,v,t);this._triggerInternalEvent("didon",{evt:s,callback:v,context:t,delegateQuery:u})
}.bind(this,q,l,n,o));m=q=l=o=n=null};f._off=function(q){var m=q.events,r=q.callback,p=q.delegateQuery,o=q.context,l=q.unboundCallback||r;
if(typeof m==="undefined"){this._eventEmitter.off();var n;for(n in this._bindings){if(this._bindings.hasOwnProperty(n)){this._removeListener(n)
}}for(n in this._delegateFuncs){if(this._delegateFuncs.hasOwnProperty(n)){this._delegateFuncs[n]=null
}}return}m=this._parseEventNames(m);m.forEach(function(w,s,u,v,t){if(typeof v==="string"&&typeof s==="function"){w=this._unregisterDelegateFunc(t,v,s,u);
if(!w){return}}if(typeof v==="string"&&typeof w==="undefined"){this._unregisterDelegateFuncs(t,v);
return}if(typeof t==="string"&&typeof w==="undefined"){this._unregisterDelegateFuncsByEvent(t);
if(typeof v==="string"){return}}this._triggerInternalEvent("willoff",{evt:t,callback:w,context:u,delegateQuery:v});
this._eventEmitter.off(t,w,u);this._triggerInternalEvent("didoff",{evt:t,callback:w,context:u,delegateQuery:v});
if(!this.has(t)){this._removeListener(t)}}.bind(this,r,l,o,p));m=r=l=p=o=null};
f._once=function(o){var l=o.events,p=o.callback,n=o.delegateQuery,m=o.context;l=this._parseEventNames(l);
l.forEach(function(t,r,s,q){if(typeof s==="string"){return this._handleDelegateOnce(q,t,r,s)
}if(!this.has(q)){this._setListener(q)}this._triggerInternalEvent("willonce",{evt:q,callback:t,context:r,delegateQuery:s});
this._eventEmitter.once.call(this,q,t,r);this._triggerInternalEvent("didonce",{evt:q,callback:t,context:r,delegateQuery:s})
}.bind(this,p,m,n));l=p=n=m=null};f._handleDelegateOnce=function(l,o,m,n){this._triggerInternalEvent("willonce",{evt:l,callback:o,context:m,delegateQuery:n});
this._on({events:l,context:m,delegateQuery:n,callback:this._getDelegateOnceCallback.bind(this,l,o,m,n),unboundCallback:o});
this._triggerInternalEvent("didonce",{evt:l,callback:o,context:m,delegateQuery:n});
return this};f._getDelegateOnceCallback=function(l,q,n,p){var m=Array.prototype.slice.call(arguments,0),o=m.slice(4,m.length);
q.apply(n,o);this._off({events:l,delegateQuery:p,callback:q,context:n})};f._getDelegateFuncBindingIdx=function(s,p,n,l,t){var r=-1;
if(this._delegateFuncs[p]&&this._delegateFuncs[p][s]){var o,m,q=this._delegateFuncs[p][s].length;
for(o=0;o<q;o++){m=this._delegateFuncs[p][s][o];if(t&&typeof n==="undefined"){n=m.func
}if(m.func===n&&m.context===l){r=o;break}}}return r};f._triggerDOMEvents=function(n,q,p){var m=[this.el];
if(p){m=a.querySelectorAll(p,this.el)}var o,r,l=m.length;for(o=0;o<l;o++){g.dispatchEvent(m[o],n,{bubbles:true,cancelable:true,detail:q})
}};b.exports=h},{"./DOMEmitterEvent":130,"@marcom/ac-dom-events/addEventListener":131,"@marcom/ac-dom-events/dispatchEvent":132,"@marcom/ac-dom-events/removeEventListener":140,"@marcom/ac-dom-traversal/matchesSelector":122,"@marcom/ac-dom-traversal/querySelectorAll":123,"ac-event-emitter":126}],130:[function(b,c,a){var f={preventDefault:b("@marcom/ac-dom-events/preventDefault"),stopPropagation:b("@marcom/ac-dom-events/stopPropagation"),target:b("@marcom/ac-dom-events/target")};
var d;var g=function(i,h){this._domEmitter=h;this.originalEvent=i||{};this._originalTarget=f.target(this.originalEvent);
this.target=this._originalTarget||this._domEmitter.el;this.currentTarget=this._domEmitter.el;
this.timeStamp=this.originalEvent.timeStamp||Date.now();if(this._isDOMEvent(this.originalEvent)){if(typeof this.originalEvent.detail==="object"){this.data=this.originalEvent.detail
}}else{if(i){this.data=this.originalEvent;this.originalEvent={}}}};d=g.prototype;
d.preventDefault=function(){f.preventDefault(this.originalEvent)};d.stopPropagation=function(){f.stopPropagation(this.originalEvent)
};d.stopImmediatePropagation=function(){if(this.originalEvent.stopImmediatePropagation){this.originalEvent.stopImmediatePropagation()
}this._domEmitter.stopImmediatePropagation()};d._isDOMEvent=function(h){if(this._originalTarget||(document.createEvent!=="undefined"&&typeof CustomEvent!=="undefined"&&h instanceof CustomEvent)){return true
}return false};c.exports=g},{"@marcom/ac-dom-events/preventDefault":139,"@marcom/ac-dom-events/stopPropagation":143,"@marcom/ac-dom-events/target":144}],131:[function(b,c,a){arguments[4][3][0].apply(a,arguments)
},{"./shared/getEventType":141,"./utils/addEventListener":145,dup:3}],132:[function(d,f,c){var a=d("./utils/dispatchEvent");
var b=d("./shared/getEventType");f.exports=function g(j,i,h){i=b(j,i);return a(j,i,h)
}},{"./shared/getEventType":141,"./utils/dispatchEvent":146}],133:[function(b,c,a){c.exports={addEventListener:b("./addEventListener"),dispatchEvent:b("./dispatchEvent"),preventDefault:b("./preventDefault"),removeEventListener:b("./removeEventListener"),stop:b("./stop"),stopPropagation:b("./stopPropagation"),target:b("./target")}
},{"./addEventListener":131,"./dispatchEvent":132,"./preventDefault":139,"./removeEventListener":140,"./stop":142,"./stopPropagation":143,"./target":144}],134:[function(b,c,a){arguments[4][4][0].apply(a,arguments)
},{"./shared/camelCasedEventTypes":135,"./shared/prefixHelper":136,"./shared/windowFallbackEventTypes":137,"./utils/eventTypeAvailable":138,dup:4}],135:[function(b,c,a){arguments[4][5][0].apply(a,arguments)
},{dup:5}],136:[function(b,c,a){arguments[4][6][0].apply(a,arguments)},{dup:6}],137:[function(b,c,a){arguments[4][7][0].apply(a,arguments)
},{dup:7}],138:[function(b,c,a){arguments[4][8][0].apply(a,arguments)},{dup:8}],139:[function(c,d,a){d.exports=function b(f){f=f||window.event;
if(f.preventDefault){f.preventDefault()}else{f.returnValue=false}}},{}],140:[function(b,c,a){arguments[4][9][0].apply(a,arguments)
},{"./shared/getEventType":141,"./utils/removeEventListener":147,dup:9}],141:[function(b,c,a){arguments[4][10][0].apply(a,arguments)
},{"@marcom/ac-prefixer/getEventType":134,dup:10}],142:[function(d,g,b){var a=d("./stopPropagation");
var c=d("./preventDefault");g.exports=function f(h){h=h||window.event;a(h);c(h);
h.stopped=true;h.returnValue=false}},{"./preventDefault":139,"./stopPropagation":143}],143:[function(c,d,b){d.exports=function a(f){f=f||window.event;
if(f.stopPropagation){f.stopPropagation()}else{f.cancelBubble=true}}},{}],144:[function(b,c,a){arguments[4][74][0].apply(a,arguments)
},{dup:74}],145:[function(b,c,a){arguments[4][11][0].apply(a,arguments)},{dup:11}],146:[function(b,c,a){b("@marcom/ac-polyfills/CustomEvent");
c.exports=function d(i,h,g){var f;if(i.dispatchEvent){if(g){f=new CustomEvent(h,g)
}else{f=new CustomEvent(h)}i.dispatchEvent(f)}else{f=document.createEventObject();
if(g&&"detail" in g){f.detail=g.detail}i.fireEvent("on"+h,f)}return i}},{"@marcom/ac-polyfills/CustomEvent":104}],147:[function(b,c,a){arguments[4][12][0].apply(a,arguments)
},{dup:12}],148:[function(b,c,a){arguments[4][126][0].apply(a,arguments)},{"./ac-event-emitter/EventEmitter":149,dup:126}],149:[function(b,c,a){arguments[4][127][0].apply(a,arguments)
},{dup:127}],150:[function(d,f,c){var a=d("qs");f.exports=function b(h,g){var i=a.stringify(h,{strictNullHandling:true});
if(i&&g!==false){i="?"+i}return i}},{qs:151}],151:[function(b,d,a){var g=b("./stringify");
var c=b("./parse");var f={};d.exports={stringify:g,parse:c}},{"./parse":152,"./stringify":153}],152:[function(b,c,a){var f=b("./utils");
var d={delimiter:"&",depth:5,arrayLimit:20,parameterLimit:1000,strictNullHandling:false,plainObjects:false,allowPrototypes:false};
d.parseValues=function(m,q){var k={};var j=m.split(q.delimiter,q.parameterLimit===Infinity?undefined:q.parameterLimit);
for(var l=0,o=j.length;l<o;++l){var g=j[l];var n=g.indexOf("]=")===-1?g.indexOf("="):g.indexOf("]=")+1;
if(n===-1){k[f.decode(g)]="";if(q.strictNullHandling){k[f.decode(g)]=null}}else{var p=f.decode(g.slice(0,n));
var h=f.decode(g.slice(n+1));if(!Object.prototype.hasOwnProperty.call(k,p)){k[p]=h
}else{k[p]=[].concat(k[p]).concat(h)}}}return k};d.parseObject=function(l,n,k){if(!l.length){return n
}var g=l.shift();var m;if(g==="[]"){m=[];m=m.concat(d.parseObject(l,n,k))}else{m=k.plainObjects?Object.create(null):{};
var j=g[0]==="["&&g[g.length-1]==="]"?g.slice(1,g.length-1):g;var i=parseInt(j,10);
var h=""+i;if(!isNaN(i)&&g!==j&&h===j&&i>=0&&(k.parseArrays&&i<=k.arrayLimit)){m=[];
m[i]=d.parseObject(l,n,k)}else{m[j]=d.parseObject(l,n,k)}}return m};d.parseKeys=function(j,n,g){if(!j){return
}if(g.allowDots){j=j.replace(/\.([^\.\[]+)/g,"[$1]")}var k=/^([^\[\]]*)/;var o=/(\[[^\[\]]*\])/g;
var m=k.exec(j);var l=[];if(m[1]){if(!g.plainObjects&&Object.prototype.hasOwnProperty(m[1])){if(!g.allowPrototypes){return
}}l.push(m[1])}var h=0;while((m=o.exec(j))!==null&&h<g.depth){++h;if(!g.plainObjects&&Object.prototype.hasOwnProperty(m[1].replace(/\[|\]/g,""))){if(!g.allowPrototypes){continue
}}l.push(m[1])}if(m){l.push("["+j.slice(m.index)+"]")}return d.parseObject(l,n,g)
};c.exports=function(k,p){p=p||{};p.delimiter=typeof p.delimiter==="string"||f.isRegExp(p.delimiter)?p.delimiter:d.delimiter;
p.depth=typeof p.depth==="number"?p.depth:d.depth;p.arrayLimit=typeof p.arrayLimit==="number"?p.arrayLimit:d.arrayLimit;
p.parseArrays=p.parseArrays!==false;p.allowDots=p.allowDots!==false;p.plainObjects=typeof p.plainObjects==="boolean"?p.plainObjects:d.plainObjects;
p.allowPrototypes=typeof p.allowPrototypes==="boolean"?p.allowPrototypes:d.allowPrototypes;
p.parameterLimit=typeof p.parameterLimit==="number"?p.parameterLimit:d.parameterLimit;
p.strictNullHandling=typeof p.strictNullHandling==="boolean"?p.strictNullHandling:d.strictNullHandling;
if(k===""||k===null||typeof k==="undefined"){return p.plainObjects?Object.create(null):{}
}var l=typeof k==="string"?d.parseValues(k,p):k;var h=p.plainObjects?Object.create(null):{};
var o=Object.keys(l);for(var j=0,m=o.length;j<m;++j){var n=o[j];var g=d.parseKeys(n,l[n],p);
h=f.merge(h,g,p)}return f.compact(h)}},{"./utils":154}],153:[function(b,c,a){var f=b("./utils");
var d={delimiter:"&",arrayPrefixGenerators:{brackets:function(h,g){return h+"[]"
},indices:function(h,g){return h+"["+g+"]"},repeat:function(h,g){return h}},strictNullHandling:false};
d.stringify=function(l,n,g,j,h){if(typeof h==="function"){l=h(n,l)}else{if(f.isBuffer(l)){l=l.toString()
}else{if(l instanceof Date){l=l.toISOString()}else{if(l===null){if(j){return f.encode(n)
}l=""}}}}if(typeof l==="string"||typeof l==="number"||typeof l==="boolean"){return[f.encode(n)+"="+f.encode(l)]
}var q=[];if(typeof l==="undefined"){return q}var k=Array.isArray(h)?h:Object.keys(l);
for(var m=0,o=k.length;m<o;++m){var p=k[m];if(Array.isArray(l)){q=q.concat(d.stringify(l[p],g(n,p),g,j,h))
}else{q=q.concat(d.stringify(l[p],n+"["+p+"]",g,j,h))}}return q};c.exports=function(o,s){s=s||{};
var j=typeof s.delimiter==="undefined"?d.delimiter:s.delimiter;var l=typeof s.strictNullHandling==="boolean"?s.strictNullHandling:d.strictNullHandling;
var n;var k;if(typeof s.filter==="function"){k=s.filter;o=k("",o)}else{if(Array.isArray(s.filter)){n=k=s.filter
}}var r=[];if(typeof o!=="object"||o===null){return""}var g;if(s.arrayFormat in d.arrayPrefixGenerators){g=s.arrayFormat
}else{if("indices" in s){g=s.indices?"indices":"repeat"}else{g="indices"}}var h=d.arrayPrefixGenerators[g];
if(!n){n=Object.keys(o)}for(var m=0,p=n.length;m<p;++m){var q=n[m];r=r.concat(d.stringify(o[q],q,h,l,k))
}return r.join(j)}},{"./utils":154}],154:[function(b,c,a){var f={};f.hexTable=new Array(256);
for(var d=0;d<256;++d){f.hexTable[d]="%"+((d<16?"0":"")+d.toString(16)).toUpperCase()
}a.arrayToObject=function(k,h){var l=h.plainObjects?Object.create(null):{};for(var j=0,g=k.length;
j<g;++j){if(typeof k[j]!=="undefined"){l[j]=k[j]}}return l};a.merge=function(o,n,h){if(!n){return o
}if(typeof n!=="object"){if(Array.isArray(o)){o.push(n)}else{if(typeof o==="object"){o[n]=true
}else{o=[o,n]}}return o}if(typeof o!=="object"){o=[o].concat(n);return o}if(Array.isArray(o)&&!Array.isArray(n)){o=a.arrayToObject(o,h)
}var l=Object.keys(n);for(var g=0,j=l.length;g<j;++g){var i=l[g];var m=n[i];if(!Object.prototype.hasOwnProperty.call(o,i)){o[i]=m
}else{o[i]=a.merge(o[i],m,h)}}return o};a.decode=function(h){try{return decodeURIComponent(h.replace(/\+/g," "))
}catch(g){return h}};a.encode=function(k){if(k.length===0){return k}if(typeof k!=="string"){k=""+k
}var h="";for(var j=0,g=k.length;j<g;++j){var l=k.charCodeAt(j);if(l===45||l===46||l===95||l===126||(l>=48&&l<=57)||(l>=65&&l<=90)||(l>=97&&l<=122)){h+=k[j];
continue}if(l<128){h+=f.hexTable[l];continue}if(l<2048){h+=f.hexTable[192|(l>>6)]+f.hexTable[128|(l&63)];
continue}if(l<55296||l>=57344){h+=f.hexTable[224|(l>>12)]+f.hexTable[128|((l>>6)&63)]+f.hexTable[128|(l&63)];
continue}++j;l=65536+(((l&1023)<<10)|(k.charCodeAt(j)&1023));h+=f.hexTable[240|(l>>18)]+f.hexTable[128|((l>>12)&63)]+f.hexTable[128|((l>>6)&63)]+f.hexTable[128|(l&63)]
}return h};a.compact=function(o,j){if(typeof o!=="object"||o===null){return o}j=j||[];
var n=j.indexOf(o);if(n!==-1){return j[n]}j.push(o);if(Array.isArray(o)){var g=[];
for(var l=0,h=o.length;l<h;++l){if(typeof o[l]!=="undefined"){g.push(o[l])}}return g
}var m=Object.keys(o);for(l=0,h=m.length;l<h;++l){var k=m[l];o[k]=a.compact(o[k],j)
}return o};a.isRegExp=function(g){return Object.prototype.toString.call(g)==="[object RegExp]"
};a.isBuffer=function(g){if(g===null||typeof g==="undefined"){return false}return !!(g.constructor&&g.constructor.isBuffer&&g.constructor.isBuffer(g))
}},{}],155:[function(b,c,a){c.exports={clone:b("./clone"),create:b("./create"),defaults:b("./defaults"),extend:b("./extend"),getPrototypeOf:b("./getPrototypeOf"),isDate:b("./isDate"),isEmpty:b("./isEmpty"),isRegExp:b("./isRegExp"),toQueryParameters:b("./toQueryParameters")}
},{"./clone":156,"./create":157,"./defaults":158,"./extend":159,"./getPrototypeOf":160,"./isDate":161,"./isEmpty":162,"./isRegExp":163,"./toQueryParameters":164}],156:[function(c,d,b){c("@marcom/ac-polyfills/Array/isArray");
var h=c("./extend");var a=Object.prototype.hasOwnProperty;var f=function(i,j){var k;
for(k in j){if(a.call(j,k)){if(j[k]===null){i[k]=null}else{if(typeof j[k]==="object"){i[k]=Array.isArray(j[k])?[]:{};
f(i[k],j[k])}else{i[k]=j[k]}}}}return i};d.exports=function g(j,i){if(i){return f({},j)
}return h({},j)}},{"./extend":159,"@marcom/ac-polyfills/Array/isArray":100}],157:[function(b,c,a){arguments[4][27][0].apply(a,arguments)
},{dup:27}],158:[function(b,c,a){arguments[4][89][0].apply(a,arguments)},{"./extend":159,dup:89}],159:[function(b,c,a){arguments[4][28][0].apply(a,arguments)
},{"@marcom/ac-polyfills/Array/prototype.forEach":101,dup:28}],160:[function(c,d,b){var a=Object.prototype.hasOwnProperty;
d.exports=function f(i){if(Object.getPrototypeOf){return Object.getPrototypeOf(i)
}else{if(typeof i!=="object"){throw new Error("Requested prototype of a value that is not an object.")
}else{if(typeof this.__proto__==="object"){return i.__proto__}else{var g=i.constructor;
var h;if(a.call(i,"constructor")){h=g;if(!(delete i.constructor)){return null}g=i.constructor;
i.constructor=h}return g?g.prototype:null}}}}},{}],161:[function(b,d,a){d.exports=function c(f){return Object.prototype.toString.call(f)==="[object Date]"
}},{}],162:[function(c,d,b){var a=Object.prototype.hasOwnProperty;d.exports=function f(g){var h;
if(typeof g!=="object"){throw new TypeError("ac-base.Object.isEmpty : Invalid parameter - expected object")
}for(h in g){if(a.call(g,h)){return false}}return true}},{}],163:[function(c,d,b){d.exports=function a(f){return window.RegExp?f instanceof RegExp:false
}},{}],164:[function(c,f,b){var a=c("@marcom/ac-url/joinSearchParams");f.exports=function d(g){if(typeof g!=="object"){throw new TypeError("toQueryParameters error: argument is not an object")
}return a(g,false)}},{"@marcom/ac-url/joinSearchParams":150}],165:[function(b,c,a){c.exports={Routes:b("./ac-routes/Routes"),Route:b("./ac-routes/Route")}
},{"./ac-routes/Route":166,"./ac-routes/Routes":167}],166:[function(b,c,a){function f(i,k,h,j,g){this.path=i;
this.callback=k;this.context=h;this.greedy=j||false;this.priority=g||0;if(typeof this.priority!=="number"){throw new Error("Priority must be a Number.")
}this.identifierPattern="([a-zA-Z0-9\\-\\_]+)";this.tokensRe=new RegExp(":"+this.identifierPattern,"g");
this.matcher=this._createRouteMatcher(i)}var d=f.prototype;d._createRouteMatcher=function(h){if(h&&h.exec){return{pattern:h}
}else{if(h==="/"){return{pattern:/^\/$/}}else{if(typeof h!=="string"){throw new Error("path must be either a string or regex")
}}}var g=this._extractRouteTokens(h);var j=h.replace(this.tokensRe,this.identifierPattern);
var i=new RegExp(j,"g");return{pattern:i,routeTokens:g}};d._extractRouteTokens=function(j){var g=j.replace(this.tokensRe,":"+this.identifierPattern);
var i=new RegExp(g,"g");var h=i.exec(j);if(h&&h.length>1){h=h.slice(1)}else{h=null
}return h};d.match=function(h){this.matcher.pattern.lastIndex=0;var g=this.matcher.pattern.exec(h);
if(g){var i=(g.length)?g.slice(1):[];var j=this.callback;if(j&&typeof j==="function"){j.apply(this.context||this,i);
return true}}return false};c.exports=f},{}],167:[function(c,d,b){var g=c("./Route");
function a(h){this._routes={};if(h){this.addRoutes(h)}}var f=a.prototype;f._getIndex=function(k,l,j){if(this._routes[k]!==undefined){var h=this._routes[k].length;
while(--h>-1){if(this._routes[k][h].callback===l&&this._routes[k][h].context===j){return h
}}}return -1};f.match=function(k){var j,h;for(j in this._routes){h=this._routes[j].length;
while(--h>-1){if(this._routes[j][h].match(k)&&this._routes[j][h].greedy){break}}}};
f.add=function(j){if(this._routes[j.path]===undefined){this._routes[j.path]=[j]
}else{if(!this.get(j.path,j.callback,j.context)){var k,h=this._routes[j.path].length;
if(h>0){for(k=0;k<h;++k){if(this._routes[j.path][k].priority>j.priority){this._routes[j.path].splice(k,0,j);
return j}}}this._routes[j.path].push(j)}}return j};f.remove=function(h){var j=this._getIndex(h.path,h.callback,h.context);
if(j>-1){this._routes[h.path].splice(j,1);return h}return false};f.get=function(k,l,j){var h=this._getIndex(k,l,j);
if(h>-1){return this._routes[k][h]}return false};f.createRoute=function(k,m,j,l,i){var h=new g(k,m,j,l,i);
this.add(h);return h};f.addRoutes=function(j){if(j instanceof Array){var l,k,h=j.length;
for(l=0;l<h;++l){k=j[l];if(k&&typeof k==="object"){this.add(k)}}}else{throw new Error("routes must be an Array.")
}};f.removeRoutes=function(j){if(j instanceof Array){var l,k,h=j.length;for(l=0;
l<h;++l){k=j[l];if(k&&typeof k==="object"){this.remove(k)}}}else{throw new Error("routes must be an Array.")
}};f.getRoutes=function(h){if(this._routes[h]===undefined){return[]}return this._routes[h]
};d.exports=a},{"./Route":166}],168:[function(b,c,a){c.exports={Router:b("./ac-router/Router"),History:b("./ac-router/History"),Routes:b("@marcom/ac-routes").Routes,Route:b("@marcom/ac-routes").Route}
},{"./ac-router/History":169,"./ac-router/Router":170,"@marcom/ac-routes":165}],169:[function(c,f,b){var d=c("@marcom/ac-object").create;
var a=c("@marcom/ac-dom-events");var i=c("@marcom/ac-event-emitter").EventEmitter;
function h(k){k=k||{};this.history=window.history;this.rootStripper=/^\/+|\/+$/g;
this.root=k.root||"/";this.root=("/"+this.root+"/").replace(this.rootStripper,"/");
var j=typeof k.resolveInitialHash!=="boolean"?true:k.resolveInitialHash;this._pushState=typeof k.pushState!=="boolean"?true:k.pushState;
this._hashChange=k.hashChange||false;this._setUpdateVars(j);if(k.autoStart){this.start()
}}var g=h.prototype=d(i.prototype);g._isRoot=function(j){return("/"+j+"/").replace(this.rootStripper,"/")===this.root
};g._isPushStateSupported=function(){return(this.history&&this.history.pushState)
};g._isHashChangeSupported=function(){return("onhashchange" in window)};g._setUpdateVars=function(k){if(this._pushState&&this._isPushStateSupported()){if(k&&this._hashChange&&window.location.href.indexOf("#")!==-1){this.history.pushState({},document.title,window.location.href.replace("#",""))
}this._hashChange=false}else{if(k&&this._pushState&&this._hashChange&&window.location.href.indexOf("#")<0){if(!window.location.origin){window.location.origin=window.location.protocol+"//"+window.location.hostname;
window.location.origin+=(window.location.port?":"+window.location.port:"")}var j=window.location.href.substr(window.location.origin.length+this.root.length);
if(j.length){window.location=window.location.origin+this.root+"#"+j;return}}if(this._hashChange&&!this._isHashChangeSupported()){this._interval=50;
this._iframe=document.createElement('<iframe src="javascript:0" tabindex="-1" style="display:none;">');
this._iframe=document.body.appendChild(this._iframe).contentWindow;this._iframe.document.open().close()
}this._pushState=false}};g._checkUrl=function(){var j=this._iframe.location.hash.substr(1);
if(j.length===0){j="/"}if(this.fragment()!==j){window.location.hash="#"+j;this._ignoreHashChange=false;
this._handleHashChange()}};g._handlePopState=function(j){this.trigger("popstate",{fragment:this.fragment()})
};g._handleHashChange=function(j){if(this._ignoreHashChange){this._ignoreHashChange=false;
return}this.trigger("popstate",{fragment:this.fragment()})};g.canUpdate=function(){return this._pushState||this._hashChange
};g.start=function(){if(!this.started&&(this._pushState||this._hashChange)){this.started=true;
if(this._pushState){this._handlePopState=this._handlePopState.bind(this);a.addEventListener(window,"popstate",this._handlePopState)
}else{if(this._hashChange){if(this._isHashChangeSupported()){this._handleHashChange=this._handleHashChange.bind(this);
a.addEventListener(window,"hashchange",this._handleHashChange)}else{this._iframe.location.hash=this.fragment();
this._checkUrl=this._checkUrl.bind(this);this._checkUrlInterval=setInterval(this._checkUrl,this._interval)
}}}}return this.started||false};g.stop=function(){if(this.started){this.started=false;
if(this._pushState){a.removeEventListener(window,"popstate",this._handlePopState)
}else{if(this._hashChange){if(this._isHashChangeSupported()){a.removeEventListener(window,"hashchange",this._handleHashChange)
}else{if(this._checkUrlInterval){clearInterval(this._checkUrlInterval);this._checkUrlInterval=null
}}}}}};g.navigate=function(l,k){if(!this.started||!this.canUpdate()){return false
}k=k||{};var j=((this._isRoot(l)?"":this.root)+l).replace(/([^:])(\/\/)/g,"$1/");
if(this._pushState){this.history.pushState(k,document.title,j)}else{if(this._hashChange){this._ignoreHashChange=true;
window.location.hash="#"+l;if(!this._isHashChangeSupported()){this._iframe.document.open().close();
this._iframe.location.hash="#"+l}}}return true};g.fragment=function(){var j="";
if(this._pushState){j=(window.location.pathname).substr(this.root.length)}else{if(this._hashChange){j=window.location.hash.substr(1)
}}return j===""?"/":j};f.exports=h},{"@marcom/ac-dom-events":133,"@marcom/ac-event-emitter":148,"@marcom/ac-object":155}],170:[function(d,c,g){var i=d("@marcom/ac-object").create;
var k=d("@marcom/ac-dom-emitter").DOMEmitter;var f=d("./History");var j=d("@marcom/ac-routes").Route;
var a=d("@marcom/ac-routes").Routes;function b(l){l=l||{};this._intercept=l.intercept||"[data-route]";
this._interceptAttribute=l.attribute||"href";this._handleTrigger=this._handleTrigger.bind(this);
this.intercept(this._intercept);this.history=l.history||new f({root:l.root,autoStart:l.autoStart,pushState:l.pushState,hashChange:l.hashChange,resolveInitialHash:l.resolveInitialHash});
a.call(this,l.routes);if(l.autoStart){if(!this.history.started){this.history.start()
}this.start()}}var h=b.prototype=i(a.prototype);h._handleTrigger=function(m){if(!this.started){return
}var l=m.target.getAttribute(this._interceptAttribute);if(l){if(/^(http|https):\/\/+/.exec(l)&&this._interceptAttribute==="href"){l=l.substr(l.indexOf(this.history.root)+this.history.root.length)||"/"
}if(this.navigate(l)){m.preventDefault()}}};h._handlePopstate=function(l){this.navigate(l.fragment,true)
};h.start=function(){if(!this.started){this.started=true;this.history.start();this._handlePopstate=this._handlePopstate.bind(this);
this.history.on("popstate",this._handlePopstate);this.navigate(this.history.fragment(),true)
}};h.stop=function(){if(this.started){this.started=false;this.history.stop();this.history.off("popstate",this._handlePopstate)
}};h.navigate=function(m,l){if(this.history.fragment()===m&&!l){return this.history.canUpdate()
}if(m&&!l){if(!this.history.navigate(m)){return false}}this.match(m);return true
};h.intercept=function(m,n){var l=new k(n||document.body);l.on("click",m,this._handleTrigger)
};c.exports=b},{"./History":169,"@marcom/ac-dom-emitter":128,"@marcom/ac-object":155,"@marcom/ac-routes":165}],171:[function(b,c,a){var d={ua:window.navigator.userAgent,platform:window.navigator.platform,vendor:window.navigator.vendor};
c.exports=b("./parseUserAgent")(d)},{"./parseUserAgent":174}],172:[function(b,c,a){c.exports={browser:{safari:false,chrome:false,firefox:false,ie:false,opera:false,android:false,edge:false,version:{name:"",major:0,minor:0,patch:0,documentMode:false}},os:{osx:false,ios:false,android:false,windows:false,linux:false,fireos:false,chromeos:false,version:{name:"",major:0,minor:0,patch:0}}}
},{}],173:[function(b,c,a){c.exports={browser:[{name:"edge",userAgent:"Edge",version:["rv","Edge"],test:function(d){return(d.ua.indexOf("Edge")>-1||d.ua==="Mozilla/5.0 (Windows NT 10.0; Win64; x64)")
}},{name:"chrome",userAgent:"Chrome"},{name:"firefox",test:function(d){return(d.ua.indexOf("Firefox")>-1&&d.ua.indexOf("Opera")===-1)
},version:"Firefox"},{name:"android",userAgent:"Android"},{name:"safari",test:function(d){return(d.ua.indexOf("Safari")>-1&&d.vendor.indexOf("Apple")>-1)
},version:"Version"},{name:"ie",test:function(d){return(d.ua.indexOf("IE")>-1||d.ua.indexOf("Trident")>-1)
},version:["MSIE","rv"],parseDocumentMode:function(){var d=false;if(document.documentMode){d=parseInt(document.documentMode,10)
}return d}},{name:"opera",userAgent:"Opera",version:["Version","Opera"]}],os:[{name:"windows",test:function(d){return(d.platform.indexOf("Win")>-1)
},version:"Windows NT"},{name:"osx",userAgent:"Mac",test:function(d){return(d.platform.indexOf("Mac")>-1)
}},{name:"ios",test:function(d){return(d.ua.indexOf("iPhone")>-1||d.ua.indexOf("iPad")>-1)
},version:["iPhone OS","CPU OS"]},{name:"linux",userAgent:"Linux",test:function(d){return(d.platform.indexOf("Linux")>-1&&d.ua.indexOf("Android")===-1)
}},{name:"fireos",test:function(d){return(d.ua.indexOf("Firefox")>-1&&d.ua.indexOf("Mobile")>-1)
},version:"rv"},{name:"android",userAgent:"Android"},{name:"chromeos",userAgent:"CrOS"}]}
},{}],174:[function(b,a,d){var c=b("./defaults");var h=b("./dictionary");function g(k){return new RegExp(k+"[a-zA-Z\\s/:]+([0-9_.]+)","i")
}function f(n,m){if(typeof n.parseVersion==="function"){return n.parseVersion(m)
}else{var p=n.version||n.userAgent;if(typeof p==="string"){p=[p]}var o=p.length;
var k;for(var l=0;l<o;l++){k=m.match(g(p[l]));if(k&&k.length>1){return k[1].replace(/_/g,".")
}}}}function j(m,r,p){var o=m.length;var q;var k;for(var n=0;n<o;n++){if(typeof m[n].test==="function"){if(m[n].test(p)===true){q=m[n].name
}}else{if(p.ua.indexOf(m[n].userAgent)>-1){q=m[n].name}}if(q){r[q]=true;k=f(m[n],p.ua);
if(typeof k==="string"){var l=k.split(".");r.version.name=k;if(l&&l.length>0){r.version.major=parseInt(l[0]||0);
r.version.minor=parseInt(l[1]||0);r.version.patch=parseInt(l[2]||0)}}else{if(q==="edge"){r.version.name="12.0.0";
r.version.major="12";r.version.minor="0";r.version.patch="0"}}if(typeof m[n].parseDocumentMode==="function"){r.version.documentMode=m[n].parseDocumentMode()
}return r}}return r}function i(l){var k={};k.browser=j(h.browser,c.browser,l);k.os=j(h.os,c.os,l);
return k}a.exports=i},{"./defaults":172,"./dictionary":173}],175:[function(b,c,a){arguments[4][44][0].apply(a,arguments)
},{"./../maps/focusableElement":181,dup:44}],176:[function(b,c,a){arguments[4][45][0].apply(a,arguments)
},{"./../maps/ariaMap":180,"./TabManager":175,"./setAttributes":178,dup:45}],177:[function(b,c,a){arguments[4][47][0].apply(a,arguments)
},{dup:47}],178:[function(b,c,a){arguments[4][48][0].apply(a,arguments)},{dup:48}],179:[function(b,c,a){arguments[4][49][0].apply(a,arguments)
},{"./../maps/ariaMap":180,"./removeAttributes":177,"./setAttributes":178,dup:49}],180:[function(b,c,a){arguments[4][51][0].apply(a,arguments)
},{dup:51}],181:[function(b,c,a){arguments[4][52][0].apply(a,arguments)},{dup:52}],182:[function(b,f,a){var g=b("./request/factory");
var d={complete:function(j,i){},error:function(j,i){},method:"GET",headers:{},success:function(j,i,k){},timeout:5000};
var h=function(){for(var k=1;k<arguments.length;k++){for(var j in arguments[k]){if(arguments[k].hasOwnProperty(j)){arguments[0][j]=arguments[k][j]
}}}return arguments[0]};var c={ajax:function(i,j){j=h({},d,j);if(i.substr(0,2)==="//"){i=window.location.protocol+i
}var k=g(i);k.open(j.method,i);k.setTransportHeaders(j.headers);k.setReadyStateChangeHandlers(j.complete,j.error,j.success);
k.setTimeout(j.timeout,j.error,j.complete);k.send(j.data);return k},get:function(i,j){j.method="GET";
return c.ajax(i,j)},head:function(i,j){j.method="HEAD";return c.ajax(i,j)},post:function(i,j){j.method="POST";
return c.ajax(i,j)}};f.exports=c},{"./request/factory":183}],183:[function(c,b,f){var j=c("./xmlhttprequest");
var i=c("./xdomainrequest");var h=/.*(?=:\/\/)/;var a=/^.*:\/\/|\/.+$/g;var d=window.XDomainRequest&&document.documentMode<10;
var g=function(l){if(!l.match(h)){return false}var k=l.replace(a,"");return k!==window.location.hostname
};b.exports=function(k,l){var m=d&&g(k)?i:j;return new m()}},{"./xdomainrequest":185,"./xmlhttprequest":186}],184:[function(b,d,a){var c=function(){};
c.create=function(){var f=function(){};f.prototype=c.prototype;return new f()};
c.prototype.open=function(g,f){g=g.toUpperCase();this.xhr.open(g,f)};c.prototype.send=function(f){this.xhr.send(f)
};c.prototype.setTimeout=function(h,g,f){this.xhr.ontimeout=function(){g(this.xhr,this.status);
f(this.xhr,this.status)}.bind(this)};c.prototype.setTransportHeaders=function(f){for(var g in f){this.xhr.setRequestHeader(g,f[g])
}};d.exports=c},{}],185:[function(b,f,a){var d=b("./request");var c=b("@marcom/ac-object/toQueryParameters");
var g=function(){this.xhr=new XDomainRequest()};g.prototype=d.create();g.prototype.setReadyStateChangeHandlers=function(h,i,j){this.xhr.onerror=function(){i(this.xhr,this.status);
h(this.xhr,this.status)}.bind(this);this.xhr.onload=function(){j(this.xhr.responseText,this.xhr.status,this.xhr);
h(this.xhr,this.status)}.bind(this)};g.prototype.send=function(h){if(h&&typeof h==="object"){h=c(h)
}this.xhr.send(h)};g.prototype.setTransportHeaders=function(h){};f.exports=g},{"./request":184,"@marcom/ac-object/toQueryParameters":215}],186:[function(b,d,a){var c=b("./request");
var f=function(){this.xhr=new XMLHttpRequest()};f.prototype=c.create();f.prototype.setReadyStateChangeHandlers=function(g,h,i){this.xhr.onreadystatechange=function(j){if(this.xhr.readyState===4){clearTimeout(this.timeout);
if(this.xhr.status>=200&&this.xhr.status<300){i(this.xhr.responseText,this.xhr.status,this.xhr);
g(this.xhr,this.status)}else{h(this.xhr,this.status);g(this.xhr,this.status)}}}.bind(this)
};d.exports=f},{"./request":184}],187:[function(c,d,b){d.exports=function a(g){if(typeof g.select==="function"){var i=false;
i=g.select();if(!i){g.setSelectionRange(0,g.value.length)}}else{var f=document.createRange();
f.selectNodeContents(g);var h=window.getSelection();h.removeAllRanges();h.addRange(f)
}}},{}],188:[function(b,c,a){arguments[4][3][0].apply(a,arguments)},{"./shared/getEventType":194,"./utils/addEventListener":195,dup:3}],189:[function(b,c,a){arguments[4][4][0].apply(a,arguments)
},{"./shared/camelCasedEventTypes":190,"./shared/prefixHelper":191,"./shared/windowFallbackEventTypes":192,"./utils/eventTypeAvailable":193,dup:4}],190:[function(b,c,a){arguments[4][5][0].apply(a,arguments)
},{dup:5}],191:[function(b,c,a){arguments[4][6][0].apply(a,arguments)},{dup:6}],192:[function(b,c,a){arguments[4][7][0].apply(a,arguments)
},{dup:7}],193:[function(b,c,a){arguments[4][8][0].apply(a,arguments)},{dup:8}],194:[function(b,c,a){arguments[4][10][0].apply(a,arguments)
},{"@marcom/ac-prefixer/getEventType":189,dup:10}],195:[function(b,c,a){arguments[4][11][0].apply(a,arguments)
},{dup:11}],196:[function(b,c,a){c.exports=b("./fullscreen")},{"./fullscreen":202}],197:[function(b,c,a){c.exports={STANDARD:"standard",IOS:"ios"}
},{}],198:[function(f,c,i){var h=f("@marcom/ac-dom-events/addEventListener");var l=f("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var a=f("./../events/types");var b=f("./../consts/modes");var d=new l();function k(n){d.trigger(a.ENTERFULLSCREEN,n)
}function m(n){d.trigger(a.EXITFULLSCREEN,n)}function g(n){if(d.fullscreenElement()){k(n)
}else{m(n)}}function j(){h(document,"fullscreenchange",g)}j();d.fullscreenEnabled=function(n){var o=document.fullscreenEnabled||document.webkitFullscreenEnabled||document.mozFullScreenEnabled||document.msFullscreenEnabled;
return !!(o)};d.fullscreenElement=function(){return document.fullscreenElement||document.webkitFullscreenElement||document.mozFullScreenElement||document.msFullscreenElement||document.webkitCurrentFullScreenElement
};d.exitFullscreen=function(n){var o;if(typeof document.exitFullscreen==="function"){o="exitFullscreen"
}else{if(typeof document.webkitExitFullscreen==="function"){o="webkitExitFullscreen"
}else{if(typeof document.webkitCancelFullScreen==="function"){o="webkitCancelFullScreen"
}else{if(typeof document.mozCancelFullScreen==="function"){o="mozCancelFullScreen"
}else{if(typeof document.msExitFullscreen==="function"){o="msExitFullscreen"}}}}}if(typeof document[o]==="function"){document[o].call(document)
}};d.requestFullscreen=function(n){var o;if(typeof n.requestFullscreen==="function"){o="requestFullscreen"
}else{if(typeof n.webkitRequestFullscreen==="function"){o="webkitRequestFullscreen"
}else{if(typeof n.webkitRequestFullScreen==="function"){o="webkitRequestFullScreen"
}else{if(typeof n.mozRequestFullScreen==="function"){o="mozRequestFullScreen"}else{if(typeof n.msRequestFullscreen==="function"){o="msRequestFullscreen"
}}}}}if(typeof n[o]==="function"){n[o].call(n)}};d.mode=b.STANDARD;c.exports=d},{"./../consts/modes":197,"./../events/types":201,"@marcom/ac-dom-events/addEventListener":188,"@marcom/ac-event-emitter-micro":33}],199:[function(c,d,a){var b=c("./ios");
var f=c("./desktop");d.exports={create:function(){var g=f;if("webkitEnterFullscreen" in document.createElement("video")&&!("webkitRequestFullScreen" in document.createElement("div"))){g=b
}return g}}},{"./desktop":198,"./ios":200}],200:[function(f,d,h){var g=f("@marcom/ac-dom-events/addEventListener");
var m=f("@marcom/ac-event-emitter-micro").EventEmitterMicro;var a=f("./../events/types");
var c=f("./../consts/modes");var l;b();function b(){g(document,"webkitbeginfullscreen",k,true);
g(document,"webkitendfullscreen",j,true)}function k(n){i.trigger(a.ENTERFULLSCREEN,n)
}function j(n){l=undefined;i.trigger(a.EXITFULLSCREEN,n)}var i=new m();i.fullscreenEnabled=function(n){return !!(n.webkitSupportsFullscreen)
};i.fullscreenElement=function(){return l};i.exitFullscreen=function(n){if(n&&typeof n.webkitExitFullscreen==="function"){n.webkitExitFullscreen()
}};i.requestFullscreen=function(n){if(typeof n.webkitEnterFullscreen==="function"){n.webkitEnterFullscreen()
}};i.mode=c.IOS;d.exports=i},{"./../consts/modes":197,"./../events/types":201,"@marcom/ac-dom-events/addEventListener":188,"@marcom/ac-event-emitter-micro":33}],201:[function(b,c,a){c.exports={ENTERFULLSCREEN:"enterfullscreen",EXITFULLSCREEN:"exitfullscreen"}
},{}],202:[function(c,b,d){var i=c("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var h=c("./delegate/factory");var a="Error: Element missing. ac-fullscreen requires an element to be specified";
var f=h.create();function j(){throw new Error(a)}var g={};g.requestFullscreen=function(k){if(!k){j()
}return f.requestFullscreen(k)};g.fullscreenEnabled=function(k){if(!k){j()}return f.fullscreenEnabled(k)
};g.fullscreenElement=function(){return f.fullscreenElement()};g.exitFullscreen=function(k){if(!k){j()
}return f.exitFullscreen(k)};g.getMode=function(){return f.mode};g.on=function(){return f.on.apply(f,arguments)
};g.off=function(){return f.off.apply(f,arguments)};g.once=function(){return f.once.apply(f,arguments)
};b.exports=g},{"./delegate/factory":199,"@marcom/ac-event-emitter-micro":33}],203:[function(b,c,a){arguments[4][11][0].apply(a,arguments)
},{dup:11}],204:[function(b,c,a){arguments[4][12][0].apply(a,arguments)},{dup:12}],205:[function(b,c,a){arguments[4][62][0].apply(a,arguments)
},{"./internal/KeyEvent":206,"@marcom/ac-dom-events/utils/addEventListener":203,"@marcom/ac-dom-events/utils/removeEventListener":204,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-object/create":213,dup:62}],206:[function(b,c,a){arguments[4][64][0].apply(a,arguments)
},{dup:64}],207:[function(b,c,a){arguments[4][150][0].apply(a,arguments)},{dup:150,qs:208}],208:[function(b,c,a){arguments[4][151][0].apply(a,arguments)
},{"./parse":209,"./stringify":210,dup:151}],209:[function(b,c,a){arguments[4][152][0].apply(a,arguments)
},{"./utils":211,dup:152}],210:[function(b,c,a){arguments[4][153][0].apply(a,arguments)
},{"./utils":211,dup:153}],211:[function(b,c,a){arguments[4][154][0].apply(a,arguments)
},{dup:154}],212:[function(b,c,a){arguments[4][156][0].apply(a,arguments)},{"./extend":214,"@marcom/ac-polyfills/Array/isArray":100,dup:156}],213:[function(b,c,a){arguments[4][27][0].apply(a,arguments)
},{dup:27}],214:[function(b,c,a){arguments[4][28][0].apply(a,arguments)},{"@marcom/ac-polyfills/Array/prototype.forEach":101,dup:28}],215:[function(b,c,a){arguments[4][164][0].apply(a,arguments)
},{"@marcom/ac-url/joinSearchParams":207,dup:164}],216:[function(b,c,a){c.exports={SharedInstance:b("./ac-shared-instance/SharedInstance")}
},{"./ac-shared-instance/SharedInstance":217}],217:[function(d,h,c){var i=window,g="AC",a="SharedInstance",f=i[g];
var b=(function(){var j={};return{get:function(l,k){var m=null;if(j[l]&&j[l][k]){m=j[l][k]
}return m},set:function(m,k,l){if(!j[m]){j[m]={}}if(typeof l==="function"){j[m][k]=new l()
}else{j[m][k]=l}return j[m][k]},share:function(m,k,l){var n=this.get(m,k);if(!n){n=this.set(m,k,l)
}return n},remove:function(l,k){var m=typeof k;if(m==="string"||m==="number"){if(!j[l]||!j[l][k]){return
}j[l][k]=null;return}if(j[l]){j[l]=null}}}}());if(!f){f=i[g]={}}if(!f[a]){f[a]=b
}h.exports=f[a]},{}],218:[function(c,f,b){var a=c("@marcom/ac-shared-instance").SharedInstance;
var g="ac-raf-emitter-id-generator:sharedRAFEmitterIDGeneratorInstance",d="1.0.3";
var h=function(){this._currentID=0};h.prototype.getNewID=function(){this._currentID++;
return"raf:"+this._currentID};f.exports=a.share(g,d,h)},{"@marcom/ac-shared-instance":216}],219:[function(b,c,a){arguments[4][216][0].apply(a,arguments)
},{"./ac-shared-instance/SharedInstance":220,dup:216}],220:[function(b,c,a){arguments[4][217][0].apply(a,arguments)
},{dup:217}],221:[function(b,d,a){b("@marcom/ac-polyfills/performance/now");var f;
function c(g){g=g||{};this._reset();this._willRun=false;this._totalSubscribeCount=-1;
this._requestAnimationFrame=window.requestAnimationFrame;this._cancelAnimationFrame=window.cancelAnimationFrame;
this._boundOnAnimationFrame=this._onAnimationFrame.bind(this);this._boundOnExternalAnimationFrame=this._onExternalAnimationFrame.bind(this)
}f=c.prototype;f.subscribe=function(g,h){this._totalSubscribeCount++;if(!this._nextFrameSubscribers[g.id]){if(h){this._nextFrameSubscribersOrder.unshift(g.id)
}else{this._nextFrameSubscribersOrder.push(g.id)}this._nextFrameSubscribers[g.id]=g;
this._nextFrameSubscriberArrayLength++;this._nextFrameSubscriberCount++;this._run()
}return this._totalSubscribeCount};f.unsubscribe=function(g){if(!this._nextFrameSubscribers[g.id]){return false
}this._nextFrameSubscribers[g.id]=null;this._nextFrameSubscriberCount--;if(this._nextFrameSubscriberCount===0){this._cancel()
}return true};f.trigger=function(j,h){var g;for(g=0;g<this._subscriberArrayLength;
g++){if(this._subscribers[this._subscribersOrder[g]]!==null&&this._subscribers[this._subscribersOrder[g]]._didDestroy===false){this._subscribers[this._subscribersOrder[g]].trigger(j,h)
}}};f.destroy=function(){var g=this._cancel();this._subscribers=null;this._subscribersOrder=null;
this._nextFrameSubscribers=null;this._nextFrameSubscribersOrder=null;this._rafData=null;
this._boundOnAnimationFrame=null;this._onExternalAnimationFrame=null;return g};
f.useExternalAnimationFrame=function(g){if(typeof g!=="boolean"){return}var h=this._isUsingExternalAnimationFrame;
if(g&&this._animationFrame){this._cancelAnimationFrame.call(window,this._animationFrame);
this._animationFrame=null}if(this._willRun&&!g&&!this._animationFrame){this._animationFrame=this._requestAnimationFrame.call(window,this._boundOnAnimationFrame)
}this._isUsingExternalAnimationFrame=g;if(g){return this._boundOnExternalAnimationFrame
}return h||false};f._run=function(){if(!this._willRun){this._willRun=true;if(this.lastFrameTime===0){this.lastFrameTime=performance.now()
}this._animationFrameActive=true;if(!this._isUsingExternalAnimationFrame){this._animationFrame=this._requestAnimationFrame.call(window,this._boundOnAnimationFrame)
}return true}};f._cancel=function(){var g=false;if(this._animationFrameActive){if(this._animationFrame){this._cancelAnimationFrame.call(window,this._animationFrame);
this._animationFrame=null}this._animationFrameActive=false;this._willRun=false;
g=true}if(!this._isRunning){this._reset()}return g};f._onSubscribersAnimationFrameStart=function(h){var g;
for(g=0;g<this._subscriberArrayLength;g++){if(this._subscribers[this._subscribersOrder[g]]!==null&&this._subscribers[this._subscribersOrder[g]]._didDestroy===false){this._subscribers[this._subscribersOrder[g]]._onAnimationFrameStart(h)
}}};f._onSubscribersAnimationFrameEnd=function(h){var g;for(g=0;g<this._subscriberArrayLength;
g++){if(this._subscribers[this._subscribersOrder[g]]!==null&&this._subscribers[this._subscribersOrder[g]]._didDestroy===false){this._subscribers[this._subscribersOrder[g]]._onAnimationFrameEnd(h)
}}};f._onAnimationFrame=function(g){this._subscribers=this._nextFrameSubscribers;
this._subscribersOrder=this._nextFrameSubscribersOrder;this._subscriberArrayLength=this._nextFrameSubscriberArrayLength;
this._subscriberCount=this._nextFrameSubscriberCount;this._nextFrameSubscribers={};
this._nextFrameSubscribersOrder=[];this._nextFrameSubscriberArrayLength=0;this._nextFrameSubscriberCount=0;
this._isRunning=true;this._willRun=false;this._didRequestNextRAF=false;this._rafData.delta=g-this.lastFrameTime;
this.lastFrameTime=g;this._rafData.fps=0;if(this._rafData.delta>=1000){this._rafData.delta=0
}if(this._rafData.delta!==0){this._rafData.fps=1000/this._rafData.delta}this._rafData.time=g;
this._rafData.naturalFps=this._rafData.fps;this._rafData.timeNow=Date.now();this._onSubscribersAnimationFrameStart(this._rafData);
this.trigger("update",this._rafData);this.trigger("external",this._rafData);this.trigger("draw",this._rafData);
this._onSubscribersAnimationFrameEnd(this._rafData);if(!this._willRun){this._reset()
}};f._onExternalAnimationFrame=function(g){if(!this._isUsingExternalAnimationFrame){return
}this._onAnimationFrame(g)};f._reset=function(){this._rafData={time:0,delta:0,fps:0,naturalFps:0,timeNow:0};
this._subscribers={};this._subscribersOrder=[];this._subscriberArrayLength=0;this._subscriberCount=0;
this._nextFrameSubscribers={};this._nextFrameSubscribersOrder=[];this._nextFrameSubscriberArrayLength=0;
this._nextFrameSubscriberCount=0;this._didEmitFrameData=false;this._animationFrame=null;
this._animationFrameActive=false;this._isRunning=false;this._shouldReset=false;
this.lastFrameTime=0};d.exports=c},{"@marcom/ac-polyfills/performance/now":108}],222:[function(c,g,b){var a=c("@marcom/ac-shared-instance").SharedInstance;
var h="ac-raf-executor:sharedRAFExecutorInstance",f="2.0.1";var d=c("./RAFExecutor");
g.exports=a.share(h,f,d)},{"./RAFExecutor":221,"@marcom/ac-shared-instance":219}],223:[function(f,g,d){var i;
var h=f("@marcom/ac-event-emitter-micro").EventEmitterMicro;var c=f("@marcom/ac-raf-executor/sharedRAFExecutorInstance");
var b=f("@marcom/ac-raf-emitter-id-generator/sharedRAFEmitterIDGeneratorInstance");
function a(j){j=j||{};h.call(this);this.id=b.getNewID();this.executor=j.executor||c;
this._reset();this._willRun=false;this._didDestroy=false}i=a.prototype=Object.create(h.prototype);
i.run=function(){if(!this._willRun){this._willRun=true}return this._subscribe()
};i.cancel=function(){this._unsubscribe();if(this._willRun){this._willRun=false
}this._reset()};i.destroy=function(){var j=this.willRun();this.cancel();this.executor=null;
h.prototype.destroy.call(this);this._didDestroy=true;return j};i.willRun=function(){return this._willRun
};i.isRunning=function(){return this._isRunning};i._subscribe=function(){return this.executor.subscribe(this)
};i._unsubscribe=function(){return this.executor.unsubscribe(this)};i._onAnimationFrameStart=function(j){this._isRunning=true;
this._willRun=false;if(!this._didEmitFrameData){this._didEmitFrameData=true;this.trigger("start",j)
}};i._onAnimationFrameEnd=function(j){if(!this._willRun){this.trigger("stop",j);
this._reset()}};i._reset=function(){this._didEmitFrameData=false;this._isRunning=false
};g.exports=a},{"@marcom/ac-event-emitter-micro":33,"@marcom/ac-raf-emitter-id-generator/sharedRAFEmitterIDGeneratorInstance":218,"@marcom/ac-raf-executor/sharedRAFExecutorInstance":222}],224:[function(b,c,a){var d=b("./SingleCallRAFEmitter");
var g=function(h){this.rafEmitter=new d();this.rafEmitter.on(h,this._onRAFExecuted.bind(this));
this.requestAnimationFrame=this.requestAnimationFrame.bind(this);this.cancelAnimationFrame=this.cancelAnimationFrame.bind(this);
this._frameCallbacks=[];this._nextFrameCallbacks=[];this._currentFrameID=-1;this._cancelFrameIdx=-1;
this._frameCallbackLength=0;this._nextFrameCallbacksLength=0;this._frameCallbackIteration=0
};var f=g.prototype;f.requestAnimationFrame=function(h){this._currentFrameID=this.rafEmitter.run();
this._nextFrameCallbacks.push(this._currentFrameID,h);this._nextFrameCallbacksLength+=2;
return this._currentFrameID};f.cancelAnimationFrame=function(h){this._cancelFrameIdx=this._nextFrameCallbacks.indexOf(h);
if(this._cancelFrameIdx===-1){return}this._nextFrameCallbacks.splice(this._cancelFrameIdx,2);
this._nextFrameCallbacksLength-=2;if(this._nextFrameCallbacksLength===0){this.rafEmitter.cancel()
}};f._onRAFExecuted=function(h){this._frameCallbacks=this._nextFrameCallbacks;this._frameCallbackLength=this._nextFrameCallbacksLength;
this._nextFrameCallbacks=[];this._nextFrameCallbacksLength=0;for(this._frameCallbackIteration=0;
this._frameCallbackIteration<this._frameCallbackLength;this._frameCallbackIteration+=2){this._frameCallbacks[this._frameCallbackIteration+1](h.time,h)
}};c.exports=g},{"./SingleCallRAFEmitter":226}],225:[function(b,c,a){var g=b("./RAFInterface");
var f=function(){this.events={}};var d=f.prototype;d.requestAnimationFrame=function(h){if(!this.events[h]){this.events[h]=new g(h)
}return this.events[h].requestAnimationFrame};d.cancelAnimationFrame=function(h){if(!this.events[h]){this.events[h]=new g(h)
}return this.events[h].cancelAnimationFrame};c.exports=new f()},{"./RAFInterface":224}],226:[function(c,d,b){var a=c("./RAFEmitter");
var f=function(h){a.call(this,h)};var g=f.prototype=Object.create(a.prototype);
g._subscribe=function(){return this.executor.subscribe(this,true)};d.exports=f},{"./RAFEmitter":223}],227:[function(b,c,a){var d=b("./RAFInterfaceController");
c.exports=d.cancelAnimationFrame("draw")},{"./RAFInterfaceController":225}],228:[function(b,c,a){var d=b("./RAFInterfaceController");
c.exports=d.requestAnimationFrame("draw")},{"./RAFInterfaceController":225}],229:[function(b,c,a){c.exports={getContentDimensions:b("./getContentDimensions"),getDimensions:b("./getDimensions"),getPagePosition:b("./getPagePosition"),getPercentInViewport:b("./getPercentInViewport"),getPixelsInViewport:b("./getPixelsInViewport"),getPosition:b("./getPosition"),getScrollX:b("./getScrollX"),getScrollY:b("./getScrollY"),getViewportPosition:b("./getViewportPosition"),isInViewport:b("./isInViewport")}
},{"./getContentDimensions":230,"./getDimensions":231,"./getPagePosition":232,"./getPercentInViewport":233,"./getPixelsInViewport":234,"./getPosition":235,"./getScrollX":236,"./getScrollY":237,"./getViewportPosition":238,"./isInViewport":239}],230:[function(d,f,c){var b=d("./utils/getBoundingClientRect");
f.exports=function a(g,i){var h=1;if(i){h=b(g).width/g.offsetWidth}return{width:g.scrollWidth*h,height:g.scrollHeight*h}
}},{"./utils/getBoundingClientRect":240}],231:[function(d,f,c){var b=d("./utils/getBoundingClientRect");
f.exports=function a(g,i){var h;if(i){h=b(g);return{width:h.width,height:h.height}
}return{width:g.offsetWidth,height:g.offsetHeight}}},{"./utils/getBoundingClientRect":240}],232:[function(g,h,f){var c=g("./getDimensions");
var d=g("./utils/getBoundingClientRect");var b=g("./getScrollX");var a=g("./getScrollY");
h.exports=function i(j,o){var l;var n;var m;var k;if(o){l=d(j);n=b();m=a();return{top:l.top+m,right:l.right+n,bottom:l.bottom+m,left:l.left+n}
}k=c(j,o);l={top:j.offsetTop,left:j.offsetLeft,width:k.width,height:k.height};while((j=j.offsetParent)){l.top+=j.offsetTop;
l.left+=j.offsetLeft}return{top:l.top,right:l.left+l.width,bottom:l.top+l.height,left:l.left}
}},{"./getDimensions":231,"./getScrollX":236,"./getScrollY":237,"./utils/getBoundingClientRect":240}],233:[function(c,f,b){var a=c("./getDimensions");
var g=c("./getPixelsInViewport");f.exports=function d(j,k){var i=g(j,k);var h=a(j,k).height;
return(i/h)}},{"./getDimensions":231,"./getPixelsInViewport":234}],234:[function(c,d,b){var a=c("./getViewportPosition");
d.exports=function f(h,k){var j=document.documentElement.clientHeight;var g=a(h,k);
var i;if(g.top>=j||g.bottom<=0){return 0}i=(g.bottom-g.top);if(g.top<0){i+=g.top
}if(g.bottom>j){i-=g.bottom-j}return i}},{"./getViewportPosition":238}],235:[function(d,f,c){var a=d("./getDimensions");
var b=d("./utils/getBoundingClientRect");f.exports=function g(i,l){var k;var h;
var j;if(l){k=b(i);if(i.offsetParent){h=b(i.offsetParent);k.top-=h.top;k.left-=h.left
}}else{j=a(i,l);k={top:i.offsetTop,left:i.offsetLeft,width:j.width,height:j.height}
}return{top:k.top,right:k.left+k.width,bottom:k.top+k.height,left:k.left}}},{"./getDimensions":231,"./utils/getBoundingClientRect":240}],236:[function(b,c,a){arguments[4][77][0].apply(a,arguments)
},{dup:77}],237:[function(b,c,a){arguments[4][78][0].apply(a,arguments)},{dup:78}],238:[function(g,h,f){var i=g("./getPagePosition");
var d=g("./utils/getBoundingClientRect");var c=g("./getScrollX");var b=g("./getScrollY");
h.exports=function a(k,n){var j;var m;var l;if(n){j=d(k);return{top:j.top,right:j.right,bottom:j.bottom,left:j.left}
}j=i(k);m=c();l=b();return{top:j.top-l,right:j.right-m,bottom:j.bottom-l,left:j.left-m}
}},{"./getPagePosition":232,"./getScrollX":236,"./getScrollY":237,"./utils/getBoundingClientRect":240}],239:[function(b,d,a){var g=b("./getPixelsInViewport");
var c=b("./getPercentInViewport");d.exports=function f(j,k,h){var i;h=h||0;if(typeof h==="string"&&h.slice(-2)==="px"){h=parseInt(h,10);
i=g(j,k)}else{i=c(j,k)}return(i>0&&i>=h)}},{"./getPercentInViewport":233,"./getPixelsInViewport":234}],240:[function(c,d,b){d.exports=function a(f){var g=f.getBoundingClientRect();
return{top:g.top,right:g.right,bottom:g.bottom,left:g.left,width:g.width||g.right-g.left,height:g.height||g.bottom-g.top}
}},{}],241:[function(g,d,i){var m=g("@marcom/ac-event-emitter-micro");var a=g("@marcom/ac-dom-metrics");
var b=g("@marcom/ac-keyboard/Keyboard");var p={num:37,string:"ArrowLeft"};var q={num:38,string:"ArrowUp"};
var n={num:39,string:"ArrowRight"};var k={num:40,string:"ArrowDown"};var l=[p,n,k,n];
var f=function(s){if(s.which){return s.which}var t=(s.key)?s.key:s.code;var u=0;
var r=l.length;for(;u<r;u++){if(l[u].string===t){return l[u].num}}return -1};var c={min:0,max:1,step:1,value:0,orientation:"horizontal",renderedPosition:false,template:'<div class="ac-slider-runnable-track">\n\t<div class="ac-slider-thumb"></div>\n</div>',keyboardMaxStepPercentage:0.05,keyboardStepMultiplier:1.25};
var o=Object.keys(c);var h=function(s,r){this.options=Object.assign({},c,r);this.model=Object.create(this.options);
this.el=s;var t=(this.options.keyboardContext!==undefined)?this.options.keyboardContext:this.el;
if(t!==null){this._keyboard=new b(t);this._keyDown={}}s.className+=" ac-slider-container";
s.innerHTML=this.model.template;m.EventEmitterMicro.call(this);this.initialize()
};h.prototype=Object.create(m.EventEmitterMicro.prototype);var j=h.prototype;j.addEventListeners=function(){this.addEventListener(this.el,"mousedown",this.onMouseDown);
this.addEventListener(this.el,"touchstart",this.onTouchStart);this.addEventListener(this.el,"mouseover",this.onMouseOver);
this.addEventListener(this.el,"mouseleave",this.onMouseLeave);this.addEventListener(this.el,"touchend",this.onTouchEnd);
this.addEventListener(document,"touchend",this.onMouseUp);if(this._keyboard){if(this.model.orientation==="horizontal"){this._keyboard.onDown(n.num,this.stepUp);
this._keyboard.onDown(p.num,this.stepDown)}else{this._keyboard.onDown(k.num,this.stepDown);
this._keyboard.onDown(q.num,this.stepUp)}}};j.addEventListener=function(r,s,t){r.addEventListener(s,t)
};j.bindMethods=function(){this.stepDown=this.stepDown.bind(this);this.stepUp=this.stepUp.bind(this);
this._triggerRelease=this._triggerRelease.bind(this);this._preventDefault=this._preventDefault.bind(this);
this.onMouseDown=this.bindMethod(this.onMouseDown,this);this.onTouchStart=this.bindMethod(this.onTouchStart,this);
this.onMouseOver=this.bindMethod(this.onMouseOver,this);this.onMouseLeave=this.bindMethod(this.onMouseLeave,this);
this.onTouchEnd=this.bindMethod(this.onTouchEnd,this);this.onMouseUp=this.bindMethod(this.onMouseUp,this);
this.onMouseMove=this.bindMethod(this.onMouseMove,this);this.onTouchMove=this.bindMethod(this.onTouchMove,this)
};j.bindMethod=function(s,r){return s.bind(r)};j.correctValueMinMax=function(t,s,r){if(t>r){t=r
}if(t<s){t=s}return t};j.calculateStepsToValue=function(s,r){return Math.abs(s-r)
};j.calculateMaxSteps=function(s,r){return Math.abs(r-s)};j.calculateStepsEqualToPercentage=function(s,r){return(s/100)*r
};j.calculateNextStepInRange=function(x,s,r,w){var u=this.calculateMaxSteps(s,r);
var v=this.calculateStepsToValue(x,s);var t=s+(Math.floor(u/w)*w);x=Math.min(t,s+Math.round(v/w)*w);
return x};j.dispatchEvent=function(r,s){r.dispatchEvent(new CustomEvent(s))};j.disableUserControls=function(){this.removeEventListeners()
};j.enableUserControls=function(){this.addEventListeners()};j.getNextValue=function(u,s,r,t){u=this.correctValueMinMax(u,s,r);
if(t!=="auto"){u=this.calculateNextStepInRange(u,s,r,t)}return u};j.getOrientation=function(){return this.model.orientation
};j.getValue=function(){return this.model.value};j.getMin=function(){return this.model.min
};j.getMax=function(){return this.model.max};j.getStep=function(){return this.model.step
};j.getClientXValue=function(x,y){var r=this.getClientXFromEvent(x);var z=(y!==null)?a.getDimensions(y||this.thumbElement):{width:0,height:0};
var A=a.getDimensions(this.runnableTrackElement);var t=r-this.runnableTrackElement.getBoundingClientRect().left-Math.round(z.width/2);
var w=A.width-z.width;var s=t/(w)*100;var u=this.calculateMaxSteps(this.getMin(),this.getMax());
var v=this.calculateStepsEqualToPercentage(s,u);return this.getMin()+v};j.getClientYValue=function(x){var r=this.getClientYFromEvent(x);
var z=a.getDimensions(this.thumbElement);var A=a.getDimensions(this.runnableTrackElement);
var s=a.getViewportPosition(this.runnableTrackElement,this.model.renderedPosition);
var w=A.height-z.height;var y=w-(r-s.top-(z.height/2));var t=y/(A.height-z.height)*100;
var u=this.calculateMaxSteps(this.model.min,this.model.max);var v=this.calculateStepsEqualToPercentage(t,u);
return this.model.min+v};j.getClientValue=function(s){s=s.originalEvent||s;var r;
if(this.model.orientation==="horizontal"){r=this.getClientXValue(s)}else{r=this.getClientYValue(s)
}return r};j.getClientXFromEvent=function(r){return r.touches?r.touches[0].clientX:r.clientX
};j.getClientYFromEvent=function(r){return r.touches?r.touches[0].clientY:r.clientY
};j.initialize=function(){this.setNodeReferences();this.setValue(this.model.value);
this.bindMethods();this.addEventListeners()};j.onMouseLeave=function(){this.preventDocumentMouseUpDispatch=false
};j.onMouseDown=function(s){var r=this.getClientValue(s);this.addEventListener(document,"mouseup",this.onMouseUp);
this.addEventListener(document,"mousemove",this.onMouseMove);this.trigger("grab",this.getValue());
this.setValue(r)};j.onMouseUp=function(){this.removeEventListener(document,"mouseup",this.onMouseUp);
this.removeEventListener(document,"mousemove",this.onMouseMove);this.trigger("release",this.getValue());
if(!this.preventDocumentMouseUpDispatch){this.dispatchEvent(this.el,"mouseup")}};
j.onMouseOver=function(){this.preventDocumentMouseUpDispatch=true};j.onTouchEnd=function(){this.removeEventListener(document,"touchend",this.onTouchEnd);
this.removeEventListener(document,"touchmove",this.onTouchMove);this.trigger("release",this.getValue());
if(!this.preventDocumentMouseUpDispatch){this.dispatchEvent(this.el,"touchend")
}};j.onTouchStart=function(s){var r=this.getClientValue(s);this.addEventListener(document,"touchend",this.onMouseUp);
this.addEventListener(document,"touchmove",this.onTouchMove);this.trigger("grab",this.getValue());
this.setValue(r)};j.onMouseMove=function(s){var r=this.getClientValue(s);this.setValue(r)
};j.onTouchMove=function(s){if(s.preventDefault){s.preventDefault()}var r=this.getClientValue(s);
this.setValue(r)};j.getElementOrientationOffsetValue=function(s,r){if(r==="horizontal"){return a.getDimensions(s).width
}return a.getDimensions(s).height};j.getAvailableRunnableTrack=function(t,r){var s=this.getElementOrientationOffsetValue(this.thumbElement,r);
return t-s};j.getPercentageByValue=function(s,r){s=this.calculateStepsToValue(s,this.getMin());
r=this.calculateMaxSteps(this.getMin(),this.getMax());return(s/r)*100};j.getPercentageOfRunnableTrack=function(v){var s=this.getOrientation();
var w=this.getElementOrientationOffsetValue(this.runnableTrackElement,s);var r=this.getAvailableRunnableTrack(w,s);
var u=this.getPercentageByValue(v,this.getMax());var t=(u/100)*r;return(t/w)*100
};j.onChange=function(s){var r=this.getPercentageOfRunnableTrack(s);if(isNaN(r)){return
}if(this.getOrientation()==="horizontal"){this.thumbElement.style.left=r+"%"}else{this.thumbElement.style.bottom=r+"%"
}this.trigger("change",this.getValue())};j.removeEventListeners=function(){this.removeEventListener(this.el,"mousedown",this.onMouseDown);
this.removeEventListener(this.el,"touchstart",this.onTouchStart);this.removeEventListener(this.el,"mouseover",this.onMouseOver);
this.removeEventListener(this.el,"mouseleave",this.onMouseLeave);this.removeEventListener(this.el,"touchend",this.onTouchEnd);
this.removeEventListener(document,"touchend",this.onMouseUp)};j.removeEventListener=function(r,s,t){r.removeEventListener(s,t)
};j.setNodeReferences=function(){this.runnableTrackElement=this.el.querySelector(".ac-slider-runnable-track");
this.thumbElement=this.el.querySelector(".ac-slider-thumb")};j.setOrientation=function(r){this.set("orientation",r)
};j._triggerRelease=function(r){this._preventDefault(r);this.trigger("release",this.getValue());
this._keyDown[f(r)]=0};j._preventDefault=function(r){r.preventDefault();r.stopPropagation()
};j._step=function(s,r){this._preventDefault(s);this.el.focus();var t=this._keyDown[f(s)]||0;
if(!t){this.trigger("grab",this.getValue());t=this.getStep();t=(t!=="auto")?t:this._cachedMaxStep;
if(!r){t*=-1}this._keyboard.onceUp(f(s),this._triggerRelease)}else{if(Math.abs(this._keyDown[f(s)])<(Math.abs(this.model.max*this.model.keyboardMaxStepPercentage))){t*=this.model.keyboardStepMultiplier
}}this._keyDown[f(s)]=t;this.setValue(this.getValue()+t)};j.stepUp=function(r){this._step(r,true)
};j.stepDown=function(r){this._step(r,false)};j.setValue=function(r){r=this.getNextValue(r,this.getMin(),this.getMax(),this.getStep());
this.set("value",r);this.el.setAttribute("aria-valuenow",r);this.onChange(r)};j.setMin=function(r){this.set("min",r);
this.el.setAttribute("aria-valuemin",r)};j.setMax=function(r){this.set("max",r);
this.el.setAttribute("aria-valuemax",r);this._cachedMaxStep=r/100};j.setStep=function(r){this.set("step",r)
};j.set=function(r,t){if(o.indexOf(r)>-1&&this.model[r]!==t){var s=this.model[r];
this.model[r]=t;this.trigger("change:model:"+r,{previous:s,current:t})}};j._removeEventListeners=function(){this.removeEventListener(this.el,"mousedown",this.onMouseDown);
this.removeEventListener(this.el,"touchstart",this.onTouchStart);this.removeEventListener(this.el,"mouseover",this.onMouseOver);
this.removeEventListener(this.el,"mouseleave",this.onMouseLeave);this.removeEventListener(this.el,"touchend",this.onTouchEnd);
this.removeEventListener(document,"touchend",this.onMouseUp);if(this.model.orientation==="horizontal"){this._keyboard.offDown(n.num,this.stepUp);
this._keyboard.offDown(p.num,this.stepDown);this._keyboard.offUp(p.num,this._triggerRelease);
this._keyboard.offUp(n.num,this._triggerRelease)}else{this._keyboard.offDown(k.num,this.stepDown);
this._keyboard.offDown(q.num,this.stepUp);this._keyboard.offUp(k.num,this._triggerRelease);
this._keyboard.offUp(q.num,this._triggerRelease)}};j.destroy=function(){this._removeEventListeners();
if(this._keyboard){this._keyboard.destroy()}m.EventEmitterMicro.prototype.destroy.call(this)
};d.exports=h},{"@marcom/ac-dom-metrics":229,"@marcom/ac-event-emitter-micro":33,"@marcom/ac-keyboard/Keyboard":205}],242:[function(b,c,a){c.exports.Slider=b("./Slider")
},{"./Slider":241}],243:[function(b,c,a){c.exports=b("./lib/")},{"./lib/":244}],244:[function(b,c,a){arguments[4][151][0].apply(a,arguments)
},{"./parse":245,"./stringify":246,dup:151}],245:[function(b,c,a){var f=b("./utils");
var d={delimiter:"&",depth:5,arrayLimit:20,parameterLimit:1000};d.parseValues=function(m,q){var k={};
var j=m.split(q.delimiter,q.parameterLimit===Infinity?undefined:q.parameterLimit);
for(var l=0,o=j.length;l<o;++l){var g=j[l];var n=g.indexOf("]=")===-1?g.indexOf("="):g.indexOf("]=")+1;
if(n===-1){k[f.decode(g)]=""}else{var p=f.decode(g.slice(0,n));var h=f.decode(g.slice(n+1));
if(!k.hasOwnProperty(p)){k[p]=h}else{k[p]=[].concat(k[p]).concat(h)}}}return k};
d.parseObject=function(l,n,k){if(!l.length){return n}var g=l.shift();var m={};if(g==="[]"){m=[];
m=m.concat(d.parseObject(l,n,k))}else{var j=g[0]==="["&&g[g.length-1]==="]"?g.slice(1,g.length-1):g;
var i=parseInt(j,10);var h=""+i;if(!isNaN(i)&&g!==j&&h===j&&i>=0&&i<=k.arrayLimit){m=[];
m[i]=d.parseObject(l,n,k)}else{m[j]=d.parseObject(l,n,k)}}return m};d.parseKeys=function(j,n,g){if(!j){return
}var k=/^([^\[\]]*)/;var o=/(\[[^\[\]]*\])/g;var m=k.exec(j);if(Object.prototype.hasOwnProperty(m[1])){return
}var l=[];if(m[1]){l.push(m[1])}var h=0;while((m=o.exec(j))!==null&&h<g.depth){++h;
if(!Object.prototype.hasOwnProperty(m[1].replace(/\[|\]/g,""))){l.push(m[1])}}if(m){l.push("["+j.slice(m.index)+"]")
}return d.parseObject(l,n,g)};c.exports=function(k,p){if(k===""||k===null||typeof k==="undefined"){return{}
}p=p||{};p.delimiter=typeof p.delimiter==="string"||f.isRegExp(p.delimiter)?p.delimiter:d.delimiter;
p.depth=typeof p.depth==="number"?p.depth:d.depth;p.arrayLimit=typeof p.arrayLimit==="number"?p.arrayLimit:d.arrayLimit;
p.parameterLimit=typeof p.parameterLimit==="number"?p.parameterLimit:d.parameterLimit;
var l=typeof k==="string"?d.parseValues(k,p):k;var h={};var o=Object.keys(l);for(var j=0,m=o.length;
j<m;++j){var n=o[j];var g=d.parseKeys(n,l[n],p);h=f.merge(h,g)}return f.compact(h)
}},{"./utils":247}],246:[function(b,c,a){var f=b("./utils");var d={delimiter:"&",indices:true};
d.stringify=function(n,m,j){if(f.isBuffer(n)){n=n.toString()}else{if(n instanceof Date){n=n.toISOString()
}else{if(n===null){n=""}}}if(typeof n==="string"||typeof n==="number"||typeof n==="boolean"){return[encodeURIComponent(m)+"="+encodeURIComponent(n)]
}var h=[];if(typeof n==="undefined"){return h}var o=Object.keys(n);for(var l=0,g=o.length;
l<g;++l){var k=o[l];if(!j.indices&&Array.isArray(n)){h=h.concat(d.stringify(n[k],m,j))
}else{h=h.concat(d.stringify(n[k],m+"["+k+"]",j))}}return h};c.exports=function(n,j){j=j||{};
var h=typeof j.delimiter==="undefined"?d.delimiter:j.delimiter;j.indices=typeof j.indices==="boolean"?j.indices:d.indices;
var m=[];if(typeof n!=="object"||n===null){return""}var o=Object.keys(n);for(var l=0,g=o.length;
l<g;++l){var k=o[l];m=m.concat(d.stringify(n[k],k,j))}return m.join(h)}},{"./utils":247}],247:[function(b,c,a){var d={};
a.arrayToObject=function(h){var j={};for(var g=0,f=h.length;g<f;++g){if(typeof h[g]!=="undefined"){j[g]=h[g]
}}return j};a.merge=function(m,l){if(!l){return m}if(typeof l!=="object"){if(Array.isArray(m)){m.push(l)
}else{m[l]=true}return m}if(typeof m!=="object"){m=[m].concat(l);return m}if(Array.isArray(m)&&!Array.isArray(l)){m=a.arrayToObject(m)
}var i=Object.keys(l);for(var f=0,h=i.length;f<h;++f){var g=i[f];var j=l[g];if(!m[g]){m[g]=j
}else{m[g]=a.merge(m[g],j)}}return m};a.decode=function(g){try{return decodeURIComponent(g.replace(/\+/g," "))
}catch(f){return g}};a.compact=function(n,h){if(typeof n!=="object"||n===null){return n
}h=h||[];var m=h.indexOf(n);if(m!==-1){return h[m]}h.push(n);if(Array.isArray(n)){var f=[];
for(var k=0,g=n.length;k<g;++k){if(typeof n[k]!=="undefined"){f.push(n[k])}}return f
}var l=Object.keys(n);for(k=0,g=l.length;k<g;++k){var j=l[k];n[j]=a.compact(n[j],h)
}return n};a.isRegExp=function(f){return Object.prototype.toString.call(f)==="[object RegExp]"
};a.isBuffer=function(f){if(f===null||typeof f==="undefined"){return false}return !!(f.constructor&&f.constructor.isBuffer&&f.constructor.isBuffer(f))
}},{}],248:[function(b,c,a){c.exports={Link:b("./ac-social/Link"),Dialog:b("./ac-social/Dialog"),Focus:b("./ac-social/Focus"),Debug:b("./ac-social/Debug")}
},{"./ac-social/Debug":249,"./ac-social/Dialog":250,"./ac-social/Focus":251,"./ac-social/Link":252}],249:[function(c,d,b){var a=c("./NetworkActions");
function g(){this.types={};var h;for(h in a){if(a.hasOwnProperty(h)){f[h]=h;this.addType(h,a[h].getDialogDebugData.bind(a[h]))
}}}var f=g.prototype;f.create=function(h,j){j=j||{};var i=this.types[h];if(!i){return
}return i(j)};f.addType=function(h,i){this.types[h]=i;return this};f.removeType=function(){this.types[name]=null;
return this};d.exports=new g()},{"./NetworkActions":253}],250:[function(d,f,c){var a=d("./NetworkActions");
function b(){this.types={};var h;for(h in a){if(a.hasOwnProperty(h)){g[h]=h;this.addType(h,a[h].generateDialog.bind(a[h]))
}}}var g=b.prototype;g.create=function(h,j){j=j||{};var i=this.types[h];if(!i){return
}return i(j)};g.addType=function(h,i){this.types[h]=i;return this};g.removeType=function(){this.types[name]=null;
return this};f.exports=new b()},{"./NetworkActions":253}],251:[function(b,c,a){c.exports=function(g){if(window.getSelection){var f=window.getSelection();
var d=document.createRange();d.selectNodeContents(g);f.removeAllRanges();f.addRange(d)
}else{if(g.setSelectionRange){g.setSelectionRange(0,g.value.length)}else{if(document.body.createTextRange){var d=document.body.createTextRange();
d.moveToElementText(g);d.select()}}}}},{}],252:[function(f,g,c){var a=f("./NetworkActions"),b=f("./network-actions/DefaultNetworkAction");
function d(){this.types={};var j;for(j in a){if(a.hasOwnProperty(j)){h[j]=j;this.addType(j,a[j].generateLink.bind(a[j]))
}}}var h=d.prototype;h.create=function(j,l,i){l=l||{};var k=this.types[j];if(!k){return
}return k(l,i)};h.createFromAnchor=function(l){var j=l.getAttribute("data-network-action");
var k;for(k in a){if(a.hasOwnProperty(k)){if(j===a[k].id){a[k].enhanceLinkEngagement(l);
return}}}b.enhanceLinkEngagement(l)};h.addType=function(i,j){this.types[i]=j;return this
};h.removeType=function(){this.types[name]=null;return this};g.exports=new d()},{"./NetworkActions":253,"./network-actions/DefaultNetworkAction":254}],253:[function(d,c,g){var m=d("./network-actions/FacebookShare"),l=d("./network-actions/PinterestShare"),n=d("./network-actions/TumblrShare"),f=d("./network-actions/TwitterFavorite"),i=d("./network-actions/TwitterReply"),p=d("./network-actions/TwitterRetweet"),o=d("./network-actions/TwitterTweet"),k=d("./network-actions/WeiboShare"),b=d("./network-actions/QQWeiboShare"),j=d("./network-actions/QZoneShare"),h=d("./network-actions/RenrenShare"),a=d("./network-actions/EMailShare");
c.exports={FACEBOOK_SHARE:m,PINTEREST_SHARE:l,TUMBLR_SHARE:n,TWITTER_FAVORITE:f,TWITTER_REPLY:i,TWITTER_RETWEET:p,TWITTER_TWEET:o,WEIBO_SHARE:k,QQWEIBO_SHARE:b,QZONE_SHARE:j,RENREN_SHARE:h,EMAIL_SHARE:a}
},{"./network-actions/EMailShare":255,"./network-actions/FacebookShare":256,"./network-actions/PinterestShare":258,"./network-actions/QQWeiboShare":259,"./network-actions/QZoneShare":260,"./network-actions/RenrenShare":261,"./network-actions/TumblrShare":262,"./network-actions/TwitterFavorite":263,"./network-actions/TwitterReply":264,"./network-actions/TwitterRetweet":265,"./network-actions/TwitterTweet":266,"./network-actions/WeiboShare":267}],254:[function(c,d,a){var f=c("./NetworkAction");
var b=function(g){return g};d.exports=new f(b,{baseLinkPath:""})},{"./NetworkAction":257}],255:[function(c,d,a){var f=c("./NetworkAction");
var b=function(h){var g={url:h.url};if(h.title){g.subject=h.title}if(h.description){g.body=h.description+"\r\n\r\n"+h.url
}else{g.body=h.url}return g};d.exports=new f(b,{id:"email-share",baseLinkPath:"mailto:",preventDialog:true})
},{"./NetworkAction":257}],256:[function(c,d,a){var f=c("./NetworkAction");var b=function(g){return{u:g.url}
};d.exports=new f(b,{id:"facebook-share",baseLinkPath:"https://www.facebook.com/sharer/sharer.php",dialogDimensions:{width:555,height:368}})
},{"./NetworkAction":257}],257:[function(c,d,b){var a=c("qs");var g;var f=function(i,h){h=h||{};
this.baseLinkPath=h.baseLinkPath;if(h.dialogDimensions){this.dialogDimensions=h.dialogDimensions
}if(h.id){this.id=h.id}if(h.preventDialog){this.preventDialog=h.preventDialog}this.normalizeData=i
};g=f.prototype;g.dataAttributeName="network-action";g.id="network-action";g.normalizeData=function(h){return h
};g.dialogDimensions={width:500,height:500};g.generateLinkURL=function(k){var j=this.normalizeData(k),i=a.stringify(j),h=this.baseLinkPath;
if(i.length>0){h=h+"?"+i}return h};g.generateLink=function(j,i){var h=this.generateLinkURL(j);
i=i||document.createElement("A");i.setAttribute("href",h);i.setAttribute("target","_blank");
i.setAttribute("data-"+this.dataAttributeName,this.id);this.enhanceLinkEngagement(i,h);
return i};g.generateDialog=function(i){var h=this.generateLinkURL(i);this._triggerDialog(h)
};g.enhanceLinkEngagement=function(j,h){var i=this||g;h=h||j.getAttribute("href");
j.addEventListener("click",this._onLinkEngaged.bind(this,h))};g.getDialogOptions=function(){var j,k="status=1",h={width:this.dialogDimensions.width,height:this.dialogDimensions.height};
h.top=(window.screen.availHeight-h.height)/2;h.left=(window.screen.availWidth-h.width)/2;
for(j in h){if(h.hasOwnProperty(j)){k+=", "+j+"="+h[j]}}return k};g.getDialogDebugData=function(h){return{data:this.normalizeData(h),dialogUrl:this.generateLinkURL(h)}
};g._triggerDialog=function(h){if(this.preventDialog){window.location.href=h;return
}window.open(h,"_blank",this.getDialogOptions())};g._onLinkEngaged=function(h,i){i.preventDefault();
this._triggerDialog(h)};d.exports=f},{qs:243}],258:[function(c,d,a){var f=c("./NetworkAction");
var b=function(h){var g={url:h.url,description:h.description};if(h.media){g.media=h.media
}return g};d.exports=new f(b,{id:"pinterest-share",baseLinkPath:"http://www.pinterest.com/pin/create/button",dialogDimensions:{width:750,height:450}})
},{"./NetworkAction":257}],259:[function(c,d,a){var f=c("./NetworkAction");var b=function(g){return{url:g.url,title:g.title,pic:g.media}
};d.exports=new f(b,{id:"qq-weibo-share",baseLinkPath:"http://v.t.qq.com/share/share.php",dialogDimensions:{width:658,height:506}})
},{"./NetworkAction":257}],260:[function(c,d,a){var f=c("./NetworkAction");var b=function(g){return{url:g.url,title:g.title,pics:g.media,summary:g.description}
};d.exports=new f(b,{id:"qzone-share",baseLinkPath:"http://sns.qzone.qq.com/cgi-bin/qzshare/cgi_qzshare_onekey",dialogDimensions:{width:620,height:645}})
},{"./NetworkAction":257}],261:[function(c,d,a){var f=c("./NetworkAction");var b=function(g){return{url:g.url,title:g.title}
};d.exports=new f(b,{id:"renren-share",baseLinkPath:"http://www.connect.renren.com/share/sharer",dialogDimensions:{width:500,height:315}})
},{"./NetworkAction":257}],262:[function(c,d,a){var f=c("./NetworkAction");var b=function(h){var g={clickthru:h.url,caption:h.description};
if(h.media){g.source=h.media}return g};d.exports=new f(b,{id:"tumblr-share",baseLinkPath:"http://www.tumblr.com/share/photo",dialogDimensions:{width:450,height:432}})
},{"./NetworkAction":257}],263:[function(c,d,a){var f=c("./NetworkAction");var b=function(h){var g={tweet_id:h.messageId};
return g};d.exports=new f(b,{id:"twitter-favorite",baseLinkPath:"https://twitter.com/intent/favorite",dialogDimensions:{width:550,height:420}})
},{"./NetworkAction":257}],264:[function(c,d,a){var f=c("./NetworkAction");var b=function(h){var g={in_reply_to:h.messageId};
if(h.hashtags){g.hashtags=h.hashtags}return g};d.exports=new f(b,{id:"twitter-reply",baseLinkPath:"https://twitter.com/intent/tweet",dialogDimensions:{width:550,height:420}})
},{"./NetworkAction":257}],265:[function(c,d,a){var f=c("./NetworkAction");var b=function(h){var g={tweet_id:h.messageId};
return g};d.exports=new f(b,{id:"twitter-retweet",baseLinkPath:"https://twitter.com/intent/retweet",dialogDimensions:{width:550,height:420}})
},{"./NetworkAction":257}],266:[function(c,d,a){var f=c("./NetworkAction");var b=function(h){var g={url:h.url,text:h.description};
if(h.hashtags){g.hashtags=h.hashtags}return g};d.exports=new f(b,{id:"twitter-tweet",baseLinkPath:"https://twitter.com/intent/tweet",dialogDimensions:{width:550,height:420}})
},{"./NetworkAction":257}],267:[function(c,d,a){var f=c("./NetworkAction");var b=function(g){return{url:g.url,title:g.title,pic:g.media}
};d.exports=new f(b,{id:"weibo-share",baseLinkPath:"http://service.weibo.com/share/share.php",dialogDimensions:{width:650,height:426}})
},{"./NetworkAction":257}],268:[function(b,c,a){c.exports=function d(h,g,f){if(!g){return h
}f=f||/{([^{}]*)}/g;return h.replace(f,function(j,i){var k=g[i];return(typeof k==="string"||typeof k==="number"||typeof k==="boolean")?k:j
})}},{}],269:[function(b,c,a){var f=function(g){this.el=g};var d=f.prototype;d.on=function(){this.el.addEventListener.apply(this.el,arguments)
};d.off=function(){this.el.removeEventListener.apply(this.el,arguments)};d.once=function(i,h){var g=function(){h();
this.off(i,g)}.bind(this);this.on(i,g)};d.trigger=function(h,i){var g=new CustomEvent(h,i);
this.el.dispatchEvent(g)};c.exports=f},{}],270:[function(b,d,a){var h=b("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var g=function(){h.call(this)};var c=h.prototype;g.prototype=Object.create(c);var f=g.prototype;
f.constructor=g;f.once=function(j,l,k){if(k){var i=function(){l.apply(k,arguments)
};c.once.apply(this,[j,i])}else{c.once.apply(this,arguments)}};f.on=function(j,l,i){if(arguments.length>2){if(!this._boundListeners){this._boundListeners={}
}if(!this._boundListeners[j]){this._boundListeners[j]=[]}var k=l.bind(i);this._boundListeners[j].push([l,i,k]);
return c.on.call(this,j,k)}else{return c.on.apply(this,arguments)}};f.off=function(m,q,l){if(arguments.length>2){try{var o=this._boundListeners[m];
var k=0;var j=o.length;for(;k<j;k++){if(o[k][0]===q&&o[k][1]===l){var n=o.splice(k,1)[0];
return c.off.call(this,m,n[2])}}}catch(p){}}else{return c.off.apply(this,arguments)
}};f.destroy=function(){this._boundListeners=undefined;c.destroy.call(this)};d.exports=g
},{"@marcom/ac-event-emitter-micro":33}],271:[function(b,c,a){c.exports=b("./utils/urlOptimizer/OptimizeVideoUrl")
},{"./utils/urlOptimizer/OptimizeVideoUrl":324}],272:[function(r,d,E){var q=r("../event-emitter-shim/EventEmitterShim");
var z=r("../dom-emitter/DOMEmitterMicro");var j=r("../video/VideoFactory").create;
var D=r("@marcom/ac-useragent");var k=r("@marcom/ac-fullscreen");var m=r("../posterframe/PosterFrameFactory");
var v=r("@marcom/ac-feature/isRetina")();var l=r("@marcom/ac-feature/isDesktop")();
var u=r("@marcom/ac-feature/isHandheld")();var C=D.browser.safari&&D.os.osx;var n=D.browser.safari&&D.os.ios;
var a=D.browser.chrome;var F="user-hover";var g="mobile";var c="initial-play";var s="ac-video-live";
var t="longform";var x=r("../ui/DefaultBreakpoints");var p=r("@marcom/ac-console/log");
var h=r("./event/EventsToForward");var B=r("./event/ReadyStateChangeEvents");var f=r("../utils/BreakpointDetect");
var i=r("../ui/KeyboardControl");var A=r("@marcom/ac-accessibility/helpers/hide");
var o=r("@marcom/ac-accessibility/helpers/show");var y=function(H){H=H||{};this.el=H.el||document.createElement("div");
this._elementEmitter=new z(this.el);this.options=H;q.call(this);this._controlsFactory=H.controlsFactory;
this._urlOptimizer=H.urlOptimizer;try{var G=window.top;this._maxWidth=H.maxWidth||Math.min(window.innerWidth,1280)||Math.min(G.innerWidth,1280)
}catch(I){this._maxWidth=H.maxWidth||Math.min(window.innerWidth,1280)}this._lastResize=0;
this._lastMouseCoords={};this.el.classList.add("ac-video-player");this._isResponsive=H.responsive;
if(this._isResponsive){this._breakpointDetect=new f({el:this.el,player:this,breakpoints:x,addClass:true})
}this._isLive=H.live;if(this._isLive){this._useLiveMode()}this._videoImpl=j(H,this.el);
this._supportsInlineVideo=l||!(u&&n);this._cachedPiPMode=this.isPictureInPicture();
this._cachedReadyState=this.getReadyState();this._cachedVisibleTracksLength=0;this.el.appendChild(this._videoImpl.getMediaElement());
if(H.poster||typeof(H.poster)==="undefined"){this._initPoster(H.poster)}this._bindMethods();
this._addEventListeners();if(l){this._keyboardControl=new i({player:this,keyboardTarget:H.keyboardTarget})
}if(H.controls){this._initUIComponents()}if(H.parentElement){H.parentElement.appendChild(this.el)
}this.refreshSize=this.refreshSize.bind(this);setTimeout(this.refreshSize,0);window.addEventListener("DOMContentLoaded",this.refreshSize)
};y.LOADEDMETADATA=1;y.LOADEDDATA=2;y.CANPLAY=3;y.CANPLAYTHROUGH=4;var b=q.prototype;
y.prototype=Object.create(b);var w=y.prototype;w.constructor=y;w._bindMethods=function(){this._onStart=this._onStart.bind(this);
this._onEnded=this._onEnded.bind(this);this._onTimeUpdate=this._onTimeUpdate.bind(this);
this._onCaptionsChanged=this._onCaptionsChanged.bind(this);this._onPlay=this._onPlay.bind(this);
this._onFullscreenChange=this._onFullscreenChange.bind(this);this._forwardEvent=this._forwardEvent.bind(this);
this._onPresentationModeChanged=this._onPresentationModeChanged.bind(this);this._forwardFullScreenChangeEvent=this._forwardNamedEvent.bind(this,"fullscreen:change");
this._forwardEnterFullScreenEvent=this._forwardNamedEvent.bind(this,"enterfullscreen");
this._forwardExitFullScreenEvent=this._forwardNamedEvent.bind(this,"exitfullscreen");
this._onDurationChange=this._onDurationChange.bind(this);this._forwardReadyStateChange=this._forwardReadyStateChange.bind(this);
this._onFocusIn=this._onFocusIn.bind(this);this._onFocusOut=this._onFocusOut.bind(this);
this._showControls=this._showControls.bind(this);this._hideControls=this._hideControls.bind(this);
this._onClick=this._onClick.bind(this);this._onUserInteraction=this._onUserInteraction.bind(this);
this._onMouseLeave=this._onMouseLeave.bind(this);this._onMouseOut=this._onMouseOut.bind(this);
this._onPlayPromiseError=this._onPlayPromiseError.bind(this)};w._addEventListeners=function(){var H=0;
var G=h.length;for(;H<G;H++){this._videoImpl.on(h[H],this._forwardEvent)}H=0;G=B.length;
for(;H<G;H++){this._videoImpl.on(B[H],this._forwardReadyStateChange)}this._videoImpl.on("timeupdate",this._onTimeUpdate);
this._videoImpl.on("webkitpresentationmodechanged",this._onPresentationModeChanged);
this._videoImpl.on("durationchange",this._onDurationChange);this._videoImpl.on("addtrack",this._forwardEvent);
this._videoImpl.on("change",this._forwardEvent);this._videoImpl.on("change",this._onCaptionsChanged);
this._videoImpl.on("removetrack",this._forwardEvent);if(l){k.on("enterfullscreen",this._forwardEnterFullScreenEvent);
k.on("exitfullscreen",this._forwardExitFullScreenEvent);k.on("enterfullscreen",this._forwardFullScreenChangeEvent);
k.on("exitfullscreen",this._forwardFullScreenChangeEvent)}else{if(n){this._videoImpl.on("webkitbeginfullscreen",this._forwardEnterFullScreenEvent);
this._videoImpl.on("webkitendfullscreen",this._forwardExitFullScreenEvent);this._videoImpl.on("webkitbeginfullscreen",this._forwardFullScreenChangeEvent);
this._videoImpl.on("webkitendfullscreen",this._forwardFullScreenChangeEvent)}}this._videoImpl.on("PlayPromiseError",this._onPlayPromiseError);
this._elementEmitter.on("focusin",this._onFocusIn);this._elementEmitter.on("focusout",this._onFocusOut);
this.on("fullscreen:change",this._onFullscreenChange)};w._removeEventListeners=function(){var H=0;
var G=h.length;for(;H<G;H++){this._videoImpl.off(h[H],this._forwardEvent)}H=0;G=B.length;
for(;H<G;H++){this._videoImpl.off(B[H],this._forwardReadyStateChange)}this._videoImpl.off("timeupdate",this._onTimeUpdate);
this._videoImpl.off("webkitpresentationmodechanged",this._onPresentationModeChanged);
this._videoImpl.off("durationchange",this._onDurationChange);if(l){k.off("enterfullscreen",this._forwardEnterFullScreenEvent);
k.off("exitfullscreen",this._forwardExitFullScreenEvent);k.off("enterfullscreen",this._forwardFullScreenChangeEvent);
k.off("exitfullscreen",this._forwardFullScreenChangeEvent)}else{if(D.os.ios){this._videoImpl.off("webkitbeginfullscreen",this._forwardEnterFullScreenEvent);
this._videoImpl.off("webkitendfullscreen",this._forwardExitFullScreenEvent);this._videoImpl.off("webkitbeginfullscreen",this._forwardFullScreenChangeEvent);
this._videoImpl.off("webkitendfullscreen",this._forwardFullScreenChangeEvent)}}this._elementEmitter.off("focusin",this._onFocusIn);
this._elementEmitter.off("focusout",this._onFocusOut);this._elementEmitter.off("mouseenter",this._onUserInteraction);
if(this.controls){this.controls.el.removeEventListener("mousemove",this._onUserInteraction,true);
this.controls.el.removeEventListener("click",this._onUserInteraction,true)}if(this._blockade){this._blockade.off("mouseenter",this._onUserInteraction);
this._blockade.off("mousemove",this._onUserInteraction);this._blockade.off("click",this._onUserInteraction);
this._elementEmitter.off("click",this._onClick);if("onmouseleave" in this.el){this._blockade.off("mouseleave",this._onMouseLeave)
}else{this._blockade.off("mouseout",this._onMouseOut)}clearTimeout(this._userInteractionTimeout)
}if(this._keyboardControl){this._keyboardControl.off("keyboardinteraction",this._onUserInteraction)
}this.off("fullscreen:change",this._onFullscreenChange);this._videoImpl.off("PlayPromiseError",this._onPlayPromiseError);
clearTimeout(this._userInteractionTimeout)};w._forwardReadyStateChange=function(){var G=this.getReadyState();
if(G>this._cachedReadyState||G===0){this._cachedReadyState=G;this.trigger("readystatechange",{readyState:G})
}};w._forwardEvent=function(G){p(G.type+" time:"+this.getCurrentTime());this.trigger(G.type)
};w._forwardNamedEvent=function(G){p(G+" time:"+this.getCurrentTime());this.trigger(G)
};w._onPlayPromiseError=function(){p("play() Promise rejected, probably because the browser is blocking autoplay");
this.el.classList.add(c);this._showStartState();this.once("play",this._onPlay)};
w._onCaptionsChanged=function(G){var H=this.getVisibleTextTracks().length;if(H>0&&this._cachedVisibleTracksLength===0){this.trigger("texttrackshow")
}else{if(H===0&&this._cachedVisibleTracksLength>0){this.trigger("texttrackhide")
}}this._cachedVisibleTracksLength=H};w._onTimeUpdate=function(){this.trigger("timeupdate",{currentTime:this.getCurrentTime()})
};w.load=function(K,J,I,H){this.refreshSize();if(!Array.isArray(K)){K=[K]}if(J&&!Array.isArray(J)){J=[{src:J}]
}this._cachedReadyState=0;if(!H){H=this.options}if(this._urlOptimizer){if(!J){J=K.map(this._urlOptimizer.getCaptionsSource).filter(function(N){return(!!N)
})}var G=this.getVisibleTextTracks();if(G&&G.length&&J&&J.length){J[0].mode="showing"
}var L=H.maxWidth||this._calcMaxWidth();K=K.map(function(N){return this._urlOptimizer.getVideoSource(N,L,null,{maxWidth:this._maxWidth})
}.bind(this))}var M=(H&&H.thumbnails)||(this._urlOptimizer&&this._urlOptimizer.getThumbnailImageSource(K[0]));
this.once("play",this._onPlay);if(this._poster){this._poster.show()}if(this.options.autoplay&&l){this.once("loadstart",function(){this.play()
}.bind(this))}if(this.controls&&this.controls.sharingModule){if(H.sharing){this.controls.sharingModule.setData(H.sharing)
}else{this.controls.sharingModule.setData(null)}}if(H.live!==undefined){this._isLive=H.live;
this._useLiveMode()}this._videoImpl.load(K,J,I);if(this.controls&&this.controls.overlays){this.controls.overlays.setData(M)
}else{if(this.controls){this.once("controlsready",function(){this.controls.overlays&&this.controls.overlays.setData(M)
}.bind(this))}}};w._calcMaxWidth=function(){if(this.el.parentElement){return this.el.parentElement.clientWidth
}else{return this._maxWidth}};w._isActiveArea=function(G){while(G!==this.el){if(G.hasAttribute("data-acv-active-area")){return true
}G=G.parentNode}return false};w._onPresentationModeChanged=function(G){this._forwardEvent(G);
var H=this.isPictureInPicture();if(this._cachedPiPMode!==H){this._cachedPiPMode=H;
p("pictureinpicture:change to "+H);this.trigger("pictureinpicture:change")}};w._onDurationChange=function(G){if(this.getDuration()>3600){this.el.classList.add(t)
}};w.appendTo=function(G){G.appendChild(this.el);this.refreshSize()};w.getTextTracks=function(){return Array.prototype.slice.call(this._videoImpl.getTextTracks())
};w.getVisibleTextTracks=function(){var G=Array.prototype.slice.call(this._videoImpl.getTextTracks());
if(G&&G.length){G=G.filter(function(H){return H.mode==="showing"})}return G};w.getFullScreenElement=function(){if(!l){return this.getMediaElement()
}else{return this.el}};w.getFullScreenEnabled=function(){return k.fullscreenEnabled(this.getFullScreenElement())
};w.isFullscreen=function(){if(l){return k.fullscreenElement()===this.getFullScreenElement()
}else{return this._videoImpl.isFullscreen()}};w.requestFullscreen=function(){if(!this.isFullscreen()){if(this.controls){this.controls.el.display="none"
}this._hideControls();this.trigger("fullscreen:willenter",{type:"enter"});this._lastResize=Date.now();
if(a){setTimeout(function(){this._lastResize=Date.now();k.requestFullscreen(this.getFullScreenElement())
}.bind(this),300)}else{k.requestFullscreen(this.getFullScreenElement())}}};w.exitFullscreen=function(){if(this.isFullscreen()){if(this.controls){this.controls.el.display="none"
}this._hideControls();this.trigger("fullscreen:willexit",{type:"exit"});if(a){setTimeout(function(){k.exitFullscreen(this.getFullScreenElement())
}.bind(this),300)}else{k.exitFullscreen(this.getFullScreenElement())}}};w._onFullscreenChange=function(){this._lastResize=Date.now();
if(this.controls){this.controls.el.display=""}this._hideControls();this._preventUserInteraction=true;
setTimeout(function(){this._preventUserInteraction=false}.bind(this),750)};w.toggleFullscreen=function(){if(this.isFullscreen()){this.exitFullscreen()
}else{this.requestFullscreen()}};w._initUIComponents=function(){if(this._controlsFactory){this._instantiateDefaultCustomUIControls();
if(!l){this.controls.el.classList.add(g);this.setControls(true)}else{this.el.appendChild(this._blockade.el)
}}else{this.setControls(true)}};w._onFocusIn=function(){clearTimeout(this._focusOutTimer);
this._focusOutTimer=null;this._hasFocus=true;if(l){this._onUserInteraction()}};
w._onFocusOut=function(G){this._focusOutTimer=setTimeout(function(){if(this._hasFocus&&!this.el.contains(document.activeElement)){this._hasFocus=false;
this._hideControls()}}.bind(this),100)};w._showControls=function(){this.el.classList.remove(c);
this.el.classList.add(F)};w._hideControls=function(){this.el.classList.remove(F)
};w._onControlsReady=function(){if(!this.options.autoplay||!l){this._showStartState()
}};w._showStartState=function(){if(this.controls){this.controls.el.classList.add("start-state")
}if(!l){A(this.getMediaElement())}};w._hideStartState=function(){if(this.controls){this.controls.el.classList.remove("start-state")
}if(!l){o(this.getMediaElement())}};w._showEndState=function(){if(this.controls){if(this.controls.mainControlsElement){if(this.controls.mainControlsElement.contains(document.activeElement)){this.controls.playButtonElement.focus()
}}this.controls.el.classList.add("end-state")}A(this.getMediaElement())};w._hideEndState=function(){this.controls.el.classList.remove("end-state");
if(!l){o(this.getMediaElement())}};w._instantiateDefaultCustomUIControls=function(){this.controls=this._controlsFactory.create({player:this,basePath:this.options.localizationBasePath,template:this.options.template,readyCallback:function(){if(!this.options.autoplay||!l){this._showStartState()
}this.trigger("controlsready")}.bind(this)});if(this.controls.el.parentNode!==this.el){this.el.appendChild(this.controls.el)
}this._videoImpl.setControls(false);this._blockade=new z(document.createElement("div"));
this._blockade.el.classList.add("ac-video-blockade");if(l){this.controls.el.addEventListener("mousemove",this._onUserInteraction,true);
this.controls.el.addEventListener("click",this._onUserInteraction,true);this._elementEmitter.on("click",this._onClick);
if("onmouseleave" in this.el){this.controls.el.addEventListener("mouseleave",this._onMouseLeave)
}else{this.controls.el.addEventListener("mouseout",this._onMouseOut,true)}if(this._keyboardControl){this._keyboardControl.on("keyboardinteraction",this._onUserInteraction)
}}return this.controls};w._onClick=function(){this._hasFocus=false};w._onMouseLeave=function(G){window.clearTimeout(this._userInteractionTimeout);
this._hideControls();this._lastMouseCoords={}};w._onMouseOut=function(G){if(!this.controls.el.contains(G.target)&&G.target!==this.controls.el){this._onMouseLeave()
}};w._onUserInteraction=function(G){this.controls.el.classList.remove("hide-cursor");
if(!this.getCurrentSrc()||this._preventUserInteraction||(G&&this._lastMouseCoords.x===G.screenX&&this._lastMouseCoords.y===G.screenY)){return
}if(G&&G.pageX){this._lastMouseCoords={x:G.screenX,y:G.screenY}}this._showControls();
window.clearTimeout(this._userInteractionTimeout);if(G&&G.target){if(this._isActiveArea(G.target)){return
}}this._userInteractionTimeout=window.setTimeout(function(){this.controls.el.classList.add("hide-cursor");
this._hideControls()}.bind(this),this.options.controlsTimeoutDuration)};w._onPlay=function(){if(!C){this.once("timeupdate",this._onStart)
}else{this.once("timeupdate",this._onStart,function(){return this.getCurrentTime()>0
}.bind(this))}};w._onStart=function(){this.el.classList.add(c);if(this._poster){this._poster.hide()
}if(this.controls){this._hideStartState();this._hideEndState()}this.once("ended",this._onEnded)
};w._onEnded=function(){if(this.isFullscreen()){this.exitFullscreen()}if(this.controls){this._hideStartState();
this._showEndState()}this.once("timeupdate",this._onStart);if(this._poster){this._poster.show()
}};w._initPoster=function(G){this._poster=m({player:this,video:this._videoImpl,useNativePoster:(this.options.controls===false),is2x:v,src:G});
if(this._poster.el){this.el.appendChild(this._poster.el)}if(!this.options.autoplay){this._poster.show()
}};w._useLiveMode=function(){if(this._isLive){this.el.classList.add(s)}else{this.el.classList.remove(s)
}};w.once=function(I,L,J){if(arguments.length<3||typeof J==="object"){b.once.apply(this,arguments)
}else{var H=arguments;var K=Array.prototype.slice.call(arguments,2);var G=function(){if(K.every(function(M){return !!M()
})){H[1].apply(this,H);this.off(H[0],G)}}.bind(this);this.on(H[0],G)}};w.getMediaElement=function(){return this._videoImpl.getMediaElement()
};w.play=function(){p("play called");this._videoImpl.play()};w.pause=function(){this._videoImpl.pause()
};w.seek=function(G){this.setCurrentTime.apply(this,arguments)};w.addTextTrack=function(G){this._videoImpl.addTextTrack(G)
};w.getReadyState=function(){return this._videoImpl.getMediaElement().readyState
};w.getPreload=function(){return this._videoImpl.getPreload()};w.setPoster=function(G){this._poster.setSrc(G)
};w.getVolume=function(){return this._videoImpl.getVolume()};w.getMuted=function(){return this._videoImpl.getMuted()
};w.getCurrentTime=function(){return this._videoImpl.getCurrentTime()};w.getDuration=function(){return this._videoImpl.getDuration()
};w.getPaused=function(){return this._videoImpl.getPaused()};w.getEnded=function(){return this._videoImpl.getEnded()
};w.setCurrentTime=function(G){return this._videoImpl.setCurrentTime(G)};w.setVolume=function(G){this.trigger("uservolumechange");
return this._videoImpl.setVolume(G)};w.setMuted=function(G){this.trigger("uservolumechange");
this._videoImpl.setMuted(G)};w.setSrc=function(G){this._videoImpl.setSrc(G)};w.getCurrentSrc=function(){return this._videoImpl.getCurrentSrc()
};w.setControls=function(G){return this._videoImpl.setControls(G)};w.getMediaHeight=function(){return this._videoImpl.getMediaElement().videoHeight
};w.getMediaWidth=function(){return this._videoImpl.getMediaElement().videoWidth
};w.supportsPictureInPicture=function(){return this._videoImpl.supportsPictureInPicture()
};w.isPictureInPicture=function(){return this._videoImpl.isPictureInPicture()};
w.setPictureInPicture=function(G){return this._videoImpl.setPictureInPicture(G)
};w.supportsAirPlay=function(){return this._videoImpl.supportsAirPlay()};w.refreshSize=function(){if(this._breakpointDetect){this._breakpointDetect.refresh()
}else{this._currentBreakpoint&&this.el.classList.remove(this._currentBreakpoint.name);
this._currentBreakpoint=f.getBreakpointFromElement(this.el,x);this.el.classList.add(this._currentBreakpoint.name)
}};w.destroy=function(){this._removeEventListeners();this._videoImpl.destroy();
if(this.controls){this.controls.destroy();this.controls=null}this._videoImpl=undefined;
this.el.innerHTML="";if(this._breakpointDetect){this._breakpointDetect.destroy()
}q.prototype.destroy.call(this)};d.exports=y},{"../dom-emitter/DOMEmitterMicro":269,"../event-emitter-shim/EventEmitterShim":270,"../posterframe/PosterFrameFactory":278,"../ui/DefaultBreakpoints":287,"../ui/KeyboardControl":289,"../utils/BreakpointDetect":318,"../video/VideoFactory":326,"./event/EventsToForward":273,"./event/ReadyStateChangeEvents":274,"@marcom/ac-accessibility/helpers/hide":176,"@marcom/ac-accessibility/helpers/show":179,"@marcom/ac-console/log":32,"@marcom/ac-feature/isDesktop":36,"@marcom/ac-feature/isHandheld":37,"@marcom/ac-feature/isRetina":38,"@marcom/ac-fullscreen":196,"@marcom/ac-useragent":171}],273:[function(b,c,a){c.exports=["loadstart","progress","suspend","abort","error","emptied","stalled","play","pause","loadedmetadata","loadeddata","waiting","playing","canplay","canplaythrough","seeking","seeked","ended","ratechange","durationchange","volumechange","addtrack","change","removetrack"]
},{}],274:[function(b,c,a){c.exports=["loadstart","suspend","abort","error","emptied","stalled","loadedmetadata","loadeddata","waiting","canplay","canplaythrough"]
},{}],275:[function(d,f,b){var c=d("../Player");var g=d("@marcom/ac-feature/isDesktop")();
f.exports=function a(h){if(!h){h={}}else{if(arguments.length>1){h=Object.assign.apply(null,Array.prototype.slice.apply(arguments))
}}if(!h.components){h.components=d("../../ui/DefaultComponents")}if(typeof h.controls==="undefined"){h.controls=true
}if(!h.controlsImplementation){h.controlsImplementation=d("../../ui/ControlBar")
}if(!h.controlsFactory){h.controlsFactory=d("../../ui/ControlsFactory")({controlsImplementation:h.controlsImplementation,components:h.components,template:h.controlsTemplate})
}if(typeof h.urlOptimizer!=="undefined"&&h.urlOptimizer===true||h.urlOptimizer==="true"){h.urlOptimizer=d("../../optimizeVideoUrl")
}if(!h.sources&&!h.src){h.sources=[]}else{h.sources=(h.sources)?h.sources:(h.src)?[h.src]:[]
}h.autoplay=(h.autoplay!==undefined)?h.autoplay:g;if(!h.controlsTimeoutDuration){h.controlsTimeoutDuration=3000
}var j=new c(h);var i={};if(h.sharing){i.sharing=Object.assign({},h.sharing)}if(h.thumbnails){i.thumbnails=Object.assign({},h.thumbnails)
}if(h.sources&&h.sources.length){j.load(h.sources,h.textTracks,h.startTime,i)}return j
}},{"../../optimizeVideoUrl":271,"../../ui/ControlBar":285,"../../ui/ControlsFactory":286,"../../ui/DefaultComponents":288,"../Player":272,"@marcom/ac-feature/isDesktop":36}],276:[function(d,f,c){var b=d("./createPlayer");
f.exports=function a(g){if(arguments.length>1){g=Object.assign.apply(null,Array.prototype.slice.apply(arguments))
}if(g.localizationBasePath){g.sharing.basePath=g.localizationBasePath}return b(g)
}},{"./createPlayer":275}],277:[function(b,c,a){var h="ac-video-poster";var g="ac-video-poster-hide";
var d=function(i){this._initialize(i)};var f=d.prototype;f._initialize=function(i){var j=i.src;
this.el=i.el||document.createElement("div");this._imgElement=document.createElement("img");
this._imgElement.src=j;this._imgElement.alt="";this.el.appendChild(this._imgElement);
this.el.classList.add(h)};f.hide=function(){this.el.classList.add(g)};f.show=function(){this.el.classList.remove(g)
};f.setSrc=function(i){this._imgElement.src=i};c.exports=d},{}],278:[function(c,d,b){var f=c("./PosterFrame");
var g={"1x":"https://images.apple.com/ac/ac-video-posterframe/1.0/images/ac-video-poster_848x480.jpg","2x":"https://images.apple.com/ac/ac-video-posterframe/1.0/images/ac-video-poster_848x480_2x.jpg"};
d.exports=function a(h){h.src=h.src||((h.is2x)?g["2x"]:g["1x"]);if(!h.useNativePoster){return new f(h)
}else{h.video.setPoster(h.src);var j=false;var i;return{show:function(){j=true;
if(i){h.video.setPoster(i);i=null}},hide:function(){j=false},setSrc:function(k){if(!j){i=k
}else{h.video.setPoster(k)}}}}}},{"./PosterFrame":277}],279:[function(d,g,b){var c=d("@marcom/ac-ajax-xhr");
var i=d("@marcom/ac-function/throttle");var f=d("./parseVTT");var a=function(j,k){this._view=j;
this._video=k.video;this._refreshTracks=this._refreshTracks.bind(this);this._throttledRefreshCurrentCaption=i(this._refreshCurrentCaption.bind(this),300);
this._addTrackListeners()};var h=a.prototype;h._addTrackListeners=function(){this._video.on("addtrack",this._refreshTracks);
this._video.on("removetrack",this._refreshTracks);this._video.on("change",this._refreshTracks)
};h._addVideoListeners=function(j){if(!j.cues){this._view.setText("");try{return c.get(j.src,{complete:function(l){j.cues=f(l.responseText);
this._addVideoListeners(j);this._refreshCurrentCaption()}.bind(this),error:function(l){}.bind(this)})
}catch(k){}}this._video.on("loadstart",this._refreshTracks);this._video.on("timeupdate",this._throttledRefreshCurrentCaption)
};h._removeVideoListeners=function(){this._video.off("loadstart",this._refreshTracks);
this._video.off("timeupdate",this._throttledRefreshCurrentCaption)};h._refreshTracks=function(){var j=this._video.getTextTracks();
if(j&&j.length){j=j.filter(function(k){return k.mode==="showing"})}if(j.length){this._activeTrack=j[0];
this._addVideoListeners(this._activeTrack)}else{this._activeTrack=null;this._removeVideoListeners()
}this._refreshCurrentCaption()};h._getCurrentCaptionText=function(n){var k=(this._activeTrack)?this._activeTrack.cues:null;
if(!k){return""}else{if(this._currentCaption&&this._currentCaption.startTime>=n&&this._currentCaption<=n){return this._currentCaption.text
}}var l=0;var j=k.length;var m;while(l<j){if(k[l].startTime<=n&&k[l].endTime>=n){m=k[l]
}else{if(k[l].startTime>=n){break}}l++}this._currentCaption=m;return(m)?m.text:""
};h._refreshCurrentCaption=function(){this._view.setText(this._getCurrentCaptionText(this._video.getCurrentTime()))
};h.destroy=function(){this._removeVideoListeners()};g.exports=a},{"./parseVTT":284,"@marcom/ac-ajax-xhr":182,"@marcom/ac-function/throttle":42}],280:[function(c,a,f){var m=c("../ui/factory/createComponents");
var d=c("./TextTracksBehavior");var i=c("../ui/elements/Label");var l=c("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var n='<div class="ac-video-player-text-track"></div>';var g="is-visible";var k="ac-video-player-text-track-container";
var j={textTracksPolyfill:{className:"ac-video-player-text-track",view:{classDef:i,options:{}},behavior:{classDef:d}}};
var b=function(o){l.call(this);this.container=o.container;this._video=o.video;this._initialize(o)
};var h=b.prototype=Object.create(l.prototype);h._initialize=function(o){this._onTrackChange=this._onTrackChange.bind(this);
this.el=document.createElement("div");this.el.innerHTML=o.template||n;this.el.classList.add(k);
this._tracks=o.tracks||[];this._textTrackComponent=m(this.el,j,{video:this._video})
};h._onTrackChange=function(){this.trigger("change");if(!this.el.parentElement){this._video.el.parentElement.appendChild(this.el);
this.el.firstElementChild.classList.add(g)}};h.addTrack=function(p){if(!this._tracks){this._tracks=[]
}var q=p.mode||"hidden";var o=this._onTrackChange;Object.defineProperty(p,"mode",{get:function(){return q
},set:function(r){q=r;o()},enumerable:true,configurable:true});this._tracks.push(p);
this.trigger("addtrack")};h.clearTracks=function(){this._tracks=[];this.trigger("removetrack");
this.trigger("change")};h.getTextTracks=function(){return this._tracks};h.trigger=function(o,p){return l.prototype.trigger.call(this,o,Object.assign({type:o},p||{}))
};h.destroy=function(){this._textTrackComponent.destroy();l.prototype.destroy.call(this)
};a.exports=b},{"../ui/elements/Label":304,"../ui/factory/createComponents":309,"./TextTracksBehavior":279,"@marcom/ac-event-emitter-micro":33}],281:[function(d,a,f){var j=d("@marcom/ac-useragent");
var k;if(j.browser.safari){k=function(l,m){l.track.mode=m}}else{k=function(l,m){l.mode=m
}}var g=function(n){var m;if(n instanceof HTMLElement){return this._videoElement.appendChild(n)
}var l=document.createElement("track");l.src=n.src;l.kind="captions";l.srclang=n.srclang;
if(l.srclang==="en"){l.label="English"}if(j.browser.firefox){m=this._videoElement.textTracks.length;
setTimeout(function(){this._videoElement.appendChild(l);k(this._videoElement.textTracks[m],n.mode||"hidden")
}.bind(this),0)}else{if(j.os.android){m=this._videoElement.textTracks.length;this._videoElement.appendChild(l);
k(this._videoElement.textTracks[m],n.mode||"hidden")}else{this._videoElement.appendChild(l);
k(l,n.mode||"hidden")}}};var c=function(){return this._videoElement.textTracks};
var h=function(){if(!this._textTracksEmitter){var l=d("../dom-emitter/DOMEmitterMicro");
this._textTracksEmitter=new l(this.getTextTracks())}return this._textTracksEmitter
};var b=function(n){var o=0;var l=n?n.length:0;for(;o<l;o++){var m=n[o];g.call(this,m)
}};var i=function(){};a.exports={create:b,add:g,get:c,getEmitter:h,destroy:i}},{"../dom-emitter/DOMEmitterMicro":269,"@marcom/ac-useragent":171}],282:[function(d,a,f){var c=d("./TextTracksDOM");
var i=function(l){if(!l){return}if(!this._textTracksPolyfill){this._textTracksPolyfill=new c({video:this,tracks:l,container:this._parentElement})
}else{this._textTracksPolyfill.clearTracks();var m=0;var k=l.length;for(;m<k;m++){this._textTracksPolyfill.addTrack(l[m])
}}};var g=function(k){return this._textTracksPolyfill.addTrack(k)};var b=function(){if(!this._textTracksPolyfill){this._createTextTrackTags([])
}return this._textTracksPolyfill.getTextTracks()};var h=function(){if(!this._textTracksPolyfill){this._createTextTrackTags([])
}return this._textTracksPolyfill};var j=function(){this._textTracksPolyfill.destroy();
this._textTracksPolyfill=null};a.exports={create:i,add:g,get:b,getEmitter:h,destroy:j}
},{"./TextTracksDOM":280}],283:[function(c,d,b){var g=c("@marcom/ac-useragent");
var f=!g.browser.ie&&!g.browser.edge;d.exports=function a(i){i=i||{};var h=(typeof i.useNativeCaptions==="undefined")?f:i.useNativeCaptions;
return(h)?c("./TextTracksNative"):c("./TextTracksPolyfill")}},{"./TextTracksNative":281,"./TextTracksPolyfill":282,"@marcom/ac-useragent":171}],284:[function(b,d,a){var f=b("../utils/Time");
d.exports=function c(n){var l=n.split(/\n/);var m=/([\d]{2}:)?[\d]{2}:[\d]{2}.[\d]{3}( \-\-> ){1}([\d]{2}:)?[\d]{2}:[\d]{2}.[\d]{3}/;
var k=[];var h;var o;var j=0;var g=l.length;for(j;j<g;j++){o="";if(m.test(l[j])){h=l[j].split(" --> ");
h[0]=h[0].split(":").length<3?"00:"+h[0]:h[0];h[1]=h[1].split(":").length<3?"00:"+h[1]:h[1];
while(++j&&j<g&&!m.test(l[j])){if(l[j]!==""){o+=l[j]+"<br />"}}o=o.substr(0,o.length-6);
if(j<g){j--}k.push({startTime:f.stringToNumber(h[0].split(" ")[0]),endTime:f.stringToNumber(h[1].split(" ")[0]),text:o})
}}return k}},{"../utils/Time":319}],285:[function(f,c,h){var b=f("@marcom/ac-string/supplant");
var l=f("../utils/Time");var j=f("./localization/Localization");var o=f("./factory/createComponents");
var m="ac-video-controls";var d="control-bar-skin-default";var g=f("@marcom/ac-feature/isDesktop")();
var a=f("./overlays/OverlayContainer");var n=f("../utils/merge");var k=function(p){this._initialize(p)
};var i=k.prototype;i._initialize=function(p){this.el=p.element||document.createElement("div");
this._basePath=p.basePath;this.el.style.display="none";this._template=p.template||'<div class="controls-container" >\n\n\t<div class="{elementClassPrefix}-social-tray hidden"></div>\n\n\t<div class="center-button-container {elementClassPrefix}-play-pause-button-container">\n\t\t<div class="button-wrapper">\n\t\t\t<button type="button" class="ac-video-icon centered-button {elementClassPrefix}-play-pause-button {elementClassPrefix}-button no-autoplay" value="{playpause}" aria-label="{playpause}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t</div>\n\t</div>\n\n\t<div class="main-controls-container" >\n\t\t<div class="ac-video-overlay-container" ></div>\n\t\t<div class="main-controls">\n\t\t\t<div class="button-wrapper">\n\t\t\t\t<div class="main-controls-item controls-volume">\n\t\t\t\t\t<button type="button" class="ac-video-icon {elementClassPrefix}-toggle-mute-volume-button {elementClassPrefix}-button" value="{togglemutevolume}" aria-label="{togglemutevolume}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t\t\t\t<div class="{elementClassPrefix}-volume-level-indicator" tabindex="0" aria-valuemin="0" aria-valuemax="100" min="0" max="100" aria-label="{adjustvolume}" role="slider" aria-orientation="vertical" step="0.05" data-acv-active-area></div>\n\t\t\t\t</div>\n\t\t\t</div>\n\n\t\t\t<div class="button-wrapper">\n\t\t\t\t<button type="button" class="ac-video-icon main-controls-item {elementClassPrefix}-text-tracks-toggle-button {elementClassPrefix}-button no-text-tracks" value="{captionscontrol}" aria-label="{captionscontrol}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t\t</div>\n\n\t\t\t<div class="main-controls-item controls-progress">\n\t\t\t\t<div class="controls-progress-time controls-progress-time-1">\n\t\t\t\t\t<div class="{elementClassPrefix}-elapsed-time-indicator" role="text" tabindex="-1">\n\t\t\t\t\t\t<span class="label">{elapsed}</span>\n\t\t\t\t\t\t<span class="{elementClassPrefix}-elapsed-time">00:00</span>\n\t\t\t\t\t</div>\n\t\t\t\t</div>\n\t\t\t\t<div class="controls-progress-bar">\n\t\t\t\t\t<div class="{elementClassPrefix}-buffered-indicator"></div>\n\t\t\t\t\t<div class="{elementClassPrefix}-progress-indicator ac-slider-inactive" aria-label="progress-indicator" role="slider" precision="float" min="0" max="{max}" step="0.0005" value="0" tabindex="0" aria-valuemax="{max}" aria-valuemin="{min}" aria-valuenow="{value}" data-acv-active-area></div>\n\t\t\t\t</div>\n\t\t\t\t<div class="controls-progress-time controls-progress-time-2">\n\t\t\t\t\t<div class="{elementClassPrefix}-remaining-time-indicator" role="text" tabindex="-1">\n\t\t\t\t\t\t<span class="label">{remaining}</span>\n\t\t\t\t\t\t<span class="{elementClassPrefix}-remaining-time">-00:00</span>\n\t\t\t\t\t</div>\n\t\t\t\t</div>\n\t\t\t</div>\n\t\t\t\n\t\t\t<div class="main-controls-item live-stream">\n\t\t\t\t<span class="live-stream-text">{livestream}</span>\n\t\t\t</div>\n\n\t\t\t<div class="button-wrapper">\n\t\t\t\t<button type="button" class="ac-video-icon main-controls-item {elementClassPrefix}-airplay-button {elementClassPrefix}-button airplay-unsupported" value="{airplay}" aria-label="{airplay}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t\t</div>\n\n\t\t\t<div class="button-wrapper">\n\t\t\t\t<button type="button" class="ac-video-icon main-controls-item {elementClassPrefix}-picture-in-picture-button {elementClassPrefix}-button picture-in-picture-unsupported" value="{pictureinpicture}" aria-label="{pictureinpicture}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t\t</div>\n\n\t\t\t<div class="button-wrapper">\n\t\t\t\t<button type="button" class="ac-video-icon main-controls-item {elementClassPrefix}-full-screen-button {elementClassPrefix}-button fullscreen-unsupported" value="{fullscreen}" aria-label="{fullscreen}" role="button" tabindex="0" data-acv-active-area></button>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n</div>\n';
this._templateData=p.templateData||Object.assign({elementClassPrefix:"controls"});
this._destroyed=false;this._localize().then(function(){if(!this._destroyed){this._initUIComponents(p);
this.el.style.display=""}if(typeof p.readyCallback==="function"){p.readyCallback()
}}.bind(this))};i._localize=function(){return new Promise(function(p){j.getTranslation({callback:function(q){p(q)
}.bind(this),basePath:this._basePath})}.bind(this)).then(function(p){this._templateData=Object.assign(this._templateData,p)
}.bind(this))};i._renderTemplateMarkup=function(){var p=b(this._template,this._templateData);
this.el.innerHTML=p};i._initDesktopControls=function(p,q){this._componentCollection=o(p,n(q,{elementClassPrefix:this._templateData.elementClassPrefix,elapsedTimeIndicator:{behavior:{observe:{source:this._player,events:["timeupdate","seeking","seeked","durationchange"],update:function(r){r.setText(l.formatTime(this._player.getCurrentTime(),this._player.getDuration()))
}.bind(this)}}},remainingTimeIndicator:{behavior:{observe:{source:this._player,events:["timeupdate","seeking","seeked","durationchange"],update:function(r){r.setText(l.formatTime(this._player.getCurrentTime()-this._player.getDuration(),this._player.getDuration()))
}.bind(this)}}},volumeLevel:{view:{options:{value:(this._player.getMuted())?0:(this._player.getVolume()*100)}}},playPauseContainer:{view:{options:{labels:{playing:this._templateData.pause,paused:this._templateData.play,ended:this._templateData.replay}}}},fullScreen:{view:{options:{labels:{initial:this._templateData.fullscreen,on:this._templateData.exitfullscreen,off:this._templateData.fullscreen}}}},pictureInPictureToggle:{view:{options:{labels:{initial:this._templateData.pictureinpicture,on:this._templateData.exitpictureinpicture,off:this._templateData.pictureinpicture}}}}}),{player:this._player,localization:this._templateData})
};i._initUIComponents=function(q){this._player=q.player;var p=this.el;var r=q.components;
p.classList.add(q.className||m);this._renderTemplateMarkup();var s=p.querySelector(".main-controls-container");
if(!g){s.parentElement.removeChild(s)}else{s.classList.add(d);this.mainControlsElement=s
}this._initDesktopControls(p,r);this.sharingModule=this._componentCollection.components.socialShare[0].behavior.sharingModule;
if(this._componentCollection.components.progressBar.length){this.scrubberView=this._componentCollection.components.progressBar[0].view
}this.playButtonElement=this.el.querySelector(".controls-play-pause-button");if(g){this.overlays=new a({el:this.el.querySelector(".ac-video-overlay-container"),player:this._player})
}};i._setVolume=function(p){if(p){this._player.setMuted(false)}this._player.setVolume(p)
};i._thirySecondsBack=function(){var q=this._player.getCurrentTime();var p=q-30;
this._player.setCurrentTime((p<0)?0:p)};i.destroy=function(){if(this._componentCollection){this._componentCollection.destroy();
this._componentCollection=null}this._destroyed=true;this._player=null;this._templateData=null
};c.exports=k},{"../utils/Time":319,"../utils/merge":320,"./factory/createComponents":309,"./localization/Localization":312,"./overlays/OverlayContainer":314,"@marcom/ac-feature/isDesktop":36,"@marcom/ac-string/supplant":268}],286:[function(c,f,b){var d={components:c("./DefaultComponents"),controlsImplementation:c("./ControlBar")};
var a=function(g){g=g||{};var h=Object.assign({},d,g);return{create:function(j){var i=Object.assign({},h,j);
i.components=g.components||d.components;return new i.controlsImplementation(i)}}
};f.exports=a},{"./ControlBar":285,"./DefaultComponents":288}],287:[function(b,c,a){c.exports=[{name:"small",minWidth:0,maxWidth:479},{name:"medium",minWidth:480,maxWidth:779},{name:"large",minWidth:780,maxWidth:Infinity}]
},{}],288:[function(i,a,t){var m=i("./elements/Button");var l=i("./elements/StatefulButton");
var p=i("./elements/Label");var n=i("./elements/Slider");var o=i("./elements/Container");
var s=i("./behaviors/MuteButtonBehavior");var f=i("./behaviors/PlayPauseButtonBehavior");
var g=i("./behaviors/PictureInPictureButtonBehavior");var q=i("./behaviors/CaptionsButtonBehavior");
var k=i("./behaviors/FullScreenButtonBehavior");var h=i("./behaviors/ProgressBarSliderBehavior");
var j=i("./behaviors/VolumeSliderBehavior");var c=i("./behaviors/SharingButtonBehavior");
var b=i("./behaviors/SocialContainerBehavior");var d=i("./behaviors/AirPlayButtonBehavior");
var r=i("./elements/mixins/CursorPointer");a.exports={back30Seconds:{className:"back-30-seconds-button",view:{classDef:m}},fullScreen:{className:"full-screen-button",view:{classDef:l,options:{states:{initial:"fullscreen-unsupported",on:"is-fullscreen",off:""},labels:{initial:"fullscreen",on:"exitfullscreen",off:"fullscreen"}}},behavior:{classDef:k}},toggleMuteVolume:{className:"toggle-mute-volume-button",view:{classDef:l,options:{states:{initial:[],on:["is-muted"],off:[]}}},behavior:{classDef:s}},playPauseContainer:{className:"play-pause-button-container",view:{classDef:l,options:{states:{playing:["is-playing"],paused:[],ended:["is-ended"]}}},behavior:{classDef:f}},pictureInPictureToggle:{className:"picture-in-picture-button",view:{classDef:l,options:{states:{initial:["picture-in-picture-unsupported"],on:["is-picture-in-picture"],off:[]},labels:{initial:"pictureinpicture",on:"exitpictureinpicture",off:"pictureinpicture"}}},behavior:{classDef:g}},captionsToggle:{className:"text-tracks-toggle-button",view:{classDef:l,options:{states:{initial:["no-text-tracks"],on:["text-tracks-visible"],off:[]}}},behavior:{classDef:q}},airplayToggle:{className:"airplay-button",view:{classDef:l,options:{states:{initial:["airplay-unsupported"],on:["airplay-active"],off:[]}}},behavior:{classDef:d}},elapsedTimeIndicator:{className:"elapsed-time",view:{classDef:p}},remainingTimeIndicator:{className:"remaining-time",view:{classDef:p}},progressBar:{className:"progress-indicator",view:{classDef:n,options:{template:'<div class="ac-slider-runnable-track">\n\t<div class="ac-slider-hover-track">\n\t\t<div class="ac-slider-hover-notch"></div>\n\t</div>\n\t<div class="ac-slider-thumb">\n\t\t<div class="ac-slider-thumb-background-wrapper">\n\t\t\t<div class="ac-slider-thumb-background"></div>\n\t\t</div>\n\t</div>\n\t<div class="ac-slider-inner-track">\n\t\t<div class="ac-slider-scrubbed"></div>\n\t</div>\n</div>',min:0,max:1,mixins:[r],orientation:"horizontal"}},behavior:{classDef:h}},volumeLevel:{className:"volume-level-indicator",view:{classDef:n,options:{template:'<div class="ac-slider-runnable-track">\n\t<div class="ac-slider-background"></div>\n\t<div class="ac-slider-thumb-wrapper">\n\t\t<div class="ac-slider-thumb">\n\t\t\t<div class="ac-slider-thumb-background-wrapper">\n\t\t\t\t<div class="ac-slider-thumb-background"></div>\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\t<div class="ac-slider-inner-track">\n\t\t<div class="ac-slider-scrubbed"></div>\n\t</div>\n</div>',min:0,max:100,mixins:[r],orientation:"vertical"}},behavior:{classDef:j}},sharing:{className:"sharing-button",view:{classDef:l,options:{states:{initial:["sharing-unsupported"],on:["is-sharing"],off:[]}}},behavior:{classDef:c}},socialShare:{className:"social-tray",view:{classDef:o,options:{}},behavior:{classDef:b}}}
},{"./behaviors/AirPlayButtonBehavior":290,"./behaviors/CaptionsButtonBehavior":293,"./behaviors/FullScreenButtonBehavior":294,"./behaviors/MuteButtonBehavior":295,"./behaviors/PictureInPictureButtonBehavior":296,"./behaviors/PlayPauseButtonBehavior":297,"./behaviors/ProgressBarSliderBehavior":298,"./behaviors/SharingButtonBehavior":299,"./behaviors/SocialContainerBehavior":300,"./behaviors/VolumeSliderBehavior":301,"./elements/Button":302,"./elements/Container":303,"./elements/Label":304,"./elements/Slider":305,"./elements/StatefulButton":306,"./elements/mixins/CursorPointer":307}],289:[function(f,c,g){var b=f("@marcom/ac-keyboard/Keyboard");
var n=f("@marcom/ac-event-emitter-micro").EventEmitterMicro;var j=32;var d=37;var m=38;
var i=39;var k=40;var a=function(o){n.call(this);this._player=o.player;this._target=o.keyboardTarget||this._player.el;
this._keyboard=new b(this._target);this._addEventListeners()};var l=n.prototype;
var h=a.prototype=Object.create(l);h._addEventListeners=function(){this._onLeftArrow=this._onLeftArrow.bind(this);
this._onRightArrow=this._onRightArrow.bind(this);this._onUpArrow=this._onUpArrow.bind(this);
this._onDownArrow=this._onDownArrow.bind(this);this._onSpaceBarUp=this._onSpaceBarUp.bind(this);
this._onSpaceBarDown=this._onSpaceBarDown.bind(this);this._onKeyboardInteraction=this._onKeyboardInteraction.bind(this);
this._onDurationChange=this._onDurationChange.bind(this);this._boundKeyboardInteraction={};
[j,d,i,m,k].forEach(function(o){this._boundKeyboardInteraction[o]=this._onKeyboardInteraction.bind(this,o);
this._keyboard.onDown(o,this._boundKeyboardInteraction[o])}.bind(this));this._keyboard.onDown(j,this._onSpaceBarDown);
this._keyboard.onDown(d,this._onLeftArrow);this._keyboard.onDown(i,this._onRightArrow);
this._keyboard.onDown(m,this._onUpArrow);this._keyboard.onDown(k,this._onDownArrow);
this._player.on("durationchange",this._onDurationChange)};h._onKeyboardInteraction=function(){this.trigger("keyboardinteraction")
};h._onDurationChange=function(){var o=this._player.getDuration();if(o>=60){this._interval=10
}else{if(o>=20){this._interval=5}else{this._interval=1}}};h._onLeftArrow=function(o){o.originalEvent.preventDefault();
o.originalEvent.stopPropagation();var p=this._player.getCurrentTime();if(!isNaN(p)){this._player.seek(Math.max(p-this._interval,0))
}};h._onRightArrow=function(o){o.originalEvent.preventDefault();o.originalEvent.stopPropagation();
var p=this._player.getCurrentTime();if(!isNaN(p)){this._player.seek(Math.min(p+this._interval,this._player.getDuration()))
}};h._onUpArrow=function(o){o.originalEvent.preventDefault();o.originalEvent.stopPropagation();
var p=this._player.getMuted()?0:this._player.getVolume();var q=Math.min(1,p+0.1);
this._player.setVolume(q);this._player.setMuted(false)};h._onDownArrow=function(o){o.originalEvent.preventDefault();
o.originalEvent.stopPropagation();var p=this._player.getMuted()?0:this._player.getVolume();
var q=Math.max(0,p-0.1);this._player.setVolume(q);this._player.setMuted(Math.round(q*10)===0)
};h._onSpaceBarDown=function(o){if(o.target.tagName==="BUTTON"){return}this._keyboard.offDown(j,this._onSpaceBarDown);
this._keyboard.onUp(j,this._onSpaceBarUp)};h._onSpaceBarUp=function(){this._keyboard.offUp(j,this._onSpaceBarUp);
if(this._player.getPaused()){this._player.play()}else{this._player.pause()}this._keyboard.onDown(j,this._onSpaceBarDown)
};h.destroy=function(){[j,d,i,m,k].forEach(function(o){this._keyboard.offDown(o,this._boundKeyboardInteraction[o])
}.bind(this));this._boundKeyboardInteraction=null;this._keyboard.offDown(j,this._onSpaceBarDown);
this._keyboard.offUp(j,this._onSpaceBarUp);this._keyboard.offDown(d,this._onLeftArrow);
this._keyboard.offDown(i,this._onRightArrow);this._keyboard.offDown(m,this._onUpArrow);
this._keyboard.offDown(k,this._onDownArrow);this._player.off("durationchange",this._onDurationChange);
this._keyboard.destroy();l.destroy.call(this)};c.exports=a},{"@marcom/ac-event-emitter-micro":33,"@marcom/ac-keyboard/Keyboard":205}],290:[function(b,g,a){var f=b("./ButtonBehavior");
var d=function(i,j){f.apply(this,arguments);if(this._player.supportsAirPlay()){this._airplayStateChange=this._airplayStateChange.bind(this);
this._player.getMediaElement().addEventListener("webkitplaybacktargetavailabilitychanged",this._airplayStateChange);
this._updateState=this._updateState.bind(this);this._player.getMediaElement().addEventListener("webkitcurrentplaybacktargetiswirelesschanged",this._updateState)
}};var c=f.prototype;var h=d.prototype=Object.create(c);h._airplayStateChange=function(i){if(i.availability==="available"){this._airplayAvailable=true
}else{this._airplayAvailable=false}this._updateState()};h._updateState=function(){if(this._player.getMediaElement().webkitCurrentPlaybackTargetIsWireless){this._view.setState("on")
}else{if(this._airplayAvailable){this._view.setState("off")}else{this._view.setState("initial")
}}};h._onClick=function(){this._player.getMediaElement().webkitShowPlaybackTargetPicker()
};h.destroy=function(){this._player.getMediaElement().removeEventListener("webkitplaybacktargetavailabilitychanged",this._airplayStateChange);
this._player.getMediaElement().removeEventListener("webkitcurrentplaybacktargetiswirelesschanged",this._updateState)
};g.exports=d},{"./ButtonBehavior":292}],291:[function(c,d,b){var a=function(f,g){this._player=g.player;
this._view=f;if(this._addViewListeners){this._addViewListeners()}if(this._addPlayerListeners){this._addPlayerListeners()
}};d.exports=a},{}],292:[function(b,f,a){var d=b("./BaseBehavior");var c=function(h,i){this._onClick=this._onClick.bind(this);
d.apply(this,arguments)};var g=c.prototype=Object.create(d.prototype);g._addViewListeners=function(){this._view.on("click",this._onClick)
};g._clickHandler=function(h){h.preventDefault();this._onClick(h)};g._onClick=function(h){};
g.destroy=function(){this._view.off("click",this._onClick)};f.exports=c},{"./BaseBehavior":291}],293:[function(b,f,a){var d=b("./ButtonBehavior");
var h=function(i,j){d.apply(this,arguments);this._updateState()};var c=d.prototype;
var g=h.prototype=Object.create(c);g._updateState=function(){var j=this._player.getVisibleTextTracks();
var i=this._player.getTextTracks();if(j.length){this._view.setState("on")}else{if(i.length){this._view.setState("off")
}else{this._view.setState("initial")}}};g._addPlayerListeners=function(){this._updateState=this._updateState.bind(this);
this._player.on("addtrack",this._updateState);this._player.on("change",this._updateState);
this._player.on("removetrack",this._updateState)};g._onClick=function(){var j=this._player.getVisibleTextTracks();
var i=this._player.getTextTracks();if(j.length){i[0].mode="hidden"}else{i[0].mode="showing"
}};g.destroy=function(){this._player.off("addtrack",this._updateState);this._player.off("change",this._updateState);
this._player.off("removetrack",this._updateState);c.destroy.call(this)};f.exports=h
},{"./ButtonBehavior":292}],294:[function(b,g,a){var f=b("./ButtonBehavior");var d=function(i,j){f.apply(this,arguments);
if(this._player.getFullScreenEnabled()){this._updateState()}};var c=f.prototype;
var h=d.prototype=Object.create(c);h._addPlayerListeners=function(){this._updateState=this._updateState.bind(this);
this._player.on("fullscreen:change",this._updateState)};h._updateState=function(){this._view.setState((this._player.isFullscreen())?"on":"off")
};h._onClick=function(){this._player.toggleFullscreen(!this._player.isFullscreen())
};h.destroy=function(){this._player.off("fullscreen:change",this._updateState);
c.destroy.call(this)};g.exports=d},{"./ButtonBehavior":292}],295:[function(b,f,a){var d=b("./ButtonBehavior");
var h=function(i,j){d.apply(this,arguments);this._updateState()};var c=d.prototype;
var g=h.prototype=Object.create(c);g._updateState=function(){this._view.setState((this._player.getMuted())?"on":"off")
};g._addPlayerListeners=function(){this._updateState=this._updateState.bind(this);
this._player.on("volumechange",this._updateState)};g._onClick=function(){if(this._player.getMuted()){this._player.setMuted(false);
if(this._player.getVolume()===0){this._player.setVolume(0.1)}}else{this._player.setMuted(true)
}};g.destroy=function(){this._player.off("volumechange",this._updateState);c.destroy.call(this)
};f.exports=h},{"./ButtonBehavior":292}],296:[function(b,g,a){var f=b("./ButtonBehavior");
var d=function(i,j){f.apply(this,arguments);this._initialize()};var c=f.prototype;
var h=d.prototype=Object.create(c);h._initialize=function(){this._updateButtonState=this._updateButtonState.bind(this);
if(this._player.supportsPictureInPicture()){this._updateButtonState();this._player.on("webkitpresentationmodechanged",this._updateButtonState)
}};h._onClick=function(){this._player.setPictureInPicture(!this._player.isPictureInPicture())
};h._updateButtonState=function(){this._view.setState((this._player.isPictureInPicture())?"on":"off")
};h.destroy=function(){this._player.off("webkitpresentationmodechanged",this._updateButtonState);
c.destroy.call(this)};g.exports=d},{"./ButtonBehavior":292}],297:[function(b,f,a){var d=b("./ButtonBehavior");
var g=function(i,j){d.apply(this,arguments);this._setPlayingState()};var c=d.prototype;
var h=g.prototype=Object.create(c);h._addPlayerListeners=function(){this._setPlayingState=this._setPlayingState.bind(this);
this._player.on("play",this._setPlayingState);this._player.on("pause",this._setPlayingState);
this._player.on("ended",this._setPlayingState)};h._onClick=function(){this._togglePlay()
};h._setPlayingState=function(){this._view.setState((this._player.getEnded())?"ended":((this._player.getPaused())?"paused":"playing"))
};h._togglePlay=function(){if(this._player.getPaused()||this._player.getEnded()){this._player.play()
}else{this._player.pause()}};h.destroy=function(){this._player.off("play",this._setPlayingState);
this._player.off("pause",this._setPlayingState);c.destroy.call(this)};f.exports=g
},{"./ButtonBehavior":292}],298:[function(d,b,g){var i=d("./BaseBehavior");var a=d("@marcom/ac-string/supplant");
var f="is-playing";var k=d("@marcom/ac-raf-emitter/draw");var c=d("@marcom/ac-raf-emitter/cancelDraw");
var j=function(l,m){i.apply(this,arguments);this._visible=false;this._ariaTextTemplate=m.localization.currenttimetext;
this._onDurationChange()};var h=j.prototype=Object.create(i.prototype);h._addViewListeners=function(){this._onSliderGrab=this._onSliderGrab.bind(this);
this._onSliderChange=this._onSliderChange.bind(this);this._onSliderRelease=this._onSliderRelease.bind(this);
this._view.on("grab",this._onSliderGrab)};h._addPlayerListeners=function(){this._onTimeUpdate=this._onTimeUpdate.bind(this);
this._onPlay=this._onPlay.bind(this);this._onPause=this._onPause.bind(this);this._onEnded=this._onEnded.bind(this);
this._onDurationChange=this._onDurationChange.bind(this);this._onRAF=this._onRAF.bind(this);
this._player.on("durationchange",this._onDurationChange);this._player.on("loadstart",this._onEnded);
this._player.on("ended",this._onEnded);this._player.on("timeupdate",this._onTimeUpdate);
this._player.on("play",this._onPlay);this._player.on("pause",this._onPause);this._player.on("ended",this._onEnded)
};h._setIsPlaying=function(l){if(l){this._view.setState(f)}else{this._view.clearState(f)
}};h._onPlay=function(){this._setIsPlaying(true);c(this._timeUpdateInterval);k(this._onRAF)
};h._onRAF=function(){this._onTimeUpdate();this._timeUpdateInterval=k(this._onRAF)
};h._onPause=function(){this._setIsPlaying(false);c(this._timeUpdateInterval);this._onTimeUpdate()
};h._onEnded=function(){this._onPause();this._updateSliderPosition(0)};h._onSliderGrab=function(){this._player.off("timeupdate",this._onTimeUpdate);
c(this._timeUpdateInterval);this._view.off("grab",this._onSliderGrab);this._view.on("change",this._onSliderChange);
this._view.on("release",this._onSliderRelease);this._onPause()};h._onSliderRelease=function(){this._view.off("change",this._onSliderChange);
this._view.off("release",this._onSliderRelease);this._view.on("grab",this._onSliderGrab);
this._player.on("timeupdate",this._onTimeUpdate);if(!this._player.getPaused()){this._onPlay()
}};h._getTimeAsPercent=function(){return this._player.getCurrentTime()/this._cachedDuration
};h._onDurationChange=function(){this._cachedDuration=this._player.getDuration();
this._updateSliderPosition(this._getTimeAsPercent());if(!this._player.getPaused()){this._onPlay()
}};h._onSliderChange=function(){var l=this._view.getValue();this._setPlayerCurrentTime(l*this._cachedDuration);
this._setAriaValueText(l*this._cachedDuration);this._updateScrubbedValue()};h._onTimeUpdate=function(){if(this._player.getPaused()){this._updateSliderPosition(this._getTimeAsPercent())
}else{this._updateSliderPosition(this._getTimeAsPercent())}};h._updateSliderPosition=function(l){this._view.setValue(l);
this._setAriaValueText(l*this._cachedDuration);this._updateScrubbedValue();if(!this._visible&&!isNaN(this._cachedDuration)){this._view.show();
this._visible=true}};h._setAriaValueText=function(l){var m=Math.floor(l/60);var n=Math.ceil(l%60);
this._view.setAriaValueText(a(this._ariaTextTemplate,{minutes:m,seconds:n}))};h._updateScrubbedValue=function(){this._view.setScrubbedValue()
};h._setPlayerCurrentTime=function(l){this._player.setCurrentTime(l)};h._removeEventListeners=function(){this._player.off("durationchange",this._onDurationChange);
this._player.off("loadstart",this._onEnded);this._player.off("ended",this._onEnded);
this._player.off("timeupdate",this._onTimeUpdate);this._view.off("change",this._onSliderChange);
this._view.off("release",this._onSliderRelease);this._view.off("grab",this._onSliderGrab);
this._player.off("play",this._onPlay);this._player.off("pause",this._onPause);this._player.off("ended",this._onPause)
};h.destroy=function(){this._removeEventListeners();c(this._timeUpdateInterval)
};b.exports=j},{"./BaseBehavior":291,"@marcom/ac-raf-emitter/cancelDraw":227,"@marcom/ac-raf-emitter/draw":228,"@marcom/ac-string/supplant":268}],299:[function(c,g,b){var f=c("./ButtonBehavior");
var a=function(i,j){f.apply(this,arguments);if(this._player.states){this._updateState()
}};var d=f.prototype;var h=a.prototype=Object.create(d);h._addPlayerListeners=function(){this._updateState=this._updateState.bind(this);
this._player.states&&this._player.states.on("statechange",this._updateState)};h._updateState=function(){this._stateChanging=false;
this._view.setState((this._player.states.getCurrentState()==="sharing")?"on":"off")
};h._onClick=function(){if(this._stateChanging){return}if(this._player.states.getCurrentState()==="sharing"){this._view.setState("off");
this._player.states.setState("none")}else{this._view.setState("on");this._player.states.setState("sharing")
}this._stateChanging=true};h.destroy=function(){this._player.states&&this._player.states.off("statechange",this._updateState);
d.destroy.call(this)};g.exports=a},{"./ButtonBehavior":292}],300:[function(c,f,b){var a=c("./BaseBehavior");
var i=c("../sharing/SharingModule");var h=function(j,k){a.apply(this,arguments);
this._updateState()};var d=a.prototype;var g=h.prototype=Object.create(d);g._updateState=function(){this.sharingModule=new i(Object.assign({},{player:this._player,parentView:this._view}));
this.sharingModule.setData(this._player.options.sharing);this._view.el.innerHTML="";
this._view.el.appendChild(this.sharingModule.el)};f.exports=h},{"../sharing/SharingModule":317,"./BaseBehavior":291}],301:[function(b,d,a){var c=b("./BaseBehavior");
var f=function(h,i){c.apply(this,arguments);this._hideVolume();this._updateSliderVolumeValue()
};var g=f.prototype=Object.create(c.prototype);g._addViewListeners=function(){this._showVolume=this._showVolume.bind(this);
this._hideVolume=this._hideVolume.bind(this);this._onSliderGrab=this._onSliderGrab.bind(this);
this._onSliderChange=this._onSliderChange.bind(this);this._onSliderRelease=this._onSliderRelease.bind(this);
this._onFocusChange=this._onFocusChange.bind(this);this._view.on("grab",this._onSliderGrab);
this._view.on("focuschange",this._onFocusChange)};g._addPlayerListeners=function(){this._updateSliderVolumeValue=this._updateSliderVolumeValue.bind(this);
this._onUserVolumeChange=this._onUserVolumeChange.bind(this);this._player.once("durationchange",this._updateSliderVolumeValue);
this._player.on("volumechange",this._updateSliderVolumeValue);this._player.on("uservolumechange",this._onUserVolumeChange)
};g._onSliderGrab=function(){this._cachedVolume=this._player.getVolume();this._player.off("volumechange",this._updateSliderVolumeValue);
this._view.off("grab",this._onSliderGrab);this._view.on("change",this._onSliderChange);
this._view.on("release",this._onSliderRelease)};g._onSliderRelease=function(){this._setPlayerVolume(this._view.getValue());
this._view.off("change",this._onSliderChange);this._view.off("release",this._onSliderRelease);
this._view.on("grab",this._onSliderGrab);this._player.on("volumechange",this._updateSliderVolumeValue)
};g._onSliderChange=function(){var h=this._view.getValue();this._setPlayerVolume(h);
this._view.setScrubbedValue()};g._setPlayerVolume=function(h){if(h){this._player.setMuted(false);
this._player.setVolume(h/100)}else{this._player.setMuted(true);this._player.setVolume(this._cachedVolume)
}};g._showVolume=function(){this._view.show()};g._hideVolume=function(){this._view.hide()
};g._onUserVolumeChange=function(){this._showVolume();clearTimeout(this._hideVolumeTimer);
if(!this._view.isFocused()){this._hideVolumeTimer=setTimeout(this._hideVolume,1000)
}};g._onFocusChange=function(){if(!this._view.isFocused()){this._hideVolume()}else{this._showVolume()
}};g._updateSliderVolumeValue=function(){if(this._player.getMuted()){this._view.setValue(0);
this._view.setScrubbedValue()}else{var h=this._player.getVolume();this._view.setValue(h*100);
this._view.setScrubbedValue()}};g._removeEventListeners=function(){this._player.off("durationchange",this._updateSliderVolumeValue);
this._player.off("volumechange",this._updateSliderVolumeValue);this._player.off("uservolumechange",this._onUserVolumeChange);
this._view.off("change",this._onSliderChange);this._view.off("release",this._onSliderRelease);
this._view.off("grab",this._onSliderGrab)};g.destroy=function(){this._removeEventListeners()
};d.exports=f},{"./BaseBehavior":291}],302:[function(c,d,b){var f=c("../../dom-emitter/DOMEmitterMicro");
var a=function(g){this.el=g};a.prototype=Object.create(f.prototype);d.exports=a
},{"../../dom-emitter/DOMEmitterMicro":269}],303:[function(c,d,b){var a=function(g){this.el=g
};var f=a.prototype;f.show=function(){this.el.classList.remove("hidden")};f.hide=function(){this.el.classList.add("hidden")
};d.exports=a},{}],304:[function(b,c,a){var f=function(g){this.el=g};var d=f.prototype;
d.setText=function(g){this.el.innerHTML=g};c.exports=f},{}],305:[function(b,c,a){var f=b("@marcom/ac-slider").Slider;
var h="ac-slider-inactive";var d=function(k,j){this.el=k;this._min=j.min||0;this._max=j.max||1;
if(j.mixins){var i=j.mixins.slice(0);while(i.length){Object.assign(this,i.pop())
}}this._slider=new f(this.el,{template:j.template,min:this._min,max:this._max,step:isNaN(+this.el.getAttribute("step"))?this.el.getAttribute("step"):+this.el.getAttribute("step"),value:(j.value!==undefined)?j.value:(+this.el.getAttribute("value")),orientation:j.orientation,renderedPosition:true,keyboardContext:this.el});
this._onFocusChange=this._onFocusChange.bind(this);this._setHoveringValue=this._setHoveringValue.bind(this);
this._onMouseOver=this._onMouseOver.bind(this);this._onMouseLeave=this._onMouseLeave.bind(this);
this._slider.el.addEventListener("blur",this._onFocusChange);this._slider.el.addEventListener("focus",this._onFocusChange);
this._slider.el.addEventListener("mouseout",this._onFocusChange);this.forceCursorPointer=this.forceCursorPointer.bind(this);
this.disableForcedCursorPointer=this.disableForcedCursorPointer.bind(this);this._slider.on("grab",this.forceCursorPointer);
this._slider.on("release",this.disableForcedCursorPointer);this._scrubbedEl=this.el.querySelector(".ac-slider-scrubbed");
this._notchEl=this.el.querySelector(".ac-slider-hover-notch");if(this._notchEl){this._slider.el.addEventListener("mouseover",this._onMouseOver);
this._slider.el.addEventListener("mouseleave",this._onMouseLeave);this._slider.el.addEventListener("mousemove",this._setHoveringValue)
}if(j.value){requestAnimationFrame(function(){if(this._slider){this.setValue(j.value)
}}.bind(this))}};var g=d.prototype;g.on=function(){return this._slider.on.apply(this._slider,arguments)
};g.off=function(){return this._slider.off.apply(this._slider,arguments)};g.trigger=function(){return this._slider.trigger.apply(this._slider,arguments)
};g.setValue=function(i){return this._slider.setValue.call(this._slider,i)};g.setAriaValueText=function(i){this._slider.el.setAttribute("aria-valuetext",i)
};g.setMin=function(i){this._min=i;this._slider.setMin(i)};g.setMax=function(i){this._max=i;
this._slider.setMax(i)};g._onMouseOver=function(){this._slider.el.classList.add("hover")
};g._onMouseLeave=function(){this._slider.el.classList.remove("hover")};g._onFocusChange=function(){setTimeout(function(){this.trigger("focuschange")
}.bind(this),0)};g.isFocused=function(){return(this._slider.el===document.activeElement&&this._hasFocusOutline())
};g._hasFocusOutline=function(){return(getComputedStyle(this._slider.el).getPropertyValue("outline-style")!=="none")
};g.getValue=function(){return this._slider.getValue.apply(this._slider,arguments)
};g.getMax=function(){return this._max};g.setScrubbedValue=function(){if(this._slider.getOrientation()==="horizontal"){this._scrubbedEl.style.left=this._slider.thumbElement.style.left
}else{this._scrubbedEl.style.bottom=this._slider.thumbElement.style.bottom}};g._setHoveringValue=function(i){var j=this.getClientXValue(i,this._notchEl);
this._notchEl.style.left=((j/this.getMax())*100)+"%";this._setNotchColor(j)};g._setNotchColor=function(i){if(i>this.getValue()){this._notchEl.style.backgroundColor="#fff"
}else{this._notchEl.style.backgroundColor="#333"}};g.show=function(){this.el.classList.remove(h)
};g.hide=function(){this.el.classList.add(h)};g.setState=function(i){this.el.classList.add(i)
};g.clearState=function(i){this.el.classList.remove(i)};g.getClientXValue=function(i,j){return this._slider.getClientXValue(i,j)
};g.destroy=function(){this._slider.el.removeEventListener("mousemove",this._setHoveringValue);
this._slider.el.removeEventListener("mouseleave",this._onMouseOver);this._slider.el.removeEventListener("mouseout",this._onMouseLeave);
this._slider.el.removeEventListener("blur",this._onFocusChange);this._slider.el.removeEventListener("focus",this._onFocusChange);
this._slider.el.removeEventListener("mouseout",this._onFocusChange);this._slider.off("grab",this.forceCursorPointer);
this._slider.off("release",this.disableForcedCursorPointer);this._slider.destroy();
this._slider=null};c.exports=d},{"@marcom/ac-slider":242}],306:[function(c,d,b){var a=c("./Button");
var g=function(i,h){a.apply(this,arguments);this._states=h.states||{};this._labels=h.labels;
this._focusTarget=this.el.querySelector("button")||this.el;if(this._states&&this._states.initial){this.setState("initial")
}};var f=g.prototype=Object.create(a.prototype);f.setState=function(h){if(this._currentState&&this._currentState!==h&&this._states[this._currentState].length){this.el.classList.remove(this._states[this._currentState])
}this._currentState=h;if(this._labels&&this._labels[this._currentState]){this._focusTarget.value=this._labels[this._currentState];
this._focusTarget.setAttribute("aria-label",this._labels[this._currentState])}if(this._currentState==="on"){this._focusTarget.setAttribute("aria-pressed",true)
}else{this._focusTarget.setAttribute("aria-pressed",false)}if(this._states[h].length){this.el.classList.add(this._states[h])
}};d.exports=g},{"./Button":302}],307:[function(b,c,a){var d="cursor-pointer";c.exports={disableForcedCursorPointer:function(){document.body.classList.remove(d);
this.onSelectStartResumeDefault()},forceCursorPointer:function(){document.body.classList.add(d);
this.onSelectStartPreventDefault()},onSelectStartResumeDefault:function(){document.removeEventListener("selectstart",this.preventDefault)
},onSelectStartPreventDefault:function(){document.addEventListener("selectstart",this.preventDefault)
},preventDefault:function(f){f.preventDefault()}}},{}],308:[function(c,d,b){var a=function(i,k,j){return new k.classDef(i,Object.assign(k.options||{},j||{}))
};var g=function(k,j,i){return function(l){k[j](l,i)}};var h=function(v,u){var m=u.handlers||{};
var p={};for(var x in m){if(m.hasOwnProperty(x)){v.on(x,p[x]=g(m,x,v))}}var n=u.observe;
var s;if(n){var o=n.update;var j=n.source;var t=j.on.bind(j)||j.addEventListener;
var k=j.off.bind(j)||j.removeEventListener;var y=n.events;var q=0;var r=y.length;
var l=function(){o.call(n,v)};for(;q<r;q++){x=y[q];t(x,l)}s=function(){for(q=0;
q<r;q++){x=y[q];k(x,l)}}}var w=function(){for(var i in p){if(p.hasOwnProperty(i)){v.off(i,p[i])
}}if(s){s()}};return{destroy:w}};d.exports=function f(i,k,j){if(k.classDef){return a(i,k,j)
}else{return h(i,k,j)}}},{}],309:[function(d,b,g){var f=d("./createView");var c=d("./createBehavior");
var h=function(l,m){if(typeof m.destroy==="function"){m.destroy()}if(typeof l.destroy==="function"){l.destroy()
}};var i=function(l){while(l.length){l.shift().destroy()}};var k=function(l){for(var m in l){if(l.hasOwnProperty(m)){i(l[m]);
delete l[m]}}};var a=function(n,p,m){var l=f(n,p.view);var o=c(l,p.behavior,m);
return{view:l,behavior:o,destroy:h.bind(null,l,o)}};b.exports=function j(u,o,t){var q={};
for(var s in o){if(o.hasOwnProperty(s)&&typeof o[s]==="object"){var m=o[s];var l=(o.elementClassPrefix)?("."+o.elementClassPrefix+"-"+m.className):"."+m.className;
var n=u.querySelectorAll(l);q[s]=[];var p=0;var r=n.length;for(;p<r;p++){q[s].push(a(n[p],m,t))
}}}return{components:q,destroy:k.bind(null,q)}}},{"./createBehavior":308,"./createView":310}],310:[function(c,d,a){d.exports=function b(f,g){return new g.classDef(f,g.options)
}},{}],311:[function(b,c,a){c.exports={backthirtyseconds:"Back 30 Seconds",playpause:"Play/Pause",play:"Play",pause:"Pause",togglemutevolume:"Toggle Mute Volume",mutevolume:"Mute Volume",minvolume:"Minimum Volume",adjustvolume:"Adjust Volume",fastreverse:"Fast Reverse",fastforward:"Fast Forward",fullvolume:"Full Volume",fullscreen:"Full Screen",exitfullscreen:"Exit Full Screen",airplay:"AirPlay",captionscontrol:"Closed Captions",captionsturnedon:"Closed Captions On",captionsturnedoff:"Closed Captions Off",subtitlescontrol:"Subtitles",subtitlesturnedon:"Subtitles On",subtitlesturnedoff:"Subtitles Off",sizescontrol:"Video Size",downloadcontrol:"Download Video",share:"Share",small:"Small",medium:"Medium",large:"Large",hd:"HD",ipod:"iPod/iPhone",mb:"MB",gb:"GB",tb:"TB",downloadquicktimetitle:"Get QuickTime.",downloadquicktimetext:"Download QuickTime to view this video. QuickTime is free for Mac + PC.",downloadquicktimebutton:"Download",downloadquicktimeurl:"https://www.apple.com/quicktime/download/",elapsed:"elapsed",remaining:"remaining",currenttimetext:"{minutes} minutes and {seconds} seconds",pictureinpicture:"Picture-in-Picture",exitpictureinpicture:"Exit Picture-in-Picture",closesharing:"Close Sharing",facebookshare:"Share to Facebook",twittershare:"Share to Twitter",copylink:"Copy Link",copyembed:"Copy Embed Code",copyarea:"Copy Link Text Area",selectlink:"Select Link Text",selectembed:"Select Embed Code",close:"Close",dismisscopy:"Dismiss Copy",replay:"Replay",livestream:"Live Streaming",newwindow:"Opens in New Window"}
},{}],312:[function(d,b,h){var n=d("./Translations");var i=d("./DefaultLabelStrings");
var g=window.document.documentElement;var f;try{f=window.top.document.documentElement
}catch(k){f=g}var r=d("@marcom/ac-ajax-xhr");var c="m";var o="/global/ac_"+c+"edia_player/scripts/ac_"+c+"edia_languages/";
var a="en-US";var l={};var q=function(u){var m;try{m=u||f.getAttribute("lang")}catch(s){m=g.getAttribute("lang")
}var t;if(!m){t=a}else{switch(m.toLowerCase()){case"es-418":t="es-LA";break;case"pt":t="pt-BR";
break;default:t=m;break}}return t};var j=function(m){m=q(m);return(l[m]!==undefined)
};var p=function(s){s=s||{};var u=q(s.lang);if(j(u)){if(s.callback){s.callback(l[u]);
return}else{return l[u]}}else{if(!s.callback){throw new Error("To use Localization.getTranslation you must either pass a callback or ensure the translation is ready via Localization.translationReady")
}}var t=s.basePath||o;var m=(n[u])?(t+n[u]):(t+n[a]);var v=i;r.get(m,{success:function(w){v=Object.assign(v,JSON.parse(w));
l[u]=v;s.callback(v)},error:function(){l[u]=v;s.callback(v)}})};b.exports={getLanguage:q,getTranslation:p,translationReady:j}
},{"./DefaultLabelStrings":311,"./Translations":313,"@marcom/ac-ajax-xhr":182}],313:[function(b,c,a){c.exports={"bg-BG":"bg-BG.json","cs-CZ":"cs-CZ.json","el-GR":"el-GR.json","de-AT":"de-AT.json","de-CH":"de-CH.json","de-DE":"de-DE.json","de-LI":"de-LI.json","da-DK":"da-DK.json",en:"en.json","en-US":"en-US.json","en-AP":"en-AP.json","en-CA":"en-CA.json","en-GB":"en-GB.json","en-HK":"en-HK.json","en-IE":"en-IE.json","en-IN":"en-IN.json","en-KR":"en-KR.json","en-AU":"en-AU.json","en-NZ":"en-NZ.json","en-SG":"en-SG.json","en-ZA":"en-ZA.json",es:"es.json","es-LA":"es-LA.json","es-MX":"es-MX.json","es-ES":"es-ES.json","et-EE":"et-EE.json","fi-FI":"fi-FI.json",fr:"fr.json","fr-BE":"fr-BE.json","fr-CA":"fr-CA.json","fr-CH":"fr-CH.json","fr-FR":"fr-FR.json","hr-HR":"hr-HR.json","hu-HU":"hu-HU.json","it-IT":"it-IT.json",ja:"ja.json","ja-JP":"ja-JP.json","ko-KR":"ko-KR.json","lt-LT":"lt-LT.json","lv-LV":"lv-LV.json","nl-BE":"nl-BE.json","nl-NL":"nl-NL.json","no-NO":"no-NO.json","pl-PL":"pl-PL.json",pt:"pt.json","pt-BR":"pt-BR.json","pt-PT":"pt-PT.json","ro-RO":"ro-RO.json","ru-RU":"ru-RU.json","sk-SK":"sk-SK.json","sv-SE":"sv-SE.json","tr-TR":"tr-TR.json",zh:"zh.json","zh-CN":"zh-CN.json","zh-HK":"zh-HK.json","zh-TW":"zh-TW.json"}
},{}],314:[function(c,d,b){var g=c("./PopUp");var a=function(h){this.el=h.el;this._player=h.player;
this._popUp=new g(h);this.el.appendChild(this._popUp.el)};var f=a.prototype;f.setData=function(h){this._popUp.setData(h)
};f.show=function(){this.el.classList.remove("hidden")};f.hide=function(){this.el.classList.add("hidden")
};f.destroy=function(){};d.exports=a},{"./PopUp":315}],315:[function(b,a,d){var k='<div class="ac-video-trickplay hidden" aria-hidden="true">\n    <div class="ac-video-trickplay-image">\n    </div>\n    <div class="ac-video-trickplay-time"></div>\n</div>\n';
var g=b("../../utils/Time");var h=b("./ThumbnailHandler");var i=b("@marcom/ac-function/throttle");
var c=5;var j=function(l){this._player=l.player;this.el=document.createElement("div");
this.el.style.opacity="0";this.el.innerHTML=k;this._thumbnailHandler=new h({el:this.el.querySelector(".ac-video-trickplay-image"),player:this._player,numberOfImages:l.numberOfImages});
this._timeLabel=this.el.querySelector(".ac-video-trickplay-time");this._bindMethods();
this._addEventListeners()};var f=j.prototype;f._initPointerTracking=function(){this._scrubberView=this._player.controls.scrubberView;
if(!this._scrubberView){return}this._runnableTrack=this._scrubberView.el.querySelector(".ac-slider-runnable-track");
this._calcOffsets();this._scrubberView.el.addEventListener("mouseover",this._show);
this._scrubberView.el.addEventListener("mouseout",this._hide);this._scrubberView.el.addEventListener("mousedown",this._startScrubbing);
this._scrubberView.el.addEventListener("mouseup",this._endScrubbing);this._scrubberView.el.addEventListener("mousemove",this._onTrackerUpdate);
this._scrubberView.el.addEventListener("mousemove",this._setThumbnail);this._player.on("resize",this._calcOffsets);
window.addEventListener("resize",this._calcOffsets)};f._bindMethods=function(){this._show=this._show.bind(this);
this._hide=this._hide.bind(this);this._onDurationChange=this._onDurationChange.bind(this);
this._onLoadedMetaData=this._onLoadedMetaData.bind(this);this._startScrubbing=this._startScrubbing.bind(this);
this._endScrubbing=this._endScrubbing.bind(this);this._initPointerTracking=this._initPointerTracking.bind(this);
this._onTrackerUpdate=this._onTrackerUpdate.bind(this);this._setThumbnail=this._setThumbnail.bind(this);
this._calcOffsets=this._calcOffsets.bind(this);this._debouncedCalcOffsets=i(this._calcOffsets,30)
};f._startScrubbing=function(l){this._thumbnailHandler.el.classList.add("hidden");
this._scrubberView.el.removeEventListener("mousemove",this._setThumbnail);this._scrubberView.el.removeEventListener("mouseout",this._hide);
document.addEventListener("mouseup",this._endScrubbing);document.addEventListener("mousemove",this._onTrackerUpdate)
};f._endScrubbing=function(l){if(l.target===this._scrubberView.el){this._hide()
}this._scrubberView.el.addEventListener("mousemove",this._setThumbnail);this._scrubberView.el.addEventListener("mouseout",this._hide);
document.removeEventListener("mouseup",this._endScrubbing);document.removeEventListener("mousemove",this._onTrackerUpdate);
this._setThumbnail(l);this._thumbnailHandler.el.classList.remove("hidden")};f._calcOffsets=function(){this._onLoadedMetaData();
var m=this._player.el.getBoundingClientRect();this._offsetLeft=m.left;var l=this._runnableTrack.getBoundingClientRect();
this._leftBoundary=l.left-this._offsetLeft+c;this._rightBoundary=this._leftBoundary+l.width-c-2;
this._imgWidth=this.el.firstElementChild.getBoundingClientRect().width};f._onLoadedMetaData=function(){var l=this._player.getMediaElement().videoWidth;
var m=this._player.getMediaElement().videoHeight;this.el.classList.remove("square-video");
this.el.classList.remove("vertical-video");if(l<m){this.el.classList.add("vertical-video");
this._thumbnailHandler.setVertical(true)}else{if(l===m){this.el.classList.add("square-video");
this._thumbnailHandler.setVertical(false)}else{this._thumbnailHandler.setVertical(false)
}}};f._addEventListeners=function(){this._player.on("durationchange",this._onDurationChange);
this._player.once("controlsready",this._initPointerTracking);this._player.on("loadedmetadata",this._calcOffsets)
};f._removeEventListeners=function(){this._player.off("durationchange",this._onDurationChange);
this._player.off("controlsready",this._initPointerTracking);this._player.off("timeupdate",this._calcOffsets);
this._player.off("resize",this._debouncedCalcOffsets);window.removeEventListener("resize",this._debouncedCalcOffsets);
this._scrubberView.el.removeEventListener("mouseover",this._show);this._scrubberView.el.removeEventListener("mouseout",this._hide);
this._scrubberView.el.removeEventListener("mousemove",this._onTrackerUpdate);this._scrubberView.el.removeEventListener("mousemove",this._setThumbnail)
};f._onTrackerUpdate=function(m){this._calcOffsets();var l=Math.min(Math.max(m.clientX-this._offsetLeft,this._leftBoundary),this._rightBoundary);
this.el.firstElementChild.style.left=(l-(this._imgWidth/2))+"px";var n=this._scrubberView.getClientXValue(m);
if(this._player.getReadyState()<=2){this._cachedTrackerUpdate=m}else{this._cachedTrackerUpdate=null
}this._setTime(Math.max(n,0))};f._onDurationChange=function(l){this._cachedDuration=this._player.getDuration();
if(this._cachedTrackerUpdate){this._onTrackerUpdate(this._cachedTrackerUpdate);
this._setThumbnail()}this.el.style.opacity="1"};f._setThumbnail=function(l){this._thumbnailHandler.setTime(this._time,this._cachedDuration)
};f._setTime=function(l){var n=(l/this._scrubberView.getMax());this._time=Math.min(n*this._cachedDuration,this._cachedDuration);
var m=g.formatTime(Math.round(this._time),this._cachedDuration);this._timeLabel.innerHTML=m
};f.setData=function(l){this.el.style.opacity="0";if(this._canPlayThroughHander){this._player.off("canplaythrough",this._canPlayThroughHander);
this._player.off("playing",this._canPlayThroughHander);this._canPlayThroughHander=null
}if(l&&this._player.getReadyState()>2){this.el.style.opacity="1";this._thumbnailHandler.setData(l);
if(this._cachedTrackerUpdate){this._onTrackerUpdate(this._cachedTrackerUpdate);
this._setThumbnail()}}else{this._thumbnailHandler.setData(null);if(l){this._canPlayThroughHander=this.setData.bind(this,l);
this._player.on("canplaythrough",this._canPlayThroughHander);this._player.on("playing",this._canPlayThroughHander)
}else{this.el.style.opacity="1"}}this._onLoadedMetaData()};f._show=function(l){this._onTrackerUpdate(l);
this.el.firstElementChild.classList.remove("hidden")};f._hide=function(){this.el.firstElementChild.classList.add("hidden")
};f.destroy=function(){if(this._canPlayThroughHander){this._player.off("canplaythrough",this._canPlayThroughHander);
this._player.off("playing",this._canPlayThroughHander)}this._tracker.destroy()};
a.exports=j},{"../../utils/Time":319,"./ThumbnailHandler":316,"@marcom/ac-function/throttle":42}],316:[function(d,g,c){var f=120;
var a=144;var b=81;var h=function(j){this.el=j.el;this._player=j.player;this._imgWidth=j.imgWidth||a;
this.el.style.backgroundSize=(this._numberOfImages*100)+"% 100%"};var i=h.prototype;
i.setVertical=function(j){this._imgWidth=(j)?b:a};i.getWidth=function(){return this._imgWidth
};i.setData=function(j){if(!j){this._imgUrl=null;this.el.style.backgroundImage="";
return}else{if(j.url===this._imgUrl){return}}if(this._imageLoadPromise){this._imageLoadPromise.cancel()
}this._imgUrl=j.url;this._numberOfImages=parseInt(j.numberOfImages||f);this.el.style.backgroundSize=(this._numberOfImages*100)+"% 100%";
this.el.style.backgroundImage="";this.el.classList.add("hidden");this._imageLoadPromise=this._loadImage(this._imgUrl).then(function(){this.el.style.backgroundImage='url("'+this._imgUrl+'")';
this._imageLoadPromise=null;this.el.classList.remove("hidden")}.bind(this))};i._loadImage=function(j){return new Promise(function(m,l){var k=new Image();
k.onload=function(){m()};k.onerror=function(){l()};k.src=j})};i.setTime=function(n,j){var m=n/j;
var k=Math.min(Math.round(m*this._numberOfImages),this._numberOfImages-1);var l=(k/(this._numberOfImages-1))*100;
this.el.style.backgroundPositionX=l+"%"};i.destroy=function(){if(this._imageLoadPromise){this._imageLoadPromise.cancel()
}};g.exports=h},{}],317:[function(b,c,a){(function(f){var n=f("PGRpdiBjbGFzcz0ic2hhcmluZy1zdGF0ZSI+CiAgICA8ZGl2IGNsYXNzPSJjb250YWluZXIiIGRhdGEtYWN2LWFjdGl2ZS1hcmVhPgogICAgICAgIDxkaXYgY2xhc3M9InNoYXJpbmctY29udGFpbmVyIj4KICAgICAgICAgICAgPGRpdiBjbGFzcz0ic2hhcmluZy1idXR0b24tY29udGFpbmVyIj4KICAgICAgICAgICAgICAgIDxidXR0b24gY2xhc3M9ImZhY2Vib29rLXNoYXJlIGFjLXZpZGVvLWljb24gaWNvbi1zaGFyZV9mYiIgYXJpYS1sYWJlbD0ie2ZhY2Vib29rc2hhcmV9LCB7bmV3d2luZG93fSI+PC9idXR0b24+CiAgICAgICAgICAgICAgICA8YnV0dG9uIGNsYXNzPSJ0d2l0dGVyLXNoYXJlIGFjLXZpZGVvLWljb24gaWNvbi1zaGFyZV90d2l0dGVyIiBhcmlhLWxhYmVsPSJ7dHdpdHRlcnNoYXJlfSwge25ld3dpbmRvd30iPjwvYnV0dG9uPgogICAgICAgICAgICAgICAgPGJ1dHRvbiBjbGFzcz0iY29weS1saW5rIGFjLXZpZGVvLWljb24gaWNvbi1zaGFyZV9saW5rIiBhcmlhLWxhYmVsPSJ7Y29weWxpbmt9Ij48L2J1dHRvbj4KICAgICAgICAgICAgICAgIDxidXR0b24gY2xhc3M9ImNvcHktZW1iZWQtY29kZSBhYy12aWRlby1pY29uIGljb24tc2hhcmVfZW1iZWQiIGFyaWEtbGFiZWw9Intjb3B5ZW1iZWR9Ij48L2J1dHRvbj4KICAgICAgICAgICAgPC9kaXY+CiAgICAgICAgPC9kaXY+CiAgICAgICAgPGRpdiBjbGFzcz0idGV4dGFyZWEtY29udGFpbmVyIj4KICAgICAgICAgICAgPHNwYW4+CiAgICAgICAgICAgICAgICA8aW5wdXQgY2xhc3M9ImNvcHktYXJlYSBmb3JtLXRleHRib3ggZm9ybS10ZXh0Ym94LXRleHQgZGlzYWJsZWQiIHR5cGU9InRleHQiIGlkPSJjb3B5LWxpbmsiIGFyaWEtbGFiZWw9Intjb3B5bGlua30iPjwvaW5wdXQ+CiAgICAgICAgICAgICAgICA8YnV0dG9uIGNsYXNzPSJ0ZXh0aW5wdXQtY2xvc2UtYnV0dG9uIGFjLXZpZGVvLWljb24gaWNvbi1zaGFyZV9jbG9zZSIgYXJpYS1sYWJlbD0ie2Rpc21pc3Njb3B5fSI+PC9idXR0b24+CiAgICAgICAgICAgIDwvc3Bhbj4KICAgICAgICA8L2Rpdj4KICAgIDwvZGl2Pgo8L2Rpdj4K","base64").toString();
var j=f("PGlmcmFtZSBzcmM9IntlbWJlZENvZGVQYXRofXt2aWRlb2lkfXtleHRlbnNpb259IiB3aWR0aD0ie3dpZHRofSIgaGVpZ2h0PSJ7aGVpZ2h0fSIgdGl0bGU9Int0aXRsZX0iIGFsbG93ZnVsbHNjcmVlbj48L2lmcmFtZT4K","base64").toString();
var w="https://www.apple.com/embed/";var m="Video Player";var k=b("@marcom/ac-console/log");
var r=b("@marcom/ac-clipboard/select");var g=b("@marcom/ac-social").Dialog;var s=b("@marcom/ac-string/supplant");
var v=b("../localization/Localization");var o=b("@marcom/ac-accessibility/helpers/TabManager");
var u;try{u=b("@marcom/ac-analytics-share/factory/create")}catch(h){k("ac-analytics-share failed to load, are you sure you've included it?")
}var t=b("@marcom/ac-useragent");var l=t.os;var p=l.ios||l.android;var d=735;var i=function(x){if(!this.el){this._initializeElement(x.el,x.template)
}this._player=x.player;this._parentView=x.parentView;this._clickedShareButton=null;
this._container=this.el.querySelector(".container");this._sharingButtonContainer=this.el.querySelector(".sharing-button-container");
this._facebookButton=this.el.querySelector(".facebook-share");this._twitterButton=this.el.querySelector(".twitter-share");
this._copyLinkButton=this.el.querySelector(".copy-link");this._copyEmbedCodeButton=this.el.querySelector(".copy-embed-code");
this._copyTextArea=this.el.querySelector(".copy-area");this._copyCloseButton=this.el.querySelector(".textinput-close-button");
this._closeButton=this.el.querySelector(".close-button");if(x.analytics===false){u=null
}if(p){this.el.firstChild.classList.add("mobile");this._player.on("loadstart",function(){if(this._getClientWidth()>d){this.el.firstChild.classList.add("mobile-large")
}}.bind(this))}this._bindMethods();this._addEventListeners();this._syncSocialShareHidden()
};var q=i.prototype;q._initializeElement=function(y,x){if(!y){this.el=document.createElement("div");
this._templateData=v.getTranslation();this.el.innerHTML=s((x||n).toString(),this._templateData)
}else{this.el=y}};q.setData=function(y){if(!y){this._parentView.hide();return}else{this._parentView.show()
}if(y.allowEmbed){this.el.firstChild.classList.add("embed-enabled")}this._sharingUrl=y.originatorUrl||window.location.href;
this._videoid=y.videoid;this._hideExtension=y.hideExtension;this._embedPath=y.embedpath||w;
this._hideFacebook=y.hideFacebookShare||false;this._hideTwitter=y.hideTwitterShare||false;
this._title=y.title||m;this._syncSocialShareHidden();this._container.classList.remove("textarea-active");
if(u&&y.analytics!==false&&y.videoid){try{this._initAnalyticsAttributes(y);if(!this._analyticsObserver){this._analyticsObserver=u({context:this.el})
}}catch(x){k("ac-analytics-share failed to load, are you sure you've included it?")
}}};q._bindMethods=function(){this._doFacebookShare=this._doSocialShare.bind(this,g.FACEBOOK_SHARE);
this._doTwitterShare=this._doSocialShare.bind(this,g.TWITTER_TWEET);this._copyUrl=this._copyUrl.bind(this);
this._copyEmbedCode=this._copyEmbedCode.bind(this);this._closeCopyArea=this._showTextArea.bind(this,false);
this._closeState=this._closeState.bind(this)};q._addEventListeners=function(){this._facebookButton&&this._facebookButton.addEventListener("click",this._doFacebookShare);
this._twitterButton&&this._twitterButton.addEventListener("click",this._doTwitterShare);
this._copyLinkButton&&this._copyLinkButton.addEventListener("click",this._copyUrl);
this._copyEmbedCodeButton&&this._copyEmbedCodeButton.addEventListener("click",this._copyEmbedCode);
this._copyCloseButton&&this._copyCloseButton.addEventListener("click",this._closeCopyArea);
this._closeButton&&this._closeButton.addEventListener("click",this._closeState)
};q._removeEventListeners=function(){this._facebookButton&&this._facebookButton.removeEventListener("click",this._doFacebookShare);
this._twitterButton&&this._twitterButton.removeEventListener("click",this._doTwitterShare);
this._copyLinkButton&&this._copyLinkButton.removeEventListener("click",this._copyUrl);
this._copyEmbedCodeButton&&this._copyEmbedCodeButton.removeEventListener("click",this._copyEmbedCode);
this._copyCloseButton&&this._copyCloseButton.removeEventListener("click",this._closeCopyArea);
this._closeButton&&this._closeButton.removeEventListener("click",this._closeState)
};q._syncSocialShareHidden=function(){if(this._facebookButton){if(this._hideFacebook){this._facebookButton.classList.add("hide-button")
}else{this._facebookButton.classList.remove("hide-button")}}if(this._twitterButton){if(this._hideTwitter){this._twitterButton.classList.add("hide-button")
}else{this._twitterButton.classList.remove("hide-button")}}};q._doSocialShare=function(x){this._clickedShareButton=null;
this._copyLinkButton.classList.remove("active");this._copyEmbedCodeButton.classList.remove("active");
this._showTextArea(false);g.create(x,{url:this._sharingUrl,title:this._title})};
q._showTextArea=function(x){if(x){this._container.classList.add("textarea-active");
r(this._copyTextArea);if(!p){this._copyTextArea.setAttribute("readonly","")}}else{this._container.classList.remove("textarea-active");
this._copyLinkButton.classList.remove("active");this._copyEmbedCodeButton.classList.remove("active");
this._copyTextArea.removeAttribute("readonly");if(this._clickedShareButton){this._clickedShareButton.focus()
}this._copyLinkButton.setAttribute("aria-label",this._templateData.copylink);this._copyEmbedCodeButton.setAttribute("aria-label",this._templateData.copyembed)
}};q._copyUrl=function(){this._clearTextArea();this._copyTextArea.value=this._sharingUrl;
this._copyLinkButton.classList.add("active");this._copyLinkButton.setAttribute("aria-label",this._templateData.selectlink);
this._showTextArea(true);this._clickedShareButton=this._copyLinkButton;this._copyTextArea.setAttribute("aria-label",this._templateData.copylink);
r(this._copyTextArea)};q._clearTextArea=function(){window.getSelection().removeAllRanges();
this._copyLinkButton.classList.remove("active");this._copyEmbedCodeButton.classList.remove("active");
this._copyTextArea.removeAttribute("readonly")};q._copyEmbedCode=function(){this._clearTextArea();
this._copyTextArea.value=s(j,{videoid:this._videoid,embedCodePath:this._embedPath,width:this._player.getMediaWidth(),height:this._player.getMediaHeight(),title:this._title,extension:this._hideExtension?"":".html"});
this._copyEmbedCodeButton.classList.add("active");this._copyEmbedCodeButton.setAttribute("aria-label",this._templateData.selectembed);
this._showTextArea(true);this._clickedShareButton=this._copyEmbedCodeButton;this._copyTextArea.setAttribute("aria-label",this._templateData.copyembed);
r(this._copyTextArea)};q._focusFirstButton=function(){if(!this._firstButton){this._firstButton=o.getTabbableElements(this._sharingButtonContainer)[0]
}this._firstButton.focus()};q.show=function(){return new Promise(function(y,x){requestAnimationFrame(function(){var z=function(){this.el.removeEventListener("transitionend",z);
if(focus){this._focusFirstButton()}y()}.bind(this);this.el.addEventListener("transitionend",z);
setTimeout(function(){this._container.classList.add("showing")}.bind(this))}.bind(this))
}.bind(this))};q.hide=function(){this._clickedShareButton=null;this._showTextArea(false);
return new Promise(function(z,y){var x=function(){this.el.removeEventListener("transitionend",x);
z()}.bind(this);this.el.addEventListener("transitionend",x);setTimeout(function(){this._container.classList.remove("showing")
}.bind(this))}.bind(this))};q._getClientHeight=function(){return this.el.clientHeight
};q._getClientWidth=function(){return this.el.clientWidth};q.destroy=function(){this._removeEventListeners()
};q._closeState=function(){this._showTextArea(false);if(this._player.getCurrentTime()===0||this._player.getEnded()){this._player.states.setState("initial")
}else{this._player.states.setState("none")}};q._getAnalyticsSource=function(){return"drawer"
};q._initAnalyticsAttributes=function(C){var B=[];this._facebookButton&&B.push({button:this._facebookButton,title:"facebook",events:"event85"});
this._twitterButton&&B.push({button:this._twitterButton,title:"twitter",events:"event84"});
this._copyLinkButton&&B.push({button:this._copyLinkButton,title:"copy-link",events:"event89"});
this._copyEmbedCodeButton&&B.push({button:this._copyEmbedCodeButton,title:"copy-embed-code",events:"event101"});
var z=(((C.url&&C.url.indexOf(".m3u8"))!==-1)?"m3u8":"mp4")+" via html5";var y=this._getAnalyticsSource();
var A=C.videoid;var x=document.head.querySelectorAll('meta[property="analytics-track"]');
x=x?(x[0].getAttribute("content")):"";B.forEach(function(D){D.button.setAttribute("data-analytics-click","");
D.button.setAttribute("data-analytics-share",JSON.stringify({title:A,events:D.events,prop2:x+" - "+A+" - "+D.title,prop18:z,eVar49:document.referrer,eVar54:document.location.href,eVar55:x+" - "+A,eVar70:y}))
}.bind(this))};c.exports=i}).call(this,b("buffer").Buffer)},{"../localization/Localization":312,"@marcom/ac-accessibility/helpers/TabManager":175,"@marcom/ac-analytics-share/factory/create":30,"@marcom/ac-clipboard/select":187,"@marcom/ac-console/log":32,"@marcom/ac-social":248,"@marcom/ac-string/supplant":268,"@marcom/ac-useragent":171,buffer:327}],318:[function(b,d,a){var h=b("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var g=function(i){h.call(this);this.el=i.el||document.body;this.breakpoints=i.breakpoints.sort(function(k,j){return k.minWidth-j.minWidth
});this._breakPointsLength=this.breakpoints.length;this._addClasses=i.addClass;
this._addEventListeners();this._onResize()};var c=h.prototype;var f=g.prototype=Object.create(c);
f.constructor=g;f._addEventListeners=function(){var i=this;this._boundOnResize=function(){i._onResize.apply(i,arguments)
};window.addEventListener("resize",this._boundOnResize);window.addEventListener("orientationchange",this._boundOnResize);
window.addEventListener("DOMContentLoaded",this._boundOnResize)};f._removeEventListeners=function(){window.removeEventListener("resize",this._boundOnResize);
window.removeEventListener("orientationchange",this._boundOnResize);window.addEventListener("DOMContentLoaded",this._boundOnResize)
};f._onResize=function(){var j=this.el.clientWidth;var i=this._currentBreakpoint;
if(i&&g.widthInBreakpoint(j,i)){return}var k=g.getBreakpointFromWidth(j,this.breakpoints,i,this._breakPointsLength);
if(this._addClasses){this._currentBreakpoint&&this.el.classList.remove(i.name);
this.el.classList.add(k.name)}this._currentBreakpoint=k;this.trigger("breakpointchange",k)
};f.getCurrentBreakpoint=function(){return this._currentBreakpoint};f.refresh=function(){this._onResize()
};f.destroy=function(){this._removeEventListeners();c.destroy.call(this)};g.getBreakpointFromElement=function(i,j){return g.getBreakpointFromWidth(i.clientWidth,j)
};g.getBreakpointFromWidth=function(o,m,n,p){var k=0;var j=p||m.length;for(;k<j;
k++){var l=m[k];if(l===n){continue}if(o>=l.minWidth&&o<=l.maxWidth){return l}}};
g.widthInBreakpoint=function(j,i){return(j>=i.minWidth&&j<=i.maxWidth)};d.exports=g
},{"@marcom/ac-event-emitter-micro":33}],319:[function(b,c,a){var f=b("@marcom/ac-string/supplant");
var d={addLeadingZero:function(h,g){g=g||2;if(h<10||g>2){h=String(h);while(h.length<g){h="0"+h
}}return h},formatTime:function(k,i,g){if(isNaN(k)){return"00:00"}k=this.splitTime(Math.floor(k),i,function(l){return this.addLeadingZero(l,g)
}.bind(this));var h;if(i>=3600){h="{PN}{hours}:{minutes}:{seconds}"}else{h="{PN}{minutes}:{seconds}"
}var j=f(h,{PN:k.negativeModifier,hours:k.hours,minutes:k.minutes,seconds:k.seconds});
return j},splitTime:function(k,g,h){h=h||function(l){return l};var j={negativeModifier:"",hours:0,minutes:0,seconds:0};
if(isNaN(k)){return j}j.negativeModifier=(k<0)?"-":"";k=Math.abs(k);j.hours=(g>=3600)?Math.floor(k/3600):0;
j.minutes=(j.hours)?Math.floor((k/60)%60):Math.floor(k/60);j.seconds=(k%60);for(var i in j){if(typeof j[i]!=="number"){continue
}if(i!=="hours"){j[i]=h(j[i])}}return j},stringToNumber:function(h){var i=0;var g=h.split(":");
while(g.length){if(g.length===3){i+=parseFloat(g.shift())*3600}else{if(g.length===2){i+=parseFloat(g.shift())*60
}else{i+=parseFloat(g.shift())}}}return i}};c.exports=d},{"@marcom/ac-string/supplant":268}],320:[function(b,c,a){var f=b("@marcom/ac-object/clone");
var d=function(){var h=Array.prototype.slice.call(arguments);if(h.length<2){return f(h[0])
}var g=f(h.shift(),true);var i=h.shift();for(var j in i){if(i.hasOwnProperty(j)){if(!g.hasOwnProperty(j)||typeof g[j]!=="object"){g[j]=i[j]
}else{if(typeof g[j]==="object"&&typeof i[j]==="object"){g[j]=d(g[j],i[j])}}}}if(h.length){return d.apply(null,[g].concat(h))
}else{return g}};c.exports=d},{"@marcom/ac-object/clone":212}],321:[function(b,c,a){c.exports=[{width:384,height:160,type:"baseline-high",suffix:"h"},{width:384,height:160,type:"small",suffix:"h"},{width:384,height:160,type:"baseline-low",suffix:"l"},{width:384,height:160,type:"baseline-medium",suffix:"m"},{width:480,height:200,type:"medium",suffix:"h"},{width:768,height:320,type:"large",suffix:""},{width:960,height:400,type:"large",suffix:""},{width:1536,height:640,type:"large",suffix:"h"},{width:1536,height:640,type:"large",suffix:"l"},{width:1920,height:800,type:"large",suffix:"l"},{width:1920,height:800,type:"large",suffix:"h"}]
},{}],322:[function(b,c,a){c.exports=[{width:416,height:234,type:"baseline-high",suffix:"h"},{width:416,height:234,type:"small",suffix:"h"},{width:416,height:234,type:"baseline-low",suffix:"l"},{width:416,height:234,type:"baseline-medium",suffix:"m"},{width:640,height:360,type:"medium",suffix:"h"},{width:848,height:480,type:"large",suffix:""},{width:960,height:540,type:"large",suffix:""},{width:1280,height:720,type:"large",suffix:"h"},{width:1280,height:720,type:"large",suffix:"l"},{width:1920,height:1080,type:"large",suffix:"l"},{width:1920,height:1080,type:"large",suffix:"h"}]
},{}],323:[function(b,c,a){c.exports=[{width:360,height:360,type:"baseline-high",suffix:"h"},{width:360,height:360,type:"small",suffix:"h"},{width:360,height:360,type:"baseline-low",suffix:"l"},{width:480,height:480,type:"medium",suffix:""},{width:540,height:540,type:"medium",suffix:""},{width:720,height:720,type:"large",suffix:"h"},{width:720,height:720,type:"large",suffix:"l"},{width:1080,height:1080,type:"large",suffix:"l"},{width:1080,height:1080,type:"large",suffix:"h"}]
},{}],324:[function(i,b,u){var t=i("@marcom/ac-string/supplant");var a=/_r[0-9].+\.mov$/;
var d=/_[0-9]+x[0-9].+\.mp4$/;var j=/_([0-9]+)x([0-9]+)/;var f=/-tpl-.*-/;var h=/-cc-[a-z].*-/;
var k=/-tft-.*-/;var s="m";var o="_{width}x{height}{suffix}."+s+"p4";var c="_{height}x{width}{suffix}."+s+"p4";
var q=i("./1X1AssetSizes");var n=i("./16X9AssetSizes");var p=i("./12X5AssetSizes");
var r=function(D,v,y,F){var E;var m;j.test(D);var w={};var z;w.width=parseInt(RegExp.$1,10);
w.height=parseInt(RegExp.$2,10);if(D.match(k)){E=p;m=1536}else{if(w.width===w.height){E=q;
m=1080}else{E=n;m=1280}}if(w.width<w.height){z=true}var C=E[0].width;var B=(F&&F.maxWidth)?Math.max(F.maxWidth,C):m;
if(!D){throw"Must provide an url to optimize"}if(v===undefined||isNaN(v)){throw"Must provide a width"
}if(v===0){v=w.width}if(y){E=E.filter(function(G){return G.type===y})}if(B<1920){E=E.filter(function(G){return G.width<=B
})}var x;if(!z){x=E.reduce(function(G,H){return Math.abs(H.width-v)<Math.abs(G.width-v)?H:G
})}else{x=E.reduce(function(G,H){return Math.abs(H.height-v)<Math.abs(G.height-v)?H:G
})}var A=o;if(z){A=c}if(D.match(d)){return D.replace(d,t(A,x))}else{if(D.match(a)){return D.replace(a,t(A,x))
}else{return D}}};var g=function(m){if(!m.match(h)){return null}if(m.match(d)){return{src:m.replace(d,"_cc.vtt"),srclang:"en"}
}else{if(m.match(a)){return{src:m.replace(a,"_cc.vtt"),srclang:"en"}}else{return null
}}};var l=function(m){if(!m.match(f)){return null}else{return{url:m.replace(d,"https://images.apple.com/ac/ac-films/5.1.0/scripts/_thumbnails.jpg")}
}};b.exports={getVideoSource:r,getCaptionsSource:g,getThumbnailImageSource:l}},{"./12X5AssetSizes":321,"./16X9AssetSizes":322,"./1X1AssetSizes":323,"@marcom/ac-string/supplant":268}],325:[function(b,a,d){var g=b("../dom-emitter/DOMEmitterMicro");
var i=b("../texttracks/createTextTracks");var c=b("@marcom/ac-console/log");var h=window.document;
var j=function(k){this._videoElement=(k&&k.mediaElement)?k.mediaElement:h.createElement("video");
this.options=k||{};this._textTracks=i(k);this._initElement();g.apply(this,[this._videoElement]);
this._forwardCaptionEvent=this._forwardCaptionEvent.bind(this);this._textTracksEmitter=this.getTextTracksEventEmitter();
this._textTracksEmitter.on("addtrack",this._forwardCaptionEvent);this._textTracksEmitter.on("change",this._forwardCaptionEvent);
this._textTracksEmitter.on("removetrack",this._forwardCaptionEvent)};var f=j.prototype=Object.create(g.prototype);
f._initElement=function(){this._videoElement.classList.add("ac-video-media-controller");
if(this.options.crossorigin!==null){this._videoElement.setAttribute("crossorigin",(this.options.crossorigin)?this.options.crossorigin:"anonymous")
}this._videoElement.setAttribute("preload",this.options.preload||"auto");this._videoElement.setAttribute("x-webkit-airplay","")
};f._forwardCaptionEvent=function(k){this.trigger(k.type)};f.load=function(m,k,l){if(l){m=m.map(function(n){return n+"#t="+l
})}this._createSourceTags(m);this._createTextTrackTags(k);this._videoElement.load()
};f._createSourceTags=function(n){this._videoElement.removeAttribute("src");this._videoElement.innerHTML="";
var l=0;var k=n.length;if(k){this._videoElement.setAttribute("src",n[0])}for(;l<k;
l++){var m=h.createElement("source");m.src=n[l];this._videoElement.appendChild(m)
}};f.play=function(){try{var l=this._videoElement.play();if(l&&typeof l["catch"]==="function"){l["catch"](function(m){if(this._playPromise===l){this.trigger("PlayPromiseError")
}}.bind(this))}this._playPromise=l}catch(k){c(k)}};f.pause=function(){this._playPromise=null;
this._videoElement.pause()};f.addTextTrack=function(k){this._addTextTrackTag(k)
};f.removeTextTrack=function(k){this._removeTextTrackTag(k)};f.getMediaElement=function(){return this._videoElement
};f._createTextTrackTags=function(){return this._textTracks.create.apply(this,arguments)
};f._addTextTrackTag=function(){return this._textTracks.add.apply(this,arguments)
};f._removeTextTrackTag=function(){return this._textTracks.remove.apply(this,arguments)
};f.getTextTracks=function(){return this._textTracks.get.apply(this,arguments)};
f.getTextTracksEventEmitter=function(){return this._textTracks.getEmitter.apply(this,arguments)
};f.getReadyState=function(){return this._videoElement.readyState};f.getPreload=function(){return this._videoElement.preload
};f.setPreload=function(k){return this._videoElement.preload=k};f.setPoster=function(k){this._videoElement.poster=k
};f.getVolume=function(){return this._videoElement.volume};f.getMuted=function(){return this._videoElement.muted
};f.getPaused=function(){return this._videoElement.paused};f.getCurrentTime=function(){return this._videoElement.currentTime
};f.getDuration=function(){return this._videoElement.duration};f.setCurrentTime=function(k){return this._videoElement.currentTime=k
};f.setVolume=function(k){return this._videoElement.volume=k};f.setMuted=function(k){this._videoElement.muted=k
};f.getEnded=function(){return this._videoElement.ended};f.setSrc=function(k){if(!this._videoElement.childNodes.length||k!==this._getSrcNode().url){this._createSourceTags([k])
}};f.getCurrentSrc=function(){return this._getSrcNode()};f._getSrcNode=function(){return this._videoElement.childNodes[0]
};f.setControls=function(k){if(!k){this._videoElement.removeAttribute("controls");
this._videoElement.setAttribute("aria-hidden","true")}else{this._videoElement.setAttribute("controls","");
this._videoElement.removeAttribute("aria-hidden")}};f.isFullscreen=function(){return this._videoElement.webkitDisplayingFullscreen
};f.supportsPictureInPicture=function(){return(typeof this._videoElement.webkitSetPresentationMode==="function")
};f.isPictureInPicture=function(){return(this._videoElement.webkitPresentationMode==="picture-in-picture")
};f.setPictureInPicture=function(k){if(!this.supportsPictureInPicture()){return
}this._videoElement.webkitSetPresentationMode((k)?"picture-in-picture":"inline")
};f.supportsAirPlay=function(){return !!window.WebKitPlaybackTargetAvailabilityEvent
};f.destroy=function(){this._textTracks.destroy();this._textTracksEmitter.off("addtrack",this._forwardCaptionEvent);
this._textTracksEmitter.off("change",this._forwardCaptionEvent);this._textTracksEmitter.off("removetrack",this._forwardCaptionEvent);
this._textTracks=null;this._textTracksEmitter=null;this._videoElement=null};a.exports=j
},{"../dom-emitter/DOMEmitterMicro":269,"../texttracks/createTextTracks":283,"@marcom/ac-console/log":32}],326:[function(c,f,a){var d=c("./HTML5Video");
var b=function(){};var g=b.prototype;g.create=function(i,h){return new d(Object.assign({},i,{parentElement:h}))
};f.exports=Object.create(b.prototype)},{"./HTML5Video":325}],327:[function(aR,a2,T){
/*!
 * The buffer module from node.js, for the browser.
 *
 * @author   Feross Aboukhadijeh <https://feross.org>
 * @license  MIT
 */
;
"use strict";var aF=aR("base64-js");var b=aR("ieee754");T.Buffer=aD;T.SlowBuffer=aQ;
T.INSPECT_MAX_BYTES=50;var U=2147483647;T.kMaxLength=U;aD.TYPED_ARRAY_SUPPORT=aJ();
if(!aD.TYPED_ARRAY_SUPPORT&&typeof console!=="undefined"&&typeof console.error==="function"){console.error("This browser lacks typed array (Uint8Array) support which is required by `buffer` v5.x. Use `buffer` v4.x if you require old browser support.")
}function aJ(){try{var a6=new Uint8Array(1);a6.__proto__={__proto__:Uint8Array.prototype,foo:function(){return 42
}};return a6.foo()===42}catch(a7){return false}}function M(a7){if(a7>U){throw new RangeError("Invalid typed array length")
}var a6=new Uint8Array(a7);a6.__proto__=aD.prototype;return a6}function aD(a6,a7,a8){if(typeof a6==="number"){if(typeof a7==="string"){throw new Error("If encoding is specified then the first argument must be a string")
}return ac(a6)}return Y(a6,a7,a8)}if(typeof Symbol!=="undefined"&&Symbol.species&&aD[Symbol.species]===aD){Object.defineProperty(aD,Symbol.species,{value:null,configurable:true,enumerable:false,writable:false})
}aD.poolSize=8192;function Y(a8,a6,a7){if(typeof a8==="number"){throw new TypeError('"value" argument must not be a number')
}if(ay(a8)){return am(a8,a6,a7)}if(typeof a8==="string"){return c(a8,a6)}return ae(a8)
}aD.from=function(a8,a6,a7){return Y(a8,a6,a7)};aD.prototype.__proto__=Uint8Array.prototype;
aD.__proto__=Uint8Array;function J(a6){if(typeof a6!=="number"){throw new TypeError('"size" argument must be a number')
}else{if(a6<0){throw new RangeError('"size" argument must not be negative')}}}function ai(a6,a8,a7){J(a6);
if(a6<=0){return M(a6)}if(a8!==undefined){return typeof a7==="string"?M(a6).fill(a8,a7):M(a6).fill(a8)
}return M(a6)}aD.alloc=function(a6,a8,a7){return ai(a6,a8,a7)};function ac(a6){J(a6);
return M(a6<0?0:aO(a6)|0)}aD.allocUnsafe=function(a6){return ac(a6)};aD.allocUnsafeSlow=function(a6){return ac(a6)
};function c(a7,a9){if(typeof a9!=="string"||a9===""){a9="utf8"}if(!aD.isEncoding(a9)){throw new TypeError('"encoding" must be a valid string encoding')
}var a8=aw(a7,a9)|0;var a6=M(a8);var ba=a6.write(a7,a9);if(ba!==a8){a6=a6.slice(0,ba)
}return a6}function I(a9){var a8=a9.length<0?0:aO(a9.length)|0;var a6=M(a8);for(var a7=0;
a7<a8;a7+=1){a6[a7]=a9[a7]&255}return a6}function am(a9,a7,a8){if(a7<0||a9.byteLength<a7){throw new RangeError("'offset' is out of bounds")
}if(a9.byteLength<a7+(a8||0)){throw new RangeError("'length' is out of bounds")
}var a6;if(a7===undefined&&a8===undefined){a6=new Uint8Array(a9)}else{if(a8===undefined){a6=new Uint8Array(a9,a7)
}else{a6=new Uint8Array(a9,a7,a8)}}a6.__proto__=aD.prototype;return a6}function ae(a8){if(aD.isBuffer(a8)){var a6=aO(a8.length)|0;
var a7=M(a6);if(a7.length===0){return a7}a8.copy(a7,0,0,a6);return a7}if(a8){if(aY(a8)||"length" in a8){if(typeof a8.length!=="number"||Z(a8.length)){return M(0)
}return I(a8)}if(a8.type==="Buffer"&&Array.isArray(a8.data)){return I(a8.data)}}throw new TypeError("First argument must be a string, Buffer, ArrayBuffer, Array, or array-like object.")
}function aO(a6){if(a6>=U){throw new RangeError("Attempt to allocate Buffer larger than maximum size: 0x"+U.toString(16)+" bytes")
}return a6|0}function aQ(a6){if(+a6!=a6){a6=0}return aD.alloc(+a6)}aD.isBuffer=function r(a6){return a6!=null&&a6._isBuffer===true
};aD.compare=function a1(a9,a8){if(!aD.isBuffer(a9)||!aD.isBuffer(a8)){throw new TypeError("Arguments must be Buffers")
}if(a9===a8){return 0}var a7=a9.length;var bb=a8.length;for(var ba=0,a6=Math.min(a7,bb);
ba<a6;++ba){if(a9[ba]!==a8[ba]){a7=a9[ba];bb=a8[ba];break}}if(a7<bb){return -1}if(bb<a7){return 1
}return 0};aD.isEncoding=function R(a6){switch(String(a6).toLowerCase()){case"hex":case"utf8":case"utf-8":case"ascii":case"latin1":case"binary":case"base64":case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return true;
default:return false}};aD.concat=function aX(ba,a9){if(!Array.isArray(ba)){throw new TypeError('"list" argument must be an Array of Buffers')
}if(ba.length===0){return aD.alloc(0)}var a8;if(a9===undefined){a9=0;for(a8=0;a8<ba.length;
++a8){a9+=ba[a8].length}}var a6=aD.allocUnsafe(a9);var bb=0;for(a8=0;a8<ba.length;
++a8){var a7=ba[a8];if(!aD.isBuffer(a7)){throw new TypeError('"list" argument must be an Array of Buffers')
}a7.copy(a6,bb);bb+=a7.length}return a6};function aw(a7,a8){if(aD.isBuffer(a7)){return a7.length
}if(aY(a7)||ay(a7)){return a7.byteLength}if(typeof a7!=="string"){a7=""+a7}var a6=a7.length;
if(a6===0){return 0}var a9=false;for(;;){switch(a8){case"ascii":case"latin1":case"binary":return a6;
case"utf8":case"utf-8":case undefined:return aT(a7).length;case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return a6*2;
case"hex":return a6>>>1;case"base64":return af(a7).length;default:if(a9){return aT(a7).length
}a8=(""+a8).toLowerCase();a9=true}}}aD.byteLength=aw;function L(a7,a9,a6){var a8=false;
if(a9===undefined||a9<0){a9=0}if(a9>this.length){return""}if(a6===undefined||a6>this.length){a6=this.length
}if(a6<=0){return""}a6>>>=0;a9>>>=0;if(a6<=a9){return""}if(!a7){a7="utf8"}while(true){switch(a7){case"hex":return ab(this,a9,a6);
case"utf8":case"utf-8":return aP(this,a9,a6);case"ascii":return F(this,a9,a6);case"latin1":case"binary":return al(this,a9,a6);
case"base64":return aH(this,a9,a6);case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return ak(this,a9,a6);
default:if(a8){throw new TypeError("Unknown encoding: "+a7)}a7=(a7+"").toLowerCase();
a8=true}}}aD.prototype._isBuffer=true;function a0(a7,a9,a6){var a8=a7[a9];a7[a9]=a7[a6];
a7[a6]=a8}aD.prototype.swap16=function C(){var a6=this.length;if(a6%2!==0){throw new RangeError("Buffer size must be a multiple of 16-bits")
}for(var a7=0;a7<a6;a7+=2){a0(this,a7,a7+1)}return this};aD.prototype.swap32=function a5(){var a6=this.length;
if(a6%4!==0){throw new RangeError("Buffer size must be a multiple of 32-bits")}for(var a7=0;
a7<a6;a7+=4){a0(this,a7,a7+3);a0(this,a7+1,a7+2)}return this};aD.prototype.swap64=function X(){var a6=this.length;
if(a6%8!==0){throw new RangeError("Buffer size must be a multiple of 64-bits")}for(var a7=0;
a7<a6;a7+=8){a0(this,a7,a7+7);a0(this,a7+1,a7+6);a0(this,a7+2,a7+5);a0(this,a7+3,a7+4)
}return this};aD.prototype.toString=function at(){var a6=this.length;if(a6===0){return""
}if(arguments.length===0){return aP(this,0,a6)}return L.apply(this,arguments)};
aD.prototype.equals=function E(a6){if(!aD.isBuffer(a6)){throw new TypeError("Argument must be a Buffer")
}if(this===a6){return true}return aD.compare(this,a6)===0};aD.prototype.inspect=function aU(){var a7="";
var a6=T.INSPECT_MAX_BYTES;if(this.length>0){a7=this.toString("hex",0,a6).match(/.{2}/g).join(" ");
if(this.length>a6){a7+=" ... "}}return"<Buffer "+a7+">"};aD.prototype.compare=function a1(bd,a6,a9,be,a7){if(!aD.isBuffer(bd)){throw new TypeError("Argument must be a Buffer")
}if(a6===undefined){a6=0}if(a9===undefined){a9=bd?bd.length:0}if(be===undefined){be=0
}if(a7===undefined){a7=this.length}if(a6<0||a9>bd.length||be<0||a7>this.length){throw new RangeError("out of range index")
}if(be>=a7&&a6>=a9){return 0}if(be>=a7){return -1}if(a6>=a9){return 1}a6>>>=0;a9>>>=0;
be>>>=0;a7>>>=0;if(this===bd){return 0}var bg=a7-be;var bf=a9-a6;var bc=Math.min(bg,bf);
var a8=this.slice(be,a7);var bb=bd.slice(a6,a9);for(var ba=0;ba<bc;++ba){if(a8[ba]!==bb[ba]){bg=a8[ba];
bf=bb[ba];break}}if(bg<bf){return -1}if(bf<bg){return 1}return 0};function ar(a6,ba,a8,a9,a7){if(a6.length===0){return -1
}if(typeof a8==="string"){a9=a8;a8=0}else{if(a8>2147483647){a8=2147483647}else{if(a8<-2147483648){a8=-2147483648
}}}a8=+a8;if(Z(a8)){a8=a7?0:(a6.length-1)}if(a8<0){a8=a6.length+a8}if(a8>=a6.length){if(a7){return -1
}else{a8=a6.length-1}}else{if(a8<0){if(a7){a8=0}else{return -1}}}if(typeof ba==="string"){ba=aD.from(ba,a9)
}if(aD.isBuffer(ba)){if(ba.length===0){return -1}return n(a6,ba,a8,a9,a7)}else{if(typeof ba==="number"){ba=ba&255;
if(typeof Uint8Array.prototype.indexOf==="function"){if(a7){return Uint8Array.prototype.indexOf.call(a6,ba,a8)
}else{return Uint8Array.prototype.lastIndexOf.call(a6,ba,a8)}}return n(a6,[ba],a8,a9,a7)
}}throw new TypeError("val must be string, number or Buffer")}function n(bd,a8,a9,a7,ba){var bg=1;
var bh=bd.length;var be=a8.length;if(a7!==undefined){a7=String(a7).toLowerCase();
if(a7==="ucs2"||a7==="ucs-2"||a7==="utf16le"||a7==="utf-16le"){if(bd.length<2||a8.length<2){return -1
}bg=2;bh/=2;be/=2;a9/=2}}function a6(bj,bk){if(bg===1){return bj[bk]}else{return bj.readUInt16BE(bk*bg)
}}var bc;if(ba){var bf=-1;for(bc=a9;bc<bh;bc++){if(a6(bd,bc)===a6(a8,bf===-1?0:bc-bf)){if(bf===-1){bf=bc
}if(bc-bf+1===be){return bf*bg}}else{if(bf!==-1){bc-=bc-bf}bf=-1}}}else{if(a9+be>bh){a9=bh-be
}for(bc=a9;bc>=0;bc--){var bi=true;for(var bb=0;bb<be;bb++){if(a6(bd,bc+bb)!==a6(a8,bb)){bi=false;
break}}if(bi){return bc}}}return -1}aD.prototype.includes=function G(a8,a6,a7){return this.indexOf(a8,a6,a7)!==-1
};aD.prototype.indexOf=function g(a8,a6,a7){return ar(this,a8,a6,a7,true)};aD.prototype.lastIndexOf=function aL(a8,a6,a7){return ar(this,a8,a6,a7,false)
};function m(a8,a7,bd,bc){bd=Number(bd)||0;var ba=a8.length-bd;if(!bc){bc=ba}else{bc=Number(bc);
if(bc>ba){bc=ba}}var bb=a7.length;if(bb%2!==0){throw new TypeError("Invalid hex string")
}if(bc>bb/2){bc=bb/2}for(var a9=0;a9<bc;++a9){var a6=parseInt(a7.substr(a9*2,2),16);
if(Z(a6)){return a9}a8[bd+a9]=a6}return a9}function V(a7,a6,a9,a8){return S(aT(a6,a7.length-a9),a7,a9,a8)
}function a3(a7,a6,a9,a8){return S(ag(a6),a7,a9,a8)}function y(a7,a6,a9,a8){return a3(a7,a6,a9,a8)
}function P(a7,a6,a9,a8){return S(af(a6),a7,a9,a8)}function q(a7,a6,a9,a8){return S(av(a6,a7.length-a9),a7,a9,a8)
}aD.prototype.write=function aW(a6,ba,a9,a8){if(ba===undefined){a8="utf8";a9=this.length;
ba=0}else{if(a9===undefined&&typeof ba==="string"){a8=ba;a9=this.length;ba=0}else{if(isFinite(ba)){ba=ba>>>0;
if(isFinite(a9)){a9=a9>>>0;if(a8===undefined){a8="utf8"}}else{a8=a9;a9=undefined
}}else{throw new Error("Buffer.write(string, encoding, offset[, length]) is no longer supported")
}}}var a7=this.length-ba;if(a9===undefined||a9>a7){a9=a7}if((a6.length>0&&(a9<0||ba<0))||ba>this.length){throw new RangeError("Attempt to write outside buffer bounds")
}if(!a8){a8="utf8"}var bb=false;for(;;){switch(a8){case"hex":return m(this,a6,ba,a9);
case"utf8":case"utf-8":return V(this,a6,ba,a9);case"ascii":return a3(this,a6,ba,a9);
case"latin1":case"binary":return y(this,a6,ba,a9);case"base64":return P(this,a6,ba,a9);
case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return q(this,a6,ba,a9);default:if(bb){throw new TypeError("Unknown encoding: "+a8)
}a8=(""+a8).toLowerCase();bb=true}}};aD.prototype.toJSON=function x(){return{type:"Buffer",data:Array.prototype.slice.call(this._arr||this,0)}
};function aH(a7,a8,a6){if(a8===0&&a6===a7.length){return aF.fromByteArray(a7)}else{return aF.fromByteArray(a7.slice(a8,a6))
}}function aP(a8,a7,ba){ba=Math.min(a8.length,ba);var bd=[];var bb=a7;while(bb<ba){var bf=a8[bb];
var be=null;var bh=(bf>239)?4:(bf>223)?3:(bf>191)?2:1;if(bb+bh<=ba){var bg,a6,bc,a9;
switch(bh){case 1:if(bf<128){be=bf}break;case 2:bg=a8[bb+1];if((bg&192)===128){a9=(bf&31)<<6|(bg&63);
if(a9>127){be=a9}}break;case 3:bg=a8[bb+1];a6=a8[bb+2];if((bg&192)===128&&(a6&192)===128){a9=(bf&15)<<12|(bg&63)<<6|(a6&63);
if(a9>2047&&(a9<55296||a9>57343)){be=a9}}break;case 4:bg=a8[bb+1];a6=a8[bb+2];bc=a8[bb+3];
if((bg&192)===128&&(a6&192)===128&&(bc&192)===128){a9=(bf&15)<<18|(bg&63)<<12|(a6&63)<<6|(bc&63);
if(a9>65535&&a9<1114112){be=a9}}}}if(be===null){be=65533;bh=1}else{if(be>65535){be-=65536;
bd.push(be>>>10&1023|55296);be=56320|be&1023}}bd.push(be);bb+=bh}return ad(bd)}var Q=4096;
function ad(a7){var a6=a7.length;if(a6<=Q){return String.fromCharCode.apply(String,a7)
}var a9="";var a8=0;while(a8<a6){a9+=String.fromCharCode.apply(String,a7.slice(a8,a8+=Q))
}return a9}function F(a8,ba,a6){var a7="";a6=Math.min(a8.length,a6);for(var a9=ba;
a9<a6;++a9){a7+=String.fromCharCode(a8[a9]&127)}return a7}function al(a8,ba,a6){var a7="";
a6=Math.min(a8.length,a6);for(var a9=ba;a9<a6;++a9){a7+=String.fromCharCode(a8[a9])
}return a7}function ab(a9,bb,a7){var a6=a9.length;if(!bb||bb<0){bb=0}if(!a7||a7<0||a7>a6){a7=a6
}var a8="";for(var ba=bb;ba<a7;++ba){a8+=az(a9[ba])}return a8}function ak(a8,bb,a7){var a6=a8.slice(bb,a7);
var ba="";for(var a9=0;a9<a6.length;a9+=2){ba+=String.fromCharCode(a6[a9]+(a6[a9+1]*256))
}return ba}aD.prototype.slice=function u(a9,a7){var a6=this.length;a9=~~a9;a7=a7===undefined?a6:~~a7;
if(a9<0){a9+=a6;if(a9<0){a9=0}}else{if(a9>a6){a9=a6}}if(a7<0){a7+=a6;if(a7<0){a7=0
}}else{if(a7>a6){a7=a6}}if(a7<a9){a7=a9}var a8=this.subarray(a9,a7);a8.__proto__=aD.prototype;
return a8};function au(a8,a6,a7){if((a8%1)!==0||a8<0){throw new RangeError("offset is not uint")
}if(a8+a6>a7){throw new RangeError("Trying to access beyond buffer length")}}aD.prototype.readUIntLE=function f(bb,a6,a9){bb=bb>>>0;
a6=a6>>>0;if(!a9){au(bb,a6,this.length)}var ba=this[bb];var a8=1;var a7=0;while(++a7<a6&&(a8*=256)){ba+=this[bb+a7]*a8
}return ba};aD.prototype.readUIntBE=function aA(ba,a6,a8){ba=ba>>>0;a6=a6>>>0;if(!a8){au(ba,a6,this.length)
}var a9=this[ba+ --a6];var a7=1;while(a6>0&&(a7*=256)){a9+=this[ba+ --a6]*a7}return a9
};aD.prototype.readUInt8=function i(a7,a6){a7=a7>>>0;if(!a6){au(a7,1,this.length)
}return this[a7]};aD.prototype.readUInt16LE=function l(a7,a6){a7=a7>>>0;if(!a6){au(a7,2,this.length)
}return this[a7]|(this[a7+1]<<8)};aD.prototype.readUInt16BE=function aK(a7,a6){a7=a7>>>0;
if(!a6){au(a7,2,this.length)}return(this[a7]<<8)|this[a7+1]};aD.prototype.readUInt32LE=function K(a7,a6){a7=a7>>>0;
if(!a6){au(a7,4,this.length)}return((this[a7])|(this[a7+1]<<8)|(this[a7+2]<<16))+(this[a7+3]*16777216)
};aD.prototype.readUInt32BE=function a4(a7,a6){a7=a7>>>0;if(!a6){au(a7,4,this.length)
}return(this[a7]*16777216)+((this[a7+1]<<16)|(this[a7+2]<<8)|this[a7+3])};aD.prototype.readIntLE=function an(bb,a6,a9){bb=bb>>>0;
a6=a6>>>0;if(!a9){au(bb,a6,this.length)}var ba=this[bb];var a8=1;var a7=0;while(++a7<a6&&(a8*=256)){ba+=this[bb+a7]*a8
}a8*=128;if(ba>=a8){ba-=Math.pow(2,8*a6)}return ba};aD.prototype.readIntBE=function v(bb,a6,a9){bb=bb>>>0;
a6=a6>>>0;if(!a9){au(bb,a6,this.length)}var a7=a6;var a8=1;var ba=this[bb+ --a7];
while(a7>0&&(a8*=256)){ba+=this[bb+ --a7]*a8}a8*=128;if(ba>=a8){ba-=Math.pow(2,8*a6)
}return ba};aD.prototype.readInt8=function aN(a7,a6){a7=a7>>>0;if(!a6){au(a7,1,this.length)
}if(!(this[a7]&128)){return(this[a7])}return((255-this[a7]+1)*-1)};aD.prototype.readInt16LE=function ax(a8,a6){a8=a8>>>0;
if(!a6){au(a8,2,this.length)}var a7=this[a8]|(this[a8+1]<<8);return(a7&32768)?a7|4294901760:a7
};aD.prototype.readInt16BE=function H(a8,a6){a8=a8>>>0;if(!a6){au(a8,2,this.length)
}var a7=this[a8+1]|(this[a8]<<8);return(a7&32768)?a7|4294901760:a7};aD.prototype.readInt32LE=function aV(a7,a6){a7=a7>>>0;
if(!a6){au(a7,4,this.length)}return(this[a7])|(this[a7+1]<<8)|(this[a7+2]<<16)|(this[a7+3]<<24)
};aD.prototype.readInt32BE=function aa(a7,a6){a7=a7>>>0;if(!a6){au(a7,4,this.length)
}return(this[a7]<<24)|(this[a7+1]<<16)|(this[a7+2]<<8)|(this[a7+3])};aD.prototype.readFloatLE=function h(a7,a6){a7=a7>>>0;
if(!a6){au(a7,4,this.length)}return b.read(this,a7,true,23,4)};aD.prototype.readFloatBE=function aE(a7,a6){a7=a7>>>0;
if(!a6){au(a7,4,this.length)}return b.read(this,a7,false,23,4)};aD.prototype.readDoubleLE=function a(a7,a6){a7=a7>>>0;
if(!a6){au(a7,8,this.length)}return b.read(this,a7,true,52,8)};aD.prototype.readDoubleBE=function ao(a7,a6){a7=a7>>>0;
if(!a6){au(a7,8,this.length)}return b.read(this,a7,false,52,8)};function aM(a7,ba,bb,a9,a6,a8){if(!aD.isBuffer(a7)){throw new TypeError('"buffer" argument must be a Buffer instance')
}if(ba>a6||ba<a8){throw new RangeError('"value" argument is out of bounds')}if(bb+a9>a7.length){throw new RangeError("Index out of range")
}}aD.prototype.writeUIntLE=function aq(a9,bc,a7,bb){a9=+a9;bc=bc>>>0;a7=a7>>>0;
if(!bb){var a6=Math.pow(2,8*a7)-1;aM(this,a9,bc,a7,a6,0)}var ba=1;var a8=0;this[bc]=a9&255;
while(++a8<a7&&(ba*=256)){this[bc+a8]=(a9/ba)&255}return bc+a7};aD.prototype.writeUIntBE=function B(a9,bc,a7,bb){a9=+a9;
bc=bc>>>0;a7=a7>>>0;if(!bb){var a6=Math.pow(2,8*a7)-1;aM(this,a9,bc,a7,a6,0)}var a8=a7-1;
var ba=1;this[bc+a8]=a9&255;while(--a8>=0&&(ba*=256)){this[bc+a8]=(a9/ba)&255}return bc+a7
};aD.prototype.writeUInt8=function aB(a6,a8,a7){a6=+a6;a8=a8>>>0;if(!a7){aM(this,a6,a8,1,255,0)
}this[a8]=(a6&255);return a8+1};aD.prototype.writeUInt16LE=function W(a6,a8,a7){a6=+a6;
a8=a8>>>0;if(!a7){aM(this,a6,a8,2,65535,0)}this[a8]=(a6&255);this[a8+1]=(a6>>>8);
return a8+2};aD.prototype.writeUInt16BE=function d(a6,a8,a7){a6=+a6;a8=a8>>>0;if(!a7){aM(this,a6,a8,2,65535,0)
}this[a8]=(a6>>>8);this[a8+1]=(a6&255);return a8+2};aD.prototype.writeUInt32LE=function ap(a6,a8,a7){a6=+a6;
a8=a8>>>0;if(!a7){aM(this,a6,a8,4,4294967295,0)}this[a8+3]=(a6>>>24);this[a8+2]=(a6>>>16);
this[a8+1]=(a6>>>8);this[a8]=(a6&255);return a8+4};aD.prototype.writeUInt32BE=function z(a6,a8,a7){a6=+a6;
a8=a8>>>0;if(!a7){aM(this,a6,a8,4,4294967295,0)}this[a8]=(a6>>>24);this[a8+1]=(a6>>>16);
this[a8+2]=(a6>>>8);this[a8+3]=(a6&255);return a8+4};aD.prototype.writeIntLE=function p(ba,bd,a7,bc){ba=+ba;
bd=bd>>>0;if(!bc){var a6=Math.pow(2,(8*a7)-1);aM(this,ba,bd,a7,a6-1,-a6)}var a8=0;
var bb=1;var a9=0;this[bd]=ba&255;while(++a8<a7&&(bb*=256)){if(ba<0&&a9===0&&this[bd+a8-1]!==0){a9=1
}this[bd+a8]=((ba/bb)>>0)-a9&255}return bd+a7};aD.prototype.writeIntBE=function aS(ba,bd,a7,bc){ba=+ba;
bd=bd>>>0;if(!bc){var a6=Math.pow(2,(8*a7)-1);aM(this,ba,bd,a7,a6-1,-a6)}var a8=a7-1;
var bb=1;var a9=0;this[bd+a8]=ba&255;while(--a8>=0&&(bb*=256)){if(ba<0&&a9===0&&this[bd+a8+1]!==0){a9=1
}this[bd+a8]=((ba/bb)>>0)-a9&255}return bd+a7};aD.prototype.writeInt8=function ah(a6,a8,a7){a6=+a6;
a8=a8>>>0;if(!a7){aM(this,a6,a8,1,127,-128)}if(a6<0){a6=255+a6+1}this[a8]=(a6&255);
return a8+1};aD.prototype.writeInt16LE=function aj(a6,a8,a7){a6=+a6;a8=a8>>>0;if(!a7){aM(this,a6,a8,2,32767,-32768)
}this[a8]=(a6&255);this[a8+1]=(a6>>>8);return a8+2};aD.prototype.writeInt16BE=function t(a6,a8,a7){a6=+a6;
a8=a8>>>0;if(!a7){aM(this,a6,a8,2,32767,-32768)}this[a8]=(a6>>>8);this[a8+1]=(a6&255);
return a8+2};aD.prototype.writeInt32LE=function aG(a6,a8,a7){a6=+a6;a8=a8>>>0;if(!a7){aM(this,a6,a8,4,2147483647,-2147483648)
}this[a8]=(a6&255);this[a8+1]=(a6>>>8);this[a8+2]=(a6>>>16);this[a8+3]=(a6>>>24);
return a8+4};aD.prototype.writeInt32BE=function O(a6,a8,a7){a6=+a6;a8=a8>>>0;if(!a7){aM(this,a6,a8,4,2147483647,-2147483648)
}if(a6<0){a6=4294967295+a6+1}this[a8]=(a6>>>24);this[a8+1]=(a6>>>16);this[a8+2]=(a6>>>8);
this[a8+3]=(a6&255);return a8+4};function N(a7,ba,bb,a9,a6,a8){if(bb+a9>a7.length){throw new RangeError("Index out of range")
}if(bb<0){throw new RangeError("Index out of range")}}function s(a6,a7,ba,a9,a8){a7=+a7;
ba=ba>>>0;if(!a8){N(a6,a7,ba,4,3.4028234663852886e+38,-3.4028234663852886e+38)}b.write(a6,a7,ba,a9,23,4);
return ba+4}aD.prototype.writeFloatLE=function j(a6,a8,a7){return s(this,a6,a8,true,a7)
};aD.prototype.writeFloatBE=function aI(a6,a8,a7){return s(this,a6,a8,false,a7)
};function o(a6,a7,ba,a9,a8){a7=+a7;ba=ba>>>0;if(!a8){N(a6,a7,ba,8,1.7976931348623157e+308,-1.7976931348623157e+308)
}b.write(a6,a7,ba,a9,52,8);return ba+8}aD.prototype.writeDoubleLE=function D(a6,a8,a7){return o(this,a6,a8,true,a7)
};aD.prototype.writeDoubleBE=function aZ(a6,a8,a7){return o(this,a6,a8,false,a7)
};aD.prototype.copy=function A(a9,ba,bb,a7){if(!bb){bb=0}if(!a7&&a7!==0){a7=this.length
}if(ba>=a9.length){ba=a9.length}if(!ba){ba=0}if(a7>0&&a7<bb){a7=bb}if(a7===bb){return 0
}if(a9.length===0||this.length===0){return 0}if(ba<0){throw new RangeError("targetStart out of bounds")
}if(bb<0||bb>=this.length){throw new RangeError("sourceStart out of bounds")}if(a7<0){throw new RangeError("sourceEnd out of bounds")
}if(a7>this.length){a7=this.length}if(a9.length-ba<a7-bb){a7=a9.length-ba+bb}var a6=a7-bb;
var a8;if(this===a9&&bb<ba&&ba<a7){for(a8=a6-1;a8>=0;--a8){a9[a8+ba]=this[a8+bb]
}}else{if(a6<1000){for(a8=0;a8<a6;++a8){a9[a8+ba]=this[a8+bb]}}else{Uint8Array.prototype.set.call(a9,this.subarray(bb,bb+a6),ba)
}}return a6};aD.prototype.fill=function w(bc,bd,a8,bb){if(typeof bc==="string"){if(typeof bd==="string"){bb=bd;
bd=0;a8=this.length}else{if(typeof a8==="string"){bb=a8;a8=this.length}}if(bc.length===1){var ba=bc.charCodeAt(0);
if(ba<256){bc=ba}}if(bb!==undefined&&typeof bb!=="string"){throw new TypeError("encoding must be a string")
}if(typeof bb==="string"&&!aD.isEncoding(bb)){throw new TypeError("Unknown encoding: "+bb)
}}else{if(typeof bc==="number"){bc=bc&255}}if(bd<0||this.length<bd||this.length<a8){throw new RangeError("Out of range index")
}if(a8<=bd){return this}bd=bd>>>0;a8=a8===undefined?this.length:a8>>>0;if(!bc){bc=0
}var a9;if(typeof bc==="number"){for(a9=bd;a9<a8;++a9){this[a9]=bc}}else{var a7=aD.isBuffer(bc)?bc:new aD(bc,bb);
var a6=a7.length;for(a9=0;a9<a8-bd;++a9){this[a9+bd]=a7[a9%a6]}}return this};var aC=/[^+/0-9A-Za-z-_]/g;
function k(a6){a6=a6.trim().replace(aC,"");if(a6.length<2){return""}while(a6.length%4!==0){a6=a6+"="
}return a6}function az(a6){if(a6<16){return"0"+a6.toString(16)}return a6.toString(16)
}function aT(a9,a7){a7=a7||Infinity;var a8;var bc=a9.length;var bb=null;var a6=[];
for(var ba=0;ba<bc;++ba){a8=a9.charCodeAt(ba);if(a8>55295&&a8<57344){if(!bb){if(a8>56319){if((a7-=3)>-1){a6.push(239,191,189)
}continue}else{if(ba+1===bc){if((a7-=3)>-1){a6.push(239,191,189)}continue}}bb=a8;
continue}if(a8<56320){if((a7-=3)>-1){a6.push(239,191,189)}bb=a8;continue}a8=(bb-55296<<10|a8-56320)+65536
}else{if(bb){if((a7-=3)>-1){a6.push(239,191,189)}}}bb=null;if(a8<128){if((a7-=1)<0){break
}a6.push(a8)}else{if(a8<2048){if((a7-=2)<0){break}a6.push(a8>>6|192,a8&63|128)}else{if(a8<65536){if((a7-=3)<0){break
}a6.push(a8>>12|224,a8>>6&63|128,a8&63|128)}else{if(a8<1114112){if((a7-=4)<0){break
}a6.push(a8>>18|240,a8>>12&63|128,a8>>6&63|128,a8&63|128)}else{throw new Error("Invalid code point")
}}}}}return a6}function ag(a8){var a6=[];for(var a7=0;a7<a8.length;++a7){a6.push(a8.charCodeAt(a7)&255)
}return a6}function av(bb,a7){var bc,a8,ba;var a6=[];for(var a9=0;a9<bb.length;
++a9){if((a7-=2)<0){break}bc=bb.charCodeAt(a9);a8=bc>>8;ba=bc%256;a6.push(ba);a6.push(a8)
}return a6}function af(a6){return aF.toByteArray(k(a6))}function S(a9,ba,a8,a7){for(var a6=0;
a6<a7;++a6){if((a6+a8>=ba.length)||(a6>=a9.length)){break}ba[a6+a8]=a9[a6]}return a6
}function ay(a6){return a6 instanceof ArrayBuffer||(a6!=null&&a6.constructor!=null&&a6.constructor.name==="ArrayBuffer"&&typeof a6.byteLength==="number")
}function aY(a6){return(typeof ArrayBuffer.isView==="function")&&ArrayBuffer.isView(a6)
}function Z(a6){return a6!==a6}},{"base64-js":328,ieee754:329}],328:[function(g,c,k){k.byteLength=q;
k.toByteArray=h;k.fromByteArray=a;var f=[];var n=[];var o=typeof Uint8Array!=="undefined"?Uint8Array:Array;
var b="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/";for(var m=0,p=b.length;
m<p;++m){f[m]=b[m];n[b.charCodeAt(m)]=m}n["-".charCodeAt(0)]=62;n["_".charCodeAt(0)]=63;
function d(r){var i=r.length;if(i%4>0){throw new Error("Invalid string. Length must be a multiple of 4")
}return r[i-2]==="="?2:r[i-1]==="="?1:0}function q(i){return(i.length*3/4)-d(i)
}function h(x){var w,u,v,y,t;var s=x.length;y=d(x);t=new o((s*3/4)-y);u=y>0?s-4:s;
var r=0;for(w=0;w<u;w+=4){v=(n[x.charCodeAt(w)]<<18)|(n[x.charCodeAt(w+1)]<<12)|(n[x.charCodeAt(w+2)]<<6)|n[x.charCodeAt(w+3)];
t[r++]=(v>>16)&255;t[r++]=(v>>8)&255;t[r++]=v&255}if(y===2){v=(n[x.charCodeAt(w)]<<2)|(n[x.charCodeAt(w+1)]>>4);
t[r++]=v&255}else{if(y===1){v=(n[x.charCodeAt(w)]<<10)|(n[x.charCodeAt(w+1)]<<4)|(n[x.charCodeAt(w+2)]>>2);
t[r++]=(v>>8)&255;t[r++]=v&255}}return t}function l(i){return f[i>>18&63]+f[i>>12&63]+f[i>>6&63]+f[i&63]
}function j(s,w,r){var v;var t=[];for(var u=w;u<r;u+=3){v=(s[u]<<16)+(s[u+1]<<8)+(s[u+2]);
t.push(l(v))}return t.join("")}function a(x){var v;var y=x.length;var z=y%3;var s="";
var u=[];var r=16383;for(var w=0,t=y-z;w<t;w+=r){u.push(j(x,w,(w+r)>t?t:(w+r)))
}if(z===1){v=x[y-1];s+=f[v>>2];s+=f[(v<<4)&63];s+="=="}else{if(z===2){v=(x[y-2]<<8)+(x[y-1]);
s+=f[v>>10];s+=f[(v>>4)&63];s+=f[(v<<2)&63];s+="="}}u.push(s);return u.join("")
}},{}],329:[function(b,c,a){a.read=function(n,l,h,g,q){var r,k;var j=q*8-g-1;var p=(1<<j)-1;
var f=p>>1;var u=-7;var o=h?(q-1):0;var t=h?-1:1;var v=n[l+o];o+=t;r=v&((1<<(-u))-1);
v>>=(-u);u+=j;for(;u>0;r=r*256+n[l+o],o+=t,u-=8){}k=r&((1<<(-u))-1);r>>=(-u);u+=g;
for(;u>0;k=k*256+n[l+o],o+=t,u-=8){}if(r===0){r=1-f}else{if(r===p){return k?NaN:((v?-1:1)*Infinity)
}else{k=k+Math.pow(2,g);r=r-f}}return(v?-1:1)*k*Math.pow(2,r-g)};a.write=function(o,w,n,h,g,r){var t,k,v;
var j=r*8-g-1;var q=(1<<j)-1;var f=q>>1;var l=(g===23?Math.pow(2,-24)-Math.pow(2,-77):0);
var p=h?0:(r-1);var u=h?1:-1;var x=w<0||(w===0&&1/w<0)?1:0;w=Math.abs(w);if(isNaN(w)||w===Infinity){k=isNaN(w)?1:0;
t=q}else{t=Math.floor(Math.log(w)/Math.LN2);if(w*(v=Math.pow(2,-t))<1){t--;v*=2
}if(t+f>=1){w+=l/v}else{w+=l*Math.pow(2,1-f)}if(w*v>=2){t++;v/=2}if(t+f>=q){k=0;
t=q}else{if(t+f>=1){k=(w*v-1)*Math.pow(2,g);t=t+f}else{k=w*Math.pow(2,f-1)*Math.pow(2,g);
t=0}}}for(;g>=8;o[n+p]=k&255,p+=u,k/=256,g-=8){}t=(t<<g)|k;j+=g;for(;j>0;o[n+p]=t&255,p+=u,t/=256,j-=8){}o[n+p-u]|=x*128
}},{}],330:[function(f,d,g){f("@marcom/ac-polyfills/Object/assign");var h="data-films-modal-link";
var j="data-films-inline-target";var c=f("./factory/createFilms");var a=true;var i;
function b(l,u){if(!(this instanceof b)&&a){a=false;i=setTimeout(b,1);return function(w,v){clearTimeout(i);
return new b(w,v)}}l=l||document;var r=Array.prototype.slice.call(l.querySelectorAll("["+h+"]"));
var k=Array.prototype.slice.call(l.querySelectorAll("["+j+"]"));var n;if(r.length){n=c(r,Object.assign(u||{},{modal:true}))
}else{if(k.length){var o={};var m=0;var p=k.length;for(;m<p;m++){var t=k[m];var q=t.getAttribute(j);
if(!o[q]){o[q]=[]}o[q].push(t)}for(var s in o){if(o.hasOwnProperty(s)){n=c(o[s],Object.assign(u||{},{targetElement:l.querySelector("#"+s)}))
}}}}return n}d.exports=b()},{"./factory/createFilms":335,"@marcom/ac-polyfills/Object/assign":107}],331:[function(b,a,c){var h;
try{h=b("@marcom/ac-analytics")}catch(j){}var f=b("@marcom/ac-useragent").browser;
var g=f.ie||f.edge;var l=b("@marcom/ac-video/event-emitter-shim/EventEmitterShim");
var i=function(n,p,o){if(o){var m=function(){p.apply(o,arguments)};l.prototype.once.apply(this,[n,m])
}else{l.prototype.once.apply(this,arguments)}};function k(n,m,o){this.player=n;
this.sources={};this.currentStubPlayer=null;this.playerType="";this.videoType="";
this.options=m;if(o){this._bindAnchors(o)}}var d=k.prototype;d._bindAnchors=function(o){var n=0;
var m=o.length;for(;n<m;n++){this._bindAnchorForAnalytics(o[n])}};d.activate=function(){this._onPlay=this._onPlay.bind(this);
this._onEnded=this._onEnded.bind(this);this._onTimeupdate=this._onTimeupdate.bind(this);
this._onTexttrackshow=this._onTexttrackshow.bind(this);this._onLoadStart=this._onLoadStart.bind(this);
this.setCurrentStubPlayer=this.setCurrentStubPlayer.bind(this);if(g){this.player.on("playing",this._onPlay)
}else{this.player.on("play",this._onPlay)}this.player.on("ended",this._onEnded);
this.player.on("loadstart",this._onLoadStart);this.player.on("timeupdate",this._onTimeupdate);
this.player.on("texttrackshow",this._onTexttrackshow);this.player.on("durationchange",this.setCurrentStubPlayer)
};d.deactivate=function(){if(g){this.player.off("playing",this._onPlay)}else{this.player.off("play",this._onPlay)
}this.player.off("ended",this._onEnded);this.player.off("timeupdate",this._onTimeupdate);
this.player.off("texttrackshow",this._onTexttrackshow);this.player.off("durationchange",this.setCurrentStubPlayer)
};d._bindAnchorForAnalytics=function(m){var o;var n;if(m){if(this.sources[m.id]){return
}o=this._createStubPlayer(m);n=m.getAttribute("data-"+this.options.dataAttribute);
if(!n){o.videoId=m.id}this.sources[m.id]={stubPlayer:o,observer:this._createObserver(o)}
}};d.addSourceObject=d._bindAnchorForAnalytics;d.setCurrentStubPlayer=function(){var n;
var p=this.player.el;var o=p.getAttribute("data-"+this.options.dataAttribute);var m=this._getCurrentSourceObject(o);
if(m&&m.stubPlayer){this.currentStubPlayer=m.stubPlayer;this.playerType="html5";
n=this.player.getCurrentSrc();if(n&&n.attributes&&n.attributes.src){this.videoType=n.attributes.src.value.split(".").pop()
}}};d.destroy=function(){this.deactivate();this.player=null;this.sources=null;this.currentStubPlayer=null;
this.options=null};d._onPlay=function(){this.setCurrentStubPlayer();if(!this._started){this._proxyEvent("play");
this._started=true}};d._onLoadStart=function(){this._started=false};d._onEnded=function(){this._started=false;
this._proxyEvent("ended")};d._onTimeupdate=function(){this._proxyEvent("timeupdate");
if(this._started&&this.player.getCurrentTime()===0&&this.player.getPaused()){this._started=false
}};d._onTexttrackshow=function(){this._proxyEvent("captions-enabled")};d._getSourceObjectBySrcObjId=function(m){return this.sources[m]||null
};d._getCurrentSourceObject=function(m){var n;if(m){n=this._getSourceObjectBySrcObjId(m)
}return n};d._createStubPlayer=function(m){var n=new l();n.once=i;n.el=m;return n
};d._getEventData=function(){return{currentTime:this.player.getCurrentTime(),playerType:(this.playerType||"html5"),videoType:(this.videoType||null)}
};d._createObserver=function(n){var m;if(h&&h.observer&&h.observer.Video){m=new h.observer.Video(n,{dataAttribute:this.options.dataAttribute})
}return m};d._proxyEvent=function(m){if(this.currentStubPlayer){this.currentStubPlayer.trigger(m,this._getEventData())
}};a.exports=k},{"@marcom/ac-analytics":"@marcom/ac-analytics","@marcom/ac-useragent":171,"@marcom/ac-video/event-emitter-shim/EventEmitterShim":270}],332:[function(c,d,b){var f=c("../windowload/windowLoad");
var h=c("../touchclick/TouchClick");var g=c("@marcom/ac-useragent");var a=(g.os.ios||g.os.android);
d.exports=function i(m,n,k,l){var j=h.create(m);j.on("click",function(){n(m)});
if(l&&m.id){l.createRoute(m.id,function(){f(function(){n(m,!a)})})}}},{"../touchclick/TouchClick":342,"../windowload/windowLoad":343,"@marcom/ac-useragent":171}],333:[function(l,h,n){var i=l("@marcom/ac-router").Router;
var j=l("@marcom/ac-video/player/factory/createShareablePlayer");var b=l("@marcom/ac-video/optimizeVideoUrl");
var r=l("@marcom/ac-useragent");var p=l("./bindAnchor");var c=l("./createClickHandler");
var m=l("./createModalLink");var g=l("./createHandheldModalLink");var o=l("./createInlineLink");
var a="data-films-options";var f=l("@marcom/ac-feature/isHandheld")();var k=r.os.ios;
var d={controls:true,urlOptimizer:b};h.exports=function q(y,w){w=w||{};w=Object.assign({},d,w);
var u;y.forEach(function(A){if(A.hasAttribute(a)){var B=JSON.parse(A.getAttribute(a));
if(B.closeOnEnd===false&&!w.closeOnEnd){w.closeOnEnd=false}}});if(!w.maxWidth){w.maxWidth=1280
}var x=j(w);var v;u=new i({hashChange:true,pushState:false});if(w.modal&&(!f||!k)){v=m(x,w)
}else{if(w.modal){v=g(x,document.body,w)}else{v=o(x,w)}}var t=v.play.bind(v);var s=function(C){var B=0;
var A=y.length;for(;B<A;B++){if(y[B].id===C||y[B]===C){t(y[B].href)}}};var z=c({player:x,playHandler:t,attr:"data-"+w.dataAttribute});
y.forEach(function(A){p(A,z,t,u)});u.start();return{play:s,player:x,modalVideo:v.modal}
}},{"./bindAnchor":332,"./createClickHandler":334,"./createHandheldModalLink":336,"./createInlineLink":337,"./createModalLink":338,"@marcom/ac-feature/isHandheld":37,"@marcom/ac-router":168,"@marcom/ac-useragent":171,"@marcom/ac-video/optimizeVideoUrl":271,"@marcom/ac-video/player/factory/createShareablePlayer":276}],334:[function(d,f,c){var a="data-films-options";
var g="data-films-modal-label";var h="Video Player";f.exports=function b(i){return function(n,m){var j=n.getAttribute(a);
var l;if(j){l=JSON.parse(j)}else{l=null}var k=n.getAttribute(g)||(l&&l.modalLabel)||i.player.options.modalLabel||h;
i.player.el.setAttribute(i.attr,n.getAttribute(i.attr)||n.id);i.playHandler(n.href,l,m,k)
}}},{}],335:[function(c,d,b){var g=c("./bindAnchors");var f=c("../analytics/AnalyticsTranslator");
var h={dataAttribute:"analytics-video-id",analytics:true};d.exports=function a(k,j){j=j||{};
j=Object.assign({},h,j);var l=g(k,j);if(j.analytics){var i=new f(l.player,j,k);
i.activate()}return l}},{"../analytics/AnalyticsTranslator":331,"./bindAnchors":333}],336:[function(c,d,a){var b="ac-films-handheld-player";
var g="player-fullscreen";d.exports=function f(k,j,i){k.el.classList.add(b);var h=function(l,n){var m=function(){if(!k.getPaused()){k.pause()
}k.el.classList.remove(g)};k.el.classList.add(g);k.once("ended",m);k.once("exitfullscreen",m);
k.load(l);if(n!==false){k.play()}};j.appendChild(k.el);return{play:h,player:k}}
},{}],337:[function(b,c,a){c.exports=function d(i,h){var g=h.targetElement;var f=function(j,k){i.load(j,null,0,k);
i.play()};h.playHandler=f;if(g){g.appendChild(i.el)}return{play:f,player:i}}},{}],338:[function(d,b,g){var a=d("@marcom/ac-modal").createFullViewportModal;
var j=d("@marcom/ac-useragent");var c=j.os.ios||j.os.android;var h="ac-films-modal-mobile";
var k=d("./link/ModalLink");var i="ac-modal-video";b.exports=function f(n,m){m=m||{};
var l=document.createElement("div");l.classList.add("ac-player-container");if(c){l.classList.add(h)
}l.appendChild(n.el);var p=a(l);p.modalElement.classList.add(i);var o=new k({player:n,modal:p,closeOnEnd:m.closeOnEnd});
return o}},{"./link/ModalLink":339,"@marcom/ac-modal":96,"@marcom/ac-useragent":171}],339:[function(f,c,h){var k="-tft-";
var a=/_([0-9]+)x([0-9]+)/;var d="ac-video-cinematic-aspect-ratio";var o="ac-video-square-aspect-ratio";
var g="ac-video-vertical-aspect-ratio";var j="ac-modal-video-pip";var l="pictureinpicture:change";
var b="has-modal";var n=f("../../resize/ResizeHandler");var m=function(p){this.modal=p.modal;
this.player=p.player;this._resizeHandler=new n({player:this.player,modal:this.modal});
this._closeOnEnd=(p.closeOnEnd!==undefined)?p.closeOnEnd:true;this._ended=false;
this._pauseTime=0;this._playing=false;this._initialize()};var i=m.prototype;i._initialize=function(){this._bindMethods();
this.player.on("ended",this._onEnded);this.player.on("pause",this._onPaused);this.modal.on("open",this._onOpen);
if(this.player.supportsPictureInPicture()){this.player.on(l,this._onPipModeChanged)
}};i._bindMethods=function(){this._onEnded=this._onEnded.bind(this);this._onPipModeChanged=this._onPipModeChanged.bind(this);
this._onPaused=this._onPaused.bind(this);this._onModalWillClose=this._onModalWillClose.bind(this);
this._onOpen=this._onOpen.bind(this)};i._onOpen=function(){this.player.refreshSize()
};i._onPaused=function(){this._pauseTime=Date.now()};i._onEnded=function(){this._ended=true;
if(!this.player.isPictureInPicture()&&this._closeOnEnd){this.modal.close()}else{if(this.player.isPictureInPicture()){this.player.setPictureInPicture(false);
this.modal.modalElement.classList.remove(j);if(!this._closeOnEnd){this.modal.open();
this._bindWillClose()}}}};i._onPipModeChanged=function(){if(this._ended){return
}if(this.player.isPictureInPicture()&&this._isModalOpen()){this._unBindWillClose();
this.modal.modalElement.classList.add(j);this.modal.close()}else{if(!this._isModalOpen()){this.modal.modalElement.classList.remove(j);
if(!this._pauseTime||(Date.now()-this._pauseTime)>400){this._bindWillClose();this.modal.open()
}else{this._resetVideo()}}}};i._resetVideo=function(){this.player.pause();this.player.setCurrentTime(0)
};i._onModalWillClose=function(){this._unBindWillClose();this._resetVideo();this.player.setPictureInPicture(false);
this.modal.modalElement.classList.remove(j)};i._setCinematicMode=function(p){if(p){this.player.el.parentElement.classList.add(d)
}else{this.player.el.parentElement.classList.remove(d)}};i._setSquareVideo=function(p){if(p){this.player.el.parentElement.classList.add(o)
}else{this.player.el.parentElement.classList.remove(o)}};i._setVerticalVideo=function(p){if(p){this.player.el.parentElement.classList.add(g)
}else{this.player.el.parentElement.classList.remove(g)}};i._resetPiPVideo=function(){var p=this.player.getVisibleTextTracks();
p.forEach(function(q){q.mode="hidden"});this._resetVideo();p.forEach(function(q){q.mode="showing"
})};i.play=function(r,s,u,q){this._ended=false;this._setCinematicMode(r.match(k));
if(a.test(r)){var t=parseInt(RegExp.$1,10);var p=parseInt(RegExp.$2,10);if(p>t){this._setVerticalVideo(true)
}else{this._setVerticalVideo(false)}if(p===t){this._setSquareVideo(true)}else{this._setSquareVideo(false)
}}else{this._setVerticalVideo(false);this._setSquareVideo(false)}this.modal.modalElement.setAttribute("aria-label",q);
if(!this.player.isPictureInPicture()){this.modal.open();this._bindWillClose()}else{this._resetPiPVideo()
}this.player.load(r,null,0,Object.assign({},s,{maxWidth:window.innerWidth}));if(u!==false){this.player.play()
}};i._bindWillClose=function(){this.modal.on("willclose",this._onModalWillClose)
};i._unBindWillClose=function(){this.modal.off("willclose",this._onModalWillClose)
};i._isModalOpen=function(){return document.documentElement.classList.contains(b)
};i.destroy=function(){this.player.off("ended",this._onEnded);this.player.off("paused",this._onPaused);
this.player.off(l,this._onPipModeChanged);this._unBindWillClose();this._resizeHandler.destroy();
this.modal.destroy();this.player.destroy()};c.exports=m},{"../../resize/ResizeHandler":341}],340:[function(b,c,a){b("../AutoFilms")()
},{"../AutoFilms":330}],341:[function(c,d,b){var i=/_([0-9]+)x([0-9]+)/;var g=c("@marcom/ac-useragent");
var a=(g.os.ios||g.os.android);function h(j){this._modal=j.modal;this._player=j.player;
this._mediaElement=j.player.getMediaElement();this._posterEl=this._player.el.querySelector(".ac-video-poster img");
this._playerContainer=this._player.el.parentElement;this._bindMethods();this._addEventListeners();
this._calcAspectRatio()}var f=h.prototype;f._bindMethods=function(){this._onLoadStart=this._onLoadStart.bind(this);
this._onResize=this._onResize.bind(this);this._fullScreenChange=this._fullScreenChange.bind(this);
this._calcAspectRatio=this._calcAspectRatio.bind(this);this._addResizeListeners=this._addResizeListeners.bind(this);
this._removeResizeListeners=this._removeResizeListeners.bind(this);this._onModalOpen=this._onModalOpen.bind(this)
};f._addEventListeners=function(){if(this._posterEl){this._posterEl.addEventListener("load",this._calcAspectRatio)
}this._modal.on("willopen",this._addResizeListeners);this._modal.on("open",this._onModalOpen);
this._modal.on("close",this._removeResizeListeners)};f._onModalOpen=function(){if(this._loadStarted){this._onResize();
this._player.el.style.display="";this._player.el.style.opacity=""}};f._addResizeListeners=function(){this._player.el.style.display="block";
this._player.el.style.opacity=0;window.addEventListener("resize",this._onResize);
window.addEventListener("orientationchange",this._onResize);this._player.on("loadstart",this._onLoadStart);
this._player.on("loadeddata",this._calcAspectRatio);this._player.on("fullscreen:change",this._fullScreenChange);
this._player.on("fullscreen:willenter",this._fullScreenChange);this._calcAspectRatio()
};f._removeResizeListeners=function(){this._onResize();window.removeEventListener("resize",this._onResize);
window.removeEventListener("orientationchange",this._onResize);this._player.off("loadstart",this._onLoadStart);
this._player.off("loadeddata",this._calcAspectRatio);this._player.off("fullscreen:change",this._fullScreenChange)
};f._removeEventListeners=function(){this._removeResizeListeners();this._modal.off("willopen",this._addResizeListeners);
this._modal.off("open",this._onModalOpen);this._modal.off("close",this._removeResizeListeners);
if(this._posterEl){this._posterEl.removeEventListener("load",this._calcAspectRatio)
}};f._onLoadStart=function(){this._loadStarted=false;requestAnimationFrame(function(){this._loadStarted=true;
this._onModalOpen()}.bind(this));this._calcAspectRatio()};f._calcAspectRatio=function(){this._aspectRatio=(this._player.getMediaWidth()/this._player.getMediaHeight());
if((isNaN(this._aspectRatio)||this._aspectRatio<=0)&&this._mediaElement.src){if(i.test(this._mediaElement.src)){this._aspectRatio=(parseInt(RegExp.$1,10)/parseInt(RegExp.$2,10))
}}if((isNaN(this._aspectRatio)||this._aspectRatio<=0)&&this._posterEl){this._aspectRatio=(this._posterEl.naturalWidth/this._posterEl.naturalHeight)
}this._onResize()};f._fullScreenChange=function(j){if(j&&j.type==="enter"){setTimeout(function(){this._isFullScreen=true;
this._onResize()}.bind(this),60);return}this._isFullScreen=this._player.isFullscreen();
this._onResize()};f.destroy=function(){this._removeEventListeners()};f._onResize=function(){var o=this._aspectRatio;
if(isNaN(o)){return}var k=window.innerWidth;var q=window.innerHeight;var j=k/q;
if(this._mediaElement.readyState<1){var n=parseInt(getComputedStyle(this._playerContainer).maxWidth.replace("px",""));
var m=n/o;var l=parseInt(getComputedStyle(this._playerContainer).minWidth.replace("px",""));
var p=(a)?parseInt(getComputedStyle(this._player.el).maxHeight.replace("px","")):m;
if(m>q||(p&&m>p)){n=(p||q)*o;m=Math.min(n/o,q)}if(n>k||n>(m*o)){m=Math.min((k/o),q);
n=m*o}this._mediaElement.style.width=n+"px";this._mediaElement.style.height=Math.min(m,q)+"px"
}else{this._mediaElement.style.width="";this._mediaElement.style.height=""}if(j>o&&!this._isFullScreen){this._playerContainer.parentElement.classList.add("center-horizontal")
}else{this._playerContainer.parentElement.classList.remove("center-horizontal")
}this._player.refreshSize()};d.exports=h},{"@marcom/ac-useragent":171}],342:[function(b,d,a){var g=b("@marcom/ac-event-emitter-micro").EventEmitterMicro;
var c=b("@marcom/ac-feature/touchAvailable")();function h(i){i=i||{};this.el=i.el;
this._onTouchStart=this._onTouchStart.bind(this);this._onTouchMove=this._onTouchMove.bind(this);
this._onTouchEnd=this._onTouchEnd.bind(this);this._onClick=this._onClick.bind(this);
this._touchStart=false;g.call(this);this.activate()}var f=h.prototype=Object.create(g.prototype);
f._broadcastClick=function(i){this.trigger("click",{originalEvent:i})};f._onClick=function(i){i.stopPropagation();
i.preventDefault();if(!c){this._broadcastClick(i)}};f._onTouchStart=function(){this._touchStart=true
};f._onTouchEnd=function(i){if(this._touchStart===true){i.stopPropagation();i.preventDefault();
this._broadcastClick(i)}this._touchStart=false};f._onTouchMove=function(){this._touchStart=false
};f.activate=function(){if(c){this.el.addEventListener("touchstart",this._onTouchStart);
this.el.addEventListener("touchmove",this._onTouchMove);this.el.addEventListener("touchend",this._onTouchEnd)
}this.el.addEventListener("click",this._onClick)};f.deactivate=function(){this.el.removeEventListener("touchstart",this._onTouchStart);
this.el.removeEventListener("touchmove",this._onTouchMove);this.el.removeEventListener("touchend",this._onTouchEnd);
this.el.removeEventListener("click",this._onClick)};h.create=function(j,i){i=i||{};
return new h({el:j})};d.exports=h},{"@marcom/ac-event-emitter-micro":33,"@marcom/ac-feature/touchAvailable":40}],343:[function(c,d,b){var a=false;
window.addEventListener("load",function(){a=true});function f(g){if(a){g()}else{window.addEventListener("load",g)
}}d.exports=f},{}]},{},[340]);