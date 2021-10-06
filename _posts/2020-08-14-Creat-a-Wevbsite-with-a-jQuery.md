---
layout: mypost
title: Creat a website with jQuery
categories: [jQuery]
---

### Javascript Lerninning:

#### Learning Journey:

##### 1.Download [GlennOu66304/frontend-nanodegree-resume](https://github.com/GlennOu66304/frontend-nanodegree-resume)

##### 2.put the jQuery into the code file project:

1.put the physical file into the code project
You need to single click the file and choose " Save link as " to download the file in the local, then use the sublime editor to open it
Tutorail could be seen in the [jQuery tutorial: Downloading and installing jQuery | lynda.com](https://www.youtube.com/watch?v=7hduZL1q-KM)

2.put the CDN into the Html file.

jQuery CDN hosted by Google
In the same way we can use jQuery CDN hosted by Google, as shown below:

```
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
</head>
```

jQuery CDN hosted by Microsoft
Microsoft also hosts jQuery and this CDN is used below:

```
<head>
    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-3.2.1.min.js"></script>
</head>
```

jQuery CDN hosted by CloudFlare
CloudFlare is a great CDN and also very popular too. It also has jQuery CDN which you can use in your website.

```
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
</head>
```

you could check the references below:  
YOGIHOSTING:[What is jQuery CDN and how you can use it in your website](https://www.yogihosting.com/jquery-cdn/)  
educative.io:[How to add jQuery from a CDN?](https://www.educative.io/edpresso/how-to-add-jquery-from-a-cdn)  
W3School:[jQuery CDN](https://www.w3schools.com/jquery/jquery_get_started.asp)  
Google Hosted Libraries:[jQuery](https://developers.google.com/speed/libraries#jquery)  
cdnjs:[jqueryJavaScript library for DOM operations](https://cdnjs.com/libraries/jquery/3.3.1)  
official documenttation[Using jQuery with a CDN](https://jquery.com/download/)  
[jQuery CDN – Latest Stable Versions](https://code.jquery.com/)

##### 3.Play around with the jQuery:

1.First download the code project from the CodePen. if you have question about this process, please go to [2020.08.07 Code pen and React Coding Learnning](http://glennou.cn/2020/08/07/React-Learning/)to get instructions.  
2. First remove the "src fold" and disc fold,and add "js" fold and "css" fold into the subfold under the main fold "getting-started-with-jquery". at the same time, you need to put the style.css file into css and put "script.js" into js fold.  
3. change the css code into

```
<link rel="stylesheet" href="css/style.css">
```

in the index.html.

4.change the js code to

```
<script  src="js/script.js"></script>
```

##### 4.apply the jQuery grammr into the code

```
$(document).ready(function(){

    $("h3").click(function(){
        $("button").hide();
    });

});
```

above code said that select the H3 paragraph and click it,
it will generate a new functon: to select the"button" and hide this button.  
Utilize the $ to select the product, and assing certain product.  
MDN:[jQuery](https://developer.mozilla.org/en-US/docs/Glossary/jQuery)  
Resources list:  
1.video:[https://api.jquery.com/](https://www.youtube.com/watch?v=KhtEmR2A1Fw)  
2.Code:[Getting started with jQuery](https://codepen.io/beaucarnes/pen/mwGZre)

##### 5.Resource list:

[Udacity Javascript Begin level Course](https://classroom.udacity.com/courses/ud245)  
[Intro to jQuery](https://www.udacity.com/course/intro-to-jquery--ud245)  
OFFICIAL Documentation:[jQuery](https://jquery.com/download/)
[[Roadmap] Learn Modern Javascript With Udacity](https://medium.com/@berkancetinkaya/roadmap-learn-modern-javascript-with-udacity-297b99033b0c)  
[Introduction to JavaScript Source Maps](https://www.html5rocks.com/en/tutorials/developertools/sourcemaps/)  
[Style Guide](https://learn.jquery.com/style-guide/)  
[jQuery API](https://api.jquery.com/)  
Udacity Course  
Kyle simpson <You don't about JS>  
Front End master JS course  
MDN documentation  
W3School Tutorial  
FreecodeCamp  
Google JS course:[Learning program with Javascript](https://openclassrooms.com/en/courses/5664271-learn-programming-by-practicing-javascript)  
JavaScript30:[JavaScript30](https://www.youtube.com/playlist?list=PLu8EoSxDXHP6CGK4YVJhL_VWetA865GOH)
