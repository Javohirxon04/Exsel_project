


🍕 Pizza Sales Data Analysis
📌 Loyiha haqida
Ushbu loyiha pizza savdo ma'lumotlarini Python yordamida tahlil qilishga bag'ishlangan.
Loyihaning asosiy maqsadi — savdo ma'lumotlaridan asosiy KPI ko'rsatkichlarini hisoblash, vaqt bo'yicha savdo tendensiyalarini aniqlash, pizza kategoriyalari va o'lchamlarini taqqoslash hamda eng ko'p sotilgan pizzalarni aniqlash.

Loyiha Data Analysis / Data Science portfolio uchun tayyorlangan.

🛠 Foydalanilgan texnologiyalar
Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

Data Cleaning & Transformation

GroupBy & Aggregation

Pivot Table

Data Visualization

📂 Dataset
Tahlilda pizza_sales.csv datasetidan foydalanildi.

Dataset bilan ishlashning boshlang'ich bosqichida:

dastlabki qatorlar head() orqali ko'rildi;

dataset hajmi shape orqali tekshirildi;

ustun nomlari ko'rib chiqildi;

info() va dtypes orqali ma'lumot turlari tekshirildi;

describe() orqali sonli ustunlarning statistik tavsifi ko'rildi.

🎯 Hisoblangan KPI ko'rsatkichlari
Loyihada quyidagi asosiy biznes KPI'lari hisoblandi:

Total Revenue — jami savdo tushumi

Total Pizzas Sold — jami sotilgan pizzalar soni

Total Orders — unique buyurtmalar soni

Average Pizzas per Order — bitta buyurtmaga o'rtacha nechta pizza to'g'ri kelishi

KPI hisoblashda sum() va nunique() kabi Pandas agregatsiya funksiyalaridan foydalanildi.

🔍 Bajarilgan tahlillar
1. Ingredientlar tahlili
pizza_ingredients ustunidagi ingredientlar:

str.split(',') yordamida ajratildi;

explode() yordamida alohida qatorlarga chiqarildi;

value_counts() yordamida eng ko'p uchraydigan ingredientlar hisoblandi.

Bu tahlil orqali pizzalarda eng ko'p ishlatiladigan ingredientlarni aniqlash imkoniyati yaratildi.

2. Hafta kunlari bo'yicha buyurtmalar
order_date ustuni datetime formatiga o'tkazildi va undan hafta kuni olindi.

groupby() va order_id.nunique() yordamida:

Haftaning har bir kunida nechta unique buyurtma berilgani

hisoblandi va bar chart orqali vizualizatsiya qilindi.

3. Hafta kunlari bo'yicha Revenue
Hafta kunlari bo'yicha total_price qiymatlari yig'ilib:

Har bir hafta kunida qancha jami tushum olingani

tahlil qilindi.

4. Soatlar bo'yicha buyurtmalar
order_time ustunidan buyurtma berilgan soat ajratildi.

Har bir soat uchun unique order_id soni hisoblanib, kun davomida buyurtmalar faolligi tahlil qilindi.

Bu analiz orqali peak hours, ya'ni buyurtmalar eng ko'p beriladigan soatlarni aniqlash mumkin.

5. Oylar bo'yicha buyurtmalar
order_date ustunidan oy nomlari yaratildi va January → December tartibida kategoriyalandi.

Har bir oy uchun unique buyurtmalar soni hisoblanib, line/area chart orqali oylik trend ko'rsatildi.

6. Pizza kategoriyalari bo'yicha savdo
Pizzalar pizza_category bo'yicha guruhlanib, har bir kategoriyaning jami total_price qiymati hisoblandi.

Natijalar foizga aylantirilib, donut/pie chart orqali kategoriyalarning umumiy savdodagi ulushi ko'rsatildi.

7. Pizza kategoriyasi va o'lchami bo'yicha savdo
pivot_table() yordamida:

qatorlarda — pizza_category;

ustunlarda — pizza_size;

qiymat sifatida — total_price

ishlatildi.

Har bir Category + Size kombinatsiyasining umumiy savdodagi foiz ulushi hisoblanib, Seaborn heatmap yordamida vizualizatsiya qilindi.

8. Kategoriya bo'yicha sotilgan pizza miqdori
pizza_category bo'yicha quantity.sum() hisoblanib:

Har bir kategoriyadan jami nechta pizza sotilgani

bar chart orqali ko'rsatildi.

9. Top 5 eng ko'p sotilgan pizzalar
Har bir pizza_name bo'yicha quantity yig'ildi, natijalar kamayish tartibida saralandi va head(5) orqali:

Sotilgan pizza miqdori bo'yicha TOP-5 pizza

aniqlandi.

10. Top 5 eng ko'p buyurtma qilingan pizzalar
Har bir pizza nomi bo'yicha unique order_id soni hisoblandi va eng yuqori natijaga ega 5 ta pizza ajratildi.

Bu tahlil sotilgan dona soni va buyurtmalarda qatnashish soni o'rtasidagi farqni ko'rishga yordam beradi.

📊 Vizualizatsiyalar
Loyihada quyidagi grafiklardan foydalanildi:

Bar Chart

Line Chart

Area/Filled Trend Chart

Pie / Donut Chart

Heatmap

Grafiklarda qiymat label'lari, sarlavhalar va o'q nomlari qo'shilib, natijalarni tushunarli ko'rinishda taqdim etishga e'tibor berildi.

💡 Loyihada qo'llanilgan Data Analytics ko'nikmalari
Datasetni tekshirish va tushunish

Datetime bilan ishlash

Feature yaratish (day_name, order_hour, month_name)

groupby() orqali ma'lumotlarni guruhlash

sum() va nunique() orqali agregatsiya

sort_values() orqali ranking

String ma'lumotlarini split() va explode() bilan qayta ishlash

Pivot Table yaratish

Foiz ko'rsatkichlarini hisoblash

KPI hisoblash

Savdo trendlarini tahlil qilish

Matplotlib va Seaborn yordamida vizualizatsiya

Biznes savollariga data orqali javob berish

📁 Repository strukturasi
Pizza-Sales-Data-Analysis/
│
├── README.md
├── Pizza_Sales_Data_Analysis.ipynb
└── pizza_sales.csv
🚀 Loyiha maqsadi
Ushbu loyiha orqali Python yordamida savdo ma'lumotlarini tahlil qilish, asosiy biznes KPI'larini hisoblash va natijalarni vizual ko'rinishda taqdim etish bo'yicha amaliy Data Analytics ko'nikmalari namoyish etildi.
