# <p align="center">tf.keras</p>

### <div dir="rtl">*tf.keras* هو مستوى عالي من واجهة برمجة التطبيقات وهنا سندرب شبكة عصوبنية لتتعرف على صور لقطع من ملابس متنوعة</div>

===============================================================================

#### <div dir="rtl">سنستخدم اصدار تنسرفلو 2.0.0 وبعض المكتبات المساعدة</div> 
``` 
import tensorflow as tf
from tensorflow import keras

import numpy as np
import matplotlib.pyplot as plt
 ```

#### <div dir="rtl">سنستخدم مجموعة البيانات المزودة من قاعدة MNIST</div>
#### <div dir="rtl">و التّي تعتبر المثال الأوّل، أو مثال "مرحبا يا عالم"</div> 
 
``` 
fashion_mnist = keras.datasets.fashion_mnist

(train_images, train_labels), (test_images, test_labels) = fashion_mnist.load_data()

 ```

 ![سكرين](https://github.com/shaimadotcom/TensorFlow/blob/master/screenshots/Screenshot%20(26).png?raw=true)
  
 #### <div dir="rtl"> ويجب أن تقسم البيانات لقسمين كماهو موضح "بيانات تدريب"و "وبيانات إختبار"</div>
  #### <div dir="rtl">و التقسيم يكون عبارة عن 20% من الصور في قسم الاختبار و80% في التدريب</div> 
 
 #### <div dir="rtl">يتم تعيين اسم واحد لكل صورة (وتوجد9صور) ويتم حفظها "كمتغير" حتّى نتمكّن من إستخدامها لاحقا عند رسم النتائج أو البيانات أو الصّور</div>
 
 ![alt text](https://www.tensorflow.org/tutorials/keras/classification_files/output_oZTImqg_CaW1_0.png?hl=ar)
 #### <div dir="rtl">قبل البدأ بالتدريب يجب خفض قيمة البكسلات من نطاقها الحاليّ من 0 إلى 255 وذلك بقسمتها على 255</div>
 ``` 
train_images = train_images / 255.0

test_images = test_images / 255.0

 ```
 
  #### <div dir="rtl">لنبني نموذج يجب تعديل الطبقات النموذج ثم تجميعها</div>
 ``` 
model = keras.Sequential([
    keras.layers.Flatten(input_shape=(28, 28)),
    keras.layers.Dense(128, activation='relu'),
    keras.layers.Dense(10)
])

model.compile(optimizer='adam',
              loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
              metrics=['accuracy'])

 ```
 ![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/Screenshot%20(27).png?token=AP3ATLDOMRYRD5C5UARX2CK7DWKWG)
  ###### <div dir="rtl">ساستخدم خوارزمية ادم لانه يحقق نتائج جيدة بسرعة</div>
  ==========================================================================
   
  #### <div dir="rtl">تدريب النموذج لشبكة عصبية يتطلب منك إطعام "بيانات التدريب"  للنموذج ليتعلم العلاقة بين المسميات والصور</div>
  ```model.fit(train_images, train_labels, epochs=10)```
  
   ###### <div dir="rtl">و الان يبدأ التدريب</div>
  
![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/Screenshot%20(4).png?token=AP3ATLFOWS3ZC7JOBDI5VW27DWATO)

   ###### <div dir="rtl">بعد أن ينتهي التدريب نقيس فعالية تدريب النموذج باستخدام بيانات الإختبار </div>
   ```test_loss, test_acc = model.evaluate(test_images,  test_labels, verbose=2)```

```print('\nTest accuracy:', test_acc) ```


  ###### <div dir="rtl">يمكنك الان بعد انهاء تدريب نموذجك أن تجعله يقوم بتنبأت وكل تنبؤ  يكون داخل صفيفة متكوّن من 10 أرقام. و هي تمثّل مدى ثقة النموذج بأنّ الصورة تتوافق مع كل صورة و تسميتها</div>
```predictions = probability_model.predict(test_images)```

 ## <div dir="rtl">تجربة النموذج </div>
![سكرين](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/Screenshot%20(29).png?token=AP3ATLCOPWIXWO56YKMAUUK7DWLJ2)
 #### <div dir="rtl">لبدأ التجربة فقط أكتب الأمر التالي و سيبدأ بإظهار صورة مع المسمى اللذي تنبأ به و تحت الصورة سيظهر المسمى الصحيح وكل ماعليك فعله هو النقر على علامة x </div>
 #### <div dir="rtl">وستظهر لك صورة جديدة و تستطيع تكرار هذا لين تطفش ثم تستطيع إنهاء التجربة </div>
 
 ![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/screenshot%20(5).jpg?token=AP3ATLD3J7CYILB5CSF54327DWMSC)
 ![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/screenshot%20(2).jpg?token=AP3ATLFPREZNPDKZENC6QKS7DWMUS)
 ![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/screenshot%20(3).jpg?token=AP3ATLAAM2MHV5745DIEW427DWMXO)
 ![meh](https://raw.githubusercontent.com/shaimadotcom/TensorFlow/master/screenshots/screenshot%20(4).jpg?token=AP3ATLGRHOXVPKPWVIINJS27DWM5G)

