## اختر الموضوع الخاص بك

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
في هذه الخطوة ، ستضيف شخصية وخلفية ، وستنشئ منصات بداية ونهاية. 
</div>
<div>
![](images/setup-example.png){:width="300px"}
</div>
</div>

--- task ---

افتح [مشروع Scratch جديد](http://rpf.io/scratch-new){: "target = "_ blank} واحذف كائن القط. سيتم فتح Scratch في علامة تبويب متصفح أخرى.

--- /task ---

--- task ---

إنشاء خلفية ملونة صلبة.

[[[scratch-paint-single-colour-backdrop]]]

--- /task ---

--- task ---

** اختر: ** هل ستنتقل شخصيتك من اليسار إلى اليمين, أم من الأسفل إلى الأعلى؟

![](images/direction-examples.png)

--- /task ---

--- task ---

قم برسم ** ابدأ ** كائن منصة جديد .

ابدأ بشكل بسيط بلون واحد. You can turn the outline off by choosing the red diagonal line.

![](images/no-outline.png)

يمكنك إضافة المزيد من التفاصيل في وقت لاحق.

قم بتوسيط المظهر في محرر الرسام.

[[[scratch-crosshair]]]

ضع كائن المنصة **ابدأ ** حيث تريد أن تبدأ شخصيتك اللعبة.

--- /task ---

--- task ---

إنشاء ** النهاية ** كائن منصة بسيط. يمكنك إضافة المزيد من التفاصيل في وقت لاحق.

قم بتوسيط المظهر في محرر الرسام.

ضع كائنك **النهاية** على المنصة حيث تريد أن تنهي شخصيتك اللعبة.

--- /task ---

--- task ---

أنشئ **شخصية** الكائن.

**اختر:** هل تريد إضافة أو رسم كائن مكون من **شخصية** الكائن ؟

قد ترغب في إضافة من أعلى لأسفل **شخصية** مثل الكائن **تاتيانا**, **تايلور**, او **تريشا**.

![صورة من أعلى إلى أسفل للكائنات متاحة في scratch](images/top-down-sprites.png)

أو ارسم كائنًا واحدًا مكونًا من **شخصية** الكائن. ابدأ بأشكال بسيطة وأضف التفاصيل لاحقًا. قم بتوسيط المظهر في محرر الرسام.

[[[generic-scratch3-draw-sprite]]]

--- /task ---

--- task ---

يحتاج كائن **شخصيتك** نص بداية لبدء التهيئة لبداية اللعبة.

Make a `variable`{:class="block3variables"} called `landed`, and set it to the size your sprite should be when it has landed and is not jumping.

Get your character to go to the **Start** `when flag clicked`{:class="block3events"}. Add a `go to front layer`{:class="block3looks"} block, so your character is on top of the platforms.

**Character:**

```blocks3
when flag clicked // setup
go to (Start v)
set [landed v] to [40] // size when not jumping
set size to (landed) % // not jumping
go to [front v] layer
show
broadcast (start v) // start other scripts
```

**Tip:** Uncheck the `landed`{:class="block3variables"} variable in the `Variables`{:class="block3variables"} Blocks menu so that it doesn't show on the Stage. The user doesn't need to see this variable.

**نصيحة:** إنها فكرة جيدة أن تقوم `بث`{: "class="block3events} رسالة `بدء`{:" class="block3events} في نهاية البرنامج النصي للإعداد للسماح للنصوص الأخرى بمعرفة وقت البدء، وإلا قد يبدأون قبل أن يصبح كل شيء جاهزًا.

--- /task ---

--- task ---

**التصحيح:**

--- collapse ---

---
title: الكائن الخاص بي يشير في الاتجاه الخاطئ
---

يمكن استخدام خاصية **اتجاه** في جزء الكائن للتحكم في الاتجاه الذي يشير إليه الكائن. لف العجلة لعمل نقطة كائن في الاتجاه الذي تريده.

![جزء الكائن مع تحديد خاصية الاتجاه. تظهر قائمة منبثقة مع عجلة اتجاه تستخدم لضبط الاتجاه الذي يشير إليه الكائن.](images/direction-property.png)

--- /collapse ---

--- /task ---

--- task ---

امنح مشروعك عنوانًا يصف لعبتك.

--- /task ---

--- save ---
