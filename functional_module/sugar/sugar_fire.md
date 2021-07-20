# Sugar 火焰感應模組

![](./images/flame1.png)

這是一隻火焰感應模組，可以檢測火焰的強度。背後亦設有塑膠積木孔，可以完美配搭塑膠積木使用。

## 產品參數

- 尺寸：24 x 24 x 23 mm
- 重量：6.7g
- 訊號：模擬信號0~1023/0~4095

## 產品接線

用3Pin 連接線將模組與Robotbit Edu連接起來。

![](./images/poten2.png)

## 編程教學

### Kittenblock 編程教學

![](./images/flame3.png)

### MicroPython 編程教學

    Flame(pin)
    value()

- value(): 模擬信號0~1023/0~4095

參考程式

    from future import *
    
    from sugar import *
    
    flame_P0 = Flame('P0')
    
    x = 0
    
    screen.sync = 0
    while True:
      screen.fill((0, 0, 0))
      screen.text(flame_P0.value(),5,10,2,(0, 119, 255))
      screen.refresh()

