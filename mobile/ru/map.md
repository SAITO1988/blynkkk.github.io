
### Карта (Map)

Виджет Карты позволяет устанавливать точки/флажки на карте со стороны оборудования. Это очень полезный виджет, если у вас есть несколько устройств, и вы хотите отслеживать их позиции на карте.

Вы можете отправить точку на карту с помощью обычной команды виртуальной записи:

```cpp
Blynk.virtualWrite(V1, pointIndex, lat, lon, "Название");
```

Мы также создали оболочку, чтобы вы могли упростить использование виджета Карты.
Вы можете изменить метки флажков на оборудовании с помощью кода:

```cpp
WidgetMap myMap(V1);
...
int index = 1;
float lat = 51.5074;
float lon = 0.1278;
myMap.location(index, lat, lon, "Название");
```

Использование уникальных ```index``` позволяет вам переопределить существующее значение точки.

**Пример кода:** [Базовый пример Карты](https://github.com/blynkkk/blynk-library/blob/master/examples/Widgets/Map/Map.ino)