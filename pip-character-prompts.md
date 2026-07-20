# Пип — лисёнок-изобретатель · пакет промптов для мультика

Единый герой для генерации кадров. Главное правило: **всегда вставляй BASE-блок**
(порода, цвета, комбинезон, гогглы, стиль), меняй только строку эмоции / позы /
ракурса / фона. Так персонаж не «плавает» между сценами.

---

## 0. BASE — якорь персонажа (вставляй в КАЖДЫЙ промпт)

**RU:**
> Милый детский 3D-мультяшный лисёнок по имени Пип. Стиль Pixar/DreamWorks, мягкий
> стилизованный 3D-рендер. Крупная голова к телу (~1:2, пропорции малыша), большие
> выразительные блестящие глаза с тёплой карей радужкой и мягкими бликами. Пушистая
> рыжевато-оранжевая шёрстка с сабсёрфейсом, белая грудка и кончик хвоста, чёрные
> лапки. Маленький нос-пуговка, круглые щёчки, большой пушистый хвост. Одет в
> крошечный жёлтый комбинезон с одной расстёгнутой лямкой и мультяшные гогглы,
> сдвинутые на лоб. Физически корректные материалы, детализированный мех, чистый
> силуэт, доброе детское настроение, мягкий тёплый трёхточечный свет, контровой
> ободок, ambient occlusion, global illumination. 4K.

**EN:**
> Cute children's 3D cartoon fox cub named Pip. Pixar/DreamWorks style, soft
> stylized 3D render. Large head-to-body ratio (~1:2, toddler proportions), big
> expressive glossy eyes, warm brown irises, soft catchlights. Fluffy reddish-orange
> fur with subsurface scattering, white chest and tail-tip, little black paws. Tiny
> button nose, round chubby cheeks, big fluffy tail. Wearing a tiny yellow overall
> with one strap unbuttoned and cartoon goggles pushed up on the forehead.
> Physically-based materials, detailed fur, clean silhouette, wholesome children's
> mood, soft warm three-point lighting, rim light, ambient occlusion, global
> illumination. 4K.

---

## 1. ЭМОЦИИ (меняй только выражение лица)

| # | RU (добавить к BASE) | EN (append to BASE) |
|---|----------------------|---------------------|
| Радость | широкая счастливая улыбка, зажмуренные глаза-дуги, приподнятые щёки | big happy smile, squinted arched eyes, raised cheeks |
| Удивление | огромные круглые глаза, приоткрытый рот «о», брови высоко | huge round eyes, open «o» mouth, eyebrows high |
| Любопытство | голова чуть набок, один глаз прищурен, лёгкая улыбка | head tilted, one eye squinted, slight curious smile |
| Грусть | опущенные ушки и брови, блестящие глаза, дрожащая губа | drooping ears and brows, teary shiny eyes, quivering lip |
| Испуг | расширенные зрачки, прижатые уши, шёрстка дыбом, рот открыт | dilated pupils, flattened ears, fur on end, mouth open |
| Хитрость | прищур, приподнятая бровь, ухмылка уголком рта | narrowed eyes, one raised brow, sly half-smirk |
| Смех | голова запрокинута, широкий смеющийся рот, зажмур | head thrown back, wide laughing mouth, eyes shut |
| Гордость | грудь колесом, довольная улыбка, лапки на бёдрах | chest puffed, proud smile, paws on hips |

---

## 2. ПОЗЫ И ДЕЙСТВИЯ (меняй позу)

| # | RU (добавить к BASE) | EN (append to BASE) |
|---|----------------------|---------------------|
| Стоит-заметил | стоит, наклонился вперёд, одна лапка поднята, «что-то увидел» | standing, leaning forward, one paw raised, noticing something |
| Бежит | динамичный бег в прыжке, уши и хвост назад, motion feel | dynamic mid-run leap, ears and tail streaming back |
| Прыгает | в воздухе, лапки раскинуты, радостный прыжок | mid-air joyful jump, limbs spread |
| Изобретает | сидит за крошечным верстаком, крутит гаечку, гогглы на глазах | sitting at a tiny workbench, turning a bolt, goggles down over eyes |
| Держит предмет | обеими лапками держит светящийся гаджет/фонарик | holding a glowing gadget/lantern in both paws |
| Крадётся | на цыпочках, палец у рта «тсс», хитрый взгляд | tiptoeing, finger to lips «shh», sneaky look |
| Спит | свернулся клубком, хвост обёрнут, глаза закрыты, «zzz» | curled up asleep, tail wrapped around, «zzz» |
| Машет | машет лапкой, приветливая улыбка, шаг вперёд | waving a paw, friendly smile, stepping forward |
| Падает/споткнулся | комично спотыкается, руки вразлёт, удивление | comically tripping, arms flailing, surprised |
| Думает | лапка у подбородка, глаза вверх, над головой лампочка | paw on chin, eyes up, thought lightbulb above head |

---

## 3. РАКУРСЫ КАМЕРЫ (для монтажа и разворотов)

- `full body, front 3/4 view, camera slightly below eye level` — главный «паспорт» героя
- `full body, side profile view` — вид сбоку (нужен для оборота модели)
- `full body, back view, tail visible` — вид сзади
- `close-up of face, expressive eyes` — эмоциональный крупный план
- `low angle hero shot, looking up at character` — героический ракурс
- `top-down slightly above, character looking up` — вид сверху
- `wide shot, character small in environment` — общий план в сцене

> Для оборота персонажа (turnaround) генерируй один и тот же BASE + одну и ту же
> эмоцию, меняя только строку ракурса.

---

## 4. ФОНЫ И ОКРУЖЕНИЯ

**Нейтральные (для карточек/оборота):**
> plain creamy pastel background, subtle gradient, soft contact shadow

**Сцены мультика (RU → EN):**

| Сцена | EN (добавить к BASE + поза) |
|-------|-----------------------------|
| Уютная мастерская | cozy stylized workshop, tiny tools on the wall, warm lamp glow, wooden shelves, dust motes in light |
| Волшебный лес | whimsical forest clearing, oversized glowing mushrooms, soft fireflies, dappled sunlight, painterly bokeh |
| Ночное небо | on a hill at night, big starry sky, glowing moon, cool blue tones with warm rim light on fur |
| Дом на дереве | interior of a cozy treehouse, round window, string lights, blanket fort, warm amber light |
| Луг днём | sunny flower meadow, rolling hills, fluffy clouds, butterflies, bright cheerful daylight |
| Дождливое окно | sitting by a rainy window, raindrops, soft grey light, warm cozy interior glow |
| Пещера с кристаллами | glowing crystal cave, teal and purple bioluminescence, magical sparkles, rim-lit fur |
| Городок игрушек | tiny stylized toy town street, rounded houses, lantern light, cobblestone, evening warmth |

---

## 5. NEGATIVE PROMPT (что отсекать)

> realistic photo, human, scary, deformed anatomy, extra limbs, extra eyes,
> low quality, blurry, watermark, text, signature, harsh shadows, cluttered
> background, adult, creepy, uncanny

---

## 6. СОВЕТЫ ПО КОНСИСТЕНТНОСТИ

1. **Не меняй порядок BASE-блока** — генераторы чувствительны к порядку слов.
2. Держи **фиксированную палитру**: рыжий #E8722C, белая грудка #FDF6EC, жёлтый
   комбинезон #F2C230, чёрные лапки #2B2B2B. Можешь дописывать hex прямо в промпт.
3. Один и тот же **seed** (если генератор поддерживает) = стабильное лицо.
4. Сначала утверди 1 «эталонный» кадр (BASE + front 3/4), потом ссылайся на него
   как reference-изображение для остальных поз.
5. Для мультика делай кадры **парами** (та же поза, две эмоции) — проще собирать
   переходы.
