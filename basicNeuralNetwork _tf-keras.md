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
 
 #### <div dir="rtl">يتم تعيين اسم واحد لكل صورة (وتوجد9صور) ويتم حفظها "كمتغير" حتّى نتمكّن من إستخدامها لاحقا عند رسم النتائج أو البيانات أو الصّور</div>
 ``` 
class_names = ['T-shirt/top', 'Trouser', 'Pullover', 'Dress', 'Coat',
               'Sandal', 'Shirt', 'Sneaker', 'Bag', 'Ankle boot']


 ```
 
 
