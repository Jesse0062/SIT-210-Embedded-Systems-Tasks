int led = 12;

// dot = short blink
void dot() {
  digitalWrite(led, HIGH);
  delay(200);
  digitalWrite(led, LOW);
  delay(200);
}

// dash = long blink
void dash() {
  digitalWrite(led, HIGH);
  delay(600);
  digitalWrite(led, LOW);
  delay(200);
}

void setup() {
  pinMode(led, OUTPUT);
  pinMode(2, INPUT);
}

void loop() {

  if(digitalRead(2)== HIGH) { // if button is pressed

    // J (.---)
    dot(); dash(); dash(); dash();
    delay(600);

    // E (.)
    dot();
    delay(600);

    // S (...)
    dot(); dot(); dot();
    delay(600);

    // S (...)
    dot(); dot(); dot();
    delay(600);

    // E (.)
    dot();

    delay(2000); // pause before repeating
  }
  else { // if button is not pressed
    digitalWrite(led, LOW); // keep LED off
  }

}
