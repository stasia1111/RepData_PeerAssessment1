<!DOCTYPE html>
<!-- saved from url=(0014)about:internet -->
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<meta http-equiv="x-ua-compatible" content="IE=9" >

<title>Reproducible Research</title>

<style type="text/css">
body, td {
   font-family: sans-serif;
   background-color: white;
   font-size: 12px;
   margin: 8px;
}

tt, code, pre {
   font-family: 'DejaVu Sans Mono', 'Droid Sans Mono', 'Lucida Console', Consolas, Monaco, monospace;
}

h1 { 
   font-size:2.2em; 
}

h2 { 
   font-size:1.8em; 
}

h3 { 
   font-size:1.4em; 
}

h4 { 
   font-size:1.0em; 
}

h5 { 
   font-size:0.9em; 
}

h6 { 
   font-size:0.8em; 
}

a:visited {
   color: rgb(50%, 0%, 50%);
}

pre {	
   margin-top: 0;
   max-width: 95%;
   border: 1px solid #ccc;
   white-space: pre-wrap;
}

pre code {
   display: block; padding: 0.5em;
}

code.r, code.cpp {
   background-color: #F8F8F8;
}

table, td, th {
  border: none;
}

blockquote {
   color:#666666;
   margin:0;
   padding-left: 1em;
   border-left: 0.5em #EEE solid;
}

hr {
   height: 0px;
   border-bottom: none;
   border-top-width: thin;
   border-top-style: dotted;
   border-top-color: #999999;
}

@media print {
   * { 
      background: transparent !important; 
      color: black !important; 
      filter:none !important; 
      -ms-filter: none !important; 
   }

   body { 
      font-size:12pt; 
      max-width:100%; 
   }
       
   a, a:visited { 
      text-decoration: underline; 
   }

   hr { 
      visibility: hidden;
      page-break-before: always;
   }

   pre, blockquote { 
      padding-right: 1em; 
      page-break-inside: avoid; 
   }

   tr, img { 
      page-break-inside: avoid; 
   }

   img { 
      max-width: 100% !important; 
   }

   @page :left { 
      margin: 15mm 20mm 15mm 10mm; 
   }
     
   @page :right { 
      margin: 15mm 10mm 15mm 20mm; 
   }

   p, h2, h3 { 
      orphans: 3; widows: 3; 
   }

   h2, h3 { 
      page-break-after: avoid; 
   }
}

</style>

<!-- Styles for R syntax highlighter -->
<style type="text/css">
   pre .operator,
   pre .paren {
     color: rgb(104, 118, 135)
   }

   pre .literal {
     color: rgb(88, 72, 246)
   }

   pre .number {
     color: rgb(0, 0, 205);
   }

   pre .comment {
     color: rgb(76, 136, 107);
   }

   pre .keyword {
     color: rgb(0, 0, 255);
   }

   pre .identifier {
     color: rgb(0, 0, 0);
   }

   pre .string {
     color: rgb(3, 106, 7);
   }
</style>

<!-- R syntax highlighter -->
<script type="text/javascript">
var hljs=new function(){function m(p){return p.replace(/&/gm,"&amp;").replace(/</gm,"&lt;")}function f(r,q,p){return RegExp(q,"m"+(r.cI?"i":"")+(p?"g":""))}function b(r){for(var p=0;p<r.childNodes.length;p++){var q=r.childNodes[p];if(q.nodeName=="CODE"){return q}if(!(q.nodeType==3&&q.nodeValue.match(/\s+/))){break}}}function h(t,s){var p="";for(var r=0;r<t.childNodes.length;r++){if(t.childNodes[r].nodeType==3){var q=t.childNodes[r].nodeValue;if(s){q=q.replace(/\n/g,"")}p+=q}else{if(t.childNodes[r].nodeName=="BR"){p+="\n"}else{p+=h(t.childNodes[r])}}}if(/MSIE [678]/.test(navigator.userAgent)){p=p.replace(/\r/g,"\n")}return p}function a(s){var r=s.className.split(/\s+/);r=r.concat(s.parentNode.className.split(/\s+/));for(var q=0;q<r.length;q++){var p=r[q].replace(/^language-/,"");if(e[p]){return p}}}function c(q){var p=[];(function(s,t){for(var r=0;r<s.childNodes.length;r++){if(s.childNodes[r].nodeType==3){t+=s.childNodes[r].nodeValue.length}else{if(s.childNodes[r].nodeName=="BR"){t+=1}else{if(s.childNodes[r].nodeType==1){p.push({event:"start",offset:t,node:s.childNodes[r]});t=arguments.callee(s.childNodes[r],t);p.push({event:"stop",offset:t,node:s.childNodes[r]})}}}}return t})(q,0);return p}function k(y,w,x){var q=0;var z="";var s=[];function u(){if(y.length&&w.length){if(y[0].offset!=w[0].offset){return(y[0].offset<w[0].offset)?y:w}else{return w[0].event=="start"?y:w}}else{return y.length?y:w}}function t(D){var A="<"+D.nodeName.toLowerCase();for(var B=0;B<D.attributes.length;B++){var C=D.attributes[B];A+=" "+C.nodeName.toLowerCase();if(C.value!==undefined&&C.value!==false&&C.value!==null){A+='="'+m(C.value)+'"'}}return A+">"}while(y.length||w.length){var v=u().splice(0,1)[0];z+=m(x.substr(q,v.offset-q));q=v.offset;if(v.event=="start"){z+=t(v.node);s.push(v.node)}else{if(v.event=="stop"){var p,r=s.length;do{r--;p=s[r];z+=("</"+p.nodeName.toLowerCase()+">")}while(p!=v.node);s.splice(r,1);while(r<s.length){z+=t(s[r]);r++}}}}return z+m(x.substr(q))}function j(){function q(x,y,v){if(x.compiled){return}var u;var s=[];if(x.k){x.lR=f(y,x.l||hljs.IR,true);for(var w in x.k){if(!x.k.hasOwnProperty(w)){continue}if(x.k[w] instanceof Object){u=x.k[w]}else{u=x.k;w="keyword"}for(var r in u){if(!u.hasOwnProperty(r)){continue}x.k[r]=[w,u[r]];s.push(r)}}}if(!v){if(x.bWK){x.b="\\b("+s.join("|")+")\\s"}x.bR=f(y,x.b?x.b:"\\B|\\b");if(!x.e&&!x.eW){x.e="\\B|\\b"}if(x.e){x.eR=f(y,x.e)}}if(x.i){x.iR=f(y,x.i)}if(x.r===undefined){x.r=1}if(!x.c){x.c=[]}x.compiled=true;for(var t=0;t<x.c.length;t++){if(x.c[t]=="self"){x.c[t]=x}q(x.c[t],y,false)}if(x.starts){q(x.starts,y,false)}}for(var p in e){if(!e.hasOwnProperty(p)){continue}q(e[p].dM,e[p],true)}}function d(B,C){if(!j.called){j();j.called=true}function q(r,M){for(var L=0;L<M.c.length;L++){if((M.c[L].bR.exec(r)||[null])[0]==r){return M.c[L]}}}function v(L,r){if(D[L].e&&D[L].eR.test(r)){return 1}if(D[L].eW){var M=v(L-1,r);return M?M+1:0}return 0}function w(r,L){return L.i&&L.iR.test(r)}function K(N,O){var M=[];for(var L=0;L<N.c.length;L++){M.push(N.c[L].b)}var r=D.length-1;do{if(D[r].e){M.push(D[r].e)}r--}while(D[r+1].eW);if(N.i){M.push(N.i)}return f(O,M.join("|"),true)}function p(M,L){var N=D[D.length-1];if(!N.t){N.t=K(N,E)}N.t.lastIndex=L;var r=N.t.exec(M);return r?[M.substr(L,r.index-L),r[0],false]:[M.substr(L),"",true]}function z(N,r){var L=E.cI?r[0].toLowerCase():r[0];var M=N.k[L];if(M&&M instanceof Array){return M}return false}function F(L,P){L=m(L);if(!P.k){return L}var r="";var O=0;P.lR.lastIndex=0;var M=P.lR.exec(L);while(M){r+=L.substr(O,M.index-O);var N=z(P,M);if(N){x+=N[1];r+='<span class="'+N[0]+'">'+M[0]+"</span>"}else{r+=M[0]}O=P.lR.lastIndex;M=P.lR.exec(L)}return r+L.substr(O,L.length-O)}function J(L,M){if(M.sL&&e[M.sL]){var r=d(M.sL,L);x+=r.keyword_count;return r.value}else{return F(L,M)}}function I(M,r){var L=M.cN?'<span class="'+M.cN+'">':"";if(M.rB){y+=L;M.buffer=""}else{if(M.eB){y+=m(r)+L;M.buffer=""}else{y+=L;M.buffer=r}}D.push(M);A+=M.r}function G(N,M,Q){var R=D[D.length-1];if(Q){y+=J(R.buffer+N,R);return false}var P=q(M,R);if(P){y+=J(R.buffer+N,R);I(P,M);return P.rB}var L=v(D.length-1,M);if(L){var O=R.cN?"</span>":"";if(R.rE){y+=J(R.buffer+N,R)+O}else{if(R.eE){y+=J(R.buffer+N,R)+O+m(M)}else{y+=J(R.buffer+N+M,R)+O}}while(L>1){O=D[D.length-2].cN?"</span>":"";y+=O;L--;D.length--}var r=D[D.length-1];D.length--;D[D.length-1].buffer="";if(r.starts){I(r.starts,"")}return R.rE}if(w(M,R)){throw"Illegal"}}var E=e[B];var D=[E.dM];var A=0;var x=0;var y="";try{var s,u=0;E.dM.buffer="";do{s=p(C,u);var t=G(s[0],s[1],s[2]);u+=s[0].length;if(!t){u+=s[1].length}}while(!s[2]);if(D.length>1){throw"Illegal"}return{r:A,keyword_count:x,value:y}}catch(H){if(H=="Illegal"){return{r:0,keyword_count:0,value:m(C)}}else{throw H}}}function g(t){var p={keyword_count:0,r:0,value:m(t)};var r=p;for(var q in e){if(!e.hasOwnProperty(q)){continue}var s=d(q,t);s.language=q;if(s.keyword_count+s.r>r.keyword_count+r.r){r=s}if(s.keyword_count+s.r>p.keyword_count+p.r){r=p;p=s}}if(r.language){p.second_best=r}return p}function i(r,q,p){if(q){r=r.replace(/^((<[^>]+>|\t)+)/gm,function(t,w,v,u){return w.replace(/\t/g,q)})}if(p){r=r.replace(/\n/g,"<br>")}return r}function n(t,w,r){var x=h(t,r);var v=a(t);var y,s;if(v){y=d(v,x)}else{return}var q=c(t);if(q.length){s=document.createElement("pre");s.innerHTML=y.value;y.value=k(q,c(s),x)}y.value=i(y.value,w,r);var u=t.className;if(!u.match("(\\s|^)(language-)?"+v+"(\\s|$)")){u=u?(u+" "+v):v}if(/MSIE [678]/.test(navigator.userAgent)&&t.tagName=="CODE"&&t.parentNode.tagName=="PRE"){s=t.parentNode;var p=document.createElement("div");p.innerHTML="<pre><code>"+y.value+"</code></pre>";t=p.firstChild.firstChild;p.firstChild.cN=s.cN;s.parentNode.replaceChild(p.firstChild,s)}else{t.innerHTML=y.value}t.className=u;t.result={language:v,kw:y.keyword_count,re:y.r};if(y.second_best){t.second_best={language:y.second_best.language,kw:y.second_best.keyword_count,re:y.second_best.r}}}function o(){if(o.called){return}o.called=true;var r=document.getElementsByTagName("pre");for(var p=0;p<r.length;p++){var q=b(r[p]);if(q){n(q,hljs.tabReplace)}}}function l(){if(window.addEventListener){window.addEventListener("DOMContentLoaded",o,false);window.addEventListener("load",o,false)}else{if(window.attachEvent){window.attachEvent("onload",o)}else{window.onload=o}}}var e={};this.LANGUAGES=e;this.highlight=d;this.highlightAuto=g;this.fixMarkup=i;this.highlightBlock=n;this.initHighlighting=o;this.initHighlightingOnLoad=l;this.IR="[a-zA-Z][a-zA-Z0-9_]*";this.UIR="[a-zA-Z_][a-zA-Z0-9_]*";this.NR="\\b\\d+(\\.\\d+)?";this.CNR="\\b(0[xX][a-fA-F0-9]+|(\\d+(\\.\\d*)?|\\.\\d+)([eE][-+]?\\d+)?)";this.BNR="\\b(0b[01]+)";this.RSR="!|!=|!==|%|%=|&|&&|&=|\\*|\\*=|\\+|\\+=|,|\\.|-|-=|/|/=|:|;|<|<<|<<=|<=|=|==|===|>|>=|>>|>>=|>>>|>>>=|\\?|\\[|\\{|\\(|\\^|\\^=|\\||\\|=|\\|\\||~";this.ER="(?![\\s\\S])";this.BE={b:"\\\\.",r:0};this.ASM={cN:"string",b:"'",e:"'",i:"\\n",c:[this.BE],r:0};this.QSM={cN:"string",b:'"',e:'"',i:"\\n",c:[this.BE],r:0};this.CLCM={cN:"comment",b:"//",e:"$"};this.CBLCLM={cN:"comment",b:"/\\*",e:"\\*/"};this.HCM={cN:"comment",b:"#",e:"$"};this.NM={cN:"number",b:this.NR,r:0};this.CNM={cN:"number",b:this.CNR,r:0};this.BNM={cN:"number",b:this.BNR,r:0};this.inherit=function(r,s){var p={};for(var q in r){p[q]=r[q]}if(s){for(var q in s){p[q]=s[q]}}return p}}();hljs.LANGUAGES.cpp=function(){var a={keyword:{"false":1,"int":1,"float":1,"while":1,"private":1,"char":1,"catch":1,"export":1,virtual:1,operator:2,sizeof:2,dynamic_cast:2,typedef:2,const_cast:2,"const":1,struct:1,"for":1,static_cast:2,union:1,namespace:1,unsigned:1,"long":1,"throw":1,"volatile":2,"static":1,"protected":1,bool:1,template:1,mutable:1,"if":1,"public":1,friend:2,"do":1,"return":1,"goto":1,auto:1,"void":2,"enum":1,"else":1,"break":1,"new":1,extern:1,using:1,"true":1,"class":1,asm:1,"case":1,typeid:1,"short":1,reinterpret_cast:2,"default":1,"double":1,register:1,explicit:1,signed:1,typename:1,"try":1,"this":1,"switch":1,"continue":1,wchar_t:1,inline:1,"delete":1,alignof:1,char16_t:1,char32_t:1,constexpr:1,decltype:1,noexcept:1,nullptr:1,static_assert:1,thread_local:1,restrict:1,_Bool:1,complex:1},built_in:{std:1,string:1,cin:1,cout:1,cerr:1,clog:1,stringstream:1,istringstream:1,ostringstream:1,auto_ptr:1,deque:1,list:1,queue:1,stack:1,vector:1,map:1,set:1,bitset:1,multiset:1,multimap:1,unordered_set:1,unordered_map:1,unordered_multiset:1,unordered_multimap:1,array:1,shared_ptr:1}};return{dM:{k:a,i:"</",c:[hljs.CLCM,hljs.CBLCLM,hljs.QSM,{cN:"string",b:"'\\\\?.",e:"'",i:"."},{cN:"number",b:"\\b(\\d+(\\.\\d*)?|\\.\\d+)(u|U|l|L|ul|UL|f|F)"},hljs.CNM,{cN:"preprocessor",b:"#",e:"$"},{cN:"stl_container",b:"\\b(deque|list|queue|stack|vector|map|set|bitset|multiset|multimap|unordered_map|unordered_set|unordered_multiset|unordered_multimap|array)\\s*<",e:">",k:a,r:10,c:["self"]}]}}}();hljs.LANGUAGES.r={dM:{c:[hljs.HCM,{cN:"number",b:"\\b0[xX][0-9a-fA-F]+[Li]?\\b",e:hljs.IMMEDIATE_RE,r:0},{cN:"number",b:"\\b\\d+(?:[eE][+\\-]?\\d*)?L\\b",e:hljs.IMMEDIATE_RE,r:0},{cN:"number",b:"\\b\\d+\\.(?!\\d)(?:i\\b)?",e:hljs.IMMEDIATE_RE,r:1},{cN:"number",b:"\\b\\d+(?:\\.\\d*)?(?:[eE][+\\-]?\\d*)?i?\\b",e:hljs.IMMEDIATE_RE,r:0},{cN:"number",b:"\\.\\d+(?:[eE][+\\-]?\\d*)?i?\\b",e:hljs.IMMEDIATE_RE,r:1},{cN:"keyword",b:"(?:tryCatch|library|setGeneric|setGroupGeneric)\\b",e:hljs.IMMEDIATE_RE,r:10},{cN:"keyword",b:"\\.\\.\\.",e:hljs.IMMEDIATE_RE,r:10},{cN:"keyword",b:"\\.\\.\\d+(?![\\w.])",e:hljs.IMMEDIATE_RE,r:10},{cN:"keyword",b:"\\b(?:function)",e:hljs.IMMEDIATE_RE,r:2},{cN:"keyword",b:"(?:if|in|break|next|repeat|else|for|return|switch|while|try|stop|warning|require|attach|detach|source|setMethod|setClass)\\b",e:hljs.IMMEDIATE_RE,r:1},{cN:"literal",b:"(?:NA|NA_integer_|NA_real_|NA_character_|NA_complex_)\\b",e:hljs.IMMEDIATE_RE,r:10},{cN:"literal",b:"(?:NULL|TRUE|FALSE|T|F|Inf|NaN)\\b",e:hljs.IMMEDIATE_RE,r:1},{cN:"identifier",b:"[a-zA-Z.][a-zA-Z0-9._]*\\b",e:hljs.IMMEDIATE_RE,r:0},{cN:"operator",b:"<\\-(?!\\s*\\d)",e:hljs.IMMEDIATE_RE,r:2},{cN:"operator",b:"\\->|<\\-",e:hljs.IMMEDIATE_RE,r:1},{cN:"operator",b:"%%|~",e:hljs.IMMEDIATE_RE},{cN:"operator",b:">=|<=|==|!=|\\|\\||&&|=|\\+|\\-|\\*|/|\\^|>|<|!|&|\\||\\$|:",e:hljs.IMMEDIATE_RE,r:0},{cN:"operator",b:"%",e:"%",i:"\\n",r:1},{cN:"identifier",b:"`",e:"`",r:0},{cN:"string",b:'"',e:'"',c:[hljs.BE],r:0},{cN:"string",b:"'",e:"'",c:[hljs.BE],r:0},{cN:"paren",b:"[[({\\])}]",e:hljs.IMMEDIATE_RE,r:0}]}};
hljs.initHighlightingOnLoad();
</script>




</head>

<body>
<h1>Reproducible Research</h1>

<h1>Peer Assessment 1</h1>

<h2>Loading and preprocessing the data</h2>

<ol>
<li>Load the data</li>
</ol>

<pre><code class="r">unzip(&quot;repdata-data-activity.zip&quot;)
activity&lt;-read.csv(&quot;activity.csv&quot;, na.strings = &quot;NA&quot;, sep=&quot;,&quot;)
</code></pre>

<ol>
<li>Process/transform the data (if necessary) into a format suitable for your analysis</li>
</ol>

<h2>What is mean total number of steps taken per day?</h2>

<ol>
<li>Make a histogram of the total number of steps taken each day</li>
</ol>

<pre><code class="r">steps.date &lt;- aggregate(steps ~ date, data = activity, FUN = sum)
barplot(steps.date$steps, names.arg = steps.date$date, xlab = &quot;date&quot;, ylab = &quot;steps - frequency&quot;, col=&quot;steelblue&quot;)
</code></pre>

<p><img src="data:image/png;base64,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" alt="plot of chunk unnamed-chunk-2"/> </p>

<ol>
<li>Calculate and report the mean and median total number of steps taken per day</li>
</ol>

<pre><code class="r">mean1&lt;-mean(steps.date$steps, na.rm=TRUE)

median1&lt;-median(steps.date$steps, na.rm=TRUE)
</code></pre>

<p>The mean of total number of steps taken per day is equal to 1.0766 &times; 10<sup>4</sup>  and median is equal to 10765.</p>

<h2>What is the average daily activity pattern?</h2>

<ol>
<li>Make a time series plot (i.e. type = &ldquo;l&rdquo;) of the 5-minute interval (x-axis) and the average number of steps taken, averaged across all days (y-axis)</li>
</ol>

<pre><code class="r">steps.interval &lt;- aggregate(steps ~ interval, data = activity, FUN = mean)
    plot(steps.interval, type = &quot;l&quot;, col=&quot;steelblue&quot;)
</code></pre>

<p><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAfgAAAH4CAMAAACR9g9NAAAAdVBMVEX9/v0AAAAAADkAAGUAOTkAOWUAOY8AZrU5AAA5ADk5AGU5OWU5OY85ZrU5j9pGgrRlAABlADllAGVlOQBltf2POQCPOTmPOWWPZgCPtY+P29qP2/21ZgC1/v3ajzna/rXa/tra/v39tWX924/9/rX9/tr9/v20Wb0MAAAAJ3RSTlP//////////////////////////////////////////////////wCDVpfZAAAACXBIWXMAAAsSAAALEgHS3X78AAAO6ElEQVR4nO3dDVvqRh6H4aK76p61jsdiu61iq0C+/0dcEwh5m8BMZoa8/J7nag+C8DeHG0iCwPklI8l+GXsBaJyAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXLQR+RVMuIXzAZSl1wIsGvGjAiwa8aMCLBrxowIsGvGjAiwa8aMCLpgdvxl6AaQS8aMHw24fil3y3G9/RYwV8USj8/nVdHH7dfXqOHivgi0Lhdy+bxqH76LECvoh7vGjB6/jdM+v4OcZWvWjAiya4O4d8nuDGHfB5CXbnHF+5PVbAF3GPF01wdw74PMGteuDzgBctxu7czdusnqsHPi/Gxt3+9Qn4uRVnd+79HviZFWl37uNfP4CfVRF2557yg4/u/hzwU46tetGAFw140eTgDb+QLwJeNOBFA1404EUDXjTgRQNeNEF45POAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140RThkc+Alw140YAXDXjRgBdNDd4Afwh40YAXDXjRgBcNeNGAFw140eTgT3+IB7xokvDIy8Eb4I8BLxrwogEvmiY88sCrBrxowIsGvGii8MgDLxrwogEvGvCiqcLLywfDbx9Webcb39GjBHxZKPz+dV0cft19eo4eJWP5SrNQ+N3LpnHoPnqUgC+Tvcerywev43fPs1rHW79UTG2r3vqlYsCLFmPjLn+0767igZ90EeCLDfrtr76jR8n0fK1XBPjt42djd25VFr500QO+LBj++eavP/J7/OPcdueAP5fDxt3+dXWffc1vdw74cy14qx74cy0ZXlseeNGAFy18q/6479bdugN+ygXf4/evT8NGjxLwZeEP9bufb4NGj5I5c0wr5XU88P0tDN6cPSoV8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBLxrwogEvGvCiAS8a8KIBL5o0vLI88KIBLxrwogEvGvCiAS8a8KIBL5ob/Mfd58dqtY46eoyAP+UEv/v59v3f9kf334gPGD1GwJ9yg3/ZfN/ngV9Sjg/1q5u3Lx7qlxQbd6JpwwvLu8HvX1er1X3c0WME/Ckn+MO/Ef/hKQ/8lHPdqj/9GW30GAF/ynGr/j7ru8dvH1Z5t90bxRzgdeXd7vHPq1UP7/71sJP3dffpOXqMgD8VulVfPv5b1gPAT7lQeO7xM815d+7u759vtnMcVwOs42eW6+7c9vHTcqcOGT1GwJ9y3Z37hl/i7ty14Kd3+/K4x39Y7/Hszg37wWPn8ZSt1Z2Nu4E/eOwS7M6tygIXLUFjwZuZwp95ynbu9/jryHvDp18qB/jT83bWx/o57c7Zrk7grdXv8ZFHjxDwVVIvxAC+Surl1cBXSb28Gviq0JdXn/mNLfDVD5kp/LmXVx9eljVg9AgBXxW+cbez/9ZumfADQRYJP3T0CAFfBXzwBJeLAT9qEeCHiQA/brOBN+nlgfebAHzw6BEKhh8KAvy4jQXvfTHg4wZ8FfB+A4APHj1CwFcB7zcA+ODRIwR8FfB+A4APHj1CwFcB7zfgavCp5YH3G5Ae3pT/m6T4wPsNuB588XU6e+D9BlwXPuHvZ4H3GwB88OgRAr4KeL8BA+E9Lgd8/ICvAt5vwLXhk8nLw3tds8BHGD1CI8I7X9C0biXARwj4KuBHh29+B/gEAV8FvB/8IAhPeAN85MaE778g8MkDvgr4seEN8MmbLLxpHAU+dhOA714c+PSNBG9qB07wQxfPJyV4++uYRodvPjsAfPxmAt/a2PP/eU4BPzX49u6d/89zSgi+5yWrV4PveQIP+NQBX08JfuSteuCvXHW9A1+lA9+HBrwt4NvnDYAvLt65PPCpMo2Dvm+7jgI+dPTVSgHvxXER3gCfogtUwNsCvn3exPCdlQnwg5sOfGb7pAvgU5UE3vNSp6+Av17m9Ef/t91HAR86OkX9O+pThs+AD80Ob3/G7Oxl+s8aBN/ZZs+Aj1Ja+NpDB/DDR6eoF/7M1ed8zdY3EoEfPjpFKeFN/cD7U236fxzwEUoIbxqHXs+vAZ+8dPCm+UUH/twU4JPXB+/McvlMffd455tW+zYCfIRSwZv2l5aHetf9Bgt853bluXhDWhR8z6spgbcE/ED47pq7dxDwqeuDd9/mvnyefvjeScCnzn7XvrDPHQpvGqc6/IDWLQb48GzEJjL8CcoC37Nxee64aT1WAD+kPvgLF3IZ3Pz6ivCp5JcNb4DvC/ih8HVsYzlf7w9YCPz2YZV3u/EdnSAL/IV9uSwKfLWhbt+4PHN8tvD713Vx+HX36Tk6QeHwPecFvtPuZdM4dB+doM4WfCT4zlmAn949vnW1At9T8Dp+9zytdfy14Y03fP0Ek80WfvDoBFngPbfq+577ax0x1cnAVyPLBi1QSDb4iy+Puwhv+fyxiPCtU2YDn2/U5Y/23VX8OPf45ktqiyOJ4TMTEd5y+enCFxv02199RyfoBG9OJ1wd3uEuuxT47ePnZHbnyhfR167QS1cc8LYuwz/f/PVHfo9/nMTuXBO+teHUe6H6EeCLHDbu9q+r++xrIrtzp7fNVOa+8BanHvisvJHVJXXgh45OkLH8fwX4+retb4rsnmKa3wQ+rDb4AHjL67RaJ8WAP57LmPZ5euGj8wM/Avzx9Vbdh3zgvWrcX+rbXkPgLavkBPC2oX0L6/S38G558KaxM+dx6eJIJHjLnbl5ntapwA+p9XyN11uYneA7F6h+oMls8LZH8f6BGfDDmhJ8yWSaJ5wdmAE/rInBmwa8bXMN+Di1nqGNDG/ZWqtUu7/+c4HvPwl4n6YIf3kHzXoS8D6Z+pXT3WK+fOnqyzMb3PVzNb4ZEd665MD3NS14MxzevuDG/+/kEPBB8MXxSPB9qyjLFmSEFgJ/+j/L/OFPl2u/ddU+zQ3+zKO3/aTepQa+r7nBn12Inu8Bb2nK8I7Lcs4V+L6GrdurS6eB99oaB35IwfDlnTMKfGNb09Xr3NmA70sA/uLbQrxbDPzg6yYyfO0m6HFbBH5IYfCn37eXt4BQ+NMZBj8IdcZdfgegd8uBH7waDIXvnAP4KxUH/vQoHxE+ilYLPtItAPh08JE2xU1tF/H004InLwg+cB1fh6+/mqML34VuHwf+KoXCZ034cuPeWFf5wIeOjlfglWAad/asDmed7g4fcx0PfLdk8Lbd+tHgG7dG4POSwneHe8BHqQ1vfxzybQHwodeBL7wF2jYwWsD3FB++vkU/HfjG0gEfAz6rnnIp/pwWfGv/AvgyAfjW45F9sfwCvg7fnmh/kf4E4MOfIQD+AvyABUgFf+SP82ta4IG3pQLfN2PQQ2oC+HJwBnxVhGt5JvCH/U5jgC9aPnzjq+O2nel+1yvgixG98IOmAX+VYsBHnZ0OvtwQBT5vcvCxXwQPvL0Jwg9ekEvjbPDDfhrwCUoMnwFftHj45mhTO8iGb1AAn6BrwJc/BPgJlXKJTOsr4CfUlZao9aDvF/AJutYSlc/nDGn+8NNzv94idX+x6Bzws671EVseAT/vgBfO92Obi4Cff8CLBrxowIsGvGiDPiEH+PmnCY/7sB154Ocf8KJ14R2uFODnXwfeZSsf+PnXgnd7Ly3w889kzRdkOm3kA7+MgBet/TariwG/jIAXDXjVGu+l61wp3WtpbvAOfyXNTP3w+Dar7ner5gffeq4ixQ+ZY1342oevW3bsZwhv7EfEs8AXX5nqz0azgjdt+Pj/VMtsO925j3801/ljwjtudJyr9dbwFP8q14wzjX/ksg5vu5qC4bcPq7zbzaXRprVAh2VtnyNrn6N23vIzHY3tjJRXfeptE757XYXC71/XxeHX3eel0Qe2xhq6/VTjcdnrn+9lytOymrpJ8Q9yLSnTvl47V1co/O5l0zjMR5Z1FsaU25oH3OJ4reOR43nLrxu3g+7thGw1rqjan1VXvMfTlApex++eHdfxNKlmtTtH8QJeNOBFA1404EUDXjTgRQNeNOBFA1404EVLCU9TLh18+3YQb1SigZKL2BPw0xoIfIqBkovYE/DTGgh8ioGSi9gT8NMaCHyKgZKL2FNEeJpTwIsGvGjAiwa8aMCLBrxowIsGvGjAixYLfve86r6PelAfq+KtuceBEeZuf2yy1riwqcXAiIuZf+bIOu4iXi4SfP4u+o/7KKPe17WBEeZ+5T7NcWFTi4ERF3P38y3b/uct5iI6FAk+/7yM4o4Q3P73t9rA8LnvN39+X745LmjqYWDExfzKfd/XERfRpUjw28fP4pYbXvE5DOtyYIy5+fXXHBc4NR8YeTE7yxbvCu0pEnz+QSlxlvP7QS+/Ox0HxpibOzXHBU4tbklRF3P/+hR3ES83uXt80ft66vf4qIu5e37K4i7i5Sa3ji9qr/GChm3jruMb8FEGbh/yDcV5ruPzx6o4G6H5Y9z+j81xYIy5+fXXHBc4tVx3RFrMg3vcRbzcJPfjb95i7s4m24+PtJgfxfte1vPcj6e5BbxowIsGvGjAiwa8aMCLBrxowIsGvGjAiwa8aMCLBrxowIsGvGjAiwa8aMCLBrxoovDVK5f7X8Oc9NXNoycKXwW8VN+o28f/rVbr3fPqdlP8kW3/+1v+iub972+H9y0Dv8By+Ifi/Wo573vx5oXtwzp/D+z28e/8fcvfZwB+eR1dDwf5e9R2L8UJH0/5f1lWHl9uwP/YFG95vnk7vLnyn/yN7+/5p10Av8Ca8C+b42nfK/g/Hz93z2se6hdaAz5fxx/X9tnH6ql8/zvwC6yC378WW/U3b4et+PwDD/K3Mf77tzXwtMCAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBcNeNGAFw140YAXDXjRgBft/5sH9iWCKEj1AAAAAElFTkSuQmCC" alt="plot of chunk unnamed-chunk-4"/> </p>

<p>Which 5-minute interval, on average across all the days in the dataset, contains the maximum number of steps?</p>

<pre><code class="r">maksimum&lt;-steps.interval$interval[which.max(steps.interval$steps)]
</code></pre>

<p>5-minute interval that on average across all the days in the dataset, contains the maximum number of steps is the 835 interval.</p>

<h2>Imputing missing values</h2>

<ol>
<li>Calculate and report the total number of missing values in the dataset (i.e. the total number of rows with NAs)</li>
</ol>

<pre><code class="r">braki&lt;- sum(!complete.cases(activity))
</code></pre>

<p>Number of missing values in the dataset is equal to 2304.</p>

<ol>
<li><p>Devise a strategy for filling in all of the missing values in the dataset. The strategy does not need to be sophisticated. For example, you could use the mean/median for that day, or the mean for that 5-minute interval, etc.</p></li>
<li><p>Create a new dataset that is equal to the original dataset but with the missing data filled in.</p></li>
</ol>

<pre><code class="r">activity &lt;- merge(activity, steps.interval, by = &quot;interval&quot;, suffixes = c(&quot;&quot;, 
    &quot;.y&quot;))
nas &lt;- is.na(activity$steps)
activity$steps[nas] &lt;- activity$steps.y[nas]
activity &lt;- activity[, c(1:3)]
</code></pre>

<ol>
<li>Make a histogram of the total number of steps taken each day and Calculate and report the mean and median total number of steps taken per day. Do these values differ from the estimates from the first part of the assignment? What is the impact of imputing missing data on the estimates of the total daily number of steps?</li>
</ol>

<pre><code class="r">steps.date &lt;- aggregate(steps ~ date, data = activity, FUN = sum)
barplot(steps.date$steps, names.arg = steps.date$date, xlab = &quot;date&quot;, ylab = &quot;steps&quot;, col=&quot;steelblue&quot;)
</code></pre>

<p><img src="data:image/png;base64,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" alt="plot of chunk unnamed-chunk-8"/> </p>

<pre><code class="r">mean2&lt;-mean(steps.date$steps, na.rm=TRUE)
median2&lt;-median(steps.date$steps, na.rm=TRUE)
</code></pre>

<p>New mean of total number of steps taken per day is equal to 1.0766 &times; 10<sup>4</sup>  and median is equal to 1.0766 &times; 10<sup>4</sup>.</p>

<h2>Are there differences in activity patterns between weekdays and weekends?</h2>

<ol>
<li>Create a new factor variable in the dataset with two levels – “weekday” and “weekend” indicating whether a given date is a weekday or weekend day.</li>
</ol>

<pre><code class="r">daytype &lt;- function(date) {
    if (weekdays(as.Date(date)) %in% c(&quot;Saturday&quot;, &quot;Sunday&quot;)) {
        &quot;weekend&quot;
    } else {
        &quot;weekday&quot;
    }
}
activity$daytype &lt;- as.factor(sapply(activity$date, daytype))
head(activity)
</code></pre>

<pre><code>##   interval steps       date daytype
## 1        0 1.717 2012-10-01 weekday
## 2        0 0.000 2012-11-23 weekday
## 3        0 0.000 2012-10-28 weekday
## 4        0 0.000 2012-11-06 weekday
## 5        0 0.000 2012-11-24 weekday
## 6        0 0.000 2012-11-15 weekday
</code></pre>

</body>

</html>

