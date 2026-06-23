<div dir="rtl" align="center">

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

<div dir="rtl">

## فهرست

| | |
| :--- | :--- |
| [✨ قابلیت‌ها](#-قابلیت‌ها) | [🚀 نصب ویندوز](#-نصب-سریع--windows) |
| [🍎 نصب macOS](#-نصب-سریع--macos) | [📋 نیازمندی‌ها](#-نیازمندی‌ها) |
| [🎛️ گزینه‌های منو](#️-گزینه‌های-منو) | [🔄 ماندگاری پس از به‌روزرسانی](#-ماندگاری-پچ-پس-از-به‌روزرسانی-ویندوز) |
| [🗑️ حذف](#️-حذف) | [🛠️ عیب‌یابی](#️-عیب‌یابی) |
| [⚠️ سلب مسئولیت](#️-سلب-مسئولیت) | [🤝 مشارکت](#-مشارکت) |

---

## ✨ قابلیت‌ها

| قابلیت | توضیح |
| :--- | :--- |
| 🔍 **شناسایی خودکار RTL** | در پاسخ‌های Claude و کادر ورودی، با تنظیم جهت در لحظه — حتی در حین دریافت پاسخ |
| 🔤 **فونت وزیرمتن** | فونت متغیر و مدرن برای فارسی و عربی، به‌صورت data URI تعبیه‌شده (بدون نیاز به اینترنت) |
| 💻 **کد، ریاضی و جدول** | بلوک‌های کد و LaTeX (`$x^2$`) در محیط RTL چپ‌به‌راست می‌مانند؛ جداول فارسی راست‌به‌چپ |
| 🪟 **رفع باگ پنجره** | وقتی زبان ویندوز فارسی یا عربی است، رابط Claude Desktop به‌اشتباه RTL می‌شود — این پچ آن را برطرف می‌کند |
| 💾 **پشتیبان‌گیری** | از همه فایل‌ها قبل از هر تغییر، با بازگشت خودکار در صورت بروز خطا |
| 🔄 **ماندگاری** | پس از به‌روزرسانی Claude (اختیاری)، از طریق میانبر دسکتاپ یا به‌روزرسانی خودکار |

> [!NOTE]
> در ویندوزی که زبان نمایش آن فارسی یا عربی است، رابط پنجره Claude Desktop به‌طور خودکار RTL می‌شود. این باگ از قبل وجود دارد و به پچ مربوط نیست — دکمه‌های پنجره روی تنظیمات Claude قرار می‌گیرند و پیش‌نمایش به سمت چپ می‌رود. پچ جهت پنجره را به LTR برمی‌گرداند، بدون تأثیر بر جهت متن گفتگو.

---

## 🚀 نصب سریع — Windows

<table>
<tr>
<td width="48" align="center">💡</td>
<td>

سرویس **Windows PowerShell** (پنجره آبی) را باز کنید و دستور زیر را اجرا کنید:

</td>
</tr>
</table>

```powershell
irm https://raw.githubusercontent.com/mhghotbi/claude-desktop-rtl-patch/main/install.ps1 | iex
```

<table>
<tr>
<td width="48" align="center">✅</td>
<td>

۱. پنجره **UAC** ظاهر می‌شود — روی **Yes** کلیک کنید  
۲. از منو گزینه **۱. نصب** را انتخاب کنید

</td>
</tr>
</table>

> [!TIP]
> ترجیح می‌دهید به `iex` وصل نکنید؟ فایل `patch.ps1` را از مخزن دانلود کنید، راست‌کلیک کنید و **Run with PowerShell** را بزنید.

---

## 🍎 نصب سریع — macOS

<table>
<tr>
<td width="48" align="center">📦</td>
<td>

نسخه مک یک **Claude-RTL.app** جداگانه در `~/Applications` می‌سازد — برنامه اصلی دست‌نخورده باقی می‌ماند.

</td>
</tr>
</table>

**نیازمندی‌ها:** Node.js ([nodejs.org](https://nodejs.org/)) · Xcode Command Line Tools (`xcode-select --install`)

```bash
git clone https://github.com/mhghotbi/claude-desktop-rtl-patch
cd claude-desktop-rtl-patch
bash patch-mac.sh
```

| مرحله | کار |
| :---: | :--- |
| **۱** | گزینه **۱. نصب** را از منو انتخاب کنید |
| **۲** | **Claude RTL** را از `~/Applications` باز کنید |

> [!NOTE]
> در macOS پچ به‌جای تغییر مستقیم، از Claude.app یک کپی می‌سازد؛ نیازی به دستکاری گواهینامه نیست. امضای ad-hoc استفاده می‌شود و Claude.app اصلی همچنان کنار Claude-RTL.app کار می‌کند.

---

## 📋 نیازمندی‌ها

### ویندوز

| نیازمندی | توضیح |
| :--- | :--- |
| **ویندوز ۱۰ / ۱۱** | با Claude Desktop نصب‌شده ([دانلود](https://downloads.claude.ai/releases/win32/ClaudeSetup.exe)) |
| **Node.js** | `npx` باید در PATH باشد ([nodejs.org](https://nodejs.org/)) |
| **دسترسی مدیر** | نصب‌کننده به‌صورت خودکار از طریق UAC ارتقا می‌یابد |

### macOS

| نیازمندی | توضیح |
| :--- | :--- |
| **macOS** | با Claude Desktop نصب‌شده ([دانلود](https://claude.ai/download)) |
| **Node.js** | `npx` باید در PATH باشد ([nodejs.org](https://nodejs.org/)) |
| **Xcode CLI tools** | برای `codesign`: `xcode-select --install` |

> [!IMPORTANT]
> در ویندوز از **Windows PowerShell** داخلی (پنجره آبی) استفاده کنید، نه PowerShell 7 (`pwsh`). جزئیات در بخش [عیب‌یابی](#️-عیب‌یابی).

---

## 🎛️ گزینه‌های منو

### ویندوز — `patch.ps1`

| # | گزینه | عملکرد |
| :---: | :--- | :--- |
| **۱** | نصب پچ RTL | پشتیبان از فایل‌های اصلی و افزودن پشتیبانی RTL |
| **۲** | بازگشت به حالت اصلی | برگرداندن همه تغییرات پچ |
| **۳** | میانبر «به‌روزرسانی سریع» | میانبر دسکتاپ برای اعمال مجدد پچ با یک کلیک |
| **۴** | فعال‌کردن به‌روزرسانی خودکار | تسک پس‌زمینه برای اعمال مجدد پچ پس از هر به‌روزرسانی Claude |
| **۵** | غیرفعال‌کردن به‌روزرسانی خودکار | حذف تسک پس‌زمینه |
| **۶** | خروج | بستن پچر |

### macOS — `patch-mac.sh`

| # | گزینه | عملکرد |
| :---: | :--- | :--- |
| **۱** | نصب | ساخت کپی از Claude.app با RTL → `~/Applications/Claude-RTL.app` |
| **۲** | بازگشت | حذف `Claude-RTL.app` (اصلی دست‌نخورده می‌ماند) |
| **۳** | خروج | بستن پچر |

---

## 🔄 ماندگاری پچ پس از به‌روزرسانی (ویندوز)

به‌روزرسانی‌های Claude Desktop پچ را پاک می‌کنند. دو راه‌حل:

| روش | توضیح |
| :--- | :--- |
| **میانبر به‌روزرسانی سریع** (گزینه ۳) | میانبر دسکتاپی **«Update Claude RTL»** — با دوبار کلیک، پچ مجدداً اعمال می‌شود |
| **به‌روزرسانی خودکار** (گزینه ۴) | تسک زمان‌بندی‌شده سبک که با راه‌اندازی نسخه جدید `claude.exe`، پچ را دوباره اعمال می‌کند |

در macOS پس از هر به‌روزرسانی، `bash patch-mac.sh` را دوباره اجرا کنید.

---

## 🗑️ حذف

| پلتفرم | دستور |
| :--- | :--- |
| **ویندوز** | اسکریپت را اجرا کنید → گزینه **۲. بازگشت** (اگر به‌روزرسانی خودکار فعال است، ابتدا گزینه **۵**) |
| **macOS** | `bash patch-mac.sh restore` یا گزینه **۲** از منو — Claude.app اصلی دست‌نخورده است |

---

## 🛠️ عیب‌یابی

<details>
<summary><b>❌ «Node.js (npx) is required»</b></summary>

Node.js را از [nodejs.org](https://nodejs.org/) نصب کنید و ترمینال را مجدداً باز کنید.

</details>

<details>
<summary><b>❌ Claude پس از پچ باز نمی‌شود (ویندوز)</b></summary>

اسکریپت را دوباره اجرا کنید: ابتدا گزینه **۲ (بازگشت)**، سپس **۱ (نصب)**.

</details>

<details>
<summary><b>❌ پچ پس از به‌روزرسانی Claude خراب شد (ویندوز)</b></summary>

میانبر **«Update Claude RTL»** را اجرا کنید، یا از به‌روزرسانی خودکار استفاده کنید. برای رفع دستی: فایل‌های `.bak` در پوشه Claude را حذف کنید و نصب‌کننده را دوباره اجرا کنید.

</details>

<details>
<summary><b>❌ <code>Import-Module … AuditToString</code></b></summary>

از **PowerShell 7 (`pwsh`)** استفاده کرده‌اید که با پچ سازگار نیست.

۱. **Win + R** بزنید، `powershell` تایپ کنید و **Enter**  
۲. پنجره **آبی** Windows PowerShell باز می‌شود (نه سیاه `pwsh`)  
۳. دستور نصب را اجرا کنید

</details>

<details>
<summary><b>❌ macOS — codesign با خطا مواجه شد</b></summary>

مطمئن شوید Xcode Command Line Tools نصب است (`xcode-select --install`) و ترمینال در **تنظیمات سیستم → حریم خصوصی و امنیت → Full Disk Access** دسترسی دارد.

</details>

---

<details>
<summary><b>🔍 نحوه کار (فنی)</b></summary>

### بار JavaScript

منطق تشخیص در [`src/rtl-core.js`](src/rtl-core.js) (خالص، تست‌شده، بدون DOM) و [`src/rtl-payload.js`](src/rtl-payload.js) (لایه DOM + تزریق فونت وزیرمتن) قرار دارد. `tools/build-payload.ps1` آن‌ها را کنار هم می‌گذارد:

۱. درون‌خطی کردن `rtl-core.js` در `rtl-payload.js` در `/*__RTL_CORE__*/`  
۲. Base64 کردن `fonts/Vazirmatn[wght].woff2` و تزریق `@font-face` در `/*__FONT_CSS__*/`  
۳. نوشتن `dist/rtl-payload-built.js` و قرار دادن نتیجه در `patch.ps1`

### پچ ویندوز

Claude Desktop یک اپ Electron **امضاشده دیجیتالی** است. پچ در سه فاز اتمی کار می‌کند:

**فاز ۱ — تزریق ASAR.** استخراج `app.asar`، افزودن payload RTL به فایل‌های renderer و اجبار UI پنجره به LTR در main process.

**فاز ۲ — جایگزینی hash در `claude.exe`.** جستجوی بایت‌به‌بایت و به‌روزرسانی hash ASAR؛ در صورت تغییر فرمت، fuse یکپارچگی غیرفعال می‌شود.

**فاز ۳ — تعویض گواهینامه در `cowork-svc.exe`.** جایگزینی گواهینامه Anthropic با خودامضا، امضای مجدد باینری‌ها و افزودن به مخزن trusted root ویندوز.

### پچ macOS

۱. **کلون** Claude.app به `~/Applications/Claude-RTL.app`  
۲. **تزریق** payload RTL در ASAR  
۳. **غیرفعال‌کردن** fuse یکپارچگی ASAR  
۴. **امضا** با ad-hoc (`codesign --force --deep --sign -`)

همه فایل‌های اصلی قبل از تغییر به‌صورت `.bak` پشتیبان می‌شوند.

</details>

---

## ⚠️ سلب مسئولیت

> [!CAUTION]
> این پچ فایل‌های باینری Claude Desktop (ویندوز) را تغییر می‌دهد یا یک کپی تغییریافته می‌سازد (macOS). نسخه ویندوز گواهینامه امضای Anthropic را با گواهینامه خودامضا جایگزین کرده، آن را به مخزن **trusted root** ویندوز اضافه می‌کند و تأیید صحت برنامه را دور می‌زند.

با نصب، موارد زیر را می‌پذیرید:

| # | شرط |
| :---: | :--- |
| **۱** | **استفاده با مسئولیت خودتان** — نویسندگان مسئولیتی در قبال آسیب، از دست دادن داده یا ناپایداری ندارند |
| **۲** | **ممکن است با شرایط خدمات Anthropic همخوانی نداشته باشد** — پیشنهاد می‌شود آن‌ها را بررسی کنید |
| **۳** | **به این مخزن اعتماد دارید** — اجرای کد با دسترسی مدیر خطر دارد؛ همیشه منبع را تأیید کنید |
| **۴** | **موقتی است** — به‌روزرسانی‌های Claude پچ را پاک می‌کنند |
| **۵** | **راه‌حل موقت** تا زمانی که Anthropic پشتیبانی RTL بومی را اضافه کند |

---

## 🤝 مشارکت

این پروژه **متن‌باز** است و تحت مجوز **MIT** منتشر شده. هر کمکی که دقت RTL را بهبود بدهد خوشامد است — PRها باز هستند. 🙏

---

## 🙏 تقدیر و سپاسگزاری

این پروژه یک کار مشتق است. جزئیات کامل در [CREDITS.md](CREDITS.md).

| پروژه | نویسنده | استفاده شده از |
| :--- | :--- | :--- |
| [claude-desktop-rtl-patch](https://github.com/shraga100/claude-desktop-rtl-patch) | shraga100 | پچ اصلی RTL ویندوز — مکانیزم پچینگ هسته از این پروژه گرفته شده |
| [claude-desktop-rtl-mac](https://github.com/soguy/claude-desktop-rtl-mac) | soguy | طراحی پچ macOS و رویکرد فونت به‌صورت base64 |
| [Vazirmatn](https://github.com/rastikerdar/vazirmatn) | صابر راستی‌کردار | فونت متغیر فارسی/عربی وزیرمتن (مجوز OFL) |
| [Claude-UniMath](https://github.com/DavidiBellaire/Claude-UniMath) | Davidi Bellaire | تکنیک جداسازی LaTeX در متن RTL |

---

## مجوز

[MIT](LICENSE) — برای اطلاعات کامل کپی‌رایت به [CREDITS.md](CREDITS.md) مراجعه کنید.

</div>
