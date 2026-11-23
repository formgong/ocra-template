# Ocra: a ceramics shop site with Formgong forms

**Live demo:** https://ocra.formgong.com · Download: the [latest release](https://github.com/formgong/ocra-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/ocra-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Focra-template&project-name=ocra&repository-name=ocra)

Each button copies the site to your GitHub and publishes it. Then replace every `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Сайт керамічної майстерні з формами Формгонг

A one-page template for a small maker who sells by message instead of a cart: ceramics, candles, bread, flowers. Everything is in a single `index.html`. The demo studio, Ocra, its pieces and its prices are fictional.

- **Header.** The logo and links, with a dark Order button. A short line below gives the place and the next firing.
- **Hero.** The name fills the width, and the O is a citrus slice that turns as you scroll. Below it are two large buttons (Shop the kiln, Book a class) and a photo that drifts slightly.
- **Orange band.** A running line of short facts.
- **The kiln.** Four product cards with orange price tags. "Order this" scrolls to the order form with that piece already selected.
- **About.** A sentence about the studio and three numbers, beside an orange panel of drawn slices that turn as you scroll.
- **Ask us.** Six rows, each with text on one side and a working form on the other:
  1. **Order a piece:** piece, quantity buttons, name, email and country. It ends on a thank-you card with a drawn tick.
  2. **Book a class:** three steps with a progress bar (time and date, experience and people, contact). Each step checks itself, and Enter moves to the next step.
  3. **Commission:** a text area that grows and counts characters, plus a drop zone for up to 3 sketches or photos of 5 MB each.
  4. **Wholesale:** choice cards (shop, café, hotel). The button goes sending → sent → ready, and the form stays on screen.
  5. **Feedback:** five faces and an optional comment.
  6. **Write to us:** floating labels on a dark card.
- **Visit.** A studio photo, opening hours and the address.
- **Newsletter.** An orange block with the email field and button in one pill and a required consent box.
- **Footer.** The wordmark again and the "Forms powered by Formgong" credit.
- **Order button.** A floating Order button appears after the hero and hides while the order form is on screen.

## English

**Set up the forms**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace every `fk_your_access_key` with that key. There are 7 forms; use find and replace.
3. Each form sends a hidden `request` field (Order, Workshop, Commission, Wholesale, Feedback, Message or Newsletter), so you can tell the messages apart in one inbox. If you want them in separate inboxes, use one Formgong form per request type.

A form shows its thank-you state only when Formgong answers `success: true`. If the answer is anything else, the form shows the error message and keeps what was typed.

**Edit**

- Colours are at the top of the styles. Change `--orange` and `--orange-soft` for the accent, and `--paper` and `--sand` for the background and cards.
- The citrus slice is one SVG `<symbol id="slice">` near the top of `<body>`. It is used in the logo, both wordmarks, the orange panel and the favicon (the favicon has its own copy in the `<link rel="icon">`).
- Products: copy an `<article class="item">` and add the same name as an `<option>` in the order form's Piece list.
- With `prefers-reduced-motion: reduce`, the slices stop turning, the band stops, and every section shows in its final state.

**Images.** The seven photos were generated for this template with ChatGPT image generation (OpenAI) and saved as WebP, about 400 KB in all. You may use them in your own site. Replace them with photos of your own work, keeping the file names. The citrus slices are drawn in SVG.

The "Powered by Formgong" links point to `https://formgong.com/review-page/fk_your_access_key`, so the same find and replace covers them. Once your key is in, the first click from your published site makes your own public review page on Formgong, where clients read and leave reviews, and every later click opens it. Switch the page off in Formgong (Reviews → your site → Settings) or change those links.

## Українська

Односторінковий шаблон для майстерні, яка продає через повідомлення, а не через кошик: кераміка, свічки, хліб, квіти. Студія Ocra, її вироби й ціни вигадані.

На сторінці по черзі:

- велика назва, де «O» — це часточка апельсина, що обертається під час прокрутки;
- дві великі кнопки й фото;
- помаранчева стрічка з короткими фактами;
- чотири вироби з цінами;
- блок про студію з намальованими часточками.

Далі блок «Ask us»: шість рядів, у кожному текст і робоча форма:

1. замовлення виробу;
2. запис на заняття в три кроки;
3. індивідуальне замовлення з ескізами (до 3 файлів по 5 МБ);
4. опт із кнопкою, що показує відправлення;
5. відгук через п'ять облич;
6. повідомлення з плаваючими підписами.

Наприкінці фото студії з годинами роботи, підписка з обов'язковою згодою і футер з підписом «Forms powered by Formgong».

**Налаштування.** Створіть форму в кабінеті Formgong і замініть усі `fk_your_access_key` у `index.html` на свій ключ (форм 7). Кожна форма надсилає приховане поле `request`, тож у спільній скриньці видно, що це: замовлення, заняття, опт тощо. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`.

**Зображення:** сім фото згенеровано для цього шаблону в ChatGPT (OpenAI) і збережено у WebP, разом близько 400 КБ. Їх можна використовувати на своєму сайті. Часточки апельсина намальовано в SVG.

MIT license.

Посилання «Powered by Formgong» ведуть на `https://formgong.com/review-page/fk_your_access_key`, тож та сама заміна ключа оновить і їх. Коли ключ стоїть, перший перехід з вашого опублікованого сайту створює вашу публічну сторінку відгуків на Formgong, де клієнти читають і залишають відгуки; далі посилання відкриває її. Вимкнути сторінку можна у Formgong (Відгуки → ваш сайт → Налаштування) або змінити ці посилання.

## More free form tools

- 14 contact form examples to copy: https://formgong.com/en/contact-form-examples/
