<div align="center">
  <h1>Sofle RGB Wireless Mechanical Keyboard</h1>
  <h5>ZMK Config for Sofle RGB</h5>
</div>

![sofle-rgb](./assets/sofle_rgb.jpg)

## Parts list

- [Sofle RGB](https://github.com/josefadamcik/SofleKeyboard)
- 2 x [nice!nano microcontrollers](https://nicekeyboards.com/nice-nano/)
- 4 x Custom acrylic plates with additional 10 x M2 screws for tenting
- 2 x Glorious GMMK Pro Rotary Knobs
- 2 x LiPo 130mAh 401230 JST Batteries
- 58 x Boba U4T
- 58 x XDA Keycaps


## Split layout details

- **Lado central (central): esquerdo (`sofle_left`)**
  - USB habilitado
  - Papel `CONFIG_ZMK_SPLIT_ROLE_CENTRAL`
- **Lado periférico: direito (`sofle_right`)**
  - Conecta via BLE ao lado central

### Periféricos por metade

- **Esquerda**: display OLED (I2C) e 1 encoder rotativo
- **Direita**: display OLED (I2C) e 1 encoder rotativo

## License

[MIT](https://choosealicense.com/licenses/mit/)
