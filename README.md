# Electrical-Circuit-Design-and-Simulation-Lesson-8
##Proteusta ARDUİNO çalıştırma
### Kodyazıldı led yakıldı topraklama yapılarak ;
        void setup() {
        pinMode(2,OUTPUT);
        }
        
        void loop() {
        digitalWrite(2,HIGH);
        delay(100);
        digitalWrite(2,LOW);
        delay(100);
    }
<img width="1277" height="774" alt="image" src="https://github.com/user-attachments/assets/7e388729-8273-44e0-86a6-bd38da29074a" />
### 7 SEGMENT
        // 7 segment display segment pinleri
        int a = 2;
        int b = 3;
        int c = 4;
        int d = 5;
        int e = 6;
        int f = 7;
        int g = 8;
        
        // Her rakam için segment durumları (common cathode için)
        byte digits[10][7] = {
          {1, 1, 1, 1, 1, 1, 0}, // 0
          {0, 1, 1, 0, 0, 0, 0}, // 1
          {1, 1, 0, 1, 1, 0, 1}, // 2
          {1, 1, 1, 1, 0, 0, 1}, // 3
          {0, 1, 1, 0, 0, 1, 1}, // 4
          {1, 0, 1, 1, 0, 1, 1}, // 5
          {1, 0, 1, 1, 1, 1, 1}, // 6
          {1, 1, 1, 0, 0, 0, 0}, // 7
          {1, 1, 1, 1, 1, 1, 1}, // 8
          {1, 1, 1, 1, 0, 1, 1}  // 9
        };
        
        int segmentPins[7] = {a, b, c, d, e, f, g};
        
        void setup() {
          // Segment pinlerini çıkış olarak ayarla
          for (int i = 0; i < 7; i++) {
            pinMode(segmentPins[i], OUTPUT);
          }
        }
        
        void loop() {
          for (int i = 0; i < 10; i++) {
            displayDigit(i);
            delay(1000); // 1 saniye bekle
          }
        }
        
        // Belirtilen rakamı göster
        void displayDigit(int digit) {
          for (int i = 0; i < 7; i++) {
            digitalWrite(segmentPins[i], digits[digit][i]);
          }
        }



<img width="1326" height="788" alt="image" src="https://github.com/user-attachments/assets/33f486fc-fea4-4b9e-8564-cba8aad8c4ec" />

## Transistor BJT
PNP VE NPN içinde NPN kullanılır en çok.

### BC237 
<img width="1134" height="840" alt="image" src="https://github.com/user-attachments/assets/eed826ed-9828-4de4-b97c-be0fac9d78d4" />
### BC556AP
<img width="916" height="752" alt="image" src="https://github.com/user-attachments/assets/51e29fc1-f6a2-4e58-b532-313467fee1bb" />

###LDR (Light Dependent Resistor)
projede Torch_ldr,2 tane direnç,1 led ,BC237,cell,topraklama

<img width="1297" height="606" alt="image" src="https://github.com/user-attachments/assets/580fe763-659e-473c-bfe9-9431b3dcc66a" />



