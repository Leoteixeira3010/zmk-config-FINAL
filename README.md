<div align="center">
  <h1>Sofle RGB Wireless Mechanical Keyboard</h1>
  <h5>ZMK Config for Sofle RGB</h5>
</div>

![sofle-rgb](./assets/sofle_rgb.jpg)

## Flash split (left/right)

Para este repositório, o papel de cada metade é:

- `sofle_left` = **central**
- `sofle_right` = **peripheral**

### Ordem recomendada de flash e pareamento BLE

1. **Flash da metade central (`sofle_left`)**
   - Grave o UF2 gerado para `sofle_left` na placa que ficará no lado esquerdo.
2. **Flash da metade peripheral (`sofle_right`)**
   - Grave o UF2 gerado para `sofle_right` na placa que ficará no lado direito.
3. **Pareamento entre metades (split BLE)**
   - Ligue as duas metades após o flash.
   - Aguarde alguns segundos para o pareamento BLE interno do split acontecer.
4. **Pareamento com o host (PC/celular)**
   - Coloque o teclado em modo de pareamento e conecte no host pela metade **central**.

> Dica: quando possível, comece o teste com apenas a metade central ligada ao host e depois ligue a peripheral.

### Diagnóstico rápido

Se as teclas aparecerem **espelhadas/invertidas**, verifique se cada UF2 foi gravado no lado correto:

- UF2 de `sofle_left` na metade esquerda (central)
- UF2 de `sofle_right` na metade direita (peripheral)

## Parts list

- [Sofle RGB](https://github.com/josefadamcik/SofleKeyboard)
- 2 x [nice!nano microcontrollers](https://nicekeyboards.com/nice-nano/)
- 4 x Custom acrylic plates with additional 10 x M2 screws for tenting
- 2 x Glorious GMMK Pro Rotary Knobs
- 2 x LiPo 130mAh 401230 JST Batteries
- 58 x Boba U4T
- 58 x XDA Keycaps

## License

[MIT](https://choosealicense.com/licenses/mit/)
