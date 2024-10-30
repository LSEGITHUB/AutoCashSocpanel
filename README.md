# AutoCash

يعمل هذا المشروع على دمج نموذج HTML بسيط مع JavaScript للتعامل مع المدفوعات التلقائية في socpanel باستخدام مكتبة AutoCash.

## المتطلبات

- Panel Id -> من التطبيق

## التثبيت

1. قم بدخول الى لوحة تحكم فى socpanel ثم API و قم بأخذ التوكن و اضفه فى التطبيق واكمل بيانات لوحة التحكم .
2. اضف كود html التالى فى طرق الدفع .
```html

<style>
   .form-group input {
        width: 100%;
        background-color: #F1F7FC;
        border-color: #C3DAEB;
        font-weight: inherit;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
        border-bottom-left-radius: 8px;
        border-bottom-right-radius: 8px;
        border-left-width: 0px;
        border-right-width: 0px;
        border-top-width: 0px;
        border-bottom-width: 2px;
        border-style: solid;
        text-align: right;
        color: #000;
   }

   button {
        color: #fff;
        background-color: #007bff;
        border-color: #007bff;
        width: 100%;      box-shadow: none;
        outline: none;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
        border-bottom-left-radius: 8px;
        border-bottom-right-radius: 8px;
        padding: 5px;
        font-weight: bolder;
   }

    .alert{
        margin-bottom: 0px;
        text-align: center;
        font-weight: 600;
        font-style: bold;
        padding-top: 12px;
        padding-left: 12px;
        padding-right: 24px;
        padding-bottom: 12px;
        border: 2px solid yellow;
        border-radius: 10px;
   }

    .alert-danger {
        color: #C81919;
        background: rgba(200, 25, 25, 0.2);
        border-color: red;
    }

    .alert-primary {
        color: #26a25e;
        background: rgba(25, 200, 104, 0.2);
        border-color: yellow;
    }
</style>

<div id="message"></div>
<center>
<p style=""><img src="https://smm.darksidehost.com/soc/Code_VF-img.png" style="display: inline-block; width: 265px; max-width: 100%;" class="img-responsive"></p>
<p style=""><font color="#008000">سعر الايداع اليوم</font><br></p>
<p style=""><b><font color="#008000">( 1<span id="storecurrencyname"></span> = <span id="rate"></span> <span id="yourcurrencyname">جنية</span> )</font></b></p>
<br>
<p style="">أرقام المحافظ الخاصه بنا:<br></p>
<span id="storenumbers"></span>

<hr>
<p style="">1. ارسل المبلغ الي رقم فودافون كاش المذكور في الاعلي أولا</p>
<p style="">2. قم بكتابه الرقم الخاص بك الذي قمت بالتحويل لنا من خلاله في الخانه المطلوبه</p>
<p style="">3. اكتب المبلغ الذي قمت بتحويله في الخانه المطلوبه</p>
<p style=""><font color="#008000">4. اضغط علي زر الدفع</font><br><br></p>
<p style=""><font color="#ff9c00">اذا فشل الايداع عليك الانتظار لمدة 5 دقائق ثم حاول مره اخري</font><br></p>
<div>في حالة <b><font color="#ff0000">واجهت اي مشاكل</font></b>, <a href="/support/dialog" target="_blank"><font color="#ff9c00">قم بفتح تذكره دعم جديده</font></a>
<br><br></div>

</center>

<form onsubmit="event.preventDefault(); PaymentCheck();">
        <div class="form-group" style="display: block;text-align: right;padding-bottom: 20px;">
            <label><span>الرقم الخاص بك</span></label>
            <input class="form-control" value="" placeholder="01000000000" type="text" id="walletphone" oninput="this.value = this.value.replace(/[^0-9]/g, '')" inputmode="numeric" autocomplete="off" required="">
        </div>
        <div class="form-group" style="display: block;text-align: right">
            <label><span>المبلغ الذي ارسلته ( بالجنيه المصري )</span></label>
            <input class="form-control" value="" type="number" id="walletamount" autocomplete="off" step="0.01" required="">
        </div>
<br>
<input type="hidden" id="langpayment" value="ar">
<button type="submit" id="payButton" class="btn btn-block btn-big-primary">دفع</button>
</form>
```
3. ادخل إلى integerations ثم other ثم اضف الكود التالى بعد تغير Your_Panel_ID بمعرف لوحة تحكم .
```html
<script data-panel-id="Your_Panel_ID" src="https://smm.darksidehost.com/soc/soc.js"></script>
```
4. اكتمل التثبيت بنجاح ^_^ .


