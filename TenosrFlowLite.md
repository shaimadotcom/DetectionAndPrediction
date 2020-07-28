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







<img src="https://github.com/shaimadotcom/TensorFlow/blob/master/screenshots/IMG_0378.jpg?raw=true" width="148" height="250">





<img src="https://github.com/shaimadotcom/TensorFlow/blob/master/screenshots/IMG_0374.jpg?raw=true" width="148" height="250">






<img src="https://github.com/shaimadotcom/TensorFlow/blob/master/screenshots/IMG_0375.jpg?raw=true" width="148" height="250">










