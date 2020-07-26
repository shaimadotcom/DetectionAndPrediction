# <p align="center">tf.keras</p>

### <div dir="rtl">*tf.keras* هو مستوى عالي من واجهة برمجة التطبيقات وهنا سندرب شبكة عصوبنية لتتعرف على صور لقطع من ملابس متنوعة</div>

====================================================================================

#### <div dir="rtl">سنستخدم اصدار تنسرفلو 2.0.0 وبعض المكتبات المساعدة</div> 
``` 
import tensorflow as tf
from tensorflow import keras

import numpy as np
import matplotlib.pyplot as plt
 ```

#### <div dir="rtl">سنستخدم مجموعة البيانات المزودة من قاعدة MNIST</div>
``` 
fashion_mnist = keras.datasets.fashion_mnist

(train_images, train_labels), (test_images, test_labels) = fashion_mnist.load_data()

 ```
 #### <div dir="rtl"> ويجب أن تقسم البيانات لقسمين "بيانات تدريب"و "وبيانات إختبار" </div>
 
 #### <div dir="rtl">يتم تعيين اسم واحد لكل صورة (وتوجد9صور) ويتم حفظها "كمتغير" حتّى نتمكّن من إستخدامها لاحقا عند رسم النتائج أو البيانات أو الصّور</div>
 ``` 
class_names = ['T-shirt/top', 'Trouser', 'Pullover', 'Dress', 'Coat',
               'Sandal', 'Shirt', 'Sneaker', 'Bag', 'Ankle boot']


 ```
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
  ###### <div dir="rtl">ساستخدم خوارزمية ادم لانه يحقق نتائج جيدة بسرعة</div>
  ==========================================================================
   
  #### <div dir="rtl">تدريب النموذج لشبكة عصبية يتطلب منك إطعام "بيانات التدريب"  للنموذج ليتعلم العلاقة بين المسميات والصور</div>
  ```model.fit(train_images, train_labels, epochs=10)```
  
   ###### <div dir="rtl">و الان يبدأ التدريب</div>
  
