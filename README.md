<p align="center">
  <img alt="Jumplander Coder32b" src="https://img.shields.io/badge/JumpLander--Coder32b-%2300C853?style=for-the-badge&logo=github&logoColor=white" />
</p>

<p align="center">
  <strong>Jumplander Coder32b</strong> — یک مدل تخصصی برای تولید، بهینه‌سازی و ریفکتور کد (CodeLLM) که بخش مرکزی اکوسیستم <a href="https://jumplander.org/">Jumplander (جامپلندر)</a> است.
</p>

---

## 🔎 خلاصه
**Jumplander Coder32b** یک مدل زبانی طراحی‌شده برای وظایف مربوط به کدنویسی: تولید کد، تکمیل، دیباگ هوشمند، ریفکتور و تولید مستندات کد. این مدل بخشی از خانواده ابزارهای Jumplander است که در پلتفرم IDE و دستیار AI استفاده می‌شود.

---

## ✨ قابلیت‌های کلیدی
- تولید کد و تکمیل خودکار با توجه به context فایل و پروژه  
- رفع خطا و پیشنهاد ریفکتور هوشمند (Code Refactor & Fix)  
- تولید خودکار مستندات تابع/کلاس از روی سورس کد  
- API ساده برای ادغام با IDE/CI/CD  
- پشتیبانی از >40 زبان برنامه‌نویسی  

---

## 📦 ساختار ریپازیتوری
```
jumplander-coder32b/
├─ README.md
├─ model_card.md
├─ src/
│   └─ server.py         # نمونه API ساده
├─ demos/
│   └─ examples.md
├─ benchmarks/
│   ├─ run_mceval.sh
│   ├─ run_humaneval.sh
│   └─ results/          # خروجی‌ها و لاگ‌ها
├─ docs/
└─ LICENSE
```

---

## 🚀 Quickstart (نمونه محلی)
1. کلون:
```bash
git clone https://github.com/Osodyssey/jumplander-coder32b.git
cd jumplander-coder32b
```
2. نصب وابستگی‌ها (Python-based inference):
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
3. اجرای سرور دمو:
```bash
python src/server.py
# سپس باز کردن: http://localhost:8080/demo
```

---

## 🧪 مقایسه و بنچمارک — نمایش بصری
> نوار مقیاس نمونه‌ای برای نمایش عملکرد تقریبی **Jumplander Coder32b** نسبت به **Qwen2.5-Coder-32B** است. برای ادعای دقیق، بنچمارک‌های بازتولید شده لازم است.

<p align="center">
  <div style="width:600px; border-radius:6px; padding:10px; background:#fafafa; border:1px solid #eee;">
    <div style="font-weight:600; margin-bottom:6px;">مقایسه عملکرد (نمونه نمایش)</div>
    <div style="display:flex; gap:12px; align-items:center;">
      <div style="flex:1">
        <div style="font-size:12px; color:#555;">Jumplander Coder32b</div>
        <div style="height:18px; background:#e6f8ed; border-radius:9px; overflow:hidden;">
          <div style="width:92%; height:100%; background:#00c853;"></div>
        </div>
      </div>
      <div style="width:90px; text-align:center; font-weight:700;">≈ PARITY</div>
      <div style="flex:1">
        <div style="font-size:12px; color:#555;">Qwen2.5-Coder-32B</div>
        <div style="height:18px; background:#f0f7ff; border-radius:9px; overflow:hidden;">
          <div style="width:92%; height:100%; background:#1976d2;"></div>
        </div>
      </div>
    </div>
    <div style="font-size:11px; color:#666; margin-top:8px;">
      توضیح: نوارها نمونه‌ای برای نمایش تساوی عملکرد هستند. نتایج رسمی باید از بنچمارک‌های McEval / HumanEval استخراج و در پوشه <code>benchmarks/results</code> قرار گیرند.
    </div>
  </div>
</p>

---

## 📊 روش پیشنهادی بنچمارک
1. **McEval / MdEval** — پوشش زبان‌ها و تعمیر کد.  
2. **HumanEval** — برای توانایی تولید توابع.  
3. **Aider / Code Editing Benchmarks** — برای ویرایش و ریفکتور.  

نمونه اجرای McEval:
```bash
pip install mceval-runner
python benchmarks/run_mceval.py --model ./models/jumplander-coder32b --output benchmarks/results/mceval.json
```

---

## 🛡️ محدودیت‌ها و هشدارها
- مدل ممکن است کد اشتباه تولید کند؛ بازبینی انسانی الزامی است.  
- برای داده‌های حساس، از محیط sandbox و تست امنیتی استفاده کنید.  

---

## 📝 مشارکت
1. Issue باز کنید (موضوع یا باگ).  
2. قبل از PR، تست بنچمارک را اجرا و لاگ‌ها را پیوست کنید.  
3. قالب PR: `feat|fix|chore: توضیح کوتاه` + لینک به issue.  

---

## 🧾 منابع
- [صفحه اصلی Jumplander](https://jumplander.org/)  
- Qwen2.5-Coder-32B — مرجع مدل برای مقایسه
