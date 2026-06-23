<div dir="rtl">

<div align="center">

# پچ RTL برای Claude Desktop

**پشتیبانی کامل از فارسی و عربی (راست‌به‌چپ) برای Claude Desktop در ویندوز و macOS**

متن RTL را به‌صورت خودکار شناسایی می‌کند، جهت را در لحظه تنظیم می‌کند و متن فارسی را با فونت **وزیرمتن** نمایش می‌دهد — بدون اینکه متن انگلیسی یا بلوک‌های کد خراب شوند.

**[English](README.en.md)** · **[مخزن GitHub](https://github.com/mhghotbi/claude-desktop-rtl-patch)**

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform: Windows](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D6.svg)](#-نیازمندی‌ها)
[![Platform: macOS](https://img.shields.io/badge/platform-macOS-lightgrey.svg)](#-نصب-سریع--macos)
[![PowerShell 5.1+](https://img.shields.io/badge/PowerShell-5.1%2B-5391FE.svg)](#-نیازمندی‌ها)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#-مشارکت)
[![GitHub stars](https://img.shields.io/github/stars/mhghotbi/claude-desktop-rtl-patch?style=social)](https://github.com/mhghotbi/claude-desktop-rtl-patch/stargazers)

</div>

---

## فهرست

<table dir="rtl">
<tr>
<td align="center" dir="rtl"><a href="#-قابلیت‌ها">✨ قابلیت‌ها</a></td>
<td align="center" dir="rtl"><a href="#-نصب-سریع--windows">🚀 نصب ویندوز</a></td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="#-نصب-سریع--macos">🍎 نصب macOS</a></td>
<td align="center" dir="rtl"><a href="#-نیازمندی‌ها">📋 نیازمندی‌ها</a></td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="#️-گزینه‌های-منو">🎛️ گزینه‌های منو</a></td>
<td align="center" dir="rtl"><a href="#-ماندگاری-پچ-پس-از-به‌روزرسانی-ویندوز">🔄 ماندگاری پس از به‌روزرسانی</a></td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="#️-حذف">🗑️ حذف</a></td>
<td align="center" dir="rtl"><a href="#️-عیب‌یابی">🛠️ عیب‌یابی</a></td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="#️-سلب-مسئولیت">⚠️ سلب مسئولیت</a></td>
<td align="center" dir="rtl"><a href="#-مشارکت">🤝 مشارکت</a></td>
</tr>
</table>

---

## ✨ قابلیت‌ها

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">قابلیت</th>
<th align="center" dir="rtl">توضیح</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl">🔍 <b>شناسایی خودکار RTL</b></td>
<td align="center" dir="rtl">در پاسخ‌های Claude و کادر ورودی، با تنظیم جهت در لحظه — حتی در حین دریافت پاسخ</td>
</tr>
<tr>
<td align="center" dir="rtl">🔤 <b>فونت وزیرمتن</b></td>
<td align="center" dir="rtl">فونت متغیر و مدرن برای فارسی و عربی، به‌صورت data URI تعبیه‌شده (بدون نیاز به اینترنت)</td>
</tr>
<tr>
<td align="center" dir="rtl">💻 <b>کد، ریاضی و جدول</b></td>
<td align="center" dir="rtl">بلوک‌های کد و LaTeX (<code dir="ltr">$x^2$</code>) در محیط RTL چپ‌به‌راست می‌مانند؛ جداول فارسی راست‌به‌چپ</td>
</tr>
<tr>
<td align="center" dir="rtl">🪟 <b>رفع باگ پنجره</b></td>
<td align="center" dir="rtl">وقتی زبان ویندوز فارسی یا عربی است، رابط Claude Desktop به‌اشتباه RTL می‌شود — این پچ آن را برطرف می‌کند</td>
</tr>
<tr>
<td align="center" dir="rtl">💾 <b>پشتیبان‌گیری</b></td>
<td align="center" dir="rtl">از همه فایل‌ها قبل از هر تغییر، با بازگشت خودکار در صورت بروز خطا</td>
</tr>
<tr>
<td align="center" dir="rtl">🔄 <b>ماندگاری</b></td>
<td align="center" dir="rtl">پس از به‌روزرسانی Claude (اختیاری)، از طریق میانبر دسکتاپ یا به‌روزرسانی خودکار</td>
</tr>
</tbody>
</table>

<div dir="rtl">

> [!NOTE]
> در ویندوزی که زبان نمایش آن فارسی یا عربی است، رابط پنجره Claude Desktop به‌طور خودکار RTL می‌شود. این باگ از قبل وجود دارد و به پچ مربوط نیست — دکمه‌های پنجره روی تنظیمات Claude قرار می‌گیرند و پیش‌نمایش به سمت چپ می‌رود. پچ جهت پنجره را به LTR برمی‌گرداند، بدون تأثیر بر جهت متن گفتگو.

</div>

---

## 🚀 نصب سریع — Windows

<table dir="rtl">
<tr>
<td width="48" align="center" dir="rtl">💡</td>
<td align="center" dir="rtl">سرویس <b>Windows PowerShell</b> (پنجره آبی) را باز کنید و دستور زیر را اجرا کنید:</td>
</tr>
</table>

<div dir="ltr">

```powershell
irm https://raw.githubusercontent.com/mhghotbi/claude-desktop-rtl-patch/main/install.ps1 | iex
```

</div>

<table dir="rtl">
<tr>
<td width="48" align="center" dir="rtl">✅</td>
<td align="center" dir="rtl">۱. پنجره <b>UAC</b> ظاهر می‌شود — روی <b>Yes</b> کلیک کنید<br>۲. از منو گزینه <b>۱. نصب</b> را انتخاب کنید</td>
</tr>
</table>

<div dir="rtl">

> [!TIP]
> ترجیح می‌دهید به <code dir="ltr">iex</code> وصل نکنید؟ فایل <code dir="ltr">patch.ps1</code> را از مخزن دانلود کنید، راست‌کلیک کنید و **Run with PowerShell** را بزنید.

</div>

---

## 🍎 نصب سریع — macOS

<table dir="rtl">
<tr>
<td width="48" align="center" dir="rtl">📦</td>
<td align="center" dir="rtl">نسخه مک یک <b>Claude-RTL.app</b> جداگانه در <code dir="ltr">~/Applications</code> می‌سازد — برنامه اصلی دست‌نخورده باقی می‌ماند.</td>
</tr>
</table>

<p dir="rtl"><b>نیازمندی‌ها:</b> Node.js (<a href="https://nodejs.org/">nodejs.org</a>) · Xcode Command Line Tools (<code dir="ltr">xcode-select --install</code>)</p>

<div dir="ltr">

```bash
git clone https://github.com/mhghotbi/claude-desktop-rtl-patch
cd claude-desktop-rtl-patch
bash patch-mac.sh
```

</div>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">مرحله</th>
<th align="center" dir="rtl">کار</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>۱</b></td>
<td align="center" dir="rtl">گزینه <b>۱. نصب</b> را از منو انتخاب کنید</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۲</b></td>
<td align="center" dir="rtl"><b>Claude RTL</b> را از <code dir="ltr">~/Applications</code> باز کنید</td>
</tr>
</tbody>
</table>

<div dir="rtl">

> [!NOTE]
> در macOS پچ به‌جای تغییر مستقیم، از Claude.app یک کپی می‌سازد؛ نیازی به دستکاری گواهینامه نیست. امضای ad-hoc استفاده می‌شود و Claude.app اصلی همچنان کنار Claude-RTL.app کار می‌کند.

</div>

---

## 📋 نیازمندی‌ها

### ویندوز

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">نیازمندی</th>
<th align="center" dir="rtl">توضیح</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>ویندوز ۱۰ / ۱۱</b></td>
<td align="center" dir="rtl">با Claude Desktop نصب‌شده (<a href="https://downloads.claude.ai/releases/win32/ClaudeSetup.exe">دانلود</a>)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>Node.js</b></td>
<td align="center" dir="rtl"><code dir="ltr">npx</code> باید در PATH باشد (<a href="https://nodejs.org/">nodejs.org</a>)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>دسترسی مدیر</b></td>
<td align="center" dir="rtl">نصب‌کننده به‌صورت خودکار از طریق UAC ارتقا می‌یابد</td>
</tr>
</tbody>
</table>

### macOS

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">نیازمندی</th>
<th align="center" dir="rtl">توضیح</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>macOS</b></td>
<td align="center" dir="rtl">با Claude Desktop نصب‌شده (<a href="https://claude.ai/download">دانلود</a>)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>Node.js</b></td>
<td align="center" dir="rtl"><code dir="ltr">npx</code> باید در PATH باشد (<a href="https://nodejs.org/">nodejs.org</a>)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>Xcode CLI tools</b></td>
<td align="center" dir="rtl">برای <code dir="ltr">codesign</code>: <code dir="ltr">xcode-select --install</code></td>
</tr>
</tbody>
</table>

<div dir="rtl">

> [!IMPORTANT]
> در ویندوز از **Windows PowerShell** داخلی (پنجره آبی) استفاده کنید، نه PowerShell 7 (<code dir="ltr">pwsh</code>). جزئیات در بخش <a href="#️-عیب‌یابی">عیب‌یابی</a>.

</div>

---

## 🎛️ گزینه‌های منو

### ویندوز — <code dir="ltr">patch.ps1</code>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">#</th>
<th align="center" dir="rtl">گزینه</th>
<th align="center" dir="rtl">عملکرد</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>۱</b></td>
<td align="center" dir="rtl">نصب پچ RTL</td>
<td align="center" dir="rtl">پشتیبان از فایل‌های اصلی و افزودن پشتیبانی RTL</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۲</b></td>
<td align="center" dir="rtl">بازگشت به حالت اصلی</td>
<td align="center" dir="rtl">برگرداندن همه تغییرات پچ</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۳</b></td>
<td align="center" dir="rtl">میانبر «به‌روزرسانی سریع»</td>
<td align="center" dir="rtl">میانبر دسکتاپ برای اعمال مجدد پچ با یک کلیک</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۴</b></td>
<td align="center" dir="rtl">فعال‌کردن به‌روزرسانی خودکار</td>
<td align="center" dir="rtl">تسک پس‌زمینه برای اعمال مجدد پچ پس از هر به‌روزرسانی Claude</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۵</b></td>
<td align="center" dir="rtl">غیرفعال‌کردن به‌روزرسانی خودکار</td>
<td align="center" dir="rtl">حذف تسک پس‌زمینه</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۶</b></td>
<td align="center" dir="rtl">خروج</td>
<td align="center" dir="rtl">بستن پچر</td>
</tr>
</tbody>
</table>

### macOS — <code dir="ltr">patch-mac.sh</code>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">#</th>
<th align="center" dir="rtl">گزینه</th>
<th align="center" dir="rtl">عملکرد</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>۱</b></td>
<td align="center" dir="rtl">نصب</td>
<td align="center" dir="rtl">ساخت کپی از Claude.app با RTL → <code dir="ltr">~/Applications/Claude-RTL.app</code></td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۲</b></td>
<td align="center" dir="rtl">بازگشت</td>
<td align="center" dir="rtl">حذف <code dir="ltr">Claude-RTL.app</code> (اصلی دست‌نخورده می‌ماند)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۳</b></td>
<td align="center" dir="rtl">خروج</td>
<td align="center" dir="rtl">بستن پچر</td>
</tr>
</tbody>
</table>

---

## 🔄 ماندگاری پچ پس از به‌روزرسانی (ویندوز)

<p dir="rtl">به‌روزرسانی‌های Claude Desktop پچ را پاک می‌کنند. دو راه‌حل:</p>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">روش</th>
<th align="center" dir="rtl">توضیح</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>میانبر به‌روزرسانی سریع</b> (گزینه ۳)</td>
<td align="center" dir="rtl">میانبر دسکتاپی <b>«Update Claude RTL»</b> — با دوبار کلیک، پچ مجدداً اعمال می‌شود</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>به‌روزرسانی خودکار</b> (گزینه ۴)</td>
<td align="center" dir="rtl">تسک زمان‌بندی‌شده سبک که با راه‌اندازی نسخه جدید <code dir="ltr">claude.exe</code>، پچ را دوباره اعمال می‌کند</td>
</tr>
</tbody>
</table>

<p dir="rtl">در macOS پس از هر به‌روزرسانی، <code dir="ltr">bash patch-mac.sh</code> را دوباره اجرا کنید.</p>

---

## 🗑️ حذف

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">پلتفرم</th>
<th align="center" dir="rtl">دستور</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>ویندوز</b></td>
<td align="center" dir="rtl">اسکریپت را اجرا کنید → گزینه <b>۲. بازگشت</b> (اگر به‌روزرسانی خودکار فعال است، ابتدا گزینه <b>۵</b>)</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>macOS</b></td>
<td align="center" dir="rtl"><code dir="ltr">bash patch-mac.sh restore</code> یا گزینه <b>۲</b> از منو — Claude.app اصلی دست‌نخورده است</td>
</tr>
</tbody>
</table>

---

## 🛠️ عیب‌یابی

<details dir="rtl">
<summary dir="rtl"><b>❌ «Node.js (npx) is required»</b></summary>

<p dir="rtl">Node.js را از <a href="https://nodejs.org/">nodejs.org</a> نصب کنید و ترمینال را مجدداً باز کنید.</p>

</details>

<details dir="rtl">
<summary dir="rtl"><b>❌ Claude پس از پچ باز نمی‌شود (ویندوز)</b></summary>

<p dir="rtl">اسکریپت را دوباره اجرا کنید: ابتدا گزینه <b>۲ (بازگشت)</b>، سپس <b>۱ (نصب)</b>.</p>

</details>

<details dir="rtl">
<summary dir="rtl"><b>❌ پچ پس از به‌روزرسانی Claude خراب شد (ویندوز)</b></summary>

<p dir="rtl">میانبر <b>«Update Claude RTL»</b> را اجرا کنید، یا از به‌روزرسانی خودکار استفاده کنید. برای رفع دستی: فایل‌های <code dir="ltr">.bak</code> در پوشه Claude را حذف کنید و نصب‌کننده را دوباره اجرا کنید.</p>

</details>

<details dir="rtl">
<summary dir="rtl"><b>❌ <code dir="ltr">Import-Module … AuditToString</code></b></summary>

<p dir="rtl">از <b>PowerShell 7 (<code dir="ltr">pwsh</code>)</b> استفاده کرده‌اید که با پچ سازگار نیست.</p>

<p dir="rtl">۱. <b>Win + R</b> بزنید، <code dir="ltr">powershell</code> تایپ کنید و <b>Enter</b><br>
۲. پنجره <b>آبی</b> Windows PowerShell باز می‌شود (نه سیاه <code dir="ltr">pwsh</code>)<br>
۳. دستور نصب را اجرا کنید</p>

</details>

<details dir="rtl">
<summary dir="rtl"><b>❌ macOS — codesign با خطا مواجه شد</b></summary>

<p dir="rtl">مطمئن شوید Xcode Command Line Tools نصب است (<code dir="ltr">xcode-select --install</code>) و ترمینال در <b>تنظیمات سیستم → حریم خصوصی و امنیت → Full Disk Access</b> دسترسی دارد.</p>

</details>

---

<details dir="rtl">
<summary dir="rtl"><b>🔍 نحوه کار (فنی)</b></summary>

<div dir="rtl">

### بار JavaScript

<p dir="rtl">منطق تشخیص در <a href="src/rtl-core.js"><code dir="ltr">src/rtl-core.js</code></a> (خالص، تست‌شده، بدون DOM) و <a href="src/rtl-payload.js"><code dir="ltr">src/rtl-payload.js</code></a> (لایه DOM + تزریق فونت وزیرمتن) قرار دارد. <code dir="ltr">tools/build-payload.ps1</code> آن‌ها را کنار هم می‌گذارد:</p>

<p dir="rtl">۱. درون‌خطی کردن <code dir="ltr">rtl-core.js</code> در <code dir="ltr">rtl-payload.js</code> در <code dir="ltr">/*__RTL_CORE__*/</code><br>
۲. Base64 کردن <code dir="ltr">fonts/Vazirmatn[wght].woff2</code> و تزریق <code dir="ltr">@font-face</code> در <code dir="ltr">/*__FONT_CSS__*/</code><br>
۳. نوشتن <code dir="ltr">dist/rtl-payload-built.js</code> و قرار دادن نتیجه در <code dir="ltr">patch.ps1</code></p>

### پچ ویندوز

<p dir="rtl">Claude Desktop یک اپ Electron <b>امضاشده دیجیتالی</b> است. پچ در سه فاز اتمی کار می‌کند:</p>

<p dir="rtl"><b>فاز ۱ — تزریق ASAR.</b> استخراج <code dir="ltr">app.asar</code>، افزودن payload RTL به فایل‌های renderer و اجبار UI پنجره به LTR در main process.</p>

<p dir="rtl"><b>فاز ۲ — جایگزینی hash در <code dir="ltr">claude.exe</code>.</b> جستجوی بایت‌به‌بایت و به‌روزرسانی hash ASAR؛ در صورت تغییر فرمت، fuse یکپارچگی غیرفعال می‌شود.</p>

<p dir="rtl"><b>فاز ۳ — تعویض گواهینامه در <code dir="ltr">cowork-svc.exe</code>.</b> جایگزینی گواهینامه Anthropic با خودامضا، امضای مجدد باینری‌ها و افزودن به مخزن trusted root ویندوز.</p>

### پچ macOS

<p dir="rtl">۱. <b>کلون</b> Claude.app به <code dir="ltr">~/Applications/Claude-RTL.app</code><br>
۲. <b>تزریق</b> payload RTL در ASAR<br>
۳. <b>غیرفعال‌کردن</b> fuse یکپارچگی ASAR<br>
۴. <b>امضا</b> با ad-hoc (<code dir="ltr">codesign --force --deep --sign -</code>)</p>

<p dir="rtl">همه فایل‌های اصلی قبل از تغییر به‌صورت <code dir="ltr">.bak</code> پشتیبان می‌شوند.</p>

</div>

</details>

---

## ⚠️ سلب مسئولیت

<div dir="rtl">

> [!CAUTION]
> این پچ فایل‌های باینری Claude Desktop (ویندوز) را تغییر می‌دهد یا یک کپی تغییریافته می‌سازد (macOS). نسخه ویندوز گواهینامه امضای Anthropic را با گواهینامه خودامضا جایگزین کرده، آن را به مخزن **trusted root** ویندوز اضافه می‌کند و تأیید صحت برنامه را دور می‌زند.

</div>

<p dir="rtl">با نصب، موارد زیر را می‌پذیرید:</p>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">#</th>
<th align="center" dir="rtl">شرط</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><b>۱</b></td>
<td align="center" dir="rtl"><b>استفاده با مسئولیت خودتان</b> — نویسندگان مسئولیتی در قبال آسیب، از دست دادن داده یا ناپایداری ندارند</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۲</b></td>
<td align="center" dir="rtl"><b>ممکن است با شرایط خدمات Anthropic همخوانی نداشته باشد</b> — پیشنهاد می‌شود آن‌ها را بررسی کنید</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۳</b></td>
<td align="center" dir="rtl"><b>به این مخزن اعتماد دارید</b> — اجرای کد با دسترسی مدیر خطر دارد؛ همیشه منبع را تأیید کنید</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۴</b></td>
<td align="center" dir="rtl"><b>موقتی است</b> — به‌روزرسانی‌های Claude پچ را پاک می‌کنند</td>
</tr>
<tr>
<td align="center" dir="rtl"><b>۵</b></td>
<td align="center" dir="rtl"><b>راه‌حل موقت</b> تا زمانی که Anthropic پشتیبانی RTL بومی را اضافه کند</td>
</tr>
</tbody>
</table>

---

## 🤝 مشارکت

<p dir="rtl">این پروژه <b>متن‌باز</b> است و تحت مجوز <b>MIT</b> منتشر شده. هر کمکی که دقت RTL را بهبود بدهد خوشامد است — PRها باز هستند. 🙏</p>

---

## 🙏 تقدیر و سپاسگزاری

<p dir="rtl">این پروژه یک کار مشتق است. جزئیات کامل در <a href="CREDITS.md">CREDITS.md</a>.</p>

<table dir="rtl">
<thead>
<tr>
<th align="center" dir="rtl">پروژه</th>
<th align="center" dir="rtl">نویسنده</th>
<th align="center" dir="rtl">استفاده شده از</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center" dir="rtl"><a href="https://github.com/shraga100/claude-desktop-rtl-patch">claude-desktop-rtl-patch</a></td>
<td align="center" dir="rtl">shraga100</td>
<td align="center" dir="rtl">پچ اصلی RTL ویندوز — مکانیزم پچینگ هسته از این پروژه گرفته شده</td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="https://github.com/soguy/claude-desktop-rtl-mac">claude-desktop-rtl-mac</a></td>
<td align="center" dir="rtl">soguy</td>
<td align="center" dir="rtl">طراحی پچ macOS و رویکرد فونت به‌صورت base64</td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="https://github.com/rastikerdar/vazirmatn">Vazirmatn</a></td>
<td align="center" dir="rtl">صابر راستی‌کردار</td>
<td align="center" dir="rtl">فونت متغیر فارسی/عربی وزیرمتن (مجوز OFL)</td>
</tr>
<tr>
<td align="center" dir="rtl"><a href="https://github.com/DavidiBellaire/Claude-UniMath">Claude-UniMath</a></td>
<td align="center" dir="rtl">Davidi Bellaire</td>
<td align="center" dir="rtl">تکنیک جداسازی LaTeX در متن RTL</td>
</tr>
</tbody>
</table>

---

## مجوز

<p dir="rtl"><a href="LICENSE">MIT</a> — برای اطلاعات کامل کپی‌رایت به <a href="CREDITS.md">CREDITS.md</a> مراجعه کنید.</p>

</div>
