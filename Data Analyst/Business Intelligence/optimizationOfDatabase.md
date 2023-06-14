<title>SQL Query Optimization: 12 Useful Performance Tuning Tips and Techniques</title><link rel="preload" as="style" href="https://fonts.googleapis.com/css?family=Open%20Sans%3A400%2C600%2C700%2C300%7CRoboto%3A400%2C500%2C700%2C300%7COpen%20Sans%3A400%2C700&#038;display=swap" /><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open%20Sans%3A400%2C600%2C700%2C300%7CRoboto%3A400%2C500%2C700%2C300%7COpen%20Sans%3A400%2C700&#038;display=swap" media="print" onload="this.media='all'" /><noscript><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open%20Sans%3A400%2C600%2C700%2C300%7CRoboto%3A400%2C500%2C700%2C300%7COpen%20Sans%3A400%2C700&#038;display=swap" /></noscript>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="pingback" href="https://blog.devart.com/xmlrpc.php" />
    <meta name='robots' content='index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1' />
<link rel="icon" type="image/png" href="https://blog.devart.com/wp-content/uploads/2022/12/favicon.ico">
	<!-- This site is optimized with the Yoast SEO plugin v20.7 - https://yoast.com/wordpress/plugins/seo/ -->
	<meta name="description" content="Read the tutorial to learn more about SQL Server performance tuning best practices that help greater improve SQL Server query optimization." />
	<link rel="canonical" href="https://blog.devart.com/how-to-optimize-sql-query.html" />
	<meta property="og:locale" content="en_US" />
	<meta property="og:type" content="article" />
	<meta property="og:title" content="SQL Query Optimization: 12 Useful Performance Tuning Tips and Techniques" />
	<meta property="og:description" content="Read the tutorial to learn more about SQL Server performance tuning best practices that help greater improve SQL Server query optimization." />
	<meta property="og:url" content="https://blog.devart.com/how-to-optimize-sql-query.html" />
	<meta property="og:site_name" content="Devart Blog" />
	<meta property="article:published_time" content="2021-12-23T10:35:09+00:00" />
	<meta property="article:modified_time" content="2023-06-12T09:13:58+00:00" />
	<meta property="og:image" content="https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg" />
	<meta property="og:image:width" content="1068" />
	<meta property="og:image:height" content="580" />
	<meta property="og:image:type" content="image/jpeg" />
	<meta name="author" content="dbForge Team" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:label1" content="Written by" />
	<meta name="twitter:data1" content="dbForge Team" />
	<meta name="twitter:label2" content="Est. reading time" />
	<meta name="twitter:data2" content="16 minutes" />
	<script type="application/ld+json" class="yoast-schema-graph">{"@context":"https://schema.org","@graph":[{"@type":"WebPage","@id":"https://blog.devart.com/how-to-optimize-sql-query.html","url":"https://blog.devart.com/how-to-optimize-sql-query.html","name":"SQL Query Optimization: 12 Useful Performance Tuning Tips and Techniques","isPartOf":{"@id":"https://blog.devart.com/#website"},"primaryImageOfPage":{"@id":"https://blog.devart.com/how-to-optimize-sql-query.html#primaryimage"},"image":{"@id":"https://blog.devart.com/how-to-optimize-sql-query.html#primaryimage"},"thumbnailUrl":"https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg","datePublished":"2021-12-23T10:35:09+00:00","dateModified":"2023-06-12T09:13:58+00:00","author":{"@id":"https://blog.devart.com/#/schema/person/64326ea21c7cb7d4cadf22a6daa9554e"},"description":"Read the tutorial to learn more about SQL Server performance tuning best practices that help greater improve SQL Server query optimization.","breadcrumb":{"@id":"https://blog.devart.com/how-to-optimize-sql-query.html#breadcrumb"},"inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https://blog.devart.com/how-to-optimize-sql-query.html"]}]},{"@type":"ImageObject","inLanguage":"en-US","@id":"https://blog.devart.com/how-to-optimize-sql-query.html#primaryimage","url":"https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg","contentUrl":"https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg","width":1068,"height":580},{"@type":"BreadcrumbList","@id":"https://blog.devart.com/how-to-optimize-sql-query.html#breadcrumb","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://blog.devart.com/"},{"@type":"ListItem","position":2,"name":"SQL Query Optimization: How to Tune Performance of SQL Queries"}]},{"@type":"WebSite","@id":"https://blog.devart.com/#website","url":"https://blog.devart.com/","name":"Devart Blog","description":"Devart company blog","potentialAction":[{"@type":"SearchAction","target":{"@type":"EntryPoint","urlTemplate":"https://blog.devart.com/?s={search_term_string}"},"query-input":"required name=search_term_string"}],"inLanguage":"en-US"},{"@type":"Person","@id":"https://blog.devart.com/#/schema/person/64326ea21c7cb7d4cadf22a6daa9554e","name":"dbForge Team","image":{"@type":"ImageObject","inLanguage":"en-US","@id":"https://blog.devart.com/#/schema/person/image/","url":"https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png","contentUrl":"https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png","caption":"dbForge Team"},"url":"https://blog.devart.com/author/dbforge"}]}</script>
	<!-- / Yoast SEO plugin. -->


<link rel='dns-prefetch' href='//fonts.googleapis.com' />
<link href='https://fonts.gstatic.com' crossorigin rel='preconnect' />
<link rel="alternate" type="application/rss+xml" title="Devart Blog &raquo; Feed" href="https://blog.devart.com/feed" />
<link rel="alternate" type="application/rss+xml" title="Devart Blog &raquo; Comments Feed" href="https://blog.devart.com/comments/feed" />
<style type="text/css">
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 0.07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
	<link rel='stylesheet' id='wp-block-library-css' href='https://blog.devart.com/wp-includes/css/dist/block-library/style.min.css?ver=6.2' type='text/css' media='all' />
<link rel='stylesheet' id='classic-theme-styles-css' href='https://blog.devart.com/wp-includes/css/classic-themes.min.css?ver=6.2' type='text/css' media='all' />
<style id='global-styles-inline-css' type='text/css'>
body{--wp--preset--color--black: #000000;--wp--preset--color--cyan-bluish-gray: #abb8c3;--wp--preset--color--white: #ffffff;--wp--preset--color--pale-pink: #f78da7;--wp--preset--color--vivid-red: #cf2e2e;--wp--preset--color--luminous-vivid-orange: #ff6900;--wp--preset--color--luminous-vivid-amber: #fcb900;--wp--preset--color--light-green-cyan: #7bdcb5;--wp--preset--color--vivid-green-cyan: #00d084;--wp--preset--color--pale-cyan-blue: #8ed1fc;--wp--preset--color--vivid-cyan-blue: #0693e3;--wp--preset--color--vivid-purple: #9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg,rgba(6,147,227,1) 0%,rgb(155,81,224) 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg,rgb(122,220,180) 0%,rgb(0,208,130) 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg,rgba(252,185,0,1) 0%,rgba(255,105,0,1) 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg,rgba(255,105,0,1) 0%,rgb(207,46,46) 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg,rgb(238,238,238) 0%,rgb(169,184,195) 100%);--wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg,rgb(74,234,220) 0%,rgb(151,120,209) 20%,rgb(207,42,186) 40%,rgb(238,44,130) 60%,rgb(251,105,98) 80%,rgb(254,248,76) 100%);--wp--preset--gradient--blush-light-purple: linear-gradient(135deg,rgb(255,206,236) 0%,rgb(152,150,240) 100%);--wp--preset--gradient--blush-bordeaux: linear-gradient(135deg,rgb(254,205,165) 0%,rgb(254,45,45) 50%,rgb(107,0,62) 100%);--wp--preset--gradient--luminous-dusk: linear-gradient(135deg,rgb(255,203,112) 0%,rgb(199,81,192) 50%,rgb(65,88,208) 100%);--wp--preset--gradient--pale-ocean: linear-gradient(135deg,rgb(255,245,203) 0%,rgb(182,227,212) 50%,rgb(51,167,181) 100%);--wp--preset--gradient--electric-grass: linear-gradient(135deg,rgb(202,248,128) 0%,rgb(113,206,126) 100%);--wp--preset--gradient--midnight: linear-gradient(135deg,rgb(2,3,129) 0%,rgb(40,116,252) 100%);--wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');--wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');--wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');--wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');--wp--preset--duotone--midnight: url('#wp-duotone-midnight');--wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');--wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');--wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');--wp--preset--font-size--small: 11px;--wp--preset--font-size--medium: 20px;--wp--preset--font-size--large: 32px;--wp--preset--font-size--x-large: 42px;--wp--preset--font-size--regular: 15px;--wp--preset--font-size--larger: 50px;--wp--preset--spacing--20: 0.44rem;--wp--preset--spacing--30: 0.67rem;--wp--preset--spacing--40: 1rem;--wp--preset--spacing--50: 1.5rem;--wp--preset--spacing--60: 2.25rem;--wp--preset--spacing--70: 3.38rem;--wp--preset--spacing--80: 5.06rem;--wp--preset--shadow--natural: 6px 6px 9px rgba(0, 0, 0, 0.2);--wp--preset--shadow--deep: 12px 12px 50px rgba(0, 0, 0, 0.4);--wp--preset--shadow--sharp: 6px 6px 0px rgba(0, 0, 0, 0.2);--wp--preset--shadow--outlined: 6px 6px 0px -3px rgba(255, 255, 255, 1), 6px 6px rgba(0, 0, 0, 1);--wp--preset--shadow--crisp: 6px 6px 0px rgba(0, 0, 0, 1);}:where(.is-layout-flex){gap: 0.5em;}body .is-layout-flow > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-flow > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-flow > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-constrained > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-constrained > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > :where(:not(.alignleft):not(.alignright):not(.alignfull)){max-width: var(--wp--style--global--content-size);margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignwide{max-width: var(--wp--style--global--wide-size);}body .is-layout-flex{display: flex;}body .is-layout-flex{flex-wrap: wrap;align-items: center;}body .is-layout-flex > *{margin: 0;}:where(.wp-block-columns.is-layout-flex){gap: 2em;}.has-black-color{color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-color{color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-color{color: var(--wp--preset--color--white) !important;}.has-pale-pink-color{color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-color{color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-color{color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-color{color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-color{color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-color{color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-color{color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-color{color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-color{color: var(--wp--preset--color--vivid-purple) !important;}.has-black-background-color{background-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-background-color{background-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-background-color{background-color: var(--wp--preset--color--white) !important;}.has-pale-pink-background-color{background-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-background-color{background-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-background-color{background-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-background-color{background-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-background-color{background-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-background-color{background-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-background-color{background-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-background-color{background-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-background-color{background-color: var(--wp--preset--color--vivid-purple) !important;}.has-black-border-color{border-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-border-color{border-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-border-color{border-color: var(--wp--preset--color--white) !important;}.has-pale-pink-border-color{border-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-border-color{border-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-border-color{border-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-border-color{border-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-border-color{border-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-border-color{border-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-border-color{border-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-border-color{border-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-border-color{border-color: var(--wp--preset--color--vivid-purple) !important;}.has-vivid-cyan-blue-to-vivid-purple-gradient-background{background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;}.has-light-green-cyan-to-vivid-green-cyan-gradient-background{background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;}.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;}.has-luminous-vivid-orange-to-vivid-red-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;}.has-very-light-gray-to-cyan-bluish-gray-gradient-background{background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;}.has-cool-to-warm-spectrum-gradient-background{background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;}.has-blush-light-purple-gradient-background{background: var(--wp--preset--gradient--blush-light-purple) !important;}.has-blush-bordeaux-gradient-background{background: var(--wp--preset--gradient--blush-bordeaux) !important;}.has-luminous-dusk-gradient-background{background: var(--wp--preset--gradient--luminous-dusk) !important;}.has-pale-ocean-gradient-background{background: var(--wp--preset--gradient--pale-ocean) !important;}.has-electric-grass-gradient-background{background: var(--wp--preset--gradient--electric-grass) !important;}.has-midnight-gradient-background{background: var(--wp--preset--gradient--midnight) !important;}.has-small-font-size{font-size: var(--wp--preset--font-size--small) !important;}.has-medium-font-size{font-size: var(--wp--preset--font-size--medium) !important;}.has-large-font-size{font-size: var(--wp--preset--font-size--large) !important;}.has-x-large-font-size{font-size: var(--wp--preset--font-size--x-large) !important;}
.wp-block-navigation a:where(:not(.wp-element-button)){color: inherit;}
:where(.wp-block-columns.is-layout-flex){gap: 2em;}
.wp-block-pullquote{font-size: 1.5em;line-height: 1.6;}
</style>
<link rel='stylesheet' id='td-plugin-multi-purpose-css' href='https://blog.devart.com/wp-content/plugins/td-composer/td-multi-purpose/style.css?ver=3dc090e4a6dd4d9e8f4a61e980b31fd9' type='text/css' media='all' />

<link rel='stylesheet' id='font_awesome-css' href='https://blog.devart.com/wp-content/plugins/td-composer/assets/fonts/font-awesome/font-awesome.css?ver=3dc090e4a6dd4d9e8f4a61e980b31fd9' type='text/css' media='all' />
<link rel='stylesheet' id='td-theme-css' href='https://blog.devart.com/wp-content/themes/Newspaper/style.css?ver=12.3.1' type='text/css' media='all' />
<style id='td-theme-inline-css' type='text/css'>
    
        @media (max-width: 767px) {
            .td-header-desktop-wrap {
                display: none;
            }
        }
        @media (min-width: 767px) {
            .td-header-mobile-wrap {
                display: none;
            }
        }
    
	
</style>
<link rel='stylesheet' id='td-legacy-framework-front-style-css' href='https://blog.devart.com/wp-content/plugins/td-composer/legacy/Newspaper/assets/css/td_legacy_main.css?ver=3dc090e4a6dd4d9e8f4a61e980b31fd9' type='text/css' media='all' />
<link rel='stylesheet' id='tdb_style_cloud_templates_front-css' href='https://blog.devart.com/wp-content/plugins/td-cloud-library/assets/css/tdb_main.css?ver=1182d95cb199c23e56f61364ae38f2e7' type='text/css' media='all' />
<style id='rocket-lazyload-inline-css' type='text/css'>
.rll-youtube-player{position:relative;padding-bottom:56.23%;height:0;overflow:hidden;max-width:100%;}.rll-youtube-player:focus-within{outline: 2px solid currentColor;outline-offset: 5px;}.rll-youtube-player iframe{position:absolute;top:0;left:0;width:100%;height:100%;z-index:100;background:0 0}.rll-youtube-player img{bottom:0;display:block;left:0;margin:auto;max-width:100%;width:100%;position:absolute;right:0;top:0;border:none;height:auto;-webkit-transition:.4s all;-moz-transition:.4s all;transition:.4s all}.rll-youtube-player img:hover{-webkit-filter:brightness(75%)}.rll-youtube-player .play{height:100%;width:100%;left:0;top:0;position:absolute;background:url(https://blog.devart.com/wp-content/plugins/wp-rocket/assets/img/youtube.png) no-repeat center;background-color: transparent !important;cursor:pointer;border:none;}
</style>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' data-rocket-src='https://blog.devart.com/wp-includes/js/jquery/jquery.min.js?ver=3.6.3' id='jquery-core-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' data-rocket-src='https://blog.devart.com/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.4.0' id='jquery-migrate-js' defer></script>
<link rel="https://api.w.org/" href="https://blog.devart.com/wp-json/" /><link rel="alternate" type="application/json" href="https://blog.devart.com/wp-json/wp/v2/posts/30364" /><link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://blog.devart.com/xmlrpc.php?rsd" />
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://blog.devart.com/wp-includes/wlwmanifest.xml" />
<meta name="generator" content="WordPress 6.2" />
<link rel='shortlink' href='https://blog.devart.com/?p=30364' />
<link rel="alternate" type="application/json+oembed" href="https://blog.devart.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fblog.devart.com%2Fhow-to-optimize-sql-query.html" />
<link rel="alternate" type="text/xml+oembed" href="https://blog.devart.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fblog.devart.com%2Fhow-to-optimize-sql-query.html&#038;format=xml" />
<!--[if lt IE 9]><script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.js"></script><![endif]-->
        <script type="rocketlazyloadscript">
        window.tdb_global_vars = {"wpRestUrl":"https:\/\/blog.devart.com\/wp-json\/","permalinkStructure":"\/%postname%.html"};
        window.tdb_p_autoload_vars = {"isAjax":false,"isAdminBarShowing":false,"autoloadScrollPercent":20,"postAutoloadStatus":"off","origPostEditUrl":null};
    </script>
    
    <style id="tdb-global-colors">
        :root {--reel-news-white: #FFFFFF;--reel-news-black: #000000;--reel-news-accent: #0071ce;--reel-news-light-grey: #919191;--reel-news-black-transparent: rgba(0,0,0,0.85);--reel-news-red: #ff0000;--reel-news-dark-gray: #313131;--reel-news-transparent: rgba(255, 255, 255, 0.55);}
    </style>
	
<link rel="preload" as="style" href="https://blog.devart.com/wp-content/plugins/code-prettify/prettify/prettify.css" />
<!-- JS generated by theme -->

<script type="rocketlazyloadscript">
    
    

	    var tdBlocksArray = []; //here we store all the items for the current page

	    //td_block class - each ajax block uses a object of this class for requests
	    function tdBlock() {
		    this.id = '';
		    this.block_type = 1; //block type id (1-234 etc)
		    this.atts = '';
		    this.td_column_number = '';
		    this.td_current_page = 1; //
		    this.post_count = 0; //from wp
		    this.found_posts = 0; //from wp
		    this.max_num_pages = 0; //from wp
		    this.td_filter_value = ''; //current live filter value
		    this.is_ajax_running = false;
		    this.td_user_action = ''; // load more or infinite loader (used by the animation)
		    this.header_color = '';
		    this.ajax_pagination_infinite_stop = ''; //show load more at page x
	    }


        // td_js_generator - mini detector
        (function(){
            var htmlTag = document.getElementsByTagName("html")[0];

	        if ( navigator.userAgent.indexOf("MSIE 10.0") > -1 ) {
                htmlTag.className += ' ie10';
            }

            if ( !!navigator.userAgent.match(/Trident.*rv\:11\./) ) {
                htmlTag.className += ' ie11';
            }

	        if ( navigator.userAgent.indexOf("Edge") > -1 ) {
                htmlTag.className += ' ieEdge';
            }

            if ( /(iPad|iPhone|iPod)/g.test(navigator.userAgent) ) {
                htmlTag.className += ' td-md-is-ios';
            }

            var user_agent = navigator.userAgent.toLowerCase();
            if ( user_agent.indexOf("android") > -1 ) {
                htmlTag.className += ' td-md-is-android';
            }

            if ( -1 !== navigator.userAgent.indexOf('Mac OS X')  ) {
                htmlTag.className += ' td-md-is-os-x';
            }

            if ( /chrom(e|ium)/.test(navigator.userAgent.toLowerCase()) ) {
               htmlTag.className += ' td-md-is-chrome';
            }

            if ( -1 !== navigator.userAgent.indexOf('Firefox') ) {
                htmlTag.className += ' td-md-is-firefox';
            }

            if ( -1 !== navigator.userAgent.indexOf('Safari') && -1 === navigator.userAgent.indexOf('Chrome') ) {
                htmlTag.className += ' td-md-is-safari';
            }

            if( -1 !== navigator.userAgent.indexOf('IEMobile') ){
                htmlTag.className += ' td-md-is-iemobile';
            }

        })();




        var tdLocalCache = {};

        ( function () {
            "use strict";

            tdLocalCache = {
                data: {},
                remove: function (resource_id) {
                    delete tdLocalCache.data[resource_id];
                },
                exist: function (resource_id) {
                    return tdLocalCache.data.hasOwnProperty(resource_id) && tdLocalCache.data[resource_id] !== null;
                },
                get: function (resource_id) {
                    return tdLocalCache.data[resource_id];
                },
                set: function (resource_id, cachedData) {
                    tdLocalCache.remove(resource_id);
                    tdLocalCache.data[resource_id] = cachedData;
                }
            };
        })();

    
    
var td_viewport_interval_list=[{"limitBottom":767,"sidebarWidth":228},{"limitBottom":1018,"sidebarWidth":300},{"limitBottom":1140,"sidebarWidth":324}];
var td_animation_stack_effect="type0";
var tds_animation_stack=true;
var td_animation_stack_specific_selectors=".entry-thumb, img, .td-lazy-img";
var td_animation_stack_general_selectors=".td-animation-stack img, .td-animation-stack .entry-thumb, .post img, .td-animation-stack .td-lazy-img";
var tdc_is_installed="yes";
var td_ajax_url="https:\/\/blog.devart.com\/wp-admin\/admin-ajax.php?td_theme_name=Newspaper&v=12.3.1";
var td_get_template_directory_uri="https:\/\/blog.devart.com\/wp-content\/plugins\/td-composer\/legacy\/common";
var tds_snap_menu="";
var tds_logo_on_sticky="";
var tds_header_style="";
var td_please_wait="Please wait...";
var td_email_user_pass_incorrect="User or password incorrect!";
var td_email_user_incorrect="Email or username incorrect!";
var td_email_incorrect="Email incorrect!";
var td_user_incorrect="Username incorrect!";
var td_email_user_empty="Email or username empty!";
var td_pass_empty="Pass empty!";
var td_pass_pattern_incorrect="Invalid Pass Pattern!";
var td_retype_pass_incorrect="Retyped Pass incorrect!";
var tds_more_articles_on_post_enable="";
var tds_more_articles_on_post_time_to_wait="";
var tds_more_articles_on_post_pages_distance_from_top=0;
var tds_theme_color_site_wide="#0071ce";
var tds_smart_sidebar="";
var tdThemeName="Newspaper";
var tdThemeNameWl="Newspaper";
var td_magnific_popup_translation_tPrev="Previous (Left arrow key)";
var td_magnific_popup_translation_tNext="Next (Right arrow key)";
var td_magnific_popup_translation_tCounter="%curr% of %total%";
var td_magnific_popup_translation_ajax_tError="The content from %url% could not be loaded.";
var td_magnific_popup_translation_image_tError="The image #%curr% could not be loaded.";
var tdBlockNonce="f813030704";
var tdDateNamesI18n={"month_names":["January","February","March","April","May","June","July","August","September","October","November","December"],"month_names_short":["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"],"day_names":["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"],"day_names_short":["Sun","Mon","Tue","Wed","Thu","Fri","Sat"]};
var tdb_modal_confirm="Save";
var tdb_modal_cancel="Cancel";
var tdb_modal_confirm_alt="Yes";
var tdb_modal_cancel_alt="No";
var td_ad_background_click_link="";
var td_ad_background_click_target="";
</script>


<!-- Header style compiled by theme -->

<style>
    

                                    @font-face {
                                      font-family: "Firasans Light";
                                      src: local("Firasans Light"), url("https://blog.devart.com/wp-content/uploads/2022/12/firasans-light-webfont.woff") format("woff");
                                      font-display: swap;
                                    }
                                
                                    @font-face {
                                      font-family: "Firasans Medium";
                                      src: local("Firasans Medium"), url("https://blog.devart.com/wp-content/uploads/2022/12/firasans-medium-webfont.woff") format("woff");
                                      font-display: swap;
                                    }
                                
                                    @font-face {
                                      font-family: "Firasans Regular";
                                      src: local("Firasans Regular"), url("https://blog.devart.com/wp-content/uploads/2022/12/firasans-regular-webfont-1.woff") format("woff");
                                      font-display: swap;
                                    }
                                
.td-header-wrap .black-menu .sf-menu > .current-menu-item > a,
    .td-header-wrap .black-menu .sf-menu > .current-menu-ancestor > a,
    .td-header-wrap .black-menu .sf-menu > .current-category-ancestor > a,
    .td-header-wrap .black-menu .sf-menu > li > a:hover,
    .td-header-wrap .black-menu .sf-menu > .sfHover > a,
    .sf-menu > .current-menu-item > a:after,
    .sf-menu > .current-menu-ancestor > a:after,
    .sf-menu > .current-category-ancestor > a:after,
    .sf-menu > li:hover > a:after,
    .sf-menu > .sfHover > a:after,
    .header-search-wrap .td-drop-down-search:after,
    .header-search-wrap .td-drop-down-search .btn:hover,
    input[type=submit]:hover,
    .td-read-more a,
    .td-post-category:hover,
    body .td_top_authors .td-active .td-author-post-count,
    body .td_top_authors .td-active .td-author-comments-count,
    body .td_top_authors .td_mod_wrap:hover .td-author-post-count,
    body .td_top_authors .td_mod_wrap:hover .td-author-comments-count,
    .td-404-sub-sub-title a:hover,
    .td-search-form-widget .wpb_button:hover,
    .td-rating-bar-wrap div,
    .dropcap,
    .td_wrapper_video_playlist .td_video_controls_playlist_wrapper,
    .wpb_default,
    .wpb_default:hover,
    .td-left-smart-list:hover,
    .td-right-smart-list:hover,
    #bbpress-forums button:hover,
    .bbp_widget_login .button:hover,
    .td-footer-wrapper .td-post-category,
    .td-footer-wrapper .widget_product_search input[type="submit"]:hover,
    .single-product .product .summary .cart .button:hover,
    .td-next-prev-wrap a:hover,
    .td-load-more-wrap a:hover,
    .td-post-small-box a:hover,
    .page-nav .current,
    .page-nav:first-child > div,
    #bbpress-forums .bbp-pagination .current,
    #bbpress-forums #bbp-single-user-details #bbp-user-navigation li.current a,
    .td-theme-slider:hover .slide-meta-cat a,
    a.vc_btn-black:hover,
    .td-trending-now-wrapper:hover .td-trending-now-title,
    .td-scroll-up,
    .td-smart-list-button:hover,
    .td-weather-information:before,
    .td-weather-week:before,
    .td_block_exchange .td-exchange-header:before,
    .td-pulldown-syle-2 .td-subcat-dropdown ul:after,
    .td_block_template_9 .td-block-title:after,
    .td_block_template_15 .td-block-title:before,
    div.wpforms-container .wpforms-form div.wpforms-submit-container button[type=submit],
    .td-close-video-fixed {
        background-color: #0071ce;
    }

    .td_block_template_4 .td-related-title .td-cur-simple-item:before {
        border-color: #0071ce transparent transparent transparent !important;
    }
    
    
    .td_block_template_4 .td-related-title .td-cur-simple-item,
    .td_block_template_3 .td-related-title .td-cur-simple-item,
    .td_block_template_9 .td-related-title:after {
        background-color: #0071ce;
    }

    a,
    cite a:hover,
    .td-page-content blockquote p,
    .td-post-content blockquote p,
    .mce-content-body blockquote p,
    .comment-content blockquote p,
    .wpb_text_column blockquote p,
    .td_block_text_with_title blockquote p,
    .td_module_wrap:hover .entry-title a,
    .td-subcat-filter .td-subcat-list a:hover,
    .td-subcat-filter .td-subcat-dropdown a:hover,
    .td_quote_on_blocks,
    .dropcap2,
    .dropcap3,
    body .td_top_authors .td-active .td-authors-name a,
    body .td_top_authors .td_mod_wrap:hover .td-authors-name a,
    .td-post-next-prev-content a:hover,
    .author-box-wrap .td-author-social a:hover,
    .td-author-name a:hover,
    .td-author-url a:hover,
    .comment-reply-link:hover,
    .logged-in-as a:hover,
    #cancel-comment-reply-link:hover,
    .td-search-query,
    .widget a:hover,
    .td_wp_recentcomments a:hover,
    .archive .widget_archive .current,
    .archive .widget_archive .current a,
    .widget_calendar tfoot a:hover,
    #bbpress-forums li.bbp-header .bbp-reply-content span a:hover,
    #bbpress-forums .bbp-forum-freshness a:hover,
    #bbpress-forums .bbp-topic-freshness a:hover,
    #bbpress-forums .bbp-forums-list li a:hover,
    #bbpress-forums .bbp-forum-title:hover,
    #bbpress-forums .bbp-topic-permalink:hover,
    #bbpress-forums .bbp-topic-started-by a:hover,
    #bbpress-forums .bbp-topic-started-in a:hover,
    #bbpress-forums .bbp-body .super-sticky li.bbp-topic-title .bbp-topic-permalink,
    #bbpress-forums .bbp-body .sticky li.bbp-topic-title .bbp-topic-permalink,
    .widget_display_replies .bbp-author-name,
    .widget_display_topics .bbp-author-name,
    .td-subfooter-menu li a:hover,
    a.vc_btn-black:hover,
    .td-smart-list-dropdown-wrap .td-smart-list-button:hover,
    .td-instagram-user a,
    .td-block-title-wrap .td-wrapper-pulldown-filter .td-pulldown-filter-display-option:hover,
    .td-block-title-wrap .td-wrapper-pulldown-filter .td-pulldown-filter-display-option:hover i,
    .td-block-title-wrap .td-wrapper-pulldown-filter .td-pulldown-filter-link:hover,
    .td-block-title-wrap .td-wrapper-pulldown-filter .td-pulldown-filter-item .td-cur-simple-item,
    .td-pulldown-syle-2 .td-subcat-dropdown:hover .td-subcat-more span,
    .td-pulldown-syle-2 .td-subcat-dropdown:hover .td-subcat-more i,
    .td-pulldown-syle-3 .td-subcat-dropdown:hover .td-subcat-more span,
    .td-pulldown-syle-3 .td-subcat-dropdown:hover .td-subcat-more i,
    .td_block_template_2 .td-related-title .td-cur-simple-item,
    .td_block_template_5 .td-related-title .td-cur-simple-item,
    .td_block_template_6 .td-related-title .td-cur-simple-item,
    .td_block_template_7 .td-related-title .td-cur-simple-item,
    .td_block_template_8 .td-related-title .td-cur-simple-item,
    .td_block_template_9 .td-related-title .td-cur-simple-item,
    .td_block_template_10 .td-related-title .td-cur-simple-item,
    .td_block_template_11 .td-related-title .td-cur-simple-item,
    .td_block_template_12 .td-related-title .td-cur-simple-item,
    .td_block_template_13 .td-related-title .td-cur-simple-item,
    .td_block_template_14 .td-related-title .td-cur-simple-item,
    .td_block_template_15 .td-related-title .td-cur-simple-item,
    .td_block_template_16 .td-related-title .td-cur-simple-item,
    .td_block_template_17 .td-related-title .td-cur-simple-item,
    .td-theme-wrap .sf-menu ul .td-menu-item > a:hover,
    .td-theme-wrap .sf-menu ul .sfHover > a,
    .td-theme-wrap .sf-menu ul .current-menu-ancestor > a,
    .td-theme-wrap .sf-menu ul .current-category-ancestor > a,
    .td-theme-wrap .sf-menu ul .current-menu-item > a,
    .td_outlined_btn,
    body .td_block_categories_tags .td-ct-item:hover,
    body .td_block_list_menu li.current-menu-item > a,
    body .td_block_list_menu li.current-menu-ancestor > a,
    body .td_block_list_menu li.current-category-ancestor > a {
        color: #0071ce;
    }

    a.vc_btn-black.vc_btn_square_outlined:hover,
    a.vc_btn-black.vc_btn_outlined:hover {
        color: #0071ce !important;
    }

    .td-next-prev-wrap a:hover,
    .td-load-more-wrap a:hover,
    .td-post-small-box a:hover,
    .page-nav .current,
    .page-nav:first-child > div,
    #bbpress-forums .bbp-pagination .current,
    .post .td_quote_box,
    .page .td_quote_box,
    a.vc_btn-black:hover,
    .td_block_template_5 .td-block-title > *,
    .td_outlined_btn {
        border-color: #0071ce;
    }

    .td_wrapper_video_playlist .td_video_currently_playing:after {
        border-color: #0071ce !important;
    }

    .header-search-wrap .td-drop-down-search:before {
        border-color: transparent transparent #0071ce transparent;
    }

    .block-title > span,
    .block-title > a,
    .block-title > label,
    .widgettitle,
    .widgettitle:after,
    body .td-trending-now-title,
    .td-trending-now-wrapper:hover .td-trending-now-title,
    .wpb_tabs li.ui-tabs-active a,
    .wpb_tabs li:hover a,
    .vc_tta-container .vc_tta-color-grey.vc_tta-tabs-position-top.vc_tta-style-classic .vc_tta-tabs-container .vc_tta-tab.vc_active > a,
    .vc_tta-container .vc_tta-color-grey.vc_tta-tabs-position-top.vc_tta-style-classic .vc_tta-tabs-container .vc_tta-tab:hover > a,
    .td_block_template_1 .td-related-title .td-cur-simple-item,
    .td-subcat-filter .td-subcat-dropdown:hover .td-subcat-more, 
    .td_3D_btn,
    .td_shadow_btn,
    .td_default_btn,
    .td_round_btn, 
    .td_outlined_btn:hover {
    	background-color: #0071ce;
    }
    .block-title,
    .td_block_template_1 .td-related-title,
    .wpb_tabs .wpb_tabs_nav,
    .vc_tta-container .vc_tta-color-grey.vc_tta-tabs-position-top.vc_tta-style-classic .vc_tta-tabs-container {
        border-color: #0071ce;
    }
    .td_block_wrap .td-subcat-item a.td-cur-simple-item {
	    color: #0071ce;
	}


    
    .td-grid-style-4 .entry-title
    {
        background-color: rgba(0, 113, 206, 0.7);
    }


    
    .td-container-wrap,
    .post,
    .tagdiv-type .td_quote_box {
        background-color: transparent;
    }
    

    
    .td-menu-background:before,
    .td-search-background:before {
        background: #000000;
        background: -moz-linear-gradient(top, #000000 0%, #000000 100%);
        background: -webkit-gradient(left top, left bottom, color-stop(0%, #000000), color-stop(100%, #000000));
        background: -webkit-linear-gradient(top, #000000 0%, #000000 100%);
        background: -o-linear-gradient(top, #000000 0%, #000000 100%);
        background: -ms-linear-gradient(top, #000000 0%, #000000 100%);
        background: linear-gradient(to bottom, #000000 0%, #000000 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#000000', endColorstr='#000000', GradientType=0 );
    }

    
    .td-mobile-content .current-menu-item > a,
    .td-mobile-content .current-menu-ancestor > a,
    .td-mobile-content .current-category-ancestor > a,
    #td-mobile-nav .td-menu-login-section a:hover,
    #td-mobile-nav .td-register-section a:hover,
    #td-mobile-nav .td-menu-socials-wrap a:hover i,
    .td-search-close span:hover i {
        color: #0071ce;
    }

    
    .td-page-header h1,
    .td-page-title {
    	color: #3d3d3d;
    }

    
    .td-page-content p,
    .td-page-content .td_block_text_with_title {
    	color: #656871;
    }

    
    .td-page-content h1,
    .td-page-content h2,
    .td-page-content h3,
    .td-page-content h4,
    .td-page-content h5,
    .td-page-content h6 {
    	color: #3d3d3d;
    }

    .td-page-content .widgettitle {
        color: #fff;
    }

    
    .td_cl .td-container {
        width: 100%;
    }
    @media (min-width: 768px) and (max-width: 1018px) {
        .td_cl {
            padding: 0 14px;
        }
    }
    @media (max-width: 767px) {
        .td_cl .td-container {
            padding: 0;
        }
    }
    @media (min-width: 1019px) and (max-width: 1140px) {
        .td_cl.stretch_row_content_no_space {
            padding-left: 20px;
            padding-right: 20px;
        }
    }
    @media (min-width: 1141px) {
        .td_cl.stretch_row_content_no_space {
            padding-left: 24px;
            padding-right: 24px;
        }
    }
</style>

<!-- Google Tag Manager -->
<script type="rocketlazyloadscript">(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-N4N25R');</script>
<!-- End Google Tag Manager -->
<!-- Button style compiled by theme -->

<style>
    .tdm_block_column_content:hover .tdm-col-content-title-url .tdm-title,
                .tds-button2 .tdm-btn-text,
                .tds-button2 i,
                .tds-button5:hover .tdm-btn-text,
                .tds-button5:hover i,
                .tds-button6 .tdm-btn-text,
                .tds-button6 i,
                .tdm_block_list .tdm-list-item i,
                .tdm_block_pricing .tdm-pricing-feature i,
                body .tdm-social-item i {
                    color: #0071ce;
                }
                .tds-button1,
                .tds-button6:after,
                .tds-title2 .tdm-title-line:after,
                .tds-title3 .tdm-title-line:after,
                .tdm_block_pricing.tdm-pricing-featured:before,
                .tdm_block_pricing.tds_pricing2_block.tdm-pricing-featured .tdm-pricing-header,
                .tds-progress-bar1 .tdm-progress-bar:after,
                .tds-progress-bar2 .tdm-progress-bar:after,
                .tds-social3 .tdm-social-item {
                    background-color: #0071ce;
                }
                .tds-button2:before,
                .tds-button6:before,
                .tds-progress-bar3 .tdm-progress-bar:after {
                  border-color: #0071ce;
                }
                .tdm-btn-style1 {
					background-color: #0071ce;
				}
				.tdm-btn-style2:before {
				    border-color: #0071ce;
				}
				.tdm-btn-style2 {
				    color: #0071ce;
				}
				.tdm-btn-style3 {
				    -webkit-box-shadow: 0 2px 16px #0071ce;
                    -moz-box-shadow: 0 2px 16px #0071ce;
                    box-shadow: 0 2px 16px #0071ce;
				}
				.tdm-btn-style3:hover {
				    -webkit-box-shadow: 0 4px 26px #0071ce;
                    -moz-box-shadow: 0 4px 26px #0071ce;
                    box-shadow: 0 4px 26px #0071ce;
				}
</style>

	<style id="tdw-css-placeholder"></style><noscript><style id="rocket-lazyload-nojs-css">.rll-youtube-player, [data-lazy-src]{display:none !important;}</style></noscript></head>

<body class="post-template-default single single-post postid-30364 single-format-standard how-to-optimize-sql-query global-block-template-10 tdb_template_55874 tdb-template  tdc-header-template  tdc-footer-template td-animation-stack-type0 td-full-layout" itemscope="itemscope" itemtype="https://schema.org/WebPage">
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-N4N25R"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
            <div class="td-scroll-up " style="display:none;"><i class="td-icon-menu-up"></i></div>
    
    <div class="td-menu-background" style="visibility:hidden"></div>
<div id="td-mobile-nav" style="visibility:hidden">
    <div class="td-mobile-container">
        <!-- mobile menu top section -->
        <div class="td-menu-socials-wrap">
            <!-- socials -->
            <div class="td-menu-socials">
                            </div>
            <!-- close button -->
            <div class="td-mobile-close">
                <span><i class="td-icon-close-mobile"></i></span>
            </div>
        </div>

        <!-- login section -->
        
        <!-- menu section -->
        <div class="td-mobile-content">
            <div class="menu-products-container"><ul id="menu-products-2" class="td-mobile-main-menu"><li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-first menu-item-55698"><a href="https://www.devart.com/products.html" target="_blank">Products<i class="td-icon-menu-right td-element-after"></i></a>
<ul class="sub-menu">
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55702"><a href="https://www.devart.com/dbforge/" target="_blank">DATABASE TOOLS<i class="td-icon-menu-right td-element-after"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55706"><a href="https://www.devart.com/dbforge/sql/" target="_blank">SQL Server Tools<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62900"><a href="https://www.devart.com/dbforge/sql/sqlcomplete/" target="_blank">dbForge SQL Complete</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62903"><a href="https://www.devart.com/dbforge/sql/studio/" target="_blank">dbForge Studio for SQL Server</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62906"><a href="https://www.devart.com/dbforge/sql/sql-tools/" target="_blank">dbForge SQL Tools</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62918"><a href="https://www.devart.com/products.html#database-tools&#038;sql-server" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55710"><a href="https://www.devart.com/dbforge/mysql/" target="_blank">MySQL Tools<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62909"><a href="https://www.devart.com/dbforge/mysql/studio/" target="_blank">dbForge Studio for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62912"><a href="https://www.devart.com/dbforge/mysql/compare-bundle/" target="_blank">Compare Bundle for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62915"><a href="https://www.devart.com/dbforge/mysql/schemacompare/" target="_blank">Schema Compare for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62921"><a href="https://www.devart.com/products.html#database-tools&#038;mysql" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55714"><a href="https://www.devart.com/dbforge/oracle/" target="_blank">Oracle Tools<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62924"><a href="https://www.devart.com/dbforge/oracle/studio/" target="_blank">dbForge Studio for Oracle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62927"><a href="https://www.devart.com/dbforge/oracle/compare-bundle/" target="_blank">Compare Bundle for Oracle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62930"><a href="https://www.devart.com/dbforge/oracle/datacompare/" target="_blank">Data Compare for Oracle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62933"><a href="https://www.devart.com/products.html#database-tools&#038;oracle" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55718"><a href="https://www.devart.com/dbforge/postgresql/" target="_blank">PostgreSQL Tools<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62936"><a href="https://www.devart.com/dbforge/postgresql/studio/" target="_blank">dbForge Studio for PostgreSQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62939"><a href="https://www.devart.com/dbforge/postgresql/datacompare/" target="_blank">Data Compare for PostgreSQL</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-65690"><a href="https://www.devart.com/dbforge/edge/" target="_blank">Multidatabase Solution</a></li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55722"><a href="https://www.devart.com/data-connectivity/" target="_blank">DATA CONNECTIVITY<i class="td-icon-menu-right td-element-after"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55726"><a href="https://www.devart.com/dotconnect/" target="_blank">ADO.NET Data Providers<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62966"><a href="https://www.devart.com/dotconnect/oracle/" target="_blank">dotConnect for Oracle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62969"><a href="https://www.devart.com/dotconnect/postgresql/" target="_blank">dotConnect for PostgreSQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62972"><a href="https://www.devart.com/dotconnect/mysql/" target="_blank">dotConnect for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62975"><a href="https://www.devart.com/products.html#data-connectivity&#038;.net" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55730"><a href="https://www.devart.com/odbc/" target="_blank">ODBC Drivers<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62978"><a href="https://www.devart.com/odbc/salesforce/" target="_blank">ODBC Driver for Salesforce</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62981"><a href="https://www.devart.com/odbc/oracle/" target="_blank">ODBC Driver for Oracle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62984"><a href="https://www.devart.com/odbc/mysql/" target="_blank">ODBC Driver for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62987"><a href="https://www.devart.com/products.html#data-connectivity&#038;odbc" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55734"><a href="https://www.devart.com/ssis/" target="_blank">SSIS Components<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63002"><a href="https://www.devart.com/ssis/salesforce/" target="_blank">SSIS Components for Salesforce</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63005"><a href="https://www.devart.com/ssis/mysql/" target="_blank">SSIS Components for MySQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63008"><a href="https://www.devart.com/ssis/database-bundle/" target="_blank">SSIS Integration Database Bundle</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63011"><a href="https://www.devart.com/products.html#data-connectivity&#038;ssis" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55738"><a href="https://www.devart.com/excel-addins/" target="_blank">Excel Add-ins<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63014"><a href="https://www.devart.com/excel-addins/sqlserver/" target="_blank">Excel Add-in for SQL Server</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63017"><a href="https://www.devart.com/excel-addins/postgresql/" target="_blank">Excel Add-in for PostgreSQL</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63020"><a href="https://www.devart.com/excel-addins/database-pack/" target="_blank">Excel Add-in Database Pack</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-63023"><a href="https://www.devart.com/products.html#data-connectivity&#038;excel" target="_blank">Others</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55742"><a href="https://www.devart.com/dac.html" target="_blank">Delphi Data Components<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62990"><a href="https://www.devart.com/unidac/" target="_blank">Universal Data Access Components</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62993"><a href="https://www.devart.com/odac/" target="_blank">Oracle Data Access Components</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62996"><a href="https://www.devart.com/sdac/" target="_blank">SQL Server Data Access Components</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62999"><a href="https://www.devart.com/products.html#data-connectivity&#038;delphi" target="_blank">Others</a></li>
		</ul>
</li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55746"><a>PRODUCTIVITY TOOLS<i class="td-icon-menu-right td-element-after"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55750"><a href="https://www.devart.com/productivity-tools.html" target="_blank">Coding Assistance Tools<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62942"><a href="https://www.devart.com/sbridge/" target="_blank">SecureBridge</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62945"><a href="https://www.devart.com/codecompare/" target="_blank">Code Compare</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62948"><a href="https://www.devart.com/review-assistant/" target="_blank">Review Assistant</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62951"><a href="https://www.devart.com/code-review-bundle/" target="_blank">Code Review Bundle</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55754"><a href="https://www.devart.com/orm-solutions.html" target="_blank">ORM Solutions<i class="td-icon-menu-right td-element-after"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62954"><a href="https://www.devart.com/entitydeveloper/" target="_blank">Entity Developer</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62957"><a href="https://www.devart.com/linqconnect/" target="_blank">LinqConnect</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62960"><a href="https://www.devart.com/entitydac/" target="_blank">EntityDAC</a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-62963"><a href="https://www.devart.com/linqinsight/" target="_blank">LINQ Insight</a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55758"><a href="https://tmetric.com/" target="_blank">Time Tracking App</a></li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55762"><a href="https://skyvia.com/" target="_blank">DATA SERVICES<i class="td-icon-menu-right td-element-after"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55766"><a href="https://skyvia.com/data-integration/" target="_blank">Data Integration Services</a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55770"><a href="https://skyvia.com/backup/" target="_blank">Cloud to Cloud Backup</a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55774"><a href="https://skyvia.com/query/" target="_blank">Online SQL Tools</a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55778"><a href="https://skyvia.com/connect/" target="_blank">Web API Server</a></li>
	</ul>
</li>
</ul>
</li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55782"><a href="https://www.devart.com/products.html" target="_blank">Store</a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55786"><a href="https://www.devart.com/support/" target="_blank">Support</a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-55790"><a>Company<i class="td-icon-menu-right td-element-after"></i></a>
<ul class="sub-menu">
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55794"><a href="https://www.devart.com/company/" target="_blank">About us</a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55798"><a href="https://www.devart.com/company/customers.html" target="_blank">Customers</a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55802"><a href="https://www.devart.com/company/partners.html" target="_blank">Partners</a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55806"><a href="https://www.devart.com/company/resellers.html" target="_blank">Resellers</a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55810"><a href="https://www.devart.com/company/contact.html" target="_blank">Contacts</a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-55814"><a href="https://www.devart.com/vacancies/" target="_blank">Vacancies</a></li>
</ul>
</li>
</ul></div>        </div>
    </div>

    <!-- register/login section -->
    </div>    <div class="td-search-background" style="visibility:hidden"></div>
<div class="td-search-wrap-mob" style="visibility:hidden">
	<div class="td-drop-down-search">
		<form method="get" class="td-search-form" action="https://blog.devart.com/">
			<!-- close button -->
			<div class="td-search-close">
				<span><i class="td-icon-close-mobile"></i></span>
			</div>
			<div role="search" class="td-search-input">
				<span>Search</span>
				<input id="td-header-search-mob" type="text" value="" name="s" autocomplete="off" />
			</div>
		</form>
		<div id="td-aj-search-mob" class="td-ajax-search-flex"></div>
	</div>
</div>
    <div id="td-outer-wrap" class="td-theme-wrap">

                    <div class="td-header-template-wrap" style="position: relative">
                                <div class="td-header-mobile-wrap ">
                    <div id="tdi_1" class="tdc-zone"><div class="tdc_zone tdi_2  wpb_row td-pb-row tdc-element-style"  >
<style scoped>

/* custom css */
.tdi_2{
                    min-height: 0;
                }

/* phone */
@media (max-width: 767px){
.tdi_2:before{
                    content: '';
                    display: block;
                    width: 100vw;
                    height: 100%;
                    position: absolute;
                    left: 50%;
                    transform: translateX(-50%);
                    box-shadow:  0px 6px 8px 0px rgba(0, 0, 0, 0.08);
                    z-index: 20;
                    pointer-events: none;
                }@media (max-width: 767px) {
                    .tdi_2:before {
                        width: 100%;
                    }
                }
}
/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_2{
position:relative;
}
}

</style>
<div class="tdi_1_rand_style td-element-style" ><style>
/* phone */
@media (max-width: 767px)
{
.tdi_1_rand_style{
background-color:#222222 !important;
}
}
 </style></div><div id="tdi_3" class="tdc-row"><div class="vc_row tdi_4  wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_4,
                .tdi_4 .tdc-columns{
                    min-height: 0;
                }.tdi_4,
				.tdi_4 .tdc-columns{
				    display: block;
				}.tdi_4 .tdc-columns{
				    width: 100%;
				}

/* phone */
@media (max-width: 767px){
@media (min-width: 768px) {
	                .tdi_4 {
	                    margin-left: -0px;
	                    margin-right: -0px;
	                }
	                .tdi_4 .tdc-row-video-background-error,
	                .tdi_4 .vc_column {
	                    padding-left: 0px;
	                    padding-right: 0px;
	                }
                }
}
</style><div class="vc_column tdi_6  wpb_column vc_column_container tdc-column td-pb-span4">
<style scoped>

/* custom css */
.tdi_6{
                    vertical-align: baseline;
                }.tdi_6 > .wpb_wrapper,
				.tdi_6 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_6 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_6 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_6 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}

/* phone */
@media (max-width: 767px){
.tdi_6{
                    vertical-align: middle;
                }
}
/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_6{
width:20% !important;
display:inline-block !important;
}
}

</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_mobile_menu tdi_7 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_7" >
<style>

/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_7{
margin-top:2px !important;
margin-left:-13px !important;
border-style:none !important;
border-color:#888888 !important;
}
}

</style>
<style>
/* custom css */
.tdb-header-align{
                  vertical-align: middle;
                }.tdb_mobile_menu{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_mobile_menu a{
                  display: inline-block !important;
                  position: relative;
                  text-align: center;
                  color: #4db2ec;
                }.tdb_mobile_menu a > span{
                  display: flex;
                  align-items: center;
                  justify-content: center;
                }.tdb_mobile_menu svg{
                  height: auto;
                }.tdb_mobile_menu svg,
                .tdb_mobile_menu svg *{
                  fill: #4db2ec;
                }#tdc-live-iframe .tdb_mobile_menu a{
                  pointer-events: none;
                }.td-menu-mob-open-menu{
                  overflow: hidden;
                }.td-menu-mob-open-menu #td-outer-wrap{
                  position: static;
                }.tdi_7 .tdb-mobile-menu-button i{
                    font-size: 22px;
                
                    width: 55px;
					height: 55px;
					line-height:  55px;
                }.tdi_7 .tdb-mobile-menu-button svg{
                    width: 22px;
                }.tdi_7 .tdb-mobile-menu-button .tdb-mobile-menu-icon-svg{
                    width: 55px;
					height: 55px;
                }.tdi_7 .tdb-mobile-menu-button{
                    color: #ffffff;
                }.tdi_7 .tdb-mobile-menu-button svg,
                .tdi_7 .tdb-mobile-menu-button svg *{
                    fill: #ffffff;
                }

/* phone */
@media (max-width: 767px){
.tdi_7 .tdb-mobile-menu-button i{
                    font-size: 27px;
                
                    width: 54px;
					height: 54px;
					line-height:  54px;
                }.tdi_7 .tdb-mobile-menu-button svg{
                    width: 27px;
                }.tdi_7 .tdb-mobile-menu-button .tdb-mobile-menu-icon-svg{
                    width: 54px;
					height: 54px;
                }
}
</style><div class="tdb-block-inner td-fix-index"><span class="tdb-mobile-menu-button"><i class="tdb-mobile-menu-icon td-icon-mobile"></i></span></div></div> <!-- ./block --></div></div><div class="vc_column tdi_9  wpb_column vc_column_container tdc-column td-pb-span4">
<style scoped>

/* custom css */
.tdi_9{
                    vertical-align: baseline;
                }.tdi_9 > .wpb_wrapper,
				.tdi_9 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_9 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_9 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_9 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}

/* phone */
@media (max-width: 767px){
.tdi_9{
                    vertical-align: middle;
                }
}
/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_9{
width:60% !important;
display:inline-block !important;
}
}

</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_header_logo tdi_10 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_10" >
<style>

/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_10{
margin-top:-8px !important;
}
}

</style>
<style>
/* custom css */
.tdb_header_logo{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_header_logo .tdb-logo-a,
                .tdb_header_logo h1{
                  display: flex;
                  pointer-events: auto;
                  align-items: flex-start;
                }.tdb_header_logo h1{
                  margin: 0;
                  line-height: 0;
                }.tdb_header_logo .tdb-logo-img-wrap img{
                  display: block;
                }.tdb_header_logo .tdb-logo-svg-wrap + .tdb-logo-img-wrap{
                  display: none;
                }.tdb_header_logo .tdb-logo-svg-wrap svg{
                  width: 50px;
                  display: block;
                  transition: fill .3s ease;
                }.tdb_header_logo .tdb-logo-text-wrap{
                  display: flex;
                }.tdb_header_logo .tdb-logo-text-title,
                .tdb_header_logo .tdb-logo-text-tagline{
                  -webkit-transition: all 0.2s ease;
                  transition: all 0.2s ease;
                }.tdb_header_logo .tdb-logo-text-title{
                  background-size: cover;
                  background-position: center center;
                  font-size: 75px;
                  font-family: serif;
                  line-height: 1.1;
                  color: #222;
                  white-space: nowrap;
                }.tdb_header_logo .tdb-logo-text-tagline{
                  margin-top: 2px;
                  font-size: 12px;
                  font-family: serif;
                  letter-spacing: 1.8px;
                  line-height: 1;
                  color: #767676;
                }.tdb_header_logo .tdb-logo-icon{
                  position: relative;
                  font-size: 46px;
                  color: #000;
                }.tdb_header_logo .tdb-logo-icon-svg{
                  line-height: 0;
                }.tdb_header_logo .tdb-logo-icon-svg svg{
                  width: 46px;
                  height: auto;
                }.tdb_header_logo .tdb-logo-icon-svg svg,
                .tdb_header_logo .tdb-logo-icon-svg svg *{
                  fill: #000;
                }.tdi_10 .tdb-logo-a,
                .tdi_10 h1{
                    align-items: center;
                
                    justify-content: center;
                }.tdi_10 .tdb-logo-svg-wrap{
                    display: block;
                }.tdi_10 .tdb-logo-img-wrap{
                    display: none;
                }.tdi_10 .tdb-logo-text-tagline{
                    margin-top: -3px;
                    margin-left: 0;
                
                    display: block;
                }.tdi_10 .tdb-logo-text-title{
                    display: block;
                
                    color: #ffffff;
                }.tdi_10 .tdb-logo-text-wrap{
                    flex-direction: column;
                
                    align-items: center;
                }.tdi_10 .tdb-logo-icon{
                    top: 0px;
                
                    display: block;
                }@media (max-width: 767px) {
                  .tdb_header_logo .tdb-logo-text-title {
                    font-size: 36px;
                  }
                }@media (max-width: 767px) {
                  .tdb_header_logo .tdb-logo-text-tagline {
                    font-size: 11px;
                  }
                }

/* portrait */
@media (min-width: 768px) and (max-width: 1018px){
.tdi_10 .tdb-logo-img{
                    max-width: 186px;
                }.tdi_10 .tdb-logo-text-tagline{
                    margin-top: -2px;
                    margin-left: 0;
                }
}

/* phone */
@media (max-width: 767px){
.tdi_10 .tdb-logo-a,
                .tdi_10 h1{
                    flex-direction: row;
                }.tdi_10 .tdb-logo-svg-wrap + .tdb-logo-img-wrap{
                    display: none;
                }.tdi_10 .tdb-logo-img{
                    max-width: 180px;
                }.tdi_10 .tdb-logo-img-wrap{
                    display: block;
                }
}
</style><div class="tdb-block-inner td-fix-index"><a class="tdb-logo-a" href="https://blog.devart.com/"><span class="tdb-logo-img-wrap"><img class="tdb-logo-img" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20146%2057'%3E%3C/svg%3E" alt="Logo"  title=""  width="146" height="57" data-lazy-src="https://blog.devart.com/wp-content/uploads/2022/12/devart_logo.png" /><noscript><img class="tdb-logo-img" src="https://blog.devart.com/wp-content/uploads/2022/12/devart_logo.png" alt="Logo"  title=""  width="146" height="57" /></noscript></span></a></div></div> <!-- ./block --></div></div><div class="vc_column tdi_12  wpb_column vc_column_container tdc-column td-pb-span4">
<style scoped>

/* custom css */
.tdi_12{
                    vertical-align: baseline;
                }.tdi_12 > .wpb_wrapper,
				.tdi_12 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_12 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_12 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_12 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}

/* phone */
@media (max-width: 767px){
.tdi_12{
                    vertical-align: middle;
                }
}
/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_12{
width:20% !important;
display:inline-block !important;
}
}

</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_mobile_search tdi_13 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_13" >
<style>

/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_13{
margin-right:-18px !important;
margin-bottom:0px !important;
}
}

</style>
<style>
/* custom css */
.tdb_mobile_search{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_mobile_search a{
                  display: inline-block !important;
                  position: relative;
                  text-align: center;
                  color: #4db2ec;
                }.tdb_mobile_search a > span{
                  display: flex;
                  align-items: center;
                  justify-content: center;
                }.tdb_mobile_search svg{
                  height: auto;
                }.tdb_mobile_search svg,
                .tdb_mobile_search svg *{
                  fill: #4db2ec;
                }#tdc-live-iframe .tdb_mobile_search a{
                  pointer-events: none;
                }.td-search-opened{
                  overflow: hidden;
                }.td-search-opened #td-outer-wrap{
                  position: static;
                }.td-search-opened .td-search-wrap-mob{
                  position: fixed;
                }.tdi_13{
                    display: inline-block;
                
                    float: right;
                    clear: none;
                }.tdi_13 .tdb-header-search-button-mob i{
                    font-size: 22px;
                
                    width: 55px;
					height: 55px;
					line-height:  55px;
                }.tdi_13 .tdb-header-search-button-mob svg{
                    width: 22px;
                }.tdi_13 .tdb-header-search-button-mob .tdb-mobile-search-icon-svg{
                    width: 55px;
					height: 55px;
					display: flex;
                    justify-content: center;
                }.tdi_13 .tdb-header-search-button-mob{
                    color: #ffffff;
                }.tdi_13 .tdb-header-search-button-mob svg,
                .tdi_13 .tdb-header-search-button-mob svg *{
                    fill: #ffffff;
                }
</style><div class="tdb-block-inner td-fix-index"><span class="tdb-header-search-button-mob dropdown-toggle" data-toggle="dropdown"><span class="tdb-mobile-search-icon tdb-mobile-search-icon-svg" ><svg version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024"><path d="M946.371 843.601l-125.379-125.44c43.643-65.925 65.495-142.1 65.475-218.040 0.051-101.069-38.676-202.588-115.835-279.706-77.117-77.148-178.606-115.948-279.644-115.886-101.079-0.061-202.557 38.738-279.665 115.876-77.169 77.128-115.937 178.627-115.907 279.716-0.031 101.069 38.728 202.588 115.907 279.665 77.117 77.117 178.616 115.825 279.665 115.804 75.94 0.020 152.136-21.862 218.061-65.495l125.348 125.46c30.915 30.904 81.029 30.904 111.954 0.020 30.915-30.935 30.915-81.029 0.020-111.974zM705.772 714.925c-59.443 59.341-136.899 88.842-214.784 88.924-77.896-0.082-155.341-29.583-214.784-88.924-59.443-59.484-88.975-136.919-89.037-214.804 0.061-77.885 29.604-155.372 89.037-214.825 59.464-59.443 136.878-88.945 214.784-89.016 77.865 0.082 155.3 29.583 214.784 89.016 59.361 59.464 88.914 136.919 88.945 214.825-0.041 77.885-29.583 155.361-88.945 214.804z"></path></svg></span></span></div></div> <!-- ./block --></div></div></div></div></div></div>                </div>
                                <div class="td-header-mobile-sticky-wrap tdc-zone-sticky-invisible tdc-zone-sticky-inactive" style="display: none">
                    <div id="tdi_14" class="tdc-zone"><div class="tdc_zone tdi_15  wpb_row td-pb-row" data-sticky-offset="0" >
<style scoped>

/* custom css */
.tdi_15{
                    min-height: 0;
                }.td-header-mobile-sticky-wrap.td-header-active{
                    opacity: 1;
                }
</style><div id="tdi_16" class="tdc-row"><div class="vc_row tdi_17  wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_17,
                .tdi_17 .tdc-columns{
                    min-height: 0;
                }.tdi_17,
				.tdi_17 .tdc-columns{
				    display: block;
				}.tdi_17 .tdc-columns{
				    width: 100%;
				}
</style><div class="vc_column tdi_19  wpb_column vc_column_container tdc-column td-pb-span12">
<style scoped>

/* custom css */
.tdi_19{
                    vertical-align: baseline;
                }.tdi_19 > .wpb_wrapper,
				.tdi_19 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_19 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_19 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_19 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}
</style><div class="wpb_wrapper" ></div></div></div></div></div></div>                </div>
                
                <div class="td-header-desktop-wrap ">
                    <!-- LOGIN MODAL -->

                <div id="login-form" class="white-popup-block mfp-hide mfp-with-anim td-login-modal-wrap">
                    <div class="td-login-wrap">
                        <a href="#" aria-label="Back" class="td-back-button"><i class="td-icon-modal-back"></i></a>
                        <div id="td-login-div" class="td-login-form-div td-display-block">
                            <div class="td-login-panel-title">Sign in</div>
                            <div class="td-login-panel-descr">Welcome! Log into your account</div>
                            <div class="td_display_err"></div>
                            <form id="loginForm" action="#" method="post">
                                <div class="td-login-inputs"><input class="td-login-input" autocomplete="username" type="text" name="login_email" id="login_email" value="" required><label for="login_email">your username</label></div>
                                <div class="td-login-inputs"><input class="td-login-input" autocomplete="current-password" type="password" name="login_pass" id="login_pass" value="" required><label for="login_pass">your password</label></div>
                                <input type="button"  name="login_button" id="login_button" class="wpb_button btn td-login-button" value="Login">
                                
                            </form>

                            

                            <div class="td-login-info-text"><a href="#" id="forgot-pass-link">Forgot your password? Get help</a></div>
                            
                            
                            
                            
                        </div>

                        

                         <div id="td-forgot-pass-div" class="td-login-form-div td-display-none">
                            <div class="td-login-panel-title">Password recovery</div>
                            <div class="td-login-panel-descr">Recover your password</div>
                            <div class="td_display_err"></div>
                            <form id="forgotpassForm" action="#" method="post">
                                <div class="td-login-inputs"><input class="td-login-input" type="text" name="forgot_email" id="forgot_email" value="" required><label for="forgot_email">your email</label></div>
                                <input type="button" name="forgot_button" id="forgot_button" class="wpb_button btn td-login-button" value="Send My Password">
                            </form>
                            <div class="td-login-info-text">A password will be e-mailed to you.</div>
                        </div>
                        
                        
                    </div>
                </div>
                <div id="tdi_20" class="tdc-zone"><div class="tdc_zone tdi_21  wpb_row td-pb-row tdc-element-style"  >
<style scoped>

/* custom css */
.tdi_21{
                    min-height: 0;
                }.tdi_21 > .td-element-style:after{
                    content: '' !important;
                    width: 100% !important;
                    height: 100% !important;
                    position: absolute !important;
                    top: 0 !important;
                    left: 0 !important;
                    z-index: 0 !important;
                    display: block !important;
                    background-color: #ffffff !important;
                }.tdi_21:before{
                    content: '';
                    display: block;
                    width: 100vw;
                    height: 100%;
                    position: absolute;
                    left: 50%;
                    transform: translateX(-50%);
                    box-shadow:  0px 6px 8px 0px rgba(0, 0, 0, 0.08);
                    z-index: 20;
                    pointer-events: none;
                }.td-header-desktop-wrap{
                    position: relative;
                }@media (max-width: 767px) {
                    .tdi_21:before {
                        width: 100%;
                    }
                }
/* inline tdc_css att */

.tdi_21{
position:relative;
}

</style>
<div class="tdi_20_rand_style td-element-style" ><style>
.tdi_20_rand_style{
background-color:#ffffff !important;
}
 </style></div><div id="tdi_22" class="tdc-row stretch_row"><div class="vc_row tdi_23  wpb_row td-pb-row tdc-element-style" >
<style scoped>

/* custom css */
.tdi_23,
                .tdi_23 .tdc-columns{
                    min-height: 0;
                }.tdi_23,
				.tdi_23 .tdc-columns{
				    display: block;
				}.tdi_23 .tdc-columns{
				    width: 100%;
				}@media (min-width: 768px) {
	                .tdi_23 {
	                    margin-left: -0px;
	                    margin-right: -0px;
	                }
	                .tdi_23 .tdc-row-video-background-error,
	                .tdi_23 .vc_column {
	                    padding-left: 0px;
	                    padding-right: 0px;
	                }
                }
/* inline tdc_css att */

.tdi_23{
position:relative;
}

.tdi_23 .td_block_wrap{ text-align:left }

</style>
<div class="tdi_22_rand_style td-element-style" ><style>
.tdi_22_rand_style{
background-color:#222222 !important;
}
 </style></div><div class="vc_column tdi_25  wpb_column vc_column_container tdc-column tdc-restr-display-none td-pb-span12">
<style scoped>

/* custom css */
.tdi_25{
                    vertical-align: baseline;
                }.tdi_25 > .wpb_wrapper,
				.tdi_25 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_25 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_25 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_25 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}
</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_header_date tdi_26 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_26" >
<style>

/* inline tdc_css att */

.tdi_26{
margin-right:32px !important;
}

/* landscape */
@media (min-width: 1019px) and (max-width: 1140px)
{
.tdi_26{
margin-right:20px !important;
}
}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px)
{
.tdi_26{
margin-right:20px !important;
}
}

</style>
<style>
/* custom css */
.tdb_header_date{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_header_date .tdb-block-inner{
                  display: flex;
                  align-items: baseline;
                }.tdb_header_date .tdb-head-date-txt{
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                  font-size: 11px;
                  line-height: 1;
                  color: #000;
                }.tdi_26{
                    display: inline-block;
                }.tdi_26 .tdb-head-date-txt{
                    color: #ffffff;
                
                    line-height:28px !important;
                }
</style><div class="tdb-block-inner td-fix-index"><div class="tdb-head-date-txt">Wednesday, June 14, 2023</div></div></div> <!-- ./block -->

<script type="rocketlazyloadscript">

var tdb_login_sing_in_shortcode="on";

</script>

<div class="td_block_wrap tdb_header_user tdi_27 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_27" >
<style>

/* inline tdc_css att */

.tdi_27{
margin-right:14px !important;
}

</style>
<style>
/* custom css */
.tdb_header_user{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_header_user .tdb-block-inner{
                  display: flex;
                  align-items: center;
                }.tdb_header_user .tdb-head-usr-item{
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                  font-size: 11px;
                  line-height: 1;
                  color: #000;
                }.tdb_header_user .tdb-head-usr-item:hover{
                  color: #4db2ec;
                }.tdb_header_user .tdb-head-usr-avatar{
                  position: relative;
                  width: 20px;
                  height: 0;
                  padding-bottom: 20px;
                  margin-right: 6px;
                  background-size: cover;
                  background-position: center center;
                }.tdb_header_user .tdb-head-usr-name{
                  margin-right: 16px;
                  font-weight: 700;
                }.tdb_header_user .tdb-head-usr-log{
                  display: flex;
                  align-items: center;
                }.tdb_header_user .tdb-head-usr-log i{
                  font-size: 10px;
                }.tdb_header_user .tdb-head-usr-log-icon{
                  position: relative;
                }.tdb_header_user .tdb-head-usr-log-icon-svg{
                  line-height: 0;
                }.tdb_header_user .tdb-head-usr-log-icon-svg svg{
                  width: 10px;
                  height: auto;
                }.tdi_27{
                    display: inline-block;
                }.tdi_27 .tdb-head-usr-avatar{
                    width: 19px;
                    padding-bottom: 19px;
                }.tdi_27 .tdb-head-usr-log .tdb-head-usr-log-icon{
                    margin-right: 2px;
                
                    top: 0px;
                }.tdi_27 .tdb-head-usr-name{
                    color: #ffffff;
                
                    line-height:28px !important;
                }.tdi_27 .tdb-head-usr-log{
                    color: #ffffff;
                
                    line-height:28px !important;
                }.tdi_27 .tdb-head-usr-log-icon-svg svg,
                .tdi_27 .tdb-head-usr-log-icon-svg svg *{
                    fill: #ffffff;
                
                    fill: #ffffff;
                }.tdi_27 .tdb-head-usr-log i{
                    color: #ffffff;
                }
</style><div class="tdb-block-inner td-fix-index"><a class="td-login-modal-js tdb-head-usr-item tdb-head-usr-log" href="#login-form" data-effect="mpf-td-login-effect"><span class="tdb-head-usr-log-txt">Sign in / Join</span></a></div></div> <!-- ./block --><div class="td_block_wrap tdb_mobile_horiz_menu tdi_28 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_28"  style=" z-index: 999;">
<style>

/* inline tdc_css att */

.tdi_28{
margin-bottom:0px !important;
}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px)
{
.tdi_28{
display:none !important;
}
}

</style>
<style>
/* custom css */
.tdb_mobile_horiz_menu{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_mobile_horiz_menu.tdb-horiz-menu-singleline{
                  width: 100%;
                }.tdb_mobile_horiz_menu.tdb-horiz-menu-singleline .tdb-horiz-menu{
                  display: block;
                  width: 100%;
                  overflow-x: auto;
                  overflow-y: hidden;
                  font-size: 0;
                  white-space: nowrap;
                }.tdb_mobile_horiz_menu.tdb-horiz-menu-singleline .tdb-horiz-menu > li{
                  position: static;
                  display: inline-block;
                  float: none;
                }.tdb_mobile_horiz_menu.tdb-horiz-menu-singleline .tdb-horiz-menu ul{
                  left: 0;
                  width: 100%;
                  z-index: -1;
                }.tdb-horiz-menu{
                  display: table;
                  margin: 0;
                }.tdb-horiz-menu,
                .tdb-horiz-menu ul{
                  list-style-type: none;
                }.tdb-horiz-menu ul,
                .tdb-horiz-menu li{
                  line-height: 1;
                }.tdb-horiz-menu li{
                  margin: 0;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                }.tdb-horiz-menu li.current-menu-item > a,
                .tdb-horiz-menu li.current-menu-ancestor > a,
                .tdb-horiz-menu li.current-category-ancestor > a,
                .tdb-horiz-menu li:hover > a,
                .tdb-horiz-menu li.tdb-hover > a{
                  color: #4db2ec;
                }.tdb-horiz-menu li.current-menu-item > a .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu li.current-menu-ancestor > a .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu li.current-category-ancestor > a .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu li:hover > a .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu li.tdb-hover > a .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu li.current-menu-item > a .tdb-sub-menu-icon-svg *,
                .tdb-horiz-menu li.current-menu-ancestor > a .tdb-sub-menu-icon-svg *,
                .tdb-horiz-menu li.current-category-ancestor > a .tdb-sub-menu-icon-svg *,
                .tdb-horiz-menu li:hover > a .tdb-sub-menu-icon-svg *,
                .tdb-horiz-menu li.tdb-hover > a .tdb-sub-menu-icon-svg *{
                  fill: #4db2ec;
                }.tdb-horiz-menu > li{
                  position: relative;
                  float: left;
                  font-size: 0;
                }.tdb-horiz-menu > li:hover ul{
                  visibility: visible;
                  opacity: 1;
                }.tdb-horiz-menu > li > a{
                  display: inline-block;
                  padding: 0 9px;
                  font-weight: 700;
                  font-size: 13px;
                  line-height: 41px;
                  vertical-align: middle;
                  -webkit-backface-visibility: hidden;
                  color: #000;
                }.tdb-horiz-menu > li > a > .tdb-menu-item-text{
                  display: inline-block;
                }.tdb-horiz-menu > li > a .tdb-sub-menu-icon{
                  margin: 0 0 0 6px;
                }.tdb-horiz-menu > li > a .tdb-sub-menu-icon-svg svg{
                  position: relative;
                  top: -1px;
                  width: 13px;
                }.tdb-horiz-menu > li .tdb-menu-sep{
                  position: relative;
                }.tdb-horiz-menu > li:last-child .tdb-menu-sep{
                  display: none;
                }.tdb-horiz-menu .tdb-sub-menu-icon-svg,
                .tdb-horiz-menu .tdb-menu-sep-svg{
                  line-height: 0;
                }.tdb-horiz-menu .tdb-sub-menu-icon-svg svg,
                .tdb-horiz-menu .tdb-menu-sep-svg svg{
                  height: auto;
                }.tdb-horiz-menu .tdb-sub-menu-icon-svg svg,
                .tdb-horiz-menu .tdb-menu-sep-svg svg,
                .tdb-horiz-menu .tdb-sub-menu-icon-svg svg *,
                .tdb-horiz-menu .tdb-menu-sep-svg svg *{
                  fill: #000;
                }.tdb-horiz-menu .tdb-sub-menu-icon{
                  vertical-align: middle;
                
                  position: relative;
                  top: 0;
                  padding-left: 0;
                }.tdb-horiz-menu .tdb-menu-sep{
                  vertical-align: middle;
                  font-size: 12px;
                }.tdb-horiz-menu .tdb-menu-sep-svg svg{
                  width: 12px;
                }.tdb-horiz-menu ul{
                  position: absolute;
                  top: auto;
                  left: -7px;
                  padding: 8px 0;
                  background-color: #fff;
                  visibility: hidden;
                  opacity: 0;
                }.tdb-horiz-menu ul li > a{
                  white-space: nowrap;
                  display: block;
                  padding: 5px 18px;
                  font-size: 11px;
                  line-height: 18px;
                  color: #111;
                }.tdb-horiz-menu ul li > a .tdb-sub-menu-icon{
                  float: right;
                  font-size: 7px;
                  line-height: 20px;
                }.tdb-horiz-menu ul li > a .tdb-sub-menu-icon-svg svg{
                  width: 7px;
                }.tdc-dragged .tdb-horiz-menu ul{
                  visibility: hidden !important;
                  opacity: 0 !important;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                }.tdi_28{
                    display: inline-block;
                }.tdi_28 .tdb-horiz-menu > li{
                    margin-right: 16px;
                }.tdi_28 .tdb-horiz-menu > li:last-child{
                    margin-right: 0;
                }.tdi_28 .tdb-horiz-menu > li > a{
                    padding: 0px;
                
                    color: #ffffff;
                
                    font-size:11px !important;line-height:28px !important;font-weight:400 !important;
                }.tdi_28 .tdb-horiz-menu > li .tdb-menu-sep{
                    top: 0px;
                }.tdi_28 .tdb-horiz-menu > li > a  .tdb-sub-menu-icon{
                    top: 0px;
                }.tdi_28 .tdb-horiz-menu > li > a .tdb-sub-menu-icon-svg svg,
                .tdi_28 .tdb-horiz-menu > li > a .tdb-sub-menu-icon-svg svg *{
                    fill: #ffffff;
                }.tdi_28 .tdb-horiz-menu > li.current-menu-item > a,
                .tdi_28 .tdb-horiz-menu > li.current-menu-ancestor > a,
                .tdi_28 .tdb-horiz-menu > li.current-category-ancestor > a,
                .tdi_28 .tdb-horiz-menu > li:hover > a{
                    color: #4db2ec;
                }.tdi_28 .tdb-horiz-menu > li.current-menu-item > a .tdb-sub-menu-icon-svg svg,
                .tdi_28 .tdb-horiz-menu > li.current-menu-item > a .tdb-sub-menu-icon-svg svg *,
                .tdi_28 .tdb-horiz-menu > li.current-menu-ancestor > a .tdb-sub-menu-icon-svg svg,
                .tdi_28 .tdb-horiz-menu > li.current-menu-ancestor > a .tdb-sub-menu-icon-svg svg *,
                .tdi_28 .tdb-horiz-menu > li.current-category-ancestor > a .tdb-sub-menu-icon-svg svg,
                .tdi_28 .tdb-horiz-menu > li.current-category-ancestor > a .tdb-sub-menu-icon-svg svg *,
                .tdi_28 .tdb-horiz-menu > li:hover > a .tdb-sub-menu-icon-svg svg,
                .tdi_28 .tdb-horiz-menu > li:hover > a .tdb-sub-menu-icon-svg svg *{
                    fill: #4db2ec;
                }.tdi_28 .tdb-horiz-menu ul{
                    left: -18px;
                
                    box-shadow:  1px 1px 4px 0px rgba(0, 0, 0, 0.15);
                }.tdi_28 .tdb-horiz-menu ul li > a{
                    line-height:1.2 !important;
                }
</style><div id=tdi_28 class="td_block_inner td-fix-index"></div></div><div class="tdm_block td_block_wrap tdm_block_socials tdi_29 tdm-content-horiz-left td-pb-border-top td_block_template_10"  data-td-block-uid="tdi_29" >
<style>
/* custom css */
.tdm_block.tdm_block_socials{
                  margin-bottom: 0;
                }.tdm-social-wrapper{
                  *zoom: 1;
                }.tdm-social-wrapper:before,
                .tdm-social-wrapper:after{
                  display: table;
                  content: '';
                  line-height: 0;
                }.tdm-social-wrapper:after{
                  clear: both;
                }.tdm-social-item-wrap{
                  display: inline-block;
                }.tdm-social-item{
                  position: relative;
                  display: inline-block;
                  vertical-align: middle;
                  -webkit-transition: all 0.2s;
                  transition: all 0.2s;
                  text-align: center;
                  -webkit-transform: translateZ(0);
                  transform: translateZ(0);
                }.tdm-social-item i{
                  font-size: 14px;
                  color: #4db2ec;
                  -webkit-transition: all 0.2s;
                  transition: all 0.2s;
                }.tdm-social-text{
                  display: none;
                  margin-top: -1px;
                  vertical-align: middle;
                  font-size: 13px;
                  color: #4db2ec;
                  -webkit-transition: all 0.2s;
                  transition: all 0.2s;
                }.tdm-social-item-wrap:hover i,
                .tdm-social-item-wrap:hover .tdm-social-text{
                  color: #000;
                }.tdm-social-item-wrap:last-child .tdm-social-text{
                  margin-right: 0 !important;
                }.tdi_29{
                    float: right;
                    clear: none;
                }
</style>
<style>
.tdi_30 .tdm-social-item i{
					font-size: 12px;
					vertical-align: middle;
				
					line-height: 22.8px;
				}.tdi_30 .tdm-social-item i.td-icon-twitter,
				.tdi_30 .tdm-social-item i.td-icon-linkedin,
				.tdi_30 .tdm-social-item i.td-icon-pinterest,
				.tdi_30 .tdm-social-item i.td-icon-blogger,
				.tdi_30 .tdm-social-item i.td-icon-vimeo{
					font-size: 9.6px;
				}.tdi_30 .tdm-social-item{
					width: 22.8px;
					height: 22.8px;
				
				    margin: 2.5px 5px 2.5px 0;
				}.tdi_30 .tdm-social-item-wrap:last-child .tdm-social-item{
				    margin-right: 0 !important;
				}.tdi_30 .tdm-social-item i,
				.tds-team-member2 .tdi_30.tds-social1 .tdm-social-item i{
					color: #ffffff;
				}.tdi_30 .tdm-social-item-wrap:hover i,
				.tds-team-member2 .tdi_30.tds-social1 .tdm-social-item:hover i{
					color: #4db2ec;
				}.tdi_30 .tdm-social-text{
					display: none;
				
					margin-left: 2px;
				
					margin-right: 18px;
				}
</style><div class="tdm-social-wrapper tds-social1 tdi_30"><div class="tdm-social-item-wrap"><a href="#"  title="Facebook" class="tdm-social-item"><i class="td-icon-font td-icon-facebook"></i></a><a href="#"  class="tdm-social-text" >Facebook</a></div><div class="tdm-social-item-wrap"><a href="#"  title="Instagram" class="tdm-social-item"><i class="td-icon-font td-icon-instagram"></i></a><a href="#"  class="tdm-social-text" >Instagram</a></div><div class="tdm-social-item-wrap"><a href="#"  title="Twitter" class="tdm-social-item"><i class="td-icon-font td-icon-twitter"></i></a><a href="#"  class="tdm-social-text" >Twitter</a></div><div class="tdm-social-item-wrap"><a href="#"  title="Vimeo" class="tdm-social-item"><i class="td-icon-font td-icon-vimeo"></i></a><a href="#"  class="tdm-social-text" >Vimeo</a></div><div class="tdm-social-item-wrap"><a href="#"  title="Youtube" class="tdm-social-item"><i class="td-icon-font td-icon-youtube"></i></a><a href="#"  class="tdm-social-text" >Youtube</a></div></div></div></div></div></div></div><div id="tdi_31" class="tdc-row tdc-row-is-sticky tdc-rist-top stretch_row_1200 td-stretch-content"><div class="vc_row tdi_32  wpb_row td-pb-row tdc-element-style" >
<style scoped>

/* custom css */
body .tdc-row.tdc-rist-top-active,
                body .tdc-row.tdc-rist-bottom-active{
                  position: fixed;
                  left: 50%;
                  transform: translateX(-50%);
                  z-index: 10000;
                }body .tdc-row.tdc-rist-top-active.td-stretch-content,
                body .tdc-row.tdc-rist-bottom-active.td-stretch-content{
                  width: 100% !important;
                }body .tdc-row.tdc-rist-top-active{
                  top: 0;
                }body .tdc-row.tdc-rist-absolute{
                  position: absolute;
                }body .tdc-row.tdc-rist-bottom-active{
                  bottom: 0;
                }.tdi_32,
                .tdi_32 .tdc-columns{
                    min-height: 0;
                }#tdi_31.tdc-rist-top-active .tdi_32 > .td-element-style:after,
                 #tdi_31.tdc-rist-bottom-active .tdi_32 > .td-element-style:after{
                    content: '' !important;
                    width: 100% !important;
                    height: 100% !important;
                    position: absolute !important;
                    top: 0 !important;
                    left: 0 !important;
                    z-index: 0 !important;
                    display: block !important;
                    background: #ffffff !important;
                }.tdi_32,
				.tdi_32 .tdc-columns{
				    display: block;
				}.tdi_32 .tdc-columns{
				    width: 100%;
				}@media (min-width: 767px) {
                  body.admin-bar .tdc-row.tdc-rist-top-active {
                    top: 32px;
                  }
                }
</style>
<div class="tdi_31_rand_style td-element-style" ></div><div class="vc_column tdi_34  wpb_column vc_column_container tdc-column td-pb-span12">
<style scoped>

/* custom css */
.tdi_34{
                    vertical-align: baseline;
                
				    flex-grow: 1;
				}.tdi_34 > .wpb_wrapper,
				.tdi_34 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_34 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_34 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_34 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}
/* inline tdc_css att */

.tdi_34{
position:relative;
}

</style>
<div class="tdi_33_rand_style td-element-style" ><div class="td-element-style-before"><style>
.tdi_33_rand_style > .td-element-style-before {
content:'' !important;
width:100% !important;
height:100% !important;
position:absolute !important;
top:0 !important;
left:0 !important;
display:block !important;
z-index:0 !important;
background-repeat:repeat !important;
background-position:center top !important;
}
</style></div><style>
.tdi_33_rand_style{
background-color:#ffffff !important;
}
 </style></div><div class="wpb_wrapper" ><div class="vc_row_inner tdi_36  vc_row vc_inner wpb_row td-pb-row tdc-row-content-vert-center" >
<style scoped>

/* custom css */
.tdi_36{
                    position: relative !important;
                    top: 0;
                    transform: none;
                    -webkit-transform: none;
                }.tdi_36,
				.tdi_36 .tdc-inner-columns{
				    display: block;
				}.tdi_36 .tdc-inner-columns{
				    width: 100%;
				}@media (min-width: 768px) {
	                .tdi_36 {
	                    margin-left: -0px;
	                    margin-right: -0px;
	                }
	                .tdi_36 .vc_column_inner {
	                    padding-left: 0px;
	                    padding-right: 0px;
	                }
                }@media (min-width: 767px) {
                    .tdi_36.tdc-row-content-vert-center,
                    .tdi_36.tdc-row-content-vert-center .tdc-inner-columns {
                        display: flex;
                        align-items: center;
                        flex: 1;
                    }
                    .tdi_36.tdc-row-content-vert-bottom,
                    .tdi_36.tdc-row-content-vert-bottom .tdc-inner-columns {
                        display: flex;
                        align-items: flex-end;
                        flex: 1;
                    }
                    .tdi_36.tdc-row-content-vert-center .td_block_wrap {
                        vertical-align: middle;
                    }
                    .tdi_36.tdc-row-content-vert-bottom .td_block_wrap {
                        vertical-align: bottom;
                    }
                }
/* inline tdc_css att */

.tdi_36{
padding-top:12px !important;
padding-bottom:9px !important;
}

.tdi_36 .td_block_wrap{ text-align:left }

/* portrait */
@media (min-width: 768px) and (max-width: 1018px)
{
.tdi_36{
margin-bottom:-3px !important;
padding-top:9px !important;
padding-bottom:0px !important;
}
}

</style><div class="vc_column_inner tdi_38  wpb_column vc_column_container tdc-inner-column td-pb-span3">
<style scoped>

/* custom css */
.tdi_38{
                    vertical-align: baseline;
                }.tdi_38 .vc_column-inner > .wpb_wrapper,
				.tdi_38 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    display: block;
				}.tdi_38 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    width: 100%;
				}
/* inline tdc_css att */

.tdi_38{
width:30% !important;
}

/* landscape */
@media (min-width: 1019px) and (max-width: 1140px)
{
.tdi_38{
width:24% !important;
}
}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px)
{
.tdi_38{
width:calc(100% - 468px) !important;
}
}

</style><div class="vc_column-inner"><div class="wpb_wrapper" ><div class="td_block_wrap tdb_header_logo tdi_39 td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_39" >
<style>
/* custom css */
.tdi_39 .tdb-logo-a,
                .tdi_39 h1{
                    align-items: center;
                
                    justify-content: flex-start;
                }.tdi_39 .tdb-logo-svg-wrap{
                    display: block;
                }.tdi_39 .tdb-logo-svg-wrap + .tdb-logo-img-wrap{
                    display: none;
                }.tdi_39 .tdb-logo-img{
                    max-width: 146px;
                }.tdi_39 .tdb-logo-text-tagline{
                    margin-top: 2px;
                    margin-left: 0;
                
                    display: block;
                }.tdi_39 .tdb-logo-text-title{
                    display: block;
                }.tdi_39 .tdb-logo-text-wrap{
                    flex-direction: column;
                
                    align-items: flex-start;
                }.tdi_39 .tdb-logo-icon{
                    top: 0px;
                
                    display: block;
                }

/* portrait */
@media (min-width: 768px) and (max-width: 1018px){
.tdi_39 .tdb-logo-img{
                    max-width: 220px;
                }
}
</style><div class="tdb-block-inner td-fix-index"><a class="tdb-logo-a" href="https://www.devart.com/"><span class="tdb-logo-img-wrap"><img class="tdb-logo-img" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20146%2057'%3E%3C/svg%3E" alt="Logo"  title=""  width="146" height="57" data-lazy-src="https://blog.devart.com/wp-content/uploads/2022/12/devart_logo.png" /><noscript><img class="tdb-logo-img" src="https://blog.devart.com/wp-content/uploads/2022/12/devart_logo.png" alt="Logo"  title=""  width="146" height="57" /></noscript></span></a></div></div> <!-- ./block --></div></div></div><div class="vc_column_inner tdi_41  wpb_column vc_column_container tdc-inner-column td-pb-span6">
<style scoped>

/* custom css */
.tdi_41{
                    vertical-align: baseline;
                }.tdi_41 .vc_column-inner > .wpb_wrapper,
				.tdi_41 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    display: block;
				}.tdi_41 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    width: 100%;
				}
</style><div class="vc_column-inner"><div class="wpb_wrapper" ><div class="td_block_wrap tdb_header_menu tdi_42 tds_menu_active1 tds_menu_sub_active1 tdb-mm-align-screen td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_42"  style=" z-index: 999;">
<style>
/* custom css */
.tdb_header_menu{
                  margin-bottom: 0;
                  z-index: 999;
                  clear: none;
                }.tdb_header_menu .tdb-main-sub-icon-fake,
                .tdb_header_menu .tdb-sub-icon-fake{
                    display: none;
                }.rtl .tdb_header_menu .tdb-menu{
                  display: flex;
                }.tdb_header_menu .tdb-menu{
                  display: inline-block;
                  vertical-align: middle;
                  margin: 0;
                }.tdb_header_menu .tdb-menu .tdb-mega-menu-inactive,
                .tdb_header_menu .tdb-menu .tdb-menu-item-inactive{
                  pointer-events: none;
                }.tdb_header_menu .tdb-menu .tdb-mega-menu-inactive > ul,
                .tdb_header_menu .tdb-menu .tdb-menu-item-inactive > ul{
                  visibility: hidden;
                  opacity: 0;
                }.tdb_header_menu .tdb-menu .sub-menu{
                  font-size: 14px;
                
                  position: absolute;
                  top: -999em;
                  background-color: #fff;
                  z-index: 99;
                }.tdb_header_menu .tdb-menu .sub-menu > li{
                  list-style-type: none;
                  margin: 0;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                }.tdb_header_menu .tdb-menu > li{
                  float: left;
                  list-style-type: none;
                  margin: 0;
                }.tdb_header_menu .tdb-menu > li > a{
                  position: relative;
                  display: inline-block;
                  padding: 0 14px;
                  font-weight: 700;
                  font-size: 14px;
                  line-height: 48px;
                  vertical-align: middle;
                  text-transform: uppercase;
                  -webkit-backface-visibility: hidden;
                  color: #000;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                }.tdb_header_menu .tdb-menu > li > a:after{
                  content: '';
                  position: absolute;
                  bottom: 0;
                  left: 0;
                  right: 0;
                  margin: 0 auto;
                  width: 0;
                  height: 3px;
                  background-color: #4db2ec;
                  -webkit-transform: translate3d(0, 0, 0);
                  transform: translate3d(0, 0, 0);
                  -webkit-transition: width 0.2s ease;
                  transition: width 0.2s ease;
                }.tdb_header_menu .tdb-menu > li > a > .tdb-menu-item-text{
                  display: inline-block;
                }.tdb_header_menu .tdb-menu > li > a .tdb-menu-item-text,
                .tdb_header_menu .tdb-menu > li > a span{
                  vertical-align: middle;
                  float: left;
                }.tdb_header_menu .tdb-menu > li > a .tdb-sub-menu-icon{
                  margin: 0 0 0 7px;
                }.tdb_header_menu .tdb-menu > li > a .tdb-sub-menu-icon-svg{
                  float: none;
                  line-height: 0;
                }.tdb_header_menu .tdb-menu > li > a .tdb-sub-menu-icon-svg svg{
                  width: 14px;
                  height: auto;
                }.tdb_header_menu .tdb-menu > li > a .tdb-sub-menu-icon-svg svg,
                .tdb_header_menu .tdb-menu > li > a .tdb-sub-menu-icon-svg svg *{
                  fill: #000;
                }.tdb_header_menu .tdb-menu > li.current-menu-item > a:after,
                .tdb_header_menu .tdb-menu > li.current-menu-ancestor > a:after,
                .tdb_header_menu .tdb-menu > li.current-category-ancestor > a:after,
                .tdb_header_menu .tdb-menu > li:hover > a:after,
                .tdb_header_menu .tdb-menu > li.tdb-hover > a:after{
                  width: 100%;
                }.tdb_header_menu .tdb-menu > li:hover > ul,
                .tdb_header_menu .tdb-menu > li.tdb-hover > ul{
                  top: auto;
                  display: block !important;
                }.tdb_header_menu .tdb-menu > li.td-normal-menu > ul.sub-menu{
                  top: auto;
                  left: 0;
                  z-index: 99;
                }.tdb_header_menu .tdb-menu > li .tdb-menu-sep{
                  position: relative;
                  vertical-align: middle;
                  font-size: 14px;
                }.tdb_header_menu .tdb-menu > li .tdb-menu-sep-svg{
                  line-height: 0;
                }.tdb_header_menu .tdb-menu > li .tdb-menu-sep-svg svg{
                  width: 14px;
                  height: auto;
                }.tdb_header_menu .tdb-menu > li:last-child .tdb-menu-sep{
                  display: none;
                }.tdb_header_menu .tdb-menu-item-text{
                  word-wrap: break-word;
                }.tdb_header_menu .tdb-menu-item-text,
                .tdb_header_menu .tdb-sub-menu-icon,
                .tdb_header_menu .tdb-menu-more-subicon{
                  vertical-align: middle;
                }.tdb_header_menu .tdb-sub-menu-icon,
                .tdb_header_menu .tdb-menu-more-subicon{
                  position: relative;
                  top: 0;
                  padding-left: 0;
                }.tdb_header_menu .tdb-normal-menu{
                  position: relative;
                }.tdb_header_menu .tdb-normal-menu ul{
                  left: 0;
                  padding: 15px 0;
                  text-align: left;
                }.tdb_header_menu .tdb-normal-menu ul ul{
                  margin-top: -15px;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item{
                  position: relative;
                  list-style-type: none;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a{
                  position: relative;
                  display: block;
                  padding: 7px 30px;
                  font-size: 12px;
                  line-height: 20px;
                  color: #111;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon,
                .tdb_header_menu .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon{
                  position: absolute;
                  top: 50%;
                  -webkit-transform: translateY(-50%);
                  transform: translateY(-50%);
                  right: 0;
                  padding-right: inherit;
                  font-size: 7px;
                  line-height: 20px;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon-svg,
                .tdb_header_menu .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon-svg{
                  line-height: 0;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon-svg svg,
                .tdb_header_menu .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon-svg svg{
                  width: 7px;
                  height: auto;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon-svg svg,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon-svg svg *,
                .tdb_header_menu .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon svg,
                .tdb_header_menu .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon svg *{
                  fill: #000;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item:hover > ul,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item.tdb-hover > ul{
                  top: 0;
                  display: block !important;
                }.tdb_header_menu .tdb-normal-menu ul .tdb-menu-item.current-menu-item > a,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item.current-menu-ancestor > a,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item.current-category-ancestor > a,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item.tdb-hover > a,
                .tdb_header_menu .tdb-normal-menu ul .tdb-menu-item:hover > a{
                  color: #4db2ec;
                }.tdb_header_menu .tdb-normal-menu > ul{
                  left: -15px;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu ul,
                .tdb_header_menu.tdb-menu-sub-inline .td-pulldown-filter-list{
                  width: 100% !important;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu ul li,
                .tdb_header_menu.tdb-menu-sub-inline .td-pulldown-filter-list li{
                  display: inline-block;
                  width: auto !important;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu,
                .tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu .tdb-menu-item{
                  position: static;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu ul ul{
                  margin-top: 0 !important;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu > ul{
                  left: 0 !important;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu .tdb-menu-item > a .tdb-sub-menu-icon{
                  float: none;
                  line-height: 1;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu .tdb-menu-item:hover > ul,
                .tdb_header_menu.tdb-menu-sub-inline .tdb-normal-menu .tdb-menu-item.tdb-hover > ul{
                  top: 100%;
                }.tdb_header_menu.tdb-menu-sub-inline .tdb-menu-items-dropdown{
                  position: static;
                }.tdb_header_menu.tdb-menu-sub-inline .td-pulldown-filter-list{
                  left: 0 !important;
                }.tdb-menu .tdb-mega-menu .sub-menu{
                  -webkit-transition: opacity 0.3s ease;
                  transition: opacity 0.3s ease;
                  width: 1114px !important;
                }.tdb-menu .tdb-mega-menu .sub-menu,
                .tdb-menu .tdb-mega-menu .sub-menu > li{
                  position: absolute;
                  left: 50%;
                  -webkit-transform: translateX(-50%);
                  transform: translateX(-50%);
                }.tdb-menu .tdb-mega-menu .sub-menu > li{
                  top: 0;
                  width: 100%;
                  max-width: 1114px !important;
                  height: auto;
                  background-color: #fff;
                  border: 1px solid #eaeaea;
                  overflow: hidden;
                }.tdc-dragged .tdb-block-menu ul{
                  visibility: hidden !important;
                  opacity: 0 !important;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                }.tdb-mm-align-screen .tdb-menu .tdb-mega-menu .sub-menu{
                  -webkit-transform: translateX(0);
                  transform: translateX(0);
                }.tdb-mm-align-parent .tdb-menu .tdb-mega-menu{
                  position: relative;
                }.tdi_42 .td_block_inner{
                    text-align: center;
                }.tdi_42 .tdb-menu > li .tdb-menu-sep,
                .tdi_42 .tdb-menu-items-dropdown .tdb-menu-sep{
                    top: -10px;
                }.tdi_42 .tdb-menu > li > a .tdb-sub-menu-icon,
                .tdi_42 .td-subcat-more .tdb-menu-more-subicon{
                    top: 0px;
                }.tdi_42 .td-subcat-more .tdb-menu-more-icon{
                    top: 0px;
                }.tdi_42 .tdb-menu > li > a,
                .tdi_42 .td-subcat-more,
                .tdi_42 .td-subcat-more > .tdb-menu-item-text{
                    font-family:Firasans Regular !important;font-size:16px !important;font-weight:500 !important;text-transform:capitalize !important;
                }.tdi_42 .tdb-normal-menu ul .tdb-menu-item > a .tdb-sub-menu-icon,
                .tdi_42 .td-pulldown-filter-list .tdb-menu-item > a .tdb-sub-menu-icon{
                    right: 0;
                
                    margin-top: 1px;
                }.tdi_42 .tdb-menu .tdb-normal-menu ul,
                .tdi_42 .td-pulldown-filter-list,
                .tdi_42 .td-pulldown-filter-list .sub-menu{
                    box-shadow:  1px 1px 4px 0px rgba(0, 0, 0, 0.15);
                }.tdi_42 .tdb-menu .tdb-normal-menu ul .tdb-menu-item > a,
                .tdi_42 .td-pulldown-filter-list li a{
                    font-family:Firasans Regular !important;
                }.tdi_42:not(.tdb-mm-align-screen) .tdb-mega-menu .sub-menu,
                .tdi_42 .tdb-mega-menu .sub-menu > li{
                    max-width: 1300px !important;
                }.tdi_42 .tdb-mega-menu .tdb_header_mega_menu{
                    min-height: 345px;
                }.tdi_42 .tdb-menu .tdb-mega-menu .sub-menu > li{
					box-shadow:  0px 2px 6px 0px rgba(0, 0, 0, 0.1);
				}@media (max-width: 1140px) {
                  .tdb-menu .tdb-mega-menu .sub-menu > li {
                    width: 100% !important;
                  }
                }

/* landscape */
@media (min-width: 1019px) and (max-width: 1140px){
.tdi_42 .tdb-mega-menu .tdb_header_mega_menu{
                    min-height: 300px;
                }
}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px){
.tdi_42 .tdb-menu > li > a,
                .tdi_42 .td-subcat-more{
                    padding: 0 12px;
                }.tdi_42 .tdb-menu > li > a,
                .tdi_42 .td-subcat-more,
                .tdi_42 .td-subcat-more > .tdb-menu-item-text{
                    font-family:Firasans Regular !important;font-size:11px !important;line-height:48px !important;font-weight:500 !important;text-transform:capitalize !important;
                }.tdi_42 .tdb-mega-menu .tdb_header_mega_menu{
                    min-height: 240px;
                }
}
</style>
<style>
.tdi_42 .tdb-menu > li > a:after,
				.tdi_42 .tdb-menu-items-dropdown .td-subcat-more:after{
					background-color: #0071ce;
				
					bottom: 0px;
				}
</style>
<style>
.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-item > a,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-ancestor > a,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-category-ancestor > a,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.tdb-hover > a,
				.tdi_42 .tdb-menu ul .tdb-normal-menu:hover > a,
				.tdi_42 .tdb-menu-items-dropdown .td-pulldown-filter-list li:hover > a{
					color: #0071ce;
				}.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-item > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-item > a .tdb-sub-menu-icon-svg svg *,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-ancestor > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-menu-ancestor > a .tdb-sub-menu-icon-svg svg *,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-category-ancestor > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.current-category-ancestor > a .tdb-sub-menu-icon-svg svg *,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.tdb-hover > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu ul .tdb-normal-menu.tdb-hover > a .tdb-sub-menu-icon-svg svg *,
				.tdi_42 .tdb-menu ul .tdb-normal-menu:hover > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu ul .tdb-normal-menu:hover > a .tdb-sub-menu-icon-svg svg *,
				.tdi_42 .tdb-menu-items-dropdown .td-pulldown-filter-list li:hover > a .tdb-sub-menu-icon-svg svg,
				.tdi_42 .tdb-menu-items-dropdown .td-pulldown-filter-list li:hover > a .tdb-sub-menu-icon-svg svg *{
					fill: #0071ce;
				}
</style><div id=tdi_42 class="td_block_inner td-fix-index"><div class="tdb-main-sub-icon-fake"><i class="tdb-sub-menu-icon td-icon-down tdb-main-sub-menu-icon"></i></div><div class="tdb-sub-icon-fake"><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></div><ul id="menu-products-3" class="tdb-block-menu tdb-menu tdb-menu-items-visible"><li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-first tdb-menu-item-button tdb-menu-item tdb-normal-menu menu-item-55698 tdb-menu-item-inactive"><a href="https://www.devart.com/products.html" target="_blank"><div class="tdb-menu-item-text">Products</div><i class="tdb-sub-menu-icon td-icon-down tdb-main-sub-menu-icon"></i></a>
<ul class="sub-menu">
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55702 tdb-menu-item-inactive"><a href="https://www.devart.com/dbforge/" target="_blank"><div class="tdb-menu-item-text">DATABASE TOOLS</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55706 tdb-menu-item-inactive"><a href="https://www.devart.com/dbforge/sql/" target="_blank"><div class="tdb-menu-item-text">SQL Server Tools</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62900"><a href="https://www.devart.com/dbforge/sql/sqlcomplete/" target="_blank"><div class="tdb-menu-item-text">dbForge SQL Complete</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62903"><a href="https://www.devart.com/dbforge/sql/studio/" target="_blank"><div class="tdb-menu-item-text">dbForge Studio for SQL Server</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62906"><a href="https://www.devart.com/dbforge/sql/sql-tools/" target="_blank"><div class="tdb-menu-item-text">dbForge SQL Tools</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62918"><a href="https://www.devart.com/products.html#database-tools&#038;sql-server" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55710 tdb-menu-item-inactive"><a href="https://www.devart.com/dbforge/mysql/" target="_blank"><div class="tdb-menu-item-text">MySQL Tools</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62909"><a href="https://www.devart.com/dbforge/mysql/studio/" target="_blank"><div class="tdb-menu-item-text">dbForge Studio for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62912"><a href="https://www.devart.com/dbforge/mysql/compare-bundle/" target="_blank"><div class="tdb-menu-item-text">Compare Bundle for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62915"><a href="https://www.devart.com/dbforge/mysql/schemacompare/" target="_blank"><div class="tdb-menu-item-text">Schema Compare for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62921"><a href="https://www.devart.com/products.html#database-tools&#038;mysql" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55714 tdb-menu-item-inactive"><a href="https://www.devart.com/dbforge/oracle/" target="_blank"><div class="tdb-menu-item-text">Oracle Tools</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62924"><a href="https://www.devart.com/dbforge/oracle/studio/" target="_blank"><div class="tdb-menu-item-text">dbForge Studio for Oracle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62927"><a href="https://www.devart.com/dbforge/oracle/compare-bundle/" target="_blank"><div class="tdb-menu-item-text">Compare Bundle for Oracle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62930"><a href="https://www.devart.com/dbforge/oracle/datacompare/" target="_blank"><div class="tdb-menu-item-text">Data Compare for Oracle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62933"><a href="https://www.devart.com/products.html#database-tools&#038;oracle" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55718 tdb-menu-item-inactive"><a href="https://www.devart.com/dbforge/postgresql/" target="_blank"><div class="tdb-menu-item-text">PostgreSQL Tools</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62936"><a href="https://www.devart.com/dbforge/postgresql/studio/" target="_blank"><div class="tdb-menu-item-text">dbForge Studio for PostgreSQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62939"><a href="https://www.devart.com/dbforge/postgresql/datacompare/" target="_blank"><div class="tdb-menu-item-text">Data Compare for PostgreSQL</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-65690"><a href="https://www.devart.com/dbforge/edge/" target="_blank"><div class="tdb-menu-item-text">Multidatabase Solution</div></a></li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55722 tdb-menu-item-inactive"><a href="https://www.devart.com/data-connectivity/" target="_blank"><div class="tdb-menu-item-text">DATA CONNECTIVITY</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55726 tdb-menu-item-inactive"><a href="https://www.devart.com/dotconnect/" target="_blank"><div class="tdb-menu-item-text">ADO.NET Data Providers</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62966"><a href="https://www.devart.com/dotconnect/oracle/" target="_blank"><div class="tdb-menu-item-text">dotConnect for Oracle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62969"><a href="https://www.devart.com/dotconnect/postgresql/" target="_blank"><div class="tdb-menu-item-text">dotConnect for PostgreSQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62972"><a href="https://www.devart.com/dotconnect/mysql/" target="_blank"><div class="tdb-menu-item-text">dotConnect for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62975"><a href="https://www.devart.com/products.html#data-connectivity&#038;.net" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55730 tdb-menu-item-inactive"><a href="https://www.devart.com/odbc/" target="_blank"><div class="tdb-menu-item-text">ODBC Drivers</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62978"><a href="https://www.devart.com/odbc/salesforce/" target="_blank"><div class="tdb-menu-item-text">ODBC Driver for Salesforce</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62981"><a href="https://www.devart.com/odbc/oracle/" target="_blank"><div class="tdb-menu-item-text">ODBC Driver for Oracle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62984"><a href="https://www.devart.com/odbc/mysql/" target="_blank"><div class="tdb-menu-item-text">ODBC Driver for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62987"><a href="https://www.devart.com/products.html#data-connectivity&#038;odbc" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55734 tdb-menu-item-inactive"><a href="https://www.devart.com/ssis/" target="_blank"><div class="tdb-menu-item-text">SSIS Components</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63002"><a href="https://www.devart.com/ssis/salesforce/" target="_blank"><div class="tdb-menu-item-text">SSIS Components for Salesforce</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63005"><a href="https://www.devart.com/ssis/mysql/" target="_blank"><div class="tdb-menu-item-text">SSIS Components for MySQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63008"><a href="https://www.devart.com/ssis/database-bundle/" target="_blank"><div class="tdb-menu-item-text">SSIS Integration Database Bundle</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63011"><a href="https://www.devart.com/products.html#data-connectivity&#038;ssis" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55738 tdb-menu-item-inactive"><a href="https://www.devart.com/excel-addins/" target="_blank"><div class="tdb-menu-item-text">Excel Add-ins</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63014"><a href="https://www.devart.com/excel-addins/sqlserver/" target="_blank"><div class="tdb-menu-item-text">Excel Add-in for SQL Server</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63017"><a href="https://www.devart.com/excel-addins/postgresql/" target="_blank"><div class="tdb-menu-item-text">Excel Add-in for PostgreSQL</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63020"><a href="https://www.devart.com/excel-addins/database-pack/" target="_blank"><div class="tdb-menu-item-text">Excel Add-in Database Pack</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-63023"><a href="https://www.devart.com/products.html#data-connectivity&#038;excel" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55742 tdb-menu-item-inactive"><a href="https://www.devart.com/dac.html" target="_blank"><div class="tdb-menu-item-text">Delphi Data Components</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62990"><a href="https://www.devart.com/unidac/" target="_blank"><div class="tdb-menu-item-text">Universal Data Access Components</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62993"><a href="https://www.devart.com/odac/" target="_blank"><div class="tdb-menu-item-text">Oracle Data Access Components</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62996"><a href="https://www.devart.com/sdac/" target="_blank"><div class="tdb-menu-item-text">SQL Server Data Access Components</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62999"><a href="https://www.devart.com/products.html#data-connectivity&#038;delphi" target="_blank"><div class="tdb-menu-item-text">Others</div></a></li>
		</ul>
</li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55746 tdb-menu-item-inactive"><a><div class="tdb-menu-item-text">PRODUCTIVITY TOOLS</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55750 tdb-menu-item-inactive"><a href="https://www.devart.com/productivity-tools.html" target="_blank"><div class="tdb-menu-item-text">Coding Assistance Tools</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62942"><a href="https://www.devart.com/sbridge/" target="_blank"><div class="tdb-menu-item-text">SecureBridge</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62945"><a href="https://www.devart.com/codecompare/" target="_blank"><div class="tdb-menu-item-text">Code Compare</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62948"><a href="https://www.devart.com/review-assistant/" target="_blank"><div class="tdb-menu-item-text">Review Assistant</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62951"><a href="https://www.devart.com/code-review-bundle/" target="_blank"><div class="tdb-menu-item-text">Code Review Bundle</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55754 tdb-menu-item-inactive"><a href="https://www.devart.com/orm-solutions.html" target="_blank"><div class="tdb-menu-item-text">ORM Solutions</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
		<ul class="sub-menu">
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62954"><a href="https://www.devart.com/entitydeveloper/" target="_blank"><div class="tdb-menu-item-text">Entity Developer</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62957"><a href="https://www.devart.com/linqconnect/" target="_blank"><div class="tdb-menu-item-text">LinqConnect</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62960"><a href="https://www.devart.com/entitydac/" target="_blank"><div class="tdb-menu-item-text">EntityDAC</div></a></li>
			<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-62963"><a href="https://www.devart.com/linqinsight/" target="_blank"><div class="tdb-menu-item-text">LINQ Insight</div></a></li>
		</ul>
</li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55758"><a href="https://tmetric.com/" target="_blank"><div class="tdb-menu-item-text">Time Tracking App</div></a></li>
	</ul>
</li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item tdb-normal-menu menu-item-55762 tdb-menu-item-inactive"><a href="https://skyvia.com/" target="_blank"><div class="tdb-menu-item-text">DATA SERVICES</div><i class="tdb-sub-menu-icon td-icon-right-arrow"></i></a>
	<ul class="sub-menu">
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55766"><a href="https://skyvia.com/data-integration/" target="_blank"><div class="tdb-menu-item-text">Data Integration Services</div></a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55770"><a href="https://skyvia.com/backup/" target="_blank"><div class="tdb-menu-item-text">Cloud to Cloud Backup</div></a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55774"><a href="https://skyvia.com/query/" target="_blank"><div class="tdb-menu-item-text">Online SQL Tools</div></a></li>
		<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55778"><a href="https://skyvia.com/connect/" target="_blank"><div class="tdb-menu-item-text">Web API Server</div></a></li>
	</ul>
</li>
</ul>
</li>
<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item-button tdb-menu-item tdb-normal-menu menu-item-55782"><a href="https://www.devart.com/products.html" target="_blank"><div class="tdb-menu-item-text">Store</div></a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item-button tdb-menu-item tdb-normal-menu menu-item-55786"><a href="https://www.devart.com/support/" target="_blank"><div class="tdb-menu-item-text">Support</div></a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children tdb-menu-item-button tdb-menu-item tdb-normal-menu menu-item-55790 tdb-menu-item-inactive"><a><div class="tdb-menu-item-text">Company</div><i class="tdb-sub-menu-icon td-icon-down tdb-main-sub-menu-icon"></i></a>
<ul class="sub-menu">
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55794"><a href="https://www.devart.com/company/" target="_blank"><div class="tdb-menu-item-text">About us</div></a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55798"><a href="https://www.devart.com/company/customers.html" target="_blank"><div class="tdb-menu-item-text">Customers</div></a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55802"><a href="https://www.devart.com/company/partners.html" target="_blank"><div class="tdb-menu-item-text">Partners</div></a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55806"><a href="https://www.devart.com/company/resellers.html" target="_blank"><div class="tdb-menu-item-text">Resellers</div></a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55810"><a href="https://www.devart.com/company/contact.html" target="_blank"><div class="tdb-menu-item-text">Contacts</div></a></li>
	<li class="menu-item menu-item-type-custom menu-item-object-custom tdb-menu-item tdb-normal-menu menu-item-55814"><a href="https://www.devart.com/vacancies/" target="_blank"><div class="tdb-menu-item-text">Vacancies</div></a></li>
</ul>
</li>
</ul></div></div></div></div></div><div class="vc_column_inner tdi_46  wpb_column vc_column_container tdc-inner-column td-pb-span3">
<style scoped>

/* custom css */
.tdi_46{
                    vertical-align: baseline;
                }.tdi_46 .vc_column-inner > .wpb_wrapper,
				.tdi_46 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    display: block;
				}.tdi_46 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    width: 100%;
				}
</style><div class="vc_column-inner"><div class="wpb_wrapper" ><div class="td_block_wrap tdb_header_search tdi_47 tdb-header-search-trigger-enabled td-pb-border-top td_block_template_10 tdb-header-align"  data-td-block-uid="tdi_47" >
<style>

/* inline tdc_css att */

/* portrait */
@media (min-width: 768px) and (max-width: 1018px)
{
.tdi_47{
margin-top:1px !important;
}
}

</style>
<style>
/* custom css */
.tdb_module_header{
                  width: 100%;
                  padding-bottom: 0;
                }.tdb_module_header .td-module-container{
                  display: flex;
                  flex-direction: column;
                  position: relative;
                }.tdb_module_header .td-module-container:before{
                  content: '';
                  position: absolute;
                  bottom: 0;
                  left: 0;
                  width: 100%;
                  height: 1px;
                }.tdb_module_header .td-image-wrap{
                  display: block;
                  position: relative;
                  padding-bottom: 70%;
                }.tdb_module_header .td-image-container{
                  position: relative;
                  width: 100%;
                  flex: 0 0 auto;
                }.tdb_module_header .td-module-thumb{
                  margin-bottom: 0;
                }.tdb_module_header .td-module-meta-info{
                  width: 100%;
                  margin-bottom: 0;
                  padding: 7px 0 0 0;
                  z-index: 1;
                  border: 0 solid #eaeaea;
                  min-height: 0;
                }.tdb_module_header .entry-title{
                  margin: 0;
                  font-size: 13px;
                  font-weight: 500;
                  line-height: 18px;
                }.tdb_module_header .td-post-author-name,
                .tdb_module_header .td-post-date,
                .tdb_module_header .td-module-comments{
                  vertical-align: text-top;
                }.tdb_module_header .td-post-author-name,
                .tdb_module_header .td-post-date{
                  top: 3px;
                }.tdb_module_header .td-thumb-css{
                  width: 100%;
                  height: 100%;
                  position: absolute;
                  background-size: cover;
                  background-position: center center;
                }.tdb_module_header .td-category-pos-image .td-post-category:not(.td-post-extra-category),
                .tdb_module_header .td-post-vid-time{
                  position: absolute;
                  z-index: 2;
                  bottom: 0;
                }.tdb_module_header .td-category-pos-image .td-post-category:not(.td-post-extra-category){
                  left: 0;
                }.tdb_module_header .td-post-vid-time{
                  right: 0;
                  background-color: #000;
                  padding: 3px 6px 4px;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                  font-size: 10px;
                  font-weight: 600;
                  line-height: 1;
                  color: #fff;
                }.tdb_module_header .td-excerpt{
                  margin: 20px 0 0;
                  line-height: 21px;
                }.tdb_module_header .td-read-more{
                  margin: 20px 0 0;
                }.tdb_module_search .tdb-author-photo{
                  display: inline-block;
                }.tdb_module_search .tdb-author-photo,
                .tdb_module_search .tdb-author-photo img{
                  vertical-align: middle;
                }.tdb_module_search .td-post-author-name{
                  white-space: normal;
                }.tdb_header_search{
                  margin-bottom: 0;
                  clear: none;
                }.tdb_header_search .tdb-block-inner{
                  position: relative;
                  display: inline-block;
                  width: 100%;
                }.tdb_header_search .tdb-search-form{
                  position: relative;
                  padding: 20px;
                  border-width: 3px 0 0;
                  border-style: solid;
                  border-color: #4db2ec;
                  pointer-events: auto;
                }.tdb_header_search .tdb-search-form:before{
                  content: '';
                  position: absolute;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  background-color: #fff;
                }.tdb_header_search .tdb-search-form-inner{
                  position: relative;
                  display: flex;
                  background-color: #fff;
                }.tdb_header_search .tdb-search-form-inner:after{
                  content: '';
                  position: absolute;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  border: 1px solid #e1e1e1;
                  pointer-events: none;
                }.tdb_header_search .tdb-head-search-placeholder{
                  position: absolute;
                  top: 50%;
                  transform: translateY(-50%);
                  padding: 3px 9px;
                  font-size: 12px;
                  line-height: 21px;
                  color: #999;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                  pointer-events: none;
                }.tdb_header_search .tdb-head-search-form-input:focus + .tdb-head-search-placeholder,
                .tdb-head-search-form-input:not(:placeholder-shown) ~ .tdb-head-search-placeholder{
                  opacity: 0;
                }.tdb_header_search .tdb-head-search-form-btn,
                .tdb_header_search .tdb-head-search-form-input{
                  height: auto;
                  min-height: 32px;
                }.tdb_header_search .tdb-head-search-form-input{
                  color: #444;
                  flex: 1;
                  background-color: transparent;
                  border: 0;
                }.tdb_header_search .tdb-head-search-form-input.tdb-head-search-nofocus{
                  color: transparent;
                  text-shadow: 0 0 0 #444;
                }.tdb_header_search .tdb-head-search-form-btn{
                  margin-bottom: 0;
                  padding: 0 15px;
                  background-color: #222222;
                  font-family: 'Roboto', sans-serif;
                  font-size: 13px;
                  font-weight: 500;
                  color: #fff;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                  z-index: 1;
                }.tdb_header_search .tdb-head-search-form-btn:hover{
                  background-color: #4db2ec;
                }.tdb_header_search .tdb-head-search-form-btn i,
                .tdb_header_search .tdb-head-search-form-btn span{
                  display: inline-block;
                  vertical-align: middle;
                }.tdb_header_search .tdb-head-search-form-btn i{
                  font-size: 12px;
                }.tdb_header_search .tdb-head-search-form-btn .tdb-head-search-form-btn-icon{
                  position: relative;
                }.tdb_header_search .tdb-head-search-form-btn .tdb-head-search-form-btn-icon-svg{
                  line-height: 0;
                }.tdb_header_search .tdb-head-search-form-btn svg{
                  width: 12px;
                  height: auto;
                }.tdb_header_search .tdb-head-search-form-btn svg,
                .tdb_header_search .tdb-head-search-form-btn svg *{
                  fill: #fff;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                }.tdb_header_search .tdb-aj-search-results{
                  padding: 20px;
                  background-color: rgba(144, 144, 144, 0.02);
                  border-width: 1px 0;
                  border-style: solid;
                  border-color: #ededed;
                  background-color: #fff;
                }.tdb_header_search .tdb-aj-search-results .td_module_wrap:last-child{
                  margin-bottom: 0;
                  padding-bottom: 0;
                }.tdb_header_search .tdb-aj-search-results .td_module_wrap:last-child .td-module-container:before{
                  display: none;
                }.tdb_header_search .tdb-aj-search-inner{
                  display: flex;
                  flex-wrap: wrap;
                  *zoom: 1;
                }.tdb_header_search .tdb-aj-search-inner:before,
                .tdb_header_search .tdb-aj-search-inner:after{
                  display: table;
                  content: '';
                  line-height: 0;
                }.tdb_header_search .tdb-aj-search-inner:after{
                  clear: both;
                }.tdb_header_search .result-msg{
                  padding: 4px 0 6px 0;
                  font-family: 'Roboto', sans-serif;
                  font-size: 12px;
                  font-style: italic;
                  background-color: #fff;
                }.tdb_header_search .result-msg a{
                  color: #222;
                }.tdb_header_search .result-msg a:hover{
                  color: #4db2ec;
                }.tdb_header_search .td-module-meta-info,
                .tdb_header_search .td-next-prev-wrap{
                  text-align: left;
                }.tdb_header_search .td_module_wrap:hover .entry-title a{
                  color: #4db2ec;
                }.tdb_header_search .tdb-aj-cur-element .entry-title a{
                  color: #4db2ec;
                }.tdc-dragged .tdb-head-search-btn:after,
                .tdc-dragged .tdb-drop-down-search{
                  visibility: hidden !important;
                  opacity: 0 !important;
                  -webkit-transition: all 0.3s ease;
                  transition: all 0.3s ease;
                }.tdb-header-search-trigger-enabled{
                  z-index: 1000;
                }.tdb-header-search-trigger-enabled .tdb-head-search-btn{
                  display: flex;
                  align-items: center;
                  position: relative;
                  text-align: center;
                  color: #4db2ec;
                }.tdb-header-search-trigger-enabled .tdb-head-search-btn:after{
                  visibility: hidden;
                  opacity: 0;
                  content: '';
                  display: block;
                  position: absolute;
                  bottom: 0;
                  left: 0;
                  right: 0;
                  margin: 0 auto;
                  width: 0;
                  height: 0;
                  border-style: solid;
                  border-width: 0 6.5px 7px 6.5px;
                  -webkit-transform: translate3d(0, 20px, 0);
                  transform: translate3d(0, 20px, 0);
                  -webkit-transition: all 0.4s ease;
                  transition: all 0.4s ease;
                  border-color: transparent transparent #4db2ec transparent;
                }.tdb-header-search-trigger-enabled .tdb-drop-down-search-open + .tdb-head-search-btn:after{
                  visibility: visible;
                  opacity: 1;
                  -webkit-transform: translate3d(0, 0, 0);
                  transform: translate3d(0, 0, 0);
                }.tdb-header-search-trigger-enabled .tdb-search-icon,
                .tdb-header-search-trigger-enabled .tdb-search-txt,
                .tdb-header-search-trigger-enabled .tdb-search-icon-svg svg *{
                  -webkit-transition: all 0.3s ease-in-out;
                  transition: all 0.3s ease-in-out;
                }.tdb-header-search-trigger-enabled .tdb-search-icon-svg{
                  display: flex;
                  align-items: center;
                  justify-content: center;
                }.tdb-header-search-trigger-enabled .tdb-search-icon-svg svg{
                  height: auto;
                }.tdb-header-search-trigger-enabled .tdb-search-icon-svg svg,
                .tdb-header-search-trigger-enabled .tdb-search-icon-svg svg *{
                  fill: #4db2ec;
                }.tdb-header-search-trigger-enabled .tdb-search-txt{
                  position: relative;
                  line-height: 1;
                }.tdb-header-search-trigger-enabled .tdb-drop-down-search{
                  visibility: hidden;
                  opacity: 0;
                  position: absolute;
                  top: 100%;
                  left: 0;
                  -webkit-transform: translate3d(0, 20px, 0);
                  transform: translate3d(0, 20px, 0);
                  -webkit-transition: all 0.4s ease;
                  transition: all 0.4s ease;
                  pointer-events: none;
                  z-index: 10;
                }.tdb-header-search-trigger-enabled .tdb-drop-down-search-open{
                  visibility: visible;
                  opacity: 1;
                  -webkit-transform: translate3d(0, 0, 0);
                  transform: translate3d(0, 0, 0);
                }.tdb-header-search-trigger-enabled .tdb-drop-down-search-inner{
                  position: relative;
                  max-width: 300px;
                  pointer-events: all;
                }.rtl .tdb-header-search-trigger-enabled .tdb-drop-down-search-inner{
                  margin-left: 0;
                  margin-right: auto;
                }.tdb_header_search .tdb-aj-srs-title{
                    margin-bottom: 10px;
                    font-family: 'Roboto', sans-serif;
                    font-weight: 500;
                    font-size: 13px;
                    line-height: 1.3;
                    color: #888;
                }.tdb_header_search .tdb-aj-sr-taxonomies{
                    display: flex;
                    flex-direction: column;
                }.tdb_header_search .tdb-aj-sr-taxonomy{
                    font-family: 'Roboto', sans-serif;
                    font-size: 13px;
                    font-weight: 500;
                    line-height: 18px;
                    color: #111;
                }.tdb_header_search .tdb-aj-sr-taxonomy:not(:last-child){
                    margin-bottom: 5px;
                }.tdb_header_search .tdb-aj-sr-taxonomy:hover{
                    color: #4db2ec;
                }.tdi_47 .tdb-head-search-btn i{
                    font-size: 20px;
                
                    width: 48px;
					height: 48px;
					line-height:  48px;
                
                    color: #000000;
                }.tdi_47 .tdb-head-search-btn svg{
                    width: 20px;
                }.tdi_47 .tdb-search-icon-svg{
                    width: 48px;
					height: 48px;
                }.tdi_47{
                    display: inline-block;
                
                    float: right;
                    clear: none;
                }.tdi_47 .tdb-search-txt{
                    top: 0px;
                }.tdi_47 .tdb-drop-down-search .tdb-drop-down-search-inner{
                    max-width: 600px;
                }.tdi_47 .tdb-search-form{
                    padding: 30px;
                
                    border-width: 0px;
                }.tdi_47 .tdb-drop-down-search{
                    left: auto;
                    right: 0;
                }body .tdi_47 .tdb-drop-down-search-inner,
                .tdi_47 .tdb-search-form,
                .tdi_47 .tdb-aj-search{
                    margin-left: auto;
                    margin-right: 0;
                }.tdi_47 .tdb-search-form-inner:after{
                    border-width: 0 0 1px 0;
                }.tdi_47 .tdb-head-search-form-btn i{
                    font-size: 7px;
                }.tdi_47 .tdb-head-search-form-btn-icon{
                    margin-left: 8px;
                
                    top: 0px;
                }.tdi_47 .tdb-head-search-form-btn{
                    padding: 0px;
                
                    color: #000000;
                
                    background-color: rgba(0,0,0,0);
                }.tdi_47 .tdb-aj-search-results{
                    padding: 0 30px 30px;
                
                    border-width: 0 0 1px 0;
                }.tdi_47 .result-msg{
                    padding: 10px 0;
                
                    text-align: center;
                
                    font-style:normal !important;
                }.tdi_47 .tdb-head-search-btn svg,
                .tdi_47 .tdb-head-search-btn svg *{
                    fill: #000000;
                }.tdi_47 .tdb-head-search-btn:after{
                    border-bottom-color: #ffffff;
                }.tdi_47 .tdb-drop-down-search-inner{
                    box-shadow:  0px 3px 6px 0px rgba(0, 0, 0, 0.2);
                }.tdi_47 .tdb-head-search-form-btn svg,
                .tdi_47 .tdb-head-search-form-btn svg *{
                    fill: #000000;
                }.tdi_47 .tdb-head-search-form-btn:hover{
                    color: #0071ce;
                
                    background-color: rgba(0,0,0,0);
                }.tdi_47 .tdb-head-search-form-btn:hover svg,
                .tdi_47 .tdb-head-search-form-btn:hover svg *{
                    fill: #0071ce;
                }.tdi_47 .result-msg a:hover{
                    color: #0071ce;
                }.tdi_47 .td_module_wrap{
					width: 50%;
					float: left;
				
					padding-left: 10px;
					padding-right: 10px;
				
					padding-bottom: 10px;
					margin-bottom: 10px;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2){
					margin-bottom: 0;
					padding-bottom: 0;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2) .td-module-container:before{
					display: none;
				}.tdi_47 .tdb-aj-search-inner{
					margin-left: -10px;
					margin-right: -10px;
				}.tdi_47 .td-module-container:before{
					bottom: -10px;
				}.tdi_47 .entry-thumb{
					background-position: center 50%;
				}.tdi_47 .td-image-wrap{
					padding-bottom: 100%;
				}.tdi_47 .td-image-container{
				 	flex: 0 0 30%;
				 	width: 30%;
			    
                	display: block; order: 0;
                }.ie10 .tdi_47 .td-image-container,
				.ie11 .tdi_47 .td-image-container{
				 	flex: 0 0 auto;
			    }.tdi_47 .td-module-container{
					flex-direction: row;
				}.ie10 .tdi_47 .td-module-meta-info,
				.ie11 .tdi_47 .td-module-meta-info{
				 	flex: 1;
			    }.tdi_47 .td-video-play-ico{
					width: 24px;
					height: 24px;
					font-size: 24px;
				}.tdi_47 .td-post-vid-time{
					display: block;
				}.tdi_47 .td-module-meta-info{
					padding: 3px 0 0 16px;
				
					border-color: #eaeaea;
				}.tdi_47 .entry-title{
					margin: 0 0 2px 0;
				
					font-size:13px !important;line-height:1.4 !important;
				}.tdi_47 .td-excerpt{
					column-count: 1;
				
					column-gap: 48px;
				
					display: none;
				}.tdi_47 .td-post-category:not(.td-post-extra-category){
					display: none;
				}.tdi_47 .td-read-more{
					display: none;
				}.tdi_47 .td-author-date{
					display: inline;
				}.tdi_47 .td-post-author-name{
					display: none;
				}.tdi_47 .td-icon-star,
                .tdi_47 .td-icon-star-empty,
                .tdi_47 .td-icon-star-half{
					font-size: 15px;
				}.tdi_47 .td-module-comments{
					display: none;
				}.tdi_47 .tdb-author-photo .avatar{
				    width: 20px;
				    height: 20px;
				
				    margin-right: 6px;
				
				    border-radius: 50%;
				}body .tdi_47 .td_module_wrap:hover .td-module-title a,
				.tdi_47 .tdb-aj-cur-element .entry-title a{
					color: #0071ce !important;
				}.tdi_47 .td-post-category{
					text-transform:uppercase !important;
				}

/* landscape */
@media (min-width: 1019px) and (max-width: 1140px){
.tdi_47 .td_module_wrap{
					padding-bottom: 10px !important;
					margin-bottom: 10px !important;
				
					padding-bottom: 10px;
					margin-bottom: 10px;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2){
					margin-bottom: 0 !important;
					padding-bottom: 0 !important;
				}.tdi_47 .td_module_wrap .td-module-container:before{
					display: block !important;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2) .td-module-container:before{
					display: none !important;
				}.tdi_47 .td-module-container:before{
					bottom: -10px;
				}
}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px){
.tdi_47 .tdb-head-search-btn i{
                    font-size: 18px;
                
                    width: 46.8px;
					height: 46.8px;
					line-height:  46.8px;
                }.tdi_47 .tdb-head-search-btn svg{
                    width: 18px;
                }.tdi_47 .tdb-search-icon-svg{
                    width: 46.8px;
					height: 46.8px;
                }.tdi_47 .tdb-search-form{
                    padding: 20px 20px 20px;
                }.tdi_47 .td_module_wrap{
					padding-bottom: 10px !important;
					margin-bottom: 10px !important;
				
					padding-bottom: 10px;
					margin-bottom: 10px;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2){
					margin-bottom: 0 !important;
					padding-bottom: 0 !important;
				}.tdi_47 .td_module_wrap .td-module-container:before{
					display: block !important;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2) .td-module-container:before{
					display: none !important;
				}.tdi_47 .td-module-container:before{
					bottom: -10px;
				}
}

/* phone */
@media (max-width: 767px){
.tdi_47 .td_module_wrap{
					padding-bottom: 10px !important;
					margin-bottom: 10px !important;
				
					padding-bottom: 10px;
					margin-bottom: 10px;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2){
					margin-bottom: 0 !important;
					padding-bottom: 0 !important;
				}.tdi_47 .td_module_wrap .td-module-container:before{
					display: block !important;
				}.tdi_47 .td_module_wrap:nth-last-child(-n+2) .td-module-container:before{
					display: none !important;
				}.tdi_47 .td-module-container:before{
					bottom: -10px;
				}
}
</style><div class="tdb-block-inner td-fix-index"><div class="tdb-drop-down-search" aria-labelledby="td-header-search-button"><div class="tdb-drop-down-search-inner"><form method="get" class="tdb-search-form" action="https://blog.devart.com/"><div class="tdb-search-form-inner"><input class="tdb-head-search-form-input" placeholder=" " type="text" value="" name="s" autocomplete="off" /><button class="wpb_button wpb_btn-inverse btn tdb-head-search-form-btn" type="submit"><span>Search</span><i class="tdb-head-search-form-btn-icon td-icon-menu-right"></i></button></div></form><div class="tdb-aj-search"></div></div></div><a href="#" role="button" aria-label="Search" class="tdb-head-search-btn dropdown-toggle" data-toggle="dropdown"><span class="tdb-search-icon tdb-search-icon-svg" ><svg version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024"><path d="M946.371 843.601l-125.379-125.44c43.643-65.925 65.495-142.1 65.475-218.040 0.051-101.069-38.676-202.588-115.835-279.706-77.117-77.148-178.606-115.948-279.644-115.886-101.079-0.061-202.557 38.738-279.665 115.876-77.169 77.128-115.937 178.627-115.907 279.716-0.031 101.069 38.728 202.588 115.907 279.665 77.117 77.117 178.616 115.825 279.665 115.804 75.94 0.020 152.136-21.862 218.061-65.495l125.348 125.46c30.915 30.904 81.029 30.904 111.954 0.020 30.915-30.935 30.915-81.029 0.020-111.974zM705.772 714.925c-59.443 59.341-136.899 88.842-214.784 88.924-77.896-0.082-155.341-29.583-214.784-88.924-59.443-59.484-88.975-136.919-89.037-214.804 0.061-77.885 29.604-155.372 89.037-214.825 59.464-59.443 136.878-88.945 214.784-89.016 77.865 0.082 155.3 29.583 214.784 89.016 59.361 59.464 88.914 136.919 88.945 214.825-0.041 77.885-29.583 155.361-88.945 214.804z"></path></svg></span></a></div></div> <!-- ./block --></div></div></div></div><div class="vc_row_inner tdi_49  vc_row vc_inner wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_49{
                    position: relative !important;
                    top: 0;
                    transform: none;
                    -webkit-transform: none;
                }.tdi_49,
				.tdi_49 .tdc-inner-columns{
				    display: block;
				}.tdi_49 .tdc-inner-columns{
				    width: 100%;
				}
</style><div class="vc_column_inner tdi_51  wpb_column vc_column_container tdc-inner-column td-pb-span12 td-is-sticky">
<style scoped>

/* custom css */
.tdi_51{
                    vertical-align: baseline;
                }.tdi_51 .vc_column-inner > .wpb_wrapper,
				.tdi_51 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    display: block;
				}.tdi_51 .vc_column-inner > .wpb_wrapper .tdc-elements{
				    width: 100%;
				}
</style><div class="vc_column-inner"><div class="wpb_wrapper" data-sticky-offset="20"></div></div></div></div></div></div></div></div></div></div>                </div>
                                <div class="td-header-desktop-sticky-wrap tdc-zone-sticky-invisible tdc-zone-sticky-inactive" style="display: none">
                    <div id="tdi_52" class="tdc-zone"><div class="tdc_zone tdi_53  wpb_row td-pb-row" data-sticky-offset="0" >
<style scoped>

/* custom css */
.tdi_53{
                    min-height: 0;
                }.td-header-desktop-sticky-wrap.td-header-active{
                    opacity: 1;
                }
</style><div id="tdi_54" class="tdc-row"><div class="vc_row tdi_55  wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_55,
                .tdi_55 .tdc-columns{
                    min-height: 0;
                }.tdi_55,
				.tdi_55 .tdc-columns{
				    display: block;
				}.tdi_55 .tdc-columns{
				    width: 100%;
				}
</style><div class="vc_column tdi_57  wpb_column vc_column_container tdc-column td-pb-span12">
<style scoped>

/* custom css */
.tdi_57{
                    vertical-align: baseline;
                }.tdi_57 > .wpb_wrapper,
				.tdi_57 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_57 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_57 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_57 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}
</style><div class="wpb_wrapper" ></div></div></div></div></div></div>                </div>
            </div>
                <div id="tdb-autoload-article" data-autoload="off" data-autoload-org-post-id="30364" data-autoload-type="" data-autoload-count="5" >
    <style>
        .tdb-autoload-wrap {
            position: relative;
        }
        .tdb-autoload-wrap .tdb-loader-autoload {
            top: auto !important;
            bottom: 50px !important;
        }
        .tdb-autoload-debug {
            display: none;
            width: 1068px;
            margin-right: auto;
            margin-left: auto;
        }
        @media (min-width: 1019px) and (max-width: 1018px) {
            .tdb-autoload-debug {
                width: 740px;
            }
        }
        @media (max-width: 767px) {
            .tdb-autoload-debug {
                display: none;
                width: 100%;
                padding-left: 20px;
                padding-right: 20px;
            }
        }
    </style>

        <div class="td-main-content-wrap td-container-wrap">
            <div class="tdc-content-wrap">
                <article id="template-id-55874"
                    class="post-55874 tdb_templates type-tdb_templates status-publish post"                    itemscope itemtype="https://schema.org/Article"                                                                            >
	                                    <div id="tdi_58" class="tdc-zone"><div class="tdc_zone tdi_59  wpb_row td-pb-row"  >
<style scoped>

/* custom css */
.tdi_59{
                    min-height: 0;
                }
</style><div id="tdi_60" class="tdc-row stretch_row_1200 td-stretch-content"><div class="vc_row tdi_61  wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_61,
                .tdi_61 .tdc-columns{
                    min-height: 0;
                }.tdi_61,
				.tdi_61 .tdc-columns{
				    display: block;
				}.tdi_61 .tdc-columns{
				    width: 100%;
				}
/* inline tdc_css att */

.tdi_61{
padding-top:22px !important;
}

.tdi_61 .td_block_wrap{ text-align:left }

</style><div class="vc_column tdi_63  wpb_column vc_column_container tdc-column td-pb-span12">
<style scoped>

/* custom css */
.tdi_63{
                    vertical-align: baseline;
                }.tdi_63 > .wpb_wrapper,
				.tdi_63 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_63 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_63 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_63 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}
</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_breadcrumbs tdi_64 td-pb-border-top td_block_template_10 tdb-breadcrumbs "  data-td-block-uid="tdi_64" >
<style>
/* custom css */
.tdb-breadcrumbs{
                  margin-bottom: 11px;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                  font-size: 12px;
                  color: #747474;
                  line-height: 18px;
                }.tdb-breadcrumbs a{
                  color: #747474;
                }.tdb-breadcrumbs a:hover{
                  color: #000;
                }.tdb-breadcrumbs .tdb-bread-sep{
                  line-height: 1;
                  vertical-align: middle;
                }.tdb-breadcrumbs .tdb-bread-sep-svg svg{
                  height: auto;
                }.tdb-breadcrumbs .tdb-bread-sep-svg svg,
                .tdb-breadcrumbs .tdb-bread-sep-svg svg *{
                  fill: #c3c3c3;
                }.single-tdb_templates.author-template .tdb_breadcrumbs{
                  margin-bottom: 2px;
                }.tdb_category_breadcrumbs{
                  margin: 21px 0 9px;
                }.search-results .tdb_breadcrumbs{
                  margin-bottom: 2px;
                }.tdi_64 .tdb-bread-sep{
                    font-size: 8px;
                
                    margin: 0 5px;
                }.td-theme-wrap .tdi_64{
					text-align: left;
				}
</style><div class="tdb-block-inner td-fix-index"><span><a title="" class="tdb-entry-crumb" href="https://blog.devart.com/">Home</a></span><i class="tdb-bread-sep td-icon-right"></i><span><a title="View all posts in Products" class="tdb-entry-crumb" href="https://blog.devart.com/category/products">Products</a></span><i class="tdb-bread-sep td-icon-right"></i><span><a title="View all posts in Productivity Tools" class="tdb-entry-crumb" href="https://blog.devart.com/category/products/productivity-tools">Productivity Tools</a></span><i class="tdb-bread-sep tdb-bred-no-url-last td-icon-right"></i><span class="tdb-bred-no-url-last">SQL Query Optimization: How to Tune Performance of SQL Queries</span></div></div><script type="application/ld+json">
                        {
                            "@context": "http://schema.org",
                            "@type": "BreadcrumbList",
                            "itemListElement": [{
                            "@type": "ListItem",
                            "position": 1,
                                "item": {
                                "@type": "WebSite",
                                "@id": "https://blog.devart.com/",
                                "name": "Home"                                               
                            }
                        },{
                            "@type": "ListItem",
                            "position": 2,
                                "item": {
                                "@type": "WebPage",
                                "@id": "https://blog.devart.com/category/products",
                                "name": "Products"
                            }
                        },{
                            "@type": "ListItem",
                            "position": 3,
                                "item": {
                                "@type": "WebPage",
                                "@id": "https://blog.devart.com/category/products/productivity-tools",
                                "name": "Productivity Tools"                                
                            }
                        },{
                            "@type": "ListItem",
                            "position": 4,
                                "item": {
                                "@type": "WebPage",
                                "@id": "",
                                "name": "SQL Query Optimization: How to Tune Performance of SQL Queries"                                
                            }
                        }    ]
                        }
                       </script></div></div></div></div><div id="tdi_65" class="tdc-row stretch_row_1200 td-stretch-content"><div class="vc_row tdi_66 td-ss-row wpb_row td-pb-row" >
<style scoped>

/* custom css */
.tdi_66,
                .tdi_66 .tdc-columns{
                    min-height: 0;
                }.tdi_66,
				.tdi_66 .tdc-columns{
				    display: block;
				}.tdi_66 .tdc-columns{
				    width: 100%;
				}
</style><div class="vc_column tdi_68  wpb_column vc_column_container tdc-column td-pb-span8">
<style scoped>

/* custom css */
.tdi_68{
                    vertical-align: baseline;
                }.tdi_68 > .wpb_wrapper,
				.tdi_68 > .wpb_wrapper > .tdc-elements{
				    display: block;
				}.tdi_68 > .wpb_wrapper > .tdc-elements{
				    width: 100%;
				}.tdi_68 > .wpb_wrapper > .vc_row_inner{
				    width: auto;
				}.tdi_68 > .wpb_wrapper{
				    width: auto;
				    height: auto;
				}div.tdi_68{
				    width: 72.6% !important;
				}

/* phone */
@media (max-width: 767px){
div.tdi_68{
				    width: 100% !important;
				}
}
</style><div class="wpb_wrapper" ><div class="td_block_wrap tdb_single_categories tdi_69 td-pb-border-top td_block_template_10 "   data-td-block-uid="tdi_69" >
<style>
/* custom css */
.tdb_single_categories{
                  margin: 0 0 10px 0;
                  line-height: 1;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                }.tdb_single_categories a{
                  pointer-events: auto;
                  font-size: 10px;
                  display: inline-block;
                  margin: 0 5px 5px 0;
                  line-height: 1;
                  color: #fff;
                  padding: 3px 6px 4px 6px;
                  white-space: nowrap;
                  position: relative;
                  vertical-align: middle;
                }.tdb_single_categories a:hover .tdb-cat-bg{
                  opacity: 0.9;
                }.tdb_single_categories a:hover .tdb-cat-bg:before{
                  opacity: 1;
                }.tdb-category i:last-of-type{
                  display: none;
                }.tdb-cat-text{
                  display: inline-block;
                  vertical-align: middle;
                  margin-right: 10px;
                }.tdb-cat-sep{
                  font-size: 14px;
                  vertical-align: middle;
                  position: relative;
                }.tdb-cat-sep-svg{
                  line-height: 0;
                }.tdb-cat-sep-svg svg{
                  width: 14px;
                  height: auto;
                }.tdb-cat-bg{
                  position: absolute;
                  background-color: #222;
                  border: 1px solid #222;
                  width: 100%;
                  height: 100%;
                  top: 0;
                  left: 0;
                  z-index: -1;
                }.tdb-cat-bg:before{
                  content: '';
                  width: 100%;
                  height: 100%;
                  left: 0;
                  top: 0;
                  position: absolute;
                  z-index: -1;
                  opacity: 0;
                  -webkit-transition: opacity 0.3s ease;
                  transition: opacity 0.3s ease;
                }.tdb-cat-style2 .tdb-cat-bg{
                  background-color: rgba(34, 34, 34, 0.85);
                }.tdi_69 .tdb-cat-bg{
					border-width: 1px;
				}.tdi_69 .tdb-cat-sep{
					font-size: 14px;
				}.tdi_69 .tdb-cat-text{
					margin-right: 10px;
				}.td-theme-wrap .tdi_69{
					text-align: left;
				}
</style><div class="tdb-category td-fix-index"><a class="tdb-entry-category" href="https://blog.devart.com/category/products" ><span class="tdb-cat-bg"></span>Products</a><a class="tdb-entry-category" href="https://blog.devart.com/category/products/productivity-tools" ><span class="tdb-cat-bg"></span>Productivity Tools</a><a class="tdb-entry-category" href="https://blog.devart.com/category/products/sql-server-tools" ><span class="tdb-cat-bg"></span>SQL Server Tools</a></div></div><div class="td_block_wrap tdb_title tdi_70 tdb-single-title td-pb-border-top td_block_template_10"  data-td-block-uid="tdi_70" >
<style>
/* custom css */
.tdb_title{
                  margin-bottom: 19px;
                }.tdb_title.tdb-content-horiz-center{
                  text-align: center;
                }.tdb_title.tdb-content-horiz-center .tdb-title-line{
                  margin: 0 auto;
                }.tdb_title.tdb-content-horiz-right{
                  text-align: right;
                }.tdb_title.tdb-content-horiz-right .tdb-title-line{
                  margin-left: auto;
                  margin-right: 0;
                }.tdb-title-text{
                  display: inline-block;
                  position: relative;
                  margin: 0;
                  word-wrap: break-word;
                  font-size: 30px;
                  line-height: 38px;
                  font-weight: 700;
                }.tdb-first-letter{
                  position: absolute;
                  -webkit-user-select: none;
                  user-select: none;
                  pointer-events: none;
                  text-transform: uppercase;
                  color: rgba(0, 0, 0, 0.08);
                  font-size: 6em;
                  font-weight: 300;
                  top: 50%;
                  -webkit-transform: translateY(-50%);
                  transform: translateY(-50%);
                  left: -0.36em;
                  z-index: -1;
                  -webkit-text-fill-color: initial;
                }.tdb-title-line{
                  display: none;
                  position: relative;
                }.tdb-title-line:after{
                  content: '';
                  width: 100%;
                  position: absolute;
                  background-color: #4db2ec;
                  top: 0;
                  left: 0;
                  margin: auto;
                }.tdb-single-title .tdb-title-text{
                  font-size: 41px;
                  line-height: 50px;
                  font-weight: 400;
                }.tdi_70 .tdb-title-text{
					color: #3d3d3d;
				
					font-family:Firasans Regular !important;font-size:38px !important;line-height:1.2 !important;
				}.tdi_70 .tdb-title-line:after{
					height: 2px;
				
					bottom: 40%;
				}.tdi_70 .tdb-title-line{
					height: 50px;
				}.td-theme-wrap .tdi_70{
					text-align: left;
				}.tdi_70 .tdb-first-letter{
					left: -0.36em;
					right: auto;
				}

/* portrait */
@media (min-width: 768px) and (max-width: 1018px){
.tdi_70 .tdb-title-text{
					font-family:Firasans Regular !important;font-size:32px !important;line-height:1.2 !important;
				}
}

/* phone */
@media (max-width: 767px){
.tdi_70 .tdb-title-text{
					font-family:Firasans Regular !important;font-size:30px !important;line-height:1.2 !important;
				}
}
</style><div class="tdb-block-inner td-fix-index"><h1 class="tdb-title-text">SQL Query Optimization: How to Tune Performance of SQL Queries</h1><div></div><div class="tdb-title-line"></div></div></div><div class="td_block_wrap tdb_single_author tdi_72 td-pb-border-top td_block_template_10 tdb-post-meta"  data-td-block-uid="tdi_72" >
<style>

/* inline tdc_css att */

.tdi_72{
margin-right:10px !important;
}

</style>
<style>
/* custom css */
.tdb-post-meta{
                  margin-bottom: 16px;
                  color: #444;
                  font-family: 'Open Sans', 'Open Sans Regular', sans-serif;
                  font-size: 11px;
                  font-weight: 400;
                  clear: none;
                  vertical-align: middle;
                  line-height: 1;
                }.tdb-post-meta span,
                .tdb-post-meta i,
                .tdb-post-meta time{
                  vertical-align: middle;
                }.tdb_single_author{
                  line-height: 30px;
                }.tdb_single_author a{
                  vertical-align: middle;
                }.tdb_single_author .tdb-block-inner{
                  display: flex;
                  align-items: center;
                }.tdb_single_author .tdb-author-name-wrap{
                  display: flex;
                }.tdb_single_author .tdb-author-name{
                  font-weight: 700;
                  margin-right: 3px;
                }.tdb_single_author .tdb-author-by{
                  margin-right: 3px;
                }.tdb_single_author .tdb-author-photo img{
                  display: block;
                }.tdi_72{
                    display: inline-block;
                }.tdi_72 .tdb-author-name-wrap{
                    align-items: baseline;
                }.tdi_72 .avatar{
                    width: 30px;
                    height: 30px;
                
                    margin-right: 6px;
                
                    border-radius: 50%;
                }.tdi_72 .tdb-author-name{
					color: #000;
				}
</style><div class="tdb-block-inner td-fix-index"><a class="tdb-author-photo"  href="https://blog.devart.com/author/dbforge" title="dbForge Team"><img alt='dbForge Team' src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%2096%2096'%3E%3C/svg%3E" data-lazy-srcset='https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png 2x' class='avatar avatar-96 photo' height='96' width='96' decoding='async' data-lazy-src="https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png"/><noscript><img alt='dbForge Team' src='https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png' srcset='https://blog.devart.com/wp-content/uploads/2023/02/avatar-dbforge-team.png 2x' class='avatar avatar-96 photo' height='96' width='96' decoding='async'/></noscript></a><div class="tdb-author-name-wrap"><span class="tdb-author-by">By</span> <a class="tdb-author-name" href="https://blog.devart.com/author/dbforge">dbForge Team</a></div></div></div><div class="td_block_wrap tdb_single_date tdi_73 td-pb-border-top td_block_template_10 tdb-post-meta"  data-td-block-uid="tdi_73" >
<style>
/* custom css */
.tdb_single_date{
                  line-height: 30px;
                }.tdb_single_date a{
                  vertical-align: middle;
                }.tdb_single_date .tdb-date-icon-svg{
                  position: relative;
                  line-height: 0;
                }.tdb_single_date svg{
                  height: auto;
                }.tdb_single_date svg,
                 .tdb_single_date svg *{
                  fill: #444;
                }.tdi_73{
                    display: inline-block;
                }.tdi_73 svg{
                    width: 14px;
                }.tdi_73 .tdb-date-icon{
                    margin-right: 5px;
                }
</style><div class="tdb-block-inner td-fix-index"><time class="entry-date updated td-module-date" datetime="2021-12-23T12:35:09+02:00">December 23, 2021</time></div></div> <!-- ./block --><div class="td_block_wrap tdb_single_comments_count tdi_74 td-pb-border-top td_block_template_10 tdb-post-meta"  data-td-block-uid="tdi_74" >
<style>
/* custom css */
.tdb_single_comments_count{
                  line-height: 30px;
                }.tdb_single_comments_count .tdb-comm-icon-svg{
                  position: relative;
                  line-height: 0;
                }.tdb_single_comments_count svg{
                  height: auto;
                }.tdb_single_comments_count svg,
                 .tdb_single_comments_count svg *{
                  fill: #444;
                }.tdi_74{
                    float: right;
                
                    display: inline-block;
                }.tdi_74 i{
                    font-size: 10px;
                }.tdi_74 .tdb-comm-icon{
                    margin-right: 5px;
                }.tdi_74 a{
					color: #444;
				}.tdi_74 a svg,
				.tdi_74 a svg *{
					fill: #444;
				}
</style><div class="tdb-block-inner td-fix-index"><a href="https://blog.devart.com/how-to-optimize-sql-query.html#respond"><i class="tdb-comm-icon td-icon-comments"></i><span class="tdb-add-text"></span><span>0</span></a></div></div><div class="td_block_wrap tdb_single_post_views tdi_75 td-pb-border-top td_block_template_10 tdb-post-meta"  data-td-block-uid="tdi_75" >
<style>

/* inline tdc_css att */

.tdi_75{
margin-right:22px !important;
}

</style>
<style>
/* custom css */
.tdb_single_post_views{
                  line-height: 30px;
                }.tdb_single_post_views a{
                  vertical-align: middle;
                }.tdb_single_post_views .tdb-views-icon-svg{
                  position: relative;
                  line-height: 0;
                }.tdb_single_post_views svg{
                  height: auto;
                }.tdb_single_post_views svg,
                 .tdb_single_post_views svg *{
                  fill: #444;
                }.tdi_75{
                    display: inline-block;
                
                    float: right;
                }.tdi_75 i{
                    font-size: 14px;
                }.tdi_75 .tdb-views-icon{
                    margin-right: 5px;
                }
</style><div class="tdb-block-inner td-fix-index"><i class="tdb-views-icon td-icon-views"></i><span class="tdb-add-text"></span><span class="td-nr-views-30364">122983</span></div></div><div class="td_block_wrap tdb_single_featured_image tdi_76 tdb-content-horiz-left td-pb-border-top td_block_template_10"  data-td-block-uid="tdi_76" >
<style>

/* inline tdc_css att */

/* phone */
@media (max-width: 767px)
{
.tdi_76{
margin-right:-20px !important;
margin-left:-20px !important;
}
}

</style>
<style>
/* custom css */
.tdb_single_featured_image{
                  margin-bottom: 26px;
                }.tdb_single_featured_image.tdb-sfi-stretch{
                  opacity: 0;
                }.tdb_single_featured_image.tdb-sfi-stretch,
                .tdb_single_featured_image .tdb-block-inner{
                  -webkit-transition: all 0.3s ease-in-out;
                  transition: all 0.3s ease-in-out;
                }.tdb_single_featured_image img{
                  display: block;
                  width: 100%;
                }.tdb_single_featured_image video{
                  max-width: 100%;
                }.tdb_single_featured_image .tdb-caption-text{
                  z-index: 1;
                  text-align: left;
                  font-size: 11px;
                  font-style: italic;
                  font-weight: normal;
                  line-height: 17px;
                  color: #444;
                }.tdb_single_featured_image.tdb-content-horiz-center .tdb-caption-text{
                  text-align: center;
                  left: 0;
                  right: 0;
                  margin-left: auto;
                  margin-right: auto;
                }.tdb_single_featured_image.tdb-content-horiz-right .tdb-caption-text{
                  text-align: right;
                  left:  auto;
                  right: 0;
                }.tdb-no-featured-img{
                  background-color: #f1f1f1;
                  width: 100%;
                  height: 500px;
                }.tdb-no-featured-audio{
                  height: 59px;
                }.tdi_76 .td-audio-player{
                    font-size: 12px;
                }.tdi_76 .tdb-caption-text{
                    margin: 6px 0 0;
                }.tdi_76:hover .tdb-block-inner:before{
                    opacity: 0;
                }
</style><div class="tdb-block-inner td-fix-index">
                                    <img 
                                        width="1068" 
                                        height="580" 
                                        class="entry-thumb" 
                                        src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201068%20580'%3E%3C/svg%3E" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg 1068w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-300x163.jpg 300w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-1024x556.jpg 1024w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-768x417.jpg 768w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-150x81.jpg 150w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-696x378.jpg 696w" data-lazy-sizes="(max-width: 1068px) 100vw, 1068px" 
                                        alt="" 
                                        title="How_to_Tune_Performance_1068x580"
                                    data-lazy-src="https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg" /><noscript><img 
                                        width="1068" 
                                        height="580" 
                                        class="entry-thumb" 
                                        src="https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg" srcset="https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580.jpg 1068w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-300x163.jpg 300w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-1024x556.jpg 1024w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-768x417.jpg 768w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-150x81.jpg 150w, https://blog.devart.com/wp-content/uploads/2021/12/How_to_Tune_Performance_1068x580-696x378.jpg 696w" sizes="(max-width: 1068px) 100vw, 1068px" 
                                        alt="" 
                                        title="How_to_Tune_Performance_1068x580"
                                    /></noscript>
                                    </div></div><div class="td_block_wrap tdb_single_content tdi_77 td-pb-border-top td_block_template_10 td-post-content tagdiv-type"  data-td-block-uid="tdi_77" >
<style>
/* custom css */
.tdb_single_content{
                  margin-bottom: 0;
                  *zoom: 1;
                }.tdb_single_content:before,
                .tdb_single_content:after{
                  display: table;
                  content: '';
                  line-height: 0;
                }.tdb_single_content:after{
                  clear: both;
                }.tdb_single_content .tdb-block-inner > *:not(.wp-block-quote):not(.alignwide):not(.alignfull.wp-block-cover.has-parallax):not(.td-a-ad){
                  margin-left: auto;
                  margin-right: auto;
                }.tdb_single_content a{
                  pointer-events: auto;
                }.tdb_single_content .td-spot-id-top_ad .tdc-placeholder-title:before{
                  content: 'Article Top Ad' !important;
                }.tdb_single_content .td-spot-id-inline_ad0 .tdc-placeholder-title:before{
                  content: 'Article Inline Ad 1' !important;
                }.tdb_single_content .td-spot-id-inline_ad1 .tdc-placeholder-title:before{
                  content: 'Article Inline Ad 2' !important;
                }.tdb_single_content .td-spot-id-inline_ad2 .tdc-placeholder-title:before{
                  content: 'Article Inline Ad 3' !important;
                }.tdb_single_content .td-spot-id-bottom_ad .tdc-placeholder-title:before{
                  content: 'Article Bottom Ad' !important;
                }.tdb_single_content .id_top_ad,
                .tdb_single_content .id_bottom_ad{
                  clear: both;
                  margin-bottom: 21px;
                  text-align: center;
                }.tdb_single_content .id_top_ad img,
                .tdb_single_content .id_bottom_ad img{
                  margin-bottom: 0;
                }.tdb_single_content .id_top_ad .adsbygoogle,
                .tdb_single_content .id_bottom_ad .adsbygoogle{
                  position: relative;
                }.tdb_single_content .id_ad_content-horiz-left,
                .tdb_single_content .id_ad_content-horiz-right,
                .tdb_single_content .id_ad_content-horiz-center{
                  margin-bottom: 15px;
                }.tdb_single_content .id_ad_content-horiz-left img,
                .tdb_single_content .id_ad_content-horiz-right img,
                .tdb_single_content .id_ad_content-horiz-center img{
                  margin-bottom: 0;
                }.tdb_single_content .id_ad_content-horiz-center{
                  text-align: center;
                }.tdb_single_content .id_ad_content-horiz-center img{
                  margin-right: auto;
                  margin-left: auto;
                }.tdb_single_content .id_ad_content-horiz-left{
                  float: left;
                  margin-top: 9px;
                  margin-right: 21px;
                }.tdb_single_content .id_ad_content-horiz-right{
                  float: right;
                  margin-top: 6px;
                  margin-left: 21px;
                }.tdb_single_content .tdc-a-ad .tdc-placeholder-title{
                  width: 300px;
                  height: 250px;
                }.tdb_single_content .tdc-a-ad .tdc-placeholder-title:before{
                  position: absolute;
                  top: 50%;
                  -webkit-transform: translateY(-50%);
                  transform: translateY(-50%);
                  margin: auto;
                  display: table;
                  width: 100%;
                }.tdb_single_content .tdb-block-inner.td-fix-index{
                    word-break: break-word;
                }.tdi_77,
                .tdi_77 > p,
                .tdi_77 .tdb-block-inner > p{
			        font-family:Open Sans !important;
		        }.tdi_77 h1{
			        font-family:Firasans Regular !important;
		        }.tdi_77 h2{
			        font-family:Firasans Regular !important;
		        }.tdi_77 h3:not(.tds-locker-title){
			        font-family:Firasans Regular !important;
		        }.tdi_77 h4{
			        font-family:Firasans Regular !important;
		        }.tdi_77 h5{
			        font-family:Firasans Regular !important;
		        }.tdi_77 h6{
			        font-family:Firasans Regular !important;
		        }.tdi_77,
				.tdi_77 p{
			        color: #656871;
		        }.tdi_77 h1,
				.tdi_77 h2,
				.tdi_77 h3:not(.tds-locker-title),
				.tdi_77 h4,
				.tdi_77 h5,
				.tdi_77 h6{
			        color: #3d3d3d;
		        }@media (max-width: 767px) {
                  .tdb_single_content .id_ad_content-horiz-left,
                  .tdb_single_content .id_ad_content-horiz-right,
                  .tdb_single_content .id_ad_content-horiz-center {
                    margin: 0 auto 26px auto;
                  }
                }@media (max-width: 767px) {
                  .tdb_single_content .id_ad_content-horiz-left {
                    margin-right: 0;
                  }
                }@media (max-width: 767px) {
                  .tdb_single_content .id_ad_content-horiz-right {
                    margin-left: 0;
                  }
                }@media (max-width: 767px) {
                  .tdb_single_content .td-a-ad {
                    float: none;
                    text-align: center;
                  }
                  .tdb_single_content .td-a-ad img {
                    margin-right: auto;
                    margin-left: auto;
                  }
                  .tdb_single_content .tdc-a-ad {
                    float: none;
                  }
                }
</style><div class="tdb-block-inner td-fix-index">
<p>In the article, we are going to examine how to optimize SQL queries and improve query performance by using SQL query optimization tips and techniques, such as <a rel="noreferrer noopener" href="https://blog.devart.com/sql-server-execution-plans.html" target="_blank">execution plans</a>, indexes, wildcards, and many others. </p>



<span id="more-30364"></span>



<figure class="wp-block-image"><a href="https://www.devart.com/dbforge/sql/studio/download.html" target="_blank" rel="noreferrer noopener"><img decoding="async" width="990" height="190" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20990%20190'%3E%3C/svg%3E" alt="Download a 30-day trial version of dbForge Studio for SQL Server and evaluate its cutting-edge features" class="wp-image-30934" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big.png 990w, https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big-300x58.png 300w, https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big-768x147.png 768w" data-lazy-sizes="(max-width: 990px) 100vw, 990px" data-lazy-src="/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big.png" /><noscript><img decoding="async" width="990" height="190" src="/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big.png" alt="Download a 30-day trial version of dbForge Studio for SQL Server and evaluate its cutting-edge features" class="wp-image-30934" srcset="https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big.png 990w, https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big-300x58.png 300w, https://blog.devart.com/wp-content/uploads/2021/12/Banner_blog_Studio_for_SQL_Server_big-768x147.png 768w" sizes="(max-width: 990px) 100vw, 990px" /></noscript></a></figure>



<p>When businesses and companies face SQL Server performance challenges, they focus usually on applying <a rel="noreferrer noopener" aria-label="performance tuning tools (opens in a new tab)" href="https://www.devart.com/dbforge/sql/studio/sql-server-query-optimization.html" target="_blank">performance tuning tools</a> and optimization techniques. This will help not only analyze and make queries run faster but also eliminate performance issues, troubleshoot poor performance, and avoid any chaos or minimize the impact on SQL Server databases.</p>



<p><strong>Contents</strong></p>



<ul>
<li><a href="#sql-query-optimization-basics">SQL query optimization basics</a></li>



<li><a href="#query-optimization-tips-for-better-performance">12 Query optimization tips for better performance</a><ul><li><a href="#missing-indexes">Tip 1: Add missing indexes </a></li><li><a href="#Non-used-indexes">Tip 2: Check for unused indexes</a></li><li><a href="#or-in-join-predicate">Tip 3: Avoid using multiple OR in the FILTER predicate </a></li></ul>
<ul>
<li><a href="#use-wildcards">Tip 4: Use wildcards at the end of a phrase only</a> </li>



<li><a href="#high-table-count">Tip 5: Avoid too many JOINs</a></li>



<li><a href="#avoid-using-select-distinct">Tip 6: Avoid using SELECT DISTINCT</a></li>



<li><a href="#use-select-fields-instead-of-select-all">Tip 7: Use SELECT fields instead of SELECT *</a></li>



<li><a href="#use-top-to-sample-query-results">Tip 8: Use TOP to sample query results</a></li>



<li><a href="#run-query-during-offpeak-hours">Tip 9: Run the query during off-peak hours</a></li>



<li><a href="#minimize-usage-of-query-hint">Tip 10: Minimize the usage of any query hint</a></li>



<li><a href="#minimize-large-write-operations">Tip 11: Minimize large write operations</a> </li>



<li><a href="#create-joins-with-inner-join">Tip 12: Create joins with INNER JOIN (not WHERE)</a></li>
</ul>
</li>



<li> <a href="#sql-query-optimization-best-practices">SQL query optimization best practices</a> </li>
</ul>



<h2 class="wp-block-heading" id="sql-query-optimization-basics">SQL query optimization basics</h2>



<p>Query optimization is a process of defining the most efficient and optimal way and techniques that can be used to improve query performance based on the rational use of system resources and performance metrics. The purpose of query tuning is to find a way to decrease the response time of the query, prevent the excessive consumption of resources, and identify poor query performance.</p>



<p>In the context of query optimization, query processing identifies how to faster retrieve data from SQL Server by analyzing the execution steps of the query, optimization techniques, and other information about the query.</p>



<h2 class="wp-block-heading" id="query-optimization-tips-for-better-performance">12 Query optimization tips for better performance </h2>



<p>Monitoring metrics can be used to evaluate query runtime, detect performance pitfalls, and show how they can be improved. For example, they include:</p>



<ul>
<li><strong>Execution plan</strong>: A SQL Server query optimizer executes the query step by step, scans indexes to retrieve data, and provides a detailed overview of metrics during query execution.</li>



<li><strong>Input/Output statistics</strong>: Used to identify the number of logical and physical reading operations during the query execution that helps users detect cache/memory capacity issues.</li>



<li><strong>Buffer cache</strong>: Used to reduce memory usage on the server.</li>



<li><strong>Latency</strong>: Used to analyze the duration of queries or operations. </li>



<li><strong>Indexes</strong>: Used to accelerate reading operations on the SQL Server.</li>



<li><strong>Memory-optimized tables</strong>: Used to store table data in memory to make reading and writing operations run faster.</li>
</ul>



<p>Now, we&#8217;ll discuss the best SQL Server performance tuning practices and tips you may apply when writing SQL queries.</p>



<h3 class="wp-block-heading" id="missing-indexes">Tip 1: Add missing indexes</h3>



<p>Table indexes in databases help retrieve information faster and more efficiently.</p>



<p>In SQL Server, when you execute a query, the optimizer generates an execution plan. If it detects the missing index that may be created to optimize performance, the execution plan suggests this in the warning section. With this suggestion, it informs you which columns the current SQL should be indexed, and how performance can be improved upon completion.</p>



<p>Let&#8217;s run the <a href="https://www.devart.com/dbforge/sql/studio/sql-query-profiler.html" target="_blank" rel="noreferrer noopener" aria-label="Query Profiler (opens in a new tab)">Query Profiler</a> available in dbForge Studio for SQL Server to see how it works.</p>



<figure class="wp-block-image"><img decoding="async" width="1000" height="649" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201000%20649'%3E%3C/svg%3E" alt="Execution plan displays missing indexes in dbForge Studio for SQL Server" class="wp-image-31391" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/missing-index.png 1000w, https://blog.devart.com/wp-content/uploads/2021/12/missing-index-300x195.png 300w, https://blog.devart.com/wp-content/uploads/2021/12/missing-index-768x498.png 768w" data-lazy-sizes="(max-width: 1000px) 100vw, 1000px" data-lazy-src="/wp-content/uploads/2021/12/missing-index.png" /><noscript><img decoding="async" width="1000" height="649" src="/wp-content/uploads/2021/12/missing-index.png" alt="Execution plan displays missing indexes in dbForge Studio for SQL Server" class="wp-image-31391" srcset="https://blog.devart.com/wp-content/uploads/2021/12/missing-index.png 1000w, https://blog.devart.com/wp-content/uploads/2021/12/missing-index-300x195.png 300w, https://blog.devart.com/wp-content/uploads/2021/12/missing-index-768x498.png 768w" sizes="(max-width: 1000px) 100vw, 1000px" /></noscript></figure>



<p>You can also understand which tables need indexes by analyzing graphical query plans. The thicker the arrow between operators on the query execution plan is, the more data is passed. Seeing thick arrows you need to think about adding indexes to the tables being processed to reduce the amount of data passed through the arrow. </p>



<figure class="wp-block-image"><img decoding="async" width="1000" height="800" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201000%20800'%3E%3C/svg%3E" alt="" class="wp-image-45803" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1.png 1000w, https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1-300x240.png 300w, https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1-768x614.png 768w" data-lazy-sizes="(max-width: 1000px) 100vw, 1000px" data-lazy-src="/wp-content/uploads/2022/09/index-optimization-1.png" /><noscript><img decoding="async" width="1000" height="800" src="/wp-content/uploads/2022/09/index-optimization-1.png" alt="" class="wp-image-45803" srcset="https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1.png 1000w, https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1-300x240.png 300w, https://blog.devart.com/wp-content/uploads/2022/09/index-optimization-1-768x614.png 768w" sizes="(max-width: 1000px) 100vw, 1000px" /></noscript></figure>



<p>On the execution plan, you might encounter Table Spool (Lazy Spool in our case) that builds a temporary table in the tempdb and fills it in a lazy manner. Simply put, the table is filled by reading and storing the data only when individual rows are required by the parent operator.  The Index Spool operator works in a somehow similar manner ⁠— all input rows are scanned and a copy of each row is placed in a hidden spool file that is stored in the tempdb database and exists only for the lifetime of the query. After that, an index on the rows is built. Both Table Spool and Index Spool might require optimization and adding indexes on the corresponding tables.</p>



<p>Nested Loops might also need your attention. Nested Loops must be indexed, as they take the first value from the first table and search for a match in the second table. Without indexes, SQL Server will have to scan and process the whole table, which can be time-consuming and resource-intensive.</p>



<p>Keep in mind that the missing index does not 100% guarantee better performance. In SQL Server, you can use the following  dynamic management views to get a deep insight in using indexes based on query execution history:</p>



<ul>
<li><strong>sys.dm_db_missing_index_details</strong>: Provides information about the suggested missing index, except for spatial indexes.</li>



<li><strong>sys.dm_db_missing_index_columns</strong>: Returns information about the table columns that do not contain indexes.</li>



<li><strong>sys.dm_db_missing_index_group_stats</strong>: Returns summary information about the missing index group, such as query cost, <em>avg_user_impact</em> (informs you how much performance can be improved by increasing the missing index), and some other metrics to measure effectiveness.</li>



<li><strong>sys.dm_db_missing_index_groups: </strong>Provides information about missing indexes included in a specific index group. </li>
</ul>



<h3 class="wp-block-heading" id="Non-used-indexes">Tip 2: Check for unused indexes</h3>



<p>You may encounter a situation where indexes exist but are not being used. One of the reasons for that might be implicit data type conversion. Let&#8217;s consider the following query:</p>



<pre class="wp-block-code"><code>SELECT *
FROM TestTable
WHERE IntColumn = '1';</code></pre>



<p>When executing this query, SQL Server will perform implicit data type conversion, i.e. convert int data to varchar and run the comparison only after that. In this case, indexes won&#8217;t be used. How can you avoid this? We recommend using the CAST() function that converts a value of any type into a specified datatype. Look at the query below.</p>



<pre class="wp-block-code"><code>SELECT *
FROM TestTable
WHERE IntColumn = CAST(@char AS INT);</code></pre>



<p>Let&#8217;s study one more example.</p>



<pre class="wp-block-code"><code>SELECT *
FROM TestTable
WHERE DATEPART(YEAR, SomeMyDate) = '2021';</code></pre>



<p>In this case, implicit data type conversion will take place too, and the indexes won&#8217;t be used. To avoid this, we can optimize the query in the following way:</p>



<pre class="wp-block-code"><code>SELECT *
FROM TestTable
WHERE SomeDate >= '20210101'
AND SomeDate &lt; '20220101'</code></pre>



<p>Filtered indexes can affect performance too. Suppose, we have an index on the Customer table.</p>



<pre class="wp-block-code"><code>CREATE UNIQUE NONCLUSTERED INDEX IX ON Customer (MembershipCode)
WHERE MembershipCode IS NOT NULL;</code></pre>



<p>The index won&#8217;t work for the following query:</p>



<pre class="wp-block-code"><code>SELECT *
FROM Customer
WHERE MembershipCode = '258410';</code></pre>



<p>To make use of the index, you&#8217;ll need to optimize the query in the following way:</p>



<pre class="wp-block-code"><code>SELECT *
FROM Customer
WHERE MembershipCode = '258410'
AND MembershipCode IS NOT NULL;</code></pre>



<h3 class="wp-block-heading" id="or-in-join-predicate">Tip 3: Avoid using multiple OR in the FILTER predicate</h3>



<p>When you need to combine two or more conditions, it is recommended to eliminate the usage of the OR operator or split the query into parts separating search expressions. SQL Server can not process OR within one operation. Instead, it evaluates each component of the OR which, in turn, may lead to poor performance. </p>



<p>Let&#8217;s consider the following query.</p>



<pre class="wp-block-code"><code>SELECT *
FROM USER
WHERE Name = @P
OR login = @P;</code></pre>



<p>If we split this query into two SELECT queries and combine them by using the UNION operator, SQL Server will be able to make use of the indexes, and the query will be optimized.</p>



<pre class="wp-block-code"><code>SELECT * FROM USER
WHERE Name = @P
UNION
SELECT * FROM USER
WHERE login = @P;</code></pre>



<h3 class="wp-block-heading" id="use-wildcards">Tip 4: Use wildcards at the end of a phrase only</h3>



<p><a href="https://www.devart.com/dbforge/sql/sqlcomplete/sql-wildcard-search.html" target="_blank">Wildcards in SQL Server</a> work as a placeholder for words and phrases and can be added at the beginning/end of them. To make data retrieval faster and more efficient, you can use wildcards in the SELECT statement at the end of a phrase. For example:</p>



<pre class="wp-block-code"><code>SELECT
  p.BusinessEntityID
 ,p.FirstName
 ,p.LastName
 ,p.Title
FROM Person.Person p
WHERE p.FirstName LIKE 'And%';</code></pre>



<p>As a result, the query will retrieve a list of customers whose First Name matches the specified condition, i.e. their First Name starts with &#8216;And&#8217;.</p>



<figure class="wp-block-image"><img decoding="async" width="529" height="524" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20529%20524'%3E%3C/svg%3E" alt="Retrieve data using wildcards in the SELECT statement" class="wp-image-31346" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/wildcards.png 529w, https://blog.devart.com/wp-content/uploads/2021/12/wildcards-150x150.png 150w, https://blog.devart.com/wp-content/uploads/2021/12/wildcards-300x297.png 300w" data-lazy-sizes="(max-width: 529px) 100vw, 529px" data-lazy-src="/wp-content/uploads/2021/12/wildcards.png" /><noscript><img decoding="async" width="529" height="524" src="/wp-content/uploads/2021/12/wildcards.png" alt="Retrieve data using wildcards in the SELECT statement" class="wp-image-31346" srcset="https://blog.devart.com/wp-content/uploads/2021/12/wildcards.png 529w, https://blog.devart.com/wp-content/uploads/2021/12/wildcards-150x150.png 150w, https://blog.devart.com/wp-content/uploads/2021/12/wildcards-300x297.png 300w" sizes="(max-width: 529px) 100vw, 529px" /></noscript></figure>



<p>However, you might encounter situations where you regularly need to search by the last symbols of a word, number, or phrase — for example, by the last digits of a telephone number. In this case, we recommend creating a persisted computed column and running the REVERSE() function on it for easier back-searching. </p>



<pre class="wp-block-code"><code>CREATE TABLE dbo.Customer (
  id INT IDENTITY PRIMARY KEY
 ,CardNo VARCHAR(128)
 ,ReversedCardNo AS REVERSE(CardNo) PERSISTED
)
GO

CREATE INDEX ByReversedCardNo ON dbo.Customer (ReversedCardNo)
GO
CREATE INDEX ByCardNo ON dbo.Customer (CardNo)
GO

INSERT INTO dbo.Customer (CardNo)
  SELECT
    NEWID()
  FROM master.dbo.spt_values sv

SELECT TOP 100
  *
FROM Customer c

--searching for CardNo that end in 510c
SELECT *
FROM dbo.Customer
WHERE CardNo LIKE '%510c'

SELECT
  *
FROM dbo.Customer
WHERE ReversedCardNo LIKE REVERSE('%510c')</code></pre>



<h3 class="wp-block-heading" id="high-table-count">Tip 5: Avoid too many JOINs</h3>



<p>When you add multiple tables to a query and join them, you may overload the server. In addition, a large number of tables to retrieve data from may result in an inefficient execution plan. When generating a plan, the SQL query optimizer needs to identify how the tables are joined, in which order, and how and when to apply filters and aggregation. </p>



<p>All SQL experts are aware of the <a href="https://www.devart.com/dbforge/sql/sqlcomplete/sql-join-statements.html" target="_blank">SQL JOINs</a> importance, and understanding how to use them in queries appropriately is critical. In particular, JOIN elimination is one of the many techniques to achieve efficient query plans. You can split a single query into several separate queries which can later be joined, and thus remove unnecessary joins, subqueries, tables, etc. </p>



<h3 class="wp-block-heading" id="avoid-using-select-distinct">Tip 6: Avoid using SELECT DISTINCT</h3>



<p> The SQL DISTINCT operator is used to select only unique values of the column and thus eliminate duplicated values. It has the following syntax:</p>



<pre class="wp-block-code"><code>SELECT DISTINCT column_name FROM table_name;</code></pre>



<p>However, this may require the tool to process large volumes of data and as a result, make the query run slowly. Generally, it is recommended to avoid using SELECT DISTINCT and simply execute the SELECT statement but specify columns. </p>



<p>Another issue is that quite often people build JOINs unnecessarily, and when the data doubles, they add DISTINCT. This happens mainly in a leader-follower relation when people do <code>SELECT DISTINCT … FROM LEADER JOIN FOLLOWER…</code> instead of doing the correct <code>SELECT … FROM LEADER WHERE EXISTS (SELECT… FROM FOLLOWER)</code>.</p>



<h3 class="wp-block-heading" id="use-select-fields-instead-of-select-all">Tip 7: Use SELECT fields instead of SELECT *</h3>



<p>The SELECT statement is used to retrieve data from the database. In the case of large databases, it is not recommended to retrieve all data because this will take more resources on querying a huge volume of data. </p>



<p>If we execute the following query, we will retrieve all data from the <strong>Users</strong> table, including, for example, users&#8217; avatar pictures. The result table will contain lots of data and will take too much memory and CPU usage.</p>



<pre class="wp-block-code"><code>SELECT
  *
FROM Users;</code></pre>



<p>Instead, you can specify the exact columns you need to get data from, thus, saving database resources. In this case, SQL Server will retrieve only the required data, and the query will have lower cost.</p>



<p>For example:</p>



<pre class="wp-block-code"><code>SELECT
    FirstName
   ,LastName
   ,Email
   ,Login
FROM Users;</code></pre>



<p>If you need to retrieve this data regularly, for example, for authentication purposes, we recommend using covering indexes, the biggest advantage of which is that they contain all the fields required by query and can significantly improve query performance and guarantee better results.</p>



<pre class="wp-block-code"><code>CREATE NONCLUSTERED INDEX IDX_Users_Covering ON Users
INCLUDE (FirstName, LastName, Email, Login)</code></pre>



<h3 class="wp-block-heading" id="use-top-to-sample-query-results">Tip 8: Use TOP to sample query results</h3>



<p>The SELECT TOP command is used to set a limit on the number of records to be returned from the database. To make sure that your query will output the required result, you can use this command to fetch several rows as a sample.</p>



<p>For example, take the query from the previous section and define the limit of 5 records in the result set.</p>



<pre class="wp-block-code"><code>SELECT TOP 5
  p.BusinessEntityID
 ,p.FirstName
 ,p.LastName
 ,p.Title
FROM Person.Person p
WHERE p.FirstName LIKE 'And%';</code></pre>



<p>This query will retrieve only 5 records matching the condition:</p>



<figure class="wp-block-image"><img decoding="async" width="419" height="360" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20419%20360'%3E%3C/svg%3E" alt="Use LIMIT (TOP in SQL) to sample query results" class="wp-image-31353" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/use-limit.png 419w, https://blog.devart.com/wp-content/uploads/2021/12/use-limit-300x258.png 300w" data-lazy-sizes="(max-width: 419px) 100vw, 419px" data-lazy-src="/wp-content/uploads/2021/12/use-limit.png" /><noscript><img decoding="async" width="419" height="360" src="/wp-content/uploads/2021/12/use-limit.png" alt="Use LIMIT (TOP in SQL) to sample query results" class="wp-image-31353" srcset="https://blog.devart.com/wp-content/uploads/2021/12/use-limit.png 419w, https://blog.devart.com/wp-content/uploads/2021/12/use-limit-300x258.png 300w" sizes="(max-width: 419px) 100vw, 419px" /></noscript></figure>



<h3 class="wp-block-heading" id="run-query-during-offpeak-hours">Tip 9: Run the query during off-peak hours</h3>



<p>Another SQL tuning technique is to schedule the query execution at off-peak hours, especially if you need to run multiple SELECT queries from large tables or execute complex queries with nested subqueries, looping queries, etc. If you are running a heavy query against a database, SQL Server locks the tables you are working with to prevent concurrent use of resources by different transactions. That means that other users are not able to work with those tables. Thus, executing heavy queries at peak times leads not only to server overload but also to restricting other users&#8217; access to certain amounts of data. One of the popular mechanisms to avoid this is to use the <strong>WITH (NOLOCK)</strong> hint. It allows the user to retrieve the data without being affected by the locks. The biggest drawback of using <strong>WITH (NOLOCK)</strong> is that it may result in working with dirty data. We recommend that users should give preference to snapshot isolation which helps avoid data locking by using row versioning and guarantees that each transaction sees a consistent snapshot of the database. </p>



<h3 class="wp-block-heading" id="minimize-usage-of-query-hint">Tip 10: Minimize the usage of any query hint</h3>



<p>When you face performance issues, you may use query hints to optimize queries. They are specified in T-SQL statements and make the optimizer select the execution plan based on this hint.&nbsp;Usually, query hints include  NOLOCK, Optimize For and Recompile. However, you should carefully consider their usage because sometimes they may cause more unexpected side effects, undesirable impacts, or even break business logic when trying to solve the issue. For example, you write additional code for the hints that can be inapplicable or obsolete after a while. This means that you should always monitor, manage, check, and keep hints up to date.</p>



<h3 class="wp-block-heading" id="minimize-large-write-operations">Tip 11: Minimize large write operations</h3>



<p>Writing, modifying, deleting, or importing large volumes of data may impact query performance and even block the table when it requires updating and manipulating data, adding indexes or check constraints to queries, processing triggers, etc. In addition, writing a lot of data will increase the size of log files. Thus, large write operations may not be a huge performance issue, but you should be aware of their consequences and be prepared in case of unexpected behavior.</p>



<p>One of the best practices in optimizing SQL Server performance lies in using filegroups that allow you to spread your data across multiple physical disks. Thereby multiple write operations can be processed simultaneously and thus much faster.</p>



<p>Compression and data partitioning can also optimize performance and help minimize the cost of large write operations.</p>



<h3 class="wp-block-heading" id="create-joins-with-inner-join">Tip 12: Create JOINs with INNER JOIN (not WHERE)</h3>



<p>The <a href="https://www.devart.com/dbforge/sql/sqlcomplete/sql-inner-join-statement.html" target="_blank">SQL INNER JOIN</a> statement returns all matching rows from joined tables, while the WHERE clause filters the resulting rows based on the specified condition. Retrieving data from multiple tables based on the WHERE keyword condition is called NON-ANSI JOINs while INNER JOIN belongs to ANSI JOINs. </p>



<p>It does not matter for SQL Server how you write the query &#8211; using ANSI or NON-ANSI joins &#8211; it&#8217;s just much easier to understand and analyze queries written using ANSI joins. You can clearly see where the JOIN conditions and the WHERE filters are, whether you missed any JOIN or filter predicates, whether you joined the required tables, etc.</p>



<p>Let&#8217;s see how to optimize a SQL query with INNER JOIN on a particular example. We are going to retrieve data from the tables <strong>HumanResources.Department </strong>and <strong>HumanResources.EmployeeDepartmentHistory </strong>where DepartmentIDs are the same. First, execute the SELECT statement with the INNER JOIN type:</p>



<pre class="wp-block-code"><code>SELECT
  d.DepartmentID
 ,d.Name
 ,d.GroupName
FROM HumanResources.Department d
INNER JOIN HumanResources.EmployeeDepartmentHistory edh
  ON d.DepartmentID = edh.DepartmentID</code></pre>



<p>Then, use the WHERE clause instead of INNER JOIN to join the tables in the SELECT statement: </p>



<pre class="wp-block-code"><code>SELECT
  d.Name
 ,d.GroupName
 ,d.DepartmentID
FROM HumanResources.Department d
    ,HumanResources.EmployeeDepartmentHistory edh
WHERE d.DepartmentID = edh.DepartmentID</code></pre>



<p>Both queries will output the following result:</p>



<figure class="wp-block-image"><img decoding="async" width="448" height="240" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20448%20240'%3E%3C/svg%3E" alt="Retrieve data using INNER JOIN" class="wp-image-31293" data-lazy-srcset="https://blog.devart.com/wp-content/uploads/2021/12/inner-joins.png 448w, https://blog.devart.com/wp-content/uploads/2021/12/inner-joins-300x161.png 300w" data-lazy-sizes="(max-width: 448px) 100vw, 448px" data-lazy-src="/wp-content/uploads/2021/12/inner-joins.png" /><noscript><img decoding="async" width="448" height="240" src="/wp-content/uploads/2021/12/inner-joins.png" alt="Retrieve data using INNER JOIN" class="wp-image-31293" srcset="https://blog.devart.com/wp-content/uploads/2021/12/inner-joins.png 448w, https://blog.devart.com/wp-content/uploads/2021/12/inner-joins-300x161.png 300w" sizes="(max-width: 448px) 100vw, 448px" /></noscript></figure>



<h2 class="wp-block-heading" id="sql-query-optimization-best-practices">SQL query optimization best practices</h2>



<p>SQL Server performance tuning and SQL query optimization are some of the main aspects for database developers and administrators. They need to carefully consider the usage of specific operators, the number of tables on a query, the size of a query, its execution plan, statistics, resource allocation, and other performance metrics &#8211; all that may improve and tune query performance or make it worse.</p>



<p>For better query performance, we recommend using tips and techniques presented in the article, such as running queries at off-peak hours, creating indexes, retrieving data only for the specific columns, applying the correct filter, joins, and operators, as well as trying not to overload queries.</p>



<p>In addition, we propose some recommendations which may not directly relate to coding techniques, but they can still help you write precise and efficient SQL code.</p>



<p><strong>Use uppercase for keywords</strong></p>



<p>Keywords in SQL are generally case-insensitive. You can use lower case, upper case, or both mixed across all popular database management systems, including Microsoft SQL Server. However, it is recommended to use the upper case for keywords for improved code readability.</p>



<p>Although some developers may find it cumbersome to switch between upper and lower case while coding, modern SQL code formatting tools provide the functionality to configure case usage, text coloring, indents, and other options. These tools can automatically apply the preferable formatting while typing.</p>



<p><strong>Write comments for your SQL code</strong></p>



<p>Commenting on the code is optional, but it is highly recommended. Even if some code solutions seem obvious at the moment, what happens in a couple of months when you need to revisit it, especially after writing lots of other code for different modules or projects? This is especially important for your colleagues who will have to work with your code.</p>



<p>Another essential point is to review your existing comments whenever you make changes to your code, ensuring that they remain relevant. It may take time, but it greatly improves the readability of your code, and your efforts will pay off.</p>



<p><strong>Use a professional SQL code editor</strong></p>



<p>As a developer, you may apply various techniques and customize your workflows according to your preferences, but creating code manually from scratch consumes a lot of time and demands exceptional precision. A reliable and potent SQL editor makes code writing easier and enhances accuracy.</p>



<p>Modern SQL editors offer robust functionality for query development, such as auto-completion options, libraries of code snippets, syntax validation, and code formatting. Advanced <a href="https://www.devart.com/dbforge/edge/" target="_blank">tools for SQL development</a> allow developers to double the coding speed twice (at least) and guarantee outstanding code quality.</p>



<h2 class="wp-block-heading">Conclusion</h2>