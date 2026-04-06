# DOXY TECH - Dashboard מנהלים

מערכת ניהול פרויקטים סולאריים עם חיבור ל-Supabase, Zoho CRM, Gemini AI ו-Resend Email.

## 🚀 העלאה ל-Vercel - 3 אפשרויות

### אופציה 1: Drag & Drop (הכי מהיר - 2 דקות) ⭐

1. היכנס ל-https://vercel.com/new
2. הירשם עם Google/GitHub (חינם)
3. לחץ **"Deploy"** או גרור את התיקייה עם `index.html` + `vercel.json` לעמוד
4. תוך 30 שניות תקבל URL כמו `https://your-project.vercel.app`

### אופציה 2: GitHub + Vercel (מומלץ לטווח ארוך)

1. צור repository חדש ב-https://github.com/new בשם `doxytech-dashboard`
2. העלה את הקבצים: `index.html`, `vercel.json`, `README.md`
3. ב-Vercel לחץ **"Import Git Repository"**
4. בחר את ה-repo → **Deploy**
5. כל עדכון עתידי - פשוט push ל-GitHub והאתר מתעדכן אוטומטית

### אופציה 3: Vercel CLI (למפתחים)

```bash
npm i -g vercel
cd /path/to/files
vercel deploy --prod
```

## 🔗 חיבורים פעילים

| שירות | סטטוס | תפקיד |
|---|---|---|
| **Supabase** | ✅ פעיל | Database בענן (Frankfurt) |
| **Zoho CRM** | ✅ פעיל | סנכרון לקוחות |
| **Gemini 2.5 Flash** | ✅ פעיל | עוזר AI (חינם) |
| **Resend Email** | ✅ פעיל | התראות deadline |

## 📋 תכונות המערכת

### ✨ ניהול לקוחות
- הוספה/עריכה/מחיקה של לקוחות
- מעקב אחרי 12 שלבים בתהליך
- סיווג לפי OFF GRID / ON GRID / HYBRID
- מעקב אחרי חסמים ופעולות הבאות

### 🔔 התראות אוטומטיות
- זיהוי deadlines מתקרבים (7 ימים)
- שליחת מייל מעוצב למנהל
- רישום היסטוריית התראות

### 🤖 עוזר AI (Gemini 2.5 Flash)
- שואל שאלות על המצב הכללי
- מקבל המלצות פרקטיות
- מזהה לקוחות דחופים
- מציע איחוד הובלות

### 🔗 אינטגרציית Zoho CRM
- סנכרון ידני של לקוחות ל-Zoho
- יצירת Leads אוטומטית
- מעקב אחרי סטטוס סנכרון

### 📄 ייצוא PDF
- הפקת דוח מעוצב לכל לקוח
- מוכן לשליחה למנהל

## 🔐 הגדרות אבטחה חשובות

### לפני עלייה לייצור - החלף את ה-API Keys:

1. **Gemini**: https://aistudio.google.com/app/apikey
2. **Resend**: https://resend.com/api-keys
3. **Zoho**: https://api-console.zoho.com

אחרי שתיצור keys חדשים, עדכן אותם ב-Supabase:

```sql
UPDATE settings 
SET value = jsonb_set(value, '{gemini_api_key}', '"YOUR_NEW_KEY"')
WHERE key = 'api_keys';
```

## 📊 Supabase Project Details

- **Project ID**: `hcmmtmfzdgzdisobvpav`
- **URL**: `https://hcmmtmfzdgzdisobvpav.supabase.co`
- **Region**: Frankfurt (eu-central-1)
- **Dashboard**: https://supabase.com/dashboard/project/hcmmtmfzdgzdisobvpav

## 🛠️ Edge Functions פעילות

1. **ai-assistant** - עוזר AI מבוסס Gemini/Claude
2. **deadline-notifications** - שליחת התראות מייל
3. **zoho-sync** - סנכרון ל-Zoho CRM
4. **zoho-exchange-code** - החלפת OAuth tokens

## 📞 תמיכה

למידע נוסף או שאלות, פנה ל-ahmad@doxy-tech.com

---

**נבנה במיוחד עבור DOXY TECH** ☀️
