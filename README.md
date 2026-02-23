<div align="center">
  <h1>Sofle RGB Wireless Mechanical Keyboard</h1>
  <h5>ZMK Config for PandaKB soflergb-mx v1</h5>
</div>

![sofle-rgb](./assets/sofle_rgb.jpg)

## Hardware alvo

- Teclado: **PandaKB soflergb-mx v1**
- MCU: **nice!nano (nRF52840)**
- Split BLE com suporte a uso **wired (USB) no lado central**
- OLED SSD1306 via I2C
- Encoder EC11
- ZMK Studio habilitado
- **RGB/LED desabilitado por decisão de projeto**

## Build local

```bash
~/.local/bin/west build -p -d build/left  -s zmk/app -b nice_nano//zmk -- -DSHIELD=sofle_left  -DZMK_CONFIG=$PWD/config
~/.local/bin/west build -p -d build/right -s zmk/app -b nice_nano//zmk -- -DSHIELD=sofle_right -DZMK_CONFIG=$PWD/config
```

## Flash (lado esquerdo/direito)

- **Left**: use o `.uf2` gerado em `build/left/zephyr/zmk.uf2` no microcontrolador do lado esquerdo.
- **Right (central)**: use o `.uf2` gerado em `build/right/zephyr/zmk.uf2` no microcontrolador do lado direito.

## Central/peripheral e uso USB

- O lado **RIGHT** é o **central**.
- O lado **RIGHT** mantém `CONFIG_ZMK_USB=y` para operação cabeada via USB.
- O lado **LEFT** é peripheral e não expõe USB.

## ZMK Studio

- `CONFIG_ZMK_STUDIO=y` habilitado.
- A tecla `&studio_unlock` está na camada **raise**, na linha de thumbs.

## OLED (SSD1306)

- Configurações habilitadas: `CONFIG_ZMK_DISPLAY`, `CONFIG_I2C`, `CONFIG_SSD1306`.
- O display usa nó `oled` do shield Sofle via I2C, com `zmk,display = &oled` no lado central.
- Endereço padrão configurado: **0x3C** (alguns módulos usam **0x3D**).
- Geometria padrão: **128x32** (caso seu módulo seja 128x64, ajuste `height`).

## Encoder (EC11)

- Configurações habilitadas: `CONFIG_EC11`, `CONFIG_ZMK_ENCODER`.
- Encoders ativados no Devicetree por lado.
- Keymap de sensores:
  - Base: volume down/up
  - Raise: page down/up

## RGB / LEDs

- Recursos de RGB e LEDs permanecem desabilitados.
- Não há underglow/ws2812 habilitado nesta configuração.

## License

[MIT](https://choosealicense.com/licenses/mit/)
