  تجربة واجهات برمجة التطبيقات (API)

 الهدف
التعرّف على طريقة جلب البيانات من الإنترنت باستخدام JavaScript وواجهات برمجة التطبيقات (API).
 


ما يحدث في الصفحة
1. عند الضغط على زر **"عرض المنشور"** يرسل الكود طلبًا إلى خادم خارجي.  
2. يستخدم الكود **fetch()** لجلب بيانات من واجهة عامة.  
3. الخادم يعيد بيانات بصيغة **JSON** (عنوان + محتوى).  
4. الصفحة تعرض هذه البيانات على الشاشة.  
5. إذا حدث خطأ، تظهر رسالة تنبيه للمستخدم.

## فكرة التجربة
- **API** هي طريقة لتبادل البيانات بين البرامج والمواقع.  
- **fetch()** تجعل الصفحة تتصل بخادم آخر دون إعادة التحميل.  
- يمكن تعديل الرابط لجلب بيانات مختلفة.

---

  تمارين للطلاب

 التمرين 1
غيّر الرقم في هذا السطر من الكود:
```javascript
fetch('https://jsonplaceholder.typicode.com/posts/1')


بدّل الرابط بالكامل لتجربة واجهة مختلفة:



fetch('https://jsonplaceholder.typicode.com/users/1')ثم عدّل عرض النتيجة ليُظهر:



ثم عدّل عرض النتيجة ليُظهر:

"الاسم: " + data.name + "\n\n" + "البريد: " + data.email







لكود البرمجي المستخدم ضمن ملف جديد اسمه  index.html :
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>تجربة API بسيطة</title>
</head>
<body>
  <h2>تجربة واجهة برمجة التطبيقات (API)</h2>
  <button id="load">عرض المنشور</button>
  <pre id="result"></pre>

  <script>
    document.getElementById('load').onclick = async function() {
      const response = await fetch('https://jsonplaceholder.typicode.com/users/3');
      const data = await response.json();
      document.getElementById('result').textContent = 
       "الاسم: " + data.name + "\n\n" + "البريد: " + data.email
    };
  </script>
</body>
</html>




ا
