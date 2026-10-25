# 노후 가계부와 AI 예측 모형 (KReIS 편)

**[한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)**

---

<a id="ko"></a>
## 노후 가계부와 AI 예측 모형 — 시계열 공백 극복과 알고리즘 앙상블

국민노후보장패널데이터(KReIS)는 2년 주기로 조사·발표되어 2~3년의 '공백기'가 생깁니다. 이 페이지는 그 공백 연도의 취약 노인가구 소비·부채를 직전 패널 데이터와 물가·부동산·고령화 지표로 선제 예측하는 AI 방법을, 대화형 실습(타임라인, 전처리, 모델 비교, 조기경보 임계값, SHAP)과 네 식구의 대화로 풀어 설명하는 심층 해설 대시보드입니다.

- **바로 보기**: `01_kreis_expenditure.html`을 브라우저로 열면 바로 실행(빌드 과정 없음). GitHub Pages 배포 시: `https://adminmrobo.github.io/<저장소>/01_kreis_expenditure.html` ← `<저장소>`를 실제 저장소 이름으로 바꿔 주세요
- **저자**: 글 · 안상선 ((주)M-Robo 대표)
- **원 논문**: 안상선 (2025). 국민노후보장패널데이터를 활용한 가구 지출 예측 모델 연구: 인공지능 모델 기반 접근. *미래사회*, 16(2), 186~207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### 구성
| 파일 | 내용 |
|---|---|
| `01_kreis_expenditure.html` | 본문 — 그림 5장 base64 내장, 단독 실행 |
| `01_kreis_expenditure.en.html` ~ `.vi.html` | 6개 외국어판 (영어·中文·日本語·Oʻzbekcha·Русский·Tiếng Việt) — 같은 폴더에 나란히 둠 |
| `og_01.png` | 공유 미리보기 1200×630 (og:image, SNS 공개 시 사용) |
| `README.md` | 이 소개 (7개 언어) |
| `INDEX.md` | 파일·이미지 인덱스 |

### 페이지에서 만나는 것
0. 2~3년의 깜깜이 공백: 왜 인공지능 예측인가? (타임라인 실습)
1. 비대칭 장부와 견고한 전처리 (절사 · RobustScaler 실습)
2. 체급별 알고리즘 총출동: 선형 규제 vs 비선형 앙상블 (R² 비교 실습)
3. 위기 가구 조기경보와 임계값 (정밀도·재현율 슬라이더)
4. SHAP과 시간의 습격: 가계부의 관성 (기여도 실습)
+ 대결: 2021년 부채 예측 (ElasticNet vs RandomForest, 차이 0.0076) · 지식 색인 · 온톨로지·서지 꾸러미 (ZIP/JSON/BibTeX 내보내기)

### 핵심 숫자 (논문 실측)
- 소비지출 최대 설명력 R² 0.6656 (2015, Gradient Boosting)
- 부채금액 최대 설명력 R² 0.6105 (2021, ElasticNet — 전 연도 1위)
- 생활비 부족 최고 정확도 0.8851 (2021, 취약 가구 조기경보 모형)

### 데이터와 이미지
- 페이지의 캔버스 시뮬레이션·차트는 논문 통계 수치를 반영한 **설명용 모형**이고, KPI 숫자는 논문 실측 값입니다.
- 그림은 AI 연구실 픽셀아트 자산(16비트 RPG 그림체)이며 HTML에 base64로 내장되어 있습니다. 그림 속 글자는 `og_01.png`의 한글 제목뿐입니다.
- 등장인물: 박사 · 조수 · 초파리 연구원 · Money-Robo(연구실 로봇)

### 라이선스
크리에이티브 커먼즈 저작자표시-비영리 4.0 국제 라이선스 (CC BY-NC 4.0) — [deed.ko](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)

---

<a id="en"></a>
## Old-Age Household Ledger and AI Prediction Models — Overcoming Time-Series Gaps with Algorithm Ensembles

The Korean Retirement Income Panel (KReIS) is surveyed and published every two years, leaving "gap years" of 2–3 years with no fresh data. This page is an interactive explainer dashboard: combining past panel ledgers with macroeconomic indicators (consumer prices, real-estate prices, aging), it shows how AI can predict the consumption and debt of vulnerable elderly households in those gap years — through five hands-on labs and the four lab members' dialogue.

- **View**: open `01_kreis_expenditure.html` in a browser — no build step. On GitHub Pages: `https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← replace `<repo>` with the actual repository name
- **Author**: Written by Ahn Sangsun (CEO, M-Robo Co., Ltd.)
- **Source paper**: Ahn Sangsun (2025). Household Expenditure Prediction Using the National Old-Age Security Panel Data: An AI-Model-Based Approach. *Mirae Sahoe*, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### What's inside
| File | Content |
|---|---|
| `01_kreis_expenditure.html` | The page — 5 images embedded as base64, runs standalone |
| `01_kreis_expenditure.en.html` ~ `.vi.html` | Six translated versions (zh, ja, uz, ru, vi) — same folder, same format |
| `og_01.png` | Share preview 1200×630 (og:image, used when sharing on social media) |
| `README.md` | This readme (7 languages) |
| `INDEX.md` | File and image index |

### Sections
0. The 2–3-year dark gap: why AI prediction? (timeline lab)
1. Skewed ledgers and robust preprocessing (winsorizing · RobustScaler lab)
2. Linear regularization vs. nonlinear ensembles (R² comparison lab)
3. Early warning for at-risk households and the threshold (precision–recall slider)
4. SHAP and the attack of time: the inertia of household spending (contribution lab)
+ Duel: 2021 debt prediction (ElasticNet vs RandomForest, gap 0.0076) · Knowledge index · Ontology & bibliography package (ZIP/JSON/BibTeX export)

### Key numbers (measured in the paper)
- Best consumption-expenditure fit R² 0.6656 (2015, Gradient Boosting)
- Best debt fit R² 0.6105 (2021, ElasticNet — first place in every year)
- Highest living-cost-shortage accuracy 0.8851 (2021, early-warning model)

### Data and images
- The canvas simulations and charts are **illustrative mock-ups** built around the paper's statistics; the KPI numbers are the paper's measured values.
- Images are 16-bit RPG pixel-art lab assets embedded in the HTML as base64. The only text inside an image is the Korean title in `og_01.png`.
- Cast: the Doctor · the Assistant · the Fruit Fly Researcher · Money-Robo (the Lab Robot)

### License
Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0) — [deed.en](https://creativecommons.org/licenses/by-nc/4.0/deed.en)

---

<a id="zh"></a>
## 养老家庭账本与AI预测模型 — 克服时序空白与算法集成

国民养老保障面板数据（KReIS）每两年调查并发布一次，中间会出现2~3年的"空白年"。本页面是一个交互式讲解仪表盘：把过去的面板账本与物价、房价、老龄化等宏观指标结合起来，用AI提前预测空白年份中脆弱老年家庭的消费与债务状况，并通过五个动手实验和四位角色的对话来讲解。

- **直接查看**：用浏览器打开 `01_kreis_expenditure.html` 即可运行，无需构建。部署到 GitHub Pages 后：`https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← 请把 `<repo>` 换成实际的仓库名
- **作者**：作者 · Ahn Sangsun（M-Robo 株式会社代表）
- **原论文**：Ahn Sangsun (2025). 利用国民养老保障面板数据的家庭支出预测模型研究：基于人工智能模型的方法. *미래사회*（未来社会）, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### 文件构成
| 文件 | 内容 |
|---|---|
| `01_kreis_expenditure.html` | 正文 — 5张图片以 base64 内嵌，可独立运行 |
| `01_kreis_expenditure.zh.html` | 中文版（同文件夹，同格式） |
| `og_01.png` | 分享预览图 1200×630（og:image，社交平台分享时使用） |
| `README.md` | 本说明（7种语言） |
| `INDEX.md` | 文件与图片索引 |

### 页面内容
0. 2~3年的数据空白：为什么需要AI预测？（时间线实验）
1. 偏态账本与稳健预处理（截尾 · RobustScaler 实验）
2. 线性正则化 vs 非线性集成（R² 对比实验）
3. 危机家庭预警与阈值（精确率·召回率滑块）
4. SHAP与时间的袭击：家庭账本的惯性（贡献度实验）
+ 对决：2021年债务预测（ElasticNet vs RandomForest，差距 0.0076） · 知识索引 · 本体与书目打包（ZIP/JSON/BibTeX 导出）

### 关键数字（论文实测）
- 消费支出最高解释力 R² 0.6656（2015年，Gradient Boosting）
- 债务金额最高解释力 R² 0.6105（2021年，ElasticNet — 各年均第一）
- 生活费不足最高准确率 0.8851（2021年，预警模型）

### 数据与图片
- 页面中的画布模拟与图表是基于论文统计值的**示意模型**；KPI 数字为论文实测值。
- 插图为16位RPG像素风实验室资产，以 base64 内嵌于 HTML。图片中唯一的文字是 `og_01.png` 中的韩文标题。
- 角色：博士 · 助手 · 果蝇研究员 · Money-Robo（研究室机器人）

### 许可
知识共享 署名-非商业性使用 4.0 国际许可协议（CC BY-NC 4.0） — [deed](https://creativecommons.org/licenses/by-nc/4.0/deed.zh-hans)

---

<a id="ja"></a>
## 高齢期家計簿とAI予測モデル — 時系列の空白克服とアルゴリズムのアンサンブル

国民老後保障パネルデータ（KReIS）は2年周期で調査・公表されるため、2〜3年の「空白年」が生じます。このページは、過去のパネル帳簿と物価・不動産・高齢化などのマクロ指標を組み合わせて、空白年の脆弱な高齢世帯の消費と負債を事前に予測するAIの手法を、5つの体験型実習と4人の仲間の対話で解説するインタラクティブ・ダッシュボードです。

- **すぐ見る**：`01_kreis_expenditure.html` をブラウザで開くだけ（ビルド不要）。GitHub Pages 配置後：`https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← `<repo>` は実際のリポジトリ名に置き換えてください
- **著者**：文・アン・サンソン（株式会社M-Robo代表）
- **原論文**：アン・サンソン (2025). 国民老後保障パネルデータを活用した世帯支出予測モデルの研究：AIモデルに基づくアプローチ. *미래사회*（未来社会）, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### 構成
| ファイル | 内容 |
|---|---|
| `01_kreis_expenditure.html` | 本文 — 画像5枚をbase64で内蔵、単体で動作 |
| `01_kreis_expenditure.ja.html` | 日本語版（同じフォルダ、同じ形式） |
| `og_01.png` | シェア用プレビュー 1200×630（og:image、SNS共有時に使用） |
| `README.md` | この紹介（7言語） |
| `INDEX.md` | ファイル・画像インデックス |

### ページで出会うもの
0. 2〜3年の暗い空白：なぜAI予測なのか（タイムライン実習）
1. 非対称な帳簿と頑健な前処理（刈り込み・RobustScaler 実習）
2. 線形正則化 vs 非線形アンサンブル（R² 比較実習）
3. 危機世帯の早期警戒としきい値（適合率・再現率スライダー）
4. SHAPと時間の襲撃：家計簿の慣性（寄与度実習）
+ 対決：2021年負債予測（ElasticNet vs RandomForest、差 0.0076） · 知識インデックス · オントロジー・書誌パック（ZIP/JSON/BibTeX 書き出し）

### キー数値（論文の実測値）
- 消費支出の最大説明力 R² 0.6656（2015年、Gradient Boosting）
- 負債額の最大説明力 R² 0.6105（2021年、ElasticNet — 全年次1位）
- 生活費不足の最高精度 0.8851（2021年、早期警戒モデル）

### データと画像
- ページ内のキャンバスのシミュレーションやチャートは論文の統計値を反映した**説明用の模型**で、KPI数値は論文の実測値です。
- 画像は16ビットRPG風ピクセルアートの実験室アセットで、HTMLにbase64で埋め込まれています。画像内の文字は `og_01.png` の韓国語タイトルのみです。
- 登場人物：博士 · 助手 · ショウジョウバエ研究員 · Money-Robo（研究室ロボット）

### ライセンス
クリエイティブ・コモンズ 表示-非営利 4.0 国際ライセンス（CC BY-NC 4.0） — [deed](https://creativecommons.org/licenses/by-nc/4.0/deed.ja)

---

<a id="uz"></a>
## Keksalik uy xoʻjaligi daftari va AI prognoz modeli — vaqt qatoridagi boʻshliqlarni yengish va algoritmlar ansambli

KReIS milliy keksalik kafolati panel maʼlumotlari har ikki yilda oʻtkaziladi va eʼlon qilinadi, shuning uchun 2–3 yillik "boʻsh yillar" hosil boʻladi. Bu sahifa — oʻtgan panel daftarlarini isteʼmol narxi, koʻchmas mulk va qarish koʻrsatkichlari bilan birlashtirib, boʻsh yillardagi noqulay keksa oilalarning isteʼmoli va qarzini oldindan bashorat qilishning AI uslubini besh amaliy mashgʻulot va toʻrt qahramon suhbati orqali tushuntiruvchi interaktiv dashboard.

- **Koʻrish**: `01_kreis_expenditure.html` faylni brauzerda oching — qurish bosqichi yoʻq. GitHub Pages: `https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← `<repo>` oʻrniga haqiqiy repozitoriya nomini yozing
- **Muallif**: Muallif · Ahn Sangsun (M-Robo kompaniyasi rahbari)
- **Asl maqola**: Ahn Sangsun (2025). KReIS panel maʼlumotlariga asoslangan oila xarajatlari prognoz modeli tadqiqoti: AI modellari asosidagi yondashuv. *Mirae Sahoe*, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### Tarkib
| Fayl | Mazmun |
|---|---|
| `01_kreis_expenditure.html` | Asosiy sahifa — 5 ta rasm base64 sifatida ichida, mustaqil ishlaydi |
| `01_kreis_expenditure.uz.html` | Oʻzbekcha versiya (bir xil papka, bir xil format) |
| `og_01.png` | Ulashish oldindan koʻrinishi 1200×630 (og:image, ijtimoiy tarmoqlarda) |
| `README.md` | Ushbu kirish (7 til) |
| `INDEX.md` | Fayl va rasm indeksi |

### Sahifa boʻlimlari
0. 2–3 yillik qorongʻi boʻshliq: nega AI bashorati? (vaqt chizigʻi mashgʻuloti)
1. Qiyshiq daftar va barqaror oldindan ishlov (kesish · RobustScaler mashgʻuloti)
2. Chiziqli regulyarlash va nochiziqli ansambl (R² taqqoslash mashgʻuloti)
3. Xavf ostidagi oilalarni erta ogohlantirish va chegara qiymati (aniqlik · qamrov slayderi)
4. SHAP va vaqt hujumi: uy daftarining inersiyasi (hissa mashgʻuloti)
+ Duel: 2021-yil qarz bashorati (ElasticNet va RandomForest, farq 0.0076) · Bilim indeksi · Ontologiya va bibliografiya paketi (ZIP/JSON/BibTeX eksporti)

### Asosiy raqamlar (maqolada oʻlchangan)
- Isteʼmol xarajatlarining eng katta tushuntirish kuchi R² 0.6656 (2015, Gradient Boosting)
- Qarz miqdorining eng katta tushuntirish kuchi R² 0.6105 (2021, ElasticNet — har yili 1-oʻrin)
- Tiriklik xarajati yetishmasligining eng yuqori aniqligi 0.8851 (2021, erta ogohlantirish modeli)

### Maʼlumot va rasmlar
- Sahifadagi canvas simulyatsiya va diagrammalar maqola statistikasi asosidagi **tushuntirish maketi**; KPI raqamlari maqolaning oʻlchangan qiymatlari.
- Rasmlar 16-bit RPG piksel-art laboratoriya aktivlari, HTML ichiga base64 bilan joylangan. Rasmdagi yagona matn — `og_01.png` dagi koreys sarlavha.
- Qahramonlar: Doktor · Yordamchi · Drozofila tadqiqotchisi · Money-Robo (Laboratoriya roboti)

### Litsenziya
Creative Commons Attribution-NonCommercial 4.0 International litsenziyasi (CC BY-NC 4.0) — [deed](https://creativecommons.org/licenses/by-nc/4.0/deed.en)

---

<a id="ru"></a>
## Домашний бюджет пожилых и ИИ-модель прогнозирования — преодоление пробелов во временных рядах и ансамбль алгоритмов

Панельные данные национальной программы пенсионного обеспечения (KReIS) собираются и публикуются раз в два года, поэтому возникают «пустые годы» длиной в 2–3 года. Эта страница — интерактивный разбор-дашборд: комбинируя прошлые панельные бюджеты с макропоказателями (потребительские цены, цены на жильё, старение населения), она объясняет, как ИИ заранее прогнозирует потребление и долги уязвимых пожилых домохозяйств в пустые годы, — через пять практических опытов и диалог четырёх персонажей.

- **Открыть**: `01_kreis_expenditure.html` в браузере — сборка не нужна. На GitHub Pages: `https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← замените `<repo>` на имя репозитория
- **Автор**: Автор · Ан Сансон (генеральный директор M-Robo Co., Ltd.)
- **Исходная статья**: Ан Сансон (2025). Исследование модели прогнозирования расходов домохозяйств на основе панельных данных KReIS: подход на базе ИИ-моделей. *Mirae Sahoe*, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### Состав
| Файл | Содержание |
|---|---|
| `01_kreis_expenditure.html` | Страница — 5 изображений встроены base64, работает автономно |
| `01_kreis_expenditure.ru.html` | Русская версия (та же папка, тот же формат) |
| `og_01.png` | Превью для обмена 1200×630 (og:image, для соцсетей) |
| `README.md` | Этот readme (7 языков) |
| `INDEX.md` | Индекс файлов и изображений |

### Разделы страницы
0. Тёмный пробел в 2–3 года: зачем ИИ-прогноз? (лаборатория таймлайна)
1. Асимметричный бюджет и устойчивая предобработка (усечение · RobustScaler)
2. Линейная регуляризация против нелинейного ансамбля (сравнение R²)
3. Раннее предупреждение о кризисных домохозяйствах и порог (слайдер точности/полноты)
4. SHAP и нападение времени: инерция семейного бюджета (лаборатория вкладов)
+ Дуэль: прогноз долгов за 2021 год (ElasticNet против RandomForest, разрыв 0.0076) · Указатель знаний · Пакет онтологии и библиографии (экспорт ZIP/JSON/BibTeX)

### Ключевые числа (измерены в статье)
- Лучшая объясняющая способность по расходам R² 0.6656 (2015, Gradient Boosting)
- Лучшая объясняющая способность по долгам R² 0.6105 (2021, ElasticNet — первое место во все годы)
- Высшая точность «не хватает на жизнь» 0.8851 (2021, модель раннего предупреждения)

### Данные и изображения
- Симуляции и графики на canvas — **иллюстративный макет** на основе статистики статьи; числа KPI — измеренные значения статьи.
- Изображения — пиксель-арт лабораторные ассеты (16-битный RPG-стиль), встроены в HTML как base64. Единственный текст на изображении — корейский заголовок в `og_01.png`.
- Персонажи: Доктор · Ассистент · Исследователь-дрозофила · Money-Robo (Робот лаборатории)

### Лицензия
лицензия Creative Commons «Атрибуция — Некоммерческое использование» 4.0 Международная (CC BY-NC 4.0) — [deed](https://creativecommons.org/licenses/by-nc/4.0/deed.ru)

---

<a id="vi"></a>
## Sổ chi tiêu tuổi già và mô hình dự đoán AI — vượt qua khoảng trống chuỗi thời gian và tập hợp thuật toán

Dữ liệu bảng quốc gia bảo đảm tuổi già (KReIS) được khảo sát và công bố theo chu kỳ hai năm nên xuất hiện những "năm trống" kéo dài 2–3 năm. Trang này là bảng điều khiển giải thích tương tác: kết hợp sổ bảng những năm trước với các chỉ số vĩ mô (giá tiêu dùng, giá bất động sản, già hóa dân số) để dự báo trước tình trạng tiêu dùng và nợ của các hộ già yếu trong năm trống — qua năm thực hành trực tiếp và đối thoại của bốn thành viên.

- **Xem ngay**: mở `01_kreis_expenditure.html` bằng trình duyệt — không cần build. Khi triển khai GitHub Pages: `https://adminmrobo.github.io/<repo>/01_kreis_expenditure.html` ← thay `<repo>` bằng tên kho lưu trữ thực tế
- **Tác giả**: Tác giả · Ahn Sangsun (Giám đốc điều hành, M-Robo Co., Ltd.)
- **Bài báo gốc**: Ahn Sangsun (2025). Nghiên cứu mô hình dự đoán chi tiêu hộ gia đình dựa trên dữ liệu bảng KReIS: cách tiếp cận dựa trên mô hình AI. *Mirae Sahoe*, 16(2), 186–207. [doi:10.22987/jifso.2025.16.2.186](https://doi.org/10.22987/jifso.2025.16.2.186)

### Cấu trúc
| Tệp | Nội dung |
|---|---|
| `01_kreis_expenditure.html` | Trang chính — 5 ảnh nhúng base64, chạy độc lập |
| `01_kreis_expenditure.vi.html` | Bản tiếng Việt (cùng thư mục, cùng định dạng) |
| `og_01.png` | Ảnh xem trước chia sẻ 1200×630 (og:image, dùng khi chia sẻ mạng xã hội) |
| `README.md` | Bài giới thiệu này (7 ngôn ngữ) |
| `INDEX.md` | Chỉ mục tệp và ảnh |

### Các phần của trang
0. Khoảng trống tối 2–3 năm: vì sao cần dự đoán bằng AI? (thực hành dòng thời gian)
1. Sổ lệch và tiền xử lý bền vững (cắt tỉa · RobustScaler)
2. Điều chỉnh tuyến tính vs tập hợp phi tuyến (so sánh R²)
3. Cảnh báo sớm hộ gia đình khủng hoảng và ngưỡng (trượt precision–recall)
4. SHAP và cơn tấn công của thời gian: quán tính của sổ chi tiêu (thực hành đóng góp)
+ Đấu: dự đoán nợ năm 2021 (ElasticNet vs RandomForest, chênh 0.0076) · Chỉ mục kiến thức · Gói bản thể luận và thư mục (xuất ZIP/JSON/BibTeX)

### Số liệu chính (đo trong bài báo)
- Khả năng giải thích cao nhất cho chi tiêu R² 0.6656 (2015, Gradient Boosting)
- Khả năng giải thích cao nhất cho nợ R² 0.6105 (2021, ElasticNet — nhất mọi năm)
- Độ chính xác cao nhất "thiếu tiền sinh hoạt" 0.8851 (2021, mô hình cảnh báo sớm)

### Dữ liệu và hình ảnh
- Mô phỏng và biểu đồ canvas trên trang là **mô hình minh họa** dựa trên số liệu thống kê của bài báo; số KPI là giá trị đo thực tế của bài báo.
- Hình ảnh là tài nguyên phòng thí nghiệm pixel art 16-bit, nhúng vào HTML dưới dạng base64. Chữ duy nhất trong ảnh là tiêu đề tiếng Hàn trong `og_01.png`.
- Nhân vật: Tiến sĩ · Trợ lý · Nhà nghiên cứu Ruồi giấm · Money-Robo (Robot phòng thí nghiệm)

### Giấy phép
Giấy phép Creative Commons Ghi công – Phi thương mại 4.0 Quốc tế (CC BY-NC 4.0) — [deed](https://creativecommons.org/licenses/by-nc/4.0/deed.vi)

---

> **참고 (검수 상태)**: README의 영어·중국어·일본어·우즈베크어·러시아어·베트남어 부분은 기계 번역 초안입니다. 특히 우즈베크어·러시아어·베트남어는 원어민 검수를 권장합니다. (Note: the six non-Korean sections above are machine-drafted translations and should get a native-speaker review before wide distribution.)
