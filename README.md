# Musical-New-Year-Effects-with-Arduino-and-Piezo-Buzzer
Example code for creating musical New Year effects with Arduino and a piezo buzzer.
#define NOTE_C4 262
#define NOTE_D4 294
#define NOTE_E4 330
#define NOTE_G4 392
#define NOTE_A4 440
#define NOTE_B4 494

int melody[] = { NOTE_E4, NOTE_D4, NOTE_C4, NOTE_D4, NOTE_E4, NOTE_E4, NOTE_E4, NOTE_D4, NOTE_D4, NOTE_D4, NOTE_E4, NOTE_G4, NOTE_G4, NOTE_G4, NOTE_G4 };
int noteDurations[] = { 4, 8, 8, 4, 4, 8, 8, 4, 4, 4, 4, 4, 4, 4, 4 };

void setup() {
    for (int thisNote = 0; thisNote < 15; thisNote++) {
        int noteDuration = 1000 / noteDurations[thisNote];
        tone(8, melody[thisNote], noteDuration);
        int pauseBetweenNotes = noteDuration * 1.30;
        delay(pauseBetweenNotes);
        noTone(8);
    }
}

void loop() {
    // Code for other New Year effects
}
