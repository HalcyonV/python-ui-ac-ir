---
layout: default
title: "جزوه جلسه ۱"
---

<div dir="rtl">

# جزوه جلسه ۱

## ۳. نمایش و خواندن فایل Markdown
🔹 **روش سریع:**  
- فایل را در **VS Code** یا **Typora** باز کنید تا فرمت Markdown را با استایل زیبا ببینید.  
- در **GitHub** آپلود کنید تا آنلاین و زیبا نمایش داده شود.  
- در **Obsidian** یا **Zettlr** برای مطالعه شخصی باز کنید.  

🔹 **روش آنلاین:**  
- فایل `.md` را در سایت‌هایی مثل **[Dillinger](https://dillinger.io/)** ببینید.  
- می‌توانید در **Google Colab** نیز متن را در **Markdown Cell** قرار دهید.

---

## ۴. اجرای کد پایتون در مرورگر 🚀
### **۱. اجرای کد در Google Colab**
برای اجرای این کد در Google Colab، روی دکمه زیر کلیک کنید:

[![اجرا در Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HalcyonV/python-ui-ac-ir/blob/main/session-1.ipynb)

---

### **۲. اجرای کد پایتون مستقیم در این صفحه**
کد زیر را تایپ کنید و روی دکمه **"اجرا کن"** کلیک کنید:

<textarea id="python-code" rows="5" cols="50">
print("سلام! این کد در مرورگر اجرا شده است!")
</textarea>
<br>
<button onclick="runPython()">اجرا کن</button>
<pre id="output"></pre>

</div>

<script src="https://cdn.jsdelivr.net/pyodide/v0.22.0/full/pyodide.js"></script>
<script>
  async function main() {
      window.pyodide = await loadPyodide();
  }
  main();
  
  async function runPython() {
      let code = document.getElementById("python-code").value;
      let output = await pyodide.runPythonAsync(code);
      document.getElementById("output").innerText = output;
  }
</script>
