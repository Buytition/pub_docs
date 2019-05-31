
<!DOCTYPE html>
<html class="no-js" lang="en-US" prefix="og: http://ogp.me/ns#">

<!-- head -->
<head>

<!-- meta -->
<meta charset="UTF-8" /><script type="text/javascript">window.NREUM||(NREUM={}),__nr_require=function(e,n,t){function r(t){if(!n[t]){var o=n[t]={exports:{}};e[t][0].call(o.exports,function(n){var o=e[t][1][n];return r(o||n)},o,o.exports)}return n[t].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<t.length;o++)r(t[o]);return r}({1:[function(e,n,t){function r(){}function o(e,n,t){return function(){return i(e,[c.now()].concat(u(arguments)),n?null:this,t),n?void 0:this}}var i=e("handle"),a=e(3),u=e(4),f=e("ee").get("tracer"),c=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],d="api-",l=d+"ixn-";a(p,function(e,n){s[n]=o(d+n,!0,"api")}),s.addPageAction=o(d+"addPageAction",!0),s.setCurrentRouteName=o(d+"routeName",!0),n.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,n){var t={},r=this,o="function"==typeof n;return i(l+"tracer",[c.now(),e,t],r),function(){if(f.emit((o?"":"no-")+"fn-start",[c.now(),r,o],t),o)try{return n.apply(this,arguments)}catch(e){throw f.emit("fn-err",[arguments,this,e],t),e}finally{f.emit("fn-end",[c.now()],t)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,n){m[n]=o(l+n)}),newrelic.noticeError=function(e,n){"string"==typeof e&&(e=new Error(e)),i("err",[e,c.now(),!1,n])}},{}],2:[function(e,n,t){function r(e,n){if(!o)return!1;if(e!==o)return!1;if(!n)return!0;if(!i)return!1;for(var t=i.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==t[a])return!1;return!0}var o=null,i=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var u=navigator.userAgent,f=u.match(a);f&&u.indexOf("Chrome")===-1&&u.indexOf("Chromium")===-1&&(o="Safari",i=f[1])}n.exports={agent:o,version:i,match:r}},{}],3:[function(e,n,t){function r(e,n){var t=[],r="",i=0;for(r in e)o.call(e,r)&&(t[i]=n(r,e[r]),i+=1);return t}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],4:[function(e,n,t){function r(e,n,t){n||(n=0),"undefined"==typeof t&&(t=e?e.length:0);for(var r=-1,o=t-n||0,i=Array(o<0?0:o);++r<o;)i[r]=e[n+r];return i}n.exports=r},{}],5:[function(e,n,t){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,n,t){function r(){}function o(e){function n(e){return e&&e instanceof r?e:e?f(e,u,i):i()}function t(t,r,o,i){if(!d.aborted||i){e&&e(t,r,o);for(var a=n(o),u=v(t),f=u.length,c=0;c<f;c++)u[c].apply(a,r);var p=s[y[t]];return p&&p.push([b,t,r,a]),a}}function l(e,n){h[e]=v(e).concat(n)}function m(e,n){var t=h[e];if(t)for(var r=0;r<t.length;r++)t[r]===n&&t.splice(r,1)}function v(e){return h[e]||[]}function g(e){return p[e]=p[e]||o(t)}function w(e,n){c(e,function(e,t){n=n||"feature",y[t]=n,n in s||(s[n]=[])})}var h={},y={},b={on:l,addEventListener:l,removeEventListener:m,emit:t,get:g,listeners:v,context:n,buffer:w,abort:a,aborted:!1};return b}function i(){return new r}function a(){(s.api||s.feature)&&(d.aborted=!0,s=d.backlog={})}var u="nr@context",f=e("gos"),c=e(3),s={},p={},d=n.exports=o();d.backlog=s},{}],gos:[function(e,n,t){function r(e,n,t){if(o.call(e,n))return e[n];var r=t();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return e[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(e,n,t){function r(e,n,t,r){o.buffer([e],r),o.emit(e,n,t)}var o=e("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(e,n,t){function r(e){var n=typeof e;return!e||"object"!==n&&"function"!==n?-1:e===window?0:a(e,i,function(){return o++})}var o=1,i="nr@id",a=e("gos");n.exports=r},{}],loader:[function(e,n,t){function r(){if(!E++){var e=x.info=NREUM.info,n=l.getElementsByTagName("script")[0];if(setTimeout(s.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&n))return s.abort();c(y,function(n,t){e[n]||(e[n]=t)}),f("mark",["onload",a()+x.offset],null,"api");var t=l.createElement("script");t.src="https://"+e.agent,n.parentNode.insertBefore(t,n)}}function o(){"complete"===l.readyState&&i()}function i(){f("mark",["domContent",a()+x.offset],null,"api")}function a(){return O.exists&&performance.now?Math.round(performance.now()):(u=Math.max((new Date).getTime(),u))-x.offset}var u=(new Date).getTime(),f=e("handle"),c=e(3),s=e("ee"),p=e(2),d=window,l=d.document,m="addEventListener",v="attachEvent",g=d.XMLHttpRequest,w=g&&g.prototype;NREUM.o={ST:setTimeout,SI:d.setImmediate,CT:clearTimeout,XHR:g,REQ:d.Request,EV:d.Event,PR:d.Promise,MO:d.MutationObserver};var h=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1123.min.js"},b=g&&w&&w[m]&&!/CriOS/.test(navigator.userAgent),x=n.exports={offset:u,now:a,origin:h,features:{},xhrWrappable:b,userAgent:p};e(1),l[m]?(l[m]("DOMContentLoaded",i,!1),d[m]("load",r,!1)):(l[v]("onreadystatechange",o),d[v]("onload",r)),f("mark",["firstbyte",u],null,"api");var E=0,O=e(5)},{}]},{},["loader"]);</script>
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
<meta name="google-site-verification" content="JAIWZWPP8qeVJa0ciP8DBw63lSxFFJYUvtcbSon9JfM" />
<link rel="shortcut icon" href="https://images.jazelc.com/uploads/galpinpremier/galpinIcon.png" />	
	

<!-- wp_head() -->
<title>Galpin Premier New Cars Inventory</title>
<!-- script | dynamic -->
<script id="mfn-dnmc-config-js">
//<![CDATA[
window.mfn_ajax = "https://www.galpinpremier.com/wp/wp-admin/admin-ajax.php";
window.mfn = {mobile_init:1025,nicescroll:40,parallax:"translate3d",responsive:1,retina_js:0};
window.mfn_lightbox = {disable:false,disableMobile:false,title:false,};
window.mfn_sliders = {blog:0,clients:0,offer:0,portfolio:0,shop:0,slider:0,testimonials:0};
//]]>
</script>
    <script type="text/javascript">
        (function() {
            window.jzla5p = {
                accountId: "0",
                publicEndpointBase: "//auto5-srp.jazelc.com/5.15.16",
                searchEndpointBase: "//search.jazelc.com/api/",
                mediaEndpointBase: "//media-cdn.jazelc.com/"
            };

            var combineUrl = function (url1, url2) {
                url1 = url1 || "";
                url2 = url2 || "";
                var url1ToCombine = url1.charAt(url1.length - 1) === "/" ? url1.substring(0, url1.length - 1) : url1;
                var url2ToCombine = url2.charAt(0) === "/" ? url2.substring(1) : url2;
                return url1ToCombine + "/" + url2ToCombine;
            };
            
            window._auto5ProductsStatic = combineUrl(window.jzla5p.publicEndpointBase, "/static/");
        })();
    </script>
    
<!-- This site is optimized with the Yoast SEO plugin v5.4.2 - https://yoast.com/wordpress/plugins/seo/ -->
<meta name="description" content="Galpin Premier has an exciting lineup of 2011 Aston Martin, Spyker, Lotus, Lincoln, Volvo and Jaguar models available now in Van Nuys, CA View New inventory, MSRP pricing and vehicle details online. Our beautiful dealership showroom is close to Los Angeles, Burbank, Glendale and surrounding L.A.communities."/>
<meta property="og:locale" content="en_US" />
<meta property="og:type" content="article" />
<meta property="og:title" content="Galpin Premier New Cars Inventory" />
<meta property="og:description" content="Galpin Premier has an exciting lineup of 2011 Aston Martin, Spyker, Lotus, Lincoln, Volvo and Jaguar models available now in Van Nuys, CA View New inventory, MSRP pricing and vehicle details online. Our beautiful dealership showroom is close to Los Angeles, Burbank, Glendale and surrounding L.A.communities." />
<meta property="og:site_name" content="Galpin Premier" />
<meta name="twitter:card" content="summary" />
<meta name="twitter:description" content="Galpin Premier has an exciting lineup of 2011 Aston Martin, Spyker, Lotus, Lincoln, Volvo and Jaguar models available now in Van Nuys, CA View New inventory, MSRP pricing and vehicle details online. Our beautiful dealership showroom is close to Los Angeles, Burbank, Glendale and surrounding L.A.communities." />
<meta name="twitter:title" content="Galpin Premier New Cars Inventory" />
<script type='application/ld+json'>{"@context":"http:\/\/schema.org","@type":"WebSite","@id":"#website","url":"https:\/\/www.galpinpremier.com\/","name":"Galpin Premier","potentialAction":{"@type":"SearchAction","target":"https:\/\/www.galpinpremier.com\/?s={search_term_string}","query-input":"required name=search_term_string"}}</script>
<!-- / Yoast SEO plugin. -->

<link rel='dns-prefetch' href='//cdn.rawgit.com' />
<link rel='dns-prefetch' href='//auto5-srp.jazelc.com' />
<link rel='dns-prefetch' href='//maxcdn.bootstrapcdn.com' />
<link rel='dns-prefetch' href='//fonts.googleapis.com' />
<link rel='dns-prefetch' href='//s.w.org' />
<link rel="alternate" type="application/rss+xml" title="Galpin Premier &raquo; Feed" href="https://www.galpinpremier.com/feed/" />
<link rel="alternate" type="application/rss+xml" title="Galpin Premier &raquo; Comments Feed" href="https://www.galpinpremier.com/comments/feed/" />
		<script type="text/javascript">
			window._wpemojiSettings = {"baseUrl":"https:\/\/s.w.org\/images\/core\/emoji\/2.3\/72x72\/","ext":".png","svgUrl":"https:\/\/s.w.org\/images\/core\/emoji\/2.3\/svg\/","svgExt":".svg","source":{"concatemoji":"https:\/\/www.galpinpremier.com\/wp\/wp-includes\/js\/wp-emoji-release.min.js?ver=4.8.2"}};
			!function(a,b,c){function d(a){var b,c,d,e,f=String.fromCharCode;if(!k||!k.fillText)return!1;switch(k.clearRect(0,0,j.width,j.height),k.textBaseline="top",k.font="600 32px Arial",a){case"flag":return k.fillText(f(55356,56826,55356,56819),0,0),b=j.toDataURL(),k.clearRect(0,0,j.width,j.height),k.fillText(f(55356,56826,8203,55356,56819),0,0),c=j.toDataURL(),b!==c&&(k.clearRect(0,0,j.width,j.height),k.fillText(f(55356,57332,56128,56423,56128,56418,56128,56421,56128,56430,56128,56423,56128,56447),0,0),b=j.toDataURL(),k.clearRect(0,0,j.width,j.height),k.fillText(f(55356,57332,8203,56128,56423,8203,56128,56418,8203,56128,56421,8203,56128,56430,8203,56128,56423,8203,56128,56447),0,0),c=j.toDataURL(),b!==c);case"emoji4":return k.fillText(f(55358,56794,8205,9794,65039),0,0),d=j.toDataURL(),k.clearRect(0,0,j.width,j.height),k.fillText(f(55358,56794,8203,9794,65039),0,0),e=j.toDataURL(),d!==e}return!1}function e(a){var c=b.createElement("script");c.src=a,c.defer=c.type="text/javascript",b.getElementsByTagName("head")[0].appendChild(c)}var f,g,h,i,j=b.createElement("canvas"),k=j.getContext&&j.getContext("2d");for(i=Array("flag","emoji4"),c.supports={everything:!0,everythingExceptFlag:!0},h=0;h<i.length;h++)c.supports[i[h]]=d(i[h]),c.supports.everything=c.supports.everything&&c.supports[i[h]],"flag"!==i[h]&&(c.supports.everythingExceptFlag=c.supports.everythingExceptFlag&&c.supports[i[h]]);c.supports.everythingExceptFlag=c.supports.everythingExceptFlag&&!c.supports.flag,c.DOMReady=!1,c.readyCallback=function(){c.DOMReady=!0},c.supports.everything||(g=function(){c.readyCallback()},b.addEventListener?(b.addEventListener("DOMContentLoaded",g,!1),a.addEventListener("load",g,!1)):(a.attachEvent("onload",g),b.attachEvent("onreadystatechange",function(){"complete"===b.readyState&&c.readyCallback()})),f=c.source||{},f.concatemoji?e(f.concatemoji):f.wpemoji&&f.twemoji&&(e(f.twemoji),e(f.wpemoji)))}(window,document,window._wpemojiSettings);
		</script>
		<style type="text/css">
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 .07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
    <style>
        body.freeze-body-behind-menu #wpadminbar { display: none; }

        .hmb-menu input[type="search"]::-webkit-search-cancel-button {
            display: none;
        }
    </style>
    <link rel='stylesheet' id='ajax-load-more-css'  href='/content/plugins/ajax-load-more/core/dist/css/ajax-load-more.min.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='sb_instagram_styles-css'  href='/content/plugins/instagram-feed/css/sb-instagram.min.css?ver=1.6.2' type='text/css' media='all' />
<link rel='stylesheet' id='sb-font-awesome-css'  href='https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css' type='text/css' media='all' />
<link rel='stylesheet' id='inventory-search-css'  href='/content/plugins/jazel-inventory-search/resources/assets/css/inventory-search.css?ver=1.0.0' type='text/css' media='all' />
<link rel='stylesheet' id='easy-tabs-style-css'  href='/content/plugins/jazel-inventory-search/resources/assets/css/easy-responsive-tabs.css?ver=1.0.0' type='text/css' media='all' />
<link rel='stylesheet' id='jzla5pbth-styles-css'  href='/content/plugins/jzl-auto5-products-betheme/styles/jzla5pbth-styles.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='gforms_reset_css-css'  href='/content/plugins/gravityforms/css/formreset.min.css?ver=1.9.14' type='text/css' media='all' />
<link rel='stylesheet' id='gforms_formsmain_css-css'  href='/content/plugins/gravityforms/css/formsmain.min.css?ver=1.9.14' type='text/css' media='all' />
<link rel='stylesheet' id='gforms_ready_class_css-css'  href='/content/plugins/gravityforms/css/readyclass.min.css?ver=1.9.14' type='text/css' media='all' />
<link rel='stylesheet' id='gforms_browsers_css-css'  href='/content/plugins/gravityforms/css/browsers.min.css?ver=1.9.14' type='text/css' media='all' />
<link rel='stylesheet' id='featherlight-styles-css'  href='//cdn.rawgit.com/noelboss/featherlight/1.3.5/release/featherlight.min.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='auto5-products-style-css'  href='//auto5-srp.jazelc.com/5.15.16/static/index.bundle.css?ver=5.15.16' type='text/css' media='all' />
<link rel='stylesheet' id='auto5-products-srp-local-styles-css'  href='/content/plugins/jzl-auto5-products/styles/jzla5p-srp.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='jzla5p-mobilenavbar-css'  href='/content/plugins/jzl-auto5-products/styles/jzla5p-mobilenavbar.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='popup-maker-site-css'  href='/content/plugins/popup-maker/assets/css/site.min.css?ver=1.6.5' type='text/css' media='all' />
<link rel='stylesheet' id='rs-plugin-settings-css'  href='https://www.galpinpremier.com/content/plugins/revslider2/public/assets/css/settings.css?ver=5.4.5.1' type='text/css' media='all' />
<style id='rs-plugin-settings-inline-css' type='text/css'>
#rs-demo-id {}
</style>
<link rel='stylesheet' id='jazel-base-css'  href='/content/themes/betheme/jazel/css/base.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='style-css'  href='/content/themes/betheme-child-buildout2/style.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-base-css'  href='/content/themes/betheme/css/base.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-layout-css'  href='/content/themes/betheme/css/layout.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-shortcodes-css'  href='/content/themes/betheme/css/shortcodes.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-animations-css'  href='/content/themes/betheme/assets/animations/animations.min.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-jquery-ui-css'  href='/content/themes/betheme/assets/ui/jquery.ui.all.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-jplayer-css'  href='/content/themes/betheme/assets/jplayer/css/jplayer.blue.monday.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-responsive-css'  href='/content/themes/betheme/css/responsive.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='Catamaran-css'  href='https://fonts.googleapis.com/css?family=Catamaran%3A1%2C400%2C400italic%2C500%2C700%2C700italic&#038;ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-child-style-css'  href='/content/themes/betheme-child-buildout2/style.css?ver=4.8.2' type='text/css' media='all' />
<link rel='stylesheet' id='mfn-skin-default-css'  href='/content/themes/betheme-child-buildout2/default.css?ver=20.4' type='text/css' media='all' />
<link rel='stylesheet' id='yelp-reviews-css'  href='/content/plugins/yelp-reviews-pro/lib/css/yelp-reviews.css?ver=1.0.0' type='text/css' media='all' />
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/jquery.js?ver=1.12.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/jquery-migrate.min.js?ver=1.4.1'></script>
<script type='text/javascript' src='/content/plugins/gravityforms/js/jquery.json.js?ver=1.9.14'></script>
<script type='text/javascript' src='/content/plugins/gravityforms/js/gravityforms.min.js?ver=1.9.14'></script>
<script type='text/javascript' src='/content/plugins/gravityforms/js/jquery.maskedinput.min.js?ver=1.9.14'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/content/plugins/revslider2/public/assets/js/jquery.themepunch.tools.min.js?ver=5.4.5.1'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/content/plugins/revslider2/public/assets/js/jquery.themepunch.revolution.min.js?ver=5.4.5.1'></script>
<script type='text/javascript' src='/content/plugins/gravityforms/js/placeholders.jquery.min.js?ver=1.9.14'></script>
<link rel='https://api.w.org/' href='https://www.galpinpremier.com/wp-json/' />
<link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://www.galpinpremier.com/wp/xmlrpc.php?rsd" />
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://www.galpinpremier.com/wp/wp-includes/wlwmanifest.xml" /> 
<meta name="generator" content="WordPress 4.8.2" />
<link rel='shortlink' href='https://www.galpinpremier.com/?p=7' />
<link rel="alternate" type="application/json+oembed" href="https://www.galpinpremier.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.galpinpremier.com%2Finventory%2Fnew-vehicles%2F" />
<link rel="alternate" type="text/xml+oembed" href="https://www.galpinpremier.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.galpinpremier.com%2Finventory%2Fnew-vehicles%2F&#038;format=xml" />
<!-- style | dynamic -->
<style id="mfn-dnmc-style-css">
@media only screen and (min-width: 1025px) {body:not(.header-simple) #Top_bar #menu{display:block!important}.tr-menu #Top_bar #menu{background:none!important}#Top_bar .menu > li > ul.mfn-megamenu{width:984px}#Top_bar .menu > li > ul.mfn-megamenu > li{float:left}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-1{width:100%}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-2{width:50%}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-3{width:33.33%}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-4{width:25%}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-5{width:20%}#Top_bar .menu > li > ul.mfn-megamenu > li.mfn-megamenu-cols-6{width:16.66%}#Top_bar .menu > li > ul.mfn-megamenu > li > ul{display:block!important;position:inherit;left:auto;top:auto;border-width:0 1px 0 0}#Top_bar .menu > li > ul.mfn-megamenu > li:last-child > ul{border:0}#Top_bar .menu > li > ul.mfn-megamenu > li > ul li{width:auto}#Top_bar .menu > li > ul.mfn-megamenu a.mfn-megamenu-title{text-transform:uppercase;font-weight:400;background:none}#Top_bar .menu > li > ul.mfn-megamenu a .menu-arrow{display:none}.menuo-right #Top_bar .menu > li > ul.mfn-megamenu{left:auto;right:0}.menuo-right #Top_bar .menu > li > ul.mfn-megamenu-bg{box-sizing:border-box}#Top_bar .menu > li > ul.mfn-megamenu-bg{padding:20px 166px 20px 20px;background-repeat:no-repeat;background-position:right bottom}.rtl #Top_bar .menu > li > ul.mfn-megamenu-bg{padding-left:166px;padding-right:20px;background-position:left bottom}#Top_bar .menu > li > ul.mfn-megamenu-bg > li{background:none}#Top_bar .menu > li > ul.mfn-megamenu-bg > li a{border:none}#Top_bar .menu > li > ul.mfn-megamenu-bg > li > ul{background:none!important;-webkit-box-shadow:0 0 0 0;-moz-box-shadow:0 0 0 0;box-shadow:0 0 0 0}.mm-vertical #Top_bar .container{position:relative;}.mm-vertical #Top_bar .top_bar_left{position:static;}.mm-vertical #Top_bar .menu > li ul{box-shadow:0 0 0 0 transparent!important;background-image:none;}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu{width:98%!important;margin:0 1%;padding:20px 0;}.mm-vertical.header-plain #Top_bar .menu > li > ul.mfn-megamenu{width:100%!important;margin:0;}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li{display:table-cell;float:none!important;width:10%;padding:0 15px;border-right:1px solid rgba(0, 0, 0, 0.05);}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li:last-child{border-right-width:0}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li.hide-border{border-right-width:0}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li a{border-bottom-width:0;padding:9px 15px;line-height:120%;}.mm-vertical #Top_bar .menu > li > ul.mfn-megamenu a.mfn-megamenu-title{font-weight:700;}.rtl .mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li:first-child{border-right-width:0}.rtl .mm-vertical #Top_bar .menu > li > ul.mfn-megamenu > li:last-child{border-right-width:1px}#Header_creative #Top_bar .menu > li > ul.mfn-megamenu{width:980px!important;margin:0;}.header-plain:not(.menuo-right) #Header .top_bar_left{width:auto!important}.header-stack.header-center #Top_bar #menu{display:inline-block!important}.header-simple #Top_bar #menu{display:none;height:auto;width:300px;bottom:auto;top:100%;right:1px;position:absolute;margin:0}.header-simple #Header a.responsive-menu-toggle{display:block;right:10px}.header-simple #Top_bar #menu > ul{width:100%;float:left}.header-simple #Top_bar #menu ul li{width:100%;padding-bottom:0;border-right:0;position:relative}.header-simple #Top_bar #menu ul li a{padding:0 20px;margin:0;display:block;height:auto;line-height:normal;border:none}.header-simple #Top_bar #menu ul li a:after{display:none}.header-simple #Top_bar #menu ul li a span{border:none;line-height:44px;display:inline;padding:0}.header-simple #Top_bar #menu ul li.submenu .menu-toggle{display:block;position:absolute;right:0;top:0;width:44px;height:44px;line-height:44px;font-size:30px;font-weight:300;text-align:center;cursor:pointer;color:#444;opacity:0.33;}.header-simple #Top_bar #menu ul li.submenu .menu-toggle:after{content:"+"}.header-simple #Top_bar #menu ul li.hover > .menu-toggle:after{content:"-"}.header-simple #Top_bar #menu ul li.hover a{border-bottom:0}.header-simple #Top_bar #menu ul.mfn-megamenu li .menu-toggle{display:none}.header-simple #Top_bar #menu ul li ul{position:relative!important;left:0!important;top:0;padding:0;margin:0!important;width:auto!important;background-image:none}.header-simple #Top_bar #menu ul li ul li{width:100%!important;display:block;padding:0;}.header-simple #Top_bar #menu ul li ul li a{padding:0 20px 0 30px}.header-simple #Top_bar #menu ul li ul li a .menu-arrow{display:none}.header-simple #Top_bar #menu ul li ul li a span{padding:0}.header-simple #Top_bar #menu ul li ul li a span:after{display:none!important}.header-simple #Top_bar .menu > li > ul.mfn-megamenu a.mfn-megamenu-title{text-transform:uppercase;font-weight:400}.header-simple #Top_bar .menu > li > ul.mfn-megamenu > li > ul{display:block!important;position:inherit;left:auto;top:auto}.header-simple #Top_bar #menu ul li ul li ul{border-left:0!important;padding:0;top:0}.header-simple #Top_bar #menu ul li ul li ul li a{padding:0 20px 0 40px}.rtl.header-simple #Top_bar #menu{left:1px;right:auto}.rtl.header-simple #Top_bar a.responsive-menu-toggle{left:10px;right:auto}.rtl.header-simple #Top_bar #menu ul li.submenu .menu-toggle{left:0;right:auto}.rtl.header-simple #Top_bar #menu ul li ul{left:auto!important;right:0!important}.rtl.header-simple #Top_bar #menu ul li ul li a{padding:0 30px 0 20px}.rtl.header-simple #Top_bar #menu ul li ul li ul li a{padding:0 40px 0 20px}.menu-highlight #Top_bar .menu > li{margin:0 2px}.menu-highlight:not(.header-creative) #Top_bar .menu > li > a{margin:20px 0;padding:0;-webkit-border-radius:5px;border-radius:5px}.menu-highlight #Top_bar .menu > li > a:after{display:none}.menu-highlight #Top_bar .menu > li > a span:not(.description){line-height:50px}.menu-highlight #Top_bar .menu > li > a span.description{display:none}.menu-highlight.header-stack #Top_bar .menu > li > a{margin:10px 0!important}.menu-highlight.header-stack #Top_bar .menu > li > a span:not(.description){line-height:40px}.menu-highlight.header-transparent #Top_bar .menu > li > a{margin:5px 0}.menu-highlight.header-simple #Top_bar #menu ul li,.menu-highlight.header-creative #Top_bar #menu ul li{margin:0}.menu-highlight.header-simple #Top_bar #menu ul li > a,.menu-highlight.header-creative #Top_bar #menu ul li > a{-webkit-border-radius:0;border-radius:0}.menu-highlight:not(.header-fixed):not(.header-simple) #Top_bar.is-sticky .menu > li > a{margin:10px 0!important;padding:5px 0!important}.menu-highlight:not(.header-fixed):not(.header-simple) #Top_bar.is-sticky .menu > li > a span{line-height:30px!important}.header-modern.menu-highlight.menuo-right .menu_wrapper{margin-right:20px}.menu-line-below #Top_bar .menu > li > a:after{top:auto;bottom:-4px}.menu-line-below #Top_bar.is-sticky .menu > li > a:after{top:auto;bottom:-4px}.menu-line-below-80 #Top_bar:not(.is-sticky) .menu > li > a:after{height:4px;left:10%;top:50%;margin-top:20px;width:80%}.menu-line-below-80-1 #Top_bar:not(.is-sticky) .menu > li > a:after{height:1px;left:10%;top:50%;margin-top:20px;width:80%}.menu-link-color #Top_bar .menu > li > a:after{display:none!important}.menu-arrow-top #Top_bar .menu > li > a:after{background:none repeat scroll 0 0 rgba(0,0,0,0)!important;border-color:#ccc transparent transparent;border-style:solid;border-width:7px 7px 0;display:block;height:0;left:50%;margin-left:-7px;top:0!important;width:0}.menu-arrow-top.header-transparent #Top_bar .menu > li > a:after,.menu-arrow-top.header-plain #Top_bar .menu > li > a:after{display:none}.menu-arrow-top #Top_bar.is-sticky .menu > li > a:after{top:0!important}.menu-arrow-bottom #Top_bar .menu > li > a:after{background:none!important;border-color:transparent transparent #ccc;border-style:solid;border-width:0 7px 7px;display:block;height:0;left:50%;margin-left:-7px;top:auto;bottom:0;width:0}.menu-arrow-bottom.header-transparent #Top_bar .menu > li > a:after,.menu-arrow-bottom.header-plain #Top_bar .menu > li > a:after{display:none}.menu-arrow-bottom #Top_bar.is-sticky .menu > li > a:after{top:auto;bottom:0}.menuo-no-borders #Top_bar .menu > li > a span:not(.description){border-right-width:0}.menuo-no-borders #Header_creative #Top_bar .menu > li > a span{border-bottom-width:0}.menuo-right #Top_bar .menu_wrapper{float:right}.menuo-right.header-stack:not(.header-center) #Top_bar .menu_wrapper{margin-right:150px}body.header-creative{padding-left:50px}body.header-creative.header-open{padding-left:250px}body.error404,body.under-construction,body.template-blank{padding-left:0!important}.header-creative.footer-fixed #Footer,.header-creative.footer-sliding #Footer,.header-creative.footer-stick #Footer.is-sticky{box-sizing:border-box;padding-left:50px;}.header-open.footer-fixed #Footer,.header-open.footer-sliding #Footer,.header-creative.footer-stick #Footer.is-sticky{padding-left:250px;}.header-rtl.header-creative.footer-fixed #Footer,.header-rtl.header-creative.footer-sliding #Footer,.header-rtl.header-creative.footer-stick #Footer.is-sticky{padding-left:0;padding-right:50px;}.header-rtl.header-open.footer-fixed #Footer,.header-rtl.header-open.footer-sliding #Footer,.header-rtl.header-creative.footer-stick #Footer.is-sticky{padding-right:250px;}#Header_creative{background:#fff;position:fixed;width:250px;height:100%;left:-200px;top:0;z-index:9002;-webkit-box-shadow:2px 0 4px 2px rgba(0,0,0,.15);box-shadow:2px 0 4px 2px rgba(0,0,0,.15)}#Header_creative .container{width:100%}#Header_creative .creative-wrapper{opacity:0;margin-right:50px}#Header_creative a.creative-menu-toggle{display:block;width:34px;height:34px;line-height:34px;font-size:22px;text-align:center;position:absolute;top:10px;right:8px;border-radius:3px}.admin-bar #Header_creative a.creative-menu-toggle{top:42px}#Header_creative #Top_bar{position:static;width:100%}#Header_creative #Top_bar .top_bar_left{width:100%!important;float:none}#Header_creative #Top_bar .top_bar_right{width:100%!important;float:none;height:auto;margin-bottom:35px;text-align:center;padding:0 20px;top:0;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}#Header_creative #Top_bar .top_bar_right:before{display:none}#Header_creative #Top_bar .top_bar_right_wrapper{top:0}#Header_creative #Top_bar .logo{float:none;text-align:center;margin:15px 0}#Header_creative #Top_bar .menu_wrapper{float:none;margin:0 0 30px}#Header_creative #Top_bar .menu > li{width:100%;float:none;position:relative}#Header_creative #Top_bar .menu > li > a{padding:0;text-align:center}#Header_creative #Top_bar .menu > li > a:after{display:none}#Header_creative #Top_bar .menu > li > a span{border-right:0;border-bottom-width:1px;line-height:38px}#Header_creative #Top_bar .menu li ul{left:100%;right:auto;top:0;box-shadow:2px 2px 2px 0 rgba(0,0,0,0.03);-webkit-box-shadow:2px 2px 2px 0 rgba(0,0,0,0.03)}#Header_creative #Top_bar .menu > li > ul.mfn-megamenu{width:700px!important;}#Header_creative #Top_bar .menu > li > ul.mfn-megamenu > li > ul{left:0}#Header_creative #Top_bar .menu li ul li a{padding-top:9px;padding-bottom:8px}#Header_creative #Top_bar .menu li ul li ul{top:0!important}#Header_creative #Top_bar .menu > li > a span.description{display:block;font-size:13px;line-height:28px!important;clear:both}#Header_creative #Top_bar .search_wrapper{left:100%;top:auto;bottom:0}#Header_creative #Top_bar a#header_cart{display:inline-block;float:none;top:3px}#Header_creative #Top_bar a#search_button{display:inline-block;float:none;top:3px}#Header_creative #Top_bar .wpml-languages{display:inline-block;float:none;top:0}#Header_creative #Top_bar .wpml-languages.enabled:hover a.active{padding-bottom:9px}#Header_creative #Top_bar a.button.action_button{display:inline-block;float:none;top:16px;margin:0}#Header_creative #Top_bar .banner_wrapper{display:block;text-align:center}#Header_creative #Top_bar .banner_wrapper img{max-width:100%;height:auto;display:inline-block}#Header_creative #Action_bar{position:absolute;bottom:0;top:auto;clear:both;padding:0 20px;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}#Header_creative #Action_bar .social{float:none;text-align:center;padding:5px 0 15px}#Header_creative #Action_bar .social li{margin-bottom:2px}#Header_creative .social li a{color:rgba(0,0,0,.5)}#Header_creative .social li a:hover{color:#000}#Header_creative .creative-social{position:absolute;bottom:10px;right:0;width:50px}#Header_creative .creative-social li{display:block;float:none;width:100%;text-align:center;margin-bottom:5px}.header-creative .fixed-nav.fixed-nav-prev{margin-left:50px}.header-creative.header-open .fixed-nav.fixed-nav-prev{margin-left:250px}.menuo-last #Header_creative #Top_bar .menu li.last ul{top:auto;bottom:0}.header-open #Header_creative{left:0}.header-open #Header_creative .creative-wrapper{opacity:1;margin:0!important;}.header-open #Header_creative .creative-menu-toggle,.header-open #Header_creative .creative-social{display:none}body.header-rtl.header-creative{padding-left:0;padding-right:50px}.header-rtl #Header_creative{left:auto;right:-200px}.header-rtl.nice-scroll #Header_creative{margin-right:10px}.header-rtl #Header_creative .creative-wrapper{margin-left:50px;margin-right:0}.header-rtl #Header_creative a.creative-menu-toggle{left:8px;right:auto}.header-rtl #Header_creative .creative-social{left:0;right:auto}.header-rtl #Footer #back_to_top.sticky{right:125px}.header-rtl #popup_contact{right:70px}.header-rtl #Header_creative #Top_bar .menu li ul{left:auto;right:100%}.header-rtl #Header_creative #Top_bar .search_wrapper{left:auto;right:100%;}.header-rtl .fixed-nav.fixed-nav-prev{margin-left:0!important}.header-rtl .fixed-nav.fixed-nav-next{margin-right:50px}body.header-rtl.header-creative.header-open{padding-left:0;padding-right:250px!important}.header-rtl.header-open #Header_creative{left:auto;right:0}.header-rtl.header-open #Footer #back_to_top.sticky{right:325px}.header-rtl.header-open #popup_contact{right:270px}.header-rtl.header-open .fixed-nav.fixed-nav-next{margin-right:250px}#Header_creative.active{left:-1px;}.header-rtl #Header_creative.active{left:auto;right:-1px;}#Header_creative.active .creative-wrapper{opacity:1;margin:0}.header-creative .vc_row[data-vc-full-width]{padding-left:50px}.header-creative.header-open .vc_row[data-vc-full-width]{padding-left:250px}.header-open .vc_parallax .vc_parallax-inner { left:auto; width: calc(100% - 250px); }.header-open.header-rtl .vc_parallax .vc_parallax-inner { left:0; right:auto; }#Header_creative.scroll{height:100%;overflow-y:auto}#Header_creative.scroll:not(.dropdown) .menu li ul{display:none!important}#Header_creative.scroll #Action_bar{position:static}#Header_creative.dropdown{outline:none}#Header_creative.dropdown #Top_bar .menu_wrapper{float:left}#Header_creative.dropdown #Top_bar #menu ul li{position:relative;float:left}#Header_creative.dropdown #Top_bar #menu ul li a:after{display:none}#Header_creative.dropdown #Top_bar #menu ul li a span{line-height:38px;padding:0}#Header_creative.dropdown #Top_bar #menu ul li.submenu .menu-toggle{display:block;position:absolute;right:0;top:0;width:38px;height:38px;line-height:38px;font-size:26px;font-weight:300;text-align:center;cursor:pointer;color:#444;opacity:0.33;}#Header_creative.dropdown #Top_bar #menu ul li.submenu .menu-toggle:after{content:"+"}#Header_creative.dropdown #Top_bar #menu ul li.hover > .menu-toggle:after{content:"-"}#Header_creative.dropdown #Top_bar #menu ul li.hover a{border-bottom:0}#Header_creative.dropdown #Top_bar #menu ul.mfn-megamenu li .menu-toggle{display:none}#Header_creative.dropdown #Top_bar #menu ul li ul{position:relative!important;left:0!important;top:0;padding:0;margin-left:0!important;width:auto!important;background-image:none}#Header_creative.dropdown #Top_bar #menu ul li ul li{width:100%!important}#Header_creative.dropdown #Top_bar #menu ul li ul li a{padding:0 10px;text-align:center}#Header_creative.dropdown #Top_bar #menu ul li ul li a .menu-arrow{display:none}#Header_creative.dropdown #Top_bar #menu ul li ul li a span{padding:0}#Header_creative.dropdown #Top_bar #menu ul li ul li a span:after{display:none!important}#Header_creative.dropdown #Top_bar .menu > li > ul.mfn-megamenu a.mfn-megamenu-title{text-transform:uppercase;font-weight:400}#Header_creative.dropdown #Top_bar .menu > li > ul.mfn-megamenu > li > ul{display:block!important;position:inherit;left:auto;top:auto}#Header_creative.dropdown #Top_bar #menu ul li ul li ul{border-left:0!important;padding:0;top:0}#Header_creative{transition: left .5s ease-in-out, right .5s ease-in-out;}#Header_creative .creative-wrapper{transition: opacity .5s ease-in-out, margin 0s ease-in-out .5s;}#Header_creative.active .creative-wrapper{transition: opacity .5s ease-in-out, margin 0s ease-in-out;}}@media only screen and (min-width: 1025px) {#Top_bar.is-sticky{position:fixed!important;width:100%;left:0;top:-60px;height:60px;z-index:701;background:#fff;opacity:.97;filter:alpha(opacity = 97);-webkit-box-shadow:0 2px 5px 0 rgba(0,0,0,0.1);-moz-box-shadow:0 2px 5px 0 rgba(0,0,0,0.1);box-shadow:0 2px 5px 0 rgba(0,0,0,0.1)}.layout-boxed.header-boxed #Top_bar.is-sticky{max-width:1025px;left:50%;-webkit-transform:translateX(-50%);transform:translateX(-50%)}.layout-boxed.header-boxed.nice-scroll #Top_bar.is-sticky{margin-left:-5px}#Top_bar.is-sticky .top_bar_left,#Top_bar.is-sticky .top_bar_right,#Top_bar.is-sticky .top_bar_right:before{background:none}#Top_bar.is-sticky .top_bar_right{top:-4px;height:auto;}#Top_bar.is-sticky .top_bar_right_wrapper{top:15px}.header-plain #Top_bar.is-sticky .top_bar_right_wrapper{top:0}#Top_bar.is-sticky .logo{width:auto;margin:0 30px 0 20px;padding:0}#Top_bar.is-sticky #logo{padding:5px 0!important;height:50px!important;line-height:50px!important}.logo-no-sticky-padding #Top_bar.is-sticky #logo{height:60px!important;line-height:60px!important}#Top_bar.is-sticky #logo img.logo-main{display:none}#Top_bar.is-sticky #logo img.logo-sticky{display:inline;max-height:35px;}#Top_bar.is-sticky .menu_wrapper{clear:none}#Top_bar.is-sticky .menu_wrapper .menu > li > a{padding:15px 0}#Top_bar.is-sticky .menu > li > a,#Top_bar.is-sticky .menu > li > a span{line-height:30px}#Top_bar.is-sticky .menu > li > a:after{top:auto;bottom:-4px}#Top_bar.is-sticky .menu > li > a span.description{display:none}#Top_bar.is-sticky .secondary_menu_wrapper,#Top_bar.is-sticky .banner_wrapper{display:none}.header-overlay #Top_bar.is-sticky{display:none}.sticky-dark #Top_bar.is-sticky{background:rgba(0,0,0,.8)}.sticky-dark #Top_bar.is-sticky #menu{background:rgba(0,0,0,.8)}.sticky-dark #Top_bar.is-sticky .menu > li > a{color:#fff}.sticky-dark #Top_bar.is-sticky .top_bar_right a{color:rgba(255,255,255,.5)}.sticky-dark #Top_bar.is-sticky .wpml-languages a.active,.sticky-dark #Top_bar.is-sticky .wpml-languages ul.wpml-lang-dropdown{background:rgba(0,0,0,0.3);border-color:rgba(0,0,0,0.1)}}@media only screen and (min-width: 768px) and (max-width: 1025px){.header_placeholder{height:0!important}}@media only screen and (max-width: 1024px){#Top_bar #menu{display:none;height:auto;width:300px;bottom:auto;top:100%;right:1px;position:absolute;margin:0}#Top_bar a.responsive-menu-toggle{display:block}#Top_bar #menu > ul{width:100%;float:left}#Top_bar #menu ul li{width:100%;padding-bottom:0;border-right:0;position:relative}#Top_bar #menu ul li a{padding:0 25px;margin:0;display:block;height:auto;line-height:normal;border:none}#Top_bar #menu ul li a:after{display:none}#Top_bar #menu ul li a span{border:none;line-height:44px;display:inline;padding:0}#Top_bar #menu ul li a span.description{margin:0 0 0 5px}#Top_bar #menu ul li.submenu .menu-toggle{display:block;position:absolute;right:15px;top:0;width:44px;height:44px;line-height:44px;font-size:30px;font-weight:300;text-align:center;cursor:pointer;color:#444;opacity:0.33;}#Top_bar #menu ul li.submenu .menu-toggle:after{content:"+"}#Top_bar #menu ul li.hover > .menu-toggle:after{content:"-"}#Top_bar #menu ul li.hover a{border-bottom:0}#Top_bar #menu ul li a span:after{display:none!important}#Top_bar #menu ul.mfn-megamenu li .menu-toggle{display:none}#Top_bar #menu ul li ul{position:relative!important;left:0!important;top:0;padding:0;margin-left:0!important;width:auto!important;background-image:none!important;box-shadow:0 0 0 0 transparent!important;-webkit-box-shadow:0 0 0 0 transparent!important}#Top_bar #menu ul li ul li{width:100%!important}#Top_bar #menu ul li ul li a{padding:0 20px 0 35px}#Top_bar #menu ul li ul li a .menu-arrow{display:none}#Top_bar #menu ul li ul li a span{padding:0}#Top_bar #menu ul li ul li a span:after{display:none!important}#Top_bar .menu > li > ul.mfn-megamenu a.mfn-megamenu-title{text-transform:uppercase;font-weight:400}#Top_bar .menu > li > ul.mfn-megamenu > li > ul{display:block!important;position:inherit;left:auto;top:auto}#Top_bar #menu ul li ul li ul{border-left:0!important;padding:0;top:0}#Top_bar #menu ul li ul li ul li a{padding:0 20px 0 45px}.rtl #Top_bar #menu{left:1px;right:auto}.rtl #Top_bar a.responsive-menu-toggle{left:20px;right:auto}.rtl #Top_bar #menu ul li.submenu .menu-toggle{left:15px;right:auto;border-left:none;border-right:1px solid #eee}.rtl #Top_bar #menu ul li ul{left:auto!important;right:0!important}.rtl #Top_bar #menu ul li ul li a{padding:0 30px 0 20px}.rtl #Top_bar #menu ul li ul li ul li a{padding:0 40px 0 20px}.header-stack .menu_wrapper a.responsive-menu-toggle{position:static!important;margin:11px 0!important}.header-stack .menu_wrapper #menu{left:0;right:auto}.rtl.header-stack #Top_bar #menu{left:auto;right:0}.admin-bar #Header_creative{top:32px}.header-creative.layout-boxed{padding-top:85px}.header-creative.layout-full-width #Wrapper{padding-top:60px}#Header_creative{position:fixed;width:100%;left:0!important;top:0;z-index:1001}#Header_creative .creative-wrapper{display:block!important;opacity:1!important}#Header_creative .creative-menu-toggle,#Header_creative .creative-social{display:none!important;opacity:1!important;filter:alpha(opacity=100)!important}#Header_creative #Top_bar{position:static;width:100%}#Header_creative #Top_bar #logo{height:50px;line-height:50px;padding:5px 0}#Header_creative #Top_bar #logo img.logo-sticky{max-height:40px!important}#Header_creative #logo img.logo-main{display:none}#Header_creative #logo img.logo-sticky{display:inline-block}.logo-no-sticky-padding #Header_creative #Top_bar #logo{height:60px;line-height:60px;padding:0}.logo-no-sticky-padding #Header_creative #Top_bar #logo img.logo-sticky{max-height:60px!important}#Header_creative #Top_bar #header_cart{top:21px}#Header_creative #Top_bar #search_button{top:20px}#Header_creative #Top_bar .wpml-languages{top:11px}#Header_creative #Top_bar .action_button{top:9px}#Header_creative #Top_bar .top_bar_right{height:60px;top:0}#Header_creative #Top_bar .top_bar_right:before{display:none}#Header_creative #Top_bar .top_bar_right_wrapper{top:0}#Header_creative #Action_bar{display:none}#Header_creative.scroll{overflow:visible!important}}html { background-color: #FFFFFF;}#Wrapper, #Content { background-color: #FFFFFF;}body, button, span.date_label, .timeline_items li h3 span, input[type="submit"], input[type="reset"], input[type="button"],input[type="text"], input[type="password"], input[type="tel"], input[type="email"], textarea, select, .offer_li .title h3 {font-family: "Catamaran", Arial, Tahoma, sans-serif;}#menu > ul > li > a, .action_button, #overlay-menu ul li a {font-family: "Catamaran", Arial, Tahoma, sans-serif;}#Subheader .title {font-family: "Catamaran", Arial, Tahoma, sans-serif;}h1, h2, h3, h4, .text-logo #logo {font-family: "Catamaran", Arial, Tahoma, sans-serif;}h5, h6 {font-family: "Catamaran", Arial, Tahoma, sans-serif;}blockquote {font-family: "Catamaran", Arial, Tahoma, sans-serif;}.chart_box .chart .num, .counter .desc_wrapper .number-wrapper, .how_it_works .image .number,.pricing-box .plan-header .price, .quick_fact .number-wrapper, .woocommerce .product div.entry-summary .price {font-family: "Catamaran", Arial, Tahoma, sans-serif;}body {font-size: 16px;line-height: 24px;font-weight: 400;letter-spacing: px;}big,.big {font-size: 16px;line-height: 28px;font-weight: 400;letter-spacing: 0px;}#menu > ul > li > a, a.button.action_button, #overlay-menu ul li a{font-size: 16px;font-weight: 100;letter-spacing: px;}#overlay-menu ul li a{line-height: 24px;}#Subheader .title {font-size: 36px;line-height: px;font-weight: 100;letter-spacing: px;}h1, .text-logo #logo { font-size: 36px;line-height: 36px;font-weight: 300;letter-spacing: px;}h2 { font-size: 30px;line-height: 30px;font-weight: 300;letter-spacing: px;}h3 {font-size: 25px;line-height: 27px;font-weight: 300;letter-spacing: px;}h4 {font-size: 21px;line-height: 25px;font-weight: 300;letter-spacing: px;}h5 {font-size: 15px;line-height: 20px;font-weight: 700;letter-spacing: px;}h6 {font-size: 13px;line-height: 20px;font-weight: 400;letter-spacing: px;}#Intro .intro-title { font-size: 70px;line-height: 70px;font-weight: 400;letter-spacing: 0px;}@media only screen and (min-width: 768px) and (max-width: 959px){body {font-size: 14px;line-height: 20px;}big,.big {font-size: 14px;line-height: 24px;}#menu > ul > li > a, a.button.action_button, #overlay-menu ul li a {font-size: 14px;}#overlay-menu ul li a{line-height: 21px;}#Subheader .title {font-size: 31px;line-height: 19px;}h1, .text-logo #logo { font-size: 31px;line-height: 31px;}h2 { font-size: 26px;line-height: 26px;}h3 {font-size: 21px;line-height: 23px;}h4 {font-size: 18px;line-height: 21px;}h5 {font-size: 13px;line-height: 19px;}h6 {font-size: 13px;line-height: 19px;}#Intro .intro-title { font-size: 60px;line-height: 60px;}blockquote { font-size: 15px;}.chart_box .chart .num { font-size: 45px; line-height: 45px; }.counter .desc_wrapper .number-wrapper { font-size: 45px; line-height: 45px;}.counter .desc_wrapper .title { font-size: 14px; line-height: 18px;}.faq .question .title { font-size: 14px; }.fancy_heading .title { font-size: 38px; line-height: 38px; }.offer .offer_li .desc_wrapper .title h3 { font-size: 32px; line-height: 32px; }.offer_thumb_ul li.offer_thumb_li .desc_wrapper .title h3 {font-size: 32px; line-height: 32px; }.pricing-box .plan-header h2 { font-size: 27px; line-height: 27px; }.pricing-box .plan-header .price > span { font-size: 40px; line-height: 40px; }.pricing-box .plan-header .price sup.currency { font-size: 18px; line-height: 18px; }.pricing-box .plan-header .price sup.period { font-size: 14px; line-height: 14px;}.quick_fact .number { font-size: 80px; line-height: 80px;}.trailer_box .desc h2 { font-size: 27px; line-height: 27px; }}@media only screen and (min-width: 480px) and (max-width: 767px){body {font-size: 13px;line-height: 19px;}big,.big {font-size: 13px;line-height: 21px;}#menu > ul > li > a, a.button.action_button, #overlay-menu ul li a {font-size: 13px;}#overlay-menu ul li a{line-height: 19.5px;}#Subheader .title {font-size: 27px;line-height: 19px;}h1, .text-logo #logo { font-size: 27px;line-height: 27px;}h2 { font-size: 23px;line-height: 23px;}h3 {font-size: 19px;line-height: 20px;}h4 {font-size: 16px;line-height: 19px;}h5 {font-size: 13px;line-height: 19px;}h6 {font-size: 13px;line-height: 19px;}#Intro .intro-title { font-size: 53px;line-height: 53px;}blockquote { font-size: 14px;}.chart_box .chart .num { font-size: 40px; line-height: 40px; }.counter .desc_wrapper .number-wrapper { font-size: 40px; line-height: 40px;}.counter .desc_wrapper .title { font-size: 13px; line-height: 16px;}.faq .question .title { font-size: 13px; }.fancy_heading .title { font-size: 34px; line-height: 34px; }.offer .offer_li .desc_wrapper .title h3 { font-size: 28px; line-height: 28px; }.offer_thumb_ul li.offer_thumb_li .desc_wrapper .title h3 {font-size: 28px; line-height: 28px; }.pricing-box .plan-header h2 { font-size: 24px; line-height: 24px; }.pricing-box .plan-header .price > span { font-size: 34px; line-height: 34px; }.pricing-box .plan-header .price sup.currency { font-size: 16px; line-height: 16px; }.pricing-box .plan-header .price sup.period { font-size: 13px; line-height: 13px;}.quick_fact .number { font-size: 70px; line-height: 70px;}.trailer_box .desc h2 { font-size: 24px; line-height: 24px; }}@media only screen and (max-width: 479px){body {font-size: 13px;line-height: 19px;}big,.big {font-size: 13px;line-height: 19px;}#menu > ul > li > a, a.button.action_button, #overlay-menu ul li a {font-size: 13px;}#overlay-menu ul li a{line-height: 19.5px;}#Subheader .title {font-size: 22px;line-height: 19px;}h1, .text-logo #logo { font-size: 22px;line-height: 22px;}h2 { font-size: 18px;line-height: 19px;}h3 {font-size: 15px;line-height: 19px;}h4 {font-size: 13px;line-height: 19px;}h5 {font-size: 13px;line-height: 19px;}h6 {font-size: 13px;line-height: 19px;}#Intro .intro-title { font-size: 42px;line-height: 42px;}blockquote { font-size: 13px;}.chart_box .chart .num { font-size: 35px; line-height: 35px; }.counter .desc_wrapper .number-wrapper { font-size: 35px; line-height: 35px;}.counter .desc_wrapper .title { font-size: 13px; line-height: 26px;}.faq .question .title { font-size: 13px; }.fancy_heading .title { font-size: 30px; line-height: 30px; }.offer .offer_li .desc_wrapper .title h3 { font-size: 26px; line-height: 26px; }.offer_thumb_ul li.offer_thumb_li .desc_wrapper .title h3 {font-size: 26px; line-height: 26px; }.pricing-box .plan-header h2 { font-size: 21px; line-height: 21px; }.pricing-box .plan-header .price > span { font-size: 32px; line-height: 32px; }.pricing-box .plan-header .price sup.currency { font-size: 14px; line-height: 14px; }.pricing-box .plan-header .price sup.period { font-size: 13px; line-height: 13px;}.quick_fact .number { font-size: 60px; line-height: 60px;}.trailer_box .desc h2 { font-size: 21px; line-height: 21px; }}.with_aside .sidebar.columns {width: 23%;}.with_aside .sections_group {width: 77%;}.aside_both .sidebar.columns {width: 18%;}.aside_both .sidebar.sidebar-1{ margin-left: -82%;}.aside_both .sections_group {width: 64%;margin-left: 18%;}@media only screen and (min-width:1240px){#Wrapper, .with_aside .content_wrapper {max-width: 1292px;}.section_wrapper, .container {max-width: 1272px;}.layout-boxed.header-boxed #Top_bar.is-sticky{max-width: 1292px;}}@media only screen and (max-width: 767px){.section_wrapper,.container,.four.columns .widget-area { max-width: 700px !important; }}#Top_bar #logo,.header-fixed #Top_bar #logo,.header-plain #Top_bar #logo,.header-transparent #Top_bar #logo {height: 0px;line-height: 0px;padding: 6px 0;}.logo-overflow #Top_bar:not(.is-sticky) .logo {height: 12px;}#Top_bar .menu > li > a {padding: -24px 0;}.menu-highlight:not(.header-creative) #Top_bar .menu > li > a {margin: -19px 0;}.header-plain:not(.menu-highlight) #Top_bar .menu > li > a span:not(.description) {line-height: 12px;}.header-fixed #Top_bar .menu > li > a {padding: -9px 0;}#Top_bar .top_bar_right,.header-plain #Top_bar .top_bar_right {height: 12px;}#Top_bar .top_bar_right_wrapper { top: -14px;}.header-plain #Top_bar a#header_cart, .header-plain #Top_bar a#search_button,.header-plain #Top_bar .wpml-languages,.header-plain #Top_bar a.button.action_button {line-height: 12px;}.header-plain #Top_bar .wpml-languages,.header-plain #Top_bar a.button.action_button {height: 12px;}@media only screen and (max-width: 767px){#Top_bar a.responsive-menu-toggle { top: 10px;}.mobile-header-mini #Top_bar #logo{height:50px!important;line-height:50px!important;margin:5px 0;}}.twentytwenty-before-label::before { content: "Before";}.twentytwenty-after-label::before { content: "After";}.blog-teaser li .desc-wrapper .desc{background-position-y:-1px;}
</style>
<!-- style | custom css | theme options -->
<style id="mfn-dnmc-theme-css">
/*Override theme extra padding for mobile*/
.section_wrapper {padding: 0 !important;}

@media all and (max-width:1024px) { .gg-invite-mobile2, .gg-chat-bubble.gg-app, .gg-app { display:none !important; } }

/* ********************
***    UTILITIES
******************** */
.flex { display:-webkit-box; display:-moz-box; display:-ms-flexbox; display:-webkit-flex; display:flex; }

@media all and (max-width:781px) {

   .admin-bar #jazel_mobile_header > div > div {
       top: 46px !important;
   }
}

@media all and (min-width:782px) {

.admin-bar #jazel_mobile_header > div > div {
       top: 33px !important;
   }
}


/* ***********************************************
    H E A D E R
*********************************************** */
#Header_wrapper {
    background-color: transparent;
    z-index: 2;
}

#Header #Action_bar { background: #082134; }

#Action_bar .column.one { margin-left:0; margin-right:0; width:100%; }

#google_translate_element {
    margin-top: 0;
    position: absolute;
    top: 0;
}

#Header #Action_bar .contact_details li {
    float: right;
    line-height: 29px;
    margin-left: 40px;
    width: auto;
}

#Header #Action_bar .contact_details a { color: #fff; }

.header_content { margin:0; }

.header_content .column {
    text-align: center;
}

#google_translate_element {
    text-align: right;
}

#Header #Top_bar {
    background-color: transparent;
}

#Top_bar .branding {
    display:block;
}

#Top_bar .branding,
#Top_bar.is-sticky .branding {
    background: #fff;
}

#Top_bar.is-sticky .top_bar_left {
    background: transparent;
}

    #Top_bar #logo { color:#000; white-space:nowrap; }
    #Top_bar .text-logo #logo > img { display:none; }
    #Top_bar #logo > span { color:#010101; display:inline-block; font-size:1em; line-height:normal; margin-top:3px; vertical-align:middle; }
    #Top_bar #logo > span em { font-style:normal; font-weight:bold; }

#Top_bar, #Action_bar { display:none; }
@media all and (min-width:1025px) {
    #Top_bar, #Action_bar { display:block; }
    #Top_bar.is-sticky #logo img.logo-sticky { display: none; }
}



    /* Action Bar */
    #Header #Action_bar { background:#082134; }
    #Action_bar .contact_details a { color:#fff; }

/* ADDED FOR CONTACT NUMBERS */
#Action_bar .column { width:100%;margin:0; }

#Action_bar .contact_details .button {
    padding: 0 30px !important;
    background: #0b2f4b;
    font-weight: bold;
    font-size: 14px;
    text-shadow: none;
}
.header-numbers {
    min-width: 300px;
    /*margin-right:-25px !important;*/
}
.header-numbers > div {
    display: -ms-flexbox;
    display: flex;
    -ms-flex-pack: start;
    justify-content: flex-start;
    -ms-flex-align: center;
    align-items: center;
    color:#000;
    font-weight:bold;
}
.header-numbers span.value {
    font-size:18px;
    line-height:1.5em;
    font-weight:normal;
    color:#000;
    min-width:50%;
}
.header-numbers span.value a {
    color:#000;
}
.header-numbers span.label {
    vertical-align: middle;
    display: inline-block;
    min-width: 50%;
    text-align: left;
    font-size:14px;
}
@media all and (max-width:1272px) {

    #Action_bar .container { width:100%;margin:0; }
    .header-numbers {margin-right: -16px !important;}
}

@media all and (max-width:900px) {

   .header-numbers { min-width:56%; }
   .header-numbers span.value { font-size:1.5vw !important; }
   .header-numbers span.label { font-size:1.35vw !important; }
}

@media only screen and (max-width:1441px) {

    .header-numbers { margin-right:19px !important; }
}


/* ********************
***    NAVIGATION
******************** */

#Top_bar .menu > li.highlight-item {background: #bf9e57;}
#Top_bar .menu > li.highlight-item a span { color:#fff; }

@media all and (max-height:800px) and (min-width:768px) {

    /* For short screens, i.e., 13" Mac Book @ default resolution */
    #Top_bar .menu_wrapper .menu li ul li { float:left; width:49% !important; }
    #Top_bar .menu_wrapper .menu li ul { min-width:40vw !important; }
}

@media all and (min-width:1024px) {

    #Top_bar #menu { width:100%; }
    #Top_bar .menu_wrapper .menu { display:-ms-flexbox; display:-webkit-flex; display:flex; -webkit-flex-wrap:nowrap; -moz-flex-wrap:nowrap; -ms-flex-wrap:nowrap; flex-wrap:nowrap; }
    #Top_bar .menu_wrapper .menu > li { -webkit-flex-grow:1; -moz-flex-grow:1; -ms-flex-grow:1; flex-grow:1; }
    #Top_bar .menu_wrapper { background:rgba(0,0,0,.8); }


    /* Top Navigation */
    #Header #Top_bar .menu > li > a,
    #Header #Top_bar .top_bar_right a { color:#fff; padding:13px 0 9px; }
    #Top_bar.is-sticky .menu_wrapper .menu > li > a { padding:7px 0 !important; }
    #Top_bar .menu > li.current-menu-item > a,
    #Top_bar .menu > li.current_page_item > a,
    #Top_bar .menu > li.current-menu-ancestor > a,
    #Top_bar .menu > li.current_page_ancestor > a,
    #Top_bar .menu > li.hover > a { color:#fff; }
    #Top_bar .menu > li > a > span:not(.description) { line-height:22px; font-weight:bold; }


    /* Sub-Navigation */
    #Top_bar .menu_wrapper .menu > li ul { background:rgba(0,0,0,.8); }
    #Top_bar .menu > li ul li a { color:#fff; }
    #Top_bar .menu > li ul li a:hover,
    #Top_bar .menu > li ul li.hover > a { color:#fff; }
    li.nav-home a span { font:0/0 arial; }
    li.nav-home a span:after { color:#fff; content:'\e89d'; display:inline-block; font-family:"mfn-icons"; font-style:normal; font-size:18px; font-variant:normal; font-weight:400; speak:none;
        line-height:1em; margin-left:.2em; margin-right:.2em; text-align:center; text-decoration:none!important; text-transform:none; vertical-align:middle; width:1em; }
}




/* ********************
***    CONTENT
******************** */  
#Content {
    position: relative;
    z-index: 0;
}
a, a:hover { color:#082134; }
.post-wrapper-content a {
    color: #bf9e57;
}

h3, h4, h5, h6 {color:#000;}
h1, h1 a, h1 a:hover { color: #000; }
	h2, h2 a, h2 a:hover { color: #000; }
	h3, h3 a, h3 a:hover { color: #000; }
	h4, h4 a, h4 a:hover { color: #000; }
	h5, h5 a, h5 a:hover { color: #000; }
	h6, h6 a, h6 a:hover, 
	a.content_link .title { color: #000; }	

/* Payment Calculator */
    .jazel-calc input[type='submit'] {
        border-color: #bf9e57;
        color: #bf9e57;
    }
    .jazel-calc input[type='submit']:hover {
    background: #bf9e57;
     }
    .jazel-calc .disclaimer > span { color: #bf9e57; }


@media all and (max-width:767px) {
    body { font-size:14px; }
}


/* L2 Ad Units */
aside.widget {
    padding-bottom: 0;
}
.jzl-photo-button a {
    position:relative;
    padding-top:25px;
    padding-left:30px;
    padding-right:20px;
    min-height:220px;
    display:block;
    background-size:cover !important; 
    max-width:270px;
    margin: 0 auto;
}
.jzl-photo-button a.white {
    color:#ffffff;
}
.jzl-photo-button a.gray{
    color:#000000;
}
.jzl-photo-button a:hover {
    text-decoration:none !important;
}
.jzl-photo-button-button {
    font-size:32px;
    font-weight:800;
    display:block;
    line-height: 36px;
}
.jzl-photo-button a::after {
    content:'';
    height:100%;
    left:0;
    position:absolute;
    top:0;
    width:100%;
}
.jzl-photo-button a:hover::after {
    background: rgba(0,0,0,.2) url('https://images.jazelc.com/uploads/galpinpremier/hover_arrow.png') center center no-repeat;
}

.jzl-sidebar { 
    border:1px solid #bdbdbd; 
    color:#000; 
    font-size:.875em; 
    line-height:22px; 
    max-width:320px; 
    min-height:220px; 
    overflow:hidden; 
    padding:24px 20px 24px 32px; 
    position:relative; 
    margin: 0 auto 2em;
    box-sizing: border-box;
}
.jzl-sidebar h1,
.jzl-sidebar h2,
.jzl-sidebar h3,
.jzl-sidebar h4 { 
    font-size:2.143em; 
    font-weight:bold; 
    margin-bottom:10px; 
    line-height: 1.25;
}
.jzl-sidebar p {
    line-height: 1.5;
}
.jzl-sidebar a { 
    color: inherit; 
    text-decoration:underline; 
}
.jzl-sidebar * { 
    position:relative; 
    z-index:5; 
}
.jzl-sidebar.white * { 
    color:#fff !important; 
}
.jzl-sidebar .click-handler { 
    bottom:0; 
    font-size:0; 
    height:100%; 
    left:0; 
    line-height:0; 
    position:absolute; 
    width:100%; 
    z-index:10; 
}
.jzl-sidebar .click-handler:hover { 
    background:rgba(0,0,0,.5) url(https://images.jazelc.com/uploads/galpinpremier/hover_arrow.png) scroll no-repeat center !important;
}
.jzl-sidebar > img { 
    bottom:0; 
    left:0; 
    position:absolute; 
    width:100% !important; 
    z-index:1; 
}
.jzl-sidebar.bg-fullheight > img { 
    height:100% !important; 
    max-width:none !important; 
    width:auto !important; 
}
.jzl-sidebar.bg-cover > img { 
    height:100% !important; 
}

@media all and (min-width: 1200px) {
    .jzl-sidebar h1,
    .jzl-sidebar h2,
    .jzl-sidebar h3,
    .jzl-sidebar h4 { 
        font-size: 1.875em;
    }
    .jzl-sidebar p {
        font-size: .95em;
    }

}

@media all and (min-width: 1024px) and (max-width: 1200px) {
    .jzl-sidebar {
        padding: 24px 24px 24px 28px;
    }
    .jzl-sidebar h1,
    .jzl-sidebar h2,
    .jzl-sidebar h3,
    .jzl-sidebar h4 { 
        font-size: 2vw;
    }
    .jzl-sidebar p {
        font-size: 1vw;
    }
}

@media all and (min-width:768px) and (max-width:1023px) {
    .jzl-photo-button-button { 
        font-size: 22px; 
        line-height:1em; 
    }
    .jzl-photo-button a { 
        padding-left:1vw; 
    }
    .jzl-sidebar {
        padding: 15px 15px 20px 20px;
    }
    .jzl-sidebar h1,
    .jzl-sidebar h2,
    .jzl-sidebar h3,
    .jzl-sidebar h4 { 
        font-size: 1.725em;
    }
    .jzl-sidebar p {
        font-size: .95em;
        line-height: 1.5;
    }
}
@media all and (max-width:767px) {
    aside.widget_text { 
        padding-bottom: 0;
        margin-bottom:0; 
    }
    .jzl-sidebar { 
        height: auto;
        min-height: 220px;
    }
}


    
/* Revolution Slider */
    .rev_slider video::-webkit-media-controls { display:none !important; }
    .rev_slider video::-webkit-media-controls-panel { display:none !important; -webkit-appearance:none !important; }
    .rev_slider video::--webkit-media-controls-play-button { display:none !important; -webkit-appearance:none !important; }
    .rev_slider video::-webkit-media-controls-start-playback-button { display:none !important; -webkit-appearance:none !important; }    

    
/* Tables */
    table tr:first-child td { background:none; border-top:solid 1px rgba(0,0,0,0.1) !important; }
    h3 { margin-bottom:0.25em; }


/* Forms */
.gform_wrapper .gfield input[type=text], .gform_wrapper .gfield input[type=number], .gform_wrapper .gfield select, .gform_wrapper .gfield textarea {
    min-height: 45px;
    background: #efefef;
    box-shadow: none;
    border: solid 1px #efefef;
    margin-bottom: 0;
}
.form_heading {
    background: #444;
    color: #fff;
    padding: 0.5em;
    margin-top: 30px !important;
    max-width: 94% !important;
}
    .gform_wrapper .gfield input[type=text], .gform_wrapper .gfield select { height:50px; padding:0 5px; }
    .gform_wrapper .gsection { border-bottom:none; }
    .gform_wrapper .gform_footer .gform_button[type='submit'] { border-color:#bf9e57; color:#fff;border-radius:0; }
    a.button_theme, a.tp-button.button_theme, button, input[type="submit"],
    input[type="reset"], input[type="button"] { background:#bf9e57; }
    .gform_wrapper .gfield input[type=text], .gform_wrapper .gfield select { height:50px; padding:0 5px; }

    
/* Blogs */
    .themebg, .pager .pages a:hover, .pager .pages a.active, .pager .pages span.page-numbers.current, .pager-single span:after,
    #comments .commentlist > li .reply a.comment-reply-link, .fixed-nav .arrow, #Filters .filters_wrapper ul li a:hover,
    #Filters .filters_wrapper ul li.current-cat a, .widget_categories ul, .Recent_posts ul li .desc:after, .Recent_posts ul li .photo .c,
    .widget_recent_entries ul li:after, .widget_mfn_menu ul li a:hover, .widget_mfn_menu ul li.current_page_item a, .widget_product_categories ul,
    div.jp-interface, #Top_bar a#header_cart span, .testimonials_slider .slider_images, .testimonials_slider .slider_images a:after,
    .testimonials_slider .slider_images:before, .slider_pagination a.selected, .slider_pagination a.selected:after,
    .tp-bullets.simplebullets.round .bullet.selected, .tp-bullets.simplebullets.round .bullet.selected:after,
    .tp-leftarrow.default, .tp-rightarrow.default, .tp-bullets.tp-thumbs .bullet.selected:after,
    .offer_thumb .slider_pagination a:before, .offer_thumb .slider_pagination a.selected:after { background-color:#bf9e57; }
    
    .themecolor, .opening_hours .opening_hours_wrapper li span, .fancy_heading_icon .icon_top, .fancy_heading_arrows .icon-right-dir,
    .fancy_heading_arrows .icon-left-dir, .fancy_heading_line h2, .button-love a.mfn-love, .format-link .post-title .icon-link,
    .pager-single > span, .pager-single a:hover, .widget_meta ul, .widget_pages ul, .widget_rss ul, .widget_mfn_recent_comments ul li:after,
    .widget_archive ul, .widget_recent_comments ul li:after, .widget_nav_menu ul, .woocommerce ul.products li.product .price,
    .shop_slider .shop_slider_ul li .item_wrapper .price, .woocommerce-page ul.products li.product .price, .widget_price_filter .price_label .from,
    .widget_price_filter .price_label .to, .woocommerce ul.product_list_widget li .quantity .amount, .woocommerce .product div.entry-summary .price,
    .woocommerce .star-rating span, #Error_404 .error_pic i { color:#bf9e57; }
    
    .hr_color, .hr_color hr, .hr_dots span { color:#bf9e57; background:#bf9e57; }
    
    
/* Shortcodes */
	.image_frame .image_wrapper .image_links { background: #bf9e57; }
	.image_frame .image_wrapper .image_links a:hover, .counter .icon_wrapper i, .quick_fact .number,
        a.content_link, a:hover.content_link, .icon_box .icon_wrapper, .icon_box a .icon_wrapper,
        .list_item .list_left, .feature_list ul li .icon i, .ui-tabs .ui-tabs-nav li.ui-state-active a,
        .accordion .question.active .title > .acc-icon-plus, .accordion .question.active .title > .acc-icon-minus,
        .faq .question.active .title > .acc-icon-plus, .faq .question.active .title, .accordion .question.active .title,
        .pricing-box .plan-header .price sup.currency, .pricing-box .plan-header .price > span { color: #bf9e57; }
	.sliding_box .desc_wrapper, .progress_bars .bars_list li .bar .progress, .how_it_works .image .number, ul.clients.clients_tiles li .client_wrapper:hover:before,
        .feature_list ul li:hover, .feature_list ul li:hover a, .ui-tabs .ui-tabs-nav li.ui-state-active a:after,
        .pricing-box .plan-inside ul li .yes, .pricing-box-box.pricing-box-featured { background: #bf9e57; }
	.sliding_box .desc_wrapper:after, a.content_link:before, ul.clients.clients_tiles li .client_wrapper:after { border-bottom-color: #bf9e57; }
	a:hover.icon_bar { color: #1f75c8 !important; }
	a.content_link:after, .timeline_items li h3:before, .timeline_items:after, .timeline .post-item:before { border-color: #bf9e57; }
	.get_in_touch, .infobox, .trailer_box .desc .subtitle, .icon_box:hover .icon_wrapper:before, .icon_box a:hover .icon_wrapper:before, .list_item.lists_1 .list_left { background-color: #bf9e57; }    


/* Coupons */
    .coupon table tr:first-child td { border-top:none !important; }
    .themeprint { color:#bf9e57; cursor:pointer; }

    @media print {
    
        body.coupon > * { display:none; }
        body.coupon > .for-print { border:3px dotted #000; display:block; }
        body.coupon { border:none; }
    }


/* Staff fix */
    .team .image_frame { display:inline-block; }


/* SRP HOOK */
img[src="https://images.jazelc.com/uploads/galpinpremier/Galpin-e-Price.png"] {max-width:100% !important;width:225px;}


    body.single-jzla5p_srp #Content { padding-top:0px !important; }
    .srp-hook { font-size:3vw; margin:10px 0; }
    .srp-hook-title { font-style:italic; font-size:4vw; font-weight:bold; }
    .srp-hook-123 > div { display:inline-block; padding:5px 0; vertical-align:middle; white-space:nowrap; width:28%; }
    .srp-hook-123 img { max-width:100%; vertical-align:middle; }
    .srp-hook-123 > div.srp-hook-3 { padding-left:2em; }

    @media all and (min-width:768px) {

        .srp-hook { font-size:20px; margin:auto; max-width:1024px; }
        .srp-hook-title { display:inline-block; font-size:24px; text-align:center; vertical-align:middle; width:25%; }
        .srp-hook-123 { display:inline-block; width:74%; }
    }


/* Eprice Form */
.hook-lead-header {
    padding: 1em;
    background: #efefef;
    border:solid 1px #dedede;
}

.hook-lead-title {
    font-weight:bold;
    text-align:center;
    font-size:1.25em;
    margin-bottom:0.5em;
}

.hook-lead-header-body {
    padding:0 1em 1em 0;
}

.eprice-form-bottom-part .vehicle-area {
    background:#efefef;
    margin-top:10px;
    border:solid 1px #dedede;
    margin-right:1em;
}
.eprice-form-bottom-part .gfield { margin-bottom: 10px; }
.eprice-form-bottom-part .gfield input[type="text"] { background:#fff !important; }
.eprice-form-bottom-part .gform_footer input[type="submit"] {
    width:100%;
}
.eprice-form-bottom-part .gform_wrapper { margin:0;max-width:100%; }
.eprice-form-bottom-part .gform_heading h3 { display:none;}
.eprice-form-bottom-part .gform_heading .gform_description { font-weight:bold; }
.eprice-form-top-part { margin-bottom:10px; }
.eprice-form-bottom-part .gform_body {
    padding: 10px;
    background: #efefef;
    border: solid 1px #dedede;
    width:100%;
}
.a5-eprice-form .photo-area { margin-top:5px;margin-bottom:10px; }
.a5-eprice-form .data-area > div { line-height:1.25em; }


/* VDP width offset */
@media all and (min-width:768px) {
.VehicleDetailsPage {
    margin-left: -1%;
    margin-right: -1%;
}
}
    
/* Misc */
    /* Hide this if present */
    img[src^='https://googleads.g.doubleclick.net'] { display:none; }
    iframe[name='google_conversion_frame'] { font-size:0 !important; float:left; height:0 !important; line-height:0 !important; margin-top:-13px; width:0 !important; }
    input[type="submit"] { -webkit-appearance:none; }

    @media all and (-ms-high-contrast:none), (-ms-high-contrast:active) {
    
        /* for IE11 fixed background bug */
        .bg-fixed.bg-fixed, .bg_fixed.bg_fixed { background-attachment:scroll; } 

        /* for IE 11 */
        select::-ms-expand { display:none; }
    }





/* ********************
***    FOOTER
******************** */  
#Footer { background:#000; font-size:16px; padding-top:21px; }
#Footer .widgets_wrapper .widget { padding:0; }
#Footer .widgets_wrapper > .container > .column { margin:0; }
#Footer .one { margin:0; width:100%; }
#Footer .one-second { margin:0; width:50%; }
#Footer .one-third { margin:0; width:33.33%; }


/* Footer Colors */
    #Footer,
    #Footer .widget_recent_entries ul li a { color:#fff; }
    #Footer a,  
    #Footer a:hover { color:#fff; }
    #Footer h1, #Footer h1 a, #Footer h1 a:hover,
    #Footer h2, #Footer h2 a, #Footer h2 a:hover,
    #Footer h3, #Footer h3 a, #Footer h3 a:hover,
    #Footer h4, #Footer h4 a, #Footer h4 a:hover,
    #Footer h5, #Footer h5 a, #Footer h5 a:hover,
    #Footer h6, #Footer h6 a, #Footer h6 a:hover { color:#fff; }


/* Footer Action Bar */
    .footer-action-bar { padding-bottom:0; padding-top:0; }
    .footer-action-bar > ul > li { margin-bottom:10px; }
    .footer-action-bar > ul > li > div { padding:0 4%; }
    .footer-action-bar1,
    .footer-action-bar2 { font-size:1em; min-height:67px; }
    .footer-action-bar1 { background:#082134; border-color:#082134; }
    .footer-action-bar2 { background:#bf9e57; border-color:#bf9e57; }
    .footer-action-bar .social a { line-height:0; text-decoration:none; }


/* Footer Site Name */
    .footer-sitename { line-height:normal; }
    .footer-sitename { display:block; font-size:1.75em; line-height:36px; margin-top:0; }
    .footer-sitename em { font-style:normal; font-weight:bold; }


/* Footer Social */
    .footer-social { -webkit-justify-content:space-around; -moz-justify-content:space-around; -ms-justify-content:space-around; justify-content:space-around;
        -webkit-flex-direction:row; -moz-flex-direction:row; -ms-flex-direction:row; flex-direction:row; -webkit-flex-wrap:wrap; -moz-flex-wrap:wrap; -ms-flex-wrap:wrap; flex-wrap:wrap; }


/* Footer Phone */
    .footer-phone { margin-top:15px; }
    .footer-phone a { display:inline-block; font-size:1.125em; line-height:22px; white-space:nowrap; }


/* Footer Logo */
    .footer-logo { margin-top:28px; }


/* Footer Links */
    .footer-links { display:-webkit-box; display:-moz-box; display:-ms-flexbox; display:-webkit-flex; display:flex; -webkit-justify-content:space-between; -moz-justify-content:space-between; -ms-justify-content:space-between;
        justify-content:space-between;  -webkit-flex-wrap:wrap; -moz-flex-wrap:wrap; -ms-flex-wrap:wrap; flex-wrap:wrap; margin-top:7px;  }
    .footer-links a { font-size:1em; line-height:20px; text-transform: uppercase;}


/* Footer Copyright */
    .footer-copyright { line-height:24px; margin-top:26px; }
    .footer-webmaster { margin-top:22px; }
    .footer-webmaster a { color: #bf9e57 !important; }


/* Below Footer */
    .below-footer > .container > .column { margin:0; }
    .bfooter h1, .below-footer h1 a, .below-footer h1 a:hover, .below-footer h2, .below-footer h2 a, .below-footer h2 a:hover, .below-footer h3, .below-footer h3 a, .below-footer h3 a:hover, .below-footer h4, .below-footer h4 a, .below-footer h4 a:hover, .below-footer h5, .below-footer h5 a, .below-footer h5 a:hover, .below-footer h6, .below-footer h6 a, .below-footer h6 a:hover {
    font-size: 1.5em;
}
    .bfooter a {text-decoration: underline;}

/* Page Footer Content */
    .page-footer-content { margin-top:23px; }


@media all and (min-width:768px) {

    #Footer { font-size:14px; padding-top:44px; }
    #Footer .widgets_wrapper { padding-bottom:0; }
    #Footer .widgets_wrapper .widget { overflow:visible; }
    #Footer .widgets_wrapper > .container { -webkit-align-items:center; -moz-align-items:center; -ms-align-items:center; align-items:center;
        display:-webkit-box; display:-moz-box; display:-ms-flexbox; display:-webkit-flex; display:flex; -webkit-justify-content:space-between;
        -moz-justify-content:space-between; -ms-justify-content:space-between; justify-content:space-between; }
    #Footer .widgets_wrapper > .container > div { -webkit-flex-grow:1; -moz-flex-grow:1; -ms-flex-grow:1; flex-grow:1; }

    /* Footer Bars */
    .footer-action-bar > ul > li { line-height:67px; margin-bottom:1%; }
    .footer-action-bar1,
    .footer-action-bar2 { min-height:67px; }
    .footer-action-bar li > div,
    .footer-action-bar li > ul { margin-bottom:0; }
    .footer-action-bar2 { text-align:right; }
    .footer-action-bar a { font-size:2.143em;  }

    /* Footer Social */
    .footer-social { -webkit-justify-content:flex-end; -moz-justify-content:flex-end; -ms-justify-content:flex-end; justify-content:flex-end; }
    .footer-social > a { line-height:63px; margin-left:30px; }

    /* Footer Sitename */
    .footer-sitename { font-size:2em; margin-top:0; }

    /* Footer Links */
    .footer-links { margin-top:32px; white-space:nowrap; }
    .footer-links a { display:inline-block; margin-bottom:0; white-space:nowrap; }

    /* Footer Phone */
    .footer-phone { display:-webkit-box; display:-moz-box; display:-ms-flexbox; display:-webkit-flex; display:flex; 
        -webkit-flex-wrap:wrap; -moz-flex-wrap:wrap; -ms-flex-wrap:wrap; flex-wrap:wrap; -webkit-justify-content:flex-end;
        -moz-justify-content:flex-end; -ms-justify-content:flex-end; justify-content:flex-end; margin:7px 0 0; }
    .footer-phone a { font-size:1.25em; line-height:normal; margin-left:30px; }
    .footer-phone a:first-child { margin-left:0; }

    /* Footer Logo */
    .footer-logo { margin-top:0; }
    
    /* Copyright */
    .footer-brand { -webkit-flex-wrap:nowrap; -moz-flex-wrap:nowrap; -ms-flex-wrap:nowrap; flex-wrap:nowrap; 
        -webkit-justify-content:space-between; -moz-justify-content:space-between; -ms-justify-content:space-between; justify-content:space-between; }
    .footer-copyright { margin-top:26px; padding:0; }
    .footer-webmaster { display:inline-block; margin-left:6.6vw; margin-top:0; padding:0; }
}

@media all and (min-width: 1024px) {

    #Footer { font-size:16px; }
    .footer-sitename { font-size:2.5em; }
    .footer-phone a { font-size:1.5em; margin-left:60px; }
}

@media all and (max-width:767px) {

    #Footer > div > .container { max-width:none !important; padding:0 15px; }
    .footer-links a { -webkit-flex-basis:50%; -moz-flex-basis:50%; -ms-flex-basis:50%; flex-basis:50%; }
}





/* ********************
***    NEWSLETTER
******************** */  
    .form_newsletter_wrapper .form_newsletter .gform_body { float:left; width:75%; }
    .footer-action-bar .form_newsletter_wrapper.gform_wrapper { font-size:1em; margin:auto; max-width:none; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield { line-height:normal; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield_label { color:#fff; font-size:1.125em; font-weight:bold; margin-bottom:0; margin-top:8px; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .ginput_container { display:inline-block; margin-top:1px; padding:0; width:100%; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_footer { clear:none; float:left; margin:31px 0 0 0; padding:0; width:25%; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield input[type=text] {
        background:#a98d51 !important; border-radius:3px; color:#e5e6e6; font-size:1em; font-style:normal; height:33px; line-height:33px; margin:0 0 10px 0; min-height:0; padding-left:15px; text-align:left;
    }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_footer input[type=submit] { 
        background-color:#fff; border-radius:3px; color:#000; float:left; font-size:1em; font-weight:bold; height:33px; line-height:33px; padding:0; text-transform:uppercase; width:100%;
    }

/* Placeholder */
    .footer-action-bar .form_newsletter_wrapper .gfield input[type=text]::-webkit-input-placeholder { color:#e5e6e6; }
    .footer-action-bar .form_newsletter_wrapper .gfield input[type=text]::-moz-placeholder { color:#e5e6e6; }
    .footer-action-bar .form_newsletter_wrapper .gfield input[type=text]:-ms-input-placeholder { color:#e5e6e6; }
    .footer-action-bar .form_newsletter_wrapper .gfield input[type=text]:-moz-placeholder { color:#e5e6e6; }

/* Validation */
    body .footer-action-bar .form_newsletter_wrapper .validation_message,
    body .footer-action-bar .form_newsletter_wrapper .validation_error,
    body .footer-action-bar .form_newsletter_wrapper .gform_anchor { display:none; }
    body .footer-action-bar .form_newsletter_wrapper .gform_ajax_spinner { display:inherit; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield.gfield_error input[type=text] { background:#ffeb10 !important; border-color:red !important; color:#393939; }

@media screen and (min-width:768px) {

    .form_newsletter_wrapper.gform_wrapper { margin:0; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter { white-space:nowrap; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_body { width:auto; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .ginput_container { margin-top:14px; padding:0 15px; width:auto; }    
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield { white-space:nowrap; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield_label { float:left; margin-top:22px; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield input[type=text] { height:42px; line-height:42px; margin-bottom:0px; width:100%; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_footer { margin-top:55px; }   
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_footer input[type=submit] { height:42px; line-height:42px; padding:0 18px; width:auto; }    
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_footer { margin-top:14px; width:auto; }
}

@media all and (min-width:768px) and (max-width:1023px) {

    .form_newsletter_wrapper.gform_wrapper .gform_footer input[type=submit] { padding:0 9px; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .gfield_label { font-size:1em; }
    .footer-action-bar .form_newsletter_wrapper .form_newsletter .gform_fields .ginput_container { padding:0 7px; }
}



/* ***********************************************
**** S R P  B A N N E R S
*********************************************** */

/* Heading */
.srp_h1 {
    font-weight:bold;
    display: inline-block;
    margin-right: 3%;
    color: #000;
    font-style: normal;
    font-size: 1.7vmax;
    padding:1% 2.125% 1% 2.125% !important;
}

/* Banner Backgrouds */
.used_srp_banner.ver1,
.new_srp_banner {
    background: rgb(249,249,249);
    background: radial-gradient(ellipse at center, rgba(249,249,249,1) 0%,rgba(224,224,224,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f9f9f9', endColorstr='#e0e0e0',GradientType=1 );
}
.used_srp_banner-mobile {
    background: rgb(116,116,116);
    background: radial-gradient(ellipse at center,  rgba(116,116,116,1) 0%,rgba(49,49,49,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#747474', endColorstr='#313131',GradientType=1 );
}

.used_srp_banner.ver2 {
    background:url(https://images.jazelc.com/uploads/galpinford/overlay_banner_bg.jpg) center bottom no-repeat;
    background-size:cover;
}

/* Mobile */
.used_srp_banner-mobile {
    display:none;
    color: #fff;
    font-weight: bold;
}
    .used_srp_banner-mobile img {
        vertical-align:middle;
        margin:5px 5px 3px 5px;
    }


/* Desktop */
.new_srp_banner { overflow:hidden; }
.used_srp_banner,
.new_srp_banner {
    display:-ms-flexbox;
    display:flex;
    -ms-flex-pack: start;
        justify-content: flex-start;
    -ms-flex-align: center;
        align-items: center;
    color:#000;
    -ms-flex-line-pack: stretch;
        align-content: stretch;
    padding: 0 2% !important;
}
    .used_srp_banner > div:first-child img {
        margin-top:5px;
        max-width:100% !important;
    }
    .new_srp_banner .banner-title {
        font-style: italic;
        font-size:1.5em;
        padding:0 10px;
        box-sizing:border-box;
        -ms-flex-preferred-size: 0;
            flex-basis: 0;
        -ms-flex-positive: 1;
            flex-grow: 1;
        text-align: left;
    }
    .used_srp_banner .banner-title {
        font-style: italic;
        font-size:1.5em;
        padding:0 10px;
        box-sizing:border-box;
        -ms-flex-preferred-size: 20%;
            flex-basis: 25%;
        -ms-flex-positive: 1;
            flex-grow: 1;
        text-align: center;
    }
    .used_srp_banner > div,
    .new_srp_banner > div {
        line-height:1.2em;
        font-size:0.875em;
    }
        .new_srp_banner > div:first-child {
            -ms-flex-preferred-size:5%;
                flex-basis:5%;
            margin-bottom: -38px;
        }
        .used_srp_banner > div:first-child {
            -ms-flex-preferred-size:10%;
                flex-basis:10%;
        }
        .used_srp_banner.ver1 > div:first-child {
            margin-bottom: -1.5%;
        }
        .used_srp_banner.ver2 > div:first-child {
            margin-top: -1.5%;
        }
        .used_srp_banner > div:last-child,
        .new_srp_banner > div:last-child {
            -ms-flex-preferred-size:60%;
                flex-basis:60%;
            display:-ms-flexbox;
            display:flex;
            -ms-flex-pack:distribute;
                justify-content:space-around;
            -ms-flex-align:end;
                align-items:flex-end;
            -ms-flex-positive: 1;
                flex-grow: 1;
        }
        .new_srp_banner > div:last-child {
            -ms-flex-pack:center;
                justify-content:center;
        }
        .used_srp_banner > div > div,
        .new_srp_banner > div > div {
            white-space:nowrap;
            display: -ms-flexbox;
            display: flex;
            -ms-flex-pack: center;
                justify-content: center;
            -ms-flex-positive: 1;
                flex-grow: 1;
            margin: 0.5%;
        }
        .used_srp_banner.ver1 > div > div,
        .new_srp_banner > div > div {
            background: #fafafa;
            padding: 0.8em;
            border-radius: 5px;
        }
            .new_srp_banner > div > div {
                -ms-flex-preferred-size: 25%;
                flex-basis: 25%;
                -ms-flex-positive: 1;
                flex-grow: 1;
            }
            .used_srp_banner > div > div > div img,
            .new_srp_banner > div > div > div img {
                vertical-align: middle;
                margin-right:5px;
                max-height:30px;
            }
            .used_srp_banner > div > div > div,
            .new_srp_banner > div > div > div {
                display: inline-block;
                vertical-align: middle;
                text-align:right;
                width: 20%;
                min-width:30px;
            }
            .used_srp_banner.ver2 > div > div > div { color:#000; font-weight:bold; }
            .used_srp_banner > div > div > div:last-child,
            .new_srp_banner > div > div > div:last-child {
                text-align:left;
                width:auto;
                font-size: 0.975em;
                padding-left: 0.125em;
            }
                .used_srp_banner > div > div:last-child > div:first-child {
                    width:30%;
                }
                    .used_srp_banner > div > div:last-child > div:first-child img {
                        margin-left: 0 !important;
                    }
                .used_srp_banner > div > div:last-child > div:last-child {
                    width:70%;
                    padding-left:10px;
                }

/* Responsive */
.new_srp_banner .show-for-small { display:none; }

@media all and (max-width:1300px) {

    .used_srp_banner > div,
    .new_srp_banner > div {
        -ms-flex-preferred-size:13%;
            flex-basis:13%;
    }
    .new_srp_banner > div:first-child {
        -ms-flex-preferred-size:20%;
            flex-basis:20%;
    }
        .new_srp_banner > div:first-child img {
            opacity: 0.1 !important;
            margin: -14% 0 -26% !important;
            max-width: 132% !important;
        }
    .used_srp_banner > div:first-child {
        -ms-flex-preferred-size:10%;
            flex-basis:10%;
        overflow:hidden;
    }
    .new_srp_banner .banner-title {
        -ms-flex-preferred-size:27%;
            flex-basis:27%;
        -ms-transform: translateX(-13%);
            transform: translateX(-13%);
        padding:5px 5px 10px;
    }
    .used_srp_banner .banner-title{
        -ms-flex-preferred-size:27%;
            flex-basis:27%;
    }
}

@media all and (max-width:1280px) {
    
    .used_srp_banner,
    .new_srp_banner { -ms-flex-wrap:wrap; flex-wrap:wrap; }
    .used_srp_banner > div > div > div img,
    .new_srp_banner > div > div > div img {
        margin-bottom:0;
    }
    .used_srp_banner .banner-title,
    .new_srp_banner .banner-title { text-align:center !important;font-size:3.5vw; }
    .used_srp_banner > div:last-child,
    .new_srp_banner > div:last-child {
        -ms-flex-preferred-size:80%;
            flex-basis:80%;
        margin-top: 1%;
        -ms-flex-item-align:end;
            align-self:flex-end;
        padding-bottom:10px;
     }
}

@media all and (max-width:768px) {
    
    .used_srp_banner,
    .hide-for-small { display:none; }
    .used_srp_banner-mobile { display:block; }
    .new_srp_banner .show-for-small { display:inline-block; }
    .new_srp_banner > div:first-child {
        max-height:50px;
    }
    .new_srp_banner .banner-title {
        -ms-flex-preferred-size:100%;
            flex-basis:100%;
        text-align: center !important;
        width: 100%;
        -ms-transform: none;
            transform: none;
        font-size:4vw;
    }
    .new_srp_banner > div:first-child img {
        margin: 0 0 -15%  !important;
        -ms-transform: translateY(-12%);
            transform: translateY(-12%);
       max-width: 250% !important;
    }
    .new_srp_banner > div:last-child {
        -ms-flex-preferred-size:100%;
            flex-basis:100%;
        width:100%;
        margin-left: 0 !important;
        padding: 0 2% 10px;
        box-sizing: border-box;
    }
    .new_srp_banner > div > div { 
        -ms-flex-wrap:wrap; 
            flex-wrap:wrap;
        padding: 1.4% !important;
        margin: 1%;
    }
    .new_srp_banner > div > div > div {
        display: block;
        text-align: center !important;
        width: 100%;
    }
    .new_srp_banner > div > div:nth-child(3) img {
        max-height: 35px !important;
        margin-bottom: -5px;
    }   
    .new_srp_banner > div > div > div:last-child {
        font-size: 0.8em;
        line-height:1em;
    }
}

/* VDP/SRP */
.a5-disclaimer {margin-bottom: 1em !important;}
.conditional-disclaimer {display: none;}
#a5-srp-container.a5-srp-container .VehicleDetailsPage.classic .price { display: none !important; }
#a5-srp-container.a5-srp-container .vehicleList .vehicle .eprice {
    margin-right:0 !important; 
}
#a5-srp-container.a5-srp-container .vehicleList .vehicle.overviewView .eprice img {
    float: right;
    max-width: 247px !important;
    min-width: 0 !important;
}
#a5-srp-container.a5-srp-container .vehicleList .vehicle.listView .eprice img {
    float: right;
    max-width: 220px !important;
    min-width: 0 !important;
}
#a5-srp-container.a5-srp-container { clear:both; }
#a5-srp-container.a5-srp-container .VehicleDetailsPage.classic .vehicleInformation .titleAndPrice .titleText h1 { font-size:26px !important; }
#a5-srp-container.a5-srp-container .VehicleDetailsPage.classic .vehicleInformation .titleAndPrice .price {
    display: none !important;
}
#a5-srp-container.a5-srp-container h1 { margin: 0.5em 0; }
#a5-srp-container.a5-srp-container .VehicleDetailsPage.classic .vdp-classic-top-right-row-one { margin-top:-60px; }
@media all and (max-width:767px) {
    #a5-srp-container.a5-srp-container .VehicleDetailsPage.classic .non-mobile-header-bar { margin-top:0 !important; }
}


/*****************************************************
    S I D E B A R   F O R M (Quick Question)
*****************************************************/
.sidebar-quick-contact.gform_wrapper {
    max-width: 1000px;
    overflow: hidden;
}
.sidebar-quick-contact .gform_heading {
    margin-bottom: 2em;
}
.sidebar-quick-contact .gform_heading h3 {
    font-size: 1.365em !important;
    font-weight: normal;
    line-height: 1em;
    margin-top: 0 !important;
}
.sidebar-quick-contact .gform_heading span {
    display: block;
    font-size: 1em !important;
}
.sidebar-quick-contact .gform_fields li {
    padding: 0 5px;
    box-sizing: border-box;
}
.sidebar-quick-contact .gform_fields li: first-child  {
    padding: 0;
}
.sidebar-quick-contact .gform_fields li: first-child span {
    width: 49.5% !important;
    margin: 0 !important;
    padding: 0 5px;
    box-sizing: border-box;
}
.sidebar-quick-contact .gform_fields .column {
    margin: 0 !important;
}
 .gform_fields .column.one-fourth {
    width: 25%;
}
body .sidebar-quick-contact .gform_wrapper label.gfield_label+div.ginput_container {
     margin-top:3px !important;
}
.sidebar-quick-contact .gform_fields label {
    color: #000;
    font-weight: bold;
}
.sidebar-quick-contact .gform_fields input[type="text"] {
    background: #eee;
    box-shadow: none;
    border: none;
    height: 45px !important;
    width: 100%;
}
.sidebar-quick-contact .gform_fields textarea {
    background: #eee;
    border: none;
}
.sidebar-quick-contact .gform_footer {
    clear: none;
    float: left;
    width: 33%;
    margin-top:  13px;
}
.sidebar-quick-contact .gform_footer input[type="submit"] {
    height: auto;
    line-height: normal;
    width: 100%;
    text-transform: uppercase;
    font-size:  1.3em;
}
.sidebar-quick-contact form {
    margin: 0;
}
.sidebar-quick-contact.with-comments .gform_fields li: first-child {
    padding: 0 5px;
}
.sidebar-quick-contact.with-comments .gform_fields .column.one {
    width: 100%;
}
.sidebar-quick-contact.with-comments .gform_fields .column.one textarea {
    width: 100%;
    height: 100px;
    margin-bottom: 0;
}
.sidebar-quick-contact.with-comments .gform_footer {
    width: 100%;
    text-align: center;
    overflow:visible;
}
.sidebar-quick-contact.with-comments .gform_footer input[type="submit"] {
    background: none;
    border: 1px solid #000;
    border-radius: 0;
    color: #000;
    font-size: 1em;
    font-weight: bold;
    max-width: 80%;    
    padding: 10px 0 !important;
    width: 100%;    
}
.sidebar-quick-contact.with-comments .gform_footer input[type="submit"]:hover {
    background:#000;
    color:#fff;
}
.sidebar-quick-contact .gform_wrapper li.gfield.gfield_error {
    background-color: transparent;
    padding: 0 5px;
}
.sidebar-quick-contact  .gfield.gfield_error .ginput_container {
    margin-top: .375em !important;
}

@media all and (min-width: 767px) {
    .sidebar-quick-contact .gform_fields li: first-child {
        width: 50%;
        margin: 0;
    }
}

@media all and (max-width: 600px) {
    .sidebar-quick-contact {
        margin: 25px auto;
    }
    .sidebar-quick-contact .gform_fields li: first-child span {
        width: 100% !important;
    }
    .sidebar-quick-contact .gform_fields input[type="text"] {
        height: 35px;
    }
    .sidebar-quick-contact .gform_heading h3 {
        font-size: 2em;
    }
    .sidebar-quick-contact .gform_heading span {
        font-size: 1em;
    }
}

/* HIDE "More Reviews" ON YELP PLUGIN */
.shortcode-yelp-reviews li.yelp-more-rv {display: none;}

    /* Hide Window Stickers */
    .windowStickerLink { display:none; }

/*Secondary CTA Styles*/
.vehicle .flex.flex-column.justify-between .flex.flex-wrap .w-50, .vehicle > div > .flex.flex-wrap > .w-50, .VehicleDetailsPage .eprice, .VehicleDetailsPage .theme-font-main.w-100.cc-container.cc-column.cc-nowrap.cc-justify-start.cc-align-center .w-100.pa2 .flex.flex-wrap div{
	width: 100%;
}
</style>

<!--[if lt IE 9]>
<script id="mfn-html5" src="https://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
<meta name="generator" content="Powered by Visual Composer - drag and drop page builder for WordPress."/>
<!--[if lte IE 9]><link rel="stylesheet" type="text/css" href="/content/plugins/js_composer/assets/css/vc_lte_ie9.min.css" media="screen"><![endif]-->    <link rel="amphtml" href="https://www.galpinpremier.com/inventory/amp/new-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA"/>
            <base href="/inventory/new-vehicles/" />
                    <script>
                (function() {

                    window.currentSrpBaseUrl = "/inventory/new-vehicles/";

                    // If we have a trailing "/" (because WordPress added it) in our URL,
                    // and we are not at the root, then we want to strip it and replaceState because it trips
                    // up the router
                    var path = window.location.pathname;
                    var hash = window.location.hash;

                    if (path !== window.currentSrpBaseUrl && path.slice(-1) === "/") {
                        history.replaceState({}, "", path.slice(0, -1));
                    }

                    // If we have an "old-school" hashed URL then we should convert it to replaceState
                    if (hash.substring(0, 2) === "#/") {
                        history.replaceState({}, "", window.currentSrpBaseUrl + hash.substring(2));
                    }

                })();
            </script>
                        <!-- SRP: SSR enabled -->
            <meta data-react-helmet="true" name="description" content="2019 Volvo XC40 Momentum - , - YV4162UK3K2134791"/><link data-react-helmet="true" rel="canonical" href="https://www.galpinpremier.com/inventory/all-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA"/><style data-react-helmet="true" >
.auto5-products .theme-primary,
.auto5-products .theme-primary-hover:hover,
.auto5-products *:hover > .theme-primary-parent-hover {
    color: #191919;
}
.auto5-products .bg-theme-primary,
.auto5-products .bg-theme-primary-hover:hover,
.auto5-products *:hover > .bg-theme-primary-parent-hover {
    background-color: #191919;
}
.auto5-products .b--theme-primary { border-color: #191919; }
 
.auto5-products .theme-secondary,
.auto5-products .theme-secondary-hover:hover,
.auto5-products *:hover > .theme-secondary-parent-hover {
    color: #bf9e57;
}
.auto5-products .bg-theme-secondary,
.auto5-products .bg-theme-secondary-hover:hover,
.auto5-products *:hover > .bg-theme-secondary-parent-hover {
    background-color: #bf9e57;
}
.auto5-products .b--theme-secondary { border-color: #bf9e57; }
 
.auto5-products .theme-icon,
.auto5-products .theme-icon-hover:hover,
.auto5-products *:hover > .theme-icon-parent-hover {
    color: #191919;
}
.auto5-products .bg-theme-icon,
.auto5-products .bg-theme-icon-hover:hover,
.auto5-products *:hover > .bg-theme-icon-parent-hover {
    background-color: #191919;
}
.auto5-products .b--theme-icon { border-color: #191919; }
 
.auto5-products .theme-disabled,
.auto5-products .theme-disabled-hover:hover,
.auto5-products *:hover > .theme-disabled-parent-hover {
    color: #dddddd;
}
.auto5-products .bg-theme-disabled,
.auto5-products .bg-theme-disabled-hover:hover,
.auto5-products *:hover > .bg-theme-disabled-parent-hover {
    background-color: #dddddd;
}
.auto5-products .b--theme-disabled { border-color: #dddddd; }
 
.auto5-products .theme-cta-primary,
.auto5-products .theme-cta-primary-hover:hover,
.auto5-products *:hover > .theme-cta-primary-parent-hover {
    color: #3399ff;
}
.auto5-products .bg-theme-cta-primary,
.auto5-products .bg-theme-cta-primary-hover:hover,
.auto5-products *:hover > .bg-theme-cta-primary-parent-hover {
    background-color: #3399ff;
}
.auto5-products .b--theme-cta-primary { border-color: #3399ff; }
 
.auto5-products .theme-cta-primary-text,
.auto5-products .theme-cta-primary-text-hover:hover,
.auto5-products *:hover > .theme-cta-primary-text-parent-hover {
    color: #FFFFFF;
}
.auto5-products .bg-theme-cta-primary-text,
.auto5-products .bg-theme-cta-primary-text-hover:hover,
.auto5-products *:hover > .bg-theme-cta-primary-text-parent-hover {
    background-color: #FFFFFF;
}
.auto5-products .b--theme-cta-primary-text { border-color: #FFFFFF; }
 
.auto5-products .theme-cta-secondary,
.auto5-products .theme-cta-secondary-hover:hover,
.auto5-products *:hover > .theme-cta-secondary-parent-hover {
    color: #191919;
}
.auto5-products .bg-theme-cta-secondary,
.auto5-products .bg-theme-cta-secondary-hover:hover,
.auto5-products *:hover > .bg-theme-cta-secondary-parent-hover {
    background-color: #191919;
}
.auto5-products .b--theme-cta-secondary { border-color: #191919; }
 
.auto5-products .theme-cta-secondary-text,
.auto5-products .theme-cta-secondary-text-hover:hover,
.auto5-products *:hover > .theme-cta-secondary-text-parent-hover {
    color: #FFFFFF;
}
.auto5-products .bg-theme-cta-secondary-text,
.auto5-products .bg-theme-cta-secondary-text-hover:hover,
.auto5-products *:hover > .bg-theme-cta-secondary-text-parent-hover {
    background-color: #FFFFFF;
}
.auto5-products .b--theme-cta-secondary-text { border-color: #FFFFFF; }
 
.auto5-products .theme-list,
.auto5-products .theme-list-hover:hover,
.auto5-products *:hover > .theme-list-parent-hover {
    color: #f5f5f5;
}
.auto5-products .bg-theme-list,
.auto5-products .bg-theme-list-hover:hover,
.auto5-products *:hover > .bg-theme-list-parent-hover {
    background-color: #f5f5f5;
}
.auto5-products .b--theme-list { border-color: #f5f5f5; }
 
.auto5-products .theme-list-item-primary,
.auto5-products .theme-list-item-primary-hover:hover,
.auto5-products *:hover > .theme-list-item-primary-parent-hover {
    color: #ffffff;
}
.auto5-products .bg-theme-list-item-primary,
.auto5-products .bg-theme-list-item-primary-hover:hover,
.auto5-products *:hover > .bg-theme-list-item-primary-parent-hover {
    background-color: #ffffff;
}
.auto5-products .b--theme-list-item-primary { border-color: #ffffff; }
 
.auto5-products .theme-list-item-secondary,
.auto5-products .theme-list-item-secondary-hover:hover,
.auto5-products *:hover > .theme-list-item-secondary-parent-hover {
    color: #ffffff;
}
.auto5-products .bg-theme-list-item-secondary,
.auto5-products .bg-theme-list-item-secondary-hover:hover,
.auto5-products *:hover > .bg-theme-list-item-secondary-parent-hover {
    background-color: #ffffff;
}
.auto5-products .b--theme-list-item-secondary { border-color: #ffffff; }
 
.auto5-products .theme-afh-text,
.auto5-products .theme-afh-text-hover:hover,
.auto5-products *:hover > .theme-afh-text-parent-hover {
    color: #000000;
}
.auto5-products .bg-theme-afh-text,
.auto5-products .bg-theme-afh-text-hover:hover,
.auto5-products *:hover > .bg-theme-afh-text-parent-hover {
    background-color: #000000;
}
.auto5-products .b--theme-afh-text { border-color: #000000; }
 
.auto5-products .theme-afh-background,
.auto5-products .theme-afh-background-hover:hover,
.auto5-products *:hover > .theme-afh-background-parent-hover {
    color: #f5f5f5;
}
.auto5-products .bg-theme-afh-background,
.auto5-products .bg-theme-afh-background-hover:hover,
.auto5-products *:hover > .bg-theme-afh-background-parent-hover {
    background-color: #f5f5f5;
}
.auto5-products .b--theme-afh-background { border-color: #f5f5f5; }
 
.auto5-products .theme-afh-icon,
.auto5-products .theme-afh-icon-hover:hover,
.auto5-products *:hover > .theme-afh-icon-parent-hover {
    color: #bf9e57;
}
.auto5-products .bg-theme-afh-icon,
.auto5-products .bg-theme-afh-icon-hover:hover,
.auto5-products *:hover > .bg-theme-afh-icon-parent-hover {
    background-color: #bf9e57;
}
.auto5-products .b--theme-afh-icon { border-color: #bf9e57; }
 
.auto5-products .theme-favorite,
.auto5-products .theme-favorite-hover:hover,
.auto5-products *:hover > .theme-favorite-parent-hover {
    color: #DBA709;
}
.auto5-products .bg-theme-favorite,
.auto5-products .bg-theme-favorite-hover:hover,
.auto5-products *:hover > .bg-theme-favorite-parent-hover {
    background-color: #DBA709;
}
.auto5-products .b--theme-favorite { border-color: #DBA709; }
</style><style data-react-helmet="true" >
.auto5-products .b--theme-cta-primary-border { border: 0px solid #000000; }
 
.auto5-products .b--theme-cta-secondary-border { border: 0px solid #000000; }
</style><meta name="generator" content="Powered by Slider Revolution 5.4.5.1 - responsive, Mobile-Friendly Slider Plugin for WordPress with comfortable drag and drop interface." />
<script type="text/javascript">function setREVStartSize(e){
				try{ var i=jQuery(window).width(),t=9999,r=0,n=0,l=0,f=0,s=0,h=0;					
					if(e.responsiveLevels&&(jQuery.each(e.responsiveLevels,function(e,f){f>i&&(t=r=f,l=e),i>f&&f>r&&(r=f,n=e)}),t>r&&(l=n)),f=e.gridheight[l]||e.gridheight[0]||e.gridheight,s=e.gridwidth[l]||e.gridwidth[0]||e.gridwidth,h=i/s,h=h>1?1:h,f=Math.round(h*f),"fullscreen"==e.sliderLayout){var u=(e.c.width(),jQuery(window).height());if(void 0!=e.fullScreenOffsetContainer){var c=e.fullScreenOffsetContainer.split(",");if (c) jQuery.each(c,function(e,i){u=jQuery(i).length>0?u-jQuery(i).outerHeight(!0):u}),e.fullScreenOffset.split("%").length>1&&void 0!=e.fullScreenOffset&&e.fullScreenOffset.length>0?u-=jQuery(window).height()*parseInt(e.fullScreenOffset,0)/100:void 0!=e.fullScreenOffset&&e.fullScreenOffset.length>0&&(u-=parseInt(e.fullScreenOffset,0))}f=u}else void 0!=e.minHeight&&f<e.minHeight&&(f=e.minHeight);e.c.closest(".rev_slider_wrapper").css({height:f})					
				}catch(d){console.log("Failure at Presize of Slider:"+d)}
			};</script>
<noscript><style type="text/css"> .wpb_animate_when_almost_visible { opacity: 1; }</style></noscript>	<style id="pum-styles" type="text/css" media="all">
	/* Popup Google Fonts */
@import url('//fonts.googleapis.com/css?family=Acme|Montserrat');

/* Popup Theme 1400: Framed Border */
.pum-theme-1400, .pum-theme-framed-border { background-color: rgba( 255, 255, 255, 0.50 ) } 
.pum-theme-1400 .pum-container, .pum-theme-framed-border .pum-container { padding: 18px; border-radius: 0px; border: 20px outset #dd3333; box-shadow: 1px 1px 3px 0px rgba( 2, 2, 2, 0.97 ) inset; background-color: rgba( 255, 251, 239, 1.00 ) } 
.pum-theme-1400 .pum-title, .pum-theme-framed-border .pum-title { color: #000000; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: inherit; font-size: 32px; line-height: 36px } 
.pum-theme-1400 .pum-content, .pum-theme-framed-border .pum-content { color: #2d2d2d; font-family: inherit } 
.pum-theme-1400 .pum-content + .pum-close, .pum-theme-framed-border .pum-content + .pum-close { height: 20px; width: 20px; left: auto; right: -20px; bottom: auto; top: -20px; padding: 0px; color: #ffffff; font-family: Acme; font-size: 20px; line-height: 20px; border: 1px none #ffffff; border-radius: 0px; box-shadow: 0px 0px 0px 0px rgba( 2, 2, 2, 0.23 ); text-shadow: 0px 0px 0px rgba( 0, 0, 0, 0.23 ); background-color: rgba( 0, 0, 0, 0.55 ) } 

/* Popup Theme 1399: Cutting Edge */
.pum-theme-1399, .pum-theme-cutting-edge { background-color: rgba( 0, 0, 0, 0.50 ) } 
.pum-theme-1399 .pum-container, .pum-theme-cutting-edge .pum-container { padding: 18px; border-radius: 0px; border: 1px none #000000; box-shadow: 0px 10px 25px 0px rgba( 2, 2, 2, 0.50 ); background-color: rgba( 30, 115, 190, 1.00 ) } 
.pum-theme-1399 .pum-title, .pum-theme-cutting-edge .pum-title { color: #ffffff; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: Sans-Serif; font-size: 26px; line-height: 28px } 
.pum-theme-1399 .pum-content, .pum-theme-cutting-edge .pum-content { color: #ffffff; font-family: inherit } 
.pum-theme-1399 .pum-content + .pum-close, .pum-theme-cutting-edge .pum-content + .pum-close { height: 24px; width: 24px; left: auto; right: 0px; bottom: auto; top: 0px; padding: 0px; color: #1e73be; font-family: inherit; font-size: 32px; line-height: 24px; border: 1px none #ffffff; border-radius: 0px; box-shadow: -1px 1px 1px 0px rgba( 2, 2, 2, 0.10 ); text-shadow: -1px 1px 1px rgba( 0, 0, 0, 0.10 ); background-color: rgba( 238, 238, 34, 1.00 ) } 

/* Popup Theme 1398: Hello Box */
.pum-theme-1398, .pum-theme-hello-box { background-color: rgba( 0, 0, 0, 0.75 ) } 
.pum-theme-1398 .pum-container, .pum-theme-hello-box .pum-container { padding: 30px; border-radius: 80px; border: 14px solid #81d742; box-shadow: 0px 0px 0px 0px rgba( 2, 2, 2, 0.00 ); background-color: rgba( 255, 255, 255, 1.00 ) } 
.pum-theme-1398 .pum-title, .pum-theme-hello-box .pum-title { color: #2d2d2d; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: Montserrat; font-size: 32px; line-height: 36px } 
.pum-theme-1398 .pum-content, .pum-theme-hello-box .pum-content { color: #2d2d2d; font-family: inherit } 
.pum-theme-1398 .pum-content + .pum-close, .pum-theme-hello-box .pum-content + .pum-close { height: auto; width: auto; left: auto; right: -30px; bottom: auto; top: -30px; padding: 0px; color: #2d2d2d; font-family: inherit; font-size: 32px; line-height: 28px; border: 1px none #ffffff; border-radius: 28px; box-shadow: 0px 0px 0px 0px rgba( 2, 2, 2, 0.23 ); text-shadow: 0px 0px 0px rgba( 0, 0, 0, 0.23 ); background-color: rgba( 255, 255, 255, 1.00 ) } 

/* Popup Theme 1397: Enterprise Blue */
.pum-theme-1397, .pum-theme-enterprise-blue { background-color: rgba( 0, 0, 0, 0.70 ) } 
.pum-theme-1397 .pum-container, .pum-theme-enterprise-blue .pum-container { padding: 28px; border-radius: 5px; border: 1px none #000000; box-shadow: 0px 10px 25px 4px rgba( 2, 2, 2, 0.50 ); background-color: rgba( 255, 255, 255, 1.00 ) } 
.pum-theme-1397 .pum-title, .pum-theme-enterprise-blue .pum-title { color: #315b7c; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: inherit; font-size: 34px; line-height: 36px } 
.pum-theme-1397 .pum-content, .pum-theme-enterprise-blue .pum-content { color: #2d2d2d; font-family: inherit } 
.pum-theme-1397 .pum-content + .pum-close, .pum-theme-enterprise-blue .pum-content + .pum-close { height: 28px; width: 28px; left: auto; right: 8px; bottom: auto; top: 8px; padding: 4px; color: #ffffff; font-family: inherit; font-size: 20px; line-height: 20px; border: 1px none #ffffff; border-radius: 42px; box-shadow: 0px 0px 0px 0px rgba( 2, 2, 2, 0.23 ); text-shadow: 0px 0px 0px rgba( 0, 0, 0, 0.23 ); background-color: rgba( 49, 91, 124, 1.00 ) } 

/* Popup Theme 1396: Light Box */
.pum-theme-1396, .pum-theme-lightbox { background-color: rgba( 0, 0, 0, 0.60 ) } 
.pum-theme-1396 .pum-container, .pum-theme-lightbox .pum-container { padding: 18px; border-radius: 3px; border: 8px solid #000000; box-shadow: 0px 0px 30px 0px rgba( 2, 2, 2, 1.00 ); background-color: rgba( 255, 255, 255, 1.00 ) } 
.pum-theme-1396 .pum-title, .pum-theme-lightbox .pum-title { color: #000000; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: inherit; font-size: 32px; line-height: 36px } 
.pum-theme-1396 .pum-content, .pum-theme-lightbox .pum-content { color: #000000; font-family: inherit } 
.pum-theme-1396 .pum-content + .pum-close, .pum-theme-lightbox .pum-content + .pum-close { height: 30px; width: 30px; left: auto; right: -24px; bottom: auto; top: -24px; padding: 0px; color: #ffffff; font-family: inherit; font-size: 24px; line-height: 26px; border: 2px solid #ffffff; border-radius: 30px; box-shadow: 0px 0px 15px 1px rgba( 2, 2, 2, 0.75 ); text-shadow: 0px 0px 0px rgba( 0, 0, 0, 0.23 ); background-color: rgba( 0, 0, 0, 1.00 ) } 

/* Popup Theme 1395: Default Theme */
.pum-theme-1395, .pum-theme-default-theme { background-color: rgba( 255, 255, 255, 1.00 ) } 
.pum-theme-1395 .pum-container, .pum-theme-default-theme .pum-container { padding: 18px; border-radius: 0px; border: 1px none #000000; box-shadow: 1px 1px 3px 0px rgba( 2, 2, 2, 0.23 ); background-color: rgba( 249, 249, 249, 1.00 ) } 
.pum-theme-1395 .pum-title, .pum-theme-default-theme .pum-title { color: #000000; text-align: left; text-shadow: 0px 0px 0px rgba( 2, 2, 2, 0.23 ); font-family: inherit; font-weight: inherit; font-size: 32px; font-style: normal; line-height: 36px } 
.pum-theme-1395 .pum-content, .pum-theme-default-theme .pum-content { color: #8c8c8c; font-family: inherit; font-weight: inherit; font-style: normal } 
.pum-theme-1395 .pum-content + .pum-close, .pum-theme-default-theme .pum-content + .pum-close { height: auto; width: auto; left: auto; right: 0px; bottom: auto; top: 0px; padding: 8px; color: #ffffff; font-family: inherit; font-weight: inherit; font-size: 12px; font-style: normal; line-height: 14px; border: 1px none #ffffff; border-radius: 0px; box-shadow: 0px 0px 0px 0px rgba( 2, 2, 2, 0.23 ); text-shadow: 0px 0px 0px rgba( 0, 0, 0, 0.23 ); background-color: rgba( 0, 183, 205, 1.00 ) } 


	
		</style></head>

<!-- body -->
<body class="jzla5p_srp-template-default single single-jzla5p_srp postid-7  color-default style-default button-default layout-full-width header-stack header-left header-fw minimalist-header sticky-header sticky-white ab-show subheader-title-left menuo-last mobile-tb-left mobile-mini-mr-ll be-204 wpb-js-composer js-comp-ver-5.2.1 vc_responsive">
	
	            <!-- Footer (Header): SSR enabled -->
                <!-- #jazel_mobile_header  -->
    <!-- skipjro --><div id="jazel_mobile_header"><div data-radium="true" data-reactroot="" data-reactid="1" data-react-checksum="905508937"><div data-radium="true" data-reactid="2"><style data-reactid="3">.jzl-a5-uibar-fixed-header {
                            background: rgba(51, 51, 51, 1)
                        }</style><div class="rmq-8cbd1fa5 jzl-a5-uibar-fixed-header jazel-a5-uibar-header    headerNotScrolling hide" style="background:rgba(51, 51, 51, 1);z-index:11;position:relative;top:0px;left:0px;width:100%;" data-radium="true" data-reactid="4"><div class="rmq-8cbd1fa5 jazel-a5-uibar-row-header-0 flex overflow-auto" style="z-index:5;background:transparent;color:#FFFFFF;" data-radium="true" data-reactid="5"><div class="flex" style="flex:1 1 0%;align-items:center;" data-reactid="6"><div id="jzl-button-0.24915409841180547" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:left;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:0ms;padding:10px 10px 0 10px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="7"><div data-radium="true" data-reactid="8"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="9">dehaze</i><div style="display:block;font-size:16px;" class="rmq-caa341b7" data-radium="true" data-reactid="10"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="11"><!-- react-text: 12 --> <!-- /react-text --><!-- react-text: 13 --><!-- /react-text --></span><style data-reactid="14">@media (maxWidth: 1024px){ .rmq-caa341b7{display: none !important;}}</style></div></div></div><div id="jazel-a5-header-site-title" style="-webkit-transition:0ms;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;font-weight:bold;min-width:20px;icon-font-size:32px;margin:10px 0 5px 4%;font-size:18px;text-align:center;transition:0ms;font-family:&quot;Catamaran&quot;, sans-serif;padding:5px 0;border:0px solid #FFFFFF;display:inline;vertical-align:middle;line-height:18px;" data-radium="true" data-reactid="15"><div style="display:inline;vertical-align:middle;" data-radium="true" data-reactid="16"><div style="display:inline;line-height:-webkit-calc(18px - 5px),-moz-calc(18px - 5px),calc(18px - 5px);" data-radium="true" data-reactid="17">GALPIN PREMIER</div><style data-reactid="18"></style></div></div></div><div class="flex" data-reactid="19"><div id="triggerGGChat" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:right;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0 10px 0 0;text-align:center;transition:0ms;padding:10px 0 0 10px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="20"><div data-radium="true" data-reactid="21"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="22">chat</i><div style="display:block;font-size:16px;" class="rmq-caa341b7" data-radium="true" data-reactid="23"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="24"><!-- react-text: 25 --> <!-- /react-text --><!-- react-text: 26 --><!-- /react-text --></span><style data-reactid="27">@media (maxWidth: 1024px){ .rmq-caa341b7{display: none !important;}}</style></div></div></div><div id="jzl-button-0.7266971960372082" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:right;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:0ms;padding:10px 12px 0 10px;width:55px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="28"><div data-radium="true" data-reactid="29"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="30">call</i><div style="display:block;font-size:16px;" data-radium="true" data-reactid="31"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="32"><!-- react-text: 33 --> <!-- /react-text --><!-- react-text: 34 --><!-- /react-text --></span><ul class="rmq-d0585693 jzl-a5-multiple-phone-number-ul" style="font-weight:normal;position:fixed;padding:0px;z-index:10;text-align:left;width:250px;background:#ffffff;list-style:none;font-size:12px;box-shadow:0 2px 2px 0 rgba(0,0,0,.14),0 3px 1px -2px rgba(0,0,0,.2),0 1px 5px 0 rgba(0,0,0,.12);border-radius:2px;font-family:Arial, Helvetica, sans-serif;margin-top:0px;right:100px;top:50px;display:none;" data-radium="true" data-reactid="35"><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8005647891" data-radium="true" data-reactid="36"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="37"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="38">Sales</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="39">(800) 564-7891</div></li></a><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8887059213" data-radium="true" data-reactid="40"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="41"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="42">Service</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="43">(888) 705-9213</div></li></a><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8887214839" data-radium="true" data-reactid="44"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="45"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="46">Parts</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="47">(888) 721-4839</div></li></a></ul><style data-reactid="48"></style></div></div></div><div id="google_translate_element_mobile_2" style="-webkit-transition:0ms;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:rgba(255, 255, 255, 1);float:right;flex:initial;icon-font-size:32px;line-height:28px;margin:0px;font-size:16px;text-align:center;transition:0ms;padding:22px 10px 8px;border:0px solid #FFFFFF;display:inline;vertical-align:middle;min-width:20px;" data-radium="true" data-reactid="49"><div style="display:inline;vertical-align:middle;" data-radium="true" data-reactid="50"><div style="display:inline;line-height:-webkit-calc(28px - 5px),-moz-calc(28px - 5px),calc(28px - 5px);" data-radium="true" data-reactid="51">Español</div><style data-reactid="52"></style></div></div></div></div></div><div class="rmq-8cbd1fa5 jzl-a5-ui-bar-hiding-header jazel-a5-uibar-header    headerNotScrolling hide" style="background:rgba(51, 51, 51, 1);z-index:10;position:fixed;left:0px;width:100%;" data-radium="true" data-reactid="53"><div class="rmq-8cbd1fa5 jazel-a5-uibar-row-header-0 flex overflow-auto" style="z-index:5;background:transparent;color:#FFFFFF;" data-radium="true" data-reactid="54"><div class="flex" style="flex:1 1 0%;align-items:center;" data-reactid="55"><div id="jzl-button-0.24915409841180547" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:left;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:0ms;padding:10px 10px 0 10px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="56"><div data-radium="true" data-reactid="57"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="58">dehaze</i><div style="display:block;font-size:16px;" class="rmq-caa341b7" data-radium="true" data-reactid="59"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="60"><!-- react-text: 61 --> <!-- /react-text --><!-- react-text: 62 --><!-- /react-text --></span><style data-reactid="63">@media (maxWidth: 1024px){ .rmq-caa341b7{display: none !important;}}</style></div></div></div><div id="jazel-a5-header-site-title" style="-webkit-transition:0ms;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;font-weight:bold;min-width:20px;icon-font-size:32px;margin:10px 0 5px 4%;font-size:18px;text-align:center;transition:0ms;font-family:&quot;Catamaran&quot;, sans-serif;padding:5px 0;border:0px solid #FFFFFF;display:inline;vertical-align:middle;line-height:18px;" data-radium="true" data-reactid="64"><div style="display:inline;vertical-align:middle;" data-radium="true" data-reactid="65"><div style="display:inline;line-height:-webkit-calc(18px - 5px),-moz-calc(18px - 5px),calc(18px - 5px);" data-radium="true" data-reactid="66">GALPIN PREMIER</div><style data-reactid="67"></style></div></div></div><div class="flex" data-reactid="68"><div id="triggerGGChat" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:right;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0 10px 0 0;text-align:center;transition:0ms;padding:10px 0 0 10px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="69"><div data-radium="true" data-reactid="70"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="71">chat</i><div style="display:block;font-size:16px;" class="rmq-caa341b7" data-radium="true" data-reactid="72"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="73"><!-- react-text: 74 --> <!-- /react-text --><!-- react-text: 75 --><!-- /react-text --></span><style data-reactid="76">@media (maxWidth: 1024px){ .rmq-caa341b7{display: none !important;}}</style></div></div></div><div id="jzl-button-0.7266971960372082" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:0ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:right;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:0ms;padding:10px 12px 0 10px;width:55px;border:0px solid #FFFFFF;align-items:center;justify-content:center;icon-font-size:32px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:16px;" data-radium="true" data-reactid="77"><div data-radium="true" data-reactid="78"><i style="font-family:Material Icons;font-style:normal;font-size:32px;" class="notranslate material-icons" data-radium="true" data-reactid="79">call</i><div style="display:block;font-size:16px;" data-radium="true" data-reactid="80"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="81"><!-- react-text: 82 --> <!-- /react-text --><!-- react-text: 83 --><!-- /react-text --></span><ul class="rmq-d0585693 jzl-a5-multiple-phone-number-ul" style="font-weight:normal;position:fixed;padding:0px;z-index:10;text-align:left;width:250px;background:#ffffff;list-style:none;font-size:12px;box-shadow:0 2px 2px 0 rgba(0,0,0,.14),0 3px 1px -2px rgba(0,0,0,.2),0 1px 5px 0 rgba(0,0,0,.12);border-radius:2px;font-family:Arial, Helvetica, sans-serif;margin-top:0px;right:100px;top:50px;display:none;" data-radium="true" data-reactid="84"><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8005647891" data-radium="true" data-reactid="85"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="86"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="87">Sales</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="88">(800) 564-7891</div></li></a><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8887059213" data-radium="true" data-reactid="89"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="90"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="91">Service</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="92">(888) 705-9213</div></li></a><a class="jzl-a5-phone-number-dropdown-anchor" style="float:left;width:100%;overflow:auto;color:black;text-decoration:none;" href="tel:8887214839" data-radium="true" data-reactid="93"><li class="jzl-a5-phone-number-dropdown-entry" style="display:block;text-decoration:none;color:#9e9e9e;padding:10px 20px;overflow:auto;" data-radium="true" data-reactid="94"><div class="jzl-a5-phone-number-department-name" style="float:left;" data-radium="true" data-reactid="95">Parts</div><div class="jzl-a5-phone-number-department-number" style="float:right;" data-radium="true" data-reactid="96">(888) 721-4839</div></li></a></ul><style data-reactid="97"></style></div></div></div><div id="google_translate_element_mobile_2" style="-webkit-transition:0ms;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:rgba(255, 255, 255, 1);float:right;flex:initial;icon-font-size:32px;line-height:28px;margin:0px;font-size:16px;text-align:center;transition:0ms;padding:22px 10px 8px;border:0px solid #FFFFFF;display:inline;vertical-align:middle;min-width:20px;" data-radium="true" data-reactid="98"><div style="display:inline;vertical-align:middle;" data-radium="true" data-reactid="99"><div style="display:inline;line-height:-webkit-calc(28px - 5px),-moz-calc(28px - 5px),calc(28px - 5px);" data-radium="true" data-reactid="100">Español</div><style data-reactid="101"></style></div></div></div></div></div></div><style data-reactid="102">@media (min-width: 1025px){ .rmq-8cbd1fa5{display: none !important;}}
@media (max-width: 350px){ .rmq-d0585693{left: 0 !important;
right: auto !important;}}</style></div></div><!-- /skipjro -->
    <!-- mfn_hook_top --><script>
    function load_autoid() {
        var s = document.getElementsByTagName('script')[0],
        	p = document.createElement('script');
        p.src = '//ai.autoid.com/ai.js';
        s.parentNode.insertBefore(p, s);
    };

    function load_gtm(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
	    new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
	    j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';
	    j.async=true;
	    j.src='https://www.googletagmanager.com/gtm.js?id='+i+dl;
	    f.parentNode.insertBefore(j,f);
    }


    if (window.addEventListener) { 
        window.addEventListener("load", load_autoid, false);
        window.addEventListener("load", function() { return load_gtm(window,document,'script','dataLayer','GTM-W66M3C'); }, false); 
    } else if (window.attachEvent) { 
        window.attachEvent("onload", load_autoid);
        window.attachEvent("onload",function() { return load_gtm(window,document,'script','dataLayer','GTM-W66M3C'); }); 
    } else {
        load_autoid();
        load_prum();
        load_gtm(window,document,'script','dataLayer','GTM-W66M3C');
    }
</script>
<!-- Google Tag Manager (noscript) -->
<noscript>
    <iframe src="https://www.googletagmanager.com/ns.html?id=GTM-W66M3C"height="0" width="0" style="display:none;visibility:hidden"></iframe>
</noscript>
<!-- End Google Tag Manager (noscript) --><!-- mfn_hook_top -->
		
		
	<!-- #Wrapper -->
	<div id="Wrapper">
	
				
		
		<!-- #Header_bg -->
		<div id="Header_wrapper" >
	
			<!-- #Header -->
			<header id="Header">
				
	<div id="Action_bar">
		<div class="container">
			<div class="column one">

				<ul class="contact_details">
					<li><div class="textwidget"><a href="/hours-directions/" class="button">HOURS & DIRECTIONS</a></div></li><li><div class="textwidget"><div class="hide-for-small" style="text-align: right;">
<span class="translation-links"><a class="arrow-after" href="#" data-lang="Spanish" style="color:#c7c7c7;" title="Translated by Google">Español</a>
<!-- Code provided by Google -->
<div id="google_translate_element" style="width:0px;height:0;margin:0;overflow:hidden;"></div>
<script type="text/javascript">
  function googleTranslateElementInit() {
    new google.translate.TranslateElement({pageLanguage: 'en', includedLanguages: 'es', layout: google.translate.TranslateElement.InlineLayout.SIMPLE, autoDisplay: false}, 'google_translate_element');
  }
</script>
<script src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit" type="text/javascript"></script>

<!-- Flag click handler -->
<script type="text/javascript">
    jQuery('.translation-links a').click(function() {
      var lang = jQuery(this).data('lang');
      var $frame = jQuery('.goog-te-menu-frame:first');
      if (!$frame.size()) {
        alert("Error: Could not find Google translate frame.");
        return false;
      }
      jQuery('.goog-te-menu-frame:first').contents().find('.goog-te-menu2-item span.text').each(function(){ if( jQuery(this).html() == lang ) jQuery(this).click(); });
      return false;
    });
</script></div></li>				</ul>

			</div>
		</div>
	</div>


<!-- .header_placeholder 4sticky  -->
<div class="header_placeholder"></div>

<div id="Top_bar" class="loading">

	<div class="container">
		<div class="column one">
		
			<div class="top_bar_left clearfix">
			
                <div class='branding'>
                
                                            
                    <!-- .logo -->
                    <div class="logo text-logo header-partial partial-first">
                    
                        <!-- Header Content 1 -->                    
                        <div class="column one-third header_content header_content_1"><div><div class="textwidget"><div style="color:#fff;float:right;line-height:normal;margin:0 0 0 19px;" class="header-numbers">
    <div><span class="label">SALES</span><span class="value"><a href="tel:(800) 564-7891">(800) 564-7891</a></span></div>
    <div><span class="label">SERVICE</span><span class="value"><a href="tel:(800) 564-7891">(888) 705-9213</a></span></div>
</div></div></div></div>                 
                    
                        <div class="column one-third logo_column">
                        <a id="logo" href="https://www.galpinpremier.com" title="Galpin Premier"><img class="logo-main   scale-with-grid" src="/content/themes/betheme/images/logo/logo.png" 	alt="Galpin Premier" /><img class="logo-sticky scale-with-grid" src="/content/themes/betheme/images/logo/logo.png" alt="" /><img class="logo-mobile scale-with-grid" src="/content/themes/betheme/images/logo/logo.png" alt="" /><span><em>GALPIN</em> PREMIER</span></a>                        </div>
                        
                        <!-- Header Content 2 -->                    
                                         
                        
                    </div>
                </div>
			
				<div class="menu_wrapper">
					<nav id="menu" class="menu-main-menu-container"><ul id="menu-main-menu" class="menu"><li id="menu-item-1549" class="nav-home menu-item menu-item-type-custom menu-item-object-custom"><a href="/"><span>Home</span></a></li>
<li id="menu-item-11" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children"><a href="/inventory/new-vehicles/"><span>New Cars</span></a>
<ul class="sub-menu">
	<li id="menu-item-1602" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/"><span>All Premier Collection</span></a></li>
	<li id="menu-item-2305" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/keep-it-new/"><span>Keep It New Program</span></a></li>
	<li id="menu-item-1603" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/models=Lincoln"><span>All Lincoln Vehicles</span></a></li>
	<li id="menu-item-1604" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/models=Volvo"><span>All Volvo Vehicles</span></a></li>
	<li id="menu-item-1605" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/models=Jaguar"><span>All Jaguar Vehicles</span></a></li>
	<li id="menu-item-1607" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/models=Lotus"><span>All Lotus Vehicles</span></a></li>
	<li id="menu-item-1606" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/new-vehicles/models=Aston%20Martin"><span>All Aston Martin Vehicles</span></a></li>
</ul>
</li>
<li id="menu-item-12" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children"><a href="/used-car-center/"><span>Used Cars</span></a>
<ul class="sub-menu">
	<li id="menu-item-1597" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/used-luxury/"><span>Luxury Pre-Owned</span></a></li>
	<li id="menu-item-1709" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/certified-pre-owned/"><span>Certified Luxury Vehicles</span></a></li>
	<li id="menu-item-1598" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/used-vehicles/models=Aston%20Martin"><span>Pre-Owned Aston Martin</span></a></li>
	<li id="menu-item-1599" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/used-vehicles/models=Jaguar"><span>Pre-Owned Jaguar</span></a></li>
	<li id="menu-item-1601" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/used-vehicles/models=Lincoln"><span>Pre-Owned Lincoln</span></a></li>
	<li id="menu-item-1600" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/inventory/used-vehicles/models=Volvo"><span>Pre-Owned Volvo</span></a></li>
	<li id="menu-item-1596" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/galpin-used-car-difference/"><span>Galpin Used Car Difference</span></a></li>
</ul>
</li>
<li id="menu-item-18" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children"><a href="/specials/"><span>Specials</span></a>
<ul class="sub-menu">
	<li id="menu-item-2304" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/keep-it-new/"><span>Keep It New Program</span></a></li>
	<li id="menu-item-1587" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://www.galpinastonmartin.com/new-specials/"><span>Aston Martin Specials</span></a></li>
	<li id="menu-item-1588" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://www.galpinjaguar.com/new-specials/"><span>Jaguar Specials</span></a></li>
	<li id="menu-item-1589" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://www.galpinlincoln.com/new-specials/"><span>Lincoln Specials</span></a></li>
	<li id="menu-item-1590" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://www.galpinlotus.com/specials"><span>Lotus Specials</span></a></li>
	<li id="menu-item-1591" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://www.galpinvolvo.com/new-specials/"><span>Volvo Specials</span></a></li>
	<li id="menu-item-1698" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/service-specials/"><span>Service Specials</span></a></li>
	<li id="menu-item-2395" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/rplate/"><span>Digital License Plate</span></a></li>
</ul>
</li>
<li id="menu-item-59" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children"><a href="https://www.galpinpremier.com/finance-center/"><span>Finance</span></a>
<ul class="sub-menu">
	<li id="menu-item-58" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/finance-center/"><span>Finance Hours</span></a></li>
	<li id="menu-item-57" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/finance/"><span>Apply Online</span></a></li>
	<li id="menu-item-1710" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/leasing/"><span>Leasing at Galpin</span></a></li>
	<li id="menu-item-56" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/payment-calculators/"><span>Estimate Payments</span></a></li>
	<li id="menu-item-2243" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/value-your-trade/"><span>Value Your Trade</span></a></li>
</ul>
</li>
<li id="menu-item-33" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children"><a href="https://www.galpinpremier.com/service-center/"><span>Service &#038; Parts</span></a>
<ul class="sub-menu">
	<li id="menu-item-2405" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/service-specials/"><span>Service Specials</span></a></li>
	<li id="menu-item-37" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/service-center/"><span>Service Hours</span></a></li>
	<li id="menu-item-36" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/schedule-service/"><span>Schedule Service</span></a></li>
	<li id="menu-item-35" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/parts-center/"><span>Parts Hours</span></a></li>
	<li id="menu-item-1586" class="menu-item menu-item-type-custom menu-item-object-custom"><a target="_blank" href="http://galpinautosports.com/"><span>Galpin Auto Sports</span></a></li>
	<li id="menu-item-2394" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/rplate/"><span>Digital License Plate</span></a></li>
</ul>
</li>
<li id="menu-item-1712" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children"><a href="/about-us/"><span>About Galpin</span></a>
<ul class="sub-menu">
	<li id="menu-item-64" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/hours-directions/"><span>Hours &#038; Directions</span></a></li>
	<li id="menu-item-1583" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/mission-statement-core-values/"><span>Galpin Mission &#038; Values</span></a></li>
	<li id="menu-item-1711" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/about-us/"><span>Galpin History</span></a></li>
	<li id="menu-item-1579" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/employment-opportunities/"><span>Join Our Team</span></a></li>
	<li id="menu-item-2103" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/newsroom/"><span>Galpin News &#038; Events</span></a></li>
	<li id="menu-item-1581" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/galpin-horseless-carriage-restaurant/"><span>Horseless Carriage Restaurant</span></a></li>
	<li id="menu-item-1580" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/starbucks/"><span>Starbucks at Galpin</span></a></li>
	<li id="menu-item-1585" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="http://www.galpinastonmartin.com/club-aston"><span>Galpin&#8217;s Club Aston</span></a></li>
	<li id="menu-item-2741" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/california-supply-chains-act/"><span>California Supply Chains Act</span></a></li>
	<li id="menu-item-60" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://www.galpinpremier.com/contact-us/"><span>Contact Us</span></a></li>
</ul>
</li>
<li id="menu-item-2682" class="menu-item menu-item-type-custom menu-item-object-custom"><a href="/employment-opportunities/"><span>Employment</span></a></li>
<li id="menu-item-1713" class="highlight-item menu-item menu-item-type-custom menu-item-object-custom"><a href="/why-galpin/"><span>Why Go Galpin</span></a></li>
</ul></nav>					
				</div>
                
                				
				<div class="secondary_menu_wrapper">
					<!-- #secondary-menu -->
									</div>
				
				<div class="banner_wrapper">
									</div>
				
                				
			</div>
			
						
		</div>
	</div>
</div>

<!-- Below Header -->
	
							</header>
				
					
		</div>
		
				
		<!-- mfn_hook_content_before --><!-- mfn_hook_content_before -->
    <!-- #Content -->
    <div id="Content">
        <div class="content_wrapper clearfix">

            <!-- .sections_group -->
            <div class="sections_group">
                
<div id="rev_slider_5_1_wrapper" class="rev_slider_wrapper fullwidthbanner-container" data-source="gallery" style="margin:0px auto;background:transparent;padding:0px;margin-top:0px;margin-bottom:0px;">
<!-- START REVOLUTION SLIDER 5.4.5.1 fullwidth mode -->
	<div id="rev_slider_5_1" class="rev_slider fullwidthabanner" style="display:none;" data-version="5.4.5.1">
<ul>	<!-- SLIDE  -->
	<li data-index="rs-12" data-transition="fade" data-slotamount="default" data-hideafterloop="0" data-hideslideonmobile="off"  data-easein="default" data-easeout="default" data-masterspeed="300"  data-link="https://www.galpinpremier.com/specials/"   data-rotate="0"  data-saveperformance="off"  data-title="Mem- 1000 + KIN" data-param1="" data-param2="" data-param3="" data-param4="" data-param5="" data-param6="" data-param7="" data-param8="" data-param9="" data-param10="" data-description="">
		<!-- MAIN IMAGE -->
		<img src="https://images.jazelc.com/uploads/galpinpremier/PREMIER_MemDay19_FD_1000_SRP_3360x504_C1_C1.jpg"  alt="" title="PREMIER_MemDay19_FD_1000_SRP_3360x504_C1_C1"  width="3360" height="504" data-bgposition="center center" data-bgfit="cover" data-bgrepeat="no-repeat" class="rev-slidebg" data-no-retina>
		<!-- LAYERS -->
	</li>
</ul>
<div class="tp-bannertimer tp-bottom" style="visibility: hidden !important;"></div>	</div>
<script>var htmlDiv = document.getElementById("rs-plugin-settings-inline-css"); var htmlDivCss="";
				if(htmlDiv) {
					htmlDiv.innerHTML = htmlDiv.innerHTML + htmlDivCss;
				}else{
					var htmlDiv = document.createElement("div");
					htmlDiv.innerHTML = "<style>" + htmlDivCss + "</style>";
					document.getElementsByTagName("head")[0].appendChild(htmlDiv.childNodes[0]);
				}
			</script>
		<script type="text/javascript">
setREVStartSize({c: jQuery('#rev_slider_5_1'), responsiveLevels: [1240,1024,778,480], gridwidth: [1920,1040,768,480], gridheight: [288,156,117,72], sliderLayout: 'fullwidth'});
			
var revapi5,
	tpj=jQuery;
			
tpj(document).ready(function() {
	if(tpj("#rev_slider_5_1").revolution == undefined){
		revslider_showDoubleJqueryError("#rev_slider_5_1");
	}else{
		revapi5 = tpj("#rev_slider_5_1").show().revolution({
			sliderType:"standard",
			jsFileLocation:"//www.galpinpremier.com/content/plugins/revslider2/public/assets/js/",
			sliderLayout:"fullwidth",
			dottedOverlay:"none",
			delay:9000,
			navigation: {
				onHoverStop:"off",
			},
			responsiveLevels:[1240,1024,778,480],
			visibilityLevels:[1240,1024,778,480],
			gridwidth:[1920,1040,768,480],
			gridheight:[288,156,117,72],
			lazyType:"none",
			shadow:0,
			spinner:"spinner0",
			stopLoop:"off",
			stopAfterLoops:-1,
			stopAtSlide:-1,
			shuffle:"off",
			autoHeight:"on",
			disableProgressBar:"on",
			hideThumbsOnMobile:"off",
			hideSliderAtLimit:0,
			hideCaptionAtLimit:0,
			hideAllCaptionAtLilmit:0,
			debugMode:false,
			fallbacks: {
				simplifyAll:"off",
				nextSlideOnWindowFocus:"off",
				disableFocusListener:false,
			}
		});
	}
	
});	/*ready*/
</script>
		</div><!-- END REVOLUTION SLIDER -->
<div class="new_srp_banner">
    <div><img src="https://images.jazelc.com/uploads/galpinpremier/warranty_badge.png" alt="Galpin Motors" style="opacity:0.16;margin:-11% 0 0;visibility:hidden;" /></div>
    <div class="banner-title" style="text-align:left;color:#bf9e57;font-weight:900;">Why Go Galpin</div>
    <div>
        <div>
            <div><img src="https://images.jazelc.com/uploads/galpinpremier/icon_family_black.png" alt="Customers are our #1 Priority" /></div>
            <div><span class="hide-for-small">Customers<br/>are #1 Priority</span><span class="show-for-small">Customers<br/>are #1</span></div>
        </div>
        <div>
            <div><img src="https://images.jazelc.com/uploads/galpinpremier/icon_credit_black.png" alt="Easy Financing for Every One" /></div>
            <div><span class="hide-for-small">Easy Financing<br/>for Every One</span><span class="show-for-small">Easy<br/>Financing</span></div>
        </div>
        <div>
            <div><img src="https://images.jazelc.com/uploads/galpinpremier/icon_inv_black.png" alt="Used Car Inventory" style="max-height: none;"/></div>
            <div><span class="hide-for-small">Huge Selection<br/>of Luxury Vehicles</span><span class="show-for-small">Huge<br/>Selection</span></div>
        </div>
        <div>
            <div><img src="https://images.jazelc.com/uploads/galpinpremier/icon_handshake_black.png" alt="Knowledgeable & Friendly Sales Staff" /></div>
            <div><span class="hide-for-small">Knowledgable &<br/>Friendly Sales Staff</span><span class="show-for-small">Friendly<br/>Staff</span></div>
        </div>
        <div>
            <div><img src="https://images.jazelc.com/uploads/galpinpremier/icon_rights_black.png" alt="Customer Bill of Rights" /></div>
            <div><span class="hide-for-small">Customer<br/>Bill of Rights</span><span class="show-for-small">Customer<br/>Bill of Rights</span></div>
        </div>
    </div>
</div>
<div class="new_srp_banner-mobile" style="text-align:center;">
</div>
<h1 class="srp_h1">New Inventory</h1>
        <!-- skipjro --><div id="srp-app"><div data-reactroot="" data-reactid="1" data-react-checksum="627345384"><div class="srp-app-container auto5-products cb" data-reactid="2"><!-- react-empty: 3 --><div class="flex" data-reactid="4"><div class="w-100" data-reactid="5"><div class="VehicleDetailsPage" data-reactid="6"><div style="display:none;" data-reactid="7"><div class="pa2 flex text-search" style="color:rgba(0, 0, 0, 0.87);background-color:#ffffff;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;box-sizing:border-box;font-family:Arial, Helvetica, sans-serif;-webkit-tap-highlight-color:rgba(0,0,0,0);box-shadow:0 3px 10px rgba(0, 0, 0, 0.16),
         0 3px 10px rgba(0, 0, 0, 0.23);border-radius:2px;" data-reactid="8"><svg class="f3 ma1 ml2 theme-primary" style="display:inline-block;fill:currentColor;height:24px;width:24px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;" viewBox="0 0 512 512" data-reactid="9"><path d="m440 368l-83-77c10-22 15-45 15-70 0-91-73-164-164-164-90 0-164 73-164 164 0 91 74 164 164 164 37 0 70-12 97-32l81 74c16 15 42 14 57-2 7-8 11-18 11-28-1-11-5-22-14-29z m-232-28c-66 0-119-53-119-119 0-66 53-119 119-119 66 0 119 53 119 119 0 66-53 119-119 119z" data-reactid="10"></path></svg><div class="flex-grow1" data-reactid="11"><input type="search" class="input-reset no-outline no-border-color no-box-shadow h2 pv2 f5 bn br2 bg-transparent w-100" placeholder="Search for vehicle (e.g. Black 2017 Coupe)" value="" autocomplete="off" autocorrect="off" autocapitalize="off" spellcheck="false" data-reactid="12"/></div></div></div><!-- react-empty: 13 --><div class="theme-font-main w-100 cc-container cc-column cc-nowrap cc-justify-start cc-align-start" data-reactid="14"><div class="w-100 w-100 pv2 bg-white bb b--linkwater" data-reactid="15"><div class="w-100 flex flex-row items-center" data-reactid="16"><a href="#" class="w-15-over-16 flex flex-row items-center center" style="margin:auto;" data-reactid="17"><svg style="display:inline-block;color:rgba(0, 0, 0, 0.87);fill:currentColor;height:24px;width:24px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;" viewBox="0 0 24 24" data-reactid="18"><path d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z" data-reactid="19"></path></svg><!-- react-text: 20 --> Back to Search Results<!-- /react-text --></a></div></div><div class="w-100 overflow-hidden bg-gray98 cc-container cc-column cc-nowrap cc-justify-start cc-align-start" data-reactid="21"><div class="w-15-over-16 ci-align-self-center cc-container cc-row cc-nowrap cc-justify-start cc-align-start" data-reactid="22"><div class="w-100" data-reactid="23"><div class="f2_5rem b pv2 overflow-hidden vehicleTitle vehicle-title" data-reactid="24"><div class="w-100 fl" data-reactid="25"><h1 class="" itemprop="name" data-reactid="26"><span itemProp="year">2019</span> <span itemProp="manufacturer" class="notranslate">Volvo</span> <span itemProp="model" class="notranslate">XC40</span> <span class="notranslate">Momentum</span></h1></div></div></div></div><div class="w-15-over-16 overflow-hidden ci-align-self-center cc-container cc-row cc-nowrap cc-justify-space-between cc-align-start" data-reactid="27"><div class="w-50 ci-non-shrinkable cc-container cc-column cc-nowrap cc-justify-start cc-align-start" data-reactid="28"><div class="w-100 overflow-hidden" data-reactid="29"><section id="image-gallery" class="image-gallery" aria-live="polite" data-reactid="30"><div class="image-gallery-content" data-reactid="31"><div class="image-gallery-slide-wrapper bottom" data-reactid="32"><div class="image-gallery-fullscreen-button" data-reactid="33"></div><span data-reactid="34"><div class="image-gallery-left-nav" disabled="" data-reactid="35"></div><div class="image-gallery-right-nav" data-reactid="36"></div></span><div class="image-gallery-swipe" data-reactid="37"><div class="image-gallery-slides" data-reactid="38"><div class="image-gallery-slide center" style="-webkit-transform:translate3d(0%, 0, 0);-moz-transform:translate3d(0%, 0, 0);-ms-transform:translate3d(0%, 0, 0);-o-transform:translate3d(0%, 0, 0);transform:translate3d(0%, 0, 0);z-index:3;" data-reactid="39"><div class="image-gallery-image" data-reactid="40"><img src="//media-cdn.jazelc.com/media/38229186" data-reactid="41"/></div></div><div class="image-gallery-slide right" style="-webkit-transform:translate3d(100%, 0, 0);-moz-transform:translate3d(100%, 0, 0);-ms-transform:translate3d(100%, 0, 0);-o-transform:translate3d(100%, 0, 0);transform:translate3d(100%, 0, 0);z-index:1;" data-reactid="42"><div class="image-gallery-image" data-reactid="43"><img src="//media-cdn.jazelc.com/media/38229187" data-reactid="44"/></div></div><div class="image-gallery-slide" style="-webkit-transform:translate3d(200%, 0, 0);-moz-transform:translate3d(200%, 0, 0);-ms-transform:translate3d(200%, 0, 0);-o-transform:translate3d(200%, 0, 0);transform:translate3d(200%, 0, 0);z-index:1;" data-reactid="45"><div style="height:100%;" data-reactid="46"></div></div><div class="image-gallery-slide" style="-webkit-transform:translate3d(300%, 0, 0);-moz-transform:translate3d(300%, 0, 0);-ms-transform:translate3d(300%, 0, 0);-o-transform:translate3d(300%, 0, 0);transform:translate3d(300%, 0, 0);z-index:0;" data-reactid="47"><div style="height:100%;" data-reactid="48"></div></div></div></div><div class="image-gallery-index" data-reactid="49"><span class="image-gallery-index-current" data-reactid="50">1</span><span class="image-gallery-index-separator" data-reactid="51"> / </span><span class="image-gallery-index-total" data-reactid="52">4</span></div></div><div class="image-gallery-thumbnails-wrapper image-gallery-thumbnails-wrapper__single-line bottom" style="text-align:center;" data-reactid="53"><div class="image-gallery-thumbnails" data-reactid="54"><div class="image-gallery-thumbnails-container" style="-webkit-transform:translate3d(0px, 0, 0);-moz-transform:translate3d(0px, 0, 0);-ms-transform:translate3d(0px, 0, 0);-o-transform:translate3d(0px, 0, 0);transform:translate3d(0px, 0, 0);" role="navigation" aria-label="Thumbnail Navigation" data-reactid="55"><a role="button" aria-pressed="true" aria-label="Go to Slide 1" class="image-gallery-thumbnail active" data-reactid="56"><img src="//media-cdn.jazelc.com/media/38229186?scale=100/-1/50" data-reactid="57"/><div class="image-gallery-thumbnail-label" data-reactid="58"></div></a><a role="button" aria-pressed="false" aria-label="Go to Slide 2" class="image-gallery-thumbnail" data-reactid="59"><img src="" data-reactid="60"/><div class="image-gallery-thumbnail-label" data-reactid="61"></div></a><a role="button" aria-pressed="false" aria-label="Go to Slide 3" class="image-gallery-thumbnail" data-reactid="62"><img src="" data-reactid="63"/><div class="image-gallery-thumbnail-label" data-reactid="64"></div></a><a role="button" aria-pressed="false" aria-label="Go to Slide 4" class="image-gallery-thumbnail" data-reactid="65"><img src="" data-reactid="66"/><div class="image-gallery-thumbnail-label" data-reactid="67"></div></a></div></div><div class="image-gallery-featured-thumbnails" style="height:auto;" data-reactid="68"></div></div></div></section><div class="w-100 pa2" data-reactid="69"><div class="dib w-100 w-50-ns pa1" data-reactid="70"><div class="dib w1_5 h1_5 v-mid mr2 ba fl br0" style="background-color:#ffffff;" data-reactid="71"></div><div class="fl db f6 pa1 pr2" data-reactid="72"><span class="di f6 pl2" itemprop="color" data-reactid="73">Ice White</span><span class="di f6 b fl" data-reactid="74">Exterior</span></div></div><div class="dib w-100 w-50-ns pa1" data-reactid="75"><div class="dib w1_5 h1_5 v-mid mr2 ba fl br0" style="background-color:white;" data-reactid="76"></div><div class="fl db f6 pa1 pr2" data-reactid="77"><span class="di f6 pl2" itemprop="color" data-reactid="78">Charcoal</span><span class="di f6 b fl" data-reactid="79">Interior</span></div></div></div></div><div class="w-100" data-reactid="80"></div></div><div class="w-50 ml3 mr3 ci-growable cc-container cc-column cc-nowrap cc-justify-start cc-align-center" data-reactid="81"><div class="w-100 cc-container cc-column" data-reactid="82"><div class="w-100 pa3 bg-grey-100 f1_125rem" data-reactid="83"><div class="vehiclePricing" style="font-size:18px;line-height:1.5;" data-reactid="84"><div style="font-weight:bold;" class="pricing_0 row" data-reactid="85"><div style="display:inline-block;line-height:1;width:65%;" class="pricing_label_0 label" data-reactid="86"><!-- react-text: 87 -->MSRP<!-- /react-text --></div><div style="display:inline-block;line-height:1;width:35%;text-align:right;" class="pricing_value_0 value" data-reactid="88">$37,795</div></div></div></div></div><div class="w-100 mt3 flex justify-end" data-reactid="89"><div class="flex flex-wrap w-40" data-reactid="90"><div class="w-100 eprice" data-reactid="91"><div class="eprice f4 ma1 pa1 br2 tr pointer" data-reactid="92"><img src="https://images.jazelc.com/uploads/galpinpremier/Galpin-e-Price.png" title="Get E-Price" data-reactid="93"/></div></div><div class="w-50 eprice" data-reactid="94"><div class="eprice f4 ma1 pa1 br2 tr pointer" data-reactid="95"><img src="https://images.jazelc.com/uploads/galpinpremier/ValueYourTrade-CTA-Smaller.png" title="Value Your Trade" data-reactid="96"/></div></div></div></div><div class="w-100" data-reactid="97"></div><div class="w-100 mt3 cc-container cc-row cc-nowrap cc-justify-space-between cc-align-stretch" data-reactid="98"><!-- react-empty: 99 --><!-- react-empty: 100 --></div><div class="w-100 mt3 pa3 bg-grey-100" data-reactid="101"><div class="cc2 f6" data-reactid="102"><div class="trigger pv1" title="23/31 (City/Hwy)" data-reactid="103"><span class="dib b w6rem" data-reactid="104"><span data-reactid="105">MPG</span><span class="" data-reactid="106">: </span></span><span class="" itemprop="fuelEfficiency" data-reactid="107">23/31 (City/Hwy)</span><br data-reactid="108"/></div><div class="pv1" title="All Wheel Drive" data-reactid="109"><span class="dib b w6rem" data-reactid="110"><span data-reactid="111">Drivetrain</span><span class="" data-reactid="112">: </span></span><span class="" data-reactid="113">All Wheel Drive</span><br data-reactid="114"/></div><div class="truncate pv1" title="Ice White" data-reactid="115"><span class="dib b w6rem" data-reactid="116"><span data-reactid="117">Ext. Color</span><span class="" data-reactid="118">: </span></span><span class="" itemprop="color" data-reactid="119">Ice White</span><br data-reactid="120"/></div><div class="pv1" title="8-Speed Geartronic Automatic -inc: start/stop" data-reactid="121"><span class="dib b w6rem" data-reactid="122"><span data-reactid="123">Trans</span><span class="" data-reactid="124">: </span></span><span class="" itemprop="vehicleTransmission" data-reactid="125">8-Speed Geartronic Automatic -inc: start/stop</span><br data-reactid="126"/></div><div class="truncate pv1" title="Charcoal" data-reactid="127"><span class="dib b w6rem" data-reactid="128"><span data-reactid="129">Int. Color</span><span class="" data-reactid="130">: </span></span><span class="" itemprop="vehicleInteriorColor" data-reactid="131">Charcoal</span><br data-reactid="132"/></div><div class="pv1" title="V190804" data-reactid="133"><span class="dib b w6rem" data-reactid="134"><span data-reactid="135">Stock #</span><span class="" data-reactid="136">: </span></span><span class="" data-reactid="137">V190804</span><br data-reactid="138"/></div><div class="pv1" title="Gasoline" data-reactid="139"><span class="dib b w6rem" data-reactid="140"><span data-reactid="141">Fuel Type</span><span class="" data-reactid="142">: </span></span><span class="" itemprop="fuelType" data-reactid="143">Gasoline</span><br data-reactid="144"/></div><div class="pv1" title="YV4162UK3K2134791" data-reactid="145"><span class="dib b w6rem" data-reactid="146"><span data-reactid="147">VIN</span><span class="" data-reactid="148">: </span></span><span class="" itemprop="vehicleIdentificationNumber" data-reactid="149">YV4162UK3K2134791</span><br data-reactid="150"/></div><div class="pv1" title="4 Cylinders" itemscope="" itemtype="http://schema.org/EngineSpecification" data-reactid="151"><span class="dib b w6rem" data-reactid="152"><span data-reactid="153">Engine</span><span class="" data-reactid="154">: </span></span><span class="" data-reactid="155">4 Cylinders</span><br data-reactid="156"/></div></div></div><div class="w-100" data-reactid="157"></div><div class="w-100 mt3 cc-container cc-row cc-nowrap cc-justify-start cc-align-stretch" data-reactid="158"><div class="w-50 bg-grey-100 pa3 f6 relative" data-reactid="159"><div class="f5 b mb2" data-reactid="160">Vehicle Location</div><div class="notranslate" data-reactid="161"><div data-reactid="162">Galpin Premier</div><div data-reactid="163">15500 Roscoe Blvd.</div><div data-reactid="164"><!-- react-text: 165 -->Van Nuys,<!-- /react-text --><!-- react-text: 166 --> <!-- /react-text --><!-- react-text: 167 -->CA<!-- /react-text --><!-- react-text: 168 --> <!-- /react-text --><!-- react-text: 169 -->91406<!-- /react-text --></div></div><a class="absolute right-1 top-1" href="#" data-reactid="170">Map</a></div><div class="w-50 ml3 bg-grey-100 pa3 f4 b theme-secondary" data-reactid="171"><div class="f5 b mb2 black" data-reactid="172">Call Us</div><div class="b" data-reactid="173"><a href="tel:8887120182" data-reactid="174">(888) 712-0182</a></div></div></div><div class="w-100 mt3 bg-grey-100 action-tools-tile" data-reactid="175"><div class="flex flex-row items-baseline justify-center" data-reactid="176"><span class="flex flex-column items-center tc mh3 mw2" data-reactid="177"><span data-reactid="178"><svg title="Save" class="save-favorite favorite pv2" style="display:inline-block;color:rgba(0, 0, 0, 0.8);fill:currentColor;height:50px;width:50px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;cursor:pointer;" viewBox="0 0 24 24" data-reactid="179"><path d="M22 9.24l-7.19-.62L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21 12 17.27 18.18 21l-1.63-7.03L22 9.24zM12 15.4l-3.76 2.27 1-4.28-3.32-2.88 4.38-.38L12 6.1l1.71 4.04 4.38.38-3.32 2.88 1 4.28L12 15.4z" data-reactid="180"></path></svg></span><span class="f8" data-reactid="181">Save</span></span><span class="flex flex-column items-center tc mh3 mw2" data-reactid="182"><span data-reactid="183"><svg title="Share" class="undefined facebook pv2" style="display:inline-block;fill:currentColor;height:50px;width:50px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;cursor:pointer;" viewBox="0 0 512 512" data-reactid="184"><path d="m512 85c0-44-40-85-85-85l-342 0c-45 0-85 41-85 85l0 342c0 45 40 85 85 85l171 0 0-193-63 0 0-86 63 0 0-33c0-57 43-109 96-109l69 0 0 85-69 0c-8 0-16 10-16 23l0 34 85 0 0 86-85 0 0 193 91 0c45 0 85-40 85-85z" data-reactid="185"></path></svg></span><span class="f8" data-reactid="186">Share</span></span><span class="flex flex-column items-center tc mh3 mw2" data-reactid="187"><span data-reactid="188"><svg title="Tweet" class="undefined twitter pv2" style="display:inline-block;fill:currentColor;height:50px;width:50px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;cursor:pointer;" viewBox="0 0 512 512" data-reactid="189"><path d="m461 0l-410 0c-28 0-51 23-51 51l0 410c0 28 23 51 51 51l410 0c28 0 51-23 51-51l0-410c0-28-23-51-51-51z m-59 187c-3 118-77 200-190 205-46 2-79-13-110-31 34 5 77-8 100-28-33-3-54-21-64-49 10 3 21 0 28 0-30-10-51-28-53-69 7 5 18 8 28 8-23-13-39-62-21-92 34 35 75 66 141 71-18-71 79-110 118-61 18-3 31-10 43-16-5 18-15 29-28 39 13-3 26-5 36-10-2 12-15 23-28 33z" data-reactid="190"></path></svg></span><span class="f8" data-reactid="191">Tweet</span></span><span class="flex flex-column items-center tc mh3 mw2" data-reactid="192"><span data-reactid="193"><svg title="Calculator" class="undefined calculator pv2" style="display:inline-block;fill:currentColor;height:50px;width:50px;user-select:none;transition:all 450ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;cursor:pointer;" viewBox="0 0 512 512" data-reactid="194"><path d="m448 0l-384 0c-18 0-32 14-32 32l0 448c0 18 14 32 32 32l384 0c18 0 32-14 32-32l0-448c0-18-14-32-32-32z m-288 448l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m128 192l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m128 192l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m0-96l-64 0 0-64 64 0z m0-128l-320 0 0-64 320 0z" data-reactid="195"></path></svg></span><span class="f8" data-reactid="196">Calculator</span></span></div></div><div class="w-100 mt3 cc-container cc-row cc-nowrap cc-justify-start cc-align-stretch" data-reactid="197"><div class="" data-reactid="198"></div><!-- react-empty: 199 --></div></div></div></div><div class="w-15-over-16 ci-align-self-center cc-container cc-column cc-nowrap cc-justify-start cc-align-start" data-reactid="200"><!-- react-empty: 201 --><div class="w-100 mt3" data-reactid="202"></div><!-- react-empty: 203 --><div class="w-100 mt3" data-reactid="204"><div class="f4 bb b--gainsboro w-100 b pa2" data-reactid="205"><div data-reactid="206">Standard Features</div></div><div class="auto5-features" data-reactid="207"><div class="w-15 fl" data-reactid="208"><ul class="tabs" data-reactid="209"><li class="ttu black bg-gray98 pv3 ph2 bb b--gainsboro pointer MECHANICAL" data-reactid="210">MECHANICAL</li><li class="ttu gray50 bg-white pv3 ph2 bb b--gainsboro pointer INTERIOR" data-reactid="211">INTERIOR</li><li class="ttu gray50 bg-white pv3 ph2 bb b--gainsboro pointer ENTERTAINMENT" data-reactid="212">ENTERTAINMENT</li><li class="ttu gray50 bg-white pv3 ph2 bb b--gainsboro pointer SAFETY" data-reactid="213">SAFETY</li><li class="ttu gray50 bg-white pv3 ph2 bb b--gainsboro pointer EXTERIOR" data-reactid="214">EXTERIOR</li><li class="ttu gray50 bg-white pv3 ph2 bb b--gainsboro pointer TECHSPECS" data-reactid="215">TECH SPECS</li></ul></div><div class="w-85 fl bg-gray98 pa2" data-reactid="216"><ul class="cc2 cg4 list-disc pl4" data-reactid="217"><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="218"><meta itemprop="name" content="feature" data-reactid="219"/><span itemprop="value" data-reactid="220"><h2 class="f5 normal di" data-reactid="221">14.2 Gal. Fuel Tank</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="222"><meta itemprop="name" content="feature" data-reactid="223"/><span itemprop="value" data-reactid="224"><h2 class="f5 normal di" data-reactid="225">3.33 Axle Ratio</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="226"><meta itemprop="name" content="feature" data-reactid="227"/><span itemprop="value" data-reactid="228"><h2 class="f5 normal di" data-reactid="229">4-Wheel Disc Brakes w/4-Wheel ABS, Front Vented Discs, Brake Assist, Hill Descent Control, Hill Hold Control and Electric Parking Brake</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="230"><meta itemprop="name" content="feature" data-reactid="231"/><span itemprop="value" data-reactid="232"><h2 class="f5 normal di" data-reactid="233">925lbs. Maximum Payload</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="234"><meta itemprop="name" content="feature" data-reactid="235"/><span itemprop="value" data-reactid="236"><h2 class="f5 normal di" data-reactid="237">Battery w/Run Down Protection</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="238"><meta itemprop="name" content="feature" data-reactid="239"/><span itemprop="value" data-reactid="240"><h2 class="f5 normal di" data-reactid="241">Brake Actuated Limited Slip Differential</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="242"><meta itemprop="name" content="feature" data-reactid="243"/><span itemprop="value" data-reactid="244"><h2 class="f5 normal di" data-reactid="245">Double Wishbone Front Suspension w/Coil Springs</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="246"><meta itemprop="name" content="feature" data-reactid="247"/><span itemprop="value" data-reactid="248"><h2 class="f5 normal di" data-reactid="249">Electric Power-Assist Speed-Sensing Steering</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="250"><meta itemprop="name" content="feature" data-reactid="251"/><span itemprop="value" data-reactid="252"><h2 class="f5 normal di" data-reactid="253">Engine: 2.0L I4 Direct-Injected Turbo-Charged</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="254"><meta itemprop="name" content="feature" data-reactid="255"/><span itemprop="value" data-reactid="256"><h2 class="f5 normal di" data-reactid="257">Front And Rear Anti-Roll Bars</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="258"><meta itemprop="name" content="feature" data-reactid="259"/><span itemprop="value" data-reactid="260"><h2 class="f5 normal di" data-reactid="261">Full-Time All-Wheel Drive</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="262"><meta itemprop="name" content="feature" data-reactid="263"/><span itemprop="value" data-reactid="264"><h2 class="f5 normal di" data-reactid="265">GVWR: 4,895 lbs (2,220 kgs)</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="266"><meta itemprop="name" content="feature" data-reactid="267"/><span itemprop="value" data-reactid="268"><h2 class="f5 normal di" data-reactid="269">Gas-Pressurized Shock Absorbers</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="270"><meta itemprop="name" content="feature" data-reactid="271"/><span itemprop="value" data-reactid="272"><h2 class="f5 normal di" data-reactid="273">Multi-Link Rear Suspension w/Transverse Leaf Springs</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="274"><meta itemprop="name" content="feature" data-reactid="275"/><span itemprop="value" data-reactid="276"><h2 class="f5 normal di" data-reactid="277">Permanent Locking Hubs</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="278"><meta itemprop="name" content="feature" data-reactid="279"/><span itemprop="value" data-reactid="280"><h2 class="f5 normal di" data-reactid="281">Quasi-Dual Stainless Steel Exhaust</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="282"><meta itemprop="name" content="feature" data-reactid="283"/><span itemprop="value" data-reactid="284"><h2 class="f5 normal di" data-reactid="285">Towing Equipment -inc: Trailer Sway Control</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="286"><meta itemprop="name" content="feature" data-reactid="287"/><span itemprop="value" data-reactid="288"><h2 class="f5 normal di" data-reactid="289">Transmission w/Driver Selectable Mode</h2></span></li><li class="lh-1_5 list-item" itemprop="additionalProperty" itemscope="" itemtype="http://schema.org/PropertyValue" data-reactid="290"><meta itemprop="name" content="feature" data-reactid="291"/><span itemprop="value" data-reactid="292"><h2 class="f5 normal di" data-reactid="293">Transmission: 8-Speed Geartronic Automatic -inc: start/stop</h2></span></li></ul></div></div></div><!-- react-empty: 294 --><div class="w-100 mt3" data-reactid="295"><div class="f4 bb b--gainsboro w-100 b pa2" data-reactid="296"><div data-reactid="297">Vehicle Disclaimer</div></div><div class="ml-15 pa2 f7 lh-2" data-reactid="298"><br/><br/><p class='a5-disclaimer'>VEHICLE DATA<br/>Certain specifications, prices and equipment data have been provided under license from Chrome Data Solutions (\&#39;Chrome Data\&#39;). © 2016 Chrome Data Solutions, LP. All Rights Reserved.  This information is supplied for personal use only and may not be used for any commercial purpose whatsoever without the express written consent of Chrome Data. Chrome Data makes no guarantee or warranty, either expressed or implied, including without limitation any warranty of merchantability or fitness for particular purpose, with respect to the data presented here. All specifications, prices and equipment are subject to change without notice.</p><p class='a5-disclaimer'>ESTIMATE MPG<br/>EPA mileage ratings are supplied by Chrome Data Solutions, LP for comparison purposes only. Your actual mileage will vary, depending on how you drive and maintain your vehicle, driving conditions, battery pack age/condition (hybrid models only) and other factors.</p><p class='a5-disclaimer'>PRICING<br/>Vehicle pricing is believed to be accurate. Tax, title and registration are not included in prices shown unless otherwise stated. Manufacturer incentives may vary by region and are subject to change. Vehicle information & features are based upon standard equipment and may vary by vehicle. Monthly payments may be higher or lower based upon incentives, qualifying programs, credit qualifications, residency & fees. No claims, or warranties are made to guarantee the accuracy of vehicle pricing, payments or actual equipment. Call to confirm accuracy of any information.</p><p class='a5-disclaimer'>MSRP<br/>The amount shown as MSRP is for informational purposes only and is the Manufacturer’s Suggested Retail Price. This amount does not represent an advertised or selling price and does not include the price of any dealer added equipment. All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Colors, options and trim levels may vary. Not responsible for typographical errors. Specifications, features, safety and warranty data are based on what is available as standard specs/features per trim level, for the designated model-year, and may not apply to vehicles with added packages or options. See dealer for written warranty information. Dealer makes no guarantees or warranties, either expressly or implied, with respect to the accuracy of any data listed on this page which was obtained from third party sources. All specifications, equipment and information are subject to change without notice. Any information contained on this page should be used for informational purposes only. Galpin’s internet advertising is intended only for persons in California.</p><p class='a5-disclaimer'>PRICE<br/>All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Not responsible for typographical errors. Prices valid through today’s close of business. Subject to prior sale. Any information contained on this page should be used for informational purposes only. Galpin’s internet advertising is intended only for persons in California.</p><br/><div class='conditional-disclaimer lojack'>Notice All of Galpin used vehicles have an active theft deterrent device installed. This advertised price excludes the purchase price of the optional theft deterrent device which can be (1) purchased for an additional cost or (2) deactivated at the time of sale. If the device is deactivated it will be a non-functional item and at no time will it be activated.</div> </div></div></div></div><div data-reactid="299"></div><!-- react-empty: 300 --></div></div></div><div style="position:fixed;left:50%;display:flex;bottom:0;z-index:2900;visibility:hidden;transform:translate(-50%, 48px);transition:transform 400ms cubic-bezier(0.23, 1, 0.32, 1) 0ms, visibility 400ms cubic-bezier(0.23, 1, 0.32, 1) 0ms;" data-reactid="301"><!-- react-empty: 302 --></div></div></div></div><!-- /skipjro -->
                    </div>

        </div>
    </div>


<!-- mfn_hook_content_after --><!-- mfn_hook_content_after -->
<!-- Above Footer -->
  

<!-- #Footer Action -->
    <div class="footer-action-bar">
        <ul class="full-bar">
                            <li class="footer-action-bar1"><div><div class="textwidget"><div class='small-align-center medium-align-right footer-social flex'><a href="https://twitter.com/GalpinPremier" target="_blank"><img class="alignnone size-full" src="https://images.jazelc.com/uploads/galpinpremier/icon-twitter.png" alt="Follow Us on Twitter" width="36" height="36" /></a><a href="https://www.instagram.com/explore/locations/6761209/galpin-premier/" target="_blank"><img src="https://images.jazelc.com/uploads/galpinpremier/icon-ig.png" alt="" width="36" height="36" class="alignnone size-full wp-image-2238" /></a><a href="http://www.youtube.com/user/GalpinPremier" target="_blank"><img class="alignnone size-full" src="https://images.jazelc.com/uploads/galpinpremier/icon-youtube-play.png" alt="Watch Us on Youtube" width="36" height="36" /></a><a href="https://www.facebook.com/GalpinPremier" target="_blank"><img class="alignnone size-full" src="https://images.jazelc.com/uploads/galpinpremier/icon-fb.png" alt="Follow Us on Facebook" width="36" height="36" /></a><a href="https://plus.google.com/100969303100455382936/posts" target="_blank"><img class="alignnone size-full" src="https://images.jazelc.com/uploads/galpinpremier/icon-google.png" alt="Join Us on Google Plus" width="36" height="36" /></a><a href="http://www.yelp.com/biz/galpin-premier-collection-van-nuys" target="_blank"><img class="alignnone size-full" src="https://images.jazelc.com/uploads/galpinpremier/icon-yelp.png" alt="Read About Us on Yelp" width="36" height="36" /></a></div></div></div></li>
                                        <li class="footer-action-bar2"><div>
                <div class='gf_browser_chrome gform_wrapper form_newsletter_wrapper' id='gform_wrapper_38' ><a id='gf_38' class='gform_anchor' ></a><form method='post' enctype='multipart/form-data' target='gform_ajax_frame_38' id='gform_38' class='form_newsletter' action='/inventory/new-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA#gf_38'> 
 <input type='hidden' class='gforms-pum' value='{"closepopup":false,"closedelay":0,"openpopup":false,"openpopup_id":0}' />
                        <div class='gform_body'><ul id='gform_fields_38' class='gform_fields top_label form_sublabel_below description_below'><li id='field_38_1' class='gfield field_sublabel_below field_description_below' ><label class='gfield_label' for='input_38_1' >Newsletter</label><div class='ginput_container ginput_container_email'>
                            <input name='input_1' id='input_38_1' type='text' value='' class='large' tabindex='1'   placeholder='signmeup@gmail.com'/>
                        </div></li>
                            </ul></div>
        <div class='gform_footer top_label'> <input type='submit' id='gform_submit_button_38' class='gform_button button' value='Join' tabindex='2' onclick='if(window["gf_submitting_38"]){return false;}  window["gf_submitting_38"]=true;  ' /> <input type='hidden' name='gform_ajax' value='form_id=38&amp;title=&amp;description=&amp;tabindex=1' />
            <input type='hidden' class='gform_hidden' name='is_submit_38' value='1' />
            <input type='hidden' class='gform_hidden' name='gform_submit' value='38' />
            
            <input type='hidden' class='gform_hidden' name='gform_unique_id' value='' />
            <input type='hidden' class='gform_hidden' name='state_38' value='WyJbXSIsImFjYWNkODE0MTg0ZGE5OGVmMTkzM2ZmZGUyNjVjNmVjIl0=' />
            <input type='hidden' class='gform_hidden' name='gform_target_page_number_38' id='gform_target_page_number_38' value='0' />
            <input type='hidden' class='gform_hidden' name='gform_source_page_number_38' id='gform_source_page_number_38' value='1' />
            <input type='hidden' name='gform_field_values' value='' />
            
        </div>
                        </form>
                        </div>
                <iframe style='display:none;width:0px;height:0px;' src='about:blank' name='gform_ajax_frame_38' id='gform_ajax_frame_38'></iframe>
                <script type='text/javascript'>jQuery(document).ready(function($){gformInitSpinner( 38, '/content/plugins/gravityforms/images/spinner.gif' );jQuery('#gform_ajax_frame_38').load( function(){var contents = jQuery(this).contents().find('*').html();var is_postback = contents.indexOf('GF_AJAX_POSTBACK') >= 0;if(!is_postback){return;}var form_content = jQuery(this).contents().find('#gform_wrapper_38');var is_confirmation = jQuery(this).contents().find('#gform_confirmation_wrapper_38').length > 0;var is_redirect = contents.indexOf('gformRedirect(){') >= 0;var is_form = form_content.length > 0 && ! is_redirect && ! is_confirmation;if(is_form){jQuery('#gform_wrapper_38').html(form_content.html());setTimeout( function() { /* delay the scroll by 50 milliseconds to fix a bug in chrome */ jQuery(document).scrollTop(jQuery('#gform_wrapper_38').offset().top); }, 50 );if(window['gformInitDatepicker']) {gformInitDatepicker();}if(window['gformInitPriceFields']) {gformInitPriceFields();}var current_page = jQuery('#gform_source_page_number_38').val();gformInitSpinner( 38, '/content/plugins/gravityforms/images/spinner.gif' );jQuery(document).trigger('gform_page_loaded', [38, current_page]);window['gf_submitting_38'] = false;}else if(!is_redirect){var confirmation_content = jQuery(this).contents().find('#gforms_confirmation_message_38').html();if(!confirmation_content){confirmation_content = contents;}setTimeout(function(){jQuery('#gform_wrapper_38').replaceWith('<' + 'div id=\'gforms_confirmation_message_38\' class=\'gform_confirmation_message_38 gforms_confirmation_message\'' + '>' + confirmation_content + '<' + '/div' + '>');jQuery(document).scrollTop(jQuery('#gforms_confirmation_message_38').offset().top);jQuery(document).trigger('gform_confirmation_loaded', [38]);window['gf_submitting_38'] = false;}, 50);}else{jQuery('#gform_38').append(contents);if(window['gformRedirect']) {gformRedirect();}}jQuery(document).trigger('gform_post_render', [38, current_page]);} );} );</script><script type='text/javascript'> if(typeof gf_global == 'undefined') var gf_global = {"gf_currency_config":{"name":"U.S. Dollar","symbol_left":"$","symbol_right":"","symbol_padding":"","thousand_separator":",","decimal_separator":".","decimals":2},"base_url":"\/content\/plugins\/gravityforms","number_formats":[],"spinnerUrl":"\/content\/plugins\/gravityforms\/images\/spinner.gif"};jQuery(document).bind('gform_post_render', function(event, formId, currentPage){if(formId == 38) {if(typeof Placeholders != 'undefined'){
                        Placeholders.enable();
                    }} } );jQuery(document).bind('gform_post_conditional_logic', function(event, formId, fields, isInit){} );</script><script type='text/javascript'> jQuery(document).ready(function(){jQuery(document).trigger('gform_post_render', [38, 1]) } ); </script></div></li>
                    </ul>
    </div>

<!-- #Footer -->		
<footer id="Footer" class="clearfix">
	
     
	
	<div class="widgets_wrapper"><div class="container"><div class="column one-second"><aside id="black-studio-tinymce-12" class="widget widget_black_studio_tinymce"><div class="textwidget"><div class='small-align-center medium-align-left footer-sitename'><em>GALPIN</em> PREMIER</div></div></aside></div><div class="column one-second"><aside id="black-studio-tinymce-13" class="widget widget_black_studio_tinymce"><div class="textwidget"><div class='footer-phone'><a href='tel:(800) 564-7891'>Sales: (800) 564-7891</a><a href='tel:(888) 705-9213'>Service: (888) 705-9213</a></div></div></aside></div></div></div>    
    <!-- Below Footer -->
            <div class='below-footer'>
            <div class='container'>
                <div class='column one'><div id="black-studio-tinymce-6" class="widget widget_black_studio_tinymce"><div class="textwidget"><div class="footer-links"><a href="/inventory/new-vehicles/">New Cars</a><a href="/inventory/used-vehicles/">Used Cars</a><a href="/finance-center/">Finance</a><a href="/service-center/">Service</a><a href="/parts-center/">Parts</a><a href="/about-us/">About Galpin</a><a href="/why-galpin/">Why Go Galpin</a><a href="/sitemap/">Site Map</a><a href="/privacy-policy/">Privacy Policy</a><a href="/california-supply-chains-act/">California Supply Chains Act</a></div></div></div><div id="black-studio-tinymce-11" class="widget widget_black_studio_tinymce"><div class="textwidget"><div class='footer-copyright'><span style='white-space:nowrap;'>Copyright © 2019 Galpin Premier.</span> <span style='white-space:nowrap;'>All rights reserved.</span><div class='footer-webmaster'>Dealer Websites by <a href="http://www.jazelauto.com" target="_blank">Jazel Auto</a></div></div></div></div></div>
            </div>
        </div>
          
    
                <div class='page-footer-content bfooter'>
                <div class='container'>
                    <div class='column one'><p><script>// <![CDATA[
    (function() {
        var excludedMakes = ['subaru', 'lotus', 'aston martin', 'spyker','bentley', 'daewoo', 'ferrari', 'lamborghini', 'maserati', 'mclaren', 'porsche', 'rolls royce'],
            excludedModels = ['fcx', 'lf-a', 'r8','transit','super duty', 'econoline', 'gt-r', 'corvette','roush','shelby','f-650',],
            excludedTrims = ['saleen', 'roush','shelby'],
            excludedStock = [],
            excludedStyles = ['saleen','roush','shelby'];
    
        var domNode = document.querySelector("#srp-app");
        domNode.addEventListener("customZoneDidMount", function(e) {
            if (e.detail.data.name === "srp-beside-certs-zone") {
                var vehicle = e.detail.data.vehicle,
                    year = Math.floor(vehicle.year),
                    style = vehicle.style_name == undefined ? '' : vehicle.style_name.toLowerCase(),
                    stock = vehicle.stock_number,
                    make = vehicle.make.toLowerCase(),
                    model = vehicle.model.toLowerCase(),
                    trim = vehicle.trim == undefined ? '' : vehicle.trim.toLowerCase(),
                    mileage = Math.floor(vehicle.mileage);
                
                function exclusions(){
                    for(var ma = 0; ma < excludedMakes.length; ma++) {
                        if(make.indexOf(excludedMakes[ma]) == 0) {
                            return true;
                        }
                    }
                    for (var mo = 0; mo < excludedModels.length; mo++) {
                        if (model.indexOf(excludedModels[mo]) == 0) {
                            return true;
                        }
                    }
                    for (var tr = 0; tr < excludedTrims.length; tr++) {
                        if (trim.indexOf(excludedTrims[tr]) == 0) {
                            return true;
                        }
                    }
                    for (var stk = 0; stk < excludedStock.length; stk++) {
                        if (stock.indexOf(excludedStock[stk]) == 0) {
                            return true;
                        }
                    }
                    for (var st = 0; st < excludedStyles.length; st++) {
                        if (style.indexOf(excludedStyles[st]) == 0) {
                            return true;
                        }
                    }

                    return false;
                };

                if( year === 2018 && model !== 'e-golf' && make === 'volkswagen' && vehicle.condition.toLowerCase() === 'new'){
                    var peopleFirst = '<a href="/people-first-warranty/"><img style="max-width: 250px; width: 100%; min-width: 150px;" src="https://images.jazelc.com/uploads/galpinpremier/People-FIrst-Warranty-Logo-1024x307.png"/></a>';
                } else {
                    peopleFirst = '';
                }

                if (!exclusions() && vehicle.condition.toLowerCase() === 'new') {
                    var keepItNew = '<a href="/keep-it-new/" title="Galpin Keep It New Program"><img src="https://images.jazelc.com/uploads/galpinpremier/PAG_gold_SRP_KINlogo_C2.jpg" class="keep_it_new_srp_badge w-250px" alt="" /></a>';
                    e.detail.element.style.display = 'flex';
                    e.detail.element.style.alignItems = 'center';
                    e.detail.appendHtmlToElement(peopleFirst + keepItNew);
                } else if (peopleFirst.length > 0) {
                    e.detail.appendHtmlToElement(peopleFirst);
                }
            }
        });
        domNode.addEventListener("customZoneDidMount", function(e) {
            if (e.detail.data.name === "vdp-beside-certs-zone") {
                var vehicle = e.detail.data.vehicle,
                    year = Math.floor(vehicle.year),
                    make = vehicle.make.toLowerCase(),
                    model = vehicle.model.toLowerCase();

                if( year === 2018 && model !== 'e-golf' && make === 'volkswagen'){
                    var peopleFirst = '<a href="/people-first-warranty/"><img style="max-width: 250px; width: 100%; min-width: 150px;" src="https://images.jazelc.com/uploads/galpinpremier/People-FIrst-Warranty-Logo-1024x307.png"/></a>'
                    e.detail.appendHtmlToElement(peopleFirst);
                }
            }
            if (e.detail.data.name === "vdp-below-price-zone") {
                var vehicle = e.detail.data.vehicle,
                    year = Math.floor(vehicle.year),
                    style = vehicle.style_name == undefined ? '' : vehicle.style_name.toLowerCase(),
                    stock = vehicle.stock_number,
                    make = vehicle.make.toLowerCase(),
                    model = vehicle.model.toLowerCase(),
                    trim = vehicle.trim == undefined ? '' : vehicle.trim.toLowerCase(),
                    mileage = Math.floor(vehicle.mileage);
                
                function exclusions(){
                    for(var ma = 0; ma < excludedMakes.length; ma++) {
                        if(make.indexOf(excludedMakes[ma]) == 0) {
                            return true;
                        }
                    }
                    for (var mo = 0; mo < excludedModels.length; mo++) {
                        if (model.indexOf(excludedModels[mo]) == 0) {
                            return true;
                        }
                    }
                    for (var tr = 0; tr < excludedTrims.length; tr++) {
                        if (trim.indexOf(excludedTrims[tr]) == 0) {
                            return true;
                        }
                    }
                    for (var stk = 0; stk < excludedStock.length; stk++) {
                        if (stock.indexOf(excludedStock[stk]) == 0) {
                            return true;
                        }
                    }
                    for (var st = 0; st < excludedStyles.length; st++) { if (style.indexOf(excludedStyles[st]) == 0) { return true; } } return false; }; if(!exclusions() && vehicle.condition.toLowerCase() === 'new') { // If buttons in default position, stretch them all to 100% var secondCta = document.querySelectorAll('.cta-buttons > .w-50')[0];
                    if(typeof secondCta != 'undefined') {
                        secondCta.classList.remove('w-50');
                        secondCta.classList.add('w-100');
                    }
                    
                    // If buttons in below price position...
                    var infoContainer = e.detail.element.parentNode.parentNode,
                        customContainer = e.detail.element.parentNode,
                        ctaContainer = e.detail.element.parentNode.previousSibling,
                        ctaInnerContainer = ctaContainer.querySelector('.w-40');
    
                    // Adjust container to flex wrap, and flex-direction as row
                    infoContainer.classList.remove('cc-column');
                    infoContainer.classList.remove('cc-nowrap');
                    infoContainer.classList.add('cc-row');
                    infoContainer.classList.add('cc-wrap');
    
                    // Set CTA and new container to w-50
                    customContainer.classList.remove('w-100');
                    ctaContainer.classList.remove('w-100');
                    customContainer.classList.add('w-50');
                    ctaContainer.classList.add('w-50');
                    
                    if(window.innerWidth >= 768) {
                        // Set CTA buttons container to w-100
                        ctaInnerContainer.classList.remove('w-40');
                        ctaInnerContainer.classList.add('w-100');
                    } else {
                        ctaContainer.querySelector('.w-50').classList.add('w-100');
                        ctaContainer.querySelector('.w-50').classList.remove('w-50');
                    }
                    
                    // Swap CTA and new container positions
                    customContainer.style.transform = 'translateX(-100%)';
                    ctaContainer.style.transform = 'translateX(100%)';

                    var keepItNew = '<a href="/keep-it-new/" title="Galpin Keep It New Program"><img src="https://images.jazelc.com/uploads/galpinpremier/PREMIER_gold_VDP_KINlogo_C2.jpg" class="keep_it_new_vdp_badge" alt="" /></a>';
                    e.detail.appendHtmlToElement(keepItNew);
                }
            }
        });
    })();
// ]]&gt;</script><script>
  (function (w,d,s,o,f,js,fjs) {
    w['mk-call-widget']=o;w[o] = w[o] || function () { 
      (w[o].q = w[o].q || []).push(arguments) };
      js = d.createElement(s), fjs = d.getElementsByTagName(s)[0];
      js.id = o; js.src = f; js.async = 1; 
      fjs.parentNode.insertBefore(js, fjs);
  }(window, document, 'script', 'mKcc', 'https://api.mykaarma.com/click2call/call_widget.js'));

  mKcc('init', { dealerUuid: "d4e55c35b74ff64b8a3208343ea2bad444154d94e91e55a216b85e794a1ffa4c", departmentUuid:"08d44a75cf5d7af294b63d86dba966267a4acd48a6da4f27fefa20c5e4e3d2eb"});



  function fireMyKarmaButton(el) {
        mKcc('call',{
            stockNumber: el.dataset.stock,
            vin: el.dataset.vin,
            make: el.dataset.make,
            model: el.dataset.model,
            year: el.dataset.year,
            trim: el.dataset.trim,
            price: el.dataset.price,
            permalink: el.dataset.permalink
        });
    }


    jQuery(document).on('click','.fireMyKarmaButton', function(e) {
        e.preventDefault();
        fireMyKarmaButton(jQuery(this)[0]);
    })
</script><script>(function() {
    var excludedMakes = ['aston martin', 'bentley', 'ferrari', 'lamborghini', 'lotus', 'maserati', 'maybach', 'mclaren', 'panoz', 'rolls royce'],
        excludedModels = ['slr-mclaren'],
        excludedTrims = [],
        excludedStock = [],
        excludedStyles = [];
    var currentYear = new Date().getFullYear();

    var domNode = document.querySelector("#srp-app");
    domNode.addEventListener("customZoneDidMount", function(e) {
        if (e.detail.data.name === "srp-beside-certs-zone") {
            var vehicle = e.detail.data.vehicle;
            var year = Math.floor(vehicle.year);
            var style = vehicle.style_name == undefined ? '' : vehicle.style_name.toLowerCase();
            var stock = vehicle.stock_number;
            var make = vehicle.make.toLowerCase();
            var model = vehicle.model.toLowerCase();
            var trim = vehicle.trim == undefined ? '' : vehicle.trim.toLowerCase();
            var mileage = Math.floor(vehicle.mileage);
            function filterOut(){
                for(var ma = 0; ma < excludedMakes.length; ma++) {
                    if(make.indexOf(excludedMakes[ma]) == 0) {
                        return false;
                    }
                }
                for(var mo = 0; mo < excludedModels.length; mo++) {
                    if(model.indexOf(excludedModels[mo]) == 0) {
                        return false;
                    }
                }
                for(var tr = 0; tr < excludedTrims.length; tr++) {
                    if(trim.indexOf(excludedTrims[tr]) == 0){
                        return false;
                    }
                }
                for(var stk = 0; stk < excludedStock.length; stk++) {
                    if(stock.indexOf(excludedStock[stk]) == 0) {
                        return false;
                    }
                }
                for(var st = 0; st < excludedStyles.length; st++) {
                    if(style.indexOf(excludedStyles[st]) == 0) {
                        return false;
                    }
                }
                
                return true;
            };
            if (year < (currentYear - 11) || year > (currentYear - 1) || !filterOut() || mileage > 100000 || vehicle.condition == 'New' || vehicle.condition == 'Certified') {
                return;
            }
            var toWrite = '<a href="/galpin-used-car-difference/" title="Galpin Motor Trend Certified Vehicle"><img src="https://images.jazelc.com/uploads/galpinpremier/MotorTrend-Certification-Badge.png" class="srp_warranty_badge" width="125" alt="" /></a>';
            // document.querySelectorAll('.conditional-disclaimer.warranty')[0].style.display = 'none';
            document.querySelectorAll('.conditional-disclaimer.lojack')[0].style.display = 'none';
            e.detail.appendHtmlToElement(toWrite);
        }
        if (e.detail.data.name === "srp-below-price-zone") {
    var myKarmaButton ='<a href="#"><img src="https://images.jazelc.com/uploads/galpinpremier/CallMeBlue-CTA.png" height="59" width="227" align="right" style="margin-right: .25rem; padding-right: .25rem;" class="fireMyKarmaButton" data-vin="'+ e.detail.data.vehicle.vin+'" data-stock="'+ e.detail.data.vehicle.stock_number+'" data-make="'+ e.detail.data.vehicle.make+'" data-model="'+ e.detail.data.vehicle.model+'" data-year="'+ e.detail.data.vehicle.year+'" data-trim="'+ e.detail.data.vehicle.trim+'" data-price="'+ e.detail.data.vehicle.price +'" data-permalink="'+ e.detail.vehicleDetailsUrl+'"></a>';
    e.detail.appendHtmlToElement(myKarmaButton);
}
    });
    domNode.addEventListener("customZoneDidMount", function(e) {
        if (e.detail.data.name === "vdp-beside-certs-zone") {
            var vehicle = e.detail.data.vehicle;
            var year = Math.floor(vehicle.year);
            var style = vehicle.style_name == undefined ? '' : vehicle.style_name.toLowerCase();
            var stock = vehicle.stock_number;
            var make = vehicle.make.toLowerCase();
            var model = vehicle.model.toLowerCase();
            var trim = vehicle.trim == undefined ? '' : vehicle.trim.toLowerCase();
            var mileage = Math.floor(vehicle.mileage);
            if(vehicle.account_name === 'Galpin Honda') {
                document.querySelectorAll('.conditional-disclaimer.lojack')[0].style.display = 'block';
            }
            function filterOut(){
                for(var ma = 0; ma < excludedMakes.length; ma++) {
                    if(make.indexOf(excludedMakes[ma]) == 0) {
                        return false;
                    }
                }
                for(var mo = 0; mo < excludedModels.length; mo++) {
                    if(model.indexOf(excludedModels[mo]) == 0) {
                        return false;
                    }
                }
                for(var tr = 0; tr < excludedTrims.length; tr++) {
                    if(trim.indexOf(excludedTrims[tr]) == 0){
                        return false;
                    }
                }
                for(var stk = 0; stk < excludedStock.length; stk++) {
                    if(stock.indexOf(excludedStock[stk]) == 0) {
                        return false;
                    }
                }
                for(var st = 0; st < excludedStyles.length; st++) {
                    if(style.indexOf(excludedStyles[st]) == 0) {
                        return false;
                    }
                }
                
                return true;
            };
            if (year < (currentYear - 11) || year > (currentYear - 1) || !filterOut() || mileage > 100000 || vehicle.condition == 'New' || vehicle.condition == 'Certified') {
                return;
            }
            document.querySelectorAll('.conditional-disclaimer.warranty')[0].style.display = 'block';
            var toWrite = '<a href="/motor-trend-certified-vehicles/" title="Galpin Motor Trend Certified Vehicle"><img src="https://images.jazelc.com/uploads/galpinpremier/MotorTrend-Certification-Badge.png" class="vdp_warranty_badge" style="margin:2em 0;" width="150" alt="" /></a>';
            e.detail.appendHtmlToElement(toWrite);
        }
        if (e.detail.data.name === "vdp-below-price-zone") {
    var myKarmaButton ='<a href="#"><img src="https://images.jazelc.com/uploads/galpinpremier/CallMeBlue-CTA.png" height="59" width="225" align="right" class="fireMyKarmaButton" data-vin="'+ e.detail.data.vehicle.vin+'" data-stock="'+ e.detail.data.vehicle.stock_number+'" data-make="'+ e.detail.data.vehicle.make+'" data-model="'+ e.detail.data.vehicle.model+'" data-year="'+ e.detail.data.vehicle.year+'" data-trim="'+ e.detail.data.vehicle.trim+'" data-price="'+ e.detail.data.vehicle.price +'" data-permalink="'+ e.detail.vehicleDetailsUrl+'"></a>';
    jQuery(e.detail.element.parentNode.previousSibling.childNodes[0].childNodes[0]).after('</p>
<div class="w-100 eprice">
<div class="eprice f4 ma1 pa1 br2 tr pointer">'+myKarmaButton+'</div>
</div>
<p>');
}
    });
})();
</script><script>
(function() {
    var domNode = document.querySelector("#srp-app");
    domNode.addEventListener("customZoneDidMount", function(e) {
        if (e.detail.data.name === "srp-beside-certs-zone") {

        }
        if (e.detail.data.name === "vdp-beside-certs-zone") {

        }
        if (e.detail.data.name === "vdp-below-price-zone") {
        	var vehicle = e.detail.data.vehicle,
        		year = Math.floor(vehicle.year),
        		make = vehicle.make,
        		model = vehicle.model,
        		trim = vehicle.trim,
        		vehicleStatus = (vehicle.used === "1") ? "Used" : "New",
				vehicleStatusExtended = (vehicle.used === "1") ? (vehicle.certifiedByManufacturer ? "CPO" : "USED") : "NEW",
				isCertified = vehicle.certifiedByManufacturer,
        		vin = vehicle.vin,
        		stock = vehicle.stock_number,
        		transmission = vehicle.transmission,
        		mileage = Math.floor(vehicle.mileage),
        		body = vehicle.vehicle_type[0],
        		listedPrice = Math.floor(vehicle.display_price),
        		interiorcolor = vehicle.interior_factory_color,
        		exteriorcolor = vehicle.exterior_factory_color;

            var txt = "<scr" + "ipt>" +
					"fbq('track', 'ViewContent', {" +
					"content_ids: ['" + vin + "'], " +
					"content_type: 'vehicle', " +
					"make: '" + make + "', " +
					"model: '" + model + "', " +
					"year: '" + year + "', " +
					"state_of_vehicle: '" + vehicleStatusExtended +"', " +
					"body_style: '" + body + "', " +
					"price: " + listedPrice + ", " +
					"currency: 'USD', " +
					"vin: '" + vin + "'" +
					"});" +
					"</scri" + "pt>";

            e.detail.appendHtmlToElement(txt);
        }
    });
    domNode.addEventListener("customZoneDidMount", function(e) {
        if (e.detail.data.name === "srp-below-price-zone") {
        	var vehicle = e.detail.data.vehicle,
        		year = Math.floor(vehicle.year),
        		make = vehicle.make,
        		model = vehicle.model,
        		trim = vehicle.trim,
        		vehicleStatus = (vehicle.used === "1") ? "Used" : "New",
        		vin = vehicle.vin,
        		stock = vehicle.stock_number,
        		transmission = vehicle.transmission,
        		mileage = Math.floor(vehicle.mileage),
        		body = vehicle.vehicle_type[0],
        		listedPrice = Math.floor(vehicle.display_price),
        		interiorcolor = vehicle.interior_factory_color,
        		exteriorcolor = vehicle.exterior_factory_color;

            var txt = '';

            e.detail.appendHtmlToElement();
        }
    });
})();
</script><script>
(function() {
    var domNode = document.querySelector("#srp-app");
    domNode.addEventListener("customZoneDidMount", function(e) {
        if (e.detail.data.name === "vdp-below-price-zone") {
            var vehicle = e.detail.data.vehicle,
                pricingName = vehicle.pricing[0].Name;

            if (pricingName == "@Galpinized"){
              console.log("Galpinized");
              jQuery(".paper-2 div:contains('Special Offers')").parent().css("display","none");
            }
        }
    });
})();
</script></p>
</div>
                </div>
            </div>
    
		<div class="footer_copy">
		<div class="container">
			<div class="column one">
			
								<a id="back_to_top" class="button button_left button_js " href=""><span class="button_icon"><i class="icon-up-open-big"></i></span></a>
				
				<ul class="social"></ul>						
			</div>
		</div>
	</div>
		
</footer>

            <!-- Footer (Footer): SSR enabled -->
                    <!-- #jazel_mobile_footer  -->
        <!-- skipjro --><div id="jazel_mobile_footer"><div data-radium="true" data-reactroot="" data-reactid="1" data-react-checksum="-1201469506"><div data-radium="true" data-reactid="2"><style data-reactid="3">.jzl-a5-uibar-fixed-footer {
                            background: rgba(51, 51, 51, 1)
                        }</style><div class="rmq-8cbd1fa5 jzl-a5-uibar-fixed-footer jazel-a5-uibar-footer    footerNotScrolling hide" style="background:rgba(51, 51, 51, 1);z-index:11;position:relative;top:0px;left:0px;width:100%;" data-radium="true" data-reactid="4"><div class="rmq-8cbd1fa5 jazel-a5-uibar-row-footer-0 flex overflow-auto" style="z-index:5;background:transparent;color:#FFFFFF;" data-radium="true" data-reactid="5"><div class="flex" style="flex:1 1 0%;align-items:center;" data-reactid="6"><div id="jzl-button-0.34333765512487147" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;height:100%;min-width:20px;margin:0px;font-size:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;border-width:0 1px 0 0;border-color:rgba(120, 120, 120, 1);border-style:solid;line-height:12px;" data-radium="true" data-reactid="7"><div data-radium="true" data-reactid="8"><i style="font-family:Material Icons;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="9">location_on</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="10"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="11"><!-- react-text: 12 --> <!-- /react-text --><!-- react-text: 13 --><!-- /react-text --></span><style data-reactid="14"></style></div></div></div><div id="jzl-button-0.8021932659465876" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;height:100%;min-width:20px;margin:0px;font-size:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;border-width:0 1px 0 0;border-color:rgba(120, 120, 120, 1);border-style:solid;line-height:12px;" data-radium="true" data-reactid="15"><div data-radium="true" data-reactid="16"><i style="font-family:auto5-font;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="17">B</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="18"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="19"><!-- react-text: 20 --> <!-- /react-text --><!-- react-text: 21 --><!-- /react-text --></span><style data-reactid="22"></style></div></div></div><div id="jzl-button-0.24047116491148857" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:left;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;border:0px solid rgba(120, 120, 120, 1);align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:0px;" data-radium="true" data-reactid="23"><div data-radium="true" data-reactid="24"><i style="font-family:Material Icons;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="25">build</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="26"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="27"><!-- react-text: 28 --> <!-- /react-text --><!-- react-text: 29 --><!-- /react-text --></span><style data-reactid="30"></style></div></div></div></div><div class="flex" data-reactid="31"></div></div></div><div class="rmq-8cbd1fa5 jzl-a5-ui-bar-hiding-footer jazel-a5-uibar-footer    footerNotScrolling hide" style="background:rgba(51, 51, 51, 1);z-index:10;position:fixed;left:0px;width:100%;" data-radium="true" data-reactid="32"><div class="rmq-8cbd1fa5 jazel-a5-uibar-row-footer-0 flex overflow-auto" style="z-index:5;background:transparent;color:#FFFFFF;" data-radium="true" data-reactid="33"><div class="flex" style="flex:1 1 0%;align-items:center;" data-reactid="34"><div id="jzl-button-0.34333765512487147" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;height:100%;min-width:20px;margin:0px;font-size:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;border-width:0 1px 0 0;border-color:rgba(120, 120, 120, 1);border-style:solid;line-height:12px;" data-radium="true" data-reactid="35"><div data-radium="true" data-reactid="36"><i style="font-family:Material Icons;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="37">location_on</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="38"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="39"><!-- react-text: 40 --> <!-- /react-text --><!-- react-text: 41 --><!-- /react-text --></span><style data-reactid="42"></style></div></div></div><div id="jzl-button-0.8021932659465876" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;box-sizing:border-box;background:transparent;color:#FFFFFF;float:left;flex:initial;height:100%;min-width:20px;margin:0px;font-size:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;border-width:0 1px 0 0;border-color:rgba(120, 120, 120, 1);border-style:solid;line-height:12px;" data-radium="true" data-reactid="43"><div data-radium="true" data-reactid="44"><i style="font-family:auto5-font;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="45">B</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="46"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="47"><!-- react-text: 48 --> <!-- /react-text --><!-- react-text: 49 --><!-- /react-text --></span><style data-reactid="50"></style></div></div></div><div id="jzl-button-0.24047116491148857" class="jazel-header-style-button flex" style="-webkit-box-pack:center;-webkit-flex:initial;-moz-box-sizing:border-box;-ms-flex:initial;-webkit-transition:300ms;-webkit-align-items:center;-webkit-justify-content:center;-ms-flex-align:center;-webkit-box-align:center;-ms-flex-pack:center;float:left;flex:initial;height:100%;min-width:20px;line-height:12px;margin:0px;text-align:center;transition:300ms;padding:12px 10px 8px;width:33%;border:0px solid rgba(120, 120, 120, 1);align-items:center;justify-content:center;icon-font-size:26px;cursor:pointer;border-radius:0px;box-sizing:border-box;background:transparent;color:#FFFFFF;font-size:0px;" data-radium="true" data-reactid="51"><div data-radium="true" data-reactid="52"><i style="font-family:Material Icons;font-style:normal;font-size:26px;" class="notranslate material-icons" data-radium="true" data-reactid="53">build</i><div style="display:block;font-size:0px;" data-radium="true" data-reactid="54"><span class="jazel-header-style-button-text" data-radium="true" data-reactid="55"><!-- react-text: 56 --> <!-- /react-text --><!-- react-text: 57 --><!-- /react-text --></span><style data-reactid="58"></style></div></div></div></div><div class="flex" data-reactid="59"></div></div></div></div><style data-reactid="60">@media (min-width: 1025px){ .rmq-8cbd1fa5{display: none !important;}}</style></div></div><!-- /skipjro -->
        </div><!-- #Wrapper -->

<!-- mfn_hook_bottom --><script type="text/javascript">
window.gubagooTrackKey = "NsV6rNGmPGBubJvMUQEDSM1D+v/x0Nc02Zzge6Y8rjHu7r+w22GO6C3nhLRL9SN9";
(function() {var e = document.createElement("script"); e.async = true;
e.src = window.location.protocol + "//gubagootracking.com/toolbars/toolbar_101910/loader_101910_1.js";
var s = document.getElementsByTagName("script")[0];
s.parentNode.insertBefore(e, s);
} ());
</script>

<script src="https://cdn.gubagoo.io/toolbars/101910/loader_101910_1.js" async></script><!-- mfn_hook_bottom -->	
<!-- wp_footer() -->
        <script>
            window.JazelAuto5HamburgerMenuSettings = {
                menuItemsFromWordpressMenu: [{"id":1549,"href":"\/","title":"Home","parent":0,"target":"","data":[]},{"id":11,"href":"\/inventory\/new-vehicles\/","title":"New Cars","parent":0,"target":"","data":[]},{"id":1602,"href":"\/inventory\/new-vehicles\/","title":"All Premier Collection","parent":11,"target":"","data":[]},{"id":2305,"href":"\/keep-it-new\/","title":"Keep It New Program","parent":11,"target":"","data":[]},{"id":1603,"href":"\/inventory\/new-vehicles\/models=Lincoln","title":"All Lincoln Vehicles","parent":11,"target":"","data":[]},{"id":1604,"href":"\/inventory\/new-vehicles\/models=Volvo","title":"All Volvo Vehicles","parent":11,"target":"","data":[]},{"id":1605,"href":"\/inventory\/new-vehicles\/models=Jaguar","title":"All Jaguar Vehicles","parent":11,"target":"","data":[]},{"id":1607,"href":"\/inventory\/new-vehicles\/models=Lotus","title":"All Lotus Vehicles","parent":11,"target":"","data":[]},{"id":1606,"href":"\/inventory\/new-vehicles\/models=Aston%20Martin","title":"All Aston Martin Vehicles","parent":11,"target":"","data":[]},{"id":12,"href":"\/used-car-center\/","title":"Used Cars","parent":0,"target":"","data":[]},{"id":1597,"href":"\/inventory\/used-luxury\/","title":"Luxury Pre-Owned","parent":12,"target":"","data":[]},{"id":1709,"href":"\/inventory\/certified-pre-owned\/","title":"Certified Luxury Vehicles","parent":12,"target":"","data":[]},{"id":1598,"href":"\/inventory\/used-vehicles\/models=Aston%20Martin","title":"Pre-Owned Aston Martin","parent":12,"target":"","data":[]},{"id":1599,"href":"\/inventory\/used-vehicles\/models=Jaguar","title":"Pre-Owned Jaguar","parent":12,"target":"","data":[]},{"id":1601,"href":"\/inventory\/used-vehicles\/models=Lincoln","title":"Pre-Owned Lincoln","parent":12,"target":"","data":[]},{"id":1600,"href":"\/inventory\/used-vehicles\/models=Volvo","title":"Pre-Owned Volvo","parent":12,"target":"","data":[]},{"id":1596,"href":"\/galpin-used-car-difference\/","title":"Galpin Used Car Difference","parent":12,"target":"","data":[]},{"id":18,"href":"\/specials\/","title":"Specials","parent":0,"target":"","data":[]},{"id":2304,"href":"\/keep-it-new\/","title":"Keep It New Program","parent":18,"target":"","data":[]},{"id":1587,"href":"http:\/\/www.galpinastonmartin.com\/new-specials\/","title":"Aston Martin Specials","parent":18,"target":"_blank","data":[]},{"id":1588,"href":"http:\/\/www.galpinjaguar.com\/new-specials\/","title":"Jaguar Specials","parent":18,"target":"_blank","data":[]},{"id":1589,"href":"http:\/\/www.galpinlincoln.com\/new-specials\/","title":"Lincoln Specials","parent":18,"target":"_blank","data":[]},{"id":1590,"href":"http:\/\/www.galpinlotus.com\/specials","title":"Lotus Specials","parent":18,"target":"_blank","data":[]},{"id":1591,"href":"http:\/\/www.galpinvolvo.com\/new-specials\/","title":"Volvo Specials","parent":18,"target":"_blank","data":[]},{"id":1698,"href":"https:\/\/www.galpinpremier.com\/service-specials\/","title":"Service Specials","parent":18,"target":"","data":[]},{"id":2395,"href":"\/rplate\/","title":"Digital License Plate","parent":18,"target":"","data":[]},{"id":59,"href":"https:\/\/www.galpinpremier.com\/finance-center\/","title":"Finance","parent":0,"target":"","data":[]},{"id":58,"href":"https:\/\/www.galpinpremier.com\/finance-center\/","title":"Finance Hours","parent":59,"target":"","data":[]},{"id":57,"href":"https:\/\/www.galpinpremier.com\/finance\/","title":"Apply Online","parent":59,"target":"","data":[]},{"id":1710,"href":"\/leasing\/","title":"Leasing at Galpin","parent":59,"target":"","data":[]},{"id":56,"href":"https:\/\/www.galpinpremier.com\/payment-calculators\/","title":"Estimate Payments","parent":59,"target":"","data":[]},{"id":2243,"href":"\/value-your-trade\/","title":"Value Your Trade","parent":59,"target":"","data":[]},{"id":33,"href":"https:\/\/www.galpinpremier.com\/service-center\/","title":"Service & Parts","parent":0,"target":"","data":[]},{"id":2405,"href":"\/service-specials\/","title":"Service Specials","parent":33,"target":"","data":[]},{"id":37,"href":"https:\/\/www.galpinpremier.com\/service-center\/","title":"Service Hours","parent":33,"target":"","data":[]},{"id":36,"href":"https:\/\/www.galpinpremier.com\/schedule-service\/","title":"Schedule Service","parent":33,"target":"","data":[]},{"id":35,"href":"https:\/\/www.galpinpremier.com\/parts-center\/","title":"Parts Hours","parent":33,"target":"","data":[]},{"id":1586,"href":"http:\/\/galpinautosports.com\/","title":"Galpin Auto Sports","parent":33,"target":"_blank","data":[]},{"id":2394,"href":"\/rplate\/","title":"Digital License Plate","parent":33,"target":"","data":[]},{"id":1712,"href":"\/about-us\/","title":"About Galpin","parent":0,"target":"","data":[]},{"id":64,"href":"https:\/\/www.galpinpremier.com\/hours-directions\/","title":"Hours & Directions","parent":1712,"target":"","data":[]},{"id":1583,"href":"\/mission-statement-core-values\/","title":"Galpin Mission & Values","parent":1712,"target":"","data":[]},{"id":1711,"href":"\/about-us\/","title":"Galpin History","parent":1712,"target":"","data":[]},{"id":1579,"href":"\/employment-opportunities\/","title":"Join Our Team","parent":1712,"target":"","data":[]},{"id":2103,"href":"\/newsroom\/","title":"Galpin News & Events","parent":1712,"target":"","data":[]},{"id":1581,"href":"\/galpin-horseless-carriage-restaurant\/","title":"Horseless Carriage Restaurant","parent":1712,"target":"","data":[]},{"id":1580,"href":"\/starbucks\/","title":"Starbucks at Galpin","parent":1712,"target":"","data":[]},{"id":1585,"href":"http:\/\/www.galpinastonmartin.com\/club-aston","title":"Galpin's Club Aston","parent":1712,"target":"","data":[]},{"id":2741,"href":"\/california-supply-chains-act\/","title":"California Supply Chains Act","parent":1712,"target":"","data":[]},{"id":60,"href":"https:\/\/www.galpinpremier.com\/contact-us\/","title":"Contact Us","parent":1712,"target":"","data":[]},{"id":2682,"href":"\/employment-opportunities\/","title":"Employment","parent":0,"target":"","data":[]},{"id":1713,"href":"\/why-galpin\/","title":"Why Go Galpin","parent":0,"target":"","data":[]}],
                textColor: "#fff",
                backgroundColor: "#082134",
                highlightColor: "#052e4e",
                highlightTextColor: "#ffffff",
                                debug: false,
                                                suppressHomeLink: true,
                                searchPlaceholderText: "Used White Truck",
                                srpUrl: "https://www.galpinpremier.com/inventory/all-vehicles/",
                                z_dummy: null
            };
        </script>
        <div id="pum-1503" class="pum pum-overlay pum-theme-1396 pum-theme-lightbox popmake-overlay click_open" data-popmake="{&quot;id&quot;:1503,&quot;slug&quot;:&quot;vehicle-specials-popup&quot;,&quot;theme_id&quot;:1396,&quot;cookies&quot;:[],&quot;triggers&quot;:[{&quot;type&quot;:&quot;click_open&quot;,&quot;settings&quot;:{&quot;extra_selectors&quot;:&quot;.specialVehicleCTAWrapper &gt; div:first-child button&quot;,&quot;do_default&quot;:null,&quot;cookie&quot;:{&quot;name&quot;:null}}}],&quot;mobile_disabled&quot;:null,&quot;tablet_disabled&quot;:null,&quot;meta&quot;:{&quot;display&quot;:{&quot;size&quot;:&quot;medium&quot;,&quot;responsive_min_width&quot;:&quot;&quot;,&quot;responsive_max_width&quot;:&quot;&quot;,&quot;custom_width&quot;:&quot;640&quot;,&quot;custom_height&quot;:&quot;380&quot;,&quot;animation_type&quot;:&quot;fade&quot;,&quot;animation_speed&quot;:&quot;350&quot;,&quot;animation_origin&quot;:&quot;center top&quot;,&quot;position_bottom&quot;:&quot;0&quot;,&quot;location&quot;:&quot;center top&quot;,&quot;position_right&quot;:&quot;0&quot;,&quot;position_top&quot;:&quot;100&quot;,&quot;position_left&quot;:&quot;0&quot;,&quot;overlay_zindex&quot;:&quot;1999999998&quot;,&quot;zindex&quot;:&quot;1999999999&quot;,&quot;responsive_min_width_unit&quot;:&quot;px&quot;,&quot;responsive_max_width_unit&quot;:&quot;px&quot;,&quot;custom_width_unit&quot;:&quot;px&quot;,&quot;custom_height_unit&quot;:&quot;px&quot;},&quot;close&quot;:{&quot;text&quot;:&quot;&quot;,&quot;button_delay&quot;:&quot;0&quot;,&quot;overlay_click&quot;:&quot;true&quot;,&quot;esc_press&quot;:&quot;true&quot;},&quot;click_open&quot;:{&quot;extra_selectors&quot;:&quot;&quot;}}}" role="dialog" aria-hidden="true" >

	<div id="popmake-1503" class="pum-container popmake theme-1396 pum-responsive pum-responsive-medium responsive size-medium">

				

				

		

				<div class="pum-content popmake-content">
			
		</div>


				

				            <button type="button" class="pum-close popmake-close" aria-label="Close">
			×            </button>
		
	</div>

</div>

    <script>
        (function() {
            window.addEventListener("buttonClick", function (e) {
                switch (e.detail.type) {
                    case "menu":
                        if ("hamburgerMenu" in window) {
                            window.hamburgerMenu.open();
                        }
                        break;
                }
            });

            jQuery('.responsive-menu-toggle').on('click', function (e) {
                e.preventDefault();
                if ("hamburgerMenu" in window) {
                    window.hamburgerMenu.open();
                }
            });
        })();
    </script>

    <script async type="text/javascript">
    var _paq = _paq || [];
  _paq.push(["disableCookies"]);
  _paq.push(['trackPageView']);
  _paq.push(['enableLinkTracking']);
  function embedTrackingCode() {
    var u="//analytics.jazel.net/analytics/piwik/";
    _paq.push(['setTrackerUrl', u+'piwik.php']);
    _paq.push(['setSiteId', 116]);
    var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
    g.type='text/javascript'; g.async=true; g.defer=true; g.src=u+'piwik.js'; s.parentNode.insertBefore(g,s);
  };
if (window.addEventListener) { 
    window.addEventListener("load", embedTrackingCode, false); 
} else if (window.attachEvent) { 
    window.attachEvent("onload",embedTrackingCode); 
} else {
    embedTrackingCode();
}
</script>			<script type="text/javascript">
				function revslider_showDoubleJqueryError(sliderID) {
					var errorMessage = "Revolution Slider Error: You have some jquery.js library include that comes after the revolution files js include.";
					errorMessage += "<br> This includes make eliminates the revolution slider libraries, and make it not work.";
					errorMessage += "<br><br> To fix it you can:<br>&nbsp;&nbsp;&nbsp; 1. In the Slider Settings -> Troubleshooting set option:  <strong><b>Put JS Includes To Body</b></strong> option to true.";
					errorMessage += "<br>&nbsp;&nbsp;&nbsp; 2. Find the double jquery.js include and remove it.";
					errorMessage = "<span style='font-size:16px;color:#BC0C06;'>" + errorMessage + "</span>";
						jQuery(sliderID).show().html(errorMessage);
				}
			</script>
			<script type='text/javascript'>
/* <![CDATA[ */
var sb_instagram_js_options = {"sb_instagram_at":"476763402.3a81a9f.d1300208c8d54e569fcba29572c4746c"};
/* ]]> */
</script>
<script type='text/javascript' src='/content/plugins/instagram-feed/js/sb-instagram.min.js?ver=1.6.2'></script>
<script type='text/javascript' src='/content/plugins/jazel-inventory-search/resources/assets/js/inventory-search.js?ver=1.0.0'></script>
<script type='text/javascript' src='/content/plugins/jazel-inventory-search/resources/assets/js/easyResponsiveTabs.js?ver=1.2.1'></script>
<script type='text/javascript' src='//auto5-srp.jazelc.com/5.15.16/static/index.bundle.js?ver=5.15.16'></script>
<script type='text/javascript' src='/content/plugins/jazel-model-dropdown/resources/assets/js/model_dropdown.js?ver=1.0.0'></script>
<script type='text/javascript' src='/content/plugins/jzl-auto5-gravityforms/js/footer-script.js?ver=1.0.0'></script>
<script type='text/javascript' src='//cdn.rawgit.com/noelboss/featherlight/1.3.5/release/featherlight.min.js?ver=1.3.5'></script>
<script type='text/javascript' src='/content/plugins/jzl-auto5-products/js/jzla5p-srpform.js?ver=1.0.0'></script>
<script type='text/javascript' src='/content/plugins/jzl-auto5-products/js/hamburger-menu-init.js?ver=1.0.1'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/core.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/widget.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/mouse.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/sortable.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/tabs.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/accordion.min.js?ver=1.11.4'></script>
<script type='text/javascript' src='/content/themes/betheme/js/plugins.js?ver=20.4'></script>
<script type='text/javascript' src='/content/themes/betheme/js/menu.js?ver=20.4'></script>
<script type='text/javascript' src='/content/themes/betheme/assets/animations/animations.min.js?ver=20.4'></script>
<script type='text/javascript' src='/content/themes/betheme/assets/jplayer/jplayer.min.js?ver=20.4'></script>
<script type='text/javascript' src='/content/themes/betheme/js/parallax/translate3d.js?ver=20.4'></script>
<script type='text/javascript' src='/content/themes/betheme/js/scripts.js?ver=20.4'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/comment-reply.min.js?ver=4.8.2'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/jquery/ui/position.min.js?ver=1.11.4'></script>
<script type='text/javascript'>
/* <![CDATA[ */
var pum_vars = {"ajaxurl":"https:\/\/www.galpinpremier.com\/wp\/wp-admin\/admin-ajax.php","restapi":"https:\/\/www.galpinpremier.com\/wp-json\/pum\/v1","rest_nonce":null,"default_theme":"1395","debug_mode":"","disable_open_tracking":""};
var pum_debug_vars = {"debug_mode_enabled":"Popup Maker Debug Mode Enabled","debug_started_at":"Debug started at:","debug_more_info":"For more information on how to use this information visit http:\/\/docs.wppopupmaker.com\/?utm_medium=js-debug-info&utm_campaign=ContextualHelp&utm_source=browser-console&utm_content=more-info","global_info":"Global Information","localized_vars":"Localized variables","popups_initializing":"Popups Initializing","popups_initialized":"Popups Initialized","single_popup_label":"Popup: #","theme_id":"Theme ID: ","label_method_call":"Method Call:","label_method_args":"Method Arguments:","label_popup_settings":"Settings","label_triggers":"Triggers","label_cookies":"Cookies","label_delay":"Delay:","label_conditions":"Conditions","label_cookie":"Cookie:","label_settings":"Settings:","label_selector":"Selector:","label_mobile_disabled":"Mobile Disabled:","label_tablet_disabled":"Tablet Disabled:","label_display_settings":"Display Settings:","label_close_settings":"Close Settings:","label_event_before_open":"Event: Before Open","label_event_after_open":"Event: After Open","label_event_open_prevented":"Event: Open Prevented","label_event_setup_close":"Event: Setup Close","label_event_close_prevented":"Event: Close Prevented","label_event_before_close":"Event: Before Close","label_event_after_close":"Event: After Close","label_event_before_reposition":"Event: Before Reposition","label_event_after_reposition":"Event: After Reposition","label_event_checking_condition":"Event: Checking Condition","triggers":{"click_open":{"name":"Click Open","modal_title":"Click Trigger Settings","settings_column":"<strong>Extra Selectors<\/strong>: {{data.extra_selectors}}"},"auto_open":{"name":"Auto Open","modal_title":"Auto Open Settings","settings_column":"<strong>Delay<\/strong>: {{data.delay}}"}},"cookies":{"on_popup_open":{"name":"On Popup Open","modal_title":"On Popup Open Settings"},"on_popup_close":{"name":"On Popup Close","modal_title":"On Popup Close Settings"},"manual":{"name":"Manual JavaScript","modal_title":"Click Trigger Settings"}}};
var ajaxurl = "https:\/\/www.galpinpremier.com\/wp\/wp-admin\/admin-ajax.php";
var popmake_default_theme = "1395";
/* ]]> */
</script>
<script type='text/javascript' src='/content/plugins/popup-maker/assets/js/site.min.js?defer&#038;ver=1.6.5' defer='defer'></script>
<script type='text/javascript' src='https://www.galpinpremier.com/wp/wp-includes/js/wp-embed.min.js?ver=4.8.2'></script>
        <script>
            (function () {

                var options = null, state = null;

                
                // initial options = {"defaultMediaRange":"large","debug":true,"data":{"footerVersion":2,"buttonRows":[{"showOnMobile":true,"showOnDesktop":false,"leftSideButtons":[{"type":"text-below-icon-button","icon":"dehaze","image":"","text":"","id":"jzl-button-0.24915409841180547","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":false,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":false,"width":0,"widthUnit":"px","style":{"fontSize":"0","padding":"10px 10px 0 10px"},"uiState":[],"url":"#","customEventName":"menu","font":"Material Icons","advancedStyles":false,"disableHoverStyles":true,"transparent":true},{"type":"text-icon-button","text":"GALPIN PREMIER","id":"jazel-a5-header-site-title","visibleOnMobile":true,"showTextOnMobile":true,"url":"\/","enabled":true,"advancedStyles":true,"style":{"fontWeight":"bold","fontSize":"18","fontFamily":"\"Catamaran\", sans-serif","padding":"5px 0","margin":"10px 0 5px 4%","lineHeight":"18"},"uiState":[],"transparent":true,"disableHoverStyles":true,"openInNewWindow":false}],"rightSideButtons":[{"type":"text-below-icon-button","icon":"chat","image":"","text":"","id":"triggerGGChat","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":false,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":false,"width":"40","widthUnit":"px","style":{"fontSize":"0","padding":"10px 0 0 10px","margin":"0 10px 0 0"},"url":"","disableHoverStyles":true,"transparent":true,"font":"Material Icons","advancedStyles":true},{"type":"text-below-icon-button-call","icon":"call","image":"","text":"","id":"jzl-button-0.7266971960372082","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":true,"width":"55","widthUnit":"px","style":{"fontSize":"0","padding":"10px 12px 0 10px","margin":"0"},"url":"","customEventName":"call","font":"Material Icons","transparent":true,"disableHoverStyles":true,"phoneNumbers":[{"department":"Sales","number":"(800) 564-7891"},{"department":"Service","number":"(888) 705-9213"},{"department":"Parts","number":"(888) 721-4839"}]},{"type":"text-icon-button","icon":"","image":"","text":"Espa\u00f1ol","id":"google_translate_element_mobile_2","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":false,"width":0,"widthUnit":"px","style":{"padding":"22px 10px 8px","textColor":"rgba(255, 255, 255, 1)","margin":"0"},"url":"#","transparent":true,"disableHoverStyles":true,"advancedStyles":true,"uiState":{"displayButtonBackgroundColorPicker":false,"displayButtonTextColorPicker":false,"displayButtonBorderColorPicker":false,"displayButtonHoverBackgroundColorPicker":false,"displayButtonHoverTextColorPicker":false,"displayButtonHoverBorderColorPicker":false}}],"showRowSpecificSettings":false}],"backgroundColor":"rgba(51, 51, 51, 1)","textColor":"#FFFFFF","buttonBackgroundColor":"#000000","buttonBackgroundGradientColor":"#FFFFFF","secondBackgroundColor":"rgba(25, 25, 25, 1)","buttonTextColor":"#FFFFFF","buttonBorderColor":"#FFFFFF","buttonHoverBackgroundColor":"#FFFFFF","buttonHoverTextColor":"#FF0000","buttonHoverBorderColor":"#FF0000","buttonVerticalPadding":"10","fontSize":"16","iconFontSize":"32","socialMediaIconHeight":"23","socialMediaIconBackgroundColor":"#FAFAFA","gradient":false,"buttonBorderRadius":"0","buttonBorderThickness":0,"buttonMargin":"10","transitionTime":0,"backgroundGradient":false,"gradientDirection":"to bottom","buttonBackgroundGradient":false,"buttonBackgroundGradientDirection":"to right","positionMode":"header","buttonWidth":"0","buttonWidthUnit":"px","mobileButtonWidth":0,"mobileButtonWidthUnit":"px","slideoutTransitionTime":300,"domNode":[],"showOnDesktop":false,"showOnMobile":true,"showSlideoutPanelSettings":false,"style":{"iconFontSize":"16px","fontSize":"10px"},"freeTextSearch":{"debug":false,"placeholder":"","searchButtonLabel":"Search","searchButtonSearchingLabel":"Search","changeEventName":"","searchEventName":"","srpUrl":"","hideSearchButton":false,"searchButtonIcon":"","searchButtonIconFont":"material-icons","searchButtonIconFontSize":18,"searchButtonIconFontColor":"#FFFFF","autocomplete":true,"accountId":0,"vehicleFilterIds":[],"searchServer":"\/\/search.jazelc.com\/api\/","useTopSearches":false,"topSearchesCount":20,"topSearchesDays":30,"providedTopSearches":[],"enableAnimationOnFocus":false,"suggestionHideTime":300,"enablePageOverlay":false,"useContainerForSizingAutocomplete":false,"isInSpa":false,"autoFocus":false,"enableSiteSearch":false,"maxResultsPerCategory":10,"showCategoryCounts":true,"alwaysOnSorts":[],"alwaysOnSortsSecondary":[],"style":{"input":[],"button":{"backgroundImage":"none"},"container":{"width":"100%"},"inputWrapper":{"display":"inline-block"},"autocompleteDropdown":[],"autocompleteDropdownItem":[],"autocompleteDropdownItemHover":{"backgroundColor":"#000099","color":"white"}}},"scrollBehavior":"hide","cognitoConfig":{"userPoolId":"us-west-2_gs0QIJThR","identityPoolId":"7c7791fa-1575-4a8c-ae03-340869c2daa2","clientId":"1rms7roj4h3fsjg58vg45v5ev7","awsRegion":"us-west-2","tableName":"website_users","usernameSuffix":"","mediaCdnBaseUrl":"\/\/media-cdn.jazelc.com\/","enableFavoriteVehicles":true,"enableCompareVehicles":true,"enableRecentVehicles":true,"allVehiclesSrpUrl":""},"cloudSearchEndpointBaseUrl":"\/\/search.jazelc.com\/api\/"}};
                options = {
                    loggedRequests: [],
                    instantiatedComponents: []                };
                state = JSON.parse("{\"footer\":{\"displayMobileHeaderPhoneNumberDropdown\":false,\"displayFreeTextSearchSlideout\":false,\"settings\":{\"footerVersion\":2,\"buttonRows\":[{\"showOnMobile\":true,\"showOnDesktop\":false,\"leftSideButtons\":[{\"type\":\"text-below-icon-button\",\"icon\":\"dehaze\",\"image\":\"\",\"text\":\"\",\"id\":\"jzl-button-0.24915409841180547\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":false,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":false,\"width\":0,\"widthUnit\":\"px\",\"style\":{\"fontSize\":\"0\",\"padding\":\"10px 10px 0 10px\"},\"uiState\":[],\"url\":\"#\",\"customEventName\":\"menu\",\"font\":\"Material Icons\",\"advancedStyles\":false,\"disableHoverStyles\":true,\"transparent\":true},{\"type\":\"text-icon-button\",\"text\":\"GALPIN PREMIER\",\"id\":\"jazel-a5-header-site-title\",\"visibleOnMobile\":true,\"showTextOnMobile\":true,\"url\":\"\/\",\"enabled\":true,\"advancedStyles\":true,\"style\":{\"fontWeight\":\"bold\",\"fontSize\":\"18\",\"fontFamily\":\"\\\"Catamaran\\\", sans-serif\",\"padding\":\"5px 0\",\"margin\":\"10px 0 5px 4%\",\"lineHeight\":\"18\"},\"uiState\":[],\"transparent\":true,\"disableHoverStyles\":true,\"openInNewWindow\":false}],\"rightSideButtons\":[{\"type\":\"text-below-icon-button\",\"icon\":\"chat\",\"image\":\"\",\"text\":\"\",\"id\":\"triggerGGChat\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":false,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":false,\"width\":\"40\",\"widthUnit\":\"px\",\"style\":{\"fontSize\":\"0\",\"padding\":\"10px 0 0 10px\",\"margin\":\"0 10px 0 0\"},\"url\":\"\",\"disableHoverStyles\":true,\"transparent\":true,\"font\":\"Material Icons\",\"advancedStyles\":true},{\"type\":\"text-below-icon-button-call\",\"icon\":\"call\",\"image\":\"\",\"text\":\"\",\"id\":\"jzl-button-0.7266971960372082\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":true,\"width\":\"55\",\"widthUnit\":\"px\",\"style\":{\"fontSize\":\"0\",\"padding\":\"10px 12px 0 10px\",\"margin\":\"0\"},\"url\":\"\",\"customEventName\":\"call\",\"font\":\"Material Icons\",\"transparent\":true,\"disableHoverStyles\":true,\"phoneNumbers\":[{\"department\":\"Sales\",\"number\":\"(800) 564-7891\"},{\"department\":\"Service\",\"number\":\"(888) 705-9213\"},{\"department\":\"Parts\",\"number\":\"(888) 721-4839\"}]},{\"type\":\"text-icon-button\",\"icon\":\"\",\"image\":\"\",\"text\":\"Espa\u00f1ol\",\"id\":\"google_translate_element_mobile_2\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":false,\"width\":0,\"widthUnit\":\"px\",\"style\":{\"padding\":\"22px 10px 8px\",\"textColor\":\"rgba(255, 255, 255, 1)\",\"margin\":\"0\"},\"url\":\"#\",\"transparent\":true,\"disableHoverStyles\":true,\"advancedStyles\":true,\"uiState\":{\"displayButtonBackgroundColorPicker\":false,\"displayButtonTextColorPicker\":false,\"displayButtonBorderColorPicker\":false,\"displayButtonHoverBackgroundColorPicker\":false,\"displayButtonHoverTextColorPicker\":false,\"displayButtonHoverBorderColorPicker\":false}}],\"showRowSpecificSettings\":false}],\"gradient\":false,\"positionMode\":\"header\",\"mobileButtonWidthUnit\":\"px\",\"domNode\":[],\"showOnDesktop\":false,\"showOnMobile\":true,\"showSlideoutPanelSettings\":false,\"style\":{\"textColor\":\"#FFFFFF\",\"fontSize\":\"16\",\"backgroundColor\":\"rgba(51, 51, 51, 1)\",\"secondBackgroundColor\":\"rgba(25, 25, 25, 1)\",\"gradientDirection\":\"to bottom\",\"backgroundGradient\":false,\"buttonTextColor\":\"#FFFFFF\",\"buttonBackgroundColor\":\"#000000\",\"buttonBackgroundGradient\":false,\"buttonBackgroundGradientColor\":\"#FFFFFF\",\"buttonBackgroundGradientDirection\":\"to right\",\"buttonWidth\":\"0\",\"buttonWidthUnit\":\"px\",\"buttonMargin\":\"10\",\"buttonVerticalPadding\":\"10\",\"buttonBorderColor\":\"#FFFFFF\",\"buttonBorderThickness\":0,\"buttonBorderRadius\":\"0\",\"buttonHoverTextColor\":\"#FF0000\",\"buttonHoverBackgroundColor\":\"#FFFFFF\",\"buttonHoverBorderColor\":\"#FF0000\",\"mobileButtonWidth\":0,\"iconFontSize\":\"32\",\"transitionTime\":0,\"slideoutTransitionTime\":300,\"socialMediaIconHeight\":\"23\",\"socialMediaIconBackgroundColor\":\"#FAFAFA\"},\"freeTextSearch\":{\"debug\":false,\"placeholder\":\"\",\"searchButtonLabel\":\"Search\",\"searchButtonSearchingLabel\":\"Search\",\"changeEventName\":\"\",\"searchEventName\":\"\",\"srpUrl\":\"\",\"hideSearchButton\":false,\"searchButtonIcon\":\"\",\"searchButtonIconFont\":\"material-icons\",\"searchButtonIconFontSize\":18,\"searchButtonIconFontColor\":\"#FFFFF\",\"autocomplete\":true,\"accountId\":0,\"vehicleFilterIds\":[],\"searchServer\":\"\/\/search.jazelc.com\/api\/\",\"useTopSearches\":false,\"topSearchesCount\":20,\"topSearchesDays\":30,\"providedTopSearches\":[],\"enableAnimationOnFocus\":false,\"suggestionHideTime\":300,\"enablePageOverlay\":false,\"useContainerForSizingAutocomplete\":false,\"isInSpa\":false,\"autoFocus\":false,\"enableSiteSearch\":false,\"maxResultsPerCategory\":10,\"showCategoryCounts\":true,\"alwaysOnSorts\":[],\"alwaysOnSortsSecondary\":[],\"style\":{\"input\":[],\"button\":{\"backgroundImage\":\"none\"},\"container\":{\"width\":\"100%\"},\"inputWrapper\":{\"display\":\"inline-block\"},\"autocompleteDropdown\":[],\"autocompleteDropdownItem\":[],\"autocompleteDropdownItemHover\":{\"backgroundColor\":\"#000099\",\"color\":\"white\"}}},\"scrollBehavior\":\"hide\",\"cognitoConfig\":{\"userPoolId\":\"us-west-2_gs0QIJThR\",\"identityPoolId\":\"7c7791fa-1575-4a8c-ae03-340869c2daa2\",\"clientId\":\"1rms7roj4h3fsjg58vg45v5ev7\",\"awsRegion\":\"us-west-2\",\"tableName\":\"website_users\",\"usernameSuffix\":\"\",\"mediaCdnBaseUrl\":\"\/\/media-cdn.jazelc.com\/\",\"enableFavoriteVehicles\":true,\"enableCompareVehicles\":true,\"enableRecentVehicles\":true,\"allVehiclesSrpUrl\":\"\"},\"cloudSearchEndpointBaseUrl\":\"\/\/search.jazelc.com\/api\/\"},\"ui\":{\"displayMobileHeaderPhoneNumberDropdown\":false}},\"freeTextSearch\":{},\"user\":{\"defaultPaymentInfo\":{},\"paymentInfo\":{},\"groupAffiliations\":{\"military\":false,\"student\":false},\"contactInfo\":{\"firstName\":\"\",\"lastName\":\"\",\"email\":\"\",\"phone\":\"\",\"isConfirmed\":false},\"favoriteVehicles\":[],\"compareVehicles\":[],\"recentVehicles\":[],\"isVehiclesInitialized\":false,\"isLoggedIn\":false},\"cognito\":{\"awsRegion\":\"\",\"tableName\":\"\",\"userPoolId\":\"\",\"identityPoolId\":\"\",\"clientId\":\"\",\"vehicleSettings\":{\"enableFavoriteVehicles\":false,\"enableCompareVehicles\":false,\"enableRecentVehicles\":false},\"identityId\":\"\",\"user\":null,\"session\":null},\"matchMedia\":{\"mediaRanges\":[],\"matchedMedia\":[],\"width\":0,\"height\":0}}");

                
                var isInSpa = document.getElementById("srp-app") != null;
                var domNode = document.querySelector("#jazel_mobile_header");
                options.isInSpa = isInSpa;

                JazelAuto5Products.startFooter(options, domNode, null, state);
                domNode.addEventListener(options.searchEventName, function (e) {
                    console.log('Searched for "' + e.detail.searchString + '"');
                });

            })();
        </script>
                <script>
            (function () {

                var options = null, state = null;

                
                // initial options = {"debug":true,"data":{"footerVersion":2,"buttonRows":[{"leftSideButtons":[{"type":"text-below-icon-button","icon":"location_on","image":"","text":"","id":"jzl-button-0.34333765512487147","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":true,"width":"33","widthUnit":"%","style":{"padding":"12px 10px 8px","borderWidth":"0 1px 0 0"},"uiState":[],"url":"\/hours-directions\/","disableHoverStyles":true,"transparent":true,"font":"Material Icons","customEventName":""},{"type":"text-below-icon-button","icon":"B","image":"","text":"","id":"jzl-button-0.8021932659465876","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":true,"width":"33","widthUnit":"%","style":{"borderWidth":"0 1px 0 0","margin":"0","iconFontSize":"0","padding":"12px 10px 8px"},"uiState":[],"url":"\/inventory\/new-vehicles\/","disableHoverStyles":true,"transparent":true,"font":"auto5-font","advancedStyles":false,"customEventName":"shop"},{"type":"text-below-icon-button","icon":"translate","image":"","text":"","id":"google_translate_element_mobile_2","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":false,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":true,"width":"33","widthUnit":"%","style":{"borderWidth":"0","margin":"0","iconFontSize":"0","padding":"12px 10px 8px"},"uiState":[],"url":"#","disableHoverStyles":true,"transparent":true,"font":"Material Icons"},{"type":"text-below-icon-button","icon":"build","image":"","text":"","id":"jzl-button-0.24047116491148857","visibleOnMobile":true,"openInNewWindow":false,"showTextOnMobile":true,"enabled":true,"boldChatAccountId":"","boldChatWebsiteDefId":"","boldChatCustomUrl":"","boldChatWindowParameters":"","boldChatBDID":"","boldChatImpressionEventName":"jazel-boldchat-impression","customWidth":true,"width":"33","widthUnit":"%","style":{"padding":"12px 10px 8px","textColor":"rgba(255, 255, 255, 1)"},"uiState":[],"url":"\/schedule-service\/","disableHoverStyles":true,"transparent":true,"font":"Material Icons"}],"rightSideButtons":[],"showOnDesktop":false,"showOnMobile":true,"showRowSpecificSettings":true}],"backgroundColor":"rgba(51, 51, 51, 1)","textColor":"#FFFFFF","buttonBackgroundColor":"rgba(0, 0, 0, 1)","buttonBackgroundGradientColor":"#FFFFFF","secondBackgroundColor":"rgba(25, 25, 25, 1)","buttonTextColor":"#FFFFFF","buttonBorderColor":"rgba(120, 120, 120, 1)","buttonHoverBackgroundColor":"#FFFFFF","buttonHoverTextColor":"#FF0000","buttonHoverBorderColor":"#FF0000","buttonVerticalPadding":"12","fontSize":"0","iconFontSize":"26","socialMediaIconHeight":"32","socialMediaIconBackgroundColor":"#FAFAFA","gradient":false,"buttonBorderRadius":"0","buttonBorderThickness":"0","buttonMargin":"20","transitionTime":300,"backgroundGradient":false,"gradientDirection":"to bottom","buttonBackgroundGradient":false,"buttonBackgroundGradientDirection":"to right","positionMode":"footer","buttonWidth":0,"buttonWidthUnit":"px","mobileButtonWidth":0,"mobileButtonWidthUnit":"px","slideoutTransitionTime":300,"domNode":[],"style":{"iconFontSize":"16px","fontSize":"10px"},"freeTextSearch":{"debug":false,"placeholder":"","searchButtonLabel":"Search","searchButtonSearchingLabel":"Search","changeEventName":"","searchEventName":"","srpUrl":"","hideSearchButton":false,"searchButtonIcon":"","searchButtonIconFont":"material-icons","searchButtonIconFontSize":18,"searchButtonIconFontColor":"#FFFFF","autocomplete":true,"accountId":0,"vehicleFilterIds":[],"searchServer":"\/\/search.jazelc.com\/api\/","useTopSearches":false,"topSearchesCount":20,"topSearchesDays":30,"providedTopSearches":[],"enableAnimationOnFocus":false,"suggestionHideTime":300,"enablePageOverlay":false,"useContainerForSizingAutocomplete":false,"isInSpa":false,"autoFocus":false,"enableSiteSearch":false,"maxResultsPerCategory":10,"showCategoryCounts":true,"alwaysOnSorts":[],"alwaysOnSortsSecondary":[],"style":{"input":[],"button":{"backgroundImage":"none"},"container":{"width":"100%"},"inputWrapper":{"display":"inline-block"},"autocompleteDropdown":[],"autocompleteDropdownItem":[],"autocompleteDropdownItemHover":{"backgroundColor":"#000099","color":"white"}}},"scrollBehavior":"hide","showOnMobile":true,"cloudSearchEndpointBaseUrl":"\/\/search.jazelc.com\/api\/"},"defaultMediaRange":"large"};
                options = {
                    loggedRequests: [],
                    instantiatedComponents: []                };
                state = JSON.parse("{\"footer\":{\"displayMobileHeaderPhoneNumberDropdown\":false,\"displayFreeTextSearchSlideout\":false,\"settings\":{\"footerVersion\":2,\"buttonRows\":[{\"leftSideButtons\":[{\"type\":\"text-below-icon-button\",\"icon\":\"location_on\",\"image\":\"\",\"text\":\"\",\"id\":\"jzl-button-0.34333765512487147\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":true,\"width\":\"33\",\"widthUnit\":\"%\",\"style\":{\"padding\":\"12px 10px 8px\",\"borderWidth\":\"0 1px 0 0\"},\"uiState\":[],\"url\":\"\/hours-directions\/\",\"disableHoverStyles\":true,\"transparent\":true,\"font\":\"Material Icons\",\"customEventName\":\"\"},{\"type\":\"text-below-icon-button\",\"icon\":\"B\",\"image\":\"\",\"text\":\"\",\"id\":\"jzl-button-0.8021932659465876\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":true,\"width\":\"33\",\"widthUnit\":\"%\",\"style\":{\"borderWidth\":\"0 1px 0 0\",\"margin\":\"0\",\"iconFontSize\":\"0\",\"padding\":\"12px 10px 8px\"},\"uiState\":[],\"url\":\"\/inventory\/new-vehicles\/\",\"disableHoverStyles\":true,\"transparent\":true,\"font\":\"auto5-font\",\"advancedStyles\":false,\"customEventName\":\"shop\"},{\"type\":\"text-below-icon-button\",\"icon\":\"translate\",\"image\":\"\",\"text\":\"\",\"id\":\"google_translate_element_mobile_2\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":false,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":true,\"width\":\"33\",\"widthUnit\":\"%\",\"style\":{\"borderWidth\":\"0\",\"margin\":\"0\",\"iconFontSize\":\"0\",\"padding\":\"12px 10px 8px\"},\"uiState\":[],\"url\":\"#\",\"disableHoverStyles\":true,\"transparent\":true,\"font\":\"Material Icons\"},{\"type\":\"text-below-icon-button\",\"icon\":\"build\",\"image\":\"\",\"text\":\"\",\"id\":\"jzl-button-0.24047116491148857\",\"visibleOnMobile\":true,\"openInNewWindow\":false,\"showTextOnMobile\":true,\"enabled\":true,\"boldChatAccountId\":\"\",\"boldChatWebsiteDefId\":\"\",\"boldChatCustomUrl\":\"\",\"boldChatWindowParameters\":\"\",\"boldChatBDID\":\"\",\"boldChatImpressionEventName\":\"jazel-boldchat-impression\",\"customWidth\":true,\"width\":\"33\",\"widthUnit\":\"%\",\"style\":{\"padding\":\"12px 10px 8px\",\"textColor\":\"rgba(255, 255, 255, 1)\"},\"uiState\":[],\"url\":\"\/schedule-service\/\",\"disableHoverStyles\":true,\"transparent\":true,\"font\":\"Material Icons\"}],\"rightSideButtons\":[],\"showOnDesktop\":false,\"showOnMobile\":true,\"showRowSpecificSettings\":true}],\"gradient\":false,\"positionMode\":\"footer\",\"mobileButtonWidthUnit\":\"px\",\"domNode\":[],\"style\":{\"textColor\":\"#FFFFFF\",\"fontSize\":\"0\",\"backgroundColor\":\"rgba(51, 51, 51, 1)\",\"secondBackgroundColor\":\"rgba(25, 25, 25, 1)\",\"gradientDirection\":\"to bottom\",\"backgroundGradient\":false,\"buttonTextColor\":\"#FFFFFF\",\"buttonBackgroundColor\":\"rgba(0, 0, 0, 1)\",\"buttonBackgroundGradient\":false,\"buttonBackgroundGradientColor\":\"#FFFFFF\",\"buttonBackgroundGradientDirection\":\"to right\",\"buttonWidth\":0,\"buttonWidthUnit\":\"px\",\"buttonMargin\":\"20\",\"buttonVerticalPadding\":\"12\",\"buttonBorderColor\":\"rgba(120, 120, 120, 1)\",\"buttonBorderThickness\":\"0\",\"buttonBorderRadius\":\"0\",\"buttonHoverTextColor\":\"#FF0000\",\"buttonHoverBackgroundColor\":\"#FFFFFF\",\"buttonHoverBorderColor\":\"#FF0000\",\"mobileButtonWidth\":0,\"iconFontSize\":\"26\",\"transitionTime\":300,\"slideoutTransitionTime\":300,\"socialMediaIconHeight\":\"32\",\"socialMediaIconBackgroundColor\":\"#FAFAFA\"},\"freeTextSearch\":{\"debug\":false,\"placeholder\":\"\",\"searchButtonLabel\":\"Search\",\"searchButtonSearchingLabel\":\"Search\",\"changeEventName\":\"\",\"searchEventName\":\"\",\"srpUrl\":\"\",\"hideSearchButton\":false,\"searchButtonIcon\":\"\",\"searchButtonIconFont\":\"material-icons\",\"searchButtonIconFontSize\":18,\"searchButtonIconFontColor\":\"#FFFFF\",\"autocomplete\":true,\"accountId\":0,\"vehicleFilterIds\":[],\"searchServer\":\"\/\/search.jazelc.com\/api\/\",\"useTopSearches\":false,\"topSearchesCount\":20,\"topSearchesDays\":30,\"providedTopSearches\":[],\"enableAnimationOnFocus\":false,\"suggestionHideTime\":300,\"enablePageOverlay\":false,\"useContainerForSizingAutocomplete\":false,\"isInSpa\":false,\"autoFocus\":false,\"enableSiteSearch\":false,\"maxResultsPerCategory\":10,\"showCategoryCounts\":true,\"alwaysOnSorts\":[],\"alwaysOnSortsSecondary\":[],\"style\":{\"input\":[],\"button\":{\"backgroundImage\":\"none\"},\"container\":{\"width\":\"100%\"},\"inputWrapper\":{\"display\":\"inline-block\"},\"autocompleteDropdown\":[],\"autocompleteDropdownItem\":[],\"autocompleteDropdownItemHover\":{\"backgroundColor\":\"#000099\",\"color\":\"white\"}}},\"scrollBehavior\":\"hide\",\"showOnMobile\":true,\"cloudSearchEndpointBaseUrl\":\"\/\/search.jazelc.com\/api\/\"},\"ui\":{\"displayMobileHeaderPhoneNumberDropdown\":false}},\"freeTextSearch\":{},\"user\":{\"defaultPaymentInfo\":{},\"paymentInfo\":{},\"groupAffiliations\":{\"military\":false,\"student\":false},\"contactInfo\":{\"firstName\":\"\",\"lastName\":\"\",\"email\":\"\",\"phone\":\"\",\"isConfirmed\":false},\"favoriteVehicles\":[],\"compareVehicles\":[],\"recentVehicles\":[],\"isVehiclesInitialized\":false,\"isLoggedIn\":false},\"cognito\":{\"awsRegion\":\"\",\"tableName\":\"\",\"userPoolId\":\"\",\"identityPoolId\":\"\",\"clientId\":\"\",\"vehicleSettings\":{\"enableFavoriteVehicles\":false,\"enableCompareVehicles\":false,\"enableRecentVehicles\":false},\"identityId\":\"\",\"user\":null,\"session\":null},\"matchMedia\":{\"mediaRanges\":[],\"matchedMedia\":[],\"width\":0,\"height\":0}}");

                
                var isInSpa = document.getElementById("srp-app") != null;
                var domNode = document.querySelector("#jazel_mobile_footer");
                options.isInSpa = isInSpa;

                JazelAuto5Products.startFooter(options, domNode, null, state);
                domNode.addEventListener(options.searchEventName, function (e) {
                    console.log('Searched for "' + e.detail.searchString + '"');
                });

            })();
        </script>
        <div id='Gravity18' class="a5-eprice-form">    <div class="srp-eprice-form-wrapper">
                <div class="eprice-form-top-part">
            <div class="hook-lead-header">
<div class="hook-lead-title">LOCK IN THIS E-PRICE</div>
<div class="hook-lead-header-body">Buying soon? Complete this short form and we will send you today's e-price.</div>
</div>        </div>
                <div class="eprice-form-bottom-part">
                        <div class="vehicle-area">
                <div class="data-area">
                    <div class="current-vehicle-name"><span class="value" data-vehicle-field="name"></span></div>
                </div>
                <div class="content-area">
                    <div class="photo-area">
                        <img class="current-vehicle-image" src="/content/plugins/jzl-auto5-products/images/no-vehicle-image.png">
                    </div>
                    <div class="data-area">
                        <div class="current-vehicle-ext-color"><span class="label">Ext Color:</span> <span class="value" data-vehicle-field="ext_color"></span></div>
                        <div class="current-vehicle-transmission"><span class="label">Transmission:</span> <span class="value" data-vehicle-field="transmission"></span></div>
                        <div class="current-vehicle-mileage"><span class="label">Mileage:</span> <span class="value" data-vehicle-field="mileage"></span></div>
                        <div class="current-vehicle-stock"><span class="label">Stock:</span> <span class="value" data-vehicle-field="stock_no"></span></div>
                        <div class="current-vehicle-drivetrain"><span class="label">Drivetrain:</span> <span class="value" data-vehicle-field="drivetrain"></span></div>
                        <div class="current-vehicle-engine"><span class="label">Engine:</span> <span class="value" data-vehicle-field="engine"></span></div>
                        <div class="current-vehicle-vin"><span class="label">VIN:</span> <span class="value" data-vehicle-field="vin"></span></div>
                    </div>
                </div>
            </div>
                        <div class="form-area">
                <div class='gf_browser_chrome gform_wrapper' id='gform_wrapper_18' ><a id='gf_18' class='gform_anchor' ></a><form method='post' enctype='multipart/form-data' target='gform_ajax_frame_18' id='gform_18'  action='/inventory/new-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA#gf_18'> 
 <input type='hidden' class='gforms-pum' value='{"closepopup":false,"closedelay":0,"openpopup":false,"openpopup_id":0}' />
                        <div class='gform_heading'>
                            <h3 class='gform_title'>Get E-Price </h3>
                            <span class='gform_description'>Contact Information</span>
                        </div>
                        <div class='gform_body'><ul id='gform_fields_18' class='gform_fields top_label form_sublabel_below description_below'><li id='field_18_6' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_18_6' >First Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_6' id='input_18_6' type='text' value='' class='large'  tabindex='1'   /></div></li><li id='field_18_7' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_18_7' >Last Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_7' id='input_18_7' type='text' value='' class='large'  tabindex='2'   /></div></li><li id='field_18_3' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_18_3' >Email<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_email'>
                            <input name='input_3' id='input_18_3' type='text' value='' class='large' tabindex='3'   />
                        </div></li><li id='field_18_2' class='gfield column one-second field_sublabel_below field_description_below' ><label class='gfield_label' for='input_18_2' >Phone</label><div class='ginput_container ginput_container_phone'><input name='input_2' id='input_18_2' type='text' value='' class='large' tabindex='4'   /></div></li><li id='field_18_5' class='gfield field_sublabel_below field_description_below' >        <div class="ginput_complex ginput_container ginput_container_vehicle_data">
                        <input type="hidden"
                   id="input_18_5_1"
                   name="input_5.1"
                   data-vehicle-data-type="year"
            />
                            <input type="hidden"
                   id="input_18_5_2"
                   name="input_5.2"
                   data-vehicle-data-type="make"
            />
                            <input type="hidden"
                   id="input_18_5_3"
                   name="input_5.3"
                   data-vehicle-data-type="model"
            />
                            <input type="hidden"
                   id="input_18_5_4"
                   name="input_5.4"
                   data-vehicle-data-type="trim"
            />
                            <input type="hidden"
                   id="input_18_5_5"
                   name="input_5.5"
                   data-vehicle-data-type="new_or_used"
            />
                            <input type="hidden"
                   id="input_18_5_6"
                   name="input_5.6"
                   data-vehicle-data-type="ext_color"
            />
                            <input type="hidden"
                   id="input_18_5_7"
                   name="input_5.7"
                   data-vehicle-data-type="vin"
            />
                            <input type="hidden"
                   id="input_18_5_8"
                   name="input_5.8"
                   data-vehicle-data-type="price"
            />
                            <input type="hidden"
                   id="input_18_5_9"
                   name="input_5.9"
                   data-vehicle-data-type="vdp"
            />
                            <input type="hidden"
                   id="input_18_5_11"
                   name="input_5.11"
                   data-vehicle-data-type="stock_no"
            />
                            <input type="hidden"
                   id="input_18_5_12"
                   name="input_5.12"
                   data-vehicle-data-type="vehicle_id"
            />
                            <input type="hidden"
                   id="input_18_5_13"
                   name="input_5.13"
                   data-vehicle-data-type="account_name"
            />
                            <input type="hidden"
                   id="input_18_5_14"
                   name="input_5.14"
                   data-vehicle-data-type="address"
            />
                            <input type="hidden"
                   id="input_18_5_15"
                   name="input_5.15"
                   data-vehicle-data-type="body_style"
            />
                            <input type="hidden"
                   id="input_18_5_16"
                   name="input_5.16"
                   data-vehicle-data-type="transmission"
            />
                            <input type="hidden"
                   id="input_18_5_17"
                   name="input_5.17"
                   data-vehicle-data-type="mileage"
            />
                            <input type="hidden"
                   id="input_18_5_18"
                   name="input_5.18"
                   data-vehicle-data-type="int_color"
            />
                        </div>
        </li><li id='field_18_8' class='gfield gform_validation_container field_sublabel_below field_description_below' ><label class='gfield_label' for='input_18_8' >Email</label><div class='ginput_container'><input name='input_8' id='input_18_8' type='text' value='' /></div><div class='gfield_description'>This field is for validation purposes and should be left unchanged.</div></li>
                            </ul></div>
        <div class='gform_footer top_label'> <input type='submit' id='gform_submit_button_18' class='gform_button button' value='Send' tabindex='5' onclick='if(window["gf_submitting_18"]){return false;}  window["gf_submitting_18"]=true;  ' /> <input type='hidden' name='gform_ajax' value='form_id=18&amp;title=1&amp;description=1&amp;tabindex=1' />
            <input type='hidden' class='gform_hidden' name='is_submit_18' value='1' />
            <input type='hidden' class='gform_hidden' name='gform_submit' value='18' />
            
            <input type='hidden' class='gform_hidden' name='gform_unique_id' value='' />
            <input type='hidden' class='gform_hidden' name='state_18' value='WyJbXSIsImFjYWNkODE0MTg0ZGE5OGVmMTkzM2ZmZGUyNjVjNmVjIl0=' />
            <input type='hidden' class='gform_hidden' name='gform_target_page_number_18' id='gform_target_page_number_18' value='0' />
            <input type='hidden' class='gform_hidden' name='gform_source_page_number_18' id='gform_source_page_number_18' value='1' />
            <input type='hidden' name='gform_field_values' value='' />
            
        </div>
                        </form>
                        </div>
                <iframe style='display:none;width:0px;height:0px;' src='about:blank' name='gform_ajax_frame_18' id='gform_ajax_frame_18'></iframe>
                <script type='text/javascript'>jQuery(document).ready(function($){gformInitSpinner( 18, '/content/plugins/gravityforms/images/spinner.gif' );jQuery('#gform_ajax_frame_18').load( function(){var contents = jQuery(this).contents().find('*').html();var is_postback = contents.indexOf('GF_AJAX_POSTBACK') >= 0;if(!is_postback){return;}var form_content = jQuery(this).contents().find('#gform_wrapper_18');var is_confirmation = jQuery(this).contents().find('#gform_confirmation_wrapper_18').length > 0;var is_redirect = contents.indexOf('gformRedirect(){') >= 0;var is_form = form_content.length > 0 && ! is_redirect && ! is_confirmation;if(is_form){jQuery('#gform_wrapper_18').html(form_content.html());setTimeout( function() { /* delay the scroll by 50 milliseconds to fix a bug in chrome */ jQuery(document).scrollTop(jQuery('#gform_wrapper_18').offset().top); }, 50 );if(window['gformInitDatepicker']) {gformInitDatepicker();}if(window['gformInitPriceFields']) {gformInitPriceFields();}var current_page = jQuery('#gform_source_page_number_18').val();gformInitSpinner( 18, '/content/plugins/gravityforms/images/spinner.gif' );jQuery(document).trigger('gform_page_loaded', [18, current_page]);window['gf_submitting_18'] = false;}else if(!is_redirect){var confirmation_content = jQuery(this).contents().find('#gforms_confirmation_message_18').html();if(!confirmation_content){confirmation_content = contents;}setTimeout(function(){jQuery('#gform_wrapper_18').replaceWith('<' + 'div id=\'gforms_confirmation_message_18\' class=\'gform_confirmation_message_18 gforms_confirmation_message\'' + '>' + confirmation_content + '<' + '/div' + '>');jQuery(document).scrollTop(jQuery('#gforms_confirmation_message_18').offset().top);jQuery(document).trigger('gform_confirmation_loaded', [18]);window['gf_submitting_18'] = false;}, 50);}else{jQuery('#gform_18').append(contents);if(window['gformRedirect']) {gformRedirect();}}jQuery(document).trigger('gform_post_render', [18, current_page]);} );} );</script><script type='text/javascript'> if(typeof gf_global == 'undefined') var gf_global = {"gf_currency_config":{"name":"U.S. Dollar","symbol_left":"$","symbol_right":"","symbol_padding":"","thousand_separator":",","decimal_separator":".","decimals":2},"base_url":"\/content\/plugins\/gravityforms","number_formats":[],"spinnerUrl":"\/content\/plugins\/gravityforms\/images\/spinner.gif"};jQuery(document).bind('gform_post_render', function(event, formId, currentPage){if(formId == 18) {if(!/(android)/i.test(navigator.userAgent)){jQuery('#input_18_2').mask('(999) 999-9999').bind('keypress', function(e){if(e.which == 13){jQuery(this).blur();} } );}} } );jQuery(document).bind('gform_post_conditional_logic', function(event, formId, fields, isInit){} );</script><script type='text/javascript'> jQuery(document).ready(function(){jQuery(document).trigger('gform_post_render', [18, 1]) } ); </script></div>
        </div>
    </div>

    </div><div id='Gravity19' class="a5-eprice-form">    <div class="srp-eprice-form-wrapper">
                <div class="eprice-form-top-part">
            <div class="hook-lead-header">
<div class="hook-lead-title">LOCK IN THIS E-PRICE</div>
<div class="hook-lead-header-body">Buying soon? Complete this short form and we will send you today's e-price.</div>
</div>        </div>
                <div class="eprice-form-bottom-part">
                        <div class="vehicle-area">
                <div class="data-area">
                    <div class="current-vehicle-name"><span class="value" data-vehicle-field="name"></span></div>
                </div>
                <div class="content-area">
                    <div class="photo-area">
                        <img class="current-vehicle-image" src="/content/plugins/jzl-auto5-products/images/no-vehicle-image.png">
                    </div>
                    <div class="data-area">
                        <div class="current-vehicle-ext-color"><span class="label">Ext Color:</span> <span class="value" data-vehicle-field="ext_color"></span></div>
                        <div class="current-vehicle-transmission"><span class="label">Transmission:</span> <span class="value" data-vehicle-field="transmission"></span></div>
                        <div class="current-vehicle-mileage"><span class="label">Mileage:</span> <span class="value" data-vehicle-field="mileage"></span></div>
                        <div class="current-vehicle-stock"><span class="label">Stock:</span> <span class="value" data-vehicle-field="stock_no"></span></div>
                        <div class="current-vehicle-drivetrain"><span class="label">Drivetrain:</span> <span class="value" data-vehicle-field="drivetrain"></span></div>
                        <div class="current-vehicle-engine"><span class="label">Engine:</span> <span class="value" data-vehicle-field="engine"></span></div>
                        <div class="current-vehicle-vin"><span class="label">VIN:</span> <span class="value" data-vehicle-field="vin"></span></div>
                    </div>
                </div>
            </div>
                        <div class="form-area">
                <div class='gf_browser_chrome gform_wrapper' id='gform_wrapper_19' ><a id='gf_19' class='gform_anchor' ></a><form method='post' enctype='multipart/form-data' target='gform_ajax_frame_19' id='gform_19'  action='/inventory/new-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA#gf_19'> 
 <input type='hidden' class='gforms-pum' value='{"closepopup":false,"closedelay":0,"openpopup":false,"openpopup_id":0}' />
                        <div class='gform_heading'>
                            <h3 class='gform_title'>Get E-Price </h3>
                            <span class='gform_description'>Contact Information</span>
                        </div>
                        <div class='gform_body'><ul id='gform_fields_19' class='gform_fields top_label form_sublabel_below description_below'><li id='field_19_6' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_19_6' >First Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_6' id='input_19_6' type='text' value='' class='large'  tabindex='1'   /></div></li><li id='field_19_7' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_19_7' >Last Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_7' id='input_19_7' type='text' value='' class='large'  tabindex='2'   /></div></li><li id='field_19_3' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_19_3' >Email<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_email'>
                            <input name='input_3' id='input_19_3' type='text' value='' class='large' tabindex='3'   />
                        </div></li><li id='field_19_2' class='gfield column one-second field_sublabel_below field_description_below' ><label class='gfield_label' for='input_19_2' >Phone</label><div class='ginput_container ginput_container_phone'><input name='input_2' id='input_19_2' type='text' value='' class='large' tabindex='4'   /></div></li><li id='field_19_5' class='gfield field_sublabel_below field_description_below' >        <div class="ginput_complex ginput_container ginput_container_vehicle_data">
                        <input type="hidden"
                   id="input_19_5_1"
                   name="input_5.1"
                   data-vehicle-data-type="year"
            />
                            <input type="hidden"
                   id="input_19_5_2"
                   name="input_5.2"
                   data-vehicle-data-type="make"
            />
                            <input type="hidden"
                   id="input_19_5_3"
                   name="input_5.3"
                   data-vehicle-data-type="model"
            />
                            <input type="hidden"
                   id="input_19_5_4"
                   name="input_5.4"
                   data-vehicle-data-type="trim"
            />
                            <input type="hidden"
                   id="input_19_5_5"
                   name="input_5.5"
                   data-vehicle-data-type="new_or_used"
            />
                            <input type="hidden"
                   id="input_19_5_6"
                   name="input_5.6"
                   data-vehicle-data-type="ext_color"
            />
                            <input type="hidden"
                   id="input_19_5_7"
                   name="input_5.7"
                   data-vehicle-data-type="vin"
            />
                            <input type="hidden"
                   id="input_19_5_8"
                   name="input_5.8"
                   data-vehicle-data-type="price"
            />
                            <input type="hidden"
                   id="input_19_5_9"
                   name="input_5.9"
                   data-vehicle-data-type="vdp"
            />
                            <input type="hidden"
                   id="input_19_5_11"
                   name="input_5.11"
                   data-vehicle-data-type="stock_no"
            />
                            <input type="hidden"
                   id="input_19_5_12"
                   name="input_5.12"
                   data-vehicle-data-type="vehicle_id"
            />
                            <input type="hidden"
                   id="input_19_5_13"
                   name="input_5.13"
                   data-vehicle-data-type="account_name"
            />
                            <input type="hidden"
                   id="input_19_5_14"
                   name="input_5.14"
                   data-vehicle-data-type="address"
            />
                            <input type="hidden"
                   id="input_19_5_15"
                   name="input_5.15"
                   data-vehicle-data-type="body_style"
            />
                            <input type="hidden"
                   id="input_19_5_16"
                   name="input_5.16"
                   data-vehicle-data-type="transmission"
            />
                            <input type="hidden"
                   id="input_19_5_17"
                   name="input_5.17"
                   data-vehicle-data-type="mileage"
            />
                            <input type="hidden"
                   id="input_19_5_18"
                   name="input_5.18"
                   data-vehicle-data-type="int_color"
            />
                        </div>
        </li><li id='field_19_8' class='gfield gform_validation_container field_sublabel_below field_description_below' ><label class='gfield_label' for='input_19_8' >Phone</label><div class='ginput_container'><input name='input_8' id='input_19_8' type='text' value='' /></div><div class='gfield_description'>This field is for validation purposes and should be left unchanged.</div></li>
                            </ul></div>
        <div class='gform_footer top_label'> <input type='submit' id='gform_submit_button_19' class='gform_button button' value='Send' tabindex='5' onclick='if(window["gf_submitting_19"]){return false;}  window["gf_submitting_19"]=true;  ' /> <input type='hidden' name='gform_ajax' value='form_id=19&amp;title=1&amp;description=1&amp;tabindex=1' />
            <input type='hidden' class='gform_hidden' name='is_submit_19' value='1' />
            <input type='hidden' class='gform_hidden' name='gform_submit' value='19' />
            
            <input type='hidden' class='gform_hidden' name='gform_unique_id' value='' />
            <input type='hidden' class='gform_hidden' name='state_19' value='WyJbXSIsImFjYWNkODE0MTg0ZGE5OGVmMTkzM2ZmZGUyNjVjNmVjIl0=' />
            <input type='hidden' class='gform_hidden' name='gform_target_page_number_19' id='gform_target_page_number_19' value='0' />
            <input type='hidden' class='gform_hidden' name='gform_source_page_number_19' id='gform_source_page_number_19' value='1' />
            <input type='hidden' name='gform_field_values' value='' />
            
        </div>
                        </form>
                        </div>
                <iframe style='display:none;width:0px;height:0px;' src='about:blank' name='gform_ajax_frame_19' id='gform_ajax_frame_19'></iframe>
                <script type='text/javascript'>jQuery(document).ready(function($){gformInitSpinner( 19, '/content/plugins/gravityforms/images/spinner.gif' );jQuery('#gform_ajax_frame_19').load( function(){var contents = jQuery(this).contents().find('*').html();var is_postback = contents.indexOf('GF_AJAX_POSTBACK') >= 0;if(!is_postback){return;}var form_content = jQuery(this).contents().find('#gform_wrapper_19');var is_confirmation = jQuery(this).contents().find('#gform_confirmation_wrapper_19').length > 0;var is_redirect = contents.indexOf('gformRedirect(){') >= 0;var is_form = form_content.length > 0 && ! is_redirect && ! is_confirmation;if(is_form){jQuery('#gform_wrapper_19').html(form_content.html());setTimeout( function() { /* delay the scroll by 50 milliseconds to fix a bug in chrome */ jQuery(document).scrollTop(jQuery('#gform_wrapper_19').offset().top); }, 50 );if(window['gformInitDatepicker']) {gformInitDatepicker();}if(window['gformInitPriceFields']) {gformInitPriceFields();}var current_page = jQuery('#gform_source_page_number_19').val();gformInitSpinner( 19, '/content/plugins/gravityforms/images/spinner.gif' );jQuery(document).trigger('gform_page_loaded', [19, current_page]);window['gf_submitting_19'] = false;}else if(!is_redirect){var confirmation_content = jQuery(this).contents().find('#gforms_confirmation_message_19').html();if(!confirmation_content){confirmation_content = contents;}setTimeout(function(){jQuery('#gform_wrapper_19').replaceWith('<' + 'div id=\'gforms_confirmation_message_19\' class=\'gform_confirmation_message_19 gforms_confirmation_message\'' + '>' + confirmation_content + '<' + '/div' + '>');jQuery(document).scrollTop(jQuery('#gforms_confirmation_message_19').offset().top);jQuery(document).trigger('gform_confirmation_loaded', [19]);window['gf_submitting_19'] = false;}, 50);}else{jQuery('#gform_19').append(contents);if(window['gformRedirect']) {gformRedirect();}}jQuery(document).trigger('gform_post_render', [19, current_page]);} );} );</script><script type='text/javascript'> if(typeof gf_global == 'undefined') var gf_global = {"gf_currency_config":{"name":"U.S. Dollar","symbol_left":"$","symbol_right":"","symbol_padding":"","thousand_separator":",","decimal_separator":".","decimals":2},"base_url":"\/content\/plugins\/gravityforms","number_formats":[],"spinnerUrl":"\/content\/plugins\/gravityforms\/images\/spinner.gif"};jQuery(document).bind('gform_post_render', function(event, formId, currentPage){if(formId == 19) {if(!/(android)/i.test(navigator.userAgent)){jQuery('#input_19_2').mask('(999) 999-9999').bind('keypress', function(e){if(e.which == 13){jQuery(this).blur();} } );}} } );jQuery(document).bind('gform_post_conditional_logic', function(event, formId, fields, isInit){} );</script><script type='text/javascript'> jQuery(document).ready(function(){jQuery(document).trigger('gform_post_render', [19, 1]) } ); </script></div>
        </div>
    </div>

    </div><div id='a5-redeem-incentive-form' class="a5-redeem-incentive-form">
                <div class='gf_browser_chrome gform_wrapper' id='gform_wrapper_31' ><a id='gf_31' class='gform_anchor' ></a><form method='post' enctype='multipart/form-data' target='gform_ajax_frame_31' id='gform_31'  action='/inventory/new-vehicles/vehicle/YV4162UK3K2134791/2019-Volvo-XC40-Van-Nuys-CA#gf_31'> 
 <input type='hidden' class='gforms-pum' value='{"closepopup":false,"closedelay":0,"openpopup":false,"openpopup_id":0}' />
                        <div class='gform_heading'>
                            <h3 class='gform_title'>Redeem Your Offer </h3>
                            <span class='gform_description'>Fill out the form below to redeem your offer so we can contact you as soon as possible.</span>
                        </div>
                        <div class='gform_body'><ul id='gform_fields_31' class='gform_fields top_label form_sublabel_below description_below'><li id='field_31_6' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_6' >First Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_6' id='input_31_6' type='text' value='' class='large'  tabindex='1'   /></div></li><li id='field_31_7' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_7' >Last Name<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_text'><input name='input_7' id='input_31_7' type='text' value='' class='large'  tabindex='2'   /></div></li><li id='field_31_3' class='gfield column one-second gfield_contains_required field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_3' >Email<span class='gfield_required'>*</span></label><div class='ginput_container ginput_container_email'>
                            <input name='input_3' id='input_31_3' type='text' value='' class='large' tabindex='3'   />
                        </div></li><li id='field_31_2' class='gfield column one-second field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_2' >Phone</label><div class='ginput_container ginput_container_phone'><input name='input_2' id='input_31_2' type='text' value='' class='large' tabindex='4'   /></div></li><li id='field_31_4' class='gfield field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_4' >Comments</label><div class='ginput_container ginput_container_textarea'>
					<textarea name='input_4' id='input_31_4' class='textarea medium' tabindex='5'    rows='10' cols='50'></textarea>
				</div></li><li id='field_31_5' class='gfield field_sublabel_below field_description_below' >        <div class="ginput_complex ginput_container ginput_container_vehicle_data">
                        <input type="hidden"
                   id="input_31_5_1"
                   name="input_5.1"
                   data-vehicle-data-type="year"
            />
                            <input type="hidden"
                   id="input_31_5_2"
                   name="input_5.2"
                   data-vehicle-data-type="make"
            />
                            <input type="hidden"
                   id="input_31_5_3"
                   name="input_5.3"
                   data-vehicle-data-type="model"
            />
                            <input type="hidden"
                   id="input_31_5_4"
                   name="input_5.4"
                   data-vehicle-data-type="trim"
            />
                            <input type="hidden"
                   id="input_31_5_5"
                   name="input_5.5"
                   data-vehicle-data-type="new_or_used"
            />
                            <input type="hidden"
                   id="input_31_5_6"
                   name="input_5.6"
                   data-vehicle-data-type="ext_color"
            />
                            <input type="hidden"
                   id="input_31_5_7"
                   name="input_5.7"
                   data-vehicle-data-type="vin"
            />
                            <input type="hidden"
                   id="input_31_5_8"
                   name="input_5.8"
                   data-vehicle-data-type="price"
            />
                            <input type="hidden"
                   id="input_31_5_9"
                   name="input_5.9"
                   data-vehicle-data-type="vdp"
            />
                            <input type="hidden"
                   id="input_31_5_11"
                   name="input_5.11"
                   data-vehicle-data-type="stock_no"
            />
                            <input type="hidden"
                   id="input_31_5_12"
                   name="input_5.12"
                   data-vehicle-data-type="vehicle_id"
            />
                            <input type="hidden"
                   id="input_31_5_13"
                   name="input_5.13"
                   data-vehicle-data-type="account_name"
            />
                            <input type="hidden"
                   id="input_31_5_14"
                   name="input_5.14"
                   data-vehicle-data-type="address"
            />
                            <input type="hidden"
                   id="input_31_5_15"
                   name="input_5.15"
                   data-vehicle-data-type="body_style"
            />
                            <input type="hidden"
                   id="input_31_5_16"
                   name="input_5.16"
                   data-vehicle-data-type="transmission"
            />
                            <input type="hidden"
                   id="input_31_5_17"
                   name="input_5.17"
                   data-vehicle-data-type="mileage"
            />
                            <input type="hidden"
                   id="input_31_5_18"
                   name="input_5.18"
                   data-vehicle-data-type="int_color"
            />
                        </div>
        </li><li id='field_31_8' class='gfield gform_validation_container field_sublabel_below field_description_below' ><label class='gfield_label' for='input_31_8' >Phone</label><div class='ginput_container'><input name='input_8' id='input_31_8' type='text' value='' /></div><div class='gfield_description'>This field is for validation purposes and should be left unchanged.</div></li>
                            </ul></div>
        <div class='gform_footer top_label'> <input type='submit' id='gform_submit_button_31' class='gform_button button' value='Send' tabindex='6' onclick='if(window["gf_submitting_31"]){return false;}  window["gf_submitting_31"]=true;  ' /> <input type='hidden' name='gform_ajax' value='form_id=31&amp;title=1&amp;description=1&amp;tabindex=1' />
            <input type='hidden' class='gform_hidden' name='is_submit_31' value='1' />
            <input type='hidden' class='gform_hidden' name='gform_submit' value='31' />
            
            <input type='hidden' class='gform_hidden' name='gform_unique_id' value='' />
            <input type='hidden' class='gform_hidden' name='state_31' value='WyJbXSIsImFjYWNkODE0MTg0ZGE5OGVmMTkzM2ZmZGUyNjVjNmVjIl0=' />
            <input type='hidden' class='gform_hidden' name='gform_target_page_number_31' id='gform_target_page_number_31' value='0' />
            <input type='hidden' class='gform_hidden' name='gform_source_page_number_31' id='gform_source_page_number_31' value='1' />
            <input type='hidden' name='gform_field_values' value='' />
            
        </div>
                        </form>
                        </div>
                <iframe style='display:none;width:0px;height:0px;' src='about:blank' name='gform_ajax_frame_31' id='gform_ajax_frame_31'></iframe>
                <script type='text/javascript'>jQuery(document).ready(function($){gformInitSpinner( 31, '/content/plugins/gravityforms/images/spinner.gif' );jQuery('#gform_ajax_frame_31').load( function(){var contents = jQuery(this).contents().find('*').html();var is_postback = contents.indexOf('GF_AJAX_POSTBACK') >= 0;if(!is_postback){return;}var form_content = jQuery(this).contents().find('#gform_wrapper_31');var is_confirmation = jQuery(this).contents().find('#gform_confirmation_wrapper_31').length > 0;var is_redirect = contents.indexOf('gformRedirect(){') >= 0;var is_form = form_content.length > 0 && ! is_redirect && ! is_confirmation;if(is_form){jQuery('#gform_wrapper_31').html(form_content.html());setTimeout( function() { /* delay the scroll by 50 milliseconds to fix a bug in chrome */ jQuery(document).scrollTop(jQuery('#gform_wrapper_31').offset().top); }, 50 );if(window['gformInitDatepicker']) {gformInitDatepicker();}if(window['gformInitPriceFields']) {gformInitPriceFields();}var current_page = jQuery('#gform_source_page_number_31').val();gformInitSpinner( 31, '/content/plugins/gravityforms/images/spinner.gif' );jQuery(document).trigger('gform_page_loaded', [31, current_page]);window['gf_submitting_31'] = false;}else if(!is_redirect){var confirmation_content = jQuery(this).contents().find('#gforms_confirmation_message_31').html();if(!confirmation_content){confirmation_content = contents;}setTimeout(function(){jQuery('#gform_wrapper_31').replaceWith('<' + 'div id=\'gforms_confirmation_message_31\' class=\'gform_confirmation_message_31 gforms_confirmation_message\'' + '>' + confirmation_content + '<' + '/div' + '>');jQuery(document).scrollTop(jQuery('#gforms_confirmation_message_31').offset().top);jQuery(document).trigger('gform_confirmation_loaded', [31]);window['gf_submitting_31'] = false;}, 50);}else{jQuery('#gform_31').append(contents);if(window['gformRedirect']) {gformRedirect();}}jQuery(document).trigger('gform_post_render', [31, current_page]);} );} );</script><script type='text/javascript'> if(typeof gf_global == 'undefined') var gf_global = {"gf_currency_config":{"name":"U.S. Dollar","symbol_left":"$","symbol_right":"","symbol_padding":"","thousand_separator":",","decimal_separator":".","decimals":2},"base_url":"\/content\/plugins\/gravityforms","number_formats":[],"spinnerUrl":"\/content\/plugins\/gravityforms\/images\/spinner.gif"};jQuery(document).bind('gform_post_render', function(event, formId, currentPage){if(formId == 31) {if(!/(android)/i.test(navigator.userAgent)){jQuery('#input_31_2').mask('(999) 999-9999').bind('keypress', function(e){if(e.which == 13){jQuery(this).blur();} } );}} } );jQuery(document).bind('gform_post_conditional_logic', function(event, formId, fields, isInit){} );</script><script type='text/javascript'> jQuery(document).ready(function(){jQuery(document).trigger('gform_post_render', [31, 1]) } ); </script></div>        <script>
            if (typeof Object.assign != 'function') {
                Object.assign = function(target) {
                    'use strict';
                    if (target == null) {
                        throw new TypeError('Cannot convert undefined or null to object');
                    }

                    target = Object(target);
                    for (var index = 1; index < arguments.length; index++) {
                        var source = arguments[index];
                        if (source != null) {
                            for (var key in source) {
                                if (Object.prototype.hasOwnProperty.call(source, key)) {
                                    target[key] = source[key];
                                }
                            }
                        }
                    }
                    return target;
                };
            }

            (function($) {

                // Prevent this page from being "cached" by safari
                window.addEventListener('pageshow', function(event) {
                    if (event.persisted) {
                        window.location.reload()
                    }
                });

                function numberWithCommas(x) {
                    return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
                }

                function combineUrl(url1, url2) {
                    url1 = url1 || "";
                    url2 = url2 || "";
                    if (url1.charAt(url1.length - 1) === "/" && url2.charAt(0) === "/") {
                        return url1.substring(0, url1.length - 1) + url2;
                    } else {
                        return url1 + url2;
                    }
                }

                var mapping = {
                    'name': function(v) {
                        return [ v.year, v.make, v.model, v.trim ]
                            .filter(function(x) { return x != null; })
                            .join(" ");
                    },
                    'year': function(v) { return v.year; },
                    'make': function(v) { return v.make; },
                    'model': function(v) { return v.model; },
                    'trim': function(v) { return v.trim; },
                    'new_or_used': function(v) { return parseInt(v.used) ? 'used' : 'new'; },
                    'ext_color': function(v) { return v.exterior_factory_color || v.exterior_generic_color; },
                    'vin': function(v) { return v.vin; },
                    'vdp': function(v) { return v.vehicleDetailsUrl; },
                    'stock_no': function(v) { return v.stock_number; },
                    'vehicle_id': function(v) { return v.id; },
                    'price': function(v) { return v.display_price; },
                    'formattedPrice': function(v) { return JazelAuto5Products.utilities.formatPrice(v.display_price); },
                    'account_name': function(v) { return v.account_name; },
                    'address': function(v) {
                        var stateZipSegments = [v.location_state, v.location_zip_code];
                        stateZipSegments = stateZipSegments.map(function(item) { return item != null ? item.trim() : ""; });
                        stateZipSegments = stateZipSegments.filter(function(item) { return item != ""; });
                        var stateZip = stateZipSegments.join(" ");

                        var segments = [v.location_address1, v.location_address2, v.location_city, stateZip];
                        segments = segments.map(function(item) { return item != null ? item.trim() : ""; });
                        segments = segments.filter(function(item) { return item != ""; });
                        return segments.join(", ");
                    },
                    'body_style': function(v) {
                        if (Array.isArray(v.vehicle_type) && v.vehicle_type.length > 0) {
                            return v.vehicle_type[0];
                        }
                        return v.vehicle_type;
                    },
                    'transmission': function(v) { return v.transmission; },
                    'drivetrain': function(v) { return v.drivetrain; },
                    'engine': function(v) { return v.engine_cylinders; },
                    'mileage': function(v) { return v.used == "1" ? numberWithCommas(v.mileage) : null; },
                    'int_color': function(v) { return v.interior_factory_color || v.interior_generic_color; },
                    'image': function(v) {
                        var url = v.vehicleThumbnailUrl;
                        if (url == null || url === "") {
                            url = "/content/plugins/jzl-auto5-products/images/no-vehicle-image.png";
                        }
                        return url;
                    },
                    'errorimage': function(v) {
                        return "/content/plugins/jzl-auto5-products/images/no-vehicle-image.png";
                    }
                };

                var domNode = document.getElementById("srp-app");

                // Keep references to featherlight instances, one per
                // dom ID.
                var fls = {};
                var openForm = function(domId, vehicleId, vehicle, topAreaHtml) {
                    topAreaHtml = (typeof topAreaHtml !== 'undefined') ? topAreaHtml : '';

                    // Create new featherlight if one doesn't exist already and
                    // save the reference
                    var fl = fls[domId];
                    if (fl == null) {
                        var overlayForm = jQuery('#' + domId);
                        fl = new jQuery.featherlight(overlayForm, {
                            persist: true
                        });
                        fls[domId] = fl;
                    }

                    jQuery(document).trigger('a5srp_form_beforeopen', [fl.$content, mapping, vehicle]);
                    // After opening the featherlight, fill in its form fields
                    fl.open().done(function() {
                        jQuery(document).trigger('a5srp_form_open', [fl.$content, mapping, vehicle, topAreaHtml]);
                    });
                };

                var handleCtaClick = function(ctaName, vehicleId, vehicle) {
                    var ctaFormSet = [{"ctaName":0,"formName":"Gravity\/18"},{"ctaName":1,"formName":"Gravity\/19"}];
                    var ctaTopAreaSet = ["<div class=\"hook-lead-header\">\r\n<div class=\"hook-lead-title\">LOCK IN THIS E-PRICE<\/div>\r\n<div class=\"hook-lead-header-body\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\r\n<\/div>","<div class=\"hook-lead-header\">\r\n<div class=\"hook-lead-title\">LOCK IN THIS E-PRICE<\/div>\r\n<div class=\"hook-lead-header-body\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\r\n<\/div>"];

                    var currentForm;
                    var currentTopAreaHtml;

                    for (i = 0; i < ctaFormSet.length; i++) {
                        if (ctaFormSet[i].ctaName === ctaName) {
                            currentForm = ctaFormSet[i];
                            currentTopAreaHtml = ctaTopAreaSet[i];
                            break;
                        }
                    }

                    if (currentForm != null) {
                        var formId = currentForm.formName.replace(/[^a-zA-Z0-9]/g, '');
                        openForm(formId, vehicleId, vehicle, currentTopAreaHtml);
                    }
                };

                domNode.addEventListener("a5-srp-button-click", function(event) {
                    var ctaName = event.detail.ctaName;
                    var vehicleId = event.detail.vehicleId;
                    var vehicle = event.detail.vehicle; // should have all the properties we want.
                    handleCtaClick(ctaName, vehicleId, vehicle);
                });

                domNode.addEventListener("a5-vdp-button-click", function(event) {
                    var ctaName = event.detail.ctaName;
                    var vehicleId = event.detail.vehicleId;
                    var vehicle = event.detail.vehicle; // should have all the properties we want.
                    handleCtaClick(ctaName, vehicleId, vehicle);
                });

                domNode.addEventListener("a5-redeem-incentive-event", function(event) {
                    var offers = event.detail.offers;
                    var vin = event.detail.vin;
                    // don't have a way to get to vehicle info at the moment
                    var vehicleId = event.detail.vehicleId;
                    var vehicle = event.detail.vehicle; // should have all the properties we want.
                    openForm("a5-redeem-incentive-form", vehicleId, vehicle);
                });

                var setupInlineForm = function(domNode) {
                    // For inline form, the first time it's shown we want to hold a reference to it
                    var inlineFormRef = null;
                    domNode.addEventListener("customZoneDidMount", function(e) {
                        var domNode = e.target;
                        var element = e.detail.element;
                        var data = e.detail.data;
                        if (data.name === "vdp-cvdp-inline-form") {
                            console.log("onCustomZoneDidMount", domNode, element, data);
                            var vehicle = data.vehicle;

                            if (inlineFormRef == null) {
                                inlineFormRef = $('#a5-cvdp-inline-form');

                                if (inlineFormRef.length > 0) {

                                    // If the form is there then we show it
                                    inlineFormRef.show();

                                } else {

                                    // If no form has been set up, then we display a quick div saying so
                                    inlineFormRef = $("<div>");
                                    inlineFormRef.text(
                                        "No inline form has been set up. " +
                                        "Select one for this page in the page editor, " +
                                        "or a default one for the site in SRP defaults."
                                    );

                                }
                            }
                            $(element).append(inlineFormRef);

                            // If form has any fields to fill in, do it.
                            $(document).trigger('a5srp_form_beforeopen', [inlineFormRef, mapping, vehicle]);
                            $(document).trigger('a5srp_form_open', [inlineFormRef, mapping, vehicle]);
                        }
                    });
                    domNode.addEventListener("customZoneWillUnmount", function(e) {
                        var domNode = e.target;
                        var element = e.detail.element;
                        var data = e.detail.data;
                        if (data.name === "vdp-cvdp-inline-form") {
                            console.log("onCustomZoneWillUnmount", domNode, element, data);

                            if (inlineFormRef != null) {
                                inlineFormRef.detach();
                            }
                        }
                    });
                };

                // Inline form setup
                setupInlineForm(domNode);

                var options = null, state = null;

                
                // initial options = {"init":{"appBaseUrl":"\/inventory\/new-vehicles\/","useCognito":false},"srp":[{"appBaseUrl":"\/inventory\/new-vehicles\/","currentUrl":"\/inventory\/new-vehicles\/vehicle\/YV4162UK3K2134791\/2019-Volvo-XC40-Van-Nuys-CA","homeUrl":"https:\/\/www.galpinpremier.com","defaultMediaRange":"large","zipCode":null,"latlong":"","useCognito":false,"autocomplete":false,"searchServer":"\/\/search.jazelc.com\/api\/","mediaCdnBaseUrl":"\/\/media-cdn.jazelc.com\/","canonicalLinkSrpUrl":"https:\/\/www.galpinpremier.com\/inventory\/all-vehicles\/","themePrimaryColor":"#191919","themeSecondaryColor":"#bf9e57","vehicleDetailsButtonBackgroundColor":"#191919","showAutocheck":true,"showCarfax":true,"incentivesDisclaimer":"<br\/><br\/><p class='a5-disclaimer'>VEHICLE DATA<br\/>Certain specifications, prices and equipment data have been provided under license from Chrome Data Solutions (\\&#39;Chrome Data\\&#39;). \u00a9 2016 Chrome Data Solutions, LP. All Rights Reserved.  This information is supplied for personal use only and may not be used for any commercial purpose whatsoever without the express written consent of Chrome Data. Chrome Data makes no guarantee or warranty, either expressed or implied, including without limitation any warranty of merchantability or fitness for particular purpose, with respect to the data presented here. All specifications, prices and equipment are subject to change without notice.<\/p><p class='a5-disclaimer'>ESTIMATE MPG<br\/>EPA mileage ratings are supplied by Chrome Data Solutions, LP for comparison purposes only. Your actual mileage will vary, depending on how you drive and maintain your vehicle, driving conditions, battery pack age\/condition (hybrid models only) and other factors.<\/p><p class='a5-disclaimer'>PRICING<br\/>Vehicle pricing is believed to be accurate. Tax, title and registration are not included in prices shown unless otherwise stated. Manufacturer incentives may vary by region and are subject to change. Vehicle information & features are based upon standard equipment and may vary by vehicle. Monthly payments may be higher or lower based upon incentives, qualifying programs, credit qualifications, residency & fees. No claims, or warranties are made to guarantee the accuracy of vehicle pricing, payments or actual equipment. Call to confirm accuracy of any information.<\/p><p class='a5-disclaimer'>MSRP<br\/>The amount shown as MSRP is for informational purposes only and is the Manufacturer\u2019s Suggested Retail Price. This amount does not represent an advertised or selling price and does not include the price of any dealer added equipment. All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Colors, options and trim levels may vary. Not responsible for typographical errors. Specifications, features, safety and warranty data are based on what is available as standard specs\/features per trim level, for the designated model-year, and may not apply to vehicles with added packages or options. See dealer for written warranty information. Dealer makes no guarantees or warranties, either expressly or implied, with respect to the accuracy of any data listed on this page which was obtained from third party sources. All specifications, equipment and information are subject to change without notice. Any information contained on this page should be used for informational purposes only. Galpin\u2019s internet advertising is intended only for persons in California.<\/p><p class='a5-disclaimer'>PRICE<br\/>All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Not responsible for typographical errors. Prices valid through today\u2019s close of business. Subject to prior sale. Any information contained on this page should be used for informational purposes only. Galpin\u2019s internet advertising is intended only for persons in California.<\/p><br\/><div class='conditional-disclaimer lojack'>Notice All of Galpin used vehicles have an active theft deterrent device installed. This advertised price excludes the purchase price of the optional theft deterrent device which can be (1) purchased for an additional cost or (2) deactivated at the time of sale. If the device is deactivated it will be a non-functional item and at no time will it be activated.<\/div> ","keepVehicleLegacyFields":true,"dataLayerVariableName":"dataLayer"},{"srpconfig":{"jzla5p_srp_vdp_style":"classic","jzla5p_srp_color_scheme":"light","jzla5p_srp_sidebar_show_icons":"true","jzla5p_srp_views_order":"overview,list,grid","jzla5p_srp_default_view":"overview","jzla5p_srp_background_color":"#f5f5f5","jzla5p_srp_list_background_color_primary":"#ffffff","jzla5p_srp_list_background_color_secondary":"#ffffff","jzla5p_srp_afh_highlight_count_srp":0,"jzla5p_srp_afh_highlight_count_vdp":0,"jzla5p_srp_afh_padding_top":"3","jzla5p_srp_afh_background_color":"#f5f5f5","jzla5p_srp_afh_text_color":"#000000","jzla5p_srp_afh_bullet_color":"#bf9e57","jzla5p_srp_afh_icon":"\u25a0","jzla5p_srp_enable_sticky_sidebar":"true","jzla5p_srp_sticky_header_selector":".top_bar_left","jzla5p_srp_sticky_footer_selector":"","jzla5p_srp_tell_me_more_number":"","jzla5p_srp_location_override_contact_number":"","jzla5p_srp_location_override_name":"","jzla5p_srp_location_override_address1":"","jzla5p_srp_location_override_city":"","jzla5p_srp_location_override_state":"","jzla5p_srp_location_override_zip_code":"","jzla5p_vehicle_title_template":"{year} {make} {model} {trim}","jzla5p_srp_specifications_fields":"mileage, mpg, transmission, stocknumber, drivetrain, colors, engine, vin, location","jzla5p_vdp_specifications_fields":"mileage, mpg, drivetrain, exterior_color, transmission, interior_color, stocknumber, fuel_type, vin, engine","jzla5p_srp_options_min_price_show":"300","jzla5p_srp_options_min_price_display_price":"300","jzla5p_srp_options_used_vehicle":"false","jzla5p_srp_price_click_links_to_vdp":"true","jzla5p_srp_e_price_number":"","jzla5p_srp_e_price_form":"Gravity\/18","jzla5p_srp_e_price_form_label":"Get E-Price","jzla5p_srp_e_price_form_label_mobile":"E-Price","jzla5p_srp_e_price_form_label_position":"below-pricing","jzla5p_srp_e_price_form_label_image":"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png","jzla5p_vdp_e_price_form":"Gravity\/19","jzla5p_vdp_e_price_form_label":"Get E-Price","jzla5p_vdp_e_price_form_label_mobile":"E-Price","jzla5p_vdp_e_price_form_label_position":"below-pricing","jzla5p_vdp_e_price_form_label_image":"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png","jzla5p_srp_e_price_form_top_area_html":"<div class=\"hook-lead-header\">\r\n<div class=\"hook-lead-title\">LOCK IN THIS E-PRICE<\/div>\r\n<div class=\"hook-lead-header-body\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\r\n<\/div>","jzla5p_srp_e_price_form_show_vehicle":"true","jzla5p_srp_redeem_incentive_form":"Gravity\/31","jzla5p_cvdp_inline_form":"","jzla5p_srp_defaults_filters":"{\"active\":[\"makeModel\",\"price\",\"years\",\"mileage\",\"mpg\",\"bodyType\",\"drivetrain_sidebar\",\"transmission_sidebar\",\"exterior_color_sidebar\",\"features_sidebar\",\"fuel_type_sidebar\",\"passenger_capacity_sidebar\"],\"inactive\":[\"account_name_sidebar\",\"location_city_state_sidebar\",\"exterior_factory_color_sidebar\",\"interior_factory_color_sidebar\",\"packages_sidebar\",\"state_sidebar\",\"payment\",\"down_payment\",\"term_length\",\"credit_rating\",\"cab_style_sidebar\",\"engine_cylinders_sidebar\",\"generic_number_1\",\"generic_number_2\",\"generic_number_3\",\"generic_text_1_literal\",\"generic_text_2_literal\",\"generic_text_3_literal\"],\"openMobile\":[],\"openDesktop\":[],\"topBarMobile\":[],\"topBarDesktop\":[],\"visibleMobile\":[\"makeModel\",\"price\",\"years\",\"mileage\",\"mpg\",\"bodyType\",\"drivetrain_sidebar\",\"transmission_sidebar\",\"exterior_color_sidebar\",\"features_sidebar\",\"fuel_type_sidebar\",\"passenger_capacity_sidebar\"],\"visibleDesktop\":[\"makeModel\",\"price\",\"years\",\"mileage\",\"mpg\",\"bodyType\",\"drivetrain_sidebar\",\"transmission_sidebar\",\"exterior_color_sidebar\",\"features_sidebar\",\"fuel_type_sidebar\",\"passenger_capacity_sidebar\"],\"settings\":{\"makeModel\":{},\"price\":{\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"}},\"payment\":{\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"isFluid\":true,\"rangeMinValue\":100,\"rangeMaxValue\":3000},\"down_payment\":{\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"isSingleLabelConfigAvailable\":true,\"isFluid\":false,\"steps\":\"0, 1000, 5000, 10000, 20000\"},\"term_length\":{\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"isSingleLabelConfigAvailable\":true,\"isFluid\":false,\"steps\":\"36, 48, 60, 72\"},\"credit_rating\":{\"ranges\":[{\"name\":\"Challenged\",\"apr\":5.6},{\"name\":\"Fair\",\"apr\":5.2},{\"name\":\"Good\",\"apr\":4.8},{\"name\":\"Very Good\",\"apr\":4.4},{\"name\":\"Excellent\",\"apr\":4}],\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"isSingleLabelConfigAvailable\":true},\"years\":{\"useSlider\":true,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"}},\"mileage\":{\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"isSingleLabelConfigAvailable\":true},\"mpg\":{\"mpgFilterSortOrder\":1,\"mpgFilterFormat\":\"31b0385f-059f-4c64-be03-835dd6f53245\",\"mpgFilterLabel\":\"c0b90ab4-cb41-448d-b107-b309981db08b\",\"useSlider\":false,\"useSingleLabel\":false,\"labelLocation\":\"above\",\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderThickness\":16,\"sliderMaxWidth\":600,\"sliderHandleSize\":24,\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"}},\"bodyType\":{\"useSvgIcons\":true,\"svgColoration\":{\"selectedItemSvgFillColor\":\"#FFFFFF\",\"selectedItemBackgroundColor\":\"#000000\",\"selectedItemLabelColor\":\"#FFFFFF\",\"unselectedItemSvgFillColor\":\"#000000\",\"unselectedItemBackgroundColor\":\"#FFFFFF\",\"unselectedItemLabelColor\":\"#000000\"}},\"drivetrain_sidebar\":{},\"transmission_sidebar\":{},\"exterior_color_sidebar\":{},\"features_sidebar\":{},\"fuel_type_sidebar\":{},\"passenger_capacity_sidebar\":{},\"account_name_sidebar\":{},\"location_city_state_sidebar\":{},\"exterior_factory_color_sidebar\":{},\"interior_factory_color_sidebar\":{},\"packages_sidebar\":{},\"state_sidebar\":{},\"cab_style_sidebar\":{},\"engine_cylinders_sidebar\":{},\"generic_number_1\":{},\"generic_number_2\":{},\"generic_number_3\":{},\"generic_text_1_literal\":{},\"generic_text_2_literal\":{},\"generic_text_3_literal\":{}}}","jzla5p_account_id_sort_order":"","jzla5p_oem_sort_order":"","jzla5p_compliance_secondary_sort":"display_price asc","jzla5p_compliance_tertiary_sort":"","jzla5p_srp_options_display_vdp_view_count":"false","jzla5p_srp_options_vdp_view_count_days":"7","jzla5p_srp_grid_view_images_force16x9":"true","jzla5p_srp_grid_view_location":"false","jzla5p_srp_grid_view_distance":"false","jzla5p_srp_always_on_sorts":"has_price desc, has_image desc","jzla5p_srp_always_on_sorts_migrated":true,"jzla5p_srp_default_sort":"display_price asc","jzla5p_srp_default_sort_migrated":true,"jzla5p_srp_cta":"{\"ctas\":[{\"jzla5p_cta_location\":\"srp\",\"jzla5p_cta_view\":\"jzla5p_cta_view_image\",\"jzla5p_cta_action_type\":\"jzla5p_cta_action_form\",\"jzla5p_cta_label\":\"Get E-Price\",\"jzla5p_cta_label_mobile\":\"E-Price\",\"jzla5p_cta_position\":\"below-pricing\",\"jzla5p_srp_e_price_form_top_area_html\":\"<div class=\\\"hook-lead-header\\\">\\r\\n<div class=\\\"hook-lead-title\\\">LOCK IN THIS E-PRICE<\/div>\\r\\n<div class=\\\"hook-lead-header-body\\\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\\r\\n<\/div>\",\"jzla5p_cta_classnames\":\"\",\"jzla5p_cta_data_attributes\":[],\"jzla5p_cta_force_anchor_tag\":\"false\",\"jzla5p_cta_apply_attributes_to_anchor\":\"false\",\"jzla5p_cta_apply_custom_css_classname_to_anchor\":\"false\",\"jzla5p_cta_name\":0,\"jzla5p_cta_action_form\":\"Gravity\/18\",\"jzla5p_cta_view_image\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png\"},{\"jzla5p_cta_location\":\"vdp\",\"jzla5p_cta_view\":\"jzla5p_cta_view_image\",\"jzla5p_cta_action_type\":\"jzla5p_cta_action_form\",\"jzla5p_cta_label\":\"Get E-Price\",\"jzla5p_cta_label_mobile\":\"E-Price\",\"jzla5p_cta_position\":\"below-pricing\",\"jzla5p_srp_e_price_form_top_area_html\":\"<div class=\\\"hook-lead-header\\\">\\r\\n<div class=\\\"hook-lead-title\\\">LOCK IN THIS E-PRICE<\/div>\\r\\n<div class=\\\"hook-lead-header-body\\\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\\r\\n<\/div>\",\"jzla5p_cta_classnames\":\"\",\"jzla5p_cta_data_attributes\":[],\"jzla5p_cta_force_anchor_tag\":\"false\",\"jzla5p_cta_apply_attributes_to_anchor\":\"false\",\"jzla5p_cta_apply_custom_css_classname_to_anchor\":\"false\",\"jzla5p_cta_name\":1,\"jzla5p_cta_action_form\":\"Gravity\/19\",\"jzla5p_cta_view_image\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png\"},{\"jzla5p_cta_location\":\"vdp\",\"jzla5p_cta_view\":\"jzla5p_cta_view_image\",\"jzla5p_cta_action_type\":\"jzla5p_cta_action_page\",\"jzla5p_cta_label\":\"Value Your Trade\",\"jzla5p_cta_label_mobile\":\"Value Your Trade\",\"jzla5p_cta_position\":\"below-pricing\",\"jzla5p_srp_e_price_form_top_area_html\":\"<div class=\\\"hook-lead-header\\\">\\r\\n<div class=\\\"hook-lead-title\\\">LOCK IN THIS E-PRICE<\/div>\\r\\n<div class=\\\"hook-lead-header-body\\\">Buying soon? Complete this short form and we will send you today's e-price.<\/div>\\r\\n<\/div>\",\"jzla5p_cta_classnames\":\"\",\"jzla5p_cta_data_attributes\":[],\"jzla5p_cta_force_anchor_tag\":\"false\",\"jzla5p_cta_apply_attributes_to_anchor\":\"false\",\"jzla5p_cta_apply_custom_css_classname_to_anchor\":\"false\",\"jzla5p_cta_name\":2,\"jzla5p_cta_view_image\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/ValueYourTrade-CTA-Smaller.png\",\"jzla5p_cta_target_url\":\"\/value-your-trade\/ \"}],\"order\":[0,1,2]}","jzla5p_srp_cta_forms_migrated":true,"jzla5p_srp_sort_by_distance_migrated":true}},{"srpconfig":{"jzla5p_srp_vehicle_filter_id":"1008","jzla5p_srp_always_on_sorts_migrated":true,"jzla5p_srp_default_sort_migrated":true,"jzla5p_srp_cta_forms_migrated":true,"jzla5p_srp_sort_by_distance_migrated":true}},{"srpconfig":[]},{"userconfig":{"jzla5p_user_payment_info_down_payment":1995,"jzla5p_user_payment_info_trade_in_value":0,"jzla5p_user_payment_info_term_month":72,"jzla5p_user_payment_info_apr":3.5,"jzla5p_user_payment_info_credit_rating":0}}]};
                                options = {"init":{"appBaseUrl":"\/inventory\/new-vehicles\/","useCognito":false},"srp":[{"debug":false,"homeUrl":"https:\/\/www.galpinpremier.com","currentUrl":"\/inventory\/new-vehicles\/vehicle\/YV4162UK3K2134791\/2019-Volvo-XC40-Van-Nuys-CA","appBaseUrl":"\/inventory\/new-vehicles\/","loggedRequests":"[{\"apiName\":\"passthroughvdp\",\"queryParams\":\"q=((vehicle_filter_ids%3A1008)%20AND%20((vin%3A%22YV4162UK3K2134791%22)))&q.parser=lucene&size=1&start=0\",\"vins\":\"YV4162UK3K2134791\"}]"}],"instantiatedComponents":["VehicleDetailsPage"]};
                state = JSON.parse("{\"settings\":{\"appSettings\":{\"defaultViewType\":\"overview\",\"gridWidth\":\"300\",\"endOfVehicleListMarkup\":\"\",\"stickySidebarTopSelector\":\".top_bar_left\",\"videoPopupTitleTemplate\":\"Your Video for Stock#: {stock_number}\",\"bestLeaseOfferLargeText\":\"Lease\",\"srpSpecOrder\":[\"mileage\",\"mpg\",\"transmission\",\"stockNumber\",\"drivetrain\",\"colors\",\"engine\",\"vin\",\"location\"],\"iframeWidth\":\"100%\",\"complianceSortExpressions\":[{\"id\":\"has_price\",\"type\":\"sort_has_price\",\"direction\":\"desc\"},{\"id\":\"has_image\",\"type\":\"sort_has_image\",\"direction\":\"desc\"}],\"bestFinanceOfferLargeText\":\"Finance\",\"enableDistanceWeightedScore\":false,\"nonOemWindowSticker\":false,\"incentivesDisclaimer\":\"<br\/><br\/><p class='a5-disclaimer'>VEHICLE DATA<br\/>Certain specifications, prices and equipment data have been provided under license from Chrome Data Solutions (\\\\&#39;Chrome Data\\\\&#39;). \u00a9 2016 Chrome Data Solutions, LP. All Rights Reserved.  This information is supplied for personal use only and may not be used for any commercial purpose whatsoever without the express written consent of Chrome Data. Chrome Data makes no guarantee or warranty, either expressed or implied, including without limitation any warranty of merchantability or fitness for particular purpose, with respect to the data presented here. All specifications, prices and equipment are subject to change without notice.<\/p><p class='a5-disclaimer'>ESTIMATE MPG<br\/>EPA mileage ratings are supplied by Chrome Data Solutions, LP for comparison purposes only. Your actual mileage will vary, depending on how you drive and maintain your vehicle, driving conditions, battery pack age\/condition (hybrid models only) and other factors.<\/p><p class='a5-disclaimer'>PRICING<br\/>Vehicle pricing is believed to be accurate. Tax, title and registration are not included in prices shown unless otherwise stated. Manufacturer incentives may vary by region and are subject to change. Vehicle information & features are based upon standard equipment and may vary by vehicle. Monthly payments may be higher or lower based upon incentives, qualifying programs, credit qualifications, residency & fees. No claims, or warranties are made to guarantee the accuracy of vehicle pricing, payments or actual equipment. Call to confirm accuracy of any information.<\/p><p class='a5-disclaimer'>MSRP<br\/>The amount shown as MSRP is for informational purposes only and is the Manufacturer\u2019s Suggested Retail Price. This amount does not represent an advertised or selling price and does not include the price of any dealer added equipment. All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Colors, options and trim levels may vary. Not responsible for typographical errors. Specifications, features, safety and warranty data are based on what is available as standard specs\/features per trim level, for the designated model-year, and may not apply to vehicles with added packages or options. See dealer for written warranty information. Dealer makes no guarantees or warranties, either expressly or implied, with respect to the accuracy of any data listed on this page which was obtained from third party sources. All specifications, equipment and information are subject to change without notice. Any information contained on this page should be used for informational purposes only. Galpin\u2019s internet advertising is intended only for persons in California.<\/p><p class='a5-disclaimer'>PRICE<br\/>All advertised prices exclude government fees and taxes, any finance charges, any dealer document processing charge, any electronic filing charge and any emission testing charge. Not responsible for typographical errors. Prices valid through today\u2019s close of business. Subject to prior sale. Any information contained on this page should be used for informational purposes only. Galpin\u2019s internet advertising is intended only for persons in California.<\/p><br\/><div class='conditional-disclaimer lojack'>Notice All of Galpin used vehicles have an active theft deterrent device installed. This advertised price excludes the purchase price of the optional theft deterrent device which can be (1) purchased for an additional cost or (2) deactivated at the time of sale. If the device is deactivated it will be a non-functional item and at no time will it be activated.<\/div> \",\"paymentCalculatorRoundResult\":false,\"paymentCalculatorDisclaimer\":\"Only an estimate. Excludes taxes, title, license, and insurance.\",\"bestCashOfferLargeText\":\"Cash\",\"useExternalLocationInput\":false,\"showOptionsOnUsedVehicles\":false,\"vehicleMultilineTitleTemplateTop\":\"{condition:used_or_certified} {year} {make}\",\"afhHighlightCountVdp\":0,\"paymentCalculatorSliderHandleBackgroundColor\":\"#FFFFFF\",\"enableCPOLogoLink\":false,\"ftsRedirectSettings\":[],\"financeOfferTabTitle\":\"All Finance Offers\",\"showMeTheCarfax\":false,\"leaseOfferTabTitle\":\"All Lease Offers\",\"showAdjustTermsLinkByMonthlyPayment\":false,\"minOptionShowPrice\":300,\"showMileageSimilarVehicles\":false,\"showFilterIcons\":true,\"desktopOffersAreaTitleText\":\"Special Offers\",\"srpSpecOrderListView\":[\"mileage\",\"stockNumber\"],\"windowStickerInline\":false,\"showCarfax\":true,\"hasGridWidth\":false,\"paymentCalculatorSliderHandleBorderColor\":\"#DDDDDD\",\"srpVehicleTitleColor\":\"#000000\",\"vehicleTitleTemplate\":\"{year} {make} {model} {trim}\",\"paymentCalculatorSliderUnselectedColor\":\"#CCCCCC\",\"searchSummaryCountClass\":\"f2rem\",\"centerAlignOffers\":false,\"srpEnableVideo\":false,\"vdpGalleryMultilineLayout\":false,\"paymentCalculatorSecondaryDisclaimer\":\"\",\"showPercentSignAfterAprs\":false,\"useGenericFeaturesOnComparePage\":true,\"showFts\":true,\"endOfVehicleListContainerStyle\":{},\"pricingViewerFontSize\":18,\"autocomplete\":true,\"certificationDisplayStyle\":\"logo\",\"displayVdpViewCount\":false,\"vdpGalleryInfiniteSliding\":false,\"useCognito\":false,\"videoPopupShowTitle\":true,\"availableViewTypes\":[\"overview\",\"list\",\"grid\"],\"iframeHeight\":\"100%\",\"immediatelyApplyPaymentCalculatorChanges\":true,\"buttonsBelowImage\":false,\"CPOLogoLinks\":[],\"cashOfferTabTitle\":\"All Cash Offers\",\"canonicalLinkSrpUrl\":\"https:\/\/www.galpinpremier.com\/inventory\/all-vehicles\/\",\"vdpBrowserTitleTemplate\":\"{year} {make} {model} {trim} {exterior_color} {location_city}, {location_state}\",\"cmpSpecOrder\":[\"vin\",\"mpg\",\"mileage\",\"fuelType\",\"engine\",\"drivetrain\",\"transmission\",\"exteriorColor\",\"interiorColor\",\"stockNumber\"],\"screenWidthForSidebar\":1025,\"dataLayerVariableName\":\"dataLayer\",\"zipCode\":null,\"doNotIncludePaymentIncentives\":false,\"showSuperScriptDisclaimers\":false,\"enableStickySidebar\":true,\"driveTimeFilterSeconds\":2160,\"financeOfferIncentiveTypeLabel\":\"Finance Rate\",\"enableGeolocationCanada\":false,\"leaseOfferIncentiveTypeLabel\":\"Lese Rate\",\"vdpSpecOrder\":[\"mileage\",\"mpg\",\"drivetrain\",\"exteriorColor\",\"transmission\",\"interiorColor\",\"stockNumber\",\"fuelType\",\"vin\",\"engine\"],\"videoPlayMode\":\"lightbox\",\"complianceSortExpressionsSecondary\":[],\"allowNonScoreSortForTextSearch\":true,\"inlineOffersSettingsApplicability\":\"srp-vdp\",\"freeTextSearchPlaceholder\":\"Search for vehicle (e.g. Black 2017 Coupe)\",\"priceClickGoesToVdp\":true,\"afhHighlightCountSrp\":0,\"popupHeight\":null,\"sortColorsByHue\":false,\"pricingViewerLineHeight\":1.5,\"useOrTextInBetweenIncentives\":false,\"absoluteAppBaseUrl\":\"https:\/\/www.galpinpremier.com\/inventory\/new-vehicles\/\",\"userSelectableSorts\":[[\"Price - Low to High\",\"display_price asc\"],[\"Price - High to Low\",\"display_price desc\"],[\"Year - Oldest to Newest\",\"year_sidebar asc\"],[\"Year - Newest to Oldest\",\"year_sidebar desc\"],[\"Make\/Model - A to Z\",\"make_sidebar asc, model_sidebar asc\"],[\"Make\/Model - Z to A\",\"make_sidebar desc, model_sidebar desc\"],[\"Miles - Low to High\",\"mileage asc\"],[\"Miles - High to Low\",\"mileage desc\"],[\"Days on Lot - Newest to Oldest\",\"date_in_stock asc\"],[\"Days on Lot - Oldest to Newest\",\"date_in_stock desc\"]],\"showVinSimilarVehicles\":false,\"showCarfaxInstantSnapshots\":false,\"displayFullPricing\":true,\"popupOffersAreaTitleText\":\"Special Offers\",\"paymentCalculatorEnableTypeChange\":false,\"srpBottomTemplate\":null,\"unlimitedDistanceSearchLabel\":\"Any\",\"currentUrl\":\"\/inventory\/new-vehicles\/vehicle\/YV4162UK3K2134791\/2019-Volvo-XC40-Van-Nuys-CA\",\"showMonthlyPayment\":false,\"redeemIncentiveEventName\":\"a5-redeem-incentive-event\",\"enableDistanceOnlyOnDistanceSort\":false,\"vdpLinkTemplate\":\"{conditions:used_or_certified} {year} {make} {model} {location_city} {location_state}\",\"searchSummaryVehiclesFoundLabel\":\"vehicles found\",\"composableVdpConfig\":{\"page\":{\"layoutPreset\":\"vdp-classic\",\"fullScreen\":true,\"z_dummy\":null},\"tiles\":{}},\"paymentCalculatorDownPaymentRowExpanded\":false,\"ctaFormSettings\":[{\"srpEventName\":\"a5-srp-button-click\",\"vdpEventName\":\"a5-vdp-button-click\",\"location\":\"srp\",\"formConfigs\":{\"pageUrl\":null,\"dataAttributes\":[],\"className\":\"eprice\",\"view\":\"image\",\"position\":\"below-pricing\",\"name\":0,\"mobileLabel\":\"E-Price\",\"customClassName\":\"\",\"imageUrl\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png\",\"label\":\"Get E-Price\",\"applyCustomClassNameToAnchor\":false,\"applyAttributesToAnchor\":false,\"action\":\"form\",\"forceAnchorTag\":false,\"jsEventName\":null}},{\"srpEventName\":\"a5-srp-button-click\",\"vdpEventName\":\"a5-vdp-button-click\",\"location\":\"vdp\",\"formConfigs\":{\"pageUrl\":null,\"dataAttributes\":[],\"className\":\"eprice\",\"view\":\"image\",\"position\":\"below-pricing\",\"name\":1,\"mobileLabel\":\"E-Price\",\"customClassName\":\"\",\"imageUrl\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/Galpin-e-Price.png\",\"label\":\"Get E-Price\",\"applyCustomClassNameToAnchor\":false,\"applyAttributesToAnchor\":false,\"action\":\"form\",\"forceAnchorTag\":false,\"jsEventName\":null}},{\"srpEventName\":\"a5-srp-button-click\",\"vdpEventName\":\"a5-vdp-button-click\",\"location\":\"vdp\",\"formConfigs\":{\"pageUrl\":\"\/value-your-trade\/ \",\"dataAttributes\":[],\"className\":\"eprice\",\"view\":\"image\",\"position\":\"below-pricing\",\"name\":2,\"mobileLabel\":\"Value Your Trade\",\"customClassName\":\"\",\"imageUrl\":\"https:\/\/images.jazelc.com\/uploads\/galpinpremier\/ValueYourTrade-CTA-Smaller.png\",\"label\":\"Value Your Trade\",\"applyCustomClassNameToAnchor\":false,\"applyAttributesToAnchor\":false,\"action\":\"page\",\"forceAnchorTag\":false,\"jsEventName\":null}}],\"cashOfferIncentiveTypeLabel\":\"Bonus Cash\",\"soldVehicle301Redirect\":true,\"carfaxInstantSnapshotPartnerCode\":\"\",\"defaultSortTitle\":\"Default\",\"popupWidth\":\"90%\",\"composableSrpConfigLayoutPresetName\":\"srp-classic\",\"latlong\":\"\",\"minOptionDisplay\":300,\"enableTransferFees\":false,\"storeLocationIn\":\"none\",\"showLocationOnGridView\":false,\"showDistanceOnGridView\":false,\"showAutocheck\":true,\"vehicleMultilineTitleTemplateBottom\":\"{model} {trim}\",\"afhIcon\":\"\u25a0\",\"stackedTotalCashText\":\"Total Cash\",\"topBarFiltersPills\":false,\"topBarFiltersIcons\":false,\"showIcons\":true,\"afhIconSize\":16,\"enableTopBarDisclaimerLinks\":false,\"appBaseUrl\":\"\/inventory\/new-vehicles\/\",\"topBarFilters\":[{\"filterId\":\"text-search\",\"className\":\"flex-grow1 ma2\"},{\"filterId\":\"sort\",\"className\":\"pa2 pr2-ns pr3\"},{\"filterId\":\"view-type\",\"className\":\"mv2 ph3\"}],\"userDefaultPaymentInfo\":{\"apr\":3.5,\"creditRating\":0,\"downPayment\":1995,\"termMonth\":72,\"tradeInValue\":0},\"useBodyTypeSidebarFacet\":false,\"enableEndOfVehicleListContentElement\":false,\"vdpViewCountDays\":7,\"sideBarFilters\":[{\"filterId\":\"summary\",\"className\":\"pa2 tc pr4 pr2-ns\"},{\"filterId\":\"conditions\",\"className\":\"pa2 pv2\",\"passProps\":{\"initOpenMobile\":true,\"initOpenDesktop\":true}},\"favorites\",\"compare\",{\"filterId\":\"distance\",\"passProps\":{\"initOpenMobile\":true,\"initOpenDesktop\":true}},{\"filterId\":\"models\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"price\",\"passProps\":{\"settings\":{\"sliderMaxWidth\":600,\"useSingleLabel\":false,\"useSlider\":false,\"labelLocation\":\"above\",\"sliderHandleSize\":24,\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"sliderThickness\":16},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"years\",\"passProps\":{\"settings\":{\"sliderMaxWidth\":600,\"useSingleLabel\":false,\"useSlider\":true,\"labelLocation\":\"above\",\"sliderHandleSize\":24,\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"sliderThickness\":16},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"mileage\",\"passProps\":{\"settings\":{\"sliderMaxWidth\":600,\"isSingleLabelConfigAvailable\":true,\"useSingleLabel\":false,\"useSlider\":false,\"labelLocation\":\"above\",\"sliderHandleSize\":24,\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"sliderThickness\":16},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"mpg\",\"passProps\":{\"settings\":{\"sliderMaxWidth\":600,\"useSingleLabel\":false,\"useSlider\":false,\"labelLocation\":\"above\",\"sliderHandleSize\":24,\"titleLocation\":\"above\",\"titleAlign\":\"default\",\"sliderColors\":{\"rail\":\"#dddddd\",\"track\":\"#3d505e\",\"handle\":\"#082134\"},\"mpgFilterFormat\":\"31b0385f-059f-4c64-be03-835dd6f53245\",\"sliderThickness\":16,\"mpgFilterSortOrder\":1,\"mpgFilterLabel\":\"c0b90ab4-cb41-448d-b107-b309981db08b\"},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"bodytypes\",\"passProps\":{\"settings\":{\"useSvgIcons\":true,\"svgColoration\":{\"selectedItemSvgFillColor\":\"#FFFFFF\",\"selectedItemBackgroundColor\":\"#000000\",\"selectedItemLabelColor\":\"#FFFFFF\",\"unselectedItemSvgFillColor\":\"#000000\",\"unselectedItemBackgroundColor\":\"#FFFFFF\",\"unselectedItemLabelColor\":\"#000000\"}},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"drivetrain\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"transmission\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"color\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"features\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"fueltype\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}},{\"filterId\":\"seating\",\"passProps\":{\"settings\":{},\"initOpenMobile\":false,\"initOpenDesktop\":false,\"topBarMobile\":false,\"topBarDesktop\":false,\"visibleMobile\":true,\"visibleDesktop\":true}}],\"mobileOffersAreaTitleText\":null,\"showSidebar\":true,\"salesTax\":0,\"paymentCalculatorSliderSelectedColor\":\"#888888\",\"defaultSort\":\"display_price asc\",\"paymentCalculatorUnderlineColor\":\"#A8A8A8\"},\"searchSettings\":{\"searchServer\":\"\/\/search.jazelc.com\/api\/\",\"afhServer\":\"\/\/afh.jazelc.com\/api\/\",\"keepVehicleLegacyFields\":true,\"vehicleFilterIds\":[1008]},\"mediaSettings\":{\"mediaCdnBaseUrl\":\"\/\/media-cdn.jazelc.com\/\",\"force16x9\":true},\"themeSettings\":{\"afhColor\":\"#000000\",\"secondaryListBackgroundColor\":\"#ffffff\",\"ctaPrimaryBackgroundColor\":\"#3399ff\",\"ctaPrimaryTextColor\":\"#FFFFFF\",\"mobileHeaderFontColor\":\"#ffffff\",\"mobileHeaderBackgroundColor\":\"#494e5b\",\"srpVehicleTitleColor\":\"#000000\",\"afhIconColor\":\"#bf9e57\",\"favoriteColor\":\"#DBA709\",\"themePrimaryColor\":\"#191919\",\"vehicleListBackgroundColor\":\"#f5f5f5\",\"vehicleDetailsButtonBackgroundColor\":\"#191919\",\"vehicleDetailsButtonTextColor\":\"#FFFFFF\",\"afhBackgroundColor\":\"#f5f5f5\",\"vehicleDetailsButtonBorder\":\"0px solid #000000\",\"primaryListBackgroundColor\":\"#ffffff\",\"themeSecondaryColor\":\"#bf9e57\",\"ctaPrimaryBorder\":\"0px solid #000000\",\"themeDisabledColor\":\"#dddddd\"}},\"searchFilters\":{\"availableFiltersId\":\"\",\"availableFilters\":{},\"previousSearchString\":\"\",\"previousScrollY\":0,\"enterTime\":1559307484235,\"enterVin\":\"YV4162UK3K2134791\"},\"cachedFilters\":{},\"searchResults\":{\"index\":0,\"vins\":[],\"filters\":{}},\"vehicles\":{\"vehiclesMap\":{\"YV4162UK3K2134791\":{\"id\":\"1438455\",\"vin\":\"YV4162UK3K2134791\",\"detailLevel\":200,\"location\":{\"accountId\":20,\"name\":\"Galpin Premier\",\"address1\":\"15500 Roscoe Blvd.\",\"city\":\"Van Nuys\",\"state\":\"CA\",\"zipCode\":\"91406\",\"contactNumber\":\"(888) 712-0182\"},\"visual\":{\"colors\":{\"interior\":{\"factory\":\"Charcoal\"},\"exterior\":{\"factory\":\"Ice White\",\"generic\":\"White\"}},\"image\":{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b3db687e83974a83b4699946ebe78a0d.jpg\",\"base64\":\"\/9j\/4AAQSkZJRgABAQEAYABgAAD\/2wBDAP\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/2wBDAf\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/wAARCABLAGQDASIAAhEBAxEB\/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL\/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6\/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL\/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6\/9oADAMBAAIRAxEAPwCSiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKQnFAC0mRTeT1pp64FAD9w\/yaNw\/yRUefWk60ATZpNwpmM\/QUdKAJM0tRjrxTxQAtFFFABSZoPSoySDQBJSVHk0bjQBJgUm0elJzRz7\/AJ0ALtFGBR060gbNABjHfilwKKKADgdBS89qSmZOc0ATUUUUANNN3D\/IpxGRUXTqKAFz9Pyp\/HtUfFLigB5OKTdmm7u3X60Z9hQAp5OD0ptKP5c0H68UAOyPWjcPSmUZ9hQA4tn2pB270cnt+VKAfSgB+aKSigBaQjNLRQAzbRsPrT6U0ARbTRtNSUooAjw1G01JSUAN2ilwBTu1JQAUUCg0AJRRRQB\/\/9k=\",\"visibleUrl\":\"\/media\/38229186\",\"visibleShortUrl\":\"\/media\/38229186\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},\"imageCount\":4,\"videoCount\":0,\"styleName\":\"T5 AWD Momentum\",\"dealerVideos\":[],\"imageSide\":null,\"dealerDescriptionPhotos\":[],\"stockPhotos\":[],\"dealerPhotos\":[{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b3db687e83974a83b4699946ebe78a0d.jpg\",\"visibleUrl\":\"\/media\/38229186\",\"visibleShortUrl\":\"\/media\/38229186\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/bb6f8405453b4f8ebede7dd8c42c80e8.jpg\",\"visibleUrl\":\"\/media\/38229187\",\"visibleShortUrl\":\"\/media\/38229187\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b5ea843924244df19a5a2628ffd5e14c.jpg\",\"visibleUrl\":\"\/media\/38229188\",\"visibleShortUrl\":\"\/media\/38229188\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/43113cfdc91a48d0bb300f11201d1665.jpg\",\"visibleUrl\":\"\/media\/38229189\",\"visibleShortUrl\":\"\/media\/38229189\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false}],\"combinedPhotos\":[{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b3db687e83974a83b4699946ebe78a0d.jpg\",\"visibleUrl\":\"\/media\/38229186\",\"visibleShortUrl\":\"\/media\/38229186\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/bb6f8405453b4f8ebede7dd8c42c80e8.jpg\",\"visibleUrl\":\"\/media\/38229187\",\"visibleShortUrl\":\"\/media\/38229187\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b5ea843924244df19a5a2628ffd5e14c.jpg\",\"visibleUrl\":\"\/media\/38229188\",\"visibleShortUrl\":\"\/media\/38229188\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false},{\"source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/43113cfdc91a48d0bb300f11201d1665.jpg\",\"visibleUrl\":\"\/media\/38229189\",\"visibleShortUrl\":\"\/media\/38229189\",\"isChromePressPhoto\":false,\"isColorMatch\":true,\"isPlaceHolder\":false}]},\"specifications\":{\"vehicleType\":[\"Sport Utility\"],\"drivetrain\":\"All Wheel Drive\",\"drivetrainCode\":\"AWD\",\"transmission\":\"8-Speed Geartronic Automatic -inc: start\/stop\",\"fuelType\":\"Gasoline\",\"mpgCityLow\":\"23\",\"mpgCityHigh\":\"23\",\"mpgCityAverage\":\"23\",\"mpgHighwayLow\":\"31\",\"mpgHighwayHigh\":\"31\",\"mpgHighwayAverage\":\"31\",\"engineCylinders\":\"4 Cylinders\",\"engine\":\"4 Cylinder Engine\"},\"certifications\":{\"certifiedByDealer\":false,\"certifiedByManufacturer\":false,\"hasCarfax\":false,\"hasCarfaxSnapshot\":false,\"carfaxSnapshotHash\":\"oYCPutiAs15jUXIEE3jK3Q==\",\"carfaxOneOwner\":false,\"hasAutocheck\":false},\"incentives\":{\"stack\":{\"ExpirationDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"ChromeStructuredIncentiveStacks\":{\"LowestPaymentLeaseDeal\":{\"Term\":48,\"TotalCash\":0,\"MonthlyPayment\":871,\"Apr\":5.28,\"Incentives\":[{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Subvented Lease Factors\",\"SignatureId\":\"743\",\"IncentiveId\":\"14928386\",\"CategoryDescription\":\"Lease Rate\"},{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Residuals Values\",\"SignatureId\":\"744\",\"IncentiveId\":\"14935144\",\"CategoryDescription\":\"Residual\"}],\"ExpiryDate\":\"6\/1\/2019 3:59:59 AM\",\"EffectiveDate\":\"5\/1\/2019 4:00:00 AM\"}},\"TcuvStructuredIncentiveStacks\":{}},\"full\":{\"ExpirationDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"ChromeStructuredIncentives\":{\"CashIncentives\":[{\"SignatureHistoryId\":29688,\"SignatureId\":9110,\"VehicleStatusList\":[\"New\"],\"DeliveryTypeList\":[\"Non-subvented Lease\",\"Subvented Lease\"],\"ProgramValues\":{\"ValueVariationList\":[{\"ProgramValueList\":[{\"NumberOfDays\":0,\"MaxValueOfPaymentsWaivedPerPayment\":0,\"MaxValueOfPaymentsWaived\":0,\"MaxNumberOfPaymentsWaived\":0,\"Cash\":500}]}]},\"ProgramRuleList\":[{\"Description\":\"Eligible customers that currently own or lease a Volvo or Saab vehicle.\",\"Type\":\"Eligibility\"},{\"Description\":\"Individuals or members of the same household who currently owns\/leases any model year Volvo or Saab vehicle OR has owned\/leased either within the last 6 months.\",\"Type\":\"Qualification\"}],\"InstitutionList\":[],\"stackabilityIncentiveIDs\":[744,743,12781,12782],\"ExpiryDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"stackableWith\":\"744|743|12781|12782\",\"IncentiveId\":\"14929202\",\"ExpiryDate\":\"2019-05-31\",\"EffectiveDate\":\"2019-05-01\",\"EndRecipient\":\"Customer\",\"GeoDesc\":\"Volvo US Western Market 1302 - Los Angeles North\",\"PreviousOwnership\":\"Loyalty\",\"CategoryDescription\":\"Bonus Cash\",\"ProgramNumber\":\"62751\",\"ProgramDescription\":\"WR Loyalty Bonus - Lease\",\"GroupAffiliation\":\"No Specific Group Affiliation\",\"Source\":\"OEM\",\"Market\":\"Retail\",\"Type\":\"Cash\",\"CategoryId\":\"123\"},{\"SignatureHistoryId\":29668,\"SignatureId\":9098,\"VehicleStatusList\":[\"New\"],\"DeliveryTypeList\":[\"Non-subvented Finance\",\"Subvented Retail Finance\"],\"ProgramValues\":{\"ValueVariationList\":[{\"ProgramValueList\":[{\"NumberOfDays\":0,\"MaxValueOfPaymentsWaivedPerPayment\":0,\"MaxValueOfPaymentsWaived\":0,\"MaxNumberOfPaymentsWaived\":0,\"Cash\":1000}]}]},\"ProgramRuleList\":[{\"Description\":\"Eligible customers that currently own or lease a Volvo or Saab vehicle.\",\"Type\":\"Eligibility\"},{\"Description\":\"Individuals or members of the same household who currently owns\/leases any model year Volvo or Saab vehicle OR has owned\/leased either within the last 6 months.\",\"Type\":\"Qualification\"}],\"InstitutionList\":[],\"stackabilityIncentiveIDs\":[],\"ExpiryDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"stackableWith\":\"\",\"IncentiveId\":\"14928639\",\"ExpiryDate\":\"2019-05-31\",\"EffectiveDate\":\"2019-05-01\",\"EndRecipient\":\"Customer\",\"GeoDesc\":\"Volvo US Western Market 1302 - Los Angeles North\",\"PreviousOwnership\":\"Loyalty\",\"CategoryDescription\":\"Bonus Cash\",\"ProgramNumber\":\"62751\",\"ProgramDescription\":\"WR Loyalty Bonus - Purchase\",\"GroupAffiliation\":\"No Specific Group Affiliation\",\"Source\":\"OEM\",\"Market\":\"Retail\",\"Type\":\"Cash\",\"CategoryId\":\"123\"}],\"FinanceIncentives\":[],\"LeaseIncentives\":[{\"SignatureHistoryId\":29966,\"SignatureId\":743,\"VehicleStatusList\":[\"New\"],\"DeliveryTypeList\":[\"Subvented Lease\"],\"ProgramValues\":{\"ValueVariationList\":[{\"ProgramValueList\":[{\"NumberOfDays\":0,\"MaxValueOfPaymentsWaivedPerPayment\":0,\"MaxValueOfPaymentsWaived\":0,\"MaxNumberOfPaymentsWaived\":0,\"Cash\":0,\"TermList\":[{\"MileageRestrictionsTo\":24,\"MileageRestrictionsFrom\":24,\"From\":24,\"To\":24,\"AmountFinancedTo\":0,\"AmountFinancedFrom\":0,\"Variance\":0,\"Value\":0.00172},{\"MileageRestrictionsTo\":30,\"MileageRestrictionsFrom\":30,\"From\":30,\"To\":30,\"AmountFinancedTo\":0,\"AmountFinancedFrom\":0,\"Variance\":0,\"Value\":0.00172},{\"MileageRestrictionsTo\":36,\"MileageRestrictionsFrom\":36,\"From\":36,\"To\":36,\"AmountFinancedTo\":0,\"AmountFinancedFrom\":0,\"Variance\":0,\"Value\":0.00172},{\"MileageRestrictionsTo\":39,\"MileageRestrictionsFrom\":39,\"From\":39,\"To\":39,\"AmountFinancedTo\":0,\"AmountFinancedFrom\":0,\"Variance\":0,\"Value\":0.00172},{\"MileageRestrictionsTo\":48,\"MileageRestrictionsFrom\":48,\"From\":48,\"To\":48,\"AmountFinancedTo\":0,\"AmountFinancedFrom\":0,\"Variance\":0,\"Value\":0.0022}]}],\"Tiers\":\"1\"}]},\"ProgramRuleList\":[{\"Description\":\"Residents residing in qualifying regions of the United States. O.A.C.\",\"Type\":\"Eligibility\"}],\"InstitutionList\":[],\"stackabilityIncentiveIDs\":[744,12781,12782,9110],\"ExpiryDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"stackableWith\":\"744|12781|12782|9110\",\"IncentiveId\":\"14928386\",\"ExpiryDate\":\"2019-05-31\",\"EffectiveDate\":\"2019-05-01\",\"EndRecipient\":\"Customer\",\"GeoDesc\":\"Volvo US Western Market 1302 - Los Angeles North\",\"PreviousOwnership\":\"No Previous Ownership Requirement\",\"CategoryDescription\":\"Lease Rate\",\"ProgramNumber\":\"19-0085\",\"ProgramDescription\":\"Subvented Lease Factors\",\"GroupAffiliation\":\"No Specific Group Affiliation\",\"Source\":\"OEM\",\"Market\":\"Retail\",\"Type\":\"Lease Rate\",\"CategoryId\":\"109\"}]},\"TcuvStructuredIncentives\":{}}},\"features\":{\"featuresStructured\":{\"MECHANICAL\":[\"14.2 Gal. Fuel Tank\",\"3.33 Axle Ratio\",\"4-Wheel Disc Brakes w\/4-Wheel ABS, Front Vented Discs, Brake Assist, Hill Descent Control, Hill Hold Control and Electric Parking Brake\",\"925lbs. Maximum Payload\",\"Battery w\/Run Down Protection\",\"Brake Actuated Limited Slip Differential\",\"Double Wishbone Front Suspension w\/Coil Springs\",\"Electric Power-Assist Speed-Sensing Steering\",\"Engine: 2.0L I4 Direct-Injected Turbo-Charged\",\"Front And Rear Anti-Roll Bars\",\"Full-Time All-Wheel Drive\",\"GVWR: 4,895 lbs (2,220 kgs)\",\"Gas-Pressurized Shock Absorbers\",\"Multi-Link Rear Suspension w\/Transverse Leaf Springs\",\"Permanent Locking Hubs\",\"Quasi-Dual Stainless Steel Exhaust\",\"Towing Equipment -inc: Trailer Sway Control\",\"Transmission w\/Driver Selectable Mode\",\"Transmission: 8-Speed Geartronic Automatic -inc: start\/stop\"],\"INTERIOR\":[\"2 12V DC Power Outlets\",\"2 Seatback Storage Pockets\",\"8-Way Driver Seat\",\"8-Way Passenger Seat -inc: Manual Recline, Height Adjustment, Fore\/Aft Movement and Cushion Tilt\",\"Air Filtration\",\"Cargo Area Concealed Storage\",\"Cargo Space Lights\",\"Carpet Floor Trim and Carpet Trunk Lid\/Rear Cargo Door Trim\",\"Cloth Door Trim Insert\",\"Day-Night Rearview Mirror\",\"Delayed Accessory Power\",\"Digital\/Analog Display\",\"Driver \/ Passenger And Rear Door Bins\",\"Driver And Passenger Visor Vanity Mirrors w\/Driver And Passenger Illumination\",\"Driver Foot Rest\",\"Engine Immobilizer\",\"Fade-To-Off Interior Lighting\",\"Front And Rear Map Lights\",\"Front Comfort Seats -inc: 8-way power driver seat w\/memory and 4-way power lumbar\",\"Front Cupholder\",\"Full Carpet Floor Covering -inc: Carpet Front And Rear Floor Mats\",\"Full Cloth Headliner\",\"Full Floor Console w\/Covered Storage and 2 12V DC Power Outlets\",\"HVAC -inc: Underseat Ducts\",\"Illuminated Locking Glove Box\",\"Interior Trim -inc: Piano Black\/Aluminum Instrument Panel Insert, Aluminum Door Panel Insert and Metal-Look Interior Accents\",\"Leather Gear Shift Knob\",\"Leather Steering Wheel\",\"Manual Anti-Whiplash Adjustable Front Head Restraints and Manual Adjustable Rear Head Restraints\",\"Manual Tilt\/Telescoping Steering Column\",\"Outside Temp Gauge\",\"Perimeter Alarm\",\"Rear Cupholder\",\"Redundant Digital Speedometer\",\"Rigid Cargo Cover\",\"Smart Device Remote Engine Start\",\"Systems Monitor\",\"Tracker System\",\"Trunk\/Hatch Auto-Latch\",\"Valet Function\"],\"ENTERTAINMENT\":[\"2 LCD Monitors In The Front\",\"330w Regular Amplifier\",\"Window Grid Diversity Antenna\"],\"SAFETY\":[\"Airbag Occupancy Sensor\",\"City Safety\",\"Curtain 1st And 2nd Row Airbags\",\"Driver Knee Airbag\",\"Dual Stage Driver And Passenger Front Airbags\",\"Dual Stage Driver And Passenger Seat-Mounted Side Airbags\",\"Outboard Front Lap And Shoulder Safety Belts -inc: Rear Center 3 Point, Height Adjusters and Pretensioners\",\"Side Impact Beams\",\"Tire Specific Low Tire Pressure Warning\",\"Volvo On-Call Emergency Sos\"],\"EXTERIOR\":[\"Black Bodyside Cladding and Black Wheel Well Trim\",\"Black Grille w\/Chrome Surround\",\"Black Side Windows Trim and Black Front Windshield Trim\",\"Body-Colored Door Handles\",\"Body-Colored Front Bumper w\/Black Rub Strip\/Fascia Accent and Metal-Look Bumper Insert\",\"Body-Colored Power w\/Tilt Down Heated Side Mirrors w\/Manual Folding and Turn Signal Indicator\",\"Body-Colored Rear Bumper w\/Black Rub Strip\/Fascia Accent and Metal-Look Bumper Insert\",\"Clearcoat Paint\",\"Compact Spare Tire Mounted Inside Under Cargo\",\"Deep Tinted Glass\",\"Fixed Rear Window w\/Fixed Interval Wiper and Defroster\",\"Galvanized Steel\/Aluminum Panels\",\"LED Brakelights\",\"Lip Spoiler\",\"Rear Fog Lamps\",\"Roof Rack Rails Only\",\"Steel Spare Wheel\"]},\"safetyFeatures\":[\"Airbag Occupancy Sensor\",\"City Safety\",\"Curtain 1st And 2nd Row Airbags\",\"Driver Knee Airbag\",\"Dual Stage Driver And Passenger Front Airbags\",\"Dual Stage Driver And Passenger Seat-Mounted Side Airbags\",\"Outboard Front Lap And Shoulder Safety Belts -inc: Rear Center 3 Point, Height Adjusters and Pretensioners\",\"Side Impact Beams\",\"Tire Specific Low Tire Pressure Warning\",\"Volvo On-Call Emergency Sos\"],\"mechanicalFeatures\":[\"14.2 Gal. Fuel Tank\",\"3.33 Axle Ratio\",\"4-Wheel Disc Brakes w\/4-Wheel ABS, Front Vented Discs, Brake Assist, Hill Descent Control, Hill Hold Control and Electric Parking Brake\",\"925lbs. Maximum Payload\",\"Battery w\/Run Down Protection\",\"Brake Actuated Limited Slip Differential\",\"Double Wishbone Front Suspension w\/Coil Springs\",\"Electric Power-Assist Speed-Sensing Steering\",\"Engine: 2.0L I4 Direct-Injected Turbo-Charged\",\"Front And Rear Anti-Roll Bars\",\"Full-Time All-Wheel Drive\",\"GVWR: 4,895 lbs (2,220 kgs)\",\"Gas-Pressurized Shock Absorbers\",\"Multi-Link Rear Suspension w\/Transverse Leaf Springs\",\"Permanent Locking Hubs\",\"Quasi-Dual Stainless Steel Exhaust\",\"Towing Equipment -inc: Trailer Sway Control\",\"Transmission w\/Driver Selectable Mode\",\"Transmission: 8-Speed Geartronic Automatic -inc: start\/stop\"],\"interiorFeatures\":[\"2 12V DC Power Outlets\",\"2 Seatback Storage Pockets\",\"8-Way Driver Seat\",\"8-Way Passenger Seat -inc: Manual Recline, Height Adjustment, Fore\/Aft Movement and Cushion Tilt\",\"Air Filtration\",\"Cargo Area Concealed Storage\",\"Cargo Space Lights\",\"Carpet Floor Trim and Carpet Trunk Lid\/Rear Cargo Door Trim\",\"Cloth Door Trim Insert\",\"Day-Night Rearview Mirror\",\"Delayed Accessory Power\",\"Digital\/Analog Display\",\"Driver \/ Passenger And Rear Door Bins\",\"Driver And Passenger Visor Vanity Mirrors w\/Driver And Passenger Illumination\",\"Driver Foot Rest\",\"Engine Immobilizer\",\"Fade-To-Off Interior Lighting\",\"Front And Rear Map Lights\",\"Front Comfort Seats -inc: 8-way power driver seat w\/memory and 4-way power lumbar\",\"Front Cupholder\",\"Full Carpet Floor Covering -inc: Carpet Front And Rear Floor Mats\",\"Full Cloth Headliner\",\"Full Floor Console w\/Covered Storage and 2 12V DC Power Outlets\",\"HVAC -inc: Underseat Ducts\",\"Illuminated Locking Glove Box\",\"Interior Trim -inc: Piano Black\/Aluminum Instrument Panel Insert, Aluminum Door Panel Insert and Metal-Look Interior Accents\",\"Leather Gear Shift Knob\",\"Leather Steering Wheel\",\"Manual Anti-Whiplash Adjustable Front Head Restraints and Manual Adjustable Rear Head Restraints\",\"Manual Tilt\/Telescoping Steering Column\",\"Outside Temp Gauge\",\"Perimeter Alarm\",\"Rear Cupholder\",\"Redundant Digital Speedometer\",\"Rigid Cargo Cover\",\"Smart Device Remote Engine Start\",\"Systems Monitor\",\"Tracker System\",\"Trunk\/Hatch Auto-Latch\",\"Valet Function\"],\"exteriorFeatures\":[\"Black Bodyside Cladding and Black Wheel Well Trim\",\"Black Grille w\/Chrome Surround\",\"Black Side Windows Trim and Black Front Windshield Trim\",\"Body-Colored Door Handles\",\"Body-Colored Front Bumper w\/Black Rub Strip\/Fascia Accent and Metal-Look Bumper Insert\",\"Body-Colored Power w\/Tilt Down Heated Side Mirrors w\/Manual Folding and Turn Signal Indicator\",\"Body-Colored Rear Bumper w\/Black Rub Strip\/Fascia Accent and Metal-Look Bumper Insert\",\"Clearcoat Paint\",\"Compact Spare Tire Mounted Inside Under Cargo\",\"Deep Tinted Glass\",\"Fixed Rear Window w\/Fixed Interval Wiper and Defroster\",\"Galvanized Steel\/Aluminum Panels\",\"LED Brakelights\",\"Lip Spoiler\",\"Rear Fog Lamps\",\"Roof Rack Rails Only\",\"Steel Spare Wheel\"],\"entertainmentFeatures\":[\"2 LCD Monitors In The Front\",\"330w Regular Amplifier\",\"Window Grid Diversity Antenna\"],\"genericEquipment\":[\"Driver Air Bag\",\"Passenger Air Bag\",\"Front Side Air Bag\",\"Front Head Air Bag\",\"Rear Head Air Bag\",\"Climate Control\",\"A\/C\",\"Security System\",\"AM\/FM Stereo\",\"ABS\",\"4-Wheel Disc Brakes\",\"Cruise Control\",\"Rear Defrost\",\"Child Safety Locks\",\"All Wheel Drive\",\"4 Cylinder Engine\",\"Turbocharged\",\"Floor Mats\",\"Gasoline Fuel\",\"Daytime Running Lights\",\"Keyless Entry\",\"Power Door Locks\",\"Heated Mirrors\",\"Power Mirror(s)\",\"Power Driver Seat\",\"Pass-Through Rear Seat\",\"Leather Seats\",\"Bucket Seats\",\"Adjustable Steering Wheel\",\"Tires - Front Performance\",\"Tires - Rear Performance\",\"Temporary Spare Tire\",\"Traction Control\",\"Aluminum Wheels\",\"Power Windows\",\"Intermittent Wipers\",\"A\/T\",\"Satellite Radio\",\"MP3 Player\",\"Privacy Glass\",\"Variable Speed Intermittent Wipers\",\"Rain Sensing Wipers\",\"Steering Wheel Audio Controls\",\"Engine Immobilizer\",\"Automatic Headlights\",\"Integrated Turn Signal Mirrors\",\"Driver Vanity Mirror\",\"Passenger Vanity Mirror\",\"Driver Illuminated Vanity Mirror\",\"Passenger Illuminated Visor Mirror\",\"Mirror Memory\",\"Driver Adjustable Lumbar\",\"Seat Memory\",\"Leather Steering Wheel\",\"Rear Spoiler\",\"Remote Trunk Release\",\"Tire Pressure Monitor\",\"Trip Computer\",\"Bluetooth Connection\",\"Telematics\",\"8-Speed A\/T\",\"Remote Engine Start\",\"Back-Up Camera\",\"Power Liftgate\",\"Stability Control\",\"Brake Assist\",\"Keyless Start\",\"Auxiliary Audio Input\",\"Cargo Shade\",\"HD Radio\",\"Rear Bench Seat\",\"Passenger Air Bag Sensor\",\"Headlights-Auto-Leveling\",\"Lane Departure Warning\",\"Knee Air Bag\",\"Lane Keeping Assist\",\"WiFi Hotspot\",\"Brake Actuated Limited Slip Differential\",\"Smart Device Integration\"]},\"warranties\":[\"4 year \/ 50,000 mile limited warranty\",\"12 year \/ Unlimited mile corrosion warranty\",\"4 year \/ 50,000 mile drivetrain warranty\",\"4 year \/ Unlimited mile Roadside Assistance \"],\"stockNumber\":\"V190804\",\"conditions\":[\"New\"],\"used\":\"0\",\"year\":\"2019\",\"make\":\"Volvo\",\"model\":\"XC40\",\"trim\":\"Momentum\",\"status\":\"On Lot\",\"mileage\":6,\"displayPrice\":37795,\"formattedPrice\":\"$37,795\",\"price\":\"37,795\",\"pricing\":[{\"Value\":37795,\"DisplayOnMobile\":true,\"DisplayOnFull\":true,\"DetailsPageVisible\":true,\"ListPageVisible\":true,\"DisplayOrder\":0,\"Type\":\"Currency\",\"Priority\":10,\"Source\":\"PricingField#415\",\"RowClass\":\"pricing_0\",\"ValueClass\":\"pricing_value_0\",\"LabelClass\":\"pricing_label_0\",\"Label\":\"MSRP\",\"Text\":\"$37,795\",\"Name\":\"@MSRP\"}],\"packages\":[{\"Standard\":false,\"Price\":0,\"Name\":[\"Ice White\"],\"InstallationCause\":\"RelatedColor\",\"Code\":\"614\",\"Category\":\"PRIMARY PAINT\"},{\"Standard\":false,\"Price\":0,\"Name\":[\"Charcoal, Leather Seating Surfaces\"],\"CategoryId\":[1078],\"InstallationCause\":\"RelatedColor\",\"Code\":\"RD00\",\"Category\":\"SEAT TRIM\"}],\"vehicleHighlights\":[\"Brake Actuated Limited Slip Differential\",\"Rigid Cargo Cover\",\"Full-Time All-Wheel Drive\",\"Transmission: 8-Speed Geartronic Automatic -inc: start\/stop\",\"Engine: 2.0L I4 Direct-Injected Turbo-Charged\"],\"tags\":[\"MPG+\"],\"expando\":{\"stack\":{\"ExpirationDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"ChromeStructuredIncentiveStacks\":{\"LowestPaymentLeaseDeal\":{\"Term\":48,\"TotalCash\":0,\"MonthlyPayment\":871,\"Apr\":5.28,\"Incentives\":[{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Subvented Lease Factors\",\"SignatureId\":\"743\",\"IncentiveId\":\"14928386\",\"CategoryDescription\":\"Lease Rate\"},{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Residuals Values\",\"SignatureId\":\"744\",\"IncentiveId\":\"14935144\",\"CategoryDescription\":\"Residual\"}],\"ExpiryDate\":\"6\/1\/2019 3:59:59 AM\",\"EffectiveDate\":\"5\/1\/2019 4:00:00 AM\"}},\"TcuvStructuredIncentiveStacks\":{}}},\"dealerDescription\":null,\"techSpecs\":[{\"Value\":[{\"Value\":\"Volvo XC40\"}],\"HeaderId\":16,\"GroupId\":7,\"TitleId\":1,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Summary\",\"Group\":\"Summary\",\"Title\":\"Vehicle Name\"},{\"Value\":[{\"Value\":\"Sport Utility\"}],\"HeaderId\":16,\"GroupId\":7,\"TitleId\":2,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Summary\",\"Group\":\"Summary\",\"Title\":\"Body Style\"},{\"Value\":[{\"Value\":\"All Wheel Drive\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":6,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Drivetrain\"},{\"Value\":[{\"Value\":\"Small Sport Utility Vehicles 4WD\"}],\"HeaderId\":0,\"GroupId\":0,\"TitleId\":7,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Vehicle\",\"Group\":\"Vehicle\",\"Title\":\"EPA Classification\"},{\"Value\":[{\"Value\":\"5\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":8,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Passenger Capacity\"},{\"Value\":[{\"Value\":\"3729\"}],\"HeaderId\":9,\"GroupId\":4,\"TitleId\":10,\"MeasurementUnit\":\"lbs\",\"Header\":\"Weight Information\",\"Group\":\"Chassis\",\"Title\":\"Base Curb Weight\"},{\"Value\":[{\"Value\":\"26\"}],\"HeaderId\":14,\"GroupId\":6,\"TitleId\":25,\"MeasurementUnit\":\"MPG\",\"Header\":\"Mileage\",\"Group\":\"Powertrain\",\"Title\":\"Fuel Economy Est-Combined\"},{\"Value\":[{\"Value\":\"23\"}],\"HeaderId\":14,\"GroupId\":6,\"TitleId\":26,\"MeasurementUnit\":\"MPG\",\"Header\":\"Mileage\",\"Group\":\"Powertrain\",\"Title\":\"EPA Fuel Economy Est - City\"},{\"Value\":[{\"Value\":\"31\"}],\"HeaderId\":14,\"GroupId\":6,\"TitleId\":27,\"MeasurementUnit\":\"MPG\",\"Header\":\"Mileage\",\"Group\":\"Powertrain\",\"Title\":\"EPA Fuel Economy Est - Hwy\"},{\"Value\":[{\"Value\":\"3500\"}],\"HeaderId\":8,\"GroupId\":4,\"TitleId\":31,\"MeasurementUnit\":\"lbs\",\"Header\":\"Trailering\",\"Group\":\"Chassis\",\"Title\":\"Dead Weight Hitch - Max Trailer Wt.\"},{\"Value\":[{\"Value\":\"350\"}],\"HeaderId\":8,\"GroupId\":4,\"TitleId\":32,\"MeasurementUnit\":\"lbs\",\"Header\":\"Trailering\",\"Group\":\"Chassis\",\"Title\":\"Dead Weight Hitch - Max Tongue Wt.\"},{\"Value\":[{\"Value\":\"3500\"}],\"HeaderId\":8,\"GroupId\":4,\"TitleId\":33,\"MeasurementUnit\":\"lbs\",\"Header\":\"Trailering\",\"Group\":\"Chassis\",\"Title\":\"Wt Distributing Hitch - Max Trailer Wt.\"},{\"Value\":[{\"Value\":\"350\"}],\"HeaderId\":8,\"GroupId\":4,\"TitleId\":34,\"MeasurementUnit\":\"lbs\",\"Header\":\"Trailering\",\"Group\":\"Chassis\",\"Title\":\"Wt Distributing Hitch - Max Tongue Wt.\"},{\"Value\":[{\"Value\":\"3500\"}],\"HeaderId\":8,\"GroupId\":4,\"TitleId\":37,\"MeasurementUnit\":\"lbs\",\"Header\":\"Trailering\",\"Group\":\"Chassis\",\"Title\":\"Maximum Trailering Capacity\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":40,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Order Code\"},{\"Value\":[{\"Value\":\"Intercooled Turbo Regular Unleaded I-4\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":41,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Type\"},{\"Value\":[{\"Value\":\"2.0 L\/120\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":42,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Displacement\"},{\"Value\":[{\"Value\":\"Gasoline Direct Injection\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":43,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Fuel System\"},{\"Value\":[{\"Value\":\"248 @ 5500\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":48,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"SAE Net Horsepower @ RPM\"},{\"Value\":[{\"Value\":\"258 @ 1800\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":49,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"SAE Net Torque @ RPM\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":51,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Trans Order Code\"},{\"Value\":[{\"Value\":\"8\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":52,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Trans Type\"},{\"Value\":[{\"Value\":\"Automatic w\/OD\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":53,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Trans Description Cont.\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":54,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Trans Description Cont. Again\"},{\"Value\":[{\"Value\":\"5.25\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":56,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"First Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"3.03\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":57,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Second Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"1.95\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":58,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Third Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"1.46\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":59,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Fourth Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"1.22\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":60,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Fifth Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"1.00\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":61,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Sixth Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"4.01\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":62,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Reverse Ratio (:1)\"},{\"Value\":[{\"Value\":\"3.33\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":69,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Final Drive Axle Ratio (:1)\"},{\"Value\":[{\"Value\":\"6.8\"}],\"HeaderId\":48,\"GroupId\":0,\"TitleId\":81,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Emissions\",\"Group\":\"Vehicle\",\"Title\":\"Tons\/yr of CO2 Emissions @ 15K mi\/year\"},{\"Value\":[{\"Value\":\"Double Wishbone\"}],\"HeaderId\":17,\"GroupId\":4,\"TitleId\":105,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Suspension\",\"Group\":\"Chassis\",\"Title\":\"Suspension Type - Front\"},{\"Value\":[{\"Value\":\"Multi-Link\"}],\"HeaderId\":17,\"GroupId\":4,\"TitleId\":106,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Suspension\",\"Group\":\"Chassis\",\"Title\":\"Suspension Type - Rear\"},{\"Value\":[{\"Value\":\"Double Wishbone\"}],\"HeaderId\":17,\"GroupId\":4,\"TitleId\":107,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Suspension\",\"Group\":\"Chassis\",\"Title\":\"Suspension Type - Front (Cont.)\"},{\"Value\":[{\"Value\":\"Multi-Link\"}],\"HeaderId\":17,\"GroupId\":4,\"TitleId\":108,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Suspension\",\"Group\":\"Chassis\",\"Title\":\"Suspension Type - Rear (Cont.)\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":137,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Front Tire Order Code\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":138,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Rear Tire Order Code\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":139,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Spare Tire Order Code\"},{\"Value\":[{\"Condition\":\"-NONTR1\",\"Value\":\"P235\/45HR20\"},{\"Condition\":\"-NONTR2\",\"Value\":\"P235\/50HR19\"},{\"Value\":\"P235\/55HR18\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":140,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Front Tire Size\"},{\"Value\":[{\"Condition\":\"-NONTR1\",\"Value\":\"P235\/45HR20\"},{\"Condition\":\"-NONTR2\",\"Value\":\"P235\/50HR19\"},{\"Value\":\"P235\/55HR18\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":141,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Rear Tire Size\"},{\"Value\":[{\"Value\":\"Compact\"}],\"HeaderId\":7,\"GroupId\":4,\"TitleId\":142,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Tires\",\"Group\":\"Chassis\",\"Title\":\"Spare Tire Size\"},{\"Value\":[{\"Value\":\"18 X 7.5\"},{\"Condition\":\"922,923\",\"Value\":\"19 X 7.5\"},{\"Condition\":\"917\",\"Value\":\"20 X 8\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":156,\"MeasurementUnit\":\"in\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Front Wheel Size\"},{\"Value\":[{\"Value\":\"18 X 7.5\"},{\"Condition\":\"922,923\",\"Value\":\"19 X 7.5\"},{\"Condition\":\"917\",\"Value\":\"20 X 8\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":157,\"MeasurementUnit\":\"in\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Rear Wheel Size\"},{\"Value\":[{\"Value\":\"Compact\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":158,\"MeasurementUnit\":\"in\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Spare Wheel Size\"},{\"Value\":[{\"Value\":\"Aluminum\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":165,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Front Wheel Material\"},{\"Value\":[{\"Value\":\"Aluminum\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":166,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Rear Wheel Material\"},{\"Value\":[{\"Value\":\"Steel\"}],\"HeaderId\":10,\"GroupId\":4,\"TitleId\":167,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Wheels\",\"Group\":\"Chassis\",\"Title\":\"Spare Wheel Material\"},{\"Value\":[{\"Value\":\"Rack-Pinion\"}],\"HeaderId\":6,\"GroupId\":4,\"TitleId\":176,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Steering\",\"Group\":\"Chassis\",\"Title\":\"Steering Type\"},{\"Value\":[{\"Value\":\"37.4\"}],\"HeaderId\":6,\"GroupId\":4,\"TitleId\":184,\"MeasurementUnit\":\"ft\",\"Header\":\"Steering\",\"Group\":\"Chassis\",\"Title\":\"Turning Diameter - Curb to Curb\"},{\"Value\":[{\"Value\":\"4-Wheel Disc\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":186,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Brake Type\"},{\"Value\":[{\"Value\":\"4-Wheel\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":187,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Brake ABS System\"},{\"Value\":[{\"Value\":\"Yes\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":190,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Disc - Front (Yes or )\"},{\"Value\":[{\"Value\":\"Yes\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":191,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Disc - Rear (Yes or )\"},{\"Value\":[{\"Value\":\"13.6\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":192,\"MeasurementUnit\":\"in\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Front Brake Rotor Diam x Thickness\"},{\"Value\":[{\"Value\":\"11.9\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":193,\"MeasurementUnit\":\"in\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Rear Brake Rotor Diam x Thickness\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":196,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Drum - Rear (Yes or )\"},{\"Value\":[{\"Value\":\"\"}],\"HeaderId\":4,\"GroupId\":4,\"TitleId\":197,\"MeasurementUnit\":\"in\",\"Header\":\"Brakes\",\"Group\":\"Chassis\",\"Title\":\"Rear Drum Diam x Width\"},{\"Value\":[{\"Value\":\"14.2\"}],\"HeaderId\":5,\"GroupId\":4,\"TitleId\":206,\"MeasurementUnit\":\"gal\",\"Header\":\"Fuel Tank\",\"Group\":\"Chassis\",\"Title\":\"Fuel Tank Capacity, Approx\"},{\"Value\":[{\"Condition\":\"30-0\",\"Value\":\"37.6\"},{\"Value\":\"39\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":256,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Front Head Room\"},{\"Value\":[{\"Value\":\"40.9\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":257,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Front Leg Room\"},{\"Value\":[{\"Value\":\"56.7\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":258,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Front Shoulder Room\"},{\"Value\":[{\"Value\":\"54.7\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":259,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Front Hip Room\"},{\"Value\":[{\"Condition\":\"30-0\",\"Value\":\"38.3\"},{\"Value\":\"39.1\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":261,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Second Head Room\"},{\"Value\":[{\"Value\":\"36.1\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":262,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Second Leg Room\"},{\"Value\":[{\"Value\":\"56.3\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":263,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Second Shoulder Room\"},{\"Value\":[{\"Value\":\"54.6\"}],\"HeaderId\":1,\"GroupId\":5,\"TitleId\":264,\"MeasurementUnit\":\"in\",\"Header\":\"Interior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Second Hip Room\"},{\"Value\":[{\"Value\":\"106.4\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":301,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Wheelbase\"},{\"Value\":[{\"Value\":\"73.3\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":305,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Width, Max w\/o mirrors\"},{\"Value\":[{\"Value\":\"65.3\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":306,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Height, Overall\"},{\"Value\":[{\"Value\":\"63\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":309,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Track Width, Front\"},{\"Value\":[{\"Value\":\"64\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":310,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Track Width, Rear\"},{\"Value\":[{\"Value\":\"8.3\"}],\"HeaderId\":2,\"GroupId\":5,\"TitleId\":326,\"MeasurementUnit\":\"in\",\"Header\":\"Exterior Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Min Ground Clearance\"},{\"Value\":[{\"Value\":\"65.7\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":353,\"MeasurementUnit\":\"in\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Area Length @ Floor to Seat 1\"},{\"Value\":[{\"Value\":\"34.9\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":354,\"MeasurementUnit\":\"in\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Area Length @ Floor to Seat 2\"},{\"Value\":[{\"Value\":\"41.7\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":362,\"MeasurementUnit\":\"in\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Area Width @ Beltline\"},{\"Value\":[{\"Value\":\"37.3\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":364,\"MeasurementUnit\":\"in\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Box Width @ Wheelhousings\"},{\"Value\":[{\"Value\":\"29.4\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":366,\"MeasurementUnit\":\"in\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Box (Area) Height\"},{\"Value\":[{\"Value\":\"47.2\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":372,\"MeasurementUnit\":\"ft\u00b3\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Volume to Seat 1\"},{\"Value\":[{\"Value\":\"20.7\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":373,\"MeasurementUnit\":\"ft\u00b3\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Volume to Seat 2\"},{\"Value\":[{\"Value\":\"20.7\"}],\"HeaderId\":3,\"GroupId\":5,\"TitleId\":374,\"MeasurementUnit\":\"ft\u00b3\",\"Header\":\"Cargo Area Dimensions\",\"Group\":\"Dimensions\",\"Title\":\"Cargo Volume to Seat 3\"},{\"Value\":[{\"Value\":\"0.81\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":401,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Seventh Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"0.67\"}],\"HeaderId\":15,\"GroupId\":6,\"TitleId\":402,\"MeasurementUnit\":\"N\/A\",\"Header\":\"Transmission\",\"Group\":\"Powertrain\",\"Title\":\"Eighth Gear Ratio (:1)\"},{\"Value\":[{\"Value\":\"Sweden Goteborg Multi-Purpose Passenger Vehicles \"}],\"HeaderId\":0,\"GroupId\":0,\"TitleId\":1110,\"Header\":\"Vehicle\",\"Group\":\"Vehicle\",\"Title\":\"Country of Origin\"},{\"Value\":[{\"Value\":\"XC40\"}],\"HeaderId\":0,\"GroupId\":0,\"TitleId\":1112,\"Header\":\"Vehicle\",\"Group\":\"Vehicle\",\"Title\":\"Model Group\"},{\"Value\":[{\"Value\":\"Compact Luxury Sport Utility\"}],\"HeaderId\":0,\"GroupId\":0,\"TitleId\":1113,\"Header\":\"Vehicle\",\"Group\":\"Vehicle\",\"Title\":\"Vehicle Segment\"},{\"Value\":[{\"Value\":\"Sport Utility\"}],\"HeaderId\":0,\"GroupId\":0,\"TitleId\":1114,\"Header\":\"Vehicle\",\"Group\":\"Vehicle\",\"Title\":\"Vehicle Type\"},{\"Value\":[{\"Value\":\"2.0\"},{\"Condition\":\"STDEN\",\"Value\":\"2.0\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":1117,\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Displacement Units\"},{\"Value\":[{\"Value\":\"DOHC\"},{\"Condition\":\"STDEN\",\"Value\":\"DOHC\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":1118,\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Camshaft\"},{\"Value\":[{\"Value\":\"aluminum\"},{\"Condition\":\"STDEN\",\"Value\":\"aluminum\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":1119,\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Block Type\"},{\"Value\":[{\"Value\":\"4\"},{\"Condition\":\"STDEN\",\"Value\":\"4\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":1120,\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Cylinder Count\"},{\"Value\":[{\"Value\":\"4\"},{\"Condition\":\"STDEN\",\"Value\":\"4\"}],\"HeaderId\":13,\"GroupId\":6,\"TitleId\":1121,\"Header\":\"Engine\",\"Group\":\"Powertrain\",\"Title\":\"Engine Valve Count\"}],\"legacyFields\":{\"id\":\"1438455\",\"vin\":\"YV4162UK3K2134791\",\"account_id\":\"20\",\"account_name\":\"Galpin Premier\",\"interior_factory_color\":\"Charcoal\",\"exterior_factory_color\":\"Ice White\",\"exterior_generic_color\":\"White\",\"drivetrain\":\"All Wheel Drive\",\"transmission\":\"Automatic\",\"condition\":\"New\",\"fuel_type\":\"Gasoline\",\"imageCount\":\"4\",\"hasVideo\":false,\"location_city\":\"Van Nuys\",\"location_state\":\"CA\",\"location_address1\":\"15500 Roscoe Blvd.\",\"location_zipcode\":\"91406\",\"location_contact_number\":\"(888) 712-0182\",\"imageUrl\":\"\/media\/38229186\",\"used\":\"0\",\"year\":\"2019\",\"make\":\"Volvo\",\"model\":\"XC40\",\"trim\":\"Momentum\",\"mpg_city_low\":\"23\",\"mpg_highway_low\":\"31\",\"style_name\":\"T5 AWD Momentum\",\"drivetrain_code\":\"AWD\",\"stock_number\":\"V190804\",\"packages\":[{\"Standard\":false,\"Price\":0,\"Name\":[\"Ice White\"],\"InstallationCause\":\"RelatedColor\",\"Code\":\"614\",\"Category\":\"PRIMARY PAINT\"},{\"Standard\":false,\"Price\":0,\"Name\":[\"Charcoal, Leather Seating Surfaces\"],\"CategoryId\":[1078],\"InstallationCause\":\"RelatedColor\",\"Code\":\"RD00\",\"Category\":\"SEAT TRIM\"}],\"engine_cylinders\":\"4 Cylinders\",\"hasCarfax\":false,\"carfaxOneOwner\":false,\"hasAutocheck\":false,\"incentivesStack\":{\"ExpirationDateUtc\":\"\/Date(1559361599000)\/\",\"EffectiveDateUtc\":\"\/Date(1556683200000)\/\",\"ChromeStructuredIncentiveStacks\":{\"LowestPaymentLeaseDeal\":{\"Term\":48,\"TotalCash\":0,\"MonthlyPayment\":871,\"Apr\":5.28,\"Incentives\":[{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Subvented Lease Factors\",\"SignatureId\":\"743\",\"IncentiveId\":\"14928386\",\"CategoryDescription\":\"Lease Rate\"},{\"ProgramValue\":\"-1\",\"ProgramDescription\":\"Residuals Values\",\"SignatureId\":\"744\",\"IncentiveId\":\"14935144\",\"CategoryDescription\":\"Residual\"}],\"ExpiryDate\":\"6\/1\/2019 3:59:59 AM\",\"EffectiveDate\":\"5\/1\/2019 4:00:00 AM\"}},\"TcuvStructuredIncentiveStacks\":{}},\"certifiedByManufacturer\":false,\"mileage\":\"6\",\"vehicleHighlights\":[\"Brake Actuated Limited Slip Differential\",\"Rigid Cargo Cover\",\"Full-Time All-Wheel Drive\",\"Transmission: 8-Speed Geartronic Automatic -inc: start\/stop\",\"Engine: 2.0L I4 Direct-Injected Turbo-Charged\"],\"price\":\"37,795\",\"display_price\":\"37795.0\",\"vehicle_type\":[\"Sport Utility\"],\"pricing\":[{\"Value\":37795,\"DisplayOnMobile\":true,\"DisplayOnFull\":true,\"DetailsPageVisible\":true,\"ListPageVisible\":true,\"DisplayOrder\":0,\"Type\":\"Currency\",\"Priority\":10,\"Source\":\"PricingField#415\",\"RowClass\":\"pricing_0\",\"ValueClass\":\"pricing_value_0\",\"LabelClass\":\"pricing_label_0\",\"Label\":\"MSRP\",\"Text\":\"$37,795\",\"Name\":\"@MSRP\"}],\"specifications\":[{\"name\":\"MPG City\",\"value\":\"23\"},{\"name\":\"MPG Hwy\",\"value\":\"31\"},{\"name\":\"Exterior Color\",\"value\":\"Ice White\"},{\"name\":\"Interior Color\",\"value\":\"Charcoal\"},{\"name\":\"Transmission\",\"value\":\"Automatic\"},{\"name\":\"Stock #\",\"value\":\"V190804\"},{\"name\":\"VIN\",\"value\":\"YV4162UK3K2134791\"}],\"image\":{\"Id\":38229186,\"VisibleShortUrl\":\"\/media\/38229186\",\"Base64\":\"\/9j\/4AAQSkZJRgABAQEAYABgAAD\/2wBDAP\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/2wBDAf\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/wAARCABLAGQDASIAAhEBAxEB\/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL\/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6\/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL\/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6\/9oADAMBAAIRAxEAPwCSiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKQnFAC0mRTeT1pp64FAD9w\/yaNw\/yRUefWk60ATZpNwpmM\/QUdKAJM0tRjrxTxQAtFFFABSZoPSoySDQBJSVHk0bjQBJgUm0elJzRz7\/AJ0ALtFGBR060gbNABjHfilwKKKADgdBS89qSmZOc0ATUUUUANNN3D\/IpxGRUXTqKAFz9Pyp\/HtUfFLigB5OKTdmm7u3X60Z9hQAp5OD0ptKP5c0H68UAOyPWjcPSmUZ9hQA4tn2pB270cnt+VKAfSgB+aKSigBaQjNLRQAzbRsPrT6U0ARbTRtNSUooAjw1G01JSUAN2ilwBTu1JQAUUCg0AJRRRQB\/\/9k=\",\"VisibleUrl\":\"\/media\/38229186\",\"Source\":\"https:\/\/content.homenetiol.com\/682\/49506\/0x0\/b3db687e83974a83b4699946ebe78a0d.jpg\",\"IsColorMatch\":true,\"IsChromePressPhoto\":false,\"Width\":\"\",\"Height\":\"\",\"IsPlaceHolder\":false}},\"feeData\":{},\"vdpViewCount\":-1}},\"highlightsMap\":{},\"targetDetailLevelsMap\":{},\"loadingAfhVinsMap\":{}},\"uiState\":{\"filterUiState\":{},\"showFilterPanelOnFull\":false,\"showDisclaimerOnFull\":false,\"snapshotScriptLoaded\":false},\"geolocation\":{\"latlong\":null,\"needGeolocation\":true},\"matchMedia\":{\"mediaRanges\":[],\"matchedMedia\":[\"small\",\"medium\",\"large\"],\"width\":1025},\"user\":{\"defaultPaymentInfo\":{\"apr\":3.5,\"creditRating\":0,\"downPayment\":1995,\"termMonth\":72,\"tradeInValue\":0},\"paymentInfo\":{\"apr\":3.5,\"creditRating\":0,\"downPayment\":1995,\"termMonth\":72,\"tradeInValue\":0},\"groupAffiliations\":{\"military\":false,\"student\":false},\"contactInfo\":{\"firstName\":\"\",\"lastName\":\"\",\"email\":\"\",\"phone\":\"\",\"isConfirmed\":false},\"favoriteVehicles\":[],\"compareVehicles\":[],\"recentVehicles\":[],\"isVehiclesInitialized\":false,\"isLoggedIn\":false},\"cognito\":{\"awsRegion\":\"\",\"tableName\":\"\",\"userPoolId\":\"\",\"identityPoolId\":\"\",\"clientId\":\"\",\"vehicleSettings\":{\"enableFavoriteVehicles\":false,\"enableCompareVehicles\":false,\"enableRecentVehicles\":false},\"identityId\":\"\",\"user\":null,\"session\":null},\"routing\":{\"locationBeforeTransitions\":{\"pathname\":\"\/\",\"search\":\"\",\"hash\":\"\",\"state\":null,\"action\":\"POP\",\"key\":\"8qr5hi\",\"basename\":\"\",\"query\":{},\"$searchBase\":{\"search\":\"\",\"searchBase\":\"\"}}},\"fees\":{\"isEmpty\":true}}");

                
                document.getElementById('Wrapper').classList.add('clearfix');

                JazelAuto5Products.startSrpApp(options, domNode, state);

                // NOTE: A5Srp returns a promise, but we want to attach the event handlers below before
                // the promise resolves

                // Enhance custom zone events

                domNode.addEventListener("beforeCustomZoneDidMount", function(event) {
                    var detail = event.detail;
                    var data = detail.data;
                    if (data != null) {
                        var vehicle = data.vehicle;
                        if (vehicle != null) {
                            data.vehicle = vehicle.legacyFields;
                        }
                    }

                    detail.$ = $;
                    detail.appendHtmlToElement = function(html) {
                        $(detail.element).append($(html));
                    };
                });

                domNode.addEventListener("beforeVehicleWasDisplayed", function(event) {
                    var detail = event.detail;
                    var vehicle = detail.vehicle;
                    if (vehicle != null) {
                        detail.vehicle = vehicle.legacyFields;
                    }
                });

                domNode.addEventListener("beforeCta", function(event) {
                    var detail = event.detail;
                    var vehicle = detail.vehicle;
                    if (vehicle != null) {
                        var vehicleThumbnailUrl = vehicle.vehicleThumbnailUrl;
                        var vehicleDetailsUrl = vehicle.vehicleDetailsUrl;
                        detail.vehicle = Object.assign({}, vehicle.legacyFields, {vehicleThumbnailUrl: vehicleThumbnailUrl, vehicleDetailsUrl: vehicleDetailsUrl});
                    }
                });

                domNode.addEventListener("beforeCustomZoneWillUnmount", function (e) {
                    var detail = e.detail;
                    detail.$ = $;
                });

                // GTM
                domNode.addEventListener("vehicleWasDisplayed", function(e) {

                    var domNode = e.target;
                    var mode = e.detail.mode;
                    var vehicle = e.detail.vehicle;
                    var vdpUrl = e.detail.vdpUrl;
                    var title = e.detail.title;
                    
                    if (mode == "vdp" && !vehicle.vehicleNotFound) {
                        var dataLayerObject = {
                            'event': 'VDPview',
                            'virtualPageURL': vdpUrl,
                            'virtualPageTitle': title,
                            'vin': vehicle.vin,
                            'stock': vehicle.stock_number,
                            'year': vehicle.year,
                            'make': vehicle.make,
                            'model': vehicle.model,
                            'trim': vehicle.trim,
                            'condition': vehicle.condition,
                            'location': vehicle.account_name
                        };

                        window["dataLayer"] = window["dataLayer"] || [];
                        window["dataLayer"].push(dataLayerObject);
                    }

                });

            })(jQuery);
        </script>
        <!-- script | custom js -->
<script id="mfn-dnmc-custom-js">
//<![CDATA[
/**
 * Print a portion of the page
*/
function printPortion(domRef) {

    jQuery('body').addClass('coupon').prepend('<div class="for-print">' + domRef.clone().html() + '</div>');

    window.print();

    jQuery('body').removeClass('coupon');
    jQuery('body').children('.for-print').remove();
}



/**
 * Adds click event to elements used for printing
*/
jQuery(function($) {

jQuery(document).on('click','#triggerGGChat', function() {
   var ggChat = jQuery('body .gg-chat-bubble');
   ggChat.length > 0 ? ggChat.click() : window.location.href = '/contact-us/';
});

jQuery(document).on('click','#google_translate_element_mobile_2', function() {
   var gTrans = jQuery('body .goog-te-menu-frame:first').contents().find('.goog-te-menu2-item span.text')
   gTrans.length > 0 ? gTrans.click() : window.location.href = '#';
});
    
    jQuery(document).on('click','.print-coupon', function() {
        
        printPortion(jQuery(this).parents('.coupon-container').find('.coupon'));
   });


/* Jump to page targets now calculates sticky header height */
    jQuery('a[href^="#"]').on('click', function(e) {
       if(jQuery(this).attr('href').length > 1) {
           e.preventDefault();
           var headerHeight = jQuery('#Top_bar > .container').height();
           var tar = jQuery(this).attr('href');
           var tarTop = jQuery(tar).offset().top;

           jQuery('html, body').animate({
               scrollTop: tarTop - headerHeight - 15
           }, 200);
       }
   });

});
//]]>
</script>

<script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","licenseKey":"29a037a487","applicationID":"101188607","transactionName":"bgZSYhAAWkYHBxVYW1dMcVUWCFtbSRcIX1NVBh1cGA1VABY7EkNE","queueTime":0,"applicationTime":649,"atts":"QkFRFFgaSUg=","errorBeacon":"bam.nr-data.net","agent":""}</script></body>
</html>