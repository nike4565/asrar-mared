# دليل المساهمة في أسرار المارد 🤝

شكراً لاهتمامك بالمساهمة في **أسرار المارد**! نرحب بكل المساهمات سواء كانت كبيرة أو صغيرة.

---

## 🚀 كيف تساهم؟

### 1️⃣ الإبلاغ عن الأخطاء 🐛

**قبل الإبلاغ:**
- ✅ تأكد أن المشكلة لم تُبلغ من قبل
- ✅ استخدم أحدث إصدار (v6.0.0 🐆)
- ✅ جرب على بيئة نظيفة

**عند الإبلاغ:**
- 📝 استخدم [قالب Bug Report](../../issues/new?template=bug_report.md)
- 📸 أرفق لقطات شاشة
- 💻 اذكر بيئة التشغيل
- 🔄 اشرح خطوات إعادة الإنتاج

---

### 2️⃣ اقتراح ميزة جديدة ✨

**قبل الاقتراح:**
- 🔍 تحقق من [خارطة الطريق](https://github.com/nike4949/asrar-mared/projects)
- 💬 ناقش الفكرة في [Discussions](https://github.com/nike4949/asrar-mared/discussions)

**عند الاقتراح:**
- 📝 استخدم [قالب Feature Request](../../issues/new?template=feature_request.md)
- 🎯 اشرح المشكلة التي تحلها
- 💡 قدم أمثلة واضحة
- 📊 اذكر الفوائد المتوقعة

---

### 3️⃣ المساهمة بالكود 💻

#### خطوات المساهمة:

```bash
# 1. Fork المشروع
# اضغط زر Fork في أعلى الصفحة

# 2. استنسخ نسختك
git clone https://github.com/YOUR-USERNAME/asrar-mared.git
cd asrar-mared

# 3. أنشئ فرع جديد
git checkout -b feature/amazing-feature
# أو
git checkout -b fix/bug-name

# 4. ثبت المتطلبات
npm install

# 5. اعمل تغييراتك
# اكتب كود نظيف ومنظم

# 6. اختبر التغييرات
npm test

# 7. Commit التغييرات
git add .
git commit -m "feat: إضافة ميزة رائعة"

# 8. Push للفرع
git push origin feature/amazing-feature

# 9. افتح Pull Request
# اذهب لصفحة GitHub وافتح PR
```

---

## 📋 معايير الكود

### قواعد البرمجة:

**JavaScript/Node.js:**
```javascript
// ✅ جيد - واضح ومنظم
function calculateTotal(items) {
    return items.reduce((sum, item) => sum + item.price, 0);
}

// ❌ سيء - غير واضح
function ct(i) {
    let t=0;for(let x of i)t+=x.p;return t;
}
```

**Python:**
```python
# ✅ جيد
def encrypt_data(data: str, key: str) -> str:
    """تشفير البيانات باستخدام المفتاح المحدد"""
    return cipher.encrypt(data, key)

# ❌ سيء
def ed(d,k):
    return cipher.encrypt(d,k)
```

### المبادئ الأساسية:
- 📝 **تعليقات واضحة** بالعربية أو الإنجليزية
- 🎯 **أسماء معبرة** للمتغيرات والدوال
- 🧪 **اختبارات شاملة** لكل ميزة
- 📚 **توثيق كامل** للـ API
- ♻️ **كود قابل لإعادة الاستخدام**

---

## 💬 رسائل Commit

نستخدم [Conventional Commits](https://www.conventionalcommits.org/):

```bash
# الأنواع المقبولة:
feat:     # ميزة جديدة
fix:      # إصلاح خطأ
docs:     # تحديث التوثيق
style:    # تنسيق الكود
refactor: # إعادة هيكلة
test:     # إضافة اختبارات
chore:    # مهام صيانة
perf:     # تحسين الأداء
security: # إصلاح أمني

# أمثلة:
feat: إضافة نظام التشفير المتقدم
fix: حل مشكلة تسريب الذاكرة
docs: تحديث دليل الاستخدام
security: إصلاح ثغرة XSS في API
```

---

## 🧪 الاختبارات

**قبل إرسال PR:**
```bash
# تشغيل جميع الاختبارات
npm test

# فحص التغطية
npm run test:coverage

# فحص الكود
npm run lint

# إصلاح التنسيق
npm run format
```

**متطلبات الاختبار:**
- ✅ تغطية 80%+ للكود الجديد
- ✅ جميع الاختبارات تنجح
- ✅ لا أخطاء في Linting

---

## 📝 Pull Request

### قبل إرسال PR:
- ✅ تأكد أن الفرع محدث مع `main`
- ✅ كل الاختبارات تنجح
- ✅ لا conflicts في الكود
- ✅ التوثيق محدث

### قالب PR:
```markdown
## 📋 الوصف
وصف مختصر للتغييرات

## 🎯 نوع التغيير
- [ ] ميزة جديدة
- [ ] إصلاح خطأ
- [ ] تحسين أداء
- [ ] تحديث توثيق

## ✅ Checklist
- [ ] الكود يتبع معايير المشروع
- [ ] اختبارات شاملة مضافة
- [ ] التوثيق محدث
- [ ] جميع الاختبارات تنجح

## 📸 لقطات الشاشة
(إن وجدت)

## 🔗 Issues المرتبطة
Closes #123
```

---

## 🏷️ Labels

نستخدم هذه التصنيفات:

| Label | الوصف |
|-------|-------|
| `bug` | خطأ في الكود |
| `enhancement` | ميزة جديدة |
| `documentation` | تحسين التوثيق |
| `good first issue` | مناسب للمبتدئين |
| `help wanted` | نحتاج مساعدة |
| `priority: high` | أولوية عالية |
| `security` | قضايا أمنية |
| `wontfix` | لن يُصلح |

---

## 👥 المراجعة

**عملية المراجعة:**
1. 👀 مراجع واحد على الأقل يوافق
2. ✅ CI/CD يمر بنجاح
3. 💬 الرد على جميع التعليقات
4. 🔄 تحديث حسب المطلوب
5. ✨ الدمج بعد الموافقة

**ما نبحث عنه:**
- 🎯 الكود يحل المشكلة المحددة
- 🧹 نظافة وتنظيم الكود
- 🧪 اختبارات شاملة
- 📚 توثيق واضح
- 🔒 لا مشاكل أمنية

---

## 🌍 المجتمع

### قنوات التواصل:

- 💬 **GitHub Discussions:** [نقاشات عامة](https://github.com/nike4949/asrar-mared/discussions)
- 🐛 **Issues:** [بلاغات ومقترحات](https://github.com/nike4949/asrar-mared/issues)
- 📧 **Email:** asrar-mared@proton.me
- 🌐 **Website:** [g.dev/nike4949](https://g.dev/nike4949)

### آداب التعامل:
- 🤝 احترم الجميع
- 💬 كن بناءً في النقد
- 🎯 ركز على الحل
- ❤️ كن صبوراً ومتعاوناً
- 📖 اقرأ [قواعد السلوك](CODE_OF_CONDUCT.md)

---

## 🎁 المساهمات الأخرى

**لست مبرمج؟ يمكنك المساهمة بـ:**

- 📝 **كتابة التوثيق** - تحسين الشروحات
- 🌐 **الترجمة** - ترجمة للغات أخرى
- 🎨 **التصميم** - تحسين الواجهات
- 🧪 **الاختبار** - اختبار الميزات الجديدة
- 📢 **الترويج** - نشر المشروع
- 💰 **الدعم المالي** - [Buy Me a Coffee](https://buymeacoffee.com/nike4949)

---

## 📚 موارد مفيدة

### للمبتدئين:
- 📖 [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- 🎓 [First Contributions](https://github.com/firstcontributions/first-contributions)
- 💻 [GitHub Docs](https://docs.github.com/)

### للمتقدمين:
- 🔐 [الأمن السيبراني](https://github.com/nike4949/asrar-mared/wiki/Security)
- 🏗️ [معمارية المشروع](https://github.com/nike4949/asrar-mared/wiki/Architecture)
- 🚀 [دليل الأداء](https://github.com/nike4949/asrar-mared/wiki/Performance)

---

## ❓ الأسئلة الشائعة

**س: كم يستغرق مراجعة PR؟**  
ج: عادة 2-3 أيام عمل.

**س: هل يمكنني العمل على أي Issue؟**  
ج: نعم! إلا إذا كان مُسند لشخص آخر.

**س: كيف أصبح Maintainer؟**  
ج: بالمساهمة المستمرة والجودة العالية.

**س: هل تقبلون مساهمات بالعربية؟**  
ج: نعم! نرحب بالعربية والإنجليزية.

---

## 🎖️ شكراً للمساهمين

جميع المساهمين يُضافون لـ:
- 📜 [قائمة الشكر](https://github.com/nike4949/asrar-mared#contributors)
- 🏆 [Hall of Fame](https://github.com/nike4949/asrar-mared/wiki/Contributors)

---

<div align="center">

## 🚀 جاهز للبدء؟

**ابدأ بـ Issues المناسبة للمبتدئين:**

[![Good First Issues](https://img.shields.io/github/issues/nike4949/asrar-mared/good%20first%20issue?color=7057ff&label=Good%20First%20Issues)](https://github.com/nike4949/asrar-mared/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)

---

**شكراً لك على المساهمة في أسرار المارد! 🐆**

*معاً نجعل الإنترنت أكثر أماناً* 🛡️

**v6.0.0 Cheetah Release**

</div>
```
