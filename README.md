# -LED
 Η φωτοαντίσταση μετράει το φως (αναλογική είσοδος).  Αν είναι σκοτάδι, το LED ανάβει.  Αν υπάρχει φως, το LED σβήνει.

int sensorPin = A0;  
int ledPin = 9;      
int sensorValue = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  sensorValue = analogRead(sensorPin);
  Serial.println(sensorValue);

  if (sensorValue < 500) {
    digitalWrite(ledPin, HIGH); 
  } else {
    digitalWrite(ledPin, LOW); 
  }
  delay(100);
}

