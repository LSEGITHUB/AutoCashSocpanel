# AutoCash

يعمل هذا المشروع على دمج نموذج HTML بسيط مع JavaScript للتعامل مع المدفوعات التلقائية في socpanel باستخدام مكتبة AutoCash.

## المتطلبات

- Panel Id -> من التطبيق

## التثبيت

1. قم بدخول الى لوحة تحكم فى socpanel ثم API و قم بأخذ التوكن و اضفه فى التطبيق واكمل بيانات لوحة التحكم .
2. اضف كود html التالى فى طرق الدفع .
```html
<div id="autocash"> </div>
```
3. ادخل إلى integerations ثم other ثم اضف الكود التالى بعد تغير Your_Panel_ID بمعرف لوحة تحكم .
```html
<script data-panel-id="Your_Panel_ID" src="https://smm.darksidehost.com/soc/soc.js"></script>
```
4. اكتمل التثبيت بنجاح ^_^ .


