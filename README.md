# Домашнее задание к занятию "12.3 Развертывание кластера на собственных серверах, лекция 1"
## Расчет всех необходимых ресурсов.

```
БД 12 Gb 3 Core
Кэш 12 GB 3 Core 
Front 0,25 Gb 1 Core
Back 6 Gb 10 Core

Сумм 31Gb 17 Core
```

## Служебные ресурсы к нодам
```
Control plane 4 Gb 2 Core 50Gb для 3 нод 
Worker node 1 Gb 1 Core 100GB
```
## Подбор рабочих нод, которые справятся с такой нагрузкой, с учетом резерва
```
10 * 3 Core = 30 Core > (17+10*1 = 27) 3 Cores reserv

8 * 4Gb + 2 * 8Gb = 48 Gb > (31+10*1 = 41) 7 Gb reserv

Volume: 10*100 = 1Tb 

```
## Cлужебные ресурсы к нодам
```
т.к. нод 10 думаю с ними справятся 3 Control plane с 8 Gb 4 core 50 Gb 
```

## Итог:
```
Control plane 8Gb 4 Core 50Gb - 3шт.
Worker node 4Gb 3 Core 100Gb - 8шт.
Worker node 8Gb 3 Core 100Gb - 2шт.
```
