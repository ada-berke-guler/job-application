---
name: "Neo-Brutalist Stüdyo — Başvuru Takip"
description: "Yüksek kontrastlı, kalın mürekkep çerçeveli ve sert ofset gölgeli Neo-Brutalist Stüdyo tasarım sistemi."
---

## Overview

Başvuru Takip'in Neo-Brutalist Stüdyo kimliği, iş arama sürecini sıradan bir tablo takibinden çıkarıp enerjik, net ve kararlı bir stüdyo panosuna dönüştürür. Sıcak krem kağıt zemini üzerinde kalın 2px siyah çerçeveler, kobalt mavisi ana aksiyonlar, kadife sarısı gündem vurguları ve mercan/nane durum etiketleriyle her kart ve buton dokunsal bir netlik taşır.

## Colors

Renk paleti, okunabilirliği ve hiyerarşiyi maksimumda tutmak için yüksek kontrastlı mürekkep siyahı ile canlı risografi tonlarını birleştirir.

- **Primary (Cobalt):** Ana eylem butonları, odak halkaları ve aktif etkileşimler için kullanılır.
- **Accent (Marigold):** Bugünün gündemi, aktif sekme vurguları ve dikkat çekici çağrılar için kullanılır.
- **Status Tones:** Nane yeşili (Teklif / Uzaktan), Mercan (Yüksek öncelik / Bugün), Leylak (Ön görüşme).

```yaml
colors:
  primary: "#233DFF"
  on-primary: "#FFFFFF"
  secondary: "#FFC700"
  on-secondary: "#111111"
  cream: "#FFFDF5"
  surface: "#FFFFFF"
  on-surface: "#111111"
  ink: "#111111"
  ink-soft: "#4B4B4B"
  cobalt: "#233DFF"
  on-cobalt: "#FFFFFF"
  cobalt-soft: "#E6E9FF"
  on-cobalt-soft: "#111111"
  marigold: "#FFC700"
  on-marigold: "#111111"
  marigold-soft: "#FFF4CC"
  on-marigold-soft: "#111111"
  coral: "#D91E48"
  on-coral: "#FFFFFF"
  coral-soft: "#FFE5EA"
  on-coral-soft: "#111111"
  mint: "#00D084"
  on-mint: "#111111"
  mint-soft: "#DDFBEF"
  on-mint-soft: "#111111"
  lilac: "#C084FC"
  on-lilac: "#111111"
  lilac-soft: "#F3E8FF"
  on-lilac-soft: "#111111"
```

## Typography

Tipografi, karakteristik **Bricolage Grotesque** başlıklarla güçlü bir görsel imza kurarken, işlevsel metinlerde **DM Sans** ve tarih/maaş/etiket verilerinde **Space Mono** kullanır.

```yaml
typography:
  display-lg:
    fontFamily: "Bricolage Grotesque"
    fontSize: 36px
    fontWeight: 800
    lineHeight: 42px
    letterSpacing: -0.5px
  display-lg-mobile:
    fontFamily: "Bricolage Grotesque"
    fontSize: 28px
    fontWeight: 800
    lineHeight: 34px
    letterSpacing: -0.25px
  headline-lg:
    fontFamily: "Bricolage Grotesque"
    fontSize: 22px
    fontWeight: 800
    lineHeight: 28px
    letterSpacing: -0.25px
  headline-md:
    fontFamily: "Bricolage Grotesque"
    fontSize: 17px
    fontWeight: 700
    lineHeight: 22px
    letterSpacing: 0px
  title-sm:
    fontFamily: "Bricolage Grotesque"
    fontSize: 15px
    fontWeight: 700
    lineHeight: 20px
    letterSpacing: 0px
  body-md:
    fontFamily: "DM Sans"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 21px
    letterSpacing: 0px
  body-sm:
    fontFamily: "DM Sans"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 19px
    letterSpacing: 0px
  label-md:
    fontFamily: "DM Sans"
    fontSize: 13px
    fontWeight: 700
    lineHeight: 18px
    letterSpacing: 0px
  mono-sm:
    fontFamily: "Space Mono"
    fontSize: 11px
    fontWeight: 700
    lineHeight: 16px
    letterSpacing: 0px
```

## Layout & Spacing

Masaüstünde maksimum 1440px genişlikte akışkan 12 sütunlu ve 5 sütunlu CSS Grid yapıları kullanılır. Tüm boşluklar 4px ve 8px katları üzerine kuruludur.

```yaml
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  2xl: 32px
```

## Elevation & Depth

Bulanık gölgeler yerine kesin **2px `#111111` kenarlıklar** ve sıfır bulanıklıklı sert ofset gölgeler (`4px 4px 0px #111111` kartlar ve paneller için, `2px 2px 0px #111111` butonlar ve rozetler için) kullanılır.

## Shapes

Kartlar ve paneller için belirgin `12px`, butonlar ve iç etiketler için `8px`, küçük rozetler için `4px` köşe yuvarlatması uygulanır.

```yaml
rounded:
  sm: 4px
  DEFAULT: 8px
  md: 8px
  lg: 12px
  xl: 16px
  full: 9999px
```

## Motion & Micro-interaction

Etkileşimler mekanik ve anlıktır; butonlar üzerine gelindiğinde veya basıldığında sert gölge yönünde 1px yer değiştirerek fiziksel bir tuş hissi verir.

```yaml
motion:
  press:
    duration: 100ms
    delay: 0ms
    timingFunction: ease-out
  surface-enter:
    duration: 180ms
    delay: 0ms
    timingFunction: cubic-bezier(0.2, 0, 0, 1)
```

## Voice & Content Strategy

Arayüz dili Türkçe, kısa, eylem odaklı ve nettir. Butonlarda "Yeni Başvuru", "Detayı Aç", "CSV Dışa Aktar" gibi doğrudan sonucu anlatan ifadeler kullanılır. Tüm rakamlar, maaşlar ve tarihler `tabular-nums` veya `Space Mono` ile hizalanır.

## Components

Component implementations live as individual HTML sticker sheet files in
`components/`. Each file contains the canonical, styled HTML components with
`<!-- COMPONENT: name -->` comment markers. Read each file before use.

- **Button** → `@components/button.html`: `button-primary`, `button-icon`, `button-with-icon`
- **Card** → `@components/card.html`: `card-elevated`, `card-action`, `card-interactive`, `card-interactive-2`
- **Table** → `@components/table.html`: `table-standard`, `table-interactive`, `table-selectable`
- **Typography** → `@components/typography.html`: `typography-display`, `typography-body`, `typography-label`
