# Описание пакета gs_logger

## Описание:
Данный пакет предоставляет инструменты для взаимодействия с логом сообщений между RPi и Pioneer

## Состав пакета:
Классы:
* Logger

## Описание классов:

### 1. Logger

#### Инициализация:
Без параметров

#### Поля:
* __log_service - rospy.ServiceProxy: gs_interfaces.srv.Log
* __log_sub - rospy.Subscriber: std_msgs.msg.String

#### Методы:
* lastMsgs - возвращает последнее сообщение лога
* allMsgs - возвращает весь лог

#### Используемые сервисы:
* geoscan/get_log (gs_interfaces/Log)

#### Используемые топики:
* geoscan/log (std_msgs/String)

## Необходимые пакеты:
ROS:
* gs_interfaces
* gs_core
* std_msgs

## Примечание:
Все классы в данном пакете могут быть использованы только при запущеной ноде ros_plaz_node.py из пакета gs_core