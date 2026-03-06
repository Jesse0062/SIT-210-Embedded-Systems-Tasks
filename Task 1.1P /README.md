// If we follow the code along we see when button is pushed the the sequence begins. Ive started the code by declaring a few varibles just to make the code slightly more modular if I wanted to change where the inputs where coming from at a later date the code would be able to be changed easily. 




int led1 = 12;   // first LED
int led2 = 7;    // second LED
int button = 2;  // push button

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(button, INPUT_PULLUP);  // button input
}

void loop() {

  if (digitalRead(button) == HIGH) {   // button pressed 

    // First LED ON for 30 seconds
    digitalWrite(led1, HIGH);
    delay(30000);
    digitalWrite(led1, LOW);

    // Second LED ON for 60 seconds
    digitalWrite(led2, HIGH);
    delay(60000);
    digitalWrite(led2, LOW);

  } else {
    // Keep LEDs off when button not pressed
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
  }

}
