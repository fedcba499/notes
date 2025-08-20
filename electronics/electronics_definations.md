## What is Relation between Voltage, Resistance and Current?
The relation between voltage (V), current (I) and resistance (R) is given by Ohm's Law:
> V = I x R

- Voltage (V) measured in volts is like the "pressure" pushing electric charges through a circuit. water pressure.
- Resistance (R) measured in ohms is the opposition to the flow of electric current. Like someone putting / applying pressure on pipe using leg / hand. thickness/narrowness of the pipe. 
- Current (I) measured in Amphere is the flow of electric charges (like water flow in a pipe). in water it is Liters per second. in Electric Current it is Amphere ( 1 A = 1 Coulomb per second ). 1 Couloumb = 6.242 x 10 power 18 electrons.

## What is voltage divider? How resistance reduces voltage? How to calculate voltage?
**Voltage Divider** is a circuit that uses resistors to reduce a larger input voltage to a smaller output voltage. A Voltage Divider consists of two resistors connected in series accross a voltage source. The Output Voltage is taken from the connection point between the two resistors.

Vin ——[R1]——•——[R2]——— Ground
            |
          Vout

**Formula** Vout = Vin x (R2/(R1+R2))
- The output voltage is always a fraction of input voltage
- It R1 = R2, then Vout = Vin /2 (Half the input Voltage)
- Larger R2 relative to R1 gives higher output voltage
- Larger R1 relative to R2 gives lower output voltage
- The circuit works because voltage diveds proportionally based on resistance ratios.



| UART | I2C | SPI |
| --- | --- | --- |
| Universal Async Rx Tx | Inter Integrated Circuit | Serial Peripheral Interface |
| 2 Pins | SDA, SCL | MISO, MOSI, CS, CLK |
| 115200 baud | 400 kHz | 10 MBPS |
| Async | Sync | Async |

