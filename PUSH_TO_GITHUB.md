# 📋 خطوات رفع المشروع إلى GitHub

## المتطلبات

- ✅ حساب GitHub نشط
- ✅ Git مثبت على جهازك
- ✅ وصول إلى organization SDAIA Academy (أو أنشئ repo جديد)

---

## الخطوة 1: إعداد المستودع المحلي

المستودع محضر بالفعل ويحتوي على:
- ✅ `.git` directory
- ✅ Initial commit مع الملفات الأساسية
- ✅ `.gitignore` لتجنب ملفات غير مهمة
- ✅ `LICENSE` (MIT)
- ✅ `CONTRIBUTING.md` لإرشادات المساهمة
- ✅ `README.md` مفصل

**تحقق من الحالة:**
```bash
cd "c:\Users\pc\OneDrive\المستندات\مشروع كلاود"
git status
git log --oneline
```

---

## الخطوة 2: إنشاء مستودع جديد على GitHub

### الطريقة 1️⃣: على github.com/SDAIAAcademy (للأعضاء)

1. اذهب إلى https://github.com/organizations/SDAIAAcademy/repositories
2. انقر على "New repository"
3. اسم المستودع: `mira-clinic`
4. الوصف: `Advanced appointment system for clinics and medical centers`
5. اختر `Public` أو `Private` حسب الحاجة
6. **لا تختر** "Initialize this repository with"
7. انقر `Create repository`

### الطريقة 2️⃣: على حسابك الشخصي

1. اذهب إلى https://github.com/new
2. اسم المستودع: `mira-clinic`
3. الباقي كما هو أعلاه

---

## الخطوة 3: إضافة Remote وتحديث البيانات

**للمستودع في organization SDAIA:**
```bash
cd "c:\Users\pc\OneDrive\المستندات\مشروع كلاود"
git remote add origin https://github.com/SDAIAAcademy/mira-clinic.git
git branch -M main
git push -u origin main
```

**للحساب الشخصي:**
```bash
cd "c:\Users\pc\OneDrive\المستندات\مشروع كلاود"
git remote add origin https://github.com/YOUR_USERNAME/mira-clinic.git
git branch -M main
git push -u origin main
```

---

## الخطوة 4: المصادقة

إذا طلب منك GitHub كلمة مرور:

### الخيار 1: استخدام GitHub CLI
```bash
gh auth login
# اتبع التعليمات
```

### الخيار 2: استخدام Personal Access Token
1. اذهب إلى https://github.com/settings/tokens
2. انقر `Generate new token`
3. اختر `repo` و `user` scopes
4. انسخ الـ token
5. استخدمه كلكلمة مرور عند الطلب

### الخيار 3: إعداد SSH
```bash
# إنشاء مفتاح SSH
ssh-keygen -t ed25519 -C "your-email@example.com"

# إضافة المفتاح إلى GitHub
# 1. اذهب إلى https://github.com/settings/keys
# 2. انقر "New SSH key"
# 3. انسخ محتوى ~/.ssh/id_ed25519.pub
```

---

## الخطوة 5: التحقق من النجاح

```bash
# تحقق من الـ remote
git remote -v

# يجب أن يظهر:
# origin  https://github.com/SDAIAAcademy/mira-clinic.git (fetch)
# origin  https://github.com/SDAIAAcademy/mira-clinic.git (push)
```

---

## الخطوة 6: إضافة حماية الفرع (اختياري)

لحماية الفرع `main`:

1. اذهب إلى Settings > Branches
2. تحت "Branch protection rules"، انقر "Add rule"
3. الفرع: `main`
4. اختر:
   - ✅ Require pull request reviews before merging
   - ✅ Require status checks to pass before merging
   - ✅ Require branches to be up to date before merging

---

## الخطوة 7: إضافة Topics (اختياري)

في صفحة المستودع > About:

أضف topics مثل:
- `clinic-management`
- `appointment-system`
- `healthcare`
- `javascript`
- `html5`
- `saudi-arabia`

---

## الخطوة 8: إضافة GitHub Actions (اختياري)

إنشاء ملف `.github/workflows/checks.yml`:

```yaml
name: Code Quality Checks

on: [push, pull_request]

jobs:
  checks:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: echo "Running tests..."
```

---

## ✅ قائمة التحقق النهائية

- [ ] المستودع تم إنشاؤه على GitHub
- [ ] تم إضافة remote صحيح
- [ ] تم الـ push بنجاح
- [ ] الملفات ظاهرة على GitHub
- [ ] README.md يظهر بشكل صحيح
- [ ] الـ LICENSE ظاهر
- [ ] اختياري: حماية الفرع مفعلة
- [ ] اختياري: Topics تم إضافتها

---

## 🆘 استكشاف الأخطاء

### خطأ: "remote origin already exists"
```bash
git remote remove origin
# ثم أضف remote جديد
```

### خطأ: "Permission denied"
```bash
# استخدم SSH بدلاً من HTTPS
git remote set-url origin git@github.com:SDAIAAcademy/mira-clinic.git
```

### خطأ: "Repository not found"
- تأكد من اسم المستودع
- تأكد من وصولك إلى organization

---

## 📞 المساعدة

- 📧 Academy@sdaia.gov.sa
- 🐙 GitHub Issues
- 📚 [GitHub Docs](https://docs.github.com)

---

**آخر تحديث**: 2026-08-18
