---
layout: default
title: NMLibrary's page
access-counter: true
---
# 設定
### アクセスカウンターの表示設定
下のアクセスカウンターは、実はこのサイト全体で動いています。
「表示する」にすると、全ページでカウンターが表示されます。
<script type="text/javascript">
  function save(){
    const button_true = document.getElementById("show-counter-true");
    const button_false = document.getElementById("show-counter-false");
    if (button_true.checked){
      localStorage.setItem("show-counter", true);
    }
    if (button_false.checked){
      localStorage.setItem("show-counter", false);
    }
  }
  function initialize(){
    const button_true = document.getElementById("show-counter-true");
    const button_false = document.getElementById("show-counter-false");
    if (localStorage.getItem("show-counter") === "true"){
      button_true.checked = true;
    } else {
      button_false.checked = true;
    }
 }
 document.addEventListener("DOMContentLoaded", initialize);
</script>

<div>
  <input type="radio" name="show-counter" value="true" id="show-counter-true" onchange="save()" />
  <label for="show-counter-true">表示する</label>  <br/>
  <input type="radio" name="show-counter" value="false" id="show-counter-false" onchange="save()" />
  <label for="show-counter-false">表示しない</label> <br/>
</div>