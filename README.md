# LED_Monitor_System
using embedded software C (keil c51 )

💡 Design a System to Monitor the Logical Status of LED using Embedded C

🎯 Objective
  To design and develop a system that monitors the logical status of an LED using an (8051 microcontroller ). The LED’s ON/OFF status changes according to the logic level of a microcontroller port pin.


⚙️ Components & Software Used
- Microcontroller: AT89C51  
- Software: Keil µVision (C51)  

🧩 Circuit Description
- LED anode is connected to Port 1.0 (P1.0) via a resistor.  
- LED cathode is connected to Ground (GND).  
- When `P1.0 = 1`, LED glows (Logic HIGH).  
- When `P1.0 = 0`, LED is OFF (Logic LOW).

---

💻 Embedded C Program

#include <reg51.h>

void delay(unsigned int x)
{
    unsigned int i;
    for(i = 0; i < x; i++);  // Simple software delay
}

void main()
{
    P1 = 0x00;  // Initialize Port 1 (all LEDs off)
    while(1)
    {
        P1 = ~P1;     // Toggle LEDs
        delay(50000); // Visible delay in simulation
    }
}

}
