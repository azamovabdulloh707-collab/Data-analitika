# Power BI dashboard — Titanic

## Ma’lumot

`output.xlsx` faylidagi `Clean_Data` varag‘ini Power BI Desktop’da import qiling (yoki `Titanic_PowerBI.csv`ni oching). Datasetda 891 yo‘lovchi bor. `Age_original` boshlang‘ich yoshni saqlaydi; `Age` esa bo‘sh qiymatlari 29.6991 o‘rtacha bilan to‘ldirilib, butun songa yaxlitlangan ustun. `age_category` yosh guruhidir.

Power Query’da `Pclass`, `Survived`, `Age`, `SibSp`, `Parch`, `PassengerId` ustunlarini Whole number; `Fare`ni Decimal number; `age_category`, `Sex` va boshqa matn ustunlarini Text qilib belgilang.

## DAX measures

```DAX
Yo'lovchilar = COUNTROWS('Clean_Data')

Omon qolganlar =
CALCULATE([Yo'lovchilar], 'Clean_Data'[Survived] = 1)

Omon qolmaganlar =
CALCULATE([Yo'lovchilar], 'Clean_Data'[Survived] = 0)

Omon qolish ulushi =
DIVIDE([Omon qolganlar], [Yo'lovchilar], 0)
```

`Omon qolish ulushi` formatini Percentage, 1–2 decimal place qilib sozlang.

## Dashboard maketi

1. KPI cards: `Yo'lovchilar`, `Omon qolganlar`, `Omon qolish ulushi`.
2. Clustered column chart: X-axis `Pclass`, values `Omon qolganlar` va `Omon qolmaganlar`.
3. Bar chart: Y-axis `Pclass`, X-axis `Omon qolish ulushi`.
4. Bar chart: Y-axis `age_category`, X-axis `Omon qolish ulushi`.
5. Matrix: rows `age_category`, columns `Pclass`, values `Omon qolish ulushi`; conditional formatting qo‘shing.
6. Slicers: `age_category`, `Sex`, `Pclass`. Shu bilan rahbar so‘ragan yosh va sinf bo‘yicha filtrlash ishlaydi.

## Topshiriq qaydlari

- Maqsad: omon qolish sinf va yoshga bog‘liq bo‘lganini ko‘rish.
- Yosh guruhlari: Children ≤14; Youth&Adults 15–64; Seniors ≥65.
- Omon qolganlar soni va ulushi sinf bo‘yicha alohida ko‘rsatiladi.
- Hisoblangan sinf ulushlari: 1-sinf 62.96%; 2-sinf 47.28%; 3-sinf 24.24%.
- Natijalar tavsifiy kuzatuvdir; sinf farqi sababiyatni o‘zi bilan isbotlamaydi. Age mean-imputation guruhlar tarkibiga ta’sir qilishi mumkin.
