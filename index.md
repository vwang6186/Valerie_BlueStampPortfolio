# Third Eye for the Blind
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Valerie W | Westmont | Computer Science | Incoming Senior


![Headstone Image](portrait.png)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone

Code:
```c++
const int trigPin = 12;
const int echoPin = 10;
const int switchPin = 5;


void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(switchPin, OUTPUT);
  tone(switchPin, 1000, 2000);
}

void loop() {
 
  long duration, inches, cm;

  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);

  inches = microsecondsToInches(duration);
  cm = microsecondsToCentimeters(duration);

  Serial.print(inches);
  Serial.print("in, ");
  Serial.print(cm);
  Serial.print("cm");
  Serial.println();

  if(cm <= 14 && inches <= 5)
  {
    tone(switchPin, 784);
    digitalWrite(switchPin, HIGH);
    delay(1000);
    Serial.println("in condition 1");
  }
    else if(cm <= 24 && inches <= 10)
    {
       tone(switchPin, 698);
       delay(1000);
       Serial.println("in condition 2");
    }
    else if(cm <= 34 && inches <= 15)
    {
      tone(switchPin, 659);
      delay(1000);
      Serial.println("in condition 3");
    }
    else if(cm <= 44 && inches <= 20)
    {
      tone(switchPin, 587);
      delay(1000);
      Serial.println("in condition 4");
    }
    else if(cm <= 55 && inches <= 25)
    {
      tone(switchPin, 523);
      delay(1000);
      Serial.println("in condition 5");
    }
    else if(cm <= 65 && inches <= 30)
    {
      tone(switchPin, 494);
      delay(1000);
      Serial.println("in condition 6");
    }
  else
  {
    noTone(switchPin);
    digitalWrite(switchPin, LOW);
  }

  delay(100);
}

long microsecondsToInches(long microseconds) {
  return microseconds / 74 / 2;
}

long microsecondsToCentimeters(long microseconds) {
  return microseconds / 29 / 2;
}
```

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project

Code:
```c++
const int trigPin = 12;
const int echoPin = 10;
const int switchPin = 5;

void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(switchPin, OUTPUT);
  tone(switchPin, 1000, 2000);
}

void loop() {
  long duration, inches, cm;
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);

  inches = microsecondsToInches(duration);
  cm = microsecondsToCentimeters(duration);

  Serial.print(inches);
  Serial.print("in, ");
  Serial.print(cm);
  Serial.print("cm");
  Serial.println();

  if(cm < 7 && inches < 4)
  {
    tone(switchPin, 784);
    digitalWrite(switchPin, HIGH);
  }
  else
  {
    noTone(switchPin);
    digitalWrite(switchPin, LOW);
  }
  delay(100);
}

long microsecondsToInches(long microseconds) {
    return microseconds / 74 / 2;
}

long microsecondsToCentimeters(long microseconds) {
    return microseconds / 29 / 2;
}
```


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++

```

# Materials Used
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **material** | **price** | **link** |
|:--:|:--:|:--:|
| safety glasses | $2.19 | <a href="https://www.amazon.com/MCR-Safety-CL010-Checklite-Glasses/dp/B009SRXSUA/ref=sr_1_4crid=2Y64BGOBG6GJH&keywords=mcr+safety+cl110+checklite+safety+glasses+with+clear+frame&qid=1688655520&sprefix=mcr+safety+cl110+checklite+safety+glasses+with+clear+frame%2Caps%2C144&sr=8-4"> Link </a> |
| solderless breadboard | $9.98 | <a href="https://www.amazon.com/EL-CP-003-Breadboard-Solderless-DistributionConnecting/dp/B01EV6LJ7G/ref=sr_1_3crid=1ELWX0HNETCH&keywords=elegoo+3pcs+breadboard+830+point+solderless+prototype+pcb+board+kit&qid=1688655674&sprefix=elegoo+3+pcs+brea%2Caps%2C166&sr=8-3"> Link </a> |
| breadboard jumper wires assorted kit | $13.35 | <a href="https://www.amazon.com/QISF-Breadboard-PreformedAntiStaticElectronics/dp/B088WNZXFQ/ref=sr_1_5crid=SX3Y99PVBCPD&keywords=breadboard+jumper+wire+assorted+kit&qid=1688655766&sprefix=breadboard+jumper+wire+assorted+kit%2Caps%2C129&sr=8-5"> Link </a> |
| precision wire stripper | $5.50 | <a href="https://www.amazon.com/Eclipse-CP-301G-ProsKit-Precision-Stripper/dp/B005JVJDIA/ref=sr_1_2?crid=1EBVRQ45Q1ML9&keywords=eclipse+tools+cp-301g+pro%27skit+precision+wire+stripper%2C+30-20+awg&qid=1688655846&sprefix=eclipse+tools+%2Caps%2C151&sr=8-2"> Link </a> |
| gorilla dual temp mini hot glue gun kit | $17.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Gorilla-8401509-Hot-Glue-Sticks/dp/B07K791YRP/ref=sr_1_1?crid=2MEANWQH01O3G&keywords=gorilla+dual+temp+mini+hot+glue+gun&qid=1689609320&sprefix=gorilla+dual+temp%2Caps%2C198&sr=8-1)"> Link </a> |
| circuit board breadboard | $6.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/HiLetgo-Finished-Prototype-Circuit-Breadboard/dp/B00FXHXT80/ref=sr_1_3?crid=ANK8O51Y30Q2&keywords=hiletgo+20+pcs+solder+finished+prototype+PCB+for+diy+5x7&qid=1689609444&sprefix=hiletgo+20+pcs+solder+finished+prototype+pcb+for+diy+5x7%2Caps%2C154&sr=8-3)"> Link </a> |
| female pin headers | $6.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Yohii-Female-Headers-2-54mm-Single/dp/B07PLBC2GT/ref=sr_1_3?crid=1PVFU2AMYA9S3&keywords=dahszhi%2Bfemale%2Bpin%2Bheaders%2B2.54mm&qid=1689609521&sprefix=dahszhi%2Bfemale%2Bpin%2Bheaders%2B2.54mm%2Caps%2C144&sr=8-3&th=1)"> Link </a> |
| VELCRO one-wrap roll | $7.98 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/VELCRO-Brand-ONE-WRAP-Double-Sided-Multi-Purpose/dp/B000078CUB/ref=sr_1_3?crid=1RLVMU74HRSLJ&keywords=velcro+one+wrap+roll+double+sided%2C+self+gripping&qid=1689609636&sprefix=velcro+one+wrap+roll+double+sided%2C+self+gripping%2Caps%2C155&sr=8-3)"> Link </a> |
| ultrasonic sensor module for arduino | $9.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/WWZMDiB-Ultrasonic-Sensor-Raspberry-HC-SR04/dp/B0C166NX3Z/ref=sr_1_8?crid=385710WVR1GS6&keywords=ultrasonic+sensor+module+for+arduino&qid=1689618009&sprefix=ultrasonic+sensor+module+for+arduino%2Caps%2C164&sr=8-8)"> Link </a> |
| electronic alarm passive buzzer sounder | $7.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/a15091400ux0103-Electronic-Mounting-Passive-Sounder/dp/B018I1WBNQ/ref=sr_1_1?crid=1AS2F4MZNZK6Y&keywords=uxcell+electronic+alarm+PCB+panel&qid=1689618282&sprefix=uxcell+electronic+alarm+pcb+panel%2Caps%2C159&sr=8-1)"> Link </a> |
| toggle switch vertical slide switch | $5.39 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/HiLetgo-SS-12D00-Toggle-Switch-Vertical/dp/B07RTJDW27/ref=sr_1_8?crid=L0HK00P6RPZF&keywords=hiletgo+20+pcs+toggle+switch+vertical&qid=1689618351&sprefix=hiletgo+20+pcs+toggle+switch+vertical%2Caps%2C154&sr=8-8)"> Link </a> |
| pitch single row pin header strip | $5.49 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/HiLetgo-20pcs-2-54mm-Single-Header/dp/B07R5QDL8D/ref=sr_1_1_sspa?crid=DDFUU6L5KWD2&keywords=hiletgo+20+pc+pitch+single+row+pin+header+strip&qid=1689618421&sprefix=hiletgo+20+pc+pitch+single+row+pin+header+stri%2Caps%2C218&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)"> Link </a> |
| LED dlode lights assortment kit | $5.88 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Diffused-Lighting-Electronics-Components-Emitting/dp/B01C3ZZT2I/ref=sr_1_3?crid=2ZHLWCX7TX7NB&keywords=chanzon+60+pcs+6+colors+x+10+pcs+5mm+led+diode+lights&qid=1689618481&sprefix=chanzon+60+pc%2Caps%2C197&sr=8-3)"> Link </a> |
| arduino micro with headers | $17.95 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Arduino-Micro-Headers-A000053-Controller/dp/B00AFY2S56/ref=sr_1_3?crid=2RLU2IGONQXSS&keywords=arduino+micro+with+headers&qid=1689618608&sprefix=arduino+micro+wit%2Caps%2C189&sr=8-3)"> Link </a> |
| digital multimeter | $12.49 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Etekcity-Multimeter-MSR-R500-Electronic-Multimeters/dp/B01N9QW620/ref=sr_1_1_sspa?crid=2E8YMTD5RKZD5&keywords=etekcity%2Bdigital%2Bmultimeter&qid=1688655187&sprefix=etekcity%2Bdigital%2Bmultimeter%2Caps%2C166&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1)"> Link </a> |
| portable charging bank | $17.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Anker-PowerCore-Ultra-Compact-High-Speed-Technology/dp/B01CU1EC6Y/ref=asc_df_B01CU1EC6Y/?tag=hyprod-20&linkCode=df0&hvadid=312111908612&hvpos=&hvnetw=g&hvrand=18094504964760026445&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-523807968135&psc=1)"> Link </a> |
| soldering iron kit | $19.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Soldering-Iron-Kit-Temperature-Desoldering/dp/B07S61WT16/ref=sr_1_6?crid=28E849CUD7Q9G&keywords=soldering+iron+kit+soldering+iron+60+w&qid=1689619086&sprefix=soldering+iron+kit+soldering+iron+60+w%2Caps%2C163&sr=8-6)"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
