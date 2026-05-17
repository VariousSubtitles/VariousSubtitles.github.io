---
layout: default
title: Various Subtitles
---

<style>
body{
  background:#111;
  color:#eee;
  font-family:sans-serif;
}

a{
  color:#8dbdff;
  text-decoration:none;
}

.container{
  max-width:1100px;
  margin:auto;
  padding:20px;
}

.header{
  background:#1b1b1b;
  border:1px solid #333;
  border-radius:16px;
  padding:30px;
  margin-bottom:20px;
}

.title{
  font-size:40px;
  font-weight:bold;
}

.subtitle{
  color:#aaa;
  margin-top:10px;
}

.nav{
  margin-top:20px;
  display:flex;
  gap:10px;
  flex-wrap:wrap;
}

.nav a{
  background:#222;
  border:1px solid #333;
  padding:10px 16px;
  border-radius:10px;
}

.layout{
  display:grid;
  grid-template-columns:2fr 1fr;
  gap:20px;
}

.card{
  background:#1b1b1b;
  border:1px solid #333;
  border-radius:16px;
  padding:20px;
  margin-bottom:20px;
}

.post{
  border-bottom:1px solid #333;
  padding:14px 0;
}

.post:last-child{
  border:none;
}

.comment{
  color:#999;
  font-size:14px;
}

.form input,
.form textarea,
.form select{
  width:100%;
  background:#111;
  border:1px solid #333;
  color:#eee;
  padding:12px;
  border-radius:10px;
  margin-top:10px;
  margin-bottom:15px;
}

.form button{
  background:#2b6fff;
  color:white;
  border:none;
  padding:12px 20px;
  border-radius:10px;
  cursor:pointer;
}

@media(max-width:900px){
  .layout{
    grid-template-columns:1fr;
  }
}
</style>

<div class="container">

<div class="header">
<div class="title">
Various Subtitles
</div>

<div class="subtitle">
Multi-language Subtitle Project
</div>

<div class="nav">
<a href="/">ホーム</a>
<a href="#blog">ブログ</a>
<a href="#about">説明</a>
<a href="#form">字幕追加フォーム</a>
</div>
</div>

<div class="layout">

<div>

<div class="card" id="blog">
<h2>ブログ</h2>

{% for post in site.posts %}

<div class="post">
<h3>
<a href="{{ post.url }}">
{{ post.title }}
</a>
</h3>

<div class="comment">
コメントあり
</div>
</div>

{% endfor %}

</div>

<div class="card" id="about">
<h2>説明 (仮)</h2>

<p>
Various Subtitles は、
多言語字幕制作を行うプロジェクトです。
</p>

<p>
字幕制作協力者も募集しています。
</p>

<p>
翻訳・校正・タイミング調整など、
興味がある方はぜひご参加ください。
</p>

</div>

</div>

<div>

<div class="card" id="form">
<h2>字幕追加フォーム</h2>

<form
class="form"
action="https://formspree.io/f/xxxxxxxx"
method="POST"
>

<label>メールアドレス:</label>
<input type="email" name="email">

<label>内容:</label>

<select name="type">
<option>字幕追加</option>
<option>字幕修正</option>
<option>翻訳協力</option>
<option>その他</option>
</select>

<label>メッセージ(具体的内容):</label>

<textarea
name="message"
rows="8"
></textarea>

<button type="submit">
送信
</button>

</form>

</div>

<div class="card">
<h2>コメント</h2>

<script src="https://giscus.app/client.js"
        data-repo="VariousSubtitles/VariousSubtitles.github.io"
        data-repo-id="REPOSITORY_ID"
        data-category="General"
        data-category-id="CATEGORY_ID"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="dark"
        data-lang="ja"
        crossorigin="anonymous"
        async>
</script>

<p style="color:#888;font-size:14px;">
※ 後でgiscus設定が必要です
</p>

</div>

</div>

</div>

</div>
