## 🚀 Usage

### Appraising the TLD for Use as a Business Card Site

```dart
final appraiser = Appraiser.personalBusinessCard();
print(appraiser.appraiseTld('com'));
```

```text
YES
```

### All suitable TLDs for Use as a Business Card Site

```dart
final appraiser = Appraiser.personalBusinessCard();
final yesFilter = appraiser.filter([Grade.YES, Grade.Yes, Grade.yes]);
print(yesFilter);
```

Grade relevance: `YES` > `Yes` > `yes`.

```text
{biz: YES, black: YES, com: YES, contact: YES, cool: YES, dad: YES, me: YES, one: YES, online: YES, page: YES, space: YES, best: Yes, bio: Yes, center: Yes, co: Yes, fan: Yes, gay: Yes, ink: Yes, io: Yes, it: Yes, life: Yes, live: Yes, net: Yes, pro: Yes, site: Yes, soy: Yes, website: Yes, win: Yes, actor: yes, art: yes, au: yes, band: yes, bike: yes, bingo: yes, blog: yes, boo: yes, business: yes, buzz: yes, ca: yes, cab: yes, cc: yes, cheap: yes, com.au: yes, com.mx: yes, digital: yes, direct: yes, dog: yes, expert: yes, family: yes, fun: yes, gallery: yes, glass: yes, global: yes, gold: yes, green: yes, guide: yes, guru: yes, hair: yes, holiday: yes, in: yes, info: yes, irish: yes, jp: yes, lat: yes, limited: yes, limo: yes, love: yes, men: yes, monster: yes, mx: yes, nexus: yes, ninja: yes, nl: yes, place: yes, plus: yes, pub: yes, quest: yes, red: yes, rest: yes, run: yes, ski: yes, skin: yes, social: yes, solar: yes, uk: yes, uno: yes, us: yes, vegas: yes, vision: yes, watch: yes, world: yes, xyz: yes, zip: yes, zone: yes}
```

## Extending

To set own grades or/and own "_domain suitablitity filter_" use this table:

- Google Drive [Business Card Suite / Domain aim (suitability)](https://docs.google.com/spreadsheets/d/19pdLp-b3vX9dGn3TsSvFMT5G0sdyfOhI6_Bmcdxju-I)

and the folder `src/suitabilities`.
