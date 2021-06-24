const int  echo = 13;
const int trig = 12;
const int RELAY_PIN = 4; // Arduino pin connected to Relay's pin
const int buzzer = 9;

int duration;
int distance;

void setup() {
  pinMode(trig, OUTPUT);
  pinMode(echo, INPUT); 
  pinMode(RELAY_PIN, OUTPUT);
  pinMode(buzzer, OUTPUT);
  pinMode(7, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(5, OUTPUT);
  Serial.begin(9600);
  delay(50);

}

void loop() {
  digitalWrite(trig, LOW);
  delayMicroseconds(2);
  
  digitalWrite(trig, HIGH);
  delayMicroseconds(2000);
  digitalWrite(trig, LOW);

  duration = pulseIn(echo, HIGH);
  distance = (duration*0.034/2)+2;
  delay(20000); //here delay is used to get a stable reading from the sensor 
  if(distance <= 130 & distance > 60){
    digitalWrite(RELAY_PIN, LOW);
    digitalWrite(buzzer,LOW);
    digitalWrite(7, LOW);
    digitalWrite(6, LOW);
    digitalWrite(5, HIGH);
  }
  else if (distance <= 60 & distance > 28 ){
    digitalWrite(RELAY_PIN, LOW);
    digitalWrite(buzzer,LOW);
    digitalWrite(7, LOW);
    digitalWrite(6, HIGH);
    digitalWrite(5, HIGH);
  }  
  else{
    digitalWrite(RELAY_PIN, HIGH);
    digitalWrite(buzzer,HIGH);
    digitalWrite(7, HIGH);
    digitalWrite(6, HIGH);
    digitalWrite(5, HIGH);
    
  }
  Serial.println(distance);
  delay(1000);
  // put your main code here, to run repeatedly:
}
