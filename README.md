
## feat/nice-view-socket (2026-11-26)

Corne-style nice!view install (per Beekeeb hidden-wire pattern), adapted to
Kyria rev3 + nice!nano after a full ZMK pin audit:

| nice!view pin | Connection |
|---|---|
| GND, VCC | existing OLED socket power pins |
| SCK | OLED socket SDA/SCL net D2 (nice!nano P0.17) |
| MOSI | OLED socket second net D3 (P0.20) |
| CS | ONE hidden wire to nice!nano pin at D9 position (P1.06), tucked under the display |

Underglow/per-key LED DIN bit-bangs from D1 (P0.06) = the factory Kyria LED
net. D0 (P0.08) reserved for possible future wired split. Matrix verified:
ZMK kyria_rev3 uses pro_micro 4-10,14-21 only; D0-D3/D9 are free.
