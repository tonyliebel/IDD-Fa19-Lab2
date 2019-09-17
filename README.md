# Digital Timer
 
Include your responses to the bold questions below. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as README.md pages on your GitHub, and post a link to that on your main class hub page.

## Part A. Solder your LCD panel

**Take a picture of your soldered panel and add it here!**

## Part B. Writing to the LCD
 
**a. What voltage level do you need to power your display?**
3.3v
**b. What voltage level do you need to power the display backlight?**
   5v
**c. What was one mistake you made when wiring up the display? How did you fix it?**
I wired up the display completely backwards (i.e. had the pins oriented the wrong way as I connected the display to the arduino) Took me some time to figure out why nothing would work, and I'm happy nothing broke!
**d. What line of code do you need to change to make it flash your name instead of "Hello World"?**
 lcd.print()
**e. Include a copy of your Lowly Multimeter code in your lab write-up.**
// initialize the library by associating any needed LCD interface pin
// with the arduino pin number it is connected to
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);
int sensorPin = A0;    // select the input pin for the potentiometer
int sensorValue = 0;  // variable to store the value coming from the sensor

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD. 
    lcd.print("Pot Voltage:");

}

void loop()
{
    // Read sensor value
  int sensorValue = analogRead (A0);
  float voltage = sensorValue * (5.0 /1023.0);

    // Display voltage
  lcd.setCursor (0, 1);
  lcd.print(voltage);

  delay (10);
  
}

## Part C. Using a time-based digital sensor

**Upload a video of your working rotary encoder here.**


## Part D. Make your Arduino sing!

**a. How would you change the code to make the song play twice as fast?**
 Shorten the note duration by half for each note, as well as reduce the PauseBetweenNotes command from 1.3 to 1.15
 
**b. What song is playing?**
Happy Birthday!


## Part E. Make your own timer

**a. Make a short video showing how your timer works, and what happens when time is up!**

**b. Post a link to the completed lab report your class hub GitHub repo.**
