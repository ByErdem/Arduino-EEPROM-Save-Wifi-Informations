# Arduino-EEPROM-Save-Wifi-Informations
This code used for wifi name and password.

#include "EEPROM.h";

void setup() {
  // put your setup code here, to run once:
    Serial.begin(9600);

    int a=21;
    int b1 =1;
    char str[]= "wifi_adi|wifi_sifresi";
    int c;

    EEPROM.write(0,a);
    Serial.print("Kayit basarili");


    c=EEPROM.read(0);
    Serial.print(c);

    for(int i = 1; i < a+1; i++){

    EEPROM.write(i,str[i-1]);

    Serial.print(str[i-1]);
  
  }
  
  for(int i = 1; i<c+1;i++)
  {
    char okunan = EEPROM.read(i);
    Serial.print(okunan);
  }
  
}

void loop() {


} 

