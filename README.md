# Project1
Project Presentation Link
https://tome.app/soma-9ae/untitled-tome-clno035n300tyo87bqfergv9d


int laserPin = 2; // Digital pin for the laser module
int ldrPin = A0;  // Analog pin for the LDR
int alarmPin = 7; // Digital pin for the alarm

void setup() {
  pinMode(laserPin, OUTPUT);
  pinMode(alarmPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int ldrValue = analogRead(ldrPin);
  if (ldrValue < 100) { // Adjust this threshold according to your setup
    digitalWrite(alarmPin, HIGH);
    Serial.println("Intruder detected!");
  } else {
    digitalWrite(alarmPin, LOW);
  }
}

