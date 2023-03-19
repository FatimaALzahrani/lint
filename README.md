# lint
## تنفيذي للمشروع النهائي لمنصة سطر بدورة lint 

### سؤال المشروع

#### *مشروع نهائي*

قم بتحميل المشروع الموجود في الرابط التالي: https://github.com/satrcodes/Lint

#### *المتطلبات*
:
قم بإضافة eslint في المشروع

قم بتشغيل eslint، وقم بتعديل على الكود مما يتوافق مع القواعد

اجعل قيمة الخاصية semi تساوي warning

 ### الحل
 ## 1- قم بإضافة eslint في المشروع

 بداخل Terminal نكتب الأمر التالي لتهيئة eslint :
 
    npx eslint --init 

#### بعد تنفيذ الأمر بيبدأ يسالنا عدة أسئلة:

##### السؤال الاول:
كيف تريد استخدام ESLint ؟ توجد ثلاثة خيارات :

أول خيار فقط يساعدك على التحقق بناء او صياغة الجملة.
ثاني خيار يساعدك في التحقق من صحة بناء الجملة والمساعدة في العثور على مشاكل في الأكواد البرمجية.
ثالث خيار يساعدك في التحقق من بناء الجملة، والعثور على مشكلة وفرض نمط على الكود.

    How would you like to use ESLint? … 
      To check syntax only
      To check syntax and find problems
    ❯ To check syntax, find problems, and enforce code style
    
باختيار الخيار الثالث To check syntax, find problems, and enforce code style وبعدها اضغط على Enter

##### السؤال الثاني :
ماهو modules المستخدم في المشروع؟

هذا السؤال يعتمد على مشروعك، تستطيع اختيار الخيار المناسب لمشروعك

    What type of modules does your project use? … 
     JavaScript modules (import/export)
     CommonJS (require/exports)
   ❯ None of these
   
   سوف أقوم باختيار الخيار الأخير وبعدها اضغط على Enter

##### السؤال الثالث :
ماهو framework المستخدم في المشروع؟

هذا السؤال يعتمد على مشروعك تستطيع اختيار الخيار المناسب لمشروعك

    Which framework does your project use? … 
     React
     Vue.js
   ❯ None of these
   
#### السؤال الرابع :
هل المشروع يستخدم TypeScript؟

هذا السؤال يعتمد على مشروعك، تستطيع اختيار الخيار المناسب لمشروعك

    ? Does your project use TypeScript? › No / Yes
سوف أقوم باختيار الخيار no وبعدها اضغط على Enter

##### السؤال الخامس :
أين تريد عمل run لكودك؟


    Where does your code run? …  (Press <space> to select, <a> to toggle all, <i> to invert selection)
    ✔ Browser
    ✔ Node
    
    نقدر نختار جميع الخيارات بالضغط على space إذا تغيرت علامة الصح إلى اللون الأخضر، يعني تم اختيار الخيار , وبعدها اضغط على Enter

##### السؤال السادس:
سوف يسأل عن style guide المراد استخدامها في المشروع؟

الخيار الأول استخدام إحدى style guides الشائعة.
الخيار الثاني سوف يسأل عده أسئلة بناءً على أجوبتك سوف ينشئ rules الخاصة بك.

     How would you like to define a style for your project? … 
     ❯ Use a popular style guide
       Answer questions about your style
          
سوف أقوم باختيار الخيار الاول Use a popular style guide وبعدها اضغط على Enter

بتطلع لنا أشهر اربعة style guides موجودة لمشاريع JavaScript نقدر نختيار style guides اللي تعجبنا ونتبعها 

     Which style guide do you want to follow? … 
      Airbnb: https://github.com/airbnb/javascript
      Standard: https://github.com/standard/standard
    ❯ Google: https://github.com/google/eslint-config-google
      XO: https://github.com/xojs/eslint-config-xo

سوف أقوم باختيار الخيار الثالث Google وبعدها اضغط على Enter

#### السؤال السابع :
هذا السؤال يسأل عن الامتداد الخاص بملف config الذي يحتوي على القواعد rules؟

يوجد ثلاثة اختيارات تستطيع اختيار أي امتداد يناسبك

     What format do you want your config file to be in? … 
       JavaScript
     ❯ YAML
       JSON
سوف أقوم باختيار الخيار الثاني YAML بسبب سهولة التعامل معها، وبعدها اضغط على Enter

#### السؤال الثامن :
هل تريد تحميله الآن ؟

    Would you like to install them now? › No / Yes

سوف اقوم باختيار الخيار Yes وبعدها اضغط على Enter

#### السؤال التاسع
ما هو package manager الذي تريد استخدامه؟

تستطيع اختيار ما يناسبك
     Which package manager do you want to use? … 
     ❯ npm
       yarn
       pnpm
       
سوف أقوم باختيار الخيار الأول npm وبعدها اضغط على Enter

##### بنلاحظ انه انشئ لي ملف باسم eslintrc.yaml هذا الملف هو config الذي يحتوي على rules.
#### بتكون القواعد منشئة حسب الاجابات على الاسئلة السابقة وفيه مكان جوة اقواس ال rule نقدر نكتب قواعد زيادة.

## 2- اجعل قيمة الخاصية semi تساوي warning
#### بنروح لملف .eslintrc.yml اللي توه انشئه لي وبنكتب جوة rule التالي :
    rules: {
    semi : warn
    }

## قم بتشغيل eslint، وقم بتعديل على الكود مما يتوافق مع القواعد
في البداية هذي الاخطاء اللي تظهر :
<img width="960" alt="2023-03-19 (1)" src="https://user-images.githubusercontent.com/107775566/226177612-534a208b-efa7-4cdd-bae0-88b19068dcc1.png">
فبنكتب الامر التالي لاصالح اي شي يمكن اصلاحه تلقائيا :

    npx eslint --fix index.js
    
الان اصبحت الاخطاء كالتالي ويجب اصلاحها يدويا
<img width="960" alt="2023-03-19 (2)" src="https://user-images.githubusercontent.com/107775566/226177685-20eacd1f-8345-4619-b1b4-ee9896e09b76.png">
فالخطأ الاول ان اسماء المتغيرات تكون بال camel case واللي يكون اول كلمة بالصغير وبعدين كل اول حرف من الكلمة الجديدة يكون كابيتل , فبتصير 
    my_name  ->  myName

الخطأين الثانيه سببهم اننا عرفنا متغيرين وما استخدمناهم , فالحل يا اما نحذف المتغيرين او نستخدمهم وانا قررت استخدمهم باني اطبعهم

    console.log(myName);
    console.log(list);
    
    <img width="960" alt="2023-03-19 (3)" src="https://user-images.githubusercontent.com/107775566/226179153-cc75bb67-cb89-40ad-9e88-c1058cc0b9e1.png">
فهذا الخطأ هو اللي اضناه بالخطوه الثانية واللي سببه ان لازم نهاية كل امر يكون فيه فاصله منقوطة 
وبعد اظافة الفواصل المنقوطة نهاية جميع الاوامر لن يظهر اي اخطاء :) 
<img width="960" alt="2023-03-19 (8)" src="https://user-images.githubusercontent.com/107775566/226179639-564f6b22-1916-4584-9f4a-8ec9c29f3d87.png">
