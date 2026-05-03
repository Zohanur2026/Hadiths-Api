# Islamic Hadith Database API

A comprehensive JSON database of authentic Islamic hadiths in 9 languages.

## 📚 Collections (10 Books)

| Collection | Arabic Name | Hadiths | Grade |
|------------|-------------|---------|-------|
| Sahih al-Bukhari | صحيح البخاري | 7,563 | Sahih ✅ |
| Sahih Muslim | صحيح مسلم | 7,453 | Sahih ✅ |
| Sunan Abu Dawud | سنن أبي داود | 5,274 | Hasan/Sahih |
| Jami at-Tirmidhi | جامع الترمذي | 3,956 | Hasan/Sahih |
| Sunan an-Nasai | سنن النسائي | 5,761 | Hasan/Sahih |
| Sunan Ibn Majah | سنن ابن ماجه | 4,341 | Mixed |
| Muwatta Malik | موطأ مالك | 1,832 | Sahih ✅ |
| Forty Hadith an-Nawawi | الأربعون النووية | 42 | Sahih ✅ |
| Forty Hadith Qudsi | الأربعون القدسية | 40 | Sahih ✅ |
| Forty Hadith Dehlawi | أربعون الدهلوي | 40 | Sahih ✅ |

## 🌍 Languages (9)

🇺🇸 English · 🇸🇦 Arabic · 🇵🇰 Urdu · 🇮🇳 Tamil · 🇧🇩 Bengali · 🇹🇷 Turkish · 🇫🇷 French · 🇮🇩 Indonesian · 🇷🇺 Russian

## 🚀 Usage

### Via jsDelivr CDN (Free, Global, Fast)

```javascript
// Fetch Bukhari in English
const response = await fetch(
  'https://cdn.jsdelivr.net/gh/Zohanur2026/Hadiths-Api@main/editions/eng-bukhari.json'
);
const data = await response.json();

console.log(`Total: ${data.hadiths.length} hadiths`);
```

### Available Endpoints

Format: `https://cdn.jsdelivr.net/gh/Zohanur2026/Hadiths-Api@main/editions/{lang}-{collection}.json`

**Languages:** `eng`, `ara`, `urd`, `tam`, `ben`, `tur`, `fra`, `ind`, `rus`

**Collections:** `bukhari`, `muslim`, `abudawud`, `tirmidhi`, `nasai`, `ibnmajah`, `malik`, `nawawi`, `qudsi`, `dehlawi`

## 📱 React Native Example

```javascript
async function fetchHadiths(collection, language = 'eng') {
  const url = `https://cdn.jsdelivr.net/gh/Zohanur2026/Hadiths-Api@main/editions/${language}-${collection}.json`;
  const response = await fetch(url);
  const data = await response.json();
  return data.hadiths;
}

// Use it
const bukhari = await fetchHadiths('bukhari', 'eng');
```

## 📄 License

Data sourced from sunnah.com - Public Domain

---

**May Allah accept this work and make it beneficial. Ameen.**
