# <p align="center">Tensorflow Lite</p>


### <div dir="rtl">تنسورفلو لايت" عبارة عن إطار عمل للتعلم العميق مفتوح المصدر يحول نموذج مدرب في "تنسورفلو" إلى بنية خاصة يمكن تحسينها, وتلك البنية الخاصة  للأجهزة المتطورة والهواتف المحمولة</div>



##### <div dir="rtl">لهذا الشرح سأستخدم مثال ios </div>

## <div dir="rtl">المتطلبات</div> 
#### <div dir="rtl">1.  تحديث نظام الاي او اس الي اخر تصدير موجود</div>
####  <div dir="rtl">2. حساب فعال في المطور ابل</div>
####  <div dir="rtl">3.بيئة تطوير codeX or VS </div>
####  <div dir="rtl">4. cocopods</div>
####  <div dir="rtl">5. مكتبة تنسرفلولايت</div>


=====================================================================================

## <div dir="rtl">بناء التطبيق</div> 
#### <div dir="rtl">1. ثبتcocoapods</div>
####  <div dir="rtl">2. [استنساخ مستودع تنسرفلولايت](https://github.com/tensorflow/examples/tree/master/lite/examples/object_detection/ios)</div>
####  <div dir="rtl">3.ثم ثبت وحدث pods </div>
###### <div dir="rtl"> فتح تنسرفلولايت في كود اكس </div>
```use_frameworks pod 'TensorFlowLiteSwift```

####  <div dir="rtl">4.اذهب لبيئة التطوير و اربط جهازك الايفون فيها حيث أن التطبيق يحتاج جهاز مزود بكاميرا و إلا لن يعمل</div>
####  <div dir="rtl">5.اذهب للكونفيقريشن وعدل التعريف حيث يجب أن يكون مميز</div>
####  <div dir="rtl">6. عندما تبدأ بتشغيله سيطلب منك السماح بالدخول الى حسابك في مطورابل ثم يجب أن تسمح له أيضابالدخول الى الايتونز والسماح له باستخدام كاميرة هاتفك </div>

====================================================================







<img src="https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/IMG_0378.jpg?token=AP3ATLESQOBI7J2RXRX6XQS7DW4FC" width="297" height="420">

<img src="https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/IMG_0374.jpg?token=AP3ATLEHHQPAZBBLDOINAEK7DW4CC" width="148" height="220">

<img src="https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/IMG_0375.jpg?token=AP3ATLED2FRAE5DMKXKMCNK7DW4FY" width="148" height="220">










###### مثال الاندرويد -بالنسبة لي- يبدوا أفضل واقل تعقيد 
 
