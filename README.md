<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عرض هوية بصرية — المحامية العنود · نِداد للتصاميم</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&family=Amiri:wght@400;700&display=swap');

:root {
  --gold: #c9a84c;
  --gold-light: #e6cd84;
  --gold-dim: rgba(201,168,76,0.13);
  --navy: #0d1117;
  --navy2: #161b22;
  --navy3: #1f2530;
  --border: rgba(255,255,255,0.07);
  --text: #e9e6df;
  --muted: rgba(233,230,223,0.45);
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: 'Tajawal', sans-serif;
  background: var(--navy);
  color: var(--text);
  overflow-x: hidden;
  line-height: 1.75;
}

h1, h2, .serif { font-family: 'Amiri', serif; }

/* ═══ HERO ═══ */
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 80px 24px 60px;
  overflow: hidden;
}
.hero-bg {
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse 80% 60% at 50% -10%, rgba(201,168,76,0.10) 0%, transparent 70%),
    radial-gradient(ellipse 40% 40% at 80% 80%, rgba(201,168,76,0.04) 0%, transparent 60%),
    var(--navy);
}
.hero-grid {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
  background-size: 60px 60px;
  mask-image: radial-gradient(ellipse 90% 80% at 50% 50%, black 30%, transparent 100%);
}

.hero-tag {
  position: relative;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: var(--gold-dim);
  border: 1px solid rgba(201,168,76,0.3);
  color: var(--gold-light);
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 2px;
  padding: 7px 18px;
  border-radius: 30px;
  margin-bottom: 30px;
  animation: fadeDown 0.7s ease both;
}
.hero-tag::before {
  content: '';
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--gold);
  animation: pulse 2s infinite;
}
@keyframes pulse {
  0%,100% { opacity:1; transform:scale(1); }
  50% { opacity:0.4; transform:scale(0.7); }
}

.hero h1 {
  position: relative;
  font-size: clamp(34px, 6.5vw, 64px);
  font-weight: 700;
  line-height: 1.35;
  margin-bottom: 22px;
  animation: fadeDown 0.7s 0.1s ease both;
}
.hero h1 .accent { color: var(--gold); display: block; }
.hero p {
  position: relative;
  font-size: clamp(14.5px, 2.1vw, 17px);
  color: var(--muted);
  max-width: 500px;
  margin: 0 auto 36px;
  font-weight: 400;
  animation: fadeDown 0.7s 0.2s ease both;
}

.inv-number {
  position: relative;
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 11px 26px;
  font-size: 12.5px;
  color: var(--muted);
  margin-bottom: 30px;
  animation: fadeDown 0.7s 0.15s ease both;
}
.inv-number strong { color: var(--gold); }

.stats {
  position: relative;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 12px 0;
  border: 1px solid var(--border);
  border-radius: 16px;
  overflow: hidden;
  max-width: 700px;
  width: 100%;
  background: rgba(255,255,255,0.02);
  backdrop-filter: blur(10px);
  animation: fadeUp 0.7s 0.3s ease both;
}
.stat {
  flex: 1;
  min-width: 120px;
  padding: 24px 20px;
  text-align: center;
  border-left: 1px solid var(--border);
}
.stat:last-child { border-left: none; }
.stat-num { font-size: 30px; font-weight: 900; color: var(--gold); line-height: 1; display: block; font-family: 'Tajawal', sans-serif; }
.stat-label { font-size: 11.5px; color: var(--muted); margin-top: 5px; display: block; }

@keyframes fadeDown { from{opacity:0;transform:translateY(-20px);} to{opacity:1;transform:translateY(0);} }
@keyframes fadeUp { from{opacity:0;transform:translateY(20px);} to{opacity:1;transform:translateY(0);} }

/* ═══ CLIENT CARD ═══ */
.client-section { padding: 60px 24px 0; max-width: 900px; margin: 0 auto; }
.client-card {
  background: var(--navy2);
  border: 1px solid rgba(201,168,76,0.2);
  border-radius: 16px;
  padding: 30px 34px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
}
.client-info { display: flex; flex-direction: column; gap: 5px; }
.client-label { font-size: 11px; color: var(--gold); font-weight: 700; letter-spacing: 2px; }
.client-name { font-size: 26px; font-weight: 700; font-family: 'Amiri', serif; }
.client-sub { font-size: 12.5px; color: var(--muted); margin-top: 2px; }
.date-info { text-align: left; }
.date-label { font-size: 11px; color: var(--muted); letter-spacing: 1px; }
.date-val { font-size: 15px; font-weight: 700; color: var(--gold-light); }

/* ═══ SECTIONS ═══ */
.section { padding: 64px 24px; max-width: 900px; margin: 0 auto; }
.section-header { text-align: center; margin-bottom: 50px; }
.section-tag {
  display: inline-block;
  font-size: 11px; font-weight: 700; letter-spacing: 3px;
  color: var(--gold); text-transform: uppercase; margin-bottom: 14px;
}
.section-title { font-size: clamp(24px, 4vw, 38px); font-weight: 700; line-height: 1.35; }
.section-title span { color: var(--gold); }

.cat-label {
  font-size: 11px; font-weight: 700; letter-spacing: 3px;
  color: var(--gold); text-transform: uppercase;
  margin: 36px 0 14px;
  display: flex; align-items: center; gap: 12px;
}
.cat-label::after {
  content: ''; flex: 1; height: 1px;
  background: linear-gradient(90deg, rgba(201,168,76,0.3), transparent);
}

/* ═══ PRINT ITEMS — separated, itemized ═══ */
.print-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
  gap: 12px;
}
.print-card {
  background: var(--navy2);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 20px 18px;
  transition: border-color 0.3s, transform 0.3s;
  position: relative;
  overflow: hidden;
  counter-increment: item;
}
.print-card::before {
  content: '٠' counter(item);
  position: absolute;
  top: 12px; left: 14px;
  font-size: 11px;
  color: rgba(201,168,76,0.4);
  font-weight: 700;
}
.print-grid { counter-reset: item; }
.print-card:hover { border-color: rgba(201,168,76,0.35); transform: translateY(-2px); }
.print-icon { font-size: 22px; margin-bottom: 10px; display: block; }
.print-name { font-size: 14.5px; font-weight: 800; margin-bottom: 5px; }
.print-desc { font-size: 12px; color: var(--muted); line-height: 1.6; }

/* ═══ PROFILE feature card ═══ */
.profile-card {
  background: linear-gradient(135deg, rgba(201,168,76,0.10), rgba(201,168,76,0.02));
  border: 1px solid rgba(201,168,76,0.3);
  border-radius: 18px;
  padding: 32px 34px;
  display: flex;
  align-items: flex-start;
  gap: 22px;
  flex-wrap: wrap;
}
.profile-icon-wrap {
  width: 60px; height: 60px;
  border-radius: 14px;
  background: rgba(201,168,76,0.15);
  border: 1px solid rgba(201,168,76,0.3);
  display: flex; align-items: center; justify-content: center;
  font-size: 28px;
  flex-shrink: 0;
}
.profile-body { flex: 1; min-width: 220px; }
.profile-title { font-size: 19px; font-weight: 800; margin-bottom: 8px; }
.profile-desc { font-size: 13.5px; color: var(--muted); line-height: 1.7; margin-bottom: 14px; }
.profile-feats { display: flex; flex-wrap: wrap; gap: 8px; }
.profile-feat-tag {
  font-size: 12px;
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--border);
  padding: 5px 13px;
  border-radius: 20px;
  color: var(--text);
}

/* ═══ PAYMENT / INVOICE ═══ */
.payment-section { padding: 64px 24px; max-width: 900px; margin: 0 auto; }
.invoice-table {
  background: var(--navy2);
  border: 1px solid var(--border);
  border-radius: 20px;
  overflow: hidden;
  max-width: 620px;
  margin: 0 auto;
}
.inv-table-head {
  background: var(--navy3);
  padding: 28px 36px 24px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
}
.inv-client-col { display: flex; flex-direction: column; gap: 3px; }
.inv-client-label { font-size: 11px; color: var(--muted); letter-spacing: 1px; }
.inv-client-name { font-size: 19px; font-weight: 800; font-family: 'Amiri', serif; }
.inv-total-col { text-align: left; }
.inv-total-label { font-size: 11px; color: var(--muted); letter-spacing: 1px; }
.inv-total-amount { font-size: 42px; font-weight: 900; color: var(--gold); line-height: 1; font-family: 'Tajawal', sans-serif; }
.inv-total-currency { font-size: 18px; font-weight: 400; }

.inv-row {
  display: flex; justify-content: space-between; align-items: center;
  padding: 20px 36px; border-bottom: 1px solid var(--border);
  gap: 16px; flex-wrap: wrap;
}
.inv-row:last-child { border-bottom: none; }
.inv-row-right { display: flex; flex-direction: column; gap: 3px; }
.inv-row-label { font-size: 14px; color: var(--text); font-weight: 600; }
.inv-row-note { font-size: 12px; color: var(--muted); }
.inv-row-amount { font-size: 22px; font-weight: 900; }
.inv-row-amount.gold { color: var(--gold); }
.inv-row-amount.white { color: var(--text); }

.required-badge {
  display: inline-flex; align-items: center; gap: 6px;
  background: rgba(201,168,76,0.12);
  border: 1px solid rgba(201,168,76,0.3);
  color: var(--gold-light);
  font-size: 11px; font-weight: 700;
  padding: 4px 12px; border-radius: 20px; margin-top: 4px;
}
.required-badge::before {
  content: ''; width: 5px; height: 5px; border-radius: 50%;
  background: var(--gold); animation: pulse 2s infinite;
}

.inv-footer-note { text-align: center; font-size: 12.5px; color: var(--muted); margin-top: 22px; }

/* ═══ TIMELINE ═══ */
.timeline { position: relative; padding-right: 30px; max-width: 580px; margin: 0 auto; }
.timeline::before {
  content: ''; position: absolute; right: 10px; top: 10px; bottom: 10px;
  width: 2px; background: linear-gradient(180deg, var(--gold), transparent);
}
.tl-item { position: relative; margin-bottom: 26px; padding-right: 24px; }
.tl-item:last-child { margin-bottom: 0; }
.tl-dot {
  position: absolute; right: -24px; top: 6px;
  width: 14px; height: 14px; border-radius: 50%;
  background: var(--gold); border: 3px solid var(--navy);
  box-shadow: 0 0 0 2px rgba(201,168,76,0.3);
}
.tl-day { font-size: 11px; font-weight: 700; letter-spacing: 2px; color: var(--gold); margin-bottom: 3px; }
.tl-title { font-size: 15px; font-weight: 700; margin-bottom: 3px; }
.tl-desc { font-size: 13px; color: var(--muted); }

/* ═══ CTA ═══ */
.cta-section { padding: 70px 24px; text-align: center; position: relative; overflow: hidden; }
.cta-section::before {
  content: ''; position: absolute; inset: 0;
  background: radial-gradient(ellipse 70% 60% at 50% 50%, rgba(201,168,76,0.06) 0%, transparent 70%);
}
.cta-section h2 { font-size: clamp(26px, 5vw, 42px); font-weight: 700; margin-bottom: 12px; position: relative; }
.cta-section p { font-size: 14px; color: var(--muted); margin-bottom: 32px; position: relative; }
.cta-btn {
  position: relative; display: inline-flex; align-items: center; gap: 10px;
  background: var(--gold); color: var(--navy);
  font-family: 'Tajawal', sans-serif; font-size: 17px; font-weight: 800;
  padding: 15px 38px; border-radius: 50px; text-decoration: none;
  transition: all 0.3s; box-shadow: 0 8px 32px rgba(201,168,76,0.3);
}
.cta-btn:hover { background: var(--gold-light); transform: translateY(-2px); box-shadow: 0 12px 40px rgba(201,168,76,0.4); }
.cta-pills { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-top: 28px; position: relative; }
.cta-pill {
  display: inline-flex; align-items: center; gap: 6px;
  background: rgba(255,255,255,0.04); border: 1px solid var(--border);
  border-radius: 20px; padding: 7px 14px; font-size: 13px; color: var(--muted);
}

.full-divider {
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--border) 20%, var(--border) 80%, transparent);
  margin: 0 24px;
}
.footer {
  border-top: 1px solid var(--border);
  padding: 26px 24px;
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 12px; max-width: 900px; margin: 0 auto;
}
.footer-brand { font-size: 14px; font-weight: 800; }
.footer-brand span { color: var(--gold); }
.footer-phone { font-size: 13px; color: var(--muted); direction: ltr; }

@media (max-width: 600px) {
  .stat { min-width: 90px; padding: 16px 10px; }
  .stat-num { font-size: 22px; }
  .inv-table-head { flex-direction: column; align-items: flex-start; }
  .inv-total-col { text-align: right; }
  .inv-row { padding: 16px 22px; }
  .inv-table-head { padding: 22px; }
  .client-card { flex-direction: column; }
  .date-info { text-align: right; }
  .profile-card { padding: 24px 22px; }
}
</style>
</head>
<body>

<!-- ═══ HERO ═══ -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>

  <div class="hero-tag">⚖️ هوية بصرية قانونية · نِداد للتصاميم</div>

  <h1>
    هوية بصرية تعكس
    <span class="accent">مكانة مكتبكم القانوني</span>
  </h1>

  <div class="inv-number">
    رقم العرض: <strong>#ND-<span id="inv-num"></span></strong> &nbsp;·&nbsp; تاريخ: <strong id="inv-date"></strong>
  </div>

  <p>هوية بصرية متكاملة بمطبوعات احترافية مفصّلة وبروفايل تعريفي يليق بمكتب محاماة</p>

  <div class="stats">
    <div class="stat">
      <span class="stat-num">٨</span>
      <span class="stat-label">مطبوعات منفصلة</span>
    </div>
    <div class="stat">
      <span class="stat-num">١</span>
      <span class="stat-label">بروفايل احترافي</span>
    </div>
    <div class="stat">
      <span class="stat-num">٣</span>
      <span class="stat-label">مراجعات مجانية</span>
    </div>
    <div class="stat">
      <span class="stat-num">٥٠٠</span>
      <span class="stat-label">ريال فقط</span>
    </div>
  </div>
</section>

<!-- ═══ CLIENT CARD ═══ -->
<div class="client-section">
  <div class="client-card">
    <div class="client-info">
      <span class="client-label">مُعدّ خصيصاً لـ</span>
      <span class="client-name">المحامية العنود</span>
      <span class="client-sub">هوية بصرية لمكتب محاماة</span>
    </div>
    <div class="date-info">
      <div class="date-label">تاريخ إصدار العرض</div>
      <div class="date-val" id="client-date"></div>
    </div>
  </div>
</div>

<div class="full-divider" style="margin-top:40px;"></div>

<!-- ═══ PRINTED MATERIALS — itemized ═══ -->
<section class="section">
  <div class="section-header">
    <div class="section-tag">المطبوعات الرسمية</div>
    <h2 class="section-title">كل قطعة طباعية<br><span>مصمَّمة ومفصَّلة بدقة</span></h2>
  </div>

  <div class="print-grid">
    <div class="print-card">
      <span class="print-icon">💳</span>
      <div class="print-name">بطاقة أعمال</div>
      <div class="print-desc">تصميم وجهين، صيغ AI / PDF / PNG</div>
    </div>
    <div class="print-card">
      <span class="print-icon">📄</span>
      <div class="print-name">ورق رسمي</div>
      <div class="print-desc">مفتوح على Word وقابل للتعديل</div>
    </div>
    <div class="print-card">
      <span class="print-icon">✉️</span>
      <div class="print-name">أظرف رسمية</div>
      <div class="print-desc">مقاسات قياسية جاهزة للطباعة</div>
    </div>
    <div class="print-card">
      <span class="print-icon">📁</span>
      <div class="print-name">فولدر</div>
      <div class="print-desc">وجهان — أمامي وخلفي</div>
    </div>
    <div class="print-card">
      <span class="print-icon">🧾</span>
      <div class="print-name">فاتورة رسمية</div>
      <div class="print-desc">تصميم احترافي قابل للتعديل</div>
    </div>
    <div class="print-card">
      <span class="print-icon">📥</span>
      <div class="print-name">سند قبض</div>
      <div class="print-desc">نموذج رسمي موحّد الهوية</div>
    </div>
    <div class="print-card">
      <span class="print-icon">📤</span>
      <div class="print-name">سند صرف</div>
      <div class="print-desc">نموذج رسمي موحّد الهوية</div>
    </div>
    <div class="print-card">
      <span class="print-icon">🔏</span>
      <div class="print-name">ختم رسمي</div>
      <div class="print-desc">دائري أو مستطيل، PNG + AI</div>
    </div>
  </div>
</section>

<div class="full-divider"></div>

<!-- ═══ COMPANY PROFILE ═══ -->
<section class="section">
  <div class="section-header">
    <div class="section-tag">البروفايل التعريفي</div>
    <h2 class="section-title">بروفايل احترافي<br><span>يُقدّم مكتبكم بثقة</span></h2>
  </div>

  <div class="profile-card">
    <div class="profile-icon-wrap">📑</div>
    <div class="profile-body">
      <div class="profile-title">بروفايل مكتب المحاماة</div>
      <div class="profile-desc">
        تصميم بروفايل PDF احترافي متعدد الصفحات، يعرّف بنشاط المكتب ومجالات الممارسة والخدمات القانونية المقدَّمة، بصياغة بصرية تليق بثقة العملاء وهيبة المهنة.
      </div>
      <div class="profile-feats">
        <span class="profile-feat-tag">تصميم متعدد الصفحات</span>
        <span class="profile-feat-tag">صيغة PDF جاهزة للمشاركة</span>
        <span class="profile-feat-tag">متوافق مع هوية المطبوعات</span>
      </div>
    </div>
  </div>
</section>

<div class="full-divider"></div>

<!-- ═══ PAYMENT / INVOICE ═══ -->
<section class="payment-section">
  <div class="section-header" style="margin-bottom:40px;">
    <div class="section-tag">التسعير والدفع</div>
    <h2 class="section-title">عرض واضح<br><span>بلا تعقيد</span></h2>
  </div>

  <div class="invoice-table">
    <div class="inv-table-head">
      <div class="inv-client-col">
        <span class="inv-client-label">العميل</span>
        <span class="inv-client-name">المحامية العنود</span>
      </div>
      <div class="inv-total-col">
        <div class="inv-total-label">الإجمالي</div>
        <div class="inv-total-amount"><span class="inv-total-currency">﷼</span>٥٠٠</div>
      </div>
    </div>

    <div class="inv-row">
      <div class="inv-row-right">
        <span class="inv-row-label">عربون بدء العمل</span>
        <span class="inv-row-note">نصف القيمة — لازم لبدء التنفيذ</span>
        <span class="required-badge">مطلوب الآن</span>
      </div>
      <div class="inv-row-amount gold">٢٥٠ ريال</div>
    </div>
    <div class="inv-row">
      <div class="inv-row-right">
        <span class="inv-row-label">المبلغ المتبقي</span>
        <span class="inv-row-note">يُسدَّد عند اكتمال التصميم</span>
      </div>
      <div class="inv-row-amount white">٢٥٠ ريال</div>
    </div>
  </div>

  <p class="inv-footer-note">
    ✦ حقوق الملكية الكاملة تنتقل إليكم · ✦ ملفات بجميع الصيغ (AI, PDF, PNG, DOCX)
  </p>
</section>

<div class="full-divider"></div>

<!-- ═══ TIMELINE ═══ -->
<section class="section">
  <div class="section-header">
    <div class="section-tag">مراحل التنفيذ</div>
    <h2 class="section-title">من الفكرة<br><span>إلى التسليم</span></h2>
  </div>
  <div class="timeline">
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ١</div>
      <div class="tl-title">استلام العربون وبدء العمل</div>
      <div class="tl-desc">نستلم شعاركم وبياناتكم، ونبدأ في تأسيس عناصر الهوية</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ٢ – ٥</div>
      <div class="tl-title">تصميم المطبوعات الأساسية</div>
      <div class="tl-desc">بطاقة الأعمال، الورق الرسمي، الأظرف، الفولدر</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ٦ – ٨</div>
      <div class="tl-title">المستندات المالية والختم</div>
      <div class="tl-desc">الفاتورة، سند القبض، سند الصرف، الختم الرسمي</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ٩ – ١١</div>
      <div class="tl-title">تصميم البروفايل التعريفي</div>
      <div class="tl-desc">صياغة وتصميم بروفايل المكتب الاحترافي</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ١٢</div>
      <div class="tl-title">المراجعات النهائية</div>
      <div class="tl-desc">تطبيق التعديلات لضمان رضاكم الكامل</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-day">اليوم ١٣</div>
      <div class="tl-title">التسليم النهائي بعد اكتمال التصميم</div>
      <div class="tl-desc">بعد سداد المبلغ المتبقي، تُسلَّم جميع الملفات منظمةً بكل الصيغ</div>
    </div>
  </div>
</section>

<div class="full-divider"></div>

<!-- ═══ CTA ═══ -->
<section class="cta-section">
  <h2>جاهزون لنبدأ<br><span style="color:var(--gold)">معكِ يا أستاذة عنود؟ ⚖️</span></h2>
  <p>حوّلي العربون وابدئي رحلة بناء هويتكم البصرية</p>
  <a href="https://wa.me/966537441043" class="cta-btn">تواصل عبر واتساب 📲</a>
  <div class="cta-pills">
    <span class="cta-pill">🔒 دفع آمن</span>
    <span class="cta-pill">⚡ تسليم سريع</span>
    <span class="cta-pill">⚖️ تصميم يليق بالمهنة</span>
    <span class="cta-pill">🔄 مراجعات مجانية</span>
    <span class="cta-pill">📁 ملفات كاملة بكل الصيغ</span>
  </div>
</section>

<div class="full-divider"></div>
<footer class="footer">
  <div class="footer-brand"><span>نِداد</span> للتصاميم والجرافيكس</div>
  <div class="footer-phone">+966 537 441 043</div>
</footer>

<script>
  const now = new Date();
  const mm = String(now.getMonth()+1).padStart(2,'0');
  const dd = String(now.getDate()).padStart(2,'0');
  const yy = String(now.getFullYear()).slice(2);
  document.getElementById('inv-num').textContent = yy + mm + dd + '03';

  const opts = { year:'numeric', month:'long', day:'numeric' };
  const ar = now.toLocaleDateString('ar-SA', opts);
  document.getElementById('inv-date').textContent = ar;
  document.getElementById('client-date').textContent = ar;
</script>

</body>
</html>

عرض سعر تصميم هوية بصرية
