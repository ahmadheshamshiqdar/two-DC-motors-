# two-DC-motors-
i coudn't find L289D on tinkecard there for i used L293D 
I connected the power and ground wires  is the describe in the Piece port 
after that i connected the contorl ports enA12 for in1 and in2 and did the same for the other side enA34 for in3 and in4, now every thing is ready 
i connected the two motores to the output ports 
and for the codes i did put the int for the pins whice is enA12 enA34 and in1 in2 in3 in4 and then made the loop 
the code :- 
---------------------------------------------------------------------------------start---------------------------------------------------------------------------------------------
int enA12 = 10;
int in1 = 9;
int in2 = 11;
int enA34 = 7;
int in3 = 6;
int in4 = 8;


void setup() {
 // put your setup code here, to run once:
 pinMode(enA12, OUTPUT);
 pinMode(in1, OUTPUT);
 pinMode(in2, OUTPUT);
 pinMode(enA34, OUTPUT);
 pinMode(in3, OUTPUT);
 pinMode(in4, OUTPUT);
}

void loop() {
 //Stage 1 – 100% speed
 analogWrite(enA12, 255);
 digitalWrite(in1, HIGH);
 digitalWrite(in2, LOW);
 analogWrite(enA34, 255);
 digitalWrite(in3, HIGH);
 digitalWrite(in4, LOW);
 delay(5000);
  
 //Stage 2 – 70% speed
 analogWrite(enA12, 0.7*255);
 digitalWrite(in1, HIGH);
 digitalWrite(in2, LOW);
 analogWrite(enA34, 0.7*255);
 digitalWrite(in3, HIGH);
 digitalWrite(in4, LOW);
 delay(5000);
  
  //Stage 3 - 50% speed with 5 sec delay

  
  
  
 //Stage 4 – 100% speed reversing the direction
 analogWrite(enA12, 255);
 digitalWrite(in1, LOW);
 digitalWrite(in2, HIGH);
 analogWrite(enA34, 255);
 digitalWrite(in3, LOW);
 digitalWrite(in4, HIGH);
 delay(5000);
  
 //Stage 5 – 70% speed with 5 sec delay in reverse



  
  //Stage 6 – 50% speed reversing the direction in reverse
  analogWrite(enA12, 255);
 digitalWrite(in1, LOW);
 digitalWrite(in2, HIGH);
 analogWrite(enA34, 255);
 digitalWrite(in3, LOW);
 digitalWrite(in4, HIGH);
 delay(5000);
  


}
---------------------------------------------------------------------------------END-------------------------------------------------------------------------------------------
the link :- 
https://www.tinkercad.com/things/k3jkIwMRbdA-amazing-waasa/editel?sharecode=7VsGp0hMa3-NIQ1Ht4RBKG0Ewt0N7T9P4C3bKELDzOc
