# المساهمة في Mira Clinic

شكراً لاهتمامك بالمساهمة في مشروع Mira Clinic! نرحب بجميع المساهمات.

## قواعد المساهمة

### قبل البدء

1. **تحقق من القضايا المفتوحة (Issues)** - قد تجد أحد يعمل على نفس المشكلة
2. **اقرأ هذا الملف بالكامل** - للتأكد من أنك تتبع الإجراءات الصحيحة
3. **افتح Issue** - قبل البدء في عمل تغييرات كبيرة

### خطوات المساهمة

#### 1. استنساخ المستودع وإعداده

```bash
# استنسخ المستودع
git clone https://github.com/SDAIAAcademy/mira-clinic.git
cd mira-clinic

# أنشئ فرع جديد
git checkout -b feature/your-feature-name
# أو للإصلاحات
git checkout -b fix/bug-description
```

#### 2. إجراء التعديلات

- اتبع أسلوب الكود الموجود
- أضف تعليقات واضحة للكود المعقد
- اختبر التغييرات على متصفحات مختلفة

#### 3. Commit والـ Push

```bash
# أضف التغييرات
git add .

# أنشئ commit برسالة واضحة
git commit -m "feat: description of what you changed"
# أو
git commit -m "fix: description of the bug fix"

# ادفع التغييرات
git push origin your-branch-name
```

#### 4. فتح Pull Request

1. اذهب إلى [GitHub](https://github.com/SDAIAAcademy/mira-clinic)
2. انقر على "New Pull Request"
3. اختر فرعك
4. اكتب وصفاً واضحاً للتغييرات
5. انتظر المراجعة

## معايير الكود

### HTML/CSS/JavaScript

- استخدم تنسيق منسق والهوامش الصحيحة
- أضف tidy comments للأقسام الرئيسية
- تجنب الأخطاء الشائعة

### أسماء المتغيرات والدوال

```javascript
// ✅ جيد
const getUserData = () => { }
let isFormValid = true;

// ❌ سيء
const get_user_data = () => { }
let valid = true;
```

### التعليقات

```javascript
// ✅ جيد - تعليق واضح ومفيد
// تحويل التاريخ إلى صيغة YYYY-MM-DD
const formatDate = (date) => { }

// ❌ سيء - تعليق غير واضح
// تحويل التاريخ
const formatDate = (date) => { }
```

## رسائل الـ Commit

استخدم الصيغة التالية:

```
<type>: <subject>

<body>

<footer>
```

### Types

- `feat`: ميزة جديدة
- `fix`: إصلاح خطأ
- `docs`: تحديثات التوثيق
- `style`: تنسيق الكود
- `refactor`: إعادة هيكلة الكود
- `perf`: تحسينات الأداء
- `test`: إضافة أو تحديث الاختبارات

### أمثلة

```
feat: add appointment reminder notifications

- Implement email notifications for upcoming appointments
- Add notification preferences to user settings
- Send reminder 24 hours before appointment

Fixes #123
```

```
fix: resolve date picker not showing correct timezone

The date picker was displaying times in UTC instead of user's local timezone.
This fix ensures the correct timezone is applied.

Closes #456
```

## المراجعة والموافقة

- قد يطلب منك مراجعون تحديثات
- كن مرناً وتقبل الملاحظات البناءة
- قد تستغرق المراجعة بعض الوقت

## سلوك المجتمع

نتوقع من جميع المساهمين:

- ✅ أن يكونوا محترمين وحسني النية
- ✅ أن يقبلوا الانتقادات البناءة
- ✅ أن يركزوا على مصلحة المشروع

## الأسئلة والمساعدة

- 📧 **البريد الإلكتروني**: Academy@sdaia.gov.sa
- 💬 **المناقشات**: استخدم GitHub Discussions
- 🐛 **الأخطاء**: فتح Issue على GitHub

---

شكراً لمساهمتك! 🎉
