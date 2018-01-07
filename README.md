<h1> SFLS-1(Blackfrog-language) 规范 </h1>

<blockquote class="todo"> ToC here </blockquote>

<h2> 0. 概述 </h2>

SFLS-1
<i>（下称
    <b>Blackfrog 或 BF</b> ）</i> 是一门函数化的面向对象高级程序设计语言
<b>概念，它目前没有编译或解释实现</b>。根据 [Zoran Chen](https://github.com/black-frog-language) 的提议， BF 的核心思想是
<b>哲学</b>。

<h2> 1. 编写 </h2>

BF 源文件应该使用 UTF-8 编写，并遵循 BF 规范，否则可能产生不可预料的问题。BF 文件可以经过编译或解释
<i>（下称
    <b>解析</b>）</i> 来得到可在一（1）个或更多计算机平台运行的版本。 BF 源文件的推荐后缀名为
<code>.bf</code> 。
<blockquote class="example">
    将 BF 源文件的后缀名设定为
    <code>.js</code> ,可能会使编辑器、解释器将其当作
    <i>JavaScript/ECMAScript</i> 解读。
</blockquote>

<h2> 2. 解析 </h2>

<b>解析</b>意指将程序转化为更底层的语言。解析器分为两种：解释器与编译器。
<br> 解释器与编译器应具有如下功能：
<ul>
    <li>可以运行程序，或将程序转换为可以在一（1）个或更多计算机平台上运行的版本；</li>
    <li>拥有完整的开发调试（性能监测，错误记录，终端（即 <i>Ribbit 或 Blackfrog-cli</i> 等）环境</li>
    <li>可以在解析过程中发现错误与疑点。</li>
    <li>支持 SFLS-3（Blackfrog-Contain）中规定的最低 Blackfrog 要求版本。</li>
    <li>支持 SFLS-3（Blackfrog-Contain）中规定的最低 Blackfrog 标准库（即 SFLS-2, aka Blackfrog-lib）要求版本。</li>
</ul>

<h2> 3. 词法及语法 </h2>

BF 的词法有 3 种：
<ul>
    <li>函数(function abbr fn)： 标准调用方式为<code><b>fn</b>(<b>arg1</b>, <i>arg2, ..., argn</i>)</code></li>
    <li>运算符(opreator abbr op)： 标准调用方式为：
        <ul>
            <li>右值一元：<code><b>opreator valueR</b></code></li>
            <li>左值一元（尚未在标准中出现）：<code><b>valueL opreator</b></code></li>
            <li>二元：<code><b>valueL opreator valueR</b></code></li>
            <li>n元：<code><b>value1 opreator value2 opreator ... opreator valuen</b></code></li>
        </ul>
    </li>
    <li></li>
</ul>

<blockquote class="example">
    计算机平台，可能为 Windows，Linux，UNIX（macOS）等。
</blockquote>

<h2>额外资料</h2>

<!-- Do NOT change the lines under. -->

<div class="background">BLACKFROG<br>standard</div>


<!-- Styles. DO NOT CHANGE. -->
<style>
    body {
        background: #ddd !important;
        color: #444 !important;
    }

    blockquote {
        margin-top: 0;
        background: rgba(0, 0, 0, 0.1) !important;
        border-left: solid 5px gray !important;
    }

    code {
        color: #002 !important;
    }

    pre {
        display: block;
        padding: 2em;
        background: rgba(0, 0, 0, 0.1) !important;
        border-radius: 5px;
    }

    blockquote.example {
        border-left-color: green !important;
    }

    blockquote.example::before {
        display: block;
        content: 'For Example';
        font-style: italic;
        color: green;
    }

    blockquote.todo {
        border-left-color: pink !important;
    }

    blockquote.todo::before {
        display: block;
        content: 'Todo';
        font-style: italic;
        color: pink;
    }



    div.background {
        font-family: 'Courier New', Courier, monospace;
        font-size: 2em;
        padding: 1em;
        background: black;
        color: white;
        opacity: 0.1;
        position: fixed;
        top: 40%;
        left: 40%;
        text-align: center;
    }
</style>