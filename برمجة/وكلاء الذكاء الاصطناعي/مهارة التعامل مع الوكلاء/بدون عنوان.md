ازاي تستخدم Claude Code بـ 1.6 مليار Token في الشهر… وببلاش؟ 🔥

من كام يوم جربت Tool اسمها OmniRoute فكرتها إنها بتخليك تستخدم Claude Code مع موديلات موجودة على OpenRouter والـ Tool بتعمل Routing بين الموديلات بشكل تلقائي.

حسب الـ Setup الحالي اللي انا جربته بقى عندي Access على أكتر من 640 Model ومع الموديلات المجانية الموجودة على OpenRouter ممكن توصل لاستخدام ضخم جدًا شهريا بدل ما تقف كل شويه بسبب الـ Limits.

فـ قولت أشارك معاكم الطريقة من أول الـ Setup لحد ما تشغل Claude 👇

=================================

أول حاجة لازم يكون عندك Node.js و npm.

بعد كده افتح الـ Terminal واكتب:

npm install -g omniroute

كده الـ Tool هتتنزل Global عندك على الجهاز.

=================================
بعد كده اعمل Setup

اكتب:

omniroute setup

هيبدأ معاك الـ Setup.

اختار:

OpenRouter

كـ Provider.

بعدها هيطلب منك الـ API Key.

=================================
طب هتجيب OpenRouter API Key منين؟

اعمل Account على OpenRouter وبعدها ادخل على صفحة الـ API Keys:

https://openrouter.ai/workspaces/default/keys

واعمل Create API Key

وخد الـ Key وحطه في الـ Terminal لما OmniRoute تطلبه منك.

وبكده أنت ربطت OmniRoute بـ OpenRouter.

=================================
بعد ما تخلص الـ Setup اكتب:

omniroute serve

OmniRoute هتشغل Server عندك Local.

وهتديك Dashboard تقدر تفتحها من البروزر.

أول مرة هتدخل عليها هيطلب منك Password.

الـ Default Password هو:

CHANGEME

وطبعًا الأفضل تغيره بعد كده.

=================================
و الـ Dashboard من خلالها تقدر تتابع:

ـ الـ Requests اللي بتطلع من Claude
ـ الموديلات اللي بيتم استخدامها
ـ استهلاك الـ Tokens
ـ حالة الـ Providers
ـ الـ Routing بين الموديلات

يعني بدل ما تكون شغال ومش عارف Claude بيستخدم إيه أو استهلك قد إيه، كل حاجة بتكون قدامك.

================================
 وبعد كده أستخدم Claude Code عادي بقا 

بعد ما OmniRoute تشتغل وتكون عامل الـ Setup صح بتسطب وتشغل Claude Code لكن بدل ما الـ Requests تروح بشكل مباشر للموديل الأساسي، OmniRoute بتبقى هي الطبقة اللي في النص وبتتعامل مع الـ Routing.

ودي أكتر نقطة عجبتني في الموضوع.

لأنك مش مربوط بموديل واحد وخلاص.

أنا جربت الطريقة وحبيت أشاركها خصوصًا مع الناس اللي شغلها تقيل على Claude Code وبتخلص الـ Limits بسرعة.