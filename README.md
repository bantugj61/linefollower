# linefollower
Contains codes for line follower robot

int motor1 = 9;  
int motor2 = 6;
int motor3 = 11;
int motor4 = 10;
int enA = A0;
int enB = A5;

int sensor1=2;
int sensor2=3;
int sensor3=4;
int sensor4=5;
int sensor5=7;

void setup()
{
  pinMode(motor1, OUTPUT);
  pinMode(motor2, OUTPUT);
  pinMode(motor3, OUTPUT);
  pinMode(motor4, OUTPUT);
  pinMode(enA,  OUTPUT);
  pinMode(enB,  OUTPUT);
  pinMode(sensor1, INPUT);
  pinMode(sensor2, INPUT);
  pinMode(sensor3, INPUT);
  pinMode(sensor4, INPUT);
  pinMode(sensor5, INPUT);
  

}
void loop()
{
  sensor1 = digitalRead(2);
  sensor2 = digitalRead(3);
  sensor3 = digitalRead(4);
  sensor4 = digitalRead(5);
  sensor5 = digitalRead(7);

  if (sensor1 == HIGH && sensor2 == LOW && sensor3 == LOW && sensor4 == LOW && sensor5 == LOW)
  {
    digitalWrite(motor2,HIGH);
    digitalWrite(motor4,LOW);
    analogWrite(enA, 180);
    analogWrite(enB, 0);

    delay(20);
  }
 else if (sensor1 == HIGH && sensor2 == LOW && sensor3 == LOW && sensor4 == LOW && sensor5 == HIGH)
 {
  digitalWrite(motor2,HIGH);//forward
  digitalWrite(motor4,HIGH);
  analogWrite(enA, 230);
  analogWrite(enB, 230);
 }
 else if (sensor1 == HIGH && sensor2 == LOW && sensor3 == LOW && sensor4 == HIGH && sensor5 == HIGH)
{
  digitalWrite(motor2,HIGH);// forward
  digitalWrite(motor4,HIGH);
  analogWrite(enA, 195);
  analogWrite(enB, 200);
  
}
else if (sensor1 == HIGH && sensor2 == HIGH&& sensor3 == LOW && sensor4 == LOW && sensor5 == HIGH)
{
   digitalWrite(motor2,HIGH);// forward
   digitalWrite(motor4,HIGH);
   analogWrite(enA, 200); //left
   analogWrite(enB, 197);  //right
}
else if (sensor1 == LOW && sensor2 == LOW&& sensor3 == LOW && sensor4 == LOW && sensor5 == HIGH)
{
    digitalWrite(motor2,LOW);
    digitalWrite(motor4,HIGH);
    analogWrite(enA,0);
    analogWrite(enB,180);  //right

    delay(20);
}
else if (sensor1 == LOW && sensor2 == LOW&& sensor3 == LOW && sensor4 == LOW && sensor5 == LOW)
{
    digitalWrite(motor2,HIGH);
    digitalWrite(motor4,HIGH);
    analogWrite(enA,180);
    analogWrite(enB,180);
    delay(20);
}
else if (sensor1 == HIGH && sensor2 == HIGH&& sensor3 == LOW && sensor4 == HIGH && sensor5 == HIGH)
{
    digitalWrite(motor2,HIGH);
    digitalWrite(motor4,HIGH);
    analogWrite(enA,250);
    analogWrite(enB,250);
}
else if (sensor1 == LOW && sensor2 == HIGH&& sensor3 == HIGH && sensor4 == HIGH && sensor5 == HIGH)
{
    digitalWrite(motor2,LOW);
    digitalWrite(motor4,HIGH);
    analogWrite(enA,0);
    analogWrite(enB,180);
   
}
else if (sensor1 == HIGH && sensor2 == HIGH&& sensor3 == HIGH && sensor4 == HIGH && sensor5 == LOW)
{
    digitalWrite(motor2,HIGH);
    digitalWrite(motor4,LOW);
    analogWrite(enA, 120);
    analogWrite(enB, 0);
   
}
else if (sensor1 == LOW && sensor2 == LOW&& sensor3 == HIGH && sensor4 == HIGH && sensor5 == HIGH)
{
    digitalWrite(motor2,LOW);
    digitalWrite(motor4,HIGH);
    analogWrite(enA,0);
    analogWrite(enB,180); //right

    delay(20);
}
}
