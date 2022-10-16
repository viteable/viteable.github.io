## دليل نسخ النصوص باستخدام جافا سكربت

سنتعلم في هذه المقالة كيفية نسخ النصوص أو الصور باستخدام جافا سكربت Clipboard API.

لأنك مستعجل هذا السكربت الخاص بالنسخ:

```js
<p id="thetext">مرحبا بالعالم</p>
<button onclick="copyText()">نسخ!</button>

<script>
  let text = document.getElementById('thetext').innerHTML;
  const copyText = async () => {
    try {
      await navigator.clipboard.writeText(text);
      console.log('تم نسخ النص بنجاح');
    } catch (err) {
      console.error('حدث مشكلة اثناء نسخ النص: ', err);
    }
  }
</script>
```
