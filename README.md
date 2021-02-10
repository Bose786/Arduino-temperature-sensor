# Arduino-temperature-sensor
void setup()
{
  Serial.begin(9600);
  pinMode(A0,INPUT);
}
void loop()
{
  int sensorValue =analogRead(A0);
  float volt=(sensorValue/1023.0)*5.0;
  float temp =(volt-0.5)*100;
  Serial.println(temp);
  delay(1000);
 
}
