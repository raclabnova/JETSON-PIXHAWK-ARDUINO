Arduino, Jetson’a USB kablosu ile bağlıdır ve Arduino Mega kullanılmaktadır.

Pixhawk (Cube Orange), Arduino Mega’nın TX (18) ve RX (19) pinleri üzerinden TELEM2 portuna bağlanır. TELEM2 bağlantısında yalnızca TX, RX ve GND hatlarını Arduino’ya bağlamak yeterlidir.

ÇOK ÖNEMLİ!!!!!! JETSON ile ARDUİNO ARASI HABERLEŞME MAVPROXY başlatıyoruz, ARDUİNO ile PİXHAWK arası MAVLink.h kütüphanesi ile yapıyoruz.


PWM komutları Arduino üzerinden verilecekse, QGroundControl programı kullanılarak motorlara ait SERVOx_FUNCTION ayarlarının RCIN1, RCIN2 gibi girişlere atanmış olmalıdır.

Örnek ayarlar:

SERVO1_FUNCTION = RCIN1

SERVO2_FUNCTION = RCIN2

Bu ayar yapılmazsa dışarıdan gönderilen PWM komutları motorlara ulaşmaz.


Eğer Pixhawk üzerinden mod değiştirmek veya joystick ile hareket kontrolü yapmak isteniyorsa,SERVOx_FUNCTION ayarları QGroundControl üzerinden MOTOR1, MOTOR2 gibi tanımlanmalıdır. 

Örnek ayarlar:

SERVO1_FUNCTION = MOTOR1

SERVO2_FUNCTION = MOTOR2

Bu durumda motorlar Pixhawk tarafından doğrudan kontrol edilir.
