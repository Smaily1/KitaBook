# متجر الكتب KitaBook
متجر كتب بسيط كمشروع تخرج وتطبيق للمعارف التي تم التطرق إليها في الدورة يحتوي على صفحة رئيسية وصفحة خاصة بكل كتاب بإمكان المستخدم إضافة كتب أو كتابة مراجعات وإضافة تقييمات للكتاب ، كل كتاب لديه متوسط عدد التقييمات بناءا على عدد التقيمات التي تم إضافتها بالإضافة لكل من عنوان الكتاب ، إسم المؤلف ، وصف الكتاب ، رمز ISBN ، و أخيرا سعر الكتاب . بإمكان الزائر إقتناء الكتاب المرغوب عبر زر الباي بال أو استعمال أحد بطاقات الدفع الالكترونية.

> التطبيق عبارة عن إطار عمل بسيط لمتجر بشكل عام لذالك بإمكانك إستعماله لعرض أي نوع من السلع وبيعها.


**صفحة العرض الرئيسية :**


![الصفحة الرئيسية للتطبيق](https://i.suar.me/nBrmg/l)

**صفحة العرض الخاصة بكل كتاب صفحة العرض الخاصة بالكتاب :**


![الصفحة الرئيسية للتطبيق](https://i.suar.me/2YwN9/l)

**صفحة إضافة كتاب صفحة إضافة كتاب جديد:**


![الصفحة الرئيسية للتطبيق](https://i.suar.me/MBgl9/l)


## Gems : المستعملة في المشروع
- simple_form
- devise
- bootstrap-sass
- jquery-rails
- paperclip
- Rating system from https://www.wbotelhos.com/raty

> ملاحظة : من أجل أن تعمل الإضافة `paperclip` في تطبيقك عليك تنصيب أداة تدعى [image magick](https://imagemagick.org/) في حاسوبك، بعد تنصيبها ومن أجل التأكد من عملها أكتب الأمر التالي في موجه الأوامر لديك `which convert` وسيظرهر لك في المخرجات مسار تنصيبها شيئ مثل `/usr/local/bin/convert` بعدها من أجل ربط paperclip بالأداة image magic توجه إلى الملف `config/environments/development.rb` وأضف الأمر التالي :
````bash
Paperclip.options[:command_path] = "/usr/local/bin/"
````
## نسخ روبي وريلز المستعملة :
- `Ruby 2.7.5`
- `Rails 5.2.7`
## طريقة التشغيل :

- قم بعمل استنساخ Clone للمشروع على حاسوبك باستخدام الأمر :
````bash
git clone git@github.com:smaily1/kitabook.git
````
- قم بالدخول لمجلد المشروع باستعمال الأمر `cd bookstore` بعدها ولتنصيب الـ Gems الموجودة بالمشروع قم بتشغيل الأمر :
````bash
bundle install
````
- ثم مرحلة التهجير وبناء الجداول في قاعدة البيانات قم بتشغيل الأمر :
````bash
rails db:migrate
````
- هذه المرحلة اختيارية بإمكانك تشغيل الخادم مباشرة أو القيام بعملية Seed أو زرع لمستخدم بمرتبة مدير مع بعض أمثلة الأصناف والكتب التي أضفتها في التطبيق كي لايظهر لديك بشكل فارغ وذلك عبر تشغيل الأمر :
````bash
rails db:seed 
````
- ثم عليك الدخول بحساب المدير لتعديلها بعد ذلك وإضافة غلافات الكتب .

> معلومات الدخول لحساب المدير الافتراضي هي : 
> -  username: "Admin",
> - email: "admin@bookstore.com",
> - password: "azerty",

- أخيرا لتشغيل التطبيق قم بكتابة الأمر :
````bash
> rails server 
````
بعدها ستجد أن التطبيق يعمل لديك على الرابط `http://localhost:3000`

## ملاحظات :

حاليا أواجه هذه المشاكل لذا سأسعد بأية اقتراحات يتم إرسالها عبر Pull Request :

- أود إضافة خاصية Shoping Cart بحيث تسمح بإضافة أكثر من منتج إلى السلة و طلب صفحة الشراء مرة واحدة مع إمكانية شراء أكثر من نسخة لنفس المنتج لكن لاأدري هل هناك خدمة دفع تقدم هذه الصفحة أم علي إنشائها يدويا وكيف تظهر لائحة المنتجات المختارة عند إعادة التوجيه لصفحة الدفع الخاصة بالباي بال.
- أود إرسال رسالة نجاح عملية الشراء للمستخدم بعد إتمام عملية الشراء.
- لازلت أحاول إيجاد حل لربط التطبيق بطرف الثالث من أجل رفع صور أغلفة الكتب عليه كون النسخة المجانية من Heroku لاتسمح بذلك لو يوجد هناك شرح فيديو للعملية لاتتردد في ارساله .
> أية اقتراحات أخرى سأكون سعيدا بإضافتها للتطبيق شكرا .

