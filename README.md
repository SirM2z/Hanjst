# Hanjst
Han JavaScript Template Language and Engine

Han is the surname of my wife, and one of the given names of my daughter and son.

Han is also Chinese in Pinyin, H��nr��n.

Hanjst is intentionally designed to stop further "Reinventing the wheel" for HTML template engines though it sounds ridiculous.

## Introduction

Hanjst is a JavaScript-based template language and its engine runs on client-side.

Hanjst can be written with logic expressions and it provides many similar powerful functions with backend templates.


### Features

+ Runtime in client-side, reduce computing render in server-side;

+ Language-independent, not-bound with backend scripts/languages;

+ Totally-isolated between MVC, data transfer with JSON;

+ Full-support template tags with built-in logic and customerized JavaScript functions;

+ No more tags languages to be learned, just JavaScript;

+ ....


### Installation

Put these codes at the end of &lt;body>, i.e. the last element of &lt;body>:

```javascript

<!-- other Hanjst template sentences -->

<!-- Hanjst codes begin -->
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 'IsDebug': true}; // optional
</script>
<script type="text/javascript" src="Hanjst.js" async></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->

</body>

<!-- other html sentences-->

</html>

```


### Simple Demo

Hanjst will be invoked by ***window.onload*** and the template sentences will be parsed automatically.

The target result page body will be refreshed and presented with interpreted contents.

Here is a few of short paragraphs written in Hanjst. 

```html

<div id="mynewscontentlist">
Features:
{foreach $newslist as $page}
    <ul>
        <li>
            <a href="{$newslist[$page]['href']}">{$newslist[$page]['title']}</a>
            {if $newslist[$page]['title'].length > 20}
                Length is too long.
            {else}
                Length is okay.
            {/if}
        </li>
    </ul>
{/foreach}
</div>

```

```html

<div id="anotherlistdiv">
Try to list an associative list:
{for var $k in $userlist}
    <li>
        Id: {$userlist[$k]['id']}, 
        Name: {$userlist[$k]['name'].substring(0, 20)}
    </li>
{/for}
</div>

```

```html

<div id="randnum"> 
Give random numbers:
{$i=0}
{while $i<5}
    <li> 
        line {$i} 
    </li>
	{$i++}
{/while}

</div>


```

```html
<p>
    <a href="#atag"{if $user['feedback'] eq "fb2"} class="fb2class"{/if}>
        This is a href.
    </a>
</p>

```


### Live Demo Page
-R/j2SP 

[Hanjst Online Demo](https://ufqi.com/dev/hanjst/Hanjst.demo.html)



---

---


# Hanjst
Han JavaScript ģ�����Լ�����


Han �������ӵ���(��), Ҳ�ǳ�����Ů���Ͷ��������е����ڡ�

Han Ҳ�����ġ����塱����˼��

Hanjst���������HTMLģ���������򲻶ϵء��������ӡ��Ļ����������������Щ���졣

## ����

Hanjst��һ�ֻ���JavaScript��ģ�����Լ��������棬�������ڿͻ��ˡ�

Hanjst�ܹ������߼����ƣ��ܹ�ʵ�����������ģ��������ͬ�Ĺ��ܡ�

### ����/����

+ Hanjst��ȫ�ͻ��˽�������ʡ�������˼�����Դ;

+ ģ�����Զ������������������Դ���κΰ󶨣�

+ �����MVC�����������JSON��ʽ���ݣ�

+ ����ģ�����Թ���ȫ֧�֣��������Ӷ�ǿ���JavaScript���������

+ ��ѧϰ�ɱ���ֱ��ʹ��JavaScript��дģ�����ԣ�

+ ....


### ��װ������

����������η�����HTMLҳ��� body Ԫ���У�ͨ��λ�� body �Ľ�����ǰ�� &lt;/body> .

```javascript

<!-- other Hanjst template sentences -->

<!-- Hanjst codes begin -->
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 'IsDebug': true}; // optional
</script>
<script type="text/javascript" src="Hanjst.js" async></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->

</body>

<!-- other html sentences-->

</html>

```

### ��ʾ��

Hanjst��HTMLҳ�����ʱ�� ***window.onload*** �Զ����á�ģ�����ᱻ�Զ����������ҳ�����ݻᱻ�Զ�ˢ�µ� body Ԫ����.

������һЩ Hanjst ��ʾ�����롣

(�μ�Ӣ�İ沿��)

### ����ʵ��
-R/j2SP 

[Hanjst Online Demo](https://ufqi.com/dev/hanjst/Hanjst.demo.html)